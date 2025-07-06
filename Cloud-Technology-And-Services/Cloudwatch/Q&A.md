# Quiz: AWS CloudWatch, EventBridge, SNS, SQS (100 Questions)

1. Which CloudWatch feature allows you to visualize metrics and alarms in one pane?  
   A. CloudWatch Logs Insights  
   B. CloudWatch Dashboards  
   C. CloudWatch Events  
   D. CloudWatch Contributor Insights  

2. In EventBridge, what is the default event bus for AWS service events?  
   A. Custom Bus  
   B. Partner Bus  
   C. Default Bus  
   D. System Bus  

3. What SNS subscription protocol delivers messages to HTTP endpoints?  
   A. SMS  
   B. Email-JSON  
   C. HTTP/HTTPS  
   D. Mobile Push  

4. Which SQS queue type guarantees exactly-once processing and ordering?  
   A. Standard Queue  
   B. FIFO Queue  
   C. Dead-Letter Queue  
   D. Delay Queue  

5. What CloudWatch alarm state indicates that a threshold has been breached?  
   A. INSUFFICIENT_DATA  
   B. OK  
   C. ALARM  
   D. PENDING  

6. In EventBridge, which resource maps incoming events to targets?  
   A. Rule  
   B. Topic  
   C. Subscription  
   D. Channel  

7. What is the maximum message size for an SQS message?  
   A. 64 KB  
   B. 128 KB  
   C. 256 KB  
   D. 512 KB  

8. Which SNS feature allows filtering messages by attributes?  
   A. Message Encryption  
   B. Message Attributes  
   C. Subscription Filters  
   D. FIFO Topics  

9. In CloudWatch Logs, what query language is used for ad-hoc log searches?  
   A. SQL  
   B. JSONPath  
   C. CloudWatch Logs Insights  
   D. PromQL  

10. What EventBridge feature lets you replay archived events?  
    A. Replay Logs  
    B. Event Replayer  
    C. Archive & Replay  
    D. Event History  

11. Which SQS feature makes a message invisible after it’s received?  
    A. Delay Queue  
    B. Visibility Timeout  
    C. Long Polling  
    D. Dead-Letter Queue  

12. Which CloudWatch metric namespace would you use for custom application metrics?  
    A. AWS/EC2  
    B. AWS/Application  
    C. Custom Namespace  
    D. AWS/CloudWatch  

13. What type of SNS topic preserves message order and duplicates?  
    A. Standard Topic  
    B. FIFO Topic  
    C. Ordered Topic  
    D. Deduplicated Topic  

14. Which EventBridge target can directly invoke a Step Functions state machine?  
    A. AWS Lambda  
    B. Amazon SNS  
    C. AWS Step Functions  
    D. Amazon SQS  

15. How do you reduce empty receives in SQS?  
    A. Increase Visibility Timeout  
    B. Enable Long Polling  
    C. Use FIFO Queues  
    D. Enable DLQ  

16. Which CloudWatch feature uses ML to detect anomalies in metric data?  
    A. Contributor Insights  
    B. Anomaly Detection  
    C. Alarms  
    D. Dashboards  

17. What EventBridge resource is used to catalog event schemas?  
    A. Schema Registry  
    B. Schema Repository  
    C. Event Catalog  
    D. Type Store  

18. Which SNS delivery retry policy is configurable?  
    A. Maximum Receives  
    B. Backoff Function  
    C. Dead-Letter Queue  
    D. Redrive Policy  

19. In SQS, what happens when messages exceed the max receive count?  
    A. They are deleted  
    B. They are moved to a dead-letter queue  
    C. They become visible immediately  
    D. They are archived  

20. Which CloudWatch Logs feature delivers log events to S3?  
    A. Log Subscriptions  
    B. Export Tasks  
    C. Metric Filters  
    D. CloudWatch Agent  

21. What EventBridge scheduling expression type supports cron syntax?  
    A. Rate Expressions  
    B. Cron Expressions  
    C. Time Expressions  
    D. Schedule Patterns  

