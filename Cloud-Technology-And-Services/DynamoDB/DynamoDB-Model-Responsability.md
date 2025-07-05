## Shared Responsibility Model Examples for Amazon DynamoDB

| **Scenario**                        | **AWS Responsibility**                                                       | **Customer Responsibility**                                                                                     |
| ----------------------------------- | ---------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Table Management**                | • Provision underlying hardware and partitions<br>• Automated scaling engine | • Define table schemas (primary key, GSIs/LSIs)<br>• Configure read/write capacity mode and throughput          |
| **Security & Access Control**       | • Provide KMS-managed encryption at rest<br>• Secure service endpoints       | • Assign IAM policies for table access<br>• Manage user/role permissions and fine-grained attribute permissions |
| **Data Encryption in Transit**      | • Support TLS endpoints                                                      | • Configure clients to enforce TLS<br>• Validate certificates                                                   |
| **Backups & Restore**               | • Continuous backups with PITR<br>• On-demand snapshot orchestration         | • Define backup retention policies<br>• Test restore procedures                                                 |
| **Monitoring & Metrics**            | • Emit CloudWatch metrics and DynamoDB Streams events                        | • Create CloudWatch alarms and dashboards<br>• Consume Streams for custom logging or triggers                   |
| **Software Updates & Patching**     | • Maintain and patch service infrastructure and DynamoDB engine versions     | • Update client SDKs<br>• Manage application compatibility with engine versions                                 |
| **High Availability & Replication** | • Replicate data across AZs for durability and failover                      | • Design applications for eventual consistency<br>• Handle retries and error handling                           |
| **Serialization & Transactions**    | • Provide ACID transaction engine                                            | • Use transactional APIs correctly<br>• Manage transaction conflicts and retries                                |
