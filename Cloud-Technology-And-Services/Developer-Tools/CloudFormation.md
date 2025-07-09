# AWS CloudFormation - Quick Guide with Examples

## What is AWS CloudFormation?

AWS CloudFormation is an **Infrastructure as Code (IaC)** service to define, provision, and manage AWS resources using YAML or JSON templates. It enables automated, consistent, and repeatable deployments across environments.

---

## Key Benefits

✅ Define infrastructure as code  
✅ Automate resource creation/updates  
✅ Consistent, version-controlled deployments  
✅ Supports most AWS services  
✅ Rollback on failure  

---

## Main Components

| Component    | Description                                       |
|--------------|---------------------------------------------------|
| **Stack**    | Group of resources managed as one unit            |
| **Template** | YAML/JSON file defining infrastructure            |
| **Parameters** | Dynamic input values                          |
| **Outputs**  | Return useful resource information               |
| **Mappings** | Static key-value mappings                        |
| **Conditions** | Conditional resource logic                     |
| **Change Sets** | Preview changes before applying               |

---

## Example 1 - Basic EC2 Instance

```yaml
AWSTemplateFormatVersion: "2010-09-09"
Description: "Basic EC2 instance example"

Parameters:
  KeyName:
    Type: String
    Description: SSH Key Pair Name

Resources:
  MyEC2Instance:
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t2.micro
      KeyName: !Ref KeyName
      ImageId: ami-0c55b159cbfafe1f0

Outputs:
  InstanceID:
    Value: !Ref MyEC2Instance
