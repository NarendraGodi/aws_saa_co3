Question 1Skipped
Domain
AWS Migration & Transfer
Question 5Skipped
A company runs a critical data analysis job every Friday evening. The job processes large datasets and requires at least 2 hours to complete without interruptions. The job is stateful and needs reliable compute resources. The company wants to minimize operational overhead while ensuring the job runs as scheduled.
Which solution will meet these requirements?
Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis.
Correct answer
Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler.
Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule.
Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution.
Overall explanation
Configure the job as a containerized task and run it on AWS Fargate using Amazon ECS. Schedule the task using Amazon EventBridge Scheduler: This is the best option because AWS Fargate provides a serverless compute engine for containers, ensuring no interruptions. EventBridge Scheduler offers an easy way to schedule tasks without requiring manual intervention.
Configure the job to run in an AWS Lambda function with reserved concurrency. Use Amazon EventBridge to invoke the function on a schedule: This is incorrect because Lambda functions are not suited for stateful, long-running jobs. Lambda has a maximum execution duration of 15 minutes.
Deploy the job on a dedicated Amazon EC2 On-Demand instance. Use a cron job to schedule the analysis: While this solution avoids interruptions, it requires managing and maintaining the EC2 instance, which increases operational overhead.
Use an Amazon EMR cluster with Spot Instances to process the job. Use Amazon EMR Step Functions to schedule the job execution: Spot Instances are not suitable for stateful jobs because they can be interrupted. This approach also introduces additional complexity with EMR setup and management.
References:
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/scheduling_tasks.html
https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-run-lambda-schedule.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Migration & Transfer
Question 22Skipped
An Amazon VPC contains several Amazon EC2 instances. The instances need to make API calls to Amazon DynamoDB. A solutions architect needs to ensure that the API calls do not traverse the internet.
How can this be accomplished? (Select TWO.)
Correct selection
Create a route table entry for the endpoint
Create an ENI for the endpoint in each of the subnets of the VPC
Create a VPC peering connection between the VPC and DynamoDB
Correct selection
Create a gateway endpoint for DynamoDB
Create a new DynamoDB table that uses the endpoint
Overall explanation
Amazon DynamoDB and Amazon S3 support gateway endpoints, not interface endpoints. With a gateway endpoint you create the endpoint in the VPC, attach a policy allowing access to the service, and then specify the route table to create a route table entry in.


CORRECT: "Create a route table entry for the endpoint" is a correct answer.
CORRECT: "Create a gateway endpoint for DynamoDB" is also a correct answer.
INCORRECT: "Create a new DynamoDB table that uses the endpoint" is incorrect as it is not necessary to create a new DynamoDB table.
INCORRECT: "Create an ENI for the endpoint in each of the subnets of the VPC" is incorrect as an ENI is used by an interface endpoint, not a gateway endpoint.
INCORRECT: "Create a VPC peering connection between the VPC and DynamoDB" is incorrect as you cannot create a VPC peering connection between a VPC and a public AWS service as public services are outside of VPCs.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/vpce-gateway.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Migration & Transfer
Question 55Skipped
The database tier of a web application is running on a Windows server on-premises. The database is a Microsoft SQL Server database. The application owner would like to migrate the database to an Amazon RDS instance.
How can the migration be executed with minimal administrative effort and downtime?
Use the AWS Database Migration Service (DMS) to directly migrate the database to RDS. Use the Schema Conversion Tool (SCT) to enable conversion from Microsoft SQL Server to Amazon RDS
Use AWS DataSync to migrate the data from the database to Amazon S3. Use AWS Database Migration Service (DMS) to migrate the database to RDS
Correct answer
Use the AWS Database Migration Service (DMS) to directly migrate the database to RDS
Use the AWS Server Migration Service (SMS) to migrate the server to Amazon EC2.Use AWS Database Migration Service (DMS) to migrate the database to RDS
Overall explanation
You can directly migrate Microsoft SQL Server from an on-premises server into Amazon RDS using the Microsoft SQL Server database engine. This can be achieved using the native Microsoft SQL Server tools, or using AWS DMS as depicted below:



CORRECT: "Use the AWS Database Migration Service (DMS) to directly migrate the database to RDS" is the correct answer.
INCORRECT: "Use the AWS Server Migration Service (SMS) to migrate the server to Amazon EC2. Use AWS Database Migration Service (DMS) to migrate the database to RDS" is incorrect. You do not need to use the AWS SMS service to migrate the server into EC2 first. You can directly migrate the database online with minimal downtime.
INCORRECT: "Use AWS DataSync to migrate the data from the database to Amazon S3. Use AWS Database Migration Service (DMS) to migrate the database to RDS" is incorrect. AWS DataSync is used for migrating data, not databases.
INCORRECT: "Use the AWS Database Migration Service (DMS) to directly migrate the database to RDS. Use the Schema Conversion Tool (SCT) to enable conversion from Microsoft SQL Server to Amazon RDS" is incorrect. You do not need to use the SCT as you are migrating into the same destination database engine (RDS is just the platform).
References:
https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/migrate-an-on-premises-microsoft-sql-server-database-to-amazon-rds-for-sql-server.html
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Source.html
https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.html
https://aws.amazon.com/dms/schema-conversion-tool/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/
Domain
AWS Migration & Transfer
Question 56Skipped
A scientific research institute stores experimental datasets in AWS. Some datasets are accessed daily for analysis, while others remain unused for weeks or months. The datasets are large and must be highly durable, but the institute wants to reduce costs without compromising availability for frequently accessed data.
The institute needs a cost-effective storage solution that adapts to these varying access patterns and ensures the highest durability.
Which storage solution meets these requirements?
Use Amazon FSx for Lustre integrated with Amazon S3 to offload unused datasets and retrieve them as needed for analysis.
Use Amazon S3 Glacier Instant Retrieval for all datasets to achieve high durability with low-cost storage for infrequent access.
Correct answer
Use Amazon S3 Intelligent-Tiering to automatically adjust storage costs based on the frequency of data access while maintaining high durability.
Use Amazon EFS with lifecycle policies to move infrequently accessed files to lower-cost storage tiers.
Overall explanation
Use Amazon S3 Intelligent-Tiering to automatically adjust storage costs based on the frequency of data access while maintaining high durability: This is correct because S3 Intelligent-Tiering dynamically transitions objects between storage tiers, optimizing costs for infrequent access while retaining the high durability and availability required for datasets.
Use Amazon EFS with lifecycle policies to move infrequently accessed files to lower-cost storage tiers: This is incorrect because Amazon EFS is optimized for file-based workloads and does not provide the same cost optimization or scalability for object storage as S3 Intelligent-Tiering.
Use Amazon S3 Glacier Instant Retrieval for all datasets to achieve high durability with low-cost storage for infrequent access: This is incorrect because S3 Glacier Instant Retrieval is optimized for archival storage, not for datasets that are frequently accessed. The latency and cost of retrieval make it unsuitable for daily analysis.
Use Amazon FSx for Lustre integrated with Amazon S3 to offload unused datasets and retrieve them as needed for analysis: This is incorrect because FSx for Lustre is designed for high-performance computing and workloads requiring fast processing speeds. It introduces unnecessary complexity and cost for general storage needs.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html
https://aws.amazon.com/s3/storage-classes/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Migration & Transfer
Question 41Skipped
A company allows its developers to attach existing IAM policies to existing IAM roles to enable faster experimentation and agility. However, the security operations team is concerned that the developers could attach the existing administrator policy, which would allow the developers to circumvent any other security policies.
How should a solutions architect address this issue?
Use service control policies to disable IAM activity across all accounts in the organizational unit
Prevent the developers from attaching any policies and assign all IAM duties to the security operations team
Create an Amazon SNS topic to send an alert every time a developer creates a new policy
Correct answer
Set an IAM permissions boundary on the developer IAM role that explicitly denies attaching the administrator policy
Overall explanation
The permissions boundary for an IAM entity (user or role) sets the maximum permissions that the entity can have. This can change the effective permissions for that user or role. The effective permissions for an entity are the permissions that are granted by all the policies that affect the user or role. Within an account, the permissions for an entity can be affected by identity-based policies, resource-based policies, permissions boundaries, Organizations SCPs, or session policies.


