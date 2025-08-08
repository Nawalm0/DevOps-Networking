# DevOps-Networking

## Overview

This project demonstrates how to deploy an NGINX web server on an Amazon EC2 instance and configure a custom domain using AWS Route 53.

## Objectives
- Register a domain via Route 53  
- Launch and configure an EC2 instance  
- Install and run NGINX  
- Set up a DNS A record pointing to the EC2 instance  
- Serve the default NGINX page at: http://nginx.nawalay.com/

## Tech Stack
- AWS EC2 – Amazon Linux 2023 (t2.micro instance)
- NGINX – Web server
- AWS Route 53 – Domain registration and DNS management
- SSH – Secure shell access using a key pair

## Setup Steps
1. Domain Registration
- Purchased domain http://nginx.nawalay.com/ via Route 53.

2. EC2 Instance Creation
- AMI: Amazon Linux 2023
- Instance Type: t2.micro
- Security Group Inbound Rules:
     Port 22 (SSH) – Your IP
     Port 80 (HTTP) – 0.0.0.0/0
     Port 443 (HTTPS) – 0.0.0.0/0
  
3. NGINX Installation (Manual via SSH)
sudo yum install nginx -y sudo systemctl start nginx


4. DNS Setup in Route 53
- Created an A Record pointing to the EC2 instance's public IPv4 address
- Domain now serves the default NGINX page at: http://nginx.nawalay.com/
