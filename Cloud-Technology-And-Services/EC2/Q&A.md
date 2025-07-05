# EC2 Knowledge Assessment (100 Questions)

Answer the following multiple-choice questions about Amazon EC2. Select the best option for each.

1. **What does EC2 stand for?**
   A) Elastic Cloud Compute
   B) Elastic Compute Cloud
   C) Elastic Container Cloud
   D) Elastic Compute Cluster

2. **Which pricing model offers up to 90% discount on spare capacity?**
   A) On-Demand
   B) Reserved Instances
   C) Spot Instances
   D) Savings Plans

3. **Which instance family is optimized for CPU-intensive tasks?**
   A) r5
   B) c5
   C) m5
   D) t3

4. **Which service is used to automate EC2 image creation?**
   A) EC2 Image Builder
   B) AWS Lambda
   C) Systems Manager
   D) AWS Batch

5. **What feature allows you to stop and start EC2 instances on a schedule?**
   A) Auto Scaling
   B) AWS Lambda
   C) Instance Scheduler
   D) CloudWatch Events

6. **Which volume type provides the highest IOPS?**
   A) gp3
   B) io2
   C) st1
   D) sc1

7. **What is the default maximum size of an EBS snapshot?**
   A) 16 TB
   B) 64 TB
   C) 1 TB
   D) Unlimited

8. **Which OS user is used by default on Amazon Linux?**
   A) ubuntu
   B) centos
   C) ec2-user
   D) admin

9. **What port is used for SSH access?**
   A) 22
   B) 3389
   C) 80
   D) 443

10. **Which metadata service version requires a session token?**
    A) IMDSv1
    B) IMDSv2
    C) Both
    D) Neither

11. **Which IAM entity is attached directly to EC2 instances?**
    A) IAM User
    B) IAM Group
    C) Role/Instance Profile
    D) IAM Policy

12. **What is a golden AMI?**
    A) Unconfigured image
    B) Custom hardened machine image
    C) Public marketplace image
    D) Free tier image

13. **Which CLI command launches a new EC2 instance?**
    A) aws ec2 start-instances
    B) aws ec2 run-instances
    C) aws ec2 create-instance
    D) aws ec2 new-instances

14. **Which tool helps right-size EC2 instances?**
    A) AWS Config
    B) Compute Optimizer
    C) Trusted Advisor
    D) Cost Explorer

15. **Which service can patch EC2 instances automatically?**
    A) AWS Systems Manager Patch Manager
    B) AWS Inspector
    C) AWS Config
    D) AWS Backup

16. **Which instance type is bare metal?**
    A) m5.large
    B) m5.metal
    C) t3.micro
    D) c5.xlarge

17. **Which network feature provides isolation at the subnet level?**
    A) Security Group
    B) NACL
    C) IAM Role
    D) VPC Endpoint

18. **Which log captures all EC2 API calls?**
    A) CloudWatch Logs
    B) VPC Flow Logs
    C) CloudTrail
    D) S3 Access Logs

19. **Which feature provides hardware-level security isolation?**
    A) SGX
    B) Nitro Hypervisor
    C) Virtual Private Cloud
    D) IAM Roles

20. **Which data store can be mounted concurrently by multiple EC2 instances?**
    A) EBS
    B) Instance Store
    C) EFS
    D) S3

21. **Which command stops an EC2 instance?**
    A) aws ec2 stop-instance
    B) aws ec2 stop-instances
    C) aws ec2 terminate-instances
    D) aws ec2 end-instances

22. **Which parameter in run-instances specifies a key pair?**
    A) --key
    B) --key-name
    C) --ssh-key
    D) --key-file

23. **Which Auto Scaling feature replaces unhealthy instances?**
    A) Lifecycle Hooks
    B) Instance Refresh
    C) Health Checks
    D) Spot Fleet

24. **Which service provides instance metadata?**
    A) AWS Metadata Service
    B) AWS IMDS
    C) EC2 Metadata Service
    D) AWS Config

25. **What is the default tenancy for EC2 instances?**
    A) Dedicated
    B) Shared
    C) Host
    D) Single

26. **Which feature encrypts EBS volume data at rest by default?**
    A) SSE-S3
    B) SSE-KMS
    C) EBS Encryption
    D) Client-side encryption

27. **Which parameter filters describe-instances by tag?**
    A) --filter Name=tag\:Name,Values=Value
    B) --tags Name=Value
    C) --query Tags.Name
    D) --attribute tag\:Name

