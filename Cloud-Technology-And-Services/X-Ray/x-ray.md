## AWS X-Ray

### Overview  
AWS X-Ray is a distributed tracing service that helps you analyze and debug production and distributed applications—from simple three-tier apps to complex microservices architectures. X-Ray collects data about requests as they travel through your application, showing a map of underlying services and highlighting performance bottlenecks or errors.

### Key Features  
- **Service Map**  
  Visualizes components (services, resources) and their interactions, with latency and error rates annotated.  
- **Traces & Segments**  
  Captures detailed timing information for individual requests (“traces”), broken into segments for each service or component.  
- **Annotations & Metadata**  
  Add custom key/value data to traces for filtering and deeper analysis.  
- **Error, Fault, and Throttle Detection**  
  Flags exceptions, HTTP 5xx errors, and throttling events in your trace data.  
- **Sampling**  
  Configurable sampling rules to control the volume of trace data (fixed rate or per-service).  
- **AWS Service Integrations**  
  Out-of-the-box tracing support for API Gateway, Lambda, EC2/ECS (via the X-Ray SDK), ELB, DynamoDB, SNS, SQS, and more.  
- **Custom Instrumentation**  
  SDKs for Java, .NET, Node.js, Python, Go, and Ruby let you instrument your own code and downstream calls.  
- **Analytics & Insights**  
  Filter and group traces by annotations, view histograms of latencies, and detect anomalies.

### Common Use Cases  
- **Performance Monitoring**  
  Identify slow services, database queries, or external HTTP calls that contribute the most latency.  
- **Root Cause Analysis**  
  Trace errors back to their origin (e.g., malformed requests, downstream service failures).  
- **Microservices Observability**  
  Understand inter-service call patterns and dependencies across a distributed system.  
- **Optimization & Tuning**  
  Pinpoint hotspots and optimize code paths or resource configurations.  
- **Error and Exception Tracking**  
  Aggregate and analyze exceptions, throttles, and retries to improve reliability.

### Pricing Model  
- **Trace Scans**  
  Billed per 1,000 traces recorded and scanned.  
- **Retention**  
  Trace data retained for 30 days; you can export to S3 or CloudWatch Logs for longer-term storage (additional S3/CloudWatch fees apply).  
- **No Upfront Costs**  
  Pay-as-you-go, with free tier offering 100,000 traces per month for the first year.

### Security & Compliance  
- **Encryption**  
  Data in transit is encrypted with TLS; at-rest encryption is managed by AWS.  
- **Access Control**  
  Fine-grained IAM policies control who can send, view, or delete trace data.  
- **VPC Endpoints**  
  Private connectivity via AWS PrivateLink to keep traffic inside your VPC.  
- **Audit Logging**  
  All X-Ray API calls recorded in CloudTrail for governance.

### Integrations  
- **AWS SDKs & Instrumentation**  
  Auto-instrumentation for API Gateway and Lambda; manual SDK integration for other runtimes.  
- **Amazon CloudWatch**  
  Export trace summaries to CloudWatch Metrics and Logs for unified monitoring.  
- **AWS Distro for OpenTelemetry (ADOT)**  
  Use OpenTelemetry instrumentation and collectors with X-Ray as a backend.  
- **Third-Party Tools**  
  Integrate with Grafana, Datadog, or other observability platforms via the X-Ray API.

### Example: Instrumenting a Node.js Application  
```javascript
const AWSXRay = require('aws-xray-sdk-core');
const express = require('express');
const app = express();

// Capture all HTTP(S) calls
AWSXRay.captureHTTPsGlobal(require('http'));
AWSXRay.captureHTTPsGlobal(require('https'));

// Wrap your express app
app.use(AWSXRay.express.openSegment('MyApp'));

// Your routes...
app.get('/', (req, res) => {
  res.send('Hello from X-Ray traced app!');
});

app.use(AWSXRay.express.closeSegment());

app.listen(3000, () => console.log('Listening on port 3000'));
