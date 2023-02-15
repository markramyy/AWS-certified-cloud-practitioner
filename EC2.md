# EC2

---

- One of the foundation services is **Elastic Compute Cloud** (**EC2**).

- It's a virtual server that you "rent" in AWS.

- Called an "Instance".

---

- There is a lot o benefits :
	1. Easy to scale 
	2. Reliable
	3. Use with other services
	4. Only pay for what you use

---

## Shared Responsibility Model for EC2

- EC2 is considered as #IaaS .

| **AWS Responsibility**                                | **Customer (Your) Responsibility**                                                                    |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| 1. Physical Hardware and Network                      | Software running on the instance, including operating system and applications (maintenance, patching) |
| 2. Hypervisors (allow you to create virtual machines) | Security groups and Network access control lists.                                                     |
| 3. Elastic Block Store (**EBS**)storage system        | Network Architecture within the Virtual Private Cloud (**VPC**)                                       |

---

## EC2 Launch Types/Purchasing Options

---

![[EC2-Types.png | 600 ]]

---

