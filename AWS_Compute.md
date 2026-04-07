## AWS Services Reference

| Service | Description |
|---|---|
| **Amazon FSx for Windows File Server** | A fully managed native Microsoft Windows file system supporting DFS namespaces and DFS replication. Ideal replacement for on-premises Windows file server farms. |
| **Amazon FSx for Lustre** | A high-performance, fully managed file system optimized for workloads like HPC, ML, video processing, and financial modelling. Integrates seamlessly with Amazon S3. |
| **Amazon EFS (Elastic File System)** | A fully managed, scalable NFS file system for Linux workloads. Supports General Purpose and Max I/O performance modes. Can be mounted across multiple EC2 instances. |
| **Amazon EBS (Elastic Block Store)** | Block-based storage volumes attached to EC2 instances. Not suitable for shared access across multiple instances without manual NFS setup. |
| **Amazon ElastiCache for Redis** | A fully managed in-memory caching service. Supports lazy loading and write-through strategies. Ideal for caching frequently queried, infrequently changing data. |
| **Amazon RDS Read Replicas** | Read-only copies of an RDS database. Can improve read performance but do not provide caching or eliminate repeated identical queries efficiently. |
| **Amazon Aurora Serverless** | An on-demand, auto-scaling configuration for Aurora. Does not have Aurora-specific built-in query caching beyond standard MySQL/PostgreSQL mechanisms. |
| **DynamoDB Accelerator (DAX)** | An in-memory cache for DynamoDB that reduces latency. Not appropriate for caching RDS/SQL queries. |
| **AWS Snowball Edge** | A physical edge computing and storage device for data transfer and processing in locations with limited connectivity. Provides inbuilt compute and storage. |
| **Amazon SQS (Simple Queue Service)** | A fully managed message queuing service. Used for decoupling components. Requires internet connectivity; not suitable for fully offline scenarios. |
| **Amazon Kinesis Data Firehose** | A fully managed service for streaming data delivery to destinations like S3. Not designed for edge/offline data ingestion. |
| **AWS Storage Gateway** | Provides cloud storage solutions for on-premises environments. Requires reliable internet connectivity for data processing. |
| **Amazon RDS SSL/TLS** | Amazon RDS provisions SSL certificates signed by a certificate authority. AWS-provided root certificates can be downloaded for use in encrypted connections. |
| **Amazon CloudWatch Detailed Monitoring** | Provides EC2 metrics at 1-minute intervals (vs. 5-minute for basic). Essential for real-time performance analysis during load testing or peak events. |
| **CloudFront Origin Groups** | Enables origin failover in CloudFront by defining a primary and secondary origin. Improves availability for static content hosted in multiple S3 regions. |
| **AWS Lambda + API Gateway** | A serverless compute pattern for microservices backends. Eliminates server management and scales automatically. |
| **Amazon Aurora Serverless** | An auto-scaling, serverless relational database. Scales capacity up/down based on application needs with no idle cost. |
| **Amazon SQS (Decoupled Scaling)** | SQS queues allow Auto Scaling groups to scale independently based on queue depth, decoupling ingestion from processing. |
| **IAM Roles Anywhere** | Enables workloads outside AWS (e.g., on-premises) to obtain temporary AWS credentials using X.509 certificates, avoiding long-term credential storage. |
| **EMR Runtime Roles** | IAM roles used per-job in Amazon EMR to enforce fine-grained, per-department permissions within a shared cluster. |
| **AWS Batch** | A fully managed service for running batch computing jobs. Automatically provisions and scales compute resources. Supports multi-node parallel jobs for HPC/MPI workloads. |
| **AWS Step Functions** | A serverless workflow orchestration service. Integrates with AWS Batch, Lambda, and other services to manage job pipelines with minimal operational overhead. |
| **EC2 Auto Scaling (SQS-based)** | Scales EC2 instances in an Auto Scaling group based on Amazon SQS queue depth metrics. Effective for processing-bound, queue-driven architectures. |
| **AWS Secrets Manager** | Stores and automatically rotates secrets (e.g., database credentials) on a configurable schedule. Integrates natively with RDS/Aurora. |
| **AWS Systems Manager Parameter Store** | Stores configuration data and secrets as SecureString parameters. Rotation requires a custom Lambda function; less integrated than Secrets Manager for DB credentials. |
| **Amazon Cognito** | A user identity and access service. Not designed for database credential generation or rotation. |
| **EC2 Auto Scaling Scheduled Action** | Sets desired, minimum, or maximum capacity at a scheduled time. Useful when load is predictable. Setting desired capacity is more cost-effective than setting min/max to the same value. |
| **Amazon EFS General Purpose Mode** | The default EFS performance mode; suitable for most workloads requiring shared file access across multiple EC2 instances with low latency. |
| **Amazon VPC CNI Plugin for Kubernetes** | Allows EKS pods to use VPC-native IP addresses from custom subnets. Required for assigning pods to specific subnets within a VPC. |
| **AWS Global Accelerator** | Improves availability and performance for global applications using the AWS global network and static anycast IPs. Supports UDP and TCP. Enables deterministic routing and automatic failover. |
| **Amazon CloudFront Custom Error Pages** | Allows CloudFront to serve custom HTML error pages when origin errors occur, reducing operational intervention for transient failures. |
| **Amazon Route 53 Failover Routing** | Active-passive failover routing using health checks. Less operationally efficient than CloudFront for handling origin errors on-the-fly. |
| **AWS PrivateLink** | Enables private connectivity between VPCs using a service-provider model with a Network Load Balancer in the provider VPC and an endpoint in the consumer VPC. |
| **Amazon API Gateway + Kinesis Firehose** | A scalable, serverless pattern for ingesting survey/event data. Firehose buffers and delivers data to S3; Lambda/Comprehend processes it asynchronously. |
| **Amazon Redshift + Redshift Spectrum** | A petabyte-scale data warehouse with Spectrum enabling SQL queries over structured (Redshift) and semi-structured/unstructured (S3) data simultaneously. |
| **Amazon MQ** | A managed message broker for Apache ActiveMQ and RabbitMQ. Supports active/standby configurations across AZs. For new cloud-native apps, SQS/SNS are preferred. |
| **Amazon SNS** | A fully managed pub/sub messaging service. Supports Lambda as a subscriber, enabling asynchronous, decoupled invocation of Lambda from EC2. |
| **AWS AppSync** | A fully managed GraphQL and Pub/Sub API service. Provides a single endpoint to query/update data across multiple backends (databases, microservices, APIs). |
| **AWS Lake Formation** | A service for building secure, centralized data lakes. Ingests and catalogues structured and unstructured data from existing cloud storage for ML and analytics. |
| **AWS Systems Manager Session Manager** | Provides secure, auditable, browser-based shell access to EC2 instances without SSH keys or open inbound ports. Integrates with IAM Identity Center for centralized access. |
| **Aurora Global Database** | Spans multiple AWS Regions with sub-second replication. Supports RPO of 1 second and RTO of under 1 minute. Ideal for business-critical, multi-region DR. |
| **Network Load Balancer + Global Accelerator** | The recommended pattern for low-latency, UDP-based global applications. NLB handles regional traffic; Global Accelerator routes to the optimal region via the AWS backbone. |
| **Virtual Private Gateway (VPG)** | Used to set up an AWS VPN over Direct Connect to provide IPsec encryption for data traversing the Direct Connect link. |
| **AWS Direct Connect Gateway** | Connects multiple VPCs across regions to on-premises via Direct Connect. Not involved with encryption. |
| **S3 Client-Side Encryption (Customer Managed Keys)** | Encrypts data before it leaves the client. The customer controls the encryption keys entirely, ensuring data is never sent to AWS unencrypted. |
| **S3 Object Lock (Compliance Mode)** | Prevents objects from being deleted or modified by any user, including root, for the duration of the retention period. Used for regulatory WORM requirements. |
| **Amazon EC2 Scheduled Reserved Instances** | Reserved capacity for specific recurring time windows (e.g., every Monday for 8 hours). Cost-effective for predictable, time-bounded workloads. |
| **Standard Reserved Instances** | Provide a significant discount for instances running continuously. Best for steady-state, always-on workloads. |
| **Amazon ECS Anywhere** | Enables running ECS tasks on on-premises infrastructure using the "external" launch type. Cloud tasks use Fargate; on-premises tasks use ECS Anywhere. |
| **Application Load Balancer (ALB)** | Best suited for HTTP/HTTPS traffic routing. Appropriate for ECS-based cloud services handling web traffic. |
| **Network Load Balancer (NLB)** | Handles TCP/UDP traffic at ultra-low latency. Used with AWS PrivateLink and Global Accelerator. Not appropriate for HTTP-only ECS services. |
| **AWS Direct Connect + Transit Gateway** | Associate a Direct Connect gateway with a transit gateway to share Direct Connect connections across multiple VPCs in the same region. |
| **DynamoDB Streams + Lambda** | Captures a time-ordered sequence of item-level changes in DynamoDB and triggers Lambda to process and store them (e.g., in S3) for compliance. |
| **CloudFront OAI + WAF** | An OAI restricts S3 bucket access to CloudFront only; WAF web ACLs on the CloudFront distribution enforce IP-based access restrictions. |
| **Bastion Host (NLB + ASG)** | The recommended pattern for resilient bastion host architectures: an NLB distributes connections to an Auto Scaling group of bastion instances across multiple AZs. |
| **Amazon EMR Runtime Roles** | Scoped IAM roles assigned per EMR job submission to enforce per-team/department granular permissions on shared clusters. |

---

## AWS Compute – Practice Questions

---

### Question 6 (Windows File Server Migration – Amazon FSx)

**Q:** A Microsoft Windows file server farm uses Distributed File System Replication (DFSR) to synchronize data in an on-premises environment. The infrastructure is being migrated to the AWS Cloud.

Which service should the solutions architect use to replace the file server farm?

**Options:**

- Amazon EFS
- AWS Storage Gateway
- Amazon EBS
- **✅ Amazon FSx**

**A:** **Amazon FSx**

**Explanation:**

Amazon FSx for Windows file server supports DFS namespaces and DFS replication. This is the best solution for replacing the on-premises infrastructure.

- **CORRECT:** "Amazon FSx" is the correct answer.
- **INCORRECT:** "Amazon EFS" is incorrect. You cannot replace a Windows file server farm with EFS as it uses a completely different protocol.
- **INCORRECT:** "Amazon EBS" is incorrect. Amazon EBS provides block-based volumes that are attached to EC2 instances. It cannot be used for replacing a shared Windows file server farm using DFSR.
- **INCORRECT:** "AWS Storage Gateway" is incorrect. This service is used for providing cloud storage solutions for on-premises servers. In this case the infrastructure is being migrated into the AWS Cloud.

**References:**
- https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html
- https://digitalcloud.training/amazon-fsx/

---

### Question 13 (Movie Streaming Catalog – ElastiCache Redis)

**Q:** A startup is prototyping a movie streaming platform on AWS. The platform consists of an Application Load Balancer, an Auto Scaling group of Amazon EC2 instances to host the frontend, and an Amazon RDS database to store the movie catalog.

Users report slow response times when browsing the catalog of available movies. The movie catalog is a set of tables in the database that is updated infrequently. A solutions architect finds that catalog queries are causing high read load on the database.

What should the solutions architect recommend to improve the performance of the platform during catalog searches?

**Options:**

- **✅ Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache.**
- Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas.
- Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora's built-in caching to handle frequent queries efficiently.
- Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog.

**A:** **Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache.**

**Explanation:**

ElastiCache provides a high-performance, in-memory caching layer. With lazy loading, the cache is only populated on a cache miss, reducing unnecessary writes and keeping the cache data relevant. Since the catalog is updated infrequently, cached data remains valid for extended periods.

- **CORRECT:** "Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache" is the correct answer.
- **INCORRECT:** "Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog" is incorrect because migrating to DynamoDB introduces unnecessary migration complexity and cost for an existing RDS workload.
- **INCORRECT:** "Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas" is incorrect because while read replicas can improve performance, they do not eliminate repeated identical queries and add complexity to query distribution.
- **INCORRECT:** "Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora's built-in caching to handle frequent queries efficiently" is incorrect because switching to Aurora Serverless introduces migration overhead and Aurora does not provide a dedicated query result cache beyond standard MySQL/PostgreSQL mechanisms.

