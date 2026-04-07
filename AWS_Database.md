## AWS Services Reference

| Service | Description |
|---|---|
| **Amazon RDS (Relational Database Service)** | A managed relational database service that makes it easy to set up, operate, and scale databases in the cloud, supporting engines like MySQL, PostgreSQL, Oracle, and SQL Server. |
| **Amazon Aurora** | A MySQL and PostgreSQL-compatible relational database built for the cloud, offering up to 5x the performance of standard MySQL and 3x of PostgreSQL with high availability. |
| **Amazon Aurora Serverless v2** | An on-demand, auto-scaling configuration for Amazon Aurora that automatically adjusts capacity based on application demand, ideal for variable workloads. |
| **Amazon DynamoDB** | A fully managed, serverless NoSQL key-value and document database that delivers single-digit millisecond performance at any scale. |
| **Amazon ElastiCache** | A fully managed, in-memory caching service supporting Redis and Memcached, used to accelerate application and database performance. |
| **Amazon S3 (Simple Storage Service)** | An object storage service offering industry-leading scalability, data availability, security, and performance for storing and retrieving any amount of data. |
| **Amazon S3 Glacier** | A low-cost, durable cloud storage service for data archiving and long-term backup, designed for infrequently accessed data. |
| **Amazon CloudFront** | A fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs globally with low latency and high transfer speeds. |
| **AWS Global Accelerator** | A networking service that improves the availability and performance of applications by routing traffic through the AWS global network to the closest edge location. |
| **Amazon SQS (Simple Queue Service)** | A fully managed message queuing service that enables decoupling and scaling of microservices, distributed systems, and serverless applications. |
| **Amazon SNS (Simple Notification Service)** | A fully managed pub/sub messaging and mobile notifications service for coordinating message delivery to subscribing endpoints and clients. |
| **Amazon MQ** | A managed message broker service for Apache ActiveMQ and RabbitMQ that supports industry-standard messaging protocols like MQTT, AMQP, and STOMP. |
| **Amazon Kinesis Data Firehose** | A fully managed service for delivering real-time streaming data to destinations like Amazon S3, Redshift, and OpenSearch Service. |
| **Amazon EventBridge** | A serverless event bus that makes it easy to connect applications using data from AWS services, integrated SaaS apps, and custom sources. |
| **Amazon EC2 (Elastic Compute Cloud)** | A web service that provides secure, resizable compute capacity in the cloud, allowing you to run virtual servers on demand. |
| **Amazon ECS (Elastic Container Service)** | A fully managed container orchestration service that makes it easy to deploy, manage, and scale containerized applications using Docker. |
| **Amazon EFS (Elastic File System)** | A fully managed, elastic NFS file system for use with AWS Cloud services and on-premises resources, designed exclusively for Linux-based workloads. |
| **Amazon FSx for Windows File Server** | A fully managed, highly reliable file storage service accessible over the SMB protocol, built on Windows Server and supporting NTFS and Active Directory. |
| **AWS Storage Gateway** | A hybrid cloud storage service that gives on-premises applications access to virtually unlimited cloud storage by connecting on-premises environments to AWS storage services. |
| **AWS DataSync** | An online data transfer service that simplifies, automates, and accelerates moving data between on-premises storage systems and AWS storage services. |
| **AWS Application Migration Service (MGN)** | A lift-and-shift migration service that simplifies migrating applications from on-premises or other clouds to AWS by replicating servers and performing cutovers. |
| **AWS DMS (Database Migration Service)** | A cloud service that helps migrate databases to AWS quickly and securely, supporting both homogeneous and heterogeneous database migrations. |
| **AWS Backup** | A fully managed centralized backup service that automates and centralizes data protection across AWS services including RDS, EFS, DynamoDB, and more. |
| **AWS Snowball** | A petabyte-scale data transport solution using secure physical appliances to transfer large amounts of data into and out of AWS, each with up to 80 TB of usable storage. |
| **Amazon Route 53** | A highly available and scalable cloud Domain Name System (DNS) web service that also supports health checks and traffic routing policies for failover. |
| **AWS Network Firewall** | A managed service that makes it easy to deploy essential network protections for all your Amazon VPCs, including domain list filtering and stateful traffic inspection. |
| **Amazon QuickSight** | A cloud-native business intelligence and data visualization service that enables you to create interactive dashboards and gain insights from your data. |
| **Amazon Athena** | An interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL; serverless with no infrastructure to manage. |
| **AWS Compute Optimizer** | A service that recommends optimal AWS resource configurations such as EC2 instance types and EBS volume sizes to reduce cost and improve performance. |
| **AWS Organizations** | A service for centrally managing and governing multiple AWS accounts, enabling policy-based management through organizational units (OUs) and service control policies (SCPs). |
| **Amazon VPC (Virtual Private Cloud)** | A service that lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network you define. |

---

## AWS Database – Practice Questions

---

### Question 14

**Q:** A global manufacturing company uses AWS Outposts servers to manage IoT workloads in its factories across multiple continents. The company regularly updates factory IoT software, consisting of 50 files. Which solution will meet this requirement with the LEAST operational overhead?

**Options:**

- Create Amazon S3 buckets in multiple Regions. Configure S3 Cross-Region Replication (CRR) between the buckets. Deploy updates from the nearest bucket to each factory location.
- Create an Amazon S3 bucket in the us-east-1 Region. Deploy AWS Outposts servers at the factories as S3 endpoints. Configure the servers to cache the updates locally.
- **✅ Create an Amazon S3 bucket in the us-east-1 Region. Set up an Amazon CloudFront distribution with the S3 bucket as the origin. Use signed URLs to download the software updates.**
- Create an Amazon S3 bucket in the us-east-1 Region. Configure Amazon S3 Transfer Acceleration for the bucket. Use the S3 Transfer Acceleration endpoint for faster downloads.

**A:** **Create an Amazon S3 bucket in the us-east-1 Region. Set up an Amazon CloudFront distribution with the S3 bucket as the origin. Use signed URLs to download the software updates.**

**Explanation:**

CloudFront distributes content through a worldwide network of edge locations, ensuring that software updates are delivered from the nearest location to each factory with low latency and high throughput. Signed URLs provide secure, controlled access to the updates.

- **CORRECT:** "Create an Amazon S3 bucket in the us-east-1 Region. Set up an Amazon CloudFront distribution with the S3 bucket as the origin. Use signed URLs to download the software updates" is the correct answer.
- **INCORRECT:** "Create Amazon S3 buckets in multiple Regions. Configure S3 Cross-Region Replication (CRR)..." is incorrect — managing multiple S3 buckets and CRR across regions adds operational overhead.
- **INCORRECT:** "Deploy AWS Outposts servers at the factories as S3 endpoints..." is incorrect — this adds unnecessary infrastructure complexity.
- **INCORRECT:** "Configure Amazon S3 Transfer Acceleration..." is incorrect — Transfer Acceleration speeds up transfers to a single S3 bucket but does not provide the global edge caching that CloudFront offers.

**References:**
- https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- https://digitalcloud.training/amazon-s3-and-glacier/
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 16

**Q:** A fintech company is modernizing its payments processing system to adopt a serverless microservices architecture. The company wants to decouple its services and implement an event-driven architecture. Which solution will meet these requirements MOST cost-effectively?

**Options:**

- Use Amazon MQ as a message broker to enable publish/subscribe communication between the payment microservices and the downstream services.
- Use Amazon Kinesis Data Firehose to deliver payment events to multiple S3 buckets. Configure downstream services to poll the buckets for event processing.
- Configure an Amazon EventBridge rule to capture payment events and route them to multiple AWS Lambda functions that handle downstream processing.
- **✅ Configure an Amazon SNS topic to receive payment events from an AWS Lambda function. Set up multiple subscribers, such as Lambda functions, to process the events.**

**A:** **Configure an Amazon SNS topic to receive payment events from an AWS Lambda function. Set up multiple subscribers, such as Lambda functions, to process the events.**

**Explanation:**

SNS is a fully managed pub/sub service that enables fan-out messaging to multiple subscribers simultaneously. It is serverless, cost-effective, and integrates natively with AWS Lambda, making it ideal for event-driven serverless microservices.

- **CORRECT:** "Configure an Amazon SNS topic to receive payment events from an AWS Lambda function. Set up multiple subscribers, such as Lambda functions, to process the events" is the correct answer.
- **INCORRECT:** "Configure an Amazon EventBridge rule..." is incorrect — EventBridge is more suited for routing events based on rules and patterns; SNS is simpler and more cost-effective for this fan-out use case.
- **INCORRECT:** "Use Amazon Kinesis Data Firehose..." is incorrect — Kinesis Data Firehose is designed for streaming data delivery to storage destinations, not for event-driven microservice communication.
- **INCORRECT:** "Use Amazon MQ..." is incorrect — Amazon MQ is a managed message broker for legacy applications that use standard messaging protocols; it adds more overhead than SNS for a serverless architecture.

**References:**
- https://docs.aws.amazon.com/sns/latest/dg/welcome.html
- https://docs.aws.amazon.com/eventbridge/latest/userguide/what-is-amazon-eventbridge.html
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 25

**Q:** A video production company is planning to move some of its workloads to the AWS Cloud. The company will require around 5 TB of storage for video processing with the maximum possible I/O performance. Which combinations of services should a Solutions Architect use to meet these requirements?

**Options:**

- Amazon EBS for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage.
- Amazon EBS for maximum performance, Amazon EFS for durable data storage, and Amazon S3 Glacier for archival storage.
- Amazon EC2 instance store for maximum performance, Amazon EFS for durable data storage, and Amazon S3 for archival storage.
- **✅ Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage.**

**A:** **Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage.**

**Explanation:**

EC2 instance store volumes provide the highest possible I/O performance for temporary processing workloads where data can be recreated from source files. Amazon S3 provides 99.999999999% durability for storing processed data, and S3 Glacier offers low-cost archival storage.

- **CORRECT:** "Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage" is the correct answer.
- **INCORRECT:** "Amazon EBS for maximum performance..." is incorrect — EBS does not provide as much I/O performance as an instance store for this type of workload.
- **INCORRECT:** "Amazon EC2 instance store for maximum performance, Amazon EFS for durable data storage..." is incorrect — EFS does not provide as much durability as Amazon S3 (99.999999999%).
- **INCORRECT:** "Amazon EBS for maximum performance, Amazon EFS for durable data storage..." is incorrect — both EBS and EFS are not the best choices for maximum I/O performance or durability respectively.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- https://aws.amazon.com/s3/storage-classes/
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 30 (a)

**Q:** A company is working with a strategic partner that has an application that must be able to send messages to one of the company's Amazon SQS queues. The partner company has its own AWS account. How can a Solutions Architect provide least privilege access to the partner?

**Options:**

- Update the permission policy on the SQS queue to grant all permissions to the partner's AWS account.
- Create a user account and grant the sqs:SendMessage permission for Amazon SQS. Share the credentials with the partner company.
- **✅ Update the permission policy on the SQS queue to grant the sqs:SendMessage permission to the partner's AWS account.**
- Create a cross-account role with access to all SQS queues and use the partner's AWS account in the trust document for the role.

