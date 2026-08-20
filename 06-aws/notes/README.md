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

  