**References:**
- https://aws.amazon.com/elasticache/
- https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
- https://digitalcloud.training/amazon-elasticache/

---

### Question 21 (Drone Surveying – AWS Snowball Edge)

**Q:** A surveying team is using a fleet of drones to collect images of construction sites. The surveying team's laptops lack the inbuilt storage and compute capacity to transfer the images and process them. The team has intermittent connectivity.

What should a solutions architect recommend?

**Options:**

- Configure Amazon Kinesis Data Firehose to create multiple delivery streams aimed separately at the S3 buckets for storage and the EC2 instances for processing the images.
- During intermittent connectivity to EC2 instances, upload images to Amazon SQS.
- **✅ Process and store the images using AWS Snowball Edge devices.**
- Cache the images locally on a hardware appliance pre-installed with AWS Storage Gateway to process the images when connectivity is restored.

**A:** **Process and store the images using AWS Snowball Edge devices.**

**Explanation:**

An AWS physical Snowball Edge device will provide much more inbuilt compute and storage compared to the current team's laptops. This negates the need to rely on a stable connection to process any images.

- **CORRECT:** "Process and store the images using AWS Snowball Edge devices" is the correct answer.
- **INCORRECT:** "During intermittent connectivity to EC2 instances, upload images to Amazon SQS" is incorrect as you would still need a reliable internet connection to upload any images to Amazon SQS.
- **INCORRECT:** "Configure Amazon Kinesis Data Firehose to create multiple delivery streams aimed separately at the S3 buckets for storage and the EC2 instances for processing the images" is incorrect as Kinesis Firehose requires a reliable internet connection and is a cloud-based streaming service.
- **INCORRECT:** "Cache the images locally on a hardware appliance pre-installed with AWS Storage Gateway to process the images when connectivity is restored" is incorrect as you would still need reliable connectivity to process images via the gateway.

**References:**
- https://docs.aws.amazon.com/snowball/latest/developer-guide/whatisedge.html
- https://digitalcloud.training/aws-migration-services/

---

### Question 24 (RDS Encryption in Transit – SSL Certificates)

**Q:** A company uses an Amazon RDS MySQL database instance to store customer order data. The security team have requested that SSL/TLS encryption in transit must be used for encrypting connections to the RDS instance.

How can a Solutions Architect enable encryption in transit?

**Options:**

- **✅ Download the AWS-provided root certificates. Use the certificates when connecting to the RDS DB instance.**
- Add a self-signed certificate to the RDS DB instance. Use the certificates in all connections to the RDS DB instance.
- Enable encryption in transit using the RDS Management console and obtain a key using AWS KMS.
- Take a snapshot of the RDS instance. Restore the snapshot to a new instance with encryption in transit enabled.

**A:** **Download the AWS-provided root certificates. Use the certificates when connecting to the RDS DB instance.**

**Explanation:**

Amazon RDS creates an SSL certificate and installs the certificate on the DB instance when Amazon RDS provisions the instance. These certificates are signed by a certificate authority. You can download a root certificate from AWS that works for all Regions or you can download Region-specific intermediate certificates.

- **CORRECT:** "Download the AWS-provided root certificates. Use the certificates when connecting to the RDS DB instance" is the correct answer.
- **INCORRECT:** "Take a snapshot of the RDS instance. Restore the snapshot to a new instance with encryption in transit enabled" is incorrect. There is no need to do this as a certificate is created when the instance is provisioned.
- **INCORRECT:** "Enable encryption in transit using the RDS Management console and obtain a key using AWS KMS" is incorrect. You cannot enable/disable encryption in transit using the RDS management console.
- **INCORRECT:** "Add a self-signed certificate to the RDS DB instance. Use the certificates in all connections to the RDS DB instance" is incorrect. You cannot use self-signed certificates with RDS.

**References:**
- https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.SSL.html
- https://digitalcloud.training/amazon-rds/

---

### Question 27 (Annual Load Event Monitoring – CloudWatch Detailed Monitoring)

**Q:** A retail company operates a multi-tier application that includes a web server layer running on Amazon EC2 instances and a database layer hosted on Amazon RDS. The company is preparing for an annual sales event that typically causes a significant spike in traffic. The company wants to monitor the performance of both layers in real time with 1-minute intervals to proactively identify and resolve bottlenecks.

What should the solutions architect do to meet this requirement?

**Options:**

- Configure Amazon CloudWatch Logs Insights to aggregate application logs for both the EC2 instances and Amazon RDS. Use Amazon QuickSight for detailed visualization.
- Configure an Amazon CloudWatch Events rule to trigger an AWS Lambda function that collects custom metrics from the EC2 instances and Amazon RDS. Use Amazon CloudWatch dashboards to display the metrics.
- Use AWS Systems Manager to collect logs from the EC2 instances and Amazon RDS. Store the logs in Amazon S3 and use Amazon Athena to query performance data.
- **✅ Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics for analysis.**

**A:** **Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics for analysis.**

**Explanation:**

Detailed monitoring provides metrics at 1-minute intervals, which is critical for identifying bottlenecks during high-traffic events. CloudWatch natively supports EC2 and RDS metrics and enables real-time dashboards with minimal overhead.

- **CORRECT:** "Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics for analysis" is the correct answer.
- **INCORRECT:** "Configure Amazon CloudWatch Logs Insights to aggregate application logs for both the EC2 instances and Amazon RDS. Use Amazon QuickSight for detailed visualization" is incorrect because while useful for log analysis, this does not provide real-time infrastructure performance metrics at 1-minute granularity.
- **INCORRECT:** "Configure an Amazon CloudWatch Events rule to trigger an AWS Lambda function that collects custom metrics from the EC2 instances and Amazon RDS. Use Amazon CloudWatch dashboards to display the metrics" is incorrect because this adds unnecessary complexity; CloudWatch already collects EC2 metrics natively with detailed monitoring enabled.
- **INCORRECT:** "Use AWS Systems Manager to collect logs from the EC2 instances and Amazon RDS. Store the logs in Amazon S3 and use Amazon Athena to query performance data" is incorrect because this solution introduces latency in analysis and is more suited for historical log querying, not real-time performance monitoring.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch.html
- https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html
- https://digitalcloud.training/amazon-cloudwatch/

---

### Question 37 (CloudFront Multi-Region S3 Availability)

**Q:** An Amazon S3 bucket in the us-east-1 Region hosts the static website content of a company. The content is made available through an Amazon CloudFront origin pointing to that bucket. A second copy of the content exists in an S3 bucket in ap-southeast-1.

Which combination of actions should a solutions architect take to increase availability? (Select TWO.)

**Options:**

- **✅ Using us-east-1 bucket as the primary bucket and ap-southeast-1 bucket as the secondary bucket, create a CloudFront origin group.**
- Create an origin for CloudFront for both buckets.
- Set up failover routing in Amazon Route 53.
- **✅ Add an origin for ap-southeast-1 to CloudFront.**
- Point Amazon Route 53 to the replica bucket by creating a record.

**A:** **Add an origin for ap-southeast-1 to CloudFront** AND **Using us-east-1 bucket as the primary bucket and ap-southeast-1 bucket as the secondary bucket, create a CloudFront origin group.**

**Explanation:**

You can set up CloudFront with origin failover for scenarios that require high availability. To get started, you create an origin group with two origins: a primary and a secondary. If the primary origin is unavailable, CloudFront automatically routes requests to the secondary origin.

- **CORRECT:** "Add an origin for ap-southeast-1 to CloudFront" is the correct answer.
- **CORRECT:** "Using us-east-1 bucket as the primary bucket and ap-southeast-1 bucket as the secondary bucket, create a CloudFront origin group" is also a correct answer.
- **INCORRECT:** "Create an origin for CloudFront for both buckets" is incorrect. This would not increase the availability of the solution on its own without configuring an origin group.
- **INCORRECT:** "Set up failover routing in Amazon Route 53" is incorrect as we are trying to enable failover in CloudFront and using Route 53 is for routing domain names.
- **INCORRECT:** "Point Amazon Route 53 to the replica bucket by creating a record" is incorrect as we are trying to enable failover in CloudFront and using Route 53 is for routing domain names.

**References:**
- https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 42 (Serverless Microservices Migration – S3 + Lambda + Aurora)

**Q:** A company has developed a non-production application that is composed of multiple microservices for each of the company's business units. A single development team maintains all the microservices. The application uses a relational database and has a static web frontend. The team wants to migrate the application to AWS while minimizing operational overhead.

Which solution will meet these requirements?

**Options:**

- Use Amazon CloudFront and AWS Amplify to host the static web frontend. Refactor the backend to AWS Lambda functions triggered by an EventBridge bus. Migrate the database to an Amazon EC2 Reserved Instance.
- Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend microservices to run on Amazon ECS on AWS Fargate. Migrate the database to Amazon DynamoDB for auto-scaling.
- **✅ Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend to use AWS Lambda functions that are invoked by Amazon API Gateway. Migrate the database to Amazon Aurora Serverless.**
- Use AWS Amplify to host the static web frontend. Refactor the backend microservices to Amazon Elastic Kubernetes Service (Amazon EKS) with auto-scaling. Migrate the database to Amazon RDS for MySQL.

**A:** **Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend to use AWS Lambda functions that are invoked by Amazon API Gateway. Migrate the database to Amazon Aurora Serverless.**

**Explanation:**

S3 and CloudFront provide secure, globally available hosting for the static frontend. AWS Lambda and API Gateway eliminate server management, and Aurora Serverless offers automatic scaling for the relational database without managing instances.

- **CORRECT:** "Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend to use AWS Lambda functions that are invoked by Amazon API Gateway. Migrate the database to Amazon Aurora Serverless" is the correct answer.
- **INCORRECT:** "Use AWS Amplify to host the static web frontend. Refactor the backend microservices to Amazon EKS with auto-scaling. Migrate the database to Amazon RDS for MySQL" is incorrect because using Amazon EKS adds operational complexity.
- **INCORRECT:** "Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend microservices to run on Amazon ECS on AWS Fargate. Migrate the database to Amazon DynamoDB for auto-scaling" is incorrect because moving a relational database to DynamoDB requires a complete redesign, which increases migration complexity and effort.
- **INCORRECT:** "Use Amazon CloudFront and AWS Amplify to host the static web frontend. Refactor the backend to AWS Lambda functions triggered by an EventBridge bus. Migrate the database to an Amazon EC2 Reserved Instance" is incorrect because EventBridge adds unnecessary complexity and hosting a database on EC2 increases operational overhead.

**References:**
- https://aws.amazon.com/s3/
- https://aws.amazon.com/rds/aurora/serverless/

---

### Question 44 (Real-Time Vehicle Sensor Data – SQS Decoupled Scaling)

**Q:** A logistics company processes real-time sensor data from delivery vehicles to optimize routes and track vehicle health. The current architecture includes an Auto Scaling group of Amazon EC2 instances for data ingestion and another for route analysis. The company has observed performance issues during peak delivery hours when the rate of data ingestion is significantly higher than the analysis and processing rate. The company wants to ensure that no data is lost during peak hours.

Which solution will meet these requirements?

**Options:**

- **✅ Use two Amazon Simple Queue Service (Amazon SQS) queues: one for data ingestion and one for route analysis. Configure the EC2 instances to poll their respective queues and scale the Auto Scaling groups independently based on queue depth.**
- Replace the EC2-based Auto Scaling groups with AWS Lambda functions to process the incoming data and analysis tasks. Use Amazon DynamoDB to store the intermediate data and scale DynamoDB based on demand.
- Use two Amazon SQS queues: one for data ingestion and one for route analysis. Configure Amazon EventBridge rules to monitor queue length and scale each Auto Scaling group based on the backlog of messages.
- Use Amazon Kinesis Data Streams to buffer the sensor data. Configure Amazon Kinesis Data Analytics to process the data and adjust the number of EC2 instances in the analysis Auto Scaling group based on stream metrics.

**A:** **Use two Amazon SQS queues: one for data ingestion and one for route analysis. Configure the EC2 instances to poll their respective queues and scale the Auto Scaling groups independently based on queue depth.**

