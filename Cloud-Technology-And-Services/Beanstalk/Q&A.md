# Quiz: AWS Elastic Beanstalk (30 Questions)

1. What command initializes your local repository for usage with Elastic Beanstalk?  
   A. `eb start`  
   B. `eb init`  
   C. `eb configure`  
   D. `eb setup`  

2. Which file do you use to define instance-level configuration and package installation in Beanstalk?  
   A. `Dockerrun.aws.json`  
   B. `.platform/hooks/prebuild`  
   C. `.ebextensions/*.config`  
   D. `ElasticBeanstalk.config`  

3. What deployment policy creates a parallel environment before swapping CNAMEs?  
   A. Rolling  
   B. Immutable  
   C. Blue/Green  
   D. All at once  

4. How do you deploy a new application version with the EB CLI?  
   A. `eb push`  
   B. `eb build`  
   C. `eb deploy`  
   D. `eb release`  

5. Which load balancer type does Elastic Beanstalk support by default for web environments?  
   A. Network Load Balancer  
   B. Application Load Balancer  
   C. Classic Load Balancer  
   D. Gateway Load Balancer  

6. Where are application versions stored by Elastic Beanstalk?  
   A. DynamoDB  
   B. S3  
   C. ECR  
   D. EFS  

7. Which setting controls the minimum and maximum number of EC2 instances in an Elastic Beanstalk environment?  
   A. `InstanceCount`  
   B. `MinSize` and `MaxSize` in the Auto Scaling group  
   C. `DesiredCapacity` only  
   D. `ReplicaCount`  

8. What is the default health check path for an Elastic Beanstalk web environment?  
   A. `/`  
   B. `/health`  
   C. `/status`  
   D. `/eb-health`  

9. How can you customize the AMI used by your Elastic Beanstalk environment?  
   A. Use `.ebextensions` to specify `aws:autoscaling:launchconfiguration` AMI ID  
   B. You cannot customize the AMI  
   C. Specify in `Dockerrun.aws.json`  
   D. Set in the AWS CLI with `--ami` flag  

10. Which Elastic Beanstalk environment type requires a Dockerfile?  
    A. Multicontainer (ECS)  
    B. Single Container Docker  
    C. Preconfigured Platform  
    D. Worker Environment  

11. What environment tier would you choose for background processing jobs?  
    A. Web Server Tier  
    B. Worker Tier  
    C. Single Container Tier  
    D. Multicontainer Tier  

12. Which EB CLI command lists your existing Beanstalk environments?  
    A. `eb list`  
    B. `eb status`  
    C. `eb environments`  
    D. `eb show`  

13. How do you enable enhanced health reporting in Elastic Beanstalk?  
    A. In `.ebextensions`, set `HealthReporting: enhanced`  
    B. Via the console or `eb health --enhanced`  
    C. It’s enabled by default  
    D. By installing the CloudWatch agent manually  

14. Which file defines environment variables for your application?  
    A. `.env` at project root  
    B. `config.yml` in `.platform`  
    C. Elastic Beanstalk console or `eb setenv`  
    D. `environment.json`  

15. What happens when you terminate an Elastic Beanstalk environment?  
    A. EC2 instances are preserved  
    B. S3 application versions are deleted  
    C. All AWS resources created by that environment are deleted  
    D. RDS instances are always retained  

16. Which feature lets you perform zero-downtime deployments in Beanstalk?  
    A. All at once  
    B. Rolling with additional batch  
    C. Immutable deployments  
    D. Rolling deployments  

17. How can you rollback to a previous application version?  
    A. Use `eb rollback`  
    B. Deploy the desired version from the console or `eb deploy --version LABEL`  
    C. Edit Auto Scaling group to use older instance AMI  
    D. Use AWS CLI S3 delete  

18. What AWS service integrates to run cron-like jobs in a Worker Tier environment?  
    A. CloudWatch Events → SQS → Worker  
    B. Lambda scheduled events  
    C. Step Functions  
    D. CodePipeline  

