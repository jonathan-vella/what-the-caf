# What the CAF
# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 1 - Azure landing zone conceptual architecture deployment

In this challenge you will be deploying one of the Reference implementations located in this [repository](https://github.com/Azure/Enterprise-Scale) using the Azure Portal experience.
There other deployment options based on Bicep and Terraform but the Portal-based experience is the quickest way to deploy the ALZ conceptual architecture, and yep there are some trade offs which we will discuss.

Success criteria for this challenge:

- Plan and document the IP addressing for the Hub network. Customer will be leveraging at least Azure Firewall, Azure VPN Gateway, and Azure Bastion. In your plan, clearly document subnet names, whether the use of NSGs and / or UDRs is allowed by Azure, and the minimum recommended subnet size. Inlcude references to online documentation. You can either use the provided [template](/learning_path_modules/04_ALZ_Accelerator/sources/Azure%20Network%20Documentation%20Template.xlsx) or build your own.
- Document the deployment process by creating a high-level workflow including pre-requisites related to AAD permissions, min. number of subscriptions, subscription naming convention and renaming, etc.
- Deploy the AdventureWorks reference implementation.

- **Do not deploy** the integrated CICD pipeline

---

## Challenge 2 - IaC with GitHub Actions

In this challenge you will be manually creating a CICD pipeline which will allow you to operate the Azure platform using [AzOps](https://github.com/Azure/AzOps) (IaC with GitHub Actions).

This PowerShell module is rooted in the principle that everything in Azure is a resource and to operate at-scale, it should be managed declaratively to determine target goal state of the overall platform. Guidance for this challenge is located [here](https://github.com/azure/azops/wiki/github-actions).

Success criteria for this challenge:

- Configure AzOps via Portal or command-line script
- Initiate the first Pull workflow
- Validate AzOps by making sure that the Azure hierarchy that got created using ARM templates as part of the Enterprise-Scale setup, such as management groups, subscription organization as well as policy definitions, policy assignments and role assignments are hydrated and organized into Git.
- Using GitHub, create a new [Policy Assignment](https://github.com/Azure/Enterprise-Scale/wiki/Deploying-Enterprise-Scale-Platform-DevOps#create-new-policy-assignment-for-validation) and validate the assignment thru the Azure Portal.
- Using GitHub, create a new Role Assignment on the "Sandbox" management group which grants members of the AAD group "Sandbox Contributors" contributor access at the management group level and validate the assignment thru the Azure Portal.

## Challenge 2a - PaC with GitHub Actions

In this challenge you will be using Policy-As-Code to modify a policy definition which is blocking you from creating the Azure Bastion Subnet.

- In your hub network, try to create the Azure Bastion Subnet. Azure Policy should block the operation.
- Using GitHub, modify the policy which is enforcing the use of Network Security Groups. You are not allowed to change the policy effect. A deny is a deny.
- Create the Azure Bastion Subnet.

## Challenge 2b - Azure Best Practices and Trade-Offs

In this challenge you will be using Policy-As-Code to modify a policy definition which is blocking you from creating the Azure Bastion Subnet.

- In your subscription, try to create a new Virtual Network. Azure Policy should block the operation.
- Discuss findings and possible solutions (e.g., change Azure Policy effect to "Audit", explore the use of Policy Exemptions, Azure Virtual Network Manager, etc.) with your peers and coach.

---

## Challenge 3 - Azure VM BCDR at scale

In this challenge you will be deploying an Azure Virtual Machine in the same region as your Hub network which will be auto-enabled for backup and DR on creation using Azure Policy. Explore the possibility of using tags to associate backup and DR policies via Azure Policy.

Success criteria for this challenge:

- Configure Azure Backup (e.g., vault, backup policy, etc.)
- Configure Azure Policy to auto-enable backup on VM creation
- Configure Azure Site Recovery (e.g., vault, policy, etc.)
- Configure Azure Policy to auto-enable DR on VM creation
- Deploy an Azure VM
- VM is enabled for BCDR (Azure Backup and Azure Site Recovery) via Azure Policy

---

## Challenge 4 - Governance Reporting

In this challenge you will be implementing [AzGovViz](https://github.com/JulianHayward/Azure-MG-Sub-Governance-Reporting) which is a PowerShell based script that iterates your Azure Tenant´s Management Group hierarchy down to Subscription level. It captures most relevant Azure governance capabilities such as Azure Policy, RBAC and Blueprints and a lot more. From the collected data AzGovViz provides visibility on your HierarchyMap, creates a TenantSummary, creates DefinitionInsights and builds granular ScopeInsights on Management Groups and Subscriptions.

Success criteria for this challenge:

- Setup AzGovViz from the console or GitHub Codespaces
- Run AzGovViz, show and tell your findings to your coach.
- If time permits, publish AzGovViz HTML output to an Azure WebApp.

---

## Challenge 5 - Azure Design Review

In this challenge you will be doing an Azure design review to double-check that best practices are being followed. You will be using this [repo](https://github.com/Azure/review-checklists) which contains code and examples to operationalize spreadsheet-based checklists that can be used for Azure design reviews on multiple technologies.

Success criteria for this challenge:

- Use the Excel spreadsheet, import the latest checklist, and explore the contents of the file.
- Review all checklist items with a "high" severity.

---

## Challenge 6 - Azure Environment Clean-up

In this challenge, you will be exploring all possible options available to you to clean up your Azure environment to minimize costs.

Success criteria for this challenge:

- Identify the resources whcih you have to delete.
- Discuss the impact of deleting these resources.
- Delete the resources identified in Step 1.
- Delete the ESLZ deployment.
- Invite your coach for end-of-day beers!

---

