# What the CAF

# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 02 - IaC with GitHub Actions

In this challenge you will be manually creating a CICD pipeline which will allow you to operate the Azure platform using [AzOps](https://github.com/Azure/AzOps) and h [GitHub Actions](https://github.com/skills/hello-github-actions).

This PowerShell module is rooted in the principle that everything in Azure is a resource and to operate at-scale, it should be managed declaratively to determine target goal state of the overall platform. Guidance for this challenge is located [here](https://github.com/azure/azops/wiki/github-actions).

## Challenge 02 - Success Criteria

1. Configure AzOps via Portal or command-line script
2. Initiate the first Pull workflow
3. Validate AzOps by making sure that the Azure hierarchy that got created using ARM templates as part of the Enterprise-Scale setup, such as management groups, subscription organization as well as policy definitions, policy assignments and role assignments are hydrated and organized into Git.
4. Using GitHub, create a new [Policy Assignment](https://github.com/Azure/Enterprise-Scale/wiki/Deploying-Enterprise-Scale-Platform-DevOps#create-new-policy-assignment-for-validation) and validate the assignment thru the Azure Portal.
5. Using GitHub, create a new Role Assignment on the "Sandbox" management group which grants members of the AAD group "Sandbox Contributors" contributor access at the management group level and validate the assignment thru the Azure Portal.

---

## Challenge 02a - PaC with GitHub Actions

In this challenge you will be using Policy-As-Code to modify a policy definition which is blocking you from creating the Azure Bastion Subnet.

## Challenge 02a - Success Criteria

1. In your hub network, try to create the Azure Bastion Subnet. Azure Policy should block the operation. Read the output of the error message.
2. Using GitHub (or VS Code but not the Azure Portal) modify the policy which is enforcing the use of Network Security Groups. You are not allowed to change the policy effect. A deny is a deny.
3. Create the Azure Bastion Subnet (but not Azure Bastion).

---

## Challenge 02b - Azure Best Practices and Trade-Offs

In this challenge you will be debating using Policy-As-Code to modify a policy definition which is blocking you from creating a new Virtual Network.

## Challenge 02b - Success Criteria

1. In your subscription, try to create a new Virtual Network. Azure Policy should block the operation.
2. Discuss findings and possible solutions (e.g., change Azure Policy effect to "Audit", explore the use of Policy Exemptions, Azure Virtual Network Manager, etc.) with your peers and coach.

---
