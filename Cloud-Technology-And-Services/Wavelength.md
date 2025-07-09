# AWS Wavelength

AWS Wavelength extends AWS infrastructure to telecommunications providers’ 5G networks, bringing compute and storage services closer to end users for ultra-low-latency applications.

---

## 1. How It Works

1. **Wavelength Zones**  
   - Specialized Availability Zones located at the edge of a telecom operator’s 5G network (e.g., Verizon in the US, Vodafone in Europe).  
   - Allow you to launch EC2 instances, ECS/EKS containers, or Lambda functions directly on the mobile network edge.

2. **Integration with Your VPC**  
   - Each Wavelength Zone is associated with an AWS VPC in the same standard region.  
   - Traffic between your edge application and other AWS services (S3, DynamoDB, RDS…) travels over the AWS backbone, not the public internet.

3. **Public & Private IP Addresses**  
   - Instances receive private IPs within your VPC and optionally edge-optimized public IPs for mobile clients.

---

## 2. Key Components

- **EC2 Instances in Wavelength Zones**  
  Standard or Graviton instances with high-performance local EBS storage.  
- **ECS/EKS**  
  Deploy containers at the edge via tasks or pods.  
- **Lambda@Edge (Preview)**  
  Run serverless functions on the 5G network for millisecond-level responses.  
- **Edge-Optimized Load Balancers**  
  Route mobile traffic to the nearest healthy endpoints.

---

## 3. Common Use Cases

- **Real-Time Gaming & AR/VR**  
  Bidirectional communication with < 10 ms latency.  
- **Industrial IoT & Robotics**  
  Real-time control of remote devices.  
- **Interactive Video Streaming**  
  Live streams with ultra-low latency for real-time interaction.  
- **Autonomous Vehicles & Drones**  
  Process sensor data at the edge before sending to the central cloud.

---

## 4. AWS CLI – Basic Example

1. **Create a Wavelength Subnet** in your VPC (region must support Wavelength and operator must be enabled):

   ```bash
   aws ec2 create-subnet \
     --vpc-id vpc-0123456789abcdef0 \
     --cidr-block 10.0.100.0/24 \
     --availability-zone us-east-1-wl1
