# AWS Health Dashboard

AWS Health Dashboard provides personalized visibility into the status of your AWS services and resources, with proactive notifications about events that may affect them.

---

## 1. Dashboard Types

- **Service Health Dashboard (SHD)**  
  - Shows the global status of AWS services by Region (e.g., “Amazon EC2 in us-east-1: operating normally”).  
  - Ideal for quickly spotting service-wide outages or degradations.

- **Personal Health Dashboard (PHD)**  
  - Displays events specific to **your** accounts and resources (scheduled maintenance, service issues, quota limits).  
  - Filter by account, Region, service, and event type.  
  - Detailed notifications with start/end times, expected impact, and recommended actions.

---

## 2. How to Access

1. In the **AWS Management Console**, navigate to **Health** → **Dashboard**.  
2. Filter by **Upcoming events**, **Open issues**, or by **Service**/**Region**.  
3. Click an event to view details and recommended steps.

---

## 3. AWS CLI Example

List up to 5 open or upcoming events:

```bash
aws health describe-events \
  --filter eventStatusCodes=open,upcoming \
  --max-results 5
