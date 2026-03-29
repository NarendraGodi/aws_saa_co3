# AWS SAA-C03 Practice Questions - Part 3

Total Questions: 194

---

## Question 1

**Q:** Which solution is the most cost-effective?

**A:** Write the log files to an Amazon S3 bucket. Create an event notification to invoke an AWS Lambda function that will process the files

---

## Question 2

**Q:** How can a solutions architect patch all the instances quickly to remediate a security exposure?

**A:** Configure AWS Systems Manager Patch Manager to apply the patch to all EC2 instances.

---

## Question 3

**Q:** The database layer of an on-premises web application is being migrated to AWS. The database uses a multi-threaded, in-memory caching layer to improve performance for repeated queries. Which service would be the most suitable replacement for the database cache?

**A:** Amazon ElastiCache Memcached

---

## Question 4

**Q:** What is the best way to meet this requirement?

**A:** Extend the file share environment to Amazon FSx for Windows File Server with a Multi-AZ configuration. Migrate all the data to FSx for Windows File Server.

---

## Question 5

**Q:** A Solutions Architect manages multiple Amazon RDS MySQL databases. To improve security, the Solutions Architect wants to enable secure user access with short-lived credentials. How can these requirements be met?

**A:** Create the MySQL user accounts to use the AWSAuthenticationPlugin with IAM

---

## Question 6

**Q:** Which actions should a Solutions Architect take to encrypt and query the data?

**A:** Use AWS KMS encryption keys for the S3 bucket and use Amazon Athena to query the data

---

## Question 7

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Set up an Amazon S3 bucket. The application should be updated to use S3 buckets to store documents. Store the object metadata in the existing database.

---

## Question 8

**Q:** According to principal of least privilege, which option out of the below will fulfill the requirement to provide the necessary access for the product manager?

**A:** Share the dashboard from the CloudWatch console. Enter the client’s email address and complete the sharing steps. Provide a shareable link for the dashboard to the product manager.

---

## Question 9

**Q:** Which solution requires the LEAST amount of effort?

**A:** Create an Amazon Elastic File System (Amazon EFS) file system and mount it on the individual Amazon EC2 instances

---

## Question 10

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Deploy a Gateway Load Balancer in the inspection VPC. Create a Gateway Load Balancer endpoint to receive the incoming packets and forward the packets to the appliance.

---

## Question 11

**Q:** How should the network connectivity be configured?

**A:** Create an AWS Transit Gateway and share it with each account using AWS Resource Access Manager

---

## Question 12

**Q:** What should a solutions architect do to meet these requirements?

**A:** Create an Application Load Balancer with Auto Scaling groups across multiple Availability Zones. Store data on Amazon EFS and mount a target on each instance

---

## Question 13

**Q:** Which of the following options makes sure that database can only be accessed by the application layer?

**A:** Create a security group that allows inbound traffic from the security group that is assigned to instances in the private subnets. Attach the security group to the DB instances.

---

## Question 14

**Q:** A company runs an API on a Linux server in their on-premises data center. The company are planning to migrate the API to the AWS cloud. The company require a highly available, scalable and cost-effective solution. What should a Solutions Architect recommend?

**A:** Migrate the API to Amazon API Gateway and use AWS Lambda as the backend

---

## Question 15

**Q:** How should the solutions architect generate the information with the LEAST operational overhead?

**A:** Use Cost Explorer's granular filtering feature to perform an in-depth analysis of EC2 costs based on instance types.

---

## Question 16

**Q:** What should a solutions architect do to meet these requirements in the easiest way possible?

**A:** Use AWS Systems Manager Run Command to run a custom command that installs the tool on all the EC2 instances.

---

## Question 17

**Q:** Which solution will meet these requirements?

**A:** Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate users and groups.

---

## Question 18

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Create an Amazon EventBridge rule for the CreateImage API call. Configure the target as an Amazon SNS topic to send an alert when a Createlmage API call is detected.

---

## Question 19

**Q:** Which option will meet these requirements?

**A:** Amazon Elastic File System (Amazon EFS) with the Standard storage class.

---

## Question 20

**Q:** Which solution will meet these requirements in the MOST operationally efficient way?

**A:** Use Amazon Aurora with MySQL compatibility. Direct the reporting functions to use one of the Aurora Replicas.

---

## Question 21

**Q:** Which solution will meet these requirements with the LEAST effort?

**A:** Search CloudTrail logs with Amazon QuickSight. Create a dashboard to identify the errors.

---

## Question 22

**Q:** An application is running in a private subnet of an Amazon VPC and must have outbound internet access for downloading updates. The Solutions Architect does not want the application exposed to inbound connection attempts. Which steps should be taken?

**A:** Create a NAT gateway and attach an internet gateway to the VPC

---

## Question 23

**Q:** Which of the following is recommended to implement the DR solution across regions cost-effectively?

