## Cost & Use Cases

### Cost Overview (US East – N. Virginia)

| Component                    | Pricing                                                           |
|------------------------------|-------------------------------------------------------------------|
| **On-Demand Reads**          | \$1.25 per million read request units                             |
| **On-Demand Writes**         | \$1.25 per million write request units                            |
| **Provisioned Read Units**   | \$0.00013 per RCU-hour                                            |
| **Provisioned Write Units**  | \$0.00065 per WCU-hour                                            |
| **Storage**                  | \$0.25 per GB-month                                               |
| **DynamoDB Accelerator (DAX)** | From \$0.136 per node-hour                                     |
| **Streams**                  | \$0.02 per GB of data read                                        |
| **On-Demand Backups**        | \$0.10 per GB-month                                               |
| **Point-in-Time Recovery**   | \$0.20 per GB-month for change logs                               |
| **Global Tables**            | Replication: \$0.25 per GB replicated                             |

> **Example Monthly Costs** (approximate):
> - **Small App Table** (5 GB, 1 M reads, 0.5 M writes per month)
>   - Storage: 5 GB × \$0.25 = \$1.25  
>   - On-Demand Reads: 1 M × \$1.25/1 M = \$1.25  
>   - On-Demand Writes: 0.5 M × \$1.25/1 M = \$0.63  
>   - **Total:** ~\$3.13/month
>
> - **Provisioned Mode** (100 RCU, 50 WCU, 10 GB data)
>   - RCU: 100 × 730 hr × \$0.00013 = \$9.49  
>   - WCU: 50 × 730 hr × \$0.00065 = \$23.73  
>   - Storage: 10 GB × \$0.25 = \$2.50  
>   - **Total:** ~\$35.72/month

### Common Use Cases

- **Gaming**  
  Player profiles and leaderboards requiring <10 ms latency (e.g., 50 K active users generating 5 M reads and 1 M writes daily).

- **IoT & Telemetry**  
  Time-series ingestion at variable rates; On-Demand mode for traffic spikes (e.g., 1 M device updates/day, ~30 GB storage/month).

- **Mobile & Web Apps**  
  Shopping carts and session data with unpredictable traffic; ideal for On-Demand capacity.

- **Real-Time Analytics**  
  Clickstream counters and dashboard metrics; combine DynamoDB Streams with Lambda for processing.

- **Ad Tech & Bidding**  
  Microsecond-level writes for bidding metadata; use provisioned capacity with auto-scaling.

- **Microservices Configuration**  
  Feature flags and shared state; low throughput but high availability requirements.

### Cost Optimization Tips

- **Choose Capacity Mode Wisely:** On-Demand for spiky workloads; Provisioned with Auto Scaling for predictable traffic.

- **Implement TTL:** Automatically expire items to free up storage.

- **Leverage DAX:** Cache frequent reads to reduce RCU consumption.

- **Right-Size Workloads:** Monitor CloudWatch metrics and adjust RCU/WCU or switch capacity modes.

- **Use Savings Plans:** Commit to sustained Provisioned usage for discounted rates.  
