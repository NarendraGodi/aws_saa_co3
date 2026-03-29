# AWS SAA-C03 Practice Questions - Part 1

Total Questions: 195

---

## Question 1

**Q:** To use a custom domain name and URL when hosting a static website in a bucket, what two services of AWS are required?

**A:** S3 and Route 53

---

## Question 2

**Q:** You are implementing an ELB solution. You want to ensure high availability. Where should the resources to which ELB directs be located?

**A:** In different Availability Zones

---

## Question 3

**Q:** You have been asked to host a static website in AWS as quickly as possible. What is the simplest solution to use?

**A:** S3

---

## Question 4

**Q:** You have implemented a NACL and notice that return traffic from an internal request is not allowed. Why is this happening?

**A:** NACLs are stateless

---

## Question 5

**Q:** You have been asked to provide a folder-like structure in S3 buckets. How can this be accomplished?

**A:** Using prefixes and delimiters

---

## Question 6

**Q:** Where are AWS Cost and Usage Reports stored?

**A:** S3 bucket

---

## Question 7

**Q:** What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?

**A:** Trusted Advisor

---

## Question 8

**Q:** What two caching engines are supported by ElastiCache?

**A:** Redis and memcached

---

## Question 9

**Q:** In addition to inbound and outbound rules, what type of rule does a security group allow?

**A:** Allow rules

---

## Question 10

**Q:** When should you use a dedicated host for an EC2 instance?

**A:** When you require a license to be locked to the hardware

---

## Question 11

**Q:** In the event of loss of access to an Availability Zone for any reason, which S3 storage class does not provide resiliency?

**A:** S3 One Zone-Infrequent Access

---

## Question 12

**Q:** When you’re editing permissions (policies and ACLs), to whom does the concept of the “owner” refer?

**A:** “Owner” refers to the identity and e-mail address used to create the AWS account.

---

## Question 13

**Q:** You are running a Mongo database that requires access to tens of thousands of low-latency IOPS. Which of the following EC2 instance families would best suit your needs?

**A:** High I/O instances

---

## Question 14

**Q:** What can be used to aggregate several AWS accounts for centralized management and billing tracking?

**A:** AWS Organizations

---

## Question 15

**Q:** You have a small database workload with infrequent I/O. These databases are mainly used as ad hoc databases for noncritical testing purposes. Which storage medium would be the most cost-effective way to meet these requirements?

**A:** Amazon RDS Magnetic Storage

---

## Question 16

**Q:** Which one of the following is controlled by a security group attached to an instance?

**A:** Inbound traffic

---

## Question 17

**Q:** You have several Windows and Linux instances within a single subnet in a VPC. You want to ensure that no inbound traffic can reach the Windows instances. What is the best option?

**A:** Security Groups

---

## Question 18

**Q:** What is the default limit on the number of S3 buckets that can be created by an account?

**A:** 100

---

## Question 19

**Q:** You must select the S3 storage class with the highest level of resiliency. Which class do you choose?

**A:** S3 Standard

---

## Question 20

**Q:** What can be used to assign permissions to more than one user login without having to modify each login individually?

**A:** Groups

---

## Question 21

**Q:** What is the default duration of cost history shown in the Cost Explorer view of AWS?

**A:** 6 months

---

## Question 22

**Q:** Which one of the following RDS database types does not support read replicas?

**A:** Aurora

---

## Question 23

**Q:** You’ve been tasked with implementing a globally accessible storage solution that will scale from a few terabytes (now) to an unknown, but significantly greater, volume of data in three years’ time. You don’t want to spend a lot of money. Which AWS service would best meet your current and projected storage needs and at the same time make sure the cost is minimal?

**A:** S3

---

## Question 24

**Q:** HTTP is used to upload to S3 buckets. Which HTTP method has eventual consistency with S3 bucket writes?

**A:** Deletes

---

## Question 25

**Q:** What is the model used within AWS wherein AWS guarantees the secure operation of the cloud and the customer ensures the security of that which is placed in the cloud?

**A:** Shared Responsibility

---

## Question 26

**Q:** Although your application customarily runs at 30% usage, you have identified a recurring usage spike (greater than 90% usage) between 8 p.m. and midnight daily. What is the most cost-effective way to scale your application to meet this increased need?

**A:** Use proactive cyclic scaling to boost your capacity at a fixed interval.

---

## Question 27

