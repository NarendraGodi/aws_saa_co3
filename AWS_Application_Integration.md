Question 1Skipped
Domain
AWS Application Integration
Question 9Skipped
A company is investigating methods to reduce the expenses associated with on-premises backup infrastructure. The Solutions Architect wants to reduce costs by eliminating the use of physical backup tapes. It is a requirement that existing backup applications and workflows should continue to function.
What should the Solutions Architect recommend?
Correct answer
Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL).
Connect the backup applications to an AWS Storage Gateway using the iSCSI protocol.
Create an Amazon EFS file system and connect the backup applications using the iSCSI protocol.
Create an Amazon EFS file system and connect the backup applications using the NFS protocol.
Overall explanation
The AWS Storage Gateway Tape Gateway enables you to replace using physical tapes on premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway emulates physical tape libraries, removes the cost and complexity of managing physical tape infrastructure, and provides more durability than physical tapes.


CORRECT: "Connect the backup applications to an AWS Storage Gateway using an iSCSI-virtual tape library (VTL)" is the correct answer.
INCORRECT: "Create an Amazon EFS file system and connect the backup applications using the NFS protocol" is incorrect. The NFS protocol is used by AWS Storage Gateway File Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
INCORRECT: "Create an Amazon EFS file system and connect the backup applications using the iSCSI protocol" is incorrect. The NFS protocol is used by AWS Storage Gateway File Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
INCORRECT: "Connect the backup applications to an AWS Storage Gateway using the NFS protocol" is incorrect. The iSCSI protocol is used by AWS Storage Gateway Volume Gateways but these do not provide virtual tape functionality that is suitable for replacing the existing backup infrastructure.
References:
https://aws.amazon.com/storagegateway/vtl/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-storage-gateway/
Domain
AWS Application Integration
Question 17Skipped
A developer created an application that uses Amazon EC2 and an Amazon RDS MySQL database instance. The developer stored the database user name and password in a configuration file on the root EBS volume of the EC2 application instance. A Solutions Architect has been asked to design a more secure solution.
What should the Solutions Architect do to achieve this requirement?
Correct answer
Create an IAM role with permission to access the database. Attach this IAM role to the EC2 instance.
Install an Amazon-trusted root certificate on the application instance and use SSL/TLS encrypted connections to the database.
Attach an additional volume to the EC2 instance with encryption enabled. Move the configuration file to the encrypted volume.
Move the configuration file to an Amazon S3 bucket. Create an IAM role with permission to the bucket and attach it to the EC2 instance.
Overall explanation
The key problem here is having plain text credentials stored in a file. Even if you encrypt the volume there is still as security risk as the credentials are loaded by the application and passed to RDS.
The best way to secure this solution is to get rid of the credentials completely by using an IAM role instead. The IAM role can be assigned permissions to the database instance and can be attached to the EC2 instance. The instance will then obtain temporary security credentials from AWS STS which is much more secure.
CORRECT: "Create an IAM role with permission to access the database. Attach this IAM role to the EC2 instance" is the correct answer.
INCORRECT: "Move the configuration file to an Amazon S3 bucket. Create an IAM role with permission to the bucket and attach it to the EC2 instance" is incorrect. This just relocates the file; the contents are still unsecured and must be loaded by the application and passed to RDS. This is an insecure process.
INCORRECT: "Attach an additional volume to the EC2 instance with encryption enabled. Move the configuration file to the encrypted volume" is incorrect. This will only encrypt the file at rest, it still must be read, and the contents passed to RDS which is insecure.
INCORRECT: "Install an Amazon-trusted root certificate on the application instance and use SSL/TLS encrypted connections to the database" is incorrect. The file is still unsecured on the EBS volume so encrypting the credentials in an encrypted channel between the EC2 instance and RDS does not solve all security issues.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Application Integration
Question 31Skipped
A company operates a multi-tier application with its backend services deployed on Amazon EC2 instances in a VPC. The backend services must communicate securely with APIs of a third-party SaaS provider that is also hosted on AWS. The company wants to ensure that this communication occurs privately and minimizes exposure to the public internet.
Which solution will meet these requirements?
Correct answer
Configure AWS PrivateLink to create a private connection between the VPC and the third-party SaaS provider's APIs.
Deploy a NAT gateway in the VPC to enable secure outbound communication with the third-party SaaS provider.
Set up an AWS Direct Connect connection between the VPC and the third-party SaaS provider to establish private communication.
Use an AWS VPN connection to establish a secure tunnel between the VPC and the third-party SaaS provider's infrastructure.
Overall explanation
Configure AWS PrivateLink to create a private connection between the VPC and the third-party SaaS provider's APIs: This is correct because AWS PrivateLink enables private connectivity between VPCs and supported AWS or third-party services, ensuring that traffic does not traverse the public internet.
Set up an AWS Direct Connect connection between the VPC and the third-party SaaS provider to establish private communication: This is incorrect because AWS Direct Connect is used for establishing private connections between on-premises environments and AWS, not for connecting to third-party SaaS providers within AWS.
Deploy a NAT gateway in the VPC to enable secure outbound communication with the third-party SaaS provider: This is incorrect because a NAT gateway facilitates outbound internet access for resources in private subnets but does not ensure private communication with third-party services.
Use an AWS VPN connection to establish a secure tunnel between the VPC and the third-party SaaS provider's infrastructure: This is incorrect because VPN connections are typically used for secure communication between on-premises environments and AWS, not for private connectivity to SaaS providers hosted on AWS.
References:
https://docs.aws.amazon.com/privatelink/latest/userguide/what-is-privatelink.html
https://aws.amazon.com/privatelink/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Application Integration
Question 40Skipped
A web application allows users to upload photos and add graphical elements to them. The application offers two tiers of service: free and paid. Photos uploaded by paid users should be processed before those submitted using the free tier. The photos are uploaded to an Amazon S3 bucket which uses an event notification to send the job information to Amazon SQS.
How should a Solutions Architect configure the Amazon SQS deployment to meet these requirements?
Use one SQS standard queue. Use batching for the paid photos and short polling for the free photos.
Use one SQS FIFO queue. Assign a higher priority to the paid photos so they are processed first.
Correct answer
Use a separate SQS Standard queue for each tier. Configure Amazon EC2 instances to prioritize polling for the paid queue over the free queue.
Use a separate SQS FIFO queue for each tier. Set the free queue to use short polling and the paid queue to use long polling.
Overall explanation
AWS recommend using separate queues when you need to provide prioritization of work. The logic can then be implemented at the application layer to prioritize the queue for the paid photos over the queue for the free photos.
CORRECT: "Use a separate SQS Standard queue for each tier. Configure Amazon EC2 instances to prioritize polling for the paid queue over the free queue" is the correct answer.
INCORRECT: "Use one SQS FIFO queue. Assign a higher priority to the paid photos so they are processed first" is incorrect. FIFO queues preserve the order of messages but they do not prioritize messages within the queue. The orders would need to be placed into the queue in a priority order and there’s no way of doing this as the messages are sent automatically through event notifications as they are received by Amazon S3.
INCORRECT: "Use one SQS standard queue. Use batching for the paid photos and short polling for the free photos" is incorrect. Batching adds efficiency but it has nothing to do with ordering or priority.
INCORRECT: "Use a separate SQS FIFO queue for each tier. Set the free queue to use short polling and the paid queue to use long polling" is incorrect. Short polling and long polling are used to control the amount of time the consumer process waits before closing the API call and trying again. Polling should be configured for efficiency of API calls and processing of messages but does not help with message prioritization.
References:
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-how-it-works.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Application Integration
Question 41Skipped
Amazon EC2 instances in an Auto Scaling group. The application stores temporary training data on attached Amazon Elastic Block Store (Amazon EBS) volumes. The company seeks recommendations to optimize costs for the EC2 instances, the Auto Scaling group, and the EBS volumes with minimal manual intervention.
Which solution will meet these requirements with the MOST operational efficiency?
Use AWS Cost and Usage Reports to export data to Amazon Athena. Query the data to identify inefficiencies in the EC2 instances, the Auto Scaling group, and the EBS volumes.
Set up Amazon CloudWatch billing alerts and manually analyze metrics to identify cost-saving opportunities for the EC2 instances, the Auto Scaling group, and the EBS volumes.
Use AWS Compute Optimizer for recommendations on EC2 instances and Auto Scaling groups. Use Amazon Data Lifecycle Manager to evaluate cost optimizations for the EBS volumes.
Correct answer
Configure AWS Compute Optimizer to provide cost optimization recommendations for the EC2 instances, the Auto Scaling group, and the EBS volumes.
Overall explanation
Configure AWS Compute Optimizer to provide cost optimization recommendations for the EC2 instances, the Auto Scaling group, and the EBS volumes: This is correct because AWS Compute Optimizer offers actionable insights for cost optimization across EC2 instances, Auto Scaling groups, and EBS volumes with minimal operational overhead.
Set up Amazon CloudWatch billing alerts and manually analyze metrics to identify cost-saving opportunities for the EC2 instances, the Auto Scaling group, and the EBS volumes: This option requires significant manual intervention, which reduces operational efficiency.
Use AWS Cost and Usage Reports to export data to Amazon Athena. Query the data to identify inefficiencies in the EC2 instances, the Auto Scaling group, and the EBS volumes: While this approach provides insights, it requires significant manual effort to analyze the data.
Use AWS Compute Optimizer for recommendations on EC2 instances and Auto Scaling groups. Use Amazon Data Lifecycle Manager to evaluate cost optimizations for the EBS volumes: This requires separate configurations for different resources, increasing complexity compared to a single AWS Compute Optimizer setup.
References:
https://docs.aws.amazon.com/compute-optimizer/latest/ug/what-is.html
https://docs.aws.amazon.com/AmazonEBS/latest/dg/ebs-automatic-snapshot-policy.html
Domain
AWS Application Integration
Question 45Skipped
A company has deployed a new website on Amazon EC2 instances behind an Application Load Balancer (ALB). Amazon Route 53 is used for the DNS service. The company has asked a Solutions Architect to create a backup website with support contact details that users will be directed to automatically if the primary website is down.
How should the Solutions Architect deploy this solution cost-effectively?
Configure a static website using Amazon S3 and create a Route 53 weighted routing policy.
Correct answer
Configure a static website using Amazon S3 and create a Route 53 failover routing policy.
Create the backup website on EC2 and ALB in another Region and create an AWS Global Accelerator endpoint.
Deploy the backup website on EC2 and ALB in another Region and use Route 53 health checks for failover routing.
Overall explanation
The most cost-effective solution is to create a static website using an Amazon S3 bucket and then use a failover routing policy in Amazon Route 53. With a failover routing policy users will be directed to the main website as long as it is responding to health checks successfully.
If the main website fails to respond to health checks (its down), Route 53 will begin to direct users to the backup website running on the Amazon S3 bucket. It’s important to set the TTL on the Route 53 records appropriately to ensure that users resolve the failover address within a short time.
CORRECT: "Configure a static website using Amazon S3 and create a Route 53 failover routing policy" is the correct answer.
INCORRECT: "Configure a static website using Amazon S3 and create a Route 53 weighted routing policy" is incorrect. Weighted routing is used when you want to send a percentage of traffic between multiple endpoints. In this case all traffic should go to the primary until if fails, then all should go to the backup.
INCORRECT: "Deploy the backup website on EC2 and ALB in another Region and use Route 53 health checks for failover routing" is incorrect. This is not a cost-effective solution for the backup website. It can be implemented using Route 53 failover routing which uses health checks but would be an expensive option.
INCORRECT: "Create the backup website on EC2 and ALB in another Region and create an AWS Global Accelerator endpoint" is incorrect. Global Accelerator is used for performance as it directs traffic to the nearest healthy endpoint. It is not useful for failover in this scenario and is also a very expensive solution.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-configuring.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
https://digitalcloud.training/amazon-route-53/
Domain
AWS Application Integration
Question 62Skipped
An eCommerce company runs an application on Amazon EC2 instances in public and private subnets. The web application runs in a public subnet and the database runs in a private subnet. Both the public and private subnets are in a single Availability Zone.
Which combination of steps should a solutions architect take to provide high availability for this architecture? (Select TWO.)
Create an EC2 Auto Scaling group in the public subnet and use an Application Load Balancer.
Create new public and private subnets in a different AZ. Create a database using Amazon EC2 in one AZ.
Correct selection
Create an EC2 Auto Scaling group and Application Load Balancer that spans across multiple AZs.
Create new public and private subnets in the same AZ but in a different Amazon VPC.
Correct selection
Create new public and private subnets in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment.
Overall explanation
High availability can be achieved by using multiple Availability Zones within the same VPC. An EC2 Auto Scaling group can then be used to launch web application instances in multiple public subnets across multiple AZs and an ALB can be used to distribute incoming load.
The database solution can be made highly available by migrating from EC2 to Amazon RDS and using a Multi-AZ deployment model. This will provide the ability to failover to another AZ in the event of a failure of the primary database or the AZ in which it runs.
CORRECT: "Create an EC2 Auto Scaling group and Application Load Balancer that spans across multiple AZs" is a correct answer.
CORRECT: "Create new public and private subnets in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment" is also a correct answer.
INCORRECT: "Create new public and private subnets in the same AZ but in a different Amazon VPC" is incorrect. You cannot use multiple VPCs for this solution as it would be difficult to manage and direct traffic (you can’t load balance across VPCs).
INCORRECT: "Create an EC2 Auto Scaling group in the public subnet and use an Application Load Balancer" is incorrect. This does not achieve HA as you need multiple public subnets across multiple AZs.
INCORRECT: "Create new public and private subnets in a different AZ. Create a database using Amazon EC2 in one AZ" is incorrect. The database solution is not HA in this answer option.
References:
https://aws.amazon.com/ec2/autoscaling/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
https://digitalcloud.training/amazon-rds/
Domain
AWS Application Integration
Question 63Skipped
A company runs workloads in the AWS Cloud and wants to consolidate and analyze security-related information to enhance workload protection. The company needs a solution that simplifies the collection and centralization of security data across multiple AWS accounts and Regions with minimal development effort.
Which solution will meet these requirements with the LEAST development effort?
Deploy an Amazon RDS cluster and use AWS Database Migration Service (AWS DMS) to load security data from multiple sources.
Correct answer
Configure Amazon Security Lake to automatically collect, normalize, and store security data in Amazon S3 for analysis.
Use AWS Glue crawlers to extract and catalog security data into an AWS Lake Formation-managed data lake.
Create a custom Lambda function to fetch security data in JSON format and store it in Amazon S3 for further analysis.
Overall explanation
Configure Amazon Security Lake to automatically collect, normalize, and store security data in Amazon S3 for analysis: This is the best solution because Amazon Security Lake is purpose-built for centralizing security data. It minimizes development effort by automatically collecting and formatting data into the Open Cybersecurity Schema Framework (OCSF) for analysis.
Use AWS Glue crawlers to extract and catalog security data into an AWS Lake Formation-managed data lake: While this approach helps create a centralized data lake, it requires more development effort to set up the data ingestion pipelines and manage the schema.
Deploy an Amazon RDS cluster and use AWS Database Migration Service (AWS DMS) to load security data from multiple sources: This is incorrect because DMS is not designed for collecting and normalizing security data. Setting up RDS for this use case introduces unnecessary complexity.
Create a custom Lambda function to fetch security data in JSON format and store it in Amazon S3 for further analysis: While possible, this solution requires custom development and ongoing maintenance, making it less efficient than using a managed service like Amazon Security Lake.
References:
https://aws.amazon.com/security-lake
https://docs.aws.amazon.com/security-lake/latest/userguide/what-is-security-lake.html
Domain
AWS Application Integration
Question 26Skipped
A media streaming company stores user activity logs in an Amazon S3 bucket. The logs are accessed frequently for real-time analytics and reporting. The company enforces strict encryption requirements for data stored in S3 and currently uses AWS Key Management Service (AWS KMS) for encryption.
The company wants to reduce costs related to encrypting objects in the S3 bucket while maintaining compliance with its encryption requirements and minimizing the number of AWS KMS calls.
Which solution will meet these requirements?
Use server-side encryption with customer-provided encryption keys (SSE-C) and store the keys in AWS Secrets Manager.
Use server-side encryption with Amazon S3 managed keys (SSE-S3) to eliminate AWS KMS usage.
Correct answer
Enable S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the objects to reduce the cost of KMS requests.
Use client-side encryption with AWS KMS customer-managed keys to encrypt the data before uploading it to S3.
Overall explanation
Enable S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the objects to reduce the cost of KMS requests: This is correct because enabling S3 Bucket Key reduces the number of AWS KMS calls required for object encryption. S3 Bucket Key caches the encryption keys at the bucket level, significantly lowering the cost of encryption for frequently accessed objects while meeting encryption requirements.
Use server-side encryption with Amazon S3 managed keys (SSE-S3) to eliminate AWS KMS usage: This is incorrect because SSE-S3 does not use AWS KMS, but it does not meet the strict encryption requirements specified by the company, which mandate the use of AWS KMS.
Use client-side encryption with AWS KMS customer-managed keys to encrypt the data before uploading it to S3: This is incorrect because client-side encryption increases operational complexity and does not optimize costs associated with AWS KMS calls.
Use server-side encryption with customer-provided encryption keys (SSE-C) and store the keys in AWS Secrets Manager: This is incorrect because SSE-C requires the company to manage its own encryption keys, introducing operational overhead. Additionally, this approach does not optimize costs related to AWS KMS.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-key.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-kms/
Domain
AWS Application Integration
Question 28Skipped
A shared services VPC is being setup for use by several AWS accounts. An application needs to be securely shared from the shared services VPC. The solution should not allow consumers to connect to other instances in the VPC.
How can this be setup with the least administrative effort? (Select TWO.)
Correct selection
Create a Network Load Balancer (NLB)
Configure security groups to restrict access
Use AWS ClassicLink to expose the application as an endpoint service
Setup VPC peering between each AWS VPC
Correct selection
Use AWS PrivateLink to expose the application as an endpoint service
Overall explanation
VPCs can be shared among multiple AWS accounts. Resources can then be shared amongst those accounts. However, to restrict access so that consumers cannot connect to other instances in the VPC the best solution is to use PrivateLink to create an endpoint for the application. The endpoint type will be an interface endpoint and it uses an NLB in the shared services VPC.

