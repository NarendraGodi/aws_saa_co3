Question 1Skipped
Domain
AWS Networking & Content Delivery
Question 2Skipped
A new application is to be published in multiple regions around the world. The Architect needs to ensure only 2 IP addresses need to be whitelisted. The solution should intelligently route traffic for lowest latency and provide fast regional failover.
How can this be achieved?
Launch EC2 instances into multiple regions behind an ALB and use Amazon CloudFront with a pair of static IP addresses
Launch EC2 instances into multiple regions behind an ALB and use a Route 53 failover routing policy
Launch EC2 instances into multiple regions behind an NLB with a static IP address
Correct answer
Launch EC2 instances into multiple regions behind an NLB and use AWS Global Accelerator
Overall explanation
AWS Global Accelerator uses the vast, congestion-free AWS global network to route TCP and UDP traffic to a healthy application endpoint in the closest AWS Region to the user.
This means it will intelligently route traffic to the closest point of presence (reducing latency). Seamless failover is ensured as AWS Global Accelerator uses anycast IP address which means the IP does not change when failing over between regions so there are no issues with client caches having incorrect entries that need to expire.


This is the only solution that provides deterministic failover.
CORRECT: "Launch EC2 instances into multiple regions behind an NLB and use AWS Global Accelerator" is the correct answer.
INCORRECT: "Launch EC2 instances into multiple regions behind an NLB with a static IP address" is incorrect. An NLB with a static IP is a workable solution as you could configure a primary and secondary address in applications. However, this solution does not intelligently route traffic for lowest latency.
INCORRECT: "Launch EC2 instances into multiple regions behind an ALB and use a Route 53 failover routing policy" is incorrect. A Route 53 failover routing policy uses a primary and standby configuration. Therefore, it sends all traffic to the primary until it fails a health check at which time it sends traffic to the secondary. This solution does not intelligently route traffic for lowest latency.
INCORRECT: "Launch EC2 instances into multiple regions behind an ALB and use Amazon CloudFront with a pair of static IP addresses" is incorrect. Amazon CloudFront cannot be configured with “a pair of static IP addresses”.
References:
https://aws.amazon.com/global-accelerator/
https://aws.amazon.com/global-accelerator/faqs/
https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-global-accelerator/
Domain
AWS Networking & Content Delivery
Question 3Skipped
A company has two accounts for perform testing and each account has a single VPC: VPC-TEST1 and VPC-TEST2. The operations team require a method of securely copying files between Amazon EC2 instances in these VPCs. The connectivity should not have any single points of failure or bandwidth constraints.
Which solution should a Solutions Architect recommend?
Attach a Direct Connect gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
Correct answer
Create a VPC peering connection between VPC-TEST1 and VPC-TEST2.
Attach a virtual private gateway to VPC-TEST1 and VPC-TEST2 and enable routing.
Create a VPC gateway endpoint for each EC2 instance and update route tables.
Overall explanation
A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network.
You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account. The VPCs can be in different regions (also known as an inter-region VPC peering connection).


CORRECT: "Create a VPC peering connection between VPC-TEST1 and VPC-TEST2" is the correct answer.
INCORRECT: "Create a VPC gateway endpoint for each EC2 instance and update route tables" is incorrect. You cannot create VPC gateway endpoints for Amazon EC2 instances. These are used with DynamoDB and S3 only.
INCORRECT: "Attach a virtual private gateway to VPC-TEST1 and VPC-TEST2 and enable routing" is incorrect. You cannot create an AWS Managed VPN connection between two VPCs.
INCORRECT: "Attach a Direct Connect gateway to VPC-TEST1 and VPC-TEST2 and enable routing" is incorrect. Direct Connect gateway is used to connect a Direct Connect connection to multiple VPCs, it is not useful in this scenario as there is no Direct Connect connection.
References:
https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Networking & Content Delivery
Question 4Skipped
A company runs an application in an on-premises data center that collects environmental data from production machinery. The data consists of JSON files stored on network attached storage (NAS) and around 5 TB of data is collected each day. The company must upload this data to Amazon S3 where it can be processed by an analytics application. The data must be transferred securely.
Which solution offers the MOST reliable and time-efficient data transfer?
AWS Database Migration Service over the Internet.
Amazon S3 Transfer Acceleration over the Internet.
Correct answer
AWS DataSync over AWS Direct Connect.
Multiple AWS Snowcone devices.
Overall explanation
The most reliable and time-efficient solution that keeps the data secure is to use AWS DataSync and synchronize the data from the NAS device directly to Amazon S3. This should take place over an AWS Direct Connect connection to ensure reliability, speed, and security.
AWS DataSync can copy data between Network File System (NFS) shares, Server Message Block (SMB) shares, self-managed object storage, AWS Snowcone, Amazon Simple Storage Service (Amazon S3) buckets, Amazon Elastic File System (Amazon EFS) file systems, and Amazon FSx for Windows File Server file systems.
CORRECT: "AWS DataSync over AWS Direct Connect" is the correct answer.
INCORRECT: "AWS Database Migration Service over the Internet" is incorrect. DMS is for migrating databases, not files.
INCORRECT: "Amazon S3 Transfer Acceleration over the Internet" is incorrect. The Internet does not offer the reliability, speed or performance that this company requires.
INCORRECT: "Multiple AWS Snowcone devices" is incorrect. This is not a time-efficient approach as it can take time to ship these devices in both directions.
References:
https://aws.amazon.com/datasync/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-migration-services/
Domain
AWS Networking & Content Delivery
Question 12Skipped
A persistent database must be migrated from an on-premises server to an Amazon EC2 instances. The database requires 64,000 IOPS and, if possible, should be stored on a single Amazon EBS volume.
Which solution should a Solutions Architect recommend?
Create an Amazon EC2 instance with four Amazon EBS General Purpose SSD (gp2) volumes attached. Max out the IOPS on each volume and use a RAID 0 stripe set.
Correct answer
Create a Nitro-based Amazon EC2 instance with an Amazon EBS Provisioned IOPS SSD (i01) volume attached. Provision 64,000 IOPS for the volume.
Use an instance from the I3 I/O optimized family and leverage instance store storage to achieve the IOPS requirement.
Create an Amazon EC2 instance with two Amazon EBS Provisioned IOPS SSD (i01) volumes attached. Provision 32,000 IOPS per volume and create a logical volume using the OS that aggregates the capacity.
Overall explanation
Amazon EC2 Nitro-based systems are not required for this solution but do offer advantages in performance that will help to maximize the usage of the EBS volume. For the data storage volume an i01 volume can support up to 64,000 IOPS so a single volume with sufficient capacity (50 IOPS per GiB) can be deliver the requirements.
The current list of EBS volume types is in the table below:


CORRECT: "Create a Nitro-based Amazon EC2 instance with an Amazon EBS Provisioned IOPS SSD (i01) volume attached. Provision 64,000 IOPS for the volume" is the correct answer.
INCORRECT: "Use an instance from the I3 I/O optimized family and leverage instance store storage to achieve the IOPS requirement" is incorrect.
INCORRECT: "Create an Amazon EC2 instance with four Amazon EBS General Purpose SSD (gp2) volumes attached. Max out the IOPS on each volume and use a RAID 0 stripe set" is incorrect. This is not a good use case for gp2 volumes. It is much better to use io1 which also meets the requirement of having a single volume with 64,000 IOPS.
INCORRECT: "Create an Amazon EC2 instance with two Amazon EBS Provisioned IOPS SSD (i01) volumes attached. Provision 32,000 IOPS per volume and create a logical volume using the OS that aggregates the capacity" is incorrect. There is no need to create two volumes and aggregate capacity through the OS, the Solutions Architect can simply create a single volume with 64,000 IOPS.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Networking & Content Delivery
Question 23Skipped
A solutions architect is creating a system that will run analytics on financial data for several hours a night, 5 days a week. The analysis is expected to run for the same duration and cannot be interrupted once it is started. The system will be required for a minimum of 1 year.
What should the solutions architect configure to ensure the EC2 instances are available when they are needed?
Savings Plans
On-Demand Instances
Regional Reserved Instances
Correct answer
On-Demand Capacity Reservations
Overall explanation
On-Demand Capacity Reservations enable you to reserve compute capacity for your Amazon EC2 instances in a specific Availability Zone for any duration. This gives you the ability to create and manage Capacity Reservations independently from the billing discounts offered by Savings Plans or Regional Reserved Instances.
By creating Capacity Reservations, you ensure that you always have access to EC2 capacity when you need it, for as long as you need it. You can create Capacity Reservations at any time, without entering a one-year or three-year term commitment, and the capacity is available immediately.
The table below shows the difference between capacity reservations and other options:


CORRECT: "On-Demand Capacity Reservations" is the correct answer.
INCORRECT: "Regional Reserved Instances" is incorrect. This type of reservation does not reserve capacity.
INCORRECT: "On-Demand Instances" is incorrect. This does not provide any kind of capacity reservation.
INCORRECT: "Savings Plans" is incorrect. This pricing option does not provide a capacity reservation.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-scheduled-instances.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Networking & Content Delivery
Question 32Skipped
A company requires that all AWS IAM user accounts have specific complexity requirements and minimum password length.
How should a Solutions Architect accomplish this?
Use an AWS Config rule to enforce the requirements when creating user accounts.
Create an IAM policy that enforces the requirements and apply it to all users.
Correct answer
Set a password policy for the entire AWS account.
Set a password policy for each IAM user in the AWS account.
Overall explanation
The easiest way to enforce this requirement is to update the password policy that applies to the entire AWS account. When you create or change a password policy, most of the password policy settings are enforced the next time your users change their passwords. However, some of the settings are enforced immediately such as the password expiration period.
CORRECT: "Set a password policy for the entire AWS account" is the correct answer.
INCORRECT: "Set a password policy for each IAM user in the AWS account" is incorrect. There’s no need to set an individual password policy for each user, it will be easier to set the policy for everyone.
INCORRECT: "Create an IAM policy that enforces the requirements and apply it to all users" is incorrect. As there is no specific targeting required it is easier to update the account password policy.
INCORRECT: "Use an AWS Config rule to enforce the requirements when creating user accounts" is incorrect. You cannot use AWS Config to enforce the password requirements at the time of creating a user account.
References:
https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords_account-policy.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Networking & Content Delivery
Question 36Skipped
A financial services company runs a trading application on a Kubernetes cluster hosted in its on-premises data center. Due to a recent surge in trading activity, the on-premises infrastructure can no longer support the increased load. The company plans to migrate the trading application to the AWS Cloud using an Amazon Elastic Kubernetes Service (Amazon EKS) cluster.
The company wants to minimize the operational overhead by avoiding management of the underlying compute infrastructure for the new AWS architecture.
Which solution will meet these requirements with the LEAST operational overhead?
Use managed node groups to provide the compute capacity for the EKS cluster. Deploy the application to the cluster using the managed nodes.
Use self-managed EC2 instances to provide the compute capacity for the EKS cluster. Deploy the application to the cluster using these instances.
Correct answer
Use AWS Fargate to provide the compute capacity for the EKS cluster. Create a Fargate profile and deploy the application using the profile.
Use Amazon EC2 Spot Instances with managed node groups to provide cost-effective compute capacity for the EKS cluster. Deploy the application using the Spot nodes.
Overall explanation
Use AWS Fargate to provide the compute capacity for the EKS cluster. Create a Fargate profile and deploy the application using the profile: This is correct because AWS Fargate eliminates the need to provision or manage EC2 instances, allowing the company to run pods without managing the underlying infrastructure. This greatly reduces operational overhead and meets the company’s requirements.
Use self-managed EC2 instances to provide the compute capacity for the EKS cluster. Deploy the application to the cluster using these instances: This is incorrect because self-managed EC2 instances require manual provisioning, patching, and scaling, which increases operational overhead compared to serverless options like Fargate.
Use managed node groups to provide the compute capacity for the EKS cluster. Deploy the application to the cluster using the managed nodes: This is incorrect because while managed node groups reduce some operational effort compared to self-managed nodes, they still require some level of instance management, such as scaling and patching, unlike Fargate.
Use Amazon EC2 Spot Instances with managed node groups to provide cost-effective compute capacity for the EKS cluster. Deploy the application using the Spot nodes: This is incorrect because Spot Instances, while cost-effective, introduce potential interruptions and require management of instance scaling, which adds operational complexity.
References:
https://docs.aws.amazon.com/eks/latest/userguide/fargate.html
https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Networking & Content Delivery
Question 38Skipped
A company runs a dynamic website that is hosted on an on-premises server in the United States. The company is expanding to Europe and is investigating how they can optimize the performance of the website for European users. The website’s backed must remain in the United States. The company requires a solution that can be implemented within a few days.
What should a Solutions Architect recommend?
Launch an Amazon EC2 instance in an AWS Region in the United States and migrate the website to it.
Use Amazon CloudFront with Lambda@Edge to direct traffic to an on-premises origin.
Correct answer
Use Amazon CloudFront with a custom origin pointing to the on-premises servers.
Migrate the website to Amazon S3. Use cross-Region replication between Regions and a latency-based Route 53 policy.
Overall explanation
A custom origin can point to an on-premises server and CloudFront is able to cache content for dynamic websites. CloudFront can provide performance optimizations for custom origins even if they are running on on-premises servers. These include persistent TCP connections to the origin, SSL enhancements such as Session tickets and OCSP stapling.
Additionally, connections are routed from the nearest Edge Location to the user across the AWS global network. If the on-premises server is connected via a Direct Connect (DX) link this can further improve performance.
CORRECT: "Use Amazon CloudFront with a custom origin pointing to the on-premises servers" is the correct answer.
INCORRECT: "Use Amazon CloudFront with Lambda@Edge to direct traffic to an on-premises origin" is incorrect. Lambda@Edge is not used to direct traffic to on-premises origins.
INCORRECT: "Launch an Amazon EC2 instance in an AWS Region in the United States and migrate the website to it" is incorrect. This would not necessarily improve performance for European users.
INCORRECT: "Migrate the website to Amazon S3. Use cross-Region replication between Regions and a latency-based Route 53 policy" is incorrect. You cannot host dynamic websites on Amazon S3 (static only).
References:
https://aws.amazon.com/cloudfront/dynamic-content/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Networking & Content Delivery
Question 43Skipped
A Solutions Architect has deployed an application on several Amazon EC2 instances across three private subnets. The application must be made accessible to internet-based clients with the least amount of administrative effort.
How can the Solutions Architect make the application available on the internet?
Create an Amazon Machine Image (AMI) of the instances in the private subnet and launch new instances from the AMI in public subnets. Create an Application Load Balancer and add the public instances to the ALB.
Create a NAT gateway in a public subnet. Add a route to the NAT gateway to the route tables of the three private subnets.
Correct answer
Create an Application Load Balancer and associate three public subnets from the same Availability Zones as the private instances. Add the private instances to the ALB.
Create an Application Load Balancer and associate three private subnets from the same Availability Zones as the private instances. Add the private instances to the ALB.
Overall explanation
To make the application instances accessible on the internet the Solutions Architect needs to place them behind an internet-facing Elastic Load Balancer. The way you add instances in private subnets to a public facing ELB is to add public subnets in the same AZs as the private subnets to the ELB. You can then add the instances and to the ELB and they will become targets for load balancing.
An example of this architecture is shown below:


CORRECT: "Create an Application Load Balancer and associate three public subnets from the same Availability Zones as the private instances. Add the private instances to the ALB" is the correct answer.
INCORRECT: "Create an Application Load Balancer and associate three private subnets from the same Availability Zones as the private instances. Add the private instances to the ALB" is incorrect. Public subnets in the same AZs as the private subnets must be added to make this configuration work.
INCORRECT: "Create an Amazon Machine Image (AMI) of the instances in the private subnet and launch new instances from the AMI in public subnets. Create an Application Load Balancer and add the public instances to the ALB" is incorrect. There is no need to use an AMI to create new instances in a public subnet. You can add instances in private subnets to a public-facing ELB.
INCORRECT: "Create a NAT gateway in a public subnet. Add a route to the NAT gateway to the route tables of the three private subnets" is incorrect. A NAT gateway is used for outbound traffic not inbound traffic and cannot make the application available to internet-based clients.
References:
https://aws.amazon.com/premiumsupport/knowledge-center/public-load-balancer-private-ec2/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
Domain
AWS Networking & Content Delivery
Question 46Skipped
A company runs containerized applications for many application workloads in an on-premise data center. The company is planning to deploy containers to AWS and the chief architect has mandated that the same configuration and administrative tools must be used across all containerized environments. The company also wishes to remain cloud agnostic to safeguard against the impact of future changes in cloud strategy.
How can a Solutions Architect design a managed solution that will align with open-source software?
Correct answer
Launch the containers on Amazon Elastic Kubernetes Service (EKS) and EKS worker nodes.
Launch the containers on Amazon Elastic Container Service (ECS) with Amazon EC2 instance worker nodes.
Launch the containers on a fleet of Amazon EC2 instances in a cluster placement group.
Launch the containers on Amazon Elastic Container Service (ECS) with AWS Fargate instances.
Overall explanation
Amazon EKS is a managed service that can be used to run Kubernetes on AWS. Kubernetes is an open-source system for automating the deployment, scaling, and management of containerized applications. Applications running on Amazon EKS are fully compatible with applications running on any standard Kubernetes environment, whether running in on-premises data centers or public clouds. This means that you can easily migrate any standard Kubernetes application to Amazon EKS without any code modification.
This solution ensures that the same open-source software is used for automating the deployment, scaling, and management of containerized applications both on-premises and in the AWS Cloud.


