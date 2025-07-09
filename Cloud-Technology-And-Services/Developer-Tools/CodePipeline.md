# AWS CodePipeline - Quick Overview

## What is AWS CodePipeline?

**AWS CodePipeline** is a fully managed **Continuous Integration and Continuous Delivery (CI/CD)** service that automates the build, test, and deployment process for your applications.

It enables rapid, reliable, and repeatable software delivery across AWS and third-party platforms.

---

## Key Benefits

✅ Fully managed CI/CD pipeline  
✅ Automates code builds, tests, and deployments  
✅ Supports integration with CodeCommit, GitHub, Bitbucket, S3  
✅ Connects with CodeBuild, CodeDeploy, CloudFormation, Lambda  
✅ Enables manual approval steps for sensitive deployments  
✅ Highly customizable stages and actions  
✅ Pay-as-you-go pricing  

---

## Typical Use Cases

- Automate application deployments to EC2, ECS, Lambda, or on-premises  
- Continuous integration for code changes with automated tests  
- Multi-stage pipelines for dev, test, and production environments  
- Integrating third-party tools (e.g., GitHub, Jenkins, SonarQube)  
- Deploying infrastructure with CloudFormation  

---

## Core Concepts

| Term        | Description                                            |
|-------------|-------------------------------------------------------|
| **Pipeline** | Defines the CI/CD workflow stages                   |
| **Stage**   | Logical step (Source, Build, Test, Deploy, etc.)      |
| **Action**  | Individual task within a stage (build, deploy, etc.)  |
| **Artifact**| Files or output passed between stages                 |

---

## Example - Simple Pipeline with CLI

```bash
aws codepipeline create-pipeline --cli-input-json file://pipeline-definition.json
