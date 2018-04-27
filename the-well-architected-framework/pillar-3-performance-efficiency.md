# Pillar 3 - Performance Efficiency

Focuses on how to use computing requirements efficiently to meet business needs. How to manage efficiency as demand changes and technology evolves. Constantly question current architecture vis-a-vi current available services.

### **Design Principles**

* Democratize advanced technologies. Team can consume advanced technologies as services instead of building expertise. E.g. DynamoDB, Machine Learning, etc
* Go global in minutes
* Use serverless architecture

### Best Practices

**Compute**

* Choose the right kind of server – CPU intensive, memory intensive or serverless
* **Questions**
  * How do you select appropriate instance type?
  * How do you continue to use appropriate services / architectures with new instances types?
  * How do you monitor instances?
  * How to ensure quantity of instances matches demands?

**Storage**

* Which storage solution to use depends on number of factors. E.g.:
  * Access Method – Block, file or Object
  * Patterns of Access – Sequential or Random
  * Throughput Required
  * Frequency of Access – Online, offline or archival
  * Frequency of Update – Worm, Dynamic
  * Availability constraints
  * Durability constraints
* **Questions**
  * How do you use select appropriate storage solution?
  * How do you ensure that you have the most appropriate storage solutions with new instance types?
  * How do you monitor your storage solution to ensure performance?

**Database**

* Do you need consistency, HA, DR needs, No-SQL
* **Questions**
  * How do you selected appropriate solution for system?
  * How do you ensure that you have the most appropriate database solutions with new solutions launched?
  * How do you monitor your database solution to ensure performance?
  * How do you ensure capacity matches demand?

**Space-time trade off**

* Use RDS to add read replicas
* Use Direct Connect to provide predictable latency
* Use global infrastructure to have multiple copies of your environment, closest to your users
* Use caching services like ElastiCache or CloudFront to reduce latency
* **Questions**
  * How do you selected appropriate proximity and caching solution for system?
  * How do you ensure that you have the most appropriate proximity and caching solutions with new solutions launched?
  * How do you monitor your proximity and caching solution to ensure performance?
  * How do you ensure proximity and caching capacity matches demand?

### **Key AWS Resources**

* Compute – Auto scaling
* Storage – EBS, S3, Glacier
* Database – RDS, DynamoDB, Redshift
* Space-time trade off – CloudFront, ElastiCache, Direct Connect, RDS Read Replicas, etc. – anything that will lower latency or time to access service