28. **Which stateless firewall filters inbound traffic?**
    A) Security Group
    B) NACL
    C) VPC Endpoint
    D) AWS WAF

29. **Which instance metadata path returns IAM role name?**
    A) /latest/meta-data/iam/info
    B) /latest/meta-data/iam/security-credentials/
    C) /latest/meta-data/instance-id
    D) /latest/meta-data/iam/role-name

30. **Which AWS service provides launch templates?**
    A) EC2
    B) CloudFormation
    C) Systems Manager
    D) IAM

31. **Which type of EBS volume should you use for cold storage?**
    A) sc1
    B) st1
    C) gp3
    D) io2

32. **Which instance type uses AWS Graviton processors?**
    A) m5
    B) c5
    C) m6g
    D) t3

33. **Which command lists EC2 instance types?**
    A) aws ec2 describe-instance-types
    B) aws ec2 list-instance-types
    C) aws ec2 describe-instances --types
    D) aws ec2 list-instances-types

34. **Which placement group type is recommended for low-latency workloads?**
    A) Cluster
    B) Spread
    C) Partition
    D) Burst

35. **Which option reduces network hops between instances in the same AZ?**
    A) Public IP
    B) Placement Group
    C) Elastic IP
    D) Dedicated Host

36. **Which AMI attribute specifies virtualization type?**
    A) VirtualizationType
    B) Hypervisor
    C) RootDeviceType
    D) Architecture

37. **Which instance storage type is ephemeral?**
    A) EBS
    B) Instance Store
    C) EFS
    D) FSx

38. **Which AWS Config rule checks EC2 root volume encryption?**
    A) encrypted-volumes
    B) restricted-common-ports
    C) ebs-snapshot-public-prohibited
    D) ec2-managed-instance-inventory

39. **Which service provides a managed bastion host solution?**
    A) AWS SSM Session Manager
    B) AWS VPN
    C) AWS Directory Service
    D) AWS IAM

40. **Which command creates an image of a running instance?**
    A) aws ec2 create-snapshot
    B) aws ec2 create-image
    C) aws ec2 launch-image
    D) aws ec2 register-image

41. **Which parameter sets the security group for a new instance?**
    A) --security-groups
    B) --security-group-ids
    C) --sg
    D) --sg-ids

42. **Which feature allows disabling public IP assignment at launch?**
    A) Launch Template
    B) Subnet setting
    C) IAM Role
    D) Security Group

43. **Which instance type is best for in-memory caching?**
    A) r5
    B) m5
    C) t3
    D) c5

44. **Which command modifies instance attributes?**
    A) aws ec2 modify-instance-attributes
    B) aws ec2 update-instance
    C) aws ec2 change-instance-attributes
    D) aws ec2 set-instance-attributes

45. **Which instance limits can be increased via support request?**
    A) vCPU limit
    B) Instance count per region
    C) EBS throughput
    D) All of the above

46. **Which feature supports launching EC2 instances in Party Mode?**
    A) Reserved Instances
    B) Placement Groups
    C) Elastic Fabric Adapter
    D) Nitro Enclaves

47. **Which instance type supports NVMe instance storage?**
    A) i3
    B) t3
    C) m5
    D) r5

48. **Which API returns instance status checks?**
    A) describe-instance-status
    B) describe-instance-health
    C) describe-instances
    D) describe-instance-checks

49. **Which CloudWatch metric shows instance reachability?**
    A) StatusCheckFailed
    B) StatusCheckFailed\_Instance
    C) StatusCheckFailed\_System
    D) CPUUtilization

50. **Which option enables detailed monitoring?**
    A) --monitoring Enabled=false
    B) --monitoring Enabled=true
    C) --detailed-monitoring
    D) --enable-detailed-monitoring

51. **Which key pair format is required for Windows instances?**
    A) PEM
    B) PPK
    C) DER
    D) PEM or PPK

52. **Which feature provides hardware isolation for GovCloud workloads?**
    A) Nitro Enclaves
    B) Dedicated Hosts
    C) Dedicated Instances
    D) VPC Endpoints

53. **Which CLI parameter specifies user data script?**
    A) --user-data
    B) --user-script
    C) --init-script
    D) --startup-script

54. **Which service provides container registry for EC2?**
    A) ECR
    B) ECS
    C) EKS
    D) Docker Hub

55. **Which SLA covers EC2 availability?**
    A) 99.99%
    B) 99.9%
    C) 99.5%
    D) 99.0%

56. **Which feature allows control over instance reboot after maintenance?**
    A) Instance Recovery
    B) Reboot Enhancement
    C) Shutdown Behavior
    D) Scheduled Events

