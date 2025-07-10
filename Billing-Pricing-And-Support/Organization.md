# AWS Organizations

AWS Organizations lets you centrally manage multiple AWS accounts, apply governance policies, and consolidate billing to optimize cost, security, and compliance.

---

## 1. Key Concepts

- **Organization**  
  The root entity that contains all your AWS accounts.  
- **Organizational Unit (OU)**  
  Logical groupings of accounts to apply common policies (e.g., “Production”, “Development”).  
- **Service Control Policies (SCPs)**  
  IAM-level policies attached at the root or OU level that allow or deny AWS service actions.  
- **Management Account**  
  The master account that creates the Organization and handles consolidated billing; should not run workloads.

---

## 2. Benefits

- **Centralized Governance**  
  Enforce SCPs to ensure compliance (e.g., block non-approved regions).  
- **Consolidated Billing**  
  Combine charges across all member accounts, leveraging volume discounts.  
- **Delegated Administration**  
  Define OU-specific administrators and apply fine-grained permissions.  
- **Environment Isolation**  
  Separate accounts for dev, test, and prod to reduce blast radius risks.

---

## 3. Core Features

- **Automated Account Provisioning**  
  Use the `CreateAccount` API or integrate with AWS Control Tower to spin up new accounts.  
- **Account Tagging**  
  Organize and filter accounts using tags (e.g., `Environment=Prod`).  
- **Permission Policies**  
  In addition to SCPs, integrate AWS SSO (IAM Identity Center) for user/group access management.  
- **Service Integrations**  
  Works with AWS Control Tower, AWS Config, CloudTrail, and CloudWatch for unified governance and monitoring.

---

## 4. AWS CLI Examples

1. **Create an OU**  
   ```bash
   aws organizations create-organizational-unit \
     --parent-id r-abcdefgh \
     --name Development
