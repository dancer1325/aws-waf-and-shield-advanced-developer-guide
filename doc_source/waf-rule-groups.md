# Rule groups<a name="waf-rule-groups"></a>

* rule group
  * == reusable set of rules / you can add | web ACL
  * see [web ACLs](web-acl.md)
  * main categories 
    + Managed rule groups
      + == created & maintained by 
        + AWS Managed Rules
        + AWS Marketplace sellers
    + Your own rule groups
      + == created & maintained by you
    + Rule groups
      + == owned & managed by other services (_Example:_ AWS Firewall Manager & Shield Advanced)
  * **vs web ACLs**  
    + BOTH contain rules / defined similarly
    + Rule groups can NOT contain rule group reference statements 
    + reusability
      + rule group can be reused | MULTIPLE web ACLs
        + -- via -- adding a rule group reference statement / EACH web ACL
      + web ACL can NOT be reused
    + default actions
      + rule groups do NOT have
      + default action / EACH rule OR rule group / included | web ACL 
    + relation with an AWS resource
      + rule group -- NOT associated directly with an -- AWS resource
        + if you want to protect resources / -- via a -- rule group -> use the rule group | web ACL 
    + capacity units
      + web ACLs -- have a -- system-defined maximum capacity of 5,000 WCUs 
      + rule group has a WCU setting / must be set | creation 
      + see [AWS WAF web ACL capacity units \(WCUs\)](aws-waf-capacity-units.md)
  * see [Rules](waf-rules.md) 

**Topics**
+ [Managed rule groups](waf-managed-rule-groups.md)
+ [Managing your own rule groups](waf-user-created-rule-groups.md)
+ [Rule groups provided by other services](waf-service-owned-rule-groups.md)