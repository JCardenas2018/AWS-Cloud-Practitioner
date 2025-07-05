## EC2 Instance Types & Families (Brief)

- **General Purpose**  
  • Balanced CPU, memory, network  
  • **Example:** `t3.micro` – 2 vCPU, 1 GiB RAM (small web servers, dev/test)

- **Compute Optimized**  
  • High CPU-to-memory ratio  
  • **Example:** `c5.large` – 2 vCPU, 4 GiB RAM (batch processing, HPC)

- **Memory Optimized**  
  • High memory-to-CPU ratio  
  • **Example:** `r5.large` – 2 vCPU, 16 GiB RAM (in-memory caches, analytics)

- **Storage Optimized**  
  • Local NVMe SSD or HDD storage  
  • **Example:** `i3.large` – 2 vCPU, 15 GiB RAM + NVMe SSD (NoSQL databases)

- **Accelerated Computing**  
  • GPUs or custom chips for parallel workloads  
  • **Example:** `g4dn.xlarge` – 4 vCPU, 16 GiB RAM + NVIDIA T4 GPU (ML inference)

- **Burstable Performance**  
  • Earn and spend CPU credits for intermittent peaks  
  • **Example:** `t4g.small` – 2 vCPU, 2 GiB RAM (microservices, low-traffic apps)
