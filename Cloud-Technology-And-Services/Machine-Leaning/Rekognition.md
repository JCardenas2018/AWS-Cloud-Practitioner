## Amazon Rekognition

### Overview  
Amazon Rekognition is a fully managed computer vision service that makes it easy to add image and video analysis to your applications. Rekognition uses deep learning models to detect objects, scenes, faces, text, and activities in images and videos, as well as to search and compare faces.

### Key Features  
- **Label Detection**  
  Identify thousands of objects (e.g., “Car,” “Tree”), scenes (e.g., “Beach”), and activities (e.g., “Running”).  
- **Face Detection & Analysis**  
  Detect faces in images or video frames and analyze attributes such as age range, emotion, gender, and pose.  
- **Face Search & Verification**  
  Index faces in a collection and then search or verify against that collection in real time.  
- **Celebrity Recognition**  
  Recognize thousands of well-known personalities in images and videos.  
- **Text in Image (OCR)**  
  Detect and extract printed and handwritten text from images.  
- **Content Moderation**  
  Automatically detect inappropriate or unsafe content (nudity, violence, etc.).  
- **Custom Labels**  
  Train your own image classification models on a labeled dataset to recognize domain-specific objects.

### Common Use Cases  
- **Security & Surveillance**: Real-time face search for authorized access or anomaly detection in video feeds.  
- **Media Analysis**: Tag and index large video libraries for search, highlight reels, or compliance.  
- **Customer Engagement**: Detect emotions or demographics in retail photo booths or kiosks.  
- **Document Processing**: OCR to extract text from scanned documents, receipts, or license plates.  
- **Content Moderation**: Automatically filter user-generated images and videos on social platforms.

### Pricing Model  
- **Image APIs**:  
  - Label Detection, Face Detection, Text Detection, etc.: charged per image processed.  
- **Video APIs**:  
  - Label Detection, Face Detection, Celebrity Recognition, etc.: charged per minute of video analyzed.  
- **Face Collection Storage**:  
  - Charged per thousand faces stored in collections per month.  
- **Custom Labels**:  
  - Training: charged per hour of GPU usage.  
  - Inference: charged per image processed.

_No upfront fees, pay-as-you-go based on usage._

### Security & Compliance  
- **Encryption**: All data in transit uses TLS; face collections and analysis results can be encrypted at rest with AWS KMS CMKs.  
- **Access Control**: Fine-grained IAM policies for each API operation.  
- **VPC Endpoints**: Private connectivity via AWS PrivateLink.  
- **Audit Logging**: All Rekognition API calls logged to AWS CloudTrail for governance and audit.  
- **Certifications**: HIPAA, PCI DSS, GDPR, SOC 1/2/3, ISO 27001, and more.

### Integrations  
- **AWS Lambda**: Trigger on S3 object creation to analyze new images or videos.  
- **Amazon S3**: Source and destination for image/video assets.  
- **AWS Step Functions**: Orchestrate multi-step workflows (e.g., upload → analyze → index).  
- **Amazon Kinesis Video Streams**: Real-time video ingestion and analysis pipelines.  
- **Amazon SageMaker**: Use Rekognition results as features in custom ML workflows.  
- **Amazon Elasticsearch / OpenSearch**: Index labels and metadata for search and analytics.

### Example: Detect Labels via AWS CLI  
```bash
aws rekognition detect-labels \
  --image '{"S3Object":{"Bucket":"my-bucket","Name":"images/photo.jpg"}}' \
  --max-labels 10 \
  --min-confidence 75
