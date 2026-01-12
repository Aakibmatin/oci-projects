# OCI Hands-On: Creating a Compartment

This guide shows you how to create a **compartment** in Oracle Cloud Infrastructure (OCI) — one of the most important first steps when starting with OCI.

Compartments help you **organize**, **isolate**, and **secure** your cloud resources (like VMs, storage, databases, etc.). They are like secure folders in your OCI tenancy.

### Why Create Compartments?
- Isolate environments (dev, test, prod)
- Control access with IAM policies
- Separate billing and resource usage
- Follow security best practices (least privilege)

### Prerequisites
- An OCI account (Free Tier works perfectly)
- Access to the OCI Console

### Step-by-Step Guide to Create a Compartment

1. **Log in to the OCI Console**  
   Go to [https://cloud.oracle.com](https://cloud.oracle.com) and sign in with your credentials.

2. **Navigate to Compartments**  
   - Open the **navigation menu** (hamburger icon ☰ in the top-left)  
   - Select **Identity & Security**  
   - Under **Identity**, click **Compartments**  
   You'll see the list of existing compartments (at least the root compartment).

3. **Start Creating the Compartment**  
   - Click the **Create Compartment** button (usually at the top of the page)  
   - If you want to create it inside an existing compartment (nested), first navigate to that compartment's details page, then click **Create Compartment**.

4. **Fill in the Details**  
   - **Name**: Enter a unique name (max 100 characters, letters, numbers, hyphens, underscores, periods). Example: `Development-Compartment`  
     → Must be unique within the parent compartment  
   - **Description**: Add a friendly description (optional but recommended)  
     Example: `Compartment for all development resources and experiments`  
   - **Parent Compartment**: It shows the current one by default. Change if needed.  
   - **Tags** (optional): Add freeform or defined tags for better organization.

5. **Create It!**  
   Click **Create Compartment**.  
   After a few seconds, refresh the page — your new compartment will appear in the list!

### Tips & Best Practices
- Start with simple names like `Dev`, `Test`, `Prod`, `Shared`, `Network`  
- Use nesting for hierarchy (up to 6 levels deep)  
- Never put production resources in the root compartment  
- After creation, go to **Identity & Security → Policies** to add IAM policies for access control

### What's Next?
- Create users, groups, and policies in this compartment  
- Launch your first Compute instance or storage bucket inside it  
- Explore moving resources between compartments (if needed)

Detailed screenshots, troubleshooting notes, and examples are inside this repository!

Happy OCI learning! ☁️  
#OCI #OracleCloud #Compartments #CloudBasics
