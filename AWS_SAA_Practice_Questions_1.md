# AWS SAA-C03 Practice Questions - Part 1

Total Questions: 39

---

## Question 1

**Q:** To use a custom domain name and URL when hosting a static website in a bucket, what two services of AWS are required?

**Options:**
- (A) S3 and DynDNS
- (B) S3 and ELB
- **(C) S3 and Route 53** [CORRECT]
- (D) S3 and ElastiCache

**Explanation:**
S3 and Route 53 is the correct answer. S3 is used to store the static website files; however, it would use a URL like bucket_name.s3-website-us-west-1.amazonaws.com. To also use a custom domain name, Route 53, the AWS DNS service, is required. DynDNS is not an AWS service. ELB and ElastiCache will not help to provide a custom DNS name.

---

## Question 2

**Q:** You are implementing an ELB solution. You want to ensure high availability. Where should the resources to which ELB directs be located?

**Options:**
- (A) In one region
- (B) In one Availability Zone
- **(C) In different Availability Zones** [CORRECT]
- (D) In one VPC

**Explanation:**
In different Availability Zones is correct. To ensure high availability, resources should be in more than one Availability Zone. ELB will direct traffic to healthy resources in the various Availability Zones.

---

## Question 3

**Q:** You have been asked to host a static website in AWS as quickly as possible. What is the simplest solution to use?

**Options:**
- **(A) S3** [CORRECT]
- (B) EFS
- (C) ELB
- (D) EC2 instance

**Explanation:**
S3 is the correct answer. The simplest solution is to place the website files into an S3 bucket and then enable web sharing on the bucket and associate it with a DNS name. ELB and EFS do not directly provide hosting. An EC2 instance would require instantiating a full instance, configuring the web service on the instance, and then placing the website files into the instance, which is more complex than hosting through an S3 bucket.

---

## Question 4

**Q:** You have implemented a NACL and notice that return traffic from an internal request is not allowed. Why is this happening?

**Options:**
- (A) NACLs are stateful
- (B) NACLs have many bugs in AWS
- **(C) NACLs are stateless** [CORRECT]
- (D) NACLs, once implemented, block all inbound traffic regardless of rules

**Explanation:**
NACLs are stateless is the correct answer. Because NACLs are stateless (unlike security groups, which are stateful) they do not automatically allow inbound responses to internally originating requests. All inbound communications must be explicitly allowed by rules.

---

## Question 5

**Q:** You have been asked to provide a folder-like structure in S3 buckets. How can this be accomplished?

**Options:**
- (A) Using actual directories
- (B) Using nested S3 buckets
- **(C) Using prefixes and delimiters** [CORRECT]
- (D) Using actual folders

**Explanation:**
. Nested S3 buckets are not supported.

---

## Question 6

**Q:** Where are AWS Cost and Usage Reports stored?

**Options:**
- (A) EBS volumes
- **(B) S3 bucket** [CORRECT]
- (C) The are not stored, they are sent via e-mail
- (D) In unmanaged, no-cost storage

**Explanation:**
S3 bucket is the correct answer. Cost and Usage Reports are generated from Redshift or QuickSight data source and are stored in S3 buckets. The Cost and Usage Reports interface provides an option to create an S3 bucket, appropriately configured, for report storage.

---

## Question 7

**Q:** What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?

**Options:**
- (A) CloudWatch
- **(B) Trusted Advisor** [CORRECT]
- (C) CloudFront
- (D) RDS

**Explanation:**
Trusted Advisor is the correct answer. AWS Trusted Advisor can provide security-related suggestions to improve the security of your AWS deployment. CloudWatch, CloudFront and RDS do not provide such advice.

---

## Question 8

**Q:** What two caching engines are supported by ElastiCache?

**Options:**
- **(A) Redis and memcached** [CORRECT]
- (B) Ready-cache and opencache
- (C) Opencache and memcached
- (D) Redis and opencache

**Explanation:**
Redis and memcached is the correct answer. ElastiCache does not support opencache or ready-cache; however, it does support both Redis and memcached. ElastiCache provides in-memory caching for improved performance.