**Q:** You have been asked to implement a read replica RDS setup. What is the primary purpose of such a configuration?

**A:** Performance

---

## Question 28

**Q:** What should be implemented when microsecond response time is required of a DynamoDB implementation?

**A:** DAX

---

## Question 29

**Q:** What is used to control network traffic at the subnet level in AWS?

**A:** Network ACLs (NACLs)

---

## Question 30

**Q:** When does Amazon recommend using the db.t2.small and db.t2.medium database instances with the Aurora database service?

**A:** For development and test servers

---

## Question 31

**Q:** You are working with AWS AMIs. What kind of AMI should be used when you want to customize an image and then reuse it to scale up a deployment?

**A:** Private AMI

---

## Question 32

**Q:** What instance type family is best used when things like specialized GPUs or FPGAs are required?

**A:** Accelerated computing

---

## Question 33

**Q:** You have been given control of an existing AWS environment (account). You want to ensure costs are being managed well. What tool should you run?

**A:** Trusted Advisor

---

## Question 34

**Q:** Which one of the following is not something for which AWS Trusted Advisor makes recommendations?

**A:** Scalability

---

## Question 35

**Q:** You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?

**A:** AWS Budget alerts

---

## Question 36

**Q:** What AWS database solution is best suited for data warehouse implementations?

**A:** Redshift

---

## Question 37

**Q:** In addition to the proper configuration of RDS database settings, what can be done to improve overall performance of database operations?

**A:** Tune SQL queries

---

## Question 38

**Q:** Which one of the following components is used at a customer location to implement a site-to-site VPN connection with AWS?

**A:** Customer gateway

---

## Question 39

**Q:** Which one of the following storage methods is object-based?

**A:** S3 Standard

---

## Question 40

**Q:** What is the benefit of multipart upload?

**A:** Greater success is achieved when uploading large files

---

## Question 41

**Q:** What can be used to provide temporary access to perform a specific function within AWS and that will automatically expire without further action?

**A:** Role

---

## Question 42

**Q:** You are creating a data lake in AWS, and one of the use cases for the data lake is batch jobs. Which AWS service would you use to ingest the data for batch jobs?

**A:** Kinesis Firehose

---

## Question 43

**Q:** You are a consultant planning to deploy DynamoDB across three AZs. Your lead DBA is concerned about data consistency. Which of the following do you advise the lead DBA to do?

**A:** Ask the development team to code for strongly consistent reads. As the consultant, you will advise the CTO of the increased cost.

---

## Question 44

**Q:** What can you monitor to see if a T2 database instance should be upgraded to an R3 instance?

**A:** CPU credits

---

## Question 45

**Q:** How does AWS deliver high durability for DynamoDB?

**A:** DynamoDB data is automatically replicated across multiple AZs.

---

## Question 46

**Q:** When implementing ELB, what should you ensure such that high availability is achieved?

**A:** Resources are in multiple Availability Zones

---

## Question 47

**Q:** What tool is provided by AWS to compare the cost of locally-implemented solutions with AWS cloud-hosted solutions?

**A:** AWS TCO Calculator

---

## Question 48

**Q:** When should RDS backups occur for best performance results?

**A:** During times of normally low write IOPS

---

## Question 49

**Q:** How is the public IP address managed in an instance session via the instance GUI/RDP or Terminal/SSH session?

**A:** The public IP address is not managed on the instance; instead, it is an alias applied as a network address translation of the private IP address.

---

## Question 50

**Q:** What kind of storage is used with EBS volumes?

**A:** Block storage

---

## Question 51

**Q:** You receive a ProvisionedThroughputExceededException error. However, the DynamoDB metrics show that your table or index has not been operating at maximum provisioned throughput. What could this error be caused by?

**A:** The throughput is not balanced across your partitions. One partition is being subjected to a disproportionate amount of the traffic and is therefore exceeding the limits.

---

## Question 52

**Q:** Which instance type runs on hardware allocated to a single customer?

**A:** Dedicated instance

---

## Question 53

**Q:** What HTTP response is given upon a successful upload of a file to an S3 bucket?

**A:** 200

---

## Question 54

**Q:** What is used to cache, or store, data and connect with S3 buckets from the on-premises customer location?

**A:** Storage gateway

---

## Question 55

**Q:** You want to perform business analytics against a large data set (several terabytes). What AWS-managed service provides such functionality?

