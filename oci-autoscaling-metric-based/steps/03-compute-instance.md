# Step 3: Compute Instance & Custom Image

Time to create your base VM! We'll use Oracle Linux, customize it (e.g., install software), and make a custom image for consistency in the pool.

## Why?
- Custom image ensures all scaled instances are identical.

## Steps in OCI Console
1. Compute > Instances > Create Instance.
   - Name: "base-instance".
   - Image: Oracle Linux (latest).
   - Shape: VM.Standard.E2.1.Micro (Free Tier eligible).
   - VCN/Subnets: Your private subnet.
   - SSH: Upload your public key.
   - Boot Volume: Default.
2. Once running, SSH in: `ssh opc@<public-ip>`.
3. Customize: Install packages (e.g., a web server if needed).
4. Create Custom Image: Compute > Instances > Your instance > More Actions > Create Custom Image.
   - Name: "autoscaling-image".

## Tips & Gotchas
- Free Tier: Micro shape is always free (up to 2 instances).
- Install stress-ng here if testing locally.
- Wait for image creation (10-15 mins).

On to [Step 4: Instance Pool](../steps/04-instance-pool.md).
