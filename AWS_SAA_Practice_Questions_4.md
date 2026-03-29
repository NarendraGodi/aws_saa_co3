# AWS SAA-C03 Practice Questions - Part 4

Total Questions: 194

---

## Question 1

**Q:** As a solutions architect, which of the following options would you recommend for the given use-case?

**A:** Use SQS long polling to retrieve messages from your Amazon SQS queues

---

## Question 2

**Q:** Which solution will you recommend to address this use-case?

**A:** Use Amazon Kinesis Data Streams to process the data streams as well as decouple the producers and consumers for the real-time data processor

---

## Question 3

**Q:** Under the given infrastructure setup, which of the following entities is doing the Network Address Translation for the Amazon EC2 instance E1?

**A:** Internet Gateway (I1)

---

## Question 4

**Q:** As a solutions architect, which of the following would you recommend as an optimized solution for high-frequency reading and writing?

**A:** Use Amazon EFS with Provisioned Throughput mode

---

## Question 5

**Q:** As a solutions architect, which of the following solutions would you recommend for this use-case?

**A:** Use AWS Volume Gateway - Cached Volume - to store the most frequently accessed logs locally for low-latency access while storing the full volume with all logs in its Amazon S3 service bucket

---

## Question 6

**Q:** As a solutions architect, which of the following solutions would you recommend to address this use-case?

**A:** Use VPC endpoint to access Amazon SQS

---

## Question 7

**Q:** As a solutions architect, which of the following solutions would you recommend to the team?

**A:** Use AWS Config to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes

---

## Question 8

**Q:** Which of the following represents the correct configuration for the IPSec VPN Connection?

**A:** Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN

---

## Question 9

**Q:** As a solutions architect, which of the following solutions would you recommend to help address the given requirements?

**A:** Use Amazon GuardDuty to monitor any malicious activity on data stored in Amazon S3. Use Amazon Macie to identify any sensitive data stored on Amazon S3

---

## Question 10

**Q:** Which solution should you implement to meet these requirements?

**A:** Deploy an internal AWS Transfer Family SFTP server across two Availability Zones backed by Amazon S3. Configure a Transfer Family managed workflow to invoke an AWS Lambda function immediately after file upload completes

---

## Question 11

**Q:** Considering the company uses only IPv4 addressing and is looking for a fully managed service, which of the following would you suggest as an optimal solution?

**A:** Configure a Network Address Translation gateway (NAT gateway) in the public subnet of the VPC

---

## Question 12

**Q:** What solution would best meet these requirements?

**A:** Set up an Amazon FSx for ONTAP instance. Configure an FSx for ONTAP file system on the root volume and migrate the data to the FSx for ONTAP volume

---

## Question 13

**Q:** As an AWS Certified Solutions Architect Associate, which of the following would you recommend?

**A:** Set up a VPC gateway endpoint for Amazon S3. Attach an endpoint policy to the endpoint. Update the route table to direct the S3-bound traffic to the VPC endpoint

---

## Question 14

**Q:** Which of the following will you recommend?

**A:** Set up database migration from Amazon RDS MySQL to Amazon Aurora MySQL. Swap out the MySQL read replicas with Aurora Replicas. Configure Aurora Auto Scaling

---

## Question 15

**Q:** Which Amazon Route 53 record should you create?

**A:** Create a CNAME record

---

## Question 16

**Q:** As a solutions architect, which of the following solutions would you recommend as the BEST fit to automate and accelerate online data transfers to these AWS storage services?

**A:** Use AWS DataSync to automate and accelerate online data transfers to the given AWS storage services

---

## Question 17

**Q:** Which of the following would you recommend as a scalable alternative to the current solution?

**A:** Use Amazon Kinesis Data Streams to ingest the data, process it using AWS Lambda or run analytics using Amazon Kinesis Data Analytics

---

## Question 18

**Q:** Which of the following addresses the given use case?

**A:** Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold

---

## Question 19

**Q:** As a solutions architect, which of the following is the MOST cost-effective solution that you would recommend to the web development team?

**A:** Create an alias record for covid19survey.com that routes traffic to www.covid19survey.com

---

## Question 20

**Q:** What do you recommend?

**A:** Use Amazon DynamoDB point in time recovery to restore the table to the state just before corrupted data was written

---

## Question 21

**Q:** As a solutions architect, which of the following solutions would you recommend such that it offers the BEST performance for this use case?

**A:** Use AWS Global Accelerator to provide a low latency way to distribute live sports results

---

## Question 22

**Q:** Which of the following is correct regarding the instances launched via Launch Template LT1 and Launch Template LT2?

**A:** The instances launched by both Launch Template LT1 and Launch Template LT2 will have dedicated instance tenancy

---

## Question 23

**Q:** Which of these options would you identify as the right way of connecting these microservices?

**A:** Configure Amazon Simple Queue Service (Amazon SQS) queue to decouple microservices running faster processes from the microservices running slower ones

---

## Question 24

**Q:** As a solutions architect, which of the following Amazon Elastic Block Store (Amazon EBS) volume types would you recommend for this use-case?

