# Quiz: Amazon EKS (30 Questions)

1. Which EKS component exposes the Kubernetes API endpoint?  
   A. Worker Nodes  
   B. Control Plane Endpoint  
   C. Node Group  
   D. Cluster Autoscaler  

2. What AWS service allows you to run Pods without managing EC2 nodes?  
   A. EKS Anywhere  
   B. AWS Fargate  
   C. AWS Batch  
   D. AWS Lambda  

3. What is the main purpose of Managed Node Groups in EKS?  
   A. Automatic management of EC2 worker nodes  
   B. Provisioning storage for Pods  
   C. Centralized logging  
   D. DNS management  

4. Which network protocol does the AWS VPC CNI plugin use to connect Pods?  
   A. VXLAN  
   B. IP over ENI  
   C. GRE  
   D. IPSec  

5. Which Kubernetes resource automatically adjusts the number of EC2 nodes?  
   A. HorizontalPodAutoscaler  
   B. Cluster Autoscaler  
   C. DaemonSet  
   D. StatefulSet  

6. What are Fargate Profiles used for in EKS?  
   A. Configuring Managed Node Groups  
   B. Defining which Pods run on Fargate  
   C. Setting logging levels  
   D. Managing Security Groups  

7. How do you enable IAM Roles for Service Accounts (IRSA) in EKS?  
   A. Attach an IAM role to each EC2 node  
   B. Associate an OIDC provider and annotate the ServiceAccount  
   C. Use instance profiles only  
   D. Enable multi-factor authentication  

8. What advantage does Bottlerocket provide as an operating system for EKS nodes?  
   A. Familiar Linux userland  
   B. Smaller attack surface and optimized for containers  
   C. Windows compatibility  
   D. Hourly automatic patching  

9. Which Kubernetes object defines the minimum and maximum replicas for a Deployment?  
   A. ReplicaSet  
   B. StatefulSet  
   C. HorizontalPodAutoscaler  
   D. DaemonSet  

10. Which type of subnets is recommended for production EKS worker nodes?  
    A. Public subnets  
    B. Private subnets  
    C. Transit subnets  
    D. NAT-only subnets  

11. What is the primary function of the Cluster Autoscaler in EKS?  
    A. Scale Pods horizontally  
    B. Adjust the size of node groups based on Pod demands  
    C. Manage Service discovery  
    D. Provide load balancing  

12. Which block storage service is commonly used for persistent volumes in EKS?  
    A. Amazon S3  
    B. Amazon EBS  
    C. Amazon DynamoDB  
    D. Amazon FSx  

13. Which AWS service allows ingesting and visualizing container metrics from EKS?  
    A. AWS CloudTrail  
    B. CloudWatch Container Insights  
    C. AWS X-Ray  
    D. AWS Config  

14. Which ConfigMap maps IAM identities to Kubernetes RBAC in EKS?  
    A. kube-proxy ConfigMap  
    B. aws-auth ConfigMap  
    C. coredns ConfigMap  
    D. kubelet ConfigMap  

15. Which Kubernetes resource type creates an AWS Load Balancer for a Service in EKS?  
    A. Ingress  
    B. Service of type LoadBalancer  
    C. Deployment  
    D. EndpointSlice  

16. How can you restrict access to the EKS control plane to specific IP addresses?  
    A. Use security groups on the worker nodes  
    B. Whitelist CIDR blocks on the public endpoint configuration  
    C. Use VPC endpoints for the control plane  
    D. Apply IAM policies  

17. Which popular GitOps tool integrates with EKS for automated deployments?  
    A. Jenkins  
    B. Ansible  
    C. Flux CD  
    D. Puppet  

18. What is the purpose of a DaemonSet in an EKS cluster?  
    A. Run one Pod on each node for logging or monitoring  
    B. Automatically scale Pods  
    C. Manage Secrets  
    D. Provide Stateful storage  

19. Which EKS feature allows you to run the Kubernetes API endpoint only within your private network?  
    A. Public endpoint only  
    B. Private endpoint configuration  
    C. VPC peering  
    D. NAT Gateway  