**Explanation:**

Using two SQS queues decouples the ingestion and analysis tiers, ensuring data is buffered and not lost during peak hours. Each Auto Scaling group can scale independently based on its queue depth, which is a native CloudWatch metric for SQS.

- **CORRECT:** "Use two Amazon SQS queues with Auto Scaling groups scaled by queue depth" is the correct answer.
- **INCORRECT:** "Replace the EC2-based Auto Scaling groups with AWS Lambda functions" is incorrect because Lambda has a maximum execution time of 15 minutes and may not be suitable for long-running vehicle analysis tasks.
- **INCORRECT:** "Use Amazon Kinesis Data Streams with Kinesis Data Analytics" is incorrect because while Kinesis can buffer data, scaling EC2 instances based on Kinesis stream metrics adds operational complexity compared to SQS-based scaling.
- **INCORRECT:** "Use two SQS queues with EventBridge rules to scale" is incorrect because EventBridge rules for monitoring SQS queue length and triggering scaling actions add unnecessary complexity compared to native SQS-based Auto Scaling policies.

**References:**
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 47 (On-Premises S3 Access – IAM Roles Anywhere)

**Q:** A financial services company stores transaction records in an Amazon S3 bucket. The company runs its analytics application on a cluster of on-premises servers. The application needs temporary, secure access to the S3 bucket.

The company uses AWS IAM Identity Center to manage identities and ensure adherence to the principle of least privilege. The solution must avoid long-term credential storage and provide a secure mechanism for on-premises workloads to access AWS resources.

Which solution will meet these requirements?

**Options:**

- Use AWS Systems Manager to store an access key and secret key for an IAM user with access to the S3 bucket. Configure the application to retrieve the credentials from Systems Manager Parameter Store.
- Create an S3 bucket policy to allow access from the public IP address range of the company's on-premises servers. Configure the application to access the S3 bucket directly.
- Deploy AWS Storage Gateway File Gateway to the on-premises environment. Configure the application to access the S3 bucket through the gateway by using NFS or SMB.
- **✅ Use IAM Roles Anywhere to issue temporary credentials to the application. Set up a trust relationship with IAM Identity Center and configure the application to assume the role using these credentials.**

**A:** **Use IAM Roles Anywhere to issue temporary credentials to the application. Set up a trust relationship with IAM Identity Center and configure the application to assume the role using these credentials.**

**Explanation:**

IAM Roles Anywhere enables on-premises workloads to obtain temporary AWS credentials using X.509 certificates without long-term credential storage. This aligns with the principle of least privilege and eliminates the risk of static credential exposure.

- **CORRECT:** "Use IAM Roles Anywhere to issue temporary credentials to the application" is the correct answer.
- **INCORRECT:** "Create an S3 bucket policy to allow access from the public IP address range of the company's on-premises servers" is incorrect because IP-based policies are difficult to manage and do not follow the principle of least privilege.
- **INCORRECT:** "Deploy AWS Storage Gateway File Gateway" is incorrect because while it provides S3 access via NFS/SMB, it does not address the credential security requirement and introduces additional infrastructure.
- **INCORRECT:** "Use AWS Systems Manager to store an access key and secret key for an IAM user" is incorrect because this stores long-term credentials, which violates the requirement to avoid long-term credential storage.

**References:**
- https://docs.aws.amazon.com/rolesanywhere/latest/userguide/introduction.html
- https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html
- https://digitalcloud.training/aws-iam/

---

### Question 51 (Shared EMR Cluster – Runtime Roles)

**Q:** A research organization wants to set up an Amazon EMR cluster for multiple departments to run their big data analytics jobs. The organization needs to ensure that each department's workloads can only access the data they are authorized to use, even though they share the same cluster.

Which solution will meet these requirements?

**Options:**

- Configure VPC interface endpoints for each AWS service that the departments require. Route traffic from the big data workloads through these VPC endpoints.
- Create an EMR security configuration that disables access to the Instance Metadata Service. Use this security configuration with application-specific IAM roles to submit the workloads.
- Assign unique EC2 IAM instance profiles to each team's workloads. Configure the instance profiles with the specific permissions needed for each department.
- **✅ Use EMR runtime roles to enforce granular permissions for each department's workloads. Configure the EMR cluster to use these roles when submitting jobs.**

**A:** **Use EMR runtime roles to enforce granular permissions for each department's workloads. Configure the EMR cluster to use these roles when submitting jobs.**

**Explanation:**

EMR runtime roles are IAM roles assumed per job submission, allowing fine-grained, per-department permissions on a shared cluster. This is the recommended AWS approach for multi-tenant EMR environments.

- **CORRECT:** "Use EMR runtime roles to enforce granular permissions for each department's workloads" is the correct answer.
- **INCORRECT:** "Configure VPC interface endpoints for each AWS service" is incorrect because VPC endpoints control network routing, not per-workload data access permissions within a shared cluster.
- **INCORRECT:** "Assign unique EC2 IAM instance profiles to each team's workloads" is incorrect because instance profiles apply at the instance level, not the job level, and cannot be scoped per job on a shared cluster.
- **INCORRECT:** "Create an EMR security configuration that disables access to the Instance Metadata Service" is incorrect because disabling IMDS prevents jobs from using instance-level credentials but does not provide per-department granular access control.

**References:**
- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-iam-roles.html
- https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-security-configuration.html
- https://digitalcloud.training/amazon-emr/

---

### Question 60 (Video Processing – AWS Batch + Step Functions)

**Q:** A media processing company is migrating its on-premises application to the AWS Cloud. The application processes high volumes of videos and generates large output files during the workflow.

The company requires a scalable solution to handle an increasing number of video processing jobs. The solution should minimize manual intervention, simplify job orchestration, and eliminate the need to manage underlying infrastructure.

Which solution will fulfill these requirements with the LEAST operational overhead?

**Options:**

- Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate to process the videos. Use Amazon Simple Queue Service (Amazon SQS) for workflow orchestration and store the processed files in Amazon S3.
- **✅ Use AWS Batch to run video processing jobs. Use AWS Step Functions to manage the workflow. Store the processed files in Amazon S3.**
- Use AWS Lambda and Amazon EC2 On-Demand Instances for video processing. Store the processed files in Amazon FSx for Lustre.
- Use a fleet of Amazon EC2 Spot Instances to process the videos. Use AWS Step Functions for workflow management and store the processed files in Amazon Elastic File System (Amazon EFS).

**A:** **Use AWS Batch to run video processing jobs. Use AWS Step Functions to manage the workflow. Store the processed files in Amazon S3.**

**Explanation:**

AWS Batch automatically manages the underlying compute infrastructure, scaling resources based on the number of jobs. Step Functions orchestrates the workflow with retries, branching, and state management. S3 provides durable, scalable storage for output files.

- **CORRECT:** "Use AWS Batch to run video processing jobs. Use AWS Step Functions to manage the workflow. Store the processed files in Amazon S3" is the correct answer.
- **INCORRECT:** "Use Amazon ECS with AWS Fargate. Use Amazon SQS for workflow orchestration" is incorrect because SQS is a messaging queue, not a workflow orchestration service. It lacks the state management and retry logic of Step Functions.
- **INCORRECT:** "Use AWS Lambda and Amazon EC2 On-Demand Instances for video processing. Store the processed files in Amazon FSx for Lustre" is incorrect because combining Lambda with EC2 adds complexity, and FSx for Lustre is optimized for HPC rather than general video output storage.
- **INCORRECT:** "Use a fleet of Amazon EC2 Spot Instances. Use AWS Step Functions for workflow management. Store the processed files in Amazon EFS" is incorrect because managing a fleet of Spot Instances requires significant operational overhead compared to AWS Batch.

**References:**
- https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html
- https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html

---

### Question 61 (eCommerce SQS Queue Depth Scaling)

**Q:** An eCommerce application consists of three tiers. The web tier includes EC2 instances behind an Application Load Balancer, the middle tier uses EC2 instances and an Amazon SQS queue to process orders, and the backend tier is an Amazon DynamoDB table. Order processing is taking too long during peak periods.

Which action will be MOST effective in accomplishing this requirement?

**Options:**

- **✅ Use Amazon EC2 Auto Scaling to scale out the middle tier instances based on the SQS queue depth.**
- Replace the Amazon SQS queue with Amazon Kinesis Data Firehose.
- Use Amazon DynamoDB Accelerator (DAX) in front of the DynamoDB backend tier.
- Add an Amazon CloudFront distribution with a custom origin to cache the responses for the web tier.

**A:** **Use Amazon EC2 Auto Scaling to scale out the middle tier instances based on the SQS queue depth.**

**Explanation:**

The most likely cause of the processing delays is insufficient instances in the middle tier where the order processing takes place. The most effective solution to reduce processing times is to scale out the middle tier EC2 instances based on the SQS queue depth metric.

- **CORRECT:** "Use Amazon EC2 Auto Scaling to scale out the middle tier instances based on the SQS queue depth" is the correct answer.
- **INCORRECT:** "Replace the Amazon SQS queue with Amazon Kinesis Data Firehose" is incorrect. The issue is not the efficiency of queuing messages but the processing of the messages.
- **INCORRECT:** "Use Amazon DynamoDB Accelerator (DAX) in front of the DynamoDB backend tier" is incorrect. The DynamoDB table is configured with Auto Scaling so this is not likely to be the bottleneck.
- **INCORRECT:** "Add an Amazon CloudFront distribution with a custom origin to cache the responses for the web tier" is incorrect. This will cache media files to speed up web response times but not order processing.

**References:**
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
- https://digitalcloud.training/amazon-ec2-auto-scaling/

---

### Question 6 (Aurora Credential Rotation – Secrets Manager)

**Q:** A gaming company operates a leaderboard application for a popular multiplayer game. The application uses an Amazon Aurora PostgreSQL DB cluster for storage. The game servers are hosted on Amazon EC2 instances.

The company has a strict security policy that requires database credentials to be encrypted and rotated every 30 days. The company wants to minimize operational overhead while ensuring the application can retrieve the latest credentials automatically.

What should a solutions architect do to meet this requirement?

**Options:**

- Use AWS Systems Manager Parameter Store to store the database credentials as SecureString parameters encrypted with AWS KMS. Implement a custom AWS Lambda function to rotate the credentials every 30 days.
- **✅ Use AWS Secrets Manager to store the database credentials. Configure Secrets Manager to rotate the credentials automatically every 30 days. Update the game server application to retrieve credentials from Secrets Manager at runtime.**
- Configure Amazon Cognito to generate temporary database credentials. Use Cognito's built-in mechanisms to rotate the credentials every 30 days. Update the game server application to request temporary credentials from Cognito.
- Store the database credentials in an Amazon DynamoDB table encrypted with AWS KMS. Configure an AWS Lambda function to rotate the credentials in Aurora every 30 days and update the DynamoDB table.

**A:** **Use AWS Secrets Manager to store the database credentials. Configure Secrets Manager to rotate the credentials automatically every 30 days. Update the game server application to retrieve credentials from Secrets Manager at runtime.**

**Explanation:**

AWS Secrets Manager natively integrates with Amazon Aurora to automatically rotate database credentials on a configurable schedule. The application retrieves the latest credentials at runtime via the Secrets Manager API, with no manual intervention required.

- **CORRECT:** "Use AWS Secrets Manager" is the correct answer.
- **INCORRECT:** "Use AWS Systems Manager Parameter Store" is incorrect because while Parameter Store supports SecureString, it does not natively rotate RDS credentials. A custom Lambda function increases operational overhead.
- **INCORRECT:** "Configure Amazon Cognito" is incorrect because Cognito is a user identity service and is not designed for database credential generation or rotation.
- **INCORRECT:** "Store credentials in DynamoDB with a Lambda rotation function" is incorrect because this is a custom implementation that introduces significant operational overhead compared to Secrets Manager's native rotation.

**References:**
- https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html
- https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html
- https://digitalcloud.training/aws-secrets-manager/

---

### Question 10 (Predictable Business Hours Scaling – Scheduled Action)

