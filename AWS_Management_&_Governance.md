Question 1Skipped
Domain
AWS Management & Governance
Question 11Skipped
A company needs to connect its on-premises data center network to a new virtual private cloud (VPC). There is a symmetrical internet connection of 100 Mbps in the data center network. The data transfer rate for an on-premises application is multiple gigabytes per day. Processing will be done using an Amazon Kinesis Data Firehose stream.
What should a solutions architect recommend for maximum performance?
Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection.
Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection.
Correct answer
Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint.
Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary.
Overall explanation
Explanation:
Using AWS PrivateLink to create an interface endpoint will allow your traffic to traverse the AWS Global Backbone to allow maximum performance and security. Also by using an AWS Direct Connect cable you can ensure you have a dedicated cable to provide maximum performance and low latency to and from AWS.
CORRECT: "Kinesis Data Firehose can be connected to the VPC using AWS PrivateLink. Install a 1 Gbps AWS Direct Connect connection between the on-premises network and AWS. To send data from on-premises to Kinesis Data Firehose, use the PrivateLink endpoint” is the correct answer (as explained above.)
INCORRECT: "Establish a peering connection between the on-premises network and the VPC. Configure routing for the on-premises network to use the VPC peering connection” is incorrect also because VPC peering connections can only exist between two VPCs within the AWS Cloud.
INCORRECT: "Get an AWS Snowball Edge Storage Optimized device. Data must be copied to the device after several days and shipped to AWS for expedited transfer to Kinesis Data Firehose. Repeat as necessary” is incorrect. AWS Snowball Edge is designed to be more of a one-time migration service which you physically receive from AWS, and then ship it into an AWS Region of your choice.
INCORRECT: "Establish an AWS Site-to-Site VPN connection between the on-premises network and the VPC. Set up BGP routing between the customer gateway and the virtual private gateway. Send data to Kinesis Data Firehose using a VPN connection” is incorrect. This is a functional solution; however a physical connection would provide a much more reliable and performant solution.
References:
https://aws.amazon.com/privatelink/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Management & Governance
Question 28Skipped
A company runs an application in a factory that has a small rack of physical compute resources. The application stores data on a network attached storage (NAS) device using the NFS protocol. The company requires a daily offsite backup of the application data.
Which solution can a Solutions Architect recommend to meet this requirement?
Use an AWS Storage Gateway volume gateway with cached volumes on premises to replicate the data to Amazon S3.
Create an IPSec VPN to AWS and configure the application to mount the Amazon EFS file system. Run a copy job to backup the data to EFS.
Correct answer
Use an AWS Storage Gateway file gateway hardware appliance on premises to replicate the data to Amazon S3.
Use an AWS Storage Gateway volume gateway with stored volumes on premises to replicate the data to Amazon S3.
Overall explanation
The AWS Storage Gateway Hardware Appliance is a physical, standalone, validated server configuration for on-premises deployments. It comes pre-loaded with Storage Gateway software, and provides all the required CPU, memory, network, and SSD cache resources for creating and configuring File Gateway, Volume Gateway, or Tape Gateway.
A file gateway is the correct type of appliance to use for this use case as it is suitable for mounting via the NFS and SMB protocols.
CORRECT: "Use an AWS Storage Gateway file gateway hardware appliance on premises to replicate the data to Amazon S3" is the correct answer.
INCORRECT: "Use an AWS Storage Gateway volume gateway with stored volumes on premises to replicate the data to Amazon S3" is incorrect. Volume gateways are used for block-based storage and this solution requires NFS (file-based storage).
INCORRECT: "Use an AWS Storage Gateway volume gateway with cached volumes on premises to replicate the data to Amazon S3" is incorrect. Volume gateways are used for block-based storage and this solution requires NFS (file-based storage).
INCORRECT: "Create an IPSec VPN to AWS and configure the application to mount the Amazon EFS file system. Run a copy job to backup the data to EFS" is incorrect. It would be better to use a Storage Gateway which will automatically take care of synchronizing a copy of the data to AWS.
References:
https://aws.amazon.com/storagegateway/hardware-appliance/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-storage-gateway/
Domain
AWS Management & Governance
Question 49Skipped
A company is deploying a fleet of Amazon EC2 instances running Linux across multiple Availability Zones within an AWS Region. The application requires a data storage solution that can be accessed by all of the EC2 instances simultaneously. The solution must be highly scalable and easy to implement. The storage must be mounted using the NFS protocol.
Which solution meets these requirements?
Create an Amazon EBS volume and use EBS Multi-Attach to mount the volume to all EC2 instances across each Availability Zone.
Create an Amazon RDS database and store the data in a BLOB format. Point the application instances to the RDS endpoint.
Correct answer
Create an Amazon EFS file system with mount targets in each Availability Zone. Configure the application instances to mount the file system.
Create an Amazon S3 bucket and create an S3 gateway endpoint to allow access to the file system using the NFS protocol.
Overall explanation
Amazon EFS provides scalable file storage for use with Amazon EC2. You can use an EFS file system as a common data source for workloads and applications running on multiple instances. The EC2 instances can run in multiple AZs within a Region and the NFS protocol is used to mount the file system.
With EFS you can create mount targets in each AZ for lower latency. The application instances in each AZ will mount the file system using the local mount target.
CORRECT: "Create an Amazon EFS file system with mount targets in each Availability Zone. Configure the application instances to mount the file system" is the correct answer.
INCORRECT: "Create an Amazon S3 bucket and create an S3 gateway endpoint to allow access to the file system using the NFS protocol" is incorrect. You cannot use NFS with S3 or with gateway endpoints.
INCORRECT: "Create an Amazon EBS volume and use EBS Multi-Attach to mount the volume to all EC2 instances across each Availability Zone" is incorrect. You cannot use Amazon EBS Multi-Attach across multiple AZs.
INCORRECT: "Create an Amazon RDS database and store the data in a BLOB format. Point the application instances to the RDS endpoint" is incorrect. This is not a suitable storage solution for a file system that is mounted over NFS.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEFS.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/
Domain
AWS Management & Governance
Question 59Skipped
A company runs an application on an Amazon EC2 instance the requires 250 GB of storage space. The application is not used often and has small spikes in usage on weekday mornings and afternoons. The disk I/O can vary with peaks hitting a maximum of 3,000 IOPS. A Solutions Architect must recommend the most cost-effective storage solution that delivers the performance required.
Which configuration should the Solutions Architect recommend?
Which solution should the solutions architect recommend?
Amazon EBS Throughput Optimized HDD (st1)
Amazon EBS Provisioned IOPS SSD (i01)
Correct answer
Amazon EBS General Purpose SSD (gp2)
Amazon EBS Cold HDD (sc1)
Overall explanation
General Purpose SSD (gp2) volumes offer cost-effective storage that is ideal for a broad range of workloads. These volumes deliver single-digit millisecond latencies and the ability to burst to 3,000 IOPS for extended periods of time.
Between a minimum of 100 IOPS (at 33.33 GiB and below) and a maximum of 16,000 IOPS (at 5,334 GiB and above), baseline performance scales linearly at 3 IOPS per GiB of volume size. AWS designs gp2 volumes to deliver their provisioned performance 99% of the time. A gp2 volume can range in size from 1 GiB to 16 TiB.
In this configuration the volume will provide a baseline performance of 750 IOPS but will always be able to burst to the required 3,000 IOPS during periods of increased traffic.
CORRECT: "Amazon EBS General Purpose SSD (gp2)" is the correct answer.
INCORRECT: "Amazon EBS Provisioned IOPS SSD (i01)" is incorrect. The i01 volume type will be more expensive and is not necessary for the performance levels required.
INCORRECT: "Amazon EBS Cold HDD (sc1)" is incorrect. The sc1 volume type is not going to deliver the performance requirements as it cannot burst to 3,000 IOPS.
INCORRECT: "Amazon EBS Throughput Optimized HDD (st1)" is incorrect. The st1 volume type is not going to deliver the performance requirements as it cannot burst to 3,000 IOPS.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
Domain
AWS Management & Governance
Question 30Skipped
A logistics company needs to replicate ongoing data changes from an on-premises Microsoft SQL Server database to Amazon RDS for SQL Server. The volume of data to replicate varies throughout the day due to periodic spikes in activity. The company plans to use AWS Database Migration Service (AWS DMS) for this task. The solution must dynamically allocate capacity based on workload demand while keeping operational overhead low.
Which solution will meet these requirements?
Create an AWS DMS replication instance with provisioned capacity in a Multi-AZ deployment to improve availability and fault tolerance.
Use Amazon EC2 Spot Instances to host the AWS DMS replication instance and manually scale up or down based on replication needs.
Deploy AWS DMS in an Amazon Elastic Kubernetes Service (Amazon EKS) cluster and use an autoscaler to adjust compute capacity during data spikes.
Correct answer
Configure AWS DMS Serverless to create a replication task that scales its capacity automatically based on workload demand.
Overall explanation
Configure AWS DMS Serverless to create a replication task that scales its capacity automatically based on workload demand: This is correct because AWS DMS Serverless dynamically adjusts replication capacity in response to data volume changes, providing cost efficiency and reducing manual management.
Deploy AWS DMS in an Amazon Elastic Kubernetes Service (Amazon EKS) cluster and use an autoscaler to adjust compute capacity during data spikes: This is incorrect because AWS DMS does not support deployment on Amazon EKS. Additionally, this solution introduces unnecessary complexity.
Use Amazon EC2 Spot Instances to host the AWS DMS replication instance and manually scale up or down based on replication needs: This is incorrect because manually scaling replication tasks increases operational overhead and Spot Instances could be interrupted, affecting replication stability.
Create an AWS DMS replication instance with provisioned capacity in a Multi-AZ deployment to improve availability and fault tolerance: This is incorrect because while Multi-AZ deployment enhances availability, it does not dynamically adjust capacity to match workload demand.
References:
https://docs.aws.amazon.com/dms/latest/userguide/what-is-dms.html
https://aws.amazon.com/dms/serverless/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/
Domain
AWS Management & Governance
Question 41Skipped
An application consists of a web tier in a public subnet and a MySQL cluster hosted on Amazon EC2 instances in a private subnet. The MySQL instances must retrieve product data from a third-party provider over the internet. A Solutions Architect must determine a strategy to enable this access with maximum security and minimum operational overhead.
What should the Solutions Architect do to meet these requirements?
Create a virtual private gateway and attach it to the VPC. Modify the private subnet route table to direct internet traffic to the virtual private gateway.
Create an internet gateway and attach it to the VPC. Modify the private subnet route table to direct internet traffic to the internet gateway.
Correct answer
Deploy a NAT gateway in the public subnet. Modify the route table in the private subnet to direct all internet traffic to the NAT gateway.
Deploy a NAT instance in the private subnet. Direct all internet traffic to the NAT instance.
Overall explanation
The MySQL clusters instances need to access a service on the internet. The most secure method of enabling this access with low operational overhead is to create a NAT gateway. When deploying a NAT gateway, the gateway itself should be deployed in a public subnet whilst the route table in the private subnet must be updated to point traffic to the NAT gateway ID.
The configuration can be seen in the diagram below:


