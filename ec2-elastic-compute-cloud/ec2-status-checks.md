---
description: >-
  There are two types of status checks: system status checks and instance status
  checks.
---

# EC2 Status Checks

### **System Status Checks**

Monitor the AWS systems required to use your instance to ensure they are working properly. These checks detect problems with your instance that require AWS involvement to repair. When a system status check fails, you can choose to wait for AWS to fix the issue, or you can resolve it yourself \(for example, by stopping and starting an instance, or by terminating and replacing an instance\).

The following are examples of problems that can cause system status checks to fail:

* Loss of network connectivity
* Loss of system power
* Software issues on the physical host
* Hardware issues on the physical host that impact network reachability

### **Instance Status Checks**

Monitor the software and network configuration of your individual instance. These checks detect problems that require your involvement to repair. When an instance status check fails, typically you will need to address the problem yourself \(for example, by rebooting the instance or by making instance configuration changes\).

The following are examples of problems that can cause instance status checks to fail:

* Failed system status checks
* Incorrect networking or startup configuration
* Exhausted memory
* Corrupted file system
* Incompatible kernel

