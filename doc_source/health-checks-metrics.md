# Metrics commonly used for health checks<a name="health-checks-metrics"></a>

This section lists the Amazon CloudWatch metrics that are commonly used in health checks to measure application health during distributed denial of service \(DDoS\) events\. For full information about the CloudWatch metrics for each resource type, see the list that follows the table\. 

**Topics**
+ [Metrics used to monitor application health](#health-checks-metrics-common)
+ [Amazon CloudWatch metrics for each resource type](#health-checks-protected-resource-metrics)

## Metrics used to monitor application health<a name="health-checks-metrics-common"></a>


| Resource | Metric | Description | 
| --- | --- | --- | 
| Route 53 | `HealthCheckStatus` | The status of the health check endpoint\. | 
| CloudFront | `5xxErrorRate` | The percentage of all requests for which the HTTP status code is 5xx\. This indicates an attack that's impacting the application\. | 
| Application Load Balancer | `ActiveConnectionCount` | The number of concurrent TCP connections that are active from clients to the load balancer, and from the load balancer to targets\. | 
| Application Load Balancer | `ConsumedLCUs` | The number of load balancer capacity units \(LCU\) used by your load balancer\. | 
| Application Load Balancer | `HTTPCode_ELB_4XX_Count `  `HTTPCode_ELB_5XX_Count` | The number of HTTP 4xx or 5xx client error codes generated by the load balancer\. | 
| Application Load Balancer | `NewConnectionCount` | The number of new TCP connections established from clients to the load balancer, and from the load balancer to targets\. | 
| Application Load Balancer | `ProcessedBytes` | The number of bytes processed by the load balancer\. | 
| Application Load Balancer | `RejectedConnectionCount` | The number of connections that were rejected because the load balancer reached its maximum number of connections\. | 
| Application Load Balancer | `TargetConnectionErrorCount` | The number of connections that were not successfully established between the load balancer and the target\. | 
| Application Load Balancer | `TargetResponseTime` |  The time elapsed in seconds after the request leaves the load balancer and when it receives a response from the target\.  | 
| Application Load Balancer | `UnHealthyHostCount` | The number of targets that are considered unhealthy\. | 
| Network Load Balancer | `ActiveFlowCount` | The number of concurrent TCP connections from clients to targets\. | 
| Network Load Balancer | `ConsumedLCUs` | The number of load balancer capacity units \(LCU\) used by your load balancer\. | 
| Network Load Balancer | `NewFlowCount` |  The number of new TCP connections established from clients to targets\.  | 
| Network Load Balancer | `PeakPacketsPerSecond` | The highest average packet rate \(packets processed per second\), calculated every 10 seconds during the sampling window\. This metric includes health check traffic\. | 
|  Network Load Balancer  |  `ProcessedBytes`  |  The number of bytes processed by the load balancer, including TCP/IP headers\.  | 
| Global Accelerator |  `NewFlowCount`  | The number of new TCP connections established from clients to targets\. | 
| Global Accelerator | `ProcessedBytesIn` | The number of incoming bytes processed by the accelerator, including TCP/IP headers\. | 
| Amazon EC2 | `CPUUtilization` | The percentage of allocated EC2 compute units that are currently in use\. | 
| Amazon EC2 | `NetworkIn` | The number of bytes received by the instance on all network interfaces\. | 
| Amazon EC2 Auto Scaling | `GroupMaxSize` | The maximum size of the Auto Scaling group\. | 

## Amazon CloudWatch metrics for each resource type<a name="health-checks-protected-resource-metrics"></a>

For additional information about the metrics that are available for your protected resources, see the following sections in the resource guides: 
+ Amazon Route 53 – [Monitoring your resources with Amazon Route 53 health checks and Amazon CloudWatch](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/monitoring-cloudwatch.html) in the Amazon Route 53 Developer Guide\.
+ Amazon CloudFront – [Monitoring CloudFront with Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/monitoring-using-cloudwatch.html) in the Amazon CloudFront Developer Guide\.
+ Application Load Balancer – [CloudWatch metrics for your Application Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html) in the User Guide for Application Load Balancers\.
+ Network Load Balancer – [CloudWatch metrics for your Network Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html) in the User Guide for Network Load Balancers\.
+ AWS Global Accelerator – [Using Amazon CloudWatch with AWS Global Accelerator](https://docs.aws.amazon.com/global-accelerator/latest/dg/cloudwatch-monitoring.html) in the AWS Global Accelerator Developer Guide\.
+ Amazon Elastic Compute Cloud – [List the available CloudWatch metrics for your instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html) in the https://docs\.aws\.amazon\.com/AWSEC2/latest/UserGuide/\.
+ Amazon EC2 Auto Scaling – [Monitoring CloudWatch metrics for your Auto Scaling groups and instances](https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-monitoring.html) in the Amazon EC2 Auto Scaling User Guide\.