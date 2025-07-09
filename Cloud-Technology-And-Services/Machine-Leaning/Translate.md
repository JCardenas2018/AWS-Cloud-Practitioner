## Amazon Translate

### Overview  
Amazon Translate is a fully managed neural machine translation (NMT) service that delivers fast, high-quality, and affordable language translation. It enables applications to localize content for international users and to build real-time translation workflows.

### Key Features  
- **Real-Time & Batch Translation**  
  - **Real-Time**: Low-latency API for on-the-fly text translation in applications.  
  - **Batch**: Asynchronous jobs for large volumes of documents stored in Amazon S3.  
- **Neural Machine Translation**  
  - Uses advanced NMT models to deliver fluent, context-aware translations.  
- **Custom Terminology**  
  - Define your own glossary of terms to override default translations (brand names, domain-specific vocabulary).  
- **Active Custom Translation (ACT)**  
  - Fine-tune base models with your own parallel text data to improve accuracy on specialized content.  
- **Automatic Language Detection**  
  - Detects source language automatically when not known in advance.  
- **Formality and Tone Controls**  
  - Support for specifying formal or informal tone in select language pairs.

### Supported Languages  
Over 80 languages and variants, including major global languages (English, Spanish, Chinese, Arabic, French, German, Japanese, Portuguese, Russian, etc.).

### Common Use Cases  
- **Website & App Localization**: Translate UI strings, help articles, product descriptions.  
- **Customer Support**: Real-time chat translation between agents and customers.  
- **Document Translation**: Batch-translate reports, legal contracts, manuals.  
- **E-commerce**: Localize catalog entries, user reviews, marketing emails.  
- **Content Moderation**: Translate user-generated content for centralized review.

### Pricing Model  
- **Real-Time Translation**: Charged per million characters of text translated.  
- **Batch Translation**: Charged per million characters of text processed in S3.  
- **Custom Terminology**: No additional cost beyond the underlying translation charge.  
- **ACT Training**: Charged per hour of model training compute and per million characters used.

### Security & Compliance  
- **Encryption**  
  - Data in transit via TLS; you can encrypt input/output in S3 with AWS KMS.  
- **Access Control**  
  - Fine-grained IAM permissions for Translate actions, custom terminology management, and S3 access.  
- **VPC Endpoints**  
  - AWS PrivateLink support to keep traffic within your VPC.  
- **Audit Logging**  
  - All API calls logged in AWS CloudTrail for auditing and compliance.  
- **Certifications**  
  - HIPAA eligibility, GDPR, SOC 1/2/3, ISO 27001, PCI DSS, FedRAMP, and more.

### Integrations  
- **AWS Services**:  
  - **Amazon S3**: Source and target for batch jobs.  
  - **AWS Lambda**: Real-time translation in serverless workflows.  
  - **Amazon API Gateway**: Expose translation APIs to your applications.  
  - **Amazon CloudWatch**: Metrics and logs for monitoring usage and performance.  
- **SDKs & CLI**: Java, Python (Boto3), JavaScript, .NET, Go, Ruby, PHP, and more.  
- **Third-Party**: Integrate with CMS, chat platforms, and localization tools.

### Example: Translate Text via AWS CLI  
```bash
aws translate translate-text \
  --text "Hello, world!" \
  --source-language-code en \
  --target-language-code es \
  --region us-east-1
