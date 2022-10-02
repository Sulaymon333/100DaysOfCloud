# Day 16 of #100daysofcloud

### I continued working on AWS Storage services.

- AWS DataSync is used to securely migrate on-prem data into EFS or S3 through the AWS Direct Connect link (or over the internet) using AWS DataSync Agent (VMWare ESXi).

- EC2 instance store is block-level storage that is physically attached to the underlying EC2 instance and provides the highest I/O speed for data stored on them. The instance store volume size increase with the EC2 instance size selected. Not all EC2 instance types support instance store volumes.

- It must be noted that the data stored on instance store volumes will be lost when the EC2 is terminated or stopped. So, no critical data should be stored on this volume but only frequently changing data (cache or buffer) should be stored on instance store volumes. Although, The data is retained if the EC2 instance is simply restarted/rebooted.

- Since the instant store is ephemeral storage, it is not recommended for persistent data or data that needs to be shared by multiple entities. No extra cost or security protection is provided for this kind of block storage beyond the underlying EC2 instance it is attached to.

- EBS is a persistent and durable block-level data storage that can be logically attachable to an EC2 instance. It is a separate resource and it is independent of an EC2 instance, unlike the instant store volume. EBS is useful for applications with specific IOPS (input/output per second) where data changes frequently.

- Without using the Multi-Attach feature, EBS can only be attached to one EC2 instance but many EBS volumes can be attached to the same EC2 instance at once. The EC2 instances and the EBS volumes must be in the same AZ for attachment to be possible. Users can determine what happens to the EBS volume (delete or retain) when the EC2 instance connected is being terminated.

- EBS Multi-Attach enables the possibility to attach an EBS volume to multiple instances at the same time. EBS Multi-Attach is only available on both provisioned IOPS SSD (io1) and provisioned IOPS SSD (io2). These volume types are typically used for specialised operations that require high throughput, high performance, and low latency.

- Additionally, EBS Multi-Attach can only be used with nitro-based EC2 instances. It is only recommended to use Multi-Attach with only Linux-based instances and not Windows. Encryption is still possible, requires the same AZ as the EC2 instance, and the recommended file system is GFS2 (cluster file system) and not EXT4 or XFS due to possible data loss. Delete on termination is based on the setting of the last EC2 instance connected.

- EBS data can be replicated/backed up through snapshots either manually or through automated AWS Cloudwatch events. The snapshots are incremental and only update new data on the block. The snapshots are stored on S3 buckets and replicated across multiple AZs. It is possible to resize the EBS volumes when needed.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