20. How do you perform a safe Kubernetes version upgrade on EKS?  
    A. Delete and recreate the cluster  
    B. Upgrade the control plane, then node groups, testing in dev first  
    C. Upgrade worker nodes only  
    D. Directly patch etcd  

21. Which authentication method does `kubectl` use to authenticate with EKS?  
    A. OIDC client library  
    B. AWS IAM Authenticator plugin  
    C. SSH key authentication  
    D. Basic HTTP auth  

22. What is the primary purpose of the AWS Load Balancer Controller in EKS?  
    A. Manage EBS volumes  
    B. Provision AWS Load Balancers for Kubernetes Ingress resources  
    C. Control Auto Scaling  
    D. Provide DNS management  

23. What is the main cost benefit of using Spot Instances for EKS worker nodes?  
    A. Guaranteed uptime  
    B. Up to 90% cost savings  
    C. Automatic hardware upgrades  
    D. Higher networking performance  

24. Which Kubernetes resource should you use to inject AWS Secrets Manager secrets into Pods?  
    A. Secret  
    B. ConfigMap  
    C. ExternalSecret (via Kubernetes External Secrets)  
    D. PersistentVolume  

25. How can you enforce network policies between Pods in EKS?  
    A. Only via Security Groups  
    B. Using NetworkPolicy objects with a compatible CNI plugin  
    C. Managing route tables  
    D. Through IAM roles  

26. What IAM component do EKS worker nodes require to launch AWS resources?  
    A. An IAM user  
    B. An Instance Profile  
    C. An Access Key ID  
    D. A Service Control Policy  

27. Which backup tool is commonly used to back up volumes and etcd in EKS?  
    A. Velero  
    B. AWS Backup  
    C. CloudTrail  
    D. DataSync  

28. How do you define a scheduled CronJob in Kubernetes on EKS?  
    A. Use a Job with a schedule field  
    B. Use the CronJob resource in YAML  
    C. Annotate a Deployment with a cron expression  
    D. Configure a ConfigMap with a cron schedule  

29. Which metrics should you monitor to right-size CPU and memory in an EKS cluster?  
    A. Disk I/O utilization  
    B. Pod CPU and memory usage  
    C. Network packet rates  
    D. Number of nodes  

30. Which security best practice enforces running containers as non-root users in EKS?  
    A. Set `runAsRoot: false`  
    B. Use `securityContext.runAsNonRoot: true` in Pod specs  
    C. Enable SELinux only  
    D. Apply PodSecurityPolicy only  

---

## Answers

1. B. Control Plane Endpoint  
2. B. AWS Fargate  
3. A. Automatic management of EC2 worker nodes  
4. B. IP over ENI  
5. B. Cluster Autoscaler  
6. B. Defining which Pods run on Fargate  
7. B. Associate an OIDC provider and annotate the ServiceAccount  
8. B. Smaller attack surface and optimized for containers  
9. C. HorizontalPodAutoscaler  
10. B. Private subnets  
11. B. Adjust the size of node groups based on Pod demands  
12. B. Amazon EBS  
13. B. CloudWatch Container Insights  
14. B. aws-auth ConfigMap  
15. B. Service of type LoadBalancer  
16. B. Whitelist CIDR blocks on the public endpoint configuration  
17. C. Flux CD  
18. A. Run one Pod on each node for logging or monitoring  
19. B. Private endpoint configuration  
20. B. Upgrade the control plane, then node groups, testing in dev first  
21. B. AWS IAM Authenticator plugin  
22. B. Provision AWS Load Balancers for Kubernetes Ingress resources  
23. B. Up to 90% cost savings  
24. C. ExternalSecret (via Kubernetes External Secrets)  
25. B. Using NetworkPolicy objects with a compatible CNI plugin  
26. B. An Instance Profile  
27. A. Velero  
28. B. Use the CronJob resource in YAML  
29. B. Pod CPU and memory usage  
30. B. Use `securityContext.runAsNonRoot: true` in Pod specs  
