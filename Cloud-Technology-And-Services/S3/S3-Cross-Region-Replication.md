## Cross-Region Replication (CRR) in Amazon S3

Amazon S3 Cross-Region Replication (CRR) automatically replicates objects from a source bucket in one AWS Region to a destination bucket in another Region.

### Key Benefits
- **Disaster Recovery & Compliance**  
  Maintain a geographically separate copy for compliance, business continuity, and fail-over scenarios.
- **Low-Latency Access**  
  Serve global users from the nearest Region.
- **Operational Simplicity**  
  Fully managed by AWS—no custom code required.

### Prerequisites & Requirements
1. **Versioning Enabled**  
   Both source and destination buckets must have versioning turned on.
2. **Bucket Permissions**  
   IAM role or bucket policy must allow S3 to replicate objects:
   - Source bucket: `s3:GetObjectVersionForReplication`, `s3:GetObjectVersionAcl`, `s3:GetObjectVersionTagging`
   - Destination bucket: `s3:ReplicateObject`, `s3:ReplicateDelete`, `s3:PutObjectAcl`, `s3:PutObjectTagging`
3. **Same AWS Account or Cross-Account**  
   Can replicate across accounts by granting the appropriate IAM role to the source account.

### How It Works
- **Asynchronous**  
  New or updated objects in the source bucket are queued and sent to the destination.
- **Eventual Consistency**  
  Replicas appear shortly after the source write completes.
- **Metadata & Tags**  
  You can choose to replicate metadata, object tags, and ACLs.

---

### Example: Enable CRR via AWS CLI

```bash
# 1. Enable versioning on both buckets
aws s3api put-bucket-versioning \
  --bucket source-bucket-us-east-1 \
  --versioning-configuration Status=Enabled

aws s3api put-bucket-versioning \
  --bucket dest-bucket-eu-west-1 \
  --versioning-configuration Status=Enabled

# 2. Create an IAM role for replication
aws iam create-role \
  --role-name s3-replication-role \
  --assume-role-policy-document file://trust-policy.json

# trust-policy.json should allow s3.amazonaws.com to assume the role

# 3. Attach replication policy to the role
aws iam put-role-policy \
  --role-name s3-replication-role \
  --policy-name S3ReplicationPolicy \
  --policy-document file://replication-policy.json

# replication-policy.json grants the necessary s3:Get* on source and s3:Replicate* on destination

# 4. Configure replication on the source bucket
aws s3api put-bucket-replication \
  --bucket source-bucket-us-east-1 \
  --replication-configuration '{
    "Role": "arn:aws:iam::123456789012:role/s3-replication-role",
    "Rules": [
      {
        "ID": "ReplicateToEU",
        "Status": "Enabled",
        "Priority": 1,
        "Filter": { "Prefix": "" },
        "Destination": {
          "Bucket": "arn:aws:s3:::dest-bucket-eu-west-1",
          "StorageClass": "STANDARD"
        }
      }
    ]
  }'
