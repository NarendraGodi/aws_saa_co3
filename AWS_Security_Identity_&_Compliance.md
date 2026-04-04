
#AWS Security, Identity, & Compliance

Question 18Skipped
**A company runs an application in a private subnet within a VPC. The application is integrated with Amazon Cognito using a user pool for user authentication. The company wants to enable users to securely upload and store their documents in an Amazon S3 bucket.
What combination of steps should the company take to securely integrate the application with Amazon S3? (Select TWO.)**
Configure the application to generate Amazon S3 access tokens directly from the Cognito user pool.
Assign IAM roles directly to the S3 bucket to allow user-level access.
**Correct selection
Enable Amazon S3 VPC endpoints in the VPC to ensure private connectivity between the application and the S3 bucket.**
**Correct selection
Configure an Amazon Cognito identity pool to provide temporary credentials** for Amazon S3 when users authenticate through the user pool.
Add a bucket policy to deny requests that do not include valid Amazon Cognito credentials.
*Overall explanation*
Configure an Amazon Cognito identity pool to provide temporary credentials for Amazon S3 when users authenticate through the user pool: This is correct because an Amazon Cognito identity pool is required to grant temporary AWS credentials for accessing S3 buckets. The user pool alone does not provide direct access to AWS resources, so the identity pool integrates with the user pool to securely grant users permissions to interact with S3.
Enable Amazon S3 VPC endpoints in the VPC to ensure private connectivity between the application and the S3 bucket: This is correct because the application runs in a private subnet and needs secure connectivity to Amazon S3. A VPC endpoint ensures traffic remains within the AWS network, improving security and reducing reliance on internet gateways or NAT gateways.
Add a bucket policy to deny requests that do not include valid Amazon Cognito credentials: This is incorrect because bucket policies can restrict access based on certain conditions, but integrating Amazon Cognito requires granting access through IAM roles tied to identity pools, not bucket policies.
Assign IAM roles directly to the S3 bucket to allow user-level access: This is incorrect because IAM roles are assigned to entities like users or identity pools, not to resources like S3 buckets. The proper method involves attaching policies to the identity pool role to grant temporary credentials.
Configure the application to generate Amazon S3 access tokens directly from the Cognito user pool: This is incorrect because user pools authenticate users but do not directly provide credentials for AWS services. An identity pool is required to bridge the authentication process with AWS resource access.
References:
https://docs.aws.amazon.com/cognito/latest/developerguide/identity-pools.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/privatelink-interface-endpoints.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cognito/
https://digitalcloud.training/amazon-s3-and-glacier/


Question 19Skipped
**A genetics research firm processes DNA sequencing data for multiple clients. The raw data is stored in relational databases provided by each client. The company must extract the data, apply unique transformation algorithms for each client, and store the processed results in Amazon S3.
Due to the sensitivity of the data, the company must encrypt it both during processing and at rest in Amazon S3. Each client must have their own encryption keys to meet compliance requirements. The company also wants to minimize operational overhead while implementing this solution.
Which solution will meet these requirements with the LEAST operational effort?**
Use AWS Glue to create a single ETL pipeline for all clients. Configure the pipeline to tag each client’s data and use server-side encryption with AWS KMS keys (SSE-KMS) to encrypt data based on client-specific keys before storing it in Amazon S3.
**Correct answer
Use AWS Glue to create individual ETL jobs for each client. Attach a security configuration that uses client-specific AWS KMS keys for server-side encryption (SSE-KMS) during processing and storage in S3.**
Deploy a centralized Amazon EMR cluster to process data for all clients. Encrypt the data in transit using TLS certificates for each client and store the data in Amazon S3 using server-side encryption with Amazon S3 managed keys (SSE-S3).
Deploy an Amazon EMR cluster for each client with a client-specific Hadoop configuration. Use client-side encryption (CSE) to encrypt data with customer-managed root keys during transformations and upload the results to S3.
*Overall explanation*
Use AWS Glue to create individual ETL jobs for each client. Attach a security configuration that uses client-specific AWS KMS keys for server-side encryption (SSE-KMS) during processing and storage in S3: This is correct because AWS Glue simplifies ETL workflows and supports attaching security configurations to enforce client-specific encryption with KMS keys. This approach minimizes operational effort by automating the process while meeting encryption requirements.
Use AWS Glue to create a single ETL pipeline for all clients. Configure the pipeline to tag each client’s data and use server-side encryption with AWS KMS keys (SSE-KMS) to encrypt data based on client-specific keys before storing it in Amazon S3: This is incorrect because a single ETL pipeline complicates the tagging and encryption logic, increasing the risk of errors. Separate ETL jobs for each client provide a cleaner and more scalable solution.
Deploy an Amazon EMR cluster for each client with a client-specific Hadoop configuration. Use client-side encryption (CSE) to encrypt data with customer-managed root keys during transformations and upload the results to S3: This is incorrect because deploying separate EMR clusters for each client significantly increases operational overhead and costs. AWS Glue is a more efficient solution for this workload.
Deploy a centralized Amazon EMR cluster to process data for all clients. Encrypt the data in transit using TLS certificates for each client and store the data in Amazon S3 using server-side encryption with Amazon S3 managed keys (SSE-S3): This is incorrect because TLS encrypts data only in transit, not during processing. Additionally, SSE-S3 does not meet the compliance requirement of using client-specific encryption keys.
References:
https://docs.aws.amazon.com/glue/latest/dg/encryption-security-configurations.html
https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-glue/


Question 33Skipped
**A company uses an Amazon RDS for MySQL instance for its operational database. To handle the increased read-only traffic during a recent peak period, the company added a read replica. During the peak period, the CPU usage on the read replica reached 60%, and the primary instance also had 60% CPU usage. After the peak period ended, the read replica's CPU usage decreased to 25%, while the primary instance consistently remains at 60%. The company wants to optimize costs while ensuring enough capacity for future growth.
Which solution will meet these requirements?**
Delete the read replica and keep the primary instance unchanged.
Upgrade the read replica to a larger instance size and downgrade the primary instance to a smaller instance size.
Delete the read replica and upgrade the primary instance to a larger instance size.
**Correct answer
Resize the read replica to a smaller instance size and keep the primary instance unchanged.**
*Overall explanation*
Resize the read replica to a smaller instance size and keep the primary instance unchanged: This is correct because the read replica’s CPU usage is now consistently low at 25%, meaning a smaller instance size can accommodate the current workload. Keeping the primary instance unchanged ensures consistent performance for write-heavy workloads.
Delete the read replica and keep the primary instance unchanged: This is incorrect because the read replica may still be needed for future peak periods or reporting and removing it could impact performance if the workload increases again.
Upgrade the read replica to a larger instance size and downgrade the primary instance to a smaller instance size: This is incorrect because the primary instance already has consistent 60% CPU usage. Downgrading it could result in performance bottlenecks.
Delete the read replica and upgrade the primary instance to a larger instance size: This is incorrect because increasing the primary instance size will unnecessarily increase costs, especially since the read replica can handle reporting traffic at a lower cost.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
https://aws.amazon.com/rds/features/resize/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/


Question 48Skipped
**An AWS Organization has an OU with multiple member accounts in it. The company needs to restrict the ability to launch only specific Amazon EC2 instance types. How can this policy be applied across the accounts with the least effort?**
Create an SCP with an allow rule that allows launching the specific instance types
Create an IAM policy to deny launching all but the specific instance types
**Correct answer
Create an SCP with a deny rule that denies all but the specific instance types
Use AWS Resource Access Manager to control which launch types can be used**
*Overall explanation*
To apply the restrictions across multiple member accounts you must use a Service Control Policy (SCP) in the AWS Organization. The way you would do this is to create a deny rule that applies to anything that does not equal the specific instance type you want to allow.
The following architecture could be used to achieve this goal:


CORRECT: "Create an SCP with a deny rule that denies all but the specific instance types" is the correct answer.
INCORRECT: "Create an SCP with an allow rule that allows launching the specific instance types" is incorrect as a deny rule is required.
INCORRECT: "Create an IAM policy to deny launching all but the specific instance types" is incorrect. With IAM you need to apply the policy within each account rather than centrally so this would require much more effort.
INCORRECT: "Use AWS Resource Access Manager to control which launch types can be used" is incorrect. AWS Resource Access Manager (RAM) is a service that enables you to easily and securely share AWS resources with any AWS account or within your AWS Organization. It is not used for restricting access or permissions.
References:
https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_example-scps.html#example-ec2-instances
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-organizations/


