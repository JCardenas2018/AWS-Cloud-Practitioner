# Amazon DynamoDB Knowledge Assessment (30 Questions)

Answer the following multiple-choice questions about Amazon DynamoDB. Select the best option for each.

1. **What data models does DynamoDB support?**
   A) Relational and graph
   B) Key-value and document
   C) Columnar and time-series
   D) Tabular and object

2. **Which capacity mode is best for unpredictable workloads?**
   A) Provisioned
   B) On-Demand
   C) Reserved
   D) Spot

3. **What is a Global Table?**
   A) A table with global secondary indexes
   B) A multi-region, multi-master table
   C) A table replicated within one region
   D) A backup of a table

4. **Which feature provides in-memory acceleration for DynamoDB?**
   A) DAX
   B) ElastiCache
   C) Memcached
   D) Redis

5. **How does DynamoDB Streams help?**
   A) Provides backup snapshots
   B) Captures data modification events
   C) Automatically scales capacity
   D) Encrypts data in transit

6. **Which consistency models does DynamoDB offer for reads?**
   A) Strong and eventual
   B) Linearizable only
   C) Read-after-write only
   D) Eventual only

7. **What unit measures write capacity in provisioned mode?**
   A) WCU
   B) RCU
   C) IOPS
   D) MB/s

8. **Which feature automatically deletes expired items?**
   A) TTL
   B) Time series
   C) Lifecycle policy
   D) Expiration index

9. **Which AWS service integrates with Streams for event-driven workflows?**
   A) EC2
   B) Lambda
   C) Batch
   D) Glue

10. **What is the cost per GB-month for DynamoDB storage?**
    A) \$0.10
    B) \$0.25
    C) \$0.50
    D) \$1.00

11. **Which feature allows you to recover data to any point in time?**
    A) On-demand backups
    B) PITR
    C) Manual snapshots
    D) Streams

12. **How many read replicas can you add per table in a Global Table?**
    A) 1
    B) 3
    C) Multiple regions
    D) Unlimited within one region

13. **Which CloudWatch metric indicates throttling?**
    A) ConsumedReadCapacityUnits
    B) ThrottledRequests
    C) ThrottledEvents
    D) ReadThrottleEvents

14. **Which access control method provides attribute-level permissions?**
    A) VPC endpoints
    B) IAM policies
    C) Security groups
    D) NACLs

15. **Which encryption option is managed by AWS KMS?**
    A) SSE-DynamoDB
    B) SSE-S3
    C) SSE-KMS
    D) Client-side encryption

16. **What is the default AWS region latency for single-digit ms performance?**
    A) Edge locations
    B) Local AZ
    C) Multi-region endpoints
    D) Peered VPCs

17. **Which SDK method writes an item to a DynamoDB table?**
    A) put\_item
    B) write\_item
    C) insert\_item
    D) add\_item

18. **How do you filter results in a Query operation?**
    A) FilterExpression
    B) KeyConditionExpression
    C) WhereClause
    D) QueryFilter

19. **Which feature helps avoid hot partitions?**
    A) Adaptive Capacity
    B) Auto Scaling only
    C) Streams
    D) DAX

20. **Which capacity unit measures read throughput for strongly consistent reads?**
    A) 0.5 RCU
    B) 1 RCU
    C) 2 RCU
    D) 4 RCU

21. **Which backup option is free up to the size of the table?**
    A) Manual backups
    B) On-Demand backups
    C) PITR
    D) Export to S3

22. **Which pricing applies to Streams data reading?**
    A) \$0.02 per 10,000 reads
    B) \$0.02 per GB read
    C) \$0.10 per million reads
    D) Included free of charge

23. **Which Well-Architected pillar involves adaptive capacity?**
    A) Security
    B) Performance Efficiency
    C) Cost Optimization
    D) Reliability

24. **Which feature can accelerate repeated reads?**
    A) Auto Scaling
    B) DAX
    C) Global Tables
    D) Streams

25. **Which use case suits microservices state storage?**
    A) S3 static hosting
    B) DynamoDB
    C) RDS
    D) EBS

26. **Which table setting enforces strong encryption?**
    A) SSE-S3 only
    B) Default encryption with CMK
    C) Transparent encryption
    D) In-transit encryption

27. **Which cost optimization tip applies to DynamoDB?**
    A) Use provisioned mode for spiky traffic
    B) Enable TTL to delete stale items
    C) Disable encryption to save cost
    D) Reduce GSIs frequency

28. **Which CloudFormation resource type creates a DynamoDB table?**
    A) AWS::DynamoDB::Table
    B) AWS::DynamoDBTable
    C) AWS::DynamoDB::Resource
    D) AWS::Database::DynamoDB

29. **Which failure scenario does Global Tables protect against?**
    A) Software bugs
    B) Single AZ failure
    C) Capacity exhaustion
    D) Data corruption

30. **Which sustainability practice helps reduce DynamoDB impact?**
    A) Overprovision capacity
    B) Use DAX with efficient instances
    C) Disable Streams
    D) Keep TTL disabled

---

## Answer Key

1. B
2. B
3. B
4. A
5. B
6. A
7. A
8. A
9. B
10. B
11. B
12. C
13. D
14. B
15. C
16. B
17. A
18. A
19. A
20. B
21. C
22. B
23. B
24. B
25. B
26. B
27. B
28. A
29. B
30. B
