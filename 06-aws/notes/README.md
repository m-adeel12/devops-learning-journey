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
- It has the ability to load traffic to multiple HTTP applications across different machines all within target groups.
- It can also load balance traffic across multiple HTTP applications on the same machine, this is super useful in environments like containers.
- ALB is perfect for microservices and container based applications
- When running ECS, ALB has a feature called port mapping which allows it  to dynamically redirect traffic to containers running on different ports.
- Thanks to its routing features ALB can handle multiple applications on a single load balancer whereas a classic load balancer can only handle one application. This is a massive improvement in terms of cost and infrastructure management

# Application Load Balancer (HTTP Based Traffic)

- Users send HTTP request to the ALB which then routes those requests to the appropriate target groups based on its writing rules, now these target groups could consist of EC2 instances or even other resources like lambda or ECS. These target groups are tied to certain services
- One target group could handle user related tasks such as logging, and another target group could handle things like product searches.

# Application Load Balancer (Target Group)

- Target groups are essentially the groups of resources like EC2 instances, lambda, ECS that ALB routes traffic to based off certain route paths or writing rules.

# Application Load Balancer (Good to Know)

- ALB gives each load balancer a fixed hostname
- The application servers don't see the IP of the client directly
- The true IP of the client is inserted in to the header X-forwarded-Fo
  
  
# Network Load Balancer 

- Network load Balancers are optimised for handling extreme performance and high traffic with low latency.
- They operate at layer 4 of the OSI model, which means it handles TCP/UDP traffic.
- It is designed for high performance use cases when you want to handle millions of requests per second
- NLB assigs one static IP address per AZ
- NLB doesn't inspect HTTP headers or handle SSL termination, which is different from ALB. Its all about efficiently forwarding traffic without modifying it making it fast and more reliable.

# Sticky Sessions (Session Affinity)

-  Sticky session ensures the client is routed to the same instance behind a load balancer.
-  Behind the scenes, a load balancer uses a cookie to keep track of which instance a client is connected to. You can set an expiration date to control how long the cookie or stickiness lasts.
-  Its primarily used so that the user doesn't lose their session data, for example they have carted an item and they want to keep their session open in order to make the necessary payment.
-  Enabling stickiness may cause load over the backend of EC2 instances which can significantly affect performance.

# SSL/TLS Basics 

- SSL stands for secure socket layer
- SSL certificate allows traffic between your client and load balancer to be encrypted in transit.
- TLS stands for transport layer security, its the newer version of SSL.
- Public SSL certificate are issued by certified authorities (CA)
- Some common CA's are Comodo, Symantec, GoDaddy, GlobalSign etc.
- SSL certificates have an expiration date and must be renewed.

# Load Balancer - SSL Certificate 

- Load balancers are basically the middleman ensuring traffic between your users and instances are encrypted.
- This is done using an X.509 certificate
- AWS allows us to manage these certificates by using an ACM (Amazon Certificate Manager)
- Its a one stop shop for creating, renewing and managing certificates.
- When your setting up a HTTPS listener on your load balancer this is how you ensure traffic is encrypted.
  . You must specify a default certificate
  . You can add an optional list of certs to support multiple domains
  . Clients use SNI to specify the hostname they reach.
  . Ability to specify a security policy to support older versions of SSL/TLS certificate. 
  
# SNI - Server Name Indication 

- SNI solves the problem of loading multiple SSL certificates onto one web server
- When your client makes the first connection to the web server, it sends the hostname of the website is trying to reach as part of the SSL handshake. The server uses this info to find the right SSL certificate for that website. If the server cant find a match it would then use the default certificate.
- SNI only works with ALB and NLB's supporting multiple SSL certificates across different domains under one load balancer.


# Connection Draining 

- Connection Draining in AWS is a feature that allows a load balancer to gracefully remove an EC2 instance without dropping active user requests.
- It ensures that when an  instance is  being removed, any in flight connections are allowed to finish before the instance is taken fully out of service.
- Without connection draining, existing user requests get cut off, causing errors.
- The Allowed range is between 1 -3600 seconds
- For CLB's this is referred to connection draining.
- For ALB's and NLB's this is referred to Deregistration delay.
  
# Auto Scaling Group

- The primary purpose of an auto scaling group is to adjust the number of running EC2 instances based on load.
- If your traffic increases, the ASG will scale out which means it will add more EC2 instances to meet up with the demand.
- When the load decreases the ASG will; scale in meaning it will reduce the number of EC2 instances.
- ASG's can automatically register new instances to load balancers.
- The best part of it all is that ASG's are free.

# Auto Scaling Group in AWS 

- Auto Scaling groups operate based off three things - minimum capacity, desired capacity and maximum capacity
- Minimum Capacity- is the least number of EC2 instances you want running even during low traffic times
- Desired Capacity- is your target number of instances for normal load.
- Maximum Capacity- this is the most  number of instances your allowing the ASG to scale up to during high periods of traffic.
- Scaling ensures your application runs smoothly during busy times and saves money when the demand drops. 
  
