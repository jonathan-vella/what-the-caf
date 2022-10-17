# What the CAF

# **Learning Path Agenda**

| Module                            | Duration | Target Roles      | Required Certifications                                                                                                                                                                                                                                                                                                                                                                                              | Recommended Certifications                                                                                                                                                                                                                                     | Recommended Self-Paced Learning                                                                                                                                                                                                    |
| --------------------------------- | -------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| *01-CAF 101*                      | 2-Days   | Sales & Technical | [AZ-900](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900)                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                | [The business value of Microsoft Azure](https://docs.microsoft.com/en-us/learn/paths/learn-business-value-of-azure/)                                                                                                               |
| *02-Strategy & Plan Hackathon*    | 1-Day    | Sales & Technical | Mod. 01 plus [AZ-900](https://docs.microsoft.com/en-us/learn/certifications/exams/az-900)                                                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                | CAF 101 or equivalent                                                                                                                                                                                                              |
| *03-Migrate Like A Pro Hackathon* | 2-Days   | Technical         | Mod. 02 plus [AZ-104](https://docs.microsoft.com/en-us/learn/certifications/exams/az-104)                                                                                                                                                                                                                                                                                                                            | [AZ-500](https://docs.microsoft.com/en-us/learn/certifications/exams/az-500), [AZ-700](https://docs.microsoft.com/en-us/certifications/exams/az-700), and [AZ-800 + 801](https://docs.microsoft.com/en-us/certifications/windows-server-hybrid-administrator/) | [Applications and infrastructure migration and modernization](https://docs.microsoft.com/en-us/learn/modules/app-and-infra-migration-and-modernization/)                                                                           |
| *04-ALZ Accelerator Hackathon*    | 2-Days   | Technical         | Mod. 03 plus [AZ-104](https://docs.microsoft.com/en-us/learn/certifications/exams/az-104) or [AZ-204](https://docs.microsoft.com/en-us/certifications/exams/az-204) or [DP-203](https://docs.microsoft.com/en-us/certifications/azure-data-engineer/), [AZ-500](https://docs.microsoft.com/en-us/learn/certifications/exams/az-500) and [AZ-305](https://docs.microsoft.com/en-us/learn/certifications/exams/az-305) | [AZ-400](https://docs.microsoft.com/en-us/learn/certifications/exams/az-400) and [AZ-700](https://docs.microsoft.com/en-us/learn/certifications/exams/az-700)                                                                                                  | [Azure Landing Zones \| Architectural Blueprint, Tooling & Best Practices Architecture](https://techcommunity.microsoft.com/t5/microsoft-mechanics-blog/azure-landing-zones-architectural-blueprint-tooling-amp-best/ba-p/3530857) |

---

## Azure subscription requirements

### **<u>Migrate Like A Pro Hackathon subscription: </u>**

- Azure subscriptions based on Azure Pass are not compatible with the hands-on labs for this hackathon.

- Compatible subscriptions include Azure in CSP, Enterprise Agreement, Pay As You Go, Visual Studio, and Azure Free Account with a Credit Card as per this [FAQ](https://azure.microsoft.com/en-us/free/free-account-faq/).

- The subscription must meet the quota requirements documented [here](https://github.com/jonathan-vella/MCW-Line-of-business-application-migration/blob/master/Hands-on%20lab/Before%20the%20HOL%20-%20Line-of-business%20application%20migration.md#requirements).

- The subscription can be shared across multiple teams as long as the number of resources required (e.g., Cores, vNets, etc.) are within the Azure subscription and service limits, quotas, and constraints.

### **<u>ALZ Accelerator Hackathon subscription: </u>**

- At least 1 Azure subscription per attendee is required; the recommendation is to have 2 Azure subscriptions per attendee.

- All subscriptions should be associated to a **non-production AAD tenant**.

- [Tenant root access](https://github.com/Azure/Enterprise-Scale/wiki/Deploying-Enterprise-Scale-Pre-requisites) is a mandatory requirement for this hackathon.

> Note: Azure subscriptions in CSP must have Azure Cost Management enabled as per this [document](https://docs.microsoft.com/en-us/azure/cost-management-billing/costs/get-started-partners)
>  

---

## Tooling Prerequisites

To avoid any delays with downloading or installing tooling, have the following ready prior to attending:

- A GitHub account.

- A modern laptop running the latest version of either Windows 10  or Window 11, Mac OS X 10.13 or higher, or Ubuntu 18.04 pr higher.

- Install your choice of Integrated Development Environment (IDE) software such as [Visual Studio Code](https://code.visualstudio.com/download)

- Download of the latest version of PowerShell 7, Az. PowerShell Modules, and [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)

- Make sure that the modules below are installed:
  
  ```powershell
  Install-Module Az.Accounts, Az.Resources, Microsoft.Graph.Identity.DirectoryManagement, Microsoft.Graph.Applications
  ```

- If you need to update them you can execute the following command:
  
  ```powershell
  Update-Module Az.Accounts, Az.Resources, Microsoft.Graph.Identity.DirectoryManagement, Microsoft.Graph.Applications
  ```

- Preferably, if using Windows, also install [WSL](https://docs.microsoft.com/en-us/windows/wsl/install)
