Question 1Skipped
Domain
AWS Analytics
Question 8Skipped
There are two applications in a company: a sender application that sends messages containing payloads, and a processing application that receives messages containing payloads. The company wants to implement an AWS service to handle messages between these two different applications. The sender application sends on average 1,000 messages each hour and the messages depending on the type sometimes take up to 2 days to be processed. If the messages fail to process, they must be retained so that they do not impact the processing of any remaining messages.
Which solution meets these requirements and is the MOST operationally efficient?
Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application.
Correct answer
Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.
Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application.
Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively.
Overall explanation
Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS eliminates the complexity and overhead associated with managing and operating message-oriented middleware and empowers developers to focus on differentiating work.
CORRECT: "Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages” is the correct answer (as explained above.)
INCORRECT: "Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS.
INCORRECT: "Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application” is incorrect, as the most operationally efficient way is to use the managed service Amazon SQS
INCORRECT: "Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application” is incorrect as Amazon SNS is not a queuing service, but a pub-sub one to many notification service and cannot be used as a queue.
References:
https://aws.amazon.com/sqs/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Analytics
Question 20Skipped
A logistics company is running a containerized application on an Amazon Elastic Kubernetes Service (Amazon EKS) cluster with Amazon EC2 instances as the worker nodes. The application includes a management dashboard that uses Amazon DynamoDB for real-time tracking data and a reporting service that stores large datasets in Amazon S3.
The company needs to ensure that the EKS Pods running the management dashboard can access only Amazon DynamoDB, and the EKS Pods running the reporting service can access only Amazon S3. The company uses AWS Identity and Access Management (IAM) for access control.
Which solution will meet these requirements?
Create IAM roles with permissions for Amazon S3 and DynamoDB access. Attach the Amazon S3 role to the reporting service Pods and the DynamoDB role to the management dashboard Pods using a shared service account.
Configure role-based access control (RBAC) within Kubernetes to define which Pods can access Amazon S3 and DynamoDB. Use Kubernetes ConfigMaps to store the IAM credentials for each service.
Correct answer
Create separate IAM roles with policies for Amazon S3 and DynamoDB access. Use Kubernetes service accounts with IAM Role for Service Accounts (IRSA) to assign the AmazonS3FullAccess policy to the reporting service Pods and the AmazonDynamoDBFullAccess policy to the management dashboard Pods.
Create separate IAM policies for Amazon S3 and DynamoDB access. Attach both policies to the IAM role associated with the EC2 instance profile. Use Kubernetes namespaces to restrict access for the respective Pods to Amazon S3 or DynamoDB.
Overall explanation
Create separate IAM roles with policies for Amazon S3 and DynamoDB access. Use Kubernetes service accounts with IAM Role for Service Accounts (IRSA) to assign the AmazonS3FullAccess policy to the reporting service Pods and the AmazonDynamoDBFullAccess policy to the management dashboard Pods: This is correct because IAM Role for Service Accounts (IRSA) allows the assignment of IAM roles directly to Kubernetes service accounts, which the Pods use to assume permissions. This solution enables fine-grained access control, ensuring that the Pods for the management dashboard can access only DynamoDB and the Pods for the reporting service can access only S3.
Create separate IAM policies for Amazon S3 and DynamoDB access. Attach both policies to the IAM role associated with the EC2 instance profile. Use Kubernetes namespaces to restrict access for the respective Pods to Amazon S3 or DynamoDB: This is incorrect because attaching both policies to the EC2 instance profile means all Pods running on the worker nodes would inherit access to both S3 and DynamoDB, violating the requirement for restricted access. Kubernetes namespaces alone do not enforce IAM permissions.
Create IAM roles with permissions for Amazon S3 and DynamoDB access. Attach the Amazon S3 role to the reporting service Pods and the DynamoDB role to the management dashboard Pods using a shared service account: This is incorrect because using a shared service account would not provide sufficient isolation between the Pods. IRSA is the correct mechanism to ensure separate access control for each service.
Configure role-based access control (RBAC) within Kubernetes to define which Pods can access Amazon S3 and DynamoDB. Use Kubernetes ConfigMaps to store the IAM credentials for each service: This is incorrect because storing IAM credentials in ConfigMaps is not a secure practice. Additionally, RBAC in Kubernetes is not designed to enforce access control for AWS services. IRSA is the proper solution for managing IAM permissions at the Pod level.
References:
https://docs.aws.amazon.com/eks/latest/userguide/iam-roles-for-service-accounts.html
https://docs.aws.amazon.com/eks/latest/userguide/associate-service-account-role.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Analytics
Question 52Skipped
A company is migrating from an on-premises infrastructure to the AWS Cloud. One of the company's applications stores files on a Windows file server farm that uses Distributed File System Replication (DFSR) to keep data in sync. A solutions architect needs to replace the file server farm.
Which service should the solutions architect use?
AWS Storage Gateway
Amazon EFS
Amazon S3
Correct answer
Amazon FSx
Overall explanation
Amazon FSx for Windows File Server provides fully managed, highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol.
Amazon FSx is built on Windows Server and provides a rich set of administrative features that include end-user file restore, user quotas, and Access Control Lists (ACLs).
Additionally, Amazon FSX for Windows File Server supports Distributed File System Replication (DFSR) in Single-AZ deployments as can be seen in the feature comparison table below.