Therefore, the solutions architect can set an IAM permissions boundary on the developer IAM role that explicitly denies attaching the administrator policy.
CORRECT: "Set an IAM permissions boundary on the developer IAM role that explicitly denies attaching the administrator policy" is the correct answer.
INCORRECT: "Create an Amazon SNS topic to send an alert every time a developer creates a new policy" is incorrect as this would mean investigating every incident which is not an efficient solution.
INCORRECT: "Use service control policies to disable IAM activity across all accounts in the organizational unit" is incorrect as this would prevent the developers from being able to work with IAM completely.
INCORRECT: "Prevent the developers from attaching any policies and assign all IAM duties to the security operations team" is incorrect as this is not necessary. The requirement is to allow developers to work with policies, the solution needs to find a secure way of achieving this.
References:
https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Migration & Transfer
Question 31Skipped
A solutions architect is designing a microservices architecture. AWS Lambda will store data in an Amazon DynamoDB table named Orders. The solutions architect needs to apply an IAM policy to the Lambda function’s execution role to allow it to put, update, and delete items in the Orders table. No other actions should be allowed.
Which of the following code snippets should be included in the IAM policy to fulfill this requirement whilst providing the LEAST privileged access?
Correct answer
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Allow",
"Action": [
"dynamodb:PutItem",
"dynamodb:UpdateItem",
"dynamodb:DeleteItem"
],
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/Orders"
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Allow",
"Action": [
"dynamodb:PutItem",
"dynamodb:UpdateItem",
"dynamodb:DeleteItem"
],
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/*"
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Allow",
"Action": "dynamodb:* ",
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/Orders"
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Deny",
"Action": "dynamodb:* ",
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/Orders"
Overall explanation
The key requirements are to allow the Lambda function the put, update, and delete actions on a single table. Using the principle of least privilege the answer should not allow any other access.
CORRECT: The following answer is correct:
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Allow",
"Action": [
"dynamodb:PutItem",
"dynamodb:UpdateItem",
"dynamodb:DeleteItem"
],
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/Orders"
This code snippet specifies the exact actions to allow and also specified the resource to apply those permissions to.
INCORRECT: the following answer is incorrect:
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Allow",
"Action": [
"dynamodb:PutItem",
"dynamodb:UpdateItem",
"dynamodb:DeleteItem"
],
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/*"
This code snippet specifies the correct list of actions but it provides a wildcard “*” instead of specifying the exact resource. Therefore, the function will be able to put, update, and delete items on any table in the account.
INCORRECT: the following answer is incorrect:
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Allow",
"Action": "dynamodb:* ",
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/Orders"
This code snippet allows any action on DynamoDB by using a wildcard “dynamodb:*”. This does not follow the principle of least privilege.
INCORRECT: the following answer is incorrect:
"Sid": "PutUpdateDeleteOnOrders",
"Effect": "Deny",
"Action": "dynamodb:* ",
"Resource": "arn:aws:dynamodb:us-east-1:227392126428:table/Orders"
This code snippet denies any action on the table. This does not have the desired effect.
References:
https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_elements.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Migration & Transfer
Question 26Skipped
A Solutions Architect needs to select a low-cost, short-term option for adding resilience to an AWS Direct Connect connection. What is the MOST cost-effective solution to provide a backup for the Direct Connect connection?
Correct answer
Implement an IPSec VPN connection and use the same BGP prefix
Configure an IPSec VPN connection over the Direct Connect link
Configure AWS Transit Gateway with an IPSec VPN backup
Implement a second AWS Direct Connection
Overall explanation
This is the most cost-effective solution. With this option both the Direct Connect connection and IPSec VPN are active and being advertised using the Border Gateway Protocol (BGP). The Direct Connect link will always be preferred unless it is unavailable.
CORRECT: "Implement an IPSec VPN connection and use the same BGP prefix" is the correct answer.
INCORRECT: "Implement a second AWS Direct Connection" is incorrect. This is not a short-term or low-cost option as it takes time to implement and is costly.
INCORRECT: "Configure AWS Transit Gateway with an IPSec VPN backup" is incorrect. This is a workable solution and provides some advantages. However, you do need to pay for the Transit Gateway so it is not the most cost-effective option and probably not suitable for a short-term need.
INCORRECT: "Configure an IPSec VPN connection over the Direct Connect link" is incorrect. This is not a solution to the problem as the VPN connection is going over the Direct Connect link. This is something you might do to add encryption to Direct Connect but it doesn’t make it more resilient.
References:
https://docs.aws.amazon.com/whitepapers/latest/hybrid-connectivity/vpn-connection-as-a-backup-to-aws-dx-connection-example.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-direct-connect/
Domain
AWS Migration & Transfer
Question 48Skipped
A solutions architect needs to backup some application log files from an online ecommerce store to Amazon S3. It is unknown how often the logs will be accessed or which logs will be accessed the most. The solutions architect must keep costs as low as possible by using the appropriate S3 storage class.
Which S3 storage class should be implemented to meet these requirements?
S3 Standard-Infrequent Access (S3 Standard-IA)
S3 Glacier
Correct answer
S3 Intelligent-Tiering
S3 One Zone-Infrequent Access (S3 One Zone-IA)
Overall explanation
The S3 Intelligent-Tiering storage class is designed to optimize costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.
It works by storing objects in two access tiers: one tier that is optimized for frequent access and another lower-cost tier that is optimized for infrequent access. This is an ideal use case for intelligent-tiering as the access patterns for the log files are not known.
CORRECT: "S3 Intelligent-Tiering" is the correct answer.
INCORRECT: "S3 Standard-Infrequent Access (S3 Standard-IA)" is incorrect as if the data is accessed often retrieval fees could become expensive.
INCORRECT: "S3 One Zone-Infrequent Access (S3 One Zone-IA)" is incorrect as if the data is accessed often retrieval fees could become expensive.
INCORRECT: "S3 Glacier" is incorrect as if the data is accessed often retrieval fees could become expensive. Glacier also requires more work in retrieving the data from the archive and quick access requirements can add further costs.
References:
https://aws.amazon.com/s3/storage-classes/#Unknown_or_changing_access
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Migration & Transfer
Question 54Skipped
A team are planning to run analytics jobs on log files each day and require a storage solution. The size and number of logs is unknown and data will persist for 24 hours only.
What is the MOST cost-effective solution?
Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
Correct answer
Amazon S3 Standard
Amazon S3 Intelligent-Tiering
Amazon S3 Glacier Deep Archive
Overall explanation
S3 standard is the best choice in this scenario for a short term storage solution. In this case the size and number of logs is unknown and it would be difficult to fully assess the access patterns at this stage. Therefore, using S3 standard is best as it is cost-effective, provides immediate access, and there are no retrieval fees or minimum capacity charge per object.
CORRECT: "Amazon S3 Standard" is the correct answer.
INCORRECT: "Amazon S3 Intelligent-Tiering" is incorrect as there is an additional fee for using this service and for a short-term requirement it may not be beneficial.
INCORRECT: "Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)" is incorrect as this storage class has a minimum capacity charge per object (128 KB) and a per GB retrieval fee.
INCORRECT: "Amazon S3 Glacier Deep Archive" is incorrect as this storage class is used for archiving data. There are retrieval fees and it take hours to retrieve data from an archive.
References:
https://aws.amazon.com/s3/storage-classes/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Migration & Transfer

Dump8
Question 1Skipped
An online game platform company is launching a new game feature that involves a significant update to their existing API hosted on Amazon API Gateway. The company wants to minimize the impact on their existing users, and they need a deployment strategy that allows them to gradually roll out the changes while monitoring for any potential issues.
What should the company do to achieve this?
Create a new version of the API and use Route 53 to gradually shift DNS queries from the existing API endpoint to the new API endpoint.
Create a completely new API for the new game feature and redirect half of the user traffic to the new API while maintaining the other half on the existing API.
Correct answer
Use an API Gateway canary release deployment. Initially direct a small percentage of user traffic to the new API version. After API verification, promote the canary stage to the production stage.
Update the existing API directly in API Gateway with the new feature and immediately direct all traffic to the updated API.
Overall explanation
The correct answer is to use Amazon API Gateway's canary release deployments. This allows the company to gradually roll out the new API version, initially exposing only a small percentage of their users to the new API. As they monitor the system and confirm that the new API is working as expected, they can increase the percentage of traffic directed to the new version.
CORRECT: "Use an API Gateway canary release deployment. Initially direct a small percentage of user traffic to the new API version. After API verification, promote the canary stage to the production stage" is the correct answer (as explained above.)
INCORRECT: "Update the existing API directly in API Gateway with the new feature and immediately direct all traffic to the updated API" is incorrect.
Updating the existing API directly in API Gateway and immediately redirecting all traffic to the updated API is risky. If there are any issues with the new API, it could negatively impact all users, rather than just a small subset of users.
INCORRECT: "Create a completely new API for the new game feature and redirect half of the user traffic to the new API while maintaining the other half on the existing API" is incorrect.
Creating a completely new API and redirecting half the user traffic to the new API is not a gradual rollout strategy. This approach would immediately expose many users to potential issues with the new API.
INCORRECT: "Create a new version of the API and use Route 53 to gradually shift DNS queries from the existing API endpoint to the new API endpoint" is incorrect.
Using Route 53 to gradually shift DNS queries from the existing API endpoint to the new API endpoint could work, but it is not as simple or efficient as using API Gateway's canary release deployments. DNS changes can also take time to propagate, potentially leading to inconsistent behavior for users.
References:
https://docs.aws.amazon.com/apigateway/latest/developerguide/canary-release.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-api-gateway/
Domain
AWS Migration & Transfer
Question 3Skipped
A multinational enterprise plans to transition from numerous independent AWS accounts to a structured, multi-account AWS setup. The enterprise anticipates creating multiple AWS accounts to cater to various departments. The enterprise seeks to authenticate access to these AWS accounts using a centralized corporate directory service.
What combination of steps should a solutions architect suggest to meet these needs? (Select TWO.)
Install and configure AWS Control Tower for centralized account management. Incorporate AWS Identity Center to manage identity.
Set up an Amazon Cognito identity pool and configure AWS Identity Center to accept Amazon Cognito authentication.
Establish an AWS Transit Gateway for centralized network management, linking AWS accounts.
Correct selection
Deploy AWS Directory Service and integrate it with the corporate directory service. Set up AWS Identity Center for authentication across accounts.
Correct selection
Create a new AWS Organizations entity with all features enabled. Create the new AWS accounts within the organization.
Overall explanation
AWS Organizations provides policy-based management for multiple AWS accounts. With Organizations, you can create member accounts that are part of your organization and centrally manage your accounts.
AWS Directory Service allows you to connect your AWS resources with an existing on-premises Microsoft Active Directory or to set up a new, stand-alone directory in the AWS Cloud. AWS Identity Center makes it easy to centrally manage access to multiple AWS accounts and business applications and provide users with single sign-on access to all their assigned accounts and applications from one place.
CORRECT: "Create a new AWS Organizations entity with all features enabled. Create the new AWS accounts within the organization" is a correct answer (as explained above.)
CORRECT: "Deploy AWS Directory Service and integrate it with the corporate directory service. Set up AWS Identity Center for authentication across accounts" is also a correct answer (as explained above.)
INCORRECT: "Install and configure AWS Control Tower for centralized account management. Incorporate AWS Identity Center to manage identity" is incorrect.
AWS Control Tower does have certain benefits, but it doesn't directly cater to the company's need for centralized corporate directory service integration. However, it could be used in conjunction with AWS Identity Center for user access management.
INCORRECT: "Set up an Amazon Cognito identity pool and configure AWS Identity Center to accept Amazon Cognito authentication" is incorrect.
Amazon Cognito is primarily used to add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily. It isn't typically used in multi-account management scenarios and isn't directly relevant to the requirement for corporate directory service integration.
INCORRECT: "Establish an AWS Transit Gateway for centralized network management, linking AWS accounts" is incorrect.
AWS Transit Gateway connects VPCs and on-premises networks through a central hub. It is a network transit hub, not a user authentication and management service. It doesn't directly address the need for centralized corporate directory service integration.
References:
https://docs.aws.amazon.com/singlesignon/latest/userguide/manage-your-identity-source-ad.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-organizations/
Domain
AWS Migration & Transfer
Question 55Skipped
An organization is planning their disaster recovery solution. They plan to run a scaled down version of a fully functional environment. In a DR situation the recovery time must be minimized.
Which DR strategy should a Solutions Architect recommend?
Multi-site
Correct answer
Warm standby
Pilot light
Backup and restore
Overall explanation
The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud. A warm standby solution extends the pilot light elements and preparation.
It further decreases the recovery time because some services are always running. By identifying your business-critical systems, you can fully duplicate these systems on AWS and have them always on.
CORRECT: "Warm standby" is the correct answer.
INCORRECT: "Backup and restore" is incorrect. This is the lowest cost DR approach that simply entails creating online backups of all data and applications.
INCORRECT: Pilot light"" is incorrect. With a pilot light strategy a core minimum of services are running and the remainder are only brought online during a disaster recovery situation.
INCORRECT: "Multi-site" is incorrect. A multi-site solution runs on AWS as well as on your existing on-site infrastructure in an active- active configuration.
References:
https://aws.amazon.com/blogs/publicsector/rapidly-recover-mission-critical-systems-in-a-disaster/
Domain
AWS Migration & Transfer

Dump9
Question 1Skipped
A Solutions Architect has created an AWS Organization with several AWS accounts. Security policy requires that use of specific API actions are limited across all accounts. The Solutions Architect requires a method of centrally controlling these actions.
What is the SIMPLEST method of achieving the requirements?
Create cross-account roles in each account to limit access to the services and actions that are allowed
Create a Network ACL that limits access to the services or actions and attach it to all relevant subnets
Create an IAM policy in the root account and attach it to users and groups in each account
Correct answer
Create a service control policy in the root organizational unit to deny access to the services or actions
Overall explanation
Service control policies (SCPs) offer central control over the maximum available permissions for all accounts in your organization allowing you to ensure your accounts stay within your organization’s access control guidelines.
In the example below, a policy in OU1 restricts all users from launching EC2 instance types other than a t2.micro:


CORRECT: "Create a service control policy in the root organizational unit to deny access to the services or actions" is the correct answer.
INCORRECT: "Create a Network ACL that limits access to the services or actions and attach it to all relevant subnets" is incorrect. Network ACLs control network traffic - not API actions.
INCORRECT: "Create an IAM policy in the root account and attach it to users and groups in each account" is incorrect. This is not an efficient or centrally managed method of applying the security restrictions.
INCORRECT: "Create cross-account roles in each account to limit access to the services and actions that are allowed" is incorrect. This is another example of a complex and inefficient method of providing access across accounts and does not restrict API actions within the account.
References:
https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_about-scps.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/certification-training/aws-solutions-architect-associate/security-identity-compliance/aws-accounts/
Domain
AWS Migration & Transfer
Question 21Skipped
A company operates a critical Python-based application that analyzes incoming real-time data. The application runs every 15 minutes and takes approximately 2 minutes to complete a run. It requires 1.5 GB of memory and uses the CPU intensively during its operation. The company wants to minimize the costs associated with running this application.
Which solution will meet these requirements?
Correct answer
Implement the application as an AWS Lambda function configured with 1.5 GB of memory. Use Amazon EventBridge to schedule the function to run every 15 minutes.
Deploy the application on an Amazon EC2 instance and manually start and stop the instance in alignment with the schedule of the application run.
Use AWS App2Container (A2C) to containerize the application. Deploy the container on an Amazon EC2 instance, configure an Amazon CloudWatch alarm to stop the instance when the application is not running.
Use AWS App2Container (A2C) to containerize the application. Run the application as an Amazon Elastic Container Service (Amazon ECS) task on AWS Fargate with 1 virtual CPU (vCPU) and 1.5 GB of memory.
Overall explanation
This is the most cost-effective solution. AWS Lambda is designed for running code in response to events or on a schedule, and you only pay for the compute time that you consume.
Configuring the function with 1.5GB memory would ensure the function has enough resources, and using Amazon EventBridge for scheduling would enable running the function every 15 minutes.
CORRECT: "Implement the application as an AWS Lambda function configured with 1.5 GB of memory. Use Amazon EventBridge to schedule the function to run every 15 minutes" is the correct answer (as explained above.)
INCORRECT: "Use AWS App2Container (A2C) to containerize the application. Run the application as an Amazon Elastic Container Service (Amazon ECS) task on AWS Fargate with 1 virtual CPU (vCPU) and 1.5 GB of memory" is incorrect.
This is not the most cost-effective solution. Even though AWS App2Container (A2C) would help in containerizing the application and AWS Fargate would abstract the need to manage underlying EC2 instances, it is still an overkill for an application that runs for short durations intermittently. It would still result in paying for unused compute resources.
INCORRECT: "Use AWS App2Container (A2C) to containerize the application. Deploy the container on an Amazon EC2 instance, configure an Amazon CloudWatch alarm to stop the instance when the application is not running" is incorrect.
AWS App2Container (A2C) is used to help containerize applications, but this does not optimize for cost because it requires running an EC2 instance continuously and stopping the instance when not in use can be complex and might not be timely, resulting in potential unnecessary costs.
INCORRECT: "Deploy the application on an Amazon EC2 instance and manually start and stop the instance in alignment with the schedule of the application run" is incorrect.
This solution involves significant manual intervention and managing EC2 instances. While it can work, it's not an optimized way, especially in terms of cost and operation overhead. It does not take advantage of the pay-per-use model and automatic scaling provided by AWS Lambda.
References:
https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-run-lambda-schedule.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudwatch/
Domain
AWS Migration & Transfer
Question 24Skipped
A High Performance Computing (HPC) application needs storage that can provide 135,000 IOPS. The storage layer is replicated across all instances in a cluster.
What is the optimal storage solution that provides the required performance and is cost-effective?
Use Amazon EBS Provisioned IOPS volume with 135,000 IOPS
Correct answer
Use Amazon Instance Store
Use Amazon EC2 Enhanced Networking with an EBS HDD Throughput Optimized volume
Use Amazon S3 with byte-range fetch
Overall explanation
Instance stores offer very high performance and low latency. As long as you can afford to lose an instance, i.e. you are replicating your data, these can be a good solution for high performance/low latency requirements. Also, the cost of instance stores is included in the instance charges so it can also be more cost-effective than EBS Provisioned IOPS.
CORRECT: "Use Amazon Instance Store" is the correct answer.
INCORRECT: "Use Amazon EBS Provisioned IOPS volume with 135,000 IOPS" is incorrect. In the case of a HPC cluster that replicates data between nodes you don’t necessarily need a shared storage solution such as Amazon EBS Provisioned IOPS – this would also be a more expensive solution as the Instance Store is included in the cost of the HPC instance.
INCORRECT: "Use Amazon S3 with byte-range fetch" is incorrect. Amazon S3 is not a solution for this HPC application as in this case it will require block-based storage to provide the required IOPS.
INCORRECT: "Enhanced networking provides higher bandwidth and lower latency and is implemented using an Elastic Network Adapter (ENA). However, using an ENA with an HDD Throughput Optimized volume is not recommended and the volume will not provide the performance required for this use case." is incorrect
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
https://digitalcloud.training/amazon-ebs/
Domain
AWS Migration & Transfer
Question 44Skipped
An application uses a MySQL database running on an Amazon EC2 instance. The application generates high I/O and constant writes to a single table on the database. Which Amazon EBS volume type will provide the MOST consistent performance and low latency?
Cold HDD (sc1)
General Purpose SSD (gp2)
Correct answer
Provisioned IOPS SSD (io1)
Throughput Optimized HDD (st1)
Overall explanation
The Provisioned IOPS SSD (io1) volume type will offer the most consistent performance and can be configured with the amount of IOPS required by the application. It will also provide the lowest latency of the options presented.


CORRECT: "Provisioned IOPS SSD (io1)" is the correct answer.
INCORRECT: "General Purpose SSD (gp2)" is incorrect. This is not the best solution for when you require high I/O, consistent performance and low latency.
INCORRECT: "Throughput Optimized HDD (st1)" is incorrect. This is a HDD type of disk and not suitable for low latency workloads that require consistent performance.
INCORRECT: "Cold HDD (sc1)" is incorrect. This is the lowest cost option and not suitable for frequently accessed workloads.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