CORRECT: "Deploy a NAT gateway in the public subnet. Modify the route table in the private subnet to direct all internet traffic to the NAT gateway" is the correct answer.
INCORRECT: "Deploy a NAT instance in the private subnet. Direct all internet traffic to the NAT instance" is incorrect. NAT instances require more operational overhead and need to be deployed in a public subnet.
INCORRECT: "Create an internet gateway and attach it to the VPC. Modify the private subnet route table to direct internet traffic to the internet gateway" is incorrect. You cannot point the instances in the private subnet to an internet gateway as they do not have public IP addresses which is required to use an internet gateway.
INCORRECT: "Create a virtual private gateway and attach it to the VPC. Modify the private subnet route table to direct internet traffic to the virtual private gateway" is incorrect. A virtual private gateway (VGW) is used with a VPN connection, not for connecting instances in private subnets to the internet.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Management & Governance
Question 46Skipped
A Solutions Architect has been tasked with migrating 30 TB of data from an on-premises data center within 20 days. The company has an internet connection that is limited to 25 Mbps and the data transfer cannot use more than 50% of the connection speed.
What should a Solutions Architect do to meet these requirements?
Use a site-to-site VPN.
Correct answer
Use AWS Snowball.
Use AWS DataSync.
Use AWS Storage Gateway.
Overall explanation
This is a simple case of working out roughly how long it will take to migrate the data using the 12.5 Mbps of bandwidth that is available for transfer and seeing which options are feasible. Transferring 30 TB of data across a 25 Mbps connection could take upwards of 200 days.
Therefore, we know that using the Internet connection will not meet the requirements and we can rule out any solution that will use the internet (all options except for Snowball). AWS Snowball is a physical device that is shipped to your office or data center. You can then load data onto it and ship it back to AWS where the data is uploaded to Amazon S3.
Snowball is the only solution that will achieve the data migration requirements within the 20-day period.
CORRECT: "Use AWS Snowball" is the correct answer.
INCORRECT: "Use AWS DataSync" is incorrect. This uses the internet which will not meet the 20-day deadline.
INCORRECT: "Use AWS Storage Gateway" is incorrect. This uses the internet which will not meet the 20-day deadline.
INCORRECT: "Use a site-to-site VPN" is incorrect. This uses the internet which will not meet the 20-day deadline.
References:
https://aws.amazon.com/snowball/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Management & Governance
Question 52Skipped
A scientific research organization runs an on-premises simulation application that processes large datasets. The organization has migrated all simulation data to Amazon S3 to reduce costs. The simulation application requires low-latency storage access for seamless performance during processing tasks.
The organization needs to design a storage solution that minimizes costs while maintaining the performance requirements of the application.
Which storage solution will meet these requirements in the MOST cost-effective way?
Copy the data from Amazon S3 to Amazon FSx for Lustre. Use an Amazon FSx File Gateway to provide low-latency access for the on-premises application.
Deploy a high-speed internet connection and configure the on-premises application to access the data directly from Amazon S3 using the S3 API for storage operations.
Use AWS DataSync to copy frequently accessed data from Amazon S3 to an on-premises storage system. Configure the application to use the local storage for low-latency access.
Correct answer
Use Amazon S3 File Gateway to provide low-latency storage for the on-premises application. The File Gateway will cache frequently accessed data locally.
Overall explanation
Use Amazon S3 File Gateway to provide low-latency storage for the on-premises application. The File Gateway will cache frequently accessed data locally: This is correct because S3 File Gateway provides a seamless and cost-effective way to access data stored in Amazon S3. It locally caches frequently accessed data, reducing latency while still leveraging the cost benefits of S3 storage.
Use AWS DataSync to copy frequently accessed data from Amazon S3 to an on-premises storage system. Configure the application to use the local storage for low-latency access: This is incorrect because DataSync is designed for batch data transfer and is not suitable for providing continuous, low-latency access to S3 data. It introduces additional complexity and costs for managing on-premises storage systems.
Copy the data from Amazon S3 to Amazon FSx for Lustre. Use an Amazon FSx File Gateway to provide low-latency access for the on-premises application: This is incorrect because FSx for Lustre is optimized for high-performance workloads but is more expensive and introduces unnecessary complexity compared to S3 File Gateway. Additionally, copying all data to FSx increases storage costs.
Deploy a high-speed internet connection and configure the on-premises application to access the data directly from Amazon S3 using the S3 API for storage operations: This is incorrect because accessing data directly from S3 over the internet does not meet the low-latency requirements for the application. While cost-effective, it will degrade performance for latency-sensitive workloads.
References:
https://docs.aws.amazon.com/storagegateway/latest/userguide/WhatIsStorageGateway.html
https://docs.aws.amazon.com/datasync/latest/userguide/what-is-datasync.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-storage-gateway/
Domain
AWS Management & Governance
Question 60Skipped
An educational content provider has accumulated several terabytes of learning resources in an Amazon S3 bucket located in a specific AWS Region. A partner organization, based in a different AWS Region, has been granted access to the S3 bucket to retrieve the resources for integration into its own platform. The content provider wants to minimize its data transfer costs when the partner organization accesses the S3 bucket.
Which solution will meet these requirements?
Configure the bucket to use S3 Standard-IA storage to reduce access costs for the partner organization.
Set up S3 Cross-Region Replication (CRR) to copy the learning resources to the partner organization’s S3 bucket.
Correct answer
Enable the Requester Pays feature on the content provider’s S3 bucket.
Use S3 Transfer Acceleration to allow the partner organization to retrieve data from the bucket.
Overall explanation
Enable the Requester Pays feature on the content provider’s S3 bucket: This is correct because the Requester Pays feature shifts the data transfer costs from the content provider to the partner organization, thereby minimizing the content provider’s expenses.
Use S3 Transfer Acceleration to allow the partner organization to retrieve data from the bucket: This solution optimizes data transfer speeds but does not specifically address minimizing the content provider's data transfer costs.
Set up S3 Cross-Region Replication (CRR) to copy the learning resources to the partner organization’s S3 bucket: While this enables data availability in the partner organization’s Region, it introduces additional costs for cross-Region replication, which the content provider would incur.
Configure the bucket to use S3 Standard-IA storage to reduce access costs for the partner organization: Changing the storage class to Standard-IA focuses on storage cost optimization and does not directly address minimizing data transfer costs for the content provider.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/RequesterPaysBuckets.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Management & Governance
Question 10Skipped
A Solutions Architect is designing an application that will run on an Amazon EC2 instance. The application must asynchronously invoke an AWS Lambda function to analyze thousands of .CSV files. The services should be decoupled.
Which service can be used to decouple the compute services?
Amazon OpsWorks
Correct answer
Amazon SNS
Amazon Kinesis
Amazon SWF
Overall explanation
You can use a Lambda function to process Amazon Simple Notification Service notifications. Amazon SNS supports Lambda functions as a target for messages sent to a topic. This solution decouples the Amazon EC2 application from Lambda and ensures the Lambda function is invoked.
CORRECT: "Amazon SNS" is the correct answer.
INCORRECT: "Amazon SWF" is incorrect. The Simple Workflow Service (SWF) is used for process automation. It is not well suited to this requirement.
INCORRECT: "Amazon Kinesis" is incorrect as this service is used for ingesting and processing real time streaming data, it is not a suitable service to be used solely for invoking a Lambda function.
INCORRECT: "Amazon OpsWorks" is incorrect as this service is used for configuration management of systems using Chef or Puppet.
References:
https://docs.aws.amazon.com/lambda/latest/dg/with-sns.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
https://digitalcloud.training/aws-lambda/
Domain
AWS Management & Governance
Question 33Skipped
A computer scientist working for a university is looking to build a machine learning application which will use telemetry data to predict weather for a given area at a given time. This application would benefit from using managed services and will need to find a solution which uses third party data within the application.

