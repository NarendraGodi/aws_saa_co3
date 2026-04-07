Question 1Skipped
Domain
AWS Database
Question 14Skipped
A global manufacturing company uses AWS Outposts servers to manage IoT workloads in its factories across multiple continents. The company regularly updates factory IoT software, consisting of 50 files, from a central Amazon S3 bucket in the us-east-1 Region. Factories report significant delays when downloading and applying the updates, causing downtime. The company needs to minimize the latency for distributing software updates globally while reducing operational overhead.
Which solution will meet this requirement with the LEAST operational overhead?
Create Amazon S3 buckets in multiple Regions. Configure S3 Cross-Region Replication (CRR) between the buckets. Deploy updates from the nearest bucket to each factory location.
Create an Amazon S3 bucket in the us-east-1 Region. Deploy AWS Outposts servers at the factories as S3 endpoints. Configure the servers to cache the updates locally.
Correct answer
Create an Amazon S3 bucket in the us-east-1 Region. Set up an Amazon CloudFront distribution with the S3 bucket as the origin. Use signed URLs to download the software updates.
Create an Amazon S3 bucket in the us-east-1 Region. Configure Amazon S3 Transfer Acceleration for the bucket. Use the S3 Transfer Acceleration endpoint for faster downloads.
Overall explanation
Create an Amazon S3 bucket in the us-east-1 Region. Set up an Amazon CloudFront distribution with the S3 bucket as the origin. Use signed URLs to download the software updates: This is correct because CloudFront caches the software updates at edge locations around the world, significantly reducing latency. Signed URLs ensure secure access, and the solution requires minimal operational overhead. Create an Amazon S3 bucket in the us-east-1 Region. Configure Amazon S3 Transfer Acceleration for the bucket. Use the S3 Transfer Acceleration endpoint for faster downloads: This is incorrect because Transfer Acceleration optimizes file transfers only when data is uploaded or downloaded from a single bucket, which may not provide consistent latency improvements for global locations. Create an Amazon S3 bucket in the us-east-1 Region. Deploy AWS Outposts servers at the factories as S3 endpoints. Configure the servers to cache the updates locally: This is incorrect because configuring Outposts servers as S3 endpoints increases operational complexity and cost. CloudFront is a simpler and more efficient solution for this use case. Create Amazon S3 buckets in multiple Regions. Configure S3 Cross-Region Replication (CRR) between the buckets. Deploy updates from the nearest bucket to each factory location: This is incorrect because managing multiple buckets and configuring CRR requires additional effort and increases complexity compared to using a single bucket with CloudFront.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Database
Question 16Skipped
A fintech company is modernizing its payments processing system to adopt a serverless microservices architecture. The company wants to decouple its services and implement an event-driven architecture to support a publish/subscribe (pub/sub) model. The system needs to notify multiple downstream services when payment events occur, ensuring scalability and low operational overhead.
Which solution will meet these requirements MOST cost-effectively?
Use Amazon MQ as a message broker to enable publish/subscribe communication between the payment microservices and the downstream services.
Use Amazon Kinesis Data Firehose to deliver payment events to multiple S3 buckets. Configure downstream services to poll the buckets for event processing.
Configure an Amazon EventBridge rule to capture payment events and route them to multiple AWS Lambda functions that handle downstream processing.
Correct answer
Configure an Amazon SNS topic to receive payment events from an AWS Lambda function. Set up multiple subscribers, such as Lambda functions, to process the events.
Overall explanation
Configure an Amazon SNS topic to receive payment events from an AWS Lambda function. Set up multiple subscribers, such as Lambda functions, to process the events: This is correct because SNS is a fully managed pub/sub messaging service that supports high-throughput, scalable delivery to multiple subscribers, which aligns with the company's requirements.
Configure an Amazon EventBridge rule to capture payment events and route them to multiple AWS Lambda functions that handle downstream processing: This is incorrect because EventBridge is more suited for complex event routing scenarios and not optimized for simple pub/sub use cases compared to SNS.
Use Amazon Kinesis Data Firehose to deliver payment events to multiple S3 buckets. Configure downstream services to poll the buckets for event processing: This is incorrect because Kinesis Data Firehose is designed for streaming data delivery, not for pub/sub messaging. It adds unnecessary overhead for the described use case.
Use Amazon MQ as a message broker to enable publish/subscribe communication between the payment microservices and the downstream services: This is incorrect because Amazon MQ is a managed message broker service that is typically used for legacy applications requiring protocols such as JMS or AMQP. It adds more operational complexity compared to SNS.
References:
https://docs.aws.amazon.com/sns/latest/dg/welcome.html
https://docs.aws.amazon.com/eventbridge/latest/userguide/what-is-amazon-eventbridge.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Database
Question 25Skipped
A video production company is planning to move some of its workloads to the AWS Cloud. The company will require around 5 TB of storage for video processing with the maximum possible I/O performance. They also require over 400 TB of extremely durable storage for storing video files and 800 TB of storage for long-term archival.
Which combinations of services should a Solutions Architect use to meet these requirements?
Amazon EBS for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage.
Amazon EBS for maximum performance, Amazon EFS for durable data storage, and Amazon S3 Glacier for archival storage.
Amazon EC2 instance store for maximum performance, Amazon EFS for durable data storage, and Amazon S3 for archival storage.
Correct answer
Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage.
Overall explanation
The best I/O performance can be achieved by using instance store volumes for the video processing. This is safe to use for use cases where the data can be recreated from the source files so this is a good use case.
For storing data durably Amazon S3 is a good fit as it provides 99.999999999% of durability. For archival the video files can then be moved to Amazon S3 Glacier which is a low cost storage option that is ideal for long-term archival.
CORRECT: "Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage" is the correct answer.
INCORRECT: "Amazon EBS for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage" is incorrect. EBS is not going to provide as much I/O performance as an instance store volume so is not the best choice for this use case.
INCORRECT: "Amazon EC2 instance store for maximum performance, Amazon EFS for durable data storage, and Amazon S3 for archival storage" is incorrect. EFS does not provide as much durability as Amazon S3 and will not be as cost-effective.
INCORRECT: "Amazon EBS for maximum performance, Amazon EFS for durable data storage, and Amazon S3 Glacier for archival storage" is incorrect. EBS and EFS are not the best choices here as described above.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
https://aws.amazon.com/s3/storage-classes/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Database
Question 30Skipped
A company is working with a strategic partner that has an application that must be able to send messages to one of the company’s Amazon SQS queues. The partner company has its own AWS account.
How can a Solutions Architect provide least privilege access to the partner?
Update the permission policy on the SQS queue to grant all permissions to the partner’s AWS account.
Create a user account and grant the sqs:SendMessage permission for Amazon SQS. Share the credentials with the partner company.
Correct answer
Update the permission policy on the SQS queue to grant the sqs:SendMessage permission to the partner’s AWS account.
Create a cross-account role with access to all SQS queues and use the partner's AWS account in the trust document for the role.
Overall explanation
Amazon SQS supports resource-based policies. The best way to grant the permissions using the principle of least privilege is to use a resource-based policy attached to the SQS queue that grants the partner company’s AWS account the sqs:SendMessage privilege.
The following policy is an example of how this could be configured:


CORRECT: "Update the permission policy on the SQS queue to grant the sqs:SendMessage permission to the partner’s AWS account" is the correct answer.
INCORRECT: "Create a user account that and grant the sqs:SendMessage permission for Amazon SQS. Share the credentials with the partner company" is incorrect. This would provide the permissions for all SQS queues, not just the queue the partner company should be able to access.
INCORRECT: "Create a cross-account role with access to all SQS queues and use the partner's AWS account in the trust document for the role" is incorrect. This would provide access to all SQS queues and the partner company should only be able to access one SQS queue.
INCORRECT: "Update the permission policy on the SQS queue to grant all permissions to the partner’s AWS account" is incorrect. This provides too many permissions; the partner company only needs to send messages to the queue.
References:
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-basic-examples-of-sqs-policies.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Database
Question 34Skipped
A company runs an application that uses an Amazon RDS PostgreSQL database. The database is currently not encrypted. A Solutions Architect has been instructed that due to new compliance requirements all existing and new data in the database must be encrypted. The database experiences high volumes of changes and no data can be lost.
How can the Solutions Architect enable encryption for the database without incurring any data loss?
Create a snapshot of the existing RDS DB instance. Create an encrypted copy of the snapshot. Create a new RDS DB instance from the encrypted snapshot. Configure the application to use the new DB endpoint.
Create an RDS read replica and specify an encryption key. Promote the encrypted read replica to primary. Update the application to point to the new RDS DB endpoint.
Update the RDS DB to Multi-AZ mode and enable encryption for the standby replica. Perform a failover to the standby instance and then delete the unencrypted RDS DB instance.
Correct answer
Create a snapshot of the existing RDS DB instance. Create an encrypted copy of the snapshot. Create a new RDS DB instance from the encrypted snapshot and update the application. Use AWS DMS to synchronize data between the source and destination RDS DBs.
Overall explanation
You cannot change the encryption status of an existing RDS DB instance. Encryption must be specified when creating the RDS DB instance. The best way to encrypt an existing database is to take a snapshot, encrypt a copy of the snapshot and restore the snapshot to a new RDS DB instance. This results in an encrypted database that is a new instance. Applications must be updated to use the new RDS DB endpoint.
In this scenario as there is a high rate of change, the databases will be out of sync by the time the new copy is created and is functional. The best way to capture the changes between the source (unencrypted) and destination (encrypted) DB is to use AWS Database Migration Service (DMS) to synchronize the data.
The slide below depicts the process for encrypting an unencrypted RDS DB instance:


CORRECT: "Create a snapshot of the existing RDS DB instance. Create an encrypted copy of the snapshot. Create a new RDS DB instance from the encrypted snapshot and update the application. Use AWS DMS to synchronize data between the source and destination RDS DBs" is the correct answer.
INCORRECT: "Create a snapshot of the existing RDS DB instance. Create an encrypted copy of the snapshot. Create a new RDS DB instance from the encrypted snapshot. Configure the application to use the new DB endpoint" is incorrect. This answer creates an encrypted DB instance but does not synchronize the data.
INCORRECT: "Create an RDS read replica and specify an encryption key. Promote the encrypted read replica to primary. Update the application to point to the new RDS DB endpoint" is incorrect. You cannot create an encrypted read replica of an unencrypted RDS DB. The read replica will always have the same encryption status as the RDS DB it is created from.
INCORRECT: "Update the RDS DB to Multi-AZ mode and enable encryption for the standby replica. Perform a failover to the standby instance and then delete the unencrypted RDS DB instance" is incorrect. You also cannot have an encrypted Multi-AZ standby instance of an unencrypted RDS DB.
References:
https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/encrypt-an-existing-amazon-rds-for-postgresql-db-instance.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Database
Question 35Skipped
A global logistics company hosts its shipment tracking system in the eu-west-1 Region. The system runs on Amazon EC2 instances, and customers access the shipment tracking API to retrieve real-time updates about their packages. Customers from Asia and South America report slower API response times compared to customers in Europe.
The company wants to improve API response times for international customers in a cost-effective manner.
Which solution will meet these requirements MOST cost-effectively?
Deploy Amazon CloudFront in front of the API. Configure the API response to be cached and use the CachingOptimized managed policy to improve efficiency and reduce latency for frequently requested data.
Deploy EC2 instances hosting the API in Asia and South America. Use an Application Load Balancer to distribute traffic across all Regions based on the geolocation of customer requests.
Correct answer
Use AWS Global Accelerator to route traffic through the closest AWS edge location to customers. Configure endpoint groups for the shipment tracking API to distribute traffic globally and reduce response times.
Establish an AWS Direct Connect connection with a public virtual interface (VIF) from each international customer's data center to the eu-west-1 Region. Route API requests over the Direct Connect connection to the shipment tracking system.
Overall explanation
Use AWS Global Accelerator to route traffic through the closest AWS edge location to customers. Configure endpoint groups for the shipment tracking API to distribute traffic globally and reduce response times: This is correct because Global Accelerator uses AWS’s global network to reduce latency by routing traffic through the nearest edge location to the customer. It ensures cost-effective performance improvement for customers in Asia and South America without requiring infrastructure duplication in multiple Regions.
Establish an AWS Direct Connect connection with a public virtual interface (VIF) from each international customer's data center to the eu-west-1 Region. Route API requests over the Direct Connect connection to the shipment tracking system: This is incorrect because Direct Connect requires significant investment in physical infrastructure and is more suitable for consistent, high-bandwidth traffic rather than improving API latency for multiple international customers.
Deploy Amazon CloudFront in front of the API. Configure the API response to be cached and use the CachingOptimized managed policy to improve efficiency and reduce latency for frequently requested data: This is incorrect because CloudFront is ideal for caching static or frequently accessed content. For real-time APIs where caching is not effective, CloudFront would not address latency issues for international users.
Deploy EC2 instances hosting the API in Asia and South America. Use an Application Load Balancer to distribute traffic across all Regions based on the geolocation of customer requests: This is incorrect because deploying additional EC2 instances in multiple Regions increases operational costs and complexity. Global Accelerator is a more cost-effective solution that avoids duplicating infrastructure.
References:
https://docs.aws.amazon.com/global-accelerator/latest/dg/introduction.html
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-managed-cache-policies.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-global-accelerator/
Domain
AWS Database
Question 54Skipped
A healthcare organization operates multiple applications on virtual machines (VMs) in its on-premises data center. Due to increasing demand for its services, the data center can no longer scale quickly enough to meet business needs. The organization has decided to migrate its non-critical workloads to AWS using a lift-and-shift strategy to expedite the process.
Which combination of steps will meet these requirements? (Select THREE.)
Correct selection
Stop all operations on the VMs. Perform a cutover by launching the migrated instances in AWS.
Correct selection
Use AWS Application Migration Service to replicate the VMs to AWS. Install the AWS Replication Agent on each VM.
Install the AWS Systems Manager Agent on the VMs to streamline operational management during migration.
Use AWS App Runner to containerize the workloads before migrating them to AWS.
Use AWS Server Migration Service (AWS SMS) to automate the migration of VMs to Amazon EC2 instances.
Correct selection
Complete the initial data replication from the VMs to AWS. Launch test instances to perform acceptance tests for the workloads.
Overall explanation
Use AWS Application Migration Service to replicate the VMs to AWS. Install the AWS Replication Agent on each VM: This is correct because AWS Application Migration Service enables lift-and-shift migrations by replicating VMs from the on-premises data center to AWS. Installing the Replication Agent is the first step to initiate data replication.
Complete the initial data replication from the VMs to AWS. Launch test instances to perform acceptance tests for the workloads: This is correct because testing the replicated workloads ensures the migrated VMs function as expected on AWS before the final cutover.
Stop all operations on the VMs. Perform a cutover by launching the migrated instances in AWS: This is correct because stopping operations ensures a clean cutover process, allowing the organization to launch the migrated instances in AWS with minimal disruption to business operations.
Use AWS Server Migration Service (AWS SMS) to automate the migration of VMs to Amazon EC2 instances: This is incorrect because AWS SMS has been deprecated in favor of AWS Application Migration Service, which provides a more streamlined and modern approach to lift-and-shift migrations.
Install the AWS Systems Manager Agent on the VMs to streamline operational management during migration: This is incorrect because while the Systems Manager Agent is useful for post-migration operations and management, it is not directly involved in the lift-and-shift migration process.
Use AWS App Runner to containerize the workloads before migrating them to AWS: This is incorrect because containerizing workloads introduces additional complexity and does not align with the lift-and-shift strategy described in the scenario.
References:
https://docs.aws.amazon.com/migrationhub/latest/ug/what-is-migrationhub.html
https://docs.aws.amazon.com/mgn/latest/ug/what-is-aws-mgn.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/
Domain
AWS Database
Question 63Skipped
A healthcare company is migrating its on-premises Oracle database to an Amazon RDS for Oracle database. The database must meet compliance requirements to retain backups for 120 days. Additionally, the company must have the ability to restore the database to any point in time within the past 10 days. The solution must minimize operational overhead and ensure compliance with these requirements.
Which solution will meet these requirements with the LEAST operational overhead?
Correct answer
Configure Amazon RDS automated backups. Set the retention period to 35 days and enable point-in-time recovery for the past 10 days. Use AWS Backup to retain additional backups for 120 days.
Use AWS Backup to create a backup plan for Amazon RDS with a 120-day retention period. Enable point-in-time recovery by combining AWS Backup and RDS automated backups.
Set up Amazon S3 Lifecycle policies to retain database exports for 120 days. Use AWS Database Migration Service (AWS DMS) to export the database to Amazon S3 every 24 hours.
Create an Amazon RDS manual snapshot every week. Use an AWS Lambda function to delete snapshots that are older than 120 days.
Overall explanation
Configure Amazon RDS automated backups. Set the retention period to 35 days and enable point-in-time recovery for the past 10 days. Use AWS Backup to retain additional backups for 120 days: This is correct because RDS automated backups support up to 35 days of retention and point-in-time recovery. AWS Backup can extend the retention period to 120 days without additional complexity.
Create an Amazon RDS manual snapshot every week. Use an AWS Lambda function to delete snapshots that are older than 120 days: This is incorrect because manual snapshot management introduces operational overhead and is not as scalable or reliable as RDS automated backups combined with AWS Backup.
Use AWS Backup to create a backup plan for Amazon RDS with a 120-day retention period. Enable point-in-time recovery by combining AWS Backup and RDS automated backups: This is incorrect because while AWS Backup can retain backups for 120 days, it cannot directly handle point-in-time recovery, which requires native RDS automated backups.
Set up Amazon S3 Lifecycle policies to retain database exports for 120 days. Use AWS Database Migration Service (AWS DMS) to export the database to Amazon S3 every 24 hours: This is incorrect because exporting the database to S3 introduces unnecessary operational complexity and does not support point-in-time recovery.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html
https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Database
Question 64Skipped
A genomics research organization is building an application to analyze large datasets. Raw genomic data is stored in an Amazon S3 bucket, processed by multiple Amazon EC2 instances, and the results are stored in a separate S3 bucket. The application frequently transfers large amounts of data between the EC2 instances during analysis. The organization wants to reduce overall data transfer costs while maintaining efficient data processing.
What should the solutions architect do to achieve this?
Use Amazon Elastic Fabric Adapter (EFA) to enable high-speed data transfer between EC2 instances, reducing transfer costs.
Use Amazon S3 Transfer Acceleration to optimize the transfer of data between the EC2 instances and the S3 buckets.
Correct answer
Deploy all the EC2 instances in the same Availability Zone to eliminate cross-AZ data transfer charges.
Configure an Auto Scaling group to launch the EC2 instances in multiple Regions to distribute the processing workload.
Overall explanation
Deploy all the EC2 instances in the same Availability Zone to eliminate cross-AZ data transfer charges: This is correct because data transfer between EC2 instances in the same AZ is free, while transferring data across AZs incurs additional charges. Keeping all instances in the same AZ minimizes data transfer costs while maintaining efficient processing.
Configure an Auto Scaling group to launch the EC2 instances in multiple Regions to distribute the processing workload: This is incorrect because distributing workloads across multiple Regions increases inter-region data transfer costs, which are higher than cross-AZ costs. This approach does not address the need to reduce data transfer costs.
Use Amazon Elastic Fabric Adapter (EFA) to enable high-speed data transfer between EC2 instances, reducing transfer costs: This is incorrect because EFAs optimize network performance for HPC (high-performance computing) workloads but do not reduce costs associated with cross-AZ or inter-AZ data transfer charges.
Use Amazon S3 Transfer Acceleration to optimize the transfer of data between the EC2 instances and the S3 buckets: This is incorrect because S3 Transfer Acceleration is designed to speed up data transfer over long distances to S3, such as from on-premises locations or remote clients. It does not reduce costs for transfers between EC2 instances.
References:
https://aws.amazon.com/ec2/pricing/on-demand/
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni-efa.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Database
Question 2Skipped
A healthcare company is building a patient records management application that uses a relational database to store user data and configuration details. The company expects steady growth in the number of patients. The database workload is expected to be variable and read-heavy, with occasional write operations. The company wants to cost-optimize the database solution while ensuring the necessary performance for its workload.
Which solution will meet these requirements MOST cost-effectively?
Deploy the database on Amazon RDS. Use magnetic storage with Multi-AZ deployments to ensure durability and handle the read-heavy workload.
Correct answer
Deploy the database on Amazon Aurora Serverless v2 to automatically scale the database capacity based on actual usage and handle fluctuations in workload.
Deploy the database on Amazon DynamoDB. Use on-demand capacity mode to automatically adjust throughput and accommodate workload changes.
Deploy the database on Amazon RDS. Use General Purpose SSD (gp3) storage with a read replica to ensure consistent performance for read and write operations.
Overall explanation
Deploy the database on Amazon Aurora Serverless v2 to automatically scale the database capacity based on actual usage and handle fluctuations in workload: This is correct because Aurora Serverless v2 is a cost-effective option that dynamically adjusts capacity to meet workload demands. It is particularly suited for variable workloads, offering the performance of Aurora with a pay-per-use pricing model.
Deploy the database on Amazon RDS. Use General Purpose SSD (gp3) storage with a read replica to ensure consistent performance for read and write operations: This is incorrect because while using a read replica can help with read-heavy workloads, it introduces additional costs and management overhead compared to Aurora Serverless v2.
Deploy the database on Amazon DynamoDB. Use on-demand capacity mode to automatically adjust throughput and accommodate workload changes: This is incorrect because DynamoDB is a NoSQL database that is not designed for relational database requirements. While it is highly scalable, it does not meet the company's need for a relational database solution.
Deploy the database on Amazon RDS. Use magnetic storage with Multi-AZ deployments to ensure durability and handle the read-heavy workload: This is incorrect because magnetic storage is outdated, has limited performance, and is not cost-effective for a read-heavy workload.
References:
https://docs.aws.amazon.com/rds/index.html
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Database
Question 3Skipped
A website runs on a Microsoft Windows server in an on-premises data center. The web server is being migrated to Amazon EC2 Windows instances in multiple Availability Zones on AWS. The web server currently uses data stored in an on-premises network-attached storage (NAS) device.
Which replacement to the NAS file share is MOST resilient and durable?
Correct answer
Migrate the file share to Amazon FSx for Windows File Server
Migrate the file share to AWS Storage Gateway
Migrate the file share to Amazon EBS
Migrate the file share to Amazon Elastic File System (Amazon EFS)
Overall explanation
Amazon FSx for Windows File Server provides fully managed, highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol. It is built on Windows Server, delivering a wide range of administrative features such as user quotas, end-user file restore, and Microsoft Active Directory (AD) integration. It offers single-AZ and multi-AZ deployment options, fully managed backups, and encryption of data at rest and in transit.


This is the only solution presented that provides resilient storage for Windows instances.
CORRECT: "Migrate the file share to Amazon FSx for Windows File Server" is the correct answer.
INCORRECT: "Migrate the file share to Amazon Elastic File System (Amazon EFS)" is incorrect as you cannot use Windows instances with Amazon EFS.
INCORRECT: "Migrate the file share to Amazon EBS" is incorrect as this is not a shared storage solution for multi-AZ deployments.
INCORRECT: "Migrate the file share to AWS Storage Gateway" is incorrect as with Storage Gateway replicated files end up on Amazon S3. The replacement storage solution should be a file share, not an object-based storage system.
References:
https://aws.amazon.com/fsx/windows/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Database
Question 18Skipped
A web application is being deployed on an Amazon ECS cluster using the Fargate launch type. The application is expected to receive a large volume of traffic initially. The company wishes to ensure that performance is good for the launch and that costs reduce as demand decreases
What should a solutions architect recommend?
Correct answer
Use Amazon ECS Service Auto Scaling with target tracking policies to scale when an Amazon CloudWatch alarm is breached.
Use Amazon EC2 Auto Scaling with simple scaling policies to scale when an Amazon CloudWatch alarm is breached.
Use Amazon EC2 Auto Scaling to scale out on a schedule and back in once the load decreases.
Use an AWS Lambda function to scale Amazon ECS based on metric breaches that trigger an Amazon CloudWatch alarm.
Overall explanation
Amazon ECS uses the AWS Application Auto Scaling service to scales tasks. This is configured through Amazon ECS using Amazon ECS Service Auto Scaling.
A Target Tracking Scaling policy increases or decreases the number of tasks that your service runs based on a target value for a specific metric. For example, in the image below the tasks will be scaled when the average CPU breaches 80% (as reported by CloudWatch):


CORRECT: "Use Amazon ECS Service Auto Scaling with target tracking policies to scale when an Amazon CloudWatch alarm is breached" is the correct answer.
INCORRECT: "Use Amazon EC2 Auto Scaling with simple scaling policies to scale when an Amazon CloudWatch alarm is breached" is incorrect
INCORRECT: "Use Amazon EC2 Auto Scaling to scale out on a schedule and back in once the load decreases" is incorrect
INCORRECT: "Use an AWS Lambda function to scale Amazon ECS based on metric breaches that trigger an Amazon CloudWatch alarm" is incorrect
References:
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-auto-scaling.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Database
Question 31Skipped
A gaming company uses a web application to display scores. An Application Load Balancer is used to distribute load across Amazon EC2 instances which run the application. The application stores data in an Amazon RDS for MySQL database. Users are experiencing long delays and interruptions due to poor database read performance. It is important for the company to improve the user experience while minimizing changes to the application's architecture.
What should a solutions architect do to meet these requirements?
Connect the database and the application layer using RDS Proxy.
Use AWS Lambda instead of Amazon EC2 for the compute layer.
Use an Amazon DynamoDB table instead of RDS.
Correct answer
Use Amazon ElastiCache to cache the database layer.
Overall explanation
Amazon ElastiCache is a fully managed, in-memory caching service supporting flexible, real-time use cases. You can use ElastiCache for caching, which accelerates application and database performance, or as a primary data store for use cases that don't require durability like session stores, gaming leaderboards, streaming, and analytics. ElastiCache is compatible with Redis and Memcached.