**A:** Create Amazon Machine Images (AMIs) to back up the EC2 instances. Copy the AMIs to a secondary AWS Region. Automate infrastructure deployment in the secondary Region by using AWS CloudFormation.

---

## Question 24

**Q:** How should the scaling be changed to address the staff complaints and keep costs to a minimum?

**A:** Implement a target tracking action triggered at a lower CPU threshold, and decrease the cooldown period

---

## Question 25

**Q:** Which solution will meet these requirements?

**A:** Use Amazon Transcribe for multiple speaker recognition. Use Amazon Athena for transcript file analysis.

---

## Question 26

**Q:** Which solution will meet these requirements?

**A:** Use Amazon Macie. Create an Amazon EventBridge rule to filter the ‘SensitiveData:S3Object/Health’ event type from Macie findings and trigger an Amazon Simple Email Service (Amazon SES) notification to the compliance team.

---

## Question 27

**Q:** A global logistics company collects shipment tracking information, which updates every few seconds. The company wishes to perform real-time analysis on these data updates to monitor shipment progress and predict delays, after which they want the data to be ingested into their Amazon S3-based data lake. Which solution will fulfill these requirements with the MOST operational efficiency?

**A:** Use Amazon Kinesis Data Firehose for data ingestion and Amazon Managed Service for Apache Flink for real-time analysis.

---

## Question 28

**Q:** Which strategy meets these requirements with the LEAST amount of effort?

**A:** Use the global key of AWS Organizations within a bucket policy using the aws:PrincipalOrgID key to allow access only to accounts which are part of the Organization.

---

## Question 29

**Q:** Which solution will meet these requirements?

**A:** Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using an Amazon Simple Queue Service (Amazon SQS) queue.

---

## Question 30

**Q:** Which actions should a Solutions Architect take?

**A:** Migrate the data to Amazon FSx for Windows File Server using AWS DataSync

---

## Question 31

**Q:** Which solution will meet these requirements?

**A:** Create a new AWS Key Management Service (AWS KMS) key. Enable Amazon EKS KMS secrets encryption on the Amazon EKS cluster.

---

## Question 32

**Q:** Which solution will meet these requirements?

**A:** Set up a warm standby Amazon RDS for PostgreSQL database on AWS. Configure AWS Database Migration Service (AWS DMS) to use change data capture (CDC).

---

## Question 33

**Q:** How should this be accomplished?

**A:** Take a snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot

---

## Question 34

**Q:** A Solutions Architect is designing a migration strategy for a company moving to the AWS Cloud. The company use a shared Microsoft filesystem that uses Distributed File System Namespaces (DFSN). What will be the MOST suitable migration strategy for the filesystem?

**A:** Use AWS DataSync to migrate to Amazon FSx for Windows File Server

---

## Question 35

**Q:** Which DR strategy should a Solutions Architect recommend?

**A:** Warm standby

---

## Question 36

**Q:** What can be done to allow the nodes to join the EKS cluster?

**A:** Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.

---

## Question 37

**Q:** Which solution will meet these requirements?

**A:** Implement geographical restrictions on CloudFront content using a deny list and create a custom error message.

---

## Question 38

**Q:** Which solution will meet these requirements with the LEAST amount of administrative effort?

**A:** Set up AWS Firewall Manager in both Regions. Centrally configure AWS WAF rules.

---

## Question 39

**Q:** Which action should a solutions architect take to quickly provision the necessary connectivity?

**A:** Configure a Virtual Private Gateway

---

## Question 40

**Q:** What should a solutions architect do to meet these requirements?

**A:** Use Spot Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.

---

## Question 41

**Q:** What should a solutions architect do to meet these requirements?

**A:** Use AWS Config to track configuration changes and AWS CloudTrail to record API calls.

---

## Question 42

**Q:** Which solution meets these requirements?

**A:** Migrate the databases to Amazon Aurora Serverless (Aurora MySQL).

---

## Question 43

**Q:** Which solution will meet these requirements?

**A:** Implement CloudFront signed cookies for authenticated students.

---

## Question 44

**Q:** What is the MOST cost-effective solution?

**A:** Order 7 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier

---

## Question 45

**Q:** What is the SIMPLEST method of achieving the requirements?

**A:** Create a service control policy in the root organizational unit to deny access to the services or actions

---

## Question 46

**Q:** Which solution would best satisfy these requirements?

**A:** Create AWS Service Catalog portfolios for the clients.

---

## Question 47

**Q:** How can a solutions architect integrate the microservices and allow them to scale independently?

**A:** Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue

---

## Question 48

**Q:** Which solution meets these requirements?

**A:** Set up S3 bucket policies to allow access from a VPC endpoint.

---

## Question 49

**Q:** Which system architecture should the solutions architect recommend?

**A:** Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function.

---

## Question 50

**Q:** Which solution is MOST cost-effective?

**A:** Create an Amazon S3 bucket and host the website there.

---

## Question 51

