# AWS SAA-C03 Practice Questions - Part 4

Total Questions: 39

---

## Question 1

**Q:** You are responsible for implementing Amazon Kinesis Data Analytics. What language is used to process the data streams as they flow through the system?

**Options:**
- **(A) SQL** [CORRECT]
- (B) PHP
- (C) Ruby
- (D) Python

**Explanation:**
SQL is the incorrect answer. Kinesis Data Analytics uses SQL to read values from the data streams and perform analysis so that no new language is required. An incoming data stream is processed with SQL queries and the results are loaded into a desired destination for further processing.

---

## Question 2

**Q:** At the monthly product meeting, one of the product owners proposes an idea to address an immediate shortcoming of the product system: storing a copy of the customer price schedule in the customer record in the database. You know that you can store large text or binary objects in DynamoDB. You give a tentative OK to do a minimum viable product (MVP) test, but you stipulate that it must comply with the size limitation on the attribute name and value. Which is the correct limitation?

**Options:**
- **(A) The value and name combined must not exceed 400KB.** [CORRECT]
- (B) The value and name combined must not exceed 1024KB.
- (C) The name must not exceed 64KB, and the value must not exceed 500KB.
- (D) The name must not exceed 64KB, and the value must not exceed 1024KB.
- (E) The value and name combined must not exceed 500KB.
- () The name must not exceed 128KB, and the value must not exceed 400KB.

**Explanation:**
The value and name combined must not exceed 400KB is correct. The combined size for the name and value can’t exceed 400KB.

---

## Question 3

**Q:** What is true about edge locations when using CloudFront?

**Options:**
- (A) They are write-only
- (B) They are read-only
- **(C) They are read/write** [CORRECT]
- (D) They are not accessible from machines outside of AWS VPCs

**Explanation:**
They are read/write is the correct answer. CloudFront edge locations are read/write. They are accessible from machines outside of AWS VPCs, which is the primary purpose of their existence - to provide localized copies of files for faster regional access.

---

## Question 4

**Q:** What AWS tool can be used to estimate the cost of storage for an AWS solution?

**Options:**
- (A) AWS Budgets
- (B) AWS Cost Explorer
- (C) AWS Cost and Usage Report
- **(D) AWS Pricing Calculator** [CORRECT]

**Explanation:**
The AWS Pricing Calculator can be used to estimate costs for the major AWS services including S3 and EC2.

---

## Question 5

**Q:** You must transfer 40 TB of data into AWS S3 buckets. You are concerned about the time it will take to transfer the files over the network and the impact it will have on user performance. What is the best option for transferring such a large amount of data without impacting network user performance?

**Options:**
- (A) HTTP transfer
- (B) Direct Connect
- **(C) Snowball** [CORRECT]
- (D) HTTPS transfer

**Explanation:**
Snowball is the correct answer. Using Snowball, you will connect the Snowball device to your local network and transfer all of the data to it. Then you will ship it to AWS and they will load it into your AWS account. This will result in no performance impact on your Internet connection.

---

## Question 6

**Q:** What is a primary difference between EFS and EBS storage in AWS?

**Options:**
- (A) EFS is block storage and EBS is object storage
- (B) EBS storage can be shared across regions and EFS cannot
- **(C) EFS storage can be shared across regions and EBS cannot** [CORRECT]
- (D) EBS is block storage and EFS is object storage

**Explanation:**
EFS storage can be shared across regions and EBS cannot is the correct answer. Elastic File System (EFS) can be shared across regions and Elastic Block Store (EBS) cannot. Both are block storage.

---

## Question 7

**Q:** What important action may help to reduce costs of AWS operations over a long period of time?

**Options:**
- (A) Use Elastic IP (EIP) addresses for all EC2 network interfaces
- (B) Use S3 Standard for all storage
- (C) Use multiple VPCs with redundant EC2 instances in separate VPCs for all EC2 instances by default
- **(D) Keep up to date with new AWS service releases** [CORRECT]

