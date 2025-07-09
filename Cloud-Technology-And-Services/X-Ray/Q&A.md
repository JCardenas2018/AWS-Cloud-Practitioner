# 30 AWS X-Ray Multiple-Choice Questions

1. AWS X-Ray is primarily used for:  
   - A. Log aggregation  
   - B. Distributed tracing  
   - C. Metrics collection  
   - D. Security auditing  

2. In X-Ray, a **segment** represents:  
   - A. A subset of sampled requests  
   - B. Work done by a single service or resource  
   - C. A group of traces  
   - D. An error event  

3. A **subsegment** in X-Ray is used to:  
   - A. Group multiple segments  
   - B. Capture detailed timing for downstream calls  
   - C. Specify sampling rules  
   - D. Store annotation data  

4. X-Ray reduces overhead by tracing only a percentage of requests, a process called:  
   - A. Filtering  
   - B. Sampling  
   - C. Throttling  
   - D. Aggregation  

5. The X-Ray daemon listens for UDP packets on which port by default?  
   - A. 2000  
   - B. 2001  
   - C. 3000  
   - D. 3001  

6. To capture outbound HTTP(S) calls in a Node.js application, you use:  
   - A. `AWSXRay.captureHTTPsGlobal(require('http'))`  
   - B. `AWSXRay.captureHTTPsGlobal(require('https'))`  
   - C. Both A and B  
   - D. Neither A nor B  

7. The default retention period for X-Ray trace data is:  
   - A. 7 days  
   - B. 14 days  
   - C. 30 days  
   - D. 90 days  

8. To create or modify sampling rules in X-Ray, you call:  
   - A. PutTraceSegments  
   - B. CreateSamplingRule  
   - C. GetSamplingRules  
   - D. BatchGetTraces  

9. You add custom key/value data to traces that you want to filter on via:  
   - A. Metadata  
   - B. Annotations  
   - C. Tags  
   - D. Labels  

10. The visual **Service Map** in X-Ray shows:  
    - A. Only error rates  
    - B. Service dependencies with latency and error annotations  
    - C. IAM roles for each service  
    - D. Sampling rates for each endpoint  

11. Which language is **not** supported by the official X-Ray SDK?  
    - A. Java  
    - B. Python  
    - C. PHP  
    - D. Go  

12. To forward trace data from EC2 to X-Ray, you must install:  
    - A. CloudWatch agent  
    - B. X-Ray daemon  
    - C. SSM agent  
    - D. Kinesis agent  

13. You can filter which traces appear in the console by writing:  
    - A. SQL queries  
    - B. Filter expressions  
    - C. Regular expressions  
    - D. Simple text search  

14. X-Ray encrypts trace data at rest using:  
    - A. SSE-S3  
    - B. SSE-KMS  
    - C. Client-side keys  
    - D. No encryption  

15. The environment variable used to point the SDK at a nondefault daemon endpoint is:  
    - A. `AWS_XRAY_DAEMON_ADDRESS`  
    - B. `X_RAY_DAEMON`  
    - C. `XRAY_ENDPOINT`  
    - D. `TRACE_DAEMON_ADDR`  

16. To instrument an Express.js application, you insert middleware calls:  
    - A. `AWSXRay.express.openSegment('App')`  
    - B. `AWSXRay.express.closeSegment()`  
    - C. Both A and B  
    - D. Neither A nor B  

17. X-Ray propagates trace context via the HTTP header:  
    - A. `X-Amzn-Trace-Id`  
    - B. `Trace-Context`  
    - C. `X-Trace-Id`  
    - D. `X-Amzn-Trace-Context`  

18. A **sampling rule** can specify both a fixed rate and a reservoir size using:  
    - A. `FixedRate` and `ReservoirSize`  
    - B. `SampleRate` and `MaxCount`  
    - C. `Rate` and `Limit`  
    - D. `Percentage` and `Bucket`  

19. To enable X-Ray tracing in API Gateway, you must:  
    - A. Add a Lambda authorizer  
    - B. Enable X-Ray tracing in the API settings  
    - C. Create a sampling rule  
    - D. Install the X-Ray SDK  

20. The “Default” sampling rule by AWS uses a fixed rate of:  
    - A. 0.01%  
    - B. 0.1%  
    - C. 1%  
    - D. 5%  

21. You can export X-Ray trace data to S3 by creating an:  
    - A. Export task in the X-Ray console or CLI  
    - B. CloudWatch Logs subscription filter  
    - C. Kinesis Firehose delivery stream  
    - D. CloudTrail trail  

22. X-Ray Analytics lets you:  
    - A. Write SQL queries against trace segments  
    - B. Generate histograms and find anomalous traces  
    - C. Export logs to QuickSight  
    - D. Predict future latencies  

23. Which AWS service automatically injects tracing headers into Lambda functions?  
    - A. AWS Lambda (when X-Ray tracing is enabled)  
    - B. API Gateway  
    - C. CloudWatch Events  
    - D. SNS  

24. To define a group for trace filtering, you use the CloudFormation resource:  
    - A. `AWS::XRay::Group`  
    - B. `AWS::XRay::Filter`  
    - C. `AWS::XRay::TraceGroup`  
    - D. `AWS::XRay::SamplingRule`  

25. Granting an application permission to send segments to X-Ray requires the IAM action:  
    - A. `xray:PutTraceSegments`  
    - B. `xray:SendSegments`  
    - C. `xray:CreateTrace`  
    - D. `xray:RecordTrace`  

26. The CloudFormation resource to create a sampling rule is:  
    - A. `AWS::XRay::SamplingRule`  
    - B. `AWS::XRay::SampleRule`  
    - C. `AWS::XRay::Rule`  
    - D. `AWS::XRay::SamplingConfig`  

27. By default, X-Ray retains traces for:  
    - A. 7 days  
    - B. 14 days  
    - C. 30 days  
    - D. 90 days  

28. The minimum service-level reservoir size for a sampling rule is:  
    - A. 0  
    - B. 1  
    - C. 10  
    - D. 100  

29. You can run the X-Ray daemon as a Docker container on ECS by using the image:  
    - A. `amazon/aws-xray-daemon`  
    - B. `amazon/xray-daemon`  
    - C. `aws/xray-daemon`  
    - D. `xray/daemon`  

30. A valid trace ID in X-Ray begins with:  
    - A. `Root=1-`  
    - B. `Trace=`  
    - C. `XRay=1-`  
    - D. `ID=1-`  

---

## Answers

1. B  
2. B  
3. B  
4. B  
5. B  
6. C  
7. C  
8. B  
9. B  
10. B  
11. C  
12. B  
13. B  
14. B  
15. A  
16. C  
17. A  
18. A  
19. B  
20. C  
21. A  
22. B  
23. A  
24. A  
25. A  
26. A  
27. C  
28. B  
29. A  
30. A  