**Q:** Which storage classes should be used?

**A:** Store data in STANDARD for 90 days then transition the data to DEEP_ARCHIVE

---

## Question 52

**Q:** What is the most efficient solution to help the company identify these security events with the LEAST amount of operational effort?

**A:** Use Amazon Athena to directly query CloudTrail logs for failed logins and unauthorized activities.

---

## Question 53

**Q:** Which AWS service can the administrator use to protect the company against attacks?

**A:** Amazon GuardDuty

---

## Question 54

**Q:** What should a solutions architect do to maintain the desired performance across all instances in the group?

**A:** Use a target tracking policy to dynamically scale the Auto Scaling group

---

## Question 55

**Q:** How can a Solutions Architect meet these requirements?

**A:** Launch the EC2 instances in a private subnet and create an Application Load Balancer in a public subnet

---

## Question 56

**Q:** Which solution should the company use to address this situation with the LEAST operational overhead?

**A:** Enable automatic storage scaling for the MySQL instance.

---

## Question 57

**Q:** How should scaling be configured?

**A:** Use a target tracking policy that keeps the average aggregate CPU utilization at 40%

---

## Question 58

**Q:** Which solution will best meet these requirements?

**A:** Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization.

---

## Question 59

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Utilize Lake Formation tag-based access control to authorize and grant cross-account permissions for the required data to the marketing team accounts.

---

## Question 60

**Q:** Which solution will meet these requirements?

**A:** Use AWS Storage Gateway to move the existing data to Amazon S3. Use AWS CloudTrail to log management events.

---

## Question 61

**Q:** Which solution will meet these requirements?

**A:** Implement the application as an AWS Lambda function configured with 1.5 GB of memory. Use Amazon EventBridge to schedule the function to run every 15 minutes.

---

## Question 62

**Q:** A company runs a streaming media service and the content is stored on Amazon S3. The media catalog server pulls updated content from S3 and can issue over 1 million read operations per second for short periods. Latency must be kept under 5ms for these updates. Which solution will provide the BEST performance for the media catalog updates?

**A:** Update the application code to use an Amazon ElastiCache for Redis cluster

---

## Question 63

**Q:** What is the optimal storage solution that provides the required performance and is cost-effective?

**A:** Use Amazon Instance Store

---

## Question 64

**Q:** Which solution will meet these requirements?

**A:** Develop a WebSocket API using Amazon API Gateway. Host the application in Amazon Elastic Kubernetes Service (EKS) in a private subnet. Establish a private VPC link for the API Gateway to securely access the Amazon EKS cluster.

---

## Question 65

**Q:** A tool needs to analyze data stored in an Amazon S3 bucket. Processing the data takes a few seconds and results are then written to another S3 bucket. Less than 256 MB of memory is needed to run the process. What would be the MOST cost-effective compute solutions for this use case?

**A:** AWS Lambda functions

---

## Question 66

**Q:** An application runs on EC2 instances in a private subnet behind an Application Load Balancer in a public subnet. The application is highly available and distributed across multiple AZs. The EC2 instances must make API calls to an internet-based service. How can the Solutions Architect enable highly available internet connectivity?

**A:** Create a NAT gateway in the public subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT gateway

---

## Question 67

**Q:** How can the Solutions Architect meet the security team’s requirements?

**A:** Create gateway VPC endpoints for Amazon S3 and DynamoDB.

---

## Question 68

**Q:** An e-commerce web application needs a highly scalable key-value database. Which AWS database service should be used?

**A:** Amazon DynamoDB

---

## Question 69

**Q:** Which approach will best meet these requirements?

**A:** Implement AWS Global Accelerator ahead of the NLBs and align the Global Accelerator endpoint to use the appropriate listener ports.

---

## Question 70

**Q:** What should a solutions architect recommend?

**A:** Install an Amazon CloudWatch agent on the instances. Run an appropriate script on a set schedule. Monitor SwapUtilization metrics in CloudWatch

---

## Question 71

**Q:** What should be done to enable encryption for future backups?

**A:** Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot

---

## Question 72

**Q:** Which storage option should the solutions architect recommend?

**A:** 1. Create an Amazon EFS file share and establish an IAM role that allows Fargate to communicate with Amazon EFS.

---

## Question 73

**Q:** An application makes calls to a REST API running on Amazon EC2 instances behind an Application Load Balancer (ALB). Most API calls complete quickly. However, a single endpoint is making API calls that require much longer to complete and this is introducing overall latency into the system. What steps can a Solutions Architect take to minimize the effects of the long-running API calls?

**A:** Create an Amazon SQS queue and decouple the long-running API calls

---

## Question 74

**Q:** Which approach would fulfill these needs with the MINIMUM operational burden?

**A:** Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets.

---

## Question 75

**Q:** Which scalable solutions should the solutions architect recommend?

**A:** Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)

---

## Question 76

**Q:** Which solution should a Solutions Architect choose to this requirement?

