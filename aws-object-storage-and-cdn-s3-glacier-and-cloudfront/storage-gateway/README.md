# Storage Gateway

* It is a service which connects an on-premises software appliance \(virtual\) with cloud based storage to provide seamless and secure connectivity between the two. Either via internet or Direct Connect.
* It can also provide connectivity from EC2 instance in VPC to S3 via Storage Gateway in same VPC
* The virtual appliance will asynchronously replicate information up to S3 or Glacier
* Can be downloaded as a VM – VMware ESXi / Hyper-V.
* All data transferred between any type of gateway appliance and AWS storage is encrypted using SSL. By default, all data stored by AWS Storage Gateway in S3 is encrypted server-side with Amazon S3-Managed Encryption Keys \(SSE-S3\). Also, when using the file gateway, you can optionally configure each file share to have your objects encrypted with AWS KMS-Managed Keys using SSE-KMS.



