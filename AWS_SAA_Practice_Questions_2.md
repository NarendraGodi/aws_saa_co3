# AWS SAA-C03 Practice Questions - Part 2

Total Questions: 39

---

## Question 1

**Q:** What is the benefit of multipart upload?

**Options:**
- **(A) Greater success is achieved when uploading large files** [CORRECT]
- (B) Uploading multiple small files is faster
- (C) Support for concurrent application uploads is enabled
- (D) Network throughput is increased in every implementation

**Explanation:**
Greater success is achieved when uploading large files is the correct answer. When uploading large files (AWS recommends its use for files larger than 100 MB), successful uploads are increased. It does not provide benefit with multiple small files, concurrent application access, or increased network throughput in most scenarios.

---

## Question 2

**Q:** What can be used to provide temporary access to perform a specific function within AWS and that will automatically expire without further action?

**Options:**
- **(A) Role** [CORRECT]
- (B) ACL
- (C) Standard group
- (D) Standard login

**Explanation:**
Role is the correct answer. Roles can be used as temporary identities. By default the granted role expires after 12 hours. While a standard login (user) could be used, it would not expire automatically. Groups also provide no solution to this scenario and neither do ACLs.

---

## Question 3

**Q:** You are creating a data lake in AWS, and one of the use cases for the data lake is batch jobs. Which AWS service would you use to ingest the data for batch jobs?

**Options:**
- (A) AWS Lambda
- (B) Kinesis Analytics
- (C) Kinesis Streams
- **(D) Kinesis Firehose** [CORRECT]

**Explanation:**
Kinesis Firehose is correct. Since the use case is batch jobs, Kinesis Firehose should be used for data ingestion. 

---

## Question 4

**Q:** You are a consultant planning to deploy DynamoDB across three AZs. Your lead DBA is concerned about data consistency. Which of the following do you advise the lead DBA to do?

**Options:**
- (A) Ask the development team to code a maintenance task to run on a schedule to check consistency.
- (B) Ask the development team to write code to check for a successful completion code (200) at the completion of every write.
- (C) Ask the development team to code for strongly consistent reads, as this will impact the read times slightly but not the budget.
- **(D) Ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost.** [CORRECT]

**Explanation:**
Ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost is correct. It is important to code for strong consistency. If you don’t code for strong consistency, you will end up having stale data, and depending on what you are trying to do, this may have an impact since you won’t be able to make decisions on real-time data. 

---

## Question 5

**Q:** What can you monitor to see if a T2 database instance should be upgraded to an R3 instance?

**Options:**
- (A) Memory allowance
- (B) CPU allowance
- (C) Memory credits
- **(D) CPU credits** [CORRECT]

**Explanation:**
CPU credits is the correct answer. By monitoring CPU credits you can determine if you're reaching a low level of credits. When a low level of credits is reached, you risk running out of credits and, in such an instance, performance will degrade significantly.

---

## Question 6

**Q:** How does AWS deliver high durability for DynamoDB?

**Options:**
- (A) AWS maintains a schedule of incremental backups and log shipping.
- **(B) DynamoDB data is automatically replicated across multiple AZs.** [CORRECT]
- (C) DynamoDB supports user snapshots to S3.
- (D) DynamoDB is a NoSQL database.

**Explanation:**
DynamoDB data is automatically replicated across multiple AZs is correct. DynamoDB tables are automatically replicated across multiple AZs. This is offered free of cost to customers.

---

## Question 7

**Q:** When implementing ELB, what should you ensure such that high availability is achieved?

**Options:**
- **(A) Resources are in multiple Availability Zones** [CORRECT]
- (B) Resources are in one region
- (C) ELB is implemented in one region
- (D) ELB is implemented in one Availability Zone

**Explanation:**
Resources are in multiple Availability Zones is correct. By implementing resources to which ELB will forward requests in multiple Availability Zones, you ensure high availability. ELB provides Elastic Load Balancing.

---

## Question 8

**Q:** What tool is provided by AWS to compare the cost of locally-implemented solutions with AWS cloud-hosted solutions?

**Options:**
- (A) AWS Trusted Advisor
- (B) AWS Simple Monthly Calculator
- **(C) AWS TCO Calculator** [CORRECT]
- (D) AWS Budget

**Explanation:**
AWS TCO Calculator is correct. The AWS Total Cost of Ownership (TCO) Calculator asks you to input the components needed to host a solution internally and then provides a cost comparison between hosting locally and in AWS. The AWS Simple Monthly Calculator allows you to calculate the cost of a specified solution in AWS alone. The Trusted Advisor provides suggestions for enhanced security, performance, and cost reduction. The AWS Budget service allows you to configure budgets and alerts for when budgets are or may be exceeded.

