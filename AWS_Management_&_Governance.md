## AWS Services Reference

| Service | Description |
|---|---|
| **AWS PrivateLink** | A service that enables private connectivity between VPCs, AWS services, and on-premises applications without exposing traffic to the public internet. |
| **AWS Direct Connect** | A dedicated network connection from your on-premises environment to AWS, providing more consistent network performance than internet-based connections. |
| **Amazon Kinesis Data Firehose** | A fully managed service for delivering real-time streaming data to destinations such as Amazon S3, Redshift, OpenSearch, and Splunk. |
| **AWS Storage Gateway** | A hybrid cloud storage service that gives on-premises applications access to virtually unlimited cloud storage by connecting on-premises environments to AWS storage services. |
| **Amazon EFS (Elastic File System)** | A fully managed, elastic NFS file system for use with AWS Cloud services and on-premises resources, designed exclusively for Linux-based workloads. |
| **Amazon EBS (Elastic Block Store)** | A high-performance block storage service designed for use with Amazon EC2, offering persistent storage with options for encryption and automated snapshots. |
| **Amazon S3 (Simple Storage Service)** | An object storage service offering industry-leading scalability, data availability, security, and performance for storing and retrieving any amount of data. |
| **AWS Snowball** | A physical data transport device that helps move terabytes to petabytes of data into and out of AWS without using the internet. |
| **AWS DataSync** | An online data transfer service that automates and accelerates moving data between on-premises storage and AWS storage services. |
| **AWS DMS (Database Migration Service)** | A service that helps you migrate databases to AWS quickly and securely, supporting both homogeneous and heterogeneous migrations. |
| **AWS DMS Serverless** | A serverless version of AWS DMS that automatically scales replication capacity based on workload demand, reducing operational overhead. |
| **NAT Gateway** | A managed AWS networking component that allows instances in a private subnet to initiate outbound internet traffic while preventing unsolicited inbound connections. |
| **Amazon SNS (Simple Notification Service)** | A fully managed pub/sub messaging and mobile notifications service for coordinating message delivery to subscribing endpoints and clients. |
| **Amazon SQS (Simple Queue Service)** | A fully managed message queuing service that enables decoupling and scaling of microservices, distributed systems, and serverless applications. |
| **Amazon SageMaker** | A fully managed service that provides tools to build, train, and deploy machine learning models for any use case with managed infrastructure and workflows. |
| **AWS Data Exchange** | A service that makes it easy for AWS customers to find, subscribe to, and use third-party data in the cloud. |
| **Amazon ECS (Elastic Container Service)** | A fully managed container orchestration service that makes it easy to deploy, manage, and scale containerized applications using Docker. |
| **AWS Fargate** | A serverless compute engine for containers that works with both Amazon ECS and Amazon EKS, removing the need to provision and manage servers. |
| **Amazon Aurora** | A fully managed relational database engine compatible with MySQL and PostgreSQL, offering up to 5x the throughput of MySQL and 3x that of PostgreSQL. |
| **Amazon RDS (Relational Database Service)** | A managed relational database service that makes it easy to set up, operate, and scale databases in the cloud, supporting multiple engine types. |
| **Amazon ElastiCache** | A fully managed in-memory caching service supporting Redis and Memcached, used to improve application performance by caching frequently accessed data. |
| **Amazon DynamoDB** | A fully managed, serverless NoSQL key-value and document database that delivers single-digit millisecond performance at any scale. |
| **Amazon CloudWatch** | A monitoring and observability service that provides data and actionable insights for AWS resources, applications, and services through metrics, logs, and alarms. |
| **Amazon OpenSearch Service** | A managed service for deploying, operating, and scaling OpenSearch clusters for log analytics, full-text search, and real-time application monitoring. |
| **AWS Config** | A service that continuously monitors and records AWS resource configurations and allows you to automate evaluation of recorded configurations against desired settings. |
| **AWS CloudTrail** | A service that enables governance, compliance, and operational and risk auditing of your AWS account by logging and retaining API calls and related events. |
| **Amazon CloudFront** | A fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency. |
| **AWS Service Catalog** | A service that enables organizations to create and manage catalogs of IT services approved for use on AWS, enabling self-service deployment and governance. |
| **Amazon S3 File Gateway** | A type of AWS Storage Gateway that provides a seamless way to connect on-premises applications to Amazon S3, with local caching for low-latency access. |

---

## AWS Management & Governance – Practice Questions

---

### Question 11

**Q:** A company needs to connect its on-premises data center network to a new virtual private cloud (VPC). There is a symmetrical internet connection of 100 Mbps in the data center network. The data transfer rate for an on-premises application is multiple gigabytes per day. Processing will be done using an Amazon Kinesis Data Firehose stream.

What should a solutions architect recommend for maximum performance?

**Options:**

- Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection.
- Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection.
- Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary.
- **✅ Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.**

**A:** **Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.**

**Explanation:**

Using AWS PrivateLink to create an interface endpoint will allow your traffic to traverse the AWS Global Backbone to allow maximum performance and security. Also by using an AWS Direct Connect cable you can ensure you have a dedicated cable to provide maximum performance and low latency to and from AWS.

- **CORRECT:** "Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection..." is the correct answer.
- **INCORRECT:** "Establish a peering connection between the on-premises network and the VPC..." is incorrect because VPC peering connections can only exist between two VPCs within the AWS Cloud.
- **INCORRECT:** "Get an AWS Snowball Edge Storage Optimized device..." is incorrect. AWS Snowball Edge is designed to be more of a one-time migration service.
- **INCORRECT:** "Establish an AWS Site-to-Site VPN connection..." is incorrect. This is a functional solution; however a physical connection would provide a much more reliable and performant solution.

**References:**
- https://aws.amazon.com/privatelink/
- https://digitalcloud.training/amazon-vpc/

---

### Question 28

**Q:** A company runs an application in a factory that has a small rack of physical compute resources. The application stores data on a network attached storage (NAS) device using the NFS protocol. The company requires a daily offsite backup of the application data.

Which solution can a Solutions Architect recommend to meet this requirement?

**Options:**

- Use an AWS Storage Gateway volume gateway with cached volumes on premises to replicate the data to Amazon S3.
- Create an IPSec VPN to AWS and configure the application to mount the Amazon EFS file system. Run a copy job to backup the data to EFS.
- Use an AWS Storage Gateway volume gateway with stored volumes on premises to replicate the data to Amazon S3.
- **✅ Use an AWS Storage Gateway file gateway hardware appliance on premises to replicate the data to Amazon S3.**

**A:** **Use an AWS Storage Gateway file gateway hardware appliance on premises to replicate the data to Amazon S3.**

**Explanation:**

The AWS Storage Gateway Hardware Appliance is a physical, standalone, validated server configuration for on-premises deployments. It comes pre-loaded with Storage Gateway software, and provides all the required CPU, memory, network, and SSD cache resources for creating and configuring File Gateway, Volume Gateway, or Tape Gateway. A file gateway is the correct type of appliance to use for this use case as it is suitable for mounting via the NFS and SMB protocols.

