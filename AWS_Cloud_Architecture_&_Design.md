Question 1Skipped
Domain
AWS Cloud Architecture & Design
Question 29Skipped
A company is deploying an Amazon ElastiCache for Redis cluster. To enhance security a password should be required to access the database. What should the solutions architect use?
AWS Directory Service
Correct answer
Redis AUTH command
VPC Security Group
AWS IAM Policy
Overall explanation
Redis authentication tokens enable Redis to require a token (password) before allowing clients to execute commands, thereby improving data security.
You can require that users enter a token on a token-protected Redis server. To do this, include the parameter --auth-token (API: AuthToken) with the correct token when you create your replication group or cluster. Also include it in all subsequent commands to the replication group or cluster.
CORRECT: "Redis AUTH command" is the correct answer.
INCORRECT: "AWS Directory Service" is incorrect. This is a managed Microsoft Active Directory service and cannot add password protection to Redis.
INCORRECT: "AWS IAM Policy" is incorrect. You cannot use an IAM policy to enforce a password on Redis.
INCORRECT: "VPC Security Group" is incorrect. A security group protects at the network layer, it does not affect application authentication.
References:
https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/auth.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-elasticache/
Domain
AWS Cloud Architecture & Design
Question 43Skipped
A company runs an internal browser-based application. The application runs on Amazon EC2 instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto Scaling group across multiple Availability Zones. The Auto Scaling group scales up to 20 instances during work hours, but scales down to 2 instances overnight. Staff are complaining that the application is very slow when the day begins, although it runs well by midmorning
How should the scaling be changed to address the staff complaints and keep costs to a minimum?
Correct answer
Implement a target tracking action triggered at a lower CPU threshold, and decrease the cooldown period
Implement a scheduled action that sets the minimum and maximum capacity to 20 shortly before the office opens
Implement a step scaling action triggered at a lower CPU threshold, and decrease the cooldown period
Implement a scheduled action that sets the desired capacity to 20 shortly before the office opens
Overall explanation
Though this sounds like a good use case for scheduled actions, both answers using scheduled actions will have 20 instances running regardless of actual demand. A better option to be more cost effective is to use a target tracking action that triggers at a lower CPU threshold.
With this solution the scaling will occur before the CPU utilization gets to a point where performance is affected. This will result in resolving the performance issues whilst minimizing costs. Using a reduced cooldown period will also more quickly terminate unneeded instances, further reducing costs.
CORRECT: "Implement a target tracking action triggered at a lower CPU threshold, and decrease the cooldown period" is the correct answer.
INCORRECT: "Implement a scheduled action that sets the desired capacity to 20 shortly before the office opens" is incorrect as this is not the most cost-effective option. Note you can choose min, max, or desired for a scheduled action.
INCORRECT: "Implement a scheduled action that sets the minimum and maximum capacity to 20 shortly before the office opens" is incorrect as this is not the most cost-effective option. Note you can choose min, max, or desired for a scheduled action.
INCORRECT: "Implement a step scaling action triggered at a lower CPU threshold, and decrease the cooldown period" is incorrect as AWS recommend you use target tracking in place of step scaling for most use cases.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Cloud Architecture & Design
Question 56Skipped
An e-commerce company operates a containerized microservices application on a fleet of Amazon EC2 instances. As part of their infrastructure improvement efforts, the company plans to migrate the application to Amazon Elastic Kubernetes Service (Amazon EKS) for enhanced scalability and management.
As part of the security protocol, the company has configured the Amazon EKS control plane with endpoint private access enabled and public access disabled. The data plane resides within private subnets. However, the company faces an issue where nodes fail to join the cluster.
What can be done to allow the nodes to join the EKS cluster?
Move nodes to public subnet and configure security group rules for the EC2 nodes.
Modify the associated IAM role to include permissions to the AmazonEKSClusterPolicy.
Establish VPC peering connection for nodes to access the control plane.
Correct answer
Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.
Overall explanation
When the EKS control plane is configured with private access, and the nodes are in a private subnet, you need to create VPC endpoints for Amazon EKS and ECR. This allows the nodes to communicate with the EKS control plane and pull container images from ECR.
CORRECT: "Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane" is the correct answer (as explained above.)
INCORRECT: "Modify the associated IAM role to include permissions to the AmazonEKSClusterPolicy" is incorrect.
IAM roles are crucial for setting up permissions, but simply modifying the associated IAM role would not solve the issue of nodes not being able to connect to the control plane.
INCORRECT: "Establish VPC peering connection for nodes to access the control plane" is incorrect.
VPC peering is not the recommended way to allow nodes in a private subnet to access the EKS control plane. This approach might also incur additional operational overhead.
INCORRECT: "Move nodes to public subnet and configure security group rules for the EC2 nodes" is incorrect.
Moving the nodes to public subnets contradicts the original requirement of having the data plane in private subnets. Additionally, this approach might introduce unnecessary security risks.
References:
https://docs.aws.amazon.com/eks/latest/userguide/private-clusters.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Cloud Architecture & Design
Question 51Skipped
There are badge readers located at every entrance of an organization’s warehouses. A message is sent over HTTPS when badges are scanned to indicate who tried to access the entrance.
A solutions architect must design a system to process these messages. A highly available solution is required. The solution must store results in a durable data store for later analysis.
Which system architecture should the solutions architect recommend?
Create an Amazon EC2 instance to serve as the HTTPS endpoint and to process messages. An Amazon S3 bucket should be configured for the EC2 instance to save the results.
Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB.
Set up an Amazon S3 gateway endpoint in your VPC. Connect the facility network to the VPC via a Site-to-Site VPN connection so that sensor data can be written directly to an S3 bucket.
Correct answer
Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function.
Overall explanation
Amazon API Gateway would be ideal for providing a secure entry point for your application, and for traffic to be sent via HTTPS. AWS Lambda would integrate seamlessly with API Gateway to process the data, as an event-driven solution like this would be perfect when designing a scalable system based on sporadic use. Finally, DynamoDB is highly scalable and is a perfect repository for data to be stored for future analysis.
CORRECT: "Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function" is the correct answer (as explained above.)
INCORRECT: "Create an Amazon EC2 instance to serve as the HTTPS endpoint and to process messages. An Amazon S3 bucket should be configured for the EC2 instance to save the results" is incorrect. As the action of a badge being read to initiate access to a warehouse should only take a few seconds, spinning up an EC2 instance to serve as a HTTPS endpoint would take minutes, and is not suitable for this use case.
INCORRECT: "Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB” is incorrect. Amazon Route 53 is a managed DNS service, and DNS is not required in this instance as the badge reader does not have a DNS name.
INCORRECT: "Set up an Amazon S3 gateway endpoint in your VPC. Connect the facility network to the VPC via a Site-to-Site VPN connection so that sensor data can be written directly to an S3 bucket" is incorrect. VPC endpoints are designed to facilitate traffic across the AWS backbone network between AWS services and are not used to create connections between external endpoints outside of the AWS network and an Amazon S3 bucket.
References:
https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
