# NAT & Bastion

* You cannot use NAT instance to SSH/RDP into private subnet. For that Bastion \(Jump Box\) is required
* Bastions are used for secure administrative tasks only. Bastions are **placed in public subnets** and connect to private subnets via private IP
* For Bastion HA, have multiple Bastions in different AZs – at least 2 public subnets. Auto scaling in multiple AZ, route 53 doing health checks

