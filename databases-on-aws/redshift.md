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
* It uses **Columnar Data Store**. Columnar data is stored sequentially on storage system. Hence low I/O required – improving performance
* Advanced Compression \(easier to do it via Columns instead of via Rows – which have different data types\). Columns have similar type of data. Doesn’t use indexes and views – hence less storage required
* Based on data, appropriate data compression scheme is used
* Allows for massive parallel processing
* Block size of columnar storage: **1024KB / 1MB**

### **Pricing**

* Based on Compute Node hours \(compute node only – no leader node\)
* Backup and Data Transfer \(only within VPC\)

### **Security**

* Transit encrypted via SSL
* At rest using AES-256 encryption
* Can use your own HSM or default AWS Key management

### **Availability**

Not Multi-AZs. Can restore snapshots.

### **Exam Tips**

* Database warehousing service, cheap, faster. 
* Best seller AWS Service. 
* Speed achieved due to columnar storage. And Data stored sequentially on disk – hence faster.

