## EC2 + NGINX + Custom Domain Deployment

## Overview 

This project demonstrates deploying a public web server using AWS EC2, installing NGINX, and connecting it to a custom domain using Route 53.
It combines key networking concepts: IP addressing, routing, DNS, ports, and basic hosting.

## Architecture 

User → Domain → Route 53 A Record → EC2 Public IP → NGINX Web Server

## 1. Domain Purchase (Route 53)

I purchased a domain using AWS Route 53.

<img width="956" height="499" alt="image" src="https://github.com/user-attachments/assets/29a6e5fc-7c3d-4f1e-ab98-0c5db8df5792" />

## 2. Launching the EC2 Instance

## Configuration

-  AMI: Amazon Linux 2 / Ubuntu
-  Instance type: t2.micro
-  Security Group:
   HTTP (80) → 0.0.0.0/0
   SSH (22) → My IP only

## Public IP 

Found under EC2 → Instances → Instance Summary → Public IPv4 address


<img width="956" height="490" alt="image" src="https://github.com/user-attachments/assets/7392effc-6221-44b6-ae6d-768fa3cb66bf" />


<img width="958" height="456" alt="image" src="https://github.com/user-attachments/assets/3e767367-8b9e-4d49-aac8-bb3c2fa41b25" />

## 4. Installing NGINX

<img width="938" height="413" alt="image" src="https://github.com/user-attachments/assets/36685934-14f0-4361-8548-fe8cf6af79bf" />

## 5. Test NGINX Using EC2 IP

<img width="956" height="518" alt="image" src="https://github.com/user-attachments/assets/fa7590e7-0eaf-4668-8a79-deb1ca356126" />

## 6. Route 53 DNS Configuration

I created an A Record pointing my domain to the EC2 public IPv4 address.

<img width="950" height="438" alt="image" src="https://github.com/user-attachments/assets/3f3e4636-2c4c-40cc-9cf1-a4a312bd8274" />

## 7. Test the Domain

<img width="959" height="511" alt="image" src="https://github.com/user-attachments/assets/b2a74293-0dc3-4737-9b31-13ea77837cc7" />

## What I Learned
-How DNS resolves domains to IPs

- How routing directs traffic to EC2

- How ports (80/443) control web access

- How NGINX serves content

- How cloud hosting works end‑to‑end

- How Route 53 connects domain → server


##  Future Improvements
- Add HTTPS using AWS Certificate Manager

- Deploy a custom HTML page

- Add a load balancer

- Automate deployment with Terraform

- Add CI/CD pipeline for automatic updates
