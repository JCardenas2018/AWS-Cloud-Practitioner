# AWS Control Tower

AWS Control Tower automates the setup of a multi-account AWS environment (“landing zone”) with best-practice governance guardrails, centralized logging, and account provisioning.

---

## 1. Key Concepts

- **Landing Zone**  
  A preconfigured environment that includes AWS Organizations structure, baseline security, and compliance guardrails.

- **Organizational Units (OUs)**  
  Logical groupings of AWS accounts (e.g., “Security”, “Sandbox”, “Production”) with shared guardrails.

- **Guardrails**  
  Pre-built rules (preventive and detective) implemented via AWS Config, CloudWatch, IAM, Service Control Policies (SCPs), etc.  
  - **Preventive**: block non-compliant actions (e.g., prohibit public S3 buckets).  
  - **Detective**: audit and alert when non-compliance is detected (e.g., monitor root-user activity).

- **Account Factory**  
  A self-service provisioning pipeline (built on AWS Service Catalog) for standardized, repeatable account creation.

---

## 2. How It Works

1. **Enable Control Tower**  
   - Must run from the master (management) account in a supported region (usually `us-east-1` or `us-west-2`).  
2. **Deploy Landing Zone**  
   - Automatically creates an AWS Organization, OUs (“LandingZone”, “Audit”, “LogArchive”), the baseline accounts, and required AWS services (Config, CloudTrail, IAM Identity Center).  
3. **Apply Guardrails**  
   - Control Tower enforces selected guardrails at OU level.  
4. **Provision New Accounts**  
   - Use Account Factory to create new accounts with networking, security, and logging preconfigured.  
5. **Dashboard & Reports**  
   - Central console shows compliance status, account inventory, and guardrail violations.

---

## 3. Key Features

- **Automated Account Provisioning**  
  Spin up new accounts in minutes with standardized naming, tags, IAM roles, and AWS Single Sign-On (SSO) access.

- **Built-In Governance**  
  Over 70 pre-built guardrails covering IAM, networking, logging, encryption, and cost management.

- **Centralized Logging & Audit**  
  All CloudTrail logs and Config snapshots are aggregated in the Log Archive account.

- **Continuous Compliance**  
  Dashboard shows guardrail compliance; non-compliant accounts trigger alerts.

- **Extensible**  
  Integrate custom guardrails via AWS Config Rules or AWS Lambda.

---

## 4. AWS CLI Examples

> **Note:** Control Tower CLI is available in AWS CLI v2.

- **Enable Control Tower (from management account in `us-east-1`):**
  ```bash
  aws controltower enable-control-tower \
    --region us-east-1
