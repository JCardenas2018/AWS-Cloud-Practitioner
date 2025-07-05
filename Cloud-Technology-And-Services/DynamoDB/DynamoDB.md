# Amazon DynamoDB

Amazon DynamoDB is a fully managed, serverless NoSQL database service that provides fast and predictable performance with seamless scalability.

## Key Features

* **Data Model**
  • Key-value and document data structures.

  • Tables, items (rows), and attributes (columns).
* **Performance & Scalability**
  • Single-digit millisecond latency at any scale.

  • Automatic partitioning to support virtually unlimited throughput and storage.
* **Capacity Modes**
  • **On-Demand:** Pay-per-request for unpredictable workloads.

  • **Provisioned:** Specify read/write units; optionally auto-scale capacity.
* **Global Tables**
  • Multi-region, multi-master replication for global applications and disaster recovery.
* **In-Memory Acceleration (DAX)**
  • Up to 10× performance improvement with DynamoDB Accelerator (DAX), a fully managed in-memory cache.
* **ACID Transactions**
  • Support for coordinated, all-or-nothing transactions across multiple items and tables.
* **Streams & Triggers**
  • Change data capture via DynamoDB Streams; integrate with AWS Lambda for event-driven workflows.
* **Security**
  • Encryption at rest with AWS KMS.

  • Fine-grained access control with IAM policies and attribute-level permissions.

  • VPC Endpoints to keep traffic within your VPC.
* **Backups & Restore**
  • On-demand backups and point-in-time recovery (PITR) for continuous data protection.
* **Time to Live (TTL)**
  • Automatic deletion of expired items to reduce storage and cost.

## Common Use Cases

* **Gaming**: Player profiles, leaderboards, session state.
* **IoT**: Telemetry ingestion and time-series data.
* **Mobile & Web Applications**: User preferences, shopping carts.
* **Real-Time Analytics**: Event tracking, dashboard counters.
* **Ad Tech**: User segmentation, bidding metadata.
* **Microservices**: Shared state, cache replacement.

## Pricing Overview (US East – N. Virginia)

| Component                | Pricing                                                                                      |
| ------------------------ | -------------------------------------------------------------------------------------------- |
| **On-Demand Capacity**   | Read: \$1.25 per million read request units<br>Write: \$1.25 per million write request units |
| **Provisioned Capacity** | Read Unit: \$0.00013 per RU-hour<br>Write Unit: \$0.00065 per WU-hour                        |
| **Storage**              | \$0.25 per GB-month                                                                          |
| **DynamoDB Accelerator** | Nodes from \$0.136 per node-hour                                                             |
| **Streams**              | \$0.02 per GB of data read                                                                   |
| **Backups**              | \$0.10 per GB-month for on-demand backups                                                    |

> **Note:** Pricing varies by region and usage patterns. See the [DynamoDB Pricing](https://aws.amazon.com/dynamodb/pricing/) page for details.

## Getting Started Examples

### AWS CLI

```bash
# 1. Create a table
aws dynamodb create-table \
  --table-name Users \
  --attribute-definitions AttributeName=UserId,AttributeType=S \
  --key-schema AttributeName=UserId,KeyType=HASH \
  --billing-mode PAY_PER_REQUEST

# 2. Put an item
aws dynamodb put-item \
  --table-name Users \
  --item '{"UserId": {"S": "123"}, "Name": {"S": "Alice"}, "Score": {"N": "42"}}'

# 3. Get an item
aws dynamodb get-item \
  --table-name Users \
  --key '{"UserId": {"S": "123"}}'

# 4. Query by secondary index
aws dynamodb query \
  --table-name Orders \
  --index-name CustomerIndex \
  --key-condition-expression "CustomerId = :cid" \
  --expression-attribute-values '{":cid": {"S": "C456"}}'
```

### Python (boto3)

```python
import boto3

ddb = boto3.resource('dynamodb', region_name='us-east-1')
users = ddb.Table('Users')

# Add a user
users.put_item(Item={'UserId': '123', 'Name': 'Alice', 'Score': 42})

# Read a user
resp = users.get_item(Key={'UserId': '123'})
print(resp.get('Item'))

# Update a user’s score
users.update_item(
    Key={'UserId': '123'},
    UpdateExpression='SET Score = :new',
    ExpressionAttributeValues={':new': 100}
)
```

## Best Practices

* **Key Design**: Choose partition and sort keys to distribute workload evenly and support access patterns.
* **Use GSIs/LSIs Sparingly**: Create only necessary secondary indexes to optimize costs and performance.
* **Enable Auto Scaling**: For provisioned tables, configure target utilization to handle variable load.
* **Monitor Hot Partitions**: Use CloudWatch metrics (`ConsumedReadCapacityUnits`, `ConsumedWriteCapacityUnits`) to detect uneven traffic.
* **Implement Caching**: Use DAX or an external cache for read-heavy workloads.
* **Leverage TTL**: Expire stale data automatically to control storage costs.
* **Encrypt Data**: Use KMS CMKs and enforce TLS for in-transit encryption.

**References:**

* Amazon DynamoDB Developer Guide: [https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/)
* DynamoDB Best Practices: [https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/best-practices.html](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/best-practices.html)