**Q:** A company runs an internal application for logging customer support information. The application runs on Amazon EC2 instances in an Auto Scaling group. The ASG scales up to 10 instances during business hours and scales back down to 2 instances after hours. The application experiences performance issues at the start of business hours because it takes too long to scale up.

How should a Solutions Architect configure the Auto Scaling group to resolve the performance issues whilst minimizing costs?

**Options:**

- Implement a scheduled action that sets the minimum and maximum capacity to 10 before business hours begin.
- **✅ Implement a scheduled action that sets the desired capacity to 10 before business hours begin.**
- Implement a target tracking action with a lower CPU threshold, and decrease the cooldown period.
- Implement a step scaling action with a lower CPU threshold and decrease the cooldown period.

**A:** **Implement a scheduled action that sets the desired capacity to 10 before business hours begin.**

**Explanation:**

Scheduled scaling allows you to set your own scaling schedule. Setting the desired capacity to 10 before business hours begin ensures instances are ready when needed, without permanently changing the minimum and maximum bounds.

- **CORRECT:** "Implement a scheduled action that sets the desired capacity to 10 before business hours begin" is the correct answer.
- **INCORRECT:** "Implement a scheduled action that sets the minimum and maximum capacity to 10 before business hours begin" is incorrect. The minimum and maximums define how many instances CAN run; changing them to 10 forces the group to always maintain 10, which is not cost-effective.
- **INCORRECT:** "Implement a step scaling action with a lower CPU threshold and decrease the cooldown period" is incorrect. A lower threshold and shorter cooldown will trigger scaling sooner but cannot guarantee instances are ready before business hours begin.
- **INCORRECT:** "Implement a target tracking action with a lower CPU threshold, and decrease the cooldown period" is incorrect. As above, this may achieve faster scaling at lower loads but does not pre-provision instances before demand arrives.

**References:**
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html
- https://digitalcloud.training/amazon-ec2/

---

### Question 11 (Shared Storage for Auto Scaling Group – Amazon EFS)

**Q:** A data analytics company is testing a Python-based application that processes customer data on an Amazon EC2 Linux instance. A single 1 TB Amazon Elastic Block Store (Amazon EBS) General Purpose SSD volume is currently used to store the data.

The company plans to deploy the application across multiple EC2 instances in an Auto Scaling group. All instances must access the same data that is currently stored on the EBS volume. The company wants a cost-effective, scalable solution.

Which solution will meet these requirements?

**Options:**

- **✅ Use Amazon Elastic File System (Amazon EFS) and configure it in General Purpose performance mode. Mount the EFS file system on all EC2 instances.**
- Configure an Amazon FSx for Lustre file system. Integrate the file system with Amazon S3 and mount it on each EC2 instance for shared access.
- Create an EC2 instance to act as an NFS server. Attach the EBS volume to this instance and share the volume with other EC2 instances in the Auto Scaling group.
- Provision Amazon S3 and use the S3 REST API to allow all EC2 instances to upload and download data from the S3 bucket.

**A:** **Use Amazon Elastic File System (Amazon EFS) and configure it in General Purpose performance mode. Mount the EFS file system on all EC2 instances.**

**Explanation:**

Amazon EFS is a highly available, scalable NFS file system that can be simultaneously mounted by multiple EC2 instances. General Purpose mode is suitable for latency-sensitive workloads and is the most cost-effective option for shared Linux file access.

- **CORRECT:** "Use Amazon EFS in General Purpose performance mode" is the correct answer.
- **INCORRECT:** "Configure an Amazon FSx for Lustre file system" is incorrect because FSx for Lustre is designed for high-performance HPC workloads and is more expensive than EFS for general-purpose shared access.
- **INCORRECT:** "Create an EC2 instance to act as an NFS server" is incorrect because using a single EC2 NFS server creates a single point of failure and increases operational overhead.
- **INCORRECT:** "Provision Amazon S3 and use the S3 REST API" is incorrect because Amazon S3 is an object storage service, not a file system, and the application requires a POSIX-compatible file system interface.

**References:**
- https://aws.amazon.com/efs/
- https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html
- https://digitalcloud.training/amazon-efs/

---

### Question 19 (EKS Custom Subnet Networking – VPC CNI Plugin)

**Q:** A retail company is migrating its supply chain application to Amazon Elastic Kubernetes Service (Amazon EKS). The company requires pods in the EKS cluster to use custom subnets in its existing VPC for network segmentation and compliance purposes.

Which solution will meet these requirements?

**Options:**

- Set up AWS Transit Gateway to manage the routing between custom subnets and the EKS pods for secure communication within the VPC.
- **✅ Use the Amazon VPC CNI plugin for Kubernetes. Configure the custom subnets in the VPC and associate the subnets with the EKS cluster to allow pods to use them.**
- Define Kubernetes network policies that enforce pod placement on specific nodes residing in the custom subnets within the VPC.
- Configure an AWS Site-to-Site VPN between the custom subnets and the EKS cluster to enable secure communication for the pods.

**A:** **Use the Amazon VPC CNI plugin for Kubernetes. Configure the custom subnets in the VPC and associate the subnets with the EKS cluster to allow pods to use them.**

**Explanation:**

The Amazon VPC CNI plugin assigns VPC-native IP addresses to pods, allowing them to reside in and communicate over custom subnets. Associating custom subnets with the EKS cluster ensures pods receive IPs from those subnets.

- **CORRECT:** "Use the Amazon VPC CNI plugin for Kubernetes" is the correct answer.
- **INCORRECT:** "Set up AWS Transit Gateway" is incorrect because Transit Gateway is used for cross-VPC and on-premises routing, not for assigning pods to specific subnets within a single VPC.
- **INCORRECT:** "Configure an AWS Site-to-Site VPN" is incorrect because the VPC and EKS cluster are already within the same network; VPN is not needed for intra-VPC connectivity.
- **INCORRECT:** "Define Kubernetes network policies" is incorrect because Kubernetes network policies control traffic flow between pods, not the subnet from which pods receive their IP addresses.

**References:**
- https://docs.aws.amazon.com/eks/latest/userguide/pod-networking.html
- https://aws.amazon.com/blogs/containers/introducing-eks-vpc-cni-custom-network-configuration/
- https://digitalcloud.training/amazon-vpc/

---

### Question 24 (Lustre Shared Storage – Amazon FSx for Lustre)

**Q:** A company is architecting a shared storage solution for an AWS-hosted gaming application. The company needs the ability to use Lustre clients to access data. The solution must be fully managed.

Which solution meets these requirements?

**Options:**

- Assign the AWS DataSync task to share the data as a mountable file system. Sync the file system with the application server.
- Create an Amazon Elastic File System (Amazon EFS) file system and configure it to support Lustre. Attach the file system to the origin server. Connect the application server to the file system.
- Create a file gateway with AWS Storage Gateway. Create a client-side file share using the required protocol. Share the file with the application server.
- **✅ Create an Amazon FSx for Lustre file system. Connect the file system to the origin server. Ensure that the file system is connected to the application server.**

**A:** **Create an Amazon FSx for Lustre file system. Connect the file system to the origin server. Ensure that the file system is connected to the application server.**

**Explanation:**

Amazon FSx for Lustre provides fully managed shared storage with the scalability and performance of the popular Lustre file system. It is fully managed and allows Lustre clients to connect directly.

- **CORRECT:** "Create an Amazon FSx for Lustre file system" is the correct answer.
- **INCORRECT:** "Assign the AWS DataSync task to share the data as a mountable file system" is incorrect. DataSync is a data transfer service, not a shared file system. It does not support Lustre clients.
- **INCORRECT:** "Create a file gateway with AWS Storage Gateway" is incorrect. Storage Gateway does not support the Lustre protocol.
- **INCORRECT:** "Create an Amazon EFS file system and configure it to support Lustre" is incorrect. EFS does not support the Lustre protocol.

**References:**
- https://aws.amazon.com/fsx/lustre/
- https://digitalcloud.training/amazon-fsx/

---

### Question 28 (Custom Error Pages – CloudFront + ALB)

**Q:** A website runs on Amazon EC2 instances behind an Application Load Balancer (ALB). The website's DNS records are hosted in Amazon Route 53 with the domain name pointing to the ALB. A solution is required to display a custom static error page if the ALB and EC2 instances experience an outage.

Which configuration should a solutions architect use to meet these requirements with the LEAST operational overhead?

**Options:**

- Set up a Route 53 active-active configuration with the ALB and an Amazon EC2 instance hosting a static error page as endpoints. Route 53 will only send requests to the instance if the health check on the ALB fails.
- Create a Route 53 weighted routing policy. Create a static website using an Amazon S3 bucket that hosts a static error page. Configure the record for the S3 static website with a weighting of zero.
- **✅ Create a Route 53 alias record for an Amazon CloudFront distribution and specify the ALB as the origin. Create custom error pages for the distribution.**
- Create a Route 53 active-passive failover configuration. Create a static website using an Amazon S3 bucket that hosts a static error page. Configure the static website as the passive record for failover.

**A:** **Create a Route 53 alias record for an Amazon CloudFront distribution and specify the ALB as the origin. Create custom error pages for the distribution.**

**Explanation:**

Using Amazon CloudFront as the front-end provides the option to specify a custom message instead of the default error message. CloudFront can serve custom error pages directly from its edge cache when the origin (ALB) is unavailable, requiring no manual intervention.

- **CORRECT:** "Create a Route 53 alias record for an Amazon CloudFront distribution and specify the ALB as the origin. Create custom error pages for the distribution" is the correct answer.
- **INCORRECT:** "Create a Route 53 active-passive failover configuration with an S3 static website" is incorrect. While it works, it requires more configuration and still depends on health check propagation time before failover activates.
- **INCORRECT:** "Create a Route 53 weighted routing policy with S3 at zero weight" is incorrect. A weight of zero means the S3 error page will never receive traffic under normal conditions, but the configuration is complex and not operationally efficient.
- **INCORRECT:** "Set up a Route 53 active-active configuration with an EC2 instance hosting a static error page" is incorrect. This requires additional EC2 instances to host error pages, increasing cost and operational overhead.

**References:**
- https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/custom-error-pages.html
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 35 (Global Multi-Region ALB Routing – Global Accelerator)

**Q:** A web application is deployed in multiple regions behind an ELB Application Load Balancer. You need deterministic routing to the closest region and automatic failover. Traffic should traverse the AWS global network.

How can this be achieved?

**Options:**

- **✅ Configure AWS Global Accelerator and configure the ALBs as targets.**
- Place an EC2 Proxy in front of the ALB and configure automatic failover.
- Use a CloudFront distribution with multiple custom origins in each region and configure for high availability.
- Create a Route 53 Alias record for each ALB and configure a latency-based routing policy.

**A:** **Configure AWS Global Accelerator and configure the ALBs as targets.**

**Explanation:**

AWS Global Accelerator is a service that improves the availability and performance of applications with local or global users. You can configure the ALB as a target and Global Accelerator will automatically route traffic to the closest healthy endpoint. Failover is automatic and uses static anycast IPs, so no client-side cache changes are needed.

- **CORRECT:** "Configure AWS Global Accelerator and configure the ALBs as targets" is the correct answer.
- **INCORRECT:** "Place an EC2 Proxy in front of the ALB and configure automatic failover" is incorrect. This does not use the AWS global network and adds operational overhead.
- **INCORRECT:** "Create a Route 53 Alias record for each ALB and configure a latency-based routing policy" is incorrect. Route 53 latency routing does provide regional routing but relies on DNS TTL for failover and does not traverse the AWS backbone.
- **INCORRECT:** "Use a CloudFront distribution with multiple custom origins in each region and configure for high availability" is incorrect. CloudFront is for HTTP/HTTPS content delivery and does not provide the same deterministic global routing as Global Accelerator for application traffic.

**References:**
- https://aws.amazon.com/global-accelerator/
- https://aws.amazon.com/global-accelerator/faqs/
- https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- https://digitalcloud.training/aws-global-accelerator/

---

### Question 55 (JSON Processing – S3 + Lambda + Aurora)

**Q:** A small Python application is used by a company to process JSON documents and output the results to a SQL database which currently lives on-premises. The application is run thousands of times every day. The company is migrating the SQL database to AWS and wants to redesign the application.

Which solution will meet these requirements?

**Options:**

