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
