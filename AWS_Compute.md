Question 1Skipped
Domain
AWS Compute
Question 6Skipped
A Microsoft Windows file server farm uses Distributed File System Replication (DFSR) to synchronize data in an on-premises environment. The infrastructure is being migrated to the AWS Cloud.
Which service should the solutions architect use to replace the file server farm?
Amazon EFS
AWS Storage Gateway
Amazon EBS
Correct answer
Amazon FSx
Overall explanation
Amazon FSx for Windows file server supports DFS namespaces and DFS replication. This is the best solution for replacing the on-premises infrastructure. Note the limitations for deployment:


CORRECT: "Amazon FSx" is the correct answer.
INCORRECT: "Amazon EFS" is incorrect. You cannot replace a Windows file server farm with EFS as it uses a completely different protocol.
INCORRECT: "Amazon EBS" is incorrect. Amazon EBS provides block-based volumes that are attached to EC2 instances. It cannot be used for replacing a shared Windows file server farm using DFSR.
INCORRECT: "AWS Storage Gateway" is incorrect. This service is used for providing cloud storage solutions for on-premises servers. In this case the infrastructure is being migrated into the AWS Cloud.
References:
https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Compute
Question 13Skipped
A startup is prototyping a movie streaming platform on AWS. The platform consists of an Application Load Balancer, an Auto Scaling group of Amazon EC2 instances to host the frontend, and an Amazon RDS for PostgreSQL DB instance running in a Single-AZ configuration.
Users report slow response times when browsing the catalog of available movies. The movie catalog is a set of tables in the database that is updated infrequently. A solutions architect finds that the database's CPU utilization spikes significantly during catalog queries.
What should the solutions architect recommend to improve the performance of the platform during catalog searches?
Correct answer
Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache.
Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas.
Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora’s built-in caching to handle frequent queries efficiently.
Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog.
Overall explanation
Implement an Amazon ElastiCache for Redis cluster to cache catalog queries. Configure the application to use lazy loading to populate the cache: This is correct because ElastiCache provides a highly performant in-memory caching layer that can significantly reduce database load and response times for infrequently updated data like a product or movie catalog. Lazy loading ensures the cache is populated only when a query misses, reducing unnecessary overhead.
Migrate the movie catalog to Amazon DynamoDB and use the DynamoDB Accelerator (DAX) service to cache queries for the catalog: This is incorrect because migrating to DynamoDB introduces unnecessary complexity and operational overhead, especially for a relational workload that involves the movie catalog. DAX is designed for NoSQL databases and is not the best fit for this use case.
Enable read replicas for the RDS instance. Configure the frontend application to distribute catalog queries across the read replicas: This is incorrect because while read replicas can improve performance for read-heavy workloads, they do not reduce query latency as effectively as an in-memory caching solution like ElastiCache.
Use Amazon Aurora Serverless for the movie catalog database. Configure Aurora’s built-in caching to handle frequent queries efficiently: This is incorrect because switching to Aurora Serverless would involve significant changes to the database architecture. While Aurora provides caching, ElastiCache is specifically optimized for high-performance caching use cases.
References:
https://aws.amazon.com/elasticache/
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-elasticache/
Domain
AWS Compute
Question 21Skipped
A surveying team is using a fleet of drones to collect images of construction sites. The surveying team's laptops lack the inbuilt storage and compute capacity to transfer the images and process the data. While the team has Amazon EC2 instances for processing and Amazon S3 buckets for storage, network connectivity is intermittent and unreliable. The images need to be processed to evaluate the progress of each construction site.
What should a solutions architect recommend?
Configure Amazon Kinesis Data Firehose to create multiple delivery streams aimed separately at the S3 buckets for storage and the EC2 instances for processing the images.
During intermittent connectivity to EC2 instances, upload images to Amazon SQS.
Correct answer
Process and store the images using AWS Snowball Edge devices.
Cache the images locally on a hardware appliance pre-installed with AWS Storage Gateway to process the images when connectivity is restored.
Overall explanation
AWS physical Snowball Edge device will provide much more inbuilt compute and storage compared to the current team’s laptops. This negates the need to rely on a stable connection to process any images and solves the team's problems easily and efficiently.
CORRECT: "Process and store the images using AWS Snowball Edge devices” is the correct answer (as explained above.)
INCORRECT: "During intermittent connectivity to EC2 instances, upload images to Amazon SQS” is incorrect as you would still need a reliable internet connection to upload any images to Amazon SQS.
INCORRECT: "Configure Amazon Kinesis Data Firehose to create multiple delivery streams aimed separately at the S3 buckets for storage and the EC2 instances for processing the images" is incorrect as you would still need a reliable internet connection to upload any images to the Amazon Kinesis Service.
INCORRECT: "Cache the images locally on a hardware appliance pre-installed with AWS Storage Gateway to process the images when connectivity is restored” is incorrect as you would still need reliable internet connection to upload any images to the Amazon Storage Gateway service.
References:
https://docs.aws.amazon.com/snowball/latest/developer-guide/whatisedge.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/
Domain
AWS Compute
Question 24Skipped
A company uses an Amazon RDS MySQL database instance to store customer order data. The security team have requested that SSL/TLS encryption in transit must be used for encrypting connections to the database from application servers. The data in the database is currently encrypted at rest using an AWS KMS key.
How can a Solutions Architect enable encryption in transit?
Correct answer
Download the AWS-provided root certificates. Use the certificates when connecting to the RDS DB instance.
Add a self-signed certificate to the RDS DB instance. Use the certificates in all connections to the RDS DB instance.
Enable encryption in transit using the RDS Management console and obtain a key using AWS KMS.
Take a snapshot of the RDS instance. Restore the snapshot to a new instance with encryption in transit enabled.
Overall explanation
Amazon RDS creates an SSL certificate and installs the certificate on the DB instance when Amazon RDS provisions the instance. These certificates are signed by a certificate authority. The SSL certificate includes the DB instance endpoint as the Common Name (CN) for the SSL certificate to guard against spoofing attacks.
You can download a root certificate from AWS that works for all Regions or you can download Region-specific intermediate certificates.
CORRECT: "Download the AWS-provided root certificates. Use the certificates when connecting to the RDS DB instance" is the correct answer.
INCORRECT: "Take a snapshot of the RDS instance. Restore the snapshot to a new instance with encryption in transit enabled" is incorrect. There is no need to do this as a certificate is created when the DB instances is launched.
INCORRECT: "Enable encryption in transit using the RDS Management console and obtain a key using AWS KMS" is incorrect. You cannot enable/disable encryption in transit using the RDS management console or use a KMS key.
INCORRECT: "Add a self-signed certificate to the RDS DB instance. Use the certificates in all connections to the RDS DB instance" is incorrect. You cannot use self-signed certificates with RDS.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.SSL.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Compute
Question 27Skipped
A retail company operates a multi-tier application that includes a web server layer running on Amazon EC2 instances and a database layer hosted on Amazon RDS. The company is preparing for an annual sales event and anticipates a significant surge in traffic to its application. The operations team wants to monitor the performance of the EC2 instances and database, analyzing metrics with a granularity of 1 minute to ensure quick detection of bottlenecks during the event.
What should the solutions architect do to meet this requirement?
Configure Amazon CloudWatch Logs Insights to aggregate application logs for both the EC2 instances and Amazon RDS. Use Amazon QuickSight for detailed visualization.
Configure an Amazon CloudWatch Events rule to trigger an AWS Lambda function that collects custom metrics from the EC2 instances and Amazon RDS. Use Amazon CloudWatch dashboards to display the metrics.
Use AWS Systems Manager to collect logs from the EC2 instances and Amazon RDS. Store the logs in Amazon S3 and use Amazon Athena to query performance data.
Correct answer
Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics for analysis.
Overall explanation
Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics for analysis: This is the correct solution because detailed monitoring provides metrics at 1-minute intervals, which allows the operations team to quickly detect and analyze potential bottlenecks during the sales event. CloudWatch natively supports metrics for both EC2 and RDS.
Configure Amazon CloudWatch Logs Insights to aggregate application logs for both the EC2 instances and Amazon RDS. Use Amazon QuickSight for detailed visualization: This is incorrect because while Logs Insights is useful for log analysis, it does not directly provide 1-minute metric granularity required for real-time monitoring.
Configure an Amazon CloudWatch Events rule to trigger an AWS Lambda function that collects custom metrics from the EC2 instances and Amazon RDS. Use Amazon CloudWatch dashboards to display the metrics: This is incorrect because using CloudWatch detailed monitoring is a simpler and more efficient solution compared to creating custom metrics with Lambda.
Use AWS Systems Manager to collect logs from the EC2 instances and Amazon RDS. Store the logs in Amazon S3 and use Amazon Athena to query performance data: This is incorrect because this solution is not suitable for real-time monitoring and involves unnecessary operational overhead.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch.html
https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudwatch/
Domain
AWS Compute
Question 37Skipped
An Amazon S3 bucket in the us-east-1 Region hosts the static website content of a company. The content is made available through an Amazon CloudFront origin pointing to that bucket. A second copy of the bucket is created in the ap-southeast-1 Region using cross-region replication. The chief solutions architect wants a solution that provides greater availability for the website.
Which combination of actions should a solutions architect take to increase availability? (Select TWO.)
Correct selection
Using us-east-1 bucket as the primary bucket and ap-southeast-1 bucket as the secondary bucket, create a CloudFront origin group.
Create an origin for CloudFront for both buckets.
Set up failover routing in Amazon Route 53.
Correct selection
Add an origin for ap-southeast-1 to CloudFront.
Point Amazon Route 53 to the replica bucket by creating a record.
Overall explanation
You can set up CloudFront with origin failover for scenarios that require high availability. To get started, you create an origin group with two origins: a primary and a secondary. If the primary origin is unavailable or returns specific HTTP response status codes that indicate a failure, CloudFront automatically switches to the secondary origin.
CORRECT: "Add an origin for ap-southeast-1 to CloudFront” is the correct answer (as explained above.)
CORRECT: "Using us-east-1 bucket as the primary bucket and ap-southeast-1 bucket as the secondary bucket, create a CloudFront origin group” is also a correct answer (as explained above.)
INCORRECT: "Create an origin for CloudFront for both buckets” is incorrect. This would not increase the availability of the solution on its own.
INCORRECT: "Set up failover routing in Amazon Route 53” is incorrect as we are trying to enable failover in CloudFront and using Route 53 is for routing domain names.
INCORRECT: "Create a record in Amazon Route 53 pointing to the replica bucket" is incorrect as we are trying to enable failover in CloudFront and using Route 53 is for routing domain names.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Compute
Question 42Skipped
A company has developed a non-production application that is composed of multiple microservices for each of the company's business units. A single development team maintains all the microservices. The current architecture uses a static web frontend and a Java-based backend that contains the application logic. The architecture also uses a MySQL database that the company hosts on an Amazon EC2 instance. The company needs to ensure that the application is secure, scalable, and globally available while minimizing operational overhead.
Which solution will meet these requirements?
Use Amazon CloudFront and AWS Amplify to host the static web frontend. Refactor the backend to AWS Lambda functions triggered by an EventBridge bus. Migrate the database to an Amazon EC2 Reserved Instance with backups configured on Amazon S3.
Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend microservices to run on Amazon ECS on AWS Fargate. Migrate the database to Amazon DynamoDB for auto-scaling and cost optimization.
Correct answer
Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend to use AWS Lambda functions that are invoked by Amazon API Gateway. Migrate the database to Amazon Aurora Serverless for auto-scaling.
Use AWS Amplify to host the static web frontend. Refactor the backend microservices to Amazon Elastic Kubernetes Service (Amazon EKS) with auto-scaling. Migrate the database to Amazon RDS for MySQL with a read replica for high availability.
Overall explanation
Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend to use AWS Lambda functions that are invoked by Amazon API Gateway. Migrate the database to Amazon Aurora Serverless for auto-scaling:
This is correct because S3 and CloudFront provide secure, globally available hosting for the static frontend. AWS Lambda and API Gateway eliminate server management, and Aurora Serverless offers a cost-effective, auto-scaling database solution.
Use AWS Amplify to host the static web frontend. Refactor the backend microservices to Amazon Elastic Kubernetes Service (Amazon EKS) with auto-scaling. Migrate the database to Amazon RDS for MySQL with a read replica for high availability:
This is incorrect because using Amazon EKS adds operational complexity. Amplify is better suited for modern full-stack applications, not static web hosting.
Use Amazon CloudFront and Amazon S3 to host the static web frontend. Refactor the backend microservices to run on Amazon ECS on AWS Fargate. Migrate the database to Amazon DynamoDB for auto-scaling and cost optimization:
This is incorrect because moving a relational database to DynamoDB requires a complete redesign, which increases migration complexity and effort.
Use Amazon CloudFront and AWS Amplify to host the static web frontend. Refactor the backend to AWS Lambda functions triggered by an EventBridge bus. Migrate the database to an Amazon EC2 Reserved Instance with backups configured on Amazon S3:
This is incorrect because EventBridge adds unnecessary complexity to trigger Lambda functions. Hosting a database on an EC2 Reserved Instance increases operational overhead compared to managed database services.
References:

https://aws.amazon.com/s3/

