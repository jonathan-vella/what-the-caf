# AzOps

## AzOps Accelerator Prerequisites

AzOps pipelines can use either a Service Principal, or a Managed Identity if running self-hosted build agents hosted in Azure. This guide walks through the prerequisites needed to setup your AzOps pipelines.

---

## Steps

- Install PowerShell Modules

- Define Variables - Service Principal Name and Management Group Name

- Connect to Azure

- Create a Service Principal

- Azure Role Assignment

- Add Service Principal/Managed Identity to Azure AD Directory Readers role

---

## Install PowerShell modules

- Install the latest version of [PowerShell 7](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2)

- Install Modules using these commands:

```powershell
Install-Module Az.Accounts, Az.Resources, Microsoft.Graph.Identity.DirectoryManagement, Microsoft.Graph.Applications
```

---

## Define Variables

```powershell
$servicePrincipalDisplayName = "<name of service principal>"
$managementGroupName = 'name of management group'
```

---

## Connect to Azure

```powershell
Connect-AzAccount
```

---

## Create a Service Principal

If you intend to run AzOps with hosted agents a Service Principal is required. Perform the steps below to create the Service Principal in Azure AD. If you plan to run with self-hosted agents and want to use a managed identity skip to the next step.

```powershell
$servicePrincipal = New-AzADServicePrincipal -DisplayName $servicePrincipalDisplayName
Write-Host "ARM_TENANT_ID: $((Get-AzContext).Tenant.Id)"
Write-Host "ARM_SUBSCRIPTION_ID: $((Get-AzContext).Subscription.Id)"
Write-Host "ARM_CLIENT_ID: $($servicePrincipal.AppId)"
Write-Host "ARM_CLIENT_SECRET: $($servicePrincipal.PasswordCredentials.SecretText)"
```

> Save the output from the script for later, it will be used when creating variables for your pipelines.

---

## Azure Role Assignment

#### Assign Azure role to management group scope

If you intend to only manage a subset of your Azure landscape, you can assign permissions at management group scope instead of root. Use the script below to assign permissions at management group level.

```powershell
$roleToAssign = 'Owner'
$ErrorActionPreference = 'Stop'
$servicePrincipal = Get-AzADServicePrincipal -DisplayName $servicePrincipalDisplayName
$managementGroup = Get-AzManagementGroup -GroupId $managementGroupName
New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName $roleToAssign -Scope $managementGroup.Id
```
#### OR
#### Assign Azure role to the tenant root (/) scope (ask yourself: do I really need this level of access?)

If you want to manage your entire Azure landscape using AzOps, assign the `Owner` role at the root `(/)` scope.

```powershell
$roleToAssign = 'Owner'
$ErrorActionPreference = 'Stop'
$servicePrincipal = Get-AzADServicePrincipal -DisplayName $servicePrincipalDisplayName
New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName $roleToAssign -Scope '/'
```

> You may need to elevate your access in Azure before being able to create a root scoped assignment.

---

## Azure AD role assignment

Assign `Directory Readers` role to Service Principal/Managed Identity.

```powershell
# Connect to Azure Active Directory
Connect-MgGraph -Scopes "Directory.Read.All,RoleManagement.ReadWrite.Directory"

# Get Service Principal from Azure Active Directory
$servicePrincipal = Get-MgServicePrincipal -Filter "DisplayName eq '$servicePrincipalDisplayName'"
if (-not $servicePrincipal) {
    Write-Error "$servicePrincipalDisplayName Service Principal not found"
}

# Add Azure Active Directory Role Member
$directoryRoleDisplayName = "Directory Readers"
$directoryRole = Get-MgDirectoryRole -Filter "DisplayName eq '$directoryRoleDisplayName'"
if (-not $directoryRole) {
    Write-Warning "$directoryRoleDisplayName role not found"
} else {
    $body = @{'@odata.id' = "https://graph.microsoft.com/v1.0/directoryObjects/$($servicePrincipal.Id)"}
    New-MgDirectoryRoleMemberByRef -DirectoryRoleId $directoryRole.id -BodyParameter $body
}
```

> If you receive a warning message "Directory Readers role not found." this can occur when the role has not yet been used in your directory. As a workaround, assign the role manually to the AzOps App from the Azure portal.


