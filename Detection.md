# Detection

---

## 1. Amazon Inspector

- This service is used to automate the monitoring and analyzing for security issues.

- Automatically detects and scans your servers (**EC2 instances**) and your containers (**Elastic container repository**) for software vulnerabilities and network exposure.

---

- And then try to makes sense of the findings and assigns a risk score to each one.

- Integrates with **Security Hub** and **EventBridge** to automate workflows and ticketing.

---

![[Inspector.png | 600 ]]

---

## 2. Amazon GuardDuty

- This is another method that you can automate some of the security work in AWS.

- It is Continuously analyzes network, account and data access from your own private network (**CloudTrail Mgmt and S3 Events** - **VPC Flow and DNS Logs**).

---

- Then using machine learning, identifies and prioritizes potential threats.

- After that using a combination of **CloudWatch** and **Lambda** to automate workflows and remediation.

---

![[GuardDuty.png | 600 ]]

---

## 3. AWS Config

- It's a service that effectively let you take an Inventory, record and audit the configuration of your various AWS resources.

---

- Example :

	1. Inventory all your **S3** buckets, and when one of them becomes publicly accessible, receive an alert.
	
	2. Receive an alert when an unauthorized port opens on a security group(**Firewall**).
	
	3. During a compliance audit, show when configurations changed.

---

## 4. AWS Security Hub

- It's a service that Pulls everything together into a central consolidated place where you can view and take actions on security issues.

	- Requires AWS Config
	
	- Cross-account
	
	- Aggregates data from different services (GuardDuty, Inspector, Macie, IAM Access Analyzer, Systems Manager and Firewall Manager).

---
