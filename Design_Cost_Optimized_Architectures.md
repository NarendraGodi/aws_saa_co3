What AWS tool can be used to provide automatic recommendations for improvements in your AWS account security configuration?
CloudWatch
Trusted Advisor
CloudFront
RDS



In the event of loss of access to an Availability Zone for any reason, which S3 storage class does not provide resiliency?
S3 Standard-Infrequent Access
S3 Standard
S3 Glacier
S3 One Zone-Infrequent Access


You have a small database workload with infrequent I/O. These databases are mainly used as ad hoc databases for noncritical testing purposes. Which storage medium would be the most cost-effective way to meet these requirements?
Amazon RDS Provisioned IOPS (SSD) Storage
Amazon RDS Magnetic Storage
Amazon RDS Cold Storage
Amazon RDS General Purpose (SSD) Storage

Which one of the following is controlled by a security group attached to an instance?
NACLs
Database error codes
Inbound traffic
HTTP error codes


You have been engaged as a consultant by a company that generates utility bills and publishes them online. PDF images are generated and then stored on a high-performance RDS instance. Generally, invoices are viewed by customers once per month. Recently, however, the number of customers has increased threefold, and the wait-time necessary to view invoices has increased unacceptably. The CTO is unwilling to alter the codebase more than necessary this quarter, but needs to return performance to an acceptable level before the end-of-the-month print run. Which of the following solutions would you feel comfortable proposing to the CTO and GM? (Choose two.)

Create RDS read replicas and additional web/app instances across all the available AZs.
Use CloudFront to accelerate the presentation of the PDF images.
Move the metadata to a DynamoDB solution, permitting real-time scaling of read IOPS to match demand.
Install an ElastiCache cluster in front of the RDS installation.
Move the images to S3 to reduce database IO.
Overall explanation


Which one of the following RDS database types does not support read replicas?
Aurora
PostgreSQL
MySQL
MariaDB

HTTP is used to upload to S3 buckets. Which HTTP method has eventual consistency with S3 bucket writes?
Updates
Deletes
Erases
PUTs of new files



You are a solutions architect working for a construction company. Your company is migrating its production estate to AWS, and you are in the process of setting up access to the AWS console using Identity Access Management (IAM). You have created 15 users for your system administrators. What further steps do you need to take to enable your system administrators to get access to the AWS console in a secure fashion? (Choose two.)

Have each user set up multifactor authentication once they have logged in to the console.
Get the systems administrators to download the CLI and configure it on their laptop, using their usernames and passwords.
Give the system administrators the secret access key and access key ID, and tell them to use these credentials to log in to the AWS console.
Generate a password for each user and give these passwords to your system administrators.

Which one of the following is not something for which AWS Trusted Advisor makes recommendations?
Performance
Scalability
Fault Tolerance
Cost

You must monitor the costs associated with your AWS account. What can you use to generate an alert should the outbound traffic exceed 250 GB for an on-demand EC2 instance?
AWS CloudFront alerts
AWS Trusted Advisor alerts
AWS ElastiCache alerts
AWS Budget alerts


What AWS database solution is best suited for data warehouse implementations?
EBS
Redshift
DynamoDB
Aurora



Your security manager has hired a security contractor to audit your firewall implementation. When the consultant asks for the login details for the firewall appliance, which of the following might you do? (Choose two.)

Tell him the details of the web application firewall.
Explain that AWS is a cloud service and that AWS manages the network appliances.
Create an IAM role with a policy that can read Security Group and Route settings.
Create an IAM role with a policy that can read Security Group and NACL settings.
Explain that AWS implements network security differently and that there is no such thing as a firewall appliance. Create an IAM user with a policy that can read Security Group and Route settings.

When should RDS backups occur for best performance results?
During times of zero activity
During the busiest time of the day
During times of normally low write IOPS
During times of medium read operations



Even if all best practices are being followed in IAM administration, what can present vulnerabilities related to your EC2 instances?
Improper IAM group usage
Improper IAM user account creation
OS security issues within the instances
Improper IAM role usage
Overall explanation

What AWS service allows you to run code in the AWS cloud without provisioning any of the underlying resources required for code execution?
Aurora
VPC
EC2
Lambda

What is the minimum volume size of a Provisioned IOPS SSD EBS volume?

4 GiB
16 TiB
1 TiB
12 GiB

What common security standard is IAM in compliance with that allows for credit card data to be processed?
GDPR
HIPAA
GLBA
PCI-DSS

You have a web-based application that requires access to a flat-file database (text in CSV format). What is the best storage solution for this data without conversion?
Aurora
MySQL
DynamoDB
S3

When creating NACLs within AWS, why is the rule order so important?

Because the first matching rule applies
Because deny rules must be placed before permit or allow rules
Because they must be entered in the order of TCP or UDP ports
Because they must be entered in the order of IP addresses

What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?

Access Key ID/Username
Username/Secret Access Key
Password/Access Key ID
Access Key ID/Secret Access Key
Overall explanation

You work for a large software company in Seattle. The company has its production environment provisioned on AWS inside a custom VPC. The VPC contains both a public subnet and a private subnet. The company tests its applications on custom EC2 instances inside a private subnet. There are approximately 500 instances, and they communicate to the outside world via a proxy server. At 3 A.M. every night, the EC2 instances pull down OS updates, which are usually 150MB or so. They then apply these updates and reboot; however, if the software has not downloaded within half an hour, the update will attempt to download the following day. You notice that a number of EC2 instances are continually failing to download the updates in the allotted time. Which of the following answers might explain this failure? (Choose two.)

The proxy server has only one Elastic IP address added to it. To increase network throughput, you should add additional Elastic IP addresses.
Your proxy server is blacklisting the address from which the updates are being downloaded, resulting in failed downloads.
The proxy server is in a private subnet and uses a NAT gateway instance to connect to the Internet. However, this instance is too small to handle the required network traffic. You should re-provision the NAT gateway instance so that it’s able to handle the throughput.
The proxy server has an inadequately sized EBS volume attached to it. The network buffer is stored on the EBS volume, and it is running out of disk space when trying to buffer the 500 simultaneous connections. You should provision an EBS volume with provisioned IOPS.
The proxy server is on an inadequately sized EC2 instance and does not have sufficient network throughput to handle all updates simultaneously. You should increase the instance size of the EC2 instance for the proxy server.


What can be configured to optimize EFS performance in relation to NFS mount options?
Use FTP instead of NFS
Use NFSv4.0
Use NFSv4.1
Use TFTP instead of NFS
Overall explanation

Which one of the following languages is not supported by Elastic Beanstalk?
Java
Python
Perl
Node.js

To audit the API calls made to your account, which AWS service would you use?

AWS CloudTrail
AWS CloudWatch
AWS Lambda
AWS Systems Manager

You must plan a Route 53 deployment in AWS. What routing policy is used to send all traffic to a single resource?
Geolocation routing
Simple routing
Latency-based routing
Route 53 is not used in this way

You have been monitoring a sensitive Auto Scaling group, and you expect it to scale in as you enter a period of downtime over the holiday. The Auto Scaling group is distributed over three AZs (AZ -A and AZ -B have two instances each, and AZ -C has three instances). All instances have different CPU and memory utilization levels and have been running for a different number of days. All instances come from different versions of a root AMI and have different numbers of sessions connected. Which instance will be the first to shut down?

The instance in AZ -C that has the oldest launch configuration will terminate first.
The instance with the fewest current sessions will terminate first.
The instance in AZ -C that has the least number of sessions will terminate first.
The instance in AZ -C that has been running the longest will terminate first.
The instance that has been running longest will terminate first.

