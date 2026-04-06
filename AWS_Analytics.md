---

## AWS Analytics – Practice Questions

---

### Question 8

**Q:** There are two applications in a company: a sender application that sends messages containing payloads, and a processing application that receives messages containing payloads. The company wants to decouple the two applications.

**Options:**

- Receive the messages from the sender application using an Amazon Kinesis data stream. Utilize the Kinesis Client Library (KCL) to integrate the processing application.
- Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic to receive notifications. Write to the SNS topic using the sender application.
- Set up a Redis database on Amazon EC2. Configure the instance to be used by both applications. The messages should be stored, processed, and deleted, respectively.
- **✅ Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.**

**A:** **Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages.**

**Explanation:**

Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS eliminates the complexity and overhead associated with managing and operating message-oriented middleware.

- **CORRECT:** "Provide an Amazon Simple Queue Service (Amazon SQS) queue for the sender and processor applications. Set up a dead-letter queue to collect failed messages" is the correct answer.
- **INCORRECT:** "Set up a Redis database on Amazon EC2..." is incorrect.
- **INCORRECT:** "Receive the messages from the sender application using an Amazon Kinesis data stream..." is incorrect.
- **INCORRECT:** "Subscribe the processing application to an Amazon Simple Notification Service (Amazon SNS) topic..." is incorrect.

**References:**
- https://aws.amazon.com/sqs/
- https://digitalcloud.training/aws-application-integration-services/

---

### Question 20

**Q:** A logistics company is running a containerized application on an Amazon Elastic Kubernetes Service (Amazon EKS) cluster with Amazon EC2 instances as the worker nodes. The application includes a reporting service that needs access to Amazon S3 and a management dashboard that needs access to DynamoDB. The company requires a secure and scalable approach to provide these permissions following the principle of least privilege.

**Options:**

- Create IAM roles with permissions for Amazon S3 and DynamoDB access. Attach the Amazon S3 role to the reporting service Pods and the DynamoDB role to the management dashboard Pods using a shared service account.
- Create separate IAM policies for Amazon S3 and DynamoDB access. Attach both policies to the IAM role associated with the EC2 instance profile. Use Kubernetes namespaces to restrict access for the relevant Pods.
- Configure role-based access control (RBAC) within Kubernetes to define which Pods can access Amazon S3 and DynamoDB. Use Kubernetes ConfigMaps to store the IAM credentials for each service.
- **✅ Create separate IAM roles with policies for Amazon S3 and DynamoDB access. Use Kubernetes service accounts with IAM Role for Service Accounts (IRSA) to assign the AmazonS3FullAccess policy to the reporting service and the AmazonDynamoDBFullAccess policy to the management dashboard.**

**A:** **Create separate IAM roles with policies for Amazon S3 and DynamoDB access. Use Kubernetes service accounts with IAM Role for Service Accounts (IRSA) to assign the AmazonS3FullAccess policy to the reporting service and the AmazonDynamoDBFullAccess policy to the management dashboard.**

**Explanation:**

- **CORRECT:** Using IRSA with separate IAM roles per service account follows the principle of least privilege and is the recommended approach for EKS workloads.
- **INCORRECT:** "Create separate IAM policies... Attach both policies to the IAM role associated with the EC2 instance profile..." is incorrect — this grants all pods on the node access to both services.
- **INCORRECT:** "Create IAM roles... using a shared service account" is incorrect — a shared service account cannot enforce per-pod IAM role separation.
- **INCORRECT:** "Configure RBAC... Use Kubernetes ConfigMaps to store IAM credentials" is incorrect — storing IAM credentials in ConfigMaps is a security anti-pattern.

**References:**
- https://docs.aws.amazon.com/eks/latest/userguide/iam-roles-for-service-accounts.html
- https://docs.aws.amazon.com/eks/latest/userguide/associate-service-account-role.html
- https://digitalcloud.training/aws-iam/

---

### Question 52 (a)

**Q:** A company is migrating from an on-premises infrastructure to the AWS Cloud. One of the company's applications stores files on a Windows file server farm that uses Distributed File System Replication (DFSR) to keep data in sync. What service should the company use?

**Options:**

- AWS Storage Gateway
- Amazon EFS
- Amazon S3
- **✅ Amazon FSx**

**A:** **Amazon FSx**

**Explanation:**

Amazon FSx for Windows File Server provides fully managed, highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol. Amazon FSx is built on Windows Server and supports Distributed File System Replication (DFSR) in Single-AZ deployments.

- **CORRECT:** "Amazon FSx" is the correct answer.
- **INCORRECT:** "Amazon EFS" is incorrect — EFS only supports Linux systems.
- **INCORRECT:** "Amazon S3" is incorrect — this is not a suitable replacement for a Microsoft filesystem.
- **INCORRECT:** "AWS Storage Gateway" is incorrect — this service is primarily used for connecting on-premises storage to cloud storage.

