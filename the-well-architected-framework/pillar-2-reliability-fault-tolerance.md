# Pillar 2 - Reliability / Fault Tolerance

* Ability of system to recover from service or infrastructure outages/disruptions
* Ability to dynamically scale

### **Design Principles**

* Test recovery procedures. E.g. Netflix simian army
* Automatically recover from failure – anticipate and recover from failure
* Scale horizontally to increase system availability
* Stop guessing capacity – don’t under provision or over provision

### **Best Practices**

**Foundations**

* E.g. side of communication link between HQ and Data Center
* AWS handles networking and compute resources. However, there are service limits to stop customers from overprovisioning. You can request increase
* **Questions**
  * How are you managing AWS Service Limits?
  * How are you planning your network topology on AWS?
  * Do you have an escalation path to deal with technical issues?

**Change Management**

* Aware of how software changes affect environments
* With AWS use CloudWatch to monitor your environment. Traditional IT Change control is not required in cloud
* **Questions**
  * How system adapts to change in demand?
  * How you monitor AWS resources?
  * How you execute change management

**Failure Management**

* Architect systems assuming failure will occur
* **Questions**
  * How are you backup up data?
  * How does system withstand component failure?
  * How are you planning for recovery?

### **Key AWS Resources**

* Foundations – IAM, VPC
* Change Management - CloudTrail
* Failure Management - CloudFormation

