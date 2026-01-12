# Hands-On OCI IAM: Building a Secure Development Environment from Scratch

This repository contains a complete step-by-step guide and resources for learning **Oracle Cloud Infrastructure (OCI) Identity and Access Management (IAM)** through practical, hands-on exercises.

If you're new to OCI, the **best way to learn** is by doing — especially starting with IAM.  
This project helps you understand the core concepts of **authentication** (who you are) and **authorization** (what you can do) by creating a secure, isolated development environment.

### How to Navigate This Repository (Recommended Learning Path)

Follow these folders/files in order — each builds on the previous one:

1. **Create a Compartment**  
   → Start here: Organize and isolate your resources  
   Folder: `compartment/`  
   File: `README.md` (step-by-step guide + screenshots)

2. **Create an Identity Domain**  
   → Next: Set up a dedicated space for users & groups  
   Folder: `identity-domain/`  
   File: `README.md`

3. **Create User and Group**  
   → Then: Add a real user and organize them into a group  
   Folder: `user-group/`  
   File: `README.md`

4. **Write & Apply IAM Policies**  
   → Finally: Grant controlled permissions to your group  
   Folder: `policies/`  
   Key files:  
   - `policies_statements.md` → All ready-to-copy policy examples  
   - `README.md` → Step-by-step creation guide

After completing these four steps, you can test the full flow:  
Log in as your new user → Switch to the compartment → Create resources (e.g., Compute Instance) → Verify everything works securely!

All folders contain detailed **README.md** files + **screenshots/** subfolders for visual walkthroughs.

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

---

→ Dive into the folders above to get hands-on!  
Happy learning! ☁️🔐
