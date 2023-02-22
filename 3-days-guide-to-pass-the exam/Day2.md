## There are 4 different ways to deal with AWS

1. AWS Management Console.
2. Software Development Kit (SDK)
3. Command Line Interface (CLI)
4. AWS Cloudshell

---

### AWS Cloud Deployment Models

Cloud | On-Premises | Hybrid
--- | --- | ---
Public | Private | _
Infrastructure available to general public on the internet | Infrastructure solely for one organization | Comprised of two or more clouds(private, cloud)  
Owned by an organization selling cloud services | May be outsources or owned, on-premises or off-premises | Bound together to enable data and application portability

#### Ways to connect cloud to an on-premises data center
SIte-to-Site VPN
AWS Direct Connect

---

### Availabilty Zone 

A single data center or group of data centers within a region, each with redundant power, networking and connectivity, housed in separate facilities.

### Edge Location

A site that Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery.

---

### AWS Technology Concepts

#### Ways to work with AWS
	- AWS Management Console (browser)
	- Programmatic access
		- From your local machine - both require access key IDs and secrets
			- Software Devloper Kit (SDK)
			- Command Line Interface (CLI)
		- AWS CloudShell
			- Browser-based; doesn't require access key ID.

#### Deployment Models
	- Public Cloud
	- On-premises
	- Hybrid (Connectivity: Site-to-Site VPN (over public internet) or Direct Connect (dedicated physical connection))

*Regions > Availability Zones > Edge Locations*

---

## Technologies

### Elastic Compute Cloud (EC2)
A virtual server that you rent in **AWS**
Called an **Instance**
Easy to scale - Reliable - use with other services - Only pay for what you use


#### Shared Responsibility Model for EC2

AWS Respnsibility | Customer (Your) Responsibility
--- | ---
Physical hardware and network | Software running on the instance, including operating system and applications (maintenance, patching, etc..)
Hypervisors (*Allow you to create virtual machines*) | Security groups and network access control lists
Elastic Block Store (EBS) storage system | Network architecture within the Virtual Private Cloud (VPC)


#### EC2 Launch Types/Purchasing Options

Type | Description
--- | ---
On-Demand Instances |  Default option, Pay by the second while instance is running (minimum 60 seconds)
Reserved Instances | Reserve instances for 1-3 years (ex: database server), Savings up to 70%
Spot Instances | Bid on unused EC2 capacity, savings up to 90%, but can lose instance at any time
Dedicated Hosts | Book an entire physical server and bring your own licenses, Can be purchased on-demand or reserved
Dedicated Instances | Ensures no other AWS customer shares your hardware, Pay by the hour
Capacity Reservations | Reserve capacity for instances in a specific availability zone for any duration

#### Secure Shell (SSH)

Protocol used to securely log into other computers and run commands from the command line, Uses TCP protocol on Port 22

---

### Elastic Load Balancer

#### Benifits of Using Elastic Load Balancing
Managed Service

	 - AWS guarantees uptime
	 - AWS hanfles maintenance, upgrades, etc.

Distibutes the load across multiple instances, and across availability zones
Can handle instance failures by doing regular health checks
Only exposes a single endpoint (DNS) to your appliction

Type | Description
--- | ---
Application Load Balancer (ALB) |  Handles HTTP/HTTPS traffic, Layer 7.
Network Load Balancer | Handles TCP-UDP-TLS, Ultra-high performance, ultra-low latencies.
Gateway Load Balancer | Used to deploy and manage third-party virtual appliances usch as firewalls, intrusion detection and prevention systems
Classic Load Balancer | Previous genertion load balancer for use with the EC2-Classic network

---

### Auto Scaling Groups (ASG)

Automatically scale out/in instances based on the load

	- Specify instance numbers: desired capacity, minimum and maximum.
	- Registers new instances with the load balancer

Replace unhealthy instances automatically
Run at optimal capacity, meaning cost savings 

--- 

### AWS Elastic Beanstalk (Magic trick for developer to avoid headache)

#### Platform as a Service (PaaS)

	- Infrastructure is handled for you
		- EC2 instances, load balancers, auto-scaling groups, database, etc...
	- Uses CloudFormation templates to deploy the infrastructure.

#### Health monitoring available in the Console

