## EC2 + NGINX + Custom Domain Deployment

## Overview 

This project demonstrates deploying a public web server using AWS EC2, installing NGINX, and connecting it to a custom domain using Route 53.
It combines key networking concepts: IP addressing, routing, DNS, ports, and basic hosting.

## Architecture 

User → Domain → Route 53 A Record → EC2 Public IP → NGINX Web Server

## 1. Domain Purchase (Route 53)

I purchased a domain using AWS Route 53.

<img width="956" height="499" alt="image" src="https://github.com/user-attachments/assets/29a6e5fc-7c3d-4f1e-ab98-0c5db8df5792" />

## 2. Hosted Zone Setup (Route 53)

After purchasing my domain madeelcloud.com, I created a Public Hosted Zone in Route 53.
This hosted zone stores all DNS records for the domain.





  