**A:** Configure Amazon EBS encryption and Amazon RDS encryption with AWS KMS keys to encrypt instance and database volumes.

---

## Question 77

**Q:** How can the required connectivity be configured?

**A:** Associate the Direct Connect gateway to a virtual private gateway in account A and B

---

## Question 78

**Q:** Which service should the Solutions Architect recommend?

**A:** Amazon ElastiCache Redis

---

## Question 79

**Q:** Which EC2 solution BEST meets these requirements?

**A:** Launch the EC2 instances in a cluster placement group in one Availability Zone

---

## Question 80

**Q:** How can the Solutions Architect meet this requirement with the LEAST operational overhead?

**A:** Create an organization in AWS Organizations that includes all accounts and create a service control policy (SCP) that denies the launch of large EC2 instances.

---

## Question 81

**Q:** Which solution is the BEST fit for these requirements?

**A:** Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment

---

## Question 82

**Q:** An application uses a MySQL database running on an Amazon EC2 instance. The application generates high I/O and constant writes to a single table on the database. Which Amazon EBS volume type will provide the MOST consistent performance and low latency?

**A:** Provisioned IOPS SSD (io1)

---

## Question 83

**Q:** What should a solutions architect use to accomplish this?

**A:** Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)

---

## Question 84

**Q:** How can this be achieved?

**A:** Create a Multi-AZ RDS Read Replica of the production RDS DB instance

---

## Question 85

**Q:** How should a solutions architect configure the replication?

**A:** Create an additional S3 bucket with versioning in another Region and configure cross-Region replication

---

## Question 86

**Q:** Which solution should the solutions architect suggest?

**A:** Set up an Amazon API Gateway and use AWS Lambda functions

---

## Question 87

**Q:** Which DR strategy should a Solutions Architect recommend?

**A:** Multi-site

---

## Question 88

**Q:** Which AWS solution can achieve this?

**A:** Amazon Aurora Global Database.

---

## Question 89

**Q:** Which service should the solutions architect choose?

**A:** Amazon CloudFront

---

## Question 90

**Q:** What is the most secure and reliable method for gathering this data?

**A:** Create a VPC flow log for each network interface associated with the ELB

---

## Question 91

**Q:** Which solution will meet these requirements?

**A:** Migrate the data and applications to Amazon RDS instances. Enable encryption at rest using AWS Key Management Service (AWS KMS).

---

## Question 92

**Q:** What is the LEAST expensive EBS volume type for this use case?

**A:** Cold HDD (sc1)

---

## Question 93

**Q:** Which solution would meet these requirements MOST efficiently?

**A:** Use Amazon API Gateway along with AWS Lambda functions with provisioned concurrency.

---

## Question 94

**Q:** What should a solutions architect recommend to ensure the application is able to handle the workload and avoid downtime?

**A:** Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule

---

## Question 95

**Q:** Which datastore will be the best fit for these requirements?

**A:** Amazon DynamoDB

---

## Question 96

**Q:** Which solution will meet these requirements?

**A:** Use Provisioned IOPS SSD (io2) EBS volumes with Amazon EBS Multi-Attach.

---

## Question 97

**Q:** Which solution will be the MOST effective in achieving this?

**A:** Configure an Amazon RDS Proxy for the database and modify the application to connect to the proxy endpoint.

---

## Question 98

**Q:** How can this be accomplished?

**A:** Use Lambda@Edge to compress the files as they are sent to users.

---

## Question 99

**Q:** Which method provides the MOST operationally efficient way to fulfill these requirements?

**A:** AWS AppSync with multiple data sources and resolvers.

---

## Question 100

**Q:** An application requires a MySQL database which will only be used several times a week for short periods. The database needs to provide automatic instantiation and scaling. Which database service is most suitable?

**A:** Amazon Aurora Serverless

---

## Question 101

**Q:** Which of the following Amazon EC2 instance topologies should this application be deployed on?

**A:** The Amazon EC2 instances should be deployed in a cluster placement group so that the underlying workload can benefit from low network latency and high network throughput

---

## Question 102

**Q:** Which of the following options is the MOST cost-optimal and resource-efficient solution to build this fleet of Amazon EC2 instances?

**A:** Use Instance Store based Amazon EC2 instances

---

## Question 103

**Q:** Which of the following will you recommend to meet these requirements?

**A:** Push score updates to Amazon Kinesis Data Streams which uses an AWS Lambda function to process these updates and then store these processed updates in Amazon DynamoDB

---

## Question 104

**Q:** Which AWS solution will best meet the company’s requirements for modernization while ensuring that all data remains on premises?

**A:** Install an AWS Outposts rack in the company’s data center. Use Amazon EKS Anywhere on Outposts to run containerized workloads locally while integrating with AWS APIs

---

## Question 105

**Q:** Given this scenario, which of the following is correct regarding the charges for this image transfer?