As the issues in this instance are caused by poor read performance, a caching solution would offload reads from the primary database instance and allow the application to perform better.
CORRECT: "Use Amazon ElastiCache to cache the database layer” is the correct answer (as explained above.)
INCORRECT: "Connect the database and the application layer using RDS Proxy” is incorrect. RDS proxy allows applications to pool and share connections established with the database, improving database efficiency and application scalability. It does not however specifically improve read performance like a caching layer would.
INCORRECT: "Use AWS Lambda instead of Amazon EC2 for the compute layer" is incorrect. AWS Lambda would not be a suitable use case for hosting leaderboards, as the maximum timeout is 15 minutes, and the issue lies with the database layer, not the compute later.
INCORRECT: "Use an Amazon DynamoDB table instead of RDS" is incorrect. Migrating to DynamoDB would not help the load of reads on the database and changing the schema of the database would cause massive changes to the application’s architecture.
References:
https://aws.amazon.com/elasticache/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-elasticache/
Domain
AWS Database
Question 32Skipped
A group of business analysts perform read-only SQL queries on an Amazon RDS database. The queries have become quite numerous and the database has experienced some performance degradation. The queries must be run against the latest data. A Solutions Architect must solve the performance problems with minimal changes to the existing web application.
What should the Solutions Architect recommend?
Load the data into Amazon ElastiCache and instruct the business analysts to run their queries against the ElastiCache endpoint.
Export the data to Amazon S3 and instruct the business analysts to run their queries using Amazon Athena.
Correct answer
Create a read replica of the primary database and instruct the business analysts to direct queries to the replica.
Load the data into an Amazon Redshift cluster and instruct the business analysts to run their queries against the cluster.
Overall explanation
The performance issues can be easily resolved by offloading the SQL queries the business analysts are performing to a read replica. This ensures that data that is being queries is up to date and the existing web application does not require any modifications to take place.
CORRECT: "Create a read replica of the primary database and instruct the business analysts to direct queries to the replica" is the correct answer.
INCORRECT: "Export the data to Amazon S3 and instruct the business analysts to run their queries using Amazon Athena" is incorrect. The data must be the latest data and this method would therefore require constant exporting of the data.
INCORRECT: "Load the data into an Amazon Redshift cluster and instruct the business analysts to run their queries against the cluster" is incorrect. This is another solution that requires exporting the loading the data which means over time it will become out of date.
INCORRECT: "Load the data into Amazon ElastiCache and instruct the business analysts to run their queries against the ElastiCache endpoint" is incorrect. It will be much easier to create a read replica. ElastiCache requires updates to the application code so should be avoided in this example.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Database
Question 33Skipped
A retail company uses an Amazon Aurora MySQL DB cluster for its order management system. The cluster includes eight Aurora Replicas. The company wants to ensure that reporting queries from its analytics team are automatically distributed across three specific Aurora Replicas that have higher compute and memory capacity than the rest of the cluster.
Which solution will meet these requirements?
Correct answer
Create and use a custom endpoint that targets the three high-capacity replicas.
Use the reader endpoint to automatically distribute reporting queries across all replicas in the cluster.
Direct reporting queries to the instance endpoints of the three high-capacity replicas.
Create a cluster clone for the reporting workload and use the writer endpoint of the cloned cluster.
Overall explanation
Create and use a custom endpoint that targets the three high-capacity replicas: This is correct because Aurora custom endpoints allow you to define a subset of replicas for specific workloads. By creating a custom endpoint, the reporting queries can be automatically distributed across the three high-capacity replicas without involving the rest of the cluster.
Use the reader endpoint to automatically distribute reporting queries across all replicas in the cluster: This is incorrect because the reader endpoint distributes queries across all Aurora Replicas in the cluster, which does not restrict queries to the desired three replicas.
Create a cluster clone for the reporting workload and use the writer endpoint of the cloned cluster: This is incorrect because creating a cluster clone duplicates data unnecessarily, which increases costs and operational complexity. Additionally, the writer endpoint does not distribute queries among replicas.
Direct reporting queries to the instance endpoints of the three high-capacity replicas: This is incorrect because managing connections manually to individual instance endpoints is inefficient and does not provide automated query distribution across the replicas.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Endpoints.html
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Database
Question 34Skipped
An application on Amazon Elastic Container Service (ECS) performs data processing in two parts. The second part takes much longer to complete. How can an Architect decouple the data processing from the backend application component?
Process each part using a separate ECS task. Create an Amazon SNS topic and send a notification when the processing completes
Correct answer
Process each part using a separate ECS task. Create an Amazon SQS queue
Process both parts using the same ECS task. Create an Amazon Kinesis Firehose stream
Create an Amazon DynamoDB table and save the output of the first part to the table
Overall explanation
Processing each part using a separate ECS task may not be essential but means you can separate the processing of the data. An Amazon Simple Queue Service (SQS) is used for decoupling applications. It is a message queue on which you place messages for processing by application components. In this case you can process each data processing part in separate ECS tasks and have them write an Amazon SQS queue. That way the backend can pick up the messages from the queue when they’re ready and there is no delay due to the second part not being complete.
CORRECT: "Process each part using a separate ECS task. Create an Amazon SQS queue" is the correct answer.
INCORRECT: "Process both parts using the same ECS task. Create an Amazon Kinesis Firehose stream" is incorrect. Amazon Kinesis Firehose is used for streaming data. This is not an example of streaming data. In this case SQS is better as a message can be placed on a queue to indicate that the job is complete and ready to be picked up by the backend application component.
INCORRECT: "Process each part using a separate ECS task. Create an Amazon SNS topic and send a notification when the processing completes" is incorrect. Amazon Simple Notification Service (SNS) can be used for sending notifications. It is useful when you need to notify multiple AWS services. In this case an Amazon SQS queue is a better solution as there is no mention of multiple AWS services and this is an ideal use case for SQS.
INCORRECT: "Create an Amazon DynamoDB table and save the output of the first part to the table" is incorrect. Amazon DynamoDB is unlikely to be a good solution for this requirement. There is a limit on the maximum amount of data that you can store in an entry in a DynamoDB table.
References:
https://digitalcloud.training/aws-application-integration-services/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Database
Question 40Skipped
A solutions architect is required to move 750 TB of data from a branch office's network-attached file system to Amazon S3 Glacier. The branch office’s internet connection is poor, and the solution must not saturate the connection. Normal business traffic loads must not be affected by the migration.
What is the MOST cost-effective solution?
Order 10 AWS Snowball appliances and point these appliances to an S3 Glacier vault and put in place a bucket policy which will only allow access via a VPC endpoint.
Copy the files directly from the network-attached file system to Amazon S3. Build a lifecycle policy to move the S3 objects across storage classes into Amazon S3 Glacier.
Create a site-to-site VPN connection directly to an Amazon S3 bucket, Enforce the connection with an VPC Endpoint.
Correct answer
Order 10 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier.
Overall explanation
The AWS Snow Family consists of several physical devices which can be used for edge computing, and to migrate large amounts of data into Amazon S3.
The process for using AWS Snowball is as follows:

The solutions architect will need 10 Snowball devices to fulfill the capacity required in this instance as each Snowball contains up to 80TB of usable storage.
CORRECT: "Order 10 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier” is the correct answer (as explained above.)
INCORRECT: "Create a site-to-site VPN connection directly to an Amazon S3 bucket, Enforce the connection with an VPC Endpoint" is incorrect, as although this would achieve the solution, it would be using the branch’s internet connection and would saturate it - preventing normal business activities from taking place.
INCORRECT: "Order 10 AWS Snowball appliances and point these appliances to an S3 Glacier vault and put in place a bucket policy which will only allow access via a VPC endpoint" is incorrect as S3 Glacier is not a viable destination for Snowball, and you need to place it into S3 Standard first then transition the data in Glacier after the fact.
INCORRECT: "Copy the files directly from the network-attached file system to Amazon S3. Build a lifecycle policy to move the S3 objects across storage classes into Amazon S3 Glacier" is incorrect. It is not possible to mount third-party NAS appliance to an S3 bucket. You could use a service like AWS DataSync to move data from the network attached file system into S3, however this would still be traveling over the branch’s internet line.
References:
https://aws.amazon.com/snowball/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/
Domain
AWS Database
Question 48Skipped
An Amazon EC2 instance runs in a VPC network, and the network must be secured by a solutions architect. The EC2 instances contain highly sensitive data and have been launched in private subnets. Company policy restricts EC2 instances that run in the VPC from accessing the internet. The instances need to access the software repositories using a third-party URL to download and install software product updates. All other internet traffic must be blocked, with no exceptions.
Which solution meets these requirements?
Create an AWS WAF web ACL. Filter traffic requests based on source and destination IP address ranges with custom rules.
Establish strict inbound rules for your security groups. Specify the URLs of the authorized software repositories on the internet in your outbound rule.
Correct answer
Configure the route table for the private subnet so that it routes the outbound traffic to an AWS Network Firewall firewall then configure domain list rule groups.
Place an Application Load Balancer in front of your EC2 instances. Direct all outbound traffic to the ALB. For outbound access to the internet, use a URL-based rule listener in the ALB's target group.
Overall explanation
The AWS Network Firewall is a managed service that makes it easy to deploy essential network protections for all your Amazon Virtual Private Clouds, and you can then use domain list rules to block HTTP or HTTPS traffic to domains identified as low-reputation, or that are known or suspected to be associated with malware or botnets.
CORRECT: "Configure the route table for the private subnet so that it routes the outbound traffic to an AWS Network Firewall firewall then configure domain list rule groups" is the correct answer (as explained above.)
INCORRECT: "Create an AWS WAF web ACL. Filter traffic requests based on source and destination IP address ranges with custom rules" is incorrect. AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits and bots that may affect availability, compromise security, or consume excessive resources. It is designed to protect your applications from malicious traffic, not your VPC.
INCORRECT: "Establish strict inbound rules for your security groups. Specify the URLs of the authorized software repositories on the internet in your outbound rule" is incorrect. You cannot specify URLs in security group rules so this would not work.
INCORRECT: "Place an Application Load Balancer in front of your EC2 instances. Direct all outbound traffic to the ALB. For outbound access to the internet, use a URL-based rule listener in the ALB's target group" is incorrect. The ALB would not work as this sits within the VPC and is unable to control traffic entering and leaving the VPC itself.
References:
https://aws.amazon.com/network-firewall/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Database
Question 54Skipped
A company hosts a monolithic web application on an Amazon EC2 instance. Application users have recently reported poor performance at specific times. Analysis of Amazon CloudWatch metrics shows that CPU utilization is 100% during the periods of poor performance.
The company wants to resolve this performance issue and improve application availability.
Which combination of steps will meet these requirements MOST cost-effectively? (Select TWO.)
Create an Auto Scaling group and an Application Load Balancer to scale vertically.
Create an Amazon Machine Image (AMI) from the web server. Reference the AMI in a new launch template.
Correct selection
Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale vertically.
Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale horizontally.
Correct selection
Create an Auto Scaling group and an Application Load Balancer to scale horizontally.
Overall explanation
Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale vertically: This is correct because AWS Compute Optimizer can suggest a more appropriate EC2 instance type with adequate resources for improved performance when scaling vertically.
Create an Auto Scaling group and an Application Load Balancer to scale horizontally: This is correct because horizontal scaling improves application availability by adding multiple EC2 instances. The Application Load Balancer ensures traffic is distributed evenly across instances.
Create an Amazon Machine Image (AMI) from the web server. Reference the AMI in a new launch template: This is incorrect because creating an AMI and a launch template alone does not address scaling or performance issues without integrating them into an Auto Scaling group.
Create an Auto Scaling group and an Application Load Balancer to scale vertically: This is incorrect because vertical scaling is achieved by changing the instance type, not by using Auto Scaling groups or load balancers.
Use AWS Compute Optimizer to obtain a recommendation for an instance type to scale horizontally: This is incorrect because horizontal scaling focuses on adding multiple instances, which does not require Compute Optimizer recommendations for instance types.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
https://aws.amazon.com/compute-optimizer
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Database
Question 56Skipped
A multi-tier application runs with eight front-end web servers in an Amazon EC2 Auto Scaling group in a single Availability Zone behind an Application Load Balancer. A solutions architect needs to modify the infrastructure to be highly available without modifying the application.
Which architecture should the solutions architect choose that provides high availability?
Correct answer
Modify the Auto Scaling group to use four instances across each of two Availability Zones
Create an Auto Scaling group that uses four instances across each of two subnets
Create an Auto Scaling group that uses four instances across each of two Regions
Create an Auto Scaling template that can be used to quickly create more instances in another Region
Overall explanation
High availability can be enabled for this architecture quite simply by modifying the existing Auto Scaling group to use multiple availability zones. The ASG will automatically balance the load so you don’t actually need to specify the instances per AZ.
The architecture for the web tier will look like the one below:


CORRECT: "Modify the Auto Scaling group to use four instances across each of two Availability Zones" is the correct answer.
INCORRECT: "Create an Auto Scaling group that uses four instances across each of two Regions" is incorrect as EC2 Auto Scaling does not support multiple regions.
INCORRECT: "Create an Auto Scaling template that can be used to quickly create more instances in another Region" is incorrect as EC2 Auto Scaling does not support multiple regions.
INCORRECT: "Create an Auto Scaling group that uses four instances across each of two subnets" is incorrect as the subnets could be in the same AZ.
References:
https://aws.amazon.com/ec2/autoscaling/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Database
Question 62Skipped
A transportation company uses GPS devices installed on its fleet of delivery trucks to monitor their location in real time. Each GPS device sends location updates every 5 minutes if the truck has traveled more than 100 meters. The data is transmitted to a web application running on three Amazon EC2 instances deployed across multiple Availability Zones in a single AWS Region.
Recently, during a peak delivery period, the web application was overwhelmed by the increased volume of GPS data, leading to data loss with no way to replay the events. The company wants to ensure that no location data is lost and that the application can scale efficiently to handle traffic spikes, all with minimal operational overhead.
What should the solutions architect do to meet these requirements?
Store the GPS location updates in an Amazon DynamoDB table. Modify the application to query the table for unprocessed data and process it. Use DynamoDB TTL to remove old records after processing.
Use Amazon Kinesis Data Streams to ingest the GPS data. Configure an AWS Lambda function to process the data in real time and store results in an Amazon DynamoDB table.
Use an Amazon S3 bucket to store the GPS location updates. Modify the application to periodically scan the bucket for new files and process the data.
Correct answer
Use an Amazon Simple Queue Service (Amazon SQS) queue to store the incoming GPS data. Modify the application to poll the queue for new messages and process the data.
Overall explanation
Use an Amazon Simple Queue Service (Amazon SQS) queue to store the incoming GPS data. Modify the application to poll the queue for new messages and process the data: This is correct because SQS decouples the data ingestion process from the application. It ensures that no data is lost during traffic spikes and allows the application to process data at its own pace, minimizing the risk of being overwhelmed.
Use an Amazon S3 bucket to store the GPS location updates. Modify the application to periodically scan the bucket for new files and process the data: This is incorrect because Amazon S3 is not ideal for real-time ingestion and processing. Scanning the bucket periodically introduces latency and may not be able to handle high throughput use cases efficiently.
Use Amazon Kinesis Data Streams to ingest the GPS data. Configure an AWS Lambda function to process the data in real time and store results in an Amazon DynamoDB table: This is incorrect because Kinesis Data Streams introduces additional operational complexity and is typically suited for high throughput streaming workloads. SQS provides a simpler, lower-overhead solution for this use case.
Store the GPS location updates in an Amazon DynamoDB table. Modify the application to query the table for unprocessed data and process it. Use DynamoDB TTL to remove old records after processing: This is incorrect because using DynamoDB as a temporary data store for this purpose is less efficient and increases complexity. SQS is specifically designed to handle message queues for this type of workload.
References:
https://docs.aws.amazon.com/sqs/index.html
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-how-it-works.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Database
Question 8Skipped
A research organization is planning to migrate its simulation analysis platform to AWS. The platform stores simulation results and logs on an on-premises NFS server. The platform's codebase is legacy and cannot be modified to use any protocol other than NFS to store and retrieve data. The organization needs a storage solution on AWS that supports NFS and is highly available and scalable.
Which storage solution should a solutions architect recommend for use after the migration?
Use Amazon FSx for Windows File Server to create a shared file system for data storage and access through the SMB protocol.
Correct answer
Use Amazon Elastic File System (Amazon EFS) to provide an NFS-compatible shared file system that integrates with AWS services.
Use Amazon Elastic Block Store (Amazon EBS) volumes attached to each EC2 instance for storage. Use NFS software on the EC2 instances to create a shared file system.
Use AWS Storage Gateway File Gateway to provide an NFS interface backed by Amazon S3 for storing and retrieving data.
Overall explanation
Use Amazon Elastic File System (Amazon EFS) to provide an NFS-compatible shared file system that integrates with AWS services: This is correct because Amazon EFS is a fully managed, scalable, and highly available file storage service that supports NFS. It is designed to work seamlessly with applications requiring NFS without additional setup or modifications.
Use AWS Storage Gateway File Gateway to provide an NFS interface backed by Amazon S3 for storing and retrieving data: This is incorrect because File Gateway is typically used to integrate on-premises environments with AWS. It is not as suitable for applications entirely migrated to AWS, especially when a native NFS solution like EFS is available.
Use Amazon Elastic Block Store (Amazon EBS) volumes attached to each EC2 instance for storage. Use NFS software on the EC2 instances to create a shared file system: This is incorrect because using EBS requires additional configuration and management to implement an NFS-based shared file system. EFS provides a simpler, fully managed solution.
Use Amazon FSx for Windows File Server to create a shared file system for data storage and access through the SMB protocol: This is incorrect because FSx for Windows File Server supports the SMB protocol, not NFS. The application explicitly requires NFS, making FSx for Windows File Server unsuitable.
References:
https://aws.amazon.com/efs/
https://aws.amazon.com/storagegateway/file/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/
Domain
AWS Database
Question 12Skipped
A company has created a disaster recovery solution for an application that runs behind an Application Load Balancer (ALB). The DR solution consists of a second copy of the application running behind a second ALB in another Region. The Solutions Architect requires a method of automatically updating the DNS record to point to the ALB in the second Region.
What action should the Solutions Architect take?
Configure an alarm on a CloudTrail trail.
Use Amazon EventBridge to cluster the ALBs.
Enable an ALB health check.
Correct answer
Enable an Amazon Route 53 health check.
Overall explanation
Amazon Route 53 health checks monitor the health and performance of your web applications, web servers, and other resources. Each health check that you create can monitor one of the following:
  •  The health of a specified resource, such as a web server
  •  The status of other health checks
  •  The status of an Amazon CloudWatch alarm
Health checks can be used with other configurations such as a failover routing policy. In this case a failover routing policy will direct traffic to the ALB of the primary Region unless health checks fail at which time it will direct traffic to the secondary record for the DR ALB.
CORRECT: "Enable an Amazon Route 53 health check" is the correct answer.
INCORRECT: "Enable an ALB health check" is incorrect. This will simply perform health checks of the instances behind the ALB, rather than the ALB itself. This could be used in combination with Route 53 health checks.
INCORRECT: "Use Amazon EventBridge to cluster the ALBs" is incorrect. You cannot cluster ALBs in any way.
INCORRECT: "Configure an alarm on a CloudTrail trail" is incorrect. CloudTrail records API activity so this does not help.
References:
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-route-53/
Domain
AWS Database
Question 20Skipped
An application runs on Amazon EC2 Linux instances. The application generates log files which are written using standard API calls. A storage solution is required that can be used to store the files indefinitely and must allow concurrent access to all files.
Which storage service meets these requirements and is the MOST cost-effective?
Correct answer
Amazon S3
Amazon EC2 instance store
Amazon EBS
Amazon EFS
Overall explanation
The application is writing the files using API calls which means it will be compatible with Amazon S3 which uses a REST API. S3 is a massively scalable key-based object store that is well-suited to allowing concurrent access to the files from many instances.
Amazon S3 will also be the most cost-effective choice. A rough calculation using the AWS pricing calculator shows the cost differences between 1TB of storage on EBS, EFS, and S3 Standard.


CORRECT: "Amazon S3" is the correct answer.
INCORRECT: "Amazon EFS" is incorrect as though this does offer concurrent access from many EC2 Linux instances, it is not the most cost-effective solution.
INCORRECT: "Amazon EBS" is incorrect. The Elastic Block Store (EBS) is not a good solution for concurrent access from many EC2 instances and is not the most cost-effective option either. EBS volumes are mounted to a single instance except when using multi-attach which is a new feature and has several constraints.
INCORRECT: "Amazon EC2 instance store" is incorrect as this is an ephemeral storage solution which means the data is lost when powered down. Therefore, this is not an option for long-term data storage.
References:
https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Database







