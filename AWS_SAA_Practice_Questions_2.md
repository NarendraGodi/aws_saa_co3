# AWS SAA-C03 Practice Questions - Part 2

Total Questions: 194

---

## Question 1

**Q:** Which solution will meet these requirements?

**A:** Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend to use AWS Lambda functions that are invoked by Amazon API Gateway. Migrate the database to Amazon Aurora Serverless for auto-scaling.

---

## Question 2

**Q:** How can the Solutions Architect make the application available on the internet?

**A:** Create an Application Load Balancer and associate three public subnets from the same Availability Zones as the private instances. Add the private instances to the ALB.

---

## Question 3

**Q:** How should the Solutions Architect deploy this solution cost-effectively?

**A:** Configure a static website using Amazon S3 and create a Route 53 failover routing policy.

---

## Question 4

**Q:** How can a Solutions Architect design a managed solution that will align with open-source software?

**A:** Launch the containers on Amazon Elastic Kubernetes Service (EKS) and EKS worker nodes.

---

## Question 5

**Q:** Which solution will meet these requirements?

**A:** Use IAM Roles Anywhere to issue temporary credentials to the application. Set up a trust relationship with IAM Identity Center and configure the application to assume the role using these credentials.

---

## Question 6

**Q:** An AWS Organization has an OU with multiple member accounts in it. The company needs to restrict the ability to launch only specific Amazon EC2 instance types. How can this policy be applied across the accounts with the least effort?

**A:** Create an SCP with a deny rule that denies all but the specific instance types

---

## Question 7

**Q:** Which solution meets these requirements?

**A:** Create an Amazon EFS file system with mount targets in each Availability Zone. Configure the application instances to mount the file system.

---

## Question 8

**Q:** Which architecture should the Solutions Architect choose to enable high availability?

**A:** Modify the Auto Scaling group to use two instances across each of three Availability Zones.

---

## Question 9

**Q:** Which solution will meet these requirements?

**A:** Use EMR runtime roles to enforce granular permissions for each department's workloads. Configure the EMR cluster to use these roles when submitting jobs.

---

## Question 10

**Q:** Which service should the solutions architect use?

**A:** Amazon FSx

---

## Question 11

**Q:** Which changes should a Solutions Architect make to the database tier to improve performance?

**A:** Migrate the database to an Amazon Aurora global database in MySQL compatibility mode. Configure the application tier in Europe to use the local reader endpoint.

---

## Question 12

**Q:** How can the migration be executed with minimal administrative effort and downtime?

**A:** Use the AWS Database Migration Service (DMS) to directly migrate the database to RDS

---

## Question 13

**Q:** Which storage solution meets these requirements?

**A:** Use Amazon S3 Intelligent-Tiering to automatically adjust storage costs based on the frequency of data access while maintaining high durability.

---

## Question 14

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Store the patient credentials in AWS Secrets Manager. Use the GetSecretValue API to securely retrieve the credentials in the application at runtime.

---

## Question 15

**Q:** Which configuration should the Solutions Architect recommend?

**A:** Amazon EBS General Purpose SSD (gp2)

---

## Question 16

**Q:** Which solution should the solutions architect recommend?

**A:** Amazon EBS General Purpose SSD (gp2)

---

## Question 17

**Q:** Which solution will fulfill these requirements with the LEAST operational overhead?

**A:** Use AWS Batch to run video processing jobs. Use AWS Step Functions to manage the workflow. Store the processed files in Amazon S3.

---

## Question 18

**Q:** Which action will be MOST effective in accomplishing this requirement?

**A:** Use Amazon EC2 Auto Scaling to scale out the middle tier instances based on the SQS queue depth.

---

## Question 19

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Configure Amazon RDS automated backups. Set the retention period to 35 days and enable point-in-time recovery for the past 10 days. Use AWS Backup to retain additional backups for 120 days.

---

## Question 20

**Q:** What should the solutions architect do to achieve this?

**A:** Deploy all the EC2 instances in the same Availability Zone to eliminate cross-AZ data transfer charges.

---

## Question 21

**Q:** Which design should a Solutions Architect implement to improve scalability?

**A:** Use Amazon Kinesis Data Streams to ingest the data. Process the data using AWS Lambda functions.

---

## Question 22

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Deploy the database on Amazon Aurora Serverless v2 to automatically scale the database capacity based on actual usage and handle fluctuations in workload.

---

## Question 23

**Q:** Which replacement to the NAS file share is MOST resilient and durable?

**A:** Migrate the file share to Amazon FSx for Windows File Server

---

## Question 24

**Q:** What is the BEST method for a solutions architect to modify the solution so users can see all documents?

