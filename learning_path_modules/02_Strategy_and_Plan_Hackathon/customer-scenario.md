# What The Hack

# Module 02: Strategy & Plan Hackathon

## Customer Scenario - Contoso Land Surveying

**Contoso Land Surveying** operates a global geology surveying business, where they deploy surveyors to carry out detailed land surveys for companies such as food producers, airports, oil companies, utilities, railway companies, ports authorities and other business which are reliant on infrastructure heavy. Surveys are carried out on dry land as well as underwater and in areas of variable terrain.

Contoso see an opportunity to leverage technology such as drones, data and AI to improve efficiency and provide deeper insights into surveys predicting the challenges of today and tomorrow for their clients and their use of land as an asset.

**Contoso basic information:**

- 2 continents, 8 countries, 5,500 employees, $$1.3bn Revenue
- End state is a global IT system in the cloud which has minimum standards for:
  - Security; Compliance; Performance; Resiliency; Cost Variable.
- Each country currently has an autonomous IT infrastructure with varying standards of DR, backup, HA, and security. Some countries will see cost savings from cloud whilst others will see an increase as their IT estate is aligned to meet the minimum standards, which were not harmonized prior to this move.
- One of the immediate priorities is to enable Contoso's Business Units to focus on core activities rather than trying to keep the lights on. They also want to downsize their on-premises IT infrastructure through use of cloud technologies, centralization, and automation.
- IT head-count is starting to become an issue since the talent pool is limited.
- Contoso has a total of 173 Applications
- Some members of the SLT are concerned that a "move to Azure" will result in additional business risk related to cost, security, and resiliency (but not only!).

Contoso's Senior Leadership Team (SLT) have already set the company direction to leverage technology to transform the business and now want a **high-level business case** so they carry out a cost vs. benefit analysis and ensure that this strategic move makes sense at this stage. At this moment in time this is a litmus test which the SLT will use to eval whether or not Contoso should release another round of funding. Further depth in the business case will be built in later stages.

Contoso Land Surveying IT team have asked Microsoft and you (the partner) to help them develop a **high-level** feasibility study which takes into consideration the following:

- How a "move-to-cloud" can enable innovation and reduce their firefighting activities so that they can focus more on activities which differentiate (core vs context).
- A return on Investment which must in payback in a 36-month period and lower overall OPEX.
- The business case needs to demonstrate where IT costs will increase & where will they decrease.
- The benefits of the cloud which make sense for Contoso must be clearly articulated. Critical success factors must be clearly documented.
- They perceive automation as a key competitive advantage in an already commoditized business. How could they optimize the deployment of surveyors by automating as much as possible their work?
- They want to leverage technology such as drones to optimize surveys & offer surveying solutions in areas not possible with people or conventional machines (think of underwater, hazardous environments, or environments with limits on heavy equipment). How can public cloud help their business?
- The audience for this high-level business case will be the CXO team at Contoso (CEO, CFO, SLT, etc.). It will however be delivered by CIO.

---

## Financials

The following information can you help you formulate a guestimate which you can use to demonstrate possible cost-savings. ROI, additional investments, etc.



![IT spending as a percent of revenue](media/IT-spending-as-percent-of-revenue.png)

![IT spending per employee](media/IT-spending-per-employee.png)

### Estimate IT spend categories

Typically, these will be in this range:

- Data Centre 15 to 22% (lower if they have high cloud adoption)
- End User Compute 10 to 14% (lower if they have low EUC usage for example limited number of knowledge workers)
- Application Development 15 to 22% (lower if they predominantly use COTS applications and don't do much custom app dev)
- Application Support 19 to 22% (linked to above as well as complexity of applications, heavy ERP usage adds to cost)
- IT Service Desk 5 to 7%
- Voice & Data Networking 10 to 15% (influenced by number of branch locations and geography)
- IT Management 8 to 12% (heavily offshore will lower these costs usually, but if there is lots of change offshore can be more expensive)

### Estimate cost savings from moving to cloud

- Try to find out how many applications they have
- Cost savings 500+ Applications likely to be in 25% range
- Cost savings for 300+ Applications likely to be in 20% range
- Cost savings for 150+ Applications likely to be in 15% range
- If not use 18% as a guesstimate
- The cost saving is derived most often from
- Switching off unused / duplicated applications
- Right Sizing the environment buy for what you need now not what you need in 3 years (cloud adoption mindset, not a capital purchase mindset you can easily upgrade along the way)
- Snoozing services out of hours, for example turning applications off during the evening and weekends can lower costs by at least a third

### Estimate the cost increase owing to countries needing to align infrastructure with new global standards

- The customer needs to provide information here, list the 8 countries, and get an anecdotal view of the state of their IT, as in this example:
  - United Kingdom, 25% IT spend, aligned to global standards, no adjustment up needed
  - France, 13% IT spend, aligned to global standards, no adjustment up needed
  - Spain, 10% IT spend, aligned to global standards, no adjustment up needed
  - Italy, 15% IT spend, under specified, high adjustment
  - Portugal, 13% IT spend, aligned to global standards, no adjustment up needed
  - Belgium, 10% IT spend, under specified, medium adjustment
  - Netherlands, 8% IT spend, aligned to global standards, no adjustment up needed
  - Luxembourg, 6% IT spend, under specified, low adjustment
- Ask about the size of the investment this is usually a range of 5 to 15%
  - Low adjustment = 5%
  - Medium adjustment = 10%
  - High adjustment = 15%
- If this is impossible to guess, hen work with a trusted party and ask for their opinion. Use country revenue as a proxy for the IT spend (sometimes this is published in the annual report).

### Estimate the cost of change

The migration complexities and efforts will result in an additional cost. This cost relies on an understanding of the current infrastructure (CAF "Plan" phase - Discover & Assess). For the purposes of this challenge, we can estimate the following:

- 5-to-8 times the anticipated monthly ACR as the cost of migration.  This excludes cost for application re-work which will need to be factored in. This range will depend on lift-and-shift efforts compared to modernization efforts.
- These numbers should always be validated with the partner supporting in the migration.