---

## Question 9

**Q:** In addition to inbound and outbound rules, what type of rule does a security group allow?

**Options:**
- (A) Filtered rules
- (B) Unfiltered rules
- **(C) Allow rules** [CORRECT]
- (D) Deny rules

**Explanation:**
Allow rules is the correct answer. Security groups only have allow rules. Anything not explicitly allowed is denied. No such rules as filtered and unfiltered exist. Allow rules can be inbound or outbound or both.

---

## Question 10

**Q:** When should you use a dedicated host for an EC2 instance?

**Options:**
- (A) When you require a license based on the number of users
- **(B) When you require a license to be locked to the hardware** [CORRECT]
- (C) When you require a license file associated with an application installation
- (D) When you will use more than one application on the instance

**Explanation:**
When you require a license to be locked to the hardware is correct. A dedicated host provides a solution to specific licensing scenarios that require the license be locked to hardware, the number of CPU sockets, etc. Licenses based on the number of users or license files can work on any tenancy model. Using more than one application is possible with any tenancy model as well.

---

## Question 11

**Q:** In the event of loss of access to an Availability Zone for any reason, which S3 storage class does not provide resiliency?

**Options:**
- (A) S3 Standard-Infrequent Access
- (B) S3 Standard
- (C) S3 Glacier
- **(D) S3 One Zone-Infrequent Access** [CORRECT]

**Explanation:**
S3 One Zone-Infrequent Access is the correct answer. S3 One Zone-IA stores the objects only in one zone and if that Availability Zone is lost or access is blocked, the objects cannot be accessed. S3 Standard, Standard-IA and Glacier store objects in multiple AZs or through other archival methods providing recoverability.

---

## Question 12

**Q:** When you’re editing permissions (policies and ACLs), to whom does the concept of the “owner” refer?

**Options:**
- (A) There is no special concept of “owner” in AWS.
- (B) The owner is the IAM user who created the object via the GUI, CLI, or API.
- **(C) “Owner” refers to the identity and e-mail address used to create the AWS account.** [CORRECT]
- (D) The owner is IAM role used to create the object via the GUI, CLI, or API.

**Explanation:**
“Owner” refers to the identity and e-mail address used to create the AWS account is correct. In AWS, the context of the owner of the account is root, which needs to be logged in using the username/password combination. 

---

## Question 13

**Q:** You are running a Mongo database that requires access to tens of thousands of low-latency IOPS. Which of the following EC2 instance families would best suit your needs?

**Options:**
- (A) Cluster GPU instances
- **(B) High I/O instances** [CORRECT]
- (C) Dense storage instances
- (D) Memory-optimized instances

**Explanation:**
High I/O instances is correct. High I/O instances use SSD-based local instance storage to deliver very high, low-latency I/O capacity to applications, and they are optimized for applications that require tens of thousands of IOPS. 

---

## Question 14

**Q:** What can be used to aggregate several AWS accounts for centralized management and billing tracking?

**Options:**
- (A) AWS Budget
- **(B) AWS Organizations** [CORRECT]
- (C) AWS Trusted Advisor
- (D) AWS Cost and Reporting

**Explanation:**
AWS Organizations is correct. AWS Organizations are collections of AWS accounts placed under centralized management. Trusted Advisor provides suggestions for improved performance, security, and cost management. AWS Cost and Reporting and AWS Budget are used strictly for cost management and reporting.

---

## Question 15

**Q:** You have a small database workload with infrequent I/O. These databases are mainly used as ad hoc databases for noncritical testing purposes. Which storage medium would be the most cost-effective way to meet these requirements?

**Options:**
- (A) Amazon RDS Provisioned IOPS (SSD) Storage
- **(B) Amazon RDS Magnetic Storage** [CORRECT]
- (C) Amazon RDS Cold Storage
- (D) Amazon RDS General Purpose (SSD) Storage

**Explanation:**
Amazon RDS Magnetic Storage is the correct answer. Amazon RDS Magnetic Storage would be the most suitable. In this case, you need to consider the lower cost since these are noncritical databases.