Question 58Skipped
**A financial institution is designing the architecture for a new data processing platform on AWS. The institution uses organizational units (OUs) in AWS Organizations to manage its accounts. To comply with regulatory requirements, all Amazon EC2 instances must include a compliance-level tag with values of compliant or noncompliant. IAM users must not be allowed to create EC2 instances without this tag or modify the tag after creation.
Which combination of steps will meet these requirements? (Select TWO.)
Create an IAM policy that denies the deletion of tags on EC2 instances. Assign this policy to all IAM users who manage EC2 resources in the organization's accounts.**
Use AWS Config to check for compliance-level tags on EC2 instances. Configure AWS Config to remediate noncompliant resources by automatically adding the required tags to EC2 instances.
**Correct selection
In AWS Organizations, create a tag policy to enforce the use of the compliance-level tag with the required values. Attach the tag policy to the appropriate OU to ensure EC2 instances adhere to the tagging requirements.
Correct selection
In AWS Organizations, create a service control policy (SCP) to deny the creation of EC2 instances if the compliance-level tag is not specified. Attach the SCP to the appropriate OU.**
Use AWS Lambda with an EventBridge rule to trigger a function whenever a new EC2 instance is created. Configure the function to terminate any instance that does not include the compliance-level tag with the correct values.
*Overall explanation*
In AWS Organizations, create a service control policy (SCP) to deny the creation of EC2 instances if the compliance-level tag is not specified. Attach the SCP to the appropriate OU: This is correct because SCPs are used to enforce policies across accounts in an organization. By denying the creation of EC2 instances without the required tag, this SCP ensures that all instances are tagged at creation.
In AWS Organizations, create a tag policy to enforce the use of the compliance-level tag with the required values. Attach the tag policy to the appropriate OU to ensure EC2 instances adhere to the tagging requirements: This is correct because tag policies enforce tagging standards for AWS resources. By attaching the tag policy to the OU, you ensure that all EC2 instances follow the defined tagging requirements.
Use AWS Config to check for compliance-level tags on EC2 instances. Configure AWS Config to remediate noncompliant resources by automatically adding the required tags to EC2 instances: This is incorrect because AWS Config cannot prevent resource creation or modification. It can detect noncompliance but requires additional tools like Lambda for remediation, which introduces operational overhead.
Create an IAM policy that denies the deletion of tags on EC2 instances. Assign this policy to all IAM users who manage EC2 resources in the organization's accounts: This is incorrect because IAM policies apply only at the user or role level and cannot enforce organization-wide restrictions. SCPs and tag policies are better suited for this requirement.
Use AWS Lambda with an EventBridge rule to trigger a function whenever a new EC2 instance is created. Configure the function to terminate any instance that does not include the compliance-level tag with the correct values: This is incorrect because using Lambda for real-time remediation introduces operational complexity. SCPs and tag policies are more efficient and simpler to manage.
References:
https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies.html
https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tag-policies.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-organizations/


Question 7Skipped
**An application upgrade caused some issues with stability. The application owner enabled logging and has generated a 5 GB log file in an Amazon S3 bucket. The log file must be securely shared with the application vendor to troubleshoot the issues.
What is the MOST secure way to share the log file?**
Create access keys using an administrative account and share the access key ID and secret access key with the vendor.
**Correct answer
Generate a presigned URL and ask the vendor to download the log file before the URL expires.**
Create an IAM user for the vendor to provide access to the S3 bucket and the application. Enforce multi-factor authentication.
Enable default encryption for the bucket and public access. Provide the S3 URL of the file to the vendor.
*Overall explanation*
A presigned URL gives you access to the object identified in the URL. When you create a presigned URL, you must provide your security credentials and then specify a bucket name, an object key, an HTTP method (PUT for uploading objects), and an expiration date and time. The presigned URLs are valid only for the specified duration. That is, you must start the action before the expiration date and time.
This is the most secure way to provide the vendor with time-limited access to the log file in the S3 bucket.
CORRECT: "Generate a presigned URL and ask the vendor to download the log file before the URL expires" is the correct answer.
INCORRECT: "Create an IAM user for the vendor to provide access to the S3 bucket and the application. Enforce multi-factor authentication" is incorrect. This is less secure as you have to create an account to access AWS and then ensure you lock down the account appropriately.
INCORRECT: "Create access keys using an administrative account and share the access key ID and secret access key with the vendor" is incorrect. This is extremely insecure as the access keys will provide administrative permissions to AWS and should never be shared.
INCORRECT: "Enable default encryption for the bucket and public access. Provide the S3 URL of the file to the vendor" is incorrect. Encryption does not assist here as the bucket would be public and anyone could access it.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/ShareObjectPreSignedURL.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/


Question 21Skipped
**An organization plans to deploy a higher performance computing (HPC) workload on AWS using Linux. The HPC workload will use many Amazon EC2 instances and will generate a large quantity of small output files that must be stored in persistent storage for future use.
A Solutions Architect must design a solution that will enable the EC2 instances to access data using native file system interfaces and to store output files in cost-effective long-term storage.
Which combination of AWS services meets these requirements?**
AWS DataSync with Amazon S3 Intelligent tiering.
Amazon EBS volumes with Amazon S3 Glacier.
**Correct answer
Amazon FSx for Lustre with Amazon S3.**
Amazon FSx for Windows File Server with Amazon S3.
*Overall explanation*
Amazon FSx for Lustre is ideal for high performance computing (HPC) workloads running on Linux instances. FSx for Lustre provides a native file system interface and works as any file system does with your Linux operating system.
When linked to an Amazon S3 bucket, FSx for Lustre transparently presents objects as files, allowing you to run your workload without managing data transfer from S3.
This solution provides all requirements as it enables Linux workloads to use the native file system interfaces and to use S3 for long-term and cost-effective storage of output files.


CORRECT: "Amazon FSx for Lustre with Amazon S3" is the correct answer.
INCORRECT: "Amazon FSx for Windows File Server with Amazon S3" is incorrect. This service should be used with Windows instances and does not integrate with S3.
INCORRECT: "Amazon EBS volumes with Amazon S3 Glacier" is incorrect. EBS volumes do not provide the shared, high performance storage solution using file system interfaces.
INCORRECT: "AWS DataSync with Amazon S3 Intelligent tiering" is incorrect. AWS DataSync is used for migrating / synchronizing data.
References:
https://aws.amazon.com/fsx/lustre/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/


Question 30Skipped
**A social media platform uses Amazon DynamoDB to store user profiles, friend connections, and post interactions. The platform is rapidly expanding to new countries and needs to ensure a seamless user experience with high availability and low latency for its global user base.
The platform must handle unpredictable workloads and regional outages while maintaining a cost-effective architecture.
Which solution will meet these requirements MOST cost-effectively?**
Use DynamoDB Accelerator (DAX) to reduce read latency for frequently accessed items. Deploy DynamoDB tables in a single Region and use manual Cross-Region Replication to replicate data to other Regions for fault tolerance.
**Correct answer
Use DynamoDB global tables to replicate data automatically across multiple Regions. Deploy the tables in on-demand capacity mode to handle workload variability.**
Deploy DynamoDB tables in a single AWS Region using provisioned capacity mode. Use DynamoDB Streams to replicate data asynchronously to a secondary Region for failover.
Use Amazon S3 to store user data and replicate the data across multiple Regions using S3 Cross-Region Replication. Use AWS Lambda to perform real-time data updates for the application.
*Overall explanation*
Use DynamoDB global tables to replicate data automatically across multiple Regions. Deploy the tables in on-demand capacity mode to handle workload variability: This is correct because DynamoDB global tables provide automatic multi-Region replication, ensuring low latency and high availability for a global user base. On-demand capacity mode is a cost-effective choice for workloads with unpredictable demand, as it adjusts capacity based on usage.
Deploy DynamoDB tables in a single AWS Region using provisioned capacity mode. Use DynamoDB Streams to replicate data asynchronously to a secondary Region for failover: This is incorrect because using DynamoDB Streams for cross-Region replication requires a custom implementation, which increases operational overhead. Additionally, a single primary Region does not ensure low latency for a global user base.
Use Amazon S3 to store user data and replicate the data across multiple Regions using S3 Cross-Region Replication. Use AWS Lambda to perform real-time data updates for the application: This is incorrect because S3 is not designed for transactional, low latency use cases like a social media platform. DynamoDB is the better choice for structured, real-time data access.
Use DynamoDB Accelerator (DAX) to reduce read latency for frequently accessed items. Deploy DynamoDB tables in a single Region and use manual Cross-Region Replication to replicate data to other Regions for fault tolerance: This is incorrect because DAX reduces read latency but does not provide global availability or automatic replication. Manual Cross-Region Replication adds operational complexity and is less reliable than global tables.
References:
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GlobalTables.html
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadWriteCapacityMode.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-dynamodb/


Question 38Skipped
**A company hosts a website on Amazon EC2 instances behind an Application Load Balancer (ALB). The website serves static content. Website traffic is increasing. The company wants to minimize the website hosting costs.
Which solution will meet these requirements?**
Move the website to an Amazon S3 bucket. Configure an Amazon ElastiCache cluster for the S3 bucket.
**Correct answer
Move the website to an Amazon S3 bucket. Configure an Amazon CloudFront distribution for the S3 bucket.**
Move the website to AWS Amplify. Configure an ALB to resolve to the Amplify website.
Move the website to AWS Amplify. Configure EC2 instances to cache the website.
*Overall explanation*
Move the website to an Amazon S3 bucket. Configure an Amazon CloudFront distribution for the S3 bucket: This is correct because Amazon S3 is cost-effective for serving static content. Adding CloudFront ensures global content delivery with reduced latency and caching, which minimizes hosting costs.
Move the website to an Amazon S3 bucket. Configure an Amazon ElastiCache cluster for the S3 bucket: This is incorrect because ElastiCache is designed for in-memory data storage and retrieval, not for optimizing S3 access for static content.
Move the website to AWS Amplify. Configure an ALB to resolve to the Amplify website: This is incorrect because Amplify is already a fully managed service that does not require an ALB for static websites.
Move the website to AWS Amplify. Configure EC2 instances to cache the website: This is incorrect because using EC2 instances for caching introduces unnecessary complexity and cost for a static website.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/


