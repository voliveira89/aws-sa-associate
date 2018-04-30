# EC2 Tips

**When you stop a running instance, the following happens:**

* The instance performs a normal shutdown and stops running; its status changes to stopping and then stopped.
* Any Amazon EBS volumes remain attached to the instance, and their data persists.
* Any data stored in the RAM of the host computer or the instance store volumes of the host computer is lost
* In most cases, the instance is migrated to a new underlying host computer when it's started.
* _EC2-Classic:_ AWS releases the public and private IPv4 addresses for the instance when you stop the instance, and assign new ones when you restart it.
* _EC2-VPC:_ The instance retains its private IPv4 addresses and any IPv6 addresses when stopped and restarted. AWS releases the public IPv4 address and assign a new one when you restart it.
* _EC2-Classic:_ AWS disassociates any Elastic IP address that's associated with the instance. You're charged for Elastic IP addresses that aren't associated with an instance. When you restart the instance, you must associate the Elastic IP address with the instance; AWS doesn't do this automatically.
* _EC2-VPC: _The instance retains its associated Elastic IP addresses. You're charged for any Elastic IP addresses associated with a stopped instance

#### EC2 Instance Meta-Data

* curl [http://169.254.169.254/latest/meta-data/](http://169.254.169.254/latest/meta-data/)
* Instance information is available in Meta-Data. Not in User-Data

Notes:

* EC2 Key Pairs are region specific
* Scripts can be passed on to the EC2 instance at first boot time as part of user-data
* EC2 – 1 subnet equals 1 Availability Zone
* Default VPC & Security group is created in when you create your account
* Default CloudWatch monitoring – **every 5 mins**. Can enabled advanced monitoring to check at interval of **each minute**
* Tag everything on AWS
* Termination protection is **turned off by default**. You need to turn it on
* When instance is terminated, root volume is deleted. You can turn if off
* It exists a soft limit to launch only **20 instances at a time, per region**
* **Enhanced networking** provides higher bandwidth, higher packet-per-second \(PPS\) performance, and consistently lower inter-instance latencies.

