# Service Control Policies (SCP) in AWS Organizations

**Service Control Policies (SCPs)** are JSON-based policy documents used within AWS Organizations to define the maximum permissions an account or organizational unit (OU) can have. Unlike IAM policies, which grant permissions, SCPs **only restrict** actions—no identity in the targeted account can perform actions outside these boundaries, even if granted by IAM.

## 🔑 Key Features

* **Hierarchical Scope**: Apply at the organization’s root, specific OUs, or individual accounts; policies inherit downward through the hierarchy.
* **Permission Boundaries**: Act as a guardrail—identities cannot exceed the restrictions set by SCPs.
* **Policy Types**:

  * **Allow List (Permissive)**: Explicitly allow specific actions; everything else is implicitly denied.
  * **Deny List (Restrictive)**: Explicitly deny specific actions; everything else follows IAM permissions.
* **Conditional Controls**: Use condition keys (e.g., tags, regions, request attributes) to fine-tune restrictions.

## 🛠️ Example SCPs

### 1. Deny All IAM Actions

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Action": "iam:*",
      "Resource": "*"
    }
  ]
}
```

**Use case**: Prevent creation, modification, or deletion of any IAM resources across all accounts.

### 2. Restrict API Calls to Specific Regions

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Action": "*",
      "Resource": "*",
      "Condition": {
        "StringNotEquals": {
          "aws:RequestedRegion": ["us-east-1", "us-west-2"]
        }
      }
    }
  ]
}
```

**Use case**: Enforce data residency by allowing actions only in approved regions.

### 3. Require an `Environment` Tag on Resource Creation

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Action": "*",
      "Resource": "*",
      "Condition": {
        "Null": {
          "aws:RequestTag/Environment": "true"
        }
      }
    }
  ]
}
```

**Use case**: Enforce tagging standards for cost allocation, automation, and governance.

## 📚 Common Use Cases

1. **Dev/Test Environment Controls**: Block expensive services (e.g., Redshift, EMR) or limit resource sizes in development OUs.
2. **Compliance & Auditing**: Deny disabling or modification of CloudTrail, Config, or other auditing services.
3. **Data Protection**: Prevent deletion or public exposure of S3 buckets in production accounts.
4. **Security Hardening**: Restrict EC2 instance creation to only approved AMIs or specific security groups.

## ✅ Best Practices

* **Start with Deny-All**: Use a restrictive SCP and explicitly allow required actions to enforce least privilege.
* **Test in Sandbox**: Validate new SCPs in a staging or test account before deploying organization-wide.
* **Version & Document**: Keep clear change logs and descriptions for each policy revision.
* **Combine with IAM**: Layer SCPs with IAM policies for defense in depth.
* **Review Regularly**: Update SCPs as organizational requirements and AWS services evolve.

---

*Created with examples and use cases to streamline SCP implementation in AWS Organizations.*
