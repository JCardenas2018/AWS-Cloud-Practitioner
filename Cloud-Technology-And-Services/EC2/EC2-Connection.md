## EC2 Connection Methods & Examples

You can connect to your EC2 instances using various methods depending on the OS, networking setup, and security requirements.

### 1. SSH (Secure Shell) — Linux Instances

**Prerequisites:**

* Key pair (.pem file) created and associated with the instance
* Security group allowing inbound TCP port 22

```bash
# Set correct permissions for your key
chmod 400 my-key-pair.pem

# Connect via SSH
ssh -i my-key-pair.pem ec2-user@ec2-203-0-113-25.compute-1.amazonaws.com
```

Usernames vary by AMI: `ec2-user` (Amazon Linux), `ubuntu` (Ubuntu), `centos` (CentOS), `admin` (Debian).

### 2. RDP (Remote Desktop Protocol) — Windows Instances

**Prerequisites:**

* Password generated via EC2 console or AWS CLI
* Security group allowing inbound TCP port 3389

1. Retrieve password:

```bash
# Using AWS CLI
aws ec2 get-password-data \
  --instance-id i-0123456789abcdef0 \
  --priv-launch-key my-key-pair.pem
```

2. Use Windows Remote Desktop client with instance’s public DNS/IP and retrieved password.

### 3. EC2 Instance Connect — Browser-based SSH

**Prerequisites:**

* IAM policy `ec2-instance-connect:SendSSHPublicKey`
* Security group allowing TCP 22
* SSM agent installed (if using newer AMIs)

1. In AWS Console, click **Connect → EC2 Instance Connect**.
2. Or via CLI:

```bash
aws ec2-instance-connect send-ssh-public-key \
  --region us-east-1 \
  --instance-id i-0123456789abcdef0 \
  --availability-zone us-east-1a \
  --instance-os-user ec2-user \
  --ssh-public-key file://my-key.pub
```

Then SSH to the instance’s public DNS.

### 4. AWS Systems Manager Session Manager

**Prerequisites:**

* SSM Agent installed and running on the instance
* IAM role with `AmazonSSMManagedInstanceCore` attached
* Security group allowing HTTPS outbound (port 443)

```bash
# Start a session via AWS CLI
aws ssm start-session --target i-0123456789abcdef0
```

No open inbound ports required; connects over AWS-managed channel.

### 5. SSM Port Forwarding

Forward local port to a remote port on the instance:

```bash
aws ssm start-session \
  --target i-0123456789abcdef0 \
  --document-name AWS-StartPortForwardingSession \
  --parameters '{"portNumber":["3389"],"localPortNumber":["9999"]}'
```

Then `rdp://localhost:9999` in your RDP client.

### 6. AWS CloudShell & AWS CLI

Use CloudShell from the AWS Console to SSH (via SSM) without local tooling:

```bash
# In CloudShell
aws ssm start-session --target i-0123456789abcdef0
```

### 7. Other Methods

* **NICE DCV**: High-performance remote desktop for graphics workloads (Linux/Windows).
* **Session Manager with Port Forwarding**: Access internal resources without exposing ports.

---

**Security Best Practices:**

* Use Session Manager to eliminate SSH/RDP exposure.
* Restrict Security Groups to trusted IPs.
* Rotate key pairs and enforce key policies.
* Monitor sessions with CloudTrail and CloudWatch Logs.