---

## Question 9

**Q:** When should RDS backups occur for best performance results?

**Options:**
- (A) During times of zero activity
- (B) During the busiest time of the day
- **(C) During times of normally low write IOPS** [CORRECT]
- (D) During times of medium read operations

**Explanation:**
During times of normally low write IOPS is correct. Because few database systems that are placed online have times of zero activity, the best time window to search for is that in which low write IOPS are seen traditionally.

---

## Question 10

**Q:** How is the public IP address managed in an instance session via the instance GUI/RDP or Terminal/SSH session?

**Options:**
- **(A) The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address.** [CORRECT]
- (B) For security reasons, the public IP address is a hidden value.
- (C) The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/local-ipv4.
- (D) The public IP address can be managed via the instance MetaData at http://169.254.169.254/latest/meta-data/public-ipv4.

**Explanation:**
The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address is correct. When you manage the public IP address in an instance session via the instance GUI/RDP or Terminal/SSH session, it is not managed on the instance. In this case, an alias is applied as a network address translator of the private IP address. 

---

## Question 11

**Q:** What kind of storage is used with EBS volumes?

**Options:**
- **(A) Block storage** [CORRECT]
- (B) Only magnetic disk storage
- (C) Object storage
- (D) Only SSD storage

**Explanation:**
Block storage is the correct answer. Block storage is used by Elastic Block Store (EBS). Object storage is used by S3. SSD and magnetic disk are both options for EBS, with SSD storage being faster.

---

## Question 12

**Q:** You receive a ProvisionedThroughputExceededException error. However, the DynamoDB metrics show that your table or index has not been operating at maximum provisioned throughput. What could this error be caused by?

**Options:**
- (A) The error is caused by excess traffic generated by your local secondary indexes. You should provision units specifically to the local secondary indexes.
- (B) It is only a warning. DynamoDB’s burst capacity will handle the extra traffic.
- (C) It is a transitory error. AWS will adjust the table to accommodate it and reprocess the transaction.
- **(D) The throughput is not balanced across your partitions. One partition is being subjected to a disproportionate amount of the traffic and is therefore exceeding the limits.** [CORRECT]

**Explanation:**
The throughput is not balanced across your partitions. One partition is being subjected to a disproportionate amount of the traffic and is therefore exceeding the limits is correct. In DynamoDB, it is possible that one of the partitions of the table get more traffic whereas others get less traffic. If one partition is getting massive traffic, you will get a ProvisionedThroughputExceededException error. Since the other partitions are not getting a lot of traffic, when you do the average of IO across the partitions for a table, it will not show you are operating at maximum provisioned throughput.   

---

## Question 13

**Q:** Which instance type runs on hardware allocated to a single customer?

**Options:**
- (A) Reserved instance
- (B) On Demand instance
- **(C) Dedicated instance** [CORRECT]
- (D) EC2 spot instance

**Explanation:**
Dedicated instance is correct. A dedicated instance runs on hardware allocated to a single customer. The dedicated instances are physically isolated at the host hardware level from instances that belong to other AWS accounts.

---

## Question 14

**Q:** What HTTP response is given upon a successful upload of a file to an S3 bucket?

**Options:**
- **(A) 200** [CORRECT]
- (B) 500
- (C) 400
- (D) 300

**Explanation:**
200 is the correct answer. HTTP 200 is the success response code. HTTP 500 indicates an internal server error. HTTP 300 indicates a redirect of some kind. HTTP 400 is a missing object response code.

---

## Question 15

**Q:** What is used to cache, or store, data and connect with S3 buckets from the on-premises customer location?

**Options:**
- **(A) Storage gateway** [CORRECT]
- (B) NAC gateway
- (C) Customer gateway
- (D) Virtual private gateway

**Explanation:**
Storage gateway is the correct answer. The storage gateway is used to connect the customer location to an S3 bucket and to cache and store data locally for faster access. The customer and virtual private gateways are used to establish VPNs. No such entity as a NAC gateway exists in association with AWS.

---

## Question 16

**Q:** You want to perform business analytics against a large data set (several terabytes). What AWS-managed service provides such functionality?

**Options:**
- (A) DynamoDB
- (B) ElastiCache
- (C) CodeDeploy
- **(D) Redshift** [CORRECT]

**Explanation:**
Redshift is the correct answer. Redshift is the AWS managed OLAP (business intelligence/analytics) solution. DynamoDB is not designed for OLAP operations. ElastiCache is in-memory caching. CodeDeploy is used to deploy application code in stages or phases.

