# AWS Compute Optimizer

AWS Compute Optimizer helps you identify optimal configurations for your EC2 instances, Auto Scaling Groups, EBS volumes, and Lambda functions by leveraging machine learning on real usage patterns.

---

## 1. How It Works

1. **Metric Collection**  
   - Gathers metrics from CloudWatch (CPU, memory, disk I/O, network) for at least 14 days.  
2. **ML-Powered Analysis**  
   - Uses machine learning algorithms to detect usage patterns and recommend right-sizing changes.  
3. **Recommendations**  
   - Suggests **downgrade** (cost savings) or **upgrade** (better performance) with estimated monthly savings or improved utilization.

---

## 2. Supported Resources

- **EC2 instances**  
- **Auto Scaling Groups**  
- **EBS volumes**  
- **AWS Lambda functions**  
- **EKS node groups** (preview)  

---

## 3. Recommendation Types

| Resource           | Recommendation Type                          |
|--------------------|----------------------------------------------|
| EC2 / ASG          | Change instance family, size, or generation  |
| EBS                | Change volume type or IOPS                   |
| Lambda             | Adjust memory allocation                     |

---

## 4. AWS CLI Example

1. **Enable Compute Optimizer** (if not already active):

   ```bash
   aws compute-optimizer update-enrollment-status --status Active