**A:** Redshift

---

## Question 56

**Q:** Even if all best practices are being followed in IAM administration, what can present vulnerabilities related to your EC2 instances?

**A:** OS security issues within the instances

---

## Question 57

**Q:** For what purpose is the Elastic Transcoder used?

**A:** To convert media formats and sizes for different target devices and systems

---

## Question 58

**Q:** What is likely to occur during the time required to take a snapshot of a Cold HDD or Throughput-Optimized HDD EBS volume?

**A:** Performance will be degraded

---

## Question 59

**Q:** You are responsible for planning EFS implementation in AWS. What is the default limit on the number of EFS file systems that can be created per account?

**A:** 10

---

## Question 60

**Q:** Your company has hired a young and enthusiastic accountant. After reviewing the AWS documentation and usage graphs, he announces that you are wasting vast amounts of the company’s money running servers for a full hour instead of spinning them up only when they are needed and down again as soon as they are idle for 1 minute. He cites the AWS claim that you only pay for what you use, and that as a senior engineer, you should be more conscious of wasting company money. How do you respond?

**A:** You thank him for his concern and then implement EC2’s pay-per-minute billing to get the maximum benefit for the company.

---

## Question 61

**Q:** What AWS service allows you to run code in the AWS cloud without provisioning any of the underlying resources required for code execution?

**A:** Lambda

---

## Question 62

**Q:** How much data can be downloaded from an S3 bucket to your local network with no transfer charges?

**A:** Up to 1 GB/Month

---

## Question 63

**Q:** What is the minimum volume size of a Provisioned IOPS SSD EBS volume?

**A:** 4 GiB

---

## Question 64

**Q:** Set up a Flow Log for the group of instances and forward them to S3 is incorrect because if you forward instances to S3, how do you use the information?

**A:** Allow all traffic in and out

---

## Question 65

**Q:** What is the default rule in a NACL created within AWS?

**A:** Allow all traffic in and out

---

## Question 66

**Q:** To what are security groups applied within an AWS IAM managed solution?

**A:** Network interfaces

---

## Question 67

**Q:** What login has the ability to cancel an AWS subscription?

**A:** Root login

---

## Question 68

**Q:** What is the default rule that exists in security groups?

**A:** Allow all outbound traffic

---

## Question 69

**Q:** You have implemented a read replica instance for a MySQL database. What should you communicate to the users in relation to how they will access the read replica?

**A:** Read replicas are accessed the same as any other database in RDS

---

## Question 70

**Q:** Your AWS environment contains several on-demand EC2 instances dedicated to a project that has just been cancelled. Your supervisor does not want to incur charges for these on-demand instances, but also does not want to lose the data just yet because there is a chance the project may be revived in the next few days. What should you do to minimize charges for these instances in the meantime?

**A:** Stop the instances.

---

## Question 71

**Q:** What common security standard is IAM in compliance with that allows for credit card data to be processed?

**A:** PCI-DSS

---

## Question 72

**Q:** Why might you choose a specific region when creating an S3 bucket rather than accepting a default region?

**A:** To place the bucket closer to the users for improved performance

---

## Question 73

**Q:** What IAM account is accessed using an e-mail address and has unlimited permissions within AWS?

**A:** Root user

---

## Question 74

**Q:** Which file sizes generally provide for faster access per megabyte when using EFS and why?

**A:** Large file sizes because the time to access the file location is the same regardless of file size

---

## Question 75

**Q:** You want to implement an Oracle database in AWS. What managed service in AWS allows you to do this in the least expensive way?

**A:** RDS

---

## Question 76

**Q:** You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?

**A:** S3

---

## Question 77

**Q:** When creating NACLs within AWS, why is the rule order so important?

**A:** Because the first matching rule applies

---

## Question 78

**Q:** What service within AWS provides for DNS name management and resolution?

**A:** Route 53

---

## Question 79

**Q:** You must implement an S3 storage solution that encrypts data at rest in the S3 buckets. Which S3 storage class supports at-rest data encryption?

**A:** All of these

---

## Question 80

**Q:** You are planning an EFS implementation in AWS. You are uncertain how many files will be created and the total storage space required. What should you specify as the allocated EFS storage space?

**A:** You do not specify storage space allocation when creating an EFS file system

---

## Question 81

**Q:** What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?

**A:** Access Key ID/Secret Access Key

---

## Question 82