https://aws.amazon.com/rds/aurora/serverless/
Domain
AWS Compute
Question 44Skipped
A logistics company processes real-time sensor data from delivery vehicles to optimize routes and track vehicle health. The current architecture includes an Auto Scaling group of Amazon EC2 instances for ingesting and storing sensor data, and a separate Auto Scaling group for analyzing and generating route optimizations based on this data.
The company has observed performance issues during peak delivery hours when the rate of data ingestion is significantly higher than the analysis and processing rate. The company wants to ensure that both systems can scale independently, and no data is lost during scaling events.
Which solution will meet these requirements?
Correct answer
Use two Amazon Simple Queue Service (Amazon SQS) queues: one for data ingestion and one for route analysis. Configure the EC2 instances to poll their respective queues and scale the Auto Scaling groups based on the ApproximateNumberOfMessages metric in each queue.
Replace the EC2-based Auto Scaling groups with AWS Lambda functions to process the incoming data and analysis tasks. Use Amazon DynamoDB to store the intermediate data and scale DynamoDB based on the traffic patterns.
Use two Amazon SQS queues: one for data ingestion and one for route analysis. Configure Amazon EventBridge rules to monitor queue length and scale each Auto Scaling group based on the backlog of messages in their respective queues.
Use Amazon Kinesis Data Streams to buffer the sensor data. Configure Amazon Kinesis Data Analytics to process the data and adjust the number of EC2 instances in the analysis Auto Scaling group based on the volume of data being processed.
Overall explanation
Use two Amazon Simple Queue Service (Amazon SQS) queues: one for data ingestion and one for route analysis. Configure the EC2 instances to poll their respective queues and scale the Auto Scaling groups based on the ApproximateNumberOfMessages metric in each queue: This is correct because SQS decouples the ingestion and analysis processes, ensuring no data is lost during traffic spikes. Scaling the Auto Scaling groups based on the queue length allows for efficient scaling that matches the workload demand for each process.
Replace the EC2-based Auto Scaling groups with AWS Lambda functions to process the incoming data and analysis tasks. Use Amazon DynamoDB to store the intermediate data and scale DynamoDB based on the traffic patterns: This is incorrect because replacing EC2 instances with Lambda introduces architectural changes and operational overhead. Additionally, DynamoDB is not required when SQS provides an efficient decoupling mechanism.
Use Amazon Kinesis Data Streams to buffer the sensor data. Configure Amazon Kinesis Data Analytics to process the data and adjust the number of EC2 instances in the analysis Auto Scaling group based on the volume of data being processed: This is incorrect because Kinesis introduces additional complexity and costs and is not necessary for this use case. SQS already provides buffering and scaling capabilities tailored to this scenario.
Use two Amazon SQS queues: one for data ingestion and one for route analysis. Configure Amazon EventBridge rules to monitor queue length and scale each Auto Scaling group based on the backlog of messages in their respective queues: This is incorrect because EventBridge is not the optimal mechanism for scaling Auto Scaling groups. Scaling directly based on SQS metrics is simpler and more efficient for managing workloads in this scenario.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Compute
Question 47Skipped
A financial services company stores transaction records in an Amazon S3 bucket. The company runs its analytics application on a cluster of on-premises servers. The application needs temporary, secure access to the S3 bucket to analyze the data files.
The company uses AWS IAM Identity Center to manage identities and ensure adherence to the principle of least privilege. The solution must avoid long-term credential storage and provide a secure method for the application to access the S3 bucket.
Which solution will meet these requirements?
Use AWS Systems Manager to store an access key and secret key for an IAM user with access to the S3 bucket. Configure the application to retrieve the credentials from Systems Manager Parameter Store when needed.
Create an S3 bucket policy to allow access from the public IP address range of the company’s on-premises servers. Configure the application to access the S3 bucket directly.
Deploy AWS Storage Gateway File Gateway to the on-premises environment. Configure the application to access the S3 bucket through the gateway by using NFS or SMB.
Correct answer
Use IAM Roles Anywhere to issue temporary credentials to the application. Set up a trust relationship with IAM Identity Center and configure the application to assume the role using these credentials.
Overall explanation
Use IAM Roles Anywhere to issue temporary credentials to the application. Set up a trust relationship with IAM Identity Center and configure the application to assume the role using these credentials: This is correct because IAM Roles Anywhere provides a secure and scalable method for on-premises workloads to obtain temporary AWS credentials. It avoids the use of long-term credentials and integrates with IAM Identity Center to ensure least privilege access to the S3 bucket.
Create an S3 bucket policy to allow access from the public IP address range of the company’s on-premises servers. Configure the application to access the S3 bucket directly: This is incorrect because opening access to a public IP address range is less secure and does not align with the principle of least privilege. It exposes the S3 bucket to potential security risks.
Deploy AWS Storage Gateway File Gateway to the on-premises environment. Configure the application to access the S3 bucket through the gateway by using NFS or SMB: This is incorrect because while File Gateway can provide access to S3, it is designed for file-based workloads and adds unnecessary complexity for this use case. IAM Roles Anywhere is a simpler and more secure option for temporary credentials.
Use AWS Systems Manager to store an access key and secret key for an IAM user with access to the S3 bucket. Configure the application to retrieve the credentials from Systems Manager Parameter Store when needed: This is incorrect because storing long-term credentials in Parameter Store introduces security risks. Temporary credentials from IAM Roles Anywhere are a more secure and compliant solution.
References:
https://docs.aws.amazon.com/rolesanywhere/latest/userguide/introduction.html
https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Compute
Question 51Skipped
A research organization wants to set up an Amazon EMR cluster for multiple departments to run their big data analytics jobs. The organization needs to ensure that each department’s workloads can access only the specific AWS services required for their analysis. Additionally, the organization wants to block access to Instance Metadata Service Version 2 (IMDSv2) on the EMR cluster's underlying EC2 instances.
Which solution will meet these requirements?
Configure VPC interface endpoints for each AWS service that the departments require. Route traffic from the big data workloads through these VPC endpoints.
Create an EMR security configuration that disables access to the Instance Metadata Service. Use this security configuration with application-specific IAM roles to submit the workloads.
Assign unique EC2 IAM instance profiles to each team’s workloads. Configure the instance profiles with the specific permissions needed for each department.
Correct answer
Use EMR runtime roles to enforce granular permissions for each department's workloads. Configure the EMR cluster to use these roles when submitting jobs.
Overall explanation
Use EMR runtime roles to enforce granular permissions for each department's workloads. Configure the EMR cluster to use these roles when submitting jobs: This is correct because EMR runtime roles allow fine-grained access control for individual workloads without exposing permissions at the instance level. Runtime roles are scoped specifically to applications, reducing the risk of unnecessary access.
Configure VPC interface endpoints for each AWS service that the departments require. Route traffic from the big data workloads through these VPC endpoints: This is incorrect because while VPC interface endpoints can restrict network access, they do not enforce permissions at the application level or prevent access to IMDSv2.
Assign unique EC2 IAM instance profiles to each team’s workloads. Configure the instance profiles with the specific permissions needed for each department: This is incorrect because instance profiles provide permissions at the instance level rather than the workload level. This does not ensure workload isolation or restrict access to IMDSv2.
Create an EMR security configuration that disables access to the Instance Metadata Service. Use this security configuration with application-specific IAM roles to submit the workloads: This is incorrect because EMR security configurations do not directly provide granular access control for individual workloads. While security configurations can restrict metadata access, they cannot enforce permissions per workload.
References:
https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-iam-roles.html
https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-security-configuration.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-emr/
Domain
AWS Compute
Question 60Skipped
A media processing company is migrating its on-premises application to the AWS Cloud. The application processes high volumes of videos and generates large output files during the workflow.
The company requires a scalable solution to handle an increasing number of video processing jobs. The solution should minimize manual intervention, simplify job orchestration, and eliminate the need to manage infrastructure. Operational overhead must be kept to a minimum.
Which solution will fulfill these requirements with the LEAST operational overhead?
Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate to process the videos. Use Amazon Simple Queue Service (Amazon SQS) for workflow orchestration and store the processed files in Amazon S3.
Correct answer
Use AWS Batch to run video processing jobs. Use AWS Step Functions to manage the workflow. Store the processed files in Amazon S3.
Use AWS Lambda and Amazon EC2 On-Demand Instances for video processing. Store the processed files in Amazon FSx for Lustre.
Use a fleet of Amazon EC2 Spot Instances to process the videos. Use AWS Step Functions for workflow management and store the processed files in Amazon Elastic File System (Amazon EFS).
Overall explanation
Use AWS Batch to run video processing jobs. Use AWS Step Functions to manage the workflow. Store the processed files in Amazon S3: This is correct because AWS Batch automatically manages the underlying infrastructure, scales based on workload and simplifies batch job management. Combining this with AWS Step Functions enables efficient orchestration of workflows. Storing the processed files in Amazon S3 provides durability and scalability, which is ideal for managing large files. This solution minimizes operational overhead by leveraging fully managed services.
Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate to process the videos. Use Amazon Simple Queue Service (Amazon SQS) for workflow orchestration and store the processed files in Amazon S3: This is incorrect because, while Fargate reduces infrastructure management, integrating SQS for workflow orchestration adds complexity compared to using AWS Step Functions. AWS Batch provides more specialized functionality for processing batch workloads.
Use AWS Lambda and Amazon EC2 On-Demand Instances for video processing. Store the processed files in Amazon FSx for Lustre: This is incorrect because combining Lambda with EC2 adds complexity to infrastructure management and does not fully eliminate operational overhead. Additionally, FSx for Lustre is more suitable for high-performance computing scenarios rather than general-purpose storage of processed files.
Use a fleet of Amazon EC2 Spot Instances to process the videos. Use AWS Step Functions for workflow management and store the processed files in Amazon Elastic File System (Amazon EFS): This is incorrect because Spot Instances are not ideal for workflows that must minimize interruptions, as they can be terminated unexpectedly. AWS Batch is a more suitable solution for managing job processing workloads with minimal operational overhead.
References:
https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html
https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html
Domain
AWS Compute
Question 61Skipped
An eCommerce application consists of three tiers. The web tier includes EC2 instances behind an Application Load balancer, the middle tier uses EC2 instances and an Amazon SQS queue to process orders, and the database tier consists of an Auto Scaling DynamoDB table. During busy periods customers have complained about delays in the processing of orders. A Solutions Architect has been tasked with reducing processing times.
Which action will be MOST effective in accomplishing this requirement?
Correct answer
Use Amazon EC2 Auto Scaling to scale out the middle tier instances based on the SQS queue depth.
Replace the Amazon SQS queue with Amazon Kinesis Data Firehose.
Use Amazon DynamoDB Accelerator (DAX) in front of the DynamoDB backend tier.
Add an Amazon CloudFront distribution with a custom origin to cache the responses for the web tier.
Overall explanation
The most likely cause of the processing delays is insufficient instances in the middle tier where the order processing takes place. The most effective solution to reduce processing times in this case is to scale based on the backlog per instance (number of messages in the SQS queue) as this reflects the amount of work that needs to be done.
CORRECT: "Use Amazon EC2 Auto Scaling to scale out the middle tier instances based on the SQS queue depth" is the correct answer.
INCORRECT: "Replace the Amazon SQS queue with Amazon Kinesis Data Firehose" is incorrect. The issue is not the efficiency of queuing messages but the processing of the messages. In this case scaling the EC2 instances to reflect the workload is a better solution.
INCORRECT: "Use Amazon DynamoDB Accelerator (DAX) in front of the DynamoDB backend tier" is incorrect. The DynamoDB table is configured with Auto Scaling so this is not likely to be the bottleneck in order processing.
INCORRECT: "Add an Amazon CloudFront distribution with a custom origin to cache the responses for the web tier" is incorrect. This will cache media files to speed up web response times but not order processing times as they take place in the middle tier.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Compute
Question 6Skipped
A gaming company operates a leaderboard application for a popular multiplayer game. The application uses an Amazon Aurora PostgreSQL DB cluster for storage. The game servers, hosted on Amazon EC2 instances, frequently update the leaderboard with player scores.
The company has a strict security policy that requires database credentials to be encrypted and rotated every 30 days. The company wants to minimize operational overhead while ensuring the application can seamlessly retrieve and use updated credentials.
What should a solutions architect do to meet this requirement?
Use AWS Systems Manager Parameter Store to store the database credentials as SecureString parameters encrypted with AWS KMS. Implement a custom AWS Lambda function to rotate the credentials every 30 days and update the parameters.
Correct answer
Use AWS Secrets Manager to store the database credentials. Configure Secrets Manager to rotate the credentials automatically every 30 days. Update the game server application to retrieve credentials from Secrets Manager.
Configure Amazon Cognito to generate temporary database credentials. Use Cognito's built-in mechanisms to rotate the credentials every 30 days. Update the game server application to request temporary credentials from Cognito.
Store the database credentials in an Amazon DynamoDB table encrypted with AWS KMS. Configure an AWS Lambda function to rotate the credentials in Aurora every 30 days and update the DynamoDB table with the new credentials.
Overall explanation
Use AWS Secrets Manager to store the database credentials. Configure Secrets Manager to rotate the credentials automatically every 30 days. Update the game server application to retrieve credentials from Secrets Manager: This is correct because AWS Secrets Manager integrates seamlessly with Aurora PostgreSQL, providing built-in credential rotation and secure storage. This minimizes operational overhead and meets the security requirements.
Use AWS Systems Manager Parameter Store to store the database credentials as SecureString parameters encrypted with AWS KMS. Implement a custom AWS Lambda function to rotate the credentials every 30 days and update the parameters: This is incorrect because while Parameter Store securely stores credentials, it does not natively integrate with Aurora for automatic rotation. Writing a custom Lambda function increases complexity.
Configure Amazon Cognito to generate temporary database credentials. Use Cognito's built-in mechanisms to rotate the credentials every 30 days. Update the game server application to request temporary credentials from Cognito: This is incorrect because Cognito is primarily designed for user identity management and is not intended for database credential management. This approach does not directly address the security requirements.
Store the database credentials in an Amazon DynamoDB table encrypted with AWS KMS. Configure an AWS Lambda function to rotate the credentials in Aurora every 30 days and update the DynamoDB table with the new credentials: This is incorrect because DynamoDB is not a service designed to securely store or manage database credentials. This approach requires unnecessary custom implementations and adds operational complexity.
References:
https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html
https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-secrets-manager/
Domain
AWS Compute
Question 10Skipped
A company runs an internal application for logging customer support information. The application runs on Amazon EC2 instances in an Auto Scaling group. The ASG scales up to 10 instances during business hours and scales down to 2 instances overnight. Staff have complained of poor performance at the beginning of the business day.
How should a Solutions Architect configure the Auto Scaling group to resolve the performance issues whilst minimizing costs?
Implement a scheduled action that sets the minimum and maximum capacity to 10 before business hours begin.
Correct answer
Implement a scheduled action that sets the desired capacity to 10 before business hours begin.
Implement a target tracking action with a lower CPU threshold, and decrease the cooldown period.
Implement a step scaling action with a lower CPU threshold and decrease the cooldown period.
Overall explanation
Scheduled scaling allows you to set your own scaling schedule. In this example it means the Solutions Architect can configure the scaling action to take place shortly before business hours begin and that will ensure adequate capacity exists from the very beginning of the business day.
In this example below the scheduled scaling policy is configured to scale at 08:45am daily with a desired count of 15. This will result in 15 instances being available shortly after.

CORRECT: "Implement a scheduled action that sets the desired capacity to 10 before business hours begin" is the correct answer.
INCORRECT: "Implement a scheduled action that sets the minimum and maximum capacity to 10 before business hours begin" is incorrect. The minimum and maximums define how many instances CAN run; the desired capacity sets how many you WANT to be running.
INCORRECT: "Implement a step scaling action with a lower CPU threshold and decrease the cooldown period" is incorrect. A cooldown period will result in faster scaling and a lower CPU threshold will cause scaling to happen at a lower loads. However, there is still a lag time before the instances are available to service users and this could result in too many instances running for the rest of the day.
INCORRECT: "Implement a target tracking action with a lower CPU threshold, and decrease the cooldown period" is incorrect. As above, this may achieve faster scaling at lower loads but is also going to be higher cost and applications may still not be ready for the beginning of the business day.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Compute
Question 11Skipped
A data analytics company is testing a Python-based application that processes customer data on an Amazon EC2 Linux instance. A single 1 TB Amazon Elastic Block Store (Amazon EBS) General Purpose SSD (gp3) volume is currently attached to the EC2 instance for data storage.
The company plans to deploy the application across multiple EC2 instances in an Auto Scaling group. All instances must access the same data that is currently stored on the EBS volume. The company needs a highly available and cost-effective solution that minimizes changes to the application code.
Which solution will meet these requirements?
Correct answer
Use Amazon Elastic File System (Amazon EFS) and configure it in General Purpose performance mode. Mount the EFS file system on all EC2 instances.
Configure an Amazon FSx for Lustre file system. Integrate the file system with Amazon S3 and mount it on each EC2 instance for shared access.
Create an EC2 instance to act as an NFS server. Attach the EBS volume to this instance and share the volume with other EC2 instances in the Auto Scaling group.
Provision Amazon S3 and use the S3 REST API to allow all EC2 instances to upload and download data from the S3 bucket.
Overall explanation
Use Amazon Elastic File System (Amazon EFS) and configure it in General Purpose performance mode. Mount the EFS file system on all EC2 instances: This is correct because Amazon EFS is a highly available, scalable, and resilient shared storage solution. It allows multiple EC2 instances to access the same data concurrently without requiring changes to the application code. General Purpose performance mode ensures low latency for shared access workloads.
Configure an Amazon FSx for Lustre file system. Integrate the file system with Amazon S3 and mount it on each EC2 instance for shared access: This is incorrect because FSx for Lustre is designed for high-performance computing and temporary storage for large-scale workloads. It does not provide the same level of availability and resilience for long-term storage as Amazon EFS.
Create an EC2 instance to act as an NFS server. Attach the EBS volume to this instance and share the volume with other EC2 instances in the Auto Scaling group: This is incorrect because using a single EC2 instance as an NFS server introduces a single point of failure, which reduces availability. EFS provides a more resilient and scalable solution.
Provision Amazon S3 and use the S3 REST API to allow all EC2 instances to upload and download data from the S3 bucket: This is incorrect because Amazon S3 is an object storage service, not a file system. It requires significant changes to the application to handle S3 API calls, which increases operational complexity.
References:
https://aws.amazon.com/efs/
https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/
Domain
AWS Compute
Question 19Skipped
A retail company is migrating its supply chain application to Amazon Elastic Kubernetes Service (Amazon EKS). The company requires pods in the EKS cluster to use custom subnets in its existing VPC. Additionally, the pods must securely communicate with other resources within the VPC, while adhering to compliance requirements.
Which solution will meet these requirements?
Set up AWS Transit Gateway to manage the routing between custom subnets and the EKS pods for secure communication within the VPC.
Correct answer
Use the Amazon VPC CNI plugin for Kubernetes. Configure the custom subnets in the VPC and associate the subnets with the EKS cluster to allow pods to use them.
Define Kubernetes network policies that enforce pod placement on specific nodes residing in the custom subnets within the VPC.
Configure an AWS Site-to-Site VPN between the custom subnets and the EKS cluster to enable secure communication for the pods.
Overall explanation
Use the Amazon VPC CNI plugin for Kubernetes. Configure the custom subnets in the VPC and associate the subnets with the EKS cluster to allow pods to use them: This is correct because the Amazon VPC CNI plugin allows EKS pods to receive IP addresses from the specified custom subnets within the VPC. This ensures that the pods can securely communicate with other resources in the VPC.
Set up AWS Transit Gateway to manage the routing between custom subnets and the EKS pods for secure communication within the VPC: This is incorrect because AWS Transit Gateway is primarily used for connecting multiple VPCs or on-premises networks. It is not needed for pod-level subnet configuration within a single VPC.
Configure an AWS Site-to-Site VPN between the custom subnets and the EKS cluster to enable secure communication for the pods: This is incorrect because the VPC and EKS cluster are already within the same AWS environment, and a VPN is unnecessary for communication within the same VPC.
Define Kubernetes network policies that enforce pod placement on specific nodes residing in the custom subnets within the VPC: This is incorrect because Kubernetes network policies are used to control traffic flow between pods, not to configure subnet usage for pods.
References:
https://docs.aws.amazon.com/eks/latest/userguide/pod-networking.html
https://aws.amazon.com/blogs/containers/introducing-eks-vpc-cni-custom-network-configuration/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 24Skipped
A company is architecting a shared storage solution for an AWS-hosted gaming application. The company needs the ability to use Lustre clients to access data. The solution must be fully managed.
Which solution meets these requirements?
Assign the AWS DataSync task to share the data as a mountable file system. Sync the file system with the application server.
Create an Amazon Elastic File System (Amazon EFS) file system and configure it to support Lustre. Attach the file system to the origin server. Connect the application server to the file system.
Create a file gateway with AWS Storage Gateway. Create a client-side file share using the required protocol. Share the file with the application server.
Correct answer
Create an Amazon FSx for Lustre file system. Connect the file system to the origin server. Ensure that the file system is connected to the application server.
Overall explanation
Amazon FSx for Lustre provides fully managed shared storage with the scalability and performance of the popular Lustre file system. It is fully managed and will allow the company to attach the file system to the origin server and connect the application server to the file system.

CORRECT: "Create an Amazon FSx for Lustre file system. Connect the file system to the origin server. Ensure that the file system is connected to the application server” is the correct answer (as explained above.)
INCORRECT: "Assign the AWS DataSync task to share the data as a mountable file system. Sync the file system with the application server” is incorrect. The solution requires a managed Lustre file system, so this would not work.
INCORRECT: "Create a file gateway with AWS Storage Gateway. Create a client-side file share using the required protocol. Share the file with the application server” is incorrect. The solution requires a managed Lustre file system, so this would not work.
INCORRECT: "Create an Amazon Elastic File System (Amazon EFS) file system and configure it to support Lustre. Attach the file system to the origin server. Connect the application server to the file system” is incorrect. The solution requires a managed Lustre file system, so this would not work.
References:
https://aws.amazon.com/fsx/lustre/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Compute
Question 28Skipped
A website runs on Amazon EC2 instances behind an Application Load Balancer (ALB). The website’s DNS records are hosted in Amazon Route 53 with the domain name pointing to the ALB. A solution is required for displaying a static error page if the website becomes unavailable.
Which configuration should a solutions architect use to meet these requirements with the LEAST operational overhead?
Set up a Route 53 active-active configuration with the ALB and an Amazon EC2 instance hosting a static error page as endpoints. Route 53 will only send requests to the instance if the health checks fail for the ALB
Create a Route 53 weighted routing policy. Create a static website using an Amazon S3 bucket that hosts a static error page. Configure the record for the S3 static website with a weighting of zero. When an issue occurs increase the weighting
Correct answer
Create a Route 53 alias record for an Amazon CloudFront distribution and specify the ALB as the origin. Create custom error pages for the distribution
Create a Route 53 active-passive failover configuration. Create a static website using an Amazon S3 bucket that hosts a static error page. Configure the static website as the passive record for failover
Overall explanation
Using Amazon CloudFront as the front-end provides the option to specify a custom message instead of the default message. To specify the specific file that you want to return and the errors for which the file should be returned, you update your CloudFront distribution to specify those values.
For example, the following is a customized error message:

The CloudFront distribution can use the ALB as the origin, which will cause the website content to be cached on the CloudFront edge caches.
This solution represents the most operationally efficient choice as no action is required in the event of an issue, other than troubleshooting the root cause.
CORRECT: "Create a Route 53 alias record for an Amazon CloudFront distribution and specify the ALB as the origin. Create custom error pages for the distribution" is the correct answer.
INCORRECT: "Create a Route 53 active-passive failover configuration. Create a static website using an Amazon S3 bucket that hosts a static error page. Configure the static website as the passive record for failover" is incorrect. This option does not represent the lowest operational overhead as manual intervention would be required to cause a fail-back to the main website.
INCORRECT: "Create a Route 53 weighted routing policy. Create a static website using an Amazon S3 bucket that hosts a static error page. Configure the record for the S3 static website with a weighting of zero. When an issue occurs increase the weighting" is incorrect. This option requires manual intervention and there would be a delay from the issue arising before an administrative action could make the changes.
INCORRECT: "Set up a Route 53 active-active configuration with the ALB and an Amazon EC2 instance hosting a static error page as endpoints. Route 53 will only send requests to the instance if the health checks fail for the ALB" is incorrect. With an active-active configuration traffic would be split between the website and the error page.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/custom-error-pages.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Compute
Question 35Skipped
A web application is deployed in multiple regions behind an ELB Application Load Balancer. You need deterministic routing to the closest region and automatic failover. Traffic should traverse the AWS global network for consistent performance.
How can this be achieved?
Correct answer
Configure AWS Global Accelerator and configure the ALBs as targets
Place an EC2 Proxy in front of the ALB and configure automatic failover
Use a CloudFront distribution with multiple custom origins in each region and configure for high availability
Create a Route 53 Alias record for each ALB and configure a latency-based routing policy
Overall explanation
AWS Global Accelerator is a service that improves the availability and performance of applications with local or global users. You can configure the ALB as a target and Global Accelerator will automatically route users to the closest point of presence.
Failover is automatic and does not rely on any client side cache changes as the IP addresses for Global Accelerator are static anycast addresses. Global Accelerator also uses the AWS global network which ensures consistent performance.

