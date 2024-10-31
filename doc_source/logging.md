# Logging web ACL traffic<a name="logging"></a>

* it can be enabled
* logging detailed information about traffic / analyzed -- by your -- web ACL
  * time / AWS WAF received a web request -- from your -- AWS resource
  * the request itself
  * rules / the request matched
* places | forward your logs
  * Amazon CloudWatch Logs log group,
  * Amazon Simple Storage Service \(Amazon S3\) bucket,
  * Amazon Kinesis Data Firehose

**Topics**
+ [Pricing for logging web ACL traffic information](logging-pricing.md)
+ [AWS WAF logging destinations](logging-destinations.md)
+ [Managing logging for a web ACL](logging-management.md)
+ [Log Fields](logging-fields.md)
+ [Log Examples](logging-examples.md)