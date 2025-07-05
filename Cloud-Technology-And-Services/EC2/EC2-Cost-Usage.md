## EC2 Cost & Usage Overview

Amazon EC2 pricing varies by instance type, region, operating system, and pricing model. Below is an overview of common cost factors and usage scenarios.

### 1. Pricing Models

| Model              | Description                                                            | Use Case                                      |
| ------------------ | ---------------------------------------------------------------------- | --------------------------------------------- |
| **On-Demand**      | Pay per second (Linux) / per hour (Windows) without commitment.        | Development, testing, unpredictable workloads |
| **Reserved**       | 1- or 3-year commitment for up to 72% discount (Standard/Convertible). | Steady state, predictable workloads           |
| **Savings Plans**  | Flexible hourly commitment for compute usage across instance families. | Cost optimization with flexibility            |
| **Spot Instances** | Up to 90% discount on spare capacity; instances can be reclaimed.      | Fault-tolerant, batch jobs, data analysis     |

### 2. Hourly Rate Examples (US East – Linux)

| Instance Type              | On-Demand (per hour) | 1‑Year Reserved (All Upfront) | Spot (average) |
| -------------------------- | -------------------- | ----------------------------- | -------------- |
| t3.micro (2 vCPU,1 GiB)    | \$0.0104/hr          | \$0.006/hr                    | \$0.003/hr     |
| m5.large (2 vCPU,8 GiB)    | \$0.096/hr           | \$0.058/hr                    | \$0.023/hr     |
| c5.xlarge (4 vCPU,8 GiB)   | \$0.17/hr            | \$0.10/hr                     | \$0.04/hr      |
| r5.2xlarge (8 vCPU,64 GiB) | \$0.504/hr           | \$0.30/hr                     | \$0.12/hr      |

### 3. Typical Usage & Monthly Cost

| Scenario                           | Instance   | Hours/Month | On-Demand Cost | Reserved Cost | Spot Cost |
| ---------------------------------- | ---------- | ----------- | -------------- | ------------- | --------- |
| Small web server (24×7)            | t3.micro   | 730         | \~\$7.60       | \~\$4.38      | \~\$2.19  |
| Application server (24×7)          | m5.large   | 730         | \~\$70.21      | \~\$42.34     | \~\$16.79 |
| Batch compute job (100 hours)      | c5.xlarge  | 100         | \~\$17.00      | \~\$10.00     | \~\$4.00  |
| Analytics cluster node (200 hours) | r5.2xlarge | 200         | \~\$100.80     | \~\$60.00     | \~\$24.00 |

### 4. Cost Optimization Tips

* **Use Spot for Fault-Tolerant Workloads:** Leverage Spot Instances for batch processing, CI/CD, and big data jobs.
* **Mix Reserved & On-Demand:** Reserve capacity for baseline usage and use On-Demand or Spot for spikes.
* **Right-Size Instances:** Monitor CPU, memory, and network metrics to downsize underutilized instances.
* **Auto Scaling:** Automatically scale in/out to match demand and avoid idle capacity.
* **Use Savings Plans:** For maximum flexibility across families and regions.
* **Turn Off Idle Instances:** Schedule start/stop for non-production environments.

> **Note:** Prices are indicative for US East (N. Virginia) region and Linux OS as of July 2025. Consult the [EC2 Pricing page](https://aws.amazon.com/ec2/pricing/) for current rates.
