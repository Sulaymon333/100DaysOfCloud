# Day 19 of #100daysofcloud

### I concluded work on AWS Storage services with a focus on AWS Snow family and AWS DataSync.

- AWS Snowball (up to 80TB of storage + EC2 instances) is a larger, non-portable device with more storage and computing power. It can be aggregated into clusters of 5-10 devices via rack mount. It does not support a battery pack. The AWS Snowball storage optimised option is used for data migration and transfer compatible with EBS volume and S3 storage. The AWS Snowball compute optimised option is used for intensive computing workloads in edge locations. It has a 43TB HDD compatible with EBS volume and S3 storage. The AWS Snowball compute optimised with GPU is used for graphic-intensive workloads like AI, HPC, and graphic acceleration. AWS Snowball can support up to 100GBit transfer speed via edge data transfer. AWS Snowball is HIPAA compliant as well.

- AWS Snowmobile (up to 100PB) - is used for transferring a very large amount of data into AWS Cloud using a truck. For example, transferring an entire Data Center into AWS Cloud in a secure and cost-efficient manner. Multiple Snowmobile devices can be used together.

- AWS DataSync is used to securely transfer data from on-premise to the AWS cloud. It is equally used to transfer data between AWS storage services. AWS DataSync works with AWS S3, AWS Snowcone, AWS EFS, AWS FSx for Windows File Transfer, NFS share, self-managed object storage and Server Message Block shares. It also supports VPC endpoints for low latency and high bandwidth. It supports up to 10Gbps transfer speed between on-premise and AWS Cloud. It supports both encryption (in transit and at rest via TLS protocol) and data validation. The pricing is based on per Gigabyte of data transferred.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
