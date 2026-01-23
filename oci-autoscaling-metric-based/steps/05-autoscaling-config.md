# Step 5: Autoscaling Configuration

The core! Set rules to scale based on CPU metrics.

## Why?
- Auto-add/remove instances on demand.

## Steps in OCI Console
1. In your Instance Pool details > Autoscaling Configurations > Create.
2. Policy Type: Metric-Based.
3. Metric: CPU Utilization.
4. Rules:
   - Scale-Out: Threshold >70%, Duration 300s, Add 1 instance.
   - Scale-In: Threshold <30%, Duration 300s, Remove 1 instance.
5. Limits: Min 1, Max 3.
6. Cooldown: 300 seconds.

## Tips & Gotchas
- Pool-wide average CPU – not per-instance.
- Test thresholds in your setup.

Finally, [Step 6: Testing](../steps/06-testing.md).