**Q:** Scenario: You are using large-scale databases and intensive processing EC2 instances. If you know the amount of resources required for one year or more for an AWS EC2 instance or RDS database, what can be utilized to reduce costs by 40% or more?

**A:** Reserved pricing

---

## Question 83

**Q:** What can be configured to optimize EFS performance in relation to NFS mount options?

**A:** Use NFSv4.1

---

## Question 84

**Q:** What is the up-front cost incurred by creating S3 buckets?

**A:** $0

---

## Question 85

**Q:** How should you enforce the use of an 8-character password for all AWS logins?

**A:** Through a password policy

---

## Question 86

**Q:** What solution is the least expensive, within AWS, for long-term data storage and archives?

**A:** Glacier

---

## Question 87

**Q:** Which one of the following languages is not supported by Elastic Beanstalk?

**A:** Perl

---

## Question 88

**Q:** Given that Elastic Beanstalk automatically creates the environment to run your application code, what is the extra cost associated with its use?

**A:** No extra cost

---

## Question 89

**Q:** To how many maximum elements can a single EC2 instance be attached?

**A:** 28

---

## Question 90

**Q:** What EC2 instance type can be used to provide up to a 90% discount off on-demand instance prices?

**A:** Spot instance

---

## Question 91

**Q:** To audit the API calls made to your account, which AWS service would you use?

**A:** AWS CloudTrail

---

## Question 92

**Q:** What should be implemented to ensure security when using AWS Access Keys?

**A:** Key Rotation

---

## Question 93

**Q:** What cannot be specified for an S3 bucket?

**A:** The Availability Zone (AZ)

---

## Question 94

**Q:** You have been engaged by a company to design and lead a migration to an AWS environment. The team is concerned about the capabilities of the new environment, especially when it comes to avoiding all bottlenecks. The design calls for about 20 instances (C3.2xLarge) pulling jobs/messages from SQS. Network traffic per instance is estimated to be around 500Mbps at the beginning and end of each job. Which network configuration should you plan on deploying?

**A:** Spread the instances over multiple AZs to minimize the traffic concentration and maximize the fault tolerance.

---

## Question 95

**Q:** You must transfer one exabyte of data into AWS and you do not want to transfer it across the Internet. What AWS solution should you use?

**A:** Snowmobile

---

## Question 96

**Q:** You must attach an EBS volume to an EC2 instance that offers 500 GiB of storage at the lowest cost. What EBS type should be used?

**A:** Cold HDD

---

## Question 97

**Q:** In addition to database instance class and redundancy options (such as Multi-AZ configurations), what has the most significant impact on the direct cost for RDS databases?

**A:** The database engine in use

---

## Question 98

**Q:** You must plan a Route 53 deployment in AWS. What routing policy is used to send all traffic to a single resource?

**A:** Simple routing

---

## Question 99

**Q:** When policies can be written in a language in AWS, what language is most often used?

**A:** JSON

---

## Question 100

**Q:** What can be easily implemented to segregate a group of servers from the rest of your AWS cloud so that the servers can communicate with each other and the Internet, but not with other servers in your cloud?

**A:** VPC

---

## Question 101

**Q:** What is the default upload operation type for data transferred to an S3 bucket?

**A:** A single PUT operation

---

## Question 102

**Q:** You want to provide multiple virtual hard disks to an EC2 instance. What can you attach to an instance to provide these virtual hard disks?

**A:** EBS volume

---

## Question 103

**Q:** Which one of the following resources cannot be automatically scaled with AWS Auto Scaling?

**A:** Microsoft SQL Server RDS databases

---

## Question 104

**Q:** What is a security best practice that should be implemented for the root login immediately after creating an AWS account?

**A:** Enable MFA

---

## Question 105

**Q:** You have been monitoring a sensitive Auto Scaling group, and you expect it to scale in as you enter a period of downtime over the holiday. The Auto Scaling group is distributed over three AZs (AZ -A and AZ -B have two instances each, and AZ -C has three instances). All instances have different CPU and memory utilization levels and have been running for a different number of days. All instances come from different versions of a root AMI and have different numbers of sessions connected. Which instance will be the first to shut down?

**A:** The instance in AZ -C that has the oldest launch configuration will terminate first.

---

## Question 106

**Q:** You want to implement a multi-account AWS cloud deployment that more easily complies with business policies during implementation. You wish to implement guardrails that prevent users from taking specific actions that might breech security policies. What AWS service can provide this and works with organizations as well?