CORRECT: "Launch the containers on Amazon Elastic Kubernetes Service (EKS) and EKS worker nodes" is the correct answer.
INCORRECT: "Launch the containers on a fleet of Amazon EC2 instances in a cluster placement group" is incorrect
INCORRECT: "Launch the containers on Amazon Elastic Container Service (ECS) with AWS Fargate instances" is incorrect
INCORRECT: "Launch the containers on Amazon Elastic Container Service (ECS) with Amazon EC2 instance worker nodes" is incorrect
References:
https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Networking & Content Delivery
Question 65Skipped
A company provides a REST-based interface to an application that allows a partner company to send data in near-real time. The application then processes the data that is received and stores it for later analysis. The application runs on Amazon EC2 instances.
The partner company has received many 503 Service Unavailable Errors when sending data to the application and the compute capacity reaches its limits and is unable to process requests when spikes in data volume occur.
Which design should a Solutions Architect implement to improve scalability?
Use Amazon API Gateway in front of the existing application. Create a usage plan with a quota limit for the partner company.
Correct answer
Use Amazon Kinesis Data Streams to ingest the data. Process the data using AWS Lambda functions.
Use Amazon SQS to ingest the data. Configure the EC2 instances to process messages from the SQS queue.
Use Amazon SNS to ingest the data and trigger AWS Lambda functions to process the data in near-real time.
Overall explanation
Amazon Kinesis enables you to ingest, buffer, and process streaming data in real-time. Kinesis can handle any amount of streaming data and process data from hundreds of thousands of sources with very low latencies. This is an ideal solution for data ingestion.
To ensure the compute layer can scale to process increasing workloads, the EC2 instances should be replaced by AWS Lambda functions. Lambda can scale seamlessly by running multiple executions in parallel.
CORRECT: "Use Amazon Kinesis Data Streams to ingest the data. Process the data using AWS Lambda functions" is the correct answer.
INCORRECT: "Use Amazon API Gateway in front of the existing application. Create a usage plan with a quota limit for the partner company" is incorrect. A usage plan will limit the amount of data that is received and cause more errors to be received by the partner company.
INCORRECT: "Use Amazon SQS to ingest the data. Configure the EC2 instances to process messages from the SQS queue" is incorrect. Amazon Kinesis Data Streams should be used for near-real time or real-time use cases instead of Amazon SQS.
INCORRECT: "Use Amazon SNS to ingest the data and trigger AWS Lambda functions to process the data in near-real time" is incorrect. SNS is not a near-real time solution for data ingestion. SNS is used for sending notifications.
References:
https://aws.amazon.com/kinesis/
https://docs.aws.amazon.com/lambda/latest/dg/invocation-scaling.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/
https://digitalcloud.training/amazon-kinesis/
Domain
AWS Networking & Content Delivery
Question 14Skipped
A company runs its critical storage application in the AWS Cloud. The application uses Amazon S3 in two AWS Regions. The company wants the application to send remote user data to the nearest S3 bucket with no public network congestion. The company also wants the application to fail over with the least amount of management of Amazon S3.
Which solution will meet these requirements?
Send user data to the regional S3 endpoints closest to the user. Configure an S3 cross-account replication rule to keep the S3 buckets synchronized.
Correct answer
Set up Amazon S3 to use Multi-Region Access Points in an active-active configuration with a single global endpoint. Configure S3 Cross-Region Replication.
Use an active-passive configuration with S3 Multi-Region Access Points. Create a global endpoint for each of the Regions.
Implement an active-active design between the two Regions. Configure the application to use the regional S3 endpoints closest to the user.
Overall explanation
Set up Amazon S3 to use Multi-Region Access Points in an active-active configuration with a single global endpoint. Configure S3 Cross-Region Replication: This is correct because S3 Multi-Region Access Points allow the application to route user requests automatically to the nearest S3 bucket based on network conditions and proximity, minimizing latency and avoiding public network congestion. It also provides failover capabilities with minimal management effort.
Implement an active-active design between the two Regions. Configure the application to use the regional S3 endpoints closest to the user: This is incorrect because this solution requires the application to manage the routing and failover logic, increasing operational overhead.
Use an active-passive configuration with S3 Multi-Region Access Points. Create a global endpoint for each of the Regions: This is incorrect because active-passive configurations introduce delays in failover and require more manual intervention.
Send user data to the regional S3 endpoints closest to the user. Configure an S3 cross-account replication rule to keep the S3 buckets synchronized: This is incorrect because this approach does not optimize routing and requires manual failover, which increases management overhead.
References:
https://docs.aws.amazon.com/AmazonS3/latest/userguide/multi-region-access-points.html
https://aws.amazon.com/s3/features/#Global_Endpoints
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Networking & Content Delivery
Question 20Skipped
To accelerate experimentation and agility, a company allows developers to apply existing IAM policies to existing IAM roles. Nevertheless, the security operations team is concerned that the developers could attach the existing administrator policy, circumventing any other security policies.
How should a solutions architect address this issue?
Send an alert every time a developer creates a new policy using an Amazon SNS topic.
Correct answer
Set a permissions boundary on the developer IAM role that denies attaching administrator access.
Disable IAM activity across all organizational accounts using service control policies.
Assign all IAM duties to the security operations team and prevent developers from attaching policies.
Overall explanation
Setting a permissions boundary is the easiest and safest way to ensure that any IAM users cannot assume any elevated permissions. A permissions boundary is an advanced feature for using a managed policy to set the maximum permissions that an identity-based policy can grant to an IAM entity. An entity's permissions boundary allows it to perform only the actions that are allowed by both its identity-based policies and its permissions boundaries.
CORRECT: "Set a permissions boundary on the developer IAM role that denies attaching administrator access" is the correct answer (as explained above.)
INCORRECT: "Send an alert every time a developer creates a new policy using an Amazon SNS topic” is incorrect. This does not explicitly prevent any developers from attaching the policy, only sending a notification.
INCORRECT: "Disable IAM activity across all organizational accounts using service control policies" is incorrect. If all IAM activity was disabled across all accounts within the Organizational unit, each IAM user would not be able to do anything within the account.
INCORRECT: "Assign all IAM duties to the security operations team and prevent developers from attaching policies" is incorrect. The easiest way to do this is to use a permissions boundary, to make sure the permissions are being administered appropriately.
References:
https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Networking & Content Delivery
Question 23Skipped
An application has been migrated to Amazon EC2 Linux instances. The EC2 instances run several 1-hour tasks on a schedule. There is no common programming language among these tasks, as they were written by different teams. Currently, these tasks run on a single instance, which raises concerns about performance and scalability. To resolve these concerns, a solutions architect must implement a solution.
Which solution will meet these requirements with the LEAST Operational overhead?
Correct answer
Create an Amazon Machine Image (AMI) of the EC2 instance that runs the tasks. Create an Auto Scaling group with the AMI to run multiple copies of the instance.
Use AWS Batch to run the tasks as jobs. Schedule the jobs by using Amazon EventBridge (Amazon CloudWatch Events).
Copy the tasks into AWS Lambda functions. Schedule the Lambda functions by using Amazon EventBridge (Amazon CloudWatch Events).
Convert the EC2 instance to a container. Use AWS App Runner to create the container on demand to run the tasks as jobs.
Overall explanation
The best solution is to create an AMI of the EC2 instance, and then use it as a template for which to launch additional instances using an Auto Scaling Group. This removes the issues of performance, scalability, and redundancy by allowing the EC2 instances to automatically scale and be launched across multiple Availability Zones.
CORRECT: "Create an Amazon Machine Image (AMI) of the EC2 instance that runs the tasks. Create an Auto Scaling group with the AMI to run multiple copies of the instance" is the correct answer (as explained above.)
INCORRECT: "Use AWS Batch to run the tasks as jobs. Schedule the jobs by using Amazon EventBridge (Amazon CloudWatch Events)" is incorrect. AWS Batch is designed to run jobs across multiple instances, there would be less operational overhead by creating an AMI instead.
INCORRECT: "Convert the EC2 instance to a container. Use AWS App Runner to create the container on demand to run the tasks as jobs" is incorrect. Converting your EC2 instances to containers is not the easiest way to achieve this task.
INCORRECT: "Copy the tasks into AWS Lambda functions. Schedule the Lambda functions by using Amazon EventBridge (Amazon CloudWatch Events)" is incorrect. The maximum execution time for a Lambda function is 15 minutes, making it unsuitable for tasks running on a one-hour schedule.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/autoscaling-load-balancer.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
Domain
AWS Networking & Content Delivery
Question 29Skipped
A global retail company needs to provide its remote IT operations team with secure access to AWS resources across multiple AWS accounts. The company uses an on-premises Microsoft Active Directory for centralized user authentication and authorization. The AWS accounts are managed through AWS Organizations and support various internal teams and projects.
The company wants to integrate its existing Active Directory with AWS to centralize identity management, reduce operational overhead, and ensure secure, role-based access to resources across all accounts.
Which solution will meet these requirements with the LEAST operational overhead?
Deploy AWS Managed Microsoft Active Directory using AWS Directory Service. Establish a one-way trust relationship with the on-premises Active Directory. Use IAM roles mapped to Active Directory groups to provide resource access in each AWS account.
Correct answer
Use AWS Identity Center (AWS IAM Identity Center) integrated with AD Connector to link the on-premises Active Directory. Configure permission sets in IAM Identity Center to assign account-level and resource-level permissions based on Active Directory groups.
Deploy an OpenID Connect (OIDC)-compatible identity provider and integrate it with the on-premises Active Directory. Use the identity provider to generate tokens for users and configure IAM roles to allow access to AWS resources.
Create individual IAM users for each team member. Assign permissions manually to each IAM user in every AWS account. Use AWS Config to enforce compliance with access policies across accounts.
Overall explanation
Use AWS Identity Center (AWS IAM Identity Center) integrated with AD Connector to link the on-premises Active Directory. Configure permission sets in IAM Identity Center to assign account-level and resource-level permissions based on Active Directory groups: This is correct because AD Connector allows seamless integration with the on-premises Active Directory without duplicating or synchronizing identities. When combined with IAM Identity Center, permissions can be centrally managed using permission sets mapped to AD groups, minimizing operational effort and ensuring consistent access control across multiple AWS accounts.
Deploy AWS Managed Microsoft Active Directory using AWS Directory Service. Establish a one-way trust relationship with the on-premises Active Directory. Use IAM roles mapped to Active Directory groups to provide resource access in each AWS account: This is incorrect because setting up AWS Managed Microsoft AD introduces additional overhead compared to using AD Connector. It requires managing a separate AWS-hosted directory and maintaining trust relationships with the on-premises directory.
Create individual IAM users for each team member. Assign permissions manually to each IAM user in every AWS account. Use AWS Config to enforce compliance with access policies across accounts: This is incorrect because creating and managing individual IAM users for a globally distributed team across multiple AWS accounts is operationally intensive and prone to errors. Additionally, AWS Config does not reduce the complexity of manually assigning permissions.
Deploy an OpenID Connect (OIDC)-compatible identity provider and integrate it with the on-premises Active Directory. Use the identity provider to generate tokens for users and configure IAM roles to allow access to AWS resources: This is incorrect because setting up an OIDC-compatible identity provider adds unnecessary complexity for a workforce identity management use case. It is more suited for customer-facing applications than for internal employee access to AWS resources.
References:
https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_ad_connector.html
https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-iam/
Domain
AWS Networking & Content Delivery
Question 36Skipped
A pharmaceutical company is migrating its legacy inventory management system to AWS. The system runs on Microsoft Windows Server and uses shared block storage for data consistency and failover. The company requires a highly available solution that supports active-passive clustering across multiple Availability Zones. The storage solution must minimize operational overhead while ensuring low-latency access to data.
Which solution will meet these requirements with the LEAST implementation effort?
Use AWS Storage Gateway with cached volumes to provide block storage. Deploy the application on a Windows Server cluster spanning two Availability Zones, using Storage Gateway to store and access shared data.
Deploy the inventory application on Amazon EC2 instances in two Availability Zones with an active-passive setup. Use Amazon S3 with the S3 File Gateway to provide shared storage for the application data.
Deploy the inventory application on Amazon EC2 instances in two Availability Zones with an active-passive configuration. Use Amazon Elastic File System (Amazon EFS) in Standard mode to store and share application data across the two instances.
Correct answer
Deploy Amazon FSx for Windows File Server in Multi-AZ mode. Configure a Windows Server failover cluster across two Amazon EC2 instances in different Availability Zones, using FSx for Windows File Server as the shared storage.
Overall explanation
Deploy Amazon FSx for Windows File Server in Multi-AZ mode. Configure a Windows Server failover cluster across two Amazon EC2 instances in different Availability Zones, using FSx for Windows File Server as the shared storage: This is correct because FSx for Windows File Server provides fully managed, highly available shared storage designed specifically for Windows-based workloads. It integrates seamlessly with Windows failover clusters, minimizing operational complexity.
Deploy the inventory application on Amazon EC2 instances in two Availability Zones with an active-passive setup. Use Amazon S3 with the S3 File Gateway to provide shared storage for the application data: This is incorrect because S3 File Gateway provides object storage through file-based interfaces (e.g., NFS), which is not compatible with Windows failover clustering or block-level storage requirements.
Use AWS Storage Gateway with cached volumes to provide block storage. Deploy the application on a Windows Server cluster spanning two Availability Zones, using Storage Gateway to store and access shared data: This is incorrect because AWS Storage Gateway is not designed for high-availability block storage in AWS-native workloads. It is intended for hybrid environments and adds operational complexity compared to FSx for Windows File Server.
Deploy the inventory application on Amazon EC2 instances in two Availability Zones with an active-passive configuration. Use Amazon Elastic File System (Amazon EFS) in Standard mode to store and share application data across the two instances: This is incorrect because Amazon EFS is a shared file system, not a block storage solution. It is better suited for Linux-based workloads and does not support the block-level requirements of Windows failover clusters.
References:
https://docs.aws.amazon.com/fsx/latest/WindowsGuide/multiAZ.html
https://aws.amazon.com/storagegateway/
https://aws.amazon.com/efs/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Networking & Content Delivery
Question 39Skipped
A company runs an eCommerce application that uses an Amazon Aurora database. The database performs well except for short periods when monthly sales reports are run. A Solutions Architect has reviewed metrics in Amazon CloudWatch and found that the Read Ops and CPUUtilization metrics are spiking during the periods when the sales reports are run.
What is the MOST cost-effective solution to solve this performance issue?
Modify the Aurora database to use an instance class with more CPU.
Enable storage Auto Scaling for the Amazon Aurora database.
Correct answer
Create an Aurora Replica and use the replica endpoint for reporting.
Create an Amazon Redshift data warehouse and run the reporting there.
Overall explanation
The simplest and most cost-effective option is to use an Aurora Replica. The replica can serve read operations which will mean the reporting application can run reports on the replica endpoint without causing any performance impact on the production database.
CORRECT: "Create an Aurora Replica and use the replica endpoint for reporting" is the correct answer.
INCORRECT: "Enable storage Auto Scaling for the Amazon Aurora database" is incorrect. Aurora storage automatically scales based on volumes, there is no storage auto scaling feature for Aurora.
INCORRECT: "Create an Amazon Redshift data warehouse and run the reporting there" is incorrect. This would be less cost-effective and require more work in copying the data to the data warehouse.
INCORRECT: "Modify the Aurora database to use an instance class with more CPU" is incorrect. This may not resolve the storage performance issues and could be more expensive depending on instances sizes.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.StorageReliability.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Networking & Content Delivery
Question 47Skipped
A retail company runs its order processing system on AWS. The system uses an Amazon RDS for MySQL Multi-AZ database cluster as its backend. The company must retain database backups for 30 days to meet compliance requirements. The company uses both automated RDS backups and manual backups for specific points in time. The company wants to enforce the 30-day retention policy for all backups while ensuring that both automated and manual backups created within the last 30 days are preserved. The solution must be cost-effective and require minimal operational effort.
Which solution will meet these requirements MOST cost-effectively?
Use AWS Backup to enforce a 30-day retention policy for automated backups. Configure an AWS Lambda function to identify and delete manual backups older than 30 days.
Correct answer
Configure the RDS backup retention policy to 30 days for automated backups. Use a script to identify and delete manual backups that are older than 30 days.
Retain the current configuration with both automated and manual backups. Use Amazon CloudWatch Events with AWS Lambda to automatically delete both automated and manual backups that are older than 30 days.
Disable RDS automated backups. Use AWS Backup to create and retain daily backups for 30 days. Use AWS Backup lifecycle policies to delete backups older than 30 days.
Overall explanation
Configure the RDS backup retention policy to 30 days for automated backups. Use a script to identify and delete manual backups that are older than 30 days: This is correct because RDS backup retention policies can only be applied to automated backups. Manual backups must be managed separately. Using a script to identify and delete older manual backups ensures compliance without additional costs. Use AWS Backup to enforce a 30-day retention policy for automated backups. Configure an AWS Lambda function to identify and delete manual backups older than 30 days: This is incorrect because AWS Backup is not required for RDS automated backups, which natively support retention policies. Using Lambda for manual backup deletion adds unnecessary operational overhead. Disable RDS automated backups. Use AWS Backup to create and retain daily backups for 30 days. Use AWS Backup lifecycle policies to delete backups older than 30 days: This is incorrect because disabling automated backups introduces operational risks and does not provide a cost-effective solution compared to the built-in RDS backup retention feature. Retain the current configuration with both automated and manual backups. Use Amazon CloudWatch Events with AWS Lambda to automatically delete both automated and manual backups that are older than 30 days: This is incorrect because CloudWatch Events and Lambda add complexity and operational overhead compared to simply using RDS retention policies and a script for manual backups.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithAutomatedBackups.html
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_WorkingWithDBInstanceAutomatedBackups.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Networking & Content Delivery
Question 49Skipped
A company requires a solution for replicating data to AWS for disaster recovery. Currently, the company uses scripts to copy data from various sources to a Microsoft Windows file server in the on-premises data center. The company also requires that a small amount of recent files are accessible to administrators with low latency.
What should a Solutions Architect recommend to meet these requirements?
Update the script to copy data to an Amazon EFS volume instead of the on-premises file server.
Update the script to copy data to an Amazon EBS volume instead of the on-premises file server.
Correct answer
Update the script to copy data to an AWS Storage Gateway for File Gateway virtual appliance instead of the on-premises file server.
Update the script to copy data to an Amazon S3 Glacier archive instead of the on-premises file server.
Overall explanation
The best solution here is to use an AWS Storage Gateway File Gateway virtual appliance in the on-premises data center. This can be accessed the same protocols as the existing Microsoft Windows File Server (SMB/CIFS). Therefore, the script simply needs to be updated to point to the gateway.
The file gateway will then store data on Amazon S3 and has a local cache for data that can be accessed at low latency. The file gateway provides an excellent method of enabling file protocol access to low cost S3 object storage.


