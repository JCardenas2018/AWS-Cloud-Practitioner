# Amazon EKS Cost Examples & Use Cases

Below are three concrete costing scenarios for Amazon EKS clusters, along with example use cases illustrating when each makes sense.

---

## Cost Example 1: Small Dev Cluster on EC2

| Component                          | Monthly Cost   |
|------------------------------------|---------------:|
| **Control Plane** (1 cluster × $0.10/hr × 730 hr) | $72.00 :contentReference[oaicite:0]{index=0} |
| **EC2 Worker Nodes** (2 × t3.medium)             | $100.00 :contentReference[oaicite:1]{index=1} |
| **EBS Storage** (100 GB gp2)                     | $10.00 :contentReference[oaicite:2]{index=2} |
| **Application Load Balancer** (1 ALB)            | $16.00 :contentReference[oaicite:3]{index=3} |
| **Total**                                        | **$198.00**    |

### Use Case: Development Environment  
A simple, predictable‐cost setup for dev or test workloads. You get full Kubernetes features on EC2 node groups while keeping monthly expenses under \$200.

---

## Cost Example 2: Fargate-Only Cluster for Production Microservices

- **Control Plane**: \$0.10/hr × 730 hr = **\$72.00**   
- **Fargate Compute**:  
  - Configuration: 3 Pods, each 2 vCPU + 4 GB RAM  
  - Hourly per-Pod cost: (2 × \$0.04048) + (4 × \$0.004445) = \$0.09874/hr :contentReference[oaicite:5]{index=5}  
  - Monthly (3 Pods × \$0.09874/hr × 730 hr) ≃ **\$216.30**  
- **Total ≃ \$288.30**

### Use Case: Serverless Production Services  
Ideal for microservices with unpredictable or spiky traffic. You pay per-second for compute, eliminate node management, and scale seamlessly.

---

## Cost Example 3: EC2 Spot Worker Nodes for Batch Processing

- **Control Plane**: \$72.00 (same as above)   
- **EC2 Spot Nodes**:  
  - Instance type equivalent to m5.large (On-Demand ≃ \$0.096/hr)  
  - Spot discount up to 90% → \$0.0096/hr per node :contentReference[oaicite:7]{index=7}  
  - Monthly per node: \$0.0096/hr × 730 hr ≃ \$7.00  
  - For 4 nodes: 4 × \$7.00 = **\$28.00**  
- **Total ≃ \$100.00**

### Use Case: Batch & Data Processing  
Perfect for interruption-tolerant ETL jobs or ML training. Spot Instances can slash node costs by up to 90%, keeping your EKS cluster expenses around \$100/month.

---
