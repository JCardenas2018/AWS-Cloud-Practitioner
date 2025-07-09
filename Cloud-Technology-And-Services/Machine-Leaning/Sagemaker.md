## AWS SageMaker

### Overview  
Amazon SageMaker is a fully managed service that accelerates the end-to-end machine learning (ML) lifecycle. It enables data scientists and developers to build, train, and deploy ML models at scale without managing underlying infrastructure.

### Key Features  
- **SageMaker Studio**  
  An integrated development environment based on Jupyter, providing notebooks, experiment management, debugging, and model monitoring in one web interface.  
- **Managed Notebooks**  
  On-demand Jupyter notebooks that auto-scale and can be stopped/started to optimize costs.  
- **Distributed Training**  
  Support for single-instance and multi-instance training on CPUs or GPUs using popular frameworks (TensorFlow, PyTorch, MXNet).  
- **Automatic Model Tuning**  
  Hyperparameter optimization using Bayesian, random, and gradient-based search to find the best model settings.  
- **Autopilot**  
  Automatically builds, trains, and tunes the best model pipeline based on your data with minimal configuration.  
- **SageMaker Pipelines**  
  A CI/CD-style workflow service to orchestrate data preparation, training, evaluation, and deployment steps as code.  
- **Model Hosting & Inference**  
  One-click deployment of real-time inference endpoints with auto-scaling, plus batch transform jobs for offline predictions.  
- **Model Monitor**  
  Continuous monitoring of deployed models for data drift, bias, and accuracy degradation.  
- **Ground Truth**  
  A data labeling service that combines human annotation workflows with machine learning to label training datasets efficiently.

### Common Use Cases  
- Image, text, and time-series classification  
- Anomaly detection for IoT or finance  
- Forecasting and demand prediction  
- Natural language processing (sentiment analysis, entity extraction)  
- Recommendation systems  
- Computer vision (object detection, image segmentation)

### Pricing Model  
- **Notebook Instances**: Charged per instance-hour based on instance type (e.g., ml.t3.medium, ml.p3.2xlarge).  
- **Training**: Charged per instance-hour for training jobs and by storage used for training data.  
- **Automatic Model Tuning**: Charged per instance-hour of tuning jobs.  
- **Autopilot**: Charged per instance-hour consumed by each step in the Autopilot pipeline.  
- **Inference Endpoints**: Charged per instance-hour for real-time endpoints and per thousand invocations for serverless endpoints.  
- **Batch Transform Jobs**: Charged per instance-hour and for data processed.

### Security & Compliance  
- **IAM**: Granular policies control access to notebooks, training jobs, models, and endpoints.  
- **VPC Integration**: Launch notebooks and training jobs within your VPC for network isolation.  
- **Encryption**: Data in transit uses TLS; data at rest (EBS volumes, S3 artifacts) encrypted with AWS KMS CMKs.  
- **Audit Logging**: All API calls recorded in AWS CloudTrail.  
- **Certifications**: HIPAA, SOC 1/2/3, ISO 27001, PCI DSS, GDPR, FedRAMP, and more.

### Integrations  
- **Storage**: Amazon S3 for datasets and model artifacts.  
- **Orchestration**: AWS Step Functions and AWS Lambda for serverless ML pipelines.  
- **Containers**: Amazon ECR for custom training and inference containers.  
- **Data Prep & ETL**: SageMaker Data Wrangler, AWS Glue, and Amazon Athena.  
- **CI/CD**: SageMaker Projects with AWS CodePipeline and CodeBuild integration.

### Example: Create a Training Job via AWS CLI  
```bash
aws sagemaker create-training-job \
  --training-job-name my-ml-training-job \
  --algorithm-specification TrainingImage=811284229777.dkr.ecr.us-east-1.amazonaws.com/xgboost:latest,TrainingInputMode=File \
  --role-arn arn:aws:iam::123456789012:role/SageMakerExecutionRole \
  --input-data-config '[{"ChannelName":"train","DataSource":{"S3DataSource":{"S3DataType":"S3Prefix","S3Uri":"s3://my-bucket/train/","AttributeNames":["label"]}},"ContentType":"text/csv"}]' \
  --output-data-config S3OutputPath=s3://my-bucket/output/ \
  --resource-config InstanceType=ml.m5.xlarge,InstanceCount=2,VolumeSizeInGB=50
