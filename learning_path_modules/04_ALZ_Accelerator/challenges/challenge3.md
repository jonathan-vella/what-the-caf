# What the CAF

# Module 04 - ALZ Accelerator Hackathon

---

## Challenge 03a - Azure VM BCDR at scale (45mins)

In this challenge you will auto-enable backup and disaster recovery on VM creation using Azure Policy. Remember that the customer's requirement is to have "all **production** VMs backed up, and **some** selected VMs in dev/test environments" to be protected at least on a weekly basis. Your solution must clearly address all of these requirements whilst minimizing management tasks and limiting the blast radius during incidents which require the use of Azure Backup.

>You can deploy the Azure VM and Azure SQL Db in the same region as your Hub network. Azure Policy assignments take up to 30 minutes to take effect.

## Challenge 03a - Success Criteria

1. Think before you act. Assess the existing Azure Policy assignments. Do you need to change anything? And which Azure Policy for Azure Backup are you going to use meet the customer's requirement?
2. Configure Azure Backup (e.g., vault, policy, etc.)
3. Configure Azure Policy to auto-enable backup on VM creation but to also audit for non-compliance
4. Configure Azure Site Recovery (e.g., vault, policy, etc.)
5. Configure Azure Policy to auto-enable DR on VM creation but to also audit for non-compliance
6. Deploy an Azure VM and make sure that the VM is enabled for BCDR (Azure Backup and Azure Site Recovery) via Azure Policy
7. In the Azure Portal, have a look at your VM's blade and note what else has the VM been automatically onboarded into.
8. Be able to answer these 2 questions: At which scope can these policies be applied? And what are you doing to clearly and easily identify "all **production** VMs backed up, and **some** selected VMs in dev/test environments"? 

---

## Challenge 03b - Azure SQL DB BCDR at scale (30mins)

In this challenge you will be creating a custom Azure Policy definition which can audit the PITR backup configuration of Azure SQL Database and / or if the PITR is not set to the user-specified number of days (e.g., 7 days), the policy will remediate this setting.

## Challenge 03b - Success Criteria

1. Create an Azure Policy definition which can support the auditing and / or configuration of Azure SQL Database PITR. You can use the code located [here](https://raw.githubusercontent.com/jonathan-vella/scripts-and-policies/master/Azure%20Policy/Deploy%20Azure%20SQL%20DB%20ShortTerm%20Backup.json) to create this policy or write your own.
2. Create the required Azure Policy assignments and perhaps exclude some others.
3. Create an Azure SQL Database and monitor the impact of the Azure Policy in scope for this challenge.

---