**A:** **Update the permission policy on the SQS queue to grant the sqs:SendMessage permission to the partner's AWS account.**

**Explanation:**

Amazon SQS supports resource-based policies. The best way to grant permissions following the principle of least privilege is to use a resource-based policy attached to the SQS queue that grants the partner's AWS account only the `sqs:SendMessage` permission on that specific queue.

- **CORRECT:** "Update the permission policy on the SQS queue to grant the sqs:SendMessage permission to the partner's AWS account" is the correct answer.
- **INCORRECT:** "Create a user account and grant the sqs:SendMessage permission for Amazon SQS. Share the credentials with the partner company" is incorrect — sharing credentials is a security risk and provides permissions beyond just the one queue.
- **INCORRECT:** "Create a cross-account role with access to all SQS queues..." is incorrect — this would provide access to all SQS queues, violating least privilege.
- **INCORRECT:** "Update the permission policy on the SQS queue to grant all permissions..." is incorrect — this provides too many permissions; the partner only needs to send messages.

**References:**
- https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-basic-examples-of-sqs-policies.html
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 34 (a)

**Q:** A company runs an application that uses an Amazon RDS PostgreSQL database. The database is currently not encrypted. A Solutions Architect has been instructed that due to new compliance requirements all data must be encrypted. The database has a high rate of change. How can the Solutions Architect enable encryption for the database without incurring any data loss?

**Options:**

- Create a snapshot of the existing RDS DB instance. Create an encrypted copy of the snapshot. Create a new RDS DB instance from the encrypted snapshot. Configure the application to use the new DB endpoint.
- Create an RDS read replica and specify an encryption key. Promote the encrypted read replica to primary. Update the application to point to the new RDS DB endpoint.
- Update the RDS DB to Multi-AZ mode and enable encryption for the standby replica. Perform a failover to the standby instance and then delete the unencrypted RDS DB instance.
- **✅ Create a snapshot of the existing RDS DB instance. Create an encrypted copy of the snapshot. Create a new RDS DB instance from the encrypted snapshot and update the application. Use AWS DMS to synchronize data between the source and target databases.**

**A:** **Create a snapshot of the existing RDS DB instance. Create an encrypted copy of the snapshot. Create a new RDS DB instance from the encrypted snapshot and update the application. Use AWS DMS to synchronize data between the source and target databases.**

**Explanation:**

You cannot change the encryption status of an existing RDS DB instance — encryption must be specified at creation. The best approach is to take a snapshot, create an encrypted copy, and restore a new encrypted instance. Because the database has a high rate of change, AWS DMS is used to capture and synchronize changes from the source (unencrypted) to the target (encrypted) database with minimal downtime.

- **CORRECT:** "Create a snapshot... Create an encrypted copy... Create a new RDS DB instance... Use AWS DMS to synchronize data" is the correct answer.
- **INCORRECT:** "Create a snapshot... Configure the application to use the new DB endpoint" is incorrect — without DMS to sync ongoing changes, data written after the snapshot is taken will be lost.
- **INCORRECT:** "Create an RDS read replica and specify an encryption key..." is incorrect — you cannot create an encrypted read replica from an unencrypted source.
- **INCORRECT:** "Update the RDS DB to Multi-AZ mode and enable encryption for the standby replica..." is incorrect — you cannot enable encryption on a standby replica of an unencrypted instance.

**References:**
- https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/encrypt-an-existing-amazon-rds-for-postgresql-db-instance.html
- https://digitalcloud.training/amazon-rds/

---

### Question 35 (a)

**Q:** A global logistics company hosts its shipment tracking system in the eu-west-1 Region. The system runs on Amazon EC2 instances, and customers access the shipment tracking API to retrieve real-time updates. The company wants to improve API response times for international customers in a cost-effective manner. Which solution will meet these requirements MOST cost-effectively?

**Options:**

- Deploy Amazon CloudFront in front of the API. Configure the API response to be cached and use the CachingOptimized managed policy to improve efficiency and reduce latency for frequently requested data.
- Deploy EC2 instances hosting the API in Asia and South America. Use an Application Load Balancer to distribute traffic across all Regions based on the geolocation of customer requests.
- **✅ Use AWS Global Accelerator to route traffic through the closest AWS edge location to customers. Configure endpoint groups for the shipment tracking API to distribute traffic globally and reduce response times.**
- Establish an AWS Direct Connect connection with a public virtual interface (VIF) from each international customer's data center to the eu-west-1 Region. Route API requests over the Direct Connect connection.

**A:** **Use AWS Global Accelerator to route traffic through the closest AWS edge location to customers. Configure endpoint groups for the shipment tracking API to distribute traffic globally and reduce response times.**

**Explanation:**

AWS Global Accelerator improves performance for dynamic, non-cacheable API traffic by routing requests through the AWS global network backbone to the optimal endpoint. Unlike CloudFront, which is best for cacheable content, Global Accelerator is suited for real-time API responses where caching is not applicable.

- **CORRECT:** "Use AWS Global Accelerator..." is the correct answer.
- **INCORRECT:** "Establish an AWS Direct Connect connection..." is incorrect — Direct Connect is expensive and typically used for enterprise private connectivity, not for improving public API latency for individual customers.
- **INCORRECT:** "Deploy Amazon CloudFront in front of the API..." is incorrect — CloudFront is better suited for cacheable content; real-time tracking data changes frequently and cannot be effectively cached.
- **INCORRECT:** "Deploy EC2 instances... in Asia and South America..." is incorrect — deploying and managing EC2 instances in multiple Regions adds significant operational and cost overhead.

**References:**
- https://docs.aws.amazon.com/global-accelerator/latest/dg/introduction.html
- https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-cache-policies.html
- https://digitalcloud.training/aws-global-accelerator/

---

### Question 54 (a)

**Q:** A healthcare organization operates multiple applications on virtual machines (VMs) in its on-premises data center. Due to increasing demand for its services, the data center can no longer scale quickly enough. The company wants to migrate its applications to AWS with minimal changes. Which combination of steps will meet these requirements? (Select THREE.)

**Options:**

- **✅ Stop all operations on the VMs. Perform a cutover by launching the migrated instances in AWS.**
- **✅ Use AWS Application Migration Service to replicate the VMs to AWS. Install the AWS Replication Agent on each VM.**
- Install the AWS Systems Manager Agent on the VMs to streamline operational management during migration.
- Use AWS App Runner to containerize the workloads before migrating them to AWS.
- Use AWS Server Migration Service (AWS SMS) to automate the migration of VMs to Amazon EC2 instances.
- **✅ Complete the initial data replication from the VMs to AWS. Launch test instances to perform acceptance tests for the workloads.**

**A:** **Use AWS Application Migration Service + Install Replication Agent**, **Complete initial replication + Launch test instances**, and **Stop operations on VMs + Perform cutover.**

**Explanation:**

AWS Application Migration Service (MGN) is the recommended lift-and-shift migration service. The standard process involves installing the Replication Agent, completing initial replication, testing with launch test instances, and performing a final cutover.

- **CORRECT:** "Use AWS Application Migration Service to replicate the VMs to AWS. Install the AWS Replication Agent on each VM" is correct.
- **CORRECT:** "Complete the initial data replication from the VMs to AWS. Launch test instances to perform acceptance tests" is correct.
- **CORRECT:** "Stop all operations on the VMs. Perform a cutover by launching the migrated instances in AWS" is correct.
- **INCORRECT:** "Use AWS Server Migration Service (AWS SMS)..." is incorrect — AWS SMS has been deprecated in favor of AWS Application Migration Service.
- **INCORRECT:** "Install the AWS Systems Manager Agent on the VMs..." is incorrect — SSM Agent is useful for post-migration management, not the migration process itself.
- **INCORRECT:** "Use AWS App Runner to containerize the workloads..." is incorrect — containerizing workloads adds complexity and does not align with a lift-and-shift migration.

**References:**
- https://docs.aws.amazon.com/migrationhub/latest/ug/what-is-migrationhub.html
- https://docs.aws.amazon.com/mgn/latest/ug/what-is-aws-mgn.html
- https://digitalcloud.training/aws-migration-services/

---

### Question 63

**Q:** A healthcare company is migrating its on-premises Oracle database to an Amazon RDS for Oracle database. The database must meet compliance requirements to retain backups for 120 days. Additionally, the company requires point-in-time recovery. Which solution will meet these requirements with the LEAST operational overhead?

**Options:**

- **✅ Configure Amazon RDS automated backups. Set the retention period to 35 days and enable point-in-time recovery for the past 10 days. Use AWS Backup to retain additional backups for 120 days.**
- Use AWS Backup to create a backup plan for Amazon RDS with a 120-day retention period. Enable point-in-time recovery by combining AWS Backup and RDS automated backups.
- Set up Amazon S3 Lifecycle policies to retain database exports for 120 days. Use AWS Database Migration Service (AWS DMS) to export the database to Amazon S3 every 24 hours.
- Create an Amazon RDS manual snapshot every week. Use an AWS Lambda function to delete snapshots that are older than 120 days.

**A:** **Configure Amazon RDS automated backups. Set the retention period to 35 days and enable point-in-time recovery for the past 10 days. Use AWS Backup to retain additional backups for 120 days.**

**Explanation:**

RDS automated backups natively support point-in-time recovery (PITR) with a retention period of up to 35 days. AWS Backup extends retention beyond this limit (up to 120 days) with minimal operational overhead, combining the best of both services.

- **CORRECT:** "Configure Amazon RDS automated backups... Use AWS Backup to retain additional backups for 120 days" is the correct answer.
- **INCORRECT:** "Create an Amazon RDS manual snapshot every week. Use an AWS Lambda function to delete snapshots..." is incorrect — manual snapshot management introduces operational overhead and complexity.
- **INCORRECT:** "Use AWS Backup to create a backup plan for Amazon RDS with a 120-day retention period..." is incorrect — AWS Backup alone does not provide the native RDS point-in-time recovery granularity.
- **INCORRECT:** "Set up Amazon S3 Lifecycle policies to retain database exports... Use AWS DMS to export the database to Amazon S3 every 24 hours" is incorrect — DMS exports are not a replacement for point-in-time recovery and add high operational overhead.

**References:**
- https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html
- https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html
- https://digitalcloud.training/amazon-rds/

---

### Question 64 (a)

**Q:** A genomics research organization is building an application to analyze large datasets. Raw genomic data is stored in an Amazon S3 bucket, processed by multiple Amazon EC2 instances, and the results are stored in another S3 bucket. The organization wants to minimize data transfer costs. What should the solutions architect do to achieve this?

**Options:**

- Use Amazon Elastic Fabric Adapter (EFA) to enable high-speed data transfer between EC2 instances, reducing transfer costs.
- Use Amazon S3 Transfer Acceleration to optimize the transfer of data between the EC2 instances and the S3 buckets.
- **✅ Deploy all the EC2 instances in the same Availability Zone to eliminate cross-AZ data transfer charges.**
- Configure an Auto Scaling group to launch the EC2 instances in multiple Regions to distribute the processing workload.

**A:** **Deploy all the EC2 instances in the same Availability Zone to eliminate cross-AZ data transfer charges.**

**Explanation:**

