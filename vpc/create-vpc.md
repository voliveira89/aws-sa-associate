# Create VPC

* Create VPC
  * Define IP range \(automatically creates default route table\)
  * Tenancy option - Dedicated hardware
* Create subnets \(automatically creates route table & nACL\)
  * Largest = /16, Smallest = /28 
  * AWS reserves the 1st 4 and last 1 IP address of any subnet, so /28 = 11 usable IPs 
    * \(32-28=4, 2x2x2x2=16-5=11\)
* Create IGW
  * By default it’s detached, need to **manually attach it** to VPC
* Create custom route table & attach IGW to it
* Associate public subnet\(s\) to use new route
  * Enable auto-assign IPv4 address
* Launch 1 instance per subnet
  * Create a new security group \(rules depend on instance objective\)
* Provision EC2 NAT instance or NAT Gateway
  * Create security group for NAT instance

The **VPC Wizard** offers the following configuration:

1. VPC with a Single Public Subnet
2. VPC with Public and Private Subnets
3. VPC with Public and Private Subnets and Hardware VPN Access
4. VPC with a Private Subnet Only and Hardware VPN Access

![VPC with Public and Private subnets](https://lh3.googleusercontent.com/cabetFgQB1OeG8Nv0vbGvxMMr8xtcS4NQXHyxYFlHrrfd7TdPiP4_ra6BEZmDxOwstBkABsqZGGrXzyk7AHYC4BJQ9tjKWqwpJ3FB1eNSZb36fTxKQKPmGOBOANNQS2a6femwAVF)

### **Custom VPC Info**

* Default security group, network ACL & route table are created for each custom VPC you create
* Doesn’t create subnets or internet gateways out of the box
* In each VPC you create, **5 IP addresses are reserved by AWS for itself**. First 4 and last IP in the CIDR block
* You **can't change the size of a VPC** after you create it. If your VPC is too small to meet your needs, create a new, larger VPC, and then migrate your instances to the new VPC To do this, create AMIs from your running instances, and then launch replacement instances in your new, larger VPC. You can then terminate your old instances, and delete your smaller VPC.
* You **can’t attached multiple Internet Gateways** to the VPC to boost performance
* When creating VPCs do not modify default route table to add your custom rules. If you modify the default route, it will affect all instances. Create a new route table for customization

### **Default vs Custom VPC**

* When you create an account a default VPC is created for you in each region
* All subnets in default VPC have a route out to the internet
* Each EC2 instance in default VPC will have a public and private IP address
* If you delete default VPC, only way to restore it is by contacting Amazon

