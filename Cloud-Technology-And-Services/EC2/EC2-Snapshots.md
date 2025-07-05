## EBS Snapshots

Amazon EBS Snapshots are incremental, point-in-time backups of EBS volumes, stored in Amazon S3 behind the scenes. Snapshots capture only changed blocks after the first full snapshot, optimizing storage and cost.

### Key Characteristics

* **Incremental Backups**: After the initial snapshot, only modified blocks are stored.
* **Durability & Availability**: Snapshots are stored redundantly across multiple Availability Zones.
* **Consistency**: Can be created while the volume is in-use; use file system freeze or application quiesce for crash-consistent backups.
* **Cross-Region Copy**: Snapshots can be copied across AWS Regions for DR and compliance.

### Use Cases

* **Disaster Recovery**: Restore volumes in the same or different Region.
* **Data Protection**: Regular backups of critical data.
* **Cloning Environments**: Create new volumes from snapshots to spin up test or dev environments.
* **Migrations**: Copy snapshots to migrate data between accounts or Regions.

### AWS CLI Examples

```bash
# 1. Create a snapshot from a volume
aws ec2 create-snapshot \
  --volume-id vol-0123456789abcdef0 \
  --description "Daily backup snapshot"

# 2. List snapshots for a volume
aws ec2 describe-snapshots \
  --filters Name=volume-id,Values=vol-0123456789abcdef0

# 3. Copy a snapshot to another region
aws ec2 copy-snapshot \
  --source-region us-east-1 \
  --source-snapshot-id snap-0123456789abcdef0 \
  --destination-region eu-west-1 \
  --description "Cross-region copy"

# 4. Create a volume from a snapshot
aws ec2 create-volume \
  --availability-zone us-east-1a \
  --snapshot-id snap-0123456789abcdef0

# 5. Delete a snapshot
aws ec2 delete-snapshot --snapshot-id snap-0123456789abcdef0
```

### Python Example (boto3)

```python
import boto3

ec2 = boto3.client('ec2', region_name='us-east-1')

# Create a snapshot
response = ec2.create_snapshot(
    VolumeId='vol-0123456789abcdef0',
    Description='Automated backup'
)
print('Snapshot ID:', response['SnapshotId'])

# Copy snapshot to another region
ec2_west = boto3.client('ec2', region_name='eu-west-1')
copy = ec2_west.copy_snapshot(
    SourceRegion='us-east-1',
    SourceSnapshotId=response['SnapshotId'],
    Description='Cross-region copy'
)
print('Copied Snapshot ID:', copy['SnapshotId'])
```

### Best Practices

* **Automate with Lifecycle Manager**: Use Data Lifecycle Manager to schedule snapshot creation and retention.
* **Tagging**: Tag snapshots with Purpose, Date, and Retention to manage and clean up old backups.
* **Locking**: Enable snapshot lock via AWS Backup for compliance and immutability.
* **Monitor**: Track snapshot usage and age with Amazon CloudWatch and AWS Config rules.

---

**References:**

* Amazon EBS Snapshots: [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)
* Data Lifecycle Manager: [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html)
