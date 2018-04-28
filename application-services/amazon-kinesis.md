---
description: 'https://aws.amazon.com/kinesis'
---

# Amazon Kinesis

* Streaming data is something which is generated by thousands of data sources – stock prices, game information, social network data, geospatial data, purchases from online stores, IoT sensor data.
* Process large streams of data. To process data - Amazon Redshift and Elastic Map Reduce \(allows root access\)
* Kinesis is an AWS platform to analyze streaming data

### Kinesis Streams

* Stores data for **24 hours \(default\) to 7 days**
* Data stored in shards
* Data consumers \(EC2 instances\) analyze the stream and then derive results/take next actions
* Data capacity of stream is a function of the number of shards you specify for the stream.

### Kinesis Firehose

* Don’t have to worry about shards, streams – **completely automated**
* It can capture, transform, and load streaming data into **Amazon S3, Amazon Redshift, Amazon Elasticsearch Service, and Splunk**
* No automatic data retention window. Data is either immediately analyzed or sent.
* Data is immediately analyzed via Lambda

### Kinesis Analytics

* Run SQL type queries on top of data contained in Streams or Firehose and store the results in S3/Redshift and Elasticsearch cluster
