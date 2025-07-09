# 100 AWS AI & ML Services Multiple-Choice Questions

1. Which Amazon Comprehend API operation identifies the dominant language in a text?  
   - A. detect-sentiment  
   - B. detect-dominant-language  
   - C. detect-key-phrases  
   - D. detect-entities  

2. Which API call extracts the most important phrases from text?  
   - A. detect-entities  
   - B. detect-syntax  
   - C. detect-key-phrases  
   - D. detect-sentiment  

3. Which Comprehend feature allows you to train a custom document classification model?  
   - A. Custom Entities  
   - B. Custom Classification  
   - C. Topic Modeling  
   - D. Sentiment Analysis  

4. What Comprehend API returns sentiment scores for POSITIVE, NEGATIVE, NEUTRAL, and MIXED?  
   - A. detect-sentiment  
   - B. detect-entities  
   - C. detect-key-phrases  
   - D. detect-syntax  

5. Which Comprehend API can identify PII data for redaction?  
   - A. detect-pii-entities  
   - B. detect-entities  
   - C. detect-sentiment  
   - D. detect-key-phrases  

6. Which operation starts training a custom Comprehend classifier?  
   - A. create-document-classifier  
   - B. detect-sentiment  
   - C. list-entities  
   - D. update-endpoint  

7. Which Comprehend feature groups documents into topics without labels?  
   - A. Topic Modeling  
   - B. Syntax Analysis  
   - C. Entity Recognition  
   - D. Sentiment Analysis  

8. To keep Comprehend traffic within your VPC, you configure:  
   - A. VPC endpoints  
   - B. Direct Connect  
   - C. NAT Gateway  
   - D. Internet Gateway  

9. Which API returns part-of-speech tags for each token?  
   - A. detect-sentiment  
   - B. detect-entities  
   - C. detect-syntax  
   - D. detect-key-phrases  

10. Comprehend uses which service to encrypt data at rest?  
    - A. AWS KMS  
    - B. Amazon S3  
    - C. AWS Secrets Manager  
    - D. IAM  

11. Which AWS CLI command creates a new Amazon Connect instance?  
    - A. aws connect create-instance  
    - B. aws connect start-instance  
    - C. aws connect launch-center  
    - D. aws connect init-instance  

12. Amazon Connect integrates with which service for conversational chatbots?  
    - A. Amazon Lex  
    - B. Amazon Polly  
    - C. Amazon Transcribe  
    - D. Amazon Translate  

13. Contact flows in Amazon Connect are designed using:  
    - A. a drag-and-drop editor  
    - B. YAML templates  
    - C. AWS SDK calls  
    - D. CloudFormation only  

14. For real-time call transcription in Connect, you use:  
    - A. Amazon Transcribe  
    - B. Amazon Comprehend  
    - C. Amazon Translate  
    - D. Amazon Polly  

15. To analyze customer sentiment in Connect calls, which service do you invoke?  
    - A. Amazon Comprehend  
    - B. Amazon Rekognition  
    - C. AWS Kinesis  
    - D. AWS Lambda  

16. Where does Amazon Connect store call recordings by default?  
    - A. Amazon S3  
    - B. Amazon DynamoDB  
    - C. Amazon RDS  
    - D. Amazon EFS  

17. Which service provides metrics and dashboards for Amazon Connect usage?  
    - A. Amazon CloudWatch  
    - B. AWS X-Ray  
    - C. AWS Config  
    - D. AWS CloudTrail  

18. Which IAM managed policy grants full access to Amazon Connect?  
    - A. AmazonConnectFullAccess  
    - B. AmazonConnectReadOnly  
    - C. AmazonConnectServiceRole  
    - D. AmazonConnectAdmin  

19. Amazon Connect supports which communication channels out of the box?  
    - A. Voice, Chat, and Email  
    - B. Voice only  
    - C. Chat only  
    - D. SMS only  

20. For SAML-based single sign-on in Connect, you set IdentityManagementType to:  
    - A. SAML  
    - B. USERPOOL  
    - C. IAM  
    - D. NONE  

21. Which API call creates a new Amazon Kendra index?  
    - A. create-index  
    - B. create-repository  
    - C. create-search-domain  
    - D. create-cluster  

22. Amazon Kendra charges are based on:  
    - A. Indexing Capacity Units  
    - B. Query count  
    - C. Document size only  
    - D. Data transfer  

23. Kendra’s pre-built connectors include all except:  
    - A. Google Drive  
    - B. SharePoint  
    - C. Salesforce  
    - D. GitHub  