Which of the following combinations of services will deliver the best solution?
Use Amazon SageMaker to build the machine learning part of the application and use AWS DataSync to gain access to the third-party telemetry data.
Correct answer
Use Amazon SageMaker to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data.
Use a TensorFlow AMI from the AWS Marketplace to build the machine learning part of the application and use AWS DataSync to gain access to the third-party telemetry data.
Use a TensorFlow AMI from the AWS Marketplace to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data.
Overall explanation
Amazon SageMaker allows you to build, train, and deploy machine learning models for any use case with fully managed infrastructure, tools, and workflows. AWS Data Exchange allows you to gain access to third party data sets across Automotive, Financial Services, Gaming, Healthcare & Life Sciences, Manufacturing, Marketing, Media & Entertainment, Retail, and many more industries.
CORRECT: "Use Amazon SageMaker to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data” is the correct answer (as explained above.)
INCORRECT: "Use Amazon SageMaker to build the machine learning part of the application and use AWS DataSync to gain access to the third-party telemetry data” is incorrect. AWS DataSync is a secure, online service that automates and accelerates moving data between on-premises and AWS storage services. It does not give access to third party data.
INCORRECT: "Use a TensorFlow AMI from the AWS Marketplace to build the machine learning part of the application and use AWS DataSync to gain access to the third-party telemetry data” is incorrect. Building an EC2 instance from a TensorFlow AMI would not involve using managed services and AWS DataSync is a secure, online service that automates and accelerates moving data between on-premises and AWS storage services. It does not give access to third party data.
INCORRECT: "Use a TensorFlow AMI from the AWS Marketplace to build the machine learning part of the application and use AWS Data Exchange to gain access to the third-party telemetry data” is incorrect. Building an EC2 instance from a TensorFlow AMI would not involve using managed services.
References:
https://aws.amazon.com/data-exchange/
Domain
AWS Management & Governance
Question 4Skipped
A law firm has recently moved an on-premises multi-tier web application to AWS. Currently, the web application is based on a containerized solution and is running inside Linux based EC2 instances which connect to a PostgreSQL database hosted on separate but dedicated EC2 instances. The company wishes to optimize operational efficiency and performance.
Which combination of actions should the solutions architect take? (Select TWO.)
Correct selection
Migrate the web application to be hosted on AWS Fargate with Amazon Elastic Container Service (Amazon ECS).
Set up Amazon ElastiCache between the web application and the PostgreSQL database.
Set up an Amazon CloudFront distribution for the web application content.
Correct selection
Migrate the PostgreSQL database to Amazon Aurora.
Migrate the web application to the same Amazon EC2 instances as the database.
Overall explanation
Amazon Aurora (Aurora) is a fully managed relational database engine that's compatible with MySQL and PostgreSQL. You already know how MySQL and PostgreSQL combine the speed and reliability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases. The code, tools, and applications you use today with your existing MySQL and PostgreSQL databases can be used with Aurora. With some workloads, Aurora can deliver up to five times the throughput of MySQL and up to three times the throughput of PostgreSQL without requiring changes to most of your existing applications.
Amazon ECS is a fully managed container orchestration service that makes it easy for you to deploy, manage, and scale containerized applications. This is a better hosting solution for a containerized solution rather than managing the underlying container platform yourself. In the case of Fargate, the solution is serverless, so it massively reduces operational overhead.
CORRECT: "Migrate the PostgreSQL database to Amazon Aurora and Migrate the web application to be hosted on AWS Fargate with Amazon Elastic Container Service (Amazon ECS)" are the correct answers (as explained above)
INCORRECT: "Migrate the web application to the same Amazon EC2 instances as the database" is incorrect. This might reduce cost but doesn’t offer any other advantages.
INCORRECT: "Set up an Amazon CloudFront distribution for the web application content" is incorrect. CloudFront helps with caching content globally for better performance but does not help reduce the operational overhead or performance of this solution.
INCORRECT: "Set up Amazon ElastiCache between the web application and the PostgreSQL database" is incorrect. Caching will only help when you have hot data segments and does not reduce the operational overhead of this solution.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/AuroraMySQL.Updates.Versions.html#AuroraMySQL.Updates.UpgradePaths
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Management & Governance
Question 8Skipped
A company stores its application logs in an Amazon CloudWatch Logs log group. A new policy requires the company to store all application logs in Amazon OpenSearch Service (Amazon Elasticsearch Service) in near-real time.
Which solution will meet this requirement with the LEAST operational overhead?
Create an AWS Lambda function. Use the log group to invoke the function to write the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service).
Create an Amazon Kinesis Data Firehose delivery stream. Configure the log group as the delivery stream's source. Configure Amazon OpenSearch Service (Amazon Elasticsearch Service) as the delivery stream's destination.
Install and configure Amazon Kinesis Agent on each application server to deliver the logs to Amazon Kinesis Data Streams. Configure Kinesis Data Streams to deliver the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service).
Correct answer
Configure a CloudWatch Logs subscription to stream the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service).
Overall explanation
You can configure a CloudWatch Logs log group to stream data it receives to your Amazon OpenSearch Service cluster in near real-time through a CloudWatch Logs subscription. This is the solution that requires the least operational overhead. Subscription filters can also be created for Kinesis, Kinesis Data Firehose, and AWS Lambda.
CORRECT: " Configure a CloudWatch Logs subscription to stream the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service) " is the correct answer (as explained above.)
INCORRECT: "Create an Amazon Kinesis Data Firehose delivery stream. Configure the log group as the delivery stream's source. Configure Amazon OpenSearch Service (Amazon Elasticsearch Service) as the delivery stream's destination" is incorrect.
This is a possible solution but requires more operational overhead as it includes an additional service which must also be configured and managed.
INCORRECT: "Create an AWS Lambda function. Use the log group to invoke the function to write the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service)" is incorrect. This would require more operational overhead as you must write and manage the code for the function yourself.
INCORRECT: "Install and configure Amazon Kinesis Agent on each application server to deliver the logs to Amazon Kinesis Data Streams. Configure Kinesis Data Streams to deliver the logs to Amazon OpenSearch Service (Amazon Elasticsearch Service)" is incorrect. Since the requirement is to dump the logs into OpenSearch and no further computation is needed, Firehose is a better candidate here.
References:
https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_OpenSearch_Stream.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudwatch/
https://digitalcloud.training/amazon-opensearch/
Domain
AWS Management & Governance
Question 9Skipped
An application that is being installed on an Amazon EC2 instance requires a persistent block storage volume. The data must be encrypted at rest and regular volume-level backups must be automated.
Which solution options should be used?
Correct answer
Use an encrypted Amazon EBS volume and use Data Lifecycle Manager to automate snapshots
Use server-side encryption on an Amazon S3 bucket and use Cross-Region-Replication to backup on a schedule
Use an encrypted Amazon EC2 instance store and copy the data to another EC2 instance using a cron job and a batch script
Use an encrypted Amazon EFS filesystem and use an Amazon CloudWatch Events rule to start a backup copy of data using AWS Lambda
Overall explanation
For block storage the Solutions Architect should use either Amazon EBS or EC2 instance store. However, the instance store is non-persistent so EBS must be used. With EBS you can encrypt your volume and automate volume-level backups using snapshots that are run by Data Lifecycle Manager.
CORRECT: "Use an encrypted Amazon EBS volume and use Data Lifecycle Manager to automate snapshots" is the correct answer.
INCORRECT: "Use an encrypted Amazon EFS filesystem and use an Amazon CloudWatch Events rule to start a backup copy of data using AWS Lambda" is incorrect. EFS is not block storage, it is a file-level storage service.
INCORRECT: "Use server-side encryption on an Amazon S3 bucket and use Cross-Region-Replication to backup on a schedule" is incorrect. Amazon S3 is an object-based storage system not a block-based storage system.
INCORRECT: "Use an encrypted Amazon EC2 instance store and copy the data to another EC2 instance using a cron job and a batch script " is incorrect as the EC2 instance store is a non-persistent volume.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
Domain
AWS Management & Governance
Question 11Skipped
A financial services company has a large, multi-Region footprint on AWS. A recent security audit highlighted some issues that must be addressed. The company must track all configuration changes affecting AWS resources and have detailed records of who has accessed the AWS environment. The data should include information such as which user has logged in and which API calls they made
What actions should a Solutions Architect take to meet these requirements?
Correct answer
Use AWS Config to track configuration changes and AWS CloudTrail to record API calls and track access patterns in the AWS Cloud.
Use AWS Config to track configuration changes and Amazon EventBridge to record API calls and track access patterns in the AWS Cloud.
Use Amazon CloudWatch to track configuration changes and AWS Config to record API calls and track access patterns in the AWS Cloud.
Use Amazon Macie to track configuration changes and Amazon CloudTrail to record API calls and track access patterns in the AWS Cloud.
Overall explanation
AWS Config is a service used to track and remediation any unauthorized configuration changes made with your AWS Account. AWS Config could be used in this example with AWS AWS CloudTrail which keeps detailed logs of all API calls made within the account such as who logged in, which AWS Identity and Access Management (IAM) role is being used and also how they interact with the AWS Cloud.
CORRECT: "Use AWS Config to track configuration changes and AWS CloudTrail to record API calls and track access patterns in the AWS Cloud" is the correct answer (as explained above.)
INCORRECT: "Use Amazon CloudWatch to track configuration changes and AWS Config to record API calls and track access patterns in the AWS Cloud" is incorrect. Amazon CloudWatch does not make track configuration changes, it tracks performance metrics and AWS Config does not track API calls, it tracks configuration changes.
INCORRECT: "Use AWS Config to track configuration changes and Amazon EventBridge to record API calls and track access patterns in the AWS Cloud" is incorrect. Although AWS Config would work in this scenario, Amazon EventBridge is a serverless event bus used to build event-driven- architectures so it cannot be used for tracking API calls.
INCORRECT: "Use Amazon Macie to track configuration changes and Amazon CloudTrail to record API calls and track access patterns in the AWS Cloud" is incorrect. Amazon Macie is used with Amazon S3 to detect sensitive PII data, which has nothing to do with tracking configuration changes.
References:
https://aws.amazon.com/config
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-config/
Domain
AWS Management & Governance
Question 12Skipped
A company wants to improve its ability to clone large amounts of production data into a test environment in the same AWS Region. The data is stored in Amazon EC2 instances on Amazon Elastic Block Store (Amazon EBS) volumes. Modifications to the cloned data must not affect the production environment. The software that accesses this data requires consistently high I/O performance.
A solutions architect needs to minimize the time that is required to clone the production data into the test environment.
Which solution will meet these requirements?
Take EBS snapshots of the production EBS volumes. Restore the snapshots onto EC2 instance store volumes in the test environment.
Take EBS snapshots of the production EBS volumes. Create and initialize new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment before restoring the volumes from the production EBS snapshots.
Correct answer
Take EBS snapshots of the production EBS volumes. Turn on the EBS fast snapshot restore feature on the EBS snapshots. Restore the snapshots into new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment.
Configure the production EBS volumes to use the EBS Multi-Attach feature. Take EBS snapshots of the production EBS volumes. Attach the production EBS volumes to the EC2 instances in the test environment.
Overall explanation
Amazon EBS fast snapshot restore (FSR) enables you to create a volume from a snapshot that is fully initialized at creation. This eliminates the latency of I/O operations on a block when it is accessed for the first time. Volumes that are created using fast snapshot restore instantly deliver all their provisioned performance.
CORRECT: "Take EBS snapshots of the production EBS volumes. Turn on the EBS fast snapshot restore feature on the EBS snapshots. Restore the snapshots into new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment" is the correct answer (as explained above.)
INCORRECT: "Take EBS snapshots of the production EBS volumes. Restore the snapshots onto EC2 instance store volumes in the test environment" is incorrect. You cannot restore EBS snapshots to instance store volumes. Instance store volumes are ephemeral storage volumes and are not used for data that requires persistence.
INCORRECT: “Take EBS snapshots of the production EBS volumes. Create and initialize new EBS volumes. Attach the new EBS volumes to EC2 instances in the test environment before restoring the volumes from the production EBS snapshots" is incorrect.
This solution may take longer and may not have the consistent performance that is offered with the correct answer.
INCORRECT: "Configure the production EBS volumes to use the EBS Multi-Attach feature. Take EBS snapshots of the production EBS volumes. Attach the production EBS volumes to the EC2 instances in the test environment" is incorrect.
Amazon EBS Multi-Attach enables you to attach a single Provisioned IOPS SSD ( io1 or io2 ) volume to multiple instances that are in the same Availability Zone. You can attach multiple Multi-Attach enabled volumes to an instance or set of instances. This does not help with the requirements of this solution.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-fast-snapshot-restore.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
Domain
AWS Management & Governance
Question 17Skipped
The database layer of an on-premises web application is being migrated to AWS. The database uses a multi-threaded, in-memory caching layer to improve performance for repeated queries. Which service would be the most suitable replacement for the database cache?
Amazon DynamoDB DAX
Amazon ElastiCache Redis
Amazon RDS MySQL
Correct answer
Amazon ElastiCache Memcached
Overall explanation
Amazon ElastiCache with the Memcached engine is an in-memory database that can be used as a database caching layer. The memached engine supports multiple cores and threads and large nodes.