CORRECT: "Create a Network Load Balancer (NLB)" is a correct answer.
CORRECT: "Use AWS PrivateLink to expose the application as an endpoint service" is also a correct answer.
INCORRECT: "Use AWS ClassicLink to expose the application as an endpoint service" is incorrect. ClassicLink allows you to link EC2-Classic instances to a VPC in your account, within the same region. This solution does not include EC2-Classic which is now deprecated (replaced by VPC).
INCORRECT: "Setup VPC peering between each AWS VPC" is incorrect. VPC peering could be used along with security groups to restrict access to the application and other instances in the VPC. However, this would be administratively difficult as you would need to ensure that you maintain the security groups as resources and addresses change.
INCORRECT: "Configure security groups to restrict access" is incorrect. This could be used in conjunction with VPC peering but better method is to use PrivateLink for this use case.
References:
https://aws.amazon.com/about-aws/whats-new/2018/12/amazon-virtual-private-clouds-can-now-be-shared-with-other-aws-accounts/
https://aws.amazon.com/blogs/networking-and-content-delivery/vpc-sharing-a-new-approach-to-multiple-accounts-and-vpc-management/
https://d1.awsstatic.com/whitepapers/aws-privatelink.pdf
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
Domain
AWS Application Integration
Question 33Skipped
A healthcare startup is building a cloud-based patient management system on AWS. The system processes sensitive health data and uses Amazon RDS for the database, Amazon S3 for storing medical reports, and AWS Lambda for processing event-driven workflows triggered by S3 Event Notifications.
The startup uses AWS IAM Identity Center to manage user authentication. The development, testing, and operations teams need secure access to RDS and S3 while ensuring compliance with healthcare regulations that mandate least privilege access and centralized access control.
Which solution meets these requirements with the LEAST operational overhead?
Configure an Amazon Cognito user pool to authenticate team members. Use a custom Lambda function to generate temporary credentials for RDS and S3 access. Implement role-based access controls within the Lambda function to enforce least privilege.
Use AWS Organizations to create separate accounts for development, testing, and operations teams. Apply Service Control Policies (SCPs) to restrict access at the account level. Use cross-account IAM roles to grant granular permissions for RDS and S3 based on team needs.
Correct answer
Use AWS IAM Identity Center integrated with the startup's existing Active Directory. Create permission sets with fine-grained permissions for RDS and S3. Assign team members to appropriate groups in Active Directory, which map to Identity Center permission sets.
Create separate IAM users for all team members. Assign each user predefined managed policies with RDS and S3 permissions. Use IAM Access Analyzer to review permissions periodically to ensure compliance with least privilege principles.
Overall explanation
Use AWS IAM Identity Center integrated with the startup's existing Active Directory. Create permission sets with fine-grained permissions for RDS and S3. Assign team members to appropriate groups in Active Directory, which map to Identity Center permission sets: This is correct because IAM Identity Center enables centralized user management and integrates seamlessly with Active Directory. It allows the creation of permission sets that enforce least privilege while minimizing operational overhead by using existing group structures.
Configure an Amazon Cognito user pool to authenticate team members. Use a custom Lambda function to generate temporary credentials for RDS and S3 access. Implement role-based access controls within the Lambda function to enforce least privilege: This is incorrect because Cognito is primarily designed for managing end-user authentication, not for managing internal team access to AWS resources. Using Cognito and a custom Lambda function would add unnecessary complexity and operational overhead.
Create separate IAM users for all team members. Assign each user predefined managed policies with RDS and S3 permissions. Use IAM Access Analyzer to review permissions periodically to ensure compliance with least privilege principles: This is incorrect because managing individual IAM users introduces significant administrative overhead. IAM Identity Center is a more scalable and centralized solution.
Use AWS Organizations to create separate accounts for development, testing, and operations teams. Apply Service Control Policies (SCPs) to restrict access at the account level. Use cross-account IAM roles to grant granular permissions for RDS and S3 based on team needs: This is incorrect because creating separate accounts and managing cross-account IAM roles adds unnecessary complexity. IAM Identity Center provides a more efficient solution for centralized access control within a single account.
References:
https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html
https://aws.amazon.com/cognito/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Application Integration
Question 3Skipped
An automotive company plans to implement IoT sensors in manufacturing equipment that will send data to AWS in real time. The solution must receive events in an ordered manner from each asset and ensure that the data is saved for future processing.
Which solution would be MOST efficient?
Use an Amazon SQS FIFO queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function for the SQS queue to save data to Amazon EFS.
Correct answer
Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3.
Use an Amazon SQS standard queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function from the SQS queue to save data to Amazon S3.
Use Amazon Kinesis Data Streams for real-time events with a shard for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon EBS.
Overall explanation
Amazon Kinesis Data Streams is the ideal service for receiving streaming data. The Amazon Kinesis Client Library (KCL) delivers all records for a given partition key to the same record processor, making it easier to build multiple applications reading from the same Amazon Kinesis data stream. Therefore, a separate partition (rather than shard) should be used for each equipment asset.
Amazon Kinesis Firehose can be used to receive streaming data from Data Streams and then load the data into Amazon S3 for future processing.
CORRECT: "Use Amazon Kinesis Data Streams for real-time events with a partition for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon S3" is the correct answer.
INCORRECT: "Use Amazon Kinesis Data Streams for real-time events with a shard for each equipment asset. Use Amazon Kinesis Data Firehose to save data to Amazon EBS" is incorrect. A partition should be used rather than a shard as explained above.
INCORRECT: "Use an Amazon SQS FIFO queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function for the SQS queue to save data to Amazon EFS" is incorrect. Amazon SQS cannot be used for real-time use cases.
INCORRECT: "Use an Amazon SQS standard queue for real-time events with one queue for each equipment asset. Trigger an AWS Lambda function from the SQS queue to save data to Amazon S3" is incorrect. Amazon SQS cannot be used for real-time use cases.
References:
https://aws.amazon.com/kinesis/data-streams/faqs/
https://aws.amazon.com/kinesis/data-firehose/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-kinesis/
Domain
AWS Application Integration
Question 4Skipped
A company hosts an application on Amazon EC2 instances behind Application Load Balancers in several AWS Regions. Distribution rights for the content require that users in different geographies must be served content from specific regions.
Which configuration meets these requirements?
Configure Application Load Balancers with multi-Region routing.
Configure Amazon CloudFront with multiple origins and AWS WAF.
Create Amazon Route 53 records with a geoproximity routing policy.
Correct answer
Create Amazon Route 53 records with a geolocation routing policy.
Overall explanation
To protect the distribution rights of the content and ensure that users are directed to the appropriate AWS Region based on the location of the user, the geolocation routing policy can be used with Amazon Route 53.
Geolocation routing lets you choose the resources that serve your traffic based on the geographic location of your users, meaning the location that DNS queries originate from.
When you use geolocation routing, you can localize your content and present some or all of your website in the language of your users. You can also use geolocation routing to restrict distribution of content to only the locations in which you have distribution rights.
CORRECT: "Create Amazon Route 53 records with a geolocation routing policy" is the correct answer.
INCORRECT: "Create Amazon Route 53 records with a geoproximity routing policy" is incorrect. Use this routing policy when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another.
INCORRECT: "Configure Amazon CloudFront with multiple origins and AWS WAF" is incorrect. AWS WAF protects against web exploits but will not assist with directing users to different content (from different origins).
INCORRECT: "Configure Application Load Balancers with multi-Region routing" is incorrect. There is no such thing as multi-Region routing for ALBs.
References:
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-route-53/
Domain
AWS Application Integration
Question 9Skipped
A financial institution with many departments wants to migrate to the AWS Cloud from their data center. Each department should have their own established AWS accounts with preconfigured, Limited access to authorized services, based on each team's needs, by the principle of least privilege.
What actions should be taken to ensure compliance with these security requirements?
Correct answer
Deploy a Landing Zone within AWS Control Tower. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions on the created accounts.
Configure AWS Organizations with SCPs and create new member accounts. Use AWS CloudFormation templates to configure the member account networking.
Deploy a Landing Zone within AWS Organizations. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions on the created accounts.
Use AWS CloudFormation to create new member accounts and networking and use IAM roles to allow access to approved AWS services.
Overall explanation
AWS Control Tower automates the setup of a new landing zone using best practices blueprints for identity, federated access, and account structure.
The account factory automates provisioning of new accounts in your organization. As a configurable account template, it helps you standardize the provisioning of new accounts with pre-approved account configurations. You can configure your account factory with pre-approved network configuration and region selections.
CORRECT: "Deploy a Landing Zone within AWS Control Tower. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions on the created accounts” is the correct answer (as explained above.)
INCORRECT: "Use AWS CloudFormation to create new member accounts and networking and use IAM roles to allow access to approved AWS services” is incorrect. Although you could perhaps make new AWS Accounts with AWS CloudFormation, the easiest way to do that is by using AWS Control Tower.
INCORRECT: "Configure AWS Organizations with SCPs and create new member accounts. Use AWS CloudFormation templates to configure the member account networking” is incorrect. You can make new accounts using AWS Organizations however the easiest way to do this is by using the AWS Control Tower service.
INCORRECT: "Deploy a Landing Zone within AWS Organizations. Allow department administrators to use the Landing Zone to create new member accounts and networking. Grant the department's AWS power user permissions on the created accounts” is incorrect. Landing Zones do not get deployed within AWS Organizations.
References:
https://aws.amazon.com/controltower/
Domain
AWS Application Integration
Question 11Skipped
A company's application is running on Amazon EC2 instances in a single Region. In the event of a disaster, a solutions architect needs to ensure that the resources can also be deployed to a second Region.
Which combination of actions should the solutions architect take to accomplish this? (Select TWO.)
Detach a volume on an EC2 instance and copy it to an Amazon S3 bucket in the second Region
Correct selection
Copy an Amazon Machine Image (AMI) of an EC2 instance and specify the second Region for the destination
Copy an Amazon Elastic Block Store (Amazon EBS) volume from Amazon S3 and launch an EC2 instance in the second Region using that EBS volume
Launch a new EC2 instance in the second Region and copy a volume from Amazon S3 to the new instance
Correct selection
Launch a new EC2 instance from an Amazon Machine Image (AMI) in the second Region
Overall explanation
You can copy an Amazon Machine Image (AMI) within or across AWS Regions using the AWS Management Console, the AWS Command Line Interface or SDKs, or the Amazon EC2 API, all of which support the CopyImage action.
Using the copied AMI the solutions architect would then be able to launch an instance from the same EBS volume in the second Region.
Note: the AMIs are stored on Amazon S3, however you cannot view them in the S3 management console or work with them programmatically using the S3 API.
CORRECT: "Copy an Amazon Machine Image (AMI) of an EC2 instance and specify the second Region for the destination" is a correct answer.
CORRECT: "Launch a new EC2 instance from an Amazon Machine Image (AMI) in the second Region" is also a correct answer.
INCORRECT: "Detach a volume on an EC2 instance and copy it to an Amazon S3 bucket in the second Region" is incorrect. You cannot copy EBS volumes directly from EBS to Amazon S3.
INCORRECT: "Launch a new EC2 instance in the second Region and copy a volume from Amazon S3 to the new instance" is incorrect. You cannot create an EBS volume directly from Amazon S3.
INCORRECT: "Copy an Amazon Elastic Block Store (Amazon EBS) volume from Amazon S3 and launch an EC2 instance in the second Region using that EBS volume" is incorrect. You cannot create an EBS volume directly from Amazon S3.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
Domain
AWS Application Integration
Question 14Skipped
A Solutions Architect is migrating a distributed application from their on-premises environment into AWS. This application consists of an Apache Cassandra NoSQL database, with a containerized SUSE Linux compute layer with an additional storage layer made up of multiple Microsoft SQL Server databases. Once in the cloud the company wants to have as little operational overhead as possible, with no schema conversion during the migration and the company wants to host the architecture in a highly available and durable way.

