# 30 AWS KMS Multiple-Choice Questions

1. Which key types are supported by AWS KMS?  
   - A. Symmetric CMKs only  
   - B. Asymmetric CMKs only  
   - C. Symmetric and asymmetric CMKs  
   - D. No CMKs  

2. Which AWS KMS API operation creates a new customer master key (CMK)?  
   - A. CreateKey  
   - B. GenerateKey  
   - C. CreateGrant  
   - D. ImportKeyMaterial  

3. Which operation generates a data key and returns both the plaintext and ciphertext?  
   - A. GenerateDataKey  
   - B. GenerateDataKeyWithoutPlaintext  
   - C. Encrypt  
   - D. Decrypt  

4. Which operation generates a data key but returns only the ciphertext?  
   - A. GenerateDataKeyWithoutPlaintext  
   - B. GenerateDataKey  
   - C. Encrypt  
   - D. Decrypt  

5. Which operation encrypts your plaintext under a CMK?  
   - A. Encrypt  
   - B. Decrypt  
   - C. ReEncrypt  
   - D. GenerateDataKey  

6. Which operation decrypts ciphertext back to plaintext?  
   - A. Decrypt  
   - B. Encrypt  
   - C. ReEncrypt  
   - D. GenerateDataKey  

7. Which operation re-encrypts ciphertext from one CMK under another CMK?  
   - A. ReEncrypt  
   - B. Encrypt  
   - C. Decrypt  
   - D. GenerateDataKey  

8. Which operation creates a digital signature with an asymmetric CMK?  
   - A. Sign  
   - B. Verify  
   - C. Encrypt  
   - D. Decrypt  

9. Which operation verifies a digital signature created by KMS?  
   - A. Verify  
   - B. Sign  
   - C. GetPublicKey  
   - D. Decrypt  

10. Which operation retrieves the public key material of an asymmetric CMK?  
    - A. GetPublicKey  
    - B. DescribeKey  
    - C. ListKeys  
    - D. ListAliases  

11. Which operation creates a grant allowing a principal to use a CMK?  
    - A. CreateGrant  
    - B. PutKeyPolicy  
    - C. AttachPolicy  
    - D. CreateAlias  

12. Which operation revokes an existing grant on a CMK?  
    - A. RevokeGrant  
    - B. RetireGrant  
    - C. DisableKey  
    - D. DeleteGrant  

13. Which operation schedules the deletion of a CMK?  
    - A. ScheduleKeyDeletion  
    - B. DisableKey  
    - C. DeleteKey  
    - D. RetireKey  

14. What is the minimum waiting period when you schedule a CMK for deletion?  
    - A. 7 days  
    - B. 1 day  
    - C. 10 days  
    - D. 30 days  

15. Which KMS feature allows cross-account use of a CMK?  
    - A. Key policy granting cross-account access  
    - B. IAM role mapping only  
    - C. Tag-based access control  
    - D. Parameter Store integration  

16. What is envelope encryption?  
    - A. Encrypt data with a data key, then encrypt that data key under a CMK  
    - B. Encrypt keys with themselves  
    - C. Encrypt data under multiple CMKs simultaneously  
    - D. Encrypt data in transit with TLS  

17. Which AWS service uses CMKs to encrypt stored secrets?  
    - A. AWS Secrets Manager  
    - B. Amazon EC2  
    - C. Amazon S3  
    - D. Amazon RDS  

18. What is an encryption context in KMS?  
    - A. Additional authenticated data passed to Encrypt/Decrypt  
    - B. The CMK alias  
    - C. The AWS region where the key resides  
    - D. A logging parameter  

19. Where are all KMS API calls logged for auditing?  
    - A. AWS CloudTrail  
    - B. CloudWatch Logs  
    - C. AWS Config  
    - D. S3 access logs  

20. How often can you enable automatic rotation of a CMK?  
    - A. Every year (annual)  
    - B. Every month  
    - C. Every day  
    - D. Every hour  

21. Which KMS feature allows you to bring your own key material?  
    - A. ImportKeyMaterial (Bring Your Own Key)  
    - B. External HSM integration  
    - C. BYO HSM (Bring Your Own HSM)  
    - D. Customer Provided Key  

22. Which operation imports your own key material into an existing CMK?  
    - A. ImportKeyMaterial  
    - B. CreateKey  
    - C. PutKeyPolicy  
    - D. GenerateDataKey  

23. What is the default quota for CMKs per AWS account per region?  
    - A. 10,000  
    - B. 1,000  
    - C. 100  
    - D. 10  

24. Which prefix must all KMS key aliases begin with?  
    - A. alias/  
    - B. kms/  
    - C. key/  
    - D. cmk/  

25. What is a multi-Region CMK?  
    - A. A CMK replicated and synchronized across multiple AWS regions  
    - B. A CMK used in multiple VPCs  
    - C. A CMK stored in multiple Availability Zones  
    - D. A CMK shared across multiple accounts  

26. Which CloudFormation resource defines a KMS key alias?  
    - A. AWS::KMS::Alias  
    - B. AWS::KMS::KeyAlias  
    - C. AWS::KMS::AliasKey  
    - D. AWS::KMS::Key  

27. Which CloudFormation property enables automatic key rotation on a CMK?  
    - A. EnableKeyRotation  
    - B. RotateAutomatically  
    - C. KeyRotationEnabled  
    - D. AutoRotate  

28. What underlying hardware does KMS use to protect CMKs?  
    - A. Hardware Security Modules (HSMs)  
    - B. EC2 instances  
    - C. S3 storage  
    - D. DynamoDB  

29. Is specifying an encryption context mandatory when calling the Encrypt API?  
    - A. No, it is optional  
    - B. Yes, it is mandatory  
    - C. It is deprecated  
    - D. Only required for asymmetric CMKs  

30. Which CLI parameter specifies the encryption context when encrypting data?  
    - A. --encryption-context  
    - B. --context  
    - C. --additional-authenticated-data  
    - D. --enc-context  

---

## Answers

1. C  
2. A  
3. A  
4. A  
5. A  
6. A  
7. A  
8. A  
9. A  
10. A  
11. A  
12. A  
13. A  
14. A  
15. A  
16. A  
17. A  
18. A  
19. A  
20. A  
21. A  
22. A  
23. A  
24. A  
25. A  
26. A  
27. A  
28. A  
29. A  
30. A  