Question 42Skipped
**A solutions architect is designing a two-tier web application. The application consists of a public-facing web tier hosted on Amazon EC2 in public subnets. The database tier consists of Microsoft SQL Server running on Amazon EC2 in a private subnet. Security is a high priority for the company.**
How should security groups be configured in this situation? (Select TWO.)
**Correct selection
Configure the security group for the web tier to allow inbound traffic on port 443 from 0.0.0.0/0 and to allow outbound traffic on port 1433 to the RDS
Configure the security group for the database tier to allow inbound traffic on ports 443 and 1433 from the security group for the web tier**
Configure the security group for the web tier to allow outbound traffic on port 443 from 0.0.0.0/0
Configure the security group for the database tier to allow outbound traffic on ports 443 and 1433 to the security group for the web tier
**Correct selection
Configure the security group for the database tier to allow inbound traffic on port 1433 from the security group for the web tier**
*Overall explanation*
In this scenario an inbound rule is required to allow traffic from any internet client to the web front end on SSL/TLS port 443. The source should therefore be set to 0.0.0.0/0 to allow any inbound traffic.
To secure the connection from the web frontend to the database tier, an outbound rule should be created from the public EC2 security group with a destination of the private EC2 security group. The port should be set to 1433 for MySQL. The private EC2 security group will also need to allow inbound traffic on 1433 from the public EC2 security group.
This configuration can be seen in the diagram:


CORRECT: "Configure the security group for the web tier to allow inbound traffic on port 443 from 0.0.0.0/0 and to allow outbound traffic on port 1433 to the RDS" is a correct answer.
CORRECT: "Configure the security group for the database tier to allow inbound traffic on port 1433 from the security group for the web tier" is also a correct answer.
INCORRECT: "Configure the security group for the web tier to allow outbound traffic on port 443 from 0.0.0.0/0" is incorrect as this is configured backwards.
INCORRECT: "Configure the security group for the database tier to allow outbound traffic on ports 443 and 1433 to the security group for the web tier" is incorrect as the MySQL database instance does not need to send outbound traffic on either of these ports.
INCORRECT: "Configure the security group for the database tier to allow inbound traffic on ports 443 and 1433 from the security group for the web tier" is incorrect as the database tier does not need to allow inbound traffic on port 443.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/


Question 43Skipped
**A company has a file share on a Microsoft Windows Server in an on-premises data center. The server uses a local network attached storage (NAS) device to store several terabytes of files. The management team require a reduction in the data center footprint and to minimize storage costs by moving on-premises storage to AWS.
What should a Solutions Architect do to meet these requirements?**
**Correct answer
Configure an AWS Storage Gateway file gateway.**
Configure an AWS Storage Gateway as a volume gateway.
Create an Amazon S3 bucket and an S3 gateway endpoint.
Create an Amazon EFS volume and use an IPSec VPN.
*Overall explanation*
An AWS Storage Gateway File Gateway provides your applications a file interface to seamlessly store files as objects in Amazon S3, and access them using industry standard file protocols. This removes the files from the on-premises NAS device and provides a method of directly mounting the file share for on-premises servers and clients.


CORRECT: "Configure an AWS Storage Gateway file gateway" is the correct answer.
INCORRECT: "Configure an AWS Storage Gateway as a volume gateway" is incorrect. A volume gateway uses block-based protocols. In this case we are replacing a NAS device which uses file-level protocols so the best option is a file gateway.
INCORRECT: "Create an Amazon EFS volume and use an IPSec VPN" is incorrect. EFS can be mounted over a VPN but it would have more latency than using a storage gateway.
INCORRECT: "Create an Amazon S3 bucket and an S3 gateway endpoint" is incorrect. S3 is an object-level storage system so is not suitable for this use case. A gateway endpoint is a method of accessing S3 using private addresses from your VPC, not from your data center.
References:
https://aws.amazon.com/storagegateway/faqs/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-storage-gateway/


Question 46Skipped
**A company runs a number of core enterprise applications in an on-premises data center. The data center is connected to an Amazon VPC using AWS Direct Connect. The company will be creating additional AWS accounts and these accounts will also need to be quickly, and cost-effectively connected to the on-premises data center in order to access the core applications.
What deployment changes should a Solutions Architect implement to meet these requirements with the LEAST operational overhead?**
Configure VPC endpoints in the Direct Connect VPC for all required services. Route the network traffic to the on-premises servers.
**Correct answer
Configure AWS Transit Gateway between the accounts. Assign Direct Connect to the transit gateway and route network traffic to the on-premises servers.**
Create a Direct Connect connection in each new account. Route the network traffic to the on-premises servers.
Create a VPN connection between each new account and the Direct Connect VPC. Route the network traffic to the on-premises servers.
*Overall explanation*
AWS Transit Gateway connects VPCs and on-premises networks through a central hub. With AWS Transit Gateway, you can quickly add Amazon VPCs, AWS accounts, VPN capacity, or AWS Direct Connect gateways to meet unexpected demand, without having to wrestle with complex connections or massive routing tables. This is the operationally least complex solution and is also cost-effective.
The image below depicts how transit gateway can assist with simplifying network deployments:


CORRECT: "Configure AWS Transit Gateway between the accounts. Assign Direct Connect to the transit gateway and route network traffic to the on-premises servers" is the correct answer.
INCORRECT: "Create a VPN connection between each new account and the Direct Connect VPC. Route the network traffic to the on-premises servers" is incorrect. You cannot connect VPCs using AWS managed VPNs and would need to configure a software VPN and then complex routing configurations. This is not the best solution.
INCORRECT: "Create a Direct Connect connection in each new account. Route the network traffic to the on-premises servers" is incorrect. This is an expensive solution as you would need to have multiple Direct Connect links.
INCORRECT: "Configure VPC endpoints in the Direct Connect VPC for all required services. Route the network traffic to the on-premises servers" is incorrect. You cannot create VPC endpoints for all services and this would be a complex solution for those you can.
References:
https://aws.amazon.com/transit-gateway/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-direct-connect/


Question 53Skipped
**A stock trading startup company has a custom web application to sell trading data to its users online. The company uses Amazon DynamoDB to store its data and wants to build a new service that sends an alert to the managers of four internal teams every time a new trading event is recorded. The company does not want this new service to affect the performance of the current application.
What should a solutions architect do to meet these requirements with the LEAST amount of operational overhead?**
Write new event data to the table using DynamoDB transactions. The transactions should be configured to notify internal teams.
**Correct answer
On the table, enable Amazon DynamoDB Streams. Subscriptions can be made to a single Amazon Simple Notification Service (Amazon SNS) topic using triggers.**
Use the current application to publish a message to four Amazon Simple Notification Service (Amazon SNS) topics. Each team should subscribe to one topic.
Create a custom attribute for each record to flag new items. A cron job can be written to scan the table every minute for new items and notify an Amazon Simple Queue Service (Amazon SQS) queue.
*Overall explanation*
DynamoDB Streams captures a time-ordered sequence of item-level modifications in any DynamoDB table and stores this information in a log for up to 24 hours. Applications can access this log and view the data items as they appeared before and after they were modified, in near-real time. This is the native way to handle this within DynamoDB, therefore will incur the least amount of operational overhead.
CORRECT: "On the table, enable Amazon DynamoDB Streams. Subscriptions can be made to a single Amazon Simple Notification Service (Amazon SNS) topic using triggers” is the correct answer (as explained above.)
INCORRECT: "Write new event data to the table using DynamoDB transactions. The transactions should be configured to notify internal teams” is incorrect. With Amazon DynamoDB transactions, you can group multiple actions together and submit them as a single all-or-nothing TransactWriteItems or TransactGetItems operation. The following sections describe API operations, capacity management, best practices, and other details about using transactional operations in DynamoDB. This is not suitable for this use case.
INCORRECT: "Use the current application to publish a message to four Amazon Simple Notification Service (Amazon SNS) topics. Each team should subscribe to one topic” is incorrect. Using four separate SNS topics will take a significant amount of overhead, and this functionality can be managed natively within DynamoDB using DynamoDB streams.
INCORRECT: "Create a custom attribute for each record to flag new items. A cron job can be written to scan the table every minute for new items and notify an Amazon Simple Queue Service (Amazon SQS) queue” is incorrect. Writing a CRON job also takes significant overhead compared to using DynamoDB streams.
References:
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-dynamodb/


Question 64Skipped
**A university operates its critical IT services, including authentication and DNS, from an on-premises data center. The data center is connected to AWS using AWS Direct Connect (DX). The university is onboarding additional AWS accounts for different departments, all of which need secure and consistent access to the on-premises services.
The university wants a scalable and cost-effective solution that minimizes operational overhead.
What should a solutions architect implement to meet these requirements?**
Deploy an AWS Site-to-Site VPN connection from the on-premises data center to each new AWS account. Configure route tables to forward traffic to the VPN.
Establish a VPC peering connection between the Direct Connect VPC and each new AWS account. Configure security groups to allow traffic to flow between the VPCs and the on-premises services.
**Correct answer
Configure AWS Transit Gateway to connect the Direct Connect gateway to the VPCs in the new accounts. Route network traffic from the new accounts to the on-premises data center through the transit gateway.**
Create a Direct Connect connection in each new AWS account and configure route tables in each VPC to send traffic to the on-premises data center.
*Overall explanation*
Configure AWS Transit Gateway to connect the Direct Connect gateway to the VPCs in the new accounts. Route network traffic from the new accounts to the on-premises data center through the transit gateway: This is correct because AWS Transit Gateway enables scalable connectivity between multiple VPCs and on-premises networks. By connecting the Direct Connect gateway to the transit gateway, traffic from new AWS accounts can securely access on-premises services with minimal operational overhead.
Deploy an AWS Site-to-Site VPN connection from the on-premises data center to each new AWS account. Configure route tables to forward traffic to the VPN: This is incorrect because setting up individual VPN connections for each account introduces significant operational complexity and ongoing costs. Direct Connect with a transit gateway is more scalable and efficient.
Establish a VPC peering connection between the Direct Connect VPC and each new AWS account. Configure security groups to allow traffic to flow between the VPCs and the on-premises services: This is incorrect because VPC peering is not scalable for managing multiple AWS accounts. Transit Gateway is designed for such use cases and reduces operational overhead.
Create a Direct Connect connection in each new AWS account and configure route tables in each VPC to send traffic to the on-premises data center: This is incorrect because creating multiple Direct Connect connections is expensive and unnecessary. A single Direct Connect gateway connected to a transit gateway can serve multiple accounts.
References:
https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-transit-gateway.html
https://aws.amazon.com/transit-gateway/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/


