# 100 Questions on AWS DevOps Services

## CodePipeline

1. What is the primary purpose of AWS CodePipeline?  
   - A. Store build artifacts  
   - B. Orchestrate continuous delivery workflows  
   - C. Manage Git repositories  
   - D. Deploy EC2 servers  

2. In CodePipeline, what is the component called that groups actions like build and deploy?  
   - A. Stage  
   - B. Phase  
   - C. Job  
   - D. Pipeline  

3. Which CodePipeline action allows you to run automated tests?  
   - A. Build  
   - B. Deploy  
   - C. Test  
   - D. Source  

4. Which of the following is natively supported as a source in CodePipeline?  
   - A. AWS S3, Amazon ECR, AWS CodeCommit  
   - B. GitHub, Bitbucket, GitLab  
   - C. Only AWS S3  
   - D. Azure Repos  

5. How does CodePipeline get notified of a new change in the repository?  
   - A. Periodic polling  
   - B. Webhook  
   - C. Manual Lambda  
   - D. SNS Topic  

6. Which AWS resource is automatically created when you define a Pipeline with CloudFormation?  
   - A. AWS::CodeBuild::Project  
   - B. AWS::CodePipeline::Pipeline  
   - C. AWS::S3::Bucket  
   - D. AWS::IAM::Role  

7. Which of these is not a typical CodePipeline event?  
   - A. PipelineExecutionStarted  
   - B. ApprovalRequired  
   - C. PipelinePaused  
   - D. ExecutionAborted  

8. What is the purpose of a manual approval action in CodePipeline?  
   - A. To run performance tests  
   - B. To block the pipeline until human intervention  
   - C. To notify the team of errors  
   - D. To deploy automatically  

9. What type of artifact does the build stage produce?  
   - A. Source code  
   - B. Packaged artifact ready for deployment  
   - C. Log files  
   - D. CloudFormation template  

10. What is the recommended way to define a Pipeline as code?  
    - A. AWS CLI  
    - B. Web console  
    - C. CloudFormation / CDK  
    - D. Python SDK  

11. Which IAM permission is essential for CodePipeline to read from CodeCommit?  
    - A. codepipeline:GetPipeline  
    - B. codecommit:GitPull  
    - C. codecommit:BatchGet*  
    - D. codepipeline:StartPipelineExecution  

12. How do you integrate CodePipeline with CodeDeploy for automated deployments?  
    - A. By configuring a webhook  
    - B. By adding a CodeDeploy deploy action  
    - C. By invoking an intermediate Lambda  
    - D. Via S3  

13. What happens if a stage fails in CodePipeline?  
    - A. The pipeline continues to the next stage  
    - B. The pipeline pauses and is marked as failed  
    - C. It automatically restarts  
    - D. It is skipped and a notification is sent  

14. What is the versioning unit within a pipeline?  
    - A. Stage  
    - B. Action  
    - C. Pipeline execution  
    - D. Artifact  

15. Which setting controls concurrent pipeline executions?  
    - A. MaximumConcurrentExecutions  
    - B. ParallelExecutionCount  
    - C. ApprovalWaitTime  
    - D. ExecutionLimit  

16. How do you parameterize a pipeline for different repository branches?  
    - A. Environment variables in CodeBuild  
    - B. CloudFormation parameters  
    - C. Pipeline variables  
    - D. It is not possible  

17. What is the AWS CLI command to manually start a pipeline?  
    - A. aws codepipeline release-pipeline  
    - B. aws codepipeline start-pipeline-execution  
    - C. aws codepipeline invoke  
    - D. aws codepipeline run-pipeline  

---

## CodeBuild

18. What file type defines the build phases in CodeBuild?  
    - A. buildspec.xml  
    - B. buildspec.yml  
    - C. Dockerfile  
    - D. pipeline.json  

19. In buildspec.yml, which phase installs dependencies?  
    - A. install  
    - B. pre_build  
    - C. build  
    - D. post_build  

20. Where does CodeBuild store the resulting artifacts?  
    - A. Only in ECR  
    - B. In an S3 bucket or ECR  
    - C. In DynamoDB  
    - D. In CloudWatch Logs  