Dump7
Question 1Skipped
Storage capacity has become an issue for a company that runs application servers on-premises. The servers are connected to a combination of block storage and NFS storage solutions. The company requires a solution that supports local caching without re-architecting its existing applications.
Which combination of changes can the company make to meet these requirements? (Select TWO.)
1. Use AWS Direct Connect and mount an Amazon FSx for Windows File Server using iSCSI.
1. Use Amazon Elastic File System (EFS) volumes to replace the block storage.
1. Use the mount command on servers to mount Amazon S3 buckets using NFS.
Correct selection
1. Use an AWS Storage Gateway file gateway to replace the NFS storage.
Correct selection
Use an AWS Storage Gateway volume gateway to replace the block storage.
Overall explanation
In this scenario the company should use cloud storage to replace the existing storage solutions that are running out of capacity. The on-premises servers mount the existing storage using block protocols (iSCSI) and file protocols (NFS). As there is a requirement to avoid re-architecting existing applications these protocols must be used in the revised solution.
The AWS Storage Gateway volume gateway should be used to replace the block-based storage systems as it is mounted over iSCSI and the file gateway should be used to replace the NFS file systems as it uses NFS.
CORRECT: "Use an AWS Storage Gateway file gateway to replace the NFS storage" is a correct answer.
CORRECT: "Use an AWS Storage Gateway volume gateway to replace the block storage" is a correct answer.
INCORRECT: "Use the mount command on servers to mount Amazon S3 buckets using NFS" is incorrect. You cannot mount S3 buckets using NFS as it is an object-based storage system (not file-based) and uses an HTTP REST API.
INCORRECT: "Use AWS Direct Connect and mount an Amazon FSx for Windows File Server using iSCSI" is incorrect. You cannot mount FSx for Windows File Server file systems using iSCSI, you must use SMB.
INCORRECT: "Use Amazon Elastic File System (EFS) volumes to replace the block storage" is incorrect. You cannot use EFS to replace block storage as it uses NFS rather than iSCSI.
References:
https://docs.aws.amazon.com/storagegateway/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-storage-gateway/
Domain
AWS Database
Question 8Skipped
A solutions architect is designing an application on AWS. The compute layer will run in parallel across EC2 instances. The compute layer should scale based on the number of jobs to be processed. The compute layer is stateless. The solutions architect must ensure that the application is loosely coupled and the job items are durably stored.
Which design should the solutions architect use?
Create an Amazon SNS topic to send the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on the number of messages published to the SNS topic
Create an Amazon SNS topic to send the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on CPU usage
Correct answer
Create an Amazon SQS queue to hold the jobs that needs to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on the number of items in the SQS queue
Create an Amazon SQS queue to hold the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on network usage
Overall explanation
In this case we need to find a durable and loosely coupled solution for storing jobs. Amazon SQS is ideal for this use case and can be configured to use dynamic scaling based on the number of jobs waiting in the queue.
To configure this scaling you can use the backlog per instance metric with the target value being the acceptable backlog per instance to maintain. You can calculate these numbers as follows:
Backlog per instance: To calculate your backlog per instance, start with the ApproximateNumberOfMessages queue attribute to determine the length of the SQS queue (number of messages available for retrieval from the queue). Divide that number by the fleet's running capacity, which for an Auto Scaling group is the number of instances in the InService state, to get the backlog per instance.
Acceptable backlog per instance: To calculate your target value, first determine what your application can accept in terms of latency. Then, take the acceptable latency value and divide it by the average time that an EC2 instance takes to process a message.
This solution will scale EC2 instances using Auto Scaling based on the number of jobs waiting in the SQS queue.
CORRECT: "Create an Amazon SQS queue to hold the jobs that needs to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on the number of items in the SQS queue" is the correct answer.
INCORRECT: "Create an Amazon SQS queue to hold the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on network usage" is incorrect as scaling on network usage does not relate to the number of jobs waiting to be processed.
INCORRECT: "Create an Amazon SNS topic to send the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on CPU usage" is incorrect. Amazon SNS is a notification service so it delivers notifications to subscribers. It does store data durably but is less suitable than SQS for this use case. Scaling on CPU usage is not the best solution as it does not relate to the number of jobs waiting to be processed.
INCORRECT: "Create an Amazon SNS topic to send the jobs that need to be processed. Create an Amazon EC2 Auto Scaling group for the compute application. Set the scaling policy for the Auto Scaling group to add and remove nodes based on the number of messages published to the SNS topic" is incorrect. Amazon SNS is a notification service so it delivers notifications to subscribers. It does store data durably but is less suitable than SQS for this use case. Scaling on the number of notifications in SNS is not possible.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Database
Question 13Skipped
A company is migrating a decoupled application to AWS. The application uses a message broker based on the MQTT protocol. The application will be migrated to Amazon EC2 instances and the solution for the message broker must not require rewriting application code.
Which AWS service can be used for the migrated message broker?
Amazon SNS
Correct answer
Amazon MQ
AWS Step Functions
Amazon SQS
Overall explanation
Amazon MQ is a managed message broker service for Apache ActiveMQ that makes it easy to set up and operate message brokers in the cloud. Connecting current applications to Amazon MQ is easy because it uses industry-standard APIs and protocols for messaging, including JMS, NMS, AMQP, STOMP, MQTT, and WebSocket. Using standards means that in most cases, there’s no need to rewrite any messaging code when you migrate to AWS.
CORRECT: "Amazon MQ" is the correct answer.
INCORRECT: "Amazon SQS" is incorrect. This is an Amazon proprietary service and does not support industry-standard messaging APIs and protocols.
INCORRECT: "Amazon SNS" is incorrect. This is a notification service not a message bus.
INCORRECT: "AWS Step Functions" is incorrect. This is a workflow orchestration service, not a message bus.
References:
https://aws.amazon.com/amazon-mq/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Database
Question 15Skipped
A company delivers content to subscribers distributed globally from an application running on AWS. The application uses a fleet of Amazon EC2 instance in a private subnet behind an Application Load Balancer (ALB). Due to an update in copyright restrictions, it is necessary to block access for specific countries.
What is the EASIEST method to meet this requirement?
Modify the ALB security group to deny incoming traffic from blocked countries
Modify the security group for EC2 instances to deny incoming traffic from blocked countries
Use a network ACL to block the IP address ranges associated with the specific countries
Correct answer
Use Amazon CloudFront to serve the application and deny access to blocked countries
Overall explanation
When a user requests your content, CloudFront typically serves the requested content regardless of where the user is located. If you need to prevent users in specific countries from accessing your content, you can use the CloudFront geo restriction feature to do one of the following:
Allow your users to access your content only if they're in one of the countries on a whitelist of approved countries.
Prevent your users from accessing your content if they're in one of the countries on a blacklist of banned countries.
For example, if a request comes from a country where, for copyright reasons, you are not authorized to distribute your content, you can use CloudFront geo restriction to block the request.
This is the easiest and most effective way to implement a geographic restriction for the delivery of content.
CORRECT: "Use Amazon CloudFront to serve the application and deny access to blocked countries" is the correct answer.
INCORRECT: "Use a Network ACL to block the IP address ranges associated with the specific countries" is incorrect as this would be extremely difficult to manage.
INCORRECT: "Modify the ALB security group to deny incoming traffic from blocked countries" is incorrect as security groups cannot block traffic by country.
INCORRECT: "Modify the security group for EC2 instances to deny incoming traffic from blocked countries" is incorrect as security groups cannot block traffic by country.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Database
Question 30Skipped
A legacy tightly-coupled High Performance Computing (HPC) application will be migrated to AWS. Which network adapter type should be used?
Elastic Network Interface (ENI)
Correct answer
Elastic Fabric Adapter (EFA)
Elastic IP Address
Elastic Network Adapter (ENA)
Overall explanation
An Elastic Fabric Adapter is an AWS Elastic Network Adapter (ENA) with added capabilities. The EFA lets you apply the scale, flexibility, and elasticity of the AWS Cloud to tightly-coupled HPC apps. It is ideal for tightly coupled app as it uses the Message Passing Interface (MPI).
CORRECT: "Elastic Fabric Adapter (EFA)" is the correct answer.
INCORRECT: "Elastic Network Interface (ENI)" is incorrect. The ENI is a basic type of adapter and is not the best choice for this use case.
INCORRECT: "Elastic Network Adapter (ENA)" is incorrect. The ENA, which provides Enhanced Networking, does provide high bandwidth and low inter-instance latency but it does not support the features for a tightly-coupled app that the EFA does.
INCORRECT: "Elastic IP Address" is incorrect. An Elastic IP address is just a static public IP address, it is not a type of network adapter.
References:
https://aws.amazon.com/blogs/aws/now-available-elastic-fabric-adapter-efa-for-tightly-coupled-hpc-workloads/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Database
Question 35Skipped
An application is running on Amazon EC2 behind an Elastic Load Balancer (ELB). Content is being published using Amazon CloudFront and you need to restrict the ability for users to circumvent CloudFront and access the content directly through the ELB.
How can you configure this solution?
Correct answer
Create a VPC Security Group for the ELB and use AWS Lambda to automatically update the CloudFront internal service IP addresses when they change
Use signed URLs or signed cookies to limit access to the content
Use a Network ACL to restrict access to the ELB
Create an Origin Access Identity (OAI) and associate it with the distribution
Overall explanation
The only way to get this working is by using a VPC Security Group for the ELB that is configured to allow only the internal service IP ranges associated with CloudFront. As these are updated from time to time, you can use AWS Lambda to automatically update the addresses. This is done using a trigger that is triggered when AWS issues an SNS topic update when the addresses are changed.
CORRECT: "Create a VPC Security Group for the ELB and use AWS Lambda to automatically update the CloudFront internal service IP addresses when they change" is the correct answer.
INCORRECT: "Create an Origin Access Identity (OAI) and associate it with the distribution" is incorrect. You can use an OAI to restrict access to content in Amazon S3 but not on EC2 or ELB.
INCORRECT: "Use signed URLs or signed cookies to limit access to the content" is incorrect. Signed cookies and URLs are used to limit access to files but this does not stop people from circumventing CloudFront and accessing the ELB directly.
INCORRECT: "Use a Network ACL to restrict access to the ELB" is incorrect. A Network ACL can be used to restrict access to an ELB but it is recommended to use security groups and this solution is incomplete as it does not account for the fact that the internal service IP ranges change over time.
References:
https://aws.amazon.com/blogs/security/how-to-automatically-update-your-security-groups-for-amazon-cloudfront-and-aws-waf-by-using-aws-lambda/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Database
Question 37Skipped
A solutions architect is creating a document submission application for a school. The application will use an Amazon S3 bucket for storage. The solution must prevent accidental deletion of the documents and ensure that all versions of the documents are available. Users must be able to upload and modify the documents.
Which combination of actions should be taken to meet these requirements? (Select TWO.)
Attach an IAM policy to the bucket
Encrypt the bucket using AWS SSE-S3
Correct selection
Enable versioning on the bucket
Set read-only permissions on the bucket
Correct selection
Enable MFA Delete on the bucket
Overall explanation
None of the options present a good solution for specifying permissions required to write and modify objects so that requirement needs to be taken care of separately. The other requirements are to prevent accidental deletion and the ensure that all versions of the document are available.
The two solutions for these requirements are versioning and MFA delete. Versioning will retain a copy of each version of the document and multi-factor authentication delete (MFA delete) will prevent any accidental deletion as you need to supply a second factor when attempting a delete.
CORRECT: "Enable versioning on the bucket" is a correct answer.
CORRECT: "Enable MFA Delete on the bucket" is also a correct answer.
INCORRECT: "Set read-only permissions on the bucket" is incorrect as this will also prevent any writing to the bucket which is not desired.
INCORRECT: "Attach an IAM policy to the bucket" is incorrect as users need to modify documents which will also allow delete. Therefore, a method must be implemented to just control deletes.
INCORRECT: "Encrypt the bucket using AWS SSE-S3" is incorrect as encryption doesn’t stop you from deleting an object.
References:
https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html
https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingMFADelete.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Database
Question 42Skipped
The Chief Financial Officer of a large corporation is looking for an AWS native tool which will help reduce their cloud spend. After receiving a budget alarm, the company has decided that they need to reduce their spend across their different areas of compute and need insights into their spend to decide where they can reduce cost.
What is the easiest way to achieve this goal?
Correct answer
AWS Compute Optimizer
AWS Cost Explorer
AWS Trusted Advisor
Cost and Usage Reports
Overall explanation
AWS Compute Optimizer helps you identify the optimal AWS resource configurations, such as Amazon Elastic Compute Cloud (EC2) instance types, Amazon Elastic Block Store (EBS) volume configurations, and AWS Lambda function memory sizes, using machine learning to analyze historical utilization metrics. AWS Compute Optimizer provides a set of APIs and a console experience to help you reduce costs and increase workload performance by recommending the optimal AWS resources for your AWS workloads.

CORRECT: "AWS Compute Optimizer" is the correct answer (as explained above.)
INCORRECT: "AWS Trusted Advisor" is incorrect. Whilst you will get some cost recommendations using Trusted Advisor, when working with reducing cost for compute specifically, AWS Compute Optimizer is a better choice.
INCORRECT: "Cost and Usage Reports" is incorrect. Cost and Usage Reports are a highly detailed report of your spend and usage across your entire AWS Environment. Whilst it can be used to understand cost, it does not make recommendations.
INCORRECT: "AWS Cost Explorer" is incorrect. Cost Explorer gives you insight into your spend and usage in a graphical format, which can be filtered and grouped by parameters like Region, instance type and can use Tags to further group resources. It does not however make any recommendations on how to reduce spend.
References:
https://aws.amazon.com/compute-optimizer/faqs/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-billing-and-pricing/
Domain
AWS Database
Question 51Skipped
A retail organization sends coupons out twice a week and this results in a predictable surge in sales traffic. The application runs on Amazon EC2 instances behind an Elastic Load Balancer. The organization is looking for ways lower costs while ensuring they meet the demands of their customers.
How can they achieve this goal?
Increase the instance size of the existing EC2 instances
Purchase Amazon EC2 dedicated hosts
Correct answer
Use capacity reservations with savings plans
Use a mixture of spot instances and on demand instances
Overall explanation
On-Demand Capacity Reservations enable you to reserve compute capacity for your Amazon EC2 instances in a specific Availability Zone for any duration. By creating Capacity Reservations, you ensure that you always have access to EC2 capacity when you need it, for as long as you need it. When used in combination with savings plans, you can also gain the advantages of cost reduction.
CORRECT: " Use capacity reservations with savings plans" is the correct answer.
INCORRECT: "Use a mixture of spot instances and on demand instances" is incorrect. You can mix spot and on-demand in an auto scaling group. However, there’s a risk the spot price may not be good, and this is a regular, predictable increase in traffic.
INCORRECT: "Increase the instance size of the existing EC2 instances" is incorrect. This would add more cost all the time rather than catering for the temporary increases in traffic.
INCORRECT: "Purchase Amazon EC2 dedicated hosts" is incorrect. This is not a way to save cost as dedicated hosts are much more expensive than shared hosts.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html#capacity-reservations-differences
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Database
Question 60Skipped
A company runs a large batch processing job at the end of every quarter. The processing job runs for 5 days and uses 15 Amazon EC2 instances. The processing must run uninterrupted for 5 hours per day. The company is investigating ways to reduce the cost of the batch processing job.
Which pricing model should the company choose?
Spot Instances
Reserved Instances
Dedicated Instances
Correct answer
On-Demand Instances
Overall explanation
Each EC2 instance runs for 5 hours a day for 5 days per quarter or 20 days per year. This is time duration is insufficient to warrant reserved instances as these require a commitment of a minimum of 1 year and the discounts would not outweigh the costs of having the reservations unused for a large percentage of time. In this case, there are no options presented that can reduce the cost and therefore on-demand instances should be used.
CORRECT: "On-Demand Instances" is the correct answer.
INCORRECT: "Reserved Instances" is incorrect. Reserved instances are good for continuously running workloads that run for a period of 1 or 3 years.
INCORRECT: "Spot Instances" is incorrect. Spot instances may be interrupted, and this is not acceptable. Note that Spot Block is deprecated and unavailable to new customers.
INCORRECT: "Dedicated Instances" is incorrect. These do not provide any cost advantages and will be more expensive.
References:
https://aws.amazon.com/ec2/pricing/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Database
Question 5Skipped
A company uses several Windows Servers as the operating system of choice for all their application servers hosted in their data center. The company wants to move some file servers into the cloud, and keep some in their data center, mounted to the same File System. The company also wants to maintain extremely low latency access to their on-premises data center, across a private network. The company has an AWS Direct Connect connection set up into the us-east-1 Region.
What should a solutions architect do to meet these requirements?
Install an NFS client on to the on-premises servers and mount an Amazon EFS file system to the servers. Mount the same file system to the EC2 instances within the Amazon VPC. Use the existing Direct Connect connection to connect the on-premises data center to the Amazon VPC.
Correct answer
Install an SMB client on to the on-premises servers and mount an Amazon FSx file system to the servers. Mount the same file system to the EC2 instances within the Amazon VPC. Use the existing Direct Connect connection to connect the on-premises data center to the Amazon VPC.
Use Amazon S3 on Outposts and mount the S3 File Gateway on to the on-premises servers.
Migrate all the data to Amazon DynamoDB Local. Ensure all users have the appropriate IAM permissions to access the relevant files.
Overall explanation
The current AWS Direct connect connection will provide the ability to share a file system between on-premises servers and Amazon EC2 instances in the AWS Cloud. Direct Connect provides low latency access to their on-premises data center, and the company’s use of Windows File Servers necessitates the use of an SMB-based Amazon FSx File System.
CORRECT: "Install an SMB client on to the on-premises servers and mount an Amazon FSx file system to the servers. Mount the same file system to the EC2 instances within the Amazon VPC. Use the existing Direct Connect connection to connect the on-premises data center to the Amazon VPC" is the correct answer (as explained above.)
INCORRECT: "Migrate all the data to Amazon DynamoDB Local. Ensure all users have the appropriate IAM permissions to access the relevant files" is incorrect. This will not give the company the use of a Windows File Server, and instead give them a NoSQL database. DynamoDB Local is not suitable for this use case.
INCORRECT: "Use Amazon S3 on Outposts and mount the S3 File Gateway on to the on-premises servers" is incorrect. Amazon S3 on Outposts would not provide a hybrid cloud experience as required by the customer, and S3 File Gateway uses a Linux based file system, which is incompatible with the Windows setup the company currently uses.
INCORRECT: "Install an NFS client on to the on-premises servers and mount an Amazon EFS file system to the servers. Mount the same file system to the EC2 instances within the Amazon VPC. Use the existing Direct Connect connection to connect the on-premises data center to the Amazon VPC" is incorrect.
Amazon EFS is a file system that is accessed using the NFS protocol and is suitable for Linux clients only. This is not natively supported for Window Servers, making this an unsuitable option.
References:
https://docs.aws.amazon.com/efs/latest/ug/efs-onpremises.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Database
Question 18Skipped
A company has multiple Windows workloads which are .NET application servers and Microsoft SQL Server databases running on Amazon EC2 instances with Windows Server 2016. The company requires a shared file system which is highly available, durable and provides high levels of throughput and IOPS.
What is the best way to meet this requirement?
Correct answer
Extend the file share environment to Amazon FSx for Windows File Server with a Multi-AZ configuration. Migrate all the data to FSx for Windows File Server.
Migrate all the data to Amazon S3. Set up IAM authentication for users to access files.
Set up an Amazon S3 File Gateway, mount the S3 File Gateway on the existing EC2 instances.
Extend the file share environment to Amazon Elastic File System (Amazon EFS) with a Multi-AZ configuration. Migrate all the data to Amazon EFS.
Overall explanation