**A:** AWS Control Tower

---

## Question 107

**Q:** You have a MySQL database running on an EC2 instance in a private subnet. You can connect via SSH, but you are unable to apply updates to the database server via the NAT instance. What might you do to remedy this problem?

**A:** Ensure that “Source/Destination Checks” is disabled on the NAT instance.

---

## Question 108

**Q:** What is the solution for logging actions taken within the AWS cloud, such as creating resources, deleting resources, and reconfiguring resources?

**A:** CloudTrail

---

## Question 109

**Q:** You are implementing a web hosting architecture in AWS. Three EC2 instances are in use. The first is a web server, the second an application server, and the third is a database server. The web server communicates with the application server, but not with the database server. The application server communicates with the database server and the web server. Outside uses may access the web server directly, but they cannot access other servers. What kind of secure architecture are you implementing?

**A:** A multi-tier secure architecture

---

## Question 110

**Q:** You are working with roles. When changes are made to roles, when do they take effect?

**A:** Immediately

---

## Question 111

**Q:** You are reviewing Change Control requests and note a change designed to reduce wasted CPU cycles by increasing the value of the VisibilityTimeout attribute. What does this mean?

**A:** When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time.

---

## Question 112

**Q:** What can be implemented to prevent traffic from the network to your EC2 instance from impacting the performance of traffic between your EC2 instance and an attached EBS volume?

**A:** Implement EBS-optimized instances

---

## Question 113

**Q:** What is the primary difference between durability and availability as it related to AWS storage?

**A:** Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not

---

## Question 114

**Q:** What AWS service can be used to automate server scaling and configuration based on Chef or Puppet?

**A:** OpsWorks

---

## Question 115

**Q:** What cannot be accomplished with an EFS storage solution?

**A:** Connecting it to a Windows instance

---

## Question 116

**Q:** What is the maximum S3 PUTs per second rate supported in AWS?

**A:** 3500

---

## Question 117

**Q:** You are designing a password policy for IAM users. Which one of the following cannot be configured for password policies in the AWS Console?

**A:** Prevent passwords including the user’s last name

---

## Question 118

**Q:** You are considering the use of encryption for an EBS volume. When should the encryption be applied?

**A:** At the time the EBS volume is created

---

## Question 119

**Q:** What kind of storage is defined as data storage that persists only during the lifetime of an associated instance and that is lost when a drive fails, an instance stops, or an instance is terminated?

**A:** Instance store

---

## Question 120

**Q:** You successfully configure VPC peering between VPC-A and VPC-B. You then establish an IGW and a Direct-Connect connection in VPC-B. Can instances in VPC-A connect to your corporate office via the Direct-Connect service as well as connect to the Internet via the IGW?

**A:** No, VPC peering does not support edge-to-edge routing.

---

## Question 121

**Q:** You are responsible for implementing Amazon Kinesis Data Analytics. What language is used to process the data streams as they flow through the system?

**A:** SQL

---

## Question 122

**Q:** At the monthly product meeting, one of the product owners proposes an idea to address an immediate shortcoming of the product system: storing a copy of the customer price schedule in the customer record in the database. You know that you can store large text or binary objects in DynamoDB. You give a tentative OK to do a minimum viable product (MVP) test, but you stipulate that it must comply with the size limitation on the attribute name and value. Which is the correct limitation?

**A:** The value and name combined must not exceed 400KB.

---

## Question 123

**Q:** What is true about edge locations when using CloudFront?

**A:** They are read/write

---

## Question 124

**Q:** What AWS tool can be used to estimate the cost of storage for an AWS solution?

**A:** AWS Pricing Calculator

---

## Question 125

**Q:** You must transfer 40 TB of data into AWS S3 buckets. You are concerned about the time it will take to transfer the files over the network and the impact it will have on user performance. What is the best option for transferring such a large amount of data without impacting network user performance?

**A:** Snowball

---

## Question 126

**Q:** What is a primary difference between EFS and EBS storage in AWS?

**A:** EFS storage can be shared across regions and EBS cannot

---

## Question 127

**Q:** What important action may help to reduce costs of AWS operations over a long period of time?

**A:** Keep up to date with new AWS service releases

---

## Question 128

**Q:** You want to limit who can modify a NACL that is associated with a subnet. What can you use?

**A:** IAM

---

## Question 129

**Q:** What is the container used to store DNS records called in Route 53?

**A:** Hosted zone

---

## Question 130

**Q:** If you want all user requests made to a CloudFront configuration to force HTTPS instead of HTTP transfers, what should you do?

**A:** Configure the Protocol Policy to specify Redirect HTTP to HTTPS

---

## Question 131

**Q:** You are implementing a content delivery network (CDN) using Amazon CloudFront. What are the locations, distributed throughout the world, that contain the cached data called?

**A:** Edge locations

---

## Question 132

**Q:** What should the last rule be in a NACL that allows three protocols and disallows everything else?

**A:** All traffic/Deny

---

## Question 133

**Q:** Your company likes the idea of storing files on AWS. However, low-latency service of the majority of files is important to customer service. Which Storage Gateway configuration would you use to achieve both these ends?

**A:** Gateway-Stored

---

## Question 134

**Q:** You are creating a data lake, and one of the criteria you are looking for is faster performance. You want the ability to transform the data directly during the ingestion process to save time and cost. Which AWS service should you choose for this?

**A:** Use Kinesis Analytics for transforming the data.

---

## Question 135

**Q:** You must attach an EBS volume to an EC2 instance that offers the highest level of performance. What EBS type should be used?

**A:** Provisioned IOPS SSD

---

## Question 136

**Q:** What is the maximum VisibilityTimeout value of an SQS message in a FIFO queue?

**A:** 12 hours

---

## Question 137

**Q:** You have three Elastic Network Interfaces (ENIs). They are attached to three instances. You need an ENI for another instance and one of the instances currently using an ENI no longer needs it. What is the best action to take?

**A:** Move the ENI from the instance no longer needing it to the instance requiring it

---

## Question 138

**Q:** You are planning VPCs and want to document their functionality. How many Availability Zones within a region does a single VPC span?

**A:** All of them

---

## Question 139

**Q:** When storing data in EC2 instances, in addition to storage space requirements, what cost factor must be considered?

**A:** Data transfer costs (from AWS to your local network)

---

## Question 140

**Q:** You must implement an AWS solution that can expand and contract the number of server instances as needed. What AWS service provides this functionality?

**A:** Auto Scaling

---

## Question 141

**Q:** You must enable alerts and other notifications to be sent to the appropriate individuals from the AWS cloud. What AWS service can provide this function?

**A:** Amazon Simple Notification Service (SNS)

---

## Question 142

**Q:** What two methods are provided in AWS RDS for database backups?

**A:** Automated backups and automated snapshots

---

## Question 143

**Q:** When multiple resources can perform the same function, which one of the following is not a valid routing policy that Route 53 can use to select the appropriate resource for a request?

**A:** OS-based routing

---

## Question 144

**Q:** Your company is generating a huge volume of data sets with billions of rows that must be summarized by column. You are going to use Tableau on top of these data sets to build daily and weekly reports. Which AWS service should you use to meet these requirements?

**A:** Amazon Redshift

---

## Question 145

**Q:** You’re building out a single-region application in us-west-2. However, disaster recovery is a strong consideration, and you need to build the application so that if us-west-2 becomes unavailable, you can fail over to us-west-1. Your application relies exclusively on pre-built AMIs. In order to share those AMIs with the region you’re using as a backup, which process would you follow?

**A:** Copy the AMI from us-west-2, manually apply launch permissions, user-defined tags, and Amazon S3 bucket permissions of the default AMI to the new instance, and launch the instance.

---

## Question 146

**Q:** How long are one-minute data points maintained for viewing in Amazon CloudWatch?

**A:** 15 days

---

## Question 147

**Q:** Which one of the following scenarios would result in a higher percentage of savings when using S3 Standard Infrequent Access storage instead of S3 Standard storage?

**A:** 1 TB monthly with 10% of content accessed per month

---

## Question 148

**Q:** You are concerned about maintaining security patches on the 103 AWS EC2 instances that you run. All instances run Windows, Ubuntu Server, or Red Hat Enterprise Linux. What AWS service can assist you on properly and automatically patching these instances?

**A:** AWS Systems Manager Patch Manager

---

## Question 149

**Q:** How many hours of EC2 compute are provided in the free tier?

**A:** 750

---

## Question 150

**Q:** You are planning VPC deployments. What is the maximum number of subnets that can be created in a VPC?