You have a MySQL database running on an EC2 instance in a private subnet. You can connect via SSH, but you are unable to apply updates to the database server via the NAT instance. What might you do to remedy this problem?
Modify the security group to allow SSH traffic from anywhere.
Replace the NAT instance.
Ensure that “Source/Destination Checks” is disabled on the NAT instance.
Ensure that the security group allows HTTP traffic.


What can be implemented to prevent traffic from the network to your EC2 instance from impacting the performance of traffic between your EC2 instance and an attached EBS volume?
Implement network-optimized instances
Implement EBS-optimized instances
Put the EBS volume in one VPC and the instance in another
Place the EBS volume in one region and the instance in another


You are a solutions architect working for an oil and gas company that’s moving its production environment to AWS and needs a custom VPC in which to put it. You have been asked to create a public subnet. You create the VPC with a subnet bearing the CIDR address range 10.0.1.0/24. Which of the following steps should you take to make this subnet public? (Choose two.)
Create a route in the route table of the subnet allowing a route out of the Customer Gateway (CGW).
Attach a Customer Gateway (CGW).
Create a route in the route table of the subnet allowing a route out of the Internet Gateway (IGW).
In the AWS Console, right-click the subnet and then select the Make Public option.
Attach an Internet Gateway (IGW) to the VPC.

You want to limit who can modify a NACL that is associated with a subnet. What can you use?
Security Group
Another NACL
Flow log
IAM



You must attach an EBS volume to an EC2 instance that offers the highest level of performance. What EBS type should be used?

Provisioned IOPS SSD
Striped SSD
Magnetic
General SSD
Overall explanation

You have three Elastic Network Interfaces (ENIs). They are attached to three instances. You need an ENI for another instance and one of the instances currently using an ENI no longer needs it. What is the best action to take?

Move the ENI from the instance no longer needing it to the instance requiring it
Delete the ENI from the instance no longer requiring it and then create a new ENI for the instance requiring it
Create a new ENI and attach it to the instance requiring it
You cannot have more than two active ENIs.

You must implement an AWS solution that can expand and contract the number of server instances as needed. What AWS service provides this functionality?

Auto Scaling
ElastiCache
Lambda
Auto Growing

In which of the following services can you have root-level access to the operating system? (Choose two.)

Amazon EMR
Amazon DynamoDB
Amazon RDS
Correct selection
Amazon EC2

You are planning VPC deployments. What is the maximum number of subnets that can be created in a VPC?
50
200
5
10


You are required to run Docker containers within AWS. What AWS solution provides this service?
Lambda
EC2 Container Service (ECS)
Lightsail
CloudFormation

When it comes to security groups within a custom VPC, which of the following statements are correct? (Choose two.)
Updates to security groups are not applied immediately; however, they are applied within the hour in which they are made.
Updates to security groups are applied immediately.
Security groups are stateless.
Security groups are stateful.


You have a fleet of EC2 instances hosting your application, running in an on-demand model that is billed on an hourly basis. For running your application, you have enabled Auto Scaling for scaling up and down, as per the workload, and while reviewing the Auto Scaling events you notice that the application is scaling up and down multiple times within the same hour. What would you do to optimize the cost while preserving elasticity at the same time? (Choose two.)

Change the Auto Scaling group’s cool-down time.
Change the CloudWatch alarm period that triggers the Auto Scaling scale-down policy.
Terminate the newest-running EC2 instance by modifying the Auto Scaling group termination policy.
Use a reserved instance instead of an on-demand instance to optimize cost.
Terminate the longest-running EC2 instance by modifying the Auto Scaling group termination policy.

A company offers an online product brochure that is delivered from a static website running on Amazon S3. The company’s customers are mainly in the United States, Canada, and Mexico. The company is looking to cost-effectively reduce the latency for users in these regions.
What is the most cost-effective solution to these requirements?
Create an Amazon CloudFront distribution and set the price class to use all Edge Locations for best performance.
Create an Amazon CloudFront distribution that uses origins in U.S, Canada and Mexico.
Create an Amazon CloudFront distribution and use Lambda@Edge to run the website's data processing closer to the users.
Create an Amazon CloudFront distribution and set the price class to use only U.S, Canada and Mexico.

A research group runs its flagship application on a fleet of Amazon EC2 instances for a specialized task that must deliver high random I/O performance. Each instance in the fleet would have access to a dataset that is replicated across the instances by the application itself. Because of the resilient application architecture, the specialized task would continue to be processed even if any instance goes down, as the underlying application would ensure the replacement instance has access to the required dataset.
Which of the following options is the MOST cost-optimal and resource-efficient solution to build this fleet of Amazon EC2 instances?
Use Amazon EC2 instances with Amazon EFS mount points
Use Amazon EC2 instances with access to Amazon S3 based storage
Use Instance Store based Amazon EC2 instances
Use Amazon Elastic Block Store (Amazon EBS) based EC2 instances


A biotech research company needs to perform data analytics on real-time lab results provided by a partner organization. The partner stores these lab results in an Amazon RDS for MySQL instance within the partner’s own AWS account. The research company has a private VPC that does not have internet access, Direct Connect, or a VPN connection. However, the company must establish secure and private connectivity to the RDS database in the partner’s VPC. The solution must allow the research company to connect from its VPC while minimizing complexity and complying with data security requirements.
Which solution will meet these requirements?

Instruct the partner to create a Network Load Balancer (NLB) in front of the Amazon RDS for MySQL instance. Use AWS PrivateLink to expose the NLB as an interface VPC endpoint in the research company’s VPC
Instruct the partner to enable public access on the Amazon RDS instance and add a security group rule to allow inbound access from the company’s IP range. The company accesses the database over the public internet through a NAT Gateway configured in a private subnet
Set up VPC peering between the company’s VPC and the partner’s VPC. Use AWS Transit Gateway in the partner's account to route traffic from the company’s VPC to the database. Modify the RDS subnet route tables to allow access from the company’s CIDR block
Configure a client VPN endpoint in the company’s account. Have researchers connect to the VPN from their local machines. Establish a Direct Connect gateway to the partner’s VPC and route RDS traffic via this connection


A large financial institution operates an on-premises data center with hundreds of petabytes of data managed on Microsoft’s Distributed File System (DFS). The CTO wants the organization to transition into a hybrid cloud environment and run data-intensive analytics workloads that support DFS.
Which of the following AWS services can facilitate the migration of these workloads?
Amazon FSx for Lustre
AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)
Amazon FSx for Windows File Server
Microsoft SQL Server on AWS


An IT company wants to review its security best-practices after an incident was reported where a new developer on the team was assigned full access to Amazon DynamoDB. The developer accidentally deleted a couple of tables from the production environment while building out a new feature.
Which is the MOST effective way to address this issue so that such incidents do not recur?
Only root user should have full database access in the organization
Remove full database access for all IAM users in the organization
The CTO should review the permissions for each new developer's IAM user so that such incidents don't recur
Use permissions boundary to control the maximum permissions employees can grant to the IAM principals


An organization wants to delegate access to a set of users from the development environment so that they can access some resources in the production environment which is managed under another AWS account.
As a solutions architect, which of the following steps would you recommend?
It is not possible to access cross-account resources
Both IAM roles and IAM users can be used interchangeably for cross-account access
Create a new IAM role with the required permissions to access the resources in the production environment. The users can then assume this IAM role while accessing the resources from the production environment
Create new IAM user credentials for the production environment and share these credentials with the set of users from the development environment


A healthcare company uses its on-premises infrastructure to run legacy applications that require specialized customizations to the underlying Oracle database as well as its host operating system (OS). The company also wants to improve the availability of the Oracle database layer. The company has hired you as an AWS Certified Solutions Architect – Associate to build a solution on AWS that meets these requirements while minimizing the underlying infrastructure maintenance effort.
Which of the following options represents the best solution for this use case?