**A:** The junior scientist does not need to pay any transfer charges for the image upload

---

## Question 106

**Q:** Which solution will meet these requirements?

**A:** Instruct the partner to create a Network Load Balancer (NLB) in front of the Amazon RDS for MySQL instance. Use AWS PrivateLink to expose the NLB as an interface VPC endpoint in the research company’s VPC

---

## Question 107

**Q:** Which configuration should be used to meet this changed requirement?

**A:** Configure AWS Web Application Firewall (AWS WAF) on the Application Load Balancer in a Amazon Virtual Private Cloud (Amazon VPC)

---

## Question 108

**Q:** Which of the following AWS services represents the best solution for this use-case?

**A:** AWS Global Accelerator

---

## Question 109

**Q:** Which of the following is the BEST solution for this use-case?

**A:** Use server-side encryption with AWS Key Management Service keys (SSE-KMS) to encrypt the user data on Amazon S3

---

## Question 110

**Q:** As an AWS Certified Solutions Architect – Associate, can you suggest a way to lower the storage costs while fulfilling the business requirements?

**A:** Configure a lifecycle policy to transition the objects to Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) after 30 days

---

## Question 111

**Q:** Which of the following AWS services can facilitate the migration of these workloads?

**A:** Amazon FSx for Windows File Server

---

## Question 112

**Q:** At this point in time, what entities exist in Region B?

**A:** 1 Amazon EC2 instance, 1 AMI and 1 snapshot exist in Region B

---

## Question 113

**Q:** As a Solutions Architect, which of the following would you suggest as the MOST efficient solution to improve the application performance?

**A:** Enable Amazon DynamoDB Accelerator (DAX) for Amazon DynamoDB and Amazon CloudFront for Amazon S3

---

## Question 114

**Q:** Which is the MOST effective way to address this issue so that such incidents do not recur?

**A:** Use permissions boundary to control the maximum permissions employees can grant to the IAM principals

---

## Question 115

**Q:** As a solutions architect, which of the following solutions would you suggest to help address the given requirement?

**A:** Use Amazon GuardDuty to monitor any malicious activity on data stored in Amazon S3. Use security assessments provided by Amazon Inspector to check for vulnerabilities on Amazon EC2 instances

---

## Question 116

**Q:** Which of the following AWS services is BEST suited to accelerate the aforementioned chip design process?

**A:** Amazon FSx for Lustre

---

## Question 117

**Q:** As a solutions architect, which of the following solutions would you recommend to the company?

**A:** Use AWS Direct Connect plus virtual private network (VPN) to establish a connection between the data center and AWS Cloud

---

## Question 118

**Q:** Which of the following is the MOST cost-effective strategy for storing this intermediary query data?

**A:** Store the intermediary query results in Amazon S3 Standard storage class

---

## Question 119

**Q:** As a solutions architect, which of the following steps would you recommend?

**A:** Create a new IAM role with the required permissions to access the resources in the production environment. The users can then assume this IAM role while accessing the resources from the production environment

---

## Question 120

**Q:** Which of the following options addresses the given use case?

**A:** Leverage Amazon API Gateway with Amazon Kinesis Data Analytics

---

## Question 121

**Q:** As a solutions architect, which of the following would you suggest as the BEST possible solution to this issue?

**A:** Amazon SNS message deliveries to AWS Lambda have crossed the account concurrency quota for AWS Lambda, so the team needs to contact AWS support to raise the account limit

---

## Question 122

**Q:** As a solutions architect, what are your recommendations to address these guidelines? (Select two) ?

**A:** Multi-AZ follows synchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow asynchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region

---

## Question 123

**Q:** Which of the following correctly summarizes these capabilities for the given database?

**A:** Multi-AZ follows synchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow asynchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region

---

## Question 124

**Q:** Which of the following options represents the best solution for this use case?

**A:** Leverage multi-AZ configuration of Amazon RDS Custom for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system

---

## Question 125

**Q:** Which of the following is the MOST resource efficient and cost-optimal way of addressing this issue?

**A:** Change the application architecture to create customer-specific custom prefixes within the single Amazon S3 bucket and then upload the daily files into those prefixed locations

---

## Question 126

**Q:** As a solutions architect, what would you recommend so that the application runs near its peak performance state?

**A:** Configure the Auto Scaling group to use target tracking policy and set the CPU utilization as the target metric with a target value of 50%

---

## Question 127

**Q:** Which of the following features of Application Load Balancers can be used for this use-case?

**A:** Path-based Routing

---

## Question 128

**Q:** What is the MOST secure and appropriate way to meet these DNS resolution requirements?

**A:** Create a Route 53 Resolver outbound endpoint. Define a forwarding rule that routes DNS queries for on-premises domains to the on-premises DNS server. Associate the rule with the VPC

---

## Question 129

**Q:** Which of the following options can be used to implement this system?

