
To perform a technology ==gap analysis==, start by defining your current technology landscape and documenting existing systems and processes. Next, identify your desired future state—what technology or capabilities you need. Then, compare the two to identify gaps in functionality, performance, or compliance. Finally, prioritize these gaps based on their impact on your goals and develop a roadmap for addressing them. 
**==gap==**
- current tech landscape and systems and processes
- desired future state - what tech capabilities need
- compare two to find gaps in
	- functionality
	- performance
	- compliance
- prioriteze gaps based on impact on goals & develop roadmap to adress
##### How to approach the case
- **Structure Your Analysis:**
    - **Identify Risks:** Categorize potential risks (e.g., operational, strategic, compliance, financial).
    - **Assess Impact and Likelihood:** Evaluate the severity and probability of each risk.
    - **Prioritize Risks:** Focus on high-impact and high-likelihood risks first.

- **Propose Solutions:**
    - **Mitigation Strategies:** Suggest practical controls or actions to reduce risks.
    - **Best Practices:** Reference industry standards and frameworks (e.g., COBIT, ITIL).
    - **Implementation Plan:** Outline steps for rolling out your recommendations, including timelines and resource considerations.

- **Communicate Effectively:**
    - **Clear and Concise:** Present your findings logically and coherently.
    - **Use Visual Aids:** If possible, incorporate diagrams or charts to illustrate points.
    - **Align with Business Goals:** Emphasize how your solutions support the client's overall objectives.




##### BCG Platinion case (==DETTA FINNS JU BARA PÅ PDFEN ISTÄLLET...==)

**Question 1:** What is a possible approach for a quick assessment of the IT application landscape and how can we prioritize the areas of intervention?

Solution:
1. Define framework to drive assessment
	1. Map IT infrastructure to supply chain and business function for holistic view
	2. Relevant dimensions of analysis could be:
		1. impact (business critical or not)
		2. Severity (high/medium/low) of the identified issues in terms of stability, scalability, high TTM (time-to-market)
		3. Type of application (e.g., custom vs. standard software)
2. Describe approach I want to take to do the assesment
	1. Look at documentation (Old incident reports to see stability issues, application map/inventory)
	2. Interviews with key stakeholders (CIO, Head of IT Ops) to complement information
3. Define drivers to prioritize deep dives and recommendations

**Question 2:** What are the main technological levers that can be used to address the pain points raised by the CIO?
Basically here you should tackle painpoints 1 by 1.

1. Pain point "Stability"
	1. Hypotheses on root causes 
		1. Buggy/Badly written custom code (e.g., due to various changes over time) with limited or no documentation 
		2. Outdated/out-of-support applications 
		3. Excessive customization of packaged SW 
	2. Suggested technical lever 
		1. Refactoring of custom applications into a modular and de-coupled architecture: Adjusting current applications would be too complex. It might be easier to re-write entire/pieces of custom applications using new technologies and most importantly with a modular approach (e.g. "microservices architecture") that enables easier isolation of failures, allowing unaffected functionalities to carry on working, hence increasing overall stability
		2. CI/CD implementation (mer scalability tho)
		3. minimze technological debt
2. Pain point "Scalability"

##### FAIR (bra struktur)
The key components of the FAIR model include:

1. **Asset**: The resource or data that is being protected (e.g., information, systems).
    
2. **Threat**: Any potential danger that could exploit a vulnerability (e.g., cyber attacks, natural disasters).
    
3. **Vulnerability**: Weaknesses in an asset that can be exploited by threats (e.g., software flaws, configuration issues).
    
4. **Event Frequency**: The estimated frequency of adverse events occurring (e.g., how often a specific threat might materialize).
    
5. **Loss Magnitude**: The potential impact or financial loss associated with an adverse event (e.g., costs from data breaches, recovery expenses).
    
6. **Risk**: The combination of event frequency and loss magnitude, representing the overall risk level.
    
7. **Controls**: Measures in place to reduce vulnerabilities or mitigate the impact of threats (e.g., firewalls, encryption).


Hey, thank u! I did have a case interview. It’s not as daunting as it sounds. For my case, they essentially give me a few pages to read. The case company had a few problems and I had to come up with solutions on how I would tackle them. The interviewer just wants to know how you think/logic. So be sure to explain like
1. The problem e.g. the company is scaling and needs better centralization
2. How you would solve it e.g. you want to implement a software
3. (Arguably most important imo) say how you would implement it. E.g. ==pilot roll out== in a department first to fix issues then expand.

**Key Components of a ==Contingency Plan==:**

1. **==Risk Assessment==:** Identify potential risks or disruptions (e.g., system failures, data breaches, natural disasters) and their potential impact.
    
2. **==Response Strategies==:** Outline specific actions to take when a risk materializes, including roles and responsibilities of team members.
    