**A:** Provisioned IOPS SSD (io1)

---

## Question 25

**Q:** As a solutions architect, which of the following would you suggest resolving this issue?

**A:** Use Availability Zone (AZ) ID to uniquely identify the Availability Zones across the two AWS Accounts

---

## Question 26

**Q:** As a Solutions Architect, can you suggest an alternate method to reduce costs while keeping the latency low?

**A:** Configure Amazon CloudFront to distribute the data hosted on Amazon S3 cost-effectively

---

## Question 27

**Q:** Which solution should the team implement to meet these requirements?

**A:** Use Amazon API Gateway HTTP API with a native JWT authorizer configured to validate tokens from the OIDC provider

---

## Question 28

**Q:** Which AWS solution best meets these requirements?

**A:** Use Amazon ECS with Fargate launch type. Provision an Amazon Elastic File System (Amazon EFS) file system. Mount the EFS volume inside the container at runtime to provide persistent storage access

---

## Question 29

**Q:** Which of the following solutions meets these requirements?

**A:** Set up an Amazon RDS MySQL DB instance with Multi-AZ functionality enabled to synchronously replicate the data

---

## Question 30

**Q:** As a solutions architect, which of the following solutions would you recommend to address this use-case?

**A:** Use a target tracking scaling policy based on a custom Amazon SQS queue metric

---

## Question 31

**Q:** Can you recommend an improved and cost-effective way of generating the business reports while keeping the production application unaffected?

**A:** Create a read replica and connect the report generation tool/application to it

---

## Question 32

**Q:** Which of the following options represents the correct solution to set up internet access for the private subnets?

**A:** Set up three NAT gateways, one in each public subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the NAT gateway in its AZ

---

## Question 33

**Q:** Which of the following is a cost-optimal solution that does not need provisioning of infrastructure?

**A:** Use Amazon CloudFront with Amazon S3 as the storage solution for the static assets

---

## Question 34

**Q:** Which of the following solutions should a solutions architect configure for the necessary permissions?

**A:** Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Configure an instance profile to assign this IAM role to the Amazon EC2 instance

---

## Question 35

**Q:** Which solution will best meet these requirements?

**A:** Deploy Amazon FSx for Windows File Server and mount it using the SMB protocol from both Windows and Linux EC2 instances

---

## Question 36

**Q:** In case of a failure, which of these options would you suggest as a cost-effective and automatic recovery procedure for the instance?

**A:** Configure an Amazon CloudWatch alarm that triggers the recovery of the Amazon EC2 instance, in case the instance fails. The instance, however, should only be configured with an Amazon EBS volume

---

## Question 37

**Q:** As a solutions architect, which of the following AWS services would you recommend for this use-case?

**A:** AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)

---

## Question 38

**Q:** Which solution best addresses these needs?

**A:** Subscribe to AWS Shield Advanced to gain proactive DDoS protection. Engage the AWS DDoS Response Team (DRT) to analyze traffic patterns and apply mitigations. Use the built-in logging and reporting to maintain an audit trail of detected events

---

## Question 39

**Q:** As a solutions architect, which of the following options would you choose to facilitate this use-case?

**A:** Use VPC sharing to share one or more subnets with other AWS accounts belonging to the same parent organization from AWS Organizations

---

## Question 40

**Q:** How will you implement this requirement without adding the overhead of splitting the data into logical groups?

**A:** Configure a single Amazon S3 bucket to hold all data. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data

---

## Question 41

**Q:** Which approach will allow the company to meet these goals with the least administrative overhead?

**A:** Enable Default Host Management Configuration in AWS Systems Manager Quick Setup

---

## Question 42

**Q:** Which of the following solutions addresses these requirements with the minimal integration effort?

**A:** Use Amazon FSx for Windows File Server as a shared storage solution

---

## Question 43

**Q:** As a Solutions Architect, can you suggest a cost-effective serverless solution for its flagship application that has both static and dynamic content?

**A:** Host the static content on Amazon S3 and use AWS Lambda with Amazon DynamoDB for the serverless web application that handles dynamic content. Amazon CloudFront will sit in front of AWS Lambda for distribution across diverse regions

---

## Question 44

**Q:** Which AWS solution best meets these requirements?

**A:** Use AWS Lambda to run the Python-based microservice. Integrate it with Amazon API Gateway for HTTP access and enable provisioned concurrency for performance during peak loads

---

## Question 45

**Q:** As a solutions architect, can you help the engineering team understand the correct routing mechanism for these target instances?

**A:** Traffic is routed to instances using the primary private IP address specified in the primary network interface for the instance

---

## Question 46

**Q:** As a solutions architect, which of the following would you identify as an INVALID option for setting up such a configuration?

**A:** You can use an Internet Gateway ID as the custom source for the inbound rule

---

## Question 47

**Q:** As a Solutions Architect, which of the following will you suggest as an optimal solution to meet the given requirements?

**A:** Use Amazon S3 for hosting the web application and use Amazon S3 Transfer Acceleration (Amazon S3TA) to reduce the latency that geographically dispersed users might face

