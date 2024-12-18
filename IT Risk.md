
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
5. ==Security risks in transfer== of info (should encrypt) (Data integrity)
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
	


### Microservices:

- **Definition**: Microservices are an architectural style that structures an application as a collection of small, loosely coupled services, each responsible for a specific business function.
- **Characteristics**:
    - Independently deployable.
    - Each service can be developed, deployed, and scaled independently.
    - Often built around specific business capabilities.

### APIs (Application Programming Interfaces):

- **Definition**: APIs are sets of rules and protocols that allow different software applications to communicate with each other.
- **Role in Microservices**: Microservices typically expose APIs to allow communication between services and with external clients. APIs define how other services can interact with a microservice.

Here are the pros and cons of **==APIs==**:

### Pros:

1. **Interoperability**: APIs enable different software systems to communicate and work together, enhancing integration.
2. **Scalability**: They allow applications to scale by enabling modular components to function independently.
3. **Reusability**: APIs can be reused across different applications, reducing development time.
4. **Easier Maintenance**: Changes to one system can be made without affecting others, simplifying updates.
5. **Faster Development**: Developers can build on existing services rather than starting from scratch.

### Cons:

1. **Security Risks**: Exposing APIs increases the attack surface, necessitating robust security measures.
2. **Complexity**: Managing multiple APIs can lead to increased architectural complexity.
3. **==Versioning Issues==**: Keeping track of different API versions can be challenging and lead to compatibility issues.
4. **==Performance Overhead==**: API calls can introduce latency, particularly if multiple calls are needed for a single task.
5. **==Dependency Management==**: Changes in one API can affect dependent services, requiring careful coordination.




Common stacks:
###### 1. **MEAN Stack**
- **Components:**
    - **MongoDB:** NoSQL database for storing data in JSON-like documents.
    - **Express.js:** Web application framework for Node.js, simplifying server-side development.
    - **Angular:** Frontend framework for building dynamic single-page applications.
    - **Node.js:** JavaScript runtime for server-side programming.
- **Use Cases:** Ideal for full-stack JavaScript applications, particularly real-time applications like chat apps.
    
###### 2. **MERN Stack**
- **Components:**
    - **MongoDB:** Same as above.
    - **Express.js:** Same as above.
    - **React:** JavaScript library for building user interfaces, focusing on component-based architecture.
    - **Node.js:** Same as above.
- **Use Cases:** Excellent for projects requiring a responsive and high-performing frontend, like dashboards and social media platforms.
    
###### 3. **LAMP Stack**
- **Components:**
    - **Linux:** Operating system that supports the stack.
    - **Apache:** Web server for serving web applications.
    - **MySQL:** Relational database management system for structured data.
    - **PHP:** Server-side scripting language for dynamic web content.
- **Use Cases:** Traditional web applications, content management systems (like WordPress), and e-commerce sites.
    
###### 4. **Django Stack**
- **Components:**
    - **Django:** High-level Python web framework that encourages rapid development.
    - **PostgreSQL:** Advanced relational database for data storage.
    - **HTML/CSS/JavaScript:** Standard languages for structuring and styling web content.
- **Use Cases:** Ideal for data-driven applications, APIs, and sites requiring strong security features, like financial apps.
    
###### 5. **.NET Stack**
- **Components:**
    - **ASP.NET:** Framework for building web applications and services with .NET.
    - **C#:** Programming language commonly used with .NET for server-side development.
    - **SQL Server:** Relational database management system by Microsoft.
- **Use Cases:** Enterprise-level applications, particularly in sectors requiring robust security and scalability, like healthcare and finance.
###### 6. **Serverless Stack**

- **Components:**
    
    - **AWS Lambda:** Serverless compute service that runs code in response to events.
    - **API Gateway:** Service for creating and managing APIs.
    - **DynamoDB:** NoSQL database service for fast and flexible data storage.
- **Use Cases:** Highly scalable applications, microservices, and applications with variable workloads, such as mobile backends.

Resilience:
- Ability to handle and recover form failures gracefully
- Detect failure then recover from it



**Cap Theorem**
Consistency, Availability and Partition tolerance
- can only give 2/3 of these
Consistency means every read recieves the latest info written.
Availability means every request recieves a non error resposne.

Partition tolerance is that the system continues to work even if some nodes have gone down if network failure. 

**Scalability**
Scalability: Increasing the capacity to meet the increasing workload
Elasticity: increasing or reducint the capacity to meet the increasing or reducing workload
Aspects of scalability:
Scale up or scale down

Choices:
CP, AP or CA
But we must have P.
SO either CP or AP.
So consitency or availability?

Failure in system, and node goes down, lets say we get a request, either we give stale data which is not consistent but available, or have consistent data but which is not available.

Example:
Online shopping. Listing module and order taking module where inventory is managed. Lets say these talk to eachother, and inventory might not be updated good and cant say how many products are available. Here you can either tell customer that they cant use it (no availability), or you can let them use it but have stuff that might not be in stock (no consistency), but you can try to solve this problem later by getting the things in instead.

So Amazon as a company choose availability over consistency. But in banking, maybe consistency is more important than availablitiy (check back later to see your balance etc…)

Partitioning
Dela upp data i mindre delar. Ex. lets say we partition employee data by age. Then we need to access specific partions of that age which makes it faster to query. So benefit is reduces maintenance if we have larger table, as well as lower latency in queries. Also good for memory saving as data required to be loaded into memory for executing a query is lower. Also benefit is high availability as if we have multiple partitions we have replicas of them too so overall system availability is higher.

We have vertical partitioning (dela på column) och horizontal partitioning (dela på row)


