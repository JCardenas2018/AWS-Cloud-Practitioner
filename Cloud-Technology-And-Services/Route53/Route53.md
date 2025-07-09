## Amazon Route 53

### Overview  
Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service that routes end-user requests to Internet applications running in AWS—or to infrastructure outside of AWS. It provides domain registration, DNS routing, and health checking.

### Key Features  
- **Hosted Zones & Record Sets**  
  - Manage public and private zones (within a VPC) with record types A, AAAA, CNAME, MX, TXT, SRV, NS, and Alias records.  
- **Alias Records**  
  - Map apex (“root”) domains (e.g., example.com) to AWS resources (ELB, CloudFront, S3 static website, API Gateway) without extra query charges.  
- **Health Checks & Failover**  
  - Continuously monitor endpoints (HTTP(S), TCP, or custom) and route traffic away from unhealthy targets.  
- **Routing Policies**  
  - **Simple**: single resource  
  - **Weighted**: distribute traffic across multiple resources by weight  
  - **Latency-Based**: route to the region with lowest latency  
  - **Geolocation / Geo-Proximity**: direct users based on their location  
  - **Multi-Value Answer**: return up to eight healthy IPs, simulating DNS-level load balancing  
- **Traffic Flow**  
  - Visual editor for designing complex traffic routing combining multiple policies, weights, and health checks.  
- **Domain Registration**  
  - Register, transfer, or renew domain names directly through the AWS console.

### Common Use Cases  
- **Global Load Balancing**: direct users to the closest region by latency or geolocation.  
- **High Availability**: automatic failover between active and standby endpoints.  
- **Alias Simplification**: map root domains to AWS resources without needing CNAMEs.  
- **Private DNS**: host internal domains for services within a VPC.

### Pricing Model  
- **Hosted Zones**  
  - \$0.50 per public hosted zone per month  
  - \$0.10 per private hosted zone per month  
- **DNS Queries**  
  - Standard queries: \$0.40 per million  
  - Latency-based, geo, and traffic-flow queries: \$0.70 per million  
- **Health Checks**  
  - \$0.50 per health check per month  
  - \$0.05 per million health check requests  
- **Domain Registration**  
  - Varies by top-level domain (e.g., \$12/year for .com)

### Security & Compliance  
- **IAM Policies**: control who can create/modify zones, records, and health checks.  
- **Private Hosted Zones**: restrict DNS resolution to within one or more VPCs.  
- **CloudTrail Logging**: audit all Route 53 API calls.  
- **DNSSEC (Beta)**: cryptographically sign zone data to protect against DNS spoofing.

### Integrations  
- **Elastic Load Balancing & CloudFront**: use Alias records for seamless mapping without charges.  
- **Amazon S3 Static Sites**: point root domains to S3 website endpoints.  
- **API Gateway & Global Accelerator**: map custom domains directly.  
- **Route 53 Resolver**: hybrid DNS resolution between on-premises networks and VPCs.

### Example: Create a Public Hosted Zone via AWS CLI  
```bash
aws route53 create-hosted-zone \
  --name example.com \
  --caller-reference "$(date +%s)" \
  --hosted-zone-config Comment="Public zone for example.com",PrivateZone=false
