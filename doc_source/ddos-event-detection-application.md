# Detection logic for application layer threats<a name="ddos-event-detection-application"></a>

AWS Shield Advanced provides web application layer detection for protected Amazon CloudFront distributions and Application Load Balancers\. When you protect these resource types with Shield Advanced, you can associate an AWS WAF web ACL with your protection to enable web application layer detection\. Shield Advanced consumes request data for the associated web ACL and builds a traffic baseline for your application\. Web application layer detection relies on the native integration between Shield Advanced and AWS WAF\. To learn more about application layer protections, including associating an AWS WAF web ACL to a Shield Advanced protected resource, see [AWS Shield Advanced application layer \(layer 7\) protections](ddos-app-layer-protections.md)\. 

For web application layer detection, Shield Advanced monitors application traffic and compares it to historic baselines looking for anomalies\. This monitoring covers total volume and the composition of traffic\. During a DDoS attack, we expect both the volume and composition of traffic to change, and Shield Advanced requires a statistically significant deviation in both to declare an event\. 

Shield Advanced performs its measurements against historical time windows\.  This approach reduces false positive notifications from legitimate changes in traffic volume or from changes in traffic that match an expected pattern, such as a sale that's offered at the same time each day\. 

**Note**  
Avoid false positives in your Shield Advanced protections by giving Shield Advanced time to establish baselines that represent normal, legitimate traffic patterns\. Associate a web ACL with your protected resource at least 24 hours before any planned event that might cause unusual patterns in your web traffic\. Shield Advanced web application layer detection is most accurate when it has observed 30 days of normal traffic\.

The time that Shield Advanced takes to detect an event is affected by how much change it observes in the volume of traffic\. For lower volume changes, Shield Advanced observes traffic for a longer period, in order to build confidence that an event is occurring\. For higher volume changes, Shield Advanced detects and reports an event more quickly\. 

**Note**  
You can architect your application to scale in response to elevated traffic or load to ensure that it is not affected by smaller request floods\. With Shield Advanced, your protected resources are covered by cost protection\. This helps protect you against unexpected increases in your cloud bill that might occur as the result of a DDoS attack\. To learn more about Shield Advanced cost protection, see [Requesting a credit in AWS Shield Advanced](request-refund.md)\.