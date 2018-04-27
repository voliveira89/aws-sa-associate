# CloudFront

### Important terms

* **CDN \(Content Delivery Network\)** – collection of distributed servers where the content is served to users based on the user’s location and the location of content origin
* **Edge location** – location where content will be cached. Different from AWS Region / AZ
* **Origin** – Can be S3 Bucket, an EC2 Instance, an Elastic Load Balancer or Route53
* **Distribution** – is the name given to CDN collection which consists of Edge locations
* **Web Distribution** – Typically used for websites & web content only
* **RTMP** – Used for Media Streaming. Adobe Flash media server’s protocol – video streaming

### Tips

* First request is slow as it comes from source origin. Subsequent requests improve speed as they are cached in nearest edge location and routed there until TTL expires
* CloudFront also works with non AWS origin which can be on premise as well
* Edge locations are for read and write as well. Objects PUT on edge location are sent to origin
* Objects are cached for life of TTL. TTL can be set for 0 seconds to 365 days. Default TTL is 24 hours. If objects change more frequently update the TTL
* You can clear cached objects, with charges
* Origin domain name – either S3 bucket, ELB or on premise domain
* Provisioning / Updating CloudFront distribution takes up to 15-20 minutes