24. To refine search with synonyms in Kendra, you configure:  
    - A. Synonym sets  
    - B. Stop words  
    - C. Custom language model  
    - D. Relevance tuning  

25. Kendra enforces user access control using:  
    - A. IAM and SAML  
    - B. Security Groups  
    - C. VPC ACLs  
    - D. KMS policies  

26. Which Kendra API runs a search query?  
    - A. query  
    - B. search-documents  
    - C. find-items  
    - D. execute-search  

27. Real-time query suggestions in Kendra are provided by:  
    - A. autocomplete-suggestions  
    - B. quick-links  
    - C. hotkeys  
    - D. instant-results  

28. In Kendra, an Index stores:  
    - A. Document metadata and content  
    - B. EC2 instances  
    - C. Lambda functions  
    - D. S3 buckets  

29. To ingest content from S3 into Kendra, you configure a:  
    - A. DataSource of type S3  
    - B. S3 replication rule  
    - C. Kinesis Firehose  
    - D. Data Pipeline  

30. Which Kendra feature lets users filter results by attributes like author or date?  
    - A. Facets  
    - B. Pipelines  
    - C. Streams  
    - D. Collections  

31. Which Amazon Lex V1 API operation creates or updates a bot?  
    - A. put-bot  
    - B. create-bot  
    - C. start-bot  
    - D. build-bot  

32. In Lex, predefined example phrases are called:  
    - A. Sample Utterances  
    - B. Intent Models  
    - C. Prompt Templates  
    - D. Phrase Lists  

33. Lex slot types are used to:  
    - A. Extract parameter values from user input  
    - B. Store conversation state  
    - C. Manage IAM roles  
    - D. Encrypt data at rest  

34. To validate user input in Lex, you use:  
    - A. Lambda code hooks  
    - B. CloudWatch metrics  
    - C. S3 events  
    - D. Kinesis streams  

35. Lex conversational context is maintained using:  
    - A. session attributes  
    - B. environment variables  
    - C. CloudWatch alarms  
    - D. S3 buckets  

36. Which property defines the voice for a Lex voice bot?  
    - A. voiceId  
    - B. speechRate  
    - C. volumeGain  
    - D. languageModel  

37. Lex integrates with Amazon Connect via:  
    - A. Lex bots in contact flows  
    - B. Lambda functions only  
    - C. S3 triggers  
    - D. SNS topics  

38. For multi-turn conversations, Lex uses:  
    - A. Intent fulfillment hooks  
    - B. DynamoDB streams  
    - C. Kinesis Firehose  
    - D. Translate  

39. Lex deprecated operation for real-time text requests is:  
    - A. post-text  
    - B. send-message  
    - C. recognize-text  
    - D. text-query  

40. To remove a bot in Lex V1, you call:  
    - A. delete-bot  
    - B. remove-bot  
    - C. unregister-bot  
    - D. destroy-bot  

41. Which Amazon Personalize API creates a dataset group?  
    - A. create-dataset-group  
    - B. create-recommendation  
    - C. create-schema  
    - D. create-campaign  

42. To import user events for real-time recommendations, use:  
    - A. put-events  
    - B. send-events  
    - C. import-events  
    - D. track-events  

43. A recipe in Personalize defines:  
    - A. an algorithm variant  
    - B. an IAM policy  
    - C. a Lambda function  
    - D. an endpoint type  

44. Which API launches a batch inference job?  
    - A. create-batch-inference-job  
    - B. start-batch-job  
    - C. run-batch-inference  
    - D. begin-batch  

45. To deploy a real-time campaign, call:  
    - A. create-campaign  
    - B. start-campaign  
    - C. deploy-solution  
    - D. launch-campaign  

46. Training a new solution version uses:  
    - A. create-solution-version  
    - B. update-solution  
    - C. train-model  
    - D. build-pipeline  

47. Minimum provisioned TPS for a campaign is specified in:  
    - A. create-campaign  
    - B. create-batch-inference-job  
    - C. create-solution-group  
    - D. create-dataset-import-job  

48. To define user and item schemas, you call:  
    - A. create-schema  
    - B. define-schema  
    - C. put-schema  
    - D. register-schema  

49. Personalize metrics are published to:  
    - A. CloudWatch  
    - B. S3 logs  
    - C. DynamoDB  
    - D. Kinesis Data Streams  

50. To delete a dataset group, use:  
    - A. delete-dataset-group  
    - B. remove-group  
    - C. unregister-dataset-group  
    - D. destroy-group  

51. Which Amazon Polly API operation synthesizes speech from text?  
    - A. synthesize-speech  
    - B. generate-speech  
    - C. speak-text  
    - D. text-to-speech  