21. What is the purpose of the post_build phase?  
    - A. Prepare the environment  
    - B. Execute the build  
    - C. Publish artifacts and notify results  
    - D. Install dependencies  

22. Which environment image does AWS CodeBuild manage without customization?  
    - A. Custom Ubuntu  
    - B. Windows Server  
    - C. Standard images provided by AWS  
    - D. Local Docker images  

23. How is the build timeout controlled?  
    - A. timeout-minutes in buildspec.yml  
    - B. Project setting in the console or CloudFormation  
    - C. It is not configurable  
    - D. Timeout in S3  

24. What is a recommended practice for credentials in CodeBuild?  
    - A. Store them in buildspec.yml  
    - B. Use encrypted environment variables in the project  
    - C. Include them in the repository  
    - D. Do not use credentials  

25. How do you enable caching to speed up builds?  
    - A. cache: enable in buildspec.yml  
    - B. Cache configuration in the project (S3 or local)  
    - C. There is no cache  
    - D. Third-party plugin  

26. Which IAM permission must CodeBuild have to send logs to CloudWatch?  
    - A. logs:CreateLogGroup and logs:PutLogEvents  
    - B. cloudwatch:PutMetric  
    - C. s3:PutObject  
    - D. codebuild:UploadLogs  

27. What is the purpose of reports in CodeBuild?  
    - A. Generate PDF logs  
    - B. Show test results (e.g. coverage)  
    - C. Build history  
    - D. Billing metrics  

28. How do you inject a variable at build time?  
    - A. CloudFormation parameters  
    - B. Environment variables in the project or build overrides  
    - C. Comments in buildspec  
    - D. It is not possible  

29. Which command starts a build from the CLI?  
    - A. aws codebuild start-build  
    - B. aws codebuild run  
    - C. aws build start  
    - D. aws codebuild invoke  

30. What happens if a pre_build phase fails?  
    - A. It continues to the build phase  
    - B. It pauses the pipeline  
    - C. The build ends with failure  
    - D. Automatic retry  

31. Which AWS resource defines a CodeBuild project?  
    - A. AWS::CodeBuild::Build  
    - B. AWS::CodeBuild::Project  
    - C. AWS::CodeBuild::Environment  
    - D. AWS::CodePipeline::Action  

32. What is the computeType parameter used for in a project?  
    - A. The type of EC2 instance used for the build  
    - B. Build disk size  
    - C. Linux version  
    - D. Network type  

33. What is the difference between Linux and Windows managed images?  
    - A. Only the underlying OS  
    - B. None  
    - C. Licensing  
    - D. Size  

34. How do you configure a build to build Docker images?  
    - A. buildspec with docker build commands  
    - B. It is not possible  
    - C. Create a specific Docker project  
    - D. Use CodeDeploy  

---

## CodeDeploy

35. Which deployment model minimizes downtime?  
    - A. In-place  
    - B. Blue/Green  
    - C. Rolling  
    - D. Canary  

36. Which resource defines an application in CodeDeploy?  
    - A. AWS::CodeDeploy::Application  
    - B. AWS::CodeDeploy::DeploymentGroup  
    - C. AWS::EC2::Instance  
    - D. AWS::CodeDeploy::DeploymentConfig  

37. Which file guides the hook sequence for EC2/On-Prem deployments?  
    - A. appspec.yml  
    - B. buildspec.yml  
    - C. codedeploy.yml  
    - D. deployspec.json  

38. Which hook allows validation before stopping the old application in an in-place deployment?  
    - A. BeforeInstall  
    - B. AfterInstall  
    - C. ApplicationStop  
    - D. ValidateService  

39. In ECS Blue/Green deployments, which resource manages the traffic?  
    - A. ALB or ELB  
    - B. Route 53  
    - C. CloudFront  
    - D. API Gateway  

40. Which IAM permission must CodeDeploy have to access EC2 instances?  
    - A. ec2:DescribeInstances  
    - B. s3:GetObject  
    - C. codecommit:GitPull  
    - D. iam:PassRole  

