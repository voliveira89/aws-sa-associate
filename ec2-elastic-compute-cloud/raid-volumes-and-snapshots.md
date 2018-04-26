# RAID, Volumes & Snapshots

* RAID types:
  * **RAID 0** – Striped, No Redundancy, Good Performance – No Backup/Failover
  * **RAID 1** – Mirrored, Redundancy
  * **RAID 5 **– Good for reads, bad for writes. AWS doesn’t recommend using RAID 5 on EBS
  * **RAID 10 **– Raid 0 + Raid 1
* Use RAID Arrays when a single volume IOPs are not sufficient for your need. E.g. Database. Then you create RAID Array to meet IOPs requirements
* To take snapshot of RAID Array
  * 1- Stop the application from writing to cache and flush all cache to Disk
  * 2 - Freeze the file system
  * 3 - Umount the RAID Array
  * 4 - Shutdown the EC2 instance
* Snapshots of encrypted volumes are encrypted automatically
* You can copy snapshot to another region while encrypting it
* The EC2 instance thus created will have root volume encrypted
* You can’t share encrypted snapshots as the encryption key is tied to your account

