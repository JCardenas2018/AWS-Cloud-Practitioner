# AWS Compute Pricing

AWS offers several pricing models for compute services. Here’s a quick overview:

---

## 1. On-Demand Instances  
- **Description**: Pay-per-use with no long-term commitment.  
- **Billing**: Charged per second or per hour, depending on instance family, OS, and region.  
- **Example**: Base vCPU-hour rate for Linux, RHEL, and SLES On-Demand instances in the T-Series Unlimited family is $0.04 per vCPU-hour; for Windows it’s $0.096 per vCPU-hour.

---

## 2. Reserved Instances (RI)  
- **Description**: Commit to a 1- or 3-year term in exchange for a significant discount.  
- **Savings**: Up to 72% off On-Demand prices.  
- **Types**:  
  - **Standard RI**: Highest discount; you can change AZ, instance size, and tenancy.  
  - **Convertible RI**: Up to 66% discount; you can change instance family, OS, or tenancy during the term.  
- **Payment Options**:  
  - **All Upfront**  
  - **Partial Upfront**  
  - **No Upfront**  

---

## 3. Savings Plans  
- **Compute Savings Plans**  
  - Up to 66% discount across EC2, Fargate, and Lambda.  
  - Automatically applies when you switch instance family, OS, region, or compute service.  
- **EC2 Instance Savings Plans**  
  - Up to 72% discount.  
  - Commitment to a specific instance family within a region.

---

## 4. Spot Instances  
- **Description**: Use spare EC2 capacity at deep discounts.  
- **Savings**: Up to 90% off On-Demand rates.  
- **Caveat**: Instances can be interrupted with a 2-minute notice.

---

## 5. On-Demand Capacity Reservations  
- **Description**: Reserve capacity in a specific AZ without long-term commitment.  
- **Billing**: Pay the On-Demand rate for the reserved capacity.

---

## Quick Comparison

| Pricing Model                        | Flexibility               | Max Discount | Commitment         |
|--------------------------------------|---------------------------|--------------|--------------------|
| **On-Demand**                        | Very high                 | 0%           | None               |
| **Spot**                             | High (interruptible)      | Up to 90%    | None               |
| **Savings Plans (Compute)**          | Medium – high             | Up to 66%    | 1–3 years (usage)  |
| **Savings Plans (Instance)**         | Medium                    | Up to 72%    | 1–3 years (family) |
| **Reserved Instances (Standard)**    | Low (family/region fixed) | Up to 72%    | 1–3 years          |
| **Reserved Instances (Convertible)** | Medium-flexible           | Up to 66%    | 1–3 years          |
| **Capacity Reservations**            | High (capacity guaranteed)| 0%           | None               |

Use these options to tailor your AWS compute spending strategy based on your needs for flexibility, savings, and risk tolerance.  