- **CORRECT:** "Use an AWS Storage Gateway file gateway hardware appliance on premises to replicate the data to Amazon S3" is the correct answer.
- **INCORRECT:** "Use an AWS Storage Gateway volume gateway with stored volumes on premises..." is incorrect. Volume gateways are used for block-based storage and this solution requires NFS (file-based storage).
- **INCORRECT:** "Use an AWS Storage Gateway volume gateway with cached volumes on premises..." is incorrect. Volume gateways are used for block-based storage and this solution requires NFS (file-based storage).
- **INCORRECT:** "Create an IPSec VPN to AWS and configure the application to mount the Amazon EFS file system..." is incorrect. It would be better to use a Storage Gateway which will automatically take care of synchronizing a copy of the data to AWS.

**References:**
- https://aws.amazon.com/storagegateway/hardware-appliance/
- https://digitalcloud.training/aws-storage-gateway/

---

### Question 49

**Q:** A company is deploying a fleet of Amazon EC2 instances running Linux across multiple Availability Zones within an AWS Region. The application requires a data storage solution that can be accessed by all of the EC2 instances simultaneously. The solution must be highly scalable and easy to implement. The storage must be mounted using the NFS protocol.

Which solution meets these requirements?

**Options:**

- Create an Amazon EBS volume and use EBS Multi-Attach to mount the volume to all EC2 instances across each Availability Zone.
- Create an Amazon RDS database and store the data in a BLOB format. Point the application instances to the RDS endpoint.
- Create an Amazon S3 bucket and create an S3 gateway endpoint to allow access to the file system using the NFS protocol.
- **✅ Create an Amazon EFS file system with mount targets in each Availability Zone. Configure the application instances to mount the file system.**

**A:** **Create an Amazon EFS file system with mount targets in each Availability Zone. Configure the application instances to mount the file system.**

**Explanation:**

Amazon EFS provides scalable file storage for use with Amazon EC2. You can use an EFS file system as a common data source for workloads and applications running on multiple instances. The EC2 instances can run in multiple AZs within a Region and the NFS protocol is used to mount the file system. With EFS you can create mount targets in each AZ for lower latency. The application instances in each AZ will mount the file system using the local mount target.

- **CORRECT:** "Create an Amazon EFS file system with mount targets in each Availability Zone. Configure the application instances to mount the file system" is the correct answer.
- **INCORRECT:** "Create an Amazon S3 bucket and create an S3 gateway endpoint to allow access to the file system using the NFS protocol" is incorrect. You cannot use NFS with S3 or with gateway endpoints.
- **INCORRECT:** "Create an Amazon EBS volume and use EBS Multi-Attach to mount the volume to all EC2 instances across each Availability Zone" is incorrect. You cannot use Amazon EBS Multi-Attach across multiple AZs.
- **INCORRECT:** "Create an Amazon RDS database and store the data in a BLOB format..." is incorrect. This is not a suitable storage solution for a file system that is mounted over NFS.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEFS.html
- https://digitalcloud.training/amazon-efs/

---

### Question 59

**Q:** A company runs an application on an Amazon EC2 instance that requires 250 GB of storage space. The application is not used often and has small spikes in usage on weekday mornings and afternoons. The disk I/O can vary with peaks hitting a maximum of 3,000 IOPS. A Solutions Architect must recommend the most cost-effective storage solution that delivers the performance required.

Which configuration should the Solutions Architect recommend?

**Options:**

- Amazon EBS Throughput Optimized HDD (st1)
- Amazon EBS Provisioned IOPS SSD (io1)
- Amazon EBS Cold HDD (sc1)
- **✅ Amazon EBS General Purpose SSD (gp2)**

**A:** **Amazon EBS General Purpose SSD (gp2)**

**Explanation:**

General Purpose SSD (gp2) volumes offer cost-effective storage that is ideal for a broad range of workloads. These volumes deliver single-digit millisecond latencies and the ability to burst to 3,000 IOPS for extended periods of time. Between a minimum of 100 IOPS (at 33.33 GiB and below) and a maximum of 16,000 IOPS (at 5,334 GiB and above), baseline performance scales linearly at 3 IOPS per GiB of volume size. In this configuration the volume will provide a baseline performance of 750 IOPS but will always be able to burst to the required 3,000 IOPS during periods of increased traffic.

- **CORRECT:** "Amazon EBS General Purpose SSD (gp2)" is the correct answer.
- **INCORRECT:** "Amazon EBS Provisioned IOPS SSD (io1)" is incorrect. The io1 volume type will be more expensive and is not necessary for the performance levels required.
- **INCORRECT:** "Amazon EBS Cold HDD (sc1)" is incorrect. The sc1 volume type is not going to deliver the performance requirements as it cannot burst to 3,000 IOPS.
- **INCORRECT:** "Amazon EBS Throughput Optimized HDD (st1)" is incorrect. The st1 volume type is not going to deliver the performance requirements as it cannot burst to 3,000 IOPS.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- https://digitalcloud.training/amazon-ebs/

---

### Question 30

**Q:** A logistics company needs to replicate ongoing data changes from an on-premises Microsoft SQL Server database to Amazon RDS for SQL Server. The volume of data to replicate varies throughout the day due to periodic spikes in activity. The company plans to use AWS Database Migration Service (AWS DMS) for this task. The solution must dynamically allocate capacity based on workload demand while keeping operational overhead low.

Which solution will meet these requirements?

**Options:**

- Create an AWS DMS replication instance with provisioned capacity in a Multi-AZ deployment to improve availability and fault tolerance.
- Use Amazon EC2 Spot Instances to host the AWS DMS replication instance and manually scale up or down based on replication needs.
- Deploy AWS DMS in an Amazon Elastic Kubernetes Service (Amazon EKS) cluster and use an autoscaler to adjust compute capacity during data spikes.
- **✅ Configure AWS DMS Serverless to create a replication task that scales its capacity automatically based on workload demand.**

**A:** **Configure AWS DMS Serverless to create a replication task that scales its capacity automatically based on workload demand.**

**Explanation:**

AWS DMS Serverless dynamically adjusts replication capacity in response to data volume changes, providing cost efficiency and reducing manual management.

- **CORRECT:** "Configure AWS DMS Serverless to create a replication task that scales its capacity automatically based on workload demand" is the correct answer.
- **INCORRECT:** "Deploy AWS DMS in an Amazon EKS cluster and use an autoscaler..." is incorrect because AWS DMS does not support deployment on Amazon EKS. Additionally, this solution introduces unnecessary complexity.
- **INCORRECT:** "Use Amazon EC2 Spot Instances to host the AWS DMS replication instance and manually scale up or down..." is incorrect because manually scaling replication tasks increases operational overhead and Spot Instances could be interrupted.
- **INCORRECT:** "Create an AWS DMS replication instance with provisioned capacity in a Multi-AZ deployment..." is incorrect because while Multi-AZ deployment enhances availability, it does not dynamically adjust capacity to match workload demand.

**References:**
- https://docs.aws.amazon.com/dms/latest/userguide/what-is-dms.html
- https://aws.amazon.com/dms/serverless/
- https://digitalcloud.training/aws-migration-services/