- **✅ Put the JSON documents in an Amazon S3 bucket. As documents arrive in the S3 bucket, create an AWS Lambda function that runs Python code to process them. Use Amazon Aurora DB clusters to store the results.**
- The JSON documents should be queued as messages in the Amazon Simple Queue Service (Amazon SQS). Using the Amazon Elastic Container Service (Amazon ECS) with the Amazon EC2 launch type, deploy the Python code to process the messages and store results in Aurora.
- Build an S3 bucket to place the JSON documents in. Run the Python code on multiple Amazon EC2 instances to process the documents. Store the results in a database using the Amazon Aurora Database service.
- Create an Amazon Elastic Block Store (Amazon EBS) volume for the JSON documents. Attach the volume to multiple Amazon EC2 instances using the EBS Multi-Attach feature. Process the documents with Python on the EC2 instances and store the results in Aurora.

**A:** **Put the JSON documents in an Amazon S3 bucket. As documents arrive in the S3 bucket, create an AWS Lambda function that runs Python code to process them. Use Amazon Aurora DB clusters to store the results.**

**Explanation:**

S3 is a highly available and durable store for JSON documents (write once, read many). AWS Lambda is triggered by S3 events, runs the Python processing code, and scales automatically with demand — no idle compute cost. Aurora provides a managed SQL database for storing results.

- **CORRECT:** "Put the JSON documents in an Amazon S3 bucket and use Lambda to process them" is the correct answer.
- **INCORRECT:** "Run the Python code on multiple Amazon EC2 instances" is incorrect. You would need to either leave EC2 instances running all the time (not cost effective) or implement complex auto-scaling logic.
- **INCORRECT:** "Use EBS Multi-Attach with EC2" is incorrect. EBS is not optimized for WORM use-cases and requires persistent EC2 instances, adding cost and management overhead.
- **INCORRECT:** "Queue JSON documents in SQS and use ECS with EC2 launch type" is incorrect. SQS is not designed for write-once-read-many workloads, and ECS with EC2 requires persistent compute, unlike serverless Lambda.

**References:**
- https://docs.aws.amazon.com/lambda/latest/dg/services-rds.html
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 57 (Cross-VPC ECS Access – AWS PrivateLink)

**Q:** A company runs an application in an Amazon VPC that requires access to an Amazon Elastic Container Service (Amazon ECS) cluster that hosts an application in another VPC. The company's security team requires that the traffic between the two VPCs does not traverse the public internet.

Which solution meets this requirement?

**Options:**

- Configure an Amazon Route 53 private hosted zone for each VPC. Use private records to resolve internal IP addresses in each VPC.
- Configure a gateway endpoint for Amazon ECS. Update the route table to include an entry pointing to the ECS cluster.
- **✅ Create a Network Load Balancer in one VPC and an AWS PrivateLink endpoint for Amazon ECS in another VPC.**
- Create a Network Load Balancer and AWS PrivateLink endpoint for Amazon ECS in the VPC that hosts the ECS cluster.

**A:** **Create a Network Load Balancer in one VPC and an AWS PrivateLink endpoint for Amazon ECS in another VPC.**

**Explanation:**

AWS PrivateLink in a service-provider model requires a Network Load Balancer in the provider VPC (the one with the ECS cluster) and a VPC endpoint in the consumer VPC. This keeps traffic entirely within the AWS network without traversing the public internet.

- **CORRECT:** "Create a Network Load Balancer in one VPC and an AWS PrivateLink endpoint for Amazon ECS in another VPC" is the correct answer.
- **INCORRECT:** "Create a Network Load Balancer and AWS PrivateLink endpoint for Amazon ECS in the VPC that hosts the ECS cluster" is incorrect. The endpoint should be in the consumer VPC, not the service provider VPC.
- **INCORRECT:** "Configure a gateway endpoint for Amazon ECS" is incorrect. You cannot use a gateway endpoint to connect to a private service in another VPC.
- **INCORRECT:** "Configure an Amazon Route 53 private hosted zone for each VPC" is incorrect. This does not provide a mechanism for routing traffic privately between VPCs without public internet traversal.

**References:**
- https://aws.amazon.com/privatelink/
- https://digitalcloud.training/amazon-vpc/

---

### Question 59 (Survey Feedback Analysis – API Gateway + Firehose + Lambda + Comprehend)

**Q:** A fitness company collects user feedback from mobile app surveys about its workout plans and features. Users submit thousands of survey responses daily, and the company wants to automate feedback processing and perform sentiment analysis. The company requires a highly scalable solution that minimizes operational complexity.

Which solution will meet these requirements in the MOST scalable way?

**Options:**

- Deploy an on-premises server that receives survey responses via a REST API. Process the data locally, use a custom machine learning model for sentiment analysis, and upload results to Amazon S3.
- Send survey responses to an Amazon EventBridge rule, which routes the data to an AWS Step Functions workflow. Use Step Functions to trigger AWS Lambda for data processing and sentiment analysis with Amazon Comprehend.
- Write survey responses directly to an Amazon Redshift database. Configure Amazon Redshift ML to perform sentiment analysis on the feedback data in real time. Use Amazon S3 to archive the processed results.
- **✅ Collect survey responses via an Amazon API Gateway endpoint integrated with Amazon Kinesis Data Firehose. Configure Firehose to stream the data to an Amazon S3 bucket. Use S3 Event Notifications to trigger an AWS Lambda function that calls Amazon Comprehend for sentiment analysis.**

**A:** **Collect survey responses via an Amazon API Gateway endpoint integrated with Amazon Kinesis Data Firehose. Configure Firehose to stream the data to an Amazon S3 bucket. Use S3 Event Notifications to trigger an AWS Lambda function that calls Amazon Comprehend for sentiment analysis.**

**Explanation:**

This architecture is highly scalable and cost-effective. Kinesis Data Firehose automatically scales to handle large volumes of data, S3 provides reliable storage, and Lambda with Comprehend provides serverless, managed sentiment analysis with no infrastructure to manage.

- **CORRECT:** "Collect survey responses via API Gateway + Kinesis Firehose + S3 + Lambda + Comprehend" is the correct answer.
- **INCORRECT:** "Send survey responses to an EventBridge rule with Step Functions" is incorrect because using EventBridge and Step Functions adds unnecessary complexity for a straightforward data ingestion and processing pipeline.
- **INCORRECT:** "Write survey responses directly to Amazon Redshift" is incorrect because Amazon Redshift is better suited for analytical queries and is not optimized for real-time sentiment analysis at high ingestion rates.
- **INCORRECT:** "Deploy an on-premises server" is incorrect because deploying and managing on-premises servers increases operational overhead and contradicts the requirement to minimize operational complexity.

**References:**
- https://docs.aws.amazon.com/streams/latest/dev/introduction.html
- https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- https://digitalcloud.training/amazon-kinesis/

---

## Dump 6

---

### Question 1 (High-Performance Financial Modelling – FSx for Lustre)

**Q:** A high-performance file system is required for a financial modelling application. The data set will be stored on Amazon S3 and the storage solution must have seamless integration so objects can be used as files.

Which storage solution should be used?

**Options:**

- Amazon Elastic Block Store (EBS)
- **✅ Amazon FSx for Lustre**
- Amazon Elastic File System (EFS)
- Amazon FSx for Windows File Server

**A:** **Amazon FSx for Lustre**

**Explanation:**

Amazon FSx for Lustre provides a high-performance file system optimized for fast processing of workloads such as machine learning, high performance computing (HPC), video processing, financial modelling, and electronic design automation (EDA). FSx for Lustre integrates natively with Amazon S3, presenting S3 objects as files in the file system.

- **CORRECT:** "Amazon FSx for Lustre" is the correct answer.
- **INCORRECT:** "Amazon FSx for Windows File Server" is incorrect. Amazon FSx for Windows File Server provides a fully managed native Microsoft Windows file system and does not integrate with S3 to present objects as files.
- **INCORRECT:** "Amazon Elastic File System (EFS)" is incorrect. Neither EFS nor EBS can present Amazon S3 objects as files to a POSIX file system.
- **INCORRECT:** "Amazon Elastic Block Store (EBS)" is incorrect. Neither EFS nor EBS can present Amazon S3 objects as files to a POSIX file system.

**References:**
- https://aws.amazon.com/fsx/
- https://digitalcloud.training/amazon-fsx/

---

### Question 4 (Resilient Bastion Hosts – NLB + ASG Multi-AZ)

**Q:** A company's staff connect from home office locations to administer applications using bastion hosts in a single AWS Region. The company requires a resilient bastion host architecture that requires a single endpoint for users to connect to.

How can a Solutions Architect best meet these requirements?

**Options:**

- **✅ Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple Availability Zones.**
- Create a Network Load Balancer backed by Reserved Instances in a cluster placement group.
- Create a Network Load Balancer backed by the existing servers in different Availability Zones.
- Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple AWS Regions.

**A:** **Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple Availability Zones.**

**Explanation:**

Bastion hosts (aka "jump hosts") are EC2 instances in public subnets that administrators connect to from the internet. An NLB provides a single, stable endpoint. An Auto Scaling group across multiple AZs ensures resilience: if one AZ becomes unavailable, instances in other AZs continue to accept connections.

- **CORRECT:** "Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple Availability Zones" is the correct answer.
- **INCORRECT:** "Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple AWS Regions" is incorrect. You cannot have instances in an ASG across multiple Regions, and NLBs are regional.
- **INCORRECT:** "Create a Network Load Balancer backed by Reserved Instances in a cluster placement group" is incorrect. A cluster placement group packs instances close together in a single AZ, reducing resilience.
- **INCORRECT:** "Create a Network Load Balancer backed by the existing servers in different Availability Zones" is incorrect. An Auto Scaling group is required to maintain instances in different AZs and replace unhealthy instances automatically.

**References:**
- https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html
- https://digitalcloud.training/amazon-ec2-auto-scaling/

---

### Question 5 (ECS Hybrid Deployment – Fargate + ECS Anywhere)

**Q:** A company wants to use Amazon Elastic Container Service (Amazon ECS) to run its containerized application in a hybrid environment. The company needs to ensure that the application can scale across both cloud and on-premises infrastructure, and it must handle HTTP traffic.

Which combination of actions will meet these requirements? (Select TWO.)

**Options:**

- Set up an ECS cluster that uses the AWS Fargate launch type. Use Fargate for the cloud application containers and the on-premises application containers.
- Set up an ECS cluster that uses the Amazon EC2 launch type for the cloud application containers. Use Amazon ECS Anywhere with an AWS Fargate launch type for the on-premises application containers.
- **✅ Set up an ECS cluster that uses the AWS Fargate launch type for the cloud application containers. Use an Amazon ECS Anywhere external launch type for the on-premises application containers.**
- **✅ Set up an Application Load Balancer for cloud ECS services.**
- Set up a Network Load Balancer for cloud ECS services.

**A:** **Set up an ECS cluster with AWS Fargate (cloud) and Amazon ECS Anywhere external launch type (on-premises)** AND **Set up an Application Load Balancer for cloud ECS services.**

**Explanation:**

ECS Anywhere with the "external" launch type allows on-premises servers to be registered and managed as ECS tasks. Fargate handles cloud workloads. An ALB is the appropriate load balancer for HTTP traffic routing to cloud ECS services.

- **CORRECT:** "Set up an ECS cluster that uses the AWS Fargate launch type for the cloud application containers. Use an Amazon ECS Anywhere external launch type for the on-premises application containers" is the correct answer.
- **CORRECT:** "Set up an Application Load Balancer for cloud ECS services" is the correct answer.
- **INCORRECT:** "Set up a Network Load Balancer for cloud ECS services" is incorrect because a Network Load Balancer is primarily used for TCP or UDP traffic, not HTTP traffic.
- **INCORRECT:** "Set up an ECS cluster that uses the AWS Fargate launch type. Use Fargate for the cloud and on-premises containers" is incorrect because Fargate cannot run on-premises infrastructure.
- **INCORRECT:** "Set up an ECS cluster that uses the Amazon EC2 launch type for the cloud containers. Use Amazon ECS Anywhere with an AWS Fargate launch type for on-premises" is incorrect because ECS Anywhere uses the "external" launch type, not Fargate, for on-premises infrastructure.