Which of the following groups of services will provide the solutions architect with the best solution ?
Correct answer
Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.
Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.
Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on EC2. Use Amazon RDS for Microsoft SQL Server to host the second storage layer.
Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon Aurora to host the second storage layer.
Overall explanation
Amazon Keyspaces (for Apache Cassandra) is a scalable, highly available, and managed Apache Cassandra–compatible database service. This combined with a containerized, serverless compute layer on Amazon ECS for Fargate and a RDS for Microsoft SQL Server database layer is a fully managed version of what currently exists on premises.
CORRECT: "Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer” is the correct answer (as explained above.)
INCORRECT: "Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on EC2. Use Amazon RDS for Microsoft SQL Server to host the second storage layer” is incorrect. DynamoDB is not a managed version of DynamoDB therefore it is not the correct answer.
INCORRECT: "Run the NoSQL database on DynamoDB, and the compute layer on Amazon ECS on Fargate. Use Amazon RDS for Microsoft SQL Server to host the second storage layer” is incorrect. DynamoDB is not a managed version of DynamoDB therefore it is not the correct answer.
INCORRECT: "Run the NoSQL database on Amazon Keyspaces, and the compute layer on Amazon ECS on Fargate. Use Amazon Aurora to host the second storage layer” is incorrect. Amazon Aurora does not have an option to run a Microsoft SQL Server database, therefore this answer is not correct.
References:
https://aws.amazon.com/keyspaces/
Save time with our AWS cheat sheets:
https://digitalcloud.training/category/aws-cheat-sheets/aws-database/
Domain
AWS Application Integration
Question 17Skipped
A telecommunications company is looking to expand its 5G coverage nationwide, and as a result needs to provision and build their own private cellular network with the help of AWS.
Which solution does AWS provide to help with this?
AWS CloudHSM
AWS Wavelength
AWS Outposts
Correct answer
AWS Private 5G
Overall explanation
AWS Private 5G is a managed service that makes it easy to deploy, operate, and scale your own private cellular network, with all required hardware and software provided by AWS.