---

### Question 41

**Q:** An application consists of a web tier in a public subnet and a MySQL cluster hosted on Amazon EC2 instances in a private subnet. The MySQL instances must retrieve product data from a third-party provider over the internet. A Solutions Architect must determine a strategy to enable this access with maximum security and minimum operational overhead.

What should the Solutions Architect do to meet these requirements?

**Options:**

- Create a virtual private gateway and attach it to the VPC. Modify the private subnet route table to direct internet traffic to the virtual private gateway.
- Create an internet gateway and attach it to the VPC. Modify the private subnet route table to direct internet traffic to the internet gateway.
- Deploy a NAT instance in the private subnet. Direct all internet traffic to the NAT instance.
- **✅ Deploy a NAT gateway in the public subnet. Modify the route table in the private subnet to direct all internet traffic to the NAT gateway.**

**A:** **Deploy a NAT gateway in the public subnet. Modify the route table in the private subnet to direct all internet traffic to the NAT gateway.**

**Explanation:**

The MySQL clusters instances need to access a service on the internet. The most secure method of enabling this access with low operational overhead is to create a NAT gateway. When deploying a NAT gateway, the gateway itself should be deployed in a public subnet whilst the route table in the private subnet must be updated to point traffic to the NAT gateway ID.

- **CORRECT:** "Deploy a NAT gateway in the public subnet. Modify the route table in the private subnet to direct all internet traffic to the NAT gateway" is the correct answer.
- **INCORRECT:** "Deploy a NAT instance in the private subnet..." is incorrect. NAT instances require more operational overhead and need to be deployed in a public subnet.
- **INCORRECT:** "Create an internet gateway and attach it to the VPC. Modify the private subnet route table to direct internet traffic to the internet gateway" is incorrect. You cannot point the instances in the private subnet to an internet gateway as they do not have public IP addresses.
- **INCORRECT:** "Create a virtual private gateway and attach it to the VPC..." is incorrect. A virtual private gateway (VGW) is used with a VPN connection, not for connecting instances in private subnets to the internet.

**References:**
- https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- https://digitalcloud.training/amazon-vpc/

---

### Question 46

**Q:** A Solutions Architect has been tasked with migrating 30 TB of data from an on-premises data center within 20 days. The company has an internet connection that is limited to 25 Mbps and the data transfer cannot use more than 50% of the connection speed.

What should a Solutions Architect do to meet these requirements?

**Options:**

- Use a site-to-site VPN.
- Use AWS DataSync.
- Use AWS Storage Gateway.
- **✅ Use AWS Snowball.**

**A:** **Use AWS Snowball.**

**Explanation:**

Transferring 30 TB of data across a 25 Mbps connection (using only 12.5 Mbps) could take upwards of 200 days. Therefore, using the Internet connection will not meet the requirements and we can rule out any solution that uses the internet (all options except for Snowball). AWS Snowball is a physical device that is shipped to your office or data center. You can then load data onto it and ship it back to AWS where the data is uploaded to Amazon S3. Snowball is the only solution that will achieve the data migration requirements within the 20-day period.

- **CORRECT:** "Use AWS Snowball" is the correct answer.
- **INCORRECT:** "Use AWS DataSync" is incorrect. This uses the internet which will not meet the 20-day deadline.
- **INCORRECT:** "Use AWS Storage Gateway" is incorrect. This uses the internet which will not meet the 20-day deadline.
- **INCORRECT:** "Use a site-to-site VPN" is incorrect. This uses the internet which will not meet the 20-day deadline.

**References:**
- https://aws.amazon.com/snowball/
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 52

**Q:** A scientific research organization runs an on-premises simulation application that processes large datasets. The organization has migrated all simulation data to Amazon S3 to reduce costs. The simulation application requires low-latency storage access for seamless performance during processing tasks. The organization needs to design a storage solution that minimizes costs while maintaining the performance requirements of the application.

Which storage solution will meet these requirements in the MOST cost-effective way?

**Options:**

- Copy the data from Amazon S3 to Amazon FSx for Lustre. Use an Amazon FSx File Gateway to provide low-latency access for the on-premises application.
- Deploy a high-speed internet connection and configure the on-premises application to access the data directly from Amazon S3 using the S3 API for storage operations.
- Use AWS DataSync to copy frequently accessed data from Amazon S3 to an on-premises storage system. Configure the application to use the local storage for low-latency access.
- **✅ Use Amazon S3 File Gateway to provide low-latency storage for the on-premises application. The File Gateway will cache frequently accessed data locally.**

**A:** **Use Amazon S3 File Gateway to provide low-latency storage for the on-premises application. The File Gateway will cache frequently accessed data locally.**

**Explanation:**

S3 File Gateway provides a seamless and cost-effective way to access data stored in Amazon S3. It locally caches frequently accessed data, reducing latency while still leveraging the cost benefits of S3 storage.

- **CORRECT:** "Use Amazon S3 File Gateway to provide low-latency storage for the on-premises application..." is the correct answer.
- **INCORRECT:** "Use AWS DataSync to copy frequently accessed data from Amazon S3 to an on-premises storage system..." is incorrect because DataSync is designed for batch data transfer and is not suitable for providing continuous, low-latency access to S3 data.
- **INCORRECT:** "Copy the data from Amazon S3 to Amazon FSx for Lustre..." is incorrect because FSx for Lustre is optimized for high-performance workloads but is more expensive and introduces unnecessary complexity compared to S3 File Gateway.
- **INCORRECT:** "Deploy a high-speed internet connection and configure the on-premises application to access the data directly from Amazon S3..." is incorrect because accessing data directly from S3 over the internet does not meet the low-latency requirements.

**References:**
- https://docs.aws.amazon.com/storagegateway/latest/userguide/WhatIsStorageGateway.html
- https://docs.aws.amazon.com/datasync/latest/userguide/what-is-datasync.html
- https://digitalcloud.training/aws-storage-gateway/

---

### Question 60

**Q:** An educational content provider has accumulated several terabytes of learning resources in an Amazon S3 bucket located in a specific AWS Region. A partner organization, based in a different AWS Region, has been granted access to the S3 bucket to retrieve the resources for integration into its own platform. The content provider wants to minimize its data transfer costs when the partner organization accesses the S3 bucket.

Which solution will meet these requirements?

**Options:**

- Configure the bucket to use S3 Standard-IA storage to reduce access costs for the partner organization.
- Set up S3 Cross-Region Replication (CRR) to copy the learning resources to the partner organization's S3 bucket.
- Use S3 Transfer Acceleration to allow the partner organization to retrieve data from the bucket.
- **✅ Enable the Requester Pays feature on the content provider's S3 bucket.**

**A:** **Enable the Requester Pays feature on the content provider's S3 bucket.**

**Explanation:**

The Requester Pays feature shifts the data transfer costs from the content provider to the partner organization, thereby minimizing the content provider's expenses.