52. For fine-grained pronunciation control, Polly uses:  
    - A. SSML  
    - B. JSON templates  
    - C. YAML definitions  
    - D. Lexicons only  

53. Neural voices in Polly are called:  
    - A. NTTS  
    - B. TTS2  
    - C. NVoice  
    - D. DeepSpeech  

54. To define custom pronunciations, you create a lexicon with:  
    - A. put-lexicon  
    - B. create-lexicon  
    - C. import-lexicon  
    - D. define-lexicon  

55. Polly speech marks provide:  
    - A. timestamps and pronunciation data  
    - B. audio levels  
    - C. speaker identification  
    - D. sentiment scores  

56. Output formats supported by Polly include:  
    - A. MP3, OGG, and PCM  
    - B. WAV only  
    - C. FLAC only  
    - D. AAC only  

57. To list available Polly voices, call:  
    - A. list-voices  
    - B. describe-voices  
    - C. get-voices  
    - D. query-voices  

58. Polly can encrypt output stored in S3 using:  
    - A. AWS KMS  
    - B. SSL  
    - C. IAM policies  
    - D. S3ACL  

59. Which service integrates Polly audio with contact flows?  
    - A. Amazon Connect  
    - B. Amazon Lex  
    - C. Amazon Transcribe  
    - D. Amazon Translate  

60. Polly SSML tags allow you to:  
    - A. control emphasis, breaks, and pronunciation  
    - B. analyze sentiment  
    - C. detect entities  
    - D. translate text  

61. Which Amazon Rekognition API detects objects and scenes in an image?  
    - A. detect-labels  
    - B. detect-objects  
    - C. detect-scenes  
    - D. detect-items  

62. To analyze facial attributes like emotion, use:  
    - A. detect-faces  
    - B. index-faces  
    - C. search-faces  
    - D. verify-faces  

63. Which API adds faces to a Rekognition collection?  
    - A. index-faces  
    - B. create-faces  
    - C. add-faces  
    - D. put-faces  

64. To search for a face in a collection, call:  
    - A. search-faces  
    - B. find-face  
    - C. locate-face  
    - D. query-face  

65. Celebrity recognition in Rekognition uses:  
    - A. recognize-celebrities  
    - B. detect-celebrities  
    - C. find-celebrities  
    - D. list-celebrities  

66. Which API extracts text (OCR) from an image?  
    - A. detect-text  
    - B. detect-ocr  
    - C. extract-text  
    - D. read-text  

67. To create a face collection, call:  
    - A. create-collection  
    - B. init-collection  
    - C. make-collection  
    - D. new-collection  

68. To delete an entire collection, use:  
    - A. delete-collection  
    - B. remove-collection  
    - C. clear-collection  
    - D. destroy-collection  

69. For real-time face search in a video stream, you call:  
    - A. start-face-search  
    - B. start-stream-analysis  
    - C. start-face-detect  
    - D. start-video-search  

70. Content moderation labels are returned by:  
    - A. detect-moderation-labels  
    - B. detect-content-labels  
    - C. detect-policy-labels  
    - D. detect-safe-labels  

71. Which SageMaker API creates a training job?  
    - A. create-training-job  
    - B. start-training  
    - C. run-training  
    - D. init-training  

72. To deploy a model for real-time inference, call:  
    - A. create-endpoint  
    - B. deploy-model  
    - C. start-endpoint  
    - D. serve-endpoint  

73. Which API launches a managed Jupyter notebook?  
    - A. create-notebook-instance  
    - B. start-notebook  
    - C. init-notebook  
    - D. open-notebook  

74. To perform hyperparameter tuning, you use:  
    - A. create-hyper-parameter-tuning-job  
    - B. create-tuning-job  
    - C. start-tuning  
    - D. tune-parameters  

75. SageMaker Autopilot automatically creates pipelines via:  
    - A. create-auto-ml-job  
    - B. create-pipeline  
    - C. build-pipeline  
    - D. start-autopilot  

76. To host custom container images, store them in:  
    - A. Amazon ECR  
    - B. S3  
    - C. DockerHub  
    - D. CodeCommit  

77. For continuous model quality checks, use:  
    - A. create-monitoring-schedule  
    - B. create-quality-job  
    - C. start-model-monitor  
    - D. init-monitoring  

78. SageMaker Pipelines workflows are defined using:  
    - A. AWS SDK or CloudFormation (Pipeline definitions)  
    - B. Step Functions only  
    - C. CodeBuild  
    - D. Lambda  

79. To label data with a human workforce, call:  
    - A. create-labeling-job  
    - B. start-labeling  
    - C. begin-annotation  
    - D. init-label-job  