**Explanation:**
Keep up to date with new AWS service releases is the correct answer. While extra costs can be incurred due to all listed items, the selected database engine has the largest impact on cost. Licensed engines (requiring a non-AWS license) such as Oracle and SQL Server can have costs 2-5 times higher the open source or AWS-original database engines.

---

## Question 8

**Q:** You want to limit who can modify a NACL that is associated with a subnet. What can you use?

**Options:**
- (A) Security Group
- (B) Another NACL
- (C) Flow log
- **(D) IAM** [CORRECT]

**Explanation:**
IAM is the correct answer. A NACL is an object that can be configured with permissions, so you can use IAM to decide who can and cannot manage the NACL. The other options in no way provide permission management for NACL objects.

---

## Question 9

**Q:** What is the container used to store DNS records called in Route 53?

**Options:**
- **(A) Hosted zone** [CORRECT]
- (B) DNS resolver
- (C) DNS record
- (D) Authoritative name server

**Explanation:**
Hosted zones is the correct answer. The hosted zone is the container object for the DNS records. The DNS resolver is the role of Route 53 - resolving DNS host names and other records. The authoritative name server is a name server having definitive information about a portion of the DNS system. A DNS record is an individual record stored in the hosted zone container.

---

## Question 10

**Q:** If you want all user requests made to a CloudFront configuration to force HTTPS instead of HTTP transfers, what should you do?

**Options:**
- **(A) Configure the Protocol Policy to specify Redirect HTTP to HTTPS** [CORRECT]
- (B) This cannot be forced if the users did not request it
- (C) Configure each edge location web server to use only HTTPS
- (D) Configure the source web server to use only HTTPS

**Explanation:**
Configure the Protocol Policy to specify Redirect HTTP to HTTPS is the correct answer.

---

## Question 11

**Q:** You are implementing a content delivery network (CDN) using Amazon CloudFront. What are the locations, distributed throughout the world, that contain the cached data called?

**Options:**
- **(A) Edge locations** [CORRECT]
- (B) Distributed locations
- (C) Cloud locations
- (D) Front locations

**Explanation:**
Edge locations is the correct answer. The term used in CloudFront is edge locations. These edge locations are data centers located in major cities throughout the world and allow for data to be cached closer to the requesting users.

---

## Question 12

**Q:** What should the last rule be in a NACL that allows three protocols and disallows everything else?

**Options:**
- (A) All traffic/Allow
- **(B) All traffic/Deny** [CORRECT]
- (C) TCP traffic/Allow
- (D) TCP traffic/Deny

**Explanation:**
All traffic/Deny is the correct answer. If the final rule is All traffic/Deny and preceding rules (lower numbered rules) allow specific traffic, the specific traffic will be allowed because it matches those rules before getting to the All traffic/Deny rule. However, because the last rule is All traffic/Deny, any traffic not specified in the rule will indeed be denied.

---

## Question 13

**Q:** Your company likes the idea of storing files on AWS. However, low-latency service of the majority of files is important to customer service. Which Storage Gateway configuration would you use to achieve both these ends?

**Options:**
- (A) Gateway-VTL
- (B) Gateway-Cached
- (C) Gateway-Snapshot
- **(D) Gateway-Stored** [CORRECT]

**Explanation:**
Gateway-Stored is correct. In this case, they key is low latency, and you have to choose the solution based on that. Since you want a low-latency solution, Gateway-Stored is the right way to go. 

---

## Question 14

**Q:** You are creating a data lake, and one of the criteria you are looking for is faster performance. You want the ability to transform the data directly during the ingestion process to save time and cost. Which AWS service should you choose for this?

**Options:**
- (A) Ingest the data in S3 and then use EMR to transform.
- **(B) Use Kinesis Analytics for transforming the data.** [CORRECT]
- (C) Ingest the data in S3 and then load it in Redshift to transform.
- (D) Use Kinesis Firehose.

**Explanation:**
Use Kinesis Analytics for transforming the data is correct. Kinesis Analytics has the ability to transform the data during ingestion.

---

## Question 15