As a fully managed service, FSx for Windows File Server eliminates the administrative overhead of setting up and provisioning file servers and storage volumes. Additionally, Amazon FSx keeps Windows software up to date, detects and addresses hardware failures, and performs backups.
Amazon FSx also provides rich integration with other AWS services like AWS IAM, AWS Directory Service for Microsoft Active Directory, Amazon WorkSpaces, AWS Key Management Service, and AWS CloudTrail.
CORRECT: "Extend the file share environment to Amazon FSx for Windows File Server with a Multi-AZ configuration. Migrate all the data to FSx for Windows File Server" is the correct answer (as explained above.)
INCORRECT: "Migrate all the data to Amazon S3. Set up IAM authentication for users to access files" is incorrect. Since the workload is Windows specific, S3 wouldn’t really help as an optimal solution though S3 can be still used to backup objects.
INCORRECT: "Set up an Amazon S3 File Gateway, mount the S3 File Gateway on the existing EC2 instances" is incorrect. Amazon S3 File Gateway provides a seamless way to connect to the cloud to store application data files and backup images as durable objects in Amazon S3 cloud storage with SMB or NFS-based access and local caching. However, this is a solution designed for on-premises servers, not EC2 instances and is not the best option for this scenario.
INCORRECT: "Extend the file share environment to Amazon Elastic File System (Amazon EFS) with a Multi-AZ configuration. Migrate all the data to Amazon EFS" is incorrect. EFS cannot be used with Microsoft workloads using the SMB protocol as it only supports Linux and NFS.
References:
https://aws.amazon.com/fsx/windows/
https://docs.aws.amazon.com/fsx/latest/WindowsGuide/managing-file-shares.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Database
Question 20Skipped
An application analyzes images of people that are uploaded to an Amazon S3 bucket. The application determines demographic data which is then saved to a .CSV file in another S3 bucket. The data must be encrypted at rest and then queried using SQL. The solution should be fully serverless.
Which actions should a Solutions Architect take to encrypt and query the data?
Use Amazon S3 server-side encryption and Amazon QuickSight to query the data
Use AWS KMS encryption keys for the S3 bucket and use Amazon Managed Service for Apache Flink to query the data.
Use Amazon S3 server-side encryption and use Amazon RedShift Spectrum to query the data
Correct answer
Use AWS KMS encryption keys for the S3 bucket and use Amazon Athena to query the data
Overall explanation
Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run. Amazon Athena supports encrypted data for both the source data and query results, for example, using Amazon S3 with AWS KMS.
CORRECT: "Use AWS KMS encryption keys for the S3 bucket and use Amazon Athena to query the data" is the correct answer.
INCORRECT: "Use Amazon S3 server-side encryption and use Amazon RedShift Spectrum to query the data" is incorrect. RedShift Spectrum is not serverless as it requires a RedShift cluster which is based on EC2 instances.
INCORRECT: "Use AWS KMS encryption keys for the S3 bucket and use Amazon Managed Service for Apache Flink to query the data" is incorrect. Amazon Managed Service for Apache Flink is used for analyzing real-time streaming data in Kinesis streams.
INCORRECT: "Use Amazon S3 server-side encryption and Amazon QuickSight to query the data" is incorrect. Amazon QuickSight is an interactive dashboard, it is not a service for running queries on data.
References:
https://d1.awsstatic.com/whitepapers/architecture/wellarchitected-Machine-Learning-Lens.pdf
https://aws.amazon.com/athena/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-athena/
Domain
AWS Database
Question 32Skipped
A software development firm uses AWS to run their compute instances across multiple accounts. These instances are individually billed. The company recently purchased an EC2 Reserved Instance (RI) for an ongoing project. However, due to the completion of that project, a significant number of EC2 instances were decommissioned. The company now wishes to utilize the benefits of their unused Reserved Instance across their other AWS accounts.
Which combination of steps should the company follow to achieve this? (Select TWO.)
Use AWS Organizations to establish a new payer account and invite the other accounts to join this organization.
Correct selection
Enable Reserved Instance sharing in the billing preferences section of the AWS Management Console for the account that purchased the existing RI.
Enable Reserved Instance sharing in the billing preferences section of the AWS Management Console for the management account.
Correct selection
Establish an AWS Organization in the AWS account that purchased the RI and hosts the remaining active EC2 instances. Invite the other AWS accounts to join this organization from the management account.
From the AWS Organizations management account, utilize AWS Resource Access Manager (AWS RAM) to share the Reserved Instance with other accounts.
Overall explanation
Just like the Savings Plans, the benefits of Reserved Instances can be applied across accounts if those accounts are part of the same AWS Organization and if sharing is enabled. This can be achieved by enabling Reserved Instance sharing in the AWS Management Console for the account that purchased the RI.
Setting up an AWS Organization from the account that purchased the Reserved Instance allows you to group your accounts. After the organization is set up, you can invite other accounts to join the organization, enabling you to share the benefits of the Reserved Instance across all accounts in the organization.
CORRECT: "Enable Reserved Instance sharing in the billing preferences section of the AWS Management Console for the account that purchased the existing RI" is a correct answer (as explained above.)
CORRECT: "Establish an AWS Organization in the AWS account that purchased the RI and hosts the remaining active EC2 instances. Invite the other AWS accounts to join this organization from the management account" is also a correct answer (as explained above.)
INCORRECT: "From the AWS Organizations management account, utilize AWS Resource Access Manager (AWS RAM) to share the Reserved Instance with other accounts" is incorrect.
AWS RAM does not apply to Reserved Instances. It is used to share other resources like Subnets, Transit Gateways, etc.
INCORRECT: "Enable Reserved Instance sharing in the billing preferences section of the AWS Management Console for the management account" is incorrect.
Reserved Instance sharing needs to be enabled in the account that purchased the RI, not the management account.
INCORRECT: "Use AWS Organizations to establish a new payer account and invite the other accounts to join this organization" is incorrect.
Creating a new payer account is not necessary. It would be more efficient to use the existing account that purchased the Reserved Instance.
References:
https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/billing-what-is.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-organizations/
Domain
AWS Database
Question 34Skipped
A data analytics company is hosting a data lake which consists of data in Amazon S3 and Amazon RDS for PostgreSQL. The company needs a reporting solution that provides data visualization for the latest dataset and includes all the data sources within the data lake. Only the company's management team should have full access to all the visualizations. The rest of the company should have only limited access.
Which solution will meet these requirements?
Correct answer
Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate users and groups.
Create an AWS Glue table and crawler for the data in Amazon S3. Use Amazon Athena Federated Query to access data within Amazon RDS for PostgreSQL. Generate reports by using Amazon Athena. Publish the reports to Amazon S3. Use S3 bucket policies to limit access to the reports.
Create an AWS Glue table and crawler for the data in Amazon S3. Create an AWS Glue extract, transform, and load (ETL) job to produce reports. Publish the reports to Amazon S3. Use S3 bucket policies to limit access to the reports.
Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate IAM roles.
Overall explanation
Amazon QuickSight is the best fit for data visualization and reporting, especially when data resides in Amazon S3 and Amazon RDS for PostgreSQL. QuickSight supports connecting to both Amazon S3 (via Athena) and RDS for PostgreSQL as data sources, allowing integrated dashboards across both.
QuickSight allows you to control access at the level of users and groups, which is more fine-grained than IAM roles for sharing dashboards. User/group sharing aligns with the need to give management full access and limited access to others, fulfilling the access control requirements effectively.
CORRECT: "Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate users and groups" is the correct answer (as explained above.)
INCORRECT: "Create an AWS Glue table and crawler for the data in Amazon S3. Use Amazon Athena Federated Query to access data within Amazon RDS for PostgreSQL. Generate reports by using Amazon Athena. Publish the reports to Amazon S3. Use S3 bucket policies to limit access to the reports" is incorrect.
While Athena Federated Queries are useful for joining S3 and RDS data, it lacks visualization capabilities. Again, S3-based reports are not ideal for dashboards or restricted sharing by user role.

