# Amazon DocumentDB (with MongoDB compatibility)

Amazon DocumentDB is a fully managed, scalable, and highly durable document database service designed to be compatible with MongoDB workloads.

## Key Features

* **MongoDB Compatibility**
  • Supports MongoDB 3.6, 4.0, and 5.0 APIs, drivers, and tools.

* **Fully Managed**
  • Automated deployment, backups, patching, and scaling.
  • Continuous backups to Amazon S3 with point-in-time recovery up to the last second.

* **Scalability & Performance**
  • Storage automatically scales up to 64 TB without downtime.
  • Read scalability via up to 15 low-latency read replicas.
  • SSD-backed storage with high throughput and low latency.

* **High Availability & Durability**
  • Replicates six copies of data across three Availability Zones (AZs).
  • Automatic failover typically within 30 seconds.

* **Security**
  • Encryption at rest using AWS KMS.
  • Encryption in transit with TLS.
  • Network isolation via Amazon VPC.
  • Integration with IAM for authentication and fine-grained access control.

## Common Use Cases

* **Content Management**: Flexible schema for dynamic content such as articles, user profiles, catalogs.
* **IoT Applications**: Store and query semi-structured telemetry data.
* **Mobile & Web Applications**: Rapid development with JSON document model.
* **Real-Time Analytics**: Low-latency querying on large document sets.

## Pricing Overview (US East - N. Virginia)

| Component          | Pricing                                                                |
| ------------------ | ---------------------------------------------------------------------- |
| **Instance Class** | db.r5.large: \$0.277 per hour<br>db.r5.xlarge: \$0.554 per hour        |
| **Storage**        | \$0.10 per GB-month (provisioned)                                      |
| **I/O Requests**   | \$0.20 per million requests                                            |
| **Backup Storage** | First 100% of cluster storage free; additional at \$0.021 per GB-month |

> Pricing varies by region and instance type. See the [DocumentDB Pricing](https://aws.amazon.com/documentdb/pricing/) page for details.

## Getting Started Example (AWS CLI)

```bash
# 1. Create a security group
aws ec2 create-security-group \
  --group-name docdb-sg --description "DocDB access" --vpc-id vpc-01234567
aws ec2 authorize-security-group-ingress \
  --group-id sg-01234567 --protocol tcp --port 27017 --cidr 10.0.0.0/16

# 2. Create a DocumentDB cluster
aws docdb create-db-cluster \
  --db-cluster-identifier my-docdb-cluster \
  --engine docdb \
  --master-username admin \
  --master-user-password MyPassword123 \
  --vpc-security-group-ids sg-01234567 \
  --backup-retention-period 7

# 3. Create an instance in the cluster
aws docdb create-db-instance \
  --db-instance-identifier my-docdb-instance \
  --db-instance-class db.r5.large \
  --engine docdb \
  --db-cluster-identifier my-docdb-cluster

# 4. Connect via mongo shell
mongo --host my-docdb-cluster.cluster-xxxxxxxxxx.us-east-1.docdb.amazonaws.com:27017 \
  --username admin --password MyPassword123 --ssl --sslCAFile rds-combined-ca-bundle.pem
```

## Best Practices

* **Use IAM authentication** for enhanced security instead of password-based access.
* **Enable TLS** for all connections to encrypt data in transit.
* **Monitor with Amazon CloudWatch**: Track CPU, memory, and connections; set alarms.
* **Scale read capacity** with multiple instances and read replicas.
* **Automate backups** retention and recovery testing via AWS Backup.

---

**References:**

* Amazon DocumentDB User Guide: [https://docs.aws.amazon.com/documentdb/latest/developerguide/](https://docs.aws.amazon.com/documentdb/latest/developerguide/)
* Amazon DocumentDB Pricing: [https://aws.amazon.com/documentdb/pricing/](https://aws.amazon.com/documentdb/pricing/)
