# AWS Cost Explorer & Cost and Usage Reports

AWS provides two complementary tools for cost visibility and reporting:

1. **AWS Cost Explorer** – an interactive console and API for analyzing historical and forecasted spend.  
2. **AWS Cost and Usage Reports (CUR)** – detailed, line-item CSV or Parquet reports delivered to S3 for custom analysis.

---

## 1. AWS Cost Explorer

### Key Features
- **Interactive Dashboards**  
  - Time-series charts (daily, monthly, custom)  
  - Filter and group by service, account, tag, region, purchase option  
- **Forecasts & Trends**  
  - Projection of your spend based on historical usage  
- **RI & Savings Plans Recommendations**  
  - Automated recommendations to maximize Reserved Instance and Savings Plan discounts  
- **API & CLI Access**  
  - Programmatic queries via `aws ce get-cost-and-usage`, `aws ce get-forecast`

### AWS CLI Examples

- **Enable Cost Explorer**  
  ```bash
  aws ce enable-cost-explorer
