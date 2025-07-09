# 30 AWS EMR Multiple-Choice Questions

1. What node type in an EMR cluster runs both HDFS DataNode and YARN NodeManager?  
   - A. Master  
   - B. Core  
   - C. Task  
   - D. Client  

2. Which EMR component coordinates YARN resource management?  
   - A. HDFS NameNode  
   - B. YARN ResourceManager  
   - C. Spark Driver  
   - D. Hive Metastore  

3. What is a “release label” in EMR?  
   - A. A tag on an S3 bucket  
   - B. The version bundle of Hadoop and supported frameworks  
   - C. The Amazon Linux AMI ID  
   - D. A CloudWatch log group name  

4. Which action lets you install custom software on every node at launch?  
   - A. Bootstrap action  
   - B. Step action  
   - C. Lifecycle configuration  
   - D. Initialization hook  

5. What is EMR Serverless designed for?  
   - A. Running long-lived clusters only  
   - B. Running jobs without provisioning clusters  
   - C. Managing Kubernetes clusters  
   - D. Hosting web servers  

6. EMR on EKS allows you to:  
   - A. Run EMR steps on EC2 only  
   - B. Run Spark and Hive jobs on a Kubernetes cluster  
   - C. Deploy Docker containers automatically  
   - D. Replace EMR Serverless  

7. Which catalog can EMR use for metadata?  
   - A. AWS Glue Data Catalog  
   - B. AWS Systems Manager  
   - C. DynamoDB Streams  
   - D. CloudFormation StackSets  

8. In EMR, what is a “step”?  
   - A. A single EC2 instance  
   - B. A discrete unit of work such as a Spark job or Hive script  
   - C. A security group rule  
   - D. A monitoring alarm  

9. Where do EMR clusters send application logs by default?  
   - A. S3 bucket (if configured)  
   - B. DynamoDB  
   - C. RDS  
   - D. EBS snapshot  

10. Which encryption option can you enable on EMR EBS volumes?  
    - A. TLS  
    - B. KMS-managed at-rest encryption  
    - C. AES-256 in-flight  
    - D. SSH tunneling  

11. What IAM role does the EMR service assume to create and manage resources?  
    - A. EC2 instance profile  
    - B. Service role (AmazonElasticMapReduceRole)  
    - C. S3 bucket policy  
    - D. EMR Studio user role  

12. What feature adds or removes instances based on workload?  
    - A. Auto Scaling rules  
    - B. Managed scaling  
    - C. Spot Fleet  
    - D. Elastic Beanstalk  

13. Managed scaling in EMR differs from auto-scaling because it:  
    - A. Requires manual step definitions  
    - B. Optimizes cost and performance automatically  
    - C. Only works with Spot instances  
    - D. Is not available in EMR Serverless  

14. EMR pricing includes a per-second charge for EMR Serverless plus:  
    - A. EBS IOPS  
    - B. EC2 instance-hours for provisioned clusters  
    - C. Lambda invocations  
    - D. Data transfer inside VPC  

15. Which CLI command creates an EMR cluster?  
    - A. `aws emr start-cluster`  
    - B. `aws emr create-cluster`  
    - C. `aws emr launch-cluster`  
    - D. `aws emr init-cluster`  

16. In CloudFormation, which resource type defines an EMR cluster?  
    - A. AWS::EMR::Cluster  
    - B. AWS::EMR::InstanceGroup  
    - C. AWS::EMR::JobFlow  
    - D. AWS::EMR::Step  

17. On which node does the HDFS NameNode run?  
    - A. Task node  
    - B. Core node  
    - C. Master node  
    - D. Edge node  

18. The YARN NodeManager runs on:  
    - A. Master only  
    - B. Core and task nodes  
    - C. Edge nodes only  
    - D. No nodes  

19. Which tool can you use to copy data between S3 and HDFS on EMR?  
    - A. DistCp  
    - B. S3Sync  
    - C. DataPipeline  
    - D. Snowball  

20. How do you submit a Spark job to an EMR cluster via CLI?  
    - A. `aws emr add-steps --steps Type=Spark`  
    - B. `spark-submit --master yarn`  
    - C. `aws emr run-job-flow`  
    - D. `hadoop jar spark.jar`  

21. On which port is the Spark Web UI accessible by default?  
    - A. 8088  
    - B. 18080  
    - C. 4040  
    - D. 50070  

22. EMR Studio provides:  
    - A. A managed Jupyter-compatible notebook IDE  
    - B. A replacement for Cloud9  
    - C. A CLI tool only  
    - D. A mobile app  

23. To use EMR Studio, you must create:  
    - A. A SageMaker domain  
    - B. A Studio workspace with IAM domain and user profiles  
    - C. An EC2 key pair  
    - D. A Virtual Private Gateway  

24. Which EMR endpoint type allows interactive queries without a cluster?  
    - A. Cluster endpoint  
    - B. Managed endpoint (EMR Serverless)  
    - C. REST endpoint  
    - D. SSH endpoint  

25. How many steps can you run concurrently in an EMR cluster by default?  
    - A. 1  
    - B. 3  
    - C. 10  
    - D. Unlimited  

26. Which framework in EMR supports event-time processing for streaming?  
    - A. Hive  
    - B. Presto  
    - C. Apache Flink  
    - D. HBase  

27. Which EMR feature lets you run Presto for interactive SQL?  
    - A. Presto Serverless  
    - B. EMR Presto Application  
    - C. Athena integration  
    - D. EMR Graph Engine  

28. EMRFS stands for:  
    - A. EMR File System connector to S3  
    - B. Elastic MapReduce File Share  
    - C. EMR Full Stack  
    - D. EMR Fast Storage  

29. If a step fails, you can debug by inspecting:  
    - A. CloudTrail events  
    - B. YARN application logs in S3 or HDFS  
    - C. RDS error logs  
    - D. Lambda metrics  

30. Which service can ingest EMR metrics for dashboards and alarms?  
    - A. CloudWatch  
    - B. X-Ray  
    - C. Inspector  
    - D. Trusted Advisor  

---

## Answers

1. B  
2. B  
3. B  
4. A  
5. B  
6. B  
7. A  
8. B  
9. A  
10. B  
11. B  
12. A  
13. B  
14. B  
15. B  
16. A  
17. C  
18. B  
19. A  
20. A  
21. C  
22. A  
23. B  
24. B  
25. A  
26. C  
27. B  
28. A  
29. B  
30. A  
