# Day 11 of #100daysofcloud

### I started studying AWS storage services for my AWS SAA-C03 certification. I recovered from horrible flu :(

- I learned that some of the most important AWS storage services are AWS S3, AWS EFS, AWS FSx, AWS EBS, ASW Snow Family, AWS Storage Gateway, and AWS DataSync.

- I learned the main aim of varying options of AWS storage services is to match on-prem storage options such as Storage area Network (SAN), Disk Attached Storage (DAS), Network Attached Storage (NAS), and Tape Backup and provide efficient storage services for customers

- I learned there are three categories of storage services provided by AWS - Block (similar to DAS), File (similar to NAS), and Object

- I learned that AWS S3 (Simple Storage Service) a regional service, is the most used AWS storage service, it is well integrated with many AWS services, and it is highly available, highly durable, cost-effective, and highly scalable with unlimited storage space. Although there is a 5TB max for the largest file size.

- Each bucket name in S3 must be globally unique. Max bucket per account has a soft limit of 100 with a possibility to increase to 1000.

- I learned about versioning of bucket in S3. It is possible for a bucket to be in 3 states - unversioned (default), versioned, and suspended. It is not possible to disable versioning on a bucket after versioning has been enabled. It is only possible to suspend it. Bucket versioning can increase storage costs. Versioning is not recommended on constantly changing files.

- I learned that object-level logging can be enabled on S3 buckets in conjunction with the AWS cloud trail to capture the data events (read/write) using our S3 buckets.

- I learned about tags and how they can be used as S3 cost allocation tags for different business units and cost centers using AWS services within our accounts. Cost Allocation tags with AWS billing must be enabled first.

- I learned about Requester pays features on S3 buckets. It requires authenticated access to the bucket in order for AWS to know whom to bill while the requester makes the request API calls to the bucket. The bucket owner will still pay for the storage cost of the bucket.

- I recovered from the horrible flu that has been disturbing me for the past few days :)

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
