## Amazon DocumentDB: Cost & Use Cases

### Cost Overview (US East - N. Virginia, July 2025)

| Component                        | Pricing                                                  |
| -------------------------------- | -------------------------------------------------------- |
| **Instance Class**               | db.r5.large: \$0.277/hr                                  |
|                                  | db.r5.xlarge: \$0.554/hr                                 |
|                                  | db.r5.2xlarge: \$1.108/hr                                |
|                                  | db.r6g.large: \$0.226/hr                                 |
|                                  | db.r6g.xlarge: \$0.452/hr                                |
| **Storage**                      | \$0.10 per GB-month (provisioned)                        |
| **I/O Requests**                 | \$0.20 per 1 million requests                            |
| **Backup Storage**               | First 100% of cluster storage free; \$0.021 per GB-month |
| **Data Transfer (inter-AZ)**     | Free                                                     |
| **Data Transfer (cross-region)** | \$0.02 per GB                                            |

> **Note:** Pricing varies by Region and may change; consult the [DocumentDB Pricing](https://aws.amazon.com/documentdb/pricing/) page.

### Common Use Cases

* **Content Management**
  Store and query JSON documents for blogs, catalogs, user profiles with flexible schemas.

* **Internet of Things (IoT)**
  Ingest and analyze semi-structured telemetry and sensor data at scale.

* **Mobile & Web Applications**
  Rapid development and iteration using a managed document database for app backends.

* **Real-Time Analytics**
  Perform low-latency queries and aggregations on large document collections.

* **Metadata Store**
  Maintain metadata for media processing pipelines (images, videos, logs).

* **Catalog & Inventory Management**
  Handle dynamic product catalogs and inventory with varied attribute sets.

* **Gaming Leaderboards & Profiles**
  Store player state, preferences, and high-score tables with low-latency access.

* **Fraud Detection**
  Maintain adaptable document models for storing transaction patterns and flags.

> **Tip:** Optimize costs by right-sizing instances, leveraging Graviton2-based classes (r6g), and cleaning up unused snapshots and collections.
