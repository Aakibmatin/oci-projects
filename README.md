# Hands-On OCI IAM: Building a Secure Development Environment from Scratch

![OCI Console Dashboard](https://blogs.oracle.com/wp-content/uploads/sites/83/2025/10/Dashboard-overview-1.png)
*(Example of OCI Console Dashboard – your actual screenshots will look similar!)*

This repository contains a complete step-by-step guide and resources for learning **Oracle Cloud Infrastructure (OCI) Identity and Access Management (IAM)** through practical, hands-on exercises.

If you're new to OCI, the **best way to learn** is by doing — especially starting with IAM. This project helps you understand the core concepts of **authentication** (who you are) and **authorization** (what you can do) by creating a secure, isolated development environment.

### Why Start with IAM?
- IAM is the foundation of security in OCI
- Teaches **compartments**, **identity domains**, **users**, **groups**, and **policies**
- Follows the principle of **least privilege**
- Prevents costly security mistakes later

### What You'll Build
A mini secure setup simulating a real dev team:
1. Isolated **Compartment** for development resources
2. Dedicated **Identity Domain**
3. New **User** with email-based login
4. **Group** for managing permissions
5. Targeted **IAM Policies** for day-to-day tasks (e.g., manage compute instances, block volumes)
6. Test login and resource access

### Prerequisites
- Free OCI account (Always Free tier is perfect!)
- Access to OCI Console
- A personal email address (for user creation & verification)

### Step-by-Step Hands-On Guide

1. **Create a Compartment**  
   Organize and isolate resources  
   → Identity & Security → Compartments → Create Compartment  
   Name: `Development-Compartment`

   ![OCI Compartment Example](https://k21academy.com/wp-content/uploads/2018/11/Compartment-in-OCI-3.png)

2. **Create an Identity Domain**  
   A dedicated space for users & groups (free tier available)  
   → Identity & Security → Domains → Create Domain  
   Name: `Development-Domain`

   ![OCI Identity Domains](https://docs.oracle.com/en-us/iaas/Content/Resources/Images/ociiam-domains.jpg)

3. **Create a User in the Domain**  
   → In your new domain → Users → Create User  
   - Use real email  
   - Enable MFA (recommended)  
   - Complete email verification

   ![OCI User Creation](https://docs.oracle.com/en-us/iaas/visual-builder-studio/doc/img/id-domains-example-user.png)

4. **Create a Group & Add the User**  
   → In the domain → Groups → Create Group  
   Name: `Dev-Admins`  
   → Add your new user to the group

5. **Assign IAM Policies**  
   → Identity & Security → Policies (in root compartment)  
   → Create Policy inside `Development-Compartment`  
   Example policy statements (copy-paste friendly):

   ```plaintext
   Allow group Dev-Admins to manage instance-family in compartment Development-Compartment
   Allow group Dev-Admins to manage volume-family in compartment Development-Compartment
   Allow group Dev-Admins to read object-family in compartment Development-Compartment
