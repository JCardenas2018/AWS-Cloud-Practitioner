## AWS Comprehend

### Overview  
Amazon Comprehend is a fully managed natural language processing (NLP) service that uses machine learning to uncover insights and relationships in text. It can identify the language of input text, extract key phrases, places, people, brands, or events, understand sentiment, and analyze text at scale.

### Key Features  
- **Language Detection**  
  Automatically identifies the dominant language in text (e.g., English, Spanish, German).  
- **Entity Recognition**  
  Detects and categorizes named entities such as PERSON, ORGANIZATION, LOCATION, DATE, QUANTITY.  
- **Key Phrase Extraction**  
  Identifies the most important phrases and terms.  
- **Sentiment Analysis**  
  Classifies overall sentiment (POSITIVE, NEGATIVE, NEUTRAL, MIXED) at document or sentence level.  
- **Syntax Analysis**  
  Parses sentences to identify tokens and their parts of speech (noun, verb, adjective, etc.).  
- **Custom Classification**  
  You can train custom models to classify documents into your own categories.  
- **Custom Entity Recognition**  
  Train your own models to detect domain-specific entities.  
- **Topic Modeling**  
  Automatically groups documents into topics using unsupervised learning.  
- **PII Data Detection**  
  Identifies and redacts personally identifiable information (names, SSNs, emails).

### Common Use Cases  
- **Customer Feedback**: Analyze product reviews or survey responses for sentiment and topics.  
- **Content Personalization**: Tag and route documents based on key phrases or entities.  
- **Compliance & Governance**: Automatically detect and redact PII in text.  
- **Social Media Monitoring**: Track brand mentions, sentiment, and emerging topics.  
- **Document Search & Indexing**: Enhance search relevancy by extracting metadata from documents.

### Pricing Model  
- **Pay-as-you-go**: Charged per unit of text processed.  
  - Language Detection, Sentiment, Entities, Key Phrases, Syntax: \$0.0001 per unit (100 characters).  
  - Custom Classification/Entities: \$0.001 per unit for training; \$0.0005 per unit for inference.  
  - Topic Modeling: \$0.001 per unit.  
- **No Upfront Costs**: No minimum fees or monthly commitments.

### Security & Compliance  
- **Encryption**: Data in transit uses TLS; at rest can be encrypted with AWS KMS keys.  
- **IAM Integration**: Fine-grained access control via IAM policies.  
- **VPC Endpoints**: PrivateLink support to keep traffic within your VPC.  
- **Audit Logging**: All API calls logged in CloudTrail for auditing and compliance.

### Integrations  
- **AWS SDKs & CLI**: Easy integration into applications in Java, Python, JavaScript, Go, .NET, Ruby.  
- **Lambda Triggers**: Invoke Comprehend in real time as part of serverless workflows.  
- **S3**: Batch analysis on large document sets stored in S3.  
- **Glue & Athena**: Enrich and query text analytics results alongside other data.

### Example: Detect Entities with AWS CLI  
```bash
aws comprehend detect-entities \
  --language-code en \
  --text "Amazon Comprehend makes it easy to analyze text at scale." \
  --region us-east-1