CORRECT: "Configure AWS Global Accelerator and configure the ALBs as targets" is the correct answer.
INCORRECT: "Place an EC2 Proxy in front of the ALB and configure automatic failover" is incorrect. Placing an EC2 proxy in front of the ALB does not meet the requirements. This solution does not ensure deterministic routing the closest region and failover is happening within a region which does not protect against regional failure. Also, this introduces a potential bottleneck and lack of redundancy.
INCORRECT: "Create a Route 53 Alias record for each ALB and configure a latency-based routing policy" is incorrect. A Route 53 Alias record for each ALB with latency-based routing does provide routing based on latency and failover. However, the traffic will not traverse the AWS global network.
INCORRECT: "Use a CloudFront distribution with multiple custom origins in each region and configure for high availability" is incorrect. You can use CloudFront with multiple custom origins and configure for HA. However, the traffic will not traverse the AWS global network.
References:
https://aws.amazon.com/global-accelerator/
https://aws.amazon.com/global-accelerator/faqs/
https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-global-accelerator/
Domain
AWS Compute
Question 55Skipped
A small Python application is used by a company to process JSON documents and output the results to a SQL database which currently lives on-premises. The application is run thousands of times every day, and the company wants to move the application to the AWS Cloud. To maximize scalability and minimize operational overhead, the company needs a highly available solution.
Which solution will meet these requirements?
Correct answer
Put the JSON documents in an Amazon S3 bucket. As documents arrive in the S3 bucket, create an AWS Lambda function that runs Python code to process them. Use Amazon Aurora DB clusters to store the results.
The JSON documents should be queued as messages in the Amazon Simple Queue Service (Amazon SQS). Using the Amazon Elastic Container Service (Amazon ECS) with the Amazon EC2 launch type, deploy the Python code as a container. The container can be used to process SQS messages. Using Amazon RDS, store the results.
Build an S3 bucket to place the JSON documents in. Run the Python code on multiple Amazon EC2 instances to process the documents. Store the results in a database using the Amazon Aurora Database engine.
Create an Amazon Elastic Block Store (Amazon EBS) volume for the JSON documents. Attach the volume to multiple Amazon EC2 instances using the EBS Multi-Attach feature. Process the documents with Python code on the EC2 instances and then extract the results to an Amazon RDS DB instance.
Overall explanation
Firstly, S3 is a highly available and durable place to store these JSON documents that will be written once and read many times (WORM). As this application runs thousands of times per day, AWS Lambda would be ideal to use as it will scale whenever the application needs to be ran, and Python is a runtime environment that is natively supported by AWS Lambda, whenever the events arrive in the S3 bucket, and this could be easily achieved using S3 event notifications. Finally Amazon Aurora is a highly available and durable AWS managed database. Amazon Aurora automatically maintains six copies of your data across three Availability Zones (AZs) to adhere to your redundancy requirements.
CORRECT: "Put the JSON documents in an Amazon S3 bucket. As documents arrive in the S3 bucket, create an AWS Lambda function that runs Python code to process them. Use Amazon Aurora DB clusters to store the results" is the correct answer (as explained above.)
INCORRECT: "Build an S3 bucket to place the JSON documents in. Run the Python code on multiple Amazon EC2 instances to process the documents. Store the results in a database using the Amazon Aurora Database engine” is incorrect.
Multiple EC2 instances could work, however if you wanted to use EC2 to process the JSON documents you would need to either leave the EC2 instances running all the time (not cost effective) or have them spin up and spin down thousands of times per day (this would be slow and not ideal).
INCORRECT: "Create an Amazon Elastic Block Store (Amazon EBS) volume for the JSON documents. Attach the volume to multiple Amazon EC2 instances using the EBS Multi-Attach feature. Process the documents with Python code on the EC2 instances and then extract the results to an Amazon RDS DB instance" is incorrect.
EBS is not optimized for write once read many use-cases, and if you wanted to use EC2 to process the JSON documents you would need to either leave the EC2 instances running all the time (not cost effective) or have them spin up and spin down thousands of times per day (this would be slow and not ideal).
INCORRECT: "The JSON documents should be queued as messages in the Amazon Simple Queue Service (Amazon SQS). Using the Amazon Elastic Container Service (Amazon ECS) with the Amazon EC2 launch type, deploy the Python code as a container. The container can be used to process SQS messages. Using Amazon RDS, store the results” is incorrect.
A queue within Amazon SQS is not designed to be used for write once read many solutions, and it is designed to be used to decouple separate layers of your architecture. Secondly, ECS for EC2 is not ideal as you would need to either leave the EC2 instances running all the time (not cost effective) or have them spin up and spin down thousands of times per day (this would be slow and not ideal) if you wanted to use ECS for EC2.
References:
https://docs.aws.amazon.com/lambda/latest/dg/services-rds.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Compute
Question 57Skipped
A company runs an application in an Amazon VPC that requires access to an Amazon Elastic Container Service (Amazon ECS) cluster that hosts an application in another VPC. The company’s security team requires that all traffic must not traverse the internet.
Which solution meets this requirement?
Configure an Amazon Route 53 private hosted zone for each VPC. Use private records to resolve internal IP addresses in each VPC.
Configure a gateway endpoint for Amazon ECS. Update the route table to include an entry pointing to the ECS cluster.
Correct answer
Create a Network Load Balancer in one VPC and an AWS PrivateLink endpoint for Amazon ECS in another VPC.
Create a Network Load Balancer and AWS PrivateLink endpoint for Amazon ECS in the VPC that hosts the ECS cluster.
Overall explanation
The correct solution is to use AWS PrivateLink in a service provider model. In this configuration a network load balancer will be implemented in the service provider VPC (the one with the ECS cluster in this example), and a PrivateLink endpoint will be created in the consumer VPC (the one with the company’s application).


CORRECT: "Create a Network Load Balancer in one VPC and an AWS PrivateLink endpoint for Amazon ECS in another VPC" is the correct answer.
INCORRECT: "Create a Network Load Balancer and AWS PrivateLink endpoint for Amazon ECS in the VPC that hosts the ECS cluster" is incorrect. The endpoint should be in the consumer VPC, not the service provider VPC (see the diagram above).
INCORRECT: "Configure a gateway endpoint for Amazon ECS. Update the route table to include an entry pointing to the ECS cluster" is incorrect. You cannot use a gateway endpoint to connect to a private service. Gateway endpoints are only for S3 and DynamoDB.
INCORRECT: "Configure an Amazon Route 53 private hosted zone for each VPC. Use private records to resolve internal IP addresses in each VPC" is incorrect. This does not provide a mechanism for resolving each other’s addresses and there’s no method of internal communication using private IPs such as VPC peering.
References:
https://aws.amazon.com/privatelink/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 59Skipped
A fitness company collects user feedback from mobile app surveys about its workout plans and features. Users submit thousands of survey responses daily, and the company wants to automate feedback analysis to track user sentiment and improve its offerings. The analyzed feedback data must be stored for at least 12 months to identify trends over time.
The company requires a highly scalable solution that minimizes operational complexity.
Which solution will meet these requirements in the MOST scalable way?
Deploy an on-premises server that receives survey responses via a REST API. Process the data locally, use a custom machine learning model for sentiment analysis, and upload results to Amazon S3. Use Amazon S3 lifecycle policies to delete the data after 12 months.
Send survey responses to an Amazon EventBridge rule, which routes the data to an AWS Step Functions workflow. Use Step Functions to trigger AWS Lambda for data processing and sentiment analysis with Amazon Comprehend. Store the results in an Amazon DynamoDB table and use DynamoDB's TTL feature to expire data after 12 months.
Write survey responses directly to an Amazon Redshift database. Configure Amazon Redshift ML to perform sentiment analysis on the feedback data in real time. Use Amazon S3 to archive the processed results and configure lifecycle policies to delete S3 objects after 12 months.
Correct answer
Collect survey responses via an Amazon API Gateway endpoint integrated with Amazon Kinesis Data Firehose. Configure Firehose to stream the data to an Amazon S3 bucket. Use S3 Event Notifications to invoke an AWS Lambda function that calls Amazon Comprehend for sentiment analysis and writes results to an Amazon DynamoDB table with TTL configured to delete records after 12 months.
Overall explanation
Collect survey responses via an Amazon API Gateway endpoint integrated with Amazon Kinesis Data Firehose. Configure Firehose to stream the data to an Amazon S3 bucket. Use S3 Event Notifications to invoke an AWS Lambda function that calls Amazon Comprehend for sentiment analysis and writes results to an Amazon DynamoDB table with TTL configured to delete records after 12 months:
This is correct because this architecture is highly scalable and cost-effective. Kinesis Data Firehose automatically scales to handle large volumes of data, and S3 provides reliable storage for raw survey responses. Using Lambda for sentiment analysis with Amazon Comprehend reduces operational complexity, and DynamoDB with TTL ensures data is stored efficiently for 12 months.
Send survey responses to an Amazon EventBridge rule, which routes the data to an AWS Step Functions workflow. Use Step Functions to trigger AWS Lambda for data processing and sentiment analysis with Amazon Comprehend. Store the results in an Amazon DynamoDB table, and use DynamoDB's TTL feature to expire data after 12 months:
This is incorrect because using EventBridge and Step Functions adds unnecessary complexity to the workflow. Kinesis Data Firehose with S3 provides a simpler and more efficient mechanism for streaming and storing data.
Write survey responses directly to an Amazon Redshift database. Configure Amazon Redshift ML to perform sentiment analysis on the feedback data in real time. Use Amazon S3 to archive the processed results, and configure lifecycle policies to delete S3 objects after 12 months:
This is incorrect because Amazon Redshift is better suited for analytical queries and is not optimized for real-time sentiment analysis. This solution introduces higher costs and complexity compared to using Amazon Comprehend and DynamoDB.
Deploy an on-premises server that receives survey responses via a REST API. Process the data locally, use a custom machine learning model for sentiment analysis, and upload results to Amazon S3. Use Amazon S3 lifecycle policies to delete the data after 12 months:
This is incorrect because deploying and managing on-premises servers increases operational overhead. AWS services like Lambda and Comprehend provide a more scalable and managed solution for this use case.
References:
https://docs.aws.amazon.com/streams/latest/dev/introduction.html
https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-kinesis/
Domain
AWS Compute



























Dump6
Question 1Skipped
A high-performance file system is required for a financial modelling application. The data set will be stored on Amazon S3 and the storage solution must have seamless integration so objects can be accessed as files.
Which storage solution should be used?
Amazon Elastic Block Store (EBS)
Correct answer
Amazon FSx for Lustre
Amazon Elastic File System (EFS)
Amazon FSx for Windows File Server
Overall explanation
Amazon FSx for Lustre provides a high-performance file system optimized for fast processing of workloads such as machine learning, high performance computing (HPC), video processing, financial modeling, and electronic design automation (EDA). Amazon FSx works natively with Amazon S3, letting you transparently access your S3 objects as files on Amazon FSx to run analyses for hours to months.

CORRECT: "Amazon FSx for Lustre" is the correct answer.
INCORRECT: "Amazon FSx for Windows File Server" is incorrect. Amazon FSx for Windows File Server provides a fully managed native Microsoft Windows file system so you can easily move your Windows-based applications that require shared file storage to AWS. This solution integrates with Windows file shares, not with Amazon S3.
INCORRECT: "Amazon Elastic File System (EFS)" is incorrect. EFS and EBS are not good use cases for this solution. Neither storage solution is capable of presenting Amazon S3 objects as files to the application.
INCORRECT: "Amazon Elastic Block Store (EBS)" is incorrect. EFS and EBS are not good use cases for this solution. Neither storage solution is capable of presenting Amazon S3 objects as files to the application.
References:
https://aws.amazon.com/fsx/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Compute
Question 4Skipped
A company’s staff connect from home office locations to administer applications using bastion hosts in a single AWS Region. The company requires a resilient bastion host architecture that requires minimal ongoing operational overhead.
How can a Solutions Architect best meet these requirements?
Correct answer
Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple Availability Zones.
Create a Network Load Balancer backed by Reserved Instances in a cluster placement group.
Create a Network Load Balancer backed by the existing servers in different Availability Zones.
Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple AWS Regions.
Overall explanation
Bastion hosts (aka “jump hosts”) are EC2 instances in public subnets that administrators and operations staff can connect to from the internet. From the bastion host they are then able to connect to other instances and applications within AWS by using internal routing within the VPC.
All answers use a Network Load Balancer which is acceptable for forwarding incoming connections to targets. The differences are in where the connections are forwarded to. The best option is to create an Auto Scaling group with EC2 instances in multiple Availability Zones. This creates a resilient architecture within a single AWS Region which is exactly what the question asks for.
CORRECT: "Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple Availability Zones" is the correct answer.
INCORRECT: "Create a Network Load Balancer backed by an Auto Scaling group with instances in multiple AWS Regions" is incorrect. You cannot have instances in an ASG across multiple Regions and you can’t have an NLB distribute connections across multiple Regions.
INCORRECT: "Create a Network Load Balancer backed by Reserved Instances in a cluster placement group" is incorrect. A cluster placement group packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly coupled node-to-node communication that is typical of HPC applications.
INCORRECT: "Create a Network Load Balancer backed by the existing servers in different Availability Zones" is incorrect. An Auto Scaling group is required to maintain instances in different AZs for resilience.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Compute
Question 5Skipped
A company wants to use Amazon Elastic Container Service (Amazon ECS) to run its containerized application in a hybrid environment. The company needs to ensure that the application can scale across both on-premises and AWS environments. It also requires a load balancer to handle HTTP traffic for the new containers that will run in the AWS Cloud.
Which combination of actions will meet these requirements? (Select TWO.)
Set up an ECS cluster that uses the AWS Fargate launch type. Use Fargate for the cloud application containers and the on-premises application containers.
Set up an ECS cluster that uses the Amazon EC2 launch type for the cloud application containers. Use Amazon ECS Anywhere with an AWS Fargate launch type for the on-premises application containers.
Correct selection
Set up an ECS cluster that uses the AWS Fargate launch type for the cloud application containers. Use an Amazon ECS Anywhere external launch type for the on-premises application containers.
Correct selection
Set up an Application Load Balancer for cloud ECS services.
Set up a Network Load Balancer for cloud ECS services.
Overall explanation
Set up an ECS cluster that uses the AWS Fargate launch type for the cloud application containers. Use an Amazon ECS Anywhere external launch type for the on-premises application containers: This meets the requirement of a hybrid environment by running containers in AWS Fargate for cloud workloads and Amazon ECS Anywhere for on-premises workloads. ECS Anywhere enables on-premises servers to join ECS clusters.
Set up an Application Load Balancer for cloud ECS services: This is the appropriate load balancer for handling HTTP traffic, ensuring proper routing and scalability for the cloud-based application containers.
Set up a Network Load Balancer for cloud ECS services: This is incorrect because a Network Load Balancer is primarily used for TCP or UDP traffic, not HTTP traffic.
Set up an ECS cluster that uses the AWS Fargate launch type. Use Fargate for the cloud application containers and the on-premises application containers: This is incorrect because Fargate cannot be used to run containers in an on-premises environment.
Set up an ECS cluster that uses the Amazon EC2 launch type for the cloud application containers. Use Amazon ECS Anywhere with an AWS Fargate launch type for the on-premises application containers: This is incorrect because ECS Anywhere uses external instances, not AWS Fargate, for on-premises environments.
References:
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/what-is-ecs.html
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-anywhere.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Compute
Question 6Skipped
A company operates a production environment on Amazon EC2 instances. The instances are required to run continuously from Tuesday to Sunday without interruptions. On Mondays, the instances are needed for only 8 hours, and they also cannot tolerate interruptions. The company wants to implement a cost-effective solution to optimize EC2 usage while meeting these requirements.
Which solution will provide the MOST cost-effective results?
Purchase Convertible Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Spot Instances for the EC2 instances that run for 8 hours on Mondays.
Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Convertible Reserved Instances for the EC2 instances that run for 8 hours on Mondays.
Use Spot Instances for the EC2 instances that run for 8 hours on Mondays. Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday.
Correct answer
Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Scheduled Reserved Instances for the EC2 instances that run for 8 hours on Mondays.
Overall explanation
Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Scheduled Reserved Instances for the EC2 instances that run for 8 hours on Mondays: This is correct because Standard Reserved Instances provide cost savings for long-term, predictable workloads, like the continuous operation from Tuesday to Sunday. Scheduled Reserved Instances are ideal for predictable workloads with fixed schedules, like the 8-hour workload on Mondays, offering savings while ensuring uninterrupted operation.
Use Spot Instances for the EC2 instances that run for 8 hours on Mondays. Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday: This is incorrect because Spot Instances, while cost-effective, are not suitable for workloads that cannot tolerate interruptions. Spot Instances may be terminated unexpectedly, which does not meet the requirement for uninterrupted operation.
Purchase Convertible Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Spot Instances for the EC2 instances that run for 8 hours on Mondays: This is incorrect because Convertible Reserved Instances, while flexible, are not the most cost-effective option for predictable and consistent workloads like continuous operation from Tuesday to Sunday. Additionally, Spot Instances are unsuitable for workloads requiring uninterrupted operation.
Purchase Standard Reserved Instances for the EC2 instances that operate continuously from Tuesday to Sunday. Use Convertible Reserved Instances for the EC2 instances that run for 8 hours on Mondays: This is incorrect because Convertible Reserved Instances are not as cost-effective as Scheduled Reserved Instances for fixed and predictable schedules, such as the 8-hour Monday workload.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-reserved-instances.html
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Compute
Question 7Skipped
A company runs a business-critical application in the us-east-1 Region. The application uses an Amazon Aurora MySQL database cluster which is 2 TB in size. A Solutions Architect needs to determine a disaster recovery strategy for failover to the us-west-2 Region. The strategy must provide a recovery time objective (RTO) of 10 minutes and a recovery point objective (RPO) of 5 minutes.
Which strategy will meet these requirements?
Correct answer
Recreate the database as an Aurora global database with the primary DB cluster in us-east-1 and a secondary DB cluster in us-west-2. Use an Amazon EventBridge rule that invokes an AWS Lambda function to promote the DB cluster in us-west-2 when failure is detected.
Create a multi-Region Aurora MySQL DB cluster in us-east-1 and us-west-2. Use an Amazon Route 53 health check to monitor us-east-1 and fail over to us-west-2 upon failure.
Recreate the database as an Aurora multi master cluster across the us-east-1 and us-west-2 Regions with multiple writers to allow read/write capabilities from all database instances.
Create a cross-Region Aurora MySQL read replica in us-west-2 Region. Configure an Amazon EventBridge rule that invokes an AWS Lambda function that promotes the read replica in us-west-2 when failure is detected.
Overall explanation
Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each region, and provides disaster recovery from region-wide outages
If your primary region suffers a performance degradation or outage, you can promote one of the secondary regions to take read/write responsibilities. An Aurora cluster can recover in less than 1 minute even in the event of a complete regional outage.
This provides your application with an effective Recovery Point Objective (RPO) of 1 second and a Recovery Time Objective (RTO) of less than 1 minute, providing a strong foundation for a global business continuity plan