22. Which SNS protocol is used for mobile push notifications to iOS?  
    A. ADM  
    B. APNS  
    C. FCM  
    D. MPNS  

23. In SQS, how many messages can you receive in a single batch call?  
    A. 1  
    B. 5  
    C. 10  
    D. 20  

24. Which CloudWatch alarm type scales resources automatically?  
    A. Composite Alarm  
    B. Metric Alarm  
    C. Auto Scaling Alarm  
    D. Anomaly Alarm  

25. What is the default retention period for CloudWatch Logs?  
    A. 1 day  
    B. 7 days  
    C. Never expire  
    D. 90 days  

26. In EventBridge, what term describes a third-party SaaS event source?  
    A. Custom Bus  
    B. Partner Event Source  
    C. External Rule  
    D. Integration Source  

27. Which SNS feature ensures secure message publishing?  
    A. HTTPS Endpoints  
    B. VPC Endpoints  
    C. IAM Policies  
    D. Server-Side Encryption  

28. In SQS, what setting delays the visibility of new messages?  
    A. Delay Queue  
    B. Visibility Timeout  
    C. Long Polling  
    D. Redrive Policy  

29. Which CloudWatch metric dimension identifies individual EC2 instances?  
    A. InstanceId  
    B. AutoScalingGroupName  
    C. ClusterName  
    D. NodeId  

30. What EventBridge feature allows you to schedule invocations without CloudWatch Events?  
    A. Scheduled Rules  
    B. Rate Rules  
    C. Cron Rules  
    D. Time Rules  

31. Which SNS protocol supports email notifications?  
    A. Email  
    B. SMS  
    C. HTTP  
    D. Lambda  

32. In SQS, which API call deletes a message after processing?  
    A. DeleteMessage  
    B. RemoveMessage  
    C. PurgeQueue  
    D. AcknowledgeMessage  

33. Which CloudWatch feature aggregates log metrics into alarms?  
    A. Metric Filters  
    B. Log Insights  
    C. Dashboards  
    D. Contributor Insights  

34. What EventBridge component holds the pattern that matches incoming events?  
    A. Target  
    B. Rule Pattern  
    C. Event Pattern  
    D. Filter  

35. Which SNS feature lets you send notifications in multiple languages?  
    A. Message Localization  
    B. Message Attributes  
    C. Topic Policies  
    D. Endpoint Localization  

36. In SQS, what is the maximum message retention period?  
    A. 7 days  
    B. 14 days  
    C. 30 days  
    D. 60 days  

37. Which CloudWatch alarm acts on multiple alarms?  
    A. Composite Alarm  
    B. Metric Alarm  
    C. SNS Alarm  
    D. Event Alarm  

38. In EventBridge, which target supports HTTP invocation of external APIs?  
    A. API Destination  
    B. HTTP Target  
    C. External Endpoint  
    D. Webhook  

39. Which SNS feature delays message delivery by seconds or minutes?  
    A. Delay Seconds  
    B. Delivery Delay  
    C. Delay Queue  
    D. Retention Policy  

40. In SQS, what API call retrieves messages without removing them?  
    A. PeekMessage  
    B. ReceiveMessage  
    C. GetMessage  
    D. BrowseQueue  

41. Which CloudWatch Logs feature creates metrics from log patterns?  
    A. Subscription Filter  
    B. Metric Filter  
    C. Insights Query  
    D. Log Export  

42. What EventBridge feature provides built-in retry logic and backoff?  
    A. Retry Policy  
    B. Dead-Letter Queue  
    C. Target Failure Handling  
    D. Circuit Breaker  

43. Which SNS feature lets you replay stored notifications?  
    A. Message Archiving  
    B. Delivery Logs  
    C. No Replay Feature  
    D. DLQ Replay  

44. In SQS, how do you purge all messages in a queue?  
    A. PurgeQueue  
    B. DeleteQueue  
    C. ClearQueue  
    D. EmptyQueue  

