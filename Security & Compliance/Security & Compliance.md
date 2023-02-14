# Security & Compliance
---
### AWS Shared Responsibility Model

- It means that you are responsible for somethings and amazon responsible for others.

---
- #### Firstly Customer Responsibility : 

1. You are responsible for **Security "IN" the Cloud**, that means customer data, platform and applications that you deployment cloud, Identity and access management, security of application servers, Network and Firewall.

2. It's also up to you to secure **Client-side Data** to do as Encryption & Data Integrity and Authentication, as well as **Server-side** and **Network Traffic**.

---

![[Customer_Responsibilty.png]]

---

- #### Secondly AWS Responsibility : 

1. They are responsible for **Security "OF" the Cloud**, they protect the global infrastructure on which your application run this includes Hardware, Software, Networking facilities, Real-state.
Data Protection
2. And the services around them like Compute, Storage, Database and etc...

3. Their third party auditors that regularly verify AWS compliance with the variety of standard regulations so you can be sure that the keep their part of the deal.

---

![[AWS_Responsibilty.png]]

---

- #### So that is the big picture but it is important to know that your responsibilities can vary depending on the service .

	1. Provisioning your own server and installing Windows oUntitledr Linux or their software, you are responsible to make sure that the system is updated and patched, etc...| **AWS Responsibility** | **Customer (Your) Responsibility |
	
	2. If you are in managed server all of that underline work is done for you.

---

### Different ways you can use AWS.

1. **Infrastructure as a Service** #IaaS : AWS will manage the bottom 4 layers and you are responsible on anything on top of that.

---

![[IaaS.png]]

---

2. **Platform as a Service** #PaaS : AWS will manage a few more things including the Runtime, Middleware and Operating System and you manage the applications and data.

---

![[PaaS.png]]

---

3. **Software as a Service**  #SaaS : AWS is responsible for everything, you just need to use the software.

---

![[SaaS.png]]

---

### Security and Compliance Services

- #### [[Infrastructure Protection]]:

	1. AWS Shield
	2. AWS Web Application Firewall (WAF)

- #### [[Data Protection]]:

	1. AWS Key Management System (KMS) 
	2. CloudHSM
	3. AWS Certificate Manager (ACM)
	4. AWS Secrets Manager
	5. Amazon Macie

---

- #### [[Detection]]:

	1. Amazon Inspector
	2. Amazon GuardDuty
	3. AWS Config
	4. AWS Security Hub

- #### [[Incident Response]]:

	- Amazon Detective

- #### [[Compliance]]:

	- AWS Artifact