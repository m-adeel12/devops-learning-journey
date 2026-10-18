# AWS Custom VPC Lab — Public & Private Subnets, NAT Gateway, EC2 Instances

This project demonstrates how to build a custom VPC with a public subnet, private subnet, proper internet routing, and EC2 instances deployed across them.
It’s designed as a hands‑on networking lab to show real AWS fundamentals — not just clicking around.

# Architecture Overview

This lab builds the following environment:

VPC: 10.0.0.0/16

Public Subnet: 10.0.1.0/24

Private Subnet: 10.0.2.0/24

Internet Gateway for public subnet outbound access

NAT Gateway for private subnet outbound access

Route tables configured for correct routing

EC2 Instances:

Public EC2 (with public IP)

Private EC2 (no public IP)

Security Groups enforcing least‑privilege access

# 1. Creating the VPC

I started by creating a custom VPC with the CIDR block 10.0.0.0/16.

<img width="776" height="419" alt="image" src="https://github.com/user-attachments/assets/bdefb289-b528-41f2-ac2a-8ea964f4aa7b" />

# 2. Creating the Subnets

I created two subnets:

Public Subnet: 10.0.1.0/24

Private Subnet: 10.0.2.0/24

I also enabled Auto‑assign public IPv4 on the public subnet so instances launched there automatically get a public IP.

<img width="764" height="149" alt="image" src="https://github.com/user-attachments/assets/74b7fe7f-99ee-4973-bf90-dd35fa84e7fc" />

<img width="746" height="403" alt="image" src="https://github.com/user-attachments/assets/52e62fdc-a128-4cc7-89f9-f7897e08b7e8" />



<img width="735" height="396" alt="image" src="https://github.com/user-attachments/assets/f2c70ea4-74ce-4313-847f-f847510fb5f6" />

# 3. Internet Gateway & NAT Gateway

I created an Internet Gateway and attached it to my VPC.
Then I allocated an Elastic IP and used it to create a NAT Gateway inside the public subnet.

<img width="766" height="256" alt="image" src="https://github.com/user-attachments/assets/e2836928-27b5-45a3-b833-3776af5626a2" />


<img width="768" height="431" alt="image" src="https://github.com/user-attachments/assets/44c7de60-460c-4370-8f32-0baecdc230f0" />


# 4.  Route Tables


I created two route tables:

Public Route Table
Associated with the public subnet

Default route → Internet Gateway

Private Route Table
Associated with the private subnet

Default route → NAT Gateway

<img width="767" height="389" alt="image" src="https://github.com/user-attachments/assets/f1bca5b2-f462-4091-961c-a6783d0f5bdd" />


<img width="759" height="380" alt="image" src="https://github.com/user-attachments/assets/f400d870-2dca-4885-aee1-6b095394a5d4" />


# 5. EC2 Instances

I launched two EC2 instances:

Public EC2
In the public subnet

Public IP enabled

Security group only allows SSH from my IP (and HTTP if needed)

Private EC2
In the private subnet

No public IP

Security group only allows SSH from the public EC2’s security group

<img width="748" height="407" alt="image" src="https://github.com/user-attachments/assets/47c29ca7-7bc1-46b1-8e98-36d714653396" />


<img width="738" height="405" alt="image" src="https://github.com/user-attachments/assets/914c7dcf-7e93-4bdd-baa9-d9250da2bb46" />

<img width="770" height="369" alt="image" src="https://github.com/user-attachments/assets/acc9d179-02f2-4ede-ab09-9dabcb941e07" />

<img width="767" height="354" alt="image" src="https://github.com/user-attachments/assets/e5debceb-e8a2-4915-83b6-42767695c89b" />

# 6. Connectivity Tests

SSH into Public EC2
I connected from my laptop to the public EC2 using SSH.

<img width="612" height="217" alt="image" src="https://github.com/user-attachments/assets/e016bac8-7245-403a-8b5f-92e23fd21630" />


SSH from Public EC2 → Private EC2
I then SSH’d into the private EC2 from the public EC2.


Private EC2 Internet Access via NAT
I tested internet access from the private EC2 using:

<img width="530" height="44" alt="image" src="https://github.com/user-attachments/assets/7b3fff89-456b-4104-8e28-64ebb3193202" />


# 7. What I Learned

In my own words:

I understand how public and private subnets work in a VPC.

I learned why a NAT Gateway is required for private instances to reach the internet.

I saw how route tables control traffic flow.

I reinforced the idea of least‑privilege security using security groups.

I practiced SSH chaining (jumping from public EC2 → private EC2).

# 8. What I Want to Improve Next Time
I want to push this lab further next time. Here’s what I plan to improve:

Technical Improvements
Build the entire VPC using Terraform instead of the console.

Add a proper Bastion Host instead of using the public EC2 as a jump box.

Enable VPC Flow Logs to monitor traffic.

Add CloudWatch Agent for memory and disk metrics.

Add NACLs to compare with security groups.

Add S3 VPC Endpoint to avoid NAT Gateway costs.

Add a Load Balancer + Auto Scaling Group to simulate a real production setup.
