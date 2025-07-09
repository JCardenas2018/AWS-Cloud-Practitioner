# AWS CodeBuild - Quick Overview

## What is AWS CodeBuild?

**AWS CodeBuild** is a fully managed continuous integration (CI) service that compiles source code, runs tests, and produces build artifacts ready for deployment.

CodeBuild scales automatically and eliminates the need to manage your own build servers.

---

## Key Benefits

✅ Fully managed, no server maintenance  
✅ Pay-as-you-go pricing (per build minute)  
✅ Supports multiple environments (Java, Node.js, Python, Docker, etc.)  
✅ Integrates with GitHub, Bitbucket, CodeCommit, S3  
✅ Scales automatically for parallel builds  
✅ Supports custom build environments using Docker images  
✅ Works with AWS CodePipeline for CI/CD  

---

## Typical Use Cases

- Continuous Integration (CI) for applications  
- Building and testing container images  
- Running unit and integration tests  
- Generating deployment-ready artifacts  
- Automating security or compliance checks  

---

## Core Concepts

| Term        | Description                                           |
|-------------|------------------------------------------------------|
| **Project** | Defines the build environment, source location, etc. |
| **BuildSpec** | YAML file specifying build commands and phases     |
| **Artifacts** | Output files produced after the build              |
| **Environment** | Docker image and compute settings for the build  |

---

## Example - Basic `buildspec.yml`

```yaml
version: 0.2

phases:
  install:
    commands:
      - echo Installing dependencies...
      - npm install
  build:
    commands:
      - echo Building project...
      - npm run build
artifacts:
  files:
    - '**/*'
