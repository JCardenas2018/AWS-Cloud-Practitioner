# AWS Resource Access Manager (RAM)

AWS Resource Access Manager (RAM) allows you to securely share AWS resources with other AWS accounts, Organizational Units (OUs), or entire AWS Organizations without needing to replicate them.

---

## 1. Key Concepts

- **Resource shares**  
  Logical containers where you define which resources to share and with whom.  
- **Principals**  
  Entities you share with—can be individual AWS account IDs, IAM Roles, OUs, or your entire AWS Organization.  
- **Shared resources**  
  Supported resource types include VPC subnets, Route 53 Resolver rules, License Manager configurations, AWS Outposts racks, RAM itself, and many more.

---

## 2. How It Works

1. **Create a resource share**  
   - Select one or more resource types and specific ARNs.  
   - Add principals (account IDs, OUs, or Organization).  
2. **Accept invitations** (for external accounts)  
   - Invited accounts receive a share invitation and must accept before accessing the resources.  
3. **Use shared resources**  
   - Once accepted, shared resources appear in the consumer account as if they were created locally.

---

## 3. Supported Resources (Examples)

| Service                  | Resource Types                                   |
|--------------------------|--------------------------------------------------|
| Amazon VPC               | Subnets, Transit Gateways, Subnet CIDR reservations |
| Amazon Route 53 Resolver | Resolver rules, Resolver endpoints               |
| AWS License Manager      | License configurations, license rules            |
| AWS Outposts             | Outpost racks, subnets                           |
| AWS RAM                  | RAM resource shares                              |

---

## 4. AWS CLI Example

1. **Create a resource share**  
   ```bash
   aws ram create-resource-share \
     --name MyVPCShare \
     --resource-arns arn:aws:ec2:us-east-1:123456789012:subnet/subnet-0abcde1234567890 \
     --principals 111122223333 444455556666 \
     --allow-external-principals
