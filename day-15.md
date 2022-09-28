# Day 15 of #100daysofcloud

### I continued working on AWS EFS.

- EFS performance options are general purpose (default) and Max I/O. The general purpose is meant for most use cases up to 7000 file system operations per second and low latency requirements. The max I/O is used for operations with over 7000 file system operations per second and unlimited throughput and IOPS requirements.

- For EFS throughput (measured in mebibytes) options are bursting (default) and provisioned. The bursting option implies that there is more throughput up 100MiB/s or more and it increases with more file storage on our EFS. With provisioned throughput mode, it is possible to burst above the allowance based on the file system size at an additional charge. The provisioned throughput mode is used when the file system is relatively small but there is a need for a high throughput rate.

- AWS EFS gives us the ability to simultaneously access a network file across multiple EC2 instances via mount targets in the same AZ or across regions and hence promoting easier collaboration and remote work. The following shows the important steps I took while configuring EFS for multiple EC2 instances on AWS.

  - Created a security group for the EFS where only the EC2 security group is allowed for inbound rules
  - Created a mount point for the EFS and allowed only the EFS security group as incoming traffic.
  - Afterward, an NFS client was installed on the EC2 instances, a new folder that will be associated with EFS was created and the NFS file system was mounted. there was a need to update the ownership of the folder created. A test file was downloaded to the file system on the first EC2 instance (write instance).
  - A similar procedure was done on the other instance (read instance) and the downloaded network test file was available via the EFS shared file system.

- I learned that an AWS EFS file system can only have mount targets in one VPC at a time.
- In order to create AWS EFS, users must have adequate access control that enables that, and to effectively work with EFS, there is a need for appropriate IAM permissions

- EFS supports encryption both at rest and during the transition

- AWS DataSync is used to import on-prem data into EFS

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
