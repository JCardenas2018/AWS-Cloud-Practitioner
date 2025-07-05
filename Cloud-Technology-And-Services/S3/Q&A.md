## S3 Knowledge Assessment Form

Answer the following 100 multiple-choice questions to test your Amazon S3 knowledge.

1. **Which S3 storage class is designed for frequently accessed data?**
   A) S3 Glacier Deep Archive
   B) S3 One Zone-IA
   C) S3 Standard
   D) S3 Standard-IA

2. **Which feature protects objects with immutable, WORM storage?**
   A) Versioning
   B) Object Lock
   C) Server Access Logging
   D) Transfer Acceleration

3. **How do you enable static website hosting on an S3 bucket?**
   A) Enable Website Configuration with index and error documents
   B) Apply a Lifecycle Rule
   C) Enable Cross-Region Replication
   D) Enable Transfer Acceleration

4. **Which API operation initiates a multipart upload?**
   A) PutObject
   B) CreateMultipartUpload
   C) UploadPart
   D) CompleteMultipartUpload

5. **Which storage class offers the lowest storage cost?**
   A) S3 Standard
   B) S3 Intelligent-Tiering
   C) S3 Glacier Flexible Retrieval
   D) S3 Glacier Deep Archive

6. **What is the minimum storage duration for S3 Standard-IA?**
   A) 0 days
   B) 30 days
   C) 90 days
   D) 180 days

7. **Which protocol secures data in transit to S3?**
   A) FTP
   B) SSL/TLS
   C) HTTP
   D) SSH

8. **What does CRR stand for?**
   A) Cross-Region Retrieval
   B) Cross-Region Replication
   C) Client-Side Replication
   D) Cloud Region Routing

9. **Which setting must be enabled on both buckets for cross-region replication?**
   A) Encryption
   B) Versioning
   C) Logging
   D) Transfer Acceleration

10. **Which IAM permission is required for replication to a destination bucket?**
    A) s3\:DeleteObject
    B) s3\:ReplicateObject
    C) s3\:GetObject
    D) s3\:PutObjectTagging

11. **How do you block all public access at the account level?**
    A) Bucket Policy
    B) ACLs
    C) Block Public Access settings
    D) IAM Users

12. **Which feature improves global upload speed without code changes?**
    A) CRR
    B) Transfer Acceleration
    C) Lifecycle Rules
    D) S3 Select

13. **Which feature allows SQL queries on S3 objects?**
    A) S3 Select
    B) Athena
    C) Redshift
    D) Glacier Select

14. **What does SSE-KMS denote?**
    A) Server-Side Encryption with AWS KMS-managed keys
    B) Server-Side Encryption with S3-managed keys
    C) Server-Side Encryption with customer-provided keys
    D) Client-Side Encryption using KMS

15. **Which S3 feature logs all access requests for a bucket?**
    A) CloudWatch Metrics
    B) Server Access Logging
    C) CloudTrail
    D) Storage Lens

16. **Which AWS service can be triggered by S3 object creation events?**
    A) AWS Lambda
    B) Athena
    C) Redshift
    D) S3 Select

17. **How do you configure multipart upload threshold in the AWS CLI?**
    A) Via `aws s3 cp` options
    B) In `~/.aws/config` under `multipart_threshold`
    C) In bucket Lifecycle rules
    D) In bucket policy

18. **Which HTTP status code indicates a successful GET request?**
    A) 200
    B) 301
    C) 404
    D) 500

19. **Which storage class moves objects automatically between tiers?**
    A) S3 One Zone-IA
    B) S3 Intelligent-Tiering
    C) S3 Standard-IA
    D) S3 Glacier Instant Retrieval

20. **How can you filter replication for JPEG files only?**
    A) Prefix `*.jpg`
    B) Filter suffix `.jpg`
    C) Prefix `images/`
    D) No filter support

21. **True or False: S3 provides strong read-after-write consistency.**
    A) True
    B) False

22. **Which SDK method lists object versions?**
    A) list\_objects
    B) list\_object\_versions
    C) get\_object
    D) head\_object

23. **If AES256 is selected as default encryption, which option is used?**
    A) SSE-KMS
    B) SSE-S3
    C) SSE-C
    D) Client-side encryption

24. **Which feature inventories objects and metadata?**
    A) S3 Inventory
    B) CloudWatch Logs
    C) AWS Config
    D) CloudTrail

25. **Which CLI command retrieves replication configuration?**
    A) get-bucket-replication
    B) get-bucket-policy
    C) get-bucket-versioning
    D) get-bucket-logging

26. **Which feature transitions objects between storage classes?**
    A) Lifecycle Rules
    B) CRR
    C) Transfer Acceleration
    D) Object Tagging