**A:** Copy the data from all EBS volumes to Amazon EFS. Modify the application to save new documents to Amazon EFS

---

## Question 25

**Q:** What should a solutions architect do to meet this requirement?

**A:** Use AWS Secrets Manager to store the database credentials. Configure Secrets Manager to rotate the credentials automatically every 30 days. Update the game server application to retrieve credentials from Secrets Manager.

---

## Question 26

**Q:** What is the MOST secure way to share the log file?

**A:** Generate a presigned URL and ask the vendor to download the log file before the URL expires.

---

## Question 27

**Q:** How should the application be deployed for best inter-node performance?

**A:** In a cluster placement group

---

## Question 28

**Q:** How should a Solutions Architect configure the Auto Scaling group to resolve the performance issues whilst minimizing costs?

**A:** Implement a scheduled action that sets the desired capacity to 10 before business hours begin.

---

## Question 29

**Q:** Which solution will meet these requirements?

**A:** Use Amazon Elastic File System (Amazon EFS) and configure it in General Purpose performance mode. Mount the EFS file system on all EC2 instances.

---

## Question 30

**Q:** What is the MOST cost-effective storage solution that meets the requirements?

**A:** Configure a lifecycle policy to transition the objects to Amazon S3 Standard-Infrequent Access (S3 Standard-IA) after 30 days.

---

## Question 31

**Q:** Which DX configuration offers the HIGHEST resiliency?

**A:** Configure DX connections at multiple DX locations.

---

## Question 32

**Q:** Which solution will meet these requirements?

**A:** Set up Amazon S3 to use Multi-Region Access Points in an active-active configuration with a single global endpoint. Configure S3 Cross-Region Replication.

---

## Question 33

**Q:** Which solution will meet these requirements with the LEAST development effort?

**A:** Apply an EBS snapshot retention rule in Recycle Bin to retain snapshots for 7 days before permanent deletion.

---

## Question 34

**Q:** How can a Solutions Architect meet these requirements?

**A:** Move the documents and media files to an Amazon FSx for Windows File Server file system.

---

## Question 35

**Q:** What should a solutions architect do to meet these requirements?

**A:** Enable an RDS Proxy instance on your RDS Database.

---

## Question 36

**Q:** What should a solutions architect recommend?

**A:** Use Amazon ECS Service Auto Scaling with target tracking policies to scale when an Amazon CloudWatch alarm is breached.

---

## Question 37

**Q:** Which solution will meet these requirements?

**A:** Use the Amazon VPC CNI plugin for Kubernetes. Configure the custom subnets in the VPC and associate the subnets with the EKS cluster to allow pods to use them.

---

## Question 38

**Q:** How should a solutions architect address this issue?

**A:** Set a permissions boundary on the developer IAM role that denies attaching administrator access.

---

## Question 39

**Q:** Which combination of AWS services meets these requirements?

**A:** Amazon FSx for Lustre with Amazon S3.

---

## Question 40

**Q:** Which solution will meet these requirements with the LEAST Operational overhead?

**A:** Create an Amazon Machine Image (AMI) of the EC2 instance that runs the tasks. Create an Auto Scaling group with the AMI to run multiple copies of the instance.

---

## Question 41

**Q:** Which solution meets these requirements?

**A:** Create an Amazon FSx for Lustre file system. Connect the file system to the origin server. Ensure that the file system is connected to the application server.

---

## Question 42

**Q:** Which option meets these requirements?

**A:** Use client-side encryption with a master key stored in AWS KMS.

---

## Question 43

**Q:** How should lifecycle management be configured?

**A:** Transition to ONEZONE_IA after 30 days. After 90 days expire the objects

---

## Question 44

**Q:** What should the company do to improve the application's performance?

**A:** Configure an Amazon EC2 Auto Scaling target tracking policy for the processing tier instances. Use the SQS ApproximateNumberOfMessages metric to dynamically scale the tier based on queue length.

---

## Question 45

**Q:** Which configuration should a solutions architect use to meet these requirements with the LEAST operational overhead?

**A:** Create a Route 53 alias record for an Amazon CloudFront distribution and specify the ALB as the origin. Create custom error pages for the distribution

---

## Question 46

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Use DynamoDB global tables to replicate data automatically across multiple Regions. Deploy the tables in on-demand capacity mode to handle workload variability.

---

## Question 47

**Q:** What should a solutions architect do to meet these requirements?

**A:** Use Amazon ElastiCache to cache the database layer.

---

## Question 48

**Q:** What should the Solutions Architect recommend?

**A:** Create a read replica of the primary database and instruct the business analysts to direct queries to the replica.

---

## Question 49

