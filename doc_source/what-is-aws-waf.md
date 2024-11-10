# What are AWS WAF, AWS Shield, and AWS Firewall Manager?<a name="what-is-aws-waf"></a>

* [AWS WAF](waf-chapter.md) + [AWS Shield](shield-chapter.md) + [AWS Firewall Manager](fms-chapter.md)
  * create a comprehensive security solution

**Topics**
+ [AWS WAF](#waf-intro)
+ [AWS Shield](#ddos-intro)
+ [AWS Firewall Manager](#fms-intro)

## AWS WAF<a name="waf-intro"></a>

* allowed behaviors / -- can be chosen by -- AWS WAF
  + **Allow ALL requests -- except the -- ones / you specify**
    + use cases
      + 👀if you serve content for a PUBLIC website, BUT want to block requests from attackers 👀 
        + public website -- served via --
          + Amazon CloudFront,
          + Amazon API Gateway,
          + Application Load Balancer,
          + AWS AppSync,
          + Amazon Cognito
  + **Block ALL requests -- except the -- ones / you specify**
    + use cases
      + 👀if you serve content for restricted website / users -- are identified by -- properties | website👀
        + _Example of those properties:_ IP addresses 
  + **Count requests / -- match -- your criteria**
    + use cases
      + track your web traffic / NO modified how to handle it
        + == general monitoring
      + test your new web requests / handle rules 
        + == previous step to allow or block requests  
  + **Run CAPTCHA or challenge checks -- against -- requests / match your criteria**
    + use cases
      + reduce bot traffic -- to your -- protected resources

* benefits of using AWS WAF
  + TODO:Additional protection against web attacks using criteria that you specify\. You can define criteria using characteristics of web requests such as the following:
    + IP addresses that requests originate from\.
    + Country that requests originate from\.
    + Values in request headers\.
    + Strings that appear in requests, either specific strings or strings that match regular expression \(regex\) patterns\.
    + Length of requests\.
    + Presence of SQL code that is likely to be malicious \(known as *SQL injection*\)\.
    + Presence of a script that is likely to be malicious \(known as *cross\-site scripting*\)\.
  + rules
    + | web request, can
      + allow, /
        + match specified criteria
      + block, /
        + match specified criteria
        + \> a specified number of requests | ANY 5\-minute period
      + count, /
        + match specified criteria
        + \> a specified number of requests | ANY 5\-minute period 
    + -- can be reused for -- MULTIPLE web applications
  + Managed rule groups -- from --
    + AWS
    + AWS Marketplace
  + Real\-time metrics and sampled web requests
  + Automated administration -- via -- AWS WAF API
  + minimize the effects of a DDoS attack -- via -- AWS WAF web ACLs 

* 👀 if you want granular control over the protections -> use AWS WAF ALONE 👀
* see [AWS WAF](waf-chapter.md)

## AWS Shield<a name="ddos-intro"></a>

* types
  * AWS Shield Standard
    * free
    * automatically included 
  * AWS Shield Advanced
    * provides 
      * expanded DDoS attack protection -- for -- your
        * Amazon EC2 instances, 
        * Elastic Load Balancing load balancers,
        * CloudFront distributions, 
        * Route 53 hosted zones,
        * AWS Global Accelerator standard accelerators
      * automatic application layer DDoS mitigation
      * advanced event visibility
      * dedicated support -- from the -- Shield Response Team \(SRT\)
    * pricing
      * extra
    * use cases
      * high visibility websites
      * prone to frequent DDoS attacks
    * see [AWS Shield Advanced capabilities and options](ddos-advanced-summary-capabilities.md)
* allows
  * additional protecting  against DDoS attacks
* see [Deciding whether to subscribe to AWS Shield Advanced and apply additional protections](ddos-advanced-summary-deciding.md)\.

## AWS Firewall Manager<a name="fms-intro"></a>

* TODO: 
AWS Firewall Manager simplifies your administration and maintenance tasks across multiple accounts and resources for a variety of protections, including AWS WAF, AWS Shield Advanced, Amazon VPC security groups, AWS Network Firewall, and Amazon Route 53 Resolver DNS Firewall\. With Firewall Manager, you set up your protections just once and the service automatically applies them across your accounts and resources, even as you add new accounts and resources\. 

For more information about Firewall Manager, see [AWS Firewall Manager](fms-chapter.md)\.