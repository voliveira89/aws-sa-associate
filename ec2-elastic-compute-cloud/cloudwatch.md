# CloudWatch

* **Default Metrics** – Network, Disk , CPU and Status check \(Instance and System\)
* Memory – **RAM is a custom metric**
* You can create custom dashboards all CloudWatch metrics
* **CloudWatch alarms** – set notifications when particular thresholds are hit
  * Three states: OK, ALARM, or INSUFFICIENT\_DATA
* **CloudWatch events** help you respond to state changes. E.g. run Lambda function in response to
* **CloudWatch Logs** helps you monitor EC2 instance/application/system logs. Logs send data to CloudWatch
* The **CloudWatch Logs agent** provides an automated way to send log data to CloudWatch Logs from Amazon EC2 instances. The agent is comprised of the following components:
  * A plug-in to the AWS CLI that pushes log data to CloudWatch Logs.
  * A script \(daemon\) that initiates the process to push data to CloudWatch Logs.
  * A cron job that ensures that the daemon is always running.
* **Basic monitoring every 5 minutes**
* **Detailed monitoring every 1 minute**
* If the AWS service supports both basic and detailed monitoring, the basic would be enabled by default and the detailed monitoring needs to be enabled for details metrics
* Retention schedules:
  * 1 minute datapoints are available for 15 days
  * 5 minute datapoints are available for 63 days
  * 1 hour datapoints are available for 455 days