A **reverse proxy** is a server that sits in front of web servers and forwards client (e.g. web browser) requests to those web servers.
Reverse proxy basically if somethign comes from the outside it is sent to the inside things.

Protection from attacks
If a hacker knows the IP address of your origin server, they can check one very big item off their attack checklist. Having a reverse proxy prevents malicious actors from directly targeting your origin server using its IP address because they do not know what it is.


**NGINX**: Why use NGINX in a system? Can work as a proxy server for email protocols. (defending your IP)
Can also be used as a load balancer.


**Load balancing**: Round robin is asimple balancing algorithm where requests are distributed across a group of servers in a sequence. Kan också load balansea med hash


**Platinion**

Hybrid cloud - take advantage of public cloud infrastructure 
Data center consolidation part of digital transformation
- need to provide new techs and solutions and renew infrastructure (8-9y old Solaris machines)
Political issues in a certain place so should not have data centers there.

Data center certification T2 bsT4 

T4 higher checks and more secure 
- if move from T2 you do not have same level of constraints as on T4

Open backend with microservices

In oil and gas company thing US is a chokepoint/bottleneck because many tickets are there and waiting as many different countries with different priorities send there

excel bad IT support system because: changetracking hard, simultaneous access ,reporting and management

if benefit in something, ex relocation - what is then the costs of setting everything up? When breakeven? Do we have the cash at hand?

BCP roles refer to the specific responsibilities assigned to individuals or teams involved in Business Continuity Planning (BCP). BCP is the process of creating systems of prevention and recovery to deal with potential threats to a company

**Data steaming** good if system needs to be updated continously, can be made cheaper as well if send in batches. 
**Point to point integration** is everything talks to everything which is good if small system but exponentially more complex when scaled
**APIs**: Structured way of communicating
**Event drive integration** - If an event triggers that needs to comunicate with other system, message brokers/busses take the info to the other system



====PRINTS:====


**The Software Development Life Cycle (SDLC) is a structured process for developing software applications. Here’s a breakdown of each phase you mentioned:**

1. **Requirements Gathering & Analysis**:
    - **Objective**: Identify what the software should achieve.
    - **Activities**: Engaging stakeholders to collect requirements through interviews, surveys, and workshops. Analysing these requirements to understand their feasibility and prioritise them.
2. **Design Phase**:
    - **Objective**: Define how the software will be built.
    - **Activities**: Creating detailed design documents that outline the architecture, interfaces, data structures, and components of the software. This phase may include creating prototypes or mockups.
3. **Development**:
    - **Objective**: Actual coding of the software.
    - **Activities**: Developers write code based on the design specifications. This phase also involves version control and regular updates to ensure collaboration and integration among team members.
4. **Testing**:
    - **Objective**: Ensure the software functions correctly and meets requirements.
    - **Activities**: Conducting various tests (unit, integration, system, acceptance) to identify and fix bugs or issues. Testing may also involve validating performance and security requirements.
5. **Production**:
    - **Objective**: Deploy the software for end-users.
    - **Activities**: Releasing the software into a live environment. This phase includes monitoring for issues, providing support, and planning for future updates or maintenance.


### Service Models
1. **SaaS (Software as a Service)**:
    - Software applications are delivered over the internet on a subscription basis. Users access the software via a web browser (e.g., Google Workspace, Salesforce).
2. **PaaS (Platform as a Service)**:
    - Provides a platform allowing developers to build, deploy, and manage applications without worrying about the underlying infrastructure (e.g., Heroku, Google App Engine).
3. **IaaS (Infrastructure as a Service)**:
    - Offers virtualized computing resources over the internet, providing users with control over the infrastructure (e.g., AWS EC2, Microsoft Azure VMs).
4. **FaaS (Function as a Service)**:
    - A serverless computing model where users can run code in response to events without managing servers. It scales automatically based on demand (e.g., AWS Lambda, Azure Functions).
### Infrastructure Elements

1. **Virtual Machines**:
    - Software-based emulations of physical computers that run an operating system and applications. They allow multiple operating systems to run on a single physical server.
2. **Containers**:
    - Lightweight, portable units that package applications and their dependencies. Containers share the host OS kernel but run in isolated user spaces (e.g., Docker).
3. **Load Balancers**:
    - Distribute network traffic across multiple servers to ensure no single server becomes overwhelmed, improving performance and reliability.
4. **Cloud Native Development**:
    - Refers to building applications specifically for cloud environments, leveraging microservices, containers, and automated scaling for improved agility and resilience.


### Agile Manifesto

The Agile Manifesto outlines four key values and twelve principles that promote flexibility, collaboration, and customer satisfaction in software development. The four main values are:

1. **Individuals and interactions** over processes and tools.
2. **Working software** over comprehensive documentation.
3. **Customer collaboration** over contract negotiation.
4. **Responding to change** over following a plan.

### Key Processes & Elements

1. **Iterations**: Short, time-boxed cycles (usually 1-4 weeks) where teams work on delivering functional software increments.
2. **Backlog**: A prioritized list of features, enhancements, and fixes that need to be developed. The backlog evolves as project needs change.
3. **Team**: Cross-functional groups consisting of members with various skills who collaborate to deliver the product increment.

### Roles

1. **Scrum Master**: Facilitates the Agile process, removes obstacles, and ensures that the team follows Agile principles. Acts as a servant leader for the team.
2. **Product Owner**: Represents stakeholders and customers, manages the product backlog, prioritizes features, and defines the vision for the product.
3. **Developer Team**: A self-organizing group responsible for delivering the product increments. Team members work collaboratively to complete tasks and meet sprint goals.

---

Api integration hard against Banks where need real time uppdaterad and such

Creatre webapp witth python shit kolla luren



