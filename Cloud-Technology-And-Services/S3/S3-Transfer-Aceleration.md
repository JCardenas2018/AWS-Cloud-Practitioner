## Amazon S3 Transfer Acceleration

Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and your S3 bucket.

### How It Works
- **Edge Locations:** Uploads are routed to the nearest AWS Edge location via the AWS global network backbone.  
- **Optimized Network Paths:** Data travels over optimized, highly redundant network paths to reach the target bucket’s Region.  
- **Accelerated Endpoint:** You use a special bucket endpoint, e.g. `my-bucket.s3-accelerate.amazonaws.com`.

### Key Benefits
- **Reduced Latency:** Significant speed improvements (up to 50–500% faster) on long-distance transfers.  
- **Ease of Use:** No client-side software changes—just switch to the accelerate endpoint.  
- **Security:** Transfers are encrypted in transit over SSL/TLS.

### Pricing
- **Data Transfer Acceleration Fee:**  
  • $0.04 per GB (first 50 TB/month)  
  • $0.03 per GB (next 450 TB/month)  
  • $0.02 per GB (over 500 TB/month)  
- **Standard S3 Data Out Fees:** Apply on top of the acceleration fee.

> **Note:** Pricing varies by Region. See the [S3 Transfer Acceleration Pricing](https://aws.amazon.com/s3/pricing/) page for your Region.

### Enabling Transfer Acceleration

```bash
# Enable on an existing bucket
aws s3api put-bucket-accelerate-configuration \
  --bucket my-bucket \
  --accelerate-configuration Status=Enabled

# Verify status
aws s3api get-bucket-accelerate-configuration --bucket my-bucket