Leverage cross AZ read-replica configuration of Amazon RDS for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
Leverage multi-AZ configuration of Amazon RDS Custom for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
Deploy the Oracle database layer on multiple Amazon EC2 instances spread across two Availability Zones (AZs). This deployment configuration guarantees high availability and also allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
Leverage multi-AZ configuration of Amazon RDS for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system


An e-commerce company manages a digital catalog of consumer products submitted by third-party sellers. Each product submission includes a description stored as a text file in an Amazon S3 bucket. These descriptions may include ingredient information for consumable products like snacks, supplements, or beverages. The company wants to build a fully automated solution that extracts ingredient names from the uploaded product descriptions and uses those names to query an Amazon DynamoDB table, which returns precomputed health and safety scores for each ingredient. Non-food items and invalid submissions can be ignored without affecting application logic. The company has no in-house machine learning (ML) experts and is looking for the most cost-effective solution with minimal operational overhead.
Which solution meets these requirements MOST cost-effectively?

Use Amazon Lookout for Vision to scan the uploaded text files in the S3 bucket and extract entities. Invoke this workflow using an S3-triggered Lambda function. Parse the output and use Amazon API Gateway to push updates to the frontend in real time

Configure S3 Event Notifications to trigger an AWS Lambda function whenever a new product description is uploaded. Inside the function, use Amazon Comprehend's custom entity recognition feature to extract ingredient names. Store these names in the DynamoDB table and let the front-end application query for health scores

Create a workflow where Amazon Transcribe is used to convert synthetic audio versions (created from text of the product descriptions) back into text. Analyze the transcripts manually or using simple keyword matching within a Lambda function. Use Amazon SNS to notify the content moderation team for each processed file

Use Amazon SageMaker with a custom-trained NLP model to identify ingredients from the uploaded descriptions. Use Amazon EventBridge to invoke a Lambda function that forwards the document content to a SageMaker endpoint and stores the results in DynamoDB. Fine-tune the model using labeled ingredient datasets from open-source repositories and retrain it monthly


While consolidating logs for the weekly reporting, a development team at an e-commerce company noticed that an unusually large number of illegal AWS application programming interface (API) queries were made sometime during the week. Due to the off-season, there was no visible impact on the systems. However, this event led the management team to seek an automated solution that can trigger near-real-time warnings in case such an event recurs.
Which of the following represents the best solution for the given scenario?

Configure AWS CloudTrail to stream event data to Amazon Kinesis. Use Amazon Kinesis stream-level metrics in the Amazon CloudWatch to trigger an AWS Lambda function that will trigger an error workflow

Run Amazon Athena SQL queries against AWS CloudTrail log files stored in Amazon S3 buckets. Use Amazon QuickSight to generate reports for managerial dashboards

Create an Amazon CloudWatch metric filter that processes AWS CloudTrail logs having API call details and looks at any errors by factoring in all the error codes that need to be tracked. Create an alarm based on this metric's rate to send an Amazon SNS notification to the required team

AWS Trusted Advisor publishes metrics about check results to Amazon CloudWatch. Create an alarm to track status changes for checks in the Service Limits category for the APIs. The alarm will then notify when the service quota is reached or exceeded


A healthcare analytics company centralizes clinical and operational datasets in an Amazon S3–based data lake. Incoming data is ingested in Apache Parquet format from multiple hospitals and wearable health devices. To ensure quality and standardization, the company applies several transformation steps: anomaly filtering, datetime normalization, and aggregation by patient cohort. The company needs a solution to support a code-free interface that enables data engineers and business analysts to collaborate on data preparation workflows. The company also requires data lineage tracking, data profiling capabilities, and an easy way to share transformation logic across teams without writing or managing code.
Which AWS solution best meets these requirements?

Use AWS Glue DataBrew to visually build transformation workflows on top of the raw Parquet files in S3. Use DataBrew recipes to track, audit, and share the transformation steps with others. Enable data profiling to inspect column statistics, null values, and data types across datasets

Use Amazon AppFlow to move and transform Parquet files in S3. Configure AppFlow transformations and mappings within the visual interface. Share flows with collaborators through AWS IAM policies and scheduled executions

Create Amazon Athena SQL queries to perform transformation steps directly on S3. Store queries in AWS Glue Data Catalog and share saved queries with other users through Amazon Athena's query editor

Use AWS Glue Studio’s visual canvas to design data transformation workflows on top of the Parquet files in Amazon S3. Configure Glue Studio jobs to run these transformations without writing code. Share the job definitions with team members for reuse. Use the visual job editor to track transformation progress and inspect profiling statistics for each dataset column



A retail company's dynamic website is hosted using on-premises servers in its data center in the United States. The company is launching its website in Asia, and it wants to optimize the website loading times for new users in Asia. The website's backend must remain in the United States. The website is being launched in a few days, and an immediate solution is needed.
What would you recommend?
Use Amazon CloudFront with a custom origin pointing to the on-premises servers
Use Amazon CloudFront with a custom origin pointing to the DNS record of the website on Amazon Route 53
Migrate the website to Amazon S3. Use S3 cross-region replication (S3 CRR) between AWS Regions in the US and Asia
Leverage a Amazon Route 53 geo-proximity routing policy pointing to on-premises servers




A retail company wants to rollout and test a blue-green deployment for its global application in the next 48 hours. Most of the customers use mobile phones which are prone to Domain Name System (DNS) caching. The company has only two days left for the annual Thanksgiving sale to commence.
As a Solutions Architect, which of the following options would you recommend to test the deployment on as many users as possible in the given time frame?
Use Elastic Load Balancing (ELB) to distribute traffic across deployments
Use AWS Global Accelerator to distribute a portion of traffic to a particular deployment
Use AWS CodeDeploy deployment options to choose the right deployment
Use Amazon Route 53 weighted routing to spread traffic across different deployments


The engineering manager for a content management application wants to set up Amazon RDS read replicas to provide enhanced performance and read scalability. The manager wants to understand the data transfer charges while setting up Amazon RDS read replicas.
Which of the following would you identify as correct regarding the data transfer charges for Amazon RDS read replicas?

There are data transfer charges for replicating data within the same AWS Region
There are no data transfer charges for replicating data across AWS Regions
There are data transfer charges for replicating data within the same Availability Zone (AZ)
There are data transfer charges for replicating data across AWS Regions


The DevOps team at a major financial services company uses Multi-Availability Zone (Multi-AZ) deployment for its MySQL Amazon RDS database in order to automate its database replication and augment data durability. The DevOps team has scheduled a maintenance window for a database engine level upgrade for the coming weekend.
Which of the following is the correct outcome during the maintenance window?

Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the standby database instance to be upgraded which is then followed by the upgrade of the primary database instance. This does not cause any downtime for the duration of the upgrade

Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the primary database instance to be upgraded which is then followed by the upgrade of the standby database instance. This does not cause any downtime for the duration of the upgrade

Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. However, this does not cause any downtime until the upgrade is complete

Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete


An HTTP application is deployed on an Auto Scaling Group, is accessible from an Application Load Balancer (ALB) that provides HTTPS termination, and accesses a PostgreSQL database managed by Amazon RDS.
How should you configure the security groups? (Select three)

The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 5432
The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 80
The security group of the Application Load Balancer should have an inbound rule from anywhere on port 443
The security group of the Application Load Balancer should have an inbound rule from anywhere on port 80
The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Amazon RDS database on port 5432
The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Application Load Balancer on port 80

