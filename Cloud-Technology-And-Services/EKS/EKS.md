# Amazon Elastic Kubernetes Service (EKS) Cluster

## 1. What Is an EKS Cluster?  
An Amazon EKS Cluster is a managed Kubernetes control plane and associated worker nodes (data plane) that make it easy to deploy, manage, and scale containerized applications using Kubernetes on AWS. AWS runs and scales the control plane components (API server, etcd, controller manager) across multiple Availability Zones for high availability.

---

## 2. Core Components

| Component                 | Description                                                                                                          |
|---------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Control Plane**         | API server, etcd datastore, controller manager, scheduler—fully managed by AWS and spread across AZs                  |
| **Data Plane (Node Group)** | Worker nodes running in your VPC (EC2 instances or Fargate) that actually run your Pods                              |
| **Managed Node Groups**   | AWS-managed EC2 Auto Scaling groups preconfigured with the EKS AMI and kubelet                                         |
| **Self-Managed Nodes**    | EC2 instances you provision and register yourself; gives full control over AMI and kubelet configuration              |
| **Fargate Profiles**      | Serverless compute for Pods—no EC2 instances to manage, billed per vCPU & memory usage                               |
| **Cluster Endpoint**      | Secure HTTPS endpoint (public or private) to communicate with the Kubernetes API                                      |
| **Cluster Autoscaler**    | Kubernetes component that automatically adjusts the size of your node groups based on Pod resource requests           |

---

## 3. Networking & Security

- **VPC & Subnets**  
  Deploy worker nodes in private/public subnets; control plane uses elastic network interfaces in your VPC.  
- **Security Groups & NACLs**  
  Tighten network traffic between control plane, nodes, and services.  
- **IAM Roles & Service Accounts (IRSA)**  
  Use IAM Roles for Kubernetes Service Accounts via OIDC to grant least-privilege AWS permissions to Pods.  
- **Encryption & Secrets**  
  - Enable etcd encryption at rest.  
  - Integrate with AWS Secrets Manager or SSM Parameter Store for injecting secrets.  
- **Control Plane Logging**  
  Enable API, audit, authenticator, controller-manager, and scheduler logs to CloudWatch.

---

## 4. Observability & Monitoring

- **CloudWatch Container Insights**  
  Collect metrics (CPU, memory, disk, network) and logs from nodes and Pods.  
- **Prometheus & Grafana**  
  Deploy Prometheus Operator on EKS for custom metrics; visualize with Grafana.  
- **Fluentd / Fluent Bit**  
  Stream application logs to CloudWatch Logs, Elasticsearch, or S3.

---

## 5. Scaling & Availability

- **Managed Node Group Auto Scaling**  
  Define minimum, maximum, and desired sizes; integrates with Cluster Autoscaler.  
- **Fargate for Bursty or Lightweight Workloads**  
  Automatically launches Pods on AWS Fargate, scaling to zero when idle.  
- **Multi-AZ Deployment**  
  Spread nodes across at least two Availability Zones to tolerate AZ failures.  
- **Horizontal Pod Autoscaler (HPA)**  
  Scale Pods based on CPU/memory or custom metrics.

---

## 6. Common Use Cases

- **Microservices Architecture**  
  Independently deploy, scale, and update services using Kubernetes primitives.  
- **Batch & Data Processing**  
  Use Kubernetes Jobs and CronJobs for ETL, ML training, or data pipelines.  
- **Hybrid & On-Premises**  
  Extend workloads to on-prem or other clouds with EKS Anywhere.  
- **CI/CD Pipelines**  
  Run dynamic build and test environments as Pods using Fargate Spot to save cost.

---

## 7. Best Practices

1. **Least-Privilege IAM**  
   Grant minimal AWS permissions to both node and Pod identities.  
2. **Version & Patch Management**  
   Keep control plane and worker nodes up to date; test upgrades in dev clusters first.  
3. **Network Policies**  
   Enforce Pod-to-Pod and Pod-to-Service traffic rules using Calico or AWS VPC CNI policies.  
4. **Secure Endpoints**  
   Use private API server endpoints and whitelist CIDR ranges for kubectl access.  
5. **Resource Requests & Limits**  
   Define CPU/memory requests and limits on every Pod to enable effective binpacking and autoscaling.  
6. **Backup & Disaster Recovery**  
   Regularly back up etcd (e.g., with Velero) and snapshot persistent volumes.

---

*With these fundamentals, you can design, deploy, and operate highly available, secure, and cost-effective Kubernetes clusters on AWS using Amazon EKS.*  
