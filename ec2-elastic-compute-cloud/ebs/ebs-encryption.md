# EBS Encryption

* EBS encryption uses AWS Key Management Service \(AWS KMS\) customer master keys \(CMKs\) when creating encrypted volumes and any snapshots created from them.
* EBS Root Volumes can be encrypted on custom AMIs only. Not on the default available AMIs. To encrypt root volumes, create a new AMI and encrypt root volume. You can also encrypt using 3rd party software like Bit Locker. Additional volumes attached to EC2 instance can be encrypted.
* When you create an encrypted EBS volume and attach it to a supported instance type, the following types of data are encrypted:
  * Data at rest inside the volume
  * All data moving between the volume and the instance
  * All snapshots created from the volume
  * All volumes created from those snapshots

