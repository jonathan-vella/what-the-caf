# What the CAF

# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 03a - Azure VM BCDR at scale

In this challenge you will be deploying an Azure Virtual Machine in the same region as your Hub network. This VM should be auto-enabled for backup and DR on creation using Azure Policy. Explore the possibility of using tags to associate backup and DR policies via Azure Policy.

## Challenge 03a - Success Criteria

1. Configure Azure Backup (e.g., vault, backup policy, etc.)
2. Configure Azure Policy to auto-enable backup on VM creation but to also audit for non-compliance
3. Configure Azure Site Recovery (e.g., vault, policy, etc.)
4. Configure Azure Policy to auto-enable DR on VM creation but to also audit for non-compliance
5. Deploy an Azure VM and make sure that the VM is enabled for BCDR (Azure Backup and Azure Site Recovery) via Azure Policy

---

## Challenge 03b - Azure SQL DB BCDR at scale

In this challenge you will be creating a custom Azure Policy definition which can audit the PITR backup configuration of Azure SQL Database and / or if the PITR is not set to the user-specified number of days (e.g., 7 days), the policy will remediate this setting.

## Challenge 03b - Success Criteria

1. Create an Azure Policy definition which can support the auditing and / or configuration of Azure SQL Database PITR. You can use the code located [here](https://raw.githubusercontent.com/jonathan-vella/scripts-and-policies/master/Azure%20Policy/Deploy%20Azure%20SQL%20DB%20ShortTerm%20Backup.json) to create this policy or write your own.
2. Create the required Azure Policy assignments
3. Create an Azure SQL Database and monitor the impact of the Azure Policy in scope for this challenge.

---


