# AWS 

- AWS stands for Amazon Web services, its a cloud provider that provides computing resources over the internet.



# AWS Use Cases 

- AWS enables you to build sophisticated, scalable applications.
- Use Cases include:
  . Enterprise IT, backup & storage, Big data analytics
  . Website hosting, mobile & social apps
  . Gaming

# AWS Regions

- A region is a cluster of data centres
- Having multiple regions ensures things run smoothly for example if one region goes down AWS can automatically switch to another.
- AWS Region is all about giving you control of where your data and services live.

# How to choose an AWS Region ?

. Compliance with data governance and requirements: data never leaves a region without your explicit permission
. Proximity to customers: reduced latency 
. Available services within a region: not every service or feature would be available in your region.
. Pricing: pricing varies region to region so its important from an angle of scaling a business 

# AZ

- Each AWS region is made up of many availability zones
- AZ is one or more discrete data centres with redundant power, connectivity and networking.

# Edge Location 

- Edge location is where physical server resources are deployed close to end users for low latency access.

# IAM Permissions 

- Users on groups on AWS can be assigned JSON documents called policies, these policies define permissions of the users.
- In AWS we apply the least privilege principle which means only giving user access to what they need.

<img width="536" height="299" alt="image" src="https://github.com/user-attachments/assets/d66b4a0b-e96e-4247-97b2-2d410fa2908a" />

- Having MFA on your root account is crucial from a security standpoint as you don't want a user accessing your account and making changes such as deleting resources in your AWS account. 

  
# How users can access AWS ?

- Users can access AWS using three ways
  . AWS management console which is protected by password + MFA
  . AWS Command Line Interface - protected by access keys which are generated using the console
  . AWS Software Development Kit - This is where you programmatically interact with AWS which is also protected by access keys.

# AWS CLI 

- AWS CLI allows you to automate tasks by running scripts rather then manually provisioning resources which also known as click ops.

# AWS SDK 

- In simple words AWS SDK is a bunch of programming languages  that allows you to interact with AWS services and build powerful cloud integration apps. 

  
# IAM Security Tools 

- IAM Credential Report (account level) : It gives you a snapshot of all the users in your AWS account and the status of the various credentials.
- IAM Access Advisor (user-level) : It shows the permissions granted to a user and when those services were last accessed, you can use this information to revise your policies. 

# Amazon Compute 

- Compute is essentially the power behind running your application.

# EC2 

- EC2 stands for Elastic Compute Cloud, its part of infrastructure as a service
- Its allows you to do the following things:
  . Rent Virtual Machines (EC2)
  . Store data on virtual drives (EBS)
  . Distribute load across machines
  . Scaling services using auto-scaling groups

# EC2 User Data 

- It is possible to bootstrap our instances using an EC2 User data script, bootstrapping means launching commands when a machine starts.
- EC2 User data is used to automate boot tasks such as:
  . Installing updates
  . Installing software
  . Downloading common files from the Internet

# EC2 Instance Types 

- General Purpose: These are well rounded EC2 instances and can be used for many use cases for example your in a web server, small database or other workloads.
- Compute Optimised: If you need lots of processing power these are quite useful, these instances give you extra CPU for tasks like heavy calculation, batch processing or even high promise computing
- Memory Optimised: When you application needs a lot of memory or RAM you go for these
- Storage Optimised: These are designed for fast and high throughput storage, if your dealing with large datasets or running databases that require access to storage, these instances are the right choice.
- Accelerated Computing: If you are doing machine learning, video streaming or scientific simulations, these are what you need
- HPC Optimised: HPC stands for high performance computing, its designed for intensive computing tasks that requires lots of powerful processing.

Naming convention:

<img width="422" height="76" alt="image" src="https://github.com/user-attachments/assets/7732ff87-1b51-47f8-a164-a69f52554059" />


# EC2 Instance Purchasing options 

<img width="479" height="266" alt="image" src="https://github.com/user-attachments/assets/7552a3b0-0f2b-49f6-8017-244560f7fcc7" />

# Security Groups

- Security groups are the  fundamental in the network security in AWS.
- They control how traffic is allowed in and out of an EC2 instance.
- Security groups only deal with allow rules, in comparison with firewalls where you can have both allow and deny rules.
- Security groups are stateful, that means if you allow inbound traffic the corresponding outbound traffic is automatically allowed.
- Security groups regulate access to ports and authorised IP's

