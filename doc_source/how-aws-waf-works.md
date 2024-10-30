# How AWS WAF works<a name="how-aws-waf-works"></a>

* goal of AWS WAF
  * control how your protected resources -- respond to -- HTTP\(S\) web requests
* steps to get it
  * define a web access control list \(ACL\)
    * create rules / define
      * traffic patterns / look for | requests
      * actions / take | matching requests
        * possible actions
          * Allow the requests -- to go to the -- protected resource
            * == processing and response
          * Block the requests
          * Count the requests
          * Run CAPTCHA or challenge checks -- against -- requests
            * Reason: 🧠 verify human users & standard browser use 🧠
  * associate ACLs -- with -- >=1 web application resources / you want to protect
    * associated resources -- will forward, by inspecting the web ACL, incoming requests to -- AWS WAF

**Topics**
+ [AWS WAF components](how-aws-waf-works-components.md)
+ [AWS WAF web ACL capacity units \(WCUs\)](aws-waf-capacity-units.md)
+ [Resources that you can protect with AWS WAF](how-aws-waf-works-resources.md)