3. **==Communication Plan==:** Define how to communicate with stakeholders during an incident, ensuring clear and timely updates.
    
4. **==Resource Allocation==:** Identify necessary resources (e.g., backup systems, personnel) needed to execute the plan effectively.
    
5. **Testing and Training:** Regularly test the plan through drills and training to ensure that everyone knows their roles and can respond effectively when needed.

##### ==Migration risks== to think about

1. ==Costs== (migration costs, running costs, Total cost of ownership comparison)
2. ==Reasons== to move
3. ==Microservices== vs Legacy code (technical debt if move fix this if have legacy code)
4. ==Regulations & compliance== (for new provider and for ourselves)
5.== Security risks in transfer== of info (should encrypt) (Data integrity)
	1. In transit encryption (TLS)
	2. Data at rest encryption (AES-256)
	3. Role based access control (RW, W, osv..)
	4. 2FA
	5. ==Data mapping== 
		1. Data Mapping is the process of defining how data from one system (such as the old ERP) will correspond to data in another system (like the new ERP). It helps ensure that data is accurately transferred, maintains its integrity, and meets the new system's structure and requirements
6. ==Downtime and business continuity==
	1. solved by:
		1. ==Gradual migration==
		2. ==pilot migration==
		3. ==Downtime scheduling== (migrate on off-hours)
7. ==Backups== in case something goes wrong
8. Incident response plan
9. ==Third party risks== How will new vendors introduce new risks?
10. Have contingency plan in mind
11. ==Integration problem== with ==current dependencies==
12. ==User adoption (cultural impact== of changing systems)
13. ==Performance risks== of new system - ==can it handle peak loads==?
14. ==Scalability== - typ onprem inte skalbart fysiskt men cloud kanske inte skalbart pengar mässigt
15. Post integration - training
16. Congestion

**Vulnerability Scanning**
Description: Automated tools scan systems and applications to identify known vulnerabilities, such as missing patches or misconfigurations.
Example of use: Regular scans of network infrastructure to identify and remediate vulnerabilities.

**Penetration testing**
Description: Ethical hackers simulate cyberattacks to identify weaknesses in a system's security defenses, helping to uncover unknown vulnerabilities.
Example: Assessing the security of a web application before a product launch.

**Business Impact Analysis** 
Description: Focuses on assessing the ==potential impact of technology-related disruptions== on business operations, continuity, and recovery. 
Example: Determining the criticality of different systems to prioritize disaster recovery planning.

**Compliance Assessment** 
Definition: Ensures that an organization ==adheres to relevant regulatory requirements== and industry standards for data protection and security. 
Example: Assessing an organization's compliance with GDPR or HIPAA regulations.

**Security Risk Matrices** 
Definition: Utilizes matrices to evaluate and prioritize risks based on likelihood and impact, often using a scoring system. 
Example Prioritizing security risks and vulnerabilities for mitigation based on their severity.


**SaaS**: Microsoft 365, salesforce
**==PaaS==**: AWS, google cloud
**==IaaS==**: Gives full place for developing: Heroku
##### Public Cloud

- **Definition**: Services offered over the public internet, shared across multiple organizations.
- **Examples**: AWS, Google Cloud, Microsoft Azure.
- **Cost**: Pay-as-you-go pricing model, generally lower costs due to shared resources.
- **Scalability**: Highly scalable; resources can be provisioned on demand.
- **Security**: Security managed by the provider; might not meet specific regulatory requirements for sensitive data.
- **Use Cases**: Best for non-sensitive data, web applications, and startups needing flexibility.

##### Private Cloud

- **Definition**: Exclusive cloud infrastructure dedicated to a single organization.
- **Examples**: On-premises servers, hosted private cloud services.
- **Cost**: Higher upfront costs due to dedicated infrastructure; ongoing maintenance required.
- **Scalability**: Limited compared to public cloud; requires additional resources to scale.
- **Security**: Enhanced security and control, often compliant with regulatory requirements.
- **Use Cases**: Ideal for businesses with strict security needs, such as finance and healthcare.

##### Hybrid Cloud

- **Definition**: Combines public and private clouds, allowing data and applications to be shared between them.
- **Examples**: Utilizing public cloud services for less sensitive operations while keeping critical data in a private cloud.
- **Cost**: Balances costs; can be cost-effective but may require investment in both environments.
- **Scalability**: Flexible scalability; can expand in the public cloud while keeping sensitive operations private.
- **Security**: Offers a balance of security and flexibility; sensitive data can remain secure while benefiting from the public cloud’s scalability.
- **Use Cases**: Suitable for organizations with fluctuating workloads or those needing to meet compliance requirements while still utilizing public resources.

### Summary

