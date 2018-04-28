---
description: 'FAQ: https://aws.amazon.com/redshift/faqs/'
---

# Redshift

Petabyte scale DW solution in cloud. Used for OLAP – sum of various columns and joining the data.

### **Configurations**

* **Single Node** – 160 GB. Used by Small and Medium Size businesses.
* **Multi-Node** – Leader Node \(handles all incoming connections & receives queries\) & compute Node \(store data and perform queries and computations – up to 128 Compute Nodes\)

### **Performance**

* Redshift is 10 times faster than usual OLAP systems.
* **Columnar Data Store - **Columnar data is stored sequentially on storage system. Hence low I/O required – improving performance. Block size of columnar storage: **1024KB / 1MB**
* **Advanced Compression** \(easier to do it via Columns instead of via Rows – which have different data types\). Columns have similar type of data. Doesn’t use indexes and views – hence less storage required
* **Massively Parallel Processing \(MPP\)- ** Amazon Redshift automatically distributes data and query load across all nodes.
* **Redshift Spectrum** - enables you to run queries against exabytes of unstructured data in Amazon S3. There is no loading or ETL required. 

### **Pricing**

* Based on Compute Node hours \(compute node only – no leader node\)
* Backup and Data Transfer \(only within VPC\)

### **Security**

* Transit encrypted via SSL
* At rest using AES-256 encryption
* Can use your own HSM or default AWS Key management

### **Availability**

* Amazon Redshift replicates all your data within your data warehouse cluster when it is loaded and also continuously backs up your data to S3. Amazon Redshift always attempts to maintain at least **three copies of your data** \(the original and replica on the compute nodes and a backup in Amazon S3\). Redshift can also asynchronously replicate your snapshots to S3 in another region for disaster recovery.
* You can add or remove nodes from your Amazon Redshift data warehouse cluster

### **Exam Tips**

* Database warehousing service, cheap, faster. 
* Best seller AWS Service. 
* Speed achieved due to columnar storage. And Data stored sequentially on disk – hence faster.

