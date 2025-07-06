# AWS CloudFront

## 1. What Is AWS CloudFront?  
AWS CloudFront is a fully managed Content Delivery Network (CDN) that accelerates delivery of websites, APIs, video content, and other web assets to users around the globe. It uses a distributed network of edge locations to cache content close to viewers, reducing latency and improving performance.

---

## 2. Key Components

- **Edge Locations**  
  Global points of presence where CloudFront caches copies of your content.

- **Origins**  
  The source of truth for your content: Amazon S3 buckets, EC2 instances, Elastic Load Balancers, API Gateway endpoints, on-premises servers, etc.

- **Distributions**  
  Configurations that tell CloudFront where to fetch content from, how to cache it, and how to serve it:
  - **Web Distribution** for HTTP/HTTPS content.
  - **RTMP Distribution** (legacy) for media streaming.

- **Cache Behaviors**  
  Rules that specify how CloudFront handles requests for specific URL path patterns: TTL settings, allowed HTTP methods, headers, cookies, and query strings.

---

## 3. Core Features

- **Global Scale**  
  Over 400 edge locations and 20 regional edge caches worldwide.

- **Protocol Optimizations**  
  Supports HTTP/2, IPv6, Gzip & Brotli compression.

- **Security**  
  Integrated SSL/TLS, free certificates via ACM, AWS WAF integration, and AWS Shield for DDoS protection.

- **Access Controls**  
  Signed URLs and Signed Cookies for restricting access to private content.

- **Invalidations**  
  On-demand cache invalidation (first 1,000 paths per month are free).

- **Geo-Restriction**  
  Whitelist or blacklist viewers by country.

- **Lambda@Edge**  
  Execute lightweight functions at edge locations to customize request/response behavior.

---

## 4. Request Flow

1. Viewer requests an asset (e.g. `https://cdn.example.com/image.jpg`).  
2. DNS routes the request to the nearest edge location.  
3. **Cache Hit**: Content is served directly from the edge cache.  
4. **Cache Miss**: CloudFront fetches the object from the origin, caches it, and returns it to the viewer.

---

## 5. Integrations

- **Amazon S3** for static asset storage.  
- **Elastic Load Balancing (ALB/NLB)** for dynamic web content.  
- **Amazon API Gateway** for API acceleration.  
- **Amazon Route 53** for DNS management and failover.  
- **Lambda@Edge** for custom logic at the network edge.  
- **AWS WAF & Shield** for application-layer security and DDoS protection.

---

## 6. Common Use Cases

- **Static Website Hosting** (SPAs, landing pages).  
- **Video on Demand & Live Streaming** (HLS, DASH).  
- **API Acceleration** for REST or GraphQL endpoints.  
- **Software Distribution** (application updates, binaries).  
- **DDoS Mitigation** with AWS Shield integration.

---

## 7. Benefits

- **Lower Latency** and faster load times for end users.  
- **Automatic Scaling** to handle traffic spikes without manual intervention.  
- **Reduced Origin Load** and bandwidth costs.  
- **Pay-as-You-Go Pricing** with no upfront fees.  
- **Built-In Security** features including encryption and access controls.

---

## 8. Pricing Model

- **Data Transfer Out** charged per GB (varies by region).  
- **HTTP/HTTPS Requests** charged per million requests.  
- **Invalidations**: first 1,000 paths per month free, then per 1,000 paths.  
- **Lambda@Edge** invocations and compute time billed separately.

---

## 9. Best Practices

1. **Fine-Tune Cache TTLs**  
   Use `Cache-Control` headers and multiple cache behaviors to optimize freshness vs. hit ratio.

2. **Enable Compression**  
   Turn on Gzip or Brotli to reduce payload sizes.

3. **Use ACM Certificates**  
   Deploy free SSL/TLS certificates with automatic renewal.

4. **Leverage Geo-Restrictions**  
   Restrict or allow access by geographic location when needed.

5. **Monitor in Real-Time**  
   Enable CloudFront real-time metrics and CloudWatch alarms for visibility into performance and errors.
