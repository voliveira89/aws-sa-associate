# Pillar 5 - Operational Excellence

Includes operational practices and procedures used to manage production workloads. Change execution and responses should be automated. All processes and procedures of operational excellence should be documented, tested and regularly reviewed.

### **Design Principles**

* Perform operations with code
* Algin operations processes to business objectives
* Make regular, small, incremental changes
* Test for responses to unexpected events
* Learn from operational events and failures
* Keep operations procedures current

### **Best Practices**

**Preparation**

* Operations checklists will ensure that workloads are ready for production operation
* Workloads should have
  * Runbooks - Operations guidance that operations teams can refer to so they can perform normal daily tasks
  * Playbooks - Guidance for responding to unexpected operational events.
* CloudFormation can used to ensure that environments contain all required resources when deployed in production
* Implement auto scaling
* Use AWS Config rules feature to create mechanisms to automatically track and respond to changes in workloads and environments
* Use tagging
* **Questions**
  * What best practices for cloud operations are you using?
  * How are you doing configuration management for your workload?

**Operations**

* Should be standardized and manageable on a routine basis
* Focus on automation
* Use AWS to set up a CI/CD pipeline
* **Questions**
  * How are evolving your workload while minimizing the impact of change?
  * How do you monitor your workload to ensure it is operating as expected?

**Responses**

* Responses to unexpected operational events should be automated
* **Questions**
  * How do you respond to unplanned operational events?
  * How is escalation managed when responding to unplanned operational events?

### **Key AWS Services**

* Preparation - AWS Config, AWS Service Catalog, Auto Scaling, Amazon SQS
* Operations - AWS CodeCommit, AWS CodeDeploy, AWS CodePipeline, AWS SDKs, AWS CloudTrail
* Responses - Amazon CloudWatch

