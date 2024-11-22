 # Dashboard Layout
- Top Section: Key metrics (Active Jobs, Queue Length, GPU Utilization, Success Rate)
- Middle: Cluster topology visualization
- Each cell = 1 node (4 GPUs)
- Grey cells = Free nodes
- Dark blue cells = Occupied nodes
- Columns represent leaf switch domains
- Bottom: Performance graphs
- Left: GPU utilization over time
- Right: Job queue and active jobs distribution
![Dashboard](images/image1)
![Metrics](images/image2)
  
## Using Simulation Controls (Sidebar)
- Job Arrival Rate: Controls frequency of new job submissions (0.0-1.0)
- Job Sizes: Select node requirements (2, 4, 8, 16)
- Update Interval: Adjust visualization refresh rate
## Basic Operations Example
### Starting State
- Fresh cluster: all nodes free (grey)
- No jobs running
- 0% utilization
### Submit 2-node job
- Watch it get placed within single leaf domain
- Observe:
  - 2 cells turn blue
  - Active Jobs: 1
  - GPU Utilization: ~1.5%

## Topology-Aware Placement
### Starting State
- Fresh cluster: all nodes free (grey)
- No jobs running
- 0% utilization
### Submit 2-node job
- Watch it get placed within single leaf domain
- Observe:
  - 2 cells turn blue
  - Active Jobs: 1
  - GPU Utilization: ~1.5%

## Performance Monitoring
### High Load Test
Settings:
- Job Arrival: 0.8
- Sizes: [8, 16]
- Update: 0.5s
- Observe:
- Queue length increasing
- Utilization spikes
- Success rate dropping

## Resource Fragmentation
### Mixed Workload
Settings:
- Enable all job sizes
- Medium arrival rate (0.4)

Watch:
- Small jobs filling gaps
- Large jobs waiting for contiguous space
- Utilization pattern in heatmap
