# Web access control lists \(web ACLs\)<a name="web-acl"></a>

* web ACL
  * allows
    * 👀fine-grained control | ALL HTTP\(S\) web requests / your protected resource -- responds -- to 👀

* 👀possible criteria -- to -- ALLOW or BLOCK requests 👀 
  + IP address origin -- of the -- request
  + Country of origin -- of the -- request
  + String match or regular expression \(regex\) match -- in a -- part of the request
  + Size of a particular part -- of the -- request
  + Detection of malicious SQL code or scripting 
  + combination of previous ones
    + -- via --  logical operators
+ 👀possible criteria -- to -- COUNT or BLOCK requests 👀
  + meet the specified conditions
  + \> specified number of requests | ANY 5\-minute period
+ run CAPTCHA puzzles and silent client session challenges -- against -- requests 

* AWS WAF rule statements
  * == matching criteria + action to take
    * [AWS WAF rule action](waf-rule-action.md)
  * [AWS WAF rule statements](waf-rule-statements.md)
  * ways to define them
    * | your web ACL or
    * | reusable rule groups / used -- by -- your web ACL

* steps to specify your web request inspection & handling criteria
  1. choose the web ACL default action
     1. possible ones
        1. Allow or
        2. Block
     2. see [Deciding on the default action for a web ACL](web-acl-default-action.md)
  2. add any rule groups / you want to use | your web ACL
     1. Managed rule groups -- usually contain -- rules / block web requests
     2. see [Rule groups](waf-rule-groups.md)
  3. specify additional matching criteria & handling instructions | >=1 rules
     1. -- via -- `AND` or `OR`
     2. if you want to negate a rule option -> use `NOT` statement
     3. rate-based rule
        1. see [Rules](waf-rules.md)

* if you add >=1 rule | web ACL -> AWS WAF evaluates the rules -- based on the -- order / they're listed for the web ACL
  * see [Web ACL rule and rule group evaluation](web-acl-processing.md)

* when you create a web ACL -> you specify the types of resources / you want to use it with
  * see [Creating a web ACL](web-acl-creating.md)
* once web ACL is defined -> web ACL -- can be associated with -- your resources
  * see [Associating or disassociating a web ACL with an AWS resource](web-acl-associating-aws-resource.md) 

## How AWS resources handle response delays from AWS WAF<a name="web-acl-processing-resource-default"></a>

* scenario
  * AWS WAF -- might encounter an -- internal error / delays the response -- to -- associated AWS resources
* 👀typical behavior 👀
  * CloudFront allows the request or serves the content
  * Regional services deny the request & do NOT serve the content

**Topics**
+ [How AWS resources handle response delays from AWS WAF](#web-acl-processing-resource-default)
+ [Web ACL rule and rule group evaluation](web-acl-processing.md)
+ [Deciding on the default action for a web ACL](web-acl-default-action.md)
+ [Body inspection size limits for CloudFront web ACLs](web-acl-setting-body-inspection-limit.md)
+ [CAPTCHA, challenge, and token domain configuration for a web ACL](web-acl-captcha-challenge-token-domains.md)
+ [Working with web ACLs](web-acl-working-with.md)