**Q:** Which solution will meet these requirements?

**A:** Create and use a custom endpoint that targets the three high-capacity replicas.

---

## Question 50

**Q:** An application on Amazon Elastic Container Service (ECS) performs data processing in two parts. The second part takes much longer to complete. How can an Architect decouple the data processing from the backend application component?

**A:** Process each part using a separate ECS task. Create an Amazon SQS queue

---

## Question 51

**Q:** How can this be achieved?

**A:** Configure AWS Global Accelerator and configure the ALBs as targets

---

## Question 52

**Q:** Which solution will meet these requirements with the LEAST implementation effort?

**A:** Deploy Amazon FSx for Windows File Server in Multi-AZ mode. Configure a Windows Server failover cluster across two Amazon EC2 instances in different Availability Zones, using FSx for Windows File Server as the shared storage.

---

## Question 53

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Create a new S3 bucket that uses server-side encryption with AWS KMS multi-Region keys (SSE-KMS). Configure Cross-Region Replication (CRR). Load the data into the new S3 bucket. Use Amazon Athena to query the data.

---

## Question 54

**Q:** Which solution will meet these requirements?

**A:** Move the website to an Amazon S3 bucket. Configure an Amazon CloudFront distribution for the S3 bucket.

---

## Question 55

**Q:** What is the MOST cost-effective solution to solve this performance issue?

**A:** Create an Aurora Replica and use the replica endpoint for reporting.

---

## Question 56

**Q:** What is the MOST cost-effective solution?

**A:** Order 10 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier.

---

## Question 57

**Q:** How should a solutions architect address this issue?

**A:** Set an IAM permissions boundary on the developer IAM role that explicitly denies attaching the administrator policy

---

## Question 58

**Q:** What should a Solutions Architect do to meet these requirements?

**A:** Configure an AWS Storage Gateway file gateway.

---

## Question 59

**Q:** Which solution will meet these requirements with the MOST operational efficiency?

**A:** Use AWS Storage Gateway Volume Gateway in cached mode. Configure cached volumes as iSCSI targets to store the primary dataset in AWS and cache frequently accessed imaging data locally.

---

## Question 60

**Q:** Which solution should a Solutions Srchitect recommend to meet this requirement?

**A:** Configure encryption for the Amazon EBS volumes and Amazon RDS database with AWS KMS keys.

---

## Question 61

**Q:** What deployment changes should a Solutions Architect implement to meet these requirements with the LEAST operational overhead?

**A:** Configure AWS Transit Gateway between the accounts. Assign Direct Connect to the transit gateway and route network traffic to the on-premises servers.

---

## Question 62

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Configure the RDS backup retention policy to 30 days for automated backups. Use a script to identify and delete manual backups that are older than 30 days.

---

## Question 63

**Q:** Which solution meets these requirements?

**A:** Configure the route table for the private subnet so that it routes the outbound traffic to an AWS Network Firewall firewall then configure domain list rule groups.

---

## Question 64

**Q:** What should a Solutions Architect recommend to meet these requirements?

**A:** Update the script to copy data to an AWS Storage Gateway for File Gateway virtual appliance instead of the on-premises file server.

---

## Question 65

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Configure a DataSync task to transfer the files to S3 Standard-Infrequent Access (S3 Standard-IA). Use a lifecycle configuration to transition the files to S3 Deep Archive after 1 year with a retention period of 7 years.

---

## Question 66

**Q:** Which solution will meet these requirements?

**A:** Use Amazon Kinesis Data Streams to ingest the data streams and process the data with AWS Lambda. Store the data in Amazon OpenSearch Service for search and analysis. Use Amazon Managed Grafana to create visual dashboards.

---

## Question 67

**Q:** How can a Solutions Architect ensure the application has the required permissions?

**A:** Create an IAM role that has read/write permissions to the bucket and update the task definition to specify the role as the taskRoleArn.

---

## Question 68

**Q:** What should a solutions architect do to meet these requirements with the LEAST amount of operational overhead?

**A:** On the table, enable Amazon DynamoDB Streams. Subscriptions can be made to a single Amazon Simple Notification Service (Amazon SNS) topic using triggers.

---

## Question 69

**Q:** Which solution will meet these requirements?

**A:** Put the JSON documents in an Amazon S3 bucket. As documents arrive in the S3 bucket, create an AWS Lambda function that runs Python code to process them. Use Amazon Aurora DB clusters to store the results.

---

## Question 70

**Q:** Which architecture should the solutions architect choose that provides high availability?

**A:** Modify the Auto Scaling group to use four instances across each of two Availability Zones

---

## Question 71

**Q:** Which solution meets this requirement?

