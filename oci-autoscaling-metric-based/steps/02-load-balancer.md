# Step 2: Load Balancer

Now that the network's ready, let's add a load balancer (LB) to distribute traffic across your future instances. In Free Tier, it's flexible and limited to 10 Mbps – perfect for testing.

## Why?
- Evenly spreads requests, essential for scaled instances.

## Steps in OCI Console
1. Networking > Load Balancers > Create Load Balancer.
2. Type: Flexible.
3. Name: "autoscaling-lb".
4. Visibility: Public (for external access).
5. Shape: 10 Mbps.
6. Assign to your VCN and public subnet.
7. Backend Set: Create one (HTTP/80 for now – we'll add backends later).
8. Listener: HTTP on port 80.
9. Health Check: Basic (e.g., HTTP / with 200 OK).

## Tips & Gotchas
- No backends yet? That's fine – we'll add the instance pool later.
- Free Tier: 10 Mbps is free forever.
- Test: Once set up, note the LB's public IP for later.

Next: [Step 3: Compute Instance](../steps/03-compute-instance.md).