Question 23Skipped
**A company has deployed an API in a VPC behind an internal Network Load Balancer (NLB). An application that consumes the API as a client is deployed in a second account in private subnets.
Which architectural configurations will allow the API to be consumed without using the public Internet? (Select TWO.)**
**Correct selection
Configure a PrivateLink connection for the API into the client VPC. Access the API using the PrivateLink address**
Configure an AWS Resource Access Manager connection between the two accounts. Access the API using the private address
Configure a ClassicLink connection for the API into the client VPC. Access the API using the ClassicLink address
Configure an AWS Direct Connect connection between the two VPCs. Access the API using the private address
**Correct selection
Configure a VPC peering connection between the two VPCs. Access the API using the private address**
*Overall explanation*
You can create your own application in your VPC and configure it as an AWS PrivateLink-powered service (referred to as an endpoint service). Other AWS principals can create a connection from their VPC to your endpoint service using an interface VPC endpoint. You are the service provider, and the AWS principals that create connections to your service are service consumers.


This configuration is powered by AWS PrivateLink and clients do not need to use an internet gateway, NAT device, VPN connection or AWS Direct Connect connection, nor do they require public IP addresses.
Another option is to use a VPC Peering connection. A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account.
CORRECT: "Configure a VPC peering connection between the two VPCs. Access the API using the private address" is a correct answer.
CORRECT: "Configure a PrivateLink connection for the API into the client VPC. Access the API using the PrivateLink address" is also a correct answer.
INCORRECT: "Configure an AWS Direct Connect connection between the two VPCs. Access the API using the private address" is incorrect. Direct Connect is used for connecting from on-premises data centers into AWS. It is not used from one VPC to another.
INCORRECT: "Configure a ClassicLink connection for the API into the client VPC. Access the API using the ClassicLink address" is incorrect. ClassicLink allows you to link EC2-Classic instances to a VPC in your account, within the same Region. This is not relevant to sending data between two VPCs.
INCORRECT: "Configure an AWS Resource Access Manager connection between the two accounts. Access the API using the private address" is incorrect. AWS RAM lets you share resources that are provisioned and managed in other AWS services. However, APIs are not shareable resources with AWS RAM.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/endpoint-service.html
https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/


Question 27Skipped
**A company is deploying an application that produces data that must be processed in the order it is received. The company requires a solution for decoupling the event data from the processing layer. The solution must minimize operational overhead.
How can a Solutions Architect meet these requirements?**
Create an Amazon SQS standard queue to decouple the application. Set up an AWS Lambda function to process messages from the queue independently.
Create an Amazon SNS topic to decouple the application. Configure an Amazon SQS queue as a subscriber.
Create an Amazon SNS topic to decouple the application. Configure an AWS Lambda function as a subscriber.
**Correct answer
Create an Amazon SQS FIFO queue to decouple the application. Configure an AWS Lambda function to process messages from the queue.**
*Overall explanation*
Amazon SQS can be used to decouple this application using a FIFO queue. With a FIFO queue the order in which messages are sent and received is strictly preserved. You can configure an AWS Lambda function to poll the queue, or you can configure a Lambda function as a destination to asynchronously process messages from the queue.


CORRECT: "Create an Amazon SQS FIFO queue to decouple the application. Configure an AWS Lambda function to process messages from the queue" is the correct answer.
INCORRECT: "Create an Amazon SQS standard queue to decouple the application. Set up an AWS Lambda function to process messages from the queue independently" is incorrect. A standard queue only offers best-effort ordering so it may not preserve the order of the data.
INCORRECT: "Create an Amazon SNS topic to decouple the application. Configure an AWS Lambda function as a subscriber" is incorrect. Amazon SQS is better for this use case as there are a sequence of events for which the order must be maintained, and these events can be queued for processing whereas SNS delivers them for immediate processing.
INCORRECT: "Create an Amazon SNS topic to decouple the application. Configure an Amazon SQS queue as a subscriber" is incorrect. As above an SQS queue would be preferred for queuing the messages.
References:
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-configure-lambda-function-trigger.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/


Question 32Skipped
**An application has multiple components for receiving requests that must be processed and subsequently processing the requests. The company requires a solution for decoupling the application components. The application receives around 10,000 requests per day and requests can take up to 2 days to process. Requests that fail to process must be retained.
Which solution meets these requirements most efficiently?**
Decouple the application components with an Amazon SQS Topic. Configure the receiving component to subscribe to the SNS Topic.
Create an Amazon DynamoDB table and enable DynamoDB streams. Configure the processing component to process requests from the stream.
Use an Amazon Kinesis data stream to decouple application components and integrate the processing component with the Kinesis Client Library (KCL).
**Correct answer
Decouple the application components with an Amazon SQS queue. Configure a dead-letter queue to collect the requests that failed to process.**
*Overall explanation*
The Amazon Simple Queue Service (SQS) is ideal for decoupling the application components. Standard queues can support up to 120,000 in flight messages and messages can be retained for up to 14 days in the queue.
To ensure the retention of requests (messages) that fail to process, a dead-letter queue can be configured. Messages that fail to process are sent to the dead-letter queue (based on the redrive policy) and can be subsequently dealt with.
CORRECT: "Decouple the application components with an Amazon SQS queue. Configure a dead-letter queue to collect the requests that failed to process" is the correct answer.
INCORRECT: "Decouple the application components with an Amazon SQS Topic. Configure the receiving component to subscribe to the SNS Topic" is incorrect. SNS does not store requests, it immediately forwards all notifications to subscribers.
INCORRECT: "Use an Amazon Kinesis data stream to decouple application components and integrate the processing component with the Kinesis Client Library (KCL)" is incorrect. This is a less efficient solution and will likely be less cost-effective compared to using Amazon SQS. There is also no option for retention of requests that fail to process.
INCORRECT: "Create an Amazon DynamoDB table and enable DynamoDB streams. Configure the processing component to process requests from the stream" is incorrect. This solution does not offer any way of retaining requests that fail to process of removal of items from the table and is therefore less efficient.
References:
https://aws.amazon.com/sqs/faqs/
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/


Question 34Skipped
**A retail company runs an on-premises application that uses Java Spring Boot on Windows servers. The application is resource-intensive and handles customer-facing operations. The company wants to modernize the application by migrating it to a containerized environment running on AWS. The new solution must automatically scale based on Amazon CloudWatch metrics and minimize operational overhead for managing infrastructure.
Which solution will meet these requirements with the LEAST operational overhead?**
Use AWS App Runner to containerize the application. Deploy the containerized application to Amazon Elastic Kubernetes Service (Amazon EKS) on Amazon EC2 instances.
Use AWS App2Container to containerize the application. Deploy the containerized application to Amazon Elastic Container Service (Amazon ECS) on AWS Fargate by using an AWS CloudFormation template.
**Correct answer
Use AWS App Runner to containerize the application. Use App Runner to automatically deploy and manage the application without using ECS or EC2.**
Use AWS App2Container to containerize the application. Deploy the containerized application to Amazon Elastic Container Service (Amazon ECS) on Amazon EC2 instances by using an AWS CloudFormation template.
*Overall explanation*
Use AWS App Runner to containerize the application. Use App Runner to automatically deploy and manage the application without using ECS or EC2: This is correct because App Runner simplifies deployment and management of containerized applications. It automatically scales based on demand and integrates with CloudWatch, minimizing operational overhead.
Use AWS App2Container to containerize the application. Deploy the containerized application to Amazon Elastic Container Service (Amazon ECS) on AWS Fargate by using an AWS CloudFormation template: This is incorrect because while Fargate reduces operational overhead by eliminating the need to manage EC2 instances, using ECS still requires more configuration and maintenance compared to App Runner.
Use AWS App2Container to containerize the application. Deploy the containerized application to Amazon Elastic Container Service (Amazon ECS) on Amazon EC2 instances by using an AWS CloudFormation template: This is incorrect because running ECS on EC2 requires managing the underlying EC2 instances, which increases operational overhead.
Use AWS App Runner to containerize the application. Deploy the containerized application to Amazon Elastic Kubernetes Service (Amazon EKS) on Amazon EC2 instances: This is incorrect because EKS involves additional complexity in managing Kubernetes clusters and EC2 instances, making it less suitable for reducing operational overhead.
References:

https://aws.amazon.com/apprunner/

https://aws.amazon.com/app2container/


Question 39Skipped
**A Solutions Architect must design a solution to allow many Amazon EC2 instances across multiple subnets to access a shared data store. The data must be accessed by all instances simultaneously and access should use the NFS protocol. The solution must also be highly scalable and easy to implement.
Which solution best meets these requirements?**
Create an Amazon S3 bucket and configure a Network ACL. Grant the EC2 instances permission to access the bucket using the NFS protocol.
**Correct answer
Create an Amazon EFS file system. Configure a mount target in each Availability Zone. Attach each instance to the appropriate mount target.**
Configure an additional EC2 instance as a file server. Create a role in AWS IAM that grants permissions to the file share and attach the role to the EC2 instances.
Create an Amazon EBS volume and create a resource-based policy that grants an AWS IAM role access to the data. Attach the role to the EC2 instances.
*Overall explanation*
The Amazon Elastic File System (EFS) is a perfect solution for this requirement. Amazon EFS filesystems are accessed using the NFS protocol and can be mounted by many instances across multiple subnets simultaneously. EFS filesystems are highly scalable and very easy to implement.