**Q:** You must attach an EBS volume to an EC2 instance that offers the highest level of performance. What EBS type should be used?

**Options:**
- **(A) Provisioned IOPS SSD** [CORRECT]
- (B) Striped SSD
- (C) Magnetic
- (D) General SSD

**Explanation:**
Provisioned IOPS SSD is the correct answer. A provisioned IOPS SSD will provide the optimum performance. A general SSD would be next. Magnetic storage provides the least performance, but it also provides the least cost. You do not directly control the physical implementation of disks, so you cannot select disk striping or mirroring at the physical level.

---

## Question 16

**Q:** What is the maximum VisibilityTimeout value of an SQS message in a FIFO queue?

**Options:**
- (A) 1 hour
- (B) 14 days
- **(C) 12 hours** [CORRECT]
- (D) 1 day

**Explanation:**
12 hours is correct. The maximum VisibilityTimeout value you can have for an SQS message in a FIFO is 12 hours.

---

## Question 17

**Q:** You have three Elastic Network Interfaces (ENIs). They are attached to three instances. You need an ENI for another instance and one of the instances currently using an ENI no longer needs it. What is the best action to take?

**Options:**
- **(A) Move the ENI from the instance no longer needing it to the instance requiring it** [CORRECT]
- (B) Delete the ENI from the instance no longer requiring it and then create a new ENI for the instance requiring it
- (C) Create a new ENI and attach it to the instance requiring it
- (D) You cannot have more than two active ENIs.

**Explanation:**
Move the ENI from the instance no longer needing it to the instance requiring it is the correct answer. While an ENI can only be attached to one instance, you can move them from one instance to another. You can have more than two active ENIs.

---

## Question 18

**Q:** When storing data in EC2 instances, in addition to storage space requirements, what cost factor must be considered?

**Options:**
- (A) Data transfer costs (from your local network to AWS)
- **(B) Data transfer costs (from AWS to your local network)** [CORRECT]
- (C) Data encryption costs
- (D) Data decryption costs

**Explanation:**
Data transfer costs (from AWS to your local network) is the correct answer. Given the scenario, reserved pricing will have a significant impact on costs. However, you must be able to accurately predict your needs for 1-3 years. Savings as high as 75% can be achieved when using reserved pricing.

---

## Question 19

**Q:** You must implement an AWS solution that can expand and contract the number of server instances as needed. What AWS service provides this functionality?

**Options:**
- **(A) Auto Scaling** [CORRECT]
- (B) ElastiCache
- (C) Lambda
- (D) Auto Growing

**Explanation:**
Auto Scaling is the correct answer. AWS Auto Scaling can expand or contract the number of servers in a solution automatically based on current demands. This allows you to use and pay for the services you require, based on the load, but not more. No such service as Auto Growing exists. ElastiCache provides in memory caching. Lambda is a code execution engine that allows you to execute code without building out the instances required to run the code.

---

## Question 20

**Q:** You must enable alerts and other notifications to be sent to the appropriate individuals from the AWS cloud. What AWS service can provide this function?

**Options:**
- **(A) Amazon Simple Notification Service (SNS)** [CORRECT]
- (B) Amazon Kinesis
- (C) Amazon Simple Queue Service (SQS)
- (D) Amazon Simple Workflow (SWF)

**Explanation:**
Amazon Simple Notification Services (SNS) is the correct answer. SNS is used to send notifications, which can be sent via HTTP/HTTPS, SMS, Lambda, SQS, or e-mail. SQS is used for queueing requests so that they can be processed as needed. SWF is used to perform operations based on the state of a system and it is being replaced with step functions.

---

## Question 21

**Q:** What two methods are provided in AWS RDS for database backups?

**Options:**
- (A) Manual backups and automated snapshots
- (B) Automated backups and manual snapshots
- (C) Manual backups and manual snapshots
- **(D) Automated backups and automated snapshots** [CORRECT]

**Explanation:**
Automated backups and automated snapshots is the correct answer. AWS RDS supports two methods of backup: automated backups and automated snapshots. The backups are complete backups of the database. The snapshots are backups of the changes incurred since the last snapshot.

