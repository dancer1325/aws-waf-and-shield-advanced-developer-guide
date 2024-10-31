# AWS WAF rule action<a name="waf-rule-action"></a>

* AWS WAF rule action
  * 👀tells AWS WAF -- what to do with a -- web request, if it -- matches the -- criteria defined | rule 👀
    * possible to add, custom behavior / EACH rule action 
  * categories
    * terminating
      * stops the web ACL evaluation of the request
      * lets
        * continue to your protected application or
        * blocks it 
    * non-terminating 
  * options 
    + **Allow**
      + == AWS WAF allows the request -- to be forwarded to the -- protected AWS resource
      + terminating action
      + customizable
        + request's headers | -- before forwarding it to the -- protected resource
    + **Block**
      + == AWS WAF -- blocks the -- request
        + response
          + by default, HTTP `403 (Forbidden)`
          + can be customized
          + -- based on -- Block action settings 
      + terminating action 
    + **Count**
      + == AWS WAF counts the request
        + NOT decide whether to allow it or block it
      + NON-terminating action
        + == AWS WAF continues processing the remaining rules | web ACL 
      + customizable
        + request's headers
        + add labels
    + **CAPTCHA and Challenge**
      + == AWS WAF uses CAPTCHA puzzles & silent challenges
        + goal
          + distinguish normal browsers vs sessions / run by bots
        + tokens
          + uses
            + by AWS WAF, -- to track -- recent successful client responses
            + decide if
              + 👀**if valid & unexpired token -> Non-terminating** 👀
                + AWS WAF handling == Count action
                  + ALSO, same possible customizations
              + 👀 **if invalid OR expired token -> terminating & blocked request** 👀
                + AWS WAF handling == Block action
      + pricing
        + additional fees
        + see [AWS WAF Pricing](http://aws.amazon.com/waf/pricing/)
      + see [CAPTCHA and Challenge actions in AWS WAF](waf-captcha-and-challenge.md)

* see [Customize web requests & responses | AWS WAF](waf-custom-request-response.md)
* see [add labels -- to match -- web requests](waf-labels.md)
* see [Web ACL rule and rule group evaluation](web-acl-processing.md) 