CORRECT: "Create an Amazon EFS file system. Configure a mount target in each Availability Zone. Attach each instance to the appropriate mount target" is the correct answer.
INCORRECT: "Configure an additional EC2 instance as a file server. Create a role in AWS IAM that grants permissions to the file share and attach the role to the EC2 instances" is incorrect. You cannot use IAM roles to grant permissions to a file share created within the operating system of an EC2 instance. Also, this solution is not as highly scalable or easy to implement as Amazon EFS.
INCORRECT: "Create an Amazon S3 bucket and configure a Network ACL. Grant the EC2 instances permission to access the bucket using the NFS protocol" is incorrect. A Network ACL is created to restrict traffic in and out of subnets, it is not used to control access to S3 buckets (use a bucket policy or bucket ACL instead). You cannot grant permission to access an S3 bucket using a protocol, and NFS is not supported for S3 as it is an object-based storage system.
INCORRECT: "Create an Amazon EBS volume and create a resource-based policy that grants an AWS IAM role access to the data. Attach the role to the EC2 instances" is incorrect. You cannot configure a resource-based policy on an Amazon EBS volume.
References:
https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/


Question 64Skipped
**A streaming service company runs its video recommendation engine on an Amazon EC2 Auto Scaling group behind an Application Load Balancer (ALB) in a single AWS Region. The service generates personalized recommendations based on user activity and serves dynamic content to millions of users worldwide.
The company needs a cost-optimized solution to improve performance and scalability while ensuring that users across the globe experience low latency when accessing personalized recommendations.
Which solution will meet these requirements?**
**Correct answer
Set up an Amazon CloudFront distribution and configure the existing ALB as the origin. Use dynamic cache settings to reduce latency for global users.**
Migrate the recommendation engine to Amazon S3 and enable static website hosting. Use an Amazon CloudFront distribution to cache the content globally.
Configure AWS Global Accelerator to route traffic to the existing ALB and EC2 instances in the Region closest to each user.
Deploy additional EC2 instances and ALBs in multiple Regions. Use Amazon Route 53 latency-based routing to direct users to the Region with the lowest latency.
*Overall explanation*
Set up an Amazon CloudFront distribution and configure the existing ALB as the origin. Use dynamic cache settings to reduce latency for global users: This is correct because CloudFront provides a global content delivery network (CDN) that reduces latency by caching content closer to users. For dynamic content, CloudFront can still improve performance by optimizing requests and routing through its edge locations. This solution is cost-effective and requires minimal architectural changes.
Configure AWS Global Accelerator to route traffic to the existing ALB and EC2 instances in the Region closest to each user: This is incorrect because Global Accelerator improves performance for static and dynamic content, but it requires additional costs and does not cache dynamic content at the edge like CloudFront. It is better suited for multi-Region deployments.
Deploy additional EC2 instances and ALBs in multiple Regions. Use Amazon Route 53 latency-based routing to direct users to the Region with the lowest latency: This is incorrect because deploying and managing resources across multiple Regions increases cost and operational overhead. For a cost-optimized solution, CloudFront is more efficient as it uses its global edge locations without requiring additional infrastructure.
Migrate the recommendation engine to Amazon S3 and enable static website hosting. Use an Amazon CloudFront distribution to cache the content globally: This is incorrect because the recommendation engine serves dynamic content, which cannot be hosted on Amazon S3. S3 is designed for static content like images or HTML files and is not appropriate for processing user-specific dynamic data.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
https://aws.amazon.com/global-accelerator/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/


Question 39Skipped
**An IoT sensor is being rolled out to thousands of a company’s existing customers. The sensors will stream high volumes of data each second to a central location. A solution must be designed to ingest and store the data for analytics. The solution must provide near-real time performance and millisecond responsiveness.
Which solution should a Solutions Architect recommend?**
Ingest the data into an Amazon SQS queue. Process the data using an AWS Lambda function and then store the data in Amazon DynamoDB.
Ingest the data into an Amazon Kinesis Data Stream. Process the data with an AWS Lambda function and then store the data in Amazon RedShift.
Ingest the data into an Amazon SQS queue. Process the data using an AWS Lambda function and then store the data in Amazon RedShift.
**Correct answer
Ingest the data into an Amazon Kinesis Data Stream. Process the data with an AWS Lambda function and then store the data in Amazon DynamoDB.**
*Overall explanation*
A Kinesis data stream is a set of shards. Each shard contains a sequence of data records. A consumer is an application that processes the data from a Kinesis data stream. You can map a Lambda function to a shared-throughput consumer (standard iterator), or to a dedicated-throughput consumer with enhanced fan-out.
Amazon DynamoDB is the best database for this use case as it supports near-real time performance and millisecond responsiveness.
CORRECT: "Ingest the data into an Amazon Kinesis Data Stream. Process the data with an AWS Lambda function and then store the data in Amazon DynamoDB" is the correct answer.
INCORRECT: "Ingest the data into an Amazon Kinesis Data Stream. Process the data with an AWS Lambda function and then store the data in Amazon RedShift" is incorrect. Amazon RedShift cannot provide millisecond responsiveness.
INCORRECT: "Ingest the data into an Amazon SQS queue. Process the data using an AWS Lambda function and then store the data in Amazon RedShift" is incorrect. Amazon SQS does not provide near real-time performance and RedShift does not provide millisecond responsiveness.
INCORRECT: "Ingest the data into an Amazon SQS queue. Process the data using an AWS Lambda function and then store the data in Amazon DynamoDB" is incorrect. Amazon SQS does not provide near real-time performance.
References:
https://docs.aws.amazon.com/lambda/latest/dg/with-kinesis.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-kinesis/


Question 41Skipped
**An Amazon RDS PostgreSQL database is configured as Multi-AZ. A solutions architect needs to scale read performance and the solution must be configured for high availability. What is the most cost-effective solution?**
Deploy a read replica in the same AZ as the master DB instance
Deploy a read replica using Amazon ElastiCache
**Correct answer
Create a read replica as a Multi-AZ DB instance**
Deploy a read replica in a different AZ to the master DB instance
*Overall explanation*
You can create a read replica as a Multi-AZ DB instance. Amazon RDS creates a standby of your replica in another Availability Zone for failover support for the replica. Creating your read replica as a Multi-AZ DB instance is independent of whether the source database is a Multi-AZ DB instance.
CORRECT: "Create a read replica as a Multi-AZ DB instance" is the correct answer.
INCORRECT: "Deploy a read replica in a different AZ to the master DB instance" is incorrect as this does not provide high availability for the read replica
INCORRECT: "Deploy a read replica using Amazon ElastiCache" is incorrect as ElastiCache is not used to create read replicas of RDS database.
INCORRECT: "Deploy a read replica in the same AZ as the master DB instance" is incorrect as this solution does not include HA for the read replica.
References:
https://aws.amazon.com/about-aws/whats-new/2018/01/amazon-rds-read-replicas-now-support-multi-az-deployments/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/


Question 47Skipped
**A large MongoDB database running on-premises must be migrated to Amazon DynamoDB within the next few weeks. The database is too large to migrate over the company’s limited internet bandwidth so an alternative solution must be used. What should a Solutions Architect recommend?**
Setup an AWS Direct Connect and migrate the database to Amazon DynamoDB using the AWS Database Migration Service (DMS)
Use the AWS Database Migration Service (DMS) to extract and load the data to an AWS Snowball Edge device. Complete the migration to Amazon DynamoDB using AWS DMS in the AWS Cloud
**Correct answer
Use the Schema Conversion Tool (SCT) to extract and load the data to an AWS Snowball Edge device. Use the AWS Database Migration Service (DMS) to migrate the data to Amazon DynamoDB**
Enable compression on the MongoDB database and use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon DynamoDB
*Overall explanation*
Larger data migrations with AWS DMS can include many terabytes of information. This process can be cumbersome due to network bandwidth limits or just the sheer amount of data. AWS DMS can use Snowball Edge and Amazon S3 to migrate large databases more quickly than by other methods.
When you're using an Edge device, the data migration process has the following stages:
1. You use the AWS Schema Conversion Tool (AWS SCT) to extract the data locally and move it to an Edge device.
2. You ship the Edge device or devices back to AWS.
3. After AWS receives your shipment, the Edge device automatically loads its data into an Amazon S3 bucket.
4. AWS DMS takes the files and migrates the data to the target data store. If you are using change data capture (CDC), those updates are written to the Amazon S3 bucket and then applied to the target data store.
CORRECT: "Use the Schema Conversion Tool (SCT) to extract and load the data to an AWS Snowball Edge device. Use the AWS Database Migration Service (DMS) to migrate the data to Amazon DynamoDB" is the correct answer.
INCORRECT: "Setup an AWS Direct Connect and migrate the database to Amazon DynamoDB using the AWS Database Migration Service (DMS)" is incorrect as Direct Connect connections can take several weeks to implement.
INCORRECT: "Enable compression on the MongoDB database and use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon DynamoDB" is incorrect. It’s unlikely that compression is going to make the difference and the company want to avoid the internet link as stated in the scenario.
INCORRECT: "Use the AWS Database Migration Service (DMS) to extract and load the data to an AWS Snowball Edge device. Complete the migration to Amazon DynamoDB using AWS DMS in the AWS Cloud" is incorrect. This is the wrong method, the Solutions Architect should use the SCT to extract and load to Snowball Edge and then AWS DMS in the AWS Cloud.
References:
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_LargeDBs.html
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.DynamoDB.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/


