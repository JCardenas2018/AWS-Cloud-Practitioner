# AWS CodeDeploy - Quick Overview

## What is AWS CodeDeploy?

**AWS CodeDeploy** is a fully managed service that automates application deployments to:

- **Amazon EC2 instances**  
- **On-premises servers**  
- **AWS Lambda functions**  
- **Amazon ECS (Blue/Green deployments)**  

It enables safe, repeatable, and automated deployments across your infrastructure.

---

## Key Benefits

✅ Fully managed deployment automation  
✅ Supports in-place and blue/green deployments  
✅ Works with EC2, ECS, Lambda, and on-premises servers  
✅ Integrates with CodePipeline, CodeCommit, GitHub, etc.  
✅ Reduces downtime and deployment risks  
✅ Rollback on failure  
✅ Customizable deployment strategies  

---

## Deployment Types

| Type           | Description                                  |
|----------------|----------------------------------------------|
| **In-Place**   | Updates existing instances or servers        |
| **Blue/Green** | Shifts traffic to new instances or containers |

---

## Typical Use Cases

- Automated application deployments to EC2 or on-premises  
- Zero-downtime deployments using blue/green strategy  
- Deploy serverless applications (Lambda)  
- Update ECS services with minimal impact  
- Rollback to previous versions on failure  

---

## Core Concepts

| Term                 | Description                                          |
|----------------------|-----------------------------------------------------|
| **Application**      | Logical representation of the app to deploy         |
| **Deployment Group** | Target set of instances, Lambda functions, or ECS   |
| **Deployment**       | Execution of an application version to targets      |
| **AppSpec File**     | YAML or JSON file defining deployment actions       |

---

## Example - Simple `appspec.yml` for EC2

```yaml
version: 0.0
os: linux
files:
  - source: /
    destination: /home/ec2-user/app

hooks:
  AfterInstall:
    - location: scripts/install_dependencies.sh
      timeout: 300
  ApplicationStart:
    - location: scripts/start_server.sh
      timeout: 300