---

## Question 22

**Q:** When multiple resources can perform the same function, which one of the following is not a valid routing policy that Route 53 can use to select the appropriate resource for a request?

**Options:**
- (A) Geo DNS routing
- (B) Weighted round robin
- **(C) OS-based routing** [CORRECT]
- (D) Latency-based routing

**Explanation:**
OS-based routing is the correct answer. Route 53 supports Geo DNS routing, Failover routing, Latency-based routing and Weighted round robin routing. It does not support redirection based on the OS of the requesting system.

---

## Question 23

**Q:** Your company is generating a huge volume of data sets with billions of rows that must be summarized by column. You are going to use Tableau on top of these data sets to build daily and weekly reports. Which AWS service should you use to meet these requirements?

**Options:**
- **(A) Amazon Redshift** [CORRECT]
- (B) ElastiCache
- (C) Amazon DynamoDB
- (D) Amazon RDS

**Explanation:**
Amazon Redshift is correct. Amazon Redshift is Amazon’s data warehouse offering, where the data is stored in columnar format. 

---

## Question 24

**Q:** You’re building out a single-region application in us-west-2. However, disaster recovery is a strong consideration, and you need to build the application so that if us-west-2 becomes unavailable, you can fail over to us-west-1. Your application relies exclusively on pre-built AMIs. In order to share those AMIs with the region you’re using as a backup, which process would you follow?

**Options:**
- (A) Copy the AMI from us-west-2 to us-west-1 and launch it as is.
- (B) Create a new instance in us-west-1, making certain the instance in the failover region shares a security group with the instance in the default region.
- **(C) Copy the AMI from us-west-2, manually apply launch permissions, user-defined tags, and Amazon S3 bucket permissions of the default AMI to the new instance, and launch the instance.** [CORRECT]
- (D) Do nothing. AMIs are specific to an account, and they can be used anywhere.

**Explanation:**
Copy the AMI from us-west-2, manually apply launch permissions, user-defined tags, and Amazon S3 bucket permissions of the default AMI to the new instance, and launch the instance is correct because AWS does not copy launch permissions, user-defined tags, or Amazon S3 bucket permissions from the source AMI to the new AMI. 

---

## Question 25

**Q:** How long are one-minute data points maintained for viewing in Amazon CloudWatch?

**Options:**
- **(A) 15 days** [CORRECT]
- (B) 15 months
- (C) 63 days
- (D) Indefinitely

**Explanation:**
15 days is the correct answer. One-minute data points are maintained for 15 days. Five-minute data points are maintained for 63 days. One-hour data points are maintained for 15 months or 455 days.

---

## Question 26

**Q:** Which one of the following scenarios would result in a higher percentage of savings when using S3 Standard Infrequent Access storage instead of S3 Standard storage?

**Options:**
- **(A) 1 TB monthly with 10% of content accessed per month** [CORRECT]
- (B) None of these, content accessed per month must be less then 5% to generate any savings
- (C) 1 TB monthly with 100% of content accessed per month
- (D) 1 TB monthly with 50% of content accessed per month

**Explanation:**
1 TB monthly with 10% of content accessed per month is the correct answer. According to the AWS 2020 Cost Optimization Pillar documentation, the consumption model is defined as paying only for the computing resources you consume and increasing or decreasing usage depending on business requirements. The other named models are not referenced in AWS documentation for the Cost Optimization Pillar.

---

## Question 27

**Q:** You are concerned about maintaining security patches on the 103 AWS EC2 instances that you run. All instances run Windows, Ubuntu Server, or Red Hat Enterprise Linux. What AWS service can assist you on properly and automatically patching these instances?

**Options:**
- **(A) AWS Systems Manager Patch Manager** [CORRECT]
- (B) AMI Manager
- (C) CloudFormation
- (D) CodeDeploy

**Explanation:**
AWS Systems Manager Patch Manager is the correct answer. The AWS Systems Manager Patch Manager can automate security patches for supported Windows and Linux systems. It can also apply non-security patches to Linux systems. AMI Manager does not exist in AWS and the other services do not provide this functionality.

---

## Question 28

**Q:** How many hours of EC2 compute are provided in the free tier?

**Options:**
- **(A) 750** [CORRECT]
- (B) 1000
- (C) 500
- (D) 250

**Explanation:**
750 is the correct answer. 750 hours of compute are provided when using free tier instance classes for the first 12 months in AWS. Amazon RDS provides the same number of hours of compute for databases in the same 12-month window.

---

## Question 29

**Q:** You manage a Ruby on Rails application that lives on a cluster of EC2 instances. Your website occasionally experiences brief, strong, and entirely unpredictable spikes in traffic that overwhelm your EC2 instances’ resources and freeze the application. As a result, you’re losing recently submitted requests from end users. You use Auto Scaling to deploy additional resources to handle the load during spikes, but the new instances don’t spin up fast enough to prevent the existing application servers from freezing. Which of the following actions will provide the most cost-effective solution in preventing the loss of recently submitted requests?

**Options:**
- (A) Keep a large EC2 instance on standby.
- (B) Increase the size of your existing EC2 instances.
- **(C) Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto Scaling instances are available.** [CORRECT]
- (D) Ask AWS support to pre-warm the Elastic Load Balancer.

**Explanation:**
Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto Scaling instances are available is correct. The cost-effective solution to the unpredictable spike in traffic is to use SQS to decouple the application components.

---

## Question 30

**Q:** When considering NACLs and security groups, what is evaluated first when a packet is inbound to an EC2 instance?

**Options:**
- (A) Neither, they are processed at the same time
- (B) Security group then NACL
- **(C) NACL then security group** [CORRECT]
- (D) Neither, they cannot be used together

**Explanation:**
NACL then security group is the correct answer. NACLs and security groups can be used together in the flow of traffic into an EC2 instance. Because the NACLs are associated with the subnet, they are processed first and then security groups, which are associated with the instance network interface, are processed.

---

## Question 31

**Q:** You are defining appropriate security options for S3 buckets in AWS. As part of the process, you must identify the default access restrictions on S3 buckets. Which one of the following best describes the default access restrictions in place on S3 buckets?

**Options:**
- **(A) Only bucket and object owners have access to the resources they create** [CORRECT]
- (B) Anonymous users have access to all S3 buckets and objects
- (C) Only IAM administrators have access to S3 buckets
- (D) All IAM users have access to all S3 buckets and objects

**Explanation:**
Only bucket and object owners have access to the resources they create is the correct answer. By default, only buck and object owners have access to the resources they create, and other users must be granted access or access must be granted to public or anonymous users, if desired.

---

## Question 32

**Q:** What does AWS provide for extremely large dataset transport to the cloud that provides for offline transport?

**Options:**
- (A) Glacier
- **(B) Snowball** [CORRECT]
- (C) CloudFront

**Explanation:**
Snowball is the correct answer. Snowball is used to transport large datasets offline. Glacier and S3 are online storage services. CloudFront is a web cache service.

---

## Question 33

**Q:** Your application uploads several thousands of files every day. The file sizes range from 500MB to 2GB. Each file is then processed to extract metadata, and the metadata processing takes a few seconds. There is no fixed uploading frequency; sometimes all the files are uploaded at a particular hour, sometimes only a few files are uploaded at a particular hour, and sometimes no uploads occur for a few hours. What is the most cost-effective way of handling this issue?

**Options:**
- (A) Use Amazon Kinesis to store the files and then use Lambda for extracting the metadata.
- (B) Use EFS to store the file and then use multiple EC2 instances to extract the metadata.
- (C) Use an SQS queue to store the file and then use an EC2 instance to extract the metadata.
- **(D) Store the files in Amazon S3 and then use an S3 event notification to invoke a Lambda function for extracting the metadata.** [CORRECT]

