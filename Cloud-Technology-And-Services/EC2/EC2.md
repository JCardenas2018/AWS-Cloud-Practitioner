# Amazon EC2 (Elastic Compute Cloud)

## 1. What is Amazon EC2?

Amazon Elastic Compute Cloud (EC2) provides resizable compute capacity in the cloud. You can launch virtual servers (instances) on-demand, with a variety of CPU, memory, storage, and network configurations.

## 2. Key Features

* **Instance Types & Families**
  • **General Purpose** (e.g., t3, m6g) – Balanced CPU, memory

  • **Compute Optimized** (e.g., c6g, c5) – High CPU performance

  • **Memory Optimized** (e.g., r6g, x1e) – High memory capacity

  • **Storage Optimized** (e.g., i3, d3en) – High-speed local storage

  • **Accelerated Computing** (e.g., p4, inf1) – GPUs and FPGAs

* **Elasticity & Scaling**
  • **Auto Scaling Groups** automatically scale capacity based on demand.
  • **On-Demand, Reserved, Spot** pricing options for cost control.

* **Custom AMIs**
  • Create Amazon Machine Images (AMIs) to capture configured OS, applications, and data.
  • Share and reuse AMIs across accounts.

* **Storage Options**
  • **EBS volumes** (gp3, io2) for persistent block storage.
  • **Instance store** for ephemeral, high-performance local storage.

* **Networking & Security**
  • **VPC Integration** – Launch instances within your Virtual Private Cloud.
  • **Security Groups & NACLs** – Stateful and stateless traffic filtering.
  • **Elastic IPs**, **ENIs**, **Placement Groups** for high availability and network performance.

* **Monitoring & Management**
  • **CloudWatch** metrics and alarms.
  • **CloudTrail** logs for API activity.
  • **Systems Manager** for patching, run commands, and inventory.

## 3. Pricing Models

* **On-Demand**: Pay per second (Linux) or per hour (Windows) without long-term commitments.
* **Reserved Instances**: Up to 75% discount for 1- or 3-year terms (Standard, Convertible RIs).
* **Savings Plans**: Flexible hourly usage commitment with compute savings.
* **Spot Instances**: Up to 90% discount on spare capacity; ideal for fault-tolerant workloads.

## 4. Common Use Cases

* **Web & Application Servers**: Scalable front-end and back-end compute.
* **Batch Processing**: High-throughput computing tasks on Spot fleets.
* **Machine Learning**: GPU-based training and inference (P4, G4 instances).
* **Big Data & Analytics**: Hadoop/Spark clusters on EC2 nodes.
* **High Performance Computing (HPC)**: Placement Groups for low-latency interconnect.

## 5. Example: AWS CLI

```bash
# 1. Launch a t3.micro instance
aws ec2 run-instances \
  --image-id ami-0abcdef1234567890 \
  --instance-type t3.micro \
  --key-name MyKeyPair \
  --security-group-ids sg-0123456789abcdef0 \
  --subnet-id subnet-0123456789abcdef0 \
  --tag-specifications 'ResourceType=instance,Tags=[{Key=Name,Value=MyInstance}]'

# 2. Describe running instances
aws ec2 describe-instances --filters Name=instance-state-name,Values=running

# 3. Terminate an instance
aws ec2 terminate-instances --instance-ids i-0123456789abcdef0
```

## 6. Example: Python (boto3)

```python
import boto3

ec2 = boto3.resource('ec2', region_name='us-east-1')

# Launch an instance
def launch_instance():
    instance = ec2.create_instances(
        ImageId='ami-0abcdef1234567890',
        InstanceType='t3.micro',
        MinCount=1,
        MaxCount=1,
        KeyName='MyKeyPair',
        SecurityGroupIds=['sg-0123456789abcdef0'],
        TagSpecifications=[{
            'ResourceType': 'instance',
            'Tags': [{'Key': 'Name', 'Value': 'MyInstance'}]
        }]
    )
    print(f'Launched instance ID: {instance[0].id}')

# Stop an instance
def stop_instance(instance_id):
    ec2.Instance(instance_id).stop()
    print(f'Stopping instance {instance_id}')

# Example usage
if __name__ == '__main__':
    launch_instance()
```

## 7. Best Practices

* **Use IAM Roles**: Assign least-privilege roles to instances, avoid embedding credentials.
* **Enable Detailed Monitoring**: Collect 1-minute metrics for critical workloads.
* **Automate Patching**: Use AWS Systems Manager Patch Manager.
* **Leverage Auto Scaling**: Define scaling policies based on CPU, memory, or custom metrics.
* **Use Placement Groups**: For HPC or latency-sensitive applications.
* **Secure Networking**: Restrict inbound/outbound with Security Groups and NACLs.

## 8. References

* [Amazon EC2 User Guide](https://docs.aws.amazon.com/ec2/index.html)
* [EC2 Pricing](https://aws.amazon.com/ec2/pricing/)
* [EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/)
* [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)
