# Amazon EC2 Image Builder

Amazon EC2 Image Builder automates the creation, maintenance, validation, and testing of golden server images for EC2, on-premises instances, and containers.

## Key Concepts

* **Image Recipe**: YAML or JSON document defining base image, components, and build steps.
* **Components**: Reusable definition of software, scripts, or configurations to apply (e.g., install packages, run tests).
* **Infrastructure Configuration**: Specifies instance type, subnet, security groups, and logging for build infrastructure.
* **Distribution Configuration**: Defines where and how to distribute the built images (regions, accounts).
* **Image Pipeline**: Automated workflow connecting recipe, infrastructure, and distribution to produce images on schedule or on demand.

## Features & Benefits

* **Automation**: Schedule regular image builds with built-in versioning and replacement of outdated images.
* **Standardization**: Enforce consistent OS patches, security hardening, and software configuration across environments.
* **Testing & Validation**: Integrate build-time tests and container validation to catch issues early.
* **Security**: Automatically apply security patches and validate images against security benchmarks (CIS).
* **Integration**: Works with AWS CodePipeline, CloudWatch, CloudTrail, and AWS Systems Manager.

## Use Cases

* **Hybrid Environments**: Build and distribute images to EC2 and on-premises VMware/Hyper-V hosts.
* **Immutable Infrastructure**: Ensure every deployment uses a fresh, tested AMI without manual steps.
* **Compliance**: Maintain up-to-date, hardened images that comply with organizational or regulatory standards.
* **Continuous Delivery**: Integrate image builds into CI/CD to deliver updated AMIs alongside application code.

## Example: Simple Image Pipeline

1. **Define a Recipe** (`my-recipe.yml`):

```yaml
name: my-base-image
version: 1.0.0
components:
  - name: aws-cli
    version: 1.0.0
    uri: "arn:aws:imagebuilder:us-east-1:aws:component/aws-cli-version-x"
  - name: security-updates
    version: 1.0.0
    uri: "arn:aws:imagebuilder:us-east-1:aws:component/amazon-linux-2-security-updates"
```

2. **Create Infrastructure Configuration**: Specify EC2 instance type and networking for build.
3. **Create Distribution Configuration**: Target `us-east-1` and `us-west-2` accounts and regions.
4. **Create Pipeline** via CLI:

```bash
aws imagebuilder create-image-pipeline \
  --name my-image-pipeline \
  --image-recipe-arn arn:aws:imagebuilder:us-east-1:123456789012:image-recipe/my-base-image/1.0.0 \
  --infrastructure-configuration-arn arn:aws:imagebuilder:us-east-1:123456789012:infrastructure-configuration/my-config \
  --distribution-configuration-arn arn:aws:imagebuilder:us-east-1:123456789012:distribution-configuration/my-dist-config
```

## Cost Considerations

* **Build Infrastructure**: You incur EC2, EBS, and data transfer charges for the instances Image Builder uses to build images.
* **Storage**: You pay for AMIs and associated snapshots stored in S3/EBS.
* **Optional**: Additional fees for AWS Systems Manager automation or third-party validation components.

> **Tip:** Use spot instances for build infrastructure to reduce costs. Implement retention policies on old AMIs to manage storage costs.

**References:**

* AWS EC2 Image Builder User Guide: [https://docs.aws.amazon.com/imagebuilder/latest/userguide/](https://docs.aws.amazon.com/imagebuilder/latest/userguide/)
* AWS CLI Reference: [https://docs.aws.amazon.com/cli/latest/reference/imagebuilder/index.html](https://docs.aws.amazon.com/cli/latest/reference/imagebuilder/index.html)
