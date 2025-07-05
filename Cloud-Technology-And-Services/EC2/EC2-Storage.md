## EC2 Storage Options Examples

* **EBS – General Purpose SSD (gp3)**

  * Performance: 3,000 IOPS and 125 MB/s by default (scalable up to 16,000 IOPS and 1,000 MB/s)
  * Use Cases: General purpose file systems, small databases, application servers.

* **EBS – Provisioned IOPS SSD (io2)**

  * Performance: Up to 64,000 IOPS and 1,000 MB/s
  * Use Cases: Mission-critical databases (Oracle, SAP), high-throughput transactional applications.

* **EBS – Throughput Optimized HDD (st1)**

  * Performance: Up to 500 MB/s per volume
  * Use Cases: Big data, data warehouses, log processing.

* **EBS – Cold HDD (sc1)**

  * Performance: Up to 250 MB/s per volume
  * Use Cases: Infrequently accessed data, backups, archival storage.

* **EBS – Magnetic (standard)**

  * Performance: Approximately 40–90 IOPS
  * Use Cases: Legacy applications, low-throughput workloads.

* **Instance Store (Ephemeral Volumes)**

  * Characteristics: Local NVMe storage, low latency
  * Use Cases: Caches, buffers, temporary files; data lost when instance stops or terminates.

* **Amazon EFS (Elastic File System)**

  * Type: Network file system (NFS) shared across multiple instances
  * Performance: Scales to hundreds of MB/s throughput
  * Use Cases: Concurrent access workloads, container storage, shared development environments.

* **Amazon FSx for Windows File Server**

  * Type: SMB/CIFS, Windows-native
  * Performance: Up to 2 GB/s throughput and 500,000 IOPS
  * Use Cases: Windows file share workloads, .NET applications, Microsoft SQL Server.