CORRECT: "Update the script to copy data to an AWS Storage Gateway for File Gateway virtual appliance instead of the on-premises file server" is the correct answer.
INCORRECT: "Update the script to copy data to an Amazon EBS volume instead of the on-premises file server" is incorrect. This would also need an attached EC2 instance running Windows to be able to mount using the same protocols and would not offer any local low-latency access.
INCORRECT: "Update the script to copy data to an Amazon EFS volume instead of the on-premises file server" is incorrect. This solution would not provide a local cache.
INCORRECT: "Update the script to copy data to an Amazon S3 Glacier archive instead of the on-premises file server" is incorrect. This would not provide any immediate access with low-latency.
References:
https://aws.amazon.com/storagegateway/file/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/
Domain
AWS Networking & Content Delivery
Question 58Skipped
A social media analytics company runs a data processing application on a single Amazon EC2 On-Demand Instance. The application is stateless and processes user behavior data in near real-time. Recently, the application has started showing performance degradation during peak times, including 5xx errors due to high traffic volumes. The company wants to implement a solution to make the application scale automatically to handle traffic spikes in a cost-effective way.
Which solution will meet these requirements MOST cost-effectively?
Increase the size of the existing EC2 instance to a larger instance type using Amazon EC2 Auto Scaling scheduled actions to handle peak hours. Use Amazon Route 53 to distribute traffic between the upgraded instance and a secondary instance in another Region.
Correct answer
Create an Auto Scaling group using an Amazon Machine Image (AMI) of the application. Use a launch template that configures the Auto Scaling group to scale out and in based on CPU utilization. Attach an Application Load Balancer to the Auto Scaling group to distribute traffic.
Create an Amazon Machine Image (AMI) of the application. Use the AMI to deploy two EC2 On-Demand Instances. Attach an Application Load Balancer to distribute traffic between the two instances.
Use AWS Lambda and Amazon SQS to redesign the application into a serverless architecture. Deploy Lambda functions to process incoming requests and store results in Amazon DynamoDB.
Overall explanation
Create an Auto Scaling group using an Amazon Machine Image (AMI) of the application. Use a launch template that configures the Auto Scaling group to scale out and in based on CPU utilization. Attach an Application Load Balancer to the Auto Scaling group to distribute traffic: This is correct because Auto Scaling ensures the application can scale automatically to meet demand, while the Application Load Balancer distributes traffic across instances, improving fault tolerance. This setup is both cost-effective and aligned with the application's stateless architecture.
Create an Amazon Machine Image (AMI) of the application. Use the AMI to deploy two EC2 On-Demand Instances. Attach an Application Load Balancer to distribute traffic between the two instances: This is incorrect because simply adding a second EC2 instance does not allow for dynamic scaling. This approach could lead to underutilization during off-peak times and increased costs.
Use AWS Lambda and Amazon SQS to redesign the application into a serverless architecture. Deploy Lambda functions to process incoming requests and store results in Amazon DynamoDB: This is incorrect because redesigning the application as a serverless architecture adds significant development effort and may not be the most cost-effective solution compared to using Auto Scaling with existing EC2-based architecture.
Increase the size of the existing EC2 instance to a larger instance type using Amazon EC2 Auto Scaling scheduled actions to handle peak hours. Use Amazon Route 53 to distribute traffic between the upgraded instance and a secondary instance in another Region: This is incorrect because increasing the instance size does not enable dynamic scaling. Route 53 does not natively provide traffic distribution between instances based on load metrics, and this solution introduces unnecessary complexity with no clear scalability benefits.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Networking & Content Delivery
Question 60Skipped
A company operates a globally accessed video-sharing platform where users can upload, view, and download videos from their mobile devices. The platform's static website is hosted in an Amazon S3 bucket.
Due to the platform’s rapid growth, users are experiencing increased latency during video uploads and downloads. The company needs to improve the performance of the platform while minimizing the complexity of the implementation.
Which solution will meet these requirements with the LEAST implementation effort?
Set up AWS Global Accelerator for the S3 bucket to optimize network routing. Configure the platform to use the Global Accelerator endpoint instead of the S3 bucket.
Deploy Amazon EC2 instances in multiple AWS Regions and migrate the platform to these instances. Use an Application Load Balancer to distribute traffic across the instances and configure AWS Global Accelerator for improved global performance.
Correct answer
Configure an Amazon CloudFront distribution for the S3 bucket to accelerate download performance. Enable S3 Transfer Acceleration to enhance upload performance.
Configure an Amazon CloudFront distribution with the S3 bucket as the origin to accelerate downloads. Use CloudFront for uploads as well. Create additional S3 buckets in multiple Regions and set up replication rules to sync user content between buckets. Redirect users to the closest bucket for downloads.
Overall explanation
Configure an Amazon CloudFront distribution for the S3 bucket to accelerate download performance. Enable S3 Transfer Acceleration to enhance upload performance: This is correct because Amazon CloudFront is a global content delivery network (CDN) that improves download performance by caching content closer to users. S3 Transfer Acceleration reduces upload latency by utilizing optimized AWS edge locations to accelerate the data transfer from the user to the S3 bucket. Together, these services provide a cost-effective and low-effort solution to improve the platform's performance.
Deploy Amazon EC2 instances in multiple AWS Regions and migrate the platform to these instances. Use an Application Load Balancer to distribute traffic across the instances and configure AWS Global Accelerator for improved global performance: This is incorrect because migrating the platform to EC2 instances and configuring Global Accelerator is significantly more complex and requires ongoing maintenance. This solution involves more implementation effort compared to using managed AWS services like CloudFront and S3 Transfer Acceleration.
Configure an Amazon CloudFront distribution with the S3 bucket as the origin to accelerate downloads. Use CloudFront for uploads as well. Create additional S3 buckets in multiple Regions and set up replication rules to sync user content between buckets. Redirect users to the closest bucket for downloads: This is incorrect because adding multiple S3 buckets and setting up replication rules increases the complexity of the solution. While CloudFront can accelerate uploads and downloads, replicating buckets adds unnecessary operational overhead when S3 Transfer Acceleration can address upload latency more efficiently.
Set up AWS Global Accelerator for the S3 bucket to optimize network routing. Configure the platform to use the Global Accelerator endpoint instead of the S3 bucket: This is incorrect because AWS Global Accelerator does not directly support S3 buckets as an endpoint. Configuring Global Accelerator would require additional infrastructure, such as custom endpoints, increasing the effort and complexity without directly solving the latency issues.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Networking & Content Delivery
Question 61Skipped
A fitness application company is launching a platform to track user activity, workout logs, and personalized settings. The database must support structured data, allow for transactions between related data, and dynamically scale to handle unpredictable traffic spikes during peak hours. The solution must also support automated backups and minimize operational management.
Which solution will meet these requirements MOST cost-effectively?
Correct answer
Use Amazon Aurora Serverless v2 to store the data. Enable serverless auto-scaling and configure automated backups to Amazon S3 with a 7-day retention period.
Deploy an Amazon RDS MySQL instance in a multi-AZ configuration. Use provisioned IOPS storage and configure automated backups to Amazon S3 Glacier Flexible Retrieval for long-term retention.
Use Amazon DynamoDB with on-demand capacity mode to handle fluctuating traffic. Enable DynamoDB Point-in-Time Recovery (PITR) for automated backups.
Deploy an open-source database on Amazon EC2 Spot Instances in an Auto Scaling group. Configure daily backups to Amazon S3 Intelligent-Tiering for cost optimization.
Overall explanation
Use Amazon Aurora Serverless v2 to store the data. Enable serverless auto-scaling and configure automated backups to Amazon S3 with a 7-day retention period: This is correct because Aurora Serverless supports relational data, transactions, and complex queries while scaling seamlessly to meet workload demands. It integrates natively with Amazon S3 for automated backups, eliminating operational overhead while remaining cost-effective.
Use Amazon DynamoDB with on-demand capacity mode to handle fluctuating traffic. Enable DynamoDB Point-in-Time Recovery (PITR) for automated backups: This is incorrect because, while DynamoDB is cost-effective and highly scalable, it lacks native support for relational data and transactions, which are required in this scenario. For structured data with relational dependencies, Aurora Serverless is the better fit.
Deploy an open-source database on Amazon EC2 Spot Instances in an Auto Scaling group. Configure daily backups to Amazon S3 Intelligent-Tiering for cost optimization: This is incorrect because managing an open-source database on EC2 Spot Instances introduces operational complexity and risks interruptions. Additionally, Spot Instances are less suitable for workloads requiring high availability.
Deploy an Amazon RDS MySQL instance in a multi-AZ configuration. Use provisioned IOPS storage and configure automated backups to Amazon S3 Glacier Flexible Retrieval for long-term retention: This is incorrect because provisioned IOPS increases costs unnecessarily, and Glacier Flexible Retrieval is unsuitable for backups requiring quick access.
References:
https://aws.amazon.com/rds/aurora/serverless/
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/backuprestore_PITR.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Networking & Content Delivery
Question 65Skipped
A solutions architect is finalizing the architecture for a distributed database that will run across multiple Amazon EC2 instances. Data will be replicated across all instances so the loss of an instance will not cause loss of data. The database requires block storage with low latency and throughput that supports up to several million transactions per second per server.
Which storage solution should the solutions architect use?
Correct answer
Amazon EC2 instance store
Amazon EFS
Amazon EBS
Amazon S3
Overall explanation
An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer. Instance store is ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers.


Some instance types use NVMe or SATA-based solid state drives (SSD) to deliver high random I/O performance. This is a good option when you need storage with very low latency, but you don't need the data to persist when the instance terminates or you can take advantage of fault-tolerant architectures.
In this scenario the data is replicated and fault tolerant so the best option to provide the level of performance required is to use instance store volumes.
CORRECT: "Amazon EC2 instance store" is the correct answer.
INCORRECT: "Amazon EBS " is incorrect. The Elastic Block Store (EBS) is a block storage device but as the data is distributed and fault tolerant a better option for performance would be to use instance stores.
INCORRECT: "Amazon EFS " is incorrect as EFS is not a block device, it is a filesystem that is accessed using the NFS protocol.
INCORRECT: "Amazon S3" is incorrect as S3 is an object-based storage system, not a block-based storage system.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ebs/
Domain
AWS Networking & Content Delivery
Question 13Skipped
An application runs on a fleet of Amazon EC2 instances in an Amazon EC2 Auto Scaling group behind an Elastic Load Balancer. The operations team has determined that the application performs best when the CPU utilization of the EC2 instances is at or near 60%.
Which scaling configuration should a Solutions Architect use to optimize the applications performance?
Correct answer
Use a target tracking policy to dynamically scale the Auto Scaling group.
Use a step scaling policy to dynamically scale the Auto Scaling group.
Use a simple scaling policy to dynamically scale the Auto Scaling group.
Use a scheduled scaling policy to dynamically the Auto Scaling group.
Overall explanation
With target tracking scaling policies, you select a scaling metric and set a target value. Amazon EC2 Auto Scaling creates and manages the CloudWatch alarms that trigger the scaling policy and calculates the scaling adjustment based on the metric and the target value.
The scaling policy adds or removes capacity as required to keep the metric at, or close to, the specified target value. In addition to keeping the metric close to the target value, a target tracking scaling policy also adjusts to changes in the metric due to a changing load pattern.
The following diagram shows a target tracking policy set to keep the CPU utilization of the EC2 instances at or close to 60%.


CORRECT: "Use a target tracking policy to dynamically scale the Auto Scaling group" is the correct answer.
INCORRECT: "Use a simple scaling policy to dynamically scale the Auto Scaling group" is incorrect. Simple scaling is not used for maintaining a target utilization. It is used for making simple adjustments up or down based on a threshold value.
INCORRECT: "Use a step scaling policy to dynamically scale the Auto Scaling group" is incorrect. Step scaling is not used for maintaining a target utilization. It is used for making step adjustments that vary based on the size of the alarm breach.
INCORRECT: "Use a scheduled scaling policy to dynamically the Auto Scaling group" is incorrect. Scheduled scaling is not used for maintaining a target utilization. It is used for scheduling changes at specific dates and times.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Networking & Content Delivery
Question 15Skipped
A company runs a containerized application on an Amazon Elastic Kubernetes Service (EKS) using a microservices architecture. The company requires a solution to collect, aggregate, and summarize metrics and logs. The solution should provide a centralized dashboard for viewing information including CPU and memory utilization for EKS namespaces, services, and pods.
Which solution meets these requirements?
Run the Amazon CloudWatch agent in the existing EKS cluster. View the metrics and logs in the CloudWatch console.
Migrate the containers to Amazon ECS and enable Amazon CloudWatch Container Insights. View the metrics and logs in the CloudWatch console.
Configure AWS X-Ray to enable tracing for the EKS microservices. Query the trace data using Amazon Elasticsearch.
Correct answer
Configure Amazon CloudWatch Container Insights in the existing EKS cluster. View the metrics and logs in the CloudWatch console.
Overall explanation
Use CloudWatch Container Insights to collect, aggregate, and summarize metrics and logs from your containerized applications and microservices. Container Insights is available for Amazon Elastic Container Service (Amazon ECS), Amazon Elastic Kubernetes Service (Amazon EKS), and Kubernetes platforms on Amazon EC2.
With Container Insights for EKS you can see the top contributors by memory or CPU, or the most recently active resources. This is available when you select any of the following dashboards in the drop-down box near the top of the page:
  •  ECS Services
  •  ECS Tasks
  •  EKS Namespaces
  •  EKS Services
  •  EKS Pods
CORRECT: "Configure Amazon CloudWatch Container Insights in the existing EKS cluster. View the metrics and logs in the CloudWatch console" is the correct answer.
INCORRECT: "Run the Amazon CloudWatch agent in the existing EKS cluster. View the metrics and logs in the CloudWatch console" is incorrect. Container Insights is the best way to view the required data.
INCORRECT: "Migrate the containers to Amazon ECS and enable Amazon CloudWatch Container Insights. View the metrics and logs in the CloudWatch console" is incorrect. There is no need to migrate containers to ECS as EKS is supported for Container Insights.
INCORRECT: "Configure AWS X-Ray to enable tracing for the EKS microservices. Query the trace data using Amazon Elasticsearch" is incorrect. X-Ray will not deliver the required statistics to a centralized dashboard.
References:
https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/ContainerInsights.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Networking & Content Delivery
Question 17Skipped
A research organization runs its photo analysis application on AWS. The application processes images uploaded by field scientists and stores them temporarily on an Amazon EC2 instance's locally attached Amazon Elastic Block Store (Amazon EBS) volume. Every evening, the processed images are uploaded to an Amazon S3 bucket for long-term storage.
The solutions architect has discovered that the images are being uploaded to S3 through the public internet. The organization wants to ensure that the upload traffic to Amazon S3 remains private and does not use the public internet.
Which solution will meet these requirements?
Configure a VPC peering connection between the VPC containing the EC2 instance and Amazon S3. Update the route table to use the peering connection for traffic to S3.
Deploy a NAT gateway in the VPC. Configure the EC2 instance's security group to allow outbound traffic to the NAT gateway, which will route traffic to the S3 bucket.
Use an Amazon S3 access point for the EC2 instance. Configure the photo analysis application to upload files to the bucket through the access point.
Correct answer
Create a gateway VPC endpoint for the S3 bucket. Update the VPC's route table to route all S3 traffic through the gateway endpoint.
Overall explanation
Create a gateway VPC endpoint for the S3 bucket. Update the VPC's route table to route all S3 traffic through the gateway endpoint: This is correct because a gateway VPC endpoint establishes a private connection to Amazon S3 without using the public internet. Updating the route table ensures all traffic to S3 is routed through this private endpoint. This solution is secure and cost-effective.
Use an Amazon S3 access point for the EC2 instance. Configure the photo analysis application to upload files to the bucket through the access point: This is incorrect because while S3 access points simplify access management for specific applications, they do not provide private connectivity. A gateway VPC endpoint is required to route traffic privately.
Configure a VPC peering connection between the VPC containing the EC2 instance and Amazon S3. Update the route table to use the peering connection for traffic to S3: This is incorrect because VPC peering does not provide connectivity to AWS services like Amazon S3. Gateway VPC endpoints are the correct mechanism for private S3 connectivity.
Deploy a NAT gateway in the VPC. Configure the EC2 instance's security group to allow outbound traffic to the NAT gateway, which will route traffic to the S3 bucket: This is incorrect because a NAT gateway routes traffic to the internet, and S3 traffic would still use public endpoints. This does not meet the requirement of avoiding the public internet.
References:
https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html
https://docs.aws.amazon.com/AmazonS3/latest/userguide/privatelink-interface-endpoints.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Networking & Content Delivery
Question 18Skipped
A media company is building a video content distribution platform on AWS. The platform uses an REST API hosted on Amazon API Gateway to serve metadata about the videos, such as titles and descriptions. The metadata is confidential and must be accessible only from a specific set of trusted IP addresses belonging to the company’s office network.
Which solution will meet these requirements?
Set up API Gateway with a private integration and restrict access to the trusted IP addresses using a VPC endpoint policy.
Deploy the API Gateway in a private subnet and configure a network ACL to permit traffic only from the trusted IP addresses.
Correct answer
Configure an API Gateway resource policy that denies access to any IP address that is not explicitly allowed.
Modify the API Gateway security group to allow inbound requests only from the trusted IP addresses.
Overall explanation
Configure an API Gateway resource policy that denies access to any IP address that is not explicitly allowed: This is correct because resource policies in API Gateway allow you to restrict access to APIs by specifying conditions, such as IP addresses. By creating a resource policy with a condition that permits traffic only from the trusted IP range, you can ensure that the API is accessible only from the company’s internal network.
Deploy the API Gateway in a private subnet and configure a network ACL to permit traffic only from the trusted IP addresses: This is incorrect because API Gateway cannot be directly deployed within a private subnet. Instead, it is a managed service that operates outside of VPCs. To use a private network, you would need a VPC endpoint, but this does not fully meet the requirements without additional configuration.
Set up API Gateway with a private integration and restrict access to the trusted IP addresses using a VPC endpoint policy: This is incorrect because private integrations in API Gateway are used to route traffic to resources within a VPC, such as an application running on Amazon EC2. While you can use a VPC endpoint policy for restricting access, this setup is more complex than using a resource policy and does not directly fulfill the requirement of limiting IP addresses for the API.
Modify the API Gateway security group to allow inbound requests only from the trusted IP addresses: This is incorrect because API Gateway is not associated with security groups. Security groups are used for resources like EC2 instances or load balancers, not for API Gateway endpoints.
References:
https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-resource-policies.html
https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-privatelink.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-api-gateway/
Domain
AWS Networking & Content Delivery
Question 19Skipped
A company runs its critical payment processing application on an Amazon Aurora MySQL cluster in the ap-southeast-1 Region. As part of its disaster recovery (DR) strategy, the company has selected the ap-northeast-1 Region for failover capabilities.
The company requires a recovery point objective (RPO) of less than 5 minutes and a recovery time objective (RTO) of no more than 15 minutes. The company also wants to minimize operational overhead and ensure failover happens with minimal downtime and configuration.
Which solution will meet these requirements with the MOST operational efficiency?
Create a new Aurora MySQL cluster in ap-northeast-1 and use AWS Database Migration Service (AWS DMS) to replicate data between clusters.
Use Amazon S3 Cross-Region Replication to replicate database backups from ap-southeast-1 to ap-northeast-1. Restore the backups to a new Aurora cluster during failover.
Correct answer
Convert the Aurora cluster to an Aurora global database. Configure cross-Region replication and managed failover.
Create an Aurora read replica in ap-northeast-1 to replicate data from the primary Aurora cluster. Promote the read replica manually in the event of a failover.
Overall explanation
Convert the Aurora cluster to an Aurora global database. Configure cross-Region replication and managed failover: This is correct because Aurora global databases are purpose-built for disaster recovery and can achieve an RPO of under 5 seconds with automated failover, meeting the company’s stringent RPO and RTO requirements.
Create an Aurora read replica in ap-northeast-1 to replicate data from the primary Aurora cluster. Promote the read replica manually in the event of a failover: While this approach provides DR capabilities, it involves manual intervention during failover, which increases downtime and operational complexity, making it less efficient for meeting the RTO goal.
Create a new Aurora MySQL cluster in ap-northeast-1 and use AWS Database Migration Service (AWS DMS) to replicate data between clusters: AWS DMS is not ideal for low-latency replication of high-throughput transactional databases, and it does not natively provide automated failover capabilities.
Use Amazon S3 Cross-Region Replication to replicate database backups from ap-southeast-1 to ap-northeast-1. Restore the backups to a new Aurora cluster during failover: Restoring backups to create a new Aurora cluster involves significant downtime and is not suitable for the given RPO and RTO requirements.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
https://aws.amazon.com/rds/aurora/global-database/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Networking & Content Delivery
Question 24Skipped
A company requires a high-performance file system that can be mounted on Amazon EC2 Windows instances and Amazon EC2 Linux instances. Applications running on the EC2 instances perform separate processing of the same files and the solution must provide a file system that can be mounted by all instances simultaneously.
Which solution meets these requirements?
Use Amazon FSx for Windows File Server for the Windows instances. Use Amazon FSx for Lustre for the Linux instances. Link both Amazon FSx file systems to the same Amazon S3 bucket.
Correct answer
Use Amazon FSx for Windows File Server for the Windows instances and the Linux instances.
Use Amazon Elastic File System (Amazon EFS) with General Purpose performance mode for the Windows instances and the Linux instances.
Use Amazon FSx for Windows File Server for the Windows instances. Use Amazon Elastic File System (Amazon EFS) with Max I/O performance mode for the Linux instances.
Overall explanation
Amazon FSx for Windows File Server provides a fully managed native Microsoft Windows file system so you can easily move your Windows-based applications that require shared file storage to AWS. You can easily connect Linux instances to the file system by installing the cifs-utils package. The Linux instances can then mount an SMB/CIFS file system.