**Explanation:**
Store the files in Amazon S3 and then use an S3 event notification to invoke a Lambda function for extracting the metadata is correct. Amazon S3 is the cheapest solution in this case.

---

## Question 34

**Q:** You are required to run Docker containers within AWS. What AWS solution provides this service?

**Options:**
- (A) Lambda
- **(B) EC2 Container Service (ECS)** [CORRECT]
- (C) Lightsail
- (D) CloudFormation

**Explanation:**
EC2 Container Service (ECS) is the correct answer. ECS is the AWS container service and it allows for the execution of Docker containers. Lambda is a code execution engine that allows you to execute code without building out the instances required to run the code. CloudFormation is an AWS service used to automatically launch entire solutions (including multiple instances and services) through code. Lightsail is the AWS service used to simply deploy web applications and web sites in AWS.

---

## Question 35

**Q:** You must backup an EBS volume as quickly as possible and perform this backup once each day. What is the best method provided within AWS to perform this backup?

**Options:**
- (A) RDS backup
- (B) Backup software centralized in one EC2 instance used to backup other instance attached EBS volumes
- **(C) Snapshots** [CORRECT]
- (D) Internal backup software in the EC2 instance

**Explanation:**
Snapshots is the correct answer. Snapshots are incremental backups such that they backup only the blocks that have changed in the EBS volume since the last snapshot was taken. This provides a fast backup option. The other options of using backup software will take much longer and require more administrative overhead. RDS backup cannot be used to backup EBS volumes, it is used to backup databases.

---

## Question 36

**Q:** You are in the process of designing a document archive solution for your company. The solution must be cost-effective; therefore, you have selected Glacier. The business wants to have the capability to get a document within 15 minutes of requesting it. Which feature of Amazon Glacier will you choose?

**Options:**
- (A) Glacier is not the correct solution. You need Amazon S3.
- **(B) Expedited retrieval** [CORRECT]
- (C) Standard retrieval
- (D) Bulk retrieval

**Explanation:**
Expedited retrieval is correct. Since you are looking for a cost-effective archival solution, Amazon Glacier is the right choice. By using the expedited retrieval option, you should be able to get the file within 5 minutes, which meets your business objective. 

---

## Question 37

**Q:** What AWS service can be used to monitor your EC2 instances and provide a dashboard for performance management?

**Options:**
- (A) CloudFormation
- (B) CloudFront
- (C) Performance Monitor
- **(D) CloudWatch** [CORRECT]

**Explanation:**
CloudWatch is the correct answer. CloudWatch is an AWS service that can gather metrics from multiple sources and provide dashboards for monitoring. CloudFront is a content distribution network (CDN) solution. CloudFormation is used to provision resources for a cloud solution automatically. Performance monitor is a performance monitoring tool in Windows and not an AWS service.

---

## Question 38

**Q:** You are in the process of deploying an application in an EC2 instance. The application must call AWS APIs. What is the secured way of passing credentials to the application?

**Options:**
- (A) Use a DynamoDB to store the API credentials.
- **(B) Assign IAM roles to the EC2 instance.** [CORRECT]
- (C) Pass the API credentials to the instance using instance user data.
- (D) Keep API credentials as an object in Amazon S3.

**Explanation:**
Assign IAM roles to the EC2 instance is correct. You need to use IAM roles to pass credentials to the application in a secured way.

---

## Question 39

**Q:** You monitor your usage in AWS to increase or decrease resources based on current business requirements. This careful monitoring and response is taken to reduce costs. What model is being implemented according to the AWS Cost Optimization Pillar?

**Options:**
- (A) Production Model
- (B) Efficiency Model
- **(C) Consumption Model** [CORRECT]
- (D) Development Model

**Explanation:**
Consumption Model is the correct answer. AWS is continually releasing new services. In many cases, processes currently running in dedicated EC2 instances can be moved to the services and significantly reduce costs. S3 Standard may be too expensive for many storage requirements. EIPs incur a charge as they are static addresses and should only be used when a static address is required. Many EC2 instances do not require high availability and implementing redundant instances when they are not required increases costs.

---


