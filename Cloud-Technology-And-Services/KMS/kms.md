## AWS KMS (Key Management Service)

### Overview  
AWS Key Management Service (KMS) is a fully managed service that makes it easy to create, control, and audit the use of cryptographic keys used to encrypt your data across AWS and in your applications. KMS stores keys securely in hardware-backed HSMs and integrates with many AWS services.

### Key Features  
- **Customer Master Keys (CMKs)**  
  - **Customer-Managed CMKs**: You create, rotate, and define access policies.  
  - **AWS-Managed CMKs**: AWS creates and rotates keys on your behalf with basic permissions.  
- **Automatic Key Rotation**  
  - Enable annual automatic rotation for CMKs with zero downtime.  
- **Hardware Security Modules (HSMs)**  
  - FIPS 140-2 Level 3 protection via integrated CloudHSM for Multi-Region CMKs.  
- **Fine-Grained Access Control**  
  - Use IAM policies and key policies to control which principals can use or manage each CMK.  
- **Audit and Monitoring**  
  - All KMS API calls are logged in AWS CloudTrail with caller identity, timestamp, and parameters.  
- **Symmetric and Asymmetric Keys**  
  - Symmetric CMKs for high-throughput encryption/decryption; asymmetric CMKs for signing, verification, and envelope encryption.

### Common Use Cases  
- **Data-at-Rest Encryption**  
  - Encrypt S3 objects, EBS volumes, RDS databases, Redshift clusters, DynamoDB tables, Elasticsearch, etc.  
- **Data-in-Transit Encryption**  
  - Protect TLS private keys managed by ACM, or implement custom TLS by storing private keys in KMS.  
- **Digital Signatures**  
  - Use the Sign and Verify APIs to validate integrity of messages or documents.  
- **Secrets Management**  
  - AWS Secrets Manager and SSM Parameter Store use KMS to encrypt stored secrets.  
- **Multi-Account & Multi-Region Sharing**  
  - Share CMKs across AWS accounts or regions to centralize key management.

### Pricing Model  
- **CMK Charges**  
  - Symmetric CMK: \$1.00 per CMK per month  
  - Asymmetric CMK: \$1.50 per CMK per month  
- **API Requests**  
  - \$0.03 per 10,000 requests (Encrypt, Decrypt, Sign, Verify, GenerateDataKey)  
- **Key Rotation**  
  - No additional charge for automatic rotation

### Security & Compliance  
- **CloudTrail Integration**  
  - Detailed audit logs for every key usage and management action.  
- **Key Policies & IAM**  
  - Combine resource-based key policies with IAM policies for granular access.  
- **Tokenization Workflows**  
  - Integrate with Lambda to build custom tokenization and de-tokenization.  
- **Certifications**  
  - PCI DSS, HIPAA, FedRAMP, SOC 1/2/3, ISO 27001, GDPR, and more.

### Integrations  
- **AWS Services**: S3, EBS, RDS, Redshift, DynamoDB, Elasticsearch, Secrets Manager, ACM  
- **SDKs & CLI**: Encrypt/decrypt data programmatically in Java, Python, Node.js, Go, Ruby, .NET, etc.  
- **CloudHSM**: For advanced HSM operations and FIPS compliance beyond KMS capabilities.

### Example: Encrypt & Decrypt with AWS CLI  
```bash
# Encrypt plaintext and save ciphertext
aws kms encrypt \
  --key-id arn:aws:kms:us-east-1:123456789012:key/abcd1234-ef56-7890-abcd-1234ef567890 \
  --plaintext "MySuperSecretValue" \
  --query CiphertextBlob \
  --output text > ciphertext.bin

# Decrypt ciphertext and output plaintext
aws kms decrypt \
  --ciphertext-blob fileb://ciphertext.bin \
  --query Plaintext \
  --output text | base64 --decode