41. What does an in-place deployment do with existing instances?  
    - A. It creates new ones  
    - B. It updates the same instances  
    - C. It deletes them all  
    - D. It does not modify them  

42. What is the smallest deployment unit in ECS with CodeDeploy?  
    - A. ECS Service  
    - B. ECS Task  
    - C. ECS Node  
    - D. ECS Cluster  

43. How do you roll back a failed deployment?  
    - A. Manually from the console  
    - B. Automatically if rollback is configured  
    - C. It never rolls back  
    - D. With a Lambda function  

44. Which strategy does CodeDeploy use for rolling updates?  
    - A. Canary  
    - B. In-place  
    - C. Rolling  
    - D. Immutable  

45. Where are revisions stored for CodeDeploy?  
    - A. In S3 or CodeCommit  
    - B. Only in ECR  
    - C. In DynamoDB  
    - D. In API Gateway  

46. Which deployment type does not replace instances, but instead creates new ones?  
    - A. In-place  
    - B. Blue/Green  
    - C. Rolling  
    - D. Canary  

47. Which CloudFormation resource creates a DeploymentGroup?  
    - A. AWS::CodeDeploy::DeploymentGroup  
    - B. AWS::EC2::Instance  
    - C. AWS::AutoScaling::Group  
    - D. AWS::ECS::Service  

---

## CodeArtifact

48. What is the purpose of AWS CodeArtifact?  
    - A. A repository for build artifacts (packages)  
    - B. A continuous delivery pipeline  
    - C. A log storage service  
    - D. A container service  

49. Which package domains does CodeArtifact support?  
    - A. npm, Maven, PyPI, NuGet  
    - B. RubyGems, Composer  
    - C. Only Docker  
    - D. Both A and B  

50. How do you authenticate an npm client with CodeArtifact?  
    - A. aws codeartifact login --tool npm  
    - B. npm install  
    - C. Static credentials in .npmrc  
    - D. No authentication required  

51. Which resource defines a repository in CodeArtifact?  
    - A. AWS::CodeArtifact::Repository  
    - B. AWS::S3::Bucket  
    - C. AWS::ECR::Repository  
    - D. AWS::DynamoDB::Table  

52. Which command retrieves the authentication token?  
    - A. aws codeartifact get-authorization-token  
    - B. aws codeartifact login  
    - C. aws codeartifact fetch-token  
    - D. aws codeartifact auth  

53. How do you share a repository cross-account?  
    - A. IAM policies and resource policies  
    - B. SNS subscription  
    - C. S3 replication  
    - D. VPC peering  

54. Which configuration allows you to mix external repositories?  
    - A. Upstream repositories  
    - B. Cross-region replication  
    - C. External connections  
    - D. Federation  

55. Where do you configure retention of stale packages?  
    - A. Lifecycle policies on the repository  
    - B. Pipeline parameters  
    - C. buildspec.yml  
    - D. There is no retention policy  

56. Which package format is not supported?  
    - A. PyPI  
    - B. Maven  
    - C. RubyGems  
    - D. Docker  

57. How do you update the access policy of a repository?  
    - A. aws codeartifact put-repository-permissions-policy  
    - B. aws codeartifact update-repo  
    - C. aws codeartifact set-policy  
    - D. aws codeartifact grant-access  

---

## CloudFormation

58. What template formats does CloudFormation support?  
    - A. JSON or YAML  
    - B. XML  
    - C. INI  
    - D. Properties files  

59. What is the root section in a CloudFormation template?  
    - A. Resources  
    - B. Parameters  
    - C. Outputs  
    - D. Mappings  

60. What is the purpose of the Parameters section?  
    - A. Define variables for stack creation  
    - B. List created resources  
    - C. Store logs  
    - D. Reference other stacks  

61. Which intrinsic function gets an attribute of a resource?  
    - A. Fn::GetAtt  
    - B. Ref  
    - C. Fn::Join  
    - D. Fn::Sub  

62. How do you define an EC2 resource?  
    - A. AWS::EC2::Instance  
    - B. AWS::Compute::EC2  
    - C. AWS::Instance::EC2  
    - D. AWS::Server::EC2  

