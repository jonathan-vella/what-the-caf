# The top technical skills for the modern IT Pro

There are many niche areas within infrastructure and security, but we find that most IT Pros have a very broad set of responsibilities, touching different products and tasks. If you’re working in a Microsoft-focussed environment, especially one that is using Azure, these are the tools and technologies to become familiar with.

## The Basics

Infrastructure concepts underpin so many technology workloads. Whether an application has been developed in-house from scratch, with backend databases on Windows Server and a front-end GUI, or whether it uses cloud components like Azure Functions - an IT Pro needs to understand how things like networking, identity, and security impact the application design, performance, and data protection. And aside from applications, there are a bunch of infrastructure-driven services that need maintaining, like file sharing, DHCP, DNS, and Group Policy, as well as Software-as-a-Service.

Start with a good understanding of the main concepts of:

### Networking

*Whether it's physical cabling and switches, or cloud networking configurations, topics like TCP/IP addressing are universal. As is a good, tidy patch panel.*

[Windows Server Network Infrastructure](https://docs.microsoft.com/learn/paths/windows-server-network-infrastructure/?WT.mc_id=modinfra-57414-socuff)

[Implement and operate an on-premises and hybrid networking infrastructure](https://docs.microsoft.com/learn/paths/implement-operate-premises-hybrid/?WT.mc_id=modinfra-57417-socuff)

[Configure and manage virtual networks](https://docs.microsoft.com/learn/paths/az-104-manage-virtual-networks/?WT.mc_id=modinfra-57417-socuff%20)

[Configuring Azure virtual network subnets with CIDR notation](https://techcommunity.microsoft.com/t5/itops-talk-blog/configuring-azure-virtual-network-subnets-with-cidr-notation/ba-p/2047809?msclkid=622e74a5b49911eca0719d39d2e2302f?WT.mc_id=modinfra-57417-socuff)

[Implement network security in Azure](https://docs.microsoft.com/learn/paths/implement-network-security/?WT.mc_id=modinfra-57417-socuff)

### Windows Server

*Contrary to popular belief, the cloud did not in fact remove the need for servers. Some of them went hybrid, some of them appeared as Azure VMs and some of them are being upgraded or deployed inside organisations all over the world. Huh.* 

[Windows Server deployment, configuration, and administration](https://docs.microsoft.com/learn/paths/windows-server-deployment-configuration-administration/?WT.mc_id=modinfra-57417-socuff)

[Windows Server files servers and storage management](https://docs.microsoft.com/learn/paths/windows-server-file-servers-storage-management/?WT.mc_id=modinfra-57417-socuff)

[Windows Server Hyper-V and Virtualization](https://docs.microsoft.com/learn/paths/windows-server-hyper-v-virtualization/?WT.mc_id=modinfra-57417-socuff)

[Implement disaster recovery in Windows Server on-premises and hybrid environments](https://docs.microsoft.com/learn/paths/implement-disaster-recovery-windows-server-premises/?WT.mc_id=modinfra-57417-socuff)

[Implement Windows Server high availability](https://docs.microsoft.com/learn/paths/implement-windows-server-high-availability/?WT.mc_id=modinfra-57417-socuff)

### Security

*Security is in everything, and many IT Pros don't have a dedicated security department. Understand the infrastructure configuration that contributes to a secure environment and the security tools that are available.* 

[Secure Windows Server on-premises and hybrid infrastructures](https://docs.microsoft.com/learn/paths/secure-windows-server-premises-hybrid-infrastructures/?WT.mc_id=modinfra-57414-socuff)

[Threat Modelling Security Fundamentals](https://docs.microsoft.com/learn/paths/tm-threat-modeling-fundamentals//WT.mc_id=modinfra-57417-socuff)

[Manage security operations in Azure](https://docs.microsoft.com/learn/paths/manage-security-operations/?WT.mc_id=modinfra-57417-socuff)

[Secure your data and applications](http://%20https//docs.microsoft.com/learn/paths/secure-your-data-applications/?WT.mc_id=modinfra-57417-socuff)

[Configure your Microsoft Sentinel environment](https://docs.microsoft.com/learn/paths/sc-200-configure-azure-sentinel-environment/?WT.mc_id=modinfra-57414-socuff)

### Identity

*With everyone wanting access to everything from everywhere, proving that you are really you is crucial to gaining access - and is often managed by IT Pros.* 

[Deploy and manage identity infrastructure](https://docs.microsoft.com/learn/paths/deploy-manage-identity-infrastructure/?WT.mc_id=modinfra-57417-socuff)

[Active Directory Domain Services](https://docs.microsoft.com/learn/paths/active-directory-domain-services/?WT.mc_id=modinfra-57417-socuff)

[Implement an initial Azure Active Directory environment](https://docs.microsoft.com/learn/paths/implement-identity-management-solution/?WT.mc_id=modinfra-57417-socuff)

[Implement an Authentication and Access Management solution](https://docs.microsoft.com/learn/paths/implement-authentication-access-management-solution//WT.mc_id=modinfra-57417-socuff)

[Plan and implement an identity governance strategy](https://docs.microsoft.com/learn/paths/plan-implement-identity-governance-strategy/?WT.mc_id=modinfra-57417-socuff)

### Monitoring and troubleshooting

*More than deployment, making sure systems are healthy and performing well is a large part of #ITProLife .... and then there's the detective work to figure out why they aren't.* 

[Monitor and troubleshoot Windows Server environments](https://docs.microsoft.com/learn/paths/monitor-troubleshoot-windows-server-environments/?WT.mc_id=modinfra-57417-socuff)

[Monitor the usage, performance, and availability of resources with Azure Monitor](https://docs.microsoft.com/learn/paths/monitor-usage-performance-availability-resources-azure-monitor/?WT.mc_id=modinfra-57417-socuff)

[Monitor and back up Azure resources](https://docs.microsoft.com/learn/paths/az-104-monitor-backup-resources/?WT.mc_id=modinfra-57417-socuff)

### Containers and Kubernetes

*This will depend on if your organization has embraced Containers yet, but if your developers come knocking on your door because they want some near your production environments, you'll know where to start.*

[Orchestrate containers on Windows Server using Kubernetes](https://docs.microsoft.com/learn/modules/orchestrate-containers-windows-server-using-kubernetes/?WT.mc_id=mofinra-57417-socuff)

[Create and manage containers using Docker and Kubernetes](https://docs.microsoft.com/learn/paths/az-400-create-manage-containers-using-docker-kubernetes/?WT.mc_id=modinfra-57417-socuff)

## Tools and Languages

As you deploy new resources, query logs or run commands at scale, there are a few scripting and automation tools and languages that can help. These are especially important for IT Pros who also manage cloud resources.

### PowerShell

*Need we say more? PowerShell is the love language of Exchange administrators, Active Directory administrators, Azure administrators and more! If you want to query some stuff or run commands at scale, learn PowerShell's structure and you're halfway there.*

[What is PowerShell?](https://docs.microsoft.com/powershell/scripting/overview?WT.mc_id=modinfra-57417-socuff)

[Automate administrative tasks by using PowerShell](https://docs.microsoft.com/learn/paths/powershell/?WT.mc_id=modinfra-57417-socuff)

[PowerShell GitHub Community](https://github.com/powershell/powershell?WT.mc_id=modinfra-57417-socuff)

### Kusto Query Language (KQL)

*All famous explorers need a query language, and you'll find KQL helpful for logs, security data, identity events and so much more.* 

[Must Learn KQL series](https://aka.ms/mustlearnkql)

[Create queries for Microsoft Sentinel using Kusto Query Language (KQL)](https://docs.microsoft.com/learn/paths/sc-200-utilize-kql-for-azure-sentinel/?WT.mc_id=modinfra-57417-socuff)

[Getting started with log queries in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/logs/get-started-queries?WT.mc_id=modinfra-57417-socuff)

### Infrastructure as Code (IaC)

*Sometimes code isn't just for developing applications ... it's for scripting the deployment and configuration of infrastructure. Get started with Azure Bicep then dive into deployment tools, including the Ops in DevOps!*

[Infrastructure as Code (IAC): Comparing the tools](https://techcommunity.microsoft.com/t5/itops-talk-blog/infrastructure-as-code-iac-comparing-the-tools/ba-p/3205045?WT.mc_id=modinfra-57417-socuff)

[Fundamentals of Azure Bicep](https://docs.microsoft.com/learn/paths/fundamentals-bicep/?WT.mc_id=modinfra-57417-socuff)

[Automate the deployment of JSON ARM templates by using GitHub Actions](https://docs.microsoft.com/learn/modules/deploy-templates-command-line-github-actions/?WT.mc_id=modinfra-57417-socuff)

[Manage infrastructure as code using Azure, DSC, and third-party tools](https://docs.microsoft.com/learn/paths/az-400-manage-infrastructure-as-code-using-azure/?WT.mc_id=modinfra-57417-socuff)

[Get started on a DevOps transformation journey](https://docs.microsoft.com/learn/paths/az-400-get-started-devops-transformation-journey/?WT.mc_id=modinfra-57417-socuff)

### GitHub

*Speaking of tools that are not just for developers - now you can store your PowerShell scripts somewhere AND have source control and versioning and other developery-stuff. It's a learning curve, but you'll be approving pull requests in no time. Or not approving them.*

[GitHub fundamentals – Administration basics and product features](https://docs.microsoft.com/learn/paths/github-administration-products/?WT.mc_id=modinfra-57417-socuff)

[Deploy Azure resources by using Bicep and GitHub Actions](https://docs.microsoft.com/learn/paths/bicep-github-actions/?WT.mc_id=modinfra-57417-socuff)

### Visual Studio Code

*OK but you have to write those PowerShell scripts first. Or at least copy them from somewhere else and edit them. VS Code has your back, with helpful syntax suggestions that beat the good old days of "Error in line 352".*

[Download Visual Studio Code](https://code.visualstudio.com/?WT.mc_id=modinfra-57417-socuff)

[Using Visual Studio Code for PowerShell development](https://docs.microsoft.com/powershell/scripting/dev-cross-plat/vscode/using-vscode?WT.mc_id=modinfra-57417-socuff)

### Windows Terminal

*No, not the green screen terminals that some of us started with, but if you were brought up with the command prompt, you will be AMAZED by Windows Terminal. Or at least a little bit impressed, we hope.* 

[What is Windows Terminal?](https://docs.microsoft.com/windows/terminal/?WT.mc_id=modinfra-57417-socuff)

[Scott Hanselman’s tips for using Windows Terminal like a pro](https://www.youtube.com/watch?v=FC-gLkYWXLw)

### Automation

*Before the robots take our jobs, we will automate things anyway, so we have more time to be doing the stuff we actually want to be doing. Get started with no code or low code Power Automate or unleash the Logic Apps!* 

[Get started with Power Automate](https://docs.microsoft.com/learn/modules/get-started-flows/?WT.mc_id=modinfra-57417-socuff)

[Power Automate documentation](https://docs.microsoft.com/power-automate/getting-started?WT.mc_id=modinfra-57417-socuff)

[Introduction to Azure Logic Apps](https://docs.microsoft.com/learn/modules/intro-to-logic-apps/?WT.mc_id=modinfra-57417-socuff)

[About Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps/logic-apps-overview?WT.mc_id=modinfra-57417-socuff)

## Conclusion

The IT Pro skillset is so vast and varied, that this list feels incomplete! We know there are big topics like architecture and more details to skills like troubleshooting. And the exact technologies you will need to go deeper into will depend on your current role. But by committing to learning across this range of concepts, tools and languages, you’ll be able to handle most IT Pro tasks that come your way, or feel confident applying for your next role (we won't tell your boss).

What did we miss that you think should be included?