CORRECT: "Amazon FSx" is the correct answer.
INCORRECT: "Amazon EFS" is incorrect as EFS only supports Linux systems.
INCORRECT: "Amazon S3" is incorrect as this is not a suitable replacement for a Microsoft filesystem.
INCORRECT: "AWS Storage Gateway" is incorrect as this service is primarily used for connecting on-premises storage to cloud storage. It consists of a software device installed on-premises and can be used with SMB shares but it actually stores the data on S3. It is also used for migration. However, in this case the company need to replace the file server farm and Amazon FSx is the best choice for this job.
References:
https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Analytics

Dump5
Question 1Skipped
A company wants to migrate a legacy web application from an on-premises data center to AWS. The web application consists of a web tier, an application tier, and a MySQL database. The company does not want to manage instances or clusters.
Which combination of services should a solutions architect include in the overall architecture? (Select TWO.)
Correct selection
Amazon RDS for MySQL
Amazon Kinesis Data Streams
Amazon DynamoDB
Correct selection
AWS Fargate
Amazon EC2 Spot Instances
Overall explanation
Amazon RDS is a managed service and you do not need to manage the instances. This is an ideal backend for the application and you can run a MySQL database on RDS without any refactoring. For the application components these can run on Docker containers with AWS Fargate. Fargate is a serverless service for running containers on AWS.
CORRECT: "AWS Fargate" is a correct answer.
CORRECT: "Amazon RDS for MySQL" is also a correct answer.
INCORRECT: "Amazon DynamoDB" is incorrect. This is a NoSQL database and would be incompatible with the relational MySQL DB.
INCORRECT: "Amazon EC2 Spot Instances" is incorrect. This would require managing instances.
INCORRECT: "Amazon Kinesis Data Streams" is incorrect. This is a service for streaming data.
References:
https://aws.amazon.com/rds/
https://aws.amazon.com/fargate/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
https://digitalcloud.training/amazon-rds/
Domain
AWS Analytics
Question 52Skipped
An application running on Amazon ECS processes data and then writes objects to an Amazon S3 bucket. The application requires permissions to make the S3 API calls.
How can a Solutions Architect ensure the application has the required permissions?
Create a set of Access Keys with read/write permissions to the bucket and update the task credential ID.
Update the S3 policy in IAM to allow read/write access from Amazon ECS, and then relaunch the container.
Correct answer
Create an IAM role that has read/write permissions to the bucket and update the task definition to specify the role as the taskRoleArn.
Attach an IAM policy with read/write permissions to the bucket to an IAM group and add the container instances to the group.
Overall explanation
With IAM roles for Amazon ECS tasks, you can specify an IAM role that can be used by the containers in a task. Applications must sign their AWS API requests with AWS credentials, and this feature provides a strategy for managing credentials for your applications to use, similar to the way that Amazon EC2 instance profiles provide credentials to EC2 instances.
You define the IAM role to use in your task definitions, or you can use a taskRoleArn override when running a task manually with the RunTask API operation.
Note that there are instances roles and task roles that you can assign in ECS when using the EC2 launch type. The task role is better when you need to assign permissions for just that specific task:


CORRECT: "Create an IAM role that has read/write permissions to the bucket and update the task definition to specify the role as the taskRoleArn" is the correct answer.
INCORRECT: "Update the S3 policy in IAM to allow read/write access from Amazon ECS, and then relaunch the container" is incorrect. Policies must be assigned to tasks using IAM Roles and this is not mentioned here.
INCORRECT: "Create a set of Access Keys with read/write permissions to the bucket and update the task credential ID" is incorrect. You cannot update the task credential ID with access keys and roles should be used instead.
INCORRECT: "Attach an IAM policy with read/write permissions to the bucket to an IAM group and add the container instances to the group" is incorrect. You cannot add container instances to an IAM group.
References:
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-iam-roles.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Analytics
Question 40Skipped
IAM permissions-related Access Denied errors and Unauthorized errors need to be analyzed and troubleshooted by a company. AWS CloudTrail has been enabled at the company.
Which solution will meet these requirements with the LEAST effort?
Write custom scripts to query CloudTrail logs using AWS Glue.
Search CloudTrail logs with Amazon RedShift. Create a dashboard to identify the errors.
Create a custom script and execute it against CloudTrail logs to find errors using AWS Batch.
Correct answer
Search CloudTrail logs with Amazon QuickSight. Create a dashboard to identify the errors.
Overall explanation
CloudTrail logs are stored natively within an S3 bucket , which can then be easily integrated with Amazon QuickSight. Amazon QuickSight is a data visualization tool which will show any IAM permissions-related Access Denied errors and Unauthorized errors.

CORRECT: "Search CloudTrail logs with Amazon QuickSight. Create a dashboard to identify the errors” is the correct answer (as explained above.)
INCORRECT: "Create a custom script and execute it against CloudTrail logs to find errors using AWS Batch” is incorrect. Writing custom scripts is inevitably more effort than using the native connection between AWS CloudTrail and Amazon QuickSight.
INCORRECT: "Search CloudTrail logs with Amazon RedShift. Create a dashboard to identify the errors” is incorrect. Amazon RedShift would not be a simple way of achieving this outcome.
INCORRECT: “Write custom scripts to query CloudTrail logs using AWS Glue” is incorrect. AWS Batch requires configuring several EC2 instances to run jobs for you. This, and writing custom scripts will significantly increase the effort involved.
References:
https://docs.aws.amazon.com/quicksight/latest/user/logging-using-cloudtrail.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-analytics-services/
Domain
AWS Analytics
Question 41Skipped
An application is running in a private subnet of an Amazon VPC and must have outbound internet access for downloading updates. The Solutions Architect does not want the application exposed to inbound connection attempts. Which steps should be taken?
Attach an internet gateway to the private subnet and create a NAT gateway
Create a NAT gateway but do not attach an internet gateway to the VPC
Correct answer
Create a NAT gateway and attach an internet gateway to the VPC
Attach an internet gateway to the VPC but do not create a NAT gateway
Overall explanation
To enable outbound connectivity for instances in private subnets a NAT gateway can be created. The NAT gateway is created in a public subnet and a route must be created in the private subnet pointing to the NAT gateway for internet-bound traffic. An internet gateway must be attached to the VPC to facilitate outbound connections.


You cannot directly connect to an instance in a private subnet from the internet. You would need to use a bastion/jump host. Therefore, the application will not be exposed to inbound connection attempts.
CORRECT: "Create a NAT gateway and attach an internet gateway to the VPC" is the correct answer.
INCORRECT: "Create a NAT gateway but do not create attach an internet gateway to the VPC" is incorrect. An internet gateway must be attached to the VPC for any outbound connections to work.
INCORRECT: "Attach an internet gateway to the private subnet and create a NAT gateway" is incorrect. You do not attach internet gateways to subnets, you attach them to VPCs.
INCORRECT: "Attach an internet gateway to the VPC but do not create a NAT gateway" is incorrect. Without a NAT gateway the instances in the private subnet will not be able to download updates from the internet.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Analytics
Question 48Skipped
A large company is currently using multiple AWS accounts as part of its cloud deployment model, and these accounts are currently structured using AWS Organizations. A Solutions Architect has been tasked with limiting access to an Amazon S3 bucket to only users of accounts that are enrolled with AWS Organizations. The Solutions Architect wants to avoid listing the many dozens of account IDs in the Bucket policy, as there are many accounts the frequent changes.
Which strategy meets these requirements with the LEAST amount of effort?
Add all the non-organizational accounts to an Organizational Unit (OU) and attached a Service Control Policy (SCP) which denies access to the specific Amazon S3 bucket.
Use AWS Config and AWS Lambda functions to make remediations to the bucket policy as and when new accounts are created and tagged as not being part of AWS Organizations. Update the S3 bucket policy accordingly.
Use Attribute Based Access Control by referencing Tags of accounts which are either enrolled as part of AWS Organizations, or not.
Correct answer
Use the global key of AWS Organizations within a bucket policy using the aws:PrincipalOrgID key to allow access only to accounts which are part of the Organization.
Overall explanation
The aws:PrincipalOrgID global key provides a simpler alternative to manually listing and updating all the account IDs for all AWS accounts that exist within an Organization. The following Amazon S3 bucket policy allows members of any account in the ‘123456789’ organization to add an object into the ‘mydctbucket’ bucket.

CORRECT: "Use the global key of AWS Organizations within a bucket policy using the aws:PrincipalOrgID key to allow access only to accounts which are part of the Organization" is the correct answer (as explained above.)
INCORRECT: "Use Attribute Based Access Control by referencing Tags of accounts which are either enrolled as part of AWS Organizations, or not" is incorrect. This could be a viable option, however maintaining an accurate tagging policy as opposed to referencing the PrincipalOrgID would much more difficult.
INCORRECT: "Use AWS Config and AWS Lambda functions to make remediations to the bucket policy as and when new accounts are created and tagged as not being part of AWS Organizations. Update the S3 bucket policy accordingly" is incorrect.
Every time an account is added or removed from the organization this workflow would have to fire. This solution would need to be built and maintained, whereas it is much easier to refer to the PrincipalOrgID once and avoid needing to change the Bucket Policy.
INCORRECT: "Add all the non-organizational accounts to an Organizational Unit (OU) and attached a Service Control Policy (SCP) which denies access to the specific Amazon S3 bucket" is incorrect. You can only use Organization Units (OUs) and Service Control Policies (SCPs) with accounts that are a part of AWS Organizations – meaning this solution could not work.
References:
https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-organizations/
Domain
AWS Analytics
Question 12Skipped
A systems administrator of a company wants to detect and remediate the compromise of services such as Amazon EC2 instances and Amazon S3 buckets.
Which AWS service can the administrator use to protect the company against attacks?
Correct answer
Amazon GuardDuty
Amazon Macie
Amazon Inspector
Amazon Cognito
Overall explanation
Amazon GuardDuty gives you access to built-in detection techniques that are developed and optimized for the cloud. The detection algorithms are maintained and continuously improved upon by AWS Security. The primary detection categories include reconnaissance, instance compromise, account compromise, and bucket compromise.
Amazon GuardDuty offers HTTPS APIs, CLI tools, and Amazon CloudWatch Events to support automated security responses to security findings. For example, you can automate the response workflow by using CloudWatch Events as an event source to trigger an AWS Lambda function.
CORRECT: "Amazon GuardDuty" is the correct answer.
INCORRECT: "Amazon Cognito" is incorrect. Cognito provides sign up and sign services for mobiles apps.
INCORRECT: "Amazon Inspector" is incorrect. Inspector is more about identifying vulnerabilities and evaluating against security best practices. It does not detect compromise.
INCORRECT: "Amazon Macie" is incorrect. Macie is used for detecting and protecting sensitive data that is in Amazon S3.
References:
https://aws.amazon.com/guardduty/features/
Save time with our AWS cheat sheets:
https://digitalcloud.training/additional-aws-services/