**References:**
- https://docs.aws.amazon.com/AmazonECS/latest/developerguide/what-is-ecs.html
- https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-anywhere.html
- https://digitalcloud.training/amazon-ecs-and-eks/

---

### Question 6 (EC2 Reserved + Scheduled Reserved Instances)

**Q:** A company operates a production environment on Amazon EC2 instances. The instances are required to run continuously from Tuesday to Sunday without interruptions. On Mondays, the instances are needed only for 8 hours.

Which solution will provide the MOST cost-effective results?

**Options:**

- Purchase Convertible Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Spot Instances for the EC2 instances that run for 8 hours on Mondays.
- Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Convertible Reserved Instances for the EC2 instances that run for 8 hours on Mondays.
- Use Spot Instances for the EC2 instances that run for 8 hours on Mondays. Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday.
- **✅ Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Scheduled Reserved Instances for the EC2 instances that run for 8 hours on Mondays.**

**A:** **Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Scheduled Reserved Instances for the EC2 instances that run for 8 hours on Mondays.**

**Explanation:**

Standard Reserved Instances are the most cost-effective option for always-on, continuous workloads. Scheduled Reserved Instances provide reserved capacity for specific recurring time windows (e.g., every Monday for 8 hours), which is more cost-effective than Spot or Convertible RIs for predictable, time-bounded workloads.

- **CORRECT:** "Purchase Standard Reserved Instances for Tuesday–Sunday. Use Scheduled Reserved Instances for 8 hours on Mondays" is the correct answer.
- **INCORRECT:** "Use Spot Instances for Mondays" is incorrect because Spot Instances can be interrupted at any time with only a 2-minute warning, making them unsuitable for predictable, scheduled production workloads.
- **INCORRECT:** "Purchase Convertible Reserved Instances for Tuesday–Sunday. Use Spot Instances for Mondays" is incorrect because Convertible RIs are less discounted than Standard RIs, and Spot Instances are interruptible.
- **INCORRECT:** "Use Convertible Reserved Instances for Mondays" is incorrect because Convertible RIs are designed for flexibility over time, not short, recurring windows, and are more expensive than Scheduled RIs for this use case.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-reserved-instances.html
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- https://digitalcloud.training/amazon-ec2/

---

### Question 7 (Aurora Multi-Region DR – Aurora Global Database)

**Q:** A company runs a business-critical application in the us-east-1 Region. The application uses an Amazon Aurora MySQL database cluster which is 2 TB in size. A Solutions Architect needs to determine the best strategy for achieving cross-region disaster recovery with an RPO of 1 second and an RTO of less than 1 minute.

Which strategy will meet these requirements?

**Options:**

- **✅ Recreate the database as an Aurora global database with the primary DB cluster in us-east-1 and a secondary DB cluster in us-west-2. Use an Amazon EventBridge rule that invokes an AWS Lambda function to promote the secondary cluster in the event of a failure.**
- Create a multi-Region Aurora MySQL DB cluster in us-east-1 and us-west-2. Use an Amazon Route 53 health check to monitor us-east-1 and fail over to us-west-2 upon failure.
- Recreate the database as an Aurora multi master cluster across the us-east-1 and us-west-2 Regions with multiple writers to allow read/write capabilities from all database instances.
- Create a cross-Region Aurora MySQL read replica in us-west-2 Region. Configure an Amazon EventBridge rule that invokes an AWS Lambda function that promotes the read replica in us-west-2 when failure is detected.

**A:** **Recreate the database as an Aurora global database with the primary DB cluster in us-east-1 and a secondary DB cluster in us-west-2. Use an Amazon EventBridge rule that invokes an AWS Lambda function to promote the secondary cluster in the event of a failure.**

**Explanation:**

Amazon Aurora Global Database is designed for globally distributed applications, replicating data with no impact on database performance. It provides an RPO of 1 second and an RTO of less than 1 minute, meeting the requirements exactly. Promotion of the secondary cluster is triggered by a Lambda function via EventBridge.

- **CORRECT:** "Recreate the database as an Aurora global database" is the correct answer.
- **INCORRECT:** "Create a multi-Region Aurora MySQL DB cluster with Route 53 health checks" is incorrect because "multi-Region Aurora MySQL DB cluster" is not a valid Aurora configuration. Aurora Global Database is the correct service.
- **INCORRECT:** "Create a cross-Region Aurora MySQL read replica" is incorrect because cross-region read replicas have a higher RTO than Aurora Global Database and are not the recommended DR mechanism for strict RTO requirements.
- **INCORRECT:** "Recreate the database as an Aurora multi master cluster across regions" is incorrect because Aurora multi-master is only supported within a single region, not across regions.

**References:**
- https://aws.amazon.com/rds/aurora/global-database/
- https://digitalcloud.training/amazon-aurora/

---

### Question 14 (UDP Low-Latency Global App – NLB + Global Accelerator)

**Q:** A Solutions Architect is designing a solution for an application that requires very low latency between the client and the backend. The application uses the UDP protocol, and the backend is hosted on Amazon EC2 instances in multiple Regions.

How can the Solutions Architect meet these requirements?

**Options:**

- Deploy an Application Load Balancer in front of the EC2 instances in each Region. Use AWS WAF to direct traffic to the most optimal Regional endpoint.
- Deploy an Amazon CloudFront distribution with a custom origin pointing to Amazon EC2 instances in multiple Regions.
- Deploy Amazon EC2 instances in multiple Regions. Create a multivalue answer routing record in Amazon Route 53 that includes all EC2 endpoints.
- **✅ Deploy a Network Load Balancer in front of the EC2 instances in each Region. Use AWS Global Accelerator to route traffic to the most optimal Regional endpoint.**

**A:** **Deploy a Network Load Balancer in front of the EC2 instances in each Region. Use AWS Global Accelerator to route traffic to the most optimal Regional endpoint.**

**Explanation:**

An NLB is ideal for latency-sensitive applications and can listen on UDP for incoming requests. As Elastic Load Balancers are region-specific it is necessary to have an NLB in each Region. AWS Global Accelerator routes traffic across the AWS global network to the most optimal endpoint based on performance, with automatic failover.

- **CORRECT:** "Deploy a Network Load Balancer in front of the EC2 instances in each Region. Use AWS Global Accelerator" is the correct answer.
- **INCORRECT:** "Deploy an Application Load Balancer. Use AWS WAF to direct traffic" is incorrect. You cannot use WAF to route traffic based on performance, and ALBs do not support UDP.
- **INCORRECT:** "Deploy an Amazon CloudFront distribution" is incorrect. CloudFront does not support UDP; it is used for HTTP/HTTPS content delivery.
- **INCORRECT:** "Create a multivalue answer routing record in Amazon Route 53" is incorrect. Route 53 multivalue routing does not use the AWS global network and provides limited failover compared to Global Accelerator.

**References:**
- https://docs.aws.amazon.com/global-accelerator/latest/dg/introduction-how-it-works.html
- https://digitalcloud.training/aws-global-accelerator/

---

### Question 16 (Direct Connect Encryption – Virtual Private Gateway)

**Q:** An organization is extending a secure development environment into AWS. They have already secured the VPC including removing the Internet Gateway and setting up a Direct Connect connection. What additional step should be taken to add encryption to the data in transit over the Direct Connect connection?

**Options:**

- Configure an AWS Direct Connect Gateway
- Setup the Border Gateway Protocol (BGP) with encryption
- Enable IPSec encryption on the Direct Connect connection
- **✅ Setup a Virtual Private Gateway (VPG)**

**A:** **Setup a Virtual Private Gateway (VPG)**

**Explanation:**

A Virtual Private Gateway is used to set up an AWS VPN which you can use in combination with Direct Connect to encrypt all data that traverses the Direct Connect link. This combination provides an IPsec-encrypted private connection over Direct Connect.

- **CORRECT:** "Setup a Virtual Private Gateway (VPG)" is the correct answer.
- **INCORRECT:** "Enable IPSec encryption on the Direct Connect connection" is incorrect. There is no option to enable IPSec encryption directly on the Direct Connect connection itself.
- **INCORRECT:** "Setup the Border Gateway Protocol (BGP) with encryption" is incorrect. BGP is used for routing, not encryption.
- **INCORRECT:** "Configure an AWS Direct Connect Gateway" is incorrect. An AWS Direct Connect Gateway is used to connect to VPCs across multiple AWS regions. It is not involved with encryption.

**References:**
- https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-direct-connect-plus-vpn-network-to-amazon.html
- https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
- https://digitalcloud.training/amazon-vpc/

---

### Question 22 (Classified Documents Encryption – Client-Side with Customer Keys)

**Q:** A government agency is moving its document management system to AWS. The application will store classified documents in Amazon S3. The agency must encrypt the documents before storing them in S3 and must retain full control over the encryption keys at all times.

Which solution will meet these requirements?

**Options:**

- Encrypt the documents by using client-side encryption with Amazon S3 managed keys and upload the encrypted files to S3.
- **✅ Encrypt the documents by using client-side encryption with customer managed keys and upload the encrypted files to S3.**
- Encrypt the documents by using server-side encryption with customer-provided keys (SSE-C).
- Encrypt the documents by using server-side encryption with AWS KMS keys (SSE-KMS) configured with custom key policies for access control.

**A:** **Encrypt the documents by using client-side encryption with customer managed keys and upload the encrypted files to S3.**

**Explanation:**

Client-side encryption means the data is encrypted before it ever leaves the client system. Using customer managed keys gives the agency maximum control over the encryption process — AWS never has access to the plaintext data or the keys.

- **CORRECT:** "Encrypt the documents by using client-side encryption with customer managed keys" is the correct answer.
- **INCORRECT:** "Encrypt by using server-side encryption with AWS KMS keys (SSE-KMS)" is incorrect because while secure and easy to manage, SSE-KMS involves AWS in the encryption process; data travels to AWS unencrypted and AWS manages key operations.
- **INCORRECT:** "Encrypt by using client-side encryption with Amazon S3 managed keys" is incorrect because S3-managed keys are controlled by AWS, not the agency, which does not meet the requirement for full key control.
- **INCORRECT:** "Encrypt by using server-side encryption with customer-provided keys (SSE-C)" is incorrect because SSE-C requires the customer to provide the encryption key on every S3 API operation, and the data is only encrypted at rest by S3, not by the client before transmission.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingEncryption.html
- https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html
- https://digitalcloud.training/aws-kms/

---

### Question 35 (Static IP Global Performance – AWS Global Accelerator)

**Q:** An application is deployed on multiple AWS regions and accessed from around the world. The application exposes static public IP addresses. Some users are experiencing poor performance when accessing the application.

What should a solutions architect recommend to reduce internet latency?

**Options:**

- Set up an Amazon Route 53 geoproximity routing policy to route traffic
- **✅ Set up AWS Global Accelerator and add endpoints**
- Set up an Amazon CloudFront distribution to access an application
- Set up AWS Direct Connect locations in multiple Regions

**A:** **Set up AWS Global Accelerator and add endpoints.**

**Explanation:**

AWS Global Accelerator is a service in which you create accelerators to improve availability and performance of your applications for local and global users. Global Accelerator directs traffic to the optimal AWS Region. By default, it provides two static anycast IP addresses that distribute incoming traffic across multiple endpoint resources in multiple Regions.

- **CORRECT:** "Set up AWS Global Accelerator and add endpoints" is the correct answer.
- **INCORRECT:** "Set up AWS Direct Connect locations in multiple Regions" is incorrect as Direct Connect is used to connect from an on-premises data center to AWS.
- **INCORRECT:** "Set up an Amazon CloudFront distribution" is incorrect as CloudFront cannot expose static public IP addresses.
- **INCORRECT:** "Set up an Amazon Route 53 geoproximity routing policy" is incorrect as this does not reduce internet latency as effectively as Global Accelerator, which routes users over the AWS global network backbone.

**References:**
- https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- https://digitalcloud.training/aws-global-accelerator/

---

### Question 37 (S3 Regulatory WORM – S3 Object Lock Compliance Mode)