INCORRECT: "Create an analysis in Amazon QuickSight. Connect all the data sources and create new datasets. Publish dashboards to visualize the data. Share the dashboards with the appropriate users and groups " is incorrect.
As with the previous answer, this option solves the problem of access sharing with resources but does not take care of delta in data. Also, you connect user and groups in your QuickSight account but not IAM Roles.
INCORRECT: "Create an AWS Glue table and crawler for the data in Amazon S3. Create an AWS Glue extract, transform, and load (ETL) job to produce reports. Publish the reports to Amazon S3. Use S3 bucket policies to limit access to the reports" is incorrect.
Amazon Athena should be used with AWS Glue to provide the required functionality as described in the explanation above and the article linked below.
References:
https://docs.aws.amazon.com/athena/latest/ug/connect-to-a-data-source.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-glue/
https://digitalcloud.training/amazon-athena/
Domain
AWS Database
Question 35Skipped
A finance organization has bootstrapped a golden image for their in-house application and the resultant AMI is to be shared across various AWS accounts as a base image. This image is to be used across many applications. The company needs to design an application that captures AWS API calls and sends alerts whenever the Amazon EC2 CreateImage API operation is called within the company's account.
Which solution will meet these requirements with the LEAST operational overhead?
Configure AWS CloudTrail with an Amazon SNS notification that occurs when updated logs are sent to Amazon S3. Use Amazon Athena to create a new table and to query on CreateImage when an API call is detected
Configure an Amazon SQS FIFO queue as a target for AWS CloudTrail logs. Create an AWS Lambda function to send an alert to an Amazon SNS topic when a CreateImage API call is detected.
Create an AWS Lambda function to query AWS CloudTrail logs and to send an alert when a CreateImage API call is detected.
Correct answer
Create an Amazon EventBridge rule for the CreateImage API call. Configure the target as an Amazon SNS topic to send an alert when a Createlmage API call is detected.
Overall explanation
You can create an Amazon EventBridge rule that triggers on an action by an AWS service that does not emit events. In this case you can base the rule on API calls made by AWS CloudTrail. The rule can trigger when the Amazon EC2 CreateImage API is called. The rule can then trigger another service or action.
CORRECT: "Create an Amazon EventBridge rule for the CreateImage API call. Configure the target as an Amazon SNS topic to send an alert when a Createlmage API call is detected" is the correct answer (as explained above.)
INCORRECT: "Configure AWS CloudTrail with an Amazon SNS notification that occurs when updated logs are sent to Amazon S3. Use Amazon Athena to create a new table and to query on CreateImage when an API call is detected" is incorrect.
Athena is a query analysis tool hence this option is incorrect.
INCORRECT: "Create an AWS Lambda function to query AWS CloudTrail logs and to send an alert when a CreateImage API call is detected" is incorrect.
Since the question asks about least operational overhead, this option becomes incorrect. This is an achievable solution but involves building custom code in Lambda and requires more effort.
INCORRECT: "Configure an Amazon SQS FIFO queue as a target for AWS CloudTrail logs. Create an AWS Lambda function to send an alert to an Amazon SNS topic when a CreateImage API call is detected" is incorrect.
You cannot configure CloudTrail logs to be sent directly to an SQS queue.
References:
https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-log-api-call.html
Domain
AWS Database
Question 39Skipped
A traffic law enforcement company is building a solution that has thousands of edge devices that collectively generate 1 TB of status alerts each day. These devices provide vehicle information and number plate data whenever alerts detecting red light jumps are detected. Each entry is around 2Kb in size. A solutions architect needs to implement a solution to ingest and store the alerts for future analysis.
The company wants a highly available solution. However, the company needs to minimize costs and does not want to manage additional infrastructure. Additionally, the company wants to keep 14 days of data available for immediate analysis and archive any data older than 14 days.
What is the MOST operationally efficient solution that meets these requirements?
Launch Amazon EC2 instances across two Availability Zones and place them behind an Elastic Load Balancer to ingest the alerts. Create a script on the EC2 instances that will store the alerts in an Amazon S3 bucket. Set up an S3 Lifecycle configuration to transition data to Amazon S3 Glacier after 14 days.
Create an Amazon Simple Queue Service (Amazon SQS) standard queue to ingest the alerts and set the message retention period to 14 days. Configure consumers to poll the SQS queue, check the age of the message, and analyze the message data as needed. If the message is 14 days old, the consumer should copy the message to an Amazon S3 bucket and delete the message from the SQS queue.
Correct answer
Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the Kinesis Data Firehose stream to deliver the alerts to an Amazon S3 bucket. Set up an S3 Lifecycle configuration to transition data to Amazon S3 Glacier after 14 days.
Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the kinesis Data Firehose stream to deliver the alerts to an Amazon OpenSearch Service (Amazon Elasticsearch Service) cluster. Set up the Amazon Open Search Service (Amazon Elasticsearch Service) cluster to take manual snapshots every day and delete data from the cluster that is older than 14 days.
Overall explanation
Data ingestion is a good use case for since it is scalable and can achieve the volumes required. Also, an S3 lifecycle configuration is appropriate for the requirement for data retention.
CORRECT: "Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the kinesis Data Firehose stream to deliver the alerts to an Amazon S3 bucket. Set up an S3 Lifecycle configuration to transition data to Amazon S3 Glacier after 14 days" is the correct answer (as explained above.)
INCORRECT: "Launch Amazon EC2 instances across two Availability Zones and place them behind an Elastic Load Balancer to ingest the alerts. Create a script on the EC2 instances that will store the alerts in an Amazon S3 bucket. Set up an S3 Lifecycle configuration to transition data to Amazon S3 Glacier after 14 days" is incorrect. Provisioning additional EC2 instances means provisioning infrastructure, and the question states that the company wants to avoid this.
INCORRECT: "Create an Amazon Kinesis Data Firehose delivery stream to ingest the alerts. Configure the kinesis Data Firehose stream to deliver the alerts to an Amazon OpenSearch Service (Amazon Elasticsearch Service) cluster. Set up the Amazon Open Search Service (Amazon Elasticsearch Service) cluster to take manual snapshots every day and delete data from the cluster that is older than 14 days" is incorrect. This option would mean provisioning ECS clusters and since the question is asking for archival of data, S3 is a better fit (data deletion is not desired).
INCORRECT: "Create an Amazon Simple Queue Service (Amazon SQS) standard queue to ingest the alerts and set the message retention period to 14 days. Configure consumers to poll the SQS queue, check the age of the message, and analyze the message data as needed. If the message is 14 days old, the consumer should copy the message to an Amazon S3 bucket and delete the message from the SQS queue" is incorrect.
With an SQS queue you must have processing components adding and retrieving messages from the queue and this means additional infrastructure to manage. With Kinesis Data Firehose the data is loaded straight to the destination without any need for additional infrastructure.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
https://aws.amazon.com/kinesis/data-firehose/features/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-kinesis/
Domain
AWS Database
Question 53Skipped
An application uses Amazon EC2 instances and an Amazon RDS MySQL database. The database is not currently encrypted. A solutions architect needs to apply encryption to the database for all new and existing data.
How should this be accomplished?
Create an RDS read replica with encryption at rest enabled. Promote the read replica to master and switch the application over to the new master. Delete the old RDS instance
Create an Amazon ElastiCache cluster and encrypt data using the cache nodes
Enable encryption for the database using the API. Take a full snapshot of the database. Delete old snapshots
Correct answer
Take a snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot
Overall explanation
There are some limitations for encrypted Amazon RDS DB Instances: you can't modify an existing unencrypted Amazon RDS DB instance to make the instance encrypted, and you can't create an encrypted read replica from an unencrypted instance.
However, you can use the Amazon RDS snapshot feature to encrypt an unencrypted snapshot that's taken from the RDS database that you want to encrypt. Restore a new RDS DB instance from the encrypted snapshot to deploy a new encrypted DB instance. Finally, switch your connections to the new DB instance.
CORRECT: "Take a snapshot of the RDS instance. Create an encrypted copy of the snapshot. Restore the RDS instance from the encrypted snapshot" is the correct answer.
INCORRECT: "Create an Amazon ElastiCache cluster and encrypt data using the cache nodes" is incorrect as you cannot encrypt an RDS database using an ElastiCache cache node.
INCORRECT: "Enable encryption for the database using the API. Take a full snapshot of the database. Delete old snapshots" is incorrect as you cannot enable encryption for an existing database.
INCORRECT: "Create an RDS read replica with encryption at rest enabled. Promote the read replica to master and switch the application over to the new master. Delete the old RDS instance" is incorrect as you cannot create an encrypted read replica from an unencrypted database instance.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
https://aws.amazon.com/premiumsupport/knowledge-center/rds-encrypt-instance-mysql-mariadb/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Database
Question 54Skipped
A Solutions Architect is designing a migration strategy for a company moving to the AWS Cloud. The company use a shared Microsoft filesystem that uses Distributed File System Namespaces (DFSN). What will be the MOST suitable migration strategy for the filesystem?
Use the AWS Server Migration Service to migrate to an Amazon S3 bucket
Correct answer
Use AWS DataSync to migrate to Amazon FSx for Windows File Server
Use AWS DataSync to migrate to an Amazon EFS filesystem
Use the AWS Server Migration Service to migrate to Amazon FSx for Lustre
Overall explanation
The destination filesystem should be Amazon FSx for Windows File Server. This supports DFSN and is the most suitable storage solution for Microsoft filesystems. AWS DataSync supports migrating to the Amazon FSx and automates the process.
CORRECT: "Use AWS DataSync to migrate to Amazon FSx for Windows File Server" is the correct answer.
INCORRECT: "Use the AWS Server Migration Service to migrate to Amazon FSx for Lustre" is incorrect. The server migration service is used to migrate virtual machines and FSx for Lustre does not support Windows filesystems.
INCORRECT: "Use AWS DataSync to migrate to an Amazon EFS filesystem" is incorrect. You can migrate data to EFS using DataSync but it is the wrong destination for a Microsoft filesystem (Linux only).
INCORRECT: "Use the AWS Server Migration Service to migrate to an Amazon S3 bucket" is incorrect. The server migration service is used to migrate virtual machines and Amazon S3 is an object-based storage system and unsuitable for hosting a Microsoft filesystem.
References:
https://aws.amazon.com/blogs/storage/migrate-to-amazon-fsx-for-windows-file-server-using-aws-datasync/
https://docs.aws.amazon.com/fsx/latest/WindowsGuide/migrate-files-fsx.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Database
Question 64Skipped
An online education platform uses Amazon CloudFront to distribute learning resources globally. The company wants to ensure that only enrolled students have access to the course materials. These materials are stored in an Amazon S3 bucket. In addition, the company occasionally provides exclusive resources to certain students for research and project work.
Which solution will meet these requirements?
Create and provide S3 pre-signed URLs to authenticated students.
Implement CloudFront Field-Level Encryption to block access to non-enrolled students.
Utilize Amazon S3 object-level encryption for course materials.
Correct answer
Implement CloudFront signed cookies for authenticated students.
Overall explanation
CloudFront signed cookies are a method to control who can access your content. When a user authenticates and is verified as an enrolled student, the application can set a cookie in the student's browser. The cookie contains the same information that can be included in a signed URL but applies to multiple files in one or multiple directories.
CORRECT: "Implement CloudFront signed cookies for authenticated students" is the correct answer (as explained above.)
INCORRECT: "Create and provide S3 pre-signed URLs to authenticated students" is incorrect.
S3 pre-signed URLs are used to grant temporary access to a specific S3 object. This could be a valid option for individual file access but would be less efficient for multiple files or directories.
INCORRECT: "Utilize Amazon S3 object-level encryption for course materials" is incorrect.
Amazon S3 object-level encryption is mainly about securing data at rest, it won't control who can or cannot access the content.
INCORRECT: "Implement CloudFront Field-Level Encryption to block access to non-enrolled students" is incorrect.
CloudFront Field-Level Encryption handles sensitive information in HTTP POST requests to help prevent the information from being seen by unauthorized viewers. It's not designed to control access to content.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-cookies.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Database
Question 16Skipped
A web application is running on a fleet of Amazon EC2 instances using an Auto Scaling Group. It is desired that the CPU usage in the fleet is kept at 40%.
How should scaling be configured?
Use a simple scaling policy that launches instances when the average CPU hits 40%
Use a step scaling policy that uses the PercentChangeInCapacity value to adjust the group size as required
Correct answer
Use a target tracking policy that keeps the average aggregate CPU utilization at 40%
Use a custom CloudWatch alarm to monitor CPU usage and notify the ASG using Amazon SNS
Overall explanation
This is a perfect use case for a target tracking scaling policy. With target tracking scaling policies, you select a scaling metric and set a target value. In this case you can just set the target value to 40% average aggregate CPU utilization.
CORRECT: "Use a target tracking policy that keeps the average aggregate CPU utilization at 40%" is the correct answer.
INCORRECT: "Use a simple scaling policy that launches instances when the average CPU hits 40%" is incorrect. A simple scaling policy will add instances when 40% CPU utilization is reached, but it is not designed to maintain 40% CPU utilization across the group.
INCORRECT: "Use a step scaling policy that uses the PercentChangeInCapacity value to adjust the group size as required" is incorrect. The step scaling policy makes scaling adjustments based on a number of factors. The PercentChangeInCapacity value increments or decrements the group size by a specified percentage. This does not relate to CPU utilization.
INCORRECT: "Use a custom CloudWatch alarm to monitor CPU usage and notify the ASG using Amazon SNS" is incorrect. You do not need to create a custom Amazon CloudWatch alarm as the ASG can scale using a policy based on CPU utilization using standard configuration.

