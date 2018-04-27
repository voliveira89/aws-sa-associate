---
description: 'FAQ: https://aws.amazon.com/swf/faqs/'
---

# Amazon SWF

* SWF \(Simple Workflow Service\) is a web service that makes it easy to coordinate work across distributed application components. Coordinate tasks & workflows
* Amazon uses SWF to process orders on its website
* No EC2 components involved
* It can also involve human actors

### **SWF Actors**

1. WF Starters – e-commerce application
2. WF Deciders – Control flow of activity tasks
3. WF Activity workers – Carry out actual task

### **SQS vs SWS**

| **Attribute** | **SQS** | **SWF** |
| --- | --- | --- | --- | --- |
| **Retention** | 14 days \(max\) | 1 year |
| **API** | Message Oriented | Task Oriented |
| **Assignment** | Might be assigned multiple times | Only once |
| **State** | Write code to implement tracking | Keeps Track of State & Events |