**Q:** A company needs to implement a new data retention policy for regulatory compliance. As part of this policy, sensitive documents that are stored in an Amazon S3 bucket must be protected from deletion or modification for a specific retention period. No user, including the root user, should be able to delete or modify the objects during the retention period.

Which solution will meet these requirements?

**Options:**

- Create an Amazon S3 bucket with versioning enabled. Use a lifecycle rule to automatically delete older versions after the retention period.
- Use AWS Backup to create immutable backups of the S3 objects and enforce a retention policy.
- **✅ Enable S3 Object Lock on the required objects and set compliance mode.**
- Activate S3 Object Lock in compliance mode on the bucket. Configure a WORM (Write Once, Read Many) policy.

**A:** **Enable S3 Object Lock on the required objects and set compliance mode.**

**Explanation:**

S3 Object Lock in compliance mode ensures that no user, including the root user, can delete or modify the locked objects for the duration of the retention period. Object Lock is applied at the object level.

- **CORRECT:** "Enable S3 Object Lock on the required objects and set compliance mode" is the correct answer.
- **INCORRECT:** "Activate S3 Object Lock in compliance mode on the bucket and configure a WORM policy" is incorrect because S3 Object Lock applies to specific objects, not the entire bucket. You enable the feature on the bucket but set retention on individual objects.
- **INCORRECT:** "Create an Amazon S3 bucket with versioning enabled. Use a lifecycle rule to automatically delete older versions" is incorrect because versioning and lifecycle policies do not prevent deletion or modification during an active retention period.
- **INCORRECT:** "Use AWS Backup to create immutable backups" is incorrect because AWS Backup does not integrate directly with S3 Object Lock to meet regulatory WORM requirements.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock-overview.html
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-object-lock.html
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 44 (ML Data Lake – AWS Lake Formation)

**Q:** A Solutions Architect works for a company looking to centralize its Machine Learning Operations. Currently they have a large amount of existing cloud storage to store their operational data which needs to be curated into a centralized repository for Machine Learning purposes.

Which service can be used to build a centralized data repository to be used for Machine Learning purposes?

**Options:**

- Amazon S3
- **✅ AWS Lake Formation**
- Amazon Quantum Ledger Database (QLDB)
- Amazon Neptune

**A:** **AWS Lake Formation**

**Explanation:**

AWS Lake Formation is a service that makes it easy to set up a secure data lake in days. A data lake is a centralized, curated, and secured repository that stores all your data, both in its original form and prepared for analysis.

- **CORRECT:** "AWS Lake Formation" is the correct answer.
- **INCORRECT:** "Amazon S3" is incorrect. While S3 is the underlying storage for a data lake, it is not a data lake service — it does not provide data cataloguing, curation, security, or ML integration out of the box.
- **INCORRECT:** "Amazon Quantum Ledger Database (QLDB)" is incorrect. QLDB is a fully managed ledger database for tracking application data changes. It is not a centralized ML data repository.
- **INCORRECT:** "Amazon Neptune" is incorrect. Amazon Neptune is a managed graph database service. It is not suitable for building a centralized data lake for Machine Learning.

**References:**
- https://aws.amazon.com/lake-formation/features/
- https://digitalcloud.training/category/aws-cheat-sheets/aws-solutions-architect-associate/aws-storage-saa/

---

### Question 59 (Secure Contractor Access – SSM Session Manager + IAM Identity Center)

**Q:** A company manages several applications that run in different AWS accounts within an AWS Organizations setup. The company has outsourced the management of certain applications to external contractors. The contractors need secure access to manage EC2 instances across multiple accounts without requiring open SSH ports or long-term credentials.

Which solution will meet these requirements MOST securely?

**Options:**

- Configure a bastion host in a public subnet. Restrict SSH access to the bastion host by using security groups to allow connections only from the contractors' IP address ranges. Provide contractors with SSH key pairs.
- **✅ Deploy AWS Systems Manager Agent (SSM Agent) to all instances. Assign an instance profile to the instances with the required Systems Manager policies. Grant contractors access to the AWS Management Console through AWS IAM Identity Center.**
- Use AWS Systems Manager Agent (SSM Agent) with an attached instance profile to manage EC2 access. Provide contractors with temporary local IAM user credentials in each AWS account for console access.
- Set up AWS VPN or Direct Connect to create a private network connection to the contractors' office. Allow access to the AWS Management Console by creating IAM user credentials in each AWS account.

**A:** **Deploy AWS Systems Manager Agent (SSM Agent) to all instances. Assign an instance profile to the instances with the required Systems Manager policies. Grant contractors access to the AWS Management Console through AWS IAM Identity Center.**

**Explanation:**

Systems Manager Session Manager provides secure, auditable access to instances without requiring SSH keys or open inbound ports. IAM Identity Center enables centralized management of contractor access across multiple AWS accounts with temporary credentials.

- **CORRECT:** "Deploy SSM Agent and use IAM Identity Center for centralized access" is the correct answer.
- **INCORRECT:** "Configure a bastion host in a public subnet with SSH key pairs" is incorrect because it increases operational overhead, requires managing SSH key pairs, and leaves an exposed attack surface.
- **INCORRECT:** "Use SSM Agent with temporary local IAM user credentials in each account" is incorrect because creating local IAM users for console access in each account increases credential management risk and does not align with centralized access management best practices.
- **INCORRECT:** "Set up AWS VPN or Direct Connect with IAM user credentials in each account" is incorrect because VPN/Direct Connect introduces unnecessary complexity and cost for this use case, and per-account IAM users are harder to manage than centralized IAM Identity Center.

**References:**
- https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html
- https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html
- https://digitalcloud.training/aws-systems-manager/

---

### Question 12 (Big Data Analytics – Redshift + Redshift Spectrum)

**Q:** Over 500 TB of data must be analyzed using standard SQL business intelligence tools. The dataset consists of a combination of structured data and unstructured data. The unstructured data is small but growing.

**Options:**

- Amazon DynamoDB with Amazon DynamoDB Accelerator (DAX)
- Amazon RDS MariaDB with Amazon Athena
- Amazon ElastiCache for Redis with cluster mode enabled
- **✅ Amazon Redshift with Amazon Redshift Spectrum**

**A:** **Amazon Redshift with Amazon Redshift Spectrum**

**Explanation:**

Amazon Redshift is an enterprise-level, petabyte scale, fully managed data warehousing service that supports standard SQL BI tools. Amazon Redshift Spectrum enables querying of structured and semi-structured data from files in Amazon S3 without loading the data into Redshift tables. Together they handle both the structured warehouse data and the unstructured S3 data.

- **CORRECT:** "Amazon Redshift with Amazon Redshift Spectrum" is the correct answer.
- **INCORRECT:** "Amazon RDS MariaDB with Amazon Athena" is incorrect. Amazon RDS is not suitable for analytics (OLAP) use cases; it is designed for transactional (OLTP) use cases.
- **INCORRECT:** "Amazon DynamoDB with Amazon DynamoDB Accelerator (DAX)" is incorrect. This is a non-relational database with a caching layer and is not suitable for an OLAP use case with SQL BI tools.
- **INCORRECT:** "Amazon ElastiCache for Redis with cluster mode enabled" is incorrect. This is an in-memory caching service designed for transactional performance, not large-scale analytics.

**References:**
- https://docs.aws.amazon.com/redshift/latest/dg/c_redshift_system_overview.html
- https://docs.aws.amazon.com/redshift/latest/dg/c-using-spectrum.html
- https://digitalcloud.training/amazon-redshift/

---

### Question 19 (ActiveMQ High Availability – Amazon MQ + RDS Multi-AZ + ASG)

**Q:** A Solutions Architect has been tasked with re-deploying an application running on AWS to enable high availability. The application processes messages that are received in an ActiveMQ queue running on a single Amazon EC2 instance. The application then processes the message and stores the result in a MySQL database running on a separate EC2 instance.

Which architecture offers the highest availability and low operational complexity?

**Options:**

- Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Launch an additional consumer EC2 instance in another Availability Zone. Use MySQL database replication to another Availability Zone.
- **✅ Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Create an Auto Scaling group for the consumer EC2 instances across two Availability Zones. Use an Amazon RDS for MySQL with Multi-AZ enabled.**
- Deploy a second Active MQ server to another Availability Zone. Launch an additional consumer EC2 instance in another Availability Zone. Use MySQL database replication to another Availability Zone.
- Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Launch an additional consumer EC2 instance in another Availability Zone. Use Amazon RDS for MySQL with Multi-AZ enabled.

**A:** **Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Create an Auto Scaling group for the consumer EC2 instances across two Availability Zones. Use an Amazon RDS for MySQL with Multi-AZ enabled.**

**Explanation:**

The correct answer offers the highest availability: Amazon MQ active/standby brokers across two AZs, an Auto Scaling group for the consumer EC2 instances across two AZs, and a Multi-AZ Amazon RDS MySQL database. It also maximizes the use of managed services, keeping operational complexity low.

- **CORRECT:** "Deploy Amazon MQ active/standby + ASG for consumers across 2 AZs + RDS Multi-AZ" is the correct answer.
- **INCORRECT:** "Deploy a second Active MQ server to another AZ with MySQL replication" is incorrect because self-managed ActiveMQ and MySQL replication increase operational complexity compared to managed services.
- **INCORRECT:** "Deploy Amazon MQ active/standby + single additional consumer EC2 + MySQL replication" is incorrect because a single additional EC2 instance (without an ASG) is not as resilient, and self-managed MySQL replication is operationally complex.
- **INCORRECT:** "Deploy Amazon MQ active/standby + single additional consumer EC2 + RDS Multi-AZ" is incorrect because a single additional EC2 consumer (without an ASG) does not provide the same availability as an Auto Scaling group across two AZs.

**References:**
- https://aws.amazon.com/architecture/well-architected/
- https://digitalcloud.training/aws-application-integration-services/
- https://digitalcloud.training/amazon-ec2-auto-scaling/
- https://digitalcloud.training/amazon-rds/

---

### Question 21 (Async EC2-to-Lambda Decoupling – Amazon SNS)

**Q:** An application running on Amazon EC2 needs to asynchronously invoke an AWS Lambda function to perform data processing. The services should be decoupled.

Which service can be used to decouple the compute services?

**Options:**

- **✅ Amazon SNS**
- Amazon MQ
- AWS Config
- AWS Step Functions

**A:** **Amazon SNS**

**Explanation:**

You can use a Lambda function to process Amazon Simple Notification Service notifications. Amazon SNS supports Lambda functions as a target for messages sent to a topic. This solution decouples the EC2 instance (publisher) from the Lambda function (subscriber) using a pub/sub messaging pattern.

- **CORRECT:** "Amazon SNS" is the correct answer.
- **INCORRECT:** "AWS Config" is incorrect. AWS Config is a service used for continuous compliance monitoring, not application decoupling.
- **INCORRECT:** "Amazon MQ" is incorrect. Amazon MQ is similar to SQS but is used for migrating existing applications that use standard messaging protocols (AMQP, MQTT, etc.) into AWS. SQS and SNS are recommended for new cloud-native applications.
- **INCORRECT:** "AWS Step Functions" is incorrect. AWS Step Functions is a workflow orchestration service. It is not the best solution for simple async decoupling between EC2 and Lambda.

**References:**
- https://docs.aws.amazon.com/lambda/latest/dg/with-sns.html
- https://aws.amazon.com/sns/features/
- https://digitalcloud.training/aws-lambda/
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 23 (Serverless GraphQL API – AWS AppSync)

**Q:** A Solutions Architect is tasked with designing a fully Serverless, Microservices based web application which requires the use of a GraphQL API to provide a single entry point to the application.

Which AWS managed service could the Solutions Architect use?

**Options:**

- API Gateway
- AWS Lambda
- **✅ AWS AppSync**
- Amazon Athena

**A:** **AWS AppSync**

**Explanation:**

AWS AppSync is a serverless GraphQL and Pub/Sub API service that simplifies building modern web and mobile applications. AWS AppSync GraphQL APIs simplify application development by providing a single endpoint to securely query or update data from multiple databases, microservices, and APIs.

