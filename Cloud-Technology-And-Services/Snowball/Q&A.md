# 30 AWS Snowball Multiple-Choice Questions

1. Which Snowball device offers built-in compute capabilities with Lambda support?  
   - A. Snowball (standard)  
   - B. Snowball Edge Storage Optimized  
   - C. Snowball Edge Compute Optimized  
   - D. Snowmobile  

2. What is the maximum usable storage capacity of a standard Snowball?  
   - A. 50 TB  
   - B. 80 TB  
   - C. 42 TB  
   - D. 100 TB  

3. Which Amazon service key is used to encrypt data on a Snowball device?  
   - A. AWS Shield  
   - B. AWS KMS  
   - C. AWS IAM  
   - D. AWS Secrets Manager  

4. Snowball Edge Compute Optimized devices include:  
   - A. GPUs for ML inference  
   - B. Only storage, no compute  
   - C. 10 Gbps networking only  
   - D. Integrated tape drive  

5. Snowmobile is best suited for transferring:  
   - A. Up to 50 TB  
   - B. Up to 100 TB  
   - C. Petabyte-scale data (up to 45 PB)  
   - D. Streaming video  

6. Which CLI command creates an import job to S3 using Snowball?  
   - A. `aws snowball start-job`  
   - B. `aws snowball create-job`  
   - C. `aws s3 cp`  
   - D. `aws snowball start-import`  

7. How is return shipping of a Snowball device arranged?  
   - A. Customer must ship via personal courier  
   - B. AWS ships a return label; device is picked up by the carrier  
   - C. Device is drop-shipped at AWS data center  
   - D. No need to return — it’s disposable  

8. What internal network speed do Snowball devices support?  
   - A. 1 Gbps  
   - B. 10 Gbps  
   - C. 100 Mbps  
   - D. 40 Gbps  

9. Which feature allows processing data on-device before shipping?  
   - A. Edge Lambda functions  
   - B. S3 Transfer Acceleration  
   - C. DataSync integration  
   - D. Kinesis Video Streams  

10. Snowball Edge Storage Optimized provides approximately how much usable storage?  
    - A. 50 TB  
    - B. 42 TB  
    - C. 80 TB  
    - D. 100 TB  

11. When creating a Snowball job, you must specify:  
    - A. A VPC ID  
    - B. An S3 bucket ARN  
    - C. A CloudFront distribution  
    - D. A Glacier vault name  

12. What happens if you power off a Snowball Edge device during transfer?  
    - A. Data is automatically erased  
    - B. Device enters safe-shutdown and data remains encrypted  
    - C. Device is permanently disabled  
    - D. Transfer job is canceled without warning  

13. Which role must you grant permissions for Snowball to write to your S3 bucket?  
    - A. EC2 instance role  
    - B. AWSDataSyncRole  
    - C. AWSDataTransferRole  
    - D. SnowballAccessRole  

14. How are Snowball devices tracked in transit?  
    - A. They include built-in GPS  
    - B. Via carrier tracking and job manifests  
    - C. Using AWS IoT  
    - D. Through CloudWatch Logs  

15. Which Snowball type would you choose for offline ML model training with GPU?  
    - A. Snowball standard  
    - B. Snowball Edge Storage Optimized  
    - C. Snowball Edge Compute Optimized  
    - D. Snowmobile  

16. You can run EC2 instances on which Snowball device?  
    - A. Any Snowball device  
    - B. Only Snowmobile  
    - C. Snowball Edge devices  
    - D. Snowball standard  

17. Which AWS service can perform incremental data transfer after initial Snowball import?  
    - A. AWS DataSync  
    - B. AWS Transfer Family  
    - C. Direct Connect  
    - D. Storage Gateway  

18. How do you unlock a Snowball device for data loading?  
    - A. By scanning a QR code  
    - B. Using the unlock code from the job manifest  
    - C. Via SSH with a key pair  
    - D. Automatic upon arrival  

19. What is the purpose of the job manifest file?  
    - A. It lists the IAM policies used  
    - B. It contains device unlock code and job metadata  
    - C. It starts the transfer job automatically  
    - D. It stores S3 bucket contents  

20. Snowball devices connect to your network over:  
    - A. Fibre Channel  
    - B. Standard Ethernet (RJ-45)  
    - C. USB 3.0  
    - D. SATA  

21. Which AWS CLI command retrieves the status of a Snowball job?  
    - A. `aws snowball describe-job`  
    - B. `aws snowball get-status`  
    - C. `aws snowball status-job`  
    - D. `aws snowball list-jobs`  

22. Data on a Snowball device is erased by AWS when:  
    - A. You delete the job in the console  
    - B. AWS receives the device and imports your data  
    - C. The device battery dies  
    - D. You power it off  

23. Which Snowball device supports S3 compatible endpoints locally?  
    - A. Snowball standard  
    - B. Snowball Edge Storage Optimized  
    - C. Snowmobile  
    - D. All of the above  

24. How long is the maximum job duration for a Snowball import/export?  
    - A. 7 days  
    - B. 30 days  
    - C. 45 days  
    - D. 60 days  

25. Which CloudFormation resource type defines a Snowball job?  
    - A. AWS::Snowball::Device  
    - B. AWS::Snowball::Job  
    - C. AWS::Snowball::Transfer  
    - D. AWS::Snowball::Order  

26. A Snowball Edge Compute Optimized device can run how many concurrent Lambda functions?  
    - A. 4 functions  
    - B. 10 functions  
    - C. Up to 250 concurrent functions  
    - D. Unlimited  

27. To archive data directly to Glacier via Snowball, you must:  
    - A. Use Snowball Edge Compute Optimized  
    - B. Configure an export job with Glacier as the destination  
    - C. Enable Glacier transfer acceleration  
    - D. Copy from S3 after import  

28. What happens if a Snowball device is lost in transit?  
    - A. Data is recovered by AWS support  
    - B. Data remains encrypted and inaccessible without your KMS key  
    - C. AWS uses backups to restore data  
    - D. The job automatically retries  

29. Which AWS Snow family device is delivered in a shipping container?  
    - A. Snowball standard  
    - B. Snowball Edge  
    - C. Snowmobile  
    - D. Snowcone  

30. Snowcone differs from Snowball in that it:  
    - A. Supports 100 TB capacity  
    - B. Is pocket-sized (~8 TB) and battery-powered  
    - C. Includes GPU acceleration  
    - D. Uses tape storage  

---

## Answers

1. C  
2. A  
3. B  
4. A  
5. C  
6. B  
7. B  
8. B  
9. A  
10. C  
11. B  
12. B  
13. C  
14. B  
15. C  
16. C  
17. A  
18. B  
19. B  
20. B  
21. A  
22. B  
23. B  
24. B  
25. B  
26. C  
27. B  
28. B  
29. C  
30. B  
