# DynamoDB

* Fast and flexible NoSQL database
* Consistent, single digit millisecond latency
* Fully managed DB – supports both document based & Key-value data models
* Great fit for mobile, IoT, web, gaming etc. applications
* Stored on SSDs
* Stored on **3 geographically distinct Data Centers \(or AZs\)**. Built in redundancy
* Consistency \(select type based on application needs\)
  * **Eventual consistent reads** - Consistency reached up to 1 second \(default\)
  * **Strongly Consistent reads** - Consistency reached after writes to all copies are completed. &lt;1 second
* Pricing – Write Capacity Units and Read Capacity Units \($/hr.\). Also Storage cost per month. You provision capacity in units/second. It can scale on the fly. Provisioned capacity
* **Expensive for Writes. Cheap for Reads.** Important point v/s RDS
* You can dynamically add columns – without the need to update other rows with the column data. As this is no RDBMS
* Reserved capacity is available for DynamoDB as well
* The maximum item size in DynamoDB is **400 KB**, which includes both attribute name binary length \(UTF-8 length\) and attribute value lengths \(again binary length\)
* Amazon DynamoDB Accelerator \(DAX\) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second

FAQ: [https://aws.amazon.com/dynamodb/faqs/](https://aws.amazon.com/dynamodb/faqs/)