CORRECT: "Recreate the database as an Aurora global database with the primary DB cluster in us-east-1 and a secondary DB cluster in us-west-2. Use an Amazon EventBridge rule that invokes an AWS Lambda function to promote the DB cluster in us-west-2 when failure is detected" is the correct answer.
INCORRECT: "Create a multi-Region Aurora MySQL DB cluster in us-east-1 and us-west-2. Use an Amazon Route 53 health check to monitor us-east-1 and fail over to us-west-2 upon failure" is incorrect. You cannot create a multi-Region Aurora MySQL DB cluster. Options are to create MySQL Replicas (may meet the RTO objectives), or to use global database.
INCORRECT: "Create a cross-Region Aurora MySQL read replica in us-west-2 Region. Configure an Amazon EventBridge rule that invokes an AWS Lambda function that promotes the read replica in us-west-2 when failure is detected" is incorrect. This may not meet the RTO objectives as large databases may well take more than 10 minutes to promote.
INCORRECT: "Recreate the database as an Aurora multi master cluster across the us-east-1 and us-west-2 Regions with multiple writers to allow read/write capabilities from all database instances" is incorrect. Multi master only works within a Region it does not work across Regions.
References:
https://aws.amazon.com/rds/aurora/global-database/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Compute
Question 14Skipped
A Solutions Architect is designing a solution for an application that requires very low latency between the client and the backend. The application uses the UDP protocol, and the backend is hosted on Amazon EC2 instances. The solution must be highly available across multiple Regions and users around the world should be directed to the most appropriate Region based on performance.
How can the Solutions Architect meet these requirements?
Deploy an Application Load Balancer in front of the EC2 instances in each Region. Use AWS WAF to direct traffic to the most optimal Regional endpoint.
Deploy an Amazon CloudFront distribution with a custom origin pointing to Amazon EC2 instances in multiple Regions.
Deploy Amazon EC2 instances in multiple Regions. Create a multivalue answer routing record in Amazon Route 53 that includes all EC2 endpoints.
Correct answer
Deploy a Network Load Balancer in front of the EC2 instances in each Region. Use AWS Global Accelerator to route traffic to the most optimal Regional endpoint.
Overall explanation
An NLB is ideal for latency-sensitive applications and can listen on UDP for incoming requests. As Elastic Load Balancers are region-specific it is necessary to have an NLB in each Region in front of the EC2 instances.
To direct traffic based on optimal performance, AWS Global Accelerator can be used. GA will ensure traffic is routed across the AWS global network to the most optimal endpoint based on performance.


CORRECT: "Deploy a Network Load Balancer in front of the EC2 instances in each Region. Use AWS Global Accelerator to route traffic to the most optimal Regional endpoint" is the correct answer.
INCORRECT: "Deploy an Application Load Balancer in front of the EC2 instances in each Region. Use AWS WAF to direct traffic to the most optimal Regional endpoint" is incorrect. You cannot use WAF to direct traffic to endpoints based on performance.
INCORRECT: "Deploy an Amazon CloudFront distribution with a custom origin pointing to Amazon EC2 instances in multiple Regions" is incorrect. CloudFront cannot listen on UDP, it is used for HTTP/HTTPS.
INCORRECT: "Deploy Amazon EC2 instances in multiple Regions. Create a multivalue answer routing record in Amazon Route 53 that includes all EC2 endpoints" is incorrect. This configuration would not route incoming requests to the most optimal endpoint based on performance, it would provide multiple records in answers and traffic would be distributed across multiple Regions.
References:
https://docs.aws.amazon.com/global-accelerator/latest/dg/introduction-how-it-works.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-global-accelerator/
Domain
AWS Compute
Question 16Skipped
An organization is extending a secure development environment into AWS. They have already secured the VPC including removing the Internet Gateway and setting up a Direct Connect connection. What else needs to be done to add encryption?
Configure an AWS Direct Connect Gateway
Setup the Border Gateway Protocol (BGP) with encryption
Enable IPSec encryption on the Direct Connect connection
Correct answer
Setup a Virtual Private Gateway (VPG)
Overall explanation
A VPG is used to setup an AWS VPN which you can use in combination with Direct Connect to encrypt all data that traverses the Direct Connect link. This combination provides an IPsec-encrypted private connection that also reduces network costs, increases bandwidth throughput, and provides a more consistent network experience than internet-based VPN connections.
CORRECT: "Setup a Virtual Private Gateway (VPG)" is the correct answer.
INCORRECT: "Enable IPSec encryption on the Direct Connect connection" is incorrect. There is no option to enable IPSec encryption on the Direct Connect connection.
INCORRECT: "Setup the Border Gateway Protocol (BGP) with encryption" is incorrect. The BGP protocol is not used to enable encryption for Direct Connect, it is used for routing.
INCORRECT: "Configure an AWS Direct Connect Gateway" is incorrect. An AWS Direct Connect Gateway is used to connect to VPCs across multiple AWS regions. It is not involved with encryption.
References:
https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-direct-connect-plus-vpn-network-to-amazon.html
https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 22Skipped
A government agency is moving its document management system to AWS. The application will store classified documents in Amazon S3. The agency must encrypt the documents before storing them in S3 to ensure compliance with strict data security regulations.
Which solution will meet these requirements?
Encrypt the documents by using client-side encryption with Amazon S3 managed keys and upload the encrypted files to S3.
Correct answer
Encrypt the documents by using client-side encryption with customer managed keys and upload the encrypted files to S3.
Encrypt the documents by using server-side encryption with customer-provided keys (SSE-C).
Encrypt the documents by using server-side encryption with AWS KMS keys (SSE-KMS) configured with custom key policies for access control.
Overall explanation
Encrypt the documents by using client-side encryption customer managed keys and upload the encrypted files to S3:
This is correct because client-side encryption means the data is encrypted before it ever leaves the client system, giving maximum control over the encryption process. Using customer managed keys (CMKs) from AWS Key Management Service (KMS), the agency retains full ownership and control over key policies, rotation, and access, which is often a requirement for handling classified or sensitive government data. This approach ensures compliance with strict regulations by minimizing trust in the cloud provider to protect unencrypted data.
Encrypt the documents by using server-side encryption with AWS KMS keys (SSE-KMS) configured with custom key policies for access control: This is incorrect because while secure and easy to manage, SSE-KMS means AWS handles the encryption after data reaches S3
Encrypt the documents by using client-side encryption with customer managed keys and upload the encrypted files to S3: This is incorrect because while client-side encryption can ensure security before data reaches S3, it increases operational complexity since the customer must manage key creation, storage, and rotation independently.
Encrypt the documents by using server-side encryption with customer-provided keys (SSE-C): This is incorrect because SSE-C requires the customer to provide the encryption keys for every S3 operation, which can increase operational overhead and risks if key management is not handled correctly.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingEncryption.html
https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-kms/
Domain
AWS Compute
Question 35Skipped
An application is deployed on multiple AWS regions and accessed from around the world. The application exposes static public IP addresses. Some users are experiencing poor performance when accessing the application over the Internet.
What should a solutions architect recommend to reduce internet latency?
Set up an Amazon Route 53 geoproximity routing policy to route traffic
Correct answer
Set up AWS Global Accelerator and add endpoints
Set up an Amazon CloudFront distribution to access an application
Set up AWS Direct Connect locations in multiple Regions
Overall explanation
AWS Global Accelerator is a service in which you create accelerators to improve availability and performance of your applications for local and global users. Global Accelerator directs traffic to optimal endpoints over the AWS global network. This improves the availability and performance of your internet applications that are used by a global audience. Global Accelerator is a global service that supports endpoints in multiple AWS Regions, which are listed in the AWS Region Table.
By default, Global Accelerator provides you with two static IP addresses that you associate with your accelerator. (Or, instead of using the IP addresses that Global Accelerator provides, you can configure these entry points to be IPv4 addresses from your own IP address ranges that you bring to Global Accelerator.)


The static IP addresses are anycast from the AWS edge network and distribute incoming application traffic across multiple endpoint resources in multiple AWS Regions, which increases the availability of your applications. Endpoints can be Network Load Balancers, Application Load Balancers, EC2 instances, or Elastic IP addresses that are located in one AWS Region or multiple Regions.
CORRECT: "Set up AWS Global Accelerator and add endpoints" is the correct answer.
INCORRECT: "Set up AWS Direct Connect locations in multiple Regions" is incorrect as this is used to connect from an on-premises data center to AWS. It does not improve performance for users who are not connected to the on-premises data center.
INCORRECT: "Set up an Amazon CloudFront distribution to access an application" is incorrect as CloudFront cannot expose static public IP addresses.
INCORRECT: "Set up an Amazon Route 53 geoproximity routing policy to route traffic" is incorrect as this does not reduce internet latency as well as using Global Accelerator. GA will direct users to the closest edge location and then use the AWS global network.
References:
https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-global-accelerator/
Domain
AWS Compute
Question 37Skipped
A company needs to implement a new data retention policy for regulatory compliance. As part of this policy, sensitive documents that are stored in an Amazon S3 bucket must be protected from deletion or modification for a fixed period of time.
Which solution will meet these requirements?
Create an Amazon S3 bucket with versioning enabled. Use a lifecycle rule to automatically delete older versions after the retention period.
Use AWS Backup to create immutable backups of the S3 objects and enforce a retention policy.
Correct answer
Enable S3 Object Lock on the required objects and set compliance mode.
Activate S3 Object Lock in compliance mode on the bucket. Configure a WORM (Write Once, Read Many) policy.
Overall explanation
Enable S3 Object Lock on the required objects and set compliance mode: This is correct because compliance mode ensures that no user, including the root user, can delete or modify objects during the retention period, making it suitable for regulatory requirements.
Activate S3 Object Lock in compliance mode on the bucket. Configure a WORM (Write Once, Read Many) policy: This is incorrect because S3 Object Lock applies to specific objects, not the entire bucket, and there is no WORM-specific configuration required beyond compliance mode.
Create an Amazon S3 bucket with versioning enabled. Use a lifecycle rule to automatically delete older versions after the retention period: This is incorrect because versioning and lifecycle policies do not provide protection against modification or deletion during the retention period.
Use AWS Backup to create immutable backups of the S3 objects and enforce a retention policy: This is incorrect because AWS Backup does not integrate directly with S3 Object Lock to meet regulatory compliance needs for immutability.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock-overview.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-object-lock.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Compute
Question 44Skipped
A Solutions Architect works for a company looking to centralize its Machine Learning Operations. Currently they have a large amount of existing cloud storage to store their operational data which is used for machine learning analysis. There is some data which exists within an Amazon RDS MySQL database, and they need a solution which can easily retrieve data from the database.
Which service can be used to build a centralized data repository to be used for Machine Learning purposes?
Amazon S3
Correct answer
AWS Lake Formation
Amazon Quantum Ledger Database (QLDB)
Amazon Neptune
Overall explanation
AWS Lake Formation is a service that makes it easy to set up a secure data lake in days. A data lake is a centralized, curated, and secured repository that stores all your data, both in its original form and prepared for analysis. With AWS Lake Formation, you can import data from MySQL, PostgreSQL, SQL Server, MariaDB, and Oracle databases running in Amazon Relational Database Service (RDS) or hosted in Amazon Elastic Compute Cloud (EC2). Both bulk and incremental data loading are supported.
CORRECT: "AWS Lake Formation" is the correct answer (as explained above.)
INCORRECT: "Amazon S3" is incorrect. Amazon Simple Storage Service (Amazon S3) is an object storage service offering industry-leading scalability, data availability, security, and performance. It is not however suitable for directly retrieving data from MySQL on RDS and using the data for a Machine learning use case.
INCORRECT: "Amazon Quantum Ledger Database" is incorrect. Amazon Quantum Ledger Database (QLDB) is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log. It is not suitable for directly retrieving data from MySQL on RDS and using the data for a Machine learning use case.
INCORRECT: "Amazon Neptune" is incorrect. Amazon Neptune is a fast, reliable, fully managed graph database service that makes it easy to build and run applications. It is not suitable for directly retrieving data from MySQL on RDS and using the data for a Machine learning use case.
References:
https://aws.amazon.com/lake-formation/features/

Save time with our AWS cheat sheets:

https://digitalcloud.training/category/aws-cheat-sheets/aws-solutions-architect-associate/aws-storage-saa/
Domain
AWS Compute
Question 59Skipped
A company manages several applications that run in different AWS accounts within an AWS Organizations setup. The company has outsourced the management of certain applications to external contractors. The contractors require secure access to the AWS Management Console and operating system access to Amazon Linux-based Amazon EC2 instances in private subnets for troubleshooting. The company must ensure all activities are logged and minimize the risk of unauthorized access.
Which solution will meet these requirements MOST securely?
Configure a bastion host in a public subnet. Restrict SSH access to the bastion host by using security groups to allow connections only from the contractors' IP address ranges. Provide contractors with IAM user credentials for Management Console access and SSH key pairs for accessing private instances via the bastion host.
Correct answer
Deploy AWS Systems Manager Agent (SSM Agent) to all instances. Assign an instance profile to the instances with the required Systems Manager policies. Grant contractors access to the AWS Management Console by configuring permission sets in AWS IAM Identity Center. Use Systems Manager Session Manager for secure instance access without requiring open network ports.
Use AWS Systems Manager Agent (SSM Agent) with an attached instance profile to manage EC2 access. Provide contractors with temporary local IAM user credentials in each AWS account for console access. Require contractors to use Systems Manager Session Manager for instance access.
Set up AWS VPN or Direct Connect to create a private network connection to the contractors’ office. Allow access to the AWS Management Console by creating IAM user credentials in each AWS account. Use security groups to allow SSH access from the contractors' office to the private EC2 instances.
Overall explanation
Deploy AWS Systems Manager Agent (SSM Agent) to all instances. Assign an instance profile to the instances with the required Systems Manager policies. Grant contractors access to the AWS Management Console by configuring permission sets in AWS IAM Identity Center. Use Systems Manager Session Manager for secure instance access without requiring open network ports:
This is correct because Systems Manager Session Manager provides secure, auditable access to instances without requiring SSH keys or open ports. IAM Identity Center enables centralized management of console access for contractors.
Configure a bastion host in a public subnet. Restrict SSH access to the bastion host by using security groups to allow connections only from the contractors' IP address ranges. Provide contractors with IAM user credentials for Management Console access and SSH key pairs for accessing private instances via the bastion host:
This is incorrect because it increases operational overhead and requires managing SSH key pairs while leaving an exposed attack surface with the bastion host.
Use AWS Systems Manager Agent (SSM Agent) with an attached instance profile to manage EC2 access. Provide contractors with temporary local IAM user credentials in each AWS account for console access. Require contractors to use Systems Manager Session Manager for instance access:
This is incorrect because creating local IAM users for console access increases the risk of credential management issues and does not align with centralized access management best practices.
Set up AWS VPN or Direct Connect to create a private network connection to the contractors’ office. Allow access to the AWS Management Console by creating IAM user credentials in each AWS account. Use security groups to allow SSH access from the contractors' office to the private EC2 instances:
This is incorrect because using VPN or Direct Connect introduces unnecessary complexity and cost. SSH access also increases the risk of mismanagement and security vulnerabilities.
References:
https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html
https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-systems-manager/
Domain
AWS Compute
Question 12Skipped
Over 500 TB of data must be analyzed using standard SQL business intelligence tools. The dataset consists of a combination of structured data and unstructured data. The unstructured data is small and stored on Amazon S3. Which AWS services are most suitable for performing analytics on the data?
Amazon DynamoDB with Amazon DynamoDB Accelerator (DAX)
Amazon RDS MariaDB with Amazon Athena
Amazon ElastiCache for Redis with cluster mode enabled
Correct answer
Amazon Redshift with Amazon Redshift Spectrum
Overall explanation
Amazon Redshift is an enterprise-level, petabyte scale, fully managed data warehousing service. An Amazon Redshift data warehouse is an enterprise-class relational database query and management system. Redshift supports client connections with many types of applications, including business intelligence (BI), reporting, data, and analytics tools.
Using Amazon Redshift Spectrum, you can efficiently query and retrieve structured and semistructured data from files in Amazon S3 without having to load the data into Amazon Redshift tables. Redshift Spectrum queries employ massive parallelism to execute very fast against large datasets.


