# Backups

* **Automated Backups** – full daily snapshot & will also store transaction logs
* Enabled by default. Stored in S3. Free backup storage in S3 up to the RDS Instance size
* You can define backup window \(changes to the backup window take effect immediately\)
* Backups are deleted when the RDS Instance is deleted
* Backup retention period - **1 to 35 days \(0 to disable backups\)**
* For the MySQL DB engine, automated backups are only supported for the InnoDB storage engine; use of these features with other MySQL storage engines, including MyISAM, may lead to unreliable behavior while restoring from backups.