---

## Question 48

**Q:** As a solutions architect, how will you fix this issue?

**A:** Security Groups are stateful, so allowing inbound traffic to the necessary ports enables the connection. Network ACLs are stateless, so you must allow both inbound and outbound traffic

---

## Question 49

**Q:** As a solutions architect, which of the following options would you recommend for this use-case?

**A:** Use AWS CloudFormation StackSets to deploy the same template across AWS accounts and regions

---

## Question 50

**Q:** The company is looking at an easy and effective way to bring down the number of IP addresses allowed by the firewall and easily manage the entire network infrastructure. Which of these options represents an appropriate solution for this requirement?

**A:** Launch AWS Global Accelerator and create endpoints for all the Regions. Register the Application Load Balancers of each Region to the corresponding endpoints

---

## Question 51

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-efficient and reliable solution?

**A:** Schedule a weekly Amazon EventBridge event cron expression to invoke an AWS Lambda function that runs the database rollover job

---

## Question 52

**Q:** Which of the following is the most appropriate solution to meet these requirements?

**A:** Create EFS mount targets in each AZ and mount the EFS file system to EC2 instances in the same AZ as the mount target

---

## Question 53

**Q:** Which of the following options represents a valid cost-optimization solution?

**A:** Use AWS Cost Optimization Hub to get a report of Amazon EC2 instances that are either idle or have low utilization and use AWS Compute Optimizer to look at instance type recommendations

---

## Question 54

**Q:** Which of the following steps would you recommend to facilitate end-to-end security for the data-in-transit while accessing the database?

**A:** Configure Amazon RDS to use SSL for data in transit

---

## Question 55

**Q:** Which of the below statements is true about traffic distribution to the target instances from Amazon Route 53?

**A:** Each of the four targets in AZ-A receives 12.5% of the traffic

---

## Question 56

**Q:** Which scaling strategy should a solutions architect recommend to meet these requirements?

**A:** Use predictive scaling for the Auto Scaling group to analyze daily and weekly patterns, and configure dynamic scaling with target tracking policies to respond to real-time traffic changes

---

## Question 57

**Q:** As a Solutions Architect, which database do you recommend for their requirements?

**A:** Amazon DynamoDB

---

## Question 58

**Q:** Which technology allows you to get a managed message broker that supports the MQTT protocol?

**A:** Amazon MQ

---

## Question 59

**Q:** Which of the following represents the MOST scalable solution with minimal configuration changes?

**A:** Set up AWS Global Accelerator. Register the Application Load Balancers in different Regions to the AWS Global Accelerator. Configure the on-premises firewall's rule to allow static IP addresses associated with the AWS Global Accelerator

---

## Question 60

**Q:** What do you recommend?

**A:** Place an Amazon ElastiCache for Redis cluster in front of the PostgreSQL database. Modify the application to cache recent location reads and updates in Redis, using a TTL-based eviction strategy

---

## Question 61

**Q:** What is an optimal solution that meets these requirements while keeping the costs to a minimum?

**A:** Use Tape Gateway, which can be used to move on-premises tape data onto AWS Cloud. Then, Amazon S3 archiving storage classes can be used to store data cost-effectively for years

---

## Question 62

**Q:** How can you easily reduce the costs while improving performance, with minimal changes?

**A:** Enable Amazon API Gateway Caching

---

## Question 63

**Q:** As a solutions architect, which of the following AWS database services would you suggest as the BEST fit to handle such use cases?

**A:** Amazon Neptune

---

## Question 64

**Q:** Which AWS solution best meets these requirements?

**A:** Deploy AWS Storage Gateway using cached volumes. Store frequently accessed data locally, while writing all primary data asynchronously to Amazon S3

---

## Question 65

**Q:** Which feature of Amazon Route 53 can help achieve this functionality?

**A:** Geoproximity routing

---

## Question 66

**Q:** Which solution will best meet these requirements?

**A:** Connect both Direct Connect links to a shared Direct Connect gateway. Attach each Region's virtual private gateway (VGW) to the Direct Connect gateway, enabling transitive routing between the VPCs and the on-premises networks across Regions

---

## Question 67

**Q:** Which of the following solutions will you recommend to address the given use-case?

**A:** Opt for Multi-AZ configuration with automatic failover functionality to help mitigate failure

---

## Question 68

**Q:** As a solutions architect, you would like to adhere to the security pillar of the well-architected framework. How do you configure the security group of the Amazon EC2 instances to only allow traffic coming from the Application Load Balancer?

**A:** Add a rule to authorize the security group of the Application Load Balancer

---

## Question 69

**Q:** As a solutions architect, which of the following would you recommend as a solution that requires MINIMAL configuration effort?

**A:** Use Secure Sockets Layer certificate (SSL certificate) with SNI

---

## Question 70

**Q:** Which configuration will best meet these requirements?

**A:** Configure the Aurora cluster to use Aurora I/O-Optimized storage. This configuration delivers high throughput and low-latency I/O performance with predictable pricing and no I/O-based charges