Used together, RedShift and RedShift spectrum are suitable for running massive analytics jobs on both the structured (RedShift data warehouse) and unstructured (Amazon S3) data.
CORRECT: "Amazon Redshift with Amazon Redshift Spectrum" is the correct answer.
INCORRECT: "Amazon RDS MariaDB with Amazon Athena" is incorrect. Amazon RDS is not suitable for analytics (OLAP) use cases as it is designed for transactional (OLTP) use cases. Athena can however be used for running SQL queries on data on S3.
INCORRECT: "Amazon DynamoDB with Amazon DynamoDB Accelerator (DAX)" is incorrect. This is an example of a non-relational DB with a caching layer and is not suitable for an OLAP use case.
INCORRECT: "Amazon ElastiCache for Redis with cluster mode enabled" is incorrect. This is an example of an in-memory caching service. It is good for performance for transactional use cases.
References:
https://docs.aws.amazon.com/redshift/latest/dg/c_redshift_system_overview.html
https://docs.aws.amazon.com/redshift/latest/dg/c-using-spectrum.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-redshift/
Domain
AWS Compute
Question 19Skipped
A Solutions Architect has been tasked with re-deploying an application running on AWS to enable high availability. The application processes messages that are received in an ActiveMQ queue running on a single Amazon EC2 instance. Messages are then processed by a consumer application running on Amazon EC2. After processing the messages the consumer application writes results to a MySQL database running on Amazon EC2.
Which architecture offers the highest availability and low operational complexity?
Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Launch an additional consumer EC2 instance in another Availability Zone. Use MySQL database replication to another Availability Zone.
Correct answer
Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Create an Auto Scaling group for the consumer EC2 instances across two Availability Zones. Use an Amazon RDS MySQL database with Multi-AZ enabled.
Deploy a second Active MQ server to another Availability Zone. Launch an additional consumer EC2 instance in another Availability Zone. Use MySQL database replication to another Availability Zone.
Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Launch an additional consumer EC2 instance in another Availability Zone. Use Amazon RDS for MySQL with Multi-AZ enabled.
Overall explanation
The correct answer offers the highest availability as it includes Amazon MQ active/standby brokers across two AZs, an Auto Scaling group across two AZ,s and a Multi-AZ Amazon RDS MySQL database deployment.
This architecture not only offers the highest availability it is also operationally simple as it maximizes the usage of managed services.
CORRECT: "Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Create an Auto Scaling group for the consumer EC2 instances across two Availability Zones. Use an Amazon RDS MySQL database with Multi-AZ enabled" is the correct answer.
INCORRECT: "Deploy a second Active MQ server to another Availability Zone. Launch an additional consumer EC2 instance in another Availability Zone. Use MySQL database replication to another Availability Zone" is incorrect. This architecture does not offer the highest availability as it does not use Auto Scaling. It is also not the most operationally efficient architecture as it does not use AWS managed services.
INCORRECT: "Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Launch an additional consumer EC2 instance in another Availability Zone. Use MySQL database replication to another Availability Zone" is incorrect. This architecture does not use Auto Scaling for best HA or the RDS managed service.
INCORRECT: "Deploy Amazon MQ with active/standby brokers configured across two Availability Zones. Launch an additional consumer EC2 instance in another Availability Zone. Use Amazon RDS for MySQL with Multi-AZ enabled" is incorrect. This solution does not use Auto Scaling.
References:
https://aws.amazon.com/architecture/well-architected/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
https://digitalcloud.training/amazon-ec2-auto-scaling/
https://digitalcloud.training/amazon-rds/
Domain
AWS Compute
Question 21Skipped
An application running on Amazon EC2 needs to asynchronously invoke an AWS Lambda function to perform data processing. The services should be decoupled.
Which service can be used to decouple the compute services?
Correct answer
Amazon SNS
Amazon MQ
AWS Config
AWS Step Functions
Overall explanation
You can use a Lambda function to process Amazon Simple Notification Service notifications. Amazon SNS supports Lambda functions as a target for messages sent to a topic. This solution decouples the Amazon EC2 application from Lambda and ensures the Lambda function is invoked.
CORRECT: "Amazon SNS" is the correct answer.
INCORRECT: "AWS Config" is incorrect. AWS Config is a service that is used for continuous compliance, not application decoupling.
INCORRECT: "Amazon MQ" is incorrect. Amazon MQ is similar to SQS but is used for existing applications that are being migrated into AWS. SQS should be used for new applications being created in the cloud.
INCORRECT: "AWS Step Functions" is incorrect. AWS Step Functions is a workflow service. It is not the best solution for this scenario.
References:
https://docs.aws.amazon.com/lambda/latest/dg/with-sns.html
https://aws.amazon.com/sns/features/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Compute
Question 23Skipped
A Solutions Architect is tasked with designing a fully Serverless, Microservices based web application which requires the use of a GraphQL API to provide a single entry point to the application.
Which AWS managed service could the Solutions Architect use?
API Gateway
AWS Lambda
Correct answer
AWS AppSync
Amazon Athena
Overall explanation
AWS AppSync is a serverless GraphQL and Pub/Sub API service that simplifies building modern web and mobile applications.
AWS AppSync GraphQL APIs simplify application development by providing a single endpoint to securely query or update data from multiple databases, microservices, and APIs.
CORRECT: "AWS AppSync" is the correct answer (as explained above.)
INCORRECT: "API Gateway" is incorrect. You cannot create GraphQL APIs on API Gateway.
INCORRECT: "Amazon Athena" is incorrect. Amazon Athena is a Serverless query service where you can query S3 using SQL statements.
INCORRECT: "AWS Lambda" is incorrect. AWS Lambda is a serverless compute service and is not designed to build APIs.
References:
https://aws.amazon.com/appsync/
Save time with our AWS cheat sheets:
https://digitalcloud.training/category/aws-cheat-sheets/aws-networking-content-delivery/
Domain
AWS Compute
Question 31Skipped
An organization want to share regular updates about their charitable work using static webpages. The pages are expected to generate a large amount of views from around the world. The files are stored in an Amazon S3 bucket. A solutions architect has been asked to design an efficient and effective solution.
Which action should the solutions architect take to accomplish this?
Use cross-Region replication to all Regions
Correct answer
Use Amazon CloudFront with the S3 bucket as its origin
Use the geoproximity feature of Amazon Route 53
Generate presigned URLs for the files
Overall explanation
Amazon CloudFront can be used to cache the files in edge locations around the world and this will improve the performance of the webpages.
To serve a static website hosted on Amazon S3, you can deploy a CloudFront distribution using one of these configurations:
Using a REST API endpoint as the origin with access restricted by an origin access identity (OAI)
Using a website endpoint as the origin with anonymous (public) access allowed
Using a website endpoint as the origin with access restricted by a Referer header
CORRECT: "Use Amazon CloudFront with the S3 bucket as its origin" is the correct answer.
INCORRECT: "Generate presigned URLs for the files" is incorrect as this is used to restrict access which is not a requirement.
INCORRECT: "Use cross-Region replication to all Regions" is incorrect as this does not provide a mechanism for directing users to the closest copy of the static webpages.
INCORRECT: "Use the geoproximity feature of Amazon Route 53" is incorrect as this does not include a solution for having multiple copies of the data in different geographic lcoations.
References:
https://aws.amazon.com/premiumsupport/knowledge-center/cloudfront-serve-static-website/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Compute
Question 43Skipped
A company is testing a new web application that runs on Amazon EC2 instances. A Solutions Architect is performing load testing and must be able to analyze the performance of the web application with a granularity of 1 minute.
What should the Solutions Architect do to meet this requirement?
Send Amazon CloudWatch logs to Amazon S3. Use Amazon Athena to perform the analysis.
Correct answer
Enable detailed monitoring on all EC2 instances. Use Amazon CloudWatch metrics to perform the analysis.
Create an AWS CloudTrail trail and log data events. Use Amazon Athena to query the CloudTrail logs.
Create an AWS Lambda function to fetch EC2 logs from Amazon CloudWatch Logs. Use Amazon CloudWatch metrics to perform the analysis.
Overall explanation
By default, your instance is enabled for basic monitoring. You can optionally enable detailed monitoring. After you enable detailed monitoring, the Amazon EC2 console displays monitoring graphs with a 1-minute period for the instance.
The following describes the data interval and charge for basic and detailed monitoring for instances:


CORRECT: "Enable detailed monitoring on all EC2 instances. Use Amazon CloudWatch metrics to perform the analysis" is the correct answer.
INCORRECT: "Send Amazon CloudWatch logs to Amazon S3. Use Amazon Athena to perform the analysis" is incorrect. You must enable detailed monitoring to get data in 1-minute periods.
INCORRECT: "Create an AWS Lambda function to fetch EC2 logs from Amazon CloudWatch Logs. Use Amazon CloudWatch metrics to perform the analysis" is incorrect. There is no need to use a Lambda function to retrieve the logs and detailed monitoring must still be enabled.
INCORRECT: "Create an AWS CloudTrail trail and log data events. Use Amazon Athena to query the CloudTrail logs" is incorrect. This will not assist with gathering the required data from EC2 instances. Detailed monitoring must be enabled instead.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch-new.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Compute
Question 44Skipped
An application that runs a computational fluid dynamics workload uses a tightly-coupled HPC architecture that uses the MPI protocol and runs across many nodes. A service-managed deployment is required to minimize operational overhead.
Which deployment option is MOST suitable for provisioning and managing the resources required for this use case?
Correct answer
Use AWS Batch to deploy a multi-node parallel job
Use Amazon EC2 Auto Scaling to deploy instances in multiple subnets
Use AWS CloudFormation to deploy a Cluster Placement Group on EC2
Use AWS Elastic Beanstalk to provision and manage the EC2 instances
Overall explanation
AWS Batch Multi-node parallel jobs enable you to run single jobs that span multiple Amazon EC2 instances. With AWS Batch multi-node parallel jobs, you can run large-scale, tightly coupled, high performance computing applications and distributed GPU model training without the need to launch, configure, and manage Amazon EC2 resources directly.
An AWS Batch multi-node parallel job is compatible with any framework that supports IP-based, internode communication, such as Apache MXNet, TensorFlow, Caffe2, or Message Passing Interface (MPI).
This is the most efficient approach to deploy the resources required and supports the application requirements most effectively.
CORRECT: "Use AWS Batch to deploy a multi-node parallel job" is the correct answer.
INCORRECT: "Use Amazon EC2 Auto Scaling to deploy instances in multiple subnets " is incorrect. This is not the best solution for a tightly-coupled HPC workload with specific requirements such as MPI support.
INCORRECT: "Use AWS CloudFormation to deploy a Cluster Placement Group on EC2" is incorrect. This would deploy a cluster placement group but not manage it. AWS Batch is a better fit for large scale workloads such as this.
INCORRECT: "Use AWS Elastic Beanstalk to provision and manage the EC2 instances" is incorrect. You can certainly provision and manage EC2 instances with Elastic Beanstalk but this scenario is for a specific workload that requires MPI support and managing a HPC deployment across a large number of nodes. AWS Batch is more suitable.
References:
https://d1.awsstatic.com/whitepapers/architecture/AWS-HPC-Lens.pdf
https://docs.aws.amazon.com/batch/latest/userguide/multi-node-parallel-jobs.html
Domain
AWS Compute
Question 45Skipped
Three Amazon VPCs are used by a company in the same region. The company has two AWS Direct Connect connections to two separate company offices and wishes to share these with all three VPCs. A Solutions Architect has created an AWS Direct Connect gateway. How can the required connectivity be configured?
Correct answer
Associate the Direct Connect gateway to a transit gateway
Create a VPC peering connection between the VPCs and route entries for the Direct Connect Gateway
Create a transit virtual interface between the Direct Connect gateway and each VPC
Associate the Direct Connect gateway to a virtual private gateway in each VPC
Overall explanation
You can manage a single connection for multiple VPCs or VPNs that are in the same Region by associating a Direct Connect gateway to a transit gateway. The solution involves the following components:
- A transit gateway that has VPC attachments.
- A Direct Connect gateway.
- An association between the Direct Connect gateway and the transit gateway.
- A transit virtual interface that is attached to the Direct Connect gateway.
The following diagram depicts this configuration:

CORRECT: "Associate the Direct Connect gateway to a transit gateway" is the correct answer.
INCORRECT: "Associate the Direct Connect gateway to a virtual private gateway in each VPC" is incorrect. For VPCs in the same region a VPG is not necessary. A transit gateway can instead be configured.
INCORRECT: "Create a VPC peering connection between the VPCs and route entries for the Direct Connect Gateway" is incorrect. You cannot add route entries for a Direct Connect gateway to each VPC and enable routing. Use a transit gateway instead.
INCORRECT: "Create a transit virtual interface between the Direct Connect gateway and each VPC" is incorrect. The transit virtual interface is attached to the Direct Connect gateway on the connection side, not the VPC/transit gateway side.
References:
https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-direct-connect/
Domain
AWS Compute
Question 50Skipped
Every time an item in an Amazon DynamoDB table is modified a record must be retained for compliance reasons. What is the most efficient solution to recording this information?
Correct answer
Enable DynamoDB Streams. Configure an AWS Lambda function to poll the stream and record the modified item data to an Amazon S3 bucket
Enable Amazon CloudWatch Logs. Configure an AWS Lambda function to monitor the log files and record deleted item data to an Amazon S3 bucket
Enable Amazon CloudTrail. Configure an Amazon EC2 instance to monitor activity in the CloudTrail log files and record changed items in another DynamoDB table
Enable DynamoDB Global Tables. Enable DynamoDB streams on the multi-region table and save the output directly to an Amazon S3 bucket
Overall explanation
Amazon DynamoDB Streams captures a time-ordered sequence of item-level modifications in any DynamoDB table and stores this information in a log for up to 24 hours. Applications can access this log and view the data items as they appeared before and after they were modified, in near-real time.
For example, in the diagram below a DynamoDB stream is being consumed by a Lambda function which processes the item data and records a record in CloudWatch Logs:


CORRECT: "Enable DynamoDB Streams. Configure an AWS Lambda function to poll the stream and record the modified item data to an Amazon S3 bucket" is the correct answer.
INCORRECT: "Enable Amazon CloudWatch Logs. Configure an AWS Lambda function to monitor the log files and record deleted item data to an Amazon S3 bucket" is incorrect. The deleted item data will not be recorded in CloudWatch Logs.
INCORRECT: "Enable Amazon CloudTrail. Configure an Amazon EC2 instance to monitor activity in the CloudTrail log files and record changed items in another DynamoDB table" is incorrect. CloudTrail records API actions so it will not record the data from the item that was modified.
INCORRECT: "Enable DynamoDB Global Tables. Enable DynamoDB streams on the multi-region table and save the output directly to an Amazon S3 bucket" is incorrect. Global Tables is used for creating a multi-region, multi-master database. It is of no additional value for this requirement as you could just enable DynamoDB streams on the main table. You also cannot save modified data straight to an S3 bucket.
References:
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-dynamodb/
Domain
AWS Compute
Question 52Skipped
A website is running on Amazon EC2 instances and access is restricted to a limited set of IP ranges. A solutions architect is planning to migrate static content from the website to an Amazon S3 bucket configured as an origin for an Amazon CloudFront distribution. Access to the static content must be restricted to the same set of IP addresses.
Which combination of steps will meet these requirements? (Select TWO.)
Create an AWS WAF web ACL that includes the same IP restrictions that exist in the EC2 security group. Associate this new web ACL with the Amazon S3 bucket.
Create an origin access identity (OAI) and associate it with the distribution. Generate presigned URLs that limit access to the OAI.
Correct selection
Create an AWS WAF web ACL that includes the same IP restrictions that exist in the EC2 security group. Associate this new web ACL with the CloudFront distribution.
Correct selection
Create an origin access identity (OAI) and associate it with the distribution. Change the permissions in the bucket policy so that only the OAI can read the objects.
Attach the existing security group that contains the IP restrictions to the Amazon CloudFront distribution.
Overall explanation
To prevent users from circumventing the controls implemented on CloudFront (using WAF or presigned URLs / signed cookies) you can use an origin access identity (OAI). An OAI is a special CloudFront user that you associate with a distribution.
The next step is to change the permissions either on your Amazon S3 bucket or on the files in your bucket so that only the origin access identity has read permission (or read and download permission). This can be implemented through a bucket policy.
To control access at the CloudFront layer the AWS Web Application Firewall (WAF) can be used. With WAF you must create an ACL that includes the IP restrictions required and then associate the web ACL with the CloudFront distribution.
CORRECT: "Create an origin access identity (OAI) and associate it with the distribution. Change the permissions in the bucket policy so that only the OAI can read the objects" is a correct answer.
CORRECT: "Create an AWS WAF web ACL that includes the same IP restrictions that exist in the EC2 security group. Associate this new web ACL with the CloudFront distribution" is also a correct answer.
INCORRECT: "Create an origin access identity (OAI) and associate it with the distribution. Generate presigned URLs that limit access to the OAI" is incorrect. Presigned URLs can be used to protect access to CloudFront but they cannot be used to limit access to an OAI.
INCORRECT: "Create an AWS WAF web ACL that includes the same IP restrictions that exist in the EC2 security group. Associate this new web ACL with the Amazon S3 bucket" is incorrect. The Web ACL should be associated with CloudFront, not S3.
INCORRECT: "Attach the existing security group that contains the IP restrictions to the Amazon CloudFront distribution" is incorrect. You cannot attach a security group to a CloudFront distribution.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
https://docs.aws.amazon.com/waf/latest/developerguide/cloudfront-features.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-waf-shield/
Domain
AWS Compute
Question 56Skipped
A web application runs in public and private subnets. The application architecture consists of a web tier and database tier running on Amazon EC2 instances. Both tiers run in a single Availability Zone (AZ).
Which combination of steps should a solutions architect take to provide high availability for this architecture? (Select TWO.)
Correct selection
1. Create an Amazon EC2 Auto Scaling group and Application Load Balancer (ALB) spanning multiple AZs
1. Create new public and private subnets in the same AZ for high availability
Correct selection
1. Create new public and private subnets in the same VPC, each in a new AZ. Migrate the database to an Amazon RDS multi-AZ deployment
1. Add the existing web application instances to an Auto Scaling group behind an Application Load Balancer (ALB)
1. Create new public and private subnets in a new AZ. Create a database using Amazon EC2 in one AZ
Overall explanation
To add high availability to this architecture both the web tier and database tier require changes. For the web tier an Auto Scaling group across multiple AZs with an ALB will ensure there are always instances running and traffic is being distributed to them.
The database tier should be migrated from the EC2 instances to Amazon RDS to take advantage of a managed database with Multi-AZ functionality. This will ensure that if there is an issue preventing access to the primary database a secondary database can take over.
CORRECT: "Create an Amazon EC2 Auto Scaling group and Application Load Balancer (ALB) spanning multiple AZs" is the correct answer.
CORRECT: "Create new public and private subnets in the same VPC, each in a new AZ. Migrate the database to an Amazon RDS multi-AZ deployment" is the correct answer.
INCORRECT: "Create new public and private subnets in the same AZ for high availability" is incorrect as this would not add high availability.
INCORRECT: "Add the existing web application instances to an Auto Scaling group behind an Application Load Balancer (ALB)" is incorrect because the existing servers are in a single subnet. For HA we need to instances in multiple subnets.
INCORRECT: "Create new public and private subnets in a new AZ. Create a database using Amazon EC2 in one AZ" is incorrect because we also need HA for the database layer.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-load-balancer.html
https://aws.amazon.com/rds/features/multi-az/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
https://digitalcloud.training/amazon-ec2-auto-scaling/
https://digitalcloud.training/amazon-rds/
Domain
AWS Compute
Question 57Skipped
A Solutions Architect for a large banking company is configuring access control within the organization for an Amazon S3 bucket containing thousands of financial records. There are 20 different teams which need to have access to this bucket, however they all need different permissions. These 20 teams correspond to 20 accounts within the banking company who are currently using AWS Organizations.