57. **Which instance type is ideal for graphic-intensive applications?**
    A) g4dn
    B) c5
    C) t3
    D) m5

58. **Which CloudWatch event rule triggers on instance state changes?**
    A) EC2 Instance State-change Notification
    B) EC2 State Change Events
    C) Instance Lifecycle Events
    D) EC2 Status Checks

59. **Which command enables termination protection?**
    A) modify-instance-attr --disable-api-termination
    B) modify-instance-attr --enable-api-termination
    C) modify-instance-attr --disable-termination-protection
    D) modify-instance-attr --termination-protection true

60. **Which parameter in describe-instances filters by availability zone?**
    A) Name=zone,Values=us-east-1a
    B) Name=availability-zone,Values=us-east-1a
    C) Name=placement,Values=us-east-1a
    D) Name=az,Values=us-east-1a

61. **Which service can clone an EC2 instance?**
    A) AWS Backup
    B) EC2 Image Builder
    C) AWS DMS
    D) AWS Glue

62. **Which command lists instance types with GPU?**
    A) describe-instance-types --filters Name=processor-info.supported-gpus,Values=\*
    B) describe-instance-types --filters Name=gpu,Values=true
    C) describe-instances --filters Name=gpu,Values=true
    D) list-instance-types --gpu

63. **Which parameter sets elastic GPU for an instance?**
    A) --elastic-gpu-specifications
    B) --gpu-type
    C) --accelerator-type
    D) --gpu-specifications

64. **Which feature encrypts data in transit to EBS?**
    A) TLS
    B) IPSec VPN
    C) AWS Certificate Manager
    D) Client-side encryption

65. **Which option defines block device mapping in run-instances?**
    A) --block-device-mappings
    B) --storage-mappings
    C) --device-map
    D) --ebs-mappings

66. **Which parameter filters describe-volumes by attachment instance ID?**
    A) Name=attachment.instance-id,Values=i-0123
    B) Name=attachments,Values=i-0123
    C) Name=volume-id,Values=i-0123
    D) Name=instance-id,Values=i-0123

67. **Which instance metadata option should be required for IMDSv2?**
    A) HttpTokens=optional
    B) HttpTokens=required
    C) HttpPutResponseHopLimit=1
    D) HttpEndpoint=enabled

68. **Which CLI command creates a dedicated host?**
    A) allocate-hosts
    B) create-host
    C) allocate-dedicated-host
    D) provision-host

69. **Which monitoring tool provides OS-level metrics?**
    A) CloudWatch Agent
    B) CloudWatch Logs
    C) CloudTrail
    D) CloudWatch Metrics

70. **Which feature isolates workloads at hardware level?**
    A) Dedicated Hosts
    B) Dedicated Instances
    C) Placement Groups
    D) Nitro Enclaves

71. **Which service can initiate AWS Config for EC2?**
    A) AWS Config Recorder
    B) EC2 Config
    C) CloudTrail
    D) AWS Systems Manager

72. **Which instance reboot type preserves the root device?**
    A) Stop/Start
    B) Reboot
    C) Terminate/Recreate
    D) Force Reboot

73. **Which command creates a launch template?**
    A) create-launch-template
    B) run-launch-template
    C) new-launch-template
    D) put-launch-template

74. **Which instance recommendation tool uses machine learning?**
    A) AWS Trusted Advisor
    B) AWS Compute Optimizer
    C) AWS Cost Explorer
    D) AWS Config

75. **Which option enables termination protection in run-instances?**
    A) --disable-api-termination
    B) --enable-termination-protection
    C) --api-termination-protection
    D) --prevent-termination

76. **Which parameter in describe-images filters by owner?**
    A) Name=owner-alias,Values=self
    B) Name=owner-id,Values=self
    C) Name=owner,Values=self
    D) Name=creator,Values=self

77. **Which AWS service launches instances from snapshots?**
    A) EC2 Restore
    B) AWS Backup
    C) CloudFormation
    D) EC2 Image Builder

78. **Which feature adds a second network interface to an instance?**
    A) ENI
    B) Secondary IP
    C) Elastic Network Interface
    D) eth1 support

79. **Which metric measures bytes transferred in?**
    A) NetworkIn
    B) NetworkOut
    C) DiskReadBytes
    D) DiskWriteBytes

80. **Which feature provides GPU access for SageMaker?**
    A) g4dn instances
    B) p4 instances
    C) inf1 instances
    D) All of the above