---

## Question 71

**Q:** Which of the following is the MOST cost-effective solution for this use-case?

**A:** Use a VPC peering connection

---

## Question 72

**Q:** As a Solutions Architect, which of the following would you suggest to asynchronously decouple the architecture?

**A:** Use Amazon EventBridge to decouple the system architecture

---

## Question 73

**Q:** As a solutions architect, which combination of AWS features should you recommend to enforce these policies effectively?

**A:** Use Amazon S3 Object Lock in Compliance mode for Policy A, and S3 Glacier Vault Lock for Policy B

---

## Question 74

**Q:** As a solutions architect, which of the following would you recommend to meet the given requirements?

**A:** Migrate the data to Amazon RDS for SQL Server database in a Multi-AZ deployment

---

## Question 75

**Q:** The users are still not redirected to the new Load Balancer. What has gone wrong in the configuration?

**A:** The Time To Live (TTL) is still in effect

---

## Question 76

**Q:** Which solution will meet these requirements with the least operational overhead?

**A:** Use AWS Key Management Service (KMS) to create a customer managed key with automatic rotation enabled. Configure the S3 bucket’s default encryption to use the customer managed key. Migrate the data to the S3 bucket

---

## Question 77

**Q:** Which solution should the architect implement to resolve this issue with the least operational overhead?

**A:** Deploy the Kubernetes Cluster Autoscaler to the EKS cluster. Configure it to integrate with the existing EC2 Auto Scaling group to automatically launch or terminate nodes based on pending pod demands

---

## Question 78

**Q:** The architecture team is planning to increase the read throughput of the database, without changing the application's core logic. As a Solutions Architect, what do you recommend?

**A:** Use Amazon RDS Read Replicas

---

## Question 79

**Q:** What can you do to improve the performance of Amazon DynamoDB and eliminate the hot partition problem without a lot of application refactoring?

**A:** Use Amazon DynamoDB DAX

---

## Question 80

**Q:** As a Solutions Architect, how will you handle the upload of these files to Amazon S3?

**A:** Use multi-part upload feature of Amazon S3

---

## Question 81

**Q:** Which solution will best meet these requirements in a cost-effective manner?

**A:** Integrate Amazon ElastiCache for Redis between the application and Aurora. Cache frequently accessed query results in Redis to reduce the number of identical read requests hitting the database

---

## Question 82

**Q:** Which of the following options will maximize the VPN throughput?

**A:** Create an AWS Transit Gateway with equal cost multipath routing and add additional VPN tunnels

---

## Question 83

**Q:** Which is the only resource-based policy that the IAM service supports?

**A:** Trust policy

---

## Question 84

**Q:** As a Solutions Architect, which of the following would you identify as the correct description for the given policy?

**A:** It authorizes an entire Classless Inter-Domain Routing (CIDR) except one IP address to access the Amazon S3 bucket

---

## Question 85

**Q:** Which of the following will you recommend as the best-fit solution?

**A:** Set up Amazon DynamoDB table in the on-demand capacity mode

---

## Question 86

**Q:** Which approach best addresses these requirements with the least operational overhead?

**A:** Enable deletion protection on DynamoDB tables

---

## Question 87

**Q:** As a Solutions architect, which of the following options would you recommend as the disaster recovery strategy?

**A:** Create an Amazon Machine Image (AMI) after installing the software and copy the AMI across all Regions. Use this Region-specific AMI to run the recovery process in the respective Regions

---

## Question 88

**Q:** Which approach should the team take to best meet these requirements?

**A:** Enable EFS burst throughput mode on the file system using the General Purpose performance mode and EFS Standard storage class

---

## Question 89

**Q:** Which of the following solutions can be used to improve the performance of the workload?

**A:** Select a cluster placement group while launching Amazon EC2 instances

---

## Question 90

**Q:** The rule *.example.com matches which of the following?

**A:** test.example.com

---

## Question 91

**Q:** A company wants to grant access to an Amazon S3 bucket to users in its own AWS account as well as to users in another AWS account. Which of the following options can be used to meet this requirement?

**A:** Use a bucket policy to grant permission to users in its account as well as to users in another account

---

## Question 92

**Q:** As a Solutions Architect, which of the following would you suggest as the solution that requires the LEAST operational overhead?

**A:** Use AWS Transit Gateway to connect the Amazon VPCs to the on-premises networks

---

## Question 93

**Q:** As a Solutions Architect, what do you propose to reduce the costs?

**A:** Convert the Amazon EC2 instance EBS volume to gp2

---

## Question 94

**Q:** As a Solutions Architect, which of the following options would you recommend to make sure your infrastructure scales for that day?

**A:** Use an Auto Scaling Group

---

## Question 95

**Q:** What will happen under the default Auto Scaling Group configuration?

**A:** The instance with the oldest launch template or launch configuration will be terminated in AZ-B

---

## Question 96

**Q:** As a Solutions Architect, which deployment do you recommend?

**A:** Use a Cluster placement group

---

## Question 97