- **CORRECT:** "Enable the Requester Pays feature on the content provider's S3 bucket" is the correct answer.
- **INCORRECT:** "Use S3 Transfer Acceleration to allow the partner organization to retrieve data from the bucket" is incorrect. This solution optimizes data transfer speeds but does not specifically address minimizing the content provider's data transfer costs.
- **INCORRECT:** "Set up S3 Cross-Region Replication (CRR)..." is incorrect. While this enables data availability in the partner organization's Region, it introduces additional costs for cross-Region replication, which the content provider would incur.
- **INCORRECT:** "Configure the bucket to use S3 Standard-IA storage..." is incorrect. Changing the storage class to Standard-IA focuses on storage cost optimization and does not directly address minimizing data transfer costs.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/RequesterPaysBuckets.html
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 10

**Q:** A Solutions Architect is designing an application that will run on an Amazon EC2 instance. The application must asynchronously invoke an AWS Lambda function to analyze thousands of .CSV files. The services should be decoupled.

Which service can be used to decouple the compute services?

**Options:**

- Amazon OpsWorks
- Amazon Kinesis
- Amazon SWF
- **✅ Amazon SNS**

**A:** **Amazon SNS**

**Explanation:**

You can use a Lambda function to process Amazon Simple Notification Service notifications. Amazon SNS supports Lambda functions as a target for messages sent to a topic. This solution decouples the Amazon EC2 application from Lambda and ensures the Lambda function is invoked.

- **CORRECT:** "Amazon SNS" is the correct answer.
- **INCORRECT:** "Amazon SWF" is incorrect. The Simple Workflow Service (SWF) is used for process automation. It is not well suited to this requirement.
- **INCORRECT:** "Amazon Kinesis" is incorrect as this service is used for ingesting and processing real-time streaming data; it is not a suitable service to be used solely for invoking a Lambda function.
- **INCORRECT:** "Amazon OpsWorks" is incorrect as this service is used for configuration management of systems using Chef or Puppet.

**References:**
- https://docs.aws.amazon.com/lambda/latest/dg/with-sns.html
- https://digitalcloud.training/aws-application-integration-services/
- https://digitalcloud.training/aws-lambda/

---

### Question 33 (a)

**Q:** A computer scientist working for a university is looking to build a machine learning application which will use telemetry data to predict weather for a given area at a given time. This application would benefit from using managed services and will need to find a solution which uses third-party data within the application.

Which of the following combinations of services will deliver the best solution?

**Options:**

- Use Amazon SageMaker to build the machine learning part of the application and use AWS DataSync to gain access to the third-party telemetry data.
- Use a TensorFlow AMI from the AWS Marketplace to build the machine learning part of the application and use AWS DataSync to gain access to the third-party telemetry data.
- Use a TensorFlow AMI from the AWS Marketplace to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data.
- **✅ Use Amazon SageMaker to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data.**

**A:** **Use Amazon SageMaker to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data.**

**Explanation:**

Amazon SageMaker allows you to build, train, and deploy machine learning models for any use case with fully managed infrastructure, tools, and workflows. AWS Data Exchange allows you to gain access to third-party data sets across Automotive, Financial Services, Gaming, Healthcare & Life Sciences, Manufacturing, Marketing, Media & Entertainment, Retail, and many more industries.

- **CORRECT:** "Use Amazon SageMaker to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data" is the correct answer.
- **INCORRECT:** "Use Amazon SageMaker... and use AWS DataSync..." is incorrect. AWS DataSync is a secure, online service that automates and accelerates moving data between on-premises and AWS storage services. It does not give access to third-party data.
- **INCORRECT:** "Use a TensorFlow AMI from the AWS Marketplace... and use AWS DataSync..." is incorrect. Building an EC2 instance from a TensorFlow AMI would not involve using managed services and AWS DataSync does not give access to third-party data.
- **INCORRECT:** "Use a TensorFlow AMI from the AWS Marketplace... and use AWS Data Exchange..." is incorrect. Building an EC2 instance from a TensorFlow AMI would not involve using managed services.

**References:**
- https://aws.amazon.com/data-exchange/

---

### Question 4

**Q:** A law firm has recently moved an on-premises multi-tier web application to AWS. Currently, the web application is based on a containerized solution and is running inside Linux based EC2 instances which connect to a PostgreSQL database hosted on separate but dedicated EC2 instances. The company wishes to optimize operational efficiency and performance.

Which combination of actions should the solutions architect take? (Select TWO.)

**Options:**

- Set up Amazon ElastiCache between the web application and the PostgreSQL database.
- Set up an Amazon CloudFront distribution for the web application content.
- Migrate the web application to the same Amazon EC2 instances as the database.
- **✅ Migrate the PostgreSQL database to Amazon Aurora.**
- **✅ Migrate the web application to be hosted on AWS Fargate with Amazon Elastic Container Service (Amazon ECS).**

**A:** **Migrate the PostgreSQL database to Amazon Aurora** and **Migrate the web application to be hosted on AWS Fargate with Amazon Elastic Container Service (Amazon ECS).**

**Explanation:**

Amazon Aurora is a fully managed relational database engine that's compatible with MySQL and PostgreSQL. With some workloads, Aurora can deliver up to five times the throughput of MySQL and up to three times the throughput of PostgreSQL without requiring changes to most of your existing applications. Amazon ECS is a fully managed container orchestration service. In the case of Fargate, the solution is serverless, so it massively reduces operational overhead.

- **CORRECT:** "Migrate the PostgreSQL database to Amazon Aurora" and "Migrate the web application to be hosted on AWS Fargate with Amazon ECS" are the correct answers.
- **INCORRECT:** "Migrate the web application to the same Amazon EC2 instances as the database" is incorrect. This might reduce cost but doesn't offer any other advantages.
- **INCORRECT:** "Set up an Amazon CloudFront distribution for the web application content" is incorrect. CloudFront helps with caching content globally for better performance but does not help reduce the operational overhead of this solution.
- **INCORRECT:** "Set up Amazon ElastiCache between the web application and the PostgreSQL database" is incorrect. Caching will only help when you have hot data segments and does not reduce the operational overhead of this solution.

**References:**
- https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html
- https://digitalcloud.training/amazon-aurora/
- https://digitalcloud.training/amazon-ecs-and-eks/

---

### Question 8

**Q:** A company stores its application logs in an Amazon CloudWatch Logs log group. A new policy requires the company to store all application logs in Amazon OpenSearch Service (Amazon Elasticsearch Service) in near-real time.

Which solution will meet this requirement with the LEAST operational overhead?

**Options:**

- Create an AWS Lambda function. Use the log group to invoke the function to write the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service).
- Create an Amazon Kinesis Data Firehose delivery stream. Configure the log group as the delivery stream's source. Configure Amazon OpenSearch Service as the delivery stream's destination.
- Install and configure Amazon Kinesis Agent on each application server to deliver the logs to Amazon Kinesis Data Streams. Configure Kinesis Data Streams to deliver the logs to Amazon OpenSearch Service.
- **✅ Configure a CloudWatch Logs subscription to stream the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service).**

**A:** **Configure a CloudWatch Logs subscription to stream the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service).**

**Explanation:**