---

## Question 16

**Q:** Which one of the following is controlled by a security group attached to an instance?

**Options:**
- (A) NACLs
- (B) Database error codes
- **(C) Inbound traffic** [CORRECT]
- (D) HTTP error codes

**Explanation:**
Inbound traffic is the correct answer. Security groups control inbound and outbound traffic. They do not control error codes of any kinds or NACLs, which are applied to the subnet and not to instances.

---

## Question 17

**Q:** You have several Windows and Linux instances within a single subnet in a VPC. You want to ensure that no inbound traffic can reach the Windows instances. What is the best option?

**Options:**
- (A) NACLs
- **(B) Security Groups** [CORRECT]
- (C) Linux firewall
- (D) IAM

**Explanation:**
Security Groups is the correct answer. The best option, in this case, is security groups for each Windows instance network interface. If this were controlled with NACLs, it would also prevent access to the Linux instances.

---

## Question 18

**Q:** What is the default limit on the number of S3 buckets that can be created by an account?

**Options:**
- **(A) 100** [CORRECT]
- (B) 200
- (C) 150

**Explanation:**
100 is the correct answer. The default limit is 100 S3 buckets per account. However, you can request an upgrade to create more S3 buckets.

---

## Question 19

**Q:** You must select the S3 storage class with the highest level of resiliency. Which class do you choose?

**Options:**
- (A) S3 Standard-Infrequent Access
- (B) S3 HA
- **(C) S3 Standard** [CORRECT]
- (D) S3 One Zone-Infrequent Access

**Explanation:**
S3 Standard is the correct answer. The S3 Standard class provides 99.999999999% uptime and is the highest resiliency offered. S3 Standard-IA provides for 99.9% uptime. S3 One Zone-IA provides for 99.5% uptime. No such class as S3 HA exists.

---

## Question 20

**Q:** What can be used to assign permissions to more than one user login without having to modify each login individually?

**Options:**
- **(A) Groups** [CORRECT]
- (B) Collections
- (C) ACL
- (D) NACL

**Explanation:**
Groups is the correct answer. AWS Identity and Access Management (IAM) supports the use of groups for such scenarios. Create a group. Assign permissions to the group. Place logins in the group. Collections are not supported in AWS and NACLs/ACLs do not provide a solution to this scenario.

---

## Question 21

**Q:** What is the default duration of cost history shown in the Cost Explorer view of AWS?

**Options:**
- (A) 1 month
- (B) 1 year
- (C) 2 years
- **(D) 6 months** [CORRECT]

**Explanation:**
6 months is the correct answer. The Cost Explorer shows 6 months' history by default. This can be adjusted. The history can be used to see where your costs are accruing and to potentially predict future costs.

---

## Question 22

**Q:** Which one of the following RDS database types does not support read replicas?

**Options:**
- **(A) Aurora** [CORRECT]
- (B) PostgreSQL
- (C) MySQL
- (D) MariaDB

**Explanation:**
Aurora is the correct answer. Aurora and Oracle, for example, do not support the RDS read replica function, though other options can be used to provide similar capabilities. MariaDB, PostgreSQL and MySQL all support the RDS read replica function.

---

## Question 23

**Q:** You’ve been tasked with implementing a globally accessible storage solution that will scale from a few terabytes (now) to an unknown, but significantly greater, volume of data in three years’ time. You don’t want to spend a lot of money. Which AWS service would best meet your current and projected storage needs and at the same time make sure the cost is minimal?

**Options:**
- **(A) S3** [CORRECT]
- (B) RDS
- (C) DynamoDB
- (D) EC2 with EBS

**Explanation:**
S3 is correct. Amazon S3 is highly scalable, secure storage and can be used for any kind of storage. S3 will scale to any projected volume of data. S3 provides different storage types to keep the cost minimal. 

---

## Question 24

**Q:** HTTP is used to upload to S3 buckets. Which HTTP method has eventual consistency with S3 bucket writes?

**Options:**
- (A) Updates
- **(B) Deletes** [CORRECT]
- (C) Erases
- (D) PUTs of new files

