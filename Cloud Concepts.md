# Cloud Concepts
---
### Any Website that you want to create needs several different things 

1. **Compute**, think of these as servers or computers that are going to do the processing required to run your website.

2. **Database**, that's were you store information about products and customers , etc...

---

3. **Storage**, this is slightly difference from databases, here we are talking about storing somethings like pictures of products, or marketing documents for the different product that you are selling.

4. **Networking**, this is what allows your customers to connect to your website through the internet just like any other websites.

5. **Security**, meaning that the data about your customers, their payment information, their order information and so on. That it can't be hacked or stolen by infectious characters. 

---

### Foundational Services 

1. Compute : Elastic Compute Cloud (**EC2**) .
2. Database : Relational Database Service (**RDS**) and **DnamoDB** .
3. Storage : Simple Storage Service (**S3**) . 
4. Networking : Virtual Private Cloud (**VPC**) . 
5. Security : Identity and Access Management (**IAM**) . 

---

![[Foundation_Services.png | 600 ]]

---

--> For these services, you are only gonna be bill for what you use and **AWS** provides a lots of tools to manage every bit of it. Including detail of which you are spending and where.

---

### What are the Benefits of the Cloud 

1. **Elasticity** : The ability to adapt to workload changes (usually dynamic , short-term).

2. **Scalability** : The ability to handle increased workloads by adding resources (usually more static , long-term).
---

3. **High Availability** : The ability to continue functioning , even if some components fail.

4. **Reliability** : The ability to function consistently and correctly when expected.

5. **Agility** : The ability to rapidly develop, test and launch applications to deliver business value.

---

![[Benifits1.png | 600 ]]

---

 6. **Global reach** : The ability to get closer to your customers through a global infrastructure (31 geographic regions{1st Q 2023}).


 7. **Pay-as-you-go pricing** : Only pay for what you use, and only when you need it.


 8. **Economies of scale** : Because of their size , AWS can purchase things more cheaply than an individual organization can.

---

![[Benifits2.png | 600 ]]

---

### Economics of AWS 

1. **Total cost of ownership**

2. **Capital expenses**

3. **Operational expenses**

4. **Software licensing costs**

---

- #### Total cost of ownership (TCO):
	1. **Up-front cost** of purchasing your servers and racks and cables and software licences, maybe an actual building to hose things in and when the servers get old you need to buy new ones over time (so these are your CAPITAL EXPENSE {"CapEx"}).
	2. **Cost to operate** things like electricity, air-conditioning, people to setup and maintain the servers, you have to train those people so they have the skills etc... (OPERATING EXPENSE {"OpEx"}).

---

--> The benefits of AWS is basically, your Capital Expenses go away, amazon does all the work of purchasing real-state, servers, routers, switches, cables and all the physical things that you could have trouble buying it.

---

--> And you can also remove some of the Operating Expense, meaning that the people required to setup and maintain the servers and other things that's covered by AWS. 

--> But the rent and the subscription you pay to AWS to use their stuff that is considered OpEx but it's likely less than if you were doing everything yourself

---

![[TCO.png | 600 ]]

---

--> ***Ways to Reduce Costs in AWS*** 

1. **Right-sized infrastructure** : basically on use infrastructure that you really need, right number of machines, right kinds, etc... 

2. **Automation** : you can schedule start and stop times for servers that you use for development.

---

3. **Compliance scope** : taking account of all the data processing in which your organization has a role, whether as a data controller or as a data processor.

4. **Manage services** : this is just let you use the service without having to worry about creating a server for it, installing a software and licensing cost.

---

### AWS Well-Architected Framework

-  It's a framework for having a design and build your Architecture in AWS taking into account best practices and pros and cons of different options.
---

- ***The pillars of the AWS Well-Architected Framework*** :

![[Pillars_AWS.png | 710 ]]

---

- ***Cloud Architecture Design Principles*** : 

![[Design_principles2.png | 600 ]]

---

1. **Design for failure** : meaning servers go down, hard-drives crash and even entire data center go down sometimes. You just need to assume things are going to fail in order to take your application accordingly to e able to flow over another data center or server.

---

![[Design_failure.png | 600 ]]

---

2. **Decouple components** : this means that the different parts of the system should be able to function independently of one another

	-  you want the component decouple and in between you have something like a #queue { For example : if your photo processing services goes down it's fine the msgs are still sending to the queue and it will be stored there ready to pick up whenever the server is back online.}

---

- This approach architecture is refer to **Micro-services** where you separate the parts of the system into smaller services independent from one another {This is a contrast of **Monolithic** system when you see it as a big black box when a component fails all the service fails} 

---

![[couple_component.png | 600 ]]

---

![[Decouple_component.png | 600 ]]

---

3. **Implement elasticity** : Basically the ability to scale up and down as needed, to implement this think about when you have a variable loads for different parts of the system.

---

4. **Think parallel** : it's so easy to add another resources in the cloud, think about the workload that can run in parallel { For Example : Rather than long data processing job that takes a lot of times on 1 server maybe you can break it into pieces then use a lot of servers in a small time to accomplish the same thing} .

---

--> You get the job done faster and less chance that something that goes 
wrong that will require you to start over.

![[Think_Parallel.png | 600 ]]

---

### Important Points To Remember

- #### Benefits 

	1. **Global reach** : data centers around the world
	
	2. **High availability** : continue functioning even when one component goes down(server, data center, etc...)
---

3. **Cost savings** : reduces up-front costs ("CapEx") and ongoing costs ("OpEx").
	
	- Only pay for what you use. 
		
	- Right-sizing infrastructure.
		
	- Managed services reduce your IT overhead/spend.

---

- #### Design Principles

	1. **Design for failure** : assume thing will fail, and architect for that.
	
	2. **Loose coupling** : reduces the dependencies between components.
	
	3. **Elasticity** : ability to scale resources up and down based on need.
	
	4. **Reliability** : perform an intended function correctly and consistently when expected.

---

- #### Review the Well-Architected Framework:

 https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html
 