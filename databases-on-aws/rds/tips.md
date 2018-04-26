# Tips

* Why you can’t connect to DB Server from DMZ. Check the security group – if it is removed or added
* Have separate groups for EC2 Instance and RDS Instance
* What data transfer charge is incurred when replicating data from your primary RDS instance to your secondary RDS instance? - There is no charge associated with this action
* When you have deployed an RDS database into multiple availability zones, can you use the secondary database as an independent read node? – **No**
* In VPC Security Group, the answer would be YES because you will have manually specify access to port & protocol
* RDS automatically creates RDS Security Group w/ TCP port **3306** enabled
* Amazon RDS does not currently support increasing storage on a SQL Server Db instance
* The easiest way to find out if an error occurred is to look for an Error node in the response from the Amazon RDS API
* When creating an RDS instance you can select which availability zone in which to deploy your instance
* By default, customers are allowed to have up to a total of **40 Amazon RDS DB instances**. Of those 40, up to 10 can be Oracle or SQL Server DB instances under the "License Included" model. All 40 can be used for Amazon Aurora, MySQL, MariaDB, PostgreSQL and Oracle under the "BYOL" model. Note that RDS for **SQL Server has a limit of 30 databases** on a single DB instance. Oracle: 1** database per instance; no limit on number of schemas.**

