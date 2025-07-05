## Storage Classes

Amazon S3 provides multiple storage classes to help you optimize cost and performance based on your data access patterns:

### S3 Standard
- **Cost:** Approx. $0.023 per GB-month (US East, first 50 TB)  
- **Availability & Durability:** 99.99% availability, 11 nines durability  
- **Use Cases:** Frequently accessed data; websites, content distribution, dynamic workloads  

### S3 Intelligent-Tiering
- **Cost:** $0.023 per GB-month for frequent tier; $0.0125 per GB-month for infrequent tier; monitoring & automation fee $0.0025 per 1 000 objects  
- **Availability & Durability:** Same as Standard  
- **Use Cases:** Unknown or changing access patterns; large datasets with unpredictable access  

### S3 Standard-Infrequent Access (Standard-IA)
- **Cost:** Approx. $0.0125 per GB-month (storage) + $0.01 per GB retrieval fee  
- **Availability & Durability:** 99.9% availability, 11 nines durability  
- **Use Cases:** Long-lived but infrequently accessed data; backups, disaster recovery  

### S3 One Zone-Infrequent Access (One Zone-IA)
- **Cost:** Approx. $0.01 per GB-month (storage) + $0.01 per GB retrieval fee  
- **Availability & Durability:** 99.5% availability, 11 nines durability (single AZ)  
- **Use Cases:** Infrequently accessed, non-critical data that can be recreated elsewhere; secondary backups  

### S3 Glacier Instant Retrieval
- **Cost:** Approx. $0.01 per GB-month storage + $0.03 per 1 000 requests  
- **Retrieval:** Millisecond access  
- **Use Cases:** Archive data requiring immediate access; media archives, healthcare  

### S3 Glacier Flexible Retrieval (formerly Glacier)
- **Cost:** Approx. $0.004 per GB-month storage + retrieval fees ($0.01 per GB expedited)  
- **Retrieval:** Expedited (1–5 min), Standard (3–5 hours), Bulk (5–12 hours)  
- **Use Cases:** Long-term archive where occasional retrieval is needed; compliance, digital preservation  

### S3 Glacier Deep Archive
- **Cost:** Approx. $0.00099 per GB-month storage + retrieval fees ($0.02 per GB standard)  
- **Retrieval:** Standard (12 hours), Bulk (48 hours)  
- **Use Cases:** Lowest-cost, long-term data retention; regulatory archives, digital preservation  

## Storage Classes (Detailed)

Below is a comprehensive overview of Amazon S3 storage classes, including detailed pricing, performance characteristics, minimum storage durations, and typical use cases.

| Storage Class                        | Storage Price (per GB-month)                                          | Request Pricing (per 1 000 requests)                                      | Retrieval & Transition Fees                                        | Min. Storage Duration | Data Access SLA    | Durability   | Typical Use Cases                                              |
|--------------------------------------|----------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------|-----------------------|--------------------|--------------|----------------------------------------------------------------|
| **S3 Standard**                      | • $0.023 (first 50 TB)¹<br>• $0.022 (next 450 TB)²<br>• $0.021 (over 500 TB)³ | • PUT/COPY/POST/LIST: $0.005<br>• GET: $0.0004                              | • No retrieval fee<br>• Lifecycle transition: $0.01                | 0 days                | 99.99% availability | 11 nines     | Websites, streaming, dynamic content, mobile apps, gaming      |
| **S3 Intelligent-Tiering**           | • $0.023 (frequent tier)¹<br>• $0.0125 (infrequent tier)¹             | Same as Standard                                                           | • Monitoring & automation: $0.0025 per 1 000 objects               | 30 days               | 99.9% availability   | 11 nines     | Unknown or changing access patterns; data lakes; analytics     |
| **S3 Standard-IA**                   | • $0.0125                                                            | • PUT/COPY/POST/LIST: $0.01<br>• GET: $0.001                                 | • Retrieval: $0.01 per GB                                         | 30 days               | 99.9% availability   | 11 nines     | Infrequently accessed data; backups; DR; long-term storage     |
| **S3 One Zone-IA**                   | • $0.010                                                             | • PUT/COPY/POST/LIST: $0.01<br>• GET: $0.001                                 | • Retrieval: $0.01 per GB                                         | 30 days               | 99.5% availability   | 11 nines     | Secondary backups; re-creatable data; lower-cost infrequent access |
| **S3 Glacier Instant Retrieval**     | • $0.01                                                              | • PUT: $0.05<br>• GET: $0.005                                                | • Retrieval: Free (millisecond)<br>• Lifecycle transition: $0.05   | 90 days               | n/a                 | 11 nines     | Archive with immediate access; media archives; regulatory needs |
| **S3 Glacier Flexible Retrieval**    | • $0.004                                                             | • PUT: $0.05<br>• GET Expedited: $0.03<br>• GET Standard: $0.01              | • Expedited: $0.03 per GB (1–5 min)<br>• Standard: no extra (3–5 hrs)<br>• Bulk: $0.0025 per GB (5–12 hrs) | 90 days               | n/a                 | 11 nines     | Long-term archives; compliance; digital preservation            |
| **S3 Glacier Deep Archive**          | • $0.00099                                                           | • PUT: $0.05<br>• GET Standard: $0.02                                       | • Standard retrieval: $0.02 per GB (12 hrs)<br>• Bulk: $0.0025 per GB (48 hrs) | 180 days              | n/a                 | 11 nines     | Lowest-cost archival; regulatory and legal archives            |
| **S3 Outposts**                      | Custom pricing                                                       | Custom pricing                                                             | Custom fees                                                        | 90 days               | 99.9% availability   | 11 nines     | On-premises object storage for data residency requirements     |

> **Free Tier:** 5 GB of Standard storage, 20 000 GET, and 2 000 PUT requests per month for 12 months.

> **Notes:** Pricing varies by AWS Region. Always consult the [AWS S3 Pricing page](https://aws.amazon.com/s3/pricing/) for your specific region.

---  
First 50 TB/month in US East (Ohio). ² Next 450 TB/month. ³ Over 500 TB/month.


> **Note:** Pricing is region-dependent and subject to change. Refer to the [AWS S3 Pricing page](https://aws.amazon.com/s3/pricing/) for the latest rates.