Data transfer between EC2 instances in the same Availability Zone is free when using private IP addresses, whereas cross-AZ data transfer incurs charges. Deploying all processing instances in the same AZ as the S3 bucket region minimizes transfer costs.

- **CORRECT:** "Deploy all the EC2 instances in the same Availability Zone to eliminate cross-AZ data transfer charges" is the correct answer.
- **INCORRECT:** "Configure an Auto Scaling group to launch the EC2 instances in multiple Regions..." is incorrect — distributing workloads across multiple Regions increases cross-region data transfer costs significantly.
- **INCORRECT:** "Use Amazon Elastic Fabric Adapter (EFA)..." is incorrect — EFAs optimize network performance for HPC workloads but do not reduce data transfer costs.
- **INCORRECT:** "Use Amazon S3 Transfer Acceleration..." is incorrect — S3 Transfer Acceleration speeds up transfers to S3 from the internet but does not reduce costs for EC2-to-S3 transfers within AWS.

**References:**
- https://aws.amazon.com/ec2/pricing/on-demand/
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni-efa.html
- https://digitalcloud.training/amazon-ec2/

---

### Question 2

**Q:** A healthcare company is building a patient records management application that uses a relational database to store user data and configuration details. The company expects steady growth in the number of users and requires a solution that can handle fluctuations in workload efficiently. Which solution will meet these requirements MOST cost-effectively?

**Options:**

- Deploy the database on Amazon RDS. Use magnetic storage with Multi-AZ deployments to ensure durability and handle the read-heavy workload.
- **✅ Deploy the database on Amazon Aurora Serverless v2 to automatically scale the database capacity based on actual usage and handle fluctuations in workload.**
- Deploy the database on Amazon DynamoDB. Use on-demand capacity mode to automatically adjust throughput and accommodate workload changes.
- Deploy the database on Amazon RDS. Use General Purpose SSD (gp3) storage with a read replica to ensure consistent performance for read and write operations.

**A:** **Deploy the database on Amazon Aurora Serverless v2 to automatically scale the database capacity based on actual usage and handle fluctuations in workload.**

**Explanation:**

Aurora Serverless v2 automatically scales compute and memory capacity up or down in fine-grained increments based on actual application demand. It is ideal for variable or unpredictable workloads and eliminates the need to provision for peak capacity, making it the most cost-effective solution.

- **CORRECT:** "Deploy the database on Amazon Aurora Serverless v2..." is the correct answer.
- **INCORRECT:** "Deploy the database on Amazon RDS. Use General Purpose SSD (gp3) storage with a read replica..." is incorrect — while read replicas help with read-heavy workloads, they do not automatically scale capacity and require manual management.
- **INCORRECT:** "Deploy the database on Amazon DynamoDB. Use on-demand capacity mode..." is incorrect — DynamoDB is a NoSQL database that is not suitable for relational workloads requiring SQL and ACID compliance.
- **INCORRECT:** "Deploy the database on Amazon RDS. Use magnetic storage with Multi-AZ deployments..." is incorrect — magnetic storage is outdated, has lower performance, and is more expensive than modern SSD options.

**References:**
- https://docs.aws.amazon.com/rds/index.html
- https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html
- https://digitalcloud.training/amazon-aurora/

---

### Question 3

**Q:** A website runs on a Microsoft Windows server in an on-premises data center. The web server is being migrated to Amazon EC2 Windows instances in multiple Availability Zones on AWS. The web server currently uses a network-attached storage (NAS) file share. Which replacement to the NAS file share is MOST resilient and durable?

**Options:**

- **✅ Migrate the file share to Amazon FSx for Windows File Server**
- Migrate the file share to AWS Storage Gateway
- Migrate the file share to Amazon EBS
- Migrate the file share to Amazon Elastic File System (Amazon EFS)

**A:** **Migrate the file share to Amazon FSx for Windows File Server**

**Explanation:**

Amazon FSx for Windows File Server provides fully managed, highly reliable file storage accessible over the industry-standard SMB protocol. It is built on Windows Server and supports features such as DFS, Active Directory integration, and multi-AZ deployments, making it the most resilient and durable replacement for a Windows NAS file share.

- **CORRECT:** "Migrate the file share to Amazon FSx for Windows File Server" is the correct answer.
- **INCORRECT:** "Migrate the file share to Amazon Elastic File System (Amazon EFS)" is incorrect — EFS only supports Linux/NFS-based workloads and cannot be used with Windows instances.
- **INCORRECT:** "Migrate the file share to Amazon EBS" is incorrect — EBS is block storage attached to a single instance and is not a shared storage solution for multi-AZ deployments.
- **INCORRECT:** "Migrate the file share to AWS Storage Gateway" is incorrect — with Storage Gateway, files end up on Amazon S3, which is object-based storage, not a direct NAS file share replacement.

**References:**
- https://aws.amazon.com/fsx/windows/
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 18 (a)

**Q:** A web application is being deployed on an Amazon ECS cluster using the Fargate launch type. The application is expected to receive a large volume of traffic initially. The company wishes to ensure that the application can scale automatically to handle the traffic. What should a solutions architect recommend?

**Options:**

- **✅ Use Amazon ECS Service Auto Scaling with target tracking policies to scale when an Amazon CloudWatch alarm is breached.**
- Use Amazon EC2 Auto Scaling with simple scaling policies to scale when an Amazon CloudWatch alarm is breached.
- Use Amazon EC2 Auto Scaling to scale out on a schedule and back in once the load decreases.
- Use an AWS Lambda function to scale Amazon ECS based on metric breaches that trigger an Amazon CloudWatch alarm.

**A:** **Use Amazon ECS Service Auto Scaling with target tracking policies to scale when an Amazon CloudWatch alarm is breached.**

**Explanation:**

Amazon ECS uses the AWS Application Auto Scaling service to scale tasks. This is configured through ECS Service Auto Scaling. A Target Tracking Scaling policy increases or decreases the number of tasks based on a target value for a specific metric (e.g., CPU utilization or request count), providing automatic and responsive scaling.

- **CORRECT:** "Use Amazon ECS Service Auto Scaling with target tracking policies to scale when an Amazon CloudWatch alarm is breached" is the correct answer.
- **INCORRECT:** "Use Amazon EC2 Auto Scaling with simple scaling policies..." is incorrect — EC2 Auto Scaling applies to EC2 instances, not ECS Fargate tasks.
- **INCORRECT:** "Use Amazon EC2 Auto Scaling to scale out on a schedule..." is incorrect — scheduled scaling does not respond to actual traffic patterns and applies to EC2, not Fargate.
- **INCORRECT:** "Use an AWS Lambda function to scale Amazon ECS..." is incorrect — building custom Lambda-based scaling adds unnecessary operational overhead when ECS Service Auto Scaling handles this natively.

**References:**
- https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-auto-scaling.html
- https://digitalcloud.training/amazon-ecs-and-eks/

---

### Question 31

**Q:** A gaming company uses a web application to display scores. An Application Load Balancer is used to distribute load across Amazon EC2 instances which run the application. The application stores data in an Amazon RDS database. The company is experiencing poor read performance on the database due to a high volume of read requests from the leaderboard feature. What should a solutions architect do to meet these requirements?

**Options:**

- Connect the database and the application layer using RDS Proxy.
- Use AWS Lambda instead of Amazon EC2 for the compute layer.
- Use an Amazon DynamoDB table instead of RDS.
- **✅ Use Amazon ElastiCache to cache the database layer.**

**A:** **Use Amazon ElastiCache to cache the database layer.**

**Explanation:**

Amazon ElastiCache is a fully managed, in-memory caching service that accelerates application and database performance. Since the issues are caused by poor read performance, a caching solution offloads reads from the primary database instance, allowing the application to perform better without modifying the database schema.

- **CORRECT:** "Use Amazon ElastiCache to cache the database layer" is the correct answer.
- **INCORRECT:** "Connect the database and the application layer using RDS Proxy" is incorrect — RDS Proxy improves connection pooling but does not cache data or reduce read load on the database.
- **INCORRECT:** "Use AWS Lambda instead of Amazon EC2 for the compute layer" is incorrect — Lambda has a maximum timeout of 15 minutes and is not suitable for hosting continuously running leaderboard applications.
- **INCORRECT:** "Use an Amazon DynamoDB table instead of RDS" is incorrect — migrating to DynamoDB would not directly reduce the read load and would require significant schema changes.

**References:**
- https://aws.amazon.com/elasticache/
- https://digitalcloud.training/amazon-elasticache/

---

### Question 32

**Q:** A group of business analysts perform read-only SQL queries on an Amazon RDS database. The queries have become quite numerous and the database has experienced some performance degradation. The queries should return data that is as current as possible. What should the Solutions Architect recommend?

**Options:**

- Load the data into Amazon ElastiCache and instruct the business analysts to run their queries against the ElastiCache endpoint.
- Export the data to Amazon S3 and instruct the business analysts to run their queries using Amazon Athena.
- **✅ Create a read replica of the primary database and instruct the business analysts to direct queries to the replica.**
- Load the data into an Amazon Redshift cluster and instruct the business analysts to run their queries against the cluster.

**A:** **Create a read replica of the primary database and instruct the business analysts to direct queries to the replica.**

**Explanation:**

A read replica offloads SQL queries to a separate database instance that is kept in sync with the primary. This ensures that the data is up to date while reducing load on the primary instance. It is the simplest and most efficient solution for this use case.

- **CORRECT:** "Create a read replica of the primary database and instruct the business analysts to direct queries to the replica" is the correct answer.
- **INCORRECT:** "Export the data to Amazon S3 and instruct the business analysts to run their queries using Amazon Athena" is incorrect — Athena queries data in S3, which would require periodic exports and would not reflect the most current data.
- **INCORRECT:** "Load the data into an Amazon Redshift cluster..." is incorrect — this also requires exporting data and introduces latency; data would not be the most current.
- **INCORRECT:** "Load the data into Amazon ElastiCache..." is incorrect — ElastiCache is a key-value store and does not support SQL queries; creating a read replica is much simpler.

**References:**
- https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
- https://digitalcloud.training/amazon-rds/

---

### Question 33

**Q:** A retail company uses an Amazon Aurora MySQL DB cluster for its order management system. The cluster includes eight Aurora Replicas. The company wants to ensure that reporting queries from its analytics team are only directed to three specific high-capacity replicas. Which solution will meet these requirements?

**Options:**

- **✅ Create and use a custom endpoint that targets the three high-capacity replicas.**
- Use the reader endpoint to automatically distribute reporting queries across all replicas in the cluster.
- Direct reporting queries to the instance endpoints of the three high-capacity replicas.
- Create a cluster clone for the reporting workload and use the writer endpoint of the cloned cluster.

**A:** **Create and use a custom endpoint that targets the three high-capacity replicas.**

**Explanation:**

Aurora custom endpoints allow you to define a subset of replicas for specific workloads. By creating a custom endpoint targeting the three high-capacity replicas, the analytics team can send all reporting queries exclusively to those replicas, ensuring optimal performance without manual connection management.

