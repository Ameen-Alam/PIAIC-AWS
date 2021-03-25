### AWS S3 ACL public-read-write: security concern

Amazon S3 Predefined Groups

Amazon S3 has a set of predefined groups. When granting account access to a group, you specify one of our URIs instead of a canonical user ID. We provide the following predefined groups:

Authenticated Users group – Represented by http://acs.amazonaws.com/groups/global/AuthenticatedUsers. This group represents all AWS accounts. Access permission to this group allows any AWS account to access the resource. However, all requests must be signed (authenticated).

All Users group – Represented by http://acs.amazonaws.com/groups/global/AllUsers. Access permission to this group allows anyone to access the resource. The requests can be signed (authenticated) or unsigned (anonymous). Unsigned requests omit the Authentication header in the request.

Log Delivery group – Represented by http://acs.amazonaws.com/groups/s3/LogDelivery. WRITE permission on a bucket enables this group to write server access logs (see Server Access Logging) to the bucket.

With ACL, you just can share your S3 bucket with other AWS Accounts. Who without logged in AWS account, they cannot access your bucket.

If you want both AWS Account and non-AWS Account can access you S3 bucket, you must define S3 Bucket Policy. For example:

 `<code>`

 `{`

 `"Version": "2008-10-17",`

 `"Statement": [`

 `{`

 `"Sid": "AllowPublicRead",`

 `"Effect": "Allow",`

 `"Principal": {`

 `                "AWS": "*"`

 `},`

 `"Action": "s3:GetObject",`

 ` "Resource": "arn:aws:s3:::S3-Bucket-name/*"`

 ` }`

 `]`

 `}`



Look at this document: http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html