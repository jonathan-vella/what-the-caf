# What the CAF

# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 01 - Azure landing zone conceptual architecture deployment

In this challenge you will be deploying one of the Reference implementations located in this [repository](https://github.com/Azure/Enterprise-Scale) using the Azure Portal experience.
There other deployment options based on Bicep and Terraform but the Portal-based experience is the quickest way to deploy the ALZ conceptual architecture, and yep there are some trade offs which we will discuss.

---

## Challenge 01 - Success criteria

1. Plan and document the IP addressing for the Hub network. Customer will be leveraging at least Azure Firewall, Azure VPN Gateway, and Azure Bastion. In your plan, clearly document subnet names, whether the use of NSGs and / or UDRs is allowed by Azure, and the minimum recommended subnet size. You must include references to online documentation. You can either use the provided [template](/learning_path_modules/04_ALZ_Accelerator/sources/Azure%20Network%20Documentation%20Template.xlsx) or build your own.

2. Document the deployment process by creating a high-level workflow including pre-requisites related to AAD permissions, min. number of subscriptions, subscription naming convention and renaming, etc.

3. Deploy the AdventureWorks reference implementation.

4. **Do not deploy** the integrated CICD pipeline

---
