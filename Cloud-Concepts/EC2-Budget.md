# 📊 AWS Budgets Overview

## 🧾 What is AWS Budgets?

**AWS Budgets** is a cost management tool that allows you to **set custom cost and usage budgets** for your AWS account. It helps you proactively track spending, usage, and savings commitments.

---

## 🎯 Key Features

### 1. **Cost Budgets**
Set a specific monetary limit (e.g., $200/month) and receive alerts when you approach or exceed it.

### 2. **Usage Budgets**
Define usage limits for specific resources, such as EC2 instance hours, S3 storage, etc.  
Example: 500 EC2 hours per month.

### 3. **Reservation and Savings Plans Budgets**
Track the utilization and coverage of your **Reserved Instances (RI)** and **Savings Plans** to ensure you're maximizing your discounts.

### 4. **Custom Alerts**
Configure notifications (via email or Amazon SNS) for when:
- You reach a budget threshold (e.g., 80%, 100%)
- AWS forecasts that you’ll exceed your budget

---

## 🛠️ How to Set Up a Budget

1. Go to the [AWS Budgets Console](https://console.aws.amazon.com/billing/home#/budgets).
2. Click **“Create budget.”**
3. Select a budget type:
   - Cost Budget
   - Usage Budget
   - Savings Plans Budget
   - Reservation Budget
4. Define the following:
   - Amount or usage limit
   - Frequency (monthly, quarterly, annually)
   - Filters (by service, account, region, tag, etc.)
   - Conditions for alerts
5. Add notification recipients (email or SNS topic)

---

## 📈 Benefits of Using AWS Budgets

- Prevent unexpected cloud charges
- Improve financial planning
- Granular cost visibility (by service, team, project, etc.)
- Integrated with **AWS Cost Explorer** for deeper analysis

---

## 💡 Pro Tip

Use **resource tags** to create targeted budgets for specific teams, applications, or environments (e.g., dev, staging, prod).

---
