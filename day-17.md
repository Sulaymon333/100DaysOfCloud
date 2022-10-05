# Day 17 of #100daysofcloud

### I continued working on AWS Storage services.

- EBS data can be replicated/backed up through snapshots either manually or through automated AWS Cloudwatch events. The snapshots are incremental and only update new data on the block. The snapshots are stored on S3 buckets and replicated across multiple AZs. It is possible to resize the EBS volumes when needed.

- EBS volume encryption can be enabled by users and it is based on the AES-256 algorithm via AWS KMS (Key Management Service) using CMK - Customer Master Keys. EBS volumes that are not encrypted cannot be used to generate encrypted volumes via snapshots. The original volume must be encrypted to achieve encrypted data via snapshots. New EBS can be created from the snapshots when needed.

- There are 2 types of EBS volume - SSD and HDD. SSD is useful for small blocks of data like databases and as boot volumes for EC2 instances. HDD is useful for large blocks of data and high rates of throughputs like big data or log processing but cannot be used as boot volumes.

- AWS Data Lifecycle Manager (DLM) is meant to schedule and manage the creation and deletion of EBS snapshots to prevent too much storage cost. This eliminates the need for cron jobs to delete EBS volume snapshots when they are no longer needed. AWS DLM relies on tagging your resources. AWS works greatly with AWS CloudWatch events and AWS CloudTrail for automated backup of EC2 instances.

- There are four types of AWS FSx. They are Amazon FSx for Windows Server, Amazon FSx for Lustre, Amazon FSx for Open ZFS, and Amazon FSX for NetApp ONTAP. Each FSx solution is designed for a different application.

- Amazon FSx for Windows Server pricing is based on capacity, throughput, or backups. Data deduplication (storing duplicate files or portions of files once), a free service provided by Amazon FSx for Windows Server helps save storage costs up to 80%. However, its throughput cost could be much quite expensive.

- Amazon FSx for Lustre does not have any associated throughput cost, only storage capacity is charged per month and it is easier to set up.

- AWS Backup is a centralised view of backups on AWS based using the specified backup policies/plans. AWS Backup works with the AWS Gateway service to back up on-premise data into AWS. It is possible to use lifecycle rules to transition from warm to cold storage options to optimise cost but with an increased retrieval period. It is important to consider the pricing options for both backup storage and restoration.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
