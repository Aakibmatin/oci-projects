# oci-projects
# OCI IAM Hands-On: Compartments, Domains, Users, Groups & Policies

## Overview
Learning project demonstrating **Oracle Cloud Infrastructure Identity and Access Management (IAM)** basics.

Implemented:
- Created **compartments** for resource isolation
- Set up an **identity domain**
- Created a **user** in the domain
- Formed a **group** and added the user
- Wrote **IAM policies** to grant controlled permissions to the group

Goal: Practice **least-privilege access**, secure multi-user setup, and compartment organization.

## Architecture Diagram
<!-- Paste PNG here or use mermaid -->
![IAM Setup Diagram](diagrams/oci-iam-setup.png)

## Step-by-Step Walkthrough
1. **Compartments** → Organized resources under root compartment  
2. **Identity Domain** → Created for centralized user/group management  
3. **User Creation** → Added new user to the domain  
4. **Group & Membership** → Created group, assigned user  
5. **Policies** → Example statements:
