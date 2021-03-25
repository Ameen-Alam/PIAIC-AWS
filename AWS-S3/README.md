# Amazon S3

Amazon Simple Storage Service is storage for the Internet. It is designed to make web-scale computing easier for developers. Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web.

https://aws.amazon.com/s3/


### Assignment 01
    
    Host static website using AWS S3 and Route53

``` e.g use aws cli and aws console ```

#### Assignment 01 (a)

- Create IAM User e.g role S3 full access
- Create S3 bucket
- Storage class: S3 Standard
- Put two objects via aws cli e.g image1.jpg image2.jpg
- Get presigned URL

#### Assignment 01 (b)

- Enable static site
- Open public access e.g assign putObject role via ACL
- Upload index.html, error.html
- Get public url

#### Assignment 01 (c)

- Enable version
- Enable encryption
- Add tag

#### Assignment 01 (d)

- Add Route53 zone
- Create alias with s3 static site

#### Assignment 01 (e)

- Create another s3 bucket upload a image
- Access a image in index.html file - using CORS

#### Assignment 01 (f)

- Read S3 Service Level Agreement
- Create Monthly Cost Report.

#### Assignment 01 (g)

 - NodeJS-File-Upload-AWS-S3-Bucket
 
 https://github.com/Ameen-Alam/NodeJS-File-Upload-AWS-S3-Bucket



-----------------------------------------------

#### Commands:

$ aws configure

$ aws s3api put-object --bucket myawsbucketnodeapp --key dir-1/my_images --body mydownload.jpeg

$ aws s3api get-object --bucket text-content --key dir/my_images.tar.bz2 my_images.tar.bz2

``` Finding the canonical user ID for your AWS account ```
$ aws s3api list-buckets --query Owner.ID --output text

$ aws organizations describe-account --account-id 444444444444

$ aws iam create-role --role-name Test-UserAccess-Role --assume-role-policy-document file://C:\policies\trustpolicyforacct123456789012.json

$ aws iam attach-role-policy --role-name Test-UserAccess-Role --policy-arn arn:aws:iam::123456789012:role/PolicyForRole


-----------------------------------------------


### Documentations:

0. [AWS Certified Developer Associate Syllabus]()

1. [AWS Security Tips: Understanding Access Controls in Amazon S3](https://redlock.io/blog/aws-security-tips-understanding-access-controls-amazon-s3)

2. [put-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/put-object.html)

3. [get-object](https://docs.aws.amazon.com/cli/latest/reference/s3api/get-object.html)

4. [Amazon S3 Service Level Agreement](https://aws.amazon.com/s3/sla/)

5. [Amazon Web Services Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html)

6. [AWS Pricing Calculator](https://calculator.aws/)

7. [Access control list (ACL) overview](https://docs.aws.amazon.com/AmazonS3/latest/userguide/acl-overview.html)

8. [Amazon S3 Reduced Redundancy Storage](https://aws.amazon.com/s3/reduced-redundancy/)

9. [Amazon S3 storage classes](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html)

10. [Amazon S3 inventory](https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-inventory.html)

11. [S3 Batch Operations: Create a Job](https://www.youtube.com/watch?v=hUv34voEftc)

12. ![AWS-S3-ACL-public-read-write-security-concern](./AWS-S3-ACL-public-read-write-security-concern)

13. [Billing & Cost Management Dashboard](https://console.aws.amazon.com/billing/home)

14. [IAM Tutorial: Delegate access to the billing console](https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_billing.html)

15. [Support Center](https://console.aws.amazon.com/support/home)

16. [server access logging](https://docs.aws.amazon.com/AmazonS3/latest/userguide/ServerLogs.html)

17. [AWS IP address ranges](https://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html)

18. [Deleting Amazon S3 log files](https://docs.aws.amazon.com/AmazonS3/latest/userguide/deleting-log-files-lifecycle.html)

19. [Managing S3 Object lifecycle](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html)

20. [PutBucketLifecycleConfiguration](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html)

20. [DeleteBucketLifecycle](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketLifecycle.html)

20. [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/)

20. [Support plans](https://console.aws.amazon.com/support/plans/home)

20. [Amazon S3 Security and Access Management](https://aws.amazon.com/s3/security/)

20. [Storage Lens](https://aws.amazon.com/blogs/aws/s3-storage-lens/)

