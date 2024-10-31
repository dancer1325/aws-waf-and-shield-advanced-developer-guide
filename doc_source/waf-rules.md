# Rules<a name="waf-rules"></a>

* AWS WAF rule
  * 👀defines ONLY | context of a rule group or web ACL, 👀  
    * how to inspect HTTP\(S\) web requests
      + likely malicious
        + scripts 
        + SQL code 
      + IP addresses or address ranges / requests -- originate -- from
      + Country or geographical location / requests -- originate -- from
      + Length of a specified part of the request
        + _Example:_ query string
      + Strings or regex / appear | request
      + Labels / prior rules | web ACL -- have added to the -- request      
    * action -- to take on a -- request, if it -- matches the -- inspection criteria 
  * requirements
    * 1 top-level statement
  * can contain
    * nested statements / ANY depth
    * logical statements `AND`, `OR`, and `NOT`
      * allows
        * combining statements | rule
  * != AWS resources
    * -> NOT have ARNs
  * ways to manage them
    * by name |
      * rule group or
      * web ACL
    * -- via --
      * JSON format of the
        * rule group or
        * web ACL / contains the rule
      * AWS WAF console **Rule Builder**

**Topics**
+ [AWS WAF rule name](waf-rule-name.md)
+ [AWS WAF rule action](waf-rule-action.md)
+ [AWS WAF rule statements](waf-rule-statements.md)