**References:**
- https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html
- https://digitalcloud.training/amazon-fsx/

---

### Question 1

**Q:** A company wants to migrate a legacy web application from an on-premises data center to AWS. The web application consists of a web tier, an application tier, and a MySQL database. The company does not want to manage servers or operating systems. Which two services should the Solutions Architect choose? *(Select TWO)*

**Options:**

- Amazon Kinesis Data Streams
- Amazon DynamoDB
- Amazon EC2 Spot Instances
- **✅ Amazon RDS for MySQL**
- **✅ AWS Fargate**

**A:** **Amazon RDS for MySQL** and **AWS Fargate**

**Explanation:**

Amazon RDS is a managed service — you do not need to manage the underlying instances. It is an ideal backend for the application and can run a MySQL database without any refactoring. For the application tier, AWS Fargate is a serverless compute engine for containers that removes the need to manage EC2 instances.

- **CORRECT:** "AWS Fargate" is a correct answer.
- **CORRECT:** "Amazon RDS for MySQL" is also a correct answer.
- **INCORRECT:** "Amazon DynamoDB" is incorrect — this is a NoSQL database and is incompatible with the relational MySQL DB.
- **INCORRECT:** "Amazon EC2 Spot Instances" is incorrect — this would require managing instances.
- **INCORRECT:** "Amazon Kinesis Data Streams" is incorrect — this is a service for streaming data.

**References:**
- https://aws.amazon.com/rds/
- https://aws.amazon.com/fargate/
- https://digitalcloud.training/amazon-ecs-and-eks/
- https://digitalcloud.training/amazon-rds/

---

### Question 52 (b)

**Q:** An application running on Amazon ECS processes data and then writes objects to an Amazon S3 bucket. The application requires permissions to make the S3 API calls. How can a Solutions Architect enable access to S3?

**Options:**

- Create a set of Access Keys with read/write permissions to the bucket and update the task credential ID.
- Update the S3 policy in IAM to allow read/write access from Amazon ECS, and then relaunch the container.
- Attach an IAM policy with read/write permissions to the bucket to an IAM group and add the container instances to the group.
- **✅ Create an IAM role that has read/write permissions to the bucket and update the task definition to specify the role as the taskRoleArn.**

**A:** **Create an IAM role that has read/write permissions to the bucket and update the task definition to specify the role as the taskRoleArn.**

**Explanation:**

With IAM roles for Amazon ECS tasks, you can specify an IAM role that can be used by the containers in a task. You define the IAM role to use in your task definitions, or you can use a `taskRoleArn` override when running a task manually with the RunTask API operation.

- **CORRECT:** "Create an IAM role that has read/write permissions to the bucket and update the task definition to specify the role as the taskRoleArn" is the correct answer.
- **INCORRECT:** "Update the S3 policy in IAM to allow read/write access from Amazon ECS..." is incorrect — policies must be assigned to tasks using IAM Roles.
- **INCORRECT:** "Create a set of Access Keys... and update the task credential ID" is incorrect — you cannot update the task credential ID with access keys.
- **INCORRECT:** "Attach an IAM policy... to an IAM group and add the container instances to the group" is incorrect — you cannot add container instances to an IAM group.

**References:**
- https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-iam-roles.html
- https://digitalcloud.training/amazon-ecs-and-eks/

---

### Question 40

**Q:** IAM permissions-related Access Denied errors and Unauthorized errors need to be analyzed and troubleshooted by a company. AWS CloudTrail has been enabled at the company. Which solution will meet these requirements most operationally efficiently?

**Options:**

- Write custom scripts to query CloudTrail logs using AWS Glue.
- Search CloudTrail logs with Amazon Redshift. Create a dashboard to identify the errors.
- Create a custom script and execute it against CloudTrail logs to find errors using AWS Batch.
- **✅ Search CloudTrail logs with Amazon QuickSight. Create a dashboard to identify the errors.**

**A:** **Search CloudTrail logs with Amazon QuickSight. Create a dashboard to identify the errors.**

**Explanation:**

CloudTrail logs are stored natively within an S3 bucket, which can then be easily integrated with Amazon QuickSight. Amazon QuickSight is a data visualization tool that can display any IAM permissions-related errors in a simple dashboard.

- **CORRECT:** "Search CloudTrail logs with Amazon QuickSight. Create a dashboard to identify the errors" is the correct answer.
- **INCORRECT:** "Create a custom script and execute it against CloudTrail logs using AWS Batch" is incorrect — writing custom scripts is more effort than using native tools.
- **INCORRECT:** "Search CloudTrail logs with Amazon Redshift. Create a dashboard to identify the errors" is incorrect — Amazon Redshift is not a simple way of achieving this outcome.
- **INCORRECT:** "Write custom scripts to query CloudTrail logs using AWS Glue" is incorrect — AWS Glue and custom scripts add unnecessary complexity.