CORRECT: "Amazon ElastiCache Memcached" is the correct answer.
INCORRECT: "Amazon ElastiCache Redis" is incorrect. The Redis engine does not support multiple CPU cores or threads.
INCORRECT: "Amazon DynamoDB DAX" is incorrect. Amazon DynamoDB Accelerator (DAX) is a database cache that should be used with DynamoDB only.
INCORRECT: "Amazon RDS MySQL" is incorrect as this is not an example of an in-memory database that can be used as a database caching layer.
References:
https://aws.amazon.com/elasticache/redis-vs-memcached/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-elasticache/
Domain
AWS Management & Governance
Question 23Skipped
A company is deploying a new web application that will run on Amazon EC2 instances in an Auto Scaling group across multiple Availability Zones. The application requires a shared storage solution that offers strong consistency as the content will be regularly updated.
Which solution requires the LEAST amount of effort?
Correct answer
Create an Amazon Elastic File System (Amazon EFS) file system and mount it on the individual Amazon EC2 instances
Create a shared Amazon Block Store (Amazon EBS) volume and mount it on the individual Amazon EC2 instances
Create a volume gateway using AWS Storage Gateway to host the data and mount it to the Auto Scaling group
Create an Amazon S3 bucket to store the web content and use Amazon CloudFront to deliver the content
Overall explanation
Amazon EFS is a fully-managed service that makes it easy to set up, scale, and cost-optimize file storage in the Amazon Cloud. EFS file systems are accessible to Amazon EC2 instances via a file system interface (using standard operating system file I/O APIs) and support full file system access semantics (such as strong consistency and file locking).
EFS is a good solution for when you need to attach a shared filesystem to multiple EC2 instances across multiple Availability Zones.
CORRECT: "Create an Amazon Elastic File System (Amazon EFS) file system and mount it on the individual Amazon EC2 instances" is the correct answer.
INCORRECT: "Create an Amazon S3 bucket to store the web content and use Amazon CloudFront to deliver the content" is incorrect as this may require more effort in terms of reprogramming the application to use the S3 API.
INCORRECT: "Create a shared Amazon Block Store (Amazon EBS) volume and mount it on the individual Amazon EC2 instances" is incorrect. Please note that you can multi-attach an EBS volume to multiple EC2 instances but the instances must be in the same AZ.
INCORRECT: "Create a volume gateway using AWS Storage Gateway to host the data and mount it to the Auto Scaling group" is incorrect as a storage gateway is used on-premises.
References:
https://aws.amazon.com/efs/faq/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/
Domain
AWS Management & Governance
Question 31Skipped
A global financial services company is currently operating a three-tier web application to handle their main customer facing website. This application uses several Amazon EC2 instances behind an Application Load Balancer and connects directly to a DynamoDB table.
Due to recent customer complaints of slow loading times, their Solutions Architect has been asked to implement changes to solve this problem, without rearchitecting the core application components.

