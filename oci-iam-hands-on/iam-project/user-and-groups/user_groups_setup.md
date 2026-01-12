# OCI Hands-On: Creating a User and Group in an Identity Domain

This guide covers creating a **User** and a **Group** inside your OCI Identity Domain — essential steps for managing authentication and scalable permissions.

Users represent individual people (or apps) who access OCI. Groups let you assign the same permissions to multiple users efficiently (principle of least privilege).

### Why Create Users & Groups?
- Users enable secure individual logins (email-based)
- Groups make permission management easy & scalable
- Groups tie directly to IAM policies for resource access
- Perfect for isolating dev/test users from production

### Prerequisites
- OCI Free Tier account
- An active **Identity Domain** (e.g., your `Development-Domain`)
- Admin access to the domain (Identity Domain Administrator role)

### Step-by-Step Guide

#### Part 1: Create a New User

1. **Navigate to Your Domain**  
   - Open OCI Console → **Identity & Security** → **Domains**  
   - Select your domain (e.g., `Development-Domain`)

2. **Go to Users**  
   - On the domain details page, under **Identity domain** (left menu) → click **Users**  
   - Or select **User management** tab → **Users** section

3. **Create the User**  
   - Click **Create user** (or **Create**)  
   - Fill in:  
     - **First name** & **Last name** (e.g., Dev, User)  
     - **Username/Email**: Use a real email you control (this is the login ID)  
     - Optional: Enable MFA, add description  
   - (You can select groups here or add later)  
   - Click **Create**

4. **Activation**  
   - OCI sends a verification email to the user  
   - User must click the link and set a password (or reset if needed)

#### Part 2: Create a Group & Add the User

1. **Go to Groups**  
   - In the same domain → left menu → **Groups**  
   - Or **User management** tab → **Groups** section

2. **Create the Group**  
   - Click **Create group**  
   - **Name**: e.g., `Dev-Admins` (unique, letters/numbers/hyphens)  
   - **Description**: e.g., `Group for development environment administrators`  
   - Click **Create**

3. **Add User to the Group** (two ways)  
   - **Option A** (from Group):  
     - Open the new group → **Users** or **Add user**  
     - Search & select your user → **Add**  
   - **Option B** (from User):  
     - Open the user → **Groups** tab → **Add to groups**  
     - Select your group → **Add**

### Tips & Best Practices
- Always use real emails for users (for password reset & MFA)  
- Create groups first if you plan multiple users  
- Enable **MFA** on users/groups for better security  
- Groups inherit no permissions automatically — assign via IAM Policies next  
- You can add users to multiple groups

### What's Next?
- Assign IAM Policies to this group (to allow resource management in your compartment)  
- Test login with the new user's email  
- Explore roles, MFA policies, or federation

Detailed console screenshots, sample naming conventions, and troubleshooting notes are inside this repository!

Happy OCI learning! ☁️🔐  
#OCI #OracleCloud #IdentityDomains #Users #Groups #IAM