45. Which CloudWatch metric alarm can combine multiple conditions using AND/OR?  
    A. Composite Alarm  
    B. Metric Math Alarm  
    C. Anomaly Alarm  
    D. Threshold Alarm  

46. In EventBridge, how many targets can a single rule have?  
    A. 1  
    B. 5  
    C. 10  
    D. Unlimited  

47. Which SNS delivery protocol can trigger a Lambda function?  
    A. HTTP  
    B. SQS  
    C. Lambda  
    D. Email  

48. In SQS, what is the effect of setting ReceiveMessageWaitTimeSeconds?  
    A. Visibility Timeout  
    B. Delay Queue  
    C. Long Polling  
    D. Redrive Policy  

49. Which CloudWatch feature lets you detect top resource contributors to anomalies?  
    A. Contributor Insights  
    B. Dashboards  
    C. Alarms  
    D. Event Correlation  

50. In EventBridge, which action archives events for future replay?  
    A. Enable Archiving  
    B. Create Archive  
    C. Start Logging  
    D. Enable History  

51. Which SNS feature allows cross-account publishing?  
    A. Topic Policy  
    B. Resource Policy  
    C. Access Control List  
    D. SNS Role  

52. In SQS, how do you move messages that fail processing to a DLQ?  
    A. Set MaxReceiveCount on redrive policy  
    B. Enable DLQ flag  
    C. Use PurgeQueue  
    D. Use Delay Queue  

53. Which CloudWatch Logs component forwards logs in real time to another service?  
    A. Metric Filter  
    B. Subscription Filter  
    C. Dashboards  
    D. Insights  

54. What EventBridge setting ensures delivery failure goes to a dead-letter queue?  
    A. Retry Policy with DLQ ARN  
    B. Target Failure Action  
    C. Enable DLQ  
    D. Configure Redrive  

55. Which SNS feature supports message encryption with customer-managed keys?  
    A. SSL/TLS  
    B. KMS Encryption  
    C. IAM Encryption  
    D. Endpoint Encryption  

56. In SQS, what determines how long a message stays in the queue after a receive without deletion?  
    A. Retention Period  
    B. Visibility Timeout  
    C. Delay Seconds  
    D. MaxReceiveCount  

57. Which CloudWatch component captures operational events and routes them?  
    A. EventBridge  
    B. CloudWatch Logs  
    C. CloudWatch Events  
    D. CloudWatch Alarms  

58. In EventBridge, which component provides schema discovery?  
    A. Schema Registry  
    B. Event Catalog  
    C. Discovery Bus  
    D. Event Library  

59. Which SNS metric tracks the number of messages published to a topic?  
    A. NumberOfMessagesPublished  
    B. PublishCount  
    C. TopicSize  
    D. MessageRate  

60. In SQS, what feature enables delaying the first delivery of a message?  
    A. Delay Queue  
    B. Delay Seconds parameter  
    C. Visibility Timeout  
    D. Long Polling  

61. Which CloudWatch alarm type uses statistical math expressions on multiple metrics?  
    A. Composite Alarm  
    B. Metric Math Alarm  
    C. Anomaly Alarm  
    D. Threshold Alarm  

62. In EventBridge, how can you send events across AWS accounts?  
    A. Cross-Account Rules  
    B. Event Bus Permissions  
    C. Resource Policies  
    D. All of the above  

63. Which SNS feature provides guaranteed message order for FIFO topics?  
    A. SequenceNumber  
    B. MessageGroupId  
    C. DeduplicationId  
    D. Timestamp  

64. In SQS, what is the effect of a ReceiveMessage call with WaitTimeSeconds set to 0?  
    A. Enables long polling  
    B. Short polling (immediate response)  
    C. Visibility Timeout is zero  
    D. Messages deleted immediately  

65. Which CloudWatch Logs feature lets you search logs with patterns?  
    A. Subscription Filter  
    B. Log Insights  
    C. Metric Filter  
    D. Export Task  