**A:** Use Amazon SQS FIFO (First-In-First-Out) queue in batch mode of 4 messages per operation to process the messages at the peak rate

---

## Question 130

**Q:** How would you implement this with minimal application refactoring?

**A:** Use an Amazon Aurora Global Database for the games table and use Amazon Aurora for the users and games_played tables

---

## Question 131

**Q:** As a Solutions Architect, which of the following will you suggest for the company?

**A:** Use an Application Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure Auto Scaling group to mask any failure of an instance

---

## Question 132

**Q:** What is the correct order of the storage charges incurred for the test file on these three storage types?

**A:** Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EFS < Cost of test file storage on Amazon EBS

---

## Question 133

**Q:** Which of the following is the fastest way to upload the daily compressed file into Amazon S3?

**A:** Upload the compressed file using multipart upload with Amazon S3 Transfer Acceleration (Amazon S3TA)

---

## Question 134

**Q:** Given these constraints, which of the following solutions is the BEST fit to develop this car-as-a-sensor service?

**A:** Ingest the sensor data in an Amazon Simple Queue Service (Amazon SQS) standard queue, which is polled by an AWS Lambda function in batches and the data is written into an auto-scaled Amazon DynamoDB table for downstream processing

---

## Question 135

**Q:** As an AWS Certified Solutions Architect – Associate, which best practices would you recommend (Select two)?

**A:** Implement an Amazon SQS FIFO queue to reliably buffer and deliver form submissions from the web application layer to the processing tier

---

## Question 136

**Q:** Which design choice best satisfies these requirements?

**A:** Implement an Amazon SQS FIFO queue to reliably buffer and deliver form submissions from the web application layer to the processing tier

---

## Question 137

**Q:** As a solutions architect, what is your recommendation to enable this collaboration with the LEAST amount of operational overhead?

**A:** The spreadsheet on the Amazon Elastic File System (Amazon EFS) can be accessed in other AWS regions by using an inter-region VPC peering connection

---

## Question 138

**Q:** As an AWS Certified Solutions Architect – Associate, which is the MOST cost-effective storage class that you would recommend to be used for this use-case?

**A:** Amazon S3 Standard-Infrequent Access (S3 Standard-IA)

---

## Question 139

**Q:** Which is the most cost-effective solution to build a solution for the workflow?

**A:** Use Amazon EC2 spot instances to run the workflow processes

---

## Question 140

**Q:** What would you recommend?

**A:** Use Amazon CloudFront with a custom origin pointing to the on-premises servers

---

## Question 141

**Q:** Which of the following is correct regarding the pricing for these two services?

**A:** Amazon ECS with EC2 launch type is charged based on EC2 instances and EBS volumes used. Amazon ECS with Fargate launch type is charged based on vCPU and memory resources that the containerized application requests

---

## Question 142

**Q:** As a Solutions Architect, which of the following options would you recommend to test the deployment on as many users as possible in the given time frame?

**A:** Use AWS Global Accelerator to distribute a portion of traffic to a particular deployment

---

## Question 143

**Q:** What could be the reason for this denial of permission for the bucket owner?

**A:** By default, an Amazon S3 object is owned by the AWS account that uploaded it. So the Amazon S3 bucket owner will not implicitly have access to the objects written by the Amazon Redshift cluster

---

## Question 144

**Q:** Which solution will best meet these requirements with high availability and minimal configuration complexity?

**A:** Deploy the application on multiple Amazon EC2 instances in an Auto Scaling group that spans two Availability Zones. Place an Application Load Balancer (ALB) in front of the group. Associate AWS WAF with the ALB

---

## Question 145

**Q:** Which solution will best meet these requirements with minimal refactoring and operational overhead?

**A:** Package the scripts into a container image. Use Amazon EventBridge Scheduler to define cron-based recurring schedules. Configure EventBridge Scheduler to invoke AWS Fargate tasks using Amazon ECS

---

## Question 146

**Q:** Which solution will provide the MOST cost-effective and scalable architecture to meet these new requirements?

**A:** Configure Amazon S3 to send event notifications to an Amazon SQS queue each time a photo is uploaded. Set up an AWS Lambda function to poll the queue and process images asynchronously

---

## Question 147

**Q:** Which of the following would you identify as correct regarding the data transfer charges for Amazon RDS read replicas?

**A:** There are data transfer charges for replicating data across AWS Regions

---

## Question 148

**Q:** Which of the following is the correct outcome during the maintenance window?

**A:** Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete

---

## Question 149

**Q:** Given that all end users of the web application would be located in the US, which of the following would be the MOST resource-efficient solution?

**A:** Deploy the web-tier Amazon EC2 instances in two Availability Zones (AZs), behind an Elastic Load Balancer. Deploy the Amazon RDS MySQL database in Multi-AZ configuration

---

## Question 150

**Q:** Which of the following options is correct?

**A:** Users belonging to the IAM user group can terminate an Amazon EC2 instance in the us-west-1 region when the user's source IP is 10.200.200.200

