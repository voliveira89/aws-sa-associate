# EBS vs Instance Store

* You can **reboot or terminate** instance store backed EC2 VMs
* You can **start, stop, reboot or terminate** EBS backed EC2 VMs
* EC2 instance on instance store is lost if host hypervisor fails. Not so with EBS backed instances.
* EBS volumes can be attached/detached to EC2 instances. One at a time
* EBS backed AMI is from EBS snapshot
* Instance store back volume is from template in S3. Hence slower to provision
* You will not lose data if you reboot for both
* With EBS, you can ask AWS not to delete the volume upon instance termination



