# Hands-On OCI Projects: Practical Learning with Oracle Cloud Infrastructure

This repository contains complete **step-by-step guides** and resources for learning **Oracle Cloud Infrastructure (OCI)** through real, hands-on projects — all using the **Always Free Tier**.

Whether you're new to cloud or preparing for OCI certifications, the best way to learn is by building!

### Current Projects

1. **IAM: Building a Secure Development Environment from Scratch**  
   Master OCI **Identity and Access Management (IAM)** by creating a secure, isolated setup with compartments, identity domains, users, groups, and least-privilege policies.  
   **Folder:** `oci-iam-hands-on/`

2. **Load Balancing with Apache Web Servers**  
   Build a highly available web application using OCI **Load Balancer** and **Weighted Round Robin** policy.  
   Learn private subnets, backend sets, health checks, and public access through a load balancer.  
   **Folder:** `load-balancer-apache/`

3. **Metric-Based Autoscaling with Compute Instance Pool**  
   Create a dynamic, auto-scaling compute environment that automatically adds or removes instances based on **CPU utilization**.  
   Includes VCN setup, flexible load balancer, custom image, instance pool, autoscaling policy, and real load testing using **stress-ng**.  
   Perfect for learning elasticity, cost optimization, and high-availability in OCI — 100% on Free Tier!  
   **Folder:** `oci-autoscaling-metric-based/`

### Why These Projects?

- **IAM** → Security foundation every cloud engineer must master  
- **Load Balancing** → Core networking & high-availability skills for production workloads  
- **Autoscaling** → Elasticity & resource optimization – handle traffic spikes automatically without manual intervention  
- All projects are **100% doable on OCI Always Free Tier**  
- Follow real-world best practices (least privilege, private/public subnets, traffic distribution, metric-based scaling)

### Recommended Learning Path

1. Start with **IAM** (security first!)  
   → `oci-iam-hands-on/`

2. Then build the **Load Balancer + Web Servers** project  
   → `load-balancer-apache/`

3. Finish with **Metric-Based Autoscaling**  
   → `oci-autoscaling-metric-based/`  
   (This project builds nicely on the previous two — it reuses VCN, load balancer, and compute concepts!)

Each project folder contains:
- Detailed **README.md** with step-by-step instructions  
- **Screenshots/** subfolder for visual walkthroughs  
- Ready-to-use configuration files, policy statements, and scripts (where applicable)

### Prerequisites (for all projects)

- Free OCI account (Always Free tier)  
- Access to OCI Console  
- Basic familiarity with the OCI Console (you'll learn as you go!)

Happy building and learning! ☁️🚀

Feel free to open issues or PRs if you'd like to contribute more projects or improvements.
