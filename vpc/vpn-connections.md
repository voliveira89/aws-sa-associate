# VPN Connections

You can connect your VPC to remote networks by using a VPN connection which can be **Direct Connect, IPsec VPN connection, AWS VPN CloudHub, or a third party software** VPN appliance.

### Components

**Virtual Private Gateway -** A virtual private gateway is the VPN concentrator on the Amazon side of the VPN connection. You create a virtual private gateway and attach it to the VPC from which you want to create the VPN connection. Create a custom route table, updating your security group rules, and creating an AWS managed VPN connection

**Customer Gateway - **A customer gateway is a physical device or software application on your side of the VPN connection. To create a VPN connection, you must create a **customer gateway resource** in AWS, which provides information to AWS about your customer gateway device. Next, you have to setup an Internet-routable IP address \(static\) of the customer gateway's external interface