80. Model artifacts and training data are typically stored in:  
    - A. Amazon S3  
    - B. DynamoDB  
    - C. EFS  
    - D. EBS  

81. Which Textract API extracts printed text and handwriting?  
    - A. detect-document-text  
    - B. detect-text  
    - C. analyze-document  
    - D. get-text  

82. To extract tables and form fields, use:  
    - A. analyze-document  
    - B. detect-text  
    - C. detect-forms  
    - D. extract-fields  

83. For asynchronous document analysis, you start with:  
    - A. start-document-analysis  
    - B. start-text-detection  
    - C. start-async-job  
    - D. start-analysis  

84. Textract asynchronous jobs notify completion via:  
    - A. SNS  
    - B. S3 events  
    - C. Lambda triggers  
    - D. CloudWatch Events  

85. To query specific values from a form, use Textract’s:  
    - A. Queries API  
    - B. Key-value API  
    - C. Search API  
    - D. Form API  

86. To detect only plain text without structure, call:  
    - A. detect-document-text  
    - B. analyze-document  
    - C. detect-text  
    - D. extract-text  

87. Textract integrates with Amazon Comprehend for:  
    - A. sentiment and entity analysis on extracted text  
    - B. image moderation  
    - C. translation  
    - D. face recognition  

88. Which Textract feature reconstructs table geometry?  
    - A. Table blocks in analyze-document  
    - B. TableExtraction API  
    - C. detect-tables  
    - D. parse-tables  

89. For handwriting-heavy forms, you should use:  
    - A. detect-document-text  
    - B. detect-text  
    - C. analyze-document  
    - D. query-document  

90. Textract results can be stored in S3 and processed by:  
    - A. Lambda functions  
    - B. DynamoDB Streams  
    - C. EC2 instances only  
    - D. Beanstalk  

91. Which API starts a batch transcription job?  
    - A. start-transcription-job  
    - B. create-transcription  
    - C. begin-transcription  
    - D. launch-transcription  

92. For real-time streaming transcription, use:  
    - A. start-stream-transcription  
    - B. start-live-transcribe  
    - C. create-stream-job  
    - D. open-stream  

93. To enable speaker identification, set ShowSpeakerLabels to true in:  
    - A. Transcription job settings  
    - B. Vocabulary settings  
    - C. Language model settings  
    - D. Output format settings  

94. For custom vocabularies in Transcribe, you call:  
    - A. create-vocabulary  
    - B. put-vocabulary  
    - C. define-vocabulary  
    - D. import-vocabulary  

95. Channel identification (agent vs. customer) is enabled with:  
    - A. channel-identification  
    - B. ShowSpeakerLabels  
    - C. MediaChannel  
    - D. SpeakerChannel  

96. Which API translates text between languages in Amazon Translate?  
    - A. translate-text  
    - B. start-translation-job  
    - C. batch-translate  
    - D. get-translation  

97. To run a batch translation job, use:  
    - A. start-text-translation-job  
    - B. create-translate-batch  
    - C. launch-batch-translate  
    - D. batch-translate-text  

98. Custom glossaries in Translate are imported with:  
    - A. import-terminology  
    - B. create-glossary  
    - C. put-terminology  
    - D. add-glossary  

99. Amazon Translate automatically detects source language when you set SourceLanguageCode to:  
    - A. auto  
    - B. auto-detect  
    - C. detect-language  
    - D. auto-language  

100. Translate real-time API pricing is based on:  
    - A. per million characters translated  
    - B. per request  
    - C. per hour of usage  
    - D. per GB of data  

---

## Answers

1. B  
2. C  
3. B  
4. A  
5. A  
6. A  
7. A  
8. A  
9. C  
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
23. D  
24. A  
25. A  
26. A  
27. A  
28. A  
29. A  
30. A  

31. A  
32. A  
33. A  
34. A  
35. A  
36. A  
37. A  
38. A  
39. A  
40. A  

41. A  
42. A  
43. A  
44. A  
45. A  
46. A  
47. A  
48. A  
49. A  
50. A  

51. A  
52. A  
53. A  
54. A  
55. A  
56. A  
57. A  
58. A  
59. A  
60. A  

61. A  
62. A  
63. A  
64. A  
65. A  
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
76. A  
77. A  
78. A  
79. A  
80. A  

81. A  
82. A  
83. A  
84. A  
85. A  
86. A  
87. A  
88. A  
89. C  
90. A  

91. A  
92. A  
93. A  
94. A  
95. A  
96. A  
97. A  
98. A  
99. A  
100. A  
