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

