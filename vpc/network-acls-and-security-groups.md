# Network ACLs & Security Groups

| **Security Group** | **Network ACL** |
| --- | --- | --- | --- | --- | --- |
| Operates at the instance level \(first layer of defense\) | Operates at the subnet level \(second layer of defense\) |
| Supports allow rules only | Supports allow rules and deny rules |
| **Is stateful**: Return traffic is automatically allowed, regardless of any rules | **Is stateless**: Return traffic must be explicitly allowed by rules |
| We **evaluate all rules** before deciding whether to allow traffic | We process rules in **number order** when deciding whether to allow traffic. Lower order rules take effect in case of conflict with higher order rules. |
| Applies to an instance only if someone specifies the security group when launching the instance, or associates the security group with the instance later on | Automatically applies to all instances in the subnets it's associated with \(backup layer of defense, so you don't have to rely on someone specifying the security group\) |

* With default ACL, all inbound and outbound traffic is allowed automatically
* When custom ACL, all inbound and outbound traffic is denied by default
* 1 subnet &lt;=&gt; 1 AZ &lt;=&gt; 1 ACL. ACLs can be associated to only 1 subnet at a time. You can reassign to another subnet. If subnet is not associated with an ACL, the default ACL is applied
* AWS recommends adding ACL rules in increments of 100s
* Ephemeral ports – Allow inbound /outbound traffic from 1024 – 65535. As clients can initiate outbound connection from any random port. Ports &lt; 1024 reserved for super user access
* If you have to block a specific IP address / range, use ACLs instead of security groups. SGs can’t deny traffic – they only allow

