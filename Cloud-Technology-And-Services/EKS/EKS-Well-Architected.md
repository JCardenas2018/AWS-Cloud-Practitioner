# Amazon EKS Use Cases Aligned with the AWS Well-Architected Framework

Below are concrete examples and patterns for running Amazon EKS clusters mapped to each of the six pillars.

---

## 1. Operational Excellence  
**Automate, observe and continuously improve procedures.**  
- **GitOps Deployment Pipeline**  
  - Store Kubernetes manifests (Helm charts or YAML) in Git.  
  - Use Flux/CD or ArgoCD to automatically apply changes to your EKS cluster.  
- **Infrastructure as Code**  
  - Define EKS cluster, node groups, VPC, and add-ons in Terraform or CloudFormation.  
  - Enable drift detection and automated rollback under detected divergence.  
- **Runbook & Run Exercises**  
  - Publish runbooks in Confluence or S3 for common tasks (node replacement, cluster upgrade).  
  - Schedule GameDays to test failover and recovery processes on EKS.

---

## 2. Security  
**Protect data, systems, and assets.**  
- **IAM Roles for Service Accounts (IRSA)**  
  - Assign S3-read or DynamoDB-write permissions directly to Kubernetes service accounts, avoiding node-wide IAM keys.  
- **Network Policies & Pod Security**  
  - Enforce Calico or AWS VPC CNI network policies to whitelist allowed Pod-to-Pod traffic.  
  - Use Pod Security Admission or OPA Gatekeeper to enforce Pod security contexts (runAsNonRoot, readOnlyRootFilesystem).  
- **Encrypt etcd & EBS**  
  - Enable EKS control plane encryption for secrets at rest.  
  - Use customer-managed KMS keys for EBS volumes attached to worker nodes.

---

## 3. Reliability  
**Recover from failures and meet availability targets.**  
- **Multi-AZ Node Groups**  
  - Deploy managed node groups across at least three Availability Zones.  
  - Tolerate AZ failures with zero downtime for critical deployments.  
- **Cluster Autoscaler**  
  - Install the Kubernetes Cluster Autoscaler to automatically add/remove EC2 nodes based on Pod requests.  
- **Self-Healing with Health Checks**  
  - Configure liveness and readiness probes on all Pods.  
  - Use AWS Fault Injection Simulator to validate recovery capabilities.

---

## 4. Performance Efficiency  
**Use resources effectively to meet system requirements.**  
- **Right-Size Resources**  
  - Monitor Pod CPU/memory metrics via CloudWatch or Prometheus; adjust requests and limits to avoid over-provisioning.  
- **Fargate for Variable Workloads**  
  - Run bursty or unpredictable microservices on Fargate profiles—no pre-provisioned nodes needed.  
- **Custom AMIs & Bottlerocket**  
  - Build optimized node AMIs with Linux kernel tuning (network, CPU cfs settings) or use Bottlerocket for faster boot times and smaller attack surface.

---

## 5. Cost Optimization  
**Avoid unnecessary costs.**  
- **Spot Node Groups**  
  - Run non-critical worker node groups on EC2 Spot Instances with a fallback to On-Demand if capacity is constrained.  
- **Scheduled Node Scaling**  
  - Use EventBridge rules to scale node groups down in off-peak windows (nights/weekends) and back up before the workday.  
- **Fargate Savings Plans**  
  - Commit to Fargate Compute Savings Plans for predictable baseline workloads to save up to 30%.

---

## 6. Sustainability  
**Minimize environmental impact.**  
- **Efficient Binpacking**  
  - Use the Kubernetes Default or Binpacking scheduler to pack Pods tightly onto nodes, reducing idle capacity.  
- **Serverless Pods with Fargate**  
  - Eliminate idle EC2 nodes by using Fargate profiles that scale to zero when no Pods are running.  
- **Optimize Container Images**  
  - Base images on minimal distros (e.g., Alpine or Distroless) to reduce image size, storage footprint, and network transfer energy.

---
