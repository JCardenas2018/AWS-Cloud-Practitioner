# AWS Global Accelerator

AWS Global Accelerator is a networking service that improves the availability and performance of your global applications by directing user traffic to the optimal AWS endpoints over the AWS global network.

---

## How It Works

1. **Static Anycast IPs**  
   - You receive two global static IP addresses.  
   - Clients connect to these IPs, regardless of their location.

2. **Accelerator**  
   - Define one or more **Listeners** (protocols & port ranges).  
   - Each listener routes traffic to one or more **Endpoint Groups** in different AWS Regions.

3. **Endpoint Groups**  
   - Point each group at regional endpoints (ALB, NLB, EC2 instance, Elastic IP).  
   - Assign a **weight** to each endpoint for traffic distribution.

4. **Health Checks & Failover**  
   - Global Accelerator continuously checks endpoint health.  
   - Automatically removes unhealthy endpoints and reroutes traffic to healthy ones.

---

## Key Benefits

- **Lower Latency**  
  Traffic travels over the AWS global backbone instead of the public internet.  
- **Improved Availability**  
  Automatic failover across Regions if an endpoint becomes unhealthy.  
- **Stable IP Addresses**  
  No need to update DNS when scaling or replacing endpoints.  
- **Global Traffic Management**  
  Fine-grained traffic control with endpoint weights and routing policies.

---

## Common Use Cases

- **Multi-Region Web Applications**  
  Serve users from the nearest Region with minimal latency.  
- **Online Gaming**  
  Guarantee low-lag connections to game servers worldwide.  
- **Global API Frontends**  
  Maintain 99.99% availability by spreading traffic across Regions.

---

## AWS CLI Example

1. **Create an Accelerator**  
   ```bash
   aws globalaccelerator create-accelerator \
     --name MyAccelerator \
     --ip-address-type IPV4 \
     --enabled