A retail company wants to share sensitive accounting data that is stored in an Amazon RDS database instance with an external auditor. The auditor has its own AWS account and needs its own copy of the database.
Which of the following would you recommend to securely share the database with the auditor?
Set up a read replica of the database and configure IAM standard database authentication to grant the auditor access
Export the database contents to text files, store the files in Amazon S3, and create a new IAM user for the auditor with access to that bucke
Create an encrypted snapshot of the database, share the snapshot, and allow access to the AWS Key Management Service (AWS KMS) encryption key
Create a snapshot of the database in Amazon S3 and assign an IAM role to the auditor to grant access to the object in that bucket

An analytics company wants to improve the performance of its big data processing workflows running on Amazon Elastic File System (Amazon EFS). Which of the following performance modes should be used for Amazon EFS to address this requirement?
General Purpose
Bursting Throughput
Max I/O
Provisioned Throughput

You are establishing a monitoring solution for desktop systems, that will be sending telemetry data into AWS every 1 minute. Data for each system must be processed in order, independently, and you would like to scale the number of consumers to be possibly equal to the number of desktop systems that are being monitored.
What do you recommend?

Use an Amazon Simple Queue Service (Amazon SQS) FIFO (First-In-First-Out) queue, and make sure the telemetry data is sent with a Group ID attribute representing the value of the Desktop ID
Use an Amazon Simple Queue Service (Amazon SQS) FIFO (First-In-First-Out) queue, and send the telemetry data as is
Use an Amazon Simple Queue Service (Amazon SQS) standard queue, and send the telemetry data as is
Use an Amazon Kinesis Data Stream, and send the telemetry data with a Partition ID that uses the value of the Desktop ID


Amazon EC2 Auto Scaling needs to terminate an instance from Availability Zone (AZ) us-east-1a as it has the most number of instances amongst the Availability Zone (AZs) being used currently. There are 4 instances in the Availability Zone (AZ) us-east-1a like so: Instance A has the oldest launch template, Instance B has the oldest launch configuration, Instance C has the newest launch configuration and Instance D is closest to the next billing hour.
Which of the following instances would be terminated per the default termination policy?
Instance D
Instance B
Instance C
Instance A



You would like to use AWS Snowball to move on-premises backups into a long term archival tier on AWS. Which solution provides the MOST cost savings?

Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier Deep Archive on the same day
Create a AWS Snowball job and target an Amazon S3 Glacier Deep Archive Vault
Create an AWS Snowball job and target a Amazon S3 Glacier Vault
Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier on the same day



A health-care solutions company wants to run their applications on single-tenant hardware to meet regulatory guidelines.
Which of the following is the MOST cost-effective way of isolating their Amazon Elastic Compute Cloud (Amazon EC2)instances to a single tenant?
On-Demand Instances
Dedicated Hosts
Spot Instances
Dedicated Instances

You have a team of developers in your company, and you would like to ensure they can quickly experiment with AWS Managed Policies by attaching them to their accounts, but you would like to prevent them from doing an escalation of privileges, by granting themselves the AdministratorAccess managed policy. How should you proceed?

For each developer, define an IAM permission boundary that will restrict the managed policies they can attach to themselves
Put the developers into an IAM group, and then define an IAM permission boundary on the group that will restrict the managed policies they can attach to themselves
Create a Service Control Policy (SCP) on your AWS account that restricts developers from attaching themselves the AdministratorAccess policy
Attach an IAM policy to your developers, that prevents them from attaching the AdministratorAccess policy


A company has hired you as an AWS Certified Solutions Architect – Associate to help with redesigning a real-time data processor. The company wants to build custom applications that process and analyze the streaming data for its specialized needs.
Which solution will you recommend to address this use-case?

Use Amazon Kinesis Data Streams to process the data streams as well as decouple the producers and consumers for the real-time data processor
Use Amazon Kinesis Data Firehose to process the data streams as well as decouple the producers and consumers for the real-time data processor
Use Amazon Simple Queue Service (Amazon SQS) to process the data streams as well as decouple the producers and consumers for the real-time data processor
Use Amazon Simple Notification Service (Amazon SNS) to process the data streams as well as decouple the producers and consumers for the real-time data processor


A company has a hybrid cloud structure for its on-premises data center and AWS Cloud infrastructure. The company wants to build a web log archival solution such that only the most frequently accessed logs are available as cached data locally while backing up all logs on Amazon S3.
As a solutions architect, which of the following solutions would you recommend for this use-case?

Use AWS Volume Gateway - Cached Volume - to store the most frequently accessed logs locally for low-latency access while storing the full volume with all logs in its Amazon S3 service bucket
Use AWS Direct Connect to store the most frequently accessed logs locally for low-latency access while storing the full backup of logs in an Amazon S3 bucket
Use AWS Volume Gateway - Stored Volume - to store the most frequently accessed logs locally for low-latency access while storing the full volume with all logs in its Amazon S3 service bucket
Use AWS Snowball Edge Storage Optimized device to store the most frequently accessed logs locally for low-latency access while storing the full backup of logs in an Amazon S3 bucket


The database backend for a retail company's website is hosted on Amazon RDS for MySQL having a primary instance and three read replicas to support read scalability. The company has mandated that the read replicas should lag no more than 1 second behind the primary instance to provide the best possible user experience. The read replicas are falling further behind during periods of peak traffic spikes, resulting in a bad user experience as the searches produce inconsistent results.
You have been hired as an AWS Certified Solutions Architect - Associate to reduce the replication lag as much as possible with minimal changes to the application code or the effort required to manage the underlying resources.
Which of the following will you recommend?
Set up an Amazon ElastiCache for Redis cluster in front of the MySQL database. Update the website to check the cache before querying the read replicas
Set up database migration from Amazon RDS MySQL to Amazon Aurora MySQL. Swap out the MySQL read replicas with Aurora Replicas. Configure Aurora Auto Scaling
Host the MySQL primary database on a memory-optimized Amazon EC2 instance. Spin up additional compute-optimized Amazon EC2 instances to host the read replicas
Set up database migration from Amazon RDS MySQL to Amazon DynamoDB. Provision a large number of read capacity units (RCUs) to support the required throughput and enable Auto-Scaling


A global pharmaceutical company wants to move most of the on-premises data into Amazon S3, Amazon Elastic File System (Amazon EFS), and Amazon FSx for Windows File Server easily, quickly, and cost-effectively.
As a solutions architect, which of the following solutions would you recommend as the BEST fit to automate and accelerate online data transfers to these AWS storage services?

Use AWS DataSync to automate and accelerate online data transfers to the given AWS storage services
Use AWS Transfer Family to automate and accelerate online data transfers to the given AWS storage services
Use AWS Snowball Edge Storage Optimized device to automate and accelerate online data transfers to the given AWS storage services
Use File Gateway to automate and accelerate online data transfers to the given AWS storage services


A data analytics company manages an application that stores user data in a Amazon DynamoDB table. The development team has observed that once in a while, the application writes corrupted data in the Amazon DynamoDB table. As soon as the issue is detected, the team needs to remove the corrupted data at the earliest.
What do you recommend?

Use Amazon DynamoDB point in time recovery to restore the table to the state just before corrupted data was written
Use Amazon DynamoDB on-demand backup to restore the table to the state just before corrupted data was written
Configure the Amazon DynamoDB table as a global table and point the application to use the table from another AWS region that has no corrupted data
Use Amazon DynamoDB Streams to restore the table to the state just before corrupted data was written