References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Database
Question 23Skipped
A healthcare company is migrating its patient record system to AWS. The company receives thousands of encrypted patient data files every day through FTP. An on-premises server processes the data files twice a day. However, the processing job takes hours to finish.
The company wants the AWS solution to process incoming data files as soon as they arrive with minimal changes to the FTP clients that send the files. The solution must delete the incoming data files after the files have been processed successfully. Processing for each file needs to take around 10 minutes.
Which solution will meet these requirements in the MOST operationally efficient way?
Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Standard. Use Amazon EC2 instances managed by an Auto Scaling group to process the files. Set an S3 event notification to trigger an AWS Lambda function that launches the EC2 instances when the files arrive. Delete the files after they are processed.
Correct answer
Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Standard. Create an AWS Lambda function to process the files and to delete the files after they are processed. Use an S3 event notification to invoke the Lambda function when the files arrive.
Use an Amazon EC2 instance that runs an SFTP server to store incoming files in Amazon S3 Standard. Configure a job queue in AWS Batch. Use Amazon EventBridge rules to invoke the job to process the files twice a day. Delete the files after the job has processed the files.
Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Glacier. Configure an Amazon EC2 instance to process the files. Use Amazon EventBridge rules to invoke the EC2 instance to process the files twice a day from S3 Glacier. Delete the objects after the job has processed the objects.
Overall explanation
AWS Transfer Family provides fully managed support for file transfers directly into and out of Amazon S3 using SFTP. Storing incoming files in S3 Standard offers high durability, availability, and performance object storage for frequently accessed data.
AWS Lambda can respond immediately to S3 events, which allows processing of files as soon as they arrive. Lambda can also delete the files after processing. This meets all requirements and is operationally efficient, as it requires minimal management and has low costs.
CORRECT: "Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Standard. Create an AWS Lambda function to process the files and to delete the files after they are processed. Use an S3 event notification to invoke the Lambda function when the files arrive" is the correct answer (as explained above.)
INCORRECT: "Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Glacier. Configure an Amazon EC2 instance to process the files. Use Amazon EventBridge rules to invoke the EC2 instance to process the files twice a day from S3 Glacier. Delete the objects after the job has processed the objects" is incorrect.
This option involves using Amazon S3 Glacier, which is primarily used for long-term archival storage. Accessing data for processing could take longer and be more expensive than using S3 Standard. In addition, EC2 instances need to be managed and are less efficient for this scenario compared to AWS Lambda.
INCORRECT: "Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Standard. Use Amazon EC2 instances managed by an Auto Scaling group to process the files. Set an S3 event notification to trigger an AWS Lambda function that launches the EC2 instances when the files arrive. Delete the files after they are processed" is incorrect.
While this solution will work, it is less efficient operationally because managing EC2 instances and an Auto Scaling group is more complex and likely more expensive than simply using AWS Lambda for processing.
INCORRECT: "Use an Amazon EC2 instance that runs an SFTP server to store incoming files in Amazon S3 Standard. Configure a job queue in AWS Batch. Use Amazon EventBridge rules to invoke the job to process the files twice a day. Delete the files after the job has processed the files" is incorrect.
This option does not meet the requirement of processing incoming data files as soon as they arrive, as EventBridge rules would invoke the job only twice a day. It also involves managing an EC2 instance, which is less operationally efficient than the AWS Transfer Family and AWS Lambda option.
References:
https://aws.amazon.com/aws-transfer-family/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/
Domain
AWS Database
Question 30Skipped
A corporation has a web-based multiplayer gaming service that operates using both TCP and UDP protocols. Amazon Route 53 is currently employed to direct application traffic to a set of Network Load Balancers (NLBs) in various AWS Regions. To prepare for an increase in user activity, the company must enhance application performance and reduce latency.
Which approach will best meet these requirements?
Substitute the NLBs with Application Load Balancers (ALBs) and set Route 53 to utilize latency-based routing.
Correct answer
Implement AWS Global Accelerator ahead of the NLBs and align the Global Accelerator endpoint to use the appropriate listener ports.
Insert an Amazon API Gateway endpoint behind the NLBs, enable API caching, and customize method caching across different stages.
Incorporate Amazon CloudFront in front of the NLBs and extend the duration of the Cache-Control max-age directive.
Overall explanation
AWS Global Accelerator is designed to improve the availability and performance of your applications for local and global users. It directs traffic to optimal endpoints over the AWS global network, thus enhancing the performance of your TCP and UDP traffic by routing packets through the AWS global network infrastructure, reducing jitter, and improving overall game performance.
CORRECT: "Implement AWS Global Accelerator ahead of the NLBs and align the Global Accelerator endpoint to use the appropriate listener ports" is the correct answer (as explained above.)
INCORRECT: "Incorporate Amazon CloudFront in front of the NLBs and extend the duration of the Cache-Control max-age directive" is incorrect.
Amazon CloudFront is a content delivery network (CDN) that speeds up the delivery of your static and dynamic web content. While it could potentially help with application performance, it doesn't directly improve TCP/UDP performance, which is the specific requirement in this case.
INCORRECT: "Substitute the NLBs with Application Load Balancers (ALBs) and set Route 53 to utilize latency-based routing" is incorrect.
Application Load Balancers (ALBs) are layer 7 load balancers and they do not support the handling of raw TCP and UDP traffic, which is a requirement for the gaming application in the question. NLBs, on the other hand, are suitable for extreme performance needs and for TCP/UDP traffic.
INCORRECT: "Insert an Amazon API Gateway endpoint behind the NLBs, enable API caching, and customize method caching across different stages" is incorrect.
While the API Gateway would add more control and security to the application, the caching feature is not necessarily beneficial for this real-time gaming scenario where the content is likely to change frequently and unpredictably.
References:
https://aws.amazon.com/global-accelerator/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-global-accelerator/
Domain
AWS Database
Question 41Skipped
A solutions architect is designing a high performance computing (HPC) application using Amazon EC2 Linux instances. All EC2 instances need to communicate to each other with low latency and high throughput network performance.
Which EC2 solution BEST meets these requirements?
Launch the EC2 instances in an Auto Scaling group spanning multiple Availability Zones
Correct answer
Launch the EC2 instances in a cluster placement group in one Availability Zone
Launch the EC2 instances in a spread placement group in one Availability Zone
Launch the EC2 instances in an Auto Scaling group in two Regions. Place a Network Load Balancer in front of the instances
Overall explanation
When you launch a new EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload. Depending on the type of workload, you can create a placement group using one of the following placement strategies:
Cluster – packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of HPC applications.
Partition – spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka.
Spread – strictly places a small group of instances across distinct underlying hardware to reduce correlated failures.
For this scenario, a cluster placement group should be used as this is the best option for providing low-latency network performance for a HPC application.
CORRECT: "Launch the EC2 instances in a cluster placement group in one Availability Zone" is the correct answer.
INCORRECT: "Launch the EC2 instances in a spread placement group in one Availability Zone" is incorrect as the spread placement group is used to spread instances across distinct underlying hardware.
INCORRECT: "Launch the EC2 instances in an Auto Scaling group in two Regions. Place a Network Load Balancer in front of the instances" is incorrect as this does not achieve the stated requirement to provide low-latency, high throughput network performance between instances. Also, you cannot use an ELB across Regions.
INCORRECT: "Launch the EC2 instances in an Auto Scaling group spanning multiple Availability Zones" is incorrect as this does not reduce network latency or improve performance.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Database
Question 48Skipped
A company is planning to migrate a large quantity of important data to Amazon S3. The data will be uploaded to a versioning enabled bucket in the us-west-1 Region. The solution needs to include replication of the data to another Region for disaster recovery purposes.
How should a solutions architect configure the replication?
Create an additional S3 bucket in another Region and configure cross-origin resource sharing (CORS)
Create an additional S3 bucket with versioning in another Region and configure cross-origin resource sharing (CORS)
Correct answer
Create an additional S3 bucket with versioning in another Region and configure cross-Region replication
Create an additional S3 bucket in another Region and configure cross-Region replication
Overall explanation
Replication enables automatic, asynchronous copying of objects across Amazon S3 buckets. Buckets that are configured for object replication can be owned by the same AWS account or by different accounts. You can copy objects between different AWS Regions or within the same Region. Both source and destination buckets must have versioning enabled.
CORRECT: "Create an additional S3 bucket with versioning in another Region and configure cross-Region replication" is the correct answer.
INCORRECT: "Create an additional S3 bucket in another Region and configure cross-Region replication" is incorrect as the destination bucket must also have versioning enabled.
INCORRECT: "Create an additional S3 bucket in another Region and configure cross-origin resource sharing (CORS)" is incorrect as CORS is not related to replication.
INCORRECT: "Create an additional S3 bucket with versioning in another Region and configure cross-origin resource sharing (CORS)" is incorrect as CORS is not related to replication.
References:
https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Database
Question 53Skipped
A solutions architect is optimizing a website for real-time streaming and on-demand videos. The website’s users are located around the world and the solutions architect needs to optimize the performance for both the real-time and on-demand streaming.
Which service should the solutions architect choose?
AWS Global Accelerator
Amazon S3 Transfer Acceleration
Amazon Route 53
Correct answer
Amazon CloudFront
Overall explanation
Amazon CloudFront can be used to stream video to users across the globe using a wide variety of protocols that are layered on top of HTTP. This can include both on-demand video as well as real time streaming video.
CORRECT: "Amazon CloudFront" is the correct answer.
INCORRECT: "AWS Global Accelerator" is incorrect as this would be an expensive way of getting the content closer to users compared to using CloudFront. As this is a use case for CloudFront and there are so many edge locations it is the better option.
INCORRECT: "Amazon Route 53" is incorrect as you still need a solution for getting the content closer to users.
INCORRECT: "Amazon S3 Transfer Acceleration" is incorrect as this is used to accelerate uploads of data to Amazon S3 buckets.
References:
https://aws.amazon.com/cloudfront/streaming/
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/on-demand-streaming-video.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Database
Question 57Skipped
A legacy application is being migrated into AWS. The application has a large amount of data that is rarely accessed. When files are accessed they are retrieved sequentially. The application will be migrated onto an Amazon EC2 instance.
What is the LEAST expensive EBS volume type for this use case?
Throughput Optimized HDD (st1)
Provisioned IOPS SSD (io1)
General Purpose SSD (gp2)
Correct answer
Cold HDD (sc1)
Overall explanation
The cold HDD (sc1) EBS volume type is the lowest cost option that is suitable for this use case. The sc1 volume type is suitable for infrequently accessed data and use cases that are oriented towards throughput like sequential data access.


CORRECT: "Cold HDD (sc1)" is the correct answer.
INCORRECT: "Provisioned IOPS SSD (io1)" is incorrect. This is the most expensive option and used for use cases that demand high IOPS.
INCORRECT: "General Purpose SSD (gp2)" is incorrect. This is a more expensive SSD volume type that is used for general use cases.
INCORRECT: "Throughput Optimized HDD (st1)" is incorrect. This is also used for throughput-oriented use cases however it is higher cost than sc1 and better for frequently accessed data.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Database
Question 61Skipped
A data analytics company is building a high-performance application that requires concurrent writes to a shared block storage volume from multiple Amazon EC2 instances.
The EC2 instances are Nitro-based and reside within the same Availability Zone. The company needs a storage solution that supports simultaneous connections to facilitate data resilience and high availability.
Which solution will meet these requirements?
Use Amazon S3 with S3 Transfer Acceleration to enhance speed.
Correct answer
Use Provisioned IOPS SSD (io2) EBS volumes with Amazon EBS Multi-Attach.
Use Amazon EFS with NFSv4.1 protocol across multiple EC2 instances.
Use General Purpose SSD (gp2) EBS volumes with Amazon EBS Multi-Attach.
Overall explanation
io2 volumes are designed for I/O-intensive workloads, particularly database workloads, that require high performance and low latency. io1 and io2 volumes support Multi-Attach, which enables you to attach a single volume to multiple EC2 instances in the same Availability Zone.
CORRECT: "Use Provisioned IOPS SSD (io2) EBS volumes with Amazon EBS Multi-Attach" is the correct answer (as explained above.)
INCORRECT: "Use Amazon EFS with NFSv4.1 protocol across multiple EC2 instances" is incorrect.
Amazon Elastic File System (EFS) is a scalable file storage for use with Amazon EC2. You can use an Amazon EFS file system as a common data source for workloads and applications running on multiple instances, but it does not provide the block-level storage required for high IOPS operations.
INCORRECT: "Use Amazon S3 with S3 Transfer Acceleration to enhance speed" is incorrect.
Amazon S3 is an object storage service. While S3 Transfer Acceleration does enhance the speed of in-transit file transfers, it is not a block storage solution, it is an object storage solution and is not suitable for this use case.
INCORRECT: "Use General Purpose SSD (gp2) EBS volumes with Amazon EBS Multi-Attach" is incorrect.
Amazon EBS Multi-Attach only supports io1 and io2 volumes, and it is not supported on gp2 volumes.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes-multi.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
Domain
AWS Database

Dump10
Question 1Skipped
An ivy-league university is assisting NASA to find potential landing sites for exploration vehicles of unmanned missions to our neighboring planets. The university uses High Performance Computing (HPC) driven application architecture to identify these landing sites.
Which of the following Amazon EC2 instance topologies should this application be deployed on?
The Amazon EC2 instances should be deployed in an Auto Scaling group so that application meets high availability requirements
Correct answer
The Amazon EC2 instances should be deployed in a cluster placement group so that the underlying workload can benefit from low network latency and high network throughput
The Amazon EC2 instances should be deployed in a partition placement group so that distributed workloads can be handled effectively
The Amazon EC2 instances should be deployed in a spread placement group so that there are no correlated failures
Overall explanation
Correct option:
The Amazon EC2 instances should be deployed in a cluster placement group so that the underlying workload can benefit from low network latency and high network throughput
The key thing to understand in this question is that HPC workloads need to achieve low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of HPC applications. Cluster placement groups pack instances close together inside an Availability Zone. These are recommended for applications that benefit from low network latency, high network throughput, or both. Therefore this option is the correct answer.
Cluster Placement Group: 

 via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html

Incorrect options:
The Amazon EC2 instances should be deployed in a partition placement group so that distributed workloads can be handled effectively - A partition placement group spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka. A partition placement group can have a maximum of seven partitions per Availability Zone. Since a partition placement group can have partitions in multiple Availability Zones in the same region, therefore instances will not have low-latency network performance. Hence the partition placement group is not the right fit for HPC applications.
Partition Placement Group: 

 via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html

The Amazon EC2 instances should be deployed in a spread placement group so that there are no correlated failures - A spread placement group is a group of instances that are each placed on distinct racks, with each rack having its own network and power source. The instances are placed across distinct underlying hardware to reduce correlated failures. You can have a maximum of seven running instances per Availability Zone per group. Since a spread placement group can span multiple Availability Zones in the same Region, therefore instances will not have low-latency network performance. Hence spread placement group is not the right fit for HPC applications.
Spread Placement Group: 

 via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html

The Amazon EC2 instances should be deployed in an Auto Scaling group so that application meets high availability requirements - An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling. You do not use Auto Scaling groups per se to meet HPC requirements.
Reference:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