- **CORRECT:** "Create and use a custom endpoint that targets the three high-capacity replicas" is the correct answer.
- **INCORRECT:** "Use the reader endpoint..." is incorrect — the reader endpoint distributes queries across ALL Aurora Replicas using load balancing, not just the high-capacity ones.
- **INCORRECT:** "Create a cluster clone for the reporting workload..." is incorrect — creating a cluster clone duplicates data unnecessarily, increasing costs without providing a connection management solution.
- **INCORRECT:** "Direct reporting queries to the instance endpoints of the three high-capacity replicas" is incorrect — managing connections manually to individual instance endpoints is inefficient and does not provide load balancing across the three replicas.

**References:**
- https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Endpoints.html
- https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
- https://digitalcloud.training/amazon-aurora/

---

### Question 34 (b)

**Q:** An application on Amazon Elastic Container Service (ECS) performs data processing in two parts. The second part takes much longer to complete. How can an Architect decouple the data processing from the backend?

**Options:**

- Process each part using a separate ECS task. Create an Amazon SNS topic and send a notification when the processing completes.
- **✅ Process each part using a separate ECS task. Create an Amazon SQS queue.**
- Process both parts using the same ECS task. Create an Amazon Kinesis Firehose stream.
- Create an Amazon DynamoDB table and save the output of the first part to the table.

**A:** **Process each part using a separate ECS task. Create an Amazon SQS queue.**

**Explanation:**

Amazon SQS is designed for decoupling application components. The first ECS task sends the output to an SQS queue, and the second ECS task polls the queue and processes messages at its own pace. This handles the disparity in processing times and decouples the two components.

- **CORRECT:** "Process each part using a separate ECS task. Create an Amazon SQS queue" is the correct answer.
- **INCORRECT:** "Process both parts using the same ECS task. Create an Amazon Kinesis Firehose stream" is incorrect — Kinesis Firehose is for streaming data delivery to storage destinations, not for decoupling application processing steps.
- **INCORRECT:** "Process each part using a separate ECS task. Create an Amazon SNS topic and send a notification when the processing completes" is incorrect — SNS is a notification service for fan-out, not a queue for handling processing backlogs.
- **INCORRECT:** "Create an Amazon DynamoDB table and save the output of the first part to the table" is incorrect — DynamoDB is a database, not a messaging queue; polling a DynamoDB table for unprocessed data is inefficient and not a best practice for decoupling.

**References:**
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 40

**Q:** A solutions architect is required to move 750 TB of data from a branch office's network-attached file system to Amazon S3 Glacier. The branch office's internet connection is poor, and the solution must be cost-effective. What is the MOST cost-effective solution?

**Options:**

- Order 10 AWS Snowball appliances and point these appliances to an S3 Glacier vault and put in place a bucket policy which will only allow access via a VPC endpoint.
- Copy the files directly from the network-attached file system to Amazon S3. Build a lifecycle policy to move the S3 objects across storage classes into Amazon S3 Glacier.
- Create a site-to-site VPN connection directly to an Amazon S3 bucket. Enforce the connection with a VPC Endpoint.
- **✅ Order 10 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier.**

**A:** **Order 10 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier.**

**Explanation:**

Each AWS Snowball device holds up to 80 TB of usable storage, so 10 devices are needed for 750 TB. Snowball avoids reliance on the poor internet connection. Data is first loaded to S3 (the only supported Snowball destination), and an S3 Lifecycle policy then transitions objects to S3 Glacier for long-term, low-cost archival.

- **CORRECT:** "Order 10 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier" is the correct answer.
- **INCORRECT:** "Create a site-to-site VPN connection directly to an Amazon S3 bucket..." is incorrect — over a poor internet connection, transferring 750 TB would be extremely slow and costly.
- **INCORRECT:** "Order 10 AWS Snowball appliances and point these appliances to an S3 Glacier vault..." is incorrect — S3 Glacier is not a direct Snowball destination; data must first go to an S3 bucket.
- **INCORRECT:** "Copy the files directly from the network-attached file system to Amazon S3..." is incorrect — a poor internet connection makes direct transfer of 750 TB impractical and slow.

**References:**
- https://aws.amazon.com/snowball/
- https://digitalcloud.training/aws-migration-services/

---

### Question 48 (a)

**Q:** An Amazon EC2 instance runs in a VPC network, and the network must be secured by a solutions architect. The EC2 instances contain highly sensitive data and have been launched in private subnets. Company policy restricts EC2 instances from downloading software patches from the internet. However, the EC2 instances must be able to download patches only from approved URLs. Which solution meets these requirements?

**Options:**

- Create an AWS WAF web ACL. Filter traffic requests based on source and destination IP address ranges with custom rules.
- Establish strict inbound rules for your security groups. Specify the URLs of the authorized software repositories on the internet in your outbound rule.
- **✅ Configure the route table for the private subnet so that it routes the outbound traffic to an AWS Network Firewall firewall then configure domain list rule groups.**
- Place an Application Load Balancer in front of your EC2 instances. Direct all outbound traffic to the ALB. For outbound access to the internet, use a URL-based rule listener in the ALB's target group.

**A:** **Configure the route table for the private subnet so that it routes the outbound traffic to an AWS Network Firewall firewall then configure domain list rule groups.**

**Explanation:**

AWS Network Firewall is a managed service that enables essential network protections for Amazon VPCs. Domain list rule groups allow you to filter outbound HTTP/HTTPS traffic based on domain names (URLs), permitting only approved URLs while blocking everything else.

- **CORRECT:** "Configure the route table for the private subnet so that it routes the outbound traffic to an AWS Network Firewall firewall then configure domain list rule groups" is the correct answer.
- **INCORRECT:** "Create an AWS WAF web ACL..." is incorrect — AWS WAF protects web applications from inbound HTTP/HTTPS threats; it cannot filter outbound traffic from EC2 instances.
- **INCORRECT:** "Establish strict inbound rules for your security groups. Specify the URLs..." is incorrect — security groups do not support URL-based filtering; they only filter by IP address and port.
- **INCORRECT:** "Place an Application Load Balancer in front of your EC2 instances. Direct all outbound traffic to the ALB..." is incorrect — ALBs are designed for inbound traffic distribution, not for filtering outbound traffic by URL.

**References:**
- https://aws.amazon.com/network-firewall/
- https://digitalcloud.training/amazon-vpc/

---

### Question 54 (b)

**Q:** A company hosts a monolithic web application on an Amazon EC2 instance. Application users have recently reported poor performance at specific times. Analysis of Amazon CloudWatch metrics shows that CPU utilization is at 100% during those periods. The company wants to resolve this performance issue and improve application availability. Which combination of steps will meet these requirements MOST cost-effectively? (Select TWO.)

**Options:**

- Create an Auto Scaling group and an Application Load Balancer to scale vertically.
- Create an Amazon Machine Image (AMI) from the web server. Reference the AMI in a new launch template.
- **✅ Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale vertically.**
- Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale horizontally.
- **✅ Create an Auto Scaling group and an Application Load Balancer to scale horizontally.**

**A:** **Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale vertically** and **Create an Auto Scaling group and an Application Load Balancer to scale horizontally.**

**Explanation:**

AWS Compute Optimizer analyzes EC2 utilization metrics and recommends a more appropriate (larger) instance type to handle the peak CPU load — this is vertical scaling. An Auto Scaling group with an Application Load Balancer enables horizontal scaling by adding more instances to distribute load, improving both performance and availability.

- **CORRECT:** "Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale vertically" is correct.
- **CORRECT:** "Create an Auto Scaling group and an Application Load Balancer to scale horizontally" is correct.
- **INCORRECT:** "Create an Amazon Machine Image (AMI) from the web server. Reference the AMI in a new launch template" is incorrect — creating an AMI and launch template alone does not address scaling or the performance issue.
- **INCORRECT:** "Create an Auto Scaling group and an Application Load Balancer to scale vertically" is incorrect — vertical scaling (changing instance type) is not achieved through Auto Scaling groups; Auto Scaling groups add/remove instances of the same type.
- **INCORRECT:** "Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale horizontally" is incorrect — Compute Optimizer recommends instance types for right-sizing (vertical scaling), not for horizontal scaling.

**References:**
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- https://aws.amazon.com/compute-optimizer
- https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
- https://digitalcloud.training/amazon-ec2-auto-scaling/

---

### Question 56

**Q:** A multi-tier application runs with eight front-end web servers in an Amazon EC2 Auto Scaling group in a single Availability Zone behind an Application Load Balancer. A solutions architect needs to modify the infrastructure to be highly available without modifying the application. Which architecture should the solutions architect choose that provides high availability?

**Options:**

- **✅ Modify the Auto Scaling group to use four instances across each of two Availability Zones**
- Create an Auto Scaling group that uses four instances across each of two subnets
- Create an Auto Scaling group that uses four instances across each of two Regions
- Create an Auto Scaling template that can be used to quickly create more instances in another Region

**A:** **Modify the Auto Scaling group to use four instances across each of two Availability Zones**

**Explanation:**

High availability can be enabled by modifying the existing Auto Scaling group to span multiple Availability Zones. The ASG will automatically balance the load across AZs, ensuring that if one AZ fails, the instances in the other AZ continue serving traffic.

- **CORRECT:** "Modify the Auto Scaling group to use four instances across each of two Availability Zones" is the correct answer.
- **INCORRECT:** "Create an Auto Scaling group that uses four instances across each of two Regions" is incorrect — EC2 Auto Scaling does not support multiple Regions.
- **INCORRECT:** "Create an Auto Scaling template that can be used to quickly create more instances in another Region" is incorrect — EC2 Auto Scaling does not support multiple Regions.
- **INCORRECT:** "Create an Auto Scaling group that uses four instances across each of two subnets" is incorrect — the subnets could be in the same AZ, which would not provide high availability.

**References:**
- https://aws.amazon.com/ec2/autoscaling/
- https://digitalcloud.training/amazon-ec2-auto-scaling/

---

### Question 62

**Q:** A transportation company uses GPS devices installed on its fleet of delivery trucks to monitor their location in real time. Each GPS device sends location updates every 5 minutes. During a peak delivery period, the web application was overwhelmed by the increased volume of GPS data, leading to data loss with no way to replay the events. The company wants to ensure that data is not lost during peak periods and that the application can process updates reliably. What should the solutions architect do to meet these requirements?

**Options:**

- Store the GPS location updates in an Amazon DynamoDB table. Modify the application to query the table for unprocessed data and process it. Use DynamoDB TTL to remove old records after processing.
- Use Amazon Kinesis Data Streams to ingest the GPS data. Configure an AWS Lambda function to process the data in real time and store results in an Amazon DynamoDB table.
- Use an Amazon S3 bucket to store the GPS location updates. Modify the application to periodically scan the bucket for new files and process the data.
- **✅ Use an Amazon Simple Queue Service (Amazon SQS) queue to store the incoming GPS data. Modify the application to poll the queue for new messages and process the data.**

**A:** **Use an Amazon Simple Queue Service (Amazon SQS) queue to store the incoming GPS data. Modify the application to poll the queue for new messages and process the data.**

**Explanation:**

SQS decouples the GPS data ingestion from the application processing. During peak periods, messages accumulate in the queue without being lost. The application polls the queue at its own pace, and messages are retained until successfully processed, ensuring no data loss.