What is the simplest way to achieve this, whilst adhering to the principle of least privilege?
Correct answer
Use S3 Access points to administer different access policies to each team, and control access points using Service Control Policies within AWS Organizations.
Create a new AWS Organizations. Assign each team to a different Organizational Unit and apply to appropriate permissions granting access to the appropriate resources in the bucket.
Copy the items from the bucket to create separate versions of each Separate the items in the bucket into new buckets. Administer Bucket policies to allow each account to access the appropriate bucket.
Create the S3 Bucket in an individual account. Configure an IAM Role for each user to enable cross account access for the S3 Bucket with a permissions policy to only access the appropriate items within the bucket.
Overall explanation
Amazon S3 Access Points, a feature of S3, simplify data access for any AWS service or customer application that stores data in S3. With S3 Access Points, customers can create unique access control policies for each access point to easily control access to shared datasets. You can also control access point usage using AWS Organizations support for AWS SCPs.
CORRECT: "Use S3 Access points to administer different access policies to each team, and control access points using Service Control Policies within AWS Organizations” is the correct answer (as explained above.)
INCORRECT: "Create a new AWS Organizations. Assign each team to a different Organizational Unit and apply to appropriate permissions granting access to the appropriate resources in the bucket” is incorrect. This would not only be incredibly time consuming but totally unnecessary as you can use the preexisting AWS Organizations and the Service Control policies to control access via S3 Access Points.
INCORRECT: "Copy the items from the bucket to create separate versions of each Separate the items in the bucket into new buckets. Administer Bucket policies to allow each account to access the appropriate bucket” is incorrect. This involves a lot of operational overhead and would be prone to significant error when administering the correct permissions to each account.
INCORRECT: "Create the S3 Bucket in an individual account. Configure an IAM Role for each user to enable cross account access for the S3 Bucket with a permissions policy to only access the appropriate items within the bucket” is incorrect. This is an unnecessary complexity as it would be much easier to provision separate policies per team using S3 Access Points.
References:
https://aws.amazon.com/s3/features/access-points/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Compute
Question 59Skipped
A solutions architect is designing a new service that will use an Amazon API Gateway API on the frontend. The service will need to persist data in a backend database using key-value requests. Initially, the data requirements will be around 1 GB and future growth is unknown. Requests can range from 0 to over 800 requests per second.
Which combination of AWS services would meet these requirements? (Select TWO.)
AWS Fargate
Amazon RDS
Correct selection
Amazon DynamoDB
Amazon EC2 Auto Scaling
Correct selection
AWS Lambda
Overall explanation
In this case AWS Lambda can perform the computation and store the data in an Amazon DynamoDB table. Lambda can scale concurrent executions to meet demand easily and DynamoDB is built for key-value data storage requirements and is also serverless and easily scalable. This is therefore a cost effective solution for unpredictable workloads.
CORRECT: "AWS Lambda" is a correct answer.
CORRECT: "Amazon DynamoDB" is also a correct answer.
INCORRECT: "AWS Fargate" is incorrect as containers run constantly and therefore incur costs even when no requests are being made.
INCORRECT: "Amazon EC2 Auto Scaling" is incorrect as this uses EC2 instances which will incur costs even when no requests are being made.
INCORRECT: "Amazon RDS" is incorrect as this is a relational database not a No-SQL database. It is therefore not suitable for key-value data storage requirements.
References:
https://aws.amazon.com/lambda/features/
https://aws.amazon.com/dynamodb/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/
https://digitalcloud.training/amazon-dynamodb/
Domain
AWS Compute
Question 61Skipped
A Solutions Architect has placed an Amazon CloudFront distribution in front of their web server, which is serving up a highly accessed website, serving content globally. The Solutions Architect needs to dynamically route the user to a new URL depending on where the user is accessing from, through running a particular script. This dynamic routing will happen on every request, and as a result requires the code to run at extremely low latency, and low cost.
What solution will best achieve this goal?
Use Route 53 Geo Proximity Routing to route users’ traffic to your resources based on their geographic location.
Correct answer
At the Edge Location, run your code with CloudFront Functions.
Use Path Based Routing to route each user to the appropriate webpage behind an Application Load Balancer.
Redirect traffic by running your code within a Lambda function using Lambda@Edge.
Overall explanation
With CloudFront Functions in Amazon CloudFront, you can write lightweight functions in JavaScript for high-scale, latency-sensitive CDN customizations. Your functions can manipulate the requests and responses that flow through CloudFront, perform basic authentication and authorization, generate HTTP responses at the edge, and more. CloudFront Functions is approximately 1/6th the cost of Lambda@Edge and is extremely low latency as the functions are run on the host in the edge location, instead of the running on a Lambda function elsewhere.
CORRECT: "At the Edge Location, run your code with CloudFront Functions” is the correct answer (as explained above.)
INCORRECT: "Redirect traffic by running your code within a Lambda function using Lambda@Edge” is incorrect. Although you could achieve this using Lambda@Edge, the question states the need for the lowest latency possible, and comparatively the lowest latency option is CloudFront Functions.
INCORRECT: "Use Path Based Routing to route each user to the appropriate webpage behind an Application Load Balancer” is incorrect. This architecture does not account for the fact that custom code needs to be run to make this happen.
INCORRECT: "Use Route 53 Geo Proximity Routing to route users’ traffic to your resources based on their geographic location.'' is incorrect. This may work, however again it does not account for the fact that custom code needs to be run to make this happen.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cloudfront-functions.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Compute
Question 63Skipped
A Solutions Architect is rearchitecting an application with decoupling. The application will send batches of up to 1000 messages per second that must be received in the correct order by the consumers.
Which action should the Solutions Architect take?
Correct answer
Create an Amazon SQS FIFO queue
Create an Amazon SQS Standard queue
Create an Amazon SNS topic
Create an AWS Step Functions state machine
Overall explanation
Only FIFO queues guarantee the ordering of messages and therefore a standard queue would not work. The FIFO queue supports up to 3,000 messages per second with batching so this is a supported scenario.


CORRECT: "Create an Amazon SQS FIFO queue" is the correct answer.
INCORRECT: "Create an Amazon SQS Standard queue" is incorrect as it does not guarantee ordering of messages.
INCORRECT: "Create an Amazon SNS topic" is incorrect. SNS is a notification service and a message queue is a better fit for this use case.
INCORRECT: "Create an AWS Step Functions state machine" is incorrect. Step Functions is a workflow orchestration service and is not useful for this scenario.
References:
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-quotas.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Compute
Question 65Skipped
A company has acquired another business and needs to migrate their 50TB of data into AWS within 1 month. They also require a secure, reliable and private connection to the AWS cloud.
How are these requirements best accomplished?
Provision an AWS VPN CloudHub connection and migrate the data over redundant links
Launch a Virtual Private Gateway (VPG) and migrate the data over the AWS VPN
Provision an AWS Direct Connect connection and migrate the data over the link
Correct answer
Migrate data using AWS Snowball. Provision an AWS VPN initially and order a Direct Connect link
Overall explanation
AWS Direct Connect provides a secure, reliable and private connection. However, lead times are often longer than 1 month so it cannot be used to migrate data within the timeframes. Therefore, it is better to use AWS Snowball to move the data and order a Direct Connect connection to satisfy the other requirement later on. In the meantime the organization can use an AWS VPN for secure, private access to their VPC.
CORRECT: "Migrate data using AWS Snowball. Provision an AWS VPN initially and order a Direct Connect link" is the correct answer.
INCORRECT: "Provision an AWS Direct Connect connection and migrate the data over the link" is incorrect due to the lead time for installation.
INCORRECT: "Launch a Virtual Private Gateway (VPG) and migrate the data over the AWS VPN" is incorrect. A VPG is the AWS-side of an AWS VPN. A VPN does not provide a private connection and is not reliable as you can never guarantee the latency over the Internet
INCORRECT: "Provision an AWS VPN CloudHub connection and migrate the data over redundant links" is incorrect. AWS VPN CloudHub is a service for connecting multiple sites into your VPC over VPN connections. It is not used for aggregating links and the limitations of Internet bandwidth from the company where the data is stored will still be an issue. It also uses the public Internet so is not a private or reliable connection.
References:
https://aws.amazon.com/snowball/
https://aws.amazon.com/directconnect/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-direct-connect/
https://digitalcloud.training/aws-migration-services/
Domain
AWS Compute
Question 10Skipped
A digital marketing agency manages numerous client websites and apps on AWS. Each AWS resource is supposed to be tagged by the account for tracking and backup purposes. The agency wants to ensure that all AWS resources, including untagged ones, are backed up properly to minimize data loss risks.
Which solution will meet these requirements with the LEAST operational overhead?
Rely on each account owner to identify their untagged resources and then use AWS Backup for backing up.
Use AWS Lambda to periodically scan for untagged resources, add necessary tags, and then set up AWS Backup.
Manually search for all untagged resources in each AWS service. Once identified, tag them appropriately and set up AWS Backup for each service separately.
Correct answer
Use AWS Config to identify all untagged resources and tag them programmatically. Then, use AWS Backup to automate the backup of all AWS resources based on tags.
Overall explanation
This solution is the most operationally efficient due to the powerful combination of AWS Config and AWS Backup.
AWS Config: This service enables you to assess, audit, and evaluate the configurations of your AWS resources. AWS Config continuously monitors and records your AWS resource configurations and allows you to automate the evaluation of recorded configurations against desired configurations. You can use AWS Config to review changes in configurations and relationships between AWS resources, dive into detailed resource configuration histories, and determine your overall compliance against the configurations specified in your internal guidelines. In this scenario, AWS Config can be utilized to identify all resources that lack proper tags.
Tagging: Tags can be added to AWS resources programmatically. By tagging resources, you organize them into groups and subgroups, which can be based on purpose, owner, environment, or other criteria. In this context, tagging resources allows AWS Backup to identify and group resources that need to be backed up.
AWS Backup: AWS Backup is a fully managed backup service that makes it easy to centralize and automate the back up of data across AWS services. You can use AWS Backup to protect several AWS resource types, including Amazon EBS volumes, Amazon RDS databases, Amazon DynamoDB tables, Amazon EFS file systems, and AWS Storage Gateway volumes. It offers a centralized dashboard where you can manage all backups and allows you to automate and monitor backups across AWS services using policies.
With AWS Config identifying and tagging untagged resources, and AWS Backup automating the backup of tagged resources, this solution requires minimal operational overhead while ensuring all resources are adequately backed up.
CORRECT: "Use AWS Config to identify all untagged resources and tag them programmatically. Then, use AWS Backup to automate the backup of all AWS resources based on tags" is the correct answer (as explained above.)
INCORRECT: "Manually search for all untagged resources in each AWS service. Once identified, tag them appropriately and set up AWS Backup for each service separately" is incorrect.
Searching for untagged resources manually in each service and setting up AWS Backup separately for each one would require a significant amount of operational overhead.
INCORRECT: "Rely on each account owner to identify their untagged resources and then use AWS Backup for backing up" is incorrect.
Relying on individual account owners could result in inconsistency and increase the risk of missed resources or backups. Centralized backup management using AWS Backup is more efficient.
INCORRECT: "Use AWS Lambda to periodically scan for untagged resources, add necessary tags, and then set up AWS Backup" is incorrect.
Although AWS Lambda could be used to scan for untagged resources and add necessary tags, this would require developing and maintaining a custom script. AWS Config can handle this process with less operational overhead.
References:
https://docs.aws.amazon.com/aws-backup/latest/devguide/assigning-resources.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-config/
Domain
AWS Compute
Question 16Skipped
A media company is running a production workload on thousands of EC2 instances which run a custom solution powered by third-party software. This software is subjected to regular updates and patches by the third-party organization.
How can a solutions architect patch all the instances quickly to remediate a security exposure?
Create an AWS Lambda function to apply the patch to all EC2 instances.
Use AWS Systems Manager Run Command to run a custom command that applies the patch to all EC2 instances.
Schedule an AWS Systems Manager maintenance window to apply the patch to all EC2 instances.
Correct answer
Configure AWS Systems Manager Patch Manager to apply the patch to all EC2 instances.
Overall explanation

Patch Manager automates the process of patching Windows and Linux managed instances. Use this feature of AWS Systems Manager to scan your instances for missing patches or scan and install missing patches. You can install patches individually or to large groups of instances by using Amazon EC2 tags.
CORRECT: "Configure AWS Systems Manager Patch Manager to apply the patch to all EC2 instances" is the correct answer (as explained above.)
INCORRECT: "Create an AWS Lambda function to apply the patch to all EC2 instances" is incorrect. Since AWS already provides an out of the box solution of creating customizable patch groups enabling easy patching of EC2 instances, writing custom AWS Lambda is not the quickest/easiest solution.
INCORRECT: "Schedule an AWS Systems Manager maintenance window to apply the patch to all EC2 instances" is incorrect. This is a valid option and would hold in case there’s a specific downtime or maintenance window when the patches are to be applied.
INCORRECT: "Use AWS Systems Manager Run Command to run a custom command that applies the patch to all EC2 instances" is incorrect. This option wouldn’t work since the requirement is to have the patching done as quickly as possible and this would slow down the process.
References:
https://aws.amazon.com/blogs/mt/patching-your-windows-ec2-instances-using-aws-systems-manager-patch-manager/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-systems-manager/
Domain
AWS Compute
Question 25Skipped
A company has several AWS accounts each with multiple Amazon VPCs. The company must establish routing between all private subnets. The architecture should be simple and allow transitive routing to occur.
How should the network connectivity be configured?
Create a transitive VPC peering connection between each Amazon VPC and configure route tables
Create a hub-and-spoke topology with AWS App Mesh and use AWS Resource Access Manager to share route tables
Create an AWS Managed VPN between each Amazon VPC and configure route tables
Correct answer
Create an AWS Transit Gateway and share it with each account using AWS Resource Access Manager
Overall explanation
You can build a hub-and-spoke topology with AWS Transit Gateway that supports transitive routing. This simplifies the network topology and adds additional features over VPC peering. AWS Resource Access Manager can be used to share the connection with the other AWS accounts.


CORRECT: "Create an AWS Transit Gateway and share it with each account using AWS Resource Access Manager" is the correct answer.
INCORRECT: "Create a transitive VPC peering connection between each Amazon VPC and configure route tables" is incorrect. You cannot create transitive connections with VPC peering.
INCORRECT: "Create an AWS Managed VPN between each Amazon VPC and configure route tables" is incorrect. This is a much more complex solution compared to AWS Transit Gateway so is not the best option.
INCORRECT: "Create a hub-and-spoke topology with AWS App Mesh and use AWS Resource Access Manager to share route tables" is incorrect. AWS App Mesh is used for application-level networking for microservices applications.
References:
https://aws.amazon.com/blogs/aws/new-use-an-aws-transit-gateway-to-simplify-your-network-architecture/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 27Skipped
A three-tier web application is composed of a front end hosted on an Amazon EC2 instance in public subnet, application middleware hosted on EC2 in a private subnet and a database hosted on an Amazon RDS MySQL database in a private subnet. The database layer should be restricted to only allow incoming connections from the application.
Which of the following options makes sure that database can only be accessed by the application layer?
Create a new route table that excludes the route to the public subnets' CIDR blocks. Associate the route table with the database subnets.
Create a new peering connection between the public subnets and the private subnets. Create a different peering connection between the private subnets and the database subnets.
Correct answer
Create a security group that allows inbound traffic from the security group that is assigned to instances in the private subnets. Attach the security group to the DB instances.
Create a security group that denies inbound traffic from the security group that is assigned to instances in the public subnets. Attach the security group to the DB instances.
Overall explanation
Security groups are stateful. All inbound traffic is blocked by default in custom security groups. If you create an inbound rule allowing traffic in, that traffic is automatically allowed back out again. You cannot block specific IP address using Security groups (instead use Network Access Control Lists).
In this case the solution is to allow inbound traffic from the security group ID of the security group attached to the application layer. The rule should specify the appropriate protocol and port. This will ensure only the application layer can communicate with the database.

CORRECT: "Create a security group that allows inbound traffic from the security group that is assigned to instances in the private subnets. Attach the security group to the DB instances" is the correct answer (as explained above.)
INCORRECT: "Create a new route table that excludes the route to the public subnets' CIDR blocks. Associate the route table with the database subnets" is incorrect. This would simply stop routing from working within the VPC.
INCORRECT: "Create a security group that denies inbound traffic from the security group that is assigned to instances in the public subnets. Attach the security group to the DB instances" is incorrect.
You cannot create deny rules with security groups.
INCORRECT: "Create a new peering connection between the public subnets and the private subnets. Create a different peering connection between the private subnets and the database subnets" is incorrect.
Peering is used when multiple VPC’s are to be connected with each other hence this is also an incorrect option.
References
https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Compute
Question 30Skipped
A financial services company is currently using 500 Amazon EC2 instances to run batch-processing workloads to analyze financial information on a periodic basis. The organization needs to install a third-party tool on all these instances as quickly and as efficiently as possible and will have to carry out similar tasks on an ongoing basis going forward. The solution also needs to scale for the addition of future EC2 instances.
What should a solutions architect do to meet these requirements in the easiest way possible?
Use AWS Systems Manager Maintenance Windows to install the tool on all the EC2 instances within a set period of time.
Create an AWS Lambda Function which will make configuration changes to all the EC2 instances. Validate the tool has been installed using another Lambda function.
Use AWS Systems Manager Patch Manager to install the tool on all the EC2 instances within a single patch.
Correct answer
Use AWS Systems Manager Run Command to run a custom command that installs the tool on all the EC2 instances.
Overall explanation
AWS Systems Manager Run command is designed to run commands across a large group of instances without having to SSH into all your instances and run the same command multiple times. You can easily run the same command to all the managed nodes as part of the workload, without having to maintain access keys or individual access for each instance.
CORRECT: "Use AWS Systems Manager Run Command to run a custom command that installs the tool on all the EC2 instances" is the correct answer (as explained above.)
INCORRECT: "Create an AWS Lambda Function which will make configuration changes to all of the EC2 instances. Validate the tool has been installed using another Lambda function" is incorrect. Whilst this may be possible, the code that would be required to create and test this solution would be difficult to design and would not scale effectively as AWS Systems Manager Run Command.
INCORRECT: "Use AWS Systems Manager Patch Manager to install the tool on all of the EC2 instances within a single patch" is incorrect. AWS Systems Manager Patch Manager is designed to apply patches to EC2 instances and is not designed to run commands across a large group of instances.
INCORRECT: "Use AWS Systems Manager Maintenance Windows to install the tool on all of the EC2 instances within a set period of time" is incorrect. AWS Systems Manager Maintenance Windows is designed to select a defined window of time in which you EC2 instances will be patched and is not capable of running commands across multiple instances.
References:
https://docs.aws.amazon.com/systems-manager/latest/userguide/execute-remote-commands.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-systems-manager/
Domain
AWS Compute
Question 44Skipped
A telemarketing company has developed customer call center functionality on AWS. The company plans to enhance the current application by enabling support for multiple speaker recognition and transcript generation. They also want to query the transcript files to analyze business patterns.
Which solution will meet these requirements?
Correct answer
Use Amazon Transcribe for multiple speaker recognition. Use Amazon Athena for transcript file analysis.
Use Amazon Rekognition for multiple speaker recognition. Store the transcript files in Amazon S3. Use Amazon Textract for transcript file analysis.
Use Amazon Rekognition for multiple speaker recognition. Store the transcript files in Amazon S3. Use machine learning models for transcript file analysis.
Use Amazon Translate for multiple speaker recognition. Store the transcript files in Amazon Redshift. Use SQL queries for transcript file analysis.
Overall explanation
Amazon Transcribe converts audio input into text, which opens the door for various text analytics applications on voice input. For instance, by using Amazon Comprehend on the converted text data from Amazon Transcribe, customers can perform sentiment analysis or extract entities and key phrases.
Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run.

