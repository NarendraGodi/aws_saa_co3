## AWS Services Reference

| Service | Description |
|---|---|
| **AWS Storage Gateway (Tape Gateway)** | A hybrid cloud storage service that emulates physical tape libraries using virtual tapes in AWS (iSCSI-VTL), enabling existing backup applications and workflows to continue without changes. |
| **Amazon EFS (Elastic File System)** | A fully managed, elastic NFS file system for Linux-based workloads. Accessible over the NFS protocol; not suitable for tape-based backup or SMB use cases. |
| **Amazon EC2 (Elastic Compute Cloud)** | A web service that provides secure, resizable compute capacity in the cloud, allowing you to run virtual servers on demand. |
| **Amazon RDS (Relational Database Service)** | A managed relational database service supporting MySQL, PostgreSQL, SQL Server, and others. Supports Multi-AZ deployments for high availability and IAM-based authentication. |
| **AWS IAM (Identity and Access Management)** | A service that enables you to securely manage access to AWS services and resources. IAM roles attached to EC2 instances can eliminate the need for stored credentials. |
| **AWS PrivateLink** | Enables private connectivity between VPCs and supported AWS or third-party services without exposing traffic to the public internet. Requires a Network Load Balancer on the provider side. |
| **NAT Gateway** | A managed AWS networking component that allows instances in a private subnet to initiate outbound internet traffic while preventing unsolicited inbound connections. |
| **AWS Direct Connect** | A dedicated private network connection between an on-premises environment and AWS. Not used for connecting to third-party SaaS providers hosted on AWS. |
| **AWS VPN** | Creates an encrypted tunnel between on-premises environments and AWS. Typically used for hybrid connectivity, not for private SaaS-to-VPC communication within AWS. |
| **Amazon SQS (Simple Queue Service)** | A fully managed message queuing service. Standard queues offer high throughput; FIFO queues preserve order. Separate queues can be used to implement priority-based processing. |
| **AWS Compute Optimizer** | Analyzes EC2 instances, Auto Scaling groups, and EBS volumes using machine learning to provide cost optimization recommendations with minimal operational overhead. |
| **Amazon CloudWatch** | A monitoring and observability service. Billing alerts can be configured but require manual analysis; not ideal as a standalone cost optimization tool. |
| **AWS Cost and Usage Reports / Athena** | Provides detailed cost data exportable to S3 for querying with Athena. Useful for insights but requires significant manual effort compared to Compute Optimizer. |
| **Amazon S3 (Simple Storage Service)** | An object storage service. Can host static websites used as failover targets with Route 53. Also used as the destination for Kinesis Firehose and security data lakes. |
| **Amazon Route 53** | A scalable DNS and traffic management service. Supports geolocation, geoproximity, weighted, and failover routing policies. Failover routing redirects traffic when health checks fail. |
| **AWS Global Accelerator** | Improves performance by routing traffic to the nearest healthy endpoint using the AWS global network. Not a cost-effective solution for simple failover scenarios. |
| **Amazon EC2 Auto Scaling** | Automatically adjusts the number of EC2 instances based on demand. Must span multiple AZs with an ALB for high availability. |
| **Application Load Balancer (ALB)** | A Layer 7 load balancer that distributes incoming application traffic across multiple targets. Must span multiple AZs for high availability. |
| **Amazon Security Lake** | A purpose-built service for centralizing security data from AWS accounts and Regions. Automatically collects, normalizes (OCSF format), and stores data in S3 with minimal development effort. |
| **AWS Glue** | A serverless data integration service. Can crawl and catalog security data into Lake Formation but requires more setup than Amazon Security Lake. |
| **Amazon RDS Multi-AZ** | A high-availability feature for RDS that maintains a synchronous standby replica in a different AZ, enabling automatic failover. |
| **S3 Bucket Key (SSE-KMS)** | Reduces the number of AWS KMS API calls by caching encryption keys at the bucket level, lowering encryption costs while maintaining KMS-based compliance requirements. |
| **SSE-S3** | Server-side encryption using S3-managed keys. Does not use AWS KMS and may not meet strict encryption compliance requirements that mandate KMS. |
| **SSE-C** | Server-side encryption with customer-provided keys. Requires the customer to manage their own keys; does not reduce KMS costs. |
| **Network Load Balancer (NLB)** | A Layer 4 load balancer required on the provider side when exposing services via AWS PrivateLink as an endpoint service. |
| **AWS IAM Identity Center** | A service for centralized user authentication and access management, integrating with Active Directory. Supports permission sets for fine-grained, least-privilege access to AWS services. |
| **Amazon Cognito** | Provides sign-up/sign-in and access control for web and mobile apps. Suitable for end-user authentication but adds complexity compared to IAM Identity Center for internal teams. |
| **AWS Organizations / SCPs** | Enables centralized management of multiple AWS accounts. Service Control Policies restrict actions at the account level; cross-account roles add operational overhead. |
| **Amazon Kinesis Data Streams** | A real-time streaming service. Uses partition keys to route ordered records for the same asset to the same processor, ensuring ordered, per-asset event processing. |
| **Amazon Kinesis Data Firehose** | Loads streaming data from Kinesis Data Streams into destinations such as Amazon S3. Fully managed with no custom code required. |
| **Amazon SQS FIFO Queue** | Preserves message order and exactly-once processing, but does not support message prioritization between tiers. |
| **Amazon CloudFront** | A content delivery network (CDN). Can cache and serve content from S3 or custom origins; used alongside Lambda and S3 for cost-effective, serverless image processing. |
| **AWS Lambda** | A serverless compute service. Ideal for event-driven image processing triggered by API Gateway; no ongoing compute cost when idle. |
| **AWS WAF (Web Application Firewall)** | Protects web applications by filtering HTTP requests. Supports IP set match statements to block specific IP addresses. Cannot be replaced by NACLs in CloudFront scenarios. |
| **EC2 Hibernate** | Saves the contents of RAM to the EBS root volume when the instance is stopped. On restart, the RAM is reloaded, processes resume, and the instance ID is retained. |
| **EC2 Reserved Instances** | Provide significant discounts for workloads that run continuously (24/7). Require a 1- or 3-year commitment; not ideal for dev environments with irregular schedules. |
| **On-Demand Capacity Reservations** | Reserve EC2 capacity in a specific AZ without a long-term commitment. Ideal for dev environments that need guaranteed capacity during business hours. |
| **EC2 Spot Instances** | Cost-effective for flexible, interruption-tolerant workloads. Not suitable when guaranteed capacity during specific hours is required. |
| **Amazon FSx for Windows File Server** | Fully managed, SMB-accessible file storage built on Windows Server. Ideal for migrating on-premises NAS/DFS workloads. Supports AWS DataSync for migration. |
| **Amazon FSx for Lustre** | A high-performance file system for compute-intensive workloads. Not suitable for SMB-based Windows file server use cases. |
| **AWS DataSync** | Automates and accelerates data migration between on-premises storage (NFS/SMB) and AWS storage services including S3, EFS, and FSx for Windows File Server. |
| **AWS Cost Explorer API** | Provides programmatic access to AWS cost and usage data. Supports pagination for large datasets and can be integrated into operational dashboards without manual steps. |
| **AWS Budgets** | Sets alerts when cost or usage thresholds are breached. Does not support programmatic data export via SMTP or FTP; not suitable for dashboard integration. |
| **AWS Control Tower** | Automates the setup of a secure, multi-account AWS landing zone using best-practice blueprints for identity, federated access, and account structure. Uses an Account Factory for standardized provisioning. |
| **Amazon Machine Image (AMI)** | A template for launching EC2 instances. Can be copied across AWS Regions using the CopyImage API to support cross-region disaster recovery deployments. |
| **Amazon EBS (Elastic Block Store)** | Persistent block storage for EC2. EBS volumes cannot be directly copied to/from S3 using the S3 API. Snapshots are used for cross-region replication. |
| **Amazon Keyspaces (for Apache Cassandra)** | A managed, Cassandra-compatible database service. The correct AWS equivalent for migrating Apache Cassandra workloads; not DynamoDB. |
| **Amazon ECS on Fargate** | A serverless container orchestration option. Eliminates the need to manage EC2 worker nodes; ideal for containerized, SUSE Linux-based compute tiers. |
| **AWS Private 5G** | A managed service that makes it easy to deploy, operate, and scale a private cellular network, with all required hardware and software provided by AWS. |
| **AWS Wavelength** | Embeds AWS compute and storage within 5G networks for mobile edge computing. Not the same as building a private cellular network. |
| **AWS Outposts** | Delivers AWS infrastructure and services to on-premises or edge locations. Does not provision private 5G cellular networks. |
| **Amazon Route 53 – Geolocation Routing** | Routes traffic based on the geographic location of DNS query origin. Used to enforce content distribution rights by directing users to region-specific resources. |
| **Amazon Route 53 – Geoproximity Routing** | Routes traffic based on the location of resources, with optional bias adjustments. Not the same as restricting access by user geography. |
| **Amazon DynamoDB** | A fully managed NoSQL key-value and document database. Not Cassandra-compatible and not a drop-in replacement for Apache Cassandra workloads. |
| **Amazon Aurora** | A MySQL/PostgreSQL-compatible managed relational database. Does not support Microsoft SQL Server workloads. |
| **Amazon RDS for SQL Server** | A managed Microsoft SQL Server database. The correct target when migrating a SQL Server-dependent application tier to AWS. |
| **Amazon EBS – General Purpose SSD (gp2)** | Cost-effective SSD storage with baseline 3 IOPS/GiB and burst to 3,000 IOPS. Suitable for most workloads with variable I/O. |
| **Amazon EBS – Provisioned IOPS SSD (io1)** | High-performance SSD for I/O-intensive workloads. More expensive than gp2; not required unless consistent high IOPS are needed. |
| **Amazon EBS – Throughput Optimized HDD (st1)** | Low-cost HDD optimized for throughput, not IOPS. Not suitable for latency-sensitive or IOPS-driven workloads. |
| **Amazon EBS – Cold HDD (sc1)** | Lowest-cost HDD for infrequently accessed data. No IOPS SLA; not suitable for active application workloads. |