**References:**
- https://docs.aws.amazon.com/quicksight/latest/user/logging-using-cloudtrail.html
- https://digitalcloud.training/aws-analytics-services/

---

### Question 41

**Q:** An application is running in a private subnet of an Amazon VPC and must have outbound internet access for downloading updates. The Solutions Architect does not want the application exposed to inbound connection attempts. Which steps should be taken?

**Options:**

- Attach an internet gateway to the private subnet and create a NAT gateway.
- Create a NAT gateway but do not attach an internet gateway to the VPC.
- Attach an internet gateway to the VPC but do not create a NAT gateway.
- **✅ Create a NAT gateway and attach an internet gateway to the VPC.**

**A:** **Create a NAT gateway and attach an internet gateway to the VPC.**

**Explanation:**

To enable outbound connectivity for instances in private subnets, a NAT gateway can be created. The NAT gateway is created in a public subnet and a route must be created in the private subnet pointing to the NAT gateway. An internet gateway must also be attached to the VPC. Instances in a private subnet cannot be directly reached from the internet, so the application will not be exposed to inbound connections.

- **CORRECT:** "Create a NAT gateway and attach an internet gateway to the VPC" is the correct answer.
- **INCORRECT:** "Create a NAT gateway but do not attach an internet gateway to the VPC" is incorrect — an internet gateway must be attached to the VPC for any outbound connections to work.
- **INCORRECT:** "Attach an internet gateway to the private subnet and create a NAT gateway" is incorrect — internet gateways are attached to VPCs, not subnets.
- **INCORRECT:** "Attach an internet gateway to the VPC but do not create a NAT gateway" is incorrect — without a NAT gateway, instances in the private subnet will not be able to download updates.

**References:**
- https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- https://digitalcloud.training/amazon-vpc/

---

### Question 48

**Q:** A large company is currently using multiple AWS accounts as part of its cloud deployment model, and these accounts are currently structured using AWS Organizations. A Solutions Architect has been tasked with ensuring that only accounts within AWS Organizations can access a specific Amazon S3 bucket. What is the most operationally efficient way to achieve this?

**Options:**

- Add all the non-organizational accounts to an Organizational Unit (OU) and attach a Service Control Policy (SCP) which denies access to the specific Amazon S3 bucket.
- Use AWS Config and AWS Lambda functions to make remediations to the bucket policy as and when new accounts are created and tagged as not being part of AWS Organizations.
- Use Attribute Based Access Control by referencing Tags of accounts which are either enrolled as part of AWS Organizations, or not.
- **✅ Use the global key of AWS Organizations within a bucket policy using the aws:PrincipalOrgID key to allow access only to accounts which are part of the Organization.**

**A:** **Use the global key of AWS Organizations within a bucket policy using the aws:PrincipalOrgID key to allow access only to accounts which are part of the Organization.**

**Explanation:**

The `aws:PrincipalOrgID` global key provides a simpler alternative to manually listing and updating all the account IDs for all AWS accounts that exist within an Organization. It can be used directly in an S3 bucket policy to restrict access.

- **CORRECT:** "Use the global key of AWS Organizations within a bucket policy using the aws:PrincipalOrgID key..." is the correct answer.
- **INCORRECT:** "Use Attribute Based Access Control by referencing Tags..." is incorrect — while viable, it is more complex and less efficient.
- **INCORRECT:** "Use AWS Config and AWS Lambda functions to make remediations..." is incorrect — this adds unnecessary operational overhead.
- **INCORRECT:** "Add all the non-organizational accounts to an OU and attach a Service Control Policy (SCP)..." is incorrect — SCPs apply to accounts within the Organization, not to external accounts.

**References:**
- https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html
- https://digitalcloud.training/aws-organizations/

---

### Question 12

**Q:** A systems administrator of a company wants to detect and remediate the compromise of services such as Amazon EC2 instances and Amazon S3 buckets. Which AWS service can the administrator use to meet this requirement?

**Options:**

- Amazon Macie
- Amazon Inspector
- Amazon Cognito
- **✅ Amazon GuardDuty**

**A:** **Amazon GuardDuty**

**Explanation:**

Amazon GuardDuty gives you access to built-in detection techniques that are developed and optimized for the cloud. It offers HTTPS APIs, CLI tools, and Amazon CloudWatch Events to support automated security responses to security findings.

- **CORRECT:** "Amazon GuardDuty" is the correct answer.
- **INCORRECT:** "Amazon Cognito" is incorrect — Cognito provides sign-up and sign-in services for mobile apps.
- **INCORRECT:** "Amazon Inspector" is incorrect — Inspector identifies vulnerabilities and evaluates against security best practices, but does not detect active compromise.
- **INCORRECT:** "Amazon Macie" is incorrect — Macie is used for detecting and protecting sensitive data stored in Amazon S3.