**Q:** As a Solutions Architect, you would like to ensure that a scaled-down version of a fully functional environment is always running in the AWS cloud, and in case of a disaster, the recovery time is kept to a minimum. Which disaster recovery strategy is that?

**A:** Warm Standby

---

## Question 98

**Q:** Which architectural choice do you recommend to maintain high availability, support scaling-up to 10 instances and comply with the bank's requirements?

**A:** Use a Network Load Balancer with an Auto Scaling Group

---

## Question 99

**Q:** How can you ensure that Amazon RDS specific best practices are incorporated into a reusable infrastructure template to be used by all your AWS users?

**A:** Use AWS CloudFormation to manage Amazon RDS databases

---

## Question 100

**Q:** As a Solutions Architect, which of the following would you suggest as the fastest possible way of building a solution for this requirement?

**A:** Leverage AWS Database Migration Service (AWS DMS) as a bridge between Amazon S3 and Amazon Kinesis Data Streams

---

## Question 101

**Q:** As a solutions architect, which of the following solutions would you suggest to the company?

**A:** Use AWS Site-to-Site VPN to establish encrypted network connectivity between the on-premises data center and AWS Cloud

---

## Question 102

**Q:** Which configuration will meet the company's requirements, while keeping the changes to a bare minimum?

**A:** Set up Amazon Route 53 active-passive type of failover routing policy. If Amazon Route 53 health check determines the Application Load Balancer endpoint as unhealthy, the traffic will be diverted to a static error page, hosted on Amazon S3 bucket

---

## Question 103

**Q:** As a solutions architect, which of the following configurations would you suggest to the engineering team?

**A:** Amazon EC2 with Amazon EBS volume of Provisioned IOPS SSD (io1) type

---

## Question 104

**Q:** Which of the following options represent the root cause for this issue?

**A:** The security group configuration for the database instance does not have the correct rules to allow inbound connections from the application servers

---

## Question 105

**Q:** Which of the following is the MOST cost-optimal and resource-efficient way to implement an automated solution until a permanent fix is delivered by the development team?

**A:** Setup an Amazon CloudWatch alarm to monitor the health status of the instance. In case of an Instance Health Check failure, an EC2 Reboot CloudWatch Alarm Action can be used to reboot the instance

---

## Question 106

**Q:** Which solution should a solutions architect recommend to meet these requirements?

**A:** Take snapshots of the production EBS volumes. Enable EBS fast snapshot restore on the snapshots. Create new EBS volumes from the snapshots and attach them to EC2 instances in the test environment

---

## Question 107

**Q:** Which solution will fulfill these requirements?

**A:** Create a gateway VPC endpoint for Amazon S3 in the VPC. Ensure that the EC2 instance’s subnet route table is updated to route S3 traffic through the endpoint. Confirm that appropriate IAM policies are in place to permit access via the VPC endpoint

---

## Question 108

**Q:** As a Solutions Architect, which of the following solutions would you recommend?

**A:** Use Amazon Transcribe to convert audio files to text and Amazon Athena to perform SQL based analysis to understand the underlying customer sentiments

---

## Question 109

**Q:** What do you recommend?

**A:** Use EC2 Instance Connect to inject a temporary public key and establish SSH access using the instance’s public IP address

---

## Question 110

**Q:** Which configuration of S3 Object Lock will ensure that the retention policy is strictly enforced, and no user (including root or administrators) can override or delete protected objects during the lock period?

**A:** Use S3 Object Lock in Compliance Mode, which enforces retention policies strictly and prevents all users from modifying or deleting data during the retention period

---

## Question 111

**Q:** Which solution will best meet these requirements?

**A:** Use AWS PrivateLink to create a private endpoint within the application’s VPC that connects securely to the SaaS provider’s VPC

---

## Question 112

**Q:** What could explain this anomaly?

**A:** The Auto Scaling group is using Amazon EC2 based health check and the Application Load Balancer is using ALB based health check

---

## Question 113

**Q:** Which of the following options offers the LOWEST data transfer egress cost for the company?

**A:** Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over a Direct Connect connection at a location in the same region

---

## Question 114

**Q:** Which solution should you recommend?

**A:** Set up AWS Global Accelerator with listeners configured for HTTPS. Create endpoint groups for Europe and Asia and add the existing us-west-2 EC2 endpoint to these groups

---

## Question 115

**Q:** Which solution should the team use to meet this requirement?

**A:** Use AWS Identity and Access Management (IAM) Access Analyzer to evaluate resource-based and identity-based policies and identify resources shared outside the account or organization

---

## Question 116

**Q:** As a solutions architect, which of the following would you select as the MOST performant solution for the given use-case?

**A:** Use AWS DataSync to migrate existing data to Amazon S3 and then use File Gateway to retain access to the migrated data for ongoing updates from the on-premises applications

---

## Question 117

**Q:** Which option best meets the application’s availability, durability, and RPO objectives?

**A:** Use Amazon Elastic File System (Amazon EFS) with the Standard storage class and configure AWS Backup to create cross-Region backups on a scheduled basis

---

## Question 118

