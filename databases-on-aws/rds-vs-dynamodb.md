# RDS vs DynamoDB

* Use DynamoDB for Push button scaling. With RDS – to scale horizontally a new instance has to be created
* DynamoDB is cheap for writes and expensive for reads
* Observe workload characteristics and decide
* Use RDS if data requires joins and relationships
* In RDBMS database structure cannot be dynamically altered. With DynamoDB you can.
* If you want push button scaling, without any downtime, you will always want to use DynamoDB. With RDS scaling is not so easy, you have to use a bigger instance or add read replicas \(manual process\)



