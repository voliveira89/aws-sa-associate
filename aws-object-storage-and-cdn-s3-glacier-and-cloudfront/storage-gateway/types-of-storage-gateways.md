# Types of Storage Gateways

**File Gateway \(NFS\)** – Just store files in S3 – Word, Pictures, PDFs, and no OS. Saves a lot of money. Files are stored as objects in S3 buckets and accessed over NFS mount point. File attributes as stored as S3 object metadata. Once transferred to S3, standard S3 features apply to all files.

**Volumes Gateway \(iSCSI\) **– uses block based storage – virtual hard disk, operating system.

* Stored Volumes – Store entire data set copy on-prem. Data async backed up to AWS S3
* Cached Volumes – Stored only recently accessed data on-premise. Rest on AWS S3

Volume gateway interface presents applications with disk volumes using iSCSI protocol. They take virtual hard disks on premise and back them up to virtual hard disks on AWS. Data written to these volumes can be asynchronously backed up as point in time snapshots of volumes and stored in cloud as EBS snapshots.

**Gateway Virtual Tape Library \(VTL\)** – Backup and Archiving solution. Create tapes and send to S3. You can use existing backup applications like NetBackup, Backup Exec, and Veam etc.

