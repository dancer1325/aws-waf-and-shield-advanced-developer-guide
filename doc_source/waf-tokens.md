# AWS WAF web request tokens<a name="waf-tokens"></a>

* AWS WAF tokens
  * ⭐️integral part of the enhanced protections / -- offered by -- AWS WAF intelligent threat mitigation ⭐️
  * named ALSO fingerprint
  * == collection of information about a single client session /
    * client 
      * stores
      * provides / EVERY web request
    * uses
      * identify
      * separate malicious client sessions vs legitimate sessions
      * enable features of the
        * AWS WAF Bot Control &
        * ATP managed rule groups
  * about costs
    * negligible for legitimate users
    * expensive | scale for botnets
  * management
    * AWS WAF, for clients / -- successfully respond to -- silent challenges & CAPTCHA puzzles 
      * creates tokens,
      * updates tokens,
      * encrypts tokens
  * how does it work?
    * client -- sends a -- web request / encrypted token passed
    * AWS WAF
      * decrypts the token
      * verifies its contents 

**Topics**
+ [How tokens are used](waf-tokens-usage.md)
+ [Token characteristics](waf-tokens-details.md)
+ [Timestamp expiration: token immunity times](waf-tokens-immunity-times.md)
+ [Token domains and domain lists](waf-tokens-domains.md)
+ [Token labeling by the Bot Control and ATP managed rule groups](waf-tokens-labeling.md)
+ [Blocking requests that don't have a valid token](waf-tokens-block-missing-tokens.md)
+ [Configuration required for Application Load Balancers that are CloudFront origins](waf-tokens-with-alb-and-cf.md)