66. In EventBridge, which target type allows sending events to Kinesis Data Streams?  
    A. Kinesis Stream Target  
    B. StreamBridge  
    C. EventBridge Stream  
    D. Data Stream Connector  

67. Which SNS feature allows batch publishing of multiple messages in one call?  
    A. PublishBatch  
    B. BatchPublish  
    C. BatchSend  
    D. MultiPublish  

68. In SQS, how do you change the visibility timeout of a single message during processing?  
    A. ChangeMessageVisibility  
    B. UpdateVisibility  
    C. ModifyMessage  
    D. SetVisibility  

69. Which CloudWatch metric dimension applies to Lambda functions?  
    A. FunctionName  
    B. ResourceId  
    C. ContainerName  
    D. ServiceName  

70. In EventBridge, which API call submits custom events?  
    A. PutEvents  
    B. SendEvent  
    C. PostEvent  
    D. PublishEvent  

71. Which SNS feature lets you remove a subscription programmatically?  
    A. Unsubscribe  
    B. DeleteSubscription  
    C. RemoveEndpoint  
    D. CancelSubscription  

72. In SQS, what is the effect of purging a queue?  
    A. Deletes the queue  
    B. Clears all messages in the queue  
    C. Moves messages to DLQ  
    D. Resets Visibility Timeout  

73. Which CloudWatch alarm can alert on metric math expressions?  
    A. Composite Alarm  
    B. Metric Math Alarm  
    C. Basic Alarm  
    D. Anomaly Alarm  

74. In EventBridge, which rule type triggers on a schedule only?  
    A. Event Pattern Rule  
    B. Scheduled Rule  
    C. Rate Rule  
    D. Cron Rule  

75. Which SNS protocol supports JSON-formatted emails?  
    A. SMS  
    B. Email  
    C. Email-JSON  
    D. Mobile Push  

76. In SQS, how are messages identified for deletion?  
    A. MessageId  
    B. ReceiptHandle  
    C. MessageHandle  
    D. DeletionToken  

77. Which CloudWatch feature generates insights from high-cardinality logs?  
    A. Contributor Insights  
    B. Dashboards  
    C. Logs Insights  
    D. Metric Filters  

78. In EventBridge, which resource allows you to set up retry attempts?  
    A. Rule RetryPolicy  
    B. Target RetryPolicy  
    C. Bus RetryPolicy  
    D. Archive RetryPolicy  

79. Which SNS metric shows the number of successful deliveries to HTTP endpoints?  
    A. HTTPDeliveredCount  
    B. NumberOfMessagesDelivered  
    C. HTTPStatusCount  
    D. DeliverySuccessCount  

80. In SQS FIFO queues, which attribute ensures deduplication within a 5-minute window?  
    A. DeduplicationScope  
    B. ContentBasedDeduplication  
    C. MessageDeduplicationId  
    D. GroupDeduplication  

81. Which CloudWatch Logs subscription destination can send data to Lambda?  
    A. Firehose  
    B. Lambda  
    C. Kinesis  
    D. All of the above  

82. In EventBridge, which protocol is used to authenticate API Destinations?  
    A. IAM Role  
    B. OAuth Client Credentials  
    C. API Key  
    D. No Auth Required  

83. Which SNS feature allows you to restrict who can publish to a topic?  
    A. Topic Policy  
    B. Subscription Policy  
    C. Access Control List  
    D. IAM Role  

84. In SQS, what is the default visibility timeout?  
    A. 30 seconds  
    B. 60 seconds  
    C. 120 seconds  
    D. 45 seconds  

85. Which CloudWatch alarm can compare a metric against a static threshold?  
    A. Threshold Alarm  
    B. Anomaly Alarm  
    C. Metric Math Alarm  
    D. Composite Alarm  

86. In EventBridge, what is the maximum archive retention period?  
    A. 7 days  
    B. 90 days  
    C. 1 year  
    D. 5 years  

