## AWS Kinesis

### Overview  
Amazon Kinesis is a fully managed suite of services for real-time data ingestion, processing, and analysis. It enables you to capture, process, and store large streams of data—such as application logs, IoT telemetry, or clickstreams—and react to them with sub-second latency.

### Core Services  
- **Kinesis Data Streams (KDS)**  
  - Shard-based streaming with millisecond latency.  
  - Custom consumers via AWS Lambda, Java, or Apache Flink.  
- **Kinesis Data Firehose**  
  - Serverless ETL: automatically loads streaming data into S3, Redshift, Elasticsearch, or Splunk.  
  - Optional in-flight transformations with Lambda.  
- **Kinesis Data Analytics**  
  - Real-time SQL queries on Data Streams or Firehose.  
  - No cluster provisioning required.  
- **Kinesis Video Streams**  
  - Ingests, processes, and stores live video for machine learning or playback.  

### Key Features  
- **Scalability**  
  - Manual shard management in Data Streams; auto-scaling in Firehose.  
- **Low Latency**  
  - Sub-second record retrieval and processing.  
- **Transformations**  
  - In-flight data transformation via Lambda in Firehose.  
- **Integration**  
  - Native connectors to Lambda, SDKs (Java, Python, Node.js), Flink, CloudWatch, CloudTrail.  
- **SQL Analytics**  
  - Continuous queries without managing infrastructure.

### Common Use Cases  
- **Application Monitoring**: ingest logs & metrics for real-time alerting.  
- **IoT Telemetry**: collect sensor data and trigger actions instantly.  
- **Clickstream Analytics**: process user interactions to drive personalization.  
- **Video Analytics**: stream camera feeds for object detection or facial recognition.

### Pricing Model  
- **Data Streams**  
  - Charged per shard-hour and per million PUT payload units.  
- **Firehose**  
  - Charged per GB delivered and per GB of data transformation.  
- **Data Analytics**  
  - Charged per hour of streaming unit (SU) usage.  
- **Video Streams**  
  - Charged per hour of video ingested and per GB stored.

### Security & Compliance  
- **Encryption**  
  - At-rest with AWS KMS; in-transit with TLS.  
- **Access Control**  
  - IAM roles and policies for producers, consumers, and administrators.  
- **Private Connectivity**  
  - VPC Endpoints (AWS PrivateLink) to keep traffic off the public Internet.  
- **Audit**  
  - CloudTrail logs all control-plane API calls.

### Integrations  
- **AWS Lambda**: event-driven consumers or transformers.  
- **Apache Flink**: stateful stream processing with Kinesis Data Analytics.  
- **S3 / Redshift / Elasticsearch / Splunk**: Firehose delivery targets.  
- **CloudWatch**: metrics, dashboards, and alarms.

### Example: Create a Data Stream with AWS CLI  
```bash
aws kinesis create-stream \
  --stream-name MyEventStream \
  --shard-count 2 \
  --region us-east-1