---

## Question 17

**Q:** Even if all best practices are being followed in IAM administration, what can present vulnerabilities related to your EC2 instances?

**Options:**
- (A) Improper IAM group usage
- (B) Improper IAM user account creation
- **(C) OS security issues within the instances** [CORRECT]
- (D) Improper IAM role usage

**Explanation:**
OS security issues within the instances is the correct answer. Even when best practices are followed in IAM, as it is focused on securing access to the AWS cloud, the OSes running within your EC2 instances can still present security issues. Given that the question specified the use of best practices in IAM, the improper IAM options are invalid.

---

## Question 18

**Q:** For what purpose is the Elastic Transcoder used?

**Options:**
- (A) To recode text submitted to S3 buckets
- (B) To convert currencies from different nations
- (C) To stream video to client devices from the cloud
- **(D) To convert media formats and sizes for different target devices and systems** [CORRECT]

**Explanation:**
To convert media formats and sizes for different target devices and systems is the correct answer. The Elastic Transcoder is a media transcoder in the cloud. It can convert to different media formats and sizes so that media is available for various target devices and systems.

---

## Question 19

**Q:** What is likely to occur during the time required to take a snapshot of a Cold HDD or Throughput-Optimized HDD EBS volume?

**Options:**
- **(A) Performance will be degraded** [CORRECT]
- (B) Data will be lost
- (C) Performance will be improved
- (D) Data will be decrypted

**Explanation:**
Performance will be degraded is the correct answer. During the creation of the snapshot on magnetic storage, performance will be degraded due to the method used to access the blocks. Data will not be decrypted or lost.

---

## Question 20

**Q:** Your company has hired a young and enthusiastic accountant. After reviewing the AWS documentation and usage graphs, he announces that you are wasting vast amounts of the company’s money running servers for a full hour instead of spinning them up only when they are needed and down again as soon as they are idle for 1 minute. He cites the AWS claim that you only pay for what you use, and that as a senior engineer, you should be more conscious of wasting company money. How do you respond?

**Options:**
- **(A) You thank him for his concern and then implement EC2’s pay-per-minute billing to get the maximum benefit for the company.** [CORRECT]
- (B) You leap across the meeting table and slap him for insulting you in front of your peers.
- (C) You grudgingly acknowledge his point and change your scheduling and tuning settings.
- (D) You acknowledge the problem and propose that you could downsize the instances so that the workload consumes the full instance capacity for the full hour. You also propose closer monitoring and automation so that you can upsize and/or downsize the instance each hour during the day to match the instance performance to the anticipated workload.

**Explanation:**
You thank him for his concern and then implement EC2’s pay-per-minute billing to get the maximum benefit for the company is correct. AWS has launched a new feature called pay-per-minute, where the billing occurs in increments of 60 seconds for certain types of instances. If cost control is one of your main objectives, it makes sense to stop the instance whenever it is not in use. 

---

## Question 21

**Q:** What AWS service allows you to run code in the AWS cloud without provisioning any of the underlying resources required for code execution?

**Options:**
- (A) Aurora
- (B) VPC
- (C) EC2
- **(D) Lambda** [CORRECT]

**Explanation:**
Lambda is the correct answer. Lambda is an AWS service that allows you to execute code without provisioning resources. Aurora is an AWS database. Virtual Private Cloud (VPC) is a container in which you place instances and control access to them. EC2 is used to launch AMI instances within VPCs in AWS.

---

## Question 22

**Q:** How much data can be downloaded from an S3 bucket to your local network with no transfer charges?

**Options:**
- (A) From 1 GB/Month to 9.999 TB/Month
- **(B) Up to 1 GB/Month** [CORRECT]
- (C) From 10 TB/Month to 40 TB/Month
- (D) From 40 TB/Month to 100 TB/Month

**Explanation:**
Up to 1GB/Month is the correct answer. There is no cost for uploading to EC2 instances from the Internet (your local network); however, there is a cost for downloading to the Internet (your local network). For example, with approximately 100 GB of transfer down to your local network per month, the cost would be approximately $9 per month in 2020. There is no cost for encryption/decryption that can be estimated beyond increase compute cycles, which are typically minimal.

---

## Question 23

**Q:** What is the minimum volume size of a Provisioned IOPS SSD EBS volume?

**Options:**
- **(A) 4 GiB** [CORRECT]
- (B) 16 TiB
- (C) 1 TiB
- (D) 12 GiB