**A:** Create a Network Load Balancer in one VPC and an AWS PrivateLink endpoint for Amazon ECS in another VPC.

---

## Question 72

**Q:** Which solution will meet these requirements with the LEAST implementation effort?

**A:** Configure an Amazon CloudFront distribution for the S3 bucket to accelerate download performance. Enable S3 Transfer Acceleration to enhance upload performance.

---

## Question 73

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Use Amazon Aurora Serverless v2 to store the data. Enable serverless auto-scaling and configure automated backups to Amazon S3 with a 7-day retention period.

---

## Question 74

**Q:** What should the solutions architect do to meet these requirements?

**A:** Use an Amazon Simple Queue Service (Amazon SQS) queue to store the incoming GPS data. Modify the application to poll the queue for new messages and process the data.

---

## Question 75

**Q:** Which solution will meet these requirements with the LEAST development effort?

**A:** Configure Amazon Security Lake to automatically collect, normalize, and store security data in Amazon S3 for analysis.

---

## Question 76

**Q:** What should a solutions architect implement to meet these requirements?

**A:** Configure AWS Transit Gateway to connect the Direct Connect gateway to the VPCs in the new accounts. Route network traffic from the new accounts to the on-premises data center through the transit gateway.

---

## Question 77

**Q:** Which storage solution should the solutions architect use?

**A:** Amazon EC2 instance store

---

## Question 78

**Q:** Which storage solution should be used?

**A:** Amazon FSx for Lustre

---

## Question 79

**Q:** How can these requirements be met?

**A:** Use an AWS Storage Gateway file gateway to provide a locally accessible file system that replicates data to the cloud, then analyze the data in the AWS Cloud.

---

## Question 80

**Q:** Which solution will meet these requirements?

**A:** Use AWS Batch to orchestrate video editing jobs on Spot Instances. Store metadata in Amazon ElastiCache for Redis and processed video files in Amazon S3 Intelligent-Tiering.

---

## Question 81

**Q:** How can a Solutions Architect best meet these requirements?

**A:** Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple Availability Zones.

---

## Question 82

**Q:** Which solution will provide the MOST cost-effective results?

**A:** Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Scheduled Reserved Instances for the EC2 instances that run for 8 hours on Mondays.

---

## Question 83

**Q:** Which storage solution should a solutions architect recommend for use after the migration?

**A:** Use Amazon Elastic File System (Amazon EFS) to provide an NFS-compatible shared file system that integrates with AWS services.

---

## Question 84

**Q:** Which solution should a Solutions Architect recommend?

**A:** Deploy an AWS DataSync agent for the on-premises environment. Configure a task to replicate the data and connect it to a VPC endpoint.

---

## Question 85

**Q:** What is the quickest way to reduce the S3 spend with the LEAST operational overhead?

**A:** Transition the objects to the appropriate storage class by using an S3 Lifecycle configuration.

---

## Question 86

**Q:** Which database should a solutions architect recommend?

**A:** Amazon ElastiCache for Redis

---

## Question 87

**Q:** What action should the Solutions Architect take?

**A:** Enable an Amazon Route 53 health check.

---

## Question 88

**Q:** Which scaling configuration should a Solutions Architect use to optimize the applications performance?

**A:** Use a target tracking policy to dynamically scale the Auto Scaling group.

---

## Question 89

**Q:** How can the Solutions Architect meet these requirements?

**A:** Deploy a Network Load Balancer in front of the EC2 instances in each Region. Use AWS Global Accelerator to route traffic to the most optimal Regional endpoint.

---

## Question 90

**Q:** Which solution meets these requirements?

**A:** Configure Amazon CloudWatch Container Insights in the existing EKS cluster. View the metrics and logs in the CloudWatch console.

---

## Question 91

**Q:** An organization is extending a secure development environment into AWS. They have already secured the VPC including removing the Internet Gateway and setting up a Direct Connect connection. What else needs to be done to add encryption?

**A:** Setup a Virtual Private Gateway (VPG)

---

## Question 92

**Q:** Which solution will meet these requirements?

**A:** Create a gateway VPC endpoint for the S3 bucket. Update the VPC's route table to route all S3 traffic through the gateway endpoint.

---

## Question 93

**Q:** Which solution will meet these requirements?

**A:** Configure an API Gateway resource policy that denies access to any IP address that is not explicitly allowed.

---

## Question 94

**Q:** Which solution will meet these requirements with the MOST operational efficiency?

**A:** Convert the Aurora cluster to an Aurora global database. Configure cross-Region replication and managed failover.

---

## Question 95

**Q:** Which storage service meets these requirements and is the MOST cost-effective?

**A:** Amazon S3