27. **Which header requests a specific object version via REST API?**
    A) x-amz-version-id
    B) x-amz-server-side-encryption
    C) x-amz-copy-source
    D) x-amz-content-sha256

28. **What does MFA-Delete enforce?**
    A) MFA for bucket creation
    B) MFA for versioned object deletion
    C) MFA for object upload
    D) MFA for bucket policy changes

29. **Which encryption mode uses customer-provided keys?**
    A) SSE-S3
    B) SSE-KMS
    C) SSE-C
    D) HTTPS

30. **What endpoint type ensures S3 traffic stays within a VPC?**
    A) Internet Gateway
    B) VPC Endpoint Gateway
    C) NAT Gateway
    D) VPN Gateway

31. **Which integration provides edge caching for S3 content?**
    A) CloudFront
    B) Transfer Acceleration
    C) S3 Access Points
    D) Accelerated Endpoints

32. **Which tool offers analytics on storage usage and access patterns?**
    A) CloudWatch
    B) S3 Storage Lens
    C) CloudTrail
    D) AWS Config

33. **Purpose of S3 Access Points?**
    A) Dedicated endpoints with custom policies
    B) Accelerate uploads
    C) Archive data
    D) Enable multi-part upload

34. **How to grant public-read access to all objects?**
    A) Block Public Access Off
    B) Bucket Policy with s3\:GetObject to "\*"
    C) ACL public-read on bucket
    D) IAM user policy

35. **Which metric tracks bytes downloaded from S3?**
    A) AllRequests
    B) BytesDownloaded
    C) DataTransferOut
    D) FirstByteLatency

36. **Which SDK method retrieves object tags?**
    A) get\_object\_tagging
    B) get\_bucket\_tagging
    C) list\_object\_versions
    D) get\_object\_acl

37. **Which feature allows SQL queries in Glacier archives?**
    A) Glacier Select
    B) S3 Select
    C) Athena
    D) Redshift Spectrum

38. **What is the SLA for S3 One Zone-IA?**
    A) 99.99%
    B) 99.9%
    C) 99.5%
    D) 99.0%

39. **Which technique reduces GET request costs by fetching partial data?**
    A) Byte-range GET
    B) Multipart Upload
    C) CRR
    D) Lifecycle Transition

40. **Which lifecycle action moves objects to Glacier Instant Retrieval?**
    A) Expire
    B) Transition to GLACIER\_INSTANT\_RETRIEVAL
    C) AbortIncompleteMultipartUpload
    D) GrantObjectLockLegalHold

41. **Which feature automates cost optimization by tiering?**
    A) Lifecycle Rules
    B) Intelligent-Tiering
    C) Storage Lens
    D) Analytics

42. **How do you prevent accidental deletions across all buckets?**
    A) Enable MFA-Delete
    B) Enable Versioning
    C) Apply Bucket Policy
    D) Use ACLs

43. **Which CLI command lists bucket inventory configurations?**
    A) list-bucket-inventory-configurations
    B) get-bucket-inventory
    C) list-inventory-configurations
    D) get-bucket-inventory-configuration

44. **Which request type incurs a lifecycle transition fee?**
    A) GET
    B) Lifecycle Transition
    C) PUT
    D) DELETE

45. **Which S3 API returns bucket location?**
    A) get-bucket-location
    B) get-bucket-region
    C) head-bucket
    D) get-bucket-info

46. **Which bucket configuration enables audit logging?**
    A) Versioning
    B) Server Access Logging
    C) Block Public Access
    D) Transfer Acceleration

47. **What prefix designates encrypted objects in a replication rule?**
    A) Prefix filter
    B) Suffix filter
    C) Tag-based filter
    D) No filter for encryption

48. **Which action does `aws s3 sync --delete` perform?**
    A) Deletes local extra files
    B) Deletes S3 extra objects
    C) Sync only deletes
    D) Deletes bucket

49. **Which multipart upload part number range is valid?**
    A) 1–9
    B) 0–10000
    C) 1–10000
    D) 1–100000

50. **What is the default maximum number of prefixes returned by list\_objects?**
    A) 1000
    B) 500
    C) 100
    D) 50

51. **Which feature secures buckets and objects with policy conditions?**
    A) Bucket Policy
    B) ACLs
    C) IAM Roles
    D) S3 Access Points

52. **Which header is required for server-side encryption with customer-provided keys?**
    A) x-amz-server-side-encryption-customer-algorithm
    B) x-amz-server-side-encryption
    C) x-amz-server-side-encryption-kms-key-id
    D) x-amz-content-sha256

53. **Which S3 feature provides event notifications?**
    A) S3 Events
    B) CloudWatch Logs
    C) SNS Topics
    D) CloudTrail