- **CORRECT:** "Use an Amazon Simple Queue Service (Amazon SQS) queue..." is the correct answer.
- **INCORRECT:** "Use an Amazon S3 bucket to store the GPS location updates..." is incorrect — S3 is not ideal for real-time, message-driven processing and does not provide a polling/queue mechanism.
- **INCORRECT:** "Use Amazon Kinesis Data Streams to ingest the GPS data..." is incorrect — Kinesis is designed for high-throughput real-time streaming analytics; SQS is simpler and more appropriate for decoupling this workload.
- **INCORRECT:** "Store the GPS location updates in an Amazon DynamoDB table..." is incorrect — querying DynamoDB for unprocessed records adds complexity and DynamoDB is not designed as a message queue.

**References:**
- https://docs.aws.amazon.com/sqs/index.html
- https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-how-it-works.html
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 8 (a)

**Q:** A research organization is planning to migrate its simulation analysis platform to AWS. The platform stores simulation results and logs on an on-premises NFS server. The platform's codebase is legacy and cannot be easily modified. Which storage solution should a solutions architect recommend for use after the migration?

**Options:**

- Use Amazon FSx for Windows File Server to create a shared file system for data storage and access through the SMB protocol.
- **✅ Use Amazon Elastic File System (Amazon EFS) to provide an NFS-compatible shared file system that integrates with AWS services.**
- Use Amazon Elastic Block Store (Amazon EBS) volumes attached to each EC2 instance for storage. Use NFS software on the EC2 instances to create a shared file system.
- Use AWS Storage Gateway File Gateway to provide an NFS interface backed by Amazon S3 for storing and retrieving data.

**A:** **Use Amazon Elastic File System (Amazon EFS) to provide an NFS-compatible shared file system that integrates with AWS services.**

**Explanation:**

Amazon EFS is a fully managed, scalable, highly available NFS file system that supports the NFS protocol natively. Since the legacy codebase cannot be modified, EFS provides a drop-in replacement for the on-premises NFS server, allowing the application to continue operating without code changes.

- **CORRECT:** "Use Amazon Elastic File System (Amazon EFS) to provide an NFS-compatible shared file system that integrates with AWS services" is the correct answer.
- **INCORRECT:** "Use AWS Storage Gateway File Gateway..." is incorrect — File Gateway is typically used to integrate on-premises environments with cloud storage and is not intended as the primary storage after a full cloud migration.
- **INCORRECT:** "Use Amazon Elastic Block Store (Amazon EBS) volumes... Use NFS software on the EC2 instances..." is incorrect — using EBS with custom NFS software is complex to manage, not fully managed, and not highly available across instances.
- **INCORRECT:** "Use Amazon FSx for Windows File Server..." is incorrect — FSx for Windows uses the SMB protocol and is designed for Windows workloads; the platform uses NFS (Linux-based).

**References:**
- https://aws.amazon.com/efs/
- https://aws.amazon.com/storagegateway/file/
- https://digitalcloud.training/amazon-efs/

---

### Question 12

**Q:** A company has created a disaster recovery solution for an application that runs behind an Application Load Balancer (ALB). The DR solution consists of a second copy of the application running behind a second ALB in a different Region. The Solutions Architect must configure Route 53 so that if the primary ALB becomes unavailable, traffic will be automatically directed to the secondary ALB. What action should the Solutions Architect take?

**Options:**

- Configure an alarm on a CloudTrail trail.
- Use Amazon EventBridge to cluster the ALBs.
- Enable an ALB health check.
- **✅ Enable an Amazon Route 53 health check.**

**A:** **Enable an Amazon Route 53 health check.**

**Explanation:**

Amazon Route 53 health checks monitor the health and performance of your web applications, web servers, and other resources. Combined with a failover routing policy, Route 53 will direct traffic to the primary ALB unless health checks detect it as unavailable, at which point traffic is automatically routed to the secondary ALB in the DR Region.

- **CORRECT:** "Enable an Amazon Route 53 health check" is the correct answer.
- **INCORRECT:** "Enable an ALB health check" is incorrect — ALB health checks perform health checks on the instances behind the ALB, not on the ALB itself or the DNS routing layer.
- **INCORRECT:** "Use Amazon EventBridge to cluster the ALBs" is incorrect — you cannot cluster ALBs in any way.
- **INCORRECT:** "Configure an alarm on a CloudTrail trail" is incorrect — CloudTrail records API activity and does not monitor resource health for DNS failover.

**References:**
- https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html
- https://digitalcloud.training/amazon-route-53/

---

### Question 20 (a)

**Q:** An application runs on Amazon EC2 Linux instances. The application generates log files which are written using standard API calls. A storage solution is required that can be used to store the files indefinitely and must allow concurrent access from multiple EC2 instances. The solution must be cost-effective. Which storage service meets these requirements and is the MOST cost-effective?

**Options:**

- **✅ Amazon S3**
- Amazon EC2 instance store
- Amazon EBS
- Amazon EFS

**A:** **Amazon S3**

**Explanation:**

The application writes files using standard API calls, which is compatible with Amazon S3's REST API. S3 is a massively scalable key-based object store that is well-suited for storing large numbers of files. It supports concurrent access from many EC2 instances and is the most cost-effective storage option compared to EBS, EFS, and instance store.

- **CORRECT:** "Amazon S3" is the correct answer.
- **INCORRECT:** "Amazon EFS" is incorrect — while EFS does offer concurrent access from many EC2 Linux instances, it is not the most cost-effective solution.
- **INCORRECT:** "Amazon EBS" is incorrect — EBS is block storage that is typically attached to a single instance and is not the most cost-effective option for shared log storage.
- **INCORRECT:** "Amazon EC2 instance store" is incorrect — instance store is ephemeral storage; data is lost when the instance is powered off, making it unsuitable for long-term storage.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance.html
- https://digitalcloud.training/amazon-s3-and-glacier/

---

## Dump 7

---

### Question 1

**Q:** Storage capacity has become an issue for a company that runs application servers on-premises. The servers are connected to a combination of block storage and NFS storage solutions. The company requires a solution that supports their existing storage protocols but extends capacity into AWS. Which combination of changes can the company make to meet these requirements? (Select TWO.)

**Options:**

- Use AWS Direct Connect and mount an Amazon FSx for Windows File Server using iSCSI.
- Use Amazon Elastic File System (EFS) volumes to replace the block storage.
- Use the mount command on servers to mount Amazon S3 buckets using NFS.
- **✅ Use an AWS Storage Gateway file gateway to replace the NFS storage.**
- **✅ Use an AWS Storage Gateway volume gateway to replace the block storage.**

**A:** **Use an AWS Storage Gateway file gateway to replace the NFS storage** and **Use an AWS Storage Gateway volume gateway to replace the block storage.**

**Explanation:**

AWS Storage Gateway provides hybrid cloud storage solutions. The **volume gateway** replaces block-based storage systems (iSCSI protocol), and the **file gateway** replaces NFS file systems (NFS protocol). Both gateways store data backed by Amazon S3, extending on-premises capacity into AWS without changing existing protocols.

- **CORRECT:** "Use an AWS Storage Gateway file gateway to replace the NFS storage" is a correct answer.
- **CORRECT:** "Use an AWS Storage Gateway volume gateway to replace the block storage" is a correct answer.
- **INCORRECT:** "Use the mount command on servers to mount Amazon S3 buckets using NFS" is incorrect — you cannot mount S3 buckets using NFS as it is an object-based storage system.
- **INCORRECT:** "Use AWS Direct Connect and mount an Amazon FSx for Windows File Server using iSCSI" is incorrect — you cannot mount FSx for Windows File Server using iSCSI; it uses SMB.
- **INCORRECT:** "Use Amazon Elastic File System (EFS) volumes to replace the block storage" is incorrect — EFS uses NFS, not iSCSI, and cannot replace block storage.

**References:**
- https://docs.aws.amazon.com/storagegateway/
- https://digitalcloud.training/aws-storage-gateway/

---

### Question 8 (b)

**Q:** A solutions architect is designing an application on AWS. The compute layer will run in parallel across EC2 instances. The compute layer should scale based on the number of jobs to be processed. The business need is to have the flexibility to change the number of EC2 instances without affecting the rest of the application, and the solution must be durable against instance failures. Which design should the solutions architect use?

**Options:**

- Create an Amazon SNS topic to send the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on CPU usage.
- Create an Amazon SNS topic to send the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on the number of SNS messages.
- **✅ Create an Amazon SQS queue to hold the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on the number of items in the SQS queue.**
- Create an Amazon SQS queue to hold the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on CPU usage.

**A:** **Create an Amazon SQS queue to hold the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on the number of items in the SQS queue.**

**Explanation:**

Amazon SQS provides a durable, loosely coupled queue for storing jobs. The Auto Scaling group scales EC2 instances based on the `ApproximateNumberOfMessages` metric (backlog per instance), ensuring the number of instances matches the processing demand. If an instance fails, the message becomes visible again and is processed by another instance.

- **CORRECT:** "Create an Amazon SQS queue to hold the jobs that need to be processed... Set the scaling policy... based on the number of items in the SQS queue" is the correct answer.
- **INCORRECT:** "...Set the scaling policy for the Auto Scaling group to add and remove nodes based on CPU usage" is incorrect — scaling based on CPU usage does not directly correlate to the number of jobs waiting to be processed.
- **INCORRECT:** "Create an Amazon SNS topic to send the jobs..." is incorrect — SNS is a pub/sub notification service; it does not retain messages and cannot be used as a durable job queue.

**References:**
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
- https://digitalcloud.training/amazon-ec2-auto-scaling/
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 13

**Q:** A company is migrating a decoupled application to AWS. The application uses a message broker based on the MQTT protocol. The application will be migrated to Amazon EC2 instances and the solution for the message broker must support the MQTT protocol. Which AWS service can be used for the migrated message broker?

**Options:**

- Amazon SNS
- **✅ Amazon MQ**
- AWS Step Functions
- Amazon SQS

**A:** **Amazon MQ**

**Explanation:**

Amazon MQ is a managed message broker service for Apache ActiveMQ and RabbitMQ that supports industry-standard messaging protocols including MQTT, AMQP, STOMP, and OpenWire. Since the application already uses MQTT, Amazon MQ allows migration without code changes.

- **CORRECT:** "Amazon MQ" is the correct answer.
- **INCORRECT:** "Amazon SQS" is incorrect — SQS is an Amazon proprietary service and does not support industry-standard messaging APIs and protocols like MQTT.
- **INCORRECT:** "Amazon SNS" is incorrect — SNS is a notification service, not a message bus, and does not support MQTT.
- **INCORRECT:** "AWS Step Functions" is incorrect — Step Functions is a workflow orchestration service, not a message broker.

**References:**
- https://aws.amazon.com/amazon-mq/
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 15

**Q:** A company delivers content to subscribers distributed globally from an application running on AWS. The application uses a fleet of Amazon EC2 instances in a private subnet behind an Application Load Balancer. Due to a recent incident, the company wants to prevent users from specific countries from accessing the content. What is the EASIEST method to meet this requirement?

**Options:**

