# Basic Operations Example
## Starting State
- Fresh cluster: all nodes free (grey)
- No jobs running
- 0% utilization
## Submit 2-node job
- Watch it get placed within single leaf domain
- Observe:
  - 2 cells turn blue
  - Active Jobs: 1
  - GPU Utilization: ~1.5%

# Topology-Aware Placement
## Starting State
- Fresh cluster: all nodes free (grey)
- No jobs running
- 0% utilization
## Submit 2-node job
- Watch it get placed within single leaf domain
- Observe:
  - 2 cells turn blue
  - Active Jobs: 1
  - GPU Utilization: ~1.5%

# Performance Monitoring
## High Load Test
Settings:
- Job Arrival: 0.8
- Sizes: [8, 16]
- Update: 0.5s
- Observe:
- Queue length increasing
- Utilization spikes
- Success rate dropping

# Resource Fragmentation
## Mixed Workload
Settings:
- Enable all job sizes
- Medium arrival rate (0.4)

Watch:
- Small jobs filling gaps
- Large jobs waiting for contiguous space
- Utilization pattern in heatmap