63. Which section publishes information after creation?  
    - A. Outputs  
    - B. Mappings  
    - C. Metadata  
    - D. Conditions  

64. What does the Conditions section allow?  
    - A. Create resources conditionally  
    - B. Define parameters  
    - C. Group resources  
    - D. Format strings  

65. How do you update a stack to avoid accidental replacement?  
    - A. DisableRollback  
    - B. ChangeSet  
    - C. UpdatePolicy  
    - D. NoUpdate  

66. What is a ChangeSet?  
    - A. Preview of changes before applying  
    - B. Backup of a stack  
    - C. Secondary template  
    - D. Rollback event  

67. Which CLI command creates a stack?  
    - A. aws cloudformation create-stack  
    - B. aws cfn up  
    - C. aws cf deploy  
    - D. aws stacks create  

68. What does AWS::NoValue indicate when used with Fn::If?  
    - A. Omit the property  
    - B. Delete the resource  
    - C. Default value  
    - D. Error  

69. Which section includes metadata for tools?  
    - A. Metadata  
    - B. Mappings  
    - C. Conditions  
    - D. Globals  

70. Which function concatenates lists?  
    - A. Fn::Join  
    - B. Fn::Select  
    - C. Fn::Split  
    - D. Fn::Merge  

71. How do you nest stacks?  
    - A. AWS::CloudFormation::Stack resource  
    - B. NestedStacks: true  
    - C. UseExports: yes  
    - D. ChildStacks  

72. Which option enables rollbacks?  
    - A. OnFailure=ROLLBACK  
    - B. EnableRollback  
    - C. RollbackEnabled  
    - D. NoRollback  

73. How do you export a value for other stacks?  
    - A. Outputs + Export  
    - B. UseOutputs: true  
    - C. ShareValue: yes  
    - D. CrossStackExports  

74. Which resource defines an S3 bucket?  
    - A. AWS::S3::Bucket  
    - B. AWS::Storage::S3Bucket  
    - C. AWS::Bucket::S3  
    - D. AWS::CloudStorage::Bucket  

75. What does the Mappings section allow?  
    - A. Map static key-based values  
    - B. Import other stacks  
    - C. Define parameters  
    - D. Create conditionals  

76. Which function checks if a parameter is present?  
    - A. Fn::If  
    - B. Fn::Equals  
    - C. Fn::Contains  
    - D. Fn::Not  

77. What is the recommended extension for YAML templates?  
    - A. .yaml  
    - B. .yml  
    - C. .json  
    - D. .cf  

---

## CodeCommit

78. What type of repository does CodeCommit create?  
    - A. AWS-managed Git  
    - B. SVN  
    - C. Mercurial  
    - D. Perforce  

79. Which command clones a CodeCommit repository?  
    - A. git clone https://git-codecommit...  
    - B. aws codecommit clone  
    - C. git checkout  
    - D. aws clone-repo  

80. How are notifications integrated in CodeCommit?  
    - A. SNS  
    - B. SQS  
    - C. Lambda triggers  
    - D. All of the above  

81. Which IAM permission allows pushes to CodeCommit?  
    - A. codecommit:GitPush  
    - B. codecommit:UploadArchive  
    - C. codecommit:Put*  
    - D. codecommit:MergePullRequest  

82. How do you create a webhook in CodeCommit?  
    - A. Console → Repository → Notifications  
    - B. Console → CodePipeline  
    - C. aws codecommit create-webhook  
    - D. aws codecommit put-repo-notifications  

83. Which feature handles protected branches?  
    - A. Approval rules in merge rules  
    - B. Branch policies  
    - C. Git hooks  
    - D. Not supported  

84. What storage backend does CodeCommit use?  
    - A. S3 + DynamoDB  
    - B. EFS  
    - C. RDS  
    - D. S3 only  

85. How do you tag a commit?  
    - A. git tag v1.0  
    - B. git label  
    - C. aws codecommit tag-commit  
    - D. git commit --tag  