- **CORRECT:** "AWS AppSync" is the correct answer.
- **INCORRECT:** "API Gateway" is incorrect. You cannot create GraphQL APIs on API Gateway; it supports REST and WebSocket APIs.
- **INCORRECT:** "Amazon Athena" is incorrect. Amazon Athena is a serverless query service where you can query S3 using SQL statements.
- **INCORRECT:** "AWS Lambda" is incorrect. AWS Lambda is a serverless compute service and is not designed to build or expose APIs.

**References:**
- https://aws.amazon.com/appsync/
- https://digitalcloud.training/category/aws-cheat-sheets/aws-networking-content-delivery/

---

### Question 31 (Global Static Website – CloudFront + S3)

**Q:** An organization wants to share regular updates about their charitable work using static webpages. The pages are expected to generate a large amount of views from around the world. The files are stored in an Amazon S3 bucket.

Which action should the solutions architect take to accomplish this?

**Options:**

- Use cross-Region replication to all Regions
- **✅ Use Amazon CloudFront with the S3 bucket as its origin**
- Use the geoproximity feature of Amazon Route 53
- Generate presigned URLs for the files

**A:** **Use Amazon CloudFront with the S3 bucket as its origin.**

**Explanation:**

Amazon CloudFront can be used to cache the files in edge locations around the world, improving the performance of the webpages for global users. CloudFront supports multiple origin configurations for S3, including OAI-restricted access and public website endpoints.

- **CORRECT:** "Use Amazon CloudFront with the S3 bucket as its origin" is the correct answer.
- **INCORRECT:** "Generate presigned URLs for the files" is incorrect as presigned URLs are used to restrict access, which is not a requirement here, and they do not improve global performance.
- **INCORRECT:** "Use cross-Region replication to all Regions" is incorrect as this does not provide a mechanism for directing users to the closest copy of the static webpages or caching content at edge locations.
- **INCORRECT:** "Use the geoproximity feature of Amazon Route 53" is incorrect as this does not include a solution for having multiple copies of the data in different geographic locations or caching at edge locations.

**References:**
- https://aws.amazon.com/premiumsupport/knowledge-center/cloudfront-serve-static-website/
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 43 (EC2 Load Testing – Detailed Monitoring)

**Q:** A company is testing a new web application that runs on Amazon EC2 instances. A Solutions Architect is performing load testing and must be able to analyze the performance of the web application with data at 1-minute intervals.

What should the Solutions Architect do to meet this requirement?

**Options:**

- Send Amazon CloudWatch logs to Amazon S3. Use Amazon Athena to perform the analysis.
- **✅ Enable detailed monitoring on all EC2 instances. Use Amazon CloudWatch metrics to perform the analysis.**
- Create an AWS CloudTrail trail and log data events. Use Amazon Athena to query the CloudTrail logs.
- Create an AWS Lambda function to fetch EC2 logs from Amazon CloudWatch Logs. Use Amazon CloudWatch metrics to perform the analysis.

**A:** **Enable detailed monitoring on all EC2 instances. Use Amazon CloudWatch metrics to perform the analysis.**

**Explanation:**

By default, instances are enabled for basic monitoring (5-minute intervals). Enabling detailed monitoring provides Amazon EC2 metrics at 1-minute intervals, which is required for granular performance analysis during load testing.

- **CORRECT:** "Enable detailed monitoring on all EC2 instances. Use Amazon CloudWatch metrics to perform the analysis" is the correct answer.
- **INCORRECT:** "Send Amazon CloudWatch logs to Amazon S3. Use Amazon Athena to perform the analysis" is incorrect. Sending logs to S3 and using Athena does not provide 1-minute metric granularity; you must enable detailed monitoring for this.
- **INCORRECT:** "Create an AWS Lambda function to fetch EC2 logs from Amazon CloudWatch Logs. Use Amazon CloudWatch metrics to perform the analysis" is incorrect. There is no need to use a Lambda function; detailed monitoring directly provides the required 1-minute metrics.
- **INCORRECT:** "Create an AWS CloudTrail trail and log data events. Use Amazon Athena to query the CloudTrail logs" is incorrect. CloudTrail records API calls, not EC2 performance metrics.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch-new.html
- https://digitalcloud.training/amazon-ec2/

---

### Question 44 (HPC MPI Workload – AWS Batch Multi-Node Parallel Jobs)

**Q:** An application that runs a computational fluid dynamics workload uses a tightly-coupled HPC architecture that uses the MPI protocol and runs across many nodes. A service-managed deployment is required.

Which deployment option is MOST suitable for provisioning and managing the resources required for this use case?

**Options:**

- **✅ Use AWS Batch to deploy a multi-node parallel job**
- Use Amazon EC2 Auto Scaling to deploy instances in multiple subnets
- Use AWS CloudFormation to deploy a Cluster Placement Group on EC2
- Use AWS Elastic Beanstalk to provision and manage the EC2 instances

**A:** **Use AWS Batch to deploy a multi-node parallel job.**

**Explanation:**

AWS Batch Multi-node parallel jobs enable you to run single jobs that span multiple Amazon EC2 instances. AWS Batch multi-node parallel jobs are compatible with any framework that supports IP-based, internode communication, such as MPI. This is the most efficient approach to deploy the resources required and supports the application requirements most effectively.

- **CORRECT:** "Use AWS Batch to deploy a multi-node parallel job" is the correct answer.
- **INCORRECT:** "Use Amazon EC2 Auto Scaling to deploy instances in multiple subnets" is incorrect. Auto Scaling is not purpose-built for tightly coupled HPC workloads with MPI inter-node communication.
- **INCORRECT:** "Use AWS CloudFormation to deploy a Cluster Placement Group on EC2" is incorrect. CloudFormation can deploy the infrastructure but does not manage job orchestration or scaling for HPC workloads.
- **INCORRECT:** "Use AWS Elastic Beanstalk to provision and manage the EC2 instances" is incorrect. Elastic Beanstalk is designed for web applications, not tightly-coupled HPC jobs requiring inter-node MPI communication.

**References:**
- https://d1.awsstatic.com/whitepapers/architecture/AWS-HPC-Lens.pdf
- https://docs.aws.amazon.com/batch/latest/userguide/multi-node-parallel-jobs.html

---

### Question 45 (Multiple VPCs + Direct Connect – Transit Gateway)

**Q:** Three Amazon VPCs are used by a company in the same region. The company has two AWS Direct Connect connections to two separate company offices and wishes to share these with all three VPCs. A Solutions Architect must recommend a solution.

**Options:**

- **✅ Associate the Direct Connect gateway to a transit gateway**
- Create a VPC peering connection between the VPCs and route entries for the Direct Connect Gateway
- Create a transit virtual interface between the Direct Connect gateway and each VPC
- Associate the Direct Connect gateway to a virtual private gateway in each VPC

**A:** **Associate the Direct Connect gateway to a transit gateway.**

**Explanation:**

You can manage a single connection for multiple VPCs or VPNs in the same Region by associating a Direct Connect gateway to a transit gateway. The solution requires:
- A transit gateway with VPC attachments
- A Direct Connect gateway
- An association between the Direct Connect gateway and the transit gateway
- A transit virtual interface attached to the Direct Connect gateway

- **CORRECT:** "Associate the Direct Connect gateway to a transit gateway" is the correct answer.
- **INCORRECT:** "Associate the Direct Connect gateway to a virtual private gateway in each VPC" is incorrect. For VPCs in the same region, a transit gateway is more appropriate and scalable than individual VPGs.
- **INCORRECT:** "Create a VPC peering connection between the VPCs and route entries for the Direct Connect Gateway" is incorrect. You cannot add route entries for a Direct Connect gateway directly to each VPC's route table.
- **INCORRECT:** "Create a transit virtual interface between the Direct Connect gateway and each VPC" is incorrect. The transit virtual interface is attached to the Direct Connect gateway on the connection side, not to individual VPCs.

**References:**
- https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
- https://digitalcloud.training/aws-direct-connect/

---

### Question 50 (DynamoDB Compliance Record – DynamoDB Streams + Lambda)

**Q:** Every time an item in an Amazon DynamoDB table is modified a record must be retained for compliance reasons. What is the most efficient solution to recording this information?

**Options:**

- **✅ Enable DynamoDB Streams. Configure an AWS Lambda function to poll the stream and record the modified item data to an Amazon S3 bucket.**
- Enable Amazon CloudWatch Logs. Configure an AWS Lambda function to monitor the log files and record deleted item data to an Amazon S3 bucket.
- Enable Amazon CloudTrail. Configure an Amazon EC2 instance to monitor activity in the CloudTrail log files and record changed items in another DynamoDB table.
- Enable DynamoDB Global Tables. Enable DynamoDB streams on the multi-region table and save the output directly to an Amazon S3 bucket.

**A:** **Enable DynamoDB Streams. Configure an AWS Lambda function to poll the stream and record the modified item data to an Amazon S3 bucket.**

**Explanation:**

Amazon DynamoDB Streams captures a time-ordered sequence of item-level modifications in any DynamoDB table and stores this information in a log for up to 24 hours. A Lambda function can poll the stream and write the records to S3 for long-term compliance storage.

- **CORRECT:** "Enable DynamoDB Streams. Configure an AWS Lambda function to poll the stream and record the modified item data to an Amazon S3 bucket" is the correct answer.
- **INCORRECT:** "Enable Amazon CloudWatch Logs" is incorrect. CloudWatch Logs does not capture DynamoDB item-level change data; Streams is the purpose-built feature for this.
- **INCORRECT:** "Enable Amazon CloudTrail" is incorrect. CloudTrail records API calls at the control plane level, not item-level data changes.
- **INCORRECT:** "Enable DynamoDB Global Tables" is incorrect. Global Tables is used for creating multi-region replicas of a DynamoDB table, not for recording item-level change history for compliance.

**References:**
- https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html
- https://digitalcloud.training/amazon-dynamodb/

---

### Question 52 (CloudFront IP Restriction – OAI + WAF)

**Q:** A website is running on Amazon EC2 instances and access is restricted to a limited set of IP ranges. A solutions architect is planning to migrate static content from the website to an Amazon S3 bucket and serve it through Amazon CloudFront. The IP restrictions must be maintained.

Which combination of steps will meet these requirements? (Select TWO.)

**Options:**

- Create an AWS WAF web ACL that includes the same IP restrictions that exist in the EC2 security group. Associate this new web ACL with the Amazon S3 bucket.
- Create an origin access identity (OAI) and associate it with the distribution. Generate presigned URLs that limit access to the OAI.
- **✅ Create an AWS WAF web ACL that includes the same IP restrictions that exist in the EC2 security group. Associate this new web ACL with the CloudFront distribution.**
- **✅ Create an origin access identity (OAI) and associate it with the distribution. Change the permissions in the bucket policy so that only the OAI can read the objects.**
- Attach the existing security group that contains the IP restrictions to the Amazon CloudFront distribution.

**A:** **Create an AWS WAF web ACL with IP restrictions and associate it with the CloudFront distribution** AND **Create an OAI and restrict the S3 bucket policy so only the OAI can read objects.**

**Explanation:**

To prevent users from bypassing CloudFront and accessing S3 directly, you use an OAI to restrict bucket access to CloudFront only. To enforce IP restrictions at the CloudFront layer, you associate a WAF web ACL with the distribution that includes the same IP allow/deny rules.

- **CORRECT:** "Create an origin access identity (OAI) and change bucket policy so only the OAI can read objects" is the correct answer.
- **CORRECT:** "Create an AWS WAF web ACL with IP restrictions and associate it with the CloudFront distribution" is the correct answer.
- **INCORRECT:** "Create an origin access identity (OAI) and generate presigned URLs that limit access to the OAI" is incorrect. Presigned URLs provide temporary access to specific objects; they cannot enforce IP restrictions at the CloudFront level.
- **INCORRECT:** "Create an AWS WAF web ACL and associate it with the Amazon S3 bucket" is incorrect. AWS WAF cannot be associated with an S3 bucket directly; it must be associated with a CloudFront distribution, ALB, or API Gateway.
- **INCORRECT:** "Attach the existing security group to the Amazon CloudFront distribution" is incorrect. You cannot attach a security group to a CloudFront distribution.

**References:**
- https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- https://docs.aws.amazon.com/waf/latest/developerguide/cloudfront-features.html
- https://digitalcloud.training/aws-waf-shield/