- **Public Cloud**: Cost-effective and scalable but less secure.
- **Private Cloud**: More secure and controlled but at a higher cost.
- **Hybrid Cloud**: Flexible, allowing a mix of both, catering to various needs and workloads.'



### Databases
**==ACID==**:
**Atomicity** - either full transaction or no transacition
**Consistency** - database goes from 1 consitent state to another consistent state
**Isolation** - Transactions happen concurrently, but will be made in isolation so they are stable
**Durability** - Once transaction committed, remains committed even if system failure (power outage or crash)

While horizontal scaling refers to adding additional nodes, vertical scaling describes adding more power to your current machines

SQL - vertical scaling (more power to same device) - but harder for horizontal scaling
- fast reads as well pga structure
- 
noSQL - horisontal scaling (Adding more computers)
- unstructured & semi structured - good for images, JSON, osv
- food for big data and ML - because can ingest and process lots of data quickly
- Document databse MONGOdb - timeseries data, 
- Column storage - Cassandra - good for distributed scaling horizontally
- ==Graph database== - good for complex relations - ex social netowrks (Neo4j) - flexible schema - slower on simple lookups compared to key value stores

**ETL** (Extract, transform, load) - (better for structured data)
retreievd from databse, transform data (clean), load into analysis
Used alot in data warehouses or databse analysis

**ELT** (Extract, load, transform) - (unstrusctured data)
extract, load into target, then transform by power of target system
Used alot in cloud where target platform can efficiently handle large columes of raw data



### System design challenges

**Redundancy** refers to the inclusion of additional components or systems that can take over in case of a failure, ensuring continuous operation and minimizing downtime. 
Ex: 
Duplicate hardware components (e.g., servers, disks) so that if one fails, another can immediately handle the workload.

**==Scalability==**
- Vertical scaling (scaling up)
	- Adding more resources to current hardware (GPU, storage, osv...)
	- Benefits
		- Easy to implement and manage
	- Drawbacks
		- Limited in how much scaling can do limited by hardware
		- ==Introduces single point of failure==
- Horizontal scaling (scaling out)
	- Add computers or hardware for distributed computing and handle load
	- ==Benefits==
		- Can do it infinitely basically
		- Adds redundancy
	- ==Drawbacks==
		- Complex to manage
		- Data synchronization problems
		- Hard to balance traffic across nodes

**==Reliability==**
- Load balancers
	- Distribute traffic onto different servers
- Failover strategies
	- Active Passive servers - one active server and one passive on standby
	- Active Active servers - many servers that take load, if one fails, put load on the others
- Backups and recovery
	- On and offsite data backups
	- Disaster and contingency plan
	- Metrics such as recovery time per incident and recovery objectives

==Security==
- Network segmentation
	- Segment network so if one part fails all does not fail
- Pen testing
	- test netowrk
- Zero trust architecture
	- Access controls, culture of threat could be from inside and outside, continuous monitoring, verify requests, check backdoors and such


### Digitalization
**Transformative impact**
- ==organisational== - automate processes, ERP
- ==Analytics== - monitoring and being data driven
- ==Customer strategy== - A/B testing, websites showcase customer journeys
- ==Sales and CS== - CRM systems
**Challenges**:
- ==Legacy== system migration or integration
- ==Change management== - training programs, culture shifts, demostrate benefits to overcome resiliance, communication


### Risks in AI
- Not much historical data
- Complex training we do not know how behave
- Young regulation environment & standardization for risks
- Ethical problems like bias

### Mergers

Cultures - Two differnet cultures, do team building to get teams together, open communication between two different groups
Integrating tech stacks - slowly and piloting, create roadmap
Workforce impact - be transparent about shifts in roles, help people re skill etc

### Devops

Collaboration
- IT and Operations team
- cross functional teams

CI/CD pipeline
- automated testing and deployment - minimize human error risk
- more frequent iterations and faster pushes to production

Culture
- devops built on testing and being innovative
- feedback loops and devops makes mistakes more kind to take care of 

rollbacks - mistakes happen

culture - have process in place with devops mindset - not do easy & fast fixes - leads to technical debt

chaos engineering


What is ==Infrastructure as code== (IaC)?
- Many of the real challenges don’t emerge until teams hit the ground in actual delivery. This is why it's so important to use infrastructure as code. IaC can be integrated seamlessly with testing and monitoring tools. This allows you to validate infrastructure changes through automated testing, perform continuous integration and delivery (CI/CD), and monitor the infrastructure's performance and health in real-time. IaC helps facilitate such integrations and ensures that infrastructure changes are thoroughly tested and monitored.

==Microservices== to think about:
- good for 
	- business critical
	- high frequency of fail
	- Other stuff dependent on 
==Cloud==:
- good for dynamic traffic stuff
- bad for if need low latency
- technical compatability with legacy code
	

















