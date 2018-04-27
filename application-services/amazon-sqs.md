# Amazon SQS

* SQS \(Simple Queue Service\) is a distributed web service that gives you access to a message queue that can be used to store messages while waiting for a computer to process them
* SQS helps decouple the components of an application so they can run independently
* Messages can be retrieved via SQS API
* The producer and consumer can run at their own independent throughput
* The queue acts as a buffer between consumer and producer. Ensures delivery of messages at least once. Ensure your application isn’t affected by processing the same message multiple times
* The default message r**etention period is 4 days**. You can increase the message retention period to a **maximum of 14 days**.
* Allows multiple readers and writers. Single queue can be used simultaneously by various applications – helps scale out applications
* SQS Message size up to **256KB** of text in any format. May consist of 1-10 messages
* Does **not guarantee FIFO messages**. If order is important, add sequencing information in each message
* SQS guarantees that your messages will be **processed at least once**
* Long polling is a way to retrieve messages from Amazon SQS queues. While the regular short polling returns immediately, even if the message queue being polled is empty, long polling doesn’t return a response until a message arrives in the message queue, or the long poll timeout
  * To enable long polling, set **ReceiveMessageWaitTimeSeconds to a number greater than 0**
* For SQS, you have to pull messages. It doesn’t push messages – unlike SNS. 

**Pricing**

* First 1 million SQS Requests per month are free
* $0.50 per 1 million SQS requests per month thereafter
* 64KB chunk = 1 request. So a message of 256KB = 4 requests
* Each messages has a visibility timeout – 12 hours by default \(maximum\). Visibility timeout period only starts when a worker node has picked up the message for processing. During this interval, the message is invisible to other processor workers
* SQS can do auto-scaling. If queue grows beyond a threshold, instantiate new web/app servers. Use Auto scaling + SQS to achieve this

### **Message Lifecycle**

1. Component 1 sends Message A to a queue, and the message is distributed across the Amazon SQS servers redundantly.
2. When Component 2 is ready to process a message, it consumes messages from the queue, and Message A is returned. While Message A is being processed, it remains in the queue and isn't returned to subsequent receive requests for the duration of the visibility timeout.
3. Component 2 deletes Message A from the queue to prevent the message from being received and processed again once the visibility timeout expires.