A startup is building a serverless microservices architecture where client applications (web and mobile) authenticate users via a third-party OIDC-compliant identity provider. The backend APIs must validate JSON Web Tokens (JWTs) issued by this provider, enforce scope-based access control, and be cost-effective with minimal latency. The development team wants to use a fully managed service that supports JWT validation natively, without writing custom authentication logic.
Which solution should the team implement to meet these requirements?

Deploy a gRPC backend on Amazon ECS Fargate and expose it through AWS App Runner, handling JWT validation inside the containerized services
Use Amazon API Gateway REST API with a Lambda function that manually validates JWT tokens
Use Amazon API Gateway WebSocket API with JWT claims validated by a Lambda authorizer
Use Amazon API Gateway HTTP API with a native JWT authorizer configured to validate tokens from the OIDC provider


An application running on an Amazon EC2 instance needs to access a Amazon DynamoDB table in the same AWS account.
Which of the following solutions should a solutions architect configure for the necessary permissions?

Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Add the Amazon EC2 instance to the trust relationship policy document so that the instance can assume the role
Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Configure an instance profile to assign this IAM role to the Amazon EC2 instance
Set up an IAM user with the appropriate permissions to allow access to the Amazon DynamoDB table. Store the access credentials in the local storage and read them from within the application code directly
Set up an IAM user with the appropriate permissions to allow access to the Amazon DynamoDB table. Store the access credentials in an Amazon S3 bucket and read them from within the application code directly


A research organization is running a high-performance computing (HPC) workload using Amazon EC2 instances that are distributed across multiple Availability Zones (AZs) within a single AWS Region. The workload requires access to a shared file system with the lowest possible latency for frequent reads and writes.The team decides to use Amazon Elastic File System (Amazon EFS) for its scalability and simplicity. To ensure optimal performance and reduce network latency, the solution architect must design the architecture so that each EC2 instance can access the file system with the least possible delay.
Which of the following is the most appropriate solution to meet these requirements?

Create a single EFS mount target in one AZ and allow all EC2 instances in other AZs to access it using the default mount target
Create EFS mount targets in each AZ and mount the EFS file system to EC2 instances in the same AZ as the mount target
Use Mountpoint for Amazon S3 to mount an S3 bucket on each EC2 instance and use it as a shared storage layer across Availability Zones
Create mount targets for Amazon EFS on an EC2 instance in each AZ and use them to serve as access points for other instances

A retail company uses AWS Cloud to manage its technology infrastructure. The company has deployed its consumer-focused web application on Amazon EC2-based web servers and uses Amazon RDS PostgreSQL database as the data store. The PostgreSQL database is set up in a private subnet that allows inbound traffic from selected Amazon EC2 instances. The database also uses AWS Key Management Service (AWS KMS) for encrypting data at rest.
Which of the following steps would you recommend to facilitate end-to-end security for the data-in-transit while accessing the database?
Create a new security group that blocks SSH from the selected Amazon EC2 instances into the database
Create a new network access control list (network ACL) that blocks SSH from the entire Amazon EC2 subnet into the database
Use IAM authentication to access the database instead of the database user's access credentials
Correct answer
Configure Amazon RDS to use SSL for data in transit


A ride-sharing company wants to improve the ride-tracking system that stores GPS coordinates for all rides. The engineering team at the company is looking for a NoSQL database that has single-digit millisecond latency, can scale horizontally, and is serverless, so that they can perform high-frequency lookups reliably.
As a Solutions Architect, which database do you recommend for their requirements?
Amazon ElastiCache
Amazon Relational Database Service (Amazon RDS)
Correct answer
Amazon DynamoDB
Amazon Neptune


A company has recently created a new department to handle their services workload. An IT team has been asked to create a custom VPC to isolate the resources created in this new department. They have set up the public subnet and internet gateway (IGW). However, they are not able to ping the Amazon EC2 instances with elastic IP address (EIP) launched in the newly created VPC.
As a Solutions Architect, the team has requested your help. How will you troubleshoot this scenario? (Select two)
Contact AWS support to map your VPC with subnet
Correct selection
Check if the security groups allow ping from the source
Disable Source / Destination check on the Amazon EC2 instance
Create a secondary internet gateway to attach with public subnet and move the current internet gateway to private and write route tables
Correct selection
Check if the route table is configured with internet gateway


A ride-hailing startup has launched a mobile app that matches passengers with nearby drivers based on real-time GPS coordinates. The application backend uses an Amazon RDS for PostgreSQL instance with read replicas to store the latitude and longitude of drivers and passengers. As the service scales, the backend experiences performance bottlenecks during peak hours, especially when thousands of updates and reads occur per second to keep location data current. The company expects its user base to double in the next few months and needs a high-performance, scalable solution that can handle frequent write and read operations with minimal latency.
What do you recommend?
Create a read-replica Auto Scaling policy for the PostgreSQL database to dynamically add replicas during peak load. Distribute traffic evenly using an RDS proxy with failover configuration
Enable Multi-AZ deployment for the primary RDS instance to improve write resilience and fault tolerance. Use Multi-AZ standby failover to distribute reads during peak hours
Correct answer
Place an Amazon ElastiCache for Redis cluster in front of the PostgreSQL database. Modify the application to cache recent location reads and updates in Redis, using a TTL-based eviction strategy
Migrate the location data to Amazon OpenSearch Service and use its geospatial indexing features to retrieve and store coordinates in near real-time. Visualize tracking data using OpenSearch Dashboards


The development team at a social media company wants to handle some complicated queries such as "What are the number of likes on the videos that have been posted by friends of a user A?".
As a solutions architect, which of the following AWS database services would you suggest as the BEST fit to handle such use cases?
Correct answer
Amazon Neptune
Amazon Aurora
Amazon Redshift
Amazon OpenSearch Service


A social media company wants the capability to dynamically alter the size of a geographic area from which traffic is routed to a specific server resource.
Which feature of Amazon Route 53 can help achieve this functionality?
Geolocation routing
Latency-based routing
Weighted routing
Correct answer
Geoproximity routing


A media company operates a video rendering pipeline on Amazon EKS, where containerized jobs are scheduled using Kubernetes deployments. The application experiences bursty traffic patterns, particularly during peak streaming hours. The platform uses the Kubernetes Horizontal Pod Autoscaler (HPA) to scale pods based on CPU utilization. A solutions architect observes that the total number of EC2 worker nodes remains constant during traffic spikes, even when all nodes are at maximum resource utilization. The company needs a solution that enables automatic scaling of the underlying compute infrastructure when pod demand exceeds cluster capacity.
Which solution should the architect implement to resolve this issue with the least operational overhead?

Enable Amazon EC2 Auto Scaling with custom CloudWatch alarms based on cluster-wide CPU and memory usage to dynamically adjust node count in the EKS worker node group

Use AWS Fargate to replace the EKS worker nodes with serverless compute profiles, allowing Fargate to scale pods automatically without managing EC2 infrastructure

Implement an AWS Lambda function that runs every 10 minutes and checks EKS pod scheduling status. Trigger node scaling manually using the eksctl CLI or AWS SDK if unschedulable pods are detected

Correct answer
Deploy the Kubernetes Cluster Autoscaler to the EKS cluster. Configure it to integrate with the existing EC2 Auto Scaling group to automatically launch or terminate nodes based on pending pod demands


A retail company is using AWS Site-to-Site VPN connections for secure connectivity to its AWS cloud resources from its on-premises data center. Due to a surge in traffic across the VPN connections to the AWS cloud, users are experiencing slower VPN connectivity.
Which of the following options will maximize the VPN throughput?

Create a virtual private gateway with equal cost multipath routing and multiple channels
Correct answer
Create an AWS Transit Gateway with equal cost multipath routing and add additional VPN tunnels
Use Transfer Acceleration for the VPN connection to maximize the throughput
Use AWS Global Accelerator for the VPN connection to maximize the throughput


