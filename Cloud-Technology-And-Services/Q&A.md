# 20 Questions on AWS CodeGuru, Global Accelerator, Health Dashboard, and Wavelength

## AWS CodeGuru

1. Which component of AWS CodeGuru reviews pull requests to suggest security and code quality improvements?  
   - A. Profiler  
   - B. Reviewer  
   - C. Security Hub  
   - D. Inspector  

2. Which of the following analyzes your production application's performance by identifying CPU hotspots?  
   - A. AWS X-Ray  
   - B. CodeGuru Profiler  
   - C. CloudWatch  
   - D. CodeBuild  

3. Which recommendation might CodeGuru Reviewer offer in Java to avoid resource leaks?  
   - A. Use `System.exit()`  
   - B. Use `try-with-resources`  
   - C. Disable the Garbage Collector  
   - D. Increase the heap size  

4. To analyze your AWS CodeCommit repository with CodeGuru Reviewer, you must:  
   - A. Install an agent on your EC2 instances  
   - B. Create an application in AWS Elastic Beanstalk  
   - C. Enable the CodeGuru integration on your repository  
   - D. Configure a CloudFormation stack  

5. CodeGuru Profiler estimates cost savings by optimizing inefficient code based on:  
   - A. Execution hours and CPU usage  
   - B. Number of lines of code  
   - C. Number of commits  
   - D. Binary size  

## AWS Global Accelerator

6. AWS Global Accelerator assigns static anycast IPs that:  
   - A. Change with each deployment  
   - B. Are different per region  
   - C. Are global and fixed  
   - D. Only work with IPv6  

7. Which of the following is **not** a valid Global Accelerator endpoint?  
   - A. Application Load Balancer  
   - B. Network Load Balancer  
   - C. EC2 instance  
   - D. Amazon S3 bucket  

8. How does Global Accelerator control traffic distribution among multiple endpoints?  
   - A. IAM policies  
   - B. Weights assigned to each endpoint  
   - C. Route 53 rules  
   - D. Tags  

9. If an endpoint becomes unhealthy, Global Accelerator:  
   - A. Leaves it unhealthy until you manually mark it as healthy  
   - B. Automatically reroutes traffic to the next best path  
   - C. Removes the endpoint from your VPC  
   - D. Restarts the affected EC2 instance  

10. Which of these is **not** a key benefit of Global Accelerator?  
    - A. Reduced latency over the AWS network  
    - B. Automatic failover across regions  
    - C. Static global IPs  
    - D. Edge object caching  

## AWS Health Dashboard

11. The Service Health Dashboard (SHD) displays:  
    - A. Events for your specific account  
    - B. Global status of AWS services by region  
    - C. EC2 performance metrics  
    - D. Security analysis results  

12. The Personal Health Dashboard (PHD) provides:  
    - A. CloudTrail logs  
    - B. Events specific to your accounts and resources  
    - C. Billing reports  
    - D. RDS metrics  

13. Which AWS CLI command returns a list of open or upcoming health events?  
    - A. `aws health describe-events`  
    - B. `aws health list-dashboard`  
    - C. `aws health get-service-status`  
    - D. `aws health show-events`  

14. To forward PHD events to an SNS topic, you typically use:  
    - A. CloudWatch Alarms  
    - B. EventBridge Rule  
    - C. AWS Step Functions  
    - D. S3 Event Notifications  

15. Which of these is **not** an event type in AWS Health Dashboard?  
    - A. UpcomingMaintenance  
    - B. IssueDetected  
    - C. PerformanceRecommendation  
    - D. AccountNotification  

## AWS Wavelength

16. AWS Wavelength brings AWS compute resources closer to the:  
    - A. Local data center  
    - B. 4G network edge  
    - C. 5G network edge  
    - D. Public internet  

17. The specialized zones in AWS Wavelength are called:  
    - A. Edge Zones  
    - B. Wavelength Zones  
    - C. Local Zones  
    - D. Transit Zones  

18. Which of these services **cannot** be launched in a Wavelength Zone?  
    - A. EC2 instance  
    - B. ECS task  
    - C. Lambda function  
    - D. Amazon RDS  

19. The typical latency goal of AWS Wavelength is:  
    - A. < 1 ms  
    - B. < 10 ms  
    - C. 50–100 ms  
    - D. > 200 ms  

20. Which feature allows serverless code to run directly on the 5G network with Wavelength?  
    - A. AWS Lambda@Edge  
    - B. AWS Fargate  
    - C. AWS Batch  
    - D. AWS Glue  

---

## Answers

1. B  
2. B  
3. B  
4. C  
5. A  
6. C  
7. D  
8. B  
9. B  
10. D  
11. B  
12. B  
13. A  
14. B  
15. C  
16. C  
17. B  
18. D  
19. B  
20. A  