Question 53Skipped
**An organization has a large amount of data on Windows (SMB) file shares in their on-premises data center. The organization would like to move data into Amazon S3. They would like to automate the migration of data over their AWS Direct Connect link.
Which AWS service can assist them?**
AWS Database Migration Service (DMS)
AWS CloudFormation
**Correct answer
AWS DataSync**
AWS Snowball
*Overall explanation*
AWS DataSync can be used to move large amounts of data online between on-premises storage and Amazon S3 or Amazon Elastic File System (Amazon EFS). DataSync eliminates or automatically handles many of these tasks, including scripting copy jobs, scheduling and monitoring transfers, validating data, and optimizing network utilization. The source datastore can be Server Message Block (SMB) file servers.
CORRECT: "AWS DataSync" is the correct answer.
INCORRECT: "AWS Database Migration Service (DMS)" is incorrect. AWS Database Migration Service (DMS) is used for migrating databases, not data on file shares.
INCORRECT: "AWS CloudFormation" is incorrect. AWS CloudFormation can be used for automating infrastructure provisioning. This is not the best use case for CloudFormation as DataSync is designed specifically for this scenario.
INCORRECT: "AWS Snowball" is incorrect. AWS Snowball is a hardware device that is used for migrating data into AWS. The organization plan to use their Direct Connect link for migrating data rather than sending it in via a physical device. Also, Snowball will not automate the migration.
References:
https://aws.amazon.com/datasync/faqs/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/


Question 58Skipped
**A Solutions Architect is designing an application that consists of AWS Lambda and Amazon RDS Aurora MySQL. The Lambda function must use database credentials to authenticate to MySQL and security policy mandates that these credentials must not be stored in the function code.
How can the Solutions Architect securely store the database credentials and make them available to the function?**
**Correct answer
Store the credentials in Systems Manager Parameter Store and update the function code and execution role**
Store the credentials in AWS Key Management Service and use environment variables in the function code pointing to KMS
Use the AWSAuthenticationPlugin and associate an IAM user account in the MySQL database
Create an IAM policy and store the credentials in the policy. Attach the policy to the Lambda function execution role
*Overall explanation*
In this case the scenario requires that credentials are used for authenticating to MySQL. The credentials need to be securely stored outside of the function code. Systems Manager Parameter Store provides secure, hierarchical storage for configuration data management and secrets management.
You can easily reference the parameters from services including AWS Lambda as depicted in the diagram below:

CORRECT: "Store the credentials in Systems Manager Parameter Store and update the function code and execution role" is the correct answer.
INCORRECT: "Store the credentials in AWS Key Management Service and use environment variables in the function code pointing to KMS" is incorrect. You cannot store credentials in KMS, it is used for creating and managing encryption keys
INCORRECT: "Use the AWSAuthenticationPlugin and associate an IAM user account in the MySQL database" is incorrect. This is a great way to securely authenticate to RDS using IAM users or roles. However, in this case the scenario requires database credentials to be used by the function.
INCORRECT: "Create an IAM policy and store the credentials in the policy. Attach the policy to the Lambda function execution role" is incorrect. You cannot store credentials in IAM policies.
References:
https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html


Question 7Skipped
**A solutions architect in a large finance organization must restrict access for a specific S3 bucket to only users in accounts within the organization in AWS Organizations. This is due to the confidentiality of project reports data.
Which solution meets these requirements with the LEAST amount of operational overhead?**
Use AWS CloudTrail to monitor the CreateAccount, InviteAccountToOrganization, LeaveOrganization, and RemoveAccountFromOrganization events. Update the S3 bucket policy accordingly.
**Correct answer
Add the aws:PrincipalOrgID global condition key with a reference to the organization ID to the S3 bucket policy.**
Tag each user that needs access to the S3 bucket. Add the aws:PrincipalTag global condition key to the S3 bucket policy.
Create an organizational unit (OU) for each department. Add the aws:PrincipalOrgPaths global condition key to the S3 bucket policy.
*Overall explanation*

PrincipalOrgId is used by specifying the Principal element in a resource-based policy. You can specify the organization ID in the condition element. When you add and remove accounts, policies that include the aws:PrincipalOrgID key automatically include the correct accounts and don't require manual updating.
For example, the following Amazon S3 bucket policy allows members of any account in the o-xxxxxxxxxxx organization to add an object into the policy-ninja-dev bucket.
CORRECT: "Add the aws:PrincipalOrgID global condition key with a reference to the organization ID to the S3 bucket policy" is the correct answer (as explained above.)
INCORRECT: "Create an organizational unit (OU) for each department. Add the aws:PrincipalOrgPaths global condition key to the S3 bucket policy" is incorrect.
This condition key ensures that the requester is an account member within the specified organization root or organizational units (OUs) in AWS Organizations. It is not required for this solution.
INCORRECT: "Use AWS CloudTrail to monitor the CreateAccount, InviteAccountToOrganization, LeaveOrganization, and RemoveAccountFromOrganization events. Update the S3 bucket policy accordingly" is incorrect. This option would be required for monitoring but not sharing access.
INCORRECT: "Tag each user that needs access to the S3 bucket. Add the aws:PrincipalTag global condition key to the S3 bucket policy" is incorrect. Since question is around cross account access, this option wouldn’t work as is.
References:
https://aws.amazon.com/blogs/security/control-access-to-aws-resources-by-using-the-aws-organization-of-iam-principals/
https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html
https://aws.amazon.com/blogs/security/iam-share-aws-resources-groups-aws-accounts-aws-organizations/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-organizations/


Question 14Skipped
**A music streaming company needs to incorporate a third-party song feed. The song feed sends a webhook to notify an external service when new songs are ready for consumption. A developer has written an AWS Lambda function to retrieve songs when the company receives a webhook callback. The developer must expose the Lambda function for the third party to invoke.
Which solution will meet these requirements with the LEAST operational complexity?**
Deploy a Network Load Balancer (NLB) to distribute requests to the Lambda function. Provide the NLB URL to the third party for the webhook.
Create an Amazon Simple Queue Service (Amazon SQS) queue. Connect the queue to the Lambda function. Provide the ARN of the SQS queue to the third party for the webhook.
Create an Amazon Simple Notification Service (Amazon SNS) topic. Link the topic to the Lambda function. Provide the SNS topic ARN to the third party for the webhook.
**Correct answer
Generate an API Gateway endpoint for the Lambda function. Provide the API Gateway endpoint to the third party for the webhook.**
*Overall explanation*
API Gateway enables you to create, deploy, and manage a RESTful API to expose backend HTTP endpoints, AWS Lambda functions, or other AWS services. You can provide the third party with the API Gateway endpoint, and they can invoke the Lambda function through it. This solution is the most operationally efficient because it requires the fewest resources and management overhead.
CORRECT: "Generate an API Gateway endpoint for the Lambda function. Provide the API Gateway endpoint to the third party for the webhook" is the correct answer (as explained above.)
INCORRECT: "Deploy a Network Load Balancer (NLB) to distribute requests to the Lambda function. Provide the NLB URL to the third party for the webhook" is incorrect.
While it is possible to trigger AWS Lambda from an Application Load Balancer (ALB), not NLB, using ALB would add unnecessary complexity to the solution.
INCORRECT: "Create an Amazon Simple Notification Service (Amazon SNS) topic. Link the topic to the Lambda function. Provide the SNS topic ARN to the third party for the webhook" is incorrect.
Amazon SNS is a pub/sub messaging service, but it is not meant to expose a public-facing endpoint for third-party webhooks. Also, providing ARN to a third party would not be possible as SNS topics cannot be invoked directly from the internet.
INCORRECT: "Create an Amazon Simple Queue Service (Amazon SQS) queue. Connect the queue to the Lambda function. Provide the ARN of the SQS queue to the third party for the webhook" is incorrect.
SQS is a message queuing service used to decouple and scale microservices, distributed systems, and serverless applications. It is not suitable for exposing a public-facing endpoint for third-party webhooks. Moreover, like SNS, SQS cannot be invoked directly from the internet.
References:
https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-api-gateway/


Question 21Skipped
**A company migrated a two-tier application from its on-premises data center to AWS Cloud. A Multi-AZ Amazon RDS for Oracle deployment is used for the data tier, along with 12 TB of General Purpose SSD Amazon EBS storage. With an average document size of 6 MB, the application processes, and stores documents as binary large objects (blobs) in the database.
Over time, the database size has grown, which has reduced performance and increased storage costs. A highly available and resilient solution is needed to improve database performance.
Which solution will meet these requirements MOST cost-effectively?**
Create a table in Amazon DynamoDB and update the application to use DynamoDB. Migrate Oracle data to DynamoDB using AWS Database Migration Service (AWS DMS).
Reduce the size of the RDS DB instance. Increase the storage capacity to 24 TiB. Magnetic storage should be selected.
Increase the RDS DB instance size. Increase the storage capacity to 24 TiB. Change the storage type to Provisioned IOPS.
**Correct answer
Set up an Amazon S3 bucket. The application should be updated to use S3 buckets to store documents. Store the object metadata in the existing database.**
*Overall explanation*
Amazon Simple Storage Service (Amazon S3) is an object storage service offering industry-leading scalability, data availability, security, and performance. The key in this question is the reference to binary large objects (blobs) which are stored in the database. Amazon S3 is an easy to use and very cost-effective solution for Write Once Read Many (WORM) applications and use cases.
CORRECT: "Set up an Amazon S3 bucket. The application should be updated to use S3 buckets to store documents. Store the object metadata in the existing database” is the correct answer (as explained above.)
INCORRECT: "Increase the RDS DB instance size. Increase the storage capacity to 24 TiB. Change the storage type to Provisioned IOPS” is incorrect. Doing this will increase the performance of your application, however the cost will go up and not go down.
INCORRECT: "Reduce the size of the RDS DB instance. Increase the storage capacity to 24 TiB. Magnetic storage should be selected” is incorrect. Reducing the instance size will only decrease the performance of your application, alongside changing your EBS volume to a Magnetic volume.
INCORRECT: "Create a table in Amazon DynamoDB and update the application to use DynamoDB. Migrate Oracle data to DynamoDB using AWS Database Migration Service (AWS DMS)” is incorrect. DynamoDB is more expensive than Amazon S3.
References:
https://aws.amazon.com/s3/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/