86. What is the size limit of a repository?  
    - A. 1 TB  
    - B. 10 GB  
    - C. 50 GB  
    - D. 100 GB  

87. How do you restore a deleted commit?  
    - A. git reflog + git reset  
    - B. aws codecommit restore-commit  
    - C. Console → History → Restore  
    - D. Not possible  

88. Which CI/CD method does CodeCommit natively support?  
    - A. Integration with CodePipeline  
    - B. Integration with Jenkins only  
    - C. It does not integrate  
    - D. AWS CodeStar  

89. How do you encrypt a repository?  
    - A. SSE-KMS on underlying S3  
    - B. Client-side encryption  
    - C. Not encrypted  
    - D. SSE-S3  

90. Which command shows differences between branches?  
    - A. git diff origin/main feature  
    - B. aws codecommit compare-branches  
    - C. git compare  
    - D. aws codecommit diff  

91. How do you configure HTTPS authentication?  
    - A. IAM credentials + credential helper  
    - B. SSH only  
    - C. Static user/password  
    - D. GitHub token  

92. What is the payload of CodeCommit events for SNS?  
    - A. JSON with commit and repository details  
    - B. Plain text  
    - C. XML  
    - D. There is no payload  

93. Does CodeCommit support pre-receive hooks?  
    - A. No  
    - B. Yes, using Lambda  
    - C. Yes, natively  
    - D. Partially  

94. How do you migrate a local Git repository to CodeCommit?  
    - A. git remote add + git push --mirror  
    - B. aws codecommit import-repo  
    - C. aws codecommit migrate  
    - D. Not possible  

95. Which event triggers a CodeCommit notification?  
    - A. Push, pull request, comment  
    - B. Push only  
    - C. Pull request only  
    - D. Comment only  

96. How do you retrieve the SSH URL of the repository?  
    - A. aws codecommit get-repository --query repositoryMetadata.cloneUrlSsh  
    - B. git remote show  
    - C. aws git get-url  
    - D. Console only  

97. What is the branch limit in a repository?  
    - A. No documented limit  
    - B. 1,000  
    - C. 100  
    - D. 10  

98. How do you manage repository access policies?  
    - A. IAM policies or resource policies  
    - B. ACLs in S3  
    - C. Security Groups  
    - D. NACL  

99. Which command shows commit logs in the CLI?  
    - A. git log  
    - B. aws codecommit get-commit-history  
    - C. aws codecommit describe-commits  
    - D. git history  

100. Which option enables automatic merge of pull requests after approval?  
    - A. auto-merge in approval rules  
    - B. ContinuousMerge: true  
    - C. Does not exist  
    - D. aws codecommit enable-auto-merge  

---

## Correct Answers

### CodePipeline
1. B  
2. A  
3. C  
4. A  
5. B  
6. B  
7. C  
8. B  
9. B  
10. C  
11. C  
12. B  
13. B  
14. C  
15. A  
16. C  
17. B  

### CodeBuild
18. B  
19. A  
20. B  
21. C  
22. C  
23. B  
24. B  
25. B  
26. A  
27. B  
28. B  
29. A  
30. C  
31. B  
32. A  
33. A  
34. A  

### CodeDeploy
35. B  
36. A  
37. A  
38. C  
39. A  
40. A  
41. B  
42. B  
43. B  
44. C  
45. A  
46. B  
47. A  

### CodeArtifact
48. A  
49. D  
50. A  
51. A  
52. A  
53. A  
54. A  
55. A  
56. D  
57. A  

### CloudFormation
58. A  
59. A  
60. A  
61. A  
62. A  
63. A  
64. A  
65. C  
66. A  
67. A  
68. A  
69. A  
70. A  
71. A  
72. A  
73. A  
74. A  
75. A  
76. B  
77. A  

### CodeCommit
78. A  
79. A  
80. D  
81. C  
82. A  
83. A  
84. A  
85. A  
86. A  
87. A  
88. A  
89. A  
90. A  
91. A  
92. A  
93. B  
94. A  
95. A  
96. A  
97. A  
98. A  
99. A  
100. A  
