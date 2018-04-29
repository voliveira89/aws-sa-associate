# S3 Buckets

* S3 bucket namespace is global. Region independent
* Data is automatically distributed across a minimum of three physical facilities that are geographically separated within an AWS Region, and Amazon S3 can also automatically replicate data to any other AWS Region.
* Amazon S3 buckets in **all** regions provide **read-after-write consistency** for PUTS of new objects and **eventual consistency** for overwrite PUTS and DELETES
* A bucket name in any region should only contain lower case characters. It has to be DNS Compliant
* To route traffic using Amazon Route53 to a website that is hosted in an Amazon S3 Bucket the bucket must have the same name as your domain or subdomain
* Object versioning - Different versions of the same object in a bucket
* Only Static website can be hosted. Auto scaling, Load Balancing etc. all managed automatically
* You can tag buckets \(or any AWS resource\) to track costs. Tags consist of keys and \(optional\) value pairs
* Lifecycle management of objects can be set. E.g. move to Glacier after 30 days
* Every bucket created, object uploaded is **private by default**
* Object Permissions – Access to Object ACLs
  * The "Owner" refers to the identity and email address used to create the account AWS account.​
* Prefix in bucket is a folder in the bucket
* Max 100 S3 buckets per account by default
* In a virtual-hosted–style URL, the bucket name is part of the domain name in the URL. For example:  
  * http://bucket.s3.amazonaws.com
  * http://bucket.s3-aws-region.amazonaws.com
* If workload in an Amazon S3 bucket routinely **exceeds 100 PUT/LIST/DELETE **requests per second or **more than 300 GET** requests per second
  * Add a Hex Hash Prefix to Key Name
  * Reverse the Key Name String
  * Use Amazon CloudFront
* Individual Amazon S3 objects can range in size from a minimum of **0 bytes** to a maximum of **5 terabytes**. The largest object that can be uploaded in a single PUT is 5 gigabytes. For objects larger than **100 megabytes**, customers should consider using the Multipart Upload capability
* Multipart Upload specifications:

| **Item** | **Specification** |
| --- | --- | --- | --- | --- | --- | --- |
| Maximum object size | 5 TB |
| Maximum number of parts per upload | 10,000 |
| Part numbers | 1 to 10,000 \(inclusive\) |
| Part size | 5 MB to 5 GB, last part can be &lt; 5 MB |
| Maximum number of parts returned for a list parts request | 1000 |
| Maximum number of multipart uploads returned in a list multipart uploads request | 1000 |