**Q:** As a solutions architect, which of the following would you recommend for improving the performance for the given use-case?

**A:** Use Enhanced Fanout feature of Amazon Kinesis Data Streams

---

## Question 119

**Q:** As a Solutions Architect, which set of services will you recommend to meet these requirements?

**A:** Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage

---

## Question 120

**Q:** As a solutions architect, which of the following solutions will you suggest?

**A:** Use Amazon ElastiCache for Redis

---

## Question 121

**Q:** How will you resolve the issue and make sure it doesn't happen again?

**A:** Install an Amazon CloudWatch Logs agents on the Amazon EC2 instances to send logs to Amazon CloudWatch

---

## Question 122

**Q:** Which of the following options will help with the exception while keeping costs at a minimum?

**A:** Use batch messages

---

## Question 123

**Q:** What AWS services would you recommend for this use-case such that the solution is cost-effective and easy to maintain?

**A:** Use Amazon Athena to run SQL based analytics against Amazon S3 data

---

## Question 124

**Q:** Which approach should the company choose to meet these requirements in the most cost-effective way?

**A:** Set up an Amazon S3 File Gateway to provide storage for the on-premises application

---

## Question 125

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Create an Amazon S3 bucket configured with server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Athena to run SQL queries on the data

---

## Question 126

**Q:** Which solution will meet these requirements?

**A:** Configure an AWS DMS Serverless replication task to synchronize historical and ongoing changes between the on-premises Oracle database and Amazon RDS for Oracle

---

## Question 127

**Q:** Which solution will fulfill these needs in the most cost-efficient manner?

**A:** Use DynamoDB global tables for automatic multi-Region replication. Enable provisioned capacity mode with auto scaling to optimize cost and ensure consistent availability

---

## Question 128

**Q:** As a solutions architect, what is your recommendation to migrate this data in the MOST cost-optimal way?

**A:** Transfer the on-premises data into multiple AWS Snowball Edge Storage Optimized devices. Copy the AWS Snowball Edge data into Amazon S3 and create a lifecycle policy to transition the data into Amazon S3 Glacier

---

## Question 129

**Q:** Which solution should the team implement?

**A:** Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics to track performance

---

## Question 130

**Q:** Which solution meets the company's encryption and cost optimization goals?

**A:** Enable S3 Bucket Keys for server-side encryption with AWS KMS (SSE-KMS) so that new objects use a bucket-level key rather than requesting individual KMS data keys for every object

---

## Question 131

**Q:** Which solution will best meet these requirements with the least development effort?

**A:** Set up a 7-day EBS snapshot retention rule in Recycle Bin and apply the rule for all snapshots

---

## Question 132

**Q:** As a solutions architect, which of the following solutions would you recommend?

**A:** Use Amazon S3 Glacier vault to store the sensitive archived data and then use a vault lock policy to enforce compliance controls

---

## Question 133

**Q:** As a solutions architect, which of the following solutions would you recommend as the MOST effective in countering these malicious attacks?

**A:** Use AWS Web Application Firewall (AWS WAF) with Amazon CloudFront distribution

---

## Question 134

**Q:** What should a solutions architect recommend to reduce internet latency and add automatic failover across AWS Regions?

**A:** Set up AWS Global Accelerator and add endpoints to cater to users in different geographic locations

---

## Question 135

**Q:** Which EC2 purchasing strategy best meets these requirements in the most cost-effective manner?

**A:** Use Reserved Instances for the baseline level of traffic and configure EC2 Auto Scaling with Spot Instances to handle spikes in message volume

---

## Question 136

**Q:** Can you identify the correct solution leveraging the capabilities of AWS WAF?

**A:** Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures

---

## Question 137

**Q:** As a solutions architect, which of the following AWS storage options would you recommend as the MOST performant as well as cost-optimal?

**A:** Use Amazon EC2 instances with Instance Store as the storage option

---

## Question 138

**Q:** Which solution should a solutions architect recommend to meet these requirements?

**A:** Migrate the order data to Amazon DynamoDB and create a global table. Deploy the application in each Region and connect to the local DynamoDB replica for low-latency access

---

## Question 139

**Q:** As a Solutions Architect, can you recommend a solution to reduce storage costs on Amazon S3 while keeping the IT team's involvement to a minimum?

**A:** Use Amazon S3 Intelligent-Tiering storage class to optimize the Amazon S3 storage costs

---

## Question 140

**Q:** As a solutions architect, which of the following would you recommend as the MOST resource-efficient and scalable solution?

**A:** Use AWS transit gateway to interconnect the VPCs

---

## Question 141

**Q:** As a solutions architect, which of the following solutions would you recommend?

**A:** Use Amazon Elasticache for distributed in-memory cache based session management

---

## Question 142

**Q:** As a Solutions Architect, which of the following configurations would you select as the best fit for these requirements?

**A:** The Auto Scaling group should be configured with the minimum capacity set to 4, with 2 instances each in two different Availability Zones. The maximum capacity of the Auto Scaling group should be set to 6

---

## Question 143