# Security Groups (Good to Know)

- SG's can be attached to multiple instances
- If your application is not accessible its a security group issue.
- All inbound traffic is blocked by default
- All outbound traffic is allowed by default

# Elastic IP

- In AWS When you stop and start an EC2 instance it can change its public IP.
- If you need to have a fixed public IP for your instance, you need an elastic IP
- Elastic IP is a public IPV4 address you own as long as you don't delete it
- You can attach it to one instance at a time. 

# EBS Volume

- EBS Volume is like a network drive you can attach to your EC2 instance.
- It allows your instances to persist data even if you have terminated or stopped it.
- Each EBS Volume is bound to a specific availability zone
- EBS Volume is ideal if you want to store data for a long period of time for databases or logs, it ensures your data is kept safe.


# AMI (Amazon Machine Image)

- AMI is a preconfigured template that contains all the information needed to launch an instance such as your OS, software configuration, monitoring tools and more.
- In simple words AMI allows you to automate the setup of your EC2 instance.

# Amazon EFS- Elastic File System

- Its a managed network file system which allows you to create a shared file system that can be mounted across multiple instances at the same time.
- It is designed to be used in multi AZ setups making it durable and reliable.
- It can be quite expensive
- Its best to use it when your application needs shared storage across multiple instances.

  # Scalability & High Availability

- Scalability means an application/ system can handle greater loads by adapting.
- There are two kind of Scalability:
  . Vertical Scalability
  . Horizontal Scalability
- High Availability ensures your application keeps running even when parts of it fails.

# Vertical Scalability  

- Vertical Scalability means increasing the size or power of your instance.
- For example, you have an application running on t2.micro and you want to scale it to t2.large this is known as vertical scalability.
- We tend to use Vertical Scalability when for non-distributed systems such as databases
- There is usually limit to how much you can scale before you start looking at different scaling options.


# Horizontal Scalability 

- Horizontal Scalability is to increase the number of instances in your application or system to handle more load.
- Horizontal Scalability implies distributed systems, for example instead of relying one powerful machine you spread the workload across multiple smaller ones.
- It's particularly common for web applications and cloud based systems.
- It adds resilience to your system, so if one fails the other can take over.

# High Availability

- High Availability is running your application or systems in multiple locations to ensure that if one part fails the other can take over.
- It goes hand in hand with horizontal scaling, the main objective of HA is to survive a data centre loss. 

# Load Balancing

- Load Balancing is a way to distribute traffic across multiple servers or instances
- The load balancer checks which instance is healthy and automatically directs traffic towards it.
- Reverse proxies are similar to load balancers but with extra functionality , they are key to building scalable and resilient applications.

# Why use a Load Balancer ?

- The primary purpose of a load balancer is to distribute incoming traffic across multiple instances. This prevents any one instance from being overloaded.
- It seamlessly handles instance failures
- Load Balancers constantly checks the health of your instances.
- It provides SSL termination for your instances
- Enforces stickiness with cookies
- Ensures HA across zones
- It can separate public and private traffic

# Why use an Elastic Load Balancer ?

- Elastic load balancer is a managed load balancer.
   . AWS guarantees it will be working
   . It also handles upgrades, maintenance and high availability
   . It is fully integrated with other AWS services making it a powerful option.   
  
# Health Checks 

- Health checks enable a load balancer to know if the instance they are forwarding traffic to are healthy.
- It does this by sending a request to a certain port/route
- Response 200 indicates the instance is healthy.

# Application Load Balancer (ALB)

- ALB operates on the 7th layer
- It has the ability to load traffic to multiple HTTP applications across different instances all within target groups.
- It can also load balance traffic across multiple HTTP applications on the same machine, this is super useful in environments like containers.
- ALB is perfect for microservices and container based applications
- When running ECS, ALB has a feature called port mapping which allows it  to dynamically redirect traffic to containers running on different ports.
- Thanks to its routing features ALB can handle multiple applications on a single load balancer whereas a classic load balancer can only handle one application. This is a massive improvement in terms of cost and infrastructure management 
