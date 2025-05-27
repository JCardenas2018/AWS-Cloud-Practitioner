# 🏢 AWS Availability Zones (AZs)

## 📌 What is an Availability Zone?

An **Availability Zone (AZ)** is one or more **physically separated data centers** within an AWS Region. Each AZ has **independent power, cooling, and networking**, but is connected to other AZs in the same region with **low-latency, high-throughput, and redundant networking**.

> **Purpose**: Improve application **availability**, **fault tolerance**, and **disaster recovery** within a region.

---

## 🌍 Structure Overview

- **Region**: A geographical area (e.g., `us-east-1`)
- **Availability Zone**: A fault-isolated location within the region (e.g., `us-east-1a`)
- Each AWS Region contains **at least two AZs** (most have three or more)

---

## 🧠 Key Characteristics

| Feature                    | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| **Physically isolated**     | Each AZ is located in a separate data center facility                      |
| **Highly available**        | Designed to withstand failures independently from other AZs                |
| **Low-latency connectivity**| Connected to other AZs with high-speed private fiber links                 |
| **Used for high availability** | Distribute workloads across AZs to prevent single points of failure       |
| **Supports key AWS services** | EC2, RDS, ELB, S3 replication, Auto Scaling, etc.                         |

---

## ⚙️ Example Use Cases

- Deploying **EC2 instances across multiple AZs** for fault tolerance
- Running **RDS with Multi-AZ deployments** for database availability
- Creating **Auto Scaling groups** that span multiple AZs
- Hosting microservices behind **Elastic Load Balancers (ELBs)** in several AZs

---

## 🧱 Availability Zone vs Region vs Edge Location

| Component               | Description                                              | Example          |
|-------------------------|----------------------------------------------------------|------------------|
| **Region**              | A geographical area with multiple AZs                    | `us-west-2`      |
| **Availability Zone**   | A fault-isolated data center inside a region             | `us-west-2a`     |
| **Edge Location**       | CDN endpoint for caching and content delivery (CloudFront) | Tokyo Edge PoP   |

---

## ✅ Summary

> An **Availability Zone (AZ)** is a **physically separate location** within an AWS Region that helps you **build highly available and fault-tolerant applications**. By deploying resources across multiple AZs, you can ensure better **resilience** and **business continuity**.

---

## 📚 Useful Resources

- [AWS Global Infrastructure Overview](https://aws.amazon.com/about-aws/global-infrastructure/)
- [Regions and Availability Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)
- [Well-Architected Framework - Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/wellarchitected-reliability-pillar.pdf)