---

## Question 96

**Q:** Which solution will meet these requirements with the LEAST amount of operational overhead?

**A:** Set up an ECS cluster behind an Application Load Balancer on AWS Fargate. Use Amazon Quantum Ledger Database (QLDB) to manage the storage layer.

---

## Question 97

**Q:** Which solution will meet these requirements?

**A:** Encrypt the documents by using client-side encryption with customer managed keys and upload the encrypted files to S3.

---

## Question 98

**Q:** Which solution meets these requirements?

**A:** Use Amazon FSx for Windows File Server for the Windows instances and the Linux instances.

---

## Question 99

**Q:** How can this be achieved?

**A:** Create an Amazon SQS queue and custom CloudWatch metric to measure the number of messages in the queue. Configure the ASG to scale based on the number of messages in the queue

---

## Question 100

**Q:** Which solution will meet these requirements?

**A:** Enable S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the objects to reduce the cost of KMS requests.

---

## Question 101

**Q:** How can a Solutions Architect meet these requirements?

**A:** Create an Amazon SQS FIFO queue to decouple the application. Configure an AWS Lambda function to process messages from the queue.

---

## Question 102

**Q:** Which solution will meet these requirements?

**A:** Configure AWS DMS Serverless to create a replication task that scales its capacity automatically based on workload demand.

---

## Question 103

**Q:** Which solution meets these requirements most efficiently?

**A:** Decouple the application components with an Amazon SQS queue. Configure a dead-letter queue to collect the requests that failed to process.

---

## Question 104

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Use AWS App Runner to containerize the application. Use App Runner to automatically deploy and manage the application without using ECS or EC2.

---

## Question 105

**Q:** What should a solutions architect recommend to reduce internet latency?

**A:** Set up AWS Global Accelerator and add endpoints

---

## Question 106

**Q:** Which solution will meet these requirements?

**A:** Enable S3 Object Lock on the required objects and set compliance mode.

---

## Question 107

**Q:** What is the effect of this policy?

**A:** Administrators can terminate an EC2 instance in the us-east-1 Region when the user's source IP is 10.1.2.28.

---

## Question 108

**Q:** Which solution best meets these requirements?

**A:** Create an Amazon EFS file system. Configure a mount target in each Availability Zone. Attach each instance to the appropriate mount target.

---

## Question 109

**Q:** What should a solutions architect do to accomplish this?

**A:** Create a service control policy in the root organizational unit to deny access to the services or actions

---

## Question 110

**Q:** What should the Solutions Architect do to meet these requirements?

**A:** Deploy a NAT gateway in the public subnet. Modify the route table in the private subnet to direct all internet traffic to the NAT gateway.

---

## Question 111

**Q:** Which solution meets these requirements?

**A:** Deploy CloudFront with an S3 origin and configure an origin access identity (OAI) to restrict access to the S3 bucket. Enable AWS WAF on the CloudFront distribution.

---

## Question 112

**Q:** Which solution will meet these requirements?

**A:** Create an Amazon Machine Image (AMI) for each application. Launch two EC2 instances for each application in different Availability Zones. Use an Application Load Balancer to distribute traffic evenly between the instances.

---

## Question 113

**Q:** Which service can be used to build a centralized data repository to be used for Machine Learning purposes?

**A:** AWS Lake Formation

---

## Question 114

**Q:** What is the best way to achieve this?

**A:** Use CloudFormation with scripts

---

## Question 115

**Q:** What should a Solutions Architect do to meet these requirements?

**A:** Use AWS Snowball.

---

## Question 116

**Q:** Which solution will meet these requirements MOST cost-effectively?

**A:** Configure an S3 gateway endpoint. Update the route table of the private subnet to direct S3 traffic through the endpoint.

---

## Question 117

**Q:** Which solution will improve storage performance?

**A:** Add more Provisioned IOPS SSD (io1) EBS volumes. Use OS commands to create a Logical Volume Management (LVM) stripe.

---

## Question 118

**Q:** What should a solutions architect recommend to the team?

**A:** Add a deny rule in the inbound table of the network ACL with a lower rule number than other rules

---

## Question 119

**Q:** Which solution will meet these requirements?

**A:** Use Amazon Route 53 latency routing policy to direct students to the Region with the lowest network latency. Use an internet-facing Application Load Balancer to distribute traffic across the EC2 instances within each Region.

---

## Question 120

**Q:** Which actions should a solutions architect take?

**A:** Use AWS CloudTrail to create a new trail. Configure the trail to log read and write data events on the S3 bucket that houses the reports. Log these events to a new bucket, and enable log file validation

---

## Question 121

**Q:** Which storage solution will meet these requirements in the MOST cost-effective way?

**A:** Use Amazon S3 File Gateway to provide low-latency storage for the on-premises application. The File Gateway will cache frequently accessed data locally.

---

## Question 122

**Q:** How can a Solutions Architect improve this architecture to remove any single point of failure?

**A:** Add additional VPNs to the Production VPC from a second customer gateway device.

---

## Question 123

**Q:** Which solution provides the required connectivity MOST securely?

**A:** Create a VPC with two private subnets. Deploy the RDS database in the private subnets. Establish connectivity between the on-premises office and AWS using AWS Site-to-Site VPN with a customer gateway.

---

## Question 124

**Q:** Which solution meets these requirements?

**A:** Create a web distribution on Amazon CloudFront pointing to an Amazon S3 origin. Create an ALIAS record in the Amazon Route 53 hosted zone that points to the CloudFront distribution, resolving to the application's URL domain name.

---

## Question 125

**Q:** Which solution meets these requirements?

**A:** Use Amazon FSx to create an SMB file share. Connect remote clients to the file share over a client VPN.

---

## Question 126

**Q:** Which solution addresses this concern?

**A:** Create an Amazon SQS queue to store incoming requests. Configure the microservices to retrieve the requests from the queue for processing.

---

## Question 127

**Q:** Which solution will meet these requirements?

**A:** Enable the Requester Pays feature on the content provider’s S3 bucket.

---

## Question 128

**Q:** How can a solutions architect automate the failover process?

**A:** Enable an Amazon Route 53 health check

---

## Question 129

**Q:** Which solution will meet these requirements?

**A:** Use Amazon FSx for NetApp ONTAP to consolidate storage and enable multi-protocol access for both SMB and NFS.

---

## Question 130

**Q:** Which solution will meet these requirements?

**A:** Set up an Amazon CloudFront distribution and configure the existing ALB as the origin. Use dynamic cache settings to reduce latency for global users.

---

## Question 131

**Q:** What should the solutions architect do to separate the read requests from the write requests?

**A:** Update the application to read from the Aurora Replica

---

## Question 132

**Q:** An application is being monitored using Amazon GuardDuty. A Solutions Architect needs to be notified by email of medium to high severity events. How can this be achieved?

**A:** Create an Amazon CloudWatch events rule that triggers an Amazon SNS topic

---

## Question 133

**Q:** Which solution would be MOST efficient?

**A:** Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3.

---

## Question 134

**Q:** Which configuration meets these requirements?

**A:** Create Amazon Route 53 records with a geolocation routing policy.

---

## Question 135

**Q:** Which lifecycle action meets the requirements whilst MINIMIZING cost?

**A:** Store the data in S3 Standard-IA for 3 months, then transition to S3 Glacier

---

## Question 136

**Q:** Which solution meets these requirements and is MOST cost-effective?

**A:** Set up an AWS DataSync agent on the on-premises servers and sync the data to Amazon S3.

---

## Question 137

**Q:** An Amazon RDS Read Replica is being deployed in a separate region. The master database is not encrypted but all data in the new region must be encrypted. How can this be achieved?

**A:** Encrypt a snapshot from the master DB instance, create a new encrypted master DB instance, and then create an encrypted cross-region Read Replica

---

## Question 138

**Q:** What actions should be taken to ensure compliance with these security requirements?

**A:** Deploy a Landing Zone within AWS Control Tower. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions on the created accounts.

---

## Question 139

**Q:** Which service can be used to decouple the compute services?

**A:** Amazon SNS

---

## Question 140

**Q:** Over 500 TB of data must be analyzed using standard SQL business intelligence tools. The dataset consists of a combination of structured data and unstructured data. The unstructured data is small and stored on Amazon S3. Which AWS services are most suitable for performing analytics on the data?

**A:** Amazon Redshift with Amazon Redshift Spectrum

---

## Question 141

**Q:** Which AWS service can be used for the migrated message broker?

**A:** Amazon MQ

---

## Question 142

**Q:** Which of the following groups of services will provide the solutions architect with the best solution ?

**A:** Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.

---

## Question 143

**Q:** What is the EASIEST method to meet this requirement?

**A:** Use Amazon CloudFront to serve the application and deny access to blocked countries

---

## Question 144

**Q:** Which solution should the Architect use?

**A:** Create an Amazon SQS queue and configure the front-end to add messages to the queue and the back-end to poll the queue for messages

---

## Question 145

**Q:** Which solution does AWS provide to help with this?

**A:** AWS Private 5G

---

## Question 146

**Q:** Which architecture offers the highest availability and low operational complexity?

