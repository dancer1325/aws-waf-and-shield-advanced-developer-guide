# Best practices for intelligent threat mitigation<a name="waf-managed-protections-best-practices"></a>

* purposes of these best practices
  * most efficient,
  * cost-effective
* best practices
  + **Implement the JavaScript & mobile application integration SDKs**
    + enable the full set of ATP or Bot Control functionality
    + application integration SDKs
      + -- provide the -- tokens /
        + ALWAYS available
        + -- used by the -- managed rule groups, to separate | session level
          + legitimate client traffic vs unwanted traffic
    + see
      + [Why you should use the application integration SDKs with Bot Control](waf-bot-with-tokens.md)
      + [Why you should use the application integration SDKs with ATP](waf-atp-with-tokens.md)
      + [AWS WAF client application integration](waf-application-integration.md)
  + **Limit the requests / you -- send to the -- ATP & Bot Control rule groups**
    + if you use intelligent threat mitigation AWS Managed Rules rule groups -> additional fees
    + Bot Control rule group -- inspects -- EVERY request / reaches it | web ACL evaluation
    + 👀ATP rule group -- inspects -- ONLY login requests 👀
      + if you plan to reject login requests (_Example:_ -- based on -- geographic origin) -> run those rules | before the ATP rule group
    + approaches 
      + exclude requests -- from -- inspection /
        + scope-down statement | managed rule group statement
          + see [Scope\-down statements](waf-rule-scope-down-statements.md)
        + -- via -- adding rules | before the rule group
          + use cases
            + rules / you can NOT use | scope-down statement
            + complex situations (_Example:_ labeling / -- followed by -- label matching)
          + see 
            + [Scope\-down statements](waf-rule-scope-down-statements.md)
            + [AWS WAF rule statements](waf-rule-statements.md)
      + run the rule groups | AFTER less expensive rules
        + see [AWS WAF rule statements](waf-rule-statements.md)
      + running order: Bot Control rule group, ATP rule groups 
        + Reason: 🧠 less expensive rule group first 🧠
  + **For distributed denial of service \(DDoS\) protection -> use Shield Advanced automatic application layer DDoS mitigation**
    + enable
      + Shield Advanced / automatic application layer DDoS mitigation
    + if Shield Advanced detected DDoS attacks -> automatically 
      + creating,
      + evaluating,
      + deploying custom AWS WAF mitigations / on your behalf 
    + see 
      + [AWS Shield Advanced overview](ddos-advanced-summary.md)
      + [AWS Shield Advanced application layer \(layer 7\) protections](ddos-app-layer-protections.md)
  + **Tune and configure token handling**
    + -> best user experience 
    + if you want to reduce operating costs & improve your end user's experience -> tune your token management immunity times -- to the -- longest / your security requirements permit
      + This keeps the use of CAPTCHA puzzles and silent challenges to a minimum\.
    + if you want to enable token sharing between protected applications -> configure a token domain list -- for -- your web ACL
    + see 
      + [Token domains and domain lists](waf-tokens-domains.md)
      + [Timestamp expiration: token immunity times](waf-tokens-immunity-times.md)
  + **Reject requests with arbitrary host specifications**
    + == configure your protected resources / require that web requests's headers `Host`
      + = targeted resource
      + accept ONLY specific set of values
        + _Example:_ `myExampleHost.com` & `www.myExampleHost.com` 
  + **For Application Load Balancers / are origins for CloudFront distributions -> configure CloudFront & AWS WAF for proper token handling**
    + requirements
      + associate your web ACL -- to an -- Application Load Balancer
      + deploy the Application Load Balancer -- as the -- origin for a CloudFront distribution
    + see [Configuration required for Application Load Balancers that are CloudFront origins](waf-tokens-with-alb-and-cf.md)
  + **Test and tune before deploying**
    + Reason: 🧠 important for paid features 🧠
    + see 
      + [Testing and tuning your AWS WAF protections](web-acl-testing.md)
      + [Testing and deploying AWS WAF Bot Control](waf-bot-control-deploying.md)
      + [Testing and deploying ATP](waf-atp-deploying.md)