**Explanation:**
The correct answer is 4 GiB. The minimum Provisioned IOPS volume size is four GiB and the maximum is 16 TiB.

---

## Question 24

**Q:** What is the default rule in a NACL created within AWS?

**Options:**
- (A) Disallow all traffic
- **(B) Allow all traffic in and out** [CORRECT]
- (C) Allow all traffic out and no traffic in
- (D) Allow all traffic in and no traffic out

**Explanation:**
Allow all traffic in and out is the correct answer. The default NACL rule is to allow all traffic in and out of the subnet to which the NACL is applied.

---

## Question 25

**Q:** To what are security groups applied within an AWS IAM managed solution?

**Options:**
- (A) Subnets
- (B) Groups
- (C) Users
- **(D) Network interfaces** [CORRECT]

**Explanation:**
 used in AWS IAM for user management are simply called groups and not security groups. This can be a point of confusion for many new users of AWS.

---

## Question 26

**Q:** What login has the ability to cancel an AWS subscription?

**Options:**
- (A) Any login
- (B) Any account admin login
- (C) Any admin login
- **(D) Root login** [CORRECT]

**Explanation:**
Root login is the correct answer. Only the root login can change the AWS support plan, cancel the account, open a billing support case, and perform several other account-related actions. For this reason, the root login should be secured and used only when these actions are required. The first action taken when creating an AWS account should be the creation of another login for all other administrative actions.

---

## Question 27

**Q:** What is the default rule that exists in security groups?

**Options:**
- (A) Allow all encrypted traffic
- (B) Allow all inbound traffic
- (C) Allow all unencrypted traffic
- **(D) Allow all outbound traffic** [CORRECT]

**Explanation:**
Allow all outbound traffic is the correct answer. By default, security groups allow all outbound traffic. You must create additional rules to allow inbound traffic. If you do not wish to allow all outbound traffic, you must remove the default rule and replace it with one allowing only the desired outbound traffic.

---

## Question 28

**Q:** You have implemented a read replica instance for a MySQL database. What should you communicate to the users in relation to how they will access the read replica?

**Options:**
- (A) Read replicas are accessed through special application APIs
- (B) Read replicas cannot be directly accessed, but are accessed by performing a read operation on the parent database instance
- **(C) Read replicas are accessed the same as any other database in RDS** [CORRECT]
- (D) Read replicas are accessed using a unique 256-bit SHA-1 key

**Explanation:**
Read replicas are accessed the same as any other database in RDS is the correct answer. A read replica exists as a normal database from the access perspective. Users will access it directly like any other RDS database; however, they can only perform read operations against it. No new required methods exist for accessing the read replica over those required to access any other RDS database.

---

## Question 29

**Q:** Your AWS environment contains several on-demand EC2 instances dedicated to a project that has just been cancelled. Your supervisor does not want to incur charges for these on-demand instances, but also does not want to lose the data just yet because there is a chance the project may be revived in the next few days. What should you do to minimize charges for these instances in the meantime?

**Options:**
- **(A) Stop the instances.** [CORRECT]
- (B) Contact AWS Support and put the instances on courtesy hold.
- (C) Create AMIs from the instances and put them on the AWS Marketplace in hopes of recovering some of the cost.
- (D) Terminate the instances.

**Explanation:**
Stop the instances is correct. When the data is stored in EBS volumes, it will be stored even if the instances are stopped. The EBS volumes persist the data, so it will always be there. On the other hand, if the data is stored in the instance store and you shut down the instance, you lose everything. 

---

## Question 30

**Q:** What common security standard is IAM in compliance with that allows for credit card data to be processed?

**Options:**
- (A) GDPR
- (B) HIPAA
- (C) GLBA
- **(D) PCI-DSS** [CORRECT]

**Explanation:**
PCI-DSS is the correct answer. The Payment Card Industry-Data Security Standard (PCI-DSS) specified operational procedures and methods to support secure payment card processing and IAM complies with this standard. HIPAA is related to health information privacy. GLBA is about financial accounting. GDPR is a European Union privacy standard.

---

## Question 31

**Q:** Why might you choose a specific region when creating an S3 bucket rather than accepting a default region?

**Options:**
- **(A) To place the bucket closer to the users for improved performance** [CORRECT]
- (B) To ensure permissions can be configured on the bucket
- (C) To ensure the data is stored with encryption
- (D) To place the bucket closer to AWS headquarters for improved performance

**Explanation:**
To place the bucket closer to the users for improved performance is the correct answer. By selecting a region closer to the primary users of the bucket, you can enhance performance for those users. Encryption and permissions may be configured regardless of where the bucket is physically stored. Placing it closer to AWS HQ will provide no benefit to you, unless, of course, you work at AWS HQ.

