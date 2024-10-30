# AWS Firewall Manager<a name="fms-chapter"></a>

* AWS Firewall Manager
  * allows
    * simplifies your administration of protections / ACROSS MULTIPLE accounts & resources
      * AWS WAF,
      * AWS Shield Advanced,
      * Amazon VPC security groups,
      * AWS Network Firewall,
      * Amazon Route 53 Resolver DNS Firewall
    * 👀== set up your protections 1! -> automatically applies them ACROSS your accounts & resources 👀
      * _Example of simplifications:_ 
        * protect ALL resources of a particular type (_Example:_ Amazon CloudFront distributions)
        * protect ALL resources -- with -- specific tags
        * adds protection to resources / are added | your account
        * subscribe ALL member accounts | AWS Organizations organization -- to -- AWS Shield Advanced
        * apply security group rules |
          * ALL member accounts or
          * specific AWS Organizations organization's subsets of accounts
        * use
          * your OWN rules, or
          * purchase managed rules -- from -- AWS Marketplace
    * centralized monitoring of DDoS attacks / ACROSS your organization
  * use cases
    * protect your WHOLE organization
      * != small number of specific accounts and resources
    * if you frequently add new resources that you want to protect

**Topics**
+ [AWS Firewall Manager pricing](aws-fms-pricing.md)
+ [AWS Firewall Manager prerequisites](fms-prereq.md)
+ [Managing the AWS Firewall Manager administrator](fms-administrator.md)
+ [Getting started with AWS Firewall Manager policies](getting-started-fms-intro.md)
+ [Working with AWS Firewall Manager policies](working-with-policies.md)
+ [Working with resource sets in Firewall Manager](fms-resource-sets.md)
+ [Viewing compliance information for an AWS Firewall Manager policy](fms-compliance.md)
+ [AWS Firewall Manager findings](fms-findings.md)
+ [Security in AWS Firewall Manager](fms-security.md)
+ [AWS Firewall Manager quotas](fms-limits.md)