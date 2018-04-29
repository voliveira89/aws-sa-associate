# Volumes and Snapshots

* **Volumes are virtual hard disks**
* You can attach volume to EC2 instance belonging to same AZ
* To detach a volume from EC2 instance, you have to unmount it first
* **Snapshots are point in time copies of volumes** – stored in S3. Taking first snapshot takes a while.
* Subsequent snapshots **will only store the delta in S3**. Only changed blocks are stored in S3
* You can create volumes from Snapshots. During this you can also change Volume Storage Type
* Volume is just block data. You need to format it create specific file system e.g. ext4
* Root Volume is one where OS is installed/booted. **It is not encrypted by default** on AWS AMIs
* Making your snapshot public shares all snapshot data with everyone; however, snapshots with AWS Marketplace product codes cannot be made public. Encrypted snapshots cannot be shared between accounts or made public.
* Snapshots that are taken from encrypted volumes are automatically encrypted. Volumes that are created from encrypted snapshots are also automatically encrypted.
* You can take a snapshot of an attached volume that** is in use**. However, snapshots only capture data that has been written to your Amazon EBS volume at the time the snapshot command is issued.
* One can **encrypt a volume that isn't encrypted** from a snapshot by following the below steps:
  * Create a snapshot of your unencrypted EBS volume. This snapshot is also unencrypted.
  * Copy the snapshot while applying encryption parameters. The resulting target snapshot is encrypted.
  * Restore the encrypted snapshot to a new volume, which is also encrypted.
* A **golden AMI** is simply a customized Amazon Machine Image that contains the latest security patches, software, configuration and software agents. You can build and deploy golden AMIs in your environment, but the AMIs quickly become dated as new vulnerabilities are discovered.

