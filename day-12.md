# Day 12 of #100daysofcloud

### I continued studying AWS storage services for my AWS SAA-C03 certification.

- I continued with AWS storage class options. The storage classes are S3 Standard, S3 Intelligent Tiering, S3 Standard Infrequent Access, S3 One Zone Infrequent Access, S3 Glacier, and S3 Glacier Deep Archive.

- S3 standard is the general purpose option with low latency, high throughput, high durability (99.99%), availability of Eleven 9s, encryption of data at rest and in transit and it has lifecycle rules for automated management of storage across different storage classes.

- S3 Intelligent Tiering (S3 INT) is ideal for an unknown pattern of data access in the S3 bucket. S3 INT will automatically move data between two tiers - frequent and infrequent access based on the data access pattern. It also differs from the S3 Standard in the sense that it has only 99.9% availability.

- S3 Standard Infrequent Access (S3 S-IA) is useful for data that are not accessed frequently. It has all the features of S3 Standard but is cheaper.

- S3 One Zone Infrequent Acces (S3 Z-IA) is similar to S3 S-IA but is only available in a single zone and has a lower availability of 99.5%.

- S3 Glacier shines when you want to cut the cost of long-term archival data. Although it comes with a demerit of not being able to access data in this class (without extra cost) as fast as the Standard S3 classes already highlighted.

- A Couple of retrieval options for S3 Glacier are - expedited (< 250MB in 5 minutes, most expensive), standard (any size in 3-5 hrs) and bulk (PB size in 5-12 hrs, cheapest)

- S3 Deep Archive (S3 G_DA) - is similar to S3 Glacier but it has a minimum data retrieval of 12 hours or less. it is the cheapest, and ideal for very long-term storage for legal requirements.

- Server-access logging is useful for capturing requests made to S3 buckets (source buckets) and their objects for compliance requirements, incident analysis, and security needs. We need another target bucket for this to work otherwise there will be an infinite loop. Both source and target buckets must be in the same region. Log Delivery group in the ACL is granted both read and write permissions automatically to the target bucket

- Hosting a website with an S3 bucket implies we have a region-specific endpoint which means the bucket and its content must be public, with no support for HTTPS, and no support for requester pays.

- I learned that Transfer Acceleration is used to speed up a long-distance S3 data transfer across AWS regions/remote clients using CloudFront. CloudFront uses edge location to achieve such high speed. There is a cost for both in-and-out S3 data transfer. The Bucket name for transfer acceleration must be DNS compliant.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
