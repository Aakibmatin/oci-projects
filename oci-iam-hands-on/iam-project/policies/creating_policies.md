# OCI Hands-On: Writing & Creating IAM Policies

This guide shows how to **create IAM Policies** in Oracle Cloud Infrastructure (OCI) — the key step to grant **authorization** to your users/groups in a compartment.

IAM Policies define "who can do what" on resources (e.g., allow Dev-Admins group to manage instances in Development-Compartment). Follow **least privilege**: give only necessary permissions.

### Why Create IAM Policies?
- Controls access to compartments/resources
- Links groups/users to actions (manage, read, use)
- Enforces security (no one has root access by default)
- Essential for testing your user/group setup

### Prerequisites
- OCI Free Tier account
- Existing **Compartment** (e.g., `Development-Compartment`)
- Active **Identity Domain**, **User**, and **Group** (e.g., `Dev-Admins`)

### Step-by-Step Guide to Create Policies

1. **Log in to OCI Console**  
   Go to [https://cloud.oracle.com](https://cloud.oracle.com) as admin.

2. **Navigate to Policies**  
   - Navigation menu (☰) → **Identity & Security**  
   - Under **Identity**, click **Policies**  
   - Select the **parent compartment** (e.g., root or your Development-Compartment)

3. **Create a New Policy**  
   - Click **Create policy** button  
   - **Policy name**: e.g., `Dev-Admins-Policy` (unique in compartment)  
   - **Description**: e.g., `Permissions for Dev-Admins group in Development-Compartment`

4. **Add Policy Statements**  
   - In the **Policy builder** tab (recommended for beginners):  
     - Click **Add statement**  
     - **Allow** selected by default  
     - **Group**: Select your domain/group (e.g., `Development-Domain/Dev-Admins`)  
     - **Target compartment**: `Development-Compartment`  
     - **Verbs**: Choose actions like `manage instance-family`, `manage volume-family`  
     - Click **Add** → Preview shows the statement  
   - Or **Manual editor** tab: Paste statements (samples in `policies/` folder)  
     Example:

     
5. **Review & Create**  
- Check **Policy preview** for errors  
- Click **Create**  
- Policy status: **Active** (refresh if needed)

6. **Verify** (Quick Test)  
- Log in as your new user (email from domain)  
- Switch to `Development-Compartment`  
- Try creating a Compute Instance → Success = policy works!

### Tips & Best Practices
- Use **Policy builder** for no typos (auto-generates syntax)  
- Common verbs: `inspect` (read), `read`, `use`, `manage` (full CRUD)  
- Families: `instance-family` (VMs), `volume-family` (storage), `object-family` (buckets)  
- Scope to **exact compartment** — avoids inheritance issues  
- Test with minimal permissions first