---

## Question 151

**Q:** You have multiple AWS accounts within a single AWS Region managed by AWS Organizations and you would like to ensure all Amazon EC2 instances in all these accounts can communicate privately. Which of the following solutions provides the capability at the CHEAPEST cost?

**A:** Create a virtual private cloud (VPC) in an account and share one or more of its subnets with the other accounts using Resource Access Manager

---

## Question 152

**Q:** As a solutions architect, which of the following solutions would you recommend so that it requires minimum development and systems administration effort to address this requirement?

**A:** Enable storage auto-scaling for Amazon RDS MySQL

---

## Question 153

**Q:** Which of the following options would you recommend?

**A:** Set up an Amazon Aurora Global Database cluster

---

## Question 154

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-optimal solution so that it can meet the workload demand in a steady state?

**A:** Purchase 80 reserved instances (RIs). Provision additional on-demand and spot instances per the workload demand (Use Auto Scaling Group with launch template to provision the mix of on-demand and spot instances)

---

## Question 155

**Q:** Which of the following would you recommend to securely share the database with the auditor?

**A:** Create an encrypted snapshot of the database, share the snapshot, and allow access to the AWS Key Management Service (AWS KMS) encryption key

---

## Question 156

**Q:** Which of the following actions meets the given requirements?

**A:** Set up a service control policy (SCP) that prohibits changes to AWS CloudTrail, and attach it to the developer accounts

---

## Question 157

**Q:** What does this IAM policy do?

**A:** It allows running Amazon EC2 instances only in the eu-west-1 region, and the API call can be made from anywhere in the world

---

## Question 158

**Q:** Which of the following Amazon S3 encryption options allows the company to leverage Amazon S3 for storing data with given constraints?

**A:** Server-Side Encryption with Customer-Provided Keys (SSE-C)

---

## Question 159

**Q:** As a solutions architect, which of the following solutions would you recommend for this use-case?

**A:** Use Amazon EC2 Instance Hibernate

---

## Question 160

**Q:** The company is looking at alternate database options and migrating database engines if required. What would you suggest?

**A:** Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and create the dev database by restoring from the automated backups of Amazon Aurora

---

## Question 161

**Q:** Which approach will best meet these requirements?

**A:** Configure individual S3 access points for each analytics service. Attach access point policies that restrict access to only the relevant prefix in the S3 bucket

---

## Question 162

**Q:** What do you recommend as a replacement for the DFSR?

**A:** Amazon FSx for Windows File Server

---

## Question 163

**Q:** As a Solutions Architect, which of the following solutions would you recommend to the development team so that it requires minimal development effort?

**A:** Use Amazon Cognito Authentication via Cognito User Pools for your Application Load Balancer

---

## Question 164

**Q:** Which of the following solutions would reduce both the administrative overhead and the costs while providing shared access to services required by workloads in each of the VPCs?

**A:** Build a shared services Amazon Virtual Private Cloud (Amazon VPC)

---

## Question 165

**Q:** As a Solutions Architect, can you identify the Amazon Virtual Private Cloud (Amazon VPC) options to be configured in order to get the private hosted zone to work?

**A:** Enable DNS hostnames and DNS resolution for private hosted zones

---

## Question 166

**Q:** Which solution will best meet these requirements?

**A:** Deploy a standard accelerator in AWS Global Accelerator and register the existing regional NLBs as endpoints. Use the accelerator to route user requests through AWS’s global edge network to the closest healthy Regional NLB

---

## Question 167

**Q:** What should the solutions architect do to meet these requirements?

**A:** Create an Amazon Simple Queue Service (Amazon SQS) queue to buffer the incoming location data. Configure the backend application to poll the queue and process messages

---

## Question 168

**Q:** Which of the following represents the MOST cost-optimal and high-performance solution?

**A:** Build the website as a static website hosted on Amazon S3. Create an Amazon CloudFront distribution with Amazon S3 as the origin. Use Amazon Route 53 to create an alias record that points to your Amazon CloudFront distribution

---

## Question 169

**Q:** Which of the following solutions would have the LEAST amount of downtime?

**A:** Set up a Amazon Route 53 failover record. Run application servers on Amazon EC2 instances behind an Application Load Balancer in an Auto Scaling group. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3

---

## Question 170

**Q:** As a solutions architect, which of the following would you recommend so that the application achieves high availability with MINIMUM cost?

**A:** Deploy the instances in three Availability Zones (AZs). Launch two instances in each Availability Zone (AZ)

---

## Question 171

**Q:** An analytics company wants to improve the performance of its big data processing workflows running on Amazon Elastic File System (Amazon EFS). Which of the following performance modes should be used for Amazon EFS to address this requirement?

**A:** Max I/O

---

## Question 172

**Q:** Which solution will best meet these goals with the least operational burden?

