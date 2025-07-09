# AWS CodeArtifact - Quick Overview

## What is AWS CodeArtifact?

AWS CodeArtifact is a **fully managed artifact repository service** that allows you to securely store, publish, and share software packages used in development.

It supports popular package formats such as:

- **npm** (JavaScript)
- **PyPI** (Python)
- **Maven** (Java)
- **NuGet** (.NET)

---

## Key Benefits

✅ Fully managed, scalable, and secure  
✅ Supports multiple package formats  
✅ Integrates with existing build tools (npm, pip, Maven, etc.)  
✅ Centralized package sharing across teams  
✅ Secure with AWS IAM and encryption  
✅ Pay-as-you-go pricing model  

---

## Typical Use Cases

- Private package repositories for internal development  
- Proxy for public repositories (e.g., npmjs, pypi.org)  
- Secure sharing of proprietary libraries  
- Isolated package management for CI/CD pipelines  

---

## Core Concepts

| Term            | Description                                        |
|-----------------|---------------------------------------------------|
| **Domain**      | Logical grouping of multiple repositories         |
| **Repository**  | Individual package store (npm, PyPI, Maven, etc.) |
| **Upstream**    | External public repository proxy configuration    |
| **Authorization Token** | Temporary token for authentication        |

---

## Example - Publish npm Package

1. Get Authorization Token
```bash
aws codeartifact get-authorization-token --domain my-domain --domain-owner 123456789012
