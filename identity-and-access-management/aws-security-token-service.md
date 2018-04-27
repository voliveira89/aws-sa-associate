# AWS Security Token Service

Grants users **limited and temporary access** to AWS resources

* User can come from:
  * Federation \(e.g. Active Directory\)
  * Federation with Mobile Apps
  * Cross Account Access
* Key terms
  * Federation - Combining users from different domains
  * Identity Broker - Allows to take an identity from point A and joint it to point B
  * Identity Store - Services like Active Directory, Facebook, Google
  * Identities - A user of a service
* Steps
  * Develop an Identity Broker to communicate with LDAP and AWS STS
  * Identity Broker always authenticates with LDAP first, then with AWS STS
  * Application then gets temporary access to AWS resources