You can configure a CloudWatch Logs log group to stream data it receives to your Amazon OpenSearch Service cluster in near real-time through a CloudWatch Logs subscription. This is the solution that requires the least operational overhead. Subscription filters can also be created for Kinesis, Kinesis Data Firehose, and AWS Lambda.

- **CORRECT:** "Configure a CloudWatch Logs subscription to stream the logs to Amazon OpenSearch Service" is the correct answer.
- **INCORRECT:** "Create an Amazon Kinesis Data Firehose delivery stream..." is incorrect. This is a possible solution but requires more operational overhead as it includes an additional service which must also be configured and managed.
- **INCORRECT:** "Create an AWS Lambda function. Use the log group to invoke the function to write the logs to Amazon OpenSearch Service" is incorrect. This would require more operational overhead as you must write and manage the code for the function yourself.
- **INCORRECT:** "Install and configure Amazon Kinesis Agent on each application server..." is incorrect. Since the requirement is to dump the logs into OpenSearch and no further computation is needed, Firehose is a better candidate here.

**References:**
- https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_OpenSearch_Stream.html
- https://digitalcloud.training/amazon-cloudwatch/
- https://digitalcloud.training/amazon-opensearch/

---

### Question 9

**Q:** An application that is being installed on an Amazon EC2 instance requires a persistent block storage volume. The data must be encrypted at rest and regular volume-level backups must be automated.

Which solution options should be used?

**Options:**

- Use server-side encryption on an Amazon S3 bucket and use Cross-Region-Replication to backup on a schedule.
- Use an encrypted Amazon EC2 instance store and copy the data to another EC2 instance using a cron job and a batch script.
- Use an encrypted Amazon EFS filesystem and use an Amazon CloudWatch Events rule to start a backup copy of data using AWS Lambda.
- **✅ Use an encrypted Amazon EBS volume and use Data Lifecycle Manager to automate snapshots.**

**A:** **Use an encrypted Amazon EBS volume and use Data Lifecycle Manager to automate snapshots.**

**Explanation:**

For block storage the Solutions Architect should use either Amazon EBS or EC2 instance store. However, the instance store is non-persistent so EBS must be used. With EBS you can encrypt your volume and automate volume-level backups using snapshots that are run by Data Lifecycle Manager.

- **CORRECT:** "Use an encrypted Amazon EBS volume and use Data Lifecycle Manager to automate snapshots" is the correct answer.
- **INCORRECT:** "Use an encrypted Amazon EFS filesystem and use an Amazon CloudWatch Events rule to start a backup copy of data using AWS Lambda" is incorrect. EFS is not block storage; it is a file-level storage service.
- **INCORRECT:** "Use server-side encryption on an Amazon S3 bucket and use Cross-Region-Replication to backup on a schedule" is incorrect. Amazon S3 is an object-based storage system, not a block-based storage system.
- **INCORRECT:** "Use an encrypted Amazon EC2 instance store and copy the data to another EC2 instance using a cron job and a batch script" is incorrect as the EC2 instance store is a non-persistent volume.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes.html
- https://digitalcloud.training/amazon-ebs/

---

### Question 11 (b)

**Q:** A financial services company has a large, multi-Region footprint on AWS. A recent security audit highlighted some issues that must be addressed. The company must track all configuration changes affecting AWS resources and have detailed records of who has accessed the AWS environment. The data should include information such as which user has logged in and which API calls they made.

What actions should a Solutions Architect take to meet these requirements?

**Options:**

- Use AWS Config to track configuration changes and Amazon EventBridge to record API calls and track access patterns in the AWS Cloud.
- Use Amazon CloudWatch to track configuration changes and AWS Config to record API calls and track access patterns in the AWS Cloud.
- Use Amazon Macie to track configuration changes and Amazon CloudTrail to record API calls and track access patterns in the AWS Cloud.
- **✅ Use AWS Config to track configuration changes and AWS CloudTrail to record API calls and track access patterns in the AWS Cloud.**

**A:** **Use AWS Config to track configuration changes and AWS CloudTrail to record API calls and track access patterns in the AWS Cloud.**

**Explanation:**

AWS Config is a service used to track and remediate any unauthorized configuration changes made within your AWS Account. AWS CloudTrail keeps detailed logs of all API calls made within the account such as who logged in, which AWS Identity and Access Management (IAM) role is being used and also how they interact with the AWS Cloud.

- **CORRECT:** "Use AWS Config to track configuration changes and AWS CloudTrail to record API calls and track access patterns in the AWS Cloud" is the correct answer.
- **INCORRECT:** "Use Amazon CloudWatch to track configuration changes and AWS Config to record API calls and track access patterns in the AWS Cloud" is incorrect. Amazon CloudWatch does not track configuration changes; it tracks performance metrics.
- **INCORRECT:** "Use AWS Config to track configuration changes and Amazon EventBridge to record API calls and track access patterns in the AWS Cloud" is incorrect. Although AWS Config would work in this context, Amazon EventBridge is not the right service for recording API calls and tracking access patterns.
- **INCORRECT:** "Use Amazon Macie to track configuration changes and Amazon CloudTrail to record API calls and track access patterns in the AWS Cloud" is incorrect. Amazon Macie is used with Amazon S3 to detect and protect sensitive data.

**References:**
- https://aws.amazon.com/config
- https://digitalcloud.training/aws-config/

---

### Question 12

**Q:** A company wants to improve its ability to clone large amounts of production data into a test environment in the same AWS Region. The data is stored in Amazon EC2 instances on Amazon Elastic Block Store (Amazon EBS) volumes. A solutions architect needs to minimize the time that is required to clone the production data into the test environment.

Which solution will meet these requirements?

**Options:**

- Take EBS snapshots of the production EBS volumes. Restore the snapshots onto EC2 instance store volumes in the test environment.
- Take EBS snapshots of the production EBS volumes. Create and initialize new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment before restoring the volumes from the production EBS snapshots.
- Configure the production EBS volumes to use the EBS Multi-Attach feature. Take EBS snapshots of the production EBS volumes. Attach the production EBS volumes to the EC2 instances in the test environment.
- **✅ Take EBS snapshots of the production EBS volumes. Turn on the EBS fast snapshot restore feature on the EBS snapshots. Restore the snapshots into new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment.**

**A:** **Take EBS snapshots of the production EBS volumes. Turn on the EBS fast snapshot restore feature on the EBS snapshots. Restore the snapshots into new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment.**

**Explanation:**

Amazon EBS fast snapshot restore (FSR) enables you to create a volume from a snapshot that is fully initialized at creation. This eliminates the latency of I/O operations on a block when it is accessed for the first time.

