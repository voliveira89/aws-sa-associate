---
description: 'https://aws.amazon.com/cloudhsm/faqs/'
---

# AWS CloudHSM

Is a **cloud-based hardware security module** \(HSM\) that enables you to **easily generate and use your own encryption keys** on the AWS Cloud.

* It is possible to lose keys that were created since the most recent daily backup if the CloudHSM cluster that you are using fails and you are not using two or more HSMs. Amazon strongly recommends that you **use two or more HSMs**, in separate Availability Zones, in any production CloudHSM Cluster to avoid loss of cryptographic keys.
* Amazon **does not have access to your keys or credentials** and therefore has no way to recover your keys if you lose your credentials.
* Dedicated access to HSM that complies with government standards \(FIPS, CC\)
* You control your keys and the application software that uses them

