---
description: 'FAQ: https://aws.amazon.com/vpc/faqs/'
---

# VPC

* VPC is a logical data center within an AWS Region
* Control over network environment, select IP address range, subnets and configure route tables and gateways
* Do not span regions, but can span AZs
* Can create public facing subnet \(Web\) having internet access and private facing subnet \(DB\) with no internet access
* **Public Subnet** – Web Servers/Jump Boxes
* **Private Subnet** – Applications Servers/Database servers
* AWS gives a maximum of /16 network
* Bastion host/Jump Box in Public subnet
* Leverage multiple layers of security – Security groups and Network ACLs to control access to EC2 instances
* Security groups, Network ACLs, Route Tables can span subnets/AZs
* Security groups are **stateful**. Network ACLs are **stateless**
* Your VPC includes a default security group whose initial rules are to deny all inbound traffic, allow all outbound traffic, and allow all traffic between instances in the group. You can’t delete this group; however, you can change the group’s rules. The procedure is the same as modifying any other security group.
* Each subnet is always mapped to an availability zone. **1 subnet = 1 AZ**
* Only one internet gateway per VPC \(trick question – improve performance by adding Gateway – just not possible\)
* By default, how many VPCs am I allowed in each AWS Region? **5**
* Typical Private IP address ranges – not publically routable.
  * 10.0.0.0 - 10.255.255.255 \(10/8 prefix\)
  * 172.16.0.0 - 172.31.255.255 \(172.16/12 prefix\)
  * 192.168.0.0 - 192.168.255.255 \(192.168/16 prefix\)
* Create a VPN
  * **Virtual private gateway **- is the VPN concentrator on the Amazon side of the VPN connection. You create a virtual private gateway and attach it to the VPC from which you want to create the VPN connection.
  * **Customer gateway** - is a physical device or software application on your side of the VPN connection.
* To have HA in general or for ELB, ensure that you have at-least 2 public and or private subnets in different availability zones

