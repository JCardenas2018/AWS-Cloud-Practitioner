# AWS Shared Responsibility Model

AWS and customers share security and compliance responsibilities. AWS manages the security **of** the cloud; customers manage security **in** the cloud.

| **Domain**                       | **AWS Responsibility**                                                   | **Customer Responsibility**                                              |
| -------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| **Physical Infrastructure**      | • Data center facilities<br>• Network hardware<br>• Physical security    | • N/A                                                                    |
| **Hypervisor & Virtualization**  | • Hypervisor patches<br>• Host OS hardening                              | • VM configuration<br>• Guest OS hardening                               |
| **Networking**                   | • Physical network<br>• Network segmentation<br>• Routing infrastructure | • VPC configuration<br>• Security groups & NACLs<br>• VPN/Direct Connect |
| **Infrastructure Security**      | • Host firewalls<br>• DDoS protection<br>• Monitoring & logging          | • Application firewalls (WAF)<br>• Security group rules                  |
| **Operating System & Runtime**   | • Patching of managed services OS and runtimes                           | • Patch and configure OS on EC2 or self-managed instances                |
| **Containers & Serverless**      | • Runtime isolation<br>• Control plane security                          | • Container image security<br>• Function code and dependencies           |
| **Data**                         | • Encryption capabilities (KMS, SSE)<br>• Key management infrastructure  | • Data classification & encryption<br>• Key usage policies               |
| **Identity & Access Management** | • IAM service availability<br>• AWS-managed roles                        | • IAM user, group, and role policies<br>• Principle of least privilege   |
| **Monitoring & Logging**         | • Capture AWS API calls (CloudTrail)<br>• Service metrics (CloudWatch)   | • Enable and analyze logs<br>• Integrate with SIEM                       |
| **Application Security**         | • Underlying platform security for managed services                      | • Secure application code<br>• Input validation and secrets management   |

---

**Key Takeaway:** AWS secures the foundational infrastructure; you secure your workloads, data, and configurations on AWS.
