# CloudFront Security

* You can force them to use CDN URL instead of S3 DNS
* To restrict bucket access you need to create **Origin Access Identity \(OAI\)**. And allow this user read permission S3 bucket content
* Set viewer protocol policy – redirect http to https, http or https
* Allows various HTTP methods – GET, PUT, POST, PATCH, DELETE, and HEAD
* Restrict viewer access for S3 and CDN using pre-Signed URLs or Signed cookies. E.g. You can view video only using that URL
* Using Web Application Firewalls to prevent SQL injection, CSS attacks
* For https access, you can either use default CloudFront certificate or own certificate can be imported via ACM
* Geo-restriction can be setup. Either whitelist or blacklist – countries from where content can be accessed
* Invalidating removes objects from CloudFront. It can be forced to remove from Cache – obviously costs
* You can force users to get content via CloudFront after removing read access to S3 bucket
* You can also upload content to CloudFront