- **CORRECT:** "Take EBS snapshots of the production EBS volumes. Turn on the EBS fast snapshot restore feature on the EBS snapshots. Restore the snapshots into new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment" is the correct answer.
- **INCORRECT:** "Take EBS snapshots of the production EBS volumes. Restore the snapshots onto EC2 instance store volumes in the test environment" is incorrect. You cannot restore EBS snapshots to instance store volumes.
- **INCORRECT:** "Take EBS snapshots of the production EBS volumes. Create and initialize new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment before restoring the volumes from the production EBS snapshots" is incorrect. This solution may take longer and may not have the consistent performance offered with the correct answer.
- **INCORRECT:** "Configure the production EBS volumes to use the EBS Multi-Attach feature..." is incorrect. Amazon EBS Multi-Attach enables you to attach a single Provisioned IOPS SSD volume to multiple instances in the same Availability Zone — this does not help with cloning production data into a test environment.

**References:**
- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-fast-snapshot-restore.html
- https://digitalcloud.training/amazon-ebs/

---

### Question 17

**Q:** The database layer of an on-premises web application is being migrated to AWS. The database uses a multi-threaded, in-memory caching layer to improve performance for repeated queries. Which service should be used?

**Options:**

- Amazon DynamoDB DAX
- Amazon ElastiCache Redis
- Amazon RDS MySQL
- **✅ Amazon ElastiCache Memcached**

**A:** **Amazon ElastiCache Memcached**

**Explanation:**

Amazon ElastiCache with the Memcached engine is an in-memory database that can be used as a database caching layer. The Memcached engine supports multiple cores and threads and large nodes.

- **CORRECT:** "Amazon ElastiCache Memcached" is the correct answer.
- **INCORRECT:** "Amazon ElastiCache Redis" is incorrect. The Redis engine does not support multiple CPU cores or threads.
- **INCORRECT:** "Amazon DynamoDB DAX" is incorrect. Amazon DynamoDB Accelerator (DAX) is a database cache that should be used with DynamoDB only.
- **INCORRECT:** "Amazon RDS MySQL" is incorrect as this is not an example of an in-memory database that can be used as a database caching layer.

**References:**
- https://aws.amazon.com/elasticache/redis-vs-memcached/
- https://digitalcloud.training/amazon-elasticache/

---

### Question 23

**Q:** A company is deploying a new web application that will run on Amazon EC2 instances in an Auto Scaling group across multiple Availability Zones. The application requires a shared storage solution that can be accessed by all EC2 instances simultaneously.

Which solution requires the LEAST amount of effort?

**Options:**

- Create a shared Amazon Block Store (Amazon EBS) volume and mount it on the individual Amazon EC2 instances.
- Create a volume gateway using AWS Storage Gateway to host the data and mount it to the Auto Scaling group.
- Create an Amazon S3 bucket to store the web content and use Amazon CloudFront to deliver the content.
- **✅ Create an Amazon Elastic File System (Amazon EFS) file system and mount it on the individual Amazon EC2 instances.**

**A:** **Create an Amazon Elastic File System (Amazon EFS) file system and mount it on the individual Amazon EC2 instances.**

**Explanation:**

Amazon EFS is a fully-managed service that makes it easy to set up, scale, and cost-optimize file storage in the Amazon Cloud. EFS file systems are accessible to Amazon EC2 instances via a file system interface and are well suited for attaching shared filesystems to multiple EC2 instances across multiple Availability Zones.

- **CORRECT:** "Create an Amazon Elastic File System (Amazon EFS) file system and mount it on the individual Amazon EC2 instances" is the correct answer.
- **INCORRECT:** "Create an Amazon S3 bucket to store the web content and use Amazon CloudFront to deliver the content" is incorrect as this may require more effort in terms of reprogramming the application to use S3.
- **INCORRECT:** "Create a shared Amazon Block Store (Amazon EBS) volume and mount it on the individual Amazon EC2 instances" is incorrect. You can multi-attach an EBS volume to multiple instances, but only within a single Availability Zone.
- **INCORRECT:** "Create a volume gateway using AWS Storage Gateway to host the data and mount it to the Auto Scaling group" is incorrect as a storage gateway is used on-premises.

**References:**
- https://aws.amazon.com/efs/faq/
- https://digitalcloud.training/amazon-efs/

---

### Question 31

**Q:** A global financial services company is currently operating a three-tier web application to handle their main customer-facing website. This application uses several Amazon EC2 instances behind an Application Load Balancer and an Amazon DynamoDB database. Due to recent customer complaints of slow loading times, their Solutions Architect has been asked to implement changes to solve this problem, without rearchitecting the core application components.

Which combination of actions should the solutions architect take to accomplish this? (Select TWO.)

**Options:**

- Migrate the web application to be hosted on a containerized solution using AWS Fargate.
- Migrate the entire application stack to AWS Elastic Beanstalk with both web server and worker environments.
- Migrate the DynamoDB database to Amazon Aurora with a multi-AZ deployment model.
- **✅ Set up an Amazon DynamoDB Accelerator (DAX) cluster in front of the DynamoDB table.**
- **✅ Create a CloudFront distribution and place it in front of the Application Load Balancer.**

**A:** **Set up an Amazon DynamoDB Accelerator (DAX) cluster in front of the DynamoDB table** and **Create a CloudFront distribution and place it in front of the Application Load Balancer.**

**Explanation:**

A CloudFront distribution would cache content in one of the many global edge locations, ensuring that any customer access to the content will be accessing it at a much lower latency compared to using the origin directly. DynamoDB has a built-in caching solution known as DynamoDB Accelerator (DAX). If your application is serving traffic from a DynamoDB database and is struggling to scale, you can use the DAX cluster to provide significantly improved read performance.

- **CORRECT:** "Create a CloudFront distribution and place it in front of the Application Load Balancer" is a correct answer.
- **CORRECT:** "Set up an Amazon DynamoDB Accelerator (DAX) cluster in front of the DynamoDB table" is also a correct answer.
- **INCORRECT:** "Migrate the entire application stack to AWS Elastic Beanstalk with both web server and worker environments" is incorrect. Migrating the entire application to AWS Elastic Beanstalk would require rearchitecting and would not necessarily improve the latency of the application for end users.
- **INCORRECT:** "Migrate the DynamoDB database to Amazon Aurora with a multi-AZ deployment model" is incorrect. Refactoring the application to move from a No-SQL database (DynamoDB) to a SQL database (Amazon Aurora) would take significant application and code changes.
- **INCORRECT:** "Migrate the web application to be hosted on a containerized solution using AWS Fargate" is incorrect. The application does not currently use containers; changing the application to use a containerized compute layer would also require architectural changes.

**References:**
- https://aws.amazon.com/cloudfront/
- https://digitalcloud.training/amazon-cloudfront/

---

### Question 33 (b)

**Q:** A health tech company runs a multi-tier medical records application in the AWS Cloud, which operates across three Availability Zones. The application architecture includes an Application Load Balancer, application servers on EC2 instances, a PostgreSQL database on EC2 instances, and session data stored on EC2 instances. The company anticipates a sharp surge in application traffic due to a new partnership. The company needs to scale to accommodate future application capacity demands and ensure high availability and fault tolerance.

Which solution will meet these requirements?

**Options:**

