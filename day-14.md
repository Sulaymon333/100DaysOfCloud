# Day 14 of #100daysofcloud

### I worked on AWS S3 lifecycle configuration and AWS EFS.

- I investigated the lifecycle configurations for saving costs on AWS S3. The lifecycle configuration is an essential cost-saving tool for data that has a predictable pattern. It is possible to move data between S3 Standard to lower archival storage like S3 Glacier after some time (30 days for example) for data retention requirements and after this time has elapsed the data can be completely deleted to further increase savings. The lifecycle configuration is equally important for cleaning up incomplete multipart uploads.

- Lifecycle configuration is made up of a rule that contains four parts. ID - this is the id of the rule, Filter - to select a specific project/resource, Status - to enable or disable the lifecycle configuration rule, and Actions - the actual changes to the data in the bucket.

- I created a lifecycle configuration rule for an object in my S3 bucket. The rule is meant to move a particular folder in my S3 bucket with a filter (prefix) specified into a low-cost (S3 Flexible Retrieval) storage option from S3 Standard after 30 days and get it deleted after 365 days. This kind of lifecycle configuration rule works well with a known access pattern.

- Lifecycle configuration can only transition objects in a uni-directional manner. From S3 Standard to Archival storage. Minimum storage duration fees and transition costs increase as we go from S3 Standard to Archival storage. Smaller objects can be aggregated into large objects to reduce transition costs.

- Both S3 standard and S3 Intelligent-tiering have no minimum storage duration. S3 Standard-IA and S3 One Zone-IA have a minimum storage duration of 30 days. While S3 Glacier Instant Retrieval and S3 Glacier Flexible Retrieval have a minimum storage duration of 90 days. And S3 Glacier Deep Archive has a minimum storage duration of 180. Any delete or overite of objects before the minimum storage duration cost the same as the entire minimum storage duration mentioned earlier.

- Elastic File System (EFS) is a regional, fully managed, highly available, and optimised service for low latency access and support access by multiple instances at once with high throughput (MB/s). The EFS resources can be accessed by EC2 instances using mount points created in different AZs.

- There are 2 EFS storage classes - Standard (default) and Infrequent Access (IA). The standard class has a standard cost, access, and performance in terms of latency. While the IA class has higher latency at a reduced cost. Although there is a separate read and write cost for IA classes.

- EFS lifecycle management can be used to transition objects (metadata files or < 128K) between the two classes using day options like 14, 30, 60, and 90 days.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