CORRECT: "AWS Private 5G" is the correct answer (as explained above.)
INCORRECT: "AWS Wavelength" is incorrect. AWS Wavelength embeds AWS compute and storage services within 5G networks, providing mobile edge computing infrastructure for developing, deploying, and scaling ultra-low-latency applications.
INCORRECT: "AWS CloudHSM" is incorrect. AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your own encryption keys on the AWS Cloud and has nothing to do with 5G.
INCORRECT: "AWS Outposts" is incorrect. AWS Outposts is a family of fully managed solutions delivering AWS infrastructure and services to virtually any on-premises or edge location for a truly consistent hybrid experience. It is not related to 5G.
References:
https://aws.amazon.com/private5g/
Domain
AWS Application Integration
Question 20Skipped
A company requires a solution to allow customers to customize images that are stored in an online catalog. The image customization parameters will be sent in requests to Amazon API Gateway. The customized image will then be generated on-demand and can be accessed online.
The solutions architect requires a highly available solution. Which solution will be MOST cost-effective?
Use Amazon EC2 instances to manipulate the original images into the requested customization. Store the original and manipulated images in Amazon S3. Configure an Elastic Load Balancer in front of the EC2 instances
Use Amazon EC2 instances to manipulate the original images into the requested customization. Store the original images in Amazon S3 and the manipulated images in Amazon DynamoDB. Configure an Amazon CloudFront distribution with the S3 bucket as the origin
Correct answer
Use AWS Lambda to manipulate the original images to the requested customization. Store the original and manipulated images in Amazon S3. Configure an Amazon CloudFront distribution with the S3 bucket as the origin
Use AWS Lambda to manipulate the original images to the requested customization. Store the original images in Amazon S3 and the manipulated images in Amazon DynamoDB. Configure an Elastic Load Balancer in front of the Amazon EC2 instances
Overall explanation
All solutions presented are highly available. The key requirement that must be satisfied is that the solution should be cost-effective and you must choose the most cost-effective option.
Therefore, it’s best to eliminate services such as Amazon EC2 and ELB as these require ongoing costs even when they’re not used. Instead, a fully serverless solution should be used. AWS Lambda, Amazon S3 and CloudFront are the best services to use for these requirements.
CORRECT: "Use AWS Lambda to manipulate the original images to the requested customization. Store the original and manipulated images in Amazon S3. Configure an Amazon CloudFront distribution with the S3 bucket as the origin" is the correct answer.
INCORRECT: "Use Amazon EC2 instances to manipulate the original images into the requested customization. Store the original and manipulated images in Amazon S3. Configure an Elastic Load Balancer in front of the EC2 instances" is incorrect. This is not the most cost-effective option as the ELB and EC2 instances will incur costs even when not used.
INCORRECT: "Use AWS Lambda to manipulate the original images to the requested customization. Store the original images in Amazon S3 and the manipulated images in Amazon DynamoDB. Configure an Elastic Load Balancer in front of the Amazon EC2 instances" is incorrect. This is not the most cost-effective option as the ELB will incur costs even when not used. Also, Amazon DynamoDB will incur RCU/WCUs when running and is not the best choice for storing images.
INCORRECT: "Use Amazon EC2 instances to manipulate the original images into the requested customization. Store the original images in Amazon S3 and the manipulated images in Amazon DynamoDB. Configure an Amazon CloudFront distribution with the S3 bucket as the origin" is incorrect. This is not the most cost-effective option as the EC2 instances will incur costs even when not used
References:
https://aws.amazon.com/serverless/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
https://digitalcloud.training/aws-lambda/
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Application Integration
Question 22Skipped
A company plans to make an Amazon EC2 Linux instance unavailable outside of business hours to save costs. The instance is backed by an Amazon EBS volume. There is a requirement that the contents of the instance’s memory must be preserved when it is made unavailable.
How can a solutions architect meet these requirements?
Use Auto Scaling to scale down the instance outside of business hours. Scale up the instance when required.
Correct answer
Hibernate the instance outside business hours. Start the instance again when required.
Terminate the instance outside business hours. Recover the instance again when required.
Stop the instance outside business hours. Start the instance again when required.
Overall explanation
When you hibernate an instance, Amazon EC2 signals the operating system to perform hibernation (suspend-to-disk). Hibernation saves the contents from the instance memory (RAM) to your Amazon Elastic Block Store (Amazon EBS) root volume. Amazon EC2 persists the instance's EBS root volume and any attached EBS data volumes. When you start your instance:
The EBS root volume is restored to its previous state
The RAM contents are reloaded
The processes that were previously running on the instance are resumed
Previously attached data volumes are reattached and the instance retains its instance ID
CORRECT: "Hibernate the instance outside business hours. Start the instance again when required" is the correct answer.
INCORRECT: "Stop the instance outside business hours. Start the instance again when required" is incorrect. When an instance is stopped the operating system is shut down and the contents of memory will be lost.
INCORRECT: "Use Auto Scaling to scale down the instance outside of business hours. Scale out the instance when required" is incorrect. Auto Scaling scales does not scale up and down, it scales in by terminating instances and out by launching instances. When scaling out new instances are launched and no state will be available from terminated instances.
INCORRECT: "Terminate the instance outside business hours. Recover the instance again when required" is incorrect. You cannot recover terminated instances, you can recover instances that have become impaired in some circumstances.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Application Integration
Question 40Skipped
A website runs on Amazon EC2 instances in an Auto Scaling group behind an Application Load Balancer (ALB) which serves as an origin for an Amazon CloudFront distribution. An AWS WAF is being used to protect against SQL injection attacks. A review of security logs revealed an external malicious IP that needs to be blocked from accessing the website.
What should a solutions architect do to protect the application?
Correct answer
Modify the configuration of AWS WAF to add an IP match condition to block the malicious IP address
Modify the network ACL on the CloudFront distribution to add a deny rule for the malicious IP address
Modify the security groups for the EC2 instances in the target groups behind the ALB to deny the malicious IP address
Modify the network ACL for the EC2 instances in the target groups behind the ALB to deny the malicious IP address
Overall explanation
A new version of the AWS Web Application Firewall was released in November 2019. With AWS WAF classic you create “IP match conditions”, whereas with AWS WAF (new version) you create “IP set match statements”. Look out for wording on the exam.
The IP match condition / IP set match statement inspects the IP address of a web request's origin against a set of IP addresses and address ranges. Use this to allow or block web requests based on the IP addresses that the requests originate from.
AWS WAF supports all IPv4 and IPv6 address ranges. An IP set can hold up to 10,000 IP addresses or IP address ranges to check.
CORRECT: "Modify the configuration of AWS WAF to add an IP match condition to block the malicious IP address" is the correct answer.
INCORRECT: "Modify the network ACL on the CloudFront distribution to add a deny rule for the malicious IP address" is incorrect as CloudFront does not sit within a subnet so network ACLs do not apply to it.
INCORRECT: "Modify the network ACL for the EC2 instances in the target groups behind the ALB to deny the malicious IP address" is incorrect as the source IP addresses of the data in the EC2 instances’ subnets will be the ELB IP addresses.
INCORRECT: "Modify the security groups for the EC2 instances in the target groups behind the ALB to deny the malicious IP address." is incorrect as you cannot create deny rules with security groups.
References:
https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-ipset-match.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-waf-shield/
Domain
AWS Application Integration
Question 64Skipped
Amazon EC2 instances in a development environment run between 9am and 5pm Monday-Friday. Production instances run 24/7. Which pricing models should be used to optimize cost and ensure capacity is available? (Select TWO.)
Use On-Demand instances for the production environment
Use Spot instances for the development environment
Use Reserved instances for the development environment
Correct selection
Use Reserved instances for the production environment
Correct selection
On-demand capacity reservations for the development environment
Overall explanation
Capacity reservations have no commitment and can be created and canceled as needed. This is ideal for the development environment as it will ensure the capacity is available. There is no price advantage but none of the other options provide a price advantage whilst also ensuring capacity is available
Reserved instances are a good choice for workloads that run continuously. This is a good option for the production environment.
CORRECT: "On-demand capacity reservations for the development environment" is a correct answer.
CORRECT: "Use Reserved instances for the production environment" is also a correct answer.
INCORRECT: "Use Spot instances for the development environment" is incorrect. Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted. Spot instances are not suitable for the development environment as important work may be interrupted.
INCORRECT: "Use Reserved instances for the development environment" is incorrect as they require a long-term commitment which is not ideal for a development environment.
INCORRECT: "Use On-Demand instances for the production environment" is incorrect. There is no long-term commitment required when you purchase On-Demand Instances. However, you do not get any discount and therefore this is the most expensive option.
References:
https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/instance-purchasing-options.html
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Application Integration
Question 50Skipped
A large quantity of data is stored on a NAS device on-premises and accessed using the SMB protocol. The company require a managed service for hosting the filesystem and a tool to automate the migration.
Which actions should a Solutions Architect take?
Migrate the data to Amazon EFS using the AWS Server Migration Service (SMS)
Correct answer
Migrate the data to Amazon FSx for Windows File Server using AWS DataSync
Migrate the data to Amazon S3 using and AWS Snowball Edge device
Migrate the data to Amazon FSx for Lustre using AWS DataSync
Overall explanation
Amazon FSx for Windows File Server provides fully managed, highly reliable, and scalable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol. This is the most suitable destination for this use case.
AWS DataSync can be used to move large amounts of data online between on-premises storage and Amazon S3, Amazon EFS, or Amazon FSx for Windows File Server. The source datastore can be Server Message Block (SMB) file servers.


