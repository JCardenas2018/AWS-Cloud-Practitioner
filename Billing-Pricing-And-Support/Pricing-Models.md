# AWS Pricing Models

AWS offers several pricing models to match different workload requirements, budget targets, and flexibility needs:

---

## 1. On-Demand

- **What it is**  
  Pay-per-use pricing with no long-term commitments.  
- **Billing unit**  
  Charged per second (Linux) or per hour (Windows) based on instance size, OS, and region.  
- **Use case**  
  Short-lived, unpredictable workloads; development and testing environments.

---

## 2. Reserved Instances (RIs)

- **What it is**  
  Commit to a 1- or 3-year term for significant discounts.  
- **Types**  
  - **Standard RIs** (up to ~72% off On-Demand)  
  - **Convertible RIs** (up to ~66% off; exchangeable instance families)  
- **Payment options**  
  All Upfront, Partial Upfront, No Upfront.  
- **Use case**  
  Steady-state, predictable workloads (e.g., production web tiers).

---

## 3. Savings Plans

- **What it is**  
  Flexible commitments based on spend rather than specific instance attributes.  
- **Types**  
  - **Compute Savings Plans** (apply to EC2, Fargate, Lambda; up to ~66% off)  
  - **EC2 Instance Savings Plans** (tied to a instance family in a region; up to ~72% off)  
- **Use case**  
  When you need flexibility to switch instance types or services but still want deep discounts.

---

## 4. Spot Instances

- **What it is**  
  Bid on spare EC2 capacity at steep discounts (up to ~90% off).  
- **Caveat**  
  Instances can be terminated with 2 minutes’ notice when capacity is reclaimed.  
- **Use case**  
  Fault-tolerant, stateless, or batch workloads that can handle interruptions (e.g., big data processing).

---

## 5. On-Demand Capacity Reservations

- **What it is**  
  Reserve capacity in a specific Availability Zone without a long-term commitment.  
- **Billing unit**  
  Charged at the On-Demand rate for the reserved capacity.  
- **Use case**  
  When you need guaranteed capacity during steady peaks (e.g., end-of-month reporting).

---

## 6. Dedicated Hosts & Instances

- **Dedicated Hosts**  
  Physical servers dedicated to you—helps meet compliance requirements (BYOL, licensing).  
- **Dedicated Instances**  
  Instances run on hardware dedicated to a single tenant, but with less host-level visibility.  
- **Use case**  
  Compliance or licensing constraints that require single-tenant hardware.

---

## 7. Free Tier & Spot Requests

- **Free Tier**  
  12 months of limited On-Demand usage for new accounts (750 hours/month of t2.micro/t3.micro).  
- **Spot Fleet & Spot Instances Requests**  
  Automate Spot allocation across multiple instance types and AZs for high availability.

---

### Choosing a Model

| Model                          | Flexibility      | Max Discount | Commitment         |
|--------------------------------|------------------|--------------|--------------------|
| **On-Demand**                  | Very high        | 0%           | None               |
| **Spot Instances**             | High (interruptible) | ~90%     | None               |
| **Savings Plans (Compute)**    | Medium-High      | ~66%         | 1–3 years (dollar) |
| **Savings Plans (Instance)**   | Medium           | ~72%         | 1–3 years (family) |
| **Reserved Instances (Standard)** | Low (fixed family/region) | ~72% | 1–3 years      |
| **Reserved Instances (Convertible)** | Medium-flexible | ~66%   | 1–3 years      |
| **Capacity Reservations**      | High             | 0%           | None               |
| **Dedicated Hosts/Instances**  | Low (single-tenant) | Up to RI discount | Optional |

Use On-Demand for flexibility, RIs/Savings Plans for predictable savings, Spot for cost-sensitive batch jobs, and Dedicated options for compliance—mix and match to optimize cost and performance.  
