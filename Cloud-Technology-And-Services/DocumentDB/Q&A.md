# Amazon DocumentDB Knowledge Assessment (30 Questions)

Answer the following multiple-choice questions about Amazon DocumentDB. Select the best option for each.

1. **What compatibility does Amazon DocumentDB offer?**
   A) MySQL 5.7
   B) PostgreSQL 12
   C) MongoDB 4.0
   D) Cassandra 3.11

2. **Which storage scaling limit does DocumentDB automatically support?**
   A) 16 TB
   B) 32 TB
   C) 64 TB
   D) 128 TB

3. **How many read replicas can you have per DocumentDB cluster?**
   A) 5
   B) 10
   C) 15
   D) 20

4. **What is the minimum number of AZs for a high-availability cluster?**
   A) 1
   B) 2
   C) 3
   D) 4

5. **Which feature provides point-in-time recovery?**
   A) Automated snapshots
   B) Manual snapshots only
   C) Journal backups
   D) Archive logs

6. **What engine version is supported by DocumentDB?**
   A) MongoDB 2.6
   B) MongoDB 3.6
   C) MongoDB 6.0
   D) MongoDB 5.0

7. **Which protocol secures connections in transit?**
   A) HTTP
   B) TLS/SSL
   C) FTP
   D) SSH

8. **Which AWS service stores the backup snapshots of DocumentDB?**
   A) S3
   B) Glacier
   C) EBS
   D) EFS

9. **Which CLI command creates a new DocumentDB cluster?**
   A) aws docdb create-db-instance
   B) aws docdb create-db-cluster
   C) aws ec2 create-db-cluster
   D) aws rds create-db-cluster

10. **How much does I/O cost in DocumentDB?**
    A) \$0.05 per million requests
    B) \$0.20 per million requests
    C) \$0.10 per million requests
    D) Free

11. **Which instance class is Graviton-based?**
    A) db.r5.large
    B) db.r6g.large
    C) db.t3.small
    D) db.m5.large

12. **What is provisioned storage priced at?**
    A) \$0.05 per GB-month
    B) \$0.10 per GB-month
    C) \$0.20 per GB-month
    D) \$0.15 per GB-month

13. **Which component defines software and config steps in Image Builder?**
    A) Recipe
    B) Pipeline
    C) Distribution Configuration
    D) Infrastructure Configuration

14. **Which VPC feature isolates DocumentDB traffic?**
    A) Public Subnet
    B) VPC Endpoint
    C) Internet Gateway
    D) NAT Gateway

15. **Which IAM feature can authenticate to DocumentDB?**
    A) IAM User Password
    B) IAM Authentication
    C) Cognito Identity
    D) STS Token only

16. **Which metric indicates replication lag?**
    A) CPUUtilization
    B) FreeableMemory
    C) ReplicationLag
    D) ReadIOPS

17. **Which security measure encrypts data at rest?**
    A) Client-side encryption only
    B) SSE-S3 only
    C) AWS KMS-managed CMKs
    D) No encryption supported

18. **Which backup retention period is default?**
    A) 1 day
    B) 7 days
    C) 14 days
    D) 30 days

19. **Which role is required for Cluster creation via CLI?**
    A) AWSServiceRoleForAmazonRDS
    B) AWSServiceRoleForDocDB
    C) AWSServiceRoleForEC2
    D) AmazonDocDBFullAccess

20. **Which document model does DocumentDB use?**
    A) Key-value store
    B) Graph model
    C) Document (JSON)
    D) Relational tables

21. **Which feature automates patching of DocumentDB engines?**
    A) Manual upgrades only
    B) Automatic patching during maintenance
    C) AWS Config
    D) Lambda functions

22. **Which logging helps analyze slow queries?**
    A) Audit logs
    B) General logs
    C) Slow query logs
    D) Error logs

23. **Which pillar covers encryption management?**
    A) Cost Optimization
    B) Security
    C) Performance Efficiency
    D) Operational Excellence

24. **Which feature ensures cluster high availability?**
    A) Single AZ deployment
    B) Multi-AZ replication
    C) Auto Scaling
    D) Read Replicas only

25. **Which CloudWatch alarm would you configure for memory issues?**
    A) CPUUtilization
    B) FreeableMemory
    C) DiskQueueDepth
    D) NetworkOut

26. **Which cost optimization tip applies to DocumentDB?**
    A) Use on-demand instances only
    B) Right-size instances and clean up snapshots
    C) Increase retention period indefinitely
    D) Disable TLS to save costs

27. **Which AWS service can provide insights to right-size DocumentDB?**
    A) AWS Config
    B) CloudWatch Dashboards
    C) AWS Compute Optimizer
    D) AWS Cost Explorer

28. **Which indexing improves read performance?**
    A) Global secondary indexes
    B) Compound indexes
    C) Multi-key indexes
    D) Secondary indexes

29. **Which operation via CLI deletes a DocumentDB cluster?**
    A) delete-db-cluster
    B) drop-db-cluster
    C) destroy-db-cluster
    D) remove-db-cluster

30. **Which sustainability practice applies to DocumentDB?**
    A) Overprovision storage
    B) Use Graviton2 instances and clean up idle resources
    C) Increase backup retention unnecessarily
    D) Disable auto-scaling

---

## Answer Key

1. C
2. C
3. C
4. C
5. A
6. B
7. B
8. A
9. B
10. B
11. B
12. B
13. A
14. B
15. B
16. C
17. C
18. B
19. B
20. C
21. B
22. C
23. B
24. B
25. B
26. B
27. C
28. B
29. A
30. B