CORRECT: "Use Amazon Transcribe for multiple speaker recognition. Use Amazon Athena for transcript file analysis" is the correct answer (as explained above.)
INCORRECT: " Use Amazon Rekognition for multiple speaker recognition. Store the transcript files in Amazon S3. Use machine learning models for transcript file analysis" is incorrect.
Amazon Rekognition Video can detect objects, scenes, faces, celebrities, text, and inappropriate content in videos. You can also search for faces appearing in a video using your own repository or collection of face images.
INCORRECT: "Use Amazon Translate for multiple speaker recognition. Store the transcript files in Amazon Redshift. Use SQL queries for transcript file analysis" is incorrect.
Amazon Translate can provide automatic translation to enable cross-lingual communications between users for your applications.
INCORRECT: "Use Amazon Rekognition for multiple speaker recognition. Store the transcript files in Amazon S3. Use Amazon Textract for transcript file analysis" is incorrect.
As mentioned above, Rekognition is better suited for identifying content in videos. Also,
Amazon Textract is a machine learning (ML) service that automatically extracts text, handwriting, and data from scanned documents.
References:
https://aws.amazon.com/blogs/machine-learning/automating-the-analysis-of-multi-speaker-audio-files-using-amazon-transcribe-and-amazon-athena/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-machine-learning-services/
Domain
AWS Compute
Question 57Skipped
A game development company is planning to build a cloud-based game platform on AWS. The player activity patterns are unpredictable and could remain idle for extended periods. Only players who have purchased the game should have the ability to log in and play.
Which combination of steps will meet these requirements MOST cost-effectively? (Select THREE.)
Correct selection
Use AWS Cognito User Pools to handle user authentication.
Use AWS Cognito Identity Pools to handle user authentication.
Correct selection
Implement an AWS Lambda function to fetch player information from Amazon DynamoDB. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the Lambda function.
Use Amazon S3 static web hosting with HTML, CSS, and JS. Use Amazon CloudFront to distribute the frontend game interface.
Set up an Amazon Elastic Container Service (Amazon ECS) service behind an Application Load Balancer to fetch player information from Amazon RDS. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the ECS service.
Correct selection
Leverage AWS Amplify to serve the frontend game interface with HTML, CSS, and JS. Use the integrated Amazon CloudFront configuration for distribution.
Overall explanation
AWS Lambda is a cost-effective solution for unpredictable traffic patterns due to its pay-per-use pricing model. DynamoDB is also a cost-effective and highly scalable solution for storing user data. The API Gateway provides a HTTP-based endpoint that can be used to expose the Lambda function.
AWS Cognito User Pools provide user directory features including sign-up and sign-in services, which are suitable for managing game user authentication.
AWS Amplify simplifies the process of hosting web applications with automated deployment processes. It also integrates with CloudFront, providing a global content delivery network to efficiently serve the game interface.
CORRECT: "Implement an AWS Lambda function to fetch player information from Amazon DynamoDB. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the Lambda function" is a correct answer (as explained above.)
CORRECT: "Use AWS Cognito User Pools to handle user authentication" is also a correct answer (as explained above.)
CORRECT: "Leverage AWS Amplify to serve the frontend game interface with HTML, CSS, and JS. Use the integrated Amazon CloudFront configuration for distribution" is also a correct answer (as explained above.)
INCORRECT: "Set up an Amazon Elastic Container Service (Amazon ECS) service behind an Application Load Balancer to fetch player information from Amazon RDS. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the ECS service" is incorrect.
Using Amazon ECS might be an overkill for this scenario and might not be as cost-effective compared to Lambda and DynamoDB, especially for unpredictable and possibly idle traffic.
INCORRECT: "Use AWS Cognito Identity Pools to handle user authentication" is incorrect.
Cognito Identity Pools are used for granting access to AWS resources rather than handling user authentication.
INCORRECT: "Use Amazon S3 static web hosting with HTML, CSS, and JS. Use Amazon CloudFront to distribute the frontend game interface" is incorrect.
While you could host a static website on S3 and use CloudFront for distribution, AWS Amplify can provide additional capabilities tailored to modern web applications. Furthermore, Amplify's automated deployment processes can provide a more streamlined and efficient approach to managing the game's frontend compared to managing separate S3 and CloudFront configurations.
References:
https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html
https://aws.amazon.com/amplify/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Compute
Question 62Skipped
A media company has grown significantly in the past few months and the management team are concerned about compliance, governance, auditing, and security. The management team requires that configuration changes are tracked a history of API calls is recorded.
What should a solutions architect do to meet these requirements?
Use AWS Config to track configuration changes and Amazon CloudWatch to record API calls.
Use AWS CloudTrail to track configuration changes and AWS Config to record API calls.
Use AWS CloudTrail to track configuration changes and Amazon CloudWatch to record API calls.
Correct answer
Use AWS Config to track configuration changes and AWS CloudTrail to record API calls.
Overall explanation
As per definition of AWS CloudTrail and AWS Config:
CloudTrail is a web service that records AWS API calls for your AWS account and delivers log files to an Amazon S3 bucket. The recorded information includes the identity of the user, the start time of the AWS API call, the source IP address, the request parameters, and the response elements returned by the service.
AWS Config tracks changes in the configuration of your AWS resources, and it regularly sends updated configuration details to an Amazon S3 bucket that you specify. For each resource type that AWS Config records, it sends a configuration history file every six hours.
CORRECT: "Use AWS Config to track configuration changes and AWS CloudTrail to record API calls" is the correct answer (as explained above.)
INCORRECT: "Use AWS CloudTrail to track configuration changes and AWS Config to record API calls " is incorrect.
This option is the reverse of what’s needed, AWS config, as the name suggests, is used to track the configuration changes in AWS accounts.
INCORRECT: "Use AWS Config to track configuration changes and Amazon CloudWatch to record API calls" is incorrect. CloudWatch is used for performance monitoring, not tracking API calls.
INCORRECT: "Use AWS CloudTrail to track configuration changes and Amazon CloudWatch to record API calls" is incorrect. CloudTrail is not the right service for tracking configuration changes hence this option is incorrect.
References:
https://docs.aws.amazon.com/awscloudtrail/latest/APIReference/Welcome.html
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/TrackingChanges.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-config/
https://digitalcloud.training/aws-cloudtrail/
Domain
AWS Compute
Question 5Skipped
An application runs on Amazon EC2 instances in a private subnet. The EC2 instances process data that is stored in an Amazon S3 bucket. The data is highly confidential and a private and secure connection is required between the EC2 instances and the S3 bucket.
Which solution meets these requirements?
Correct answer
Set up S3 bucket policies to allow access from a VPC endpoint.
Configure encryption for the S3 bucket using an AWS KMS key.
Configure a custom SSL/TLS certificate on the S3 bucket.
Set up an IAM policy to grant read-write access to the S3 bucket.
Overall explanation
A gateway VPC endpoint can be used to access an Amazon S3 bucket using private IP addresses. To further secure the solution an S3 bucket policy can be created that restricts access to the VPC endpoint so connections cannot be made to the bucket from other sources.
CORRECT: "Set up S3 bucket policies to allow access from a VPC endpoint" is the correct answer.
INCORRECT: "Set up an IAM policy to grant read-write access to the S3 bucket" is incorrect. This does not enable private access from EC2. A gateway VPC endpoint is required.
INCORRECT: "Configure encryption for the S3 bucket using an AWS KMS key" is incorrect. This will encrypt data at rest but does not secure the connection to the bucket or ensure private connections must be made.
INCORRECT: "Configure a custom SSL/TLS certificate on the S3 bucket" is incorrect. You cannot add a custom SSL/TLS certificate to Amazon S3.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies-vpc-endpoint.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 8Skipped
A company operates multiple AWS accounts under AWS Organizations. To better manage the costs, the company wants to allocate different budgets for each of these accounts. The company also wants to prevent additional resource provisioning in an AWS account if it reaches its allocated budget before the end of the budget period.
Which combination of solutions will meet these requirements? (Select THREE.)
Correct selection
Configure alerts in AWS Budgets to notify the company when an account is about to reach its budget threshold. Then use a budget action that links to the IAM role to prevent additional resource provisioning.
Use AWS Budgets in the AWS Management Console to set up budgets and specify the cost threshold for each AWS account.
Create an IAM user with adequate permissions to allow AWS Budgets to enforce budget actions.
Set up an alert in AWS Budgets to notify the company when a particular account meets its budget threshold. Enable real-time monitoring for immediate notification.
Correct selection
Set up an IAM role with the necessary permissions that allow AWS Budgets to execute budget actions.
Correct selection
Use AWS Budgets to establish different budgets for each AWS account. Configure the budgets in the Billing and Cost Management console.
Overall explanation
AWS Budgets is a tool that enables you to set custom cost and usage budgets. You can set your budget amount, and AWS provides you with estimated charges and forecasted costs for your AWS usage. Configuring the budgets in the Billing and Cost Management console is a recommended step.
AWS Budgets can execute budget actions (like preventing additional resource provisioning) using an IAM role with the necessary permissions.
Configuring alerts in AWS Budgets and linking a budget action to an IAM role for automatic prevention of additional resource provisioning is a correct and efficient way to manage costs.
CORRECT: "Use AWS Budgets to establish different budgets for each AWS account. Configure the budgets in the Billing and Cost Management console" is a correct answer (as explained above.)
CORRECT: "Set up an IAM role with the necessary permissions that allow AWS Budgets to execute budget actions" is also a correct answer (as explained above.)
CORRECT: "Configure alerts in AWS Budgets to notify the company when an account is about to reach its budget threshold. Then use a budget action that links to the IAM role to prevent additional resource provisioning" is also a correct answer (as explained above.)
INCORRECT: "Use AWS Budgets in the AWS Management Console to set up budgets and specify the cost threshold for each AWS account" is incorrect.
While AWS Budgets can indeed be set up in the AWS Management Console, the budgets aren't set in the context of cost thresholds for each AWS account. This option is not fully accurate.
INCORRECT: "Create an IAM user with adequate permissions to allow AWS Budgets to enforce budget actions" is incorrect.
Although you can create an IAM user with necessary permissions, using an IAM role is generally a better practice. An IAM user is an entity that you create in AWS to represent the person or service that uses it to interact with AWS, while an IAM role is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. A role does not have long-term credentials associated with it like an IAM user does.
INCORRECT: "Set up an alert in AWS Budgets to notify the company when a particular account meets its budget threshold. Enable real-time monitoring for immediate notification" is incorrect.
AWS Budgets doesn't allow for real-time monitoring; the data can be delayed up to 24 hours. The frequency of budget alert notifications is not customizable to the minute or hour; they are typically sent out daily, weekly, or when a certain threshold is crossed.
References:
https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-controls.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-cost-management/
Domain
AWS Compute
Question 14Skipped
An application uses an Amazon RDS database and Amazon EC2 instances in a web tier. The web tier instances must not be directly accessible from the internet to improve security.
How can a Solutions Architect meet these requirements?
Correct answer
Launch the EC2 instances in a private subnet and create an Application Load Balancer in a public subnet
Launch the EC2 instances in a public subnet and create an Application Load Balancer in a public subnet
Launch the EC2 instances in a public subnet and use AWS WAF to protect the instances from internet-based attacks
Launch the EC2 instances in a private subnet with a NAT gateway and update the route table
Overall explanation
To prevent direct connectivity to the EC2 instances from the internet you can deploy your EC2 instances in a private subnet and have the ELB in a public subnet. To configure this you must enable a public subnet in the ELB that is in the same AZ as the private subnet.


