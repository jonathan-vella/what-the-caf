# What the CAF

# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 01 - ALZ deployment (2hrs)

In the first part of this challenge you will be deploying one of the Reference implementations located in this [repository](https://github.com/Azure/Enterprise-Scale) using the Azure Portal experience. There other deployment options based on Bicep and Terraform but the Portal-based experience is the quickest way to deploy the ALZ conceptual architecture, and yep there are some trade offs which we will discuss.

In the second part of this challenge you will be documenting how you will meet Contoso's business and technical objectives.

---

## Challenge 01 - Success criteria

1. Plan and document the IP addressing for the Hub network. Customer will be leveraging at least Azure Firewall, Azure VPN Gateway, and Azure Bastion. In your plan, clearly document subnet names, whether the use of NSGs and / or UDRs is allowed by Azure, and the minimum recommended subnet size. You must include references to online documentation. You can either use the provided [template](/learning_path_modules/04_ALZ_Accelerator/sources/Azure%20Network%20Documentation%20Template.xlsx) or build your own.
2. Document the deployment process by creating a high-level workflow including pre-requisites related to AAD permissions, min. number of subscriptions, subscription naming convention and renaming, etc.
3. Deploy the Contoso reference implementation.
4. **Do not deploy** the integrated CICD pipeline

---

## Challenge 01a - Success criteria

1. Document and share with your coach what you believe should be the minimum requirements and level of information you need have at hand to deploy the ALZ accelerator. Think of tenants, priviliged identities, security contacts, IP addresses, etc.
2. What will you use to help the customer easily create cost-related reports for each workload based on department, owner, and environment? And how will you apply it?
3. How will you implement the customer's regulatory & compliance requirements? You must include links to relevant documentation which supports your approach.
4. How are you going to make sure that M-Series and L-Series VMs can only be deployed in the SAP environments without impacting agility and scale?
5. How will ensure that "development environments and associated VNETs are not able to communicate with production"?

---
