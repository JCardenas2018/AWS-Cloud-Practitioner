# 30 Amazon RDS Multiple-Choice Questions

1. Which RDS feature provides automated point-in-time recovery of your database instance?  
   - A. Read Replica  
   - B. Automated Backups  
   - C. Snapshots  
   - D. Multi-AZ Deployment  

2. What is the maximum retention period you can configure for automated RDS backups?  
   - A. 7 days  
   - B. 35 days  
   - C. 60 days  
   - D. 90 days  

3. A Multi-AZ deployment in RDS uses what type of replication?  
   - A. Asynchronous  
   - B. Synchronous  
   - C. Logical  
   - D. Manual  

4. Which engine is NOT supported by Amazon RDS?  
   - A. MariaDB  
   - B. Oracle  
   - C. MongoDB  
   - D. PostgreSQL  

5. How many read replicas are supported per RDS primary instance?  
   - A. 3  
   - B. 5  
   - C. 15  
   - D. Unlimited  

6. Which RDS storage type offers the lowest latency and highest IOPS?  
   - A. Magnetic (standard)  
   - B. General Purpose SSD (gp2/gp3)  
   - C. Provisioned IOPS SSD (io1/io2)  
   - D. Throughput Optimized HDD (st1)  

7. To enable IAM database authentication on RDS, you must:  
   - A. Enable encryption at rest  
   - B. Enable the option “IAM DB Authentication”  
   - C. Use a Multi-AZ deployment  
   - D. Attach an IAM role to the DB subnet group  

8. Which RDS engine supports serverless operation?  
   - A. MySQL  
   - B. PostgreSQL  
   - C. Aurora (MySQL-compatible)  
   - D. SQL Server  

9. For Aurora Global Database, how many secondary regions can you replicate to?  
   - A. 1  
   - B. 2  
   - C. 5  
   - D. 15  

10. What feature lets you run SQL queries directly against an Aurora Serverless cluster without managing connections?  
    - A. Data API  
    - B. Performance Insights  
    - C. Proxy  
    - D. IAM authentication  

11. Which RDS monitoring tool provides fine-grained performance metrics and visualizations?  
    - A. CloudWatch Alarms  
    - B. Enhanced Monitoring  
    - C. Performance Insights  
    - D. CloudTrail Logs  

12. Which parameter group change requires a reboot of the RDS instance to take effect?  
    - A. A dynamic parameter  
    - B. A static parameter  
    - C. Adding a tag  
    - D. Enabling backups  

13. What does RDS deletion protection prevent?  
    - A. Accidental snapshot deletion  
    - B. Dropping the primary instance  
    - C. Altering security groups  
    - D. Changing the instance class  

14. Which RDS feature allows you to apply database engine patches automatically?  
    - A. Maintenance Window  
    - B. Auto Minor Version Upgrade  
    - C. Automated Backups  
    - D. Multi-AZ  

15. To encrypt data at rest for an RDS instance, you must:  
    - A. Use SSL/TLS for connections  
    - B. Enable storage encryption when creating the instance  
    - C. Enable IAM authentication  
    - D. Use a dedicated KMS key only  

16. When promoting a read replica to standalone, which replication type does it become?  
    - A. Multi-AZ standby  
    - B. Primary instance  
    - C. S3 export source  
    - D. Snapshot only  

17. Which AWS service can migrate an on-premises database to RDS with minimal downtime?  
    - A. AWS DataSync  
    - B. AWS Database Migration Service (DMS)  
    - C. AWS Transfer Family  
    - D. AWS Glue  

18. Which RDS engine supports “parallel query” for faster analytics?  
    - A. MySQL  
    - B. MariaDB  
    - C. Aurora MySQL  
    - D. Oracle  

19. A custom option group in RDS is used to:  
    - A. Define parameter values  
    - B. Enable additional database features (e.g., Oracle TDE)  
    - C. Configure security groups  
    - D. Control backup retention  

20. Which network feature ensures your RDS instance is not publicly accessible?  
    - A. PubliclyAccessible=false  
    - B. Multi-AZ=true  
    - C. AutoMinorVersionUpgrade=false  
    - D. StorageEncrypted=true  

21. RDS Proxy improves application availability by:  
    - A. Caching queries  
    - B. Managing and pooling connections  
    - C. Encrypting traffic  
    - D. Auto-scaling storage  

22. In a cross-Region read replica setup, what type of replication is used?  
    - A. Synchronous  
    - B. Asynchronous  
    - C. Logical  
    - D. Batch  

23. Which metric would you monitor to detect CPU pressure on an RDS instance?  
    - A. WriteIOPS  
    - B. FreeStorageSpace  
    - C. CPUUtilization  
    - D. DatabaseConnections  

24. Which feature allows you to pause and resume compute on Aurora Serverless v1?  
    - A. PauseCompute  
    - B. ScalingConfiguration  
    - C. Data API  
    - D. Serverless Mode  

25. What is the default maximum number of parameters you can set in a DB parameter group?  
    - A. 100  
    - B. 500  
    - C. 1000  
    - D. 5000  

26. To capture detailed audit logs for MySQL on RDS, you enable:  
    - A. General log and slow query log  
    - B. Error log only  
    - C. Audit logs (requires option group)  
    - D. Performance Insights  

27. Which Multi-AZ failover action is automatic by default?  
    - A. DNS endpoint switch  
    - B. Snapshot creation  
    - C. Parameter group update  
    - D. Manual approval  

28. Which of these RDS engines supports logical replication slots?  
    - A. Oracle  
    - B. SQL Server  
    - C. PostgreSQL  
    - D. MariaDB  

29. Which CLI command resets a DB parameter group to default values?  
    - A. aws rds reset-db-parameter-group  
    - B. aws rds modify-db-parameter-group --reset  
    - C. aws rds restore-db-defaults  
    - D. aws rds delete-db-parameter-group  

30. For high-traffic read scaling with Aurora, you should provision:  
    - A. Many small primary instances  
    - B. Multiple reader endpoints (Aurora Replicas)  
    - C. Larger storage  
    - D. Larger DB subnet group  

---

## Correct Answers

1. B  
2. B  
3. B  
4. C  
5. B  
6. C  
7. B  
8. C  
9. D  
10. A  
11. C  
12. B  
13. B  
14. B  
15. B  
16. B  
17. B  
18. C  
19. B  
20. A  
21. B  
22. B  
23. C  
24. B  
25. C  
26. C  
27. A  
28. C  
29. A  
30. B  