CORRECT: "Launch the EC2 instances in a private subnet and create an Application Load Balancer in a public subnet" is the correct answer.
INCORRECT: "Launch the EC2 instances in a private subnet with a NAT gateway and update the route table" is incorrect. This configuration will not allow the application to be accessible from the internet, the aim is to only prevent direct access to the EC2 instances.
INCORRECT: "Launch the EC2 instances in a public subnet and use AWS WAF to protect the instances from internet-based attacks" is incorrect. With the EC2 instances in a public subnet, direct access from the internet is possible. It only takes a security group misconfiguration or software exploit and the instance becomes vulnerable to attack.
INCORRECT: "Launch the EC2 instances in a public subnet and create an Application Load Balancer in a public subnet" is incorrect. The EC2 instances should be launched in a private subnet.
References:
https://aws.amazon.com/premiumsupport/knowledge-center/public-load-balancer-private-ec2/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 17Skipped
A financial institution wants to use machine learning (ML) algorithms to detect potential fraudulent transactions. They need to create ML models based on their vast financial transaction data and integrate these models into their business intelligence system for real-time decision-making. The solution should require minimal operational overhead.
Which solution will best meet these requirements?
Use Amazon Comprehend for analyzing the transaction data and Amazon Elasticsearch for visualization.
Correct answer
Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization.
Use a pre-built ML Amazon Machine Image (AMI) from the AWS Marketplace to build and train models and use AWS Athena for data visualization.
1. Use AWS Glue to perform ETL jobs on the transaction data and use Amazon Forecast for predictive analytics.
Overall explanation
Amazon SageMaker is a fully managed service that provides every developer and data scientist with the ability to build, train, and deploy machine learning models quickly. It can directly connect with data sources and has built-in algorithms to ease the ML process.
Amazon QuickSight is a business intelligence tool that can be used to create dashboards for data visualization. This combination perfectly suits the requirement.
CORRECT: "Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization" is the correct answer (as explained above.)
INCORRECT: "Use AWS Glue to perform ETL jobs on the transaction data and use Amazon Forecast for predictive analytics" is incorrect.
AWS Glue is primarily used for ETL jobs - cleaning, preparing, and moving data. Amazon Forecast is a fully managed service for time-series forecasting, which might not be a complete solution for detecting fraudulent transactions.
INCORRECT: "Use a pre-built ML Amazon Machine Image (AMI) from the AWS Marketplace to build and train models and use AWS Athena for data visualization" is incorrect.
AWS Marketplace ML AMIs can be used to create and train models, but this will require manual operational effort in terms of setting up and managing the instances. Athena is a query service and does not provide data visualization capabilities that a business intelligence tool like QuickSight provides.
INCORRECT: "Use Amazon Comprehend for analyzing the transaction data and Amazon Elasticsearch for visualization" is incorrect.
Amazon Comprehend is primarily used for natural language processing (NLP), which isn't suited for detecting fraudulent transactions. Elasticsearch is a search and analytics engine and might not be the best tool for the use case described here.
References:
https://aws.amazon.com/sagemaker/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-machine-learning-services/
Domain
AWS Compute
Question 19Skipped
A media company hosts several terabytes of multimedia content across multiple AWS accounts. The company uses AWS Lake Formation to manage its data lake. The company's marketing team needs to securely access and analyze selective data from various accounts for targeted advertisement campaigns.
Which solution will meet these requirements with the LEAST operational overhead?
Correct answer
Utilize Lake Formation tag-based access control to authorize and grant cross-account permissions for the required data to the marketing team accounts.
Replicate the required data to a shared account. Create an IAM access role in that account. Grant access by defining a permission policy that includes users from the marketing team accounts as trusted entities.
Use the Lake Formation permissions Grant command in each account where the data is stored to permit the required marketing team users to access the data.
Use AWS DataSync to synchronize the necessary data to the marketing team accounts.
Overall explanation
With Lake Formation tag-based access control, you can manage permissions using tags and grant cross-account permissions, which would meet the requirements with the least operational overhead.
CORRECT: "Utilize Lake Formation tag-based access control to authorize and grant cross-account permissions for the required data to the marketing team accounts" is the correct answer (as explained above.)
INCORRECT: "Replicate the required data to a shared account. Create an IAM access role in that account. Grant access by defining a permission policy that includes users from the marketing team accounts as trusted entities" is incorrect.
This solution involves the unnecessary replication of data, leading to increased storage costs and operational overhead.
INCORRECT: "Use the Lake Formation permissions Grant command in each account where the data is stored to permit the required marketing team users to access the data" is incorrect.
The Grant command would need to be manually executed in each account where data is stored, which could lead to increased operational overhead, particularly if the data is spread across many accounts.
INCORRECT: "Use AWS DataSync to synchronize the necessary data to the marketing team accounts" is incorrect.
AWS DataSync is designed for online data transfer, not for granting access permissions to data already stored in AWS, so this would not meet the requirement.
References:
https://docs.aws.amazon.com/lake-formation/latest/dg/tag-based-access-control.html
Domain
AWS Compute
Question 22Skipped
A company runs a streaming media service and the content is stored on Amazon S3. The media catalog server pulls updated content from S3 and can issue over 1 million read operations per second for short periods. Latency must be kept under 5ms for these updates. Which solution will provide the BEST performance for the media catalog updates?
Implement an Instance store volume on the media catalog server
Implement Amazon CloudFront and cache the content at Edge Locations
Update the application code to use an Amazon DynamoDB Accelerator cluster
Correct answer
Update the application code to use an Amazon ElastiCache for Redis cluster
Overall explanation
Some applications, such as media catalog updates require high frequency reads, and consistent throughput. For such applications, customers often complement S3 with an in-memory cache, such as Amazon ElastiCache for Redis, to reduce the S3 retrieval cost and to improve performance.
ElastiCache for Redis is a fully managed, in-memory data store that provides sub-millisecond latency performance with high throughput. ElastiCache for Redis complements S3 in the following ways:
- Redis stores data in-memory, so it provides sub-millisecond latency and supports incredibly high requests per second.
- It supports key/value based operations that map well to S3 operations (for example, GET/SET => GET/PUT), making it easy to write code for both S3 and ElastiCache.
- It can be implemented as an application side cache. This allows you to use S3 as your persistent store and benefit from its durability, availability, and low cost. Your applications decide what objects to cache, when to cache them, and how to cache them.
In this example the media catalog is pulling updates from S3 so the performance between these components is what needs to be improved. Therefore, using ElastiCache to cache the content will dramatically increase the performance.
CORRECT: "Update the application code to use an Amazon ElastiCache for Redis cluster" is the correct answer.
INCORRECT: "Implement Amazon CloudFront and cache the content at Edge Locations" is incorrect. CloudFront is good for getting media closer to users but in this case we’re trying to improve performance within the data center moving data from S3 to the media catalog server.
INCORRECT: "Update the application code to use an Amazon DynamoDB Accelerator cluster" is incorrect. DynamoDB Accelerator (DAX) is used with DynamoDB but is unsuitable for use with Amazon S3.
INCORRECT: "Implement an Instance store volume on the media catalog server" is incorrect. This will improve local disk performance but will not improve reads from Amazon S3.
References:
https://aws.amazon.com/blogs/storage/turbocharge-amazon-s3-with-amazon-elasticache-for-redis/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-elasticache/
Domain
AWS Compute
Question 27Skipped
An application runs on EC2 instances in a private subnet behind an Application Load Balancer in a public subnet. The application is highly available and distributed across multiple AZs. The EC2 instances must make API calls to an internet-based service. How can the Solutions Architect enable highly available internet connectivity?
Configure an internet gateway. Add a route to the gateway to each private subnet route table
Create a NAT instance in the private subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT instance
Create a NAT gateway and attach it to the VPC. Add a route to the gateway to each private subnet route table
Correct answer
Create a NAT gateway in the public subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT gateway
Overall explanation
The only solution presented that actually works is to create a NAT gateway in the public subnet of each AZ. They must be created in the public subnet as they gain public IP addresses and use an internet gateway for internet access.
The route tables in the private subnets must then be configured with a route to the NAT gateway and then the EC2 instances will be able to access the internet (subject to security group configuration).
CORRECT: "Create a NAT gateway in the public subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT gateway" is the correct answer.
INCORRECT: "Create a NAT gateway and attach it to the VPC. Add a route to the gateway to each private subnet route table" is incorrect. You do not attach NAT gateways to VPCs, you add them to public subnets.
INCORRECT: "Configure an internet gateway. Add a route to the gateway to each private subnet route table" is incorrect. You cannot add a route to an internet gateway to a private subnet route table (private EC2 instances don’t even have public IP addresses).
INCORRECT: "Create a NAT instance in the private subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT instance" is incorrect. You do not create NAT instances in private subnets, they must be created in public subnets.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 28Skipped
A Solutions Architect is designing an application that will run on Amazon EC2 instances. The application will use Amazon S3 for storing image files and an Amazon DynamoDB table for storing customer information. The security team require that traffic between the EC2 instances and AWS services must not traverse the public internet.
How can the Solutions Architect meet the security team’s requirements?
Create a virtual private gateway and configure VPC route tables.
Correct answer
Create gateway VPC endpoints for Amazon S3 and DynamoDB.
Create a NAT gateway in a public subnet and configure route tables.
Create interface VPC endpoints for Amazon S3 and DynamoDB.
Overall explanation
A VPC endpoint enables private connections between your VPC and supported AWS services and VPC endpoint services powered by AWS PrivateLink. A gateway endpoint is used for Amazon S3 and Amazon DynamoDB. You specify a gateway endpoint as a route table target for traffic that is destined for the supported AWS services.
CORRECT: "Create gateway VPC endpoints for Amazon S3 and DynamoDB" is the correct answer.
INCORRECT: "Create a NAT gateway in a public subnet and configure route tables" is incorrect. A NAT gateway is used for enabling internet connectivity for instances in private subnets. Connections will traverse the internet.
INCORRECT: "Create interface VPC endpoints for Amazon S3 and DynamoDB" is incorrect. You should use a gateway VPC endpoint for S3 and DynamoDB.
INCORRECT: "Create a virtual private gateway and configure VPC route tables" is incorrect VGWs are used for VPN connections, they do not allow access to AWS services from a VPC.
References:
https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Compute
Question 33Skipped
A company is deploying an analytics application on AWS Fargate. The application requires connected storage that offers concurrent access to files and high performance.
Which storage option should the solutions architect recommend?
Correct answer
1. Create an Amazon EFS file share and establish an IAM role that allows Fargate to communicate with Amazon EFS.
1. Create an Amazon S3 bucket for the application and establish an IAM role for Fargate to communicate with Amazon S3.
1. Create an Amazon EBS volume for the application and establish an IAM role that allows Fargate to communicate with Amazon EBS.
1. Create an Amazon FSx for Lustre file share and establish an IAM role that allows Fargate to communicate with FSx for Lustre.
Overall explanation
The Amazon Elastic File System offers concurrent access to a shared file system and provides high performance. You can create file system policies for controlling access and then use an IAM role that is specified in the policy for access.
CORRECT: "Create an Amazon EFS file share and establish an IAM role that allows Fargate to communicate with Amazon EFS" is the correct answer.
INCORRECT: "Create an Amazon S3 bucket for the application and establish an IAM role for Fargate to communicate with Amazon S3" is incorrect. S3 uses a REST API not a file system API so access can be shared but is not concurrent.
INCORRECT: "Create an Amazon EBS volume for the application and establish an IAM role that allows Fargate to communicate with Amazon EBS" is incorrect. EBS volumes cannot be shared amongst Fargate tasks, they are used with EC2 instances.
INCORRECT: "Create an Amazon FSx for Lustre file share and establish an IAM role that allows Fargate to communicate with FSx for Lustre" is incorrect. It is not supported to connect Fargate to FSx for Lustre.
References:
https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/
Domain
AWS Compute
Question 42Skipped
A company has several AWS accounts that are used by developers for development, testing and pre-production environments. The company has received large bills for Amazon EC2 instances that are underutilized. A Solutions Architect has been tasked with restricting the ability to launch large EC2 instances in all accounts.
How can the Solutions Architect meet this requirement with the LEAST operational overhead?
Correct answer
Create an organization in AWS Organizations that includes all accounts and create a service control policy (SCP) that denies the launch of large EC2 instances.
Create an IAM role in each account that denies the launch of large EC2 instances. Grant the developers IAM group access to the role.
Create a service-linked role for Amazon EC2 and attach a policy the denies the launch of large EC2 instances.
Create a resource-based policy that denies the launch of large EC2 instances and attach it to Amazon EC2 in each account.
Overall explanation
Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. An SCP defines a guardrail, or sets limits, on the actions that the account's administrator can delegate to the IAM users and roles in the affected accounts.
In this case the Solutions Architect can use an SCP to define a restriction that denies the launch of large EC2 instances. The SCP can be applied to all accounts, and this will ensure that even those users with permissions to launch EC2 instances will be restricted to smaller EC2 instance types.
CORRECT: "Create an organization in AWS Organizations that includes all accounts and create a service control policy (SCP) that denies the launch of large EC2 instances" is the correct answer.
INCORRECT: "Create a service-linked role for Amazon EC2 and attach a policy the denies the launch of large EC2 instances" is incorrect. You cannot create service-linked roles yourself; they are created by AWS with predefined policies.
INCORRECT: "Create a resource-based policy that denies the launch of large EC2 instances and attach it to Amazon EC2 in each account" is incorrect. You cannot attach a resource-based policy to Amazon EC2.
INCORRECT: "Create an IAM role in each account that denies the launch of large EC2 instances. Grant the developers IAM group access to the role" is incorrect. This is much less operationally efficient compared to using SCPs with AWS Organizations.
References:
https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-organizations/
Domain
AWS Compute
Question 45Skipped
A company is planning to use Amazon S3 to store documents uploaded by its customers. The images must be encrypted at rest in Amazon S3. The company does not want to spend time managing and rotating the keys, but it does want to control who can access those keys.
What should a solutions architect use to accomplish this?
Server-Side Encryption with keys stored in an S3 bucket
Correct answer
Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)
Server-Side Encryption with Customer-Provided Keys (SSE-C)
Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)
Overall explanation
SSE-KMS requires that AWS manage the data key but you manage the customer master key (CMK) in AWS KMS. You can choose a customer managed CMK or the AWS managed CMK for Amazon S3 in your account.
Customer managed CMKs are CMKs in your AWS account that you create, own, and manage. You have full control over these CMKs, including establishing and maintaining their key policies, IAM policies, and grants, enabling and disabling them, rotating their cryptographic material, adding tags, creating aliases that refer to the CMK, and scheduling the CMKs for deletion.
For this scenario, the solutions architect should use SSE-KMS with a customer managed CMK. That way KMS will manage the data key but the company can configure key policies defining who can access the keys.
CORRECT: "Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)" is the correct answer.
INCORRECT: "Server-Side Encryption with keys stored in an S3 bucket" is incorrect as you cannot store your keys in a bucket with server-side encryption
INCORRECT: "Server-Side Encryption with Customer-Provided Keys (SSE-C)" is incorrect as the company does not want to manage the keys.
INCORRECT: "Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)" is incorrect as the company needs to manage access control for the keys which is not possible when they’re managed by Amazon.
References:
https://docs.aws.amazon.com/kms/latest/developerguide/services-s3.html#sse
https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
https://digitalcloud.training/aws-kms/
Domain
AWS Compute
Question 47Skipped
A production application runs on an Amazon RDS MySQL DB instance. A solutions architect is building a new reporting tool that will access the same data. The reporting tool must be highly available and not impact the performance of the production application.
How can this be achieved?
Use Amazon Data Lifecycle Manager to automatically create and manage snapshots
Create a Single-AZ RDS Read Replica of the production RDS DB instance. Create a second Single-AZ RDS Read Replica from the replica
Create a cross-region Multi-AZ deployment and create a read replica in the second region
Correct answer
Create a Multi-AZ RDS Read Replica of the production RDS DB instance
Overall explanation
You can create a read replica as a Multi-AZ DB instance. Amazon RDS creates a standby of your replica in another Availability Zone for failover support for the replica. Creating your read replica as a Multi-AZ DB instance is independent of whether the source database is a Multi-AZ DB instance.
CORRECT: "Create a Multi-AZ RDS Read Replica of the production RDS DB instance" is the correct answer.
INCORRECT: "Create a Single-AZ RDS Read Replica of the production RDS DB instance. Create a second Single-AZ RDS Read Replica from the replica" is incorrect. Read replicas are primarily used for horizontal scaling. The best solution for high availability is to use a Multi-AZ read replica.
INCORRECT: "Create a cross-region Multi-AZ deployment and create a read replica in the second region" is incorrect as you cannot create a cross-region Multi-AZ deployment with RDS.
INCORRECT: "Use Amazon Data Lifecycle Manager to automatically create and manage snapshots" is incorrect as using snapshots is not the best solution for high availability.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_MySQL.Replication.ReadReplicas.html#USER_MySQL.Replication.ReadReplicas.MultiAZ
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Compute
Question 55Skipped
A Solutions Architect needs to capture information about the traffic that reaches an Amazon Elastic Load Balancer. The information should include the source, destination, and protocol.
What is the most secure and reliable method for gathering this data?
Create a VPC flow log for the subnets in which the ELB is running
Correct answer
Create a VPC flow log for each network interface associated with the ELB
Use Amazon CloudWatch Logs to review detailed logging information
Enable Amazon CloudTrail logging and configure packet capturing
Overall explanation
You can use VPC Flow Logs to capture detailed information about the traffic going to and from your Elastic Load Balancer. Create a flow log for each network interface for your load balancer. There is one network interface per load balancer subnet.
CORRECT: "Create a VPC flow log for each network interface associated with the ELB" is the correct answer.
INCORRECT: "Enable Amazon CloudTrail logging and configure packet capturing" is incorrect. CloudTrail performs auditing of API actions, it does not do packet capturing.
INCORRECT: "Use Amazon CloudWatch Logs to review detailed logging information" is incorrect as this service does not record this information in CloudWatch logs.
INCORRECT: "Create a VPC flow log for the subnets in which the ELB is running" is incorrect as the more secure option is to use the ELB network interfaces.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html
https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-monitoring.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
Domain
AWS Compute
Question 58Skipped
A telecommunication company has an API that allows users to manage their mobile plans and services. The API experiences significant traffic spikes during specific times such as end of the month and special offer periods. The company needs to ensure low latency response time consistently to ensure a good user experience. The solution should also minimize operational overhead.
Which solution would meet these requirements MOST efficiently?
Implement the API on an Amazon EC2 instance behind an Application Load Balancer with manual scaling.
Use Amazon API Gateway with AWS Fargate tasks to handle the API requests.
Correct answer
Use Amazon API Gateway along with AWS Lambda functions with provisioned concurrency.
Implement the API using AWS Elastic Beanstalk with auto-scaling groups.
Overall explanation
Amazon API Gateway and AWS Lambda together make a highly scalable solution for APIs. Provisioned concurrency in Lambda ensures that there is always a warm pool of functions ready to quickly respond to API requests, thereby guaranteeing low latency even during peak traffic times.
CORRECT: "Use Amazon API Gateway along with AWS Lambda functions with provisioned concurrency" is the correct answer (as explained above.)
INCORRECT: "Implement the API using AWS Elastic Beanstalk with auto-scaling groups" is incorrect.
Elastic Beanstalk is a viable option for deploying applications and auto-scaling and can help handle increased traffic, but it doesn't guarantee the low latency requirement during peak traffic times.
INCORRECT: "Use Amazon API Gateway with AWS Fargate tasks to handle the API requests" is incorrect.
API Gateway with Fargate can provide scalable compute, but this approach can result in higher operational overhead because of the need to manage the container lifecycle.
INCORRECT: "Implement the API on an Amazon EC2 instance behind an Application Load Balancer with manual scaling" is incorrect.
This solution does not scale automatically and would require manual intervention to ensure optimal performance during traffic spikes. Therefore, it doesn't satisfy the requirement of minimizing operational overhead.
References:
https://docs.aws.amazon.com/lambda/latest/dg/provisioned-concurrency.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-api-gateway/
Domain
AWS Compute
Question 60Skipped
A company runs an application on premises that stores a large quantity of semi-structured data using key-value pairs. The application code will be migrated to AWS Lambda and a highly scalable solution is required for storing the data.
Which datastore will be the best fit for these requirements?
Amazon RDS MySQL
Amazon EFS
Amazon EBS
Correct answer
Amazon DynamoDB
Overall explanation
Amazon DynamoDB is a no-SQL database that stores data using key-value pairs. It is ideal for storing large amounts of semi-structured data and is also highly scalable. This is the best solution for storing this data based on the requirements in the scenario.
CORRECT: "Amazon DynamoDB" is the correct answer.
INCORRECT: "Amazon EFS" is incorrect. The Amazon Elastic File System (EFS) is not suitable for storing key-value pairs.
INCORRECT: "Amazon RDS MySQL" is incorrect. Amazon Relational Database Service (RDS) is used for structured data as it is an SQL type of database.
INCORRECT: "Amazon EBS" is incorrect. Amazon Elastic Block Store (EBS) is a block-based storage system. You attach volumes to EC2 instances. It is not used for key-value pairs or to be used by Lambda functions.
References:
https://aws.amazon.com/dynamodb/features/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-dynamodb/
Domain
AWS Compute
Question 62Skipped
A cloud architect is assessing the resilience of a web application deployed on AWS. It was observed that the application experienced a downtime of about 3 minutes when a scheduled failover was performed on the application's Amazon RDS MySQL database as part of a scaling operation.
The organization wants to mitigate such downtime in future scaling exercises while minimizing operational overhead.
Which solution will be the MOST effective in achieving this?
Implement more RDS MySQL read replicas in the cluster to manage the load during the failover.
Establish a secondary RDS MySQL cluster within the same AWS Region. During any future failover, modify the application to connect to the secondary cluster's writer endpoint.
Implement an Amazon ElastiCache for Redis cluster to manage the load during the failover.
Correct answer
Configure an Amazon RDS Proxy for the database and modify the application to connect to the proxy endpoint.
Overall explanation
Amazon RDS Proxy is a fully managed, highly available database proxy for Amazon RDS that makes applications more scalable, more resilient to database failures, and more secure.
During a failover, RDS Proxy automatically connects to a standby database instance while preserving connections from your application and reducing failover times for RDS and Aurora multi-AZ databases. So, there is minimal downtime for the application.
CORRECT: "Configure an Amazon RDS Proxy for the database and modify the application to connect to the proxy endpoint" is the correct answer (as explained above.)
INCORRECT: "Implement more RDS MySQL read replicas in the cluster to manage the load during the failover" is incorrect.
Adding more read replicas to the cluster does not decrease the downtime during a failover. It only improves the database's ability to handle read-heavy workloads. Read replicas do not contribute to a faster failover process.
INCORRECT: "Establish a secondary RDS MySQL cluster within the same AWS Region. During any future failover, modify the application to connect to the secondary cluster's writer endpoint" is incorrect.
This approach is operationally heavy as it involves managing two separate RDS clusters and manually updating the application's database endpoint during a failover. Moreover, it does not necessarily reduce the downtime during a failover as there might be data inconsistency issues between the primary and secondary clusters, depending on the replication latency.
INCORRECT: "Implement an Amazon ElastiCache for Redis cluster to manage the load during the failover" is incorrect.
ElastiCache is an in-memory cache and not a relational database service. It is typically used to cache frequently accessed data to reduce latency and improve application performance, not for managing failovers.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Compute
Question 63Skipped
An application generates unique files that are returned to customers after they submit requests to the application. The application uses an Amazon CloudFront distribution for sending the files to customers. The company wishes to reduce data transfer costs without modifying the application.
How can this be accomplished?
Correct answer
Use Lambda@Edge to compress the files as they are sent to users.
Enable Amazon S3 Transfer Acceleration to reduce the transfer times.
Enable caching on the CloudFront distribution to store generated files at the edge.
Use AWS Global Accelerator to reduce application latency for customers.
Overall explanation
Lambda@Edge is a feature of Amazon CloudFront that lets you run code closer to users of your application, which improves performance and reduces latency. Lambda@Edge runs code in response to events generated by the Amazon CloudFront.
You simply upload your code to AWS Lambda, and it takes care of everything required to run and scale your code with high availability at an AWS location closest to your end user.
In this case Lambda@Edge can compress the files before they are sent to users which will reduce data egress costs.
CORRECT: "Use Lambda@Edge to compress the files as they are sent to users" is the correct answer.
INCORRECT: "Enable caching on the CloudFront distribution to store generated files at the edge" is incorrect. The files are unique to each customer request, so caching does not help.
INCORRECT: "Use AWS Global Accelerator to reduce application latency for customers" is incorrect. The aim is to reduce cost not latency and AWS GA uses the same network as CloudFront so does not assist with latency anyway.
INCORRECT: "Enable Amazon S3 Transfer Acceleration to reduce the transfer times" is incorrect. This does not lower costs.
References:
https://aws.amazon.com/lambda/edge/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Compute
Question 65Skipped
An application requires a MySQL database which will only be used several times a week for short periods. The database needs to provide automatic instantiation and scaling. Which database service is most suitable?
Correct answer
Amazon Aurora Serverless
Amazon Aurora
Amazon RDS MySQL
Amazon EC2 instance with MySQL database installed
Overall explanation
Amazon Aurora Serverless is an on-demand, auto-scaling configuration for Amazon Aurora. The database automatically starts up, shuts down, and scales capacity up or down based on application needs. This is an ideal database solution for infrequently-used applications.
CORRECT: "Amazon Aurora Serverless" is the correct answer.
INCORRECT: "Amazon RDS MySQL" is incorrect as this service requires an instance to be running all the time which is more costly.
INCORRECT: "Amazon EC2 instance with MySQL database installed" is incorrect as this service requires an instance to be running all the time which is more costly.
INCORRECT: "Amazon Aurora" is incorrect as this service requires an instance to be running all the time which is more costly.
References:
https://aws.amazon.com/rds/aurora/serverless/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