**A:** Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Create an Auto Scaling group for the consumer EC2 instances across two Availability Zones. Use an Amazon RDS MySQL database with Multi-AZ enabled.

---

## Question 147

**Q:** The solutions architect requires a highly available solution. Which solution will be MOST cost-effective?

**A:** Use AWS Lambda to manipulate the original images to the requested customization. Store the original and manipulated images in Amazon S3. Configure an Amazon CloudFront distribution with the S3 bucket as the origin

---

## Question 148

**Q:** How can a solutions architect meet these requirements?

**A:** Hibernate the instance outside business hours. Start the instance again when required.

---

## Question 149

**Q:** Which AWS managed service could the Solutions Architect use?

**A:** AWS AppSync

---

## Question 150

**Q:** A company has divested a single business unit and needs to move the AWS account owned by the business unit to another AWS Organization. How can this be achieved?

**A:** Migrate the account using the AWS Organizations console

---

## Question 151

**Q:** A Solutions Architect needs to select a low-cost, short-term option for adding resilience to an AWS Direct Connect connection. What is the MOST cost-effective solution to provide a backup for the Direct Connect connection?

**A:** Implement an IPSec VPN connection and use the same BGP prefix

---

## Question 152

**Q:** Which DR strategy is the company using?

**A:** Pilot light

---

## Question 153

**Q:** A company is deploying an Amazon ElastiCache for Redis cluster. To enhance security a password should be required to access the database. What should the solutions architect use?

**A:** Redis AUTH command

---

## Question 154

**Q:** A legacy tightly-coupled High Performance Computing (HPC) application will be migrated to AWS. Which network adapter type should be used?

**A:** Elastic Fabric Adapter (EFA)

---

## Question 155

**Q:** Which action should the solutions architect take to accomplish this?

**A:** Use Amazon CloudFront with the S3 bucket as its origin

---

## Question 156

**Q:** What actions should be taken to ensure they are managing the licenses appropriately going forward?

**A:** Use AWS License Manager to manage the software licenses

---

## Question 157

**Q:** Which of the following combinations of services will deliver the best solution?

**A:** Use Amazon SageMaker to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data.

---

## Question 158

**Q:** An application in a private subnet needs to query data in an Amazon DynamoDB table. Use of the DynamoDB public endpoints must be avoided. What is the most EFFICIENT and secure method of enabling access to the table?

**A:** Create a gateway VPC endpoint and add an entry to the route table

---

## Question 159

**Q:** How can you configure this solution?

**A:** Create a VPC Security Group for the ELB and use AWS Lambda to automatically update the CloudFront internal service IP addresses when they change

---

## Question 160

**Q:** How can the Solutions Architect configure secure access to the database tier?

**A:** Configure the database security group to allow traffic only from the application security group

---

## Question 161

**Q:** Which solution should a Solutions Architect recommend?

**A:** Ingest the data into an Amazon Kinesis Data Stream. Process the data with an AWS Lambda function and then store the data in Amazon DynamoDB.

---

## Question 162

**Q:** What should a solutions architect do to protect the application?

**A:** Modify the configuration of AWS WAF to add an IP match condition to block the malicious IP address

---

## Question 163

**Q:** An Amazon RDS PostgreSQL database is configured as Multi-AZ. A solutions architect needs to scale read performance and the solution must be configured for high availability. What is the most cost-effective solution?

**A:** Create a read replica as a Multi-AZ DB instance

---

## Question 164

**Q:** What is the easiest way to achieve this goal?

**A:** AWS Compute Optimizer

---

## Question 165

**Q:** What should the Solutions Architect do to meet this requirement?

**A:** Enable detailed monitoring on all EC2 instances. Use Amazon CloudWatch metrics to perform the analysis.

---

## Question 166

**Q:** Which deployment option is MOST suitable for provisioning and managing the resources required for this use case?

**A:** Use AWS Batch to deploy a multi-node parallel job

---

## Question 167

**Q:** Three Amazon VPCs are used by a company in the same region. The company has two AWS Direct Connect connections to two separate company offices and wishes to share these with all three VPCs. A Solutions Architect has created an AWS Direct Connect gateway. How can the required connectivity be configured?

**A:** Associate the Direct Connect gateway to a transit gateway

---

## Question 168

**Q:** Which of the following solutions is MOST effective?

**A:** Configure an AWS WAF ACL with rate-based rules. Enable the WAF ACL on the Application Load Balancer.

---

## Question 169

**Q:** A large MongoDB database running on-premises must be migrated to Amazon DynamoDB within the next few weeks. The database is too large to migrate over the company’s limited internet bandwidth so an alternative solution must be used. What should a Solutions Architect recommend?