**A:** Migrate the SQL Server databases to a Multi-AZ Amazon RDS for SQL Server deployment. Enable encryption at rest by using an AWS Key Management Service (AWS KMS) managed key

---

## Question 173

**Q:** Upon a security review of your AWS account, an AWS consultant has found that a few Amazon RDS databases are unencrypted. As a Solutions Architect, what steps must be taken to encrypt the Amazon RDS databases?

**A:** Take a snapshot of the database, copy it as an encrypted snapshot, and restore a database from the encrypted snapshot. Terminate the previous database

---

## Question 174

**Q:** Which AWS architecture will best fulfill these requirements?

**A:** Migrate the application to Amazon EC2 instances in an Auto Scaling group behind an Application Load Balancer. Use Amazon Aurora Serverless v2 for MySQL to manage the database layer with auto-scaling and built-in high availability

---

## Question 175

**Q:** Which solution will best meet these requirements?

**A:** Send the extracted text to Amazon Comprehend for entity detection and sentiment analysis. Store the results in Amazon S3 for further access or visualization.

---

## Question 176

**Q:** As an AWS Certified Solutions Architect Associate, what would you recommend to separate the read requests from the write requests?

**A:** Set up a read replica and modify the application to use the appropriate endpoint

---

## Question 177

**Q:** Which of the following options represents the best solution for the given requirements?

**A:** Amazon Elastic File System (EFS) Standard–IA storage class

---

## Question 178

**Q:** What do you recommend?

**A:** Use an Amazon Simple Queue Service (Amazon SQS) FIFO (First-In-First-Out) queue, and make sure the telemetry data is sent with a Group ID attribute representing the value of the Desktop ID

---

## Question 179

**Q:** Which solution will best meet the requirements with the LEAST administrative overhead?

**A:** Provision an Amazon FSx for Windows File Server file system. Mount the file system using the SMB protocol on the media servers

---

## Question 180

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-optimal solution?

**A:** Purchase 70 reserved instances (RIs) and 30 spot instances

---

## Question 181

**Q:** Which of the following instances would be terminated per the default termination policy?

**A:** Instance B

---

## Question 182

**Q:** You would like to use AWS Snowball to move on-premises backups into a long term archival tier on AWS. Which solution provides the MOST cost savings?

**A:** Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier Deep Archive on the same day

---

## Question 183

**Q:** Which of the following is the MOST cost-effective way of isolating their Amazon Elastic Compute Cloud (Amazon EC2)instances to a single tenant?

**A:** Dedicated Instances

---

## Question 184

**Q:** Which is the MOST cost-optimal solution for this workload?

**A:** Run the workload on a Spot Fleet

---

## Question 185

**Q:** You have a team of developers in your company, and you would like to ensure they can quickly experiment with AWS Managed Policies by attaching them to their accounts, but you would like to prevent them from doing an escalation of privileges, by granting themselves the AdministratorAccess managed policy. How should you proceed?

**A:** For each developer, define an IAM permission boundary that will restrict the managed policies they can attach to themselves

---

## Question 186

**Q:** Which is the MOST operationally efficient solution?

**A:** Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with automatic key rotation

---

## Question 187

**Q:** Which solution will fulfill these needs with the least development effort?

**A:** Use Amazon Security Lake to create a centralized data lake that automatically collects security-related logs and events from AWS services and third-party sources. Store the data in an Amazon S3 bucket managed by Security Lake

---

## Question 188

**Q:** As a Solutions Architect, which of the following will you recommend to meet this requirement?

**A:** Create an IAM role for the AWS Lambda function that grants access to the Amazon S3 bucket. Set the IAM role as the AWS Lambda function's execution role. Make sure that the bucket policy also grants access to the AWS Lambda function's execution role

---

## Question 189

**Q:** As a solutions architect, which of the following actions would you recommend to stop the attacks?

**A:** Create an IP match condition in the AWS WAF to block the malicious IP address

---

## Question 190

**Q:** As a solutions architect, which of the following solutions would you recommend as the MOST secure option?

**A:** Attach the appropriate IAM role to the Amazon EC2 instance profile so that the instance can access Amazon S3 and Amazon DynamoDB

---

## Question 191

**Q:** What does this IAM policy do?

**A:** It allows starting an Amazon EC2 instance only when the IP where the call originates is within the 34.50.31.0/24 CIDR block

---

## Question 192

**Q:** Which of the following will you recommend as the MOST cost-effective and high-performance solution?

**A:** Use Amazon Aurora Global Database to enable fast local reads with low latency in each region

---

## Question 193

**Q:** What should the architect do to meet these requirements?

**A:** Create a resource policy for the API Gateway API that explicitly denies access to all IP addresses except those listed in an allow list

---

## Question 194

**Q:** Which solution should the team implement to enforce rate limiting and usage quotas at the API layer?

**A:** Use Amazon API Gateway and configure usage plans with API keys to apply rate limits and quotas per client

---


