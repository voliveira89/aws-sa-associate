# Provisioned IOPS

* Amazon RDS provisions that IOPS rate and storage for the lifetime of the DB instance or until you change it
* Provisioned IOPS storage** is optimized for I/O intensive**, Online Transaction Processing \(OLTP\) workloads that have consistent performance requirements
* Provisioned IOPS helps performance tuning
* You can modify the settings for an Oracle, PostgreSQL, MySQL, or MariaDB DB instance that uses Provisioned IOPS storage by using the AWS Management Console, the Amazon RDS API, or the AWS Command Line Interface \(AWS CLI\).

|  | **Range of Provisioned IOPS** | **Range of Storage** | **Range of IOPS to Storage \(GiB\) Ratio** |
| --- | --- | --- | --- | --- | --- | --- |
| **MariaDB** | 1,000–40,000 IOPS | 100 GiB–16 TiB | 1:1–50:1 |
| **Microsoft SQL Server, Enterprise and Standard editions** | 1000–32,000 IOPS | 200 GiB–16 TiB | 1:1–50:1 |
| **Microsoft SQL Server, Web and Express editions** | 1000–32,000 IOPS | 100 GiB–16 TiB | 1:1–50:1 |
| **MySQL** | 1,000–40,000 IOPS | 100 GiB–16 TiB | 1:1–50:1 |
| **Oracle** | 1,000–40,000 IOPS | 100 GiB–16 TiB | 1:1–50:1 |
| **PostgreSQL** | 1,000–40,000 IOPS | 100 GiB–16 TiB | 1:1–50:1 |

