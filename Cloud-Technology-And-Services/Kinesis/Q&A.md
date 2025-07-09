# 30 AWS Kinesis Multiple-Choice Questions

1. What is the default data retention period for Kinesis Data Streams?  
   - A. 24 hours  
   - B. 48 hours  
   - C. 7 days  
   - D. 30 days  

2. What is the maximum data retention period you can configure for Kinesis Data Streams?  
   - A. 24 hours  
   - B. 7 days  
   - C. 30 days  
   - D. 90 days  

3. What is the maximum ingest throughput per shard in Kinesis Data Streams?  
   - A. 1 MB/s or 1,000 records/s  
   - B. 2 MB/s or 2,000 records/s  
   - C. 5 MB/s or 5,000 records/s  
   - D. 10 MB/s or 10,000 records/s  

4. Which API call writes multiple records in a single request to a stream?  
   - A. PutRecord  
   - B. PutRecords  
   - C. BatchWriteItem  
   - D. WriteRecords  

5. Which required parameter must you include when calling PutRecord?  
   - A. Data only  
   - B. Data plus PartitionKey  
   - C. Data plus ExplicitHashKey  
   - D. Data plus SequenceNumber  

6. What feature provides each consumer with a dedicated 2 MB/s read throughput per shard?  
   - A. Auto-scaling  
   - B. Enhanced fan-out  
   - C. Shared throughput  
   - D. Serverless processing  

7. With enhanced fan-out enabled, how many consumers can you attach per shard?  
   - A. 1  
   - B. 5  
   - C. 10  
   - D. Unlimited  

8. Which Kinesis service automatically loads streaming data into S3, Redshift, Elasticsearch, or Splunk?  
   - A. Data Streams  
   - B. Data Firehose  
   - C. Data Analytics  
   - D. Video Streams  

9. In Firehose buffering hints, what is the maximum buffer size you can configure?  
   - A. 1 MB  
   - B. 5 MB  
   - C. 10 MB  
   - D. 50 MB  

10. How do you apply in-flight record transformations in Firehose?  
    - A. AWS Glue  
    - B. AWS Lambda  
    - C. Amazon KMS  
    - D. Amazon Athena  

11. Which language does Kinesis Data Analytics for SQL applications use?  
    - A. SQL  
    - B. Python  
    - C. Java  
    - D. Node.js  

12. Under the hood, Kinesis Data Analytics for Apache Flink runs on which engine?  
    - A. Apache Spark  
    - B. Apache Flink  
    - C. Apache Hive  
    - D. Apache Storm  

13. Kinesis Video Streams uses which SDK for producers and consumers?  
    - A. Data Streams SDK  
    - B. Video Streams SDK  
    - C. MediaConnect SDK  
    - D. Live Streaming API  

14. Video Streams retention period is measured in:  
    - A. Hours  
    - B. Days  
    - C. Minutes  
    - D. Streams  

15. How do you scale the capacity of a Kinesis Data Stream?  
    - A. Increase retention period  
    - B. Add or remove shards  
    - C. Change encryption settings  
    - D. Update Firehose configuration  

16. Merging shards in a stream primarily reduces:  
    - A. Latency  
    - B. Cost  
    - C. Security risk  
    - D. Data retention  

17. Splitting a shard increases:  
    - A. Data durability  
    - B. Throughput capacity  
    - C. Encryption strength  
    - D. Retention period  

18. Which server-side encryption option is supported for Kinesis Data Streams?  
    - A. SSE-S3  
    - B. SSE-KMS  
    - C. SSE-C  
    - D. No encryption  

19. What is the default soft limit for the number of shards per stream in most AWS regions?  
    - A. 500  
    - B. 1,000  
    - C. 200  
    - D. 50  

20. The Kinesis Agent is primarily used to:  
    - A. Consume data from streams  
    - B. Collect and send log files to Data Streams  
    - C. Transform records in-flight  
    - D. Monitor stream metrics  

21. Which IAM permission is required to call PutRecord on a stream?  
    - A. kinesis:PutRecord  
    - B. kinesis:GetRecords  
    - C. kinesis:DescribeStream  
    - D. kinesis:DeleteStream  

22. Which CloudWatch metric shows the total incoming data volume for a shard?  
    - A. IncomingBytes  
    - B. GetRecords.IteratorAgeMilliseconds  
    - C. WriteProvisionedThroughputExceeded  
    - D. ReadProvisionedThroughputExceeded  

23. Which metric indicates how far behind a consumer is from the latest record?  
    - A. GetRecords.IteratorAgeMilliseconds  
    - B. AgeOfRecord  
    - C. IteratorLag  
    - D. ProcessingLatency  

24. To connect to a private Kinesis Data Stream from within a VPC without internet access, you use:  
    - A. NAT Gateway  
    - B. VPC Interface Endpoint (AWS PrivateLink)  
    - C. Internet Gateway  
    - D. Transit Gateway  

25. Which API creates the event source mapping between a stream and a Lambda function?  
    - A. AddTrigger  
    - B. SubscribeToStream  
    - C. CreateEventSourceMapping  
    - D. InvokeFunction  

26. Kinesis Data Firehose does NOT support which delivery destination?  
    - A. Amazon S3  
    - B. Amazon Redshift  
    - C. Amazon DynamoDB  
    - D. Splunk  

27. Which runtime environment does Kinesis Data Analytics for SQL use?  
    - A. Python  
    - B. SQL  
    - C. Java  
    - D. Scala  

28. Kinesis Data Analytics for Apache Flink applications must be written in:  
    - A. SQL scripts  
    - B. Java or Python  
    - C. Spark code  
    - D. HiveQL  

29. What tool can you use to test Kinesis Data Analytics SQL queries locally?  
    - A. KDA CLI  
    - B. EMR Studio  
    - C. Flink Local Runner  
    - D. JDBC Driver  

30. Which AWS service natively integrates with Kinesis Data Streams for real-time data visualization?  
    - A. Amazon QuickSight  
    - B. AWS CloudTrail  
    - C. AWS CloudFormation  
    - D. AWS CodeBuild  

---

## Answers

1. A  
2. B  
3. A  
4. B  
5. B  
6. B  
7. D  
8. B  
9. B  
10. B  
11. A  
12. B  
13. B  
14. A  
15. B  
16. B  
17. B  
18. B  
19. A  
20. B  
21. A  
22. A  
23. A  
24. B  
25. C  
26. C  
27. B  
28. B  
29. C  
30. A  