- Modify the ALB security group to deny incoming traffic from blocked countries.
- Modify the security group for EC2 instances to deny incoming traffic from blocked countries.
- Use a network ACL to block the IP address ranges associated with the specific countries.
- **✅ Use Amazon CloudFront to serve the application and deny access to blocked countries.**

**A:** **Use Amazon CloudFront to serve the application and deny access to blocked countries.**

**Explanation:**

Amazon CloudFront supports geographic restrictions (geo-restriction), which allows you to either whitelist countries that can access your content or blacklist countries that cannot. This is built into CloudFront and requires no custom rule management, making it the easiest solution.

- **CORRECT:** "Use Amazon CloudFront to serve the application and deny access to blocked countries" is the correct answer.
- **INCORRECT:** "Use a Network ACL to block the IP address ranges associated with the specific countries" is incorrect — maintaining an up-to-date list of IP ranges for entire countries is extremely complex and operationally burdensome.
- **INCORRECT:** "Modify the ALB security group to deny incoming traffic from blocked countries" is incorrect — security groups filter by IP address and port, not by geographic country.
- **INCORRECT:** "Modify the security group for EC2 instances to deny incoming traffic from blocked countries" is incorrect — security groups cannot filter traffic by country.

**References:**
- https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 30 (b)

**Q:** A legacy tightly-coupled High Performance Computing (HPC) application will be migrated to AWS. Which network adapter type should be used?

**Options:**

- Elastic Network Interface (ENI)
- **✅ Elastic Fabric Adapter (EFA)**
- Elastic IP Address
- Elastic Network Adapter (ENA)

**A:** **Elastic Fabric Adapter (EFA)**

**Explanation:**

An Elastic Fabric Adapter (EFA) is an AWS network interface with added capabilities specifically designed for tightly-coupled HPC applications. It provides low-latency, high-bandwidth networking using OS-bypass capabilities, which enables applications to communicate directly with the network hardware for maximum performance.

- **CORRECT:** "Elastic Fabric Adapter (EFA)" is the correct answer.
- **INCORRECT:** "Elastic Network Interface (ENI)" is incorrect — the ENI is a basic network adapter and is not optimized for HPC workloads.
- **INCORRECT:** "Elastic Network Adapter (ENA)" is incorrect — the ENA provides Enhanced Networking with high bandwidth and low latency but does not support the OS-bypass capabilities required for tightly-coupled HPC.
- **INCORRECT:** "Elastic IP Address" is incorrect — an Elastic IP address is a static public IP address, not a network adapter type.

**References:**
- https://aws.amazon.com/blogs/aws/now-available-elastic-fabric-adapter-efa-for-tightly-coupled-hpc-workloads/
- https://digitalcloud.training/amazon-ec2/

---

### Question 35 (b)

**Q:** An application is running on Amazon EC2 behind an Elastic Load Balancer (ELB). Content is being published using Amazon CloudFront and you need to restrict the ability for users to circumvent CloudFront and connect directly to the ELB. How can you configure this solution?

**Options:**

- **✅ Create a VPC Security Group for the ELB and use AWS Lambda to automatically update the CloudFront internal service IP addresses when they change.**
- Use signed URLs or signed cookies to limit access to the content.
- Use a Network ACL to restrict access to the ELB.
- Create an Origin Access Identity (OAI) and associate it with the distribution.

**A:** **Create a VPC Security Group for the ELB and use AWS Lambda to automatically update the CloudFront internal service IP addresses when they change.**

**Explanation:**

The only way to prevent users from bypassing CloudFront and connecting directly to the ELB is to configure a VPC Security Group on the ELB that only allows traffic from CloudFront's IP address ranges. Because CloudFront's IP ranges can change, an AWS Lambda function is used to automatically update the security group whenever Amazon publishes updated IP ranges.

- **CORRECT:** "Create a VPC Security Group for the ELB and use AWS Lambda to automatically update the CloudFront internal service IP addresses when they change" is the correct answer.
- **INCORRECT:** "Create an Origin Access Identity (OAI) and associate it with the distribution" is incorrect — OAI is used to restrict access to content in Amazon S3 buckets, not to EC2/ELB origins.
- **INCORRECT:** "Use signed URLs or signed cookies to limit access to the content" is incorrect — signed URLs/cookies control who can access the content but do not prevent users from connecting directly to the ELB endpoint.
- **INCORRECT:** "Use a Network ACL to restrict access to the ELB" is incorrect — while NACLs can filter traffic by IP, they require manual maintenance and security groups are the recommended approach for this use case.

**References:**
- https://aws.amazon.com/blogs/security/how-to-automatically-update-your-security-groups-for-amazon-cloudfront-and-aws-waf-by-using-aws-lambda/
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 37

**Q:** A solutions architect is creating a document submission application for a school. The application will use an Amazon S3 bucket for storage. The solution must prevent accidental deletion of the documents and ensure that all versions of the documents are available. Users must be able to upload and modify the documents. Which combination of actions should be taken to meet these requirements? (Select TWO.)

**Options:**

- Attach an IAM policy to the bucket.
- Encrypt the bucket using AWS SSE-S3.
- **✅ Enable versioning on the bucket.**
- Set read-only permissions on the bucket.
- **✅ Enable MFA Delete on the bucket.**

**A:** **Enable versioning on the bucket** and **Enable MFA Delete on the bucket.**

**Explanation:**

S3 Versioning retains a copy of every version of each document, so even if a document is deleted or overwritten, previous versions remain recoverable. MFA Delete adds an extra layer of protection by requiring multi-factor authentication to permanently delete object versions, preventing accidental or unauthorized deletions.

- **CORRECT:** "Enable versioning on the bucket" is a correct answer.
- **CORRECT:** "Enable MFA Delete on the bucket" is also a correct answer.
- **INCORRECT:** "Set read-only permissions on the bucket" is incorrect — this would prevent users from uploading and modifying documents, which is a requirement.
- **INCORRECT:** "Attach an IAM policy to the bucket" is incorrect — while IAM policies control access, they cannot specifically prevent delete operations while still allowing write/modify operations without additional complexity.
- **INCORRECT:** "Encrypt the bucket using AWS SSE-S3" is incorrect — encryption protects data at rest but does not prevent deletion of objects.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html
- https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingMFADelete.html
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 42

**Q:** The Chief Financial Officer of a large corporation is looking for an AWS native tool which will help reduce their cloud spend on EC2 compute resources. After receiving a budget alarm, the company has decided that they need to identify opportunities to reduce costs. What is the easiest way to achieve this goal?

**Options:**

- **✅ AWS Compute Optimizer**
- AWS Cost Explorer
- AWS Trusted Advisor
- Cost and Usage Reports

**A:** **AWS Compute Optimizer**

**Explanation:**

AWS Compute Optimizer analyzes the configuration and utilization metrics of your AWS resources, such as EC2 instance types and EBS volume configurations, and provides recommendations to optimize cost and performance. It identifies over-provisioned instances and recommends right-sized alternatives.

- **CORRECT:** "AWS Compute Optimizer" is the correct answer.
- **INCORRECT:** "AWS Trusted Advisor" is incorrect — while Trusted Advisor provides some cost recommendations, AWS Compute Optimizer provides more detailed, ML-powered recommendations specifically for compute resources.
- **INCORRECT:** "Cost and Usage Reports" is incorrect — Cost and Usage Reports provide highly detailed spending data but do not provide recommendations for right-sizing resources.
- **INCORRECT:** "AWS Cost Explorer" is incorrect — Cost Explorer provides graphical insights into spending and usage patterns but does not provide actionable right-sizing recommendations like Compute Optimizer.

**References:**
- https://aws.amazon.com/compute-optimizer/faqs/
- https://digitalcloud.training/aws-billing-and-pricing/

---

### Question 51

**Q:** A retail organization sends coupons out twice a week and this results in a predictable surge in sales traffic. The application runs on Amazon EC2 instances behind an Elastic Load Balancer. The organization wants to ensure capacity is available when needed but does not want to pay for it at other times. How can they achieve this goal?

**Options:**

- Increase the instance size of the existing EC2 instances.
- Purchase Amazon EC2 dedicated hosts.
- **✅ Use capacity reservations with savings plans.**
- Use a mixture of spot instances and on demand instances.

**A:** **Use capacity reservations with savings plans.**

**Explanation:**

On-Demand Capacity Reservations allow you to reserve EC2 compute capacity in a specific Availability Zone for any duration. Combined with Savings Plans (which provide discounted pricing), this ensures capacity is available during the predictable traffic surges while reducing the cost compared to standard On-Demand pricing.

- **CORRECT:** "Use capacity reservations with savings plans" is the correct answer.
- **INCORRECT:** "Use a mixture of spot instances and on demand instances" is incorrect — spot instances can be interrupted at any time, which is a risk for predictable, time-sensitive traffic surges.
- **INCORRECT:** "Increase the instance size of the existing EC2 instances" is incorrect — vertical scaling adds cost all the time, not just during the traffic surge periods.
- **INCORRECT:** "Purchase Amazon EC2 dedicated hosts" is incorrect — dedicated hosts are significantly more expensive than shared hosts and do not provide a cost-effective solution.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html
- https://digitalcloud.training/amazon-ec2/

---

### Question 60

**Q:** A company runs a large batch processing job at the end of every quarter. The processing job runs for 5 days and uses 15 Amazon EC2 instances. The processing must run uninterrupted for 5 hours per day. Which pricing model should the company choose?

**Options:**

- Spot Instances
- Reserved Instances
- Dedicated Instances
- **✅ On-Demand Instances**

**A:** **On-Demand Instances**

**Explanation:**

Each EC2 instance runs for 5 hours a day for 5 days per quarter, totaling 20 days per year. This short, infrequent usage does not justify the 1- or 3-year commitment of Reserved Instances. On-Demand Instances are the most cost-effective choice for this use case, with no upfront commitment and no minimum usage requirements.

- **CORRECT:** "On-Demand Instances" is the correct answer.
- **INCORRECT:** "Reserved Instances" is incorrect — Reserved Instances require a minimum 1-year commitment and are cost-effective only for continuously running or frequently used workloads.
- **INCORRECT:** "Spot Instances" is incorrect — Spot Instances can be interrupted at any time by AWS, and the requirement states that processing must run uninterrupted.
- **INCORRECT:** "Dedicated Instances" is incorrect — Dedicated Instances are more expensive than standard instances and do not provide a cost advantage for this use case.

**References:**
- https://aws.amazon.com/ec2/pricing/
- https://digitalcloud.training/amazon-ec2/

---

### Question 5

**Q:** A company uses several Windows Servers as the operating system of choice for all their application servers hosted in their data center. The company wants to move some file servers into the cloud, and the solution must support existing Active Directory configurations. The company has an existing AWS Direct Connect connection. What should a solutions architect do to meet these requirements?

**Options:**

- Install an NFS client on to the on-premises servers and mount an Amazon EFS file system to the servers. Mount the same file system to the EC2 instances within the Amazon VPC. Use the existing Direct Connect connection.
- **✅ Install an SMB client on to the on-premises servers and mount an Amazon FSx file system to the servers. Mount the same file system to the EC2 instances within the Amazon VPC. Use the existing Direct Connect connection.**
- Use Amazon S3 on Outposts and mount the S3 File Gateway on to the on-premises servers.
- Migrate all the data to Amazon DynamoDB Local. Ensure all users have the appropriate IAM permissions to access the relevant files.

