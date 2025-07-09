# 20 Amazon MQ Multiple-Choice Questions

1. Which broker engines are supported by Amazon MQ?  
   - A. Apache ActiveMQ and RabbitMQ  
   - B. Apache Kafka and RabbitMQ  
   - C. Amazon SQS and Amazon SNS  
   - D. Apache Pulsar and Amazon Kinesis  

2. What deployment mode provides automatic failover across Availability Zones?  
   - A. Single-instance  
   - B. Active/Standby Multi-AZ  
   - C. Clustered brokers  
   - D. On-premises gateway  

3. Which protocol is NOT natively supported by Amazon MQ?  
   - A. MQTT  
   - B. AMQP  
   - C. STOMP  
   - D. HTTP/2  

4. For persistent messaging durability, Amazon MQ stores data on:  
   - A. Amazon DynamoDB  
   - B. Amazon EBS or Amazon EFS  
   - C. Amazon S3  
   - D. Local instance store  

5. Which AWS feature encrypts messages at rest in Amazon MQ?  
   - A. AWS Shield  
   - B. AWS KMS customer-managed CMKs  
   - C. AWS WAF  
   - D. AWS IAM  

6. To limit network access to your broker, you would configure:  
   - A. Security Groups and VPC subnets  
   - B. Public IP addressing  
   - C. Internet Gateway rules  
   - D. CloudFront distributions  

7. Which CloudWatch metric indicates the number of messages waiting in a queue?  
   - A. ActiveConsumers  
   - B. EnqueueCount  
   - C. QueueDepth  
   - D. PublishLatency  

8. Scaling a broker vertically involves changing its:  
   - A. Storage type  
   - B. Instance type (host instance)  
   - C. Number of queues  
   - D. Protocol settings  

9. Which CLI command creates a new Amazon MQ broker?  
   - A. `aws mq create-broker`  
   - B. `aws mq launch-broker`  
   - C. `aws mq init-broker`  
   - D. `aws mq start-broker`  

10. How do you rotate the user credentials for an Amazon MQ broker?  
    - A. Modify the broker’s Users property via CLI or console  
    - B. Restart the broker instance  
    - C. Update the IAM role attached to the broker  
    - D. Delete and recreate the broker  

11. Which pricing component is billed per GB-month for Amazon MQ?  
    - A. Broker instance hours  
    - B. Data transfer  
    - C. Persistent storage usage  
    - D. Number of connections  

12. High availability in RabbitMQ on Amazon MQ is achieved by:  
    - A. AMQP 1.0 clustering  
    - B. Queue mirroring across nodes  
    - C. Automatic shard splitting  
    - D. Broker federation  

13. Which IAM policy element controls who can manage Amazon MQ resources?  
    - A. Action: “mq:*”  
    - B. Resource: “arn:aws:sqs:*”  
    - C. Service: “mq.amazonaws.com”  
    - D. Condition: “StringEquals”: { “mq:EngineType”: “ActiveMQ” }  

14. Amazon MQ integrates with which service for event-driven workflows?  
    - A. AWS Batch  
    - B. AWS Step Functions  
    - C. Amazon RDS  
    - D. Amazon EKS  

15. Which deployment option allows you to manage RabbitMQ plugins?  
    - A. ActiveMQ engine only  
    - B. RabbitMQ engine  
    - C. Both engines support plugins equally  
    - D. Neither engine  

16. What backup mechanism does Amazon MQ provide?  
    - A. Automated snapshots of broker storage  
    - B. Continuous replication to S3  
    - C. Manual export via CLI only  
    - D. No backup support  

17. Which metric would you monitor to detect slow message delivery?  
    - A. ConsumerLatency  
    - B. InflightCount  
    - C. PublishCount  
    - D. ConnectCount  

18. To connect an on-premises application securely to Amazon MQ, you would use:  
    - A. Internet Gateway  
    - B. VPC peering  
    - C. AWS Direct Connect or VPN  
    - D. NAT Gateway  

19. Which broker property defines the engine version?  
    - A. EngineType  
    - B. EngineVersion  
    - C. HostInstanceType  
    - D. DeploymentMode  

20. Which AWS service can act as a bridge between Amazon MQ and serverless architectures?  
    - A. Amazon SQS  
    - B. AWS Lambda  
    - C. Amazon SNS  
    - D. AWS Glue  

---

## Answers

1. A  
2. B  
3. D  
4. B  
5. B  
6. A  
7. C  
8. B  
9. A  
10. A  
11. C  
12. B  
13. A  
14. B  
15. B  
16. A  
17. A  
18. C  
19. B  
20. B  