#### Support for many platforms
	- Node, PHP, Java, Python, Go, .NET, Ruby, Docker, etc...


---

###  AWS Batch
Managed service for running batch jobs
	- Deep learning, big data, media encoding, image processing, email daily reports, etc..

You create the batch jobs (scripts, business logic)
	- Defined as Docker images

AWS handles everything else (instances, scheduler, queues, retries, etc...)
	- Processing at scale, optimized for the work load

---

### AWS Lightsail

**AWS** *lite*

	- Meant for people with little to no cloud experience

Good for simple applications and websites
Pricing

	- Predictable
	- Less expensive

---

### Amazon WorkSpaces

Desktop in the cloud

	- Employees and contractors can easily access applications and desktops from anywhere.

Windows and linux operating systems, with common app bundles (LibreOffice, Microsoft Office, browsers, antivirus, etc...)

Replaces on premises Virtual Desktop Infrastructure (VDI)

---

### AWS Lambda

~~Serverless computing~~
Its a code that runs on a server you don't have to buy or manage, in response to some event.
Can also be though of as *Scripts* or *Functions*

	- Single purpose
	- Right-sized
	- Easy to scale (up AND down)


#### Shared Responsibility Model for Lambda

AWS Respnsibility | Customer (Your) Responsibility
--- | ---
Underlying infrastructuer | Security of your code
Operating systems | Storage and access of data
Application platform | Identity and access management

---

### Docker
Underlying container technology used in AWS 
Docker images are read-only templates/blueprints used to create Docker containers

	- Created only once
	- Stored in Docker repositories

Docker containers are running instance of an image

	- Create multiple containers from the same image.

### Amazon Elastic Container Service (ECS)
Used to run, stop and manage Docker conatiners in AWS
Integrated with many AWS services, including IAM, load balancers, auto scaling, VPC, etc...
Created by AWS.

### Amazon Elastic Kubernetes Service (EKS)
**Kubernetes as a service** on AWS

	- Kubernetes is an open source container orchestration platform 
	- Automates deploying, scaling, management and scheduling of containers
	- Originally built by Google
	- Has large community and support

AWS installs, operates, and maintains the Kubernetes cluster/nodes

### Two Options for Running ECS/EKS
EC2 instances | Fargate
--- | ---
You provision and maintain the EC2 instaces that the containers run on | Serveless solution, AWS handles the underlying infrastructure.

### Amazon Elastic Container Registry (ECR)
Private Repository on AWS for Docker images.
ECS, EKS pull images from here to build containers.

---

## Storage

### Simple Storage Service (S3)
Inexpensive object (think *file*) storage in AWS
**Unlimited** storage capacity
Organized by **buckets**

	- Easy to scale
	- Reliable
	- Inexpensive

### S3 Transfer Accelartion
Speeds up content transfers by as much as 50-500% for larger objects
Routes traffic through CLoudFront edge locations
Enabled at the bucket level

### Elastic Block Store (EBS)

#### Storage for an EC2 instance

	- Think of this as a virtual hard drive
		- Attached over the network (not physically)
	- Root Volume created for an EC2 instance; can add additional volumes as needed
	- A volume can only be attached to one instance at a time
	- Must be in the same availability zone as the instance

#### Default persistence settings

	- Persists when an instance is shut down
	- Deletes when an instance is terminated

#### Can create a snapshot of a volume and then restore it

	- Stored in S3
	- Useful for backup/recovery or copying to another availability region

### Elastic File System (EFS)

Storage for an EC2 instances, containers, lambda functions, on-premises servers

	- Can be used by Multiple things at a time
	- Can be used across Multiple availability

Only pay for the storage you use (no up-front provisioning)

### Amazon FSx
Fully managed third-party file systems

	- Benifits of the cloud (replication, high availability, etc..), but also features specific to the third-party (Active Directory integration, NTFS, etc...)

Amazon FSx for windows File Server (*Built on Windows Server*)
Amazon FSx for Lustre (High-performance file system built on linux)


### AWS Storage Gateway 
Used in a hybrid architecture, to store data in AWS from on-premises

### AWS Snow Family 
Physical storage devices used to transfer massive amounts of data (Snowcone, Snowball, Snowmobile)

### AWS Backup

---

### Virtual Private Cloud 
Your own private cloud/network within the cloud Isolates your resources from everyone else's