# NAT Instance & NAT Gateway

* Enable instances in a private subnet to **connect to the internet or other AWS services**, but prevent the internet from initiating a connection with those instances.
* **NAT Instance is one EC2 instance**. You are responsible for performance management, scale out and security groups. **NAT Gateway is a managed service.**
* On NAT instance, remember to disable source/destination IP check. This is required to allow private subnet internet connectivity. This is not required on NAT Gateway
* Allow both HTTP and HTTPS access on security groups associated with NAT instances. Security groups are always associated with NAT Instances
* Both NAT Instance and NAT Gateways are deployed to public subnet. Elastic IP has to be added to NAT Instance. NAT Gateway is automatically assigned a public IP
* In VPC, update default route table to allow connectivity from private subnet to NAT Instance and Gateway
* NAT instance is single point of failure. You can place NAT instance behind Auto Scaling group, multiple subnets in different AZs and scripted failover. To improve performance increase the size of the NAT instance to allow for higher throughput
* You can use Network ACLs to control traffic for both NAT Instance and Gateway
* NAT Gateways scale up to 10GBps. No need to disable source/ destination checks on Gateways

