# 30 AWS Systems Manager Multiple-Choice Questions

1. Which Systems Manager feature provides hierarchical storage for configuration data and secrets?  
   - A. Secrets Manager  
   - B. Parameter Store  
   - C. Config Store  
   - D. Credential Manager  

2. What feature allows you to open a secure, browser-based shell session to an instance without SSH or RDP?  
   - A. Run Command  
   - B. Session Manager  
   - C. State Manager  
   - D. Maintenance Windows  

3. Which API operation executes a script or command on one or more instances?  
   - A. SendCommand  
   - B. RunScript  
   - C. ExecuteAutomation  
   - D. StartSession  

4. Which CloudFormation resource type defines a State Manager association?  
   - A. AWS::SSM::Document  
   - B. AWS::SSM::Association  
   - C. AWS::SSM::MaintenanceWindow  
   - D. AWS::SSM::Parameter  

5. Which Systems Manager document runs OS patching tasks?  
   - A. AWS-ApplyPatchBaseline  
   - B. AWS-RunPatchTasks  
   - C. AWS-PatchManager  
   - D. AWS-InstallPatches  

6. Which document type must you set to use Automation runbooks?  
   - A. Command  
   - B. Automation  
   - C. Session  
   - D. Package  

7. Which feature automatically collects OS and application inventory from managed instances?  
   - A. Inventory  
   - B. State Manager  
   - C. Run Command  
   - D. Distributor  

8. Which CloudFormation resource type schedules maintenance tasks in Systems Manager?  
   - A. AWS::SSM::MaintenanceWindow  
   - B. AWS::SSM::TaskSchedule  
   - C. AWS::SSM::CronJob  
   - D. AWS::SSM::Association  

9. Which feature packages and deploys your own or third-party software to instances?  
   - A. Distributor  
   - B. State Manager  
   - C. Inventory  
   - D. OpsCenter  

10. Which feature provides a centralized console for tracking operational issues (OpsItems)?  
    - A. OpsCenter  
    - B. CloudWatch Events  
    - C. Incident Manager  
    - D. EventBridge  

11. What is the maximum size of a Standard parameter value in Parameter Store?  
    - A. 4 KB  
    - B. 8 KB  
    - C. 4 MB  
    - D. 256 KB  

12. What is the maximum size of an Advanced parameter value in Parameter Store?  
    - A. 4 KB  
    - B. 8 KB  
    - C. 64 KB  
    - D. 256 KB  

13. Which AWS service can trigger actions when a parameter value changes in Parameter Store?  
    - A. Amazon EventBridge (CloudWatch Events)  
    - B. Amazon SNS  
    - C. Amazon S3 Notifications  
    - D. AWS CloudTrail  

14. Which document name starts a port-forwarding session in Session Manager?  
    - A. AWS-StartSession  
    - B. AWS-CreatePortForwarding  
    - C. AWS-SSMSessionPort  
    - D. AWS-StartPortForwardingSession  

15. Where can Session Manager session data be logged?  
    - A. Amazon CloudWatch Logs  
    - B. Amazon S3  
    - C. Both A and B  
    - D. EC2 Instance Storage  

16. To restrict which instances a user can access with Session Manager, you configure:  
    - A. Security Groups  
    - B. IAM resource-level permissions on `ssm:StartSession`  
    - C. VPC endpoint policies  
    - D. Network ACLs  

17. What is the default patch baseline name provided by Patch Manager?  
    - A. AWS-Windows-DefaultPatchBaseline  
    - B. AWS-DefaultPatchBaseline  
    - C. AWS-PatchBaseline-Default  
    - D. AWS-ApplyBaseline  

18. Which CLI command initiates an Automation runbook?  
    - A. `aws ssm run-automation`  
    - B. `aws ssm start-automation`  
    - C. `aws ssm start-automation-execution`  
    - D. `aws ssm execute-automation`  

19. What agent must be installed on servers to enable Systems Manager features?  
    - A. AWS SSM Agent  
    - B. AWS Config Agent  
    - C. CloudWatch Agent  
    - D. AWS Inspector Agent  

20. Which feature uses cron or rate expressions to schedule tasks?  
    - A. Maintenance Windows  
    - B. State Manager  
    - C. Parameter Store  
    - D. Inventory  

21. Which document type is used by Distributor to deploy software packages?  
    - A. Command  
    - B. Package  
    - C. Automation  
    - D. Session  

22. Which API operation creates an OpsCenter item?  
    - A. CreateOpsItem  
    - B. CreateIncident  
    - C. PutOpsItem  
    - D. AddOpsItem  

23. Patch Manager supports patching for which operating systems?  
    - A. Windows only  
    - B. Linux only  
    - C. Windows and Linux  
    - D. macOS  

24. Which feature continuously enforces a desired configuration state on instances?  
    - A. State Manager  
    - B. Run Command  
    - C. Maintenance Windows  
    - D. Inventory  

25. Which service should you use for automatic rotation of secrets instead of Parameter Store?  
    - A. AWS CloudTrail  
    - B. AWS Secrets Manager  
    - C. AWS KMS  
    - D. AWS IAM  

26. Which encryption mechanism does Parameter Store use for encrypted values?  
    - A. AES-256 with AWS-managed keys  
    - B. Customer-managed AWS KMS keys  
    - C. SSL/TLS in transit  
    - D. Hardware HSM  

27. Which CLI command retrieves all parameters under a specific path?  
    - A. `get-parameters`  
    - B. `get-parameters-by-path`  
    - C. `describe-parameters`  
    - D. `list-parameters`  

28. Which `schemaVersion` is used in SSM documents for Run Command?  
    - A. `2.2`  
    - B. `1.0`  
    - C. `3.0`  
    - D. `2.0`  

29. Which document name installs Windows updates via Run Command?  
    - A. AWS-InstallWindowsUpdates  
    - B. AWS-ApplyPatchBaseline  
    - C. AWS-InstallPatches  
    - D. AWS-RunPatchInstallation  

30. Which feature can aggregate inventory data across multiple accounts and Regions?  
    - A. Resource Data Sync  
    - B. OpsCenter  
    - C. Maintenance Windows  
    - D. Automation  

---

## Answers

1. B  
2. B  
3. A  
4. B  
5. A  
6. B  
7. A  
8. A  
9. A  
10. A  
11. A  
12. B  
13. A  
14. D  
15. C  
16. B  
17. B  
18. C  
19. A  
20. A  
21. B  
22. A  
23. C  
24. A  
25. B  
26. B  
27. B  
28. A  
29. A  
30. A  
