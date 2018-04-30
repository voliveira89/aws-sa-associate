# EC2 Options

### **On demand** 

Allow you to pay a fixed rate **by the second** \(it used to by both of the hour and second\) with no commitment.

* Users that want the low cost and flexibility of EC2 without any upfront payment or long term commitment.
* Applications with short term, spiky, or unpredictable workloads that cannot be interrupted.
* Applications being developed or tested on EC2 for the first time.

### **Reserved** 

Provide you with a capacity reservation, and offer a significant discount on the hourly charge for an instance. 1 year or 3 year terms. Pay upfront, get discount \(**upto 70%**\).

* Applications with steady state or predictable usage.
* Applications that require reserved capacity.
* Reserved instances can’t be moved from one region to another
* Users able to make upfront payments to reduce their total computing costs even further:
  * Standard RI \(Reserved Instances\)
  * Convertible RI
  * Scheduled RI
* To **stop incurring charges** you have to:
  * Terminate the Reserved instances as soon as possible
  * Go to the AWS Reserved Instance Marketplace and sell the Reserved instances

### **Spot**

Enable you to bid whatever price you want for instance capacity, providing for even greater savings if your applications have flexible start and end times.

* Applications that have flexible start and end times
* Applications that are only feasible at very low compute prices
* Users with urgent computing needs for large amounts of additional capacity
* By simply selecting Spot when launching EC2 instances, you can **save up-to 90%** on On-Demand prices.
* If your Spot instance is terminated or stopped by Amazon EC2 in the first instance hour, you will not be charged for that usage. However, if you terminate the instance yourself, you will be charged to the nearest second. If the Spot instance is terminated or stopped by Amazon EC2 in any subsequent hour, you will be charged for your usage to the nearest second. If you are running on Windows and you terminate the instance yourself, you will be charged for an entire hour.
* You can choose to have your Spot instances terminated, stopped, or hibernated upon interruption. Stop and hibernate options are available for persistent Spot requests and Spot Fleets with the maintain option enabled. **By default, your instances are terminated.**

### Dedicated Hosts

Physical EC2 server dedicated for your use. Dedicated Hosts can help you reduce costs by allowing you to use your existing server-bound software licenses.

* Useful for regulatory requirements that may not support multitenant virtualization.
* Great for licensing which doesn't support multi-tenancy or cloud deployments.
* Can be purchased On-Demand \(hourly\).
* Can be purchased as a Reservation for up to 70% off the On-Demand price.

