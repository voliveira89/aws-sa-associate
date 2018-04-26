# ElastiCache

* Easy to deploy, operate and scale an in-memory cache in the cloud.
* Improve performance by avoiding repeated calls to DB.
* Improve latency and throughput for read-heavy applications.
* Can be used for compute intensive data

FAQ: [https://aws.amazon.com/elasticache/faqs/](https://aws.amazon.com/elasticache/faqs/)

### **Memcached**

* All Memcached tooling can be easily ported over

### **Redis**

* Supports Master / Slave replication and multi-AZ deployment to get redundancy
* ElastiCache is used if DB is primarily read-heavy and not frequently changing
* Use Redshift – if application is slow due to constant OLAP transactions on top of OLTP focused DB

