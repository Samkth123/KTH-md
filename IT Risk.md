
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
3. (Arguably most important imo) say how you would implement it. E.g. pilot roll out in a department first to fix issues then expand.

**Key Components of a Contingency Plan:**

1. **Risk Assessment:** Identify potential risks or disruptions (e.g., system failures, data breaches, natural disasters) and their potential impact.
    
2. **Response Strategies:** Outline specific actions to take when a risk materializes, including roles and responsibilities of team members.
    
3. **Communication Plan:** Define how to communicate with stakeholders during an incident, ensuring clear and timely updates.
    
4. **Resource Allocation:** Identify necessary resources (e.g., backup systems, personnel) needed to execute the plan effectively.
    
5. **Testing and Training:** Regularly test the plan through drills and training to ensure that everyone knows their roles and can respond effectively when needed.

##### Migration risks to think about

1. Costs (migration costs, running costs, Total cost of ownership comparison)
2. Reasons to move
3. Microservices vs Legacy code (technical debt if move fix this if have legacy code)
4. Regulations & compliance (for new provider and for ourselves)
5. Security risks in transfer of info (should encrypt) (Data integrity)
	1. In transit encryption (TLS)
	2. Data at rest encryption (AES-256)
	3. Role based access control (RW, W, osv..)
	4. 2FA
	5. Data mapping 
		1. Data Mapping is the process of defining how data from one system (such as the old ERP) will correspond to data in another system (like the new ERP). It helps ensure that data is accurately transferred, maintains its integrity, and meets the new system's structure and requirements
6. Downtime and business continuity
	1. solved by:
		1. Gradual migration
		2. pilot migration
		3. Downtime scheduling (migrate on off-hours)
7. Backups in case something goes wrong
8. Incident response plan
9. Third party risks How will new vendors introduce new risks?
10. Have contingency plan in mind
11. Integration problem with current dependencies
12. User adoption (cultural impact of changing systems)
13. Performance risks of new system - can it handle peak loads?
14. Scalability - typ onprem inte skalbart fysiskt men cloud kanske inte skalbart pengar mässigt
15. Post integration - training
16. Congestion

**Vulnerability Scanning**
Description: Automated tools scan systems and applications to identify known vulnerabilities, such as missing patches or misconfigurations.
Example of use: Regular scans of network infrastructure to identify and remediate vulnerabilities.

**Penetration testing**
Description: Ethical hackers simulate cyberattacks to identify weaknesses in a system's security defenses, helping to uncover unknown vulnerabilities.
Example: Assessing the security of a web application before a product launch.

**Business Impact Analysis** 
Description: Focuses on assessing the potential impact of technology-related disruptions on business operations, continuity, and recovery. 
Example: Determining the criticality of different systems to prioritize disaster recovery planning.

**Compliance Assessment** 
Definition: Ensures that an organization adheres to relevant regulatory requirements and industry standards for data protection and security. 
Example: Assessing an organization's compliance with GDPR or HIPAA regulations.

**Security Risk Matrices** 
Definition: Utilizes matrices to evaluate and prioritize risks based on likelihood and impact, often using a scoring system. 
Example Prioritizing security risks and vulnerabilities for mitigation based on their severity.


**SaaS**: Microsoft 365, salesforce
**PaaS**: AWS, google cloud
**IaaS**: Gives full place for developing: Heroku
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
- **Hybrid Cloud**: Flexible, allowing a mix of both, catering to various needs and workloads.