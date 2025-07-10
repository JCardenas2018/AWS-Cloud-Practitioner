# AWS Cost Explorer

AWS Cost Explorer is an interactive tool in AWS Cost Management that helps you visualize, understand, and manage your AWS costs and usage over time.

---

## 1. Key Features

- **Historical Data Analysis**  
  View your spend and usage by day, month, or custom date range—break down by service, account, tag, or region.

- **Filters & Grouping**  
  Filter by service (EC2, S3, RDS…), purchase option (On-Demand, RI, Spot) or tag, and group to compare (e.g. “dev” vs “prod”).

- **Charts & Tables**  
  Use line charts, stacked bar charts, or detailed summary tables to explore your data.

- **Forecasts**  
  Based on historical trends, Cost Explorer projects your spend for the remainder of the month or quarter.

- **Savings Plans & RI Recommendations**  
  Get tailored recommendations on Savings Plans and Reserved Instances based on your usage patterns.

---

## 2. Getting Started

1. In the **AWS Management Console**, go to **Billing & Cost Management** → **Cost Explorer**.  
2. **Enable** Cost Explorer (data may take up to 24 hours to appear).  
3. Select a **date range**, apply **filters** or **groupings**, and explore the interactive charts.  
4. **Export** data to CSV for deeper analysis or reporting.

---

## 3. AWS CLI Examples

- **Enable Cost Explorer**  
  ```bash
  aws ce enable-cost-explorer
