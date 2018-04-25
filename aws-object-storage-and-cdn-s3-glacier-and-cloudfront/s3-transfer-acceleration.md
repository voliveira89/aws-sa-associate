# S3 Transfer Acceleration

It utilizes the CloudFront Edge Network to accelerate uploads to S3. Instead of uploading directly to S3, you can use a distinct URL to upload directly to an edge location which will then transfer to S3 using Amazon’s backbone network.

The farther you are from S3 bucket region the higher is the improvement you can observe using S3 Transfer Acceleration. High cost for usage than standard S3 transfer rates.  


