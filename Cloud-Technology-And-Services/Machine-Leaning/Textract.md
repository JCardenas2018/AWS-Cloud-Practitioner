## Amazon Textract

### Overview  
Amazon Textract is a fully managed OCR (Optical Character Recognition) and document analysis service that automatically extracts printed text, handwriting, forms, tables, and key–value pairs from scanned documents or images. It goes beyond simple text detection by understanding the structure of documents.

### Key Features  
- **Text Detection**  
  - Extract printed and handwritten text from scanned documents, PDFs, and images.  
- **Form & Table Extraction**  
  - Identify form fields (key–value pairs) and reconstruct tables with rows and columns.  
- **Queries API**  
  - Ask high-level questions (“What is the total amount due?”) and get targeted answers from complex documents.  
- **Batch & Asynchronous Processing**  
  - Process large multi-page documents asynchronously and retrieve results via job APIs.  
- **Customizable Workflows**  
  - Combine with AWS Lambda, Step Functions, and Amazon Comprehend for full document-processing pipelines.  
- **Integration with ML & AI**  
  - Feed extracted data into Amazon Comprehend for sentiment or entity analysis, or SageMaker for custom models.

### Common Use Cases  
- **Invoice & Receipt Processing**: Automatically extract line items, totals, dates, and vendor names.  
- **Contract Review**: Pull key clauses, parties, and effective dates from legal documents.  
- **Identity Verification (KYC)**: Read passports, driver’s licenses, and ID cards to capture name, birthdate, and document number.  
- **Healthcare Records**: Digitize patient forms, prescriptions, and lab reports for downstream analytics.  
- **Government Forms**: Process applications, tax forms, and surveys at scale.

### Pricing Model  
- **Document Text & Forms**: Charged per page processed (first 1,000 pages/month free).  
- **Queries**: Additional per-query fee on top of page processing.  
- **No Upfront Fees**: Pay-as-you-go, based on monthly usage.

### Security & Compliance  
- **Encryption**: All data in transit is protected with TLS; results and input stored in S3 can be encrypted with AWS KMS CMKs.  
- **Access Control**: Fine-grained IAM policies control who can start jobs, retrieve results, and manage models.  
- **VPC Endpoints**: Use AWS PrivateLink to keep all traffic within your VPC.  
- **Audit Logging**: All API calls are logged in AWS CloudTrail for auditing and compliance.  
- **Certifications**: HIPAA, PCI DSS, SOC 1/2/3, ISO 27001, GDPR, FedRAMP.

### Integrations  
- **Amazon S3**: Trigger Textract jobs on new document uploads.  
- **AWS Lambda**: Orchestrate asynchronous jobs and post-process extracted data.  
- **Amazon Comprehend & QuickSight**: Analyze and visualize extracted text.  
- **AWS Step Functions**: Build serverless workflows for multi-step document processing.  
- **Amazon SageMaker**: Train custom extraction models or downstream analytics.

### Example: Start Asynchronous Document Analysis via AWS CLI  
```bash
aws textract start-document-analysis \
  --document-location '{"S3Object":{"Bucket":"my-bucket","Name":"invoices/2025-07.pdf"}}' \
  --feature-types TABLES FORMS \
  --notification-channel SNSTopicArn=arn:aws:sns:us-east-1:123456789012:TextractTopic,RoleArn=arn:aws:iam::123456789012:role/TextractServiceRole \
  --region us-east-1