**A:** Use the Schema Conversion Tool (SCT) to extract and load the data to an AWS Snowball Edge device. Use the AWS Database Migration Service (DMS) to migrate the data to Amazon DynamoDB

---

## Question 170

**Q:** Which S3 storage class should be implemented to meet these requirements?

**A:** S3 Intelligent-Tiering

---

## Question 171

**Q:** What should the solutions architect do to meet these requirements?

**A:** Configure an Application Load Balancer in front of an Auto Scaling group to deploy instances to multiple Availability Zones

---

## Question 172

**Q:** Every time an item in an Amazon DynamoDB table is modified a record must be retained for compliance reasons. What is the most efficient solution to recording this information?

**A:** Enable DynamoDB Streams. Configure an AWS Lambda function to poll the stream and record the modified item data to an Amazon S3 bucket

---

## Question 173

**Q:** How can they achieve this goal?

**A:** Use capacity reservations with savings plans

---

## Question 174

**Q:** Which AWS service can assist them?

**A:** AWS DataSync

---

## Question 175

**Q:** What is the MOST cost-effective solution?

**A:** Amazon S3 Standard

---

## Question 176

**Q:** How can you assign these permissions only to the specific ECS task that is running the application?

**A:** Create an IAM policy with permissions to DynamoDB and assign It to a task using the taskRoleArn parameter

---

## Question 177

**Q:** What is the simplest way to achieve this, whilst adhering to the principle of least privilege?

**A:** Use S3 Access points to administer different access policies to each team, and control access points using Service Control Policies within AWS Organizations.

---

## Question 178

**Q:** How can the Solutions Architect securely store the database credentials and make them available to the function?

**A:** Store the credentials in Systems Manager Parameter Store and update the function code and execution role

---

## Question 179

**Q:** Which pricing model should the company choose?

**A:** On-Demand Instances

---

## Question 180

**Q:** What solution will best achieve this goal?

**A:** At the Edge Location, run your code with CloudFront Functions.

---

## Question 181

**Q:** Which scenario represents the easiest solution for this task?

**A:** Store the images in Amazon S3, behind a CloudFront distribution. Use S3 Object Lambda to transform and process the images whenever a GET request is initiated on an object.

---

## Question 182

**Q:** Which action should the Solutions Architect take?

**A:** Create an Amazon SQS FIFO queue

---

## Question 183

**Q:** How are these requirements best accomplished?

**A:** Migrate data using AWS Snowball. Provision an AWS VPN initially and order a Direct Connect link

---

## Question 184

**Q:** What should the company do to achieve this?

**A:** Use an API Gateway canary release deployment. Initially direct a small percentage of user traffic to the new API version. After API verification, promote the canary stage to the production stage.

---

## Question 185

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Order an AWS Snowball Edge Storage Optimized device. Copy the data to the device. and create a custom transformation job by using AWS Glue.

---

## Question 186

**Q:** What should a solutions architect do to remediate the vulnerability?

**A:** Create an Application Load Balancer. Put the web layer behind the load balancer and enable AWS WAF

---

## Question 187

**Q:** Which solution meets these requirements with the LEAST amount of operational overhead?

**A:** Add the aws:PrincipalOrgID global condition key with a reference to the organization ID to the S3 bucket policy.

---

## Question 188

**Q:** Which solution will meet this requirement with the LEAST operational overhead?

**A:** Configure a CloudWatch Logs subscription to stream the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service).

---

## Question 189

**Q:** Which solution options should be used?

**A:** Use an encrypted Amazon EBS volume and use Data Lifecycle Manager to automate snapshots

---

## Question 190

**Q:** Which solution will meet these requirements with the LEAST operational overhead?

**A:** Use AWS Config to identify all untagged resources and tag them programmatically. Then, use AWS Backup to automate the backup of all AWS resources based on tags.

---

## Question 191

**Q:** What actions should a Solutions Architect take to meet these requirements?

**A:** Use AWS Config to track configuration changes and AWS CloudTrail to record API calls and track access patterns in the AWS Cloud.

---

## Question 192

**Q:** Which solution will meet these requirements?

**A:** Take EBS snapshots of the production EBS volumes. Turn on the EBS fast snapshot restore feature on the EBS snapshots. Restore the snapshots into new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment.

---

## Question 193

**Q:** Which action will MOST securely grant the EC2 instance access to the S3 bucket?

**A:** Create an IAM role with least privilege permissions and attach it to the EC2 instance profile.

---

## Question 194

**Q:** Which solution will meet these requirements with the LEAST operational complexity?

**A:** Generate an API Gateway endpoint for the Lambda function. Provide the API Gateway endpoint to the third party for the webhook.

---


