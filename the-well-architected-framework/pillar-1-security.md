# Pillar 1 - Security

### **Design Principles**

1. Apply security at all layers
   1. Not just edge firewalls. Apply it a subnet level, ACLs, which ports used on ELB, instances
   2. Run antivirus on Windows instances
2. Enables traceability
3. Automate responses to security events – E.g. SNS notification for ssh
4. Focus on securing your system
5. Automate security best practices – Use hardened AMIs
6. AWS Shared Responsibility Model – Customer responsible for data and OS. AWS responsible for security of underlying infrastructure & as a service offerings – RDS etc.

### **Best Practices**

**Data protection**

* Basic data classification should be in place. Organize data into segments. Who should have access to data? Implement least privilege principle
* Encrypt everything where possible – both at rest and in transit
* AWS customers maintain full control of their data
* AWS makes it easier for you to encrypt your data and manage keys – KMS or by a customer
* Detailed logging available
* AWS systems are exceptionally resilient
* Versioning can be used as data lifecycle management
* AWS never initiates movement of data between regions unless a feature is enabled or leverages a services
* **Questions**
  * How are you encrypting data at rest and transit?
  * How are you encrypting data at rest and transit \(SSL\)?

**Privilege management**

* Allow only authorized and authenticated users are able to access resources. This is achieved via:
  * ACLs
  * RBAC – Role based access control
  * Password Management
* Questions
  * How are you protecting access to and use of AWS root account credentials?
  * How are you defining roles and responsibilities of system users to control human access to AWS Console and APIs – e.g. Groups for system admins, group for HR and other departments?
  * How are you limiting automated access to AWS resources? – Application scripts, tools – by using roles
  * How are you managing keys and credentials?

**Infrastructure protection**

* How do you protect your data center – RFID controls, security, CCTV etc?
* Infrastructure protection essentially exists at VPC level – Physical infra is managed by AWS
* Questions
  * How are you enforcing network and host-level boundary protection? E.g. Jump host. Which ports can be used.
  * How are you enforcing AWS Service level protections? Are you using IAM?
  * How are you protecting integrity of operating system?

**Detective controls**

* Detect or identify a security breach
  * CloudTrail
  * CloudWatch
  * Config
  * S3
  * Glacier
* Questions
  * How are you capturing and analyzing your AWS logs. CloudTrail is a regional service. Which 3rd party tools you are using for this analysis.

### **Key AWS Services**

* ELB, EBS, S3, RDS
* IAM, MFA
* VPC
* CloudTrail, CloudWatch, Config