**A:** 200

---

## Question 151

**Q:** You manage a Ruby on Rails application that lives on a cluster of EC2 instances. Your website occasionally experiences brief, strong, and entirely unpredictable spikes in traffic that overwhelm your EC2 instances’ resources and freeze the application. As a result, you’re losing recently submitted requests from end users. You use Auto Scaling to deploy additional resources to handle the load during spikes, but the new instances don’t spin up fast enough to prevent the existing application servers from freezing. Which of the following actions will provide the most cost-effective solution in preventing the loss of recently submitted requests?

**A:** Use Amazon SQS to decouple the application components and keep the requests in queue until the extra Auto Scaling instances are available.

---

## Question 152

**Q:** When considering NACLs and security groups, what is evaluated first when a packet is inbound to an EC2 instance?

**A:** NACL then security group

---

## Question 153

**Q:** You are defining appropriate security options for S3 buckets in AWS. As part of the process, you must identify the default access restrictions on S3 buckets. Which one of the following best describes the default access restrictions in place on S3 buckets?

**A:** Only bucket and object owners have access to the resources they create

---

## Question 154

**Q:** What does AWS provide for extremely large dataset transport to the cloud that provides for offline transport?

**A:** Snowball

---

## Question 155

**Q:** Your application uploads several thousands of files every day. The file sizes range from 500MB to 2GB. Each file is then processed to extract metadata, and the metadata processing takes a few seconds. There is no fixed uploading frequency; sometimes all the files are uploaded at a particular hour, sometimes only a few files are uploaded at a particular hour, and sometimes no uploads occur for a few hours. What is the most cost-effective way of handling this issue?

**A:** Store the files in Amazon S3 and then use an S3 event notification to invoke a Lambda function for extracting the metadata.

---

## Question 156

**Q:** You are required to run Docker containers within AWS. What AWS solution provides this service?

**A:** EC2 Container Service (ECS)

---

## Question 157

**Q:** You must backup an EBS volume as quickly as possible and perform this backup once each day. What is the best method provided within AWS to perform this backup?

**A:** Snapshots

---

## Question 158

**Q:** You are in the process of designing a document archive solution for your company. The solution must be cost-effective; therefore, you have selected Glacier. The business wants to have the capability to get a document within 15 minutes of requesting it. Which feature of Amazon Glacier will you choose?

**A:** Expedited retrieval

---

## Question 159

**Q:** What AWS service can be used to monitor your EC2 instances and provide a dashboard for performance management?

**A:** CloudWatch

---

## Question 160

**Q:** You are in the process of deploying an application in an EC2 instance. The application must call AWS APIs. What is the secured way of passing credentials to the application?

**A:** Assign IAM roles to the EC2 instance.

---

## Question 161

**Q:** You monitor your usage in AWS to increase or decrease resources based on current business requirements. This careful monitoring and response is taken to reduce costs. What model is being implemented according to the AWS Cost Optimization Pillar?

**A:** Consumption Model

---

## Question 162

**Q:** What is the most cost-effective solution to these requirements?

**A:** Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.

---

## Question 163

**Q:** How can this be achieved?

**A:** Launch EC2 instances into multiple regions behind an NLB and use AWS Global Accelerator

---

## Question 164

**Q:** Which solution should a Solutions Architect recommend?

**A:** Create a VPC peering connection between VPC-TEST1 and VPC-TEST2.

---

## Question 165

**Q:** Which solution offers the MOST reliable and time-efficient data transfer?

**A:** AWS DataSync over AWS Direct Connect.

---

## Question 166

**Q:** Which solution will meet these requirements?

**A:** Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler.

---

## Question 167

**Q:** Which service should the solutions architect use to replace the file server farm?

**A:** Amazon FSx

---

## Question 168

**Q:** Which solution would be MOST efficient?

**A:** Use Amazon Kinesis Data Streams for real-time events with a partition key for each device. Use Amazon Kinesis Data Firehose to save data to Amazon S3

---

## Question 169

**Q:** Which solution meets these requirements and is the MOST operationally efficient?

**A:** Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.

---

## Question 170

**Q:** What should the Solutions Architect recommend?

**A:** Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).

---

## Question 171

**Q:** What should a solutions architect recommend for maximum performance?

**A:** Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.

---

## Question 172

**Q:** Which solution should a Solutions Architect recommend?