Question 28Skipped
**A company runs an API on a Linux server in their on-premises data center. The company are planning to migrate the API to the AWS cloud. The company require a highly available, scalable and cost-effective solution. What should a Solutions Architect recommend?**
Migrate the API server to Amazon EC2 instances in an Auto Scaling group and attach an Application Load Balancer
Migrate the API to Amazon API Gateway and migrate the backend to Amazon EC2
**Correct answer
Migrate the API to Amazon API Gateway and use AWS Lambda as the backend**
Migrate the API to Amazon CloudFront and use AWS Lambda as the origin
*Overall explanation*
The best option is to use a fully serverless solution. This will provide high availability, scalability and be cost-effective. The components for this would be Amazon API Gateway for hosting the API and AWS Lambda for running the backend.
As you can see in the image below, API Gateway can be the frontend for multiple backend services:


CORRECT: "Migrate the API to Amazon API Gateway and use AWS Lambda as the backend" is the correct answer.
INCORRECT: "Migrate the API to Amazon API Gateway and migrate the backend to Amazon EC2" is incorrect. This is a less available and cost-effective solution for the backend compared to AWS Lambda.
INCORRECT: "Migrate the API server to Amazon EC2 instances in an Auto Scaling group and attach an Application Load Balancer" is incorrect. Firstly, it may be difficult to load balance to an API. Additionally, this is a less cost-effective solution.
INCORRECT: "Migrate the API to Amazon CloudFront and use AWS Lambda as the origin" is incorrect. You cannot migrate an API to CloudFront. You can use CloudFront in front of API Gateway but that is not what this answer specifies.
References:
https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-with-lambda-integration.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/


Question 36Skipped
**A software firm is developing a microservices-based application to be deployed on Amazon ECS. This application needs to interact with a resilient, shared filesystem capable of restoring data to a different AWS Region with a Recovery Point Objective (RPO) of 2 hours.
The filesystem is also expected to provide a mount target in each Availability Zone (AZ) within a Region. The solutions architect intends to employ AWS Backup to oversee the cross-Region data replication.
Which option will meet these requirements?**
Amazon FSx for Windows File Server with a Multi-AZ deployment.
Amazon FSx for OpenZFS.
**Correct answer
Amazon Elastic File System (Amazon EFS) with the Standard storage class.**
Amazon FSx for NetApp ONTAP with a Multi-AZ deployment.
*Overall explanation*
Amazon Elastic File System (Amazon EFS) provides simple, scalable file storage for use with Amazon EC2 instances and other AWS services. It supports the Network File System (NFS) protocol and can be configured with mount points in multiple AZs.
EFS can be used with AWS Backup for automated and centralized backup across AWS services, and supports replication to another region, satisfying the given requirement.
All replication traffic stays on the AWS global backbone, and most changes are replicated within a minute, with an overall Recovery Point Objective (RPO) of 15 minutes for most file systems.
CORRECT: "Amazon Elastic File System (Amazon EFS) with the Standard storage class" is the correct answer (as explained above.)
INCORRECT: "Amazon FSx for Windows File Server with a Multi-AZ deployment" is incorrect.
Amazon FSx for Windows File Server provides fully managed, reliable, and scalable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol. It is built on Windows Server and offers a native Windows file system experience for Windows-based applications. However, it doesn't support cross-Region data replication, making it unsuitable for the given requirement.
INCORRECT: "Amazon FSx for NetApp ONTAP with a Multi-AZ deployment" is incorrect.
Amazon FSx for NetApp ONTAP is more suitable to scenarios where you want to migrate applications using ONTAP software and if you’re already using NetApp systems. It is better in this case to use Amazon EFS.
INCORRECT: "Amazon FSx for OpenZFS" is incorrect.
Amazon FSx for OpenZFS is suitable if you have a specific requirement to use OpenZFS. For this use case Amazon EFS is a better choice and will likely be more cost-effective.
References:
https://docs.aws.amazon.com/efs/latest/ug/efs-replication.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/


Question 47Skipped
**A global logistics company collects shipment tracking information, which updates every few seconds. The company wishes to perform real-time analysis on these data updates to monitor shipment progress and predict delays, after which they want the data to be ingested into their Amazon S3-based data lake. Which solution will fulfill these requirements with the MOST operational efficiency?**
Use Amazon SQS for data ingestion and Amazon EMR for real-time analysis.
Use AWS Direct Connect for data ingestion and Amazon Athena for real-time analysis.
**Correct answer
Use Amazon Kinesis Data Firehose for data ingestion and Amazon Managed Service for Apache Flink for real-time analysis.**
Use Amazon Kinesis Data Streams for data ingestion and AWS Lambda for real-time data analysis.
*Overall explanation*
Amazon Kinesis Data Firehose is ideal for ingesting high-velocity data into AWS, like the shipment tracking data in this scenario. It can capture, transform, and load streaming data into data lakes on S3. Amazon Managed Service for Apache Flink can then analyze this data in real-time, making this the most operationally efficient solution.
CORRECT: "Use Amazon Kinesis Data Firehose for data ingestion and Amazon Managed Service for Apache Flink for real-time analysis" is the correct answer (as explained above.)
INCORRECT: "Use Amazon Kinesis Data Streams for data ingestion and AWS Lambda for real-time data analysis" is incorrect.
Kinesis Data Streams can handle real-time data ingestion and Lambda can perform real-time processing, but this approach requires managing the stream consumers (like AWS Lambda) and ensuring they are scaled properly. This may not be the most operationally efficient solution.
INCORRECT: "Use AWS Direct Connect for data ingestion and Amazon Athena for real-time analysis" is incorrect.
AWS Direct Connect is a networking service primarily for establishing dedicated network connections from on-premises to AWS, not typically used for high-velocity data ingestion. Amazon Athena is more suitable for ad-hoc querying on S3 data, not real-time analysis.
INCORRECT: "Use Amazon SQS for data ingestion and Amazon EMR for real-time analysis" is incorrect.
Amazon SQS is capable of handling high-throughput workloads, but it's more suited to decoupling and scaling microservices, distributed systems, and serverless applications. Amazon EMR is a managed cluster platform that simplifies running big data frameworks, but it is not suitable for real-time data analysis.
References:
https://aws.amazon.com/kinesis/data-analytics/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-kinesis/


Question 52Skipped
**A financial firm is aiming to leverage AWS Cloud for augmenting its on-premises disaster recovery (DR) architecture. The firm's main application, running on PostgreSQL, is housed on a virtual machine (VM) on-premises. The DR solution needs to align with the application's recovery point objective (RPO) of less than a minute and a recovery time objective (RTO) of within two hours, all while keeping costs to a minimum.
Which solution will meet these requirements?**
Configure an active-active multi-site setup between the on-premises server and AWS using PostgreSQL with a third-party high availability solution.
**Correct answer
Set up a warm standby Amazon RDS for PostgreSQL database on AWS.** Configure AWS Database Migration Service (AWS DMS) to use change data capture (CDC).
Utilize third-party backup software to perform daily backups and store a secondary set of backups in Amazon S3.
Use AWS Elastic Disaster Recovery with continuous replication to act as a pilot light solution on AWS.
*Overall explanation*
Configuring a warm standby Amazon RDS for PostgreSQL database on AWS and using AWS DMS with change data capture will meet the RTO and RPO requirements. DMS can handle the ongoing replication from the on-premises PostgreSQL to the standby RDS instance, providing a near real-time replica of the data.
In a DR scenario, this standby instance can be promoted to become the new primary database, meeting the required RTO and RPO.
CORRECT: "Set up a warm standby Amazon RDS for PostgreSQL database on AWS. Configure AWS Database Migration Service (AWS DMS) to use change data capture (CDC)" is the correct answer (as explained above.)
INCORRECT: "Configure an active-active multi-site setup between the on-premises server and AWS using PostgreSQL with a third-party high availability solution" is incorrect.
Setting up an active-active multi-site setup between the on-premises server and AWS using PostgreSQL with a third-party high availability solution might meet the RPO and RTO requirements, but it would likely be more expensive and complex than the correct answer.
INCORRECT: "Use AWS Elastic Disaster Recovery with continuous replication to act as a pilot light solution on AWS" is incorrect.
AWS Elastic Disaster Recovery with continuous replication can provide a DR solution, but for a database, it is typically more efficient to use a service designed for that purpose, like RDS with DMS.
INCORRECT: "Utilize third-party backup software to perform daily backups and store a secondary set of backups in Amazon S3" is incorrect.
Using third-party backup software to perform daily backups and storing a secondary set of backups in Amazon S3 would not meet the RPO of less than a minute, as this approach could lead to a data loss up to 24 hours. Also, the process of restoring from a backup might not meet the RTO of within two hours.
References:
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Task.CDC.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
https://digitalcloud.training/aws-migration-services/


