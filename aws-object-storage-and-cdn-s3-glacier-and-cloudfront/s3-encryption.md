# S3 Encryption

### **In Transit**

* Secured using SSL/TLS

### **At rest**

* Use** Server-Side Encryption** – You request Amazon S3 to encrypt your object before saving it on disks in its data centers and decrypt it when you download the objects.
  * Use Server-Side Encryption with Amazon S3-Managed Keys \(SSE-S3\)
  * Use Server-Side Encryption with AWS KMS-Managed Keys \(SSE-KMS\)
  * Use Server-Side Encryption with Customer-Provided Keys \(SSE-C\)
* Use **Client-Side Encryption** – You can encrypt data client-side and upload the encrypted data to Amazon S3. In this case, you manage the encryption process, the encryption keys, and related tools
  * Use Client-Side Encryption with AWS KMS–Managed Customer Master Key \(CMK\)
  * Use Client-Side Encryption Using a Client-Side Master Key

