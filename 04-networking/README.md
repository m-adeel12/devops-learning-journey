## EC2 + NGINX + Custom Domain Deployment

## Overview 

This project demonstrates deploying a public web server using AWS EC2, installing NGINX, and connecting it to a custom domain using Route 53.
It combines key networking concepts: IP addressing, routing, DNS, ports, and basic hosting.

## Architecture 

User → Domain → Route 53 A Record → EC2 Public IP → NGINX Web Server

## 1. Domain Purchase (Route 53)

I purchased a domain using AWS Route 53.

<img width="956" height="499" alt="image" src="https://github.com/user-attachments/assets/29a6e5fc-7c3d-4f1e-ab98-0c5db8df5792" />

## Launching the EC2 Instance

## Configuration

-  AMI: Amazon Linux 2 / Ubuntu
-  Instance type: t2.micro
-  Security Group:
   HTTP (80) → 0.0.0.0/0
   SSH (22) → My IP only

## Public IP 

Found under EC2 → Instances → Instance Summary → Public IPv4 address


<img width="940" height="473" alt="image" src="https://github.com/user-attachments/assets/0a752818-3052-4cf2-b9ee-afa46d9abe73" />


<img width="940" height="407" alt="image" src="https://github.com/user-attachments/assets/f9efd31e-e555-40e4-ba2c-61928ddccab8" />





  