---

## Question 32

**Q:** What IAM account is accessed using an e-mail address and has unlimited permissions within AWS?

**Options:**
- (A) All administrator users
- (B) Any user in a group
- **(C) Root user** [CORRECT]
- (D) Standard created user

**Explanation:**
Root user is the correct answer. The root user account can do anything in relation to the AWS account and is accessed by logging in with the e-mail address used to create the account. As a best practice, this account should not be used for daily administration and should have multi-factor authentication (MFA) enabled.

---

## Question 33

**Q:** Which file sizes generally provide for faster access per megabyte when using EFS and why?

**Options:**
- (A) Small file sizes because the time to access small file locations is less than the time to access large file locations
- **(B) Large file sizes because the time to access the file location is the same regardless of file size** [CORRECT]
- (C) Large file sizes because the drives spin faster and faster as the file is accessed
- (D) Small file sizes because they are often read in a single spin of the disk

**Explanation:**
Large file sizes because the time to access the file location is the same regardless of file size is the correct answer. To understand the answer to this question, you must remember that EFS distributes files for availability and durability. The result is that the files must be located before they are accessed. Therefore, performance per megabyte will increase when accessing larger files as the file location time is lessened in comparison to total file access time.

---

## Question 34

**Q:** You want to implement an Oracle database in AWS. What managed service in AWS allows you to do this in the least expensive way?

**Options:**
- (A) Aurora
- **(B) RDS** [CORRECT]
- (C) Redshift
- (D) EC2

**Explanation:**
RDS is the correct answer. RDS is the Relational Database Service and it supports Oracle databases run in the managed service. Redshift and Aurora are specific AWS databases and are not compatible with Oracle databases. EC2 instances could be used by installing the OS and Oracle database server, but it is not a managed service like RDS.

---

## Question 35

**Q:** You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?

**Options:**
- (A) Aurora
- (B) MySQL
- (C) DynamoDB
- **(D) S3** [CORRECT]

**Explanation:**
S3 is the correct answer. Because you desire to use the data without conversion, it cannot be converted to any database structure, such as Aurora, DynamoDB, or MySQL. Therefore, the best option among those listed is S3.

---

## Question 36

**Q:** When creating NACLs within AWS, why is the rule order so important?

**Options:**
- **(A) Because the first matching rule applies** [CORRECT]
- (B) Because deny rules must be placed before permit or allow rules
- (C) Because they must be entered in the order of TCP or UDP ports
- (D) Because they must be entered in the order of IP addresses

**Explanation:**
Because the matching rule applies is the correct answer. When processing a Network Access Control List (NACL), the AWS system applies the first rule that matches, starting with the lowest numbered rule first. Therefore, the rules must be numbered in an order that will ensure an allowance or denial that should always be applied if higher in the list (by having a lower number).

---

## Question 37

**Q:** What service within AWS provides for DNS name management and resolution?

**Options:**
- (A) Route 47
- **(B) Route 53** [CORRECT]
- (C) Kinesis
- (D) ENI

**Explanation:**
Route 53 is the correct answer. Route 53 is the AWS DNS service. ENI is the Elastic Network Interface, which may be attached to an instance and provided an Elastic IP (EIP) address, which is routable on the Internet. Kinesis is for working with real-time data streams. Route 47 does not exist in AWS.

---

## Question 38

**Q:** You must implement an S3 storage solution that encrypts data at rest in the S3 buckets. Which S3 storage class supports at-rest data encryption?

**Options:**
- (A) S3-Standard
- (B) S3-One Zone-IA
- **(C) All of these** [CORRECT]
- (D) S3-IA

**Explanation:**
All of these answers are correct. All S3 storage classes support at-rest data encryption. Additionally, SSL may be used for encryption during transmission as data is placed into the S3 buckets or read from the S3 buckets.

---

## Question 39

**Q:** You are planning an EFS implementation in AWS. You are uncertain how many files will be created and the total storage space required. What should you specify as the allocated EFS storage space?

**Options:**
- (A) 1 TB
- **(B) You do not specify storage space allocation when creating an EFS file system** [CORRECT]
- (C) 100 GB
- (D) 100 MB

**Explanation:**
You do not specify storage space allocation when creating an EFS file system is the correct answer. When implementing EFS, you do not specify the amount of storage space. This is why it is called elastic (the Elastic File System). The file system will grow as required to accommodate the files stored and you pay for the storage consumed.

---


