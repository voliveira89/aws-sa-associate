---
description: 'FAQ: https://aws.amazon.com/efs/faq/'
---

# Amazon Elastic File System

Amazon Elastic File System \(Amazon EFS\) provides simple, scalable file storage for use with Amazon EC2. With Amazon EFS, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it.

* Simple web services interface that allows you to create and configure file systems quickly and easily
* The service manages all the file storage infrastructure for you, avoiding the complexity of deploying, patching, and maintaining complex file system deployments
* Supports the **Network File System versions 4.0 and 4.1 \(NFSv4\) protocol**, so the applications and tools that you use today work seamlessly with Amazon EFS
* **Multiple Amazon EC2 instances can access an Amazon EFS file system at the same time**, providing a common data source for workloads and applications running on more than one instance or server
* You **pay only for the storage used by your file system**. You don't need to provision storage in advance and there is no minimum fee or setup cost.
* Allows you to control access to your file systems through** Portable Operating System Interface \(POSIX\)** permissions.

Amazon EFS supports two forms of encryption for file systems, **encryption in transit and encryption at rest**. You can enable encryption at rest when creating an Amazon EFS file system. If you do, all your data and metadata is encrypted. You can enable encryption in transit when you mount the file system. 

EFS is SSD based storage and its storage capacity and pricing will scale in or out as needed, so there is no need for the system administrator to do additional operations. It can grow to a petabyte scale.

