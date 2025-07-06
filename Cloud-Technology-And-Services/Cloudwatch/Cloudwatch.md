# AWS CloudWatch

## 1. What Is AWS CloudWatch?  
Amazon CloudWatch is a fully managed monitoring and observability service that provides data and actionable insights for AWS, hybrid, and on-premises applications and infrastructure. It collects and visualizes metrics, logs, and events in real time, enabling you to detect anomalies, set alarms, and automate responses.

---

## 2. Key Components

- **Metrics**  
  Time-series data about resource utilization, application performance, and operational health (CPU, memory, disk I/O, custom business metrics).

- **Alarms**  
  Threshold-based evaluations on metrics that can trigger notifications (SNS), auto-scaling actions, or custom responses via EventBridge.

- **Logs**  
  Centralized log ingestion, storage, and querying (Linux/Windows agent, Lambda, VPC Flow Logs). Supports CloudWatch Logs Insights for ad-hoc queries.

- **Dashboards**  
  Customizable, shareable visualizations of metrics and alarms in a single pane of glass.

- **Events / EventBridge**  
  Near real-time event bus for AWS service events and custom application events. Can route to Lambda, SQS, SNS, Step Functions, etc.

- **Contributor Insights**  
  Analyzes log and metric patterns to surface top contributors (e.g., highest error rates, busiest hosts).

- **Synthetics**  
  Canary scripts that run on a schedule to monitor application endpoints, APIs, and workflows.

- **CloudWatch Agent & Container Insights**  
  Unified agent for advanced OS metrics and custom logs; Container Insights for ECS/EKS monitoring.

---

## 3. Core Features

- **Real-Time Monitoring**  
  One-second granularity for many AWS services; default five-minute granularity for others.

- **Automated Actions**  
  Auto-scale EC2, ECS, and DynamoDB; trigger remediation playbooks via EventBridge and Systems Manager.

- **Anomaly Detection**  
  Built-in ML models that automatically set dynamic thresholds on metrics.

- **Log Retention & Archival**  
  Define retention policies per log group; archive older logs to S3 or expire them automatically.

- **Cross-Account & Cross-Region Dashboards**  
  Aggregate data from multiple accounts and regions into a unified view.

---

## 4. Integrations

- **AWS Services**  
  Native integration with EC2, ECS, EKS, Lambda, RDS, DynamoDB, VPC Flow Logs, API Gateway, Step Functions, and more.

- **Custom Applications**  
  Publish custom metrics via PutMetricData API or StatsD/prometheus agents.

- **Third-Party Systems**  
  Ingest metrics and logs from on-premises servers or other clouds using the CloudWatch Agent or API.

- **Notification & Automation**  
  SNS for alerts; EventBridge for workflow automation; Systems Manager for automated remediation.

---

## 5. Common Use Cases

- **Infrastructure Monitoring**  
  Track resource utilization, detect under- or over-provisioning, and optimize costs.

- **Application Performance**  
  Monitor latency, error rates, request counts; set alarms on service-level objectives (SLOs).

- **Security & Compliance**  
  Alert on unusual API calls, unauthorized access patterns, or configuration changes.

- **Operational Troubleshooting**  
  Query logs with Logs Insights to pinpoint root causes of incidents.

- **Synthetic Testing**  
  Use canaries to validate endpoint availability and performance from multiple geographies.

---

## 6. Benefits

- **Unified Observability**  
  Metrics, logs, events, and traces (when integrated with X-Ray) in one platform.

- **Scalable & Serverless**  
  Automatically scales to ingest millions of metrics and terabytes of logs without you managing servers.

- **Pay-As-You-Go**  
  No upfront costs; pay only for metrics, logs ingestion/storage, alarms, dashboards, and Synthetics run.

- **Built-In Security**  
  Encryption at rest (SSE-KMS), IAM-based access control, and VPC endpoint support.

---

## 7. Pricing Model

- **Metrics**  
  Standard metrics: \$0.30 per metric per month; custom metrics: \$0.30 each.

- **Alarms**  
  \$0.10 per alarm per month.

- **Logs Ingestion & Storage**  
  \$0.50 per GB ingested; \$0.03 per GB-month stored (first 5 GB ingested free).

- **Dashboards**  
  \$3.00 per dashboard per month.

- **Events / EventBridge**  
  \$1.00 per million events published or matched.

- **CloudWatch Synthetics**  
  \$0.10 per canary run and compute time.

---

## 8. Best Practices

1. **Optimize Metric Granularity**  
   Use high-resolution (1s) metrics only where needed to control costs.

2. **Use Namespaces & Dimensions**  
   Organize custom metrics with clear namespaces and dimensions for filtering.

3. **Implement Retention Policies**  
   Automatically expire or archive old log data to S3 to manage storage costs.

4. **Leverage Dashboards & Contributor Insights**  
   Build operational dashboards and identify top contributors to performance issues.

5. **Automate Remediation**  
   Combine Alarms, EventBridge, and Systems Manager to automatically resolve known issues.

6. **Secure Access**  
   Restrict write permissions to metrics and logs; use IAM roles and encryption keys.

7. **Correlate with Tracing**  
   Integrate with AWS X-Ray for end-to-end trace-level visibility alongside CloudWatch metrics and logs.
