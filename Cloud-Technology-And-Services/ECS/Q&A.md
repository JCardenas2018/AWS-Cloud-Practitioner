# Quiz: AWS ECS Cost Optimization (30 Questions)

1. What is the most cost-effective way to run non-critical batch tasks in ECS?  
   A. Fargate On-Demand  
   B. Fargate Spot  
   C. EC2 On-Demand  
   D. EC2 Reserved Instances  

2. In Fargate, why can using Savings Plans reduce costs?  
   A. Because they guarantee dedicated instances  
   B. Because they apply discounts for committed usage  
   C. Because they allow automatic Spot execution  
   D. Because they eliminate memory charges  

3. For a stable service with high continuous utilization, which EC2 model do you recommend to optimize costs?  
   A. On-Demand  
   B. Spot  
   C. Reserved Instances  
   D. Savings Plans  

4. What approximate discount rate does Fargate Spot offer compared to On-Demand?  
   A. 10–20%  
   B. 30–40%  
   C. 50–60%  
   D. Up to 70%  

5. When scheduling scaling down tasks in dev/test outside business hours, which AWS service would you use to trigger those actions?  
   A. SNS  
   B. CloudWatch Logs  
   C. EventBridge (CloudWatch Events)  
   D. Systems Manager  

6. For a job with 2 vCPU and 4 GB RAM that runs 30 minutes daily, what approximate monthly cost would it have on Fargate On-Demand (0.04048 USD/vCPU-hr and 0.004445 USD/GB-hr)?  
   A. ~0.12 USD/month  
   B. ~1.80 USD/month  
   C. ~3.60 USD/month  
   D. ~7.20 USD/month  

7. Which of these EC2 placement strategies aims to maximize instance utilization?  
   A. spread  
   B. random  
   C. binpack  
   D. none  

8. Which practice helps reduce ECR image storage costs?  
   A. Disable vulnerability scanning  
   B. Keep only “latest” tags  
   C. Remove old images with lifecycle policies  
   D. Increase repository size  

9. If you have a critical web service with 3 tasks of 1 vCPU + 2 GB, what approximate monthly cost does it represent on Fargate Spot (0.0124419 USD/vCPU-hr, 0.00136621 USD/GB-hr) running 24×7?  
   A. ~27 USD  
   B. ~54 USD  
   C. ~81 USD  
   D. ~108 USD  

10. Which combination of models offers the greatest cost flexibility for variable workloads?  
    A. Only EC2 On-Demand  
    B. Only Fargate On-Demand  
    C. EC2 Reserved + EC2 Spot  
    D. EC2 On-Demand + Fargate Spot  

11. What is the main benefit of using Fargate instead of EC2 for sporadic services?  
    A. Discounts for commitment  
    B. No server management  
    C. Higher CPU performance  
    D. Free block storage  

12. Which metric do you recommend monitoring to right-size CPU/memory in Task Definitions?  
    A. Network latency  
    B. CPU and memory utilization  
    C. Number of HTTP requests  
    D. Log duration  

13. For interruption-tolerant batch workloads, what Spot priority level is appropriate?  
    A. High priority  
    B. Low priority  
    C. Critical  
    D. Immediate  

14. When using Compute Savings Plans in Fargate, you must commit to:  
    A. A fixed number of simultaneous tasks  
    B. A level of vCPU and GB-hours per month  
    C. A group of specific EC2 instances  
    D. A variable Spot period  

15. Which of these activities reduces network traffic costs the most?  
    A. Compress containers  
    B. Use VPC endpoints for S3  
    C. Increase number of tasks  
    D. Use larger images  

16. How can you automate time-based scaling to reduce nighttime costs?  
    A. Scheduling AWS Config  
    B. Using Scheduled Scaling in Application Auto Scaling  
    C. Manual scaling  
    D. Changing the Task Definition daily  

17. In a multi-AZ environment, which configuration minimizes risk and controls costs?  
    A. Deploy all tasks in one AZ  
    B. Distribute tasks across each AZ using Fargate  
    C. Use EC2 Spot in one AZ and On-Demand in another  
    D. Run tasks only in the cheapest AZ  

18. For stable, critical workloads, which mix of EC2 instances do you recommend?  
    A. 100% Spot  
    B. 100% On-Demand  
    C. On-Demand + Reserved Instances  
    D. Spot + Savings Plans  

19. What is one way to ensure idle tasks do not consume resources?  
    A. Keep the desired count high  
    B. Use Health Checks  
    C. Run tasks on Spot  
    D. Manually shut down the cluster  

20. What approximate savings do you achieve with 1-year Reserved Instances versus On-Demand?  
    A. 0%  
    B. 10–15%  
    C. 25–30%  
    D. 50–60%  

21. Which service allows you to store and rotate secrets with no additional cost to ECS?  
    A. S3  
    B. DynamoDB  
    C. AWS Secrets Manager  
    D. Systems Manager Parameter Store  

22. For development environments, which practice saves the most?  
    A. Run on Fargate Spot  
    B. Keep the cluster running continuously  
    C. Turn off the cluster off-hours with Lambda + EventBridge  
    D. Increase desired count  

23. What type of auto scaling does Fargate natively use?  
    A. Cluster auto scaling  
    B. Service auto scaling with Target Tracking  
    C. Manual scaling on EC2  
    D. Log-based scaling  

24. How do you reduce EBS snapshot costs for volumes used by ECS?  
    A. Increase snapshot frequency  
    B. Use snapshot lifecycle policies  
    C. Keep all snapshots indefinitely  
    D. Disable snapshots  

25. What discount do you typically get with Savings Plans versus On-Demand?  
    A. 5–10%  
    B. 10–20%  
    C. 20–30%  
    D. 40–50%  

26. A strategy to reduce centralized logging costs is:  
    A. Increase logging level to DEBUG  
    B. Filter and batch logs before sending  
    C. Send uncompressed logs  
    D. Multiply log streams  

27. For stateful workloads on ECS, which option can increase costs but provide durability?  
    A. Mount Amazon EFS per task  
    B. Use only environment variables  
    C. Store data in ephemeral containers  
    D. Keep data in container memory  

28. In a “Spot + On-Demand mixed” pattern, what do you use Spot for?  
    A. Critical workloads  
    B. Batch and non-critical processing  
    C. Databases  
    D. ECS control plane  

29. Which IaC component facilitates auditing and rollback of ECS configurations?  
    A. AWS CLI  
    B. Terraform or CloudFormation  
    C. ECS Console  
    D. Ad-hoc bash scripts  

30. Which metric should you monitor to avoid memory overprovisioning?  
    A. Network latency  
    B. Container memory usage  
    C. Number of tasks  
    D. Log count  

---

## Answers

1. B  
2. B  
3. C  
4. D  
5. C  
6. B  
7. C  
8. C  
9. A  
10. D  
11. B  
12. B  
13. B  
14. B  
15. B  
16. B  
17. B  
18. C  
19. B  
20. C  
21. D  
22. C  
23. B  
24. B  
25. C  
26. B  
27. A  
28. B  
29. B  
30. B  
