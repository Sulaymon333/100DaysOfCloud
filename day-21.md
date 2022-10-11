# Day 21 of #100daysofcloud

### I started working on Databases in AWS - AWS RDS overview

The general purpose SSD storage is a cost-effective solution with single-digit milliseconds latency for a wide range of cases. For the primary data SSD, there is a minimum of 20GiB and a maximum of 64TiB (SQL serve is 16TiB).

Provisioned IOPS (SSD) storage is applicable for workloads with high I/O. The IOPS has a minimum of 8,000 and a maximum of 80,000 (SQL server is 40,000). For the primary data SSD, there is a minimum of 100GiB and a maximum of 64TiB (SQL serve is 16TiB)
Scaling of Aurora database storage happens automatically as required and no need to configure storage autoscaling options.
For compute autoscaling on AWS RDS, there are both vertical and horizontal scaling options. The autoscaling can be applied immediately or on a scheduled basis.

Horizontal scaling is useful for creating a read replica to enhance the performance of the primary instance. A snapshot can be created from the primary instance or secondary instance if Multi-AZ is enabled and the snapshot created can be used to create the read replica that accepts only read traffic for the database. There is an asynchronous link between the primary and read replica instance.

Backup can be enabled on AWS RDS in case of failure with a retention period of 0–35 days. The backup will be deleted automatically after the retention period expires. Manual backups are also possible but the backups must be manually removed.
Backtrack is another important feature that can be enabled on AWS RDS. AWS RDS can restore data up to the last 72 hours.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