Question 60Skipped
**An application has been migrated from on-premises to an Amazon EC2 instance. The migration has failed to an unknown dependency that the application must communicate with an on-premises server using private IP addresses.
Which action should a solutions architect take to quickly provision the necessary connectivity?**
Create an Amazon CloudFront distribution
Create an AWS Transit Gateway
**Correct answer
Configure a Virtual Private Gateway**
Setup an AWS Direct Connect connection
*Overall explanation*
A virtual private gateway is a logical, fully redundant distributed edge routing function that sits at the edge of your VPC. You must create a VPG in your VPC before you can establish an AWS Managed site-to-site VPN connection. The other end of the connection is the customer gateway which must be established on the customer side of the connection.

CORRECT: "Configure a Virtual Private Gateway" is the correct answer.
INCORRECT: "Setup an AWS Direct Connect connection" is incorrect as this would take too long to provision.
INCORRECT: "Create an Amazon CloudFront distribution" is incorrect. This is not a solution for enabling connectivity using private addresses to an on-premises site. CloudFront is a content delivery network (CDN).
INCORRECT: "Create an AWS Transit Gateway" is incorrect. AWS Transit Gateway connects VPCs and on-premises networks through a central hub which is not a requirement of this solution.
References:
https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/


Question 63Skipped
**An organization manages its own MySQL databases, which are hosted on Amazon EC2 instances. In response to changes in demand, replication and scaling are manually managed by the company. It is essential for the company to have a way to add and remove compute capacity as needed from the database tier. The solution also must offer improved performance, scaling, and durability with minimal effort from operations.
Which solution meets these requirements?**
Consolidate the databases into a single MySQL database. Use larger EC2 instances for the larger database.
Migrate the databases to Amazon Aurora Serverless (Aurora PostgreSQL).
For the database tier, create an EC2 Auto Scaling group. Create a new database environment and migrate the existing databases.
**Correct answer
Migrate the databases to Amazon Aurora Serverless (Aurora MySQL).**
*Overall explanation*
Amazon Aurora provides automatic scaling for MySQL databases. Amazon Aurora provides built-in security, continuous backups, serverless compute, up to 15 read replicas, automated multi-Region replication, and integrations with other AWS services. Aurora Serverless reduces any effort from operations also to provision any servers to manage the database cluster.
CORRECT: "Migrate the databases to Amazon Aurora Serverless (Aurora MySQL)” is the correct answer (as explained above.)
INCORRECT: "Migrate the databases to Amazon Aurora Serverless (Aurora PostgreSQL)” is incorrect. Although PostgreSQL is an option for Aurora, the database schema would have to be changed to allow PostgreSQL compatibility.
INCORRECT: "Consolidate the databases into a single MySQL database. Use larger EC2 instances for the larger database” is incorrect. Databases run on a larger EC2 instance would not provide improved performance, scaling, and durability.
INCORRECT: "For the database tier, create an EC2 Auto Scaling group. Create a new database environment and migrate the existing databases” is incorrect. This would improve the scalability of the solution but would still have to be heavily managed by the organization, something that would not be needed with Aurora Serverless.
References:
https://aws.amazon.com/rds/aurora/serverless/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/


Question 6Skipped
**There are badge readers located at every entrance of an organization’s warehouses. A message is sent over HTTPS when badges are scanned to indicate who tried to access the entrance.
A solutions architect must design a system to process these messages. A highly available solution is required. The solution must store results in a durable data store for later analysis.**
Which system architecture should the solutions architect recommend?
**Correct answer
Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function.**
Set up an Amazon S3 gateway endpoint in your VPC. Connect the facility network to the VPC via a Site-to-Site VPN connection so that sensor data can be written directly to an S3 bucket.
Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB.
Create an Amazon EC2 instance to serve as the HTTPS endpoint and to process messages. An Amazon S3 bucket should be configured for the EC2 instance to save the results.
*Overall explanation*
Amazon API Gateway would be ideal for providing a secure entry point for your application, and for traffic to be sent via HTTPS. AWS Lambda would integrate seamlessly with API Gateway to process the data, as an event-driven solution like this would be perfect when designing a scalable system based on sporadic use. Finally, DynamoDB is highly scalable and is a perfect repository for data to be stored for future analysis.
CORRECT: "Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function" is the correct answer (as explained above.)
INCORRECT: "Create an Amazon EC2 instance to serve as the HTTPS endpoint and to process messages. An Amazon S3 bucket should be configured for the EC2 instance to save the results" is incorrect. As the action of a badge being read to initiate access to a warehouse should only take a few seconds, spinning up an EC2 instance to serve as a HTTPS endpoint would take minutes, and is not suitable for this use case.
INCORRECT: "Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB” is incorrect. Amazon Route 53 is a managed DNS service, and DNS is not required in this instance as the badge reader does not have a DNS name.
INCORRECT: "Set up an Amazon S3 gateway endpoint in your VPC. Connect the facility network to the VPC via a Site-to-Site VPN connection so that sensor data can be written directly to an S3 bucket" is incorrect. VPC endpoints are designed to facilitate traffic across the AWS backbone network between AWS services and are not used to create connections between external endpoints outside of the AWS network and an Amazon S3 bucket.
References:
https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/


Question 13Skipped
**An application runs on Amazon EC2 instances across multiple Availability Zones. The instances run in an Amazon EC2 Auto Scaling group behind an Application Load Balancer. The application performs best when the CPU utilization of the EC2 instances is at or near 40%.
What should a solutions architect do to maintain the desired performance across all instances in the group?**
**Correct answer
Use a target tracking policy to dynamically scale the Auto Scaling group**
Use an AWS Lambda function to update the desired Auto Scaling group capacity
Use scheduled scaling actions to scale up and scale down the Auto Scaling group
Use a simple scaling policy to dynamically scale the Auto Scaling group
*Overall explanation*
With target tracking scaling policies, you select a scaling metric and set a target value. Amazon EC2 Auto Scaling creates and manages the CloudWatch alarms that trigger the scaling policy and calculates the scaling adjustment based on the metric and the target value.
The scaling policy adds or removes capacity as required to keep the metric at, or close to, the specified target value. In addition to keeping the metric close to the target value, a target tracking scaling policy also adjusts to the changes in the metric due to a changing load pattern.
CORRECT: "Use a target tracking policy to dynamically scale the Auto Scaling group" is the correct answer.
INCORRECT: "Use a simple scaling policy to dynamically scale the Auto Scaling group" is incorrect as target tracking is a better way to keep the aggregate CPU usage at around 40%
INCORRECT: "Use an AWS Lambda function to update the desired Auto Scaling group capacity" is incorrect as this can be done automatically.
INCORRECT: "Use scheduled scaling actions to scale up and scale down the Auto Scaling group" is incorrect as dynamic scaling is required to respond to changes in utilization.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/


Question 35Skipped
**An application makes calls to a REST API running on Amazon EC2 instances behind an Application Load Balancer (ALB). Most API calls complete quickly. However, a single endpoint is making API calls that require much longer to complete and this is introducing overall latency into the system. What steps can a Solutions Architect take to minimize the effects of the long-running API calls?**
Increase the ALB idle timeout to allow the long-running requests to complete
Change the ALB to a Network Load Balancer (NLB) and use SSL/TLS termination
Change the EC2 instance to one with enhanced networking to reduce latency
**Correct answer
Create an Amazon SQS queue and decouple the long-running API calls**
*Overall explanation*
An Amazon Simple Queue Service (SQS) can be used to offload and decouple the long-running requests. They can then be processed asynchronously by separate EC2 instances. This is the best way to reduce the overall latency introduced by the long-running API call.
CORRECT: "Create an Amazon SQS queue and decouple the long-running API calls" is the correct answer.
INCORRECT: "Change the EC2 instance to one with enhanced networking to reduce latency" is incorrect. This will not reduce the latency of the API call as network latency is not the issue here, it is the latency of how long the API call takes to complete.
INCORRECT: "Increase the ALB idle timeout to allow the long-running requests to complete" is incorrect. The issue is not the connection being interrupted, it is that the API call takes a long time to complete.
INCORRECT: "Change the ALB to a Network Load Balancer (NLB) and use SSL/TLS termination" is incorrect. SSL/TLS termination is not of benefit here as the problem is not encryption or processing of encryption. The issue is API call latency.
References:
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/


Question 39Skipped
**Three AWS accounts are owned by the same company but in different regions. Account Z has two AWS Direct Connect connections to two separate company offices. Accounts A and B require the ability to route across account Z’s Direct Connect connections to each company office. A Solutions Architect has created an AWS Direct Connect gateway in account Z.
How can the required connectivity be configured?**
Associate the Direct Connect gateway to a transit gateway in each region
Create a VPC Endpoint to the Direct Connect gateway in account A and B
Create a PrivateLink connection in Account Z and ENIs in accounts A and B
**Correct answer
Associate the Direct Connect gateway to a virtual private gateway in account A and B**
*Overall explanation*
You can associate an AWS Direct Connect gateway with either of the following gateways:
- A transit gateway when you have multiple VPCs in the same Region.
- A virtual private gateway.
In this case account Z owns the Direct Connect gateway so a VPG in accounts A and B must be associated with it to enable this configuration to work. After Account Z accepts the proposals, Account A and Account B can route traffic from their virtual private gateway to the Direct Connect gateway.


CORRECT: "Associate the Direct Connect gateway to a virtual private gateway in account A and B" is the correct answer.
INCORRECT: "Associate the Direct Connect gateway to a transit gateway in each region" is incorrect. This would be a good solution if the accounts were in VPCs within a region rather than across regions.
INCORRECT: "Create a VPC Endpoint to the Direct Connect gateway in account A and B" is incorrect. You cannot create a VPC endpoint for Direct Connect gateways.
INCORRECT: "Create a PrivateLink connection in Account Z and ENIs in accounts A and B" is incorrect. You cannot use PrivateLink connections to publish a Direct Connect gateway.
References:
https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-direct-connect/