54. **How can you paginate list\_objects results?**
    A) Using `--max-items` and `--starting-token`
    B) Using `--limit` and `--offset`
    C) Using `--page-size` only
    D) Using `--continuation-token` only

55. **Which encryption type is free of charge?**
    A) SSE-KMS
    B) SSE-S3
    C) SSE-C
    D) Client-side encryption

56. **Which feature identifies replication failures?**
    A) CloudWatch Alarms
    B) S3 Event Notifications
    C) Replication Metrics
    D) CloudTrail Events

57. **What does `storage-class: STANDARD_IA` in lifecycle policy do?**
    A) Expires objects
    B) Deletes objects
    C) Transitions to S3 Standard-IA
    D) Archives to Glacier

58. **Which S3 option allows custom DNS CNAME for website endpoint?**
    A) Bucket website configuration
    B) CloudFront
    C) DNS Alias record
    D) Route 53 alias

59. **Which metric shows number of objects in a bucket?**
    A) NumberOfObjects
    B) AllRequests
    C) BytesUploaded
    D) BucketSizeBytes

60. **Which parameter on put-object sets object metadata?**
    A) --metadata-directive
    B) --metadata
    C) --tagging
    D) --acl

61. **Which lifecycle action aborts incomplete multipart uploads?**
    A) AbortIncompleteMultipartUpload
    B) ExpireObjectDeleteMarker
    C) Transition to GLACIER
    D) TagExpiration

62. **Which CLI command removes all objects in a bucket?**
    A) aws s3 rm s3://bucket --recursive
    B) aws s3 delete-bucket --all
    C) aws s3 destroy
    D) aws s3 purge

63. **What option shows progress during aws s3 cp?**
    A) --quiet
    B) --progress
    C) --verbose
    D) --no-progress

64. **Which header returns replication status of an object?**
    A) x-amz-replication-status
    B) x-amz-server-side-encryption
    C) x-amz-storage-class
    D) x-amz-version-id

65. **Which feature enables custom IAM roles per access point?**
    A) Object Lock
    B) S3 Access Point
    C) Multi-Region Access Point
    D) VPC Endpoint

66. **What is the default maximum object size for put-object?**
    A) 5 MB
    B) 5 GB
    C) 100 GB
    D) 5 TB

67. **Which storage class is single-AZ only?**
    A) S3 Standard
    B) S3 One Zone-IA
    C) S3 Intelligent-Tiering
    D) S3 Standard-IA

68. **Which API returns bucket inventory list?**
    A) list\_bucket\_inventory\_configurations
    B) get-bucket-inventory-list
    C) list\_inventory
    D) get-inventory-list

69. **Which storage lens feature provides usage recommendations?**
    A) Cost Optimization Insights
    B) Security Metrics
    C) Activity Metrics
    D) Operations Dashboard

70. **Which replication rule ID must be unique per bucket?**
    A) RuleName
    B) ID
    C) Prefix
    D) Priority

71. **Which permission is required for get-object-legal-hold?**
    A) s3\:GetObjectRetention
    B) s3\:GetBucketPolicy
    C) s3\:GetObjectLegalHold
    D) s3\:GetObjectLockConfiguration

72. **Which AWS SDK supports asynchronous S3 operations?**
    A) boto3
    B) AWS SDK for JavaScript v3
    C) AWS CLI
    D) AWS SDK for Go v1

73. **Which header is used for conditional GET on ETag?**
    A) If-Match
    B) If-Modified-Since
    C) If-Unmodified-Since
    D) If-None-Match

74. **Which feature splits large objects into parts for parallel upload?**
    A) Multipart Upload
    B) Transfer Acceleration
    C) S3 Batch
    D) S3 Select

75. **Which CLI command lists all buckets in an account?**
    A) aws s3 ls
    B) aws s3api list-buckets
    C) aws s3 list-buckets
    D) aws s3api ls

76. **Which lifecycle rule action marks expired object delete markers?**
    A) ExpireCurrentObjectVersion
    B) ExpireObjectDeleteMarker
    C) TransitionExpiredObject
    D) DeleteExpiredMarkers

77. **Which feature allows data retrieval in hours from Glacier?**
    A) Glacier Instant Retrieval
    B) Glacier Flexible Retrieval
    C) Glacier Deep Archive
    D) S3 Select

78. **Which console section shows per-bucket metrics?**
    A) Monitoring tab
    B) Permissions tab
    C) Management tab
    D) Properties tab

79. **Which AWS service uses S3 Inventory to audit access?**
    A) AWS Config
    B) Amazon Inspector
    C) AWS Shield
    D) AWS Trusted Advisor

80. **Which parameter sets ACL when uploading via CLI?**
    A) --acl
    B) --permission
    C) --access-control
    D) --grant-read