**Q:** As a solutions architect, which of the following solutions would you recommend for handling such message failures?

**A:** Use a dead-letter queue to handle message processing failures

---

## Question 144

**Q:** Which solution is the MOST cost-effective for the given use case?

**A:** Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Delete the files 5 years after object creation

---

## Question 145

**Q:** Which solution offers the most cost-effective architecture?

**A:** Create an Amazon S3 bucket with Intelligent-Tiering enabled. Update the application to store and retrieve project files using the Amazon S3 API

---

## Question 146

**Q:** Which solution best meets these requirements?

**A:** Set up AWS Site-to-Site VPN to connect the on-premises network to the AWS VPC. Use route tables to manage traffic flow and configure security groups and network ACLs to allow only authorized communication between systems

---

## Question 147

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Configure the S3 bucket to send an event notification to an AWS Lambda function each time a new image is uploaded. Use the Lambda function to process the image, create a thumbnail, and store the thumbnail in the second S3 bucket

---

## Question 148

**Q:** As a Solutions Architect, which of the following will you identify as the outcome of the scenario?

**A:** The CNAME record will be updated to point to the standby database

---

## Question 149

**Q:** Which solution best meets these requirements while ensuring the least operational overhead?

**A:** Use AWS Batch to process image jobs. Orchestrate the workflow using AWS Step Functions and store output files in Amazon S3

---

## Question 150

**Q:** As a solutions architect, how will you fix this issue?

**A:** Security Groups are stateful, so allowing inbound traffic to the necessary ports enables the connection. Network access control list (network ACL) are stateless, so you must allow both inbound and outbound traffic

---

## Question 151

**Q:** Which of the following is the MOST cost-optimal solution to fix this issue?

**A:** Create a Read Replica in the same Region as the Master database and point the analytics workload there

---

## Question 152

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-effective solution?

**A:** Use Amazon EC2 dedicated hosts

---

## Question 153

**Q:** How would you go about providing private access to these AWS resources which are not part of this custom VPC?

**A:** Create a separate gateway endpoint for Amazon S3 and Amazon DynamoDB each. Add two new target entries for these two gateway endpoints in the route table of the custom VPC

---

## Question 154

**Q:** Which solution best meets these goals while minimizing operational overhead?

**A:** Use AWS Control Tower to create and govern accounts. Deploy a centralized VPC in a shared networking account and share its subnets across workload accounts using AWS Resource Access Manager (AWS RAM)

---

## Question 155

**Q:** A startup uses a fleet of Amazon EC2 servers to manage its CRM application. These Amazon EC2 servers are behind Elastic Load Balancing (ELB). Which of the following configurations are NOT allowed for Elastic Load Balancing?

**A:** Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region

---

## Question 156

**Q:** As a solutions architect, which of the following services would you recommend for the given use case?

**A:** Amazon ElastiCache for Memcached

---

## Question 157

**Q:** Which of the following Amazon SQS queue types is the best fit to meet this requirement?

**A:** Amazon Simple Queue Service (Amazon SQS) temporary queues

---

## Question 158

**Q:** As a solutions architect, which of the following solutions would you suggest to the company?

**A:** Use delay queues to postpone the delivery of new messages to the queue for a few seconds

---

## Question 159

**Q:** How can you provide these users access in the least possible time, with minimal changes?

**A:** Create a group, attach the policy to the group and place the users in the group

---

## Question 160

**Q:** Which of the following represents a correct option regarding the capabilities of Amazon S3 Analytics storage class analysis?

**A:** Storage class analysis only provides recommendations for Standard to Standard IA classes

---

## Question 161

**Q:** As a solutions architect, which of the following solutions would you recommend?

**A:** Create two Amazon SQS standard queues: one for pro and one for lite. Set up Amazon EC2 instances to prioritize polling for the pro queue over the lite queue

---

## Question 162

**Q:** What do you recommend?

**A:** Create an origin access identity (OAI) and update the Amazon S3 Bucket Policy

---

## Question 163

**Q:** Which solution will help improve the application’s responsiveness and scalability during peak load periods?

**A:** Use an EC2 Auto Scaling group with a target tracking policy to automatically scale the processing tier. Configure the policy to monitor the ApproximateNumberOfMessages in the SQS queue

---

## Question 164

**Q:** As a solutions architect, what is your recommendation to build the MOST cost-effective solution?

**A:** Store the images using the Amazon S3 Intelligent-Tiering storage class

---

## Question 165

**Q:** As an AWS Certified Solutions Architect - Associate, which of the following would you suggest as the MOST cost-optimal solution to improve the performance?

**A:** Create a read-replica with the same compute capacity and the same storage capacity as the primary. Point the reporting queries to run against the read replica

---

## Question 166

**Q:** What do you recommend?

**A:** AWS Transit Gateway

---

## Question 167

**Q:** As a solutions architect, which of the following AWS services would you recommend as the MOST cost-optimal solution?

**A:** Amazon EFS Infrequent Access

---

## Question 168

**Q:** Which solution will most effectively address the performance issues with the least operational overhead?