- Migrate the PostgreSQL database to Amazon Aurora with PostgreSQL compatibility with a single AZ deployment. Use Amazon ElastiCache for Memcached to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones.
- Keep the PostgreSQL database on EC2 instance. Use Amazon ElastiCache for Redis to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones.
- Migrate the PostgreSQL database to Amazon DynamoDB. Use DynamoDB Accelerator (DAX) to cache reads. Store the session data in DynamoDB. Migrate the application server to an Auto Scaling group across three Availability Zones.
- **✅ Migrate the PostgreSQL database to Amazon RDS for PostgreSQL with a Multi-AZ DB instance deployment. Use Amazon ElastiCache for Redis with a replication group to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones.**

**A:** **Migrate the PostgreSQL database to Amazon RDS for PostgreSQL with a Multi-AZ DB instance deployment. Use Amazon ElastiCache for Redis with a replication group to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones.**

**Explanation:**

This solution fulfills all the requirements. Amazon RDS with Multi-AZ instances provides high availability and failover support for DB instances. ElastiCache for Redis supports storing session state and read caching with high availability through replication groups.

- **CORRECT:** "Migrate the PostgreSQL database to Amazon RDS for PostgreSQL with a Multi-AZ DB instance deployment. Use Amazon ElastiCache for Redis with a replication group..." is the correct answer.
- **INCORRECT:** "Migrate the PostgreSQL database to Amazon Aurora with PostgreSQL compatibility with a single AZ deployment..." is incorrect. Using a single AZ deployment doesn't provide the high availability across multiple AZs the company wants. Also, while ElastiCache for Memcached provides caching, it does not support session state replication.
- **INCORRECT:** "Migrate the PostgreSQL database to Amazon DynamoDB..." is incorrect. DynamoDB is a high-performance, scalable NoSQL database; it is not a drop-in replacement for a relational database like PostgreSQL.
- **INCORRECT:** "Keep the PostgreSQL database on EC2 instance..." is incorrect. Although the EC2 instance can run the PostgreSQL database, it does not provide the same level of managed service benefits like automatic patching, backups, and high availability with Multi-AZ deployments.

**References:**
- https://aws.amazon.com/rds/features/multi-az/
- https://aws.amazon.com/elasticache/redis/
- https://aws.amazon.com/ec2/autoscaling/
- https://digitalcloud.training/amazon-elasticache/

---

### Question 49 (b)

**Q:** An e-commerce company has developed a new application which has been successfully deployed on AWS. For an upcoming sale, the company is expecting a huge rise in traffic and while testing for the expected load it has been identified that the database layer is a bottleneck. The current application stack is Amazon Aurora PostgreSQL database with an AWS Lambda compute layer fronted by API Gateway. A solutions architect must recommend improvements to scalability whilst minimizing operational overhead.

Which solution will meet these requirements?

**Options:**

- Change the platform from Aurora to Amazon DynamoDB. Provision a DynamoDB Accelerator (DAX) cluster. Use the DAX client SDK to point the existing DynamoDB API calls at the DAX cluster.
- Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using Amazon SNS.
- Refactor the Lambda function code to Apache Tomcat code that runs on Amazon EC2 instances. Connect the database by using native Java Database Connectivity (JDBC) drivers.
- **✅ Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using an Amazon SQS queue.**

**A:** **Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using an Amazon SQS queue.**

**Explanation:**

With Amazon SQS, you can offload tasks from one component of your application by sending them to a queue and processing them asynchronously. Lambda polls the queue and invokes your Lambda function synchronously with an event that contains queue messages, allowing the database writes to be queued and processed at a manageable rate.

- **CORRECT:** "Set up two Lambda functions... Integrate the Lambda functions by using an Amazon SQS queue" is the correct answer.
- **INCORRECT:** "Refactor the Lambda function code to Apache Tomcat code that runs on Amazon EC2 instances..." is incorrect. This would increase operational overhead and move away from the serverless architecture.
- **INCORRECT:** "Change the platform from Aurora to Amazon DynamoDB..." is incorrect. Migrating from a relational database to a NoSQL database would require significant application refactoring.
- **INCORRECT:** "Set up two Lambda functions... Integrate the Lambda functions by using Amazon SNS" is incorrect. SNS is a push-based notification service and does not provide the queuing and rate-limiting capabilities that SQS provides.

**References:**
- https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html
- https://digitalcloud.training/aws-lambda/
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 2

**Q:** An international software firm provides its clients with custom solutions and tools designed for efficient data collection and analysis on AWS. The firm intends to centrally manage and distribute these software tools to its clients, enabling them to deploy and use the tools independently.

Which solution would best satisfy these requirements?

**Options:**

- Create AWS Config rules for the clients.
- Create AWS CloudFormation stacks for the clients.
- Create AWS Systems Manager documents for the clients.
- **✅ Create AWS Service Catalog portfolios for the clients.**

**A:** **Create AWS Service Catalog portfolios for the clients.**

**Explanation:**

AWS Service Catalog enables organizations to create and manage catalogs of IT services that are approved for use on AWS. It allows centrally managed service portfolios, which clients can use on a self-service basis. AWS Service Catalog provides a single location where organizations can centrally manage catalogs of IT services, which simplifies the organizational process and helps ensure compliance.

- **CORRECT:** "Create AWS Service Catalog portfolios for the clients" is the correct answer.
- **INCORRECT:** "Create AWS CloudFormation stacks for the clients" is incorrect. While AWS CloudFormation is a powerful service for infrastructure as code (IaC), it doesn't provide a straightforward way for clients to discover and use shared tools or solutions for self-service deployment.
- **INCORRECT:** "Create AWS Systems Manager documents for the clients" is incorrect. AWS Systems Manager documents define the actions that Systems Manager performs on your managed instances; it isn't designed to centrally manage and distribute software tools on a self-service basis.
- **INCORRECT:** "Create AWS Config rules for the clients" is incorrect. AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. It isn't designed to centrally manage and distribute software tools or solutions.

**References:**
- https://aws.amazon.com/servicecatalog/
- https://digitalcloud.training/aws-service-catalog/

---

### Question 3

**Q:** A company has refactored a legacy application to run as two microservices using Amazon ECS. The application processes data in two parts and the second part of the process takes longer than the first.

How can a solutions architect integrate the microservices and allow them to scale independently?

**Options:**

- Implement code in microservice 1 to publish data to an Amazon SNS topic. Implement code in microservice 2 to subscribe to this topic.
- Implement code in microservice 1 to send data to Amazon Kinesis Data Firehose. Implement code in microservice 2 to read from Kinesis Data Firehose.
- Implement code in microservice 1 to send data to an Amazon S3 bucket. Use S3 event notifications to invoke microservice 2.
- **✅ Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue.**

**A:** **Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue.**

**Explanation:**

This is a good use case for Amazon SQS. The microservices must be decoupled so they can scale independently. An Amazon SQS queue will enable microservice 1 to add messages to the queue. Microservice 2 can then process the messages when it is ready (at its own pace), and the second part of the process takes longer, so the queue acts as a buffer.

