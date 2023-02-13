# Data Protection

---
## Encryption

- ### Two Types of Encyption :

	1. **AT REST** :
	
		-  Data that’s stored or archived on a device (S3 bucket, Hard disk, Database)

---

2. **IN TRANSIT** : 
	- Data being transferred from one location to another (Moving data from an EC2 instance to an S3 bucket , Moving data from an on-premises data center to AWS)


---

- ### Encryption Keys

1. Let's say you have a super secret msg that you want to send to somebody but you don't want anyone to be able to read it. 
2. So you gonna run it through an encryption algorithm and crypt it into something different.

---

![[Encryption.png | 600 ]]

---

![[Encryption-Method.png | 600 ]]

Note: It works the same way on AWS but with much more sophisticated algorithm and longer keys.

---

## Types of Keys

### 1. AWS Managed

- AWS creates and manages.

- Used by AWS services (aws/lambda , aws/s3 , aws/cloud9)

---

### 2. Customer Managed

- You (customer) create and manage.

- Can create policies to rotate keys.

- Specify who can use and manage the keys.

- Supports “bring your oYou own and managewn key”.

---

### 3. Custom Key Stores

- Created with CloudHSM .

- You own and manage

---

## Understanding Certificates

- You use certificate to make sure that the connection between your request and the response that you receive is encrypted and safe.

- Certificate is just a text file that you put on your server and **Identifies the server as reputable** and also **Ensures communication between us is encrypted**.

---

- This is called **Transport Layer Security** (TLS) and it replaces the old certificate **Secure Sockets Layer** (SSL).

---

![[Certificates-TLS.png | 600 ]]

---

## Data Protection Services : 

### 1. AWS Key Management System (KMS)

- Primary service for encryption in AWS

- AWS manages the encryption hardware, software and keys for you.
---
---

- Integrated with many AWS services, including EBS, S3, Redshift and CloudTrail.

- FIPS 140-2 Compliance: This is a government standard that kinda bench mark when it comes to cryptographic modules. Level 2 overall (3 in some areas)

---

### 2. AWS CloudHSM

- **HSM** : Hardware Security Module

- AWS provisions the hardware and you do everything else (AWS cannot access/recover your keys).

---

- Integrated with a limited number of other AWS services.

- FIPS 140-2 Compliance: Level 3 (considered more secure)

---

### 3. AWS Certificate Manager (ACM)

- Provision, manage, and deploy public and private **SSL/TLS** certificates.

	1. Public = for resources on the public internet (these certificates are free).
	2. Private = for resources on private networks.

---

- Loads certificates on:

	1. API Gateway
	2. Elastic load balancers
	3. CloudFront distributions

---

### 4. AWS Secrets Manager

- The recommended way to protect secrets (e.g., user names and passwords) needed by your applications and services.

---

- Example: You created a application that has database on the backend and you need to access this database and it requires username and password.
	1. Hard-code the credentials
	2. Store credentials on the file system ad then retrieve them when you need it.
	3. Use AWS Secrets Manager

---

- The first and Second option are not preferable cause the are not that secure. So we go to the usage of AWS Secrets Manager.

---

### 5. Amazon Macie

- It works specificaly with simple storage service S3 and Automatically inventories S3 buckets.

- Then Identifies and analyzes **PII** data using machine learning and pattern matching.

---

- **PII** (Personally Identifiable Information): this is information that if somebody knew it, they will be able to connect to you personally.

- Outputs finding which can integrate with **CloudWatch** and **EventBridge** to automate workflows and remediation.