---

## AWS Application Integration – Practice Questions

---

### Question 9 (Backup Infrastructure)

**Q:** A company is investigating methods to reduce the expenses associated with on-premises backup infrastructure. The Solutions Architect wants to reduce costs by eliminating the use of physical backup tapes. It is a requirement that existing backup applications and workflows should continue to function.

What should the Solutions Architect recommend?

**Options:**

- **✅ Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).**
- Connect the backup applications to an AWS Storage Gateway using the iSCSI protocol.
- Create an Amazon EFS file system and connect the backup applications using the iSCSI protocol.
- Create an Amazon EFS file system and connect the backup applications using the NFS protocol.

**A:** **Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).**

**Explanation:**

The AWS Storage Gateway Tape Gateway enables you to replace using physical tapes on premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway emulates physical tape libraries, removes the cost and complexity of managing physical tape infrastructure, and provides more durability than physical tapes.

- **CORRECT:** "Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL)" is the correct answer.
- **INCORRECT:** "Create an Amazon EFS file system and connect the backup applications using the NFS protocol" is incorrect. The NFS protocol is used by AWS Storage Gateway File Gateways but these do not provide virtual tape functionality suitable for replacing the existing backup infrastructure.
- **INCORRECT:** "Create an Amazon EFS file system and connect the backup applications using the iSCSI protocol" is incorrect. The NFS protocol is used by AWS Storage Gateway File Gateways but these do not provide virtual tape functionality suitable for replacing the existing backup infrastructure.
- **INCORRECT:** "Connect the backup applications to an AWS Storage Gateway using the iSCSI protocol" is incorrect. The iSCSI protocol is used by AWS Storage Gateway Volume Gateways but these do not provide virtual tape functionality suitable for replacing the existing backup infrastructure.

**References:**
- https://aws.amazon.com/storagegateway/vtl/
- https://digitalcloud.training/aws-storage-gateway/

---

### Question 17 (Secure Database Credentials)

**Q:** A developer created an application that uses Amazon EC2 and an Amazon RDS MySQL database instance. The developer stored the database user name and password in a configuration file on the root EBS volume of the EC2 application instance. A Solutions Architect has been asked to design a more secure solution.

What should the Solutions Architect do to achieve this requirement?

**Options:**

- **✅ Create an IAM role with permission to access the database. Attach this IAM role to the EC2 instance.**
- Install an Amazon-trusted root certificate on the application instance and use SSL/TLS encrypted connections to the database.
- Attach an additional volume to the EC2 instance with encryption enabled. Move the configuration file to the encrypted volume.
- Move the configuration file to an Amazon S3 bucket. Create an IAM role with permission to the bucket and attach it to the EC2 instance.

**A:** **Create an IAM role with permission to access the database. Attach this IAM role to the EC2 instance.**

**Explanation:**

The key problem here is having plain text credentials stored in a file. Even if you encrypt the volume there is still a security risk as the credentials are loaded by the application and passed to RDS. The best way to secure this solution is to get rid of the credentials completely by using an IAM role instead. The IAM role can be assigned permissions to the database instance and can be attached to the EC2 instance. The instance will then obtain temporary security credentials from AWS STS which is much more secure.

- **CORRECT:** "Create an IAM role with permission to access the database. Attach this IAM role to the EC2 instance" is the correct answer.
- **INCORRECT:** "Move the configuration file to an Amazon S3 bucket. Create an IAM role with permission to the bucket and attach it to the EC2 instance" is incorrect. This just relocates the file; the contents are still unsecured and must be loaded by the application and passed to RDS. This is an insecure process.
- **INCORRECT:** "Attach an additional volume to the EC2 instance with encryption enabled. Move the configuration file to the encrypted volume" is incorrect. This will only encrypt the file at rest, it still must be read, and the contents passed to RDS which is insecure.
- **INCORRECT:** "Install an Amazon-trusted root certificate on the application instance and use SSL/TLS encrypted connections to the database" is incorrect. The file is still unsecured on the EBS volume so encrypting the credentials in an encrypted channel between the EC2 instance and RDS does not solve all security issues.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html
- https://digitalcloud.training/aws-iam/

---

### Question 31 (Private SaaS Connectivity)

**Q:** A company operates a multi-tier application with its backend services deployed on Amazon EC2 instances in a VPC. The backend services must communicate securely with APIs of a third-party SaaS provider that is also hosted on AWS. The company wants to ensure that this communication occurs privately and minimizes exposure to the public internet.

Which solution will meet these requirements?

**Options:**

- **✅ Configure AWS PrivateLink to create a private connection between the VPC and the third-party SaaS provider's APIs.**
- Deploy a NAT gateway in the VPC to enable secure outbound communication with the third-party SaaS provider.
- Set up an AWS Direct Connect connection between the VPC and the third-party SaaS provider to establish private communication.
- Use an AWS VPN connection to establish a secure tunnel between the VPC and the third-party SaaS provider's infrastructure.