81. **Which command allocates an Elastic IP?**
    A) allocate-address
    B) create-elastic-ip
    C) allocate-eip
    D) new-elastic-ip

82. **Which SSH option specifies a different port?**
    A) -p
    B) -P
    C) --port
    D) --ssh-port

83. **Which parameter specifies the AMI ID in run-instances?**
    A) --ami-id
    B) --image-id
    C) --image
    D) --source-ami

84. **Which CLI command stops all running instances?**
    A) stop-instances --all
    B) stop-instances --filters Name=instance-state-name,Values=running
    C) stop-all-instances
    D) terminate-instances --state running

85. **Which service provides managed certificate deployment for instances?**
    A) ACM
    B) IAM
    C) CloudHSM
    D) KMS

86. **Which option defines placement group in run-instances?**
    A) --placement GroupName=my-group
    B) --placement GroupName=my-group,Tenancy=default
    C) --group-name my-group
    D) --placement-group my-group

87. **Which parameter in terminate-instances specifies multiple IDs?**
    A) --instance-id i-1 i-2
    B) --instance-ids i-1 i-2
    C) --ids i-1,i-2
    D) --instances i-1,i-2

88. **Which feature encrypts instance root volume automatically?**
    A) Default EBS encryption
    B) SSE-S3
    C) Client-side encryption
    D) User-data script

89. **Which tool integrates with EC2 for patch compliance reporting?**
    A) AWS Systems Manager Inventory
    B) AWS Config
    C) AWS Inspector
    D) CloudWatch Logs Insights

90. **Which feature minimizes network latency between instances?**
    A) Placement Group
    B) Dedicated Host
    C) VPC Peering
    D) Transit Gateway

91. **Which command describes reserved instances?**
    A) describe-reserved-instances
    B) list-reserved-instances
    C) describe-ris
    D) list-ris

92. **Which tag-based filter can you use in describe-instances?**
    A) Name=tag-key,Values=Name
    B) Name=tag\:Name,Values=MyInstance
    C) Name=tags,Values=MyInstance
    D) Name=tag\_values,Values=MyInstance

93. **Which default VPC component provides NAT?**
    A) Internet Gateway
    B) NAT Gateway
    C) NAT Instance
    D) VPC Endpoint

94. **Which CLI command creates a security group?**
    A) create-security-group
    B) create-sg
    C) new-security-group
    D) run-security-group

95. **Which feature allows unattended instance termination?**
    A) Spot Instances termination
    B) Auto Scaling
    C) Lifecycle Hooks
    D) Health Checks

96. **Which parameter in describe-security-groups filters by group name?**
    A) Name=group-name,Values=my-sg
    B) Name=groupName,Values=my-sg
    C) Name=Name,Values=my-sg
    D) Name=group-name,Values=my-sg

97. **Which option limits the IAM role session duration?**
    A) MaxSessionDuration on role
    B) DurationSeconds on assume-role API
    C) SessionDuration in trust policy
    D) Expiration in instance profile

98. **Which CLI command disassociates an Elastic IP from an instance?**
    A) disassociate-address
    B) release-address
    C) disassociate-eip
    D) remove-elastic-ip

99. **Which instance metadata feature can be disabled?**
    A) Metadata service endpoint
    B) IMDSv2 enforcement
    C) HTTP PUT access
    D) User data retrieval

100. **Which tool provides historical cost data by instance?**
     A) Cost Explorer
     B) AWS Budgets
     C) AWS Pricing Calculator
     D) AWS Cost and Usage Report

---

## Answer Key

1. B
2. C
3. B
4. A
5. D
6. B
7. D
8. C
9. A
10. B
11. C
12. B
13. B
14. B
15. A
16. B
17. B
18. C
19. B
20. C
21. B
22. B
23. C
24. C
25. B
26. C
27. A
28. B
29. B
30. A
31. A
32. C
33. A
34. A
35. B
36. A
37. B
38. A
39. A
40. B
41. B
42. B
43. A
44. A
45. D
46. B
47. A
48. A
49. B
50. B
51. D
52. C
53. A
54. A
55. B
56. D
57. A
58. A
59. A
60. B
61. B
62. A
63. A
64. A
65. A
66. A
67. B
68. A
69. A
70. D
71. A
72. B
73. A
74. B
75. A
76. B
77. C
78. C
79. A
80. D
81. A
82. A
83. B
84. B
85. A
86. B
87. B
88. A
89. A
90. A
91. A
92. B
93. A
94. A
95. A
96. A
97. A
98. A
99. A
100. D