87. Which SNS protocol requires confirmation before delivering messages?  
    A. SQS  
    B. HTTP  
    C. Email  
    D. Lambda  

88. In SQS, which attribute allows message grouping in FIFO queues?  
    A. MessageGroupId  
    B. GroupId  
    C. QueueGroupId  
    D. BatchGroupId  

89. Which CloudWatch Logs action lets you import VPC Flow Logs?  
    A. Create Log Group  
    B. Create Subscription  
    C. Create Log Stream  
    D. Create Log Resource Policy  

90. In EventBridge, which API returns the list of rules for a bus?  
    A. ListRules  
    B. DescribeRules  
    C. GetRules  
    D. ShowRules  

91. Which SNS delivery protocol supports chunked transfer?  
    A. HTTP  
    B. SMS  
    C. Email  
    D. Lambda  

92. In SQS, what does the ApproximateNumberOfMessagesVisible metric indicate?  
    A. Total messages ever sent  
    B. Messages available for retrieval  
    C. Messages in DLQ  
    D. Messages in flight  

93. Which CloudWatch alarm comparison operator triggers when metric goes below threshold?  
    A. GreaterThanThreshold  
    B. LessThanThreshold  
    C. GreaterThanOrEqualToThreshold  
    D. LessThanOrEqualToThreshold  

94. In EventBridge, which CLI command lists event buses?  
    A. aws events list-event-buses  
    B. aws eventbridge list-buses  
    C. aws events describe-buses  
    D. aws eventbridge describe-buses  

95. Which SNS feature provides message batching for FIFO topics?  
    A. MessageGroupId  
    B. PublishBatch  
    C. BatchDelivery  
    D. ChunkPublish  

96. In SQS, which parameter controls the maximum time to wait for long polling?  
    A. ReceiveMessageWaitTimeSeconds  
    B. PollingTimeout  
    C. WaitTimeSeconds  
    D. LongPollTimeout  

97. Which CloudWatch feature can trigger an AWS Lambda function on specific log patterns?  
    A. Metric Filters  
    B. Log Insights  
    C. Dashboards  
    D. Contributor Insights  

98. In EventBridge, what is the default archive state when you enable archiving?  
    A. Disabled  
    B. Enabled  
    C. Paused  
    D. Active  

99. Which SNS metric tracks the number of messages that failed to deliver?  
    A. NumberOfNotificationsFailed  
    B. NumberOfMessagesFailed  
    C. PublishFailures  
    D. DeliveryFailures  

100. In SQS, which tool helps you move messages between queues for debugging?  
    A. SQS Console Move Feature  
    B. AWS CLI with Receive/Send  
    C. SQS Message Explorer  
    D. Dead-Letter Redrive  

---

## Answers

1. B  
2. C  
3. C  
4. B  
5. C  
6. A  
7. C  
8. C  
9. C  
10. C  
11. B  
12. C  
13. B  
14. C  
15. B  
16. B  
17. A  
18. B  
19. B  
20. B  
21. B  
22. B  
23. C  
24. B  
25. C  
26. B  
27. D  
28. A  
29. A  
30. A  
31. A  
32. A  
33. A  
34. C  
35. B  
36. B  
37. A  
38. A  
39. A  
40. B  
41. B  
42. A  
43. C  
44. A  
45. A  
46. D  
47. C  
48. C  
49. A  
50. B  
51. A  
52. A  
53. B  
54. A  
55. B  
56. B  
57. C  
58. A  
59. A  
60. B  
61. B  
62. D  
63. B  
64. B  
65. B  
66. A  
67. A  
68. A  
69. A  
70. A  
71. A  
72. B  
73. B  
74. B  
75. C  
76. B  
77. A  
78. B  
79. B  
80. C  
81. D  
82. B  
83. A  
84. A  
85. A  
86. C  
87. C  
88. A  
89. A  
90. A  
91. A  
92. B  
93. B  
94. A  
95. B  
96. A  
97. A  
98. D  
99. A  
100. B  