An IT company runs a high-performance computing (HPC) workload on AWS. The workload requires high network throughput and low-latency network performance along with tightly coupled node-to-node communications. The Amazon EC2 instances are properly sized for compute and storage capacity and are launched using default options.
Which of the following solutions can be used to improve the performance of the workload?
Select dedicated instance tenancy while launching Amazon EC2 instances
Correct answer
Select a cluster placement group while launching Amazon EC2 instances
Select the appropriate capacity reservation while launching Amazon EC2 instances
Select an Elastic Inference accelerator while launching Amazon EC2 instances

The engineering team at a leading e-commerce company is anticipating a surge in the traffic because of a flash sale planned for the weekend. You have estimated the web traffic to be 10x. The content of your website is highly dynamic and changes very often.
As a Solutions Architect, which of the following options would you recommend to make sure your infrastructure scales for that day?
Use an Amazon Route 53 Multi Value record
Correct answer
Use an Auto Scaling Group
Use an Amazon CloudFront distribution in front of your website
Deploy the website on Amazon S3


As a solutions architect, you have created a solution that utilizes an Application Load Balancer with stickiness and an Auto Scaling Group (ASG). The Auto Scaling Group spans across 2 Availability Zones (AZs). AZ-A has 3 Amazon EC2 instances and AZ-B has 4 Amazon EC2 instances. The Auto Scaling Group is about to go into a scale-in event due to the triggering of a Amazon CloudWatch alarm.
What will happen under the default Auto Scaling Group configuration?
Correct answer
The instance with the oldest launch template or launch configuration will be terminated in AZ-B
A random instance in the AZ-A will be terminated
A random instance will be terminated in AZ-B
An instance in the AZ-A will be created


A financial analytics firm runs performance-intensive modeling software on Amazon EC2 instances backed by Amazon EBS volumes. The production data resides on EBS volumes attached to EC2 instances in the same AWS Region where the testing environment is hosted. To maintain data integrity, any changes made during testing must not affect production data. The development team needs to frequently create clones of this production data for simulations. The modeling software requires high and consistent I/O performance, and the firm wants to minimize the time required to provision test data.
Which solution should a solutions architect recommend to meet these requirements?
Create Amazon EBS-backed Amazon Machine Images (AMIs) from the production EC2 instances. Launch new EC2 instances in the test environment from the AMIs. Use Amazon EC2 instance store volumes for temporary simulation data
Correct answer
Take snapshots of the production EBS volumes. Enable EBS fast snapshot restore on the snapshots. Create new EBS volumes from the snapshots and attach them to EC2 instances in the test environment
Create new EBS volumes in the test environment and use AWS Backup to perform a backup job of the production volumes. Restore the backup directly to the test EBS volumes to begin simulations
Use Amazon EBS io2 volumes with Multi-Attach enabled. Attach the same production EBS volumes to both the production and test EC2 instances simultaneously to avoid cloning delays and ensure high IOPS performance


A multinational logistics company operates its shipment tracking platform from Amazon EC2 instances deployed in the AWS us-west-2 Region. The platform exposes a set of APIs over HTTPS, which are used by logistics partners and customers around the world to retrieve real-time tracking data. The company has observed that users from Europe and Asia experience latency issues and inconsistent API response times when accessing the service. As a cloud architect, you have been tasked to propose the most cost-effective solution to improve performance for these international users without migrating the application.
Which solution should you recommend?
Correct answer
Set up AWS Global Accelerator with listeners configured for HTTPS. Create endpoint groups for Europe and Asia and add the existing us-west-2 EC2 endpoint to these groups
Use Amazon Route 53 latency-based routing to direct user requests to a copy of the EC2 API deployed in each major geographic Region
Deploy Amazon API Gateway in multiple AWS Regions and synchronize the API definitions. Use AWS Lambda as a proxy to forward requests to the EC2-hosted API in us-west-2
Deploy an Amazon CloudFront distribution in front of the API endpoint and apply the CachingOptimized managed policy to enhance caching behavior and improve content delivery efficiency


A streaming service provider collects user experience feedback through embedded feedback forms in their mobile and web apps. Feedback submissions frequently spike to thousands per hour during content launches or service outages. Currently, the feedback is sent via email to the operations team for manual review. The company now wants to automate feedback collection and sentiment analysis so that insights can be generated quickly and stored for a full year for trend analysis.
Which solution provides the most scalable and automated approach to meet these requirements?

Build a web service on Amazon EC2 that receives feedback data and stores each record in a DynamoDB table. Use the EC2 application to invoke Amazon Comprehend for sentiment detection and write results to a second table. Apply a TTL of 365 days to each table

Correct answer
Design a RESTful API with Amazon API Gateway that forwards incoming feedback data to an Amazon SQS queue. Set up an AWS Lambda function to process the queue messages, analyze sentiment using Amazon Comprehend, and store results in a DynamoDB table with a 365-day TTL configured on each item

Route all feedback submissions through Amazon Kinesis Data Streams. Use an AWS Lambda consumer to batch process incoming records, invoke Amazon Translate to detect language and convert input to English, and save the processed content in an Amazon OpenSearch Service index. Configure OpenSearch Index State Management (ISM) policies to delete documents after 12 months

Use Amazon EventBridge to capture feedback events and forward them to an AWS Step Functions workflow. The workflow invokes Lambda functions for validation, calls Amazon Transcribe to convert the text to audio for archival, and stores the results in an Amazon RDS database. Configure a lifecycle policy to remove records after 12 months


A digital content production company has transitioned all of its media assets to Amazon S3 in an effort to reduce storage costs. However, the rendering engine used in production continues to run in an on-premises data center and requires frequent and low-latency access to large media files. The company wants to implement a storage solution that maintains application performance while keeping costs low.
Which approach should the company choose to meet these requirements in the most cost-effective way?
Use Mountpoint for Amazon S3 on the on-premises rendering servers to facilitate low-latency access to the S3 bucket
Set up a dedicated on-premises storage array that periodically fetches data from Amazon S3 using a custom-built application. Mount this storage volume on the rendering servers as their primary working directory
Deploy an Amazon FSx for Lustre file system and sync media data from Amazon S3 into it using DataSync. Mount the FSx file system on the on-premises render servers using a VPN tunnel
Correct answer
Set up an Amazon S3 File Gateway to provide storage for the on-premises application


A data analytics team at a global media firm is building a new analytics platform to process large volumes of both historical and real-time data. This data is stored in Amazon S3. The team wants to implement a serverless solution that allows them to query the data directly using SQL. Additionally, the solution must ensure that all data is encrypted at rest and automatically replicated to another AWS Region to support business continuity.
Which solution will meet these requirements with the LEAST operational overhead?

Correct answer
Create an Amazon S3 bucket configured with server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Athena to run SQL queries on the data

Enable Cross-Region Replication (CRR) on the existing Amazon S3 bucket. Apply server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Use Amazon Athena to run SQL queries on the replicated data

Enable Cross-Region Replication (CRR) on the existing Amazon S3 bucket. Apply server-side encryption using Amazon S3 managed keys (SSE-S3). Use Amazon Athena to run SQL queries on the replicated data

Create an Amazon S3 bucket configured with server-side encryption using Amazon S3 managed keys (SSE-S3). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Redshift Spectrum to query the S3 data using SQL



A media company operates a web application that enables users to upload photos. These uploads are stored in an Amazon S3 bucket located in the eu-west-2 Region. To enhance performance and provide secure access under a custom domain name, the company wants to integrate Amazon CloudFront for uploads to the S3 bucket. The architecture must support secure HTTPS connections using a custom domain, and the upload process must ensure optimal speed and security.
Which combination of actions will fulfill these requirements? (Select two)