CORRECT: "Use Amazon FSx for Windows File Server for the Windows instances and the Linux instances" is the correct answer.
INCORRECT: "Use Amazon FSx for Windows File Server for the Windows instances. Use Amazon Elastic File System (Amazon EFS) with Max I/O performance mode for the Linux instances" is incorrect. This solution results in two separate file systems and a shared file system is required.
INCORRECT: "Use Amazon Elastic File System (Amazon EFS) with General Purpose performance mode for the Windows instances and the Linux instances" is incorrect. You cannot use Amazon EFS for Windows instances as this is not supported.
INCORRECT: "Use Amazon FSx for Windows File Server for the Windows instances. Use Amazon FSx for Lustre for the Linux instances. Link both Amazon FSx file systems to the same Amazon S3 bucket" is incorrect. Amazon FSx for Windows File Server does not use Amazon S3 buckets, so this is another solution that results in separate file systems.
References:
https://docs.aws.amazon.com/fsx/latest/WindowsGuide/using-file-shares.html#map-shares-linux
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Networking & Content Delivery
Question 29Skipped
A financial services company manages its web application on Amazon EC2 instances. The EC2 instances are registered in an IP address-type target group behind an Application Load Balancer (ALB). The company uses AWS Systems Manager for patching and routine maintenance of the instances.
To meet security compliance requirements, the company must ensure that EC2 instances are temporarily removed from service during patching to prevent serving traffic. During a recent patching attempt, the company experienced application errors and traffic disruptions.
Which combination of solutions will resolve these issues? (Select TWO.)
Correct selection
Use the Systems Manager Maintenance Windows feature to schedule patching and automatically deregister instances from the ALB during updates.
Configure ALB health checks to automatically remove unhealthy instances during patching. Use Systems Manager Run Command to apply the patches manually.
Use Systems Manager State Manager to schedule patching jobs and ensure instances are deregistered and re-registered with the ALB after patching is complete.
Change the target type of the target group from IP address type to instance type and re-register the instances.
Correct selection
Implement the AWSEC2-PatchLoadBalancerInstance Systems Manager Automation document to manage the patching process for EC2 instances behind the ALB.
Overall explanation
Use the Systems Manager Maintenance Windows feature to schedule patching and automatically deregister instances from the ALB during updates: This is correct because Maintenance Windows coordinate the patching process, including removing instances from the ALB during updates, ensuring compliance and preventing traffic disruptions.
Implement the AWSEC2-PatchLoadBalancerInstance Systems Manager Automation document to manage the patching process for EC2 instances behind the ALB: This is correct because this Automation document automates the removal of instances from the ALB, applies patches, and re-registers the instances after patching. This eliminates manual errors and ensures seamless updates without disrupting application traffic.
Change the target type of the target group from IP address type to instance type and re-register the instances: This is incorrect because changing the target type does not address the root cause of the errors. The patching process itself requires proper management of instance removal and re-registration.
Configure ALB health checks to automatically remove unhealthy instances during patching. Use Systems Manager Run Command to apply the patches manually: This is incorrect because relying on ALB health checks for patching introduces unnecessary delays. Manually applying patches with Run Command is operationally inefficient compared to using Automation documents.
Use Systems Manager State Manager to schedule patching jobs and ensure instances are deregistered and re-registered with the ALB after patching is complete: This is incorrect because State Manager is not designed to dynamically handle instance deregistration and re-registration with load balancers. Automation documents like AWSEC2-PatchLoadBalancerInstance are more appropriate.
References:
https://docs.aws.amazon.com/systems-manager-automation-runbooks/latest/userguide/automation-awsec2-patch-load-balancer-instance.html
https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-maintenance.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-systems-manager/
Domain
AWS Networking & Content Delivery
Question 36Skipped
A gaming company recently launched a multiplayer gaming platform for its users. The platform runs on multiple Amazon EC2 instances across two Availability Zones. Players use TCP to communicate with the platform in real time. The platform must be highly available and automatically scale as the number of players increases, while remaining cost-effective.
Which combination of steps will meet these requirements MOST cost-effectively? (Select TWO.)
Correct selection
Configure an Auto Scaling group to add or remove EC2 instances based on player traffic.
Correct selection
Add a Network Load Balancer in front of the EC2 instances to manage TCP traffic.
Use an Application Load Balancer to distribute TCP traffic to the EC2 instances.
Deploy an Amazon ECS cluster to replace the EC2 instances and handle player traffic.
Configure Amazon Route 53 to implement latency-based routing across multiple EC2 instances.
Overall explanation
Configure an Auto Scaling group to add or remove EC2 instances based on player traffic: This is correct because an Auto Scaling group automatically adjusts the number of EC2 instances in response to traffic changes. This ensures cost efficiency by scaling out during high demand and scaling in during low demand.
Add a Network Load Balancer in front of the EC2 instances to manage TCP traffic: This is correct because a Network Load Balancer is optimized for handling TCP traffic with low latency. It provides the required scalability and high availability across multiple Availability Zones.
Use an Application Load Balancer to distribute TCP traffic to the EC2 instances: This is incorrect because Application Load Balancers are optimized for HTTP/HTTPS traffic, not TCP. A Network Load Balancer is more cost-effective and appropriate for this use case.
Deploy an Amazon ECS cluster to replace the EC2 instances and handle player traffic: This is incorrect because switching to Amazon ECS introduces operational complexity and higher costs. The question specifies using EC2 instances, so Auto Scaling and a Network Load Balancer are more cost-effective and aligned with the scenario.
Configure Amazon Route 53 to implement latency-based routing across multiple EC2 instances: This is incorrect because Route 53 latency-based routing is not designed to provide automatic scaling or load balancing. Instead, it is used for directing traffic across endpoints in different Regions or locations.
References:
https://aws.amazon.com/elasticloadbalancing/network-load-balancer/
https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
Domain
AWS Networking & Content Delivery
Question 42Skipped
A company is deploying a solution for sharing media files around the world using Amazon CloudFront with an Amazon S3 origin configured as a static website. The company requires that all traffic for the website must be inspected by AWS WAF.
Which solution meets these requirements?
Correct answer
Deploy CloudFront with an S3 origin and configure an origin access identity (OAI) to restrict access to the S3 bucket. Enable AWS WAF on the CloudFront distribution.
Create an S3 bucket policy with a condition that only allows requests that originate from AWS WAF.
Use an Amazon Route 53 Alias record to forward traffic for the website to AWS WAF. Configure AWS WAF to inspect traffic and attach the CloudFront distribution.
Create a Network ACL that limits access to the S3 bucket to the CloudFront IP addresses. Attach a WebACL to the CloudFront distribution.
Overall explanation
The AWS Web Application Firewall (WAF) can be attached to an Amazon CloudFront distribution to enable protection from web exploits. In this case the distribution uses an S3 origin, and the question is stating that all traffic must be inspected by AWS WAF. This means we need to ensure that requests cannot circumvent AWS WAF and hit the S3 bucket directly.
This can be achieved by configuring an origin access identity (OAI) which is a special type of CloudFront user that is created within the distribution and configured in an S3 bucket policy. The policy will only allow requests that come from the OAI which means all requests must come via the distribution and cannot hit S3 directly.


CORRECT: "Deploy CloudFront with an S3 origin and configure an origin access identity (OAI) to restrict access to the S3 bucket. Enable AWS WAF on the CloudFront distribution" is the correct answer.
INCORRECT: "Create a Network ACL that limits access to the S3 bucket to the CloudFront IP addresses. Attach a WebACL to the CloudFront distribution" is incorrect. Network ACLs restrict traffic in/out of subnets but S3 is a public service.
INCORRECT: "Use an Amazon Route 53 Alias record to forward traffic for the website to AWS WAF. Configure AWS WAF to inspect traffic and attach the CloudFront distribution" is incorrect. You cannot direct traffic to AWS WAF using an Alias record.
INCORRECT: "Create an S3 bucket policy with a condition that only allows requests that originate from AWS WAF" is incorrect. This cannot be done. Instead use an OAI in the bucket policy.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Networking & Content Delivery
Question 43Skipped
A company is migrating its legacy customer support applications from an on-premises data center to AWS. Each application runs on a dedicated virtual machine and relies on proprietary software that cannot be modified. The applications must remain highly available and continue to operate in the event of a single Availability Zone failure. The company wants to minimize changes to its architecture and operational overhead.
Which solution will meet these requirements?
Use AWS Elastic Disaster Recovery (AWS DRS) to replicate the on-premises virtual machines to AWS. Launch the virtual machines in an Auto Scaling group configured to span multiple Availability Zones.
Refactor the applications into microservices and deploy them on Amazon ECS with Fargate. Use a Network Load Balancer to route traffic to the Fargate tasks.
Use AWS Backup to configure hourly backups of each EC2 instance. Store backups in Amazon S3 Glacier. In case of failure, restore the latest backup to a new EC2 instance in another Availability Zone.
Correct answer
Create an Amazon Machine Image (AMI) for each application. Launch two EC2 instances for each application in different Availability Zones. Use an Application Load Balancer to distribute traffic evenly between the instances.
Overall explanation
Create an Amazon Machine Image (AMI) for each application. Launch two EC2 instances for each application in different Availability Zones. Use an Application Load Balancer to distribute traffic evenly between the instances: This is the correct solution as it provides high availability by deploying instances across Availability Zones and distributes traffic using a load balancer.
Use AWS Backup to configure hourly backups of each EC2 instance. Store backups in Amazon S3 Glacier. In case of failure, restore the latest backup to a new EC2 instance in another Availability Zone: While backups help in disaster recovery, this solution does not provide high availability or fault tolerance in real-time.
Use AWS Elastic Disaster Recovery (AWS DRS) to replicate the on-premises virtual machines to AWS. Launch the virtual machines in an Auto Scaling group configured to span multiple Availability Zones: While AWS DRS is useful for disaster recovery, this approach introduces unnecessary complexity for an already migrated application.
Refactor the applications into microservices and deploy them on Amazon ECS with Fargate. Use a Network Load Balancer to route traffic to the Fargate tasks: This is incorrect because the requirement explicitly states that the proprietary applications cannot be modified.
References:
https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
https://docs.aws.amazon.com/auto-scaling/index.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
Domain
AWS Networking & Content Delivery
Question 50Skipped
An online education company is launching a new e-learning platform on AWS. The platform will run on Amazon EC2 instances deployed across multiple Availability Zones in multiple AWS Regions. Students worldwide will access the platform through the internet to stream educational content. The company wants to ensure that each student is directed to the EC2 instances in the Region that is geographically closest to their location. The solution must provide high availability and efficient traffic routing.
Which solution will meet these requirements?
Correct answer
Use Amazon Route 53 latency routing policy to direct students to the Region with the lowest network latency. Use an internet-facing Application Load Balancer to distribute traffic across the EC2 instances within each Region.
Use Amazon Route 53 geoproximity routing policy to route students to the geographically closest Region. Configure an internet-facing Network Load Balancer to distribute traffic across the EC2 instances within each Availability Zone.
Use Amazon Route 53 weighted routing policy to balance traffic across Regions. Use an internet-facing Application Load Balancer to distribute traffic across the EC2 instances within each Availability Zone.
Use Amazon Route 53 geolocation routing policy to direct students to the closest Region. Use an internet-facing Application Load Balancer to distribute traffic across the EC2 instances within each Region.
Overall explanation
Use Amazon Route 53 latency routing policy to direct students to the Region with the lowest network latency. Use an internet-facing Application Load Balancer to distribute traffic across the EC2 instances within each Region: This is correct because the latency routing policy dynamically routes users to the Region with the lowest latency. The Application Load Balancer ensures traffic is evenly distributed across all EC2 instances within the Region.
Use Amazon Route 53 geolocation routing policy to direct students to the closest Region. Use an internet-facing Application Load Balancer to distribute traffic across the EC2 instances within each Region: This is incorrect because the geolocation routing policy routes users based on their geographic location, which may not always align with the Region with the lowest latency. For example, users in a region geographically close to a Region with high latency may not experience the best performance.
Use Amazon Route 53 geoproximity routing policy to route students to the geographically closest Region. Configure an internet-facing Network Load Balancer to distribute traffic across the EC2 instances within each Availability Zone: This is incorrect because while geoproximity routing directs users based on proximity, it requires manual adjustments for bias, which increases operational complexity. Additionally, a Network Load Balancer is less suitable for HTTP/HTTPS workloads compared to an Application Load Balancer.
Use Amazon Route 53 weighted routing policy to balance traffic across Regions. Use an internet-facing Application Load Balancer to distribute traffic across the EC2 instances within each Availability Zone: This is incorrect because a weighted routing policy does not guarantee that users are directed to the closest Region or the one with the lowest latency.
References:
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
https://aws.amazon.com/elasticloadbalancing/application-load-balancer/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-route-53/
Domain
AWS Networking & Content Delivery
Question 51Skipped
A security officer requires that access to company financial reports is logged. The reports are stored in an Amazon S3 bucket. Additionally, any modifications to the log files must be detected.
Which actions should a solutions architect take?
Correct answer
Use AWS CloudTrail to create a new trail. Configure the trail to log read and write data events on the S3 bucket that houses the reports. Log these events to a new bucket, and enable log file validation
Use AWS CloudTrail to create a new trail. Configure the trail to log read and write management events on the S3 bucket that houses the reports. Log these events to a new bucket, and enable log file validation
Use S3 server access logging on the bucket that houses the reports with the read and write data events and the log file validation options enabled
Use S3 server access logging on the bucket that houses the reports with the read and write management events and log file validation options enabled
Overall explanation
Amazon CloudTrail can be used to log activity on the reports. The key difference between the two answers that include CloudTrail is that one references data events whereas the other references management events.
Data events provide visibility into the resource operations performed on or within a resource. These are also known as data plane operations. Data events are often high-volume activities.
Example data events include:
• Amazon S3 object-level API activity (for example, GetObject, DeleteObject, and PutObject API operations).
• AWS Lambda function execution activity (the Invoke API).
Management events provide visibility into management operations that are performed on resources in your AWS account. These are also known as control plane operations. Example management events include:
• Configuring security (for example, IAM AttachRolePolicy API operations)
• Registering devices (for example, Amazon EC2 CreateDefaultVpc API operations).
Therefore, to log data about access to the S3 objects the solutions architect should log read and write data events.


Log file validation can also be enabled on the destination bucket:


CORRECT: "Use AWS CloudTrail to create a new trail. Configure the trail to log read and write data events on the S3 bucket that houses the reports. Log these events to a new bucket, and enable log file validation" is the correct answer.
INCORRECT: "Use AWS CloudTrail to create a new trail. Configure the trail to log read and write management events on the S3 bucket that houses the reports. Log these events to a new bucket, and enable log file validation" is incorrect as data events should be logged rather than management events.
INCORRECT: "Use S3 server access logging on the bucket that houses the reports with the read and write data events and the log file validation options enabled" is incorrect as server access logging does not have an option for choosing data events or log file validation.
INCORRECT: "Use S3 server access logging on the bucket that houses the reports with the read and write management events and log file validation options enabled" is incorrect as server access logging does not have an option for choosing management events or log file validation.
References:
https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-data-events-with-cloudtrail.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-cloudtrail/
Domain
AWS Networking & Content Delivery
Question 54Skipped
A financial services company needs to set up an Amazon RDS Multi-AZ database to store customer transaction records. The database will serve as the backend for an on-premises financial analysis application. The company requires the on-premises application to connect directly to the RDS database when employees are working from the office.
The company must ensure the connection is established securely and efficiently.
Which solution provides the required connectivity MOST securely?
Create a VPC with two private subnets. Deploy the RDS database in the private subnets. Configure RDS security groups to allow the on-premises office IP ranges to access the database directly over the internet.
Correct answer
Create a VPC with two private subnets. Deploy the RDS database in the private subnets. Establish connectivity between the on-premises office and AWS using AWS Site-to-Site VPN with a customer gateway.
Create a VPC with two public subnets. Deploy the RDS database in the public subnets. Configure an AWS Direct Connect connection between the on-premises office and the VPC for low-latency access.
Create a VPC with two public subnets. Deploy the RDS database in the public subnets. Use AWS Client VPN to establish secure connectivity between employees’ desktops and the database.
Overall explanation
Create a VPC with two private subnets. Deploy the RDS database in the private subnets. Establish connectivity between the on-premises office and AWS using AWS Site-to-Site VPN with a customer gateway:
This is correct because placing the RDS database in private subnets ensures it is not publicly accessible. Using AWS Site-to-Site VPN securely connects the on-premises office to the VPC, allowing direct connectivity to the database while maintaining security.
Create a VPC with two public subnets. Deploy the RDS database in the public subnets. Configure an AWS Direct Connect connection between the on-premises office and the VPC for low-latency access:
This is incorrect because placing the RDS database in public subnets exposes it to the internet, violating security best practices. While Direct Connect provides low latency, public subnets do not meet the company's security requirements.
Create a VPC with two private subnets. Deploy the RDS database in the private subnets. Configure RDS security groups to allow the on-premises office IP ranges to access the database directly over the internet:
This is incorrect because private subnets do not have direct internet access, and accessing the database over the internet introduces security vulnerabilities, even with security group rules.
Create a VPC with two public subnets. Deploy the RDS database in the public subnets. Use AWS Client VPN to establish secure connectivity between employees’ desktops and the database:
This is incorrect because deploying the database in public subnets unnecessarily exposes it to potential threats. Client VPN is a good solution for employee access but does not address the requirement to connect securely from an on-premises office.
References:
https://docs.aws.amazon.com/vpn/latest/s2svpn/VPN_Overview.html
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_VPC.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-vpc/
Domain
AWS Networking & Content Delivery
Question 55Skipped
A company hosts statistical data in an Amazon S3 bucket that users around the world download from their website using a URL that resolves to a domain name. The company needs to provide low latency access to users and plans to use Amazon Route 53 for hosting DNS records.
Which solution meets these requirements?
Correct answer
Create a web distribution on Amazon CloudFront pointing to an Amazon S3 origin. Create an ALIAS record in the Amazon Route 53 hosted zone that points to the CloudFront distribution, resolving to the application's URL domain name.
Create an A record in Route 53, use a Route 53 traffic policy for the web application, and configure a geolocation rule. Configure health checks to check the health of the endpoint and route DNS queries to other endpoints if an endpoint is unhealthy.
Create an A record in Route 53, use a Route 53 traffic policy for the web application, and configure a geoproximity rule. Configure health checks to check the health of the endpoint and route DNS queries to other endpoints if an endpoint is unhealthy.
Create a web distribution on Amazon CloudFront pointing to an Amazon S3 origin. Create a CNAME record in a Route 53 hosted zone that points to the CloudFront distribution, resolving to the application's URL domain name.
Overall explanation
This is a simple requirement for low latency access to the contents of an Amazon S3 bucket for global users. The best solution here is to use Amazon CloudFront to cache the content in Edge Locations around the world. This involves creating a web distribution that points to an S3 origin (the bucket) and then create an Alias record in Route 53 that resolves the applications URL to the CloudFront distribution endpoint.
CORRECT: "Create a web distribution on Amazon CloudFront pointing to an Amazon S3 origin. Create an ALIAS record in the Amazon Route 53 hosted zone that points to the CloudFront distribution, resolving to the application's URL domain name" is the correct answer.
INCORRECT: "Create a web distribution on Amazon CloudFront pointing to an Amazon S3 origin. Create a CNAME record in a Route 53 hosted zone that points to the CloudFront distribution, resolving to the application's URL domain name" is incorrect. An Alias record should be used to point to an Amazon CloudFront distribution.
INCORRECT: "Create an A record in Route 53, use a Route 53 traffic policy for the web application, and configure a geolocation rule. Configure health checks to check the health of the endpoint and route DNS queries to other endpoints if an endpoint is unhealthy" is incorrect. There is only a single endpoint (the Amazon S3 bucket) so this strategy would not work. Much better to use CloudFront to cache in multiple locations.
INCORRECT: "Create an A record in Route 53, use a Route 53 traffic policy for the web application, and configure a geoproximity rule. Configure health checks to check the health of the endpoint and route DNS queries to other endpoints if an endpoint is unhealthy" is incorrect. Again, there is only one endpoint so this strategy will simply not work.
References:
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/RoutingToS3Bucket.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
https://digitalcloud.training/amazon-route-53/
Domain
AWS Networking & Content Delivery
Question 56Skipped
A company requires a fully managed replacement for an on-premises storage service. The company’s employees often work remotely from various locations. The solution should also be easily accessible to systems connected to the on-premises environment.
Which solution meets these requirements?
Use AWS DataSync to synchronize data between the on-premises service and Amazon S3.
Use AWS Transfer Acceleration to replicate files to Amazon S3 and enable public access.
Use AWS Storage Gateway to create a volume gateway to store and transfer files to Amazon S3.
Correct answer
Use Amazon FSx to create an SMB file share. Connect remote clients to the file share over a client VPN.
Overall explanation
Amazon FSx for Windows File Server (Amazon FSx) is a fully managed, highly available, and scalable file storage solution built on Windows Server that uses the Server Message Block (SMB) protocol. It allows for Microsoft Active Directory integration, data deduplication, and fully managed backups, among other critical enterprise features.
An Amazon FSx file system can be created to host the file shares. Clients can then be connected to an AWS Client VPN endpoint and gateway to enable remote access. The protocol used in this solution will be SMB.
CORRECT: "Use Amazon FSx to create an SMB file share. Connect remote clients to the file share over a client VPN" is the correct answer.
INCORRECT: "Use AWS Transfer Acceleration to replicate files to Amazon S3 and enable public access" is incorrect. This is simply a way of improving upload speeds to S3, it is not suitable for enabling internal and external access to a file system.
INCORRECT: "Use AWS DataSync to synchronize data between the on-premises service and Amazon S3" is incorrect. The on-premises solution is to be replaced so this is not a satisfactory solution. Also, DataSync syncs one way, it is not bidirectional.
INCORRECT: "Use AWS Storage Gateway to create a volume gateway to store and transfer files to Amazon S3" is incorrect. Storage Gateway volume gateways are mounted using block-based protocols (iSCSI), so this would not be workable as block-based protocols cannot be used over long distances such as by the workers in remote locations.
References:
https://aws.amazon.com/blogs/storage/accessing-smb-file-shares-remotely-with-amazon-fsx-for-windows-file-server/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Networking & Content Delivery
Question 58Skipped
A company has deployed an application that consists of several microservices running on Amazon EC2 instances behind an Amazon API Gateway API. A Solutions Architect is concerned that the microservices are not designed to elastically scale when large increases in demand occur.
Which solution addresses this concern?
Use Amazon CloudWatch alarms to notify operations staff when the microservices are suffering high CPU utilization.
Use an Elastic Load Balancer to distribute the traffic between the microservices. Configure Amazon CloudWatch metrics to monitor traffic to the microservices.
Spread the microservices across multiple Availability Zones and configure Amazon Data Lifecycle Manager to take regular snapshots.
Correct answer
Create an Amazon SQS queue to store incoming requests. Configure the microservices to retrieve the requests from the queue for processing.
Overall explanation
The individual microservices are not designed to scale. Therefore, the best way to ensure they are not overwhelmed by requests is to decouple the requests from the microservices. An Amazon SQS queue can be created, and the API Gateway can be configured to add incoming requests to the queue. The microservices can then pick up the requests from the queue when they are ready to process them.
CORRECT: "Create an Amazon SQS queue to store incoming requests. Configure the microservices to retrieve the requests from the queue for processing" is the correct answer.
INCORRECT: "Use Amazon CloudWatch alarms to notify operations staff when the microservices are suffering high CPU utilization" is incorrect. This solution requires manual intervention and does not help the application to elastically scale.
INCORRECT: "Spread the microservices across multiple Availability Zones and configure Amazon Data Lifecycle Manager to take regular snapshots" is incorrect. This does not automate the elasticity of the application.
INCORRECT: "Use an Elastic Load Balancer to distribute the traffic between the microservices. Configure Amazon CloudWatch metrics to monitor traffic to the microservices" is incorrect. You cannot use an ELB spread traffic across many different individual microservices as the requests must be directed to individual microservices. Therefore, you would need a target group per microservice, and you would need Auto Scaling to scale the microservices.
References:
https://aws.amazon.com/blogs/compute/understanding-asynchronous-messaging-for-microservices/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Networking & Content Delivery
Question 62Skipped
A company has on-premises file servers that include both Windows SMB and Linux NFS protocols. The company plans to migrate to AWS and consolidate these file servers into a managed cloud solution. The chosen solution must support both NFS and SMB access, provide protocol sharing, and offer redundancy at the Availability Zone level.
Which solution will meet these requirements?
Correct answer
Use Amazon FSx for NetApp ONTAP to consolidate storage and enable multi-protocol access for both SMB and NFS.
Use Amazon S3 for storage and deploy an Amazon S3 File Gateway for on-premises access to both SMB and NFS clients.
Deploy Amazon FSx for Windows File Server for SMB access and Amazon FSx for OpenZFS for NFS access.
Create two Amazon EC2 instances with locally attached storage: one instance for SMB access and the other instance for NFS access.
Overall explanation
Use Amazon FSx for NetApp ONTAP to consolidate storage and enable multi-protocol access for both SMB and NFS: This is correct because Amazon FSx for NetApp ONTAP supports both SMB and NFS protocols with multi-protocol sharing and redundancy across Availability Zones.
Deploy Amazon FSx for Windows File Server for SMB access and Amazon FSx for OpenZFS for NFS access: This is incorrect because this approach separates SMB and NFS access, does not provide protocol sharing, and introduces additional complexity.
Use Amazon S3 for storage and deploy an Amazon S3 File Gateway for on-premises access to both SMB and NFS clients: This is incorrect because Amazon S3 File Gateway does not natively support SMB or NFS protocols for simultaneous access.
Create two Amazon EC2 instances with locally attached storage: one instance for SMB access and the other instance for NFS access: This is incorrect because this solution is not a managed service, lacks redundancy at the Availability Zone level, and increases operational overhead.
References:
https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/what-is-fsx-ontap.html
https://aws.amazon.com/fsx/netapp-ontap/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-fsx/
Domain
AWS Networking & Content Delivery
Question 65Skipped
An online store uses an Amazon Aurora database. The database is deployed as a Multi-AZ deployment. Recently, metrics have shown that database read requests are high and causing performance issues which result in latency for write requests.
What should the solutions architect do to separate the read requests from the write requests?
Create a second Amazon Aurora database and link it to the primary database as a read replica
Enable read through caching on the Amazon Aurora database
Correct answer
Update the application to read from the Aurora Replica
Create a read replica and modify the application to use the appropriate endpoint
Overall explanation
Aurora Replicas are independent endpoints in an Aurora DB cluster, best used for scaling read operations and increasing availability. Up to 15 Aurora Replicas can be distributed across the Availability Zones that a DB cluster spans within an AWS Region.
The DB cluster volume is made up of multiple copies of the data for the DB cluster. However, the data in the cluster volume is represented as a single, logical volume to the primary instance and to Aurora Replicas in the DB cluster.


As well as providing scaling for reads, Aurora Replicas are also targets for multi-AZ. In this case the solutions architect can update the application to read from the Aurora Replica
CORRECT: "Update the application to read from the Aurora Replica" is the correct answer.
INCORRECT: "Create a read replica and modify the application to use the appropriate endpoint" is incorrect. An Aurora Replica is both a standby in a Multi-AZ configuration and a target for read traffic. The architect simply needs to direct traffic to the Aurora Replica.
INCORRECT: "Enable read through caching on the Amazon Aurora database." is incorrect as this is not a feature of Amazon Aurora.
INCORRECT: "Create a second Amazon Aurora database and link it to the primary database as a read replica" is incorrect as an Aurora Replica already exists as this is a Multi-AZ configuration and the standby is an Aurora Replica that can be used for read traffic.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Networking & Content Delivery
Question 5Skipped
A HR application stores employment records on Amazon S3. Regulations mandate the records are retained for seven years. Once created the records are accessed infrequently for the first three months and then must be available within 10 minutes if required thereafter.
Which lifecycle action meets the requirements whilst MINIMIZING cost?
Correct answer
Store the data in S3 Standard-IA for 3 months, then transition to S3 Glacier
Store the data in S3 Intelligent Tiering for 3 months, then transition to S3 Standard-IA
Store the data in S3 Standard for 3 months, then transition to S3 Standard-IA
Store the data in S3 Standard for 3 months, then transition to S3 Glacier
Overall explanation
The most cost-effective solution is to first store the data in S3 Standard-IA where it will be infrequently accessed for the first three months. Then, after three months expires, transition the data to S3 Glacier where it can be stored at lower cost for the remainder of the seven year period. Expedited retrieval can bring retrieval times down to 1-5 minutes.
CORRECT: "Store the data in S3 Standard-IA for 3 months, then transition to S3 Glacier" is the correct answer.
INCORRECT: "Store the data in S3 Standard for 3 months, then transition to S3 Glacier" is incorrect. S3 Standard is more costly than S3 Standard-IA and the data is only accessed infrequently.
INCORRECT: "Store the data in S3 Standard for 3 months, then transition to S3 Standard-IA" is incorrect. Neither storage class in this answer is the most cost-effective option.
INCORRECT: "Store the data in S3 Intelligent Tiering for 3 months, then transition to S3 Standard-IA" is incorrect. Intelligent tiering moves data between tiers based on access patterns, this is more costly and better suited to use cases that are unknown or unpredictable.
References:
https://aws.amazon.com/s3/storage-classes/
https://docs.aws.amazon.com/amazonglacier/latest/dev/downloading-an-archive-two-steps.html#api-downloading-an-archive-two-steps-retrieval-options
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Networking & Content Delivery
Question 16Skipped
A new application will run across multiple Amazon ECS tasks. Front-end application logic will process data and then pass that data to a back-end ECS task to perform further processing and write the data to a datastore. The Architect would like to reduce-interdependencies so failures do no impact other components.
Which solution should the Architect use?
Create an Amazon Kinesis Firehose delivery stream that delivers data to an Amazon S3 bucket, configure the front-end to write data to the stream and the back-end to read data from Amazon S3
Correct answer
Create an Amazon SQS queue and configure the front-end to add messages to the queue and the back-end to poll the queue for messages
Create an Amazon SQS queue that pushes messages to the back-end. Configure the front-end to add messages to the queue
Create an Amazon Kinesis Firehose delivery stream and configure the front-end to add data to the stream and the back-end to read data from the stream
Overall explanation
This is a good use case for Amazon SQS. SQS is a service that is used for decoupling applications, thus reducing interdependencies, through a message bus. The front-end application can place messages on the queue and the back-end can then poll the queue for new messages. Please remember that Amazon SQS is pull-based (polling) not push-based (use SNS for push-based).
CORRECT: "Create an Amazon SQS queue and configure the front-end to add messages to the queue and the back-end to poll the queue for messages" is the correct answer.
INCORRECT: "Create an Amazon Kinesis Firehose delivery stream and configure the front-end to add data to the stream and the back-end to read data from the stream" is incorrect. Amazon Kinesis Firehose is used for streaming data. With Firehose the data is immediately loaded into a destination that can be Amazon S3, RedShift, Elasticsearch, or Splunk. This is not an ideal use case for Firehose as this is not streaming data and there is no need to load data into an additional AWS service.
INCORRECT: "Create an Amazon Kinesis Firehose delivery stream that delivers data to an Amazon S3 bucket, configure the front-end to write data to the stream and the back-end to read data from Amazon S3" is incorrect as per the previous explanation.
INCORRECT: "Create an Amazon SQS queue that pushes messages to the back-end. Configure the front-end to add messages to the queue " is incorrect as SQS is pull-based, not push-based. EC2 instances must poll the queue to find jobs to process.
References:
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/common_use_cases.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-kinesis/
https://digitalcloud.training/aws-application-integration-services/
Domain
AWS Networking & Content Delivery
Question 18Skipped
A company hosts a multiplayer game on AWS. The application uses Amazon EC2 instances in a single Availability Zone and users connect over Layer 4. Solutions Architect has been tasked with making the architecture highly available and also more cost-effective.
How can the solutions architect best meet these requirements? (Select TWO.)
Configure an Application Load Balancer in front of the EC2 instances
Increase the number of instances and use smaller EC2 instance types
Correct selection
Configure a Network Load Balancer in front of the EC2 instances
Correct selection
Configure an Auto Scaling group to add or remove instances in multiple Availability Zones automatically
1. Configure an Auto Scaling group to add or remove instances in the Availability Zone automatically
Overall explanation
The solutions architect must enable high availability for the architecture and ensure it is cost-effective. To enable high availability an Amazon EC2 Auto Scaling group should be created to add and remove instances across multiple availability zones.
In order to distribute the traffic to the instances the architecture should use a Network Load Balancer which operates at Layer 4. This architecture will also be cost-effective as the Auto Scaling group will ensure the right number of instances are running based on demand.
CORRECT: "Configure a Network Load Balancer in front of the EC2 instances" is a correct answer.
CORRECT: "Configure an Auto Scaling group to add or remove instances in multiple Availability Zones automatically" is also a correct answer.
INCORRECT: "Increase the number of instances and use smaller EC2 instance types" is incorrect as this is not the most cost-effective option. Auto Scaling should be used to maintain the right number of active instances.
INCORRECT: "Configure an Auto Scaling group to add or remove instances in the Availability Zone automatically" is incorrect as this is not highly available as it’s a single AZ.
INCORRECT: "Configure an Application Load Balancer in front of the EC2 instances" is incorrect as an ALB operates at Layer 7 rather than Layer 4.
References:
https://docsaws.amazon.com/autoscaling/ec2/userguide/autoscaling-load-balancer.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
Domain
AWS Networking & Content Delivery
Question 24Skipped
A company has uploaded some highly critical data to an Amazon S3 bucket. Management are concerned about data availability and require that steps are taken to protect the data from accidental deletion. The data should still be accessible, and a user should be able to delete the data intentionally.
Which combination of steps should a solutions architect take to accomplish this? (Select TWO.)
Create a bucket policy on the S3 bucket.
Enable default encryption on the S3 bucket.
Correct selection
Enable versioning on the S3 bucket.
Create a lifecycle policy for the objects in the S3 bucket.
Correct selection
Enable MFA Delete on the S3 bucket.
Overall explanation
Multi-factor authentication (MFA) delete adds an additional step before an object can be deleted from a versioning-enabled bucket.
With MFA delete the bucket owner must include the x-amz-mfa request header in requests to permanently delete an object version or change the versioning state of the bucket.
CORRECT: "Enable versioning on the S3 bucket" is a correct answer.
CORRECT: "Enable MFA Delete on the S3 bucket" is also a correct answer.
INCORRECT: "Create a bucket policy on the S3 bucket" is incorrect. A bucket policy is not required to enable MFA delete.
INCORRECT: "Enable default encryption on the S3 bucket" is incorrect. Encryption does not protect against deletion.
INCORRECT: "Create a lifecycle policy for the objects in the S3 bucket" is incorrect. A lifecycle policy will move data to another storage class but does not protect against deletion.
References:
https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingMFADelete.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Networking & Content Delivery
Question 27Skipped
To increase performance and redundancy for an application a company has decided to run multiple implementations in different AWS Regions behind network load balancers. The company currently advertise the application using two public IP addresses from separate /24 address ranges and would prefer not to change these. Users should be directed to the closest available application endpoint.
Which actions should a solutions architect take? (Select TWO.)
Correct selection
Migrate both public IP addresses to the AWS Global Accelerator
Create PTR records to map existing public IP addresses to an Alias
Correct selection
Create an AWS Global Accelerator and attach endpoints in each AWS Region
Create an Amazon Route 53 geolocation based routing policy
Assign new static anycast IP addresses and modify any existing pointers
Overall explanation
AWS Global Accelerator uses static IP addresses as fixed entry points for your application. You can migrate up to two /24 IPv4 address ranges and choose which /32 IP addresses to use when you create your accelerator.
This solution ensures the company can continue using the same IP addresses and they are able to direct traffic to the application endpoint in the AWS Region closest to the end user. Traffic is sent over the AWS global network for consistent performance.

