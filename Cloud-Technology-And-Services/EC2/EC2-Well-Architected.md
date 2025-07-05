# Amazon EC2 & AWS Well-Architected Framework (6 Pillars)

This document aligns Amazon EC2 best practices to each of the six AWS Well-Architected Framework pillars.

---

## 1. Operational Excellence

**Objectives:** Improve processes, monitoring, and readiness for change.

* **Infrastructure as Code**
  • Define EC2 instances, Auto Scaling Groups, and Security Groups in CloudFormation or Terraform.
* **Automation & Deployment**
  • Use CodeDeploy or Systems Manager Automation to deploy and patch workloads.
* **Monitoring & Alerting**
  • Instrument EC2 metrics (CPU, memory via CloudWatch Agent) and set alarms.
  • Capture EC2 API activity with CloudTrail for operational auditing.
* **Runbook & Playbooks**
  • Document instance recovery steps; automate common operations via SSM run commands.

---

## 2. Security

**Objectives:** Protect data and systems, manage identity, and enforce least privilege.

* **Identity & Access Management**
  • Assign IAM Roles with least-privilege policies to EC2 (Instance Profiles).
  • Enforce IMDSv2 for metadata service access.
* **Network Security**
  • Place instances in private subnets with NAT for egress.
  • Use Security Groups and Network ACLs to restrict inbound/outbound traffic.
* **Encryption**
  • Encrypt EBS volumes with SSE-KMS.
  • Use encrypted AMIs and ensure root volumes are encrypted.
* **OS & Application Hardening**
  • Automate OS patching with AWS Systems Manager Patch Manager.
  • Disable unused ports and services.
* **Logging & Auditing**
  • Enable CloudTrail, CloudWatch Logs, and VPC Flow Logs to monitor instance activity.

---

## 3. Reliability

**Objectives:** Ensure workload availability, fault tolerance, and recover quickly.

* **Auto Scaling & Health Checks**
  • Deploy EC2 instances in ASGs across multiple AZs; configure ELB health checks.
* **Backup & Recovery**
  • Schedule EBS snapshots with Data Lifecycle Manager; automate AMI creation.
  • Use EC2 Auto Recovery or CloudWatch alarms to replace impaired instances.
* **Fault Isolation**
  • Distribute instances across AZs and use Placement Groups for cluster workloads.
  • Tag and group resources by environment for targeted recovery.
* **DR Preparedness**
  • Replicate critical data (snapshots, AMIs) to another region.
  • Script and test recovery of EC2 instances in a secondary region.

---

## 4. Performance Efficiency

**Objectives:** Use resources efficiently at scale and adapt to changing requirements.

* **Instance Type Selection**
  • Choose the right family (Compute, Memory, Storage, Accelerated) based on workload profile.
  • Evaluate Graviton instances for cost-performance gains.
* **Scaling Strategies**
  • Implement predictive scaling in ASGs based on scheduled or forecasted demand.
* **Caching & Offloading**
  • Offload static content to CloudFront; use ElastiCache for in-memory caching.
* **Monitoring & Optimization**
  • Use CloudWatch metrics and Compute Optimizer recommendations to right-size instances.
  • Leverage AWS Application Auto Scaling for flexible resource management.

---

## 5. Cost Optimization

**Objectives:** Eliminate unnecessary costs and maximize efficiency.

* **Pricing Models Mix**
  • Use On-Demand for flexibility, Reserved Instances or Savings Plans for steady-state, Spot for fault-tolerant workloads.
* **Right-Sizing & Scheduling**
  • Use Compute Optimizer to identify underutilized instances; schedule stop/start for non-production.
* **Storage Cost Management**
  • Attach appropriate EBS volume types (gp3, st1) and delete unused volumes.
* **Monitor & Alert**

  • Track EC2 spend in Cost Explorer; set budget alerts.

---

## 6. Sustainability

**Objectives:** Minimize environmental impact.

* **Efficient Resource Utilization**
  • Right-size instances to avoid over-provisioning.
  • Consolidate workloads onto fewer, more efficient instance types.
* **Use Energy-Efficient Hardware**
  • Adopt AWS Graviton (Arm-based) instances for lower power consumption per workload.
* **Lifecycle Management**

  • Clean up idle or unattached resources (EBS volumes, unused AMIs).
  • Automate termination of obsolete instances.
* **Monitoring & Reporting**
  • Tag resources to map compute usage by application or team for carbon footprint analysis.
  • Use AWS Cost and Usage Reports to correlate usage with sustainability metrics.

---

**References:**

* AWS Well-Architected Framework: [https://aws.amazon.com/architecture/well-architected/](https://aws.amazon.com/architecture/well-architected/)
* EC2 Best Practices: [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/best-practices.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/best-practices.html)
