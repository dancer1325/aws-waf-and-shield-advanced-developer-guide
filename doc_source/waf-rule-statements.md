# AWS WAF rule statements<a name="waf-rule-statements"></a>

* AWS WAF Rule statements
  * == part of a rule / tells AWS WAF -- how to -- inspect a web request
    * web request matches the statement == AWS WAF -- finds the -- inspection criteria | web request 
  * 1! top-level rule statement / rule
  * nesting rule statements
    * == contain other statements / 👀certain restrictions 👀
      * _Example:_ NOT allowed nesting a rule group statement | another statement
    * visual editor ONLY supports 1 level of nesting
  * _Examples:_
    * _Example1:_ statement / provides a set of originating countries -- to check -- your web requests
    * _Example2:_ statement / just -- references a -- rule group

**Topics**
+ [Rule statements list](waf-rule-statements-list.md)
+ [Web request components](waf-rule-statement-fields.md)
+ [Statements that reference a set or a rule group](waf-rule-statement-reusable-entities.md)
+ [Scope\-down statements](waf-rule-scope-down-statements.md)
+ [Forwarded IP address](waf-rule-statement-forwarded-ip-address.md)