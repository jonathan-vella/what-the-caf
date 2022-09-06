# What the CAF

# Module 02 - Migrate Like A Pro Hackathon

## Challenge 02 - Discover and Assess

In this challenge, you will assess customer's existing operating environment for the applications and map them to Azure resources. Your assessment will determine how existing servers and workloads are connected and how they will perform in Azure.

> Remember that while your initial focus is on a subset of servers and applications within the current datacenter, you are tasked with developing a process which can scale beyond just a handful of servers.

Assessments should not just be limited to using tooling only as a means to discover information about an environment. You should schedule time to speak to business owners, end-users, other members within the IT department, etc. in order to get a full picture of what is happening within the environment and understand things which tooling cannot ever tell you.

The business owners currently pay for the servers that host their applications and are very cost-conscious. The IT leadership team wants to make sure that before any migrations begin a cost assessment is performed for each application to demonstrate the cost to the business owners who will continue to bear the cost of the servers, even in Azure.

Last but not least the IT leadership team is very concerned about dependent services for migrated applications. This is based on the feedback they have received from the Infrastructure and Application Support teams. 

> Note: Today, the IT leadership team are of the opinion that they cannot understand their existing on-premises environment. 
> 
> This is based on facts and not assumptions. They have recently experienced an outage, plus they do not have access to the source code for the workloads in scope meaning they can't make updates if dependencies cannot be mapped before migration.
> 
> As a reminder, the current application server architecture is documented [here](./../media/application_architecture.png)

 ---

## Customer requirements

The customer has the following **mandatory** requirements which you should take into consideration:

- While the Infrastructure and Application Support teams feel they understand their operating environment today, they want to have a verification before migrating and have a way to report the current state to IT leadership.
- Before migration, the business owners of each application need to know the estimated monthly cost to host their applications in Azure.
- In the existing environment, applications are segmented and secured through subnets and local OS firewalls. They would like to know what their network topology in Azure will look like and how they can be as secure in Azure as in their current on-premises environment.

---

## Challenge 02 - Success Criteria

- The servers targeted for migration are sized appropriately and the compute needs of each server can be adjusted to meet application owner requirements before migration.
- The estimated cost for each application can be viewed independently and demonstrates the lowest acceptable cost with equivalent performance to the existing on-premises servers.
- Dependencies between servers in the on-premises environment are visualized before migration and visualizations include server-to-server connections as well as ports and protocols.
- The network design limits communication between application tiers to only the required ports and protocols while limiting lateral movement within the network.
- The network design must include secure application delivery whilst minimizing the overhead of certificate lifecycle management. Any modifications to public DNS, IIS and / or Windows Firewall are not allowed at this stage.
