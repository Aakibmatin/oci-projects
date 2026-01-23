# Step 6: Testing with stress-ng

Simulate load to trigger scaling!

## Why?
- Verify it works end-to-end.

## Steps
1. SSH into a pool instance.
2. Install stress-ng: `sudo dnf install stress-ng -y`.
3. Stress CPU: `stress-ng --cpu 0 --cpu-load 90 --timeout 10m`.
4. Monitor in OCI: Compute > Instance Pools > Metrics. Watch instances add on spike, remove on drop.
5. Stop: Ctrl+C or `pkill stress-ng`.

## Tips & Gotchas
- Check Monitoring tab for CPU graphs.
- Scale-in might take a few mins.

Congrats – you've got autoscaling! Back to [README](../../README.md).
