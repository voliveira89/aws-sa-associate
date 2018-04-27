# Overview of Security Processes Whitepaper

### Shared security model with AWS

* For IaaS - Customer manages OS and above including security and patches. E.g. with EC2, VPC, S3 – you are responsible for all security configuration and management. AWS manages hypervisor and below including physical infrastructure
* For SaaS – AWS manages everything except user credentials and account management. Recommended to have MFA access to these services, SSL/TLS access to these services and log all API/user usage using CloudTrail

![](https://lh4.googleusercontent.com/VQ93jp047HEnMzaE-NHP3UMGAVFylHuUn65QJlDpu4-Hy0Lh-yZHc_U3nUb-GVvH1a7IPULsGQ-HAN2vg_SOCKXW50vlqNUAVYcys9wZvRQWmcbW-FPVQ3_c_o_m50JahkG0RLGl)

### Storage Decommissioning

* When storage device reaches EoL, AWS procedures include decommissioning process to prevent customer data from being exposed in the cloud
* All decommissioned magnetic storage devices are degaussed and physically destroyed

### Network Security

* Transmission Protection – Connect via http or https using SSL
* Additional security via VPC, use IPsec to provide encrypted tunnel between Amazon VPC and customer data center. You can also use Amazon Direct Connect or Gateway Services.
* Logically Amazon production network is segregated from Amazon Corporate network using security/segregation devices. \[Amazon.com network different from AWS network\]

### Network monitoring and protection

* IP Spoofing – not possible. Each instance will send traffic with its own IP/MAC address
* No Man-in-Middle attacks due to Amazons control on host based firewalls
* Unauthorized port scans are violation. You should request in advance and limit scan only to your instances

### AWS Credentials

* Passwords, MFA, Access Keys, Key Pairs, X.509 certificates
* CloudFront content can be secured by using X.509 certificates. E.g. you can secure access to a CloudFront video by sharing the link using X.509 certificates.

### AWS Trusted Advisor

* Inspects your AWS environment and makes recommendation to save money, improve performance, fault tolerant architecture or close security gaps, and service limits.

### Instance Isolation

* Different instances running on the same physical machine are isolated from each other via the Xen Hypervisor. In addition AWS firewall sits between physical network interface and the instance’s virtual interface – all traffic must pass through this.
* RAM Isolation also along similar lines
* Customer don’t have access to RAW disks – instead are presented with virtual disks
* Disk zeroing – all disk and memory allocated to a guest is scrubbed to 0 by the hypervisor upon deallocation

### Guest Operating system

* AWS doesn’t have access to your VMs. No backdoors
* Encrypt Data at rest – AES 256. Encrypt EBS volumes and their snapshots. Encryption occurs on servers thus allowing for encryption between EC2 instances and EBS volumes
* To allow for efficiency, the EBS encryption feature is available only on EC2 powerful instances

### Firewall

* Mandatory inbound firewall is in default deny-all mode. Ingress denied by default and all egress is allowed.

### Elastic Load Balancing

* SSL termination on ELB is terminated. It allows you to identify the original client IP connecting to server either via HTTPS or TCP.

### Direct Connect

* Bypass internet service providers and connect directly to AWS resources
* You can extend office network range into AWS VPC and connect to the VPC instances using Direct connect

