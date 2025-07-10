# AWS Service Catalog

AWS Service Catalog allows organizations to centrally manage catalogs of approved IT services that can be deployed on AWS. It enforces governance and compliance by controlling which products, versions, and configurations end users can provision.

---

## 1. Core Concepts

- **Portfolio**  
  A container for products, constraints, and access controls.  

- **Product**  
  An IT service defined by a CloudFormation template (e.g., a web app stack, database cluster, or CI/CD pipeline).

- **Provisioning Artifact**  
  A version of a product (for example, v1, v2) linked to a specific CloudFormation template or parameter set.

- **Constraint**  
  Rules that govern how a product can be deployed, such as allowed instance types, regions, or IAM roles.

- **Principal**  
  An IAM user, group, or role (or AWS SSO user/group) that is granted access to portfolios.

---

## 2. How It Works

1. **Create a Portfolio**  
2. **Add Products** (CloudFormation templates) and one or more Provisioning Artifacts.  
3. **Define Constraints** (launch constraints, template constraints) to enforce guardrails.  
4. **Grant Access** by associating IAM principals (users, groups, or roles) with the portfolio.  
5. **End Users Launch Products** via the Service Catalog console, CLI, or API—deploying only approved configurations.

---

## 3. Key Features

- **Governance**  
  Enforce compliance with organizational policies through constraints and launch role control.  

- **Standardization**  
  Distribute vetted, versioned services across teams for consistent deployments.  

- **Version Management**  
  Maintain multiple versions of products and control who can upgrade or downgrade.  

- **Multi-Account Sharing**  
  Share portfolios across AWS Organizations for centralized service catalogs in multiple accounts.

---

## 4. AWS CLI Examples

```bash
# 1. Create a portfolio
aws servicecatalog create-portfolio \
  --display-name "MyPortfolio" \
  --provider-name "IT Department"

# 2. Create a product with a CloudFormation template
aws servicecatalog create-product \
  --name "WebApp" \
  --owner "IT Department" \
  --product-type CLOUD_FORMATION_TEMPLATE \
  --provisioning-artifact-parameters Name="v1",Info={LoadTemplateFromURL="https://bucket.s3.amazonaws.com/templates/webapp.yaml"},Type="CLOUD_FORMATION_TEMPLATE"

# 3. Associate the product with the portfolio
aws servicecatalog associate-product-with-portfolio \
  --product-id prod-abcdefghijk \
  --portfolio-id port-uvwxyz12345

# 4. Grant a role access to the portfolio
aws servicecatalog associate-principal-with-portfolio \
  --portfolio-id port-uvwxyz12345 \
  --principal-arn arn:aws:iam::123456789012:role/DevRole \
  --principal-type IAM
