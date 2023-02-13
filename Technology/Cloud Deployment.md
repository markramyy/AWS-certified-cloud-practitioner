# Cloud Deployment

---

### There are 3 Different Cloud Deployment Modules.

---

![[Cloud-Types.png | 600 ]]

---

#### 1. Cloud ("Public")

- In another words AWS. This is sometimes refer to as a public cloud.

- Advantage :
	1. Cost savings
	2. Scalability
	3. Flexibility

---
- Infrastructure available to general public over the internet, Owned b an organization selling cloud services (e.g., Amazon). 

- As a Customer you can distinguish or control the location of the infrastructure.

- Gives a lot of efficiency and shared resources and it's a good choice for collaborations or applications used by a lot of people. 

---

#### 2. On-Premises ("Private")

- Where you keep things at your data centers rather than using AWS. this is sometimes refer to as a private cloud. 

- Advantage : 
	1. Privacy
	2. Total Control
	3. Dedicated resources

---
- Infrastructure solely for one organization protected by a Firewall and under the governess of the IT department of the organization.

- May be outsourced or owned, on-premises or off-premises. 

---

#### 3. Hybrid

- Where you might have some things on premises and others in AWS.

- Let you segment different parts of your business  to the most efficient environment.

---

- Comprised of two or more clouds (private, public).

- Bound together to enable data and application portability.

- The potential down sides of this is that the Overall system can be complexes integrate and maintain.

---

![[Cloud-Properties.png | 600 ]]

---

### How to Connect your On-Premises resources to AWS?

---

#### 1. Site-to-Site VPN

- Using Virtual Private Network (**VPN**), that when you connect from On-Premises to AWS over a **VPN**.

---

- It will be automatically Encrypted.

- It uses public Internet so it's not the most secure option.

- Fast and easy to set up and relatively inexpensive.

---

![[Site-to-Site-VPN.png | 600 ]]

---

#### 2. AWS Direct Connect

- It offers a Dedicated Physical Connection from your On-premises data center to AWS (Physical cables).

---

- Bypasses the public internet using a dedicated private network instead (But Data will not be Encrypted by Default).

- Faster and more expensive.

- Takes longer to set up.

---

![[AWS Direct Connect.png | 600 ]]

---