CORRECT: "Create an AWS Global Accelerator and attach endpoints in each AWS Region" is a correct answer.
CORRECT: "Migrate both public IP addresses to the AWS Global Accelerator" is also a correct answer.
INCORRECT: "Create an Amazon Route 53 geolocation based routing policy" is incorrect. With this solution new IP addresses will be required as there will be application endpoints in different regions.
INCORRECT: "Assign new static anycast IP addresses and modify any existing pointers" is incorrect. This is unnecessary as you can bring your own IP addresses to AWS Global Accelerator and this is preferred in this scenario.
INCORRECT: "Create PTR records to map existing public IP addresses to an Alias" is incorrect. This is not a workable solution for mapping existing IP addresses to an Amazon Route 53 Alias.
References:
https://aws.amazon.com/global-accelerator/features/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-global-accelerator/
Domain
AWS Networking & Content Delivery
Question 28Skipped
A company are finalizing their disaster recovery plan. A limited set of core services will be replicated to the DR site ready to seamlessly take over the in the event of a disaster. All other services will be switched off.
Which DR strategy is the company using?
Warm standby
Backup and restore
Multi-site
Correct answer
Pilot light
Overall explanation
In this DR approach, you simply replicate part of your IT structure for a limited set of core services so that the AWS cloud environment seamlessly takes over in the event of a disaster.
A small part of your infrastructure is always running simultaneously syncing mutable data (as databases or documents), while other parts of your infrastructure are switched off and used only during testing.
Unlike a backup and recovery approach, you must ensure that your most critical core elements are already configured and running in AWS (the pilot light). When the time comes for recovery, you can rapidly provision a full-scale production environment around the critical core.
CORRECT: "Pilot light" is the correct answer.
INCORRECT: "Backup and restore" is incorrect. This is the lowest cost DR approach that simply entails creating online backups of all data and applications.
INCORRECT: "Warm standby" is incorrect. The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud.
INCORRECT: "Multi-site" is incorrect. A multi-site solution runs on AWS as well as on your existing on-site infrastructure in an active- active configuration.
References:
https://aws.amazon.com/blogs/publicsector/rapidly-recover-mission-critical-systems-in-a-disaster/
Domain
AWS Networking & Content Delivery
Question 32Skipped
As part of a company’s shift to the AWS cloud, they need to gain an insight into their total on-premises footprint. They have discovered that they are currently struggling with managing their software licenses. They would like to maintain a hybrid cloud setup, with some of their licenses stored in the cloud with some stored on-premises.

What actions should be taken to ensure they are managing the licenses appropriately going forward?
Use AWS Secrets Manager to store the licenses as secrets to ensure they are stored securely
Correct answer
Use AWS License Manager to manage the software licenses
Use the AWS Key Management Service to treat the license key safely and store it securely
Use Amazon S3 with governance lock to manage the storage of the licenses
Overall explanation
AWS License Manager makes it easier to manage your software licenses from vendors such as Microsoft, SAP, Oracle, and IBM across AWS and on-premises environments. AWS License Manager lets administrators create customized licensing rules that mirror the terms of their licensing agreements.
CORRECT: "Use AWS License Manager to manage the software licenses" is the correct answer (as explained above.)
INCORRECT: "Use AWS Secrets Manager to store the licenses as secrets to ensure they are stored securely" is incorrect. AWS Secrets Manager helps you protect secrets needed to access your applications, services, and IT resources. This does not include license keys.
INCORRECT: "Use the AWS Key Management Service to treat the license key safely and store it securely" is incorrect. AWS Key Management Service (AWS KMS) makes it easy for you to create and manage cryptographic keys and control their use across a wide range of AWS services and in your applications, not license keys.
INCORRECT: "Use Amazon S3 with governance lock to manage the storage of the licenses" is incorrect. Amazon S3 is not designed to store software licenses.
References:
https://aws.amazon.com/license-manager/
Domain
AWS Networking & Content Delivery
Question 36Skipped
A company runs a web application that serves weather updates. The application runs on a fleet of Amazon EC2 instances in a Multi-AZ Auto scaling group behind an Application Load Balancer (ALB). The instances store data in an Amazon Aurora database. A solutions architect needs to make the application more resilient to sporadic increases in request rates.
Which architecture should the solutions architect implement? (Select TWO.)
Add an AWS Global Accelerator endpoint
Correct selection
Add Amazon Aurora Replicas
Correct selection
Add an Amazon CloudFront distribution in front of the ALB
Add and AWS WAF in front of the ALB
Add an AWS Transit Gateway to the Availability Zones
Overall explanation
The architecture is already highly resilient but may be subject to performance degradation if there are sudden increases in request rates. To resolve this situation Amazon Aurora Read Replicas can be used to serve read traffic which offloads requests from the main database. On the frontend an Amazon CloudFront distribution can be placed in front of the ALB and this will cache content for better performance and also offloads requests from the backend.
CORRECT: "Add Amazon Aurora Replicas" is the correct answer.
CORRECT: "Add an Amazon CloudFront distribution in front of the ALB" is the correct answer.
INCORRECT: "Add and AWS WAF in front of the ALB" is incorrect. A web application firewall protects applications from malicious attacks. It does not improve performance.
INCORRECT: "Add an AWS Transit Gateway to the Availability Zones" is incorrect as this is used to connect on-premises networks to VPCs.
INCORRECT: "Add an AWS Global Accelerator endpoint" is incorrect as this service is used for directing users to different instances of the application in different regions based on latency.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Networking & Content Delivery
Question 46Skipped
An application has been deployed on Amazon EC2 instances behind an Application Load Balancer (ALB). A Solutions Architect must improve the security posture of the application and minimize the impact of a DDoS attack on resources.
Which of the following solutions is MOST effective?
Correct answer
Configure an AWS WAF ACL with rate-based rules. Enable the WAF ACL on the Application Load Balancer.
Enable access logs on the Application Load Balancer and configure Amazon CloudWatch to monitor the access logs and trigger a Lambda function when potential attacks are identified. Configure the Lambda function to modify the ALBs security group and block the attack.
Enable VPC Flow Logs and store them in Amazon S3. Use Amazon Athena to parse the logs and identify and block potential DDoS attacks.
Create a custom AWS Lambda function that monitors for suspicious traffic and modifies a network ACL when a potential DDoS attack is identified.
Overall explanation
A rate-based rule tracks the rate of requests for each originating IP address, and triggers the rule action on IPs with rates that go over a limit. You set the limit as the number of requests per 5-minute time span.
You can use this type of rule to put a temporary block on requests from an IP address that's sending excessive requests. By default, AWS WAF aggregates requests based on the IP address from the web request origin, but you can configure the rule to use an IP address from an HTTP header, like X-Forwarded-For, instead.
CORRECT: "Configure an AWS WAF ACL with rate-based rules. Enable the WAF ACL on the Application Load Balancer" is the correct answer.
INCORRECT: "Create a custom AWS Lambda function that monitors for suspicious traffic and modifies a network ACL when a potential DDoS attack is identified" is incorrect. There’s not description here of how Lambda is going to monitor for traffic.
INCORRECT: "Enable VPC Flow Logs and store them in Amazon S3. Use Amazon Athena to parse the logs and identify and block potential DDoS attacks" is incorrect. Amazon Athena is not able to block DDoS attacks, another service would be needed.
INCORRECT: "Enable access logs on the Application Load Balancer and configure Amazon CloudWatch to monitor the access logs and trigger a Lambda function when potential attacks are identified. Configure the Lambda function to modify the ALBs security group and block the attack" is incorrect. Access logs are exported to S3 but not to CloudWatch. Also, it would not be possible to block an attack from a specific IP using a security group (while still allowing any other source access) as they do not support deny rules.
References:
https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-rate-based.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-waf-shield/
Domain
AWS Networking & Content Delivery
Question 62Skipped
A Solutions Architect has been tasked with building an application which stores images to be used for a website. The website will be accessed by thousands of customers. The images within the application need to be able to be transformed and processed as they are being retrieved. The solutions architect would prefer to use managed services to achieve this, and the solution should be highly available and scalable, and be able to serve users from around the world with low latency.

Which scenario represents the easiest solution for this task?
Store the images in a DynamoDB table, with DynamoDB Accelerator enabled. Use Amazon EventBridge to pass the data into an event bus as it is retrieved from DynamoDB and use AWS Lambda to process the data.
Store the images in a DynamoDB table, with DynamoDB Global Tables enabled. Provision a Lambda function to process the data on demand as it leaves the table.
Correct answer
Store the images in Amazon S3, behind a CloudFront distribution. Use S3 Object Lambda to transform and process the images whenever a GET request is initiated on an object.
Store the images in Amazon S3, behind a CloudFront distribution. Use S3 Event Notifications to connect to a Lambda function to process and transform the images when a GET request is initiated on an object.
Overall explanation
With S3 Object Lambda you can add your own code to S3 GET requests to modify and process data as it is returned to an application. For the first time, you can use custom code to modify the data returned by standard S3 GET requests to filter rows, dynamically resize images, redact confidential data, and much more. Powered by AWS Lambda functions, your code runs on infrastructure that is fully managed by AWS, eliminating the need to create and store derivative copies of your data or to run expensive proxies, all with no changes required to your applications.
CORRECT: "Store the images in Amazon S3, behind a CloudFront distribution. Use S3 Object Lambda to transform and process the images whenever a GET request is initiated on an object” is the correct answer (as explained above.)
INCORRECT: "Store the images in a DynamoDB table, with DynamoDB Global Tables enabled. Provision a Lambda function to process the data on demand as it leaves the table” is incorrect. DynamoDB is not as well designed for Write Once Read Many workloads and adding a Lambda function to the DynamoDB table takes more manual provisioning of resources than using S3 Object Lambda.
INCORRECT: "Store the images in Amazon S3, behind a CloudFront distribution. Use S3 Event Notifications to connect to a Lambda function to process and transform the images when a GET request is initiated on an object” is incorrect. This would work; however it is easier to use S3 Object Lambda as this manages the Lambda function for you.
INCORRECT: "Store the images in a DynamoDB table, with DynamoDB Accelerator enabled. Use Amazon EventBridge to pass the data into an event bus as it is retrieved from DynamoDB and use AWS Lambda to process the data” is incorrect. DynamoDB is not as well designed for Write Once Read Many workloads and adding a Lambda function to the DynamoDB table takes more manual provisioning of resources than using S3 Object Lambda.
References:
https://aws.amazon.com/s3/features/object-lambda/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/
Domain
AWS Networking & Content Delivery
Question 2Skipped
Data from 45 TB of data is used for reporting by a company. The company wants to move this data from on premises into the AWS cloud. A custom application in the company's data center runs a weekly data transformation job and the company plans to pause the application until the data transfer is complete and needs to begin the transfer process as soon as possible.
The data center bandwidth is saturated, and a solutions architect has been tasked to transfer the data and must configure the transformation job to continue to run in the AWS Cloud.
Which solution will meet these requirements with the LEAST operational overhead?
The data will be moved using an AWS Snowcone device. The transformation application should be deployed to the device.
Correct answer
Order an AWS Snowball Edge Storage Optimized device. Copy the data to the device. and create a custom transformation job by using AWS Glue.
The data can be moved using AWS DataSync. Using AWS Glue, create a custom transformation job.
Order an AWS Snowball Edge Storage Optimized device that includes Amazon EC2 compute. Transfer the data to the device. Launch a new EC2 instance to run the transformation application.
Overall explanation
As the network is saturated, the solutions architect will have to use a physical solution, i.e. a member of the snow family to achieve this requirement quickly. As the data transformation job needs to be completed in the cloud, using AWS Glue will suit this requirement also. AWS Glue is a managed data transformation service.
CORRECT: "Order an AWS Snowball Edge Storage Optimized device. Copy the data to the device. and create a custom transformation job by using AWS Glue" is the correct answer (as explained above.)
INCORRECT: "The data can be moved using AWS DataSync. Using AWS Glue, create a custom transformation job” is incorrect. As the network is saturated, AWS DataSync will not work as it is primarily an online data transfer service to transfer data between a data center and AWS.
INCORRECT: "The data will be moved using an AWS Snowcone device. The transformation application should be deployed to the device” is incorrect. You would not be able to deploy a transformation service locally to the Snowcone device as it is not optimized for compute operations.
INCORRECT: "Order an AWS Snowball Edge Storage Optimized device that includes Amazon EC2 compute. Transfer the data to the device. Launch a new EC2 instance to run the transformation application” is incorrect. Using an EC2 instance instead of a managed service like AWS Glue will include more operational overhead for the organization.
References:
https://aws.amazon.com/glue/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-glue/
Domain
AWS Networking & Content Delivery
Question 15Skipped
A Solutions Architect is designing an application for processing and extracting data from log files. The log files are generated by an application and the number and frequency of updates varies. The files are up to 1 GB in size and processing will take around 40 seconds for each file.
Which solution is the most cost-effective?
Write the log files to an Amazon SQS queue. Use AWS Lambda to process the files from the queue and save to an Amazon S3 bucket
Correct answer
Write the log files to an Amazon S3 bucket. Create an event notification to invoke an AWS Lambda function that will process the files
Write the log files to an Amazon EC2 instance with an attached EBS volume. After processing, save the files to an Amazon S3 bucket
Write the log files to an Amazon S3 bucket. Create an event notification to invoke an Amazon ECS task to process the files and save to an Amazon S3 bucket
Overall explanation
The question asks for the most cost-effective solution and therefor a serverless and automated solution will be the best choice.
AWS Lambda can run custom code in response to Amazon S3 bucket events. You upload your custom code to AWS Lambda and create a function. When Amazon S3 detects an event of a specific type (for example, an object created event), it can publish the event to AWS Lambda and invoke your function in Lambda. In response, AWS Lambda executes your function.


CORRECT: "Write the log files to an Amazon S3 bucket. Create an event notification to invoke an AWS Lambda function that will process the files" is the correct answer.
INCORRECT: "Write the log files to an Amazon EC2 instance with an attached EBS volume. After processing, save the files to an Amazon S3 bucket" is incorrect. This is not cost effective as it is not serverless.
INCORRECT: "Write the log files to an Amazon SQS queue. Use AWS Lambda to process the files from the queue and save to an Amazon S3 bucket" is incorrect. SQS has a maximum message size of 256 KB so the message body would need to be saved in S3 anyway. Using an event source mapping from S3 would be less complex and preferable.
INCORRECT: "Write the log files to an Amazon S3 bucket. Create an event notification to invoke an Amazon ECS task to process the files and save to an Amazon S3 bucket" is incorrect. You cannot use event notifications to process Amazon ECS tasks.
References:
https://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
https://digitalcloud.training/aws-lambda/
Domain
AWS Networking & Content Delivery
Question 26Skipped
A company's web application is using multiple Amazon EC2 Linux instances and storing data on Amazon EBS volumes. The company is looking for a solution to increase the resiliency of the application in case of a failure.
What should a solutions architect do to meet these requirements?
Launch the application on EC2 instances in each Availability Zone. Attach EBS volumes to each EC2 instance
Correct answer
Create an Application Load Balancer with Auto Scaling groups across multiple Availability Zones. Store data on Amazon EFS and mount a target on each instance
Create an Application Load Balancer with Auto Scaling groups across multiple Availability Zones. Mount an instance store on each EC2 instance
Create an Application Load Balancer with Auto Scaling groups across multiple Availability Zones. Store data using Amazon S3 One Zone-Infrequent Access (S3 One Zone-A)
Overall explanation
To increase the resiliency of the application the solutions architect can use Auto Scaling groups to launch and terminate instances across multiple availability zones based on demand. An application load balancer (ALB) can be used to direct traffic to the web application running on the EC2 instances.
Lastly, the Amazon Elastic File System (EFS) can assist with increasing the resilience of the application by providing a shared file system that can be mounted by multiple EC2 instances from multiple availability zones.
CORRECT: "Create an Application Load Balancer with Auto Scaling groups across multiple Availability Zones. Store data on Amazon EFS and mount a target on each instance" is the correct answer.
INCORRECT: "Launch the application on EC2 instances in each Availability Zone. Attach EBS volumes to each EC2 instance" is incorrect as the EBS volumes are single points of failure which are not shared with other instances.
INCORRECT: "Create an Application Load Balancer with Auto Scaling groups across multiple Availability Zones. Mount an instance store on each EC2 instance" is incorrect as instance stores are ephemeral data stores which means data is lost when powered down. Also, instance stores cannot be shared between instances.
INCORRECT: "Create an Application Load Balancer with Auto Scaling groups across multiple Availability Zones. Store data using Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)" is incorrect as there are data retrieval charges associated with this S3 tier. It is not a suitable storage tier for application files.
References:
https://docs.aws.amazon.com/efs/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-efs/
Domain
AWS Networking & Content Delivery
Question 29Skipped
A company observed an increase in Amazon EC2 costs in its most recent bill. The billing team noticed unwanted vertical scaling of instance types for a couple of EC2 instances. A solutions architect needs to create a graph comparing the last 2 months of EC2 costs and perform an in-depth analysis to identify the root cause of the vertical scaling.
How should the solutions architect generate the information with the LEAST operational overhead?
Correct answer
Use Cost Explorer's granular filtering feature to perform an in-depth analysis of EC2 costs based on instance types.
Use AWS Budgets to create a budget report and compare EC2 costs based on instance types.
Use graphs from the AWS Billing and Cost Management dashboard to compare EC2 costs based on instance types for the last 2 months.
Use AWS Cost and Usage Reports to create a report and send it to an Amazon S3 bucket. Use Amazon QuickSight with Amazon S3 as a source to generate an interactive graph based on instance types.
Overall explanation
AWS Cost Explorer would be the easiest way to graph this data. Cost Explorer can be accessed easily and has features for filtering billing data and graphing across relevant time periods.

