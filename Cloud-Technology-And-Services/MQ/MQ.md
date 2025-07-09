## Amazon MQ

### Overview  
Amazon MQ is a managed message broker service for Apache ActiveMQ and RabbitMQ that makes it easy to set up and operate message brokers in the cloud. It handles provisioning, patching, failure detection and recovery, and provides highly available, secure, and durable messaging.

### Key Features  
- **Managed Brokers**  
  - Choose between Apache ActiveMQ or RabbitMQ engines.  
  - Fully managed provisioning, software patching, and broker maintenance.  
- **Multi-AZ High Availability**  
  - Brokers deployed across Availability Zones with automated failover.  
- **Standard Protocol Support**  
  - JMS, AMQP, MQTT, STOMP, WSS, WebSocket and NMS for broad client compatibility.  
- **Durable Storage**  
  - Persistent queues and topics backed by Amazon EFS or EBS for durability.  
- **Automatic Scaling**  
  - Scale broker instance types up or down; support for Amazon MQ for RabbitMQ horizontal clustering.  
- **Monitoring & Metrics**  
  - Native CloudWatch metrics and integration with Amazon EventBridge for alerts.  
- **Encryption & Security**  
  - TLS for in-transit encryption; encryption at rest using AWS KMS keys.  
  - Fine-grained IAM policies and VPC support for network isolation.

### Common Use Cases  
- Decoupling microservices with reliable asynchronous messaging  
- Event-driven architectures and streaming data ingestion  
- Legacy JMS applications lift-and-shift to AWS without code changes  
- IoT device messaging with MQTT support  
- Cross-language interoperability between Java, .NET, Python, JavaScript, etc.

### Pricing Model  
- **Broker Instance Hours**  
  - Charged per hour per broker instance (MQ.T3.Medium up to MQ.M5.Large, etc.).  
- **Storage**  
  - Persistent storage billed per GB-month used by brokers.  
- **Data Transfer**  
  - Standard AWS data-transfer charges for traffic leaving the VPC (in-VPC traffic is free).  
- **No Upfront Fees**  
  - Pay-as-you-go with no minimum commitments.

### Security & Compliance  
- **Encryption**  
  - In-transit: TLS 1.2/1.3 for all broker endpoints.  
  - At-rest: AWS KMS customer-managed CMKs.  
- **Access Control**  
  - Broker user/password credentials, LDAP or Active Directory integration, and IAM policies.  
- **Network Isolation**  
  - Launch brokers in a customer VPC, control access with Security Groups and NACLs.  
- **Audit & Logging**  
  - CloudWatch Logs capture broker logs; EventBridge for operational events.  
- **Certifications**  
  - Compliance with PCI DSS, ISO, SOC, HIPAA, GDPR, and FedRAMP standards.

### Integrations  
- **AWS Lambda**: Trigger functions in response to messages.  
- **Amazon SQS**: Bridge between MQ and SQS queues.  
- **AWS Step Functions**: Orchestrate workflows based on message events.  
- **Amazon Kinesis Data Streams**: Stream processing pipelines.  
- **Amazon CloudWatch & EventBridge**: Monitoring, metrics, and automated alerts.

### Example: Create a Broker via AWS CLI  
```bash
aws mq create-broker \
  --broker-name MyActiveMQBroker \
  --engine-type ACTIVEMQ \
  --engine-version 5.15.14 \
  --deployment-mode ACTIVE_STANDBY_MULTI_AZ \
  --host-instance-type mq.t3.medium \
  --publicly-accessible \
  --users Username=appUser,Password='ChangeMe123!' \
  --encryption-options UseAwsOwnedKey=true \
  --auto-minor-version-upgrade \
  --region us-east-1
