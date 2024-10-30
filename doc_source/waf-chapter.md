# AWS WAF<a name="waf-chapter"></a>

* AWS WAF
  * := web application firewall /
    * lets you
      * monitor the HTTP\(S\) requests /
        * -- are forwarded to -- your protected web application resources
        * 👀resource types / can be protected 👀
          + Amazon CloudFront distribution
          + Amazon API Gateway REST API
          + Application Load Balancer
          + AWS AppSync GraphQL API
          + Amazon Cognito user pool
          + AWS App Runner service
          + applications / hosted | Amazon ECS containers
            + requirements
              + configure ECS -- with an -- Application Load Balancer / -- enabled for -- AWS WAF
                + see [Service Load Balancing](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-load-balancing.html)
      * control access -- to your -- content
        * -- based on -- criteria / you specify
          * _Example:_
            * IP addresses / requests originate from
            * values of query strings
    * service -- associated with -- your protected resource -> responds to requests with the
      * requested content, or
      * HTTP 403 status code \(Forbidden\), or
      * custom response

**Topics**
+ [How AWS WAF works](how-aws-waf-works.md)
+ [Getting started with AWS WAF](getting-started.md)
+ [Web access control lists \(web ACLs\)](web-acl.md)
+ [Rule groups](waf-rule-groups.md)
+ [Rules](waf-rules.md)
+ [Handling oversize web request components](waf-oversize-request-components.md)
+ [IP sets and regex pattern sets](waf-referenced-set-managing.md)
+ [Customized web requests and responses in AWS WAF](waf-custom-request-response.md)
+ [Labels on web requests](waf-labels.md)
+ [AWS WAF intelligent threat mitigation](waf-managed-protections.md)
+ [Logging web ACL traffic](logging.md)
+ [Listing IP addresses that are being rate limited by rate\-based rules](listing-managed-ips.md)
+ [Testing and tuning your AWS WAF protections](web-acl-testing.md)
+ [How AWS WAF works with Amazon CloudFront features](cloudfront-features.md)
+ [Security in your use of the AWS WAF service](security.md)
+ [AWS WAF quotas](limits.md)
+ [Migrating your AWS WAF Classic resources to AWS WAF](waf-migrating-from-classic.md)