**A:** Deploy an Amazon CloudFront distribution with the S3 bucket as the origin to improve download speeds. Enable S3 Transfer Acceleration to reduce upload latency for global users

---

## Question 169

**Q:** Leadership has asked for a DR solution that ensures fast cross-regional failover with minimal operational overhead and configuration effort. What do you recommend?

**A:** Convert the Aurora cluster to an Aurora global database, with the secondary cluster deployed in us-west-2. Rely on Aurora global database managed failover to meet RTO and RPO objectives

---

## Question 170

**Q:** What is the MOST operationally efficient way to achieve this?

**A:** Use AWS Budgets to create a daily coverage budget specifically for Compute Savings Plans. Define a coverage threshold and configure notifications to alert relevant stakeholders

---

## Question 171

**Q:** As a solutions architect, which of the following AWS services would you recommend addressing this use-case?

**A:** AWS VPN CloudHub

---

## Question 172

**Q:** As a solutions architect, which of the following options would you recommend as the solution?

**A:** Create a public Network Load Balancer that links to Amazon EC2 instances that are bastion hosts managed by an Auto Scaling Group

---

## Question 173

**Q:** Which of the following is the MOST cost-effective way of isolating the Amazon EC2 instances to a single tenant?

**A:** Dedicated Instances

---

## Question 174

**Q:** Which of the following options would you suggest?

**A:** Set up a total of two NAT gateways. NAT gateway N1 should be set up in public subnet PU1 in Availability Zone A1. NAT gateway N2 should be set up in public subnet PU2 in Availability Zone A2

---

## Question 175

**Q:** Which of the following options do you recommend as the MOST cost-effective solution?

**A:** Run on a Spot Instance with a persistent request type

---

## Question 176

**Q:** Which database would you recommend using?

**A:** Amazon Aurora Serverless

---

## Question 177

**Q:** As a solutions architect, which of the following will you recommend?

**A:** Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 as the document store

---

## Question 178

**Q:** Which AWS Directory Service is the best fit for this requirement?

**A:** AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)

---

## Question 179

**Q:** What do you recommend?

**A:** Client Side Encryption

---

## Question 180

**Q:** How can you build this index efficiently?

**A:** Create an application that will traverse the S3 bucket, issue a Byte Range Fetch for the first 250 bytes, and store that information in Amazon RDS

---

## Question 181

**Q:** Which solution meets these requirements most cost-effectively?

**A:** Define an S3 Lifecycle policy that transitions datasets to S3 Standard-Infrequent Access (S3 Standard-IA) 30 days after creation and schedules the deletion of each object exactly 4 years after its creation

---

## Question 182

**Q:** As a solutions architect, which of the following networking components would you recommend on the Amazon EC2 instances running these HPC workflows?

**A:** Elastic Fabric Adapter (EFA)

---

## Question 183

**Q:** How can you efficiently prevent attackers from overwhelming your application?

**A:** Use an AWS Web Application Firewall (AWS WAF) and setup a rate-based rule

---

## Question 184

**Q:** Which solution best satisfies these requirements in the most cost-effective manner?

**A:** Create a gateway VPC endpoint for Amazon S3 and update the route table for the private subnet to direct S3 traffic through the endpoint

---

## Question 185

**Q:** Which solution should a solutions architect implement to address these requirements in the most secure manner?

**A:** Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer

---

## Question 186

**Q:** As a solutions architect, which of the following AWS services would you recommend that can provide support for quick and easy migration from RabbitMQ?

**A:** Amazon MQ

---

## Question 187

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Enable Amazon S3 Storage Lens with advanced metrics and recommendations. Use the per-bucket dashboard to filter and view versioning status across Regions and identify all buckets that do not have versioning enabled

---

## Question 188

**Q:** Which of the following represents the best way of configuring a solution for this requirement with minimal effort?

**A:** Run the custom scripts as user data scripts on the Amazon EC2 instances

---

## Question 189

**Q:** What can you do to decrease the replication cost?

**A:** Use the Amazon EC2 instances private IP for the replication

---

## Question 190

**Q:** Which Amazon EBS volume type is the correct choice for these Amazon EC2 instances?

**A:** Provisioned IOPS SSD Amazon EBS volumes

---

## Question 191

**Q:** Which configuration should the network engineering team implement to allow direct access to Amazon S3 from the on-premises data center using Direct Connect?

**A:** Provision a Public Virtual Interface (Public VIF) on the Direct Connect connection to access Amazon S3 public IP addresses from the on-premises data center

---

## Question 192

**Q:** What is the MOST cost-effective way to establish such a connection?

**A:** Set up an AWS Site-to-Site VPN connection

---

## Question 193

**Q:** Which solution will meet these requirements in the MOST efficient and scalable way?

**A:** Use an Amazon Kinesis Data Streams stream in on-demand capacity mode to ingest user engagement data. Configure an AWS Lambda function as a consumer to process the events in real time

---

## Question 194

**Q:** Which AWS service can be used to protect the Amazon EC2 instances from such unauthorized behavior in the future?

**A:** Amazon GuardDuty

---


