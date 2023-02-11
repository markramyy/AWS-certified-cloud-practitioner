# Identity and Access Management

---

- ### There is one core surface that really suits in the center of everything else and that's Identity and Access Management (IAM)

---

- #### Services used to securely control access to your AWS resources.

- #### Controls authentication (who) and authorization (what they can do).

---

- ### There is different constructs, and by using a combination of these concepts you will be able to secure and control who does what.

---

## These are the Identities (the "Who")

![[Identities.png | 600 ]]

---

### 1. Users 

- #### Root User:
	1. **One per Account**
	2. **Unrestricted access** : full access to the AWS services and resources.
	3. **Difficult to restrict or revoke access** 
	4. **Can preform some tasks :**
		- Close an AWS account 
		- Change an AWS support plan
		- Change AWS account settings

---

- #### IAM User:
	1. **Created by Root User**
	2. **Multiple per account**
	3. **User can be deleted or disabled**
	4. **Easy to restrict access**

Note: Always work in your IAM account not the root account && set up IAM users with least number of permissions needed.

---

### 2. User Groups 

![[UserGroup.png]]

![[UserGroup-users.png]]

---

### 3. Roles 

- It's an identity you can create that has specific permissions with credentials that are valid for short duration. Roles can be assumed by entities that you trust.

	1. **Similar to a user** (an identity with permissions)
	2. **Does not have credentials** (password or keys)
	3. **Assumable, temporarily,** by anyone who needs it.

---

- ##### Example:

Say that you are creating a virtual server(**EC2**) to host an application and the application need to use a simple storage service(**S3**) and also to publish logs to a service (**CloudWatch**)

---

![[Role.png | 600 ]]

---
1. **OPTION 1** :

	- Create an IAM user for the application with appropriate permissions.
	- Hard-code user credentials in the application or on the EC2 instance’s file system and retrieve them at runtime.

---

![[Role-Option1.png | 600 ]]

---

2. **OPTION 2** : 

	- Create an IAM role for the application with appropriate permissions.
	- When creating the EC2 instance, assign it this role.
	- No credentials required.

---

- #### Using a Hat analogy for Role :
1. In a **Real-life** Analogy, you probably heard someone wearing a lot of hat. You are a lot of different hats playing a lot of different roles depending on the place , time and situation.  

---

![[Analogy-Theory.png | 600 ]]

---

2. Well in AWS, there are similar you can assume or wear by putting on that hat, and when you put, you can do anything the role can do.

---

![[AWS-Hat.png | 600 ]]

---
***PS***: On the exam if you get a question about one service needing permissions to do things on another services then the **Role** is the first thing that you need to consider. 

---
3. And so does Users and Group Users, they can assume rules too and it works the same way. Temporarily you as a user will be able to do whatever that role can do.

------

4. You can switch roles easily.

![[SwitchRole.png]]

---
## Authorization (what they can do)

### 4. Policies (and attach them)

- **Policy** is who can do what to which resources and when.
- This is the basic syntax of the policy:

---

![[Policy-syntax.png | 600 ]]

---

1. For **Effect** : there are 2 options Allow or Deny (Default is Deny)

2. **Action** : Corresponds to API calls to AWS services (Example: **s3:DeleteBucket**)

Note: API is basically the code that your application calls to do something in AWS

---

3. **arn** (Amazon Resource Name) : the resource name you want to apply permission to (Example: **arn:aws:ec2:():instance/instance-id** )

4. **Condition** : Optional conditions to control when this policy is in effect (Example : **{ "StringEquals" : { "aws:username" : "johndoe" }}** ).

---