CORRECT: "Use Cost Explorer's granular filtering feature to perform an in-depth analysis of EC2 costs based on instance types" is the correct answer (as explained above.)
INCORRECT: "Use AWS Budgets to create a budget report and compare EC2 costs based on instance types" is incorrect.
AWS Budgets lets you set custom cost and usage budgets that alert you when your budget thresholds are exceeded (or forecasted to be exceeded).
INCORRECT: "Use graphs from the AWS Billing and Cost Management dashboard to compare EC2 costs based on instance types for the last 2 months" is incorrect.
The granularity required is not available in the billing and cost management dashboard unless using the cost and usage report.
INCORRECT: "Use AWS Cost and Usage Reports to create a report and send it to an Amazon S3 bucket. Use Amazon QuickSight with Amazon S3 as a source to generate an interactive graph based on instance types" is incorrect. This could provide the required graphs, but it involves much more operational overhead.
References:
https://aws.amazon.com/aws-cost-management/aws-cost-explorer/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-cost-management/
Domain
AWS Networking & Content Delivery
Question 38Skipped
A company has an on-premises server that uses a MySQL database to process and store customer information. The company wants to migrate to an AWS database service to achieve higher availability and to improve application performance. Additionally, the company wants to offload reporting workloads from its primary database to ensure it remains performant.
Which solution will meet these requirements in the MOST operationally efficient way?
Use AWS Database Migration Service (AWS DMS) to create an Amazon Aurora DB cluster in multiple AWS Regions. Point the reporting functions toward a separate DB instance from the primary DB instance.
Use Amazon RDS with MySQL in a Single-AZ deployment. Create a read replica in the same availability zone as the primary DB instance. Direct the reporting functions to the read replica.
Correct answer
Use Amazon Aurora with MySQL compatibility. Direct the reporting functions to use one of the Aurora Replicas.
Use Amazon EC2 instances to deploy a self-managed MySQL database with a replication setup for reporting purposes. Place instances in multiple availability zones and manage backups and patching manually.
Overall explanation
Amazon Aurora with MySQL compatibility is a good fit for achieving high availability and improved performance. Aurora automatically distributes the data across multiple AZs in a single region. Additionally, Aurora allows the creation of up to 15 Aurora Replicas that share the same underlying volume as the primary instance. Directing reporting functions to the Aurora Replica is an effective way to offload reporting workloads from the primary database.
CORRECT: "Use Amazon Aurora with MySQL compatibility. Direct the reporting functions to use one of the Aurora Replicas" is the correct answer (as explained above.)
INCORRECT: "Use Amazon RDS with MySQL in a Single-AZ deployment. Create a read replica in the same availability zone as the primary DB instance. Direct the reporting functions to the read replica" is incorrect.
Though you can use Amazon RDS with MySQL in a Single-AZ deployment and create a read replica, it is not the most operationally efficient option as it does not provide the high availability that Aurora's architecture offers.
INCORRECT: "Use AWS Database Migration Service (AWS DMS) to create an Amazon Aurora DB cluster in multiple AWS Regions. Point the reporting functions toward a separate DB instance from the primary DB instance" is incorrect.
Using AWS DMS to create Amazon Aurora DB clusters in multiple AWS Regions would be overkill for the requirements. It could also introduce additional complexity and doesn’t specifically address using a replica for reporting purposes.
INCORRECT: "Use Amazon EC2 instances to deploy a self-managed MySQL database with a replication setup for reporting purposes. Place instances in multiple availability zones and manage backups and patching manually" is incorrect.
Managing your own database on Amazon EC2 instances requires a significant operational overhead as you need to handle backups, patch management, and high availability yourself. This option is not the most operationally efficient compared to using a managed database service like Amazon Aurora.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Networking & Content Delivery
Question 42Skipped
A media company is designing a disaster recovery (DR) solution for a business-critical application. The recovery time objective (RTO) should be 4 hours or less. The application is running on Amazon EC2 instances using the fewest possible AWS resources during normal operations.
Which of the following is recommended to implement the DR solution across regions cost-effectively?
Correct answer
Create Amazon Machine Images (AMIs) to back up the EC2 instances. Copy the AMIs to a secondary AWS Region. Automate infrastructure deployment in the secondary Region by using AWS CloudFormation.
Launch EC2 instances in a secondary Availability Zone. Keep the EC2 instances in the secondary Availability Zone active at all times.
Create Amazon Machine Images (AMI) to back up the EC2 instances. Copy the AMIs to a secondary AWS Region. Automate infrastructure deployment in the secondary Region by using AWS Lambda and custom scripts.
Launch EC2 instances in a secondary AWS Region. Keep the EC2 instances in the secondary Region active at all times.
Overall explanation
When you have a few hours to achieve disaster recovery, copying AMI’s across regions is an achievable solution. AWS CloudFormation can then be us
ed to quickly spin up the instances in the second region when a disaster recovery event occurs. This is the most cost-effective option as only the active site has running instances.

CORRECT: "Create Amazon Machine Images (AMIs) to back up the EC2 instances. Copy the AMIs to a secondary AWS Region. Automate infrastructure deployment in the secondary Region by using AWS CloudFormation" is the correct answer (as explained above.)
INCORRECT: "Create Amazon Machine Images (AMI) to back up the EC2 instances. Copy the AMIs to a secondary AWS Region. Automate infrastructure deployment in the secondary Region by using AWS Lambda and custom scripts" is incorrect.
AWS CloudFormation is more suited to deploying infrastructure than using Lambda with custom scripts.
INCORRECT: "Launch EC2 instances in a secondary AWS Region. Keep the EC2 instances in the secondary Region active at all times" is incorrect.
This approach can work but this is not a cost-effective choice.
INCORRECT: "Launch EC2 instances in a secondary Availability Zone. Always keep the EC2 instances in the secondary Availability Zone active" is incorrect. As with the previous answer, this is not cost-effective.
References:
https://aws.amazon.com/blogs/architecture/disaster-recovery-dr-architecture-on-aws-part-i-strategies-for-recovery-in-the-cloud/
https://aws.amazon.com/blogs/architecture/creating-a-multi-region-application-with-aws-services-part-1-compute-and-security/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-cloudformation/
Domain
AWS Networking & Content Delivery
Question 46Skipped
A healthcare company maintains patient records in Amazon S3. To comply with HIPAA regulations, the stored data must not contain any protected health information (PHI). The company recently found out that some objects in the S3 buckets contain PHI. The company needs to automate the detection of PHI in the S3 buckets and notify its compliance team when such data is detected.
Which solution will meet these requirements?
Use AWS Security Hub. Create an AWS Lambda function to filter the ‘Security Hub findings - High severity’ event type and trigger an Amazon Simple Email Service (Amazon SES) notification to the compliance team.
Correct answer
Use Amazon Macie. Create an Amazon EventBridge rule to filter the ‘SensitiveData:S3Object/Health’ event type from Macie findings and trigger an Amazon Simple Email Service (Amazon SES) notification to the compliance team.
Use Amazon Macie. Create an AWS Lambda function to filter the ‘SensitiveData:S3Object/Personal’ event type from Macie findings and trigger an Amazon Simple Notification Service (Amazon SNS) notification to the compliance team.
Use AWS Security Hub. Create an Amazon EventBridge rule to filter the ‘Security Hub findings - High severity’ event type and send an Amazon Simple Notification Service (Amazon SNS) notification to the compliance team.
Overall explanation
Amazon Macie is a security service that uses machine learning to automatically discover, classify, and protect sensitive data like PHI. An Amazon EventBridge rule can be created to filter specific event types from Macie findings. When Macie identifies PHI in the S3 bucket, the EventBridge rule triggers an Amazon SNS notification to the compliance team.
CORRECT: "Use Amazon Macie. Create an Amazon EventBridge rule to filter the ‘SensitiveData:S3Object/Health’ event type from Macie findings and trigger an Amazon Simple Email Service (Amazon SES) notification to the compliance team".
The correct filter is ‘SensitiveData:S3Object/Personal’ which includes personally identifiable information (PII) such as passport numbers or driver's license identification numbers, personal health information (PHI) such as health insurance or medical identification numbers, or a combination of PII and PHI.
INCORRECT: "Use AWS Security Hub. Create an Amazon EventBridge rule to filter the ‘Security Hub findings - High severity’ event type and send an Amazon Simple Notification Service (Amazon SNS) notification to the compliance team" is incorrect.
AWS Security Hub gives a comprehensive view of high-priority security alerts and compliance status, but it does not offer data-specific detection like PHI in S3 objects.
INCORRECT: "Use Amazon Macie. Create an AWS Lambda function to filter the ‘SensitiveData:S3Object/Personal’ event type from Macie findings and trigger an Amazon Simple Notification Service (Amazon SNS) notification to the compliance team".
INCORRECT: "Use AWS Security Hub. Create an AWS Lambda function to filter the ‘Security Hub findings - High severity’ event type and trigger an Amazon Simple Email Service (Amazon SES) notification to the compliance team" is incorrect.
AWS Security Hub does not offer detection of specific data types like PHI in S3 objects. Therefore, using it for this purpose would not meet the requirements.
References:
https://docs.aws.amazon.com/macie/latest/user/findings-types.html
Domain
AWS Networking & Content Delivery
Question 58Skipped
A multinational podcast company uses Amazon CloudFront for distributing its digital content. The company wants to gradually introduce content across various regions. It also needs to ensure that listeners who are outside the regions to which the content is currently released, cannot access the content.
Which solution will meet these requirements?
Encrypt the company's distributed content data and establish a custom error message.
Establish a new URL for the restricted content, control access with signed URLs and cookies, and set up a custom error message.
Create a new URL for the restricted content and establish an expiration date-based access policy for signed URLs.
Correct answer
Implement geographical restrictions on CloudFront content using a deny list and create a custom error message.
Overall explanation
By setting geographical restrictions on CloudFront content using a deny list, the company can block access to content for users outside of the released regions. If a user from a blocked region attempts to access the content, they would receive the custom error message, thereby meeting the company's requirements.
CORRECT: "Implement geographical restrictions on CloudFront content using a deny list and create a custom error message" is the correct answer (as explained above.)
INCORRECT: "Establish a new URL for the restricted content, control access with signed URLs and cookies, and set up a custom error message" is incorrect.
While signed URLs and cookies can be used to control access to content, they don't inherently consider the geographical location of the users, thus it would not guarantee that only users in the released regions could access the content.
INCORRECT: "Encrypt the company's distributed content data and establish a custom error message" is incorrect.
Although encrypting the content data adds a layer of security, it does not restrict access based on the geographical location of the users.
INCORRECT: "Create a new URL for the restricted content and establish an expiration date-based access policy for signed URLs" is incorrect.
Time-based access policies with signed URLs can limit access to the content after a certain time, but it does not restrict access based on the geographical location of the users.
References:
https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudfront/
Domain
AWS Networking & Content Delivery
Question 59Skipped
As a security measure, a finance-based organization want to introduce additional security measures for an existing application deployed in AWS. The application is serverless and has an Amazon API Gateway in front which is deployed in the us-east-1 Region and the eu-west-1 Region. The company requires the accounts to be secured against SQL injection and cross-site scripting attacks.
Which solution will meet these requirements with the LEAST amount of administrative effort?
Correct answer
Set up AWS Firewall Manager in both Regions. Centrally configure AWS WAF rules.
Set up AWS WAF in both Regions. Associate Regional web ACLs with an API stage
Set up AWS Shield in one of the Regions. Associate Regional web ACLs with an API stage.
Set up AWS Shield in both Regions. Associate Regional web ACLs with an API stage.
Overall explanation
AWS Firewall Manager simplifies your administration and maintenance tasks across multiple accounts and resources for a variety of protections, including AWS WAF, AWS Shield Advanced, Amazon VPC security groups, AWS Network Firewall, and Amazon Route 53 Resolver DNS Firewall. With Firewall Manager, you set up your protections just once and the service automatically applies them across your accounts and resources, even as you add new accounts and resources.
AWS WAF is used for protecting against malicious web attacks and is the best service to use to protect against SQL injection and cross-site scripting attacks. Used in combination with AWS Firewall Manager this solution protects both Regions and requires the least administrative effort.
CORRECT: "Set up AWS Firewall Manager in both Regions. Centrally configure AWS WAF rules" is the correct answer (as explained above.)
INCORRECT: "Set up AWS WAF in both Regions. Associate Regional web ACLs with an API stage" is incorrect. This solution requires more administrative effort in rule management.
INCORRECT: "Set up AWS Shield in both Regions. Associate Regional web ACLs with an API stage" is incorrect. The primary difference between AWS Shield and WAF is that while AWS WAF can mitigate DDoS attacks at layer 7 of the OSI reference model, AWS Shield protects web services from DDoS attacks at layer 3 and 4 of the OSI reference model. In this case AWS WAF should be used.
INCORRECT: "Set up AWS Shield in one of the Regions. Associate Regional web ACLs with an API stage" is incorrect. As mentioned above, AWS Shield is not an appropriate choice for securing the accounts from SQL injection and cross-site scripting attacks.
References:
https://docs.aws.amazon.com/waf/latest/developerguide/fms-chapter.html
https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-waf-shield/
Domain
AWS Networking & Content Delivery
Question 61Skipped
A finance organization wants to deploy end of day processing applications to a fleet of Amazon EC2 instances with a focus on reducing cost. These applications are stateless and can be re-triggered in case of failure. The company needs a solution that minimizes cost and operational overhead.
What should a solutions architect do to meet these requirements?
Correct answer
Use Spot Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.
Use On-Demand Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.
Use On-Demand Instances in an Amazon EC2 Auto Scaling group to run the application containers.
Use Spot Instances in an Amazon EC2 Auto Scaling group to run the application containers.
Overall explanation
Since by using EC2 Spot Instances, customers can access additional compute capacity between 70%-90% off On-Demand Instance pricing, we can directly eliminate two options utilizing on demand instances.
Among the two options with spot instances, since the application is stateless, the better idea is to have a containerized approach and utilize EKS to reduce operational overhead.
CORRECT: "Use Spot Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group" is the correct answer (as explained above.)
INCORRECT: "Use Spot Instances in an Amazon EC2 Auto Scaling group to run the application containers" is incorrect. As mentioned above, EKS gives you more options towards application fleet orchestration which makes it a better choice.
INCORRECT: "Use On-Demand Instances in an Amazon EC2 Auto Scaling group to run the application containers" is incorrect.
As compared to spot instances, on demand instances are costlier and for end of day processing where failures can be re-triggered and are acceptable, spot instances are a better choice.
INCORRECT: "Use On-Demand Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group" is incorrect.
As compared to spot instances, on demand instances are more expensive and for end of day processing where failures can be re-triggered and are acceptable, spot instances are a better choice.
References:
https://aws.amazon.com/blogs/compute/best-practices-for-handling-ec2-spot-instance-interruptions/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ecs-and-eks/
Domain
AWS Networking & Content Delivery
Question 65Skipped
A company have 500 TB of data in an on-premises file share that needs to be moved to Amazon S3 Glacier. The migration must not saturate the company’s low-bandwidth internet connection and the migration must be completed within a few weeks.
What is the MOST cost-effective solution?
Create an AWS Direct Connect connection and migrate the data straight into Amazon Glacier
Correct answer
Order 7 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier
Use AWS Global Accelerator to accelerate upload and optimize usage of the available bandwidth
Order 7 AWS Snowball appliances and select an S3 Glacier vault as the destination. Create a bucket policy to enforce a VPC endpoint
Overall explanation
As the company’s internet link is low-bandwidth uploading directly to Amazon S3 (ready for transition to Glacier) would saturate the link. The best alternative is to use AWS Snowball appliances. The Snowball edge appliance can hold up to 80 TB of data so 7 devices would be required to migrate 500 TB of data.
Snowball moves data into AWS using a hardware device and the data is then copied into an Amazon S3 bucket of your choice. From there, lifecycle policies can transition the S3 objects to Amazon S3 Glacier.
CORRECT: "Order 7 AWS Snowball appliances and select an Amazon S3 bucket as the destination. Create a lifecycle policy to transition the S3 objects to Amazon S3 Glacier" is the correct answer.
INCORRECT: "Order 7 AWS Snowball appliances and select an S3 Glacier vault as the destination. Create a bucket policy to enforce a VPC endpoint" is incorrect as you cannot set a Glacier vault as the destination, it must be an S3 bucket. You also can’t enforce a VPC endpoint using a bucket policy.
INCORRECT: "Create an AWS Direct Connect connection and migrate the data straight into Amazon Glacier" is incorrect as this is not the most cost-effective option and takes time to setup.
INCORRECT: "Use AWS Global Accelerator to accelerate upload and optimize usage of the available bandwidth" is incorrect as this service is not used for accelerating or optimizing the upload of data from on-premises networks.
References:
https://docs.aws.amazon.com/snowball/latest/developer-guide/specifications.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-s3-and-glacier/
Domain
AWS Networking & Content Delivery
Question 7Skipped
A multinational organization has a distributed application that runs on Amazon EC2 instances, which are behind an Application Load Balancer in an Auto Scaling group. The application utilizes a MySQL database hosted on Amazon Aurora. The database cluster spans across multiple Availability Zones in a single region.
The organization plans to launch its services in a new geographical area and wants to ensure maximum availability with minimal service interruption.
Which strategy should the organization adopt?
Expand the existing Auto Scaling group into the new Region. Utilize Amazon Aurora Global Database to extend the database across the primary and new regions. Implement Amazon Route 53 health checks with a failover routing policy directed towards the new region.
Correct answer
Establish the application layer in the new region. Use Amazon Aurora Global Database for deploying the database in the primary and new regions. Apply Amazon Route 53 health checks with a failover routing policy to the new region. Promote the secondary to primary as needed.
Create a similar application layer in the new region. Establish a new Aurora MySQL database in this region. Use AWS Database Migration Service (AWS DMS) for ongoing replication from the primary database to the new region. Implement Amazon Route 53 health checks with a failover routing policy to the new region.
Replicate the application layer in the new region. Implement an Aurora MySQL Read Replica in the new region using Route 53 health checks and a failover routing policy. In case of primary failure, promote the Read Replica to primary.
Overall explanation
This solution involves creating an application layer in the new region and using Amazon Aurora Global Database, which supports replicating your databases across multiple regions with minimal impact on performance.
This configuration can enhance disaster recovery capabilities and can reduce the impact of planned maintenance. Amazon Route 53 health checks with a failover routing policy can automatically route traffic to the new region in the event of a failure in the primary region, thereby ensuring high availability.
With an Aurora global database, there are two different approaches to failover depending on the scenario. You can use manual unplanned failover (detach and promote) or managed planned failover.
CORRECT: "Establish the application layer in the new region. Use Amazon Aurora Global Database for deploying the database in the primary and new regions. Apply Amazon Route 53 health checks with a failover routing policy to the new region. Perform a manual failover as required" is the correct answer (as explained above.)
INCORRECT: "Replicate the application layer in the new region. Implement an Aurora MySQL Read Replica in the new region using Route 53 health checks and a failover routing policy. In case of primary failure, promote the Read Replica to primary" is incorrect.
This solution involves creating a Read Replica in the new region, which would indeed allow for the promotion of the Read Replica to a primary instance if necessary. However, this process isn't instantaneous and could lead to service interruption, which is not what the question asked for. Aurora Global Database provides a lower RTO/RPO.
INCORRECT: "Create a similar application layer in the new region. Establish a new Aurora MySQL database in this region. Use AWS Database Migration Service (AWS DMS) for ongoing replication from the primary database to the new region. Implement Amazon Route 53 health checks with a failover routing policy to the new region" is incorrect.
AWS Database Migration Service (AWS DMS) is primarily used for migrating databases to AWS from on-premises environments or for replicating databases for data warehousing and other use cases. It isn't as suitable for ongoing high-availability or failover scenarios as Amazon Aurora Global Database, which is specifically designed for these situations.
INCORRECT: "Expand the existing Auto Scaling group into the new Region. Utilize Amazon Aurora Global Database to extend the database across the primary and new regions. Implement Amazon Route 53 health checks with a failover routing policy directed towards the new region" is incorrect.
It is not possible to expand an Auto Scaling group across multiple Regions. ASGs operate within a Region only.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database-disaster-recovery.html#aurora-global-database-failover
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Networking & Content Delivery
Question 15Skipped
A digital media company uses an Amazon RDS MySQL instance for its content management system. Recently, the company has observed that their RDS instance is nearing its storage capacity due to the constant influx of new data. The company wants to ensure there's always sufficient storage without any operational interruption or manual intervention.
Which solution should the company use to address this situation with the LEAST operational overhead?
Migrate the database to a larger Amazon RDS MySQL instance.
Utilize Amazon ElastiCache to offload some read traffic and reduce database load.
Implement a lifecycle policy to delete older data from the MySQL instance.
Correct answer
Enable automatic storage scaling for the MySQL instance.
Overall explanation
Amazon RDS's automatic storage scaling allows the database to automatically increase its storage capacity when the available storage is low. This feature helps to prevent out-of-storage situations and requires no operational overhead.
CORRECT: "Enable automatic storage scaling for the MySQL instance" is the correct answer (as explained above.)
INCORRECT: "Migrate the database to a larger Amazon RDS MySQL instance" is incorrect.
While this would provide more storage, it does not address the issue of potential future storage shortages and requires significant operational effort for the migration.
INCORRECT: "Implement a lifecycle policy to delete older data from the MySQL instance" is incorrect.
While this might help free up some storage, it might not be suitable if all data is essential for business operations. Also, this does not provide a long-term solution if data growth continues.
INCORRECT: "Utilize Amazon ElastiCache to offload some read traffic and reduce database load" is incorrect.
While ElastiCache can help to improve the database's read efficiency, it doesn't directly address the disk space concern for the RDS instance.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PIOPS.StorageTypes.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
Domain
AWS Networking & Content Delivery
Question 26Skipped
A tool needs to analyze data stored in an Amazon S3 bucket. Processing the data takes a few seconds and results are then written to another S3 bucket. Less than 256 MB of memory is needed to run the process. What would be the MOST cost-effective compute solutions for this use case?
Correct answer
AWS Lambda functions
Amazon Elastic Beanstalk
Amazon EC2 spot instances
AWS Fargate tasks
Overall explanation
AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume. Lambda has a maximum execution time of 900 seconds and memory can be allocated up to 3008 MB. Therefore, the most cost-effective solution will be AWS Lambda.
CORRECT: "AWS Lambda functions" is the correct answer.
INCORRECT: "AWS Fargate tasks" is incorrect. Fargate runs Docker containers and is serverless. However, you do pay for the running time of the tasks so it will not be as cost-effective.
INCORRECT: "Amazon EC2 spot instances" is incorrect. EC2 instances must run continually waiting for jobs to process so even with spot this would be less cost-effective (and subject to termination).
INCORRECT: "Amazon Elastic Beanstalk" is incorrect. This services also relies on Amazon EC2 instances so would not be as cost-effective.
References:
https://aws.amazon.com/lambda/
Save time with our AWS cheat sheets:
https://digitalcloud.training/aws-lambda/
Domain
AWS Networking & Content Delivery
Question 29Skipped
An e-commerce web application needs a highly scalable key-value database. Which AWS database service should be used?
Amazon RDS
Amazon ElastiCache
Correct answer
Amazon DynamoDB
Amazon RedShift
Overall explanation
A key-value database is a type of nonrelational (NoSQL) database that uses a simple key-value method to store data. A key-value database stores data as a collection of key-value pairs in which a key serves as a unique identifier. Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability – this is the best database for these requirements.
CORRECT: "Amazon DynamoDB" is the correct answer.
INCORRECT: "Amazon RDS" is incorrect. Amazon RDS is a relational (SQL) type of database, not a key-value / nonrelational database.
INCORRECT: "Amazon RedShift" is incorrect. Amazon RedShift is a data warehouse service used for online analytics processing (OLAP) workloads.
INCORRECT: "Amazon ElastiCache" is incorrect. Amazon ElastiCache is an in-memory caching database. This is not a nonrelational key-value database.
References:
https://aws.amazon.com/nosql/key-value/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-dynamodb/
Domain
AWS Networking & Content Delivery
Question 31Skipped
A web application in a three-tier architecture runs on a fleet of Amazon EC2 instances. Performance issues have been reported and investigations point to insufficient swap space. The operations team requires monitoring to determine if this is correct.
What should a solutions architect recommend?
Enable detailed monitoring in the EC2 console. Create an Amazon CloudWatch SwapUtilization custom metric. Monitor SwapUtilization metrics in CloudWatch
Correct answer
Install an Amazon CloudWatch agent on the instances. Run an appropriate script on a set schedule. Monitor SwapUtilization metrics in CloudWatch
Configure an Amazon CloudWatch SwapUsage metric dimension. Monitor the SwapUsage dimension in the EC2 metrics in CloudWatch
Use EC2 metadata to collect information, then publish it to Amazon CloudWatch custom metrics. Monitor SwapUsage metrics in CloudWatch
Overall explanation
You can use the CloudWatch agent to collect both system metrics and log files from Amazon EC2 instances and on-premises servers. The agent supports both Windows Server and Linux, and enables you to select the metrics to be collected, including sub-resource metrics such as per-CPU core.
There is now a unified agent and previously there were monitoring scripts. Both of these tools can capture SwapUtilization metrics and send them to CloudWatch. This is the best way to get memory utilization metrics from Amazon EC2 instnaces.
CORRECT: "Install an Amazon CloudWatch agent on the instances. Run an appropriate script on a set schedule. Monitor SwapUtilization metrics in CloudWatch" is the correct answer.
INCORRECT: "Enable detailed monitoring in the EC2 console. Create an Amazon CloudWatch SwapUtilization custom metric. Monitor SwapUtilization metrics in CloudWatch" is incorrect as you do not create custom metrics in the console, you must configure the instances to send the metric information to CloudWatch.
INCORRECT: "Configure an Amazon CloudWatch SwapUsage metric dimension. Monitor the SwapUsage dimension in the EC2 metrics in CloudWatch" is incorrect as there is no SwapUsage metric in CloudWatch. All memory metrics must be custom metrics.
INCORRECT: "Use EC2 metadata to collect information, then publish it to Amazon CloudWatch custom metrics. Monitor SwapUsage metrics in CloudWatch" is incorrect as performance related information is not stored in metadata.
References:
https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-cloudwatch/
Domain
AWS Networking & Content Delivery
Question 40Skipped
The database layer of an on-premises web application is being migrated to AWS. The database currently uses an in-memory cache. A Solutions Architect must deliver a solution that supports high availability and replication for the caching layer.
Which service should the Solutions Architect recommend?
Amazon RDS Multi-AZ
Correct answer
Amazon ElastiCache Redis
Amazon DynamoDB
Amazon ElastiCache Memcached
Overall explanation
Amazon ElastiCache Redis is an in-memory database cache and supports high availability through replicas and multi-AZ. The table below compares ElastiCache Redis with Memcached:


