# EC2 Security Groups

* A security group is a **virtual firewall**
* First line of defense. Network ACLs are second line
* One instance can have multiple security groups.
* Each security group only "allows" inbound traffic, there will never be a conflict on security group rules
* Security group changes are applied immediately
* **Security groups are stateful**. Rules added as inbound rules – **automatic outbound rules are added**. Response back on the same channel. **NACLs are stateless**
* All inbound traffic **is blocked by default**. You have to allow specific inbound rules for protocols
* All outbound traffic is **allowed by default**
* Only allow rules, no deny rules exist. Use NACLs to deny specific IPs
* Any number of EC2 instances in a security group
* EC2 instances in the **default security group can communicate with each other**



