# Infrastructure Protection

---

## 1. AWS Shield

- This is a service that AWS offer for protection against **DDoS**.
- Think of it as Shield that sets and protects the server from attacks.

---

![[AWS-Shield.png | 600 ]]

---

- There is 2 types of AWS Shield:
	1. **STANDARD** :
	
		- Automatically protects all AWS customers.
		
		- Free
		
		- Protects from the most common types of **DDoS** attacks.
---
2. **ADVANCED** : 

	- A paid service that protects against more sophisticated attacks and provides detailed diagnostics.
	
	- Integrates with other services like CloudFront, Route 53 and Elastic Load Balancing.
	
	- AWS Web Application Firewall (**WAF**) included at no extra cost.

---

## 2. WAF

- FireWall is a term refers to a physical wall between houses or structures that was meant to prevent the spread of fire.
- Same in technology, a Web Application Firewall also set in front of your web applications protecting it against common exploits and bots.

---

![[WAF.png | 600 ]]

---

- **Configure rules** :
	1. Allow, block, monitor/count.
	2. IP addresses, country of origin, presence of a script, URL strings, etc...

---
