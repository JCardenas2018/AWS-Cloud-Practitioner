# 30 Amazon Route 53 Multiple-Choice Questions

1. Which record type in Route 53 lets you point your apex domain (example.com) to an ELB?  
   - A. CNAME  
   - B. ALIAS A  
   - C. TXT  
   - D. MX  

2. What is the default TTL (time to live) for a new record set if you don’t specify one?  
   - A. 30 seconds  
   - B. 300 seconds  
   - C. 3600 seconds  
   - D. 86400 seconds  

3. A Private Hosted Zone is visible to:  
   - A. Everyone on the internet  
   - B. Only specified EC2 instances via security groups  
   - C. Resources within the associated VPC(s)  
   - D. Only if you enable DNSSEC  

4. Which routing policy returns multiple healthy records in a single response to the DNS resolver?  
   - A. Simple  
   - B. Weighted  
   - C. Multivalue Answer  
   - D. Latency-based  

5. To distribute traffic in the ratio 70:30 between two endpoints, you use:  
   - A. Latency-based routing  
   - B. Weighted routing  
   - C. Geo-proximity routing  
   - D. Failover routing  

6. Which health check type can monitor TCP port 443 on an endpoint?  
   - A. HTTP  
   - B. HTTPS  
   - C. TCP  
   - D. All of the above  

7. Latency-based routing chooses the endpoint based on:  
   - A. Geolocation of the client  
   - B. Weighted distribution  
   - C. Measured network latency between client and region  
   - D. DNS resolver speed  

8. What CLI command lists all record sets in a hosted zone?  
   - A. `aws route53 list-hosted-zones`  
   - B. `aws route53 list-resource-record-sets`  
   - C. `aws route53 list-records`  
   - D. `aws route53 list-zone-records`  

9. Which record type would you use to verify domain ownership for ACM certificates?  
   - A. A  
   - B. CNAME  
   - C. TXT  
   - D. SRV  

10. DNSSEC in Route 53 helps prevent:  
    - A. DDoS attacks  
    - B. DNS cache poisoning  
    - C. IP spoofing  
    - D. Latency spikes  

11. Geolocation routing allows you to route based on:  
    - A. Client’s IP address location  
    - B. DNS resolver’s IP location  
    - C. Both A and B  
    - D. Neither A nor B  

12. A Failover routing policy requires you to configure:  
    - A. Primary and secondary record sets with health checks  
    - B. Weight values summing to 100  
    - C. Geolocation maps  
    - D. Traffic policy records  

13. Which Route 53 feature lets you visually design complex routing logic?  
    - A. Traffic Flow (Traffic Policies)  
    - B. Health Dashboard  
    - C. Resolver Query Logging  
    - D. Hosted Zone Editor  

14. To register a new domain through Route 53, you use:  
    - A. create-hosted-zone  
    - B. register-domain  
    - C. create-domain  
    - D. purchase-domain  

15. Cross-account DNS resolution between on-premises and AWS VPC uses:  
    - A. Health checks  
    - B. Route 53 Resolver endpoints (inbound/outbound)  
    - C. Private Hosted Zones only  
    - D. Traffic policies  

16. Query logging in Route 53 logs queries to:  
    - A. CloudWatch Logs or S3  
    - B. CloudTrail  
    - C. Kinesis Data Streams  
    - D. DynamoDB  

17. In Weightless geo-proximity routing you can shift traffic by setting:  
    - A. Bias values  
    - B. Weight values  
    - C. TTL values  
    - D. Health check thresholds  

18. Which record type supports alias target but cannot have a TTL?  
    - A. A  
    - B. CNAME  
    - C. PTR  
    - D. TXT  

19. To change the health check threshold before marking an endpoint unhealthy, you adjust:  
    - A. RequestInterval  
    - B. FailureThreshold  
    - C. HealthThreshold  
    - D. CheckInterval  

20. Route 53’s domain transfer process typically takes:  
    - A. Minutes  
    - B. Hours  
    - C. 1–7 days  
    - D. 30 days  

21. A “glue record” in Route 53 is necessary when:  
    - A. You host your DNS outside AWS  
    - B. Your nameserver is within the zone it serves  
    - C. You use alias records  
    - D. You enable DNSSEC  

22. Which API call changes the comment on a health check?  
    - A. UpdateHealthCheck  
    - B. ChangeHealthCheck  
    - C. ModifyHealthCheck  
    - D. EditHealthCheck  

23. Route 53 charges extra for queries to:  
    - A. Private Hosted Zones  
    - B. Standard record lookups  
    - C. Latency, geolocation, and traffic-flow queries  
    - D. Medical record lookups  

24. To migrate DNS from another provider to Route 53 without downtime, you:  
    - A. Delete existing records immediately  
    - B. Lower TTL on old provider, create identical records in Route 53, then switch NS  
    - C. Use Traffic Flow policies  
    - D. Register a new domain  

25. Which record type routes based on request source continent?  
    - A. Geolocation  
    - B. Geo-proximity  
    - C. Latency-based  
    - D. Weighted  

26. You can fail over only HTTP(S) endpoints with:  
    - A. HTTP and HTTPS health checks  
    - B. TCP health checks  
    - C. DNS health checks  
    - D. None of the above  

27. A record set alias for an S3 website endpoint must specify alias target’s:  
    - A. DNSName and HostedZoneId  
    - B. IP address  
    - C. CNAME  
    - D. PTR record  

28. Which CLI command deletes a hosted zone (and all its records)?  
    - A. `aws route53 delete-hosted-zone --id ZONEID`  
    - B. `aws route53 remove-hosted-zone --id ZONEID`  
    - C. `aws route53 destroy-hosted-zone --zone-id ZONEID`  
    - D. `aws route53 purge-hosted-zone --id ZONEID`  

29. By default, how many health checks can you create per AWS account?  
    - A. 50  
    - B. 200  
    - C. 1,000  
    - D. 10,000  

30. To update multiple record sets atomically, you use:  
    - A. ChangeResourceRecordSets API with a batch of changes  
    - B. UpdateRecordSet API per record  
    - C. PutRecord API  
    - D. ModifyHostedZone API  

---

## Correct Answers

1. B  
2. C  
3. C  
4. C  
5. B  
6. D  
7. C  
8. B  
9. C  
10. B  
11. A  
12. A  
13. A  
14. B  
15. B  
16. A  
17. A  
18. A  
19. B  
20. C  
21. B  
22. A  
23. C  
24. B  
25. A  
26. A  
27. A  
28. A  
29. B  
30. A  
