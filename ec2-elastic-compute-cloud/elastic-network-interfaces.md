# Elastic Network Interfaces

An elastic network interface is a logical networking component in a VPC that represents a virtual network card.

A network interface can include the following attributes:

* A primary private IPv4 address from the IPv4 address range of your VPC
* One or more secondary private IPv4 addresses from the IPv4 address range of your VPC
* One Elastic IP address \(IPv4\) per private IPv4 address
* One public IPv4 address
* One or more IPv6 addresses
* One or more security groups
* A MAC address
* A source/destination check flag
* A description

You can create and configure network interfaces in your account and attach them to instances in your VPC. Your account might also have _requester-managed_ network interfaces, which are created and managed by AWS services to enable you to use other resources and services. You cannot manage these network interfaces yourself. 

All network interfaces have the _eni-xxxxxxxx_ resource identifier.