**A:** Create a Nitro-based Amazon EC2 instance with an Amazon EBS Provisioned IOPS SSD (i01) volume attached. Provision 64,000 IOPS for the volume.

---

## Question 173

**Q:** What should the solutions architect recommend to improve the performance of the platform during catalog searches?

**A:** Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache.

---

## Question 174

**Q:** Which solution will meet this requirement with the LEAST operational overhead?

**A:** Create an Amazon S3 bucket in the us-east-1 Region. Set up an Amazon CloudFront distribution with the S3 bucket as the origin. Use signed URLs to download the software updates.

---

## Question 175

**Q:** Which changes should be made to the database tier to improve performance?

**A:** Migrate the database to an Amazon Aurora global database in MySQL compatibility mode. Configure read replicas in ap-southeast-2

---

## Question 176

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Configure an Amazon SNS topic to receive payment events from an AWS Lambda function. Set up multiple subscribers, such as Lambda functions, to process the events.

---

## Question 177

**Q:** What should the Solutions Architect do to achieve this requirement?

**A:** Create an IAM role with permission to access the database. Attach this IAM role to the EC2 instance.

---

## Question 178

**Q:** Which solution will meet these requirements with the LEAST operational effort?

**A:** Use AWS Glue to create individual ETL jobs for each client. Attach a security configuration that uses client-specific AWS KMS keys for server-side encryption (SSE-KMS) during processing and storage in S3.

---

## Question 179

**Q:** What should a solutions architect recommend?

**A:** Process and store the images using AWS Snowball Edge devices.

---

## Question 180

**Q:** What should the solutions architect configure to ensure the EC2 instances are available when they are needed?

**A:** On-Demand Capacity Reservations

---

## Question 181

**Q:** How can a Solutions Architect enable encryption in transit?

**A:** Download the AWS-provided root certificates. Use the certificates when connecting to the RDS DB instance.

---

## Question 182

**Q:** Which combinations of services should a Solutions Architect use to meet these requirements?

**A:** Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage.

---

## Question 183

**Q:** Which solution will meet these requirements?

**A:** Deploy a Gateway Load Balancer (GWLB) in the networking account to route traffic to the security appliance. Configure the service accounts to send traffic to the GWLB by using a Gateway Load Balancer endpoint in each service account.

---

## Question 184

**Q:** What should the solutions architect do to meet this requirement?

**A:** Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics for analysis.

---

## Question 185

**Q:** Which solution can a Solutions Architect recommend to meet this requirement?

**A:** Use an AWS Storage Gateway file gateway hardware appliance on premises to replicate the data to Amazon S3.

---

## Question 186

**Q:** Which actions would meet these needs?

**A:** Store the data in an Amazon EFS filesystem. Mount the file system on the application instances

---

## Question 187

**Q:** How can a Solutions Architect provide least privilege access to the partner?

**A:** Update the permission policy on the SQS queue to grant the sqs:SendMessage permission to the partner’s AWS account.

---

## Question 188

**Q:** Which solution will meet these requirements?

**A:** Configure AWS PrivateLink to create a private connection between the VPC and the third-party SaaS provider's APIs.

---

## Question 189

**Q:** How should a Solutions Architect accomplish this?

**A:** Set a password policy for the entire AWS account.

---

## Question 190

**Q:** Which solution will meet these requirements?

**A:** Resize the read replica to a smaller instance size and keep the primary instance unchanged.

---

## Question 191

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Use AWS Global Accelerator to route traffic through the closest AWS edge location to customers. Configure endpoint groups for the shipment tracking API to distribute traffic globally and reduce response times.

---

## Question 192

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Use AWS Fargate to provide the compute capacity for the EKS cluster. Create a Fargate profile and deploy the application using the profile.

---

## Question 193

**Q:** What should a Solutions Architect recommend?

**A:** Use Amazon CloudFront with a custom origin pointing to the on-premises servers.

---

## Question 194

**Q:** How should a Solutions Architect configure the Amazon SQS deployment to meet these requirements?

**A:** Use a separate SQS Standard queue for each tier. Configure Amazon EC2 instances to prioritize polling for the paid queue over the free queue.

---

## Question 195

**Q:** Which solution will meet these requirements with the MOST operational efficiency?

**A:** Configure AWS Compute Optimizer to provide cost optimization recommendations for the EC2 instances, the Auto Scaling group, and the EBS volumes.

---


