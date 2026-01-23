# OCI Free Tier Metric-Based Autoscaling Demo

Welcome! This repository is a dedicated guide to setting up **metric-based autoscaling** in Oracle Cloud Infrastructure (OCI) using only the Free Tier. No credit card or paid features needed – perfect for learning cloud scaling hands-on.

I built this based on my real experiment: creating a VCN, load balancer, compute instance, instance pool, autoscaling rules (scale-out and scale-in based on CPU), and testing it with CPU stress.

## Why This Repo?
- **Step-by-Step Breakdown**: Each major step has its own detailed Markdown file in the `steps/` folder.
- **Real-Life Approach**: Conversational explanations, tips, and gotchas from actual tinkering.
- **Free Tier Focus**: Everything stays within OCI Free Tier limits (e.g., max 3 instances).
- **Visuals**: Add screenshots to `images/` for clarity (I'll suggest where).

## Prerequisites
- An OCI Free Tier account (sign up at [oracle.com/cloud/free](https://www.oracle.com/cloud/free/)).
- Basic familiarity with OCI Console (web UI).
- SSH access setup for instances (generate keys in OCI).

## Quick Overview
1. **Network Setup**: VCN + public subnet.
2. **Load Balancer**: Distribute traffic.
3. **Compute Instance**: Base VM + custom image.
4. **Instance Pool**: Group of scalable VMs.
5. **Autoscaling Config**: CPU-based rules for scaling out/in.
6. **Testing**: Use stress-ng to simulate load and watch it scale.

## Full Step-by-Step Guides
Follow these in order:
- [Step 1: Network Setup](steps/01-network-setup.md)
- [Step 2: Load Balancer](steps/02-load-balancer.md)
- [Step 3: Compute Instance & Custom Image](steps/03-compute-instance.md)
- [Step 4: Instance Pool](steps/04-instance-pool.md)
- [Step 5: Autoscaling Configuration](steps/05-autoscaling-config.md)
- [Step 6: Testing with stress-ng](steps/06-testing.md)

## Key Learnings
- Autoscaling makes your setup resilient to load spikes without manual work.
- Always test scale-in to avoid overusing resources.
- Free Tier is generous – but watch limits like instance counts and bandwidth.

## Related
- Inspired by my LinkedIn post: [Link to your post here].
- Questions? Open an issue or PR!

#OCI #OracleCloud #Autoscaling #CloudComputing #DevOps #FreeTier

Licensed under MIT – feel free to fork and experiment!
