# Pricing for logging web ACL traffic information<a name="logging-pricing"></a>

* == costs -- associated with -- each log destination type
  * \+ own charges for using AWS WAF 
    * see [AWS WAF Pricing](http://aws.amazon.com/waf/pricing/)
  * for
    + **CloudWatch Logs**
      + charges -- are for -- vended log delivery
      + see [Amazon CloudWatch Logs Pricing](http://aws.amazon.com/cloudwatch/pricing/)
    + **Amazon S3 buckets**
      + charges == charges for CloudWatch Logs vended log delivery to the Amazon S3 + charges of using Amazon S3
      + see [Amazon S3 Pricing](http://aws.amazon.com/s3/pricing/)\. 
        + For CloudWatch Logs vended log delivery to the Amazon S3, see [Amazon CloudWatch Logs Pricing](http://aws.amazon.com/cloudwatch/pricing/)
    + **Kinesis Data Firehose**
      + see [Amazon Kinesis Data Firehose Pricing](http://aws.amazon.com/kinesis/data-firehose/pricing/)