**A:** **Install an SMB client on to the on-premises servers and mount an Amazon FSx file system to the servers. Mount the same file system to the EC2 instances within the Amazon VPC. Use the existing Direct Connect connection.**

**Explanation:**

Amazon FSx for Windows File Server supports the SMB protocol and integrates natively with Active Directory. The existing Direct Connect connection provides low-latency, private connectivity between on-premises Windows Servers and the FSx file system in AWS, creating a seamless hybrid file sharing environment.

- **CORRECT:** "Install an SMB client on to the on-premises servers and mount an Amazon FSx file system..." is the correct answer.
- **INCORRECT:** "Migrate all the data to Amazon DynamoDB Local..." is incorrect — DynamoDB is a NoSQL database and does not provide a file system interface compatible with Windows file shares.
- **INCORRECT:** "Use Amazon S3 on Outposts..." is incorrect — S3 on Outposts does not provide the hybrid cloud file share experience required and does not support Active Directory.
- **INCORRECT:** "Install an NFS client on to the on-premises servers and mount an Amazon EFS file system..." is incorrect — EFS uses the NFS protocol and is suitable for Linux clients only; it is not natively supported on Windows Servers.

**References:**
- https://docs.aws.amazon.com/efs/latest/ug/efs-onpremises.html
- https://digitalcloud.training/amazon-fsx/

---

### Question 18 (b)

**Q:** A company has multiple Windows workloads which are .NET application servers and Microsoft SQL Server databases running on Amazon EC2 instances with Windows Server 2016. The company requires a shared file system that is accessible by all EC2 instances and must support Active Directory, Windows ACLs, and DFS namespaces. What is the best way to meet this requirement?

**Options:**

- **✅ Extend the file share environment to Amazon FSx for Windows File Server with a Multi-AZ configuration. Migrate all the data to FSx for Windows File Server.**
- Migrate all the data to Amazon S3. Set up IAM authentication for users to access files.
- Set up an Amazon S3 File Gateway, mount the S3 File Gateway on the existing EC2 instances.
- Extend the file share environment to Amazon Elastic File System (Amazon EFS) with a Multi-AZ configuration. Migrate all the data to Amazon EFS.

**A:** **Extend the file share environment to Amazon FSx for Windows File Server with a Multi-AZ configuration. Migrate all the data to FSx for Windows File Server.**

**Explanation:**

Amazon FSx for Windows File Server is a fully managed Windows file system that supports SMB, NTFS, Active Directory integration, Windows ACLs, and DFS namespaces. A Multi-AZ configuration provides high availability. It is the ideal solution for Windows-specific workloads running on EC2.

- **CORRECT:** "Extend the file share environment to Amazon FSx for Windows File Server with a Multi-AZ configuration..." is the correct answer.
- **INCORRECT:** "Migrate all the data to Amazon S3. Set up IAM authentication for users to access files" is incorrect — S3 does not provide a Windows-native file system interface or support for Windows ACLs and DFS namespaces.
- **INCORRECT:** "Set up an Amazon S3 File Gateway..." is incorrect — S3 File Gateway is designed for hybrid cloud connectivity between on-premises environments and S3, not for native Windows EC2 workloads.
- **INCORRECT:** "Extend the file share environment to Amazon Elastic File System (Amazon EFS)..." is incorrect — EFS cannot be used with Microsoft Windows instances as it only supports the NFS protocol.

**References:**
- https://aws.amazon.com/fsx/windows/
- https://docs.aws.amazon.com/fsx/latest/WindowsGuide/managing-file-shares.html
- https://digitalcloud.training/amazon-fsx/

---

### Question 20 (b)

**Q:** An application analyzes images of people that are uploaded to an Amazon S3 bucket. The application determines demographic data which is then saved to a .CSV file in another S3 bucket. The data must be encrypted and analysts must be able to run SQL queries against the data. Which actions should a Solutions Architect take to encrypt and query the data?

**Options:**

- Use Amazon S3 server-side encryption and Amazon QuickSight to query the data.
- Use AWS KMS encryption keys for the S3 bucket and use Amazon Managed Service for Apache Flink to query the data.
- Use Amazon S3 server-side encryption and use Amazon RedShift Spectrum to query the data.
- **✅ Use AWS KMS encryption keys for the S3 bucket and use Amazon Athena to query the data.**

**A:** **Use AWS KMS encryption keys for the S3 bucket and use Amazon Athena to query the data.**

**Explanation:**

AWS KMS encryption keys provide robust server-side encryption for data stored in S3. Amazon Athena is a serverless, interactive SQL query service that can directly query data stored in S3, including KMS-encrypted data. Athena requires no infrastructure to manage and is highly cost-effective for this use case.

- **CORRECT:** "Use AWS KMS encryption keys for the S3 bucket and use Amazon Athena to query the data" is the correct answer.
- **INCORRECT:** "Use Amazon S3 server-side encryption and use Amazon RedShift Spectrum to query the data" is incorrect — Redshift Spectrum requires a running Redshift cluster, which adds cost and operational overhead compared to serverless Athena.
- **INCORRECT:** "Use AWS KMS encryption keys for the S3 bucket and use Amazon Managed Service for Apache Flink to query the data" is incorrect — Apache Flink is used for real-time stream processing analytics, not for ad hoc SQL queries on CSV files in S3.
- **INCORRECT:** "Use Amazon S3 server-side encryption and Amazon QuickSight to query the data" is incorrect — QuickSight is a business intelligence visualization tool, not a SQL query engine for running analytical queries on raw data.

**References:**
- https://d1.awsstatic.com/whitepapers/architecture/wellarchitected-Machine-Learning-Lens.pdf
- https://aws.amazon.com/athena/
- https://digitalcloud.training/amazon-athena/

---

### Question 32

**Q:** A software development firm uses AWS to run their compute instances across multiple accounts. These instances are individually billed. The company recently purchased an EC2 Reserved Instance (RI) for one account and wants the RI benefits to apply across all their AWS accounts. Which combination of steps should the company follow to achieve this? (Select TWO.)

**Options:**

- Use AWS Organizations to establish a new payer account and invite the other accounts to join this organization.
- **✅ Enable Reserved Instance sharing in the billing preferences section of the AWS Management Console for the account that purchased the existing RI.**
- Enable Reserved Instance sharing in the billing preferences section of the AWS Management Console for the management account.
- **✅ Establish an AWS Organization in the AWS account that purchased the RI and hosts the remaining active EC2 instances. Invite the other AWS accounts to join this organization from the management account.**
- From the AWS Organizations management account, utilize AWS Resource Access Manager (AWS RAM) to share the Reserved Instance with other accounts.

**A:** **Enable Reserved Instance sharing in the billing preferences for the account that purchased the RI** and **Establish an AWS Organization from the account that purchased the RI and invite the other accounts.**

**Explanation:**

Reserved Instance benefits are shared across accounts in the same AWS Organization when RI sharing is enabled. The organization must be established from the account that purchased the RI (making it the management account), and RI sharing must be enabled in that account's billing preferences.

- **CORRECT:** "Enable Reserved Instance sharing in the billing preferences section of the AWS Management Console for the account that purchased the existing RI" is a correct answer.
- **CORRECT:** "Establish an AWS Organization in the AWS account that purchased the RI and hosts the remaining active EC2 instances. Invite the other AWS accounts to join this organization" is a correct answer.
- **INCORRECT:** "From the AWS Organizations management account, utilize AWS Resource Access Manager (AWS RAM) to share the Reserved Instance..." is incorrect — AWS RAM does not support Reserved Instance sharing; it is used for sharing resources like subnets and Transit Gateways.
- **INCORRECT:** "Enable Reserved Instance sharing... for the management account" is incorrect — RI sharing must be enabled in the account that purchased the RI, not in a separate management account.
- **INCORRECT:** "Use AWS Organizations to establish a new payer account..." is incorrect — creating a new payer account is unnecessary; the existing account that purchased the RI should become the management account.

**References:**
- https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/billing-what-is.html
- https://digitalcloud.training/aws-organizations/

---

### Question 34 (c)

**Q:** A data analytics company is hosting a data lake which consists of data in Amazon S3 and Amazon RDS for PostgreSQL. The company needs a reporting solution that provides data visualization for the latest data. The solution must allow management to view dashboards and control access at the user and group level. Which solution will meet these requirements?

**Options:**

- **✅ Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate users and groups.**
- Create an AWS Glue table and crawler for the data in Amazon S3. Use Amazon Athena Federated Query to access data within Amazon RDS for PostgreSQL. Generate reports by using Amazon Athena. Publish the reports to Amazon S3. Use S3 bucket policies to control access.
- Create an AWS Glue table and crawler for the data in Amazon S3. Create an AWS Glue extract, transform, and load (ETL) job to produce reports. Publish the reports to Amazon S3. Use S3 bucket policies to control access.
- Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate IAM roles.

**A:** **Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate users and groups.**

**Explanation:**

Amazon QuickSight is purpose-built for data visualization and business intelligence dashboards. It natively connects to both Amazon S3 and Amazon RDS for PostgreSQL. QuickSight supports sharing dashboards at the user and group level, providing the fine-grained access control required for management visibility.

- **CORRECT:** "Create an analysis in Amazon QuickSight... Share the dashboards with the appropriate users and groups" is the correct answer.
- **INCORRECT:** "Create an AWS Glue table and crawler... Use Amazon Athena Federated Query... Generate reports by using Amazon Athena. Publish the reports to Amazon S3..." is incorrect — Athena lacks data visualization capabilities and S3-based reports do not provide an interactive dashboard experience.
- **INCORRECT:** "Create an AWS Glue table and crawler... Create an AWS Glue ETL job to produce reports. Publish the reports to Amazon S3..." is incorrect — Glue ETL jobs are for data transformation, not visualization; this approach lacks interactive dashboard functionality.
- **INCORRECT:** "Create an analysis in Amazon QuickSight... Share the dashboards with the appropriate IAM roles" is incorrect — QuickSight sharing is done at the user and group level within QuickSight, not via IAM roles.

**References:**
- https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html
- https://digitalcloud.training/aws-glue/
- https://digitalcloud.training/amazon-athena/

---

### Question 35 (c)

**Q:** A finance organization has bootstrapped a golden image for their in-house application and the resultant AMI is to be shared across various AWS accounts as a base image. The organization wants to be notified whenever a new AMI is created so that they can perform security checks. Which solution will meet these requirements with the LEAST operational overhead?

**Options:**

- Configure AWS CloudTrail with an Amazon SNS notification that occurs when updated logs are sent to Amazon S3. Use Amazon Athena to create a new table and to query on CreateImage when an API call is detected.
- Configure an Amazon SQS FIFO queue as a target for AWS CloudTrail logs. Create an AWS Lambda function to send an alert to an Amazon SNS topic when a CreateImage API call is detected.
- Create an AWS Lambda function to query AWS CloudTrail logs and to send an alert when a CreateImage API call is detected.
- **✅ Create an Amazon EventBridge rule for the CreateImage API call. Configure the target as an Amazon SNS topic to send an alert when a CreateImage API call is detected.**

