# Day 20 of #100daysofcloud

### I started working on Databases in AWS - AWS RDS overview

AWS RDS is a managed service for relational database solutions. Users can create, scale, and provision databases while AWS takes care of backing up and patching the underlying OS and database engine.

There are various database engines available on AWS RDS. These are MySQL, MariaDB, Postgres, Oracle, SQL server, and Aurora by AWS.

For memory and processing needs, there are two types of compute instances types available to run AWS RDS databases on. These are General purpose and Memory optimised. Instance types equally have instance sizes based on the number of vCPUs and memory (GiB).

In terms of availability and resilience, there is a Multi-AZ option where a secondary DB can be created in another AZ within the region. There is synchronous connectivity between the primary and secondary instances. The Multi-AZ feature is useful for automatic failover (usually 60–120s) in case of any of the following cases. The failover will occur in any of the following occurs on the primary instance - reboot, instance class modification, AZ failure, host failure, or patching maintenance.

In terms of scaling AWS RDS for both the compute and storage, there is a storage autoscaling option based on AWS EBS storage for MySQL, MariaDB, Postgres, Oracle, and SQL servers. AWS Aurora uses shared cluster storage managed by the service itself and does not use AWS EBS for storage scaling. For database engines that support EBS for storage autoscaling, there are three options to choose from. These are general-purpose SSD storage, provisioned IOPS (SSD) storage, and Magnetic storage (only meant for backward compatibility, it is not recommended by AWS, the general purpose should be used).

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
