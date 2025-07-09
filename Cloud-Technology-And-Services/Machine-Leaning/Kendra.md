## AWS Kendra

### Overview  
Amazon Kendra is a fully managed, intelligent enterprise search service powered by machine learning. It enables organizations to index a variety of content repositories and deliver highly accurate, context-aware search within applications, web portals, and FAQs—understanding natural language queries and returning relevant results.

### Key Features  
- **Natural Language Understanding**  
  - Supports question-and-answer style queries (“When is my next invoice due?”) rather than just keyword matching.  
- **Pre-built Connectors**  
  - Native connectors for S3, SharePoint, Salesforce, ServiceNow, Google Drive, Confluence, and more.  
- **Custom Data Sources**  
  - Crawl websites or ingest content via APIs and SDKs.  
- **Relevance Tuning & Synonyms**  
  - Boost or demote specific fields, add synonyms and stop words to refine search behavior.  
- **Fine-Grained Access Control**  
  - Honor user permissions via IAM, Active Directory, or application tokens so users see only authorized content.  
- **Facets & Filters**  
  - Automatically extract facets (e.g., document type, date, author) and allow users to filter results.  
- **Query Suggestions & Autocomplete**  
  - Real-time suggestions as users type, improving discovery and usability.  
- **Analytics Dashboard**  
  - Monitor popular queries, zero-result queries, click-through rates, and tune accordingly.

### Common Use Cases  
- **Enterprise Document Search**  
  - Search across business wikis, file shares, and ticketing systems.  
- **Website & Application Search**  
  - Embed intelligent search in customer-facing portals or internal apps.  
- **Support Knowledge Bases**  
  - Enable agents and customers to quickly find troubleshooting guides and FAQs.  
- **Regulatory & Compliance**  
  - Search contracts, policies, and audit logs with fine-grained access controls.

### Pricing Model  
- **Indexing Capacity Units (ICUs)**  
  - You pay per hour for each ICU provisioned to index and query your data.  
- **Storage**  
  - Charges per GB of data stored in the index.  
- **Query Requests**  
  - Included in the ICU hourly rate (no per-query charges).  
- **Data Transfer & Connector Use**  
  - Standard AWS data transfer rates and any applicable connector API costs.

### Security & Compliance  
- **Encryption**  
  - All data at rest is encrypted with AWS KMS CMKs; in transit via HTTPS/TLS.  
- **Access Control**  
  - Integrates with IAM, Amazon Cognito, or SAML providers for user authentication and authorization.  
- **VPC Connectivity**  
  - Enable private access via VPC endpoints (AWS PrivateLink).  
- **Audit Logging**  
  - All API calls are logged in AWS CloudTrail for governance and audit.

### Integrations  
- **AWS Services**: S3, DynamoDB, RDS, Lambda (for custom ingestion), CloudWatch (metrics & logs)  
- **Analytics & BI**: QuickSight, Athena (query logs)  
- **Security**: IAM, KMS, CloudTrail  
- **Applications**: Salesforce, ServiceNow, Confluence, SharePoint, Google Drive, custom HTTP/S sources

### Example: Create an Index with AWS CLI  
```bash
aws kendra create-index \
  --name "EnterpriseSearchIndex" \
  --role-arn arn:aws:iam::123456789012:role/KendraIndexRole \
  --edition ENTERPRISE_EDITION \
  --region us-east-1