CORRECT: "Migrate the data to Amazon FSx for Windows File Server using AWS DataSync" is the correct answer.
INCORRECT: "Migrate the data to Amazon EFS using the AWS Server Migration Service (SMS)" is incorrect. EFS is used for hosting filesystems accessed over NFS from Linux (not Windows). The SMS service is used for migrating virtual machines, not data.
INCORRECT: "Migrate the data to Amazon FSx for Lustre using AWS DataSync" is incorrect. Amazon FSx for Windows File Server should be used for hosting SMB shares.
INCORRECT: "Migrate the data to Amazon S3 using and AWS Snowball Edge device" is incorrect. Amazon S3 is an object store and unsuitable for hosting an SMB filesystem. Snowball is not required in this case as the data is not going to S3 and there are no time or bandwidth limitations mentioned in the scenario.
References:
https://aws.amazon.com/fsx/windows/
https://aws.amazon.com/datasync/features/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
https://digitalcloud.training/aws-migration-services/
Domain
AWS Application Integration
Question 4Skipped
A new application will be launched on an Amazon EC2 instance with an Elastic Block Store (EBS) volume. A solutions architect needs to determine the most cost-effective storage option. The application will have infrequent usage, with peaks of traffic for a couple of hours in the morning and evening. Disk I/O is variable with peaks of up to 3,000 IOPS.
Which solution should the solutions architect recommend?
Amazon EBS Cold HDD (sc1)
Correct answer
Amazon EBS General Purpose SSD (gp2)
Amazon EBS Provisioned IOPS SSD (io1)
Amazon EBS Throughput Optimized HDD (st1)
Overall explanation
General Purpose SSD (gp2) volumes offer cost-effective storage that is ideal for a broad range of workloads. These volumes deliver single-digit millisecond latencies and the ability to burst to 3,000 IOPS for extended periods of time.
Between a minimum of 100 IOPS (at 33.33 GiB and below) and a maximum of 16,000 IOPS (at 5,334 GiB and above), baseline performance scales linearly at 3 IOPS per GiB of volume size. AWS designs gp2 volumes to deliver their provisioned performance 99% of the time. A gp2 volume can range in size from 1 GiB to 16 TiB.
In this case the volume would have a baseline performance of 3 x 200 = 600 IOPS. The volume could also burst to 3,000 IOPS for extended periods. As the I/O varies, this should be suitable.
CORRECT: "Amazon EBS General Purpose SSD (gp2)" is the correct answer.
INCORRECT: "Amazon EBS Provisioned IOPS SSD (io1) " is incorrect as this would be a more expensive option and is not required for the performance characteristics of this workload.
INCORRECT: "Amazon EBS Cold HDD (sc1)" is incorrect as there is no IOPS SLA for HDD volumes and they would likely not perform well enough for this workload.
INCORRECT: "Amazon EBS Throughput Optimized HDD (st1)" is incorrect as there is no IOPS SLA for HDD volumes and they would likely not perform well enough for this workload.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
Domain
AWS Application Integration
Question 36Skipped
A company is looking for ways to incorporate its current AWS usage expenditure into its operational expense tracking dashboard. A solutions architect has been tasked with proposing a method that enables the company to fetch its current year's cost data and project the costs for the forthcoming 12 months programmatically.
Which approach would fulfill these needs with the MINIMUM operational burden?
Correct answer
Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets.
Generate AWS Budgets reports on usage cost data and dispatch the data to the corporation through SMTP.
Set up AWS Budgets actions to transmit usage cost data to the corporation via FTP.
Make use of downloadable AWS Cost Explorer report files in the .csv format to access usage cost-related data.
Overall explanation
AWS Cost Explorer API provides programmatic access to AWS cost and usage information. The user can query for aggregated data such as total monthly costs or total daily usage with this API.
Also, the Cost Explorer API supports pagination for managing larger data sets, making it efficient for larger queries.
CORRECT: "Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets" is the correct answer (as explained above.)
INCORRECT: "Make use of downloadable AWS Cost Explorer report files in the .csv format to access usage cost-related data" is incorrect.
While AWS Cost Explorer does allow you to download .csv reports of your cost data, this method would not be programmatically accessible and would involve manual steps to download and process the data.
INCORRECT: "Set up AWS Budgets actions to transmit usage cost data to the corporation via FTP" is incorrect.
AWS Budgets actions allow you to set custom cost and usage budgets that trigger actions (such as turning off EC2 instances) when the budget thresholds you set are breached. However, AWS Budgets does not support transmitting data via FTP.
INCORRECT: "Generate AWS Budgets reports on usage cost data and dispatch the data to the corporation through SMTP" is incorrect.
AWS Budgets does not support the dispatching of data through SMTP. AWS Budgets is primarily a tool for setting up alerts on your AWS costs or usage to control your costs, rather than a tool for exporting or transmitting cost data.
References:
https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_Operations_AWS_Cost_Explorer_Service.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-cost-management/
