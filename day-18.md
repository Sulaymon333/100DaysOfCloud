# Day 18 of #100daysofcloud

### I concluded work on AWS Storage services with a focus on AWS Storage Gateway, AWS Snow family, and AWS DataSync.

- AWS Storage Gateway (software or Hardware) is used to integrate on-premise data storage (NAS, DAS, SAN) with AWS S3 and AWS Glacier. It helps to scale customer storage needs securely with less cost

- AWS Storage Gateway comes in different configurations such as File, Volume, or Tape Gateway.

- File Gateway is used to securely store on-premise files using AWS S3. Its cost (per GB) is based on S3 pricing (for both request and storage costs) with a maximum request pricing of $125/month (the first 100GB is free). File Gateway has an on-premise cache to reduce latency.

- Volume Gateway can be used in either stored volume or cached volume gateways. Stored volume is used to back up local storage volumes to AWS S3 in form of EBS snapshots while keeping the local copy of data on-premise to reduce latency. Stored volume cost is based on AWS EBS snapshots' pricing. Cached volume gateways act as on-premise buffers for data primarily stored on AWS S3. Therefore Cached volume gateways help to reduce the latency of recently accessed data. Cached volume gateways' monthly cost is based on per GB of data stored. For volume Gateway, the maximum cost per GB for data written to S3 is $125/month (the first 100GB is free).

- Tape Gateway (Virtual Tape Library - VTL) is used to back up on-premise data into the archival AWS Glacier storage option. Retrieval time must be taken into consideration when choosing this solution. The maximum monthly cost per GB for data written to S3 by the Tape Gateway is $125.00 (the first 100GB is free).

- The Snow family consists of physical hardware devices that are used to transfer a large amount (minimum of 8TB) of data from on-premise into Amazon Cloud and vice-versa at the edge locations. The Snow family comes in three classes - AWS Snowcone, AWS Snowball, and AWS Snowmobile. The AWS Snowball is further divided into AWS Snowball compute optimised, AWS Snowball compute optimised with GPU, and AWS Snowball storage optimised. Both AWS Snowcone and AWS Snowball have automatic data encryption. All data are securely erased after transfer.

- AWS Snowcone (up to 8TB of storage + EC2 instance) is a portable, lightweight, and rugged device that be used with a battery pack and can fit into a standard backpack. It can be used to capture, process and analyse data at the edge locations and then sent back to AWS. It also uses AWS DataSync to transfer data over the standard network to AWS Cloud. AWS Snowcone can support up to 10GBit transfer speed.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