Create a CloudFront distribution with an S3 static website endpoint as the origin and enable upload operations

Set up a custom origin request policy in CloudFront that includes all viewer headers and query strings. Enable S3 Object Ownership to allow CloudFront to assume control of uploaded files via a signed URL

Request a public certificate from AWS Certificate Manager (ACM) in the eu-west-2 Region and associate it with the CloudFront distribution

Correct selection
Set up Amazon S3 to accept uploads from CloudFront by enabling origin access control (OAC)

Correct selection
Request a public certificate from AWS Certificate Manager (ACM) in the us-east-1 Region and associate it with the CloudFront distribution


An enterprise is developing an internal compliance framework for its cloud infrastructure hosted on AWS. The enterprise uses AWS Organizations to group accounts under various organizational units (OUs) based on departmental function. As part of its governance controls, the security team mandates that all Amazon EC2 instances must be tagged to indicate the level of data classification — either 'confidential' or 'public'. Additionally, the organization must ensure that IAM users cannot launch EC2 instances without assigning a classification tag, nor should they be able to remove the tag from running instances. A solutions architect must design a solution to meet these compliance controls while minimizing operational overhead.
Which combination of steps will meet these requirements? (Select two)

Enable AWS Config rules to detect noncompliant EC2 instances. Trigger an AWS Systems Manager Automation runbook to reapply missing tags automatically when noncompliance is detected
Create a tag enforcement Lambda function that runs on a schedule to identify EC2 instances without the required tag. The function sends a notification to administrators and optionally shuts down noncompliant resources
Correct selection
Define a tag policy in AWS Organizations that enforces the dataClassification key and restricts values to 'confidential' and 'public'. Attach this tag policy to the applicable organizational unit (OU) to enforce uniform tagging behavior across accounts
Correct selection
Create a service control policy (SCP) that denies the ec2:RunInstances API action unless the required tag key is present in the request. Create a second SCP that denies the ec2:DeleteTags action for EC2 resources. Attach both SCPs to the relevant OU in AWS Organizations
Use AWS Identity and Access Management (IAM) permission boundaries to restrict EC2-related actions unless the dataClassification tag is present. Apply these boundaries to all IAM roles used for EC2 provisioning