**A:** **Configure AWS PrivateLink to create a private connection between the VPC and the third-party SaaS provider's APIs.**

**Explanation:**

AWS PrivateLink enables private connectivity between VPCs and supported AWS or third-party services, ensuring that traffic does not traverse the public internet.

- **CORRECT:** "Configure AWS PrivateLink to create a private connection between the VPC and the third-party SaaS provider's APIs" is the correct answer.
- **INCORRECT:** "Set up an AWS Direct Connect connection between the VPC and the third-party SaaS provider to establish private communication" is incorrect. AWS Direct Connect is used for establishing private connections between on-premises environments and AWS, not for connecting to third-party SaaS providers within AWS.
- **INCORRECT:** "Deploy a NAT gateway in the VPC to enable secure outbound communication with the third-party SaaS provider" is incorrect. A NAT gateway facilitates outbound internet access for resources in private subnets but does not ensure private communication with third-party services.
- **INCORRECT:** "Use an AWS VPN connection to establish a secure tunnel between the VPC and the third-party SaaS provider's infrastructure" is incorrect. VPN connections are typically used for secure communication between on-premises environments and AWS, not for private connectivity to SaaS providers hosted on AWS.

**References:**
- https://docs.aws.amazon.com/privatelink/latest/userguide/what-is-privatelink.html
- https://aws.amazon.com/privatelink/
- https://digitalcloud.training/amazon-vpc/

---

### Question 40 (SQS Priority Queues)

**Q:** A web application allows users to upload photos and add graphical elements to them. The application offers two tiers of service: free and paid. Photos uploaded by paid users should be processed before those submitted using the free tier. The photos are uploaded to an Amazon S3 bucket which uses an event notification to send the job information to Amazon SQS.

How should a Solutions Architect configure the Amazon SQS deployment to meet these requirements?

**Options:**

- Use one SQS standard queue. Use batching for the paid photos and short polling for the free photos.
- Use one SQS FIFO queue. Assign a higher priority to the paid photos so they are processed first.
- **✅ Use a separate SQS Standard queue for each tier. Configure Amazon EC2 instances to prioritize polling for the paid queue over the free queue.**
- Use a separate SQS FIFO queue for each tier. Set the free queue to use short polling and the paid queue to use long polling.

**A:** **Use a separate SQS Standard queue for each tier. Configure Amazon EC2 instances to prioritize polling for the paid queue over the free queue.**

**Explanation:**

AWS recommend using separate queues when you need to provide prioritization of work. The logic can then be implemented at the application layer to prioritize the queue for the paid photos over the queue for the free photos.

- **CORRECT:** "Use a separate SQS Standard queue for each tier. Configure Amazon EC2 instances to prioritize polling for the paid queue over the free queue" is the correct answer.
- **INCORRECT:** "Use one SQS FIFO queue. Assign a higher priority to the paid photos so they are processed first" is incorrect. FIFO queues preserve the order of messages but they do not prioritize messages within the queue. The orders would need to be placed into the queue in a priority order and there's no way of doing this as the messages are sent automatically through event notifications as they are received by Amazon S3.
- **INCORRECT:** "Use one SQS standard queue. Use batching for the paid photos and short polling for the free photos" is incorrect. Batching adds efficiency but it has nothing to do with ordering or priority.
- **INCORRECT:** "Use a separate SQS FIFO queue for each tier. Set the free queue to use short polling and the paid queue to use long polling" is incorrect. Short polling and long polling are used to control the amount of time the consumer process waits before closing the API call and trying again. Polling should be configured for efficiency of API calls and processing of messages but does not help with message prioritization.

**References:**
- https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-how-it-works.html
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 41 (Compute Optimizer)

**Q:** Amazon EC2 instances in an Auto Scaling group. The application stores temporary training data on attached Amazon Elastic Block Store (Amazon EBS) volumes. The company seeks recommendations to optimize costs for the EC2 instances, the Auto Scaling group, and the EBS volumes with minimal manual intervention.

Which solution will meet these requirements with the MOST operational efficiency?

**Options:**

- Use AWS Cost and Usage Reports to export data to Amazon Athena. Query the data to identify inefficiencies in the EC2 instances, the Auto Scaling group, and the EBS volumes.
- Set up Amazon CloudWatch billing alerts and manually analyze metrics to identify cost-saving opportunities for the EC2 instances, the Auto Scaling group, and the EBS volumes.
- Use AWS Compute Optimizer for recommendations on EC2 instances and Auto Scaling groups. Use Amazon Data Lifecycle Manager to evaluate cost optimizations for the EBS volumes.
- **✅ Configure AWS Compute Optimizer to provide cost optimization recommendations for the EC2 instances, the Auto Scaling group, and the EBS volumes.**

**A:** **Configure AWS Compute Optimizer to provide cost optimization recommendations for the EC2 instances, the Auto Scaling group, and the EBS volumes.**

**Explanation:**

AWS Compute Optimizer offers actionable insights for cost optimization across EC2 instances, Auto Scaling groups, and EBS volumes with minimal operational overhead.

- **CORRECT:** "Configure AWS Compute Optimizer to provide cost optimization recommendations for the EC2 instances, the Auto Scaling group, and the EBS volumes" is the correct answer.
- **INCORRECT:** "Set up Amazon CloudWatch billing alerts and manually analyze metrics to identify cost-saving opportunities for the EC2 instances, the Auto Scaling group, and the EBS volumes" is incorrect. This option requires significant manual intervention, which reduces operational efficiency.
- **INCORRECT:** "Use AWS Cost and Usage Reports to export data to Amazon Athena. Query the data to identify inefficiencies in the EC2 instances, the Auto Scaling group, and the EBS volumes" is incorrect. While this approach provides insights, it requires significant manual effort to analyze the data.
- **INCORRECT:** "Use AWS Compute Optimizer for recommendations on EC2 instances and Auto Scaling groups. Use Amazon Data Lifecycle Manager to evaluate cost optimizations for the EBS volumes" is incorrect. This requires separate configurations for different resources, increasing complexity compared to a single AWS Compute Optimizer setup.

**References:**
- https://docs.aws.amazon.com/compute-optimizer/latest/ug/what-is.html
- https://docs.aws.amazon.com/AmazonEBS/latest/dg/ebs-automatic-snapshot-policy.html

---

### Question 45 (S3 Static Failover Website)

**Q:** A company has deployed a new website on Amazon EC2 instances behind an Application Load Balancer (ALB). Amazon Route 53 is used for the DNS service. The company has asked a Solutions Architect to create a backup website with support contact details that users will be directed to automatically if the primary website is down.

How should the Solutions Architect deploy this solution cost-effectively?

**Options:**

- Configure a static website using Amazon S3 and create a Route 53 weighted routing policy.
- **✅ Configure a static website using Amazon S3 and create a Route 53 failover routing policy.**
- Create the backup website on EC2 and ALB in another Region and create an AWS Global Accelerator endpoint.
- Deploy the backup website on EC2 and ALB in another Region and use Route 53 health checks for failover routing.

**A:** **Configure a static website using Amazon S3 and create a Route 53 failover routing policy.**

**Explanation:**

