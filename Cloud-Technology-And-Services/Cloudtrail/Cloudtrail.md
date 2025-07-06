# AWS CloudTrail

## 1. What Is AWS CloudTrail?  
AWS CloudTrail is a fully managed service that records AWS API calls and related events for your AWS account and delivers log files to an Amazon S3 bucket. CloudTrail provides a history of activity—who made calls, from where, and when—enabling auditing, compliance validation, resource change tracking, and security analysis.

---

## 2. Key Components

- **Trails**  
  Configurations that capture events in one or more regions and deliver log files to an S3 bucket (and optionally to CloudWatch Logs or EventBridge).

- **Event History**  
  A console view of the last 90 days of API activity for your account, searchable without setting up a trail.

- **CloudTrail Insights**  
  Automated detection of unusual API usage patterns (spikes, drops) to surface potential operational issues or security threats.

- **Log Files**  
  JSON-formatted files delivered to S3, containing details such as the API caller, time, source IP, request parameters, and response elements.

- **Integration with CloudWatch & EventBridge**  
  You can monitor log streams and trigger alerts or workflows based on specific API activity.

---

## 3. Core Features

- **Multi-Region and Organization Trails**  
  Record activity across all AWS regions and all accounts in an AWS Organization with a single trail.

- **Data Events**  
  Capture high-volume data-plane operations on S3 objects and Lambda functions (e.g., GetObject, InvokeFunction).

- **Global Service Events**  
  Record control-plane operations for global services such as IAM and CloudFront.

- **Encryption**  
  Server-side encryption of log files in S3 using SSE-KMS for extra security.

- **Log File Validation**  
  Verify that log files have not been altered after delivery.

---

## 4. Integrations

- **Amazon S3**  
  Central storage for delivered CloudTrail logs.

- **Amazon CloudWatch Logs**  
  Forward events in near real-time for monitoring, alerting, and archival.

- **Amazon EventBridge**  
  Route events to Lambda, SNS, SQS, or other targets to automate responses.

- **AWS Organizations**  
  Create organization-level trails that apply to all member accounts for centralized governance.

- **AWS Config**  
  Combine with configuration snapshots to provide a complete change history.

---

## 5. Common Use Cases

- **Security Analysis & Incident Response**  
  Investigate unauthorized API calls, privilege escalations, and anomalous behavior.

- **Compliance Auditing**  
  Demonstrate to auditors that you are logging required API activity (PCI-DSS, HIPAA, GDPR).

- **Operational Troubleshooting**  
  Track configuration changes that may have led to performance issues or service interruptions.

- **Resource Change Tracking**  
  Identify who changed security groups, IAM policies, or VPC configurations and when.

- **Automated Remediation**  
  Trigger Lambda functions via EventBridge on specific API calls (e.g., disabling public S3 buckets).

---

## 6. Benefits

- **Visibility**  
  Gain detailed insight into every API call in your AWS environment.

- **Accountability**  
  Attribute actions to specific IAM users, roles, or AWS services.

- **Centralized Logging**  
  Aggregate logs from multiple regions and accounts in a single S3 bucket.

- **Low Operational Overhead**  
  Fully managed with pay-as-you-go pricing and no servers to maintain.

---

## 7. Pricing Model

- **Management Events** (create, modify, delete API calls):  
  First copy per region, per month is free; additional copies are charged per 100,000 events.

- **Data Events** (S3 object-level, Lambda invocation):  
  Charged per 100,000 events.

- **Insights Events**  
  Charged per 100,000 events analyzed.

- **Log Data Delivery**  
  Standard S3 storage and request rates apply; optional CloudWatch Logs ingestion costs.

---

## 8. Best Practices

1. **Enable Organization Trails**  
   Create a single trail that records activity across all AWS accounts and regions.

2. **Turn On Data Events Judiciously**  
   Only for critical S3 buckets or Lambda functions to control costs.

3. **Integrate with CloudWatch & EventBridge**  
   Define filters and alarms to get near real-time notifications of suspicious activity.

4. **Configure Log File Validation**  
   Ensure delivered logs cannot be tampered with.

5. **Use S3 Lifecycle Policies**  
   Archive older log files to Glacier or delete after compliance retention periods to optimize storage costs.

6. **Encrypt with KMS**  
   Protect log confidentiality by using a customer-managed KMS key.

7. **Regularly Review Event History**  
   Use the console or CloudTrail Lake to query and analyze past API activity for anomalies.
