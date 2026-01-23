# OCI Load Balancer with Apache Web Servers (Hands-On Project)

![OCI Load Balancer](https://img.shields.io/badge/Oracle%20Cloud%20Infrastructure-Load%20Balancer-blue?style=for-the-badge&logo=oracle&logoColor=white)
![Free Tier](https://img.shields.io/badge/Always%20Free%20Tier-Enabled-success?style=for-the-badge)

This project shows how to build a **highly available web application** using **Oracle Cloud Infrastructure (OCI) Load Balancer** — 100% on the **Always Free Tier**.

### What You'll Build

- A **Virtual Cloud Network (VCN)** with **public** and **private subnets**
- **Two Apache web servers** running on Compute Instances in a **private subnet**
- A **public Flexible Load Balancer** distributing traffic using **Weighted Round Robin** policy
- Simple web pages served through the Load Balancer's **public IP**

### Learning Objectives

- Understand **public vs private subnets** for security
- Configure a **Load Balancer** and attach **backend sets**
- Use **Weighted Round Robin** load balancing policy
- Set up **health checks** for automatic failover
- Experience basic **high availability** in the cloud

### Prerequisites

- **Free OCI Account** (Always Free Tier)
- Access to the **OCI Console**
- (Optional) SSH client for instance access

### Step-by-Step Guide

1. **Create VCN & Subnets**
   - Create a new **VCN**
   - Add a **public subnet** (for the Load Balancer)
   - Add a **private subnet** (for Compute Instances)
   - Set up **Internet Gateway** + **Route Table** for the public subnet
   - Configure **Security Lists** to allow HTTP (port 80) from the Load Balancer to the private subnet

2. **Launch Two Compute Instances**
   - Use an **Always Free eligible** shape (e.g., VM.Standard.A1.Flex – 1 OCPU, 6 GB RAM)
   - Place both instances in the **private subnet**
   - Use the same **Availability Domain** (Free Tier limitation)
   - Use the same **SSH key** for both instances
   - Install and start **Apache** on each instance:

   (Recommended) Customize the default page to identify each server:Bash

    On Server 1
      echo "<h1>Server 1 - Instance A</h1>" | sudo tee /var/www/html/index.html

    On Server 2
      echo "<h1>Server 2 - Instance B</h1>" | sudo tee /var/www/html/index.html


3. **Create the Load Balancer**
  -  Navigate to Networking → Load Balancers in the OCI Console
  -  Click Create Load Balancer
  -  Choose Flexible Load Balancer (public)
  -  Select your VCN and the public subnet
  -  Choose Weighted Round Robin as the load balancing policy
  -  dd a Listener:
  -  Protocol: HTTP
  -  Port: 80


4. **Configure Backend Set**
   - Create a new Backend Set
   - Name it (e.g., apache-backend-set)
-Protocol: HTTP
Port: 80
Health Check:
Type: HTTP
Path: /
Port: 80

Add both Compute Instances as Backends
Assign weights (example: 1 for Server 1, 2 for Server 2 to demonstrate weighted distribution)

Test Your Load Balancer
Copy the Public IP address of the Load Balancer (found on the Load Balancer details page)
Open your browser and visit:
http://<load-balancer-public-ip>
Refresh the page multiple times — you should see responses alternating between Server 1 and Server 2
With different weights (e.g., 1 vs 2), you’ll notice one server appears more frequently