**Explanation:**
Deletes is the correct answer. Deletes and Overwrite PUTs have eventual consistency. Others have write and then read consistency. Erases are not supported.

---

## Question 25

**Q:** What is the model used within AWS wherein AWS guarantees the secure operation of the cloud and the customer ensures the security of that which is placed in the cloud?

**Options:**
- (A) Customer Responsibility
- **(B) Shared Responsibility** [CORRECT]
- (C) Provider Responsibility
- (D) User Responsibility

**Explanation:**
Shared Responsibility is the correct answer. The Shared Responsibility model is used in AWS. It states that AWS will secure the cloud itself, but the customer or user must secure that which they place in the cloud. For example, the customer must secure the operating system running in an EC2 instance as AWS will not control or manage that which runs in an instance.

---

## Question 26

**Q:** Although your application customarily runs at 30% usage, you have identified a recurring usage spike (greater than 90% usage) between 8 p.m. and midnight daily. What is the most cost-effective way to scale your application to meet this increased need?

**Options:**
- **(A) Use proactive cyclic scaling to boost your capacity at a fixed interval.** [CORRECT]
- (B) Increase the size of the resource group to meet demand.
- (C) Deploy additional EC2 instances to meet the demand.
- (D) Manually deploy reactive event-based scaling each night at 7:45.

**Explanation:**
Use proactive cyclic scaling to boost your capacity at a fixed interval. is the correct answer. In this case, you need to use proactive scaling at 8 p.m. and midnight, so you can have Auto Scaling policies that can handle the workload during that time. 

---

## Question 27

**Q:** You have been asked to implement a read replica RDS setup. What is the primary purpose of such a configuration?

**Options:**
- (A) Redundancy
- (B) Business continuity
- (C) Security
- **(D) Performance** [CORRECT]

**Explanation:**
Performance is the correct answer. Read replicas are created to improve the performance of read operations. They have a dedicated instance for read processing and write operations, as read operations are moved from the primary instance to a read replica instance. Read replicas are not primarily created for business continuity, redundancy, or security.

---

## Question 28

**Q:** What should be implemented when microsecond response time is required of a DynamoDB implementation?

**Options:**
- (A) ElastiCache
- (B) EFS
- (C) EBS
- **(D) DAX** [CORRECT]

**Explanation:**
DAX is the correct answer. DAX is the DynamoDB Accelerator, which is an in-memory cache solution specifically designed for DynamoDB and can result in response times in microseconds. ElastiCache can be used with DynamoDB, but is not optimized for it. EBS and EFS have no impact here.

---

## Question 29

**Q:** What is used to control network traffic at the subnet level in AWS?

**Options:**
- (A) Logins
- (B) Groups
- **(C) Network ACLs (NACLs)** [CORRECT]
- (D) Security groups

**Explanation:**
Network ACLs (NACLs) is the correct answer. NACLs operate at the subnet level and security groups operate at the instance level. NACLs support allow and deny rules and security groups support only allow rules. Logins and groups do not control network traffic, they control the ability to login and the permissions associated with a user (login).

---

## Question 30

**Q:** When does Amazon recommend using the db.t2.small and db.t2.medium database instances with the Aurora database service?

**Options:**
- (A) For heavy load servers
- (B) For medium load servers
- **(C) For development and test servers** [CORRECT]
- (D) For small load servers

**Explanation:**
For development and test servers is the correct answer. Amazon only recommends the use of db.t2.small and db.t2.medium for non-production servers such as development and test servers.

---

## Question 31

**Q:** You are working with AWS AMIs. What kind of AMI should be used when you want to customize an image and then reuse it to scale up a deployment?

**Options:**
- **(A) Private AMI** [CORRECT]
- (B) Amazon Quick Start AMI
- (C) AWS Marketplace AMI
- (D) Community AMI

**Explanation:**
Private AMI is the correct answer. A private AMI can be created based on your customized image. This allows you to easily scale up a solution. Community, Marketplace, and Quick Start AMIs can be used for the initial instance that is to be customized, but they cannot be customized themselves.

---

