# What the CAF

# Module 03 - Migrate Like A Pro Hackathon

## Challenge 04 - Migrate

In this challenge you will be migrating  the webserver and the Ubuntu WAF to Azure IaaS and the database to Azure SQL DB (unless you have already done so at an earlier stage).

We don't provide any additional information - we want to first hear your concept and after the concept is discussed, we want your team to migrate to PaaS in Azure. 

---

Challenge 04 - Success Criteria

1. On-premises servers are replicated to Azure. 
2. Document at a high-level your migration approach incl. estimated downtime & mandatory changes to the application (if any). Remember that the customer loves PaaS and security - what else can we quickly refactor?
3. Share your approach with your coach wait for "GO" before proceeding with migration. 
4. Migrate the workload to Azure.
5. The SmartHotel application must be accessible over the internet using HTTPS

---

Have in mind, there are a number of post-migration steps that should be completed before the migrated services is ready for production use.
These include:

- Validation that the Azure VM agent is deployed.
- Enabling backup and disaster recovery at scale
- Encrypting VM disks at scale
- Ensuring the network is properly secured
- Ensuring proper subscription governance is in place, such as role-based access control and Azure Policy
- Reviewing recommendations from Azure Advisor and Azure Defender for Cloud
- Cleaning up migration resources

.
