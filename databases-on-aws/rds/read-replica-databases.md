# Read Replica Databases

**Read replica** – **async** data transfer to another RDS instance. You can actually read from these instances, unlike Multi-AZ deployments. You can also have read replicas of read replicas up to 5 copies. Note: watch out as async causes latency.

* Read replicas can be used for dev/test environments, run certain workloads only against them and not against direct production deployment – intensive workloads
* MySQL, MariaDB, PostgreSQL only for read replicas, **no Oracle & SQL Server**
* You **cannot have read replicas that have multi AZ**. However, **you can create read replicas of multi AZ source** databases
* Read replicas can be of a different size than source DB
* Each read replica will have **its own DNS endpoint**
* Automatic backups must be turned on in order to deploy a read replica
* Read replicas **can be promoted to be their own databases**. This breaks replication. E.g. dev/test can be connected to the replica by first promoting it as DB itself
* Read replicas **can be done in a second region** for MySQL, MariaDB, PostgreSQL and Aurora
* Application re-architecture is required to make use of read replicas
* Read replicas are not used for disaster recovery, they are used for performance scaling only
* The new DB Instance that is created when you promote a Read Replica retains the backup window period