19. Which platform branch would you select to get the latest updates of a language runtime?  
    A. A stable branch name like `Node.js 14 running on 64bit Amazon Linux 2`  
    B. A custom Docker platform  
    C. `Latest` alias  
    D. Multi-container platform  

20. How do you tail logs from your Elastic Beanstalk instances using the EB CLI?  
    A. `eb tail`  
    B. `eb logs --stream`  
    C. `eb logs --follow`  
    D. `eb show-logs`  

21. Which resource policy ensures your environment’s S3 bucket logs are encrypted?  
    A. Bucket lifecycle policy  
    B. Bucket encryption configuration  
    C. IAM role on EC2 instance  
    D. Auto Scaling policy  

22. What is the purpose of the `.platform` directory in a Beanstalk application?  
    A. Define Docker Compose files  
    B. Store application source code  
    C. Provide custom platform hooks and extensions  
    D. Override security group settings  

23. Which CloudFormation resource type is used to define an Elastic Beanstalk Environment?  
    A. `AWS::ElasticBeanstalk::Application`  
    B. `AWS::ElasticBeanstalk::Environment`  
    C. `AWS::ECS::Service`  
    D. `AWS::CloudFormation::Stack`  

24. How do you configure a managed RDS database to be created with your Beanstalk environment?  
    A. Via `.ebextensions` with `AWS::RDS::DBInstance`  
    B. Use RDS console separately  
    C. Enable “Create a new RDS database” option in environment settings  
    D. It’s not supported  

25. Which command updates environment configuration without deploying new code?  
    A. `eb config`  
    B. `eb deploy`  
    C. `eb config save`  
    D. `eb update-config`  

26. How can you apply platform-level customizations before the application deploys?  
    A. `.ebextensions` only  
    B. `.platform/hooks/prebuild` and other lifecycle hooks  
    C. Editing the source bundle directly  
    D. Using AWS Systems Manager  

27. What is the default instance type for a new web environment if not specified?  
    A. t2.micro  
    B. t3.small  
    C. t3.micro  
    D. m5.large  

28. Which metric would you monitor to decide if you need more instances?  
    A. Application CPU utilization  
    B. S3 bucket size  
    C. RDS connections  
    D. DynamoDB read capacity  

29. How do you swap the CNAMEs of two Beanstalk environments?  
    A. `eb swap`  
    B. `eb switch`  
    C. `eb cnam`  
    D. `eb swap-environment-cnames`  

30. Which option lets you keep your RDS database when terminating the environment?  
    A. Enable “Retain DB on Termination” in environment settings  
    B. Use `eb terminate --keep-db`  
    C. Move DB to a different environment first  
    D. Not possible  

---

## Answers

1. B. `eb init`  
2. C. `.ebextensions/*.config`  
3. C. Blue/Green  
4. C. `eb deploy`  
5. C. Classic Load Balancer  
6. B. S3  
7. B. `MinSize` and `MaxSize` in the Auto Scaling group  
8. A. `/`  
9. A. Use `.ebextensions` to specify `aws:autoscaling:launchconfiguration` AMI ID  
10. B. Single Container Docker  
11. B. Worker Tier  
12. A. `eb list`  
13. B. Via the console or `eb health --enhanced`  
14. C. Elastic Beanstalk console or `eb setenv`  
15. C. All AWS resources created by that environment are deleted  
16. C. Immutable deployments  
17. B. Deploy the desired version from the console or `eb deploy --version LABEL`  
18. A. CloudWatch Events → SQS → Worker  
19. A. A stable branch name like `Node.js 14 running on 64bit Amazon Linux 2`  
20. B. `eb logs --stream`  
21. B. Bucket encryption configuration  
22. C. Provide custom platform hooks and extensions  
23. B. `AWS::ElasticBeanstalk::Environment`  
24. C. Enable “Create a new RDS database” option in environment settings  
25. A. `eb config`  
26. B. `.platform/hooks/prebuild` and other lifecycle hooks  
27. A. t2.micro  
28. A. Application CPU utilization  
29. D. `eb swap-environment-cnames`  
30. A. Enable “Retain DB on Termination” in environment settings  