The most cost-effective solution is to create a static website using an Amazon S3 bucket and then use a failover routing policy in Amazon Route 53. With a failover routing policy users will be directed to the main website as long as it is responding to health checks successfully. If the main website fails to respond to health checks (it's down), Route 53 will begin to direct users to the backup website running on the Amazon S3 bucket. It's important to set the TTL on the Route 53 records appropriately to ensure that users resolve the failover address within a short time.

- **CORRECT:** "Configure a static website using Amazon S3 and create a Route 53 failover routing policy" is the correct answer.
- **INCORRECT:** "Configure a static website using Amazon S3 and create a Route 53 weighted routing policy" is incorrect. Weighted routing is used when you want to send a percentage of traffic between multiple endpoints. In this case all traffic should go to the primary until it fails, then all should go to the backup.
- **INCORRECT:** "Deploy the backup website on EC2 and ALB in another Region and use Route 53 health checks for failover routing" is incorrect. This is not a cost-effective solution for the backup website. It can be implemented using Route 53 failover routing which uses health checks but would be an expensive option.
- **INCORRECT:** "Create the backup website on EC2 and ALB in another Region and create an AWS Global Accelerator endpoint" is incorrect. Global Accelerator is used for performance as it directs traffic to the nearest healthy endpoint. It is not useful for failover in this scenario and is also a very expensive solution.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
- https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-configuring.html
- https://digitalcloud.training/amazon-s3-and-glacier/
- https://digitalcloud.training/amazon-route-53/

---

### Question 62 (High Availability – Multi-AZ)

**Q:** An eCommerce company runs an application on Amazon EC2 instances in public and private subnets. The web application runs in a public subnet and the database runs in a private subnet. Both the public and private subnets are in a single Availability Zone.

Which combination of steps should a solutions architect take to provide high availability for this architecture? (Select TWO.)

**Options:**

- Create an EC2 Auto Scaling group in the public subnet and use an Application Load Balancer.
- Create new public and private subnets in a different AZ. Create a database using Amazon EC2 in one AZ.
- **✅ Create an EC2 Auto Scaling group and Application Load Balancer that spans across multiple AZs.**
- Create new public and private subnets in the same AZ but in a different Amazon VPC.
- **✅ Create new public and private subnets in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment.**

**A:** **Create an EC2 Auto Scaling group and Application Load Balancer that spans across multiple AZs** AND **Create new public and private subnets in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment.**

**Explanation:**

High availability can be achieved by using multiple Availability Zones within the same VPC. An EC2 Auto Scaling group can then be used to launch web application instances in multiple public subnets across multiple AZs and an ALB can be used to distribute incoming load. The database solution can be made highly available by migrating from EC2 to Amazon RDS and using a Multi-AZ deployment model. This will provide the ability to failover to another AZ in the event of a failure of the primary database or the AZ in which it runs.

- **CORRECT:** "Create an EC2 Auto Scaling group and Application Load Balancer that spans across multiple AZs" is a correct answer.
- **CORRECT:** "Create new public and private subnets in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment" is also a correct answer.
- **INCORRECT:** "Create new public and private subnets in the same AZ but in a different Amazon VPC" is incorrect. You cannot use multiple VPCs for this solution as it would be difficult to manage and direct traffic (you can't load balance across VPCs).
- **INCORRECT:** "Create an EC2 Auto Scaling group in the public subnet and use an Application Load Balancer" is incorrect. This does not achieve HA as you need multiple public subnets across multiple AZs.
- **INCORRECT:** "Create new public and private subnets in a different AZ. Create a database using Amazon EC2 in one AZ" is incorrect. The database solution is not HA in this answer option.

**References:**
- https://aws.amazon.com/ec2/autoscaling/
- https://digitalcloud.training/amazon-ec2-auto-scaling/
- https://digitalcloud.training/amazon-rds/

---

### Question 63 (Security Lake)

**Q:** A company runs workloads in the AWS Cloud and wants to consolidate and analyze security-related information to enhance workload protection. The company needs a solution that simplifies the collection and centralization of security data across multiple AWS accounts and Regions with minimal development effort.

Which solution will meet these requirements with the LEAST development effort?

**Options:**

- Deploy an Amazon RDS cluster and use AWS Database Migration Service (AWS DMS) to load security data from multiple sources.
- **✅ Configure Amazon Security Lake to automatically collect, normalize, and store security data in Amazon S3 for analysis.**
- Use AWS Glue crawlers to extract and catalog security data into an AWS Lake Formation-managed data lake.
- Create a custom Lambda function to fetch security data in JSON format and store it in Amazon S3 for further analysis.

**A:** **Configure Amazon Security Lake to automatically collect, normalize, and store security data in Amazon S3 for analysis.**

**Explanation:**

Amazon Security Lake is purpose-built for centralizing security data. It minimizes development effort by automatically collecting and formatting data into the Open Cybersecurity Schema Framework (OCSF) for analysis.

- **CORRECT:** "Configure Amazon Security Lake to automatically collect, normalize, and store security data in Amazon S3 for analysis" is the correct answer.
- **INCORRECT:** "Use AWS Glue crawlers to extract and catalog security data into an AWS Lake Formation-managed data lake" is incorrect. While this approach helps create a centralized data lake, it requires more development effort to set up the data ingestion pipelines and manage the schema.
- **INCORRECT:** "Deploy an Amazon RDS cluster and use AWS Database Migration Service (AWS DMS) to load security data from multiple sources" is incorrect. DMS is not designed for collecting and normalizing security data. Setting up RDS for this use case introduces unnecessary complexity.
- **INCORRECT:** "Create a custom Lambda function to fetch security data in JSON format and store it in Amazon S3 for further analysis" is incorrect. While possible, this solution requires custom development and ongoing maintenance, making it less efficient than using a managed service like Amazon Security Lake.

**References:**
- https://aws.amazon.com/security-lake
- https://docs.aws.amazon.com/security-lake/latest/userguide/what-is-security-lake.html

---

### Question 26 (S3 Bucket Key / SSE-KMS)

**Q:** A media streaming company stores user activity logs in an Amazon S3 bucket. The logs are accessed frequently for real-time analytics and reporting. The company enforces strict encryption requirements for data stored in S3 and currently uses AWS Key Management Service (AWS KMS) for encryption.

The company wants to reduce costs related to encrypting objects in the S3 bucket while maintaining compliance with its encryption requirements and minimizing the number of AWS KMS calls.

Which solution will meet these requirements?

**Options:**

- Use server-side encryption with customer-provided encryption keys (SSE-C) and store the keys in AWS Secrets Manager.
- Use server-side encryption with Amazon S3 managed keys (SSE-S3) to eliminate AWS KMS usage.
- **✅ Enable S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the objects to reduce the cost of KMS requests.**
- Use client-side encryption with AWS KMS customer-managed keys to encrypt the data before uploading it to S3.

**A:** **Enable S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the objects to reduce the cost of KMS requests.**

**Explanation:**

Enabling S3 Bucket Key reduces the number of AWS KMS calls required for object encryption. S3 Bucket Key caches the encryption keys at the bucket level, significantly lowering the cost of encryption for frequently accessed objects while meeting encryption requirements.

- **CORRECT:** "Enable S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the objects to reduce the cost of KMS requests" is the correct answer.
- **INCORRECT:** "Use server-side encryption with Amazon S3 managed keys (SSE-S3) to eliminate AWS KMS usage" is incorrect. SSE-S3 does not use AWS KMS, but it does not meet the strict encryption requirements specified by the company, which mandate the use of AWS KMS.
- **INCORRECT:** "Use client-side encryption with AWS KMS customer-managed keys to encrypt the data before uploading it to S3" is incorrect. Client-side encryption increases operational complexity and does not optimize costs associated with AWS KMS calls.
- **INCORRECT:** "Use server-side encryption with customer-provided encryption keys (SSE-C) and store the keys in AWS Secrets Manager" is incorrect. SSE-C requires the company to manage its own encryption keys, introducing operational overhead. Additionally, this approach does not optimize costs related to AWS KMS.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-key.html
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html
- https://digitalcloud.training/aws-kms/

---

### Question 28 (VPC PrivateLink Shared Services)

**Q:** A shared services VPC is being setup for use by several AWS accounts. An application needs to be securely shared from the shared services VPC. The solution should not allow consumers to connect to other instances in the VPC.

How can this be setup with the least administrative effort? (Select TWO.)

**Options:**

- **✅ Create a Network Load Balancer (NLB)**
- Configure security groups to restrict access
- Use AWS ClassicLink to expose the application as an endpoint service
- Setup VPC peering between each AWS VPC
- **✅ Use AWS PrivateLink to expose the application as an endpoint service**

**A:** **Create a Network Load Balancer (NLB)** AND **Use AWS PrivateLink to expose the application as an endpoint service**

**Explanation:**

VPCs can be shared among multiple AWS accounts. However, to restrict access so that consumers cannot connect to other instances in the VPC the best solution is to use PrivateLink to create an endpoint for the application. The endpoint type will be an interface endpoint and it uses an NLB in the shared services VPC.

- **CORRECT:** "Create a Network Load Balancer (NLB)" is a correct answer.
- **CORRECT:** "Use AWS PrivateLink to expose the application as an endpoint service" is also a correct answer.
- **INCORRECT:** "Use AWS ClassicLink to expose the application as an endpoint service" is incorrect. ClassicLink allows you to link EC2-Classic instances to a VPC in your account, within the same region. This solution does not include EC2-Classic which is now deprecated (replaced by VPC).
- **INCORRECT:** "Setup VPC peering between each AWS VPC" is incorrect. VPC peering could be used along with security groups to restrict access to the application and other instances in the VPC. However, this would be administratively difficult as you would need to ensure that you maintain the security groups as resources and addresses change.
- **INCORRECT:** "Configure security groups to restrict access" is incorrect. This could be used in conjunction with VPC peering but better method is to use PrivateLink for this use case.

**References:**
- https://aws.amazon.com/about-aws/whats-new/2018/12/amazon-virtual-private-clouds-can-now-be-shared-with-other-aws-accounts/
- https://aws.amazon.com/blogs/networking-and-content-delivery/vpc-sharing-a-new-approach-to-multiple-accounts-and-vpc-management/
- https://d1.awsstatic.com/whitepapers/aws-privatelink.pdf
- https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/

---

### Question 33 (IAM Identity Center – Healthcare)

**Q:** A healthcare startup is building a cloud-based patient management system on AWS. The system processes sensitive health data and uses Amazon RDS for the database, Amazon S3 for storing medical reports, and AWS Lambda for processing event-driven workflows triggered by S3 Event Notifications.

The startup uses AWS IAM Identity Center to manage user authentication. The development, testing, and operations teams need secure access to RDS and S3 while ensuring compliance with healthcare regulations that mandate least privilege access and centralized access control.

Which solution meets these requirements with the LEAST operational overhead?

**Options:**

- Configure an Amazon Cognito user pool to authenticate team members. Use a custom Lambda function to generate temporary credentials for RDS and S3 access. Implement role-based access controls within the Lambda function to enforce least privilege.
- Use AWS Organizations to create separate accounts for development, testing, and operations teams. Apply Service Control Policies (SCPs) to restrict access at the account level. Use cross-account IAM roles to grant granular permissions for RDS and S3 based on team needs.
- **✅ Use AWS IAM Identity Center integrated with the startup's existing Active Directory. Create permission sets with fine-grained permissions for RDS and S3. Assign team members to appropriate groups in Active Directory, which map to Identity Center permission sets.**
- Create separate IAM users for all team members. Assign each user predefined managed policies with RDS and S3 permissions. Use IAM Access Analyzer to review permissions periodically to ensure compliance with least privilege principles.

**A:** **Use AWS IAM Identity Center integrated with the startup's existing Active Directory. Create permission sets with fine-grained permissions for RDS and S3. Assign team members to appropriate groups in Active Directory, which map to Identity Center permission sets.**

**Explanation:**

IAM Identity Center enables centralized user management and integrates seamlessly with Active Directory. This allows permission sets to be mapped directly to AD groups, providing fine-grained, least-privilege access with minimal operational overhead.

- **CORRECT:** "Use AWS IAM Identity Center integrated with the startup's existing Active Directory..." is the correct answer.
- **INCORRECT:** "Configure an Amazon Cognito user pool to authenticate team members. Use a custom Lambda function to generate temporary credentials..." is incorrect. This introduces unnecessary complexity through custom Lambda development.
- **INCORRECT:** "Create separate IAM users for all team members. Assign each user predefined managed policies..." is incorrect. Managing individual IAM users introduces significant operational overhead and is not scalable.
- **INCORRECT:** "Use AWS Organizations to create separate accounts for development, testing, and operations teams. Apply SCPs..." is incorrect. This adds excessive complexity and operational overhead for this use case.

**References:**
- https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html
- https://aws.amazon.com/cognito/
- https://digitalcloud.training/aws-iam/

---

### Question 3 (Kinesis IoT Streaming)

**Q:** An automotive company plans to implement IoT sensors in manufacturing equipment that will send data to AWS in real time. The solution must receive events in an ordered manner from each asset and ensure that data is stored for future processing.

Which solution would be MOST efficient?

**Options:**

- Use an Amazon SQS FIFO queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function for the SQS queue to save data to Amazon EFS.
- **✅ Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3.**
- Use an Amazon SQS standard queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function from the SQS queue to save data to Amazon S3.
- Use Amazon Kinesis Data Streams for real-time events with a shard for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon EBS.

**A:** **Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3.**

**Explanation:**

Amazon Kinesis Data Streams is the ideal service for receiving streaming data. The Amazon Kinesis Client Library (KCL) delivers all records for a given partition key to the same record processor, making it ideal for receiving ordered events per asset. Amazon Kinesis Firehose can be used to receive streaming data from Data Streams and then load the data into Amazon S3 for future processing.

- **CORRECT:** "Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3" is the correct answer.
- **INCORRECT:** "Use Amazon Kinesis Data Streams for real-time events with a shard for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon EBS" is incorrect. A partition should be used per asset (not a shard); also, Kinesis Firehose cannot deliver data to Amazon EBS.
- **INCORRECT:** "Use an Amazon SQS FIFO queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function for the SQS queue to save data to Amazon EFS" is incorrect. Amazon EFS is not a suitable destination for streaming IoT data that requires future bulk processing. SQS is not optimized for high-throughput streaming.
- **INCORRECT:** "Use an Amazon SQS standard queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function from the SQS queue to save data to Amazon S3" is incorrect. Amazon SQS standard queues do not guarantee ordering of messages, which is a key requirement.

**References:**
- https://aws.amazon.com/kinesis/data-streams/faqs/
- https://aws.amazon.com/kinesis/data-firehose/
- https://digitalcloud.training/amazon-kinesis/

---

### Question 4 (Route 53 Geolocation Routing)

**Q:** A company hosts an application on Amazon EC2 instances behind Application Load Balancers in several AWS Regions. Distribution rights for the content require that users in different geographies must be served content from specific AWS Regions.

Which configuration meets these requirements?

**Options:**

- Configure Application Load Balancers with multi-Region routing.
- Configure Amazon CloudFront with multiple origins and AWS WAF.
- Create Amazon Route 53 records with a geoproximity routing policy.
- **✅ Create Amazon Route 53 records with a geolocation routing policy.**

**A:** **Create Amazon Route 53 records with a geolocation routing policy.**

**Explanation:**

Geolocation routing lets you choose the resources that serve your traffic based on the geographic location of your users, meaning the location that DNS queries originate from. When you use geolocation routing, you can localize your content and present some or all of your website in the language of your users. You can also use geolocation routing to restrict distribution of content to only the locations in which you have distribution rights.

- **CORRECT:** "Create Amazon Route 53 records with a geolocation routing policy" is the correct answer.
- **INCORRECT:** "Create Amazon Route 53 records with a geoproximity routing policy" is incorrect. Use this routing policy when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to another.
- **INCORRECT:** "Configure Amazon CloudFront with multiple origins and AWS WAF" is incorrect. AWS WAF protects against web exploits but will not assist with directing users to different content (from different Regions) based on the user's location.
- **INCORRECT:** "Configure Application Load Balancers with multi-Region routing" is incorrect. There is no such thing as multi-Region routing for ALBs.

**References:**
- https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- https://digitalcloud.training/amazon-route-53/

---

### Question 9 (AWS Control Tower Landing Zone)

**Q:** A financial institution with many departments wants to migrate to the AWS Cloud from their data center. Each department should have their own established AWS accounts with preconfigured, limited access to only approved AWS services.

What actions should be taken to ensure compliance with these security requirements?

**Options:**

- **✅ Deploy a Landing Zone within AWS Control Tower. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions to the account.**
- Configure AWS Organizations with SCPs and create new member accounts. Use AWS CloudFormation templates to configure the member account networking.
- Deploy a Landing Zone within AWS Organizations. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions to the account.
- Use AWS CloudFormation to create new member accounts and networking and use IAM roles to allow access to approved AWS services.

**A:** **Deploy a Landing Zone within AWS Control Tower. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions to the account.**

**Explanation:**

AWS Control Tower automates the setup of a new landing zone using best practices blueprints for identity, federated access, and account structure. The account factory automates provisioning of new accounts in your organization. As a configurable account template, it helps you standardize the provisioning of new accounts with pre-approved account configurations.

- **CORRECT:** "Deploy a Landing Zone within AWS Control Tower. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions to the account" is the correct answer.
- **INCORRECT:** "Use AWS CloudFormation to create new member accounts and networking and use IAM roles to allow access to approved AWS services" is incorrect. Although you could perhaps make new AWS Accounts using CloudFormation, it would be a lot of work and difficult to maintain.
- **INCORRECT:** "Configure AWS Organizations with SCPs and create new member accounts. Use AWS CloudFormation templates to configure the member account networking" is incorrect. You can make new accounts in AWS Organizations however there is no Landing Zone feature in Organizations.
- **INCORRECT:** "Deploy a Landing Zone within AWS Organizations. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions to the account" is incorrect. There is no Landing Zone feature within Organizations; this is a Control Tower feature.

**References:**
- https://aws.amazon.com/controltower/

---

### Question 11 (Cross-Region AMI Disaster Recovery)

**Q:** A company's application is running on Amazon EC2 instances in a single Region. In the event of a disaster, a solutions architect needs to ensure that the resources can also be deployed to a second Region.

Which combination of actions should the solutions architect take to accomplish this? (Select TWO.)

**Options:**

- Detach a volume on an EC2 instance and copy it to an Amazon S3 bucket in the second Region
- **✅ Copy an Amazon Machine Image (AMI) of an EC2 instance and specify the second Region for the destination**
- Copy an Amazon Elastic Block Store (Amazon EBS) volume from Amazon S3 and launch an EC2 instance in the second Region using that EBS volume
- Launch a new EC2 instance in the second Region and copy a volume from Amazon S3 to the new instance
- **✅ Launch a new EC2 instance from an Amazon Machine Image (AMI) in the second Region**

**A:** **Copy an Amazon Machine Image (AMI) of an EC2 instance and specify the second Region for the destination** AND **Launch a new EC2 instance from an Amazon Machine Image (AMI) in the second Region**

**Explanation:**

You can copy an Amazon Machine Image (AMI) within or across AWS Regions using the AWS Management Console, the AWS Command Line Interface or SDKs, or the Amazon EC2 API, all of which support the CopyImage action. Using the copied AMI the solutions architect would then be able to launch an instance from the same EBS volume in the second Region. Note: the AMIs are stored on Amazon S3, however you cannot view them in the S3 management console or work with them programmatically using the S3 API.

- **CORRECT:** "Copy an Amazon Machine Image (AMI) of an EC2 instance and specify the second Region for the destination" is a correct answer.
- **CORRECT:** "Launch a new EC2 instance from an Amazon Machine Image (AMI) in the second Region" is also a correct answer.
- **INCORRECT:** "Detach a volume on an EC2 instance and copy it to an Amazon S3 bucket in the second Region" is incorrect. You cannot copy EBS volumes directly from EBS to Amazon S3.
- **INCORRECT:** "Launch a new EC2 instance in the second Region and copy a volume from Amazon S3 to the new instance" is incorrect. You cannot create an EBS volume directly from Amazon S3.
- **INCORRECT:** "Copy an Amazon Elastic Block Store (Amazon EBS) volume from Amazon S3 and launch an EC2 instance in the second Region using that EBS volume" is incorrect. You cannot create an EBS volume from Amazon S3.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html
- https://digitalcloud.training/amazon-ebs/

---

### Question 14 (Cassandra Migration to Keyspaces)

**Q:** A Solutions Architect is migrating a distributed application from their on-premises environment into AWS. This application consists of an Apache Cassandra NoSQL database, with a containerized SUSE Linux compute layer, and a Microsoft SQL Server database as a second storage layer.

Which of the following groups of services will provide the solutions architect with the best solution?

**Options:**

- **✅ Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.**
- Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.
- Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on EC2. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.
- Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon Aurora to host the second storage layer.

**A:** **Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.**

**Explanation:**

Amazon Keyspaces (for Apache Cassandra) is a scalable, highly available, and managed Apache Cassandra–compatible database service. This combined with a containerized, serverless compute layer on Amazon ECS on Fargate (for SUSE Linux containers) and Amazon RDS for Microsoft SQL Server provides the correct fully managed AWS equivalent of each component.

- **CORRECT:** "Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer" is the correct answer.
- **INCORRECT:** "Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on EC2. Use Amazon RDS for Microsoft SQL Server to host the second storage layer" is incorrect. DynamoDB is not a Cassandra-compatible database service. ECS on EC2 requires managing the underlying instances.
- **INCORRECT:** "Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer" is incorrect. DynamoDB is not a Cassandra-compatible database service.
- **INCORRECT:** "Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon Aurora to host the second storage layer" is incorrect. Amazon Aurora does not support Microsoft SQL Server.

**References:**
- https://aws.amazon.com/keyspaces/
- https://digitalcloud.training/category/aws-cheat-sheets/aws-database/

---

### Question 17 (AWS Private 5G)

**Q:** A telecommunications company is looking to expand its 5G coverage nationwide, and as a result needs to provision and build their own private cellular network with the help of AWS.

Which solution does AWS provide to help with this?

**Options:**

- AWS CloudHSM
- AWS Wavelength
- AWS Outposts
- **✅ AWS Private 5G**

**A:** **AWS Private 5G**

**Explanation:**

AWS Private 5G is a managed service that makes it easy to deploy, operate, and scale your own private cellular network, with all required hardware and software provided by AWS.

- **CORRECT:** "AWS Private 5G" is the correct answer.
- **INCORRECT:** "AWS Wavelength" is incorrect. AWS Wavelength embeds AWS compute and storage services within 5G networks, providing mobile edge computing infrastructure for developing, deploying, and scaling applications. It does not help you build your own private cellular network.
- **INCORRECT:** "AWS CloudHSM" is incorrect. AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your own encryption keys on the AWS Cloud and has nothing to do with cellular networks.
- **INCORRECT:** "AWS Outposts" is incorrect. AWS Outposts is a family of fully managed solutions delivering AWS infrastructure and services to virtually any on-premises or edge location for a truly consistent hybrid experience.

**References:**
- https://aws.amazon.com/private5g/

---

### Question 20 (Serverless Image Processing)

**Q:** A company requires a solution to allow customers to customize images that are stored in an online catalog. The image customization parameters will be sent in requests to Amazon API Gateway. The customized image will be generated on-the-fly.

The solutions architect requires a highly available solution. Which solution will be MOST cost-effective?

**Options:**

- Use Amazon EC2 instances to manipulate the original images into the requested customization. Store the original and manipulated images in Amazon S3. Configure an Elastic Load Balancer in front of the EC2 instances.
- Use Amazon EC2 instances to manipulate the original images into the requested customization. Store the original images in Amazon S3 and the manipulated images in Amazon DynamoDB. Configure an Amazon CloudFront distribution.
- **✅ Use AWS Lambda to manipulate the original images to the requested customization. Store the original and manipulated images in Amazon S3. Configure an Amazon CloudFront distribution with the S3 bucket as the origin.**
- Use AWS Lambda to manipulate the original images to the requested customization. Store the original images in Amazon S3 and the manipulated images in Amazon DynamoDB. Configure an Elastic Load Balancer in front of Lambda.

**A:** **Use AWS Lambda to manipulate the original images to the requested customization. Store the original and manipulated images in Amazon S3. Configure an Amazon CloudFront distribution with the S3 bucket as the origin.**

**Explanation:**

All solutions presented are highly available. The key requirement that must be satisfied is that the solution should be cost-effective and you must choose the most cost-effective option. Therefore, it's best to eliminate services such as Amazon EC2 and ELB as these require ongoing costs even when they're not used. Instead, a fully serverless solution should be used. AWS Lambda, Amazon S3, and Amazon CloudFront are all serverless services that scale on demand and only incur costs when used.

- **CORRECT:** "Use AWS Lambda to manipulate the original images to the requested customization. Store the original and manipulated images in Amazon S3. Configure an Amazon CloudFront distribution with the S3 bucket as the origin" is the correct answer.
- **INCORRECT:** "Use Amazon EC2 instances to manipulate the original images... Configure an Elastic Load Balancer in front of the EC2 instances" is incorrect. EC2 and ELB are not serverless and incur costs even when idle.
- **INCORRECT:** "Use AWS Lambda to manipulate the original images... Store the manipulated images in Amazon DynamoDB. Configure an Elastic Load Balancer in front of Lambda" is incorrect. DynamoDB is unsuitable for storing images, and ELB in front of Lambda adds unnecessary cost.
- **INCORRECT:** "Use Amazon EC2 instances to manipulate the original images... Store the manipulated images in Amazon DynamoDB. Configure an Amazon CloudFront distribution" is incorrect. EC2 has ongoing costs and DynamoDB is not suitable for image storage.

**References:**
- https://aws.amazon.com/serverless/
- https://digitalcloud.training/amazon-s3-and-glacier/
- https://digitalcloud.training/aws-lambda/
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 22 (EC2 Hibernate)

**Q:** A company plans to make an Amazon EC2 Linux instance unavailable outside of business hours to save costs. The instance is backed by an Amazon EBS volume. There is a requirement that the contents of the instance's memory (RAM) must be preserved when it is made unavailable.

How can a solutions architect meet these requirements?

**Options:**

- Use Auto Scaling to scale down the instance outside of business hours. Scale up the instance when required.
- **✅ Hibernate the instance outside business hours. Start the instance again when required.**
- Terminate the instance outside business hours. Recover the instance again when required.
- Stop the instance outside business hours. Start the instance again when required.

**A:** **Hibernate the instance outside business hours. Start the instance again when required.**

**Explanation:**

When you hibernate an instance, Amazon EC2 signals the operating system to perform hibernation (suspend-to-disk). Hibernation saves the contents from the instance memory (RAM) to your Amazon Elastic Block Store (Amazon EBS) root volume. On restart:
- The EBS root volume is restored to its previous state
- The RAM contents are reloaded
- The processes that were previously running on the instance are resumed
- Previously attached data volumes are reattached and the instance retains its instance ID

- **CORRECT:** "Hibernate the instance outside business hours. Start the instance again when required" is the correct answer.
- **INCORRECT:** "Stop the instance outside business hours. Start the instance again when required" is incorrect. When an instance is stopped the operating system is shut down and the contents of memory will not be preserved.
- **INCORRECT:** "Use Auto Scaling to scale down the instance outside of business hours. Scale out the instance when required" is incorrect. Auto Scaling scales does not scale up and down, it scales in by terminating instances and out by launching them.
- **INCORRECT:** "Terminate the instance outside business hours. Recover the instance again when required" is incorrect. You cannot recover terminated instances, you can recover instances that have become impaired due to hardware or software issues.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html
- https://digitalcloud.training/amazon-ec2/

---

### Question 40 (AWS WAF IP Blocking)

**Q:** A website runs on Amazon EC2 instances in an Auto Scaling group behind an Application Load Balancer (ALB) which serves as an origin for an Amazon CloudFront distribution. An AWS WAF is being used to protect against SQL injection and cross-site scripting attacks. A review of security logs reveals an attack from a specific IP address.

What should a solutions architect do to protect the application?

**Options:**

- **✅ Modify the configuration of AWS WAF to add an IP match condition to block the malicious IP address**
- Modify the network ACL on the CloudFront distribution to add a deny rule for the malicious IP address
- Modify the security groups for the EC2 instances in the target groups behind the ALB to deny the malicious IP address
- Modify the network ACL for the EC2 instances in the target groups behind the ALB to deny the malicious IP address

**A:** **Modify the configuration of AWS WAF to add an IP match condition to block the malicious IP address**

**Explanation:**

A new version of the AWS Web Application Firewall was released in November 2019. With AWS WAF classic you create "IP match conditions", whereas with AWS WAF (new version) you create "IP set match statements". The IP match condition / IP set match statement inspects the IP address of a web request's origin against a set of IP addresses and address ranges. Use this to allow or block web requests based on the IP addresses that the requests originate from. AWS WAF supports all IPv4 and IPv6 address ranges. An IP set can hold up to 10,000 IP addresses or IP address ranges to check.

- **CORRECT:** "Modify the configuration of AWS WAF to add an IP match condition to block the malicious IP address" is the correct answer.
- **INCORRECT:** "Modify the network ACL on the CloudFront distribution to add a deny rule for the malicious IP address" is incorrect as CloudFront does not sit within a subnet so network ACLs do not apply to it.
- **INCORRECT:** "Modify the network ACL for the EC2 instances in the target groups behind the ALB to deny the malicious IP address" is incorrect as the source IP addresses of the data in the EC2 instances' subnets will be the ELB IP addresses.
- **INCORRECT:** "Modify the security groups for the EC2 instances in the target groups behind the ALB to deny the malicious IP address" is incorrect as you cannot create deny rules with security groups.

**References:**
- https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-ipset-match.html
- https://digitalcloud.training/aws-waf-shield/

---

### Question 64 (EC2 Pricing Models)

**Q:** Amazon EC2 instances in a development environment run between 9am and 5pm Monday-Friday. Production instances run 24/7. Which pricing models should be used to optimize cost and ensure capacity is available when needed? (Select TWO.)

**Options:**

- Use On-Demand instances for the production environment
- Use Spot instances for the development environment
- Use Reserved instances for the development environment
- **✅ Use Reserved instances for the production environment**
- **✅ On-demand capacity reservations for the development environment**

**A:** **Use Reserved instances for the production environment** AND **On-demand capacity reservations for the development environment**

**Explanation:**

Capacity reservations have no commitment and can be created and canceled as needed. This is ideal for the development environment as it will ensure the capacity is available. There is no price advantage, but the capacity is guaranteed during business hours. Reserved instances are a good choice for workloads that run continuously. This is a good option for the production environment.

- **CORRECT:** "On-demand capacity reservations for the development environment" is a correct answer.
- **CORRECT:** "Use Reserved instances for the production environment" is also a correct answer.
- **INCORRECT:** "Use Spot instances for the development environment" is incorrect. Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted. For a development environment that runs during specific business hours, guaranteed capacity is required.
- **INCORRECT:** "Use Reserved instances for the development environment" is incorrect as they require a long-term commitment which is not ideal for a development environment.
- **INCORRECT:** "Use On-Demand instances for the production environment" is incorrect. There is no long-term commitment required when you purchase On-Demand Instances. However, you do not get any discount and for a 24/7 production workload Reserved Instances would be significantly more cost-effective.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/instance-purchasing-options.html
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html
- https://digitalcloud.training/amazon-ec2/

---

### Question 50 (FSx for Windows + DataSync)

**Q:** A large quantity of data is stored on a NAS device on-premises and accessed using the SMB protocol. The company require a managed service for hosting the filesystem and a tool to automate the migration of data from the NAS device.

Which actions should a Solutions Architect take?

**Options:**

- Migrate the data to Amazon EFS using the AWS Server Migration Service (SMS)
- **✅ Migrate the data to Amazon FSx for Windows File Server using AWS DataSync**
- Migrate the data to Amazon S3 using and AWS Snowball Edge device
- Migrate the data to Amazon FSx for Lustre using AWS DataSync

**A:** **Migrate the data to Amazon FSx for Windows File Server using AWS DataSync**

**Explanation:**

Amazon FSx for Windows File Server provides fully managed, highly reliable, and scalable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol. This is the most suitable destination for an SMB-based NAS migration. AWS DataSync can be used to move large amounts of data online between on-premises storage and Amazon S3, Amazon EFS, or Amazon FSx for Windows File Server. The source datastore can be Server Message Block (SMB) file servers.

- **CORRECT:** "Migrate the data to Amazon FSx for Windows File Server using AWS DataSync" is the correct answer.
- **INCORRECT:** "Migrate the data to Amazon EFS using the AWS Server Migration Service (SMS)" is incorrect. EFS is used for hosting filesystems accessed over NFS from Linux (not Windows). The SMS service is used for migrating virtual machines, not data.
- **INCORRECT:** "Migrate the data to Amazon FSx for Lustre using AWS DataSync" is incorrect. Amazon FSx for Windows File Server should be used for hosting SMB shares, not FSx for Lustre.
- **INCORRECT:** "Migrate the data to Amazon S3 using and AWS Snowball Edge device" is incorrect. Amazon S3 is an object store and unsuitable for hosting an SMB filesystem. Snowball is not required in this scenario as DataSync can migrate the data online.

**References:**
- https://aws.amazon.com/fsx/windows/
- https://aws.amazon.com/datasync/features/
- https://digitalcloud.training/amazon-fsx/
- https://digitalcloud.training/aws-migration-services/

---

### Question 4 (EBS Volume Type Selection)

**Q:** A new application will be launched on an Amazon EC2 instance with an Elastic Block Store (EBS) volume. A solutions architect needs to determine the most cost-effective storage option. The application has a variable I/O pattern with an application that requires up to 600 IOPS, on a 200 GiB volume.

Which solution should the solutions architect recommend?

**Options:**

- Amazon EBS Cold HDD (sc1)
- **✅ Amazon EBS General Purpose SSD (gp2)**
- Amazon EBS Provisioned IOPS SSD (io1)
- Amazon EBS Throughput Optimized HDD (st1)

**A:** **Amazon EBS General Purpose SSD (gp2)**

**Explanation:**

General Purpose SSD (gp2) volumes offer cost-effective storage that is ideal for a broad range of workloads. These volumes deliver single-digit millisecond latencies and the ability to burst to 3,000 IOPS for extended periods. Between a minimum of 100 IOPS (at 33.33 GiB and below) and a maximum of 16,000 IOPS (at 5,334 GiB and above), baseline performance scales linearly at 3 IOPS per GiB of volume size. In this case the volume would have a baseline performance of 3 x 200 = 600 IOPS. The volume could also burst to 3,000 IOPS for extended periods. As the I/O varies, this should be suitable.

- **CORRECT:** "Amazon EBS General Purpose SSD (gp2)" is the correct answer.
- **INCORRECT:** "Amazon EBS Provisioned IOPS SSD (io1)" is incorrect as this would be a more expensive option and is not required for the performance characteristics of this workload.
- **INCORRECT:** "Amazon EBS Cold HDD (sc1)" is incorrect as there is no IOPS SLA for HDD volumes and they would likely not perform well enough for this workload.
- **INCORRECT:** "Amazon EBS Throughput Optimized HDD (st1)" is incorrect as there is no IOPS SLA for HDD volumes and they would likely not perform well enough for this workload.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- https://digitalcloud.training/amazon-ebs/

---

### Question 36 (Cost Explorer API)

**Q:** A company is looking for ways to incorporate its current AWS usage expenditure into its operational expense tracking dashboard. A solutions architect has been tasked with proposing a method that enables programmatic access to the cost data.

Which approach would fulfill these needs with the MINIMUM operational burden?

**Options:**

- **✅ Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets.**
- Generate AWS Budgets reports on usage cost data and dispatch the data to the corporation through SMTP.
- Set up AWS Budgets actions to transmit usage cost data to the corporation via FTP.
- Make use of downloadable AWS Cost Explorer report files in the .csv format to access usage cost-related data.

**A:** **Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets.**

**Explanation:**

AWS Cost Explorer API provides programmatic access to AWS cost and usage information. The user can query for aggregated data such as total monthly costs or total daily usage with this API. Also, the Cost Explorer API supports pagination for managing larger data sets, making it efficient for larger queries.

- **CORRECT:** "Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets" is the correct answer.
- **INCORRECT:** "Make use of downloadable AWS Cost Explorer report files in the .csv format to access usage cost-related data" is incorrect. While AWS Cost Explorer does allow you to download .csv reports of your cost data, this method would not be programmatically accessible and would involve manual steps to download and process the data.
- **INCORRECT:** "Set up AWS Budgets actions to transmit usage cost data to the corporation via FTP" is incorrect. AWS Budgets actions allow you to set custom cost and usage budgets that trigger actions (such as turning off EC2 instances) when the budget thresholds you set are breached. However, AWS Budgets does not support transmitting data via FTP.
- **INCORRECT:** "Generate AWS Budgets reports on usage cost data and dispatch the data to the corporation through SMTP" is incorrect. AWS Budgets does not support the dispatching of data through SMTP. AWS Budgets is primarily a tool for setting up alerts on your AWS costs or usage to control your costs, rather than a tool for exporting cost data.

**References:**
- https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_Operations_AWS_Cost_Explorer_Service.html
- https://digitalcloud.training/aws-cost-management/
