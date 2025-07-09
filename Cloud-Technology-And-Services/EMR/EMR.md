## AWS EMR (Elastic MapReduce)

### Overview
AWS EMR is a fully managed big data platform that simplifies running open-source frameworks such as Apache Hadoop, Spark, Presto, Hive, HBase, and Flink on AWS. It automates provisioning, configuration, tuning, and scaling of clusters, so you can focus on data processing instead of infrastructure.

### Key Features
- **Managed Cluster Provisioning**  
  Auto-provision EC2 instances, bootstrap software, and configure clusters in minutes.
- **Flexible Frameworks**  
  Support for Hadoop, Spark, Hive, HBase, Presto, Flink, and more.
- **Auto Scaling & Managed Scaling**  
  Dynamically add or remove instances based on workload or cost targets.
- **EMR Serverless**  
  Run analytics applications without provisioning clusters; pay only for resources used.
- **EMR on EKS**  
  Deploy Spark, Hive, and Presto jobs on your Kubernetes cluster managed by Amazon EKS.
- **EMR Studio & Notebooks**  
  Integrated IDE and Jupyter-compatible notebooks for interactive data exploration.

### Core Concepts
- **Master, Core & Task Nodes**  
  - **Master**: Coordinates the cluster (YARN ResourceManager, HDFS NameNode).  
  - **Core**: Runs HDFS DataNode and YARN NodeManager—stores data and runs tasks.  
  - **Task**: Runs only YARN NodeManager—executes processing steps without HDFS storage.
- **Steps**  
  Discrete units of work (e.g., Spark job, Hive script) submitted to the cluster’s master.
- **Release Labels**  
  Version identifiers (e.g., `emr-6.6.0`) that bundle specific framework and Hadoop versions.

### Common Use Cases
- **Batch ETL**: Transform and load large datasets in S3 into data warehouses (Redshift, RDS).  
- **Interactive Analytics**: Run ad-hoc SQL queries with Presto or Hive.  
- **Machine Learning**: Train models at scale with Spark MLlib.  
- **Streaming**: Process real-time data with Apache Flink or Spark Streaming.

### Pricing Model
- **EC2 Instance-Hours**: Billed per second with a one-minute minimum, based on instance type.  
- **EMR Pricing**: Per-second charge on top of EC2 for EMR Serverless and EMR on EKS.  
- **Storage**: S3 data transfer and storage fees apply separately.

### Security & Compliance
- **IAM Roles**: Separate EMR service role and EC2 instance profile with least-privilege policies.  
- **Encryption**: At-rest (S3, HDFS, EBS) and in-transit (TLS) encryption options.  
- **VPC Integration**: Launch clusters in private subnets, control network traffic with Security Groups and NACLs.  
- **Kerberos**: Optional Kerberos realm integration for fine-grained access control.

### Integrations
- **Data Sources**: S3, DynamoDB, RDS, Redshift, Kinesis Data Streams  
- **Catalog & Metadata**: AWS Glue Data Catalog or Hive Metastore  
- **Monitoring & Logging**: CloudWatch Metrics, CloudTrail, YARN UI, Ganglia

### Example: Create a Spark Cluster with AWS CLI
```bash
aws emr create-cluster \
  --name "SparkCluster" \
  --release-label emr-6.6.0 \
  --applications Name=Hadoop Name=Spark \
  --ec2-attributes KeyName=MyKeyPair,InstanceProfile=EMR_EC2_DefaultRole \
  --instance-type m5.xlarge \
  --instance-count 3 \
  --use-default-roles \
  --region us-east-1
