# Step 1: Network Setup (VCN + Public Subnet)

Hey! First things first – we need a network foundation. In OCI, this means creating a Virtual Cloud Network (VCN) and a public subnet. It's like setting up your home WiFi before connecting devices.

## Why?
- VCN: Your isolated cloud network.
- Public Subnet: Allows internet access for your instances and load balancer.

## Steps in OCI Console
1. Log in to OCI Console > Networking > Virtual Cloud Networks.
2. Click "Create VCN".
   - Name: Something like "autoscaling-vcn".
   - CIDR Block: Use default (10.0.0.0/16) or your own.
   - Create!
3. In the VCN details, go to Subnets > Create Subnet.
   - Name: "public-subnet".
   - Type: Public.
   - CIDR: 10.0.0.0/24 (or subset of VCN CIDR).
   - Route Table: Default (should have internet gateway – if not, add one).
   - Security List: Default (open ports as needed, e.g., 22 for SSH, 80/443 for HTTP).
4. In the VCN details, go to Subnets > Create Subnet.
   - Name: "private-subnet".
   - Type: Private.
   - CIDR: 10.0.1.0/24 (or subset of VCN CIDR).
   - Route Table: Default (should have internet gateway – if not, add one).
   - Security List: Default (open ports as needed, e.g., 22 for SSH, 80/443 for HTTP).

## Tips & Gotchas
- Ensure the subnet has enough IP space for scaling (e.g., /24 gives ~250 IPs).
- Free Tier: No cost for VCN/subnets.

Done? Move to [Step 2: Load Balancer](../steps/02-load-balancer.md).
