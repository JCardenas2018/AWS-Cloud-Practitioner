# Quiz: AWS CloudTrail (30 Questions)

1. Which type of CloudTrail event includes S3 object-level operations like GetObject?  
   A. Management events  
   B. Data events  
   C. Insights events  
   D. Log file events  

2. What is a “trail” in AWS CloudTrail?  
   A. A copy of API responses  
   B. A configuration that delivers log files to destinations  
   C. A dashboard view of API calls  
   D. A list of active IAM users  

3. By default, where does CloudTrail deliver log files?  
   A. Amazon S3  
   B. Amazon DynamoDB  
   C. Amazon RDS  
   D. Amazon Elasticsearch  

4. How long are events available in CloudTrail Event History in the AWS Console?  
   A. 7 days  
   B. 30 days  
   C. 90 days  
   D. 365 days  

5. Which integration allows you to send CloudTrail events to trigger Lambdas or SNS notifications?  
   A. Amazon Inspector  
   B. AWS Config  
   C. Amazon EventBridge  
   D. AWS X-Ray  

6. What does CloudTrail Insights help you detect?  
   A. S3 bucket encryption status  
   B. Unusual API activity patterns  
   C. EC2 CPU utilization spikes  
   D. RDS backup failures  

7. How can you ensure log files in S3 are not tampered with?  
   A. Enable S3 Versioning  
   B. Use CloudTrail log file validation  
   C. Enable MFA Delete  
   D. Use Glacier storage  

8. Which feature allows multiple AWS accounts in an Organization to be recorded by a single trail?  
   A. Multi-Region  
   B. Organization Trails  
   C. Global Services  
   D. CloudTrail Lake  

9. CloudTrail Data Events incur additional charges and must be...  
   A. Disabled to avoid fees  
   B. Explicitly enabled per resource  
   C. Automatically enabled by default  
   D. Only for global services  

10. Which AWS service do you use to query and analyze your CloudTrail logs interactively?  
    A. AWS Athena  
    B. Amazon QuickSight  
    C. AWS Glue  
    D. AWS Lambda  

11. To capture API activity for global services like IAM, you must enable...  
    A. Global service events  
    B. S3 object events  
    C. Lambda invocation events  
    D. EC2 instance events  

12. Which CloudTrail feature lets you store full event logs for compliance and auditing?  
    A. Event History  
    B. Trails with S3 integration  
    C. Console snapshot  
    D. CloudTrail Lake  

13. How do you encrypt CloudTrail logs at rest in S3?  
    A. Use SSE-S3 by default  
    B. Enable SSE-KMS with a customer-managed key  
    C. TLS encryption  
    D. JSON encryption  

14. What is the default log file format delivered by CloudTrail?  
    A. CSV  
    B. JSON  
    C. XML  
    D. Parquet  

15. CloudTrail Lake allows you to define...  
    A. SQL queries over event data  
    B. Real-time metrics dashboards  
    C. Automatic remediation runbooks  
    D. IAM policies  

16. When enabling a new trail, enabling “Apply trail to all regions” ensures what?  
    A. Logs only the current region  
    B. Logs across all existing and future regions  
    C. Logs only when a region is specified  
    D. Logs only global services  

17. CloudTrail can log management events for which of the following?  
    A. S3 bucket object uploads  
    B. IAM user creation  
    C. Lambda function payloads  
    D. DynamoDB Table scans  

18. What AWS CLI command lists all CloudTrail trails in your account?  
    A. `aws cloudtrail describe-trails`  
    B. `aws ct list-trails`  
    C. `aws trail list`  
    D. `aws cloudtrail list-event-history`  

19. To forward CloudTrail logs to CloudWatch Logs, you must...  
    A. Create a CloudWatch Logs subscription filter  
    B. Enable CloudWatch Logs integration in Trail settings  
    C. Use AWS Config  
    D. Use CloudTrail Lake  

20. CloudTrail Insights events are charged per...  
    A. Trail  
    B. Event analyzed  
    C. Region enabled  
    D. 100,000 events  

21. Which type of event would you enable to log AWS Lambda function invocations?  
    A. Management events  
    B. Data events  
    C. Insights events  
    D. Home events  

22. What is the maximum retention period you can set for Athena queries on CloudTrail logs?  
    A. 90 days  
    B. 1 year  
    C. AWS Athena does not set retention; S3 lifecycle policies apply  
    D. 7 days  

23. How can you restrict who has permission to create or modify trails?  
    A. S3 bucket policies  
    B. IAM service control policies or IAM policies on CloudTrail actions  
    C. VPC endpoint policies  
    D. Security group rules  

24. Which of the following events does AWS CloudTrail NOT record by default?  
    A. Amazon S3 object-level API calls  
    B. IAM role creation  
    C. EC2 instance launch  
    D. VPC configuration changes  

25. How do you disable logging of read-only management events in CloudTrail?  
    A. Deselect management Event type “Read” in the trail settings  
    B. Disable the trail  
    C. Delete the S3 bucket  
    D. Turn off CloudTrail  

26. What CloudTrail setting helps capture changes to IAM policies?  
    A. Data events  
    B. Management events – Write events  
    C. Insights events  
    D. Log file validation  

27. Which of the following can be a CloudTrail log file prefix?  
    A. `AWSLogs/<AWSAccountID>/CloudTrail/`  
    B. `cloudtrail-logs/` only  
    C. `/var/log/cloudtrail/`  
    D. `arn:aws:cloudtrail:*:*:`  

28. What AWS service can you integrate with CloudTrail to automatically remediate non-compliant actions?  
    A. AWS Config with Config Rules and EventBridge  
    B. AWS Shield  
    C. Amazon Macie  
    D. CloudFront  

29. How are CloudTrail log files named by default?  
    A. Random UUIDs  
    B. Using date and hour prefix in S3 object key  
    C. Incremental numeric sequence  
    D. Using service name only  

30. When you delete a trail, what happens to the existing log files in S3?  
    A. They are deleted immediately  
    B. They remain in the S3 bucket  
    C. They are moved to Glacier  
    D. CloudTrail re-enables the trail  

---

## Answers

1. B  
2. B  
3. A  
4. C  
5. C  
6. B  
7. B  
8. B  
9. B  
10. A  
11. A  
12. B  
13. B  
14. B  
15. A  
16. B  
17. B  
18. A  
19. B  
20. B  
21. B  
22. C  
23. B  
24. A  
25. A  
26. B  
27. A  
28. A  
29. B  
30. B  
