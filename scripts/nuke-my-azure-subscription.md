# Clean up your entire Azure subscription aka Nuke-My-Azure

**Proceed with extreme caution**

This a very effiicient way to clean up resources in an Azure subscription. 

Disclaimer: I (or my employer) cannot be held responsible for any loss of data resulting from executing the commands below.

---

#### Use variables to define your target environment.

```powershell
$subscription = 'my subscription name'
$filter = 'filter e.g. ilc*'
```

#### Set the subscription context.

```powershell
Set-AzContext -Subscription $subscription
```

#### Verify that the resource group filter is working.

```powershell
Get-AzResourceGroup | ? ResourceGroupName -match $filter | Select-Object ResourceGroupName
```

#### Async delete the filtered Azure Resource Groups

```powershell
Get-AzResourceGroup | ? ResourceGroupName -match $filter | Remove-AzResourceGroup -AsJob -Force
```

#### Or don't use any filters and really nuke everything.

```powershell
Get-AzResourceGroup | Remove-AzResourceGroup -AsJob -Force
```

#### Monitor progress.

```powershell
Get-Job
```

#### Optionally remove all policy assignments.

```powershell
get-AzPolicyAssignment | Remove-AzPolicyAssignment
Get-AzPolicySetDefinition -custom | Remove-AzPolicySetDefinition -force
Get-AzPolicyDefinition -custom | Remove-AzPolicyDefinition -force
```

---