CORRECT: "Amazon ElastiCache Redis" is the correct answer.
INCORRECT: "Amazon ElastiCache Memcached" is incorrect as it does not support high availability or multi-AZ.
INCORRECT: "Amazon RDS Multi-AZ" is incorrect. This is not an in-memory database and it not suitable for use as a caching layer.
INCORRECT: "Amazon DynamoDB" is incorrect. DynamoDB is a non-relational database. You would not use it for a caching layer. Also, the in-memory, low-latency caching for DynamoDB is implemented using DynamoDB Accelerator (DAX).
References:
https://aws.amazon.com/elasticache/redis-vs-memcached/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-elasticache/
Domain
AWS Networking & Content Delivery
Question 50Skipped
A company needs to ensure that they can failover between AWS Regions in the event of a disaster seamlessly with minimal downtime and data loss. The applications will run in an active-active configuration.
Which DR strategy should a Solutions Architect recommend?
Pilot light
Warm standby
Correct answer
Multi-site
Backup and restore
Overall explanation
A multi-site solution runs on AWS as well as on your existing on-site infrastructure in an active- active configuration. The data replication method that you employ will be determined by the recovery point that you choose. This is either Recovery Time Objective (the maximum allowable downtime before degraded operations are restored) or Recovery Point Objective (the maximum allowable time window whereby you will accept the loss of transactions during the DR process).
CORRECT: "Multi-site" is the correct answer.
INCORRECT: "Backup and restore" is incorrect. This is the lowest cost DR approach that simply entails creating online backups of all data and applications.
INCORRECT: "Pilot light" is incorrect. With a pilot light strategy a core minimum of services are running and the remainder are only brought online during a disaster recovery situation.
INCORRECT: "Warm standby" is incorrect. The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud.
References:
https://aws.amazon.com/blogs/publicsector/rapidly-recover-mission-critical-systems-in-a-disaster/
Domain
AWS Networking & Content Delivery
Question 52Skipped
A company is creating a solution that must offer disaster recovery across multiple AWS Regions. The solution requires relational a database that can support a Recovery Point Objective (RPO) of 1 second and a Recovery Time Objective (RTO) of 1 minute.
Which AWS solution can achieve this?
Amazon RDS for with a cross-Region replica.
Amazon DynamoDB global tables.
Amazon RDS for with Multi-AZ enabled.
Correct answer
Amazon Aurora Global Database.
Overall explanation
Aurora Global Database lets you easily scale database reads across the world and place your applications close to your users. Your applications enjoy quick data access regardless of the number and location of secondary regions, with typical cross-region replication latencies below 1 second.
If your primary region suffers a performance degradation or outage, you can promote one of the secondary regions to take read/write responsibilities. An Aurora cluster can recover in less than 1 minute even in the event of a complete regional outage. This provides your application with an effective Recovery Point Objective (RPO) of 1 second and a Recovery Time Objective (RTO) of less than 1 minute, providing a strong foundation for a global business continuity plan.
CORRECT: "Amazon Aurora Global Database" is the correct answer.
INCORRECT: "Amazon RDS for with Multi-AZ enabled" is incorrect. RDS Multi-AZ is across availability zones, not across Regions.
INCORRECT: "Amazon RDS for with a cross-Region replica" is incorrect. A cross-Region replica for RDS cannot provide an RPO of 1 second as there is typically more latency. You also cannot achieve a minute RPO as it takes much longer to promote a replica to a master.
INCORRECT: "Amazon DynamoDB global tables" is incorrect. This is not a relational database; it is a non-relational database (NoSQL).
References:
https://aws.amazon.com/rds/aurora/global-database/
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-aurora/
Domain
AWS Networking & Content Delivery
Question 54Skipped
A company has launched a multi-tier application architecture. The web tier and database tier run on Amazon EC2 instances in private subnets within the same Availability Zone.
Which combination of steps should a Solutions Architect take to add high availability to this architecture? (Select TWO.)
Add the existing web application instances to an Auto Scaling group behind an Application Load Balancer (ALB)
Create new private subnets in the same VPC but in a different AZ. Create a database using Amazon EC2 in one AZ
Correct selection
Create new private subnets in the same VPC but in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment
Correct selection
Create an Amazon EC2 Auto Scaling group and Application Load Balancer (ALB) spanning multiple AZs
Create new public subnets in the same AZ for high availability and move the web tier to the public subnets
Overall explanation
The Solutions Architect can use Auto Scaling group across multiple AZs with an ALB in front to create an elastic and highly available architecture. Then, migrate the database to an Amazon RDS multi-AZ deployment to create HA for the database tier. This results in a fully redundant architecture that can withstand the failure of an availability zone.
CORRECT: "Create an Amazon EC2 Auto Scaling group and Application Load Balancer (ALB) spanning multiple AZs" is a correct answer.
CORRECT: "Create new private subnets in the same VPC but in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment" is also a correct answer.
INCORRECT: "Create new public subnets in the same AZ for high availability and move the web tier to the public subnets" is incorrect. If subnets share the same AZ they are not suitable for splitting your tier across them for HA as the failure of a an AZ will take out both subnets.
INCORRECT: "Add the existing web application instances to an Auto Scaling group behind an Application Load Balancer (ALB)" is incorrect. The instances are in a single AZ so the Solutions Architect should create a new auto scaling group and launch instances across multiple AZs.
INCORRECT: "Create new private subnets in the same VPC but in a different AZ. Create a database using Amazon EC2 in one AZ" is incorrect. A database in a single AZ will not be highly available.
References:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-increase-availability.html
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2/
https://digitalcloud.training/amazon-rds/
Domain
AWS Networking & Content Delivery
Question 56Skipped
A financial services company is migrating its sensitive customer data and applications to AWS. They want to ensure that the data is securely stored and managed while reducing the overall maintenance and operational overhead associated with managing databases.
Which solution will meet these requirements?
Store the data in Amazon S3. Utilize Amazon Macie for ongoing data security and threat detection.
Correct answer
Migrate the data and applications to Amazon RDS instances. Enable encryption at rest using AWS Key Management Service (AWS KMS).
Migrate the data to Amazon RDS instances. Enable Amazon GuardDuty for data protection and threat detection.
Migrate the applications and data to Amazon EC2 instances. Utilize the AWS Key Management Service (AWS KMS) customer managed keys for encryption.
Overall explanation
Amazon RDS makes it easy to go from project conception to deployment by managing time-consuming database administration tasks including backups, software patching, monitoring, scaling, and replication.
Amazon RDS supports encryption at rest, which ensures the security of sensitive data and meets regulatory compliance requirements. AWS Key Management Service (AWS KMS) is integrated with Amazon RDS to make it easier to create, control, and manage keys for encryption.
CORRECT: "Migrate the data and applications to Amazon RDS instances. Enable encryption at rest using AWS Key Management Service (AWS KMS)" is the correct answer (as explained above.)
INCORRECT: "Migrate the applications and data to Amazon EC2 instances. Utilize the AWS Key Management Service (AWS KMS) customer managed keys for encryption" is incorrect.
While this solution offers data encryption, it does not meet the requirement to reduce operational overhead. Managing databases on EC2 instances requires additional administrative tasks, such as managing backups and applying software patches, which Amazon RDS handles automatically.
INCORRECT: "Store the data in Amazon S3. Utilize Amazon Macie for ongoing data security and threat detection" is incorrect.
Amazon S3 and Macie are suitable for data storage and security analysis, respectively. However, Amazon S3 is not designed to serve as a transactional database for applications, which is a key requirement in this scenario.
INCORRECT: "Migrate the data to Amazon RDS instances. Enable Amazon GuardDuty for data protection and threat detection" is incorrect.
While Amazon RDS is a correct choice for database management and Amazon GuardDuty offers threat detection, GuardDuty is not specifically designed for data protection within databases. It's a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts and workloads.
References:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-rds/
https://digitalcloud.training/aws-kms/
Domain
AWS Networking & Content Delivery
Question 59Skipped
A company runs a financial application using an Amazon EC2 Auto Scaling group behind an Application Load Balancer (ALB). When running month-end reports on a specific day and time each month the application becomes unacceptably slow. Amazon CloudWatch metrics show the CPU utilization hitting 100%.
What should a solutions architect recommend to ensure the application is able to handle the workload and avoid downtime?
Correct answer
Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule
Configure Amazon ElastiCache to remove some of the workload from the EC2 instances
Configure an Amazon CloudFront distribution in front of the ALB
Configure an EC2 Auto Scaling simple scaling policy based on CPU utilization
Overall explanation
Scheduled scaling allows you to set your own scaling schedule. In this case the scaling action can be scheduled to occur just prior to the time that the reports will be run each month. Scaling actions are performed automatically as a function of time and date. This will ensure that there are enough EC2 instances to serve the demand and prevent the application from slowing down.
CORRECT: "Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule" is the correct answer.
INCORRECT: "Configure an Amazon CloudFront distribution in front of the ALB" is incorrect as this would be more suitable for providing access to global users by caching content.
INCORRECT: "Configure an EC2 Auto Scaling simple scaling policy based on CPU utilization" is incorrect as this would not prevent the slow-down from occurring as there would be a delay between when the CPU hits 100% and the metric being reported and additional instances being launched.
INCORRECT: "Configure Amazon ElastiCache to remove some of the workload from the EC2 instances" is incorrect as ElastiCache is a database cache, it cannot replace the compute functions of an EC2 instance.
References:
https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html
Save time with our AWS cheat sheets:
https://digitalcloud.training/amazon-ec2-auto-scaling/
Domain
AWS Networking & Content Delivery
Question 64Skipped
An e-commerce company operates a serverless web application that must interact with numerous Amazon DynamoDB tables to fulfill user requests. It is critical that the application's performance remains consistent and unaffected while interacting with these tables.
Which method provides the MOST operationally efficient way to fulfill these requirements?
AWS Glue with a DynamoDB connector.
Correct answer
AWS AppSync with multiple data sources and resolvers.
AWS Lambda with Step Functions.
Amazon S3 with Lambda triggers.
Overall explanation
AWS AppSync simplifies application development by letting you create a flexible API to securely access, manipulate, and combine data from one or more data sources. AppSync is a managed service that uses GraphQL to make it easy for applications to get exactly the data they need, including from multiple DynamoDB tables.
AWS AppSync is designed for real-time and offline data access which makes it an ideal solution for this scenario.
CORRECT: "AWS AppSync with multiple data sources and resolvers" is the correct answer (as explained above.)
INCORRECT: "AWS Lambda with Step Functions" is incorrect.
AWS Step Functions make it easy to coordinate the components of distributed applications and microservices using visual workflows. However, while you could theoretically build a flow to retrieve data from multiple tables, it's not the most efficient solution as it introduces additional complexity and potential latency.
INCORRECT: "Amazon S3 with Lambda triggers" is incorrect.
While you can use AWS Lambda to execute code in response to triggers like changes to data in an Amazon S3 bucket, this doesn't directly allow the application to retrieve data from multiple DynamoDB tables. This approach would also involve unnecessary data transfers and added latency.
INCORRECT: "AWS Glue with a DynamoDB connector" is incorrect.
AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy to prepare and load your data for analytics. However, AWS Glue isn't meant for real-time data retrieval in an application. Using it for real-time data retrieval would likely be overcomplicated and inefficient.
References:
https://aws.amazon.com/appsync/product-details/
