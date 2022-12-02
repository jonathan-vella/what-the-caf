# What the CAF

# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 02 - IaC with GitHub Actions (90mins)

In this challenge you will be manually creating a CICD pipeline which will allow you to operate the Azure platform using [AzOps](https://github.com/Azure/AzOps) and [GitHub Actions](https://github.com/skills/hello-github-actions).

This PowerShell module is rooted in the principle that everything in Azure is a resource and to operate at-scale, it should be managed declaratively to determine target goal state of the overall platform. Guidance for this challenge is located [here](https://github.com/azure/azops/wiki/github-actions).

## Challenge 02 - Success Criteria

1. Every action in Azure must be performed by an identity. Read all 5 points in this challenge and using the concept of least privilige, identify the RBAC role you must use and the scope assignment for the idenitity you will be using. **Do not proceed before discussing your solution with your coach**
2. You must configure AzOps via Portal (or command-line script!) and initiate the first Pull workflow.
3. Validate AzOps by making sure that the Azure hierarchy that got created using ARM templates as part of the ALZ setup, such as management groups, subscription organization as well as policy definitions, policy assignments and role assignments are hydrated and organized into Git.
4. Using GitHub, create a new [Policy Assignment](https://github.com/Azure/Enterprise-Scale/wiki/Deploying-ALZ-Platform-DevOps#operating-the-azure-platform-using-azops-infrastructure-as-code-with-github-actions) and validate the assignment thru the Azure Portal. **Do not update the Azure Policy assignment to Enforce!**
5. Using GitHub, create a new Role Assignment on the "Sandbox" management group which grants members of the AAD group "Contoso Sandbox Contributors" contributor access at the management group level and validate the assignment thru the Azure Portal.

---

## Challenge 02a - PaC with GitHub Actions

In this challenge you will be using Policy-As-Code to modify a policy definition which is blocking you from creating the Azure Bastion Subnet.

## Challenge 02a - Success Criteria

1. In your hub network, try to create the Azure Bastion Subnet. Azure Policy should block the operation. Read carefully the output of the error message.
2. Using GitHub (or VS Code but not the Azure Portal) modify the policy which is enforcing the use of Network Security Groups. You are not allowed to change the policy effect. A deny is a deny. Hint: Read the Policy definition.
3. You should be now be able to create the Azure Bastion Subnet (but not Azure Bastion).

---

