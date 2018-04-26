# Auto Scaling 101

* Before you can create auto scaling group you **need to create a launch configuration**
* **Launch Configuration** – Select AMI, Instance Type, Bootstrap script
* No actual instances are created just with launch configuration
* **Auto scaling group** – Set minimum size, spread it over subnets \(AZs\) - select all available AZs
* Run health checks from ELB
* Configure Auto scaling policy – Based on Alarm take action – trigger a new instance creation when CPU Utilization is greater than 90% for 5 minutes. You can also delete instance based on alarms
* When Auto scaling group is launched it creates the instances based on definition
* The cooldown period is a configurable setting for your Auto Scaling group that helps to ensure that it doesn't launch or terminate additional instances before the previous scaling activity takes effect. The default value for cooldown period is 300 seconds
* Attach EC2 Instances to Your Auto Scaling Group
  * The instance is in the **running state**
  * The AMI used to launch the instance **must still exist**
  * The instance is **not a member **of another Auto Scaling group
  * The instance is in the **same Availability Zone** as the Auto Scaling group
  * If the Auto Scaling group has an attached load balancer, the instance and the load balancer must both be in EC2-Classic or the same VPC. If the Auto Scaling group has an attached target group, the instance and the load balancer must both be in the same VPC.

![Scale in diagram](https://lh4.googleusercontent.com/2gOQnmpZsz2BS3hZa98o5z9HdaTQjfv4hFYwCFZNL2ocp2m52mc1F-viPzYY_r1dWhRzakYW-m6Dk7Sl6qdd2Dl4IGD1pBZT34pQsCoDX4VrdIU4IxpW2bK5_s3wMGtPu11jkXM9)



