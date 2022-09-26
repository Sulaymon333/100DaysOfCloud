# Day 13 of #100daysofcloud

### I continued studying AWS storage services for my AWS SAA-C03 certification and completed important aspects of AWS S3.

- I continued with AWS storage Service. I used S3 for static web hosting without server-side scripting. The bucket has a region-specific endpoint that can be redirected to a custom domain (using AWS Route 53 or other DNS registrar) or another target bucket, the bucket and its contents must be public and the bucket policy updated for public access of bucket objects, with no support for HTTPS, and no support for requester pays.

- Using AWS Cloudfront with S3 static hosting, it is possible to achieve a highly available website with low latency using edge locations.

- I investigated object Lock for AWS S3 budgets. This feature is useful to meet regulatory compliance and it follows the WORM (Write Once Read Many) model. With object Lock, data can be protected from being deleted for a certain retention period. It is only possible to apply object lock while creating an S3 bucket. Versioning must be enabled as well. There are 2 retention modes for object lock.

  - Governance mode - this can be overridden during the retention period with adequate privileges
  - compliance modes - this cannot be overridden at any time during the retention period.

- Cross-Origin Resource Sharing (CORS) occurs when a website can request resources from other websites with different domains outside its own. This is useful for cross-resource sharing between a client-side web application and S3 objects for example. This can be implemented using the preflight request in the Access-Control-Request-Headers header in the CORSRule.

- I learned that S3 Policies and permissions ensure that only authorised entities have access to the bucket and its contents. There are two policy options, identity-based and resource-based.

  - Identity-based - this policy is associated with an identity and not a resource. So, no need to specify the principal but requires that the resource (bucket name for example) is defined in the policy which can then be associated with a user.
  - Resource-based - this policy is associated with the resource and not an identity. This is achieved using Access Control Lists and Bucket Policies. There is a specification of the principal. The Bucket policy (JSON format) is directly attached to the bucket.

- IAM policies for buckets are useful for centralised management of access from one service (IAM). One IAM policy can be attached to multiple buckets. Size can be a maximum of 2kb for users, 5kb for groups and 10kb for roles.

- Bucket policies can be useful for maintaining security policies within S3 alone. And for granting cross-account access without using IAM roles. Size can be up to 20kb

- It is very important to pay special attention to bucket security. We can use the four options provided by AWS to block bucket access based on our choice.

- The "block all public access" when checked on a bucket overrides the bucket ACL.

#aws #awscertification #cloudcomputing #cloud #publiccloud #hyperscaler #terraform #iac #linux #learninpublic
