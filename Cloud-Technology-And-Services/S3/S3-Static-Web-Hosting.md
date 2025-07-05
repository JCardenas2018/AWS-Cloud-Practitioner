## Static Website Hosting on Amazon S3

Amazon S3 can serve static websites (HTML, CSS, JavaScript, images) directly from a bucket without running servers.

### Key Features
- **No server management**: Host your site entirely on S3.
- **High availability & scalability**: Backed by S3’s 99.99% availability SLA.
- **Low cost**: Pay only for storage and data transfer.
- **Custom domain & HTTPS**: Use Amazon CloudFront for SSL/TLS and custom CNAMEs.

### Steps to Configure

1. **Create a Public Bucket**  
   ```bash
   aws s3 mb s3://my-website-bucket --region us-east-1
   aws s3 website s3://my-website-bucket/ --index-document index.html --error-document error.html
