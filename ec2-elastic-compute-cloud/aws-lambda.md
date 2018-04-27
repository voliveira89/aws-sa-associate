---
description: 'FAQ: https://aws.amazon.com/lambda/faqs/'
---

# AWS Lambda

AWS Lambda is a compute service where you can upload your code and create a Lambda function. AWS Lambda takes care of provisioning and managing the servers that you use to run the code. You don't have to worry about operating systems, patching, scaling, etc. You can use Lambda in the following ways:

* As an event-driven compute service where AWS Lambda runs your code in response to events. These events could be changes to data in an Amazon S3 bucket or an Amazon DynamoDB table.
* As a compute service to run your code in response to HTTP requests using Amazon API Gateway or API calls made using AWS SDKs.

Lambda function can trigger another Lambda function and it can also use other AWS services. Lambda **can scale out automatically**. If multiple users send to HTTP requests concurrently, there will be multiple Lambda functions are invoked \(scaled out automatically\) and give responses to users, but the code of the Lambda functions are identical, so one set of code but it will respond to multiple requests. This is very different with EC2 instances behind the ELB. The specific number of EC2 instances will always take charge of responding to the requests, no matter how many requests are there, and the code are copied across the EC2 instances. For the automatic scaling out of Lambda function, there is a good news that you get a million free invocations per month.

* Create a new Lambda function:
  * Configure Triggers, such as SNS, S3, Kinesis, DynamoDB, Alexa, AWS IOT, CloudFront, CloudWatch, CodeCommit, API Gateway, etc.
  * Configure Function. Lambda support languages/runtime including: Node.js, Java, Python and C\#.
  * Review.
* Pricing based on:
  * Number of requests
    * First 1 million requests are free, and $0.2 per 1 million requests thereafter.
  * Duration
    * Duration is calculated from the time your code begins executing until it returns or otherwise terminates, rounded up to the nearest 100ms. The price depends on the amount of memory you allocate to your function. You are charged $ 0.00001667 for every GB-second used. **Duration has a threshold, it is 5 minutes**. The function cannot get executed over 5 minutes, so you have to break your function into multiple functions, and let one function trigger next one.

**Why Lambda is cool?**

* No servers. No database admin, no network admin, no system admin. You only need to focus on your code.
* Continuous scaling. Unlike auto scaling of EC2 instances or something others, you don't need to set any Rule, you don't need to wait a couple of minutes, and Lambda will auto scaling instantly.
* Super cheap.
* Alexa is using Lambda. When you talk to it, you trigger a lambda function, and this lambda function will respond to you.

Notes:

* Lambda scale out, not up, automatically.
* Lambda functions are independent, 1 event = 1 function.
* Lambda is serverless.
* Know what services are serverless, such as S3, API Gateway, Lambda, DynamoDB, etc. EC2 is not, it will need to maintain instances.
* Lambda functions can trigger other lambda functions, 1 event can = x functions if functions trigger other functions.
* Architectures can get extremely complicated. **AWS X-ray** allows you to debug what is happening.
* Lambda can do things globally, you can use it to back up S3 buckets to other S3 buckets, etc.
* Know your triggers. \(i.e. SNS, S3, Kinesis, DynamoDB, Alexa, AWS IOT, CloudFront, CloudWatch, CodeCommit, API Gateway, etc\).
* The **available languages/runtime** for Lambda: Node.js \(JavaScript\), Python, Java \(Java 8 compatible\), and C\# \(.NET Core\) and Go.
* Lambda automatically monitors functions on your behalf, reporting metrics through CloudWatch. These metrics are including:
  * total requests
  * latency
  * error rates

