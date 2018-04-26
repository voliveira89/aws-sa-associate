# EBS Volume Types

**SSD Drives**

* **General Purpose SSD** – gp2 – up to 10,000 IOPS. 3 IOPS per GB. Balances price and performance. You can burst **upto 3000 IOPS for 1GB**. Volume size: **1GiB to 16TiB**
* **Provisioned SSD** – io1– when you need more than 10,000 IOPS. Large RDBMS DBs and NoSQL DBs. **Up to 32000 \(20000 on the course\) IOPS**. Volume size: **4GiB to 16TiB**

**Magnetic Drives**

* **HDD, Throughput Optimized **– st1 – Required for data written in sequence. Big Data, DWH, Log processing. Cannot be used as boot volume. Volume size: **500MiB to 16TiB**
* **HDD, Cold** – sc1 – Data that isn’t frequently accessed. E.g. File Server. Cannot be used as boot volume. Volume size: **500MiB to 16TiB**
* **HDD, Magnetic \(Standard\)** – Cheapest bootable EBS volume type. Used for apps where data is less frequently accessed and low cost is important. Volume size: **1GiB to 1TiB**