- **CORRECT:** "Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue" is the correct answer.
- **INCORRECT:** "Implement code in microservice 1 to send data to an Amazon S3 bucket. Use S3 event notifications to invoke microservice 2" is incorrect as a message queue would be preferable to an S3 bucket in this scenario.
- **INCORRECT:** "Implement code in microservice 1 to publish data to an Amazon SNS topic. Implement code in microservice 2 to subscribe to this topic" is incorrect as notifications to topics are push-based and cannot queue work items for microservice 2 to process at its own rate.
- **INCORRECT:** "Implement code in microservice 1 to send data to Amazon Kinesis Data Firehose. Implement code in microservice 2 to read from Kinesis Data Firehose" is incorrect as this is not how Firehose is designed to work.

**References:**
- https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 9 (b)

**Q:** A Solutions Architect needs a solution for hosting a website that will be used by a development team. The website contents will consist of HTML, CSS, client-side JavaScript, and images.

Which solution is MOST cost-effective?

**Options:**

- Use a Docker container to host the website on AWS Fargate.
- Launch an Amazon EC2 instance and host the website there.
- Create an Application Load Balancer with an AWS Lambda target.
- **✅ Create an Amazon S3 bucket and host the website there.**

**A:** **Create an Amazon S3 bucket and host the website there.**

**Explanation:**

Amazon S3 can be used for hosting static websites and cannot be used for dynamic content. In this case the content is purely static with client-side code running. Therefore, an S3 static website is the most cost-effective solution.

- **CORRECT:** "Create an Amazon S3 bucket and host the website there" is the correct answer.
- **INCORRECT:** "Launch an Amazon EC2 instance and host the website there" is incorrect. This will be more expensive as it uses an EC2 instance.
- **INCORRECT:** "Use a Docker container to host the website on AWS Fargate" is incorrect. A static website on S3 is sufficient for this use case and will be more cost-effective than Fargate.
- **INCORRECT:** "Create an Application Load Balancer with an AWS Lambda target" is incorrect. This is also a more expensive solution and unnecessary for this use case.

**References:**
- https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 32

**Q:** A company operates a production web application that uses an Amazon RDS MySQL database. The database has automated, non-encrypted daily backups. To increase the security of the data, it has been decided that encryption should be enabled for backups.

What should be done to enable encryption for future backups?

**Options:**

- Enable default encryption for the Amazon S3 bucket where backups are stored.
- Modify the backup section of the database configuration to toggle the Enable encryption check box.
- Enable an encrypted read replica on RDS for MySQL. Promote the encrypted read replica to primary. Remove the original database instance.
- **✅ Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot.**

**A:** **Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot.**

**Explanation:**

Amazon RDS uses snapshots for backup. Snapshots are encrypted when created only if the database is encrypted and you can only select encryption for the database when you first create it. However, you can create an encrypted copy of a snapshot. You can restore using that snapshot which creates a new DB instance that has encryption enabled. From that point on encryption will be enabled for all automated backups.

- **CORRECT:** "Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot" is the correct answer.
- **INCORRECT:** "Enable an encrypted read replica on RDS for MySQL. Promote the encrypted read replica to primary. Remove the original database instance" is incorrect as you cannot create an encrypted read replica of an unencrypted instance.
- **INCORRECT:** "Modify the backup section of the database configuration to toggle the Enable encryption check box" is incorrect as you cannot add encryption for an existing database.
- **INCORRECT:** "Enable default encryption for the Amazon S3 bucket where backups are stored" is incorrect because you do not have access to the S3 bucket in which snapshots are stored.

**References:**
- https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- https://digitalcloud.training/amazon-rds/

---

### Question 37

**Q:** An application allows users to upload and download files. Files older than 2 years will be accessed less frequently. A solutions architect needs to ensure that the application can scale to any number of files while maintaining high availability and durability.

Which scalable solutions should the solutions architect recommend?

**Options:**

- Store the files in Amazon Elastic Block Store (EBS) volumes. Schedule snapshots of the volumes. Use the snapshots to archive data older than 2 years.
- Store the files in Amazon Elastic Block Store (EBS) volumes. Create a lifecycle policy to move files older than 2 years to Amazon S3 Glacier.
- Store the files on Amazon Elastic File System (EFS) with a lifecycle policy that moves objects older than 2 years to EFS Infrequent Access (EFS IA).
- **✅ Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA).**

**A:** **Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA).**

**Explanation:**

S3 Standard-IA is for data that is accessed less frequently, but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval charge. Amazon S3 can scale infinitely and is highly available and durable.

- **CORRECT:** "Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)" is the correct answer.
- **INCORRECT:** "Store the files on Amazon Elastic File System (EFS) with a lifecycle policy that moves objects older than 2 years to EFS Infrequent Access (EFS IA)" is incorrect. With EFS you can transition to EFS IA but this is not as scalable as S3.
- **INCORRECT:** "Store the files in Amazon Elastic Block Store (EBS) volumes. Schedule snapshots of the volumes. Use the snapshots to archive data older than 2 years" is incorrect. You cannot identify individual files within a snapshot.
- **INCORRECT:** "Store the files in Amazon Elastic Block Store (EBS) volumes. Create a lifecycle policy to move files older than 2 years to Amazon S3 Glacier" is incorrect. You cannot archive files from EBS directly to S3 Glacier using a lifecycle policy.

**References:**
- https://aws.amazon.com/s3/storage-classes/
- https://digitalcloud.training/amazon-s3-and-glacier/

---

### Question 43

**Q:** An on-premises server runs a MySQL database and will be migrated to the AWS Cloud. The company requires a managed solution that supports high availability and automatic failover in the event of the loss of an Availability Zone.

Which solution is the BEST fit for these requirements?

**Options:**

- Use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon RDS MySQL. Use the Schema Conversion Tool (SCT) to enable conversion from MySQL to Amazon RDS.
- Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon EC2 MySQL Multi-AZ deployment.
- Create a snapshot of the MySQL database server and use AWS DataSync to migrate the data to Amazon S3. Launch a new Amazon RDS MySQL Multi-AZ deployment from the snapshot.
- **✅ Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment.**

**A:** **Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment.**

**Explanation:**

The AWS DMS service can be used to directly migrate the MySQL database to an Amazon RDS Multi-AZ deployment. The entire process can be online and is managed for you. There is no need to perform schema translation from MySQL to RDS (RDS is just the service wrapper, the DB engine is MySQL).

- **CORRECT:** "Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment" is the correct answer.
- **INCORRECT:** "Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon EC2 MySQL Multi-AZ deployment" is incorrect as there is no such thing as "multi-AZ" on Amazon EC2.
- **INCORRECT:** "Create a snapshot of the MySQL database server and use AWS DataSync to migrate the data to Amazon S3. Launch a new Amazon RDS MySQL Multi-AZ deployment from the snapshot" is incorrect. AWS DataSync is not the right tool for migrating database snapshots to RDS.
- **INCORRECT:** "Use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon RDS MySQL. Use the Schema Conversion Tool (SCT) to enable conversion from MySQL to Amazon RDS" is incorrect. The SCT is not required when migrating between the same database engines.

**References:**
- https://aws.amazon.com/rds/features/multi-az/
- https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.html
- https://digitalcloud.training/amazon-rds/
- https://digitalcloud.training/aws-migration-services/
