## Shared Responsibility Model for Amazon S3

### Core Responsibilities

| AWS Responsibility                                                | Customer Responsibility                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------|
| - Physical infrastructure (data centers, hardware)                | - Data classification and encryption                                             |
| - Network availability and resilience                             | - Bucket policies and Access Control Lists (ACLs)                                 |
| - Host and network protection (hypervisor, underlying OS)         | - IAM user and role management                                                    |
| - Storage service software patching and maintenance               | - Versioning, lifecycle rules and object lock configurations                      |
| - Encryption of data at rest when using AWS-managed keys (SSE-S3) | - Client-side or KMS-managed encryption, key rotation and access control policies |

### Additional Feature Scenarios

| Feature / Scenario               | AWS Responsibility                                               | Customer Responsibility                                                                                        |
|----------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| **Server Access Logging**        | • Provide log capture and delivery infrastructure                | • Enable logging on the bucket<br>• Choose and secure target bucket<br>• Configure log retention policies      |
| **Cross-Region Replication**     | • Maintain the replication engine and network connectivity       | • Define replication rules and filters<br>• Create and grant IAM replication role<br>• Monitor replication status |
| **SSL/TLS Encryption in Transit**| • Support HTTPS endpoints and TLS certificate rotation           | • Always use HTTPS when interacting with S3<br>• Validate server certificates in your client                   |
| **MFA-Delete**                   | • Enforce MFA-Delete checks on the service side                  | • Enable MFA-Delete on the bucket<br>• Manage and secure MFA devices                                          |
| **Object Lock & WORM**           | • Provide immutable storage engine and retention enforcement     | • Configure retention periods (Governance or Compliance mode)<br>• Apply legal holds if needed                |
