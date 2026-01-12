# OCI Hands-On: Creating an Identity Domain

This guide walks you through creating an **Identity Domain** in Oracle Cloud Infrastructure (OCI) — a key step for managing users, groups, and advanced authentication separately from the default domain.

Identity Domains are dedicated containers for users, groups, roles, federation, MFA, and more. They allow you to isolate identity management (e.g., for development teams or external users) while keeping everything secure and organized.

### Why Create an Identity Domain?
- Separate user populations (e.g., dev vs. production users)
- Enable advanced features like MFA, SSO, or federation
- Use "Free" type for learning/experiments (no extra cost)
- Better control over security policies per domain

### Prerequisites
- OCI account (Free Tier is sufficient)
- Administrator access to the OCI Console
- A compartment ready (recommended: create it in your Development-Compartment)

### Step-by-Step Guide to Create an Identity Domain

1. **Log in to the OCI Console**  
   Go to [https://cloud.oracle.com](https://cloud.oracle.com) and sign in.

2. **Navigate to Domains**  
   - Click the navigation menu (☰) in the top-left  
   - Select **Identity & Security**  
   - Under **Identity**, click **Domains**  
   You'll see the Default domain and any existing ones.

   ![OCI Domains List](https://docs.oracle.com/en-us/iaas/Content/Resources/Images/ociiam-domains.jpg)  
   *Example: Domains overview page*

3. **Start Creating the Domain**  
   - Click **Create domain**

4. **Fill in the Details**  
   - **Display Name**: e.g., `Development-Domain` (letters, numbers, hyphens, periods, underscores only)  
   - **Description**: e.g., `Identity domain for development users and testing`  
   - **Compartment**: Select your compartment (e.g., Development-Compartment)  
   - **Domain Type**: Choose **Free** (perfect for learning and hands-on)  
   - **Administrator Details** (optional for Free):  
     - You can create a new admin user (provide name, email) or skip and use your current admin  

5. **Create It!**  
   - Click **Create**  
   - The domain status will show **Creating** → wait a few minutes until it becomes **Active**

### Tips & Best Practices
- Use **Free** domain type for experiments — it includes MFA support  
- Place the domain in a non-root compartment for better organization  
- After creation, you can manage users/groups inside this specific domain  
- The Default domain can't be deleted — use additional ones for isolation

### What's Next?
- Create users and groups inside this domain  
- Assign IAM policies to allow access  
- Test login with a new user from this domain

Detailed screenshots, policy examples, and troubleshooting notes are inside this repository!

Happy OCI learning! ☁️🔐  
#OCI #OracleCloud #IdentityDomains #IAM #CloudSecurity
