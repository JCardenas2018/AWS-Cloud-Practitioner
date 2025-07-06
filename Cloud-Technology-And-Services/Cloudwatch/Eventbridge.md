````markdown
# AWS EventBridge

## 1. What Is Amazon EventBridge?  
Amazon EventBridge is a serverless event bus service that makes it easy to connect applications using data from your own applications, SaaS providers, and AWS services. EventBridge ingests events in near-real time, applies routing rules, and delivers them to targets (Lambda functions, queues, streams, etc.) without the need to manage infrastructure.

---

## 2. Core Concepts

- **Event Bus**  
  A routing layer that receives and processes events.  
  - **Default Bus**: Receives events from most AWS services.  
  - **Custom Buses**: For your application-generated events.  
  - **Partner Buses**: Ingest events from SaaS partners (e.g., Zendesk, Datadog).

- **Event**  
  A JSON object that describes a change in state or an action.  
  ```json
  {
    "source": "aws.ec2",
    "detail-type": "EC2 Instance State-change Notification",
    "detail": { ... }
  }
````

* **Rule**
  Defines event patterns or schedules that match incoming events and routes them to one or more targets.

* **Target**
  A resource that processes the event, such as:

  * AWS Lambda
  * Amazon SQS queue
  * Amazon SNS topic
  * Step Functions state machine
  * Kinesis Data Streams
  * HTTP/S API Destination
  * Other event buses (cross-account or cross-region)

* **Schema Registry & Discovery**
  Automatically infer, catalog, and download event schemas for tighter type safety in your applications.

---

## 3. Key Features

* **Rich Event Filtering**
  Use content-based rules to match only the events you care about (by source, detail-type, or JSON fields).

* **Scheduled Events**
  Create cron-like schedules without CloudWatch Events; rules can fire on a fixed rate or cron expression.

* **Cross-Account & Cross-Region**
  Send events between AWS accounts and regions securely, enabling centralized event processing.

* **Partner Event Sources**
  Integrate with dozens of SaaS and third-party services without custom polling or webhooks.

* **Event Replay & Archiving**
  Archive events and later replay them to a bus to rehydrate systems for debugging or recovery.

* **Built-In Retries & Dead-Letter Queues**
  Automatic retries on target failures and optional dead-letter queues (DLQs) for unprocessed events.

* **API Destinations**
  Send events to any external HTTP/S endpoint with built-in authorization and rate-limiting.

---

## 4. Integrations

* **AWS Services**
  Nearly all AWS services can emit events (CloudTrail, CodePipeline, ECS, S3, RDS, etc.) and serve as targets.

* **SaaS Partners**
  Out-of-the-box connectors for services like Auth0, Datadog, PagerDuty, Shopify, and more.

* **Custom Applications**
  Put custom events with the SDK or AWS CLI (`PutEvents`), enabling loosely coupled microservices.

* **Monitoring & Security**
  Combine with CloudWatch Logs, CloudWatch Alarms, and AWS X-Ray to trace and troubleshoot event-driven flows.

---

## 5. Common Use Cases

1. **Event-Driven Microservices**
   Decouple components by publishing and subscribing to domain events (e.g., order placed, payment processed).

2. **Cloud Resource Automation**
   React to infrastructure changes (EC2 start/stop, VPC changes) to trigger automated remediations or notifications.

3. **SaaS Integration**
   Ingest events from third-party systems (like Zendesk ticket updates) and route them into your workflows.

4. **Scheduled Tasks**
   Replace cron jobs with EventBridge scheduled rules to kick off batch jobs, health checks, or data pipelines.

5. **Audit & Compliance**
   Route CloudTrail events to auditing targets (Lambda, S3) for real-time security alerts or long-term storage.

---

## 6. Benefits

* **Serverless & Scalable**
  No servers to provision; scales automatically to handle millions of events per second.

* **Low Latency**
  Delivers events in under one second for most targets.

* **Cost-Effective**
  Pay only per million events published and per million events matched by rules, with generous free tier.

* **Loose Coupling**
  Enables asynchronous, event-driven architectures that improve reliability and resilience.

* **Operational Simplicity**
  Built-in retries, dead-letter queues, and event archiving reduce custom error-handling code.

---

## 7. Pricing Model

* **Event Ingestion**
  \$1.00 per million events published to custom buses.

* **Event Matching**
  \$1.00 per million events matched by rules.

* **Schema Registry**
  Free for inference; small fee for proactive schema discovery and downloads beyond free tier.

* **API Destinations**
  Additional charges for invocation minutes and connection hours.

> *Prices may vary by region.*

---

## 8. Best Practices

1. **Design Idempotent Targets**
   Ensure your consumers can handle duplicate events gracefully.

2. **Limit Event Size**
   Keep payloads under 256 KB; use S3 for large payloads and pass references.

3. **Use Dead-Letter Queues**
   Configure DLQs on rules to capture failed deliveries for inspection.

4. **Implement Fine-Grained Filtering**
   Narrow event patterns to reduce unnecessary target invocations and cost.

5. **Archive Critical Events**
   Enable event archiving and replay for debugging and disaster recovery.

6. **Secure Cross-Account Access**
   Use resource-based policies and IAM principals to control who can put and read events.

```
```
