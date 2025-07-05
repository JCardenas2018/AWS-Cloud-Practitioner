# EC2 IAM Roles, AssumeRole, and Permissions

Amazon EC2 instances often need access to AWS resources without embedding long‑term credentials. IAM roles and the AssumeRole API enable secure, temporary credentials for that purpose.

## 1. IAM Roles for EC2 (Instance Profiles)

* **Instance Profile**: A container for an IAM role that you attach to an EC2 instance.
* **Trust Policy**: Allows EC2 service (`ec2.amazonaws.com`) to assume the role.
* **Role Permissions**: Attached IAM policies grant the permissions the instance needs (e.g., `s3:GetObject`).

### Example Trust Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Principal": { "Service": "ec2.amazonaws.com" },
    "Action": "sts:AssumeRole"
  }]
}
```

### Creating & Attaching a Role (AWS CLI)

```bash
# 1. Create role with trust policy
aws iam create-role \
  --role-name EC2S3AccessRole \
  --assume-role-policy-document file://trust-policy.json

# 2. Attach policy (e.g., AmazonS3ReadOnlyAccess)
aws iam attach-role-policy \
  --role-name EC2S3AccessRole \
  --policy-arn arn:aws:iam::aws:policy/AmazonS3ReadOnlyAccess

# 3. Create instance profile and add role
aws iam create-instance-profile --instance-profile-name EC2S3Profile
aws iam add-role-to-instance-profile \
  --instance-profile-name EC2S3Profile \
  --role-name EC2S3AccessRole

# 4. Launch EC2 with instance profile
aws ec2 run-instances \
  --image-id ami-0123456789abcdef0 \
  --instance-type t3.micro \
  --iam-instance-profile Name=EC2S3Profile
```

## 2. sts\:AssumeRole for Cross-Account Access

EC2 instances can assume a role in another AWS account to access its resources.

### Cross-Account Trust Policy (Account B)

```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Principal": { "AWS": "arn:aws:iam::111122223333:role/EC2S3AccessRole" },
    "Action": "sts:AssumeRole"
  }]
}
```

### Assuming Role from EC2 (CLI)

```bash
# Assume the target role
aws sts assume-role \
  --role-arn arn:aws:iam::444455556666:role/RemoteAccessRole \
  --role-session-name EC2Session

# Use returned temporary credentials
env \
  AWS_ACCESS_KEY_ID=... \
  AWS_SECRET_ACCESS_KEY=... \
  AWS_SESSION_TOKEN=... \
  aws s3 ls s3://remote-account-bucket
```

## 3. Instance Metadata Service (IMDS)

EC2 instances retrieve temporary credentials via IMDS:

* **IMDSv1 vs. IMDSv2**: Use IMDSv2 (session-oriented) for stronger security.
* **Metadata URI**: `http://169.254.169.254/latest/meta-data/iam/security-credentials/<role-name>`

### Example: Fetch Credentials (IMDSv2)

```bash
# 1. Get token
token=$(curl -X PUT "http://169.254.169.254/latest/api/token" \
  -H "X-aws-ec2-metadata-token-ttl-seconds: 21600")
# 2. Fetch creds
curl -H "X-aws-ec2-metadata-token: $token" \
  http://169.254.169.254/latest/meta-data/iam/security-credentials/EC2S3AccessRole
```

## 4. Best Practices

* **Least Privilege**: Grant only necessary permissions.
* **Use IMDSv2**: Enforce `HttpTokens: required` in instance profile settings.
* **Rotate Sessions**: Limit session duration (`MaxSessionDuration` on role).
* **Audit & Monitor**: Enable CloudTrail to record `AssumeRole` calls and IAM policy usage.

---

**References:**

* IAM Roles for Amazon EC2: [https://docs.aws.amazon.com/IAM/latest/UserGuide/id\_roles\_use\_switch-role-ec2.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html)
* STS AssumeRole: [https://docs.aws.amazon.com/STS/latest/APIReference/API\_AssumeRole.html](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html)
* Instance Metadata: [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/configuring-instance-metadata-service.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/configuring-instance-metadata-service.html)
