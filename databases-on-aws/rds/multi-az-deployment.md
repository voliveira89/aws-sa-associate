# Multi-AZ Deployment

* A standby copy is created in another AZ. AWS handles replication and auto-failover
* AWS can automatically failover RDS instance to another instance
* In case of failover, no need to change connection string
* This can be used for Disaster Recovery purpose only. This option has to be selected at instance creation time. This option is not useful for improving performance/scaling. For performance improvement use, multiple read-replicas
* When failing over, Amazon RDS simply flips the canonical name record \(CNAME\) for your DB Instance to point at the standby, which is in turn promoted to become the new primary