The infrastructure team at a company maintains 5 different VPCs (let's call these VPCs A, B, C, D, E) for resource isolation. Due to the changed organizational structure, the team wants to interconnect all VPCs together. To facilitate this, the team has set up VPC peering connection between VPC A and all other VPCs in a hub and spoke model with VPC A at the center. However, the team has still failed to establish connectivity between all VPCs.
As a solutions architect, which of the following would you recommend as the MOST resource-efficient and scalable solution?
Use an internet gateway to interconnect the VPCs
Correct answer
Use AWS transit gateway to interconnect the VPCs
Use a VPC endpoint to interconnect the VPCs
Establish VPC peering connections between all VPCs



The engineering team at an e-commerce company uses an AWS Lambda function to write the order data into a single DB instance Amazon Aurora cluster. The team has noticed that many order- writes to its Aurora cluster are getting missed during peak load times. The diagnostics data has revealed that the database is experiencing high CPU and memory consumption during traffic spikes. The team also wants to enhance the availability of the Aurora DB.
Which of the following steps would you combine to address the given scenario? (Select two)
Correct selection
Handle all read operations for your application by connecting to the reader endpoint of the Amazon Aurora cluster so that Aurora can spread the load for read-only connections across the Aurora replica
Create a standby Aurora instance in another Availability Zone to improve the availability as the standby can serve as a failover target
Correct selection
Create a replica Aurora instance in another Availability Zone to improve the availability as the replica can serve as a failover target
Use Amazon EC2 instances behind an Application Load Balancer to write the order data into Amazon Aurora cluster
Increase the concurrency of the AWS Lambda function so that the order-writes do not get missed during traffic spikes


A retail enterprise is expanding its hybrid IT infrastructure and plans to securely connect its on-premises corporate network to its AWS environment. The company wants to ensure that all data exchanged between on-premises systems and AWS is encrypted at both the network and session layers. Additionally, the solution must incorporate granular security controls that restrict unnecessary or unauthorized access between the cloud and on-premises environments. A solutions architect must recommend a scalable and secure approach that supports these goals.
Which solution best meets these requirements?
Establish a dedicated AWS Direct Connect connection between the corporate network and AWS. Configure VPC route tables to control traffic flow and use security groups and network ACLs to restrict access as needed
Correct answer
Set up AWS Site-to-Site VPN to connect the on-premises network to the AWS VPC. Use route tables to manage traffic flow and configure security groups and network ACLs to allow only authorized communication between systems
Use AWS Client VPN to allow corporate users to connect to the VPC individually. Manage access controls with security groups and IAM policies
Set up a bastion host in a public subnet of the VPC to provide SSH-based access to AWS resources from the corporate network. Use security groups to control access
Overall explanation


A financial services company is looking to move its on-premises IT infrastructure to AWS Cloud. The company has multiple long-term server bound licenses across the application stack and the CTO wants to continue to utilize those licenses while moving to AWS.
As a solutions architect, which of the following would you recommend as the MOST cost-effective solution?
Use Amazon EC2 reserved instances (RI)
Use Amazon EC2 dedicated instances
Use Amazon EC2 on-demand instances
Correct answer
Use Amazon EC2 dedicated hosts



A company has multiple Amazon EC2 instances operating in a private subnet which is part of a custom VPC. These instances are running an image processing application that needs to access images stored on Amazon S3. Once each image is processed, the status of the corresponding record needs to be marked as completed in a Amazon DynamoDB table.
How would you go about providing private access to these AWS resources which are not part of this custom VPC?
Create a separate interface endpoint for Amazon S3 and Amazon DynamoDB each. Then connect to these services by adding these as targets in the route table of the custom VPC
Create a gateway endpoint for Amazon DynamoDB and add it as a target in the route table of the custom VPC. Create an Origin Access Identity for Amazon S3 and then connect to the S3 service using the private IP address
Create a gateway endpoint for Amazon S3 and add it as a target in the route table of the custom VPC. Create an interface endpoint for Amazon DynamoDB and then add it as a target in the route table of the custom VPC
Correct answer
Create a separate gateway endpoint for Amazon S3 and Amazon DynamoDB each. Add two new target entries for these two gateway endpoints in the route table of the custom VPC


A social media application lets users upload photos and perform image editing operations. The application offers two classes of service: pro and lite. The product team wants the photos submitted by pro users to be processed before those submitted by lite users. Photos are uploaded to Amazon S3 and the job information is sent to Amazon SQS.
As a solutions architect, which of the following solutions would you recommend?
Create two Amazon SQS standard queues: one for pro and one for lite. Set the lite queue to use short polling and the pro queue to use long polling
Correct answer
Create two Amazon SQS standard queues: one for pro and one for lite. Set up Amazon EC2 instances to prioritize polling for the pro queue over the lite queue
Create one Amazon SQS standard queue. Set the visibility timeout of the pro photos to zero. Set up Amazon EC2 instances to prioritize visibility settings so pro photos are processed first
Create two Amazon SQS FIFO queues: one for pro and one for lite. Set the lite queue to use short polling and the pro queue to use long polling


An e-commerce company uses Amazon RDS MySQL DB to store the data. The analytics department at the company runs its reports on the same database. The engineering team has noticed sluggish performance on the database when the analytics reporting process is in progress.
As an AWS Certified Solutions Architect - Associate, which of the following would you suggest as the MOST cost-optimal solution to improve the performance?
Correct answer
Create a read-replica with the same compute capacity and the same storage capacity as the primary. Point the reporting queries to run against the read replica
Create a standby instance in a multi-AZ configuration with the same compute capacity and the same storage capacity as the primary. Point the reporting queries to run against the standby instance
Create a standby instance in a multi-AZ configuration with half compute capacity and half storage capacity as the primary. Point the reporting queries to run against the standby instance
Create a read-replica with half compute capacity and half storage capacity as the primary. Point the reporting queries to run against the read replica


A global photography startup hosts a static image-sharing site on an Amazon S3 bucket. The website allows users from different parts of the world to upload, view, and download photos through their mobile devices. As the platform has gained popularity, users have started experiencing latency issues, especially when uploading and downloading images. The team needs a solution to enhance global performance but wants to implement it with minimal development effort and without redesigning the application.
Which solution will most effectively address the performance issues with the least operational overhead?
Create multiple S3 buckets in different Regions and replicate image data based on user location. Configure CloudFront to upload and download from the nearest bucket
Migrate the website from S3 to Amazon EC2 instances in multiple Regions. Use an Application Load Balancer with AWS Global Accelerator to distribute global traffic and reduce latency
Correct answer
Deploy an Amazon CloudFront distribution with the S3 bucket as the origin to improve download speeds. Enable S3 Transfer Acceleration to reduce upload latency for global users
Enable AWS Global Accelerator on the S3 bucket to accelerate both uploads and downloads. Reconfigure the website to route requests through the accelerator


You are deploying a critical monolith application that must be deployed on a single web server, as it hasn't been created to work in distributed mode. Still, you want to make sure your setup can automatically recover from the failure of an Availability Zone (AZ).
Which of the following options should be combined to form the MOST cost-efficient solution? (Select three)
Correct selection
Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=1, desired=1
Create a Spot Fleet request
Correct selection
Assign an Amazon EC2 Instance Role to perform the necessary API calls
Correct selection
Create an elastic IP address (EIP) and use the Amazon EC2 user-data script to attach it
Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=2, desired=2
Create an Application Load Balancer and a target group with the instance(s) of the Auto Scaling Group


A healthcare company runs a fleet of Amazon EC2 instances in two private subnets (named PR1 and PR2) across two Availability Zones (AZs) named A1 and A2. The Amazon EC2 instances need access to the internet for operating system patch management and third-party software maintenance. To facilitate this, the engineering team at the company wants to set up two Network Address Translation gateways (NAT gateways) in a highly available configuration.
Which of the following options would you suggest?
Set up a total of one NAT gateway. NAT gateway N1 should be set up in public subnet PU1 in any of the Availability Zones A1 or A2
Set up a total of two NAT gateways. Both NAT gateways N1 and N2 should be set up in a single public subnet PU1 in any of the Availability Zones A1 or A2
Set up a total of two NAT gateways. NAT gateway N1 should be set up in private subnet PR1 in Availability Zone A1. NAT gateway N2 should be set up in private subnet PR2 in Availability Zone A2
Correct answer
Set up a total of two NAT gateways. NAT gateway N1 should be set up in public subnet PU1 in Availability Zone A1. NAT gateway N2 should be set up in public subnet PU2 in Availability Zone A2


The engineering team at an IT company is deploying an Online Transactional Processing (OLTP) application that needs to support relational queries. The application will have unpredictable spikes of usage that the team does not know in advance.
Which database would you recommend using?
Correct answer
Amazon Aurora Serverless
Amazon ElastiCache
Amazon DynamoDB with Provisioned Capacity and Auto Scaling
Amazon DynamoDB with On-Demand Capacity



A company is developing a document management application on AWS. The application runs on Amazon EC2 instances in multiple Availability Zones (AZs). The company requires the document store to be highly available and the documents need to be returned immediately when requested. The engineering team has configured the application to use Amazon Elastic Block Store (Amazon EBS) to store the documents but the team is willing to consider other options to meet the availability requirement.
As a solutions architect, which of the following will you recommend?
Create snapshots for the Amazon EBS volumes regularly and then build new volumes using those snapshots in additional Availability Zones
Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 Glacier as the document store
Provision at least three Provisioned IOPS Amazon Instance Store volumes for the Amazon EC2 instances and then mount these volumes to multiple Amazon EC2 instances
Correct answer
Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 as the document store


A company manages a multi-tier social media application that runs on Amazon Elastic Compute Cloud (Amazon EC2) instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto Scaling group across multiple Availability Zones (AZs) and use an Amazon Aurora database. As an AWS Certified Solutions Architect – Associate, you have been tasked to make the application more resilient to periodic spikes in read request rates.
Which of the following solutions would you recommend for the given use-case? (Select two)
Correct selection
Use Amazon Aurora Replica
Use AWS Direct Connect
Use AWS Shield
Correct selection
Use Amazon CloudFront distribution in front of the Application Load Balancer
Use AWS Global Accelerator


Your application is deployed on Amazon EC2 instances fronted by an Application Load Balancer. Recently, your infrastructure has come under attack. Attackers perform over 100 requests per second, while your normal users only make about 5 requests per second.
How can you efficiently prevent attackers from overwhelming your application?
Use AWS Shield Advanced and setup a rate-based rule
Correct answer
Use an AWS Web Application Firewall (AWS WAF) and setup a rate-based rule
Configure Sticky Sessions on the Application Load Balancer
Define a network access control list (network ACL) on your Application Load Balancer



A company is deploying a publicly accessible web application. To accomplish this, the engineering team has designed the VPC with a public subnet and a private subnet. The application will be hosted on several Amazon EC2 instances in an Auto Scaling group. The team also wants Transport Layer Security (TLS) termination to be offloaded from the Amazon EC2 instances.
Which solution should a solutions architect implement to address these requirements in the most secure manner?
Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
Set up a Network Load Balancer in the private subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
Correct answer
Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer
Set up a Network Load Balancer in the private subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer


An application is hosted on multiple Amazon EC2 instances in the same Availability Zone (AZ). The engineering team wants to set up shared data access for these Amazon EC2 instances using Amazon EBS Multi-Attach volumes.
Which Amazon EBS volume type is the correct choice for these Amazon EC2 instances?
Cold HDD Amazon EBS volumes
Throughput Optimized HDD Amazon EBS volumes
General-purpose SSD-based Amazon EBS volumes
Correct answer
Provisioned IOPS SSD Amazon EBS volumes


A digital media company wants to track user engagement across its streaming platform by capturing events such as video starts, pauses, and search queries. These events must be ingested and analyzed in real time to improve user experience and optimize recommendations. The platform experiences unpredictable spikes in traffic during popular content releases. The company needs a highly scalable and serverless solution that can seamlessly adjust to changing workloads without manual provisioning.
Which solution will meet these requirements in the MOST efficient and scalable way?
Correct answer
Use an Amazon Kinesis Data Streams stream in on-demand capacity mode to ingest user engagement data. Configure an AWS Lambda function as a consumer to process the events in real time
Deploy a fleet of Amazon EC2 instances running Apache Kafka to ingest clickstream data. Set up custom scripts to manually scale the Kafka cluster based on CPU usage. Use Amazon Athena to run periodic queries on stored clickstream logs
Use Amazon Simple Notification Service (Amazon SNS) to publish clickstream events. Subscribe an Amazon SQS standard queue to receive the events. Process the events in batches with AWS Glue jobs scheduled at fixed intervals
Use Amazon Kinesis Data Firehose to ingest user events. Set the destination as Amazon S3. Use Amazon Athena with scheduled queries to analyze the data periodically
