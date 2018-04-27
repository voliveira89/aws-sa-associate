# Snowball

Next version of Import/Export Gateway. You could accelerate moving large amounts of data into and out of AWS using portable storage devices for transport. Ship the storage device – no need to transfer over the internet. Problem arose with different types of disks.

### Snowball Standard

* Bigger than briefcase sized storage devices
* Petabyte scale data transport solution used to transfer data in/out of AWS
* Cost is 1/5th as compared to transfer via high speed internet
* 80TB snowball available
* Multiple layers of security to protect data. Tamper resistant enclosure, 256-bit encryption
* Once data is transferred, AWS performs software erasure of Snowball appliance
* If using Glacier first need to import into S3 and then into Snowball

### Snowball Edge

* 100 TB data transfer device which has onboard storage and compute capabilities
* Move large amounts of data in and out of AWS, as a temporary storage tier for large local datasets
* You can run Lambda functions
* Devices connect to existing applications and infrastructure using standard storage interfaces
* Snowball Edges can be clustered together to process your data on premise

### Snowmobile

* Massive 45 foot long ruggedized shipping container, pulled by a truck.
* Petabyte or Exabyte of data that has to be transferred to AWS. 100 PB per snowmobile.
* You can use it for data center migration

