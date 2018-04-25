# S3 Security

* By default all newly created buckets are **private**
* Control Access to buckets using
  * Bucket Policies – bucket wide
  * Access Control Lists – up to individual objects
    * You grant permission to an AWS account using the email address or the canonical user ID
  * S3 buckets can log all access requests to another S3 bucket even another AWS account.
* You can use pre-signed URLs to give your users access to Amazon S3 objects. A pre-signed URL provides access to an object without requiring AWS security credentials or permissions

