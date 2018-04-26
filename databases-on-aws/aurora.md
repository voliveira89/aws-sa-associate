# Aurora

* Bespoke Database Engine
* It is MySQL compatible
* However you can’t download and install on your workstation
* No Free Tier usage available 
* Also available only in select regions
* Takes slightly longer to provision

FAQ: [https://aws.amazon.com/rds/aurora/faqs/](https://aws.amazon.com/rds/aurora/faqs/)

### **Performance**

5 times better performance than MySQL. At a fraction of cost as compared to Oracle.

### **Scaling**

* Outset 10 Gb Storage, auto increment of storage
* No push button scaling – unlike DynamoDB

### **Fault Tolerance**

* Maintains 2 copies of your data in at least 3 availability zones \(6 copies in total\). This is for the Data only not for the instances that runs the Database
* 2 copies lost – no impact on write availability
* 3 copies lost – no impact on read availability
* Storage is self-healing

### **Replicas**

* MySQL read replica can be created from the Aurora source DB \(up to 5 of them\)
* Aurora Replicas – up to 15 of them. If leader crashes, the replica with the highest tiers becomes the leader. While creating replicas, remember to assign different tier levels.
* Cluster Endpoint vs Individual Endpoint



