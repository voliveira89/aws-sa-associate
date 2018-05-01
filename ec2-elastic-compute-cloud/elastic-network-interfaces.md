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

You can create and configure network interfaces in your account and attach them to instances in your VPC. Your account might also have requester-managed network interfaces, which are created and managed by AWS services to enable you to use other resources and services. You cannot manage these network interfaces yourself. 

All network interfaces have the _eni-xxxxxxxx_ resource identifier.

### Best Practices for Configuring Network Interfaces {#best-practices-for-configuring-network-interfaces}

* You can attach a network interface to an instance when it's **running \(hot attach\)**, when it's **stopped \(warm attach\)**, or when the instance is being **launched \(cold attach\)**.
* You can detach secondary \(eth_N_\) network interfaces when the instance is running or stopped. However, **you can't detach the primary \(eth0\) interface**.
* You can attach a network interface in one subnet to an instance in another subnet in the same VPC; however, **both the network interface and the instance must reside in the same Availability Zone**.
* When launching an instance from the CLI or API, you can specify the network interfaces to attach to the instance for both the primary \(eth0\) and additional network interfaces.
* Launching an Amazon Linux or Windows Server instance with multiple network interfaces automatically configures interfaces, private IPv4 addresses, and route tables on the operating system of the instance.
* A warm or hot attach of an additional network interface may require you to manually bring up the second interface, configure the private IPv4 address, and modify the route table accordingly. Instances running Amazon Linux or Windows Server automatically recognize the warm or hot attach and configure themselves.
* Attaching another network interface to an instance \(for example, a NIC teaming configuration\) cannot be used as a method to increase or double the network bandwidth to or from the dual-homed instance.
* If you attach two or more network interfaces from the same subnet to an instance, you may encounter networking issues such as asymmetric routing. If possible, use a secondary private IPv4 address on the primary network interface instead. 