**A:** **Create an Amazon EventBridge rule for the CreateImage API call. Configure the target as an Amazon SNS topic to send an alert when a CreateImage API call is detected.**

**Explanation:**

Amazon EventBridge can trigger rules based on API calls captured by AWS CloudTrail. By creating an EventBridge rule that matches the `CreateImage` API call and targeting an SNS topic, the organization receives instant notifications with no custom code or infrastructure to manage — the lowest operational overhead solution.

- **CORRECT:** "Create an Amazon EventBridge rule for the CreateImage API call. Configure the target as an Amazon SNS topic..." is the correct answer.
- **INCORRECT:** "Configure AWS CloudTrail with an Amazon SNS notification... Use Amazon Athena to create a new table and to query on CreateImage..." is incorrect — Athena is a query analysis tool and requires manual querying; it does not provide real-time notifications.
- **INCORRECT:** "Create an AWS Lambda function to query AWS CloudTrail logs and to send an alert..." is incorrect — writing and maintaining custom Lambda code adds operational overhead compared to using native EventBridge rules.
- **INCORRECT:** "Configure an Amazon SQS FIFO queue as a target for AWS CloudTrail logs. Create an AWS Lambda function to send an alert..." is incorrect — CloudTrail logs cannot be sent directly to an SQS queue; this approach also requires custom Lambda code.

**References:**
- https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-log-api-call.html

---

### Question 39

**Q:** A traffic law enforcement company is building a solution that has thousands of edge devices that collectively generate 1 TB of status alerts each day. The company wants a highly available solution that minimizes costs, does not require managing additional infrastructure, and retains 14 days of data. What is the MOST operationally efficient solution that meets these requirements?

**Options:**

- Launch Amazon EC2 instances across two Availability Zones and place them behind an Elastic Load Balancer to ingest the alerts. Create a script on the EC2 instances that will store the alerts in an Amazon S3 bucket. Set up an S3 Lifecycle configuration.
- Create an Amazon Simple Queue Service (Amazon SQS) standard queue to ingest the alerts and set the message retention period to 14 days. Configure consumers to poll the SQS queue, check the age of the messages, and process the data.
- **✅ Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the Kinesis Data Firehose stream to deliver the alerts to an Amazon S3 bucket. Set up an S3 Lifecycle configuration to delete objects after 14 days.**
- Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the Kinesis Data Firehose stream to deliver the alerts to an Amazon OpenSearch Service cluster. Set up an index lifecycle policy to delete indexes after 14 days.

**A:** **Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the Kinesis Data Firehose stream to deliver the alerts to an Amazon S3 bucket. Set up an S3 Lifecycle configuration to delete objects after 14 days.**

**Explanation:**

Kinesis Data Firehose is a fully managed, serverless data ingestion service that scales automatically and requires no infrastructure management. It loads data directly to S3 without requiring consumers. An S3 Lifecycle policy automatically deletes objects after 14 days, meeting the retention requirement with the least operational overhead.

- **CORRECT:** "Create an Amazon Kinesis Data Firehose delivery stream... deliver the alerts to an Amazon S3 bucket. Set up an S3 Lifecycle configuration to delete objects after 14 days" is the correct answer.
- **INCORRECT:** "Launch Amazon EC2 instances... create a script on the EC2 instances..." is incorrect — managing EC2 instances and custom scripts adds significant operational overhead.
- **INCORRECT:** "Create an Amazon Kinesis Data Firehose delivery stream... deliver the alerts to an Amazon OpenSearch Service cluster..." is incorrect — OpenSearch Service requires provisioning and managing a cluster, adding infrastructure overhead and cost.
- **INCORRECT:** "Create an Amazon Simple Queue Service (Amazon SQS) standard queue..." is incorrect — SQS requires consumer applications to retrieve and process messages; this means additional infrastructure to manage. With Kinesis Data Firehose, data is loaded directly to S3 without consumer applications.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- https://aws.amazon.com/kinesis/data-firehose/features/
- https://digitalcloud.training/amazon-kinesis/

---

### Question 53

**Q:** An application uses Amazon EC2 instances and an Amazon RDS MySQL database. The database is not currently encrypted. A solutions architect needs to apply encryption to the database for all new and existing data. How should this be accomplished?

**Options:**

- Create an RDS read replica with encryption at rest enabled. Promote the read replica to master and switch the application over to the new master. Delete the old RDS instance.
- Create an Amazon ElastiCache cluster and encrypt data using the cache nodes.
- Enable encryption for the database using the API. Take a full snapshot of the database. Delete old snapshots.
- **✅ Take a snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot.**

**A:** **Take a snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot.**

**Explanation:**

You cannot modify an existing unencrypted RDS DB instance to make it encrypted, and you cannot create an encrypted read replica from an unencrypted source. The only supported method is to take a snapshot of the unencrypted database, create an encrypted copy of that snapshot, and then restore a new RDS instance from the encrypted snapshot.

- **CORRECT:** "Take a snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot" is the correct answer.
- **INCORRECT:** "Create an Amazon ElastiCache cluster and encrypt data using the cache nodes" is incorrect — you cannot encrypt an RDS database using an ElastiCache cache node.
- **INCORRECT:** "Enable encryption for the database using the API. Take a full snapshot of the database. Delete old snapshots" is incorrect — you cannot enable encryption for an existing, unencrypted RDS database instance via the API.
- **INCORRECT:** "Create an RDS read replica with encryption at rest enabled. Promote the read replica to master..." is incorrect — you cannot create an encrypted read replica from an unencrypted source RDS instance.

**References:**
- https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- https://aws.amazon.com/premiumsupport/knowledge-center/rds-encrypt-instance-mysql-mariadb/
- https://digitalcloud.training/amazon-rds/

---

### Question 54 (c)

**Q:** A Solutions Architect is designing a migration strategy for a company moving to the AWS Cloud. The company uses a shared Microsoft filesystem that uses Distributed File System Namespaces (DFSN). What would be the most suitable migration strategy?

**Options:**

- Use the AWS Server Migration Service to migrate to an Amazon S3 bucket.
- **✅ Use AWS DataSync to migrate to Amazon FSx for Windows File Server.**
- Use AWS DataSync to migrate to an Amazon EFS filesystem.
- Use the AWS Server Migration Service to migrate to Amazon FSx for Lustre.

**A:** **Use AWS DataSync to migrate to Amazon FSx for Windows File Server.**

**Explanation:**

Amazon FSx for Windows File Server supports Distributed File System Namespaces (DFSN) and is the most suitable destination for Microsoft filesystems. AWS DataSync is the recommended tool for migrating data to FSx, supporting fast, automated, and scheduled data transfers.

- **CORRECT:** "Use AWS DataSync to migrate to Amazon FSx for Windows File Server" is the correct answer.
- **INCORRECT:** "Use the AWS Server Migration Service to migrate to Amazon FSx for Lustre" is incorrect — AWS SMS migrates virtual machines, not filesystems; FSx for Lustre also does not support Windows DFSN.
- **INCORRECT:** "Use AWS DataSync to migrate to an Amazon EFS filesystem" is incorrect — EFS is a Linux NFS filesystem and cannot be the destination for a Windows DFSN-based filesystem.
- **INCORRECT:** "Use the AWS Server Migration Service to migrate to an Amazon S3 bucket" is incorrect — AWS SMS migrates virtual machines to EC2; S3 is object-based storage and not a suitable replacement for a Windows file server.

**References:**
- https://aws.amazon.com/blogs/storage/migrate-to-amazon-fsx-for-windows-file-server-using-aws-datasync/
- https://docs.aws.amazon.com/fsx/latest/WindowsGuide/migrate-files-fsx.html
- https://digitalcloud.training/amazon-fsx/

---

### Question 64 (b)

**Q:** An online education platform uses Amazon CloudFront to distribute learning resources globally. The company wants to ensure that only enrolled students have access to the course materials. These materials span multiple files and directories. Which solution will meet these requirements?

**Options:**

- Create and provide S3 pre-signed URLs to authenticated students.
- Implement CloudFront Field-Level Encryption to block access to non-enrolled students.
- Utilize Amazon S3 object-level encryption for course materials.
- **✅ Implement CloudFront signed cookies for authenticated students.**

**A:** **Implement CloudFront signed cookies for authenticated students.**

**Explanation:**

CloudFront signed cookies allow you to control access to multiple restricted files without changing the URLs. When a student authenticates and is verified as enrolled, the application sets a signed cookie in the student's browser. All subsequent CloudFront requests include this cookie, granting access to the course materials across multiple files and directories.

- **CORRECT:** "Implement CloudFront signed cookies for authenticated students" is the correct answer.
- **INCORRECT:** "Create and provide S3 pre-signed URLs to authenticated students" is incorrect — S3 pre-signed URLs grant temporary access to a single S3 object and are inefficient when access to multiple files or directories is required.
- **INCORRECT:** "Utilize Amazon S3 object-level encryption for course materials" is incorrect — S3 encryption protects data at rest and does not control who can access the content.
- **INCORRECT:** "Implement CloudFront Field-Level Encryption to block access to non-enrolled students" is incorrect — CloudFront Field-Level Encryption is designed to protect sensitive data in HTTP POST requests (e.g., form submissions), not to control access to content.

**References:**
- https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-cookies.html
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 16

**Q:** A web application is running on a fleet of Amazon EC2 instances using an Auto Scaling Group. It is desired that the CPU usage in the fleet is kept at 40%. How should scaling be configured?

**Options:**

- Use a simple scaling policy that launches instances when the average CPU hits 40%.
- Use a step scaling policy that uses the PercentChangeInCapacity value to adjust the group size as required.
- **✅ Use a target tracking policy that keeps the average aggregate CPU utilization at 40%.**
- Use a custom CloudWatch alarm to monitor CPU usage and notify the ASG using Amazon SNS.

**A:** **Use a target tracking policy that keeps the average aggregate CPU utilization at 40%.**

**Explanation:**

Target tracking scaling policies are designed exactly for this use case. You define a target value for a metric (e.g., 40% CPU utilization), and Auto Scaling automatically adds or removes instances to keep the metric at or near the target. It is the simplest and most accurate way to maintain a specific CPU utilization.

- **CORRECT:** "Use a target tracking policy that keeps the average aggregate CPU utilization at 40%" is the correct answer.
- **INCORRECT:** "Use a simple scaling policy that launches instances when the average CPU hits 40%" is incorrect — a simple scaling policy triggers a fixed scaling action when an alarm threshold is breached but does not continuously track the metric to maintain a target value.
- **INCORRECT:** "Use a step scaling policy that uses the PercentChangeInCapacity value..." is incorrect — step scaling adjustments are based on the magnitude of the alarm breach, not on maintaining a specific target metric value.
- **INCORRECT:** "Use a custom CloudWatch alarm to monitor CPU usage and notify the ASG using Amazon SNS" is incorrect — you do not need a custom alarm; the ASG can scale automatically using native target tracking scaling without SNS notification.

**References:**
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html
- https://digitalcloud.training/amazon-ec2-auto-scaling/