Which combination of actions should the solutions architect take to accomplish this? (Select TWO.)
Migrate the web application to be hosted on a containerized solution using AWS Fargate.
Migrate the entire application stack to AWS Elastic Beanstalk with both web server and worker environments.
Correct selection
Set up an Amazon DynamoDB Accelerator (DAX) cluster in front of the DynamoDB table.
Correct selection
Create a CloudFront distribution and place it in front of the Application Load Balancer.
Migrate the DynamoDB database to Amazon Aurora with a multi-AZ deployment model.
Overall explanation
A CloudFront distribution would cache content in one of the many global edge locations, ensuring that any customer access to the content will be accessing it at a much lower latency compared to using the Application Load Balancer on its own.
Secondly, DynamoDB has a built-in caching solution known as DynamoDB Accelerator (DAX). If your application is serving traffic from a DynamoDB database and is struggling to scale, you can use the DynamoDB cache to improve application.
CORRECT: "Create a CloudFront distribution and place it in front of the Application Load Balancer" is a correct answer (as explained above.)
CORRECT: "Set up an Amazon DynamoDB Accelerator (DAX) cluster in front of the DynamoDB table" is also a correct answer (as explained above.)
INCORRECT: "Migrate the entire application stack to AWS Elastic Beanstalk with both web server and worker environments" is incorrect.
Migrating the entire application to AWS Elastic Beanstalk would require rearchitecting and would not necessarily improve the latency of the application for end users.
INCORRECT: "Migrate the DynamoDB database to Amazon Aurora with a multi-AZ deployment model" is incorrect.
Refactoring the application to move from a No-SQL database (DynamoDB) to a SQL database (Amazon Aurora) would take a significant amount of application and code changes, due to the fundamental differences between SQL and NoSQL databases.
INCORRECT: "Migrate the web application to be hosted on a containerized solution using AWS Fargate" is incorrect.
The application does not currently use containers, and instead uses Amazon EC2 instances. Changing the application to using a containerized compute layer would also require architectural changes and would not be suitable for this use case.
References:
https://aws.amazon.com/cloudfront/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Management & Governance
Question 33Skipped
A health tech company runs a multi-tier medical records application in the AWS Cloud, which operates across three Availability Zones. The application architecture includes an Application Load Balancer, a cluster of Amazon EC2 instances that handle user session states, and a PostgreSQL database running on an EC2 instance.
The company anticipates a sharp surge in application traffic due to a new partnership. The company needs to scale to accommodate future application capacity demands and ensure high availability across all three Availability Zones.
Which solution will meet these requirements?
Migrate the PostgreSQL database to Amazon Aurora with PostgreSQL compatibility with a single AZ deployment. Use Amazon ElastiCache for Memcached to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones.
Correct answer
Migrate the PostgreSQL database to Amazon RDS for PostgreSQL with a Multi-AZ DB instance deployment. Use Amazon ElastiCache for Redis with a replication group to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones.
Keep the PostgreSQL database on EC2 instance. Use Amazon ElastiCache for Redis to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones.
Migrate the PostgreSQL database to Amazon DynamoDB. Use DynamoDB Accelerator (DAX) to cache reads. Store the session data in DynamoDB. Migrate the application server to an Auto Scaling group across three Availability Zones.
Overall explanation
This solution fulfills all the requirements. Amazon RDS with Multi-AZ instances provides high availability and failover support for DB instances. ElastiCache for Redis supports storing session state data and can provide sub-millisecond response times, enabling applications to achieve instant, high-speed reads and writes. Auto Scaling ensures that the application has the correct number of Amazon EC2 instances to handle the load for your application.
CORRECT: "Migrate the PostgreSQL database to Amazon RDS for PostgreSQL with a Multi-AZ DB instance deployment. Use Amazon ElastiCache for Redis with a replication group to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones" is the correct answer (as explained above.)
INCORRECT: "Migrate the PostgreSQL database to Amazon Aurora with PostgreSQL compatibility with a single AZ deployment. Use Amazon ElastiCache for Memcached to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones" is incorrect.
Aurora is a high-performance database service, but using a single AZ deployment doesn't provide the high availability across multiple AZs the company wants. Also, while ElastiCache for Memcached can be used for caching, it doesn't offer the durability and atomicity that Redis offers, which is particularly useful for session data.
INCORRECT: "Migrate the PostgreSQL database to Amazon DynamoDB. Use DynamoDB Accelerator (DAX) to cache reads. Store the session data in DynamoDB. Migrate the application server to an Auto Scaling group across three Availability Zones" is incorrect.
Although DynamoDB is a high-performance, scalable NoSQL database, it is not a drop-in replacement for a relational database like PostgreSQL. It has a different data model and supports a different set of query options. This change could require significant modifications to the application code and may not support the same transactional capabilities as PostgreSQL.
INCORRECT: "Keep the PostgreSQL database on EC2 instance. Use Amazon ElastiCache for Redis to manage session data and cache reads. Migrate the application server to an Auto Scaling group across three Availability Zones" is incorrect.
Although the EC2 instance can run the PostgreSQL database, it does not provide the same level of managed service benefits (like automatic patching, backups, and high availability with Multi-AZ deployments) as Amazon RDS. This option would likely result in higher operational overhead and doesn't fully utilize the benefits of managed AWS services.
References:
https://aws.amazon.com/rds/features/multi-az/
https://aws.amazon.com/elasticache/redis/
https://aws.amazon.com/ec2/autoscaling/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-elasticache/
Domain
AWS Management & Governance
Question 49Skipped
An e-commerce company has developed a new application which has been successfully deployed on AWS. For an upcoming sale, the company is expecting a huge rise in traffic and while testing for the event they have encountered performance issues in the application when many requests are sent to the application.
The current application stack is Amazon Aurora PostgreSQL database with an AWS Lambda compute layer fronted by API Gateway. A solutions architect must recommend improvements scalability whilst minimizing the configuration effort.
Which solution will meet these requirements?
Change the platform from Aurora to Amazon DynamoDB. Provision a DynamoDB Accelerator (DAX) cluster. Use the DAX client SDK to point the existing DynamoDB API calls at the DAX cluster.
Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using Amazon Simple Notification Service (Amazon SNS).
Refactor the Lambda function code to Apache Tomcat code that runs on Amazon EC2 instances. Connect the database by using native Java Database Connectivity (JDBC) drivers.
Correct answer
Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using an Amazon Simple Queue Service (Amazon SQS) queue.
Overall explanation
With Amazon SQS, you can offload tasks from one component of your application by sending them to a queue and processing them asynchronously. Lambda polls the queue and invokes your Lambda function synchronously with an event that contains the message from the SQS queue. This solution improves scalability as the message bus decouples the processing components of the application meaning it is less likely that the application will suffer outages or lost data.
CORRECT: "Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using an Amazon Simple Queue Service (Amazon SQS) queue" is the correct answer (as explained above.)
INCORRECT: "Refactor the Lambda function code to Apache Tomcat code that runs on Amazon EC2 instances. Connect the database by using native Java Database Connectivity (JDBC) drivers" is incorrect. You cannot run Lambda code on Amazon EC2 instances.
INCORRECT: "Change the platform from Aurora to Amazon DynamoDB. Provision a DynamoDB Accelerator (DAX) cluster. Use the DAX client SDK to point the existing DynamoDB API calls at the DAX cluster" is incorrect. Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for Amazon DynamoDB. The question doesn’t talk about hot or frequently accessed data only about an increase in volume so introducing DAX might not completely solve the issues.
INCORRECT: "Set up two Lambda functions. Configure one function to receive the information. Configure the other function to load the information into the database. Integrate the Lambda functions by using Amazon Simple Notification Service (Amazon SNS)" is incorrect. SNS is used for fan-out scenarios when a single event is to be broadcasted among consumers and hence is not a good fit here.
References:
https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Management & Governance
Question 2Skipped
An international software firm provides its clients with custom solutions and tools designed for efficient data collection and analysis on AWS. The firm intends to centrally manage and distribute a standard set of solutions and tools for its clients' self-service needs.
Which solution would best satisfy these requirements?
Create AWS Config rules for the clients.
Create AWS CloudFormation stacks for the clients.
Correct answer
Create AWS Service Catalog portfolios for the clients.
Create AWS Systems Manager documents for the clients.
Overall explanation
AWS Service Catalog enables organizations to create and manage catalogs of IT services that are approved for use on AWS. It allows centrally managed service portfolios, which clients can use on a self-service basis.
AWS Service Catalog provides a single location where organizations can centrally manage catalogs of IT services, which simplifies the organizational process and helps ensure compliance.
CORRECT: "Create AWS Service Catalog portfolios for the clients" is the correct answer (as explained above.)
INCORRECT: "Create AWS CloudFormation stacks for the clients" is incorrect.
While AWS CloudFormation is a powerful service for infrastructure as code (IaC), it doesn't provide a straightforward way for clients to discover and use shared tools or solutions for self-service needs. It lacks the management features and access control mechanisms necessary for this scenario.
INCORRECT: "Create AWS Systems Manager documents for the clients" is incorrect.
AWS Systems Manager documents define the actions that Systems Manager performs on your managed instances. Although Systems Manager allows the central management of resources and applications, it doesn't provide an effective means for clients to self-discover and use shared tools or solutions.
INCORRECT: "Create AWS Config rules for the clients" is incorrect.
AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. It isn't designed to centrally manage and distribute software tools or solutions.
References:
https://aws.amazon.com/servicecatalog/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-service-catalog/
Domain
AWS Management & Governance
Question 3Skipped
A company has refactored a legacy application to run as two microservices using Amazon ECS. The application processes data in two parts and the second part of the process takes longer than the first.
How can a solutions architect integrate the microservices and allow them to scale independently?
Implement code in microservice 1 to publish data to an Amazon SNS topic. Implement code in microservice 2 to subscribe to this topic
Correct answer
Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue
Implement code in microservice 1 to send data to Amazon Kinesis Data Firehose. Implement code in microservice 2 to read from Kinesis Data Firehose
Implement code in microservice 1 to send data to an Amazon S3 bucket. Use S3 event notifications to invoke microservice 2
Overall explanation
This is a good use case for Amazon SQS. The microservices must be decoupled so they can scale independently. An Amazon SQS queue will enable microservice 1 to add messages to the queue. Microservice 2 can then pick up the messages and process them. This ensures that if there’s a spike in traffic on the frontend, messages do not get lost due to the backend process not being ready to process them.
CORRECT: "Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue" is the correct answer.
INCORRECT: "Implement code in microservice 1 to send data to an Amazon S3 bucket. Use S3 event notifications to invoke microservice 2" is incorrect as a message queue would be preferable to an S3 bucket.
INCORRECT: "Implement code in microservice 1 to publish data to an Amazon SNS topic. Implement code in microservice 2 to subscribe to this topic" is incorrect as notifications to topics are pushed to subscribers. In this case we want the second microservice to pickup the messages when ready (pull them).
INCORRECT: "Implement code in microservice 1 to send data to Amazon Kinesis Data Firehose. Implement code in microservice 2 to read from Kinesis Data Firehose" is incorrect as this is not how Firehose works. Firehose sends data directly to destinations, it is not a message queue.
References:
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Management & Governance
Question 9Skipped
A Solutions Architect needs a solution for hosting a website that will be used by a development team. The website contents will consist of HTML, CSS, client-side JavaScript, and images.
Which solution is MOST cost-effective?
Use a Docker container to host the website on AWS Fargate.
Correct answer
Create an Amazon S3 bucket and host the website there.
Launch an Amazon EC2 instance and host the website there.
Create an Application Load Balancer with an AWS Lambda target.
Overall explanation
Amazon S3 can be used for hosting static websites and cannot be used for dynamic content. In this case the content is purely static with client-side code running. Therefore, an S3 static website will be the most cost-effective solution for hosting this website.
CORRECT: "Create an Amazon S3 bucket and host the website there" is the correct answer.
INCORRECT: "Launch an Amazon EC2 instance and host the website there" is incorrect. This will be more expensive as it uses an EC2 instances.
INCORRECT: "Use a Docker container to host the website on AWS Fargate" is incorrect. A static website on S3 is sufficient for this use case and will be more cost-effective than Fargate.
INCORRECT: "Create an Application Load Balancer with an AWS Lambda target" is incorrect. This is also a more expensive solution and unnecessary for this use case.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Management & Governance
Question 32Skipped
A company operates a production web application that uses an Amazon RDS MySQL database. The database has automated, non-encrypted daily backups. To increase the security of the data, it has been recommended that encryption should be enabled for backups. Unencrypted backups will be destroyed after the first encrypted backup has been completed.
What should be done to enable encryption for future backups?
Correct answer
Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot
Enable default encryption for the Amazon S3 bucket where backups are stored
Modify the backup section of the database configuration to toggle the Enable encryption check box
Enable an encrypted read replica on RDS for MySQL. Promote the encrypted read replica to primary. Remove the original database instance
Overall explanation
Amazon RDS uses snapshots for backup. Snapshots are encrypted when created only if the database is encrypted and you can only select encryption for the database when you first create it. In this case the database, and hence the snapshots, ad unencrypted.
However, you can create an encrypted copy of a snapshot. You can restore using that snapshot which creates a new DB instance that has encryption enabled. From that point on encryption will be enabled for all snapshots.
CORRECT: "Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot" is the correct answer.
INCORRECT: "Enable an encrypted read replica on RDS for MySQL. Promote the encrypted read replica to primary. Remove the original database instance" is incorrect as you cannot create an encrypted read replica from an unencrypted master.
INCORRECT: "Modify the backup section of the database configuration to toggle the Enable encryption check box" is incorrect as you cannot add encryption for an existing database.
INCORRECT: "Enable default encryption for the Amazon S3 bucket where backups are stored" is incorrect because you do not have access to the S3 bucket in which snapshots are stored.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Management & Governance
Question 37Skipped
An application allows users to upload and download files. Files older than 2 years will be accessed less frequently. A solutions architect needs to ensure that the application can scale to any number of files while maintaining high availability and durability.
Which scalable solutions should the solutions architect recommend?
Store the files in Amazon Elastic Block Store (EBS) volumes. Schedule snapshots of the volumes. Use the snapshots to archive data older than 2 years
Store the files in Amazon Elastic Block Store (EBS) volumes. Create a lifecycle policy to move files older than 2 years to Amazon S3 Glacier
Store the files on Amazon Elastic File System (EFS) with a lifecycle policy that moves objects older than 2 years to EFS Infrequent Access (EFS IA)
Correct answer
Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)
Overall explanation
S3 Standard-IA is for data that is accessed less frequently, but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval fee. This combination of low cost and high performance make S3 Standard-IA ideal for long-term storage, backups, and as a data store for disaster recovery files.
CORRECT: "Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)" is the correct answer.
INCORRECT: "Store the files on Amazon Elastic File System (EFS) with a lifecycle policy that moves objects older than 2 years to EFS Infrequent Access (EFS IA)" is incorrect. With EFS you can transition files to EFS IA after a file has not been accessed for a specified period of time with options up to 90 days. You cannot transition based on an age of 2 years.
INCORRECT: "Store the files in Amazon Elastic Block Store (EBS) volumes. Schedule snapshots of the volumes. Use the snapshots to archive data older than 2 years" is incorrect. You cannot identify the age of data and archive snapshots in this way with EBS.
INCORRECT: "Store the files in Amazon Elastic Block Store (EBS) volumes. Create a lifecycle policy to move files older than 2 years to Amazon S3 Glacier" is incorrect. You cannot archive files from an EBS volume to Glacier using lifecycle policies.
References:
https://aws.amazon.com/s3/storage-classes/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Management & Governance
Question 43Skipped
An on-premises server runs a MySQL database and will be migrated to the AWS Cloud. The company require a managed solution that supports high availability and automatic failover in the event of the outage of an Availability Zone (AZ).
Which solution is the BEST fit for these requirements?
Correct answer
Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment
Use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon RDS MySQL. Use the Schema Conversion Tool (SCT) to enable conversion from MySQL to Amazon RDS
Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon EC2 MySQL Multi-AZ deployment
Create a snapshot of the MySQL database server and use AWS DataSync to migrate the data Amazon S3. Launch a new Amazon RDS MySQL Multi-AZ deployment from the snapshot
Overall explanation
The AWS DMS service can be used to directly migrate the MySQL database to an Amazon RDS Multi-AZ deployment. The entire process can be online and is managed for you. There is no need to perform schema translation between MySQL and RDS (assuming you choose the MySQL RDS engine).


CORRECT: "Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment" is the correct answer.
INCORRECT: "Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon EC2 MySQL Multi-AZ deployment" is incorrect as there is no such thing as “multi-AZ” on Amazon EC2 with MySQL, you must use RDS.
INCORRECT: "Create a snapshot of the MySQL database server and use AWS DataSync to migrate the data Amazon S3. Launch a new Amazon RDS MySQL Multi-AZ deployment from the snapshot" is incorrect. You cannot create a snapshot of a MySQL database server running on-premises.
INCORRECT: "Use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon RDS MySQL. Use the Schema Conversion Tool (SCT) to enable conversion from MySQL to Amazon RDS" is incorrect. There is no need to convert the schema when migrating from MySQL to Amazon RDS (MySQL engine).
References:
https://aws.amazon.com/rds/features/multi-az/
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
https://digitalcloud.training/aws-migration-services/
