# What the CAF

# ALZ Accelerator Customer Scenario

## Contoso Corporation

### Company background & information

- They are a localized brand focusing on wholesale, distribution and retail having their HQ in Athens with warehouses, distribution centres & shops located across the entire Greek territory.
- The CEO demands that no data is stored outside of the EU.
- Due to COVID-19 they are looking to migrate all workloads to Microsoft Azure.
- They are currently hosting all of their workloads on VMware vSphere and have 2 main sites - Athens (Prod DC) and Thessaloniki (DR DC)
- Circa 75 VMs for Prod, less than 20 for Dev / Test.
- COVID-19 triggered a heavy investment in their online presence which is now one of the key revenue stream for the business.
- They have a separate payment service which is subject to PCI-DSS.
- They have a MPLS connection between both DCs; some warehouses and disti. centers also act as internet breakout points for their shops.
- They are already using Microsoft 365 services.

### Technical details

- They have an active Enterprise Agreement covering all Microsoft software.
- They have a mix of Microsoft 365 E3 and E5 licenses.
- They have 2 Azure subscriptions in use by developers as a sandbox.
- The on-premises AD DS domain is synchronized to AAD.
- They have a network team with strong skills in Cisco, Checkpoint, and F5.
- Some of the IT staff are trained and certified in Microsoft Azure (AZ-900, AZ-104, AZ-204 and some AZ-305, but no AZ-500 and no AZ-700).
- They have limited expertise and experience with ARM Templates, GitHub, Azure DevOps.
- They have dedicated 10.0.0.0/16 as the IP address space for all networks in Azure.

### Requirements

- The first workload to be migrated to Azure is the SAP production landscape; migration must be completed in less than 6 weeks due to capacity and reliability issues with their datacenters. Customer recently experienced capacity-related outages which resulted in unexpected downtime and data loss.
- They want to be able to easily create cost-related reports for each workload based on department, owner, and environment.
- They want to minimize their existing on-premises footprint and want to replace the existing MPLS solution with a 'cloud-based' approach.
- They want to start allowing local internet breakout from all sites to improve SaaS application performance and reduce the load on their WAN.
- They require the ability to deny certain Azure Resources and or Services. For example, a must-have is "No M-Series or L-Series VMs can be deployed except for the SAP environments".
- They require separate Production, Staging & Development environments for security, agility and cost purposes. But they do not want to have development environments and associated VNETs to be able to communicate with production. Also, developers must granted "unrestricted" access to development environments at scale with minimal administrative overhead.
- All production VMs must be backed up, and some selected VMs in dev/test environments also need to be protected.
- They require built-in platform regulatory compliance security checks and reporting for all production environments (PCI-DSS, ISO27001, CIS etc.)
  - ISO27001 for all environments except Sandbox subscriptions.
  - PCI-DSS for the payment system.
- All Subnets must be protected with NSGs and cannot be disabled.
- Azure Activity Logs for all Subscriptions & Diagnostic settings for all Azure Resources should be enabled automatically and sent to a centralized LAW.
- TDE & Auditing should be enforced on all Azure SQL Databases.
- Azure Monitor VM Insights should be enabled on all VMs and any required agents automatically installed.
- No Public IP Addresses are allowed in the environment except for core network functionality, sandbox environments, and online applications.
- They should receive alerts related to abnornmal consumption, cost overruns, etc.