81. **Which storage class supports automatic tiering with no additional charges for access?**
    A) S3 Standard-IA
    B) S3 Glacier Flexible Retrieval
    C) S3 Intelligent-Tiering
    D) S3 Glacier Deep Archive

82. **What is the maximum number of buckets per account by default?**
    A) 100
    B) 50
    C) 200
    D) 500

83. **Which request header requests a checksum in response?**
    A) x-amz-checksum-crc32
    B) x-amz-request-checksum
    C) x-amz-meta-checksum
    D) None; use SDK options

84. **Which feature ensures TLS certificates rotate automatically?**
    A) CloudFront integration
    B) Transfer Acceleration
    C) S3-managed encryption
    D) Bucket Policy

85. **Which operation copies objects between buckets server-side?**
    A) PutObject
    B) CopyObject
    C) UploadPartCopy
    D) ReplicateObject

86. **Which lifecycle rule action transitions to Standard-IA?**
    A)                   Transition to STANDARD\_IA
    B) Transition to ONEZONE\_IA
    C) Transition to GLACIER
    D) AbortIncompleteMultipartUpload

87. **Which parameter enables encryption with KMS key in CLI?**
    A) --server-side-encryption AES256
    B) --server-side-encryption aws\:kms
    C) --sse-kms-key-id
    D) Both B and C

88. **Which credential type can assume an IAM role for S3 access?**
    A) IAM User
    B) IAM Role
    C) Federated User
    D) All of the above

89. **Which feature returns bucket metrics at prefix level?**
    A) CloudWatch
    B) S3 Storage Lens
    C) CloudTrail
    D) S3 Access Logs

90. **Which command lists objects with a specified prefix?**
    A) aws s3 ls s3://bucket/prefix
    B) aws s3api list-objects --prefix prefix
    C) aws s3api list-objects-v2 --prefix prefix
    D) Both B and C

91. **Which header in replication rule preserves object tags?**
    A) TaggingDirective
    B) MetadataDirective
    C) ReplicationConfiguration
    D) None; always copies tags

92. **Which IAM condition key restricts access by object tag?**
    A) s3\:prefix
    B) s3\:ExistingObjectTag/<tag>
    C) s3\:TagKey
    D) None exist

93. **Which feature exports metrics to CloudWatch for storage efficiency?**
    A) Storage Lens
    B) CloudTrail
    C) Inventory
    D) Analytics

94. **What is the default throughput for multipart upload parts?**
    A) 5 MB/s per part
    B) Unlimited
    C) 100 MB/s per part
    D) Depends on network

95. **Which CLI option decrypts an encrypted object on download?**
    A) --sse-c
    B) --sse-customer-algorithm
    C) --sse-kms-key-id
    D) SDK handles decryption automatically

96. **Which feature allows custom notifications on replication failure?**
    A) S3 Events
    B) CloudWatch Events
    C) EventBridge
    D) SNS notifications via Replication Configuration

97. **Which property in CloudFormation defines bucket encryption?**
    A) BucketEncryptionConfiguration
    B) EncryptionConfiguration
    C) BucketEncryption
    D) ServerSideEncryptionConfiguration

98. **Which tool can sync local folder to S3 with delete option?**
    A) aws s3 mv
    B) aws s3 sync --delete
    C) aws s3 cp
    D) aws s3api put-object

99. **Which feature lets you host websites with index and error documents?**
    A) Static Website Hosting
    B) CloudFront Distribution
    C) Access Points
    D) S3 Batch Operations

100. **Which AWS service provides drill-down dashboards for S3 usage?**
     A) CloudWatch Dashboards
     B) S3 Storage Lens
     C) AWS Trusted Advisor
     D) AWS Cost Explorer

---

## Answer Key

1. C
2. B
3. A
4. B
5. D
6. B
7. B
8. B
9. B
10. B
11. C
12. B
13. A
14. A
15. B
16. A
17. B
18. A
19. B
20. B
21. A
22. B
23. B
24. A
25. A
26. A
27. A
28. B
29. C
30. B
31. A
32. B
33. A
34. B
35. B
36. A
37. A
38. C
39. A
40. B
41. B
42. A
43. D
44. B
45. A
46. B
47. C
48. B
49. C
50. A
51. A
52. A
53. A
54. D
55. B
56. C
57. C
58. B
59. D
60. B
61. A
62. A
63. D
64. A
65. B
66. B
67. B
68. A
69. A
70. B
71. C
72. B
73. D
74. A
75. B
76. B
77. B
78. A
79. A
80. A
81. C
82. A
83. D
84. A
85. B
86. A
87. D
88. D
89. B
90. D
91. D
92. B
93. A
94. D
95. D
96. D
97. C
98. B
99. A
100. B
