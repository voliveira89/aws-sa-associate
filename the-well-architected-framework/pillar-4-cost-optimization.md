# Pillar 4 - Cost Optimization

Use cost to minimum and use the savings in other parts of business.

### **Design Principles**

* Transparently attribute expenditure – tag who spends how much and optimize accordingly
* Use managed services to reduce cost of ownership
* Trade capital expense for operating expense
* Benefit from economies of scale
* Stop spending money on data center operations

### **Best Practices**

**Match supply and demand**

* Don’t over or under provision. Use Auto scaling or Lambda for serverless. Pay only when used. Use CloudWatch.
* **Questions**
  * How do you ensure capacity matches and does not substantially exceed your need?
  * How do you optimize your usage of AWS resources?

**Cost effective resources**

* Use the correct instance type. A well architected system will use the most cost efficient resources to reach the end business goal.
* **Questions**
  * Have you selected appropriate resource type to match cost targets?
  * Have you selected the appropriate pricing model?
  * Are there managed services which can be used to improve ROI?

**Expenditure awareness**

* Isolate AWS Accounts in the same organization. Need to be aware which team is spending where. Also use 3rd party tools and tags. Billing alerts.
* Consolidated billing
* **Questions**
  * What access controls are in place to govern AWS costs?
  * How are you monitoring usage and spending?
  * How are you decommissioning resources you don’t need or stop that are temporarily not needed?
  * How do you consider data transfer changes?

**Optimizing over time**

* AWS Constantly changing. What is good today might not be so good next time around when newer changes are released.
* Subscribe to AWS Blog
* Use AWS Trusted Advisor
* **Questions**
  * How do you manage and/or consider adoption of new services?

#### **Key AWS Services**

* Match supply and demand – Auto scaling
* Cost effective resources – EC2 \(reserved instances\), AWS Trusted Advisor
* Expenditure awareness – CloudWatch alarms, SNS
* Optimizing over time – AWS Blog, AWS Trusted Advisor

