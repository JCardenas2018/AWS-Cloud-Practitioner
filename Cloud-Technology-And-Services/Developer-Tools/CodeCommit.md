# AWS CodeCommit - Quick Overview

## What is AWS CodeCommit?

**AWS CodeCommit** is a fully managed source control service that hosts secure, private Git repositories. It enables teams to store, manage, and version code in the cloud with high availability and scalability.

---

## Key Benefits

✅ Fully managed, no server maintenance  
✅ Secure with encryption at rest and in transit  
✅ Integrated with AWS IAM for access control  
✅ Supports Git-based workflows (branches, commits, pull requests)  
✅ High availability across multiple Availability Zones  
✅ Works with AWS CodePipeline and other DevOps tools  

---

## Typical Use Cases

- Private Git repositories for code storage  
- Version control for applications and infrastructure-as-code  
- Integration with CI/CD pipelines  
- Team collaboration using pull requests and code reviews  
- Secure storage of sensitive code or artifacts  

---

## Core Concepts

| Term            | Description                                         |
|-----------------|----------------------------------------------------|
| **Repository**  | Git repository hosted in AWS CodeCommit            |
| **Branch**      | Parallel versions of code for development workflows |
| **Pull Request**| Code review and collaboration process              |
| **Trigger**     | Event-based actions (e.g., start a build)          |

---

## Example - Creating a Repository (CLI)

```bash
aws codecommit create-repository --repository-name MyRepo \
  --repository-description "Sample repository for project"
