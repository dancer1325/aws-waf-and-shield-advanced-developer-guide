# Options for intelligent threat mitigation<a name="waf-managed-protections-comparison-table"></a>

+ **AWS WAF Fraud Control account takeover prevention \(ATP\)**
  + allows, about your application's login page
    + detects
    + manages malicious takeover attempts 
  + core functionality -- is provided by the -- ATP managed rule group /
    + use tokens
  + see 
    + [AWS WAF Fraud Control account takeover prevention \(ATP\)](waf-atp.md)
    + [AWS WAF Fraud Control account takeover prevention \(ATP\) rule group](aws-managed-rule-groups-atp.md)
+ **AWS WAF Bot Control**
  + allows, about friendly and malicious bots
    + identifies,
    + labels,
    + manages
  + affected bots
    + common bots / signatures are unique | ACROSS applications
    + targeted bots / have signatures -- specific to an -- application 
  + core functionality -- is provided by the -- Bot Control managed rule group /
    + use tokens
  + see 
    + [AWS WAF Bot Control](waf-bot-control.md)
    + [AWS WAF Bot Control rule group](aws-managed-rule-groups-bot.md)
+ **Client application integration SDKs**
  + allows, about clients 
    + validating client sessions
    + acquire AWS WAF tokens 
  + if you use ATP or Bot Control -> implement the application integration SDKs | your client application
    + Reason: 🧠 take full advantage of ALL rule group features 🧠 
  + recommendations
    + rule groups / WITHOUT an SDK integration ONLY as a temporary measure
  + see [AWS WAF client application integration](waf-application-integration.md) 
+ **Challenge and CAPTCHA rule actions**
  + allows
    + validating client sessions & end users
    + acquire AWS WAF tokens -- for -- clients
  + it can be implemented | ANYWHERE / you specify a rule action 
    + _Example:_
      + | your
        + rules
        + rule groups
  + requirements
    + AWS WAF JavaScript interstitials
  + see [CAPTCHA and Challenge actions in AWS WAF](waf-captcha-and-challenge.md)

* features / tokens enable | rule groups
  * [Why you should use the application integration SDKs with ATP](waf-atp-with-tokens.md)
  * [Why you should use the application integration SDKs with Bot Control](waf-bot-with-tokens.md) 

* range of options -- for -- implementing intelligent threat mitigation
  * [basic use of rule actions / run challenges & enforce token acquisition, advanced features / -- offered by the -- Bot Control and ATP AWS Managed Rules rule groups]

**Topics**
+ [Challenges and token acquisition](waf-managed-protections-comparison-table-token.md)
+ [Bot Control and ATP managed rule groups](waf-managed-protections-comparison-table-rg.md)
+ [Rate limiting options in rate\-based rules and targeted Bot Control rules](waf-managed-protections-comparison-table-rbr-bot.md)