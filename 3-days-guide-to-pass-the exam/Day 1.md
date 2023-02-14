## Study Plan

1. Introduction to **AWS**
2. Cloud Concepts
3. Security and Compliance
4. Technology
5. Billing and Pricing
6. Preparing for the exam

### Signup to AWS Educate and apply for introduction to Cloud 101 (Labs) to practice while studying

---

## Cloud Concepts (*26% of the exam*) :

### Any website you intend to construct need a number of distinct components.
1. **Compute**, think of these as servers or computers that are going to do the processing required to run your website.

2. **Database**, that's were you store information about products and customers , etc...

3. **Storage**, this is slightly difference from databases, here we are talking about storing somethings like pictures of products, or marketing documents for the different product that you are selling.

4. **Networking**, this is what allows your customers to connect to your website through the internet just like any other websites.

5. **Security**, meaning that the data about your customers, their payment information, their order information and so on. That it can't be hacked or stolen by infectious characters. 

**You are basicly going to replace all this with migrating into the cloud which makes all of this available for you and ready to use with a pay as you go pricing. How Cool is That ?**

---

### Foundational Services 
	1. Compute : Elastic Compute Cloud (**EC2**) .
	2. Database : Relational Database Service (**RDS**) and **DnamoDB** .
	3. Storage : Simple Storage Service (**S3**) . 
	4. Networking : Virtual Private Cloud (**VPC**) . 
	5. Security : Identity and Access Management (**IAM**) . 

### Benifits of the Cloud

Term | Description | Example
-- | -- | --
Elasticity | The ability to adapt to workload changes. | Amazon.com hanlding a hige spike in traffic on Prime Day.
Scalibility | The ability to handle increased workloads by adding resources. | Scale up a database because the size has grown over time.
High availability | The ability to continue functioning even if some components fail. | When a power outage causes on data center to go down, traffic is routed to another.
Reliability | The ability to function consistently and correctly when expected. | 99.99% uptime for EC2 instances during a given month.
Agility | The ability to rapidly develop, test, and launch applications to deliver business value. | Launch a new business application in days rather than months.
Global reach | The ability to get closer to your customers through a global infrastructure. | 25 Availability Zones around the world.
Pay-as-go pricing | Only pay for what you use, and only when you need it | An EC2 instance only used for 2 hours; only pay for 2 hours.
Economies of scale | Because of their size, AWS can purchase things more cheaply than an individual organization can | Amazon purchases servers at a fraction of the cost that you could, and pass the savings on to you.

---

### What is Total Cost of Ownership (TCO) ?
Its is basicly the sum of the **Up-front cost** (Capital Expnese: *CapEx*) and the **cost to operate** (Operating Expense *OpEx*).

With **AWS** you can get rid of the Capital Expenses totally cause **AWS Services** provide it for you but for the Operating Expenses you git rid of some of it but you pay much less on compared to building your own data center.

### Ways to Reduce Costs in AWS 
	- Right-sized infrastructure
	- Automation
	- Compliance scope
	- Managed Services

### What is the AWS Well-Architected Framework ?
The **AWS Well-Architected Framework** helps you understand the pros and cons of decisions you make while building systems on **AWS**. By using the Framework you will learn architectural best practices for designing and operating reliable, secure, efficient, and costeffective systems in the cloud.

You should get familiar with the pillars as they could be mentioned in the exam.

Name | Description
--- | ---
Operational Excellence | The ability to support development and run workloads effectively , gain insight into their operations, and continuously improve supporting process and procedures to deliver business value.
Security | The security pillar describes how to take advantage of cloud technologies to protect data, systems, and assets in a way that can improve your security posture.
Reliability | The reliability pillar encompasses the ability of a workload to perform its intended function correctly and consistenly when it's expected to. This includes the ability to operate and test the workload through its total lifecycle. This paper provides in-depth, best practice guidance for implementing reliable workloads on **AWS**.
Performance Efficiency | The ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.
Cost Optimization | The ability to run systems to deliver business value at the lowest price point.
Sustainability | The ability to coninually improve sustainability impacts by reducing energy consumption and increasing efficiency across all components of a workload by maximizing the benifits from the provisioned resources and minimizing the total resources required.

