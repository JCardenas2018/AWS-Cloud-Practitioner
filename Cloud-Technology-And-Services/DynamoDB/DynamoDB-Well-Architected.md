## DynamoDB & AWS Well-Architected Framework Examples

Below are practical examples of how to apply each of the six AWS Well-Architected Framework pillars to Amazon DynamoDB.

---

### 1. Operational Excellence

* **Infrastructure as Code**: Define DynamoDB tables, GSIs, TTL rules, and point-in-time recovery in CloudFormation or Terraform.
* **Automated Deployments**: Use CodePipeline to deploy table updates (e.g. new GSIs) and SSM Automation to apply capacity adjustments.
* **Runbooks & Playbooks**: Create Systems Manager runbooks for common operational tasks, such as restoring a backup or handling throttling events.

### 2. Security

* **Access Control**: Use IAM policies with `dynamodb:Condition` on `dynamodb:LeadingKeys` to enforce row-level permissions.
* **Encryption**: Enable encryption at rest with customer-managed CMKs and enforce TLS for all application connections.
* **Network Protection**: Configure VPC endpoints and security groups to restrict table access to specific subnets or Lambda functions.
* **Audit Logging**: Enable CloudTrail logging for all DynamoDB API calls and route logs to CloudWatch Logs for analysis.

### 3. Reliability

* **High Availability**: Use On-Demand or Provisioned mode with Auto Scaling across multiple AZs—DynamoDB automatically replicates data.
* **Backups & Restores**: Schedule on-demand backups and enable point-in-time recovery; regularly test restores in a sandbox account.
* **Error Handling**: Implement exponential backoff and retry logic in your SDK calls to handle `ProvisionedThroughputExceededException`.
* **Fault Isolation**: Tag tables by environment (dev/test/prod) and configure separate monitoring and alerting channels.

### 4. Performance Efficiency

* **Adaptive Capacity**: Leverage DynamoDB’s adaptive capacity to handle uneven traffic across partitions without manual intervention.
* **DAX Caching**: Deploy DynamoDB Accelerator for read-heavy workloads, reducing average latency from single-digit ms to microseconds.
* **Efficient Queries**: Design composite keys and GSIs to support access patterns without table scans; project only needed attributes.
* **Auto Scaling**: Configure provisioned tables with target utilization to automatically adjust RCUs/WCUs based on load.

### 5. Cost Optimization

* **On-Demand Mode**: Use On-Demand billing for unpredictable or spiky workloads to avoid over-provisioning.
* **Provisioned Mode Savings**: For stable workloads, use Provisioned capacity with Auto Scaling and consider Savings Plans for long-term discounts.
* **Time to Live (TTL)**: Enable TTL on ephemeral data (e.g., session tokens) to automatically remove old items and reduce storage cost.
* **Monitoring & Alerts**: Set CloudWatch billing alerts on RCU/WCU usage to detect and right-size over-provisioned tables.

### 6. Sustainability

* **Right-Sizing**: Regularly review usage patterns and downsize provisioned capacity or switch to On-Demand during low-traffic periods.
* **Efficient Storage**: Use TTL to expire stale items; archive rarely accessed data to S3 for long-term retention.
* **Energy-Efficient Instances**: Where possible, leverage DAX clusters with Graviton2-based instances to reduce vCPU-hours.
* **Resource Cleanup**: Automate deletion of abandoned tables and expired backups via AWS Config rules and Lifecycle Manager.

---

*These examples illustrate applying the Well-Architected pillars to DynamoDB for robust, secure, and cost-effective designs.*
