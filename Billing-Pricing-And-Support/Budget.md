# AWS Budgets

AWS Budgets helps you plan and control your AWS costs and usage by setting custom thresholds and receiving alerts when your consumption approaches or exceeds those limits.

---

## 1. Overview

- **Define thresholds** for cost, usage, Reserved Instance (RI) and Savings Plans (SP) utilization and coverage.  
- **Monitor** your actual or forecasted spending over a period (monthly, quarterly, or yearly).  
- **Receive alerts** via email or Amazon SNS when budgets are breached.

---

## 2. Budget Types

| Budget Type                 | What It Measures                                    |
|-----------------------------|------------------------------------------------------|
| **Cost**                    | Actual or forecasted spend in USD                    |
| **Usage**                   | Units consumed (EC2 instance-hours, GB of data…)     |
| **RI Utilization**          | % utilization of your Reserved Instances             |
| **RI Coverage**             | % of consumption covered by Reserved Instances       |
| **SP Utilization**          | % utilization of your Savings Plans                  |
| **SP Coverage**             | % of consumption covered by Savings Plans            |

---

## 3. How It Works

1. **Create a budget** by choosing type, time unit (MONTHLY/QUARTERLY/ANNUALLY) and threshold (e.g. 80%).  
2. **Configure notifications**:  
   - **Notification type:** ACTUAL (what you’ve spent) or FORECASTED (projected spend).  
   - **Comparison operator:** GREATER_THAN or LESS_THAN.  
   - **Threshold:** percentage or absolute value.  
   - **Subscribers:** email address or SNS topic.  
3. **AWS Budgets evaluates** your usage and spend daily and sends alerts when thresholds are crossed.

---

## 4. AWS CLI Example

1. **Define budget in JSON (`budget.json`):**

   ```json
   {
     "BudgetName": "MonthlyCostBudget",
     "BudgetLimit": { "Amount": 1000, "Unit": "USD" },
     "TimeUnit": "MONTHLY",
     "BudgetType": "COST",
     "TimePeriod": { "Start": "2025-07-01T00:00:00Z" }
   }
