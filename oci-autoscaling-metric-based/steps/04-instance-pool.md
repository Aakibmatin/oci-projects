# Step 4: Instance Configuration & Pool

Using your custom image, create an instance configuration and then the pool – this is the group that will scale.

## Why?
- Pool: Managed group of identical instances.

## Steps in OCI Console
1. Compute > Instance Configurations > Create Instance Configuration.
   - From your custom image.
   - Shape: Same as base (Micro).
   - Networking: Your VCN/public subnet.
2. Compute > Instance Pools > Create Instance Pool.
   - Name: "autoscaling-pool".
   - Use your instance config.
   - Initial Size: 1 (min for Free Tier).
   - Attach to Load Balancer: Select your LB's backend set.

## Tips & Gotchas
- Pool starts with 1 instance – we'll scale it dynamically next.
- Free Tier: Limit to 2-3 instances total.

Ready for scaling? [Step 5: Autoscaling Config](../steps/05-autoscaling-config.md).
