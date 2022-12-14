# What the CAF

# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 04 - Automated Governance Reporting and Best Practice Validation (1hr)

In this challenge you will be implementing [AzGovViz](https://github.com/JulianHayward/Azure-MG-Sub-Governance-Reporting) which is a PowerShell based script that iterates your Azure Tenant´s Management Group hierarchy down to Subscription level. It captures most relevant Azure governance capabilities such as Azure Policy, RBAC and Blueprints and a lot more. As part of this challenge you will be using [PSRule for Azure](https://azure.github.io/PSRule.Rules.Azure/features/) which is aligned to the Azure Well-Architected Framework (WAF). Tests called "rules" check the configuration of Azure resources against WAF principles.

>Since Azure Resource Manager sometimes caches configurations and data to improve performance, it can sometimes take up to 30 minutes for changes to take effect when you assign roles or remove role assignments.

## Challenge 04 - Success criteria:

1. Take your time and read the setup guide. And read the note above! If you need to create new identities and assign roles do it now.
2. Setup AzGovViz with GitHub Actions using OIDC.
3. Configure AzGovViz to use "PSRule for Azure".
4. Publishing the AzGovViz HTML to an Azure Web App.
5. Export to CSV your PSRule results.

---

## 
