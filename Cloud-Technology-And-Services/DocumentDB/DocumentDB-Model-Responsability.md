## Shared Responsibility Model Examples for Amazon DocumentDB

| **Scenario**              | **AWS Responsibility**                                                                 | **Customer Responsibility**                                                         |
|---------------------------|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Cluster Provisioning**  | • Manage control plane and cluster lifecycle<br>• Handle AZ placement and networking   | • Define VPC, subnets and security groups<br>• Configure parameter groups and options |
| **Engine Patching**       | • Apply engine and OS patches automatically during maintenance windows                 | • Test new engine versions in staging<br>• Schedule maintenance windows to minimize impact |
| **Backups & Recovery**    | • Continuous, incremental backups to S3<br>• Point-in-time restore capability         | • Configure backup retention policies<br>• Periodically perform restore drills      |
| **High Availability**     | • Replicate data six ways across three AZs<br>• Automated failover within ~30 seconds  | • Use drivers/connection strings that support failover retry logic                  |
| **Storage Scaling**       | • Automatically scale storage up to 64 TB as data grows                               | • Monitor performance metrics<br>• Choose appropriate instance class and read-replica count |
| **Encryption**            | • Encrypt data at rest with AWS-managed KMS keys<br>• Enforce TLS for in-transit data | • Define and rotate customer-managed keys (CMKs)<br>• Configure client drivers to require TLS |
| **Monitoring & Logging**  | • Expose CloudWatch metrics (CPU, memory, connections)<br>• Emit slow-log to CloudWatch Logs | • Enable slow-query logging<br>• Create CloudWatch alarms and dashboards for key metrics |
