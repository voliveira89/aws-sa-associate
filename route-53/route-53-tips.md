# Route 53 Tips

* Remember difference between Alias and CNAME
  * Given a choice between Alias Record vs CNAME – always choose Alias. Alias records **are free and can connect to AWS resources**
* R53 supports zone apex records
* With Route 53, there is a default limit of 50 domain names. However, this limit can be increased by contacting AWS support
* Naked domain – which doesn’t have the www in front of the domain e.g. acloud.guru. [www.acloud.guru](http://www.acloud.guru/) isn’t
* Route53 has a security feature that prevents internal DNS from being read by external sources. The work around is to create a EC2 hosted DNS instance that does zone transfers from the internal DNS, and allows itself to be queried by external serversTips
* **Routing Traffic to a Website that Is Hosted in an Amazon S3 Bucket**
  * An S3 bucket that is configured to host a static website.
  * The bucket must have the same name as your domain or subdomain.
  * A registered domain name.
  * Route 53 as the DNS service for the domain.