## Question 32

**Q:** What instance type family is best used when things like specialized GPUs or FPGAs are required?

**Options:**
- **(A) Accelerated computing** [CORRECT]
- (B) Memory-optimized
- (C) Storage-optimized
- (D) Compute-optimized

**Explanation:**
Accelerated computing is the correct answer. Accelerated computing supports graphics processing units (GPUs) and field-programmable gate arrays (FPGAs) for enhanced processing. Compute-optimized simply provides more powerful CPUs, memory-optimized provides more and faster memory, and storage-optimized provides storage up to 48 TB.

---

## Question 33

**Q:** You have been given control of an existing AWS environment (account). You want to ensure costs are being managed well. What tool should you run?

**Options:**
- (A) CloudFormation
- **(B) Trusted Advisor** [CORRECT]
- (C) CloudTrail
- (D) CloudWatch

**Explanation:**
Trusted Advisor is correct. The Trusted Advisor can give recommendations for reducing costs, so this is the tool to run among those listed. CloudWatch monitors the AWS cloud. CloudTrail provides logging for activities in the cloud. CloudFormation is used to automatically deploy a solution.

---

## Question 34

**Q:** Which one of the following is not something for which AWS Trusted Advisor makes recommendations?

**Options:**
- (A) Performance
- **(B) Scalability** [CORRECT]
- (C) Fault Tolerance
- (D) Cost

**Explanation:**
Scalability is correct. Trusted advisor can make recommendations in the areas of cost, performance, fault tolerance, security, and service limits. It does not make direct recommendations for scalability.

---

## Question 35

**Q:** You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?

**Options:**
- (A) AWS CloudFront alerts
- (B) AWS Trusted Advisor alerts
- (C) AWS ElastiCache alerts
- **(D) AWS Budget alerts** [CORRECT]

**Explanation:**
AWS Budget alerts is correct. The AWS Budget service can be configured with your budgets for all areas of cost. Alerts can be sent via email or stored in S3 buckets. CloudFront is used for CDN caching and ElastiCache is an in-memory caching service. Trusted Advisor analyzes your account and makes suggestions, but does not provide direct budgetary control.

---

## Question 36

**Q:** What AWS database solution is best suited for data warehouse implementations?

**Options:**
- (A) EBS
- **(B) Redshift** [CORRECT]
- (C) DynamoDB
- (D) Aurora

**Explanation:**
Redshift is the correct answer. Redshift is designed as on OLAP data warehouse database solution. Aurora and DynamoDB service other purposes (OLTP and NoSQL respectively). EBS is a block storage solution and not a database solution.

---

## Question 37

**Q:** In addition to the proper configuration of RDS database settings, what can be done to improve overall performance of database operations?

**Options:**
- (A) Use better EFS implementations
- (B) Use fewer security groups
- **(C) Tune SQL queries** [CORRECT]
- (D) Use better EBS volumes

**Explanation:**
Tune SQL queries is the correct answer. RDS databases do not provide storage-level access for EBS or EFS volumes, so you should consider tuning the SQL queries to improve overall performance. Security groups should not impact performance in operation.

---

## Question 38

**Q:** Which one of the following components is used at a customer location to implement a site-to-site VPN connection with AWS?

**Options:**
- **(A) Customer gateway** [CORRECT]
- (B) AWS VPN on-premises gateway
- (C) Virtual private gateway
- (D) Filtered firewall gateway

**Explanation:**
Customer gateway is the correct answer. The customer gateway is implemented on-premises at the customer location. The virtual private gateway (VPG) exists on the AWS cloud side of the VPN. Filtered firewall gateway and AWS CPN on-premises gateway are not terms used in association with AWS VPNs.

---

## Question 39

**Q:** Which one of the following storage methods is object-based?

**Options:**
- **(A) S3 Standard** [CORRECT]
- (B) EFS
- (C) VHD
- (D) EBS

**Explanation:**
S3 Standard is the correct answer. All S3 storage is object-based. EBS is block-based. VHD is used to import virtual machines as AWS Machine Images (AMIs). EFS is also block-based.

---


