# AWS SAA-C03 Practice Questions - Part 1

Total Questions: 207

---

## Question 1

**Q:** To use a custom domain name and URL when hosting a static website in a bucket, what two services of AWS are required?

**Options:**
- (A) S3 and DynDNS
- (B) S3 and ELB
- (C) S3 and Route 53
- (D) S3 and ElastiCache
- (E) S3 and Route 53 is the correct answer. S3 is used to store the static website files; however, it would use a URL like bucket_name.s3-website-us-west-1.amazonaws.com. To also use a custom domain name, Route 53, the AWS DNS service, is required. DynDNS is not an AWS service. ELB and ElastiCache will not help to provide a custom DNS name.
- (F) You are implementing an ELB solution. You want to ensure high availability. Where should the resources to which ELB directs be located?
- (G) In one region
- (H) In one Availability Zone
- (I) In different Availability Zones
- (J) In one VPC
- () In different Availability Zones is correct. To ensure high availability, resources should be in more than one Availability Zone. ELB will direct traffic to healthy resources in the various Availability Zones.
- () You have been asked to host a static website in AWS as quickly as possible. What is the simplest solution to use?
- () S3
- () EFS
- () ELB
- () EC2 instance
- () S3 is the correct answer. The simplest solution is to place the website files into an S3 bucket and then enable web sharing on the bucket and associate it with a DNS name. ELB and EFS do not directly provide hosting. An EC2 instance would require instantiating a full instance, configuring the web service on the instance, and then placing the website files into the instance, which is more complex than hosting through an S3 bucket.
- () You have implemented a NACL and notice that return traffic from an internal request is not allowed. Why is this happening?
- () NACLs are stateful
- () NACLs have many bugs in AWS
- () NACLs are stateless
- () NACLs, once implemented, block all inbound traffic regardless of rules
- () NACLs are stateless is the correct answer. Because NACLs are stateless (unlike security groups, which are stateful) they do not automatically allow inbound responses to internally originating requests. All inbound communications must be explicitly allowed by rules.
- () You have been asked to provide a folder-like structure in S3 buckets. How can this be accomplished?
- () Using actual directories
- () Using nested S3 buckets
- **() Using prefixes and delimiters** [CORRECT]

**Answer:**
Correct Answer: **Using prefixes and delimiters**

**Explanation:**
NACLs are stateless is the correct answer. Because NACLs are stateless (unlike security groups, which are stateful) they do not automatically allow inbound responses to internally originating requests. All inbound communications must be explicitly allowed by rules.

---

## Question 2

**Q:** You are implementing an ELB solution. You want to ensure high availability. Where should the resources to which ELB directs be located?

**Options:**
- (A) In one region
- (B) In one Availability Zone
- (C) In different Availability Zones
- (D) In one VPC
- (E) In different Availability Zones is correct. To ensure high availability, resources should be in more than one Availability Zone. ELB will direct traffic to healthy resources in the various Availability Zones.
- (F) You have been asked to host a static website in AWS as quickly as possible. What is the simplest solution to use?
- (G) S3
- (H) EFS
- (I) ELB
- (J) EC2 instance
- () S3 is the correct answer. The simplest solution is to place the website files into an S3 bucket and then enable web sharing on the bucket and associate it with a DNS name. ELB and EFS do not directly provide hosting. An EC2 instance would require instantiating a full instance, configuring the web service on the instance, and then placing the website files into the instance, which is more complex than hosting through an S3 bucket.
- () You have implemented a NACL and notice that return traffic from an internal request is not allowed. Why is this happening?
- () NACLs are stateful
- () NACLs have many bugs in AWS
- () NACLs are stateless
- () NACLs, once implemented, block all inbound traffic regardless of rules
- () NACLs are stateless is the correct answer. Because NACLs are stateless (unlike security groups, which are stateful) they do not automatically allow inbound responses to internally originating requests. All inbound communications must be explicitly allowed by rules.
- () You have been asked to provide a folder-like structure in S3 buckets. How can this be accomplished?
- () Using actual directories
- () Using nested S3 buckets
- () Using prefixes and delimiters
- () Using actual folders
- () . Nested S3 buckets are not supported.
- () Where are AWS Cost and Usage Reports stored?
- () EBS volumes
- **() S3 bucket** [CORRECT]

**Answer:**
Correct Answer: **S3 bucket**

**Explanation:**
. Nested S3 buckets are not supported.

---

## Question 3

**Q:** You have been asked to host a static website in AWS as quickly as possible. What is the simplest solution to use?

**Options:**
- (A) S3
- (B) EFS
- (C) ELB
- (D) EC2 instance
- (E) S3 is the correct answer. The simplest solution is to place the website files into an S3 bucket and then enable web sharing on the bucket and associate it with a DNS name. ELB and EFS do not directly provide hosting. An EC2 instance would require instantiating a full instance, configuring the web service on the instance, and then placing the website files into the instance, which is more complex than hosting through an S3 bucket.
- (F) You have implemented a NACL and notice that return traffic from an internal request is not allowed. Why is this happening?
- (G) NACLs are stateful
- (H) NACLs have many bugs in AWS
- (I) NACLs are stateless
- (J) NACLs, once implemented, block all inbound traffic regardless of rules
- () NACLs are stateless is the correct answer. Because NACLs are stateless (unlike security groups, which are stateful) they do not automatically allow inbound responses to internally originating requests. All inbound communications must be explicitly allowed by rules.
- () You have been asked to provide a folder-like structure in S3 buckets. How can this be accomplished?
- () Using actual directories
- () Using nested S3 buckets
- () Using prefixes and delimiters
- () Using actual folders
- () . Nested S3 buckets are not supported.
- () Where are AWS Cost and Usage Reports stored?
- () EBS volumes
- () S3 bucket
- () The are not stored, they are sent via e-mail
- () In unmanaged, no-cost storage
- () S3 bucket is the correct answer. Cost and Usage Reports are generated from Redshift or QuickSight data source and are stored in S3 buckets. The Cost and Usage Reports interface provides an option to create an S3 bucket, appropriately configured, for report storage.
- () What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?
- () CloudWatch
- **() Trusted Advisor** [CORRECT]

**Answer:**
Correct Answer: **Trusted Advisor**

**Explanation:**
S3 bucket is the correct answer. Cost and Usage Reports are generated from Redshift or QuickSight data source and are stored in S3 buckets. The Cost and Usage Reports interface provides an option to create an S3 bucket, appropriately configured, for report storage.

---

## Question 4

**Q:** You have implemented a NACL and notice that return traffic from an internal request is not allowed. Why is this happening?

**Options:**
- (A) NACLs are stateful
- (B) NACLs have many bugs in AWS
- (C) NACLs are stateless
- (D) NACLs, once implemented, block all inbound traffic regardless of rules
- (E) NACLs are stateless is the correct answer. Because NACLs are stateless (unlike security groups, which are stateful) they do not automatically allow inbound responses to internally originating requests. All inbound communications must be explicitly allowed by rules.
- (F) You have been asked to provide a folder-like structure in S3 buckets. How can this be accomplished?
- (G) Using actual directories
- (H) Using nested S3 buckets
- (I) Using prefixes and delimiters
- (J) Using actual folders
- () . Nested S3 buckets are not supported.
- () Where are AWS Cost and Usage Reports stored?
- () EBS volumes
- () S3 bucket
- () The are not stored, they are sent via e-mail
- () In unmanaged, no-cost storage
- () S3 bucket is the correct answer. Cost and Usage Reports are generated from Redshift or QuickSight data source and are stored in S3 buckets. The Cost and Usage Reports interface provides an option to create an S3 bucket, appropriately configured, for report storage.
- () What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?
- () CloudWatch
- () Trusted Advisor
- () CloudFront
- () RDS
- () Trusted Advisor is the correct answer. AWS Trusted Advisor can provide security-related suggestions to improve the security of your AWS deployment. CloudWatch, CloudFront and RDS do not provide such advice.
- () What two caching engines are supported by ElastiCache?
- **() Redis and memcached** [CORRECT]
- () Ready-cache and opencache

**Answer:**
Correct Answer: **Redis and memcached**

**Explanation:**
Trusted Advisor is the correct answer. AWS Trusted Advisor can provide security-related suggestions to improve the security of your AWS deployment. CloudWatch, CloudFront and RDS do not provide such advice.

---

## Question 5

**Q:** You have been asked to provide a folder-like structure in S3 buckets. How can this be accomplished?

**Options:**
- (A) Using actual directories
- (B) Using nested S3 buckets
- (C) Using prefixes and delimiters
- (D) Using actual folders
- (E) . Nested S3 buckets are not supported.
- (F) Where are AWS Cost and Usage Reports stored?
- (G) EBS volumes
- (H) S3 bucket
- (I) The are not stored, they are sent via e-mail
- (J) In unmanaged, no-cost storage
- () S3 bucket is the correct answer. Cost and Usage Reports are generated from Redshift or QuickSight data source and are stored in S3 buckets. The Cost and Usage Reports interface provides an option to create an S3 bucket, appropriately configured, for report storage.
- () What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?
- () CloudWatch
- () Trusted Advisor
- () CloudFront
- () RDS
- () Trusted Advisor is the correct answer. AWS Trusted Advisor can provide security-related suggestions to improve the security of your AWS deployment. CloudWatch, CloudFront and RDS do not provide such advice.
- () What two caching engines are supported by ElastiCache?
- **() Redis and memcached** [CORRECT]
- () Ready-cache and opencache
- () Opencache and memcached
- () Redis and opencache
- () Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.
- () Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70%.
- () Correct selection
- () Use ElastiCache to cache the most commonly accessed DB queries.

**Answer:**
Correct Answer: **Redis and memcached**

**Explanation:**
Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.

---

## Question 6

**Q:** Where are AWS Cost and Usage Reports stored?

**Options:**
- (A) EBS volumes
- (B) S3 bucket
- (C) The are not stored, they are sent via e-mail
- (D) In unmanaged, no-cost storage
- (E) S3 bucket is the correct answer. Cost and Usage Reports are generated from Redshift or QuickSight data source and are stored in S3 buckets. The Cost and Usage Reports interface provides an option to create an S3 bucket, appropriately configured, for report storage.
- (F) What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?
- (G) CloudWatch
- (H) Trusted Advisor
- (I) CloudFront
- (J) RDS
- () Trusted Advisor is the correct answer. AWS Trusted Advisor can provide security-related suggestions to improve the security of your AWS deployment. CloudWatch, CloudFront and RDS do not provide such advice.
- () What two caching engines are supported by ElastiCache?
- **() Redis and memcached** [CORRECT]
- () Ready-cache and opencache
- () Opencache and memcached
- () Redis and opencache
- () Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.
- () Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70%.
- () Correct selection
- () Use ElastiCache to cache the most commonly accessed DB queries.
- () Upgrade the RDS instance to a higher memory instance.
- () Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website.
- () Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53.
- () Correct Answers:
- () Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website, Use ElastiCache to cache the most commonly accessed DB queries, and Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53 are correct.
- () Your RDS instance is already the largest currently offered by AWS, so you cannot upgrade this further. Changing your Auto Scaling policies will not help improve performance times, as it is much more likely that the performance issue is with the database back end rather than the front end. 
- () Incorrect Answer:
- () Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70% is incorrect because scaling when CPU utilization is 50% is going to add more cost and won’t fully leverage the resource of the existing server. E is incorrect because there is no data point that shows the issue is memory related.

**Answer:**
Correct Answer: **Redis and memcached**

**Explanation:**
Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.

---

## Question 7

**Q:** What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?

**Options:**
- (A) CloudWatch
- (B) Trusted Advisor
- (C) CloudFront
- (D) RDS
- (E) Trusted Advisor is the correct answer. AWS Trusted Advisor can provide security-related suggestions to improve the security of your AWS deployment. CloudWatch, CloudFront and RDS do not provide such advice.
- (F) What two caching engines are supported by ElastiCache?
- **(G) Redis and memcached** [CORRECT]
- (H) Ready-cache and opencache
- (I) Opencache and memcached
- (J) Redis and opencache
- () Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.
- () Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70%.
- () Correct selection
- () Use ElastiCache to cache the most commonly accessed DB queries.
- () Upgrade the RDS instance to a higher memory instance.
- () Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website.
- () Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53.
- () Correct Answers:
- () Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website, Use ElastiCache to cache the most commonly accessed DB queries, and Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53 are correct.
- () Your RDS instance is already the largest currently offered by AWS, so you cannot upgrade this further. Changing your Auto Scaling policies will not help improve performance times, as it is much more likely that the performance issue is with the database back end rather than the front end. 
- () Incorrect Answer:
- () Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70% is incorrect because scaling when CPU utilization is 50% is going to add more cost and won’t fully leverage the resource of the existing server. E is incorrect because there is no data point that shows the issue is memory related.

**Answer:**
Correct Answer: **Redis and memcached**

**Explanation:**
Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.

---

## Question 8

**Q:** What two caching engines are supported by ElastiCache?

**Options:**
- **(A) Redis and memcached** [CORRECT]
- (B) Ready-cache and opencache
- (C) Opencache and memcached
- (D) Redis and opencache
- (E) Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.
- (F) Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70%.
- (G) Correct selection
- (H) Use ElastiCache to cache the most commonly accessed DB queries.
- (I) Upgrade the RDS instance to a higher memory instance.
- (J) Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website.
- () Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53.
- () Correct Answers:
- () Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website, Use ElastiCache to cache the most commonly accessed DB queries, and Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53 are correct.
- () Your RDS instance is already the largest currently offered by AWS, so you cannot upgrade this further. Changing your Auto Scaling policies will not help improve performance times, as it is much more likely that the performance issue is with the database back end rather than the front end. 
- () Incorrect Answer:
- () Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70% is incorrect because scaling when CPU utilization is 50% is going to add more cost and won’t fully leverage the resource of the existing server. E is incorrect because there is no data point that shows the issue is memory related.

**Answer:**
Correct Answer: **Redis and memcached**

**Explanation:**
Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.

---

## Question 9

**Q:** You are running a media-rich website with a global audience in US-EAST-1 for a customer in the publishing industry. The website updates every 20 minutes. The web-tier of the site sits on three EC2 instances inside an Auto Scaling group. The Auto Scaling group is configured to scale when CPU utilization of the instances is greater than 70%. The Auto Scaling group sits behind an Elastic Load Balancer, and your static content lives in S3 and is distributed globally by CloudFront. Your RDS database is an db.m5.4xlarge instance. CloudWatch metrics show that your RDS instance usually has around 2GB of memory free, and an average CPU utilization of 75%. Currently, it is taking your users in Japan and Australia approximately 3 to 5 seconds to load your website, and you have been asked to help reduce these load times. How might you improve your page load times? (Choose three.)

**Options:**
- **(A) Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70%.** [CORRECT]
- (B) Correct selection
- (C) Use ElastiCache to cache the most commonly accessed DB queries.
- (D) Upgrade the RDS instance to a higher memory instance.
- (E) Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website.
- (F) Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53.
- (G) Correct Answers:
- (H) Set up CloudFront with dynamic content support to enable the caching of reusable content from the media-rich website, Use ElastiCache to cache the most commonly accessed DB queries, and Set up a read replica of your production environment in the Asia Pacific region and configure latency-based routing on Route 53 are correct.
- (I) Your RDS instance is already the largest currently offered by AWS, so you cannot upgrade this further. Changing your Auto Scaling policies will not help improve performance times, as it is much more likely that the performance issue is with the database back end rather than the front end. 
- (J) Incorrect Answer:
- () Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70% is incorrect because scaling when CPU utilization is 50% is going to add more cost and won’t fully leverage the resource of the existing server. E is incorrect because there is no data point that shows the issue is memory related.

**Answer:**
Correct Answer: **Change your Auto Scaling group so that it will scale when CPU utilization is only 50%, rather than 70%.**

---

## Question 10

**Q:** In addition to inbound and outbound rules, what type of rule does a security group allow?

**Options:**
- (A) Filtered rules
- (B) Unfiltered rules
- (C) Allow rules
- (D) Deny rules
- (E) Allow rules is the correct answer. Security groups only have allow rules. Anything not explicitly allowed is denied. No such rules as filtered and unfiltered exist. Allow rules can be inbound or outbound or both.
- (F) When should you use a dedicated host for an EC2 instance?
- (G) When you require a license based on the number of users
- **(H) When you require a license to be locked to the hardware** [CORRECT]
- (I) When you require a license file associated with an application installation
- (J) When you will use more than one application on the instance
- () When you require a license to be locked to the hardware is correct. A dedicated host provides a solution to specific licensing scenarios that require the license be locked to hardware, the number of CPU sockets, etc. Licenses based on the number of users or license files can work on any tenancy model. Using more than one application is possible with any tenancy model as well.

**Answer:**
Correct Answer: **When you require a license to be locked to the hardware**

**Explanation:**
When you require a license to be locked to the hardware is correct. A dedicated host provides a solution to specific licensing scenarios that require the license be locked to hardware, the number of CPU sockets, etc. Licenses based on the number of users or license files can work on any tenancy model. Using more than one application is possible with any tenancy model as well.

---

## Question 11

**Q:** When should you use a dedicated host for an EC2 instance?

**Options:**
- (A) When you require a license based on the number of users
- **(B) When you require a license to be locked to the hardware** [CORRECT]
- (C) When you require a license file associated with an application installation
- (D) When you will use more than one application on the instance
- (E) When you require a license to be locked to the hardware is correct. A dedicated host provides a solution to specific licensing scenarios that require the license be locked to hardware, the number of CPU sockets, etc. Licenses based on the number of users or license files can work on any tenancy model. Using more than one application is possible with any tenancy model as well.

**Answer:**
Correct Answer: **When you require a license to be locked to the hardware**

**Explanation:**
When you require a license to be locked to the hardware is correct. A dedicated host provides a solution to specific licensing scenarios that require the license be locked to hardware, the number of CPU sockets, etc. Licenses based on the number of users or license files can work on any tenancy model. Using more than one application is possible with any tenancy model as well.

---

## Question 12

**Q:** In the event of loss of access to an Availability Zone for any reason, which S3 storage class does not provide resiliency?

**Options:**
- (A) S3 Standard-Infrequent Access
- (B) S3 Standard
- (C) S3 Glacier
- **(D) S3 One Zone-Infrequent Access** [CORRECT]
- (E) S3 One Zone-Infrequent Access is the correct answer. S3 One Zone-IA stores the objects only in one zone and if that Availability Zone is lost or access is blocked, the objects cannot be accessed. S3 Standard, Standard-IA and Glacier store objects in multiple AZs or through other archival methods providing recoverability.

**Answer:**
Correct Answer: **S3 One Zone-Infrequent Access**

**Explanation:**
S3 One Zone-Infrequent Access is the correct answer. S3 One Zone-IA stores the objects only in one zone and if that Availability Zone is lost or access is blocked, the objects cannot be accessed. S3 Standard, Standard-IA and Glacier store objects in multiple AZs or through other archival methods providing recoverability.

---

## Question 13

**Q:** When you’re editing permissions (policies and ACLs), to whom does the concept of the “owner” refer?

**Options:**
- (A) There is no special concept of “owner” in AWS.
- (B) The owner is the IAM user who created the object via the GUI, CLI, or API.
- (C) “Owner” refers to the identity and e-mail address used to create the AWS account.
- (D) The owner is IAM role used to create the object via the GUI, CLI, or API.
- (E) “Owner” refers to the identity and e-mail address used to create the AWS account is correct. In AWS, the context of the owner of the account is root, which needs to be logged in using the username/password combination. 
- (F) Incorrect Answers:
- (G) The owner is the IAM user who created the object via the GUI, CLI, or API and The owner is IAM role used to create the object via the GUI, CLI, or API are incorrect because neither of these is the correct explanations of the owner.
- (H) There is no special concept of “owner” in AWS is incorrect because there is a concept of “owner” in AWS.
- (I) You are running a Mongo database that requires access to tens of thousands of low-latency IOPS. Which of the following EC2 instance families would best suit your needs?
- (J) Cluster GPU instances
- () High I/O instances
- () Dense storage instances
- () Memory-optimized instances
- () High I/O instances is correct. High I/O instances use SSD-based local instance storage to deliver very high, low-latency I/O capacity to applications, and they are optimized for applications that require tens of thousands of IOPS. 
- () Memory-optimized instances, Dense storage instances, and Cluster GPU instances are incorrect because low latency is the key, and you need to solve the I/O problem. High memory, dense storage, or a cluster of GPU instances won’t help here.
- () What can be used to aggregate several AWS accounts for centralized management and billing tracking?
- () AWS Budget
- () AWS Organizations
- () AWS Trusted Advisor
- () AWS Cost and Reporting
- () AWS Organizations is correct. AWS Organizations are collections of AWS accounts placed under centralized management. Trusted Advisor provides suggestions for improved performance, security, and cost management. AWS Cost and Reporting and AWS Budget are used strictly for cost management and reporting.
- () You have a small database workload with infrequent I/O. These databases are mainly used as ad hoc databases for noncritical testing purposes. Which storage medium would be the most cost-effective way to meet these requirements?
- () Amazon RDS Provisioned IOPS (SSD) Storage
- **() Amazon RDS Magnetic Storage** [CORRECT]
- () Amazon RDS Cold Storage
- () Amazon RDS General Purpose (SSD) Storage
- () Amazon RDS Magnetic Storage is the correct answer. Amazon RDS Magnetic Storage would be the most suitable. In this case, you need to consider the lower cost since these are noncritical databases.
- () Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are incorrect because Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are going to add more cost.
- () Amazon RDS Cold Storage is incorrect because RDS Cold Storage doesn’t exist.

**Answer:**
Correct Answer: **Amazon RDS Magnetic Storage**

**Explanation:**
Amazon RDS Magnetic Storage is the correct answer. Amazon RDS Magnetic Storage would be the most suitable. In this case, you need to consider the lower cost since these are noncritical databases.

---

## Question 14

**Q:** You are running a Mongo database that requires access to tens of thousands of low-latency IOPS. Which of the following EC2 instance families would best suit your needs?

**Options:**
- (A) Cluster GPU instances
- (B) High I/O instances
- (C) Dense storage instances
- (D) Memory-optimized instances
- (E) High I/O instances is correct. High I/O instances use SSD-based local instance storage to deliver very high, low-latency I/O capacity to applications, and they are optimized for applications that require tens of thousands of IOPS. 
- (F) Incorrect Answers:
- (G) Memory-optimized instances, Dense storage instances, and Cluster GPU instances are incorrect because low latency is the key, and you need to solve the I/O problem. High memory, dense storage, or a cluster of GPU instances won’t help here.
- (H) What can be used to aggregate several AWS accounts for centralized management and billing tracking?
- (I) AWS Budget
- (J) AWS Organizations
- () AWS Trusted Advisor
- () AWS Cost and Reporting
- () AWS Organizations is correct. AWS Organizations are collections of AWS accounts placed under centralized management. Trusted Advisor provides suggestions for improved performance, security, and cost management. AWS Cost and Reporting and AWS Budget are used strictly for cost management and reporting.
- () You have a small database workload with infrequent I/O. These databases are mainly used as ad hoc databases for noncritical testing purposes. Which storage medium would be the most cost-effective way to meet these requirements?
- () Amazon RDS Provisioned IOPS (SSD) Storage
- () Amazon RDS Magnetic Storage
- () Amazon RDS Cold Storage
- () Amazon RDS General Purpose (SSD) Storage
- () Amazon RDS Magnetic Storage is the correct answer. Amazon RDS Magnetic Storage would be the most suitable. In this case, you need to consider the lower cost since these are noncritical databases.
- () Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are incorrect because Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are going to add more cost.
- () Amazon RDS Cold Storage is incorrect because RDS Cold Storage doesn’t exist.
- () Which one of the following is controlled by a security group attached to an instance?
- () NACLs
- () Database error codes
- **() Inbound traffic** [CORRECT]
- () HTTP error codes
- () Inbound traffic is the correct answer. Security groups control inbound and outbound traffic. They do not control error codes of any kinds or NACLs, which are applied to the subnet and not to instances.
- () You have several Windows and Linux instances within a single subnet in a VPC. You want to ensure that no inbound traffic can reach the Windows instances. What is the best option?

**Answer:**
Correct Answer: **Inbound traffic**

**Explanation:**
Inbound traffic is the correct answer. Security groups control inbound and outbound traffic. They do not control error codes of any kinds or NACLs, which are applied to the subnet and not to instances.

---

## Question 15

**Q:** What can be used to aggregate several AWS accounts for centralized management and billing tracking?

**Options:**
- (A) AWS Budget
- (B) AWS Organizations
- (C) AWS Trusted Advisor
- (D) AWS Cost and Reporting
- (E) AWS Organizations is correct. AWS Organizations are collections of AWS accounts placed under centralized management. Trusted Advisor provides suggestions for improved performance, security, and cost management. AWS Cost and Reporting and AWS Budget are used strictly for cost management and reporting.
- (F) You have a small database workload with infrequent I/O. These databases are mainly used as ad hoc databases for noncritical testing purposes. Which storage medium would be the most cost-effective way to meet these requirements?
- (G) Amazon RDS Provisioned IOPS (SSD) Storage
- (H) Amazon RDS Magnetic Storage
- (I) Amazon RDS Cold Storage
- (J) Amazon RDS General Purpose (SSD) Storage
- () Amazon RDS Magnetic Storage is the correct answer. Amazon RDS Magnetic Storage would be the most suitable. In this case, you need to consider the lower cost since these are noncritical databases.
- () Incorrect Answers:
- () Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are incorrect because Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are going to add more cost.
- () Amazon RDS Cold Storage is incorrect because RDS Cold Storage doesn’t exist.
- () Which one of the following is controlled by a security group attached to an instance?
- () NACLs
- () Database error codes
- () Inbound traffic
- () HTTP error codes
- () Inbound traffic is the correct answer. Security groups control inbound and outbound traffic. They do not control error codes of any kinds or NACLs, which are applied to the subnet and not to instances.
- () You have several Windows and Linux instances within a single subnet in a VPC. You want to ensure that no inbound traffic can reach the Windows instances. What is the best option?
- () Security Groups
- () Linux firewall
- () IAM
- () Security Groups is the correct answer. The best option, in this case, is security groups for each Windows instance network interface. If this were controlled with NACLs, it would also prevent access to the Linux instances.
- () What is the default limit on the number of S3 buckets that can be created by an account?
- **() 100** [CORRECT]

**Answer:**
Correct Answer: **100**

**Explanation:**
Security Groups is the correct answer. The best option, in this case, is security groups for each Windows instance network interface. If this were controlled with NACLs, it would also prevent access to the Linux instances.

---

## Question 16

**Q:** You have a small database workload with infrequent I/O. These databases are mainly used as ad hoc databases for noncritical testing purposes. Which storage medium would be the most cost-effective way to meet these requirements?

**Options:**
- (A) Amazon RDS Provisioned IOPS (SSD) Storage
- (B) Amazon RDS Magnetic Storage
- (C) Amazon RDS Cold Storage
- (D) Amazon RDS General Purpose (SSD) Storage
- (E) Amazon RDS Magnetic Storage is the correct answer. Amazon RDS Magnetic Storage would be the most suitable. In this case, you need to consider the lower cost since these are noncritical databases.
- (F) Incorrect Answers:
- (G) Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are incorrect because Amazon RDS General Purpose (SSD) Storage and Amazon RDS Provisioned IOPS (SSD) Storage are going to add more cost.
- (H) Amazon RDS Cold Storage is incorrect because RDS Cold Storage doesn’t exist.
- (I) Which one of the following is controlled by a security group attached to an instance?
- (J) NACLs
- () Database error codes
- () Inbound traffic
- () HTTP error codes
- () Inbound traffic is the correct answer. Security groups control inbound and outbound traffic. They do not control error codes of any kinds or NACLs, which are applied to the subnet and not to instances.
- () You have several Windows and Linux instances within a single subnet in a VPC. You want to ensure that no inbound traffic can reach the Windows instances. What is the best option?
- () Security Groups
- () Linux firewall
- () IAM
- () Security Groups is the correct answer. The best option, in this case, is security groups for each Windows instance network interface. If this were controlled with NACLs, it would also prevent access to the Linux instances.
- () What is the default limit on the number of S3 buckets that can be created by an account?
- () 100
- () 200
- () 150
- () 100 is the correct answer. The default limit is 100 S3 buckets per account. However, you can request an upgrade to create more S3 buckets.
- () What is the default maximum number of VPCs that can be created in a region?
- **() 5** [CORRECT]

**Answer:**
Correct Answer: **5**

**Explanation:**
100 is the correct answer. The default limit is 100 S3 buckets per account. However, you can request an upgrade to create more S3 buckets.

---

## Question 17

**Q:** Which one of the following is controlled by a security group attached to an instance?

**Options:**
- (A) NACLs
- (B) Database error codes
- (C) Inbound traffic
- (D) HTTP error codes
- (E) Inbound traffic is the correct answer. Security groups control inbound and outbound traffic. They do not control error codes of any kinds or NACLs, which are applied to the subnet and not to instances.
- (F) You have several Windows and Linux instances within a single subnet in a VPC. You want to ensure that no inbound traffic can reach the Windows instances. What is the best option?
- (G) Security Groups
- (H) Linux firewall
- (I) IAM
- (J) Security Groups is the correct answer. The best option, in this case, is security groups for each Windows instance network interface. If this were controlled with NACLs, it would also prevent access to the Linux instances.
- () What is the default limit on the number of S3 buckets that can be created by an account?
- () 100
- () 200
- () 150
- () 100 is the correct answer. The default limit is 100 S3 buckets per account. However, you can request an upgrade to create more S3 buckets.
- () What is the default maximum number of VPCs that can be created in a region?
- () 5
- () 5 is the correct answer. You can create a maximum of five VPCs in a region. To create more, you must request the ability from AWS support.
- () You must select the S3 storage class with the highest level of resiliency. Which class do you choose?
- () S3 Standard-Infrequent Access
- () S3 HA
- **() S3 Standard** [CORRECT]

**Answer:**
Correct Answer: **S3 Standard**

**Explanation:**
5 is the correct answer. You can create a maximum of five VPCs in a region. To create more, you must request the ability from AWS support.

---

## Question 18

**Q:** You have several Windows and Linux instances within a single subnet in a VPC. You want to ensure that no inbound traffic can reach the Windows instances. What is the best option?

**Options:**
- (A) NACLs
- (B) Security Groups
- (C) Linux firewall
- (D) IAM
- (E) Security Groups is the correct answer. The best option, in this case, is security groups for each Windows instance network interface. If this were controlled with NACLs, it would also prevent access to the Linux instances.
- (F) What is the default limit on the number of S3 buckets that can be created by an account?
- (G) 100
- (H) 200
- (I) 150
- (J) 100 is the correct answer. The default limit is 100 S3 buckets per account. However, you can request an upgrade to create more S3 buckets.
- () What is the default maximum number of VPCs that can be created in a region?
- () 5
- () 5 is the correct answer. You can create a maximum of five VPCs in a region. To create more, you must request the ability from AWS support.
- () You must select the S3 storage class with the highest level of resiliency. Which class do you choose?
- () S3 Standard-Infrequent Access
- () S3 HA
- () S3 Standard
- () S3 One Zone-Infrequent Access
- () S3 Standard is the correct answer. The S3 Standard class provides 99.999999999% uptime and is the highest resiliency offered. S3 Standard-IA provides for 99.9% uptime. S3 One Zone-IA provides for 99.5% uptime. No such class as S3 HA exists.
- () What can be used to assign permissions to more than one user login without having to modify each login individually?
- **() Groups** [CORRECT]
- () Collections

**Answer:**
Correct Answer: **Groups**

**Explanation:**
S3 Standard is the correct answer. The S3 Standard class provides 99.999999999% uptime and is the highest resiliency offered. S3 Standard-IA provides for 99.9% uptime. S3 One Zone-IA provides for 99.5% uptime. No such class as S3 HA exists.

---

## Question 19

**Q:** What is the default limit on the number of S3 buckets that can be created by an account?

**Options:**
- (A) 100
- (B) 200
- (C) 150
- (D) 100 is the correct answer. The default limit is 100 S3 buckets per account. However, you can request an upgrade to create more S3 buckets.
- (E) What is the default maximum number of VPCs that can be created in a region?
- (F) 5
- (G) 5 is the correct answer. You can create a maximum of five VPCs in a region. To create more, you must request the ability from AWS support.
- (H) You must select the S3 storage class with the highest level of resiliency. Which class do you choose?
- (I) S3 Standard-Infrequent Access
- (J) S3 HA
- () S3 Standard
- () S3 One Zone-Infrequent Access
- () S3 Standard is the correct answer. The S3 Standard class provides 99.999999999% uptime and is the highest resiliency offered. S3 Standard-IA provides for 99.9% uptime. S3 One Zone-IA provides for 99.5% uptime. No such class as S3 HA exists.
- () What can be used to assign permissions to more than one user login without having to modify each login individually?
- **() Groups** [CORRECT]
- () Collections
- () ACL
- () NACL
- () Groups is the correct answer. AWS Identity and Access Management (IAM) supports the use of groups for such scenarios. Create a group. Assign permissions to the group. Place logins in the group. Collections are not supported in AWS and NACLs/ACLs do not provide a solution to this scenario.
- () What is the default duration of cost history shown in the Cost Explorer view of AWS?
- () 1 month
- () 1 year
- () 2 years

**Answer:**
Correct Answer: **Groups**

**Explanation:**
Groups is the correct answer. AWS Identity and Access Management (IAM) supports the use of groups for such scenarios. Create a group. Assign permissions to the group. Place logins in the group. Collections are not supported in AWS and NACLs/ACLs do not provide a solution to this scenario.

---

## Question 20

**Q:** What is the default maximum number of VPCs that can be created in a region?

**Options:**
- (A) 5
- (B) 5 is the correct answer. You can create a maximum of five VPCs in a region. To create more, you must request the ability from AWS support.
- (C) You must select the S3 storage class with the highest level of resiliency. Which class do you choose?
- (D) S3 Standard-Infrequent Access
- (E) S3 HA
- (F) S3 Standard
- (G) S3 One Zone-Infrequent Access
- (H) S3 Standard is the correct answer. The S3 Standard class provides 99.999999999% uptime and is the highest resiliency offered. S3 Standard-IA provides for 99.9% uptime. S3 One Zone-IA provides for 99.5% uptime. No such class as S3 HA exists.
- (I) What can be used to assign permissions to more than one user login without having to modify each login individually?
- (J) Groups
- () Collections
- () ACL
- () NACL
- () Groups is the correct answer. AWS Identity and Access Management (IAM) supports the use of groups for such scenarios. Create a group. Assign permissions to the group. Place logins in the group. Collections are not supported in AWS and NACLs/ACLs do not provide a solution to this scenario.
- () What is the default duration of cost history shown in the Cost Explorer view of AWS?
- () 1 month
- () 1 year
- () 2 years
- **() 6 months** [CORRECT]
- () 6 months is the correct answer. The Cost Explorer shows 6 months' history by default. This can be adjusted. The history can be used to see where your costs are accruing and to potentially predict future costs.
- () Correct selection
- () Create RDS read replicas and additional web/app instances across all the available AZs.
- () Use CloudFront to accelerate the presentation of the PDF images.
- () Move the metadata to a DynamoDB solution, permitting real-time scaling of read IOPS to match demand.

**Answer:**
Correct Answer: **6 months**

**Explanation:**
6 months is the correct answer. The Cost Explorer shows 6 months' history by default. This can be adjusted. The history can be used to see where your costs are accruing and to potentially predict future costs.

---

## Question 21

**Q:** You must select the S3 storage class with the highest level of resiliency. Which class do you choose?

**Options:**
- (A) S3 Standard-Infrequent Access
- (B) S3 HA
- (C) S3 Standard
- (D) S3 One Zone-Infrequent Access
- (E) S3 Standard is the correct answer. The S3 Standard class provides 99.999999999% uptime and is the highest resiliency offered. S3 Standard-IA provides for 99.9% uptime. S3 One Zone-IA provides for 99.5% uptime. No such class as S3 HA exists.
- (F) What can be used to assign permissions to more than one user login without having to modify each login individually?
- (G) Groups
- (H) Collections
- (I) ACL
- (J) NACL
- () Groups is the correct answer. AWS Identity and Access Management (IAM) supports the use of groups for such scenarios. Create a group. Assign permissions to the group. Place logins in the group. Collections are not supported in AWS and NACLs/ACLs do not provide a solution to this scenario.
- () What is the default duration of cost history shown in the Cost Explorer view of AWS?
- () 1 month
- () 1 year
- () 2 years
- **() 6 months** [CORRECT]
- () 6 months is the correct answer. The Cost Explorer shows 6 months' history by default. This can be adjusted. The history can be used to see where your costs are accruing and to potentially predict future costs.
- () Correct selection
- () Create RDS read replicas and additional web/app instances across all the available AZs.
- () Use CloudFront to accelerate the presentation of the PDF images.
- () Move the metadata to a DynamoDB solution, permitting real-time scaling of read IOPS to match demand.
- () Install an ElastiCache cluster in front of the RDS installation.
- () Move the images to S3 to reduce database IO.
- () Correct answers:
- () Install an ElastiCache cluster in front of the RDS installation and Create RDS read replicas and additional web/app instances across all the available AZs are correct. In this case, the customer can’t change the architecture immediately so they have to keep the PDFs in RDS. Thus, in order to provide faster read-only performance, you need to create read replicas. ElastiCache in front of RDS is going to provide an additional performance boost. 
- () Incorrect Answers:
- () Use CloudFront to accelerate the presentation of the PDF images is incorrect because, as per the CTO, you can’t change the code.
- () Move the images to S3 to reduce database IO is incorrect because, as per the CTO, you can’t change the code. E is incorrect because, as per the CTO, you can’t change the code.
- () Which one of the following RDS database types does not support read replicas?

**Answer:**
Correct Answer: **6 months**

**Explanation:**
6 months is the correct answer. The Cost Explorer shows 6 months' history by default. This can be adjusted. The history can be used to see where your costs are accruing and to potentially predict future costs.

---

## Question 22

**Q:** What can be used to assign permissions to more than one user login without having to modify each login individually?

**Options:**
- (A) Groups
- (B) Collections
- (C) ACL
- (D) NACL
- (E) Groups is the correct answer. AWS Identity and Access Management (IAM) supports the use of groups for such scenarios. Create a group. Assign permissions to the group. Place logins in the group. Collections are not supported in AWS and NACLs/ACLs do not provide a solution to this scenario.
- (F) What is the default duration of cost history shown in the Cost Explorer view of AWS?
- (G) 1 month
- (H) 1 year
- (I) 2 years
- (J) 6 months
- () 6 months is the correct answer. The Cost Explorer shows 6 months' history by default. This can be adjusted. The history can be used to see where your costs are accruing and to potentially predict future costs.
- () Correct selection
- () Create RDS read replicas and additional web/app instances across all the available AZs.
- () Use CloudFront to accelerate the presentation of the PDF images.
- () Move the metadata to a DynamoDB solution, permitting real-time scaling of read IOPS to match demand.
- () Install an ElastiCache cluster in front of the RDS installation.
- () Move the images to S3 to reduce database IO.
- () Correct answers:
- () Install an ElastiCache cluster in front of the RDS installation and Create RDS read replicas and additional web/app instances across all the available AZs are correct. In this case, the customer can’t change the architecture immediately so they have to keep the PDFs in RDS. Thus, in order to provide faster read-only performance, you need to create read replicas. ElastiCache in front of RDS is going to provide an additional performance boost. 
- () Incorrect Answers:
- () Use CloudFront to accelerate the presentation of the PDF images is incorrect because, as per the CTO, you can’t change the code.
- () Move the images to S3 to reduce database IO is incorrect because, as per the CTO, you can’t change the code. E is incorrect because, as per the CTO, you can’t change the code.
- () Which one of the following RDS database types does not support read replicas?
- **() Aurora** [CORRECT]
- () PostgreSQL
- () MySQL
- () MariaDB
- () Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.
- () Your company has a policy of encrypting all data at rest. You host your production environment on EC2 in a non-default VPC. Attached to your EC2 instances are multiple EBS volumes, and you must ensure this data is encrypted. Which of the following options will allow you to do this? (Choose three.)

**Answer:**
Correct Answer: **Aurora**

**Explanation:**
Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.

---

## Question 23

**Q:** What is the default duration of cost history shown in the Cost Explorer view of AWS?

**Options:**
- (A) 1 month
- (B) 1 year
- (C) 2 years
- (D) 6 months
- (E) 6 months is the correct answer. The Cost Explorer shows 6 months' history by default. This can be adjusted. The history can be used to see where your costs are accruing and to potentially predict future costs.
- (F) Correct selection
- (G) Create RDS read replicas and additional web/app instances across all the available AZs.
- (H) Use CloudFront to accelerate the presentation of the PDF images.
- (I) Move the metadata to a DynamoDB solution, permitting real-time scaling of read IOPS to match demand.
- (J) Install an ElastiCache cluster in front of the RDS installation.
- () Move the images to S3 to reduce database IO.
- () Correct answers:
- () Install an ElastiCache cluster in front of the RDS installation and Create RDS read replicas and additional web/app instances across all the available AZs are correct. In this case, the customer can’t change the architecture immediately so they have to keep the PDFs in RDS. Thus, in order to provide faster read-only performance, you need to create read replicas. ElastiCache in front of RDS is going to provide an additional performance boost. 
- () Incorrect Answers:
- () Use CloudFront to accelerate the presentation of the PDF images is incorrect because, as per the CTO, you can’t change the code.
- () Move the images to S3 to reduce database IO is incorrect because, as per the CTO, you can’t change the code. E is incorrect because, as per the CTO, you can’t change the code.
- () Which one of the following RDS database types does not support read replicas?
- **() Aurora** [CORRECT]
- () PostgreSQL
- () MySQL
- () MariaDB
- () Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.
- () Your company has a policy of encrypting all data at rest. You host your production environment on EC2 in a non-default VPC. Attached to your EC2 instances are multiple EBS volumes, and you must ensure this data is encrypted. Which of the following options will allow you to do this? (Choose three.)
- () Encrypt the data inside your application, before storing it on EBS.
- () EBS volumes are encrypted by default. You do not need to do anything.
- () Use third-party volume encryption tools.
- () Encrypt the data using native encryption tools available in the operating system.
- () Install SSL certificates on the servers so as to encrypt your data.
- () Use third-party volume encryption tools, Encrypt the data using native encryption tools available in the operating system, and Encrypt the data inside your application, before storing it on EBS are correct. These answers cover all the options required to encrypt all the data at rest. 
- () Install SSL certificates on the servers so as to encrypt your data is incorrect because SSL certificates will only be useful to encrypt data in transit, not data at rest.

**Answer:**
Correct Answer: **Aurora**

**Explanation:**
Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.

---

## Question 24

**Q:** You have been engaged as a consultant by a company that generates utility bills and publishes them online. PDF images are generated and then stored on a high-performance RDS instance. Generally, invoices are viewed by customers once per month. Recently, however, the number of customers has increased threefold, and the wait-time necessary to view invoices has increased unacceptably. The CTO is unwilling to alter the codebase more than necessary this quarter, but needs to return performance to an acceptable level before the end-of-the-month print run. Which of the following solutions would you feel comfortable proposing to the CTO and GM? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Create RDS read replicas and additional web/app instances across all the available AZs.
- (C) Use CloudFront to accelerate the presentation of the PDF images.
- (D) Move the metadata to a DynamoDB solution, permitting real-time scaling of read IOPS to match demand.
- (E) Install an ElastiCache cluster in front of the RDS installation.
- (F) Move the images to S3 to reduce database IO.
- (G) Correct answers:
- (H) Install an ElastiCache cluster in front of the RDS installation and Create RDS read replicas and additional web/app instances across all the available AZs are correct. In this case, the customer can’t change the architecture immediately so they have to keep the PDFs in RDS. Thus, in order to provide faster read-only performance, you need to create read replicas. ElastiCache in front of RDS is going to provide an additional performance boost. 
- (I) Incorrect Answers:
- (J) Use CloudFront to accelerate the presentation of the PDF images is incorrect because, as per the CTO, you can’t change the code.
- () Move the images to S3 to reduce database IO is incorrect because, as per the CTO, you can’t change the code. E is incorrect because, as per the CTO, you can’t change the code.
- () Which one of the following RDS database types does not support read replicas?
- **() Aurora** [CORRECT]
- () PostgreSQL
- () MySQL
- () MariaDB
- () Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.
- () Your company has a policy of encrypting all data at rest. You host your production environment on EC2 in a non-default VPC. Attached to your EC2 instances are multiple EBS volumes, and you must ensure this data is encrypted. Which of the following options will allow you to do this? (Choose three.)
- () Encrypt the data inside your application, before storing it on EBS.
- () EBS volumes are encrypted by default. You do not need to do anything.
- () Use third-party volume encryption tools.
- () Encrypt the data using native encryption tools available in the operating system.
- () Install SSL certificates on the servers so as to encrypt your data.
- () Use third-party volume encryption tools, Encrypt the data using native encryption tools available in the operating system, and Encrypt the data inside your application, before storing it on EBS are correct. These answers cover all the options required to encrypt all the data at rest. 
- () Install SSL certificates on the servers so as to encrypt your data is incorrect because SSL certificates will only be useful to encrypt data in transit, not data at rest.
- () EBS volumes are encrypted by default. You do not need to do anything is incorrect because EBS volumes are not encrypted by default.

**Answer:**
Correct Answer: **Aurora**

**Explanation:**
Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.

---

## Question 25

**Q:** Which one of the following RDS database types does not support read replicas?

**Options:**
- **(A) Aurora** [CORRECT]
- (B) PostgreSQL
- (C) MySQL
- (D) MariaDB
- (E) Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.
- (F) Your company has a policy of encrypting all data at rest. You host your production environment on EC2 in a non-default VPC. Attached to your EC2 instances are multiple EBS volumes, and you must ensure this data is encrypted. Which of the following options will allow you to do this? (Choose three.)
- (G) Correct selection
- (H) Encrypt the data inside your application, before storing it on EBS.
- (I) EBS volumes are encrypted by default. You do not need to do anything.
- (J) Use third-party volume encryption tools.
- () Encrypt the data using native encryption tools available in the operating system.
- () Install SSL certificates on the servers so as to encrypt your data.
- () Correct Answers:
- () Use third-party volume encryption tools, Encrypt the data using native encryption tools available in the operating system, and Encrypt the data inside your application, before storing it on EBS are correct. These answers cover all the options required to encrypt all the data at rest. 
- () Incorrect Answers:
- () Install SSL certificates on the servers so as to encrypt your data is incorrect because SSL certificates will only be useful to encrypt data in transit, not data at rest.
- () EBS volumes are encrypted by default. You do not need to do anything is incorrect because EBS volumes are not encrypted by default.

**Answer:**
Correct Answer: **Aurora**

**Explanation:**
Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.

---

## Question 26

**Q:** Your company has a policy of encrypting all data at rest. You host your production environment on EC2 in a non-default VPC. Attached to your EC2 instances are multiple EBS volumes, and you must ensure this data is encrypted. Which of the following options will allow you to do this? (Choose three.)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Encrypt the data inside your application, before storing it on EBS.
- (C) EBS volumes are encrypted by default. You do not need to do anything.
- (D) Use third-party volume encryption tools.
- (E) Encrypt the data using native encryption tools available in the operating system.
- (F) Install SSL certificates on the servers so as to encrypt your data.
- (G) Correct Answers:
- (H) Use third-party volume encryption tools, Encrypt the data using native encryption tools available in the operating system, and Encrypt the data inside your application, before storing it on EBS are correct. These answers cover all the options required to encrypt all the data at rest. 
- (I) Incorrect Answers:
- (J) Install SSL certificates on the servers so as to encrypt your data is incorrect because SSL certificates will only be useful to encrypt data in transit, not data at rest.
- () EBS volumes are encrypted by default. You do not need to do anything is incorrect because EBS volumes are not encrypted by default.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 27

**Q:** You’ve been tasked with implementing a globally accessible storage solution that will scale from a few terabytes (now) to an unknown, but significantly greater, volume of data in three years’ time. You don’t want to spend a lot of money. Which AWS service would best meet your current and projected storage needs and at the same time make sure the cost is minimal?

**Options:**
- (A) S3
- (B) RDS
- (C) DynamoDB
- (D) EC2 with EBS
- (E) S3 is correct. Amazon S3 is highly scalable, secure storage and can be used for any kind of storage. S3 will scale to any projected volume of data. S3 provides different storage types to keep the cost minimal. 
- (F) Incorrect Answers:
- (G) DynamoDB is incorrect because DynamoDB is a NoSQL database.
- (H) EC2 with EBS is incorrect because EC2 with EBS is going to increase the cost.
- (I) RDS is incorrect because RDS is a relational database service.
- (J) HTTP is used to upload to S3 buckets. Which HTTP method has eventual consistency with S3 bucket writes?
- () Updates
- () Deletes
- () Erases
- () PUTs of new files
- () Deletes is the correct answer. Deletes and Overwrite PUTs have eventual consistency. Others have write and then read consistency. Erases are not supported.
- () What is the maximum number of security groups that can be assigned to an instance?
- () Unlimited
- () 5
- () 5 is the correct answer. You can assign up to five security groups to an instance.
- () What is the model used within AWS wherein AWS guarantees the secure operation of the cloud and the customer ensures the security of that which is placed in the cloud?
- () Customer Responsibility
- **() Shared Responsibility** [CORRECT]
- () Provider Responsibility
- () User Responsibility
- () Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

**Answer:**
Correct Answer: **Shared Responsibility**

**Explanation:**
Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

---

## Question 28

**Q:** HTTP is used to upload to S3 buckets. Which HTTP method has eventual consistency with S3 bucket writes?

**Options:**
- (A) Updates
- (B) Deletes
- (C) Erases
- (D) PUTs of new files
- (E) Deletes is the correct answer. Deletes and Overwrite PUTs have eventual consistency. Others have write and then read consistency. Erases are not supported.
- (F) What is the maximum number of security groups that can be assigned to an instance?
- (G) Unlimited
- (H) 5
- (I) 5 is the correct answer. You can assign up to five security groups to an instance.
- (J) What is the model used within AWS wherein AWS guarantees the secure operation of the cloud and the customer ensures the security of that which is placed in the cloud?
- () Customer Responsibility
- **() Shared Responsibility** [CORRECT]
- () Provider Responsibility
- () User Responsibility
- () Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

**Answer:**
Correct Answer: **Shared Responsibility**

**Explanation:**
Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

---

## Question 29

**Q:** What is the maximum number of security groups that can be assigned to an instance?

**Options:**
- (A) Unlimited
- (B) 5
- (C) 5 is the correct answer. You can assign up to five security groups to an instance.
- (D) What is the model used within AWS wherein AWS guarantees the secure operation of the cloud and the customer ensures the security of that which is placed in the cloud?
- (E) Customer Responsibility
- **(F) Shared Responsibility** [CORRECT]
- (G) Provider Responsibility
- (H) User Responsibility
- (I) Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

**Answer:**
Correct Answer: **Shared Responsibility**

**Explanation:**
Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

---

## Question 30

**Q:** What is the model used within AWS wherein AWS guarantees the secure operation of the cloud and the customer ensures the security of that which is placed in the cloud?

**Options:**
- (A) Customer Responsibility
- **(B) Shared Responsibility** [CORRECT]
- (C) Provider Responsibility
- (D) User Responsibility
- (E) Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

**Answer:**
Correct Answer: **Shared Responsibility**

**Explanation:**
Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

---

## Question 31

**Q:** Although your application customarily runs at 30% usage, you have identified a recurring usage spike (greater than 90% usage) between 8 p.m. and midnight daily. What is the most cost-effective way to scale your application to meet this increased need?

**Options:**
- (A) Use proactive cyclic scaling to boost your capacity at a fixed interval.
- (B) Increase the size of the resource group to meet demand.
- (C) Deploy additional EC2 instances to meet the demand.
- (D) Manually deploy reactive event-based scaling each night at 7:45.
- (E) Use proactive cyclic scaling to boost your capacity at a fixed interval. is the correct answer. In this case, you need to use proactive scaling at 8 p.m. and midnight, so you can have Auto Scaling policies that can handle the workload during that time. 
- (F) Incorrect Answers:
- (G) Increase the size of the resource group to meet demand is incorrect because it doesn’t indicate when to increase.
- (H) Deploy additional EC2 instances to meet the demand is incorrect because it doesn’t indicate when to increase.
- (I) Manually deploy reactive event-based scaling each night at 7:45 is incorrect because 7:45 p.m. is too early, and in this case you won’t be doing reactive event-based scaling.
- (J) You are a solutions architect working for a construction company. Your company is migrating its production estate to AWS, and you are in the process of setting up access to the AWS console using Identity Access Management (IAM). You have created 15 users for your system administrators. What further steps do you need to take to enable your system administrators to get access to the AWS console in a secure fashion? (Choose two.)
- () Correct selection
- () Have each user set up multifactor authentication once they have logged in to the console.
- () Get the systems administrators to download the CLI and configure it on their laptop, using their usernames and passwords.
- () Give the system administrators the secret access key and access key ID, and tell them to use these credentials to log in to the AWS console.
- () Generate a password for each user and give these passwords to your system administrators.
- () Correct Answers:
- () Have each user set up multifactor authentication once they have logged in to the console and Generate a password for each user and give these passwords to your system administrators are correct. You should generate a password for each user and give these passwords to your system administrators. You should then have each user set up multifactor authentication once they have been able to log in to the console.
- () Give the system administrators the secret access key and access key ID, and tell them to use these credentials to log in to the AWS console is incorrect because you cannot use the secret access key and access key ID to log in to the AWS console; rather, these credentials are used to call Amazon APIs.
- () Get the systems administrators to download the CLI and configure it on their laptop, using their usernames and passwords is incorrect because for the AWS CLI, you need an access key ID and secret access key.
- () You have been asked to implement a read replica RDS setup. What is the primary purpose of such a configuration?
- () Redundancy
- () Business continuity
- () Security
- () Performance
- () Performance is the correct answer. Read replicas are created to improve the performance of read operations. They have a dedicated instance for read processing and write operations, as read operations are moved from the primary instance to a read replica instance. Read replicas are not primarily created for business continuity, redundancy, or security.
- () What should be implemented when microsecond response time is required of a DynamoDB implementation?
- () ElastiCache
- () EFS
- () EBS
- **() DAX** [CORRECT]
- () DAX is the correct answer. DAX is the DynamoDB Accelerator, which is an in-memory cache solution specifically designed for DynamoDB and can result in response times in microseconds. ElastiCache can be used with DynamoDB, but is not optimized for it. EBS and EFS have no impact here.

**Answer:**
Correct Answer: **DAX**

**Explanation:**
DAX is the correct answer. DAX is the DynamoDB Accelerator, which is an in-memory cache solution specifically designed for DynamoDB and can result in response times in microseconds. ElastiCache can be used with DynamoDB, but is not optimized for it. EBS and EFS have no impact here.

---

## Question 32

**Q:** You are a solutions architect working for a construction company. Your company is migrating its production estate to AWS, and you are in the process of setting up access to the AWS console using Identity Access Management (IAM). You have created 15 users for your system administrators. What further steps do you need to take to enable your system administrators to get access to the AWS console in a secure fashion? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Have each user set up multifactor authentication once they have logged in to the console.
- (C) Get the systems administrators to download the CLI and configure it on their laptop, using their usernames and passwords.
- (D) Give the system administrators the secret access key and access key ID, and tell them to use these credentials to log in to the AWS console.
- (E) Generate a password for each user and give these passwords to your system administrators.
- (F) Correct Answers:
- (G) Have each user set up multifactor authentication once they have logged in to the console and Generate a password for each user and give these passwords to your system administrators are correct. You should generate a password for each user and give these passwords to your system administrators. You should then have each user set up multifactor authentication once they have been able to log in to the console.
- (H) Incorrect Answers:
- (I) Give the system administrators the secret access key and access key ID, and tell them to use these credentials to log in to the AWS console is incorrect because you cannot use the secret access key and access key ID to log in to the AWS console; rather, these credentials are used to call Amazon APIs.
- (J) Get the systems administrators to download the CLI and configure it on their laptop, using their usernames and passwords is incorrect because for the AWS CLI, you need an access key ID and secret access key.
- () You have been asked to implement a read replica RDS setup. What is the primary purpose of such a configuration?
- () Redundancy
- () Business continuity
- () Security
- () Performance
- () Performance is the correct answer. Read replicas are created to improve the performance of read operations. They have a dedicated instance for read processing and write operations, as read operations are moved from the primary instance to a read replica instance. Read replicas are not primarily created for business continuity, redundancy, or security.
- () What should be implemented when microsecond response time is required of a DynamoDB implementation?
- () ElastiCache
- () EFS
- () EBS
- **() DAX** [CORRECT]
- () DAX is the correct answer. DAX is the DynamoDB Accelerator, which is an in-memory cache solution specifically designed for DynamoDB and can result in response times in microseconds. ElastiCache can be used with DynamoDB, but is not optimized for it. EBS and EFS have no impact here.
- () When copying an AMI, you must manually copy which of the following types of information to the new instance? (Choose three.)
- () User-defined tags
- () User data
- () S3 bucket permissions
- () Launch permissions
- () Launch permissions, S3 bucket permissions, and User-defined tags are correct. Launch permissions, S3 bucket permissions, and user-defined tags must be copied manually to an instance based on an AMI. 
- () Incorrect Answer:
- () User data is incorrect. User data is part of the AMI itself and does not need to be copied manually.

**Answer:**
Correct Answer: **DAX**

**Explanation:**
DAX is the correct answer. DAX is the DynamoDB Accelerator, which is an in-memory cache solution specifically designed for DynamoDB and can result in response times in microseconds. ElastiCache can be used with DynamoDB, but is not optimized for it. EBS and EFS have no impact here.

---

## Question 33

**Q:** You have been asked to implement a read replica RDS setup. What is the primary purpose of such a configuration?

**Options:**
- (A) Redundancy
- (B) Business continuity
- (C) Security
- (D) Performance
- (E) Performance is the correct answer. Read replicas are created to improve the performance of read operations. They have a dedicated instance for read processing and write operations, as read operations are moved from the primary instance to a read replica instance. Read replicas are not primarily created for business continuity, redundancy, or security.
- (F) What should be implemented when microsecond response time is required of a DynamoDB implementation?
- (G) ElastiCache
- (H) EFS
- (I) EBS
- (J) DAX
- () DAX is the correct answer. DAX is the DynamoDB Accelerator, which is an in-memory cache solution specifically designed for DynamoDB and can result in response times in microseconds. ElastiCache can be used with DynamoDB, but is not optimized for it. EBS and EFS have no impact here.
- () When copying an AMI, you must manually copy which of the following types of information to the new instance? (Choose three.)
- () Correct selection
- () User-defined tags
- () User data
- () S3 bucket permissions
- () Launch permissions
- () Correct Answers:
- () Launch permissions, S3 bucket permissions, and User-defined tags are correct. Launch permissions, S3 bucket permissions, and user-defined tags must be copied manually to an instance based on an AMI. 
- () Incorrect Answer:
- () User data is incorrect. User data is part of the AMI itself and does not need to be copied manually.
- () What is used to control network traffic at the subnet level in AWS?
- () Logins
- () Groups
- **() Network ACLs (NACLs)** [CORRECT]
- () Security groups
- () Network ACLs (NACLs) is the correct answer. NACLs operate at the subnet level and security groups operate at the instance level. NACLs support allow and deny rules and security groups support only allow rules. Logins and groups do not control network traffic, they control the ability to login and the permissions associated with a user (login).
- () When does Amazon recommend using the db.t2.small and db.t2.medium database instances with the Aurora database service?

**Answer:**
Correct Answer: **Network ACLs (NACLs)**

**Explanation:**
Network ACLs (NACLs) is the correct answer. NACLs operate at the subnet level and security groups operate at the instance level. NACLs support allow and deny rules and security groups support only allow rules. Logins and groups do not control network traffic, they control the ability to login and the permissions associated with a user (login).

---

## Question 34

**Q:** What should be implemented when microsecond response time is required of a DynamoDB implementation?

**Options:**
- (A) ElastiCache
- (B) EFS
- (C) EBS
- (D) DAX
- (E) DAX is the correct answer. DAX is the DynamoDB Accelerator, which is an in-memory cache solution specifically designed for DynamoDB and can result in response times in microseconds. ElastiCache can be used with DynamoDB, but is not optimized for it. EBS and EFS have no impact here.
- (F) When copying an AMI, you must manually copy which of the following types of information to the new instance? (Choose three.)
- (G) Correct selection
- (H) User-defined tags
- (I) User data
- (J) S3 bucket permissions
- () Launch permissions
- () Correct Answers:
- () Launch permissions, S3 bucket permissions, and User-defined tags are correct. Launch permissions, S3 bucket permissions, and user-defined tags must be copied manually to an instance based on an AMI. 
- () Incorrect Answer:
- () User data is incorrect. User data is part of the AMI itself and does not need to be copied manually.
- () What is used to control network traffic at the subnet level in AWS?
- () Logins
- () Groups
- () Network ACLs (NACLs)
- () Security groups
- () Network ACLs (NACLs) is the correct answer. NACLs operate at the subnet level and security groups operate at the instance level. NACLs support allow and deny rules and security groups support only allow rules. Logins and groups do not control network traffic, they control the ability to login and the permissions associated with a user (login).
- () When does Amazon recommend using the db.t2.small and db.t2.medium database instances with the Aurora database service?
- () For heavy load servers
- () For medium load servers
- **() For development and test servers** [CORRECT]
- () For small load servers
- () For development and test servers is the correct answer. Amazon only recommends the use of db.t2.small and db.t2.medium for non-production servers such as development and test servers.
- () You are working with AWS AMIs. What kind of AMI should be used when you want to customize an image and then reuse it to scale up a deployment?

**Answer:**
Correct Answer: **For development and test servers**

**Explanation:**
For development and test servers is the correct answer. Amazon only recommends the use of db.t2.small and db.t2.medium for non-production servers such as development and test servers.

---

## Question 35

**Q:** When copying an AMI, you must manually copy which of the following types of information to the new instance? (Choose three.)

**Options:**
- (A) Correct selection
- (B) User-defined tags
- (C) User data
- (D) S3 bucket permissions
- (E) Launch permissions
- (F) Correct Answers:
- (G) Launch permissions, S3 bucket permissions, and User-defined tags are correct. Launch permissions, S3 bucket permissions, and user-defined tags must be copied manually to an instance based on an AMI. 
- (H) Incorrect Answer:
- (I) User data is incorrect. User data is part of the AMI itself and does not need to be copied manually.
- (J) What is used to control network traffic at the subnet level in AWS?
- () Logins
- () Groups
- () Network ACLs (NACLs)
- () Security groups
- () Network ACLs (NACLs) is the correct answer. NACLs operate at the subnet level and security groups operate at the instance level. NACLs support allow and deny rules and security groups support only allow rules. Logins and groups do not control network traffic, they control the ability to login and the permissions associated with a user (login).
- () When does Amazon recommend using the db.t2.small and db.t2.medium database instances with the Aurora database service?
- () For heavy load servers
- () For medium load servers
- () For development and test servers
- () For small load servers
- () For development and test servers is the correct answer. Amazon only recommends the use of db.t2.small and db.t2.medium for non-production servers such as development and test servers.
- () You are working with AWS AMIs. What kind of AMI should be used when you want to customize an image and then reuse it to scale up a deployment?
- **() Private AMI** [CORRECT]
- () Amazon Quick Start AMI
- () AWS Marketplace AMI
- () Community AMI
- () Private AMI is the correct answer. A private AMI can be created based on your customized image. This allows you to easily scale up a solution. Community, Marketplace, and Quick Start AMIs can be used for the initial instance that is to be customized, but they cannot be customized themselves.
- () What instance type family is best used when things like specialized GPUs or FPGAs are required?

**Answer:**
Correct Answer: **Private AMI**

**Explanation:**
Private AMI is the correct answer. A private AMI can be created based on your customized image. This allows you to easily scale up a solution. Community, Marketplace, and Quick Start AMIs can be used for the initial instance that is to be customized, but they cannot be customized themselves.

---

## Question 36

**Q:** What is used to control network traffic at the subnet level in AWS?

**Options:**
- (A) Logins
- (B) Groups
- (C) Network ACLs (NACLs)
- (D) Security groups
- (E) Network ACLs (NACLs) is the correct answer. NACLs operate at the subnet level and security groups operate at the instance level. NACLs support allow and deny rules and security groups support only allow rules. Logins and groups do not control network traffic, they control the ability to login and the permissions associated with a user (login).
- (F) When does Amazon recommend using the db.t2.small and db.t2.medium database instances with the Aurora database service?
- (G) For heavy load servers
- (H) For medium load servers
- (I) For development and test servers
- (J) For small load servers
- () For development and test servers is the correct answer. Amazon only recommends the use of db.t2.small and db.t2.medium for non-production servers such as development and test servers.
- () You are working with AWS AMIs. What kind of AMI should be used when you want to customize an image and then reuse it to scale up a deployment?
- () Private AMI
- () Amazon Quick Start AMI
- () AWS Marketplace AMI
- () Community AMI
- () Private AMI is the correct answer. A private AMI can be created based on your customized image. This allows you to easily scale up a solution. Community, Marketplace, and Quick Start AMIs can be used for the initial instance that is to be customized, but they cannot be customized themselves.
- () What instance type family is best used when things like specialized GPUs or FPGAs are required?
- () Accelerated computing
- () Memory-optimized
- () Storage-optimized
- () Compute-optimized
- () Accelerated computing is the correct answer. Accelerated computing supports graphics processing units (GPUs) and field-programmable gate arrays (FPGAs) for enhanced processing. Compute-optimized simply provides more powerful CPUs, memory-optimized provides more and faster memory, and storage-optimized provides storage up to 48 TB.
- () You have been given control of an existing AWS environment (account). You want to ensure costs are being managed well. What tool should you run?
- () CloudFormation
- **() Trusted Advisor** [CORRECT]

**Answer:**
Correct Answer: **Trusted Advisor**

**Explanation:**
Accelerated computing is the correct answer. Accelerated computing supports graphics processing units (GPUs) and field-programmable gate arrays (FPGAs) for enhanced processing. Compute-optimized simply provides more powerful CPUs, memory-optimized provides more and faster memory, and storage-optimized provides storage up to 48 TB.

---

## Question 37

**Q:** When does Amazon recommend using the db.t2.small and db.t2.medium database instances with the Aurora database service?

**Options:**
- (A) For heavy load servers
- (B) For medium load servers
- (C) For development and test servers
- (D) For small load servers
- (E) For development and test servers is the correct answer. Amazon only recommends the use of db.t2.small and db.t2.medium for non-production servers such as development and test servers.
- (F) You are working with AWS AMIs. What kind of AMI should be used when you want to customize an image and then reuse it to scale up a deployment?
- (G) Private AMI
- (H) Amazon Quick Start AMI
- (I) AWS Marketplace AMI
- (J) Community AMI
- () Private AMI is the correct answer. A private AMI can be created based on your customized image. This allows you to easily scale up a solution. Community, Marketplace, and Quick Start AMIs can be used for the initial instance that is to be customized, but they cannot be customized themselves.
- () What instance type family is best used when things like specialized GPUs or FPGAs are required?
- () Accelerated computing
- () Memory-optimized
- () Storage-optimized
- () Compute-optimized
- () Accelerated computing is the correct answer. Accelerated computing supports graphics processing units (GPUs) and field-programmable gate arrays (FPGAs) for enhanced processing. Compute-optimized simply provides more powerful CPUs, memory-optimized provides more and faster memory, and storage-optimized provides storage up to 48 TB.
- () You have been given control of an existing AWS environment (account). You want to ensure costs are being managed well. What tool should you run?
- () CloudFormation
- () Trusted Advisor
- () CloudTrail
- () CloudWatch
- () Trusted Advisor is correct. The Trusted Advisor can give recommendations for reducing costs, so this is the tool to run among those listed. CloudWatch monitors the AWS cloud. CloudTrail provides logging for activities in the cloud. CloudFormation is used to automatically deploy a solution.
- () Which one of the following is not something for which AWS Trusted Advisor makes recommendations?
- () Performance
- **() Scalability** [CORRECT]

**Answer:**
Correct Answer: **Scalability**

**Explanation:**
Trusted Advisor is correct. The Trusted Advisor can give recommendations for reducing costs, so this is the tool to run among those listed. CloudWatch monitors the AWS cloud. CloudTrail provides logging for activities in the cloud. CloudFormation is used to automatically deploy a solution.

---

## Question 38

**Q:** You are working with AWS AMIs. What kind of AMI should be used when you want to customize an image and then reuse it to scale up a deployment?

**Options:**
- (A) Private AMI
- (B) Amazon Quick Start AMI
- (C) AWS Marketplace AMI
- (D) Community AMI
- (E) Private AMI is the correct answer. A private AMI can be created based on your customized image. This allows you to easily scale up a solution. Community, Marketplace, and Quick Start AMIs can be used for the initial instance that is to be customized, but they cannot be customized themselves.
- (F) What instance type family is best used when things like specialized GPUs or FPGAs are required?
- (G) Accelerated computing
- (H) Memory-optimized
- (I) Storage-optimized
- (J) Compute-optimized
- () Accelerated computing is the correct answer. Accelerated computing supports graphics processing units (GPUs) and field-programmable gate arrays (FPGAs) for enhanced processing. Compute-optimized simply provides more powerful CPUs, memory-optimized provides more and faster memory, and storage-optimized provides storage up to 48 TB.
- () You have been given control of an existing AWS environment (account). You want to ensure costs are being managed well. What tool should you run?
- () CloudFormation
- () Trusted Advisor
- () CloudTrail
- () CloudWatch
- () Trusted Advisor is correct. The Trusted Advisor can give recommendations for reducing costs, so this is the tool to run among those listed. CloudWatch monitors the AWS cloud. CloudTrail provides logging for activities in the cloud. CloudFormation is used to automatically deploy a solution.
- () Which one of the following is not something for which AWS Trusted Advisor makes recommendations?
- () Performance
- **() Scalability** [CORRECT]
- () Fault Tolerance
- () Cost
- () Scalability is correct. Trusted advisor can make recommendations in the areas of cost, performance, fault tolerance, security, and service limits. It does not make direct recommendations for scalability.
- () You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?
- () AWS CloudFront alerts
- () AWS Trusted Advisor alerts
- () AWS ElastiCache alerts

**Answer:**
Correct Answer: **Scalability**

**Explanation:**
Scalability is correct. Trusted advisor can make recommendations in the areas of cost, performance, fault tolerance, security, and service limits. It does not make direct recommendations for scalability.

---

## Question 39

**Q:** What instance type family is best used when things like specialized GPUs or FPGAs are required?

**Options:**
- (A) Accelerated computing
- (B) Memory-optimized
- (C) Storage-optimized
- (D) Compute-optimized
- (E) Accelerated computing is the correct answer. Accelerated computing supports graphics processing units (GPUs) and field-programmable gate arrays (FPGAs) for enhanced processing. Compute-optimized simply provides more powerful CPUs, memory-optimized provides more and faster memory, and storage-optimized provides storage up to 48 TB.
- (F) You have been given control of an existing AWS environment (account). You want to ensure costs are being managed well. What tool should you run?
- (G) CloudFormation
- (H) Trusted Advisor
- (I) CloudTrail
- (J) CloudWatch
- () Trusted Advisor is correct. The Trusted Advisor can give recommendations for reducing costs, so this is the tool to run among those listed. CloudWatch monitors the AWS cloud. CloudTrail provides logging for activities in the cloud. CloudFormation is used to automatically deploy a solution.
- () Which one of the following is not something for which AWS Trusted Advisor makes recommendations?
- () Performance
- () Scalability
- () Fault Tolerance
- () Cost
- () Scalability is correct. Trusted advisor can make recommendations in the areas of cost, performance, fault tolerance, security, and service limits. It does not make direct recommendations for scalability.
- () You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?
- () AWS CloudFront alerts
- () AWS Trusted Advisor alerts
- () AWS ElastiCache alerts
- () AWS Budget alerts
- () AWS Budget alerts is correct. The AWS Budget service can be configured with your budgets for all areas of cost. Alerts can be sent via email or stored in S3 buckets. CloudFront is used for CDN caching and ElastiCache is an in-memory caching service. Trusted Advisor analyzes your account and makes suggestions, but does not provide direct budgetary control.
- () What AWS database solution is best suited for data warehouse implementations?
- () EBS
- **() Redshift** [CORRECT]

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
AWS Budget alerts is correct. The AWS Budget service can be configured with your budgets for all areas of cost. Alerts can be sent via email or stored in S3 buckets. CloudFront is used for CDN caching and ElastiCache is an in-memory caching service. Trusted Advisor analyzes your account and makes suggestions, but does not provide direct budgetary control.

---

## Question 40

**Q:** You have been given control of an existing AWS environment (account). You want to ensure costs are being managed well. What tool should you run?

**Options:**
- (A) CloudFormation
- (B) Trusted Advisor
- (C) CloudTrail
- (D) CloudWatch
- (E) Trusted Advisor is correct. The Trusted Advisor can give recommendations for reducing costs, so this is the tool to run among those listed. CloudWatch monitors the AWS cloud. CloudTrail provides logging for activities in the cloud. CloudFormation is used to automatically deploy a solution.
- (F) Which one of the following is not something for which AWS Trusted Advisor makes recommendations?
- (G) Performance
- (H) Scalability
- (I) Fault Tolerance
- (J) Cost
- () Scalability is correct. Trusted advisor can make recommendations in the areas of cost, performance, fault tolerance, security, and service limits. It does not make direct recommendations for scalability.
- () You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?
- () AWS CloudFront alerts
- () AWS Trusted Advisor alerts
- () AWS ElastiCache alerts
- () AWS Budget alerts
- () AWS Budget alerts is correct. The AWS Budget service can be configured with your budgets for all areas of cost. Alerts can be sent via email or stored in S3 buckets. CloudFront is used for CDN caching and ElastiCache is an in-memory caching service. Trusted Advisor analyzes your account and makes suggestions, but does not provide direct budgetary control.
- () What AWS database solution is best suited for data warehouse implementations?
- () EBS
- **() Redshift** [CORRECT]
- () DynamoDB
- () Aurora
- () Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

---

## Question 41

**Q:** Which one of the following is not something for which AWS Trusted Advisor makes recommendations?

**Options:**
- (A) Performance
- (B) Scalability
- (C) Fault Tolerance
- (D) Cost
- (E) Scalability is correct. Trusted advisor can make recommendations in the areas of cost, performance, fault tolerance, security, and service limits. It does not make direct recommendations for scalability.
- (F) You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?
- (G) AWS CloudFront alerts
- (H) AWS Trusted Advisor alerts
- (I) AWS ElastiCache alerts
- (J) AWS Budget alerts
- () AWS Budget alerts is correct. The AWS Budget service can be configured with your budgets for all areas of cost. Alerts can be sent via email or stored in S3 buckets. CloudFront is used for CDN caching and ElastiCache is an in-memory caching service. Trusted Advisor analyzes your account and makes suggestions, but does not provide direct budgetary control.
- () What AWS database solution is best suited for data warehouse implementations?
- () EBS
- **() Redshift** [CORRECT]
- () DynamoDB
- () Aurora
- () Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

---

## Question 42

**Q:** You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?

**Options:**
- (A) AWS CloudFront alerts
- (B) AWS Trusted Advisor alerts
- (C) AWS ElastiCache alerts
- (D) AWS Budget alerts
- (E) AWS Budget alerts is correct. The AWS Budget service can be configured with your budgets for all areas of cost. Alerts can be sent via email or stored in S3 buckets. CloudFront is used for CDN caching and ElastiCache is an in-memory caching service. Trusted Advisor analyzes your account and makes suggestions, but does not provide direct budgetary control.
- (F) What AWS database solution is best suited for data warehouse implementations?
- (G) EBS
- **(H) Redshift** [CORRECT]
- (I) DynamoDB
- (J) Aurora
- () Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

---

## Question 43

**Q:** What AWS database solution is best suited for data warehouse implementations?

**Options:**
- (A) EBS
- **(B) Redshift** [CORRECT]
- (C) DynamoDB
- (D) Aurora
- (E) Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

---

## Question 44

**Q:** In addition to the proper configuration of RDS database settings, what can be done to improve overall performance of database operations?

**Options:**
- (A) Use better EFS implementations
- (B) Use fewer security groups
- (C) Tune SQL queries
- (D) Use better EBS volumes
- (E) Tune SQL queries is the correct answer. RDS databases do not provide storage-level access for EBS or EFS volumes, so you should consider tuning the SQL queries to improve overall performance. Security groups should not impact performance in operation.
- (F) Which one of the following components is used at a customer location to implement a site-to-site VPN connection with AWS?
- (G) Customer gateway
- (H) AWS VPN on-premises gateway
- (I) Virtual private gateway
- (J) Filtered firewall gateway
- () Customer gateway is the correct answer. The customer gateway is implemented on-premises at the customer location. The virtual private gateway (VPG) exists on the AWS cloud side of the VPN. Filtered firewall gateway and AWS CPN on-premises gateway are not terms used in association with AWS VPNs.
- () Which one of the following storage methods is object-based?
- () S3 Standard
- () EFS
- () VHD
- () EBS
- () S3 Standard is the correct answer. All S3 storage is object-based. EBS is block-based. VHD is used to import virtual machines as AWS Machine Images (AMIs). EFS is also block-based.
- () You’ve been commissioned to develop a high-availability application with a stateless web tier. Identify the most cost-effective means of reaching this goal.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of RDS.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of DynamoDB.
- **() Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and DynamoDB.** [CORRECT]
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 On-Demand instances (primary) running in tandem with an Auto Scaling group of EC2 Spot instances (secondary), and a multi-AZ deployment of RDS.
- () Incorrect Answers:
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 On-Demand instances (primary) running in tandem with an Auto Scaling group of EC2 Spot instances (secondary), and a multi-AZ deployment of RDS is incorrect because it uses EC2 On-Demand instances as the primary, which is going to spike the cost.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of RDS is incorrect because it uses RDS, which is going to increase the cost.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of DynamoDB is incorrect because it uses a multi-AZ deployment of DynamoDB, which is going to increase the cost. DynamoDB comes with built-in HA since it is a managed service.
- () Your security manager has hired a security contractor to audit your firewall implementation. When the consultant asks for the login details for the firewall appliance, which of the following might you do? (Choose two.)

**Answer:**
Correct Answer: **Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and DynamoDB.**

**Explanation:**
Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and DynamoDB is correct. With proper scripting and scaling policies, the On-Demand instances behind the Spot instances will deliver the most cost-effective solution because the On-Demand instances will only spin up if the Spot instances are not available. DynamoDB is a regional service; there is no need to explicitly create a multi-AZ deployment. RDS could be used, but DynamoDB lends itself better to supporting stateless web/app installations. 

---

## Question 45

**Q:** Which one of the following components is used at a customer location to implement a site-to-site VPN connection with AWS?

**Options:**
- (A) Customer gateway
- (B) AWS VPN on-premises gateway
- (C) Virtual private gateway
- (D) Filtered firewall gateway
- (E) Customer gateway is the correct answer. The customer gateway is implemented on-premises at the customer location. The virtual private gateway (VPG) exists on the AWS cloud side of the VPN. Filtered firewall gateway and AWS CPN on-premises gateway are not terms used in association with AWS VPNs.
- (F) Which one of the following storage methods is object-based?
- (G) S3 Standard
- (H) EFS
- (I) VHD
- (J) EBS
- () S3 Standard is the correct answer. All S3 storage is object-based. EBS is block-based. VHD is used to import virtual machines as AWS Machine Images (AMIs). EFS is also block-based.
- () You’ve been commissioned to develop a high-availability application with a stateless web tier. Identify the most cost-effective means of reaching this goal.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of RDS.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of DynamoDB.
- **() Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and DynamoDB.** [CORRECT]
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 On-Demand instances (primary) running in tandem with an Auto Scaling group of EC2 Spot instances (secondary), and a multi-AZ deployment of RDS.
- () Incorrect Answers:
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 On-Demand instances (primary) running in tandem with an Auto Scaling group of EC2 Spot instances (secondary), and a multi-AZ deployment of RDS is incorrect because it uses EC2 On-Demand instances as the primary, which is going to spike the cost.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of RDS is incorrect because it uses RDS, which is going to increase the cost.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of DynamoDB is incorrect because it uses a multi-AZ deployment of DynamoDB, which is going to increase the cost. DynamoDB comes with built-in HA since it is a managed service.
- () Your security manager has hired a security contractor to audit your firewall implementation. When the consultant asks for the login details for the firewall appliance, which of the following might you do? (Choose two.)
- () Correct selection
- () Tell him the details of the web application firewall.
- () Explain that AWS is a cloud service and that AWS manages the network appliances.
- () Create an IAM role with a policy that can read Security Group and Route settings.
- () Create an IAM role with a policy that can read Security Group and NACL settings.
- () Explain that AWS implements network security differently and that there is no such thing as a firewall appliance. Create an IAM user with a policy that can read Security Group and Route settings.
- () Correct Answers:
- () Tell him the details of the web application firewall and Explain that AWS implements network security differently and that there is no such thing as a firewall appliance. Create an IAM user with a policy that can read Security Group and Route settings are correct.
- () AWS has removed the firewall appliance from the hub of the network and implemented the firewall functionality as stateful Security Groups and stateless subnet NACLs. This is not a new concept in networking.
- () Create an IAM role with a policy that can read Security Group and Route settings is incorrect because you need to create a user with a policy and not a role with a policy.

**Answer:**
Correct Answer: **Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and DynamoDB.**

**Explanation:**
Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and DynamoDB is correct. With proper scripting and scaling policies, the On-Demand instances behind the Spot instances will deliver the most cost-effective solution because the On-Demand instances will only spin up if the Spot instances are not available. DynamoDB is a regional service; there is no need to explicitly create a multi-AZ deployment. RDS could be used, but DynamoDB lends itself better to supporting stateless web/app installations. 

---

## Question 46

**Q:** Which one of the following storage methods is object-based?

**Options:**
- (A) S3 Standard
- (B) EFS
- (C) VHD
- (D) EBS
- (E) S3 Standard is the correct answer. All S3 storage is object-based. EBS is block-based. VHD is used to import virtual machines as AWS Machine Images (AMIs). EFS is also block-based.
- (F) You’ve been commissioned to develop a high-availability application with a stateless web tier. Identify the most cost-effective means of reaching this goal.
- (G) Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of RDS.
- (H) Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of DynamoDB.
- (I) Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and DynamoDB.
- (J) Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 On-Demand instances (primary) running in tandem with an Auto Scaling group of EC2 Spot instances (secondary), and a multi-AZ deployment of RDS.
- () Incorrect Answers:
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 On-Demand instances (primary) running in tandem with an Auto Scaling group of EC2 Spot instances (secondary), and a multi-AZ deployment of RDS is incorrect because it uses EC2 On-Demand instances as the primary, which is going to spike the cost.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of RDS is incorrect because it uses RDS, which is going to increase the cost.
- () Use an Elastic Load Balancer, a multi-AZ deployment of an Auto Scaling group of EC2 Spot instances (primary) running in tandem with an Auto Scaling group of EC2 On-Demand instances (secondary), and a multi-AZ deployment of DynamoDB is incorrect because it uses a multi-AZ deployment of DynamoDB, which is going to increase the cost. DynamoDB comes with built-in HA since it is a managed service.
- () Your security manager has hired a security contractor to audit your firewall implementation. When the consultant asks for the login details for the firewall appliance, which of the following might you do? (Choose two.)
- () Correct selection
- () Tell him the details of the web application firewall.
- () Explain that AWS is a cloud service and that AWS manages the network appliances.
- () Create an IAM role with a policy that can read Security Group and Route settings.
- () Create an IAM role with a policy that can read Security Group and NACL settings.
- () Explain that AWS implements network security differently and that there is no such thing as a firewall appliance. Create an IAM user with a policy that can read Security Group and Route settings.
- () Correct Answers:
- () Tell him the details of the web application firewall and Explain that AWS implements network security differently and that there is no such thing as a firewall appliance. Create an IAM user with a policy that can read Security Group and Route settings are correct.
- () AWS has removed the firewall appliance from the hub of the network and implemented the firewall functionality as stateful Security Groups and stateless subnet NACLs. This is not a new concept in networking.
- () Create an IAM role with a policy that can read Security Group and Route settings is incorrect because you need to create a user with a policy and not a role with a policy.
- () Explain that AWS is a cloud service and that AWS manages the network appliances is incorrect because, although AWS manages the network appliance, you can still give the requested info to the security consultant.
- () Create an IAM role with a policy that can read Security Group and NACL settings is incorrect because the answer is incomplete.
- () What is the benefit of multipart upload?
- **() Greater success is achieved when uploading large files** [CORRECT]
- () Uploading multiple small files is faster
- () Support for concurrent application uploads is enabled
- () Network throughput is increased in every implementation
- () Greater success is achieved when uploading large files is the correct answer. When uploading large files (AWS recommends its use for files larger than 100 MB), successful uploads are increased. It does not provide benefit with multiple small files, concurrent application access, or increased network throughput in most scenarios.

**Answer:**
Correct Answer: **Greater success is achieved when uploading large files**

**Explanation:**
Greater success is achieved when uploading large files is the correct answer. When uploading large files (AWS recommends its use for files larger than 100 MB), successful uploads are increased. It does not provide benefit with multiple small files, concurrent application access, or increased network throughput in most scenarios.

---

## Question 47

**Q:** Your security manager has hired a security contractor to audit your firewall implementation. When the consultant asks for the login details for the firewall appliance, which of the following might you do? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Tell him the details of the web application firewall.
- (C) Explain that AWS is a cloud service and that AWS manages the network appliances.
- (D) Create an IAM role with a policy that can read Security Group and Route settings.
- (E) Create an IAM role with a policy that can read Security Group and NACL settings.
- (F) Explain that AWS implements network security differently and that there is no such thing as a firewall appliance. Create an IAM user with a policy that can read Security Group and Route settings.
- (G) Correct Answers:
- (H) Tell him the details of the web application firewall and Explain that AWS implements network security differently and that there is no such thing as a firewall appliance. Create an IAM user with a policy that can read Security Group and Route settings are correct.
- (I) AWS has removed the firewall appliance from the hub of the network and implemented the firewall functionality as stateful Security Groups and stateless subnet NACLs. This is not a new concept in networking.
- (J) Incorrect Answers:
- () Create an IAM role with a policy that can read Security Group and Route settings is incorrect because you need to create a user with a policy and not a role with a policy.
- () Explain that AWS is a cloud service and that AWS manages the network appliances is incorrect because, although AWS manages the network appliance, you can still give the requested info to the security consultant.
- () Create an IAM role with a policy that can read Security Group and NACL settings is incorrect because the answer is incomplete.
- () What is the benefit of multipart upload?
- () Greater success is achieved when uploading large files
- () Uploading multiple small files is faster
- () Support for concurrent application uploads is enabled
- () Network throughput is increased in every implementation
- () Greater success is achieved when uploading large files is the correct answer. When uploading large files (AWS recommends its use for files larger than 100 MB), successful uploads are increased. It does not provide benefit with multiple small files, concurrent application access, or increased network throughput in most scenarios.
- () What can be used to provide temporary access to perform a specific function within AWS and that will automatically expire without further action?
- **() Role** [CORRECT]
- () ACL
- () Standard group
- () Standard login
- () Role is the correct answer. Roles can be used as temporary identities. By default the granted role expires after 12 hours. While a standard login (user) could be used, it would not expire automatically. Groups also provide no solution to this scenario and neither do ACLs.

**Answer:**
Correct Answer: **Role**

**Explanation:**
Role is the correct answer. Roles can be used as temporary identities. By default the granted role expires after 12 hours. While a standard login (user) could be used, it would not expire automatically. Groups also provide no solution to this scenario and neither do ACLs.

---

## Question 48

**Q:** What is the benefit of multipart upload?

**Options:**
- (A) Greater success is achieved when uploading large files
- (B) Uploading multiple small files is faster
- (C) Support for concurrent application uploads is enabled
- (D) Network throughput is increased in every implementation
- (E) Greater success is achieved when uploading large files is the correct answer. When uploading large files (AWS recommends its use for files larger than 100 MB), successful uploads are increased. It does not provide benefit with multiple small files, concurrent application access, or increased network throughput in most scenarios.
- (F) What can be used to provide temporary access to perform a specific function within AWS and that will automatically expire without further action?
- **(G) Role** [CORRECT]
- (H) ACL
- (I) Standard group
- (J) Standard login
- () Role is the correct answer. Roles can be used as temporary identities. By default the granted role expires after 12 hours. While a standard login (user) could be used, it would not expire automatically. Groups also provide no solution to this scenario and neither do ACLs.

**Answer:**
Correct Answer: **Role**

**Explanation:**
Role is the correct answer. Roles can be used as temporary identities. By default the granted role expires after 12 hours. While a standard login (user) could be used, it would not expire automatically. Groups also provide no solution to this scenario and neither do ACLs.

---

## Question 49

**Q:** What can be used to provide temporary access to perform a specific function within AWS and that will automatically expire without further action?

**Options:**
- **(A) Role** [CORRECT]
- (B) ACL
- (C) Standard group
- (D) Standard login
- (E) Role is the correct answer. Roles can be used as temporary identities. By default the granted role expires after 12 hours. While a standard login (user) could be used, it would not expire automatically. Groups also provide no solution to this scenario and neither do ACLs.

**Answer:**
Correct Answer: **Role**

**Explanation:**
Role is the correct answer. Roles can be used as temporary identities. By default the granted role expires after 12 hours. While a standard login (user) could be used, it would not expire automatically. Groups also provide no solution to this scenario and neither do ACLs.

---

## Question 50

**Q:** You are creating a data lake in AWS, and one of the use cases for the data lake is batch jobs. Which AWS service would you use to ingest the data for batch jobs?

**Options:**
- (A) AWS Lambda
- (B) Kinesis Analytics
- (C) Kinesis Streams
- (D) Kinesis Firehose
- (E) Kinesis Firehose is correct. Since the use case is batch jobs, Kinesis Firehose should be used for data ingestion. 
- (F) Incorrect Answers:
- (G) Kinesis Streams is incorrect because Kinesis Steams is used to ingest real-time data and steams of data.
- (H) Kinesis Analytics is incorrect because Kinesis Analytics is used to transform the data at the time of ingestion.
- (I) AWS Lambda is incorrect because AWS Lambda is used to run your code, not to ingest the data. However, you can write a Lambda function to trigger the next step once the data ingestion is complete.
- (J) You are a consultant planning to deploy DynamoDB across three AZs. Your lead DBA is concerned about data consistency. Which of the following do you advise the lead DBA to do?
- () Ask the development team to code a maintenance task to run on a schedule to check consistency.
- () Ask the development team to write code to check for a successful completion code (200) at the completion of every write.
- () Ask the development team to code for strongly consistent reads, as this will impact the read times slightly but not the budget.
- () Ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost.
- () Ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost is correct. It is important to code for strong consistency. If you don’t code for strong consistency, you will end up having stale data, and depending on what you are trying to do, this may have an impact since you won’t be able to make decisions on real-time data. 
- () Ask the development team to write code to check for a successful completion code (200) at the completion of every write is incorrect because successful completion of the code doesn’t guarantee strongly consistent reads.
- () Ask the development team to code for strongly consistent reads, as this will impact the read times slightly but not the budget is incorrect because it impacts the budget.
- () Ask the development team to code a maintenance task to run on a schedule to check consistency is incorrect because a maintenance task will only check for consistency but won’t fix it.
- () What can you monitor to see if a T2 database instance should be upgraded to an R3 instance?
- () Memory allowance
- () CPU allowance
- () Memory credits
- () CPU credits
- () CPU credits is the correct answer. By monitoring CPU credits you can determine if you're reaching a low level of credits. When a low level of credits is reached, you risk running out of credits and, in such an instance, performance will degrade significantly.
- () How does AWS deliver high durability for DynamoDB?
- () AWS maintains a schedule of incremental backups and log shipping.
- **() DynamoDB data is automatically replicated across multiple AZs.** [CORRECT]
- () DynamoDB supports user snapshots to S3.
- () DynamoDB is a NoSQL database.
- () DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.
- () AWS maintains a schedule of incremental backups and log shipping is incorrect because this option doesn’t increase the durability.

**Answer:**
Correct Answer: **DynamoDB data is automatically replicated across multiple AZs.**

**Explanation:**
DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.

---

## Question 51

**Q:** You are a consultant planning to deploy DynamoDB across three AZs. Your lead DBA is concerned about data consistency. Which of the following do you advise the lead DBA to do?

**Options:**
- (A) Ask the development team to code a maintenance task to run on a schedule to check consistency.
- (B) Ask the development team to write code to check for a successful completion code (200) at the completion of every write.
- (C) Ask the development team to code for strongly consistent reads, as this will impact the read times slightly but not the budget.
- (D) Ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost.
- (E) Ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost is correct. It is important to code for strong consistency. If you don’t code for strong consistency, you will end up having stale data, and depending on what you are trying to do, this may have an impact since you won’t be able to make decisions on real-time data. 
- (F) Incorrect Answers:
- (G) Ask the development team to write code to check for a successful completion code (200) at the completion of every write is incorrect because successful completion of the code doesn’t guarantee strongly consistent reads.
- (H) Ask the development team to code for strongly consistent reads, as this will impact the read times slightly but not the budget is incorrect because it impacts the budget.
- (I) Ask the development team to code a maintenance task to run on a schedule to check consistency is incorrect because a maintenance task will only check for consistency but won’t fix it.
- (J) What can you monitor to see if a T2 database instance should be upgraded to an R3 instance?
- () Memory allowance
- () CPU allowance
- () Memory credits
- () CPU credits
- () CPU credits is the correct answer. By monitoring CPU credits you can determine if you're reaching a low level of credits. When a low level of credits is reached, you risk running out of credits and, in such an instance, performance will degrade significantly.
- () How does AWS deliver high durability for DynamoDB?
- () AWS maintains a schedule of incremental backups and log shipping.
- **() DynamoDB data is automatically replicated across multiple AZs.** [CORRECT]
- () DynamoDB supports user snapshots to S3.
- () DynamoDB is a NoSQL database.
- () DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.
- () AWS maintains a schedule of incremental backups and log shipping is incorrect because this option doesn’t increase the durability.
- () DynamoDB supports user snapshots to S3 is incorrect because a snapshot doesn’t help in delivering the durability.

**Answer:**
Correct Answer: **DynamoDB data is automatically replicated across multiple AZs.**

**Explanation:**
DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.

---

## Question 52

**Q:** What can you monitor to see if a T2 database instance should be upgraded to an R3 instance?

**Options:**
- (A) Memory allowance
- (B) CPU allowance
- (C) Memory credits
- (D) CPU credits
- (E) CPU credits is the correct answer. By monitoring CPU credits you can determine if you're reaching a low level of credits. When a low level of credits is reached, you risk running out of credits and, in such an instance, performance will degrade significantly.
- (F) How does AWS deliver high durability for DynamoDB?
- (G) AWS maintains a schedule of incremental backups and log shipping.
- **(H) DynamoDB data is automatically replicated across multiple AZs.** [CORRECT]
- (I) DynamoDB supports user snapshots to S3.
- (J) DynamoDB is a NoSQL database.
- () DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.
- () Incorrect Answers:
- () AWS maintains a schedule of incremental backups and log shipping is incorrect because this option doesn’t increase the durability.
- () DynamoDB supports user snapshots to S3 is incorrect because a snapshot doesn’t help in delivering the durability.

**Answer:**
Correct Answer: **DynamoDB data is automatically replicated across multiple AZs.**

**Explanation:**
DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.

---

## Question 53

**Q:** How does AWS deliver high durability for DynamoDB?

**Options:**
- (A) AWS maintains a schedule of incremental backups and log shipping.
- **(B) DynamoDB data is automatically replicated across multiple AZs.** [CORRECT]
- (C) DynamoDB supports user snapshots to S3.
- (D) DynamoDB is a NoSQL database.
- (E) DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.
- (F) Incorrect Answers:
- (G) AWS maintains a schedule of incremental backups and log shipping is incorrect because this option doesn’t increase the durability.
- (H) DynamoDB supports user snapshots to S3 is incorrect because a snapshot doesn’t help in delivering the durability.

**Answer:**
Correct Answer: **DynamoDB data is automatically replicated across multiple AZs.**

**Explanation:**
DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.

---

## Question 54

**Q:** When implementing ELB, what should you ensure such that high availability is achieved?

**Options:**
- (A) Resources are in multiple Availability Zones
- (B) Resources are in one region
- (C) ELB is implemented in one region
- (D) ELB is implemented in one Availability Zone
- (E) Resources are in multiple Availability Zones is correct. By implementing resources to which ELB will forward requests in multiple Availability Zones, you ensure high availability. ELB provides Elastic Load Balancing.
- (F) You have been asked by your employer to create an identical copy of your production environment in another region for disaster recovery purposes. Which of the following AWS resources would you NOT need to re-create because they are available universally across the console? (Choose two.)
- (G) Correct selection
- (H) Route 53
- (I) Elastic Load Balancers
- (J) Identity Access Management roles
- () Security groups
- () EC2 key pairs
- () Correct Answers:
- () Route 53 and Identity Access Management roles are correct. Route 53 and IAM are global services, so it does not matter which region you choose because you can leverage them globally. Conversely, ELB, security groups, and EC2 key pairs are tied to a particular region. 
- () Incorrect Answers:
- () Elastic Load Balancers is incorrect because ELB is a regional service.
- () Security groups is incorrect because security groups are tied to a particular region.
- () EC2 key pairs is incorrect because EC2 key pairs are tied to a particular region.
- () What tool is provided by AWS to compare the cost of locally-implemented solutions with AWS cloud-hosted solutions?
- () AWS Trusted Advisor
- () AWS Simple Monthly Calculator
- () AWS TCO Calculator
- () AWS Budget
- () When should RDS backups occur for best performance results?
- () During times of zero activity
- () During the busiest time of the day
- **() During times of normally low write IOPS** [CORRECT]
- () During times of medium read operations
- () During times of normally low write IOPS is correct. Because few database systems that are placed online have times of zero activity, the best time window to search for is that in which low write IOPS are seen traditionally.

**Answer:**
Correct Answer: **During times of normally low write IOPS**

**Explanation:**
During times of normally low write IOPS is correct. Because few database systems that are placed online have times of zero activity, the best time window to search for is that in which low write IOPS are seen traditionally.

---

## Question 55

**Q:** You have been asked by your employer to create an identical copy of your production environment in another region for disaster recovery purposes. Which of the following AWS resources would you NOT need to re-create because they are available universally across the console? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Route 53
- (C) Elastic Load Balancers
- (D) Identity Access Management roles
- (E) Security groups
- (F) EC2 key pairs
- (G) Correct Answers:
- (H) Route 53 and Identity Access Management roles are correct. Route 53 and IAM are global services, so it does not matter which region you choose because you can leverage them globally. Conversely, ELB, security groups, and EC2 key pairs are tied to a particular region. 
- (I) Incorrect Answers:
- (J) Elastic Load Balancers is incorrect because ELB is a regional service.
- () Security groups is incorrect because security groups are tied to a particular region.
- () EC2 key pairs is incorrect because EC2 key pairs are tied to a particular region.
- () What tool is provided by AWS to compare the cost of locally-implemented solutions with AWS cloud-hosted solutions?
- () AWS Trusted Advisor
- () AWS Simple Monthly Calculator
- () AWS TCO Calculator
- () AWS Budget
- () When should RDS backups occur for best performance results?
- () During times of zero activity
- () During the busiest time of the day
- () During times of normally low write IOPS
- () During times of medium read operations
- () During times of normally low write IOPS is correct. Because few database systems that are placed online have times of zero activity, the best time window to search for is that in which low write IOPS are seen traditionally.
- () How is the public IP address managed in an instance session via the instance GUI/RDP or Terminal/SSH session?
- **() The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address.** [CORRECT]
- () For security reasons, the public IP address is a hidden value.
- () The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4.
- () The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4.
- () The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address is correct. When you manage the public IP address in an instance session via the instance GUI/RDP or Terminal/SSH session, it is not managed on the instance. In this case, an alias is applied as a network address translator of the private IP address. 
- () The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4, The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4, and For security reasons, the public IP address is a hidden value are incorrect.

**Answer:**
Correct Answer: **The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address.**

**Explanation:**
The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address is correct. When you manage the public IP address in an instance session via the instance GUI/RDP or Terminal/SSH session, it is not managed on the instance. In this case, an alias is applied as a network address translator of the private IP address. 

---

## Question 56

**Q:** What tool is provided by AWS to compare the cost of locally-implemented solutions with AWS cloud-hosted solutions?

**Options:**
- (A) AWS Trusted Advisor
- (B) AWS Simple Monthly Calculator
- (C) AWS TCO Calculator
- (D) AWS Budget
- (E) When should RDS backups occur for best performance results?
- (F) During times of zero activity
- (G) During the busiest time of the day
- (H) During times of normally low write IOPS
- (I) During times of medium read operations
- (J) During times of normally low write IOPS is correct. Because few database systems that are placed online have times of zero activity, the best time window to search for is that in which low write IOPS are seen traditionally.
- () How is the public IP address managed in an instance session via the instance GUI/RDP or Terminal/SSH session?
- () The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address.
- () For security reasons, the public IP address is a hidden value.
- () The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4.
- () The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4.
- () The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address is correct. When you manage the public IP address in an instance session via the instance GUI/RDP or Terminal/SSH session, it is not managed on the instance. In this case, an alias is applied as a network address translator of the private IP address. 
- () Incorrect Answers:
- () The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4, The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4, and For security reasons, the public IP address is a hidden value are incorrect.
- () What kind of storage is used with EBS volumes?
- **() Block storage** [CORRECT]
- () Only magnetic disk storage
- () Object storage
- () Only SSD storage
- () Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

**Answer:**
Correct Answer: **Block storage**

**Explanation:**
Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

---

## Question 57

**Q:** When should RDS backups occur for best performance results?

**Options:**
- (A) During times of zero activity
- (B) During the busiest time of the day
- (C) During times of normally low write IOPS
- (D) During times of medium read operations
- (E) During times of normally low write IOPS is correct. Because few database systems that are placed online have times of zero activity, the best time window to search for is that in which low write IOPS are seen traditionally.
- (F) How is the public IP address managed in an instance session via the instance GUI/RDP or Terminal/SSH session?
- (G) The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address.
- (H) For security reasons, the public IP address is a hidden value.
- (I) The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4.
- (J) The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4.
- () The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address is correct. When you manage the public IP address in an instance session via the instance GUI/RDP or Terminal/SSH session, it is not managed on the instance. In this case, an alias is applied as a network address translator of the private IP address. 
- () Incorrect Answers:
- () The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4, The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4, and For security reasons, the public IP address is a hidden value are incorrect.
- () What kind of storage is used with EBS volumes?
- **() Block storage** [CORRECT]
- () Only magnetic disk storage
- () Object storage
- () Only SSD storage
- () Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

**Answer:**
Correct Answer: **Block storage**

**Explanation:**
Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

---

## Question 58

**Q:** How is the public IP address managed in an instance session via the instance GUI/RDP or Terminal/SSH session?

**Options:**
- (A) The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address.
- (B) For security reasons, the public IP address is a hidden value.
- (C) The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4.
- (D) The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4.
- (E) The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address is correct. When you manage the public IP address in an instance session via the instance GUI/RDP or Terminal/SSH session, it is not managed on the instance. In this case, an alias is applied as a network address translator of the private IP address. 
- (F) Incorrect Answers:
- (G) The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4, The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4, and For security reasons, the public IP address is a hidden value are incorrect.
- (H) What kind of storage is used with EBS volumes?
- **(I) Block storage** [CORRECT]
- (J) Only magnetic disk storage
- () Object storage
- () Only SSD storage
- () Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

**Answer:**
Correct Answer: **Block storage**

**Explanation:**
Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

---

## Question 59

**Q:** What kind of storage is used with EBS volumes?

**Options:**
- **(A) Block storage** [CORRECT]
- (B) Only magnetic disk storage
- (C) Object storage
- (D) Only SSD storage
- (E) Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

**Answer:**
Correct Answer: **Block storage**

**Explanation:**
Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

---

## Question 60

**Q:** You receive a ProvisionedThroughputExceededException error. However, the DynamoDB metrics show that your table or index has not been operating at maximum provisioned throughput. What could this error be caused by?

**Options:**
- (A) The error is caused by excess traffic generated by your local secondary indexes. You should provision units specifically to the local secondary indexes.
- (B) It is only a warning. DynamoDB’s burst capacity will handle the extra traffic.
- (C) It is a transitory error. AWS will adjust the table to accommodate it and reprocess the transaction.
- (D) The throughput is not balanced across your partitions. One partition is being subjected to a disproportionate amount of the traffic and is therefore exceeding the limits.
- (E) Incorrect Answers:
- (F) The error is caused by excess traffic generated by your local secondary indexes. You should provision units specifically to the local secondary indexes is incorrect because the error is about throughput and not excess traffic.
- (G) It is a transitory error. AWS will adjust the table to accommodate it and reprocess the transaction is incorrect because this is not a transitory error.
- (H) Which instance type runs on hardware allocated to a single customer?
- (I) Reserved instance
- (J) On Demand instance
- () Dedicated instance
- () EC2 spot instance
- () Dedicated instance is correct. A dedicated instance runs on hardware allocated to a single customer. The dedicated instances are physically isolated at the host hardware level from instances that belong to other AWS accounts.
- () EC2 spot instance is incorrect because a spot instance can be run in a shared VM.
- () Reserved instance and On Demand instance are incorrect because Reserved and On Demand are pricing mechanisms.
- () What HTTP response is given upon a successful upload of a file to an S3 bucket?
- **() 200** [CORRECT]
- () 500
- () 400
- () 300
- () 200 is the correct answer. HTTP 200 is the success response code. HTTP 500 indicates an internal server error. HTTP 300 indicates a redirect of some kind. HTTP 400 is a missing object response code.

**Answer:**
Correct Answer: **200**

**Explanation:**
200 is the correct answer. HTTP 200 is the success response code. HTTP 500 indicates an internal server error. HTTP 300 indicates a redirect of some kind. HTTP 400 is a missing object response code.

---

## Question 61

**Q:** Which instance type runs on hardware allocated to a single customer?

**Options:**
- (A) Reserved instance
- (B) On Demand instance
- (C) Dedicated instance
- (D) EC2 spot instance
- (E) Dedicated instance is correct. A dedicated instance runs on hardware allocated to a single customer. The dedicated instances are physically isolated at the host hardware level from instances that belong to other AWS accounts.
- (F) Incorrect Answers:
- (G) EC2 spot instance is incorrect because a spot instance can be run in a shared VM.
- (H) Reserved instance and On Demand instance are incorrect because Reserved and On Demand are pricing mechanisms.
- (I) What HTTP response is given upon a successful upload of a file to an S3 bucket?
- **(J) 200** [CORRECT]
- () 500
- () 400
- () 300
- () 200 is the correct answer. HTTP 200 is the success response code. HTTP 500 indicates an internal server error. HTTP 300 indicates a redirect of some kind. HTTP 400 is a missing object response code.

**Answer:**
Correct Answer: **200**

**Explanation:**
200 is the correct answer. HTTP 200 is the success response code. HTTP 500 indicates an internal server error. HTTP 300 indicates a redirect of some kind. HTTP 400 is a missing object response code.

---

## Question 62

**Q:** What HTTP response is given upon a successful upload of a file to an S3 bucket?

**Options:**
- **(A) 200** [CORRECT]
- (B) 500
- (C) 400
- (D) 300
- (E) 200 is the correct answer. HTTP 200 is the success response code. HTTP 500 indicates an internal server error. HTTP 300 indicates a redirect of some kind. HTTP 400 is a missing object response code.

**Answer:**
Correct Answer: **200**

**Explanation:**
200 is the correct answer. HTTP 200 is the success response code. HTTP 500 indicates an internal server error. HTTP 300 indicates a redirect of some kind. HTTP 400 is a missing object response code.

---

## Question 63

**Q:** What is used to cache, or store, data and connect with S3 buckets from the on-premises customer location?

**Options:**
- (A) Storage gateway
- (B) NAC gateway
- (C) Customer gateway
- (D) Virtual private gateway
- (E) Storage gateway is the correct answer. The storage gateway is used to connect the customer location to an S3 bucket and to cache and store data locally for faster access. The customer and virtual private gateways are used to establish VPNs. No such entity as a NAC gateway exists in association with AWS.
- (F) When using an encrypted EBS volume, what type of data is encrypted automatically? (Choose the single best answer.)
- (G) All data stored on the volume
- (H) User documents
- (I) Database files
- (J) Configuration data
- () All data stored on the volume is the correct answer. Encrypted EBS volumes encrypt all data stored on the volume regardless of data type.
- () Dump 2
- () You have five elastic IP addresses in a region. How many more can you create within that region without contacting support to request more?
- **() 0** [CORRECT]
- () 0 is the correct answer. The default limit is five per region. Therefore, with five already created, you cannot create any more without requesting an extension.
- () Your server logs are full of what appear to be application-layer attacks, so you deploy AWS Web Application Firewall. Which of the following conditions can you set when configuring AWS WAF? (Choose three.)
- () Correct selection
- () String match conditions
- () Termination conditions
- () IP match conditions
- () URL match conditions
- () SQL rejection match conditions
- () Size constraint conditions
- () Correct Answers:
- () String match conditions, Size constraint conditions, and IP match conditions are correct. In AWS WAF, you can set string match, IP match, and size constraint conditions. 
- () Incorrect Answers:
- () URL match conditions, Termination conditions, and SQL rejection match conditions are incorrect because these conditions are not options in WAF.

**Answer:**
Correct Answer: **0**

**Explanation:**
0 is the correct answer. The default limit is five per region. Therefore, with five already created, you cannot create any more without requesting an extension.

---

## Question 64

**Q:** When using an encrypted EBS volume, what type of data is encrypted automatically? (Choose the single best answer.)

**Options:**
- (A) All data stored on the volume
- (B) User documents
- (C) Database files
- (D) Configuration data
- (E) All data stored on the volume is the correct answer. Encrypted EBS volumes encrypt all data stored on the volume regardless of data type.
- (F) Dump 2
- (G) You have five elastic IP addresses in a region. How many more can you create within that region without contacting support to request more?
- (H) 0
- (I) 0 is the correct answer. The default limit is five per region. Therefore, with five already created, you cannot create any more without requesting an extension.
- (J) Your server logs are full of what appear to be application-layer attacks, so you deploy AWS Web Application Firewall. Which of the following conditions can you set when configuring AWS WAF? (Choose three.)
- () Correct selection
- () String match conditions
- () Termination conditions
- () IP match conditions
- () URL match conditions
- () SQL rejection match conditions
- () Size constraint conditions
- () Correct Answers:
- () String match conditions, Size constraint conditions, and IP match conditions are correct. In AWS WAF, you can set string match, IP match, and size constraint conditions. 
- () Incorrect Answers:
- () URL match conditions, Termination conditions, and SQL rejection match conditions are incorrect because these conditions are not options in WAF.
- () You want to perform business analytics against a large data set (several terabytes). What AWS-managed service provides such functionality?
- () DynamoDB
- () ElastiCache
- () CodeDeploy
- **() Redshift** [CORRECT]
- () Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

---

## Question 65

**Q:** You have five elastic IP addresses in a region. How many more can you create within that region without contacting support to request more?

**Options:**
- (A) 0
- (B) 0 is the correct answer. The default limit is five per region. Therefore, with five already created, you cannot create any more without requesting an extension.
- (C) Your server logs are full of what appear to be application-layer attacks, so you deploy AWS Web Application Firewall. Which of the following conditions can you set when configuring AWS WAF? (Choose three.)
- (D) Correct selection
- (E) String match conditions
- (F) Termination conditions
- (G) IP match conditions
- (H) URL match conditions
- (I) SQL rejection match conditions
- (J) Size constraint conditions
- () Correct Answers:
- () String match conditions, Size constraint conditions, and IP match conditions are correct. In AWS WAF, you can set string match, IP match, and size constraint conditions. 
- () Incorrect Answers:
- () URL match conditions, Termination conditions, and SQL rejection match conditions are incorrect because these conditions are not options in WAF.
- () You want to perform business analytics against a large data set (several terabytes). What AWS-managed service provides such functionality?
- () DynamoDB
- () ElastiCache
- () CodeDeploy
- **() Redshift** [CORRECT]
- () Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

---

## Question 66

**Q:** Your server logs are full of what appear to be application-layer attacks, so you deploy AWS Web Application Firewall. Which of the following conditions can you set when configuring AWS WAF? (Choose three.)

**Options:**
- (A) Correct selection
- (B) String match conditions
- (C) Termination conditions
- (D) IP match conditions
- (E) URL match conditions
- (F) SQL rejection match conditions
- (G) Size constraint conditions
- (H) Correct Answers:
- (I) String match conditions, Size constraint conditions, and IP match conditions are correct. In AWS WAF, you can set string match, IP match, and size constraint conditions. 
- (J) Incorrect Answers:
- () URL match conditions, Termination conditions, and SQL rejection match conditions are incorrect because these conditions are not options in WAF.
- () You want to perform business analytics against a large data set (several terabytes). What AWS-managed service provides such functionality?
- () DynamoDB
- () ElastiCache
- () CodeDeploy
- **() Redshift** [CORRECT]
- () Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

---

## Question 67

**Q:** You want to perform business analytics against a large data set (several terabytes). What AWS-managed service provides such functionality?

**Options:**
- (A) DynamoDB
- (B) ElastiCache
- (C) CodeDeploy
- **(D) Redshift** [CORRECT]
- (E) Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

**Answer:**
Correct Answer: **Redshift**

**Explanation:**
Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

---

## Question 68

**Q:** Even if all best practices are being followed in IAM administration, what can present vulnerabilities related to your EC2 instances?

**Options:**
- (A) Improper IAM group usage
- (B) Improper IAM user account creation
- (C) OS security issues within the instances
- (D) Improper IAM role usage
- (E) For what purpose is the Elastic Transcoder used?
- (F) To recode text submitted to S3 buckets
- (G) To convert currencies from different nations
- (H) To stream video to client devices from the cloud
- (I) To convert media formats and sizes for different target devices and systems
- (J) To convert media formats and sizes for different target devices and systems is the correct answer. The Elastic Transcoder is a media transcoder in the cloud. It can convert to different media formats and sizes so that media is available for various target devices and systems.
- () What is likely to occur during the time required to take a snapshot of a Cold HDD or Throughput-Optimized HDD EBS volume?
- () Performance will be degraded
- () Data will be lost
- () Performance will be improved
- () Data will be decrypted
- () Performance will be degraded is the correct answer. During the creation of the snapshot on magnetic storage, performance will be degraded due to the method used to access the blocks. Data will not be decrypted or lost.
- () You are responsible for planning EFS implementation in AWS. What is the default limit on the number of EFS file systems that can be created per account?
- **() 10** [CORRECT]
- () Unlimited
- () 10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

**Answer:**
Correct Answer: **10**

**Explanation:**
10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

---

## Question 69

**Q:** For what purpose is the Elastic Transcoder used?

**Options:**
- (A) To recode text submitted to S3 buckets
- (B) To convert currencies from different nations
- (C) To stream video to client devices from the cloud
- (D) To convert media formats and sizes for different target devices and systems
- (E) To convert media formats and sizes for different target devices and systems is the correct answer. The Elastic Transcoder is a media transcoder in the cloud. It can convert to different media formats and sizes so that media is available for various target devices and systems.
- (F) What is likely to occur during the time required to take a snapshot of a Cold HDD or Throughput-Optimized HDD EBS volume?
- (G) Performance will be degraded
- (H) Data will be lost
- (I) Performance will be improved
- (J) Data will be decrypted
- () Performance will be degraded is the correct answer. During the creation of the snapshot on magnetic storage, performance will be degraded due to the method used to access the blocks. Data will not be decrypted or lost.
- () You are responsible for planning EFS implementation in AWS. What is the default limit on the number of EFS file systems that can be created per account?
- **() 10** [CORRECT]
- () Unlimited
- () 10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

**Answer:**
Correct Answer: **10**

**Explanation:**
10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

---

## Question 70

**Q:** What is likely to occur during the time required to take a snapshot of a Cold HDD or Throughput-Optimized HDD EBS volume?

**Options:**
- (A) Performance will be degraded
- (B) Data will be lost
- (C) Performance will be improved
- (D) Data will be decrypted
- (E) Performance will be degraded is the correct answer. During the creation of the snapshot on magnetic storage, performance will be degraded due to the method used to access the blocks. Data will not be decrypted or lost.
- (F) You are responsible for planning EFS implementation in AWS. What is the default limit on the number of EFS file systems that can be created per account?
- **(G) 10** [CORRECT]
- (H) Unlimited
- (I) 10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

**Answer:**
Correct Answer: **10**

**Explanation:**
10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

---

## Question 71

**Q:** You are responsible for planning EFS implementation in AWS. What is the default limit on the number of EFS file systems that can be created per account?

**Options:**
- **(A) 10** [CORRECT]
- (B) Unlimited
- (C) 10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

**Answer:**
Correct Answer: **10**

**Explanation:**
10 is the correct answer. The default limit on EFS file systems is 10. This can be increased by opening a support ticket with AWS.

---

## Question 72

**Q:** Your company has hired a young and enthusiastic accountant. After reviewing the AWS documentation and usage graphs, he announces that you are wasting vast amounts of the company’s money running servers for a full hour instead of spinning them up only when they are needed and down again as soon as they are idle for 1 minute. He cites the AWS claim that you only pay for what you use, and that as a senior engineer, you should be more conscious of wasting company money. How do you respond?

**Options:**
- (A) You thank him for his concern and then implement EC2’s pay-per-minute billing to get the maximum benefit for the company.
- (B) You leap across the meeting table and slap him for insulting you in front of your peers.
- (C) You grudgingly acknowledge his point and change your scheduling and tuning settings.
- (D) You acknowledge the problem and propose that you could downsize the instances so that the workload consumes the full instance capacity for the full hour. You also propose closer monitoring and automation so that you can upsize and/or downsize the instance each hour during the day to match the instance performance to the anticipated workload.
- (E) You thank him for his concern and then implement EC2’s pay-per-minute billing to get the maximum benefit for the company is correct. AWS has launched a new feature called pay-per-minute, where the billing occurs in increments of 60 seconds for certain types of instances. If cost control is one of your main objectives, it makes sense to stop the instance whenever it is not in use. 
- (F) Incorrect Answers:
- (G) You leap across the meeting table and slap him for insulting you in front of your peers is incorrect because in real life you would never do this.
- (H) You leap across the meeting table and slap him for insulting you in front of your peers is incorrect because changing the scheduling won’t help in reducing the cost.
- (I) You acknowledge the problem and propose that you could downsize the instances so that the workload consumes the full instance capacity for the full hour. You also propose closer monitoring and automation so that you can upsize and/or downsize the instance each hour during the day to match the instance performance to the anticipated workload is incorrect because changing the instance size won’t help to reduce the bill if the server is idle for more than a minute.
- (J) What AWS service allows you to run code in the AWS cloud without provisioning any of the underlying resources required for code execution?
- () Aurora
- () VPC
- () EC2
- () Lambda
- () Lambda is the correct answer. Lambda is an AWS service that allows you to execute code without provisioning resources. Aurora is an AWS database. Virtual Private Cloud (VPC) is a container in which you place instances and control access to them. EC2 is used to launch AMI instances within VPCs in AWS.
- () How much data can be downloaded from an S3 bucket to your local network with no transfer charges?
- () From 1 GB/Month to 9.999 TB/Month
- () Up to 1 GB/Month
- () From 10 TB/Month to 40 TB/Month
- () From 40 TB/Month to 100 TB/Month
- () Up to 1GB/Month is the correct answer. There is no cost for uploading to EC2 instances from the Internet (your local network); however, there is a cost for downloading to the Internet (your local network). For example, with approximately 100 GB of transfer down to your local network per month, the cost would be approximately $9 per month in 2020. There is no cost for encryption/decryption that can be estimated beyond increase compute cycles, which are typically minimal.
- () What is the minimum volume size of a Provisioned IOPS SSD EBS volume?
- **() 4 GiB** [CORRECT]
- () 16 TiB
- () 1 TiB
- () 12 GiB
- () The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.
- () A client is concerned that someone other than approved administrators is trying to gain access to the Linux web app instances in their VPC. The client asks what sort of network access logging can be added. Which of the following might you recommend? (Choose two.)

**Answer:**
Correct Answer: **4 GiB**

**Explanation:**
The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.

---

## Question 73

**Q:** What AWS service allows you to run code in the AWS cloud without provisioning any of the underlying resources required for code execution?

**Options:**
- (A) Aurora
- (B) VPC
- (C) EC2
- (D) Lambda
- (E) Lambda is the correct answer. Lambda is an AWS service that allows you to execute code without provisioning resources. Aurora is an AWS database. Virtual Private Cloud (VPC) is a container in which you place instances and control access to them. EC2 is used to launch AMI instances within VPCs in AWS.
- (F) How much data can be downloaded from an S3 bucket to your local network with no transfer charges?
- (G) From 1 GB/Month to 9.999 TB/Month
- (H) Up to 1 GB/Month
- (I) From 10 TB/Month to 40 TB/Month
- (J) From 40 TB/Month to 100 TB/Month
- () Up to 1GB/Month is the correct answer. There is no cost for uploading to EC2 instances from the Internet (your local network); however, there is a cost for downloading to the Internet (your local network). For example, with approximately 100 GB of transfer down to your local network per month, the cost would be approximately $9 per month in 2020. There is no cost for encryption/decryption that can be estimated beyond increase compute cycles, which are typically minimal.
- () What is the minimum volume size of a Provisioned IOPS SSD EBS volume?
- **() 4 GiB** [CORRECT]
- () 16 TiB
- () 1 TiB
- () 12 GiB
- () The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.
- () A client is concerned that someone other than approved administrators is trying to gain access to the Linux web app instances in their VPC. The client asks what sort of network access logging can be added. Which of the following might you recommend? (Choose two.)
- () Use Event Log filters to trigger alerts that are forwarded to CloudWatch.
- () Correct selection
- () Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3.
- () Set up a Flow Log for the group of instances and forward them to CloudWatch.
- () Set up a traffic-logging rule on the VPC firewall appliance and direct the log to CloudWatch or S3.
- () Set up a Flow Log for the group of instances and forward them to S3.
- () Correct Answers:
- () Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3 and Set up a Flow Log for the group of instances and forward them to CloudWatch are correct. Since someone is trying to get into the web tier and the app tier, you have to analyze the logs from the operating system, and the Flow Log is going to give you all the information you are looking for. 
- () Incorrect Answers:
- () Use Event Log filters to trigger alerts that are forwarded to CloudWatch is incorrect because the Event Log won’t provide you the required information.

**Answer:**
Correct Answer: **4 GiB**

**Explanation:**
The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.

---

## Question 74

**Q:** How much data can be downloaded from an S3 bucket to your local network with no transfer charges?

**Options:**
- (A) From 1 GB/Month to 9.999 TB/Month
- (B) Up to 1 GB/Month
- (C) From 10 TB/Month to 40 TB/Month
- (D) From 40 TB/Month to 100 TB/Month
- (E) Up to 1GB/Month is the correct answer. There is no cost for uploading to EC2 instances from the Internet (your local network); however, there is a cost for downloading to the Internet (your local network). For example, with approximately 100 GB of transfer down to your local network per month, the cost would be approximately $9 per month in 2020. There is no cost for encryption/decryption that can be estimated beyond increase compute cycles, which are typically minimal.
- (F) What is the minimum volume size of a Provisioned IOPS SSD EBS volume?
- **(G) 4 GiB** [CORRECT]
- (H) 16 TiB
- (I) 1 TiB
- (J) 12 GiB
- () The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.
- () A client is concerned that someone other than approved administrators is trying to gain access to the Linux web app instances in their VPC. The client asks what sort of network access logging can be added. Which of the following might you recommend? (Choose two.)
- () Use Event Log filters to trigger alerts that are forwarded to CloudWatch.
- () Correct selection
- () Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3.
- () Set up a Flow Log for the group of instances and forward them to CloudWatch.
- () Set up a traffic-logging rule on the VPC firewall appliance and direct the log to CloudWatch or S3.
- () Set up a Flow Log for the group of instances and forward them to S3.
- () Correct Answers:
- () Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3 and Set up a Flow Log for the group of instances and forward them to CloudWatch are correct. Since someone is trying to get into the web tier and the app tier, you have to analyze the logs from the operating system, and the Flow Log is going to give you all the information you are looking for. 
- () Incorrect Answers:
- () Use Event Log filters to trigger alerts that are forwarded to CloudWatch is incorrect because the Event Log won’t provide you the required information.

**Answer:**
Correct Answer: **4 GiB**

**Explanation:**
The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.

---

## Question 75

**Q:** What is the minimum volume size of a Provisioned IOPS SSD EBS volume?

**Options:**
- **(A) 4 GiB** [CORRECT]
- (B) 16 TiB
- (C) 1 TiB
- (D) 12 GiB
- (E) The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.
- (F) A client is concerned that someone other than approved administrators is trying to gain access to the Linux web app instances in their VPC. The client asks what sort of network access logging can be added. Which of the following might you recommend? (Choose two.)
- (G) Use Event Log filters to trigger alerts that are forwarded to CloudWatch.
- (H) Correct selection
- (I) Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3.
- (J) Set up a Flow Log for the group of instances and forward them to CloudWatch.
- () Set up a traffic-logging rule on the VPC firewall appliance and direct the log to CloudWatch or S3.
- () Set up a Flow Log for the group of instances and forward them to S3.
- () Correct Answers:
- () Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3 and Set up a Flow Log for the group of instances and forward them to CloudWatch are correct. Since someone is trying to get into the web tier and the app tier, you have to analyze the logs from the operating system, and the Flow Log is going to give you all the information you are looking for. 
- () Incorrect Answers:
- () Use Event Log filters to trigger alerts that are forwarded to CloudWatch is incorrect because the Event Log won’t provide you the required information.

**Answer:**
Correct Answer: **4 GiB**

**Explanation:**
The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.

---

## Question 76

**Q:** A client is concerned that someone other than approved administrators is trying to gain access to the Linux web app instances in their VPC. The client asks what sort of network access logging can be added. Which of the following might you recommend? (Choose two.)

**Options:**
- **(A) Use Event Log filters to trigger alerts that are forwarded to CloudWatch.** [CORRECT]
- (B) Correct selection
- (C) Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3.
- (D) Set up a Flow Log for the group of instances and forward them to CloudWatch.
- (E) Set up a traffic-logging rule on the VPC firewall appliance and direct the log to CloudWatch or S3.
- (F) Set up a Flow Log for the group of instances and forward them to S3.
- (G) Correct Answers:
- (H) Make use of an OS-level logging tool such as iptables and log events to CloudWatch or S3 and Set up a Flow Log for the group of instances and forward them to CloudWatch are correct. Since someone is trying to get into the web tier and the app tier, you have to analyze the logs from the operating system, and the Flow Log is going to give you all the information you are looking for. 
- (I) Incorrect Answers:
- (J) Use Event Log filters to trigger alerts that are forwarded to CloudWatch is incorrect because the Event Log won’t provide you the required information.

**Answer:**
Correct Answer: **Use Event Log filters to trigger alerts that are forwarded to CloudWatch.**

---

## Question 77

**Q:** Set up a Flow Log for the group of instances and forward them to S3 is incorrect because if you forward instances to S3, how do you use the information?

**Options:**
- (A) Set up a traffic-logging rule on the VPC firewall appliance and direct the log to CloudWatch or S3 is incorrect because this option is purposely misleading.
- (B) You work for a games development company that is re-architecting its production environment. The company has decided to make all web servers stateless. Which of the following AWS services will help the company achieve this goal? (Choose three.)
- (C) Correct selection
- (D) RDS
- (E) EMR
- (F) ELB
- (G) ElastiCache
- (H) DynamoDB
- (I) Correct Answers:
- (J) ElastiCache, RDS, and DynamoDB are correct. ElastiCache, RDS, and DynamoDB can be used to help make all web servers stateless. 
- () Incorrect Answers:
- () ELB and EMR are incorrect. An Elastic Load Balancer can help you deliver stateful services, but not stateless. Elastic Map Reduce is a data-crunching service and is not related to servicing web traffic.
- () What is the default rule in a NACL created within AWS?
- () Disallow all traffic
- () Allow all traffic in and out
- () Allow all traffic out and no traffic in
- () Allow all traffic in and no traffic out
- () Allow all traffic in and out is the correct answer. The default NACL rule is to allow all traffic in and out of the subnet to which the NACL is applied.
- () To what are security groups applied within an AWS IAM managed solution?
- () Subnets
- () Groups
- () Users
- () Network interfaces
- ()  used in AWS IAM for user management are simply called groups and not security groups. This can be a point of confusion for many new users of AWS.
- () What login has the ability to cancel an AWS subscription?
- () Any login
- () Any account admin login
- () Any admin login
- **() Root login** [CORRECT]

**Answer:**
Correct Answer: **Root login**

**Explanation:**
Root login is the correct answer. Only the root login can change the AWS support plan, cancel the account, open a billing support case, and perform several other account-related actions. For this reason, the root login should be secured and used only when these actions are required. The first action taken when creating an AWS account should be the creation of another login for all other administrative actions.

---

## Question 78

**Q:** You work for a games development company that is re-architecting its production environment. The company has decided to make all web servers stateless. Which of the following AWS services will help the company achieve this goal? (Choose three.)

**Options:**
- (A) Correct selection
- (B) RDS
- (C) EMR
- (D) ELB
- (E) ElastiCache
- (F) DynamoDB
- (G) Correct Answers:
- (H) ElastiCache, RDS, and DynamoDB are correct. ElastiCache, RDS, and DynamoDB can be used to help make all web servers stateless. 
- (I) Incorrect Answers:
- (J) ELB and EMR are incorrect. An Elastic Load Balancer can help you deliver stateful services, but not stateless. Elastic Map Reduce is a data-crunching service and is not related to servicing web traffic.
- () What is the default rule in a NACL created within AWS?
- () Disallow all traffic
- () Allow all traffic in and out
- () Allow all traffic out and no traffic in
- () Allow all traffic in and no traffic out
- () Allow all traffic in and out is the correct answer. The default NACL rule is to allow all traffic in and out of the subnet to which the NACL is applied.
- () To what are security groups applied within an AWS IAM managed solution?
- () Subnets
- () Groups
- () Users
- () Network interfaces
- ()  used in AWS IAM for user management are simply called groups and not security groups. This can be a point of confusion for many new users of AWS.
- () What login has the ability to cancel an AWS subscription?
- () Any login
- () Any account admin login
- () Any admin login
- **() Root login** [CORRECT]

**Answer:**
Correct Answer: **Root login**

**Explanation:**
Root login is the correct answer. Only the root login can change the AWS support plan, cancel the account, open a billing support case, and perform several other account-related actions. For this reason, the root login should be secured and used only when these actions are required. The first action taken when creating an AWS account should be the creation of another login for all other administrative actions.

---

## Question 79

**Q:** What is the default rule in a NACL created within AWS?

**Options:**
- (A) Disallow all traffic
- (B) Allow all traffic in and out
- (C) Allow all traffic out and no traffic in
- (D) Allow all traffic in and no traffic out
- (E) Allow all traffic in and out is the correct answer. The default NACL rule is to allow all traffic in and out of the subnet to which the NACL is applied.
- (F) To what are security groups applied within an AWS IAM managed solution?
- (G) Subnets
- (H) Groups
- (I) Users
- (J) Network interfaces
- ()  used in AWS IAM for user management are simply called groups and not security groups. This can be a point of confusion for many new users of AWS.
- () What login has the ability to cancel an AWS subscription?
- () Any login
- () Any account admin login
- () Any admin login
- () Root login
- () What is the default rule that exists in security groups?
- () Allow all encrypted traffic
- () Allow all inbound traffic
- () Allow all unencrypted traffic
- **() Allow all outbound traffic** [CORRECT]
- () Allow all outbound traffic is the correct answer. By default, security groups allow all outbound traffic. You must create additional rules to allow inbound traffic. If you do not wish to allow all outbound traffic, you must remove the default rule and replace it with one allowing only the desired outbound traffic.
- () Which of the following services should you implement in multiple availability zones in order to achieve high availability? (Choose two.)
- () DynamoDB
- () Correct selection
- () RDS

**Answer:**
Correct Answer: **Allow all outbound traffic**

**Explanation:**
Allow all outbound traffic is the correct answer. By default, security groups allow all outbound traffic. You must create additional rules to allow inbound traffic. If you do not wish to allow all outbound traffic, you must remove the default rule and replace it with one allowing only the desired outbound traffic.

---

## Question 80

**Q:** To what are security groups applied within an AWS IAM managed solution?

**Options:**
- (A) Subnets
- (B) Groups
- (C) Users
- (D) Network interfaces
- (E)  used in AWS IAM for user management are simply called groups and not security groups. This can be a point of confusion for many new users of AWS.
- (F) What login has the ability to cancel an AWS subscription?
- (G) Any login
- (H) Any account admin login
- (I) Any admin login
- (J) Root login
- () What is the default rule that exists in security groups?
- () Allow all encrypted traffic
- () Allow all inbound traffic
- () Allow all unencrypted traffic
- **() Allow all outbound traffic** [CORRECT]
- () Allow all outbound traffic is the correct answer. By default, security groups allow all outbound traffic. You must create additional rules to allow inbound traffic. If you do not wish to allow all outbound traffic, you must remove the default rule and replace it with one allowing only the desired outbound traffic.
- () Which of the following services should you implement in multiple availability zones in order to achieve high availability? (Choose two.)
- () DynamoDB
- () Correct selection
- () RDS
- () EC2
- () Simple Queue Service
- () Simple Storage Service
- () Correct Answers:
- () EC2 and RDS are correct. S3, SQS, and DynamoDB are already built in a fault-tolerant fashion, so you do not need to provision these services across multiple availability zones.
- () Incorrect Answers:
- () DynamoDB is incorrect because DynamoDB is a managed service and comes with high availability built in.
- () Simple Queue Service is incorrect because SQS is a managed service and comes with high availability built in.
- () Simple Storage Service is incorrect because S3 is a managed service and comes with high availability built in.

**Answer:**
Correct Answer: **Allow all outbound traffic**

**Explanation:**
Allow all outbound traffic is the correct answer. By default, security groups allow all outbound traffic. You must create additional rules to allow inbound traffic. If you do not wish to allow all outbound traffic, you must remove the default rule and replace it with one allowing only the desired outbound traffic.

---

## Question 81

**Q:** What login has the ability to cancel an AWS subscription?

**Options:**
- (A) Any login
- (B) Any account admin login
- (C) Any admin login
- (D) Root login
- (E) What is the default rule that exists in security groups?
- (F) Allow all encrypted traffic
- (G) Allow all inbound traffic
- (H) Allow all unencrypted traffic
- (I) Allow all outbound traffic
- (J) Allow all outbound traffic is the correct answer. By default, security groups allow all outbound traffic. You must create additional rules to allow inbound traffic. If you do not wish to allow all outbound traffic, you must remove the default rule and replace it with one allowing only the desired outbound traffic.
- () Which of the following services should you implement in multiple availability zones in order to achieve high availability? (Choose two.)
- () DynamoDB
- () Correct selection
- () RDS
- () EC2
- () Simple Queue Service
- () Simple Storage Service
- () Correct Answers:
- () EC2 and RDS are correct. S3, SQS, and DynamoDB are already built in a fault-tolerant fashion, so you do not need to provision these services across multiple availability zones.
- () Incorrect Answers:
- () DynamoDB is incorrect because DynamoDB is a managed service and comes with high availability built in.
- () Simple Queue Service is incorrect because SQS is a managed service and comes with high availability built in.
- () Simple Storage Service is incorrect because S3 is a managed service and comes with high availability built in.
- () You have implemented a read replica instance for a MySQL database. What should you communicate to the users in relation to how they will access the read replica?
- () Read replicas are accessed through special application APIs
- () Read replicas cannot be directly accessed, but are accessed by performing a read operation on the parent database instance
- **() Read replicas are accessed the same as any other database in RDS** [CORRECT]
- () Read replicas are accessed using a unique 256-bit SHA-1 key
- () Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

**Answer:**
Correct Answer: **Read replicas are accessed the same as any other database in RDS**

**Explanation:**
Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

---

## Question 82

**Q:** What is the default rule that exists in security groups?

**Options:**
- (A) Allow all encrypted traffic
- (B) Allow all inbound traffic
- (C) Allow all unencrypted traffic
- (D) Allow all outbound traffic
- (E) Allow all outbound traffic is the correct answer. By default, security groups allow all outbound traffic. You must create additional rules to allow inbound traffic. If you do not wish to allow all outbound traffic, you must remove the default rule and replace it with one allowing only the desired outbound traffic.
- (F) Which of the following services should you implement in multiple availability zones in order to achieve high availability? (Choose two.)
- (G) DynamoDB
- (H) Correct selection
- (I) RDS
- (J) EC2
- () Simple Queue Service
- () Simple Storage Service
- () Correct Answers:
- () EC2 and RDS are correct. S3, SQS, and DynamoDB are already built in a fault-tolerant fashion, so you do not need to provision these services across multiple availability zones.
- () Incorrect Answers:
- () DynamoDB is incorrect because DynamoDB is a managed service and comes with high availability built in.
- () Simple Queue Service is incorrect because SQS is a managed service and comes with high availability built in.
- () Simple Storage Service is incorrect because S3 is a managed service and comes with high availability built in.
- () You have implemented a read replica instance for a MySQL database. What should you communicate to the users in relation to how they will access the read replica?
- () Read replicas are accessed through special application APIs
- () Read replicas cannot be directly accessed, but are accessed by performing a read operation on the parent database instance
- **() Read replicas are accessed the same as any other database in RDS** [CORRECT]
- () Read replicas are accessed using a unique 256-bit SHA-1 key
- () Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

**Answer:**
Correct Answer: **Read replicas are accessed the same as any other database in RDS**

**Explanation:**
Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

---

## Question 83

**Q:** Which of the following services should you implement in multiple availability zones in order to achieve high availability? (Choose two.)

**Options:**
- (A) DynamoDB
- (B) Correct selection
- (C) RDS
- (D) EC2
- (E) Simple Queue Service
- (F) Simple Storage Service
- (G) Correct Answers:
- (H) EC2 and RDS are correct. S3, SQS, and DynamoDB are already built in a fault-tolerant fashion, so you do not need to provision these services across multiple availability zones.
- (I) Incorrect Answers:
- (J) DynamoDB is incorrect because DynamoDB is a managed service and comes with high availability built in.
- () Simple Queue Service is incorrect because SQS is a managed service and comes with high availability built in.
- () Simple Storage Service is incorrect because S3 is a managed service and comes with high availability built in.
- () You have implemented a read replica instance for a MySQL database. What should you communicate to the users in relation to how they will access the read replica?
- () Read replicas are accessed through special application APIs
- () Read replicas cannot be directly accessed, but are accessed by performing a read operation on the parent database instance
- **() Read replicas are accessed the same as any other database in RDS** [CORRECT]
- () Read replicas are accessed using a unique 256-bit SHA-1 key
- () Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

**Answer:**
Correct Answer: **Read replicas are accessed the same as any other database in RDS**

**Explanation:**
Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

---

## Question 84

**Q:** You have implemented a read replica instance for a MySQL database. What should you communicate to the users in relation to how they will access the read replica?

**Options:**
- (A) Read replicas are accessed through special application APIs
- (B) Read replicas cannot be directly accessed, but are accessed by performing a read operation on the parent database instance
- **(C) Read replicas are accessed the same as any other database in RDS** [CORRECT]
- (D) Read replicas are accessed using a unique 256-bit SHA-1 key
- (E) Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

**Answer:**
Correct Answer: **Read replicas are accessed the same as any other database in RDS**

**Explanation:**
Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

---

## Question 85

**Q:** Your AWS environment contains several on-demand EC2 instances dedicated to a project that has just been cancelled. Your supervisor does not want to incur charges for these on-demand instances, but also does not want to lose the data just yet because there is a chance the project may be revived in the next few days. What should you do to minimize charges for these instances in the meantime?

**Options:**
- (A) Stop the instances.
- (B) Contact AWS Support and put the instances on courtesy hold.
- (C) Create AMIs from the instances and put them on the AWS Marketplace in hopes of recovering some of the cost.
- (D) Terminate the instances.
- (E) Stop the instances is correct. When the data is stored in EBS volumes, it will be stored even if the instances are stopped. The EBS volumes persist the data, so it will always be there. On the other hand, if the data is stored in the instance store and you shut down the instance, you lose everything. 
- (F) Incorrect Answers:
- (G) Terminate the instances is incorrect because termination will delete all the data.
- (H) Create AMIs from the instances and put them on the AWS Marketplace in hopes of recovering some of the cost is incorrect because creating AMIs from instances will add cost.
- (I) Contact AWS Support and put the instances on courtesy hold is incorrect because no such option exists.
- (J) What common security standard is IAM in compliance with that allows for credit card data to be processed?
- () GDPR
- () HIPAA
- () GLBA
- () PCI-DSS
- () PCI-DSS is the correct answer. The Payment Card Industry-Data Security Standard (PCI-DSS) specified operational procedures and methods to support secure payment card processing and IAM complies with this standard. HIPAA is related to health information privacy. GLBA is about financial accounting. GDPR is a European Union privacy standard.
- () Why might you choose a specific region when creating an S3 bucket rather than accepting a default region?
- () To place the bucket closer to the users for improved performance
- () To ensure permissions can be configured on the bucket
- () To ensure the data is stored with encryption
- () To place the bucket closer to AWS headquarters for improved performance
- () To place the bucket closer to the users for improved performance is the correct answer. By selecting a region closer to the primary users of the bucket, you can enhance performance for those users. Encryption and permissions may be configured regardless of where the bucket is physically stored. Placing it closer to AWS HQ will provide no benefit to you, unless, of course, you work at AWS HQ.
- () What IAM account is accessed using an e-mail address and has unlimited permissions within AWS?
- () All administrator users
- () Any user in a group
- **() Root user** [CORRECT]
- () Standard created user
- () Root user is the correct answer. The root user account can do anything in relation to the AWS account and is accessed by logging in with the e-mail address used to create the account. As a best practice, this account should not be used for daily administration and should have multi-factor authentication (MFA) enabled.
- () Which file sizes generally provide for faster access per megabyte when using EFS and why?

**Answer:**
Correct Answer: **Root user**

**Explanation:**
Root user is the correct answer. The root user account can do anything in relation to the AWS account and is accessed by logging in with the e-mail address used to create the account. As a best practice, this account should not be used for daily administration and should have multi-factor authentication (MFA) enabled.

---

## Question 86

**Q:** What common security standard is IAM in compliance with that allows for credit card data to be processed?

**Options:**
- (A) GDPR
- (B) HIPAA
- (C) GLBA
- (D) PCI-DSS
- (E) PCI-DSS is the correct answer. The Payment Card Industry-Data Security Standard (PCI-DSS) specified operational procedures and methods to support secure payment card processing and IAM complies with this standard. HIPAA is related to health information privacy. GLBA is about financial accounting. GDPR is a European Union privacy standard.
- (F) Why might you choose a specific region when creating an S3 bucket rather than accepting a default region?
- (G) To place the bucket closer to the users for improved performance
- (H) To ensure permissions can be configured on the bucket
- (I) To ensure the data is stored with encryption
- (J) To place the bucket closer to AWS headquarters for improved performance
- () To place the bucket closer to the users for improved performance is the correct answer. By selecting a region closer to the primary users of the bucket, you can enhance performance for those users. Encryption and permissions may be configured regardless of where the bucket is physically stored. Placing it closer to AWS HQ will provide no benefit to you, unless, of course, you work at AWS HQ.
- () What IAM account is accessed using an e-mail address and has unlimited permissions within AWS?
- () All administrator users
- () Any user in a group
- () Root user
- () Standard created user
- () Root user is the correct answer. The root user account can do anything in relation to the AWS account and is accessed by logging in with the e-mail address used to create the account. As a best practice, this account should not be used for daily administration and should have multi-factor authentication (MFA) enabled.
- () Which file sizes generally provide for faster access per megabyte when using EFS and why?
- () Small file sizes because the time to access small file locations is less than the time to access large file locations
- () Large file sizes because the time to access the file location is the same regardless of file size
- () Large file sizes because the drives spin faster and faster as the file is accessed
- () Small file sizes because they are often read in a single spin of the disk
- () You want to implement an Oracle database in AWS. What managed service in AWS allows you to do this in the least expensive way?
- () Aurora
- **() RDS** [CORRECT]

**Answer:**
Correct Answer: **RDS**

**Explanation:**
Large file sizes because the time to access the file location is the same regardless of file size is the correct answer. To understand the answer to this question, you must remember that EFS distributes files for availability and durability. The result is that the files must be located before they are accessed. Therefore, performance per megabyte will increase when accessing larger files as the file location time is lessened in comparison to total file access time.

---

## Question 87

**Q:** Why might you choose a specific region when creating an S3 bucket rather than accepting a default region?

**Options:**
- (A) To place the bucket closer to the users for improved performance
- (B) To ensure permissions can be configured on the bucket
- (C) To ensure the data is stored with encryption
- (D) To place the bucket closer to AWS headquarters for improved performance
- (E) To place the bucket closer to the users for improved performance is the correct answer. By selecting a region closer to the primary users of the bucket, you can enhance performance for those users. Encryption and permissions may be configured regardless of where the bucket is physically stored. Placing it closer to AWS HQ will provide no benefit to you, unless, of course, you work at AWS HQ.
- (F) What IAM account is accessed using an e-mail address and has unlimited permissions within AWS?
- (G) All administrator users
- (H) Any user in a group
- (I) Root user
- (J) Standard created user
- () Root user is the correct answer. The root user account can do anything in relation to the AWS account and is accessed by logging in with the e-mail address used to create the account. As a best practice, this account should not be used for daily administration and should have multi-factor authentication (MFA) enabled.
- () Which file sizes generally provide for faster access per megabyte when using EFS and why?
- () Small file sizes because the time to access small file locations is less than the time to access large file locations
- () Large file sizes because the time to access the file location is the same regardless of file size
- () Large file sizes because the drives spin faster and faster as the file is accessed
- () Small file sizes because they are often read in a single spin of the disk
- () You want to implement an Oracle database in AWS. What managed service in AWS allows you to do this in the least expensive way?
- () Aurora
- **() RDS** [CORRECT]
- () Redshift
- () EC2
- () RDS is the correct answer. RDS is the Relational Database Service and it supports Oracle databases run in the managed service. Redshift and Aurora are specific AWS databases and are not compatible with Oracle databases. EC2 instances could be used by installing the OS and Oracle database server, but it is not a managed service like RDS.
- () You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?
- () MySQL
- () DynamoDB

**Answer:**
Correct Answer: **RDS**

**Explanation:**
RDS is the correct answer. RDS is the Relational Database Service and it supports Oracle databases run in the managed service. Redshift and Aurora are specific AWS databases and are not compatible with Oracle databases. EC2 instances could be used by installing the OS and Oracle database server, but it is not a managed service like RDS.

---

## Question 88

**Q:** What IAM account is accessed using an e-mail address and has unlimited permissions within AWS?

**Options:**
- (A) All administrator users
- (B) Any user in a group
- (C) Root user
- (D) Standard created user
- (E) Root user is the correct answer. The root user account can do anything in relation to the AWS account and is accessed by logging in with the e-mail address used to create the account. As a best practice, this account should not be used for daily administration and should have multi-factor authentication (MFA) enabled.
- (F) Which file sizes generally provide for faster access per megabyte when using EFS and why?
- (G) Small file sizes because the time to access small file locations is less than the time to access large file locations
- (H) Large file sizes because the time to access the file location is the same regardless of file size
- (I) Large file sizes because the drives spin faster and faster as the file is accessed
- (J) Small file sizes because they are often read in a single spin of the disk
- () You want to implement an Oracle database in AWS. What managed service in AWS allows you to do this in the least expensive way?
- () Aurora
- () RDS
- () Redshift
- () EC2
- () RDS is the correct answer. RDS is the Relational Database Service and it supports Oracle databases run in the managed service. Redshift and Aurora are specific AWS databases and are not compatible with Oracle databases. EC2 instances could be used by installing the OS and Oracle database server, but it is not a managed service like RDS.
- () You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?
- () MySQL
- () DynamoDB
- **() S3** [CORRECT]
- () S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

**Answer:**
Correct Answer: **S3**

**Explanation:**
S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

---

## Question 89

**Q:** Which file sizes generally provide for faster access per megabyte when using EFS and why?

**Options:**
- (A) Small file sizes because the time to access small file locations is less than the time to access large file locations
- (B) Large file sizes because the time to access the file location is the same regardless of file size
- (C) Large file sizes because the drives spin faster and faster as the file is accessed
- (D) Small file sizes because they are often read in a single spin of the disk
- (E) You want to implement an Oracle database in AWS. What managed service in AWS allows you to do this in the least expensive way?
- (F) Aurora
- (G) RDS
- (H) Redshift
- (I) EC2
- (J) RDS is the correct answer. RDS is the Relational Database Service and it supports Oracle databases run in the managed service. Redshift and Aurora are specific AWS databases and are not compatible with Oracle databases. EC2 instances could be used by installing the OS and Oracle database server, but it is not a managed service like RDS.
- () You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?
- () MySQL
- () DynamoDB
- **() S3** [CORRECT]
- () S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

**Answer:**
Correct Answer: **S3**

**Explanation:**
S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

---

## Question 90

**Q:** You want to implement an Oracle database in AWS. What managed service in AWS allows you to do this in the least expensive way?

**Options:**
- (A) Aurora
- (B) RDS
- (C) Redshift
- (D) EC2
- (E) RDS is the correct answer. RDS is the Relational Database Service and it supports Oracle databases run in the managed service. Redshift and Aurora are specific AWS databases and are not compatible with Oracle databases. EC2 instances could be used by installing the OS and Oracle database server, but it is not a managed service like RDS.
- (F) You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?
- (G) MySQL
- (H) DynamoDB
- **(I) S3** [CORRECT]
- (J) S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

**Answer:**
Correct Answer: **S3**

**Explanation:**
S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

---

## Question 91

**Q:** You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?

**Options:**
- (A) Aurora
- (B) MySQL
- (C) DynamoDB
- **(D) S3** [CORRECT]
- (E) S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

**Answer:**
Correct Answer: **S3**

**Explanation:**
S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

---

## Question 92

**Q:** When creating NACLs within AWS, why is the rule order so important?

**Options:**
- (A) Because the first matching rule applies
- (B) Because deny rules must be placed before permit or allow rules
- (C) Because they must be entered in the order of TCP or UDP ports
- (D) Because they must be entered in the order of IP addresses
- (E) Because the matching rule applies is the correct answer. When processing a Network Access Control List (NACL), the AWS system applies the first rule that matches, starting with the lowest numbered rule first. Therefore, the rules must be numbered in an order that will ensure an allowance or denial that should always be applied if higher in the list (by having a lower number).
- (F) What service within AWS provides for DNS name management and resolution?
- (G) Route 47
- (H) Route 53
- (I) Kinesis
- (J) ENI
- () Route 53 is the correct answer. Route 53 is the AWS DNS service. ENI is the Elastic Network Interface, which may be attached to an instance and provided an Elastic IP (EIP) address, which is routable on the Internet. Kinesis is for working with real-time data streams. Route 47 does not exist in AWS.
- () You must implement an S3 storage solution that encrypts data at rest in the S3 buckets. Which S3 storage class supports at-rest data encryption?
- () S3-Standard
- () S3-One Zone-IA
- () All of these
- () S3-IA
- () All of these answers are correct. All S3 storage classes support at-rest data encryption. Additionally, SSL may be used for encryption during transmission as data is placed into the S3 buckets or read from the S3 buckets.
- () You are planning an EFS implementation in AWS. You are uncertain how many files will be created and the total storage space required. What should you specify as the allocated EFS storage space?
- () 1 TB
- **() You do not specify storage space allocation when creating an EFS file system** [CORRECT]
- () 100 GB
- () 100 MB
- () You do not specify storage space allocation when creating an EFS file system is the correct answer. When implementing EFS, you do not specify the amount of storage space. This is why it is called elastic (the Elastic File System). The file system will grow as required to accommodate the files stored and you pay for the storage consumed.
- () Change the core nodes to spot instances and lower the spot price.
- () Correct selection
- () Change the task nodes to on-demand instances.
- () Increase the bid price for the core nodes.

**Answer:**
Correct Answer: **You do not specify storage space allocation when creating an EFS file system**

**Explanation:**
You do not specify storage space allocation when creating an EFS file system is the correct answer. When implementing EFS, you do not specify the amount of storage space. This is why it is called elastic (the Elastic File System). The file system will grow as required to accommodate the files stored and you pay for the storage consumed.

---

## Question 93

**Q:** What service within AWS provides for DNS name management and resolution?

**Options:**
- (A) Route 47
- (B) Route 53
- (C) Kinesis
- (D) ENI
- (E) Route 53 is the correct answer. Route 53 is the AWS DNS service. ENI is the Elastic Network Interface, which may be attached to an instance and provided an Elastic IP (EIP) address, which is routable on the Internet. Kinesis is for working with real-time data streams. Route 47 does not exist in AWS.
- (F) You must implement an S3 storage solution that encrypts data at rest in the S3 buckets. Which S3 storage class supports at-rest data encryption?
- (G) S3-Standard
- (H) S3-One Zone-IA
- (I) All of these
- (J) S3-IA
- () All of these answers are correct. All S3 storage classes support at-rest data encryption. Additionally, SSL may be used for encryption during transmission as data is placed into the S3 buckets or read from the S3 buckets.
- () You are planning an EFS implementation in AWS. You are uncertain how many files will be created and the total storage space required. What should you specify as the allocated EFS storage space?
- () 1 TB
- **() You do not specify storage space allocation when creating an EFS file system** [CORRECT]
- () 100 GB
- () 100 MB
- () You do not specify storage space allocation when creating an EFS file system is the correct answer. When implementing EFS, you do not specify the amount of storage space. This is why it is called elastic (the Elastic File System). The file system will grow as required to accommodate the files stored and you pay for the storage consumed.
- () Change the core nodes to spot instances and lower the spot price.
- () Correct selection
- () Change the task nodes to on-demand instances.
- () Increase the bid price for the core nodes.
- () Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated.
- () Correct Answers:
- () Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated and Change the task nodes to on-demand instances are correct. Task nodes perform the jobs, whereas core nodes provide the pure core for performing the jobs. Even if a core node goes down, the jobs won’t fail. 
- () Incorrect Answers:
- () Increase the bid price for the core nodes is incorrect because it is the task nodes that do all the work; the issue is with the task nodes.
- () Change the core nodes to spot instances and lower the spot price is incorrect because the problem is with the task nodes.
- () What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?
- () Access Key ID/Username
- () Username/Secret Access Key
- () Password/Access Key ID

**Answer:**
Correct Answer: **You do not specify storage space allocation when creating an EFS file system**

**Explanation:**
You do not specify storage space allocation when creating an EFS file system is the correct answer. When implementing EFS, you do not specify the amount of storage space. This is why it is called elastic (the Elastic File System). The file system will grow as required to accommodate the files stored and you pay for the storage consumed.

---

## Question 94

**Q:** You must implement an S3 storage solution that encrypts data at rest in the S3 buckets. Which S3 storage class supports at-rest data encryption?

**Options:**
- (A) S3-Standard
- (B) S3-One Zone-IA
- (C) All of these
- (D) S3-IA
- (E) All of these answers are correct. All S3 storage classes support at-rest data encryption. Additionally, SSL may be used for encryption during transmission as data is placed into the S3 buckets or read from the S3 buckets.
- (F) You are planning an EFS implementation in AWS. You are uncertain how many files will be created and the total storage space required. What should you specify as the allocated EFS storage space?
- (G) 1 TB
- (H) You do not specify storage space allocation when creating an EFS file system
- (I) 100 GB
- (J) 100 MB
- () You do not specify storage space allocation when creating an EFS file system is the correct answer. When implementing EFS, you do not specify the amount of storage space. This is why it is called elastic (the Elastic File System). The file system will grow as required to accommodate the files stored and you pay for the storage consumed.
- () Change the core nodes to spot instances and lower the spot price.
- () Correct selection
- () Change the task nodes to on-demand instances.
- () Increase the bid price for the core nodes.
- () Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated.
- () Correct Answers:
- () Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated and Change the task nodes to on-demand instances are correct. Task nodes perform the jobs, whereas core nodes provide the pure core for performing the jobs. Even if a core node goes down, the jobs won’t fail. 
- () Incorrect Answers:
- () Increase the bid price for the core nodes is incorrect because it is the task nodes that do all the work; the issue is with the task nodes.
- () Change the core nodes to spot instances and lower the spot price is incorrect because the problem is with the task nodes.
- () What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?
- () Access Key ID/Username
- () Username/Secret Access Key
- () Password/Access Key ID
- **() Access Key ID/Secret Access Key** [CORRECT]
- () Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.
- () You are a solutions architect working for a large antivirus company and your job is to secure your company’s production AWS environment. A new policy dictates that a particular public-facing subnet needs to allow RDP on port 3389 at the network ACL layer. You create an inbound rule allowing traffic to port 3389 on the ACL level. However, users complain that they still cannot connect. Which of the following answers may represent the root cause of the connectivity issues? (Choose two.)
- () You need to create an outbound rule allowing RDP response traffic to go back out again.

**Answer:**
Correct Answer: **Access Key ID/Secret Access Key**

**Explanation:**
Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.

---

## Question 95

**Q:** You are planning an EFS implementation in AWS. You are uncertain how many files will be created and the total storage space required. What should you specify as the allocated EFS storage space?

**Options:**
- (A) 1 TB
- (B) You do not specify storage space allocation when creating an EFS file system
- (C) 100 GB
- (D) 100 MB
- (E) You do not specify storage space allocation when creating an EFS file system is the correct answer. When implementing EFS, you do not specify the amount of storage space. This is why it is called elastic (the Elastic File System). The file system will grow as required to accommodate the files stored and you pay for the storage consumed.
- (F) Change the core nodes to spot instances and lower the spot price.
- (G) Correct selection
- (H) Change the task nodes to on-demand instances.
- (I) Increase the bid price for the core nodes.
- (J) Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated.
- () Correct Answers:
- () Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated and Change the task nodes to on-demand instances are correct. Task nodes perform the jobs, whereas core nodes provide the pure core for performing the jobs. Even if a core node goes down, the jobs won’t fail. 
- () Incorrect Answers:
- () Increase the bid price for the core nodes is incorrect because it is the task nodes that do all the work; the issue is with the task nodes.
- () Change the core nodes to spot instances and lower the spot price is incorrect because the problem is with the task nodes.
- () What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?
- () Access Key ID/Username
- () Username/Secret Access Key
- () Password/Access Key ID
- **() Access Key ID/Secret Access Key** [CORRECT]
- () Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.
- () You are a solutions architect working for a large antivirus company and your job is to secure your company’s production AWS environment. A new policy dictates that a particular public-facing subnet needs to allow RDP on port 3389 at the network ACL layer. You create an inbound rule allowing traffic to port 3389 on the ACL level. However, users complain that they still cannot connect. Which of the following answers may represent the root cause of the connectivity issues? (Choose two.)
- () You need to create an outbound rule allowing RDP response traffic to go back out again.
- () Network access control lists are stateless.
- () Network access control lists are stateful.
- () Updates to network access control lists can take time to propagate.
- () Network access control lists are stateless and You need to create an outbound rule allowing RDP response traffic to go back out again are correct. Network access control lists (NACLs) are stateless and security groups are stateful. Since there is no outbound rule there, you must create it explicitly. 
- () Updates to network access control lists can take time to propagate is incorrect because this statement is misleading.
- () Network access control lists are stateful is incorrect because NACLs are stateless.

**Answer:**
Correct Answer: **Access Key ID/Secret Access Key**

**Explanation:**
Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.

---

## Question 96

**Q:** You work for a genomics company that is developing a cure for motor neuron disease by using advanced gene therapies. As a part of its research, the company takes extremely large data sets (usually in the terabytes) and analyzes them using Elastic Map Reduce (EMR). In order to keep costs low, the company runs the analysis for only a few hours in the early hours of the morning, using spot instances for the task nodes. The core nodes are on-demand instances. Lately, however, the EMR jobs have been failing. This is due to spot instances being unexpectedly terminated. Which of the following remedies would both keep costs manageable and mitigate the issues caused by terminated spot instances? (Choose two.)

**Options:**
- (A) Change the core nodes to spot instances and lower the spot price.
- (B) Correct selection
- (C) Change the task nodes to on-demand instances.
- (D) Increase the bid price for the core nodes.
- (E) Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated.
- (F) Correct Answers:
- (G) Increase the bid price for the task nodes so that you have a greater threshold before the task nodes are terminated and Change the task nodes to on-demand instances are correct. Task nodes perform the jobs, whereas core nodes provide the pure core for performing the jobs. Even if a core node goes down, the jobs won’t fail. 
- (H) Incorrect Answers:
- (I) Increase the bid price for the core nodes is incorrect because it is the task nodes that do all the work; the issue is with the task nodes.
- (J) Change the core nodes to spot instances and lower the spot price is incorrect because the problem is with the task nodes.
- () What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?
- () Access Key ID/Username
- () Username/Secret Access Key
- () Password/Access Key ID
- **() Access Key ID/Secret Access Key** [CORRECT]
- () Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.
- () You are a solutions architect working for a large antivirus company and your job is to secure your company’s production AWS environment. A new policy dictates that a particular public-facing subnet needs to allow RDP on port 3389 at the network ACL layer. You create an inbound rule allowing traffic to port 3389 on the ACL level. However, users complain that they still cannot connect. Which of the following answers may represent the root cause of the connectivity issues? (Choose two.)
- () You need to create an outbound rule allowing RDP response traffic to go back out again.
- () Network access control lists are stateless.
- () Network access control lists are stateful.
- () Updates to network access control lists can take time to propagate.
- () Network access control lists are stateless and You need to create an outbound rule allowing RDP response traffic to go back out again are correct. Network access control lists (NACLs) are stateless and security groups are stateful. Since there is no outbound rule there, you must create it explicitly. 
- () Updates to network access control lists can take time to propagate is incorrect because this statement is misleading.
- () Network access control lists are stateful is incorrect because NACLs are stateless.
- () You should configure your Elastic Load Balancer to act as a reverse proxy so that the EC2 instance can communicate back to the on-premises data center.
- () You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit.
- () You should attach an Elastic IP address to the VPC so that it will be able to communicate with the on-premises site.
- () You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution.
- () You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution and You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit are correct.

**Answer:**
Correct Answer: **Access Key ID/Secret Access Key**

**Explanation:**
Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.

---

## Question 97

**Q:** What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?

**Options:**
- (A) Access Key ID/Username
- (B) Username/Secret Access Key
- (C) Password/Access Key ID
- **(D) Access Key ID/Secret Access Key** [CORRECT]
- (E) Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.
- (F) You are a solutions architect working for a large antivirus company and your job is to secure your company’s production AWS environment. A new policy dictates that a particular public-facing subnet needs to allow RDP on port 3389 at the network ACL layer. You create an inbound rule allowing traffic to port 3389 on the ACL level. However, users complain that they still cannot connect. Which of the following answers may represent the root cause of the connectivity issues? (Choose two.)
- (G) Correct selection
- (H) You need to create an outbound rule allowing RDP response traffic to go back out again.
- (I) Network access control lists are stateless.
- (J) Network access control lists are stateful.
- () Updates to network access control lists can take time to propagate.
- () Correct Answers:
- () Network access control lists are stateless and You need to create an outbound rule allowing RDP response traffic to go back out again are correct. Network access control lists (NACLs) are stateless and security groups are stateful. Since there is no outbound rule there, you must create it explicitly. 
- () Incorrect Answers:
- () Updates to network access control lists can take time to propagate is incorrect because this statement is misleading.
- () Network access control lists are stateful is incorrect because NACLs are stateless.
- () You should configure your Elastic Load Balancer to act as a reverse proxy so that the EC2 instance can communicate back to the on-premises data center.
- () You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit.
- () You should attach an Elastic IP address to the VPC so that it will be able to communicate with the on-premises site.
- () You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution.
- () You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution and You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit are correct.
- () Your Internet Gateway (IGW) on your VPC has provisioned too many EC2 instances.
- () AWS reserves both the first two and the last two IP addresses in each subnet’s CIDR block.
- () Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet.
- () AWS reserves both the first three and the last two IP addresses in each subnet’s CIDR block.
- () AWS reserves both the first four and the last IP address in each subnet’s CIDR block.
- () AWS reserves both the first four and the last IP address in each subnet’s CIDR block and Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet are correct.

**Answer:**
Correct Answer: **Access Key ID/Secret Access Key**

**Explanation:**
Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.

---

## Question 98

**Q:** You are a solutions architect working for a large antivirus company and your job is to secure your company’s production AWS environment. A new policy dictates that a particular public-facing subnet needs to allow RDP on port 3389 at the network ACL layer. You create an inbound rule allowing traffic to port 3389 on the ACL level. However, users complain that they still cannot connect. Which of the following answers may represent the root cause of the connectivity issues? (Choose two.)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) You need to create an outbound rule allowing RDP response traffic to go back out again.
- (C) Network access control lists are stateless.
- (D) Network access control lists are stateful.
- (E) Updates to network access control lists can take time to propagate.
- (F) Correct Answers:
- (G) Network access control lists are stateless and You need to create an outbound rule allowing RDP response traffic to go back out again are correct. Network access control lists (NACLs) are stateless and security groups are stateful. Since there is no outbound rule there, you must create it explicitly. 
- (H) Incorrect Answers:
- (I) Updates to network access control lists can take time to propagate is incorrect because this statement is misleading.
- (J) Network access control lists are stateful is incorrect because NACLs are stateless.
- () You should configure your Elastic Load Balancer to act as a reverse proxy so that the EC2 instance can communicate back to the on-premises data center.
- () You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit.
- () You should attach an Elastic IP address to the VPC so that it will be able to communicate with the on-premises site.
- () You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution.
- () You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution and You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit are correct.
- () Your Internet Gateway (IGW) on your VPC has provisioned too many EC2 instances.
- () AWS reserves both the first two and the last two IP addresses in each subnet’s CIDR block.
- () Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet.
- () AWS reserves both the first three and the last two IP addresses in each subnet’s CIDR block.
- () AWS reserves both the first four and the last IP address in each subnet’s CIDR block.
- () AWS reserves both the first four and the last IP address in each subnet’s CIDR block and Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet are correct.
- () AWS reserves both the first two and the last two IP addresses in each subnet’s CIDR block is incorrect because AWS doesn’t reserve the first two and last two IP addresses in a subnet’s CIDR block.
- () AWS reserves both the first three and the last two IP addresses in each subnet’s CIDR block is incorrect because AWS doesn’t reserve the first three and last two IP addresses in a subnet’s CIDR block.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 99

**Q:** You are a solutions architect with a manufacturing company running several legacy applications. One of these applications needs to communicate with services that are currently hosted on premises. The people who wrote this application have left the company, and there is no documentation describing how the application works. You need to ensure that this application can be hosted in a non-default VPC but remains able to communicate with the back-end services hosted on premises. Which of the following options will allow the application to communicate back to the on-premises equipment without the need to reprogram the application? (Choose two.)

**Options:**
- **(A) You should configure your Elastic Load Balancer to act as a reverse proxy so that the EC2 instance can communicate back to the on-premises data center.** [CORRECT]
- (B) Correct selection
- (C) You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit.
- (D) You should attach an Elastic IP address to the VPC so that it will be able to communicate with the on-premises site.
- (E) You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution.
- (F) Correct Answers:
- (G) You should configure an AWS Direct-Connect link between the VPC and the site with the on-premises solution and You should configure the VPC subnet in which the application sits so that it does not have an IP address range that conflicts with that of the on-premises VLAN in which the back-end services sit are correct.
- (H) Your Internet Gateway (IGW) on your VPC has provisioned too many EC2 instances.
- (I) AWS reserves both the first two and the last two IP addresses in each subnet’s CIDR block.
- (J) Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet.
- () AWS reserves both the first three and the last two IP addresses in each subnet’s CIDR block.
- () AWS reserves both the first four and the last IP address in each subnet’s CIDR block.
- () AWS reserves both the first four and the last IP address in each subnet’s CIDR block and Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet are correct.
- () Incorrect Answers:
- () AWS reserves both the first two and the last two IP addresses in each subnet’s CIDR block is incorrect because AWS doesn’t reserve the first two and last two IP addresses in a subnet’s CIDR block.
- () AWS reserves both the first three and the last two IP addresses in each subnet’s CIDR block is incorrect because AWS doesn’t reserve the first three and last two IP addresses in a subnet’s CIDR block.

**Answer:**
Correct Answer: **You should configure your Elastic Load Balancer to act as a reverse proxy so that the EC2 instance can communicate back to the on-premises data center.**

---

## Question 100

**Q:** You have provisioned a custom VPC with a subnet that has a CIDR block address range of 10.0.3.0/28. Inside this subnet, you have two web servers, two application servers, two database servers, and a NAT. You have configured an Auto Scaling group on the two web servers to automatically scale when the CPU utilization goes above 90%. Several days later, you notice that Auto Scaling is no longer deploying new instances into the subnet, despite the CPU utilization of all web servers being at 100%. Which of the following answers may offer an explanation? (Choose two.)

**Options:**
- **(A) Your Internet Gateway (IGW) on your VPC has provisioned too many EC2 instances.** [CORRECT]
- (B) AWS reserves both the first two and the last two IP addresses in each subnet’s CIDR block.
- (C) Correct selection
- (D) Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet.
- (E) AWS reserves both the first three and the last two IP addresses in each subnet’s CIDR block.
- (F) AWS reserves both the first four and the last IP address in each subnet’s CIDR block.
- (G) Correct Answers:
- (H) AWS reserves both the first four and the last IP address in each subnet’s CIDR block and Your Auto Scaling group (ASG) has provisioned too many EC2 instances and has exhausted the number of internal IP addresses available in the subnet are correct.
- (I) Incorrect Answers:
- (J) AWS reserves both the first two and the last two IP addresses in each subnet’s CIDR block is incorrect because AWS doesn’t reserve the first two and last two IP addresses in a subnet’s CIDR block.
- () AWS reserves both the first three and the last two IP addresses in each subnet’s CIDR block is incorrect because AWS doesn’t reserve the first three and last two IP addresses in a subnet’s CIDR block.

**Answer:**
Correct Answer: **Your Internet Gateway (IGW) on your VPC has provisioned too many EC2 instances.**

---

## Question 101

**Q:** Scenario: You are using large-scale databases and intensive processing EC2 instances. If you know the amount of resources required for one year or more for an AWS EC2 instance or RDS database, what can be utilized to reduce costs by 40% or more?

**Options:**
- (A) Reserved pricing
- (B) Free tier services
- (C) None of these
- (D) On-Demand pricing
- (E) Reserved pricing is the correct answer. The AWS Pricing Calculator can be used to estimate costs for the major AWS services including S3 and EC2. The other listed items are used to work with costs related to actual implemented solutions.
- (F) The proxy server has only one Elastic IP address added to it. To increase network throughput, you should add additional Elastic IP addresses.
- (G) Your proxy server is blacklisting the address from which the updates are being downloaded, resulting in failed downloads.
- (H) Correct selection
- (I) The proxy server is in a private subnet and uses a NAT gateway instance to connect to the Internet. However, this instance is too small to handle the required network traffic. You should re-provision the NAT gateway instance so that it’s able to handle the throughput.
- (J) The proxy server has an inadequately sized EBS volume attached to it. The network buffer is stored on the EBS volume, and it is running out of disk space when trying to buffer the 500 simultaneous connections. You should provision an EBS volume with provisioned IOPS.
- () The proxy server is on an inadequately sized EC2 instance and does not have sufficient network throughput to handle all updates simultaneously. You should increase the instance size of the EC2 instance for the proxy server.
- () Correct Answers:
- () Incorrect Answers:
- () Your proxy server is blacklisting the address from which the updates are being downloaded, resulting in failed downloads is incorrect because there is no data point stating that the proxy server is blacklisting.
- () The proxy server has only one Elastic IP address added to it. To increase network throughput, you should add additional Elastic IP addresses is incorrect because adding elastic IP does not increase network throughput. 
- () The proxy server has an inadequately sized EBS volume attached to it. The network buffer is stored on the EBS volume, and it is running out of disk space when trying to buffer the 500 simultaneous connections. You should provision an EBS volume with provisioned IOPS is incorrect because there is no data point stating that the EBS volume is running out of space.
- () For which of the following does the AWS Trusted Adviser service offer advice? (Choose two.)
- () Whether MFA is configured on the root account
- () Antivirus protection on EC2 instances
- () Vulnerability scans on existing VPCs
- () Advice on security groups and what ports have unrestricted access
- () Whether MFA is configured on the root account and Advice on security groups and what ports have unrestricted access are correct. Trusted Advisor provides more than 40 different types of checks to make sure you are running your infrastructure in AWS in the most optimized way. It can check whether multifactor authentication (MFA) is configured on the root account as well as provide advice on security groups and what ports have unrestricted access.
- () Antivirus protection on EC2 instances is incorrect because Trusted Advisor does not provide antivirus protection.
- () Vulnerability scans on existing VPCs is incorrect because Trusted Advisor does not perform vulnerability scans on VPCs.
- () What can be configured to optimize EFS performance in relation to NFS mount options?
- () Use FTP instead of NFS
- () Use NFSv4.0
- **() Use NFSv4.1** [CORRECT]
- () Use TFTP instead of NFS
- () Use NFSv4.1 is the correct answer. NFSv4.1 improves performance over NFSv4.0 and should be used whenever possible. Neither FTP nor TFTP improve performance over NFS and are not available as an NFS mount configuration option.

**Answer:**
Correct Answer: **Use NFSv4.1**

**Explanation:**
Use NFSv4.1 is the correct answer. NFSv4.1 improves performance over NFSv4.0 and should be used whenever possible. Neither FTP nor TFTP improve performance over NFS and are not available as an NFS mount configuration option.

---

## Question 102

**Q:** You work for a large software company in Seattle. The company has its production environment provisioned on AWS inside a custom VPC. The VPC contains both a public subnet and a private subnet. The company tests its applications on custom EC2 instances inside a private subnet. There are approximately 500 instances, and they communicate to the outside world via a proxy server. At 3 A.M. every night, the EC2 instances pull down OS updates, which are usually 150MB or so. They then apply these updates and reboot; however, if the software has not downloaded within half an hour, the update will attempt to download the following day. You notice that a number of EC2 instances are continually failing to download the updates in the allotted time. Which of the following answers might explain this failure? (Choose two.)

**Options:**
- (A) The proxy server has only one Elastic IP address added to it. To increase network throughput, you should add additional Elastic IP addresses.
- (B) Your proxy server is blacklisting the address from which the updates are being downloaded, resulting in failed downloads.
- (C) Correct selection
- (D) The proxy server is in a private subnet and uses a NAT gateway instance to connect to the Internet. However, this instance is too small to handle the required network traffic. You should re-provision the NAT gateway instance so that it’s able to handle the throughput.
- (E) The proxy server has an inadequately sized EBS volume attached to it. The network buffer is stored on the EBS volume, and it is running out of disk space when trying to buffer the 500 simultaneous connections. You should provision an EBS volume with provisioned IOPS.
- (F) The proxy server is on an inadequately sized EC2 instance and does not have sufficient network throughput to handle all updates simultaneously. You should increase the instance size of the EC2 instance for the proxy server.
- (G) Correct Answers:
- (H) Incorrect Answers:
- (I) Your proxy server is blacklisting the address from which the updates are being downloaded, resulting in failed downloads is incorrect because there is no data point stating that the proxy server is blacklisting.
- (J) The proxy server has only one Elastic IP address added to it. To increase network throughput, you should add additional Elastic IP addresses is incorrect because adding elastic IP does not increase network throughput. 
- () The proxy server has an inadequately sized EBS volume attached to it. The network buffer is stored on the EBS volume, and it is running out of disk space when trying to buffer the 500 simultaneous connections. You should provision an EBS volume with provisioned IOPS is incorrect because there is no data point stating that the EBS volume is running out of space.
- () For which of the following does the AWS Trusted Adviser service offer advice? (Choose two.)
- () Whether MFA is configured on the root account
- () Antivirus protection on EC2 instances
- () Vulnerability scans on existing VPCs
- () Advice on security groups and what ports have unrestricted access
- () Whether MFA is configured on the root account and Advice on security groups and what ports have unrestricted access are correct. Trusted Advisor provides more than 40 different types of checks to make sure you are running your infrastructure in AWS in the most optimized way. It can check whether multifactor authentication (MFA) is configured on the root account as well as provide advice on security groups and what ports have unrestricted access.
- () Antivirus protection on EC2 instances is incorrect because Trusted Advisor does not provide antivirus protection.
- () Vulnerability scans on existing VPCs is incorrect because Trusted Advisor does not perform vulnerability scans on VPCs.
- () What can be configured to optimize EFS performance in relation to NFS mount options?
- () Use FTP instead of NFS
- () Use NFSv4.0
- () Use NFSv4.1
- () Use TFTP instead of NFS
- () Use NFSv4.1 is the correct answer. NFSv4.1 improves performance over NFSv4.0 and should be used whenever possible. Neither FTP nor TFTP improve performance over NFS and are not available as an NFS mount configuration option.
- () What is the up-front cost incurred by creating S3 buckets?
- () Variable depending on bucket configuration parameters
- **() $0** [CORRECT]
- () $10 per bucket
- () $100 per bucket
- () $0 is the correct answer. The creation of S3 buckets does not incur cost. Costs accrue based on the usage of the bucket (storage consumed and data transferred).

**Answer:**
Correct Answer: **$0**

**Explanation:**
$0 is the correct answer. The creation of S3 buckets does not incur cost. Costs accrue based on the usage of the bucket (storage consumed and data transferred).

---

## Question 103

**Q:** For which of the following does the AWS Trusted Adviser service offer advice? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Whether MFA is configured on the root account
- (C) Antivirus protection on EC2 instances
- (D) Vulnerability scans on existing VPCs
- (E) Advice on security groups and what ports have unrestricted access
- (F) Whether MFA is configured on the root account and Advice on security groups and what ports have unrestricted access are correct. Trusted Advisor provides more than 40 different types of checks to make sure you are running your infrastructure in AWS in the most optimized way. It can check whether multifactor authentication (MFA) is configured on the root account as well as provide advice on security groups and what ports have unrestricted access.
- (G) Incorrect Answers:
- (H) Antivirus protection on EC2 instances is incorrect because Trusted Advisor does not provide antivirus protection.
- (I) Vulnerability scans on existing VPCs is incorrect because Trusted Advisor does not perform vulnerability scans on VPCs.
- (J) What can be configured to optimize EFS performance in relation to NFS mount options?
- () Use FTP instead of NFS
- () Use NFSv4.0
- () Use NFSv4.1
- () Use TFTP instead of NFS
- () Use NFSv4.1 is the correct answer. NFSv4.1 improves performance over NFSv4.0 and should be used whenever possible. Neither FTP nor TFTP improve performance over NFS and are not available as an NFS mount configuration option.
- () What is the up-front cost incurred by creating S3 buckets?
- () Variable depending on bucket configuration parameters
- () $0
- () $10 per bucket
- () $100 per bucket
- () $0 is the correct answer. The creation of S3 buckets does not incur cost. Costs accrue based on the usage of the bucket (storage consumed and data transferred).
- () How should you enforce the use of an 8-character password for all AWS logins?
- **() Through a password policy** [CORRECT]
- () For each login created
- () For each group
- () You cannot enforce such settings
- () Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

**Answer:**
Correct Answer: **Through a password policy**

**Explanation:**
Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

---

## Question 104

**Q:** What can be configured to optimize EFS performance in relation to NFS mount options?

**Options:**
- (A) Use FTP instead of NFS
- (B) Use NFSv4.0
- (C) Use NFSv4.1
- (D) Use TFTP instead of NFS
- (E) Use NFSv4.1 is the correct answer. NFSv4.1 improves performance over NFSv4.0 and should be used whenever possible. Neither FTP nor TFTP improve performance over NFS and are not available as an NFS mount configuration option.
- (F) What is the up-front cost incurred by creating S3 buckets?
- (G) Variable depending on bucket configuration parameters
- (H) $0
- (I) $10 per bucket
- (J) $100 per bucket
- () $0 is the correct answer. The creation of S3 buckets does not incur cost. Costs accrue based on the usage of the bucket (storage consumed and data transferred).
- () How should you enforce the use of an 8-character password for all AWS logins?
- **() Through a password policy** [CORRECT]
- () For each login created
- () For each group
- () You cannot enforce such settings
- () Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

**Answer:**
Correct Answer: **Through a password policy**

**Explanation:**
Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

---

## Question 105

**Q:** What is the up-front cost incurred by creating S3 buckets?

**Options:**
- (A) Variable depending on bucket configuration parameters
- (B) $0
- (C) $10 per bucket
- (D) $100 per bucket
- (E) $0 is the correct answer. The creation of S3 buckets does not incur cost. Costs accrue based on the usage of the bucket (storage consumed and data transferred).
- (F) How should you enforce the use of an 8-character password for all AWS logins?
- **(G) Through a password policy** [CORRECT]
- (H) For each login created
- (I) For each group
- (J) You cannot enforce such settings
- () Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

**Answer:**
Correct Answer: **Through a password policy**

**Explanation:**
Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

---

## Question 106

**Q:** How should you enforce the use of an 8-character password for all AWS logins?

**Options:**
- **(A) Through a password policy** [CORRECT]
- (B) For each login created
- (C) For each group
- (D) You cannot enforce such settings
- (E) Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

**Answer:**
Correct Answer: **Through a password policy**

**Explanation:**
Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

---

## Question 107

**Q:** What solution is the least expensive, within AWS, for long-term data storage and archives?

**Options:**
- (A) Snowball
- (B) S3 Standard
- (C) Redshift
- (D) Glacier
- (E) Glacier is the correct answer. Glacier is the best option among those listed for long-term storage at lower cost. Snowball is used to move data into the cloud using an offline device. Redshift is an OLAP data warehouse database. S3 standard could be used, but it is more expensive than Glacier for long-term storage.
- (F) Which one of the following languages is not supported by Elastic Beanstalk?
- (G) Java
- (H) Python
- **(I) Perl** [CORRECT]
- (J) Node.js
- () Perl is the correct answer. Perl is not supported by Elastic Beanstalk. Java, .NET, Node.js, PHP, Ruby, Python, and Go are supported.

**Answer:**
Correct Answer: **Perl**

**Explanation:**
Perl is the correct answer. Perl is not supported by Elastic Beanstalk. Java, .NET, Node.js, PHP, Ruby, Python, and Go are supported.

---

## Question 108

**Q:** Which one of the following languages is not supported by Elastic Beanstalk?

**Options:**
- (A) Java
- (B) Python
- **(C) Perl** [CORRECT]
- (D) Node.js
- (E) Perl is the correct answer. Perl is not supported by Elastic Beanstalk. Java, .NET, Node.js, PHP, Ruby, Python, and Go are supported.

**Answer:**
Correct Answer: **Perl**

**Explanation:**
Perl is the correct answer. Perl is not supported by Elastic Beanstalk. Java, .NET, Node.js, PHP, Ruby, Python, and Go are supported.

---

## Question 109

**Q:** Your client has been experiencing problems with their aging in-house infrastructure and is extremely concerned about managing the cost of maintaining their online presence. After deciding that the cost of developing a sound DR plan more than makes up for the negative impact of being offline, the board has directed you to prepare a proposal that achieves an RTO of 20 hours, an RPO of 1 hour, and keeps the costs of meeting those target time windows to a minimum. They have also mandated the use of the AWS Storage Gateway to mitigate the risk associated with a catastrophic NAS failure. Which of the following solutions best meet the requirements?

**Options:**
- (A) Provide their engineering staff with an AWS account and create IAM users, groups, and roles. Use CloudFormation/CloudFormer to clone the existing on-premises environment and store the build scripts in GitHub. Migrate the in-house DNS to Route 53 to simplify cutover. Set up the Storage Gateway and the Snapshot schedule to meet the RPO. Provide the engineering team with a CLI script to kick-start the CloudFormation build and restoration of the Storage Gateway snapshots.
- (B) Provide their engineering staff with an AWS account. Create a small, under-sized DR DB instance and use application synchronization to keep the DR instance synchronized within 30 seconds of the production instance. Build one of each web/app server and keep these patched and online. Provide the Ops team with written instructions explaining how to upgrade the DB host to a full-sized instance within 20 minutes.
- (C) Provide their engineering staff with an AWS account, and ask them to rebuild all the servers in AWS to form a fully functional hot-standby environment. Use Storage Gateway to copy the data on the NAS to S3 so that it can be accessed by the database servers.
- **(D) Work with the customer’s engineers to identify the key servers and data. Help them set up an AWS account with IAM users, groups, and roles. Build templates of the critical web/app servers and save these as AMIs. Agree upon RDS specifications that meet the stated requirements. Set up the Storage Gateway and the Snapshot schedule to meet the RPO. Document, script, or automate the steps to initiate the RDS instance, the EC2 instances, the steps to restore the latest data from the Storage Gateway snapshots into RDS, plus any DNS changes. Test the process with each of the operations team’s shifts.** [CORRECT]
- (E) There are three key aspects: RTO, RPO, and cost. All three must be balanced and meet objectives for the design to be considered acceptable. 
- (F) Incorrect Answers:
- (G) Provide their engineering staff with an AWS account, and ask them to rebuild all the servers in AWS to form a fully functional hot-standby environment. Use Storage Gateway to copy the data on the NAS to S3 so that it can be accessed by the database servers is incorrect because you won’t be able to meet the RTO and RPO objectives using this.
- (H) Provide their engineering staff with an AWS account, and ask them to rebuild all the servers in AWS to form a fully functional hot-standby environment. Use Storage Gateway to copy the data on the NAS to S3 so that it can be accessed by the database servers is incorrect because it doesn’t exactly tell how you are going to meet the 1-hour RPO.
- (I) Provide their engineering staff with an AWS account. Create a small, under-sized DR DB instance and use application synchronization to keep the DR instance synchronized within 30 seconds of the production instance. Build one of each web/app server and keep these patched and online. Provide the Ops team with written instructions explaining how to upgrade the DB host to a full-sized instance within 20 minutes is incorrect because it will cause the costs to rise.

**Answer:**
Correct Answer: **Work with the customer’s engineers to identify the key servers and data. Help them set up an AWS account with IAM users, groups, and roles. Build templates of the critical web/app servers and save these as AMIs. Agree upon RDS specifications that meet the stated requirements. Set up the Storage Gateway and the Snapshot schedule to meet the RPO. Document, script, or automate the steps to initiate the RDS instance, the EC2 instances, the steps to restore the latest data from the Storage Gateway snapshots into RDS, plus any DNS changes. Test the process with each of the operations team’s shifts.**

**Explanation:**
Work with the customer’s engineers to identify the key servers and data. Help them set up an AWS account with IAM users, groups, and roles. Build templates of the critical web/app servers and save these as AMIs. Agree upon RDS specifications that meet the stated requirements. Set up the Storage Gateway and the Snapshot schedule to meet the RPO. Document, script, or automate the steps to initiate the RDS instance, the EC2 instances, the steps to restore the latest data from the Storage Gateway snapshots into RDS, plus any DNS changes. Test the process with each of the operations team’s shifts is correct.

---

## Question 110

**Q:** Given that Elastic Beanstalk automatically creates the environment to run your application code, what is the extra cost associated with its use?

**Options:**
- (A) $0.25 per minute required to create the environment
- (B) $50 per application
- (C) No extra cost
- (D) $100 per application
- (E) No extra cost is the correct answer. There is no extra cost associated with using Elastic Beanstalk. You are charged for the resources used to actually run the application, but are not charged to implement the environment required.
- (F) To how many maximum elements can a single EC2 instance be attached?
- (G) 28
- (H) 28 is the correct answer. An EC2 instance can be attached to up to 28 elements, such as network interfaces and EBS volumes. For example, if you attach one network interface, you can also attach 27 EBS volumes.
- (I) What EC2 instance type can be used to provide up to a 90% discount off on-demand instance prices?
- (J) Reduced Cost instance
- **() Spot instance** [CORRECT]
- () Downgraded instance
- () Automatic instance

**Answer:**
Correct Answer: **Spot instance**

**Explanation:**
Spot instance is the correct answer. Spot instances run whenever capacity is available and the maximum price for a request exceeds the Spot price, according to AWS documentation. They should only when your process includes the flexibility of running with interruption and running whenever it can as opposed to specific required times. On-Demand instances are also used when you desire to reduce costs over always-on instances (typical EC2 instances) but allows for launching at specific required times. The other instance types listed do not exist in AWS.

---

## Question 111

**Q:** To how many maximum elements can a single EC2 instance be attached?

**Options:**
- (A) 28
- (B) 28 is the correct answer. An EC2 instance can be attached to up to 28 elements, such as network interfaces and EBS volumes. For example, if you attach one network interface, you can also attach 27 EBS volumes.
- (C) What EC2 instance type can be used to provide up to a 90% discount off on-demand instance prices?
- (D) Reduced Cost instance
- **(E) Spot instance** [CORRECT]
- (F) Downgraded instance
- (G) Automatic instance

**Answer:**
Correct Answer: **Spot instance**

**Explanation:**
Spot instance is the correct answer. Spot instances run whenever capacity is available and the maximum price for a request exceeds the Spot price, according to AWS documentation. They should only when your process includes the flexibility of running with interruption and running whenever it can as opposed to specific required times. On-Demand instances are also used when you desire to reduce costs over always-on instances (typical EC2 instances) but allows for launching at specific required times. The other instance types listed do not exist in AWS.

---

## Question 112

**Q:** What EC2 instance type can be used to provide up to a 90% discount off on-demand instance prices?

**Options:**
- (A) Reduced Cost instance
- **(B) Spot instance** [CORRECT]
- (C) Downgraded instance
- (D) Automatic instance

**Answer:**
Correct Answer: **Spot instance**

**Explanation:**
Spot instance is the correct answer. Spot instances run whenever capacity is available and the maximum price for a request exceeds the Spot price, according to AWS documentation. They should only when your process includes the flexibility of running with interruption and running whenever it can as opposed to specific required times. On-Demand instances are also used when you desire to reduce costs over always-on instances (typical EC2 instances) but allows for launching at specific required times. The other instance types listed do not exist in AWS.

---

## Question 113

**Q:** To audit the API calls made to your account, which AWS service would you use?

**Options:**
- (A) AWS CloudTrail
- (B) AWS CloudWatch
- (C) AWS Lambda
- (D) AWS Systems Manager
- (E) AWS CloudTrail is correct. AWS CloudTrail is used to audit the API calls.
- (F) Incorrect Answers:
- (G) AWS Systems Manager is incorrect because AWS Systems Manager gives you visibility into and control over your infrastructure in AWS.
- (H) AWS Lambda is incorrect because AWS Lambda lets you run code without provisioning or managing servers.
- (I) AWS CloudWatch is incorrect because AWS CloudWatch is used to monitor AWS resources like EC2 servers, and it provides various metrics in terms of CPU, memory, and so on.
- (J) What should be implemented to ensure security when using AWS Access Keys?
- () Key Decryption
- () Key Encryption
- () Password-protected keys
- () Key Rotation
- () Key rotation is the correct answer. Key rotation is used to retire older keys. The longer keys are used, the more likely they have been compromised. Rotate keys by generating new keys, updating applications and users with the new keys, deactivating the old keys, monitoring to ensure you've captured all of the use cases for the keys.
- () What cannot be specified for an S3 bucket?
- () The name
- () Encryption
- **() The Availability Zone (AZ)** [CORRECT]
- () The permissions
- () The Availability Zone (AZ) is the correct answer. While S3 buckets are stored in an AZ, you cannot specify into which AZ it should be placed. Regardless of the S3 storage class, the AZ is selected automatically by AWS.

**Answer:**
Correct Answer: **The Availability Zone (AZ)**

**Explanation:**
The Availability Zone (AZ) is the correct answer. While S3 buckets are stored in an AZ, you cannot specify into which AZ it should be placed. Regardless of the S3 storage class, the AZ is selected automatically by AWS.

---

## Question 114

**Q:** What should be implemented to ensure security when using AWS Access Keys?

**Options:**
- (A) Key Decryption
- (B) Key Encryption
- (C) Password-protected keys
- (D) Key Rotation
- (E) Key rotation is the correct answer. Key rotation is used to retire older keys. The longer keys are used, the more likely they have been compromised. Rotate keys by generating new keys, updating applications and users with the new keys, deactivating the old keys, monitoring to ensure you've captured all of the use cases for the keys.
- (F) What cannot be specified for an S3 bucket?
- (G) The name
- (H) Encryption
- **(I) The Availability Zone (AZ)** [CORRECT]
- (J) The permissions
- () The Availability Zone (AZ) is the correct answer. While S3 buckets are stored in an AZ, you cannot specify into which AZ it should be placed. Regardless of the S3 storage class, the AZ is selected automatically by AWS.

**Answer:**
Correct Answer: **The Availability Zone (AZ)**

**Explanation:**
The Availability Zone (AZ) is the correct answer. While S3 buckets are stored in an AZ, you cannot specify into which AZ it should be placed. Regardless of the S3 storage class, the AZ is selected automatically by AWS.

---

## Question 115

**Q:** What cannot be specified for an S3 bucket?

**Options:**
- (A) The name
- (B) Encryption
- **(C) The Availability Zone (AZ)** [CORRECT]
- (D) The permissions
- (E) The Availability Zone (AZ) is the correct answer. While S3 buckets are stored in an AZ, you cannot specify into which AZ it should be placed. Regardless of the S3 storage class, the AZ is selected automatically by AWS.

**Answer:**
Correct Answer: **The Availability Zone (AZ)**

**Explanation:**
The Availability Zone (AZ) is the correct answer. While S3 buckets are stored in an AZ, you cannot specify into which AZ it should be placed. Regardless of the S3 storage class, the AZ is selected automatically by AWS.

---

## Question 116

**Q:** You have been engaged by a company to design and lead a migration to an AWS environment. The team is concerned about the capabilities of the new environment, especially when it comes to avoiding all bottlenecks. The design calls for about 20 instances (C3.2xLarge) pulling jobs/messages from SQS. Network traffic per instance is estimated to be around 500Mbps at the beginning and end of each job. Which network configuration should you plan on deploying?

**Options:**
- (A) Activate EBS-Optimization on the instance to maximize network throughput.
- (B) Use a second network interface to separate the SQS traffic from the storage traffic.
- (C) Choose a different instance type that better matched the traffic demand.
- (D) Deploy as a placement group, as the aggregated burst traffic could be around 10Gbps.
- (E) Spread the instances over multiple AZs to minimize the traffic concentration and maximize the fault tolerance.
- (F) Incorrect Answers:
- (G) Choose a different instance type that better matched the traffic demand is incorrect because even if you choose a different instance type, you still won’t be distributing your network traffic.
- (H) Use a second network interface to separate the SQS traffic from the storage traffic is incorrect because you can just separate the SQS traffic with a second network card.
- (I) Activate EBS-Optimization on the instance to maximize network throughput is incorrect because the placement group will bring the instance within proximity.
- (J) Spread the instances over multiple AZs to minimize the traffic concentration and maximize the fault tolerance is incorrect because an EBS-optimized instance will not distribute the network traffic.
- () You must transfer one exabyte of data into AWS and you do not want to transfer it across the Internet. What AWS solution should you use?
- () Snowball
- () HTTPS transfer to S3 buckets
- () Snowmobile
- () Direct Connect
- () Snowmobile is the correct answer. AWS Snowmobile supports exabyte-scale data transfer. The Snowmobile is connected to your network, the data is transferred to the Snowmobile, and then it is physically transported to an AWS data center and transferred to the cloud. The Snowball solution can handle up to 80 TB of data. Both Direct Connect and HTTPS transfer to S3 buckets that would transfer across the Internet in some way.
- () You must attach an EBS volume to an EC2 instance that offers 500 GiB of storage at the lowest cost. What EBS type should be used?
- () Throughput-optimized HDD
- () Provisioned IOPS
- **() Cold HDD** [CORRECT]
- () General SSD
- () Cold HDD is the correct answer. Cold HDD is the lowest cost storage solution. General (or General Purpose) SSD is more expensive, though not as expensive as Provisioned IOPS. Throughput-optimized HDD is magnetic storage, like Cold HDD, but is not as inexpensive as Cold HDD.

**Answer:**
Correct Answer: **Cold HDD**

**Explanation:**
Cold HDD is the correct answer. Cold HDD is the lowest cost storage solution. General (or General Purpose) SSD is more expensive, though not as expensive as Provisioned IOPS. Throughput-optimized HDD is magnetic storage, like Cold HDD, but is not as inexpensive as Cold HDD.

---

## Question 117

**Q:** You must transfer one exabyte of data into AWS and you do not want to transfer it across the Internet. What AWS solution should you use?

**Options:**
- (A) Snowball
- (B) HTTPS transfer to S3 buckets
- (C) Snowmobile
- (D) Direct Connect
- (E) Snowmobile is the correct answer. AWS Snowmobile supports exabyte-scale data transfer. The Snowmobile is connected to your network, the data is transferred to the Snowmobile, and then it is physically transported to an AWS data center and transferred to the cloud. The Snowball solution can handle up to 80 TB of data. Both Direct Connect and HTTPS transfer to S3 buckets that would transfer across the Internet in some way.
- (F) You must attach an EBS volume to an EC2 instance that offers 500 GiB of storage at the lowest cost. What EBS type should be used?
- (G) Throughput-optimized HDD
- (H) Provisioned IOPS
- **(I) Cold HDD** [CORRECT]
- (J) General SSD
- () Cold HDD is the correct answer. Cold HDD is the lowest cost storage solution. General (or General Purpose) SSD is more expensive, though not as expensive as Provisioned IOPS. Throughput-optimized HDD is magnetic storage, like Cold HDD, but is not as inexpensive as Cold HDD.

**Answer:**
Correct Answer: **Cold HDD**

**Explanation:**
Cold HDD is the correct answer. Cold HDD is the lowest cost storage solution. General (or General Purpose) SSD is more expensive, though not as expensive as Provisioned IOPS. Throughput-optimized HDD is magnetic storage, like Cold HDD, but is not as inexpensive as Cold HDD.

---

## Question 118

**Q:** You must attach an EBS volume to an EC2 instance that offers 500 GiB of storage at the lowest cost. What EBS type should be used?

**Options:**
- (A) Throughput-optimized HDD
- (B) Provisioned IOPS
- **(C) Cold HDD** [CORRECT]
- (D) General SSD
- (E) Cold HDD is the correct answer. Cold HDD is the lowest cost storage solution. General (or General Purpose) SSD is more expensive, though not as expensive as Provisioned IOPS. Throughput-optimized HDD is magnetic storage, like Cold HDD, but is not as inexpensive as Cold HDD.

**Answer:**
Correct Answer: **Cold HDD**

**Explanation:**
Cold HDD is the correct answer. Cold HDD is the lowest cost storage solution. General (or General Purpose) SSD is more expensive, though not as expensive as Provisioned IOPS. Throughput-optimized HDD is magnetic storage, like Cold HDD, but is not as inexpensive as Cold HDD.

---

## Question 119

**Q:** In addition to database instance class and redundancy options (such as Multi-AZ configurations), what has the most significant impact on the direct cost for RDS databases?

**Options:**
- (A) The use of EC2 instances to access the database
- (B) The use of remote clients to access the database
- (C) The database engine in use
- (D) The creation of snapshots
- (E) The database engine in use is the correct answer. You can download, from AWS S3 to your local network, up to 1 GB per month at no charge. The other listed ranges are the pricing scales as of 2020. For example, from 1 GB to 9.999 TB is $0.09 per GB of transfer. From 10 TB to 40 TB is $0.085 per GB of transfer. And from 40 TB to 100 TB is $0.07 per GB of transfer.
- (F) You must plan a Route 53 deployment in AWS. What routing policy is used to send all traffic to a single resource?
- (G) Geolocation routing
- **(H) Simple routing** [CORRECT]
- (I) Latency-based routing
- (J) Route 53 is not used in this way
- () Simple routing is the correct answer. Simple routing routes all traffic to a particular resource. This is typical DNS name resolution. Geolocation routing routes based on the location of the requestor. Latency-based routing routes based on the delay in communications between the source and the various possible resources.

**Answer:**
Correct Answer: **Simple routing**

**Explanation:**
Simple routing is the correct answer. Simple routing routes all traffic to a particular resource. This is typical DNS name resolution. Geolocation routing routes based on the location of the requestor. Latency-based routing routes based on the delay in communications between the source and the various possible resources.

---

## Question 120

**Q:** You must plan a Route 53 deployment in AWS. What routing policy is used to send all traffic to a single resource?

**Options:**
- (A) Geolocation routing
- **(B) Simple routing** [CORRECT]
- (C) Latency-based routing
- (D) Route 53 is not used in this way
- (E) Simple routing is the correct answer. Simple routing routes all traffic to a particular resource. This is typical DNS name resolution. Geolocation routing routes based on the location of the requestor. Latency-based routing routes based on the delay in communications between the source and the various possible resources.

**Answer:**
Correct Answer: **Simple routing**

**Explanation:**
Simple routing is the correct answer. Simple routing routes all traffic to a particular resource. This is typical DNS name resolution. Geolocation routing routes based on the location of the requestor. Latency-based routing routes based on the delay in communications between the source and the various possible resources.

---

## Question 121

**Q:** When policies can be written in a language in AWS, what language is most often used?

**Options:**
- (A) Python
- (B) HTML
- **(C) JSON** [CORRECT]
- (D) YAML
- (E) JSON is the correct answer. JSON is the most common language used for policy creation in AWS. JSON stands for JavaScript Object Notation.

**Answer:**
Correct Answer: **JSON**

**Explanation:**
JSON is the correct answer. JSON is the most common language used for policy creation in AWS. JSON stands for JavaScript Object Notation.

---

## Question 122

**Q:** What can be easily implemented to segregate a group of servers from the rest of your AWS cloud so that the servers can communicate with each other and the Internet, but not with other servers in your cloud?

**Options:**
- (A) Availability Zone (AZ)
- (B) AWS Marketplace AMIs
- (C) VPN
- (D) VPC
- (E) VPC is the correct answer. A Virtual Private Cloud (VPC) can be created and instances can be placed in the VPC and allowed to communicate with each other and the Internet. If you do not enable the VPC to communicate with other VPCs, the server instances in one VPC cannot communicate with the instances in other VPCs. Availability Zones and AMIs do not directly provide for this. A VPN also does not provide this solution.
- (F) Which of the following statements are true regarding SAML-enabled single sign-on? (Choose two.)
- (G) Correct selection
- (H) The portal first verifies the user's identity in the organization and then generates a SAML authentication response.
- (I) The client browser is immediately directed to the AWS Console.
- (J) The portal acknowledges a SAML authentication response and then verifies the user’s identity in the organization.
- () After the client browser posts the SAML assertion, AWS sends the sign-in URL as a redirect and then the client browser is redirected to the Console.
- () Correct Answers:
- () Incorrect Answers:
- () The client browser is immediately directed to the AWS Console and The portal acknowledges a SAML authentication response and then verifies the user’s identity in the organization are incorrect. The true statements regarding SAML-enabled single sign-on are provided in answers A and D.
- () What is the default upload operation type for data transferred to an S3 bucket?
- () A single PUT operation
- () FTP transmission
- () sFTP transmission
- () A multi-part PUT operation
- () A single PUT operation is the correct answer. By default, all files transferred to an S3 bucket are transferred using a single PUT operation. AWS suggests that files up to 100 MB in size can be transferred using this default operation. Larger files may require uploads through multi-part operations.
- () You want to provide multiple virtual hard disks to an EC2 instance. What can you attach to an instance to provide these virtual hard disks?
- () EIP
- () NACL
- **() EBS volume** [CORRECT]
- () Which one of the following resources cannot be automatically scaled with AWS Auto Scaling?
- () EC2 Auto Scaling groups

**Answer:**
Correct Answer: **EBS volume**

**Explanation:**
EBS volume is the correct answer. Multiple Elastic Block Store (EBS) volumes can be attached to an EC2 instance to act as hard disks. Several EBS volume types exist providing different performance levels. A VPC is not a virtual hard disk, but a virtual network segment. A NACL is a network access control list used to function as a firewall for a VPC. An Elastic IP (EIP) address is a statically assigned IP address that can be purchased for an instance by associating it with an Elastic Network Interface (ENI) bound to the instance.

---

## Question 123

**Q:** Which of the following statements are true regarding SAML-enabled single sign-on? (Choose two.)

**Options:**
- (A) Correct selection
- (B) The portal first verifies the user's identity in the organization and then generates a SAML authentication response.
- (C) The client browser is immediately directed to the AWS Console.
- (D) The portal acknowledges a SAML authentication response and then verifies the user’s identity in the organization.
- (E) After the client browser posts the SAML assertion, AWS sends the sign-in URL as a redirect and then the client browser is redirected to the Console.
- (F) Correct Answers:
- (G) Incorrect Answers:
- (H) The client browser is immediately directed to the AWS Console and The portal acknowledges a SAML authentication response and then verifies the user’s identity in the organization are incorrect. The true statements regarding SAML-enabled single sign-on are provided in answers A and D.
- (I) What is the default upload operation type for data transferred to an S3 bucket?
- (J) A single PUT operation
- () FTP transmission
- () sFTP transmission
- () A multi-part PUT operation
- () A single PUT operation is the correct answer. By default, all files transferred to an S3 bucket are transferred using a single PUT operation. AWS suggests that files up to 100 MB in size can be transferred using this default operation. Larger files may require uploads through multi-part operations.
- () You want to provide multiple virtual hard disks to an EC2 instance. What can you attach to an instance to provide these virtual hard disks?
- () EIP
- () VPC
- () NACL
- () EBS volume
- () Which one of the following resources cannot be automatically scaled with AWS Auto Scaling?
- () EC2 Auto Scaling groups
- **() Microsoft SQL Server RDS databases** [CORRECT]
- () DynamoDB tables
- () Aurora DB clusters
- () Microsoft SQL Server RDS databases is the correct answer. You cannot scale Microsoft SQL Server or Oracle databases hosted in RDS. You can scale EC2 Auto Scaling groups, Aurora DB clusters, DynamoDB tables, DynamoDB global secondary indexes, ECS services, and Spot Fleet requests.
- () To establish a successful site-to-site VPN connection from your on-premises network to an AWS virtual private cloud, which of the following must be configured? (Choose three.)

**Answer:**
Correct Answer: **Microsoft SQL Server RDS databases**

**Explanation:**
Microsoft SQL Server RDS databases is the correct answer. You cannot scale Microsoft SQL Server or Oracle databases hosted in RDS. You can scale EC2 Auto Scaling groups, Aurora DB clusters, DynamoDB tables, DynamoDB global secondary indexes, ECS services, and Spot Fleet requests.

---

## Question 124

**Q:** What is the default upload operation type for data transferred to an S3 bucket?

**Options:**
- (A) A single PUT operation
- (B) FTP transmission
- (C) sFTP transmission
- (D) A multi-part PUT operation
- (E) A single PUT operation is the correct answer. By default, all files transferred to an S3 bucket are transferred using a single PUT operation. AWS suggests that files up to 100 MB in size can be transferred using this default operation. Larger files may require uploads through multi-part operations.
- (F) You want to provide multiple virtual hard disks to an EC2 instance. What can you attach to an instance to provide these virtual hard disks?
- (G) EIP
- (H) VPC
- (I) NACL
- (J) EBS volume
- () Which one of the following resources cannot be automatically scaled with AWS Auto Scaling?
- () EC2 Auto Scaling groups
- **() Microsoft SQL Server RDS databases** [CORRECT]
- () DynamoDB tables
- () Aurora DB clusters
- () Microsoft SQL Server RDS databases is the correct answer. You cannot scale Microsoft SQL Server or Oracle databases hosted in RDS. You can scale EC2 Auto Scaling groups, Aurora DB clusters, DynamoDB tables, DynamoDB global secondary indexes, ECS services, and Spot Fleet requests.
- () To establish a successful site-to-site VPN connection from your on-premises network to an AWS virtual private cloud, which of the following must be configured? (Choose three.)
- () Correct selection
- () A virtual private gateway
- () A private subnet in your VPC
- () An on-premises customer gateway
- () A NAT instance
- () A VPC with hardware VPN access
- () Correct Answers:
- () An on-premises customer gateway, A virtual private gateway,and A VPC with hardware VPN access are correct.
- () You must have a VPC with hardware VPN access, an on-premises customer gateway, and a virtual private gateway to make the VPN connection work. 
- () Incorrect Answers:
- () A NAT instance is incorrect because a NAT instance is not needed for a successful VPN connection.
- () A private subnet in your VPC is incorrect because a private subnet doesn’t have any correlation with a VPN connection.

**Answer:**
Correct Answer: **Microsoft SQL Server RDS databases**

**Explanation:**
Microsoft SQL Server RDS databases is the correct answer. You cannot scale Microsoft SQL Server or Oracle databases hosted in RDS. You can scale EC2 Auto Scaling groups, Aurora DB clusters, DynamoDB tables, DynamoDB global secondary indexes, ECS services, and Spot Fleet requests.

---

## Question 125

**Q:** You want to provide multiple virtual hard disks to an EC2 instance. What can you attach to an instance to provide these virtual hard disks?

**Options:**
- (A) EIP
- (B) VPC
- (C) NACL
- (D) EBS volume
- (E) Which one of the following resources cannot be automatically scaled with AWS Auto Scaling?
- (F) EC2 Auto Scaling groups
- (G) Microsoft SQL Server RDS databases
- (H) DynamoDB tables
- (I) Aurora DB clusters
- (J) Microsoft SQL Server RDS databases is the correct answer. You cannot scale Microsoft SQL Server or Oracle databases hosted in RDS. You can scale EC2 Auto Scaling groups, Aurora DB clusters, DynamoDB tables, DynamoDB global secondary indexes, ECS services, and Spot Fleet requests.
- () To establish a successful site-to-site VPN connection from your on-premises network to an AWS virtual private cloud, which of the following must be configured? (Choose three.)
- () Correct selection
- () A virtual private gateway
- () A private subnet in your VPC
- () An on-premises customer gateway
- () A NAT instance
- () A VPC with hardware VPN access
- () Correct Answers:
- () An on-premises customer gateway, A virtual private gateway,and A VPC with hardware VPN access are correct.
- () You must have a VPC with hardware VPN access, an on-premises customer gateway, and a virtual private gateway to make the VPN connection work. 
- () Incorrect Answers:
- () A NAT instance is incorrect because a NAT instance is not needed for a successful VPN connection.
- () A private subnet in your VPC is incorrect because a private subnet doesn’t have any correlation with a VPN connection.
- () What is a security best practice that should be implemented for the root login immediately after creating an AWS account?
- **() Enable MFA** [CORRECT]
- () Disable MFA
- () Delete the root login
- () Enable root login firewalling
- () Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.

**Answer:**
Correct Answer: **Enable MFA**

**Explanation:**
Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.

---

## Question 126

**Q:** Which one of the following resources cannot be automatically scaled with AWS Auto Scaling?

**Options:**
- (A) EC2 Auto Scaling groups
- (B) Microsoft SQL Server RDS databases
- (C) DynamoDB tables
- (D) Aurora DB clusters
- (E) Microsoft SQL Server RDS databases is the correct answer. You cannot scale Microsoft SQL Server or Oracle databases hosted in RDS. You can scale EC2 Auto Scaling groups, Aurora DB clusters, DynamoDB tables, DynamoDB global secondary indexes, ECS services, and Spot Fleet requests.
- (F) To establish a successful site-to-site VPN connection from your on-premises network to an AWS virtual private cloud, which of the following must be configured? (Choose three.)
- (G) Correct selection
- (H) A virtual private gateway
- (I) A private subnet in your VPC
- (J) An on-premises customer gateway
- () A NAT instance
- () A VPC with hardware VPN access
- () Correct Answers:
- () An on-premises customer gateway, A virtual private gateway,and A VPC with hardware VPN access are correct.
- () You must have a VPC with hardware VPN access, an on-premises customer gateway, and a virtual private gateway to make the VPN connection work. 
- () Incorrect Answers:
- () A NAT instance is incorrect because a NAT instance is not needed for a successful VPN connection.
- () A private subnet in your VPC is incorrect because a private subnet doesn’t have any correlation with a VPN connection.
- () What is a security best practice that should be implemented for the root login immediately after creating an AWS account?
- **() Enable MFA** [CORRECT]
- () Disable MFA
- () Delete the root login
- () Enable root login firewalling
- () Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.
- () Following advice from your consultant, you have configured your VPC to use Dedicated hosting tenancy. A subsequent change to your application has rendered the performance gains from Dedicated tenancy superfluous, and you would now like to recoup some of these greater costs. How do you revert to Default hosting tenancy? (Choose two.)
- () Change tenancy using CLI/SDK.
- () Change the hosting attribute and then restart the instance.
- () Stop each instance, change the hosting attribute, and restart.
- () Create AMIs of all your instances and use them to create new instances using Default hosting.
- () Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy.
- () Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy and Change tenancy using CLI/SDK are correct.
- () Once the VPC is created, the ways to change the tenancy are either create a new VPC with different tenancy and migrate all the instance or use CLI/SDK to change the tenancy. 

**Answer:**
Correct Answer: **Enable MFA**

**Explanation:**
Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.

---

## Question 127

**Q:** To establish a successful site-to-site VPN connection from your on-premises network to an AWS virtual private cloud, which of the following must be configured? (Choose three.)

**Options:**
- (A) Correct selection
- (B) A virtual private gateway
- (C) A private subnet in your VPC
- (D) An on-premises customer gateway
- (E) A NAT instance
- (F) A VPC with hardware VPN access
- (G) Correct Answers:
- (H) An on-premises customer gateway, A virtual private gateway,and A VPC with hardware VPN access are correct.
- (I) You must have a VPC with hardware VPN access, an on-premises customer gateway, and a virtual private gateway to make the VPN connection work. 
- (J) Incorrect Answers:
- () A NAT instance is incorrect because a NAT instance is not needed for a successful VPN connection.
- () A private subnet in your VPC is incorrect because a private subnet doesn’t have any correlation with a VPN connection.
- () What is a security best practice that should be implemented for the root login immediately after creating an AWS account?
- **() Enable MFA** [CORRECT]
- () Disable MFA
- () Delete the root login
- () Enable root login firewalling
- () Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.
- () Following advice from your consultant, you have configured your VPC to use Dedicated hosting tenancy. A subsequent change to your application has rendered the performance gains from Dedicated tenancy superfluous, and you would now like to recoup some of these greater costs. How do you revert to Default hosting tenancy? (Choose two.)
- () Change tenancy using CLI/SDK.
- () Change the hosting attribute and then restart the instance.
- () Stop each instance, change the hosting attribute, and restart.
- () Create AMIs of all your instances and use them to create new instances using Default hosting.
- () Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy.
- () Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy and Change tenancy using CLI/SDK are correct.
- () Once the VPC is created, the ways to change the tenancy are either create a new VPC with different tenancy and migrate all the instance or use CLI/SDK to change the tenancy. 
- () Stop each instance, change the hosting attribute, and restart, Create AMIs of all your instances and use them to create new instances using Default hosting, and Change the hosting attribute and then restart the instance are incorrect.
- () If you create a VPC with a dedicated hosting type of tenancy, you can’t change it. You can either create a new VPC or drop and re-create the existing one.

**Answer:**
Correct Answer: **Enable MFA**

**Explanation:**
Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.

---

## Question 128

**Q:** What is a security best practice that should be implemented for the root login immediately after creating an AWS account?

**Options:**
- **(A) Enable MFA** [CORRECT]
- (B) Disable MFA
- (C) Delete the root login
- (D) Enable root login firewalling
- (E) Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.
- (F) Following advice from your consultant, you have configured your VPC to use Dedicated hosting tenancy. A subsequent change to your application has rendered the performance gains from Dedicated tenancy superfluous, and you would now like to recoup some of these greater costs. How do you revert to Default hosting tenancy? (Choose two.)
- (G) Correct selection
- (H) Change tenancy using CLI/SDK.
- (I) Change the hosting attribute and then restart the instance.
- (J) Stop each instance, change the hosting attribute, and restart.
- () Create AMIs of all your instances and use them to create new instances using Default hosting.
- () Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy.
- () Correct Answers:
- () Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy and Change tenancy using CLI/SDK are correct.
- () Once the VPC is created, the ways to change the tenancy are either create a new VPC with different tenancy and migrate all the instance or use CLI/SDK to change the tenancy. 
- () Incorrect Answers:
- () Stop each instance, change the hosting attribute, and restart, Create AMIs of all your instances and use them to create new instances using Default hosting, and Change the hosting attribute and then restart the instance are incorrect.
- () If you create a VPC with a dedicated hosting type of tenancy, you can’t change it. You can either create a new VPC or drop and re-create the existing one.

**Answer:**
Correct Answer: **Enable MFA**

**Explanation:**
Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.

---

## Question 129

**Q:** Following advice from your consultant, you have configured your VPC to use Dedicated hosting tenancy. A subsequent change to your application has rendered the performance gains from Dedicated tenancy superfluous, and you would now like to recoup some of these greater costs. How do you revert to Default hosting tenancy? (Choose two.)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Change tenancy using CLI/SDK.
- (C) Change the hosting attribute and then restart the instance.
- (D) Stop each instance, change the hosting attribute, and restart.
- (E) Create AMIs of all your instances and use them to create new instances using Default hosting.
- (F) Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy.
- (G) Correct Answers:
- (H) Create AMIs of all your instances. Create a new VPC with Default as the hosting tenancy attribute and then use them to create new instances using Default tenancy and Change tenancy using CLI/SDK are correct.
- (I) Once the VPC is created, the ways to change the tenancy are either create a new VPC with different tenancy and migrate all the instance or use CLI/SDK to change the tenancy. 
- (J) Incorrect Answers:
- () Stop each instance, change the hosting attribute, and restart, Create AMIs of all your instances and use them to create new instances using Default hosting, and Change the hosting attribute and then restart the instance are incorrect.
- () If you create a VPC with a dedicated hosting type of tenancy, you can’t change it. You can either create a new VPC or drop and re-create the existing one.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 130

**Q:** You have been monitoring a sensitive Auto Scaling group, and you expect it to scale in as you enter a period of downtime over the holiday. The Auto Scaling group is distributed over three AZs (AZ -A and AZ -B have two instances each, and AZ -C has three instances). All instances have different CPU and memory utilization levels and have been running for a different number of days. All instances come from different versions of a root AMI and have different numbers of sessions connected. Which instance will be the first to shut down?

**Options:**
- (A) The instance in AZ -C that has the oldest launch configuration will terminate first.
- (B) The instance with the fewest current sessions will terminate first.
- (C) The instance in AZ -C that has the least number of sessions will terminate first.
- (D) The instance in AZ -C that has been running the longest will terminate first.
- (E) The instance that has been running longest will terminate first.
- (F) Incorrect Answers:
- (G) The instance in AZ -C that has been running the longest will terminate first is incorrect because it states that the instance that is running the longest will terminate.
- (H) The instance with the fewest current sessions will terminate first is incorrect because it states that the instance with fewest current sessions will terminate.
- (I) The instance in AZ -C that has the least number of sessions will terminate first is incorrect because it states that the instance with least number of sessions will terminate.
- (J) The instance that has been running longest will terminate first is incorrect because it states that the longest running session will terminate.
- () Dump 3
- () You want to implement a multi-account AWS cloud deployment that more easily complies with business policies during implementation. You wish to implement guardrails that prevent users from taking specific actions that might breech security policies. What AWS service can provide this and works with organizations as well?
- () Amazon EventBridge
- () Amazon Sumerian
- () AWS Glue
- **() AWS Control Tower** [CORRECT]

**Answer:**
Correct Answer: **AWS Control Tower**

**Explanation:**
AWS Control Tower is the correct answer. The one service that provides all the required features is AWS Control Tower. According to AWS documentation, AWS Control Tower provides the easiest way to set up and govern a secure, compliant, multi-account AWS environment. Amazon Sumerian is used for Augmented Reality and Virtual Reality. Amazon EventBridge is used to connect applications to various data sources. AWS Glue is an ETL (extract, transform, and load) tool for data manipulation and transfer.

---

## Question 131

**Q:** You want to implement a multi-account AWS cloud deployment that more easily complies with business policies during implementation. You wish to implement guardrails that prevent users from taking specific actions that might breech security policies. What AWS service can provide this and works with organizations as well?

**Options:**
- (A) Amazon EventBridge
- (B) Amazon Sumerian
- (C) AWS Glue
- **(D) AWS Control Tower** [CORRECT]

**Answer:**
Correct Answer: **AWS Control Tower**

**Explanation:**
AWS Control Tower is the correct answer. The one service that provides all the required features is AWS Control Tower. According to AWS documentation, AWS Control Tower provides the easiest way to set up and govern a secure, compliant, multi-account AWS environment. Amazon Sumerian is used for Augmented Reality and Virtual Reality. Amazon EventBridge is used to connect applications to various data sources. AWS Glue is an ETL (extract, transform, and load) tool for data manipulation and transfer.

---

## Question 132

**Q:** You have a MySQL database running on an EC2 instance in a private subnet. You can connect via SSH, but you are unable to apply updates to the database server via the NAT instance. What might you do to remedy this problem?

**Options:**
- (A) Modify the security group to allow SSH traffic from anywhere.
- (B) Replace the NAT instance.
- **(C) Ensure that “Source/Destination Checks” is disabled on the NAT instance.** [CORRECT]
- (D) Ensure that the security group allows HTTP traffic.
- (E) Incorrect Answers:
- (F) Modify the security group to allow SSH traffic from anywhere is incorrect because this issue is related to NAT and not security groups.
- (G) Replace the NAT instance is incorrect because this is a configuration issue, and replacing the NAT instance won’t solve the problem.
- (H) Ensure that the security group allows HTTP traffic is incorrect because this issue is not related to security groups.

**Answer:**
Correct Answer: **Ensure that “Source/Destination Checks” is disabled on the NAT instance.**

---

## Question 133

**Q:** What is the solution for logging actions taken within the AWS cloud, such as creating resources, deleting resources, and reconfiguring resources?

**Options:**
- **(A) CloudTrail** [CORRECT]
- (B) SQS
- (C) CloudWatch
- (D) SNS
- (E) CloudTrail is the correct answer. AWS CloudTrail is used to audit or log the administrative actions taken within AWS. All actions occur based on API calls and these API action activities are logged. CloudWatch captures performance metrics. SNS is the notification service and SQS is the message queueing service.

**Answer:**
Correct Answer: **CloudTrail**

**Explanation:**
CloudTrail is the correct answer. AWS CloudTrail is used to audit or log the administrative actions taken within AWS. All actions occur based on API calls and these API action activities are logged. CloudWatch captures performance metrics. SNS is the notification service and SQS is the message queueing service.

---

## Question 134

**Q:** You are implementing a web hosting architecture in AWS. Three EC2 instances are in use. The first is a web server, the second an application server, and the third is a database server. The web server communicates with the application server, but not with the database server. The application server communicates with the database server and the web server. Outside uses may access the web server directly, but they cannot access other servers. What kind of secure architecture are you implementing?

**Options:**
- (A) A monolithic secure architecture
- (B) A single-server secure architecture
- **(C) A multi-tier secure architecture** [CORRECT]
- (D) A single-tier secure architecture
- (E) A multi-tier secure architecture is the correct answer. The description is of a multi-tier or n-tier secure architecture – in this case, a three-tier architecture. A single-tier, monolithic, or single-server architecture may refer to the same type of architecture that uses only one tier.

**Answer:**
Correct Answer: **A multi-tier secure architecture**

**Explanation:**
A multi-tier secure architecture is the correct answer. The description is of a multi-tier or n-tier secure architecture – in this case, a three-tier architecture. A single-tier, monolithic, or single-server architecture may refer to the same type of architecture that uses only one tier.

---

## Question 135

**Q:** You are working with roles. When changes are made to roles, when do they take effect?

**Options:**
- (A) When any associate instance is restarted
- (B) Immediately
- (C) When resources become available
- (D) When the active role is not longer actively used
- (E) immediately is the correct answer. Any changes made to roles are effective immediately. There is no delay or wait for resources.
- (F) You are reviewing Change Control requests and note a change designed to reduce wasted CPU cycles by increasing the value of the VisibilityTimeout attribute. What does this mean?
- (G) When the consumer instance polls for new work, the consumer instance will wait a certain amount of time until it has a full workload before closing the connection.
- (H) When the consumer instance polls for new work, the SQS service will allow it to wait a certain amount of time for a message to be available before closing the connection.
- (I) When a new message is added to the SQS queue, it will be hidden from consumer instances for a fixed period of time.
- (J) While processing a message, a consumer instance can amend the message visibility counter by a fixed amount.
- () While processing a message, a consumer instance can reset the message visibility by restarting the preset timeout counter.
- () When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time.
- () When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time is correct. When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time. You have the ability to control this timeout period. 
- () What can be implemented to prevent traffic from the network to your EC2 instance from impacting the performance of traffic between your EC2 instance and an attached EBS volume?
- () Implement network-optimized instances
- **() Implement EBS-optimized instances** [CORRECT]
- () Put the EBS volume in one VPC and the instance in another
- () Place the EBS volume in one region and the instance in another
- () Implement EBS-optimized instances is the correct answer. Using EBS-optimized instances will prevent regular instance network traffic from impacting communications between the instance and the EBS volume. It is never a good idea, for performance, to move storage farther away from the processing instance.
- () DynamoDB has many use cases. Which of the following are legitimate use cases for DynamoDB? (Choose three.)
- () Storing archive data that you do not need to access often
- () Storing data that requires relational joins and highly complex updates
- () Correct selection
- () Storing JSON data
- () Storing the metadata of BLOB data stored in S3
- () Storing web session data
- () Correct Answers:
- () Storing JSON data, Storing the metadata of BLOB data stored in S3, and Storing web session data are correct. Use cases include storing JSON data, BLOB data, and web session data. 
- () Incorrect Answers:
- () Storing data that requires relational joins and highly complex updates is incorrect because you cannot run relational joins on DynamoDB.
- () Storing archive data that you do not need to access often is incorrect because archived data would be better placed on Glacier.

**Answer:**
Correct Answer: **Implement EBS-optimized instances**

**Explanation:**
Implement EBS-optimized instances is the correct answer. Using EBS-optimized instances will prevent regular instance network traffic from impacting communications between the instance and the EBS volume. It is never a good idea, for performance, to move storage farther away from the processing instance.

---

## Question 136

**Q:** You are reviewing Change Control requests and note a change designed to reduce wasted CPU cycles by increasing the value of the VisibilityTimeout attribute. What does this mean?

**Options:**
- (A) When the consumer instance polls for new work, the consumer instance will wait a certain amount of time until it has a full workload before closing the connection.
- (B) When the consumer instance polls for new work, the SQS service will allow it to wait a certain amount of time for a message to be available before closing the connection.
- (C) When a new message is added to the SQS queue, it will be hidden from consumer instances for a fixed period of time.
- (D) While processing a message, a consumer instance can amend the message visibility counter by a fixed amount.
- (E) While processing a message, a consumer instance can reset the message visibility by restarting the preset timeout counter.
- (F) When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time.
- (G) When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time is correct. When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time. You have the ability to control this timeout period. 
- (H) What can be implemented to prevent traffic from the network to your EC2 instance from impacting the performance of traffic between your EC2 instance and an attached EBS volume?
- (I) Implement network-optimized instances
- **(J) Implement EBS-optimized instances** [CORRECT]
- () Put the EBS volume in one VPC and the instance in another
- () Place the EBS volume in one region and the instance in another
- () Implement EBS-optimized instances is the correct answer. Using EBS-optimized instances will prevent regular instance network traffic from impacting communications between the instance and the EBS volume. It is never a good idea, for performance, to move storage farther away from the processing instance.
- () DynamoDB has many use cases. Which of the following are legitimate use cases for DynamoDB? (Choose three.)
- () Storing archive data that you do not need to access often
- () Storing data that requires relational joins and highly complex updates
- () Correct selection
- () Storing JSON data
- () Storing the metadata of BLOB data stored in S3
- () Storing web session data
- () Correct Answers:
- () Storing JSON data, Storing the metadata of BLOB data stored in S3, and Storing web session data are correct. Use cases include storing JSON data, BLOB data, and web session data. 
- () Incorrect Answers:
- () Storing data that requires relational joins and highly complex updates is incorrect because you cannot run relational joins on DynamoDB.
- () Storing archive data that you do not need to access often is incorrect because archived data would be better placed on Glacier.
- () Which of the following strategies does AWS use to deliver the promised levels of DynamoDB performance? (Choose two.)
- () Data is stored on solid state disks (SSDs).
- () AWS deploys caching instances in front of the DynamoDB cluster.
- () DynamoDB instances can be configured with EBS-optimized connections.
- () The database is partitioned across a number of instances.
- () Data is stored on solid state disks (SSDs) and The database is partitioned across a number of instances are correct. SSDs provide high performance, and the database is partitioned; these two aspects combined provide the promised level of performance for DynamoDB. 

**Answer:**
Correct Answer: **Implement EBS-optimized instances**

**Explanation:**
Implement EBS-optimized instances is the correct answer. Using EBS-optimized instances will prevent regular instance network traffic from impacting communications between the instance and the EBS volume. It is never a good idea, for performance, to move storage farther away from the processing instance.

---

## Question 137

**Q:** What can be implemented to prevent traffic from the network to your EC2 instance from impacting the performance of traffic between your EC2 instance and an attached EBS volume?

**Options:**
- (A) Implement network-optimized instances
- **(B) Implement EBS-optimized instances** [CORRECT]
- (C) Put the EBS volume in one VPC and the instance in another
- (D) Place the EBS volume in one region and the instance in another
- (E) Implement EBS-optimized instances is the correct answer. Using EBS-optimized instances will prevent regular instance network traffic from impacting communications between the instance and the EBS volume. It is never a good idea, for performance, to move storage farther away from the processing instance.
- (F) DynamoDB has many use cases. Which of the following are legitimate use cases for DynamoDB? (Choose three.)
- (G) Storing archive data that you do not need to access often
- (H) Storing data that requires relational joins and highly complex updates
- (I) Correct selection
- (J) Storing JSON data
- () Storing the metadata of BLOB data stored in S3
- () Storing web session data
- () Correct Answers:
- () Storing JSON data, Storing the metadata of BLOB data stored in S3, and Storing web session data are correct. Use cases include storing JSON data, BLOB data, and web session data. 
- () Incorrect Answers:
- () Storing data that requires relational joins and highly complex updates is incorrect because you cannot run relational joins on DynamoDB.
- () Storing archive data that you do not need to access often is incorrect because archived data would be better placed on Glacier.
- () Which of the following strategies does AWS use to deliver the promised levels of DynamoDB performance? (Choose two.)
- () Data is stored on solid state disks (SSDs).
- () AWS deploys caching instances in front of the DynamoDB cluster.
- () DynamoDB instances can be configured with EBS-optimized connections.
- () The database is partitioned across a number of instances.
- () Data is stored on solid state disks (SSDs) and The database is partitioned across a number of instances are correct. SSDs provide high performance, and the database is partitioned; these two aspects combined provide the promised level of performance for DynamoDB. 
- () Incorrect Answers
- () DynamoDB instances can be configured with EBS-optimized connections is incorrect because DynamoDB can’t be configured with EBS-optimized instances.
- () AWS deploys caching instances in front of the DynamoDB cluster is incorrect because, by default, caching is not enabled.
- () Amazon Web Services (AWS) offers four different levels of support. Which of the following are valid support levels? (Choose three.)
- () Business
- () Developer
- () Free tier
- () Enterprise
- () Corporate tier

**Answer:**
Correct Answer: **Implement EBS-optimized instances**

**Explanation:**
Implement EBS-optimized instances is the correct answer. Using EBS-optimized instances will prevent regular instance network traffic from impacting communications between the instance and the EBS volume. It is never a good idea, for performance, to move storage farther away from the processing instance.

---

## Question 138

**Q:** DynamoDB has many use cases. Which of the following are legitimate use cases for DynamoDB? (Choose three.)

**Options:**
- (A) Storing archive data that you do not need to access often
- (B) Storing data that requires relational joins and highly complex updates
- (C) Correct selection
- (D) Storing JSON data
- (E) Storing the metadata of BLOB data stored in S3
- (F) Storing web session data
- (G) Correct Answers:
- (H) Storing JSON data, Storing the metadata of BLOB data stored in S3, and Storing web session data are correct. Use cases include storing JSON data, BLOB data, and web session data. 
- (I) Incorrect Answers:
- (J) Storing data that requires relational joins and highly complex updates is incorrect because you cannot run relational joins on DynamoDB.
- () Storing archive data that you do not need to access often is incorrect because archived data would be better placed on Glacier.
- () Which of the following strategies does AWS use to deliver the promised levels of DynamoDB performance? (Choose two.)
- () Data is stored on solid state disks (SSDs).
- () AWS deploys caching instances in front of the DynamoDB cluster.
- () DynamoDB instances can be configured with EBS-optimized connections.
- () The database is partitioned across a number of instances.
- () Data is stored on solid state disks (SSDs) and The database is partitioned across a number of instances are correct. SSDs provide high performance, and the database is partitioned; these two aspects combined provide the promised level of performance for DynamoDB. 
- () Incorrect Answers
- () DynamoDB instances can be configured with EBS-optimized connections is incorrect because DynamoDB can’t be configured with EBS-optimized instances.
- () AWS deploys caching instances in front of the DynamoDB cluster is incorrect because, by default, caching is not enabled.
- () Amazon Web Services (AWS) offers four different levels of support. Which of the following are valid support levels? (Choose three.)
- () Business
- () Developer
- () Free tier
- () Enterprise
- () Corporate tier
- () Business, Developer, and Enterprise are correct. Developer, and Enterprise are all support level categories in AWS.
- () Free tier is incorrect because there is no Free tier support level.
- () Corporate tier is incorrect because there is no Corporate tier support level.
- () What is the primary difference between durability and availability as it related to AWS storage?
- () Availability and durability are synonymous
- **() Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not** [CORRECT]
- () Durability is related to accessing the data at a point in time and accessibility is related to the existence of the data whether durable or not
- () Availability ensures data can be recovered and durability ensures data can be accessed

**Answer:**
Correct Answer: **Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not**

**Explanation:**
Business, Developer, and Enterprise are correct. Developer, and Enterprise are all support level categories in AWS.

---

## Question 139

**Q:** Which of the following strategies does AWS use to deliver the promised levels of DynamoDB performance? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Data is stored on solid state disks (SSDs).
- (C) AWS deploys caching instances in front of the DynamoDB cluster.
- (D) DynamoDB instances can be configured with EBS-optimized connections.
- (E) The database is partitioned across a number of instances.
- (F) Correct Answers:
- (G) Data is stored on solid state disks (SSDs) and The database is partitioned across a number of instances are correct. SSDs provide high performance, and the database is partitioned; these two aspects combined provide the promised level of performance for DynamoDB. 
- (H) Incorrect Answers
- (I) DynamoDB instances can be configured with EBS-optimized connections is incorrect because DynamoDB can’t be configured with EBS-optimized instances.
- (J) AWS deploys caching instances in front of the DynamoDB cluster is incorrect because, by default, caching is not enabled.
- () Amazon Web Services (AWS) offers four different levels of support. Which of the following are valid support levels? (Choose three.)
- () Business
- () Developer
- () Free tier
- () Enterprise
- () Corporate tier
- () Business, Developer, and Enterprise are correct. Developer, and Enterprise are all support level categories in AWS.
- () Incorrect Answers:
- () Free tier is incorrect because there is no Free tier support level.
- () Corporate tier is incorrect because there is no Corporate tier support level.
- () What is the primary difference between durability and availability as it related to AWS storage?
- () Availability and durability are synonymous
- () Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not
- () Durability is related to accessing the data at a point in time and accessibility is related to the existence of the data whether durable or not
- () Availability ensures data can be recovered and durability ensures data can be accessed
- () What AWS service can be used to automate server scaling and configuration based on Chef or Puppet?
- **() OpsWorks** [CORRECT]
- () Elastic MapReduce
- () CloudFormation
- () CloudFront
- () OpsWorks is the correct answer. AWS OpsWorks supports Chef, Puppet, and stacks for automatic scaling and configuration of server environments. CloudFront is a CDN and Elastic MapReduce is used for data analytics. CloudFormation is not based on Chef or Puppet, but can be used to initially launch an entire required solution.

**Answer:**
Correct Answer: **OpsWorks**

**Explanation:**
OpsWorks is the correct answer. AWS OpsWorks supports Chef, Puppet, and stacks for automatic scaling and configuration of server environments. CloudFront is a CDN and Elastic MapReduce is used for data analytics. CloudFormation is not based on Chef or Puppet, but can be used to initially launch an entire required solution.

---

## Question 140

**Q:** Amazon Web Services (AWS) offers four different levels of support. Which of the following are valid support levels? (Choose three.)

**Options:**
- (A) Correct selection
- (B) Business
- (C) Developer
- (D) Free tier
- (E) Enterprise
- (F) Corporate tier
- (G) Business, Developer, and Enterprise are correct. Developer, and Enterprise are all support level categories in AWS.
- (H) Incorrect Answers:
- (I) Free tier is incorrect because there is no Free tier support level.
- (J) Corporate tier is incorrect because there is no Corporate tier support level.
- () What is the primary difference between durability and availability as it related to AWS storage?
- () Availability and durability are synonymous
- () Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not
- () Durability is related to accessing the data at a point in time and accessibility is related to the existence of the data whether durable or not
- () Availability ensures data can be recovered and durability ensures data can be accessed
- () What AWS service can be used to automate server scaling and configuration based on Chef or Puppet?
- () OpsWorks
- () Elastic MapReduce
- () CloudFormation
- () CloudFront
- () OpsWorks is the correct answer. AWS OpsWorks supports Chef, Puppet, and stacks for automatic scaling and configuration of server environments. CloudFront is a CDN and Elastic MapReduce is used for data analytics. CloudFormation is not based on Chef or Puppet, but can be used to initially launch an entire required solution.
- () What cannot be accomplished with an EFS storage solution?
- () Connecting it to a Linux instance
- () Encryption
- **() Connecting it to a Windows instance** [CORRECT]
- () Storing documents as well as database files
- () Connecting it to a Windows instance is the correct answer. EFS supports Linux instances, but it does not support Windows instances. It can be used to store any file types and it also supports encryption.

**Answer:**
Correct Answer: **Connecting it to a Windows instance**

**Explanation:**
Connecting it to a Windows instance is the correct answer. EFS supports Linux instances, but it does not support Windows instances. It can be used to store any file types and it also supports encryption.

---

## Question 141

**Q:** What is the primary difference between durability and availability as it related to AWS storage?

**Options:**
- (A) Availability and durability are synonymous
- (B) Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not
- (C) Durability is related to accessing the data at a point in time and accessibility is related to the existence of the data whether durable or not
- (D) Availability ensures data can be recovered and durability ensures data can be accessed
- (E) What AWS service can be used to automate server scaling and configuration based on Chef or Puppet?
- (F) OpsWorks
- (G) Elastic MapReduce
- (H) CloudFormation
- (I) CloudFront
- (J) OpsWorks is the correct answer. AWS OpsWorks supports Chef, Puppet, and stacks for automatic scaling and configuration of server environments. CloudFront is a CDN and Elastic MapReduce is used for data analytics. CloudFormation is not based on Chef or Puppet, but can be used to initially launch an entire required solution.
- () What cannot be accomplished with an EFS storage solution?
- () Connecting it to a Linux instance
- () Encryption
- **() Connecting it to a Windows instance** [CORRECT]
- () Storing documents as well as database files
- () Connecting it to a Windows instance is the correct answer. EFS supports Linux instances, but it does not support Windows instances. It can be used to store any file types and it also supports encryption.
- () You are running and hosting a web application in AWS. The web server is hosted in an EC2 server in the public subnet, and it is using the Oracle database in RDS in a private subnet. All the users must use SSL to connect to the web server, and only the web server should be able to connect to the database server. Which of the following actions satisfy this condition? (Choose two.)
- () Correct selection
- () Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere).
- () Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound.
- () Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic.
- () Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group.
- () Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group.
- () Correct Answers:
- () Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere) and Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group are correct.
- () Creating a security group for the database server is correct because it states the actual port of the database server, which needs to be open for the web server. 
- () Incorrect Answers:
- () Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group is incorrect because it specifies from which port the traffic would come but not the port of the database that needs to be open.
- () Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.
- () Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.

**Answer:**
Correct Answer: **Connecting it to a Windows instance**

**Explanation:**
Connecting it to a Windows instance is the correct answer. EFS supports Linux instances, but it does not support Windows instances. It can be used to store any file types and it also supports encryption.

---

## Question 142

**Q:** What AWS service can be used to automate server scaling and configuration based on Chef or Puppet?

**Options:**
- (A) OpsWorks
- (B) Elastic MapReduce
- (C) CloudFormation
- (D) CloudFront
- (E) OpsWorks is the correct answer. AWS OpsWorks supports Chef, Puppet, and stacks for automatic scaling and configuration of server environments. CloudFront is a CDN and Elastic MapReduce is used for data analytics. CloudFormation is not based on Chef or Puppet, but can be used to initially launch an entire required solution.
- (F) What cannot be accomplished with an EFS storage solution?
- (G) Connecting it to a Linux instance
- (H) Encryption
- (I) Connecting it to a Windows instance
- (J) Storing documents as well as database files
- () Connecting it to a Windows instance is the correct answer. EFS supports Linux instances, but it does not support Windows instances. It can be used to store any file types and it also supports encryption.
- () You are running and hosting a web application in AWS. The web server is hosted in an EC2 server in the public subnet, and it is using the Oracle database in RDS in a private subnet. All the users must use SSL to connect to the web server, and only the web server should be able to connect to the database server. Which of the following actions satisfy this condition? (Choose two.)
- () Correct selection
- () Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere).
- () Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound.
- () Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic.
- () Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group.
- () Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group.
- () Correct Answers:
- () Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere) and Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group are correct.
- () Creating a security group for the database server is correct because it states the actual port of the database server, which needs to be open for the web server. 
- () Incorrect Answers:
- () Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group is incorrect because it specifies from which port the traffic would come but not the port of the database that needs to be open.
- () Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.
- () Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.
- () What is the maximum S3 PUTs per second rate supported in AWS?
- **() 3500** [CORRECT]
- () 100
- () 2500
- () 1000
- () 3500 is the correct answer. The PUTs per second rate was raised from 100 to 3500 in 2018 and can be very important for those preparing for the AWS exams.

**Answer:**
Correct Answer: **3500**

**Explanation:**
3500 is the correct answer. The PUTs per second rate was raised from 100 to 3500 in 2018 and can be very important for those preparing for the AWS exams.

---

## Question 143

**Q:** What cannot be accomplished with an EFS storage solution?

**Options:**
- (A) Connecting it to a Linux instance
- (B) Encryption
- (C) Connecting it to a Windows instance
- (D) Storing documents as well as database files
- (E) Connecting it to a Windows instance is the correct answer. EFS supports Linux instances, but it does not support Windows instances. It can be used to store any file types and it also supports encryption.
- (F) You are running and hosting a web application in AWS. The web server is hosted in an EC2 server in the public subnet, and it is using the Oracle database in RDS in a private subnet. All the users must use SSL to connect to the web server, and only the web server should be able to connect to the database server. Which of the following actions satisfy this condition? (Choose two.)
- (G) Correct selection
- (H) Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere).
- (I) Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound.
- (J) Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic.
- () Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group.
- () Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group.
- () Correct Answers:
- () Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere) and Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group are correct.
- () Creating a security group for the database server is correct because it states the actual port of the database server, which needs to be open for the web server. 
- () Incorrect Answers:
- () Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group is incorrect because it specifies from which port the traffic would come but not the port of the database that needs to be open.
- () Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.
- () Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.
- () What is the maximum S3 PUTs per second rate supported in AWS?
- () 3500
- () 100
- () 2500
- () 1000
- () 3500 is the correct answer. The PUTs per second rate was raised from 100 to 3500 in 2018 and can be very important for those preparing for the AWS exams.
- () You are designing a password policy for IAM users. Which one of the following cannot be configured for password policies in the AWS Console?
- **() Prevent passwords including the user’s last name** [CORRECT]
- () Enable password expiration
- () Require at least one number
- () Minimum password length
- () Prevent passwords including the user’s last name is the correct answer. You cannot prevent passwords including the user’s last name in the password policies for IAM. However, you can specify minimum password length, uppercase letters, lowercase letters, numbers, nonalphanumeric characters, voluntary user password changes, password expiration, prevent password reuse, and password expiration requires administrator reset.

**Answer:**
Correct Answer: **Prevent passwords including the user’s last name**

**Explanation:**
Prevent passwords including the user’s last name is the correct answer. You cannot prevent passwords including the user’s last name in the password policies for IAM. However, you can specify minimum password length, uppercase letters, lowercase letters, numbers, nonalphanumeric characters, voluntary user password changes, password expiration, prevent password reuse, and password expiration requires administrator reset.

---

## Question 144

**Q:** You are running and hosting a web application in AWS. The web server is hosted in an EC2 server in the public subnet, and it is using the Oracle database in RDS in a private subnet. All the users must use SSL to connect to the web server, and only the web server should be able to connect to the database server. Which of the following actions satisfy this condition? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere).
- (C) Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound.
- (D) Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic.
- (E) Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group.
- (F) Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group.
- (G) Correct Answers:
- (H) Create a security group for the web server. The security group should allow inbound HTTPS traffic on port 443 from 0.0.0.0/0 (anywhere) and Create a security group for the database server. The security group should allow traffic on TCP port 1521 from the web server security group are correct.
- (I) Creating a security group for the database server is correct because it states the actual port of the database server, which needs to be open for the web server. 
- (J) Incorrect Answers:
- () Create a security group for the database server. The security group should allow inbound HTTPS traffic from port 443 from the web server security group is incorrect because it specifies from which port the traffic would come but not the port of the database that needs to be open.
- () Create an ACL for web server’s subnet that allows HTTPS on port 443 from 0.0.0.0/0 inbound and HTTPS on port 443 to 0.0.0.0/0 outbound is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.
- () Create an ACL for database server’s subnet that allows inbound traffic on TCP port 1521 from the web server and denies all outgoing traffic is incorrect because it suggests using an ACL, which is used at the subnet level and not at the instance level.
- () What is the maximum S3 PUTs per second rate supported in AWS?
- () 3500
- () 100
- () 2500
- () 1000
- () 3500 is the correct answer. The PUTs per second rate was raised from 100 to 3500 in 2018 and can be very important for those preparing for the AWS exams.
- () You are designing a password policy for IAM users. Which one of the following cannot be configured for password policies in the AWS Console?
- () Prevent passwords including the user’s last name
- () Enable password expiration
- () Require at least one number
- () Minimum password length
- () Prevent passwords including the user’s last name is the correct answer. You cannot prevent passwords including the user’s last name in the password policies for IAM. However, you can specify minimum password length, uppercase letters, lowercase letters, numbers, nonalphanumeric characters, voluntary user password changes, password expiration, prevent password reuse, and password expiration requires administrator reset.
- () You are considering the use of encryption for an EBS volume. When should the encryption be applied?
- () When the EBS volume is detached from an instance
- () During OS installation within the instance that will use the EBS volume
- () When the EBS volume is attached to an instance
- **() At the time the EBS volume is created** [CORRECT]
- () At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

**Answer:**
Correct Answer: **At the time the EBS volume is created**

**Explanation:**
At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

---

## Question 145

**Q:** What is the maximum S3 PUTs per second rate supported in AWS?

**Options:**
- (A) 3500
- (B) 100
- (C) 2500
- (D) 1000
- (E) 3500 is the correct answer. The PUTs per second rate was raised from 100 to 3500 in 2018 and can be very important for those preparing for the AWS exams.
- (F) You are designing a password policy for IAM users. Which one of the following cannot be configured for password policies in the AWS Console?
- (G) Prevent passwords including the user’s last name
- (H) Enable password expiration
- (I) Require at least one number
- (J) Minimum password length
- () Prevent passwords including the user’s last name is the correct answer. You cannot prevent passwords including the user’s last name in the password policies for IAM. However, you can specify minimum password length, uppercase letters, lowercase letters, numbers, nonalphanumeric characters, voluntary user password changes, password expiration, prevent password reuse, and password expiration requires administrator reset.
- () You are considering the use of encryption for an EBS volume. When should the encryption be applied?
- () When the EBS volume is detached from an instance
- () During OS installation within the instance that will use the EBS volume
- () When the EBS volume is attached to an instance
- **() At the time the EBS volume is created** [CORRECT]
- () At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

**Answer:**
Correct Answer: **At the time the EBS volume is created**

**Explanation:**
At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

---

## Question 146

**Q:** You are designing a password policy for IAM users. Which one of the following cannot be configured for password policies in the AWS Console?

**Options:**
- (A) Prevent passwords including the user’s last name
- (B) Enable password expiration
- (C) Require at least one number
- (D) Minimum password length
- (E) Prevent passwords including the user’s last name is the correct answer. You cannot prevent passwords including the user’s last name in the password policies for IAM. However, you can specify minimum password length, uppercase letters, lowercase letters, numbers, nonalphanumeric characters, voluntary user password changes, password expiration, prevent password reuse, and password expiration requires administrator reset.
- (F) You are considering the use of encryption for an EBS volume. When should the encryption be applied?
- (G) When the EBS volume is detached from an instance
- (H) During OS installation within the instance that will use the EBS volume
- (I) When the EBS volume is attached to an instance
- **(J) At the time the EBS volume is created** [CORRECT]
- () At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

**Answer:**
Correct Answer: **At the time the EBS volume is created**

**Explanation:**
At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

---

## Question 147

**Q:** You are considering the use of encryption for an EBS volume. When should the encryption be applied?

**Options:**
- (A) When the EBS volume is detached from an instance
- (B) During OS installation within the instance that will use the EBS volume
- (C) When the EBS volume is attached to an instance
- **(D) At the time the EBS volume is created** [CORRECT]
- (E) At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

**Answer:**
Correct Answer: **At the time the EBS volume is created**

**Explanation:**
At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

---

## Question 148

**Q:** What kind of storage is defined as data storage that persists only during the lifetime of an associated instance and that is lost when a drive fails, an instance stops, or an instance is terminated?

**Options:**
- (A) Instance store
- (B) EFS
- (C) EBS volume
- (D) Instance store is the correct answer. The instance store is a temporary block storage solution for an instance. It holds temporary information such as buffers, caches, and scratch data. Instance stores are exposed as block devices known as ephemeral0 through ephemeral23 as needed, for a maximum of 24 instance stores per instance. EBS, EFS and S3 all provide permanent storage.
- (E) You successfully configure VPC peering between VPC-A and VPC-B. You then establish an IGW and a Direct-Connect connection in VPC-B. Can instances in VPC-A connect to your corporate office via the Direct-Connect service as well as connect to the Internet via the IGW?
- (F) Instances in VPC-A will be able to access the corporate office but not the Internet.
- (G) Yes, VPC peering is designed to route traffic between the VPCs.
- (H) Instances in VPC-A will be able to access the Internet, but not the corporate office.
- (I) No, VPC peering does not support edge-to-edge routing.
- (J) No, VPC peering does not support edge-to-edge routing is correct. The answer is no because VPC peering does not support edge-to-edge routing. Say, for example, that VPC-A is peered to VPC-B, and VPC-B is peered to VPC-C. In this case, VPC-A and VPC-C won’t be able to talk unless there is a peering between them. 
- () You are responsible for implementing Amazon Kinesis Data Analytics. What language is used to process the data streams as they flow through the system?
- **() SQL** [CORRECT]
- () PHP
- () Ruby
- () Python
- () SQL is the incorrect answer. Kinesis Data Analytics uses SQL to read values from the data streams and perform analysis so that no new language is required. An incoming data stream is processed with SQL queries and the results are loaded into a desired destination for further processing.

**Answer:**
Correct Answer: **SQL**

**Explanation:**
SQL is the incorrect answer. Kinesis Data Analytics uses SQL to read values from the data streams and perform analysis so that no new language is required. An incoming data stream is processed with SQL queries and the results are loaded into a desired destination for further processing.

---

## Question 149

**Q:** You successfully configure VPC peering between VPC-A and VPC-B. You then establish an IGW and a Direct-Connect connection in VPC-B. Can instances in VPC-A connect to your corporate office via the Direct-Connect service as well as connect to the Internet via the IGW?

**Options:**
- (A) Instances in VPC-A will be able to access the corporate office but not the Internet.
- (B) Yes, VPC peering is designed to route traffic between the VPCs.
- (C) Instances in VPC-A will be able to access the Internet, but not the corporate office.
- (D) No, VPC peering does not support edge-to-edge routing.
- (E) No, VPC peering does not support edge-to-edge routing is correct. The answer is no because VPC peering does not support edge-to-edge routing. Say, for example, that VPC-A is peered to VPC-B, and VPC-B is peered to VPC-C. In this case, VPC-A and VPC-C won’t be able to talk unless there is a peering between them. 
- (F) You are responsible for implementing Amazon Kinesis Data Analytics. What language is used to process the data streams as they flow through the system?
- **(G) SQL** [CORRECT]
- (H) PHP
- (I) Ruby
- (J) Python
- () SQL is the incorrect answer. Kinesis Data Analytics uses SQL to read values from the data streams and perform analysis so that no new language is required. An incoming data stream is processed with SQL queries and the results are loaded into a desired destination for further processing.

**Answer:**
Correct Answer: **SQL**

**Explanation:**
SQL is the incorrect answer. Kinesis Data Analytics uses SQL to read values from the data streams and perform analysis so that no new language is required. An incoming data stream is processed with SQL queries and the results are loaded into a desired destination for further processing.

---

## Question 150

**Q:** You are responsible for implementing Amazon Kinesis Data Analytics. What language is used to process the data streams as they flow through the system?

**Options:**
- **(A) SQL** [CORRECT]
- (B) PHP
- (C) Ruby
- (D) Python
- (E) SQL is the incorrect answer. Kinesis Data Analytics uses SQL to read values from the data streams and perform analysis so that no new language is required. An incoming data stream is processed with SQL queries and the results are loaded into a desired destination for further processing.

**Answer:**
Correct Answer: **SQL**

**Explanation:**
SQL is the incorrect answer. Kinesis Data Analytics uses SQL to read values from the data streams and perform analysis so that no new language is required. An incoming data stream is processed with SQL queries and the results are loaded into a desired destination for further processing.

---

## Question 151

**Q:** At the monthly product meeting, one of the product owners proposes an idea to address an immediate shortcoming of the product system: storing a copy of the customer price schedule in the customer record in the database. You know that you can store large text or binary objects in DynamoDB. You give a tentative OK to do a minimum viable product (MVP) test, but you stipulate that it must comply with the size limitation on the attribute name and value. Which is the correct limitation?

**Options:**
- (A) The value and name combined must not exceed 400KB.
- (B) The value and name combined must not exceed 1024KB.
- (C) The name must not exceed 64KB, and the value must not exceed 500KB.
- (D) The name must not exceed 64KB, and the value must not exceed 1024KB.
- (E) The value and name combined must not exceed 500KB.
- (F) The name must not exceed 128KB, and the value must not exceed 400KB.
- (G) The value and name combined must not exceed 400KB is correct. The combined size for the name and value can’t exceed 400KB.
- (H) What is true about edge locations when using CloudFront?
- (I) They are write-only
- (J) They are read-only
- () They are read/write
- () They are not accessible from machines outside of AWS VPCs
- () They are read/write is the correct answer. CloudFront edge locations are read/write. They are accessible from machines outside of AWS VPCs, which is the primary purpose of their existence - to provide localized copies of files for faster regional access.
- () What AWS tool can be used to estimate the cost of storage for an AWS solution?
- () AWS Budgets
- () AWS Cost Explorer
- () AWS Cost and Usage Report
- **() AWS Pricing Calculator** [CORRECT]
- () The AWS Pricing Calculator can be used to estimate costs for the major AWS services including S3 and EC2.
- () You are a solutions architect working for an oil and gas company that’s moving its production environment to AWS and needs a custom VPC in which to put it. You have been asked to create a public subnet. You create the VPC with a subnet bearing the CIDR address range 10.0.1.0/24. Which of the following steps should you take to make this subnet public? (Choose two.)
- () Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW).
- () Attach a Customer Gateway (CGW).
- () Correct selection
- () Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW).
- () In the AWS Console, right-click the subnet and then select the Make Public option.
- () Attach an Internet Gateway (IGW) to the VPC.
- () Correct Answers:
- () Attach an Internet Gateway (IGW) to the VPC and Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW) are correct. When an Internet Gateway (IGW) is attached to a VPC, it can be used to access the Internet. In this case, you need to attach an IGW to the VPC, which is going to allow the Internet access, and then create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW). 
- () Incorrect Answers:
- () In the AWS Console, right-click the subnet and then select the Make Public option is incorrect because that’s not how you make a subnet public.
- () Attach a Customer Gateway (CGW) is incorrect because you can’t attach a Customer Gateway to a VPC.
- () Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW) is incorrect because it refers to a Customer Gateway.

**Answer:**
Correct Answer: **AWS Pricing Calculator**

**Explanation:**
The AWS Pricing Calculator can be used to estimate costs for the major AWS services including S3 and EC2.

---

## Question 152

**Q:** What is true about edge locations when using CloudFront?

**Options:**
- (A) They are write-only
- (B) They are read-only
- (C) They are read/write
- (D) They are not accessible from machines outside of AWS VPCs
- (E) They are read/write is the correct answer. CloudFront edge locations are read/write. They are accessible from machines outside of AWS VPCs, which is the primary purpose of their existence - to provide localized copies of files for faster regional access.
- (F) What AWS tool can be used to estimate the cost of storage for an AWS solution?
- (G) AWS Budgets
- (H) AWS Cost Explorer
- (I) AWS Cost and Usage Report
- (J) AWS Pricing Calculator
- () The AWS Pricing Calculator can be used to estimate costs for the major AWS services including S3 and EC2.
- () You are a solutions architect working for an oil and gas company that’s moving its production environment to AWS and needs a custom VPC in which to put it. You have been asked to create a public subnet. You create the VPC with a subnet bearing the CIDR address range 10.0.1.0/24. Which of the following steps should you take to make this subnet public? (Choose two.)
- () Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW).
- () Attach a Customer Gateway (CGW).
- () Correct selection
- () Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW).
- () In the AWS Console, right-click the subnet and then select the Make Public option.
- () Attach an Internet Gateway (IGW) to the VPC.
- () Correct Answers:
- () Attach an Internet Gateway (IGW) to the VPC and Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW) are correct. When an Internet Gateway (IGW) is attached to a VPC, it can be used to access the Internet. In this case, you need to attach an IGW to the VPC, which is going to allow the Internet access, and then create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW). 
- () Incorrect Answers:
- () In the AWS Console, right-click the subnet and then select the Make Public option is incorrect because that’s not how you make a subnet public.
- () Attach a Customer Gateway (CGW) is incorrect because you can’t attach a Customer Gateway to a VPC.
- () Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW) is incorrect because it refers to a Customer Gateway.
- () You must transfer 40 TB of data into AWS S3 buckets. You are concerned about the time it will take to transfer the files over the network and the impact it will have on user performance. What is the best option for transferring such a large amount of data without impacting network user performance?
- () HTTP transfer
- () Direct Connect
- **() Snowball** [CORRECT]
- () HTTPS transfer
- () Snowball is the correct answer. Using Snowball, you will connect the Snowball device to your local network and transfer all of the data to it. Then you will ship it to AWS and they will load it into your AWS account. This will result in no performance impact on your Internet connection.

**Answer:**
Correct Answer: **Snowball**

**Explanation:**
Snowball is the correct answer. Using Snowball, you will connect the Snowball device to your local network and transfer all of the data to it. Then you will ship it to AWS and they will load it into your AWS account. This will result in no performance impact on your Internet connection.

---

## Question 153

**Q:** What AWS tool can be used to estimate the cost of storage for an AWS solution?

**Options:**
- (A) AWS Budgets
- (B) AWS Cost Explorer
- (C) AWS Cost and Usage Report
- (D) AWS Pricing Calculator
- (E) The AWS Pricing Calculator can be used to estimate costs for the major AWS services including S3 and EC2.
- (F) You are a solutions architect working for an oil and gas company that’s moving its production environment to AWS and needs a custom VPC in which to put it. You have been asked to create a public subnet. You create the VPC with a subnet bearing the CIDR address range 10.0.1.0/24. Which of the following steps should you take to make this subnet public? (Choose two.)
- (G) Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW).
- (H) Attach a Customer Gateway (CGW).
- (I) Correct selection
- (J) Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW).
- () In the AWS Console, right-click the subnet and then select the Make Public option.
- () Attach an Internet Gateway (IGW) to the VPC.
- () Correct Answers:
- () Attach an Internet Gateway (IGW) to the VPC and Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW) are correct. When an Internet Gateway (IGW) is attached to a VPC, it can be used to access the Internet. In this case, you need to attach an IGW to the VPC, which is going to allow the Internet access, and then create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW). 
- () Incorrect Answers:
- () In the AWS Console, right-click the subnet and then select the Make Public option is incorrect because that’s not how you make a subnet public.
- () Attach a Customer Gateway (CGW) is incorrect because you can’t attach a Customer Gateway to a VPC.
- () Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW) is incorrect because it refers to a Customer Gateway.
- () You must transfer 40 TB of data into AWS S3 buckets. You are concerned about the time it will take to transfer the files over the network and the impact it will have on user performance. What is the best option for transferring such a large amount of data without impacting network user performance?
- () HTTP transfer
- () Direct Connect
- () Snowball
- () HTTPS transfer
- () Snowball is the correct answer. Using Snowball, you will connect the Snowball device to your local network and transfer all of the data to it. Then you will ship it to AWS and they will load it into your AWS account. This will result in no performance impact on your Internet connection.
- () What is a primary difference between EFS and EBS storage in AWS?
- () EFS is block storage and EBS is object storage
- () EBS storage can be shared across regions and EFS cannot
- **() EFS storage can be shared across regions and EBS cannot** [CORRECT]
- () EBS is block storage and EFS is object storage
- () EFS storage can be shared across regions and EBS cannot is the correct answer. Elastic File System (EFS) can be shared across regions and Elastic Block Store (EBS) cannot. Both are block storage.

**Answer:**
Correct Answer: **EFS storage can be shared across regions and EBS cannot**

**Explanation:**
EFS storage can be shared across regions and EBS cannot is the correct answer. Elastic File System (EFS) can be shared across regions and Elastic Block Store (EBS) cannot. Both are block storage.

---

## Question 154

**Q:** You are a solutions architect working for an oil and gas company that’s moving its production environment to AWS and needs a custom VPC in which to put it. You have been asked to create a public subnet. You create the VPC with a subnet bearing the CIDR address range 10.0.1.0/24. Which of the following steps should you take to make this subnet public? (Choose two.)

**Options:**
- (A) Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW).
- (B) Attach a Customer Gateway (CGW).
- (C) Correct selection
- (D) Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW).
- (E) In the AWS Console, right-click the subnet and then select the Make Public option.
- (F) Attach an Internet Gateway (IGW) to the VPC.
- (G) Correct Answers:
- (H) Attach an Internet Gateway (IGW) to the VPC and Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW) are correct. When an Internet Gateway (IGW) is attached to a VPC, it can be used to access the Internet. In this case, you need to attach an IGW to the VPC, which is going to allow the Internet access, and then create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW). 
- (I) Incorrect Answers:
- (J) In the AWS Console, right-click the subnet and then select the Make Public option is incorrect because that’s not how you make a subnet public.
- () Attach a Customer Gateway (CGW) is incorrect because you can’t attach a Customer Gateway to a VPC.
- () Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW) is incorrect because it refers to a Customer Gateway.
- () You must transfer 40 TB of data into AWS S3 buckets. You are concerned about the time it will take to transfer the files over the network and the impact it will have on user performance. What is the best option for transferring such a large amount of data without impacting network user performance?
- () HTTP transfer
- () Direct Connect
- () Snowball
- () HTTPS transfer
- () Snowball is the correct answer. Using Snowball, you will connect the Snowball device to your local network and transfer all of the data to it. Then you will ship it to AWS and they will load it into your AWS account. This will result in no performance impact on your Internet connection.
- () What is a primary difference between EFS and EBS storage in AWS?
- () EFS is block storage and EBS is object storage
- () EBS storage can be shared across regions and EFS cannot
- () EFS storage can be shared across regions and EBS cannot
- () EBS is block storage and EFS is object storage
- () EFS storage can be shared across regions and EBS cannot is the correct answer. Elastic File System (EFS) can be shared across regions and Elastic Block Store (EBS) cannot. Both are block storage.
- () What important action may help to reduce costs of AWS operations over a long period of time?
- () Use Elastic IP (EIP) addresses for all EC2 network interfaces
- () Use S3 Standard for all storage
- () Use multiple VPCs with redundant EC2 instances in separate VPCs for all EC2 instances by default
- **() Keep up to date with new AWS service releases** [CORRECT]
- () Keep up to date with new AWS service releases is the correct answer. While extra costs can be incurred due to all listed items, the selected database engine has the largest impact on cost. Licensed engines (requiring a non-AWS license) such as Oracle and SQL Server can have costs 2-5 times higher the open source or AWS-original database engines.

**Answer:**
Correct Answer: **Keep up to date with new AWS service releases**

**Explanation:**
Keep up to date with new AWS service releases is the correct answer. While extra costs can be incurred due to all listed items, the selected database engine has the largest impact on cost. Licensed engines (requiring a non-AWS license) such as Oracle and SQL Server can have costs 2-5 times higher the open source or AWS-original database engines.

---

## Question 155

**Q:** You must transfer 40 TB of data into AWS S3 buckets. You are concerned about the time it will take to transfer the files over the network and the impact it will have on user performance. What is the best option for transferring such a large amount of data without impacting network user performance?

**Options:**
- (A) HTTP transfer
- (B) Direct Connect
- (C) Snowball
- (D) HTTPS transfer
- (E) Snowball is the correct answer. Using Snowball, you will connect the Snowball device to your local network and transfer all of the data to it. Then you will ship it to AWS and they will load it into your AWS account. This will result in no performance impact on your Internet connection.
- (F) What is a primary difference between EFS and EBS storage in AWS?
- (G) EFS is block storage and EBS is object storage
- (H) EBS storage can be shared across regions and EFS cannot
- (I) EFS storage can be shared across regions and EBS cannot
- (J) EBS is block storage and EFS is object storage
- () EFS storage can be shared across regions and EBS cannot is the correct answer. Elastic File System (EFS) can be shared across regions and Elastic Block Store (EBS) cannot. Both are block storage.
- () What important action may help to reduce costs of AWS operations over a long period of time?
- () Use Elastic IP (EIP) addresses for all EC2 network interfaces
- () Use S3 Standard for all storage
- () Use multiple VPCs with redundant EC2 instances in separate VPCs for all EC2 instances by default
- () Keep up to date with new AWS service releases
- () Keep up to date with new AWS service releases is the correct answer. While extra costs can be incurred due to all listed items, the selected database engine has the largest impact on cost. Licensed engines (requiring a non-AWS license) such as Oracle and SQL Server can have costs 2-5 times higher the open source or AWS-original database engines.
- () You want to limit who can modify a NACL that is associated with a subnet. What can you use?
- () Security Group
- () Another NACL
- () Flow log
- () IAM
- () IAM is the correct answer. A NACL is an object that can be configured with permissions, so you can use IAM to decide who can and cannot manage the NACL. The other options in no way provide permission management for NACL objects.
- () What is the container used to store DNS records called in Route 53?
- **() Hosted zone** [CORRECT]
- () DNS resolver

**Answer:**
Correct Answer: **Hosted zone**

**Explanation:**
IAM is the correct answer. A NACL is an object that can be configured with permissions, so you can use IAM to decide who can and cannot manage the NACL. The other options in no way provide permission management for NACL objects.

---

## Question 156

**Q:** What is a primary difference between EFS and EBS storage in AWS?

**Options:**
- (A) EFS is block storage and EBS is object storage
- (B) EBS storage can be shared across regions and EFS cannot
- (C) EFS storage can be shared across regions and EBS cannot
- (D) EBS is block storage and EFS is object storage
- (E) EFS storage can be shared across regions and EBS cannot is the correct answer. Elastic File System (EFS) can be shared across regions and Elastic Block Store (EBS) cannot. Both are block storage.
- (F) What important action may help to reduce costs of AWS operations over a long period of time?
- (G) Use Elastic IP (EIP) addresses for all EC2 network interfaces
- (H) Use S3 Standard for all storage
- (I) Use multiple VPCs with redundant EC2 instances in separate VPCs for all EC2 instances by default
- (J) Keep up to date with new AWS service releases
- () Keep up to date with new AWS service releases is the correct answer. While extra costs can be incurred due to all listed items, the selected database engine has the largest impact on cost. Licensed engines (requiring a non-AWS license) such as Oracle and SQL Server can have costs 2-5 times higher the open source or AWS-original database engines.
- () You want to limit who can modify a NACL that is associated with a subnet. What can you use?
- () Security Group
- () Another NACL
- () Flow log
- () IAM
- () IAM is the correct answer. A NACL is an object that can be configured with permissions, so you can use IAM to decide who can and cannot manage the NACL. The other options in no way provide permission management for NACL objects.
- () What is the container used to store DNS records called in Route 53?
- **() Hosted zone** [CORRECT]
- () DNS resolver
- () DNS record
- () Authoritative name server
- () Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

**Answer:**
Correct Answer: **Hosted zone**

**Explanation:**
Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

---

## Question 157

**Q:** What important action may help to reduce costs of AWS operations over a long period of time?

**Options:**
- (A) Use Elastic IP (EIP) addresses for all EC2 network interfaces
- (B) Use S3 Standard for all storage
- (C) Use multiple VPCs with redundant EC2 instances in separate VPCs for all EC2 instances by default
- (D) Keep up to date with new AWS service releases
- (E) Keep up to date with new AWS service releases is the correct answer. While extra costs can be incurred due to all listed items, the selected database engine has the largest impact on cost. Licensed engines (requiring a non-AWS license) such as Oracle and SQL Server can have costs 2-5 times higher the open source or AWS-original database engines.
- (F) You want to limit who can modify a NACL that is associated with a subnet. What can you use?
- (G) Security Group
- (H) Another NACL
- (I) Flow log
- (J) IAM
- () IAM is the correct answer. A NACL is an object that can be configured with permissions, so you can use IAM to decide who can and cannot manage the NACL. The other options in no way provide permission management for NACL objects.
- () What is the container used to store DNS records called in Route 53?
- **() Hosted zone** [CORRECT]
- () DNS resolver
- () DNS record
- () Authoritative name server
- () Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

**Answer:**
Correct Answer: **Hosted zone**

**Explanation:**
Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

---

## Question 158

**Q:** You want to limit who can modify a NACL that is associated with a subnet. What can you use?

**Options:**
- (A) Security Group
- (B) Another NACL
- (C) Flow log
- (D) IAM
- (E) IAM is the correct answer. A NACL is an object that can be configured with permissions, so you can use IAM to decide who can and cannot manage the NACL. The other options in no way provide permission management for NACL objects.
- (F) What is the container used to store DNS records called in Route 53?
- **(G) Hosted zone** [CORRECT]
- (H) DNS resolver
- (I) DNS record
- (J) Authoritative name server
- () Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

**Answer:**
Correct Answer: **Hosted zone**

**Explanation:**
Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

---

## Question 159

**Q:** What is the container used to store DNS records called in Route 53?

**Options:**
- **(A) Hosted zone** [CORRECT]
- (B) DNS resolver
- (C) DNS record
- (D) Authoritative name server
- (E) Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

**Answer:**
Correct Answer: **Hosted zone**

**Explanation:**
Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

---

## Question 160

**Q:** If you want all user requests made to a CloudFront configuration to force HTTPS instead of HTTP transfers, what should you do?

**Options:**
- **(A) Configure the Protocol Policy to specify Redirect HTTP to HTTPS** [CORRECT]
- (B) This cannot be forced if the users did not request it
- (C) Configure each edge location web server to use only HTTPS
- (D) Configure the source web server to use only HTTPS
- (E) Configure the Protocol Policy to specify Redirect HTTP to HTTPS is the correct answer.
- (F) The proper way to configure this in CloudFront deployments is through the Protocol Policy. The Protocol Policy can be set to HTTP and HTTPS, Redirect HTTP to HTTPS, or HTTPS Only.

**Answer:**
Correct Answer: **Configure the Protocol Policy to specify Redirect HTTP to HTTPS**

**Explanation:**
Configure the Protocol Policy to specify Redirect HTTP to HTTPS is the correct answer.

---

## Question 161

**Q:** You are implementing a content delivery network (CDN) using Amazon CloudFront. What are the locations, distributed throughout the world, that contain the cached data called?

**Options:**
- (A) Edge locations
- (B) Distributed locations
- (C) Cloud locations
- (D) Front locations
- (E) Edge locations is the correct answer. The term used in CloudFront is edge locations. These edge locations are data centers located in major cities throughout the world and allow for data to be cached closer to the requesting users.
- (F) What should the last rule be in a NACL that allows three protocols and disallows everything else?
- (G) All traffic/Allow
- **(H) All traffic/Deny** [CORRECT]
- (I) TCP traffic/Allow
- (J) TCP traffic/Deny
- () All traffic/Deny is the correct answer. If the final rule is All traffic/Deny and preceding rules (lower numbered rules) allow specific traffic, the specific traffic will be allowed because it matches those rules before getting to the All traffic/Deny rule. However, because the last rule is All traffic/Deny, any traffic not specified in the rule will indeed be denied.

**Answer:**
Correct Answer: **All traffic/Deny**

**Explanation:**
All traffic/Deny is the correct answer. If the final rule is All traffic/Deny and preceding rules (lower numbered rules) allow specific traffic, the specific traffic will be allowed because it matches those rules before getting to the All traffic/Deny rule. However, because the last rule is All traffic/Deny, any traffic not specified in the rule will indeed be denied.

---

## Question 162

**Q:** What should the last rule be in a NACL that allows three protocols and disallows everything else?

**Options:**
- (A) All traffic/Allow
- **(B) All traffic/Deny** [CORRECT]
- (C) TCP traffic/Allow
- (D) TCP traffic/Deny
- (E) All traffic/Deny is the correct answer. If the final rule is All traffic/Deny and preceding rules (lower numbered rules) allow specific traffic, the specific traffic will be allowed because it matches those rules before getting to the All traffic/Deny rule. However, because the last rule is All traffic/Deny, any traffic not specified in the rule will indeed be denied.

**Answer:**
Correct Answer: **All traffic/Deny**

**Explanation:**
All traffic/Deny is the correct answer. If the final rule is All traffic/Deny and preceding rules (lower numbered rules) allow specific traffic, the specific traffic will be allowed because it matches those rules before getting to the All traffic/Deny rule. However, because the last rule is All traffic/Deny, any traffic not specified in the rule will indeed be denied.

---

## Question 163

**Q:** Your company likes the idea of storing files on AWS. However, low-latency service of the majority of files is important to customer service. Which Storage Gateway configuration would you use to achieve both these ends?

**Options:**
- (A) Gateway-VTL
- (B) Gateway-Cached
- (C) Gateway-Snapshot
- (D) Gateway-Stored
- (E) Gateway-Stored is correct. In this case, they key is low latency, and you have to choose the solution based on that. Since you want a low-latency solution, Gateway-Stored is the right way to go. 
- (F) Incorrect Answers:
- (G) Gateway-Cached is incorrect because Gateway-Cached won’t provide the lowest latency.
- (H) Gateway-VTL is incorrect because Gateway-VTL won’t provide the lowest latency.
- (I) Gateway-Snapshot is incorrect because Gateway-Snapshot won’t provide the lowest latency.
- (J) You are working with roles. How many roles can be assigned to an instance?
- **() 1** [CORRECT]
- () Unlimited
- () 1 is the correct answer. An instance can have only one role assigned at a time.

**Answer:**
Correct Answer: **1**

**Explanation:**
1 is the correct answer. An instance can have only one role assigned at a time.

---

## Question 164

**Q:** You are working with roles. How many roles can be assigned to an instance?

**Options:**
- **(A) 1** [CORRECT]
- (B) Unlimited
- (C) 1 is the correct answer. An instance can have only one role assigned at a time.

**Answer:**
Correct Answer: **1**

**Explanation:**
1 is the correct answer. An instance can have only one role assigned at a time.

---

## Question 165

**Q:** You are creating a data lake, and one of the criteria you are looking for is faster performance. You want the ability to transform the data directly during the ingestion process to save time and cost. Which AWS service should you choose for this?

**Options:**
- (A) Ingest the data in S3 and then use EMR to transform.
- (B) Use Kinesis Analytics for transforming the data.
- (C) Ingest the data in S3 and then load it in Redshift to transform.
- (D) Use Kinesis Firehose.
- (E) Use Kinesis Analytics for transforming the data is correct. Kinesis Analytics has the ability to transform the data during ingestion.
- (F) Incorrect Answers:
- (G) Ingest the data in S3 and then load it in Redshift to transform, Ingest the data in S3 and then use EMR to transform, and Use Kinesis Firehose are incorrect. Loading the data in S3 and then using EMR to transform it is going to take lot of time. You are looking for faster performance. Redshift is a data warehouse solution. Kinesis Firehose can ingest the data, but it does not have any ability to transform the data.
- (H) You must attach an EBS volume to an EC2 instance that offers the highest level of performance. What EBS type should be used?
- (I) Provisioned IOPS SSD
- (J) Striped SSD
- () Magnetic
- () General SSD
- () Provisioned IOPS SSD is the correct answer. A provisioned IOPS SSD will provide the optimum performance. A general SSD would be next. Magnetic storage provides the least performance, but it also provides the least cost. You do not directly control the physical implementation of disks, so you cannot select disk striping or mirroring at the physical level.
- () What is the maximum VisibilityTimeout value of an SQS message in a FIFO queue?
- () 1 hour
- () 14 days
- () 12 hours
- () 1 day
- () 12 hours is correct. The maximum VisibilityTimeout value you can have for an SQS message in a FIFO is 12 hours.
- () You have three Elastic Network Interfaces (ENIs). They are attached to three instances. You need an ENI for another instance and one of the instances currently using an ENI no longer needs it. What is the best action to take?
- () Move the ENI from the instance no longer needing it to the instance requiring it
- () Delete the ENI from the instance no longer requiring it and then create a new ENI for the instance requiring it
- () Create a new ENI and attach it to the instance requiring it
- () You cannot have more than two active ENIs.
- () Move the ENI from the instance no longer needing it to the instance requiring it is the correct answer. While an ENI can only be attached to one instance, you can move them from one instance to another. You can have more than two active ENIs.
- () You are planning VPCs and want to document their functionality. How many Availability Zones within a region does a single VPC span?
- **() All of them** [CORRECT]

**Answer:**
Correct Answer: **All of them**

**Explanation:**
Move the ENI from the instance no longer needing it to the instance requiring it is the correct answer. While an ENI can only be attached to one instance, you can move them from one instance to another. You can have more than two active ENIs.

---

## Question 166

**Q:** You must attach an EBS volume to an EC2 instance that offers the highest level of performance. What EBS type should be used?

**Options:**
- (A) Provisioned IOPS SSD
- (B) Striped SSD
- (C) Magnetic
- (D) General SSD
- (E) Provisioned IOPS SSD is the correct answer. A provisioned IOPS SSD will provide the optimum performance. A general SSD would be next. Magnetic storage provides the least performance, but it also provides the least cost. You do not directly control the physical implementation of disks, so you cannot select disk striping or mirroring at the physical level.
- (F) What is the maximum VisibilityTimeout value of an SQS message in a FIFO queue?
- (G) 1 hour
- (H) 14 days
- (I) 12 hours
- (J) 1 day
- () 12 hours is correct. The maximum VisibilityTimeout value you can have for an SQS message in a FIFO is 12 hours.
- () You have three Elastic Network Interfaces (ENIs). They are attached to three instances. You need an ENI for another instance and one of the instances currently using an ENI no longer needs it. What is the best action to take?
- () Move the ENI from the instance no longer needing it to the instance requiring it
- () Delete the ENI from the instance no longer requiring it and then create a new ENI for the instance requiring it
- () Create a new ENI and attach it to the instance requiring it
- () You cannot have more than two active ENIs.
- () Move the ENI from the instance no longer needing it to the instance requiring it is the correct answer. While an ENI can only be attached to one instance, you can move them from one instance to another. You can have more than two active ENIs.
- () You are planning VPCs and want to document their functionality. How many Availability Zones within a region does a single VPC span?
- **() All of them** [CORRECT]
- () All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

**Answer:**
Correct Answer: **All of them**

**Explanation:**
All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

---

## Question 167

**Q:** What is the maximum VisibilityTimeout value of an SQS message in a FIFO queue?

**Options:**
- (A) 1 hour
- (B) 14 days
- (C) 12 hours
- (D) 1 day
- (E) 12 hours is correct. The maximum VisibilityTimeout value you can have for an SQS message in a FIFO is 12 hours.
- (F) You have three Elastic Network Interfaces (ENIs). They are attached to three instances. You need an ENI for another instance and one of the instances currently using an ENI no longer needs it. What is the best action to take?
- (G) Move the ENI from the instance no longer needing it to the instance requiring it
- (H) Delete the ENI from the instance no longer requiring it and then create a new ENI for the instance requiring it
- (I) Create a new ENI and attach it to the instance requiring it
- (J) You cannot have more than two active ENIs.
- () Move the ENI from the instance no longer needing it to the instance requiring it is the correct answer. While an ENI can only be attached to one instance, you can move them from one instance to another. You can have more than two active ENIs.
- () You are planning VPCs and want to document their functionality. How many Availability Zones within a region does a single VPC span?
- **() All of them** [CORRECT]
- () All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

**Answer:**
Correct Answer: **All of them**

**Explanation:**
All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

---

## Question 168

**Q:** You have three Elastic Network Interfaces (ENIs). They are attached to three instances. You need an ENI for another instance and one of the instances currently using an ENI no longer needs it. What is the best action to take?

**Options:**
- (A) Move the ENI from the instance no longer needing it to the instance requiring it
- (B) Delete the ENI from the instance no longer requiring it and then create a new ENI for the instance requiring it
- (C) Create a new ENI and attach it to the instance requiring it
- (D) You cannot have more than two active ENIs.
- (E) Move the ENI from the instance no longer needing it to the instance requiring it is the correct answer. While an ENI can only be attached to one instance, you can move them from one instance to another. You can have more than two active ENIs.
- (F) You are planning VPCs and want to document their functionality. How many Availability Zones within a region does a single VPC span?
- **(G) All of them** [CORRECT]
- (H) All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

**Answer:**
Correct Answer: **All of them**

**Explanation:**
All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

---

## Question 169

**Q:** You are planning VPCs and want to document their functionality. How many Availability Zones within a region does a single VPC span?

**Options:**
- **(A) All of them** [CORRECT]
- (B) All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

**Answer:**
Correct Answer: **All of them**

**Explanation:**
All of these answers are correct. A VPC spans all Availability Zones within the region in which it is created.

---

## Question 170

**Q:** When storing data in EC2 instances, in addition to storage space requirements, what cost factor must be considered?

**Options:**
- (A) Data transfer costs (from your local network to AWS)
- (B) Data transfer costs (from AWS to your local network)
- (C) Data encryption costs
- (D) Data decryption costs
- (E) Data transfer costs (from AWS to your local network) is the correct answer. Given the scenario, reserved pricing will have a significant impact on costs. However, you must be able to accurately predict your needs for 1-3 years. Savings as high as 75% can be achieved when using reserved pricing.
- (F) You must implement an AWS solution that can expand and contract the number of server instances as needed. What AWS service provides this functionality?
- (G) Auto Scaling
- (H) ElastiCache
- (I) Lambda
- (J) Auto Growing
- () Auto Scaling is the correct answer. AWS Auto Scaling can expand or contract the number of servers in a solution automatically based on current demands. This allows you to use and pay for the services you require, based on the load, but not more. No such service as Auto Growing exists. ElastiCache provides in memory caching. Lambda is a code execution engine that allows you to execute code without building out the instances required to run the code.
- () You must enable alerts and other notifications to be sent to the appropriate individuals from the AWS cloud. What AWS service can provide this function?
- () Amazon Simple Notification Service (SNS)
- () Amazon Kinesis
- () Amazon Simple Queue Service (SQS)
- () Amazon Simple Workflow (SWF)
- () Amazon Simple Notification Services (SNS) is the correct answer. SNS is used to send notifications, which can be sent via HTTP/HTTPS, SMS, Lambda, SQS, or e-mail. SQS is used for queueing requests so that they can be processed as needed. SWF is used to perform operations based on the state of a system and it is being replaced with step functions.
- () What two methods are provided in AWS RDS for database backups?
- () Manual backups and automated snapshots
- () Automated backups and manual snapshots
- () Manual backups and manual snapshots
- **() Automated backups and automated snapshots** [CORRECT]
- () Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

**Answer:**
Correct Answer: **Automated backups and automated snapshots**

**Explanation:**
Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

---

## Question 171

**Q:** You must implement an AWS solution that can expand and contract the number of server instances as needed. What AWS service provides this functionality?

**Options:**
- (A) Auto Scaling
- (B) ElastiCache
- (C) Lambda
- (D) Auto Growing
- (E) Auto Scaling is the correct answer. AWS Auto Scaling can expand or contract the number of servers in a solution automatically based on current demands. This allows you to use and pay for the services you require, based on the load, but not more. No such service as Auto Growing exists. ElastiCache provides in memory caching. Lambda is a code execution engine that allows you to execute code without building out the instances required to run the code.
- (F) You must enable alerts and other notifications to be sent to the appropriate individuals from the AWS cloud. What AWS service can provide this function?
- (G) Amazon Simple Notification Service (SNS)
- (H) Amazon Kinesis
- (I) Amazon Simple Queue Service (SQS)
- (J) Amazon Simple Workflow (SWF)
- () Amazon Simple Notification Services (SNS) is the correct answer. SNS is used to send notifications, which can be sent via HTTP/HTTPS, SMS, Lambda, SQS, or e-mail. SQS is used for queueing requests so that they can be processed as needed. SWF is used to perform operations based on the state of a system and it is being replaced with step functions.
- () What two methods are provided in AWS RDS for database backups?
- () Manual backups and automated snapshots
- () Automated backups and manual snapshots
- () Manual backups and manual snapshots
- **() Automated backups and automated snapshots** [CORRECT]
- () Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

**Answer:**
Correct Answer: **Automated backups and automated snapshots**

**Explanation:**
Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

---

## Question 172

**Q:** You must enable alerts and other notifications to be sent to the appropriate individuals from the AWS cloud. What AWS service can provide this function?

**Options:**
- (A) Amazon Simple Notification Service (SNS)
- (B) Amazon Kinesis
- (C) Amazon Simple Queue Service (SQS)
- (D) Amazon Simple Workflow (SWF)
- (E) Amazon Simple Notification Services (SNS) is the correct answer. SNS is used to send notifications, which can be sent via HTTP/HTTPS, SMS, Lambda, SQS, or e-mail. SQS is used for queueing requests so that they can be processed as needed. SWF is used to perform operations based on the state of a system and it is being replaced with step functions.
- (F) What two methods are provided in AWS RDS for database backups?
- (G) Manual backups and automated snapshots
- (H) Automated backups and manual snapshots
- (I) Manual backups and manual snapshots
- **(J) Automated backups and automated snapshots** [CORRECT]
- () Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

**Answer:**
Correct Answer: **Automated backups and automated snapshots**

**Explanation:**
Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

---

## Question 173

**Q:** What two methods are provided in AWS RDS for database backups?

**Options:**
- (A) Manual backups and automated snapshots
- (B) Automated backups and manual snapshots
- (C) Manual backups and manual snapshots
- **(D) Automated backups and automated snapshots** [CORRECT]
- (E) Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

**Answer:**
Correct Answer: **Automated backups and automated snapshots**

**Explanation:**
Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

---

## Question 174

**Q:** When multiple resources can perform the same function, which one of the following is not a valid routing policy that Route 53 can use to select the appropriate resource for a request?

**Options:**
- (A) Geo DNS routing
- (B) Weighted round robin
- (C) OS-based routing
- (D) Latency-based routing
- (E) OS-based routing is the correct answer. Route 53 supports Geo DNS routing, Failover routing, Latency-based routing and Weighted round robin routing. It does not support redirection based on the OS of the requesting system.
- (F) Your company is generating a huge volume of data sets with billions of rows that must be summarized by column. You are going to use Tableau on top of these data sets to build daily and weekly reports. Which AWS service should you use to meet these requirements?
- **(G) Amazon Redshift** [CORRECT]
- (H) ElastiCache
- (I) Amazon DynamoDB
- (J) Amazon RDS
- () Amazon Redshift is correct. Amazon Redshift is Amazon’s data warehouse offering, where the data is stored in columnar format. 
- () Incorrect Answers:
- () Amazon RDS is incorrect because Amazon RDS is Amazon’s relational database offering, and in a relational database, the data is not stored in columnar format.
- () Amazon DynamoDB is incorrect because Amazon DynamoDB is a NoSQL database, which is based on key-value pair and does not store data in columnar format.
- () ElastiCache is incorrect because ElastiCache is used for caching database objects in order to provide a faster turnaround time.

**Answer:**
Correct Answer: **Amazon Redshift**

**Explanation:**
Amazon Redshift is correct. Amazon Redshift is Amazon’s data warehouse offering, where the data is stored in columnar format. 

---

## Question 175

**Q:** Your company is generating a huge volume of data sets with billions of rows that must be summarized by column. You are going to use Tableau on top of these data sets to build daily and weekly reports. Which AWS service should you use to meet these requirements?

**Options:**
- **(A) Amazon Redshift** [CORRECT]
- (B) ElastiCache
- (C) Amazon DynamoDB
- (D) Amazon RDS
- (E) Amazon Redshift is correct. Amazon Redshift is Amazon’s data warehouse offering, where the data is stored in columnar format. 
- (F) Incorrect Answers:
- (G) Amazon RDS is incorrect because Amazon RDS is Amazon’s relational database offering, and in a relational database, the data is not stored in columnar format.
- (H) Amazon DynamoDB is incorrect because Amazon DynamoDB is a NoSQL database, which is based on key-value pair and does not store data in columnar format.
- (I) ElastiCache is incorrect because ElastiCache is used for caching database objects in order to provide a faster turnaround time.

**Answer:**
Correct Answer: **Amazon Redshift**

**Explanation:**
Amazon Redshift is correct. Amazon Redshift is Amazon’s data warehouse offering, where the data is stored in columnar format. 

---

## Question 176

**Q:** You’re building out a single-region application in us-west-2. However, disaster recovery is a strong consideration, and you need to build the application so that if us-west-2 becomes unavailable, you can fail over to us-west-1. Your application relies exclusively on pre-built AMIs. In order to share those AMIs with the region you’re using as a backup, which process would you follow?

**Options:**
- (A) Copy the AMI from us-west-2 to us-west-1 and launch it as is.
- (B) Create a new instance in us-west-1, making certain the instance in the failover region shares a security group with the instance in the default region.
- (C) Copy the AMI from us-west-2, manually apply launch permissions, user-defined tags, and Amazon S3 bucket permissions of the default AMI to the new instance, and launch the instance.
- (D) Do nothing. AMIs are specific to an account, and they can be used anywhere.
- (E) Copy the AMI from us-west-2, manually apply launch permissions, user-defined tags, and Amazon S3 bucket permissions of the default AMI to the new instance, and launch the instance is correct because AWS does not copy launch permissions, user-defined tags, or Amazon S3 bucket permissions from the source AMI to the new AMI. 
- (F) Incorrect Answers:
- (G) Create a new instance in us-west-1, making certain the instance in the failover region shares a security group with the instance in the default region is incorrect because creating a new instance won’t copy the properties like user-defined tags, launch permissions and so on.
- (H) Do nothing. AMIs are specific to an account, and they can be used anywhere is incorrect because AMIs are tied to a region.
- (I) Copy the AMI from us-west-2 to us-west-1 and launch it as is is incorrect because copying the AMI won’t copy the properties.
- (J) How long are one-minute data points maintained for viewing in Amazon CloudWatch?
- () 15 days
- () 15 months
- () 63 days
- () Indefinitely
- () 15 days is the correct answer. One-minute data points are maintained for 15 days. Five-minute data points are maintained for 63 days. One-hour data points are maintained for 15 months or 455 days.
- () Which one of the following scenarios would result in a higher percentage of savings when using S3 Standard Infrequent Access storage instead of S3 Standard storage?
- **() 1 TB monthly with 10% of content accessed per month** [CORRECT]
- () None of these, content accessed per month must be less then 5% to generate any savings
- () 1 TB monthly with 100% of content accessed per month
- () 1 TB monthly with 50% of content accessed per month
- () 1 TB monthly with 10% of content accessed per month is the correct answer. According to the AWS 2020 Cost Optimization Pillar documentation, the consumption model is defined as paying only for the computing resources you consume and increasing or decreasing usage depending on business requirements. The other named models are not referenced in AWS documentation for the Cost Optimization Pillar.
- () In which of the following services can you have root-level access to the operating system? (Choose two.)
- () Correct selection
- () Amazon EMR
- () Amazon DynamoDB
- () Amazon RDS
- () Amazon EC2
- () Correct Answers:
- () Amazon EC2 and Amazon EMR are correct. Only Amazon EC2 and EMR provide root-level access.
- () Amazon RDS and Amazon DynamoDB are incorrect. Amazon EMR and Amazon DynamoDB are managed services for which you don’t have root-level access.

**Answer:**
Correct Answer: **1 TB monthly with 10% of content accessed per month**

**Explanation:**
1 TB monthly with 10% of content accessed per month is the correct answer. According to the AWS 2020 Cost Optimization Pillar documentation, the consumption model is defined as paying only for the computing resources you consume and increasing or decreasing usage depending on business requirements. The other named models are not referenced in AWS documentation for the Cost Optimization Pillar.

---

## Question 177

**Q:** How long are one-minute data points maintained for viewing in Amazon CloudWatch?

**Options:**
- (A) 15 days
- (B) 15 months
- (C) 63 days
- (D) Indefinitely
- (E) 15 days is the correct answer. One-minute data points are maintained for 15 days. Five-minute data points are maintained for 63 days. One-hour data points are maintained for 15 months or 455 days.
- (F) Which one of the following scenarios would result in a higher percentage of savings when using S3 Standard Infrequent Access storage instead of S3 Standard storage?
- **(G) 1 TB monthly with 10% of content accessed per month** [CORRECT]
- (H) None of these, content accessed per month must be less then 5% to generate any savings
- (I) 1 TB monthly with 100% of content accessed per month
- (J) 1 TB monthly with 50% of content accessed per month
- () 1 TB monthly with 10% of content accessed per month is the correct answer. According to the AWS 2020 Cost Optimization Pillar documentation, the consumption model is defined as paying only for the computing resources you consume and increasing or decreasing usage depending on business requirements. The other named models are not referenced in AWS documentation for the Cost Optimization Pillar.
- () In which of the following services can you have root-level access to the operating system? (Choose two.)
- () Correct selection
- () Amazon EMR
- () Amazon DynamoDB
- () Amazon RDS
- () Amazon EC2
- () Correct Answers:
- () Amazon EC2 and Amazon EMR are correct. Only Amazon EC2 and EMR provide root-level access.
- () Incorrect Answers:
- () Amazon RDS and Amazon DynamoDB are incorrect. Amazon EMR and Amazon DynamoDB are managed services for which you don’t have root-level access.

**Answer:**
Correct Answer: **1 TB monthly with 10% of content accessed per month**

**Explanation:**
1 TB monthly with 10% of content accessed per month is the correct answer. According to the AWS 2020 Cost Optimization Pillar documentation, the consumption model is defined as paying only for the computing resources you consume and increasing or decreasing usage depending on business requirements. The other named models are not referenced in AWS documentation for the Cost Optimization Pillar.

---

## Question 178

**Q:** Which one of the following scenarios would result in a higher percentage of savings when using S3 Standard Infrequent Access storage instead of S3 Standard storage?

**Options:**
- **(A) 1 TB monthly with 10% of content accessed per month** [CORRECT]
- (B) None of these, content accessed per month must be less then 5% to generate any savings
- (C) 1 TB monthly with 100% of content accessed per month
- (D) 1 TB monthly with 50% of content accessed per month
- (E) 1 TB monthly with 10% of content accessed per month is the correct answer. According to the AWS 2020 Cost Optimization Pillar documentation, the consumption model is defined as paying only for the computing resources you consume and increasing or decreasing usage depending on business requirements. The other named models are not referenced in AWS documentation for the Cost Optimization Pillar.
- (F) In which of the following services can you have root-level access to the operating system? (Choose two.)
- (G) Correct selection
- (H) Amazon EMR
- (I) Amazon DynamoDB
- (J) Amazon RDS
- () Amazon EC2
- () Correct Answers:
- () Amazon EC2 and Amazon EMR are correct. Only Amazon EC2 and EMR provide root-level access.
- () Incorrect Answers:
- () Amazon RDS and Amazon DynamoDB are incorrect. Amazon EMR and Amazon DynamoDB are managed services for which you don’t have root-level access.

**Answer:**
Correct Answer: **1 TB monthly with 10% of content accessed per month**

**Explanation:**
1 TB monthly with 10% of content accessed per month is the correct answer. According to the AWS 2020 Cost Optimization Pillar documentation, the consumption model is defined as paying only for the computing resources you consume and increasing or decreasing usage depending on business requirements. The other named models are not referenced in AWS documentation for the Cost Optimization Pillar.

---

## Question 179

**Q:** In which of the following services can you have root-level access to the operating system? (Choose two.)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Amazon EMR
- (C) Amazon DynamoDB
- (D) Amazon RDS
- (E) Amazon EC2
- (F) Correct Answers:
- (G) Amazon EC2 and Amazon EMR are correct. Only Amazon EC2 and EMR provide root-level access.
- (H) Incorrect Answers:
- (I) Amazon RDS and Amazon DynamoDB are incorrect. Amazon EMR and Amazon DynamoDB are managed services for which you don’t have root-level access.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 180

**Q:** You are concerned about maintaining security patches on the 103 AWS EC2 instances that you run. All instances run Windows, Ubuntu Server, or Red Hat Enterprise Linux. What AWS service can assist you on properly and automatically patching these instances?

**Options:**
- (A) AWS Systems Manager Patch Manager
- (B) AMI Manager
- (C) CloudFormation
- (D) CodeDeploy
- (E) AWS Systems Manager Patch Manager is the correct answer. The AWS Systems Manager Patch Manager can automate security patches for supported Windows and Linux systems. It can also apply non-security patches to Linux systems. AMI Manager does not exist in AWS and the other services do not provide this functionality.
- (F) How many hours of EC2 compute are provided in the free tier?
- (G) 750
- (H) 1000
- (I) 500
- (J) 250
- () 750 is the correct answer. 750 hours of compute are provided when using free tier instance classes for the first 12 months in AWS. Amazon RDS provides the same number of hours of compute for databases in the same 12-month window.
- () You are planning VPC deployments. What is the maximum number of subnets that can be created in a VPC?
- **() 200** [CORRECT]
- () 200 is the correct answer. VPCs can contain up to 200 subnets. A region can contain up to 5 VPCs by default.

**Answer:**
Correct Answer: **200**

**Explanation:**
200 is the correct answer. VPCs can contain up to 200 subnets. A region can contain up to 5 VPCs by default.

---

## Question 181

**Q:** How many hours of EC2 compute are provided in the free tier?

**Options:**
- (A) 750
- (B) 1000
- (C) 500
- (D) 250
- (E) 750 is the correct answer. 750 hours of compute are provided when using free tier instance classes for the first 12 months in AWS. Amazon RDS provides the same number of hours of compute for databases in the same 12-month window.
- (F) You are planning VPC deployments. What is the maximum number of subnets that can be created in a VPC?
- **(G) 200** [CORRECT]
- (H) 200 is the correct answer. VPCs can contain up to 200 subnets. A region can contain up to 5 VPCs by default.

**Answer:**
Correct Answer: **200**

**Explanation:**
200 is the correct answer. VPCs can contain up to 200 subnets. A region can contain up to 5 VPCs by default.

---

## Question 182

**Q:** You are planning VPC deployments. What is the maximum number of subnets that can be created in a VPC?

**Options:**
- **(A) 200** [CORRECT]
- (B) 200 is the correct answer. VPCs can contain up to 200 subnets. A region can contain up to 5 VPCs by default.

**Answer:**
Correct Answer: **200**

**Explanation:**
200 is the correct answer. VPCs can contain up to 200 subnets. A region can contain up to 5 VPCs by default.

---

## Question 183

**Q:** You manage a Ruby on Rails application that lives on a cluster of EC2 instances. Your website occasionally experiences brief, strong, and entirely unpredictable spikes in traffic that overwhelm your EC2 instances’ resources and freeze the application. As a result, you’re losing recently submitted requests from end users. You use Auto Scaling to deploy additional resources to handle the load during spikes, but the new instances don’t spin up fast enough to prevent the existing application servers from freezing. Which of the following actions will provide the most cost-effective solution in preventing the loss of recently submitted requests?

**Options:**
- (A) Keep a large EC2 instance on standby.
- (B) Increase the size of your existing EC2 instances.
- **(C) Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto Scaling instances are available.** [CORRECT]
- (D) Ask AWS support to pre-warm the Elastic Load Balancer.
- (E) Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto Scaling instances are available is correct. The cost-effective solution to the unpredictable spike in traffic is to use SQS to decouple the application components.
- (F) Incorrect Answers:
- (G) Increase the size of your existing EC2 instances is incorrect because increasing the size of EC2 will increase the cost.
- (H) Ask AWS support to pre-warm the Elastic Load Balancer is incorrect because pre-warming of the ELB can be done only when the traffic is predictable.
- (I) Keep a large EC2 instance on standby is incorrect because keeping large EC2 servers on standby is going to spike the cost.

**Answer:**
Correct Answer: **Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto Scaling instances are available.**

**Explanation:**
Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto Scaling instances are available is correct. The cost-effective solution to the unpredictable spike in traffic is to use SQS to decouple the application components.

---

## Question 184

**Q:** When considering NACLs and security groups, what is evaluated first when a packet is inbound to an EC2 instance?

**Options:**
- (A) Neither, they are processed at the same time
- (B) Security group then NACL
- **(C) NACL then security group** [CORRECT]
- (D) Neither, they cannot be used together
- (E) NACL then security group is the correct answer. NACLs and security groups can be used together in the flow of traffic into an EC2 instance. Because the NACLs are associated with the subnet, they are processed first and then security groups, which are associated with the instance network interface, are processed.

**Answer:**
Correct Answer: **NACL then security group**

**Explanation:**
NACL then security group is the correct answer. NACLs and security groups can be used together in the flow of traffic into an EC2 instance. Because the NACLs are associated with the subnet, they are processed first and then security groups, which are associated with the instance network interface, are processed.

---

## Question 185

**Q:** You are defining appropriate security options for S3 buckets in AWS. As part of the process, you must identify the default access restrictions on S3 buckets. Which one of the following best describes the default access restrictions in place on S3 buckets?

**Options:**
- (A) Only bucket and object owners have access to the resources they create
- (B) Anonymous users have access to all S3 buckets and objects
- (C) Only IAM administrators have access to S3 buckets
- (D) All IAM users have access to all S3 buckets and objects
- (E) Only bucket and object owners have access to the resources they create is the correct answer. By default, only buck and object owners have access to the resources they create, and other users must be granted access or access must be granted to public or anonymous users, if desired.
- (F) What does AWS provide for extremely large dataset transport to the cloud that provides for offline transport?
- (G) Glacier
- **(H) Snowball** [CORRECT]
- (I) CloudFront
- (J) Snowball is the correct answer. Snowball is used to transport large datasets offline. Glacier and S3 are online storage services. CloudFront is a web cache service.

**Answer:**
Correct Answer: **Snowball**

**Explanation:**
Snowball is the correct answer. Snowball is used to transport large datasets offline. Glacier and S3 are online storage services. CloudFront is a web cache service.

---

## Question 186

**Q:** What does AWS provide for extremely large dataset transport to the cloud that provides for offline transport?

**Options:**
- (A) Glacier
- **(B) Snowball** [CORRECT]
- (C) CloudFront
- (D) Snowball is the correct answer. Snowball is used to transport large datasets offline. Glacier and S3 are online storage services. CloudFront is a web cache service.

**Answer:**
Correct Answer: **Snowball**

**Explanation:**
Snowball is the correct answer. Snowball is used to transport large datasets offline. Glacier and S3 are online storage services. CloudFront is a web cache service.

---

## Question 187

**Q:** Your application uploads several thousands of files every day. The file sizes range from 500MB to 2GB. Each file is then processed to extract metadata, and the metadata processing takes a few seconds. There is no fixed uploading frequency; sometimes all the files are uploaded at a particular hour, sometimes only a few files are uploaded at a particular hour, and sometimes no uploads occur for a few hours. What is the most cost-effective way of handling this issue?

**Options:**
- (A) Use Amazon Kinesis to store the files and then use Lambda for extracting the metadata.
- (B) Use EFS to store the file and then use multiple EC2 instances to extract the metadata.
- (C) Use an SQS queue to store the file and then use an EC2 instance to extract the metadata.
- (D) Store the files in Amazon S3 and then use an S3 event notification to invoke a Lambda function for extracting the metadata.
- (E) Store the files in Amazon S3 and then use an S3 event notification to invoke a Lambda function for extracting the metadata is correct. Amazon S3 is the cheapest solution in this case.
- (F) Incorrect Answers:
- (G) You are required to run Docker containers within AWS. What AWS solution provides this service?
- (H) Lambda
- (I) EC2 Container Service (ECS)
- (J) Lightsail
- () CloudFormation
- () EC2 Container Service (ECS) is the correct answer. ECS is the AWS container service and it allows for the execution of Docker containers. Lambda is a code execution engine that allows you to execute code without building out the instances required to run the code. CloudFormation is an AWS service used to automatically launch entire solutions (including multiple instances and services) through code. Lightsail is the AWS service used to simply deploy web applications and web sites in AWS.
- () You must backup an EBS volume as quickly as possible and perform this backup once each day. What is the best method provided within AWS to perform this backup?
- () RDS backup
- () Backup software centralized in one EC2 instance used to backup other instance attached EBS volumes
- **() Snapshots** [CORRECT]
- () Internal backup software in the EC2 instance
- () Snapshots is the correct answer. Snapshots are incremental backups such that they backup only the blocks that have changed in the EBS volume since the last snapshot was taken. This provides a fast backup option. The other options of using backup software will take much longer and require more administrative overhead. RDS backup cannot be used to backup EBS volumes, it is used to backup databases.

**Answer:**
Correct Answer: **Snapshots**

**Explanation:**
Snapshots is the correct answer. Snapshots are incremental backups such that they backup only the blocks that have changed in the EBS volume since the last snapshot was taken. This provides a fast backup option. The other options of using backup software will take much longer and require more administrative overhead. RDS backup cannot be used to backup EBS volumes, it is used to backup databases.

---

## Question 188

**Q:** You are required to run Docker containers within AWS. What AWS solution provides this service?

**Options:**
- (A) Lambda
- (B) EC2 Container Service (ECS)
- (C) Lightsail
- (D) CloudFormation
- (E) EC2 Container Service (ECS) is the correct answer. ECS is the AWS container service and it allows for the execution of Docker containers. Lambda is a code execution engine that allows you to execute code without building out the instances required to run the code. CloudFormation is an AWS service used to automatically launch entire solutions (including multiple instances and services) through code. Lightsail is the AWS service used to simply deploy web applications and web sites in AWS.
- (F) You must backup an EBS volume as quickly as possible and perform this backup once each day. What is the best method provided within AWS to perform this backup?
- (G) RDS backup
- (H) Backup software centralized in one EC2 instance used to backup other instance attached EBS volumes
- **(I) Snapshots** [CORRECT]
- (J) Internal backup software in the EC2 instance
- () Snapshots is the correct answer. Snapshots are incremental backups such that they backup only the blocks that have changed in the EBS volume since the last snapshot was taken. This provides a fast backup option. The other options of using backup software will take much longer and require more administrative overhead. RDS backup cannot be used to backup EBS volumes, it is used to backup databases.

**Answer:**
Correct Answer: **Snapshots**

**Explanation:**
Snapshots is the correct answer. Snapshots are incremental backups such that they backup only the blocks that have changed in the EBS volume since the last snapshot was taken. This provides a fast backup option. The other options of using backup software will take much longer and require more administrative overhead. RDS backup cannot be used to backup EBS volumes, it is used to backup databases.

---

## Question 189

**Q:** You must backup an EBS volume as quickly as possible and perform this backup once each day. What is the best method provided within AWS to perform this backup?

**Options:**
- (A) RDS backup
- (B) Backup software centralized in one EC2 instance used to backup other instance attached EBS volumes
- **(C) Snapshots** [CORRECT]
- (D) Internal backup software in the EC2 instance
- (E) Snapshots is the correct answer. Snapshots are incremental backups such that they backup only the blocks that have changed in the EBS volume since the last snapshot was taken. This provides a fast backup option. The other options of using backup software will take much longer and require more administrative overhead. RDS backup cannot be used to backup EBS volumes, it is used to backup databases.

**Answer:**
Correct Answer: **Snapshots**

**Explanation:**
Snapshots is the correct answer. Snapshots are incremental backups such that they backup only the blocks that have changed in the EBS volume since the last snapshot was taken. This provides a fast backup option. The other options of using backup software will take much longer and require more administrative overhead. RDS backup cannot be used to backup EBS volumes, it is used to backup databases.

---

## Question 190

**Q:** You are in the process of designing a document archive solution for your company. The solution must be cost-effective; therefore, you have selected Glacier. The business wants to have the capability to get a document within 15 minutes of requesting it. Which feature of Amazon Glacier will you choose?

**Options:**
- (A) Glacier is not the correct solution. You need Amazon S3.
- (B) Expedited retrieval
- (C) Standard retrieval
- (D) Bulk retrieval
- (E) Expedited retrieval is correct. Since you are looking for a cost-effective archival solution, Amazon Glacier is the right choice. By using the expedited retrieval option, you should be able to get the file within 5 minutes, which meets your business objective. 
- (F) Incorrect Answers:
- (G) Standard retrieval is incorrect because standard retrieval won’t be able to meet the 15-minute SLA.
- (H) Glacier is not the correct solution. You need Amazon S3 is incorrect because you are developing an archival solution. If you choose S3, cost will go up.
- (I) Bulk retrieval is incorrect because bulk retrieval won’t be able to meet the 15-minute SLA.
- (J) When it comes to security groups within a custom VPC, which of the following statements are correct? (Choose two.)
- () Updates to security groups are not applied immediately; however, they are applied within the hour in which they are made.
- () Correct selection
- () Updates to security groups are applied immediately.
- () Security groups are stateless.
- () Security groups are stateful.
- () Correct Answers:
- () Updates to security groups are applied immediately and Security groups are stateful are correct. Any update to security group happens instantly and gets propagated automatically to the EC2 instances. There is no need to bounce the instances or restart anything.
- () Security groups are stateless is incorrect because security groups are stateful.
- () Updates to security groups are not applied immediately; however, they are applied within the hour in which they are made is incorrect because any update to a security group is applied immediately.
- () What AWS service can be used to monitor your EC2 instances and provide a dashboard for performance management?
- () CloudFormation
- () CloudFront
- () Performance Monitor
- () CloudWatch
- () CloudWatch is the correct answer. CloudWatch is an AWS service that can gather metrics from multiple sources and provide dashboards for monitoring. CloudFront is a content distribution network (CDN) solution. CloudFormation is used to provision resources for a cloud solution automatically. Performance monitor is a performance monitoring tool in Windows and not an AWS service.
- () You are in the process of deploying an application in an EC2 instance. The application must call AWS APIs. What is the secured way of passing credentials to the application?
- () Use a DynamoDB to store the API credentials.
- **() Assign IAM roles to the EC2 instance.** [CORRECT]
- () Pass the API credentials to the instance using instance user data.
- () Keep API credentials as an object in Amazon S3.
- () Assign IAM roles to the EC2 instance is correct. You need to use IAM roles to pass credentials to the application in a secured way.
- () Pass the API credentials to the instance using instance user data is incorrect because passing API credentials to the instance using the instance user data is not a solution since API credentials may change or you might change the EC2 server.

**Answer:**
Correct Answer: **Assign IAM roles to the EC2 instance.**

**Explanation:**
Assign IAM roles to the EC2 instance is correct. You need to use IAM roles to pass credentials to the application in a secured way.

---

## Question 191

**Q:** When it comes to security groups within a custom VPC, which of the following statements are correct? (Choose two.)

**Options:**
- (A) Updates to security groups are not applied immediately; however, they are applied within the hour in which they are made.
- (B) Correct selection
- (C) Updates to security groups are applied immediately.
- (D) Security groups are stateless.
- (E) Security groups are stateful.
- (F) Correct Answers:
- (G) Updates to security groups are applied immediately and Security groups are stateful are correct. Any update to security group happens instantly and gets propagated automatically to the EC2 instances. There is no need to bounce the instances or restart anything.
- (H) Incorrect Answers:
- (I) Security groups are stateless is incorrect because security groups are stateful.
- (J) Updates to security groups are not applied immediately; however, they are applied within the hour in which they are made is incorrect because any update to a security group is applied immediately.
- () What AWS service can be used to monitor your EC2 instances and provide a dashboard for performance management?
- () CloudFormation
- () CloudFront
- () Performance Monitor
- () CloudWatch
- () CloudWatch is the correct answer. CloudWatch is an AWS service that can gather metrics from multiple sources and provide dashboards for monitoring. CloudFront is a content distribution network (CDN) solution. CloudFormation is used to provision resources for a cloud solution automatically. Performance monitor is a performance monitoring tool in Windows and not an AWS service.
- () You are in the process of deploying an application in an EC2 instance. The application must call AWS APIs. What is the secured way of passing credentials to the application?
- () Use a DynamoDB to store the API credentials.
- () Assign IAM roles to the EC2 instance.
- () Pass the API credentials to the instance using instance user data.
- () Keep API credentials as an object in Amazon S3.
- () Assign IAM roles to the EC2 instance is correct. You need to use IAM roles to pass credentials to the application in a secured way.
- () Pass the API credentials to the instance using instance user data is incorrect because passing API credentials to the instance using the instance user data is not a solution since API credentials may change or you might change the EC2 server.
- () You monitor your usage in AWS to increase or decrease resources based on current business requirements. This careful monitoring and response is taken to reduce costs. What model is being implemented according to the AWS Cost Optimization Pillar?
- () Production Model
- () Efficiency Model
- **() Consumption Model** [CORRECT]
- () Development Model

**Answer:**
Correct Answer: **Consumption Model**

**Explanation:**
Consumption Model is the correct answer. AWS is continually releasing new services. In many cases, processes currently running in dedicated EC2 instances can be moved to the services and significantly reduce costs. S3 Standard may be too expensive for many storage requirements. EIPs incur a charge as they are static addresses and should only be used when a static address is required. Many EC2 instances do not require high availability and implementing redundant instances when they are not required increases costs.

---

## Question 192

**Q:** What AWS service can be used to monitor your EC2 instances and provide a dashboard for performance management?

**Options:**
- (A) CloudFormation
- (B) CloudFront
- (C) Performance Monitor
- (D) CloudWatch
- (E) CloudWatch is the correct answer. CloudWatch is an AWS service that can gather metrics from multiple sources and provide dashboards for monitoring. CloudFront is a content distribution network (CDN) solution. CloudFormation is used to provision resources for a cloud solution automatically. Performance monitor is a performance monitoring tool in Windows and not an AWS service.
- (F) You are in the process of deploying an application in an EC2 instance. The application must call AWS APIs. What is the secured way of passing credentials to the application?
- (G) Use a DynamoDB to store the API credentials.
- (H) Assign IAM roles to the EC2 instance.
- (I) Pass the API credentials to the instance using instance user data.
- (J) Keep API credentials as an object in Amazon S3.
- () Assign IAM roles to the EC2 instance is correct. You need to use IAM roles to pass credentials to the application in a secured way.
- () Incorrect Answers:
- () Pass the API credentials to the instance using instance user data is incorrect because passing API credentials to the instance using the instance user data is not a solution since API credentials may change or you might change the EC2 server.
- () You monitor your usage in AWS to increase or decrease resources based on current business requirements. This careful monitoring and response is taken to reduce costs. What model is being implemented according to the AWS Cost Optimization Pillar?
- () Production Model
- () Efficiency Model
- **() Consumption Model** [CORRECT]
- () Development Model
- () You have a fleet of EC2 instances hosting your application, running in an on-demand model that is billed on an hourly basis. For running your application, you have enabled Auto Scaling for scaling up and down, as per the workload, and while reviewing the Auto Scaling events you notice that the application is scaling up and down multiple times within the same hour. What would you do to optimize the cost while preserving elasticity at the same time? (Choose two.)
- () Correct selection
- () Change the Auto Scaling group’s cool-down time.
- () Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy.
- () Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy.
- () Use a reserved instance instead of an on-demand instance to optimize cost.
- () Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy.
- () Correct Answers:
- () Change the Auto Scaling group’s cool-down time and Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy are correct because you can modify the Auto Scaling group’s cool down time so that an EC2 instance can run for nearly an hour instead of running for a few minutes. If the EC2 instance runs even for a few minutes, you are still going to pay for the hour, so why not run it until the close of the hour. 
- () Use a reserved instance instead of an on-demand instance to optimize cost is incorrect because, in this case, you can’t use a reserved instance since you don’t know the optimal number of EC2 instances you will always be running.
- () Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because even if you terminate the longest-running EC2 instance, it won’t help you to optimize cost.
- () Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because by terminating the newest-running EC2 instance, you won’t save additional cost.

**Answer:**
Correct Answer: **Consumption Model**

**Explanation:**
Consumption Model is the correct answer. AWS is continually releasing new services. In many cases, processes currently running in dedicated EC2 instances can be moved to the services and significantly reduce costs. S3 Standard may be too expensive for many storage requirements. EIPs incur a charge as they are static addresses and should only be used when a static address is required. Many EC2 instances do not require high availability and implementing redundant instances when they are not required increases costs.

---

## Question 193

**Q:** You are in the process of deploying an application in an EC2 instance. The application must call AWS APIs. What is the secured way of passing credentials to the application?

**Options:**
- (A) Use a DynamoDB to store the API credentials.
- (B) Assign IAM roles to the EC2 instance.
- (C) Pass the API credentials to the instance using instance user data.
- (D) Keep API credentials as an object in Amazon S3.
- (E) Assign IAM roles to the EC2 instance is correct. You need to use IAM roles to pass credentials to the application in a secured way.
- (F) Incorrect Answers:
- (G) Pass the API credentials to the instance using instance user data is incorrect because passing API credentials to the instance using the instance user data is not a solution since API credentials may change or you might change the EC2 server.
- (H) You monitor your usage in AWS to increase or decrease resources based on current business requirements. This careful monitoring and response is taken to reduce costs. What model is being implemented according to the AWS Cost Optimization Pillar?
- (I) Production Model
- (J) Efficiency Model
- () Consumption Model
- () Development Model
- () You have a fleet of EC2 instances hosting your application, running in an on-demand model that is billed on an hourly basis. For running your application, you have enabled Auto Scaling for scaling up and down, as per the workload, and while reviewing the Auto Scaling events you notice that the application is scaling up and down multiple times within the same hour. What would you do to optimize the cost while preserving elasticity at the same time? (Choose two.)
- () Correct selection
- () Change the Auto Scaling group’s cool-down time.
- () Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy.
- () Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy.
- () Use a reserved instance instead of an on-demand instance to optimize cost.
- () Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy.
- () Correct Answers:
- () Change the Auto Scaling group’s cool-down time and Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy are correct because you can modify the Auto Scaling group’s cool down time so that an EC2 instance can run for nearly an hour instead of running for a few minutes. If the EC2 instance runs even for a few minutes, you are still going to pay for the hour, so why not run it until the close of the hour. 
- () Use a reserved instance instead of an on-demand instance to optimize cost is incorrect because, in this case, you can’t use a reserved instance since you don’t know the optimal number of EC2 instances you will always be running.
- () Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because even if you terminate the longest-running EC2 instance, it won’t help you to optimize cost.
- () Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because by terminating the newest-running EC2 instance, you won’t save additional cost.
- () Dump 4
- () A company offers an online product brochure that is delivered from a static website running on Amazon S3. The company’s customers are mainly in the United States, Canada, and Mexico. The company is looking to cost-effectively reduce the latency for users in these regions.
- () What is the most cost-effective solution to these requirements?
- () Create an Amazon CloudFront distribution and set the price class to use all Edge Locations for best performance.
- () Create an Amazon CloudFront distribution that uses origins in U.S, Canada and Mexico.
- () Create an Amazon CloudFront distribution and use Lambda@Edge to run the website's data processing closer to the users.
- **() Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.** [CORRECT]
- () With Amazon CloudFront you can set the price class to determine where in the world the content will be cached. One of the price classes is “U.S, Canada and Mexico” and this is where the company’s users are located. Choosing this price class will result in lower costs and better performance for the company’s users.

**Answer:**
Correct Answer: **Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.**

**Explanation:**
Consumption Model is the correct answer. AWS is continually releasing new services. In many cases, processes currently running in dedicated EC2 instances can be moved to the services and significantly reduce costs. S3 Standard may be too expensive for many storage requirements. EIPs incur a charge as they are static addresses and should only be used when a static address is required. Many EC2 instances do not require high availability and implementing redundant instances when they are not required increases costs.

---

## Question 194

**Q:** You monitor your usage in AWS to increase or decrease resources based on current business requirements. This careful monitoring and response is taken to reduce costs. What model is being implemented according to the AWS Cost Optimization Pillar?

**Options:**
- (A) Production Model
- (B) Efficiency Model
- (C) Consumption Model
- (D) Development Model
- (E) You have a fleet of EC2 instances hosting your application, running in an on-demand model that is billed on an hourly basis. For running your application, you have enabled Auto Scaling for scaling up and down, as per the workload, and while reviewing the Auto Scaling events you notice that the application is scaling up and down multiple times within the same hour. What would you do to optimize the cost while preserving elasticity at the same time? (Choose two.)
- (F) Correct selection
- (G) Change the Auto Scaling group’s cool-down time.
- (H) Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy.
- (I) Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy.
- (J) Use a reserved instance instead of an on-demand instance to optimize cost.
- () Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy.
- () Correct Answers:
- () Change the Auto Scaling group’s cool-down time and Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy are correct because you can modify the Auto Scaling group’s cool down time so that an EC2 instance can run for nearly an hour instead of running for a few minutes. If the EC2 instance runs even for a few minutes, you are still going to pay for the hour, so why not run it until the close of the hour. 
- () Incorrect Answers:
- () Use a reserved instance instead of an on-demand instance to optimize cost is incorrect because, in this case, you can’t use a reserved instance since you don’t know the optimal number of EC2 instances you will always be running.
- () Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because even if you terminate the longest-running EC2 instance, it won’t help you to optimize cost.
- () Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because by terminating the newest-running EC2 instance, you won’t save additional cost.
- () Dump 4
- () A company offers an online product brochure that is delivered from a static website running on Amazon S3. The company’s customers are mainly in the United States, Canada, and Mexico. The company is looking to cost-effectively reduce the latency for users in these regions.
- () What is the most cost-effective solution to these requirements?
- () Create an Amazon CloudFront distribution and set the price class to use all Edge Locations for best performance.
- () Create an Amazon CloudFront distribution that uses origins in U.S, Canada and Mexico.
- () Create an Amazon CloudFront distribution and use Lambda@Edge to run the website's data processing closer to the users.
- **() Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.** [CORRECT]
- () With Amazon CloudFront you can set the price class to determine where in the world the content will be cached. One of the price classes is “U.S, Canada and Mexico” and this is where the company’s users are located. Choosing this price class will result in lower costs and better performance for the company’s users.
- ()  is the correct answer.
- ()  is incorrect. This will be more expensive as it will cache content in Edge Locations all over the world.
- ()  is incorrect. The origin can be in one place, there’s no need to add origins in different Regions. The price class should be used to limit the caching of the content to reduce cost.
- ()  is incorrect. Lambda@Edge will not assist in this situation as there is no data processing required, the content from the static website must simply be cached at an edge location.
- () References:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Networking & Content Delivery
- () A new application is to be published in multiple regions around the world. The Architect needs to ensure only 2 IP addresses need to be whitelisted. The solution should intelligently route traffic for lowest latency and provide fast regional failover.
- () How can this be achieved?
- () Launch EC2 instances into multiple regions behind an ALB and use Amazon CloudFront with a pair of static IP addresses
- () Launch EC2 instances into multiple regions behind an ALB and use a Route 53 failover routing policy
- () Launch EC2 instances into multiple regions behind an NLB with a static IP address

**Answer:**
Correct Answer: **Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.**

**Explanation:**
Consumption Model is the correct answer. AWS is continually releasing new services. In many cases, processes currently running in dedicated EC2 instances can be moved to the services and significantly reduce costs. S3 Standard may be too expensive for many storage requirements. EIPs incur a charge as they are static addresses and should only be used when a static address is required. Many EC2 instances do not require high availability and implementing redundant instances when they are not required increases costs.

---

## Question 195

**Q:** You have a fleet of EC2 instances hosting your application, running in an on-demand model that is billed on an hourly basis. For running your application, you have enabled Auto Scaling for scaling up and down, as per the workload, and while reviewing the Auto Scaling events you notice that the application is scaling up and down multiple times within the same hour. What would you do to optimize the cost while preserving elasticity at the same time? (Choose two.)

**Options:**
- (A) Correct selection
- (B) Change the Auto Scaling group’s cool-down time.
- (C) Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy.
- (D) Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy.
- (E) Use a reserved instance instead of an on-demand instance to optimize cost.
- (F) Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy.
- (G) Correct Answers:
- (H) Change the Auto Scaling group’s cool-down time and Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy are correct because you can modify the Auto Scaling group’s cool down time so that an EC2 instance can run for nearly an hour instead of running for a few minutes. If the EC2 instance runs even for a few minutes, you are still going to pay for the hour, so why not run it until the close of the hour. 
- (I) Incorrect Answers:
- (J) Use a reserved instance instead of an on-demand instance to optimize cost is incorrect because, in this case, you can’t use a reserved instance since you don’t know the optimal number of EC2 instances you will always be running.
- () Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because even if you terminate the longest-running EC2 instance, it won’t help you to optimize cost.
- () Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy is incorrect because by terminating the newest-running EC2 instance, you won’t save additional cost.
- () Dump 4
- () A company offers an online product brochure that is delivered from a static website running on Amazon S3. The company’s customers are mainly in the United States, Canada, and Mexico. The company is looking to cost-effectively reduce the latency for users in these regions.
- () What is the most cost-effective solution to these requirements?
- () Create an Amazon CloudFront distribution and set the price class to use all Edge Locations for best performance.
- () Create an Amazon CloudFront distribution that uses origins in U.S, Canada and Mexico.
- () Create an Amazon CloudFront distribution and use Lambda@Edge to run the website's data processing closer to the users.
- () Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.
- () With Amazon CloudFront you can set the price class to determine where in the world the content will be cached. One of the price classes is “U.S, Canada and Mexico” and this is where the company’s users are located. Choosing this price class will result in lower costs and better performance for the company’s users.
- ()  is the correct answer.
- ()  is incorrect. This will be more expensive as it will cache content in Edge Locations all over the world.
- ()  is incorrect. The origin can be in one place, there’s no need to add origins in different Regions. The price class should be used to limit the caching of the content to reduce cost.
- ()  is incorrect. Lambda@Edge will not assist in this situation as there is no data processing required, the content from the static website must simply be cached at an edge location.
- () References:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Networking & Content Delivery
- () A new application is to be published in multiple regions around the world. The Architect needs to ensure only 2 IP addresses need to be whitelisted. The solution should intelligently route traffic for lowest latency and provide fast regional failover.
- () How can this be achieved?
- () Launch EC2 instances into multiple regions behind an ALB and use Amazon CloudFront with a pair of static IP addresses
- () Launch EC2 instances into multiple regions behind an ALB and use a Route 53 failover routing policy
- () Launch EC2 instances into multiple regions behind an NLB with a static IP address
- **() Launch EC2 instances into multiple regions behind an NLB and use AWS Global Accelerator** [CORRECT]
- () AWS Global Accelerator uses the vast, congestion-free AWS global network to route TCP and UDP traffic to a healthy application endpoint in the closest AWS Region to the user.
- () This means it will intelligently route traffic to the closest point of presence (reducing latency). Seamless failover is ensured as AWS Global Accelerator uses anycast IP address which means the IP does not change when failing over between regions so there are no issues with client caches having incorrect entries that need to expire.
- () This is the only solution that provides deterministic failover.
- ()  is incorrect. An NLB with a static IP is a workable solution as you could configure a primary and secondary address in applications. However, this solution does not intelligently route traffic for lowest latency.
- ()  is incorrect. A Route 53 failover routing policy uses a primary and standby configuration. Therefore, it sends all traffic to the primary until it fails a health check at which time it sends traffic to the secondary. This solution does not intelligently route traffic for lowest latency.
- ()  is incorrect. Amazon CloudFront cannot be configured with “a pair of static IP addresses”.
- () https://aws.amazon.com/global-accelerator/

**Answer:**
Correct Answer: **Launch EC2 instances into multiple regions behind an NLB and use AWS Global Accelerator**

---

## Question 196

**Q:** What is the most cost-effective solution to these requirements?

**Options:**
- (A) Create an Amazon CloudFront distribution and set the price class to use all Edge Locations for best performance.
- (B) Create an Amazon CloudFront distribution that uses origins in U.S, Canada and Mexico.
- (C) Create an Amazon CloudFront distribution and use Lambda@Edge to run the website's data processing closer to the users.
- (D) Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.
- (E) With Amazon CloudFront you can set the price class to determine where in the world the content will be cached. One of the price classes is “U.S, Canada and Mexico” and this is where the company’s users are located. Choosing this price class will result in lower costs and better performance for the company’s users.
- (F)  is the correct answer.
- (G)  is incorrect. This will be more expensive as it will cache content in Edge Locations all over the world.
- (H)  is incorrect. The origin can be in one place, there’s no need to add origins in different Regions. The price class should be used to limit the caching of the content to reduce cost.
- (I)  is incorrect. Lambda@Edge will not assist in this situation as there is no data processing required, the content from the static website must simply be cached at an edge location.
- (J) References:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Networking & Content Delivery
- () A new application is to be published in multiple regions around the world. The Architect needs to ensure only 2 IP addresses need to be whitelisted. The solution should intelligently route traffic for lowest latency and provide fast regional failover.
- () How can this be achieved?
- () Launch EC2 instances into multiple regions behind an ALB and use Amazon CloudFront with a pair of static IP addresses
- () Launch EC2 instances into multiple regions behind an ALB and use a Route 53 failover routing policy
- () Launch EC2 instances into multiple regions behind an NLB with a static IP address
- () Launch EC2 instances into multiple regions behind an NLB and use AWS Global Accelerator
- () AWS Global Accelerator uses the vast, congestion-free AWS global network to route TCP and UDP traffic to a healthy application endpoint in the closest AWS Region to the user.
- () This means it will intelligently route traffic to the closest point of presence (reducing latency). Seamless failover is ensured as AWS Global Accelerator uses anycast IP address which means the IP does not change when failing over between regions so there are no issues with client caches having incorrect entries that need to expire.
- () This is the only solution that provides deterministic failover.
- ()  is incorrect. An NLB with a static IP is a workable solution as you could configure a primary and secondary address in applications. However, this solution does not intelligently route traffic for lowest latency.
- ()  is incorrect. A Route 53 failover routing policy uses a primary and standby configuration. Therefore, it sends all traffic to the primary until it fails a health check at which time it sends traffic to the secondary. This solution does not intelligently route traffic for lowest latency.
- ()  is incorrect. Amazon CloudFront cannot be configured with “a pair of static IP addresses”.
- () https://aws.amazon.com/global-accelerator/
- () https://aws.amazon.com/global-accelerator/faqs/
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- () https://digitalcloud.training/aws-global-accelerator/
- () A company has two accounts for perform testing and each account has a single VPC: VPC-TEST1 and VPC-TEST2. The operations team require a method of securely copying files between Amazon EC2 instances in these VPCs. The connectivity should not have any single points of failure or bandwidth constraints.
- () Which solution should a Solutions Architect recommend?
- () Attach a Direct Connect gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
- **() Create a VPC peering connection between VPC-TEST1 and VPC-TEST2.** [CORRECT]
- () Attach a virtual private gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
- () Create a VPC gateway endpoint for each EC2 instance and update route tables.
- () A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network.
- () You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. The VPCs can be in different regions (also known as an inter-region VPC peering connection).
- ()  is incorrect. You cannot create VPC gateway endpoints for Amazon EC2 instances. These are used with DynamoDB and S3 only.
- ()  is incorrect. You cannot create an AWS Managed VPN connection between two VPCs.

**Answer:**
Correct Answer: **Create a VPC peering connection between VPC-TEST1 and VPC-TEST2.**

---

## Question 197

**Q:** How can this be achieved?

**Options:**
- (A) Launch EC2 instances into multiple regions behind an ALB and use Amazon CloudFront with a pair of static IP addresses
- (B) Launch EC2 instances into multiple regions behind an ALB and use a Route 53 failover routing policy
- (C) Launch EC2 instances into multiple regions behind an NLB with a static IP address
- (D) Launch EC2 instances into multiple regions behind an NLB and use AWS Global Accelerator
- (E) AWS Global Accelerator uses the vast, congestion-free AWS global network to route TCP and UDP traffic to a healthy application endpoint in the closest AWS Region to the user.
- (F) This means it will intelligently route traffic to the closest point of presence (reducing latency). Seamless failover is ensured as AWS Global Accelerator uses anycast IP address which means the IP does not change when failing over between regions so there are no issues with client caches having incorrect entries that need to expire.
- (G) This is the only solution that provides deterministic failover.
- (H)  is the correct answer.
- (I)  is incorrect. An NLB with a static IP is a workable solution as you could configure a primary and secondary address in applications. However, this solution does not intelligently route traffic for lowest latency.
- (J)  is incorrect. A Route 53 failover routing policy uses a primary and standby configuration. Therefore, it sends all traffic to the primary until it fails a health check at which time it sends traffic to the secondary. This solution does not intelligently route traffic for lowest latency.
- ()  is incorrect. Amazon CloudFront cannot be configured with “a pair of static IP addresses”.
- () References:
- () https://aws.amazon.com/global-accelerator/
- () https://aws.amazon.com/global-accelerator/faqs/
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-global-accelerator/
- () AWS Networking & Content Delivery
- () A company has two accounts for perform testing and each account has a single VPC: VPC-TEST1 and VPC-TEST2. The operations team require a method of securely copying files between Amazon EC2 instances in these VPCs. The connectivity should not have any single points of failure or bandwidth constraints.
- () Which solution should a Solutions Architect recommend?
- () Attach a Direct Connect gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
- () Create a VPC peering connection between VPC-TEST1 and VPC-TEST2.
- () Attach a virtual private gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
- () Create a VPC gateway endpoint for each EC2 instance and update route tables.
- () A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network.
- () You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. The VPCs can be in different regions (also known as an inter-region VPC peering connection).
- ()  is incorrect. You cannot create VPC gateway endpoints for Amazon EC2 instances. These are used with DynamoDB and S3 only.
- ()  is incorrect. You cannot create an AWS Managed VPN connection between two VPCs.
- ()  is incorrect. Direct Connect gateway is used to connect a Direct Connect connection to multiple VPCs, it is not useful in this scenario as there is no Direct Connect connection.
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () https://digitalcloud.training/amazon-vpc/
- () A company runs an application in an on-premises data center that collects environmental data from production machinery. The data consists of JSON files stored on network attached storage (NAS) and around 5 TB of data is collected each day. The company must upload this data to Amazon S3 where it can be processed by an analytics application. The data must be transferred securely.
- () Which solution offers the MOST reliable and time-efficient data transfer?
- () AWS Database Migration Service over the Internet.
- () Amazon S3 Transfer Acceleration over the Internet.
- **() AWS DataSync over AWS Direct Connect.** [CORRECT]
- () Multiple AWS Snowcone devices.
- () The most reliable and time-efficient solution that keeps the data secure is to use AWS DataSync and synchronize the data from the NAS device directly to Amazon S3. This should take place over an AWS Direct Connect connection to ensure reliability, speed, and security.
- () AWS DataSync can copy data between Network File System (NFS) shares, Server Message Block (SMB) shares, self-managed object storage, AWS Snowcone, Amazon Simple Storage Service (Amazon S3) buckets, Amazon Elastic File System (Amazon EFS) file systems, and Amazon FSx for Windows File Server file systems.
- ()  is incorrect. DMS is for migrating databases, not files.

**Answer:**
Correct Answer: **AWS DataSync over AWS Direct Connect.**

---

## Question 198

**Q:** Which solution should a Solutions Architect recommend?

**Options:**
- (A) Attach a Direct Connect gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
- (B) Create a VPC peering connection between VPC-TEST1 and VPC-TEST2.
- (C) Attach a virtual private gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
- (D) Create a VPC gateway endpoint for each EC2 instance and update route tables.
- (E) A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network.
- (F) You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. The VPCs can be in different regions (also known as an inter-region VPC peering connection).
- (G)  is the correct answer.
- (H)  is incorrect. You cannot create VPC gateway endpoints for Amazon EC2 instances. These are used with DynamoDB and S3 only.
- (I)  is incorrect. You cannot create an AWS Managed VPN connection between two VPCs.
- (J)  is incorrect. Direct Connect gateway is used to connect a Direct Connect connection to multiple VPCs, it is not useful in this scenario as there is no Direct Connect connection.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-vpc/
- () AWS Networking & Content Delivery
- () A company runs an application in an on-premises data center that collects environmental data from production machinery. The data consists of JSON files stored on network attached storage (NAS) and around 5 TB of data is collected each day. The company must upload this data to Amazon S3 where it can be processed by an analytics application. The data must be transferred securely.
- () Which solution offers the MOST reliable and time-efficient data transfer?
- () AWS Database Migration Service over the Internet.
- () Amazon S3 Transfer Acceleration over the Internet.
- () AWS DataSync over AWS Direct Connect.
- () Multiple AWS Snowcone devices.
- () The most reliable and time-efficient solution that keeps the data secure is to use AWS DataSync and synchronize the data from the NAS device directly to Amazon S3. This should take place over an AWS Direct Connect connection to ensure reliability, speed, and security.
- () AWS DataSync can copy data between Network File System (NFS) shares, Server Message Block (SMB) shares, self-managed object storage, AWS Snowcone, Amazon Simple Storage Service (Amazon S3) buckets, Amazon Elastic File System (Amazon EFS) file systems, and Amazon FSx for Windows File Server file systems.
- ()  is incorrect. DMS is for migrating databases, not files.
- ()  is incorrect. The Internet does not offer the reliability, speed or performance that this company requires.
- ()  is incorrect. This is not a time-efficient approach as it can take time to ship these devices in both directions.
- () https://aws.amazon.com/datasync/
- () https://digitalcloud.training/aws-migration-services/
- () AWS Migration & Transfer
- () A company runs a critical data analysis job every Friday evening. The job processes large datasets and requires at least 2 hours to complete without interruptions. The job is stateful and needs reliable compute resources. The company wants to minimize operational overhead while ensuring the job runs as scheduled.
- () Which solution will meet these requirements?
- () Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis.
- **() Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler.** [CORRECT]
- () Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule.
- () Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution.
- () Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler: This is the best option because AWS Fargate provides a serverless compute engine for containers, ensuring no interruptions. EventBridge Scheduler offers an easy way to schedule tasks without requiring manual intervention.
- () Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule: This is incorrect because Lambda functions are not suited for stateful, long-running jobs. Lambda has a maximum execution duration of 15 minutes.
- () Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis: While this solution avoids interruptions, it requires managing and maintaining the EC2 instance, which increases operational overhead.
- () Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution: Spot Instances are not suitable for stateful jobs because they can be interrupted. This approach also introduces additional complexity with EMR setup and management.
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/scheduling_tasks.html
- () https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-run-lambda-schedule.html
- () https://digitalcloud.training/amazon-ecs-and-eks/

**Answer:**
Correct Answer: **Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler.**

---

## Question 199

**Q:** Which solution offers the MOST reliable and time-efficient data transfer?

**Options:**
- (A) AWS Database Migration Service over the Internet.
- (B) Amazon S3 Transfer Acceleration over the Internet.
- (C) AWS DataSync over AWS Direct Connect.
- (D) Multiple AWS Snowcone devices.
- (E) The most reliable and time-efficient solution that keeps the data secure is to use AWS DataSync and synchronize the data from the NAS device directly to Amazon S3. This should take place over an AWS Direct Connect connection to ensure reliability, speed, and security.
- (F) AWS DataSync can copy data between Network File System (NFS) shares, Server Message Block (SMB) shares, self-managed object storage, AWS Snowcone, Amazon Simple Storage Service (Amazon S3) buckets, Amazon Elastic File System (Amazon EFS) file systems, and Amazon FSx for Windows File Server file systems.
- (G)  is the correct answer.
- (H)  is incorrect. DMS is for migrating databases, not files.
- (I)  is incorrect. The Internet does not offer the reliability, speed or performance that this company requires.
- (J)  is incorrect. This is not a time-efficient approach as it can take time to ship these devices in both directions.
- () References:
- () https://aws.amazon.com/datasync/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-migration-services/
- () AWS Migration & Transfer
- () A company runs a critical data analysis job every Friday evening. The job processes large datasets and requires at least 2 hours to complete without interruptions. The job is stateful and needs reliable compute resources. The company wants to minimize operational overhead while ensuring the job runs as scheduled.
- () Which solution will meet these requirements?
- () Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis.
- () Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler.
- () Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule.
- () Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution.
- () Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler: This is the best option because AWS Fargate provides a serverless compute engine for containers, ensuring no interruptions. EventBridge Scheduler offers an easy way to schedule tasks without requiring manual intervention.
- () Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule: This is incorrect because Lambda functions are not suited for stateful, long-running jobs. Lambda has a maximum execution duration of 15 minutes.
- () Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis: While this solution avoids interruptions, it requires managing and maintaining the EC2 instance, which increases operational overhead.
- () Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution: Spot Instances are not suitable for stateful jobs because they can be interrupted. This approach also introduces additional complexity with EMR setup and management.
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/scheduling_tasks.html
- () https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-run-lambda-schedule.html
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Compute
- () A Microsoft Windows file server farm uses Distributed File System Replication (DFSR) to synchronize data in an on-premises environment. The infrastructure is being migrated to the AWS Cloud.
- () Which service should the solutions architect use to replace the file server farm?
- () Amazon EFS
- () AWS Storage Gateway
- () Amazon EBS
- **() Amazon FSx** [CORRECT]
- () Amazon FSx for Windows file server supports DFS namespaces and DFS replication. This is the best solution for replacing the on-premises infrastructure. Note the limitations for deployment:
- ()  is incorrect. You cannot replace a Windows file server farm with EFS as it uses a completely different protocol.
- ()  is incorrect. Amazon EBS provides block-based volumes that are attached to EC2 instances. It cannot be used for replacing a shared Windows file server farm using DFSR.
- ()  is incorrect. This service is used for providing cloud storage solutions for on-premises servers. In this case the infrastructure is being migrated into the AWS Cloud.
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html
- () https://digitalcloud.training/amazon-fsx/

**Answer:**
Correct Answer: **Amazon FSx**

---

## Question 200

**Q:** Which solution will meet these requirements?

**Options:**
- (A) Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis.
- (B) Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler.
- (C) Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule.
- (D) Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution.
- (E) Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler: This is the best option because AWS Fargate provides a serverless compute engine for containers, ensuring no interruptions. EventBridge Scheduler offers an easy way to schedule tasks without requiring manual intervention.
- (F) Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule: This is incorrect because Lambda functions are not suited for stateful, long-running jobs. Lambda has a maximum execution duration of 15 minutes.
- (G) Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis: While this solution avoids interruptions, it requires managing and maintaining the EC2 instance, which increases operational overhead.
- (H) Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution: Spot Instances are not suitable for stateful jobs because they can be interrupted. This approach also introduces additional complexity with EMR setup and management.
- (I) References:
- (J) https://docs.aws.amazon.com/AmazonECS/latest/developerguide/scheduling_tasks.html
- () https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-run-lambda-schedule.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Compute
- () A Microsoft Windows file server farm uses Distributed File System Replication (DFSR) to synchronize data in an on-premises environment. The infrastructure is being migrated to the AWS Cloud.
- () Which service should the solutions architect use to replace the file server farm?
- () Amazon EFS
- () AWS Storage Gateway
- () Amazon EBS
- () Amazon FSx
- () Amazon FSx for Windows file server supports DFS namespaces and DFS replication. This is the best solution for replacing the on-premises infrastructure. Note the limitations for deployment:
- ()  is the correct answer.
- ()  is incorrect. You cannot replace a Windows file server farm with EFS as it uses a completely different protocol.
- ()  is incorrect. Amazon EBS provides block-based volumes that are attached to EC2 instances. It cannot be used for replacing a shared Windows file server farm using DFSR.
- ()  is incorrect. This service is used for providing cloud storage solutions for on-premises servers. In this case the infrastructure is being migrated into the AWS Cloud.
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html
- () https://digitalcloud.training/amazon-fsx/
- () AWS Storage
- () A retail company with many stores and warehouses is implementing IoT sensors to gather monitoring data from devices in each location. The data will be sent to AWS in real time. A solutions architect must provide a solution for ensuring events are received in order for each device and ensure that data is saved for future processing.
- () Which solution would be MOST efficient?
- () Use an Amazon SQS FIFO queue for real-time events with one queue for each device. Trigger an AWS Lambda function for the SQS queue to save data to Amazon EFS
- () Use Amazon Kinesis Data Streams for real-time events with a shard for each device. Use Amazon Kinesis Data Firehose to save data to Amazon EBS
- **() Use Amazon Kinesis Data Streams for real-time events with a partition key for each device. Use Amazon Kinesis Data Firehose to save data to Amazon S3** [CORRECT]
- () Use an Amazon SQS standard queue for real-time events with one queue for each device. Trigger an AWS Lambda function from the SQS queue to save data to Amazon S3
- () Amazon Kinesis Data Streams collect and process data in real time. A Kinesis data stream is a set of shards. Each shard has a sequence of data records. Each data record has a sequence number that is assigned by Kinesis Data Streams. A shard is a uniquely identified sequence of data records in a stream.
- () A partition key is used to group data by shard within a stream. Kinesis Data Streams segregates the data records belonging to a stream into multiple shards. It uses the partition key that is associated with each data record to determine which shard a given data record belongs to.
- () For this scenario, the solutions architect can use a partition key for each device. This will ensure the records for that device are grouped by shard and the shard will ensure ordering. Amazon S3 is a valid destination for saving the data records.
- ()  is incorrect as you cannot save data to EBS from Kinesis.
- ()  is incorrect as SQS is not the most efficient service for streaming, real time data.
- () https://docs.aws.amazon.com/streams/latest/dev/key-concepts.html

**Answer:**
Correct Answer: **Use Amazon Kinesis Data Streams for real-time events with a partition key for each device. Use Amazon Kinesis Data Firehose to save data to Amazon S3**

---

## Question 201

**Q:** Which service should the solutions architect use to replace the file server farm?

**Options:**
- (A) Amazon EFS
- (B) AWS Storage Gateway
- (C) Amazon EBS
- (D) Amazon FSx
- (E) Amazon FSx for Windows file server supports DFS namespaces and DFS replication. This is the best solution for replacing the on-premises infrastructure. Note the limitations for deployment:
- (F)  is the correct answer.
- (G)  is incorrect. You cannot replace a Windows file server farm with EFS as it uses a completely different protocol.
- (H)  is incorrect. Amazon EBS provides block-based volumes that are attached to EC2 instances. It cannot be used for replacing a shared Windows file server farm using DFSR.
- (I)  is incorrect. This service is used for providing cloud storage solutions for on-premises servers. In this case the infrastructure is being migrated into the AWS Cloud.
- (J) References:
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-fsx/
- () AWS Storage
- () A retail company with many stores and warehouses is implementing IoT sensors to gather monitoring data from devices in each location. The data will be sent to AWS in real time. A solutions architect must provide a solution for ensuring events are received in order for each device and ensure that data is saved for future processing.
- () Which solution would be MOST efficient?
- () Use an Amazon SQS FIFO queue for real-time events with one queue for each device. Trigger an AWS Lambda function for the SQS queue to save data to Amazon EFS
- () Use Amazon Kinesis Data Streams for real-time events with a shard for each device. Use Amazon Kinesis Data Firehose to save data to Amazon EBS
- () Use Amazon Kinesis Data Streams for real-time events with a partition key for each device. Use Amazon Kinesis Data Firehose to save data to Amazon S3
- () Use an Amazon SQS standard queue for real-time events with one queue for each device. Trigger an AWS Lambda function from the SQS queue to save data to Amazon S3
- () Amazon Kinesis Data Streams collect and process data in real time. A Kinesis data stream is a set of shards. Each shard has a sequence of data records. Each data record has a sequence number that is assigned by Kinesis Data Streams. A shard is a uniquely identified sequence of data records in a stream.
- () A partition key is used to group data by shard within a stream. Kinesis Data Streams segregates the data records belonging to a stream into multiple shards. It uses the partition key that is associated with each data record to determine which shard a given data record belongs to.
- () For this scenario, the solutions architect can use a partition key for each device. This will ensure the records for that device are grouped by shard and the shard will ensure ordering. Amazon S3 is a valid destination for saving the data records.
- ()  is incorrect as you cannot save data to EBS from Kinesis.
- ()  is incorrect as SQS is not the most efficient service for streaming, real time data.
- () https://docs.aws.amazon.com/streams/latest/dev/key-concepts.html
- () https://digitalcloud.training/amazon-kinesis/
- () AWS Analytics
- () Which solution meets these requirements and is the MOST operationally efficient?
- () Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application.
- **() Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.** [CORRECT]
- () Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application.
- () Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively.
- () Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS eliminates the complexity and overhead associated with managing and operating message-oriented middleware and empowers developers to focus on differentiating work.
- () Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages” is the correct answer (as explained above.)
- () Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS.
- () Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS
- () Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application” is incorrect as Amazon SNS is not a queuing service, but a pub-sub one to many notification service and cannot be used as a queue.
- () https://aws.amazon.com/sqs/

**Answer:**
Correct Answer: **Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.**

---

## Question 202

**Q:** Which solution would be MOST efficient?

**Options:**
- (A) Use an Amazon SQS FIFO queue for real-time events with one queue for each device. Trigger an AWS Lambda function for the SQS queue to save data to Amazon EFS
- (B) Use Amazon Kinesis Data Streams for real-time events with a shard for each device. Use Amazon Kinesis Data Firehose to save data to Amazon EBS
- (C) Use Amazon Kinesis Data Streams for real-time events with a partition key for each device. Use Amazon Kinesis Data Firehose to save data to Amazon S3
- (D) Use an Amazon SQS standard queue for real-time events with one queue for each device. Trigger an AWS Lambda function from the SQS queue to save data to Amazon S3
- (E) Amazon Kinesis Data Streams collect and process data in real time. A Kinesis data stream is a set of shards. Each shard has a sequence of data records. Each data record has a sequence number that is assigned by Kinesis Data Streams. A shard is a uniquely identified sequence of data records in a stream.
- (F) A partition key is used to group data by shard within a stream. Kinesis Data Streams segregates the data records belonging to a stream into multiple shards. It uses the partition key that is associated with each data record to determine which shard a given data record belongs to.
- (G) For this scenario, the solutions architect can use a partition key for each device. This will ensure the records for that device are grouped by shard and the shard will ensure ordering. Amazon S3 is a valid destination for saving the data records.
- (H)  is the correct answer.
- (I)  is incorrect as you cannot save data to EBS from Kinesis.
- (J)  is incorrect as SQS is not the most efficient service for streaming, real time data.
- () References:
- () https://docs.aws.amazon.com/streams/latest/dev/key-concepts.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-kinesis/
- () AWS Analytics
- () Which solution meets these requirements and is the MOST operationally efficient?
- () Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application.
- () Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.
- () Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application.
- () Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively.
- () Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS eliminates the complexity and overhead associated with managing and operating message-oriented middleware and empowers developers to focus on differentiating work.
- () Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages” is the correct answer (as explained above.)
- () Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS.
- () Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS
- () Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application” is incorrect as Amazon SNS is not a queuing service, but a pub-sub one to many notification service and cannot be used as a queue.
- () https://aws.amazon.com/sqs/
- () https://digitalcloud.training/aws-application-integration-services/
- () AWS Application Integration
- () A company is investigating methods to reduce the expenses associated with on-premises backup infrastructure. The Solutions Architect wants to reduce costs by eliminating the use of physical backup tapes. It is a requirement that existing backup applications and workflows should continue to function.
- () What should the Solutions Architect recommend?
- **() Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).** [CORRECT]
- () Connect the backup applications to an AWS Storage Gateway using the iSCSI protocol.
- () Create an Amazon EFS file system and connect the backup applications using the iSCSI protocol.
- () Create an Amazon EFS file system and connect the backup applications using the NFS protocol.
- () The AWS Storage Gateway Tape Gateway enables you to replace using physical tapes on premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway emulates physical tape libraries, removes the cost and complexity of managing physical tape infrastructure, and provides more durability than physical tapes.
- ()  is incorrect. The NFS protocol is used by AWS Storage Gateway File Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
- ()  is incorrect. The iSCSI protocol is used by AWS Storage Gateway Volume Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
- () https://aws.amazon.com/storagegateway/vtl/

**Answer:**
Correct Answer: **Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).**

---

## Question 203

**Q:** Which solution meets these requirements and is the MOST operationally efficient?

**Options:**
- (A) Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application.
- (B) Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.
- (C) Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application.
- (D) Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively.
- (E) Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS eliminates the complexity and overhead associated with managing and operating message-oriented middleware and empowers developers to focus on differentiating work.
- (F) Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages” is the correct answer (as explained above.)
- (G) Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS.
- (H) Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS
- (I) Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application” is incorrect as Amazon SNS is not a queuing service, but a pub-sub one to many notification service and cannot be used as a queue.
- (J) References:
- () https://aws.amazon.com/sqs/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-application-integration-services/
- () AWS Application Integration
- () A company is investigating methods to reduce the expenses associated with on-premises backup infrastructure. The Solutions Architect wants to reduce costs by eliminating the use of physical backup tapes. It is a requirement that existing backup applications and workflows should continue to function.
- () What should the Solutions Architect recommend?
- () Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).
- () Connect the backup applications to an AWS Storage Gateway using the iSCSI protocol.
- () Create an Amazon EFS file system and connect the backup applications using the iSCSI protocol.
- () Create an Amazon EFS file system and connect the backup applications using the NFS protocol.
- () The AWS Storage Gateway Tape Gateway enables you to replace using physical tapes on premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway emulates physical tape libraries, removes the cost and complexity of managing physical tape infrastructure, and provides more durability than physical tapes.
- ()  is the correct answer.
- ()  is incorrect. The NFS protocol is used by AWS Storage Gateway File Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
- ()  is incorrect. The iSCSI protocol is used by AWS Storage Gateway Volume Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
- () https://aws.amazon.com/storagegateway/vtl/
- () https://digitalcloud.training/aws-storage-gateway/
- () AWS Storage
- () A company is launching a new internal platform for managing multiple independent projects. Each project will require its own dedicated AWS account for isolation. The company needs a solution that automates account creation, applies mandatory security guardrails, and centrally manages shared networking resources such as VPNs and subnets for the accounts. The solution must minimize manual effort and ensure compliance with security standards.
- () Which solution will meet these requirements with the LEAST operational overhead?
- () Use AWS Organizations to create accounts for each project. Deploy a shared VPC in a centralized account. Configure AWS Firewall Manager to enforce security controls. Manually configure routing for project account traffic through the shared VPC.
- **() Use AWS Control Tower to automate account provisioning. Create a dedicated networking account with a centralized VPC. Use AWS Resource Access Manager (AWS RAM) to share subnets with project accounts. Enforce security guardrails by using AWS Control Tower guardrails.** [CORRECT]
- () Use AWS Control Tower to set up accounts with pre-configured VPCs in each project account. Connect these VPCs to a central networking account through a transit gateway. Enforce security controls with AWS Config.
- () Use AWS Organizations to create project accounts manually. Deploy a VPC in a centralized networking account. Use AWS RAM to share subnets. Manually configure security policies in each account.
- () Use AWS Control Tower to automate account provisioning. Create a dedicated networking account with a centralized VPC. Use AWS Resource Access Manager (AWS RAM) to share subnets with project accounts. Enforce security guardrails by using AWS Control Tower guardrails: This is correct because AWS Control Tower simplifies account setup with built-in security guardrails. It minimizes operational overhead by automating VPC sharing and guardrail enforcement through AWS RAM.
- () Use AWS Organizations to create project accounts manually. Deploy a VPC in a centralized networking account. Use AWS RAM to share subnets. Manually configure security policies in each account: This is incorrect because manual account setup and security configuration increase operational overhead.
- () Use AWS Control Tower to set up accounts with pre-configured VPCs in each project account. Connect these VPCs to a central networking account through a transit gateway. Enforce security controls with AWS Config: This is incorrect because configuring a transit gateway and enforcing controls through AWS Config introduces more complexity than required for this use case.
- () Use AWS Organizations to create accounts for each project. Deploy a shared VPC in a centralized account. Configure AWS Firewall Manager to enforce security controls. Manually configure routing for project account traffic through the shared VPC: This is incorrect because it requires more manual effort to configure routing and lacks automation in account creation and security enforcement.
- () https://docs.aws.amazon.com/controltower/latest/userguide/
- () https://docs.aws.amazon.com/ram/latest/userguide/
- () AWS Management & Governance

**Answer:**
Correct Answer: **Use AWS Control Tower to automate account provisioning. Create a dedicated networking account with a centralized VPC. Use AWS Resource Access Manager (AWS RAM) to share subnets with project accounts. Enforce security guardrails by using AWS Control Tower guardrails.**

---

## Question 204

**Q:** What should the Solutions Architect recommend?

**Options:**
- (A) Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).
- (B) Connect the backup applications to an AWS Storage Gateway using the iSCSI protocol.
- (C) Create an Amazon EFS file system and connect the backup applications using the iSCSI protocol.
- (D) Create an Amazon EFS file system and connect the backup applications using the NFS protocol.
- (E) The AWS Storage Gateway Tape Gateway enables you to replace using physical tapes on premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway emulates physical tape libraries, removes the cost and complexity of managing physical tape infrastructure, and provides more durability than physical tapes.
- (F)  is the correct answer.
- (G)  is incorrect. The NFS protocol is used by AWS Storage Gateway File Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
- (H)  is incorrect. The iSCSI protocol is used by AWS Storage Gateway Volume Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
- (I) References:
- (J) https://aws.amazon.com/storagegateway/vtl/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-storage-gateway/
- () AWS Storage
- () A company is launching a new internal platform for managing multiple independent projects. Each project will require its own dedicated AWS account for isolation. The company needs a solution that automates account creation, applies mandatory security guardrails, and centrally manages shared networking resources such as VPNs and subnets for the accounts. The solution must minimize manual effort and ensure compliance with security standards.
- () Which solution will meet these requirements with the LEAST operational overhead?
- () Use AWS Organizations to create accounts for each project. Deploy a shared VPC in a centralized account. Configure AWS Firewall Manager to enforce security controls. Manually configure routing for project account traffic through the shared VPC.
- () Use AWS Control Tower to automate account provisioning. Create a dedicated networking account with a centralized VPC. Use AWS Resource Access Manager (AWS RAM) to share subnets with project accounts. Enforce security guardrails by using AWS Control Tower guardrails.
- () Use AWS Control Tower to set up accounts with pre-configured VPCs in each project account. Connect these VPCs to a central networking account through a transit gateway. Enforce security controls with AWS Config.
- () Use AWS Organizations to create project accounts manually. Deploy a VPC in a centralized networking account. Use AWS RAM to share subnets. Manually configure security policies in each account.
- () Use AWS Control Tower to automate account provisioning. Create a dedicated networking account with a centralized VPC. Use AWS Resource Access Manager (AWS RAM) to share subnets with project accounts. Enforce security guardrails by using AWS Control Tower guardrails: This is correct because AWS Control Tower simplifies account setup with built-in security guardrails. It minimizes operational overhead by automating VPC sharing and guardrail enforcement through AWS RAM.
- () Use AWS Organizations to create project accounts manually. Deploy a VPC in a centralized networking account. Use AWS RAM to share subnets. Manually configure security policies in each account: This is incorrect because manual account setup and security configuration increase operational overhead.
- () Use AWS Control Tower to set up accounts with pre-configured VPCs in each project account. Connect these VPCs to a central networking account through a transit gateway. Enforce security controls with AWS Config: This is incorrect because configuring a transit gateway and enforcing controls through AWS Config introduces more complexity than required for this use case.
- () Use AWS Organizations to create accounts for each project. Deploy a shared VPC in a centralized account. Configure AWS Firewall Manager to enforce security controls. Manually configure routing for project account traffic through the shared VPC: This is incorrect because it requires more manual effort to configure routing and lacks automation in account creation and security enforcement.
- () https://docs.aws.amazon.com/controltower/latest/userguide/
- () https://docs.aws.amazon.com/ram/latest/userguide/
- () AWS Management & Governance
- () A company needs to connect its on-premises data center network to a new virtual private cloud (VPC). There is a symmetrical internet connection of 100 Mbps in the data center network. The data transfer rate for an on-premises application is multiple gigabytes per day. Processing will be done using an Amazon Kinesis Data Firehose stream.
- () What should a solutions architect recommend for maximum performance?
- () Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection.
- () Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection.
- **() Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.** [CORRECT]
- () Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary.
- () Explanation:
- () Using AWS PrivateLink to create an interface endpoint will allow your traffic to traverse the AWS Global Backbone to allow maximum performance and security. Also by using an AWS Direct Connect cable you can ensure you have a dedicated cable to provide maximum performance and low latency to and from AWS.
- () Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint” is the correct answer (as explained above.)
- () Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection” is incorrect also because VPC peering connections can only exist between two VPCs within the AWS Cloud.
- () Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary” is incorrect. AWS Snowball Edge is designed to be more of a one-time migration service which you physically receive from AWS, and then ship it into an AWS Region of your choice.
- () Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection” is incorrect. This is a functional solution; however a physical connection would provide a much more reliable and performant solution.
- () https://aws.amazon.com/privatelink/
- () https://digitalcloud.training/amazon-vpc/

**Answer:**
Correct Answer: **Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.**

---

## Question 205

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**Options:**
- (A) Use AWS Organizations to create accounts for each project. Deploy a shared VPC in a centralized account. Configure AWS Firewall Manager to enforce security controls. Manually configure routing for project account traffic through the shared VPC.
- (B) Use AWS Control Tower to automate account provisioning. Create a dedicated networking account with a centralized VPC. Use AWS Resource Access Manager (AWS RAM) to share subnets with project accounts. Enforce security guardrails by using AWS Control Tower guardrails.
- (C) Use AWS Control Tower to set up accounts with pre-configured VPCs in each project account. Connect these VPCs to a central networking account through a transit gateway. Enforce security controls with AWS Config.
- (D) Use AWS Organizations to create project accounts manually. Deploy a VPC in a centralized networking account. Use AWS RAM to share subnets. Manually configure security policies in each account.
- (E) Use AWS Control Tower to automate account provisioning. Create a dedicated networking account with a centralized VPC. Use AWS Resource Access Manager (AWS RAM) to share subnets with project accounts. Enforce security guardrails by using AWS Control Tower guardrails: This is correct because AWS Control Tower simplifies account setup with built-in security guardrails. It minimizes operational overhead by automating VPC sharing and guardrail enforcement through AWS RAM.
- (F) Use AWS Organizations to create project accounts manually. Deploy a VPC in a centralized networking account. Use AWS RAM to share subnets. Manually configure security policies in each account: This is incorrect because manual account setup and security configuration increase operational overhead.
- (G) Use AWS Control Tower to set up accounts with pre-configured VPCs in each project account. Connect these VPCs to a central networking account through a transit gateway. Enforce security controls with AWS Config: This is incorrect because configuring a transit gateway and enforcing controls through AWS Config introduces more complexity than required for this use case.
- (H) Use AWS Organizations to create accounts for each project. Deploy a shared VPC in a centralized account. Configure AWS Firewall Manager to enforce security controls. Manually configure routing for project account traffic through the shared VPC: This is incorrect because it requires more manual effort to configure routing and lacks automation in account creation and security enforcement.
- (I) References:
- (J) https://docs.aws.amazon.com/controltower/latest/userguide/
- () https://docs.aws.amazon.com/ram/latest/userguide/
- () AWS Management & Governance
- () A company needs to connect its on-premises data center network to a new virtual private cloud (VPC). There is a symmetrical internet connection of 100 Mbps in the data center network. The data transfer rate for an on-premises application is multiple gigabytes per day. Processing will be done using an Amazon Kinesis Data Firehose stream.
- () What should a solutions architect recommend for maximum performance?
- () Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection.
- () Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection.
- () Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.
- () Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary.
- () Explanation:
- () Using AWS PrivateLink to create an interface endpoint will allow your traffic to traverse the AWS Global Backbone to allow maximum performance and security. Also by using an AWS Direct Connect cable you can ensure you have a dedicated cable to provide maximum performance and low latency to and from AWS.
- () Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint” is the correct answer (as explained above.)
- () Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection” is incorrect also because VPC peering connections can only exist between two VPCs within the AWS Cloud.
- () Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary” is incorrect. AWS Snowball Edge is designed to be more of a one-time migration service which you physically receive from AWS, and then ship it into an AWS Region of your choice.
- () Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection” is incorrect. This is a functional solution; however a physical connection would provide a much more reliable and performant solution.
- () https://aws.amazon.com/privatelink/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-vpc/
- () AWS Networking & Content Delivery
- () A persistent database must be migrated from an on-premises server to an Amazon EC2 instances. The database requires 64,000 IOPS and, if possible, should be stored on a single Amazon EBS volume.
- () Which solution should a Solutions Architect recommend?
- () Create an Amazon EC2 instance with four Amazon EBS General Purpose SSD (gp2) volumes attached. Max out the IOPS on each volume and use a RAID 0 stripe set.
- **() Create a Nitro-based Amazon EC2 instance with an Amazon EBS Provisioned IOPS SSD (i01) volume attached. Provision 64,000 IOPS for the volume.** [CORRECT]
- () Use an instance from the I3 I/O optimized family and leverage instance store storage to achieve the IOPS requirement.
- () Create an Amazon EC2 instance with two Amazon EBS Provisioned IOPS SSD (i01) volumes attached. Provision 32,000 IOPS per volume and create a logical volume using the OS that aggregates the capacity.
- () Amazon EC2 Nitro-based systems are not required for this solution but do offer advantages in performance that will help to maximize the usage of the EBS volume. For the data storage volume an i01 volume can support up to 64,000 IOPS so a single volume with sufficient capacity (50 IOPS per GiB) can be deliver the requirements.
- () The current list of EBS volume types is in the table below:
- ()  is the correct answer.
- ()  is incorrect.
- ()  is incorrect. This is not a good use case for gp2 volumes. It is much better to use io1 which also meets the requirement of having a single volume with 64,000 IOPS.
- ()  is incorrect. There is no need to create two volumes and aggregate capacity through the OS, the Solutions Architect can simply create a single volume with 64,000 IOPS.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () https://digitalcloud.training/amazon-ec2/

**Answer:**
Correct Answer: **Create a Nitro-based Amazon EC2 instance with an Amazon EBS Provisioned IOPS SSD (i01) volume attached. Provision 64,000 IOPS for the volume.**

---

## Question 206

**Q:** What should a solutions architect recommend for maximum performance?

**Options:**
- (A) Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection.
- (B) Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection.
- (C) Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.
- (D) Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary.
- (E) Explanation:
- (F) Using AWS PrivateLink to create an interface endpoint will allow your traffic to traverse the AWS Global Backbone to allow maximum performance and security. Also by using an AWS Direct Connect cable you can ensure you have a dedicated cable to provide maximum performance and low latency to and from AWS.
- (G) Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint” is the correct answer (as explained above.)
- (H) Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection” is incorrect also because VPC peering connections can only exist between two VPCs within the AWS Cloud.
- (I) Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary” is incorrect. AWS Snowball Edge is designed to be more of a one-time migration service which you physically receive from AWS, and then ship it into an AWS Region of your choice.
- (J) Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection” is incorrect. This is a functional solution; however a physical connection would provide a much more reliable and performant solution.
- () References:
- () https://aws.amazon.com/privatelink/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-vpc/
- () AWS Networking & Content Delivery
- () A persistent database must be migrated from an on-premises server to an Amazon EC2 instances. The database requires 64,000 IOPS and, if possible, should be stored on a single Amazon EBS volume.
- () Which solution should a Solutions Architect recommend?
- () Create an Amazon EC2 instance with four Amazon EBS General Purpose SSD (gp2) volumes attached. Max out the IOPS on each volume and use a RAID 0 stripe set.
- () Create a Nitro-based Amazon EC2 instance with an Amazon EBS Provisioned IOPS SSD (i01) volume attached. Provision 64,000 IOPS for the volume.
- () Use an instance from the I3 I/O optimized family and leverage instance store storage to achieve the IOPS requirement.
- () Create an Amazon EC2 instance with two Amazon EBS Provisioned IOPS SSD (i01) volumes attached. Provision 32,000 IOPS per volume and create a logical volume using the OS that aggregates the capacity.
- () Amazon EC2 Nitro-based systems are not required for this solution but do offer advantages in performance that will help to maximize the usage of the EBS volume. For the data storage volume an i01 volume can support up to 64,000 IOPS so a single volume with sufficient capacity (50 IOPS per GiB) can be deliver the requirements.
- () The current list of EBS volume types is in the table below:
- ()  is the correct answer.
- ()  is incorrect.
- ()  is incorrect. This is not a good use case for gp2 volumes. It is much better to use io1 which also meets the requirement of having a single volume with 64,000 IOPS.
- ()  is incorrect. There is no need to create two volumes and aggregate capacity through the OS, the Solutions Architect can simply create a single volume with 64,000 IOPS.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () https://digitalcloud.training/amazon-ec2/
- () AWS Compute
- () A startup is prototyping a movie streaming platform on AWS. The platform consists of an Application Load Balancer, an Auto Scaling group of Amazon EC2 instances to host the frontend, and an Amazon RDS for PostgreSQL DB instance running in a Single-AZ configuration.
- () Users report slow response times when browsing the catalog of available movies. The movie catalog is a set of tables in the database that is updated infrequently. A solutions architect finds that the database's CPU utilization spikes significantly during catalog queries.
- () What should the solutions architect recommend to improve the performance of the platform during catalog searches?
- **() Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache.** [CORRECT]
- () Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas.
- () Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora’s built-in caching to handle frequent queries efficiently.
- () Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog.
- () Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache: This is correct because ElastiCache provides a highly performant in-memory caching layer that can significantly reduce database load and response times for infrequently updated data like a product or movie catalog. Lazy loading ensures the cache is populated only when a query misses, reducing unnecessary overhead.
- () Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog: This is incorrect because migrating to DynamoDB introduces unnecessary complexity and operational overhead, especially for a relational workload that involves the movie catalog. DAX is designed for NoSQL databases and is not the best fit for this use case.
- () Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas: This is incorrect because while read replicas can improve performance for read-heavy workloads, they do not reduce query latency as effectively as an in-memory caching solution like ElastiCache.
- () Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora’s built-in caching to handle frequent queries efficiently: This is incorrect because switching to Aurora Serverless would involve significant changes to the database architecture. While Aurora provides caching, ElastiCache is specifically optimized for high-performance caching use cases.
- () https://aws.amazon.com/elasticache/
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html

**Answer:**
Correct Answer: **Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache.**

---

## Question 207

**Q:** What should the solutions architect recommend to improve the performance of the platform during catalog searches?

**Options:**
- (A) Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache.
- (B) Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas.
- (C) Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora’s built-in caching to handle frequent queries efficiently.
- (D) Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog.
- (E) Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache: This is correct because ElastiCache provides a highly performant in-memory caching layer that can significantly reduce database load and response times for infrequently updated data like a product or movie catalog. Lazy loading ensures the cache is populated only when a query misses, reducing unnecessary overhead.
- (F) Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog: This is incorrect because migrating to DynamoDB introduces unnecessary complexity and operational overhead, especially for a relational workload that involves the movie catalog. DAX is designed for NoSQL databases and is not the best fit for this use case.
- (G) Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas: This is incorrect because while read replicas can improve performance for read-heavy workloads, they do not reduce query latency as effectively as an in-memory caching solution like ElastiCache.
- (H) Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora’s built-in caching to handle frequent queries efficiently: This is incorrect because switching to Aurora Serverless would involve significant changes to the database architecture. While Aurora provides caching, ElastiCache is specifically optimized for high-performance caching use cases.
- (I) References:
- (J) https://aws.amazon.com/elasticache/
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-elasticache/
- () AWS Database
- () A global manufacturing company uses AWS Outposts servers to manage IoT workloads in its factories across multiple continents. The company regularly updates factory IoT software, consisting of 50 files, from a central Amazon S3 bucket in the us-east-1 Region. Factories report significant delays when downloading and applying the updates, causing downtime. The company needs to minimize the latency for distributing software updates globally while reducing operational overhead.
- () Which solution will meet this requirement with the LEAST operational overhead?
- () Create Amazon S3 buckets in multiple Regions. Configure S3 Cross-Region Replication (CRR) between the buckets. Deploy updates from the nearest bucket to each factory location.
- () Create an Amazon S3 bucket in the us-east-1 Region. Deploy AWS Outposts servers at the factories as S3 endpoints. Configure the servers to cache the updates locally.
- () Create an Amazon S3 bucket in the us-east-1 Region. Set up an Amazon CloudFront distribution with the S3 bucket as the origin. Use signed URLs to download the software updates.
- () Create an Amazon S3 bucket in the us-east-1 Region. Configure Amazon S3 Transfer Acceleration for the bucket. Use the S3 Transfer Acceleration endpoint for faster downloads.
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Storage
- () An insurance company has a web application that serves users in the United Kingdom and Australia. The application includes a database tier using a MySQL database hosted in eu-west-2. The web tier runs from eu-west-2 and ap-southeast-2. Amazon Route 53 geoproximity routing is used to direct users to the closest web tier. It has been noted that Australian users receive slow response times to queries.
- () Which changes should be made to the database tier to improve performance?
- () Migrate the database to Amazon DynamoDB. Use DynamoDB global tables to enable replication to additional Regions
- **() Migrate the database to an Amazon Aurora global database in MySQL compatibility mode. Configure read replicas in ap-southeast-2** [CORRECT]
- () Migrate the database to Amazon RDS for MySQL. Configure Multi-AZ in the Australian Region
- () Deploy MySQL instances in each Region. Deploy an Application Load Balancer in front of MySQL to reduce the load on the primary instance
- () The issue here is latency with read queries being directed from Australia to UK which is great physical distance. A solution is required for improving read performance in Australia.
- () An Aurora global database consists of one primary AWS Region where your data is mastered, and up to five read-only, secondary AWS Regions. Aurora replicates data to the secondary AWS Regions with typical latency of under a second. You issue write operations directly to the primary DB instance in the primary AWS Region.
- () This solution will provide better performance for users in the Australia Region for queries. Writes must still take place in the UK Region but read performance will be greatly improved.
- ()  is the correct answer.
- ()  is incorrect. The database is located in UK. If the database is migrated to Australia then the reverse problem will occur. Multi-AZ does not assist with improving query performance across Regions.
- ()  is incorrect as a relational database running on MySQL is unlikely to be compatible with DynamoDB.
- ()  is incorrect as you can only put ALBs in front of the web tier, not the DB tier.
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
- () https://digitalcloud.training/amazon-aurora/

**Answer:**
Correct Answer: **Migrate the database to an Amazon Aurora global database in MySQL compatibility mode. Configure read replicas in ap-southeast-2**

---