---

### Getting back to the [Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf)  you should really be familiar with the General Design Principals.

#### Cloud Architecture Design Principles 
	- Design for failure (*Everything fails all the time*).
	- Decouple components (*Different components of the system should work independently*).
	- Implement elasticity (*Scale up and down when needed*).
	- Think parallel (*Think about the workload*)

---

### Important Points to Remember for the Exam

#### BENIFITS
	- Global reach: Data Centers around the world.
	- High availability: Continue functioning even when one component goes down.
	- Cost Savings: Reduces up-front costs and ongoing costs.
		- Only pay for what you use.
		- Right-sizing infrastructure means you don't have to "guess" capacity.
		- Managed services reduce your IT overhead/spend.

#### DESIGN PRINCIPLES
	 - Design for failure: assume things will fail, and architect for that.
	 - Loose coupling: reduces the dependencies between components.
	 - Elasticity: ability to scale resources up and down based on needs.
	 - Reliability: perform an intended function correctly and consistently when expected to.


### You should get a look at [Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)
 
---

## Security and Compliance (*25% of the Exam*)

### AWS Shared Responsibility Model :

![Chart-1024x603-1.png (1024×603) (sonraisecurity.com)](https://sonraisecurity.com/wp-content/uploads/Chart-1024x603-1.png)


1. **Infrastructure as a Service (IaaS)** : AWS will manage the bottom 4 layers and you are responsible on anything on top of that.

2. **Platform as a Service (PaaS)** : AWS will manage a few more things including the Runtime, Middleware and Operating System and you manage the applications and data.

3. **Software as a Service (SaaS)** : AWS is responsible for everything, you just need to use the software.

### What is Identity and Access Management (IAM) ?
Service that used o securly control access to your AWS resources. It controls **Authentication** (*Who*) and **Authorization** (*What they can do*).

### You should Know go to Lab6 in introduction 101 labs which is the introduction to AWS Identity and Access Management (IAM).

### 1. Users

Root User | IAM User
--- | ---
One per account | Multiple per account
Unrestricted access | Users can be deleted or disabled
Difficult to restrict or revoke access | Easy to restrict access

#### A root user can perform the following tasks:

	- Close an AWS Account
	- Change an AWS support plan
	- Change AWS Account settings

*Note: For best practices always work in your IAM account not the root account, Set up IAM users with the least number of permissions needed.*

### 2. User Groups
Is a group of users that share the same roles and policies.

### 3. Role 

	- Similar to a user (an identity with permissions).
	- Does not have credentials (passwords or keys).
	- Assumable, temporarily, by anyone who needs it.

*Whatever hat you put on or whatever hat you put on as long as you are wearing this hat you can do the specific tasks with the role.*

### 4. Policies (Who can do what to which resources and when)
*Ex: Allow IAM to rotate their own credentials programmatically and in the console, Allow user to start and stop EC2 instances, etc...*

**Policy Example**
```json
{
	"Version" : "2012-10-17",
	"Statement": [
		{
			"Effect": "Allow", 
			"Action": [
				"ec2: StartInstances",
				"ec2: StopInstances"
			],
			"Resource": "arn:aws:ec2:*:*:instance/*",
			"Condition": {
				"StringEquals": {
					"aws:ResourceTag/Owner": "${aws:username}" 
				}
			}
		},
		{
			"Effect": "Allow",
			"Action": "ec2:DescribeInstances",
			"Resources": "*"
		}
	]
}
```

to finish up the section you should be able to create a normal users, group users, roles, Policies(and attach them)

---

### Multi-Factor Authentication (MFA)
Two or more factors in order to authenticate (i.e, figure out who you are)

	- Something you know (e.g. , a password)
	- Something you have (e.g. , a phone or a hardware token)
	- Something you are (e.g. , fingerprint)

#### Three types of MFA Devices

	1. Virtual MFA device for smartphone or tablet (google, microsoft)
	2. U2F Security key (yubikey)
	3. Other hardware key ex:gamalto

*Best Practices is to enable MFA for your root account and IAM users*

#### What is an Access key ?
an access key is a way to have permessions into the console using your terminal but you two things

	1. Access key ID
	2. Secret Key (which you shouldn't have it in any code source)

### IAM Best Practices

	- Use an IAM user for day-to-day work, NOT the root account.
	- Use roles to give permissions to AWS services.
	- Don't share credentials.
	- Assign permissions to groups rather than individual users.
	- When assigning permissions, give the least amount possible.
	- Enforce MFA and strong password policies.
	- Use the IAM Credentials Report to audit permissions.

---

## Security and Compliance Services

- Infrastructure Protection
- Data Protection
- Detection
- Incident Response
- Compliance

### Infrastructure Protection :

#### What is a DDoS attack ? 
A DDoS attack is a cyber attack that overloads a website or service with too much traffic, making it unavailable. The attack originates from multiple sources to overwhelm the target. It is important for organizations to have proper security measures in place to protect against DDoS attacks.

#### 1. AWS Shield

- This is a service that AWS offer for protection against **DDoS**.
- Think of it as Shield that sets and protects the server from attacks.

- There is 2 types of AWS Shield:
	1. **STANDARD** :
		- Automatically protects all AWS customers.
		- Free
		- Protects from the most common types of **DDoS** attacks.

	2. **ADVANCED** : 
		- A paid service that protects against more sophisticated attacks and provides detailed diagnostics.
		- Integrates with other services like CloudFront, Route 53 and Elastic Load Balancing.
		- AWS Web Application Firewall (**WAF**) included at no extra cost.

#### 2. Web Applicatoin Firewall (WAF) :
- FireWall is a term refers to a physical wall between houses or structures that was meant to prevent the spread of fire.
- Same in technology, a Web Application Firewall also set in front of your web applications protecting it against common exploits and bots.

- **Configure rules** :
	1. Allow, block, monitor/count.
	2. IP addresses, country of origin, presence of a script, URL strings, etc...


### Data Protection

#### Two Types of Encryption

AT REST | IN TRANSIT
--- | ---
Data is stored or archived on a device | Data being transferred from one location to another
Examples : S3 bucket, Hard disk, Databse | Examples: Moving data from an EC2 instance to an S3 bucket, Moving data from an on-premises data center to AWS

#### Encryption Keys

1. Let's say you have a super secret msg that you want to send to somebody but you don't want anyone to be able to read it. 
2. So you gonna run it through an encryption algorithm and crypt it into something different.

#### AWS Key Management System (KMS) :

	- Primary Service for encryption in AWS
	- AWS manages the encryption hardware software and keys for you
	- Integrated with many AWS services, including EBS, S3, Redshift, and CloudTrail (ex: I want to encrypt a document stored in a S3 bucket.)
	- FIPS 140-2 Compliance: Level 2 overall (3 in some areas)

#### AWS CloudHSM (*Hardware Security Module*)

	 - AWS provisions the hardware and you do everything else
		 - AWS cannot access your keys 
		 - AWS cannot recover your keys
	- Integrated with a limited number of other AWS services
	- FIPS 140-2 Compliance: Level 3 (considered more secure)


#### Types of Keys

AWS MANAGED | CUSTOMER MANAGED | CUSTOM KEY STORES
--- | --- | ---
AWS creates and manages | You (customer) create and manage | Created with CloudHSM
Used by AWS services (*aws/lambda, aws/cloud9, aws/s3*) | Can create policies | you own and manage
 __ | Specify who can use and manage the keys | __

