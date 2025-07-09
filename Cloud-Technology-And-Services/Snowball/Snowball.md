## AWS Snowball

### Overview  
AWS Snowball is a physical data transport service that accelerates moving large amounts of data into and out of AWS. It’s ideal when network transfer is too slow, costly, or unreliable.

### Device Types & Variants  
- **Snowball Edge Storage Optimized**  
  - 80 TB usable storage, up to 52 vCPUs, ideal for heavy storage workloads.  
- **Snowball Edge Compute Optimized**  
  - 42 TB usable storage, up to 96 vCPUs and optional GPU for local processing (IoT, analytics, ML).  
- **Snowball**  
  - Up to 50 TB usable capacity; simple import/export devices.  
- **Snowmobile**  
  - 45 PB trailer for exabyte-scale data migrations.

### Key Features  
- **High-Performance Offline Transfer**  
  - Internal 10 Gbps network speeds; supports concurrent clients.  
- **End-to-End Encryption & Security**  
  - AES-256 encryption managed by AWS KMS; tamper-evident seals and secure boot.  
- **Seamless S3 & Glacier Integration**  
  - Import/export directly to S3 buckets or archive to Glacier.  
- **Local Compute with Edge Lambda & EC2**  
  - Run functions and instances on Snowball Edge Compute devices without constant connectivity.  
- **Rugged & Durable**  
  - MIL-STD-810G tested for dust, shock, and vibration.

### Common Use Cases  
- **Large-Scale Data Migration**  
  - Move petabytes from on-premises to AWS without saturating WAN links.  
- **Edge Data Collection**  
  - Gather IoT or scientific data at remote sites with limited bandwidth.  
- **Offline Machine Learning**  
  - Train models locally on Snowball Edge Compute and then ship results to AWS.  
- **Disaster Recovery & Backup**  
  - Create offline vaults of critical data in S3 or Glacier.

### Pricing Model  
- **Device Rental Fee**  
  - ~\$15/day for standard Snowball, ~\$30/day for Snowball Edge devices.  
- **Job Service Fee**  
  - Flat per-job charge (region-dependent, typically \$200–\$300).  
- **Storage Fees**  
  - Standard S3/Glacier storage rates apply once data is imported.

### Security & Compliance  
- **On-Device Encryption**  
  - Data encrypted at rest with KMS-managed keys; never exposed unencrypted.  
- **Chain of Custody**  
  - Sealed, tracked shipments with signature confirmation.  
- **Certifications**  
  - HIPAA, PCI DSS, SOC 1/2/3, ISO 27001, GDPR, FedRAMP.  
- **Access Control**  
  - IAM-based job creation; S3 bucket policies restrict imported data access.

### Integrations  
- **Amazon S3 & Glacier**  
  - Configure import/export jobs to specific buckets or vaults.  
- **AWS Lambda & EC2 on Edge**  
  - Execute compute tasks locally on Snowball Edge.  
- **AWS DataSync**  
  - After import, use DataSync for incremental sync and replication.

### Example: Create an Import Job via AWS CLI  
```bash
aws snowball create-job \
  --job-type IMPORT \
  --resources '{"S3Resources":[{"BucketArn":"arn:aws:s3:::my-bucket","KeyRange":{"BeginMarker":"","EndMarker":""}}]}' \
  --address-id addr-0a1b2c3d4e5f6g7h \
  --snowball-capacity-preference T80 \
  --kms-key-arn arn:aws:kms:us-east-1:123456789012:key/abcd-ef01-2345-6789 \
  --role-arn arn:aws:iam::123456789012:role/AWSDataTransferRole \
  --description "Import data to S3"
