# AWS SAA-C03 Practice Questions - Part 3

Total Questions: 206

---

## Question 1

**Q:** A Solutions Architect is designing a migration strategy for a company moving to the AWS Cloud. The company use a shared Microsoft filesystem that uses Distributed File System Namespaces (DFSN). What will be the MOST suitable migration strategy for the filesystem?

**Options:**
- (A) Use the AWS Server Migration Service to migrate to an Amazon S3 bucket
- (B) Use AWS DataSync to migrate to Amazon FSx for Windows File Server
- (C) Use AWS DataSync to migrate to an Amazon EFS filesystem
- (D) Use the AWS Server Migration Service to migrate to Amazon FSx for Lustre
- (E) The destination filesystem should be Amazon FSx for Windows File Server. This supports DFSN and is the most suitable storage solution for Microsoft filesystems. AWS DataSync supports migrating to the Amazon FSx and automates the process.
- (F)  is the correct answer.
- (G)  is incorrect. The server migration service is used to migrate virtual machines and FSx for Lustre does not support Windows filesystems.
- (H)  is incorrect. You can migrate data to EFS using DataSync but it is the wrong destination for a Microsoft filesystem (Linux only).
- (I)  is incorrect. The server migration service is used to migrate virtual machines and Amazon S3 is an object-based storage system and unsuitable for hosting a Microsoft filesystem.
- (J) References:
- () https://aws.amazon.com/blogs/storage/migrate-to-amazon-fsx-for-windows-file-server-using-aws-datasync/
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/migrate-files-fsx.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-fsx/
- () AWS Migration & Transfer
- () An organization is planning their disaster recovery solution. They plan to run a scaled down version of a fully functional environment. In a DR situation the recovery time must be minimized.
- () Which DR strategy should a Solutions Architect recommend?
- () Multi-site
- () Warm standby
- () Pilot light
- () Backup and restore
- () The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud. A warm standby solution extends the pilot light elements and preparation.
- () It further decreases the recovery time because some services are always running. By identifying your business-critical systems, you can fully duplicate these systems on AWS and have them always on.
- ()  is incorrect. This is the lowest cost DR approach that simply entails creating online backups of all data and applications.
- ()  is incorrect. With a pilot light strategy a core minimum of services are running and the remainder are only brought online during a disaster recovery situation.
- ()  is incorrect. A multi-site solution runs on AWS as well as on your existing on-site infrastructure in an active- active configuration.
- () https://aws.amazon.com/blogs/publicsector/rapidly-recover-mission-critical-systems-in-a-disaster/
- () AWS Cloud Architecture & Design
- () An e-commerce company operates a containerized microservices application on a fleet of Amazon EC2 instances. As part of their infrastructure improvement efforts, the company plans to migrate the application to Amazon Elastic Kubernetes Service (Amazon EKS) for enhanced scalability and management.
- () As part of the security protocol, the company has configured the Amazon EKS control plane with endpoint private access enabled and public access disabled. The data plane resides within private subnets. However, the company faces an issue where nodes fail to join the cluster.
- () What can be done to allow the nodes to join the EKS cluster?
- () Move nodes to public subnet and configure security group rules for the EC2 nodes.
- () Modify the associated IAM role to include permissions to the AmazonEKSClusterPolicy.
- () Establish VPC peering connection for nodes to access the control plane.
- **() Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.** [CORRECT]
- () When the EKS control plane is configured with private access, and the nodes are in a private subnet, you need to create VPC endpoints for Amazon EKS and ECR. This allows the nodes to communicate with the EKS control plane and pull container images from ECR.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () IAM roles are crucial for setting up permissions, but simply modifying the associated IAM role would not solve the issue of nodes not being able to connect to the control plane.
- () VPC peering is not the recommended way to allow nodes in a private subnet to access the EKS control plane. This approach might also incur additional operational overhead.
- () Moving the nodes to public subnets contradicts the original requirement of having the data plane in private subnets. Additionally, this approach might introduce unnecessary security risks.
- () https://docs.aws.amazon.com/eks/latest/userguide/private-clusters.html
- () https://digitalcloud.training/amazon-ecs-and-eks/

**Answer:**
Correct Answer: **Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.**

---

## Question 2

**Q:** Which DR strategy should a Solutions Architect recommend?

**Options:**
- (A) Multi-site
- (B) Warm standby
- (C) Pilot light
- (D) Backup and restore
- (E) The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud. A warm standby solution extends the pilot light elements and preparation.
- (F) It further decreases the recovery time because some services are always running. By identifying your business-critical systems, you can fully duplicate these systems on AWS and have them always on.
- (G)  is the correct answer.
- (H)  is incorrect. This is the lowest cost DR approach that simply entails creating online backups of all data and applications.
- (I)  is incorrect. With a pilot light strategy a core minimum of services are running and the remainder are only brought online during a disaster recovery situation.
- (J)  is incorrect. A multi-site solution runs on AWS as well as on your existing on-site infrastructure in an active- active configuration.
- () References:
- () https://aws.amazon.com/blogs/publicsector/rapidly-recover-mission-critical-systems-in-a-disaster/
- () AWS Cloud Architecture & Design
- () An e-commerce company operates a containerized microservices application on a fleet of Amazon EC2 instances. As part of their infrastructure improvement efforts, the company plans to migrate the application to Amazon Elastic Kubernetes Service (Amazon EKS) for enhanced scalability and management.
- () As part of the security protocol, the company has configured the Amazon EKS control plane with endpoint private access enabled and public access disabled. The data plane resides within private subnets. However, the company faces an issue where nodes fail to join the cluster.
- () What can be done to allow the nodes to join the EKS cluster?
- () Move nodes to public subnet and configure security group rules for the EC2 nodes.
- () Modify the associated IAM role to include permissions to the AmazonEKSClusterPolicy.
- () Establish VPC peering connection for nodes to access the control plane.
- **() Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.** [CORRECT]
- () When the EKS control plane is configured with private access, and the nodes are in a private subnet, you need to create VPC endpoints for Amazon EKS and ECR. This allows the nodes to communicate with the EKS control plane and pull container images from ECR.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () IAM roles are crucial for setting up permissions, but simply modifying the associated IAM role would not solve the issue of nodes not being able to connect to the control plane.
- () VPC peering is not the recommended way to allow nodes in a private subnet to access the EKS control plane. This approach might also incur additional operational overhead.
- () Moving the nodes to public subnets contradicts the original requirement of having the data plane in private subnets. Additionally, this approach might introduce unnecessary security risks.
- () https://docs.aws.amazon.com/eks/latest/userguide/private-clusters.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Compute
- () A game development company is planning to build a cloud-based game platform on AWS. The player activity patterns are unpredictable and could remain idle for extended periods. Only players who have purchased the game should have the ability to log in and play.
- () Which combination of steps will meet these requirements MOST cost-effectively? (Select THREE.)
- () Correct selection
- () Use AWS Cognito User Pools to handle user authentication.
- () Use AWS Cognito Identity Pools to handle user authentication.
- () Implement an AWS Lambda function to fetch player information from Amazon DynamoDB. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the Lambda function.
- () Use Amazon S3 static web hosting with HTML, CSS, and JS. Use Amazon CloudFront to distribute the frontend game interface.
- () Set up an Amazon Elastic Container Service (Amazon ECS) service behind an Application Load Balancer to fetch player information from Amazon RDS. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the ECS service.
- () Leverage AWS Amplify to serve the frontend game interface with HTML, CSS, and JS. Use the integrated Amazon CloudFront configuration for distribution.
- () AWS Lambda is a cost-effective solution for unpredictable traffic patterns due to its pay-per-use pricing model. DynamoDB is also a cost-effective and highly scalable solution for storing user data. The API Gateway provides a HTTP-based endpoint that can be used to expose the Lambda function.
- () AWS Cognito User Pools provide user directory features including sign-up and sign-in services, which are suitable for managing game user authentication.
- () AWS Amplify simplifies the process of hosting web applications with automated deployment processes. It also integrates with CloudFront, providing a global content delivery network to efficiently serve the game interface.
- ()  is a correct answer (as explained above.)
- ()  is also a correct answer (as explained above.)

**Answer:**
Correct Answer: **Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.**

---

## Question 3

**Q:** What can be done to allow the nodes to join the EKS cluster?

**Options:**
- (A) Move nodes to public subnet and configure security group rules for the EC2 nodes.
- (B) Modify the associated IAM role to include permissions to the AmazonEKSClusterPolicy.
- (C) Establish VPC peering connection for nodes to access the control plane.
- **(D) Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.** [CORRECT]
- (E) When the EKS control plane is configured with private access, and the nodes are in a private subnet, you need to create VPC endpoints for Amazon EKS and ECR. This allows the nodes to communicate with the EKS control plane and pull container images from ECR.
- (F)  is the correct answer (as explained above.)
- (G)  is incorrect.
- (H) IAM roles are crucial for setting up permissions, but simply modifying the associated IAM role would not solve the issue of nodes not being able to connect to the control plane.
- (I) VPC peering is not the recommended way to allow nodes in a private subnet to access the EKS control plane. This approach might also incur additional operational overhead.
- (J) Moving the nodes to public subnets contradicts the original requirement of having the data plane in private subnets. Additionally, this approach might introduce unnecessary security risks.
- () References:
- () https://docs.aws.amazon.com/eks/latest/userguide/private-clusters.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Compute
- () A game development company is planning to build a cloud-based game platform on AWS. The player activity patterns are unpredictable and could remain idle for extended periods. Only players who have purchased the game should have the ability to log in and play.
- () Which combination of steps will meet these requirements MOST cost-effectively? (Select THREE.)
- () Correct selection
- () Use AWS Cognito User Pools to handle user authentication.
- () Use AWS Cognito Identity Pools to handle user authentication.
- () Implement an AWS Lambda function to fetch player information from Amazon DynamoDB. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the Lambda function.
- () Use Amazon S3 static web hosting with HTML, CSS, and JS. Use Amazon CloudFront to distribute the frontend game interface.
- () Set up an Amazon Elastic Container Service (Amazon ECS) service behind an Application Load Balancer to fetch player information from Amazon RDS. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the ECS service.
- () Leverage AWS Amplify to serve the frontend game interface with HTML, CSS, and JS. Use the integrated Amazon CloudFront configuration for distribution.
- () AWS Lambda is a cost-effective solution for unpredictable traffic patterns due to its pay-per-use pricing model. DynamoDB is also a cost-effective and highly scalable solution for storing user data. The API Gateway provides a HTTP-based endpoint that can be used to expose the Lambda function.
- () AWS Cognito User Pools provide user directory features including sign-up and sign-in services, which are suitable for managing game user authentication.
- () AWS Amplify simplifies the process of hosting web applications with automated deployment processes. It also integrates with CloudFront, providing a global content delivery network to efficiently serve the game interface.
- ()  is a correct answer (as explained above.)
- ()  is also a correct answer (as explained above.)
- () Using Amazon ECS might be an overkill for this scenario and might not be as cost-effective compared to Lambda and DynamoDB, especially for unpredictable and possibly idle traffic.
- () Cognito Identity Pools are used for granting access to AWS resources rather than handling user authentication.
- () While you could host a static website on S3 and use CloudFront for distribution, AWS Amplify can provide additional capabilities tailored to modern web applications. Furthermore, Amplify's automated deployment processes can provide a more streamlined and efficient approach to managing the game's frontend compared to managing separate S3 and CloudFront configurations.
- () https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html
- () https://aws.amazon.com/amplify/
- () https://digitalcloud.training/aws-lambda/
- () AWS Networking & Content Delivery
- () A multinational podcast company uses Amazon CloudFront for distributing its digital content. The company wants to gradually introduce content across various regions. It also needs to ensure that listeners who are outside the regions to which the content is currently released, cannot access the content.
- () Which solution will meet these requirements?
- () Encrypt the company's distributed content data and establish a custom error message.
- () Establish a new URL for the restricted content, control access with signed URLs and cookies, and set up a custom error message.
- () Create a new URL for the restricted content and establish an expiration date-based access policy for signed URLs.

**Answer:**
Correct Answer: **Set up VPC endpoints for Amazon EKS and ECR to enable nodes to communicate with the control plane.**

---

## Question 4

**Q:** Which combination of steps will meet these requirements MOST cost-effectively? (Select THREE.)

**Options:**
- (A) Correct selection
- (B) Use AWS Cognito User Pools to handle user authentication.
- (C) Use AWS Cognito Identity Pools to handle user authentication.
- (D) Implement an AWS Lambda function to fetch player information from Amazon DynamoDB. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the Lambda function.
- (E) Use Amazon S3 static web hosting with HTML, CSS, and JS. Use Amazon CloudFront to distribute the frontend game interface.
- (F) Set up an Amazon Elastic Container Service (Amazon ECS) service behind an Application Load Balancer to fetch player information from Amazon RDS. Establish an Amazon API Gateway endpoint to handle RESTful API calls, directing them to the ECS service.
- (G) Leverage AWS Amplify to serve the frontend game interface with HTML, CSS, and JS. Use the integrated Amazon CloudFront configuration for distribution.
- (H) AWS Lambda is a cost-effective solution for unpredictable traffic patterns due to its pay-per-use pricing model. DynamoDB is also a cost-effective and highly scalable solution for storing user data. The API Gateway provides a HTTP-based endpoint that can be used to expose the Lambda function.
- (I) AWS Cognito User Pools provide user directory features including sign-up and sign-in services, which are suitable for managing game user authentication.
- (J) AWS Amplify simplifies the process of hosting web applications with automated deployment processes. It also integrates with CloudFront, providing a global content delivery network to efficiently serve the game interface.
- ()  is a correct answer (as explained above.)
- ()  is also a correct answer (as explained above.)
- ()  is incorrect.
- () Using Amazon ECS might be an overkill for this scenario and might not be as cost-effective compared to Lambda and DynamoDB, especially for unpredictable and possibly idle traffic.
- () Cognito Identity Pools are used for granting access to AWS resources rather than handling user authentication.
- () While you could host a static website on S3 and use CloudFront for distribution, AWS Amplify can provide additional capabilities tailored to modern web applications. Furthermore, Amplify's automated deployment processes can provide a more streamlined and efficient approach to managing the game's frontend compared to managing separate S3 and CloudFront configurations.
- () References:
- () https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html
- () https://aws.amazon.com/amplify/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-lambda/
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Networking & Content Delivery
- () A multinational podcast company uses Amazon CloudFront for distributing its digital content. The company wants to gradually introduce content across various regions. It also needs to ensure that listeners who are outside the regions to which the content is currently released, cannot access the content.
- () Which solution will meet these requirements?
- () Encrypt the company's distributed content data and establish a custom error message.
- () Establish a new URL for the restricted content, control access with signed URLs and cookies, and set up a custom error message.
- () Create a new URL for the restricted content and establish an expiration date-based access policy for signed URLs.
- () Implement geographical restrictions on CloudFront content using a deny list and create a custom error message.
- () By setting geographical restrictions on CloudFront content using a deny list, the company can block access to content for users outside of the released regions. If a user from a blocked region attempts to access the content, they would receive the custom error message, thereby meeting the company's requirements.
- ()  is the correct answer (as explained above.)
- () While signed URLs and cookies can be used to control access to content, they don't inherently consider the geographical location of the users, thus it would not guarantee that only users in the released regions could access the content.
- () Although encrypting the content data adds a layer of security, it does not restrict access based on the geographical location of the users.
- () Time-based access policies with signed URLs can limit access to the content after a certain time, but it does not restrict access based on the geographical location of the users.
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/georestrictions.html
- () https://digitalcloud.training/amazon-cloudfront/
- () As a security measure, a finance-based organization want to introduce additional security measures for an existing application deployed in AWS. The application is serverless and has an Amazon API Gateway in front which is deployed in the us-east-1 Region and the eu-west-1 Region. The company requires the accounts to be secured against SQL injection and cross-site scripting attacks.
- () Which solution will meet these requirements with the LEAST amount of administrative effort?
- **() Set up AWS Firewall Manager in both Regions. Centrally configure AWS WAF rules.** [CORRECT]
- () Set up AWS WAF in both Regions. Associate Regional web ACLs with an API stage

**Answer:**
Correct Answer: **Set up AWS Firewall Manager in both Regions. Centrally configure AWS WAF rules.**

---

## Question 5

**Q:** Which solution will meet these requirements with the LEAST amount of administrative effort?

**Options:**
- (A) Set up AWS Firewall Manager in both Regions. Centrally configure AWS WAF rules.
- (B) Set up AWS WAF in both Regions. Associate Regional web ACLs with an API stage
- (C) Set up AWS Shield in one of the Regions. Associate Regional web ACLs with an API stage.
- (D) Set up AWS Shield in both Regions. Associate Regional web ACLs with an API stage.
- (E) AWS Firewall Manager simplifies your administration and maintenance tasks across multiple accounts and resources for a variety of protections, including AWS WAF, AWS Shield Advanced, Amazon VPC security groups, AWS Network Firewall, and Amazon Route 53 Resolver DNS Firewall. With Firewall Manager, you set up your protections just once and the service automatically applies them across your accounts and resources, even as you add new accounts and resources.
- (F) AWS WAF is used for protecting against malicious web attacks and is the best service to use to protect against SQL injection and cross-site scripting attacks. Used in combination with AWS Firewall Manager this solution protects both Regions and requires the least administrative effort.
- (G)  is the correct answer (as explained above.)
- (H)  is incorrect. This solution requires more administrative effort in rule management.
- (I)  is incorrect. The primary difference between AWS Shield and WAF is that while AWS WAF can mitigate DDoS attacks at layer 7 of the OSI reference model, AWS Shield protects web services from DDoS attacks at layer 3 and 4 of the OSI reference model. In this case AWS WAF should be used.
- (J)  is incorrect. As mentioned above, AWS Shield is not an appropriate choice for securing the accounts from SQL injection and cross-site scripting attacks.
- () References:
- () https://docs.aws.amazon.com/waf/latest/developerguide/fms-chapter.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-waf-shield/
- () AWS Security, Identity, & Compliance
- () An application has been migrated from on-premises to an Amazon EC2 instance. The migration has failed to an unknown dependency that the application must communicate with an on-premises server using private IP addresses.
- () Which action should a solutions architect take to quickly provision the necessary connectivity?
- () Create an Amazon CloudFront distribution
- () Create an AWS Transit Gateway
- () Configure a Virtual Private Gateway
- () Setup an AWS Direct Connect connection
- () A virtual private gateway is a logical, fully redundant distributed edge routing function that sits at the edge of your VPC. You must create a VPG in your VPC before you can establish an AWS Managed site-to-site VPN connection. The other end of the connection is the customer gateway which must be established on the customer side of the connection.
- ()  is the correct answer.
- ()  is incorrect as this would take too long to provision.
- ()  is incorrect. This is not a solution for enabling connectivity using private addresses to an on-premises site. CloudFront is a content delivery network (CDN).
- ()  is incorrect. AWS Transit Gateway connects VPCs and on-premises networks through a central hub which is not a requirement of this solution.
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- () https://digitalcloud.training/amazon-vpc/
- () AWS Networking & Content Delivery
- () A finance organization wants to deploy end of day processing applications to a fleet of Amazon EC2 instances with a focus on reducing cost. These applications are stateless and can be re-triggered in case of failure. The company needs a solution that minimizes cost and operational overhead.
- () What should a solutions architect do to meet these requirements?
- **() Use Spot Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.** [CORRECT]
- () Use On-Demand Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.
- () Use On-Demand Instances in an Amazon EC2 Auto Scaling group to run the application containers.
- () Use Spot Instances in an Amazon EC2 Auto Scaling group to run the application containers.
- () Since by using EC2 Spot Instances, customers can access additional compute capacity between 70%-90% off On-Demand Instance pricing, we can directly eliminate two options utilizing on demand instances.
- () Among the two options with spot instances, since the application is stateless, the better idea is to have a containerized approach and utilize EKS to reduce operational overhead.
- ()  is incorrect. As mentioned above, EKS gives you more options towards application fleet orchestration which makes it a better choice.
- ()  is incorrect.
- () As compared to spot instances, on demand instances are costlier and for end of day processing where failures can be re-triggered and are acceptable, spot instances are a better choice.
- () As compared to spot instances, on demand instances are more expensive and for end of day processing where failures can be re-triggered and are acceptable, spot instances are a better choice.
- () https://aws.amazon.com/blogs/compute/best-practices-for-handling-ec2-spot-instance-interruptions/

**Answer:**
Correct Answer: **Use Spot Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.**

---

## Question 6

**Q:** Which action should a solutions architect take to quickly provision the necessary connectivity?

**Options:**
- (A) Create an Amazon CloudFront distribution
- (B) Create an AWS Transit Gateway
- (C) Configure a Virtual Private Gateway
- (D) Setup an AWS Direct Connect connection
- (E) A virtual private gateway is a logical, fully redundant distributed edge routing function that sits at the edge of your VPC. You must create a VPG in your VPC before you can establish an AWS Managed site-to-site VPN connection. The other end of the connection is the customer gateway which must be established on the customer side of the connection.
- (F)  is the correct answer.
- (G)  is incorrect as this would take too long to provision.
- (H)  is incorrect. This is not a solution for enabling connectivity using private addresses to an on-premises site. CloudFront is a content delivery network (CDN).
- (I)  is incorrect. AWS Transit Gateway connects VPCs and on-premises networks through a central hub which is not a requirement of this solution.
- (J) References:
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-vpc/
- () AWS Networking & Content Delivery
- () A finance organization wants to deploy end of day processing applications to a fleet of Amazon EC2 instances with a focus on reducing cost. These applications are stateless and can be re-triggered in case of failure. The company needs a solution that minimizes cost and operational overhead.
- () What should a solutions architect do to meet these requirements?
- () Use Spot Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.
- () Use On-Demand Instances in an Amazon Elastic Kubernetes Service (Amazon EKS) managed node group.
- () Use On-Demand Instances in an Amazon EC2 Auto Scaling group to run the application containers.
- () Use Spot Instances in an Amazon EC2 Auto Scaling group to run the application containers.
- () Since by using EC2 Spot Instances, customers can access additional compute capacity between 70%-90% off On-Demand Instance pricing, we can directly eliminate two options utilizing on demand instances.
- () Among the two options with spot instances, since the application is stateless, the better idea is to have a containerized approach and utilize EKS to reduce operational overhead.
- ()  is the correct answer (as explained above.)
- ()  is incorrect. As mentioned above, EKS gives you more options towards application fleet orchestration which makes it a better choice.
- ()  is incorrect.
- () As compared to spot instances, on demand instances are costlier and for end of day processing where failures can be re-triggered and are acceptable, spot instances are a better choice.
- () As compared to spot instances, on demand instances are more expensive and for end of day processing where failures can be re-triggered and are acceptable, spot instances are a better choice.
- () https://aws.amazon.com/blogs/compute/best-practices-for-handling-ec2-spot-instance-interruptions/
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Compute
- () A media company has grown significantly in the past few months and the management team are concerned about compliance, governance, auditing, and security. The management team requires that configuration changes are tracked a history of API calls is recorded.
- () Use AWS Config to track configuration changes and Amazon CloudWatch to record API calls.
- () Use AWS CloudTrail to track configuration changes and AWS Config to record API calls.
- () Use AWS CloudTrail to track configuration changes and Amazon CloudWatch to record API calls.
- **() Use AWS Config to track configuration changes and AWS CloudTrail to record API calls.** [CORRECT]
- () As per definition of AWS CloudTrail and AWS Config:
- () CloudTrail is a web service that records AWS API calls for your AWS account and delivers log files to an Amazon S3 bucket. The recorded information includes the identity of the user, the start time of the AWS API call, the source IP address, the request parameters, and the response elements returned by the service.
- () AWS Config tracks changes in the configuration of your AWS resources, and it regularly sends updated configuration details to an Amazon S3 bucket that you specify. For each resource type that AWS Config records, it sends a configuration history file every six hours.
- () This option is the reverse of what’s needed, AWS config, as the name suggests, is used to track the configuration changes in AWS accounts.
- ()  is incorrect. CloudWatch is used for performance monitoring, not tracking API calls.
- ()  is incorrect. CloudTrail is not the right service for tracking configuration changes hence this option is incorrect.

**Answer:**
Correct Answer: **Use AWS Config to track configuration changes and AWS CloudTrail to record API calls.**

---

## Question 7

**Q:** What is the SIMPLEST method of achieving the requirements?

**Options:**
- (A) Create cross-account roles in each account to limit access to the services and actions that are allowed
- (B) Create a Network ACL that limits access to the services or actions and attach it to all relevant subnets
- (C) Create an IAM policy in the root account and attach it to users and groups in each account
- (D) Create a service control policy in the root organizational unit to deny access to the services or actions
- (E) Service control policies (SCPs) offer central control over the maximum available permissions for all accounts in your organization allowing you to ensure your accounts stay within your organization’s access control guidelines.
- (F) In the example below, a policy in OU1 restricts all users from launching EC2 instance types other than a t2.micro:
- (G)  is the correct answer.
- (H)  is incorrect. Network ACLs control network traffic - not API actions.
- (I)  is incorrect. This is not an efficient or centrally managed method of applying the security restrictions.
- (J)  is incorrect. This is another example of a complex and inefficient method of providing access across accounts and does not restrict API actions within the account.
- () References:
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_about-scps.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/certification-training/aws-solutions-architect-associate/security-identity-compliance/aws-accounts/
- () AWS Management & Governance
- () An international software firm provides its clients with custom solutions and tools designed for efficient data collection and analysis on AWS. The firm intends to centrally manage and distribute a standard set of solutions and tools for its clients' self-service needs.
- () Which solution would best satisfy these requirements?
- () Create AWS Config rules for the clients.
- () Create AWS CloudFormation stacks for the clients.
- () Create AWS Service Catalog portfolios for the clients.
- () Create AWS Systems Manager documents for the clients.
- () AWS Service Catalog enables organizations to create and manage catalogs of IT services that are approved for use on AWS. It allows centrally managed service portfolios, which clients can use on a self-service basis.
- () AWS Service Catalog provides a single location where organizations can centrally manage catalogs of IT services, which simplifies the organizational process and helps ensure compliance.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () While AWS CloudFormation is a powerful service for infrastructure as code (IaC), it doesn't provide a straightforward way for clients to discover and use shared tools or solutions for self-service needs. It lacks the management features and access control mechanisms necessary for this scenario.
- () AWS Systems Manager documents define the actions that Systems Manager performs on your managed instances. Although Systems Manager allows the central management of resources and applications, it doesn't provide an effective means for clients to self-discover and use shared tools or solutions.
- () AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. It isn't designed to centrally manage and distribute software tools or solutions.
- () https://aws.amazon.com/servicecatalog/
- () https://digitalcloud.training/aws-service-catalog/
- () A company has refactored a legacy application to run as two microservices using Amazon ECS. The application processes data in two parts and the second part of the process takes longer than the first.
- () How can a solutions architect integrate the microservices and allow them to scale independently?
- () Implement code in microservice 1 to publish data to an Amazon SNS topic. Implement code in microservice 2 to subscribe to this topic
- **() Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue** [CORRECT]
- () Implement code in microservice 1 to send data to Amazon Kinesis Data Firehose. Implement code in microservice 2 to read from Kinesis Data Firehose
- () Implement code in microservice 1 to send data to an Amazon S3 bucket. Use S3 event notifications to invoke microservice 2
- () This is a good use case for Amazon SQS. The microservices must be decoupled so they can scale independently. An Amazon SQS queue will enable microservice 1 to add messages to the queue. Microservice 2 can then pick up the messages and process them. This ensures that if there’s a spike in traffic on the frontend, messages do not get lost due to the backend process not being ready to process them.
- ()  is incorrect as a message queue would be preferable to an S3 bucket.
- ()  is incorrect as notifications to topics are pushed to subscribers. In this case we want the second microservice to pickup the messages when ready (pull them).
- ()  is incorrect as this is not how Firehose works. Firehose sends data directly to destinations, it is not a message queue.

**Answer:**
Correct Answer: **Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue**

---

## Question 8

**Q:** Which solution would best satisfy these requirements?

**Options:**
- (A) Create AWS Config rules for the clients.
- (B) Create AWS CloudFormation stacks for the clients.
- (C) Create AWS Service Catalog portfolios for the clients.
- (D) Create AWS Systems Manager documents for the clients.
- (E) AWS Service Catalog enables organizations to create and manage catalogs of IT services that are approved for use on AWS. It allows centrally managed service portfolios, which clients can use on a self-service basis.
- (F) AWS Service Catalog provides a single location where organizations can centrally manage catalogs of IT services, which simplifies the organizational process and helps ensure compliance.
- (G)  is the correct answer (as explained above.)
- (H)  is incorrect.
- (I) While AWS CloudFormation is a powerful service for infrastructure as code (IaC), it doesn't provide a straightforward way for clients to discover and use shared tools or solutions for self-service needs. It lacks the management features and access control mechanisms necessary for this scenario.
- (J) AWS Systems Manager documents define the actions that Systems Manager performs on your managed instances. Although Systems Manager allows the central management of resources and applications, it doesn't provide an effective means for clients to self-discover and use shared tools or solutions.
- () AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. It isn't designed to centrally manage and distribute software tools or solutions.
- () References:
- () https://aws.amazon.com/servicecatalog/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-service-catalog/
- () AWS Management & Governance
- () A company has refactored a legacy application to run as two microservices using Amazon ECS. The application processes data in two parts and the second part of the process takes longer than the first.
- () How can a solutions architect integrate the microservices and allow them to scale independently?
- () Implement code in microservice 1 to publish data to an Amazon SNS topic. Implement code in microservice 2 to subscribe to this topic
- () Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue
- () Implement code in microservice 1 to send data to Amazon Kinesis Data Firehose. Implement code in microservice 2 to read from Kinesis Data Firehose
- () Implement code in microservice 1 to send data to an Amazon S3 bucket. Use S3 event notifications to invoke microservice 2
- () This is a good use case for Amazon SQS. The microservices must be decoupled so they can scale independently. An Amazon SQS queue will enable microservice 1 to add messages to the queue. Microservice 2 can then pick up the messages and process them. This ensures that if there’s a spike in traffic on the frontend, messages do not get lost due to the backend process not being ready to process them.
- ()  is the correct answer.
- ()  is incorrect as a message queue would be preferable to an S3 bucket.
- ()  is incorrect as notifications to topics are pushed to subscribers. In this case we want the second microservice to pickup the messages when ready (pull them).
- ()  is incorrect as this is not how Firehose works. Firehose sends data directly to destinations, it is not a message queue.
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://digitalcloud.training/aws-application-integration-services/
- () AWS Application Integration
- () A new application will be launched on an Amazon EC2 instance with an Elastic Block Store (EBS) volume. A solutions architect needs to determine the most cost-effective storage option. The application will have infrequent usage, with peaks of traffic for a couple of hours in the morning and evening. Disk I/O is variable with peaks of up to 3,000 IOPS.
- () Which solution should the solutions architect recommend?
- () Amazon EBS Cold HDD (sc1)
- **() Amazon EBS General Purpose SSD (gp2)** [CORRECT]
- () Amazon EBS Provisioned IOPS SSD (io1)
- () Amazon EBS Throughput Optimized HDD (st1)
- () General Purpose SSD (gp2) volumes offer cost-effective storage that is ideal for a broad range of workloads. These volumes deliver single-digit millisecond latencies and the ability to burst to 3,000 IOPS for extended periods of time.
- () Between a minimum of 100 IOPS (at 33.33 GiB and below) and a maximum of 16,000 IOPS (at 5,334 GiB and above), baseline performance scales linearly at 3 IOPS per GiB of volume size. AWS designs gp2 volumes to deliver their provisioned performance 99% of the time. A gp2 volume can range in size from 1 GiB to 16 TiB.
- () In this case the volume would have a baseline performance of 3 x 200 = 600 IOPS. The volume could also burst to 3,000 IOPS for extended periods. As the I/O varies, this should be suitable.
- ()  is incorrect as this would be a more expensive option and is not required for the performance characteristics of this workload.
- ()  is incorrect as there is no IOPS SLA for HDD volumes and they would likely not perform well enough for this workload.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html

**Answer:**
Correct Answer: **Amazon EBS General Purpose SSD (gp2)**

---

## Question 9

**Q:** How can a solutions architect integrate the microservices and allow them to scale independently?

**Options:**
- (A) Implement code in microservice 1 to publish data to an Amazon SNS topic. Implement code in microservice 2 to subscribe to this topic
- (B) Implement code in microservice 1 to send data to an Amazon SQS queue. Implement code in microservice 2 to process messages from the queue
- (C) Implement code in microservice 1 to send data to Amazon Kinesis Data Firehose. Implement code in microservice 2 to read from Kinesis Data Firehose
- (D) Implement code in microservice 1 to send data to an Amazon S3 bucket. Use S3 event notifications to invoke microservice 2
- (E) This is a good use case for Amazon SQS. The microservices must be decoupled so they can scale independently. An Amazon SQS queue will enable microservice 1 to add messages to the queue. Microservice 2 can then pick up the messages and process them. This ensures that if there’s a spike in traffic on the frontend, messages do not get lost due to the backend process not being ready to process them.
- (F)  is the correct answer.
- (G)  is incorrect as a message queue would be preferable to an S3 bucket.
- (H)  is incorrect as notifications to topics are pushed to subscribers. In this case we want the second microservice to pickup the messages when ready (pull them).
- (I)  is incorrect as this is not how Firehose works. Firehose sends data directly to destinations, it is not a message queue.
- (J) References:
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-application-integration-services/
- () AWS Application Integration
- () A new application will be launched on an Amazon EC2 instance with an Elastic Block Store (EBS) volume. A solutions architect needs to determine the most cost-effective storage option. The application will have infrequent usage, with peaks of traffic for a couple of hours in the morning and evening. Disk I/O is variable with peaks of up to 3,000 IOPS.
- () Which solution should the solutions architect recommend?
- () Amazon EBS Cold HDD (sc1)
- () Amazon EBS General Purpose SSD (gp2)
- () Amazon EBS Provisioned IOPS SSD (io1)
- () Amazon EBS Throughput Optimized HDD (st1)
- () General Purpose SSD (gp2) volumes offer cost-effective storage that is ideal for a broad range of workloads. These volumes deliver single-digit millisecond latencies and the ability to burst to 3,000 IOPS for extended periods of time.
- () Between a minimum of 100 IOPS (at 33.33 GiB and below) and a maximum of 16,000 IOPS (at 5,334 GiB and above), baseline performance scales linearly at 3 IOPS per GiB of volume size. AWS designs gp2 volumes to deliver their provisioned performance 99% of the time. A gp2 volume can range in size from 1 GiB to 16 TiB.
- () In this case the volume would have a baseline performance of 3 x 200 = 600 IOPS. The volume could also burst to 3,000 IOPS for extended periods. As the I/O varies, this should be suitable.
- ()  is incorrect as this would be a more expensive option and is not required for the performance characteristics of this workload.
- ()  is incorrect as there is no IOPS SLA for HDD volumes and they would likely not perform well enough for this workload.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () https://digitalcloud.training/amazon-ebs/
- () AWS Compute
- () An application runs on Amazon EC2 instances in a private subnet. The EC2 instances process data that is stored in an Amazon S3 bucket. The data is highly confidential and a private and secure connection is required between the EC2 instances and the S3 bucket.
- () Which solution meets these requirements?
- **() Set up S3 bucket policies to allow access from a VPC endpoint.** [CORRECT]
- () Configure encryption for the S3 bucket using an AWS KMS key.
- () Configure a custom SSL/TLS certificate on the S3 bucket.
- () Set up an IAM policy to grant read-write access to the S3 bucket.
- () A gateway VPC endpoint can be used to access an Amazon S3 bucket using private IP addresses. To further secure the solution an S3 bucket policy can be created that restricts access to the VPC endpoint so connections cannot be made to the bucket from other sources.
- ()  is incorrect. This does not enable private access from EC2. A gateway VPC endpoint is required.
- ()  is incorrect. This will encrypt data at rest but does not secure the connection to the bucket or ensure private connections must be made.
- ()  is incorrect. You cannot add a custom SSL/TLS certificate to Amazon S3.
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies-vpc-endpoint.html
- () https://digitalcloud.training/amazon-vpc/
- () AWS Security, Identity, & Compliance

**Answer:**
Correct Answer: **Set up S3 bucket policies to allow access from a VPC endpoint.**

---

## Question 10

**Q:** Which system architecture should the solutions architect recommend?

**Options:**
- (A) Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function.
- (B) Set up an Amazon S3 gateway endpoint in your VPC. Connect the facility network to the VPC via a Site-to-Site VPN connection so that sensor data can be written directly to an S3 bucket.
- (C) Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB.
- (D) Create an Amazon EC2 instance to serve as the HTTPS endpoint and to process messages. An Amazon S3 bucket should be configured for the EC2 instance to save the results.
- (E) Amazon API Gateway would be ideal for providing a secure entry point for your application, and for traffic to be sent via HTTPS. AWS Lambda would integrate seamlessly with API Gateway to process the data, as an event-driven solution like this would be perfect when designing a scalable system based on sporadic use. Finally, DynamoDB is highly scalable and is a perfect repository for data to be stored for future analysis.
- (F)  is the correct answer (as explained above.)
- (G)  is incorrect. As the action of a badge being read to initiate access to a warehouse should only take a few seconds, spinning up an EC2 instance to serve as a HTTPS endpoint would take minutes, and is not suitable for this use case.
- (H) Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB” is incorrect. Amazon Route 53 is a managed DNS service, and DNS is not required in this instance as the badge reader does not have a DNS name.
- (I)  is incorrect. VPC endpoints are designed to facilitate traffic across the AWS backbone network between AWS services and are not used to create connections between external endpoints outside of the AWS network and an Amazon S3 bucket.
- (J) References:
- () https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-application-integration-services/
- () AWS Networking & Content Delivery
- () A multinational organization has a distributed application that runs on Amazon EC2 instances, which are behind an Application Load Balancer in an Auto Scaling group. The application utilizes a MySQL database hosted on Amazon Aurora. The database cluster spans across multiple Availability Zones in a single region.
- () The organization plans to launch its services in a new geographical area and wants to ensure maximum availability with minimal service interruption.
- () Which strategy should the organization adopt?
- () Expand the existing Auto Scaling group into the new Region. Utilize Amazon Aurora Global Database to extend the database across the primary and new regions. Implement Amazon Route 53 health checks with a failover routing policy directed towards the new region.
- **() Establish the application layer in the new region. Use Amazon Aurora Global Database for deploying the database in the primary and new regions. Apply Amazon Route 53 health checks with a failover routing policy to the new region. Promote the secondary to primary as needed.** [CORRECT]
- () Create a similar application layer in the new region. Establish a new Aurora MySQL database in this region. Use AWS Database Migration Service (AWS DMS) for ongoing replication from the primary database to the new region. Implement Amazon Route 53 health checks with a failover routing policy to the new region.
- () Replicate the application layer in the new region. Implement an Aurora MySQL Read Replica in the new region using Route 53 health checks and a failover routing policy. In case of primary failure, promote the Read Replica to primary.
- () This solution involves creating an application layer in the new region and using Amazon Aurora Global Database, which supports replicating your databases across multiple regions with minimal impact on performance.
- () This configuration can enhance disaster recovery capabilities and can reduce the impact of planned maintenance. Amazon Route 53 health checks with a failover routing policy can automatically route traffic to the new region in the event of a failure in the primary region, thereby ensuring high availability.
- () With an Aurora global database, there are two different approaches to failover depending on the scenario. You can use manual unplanned failover (detach and promote) or managed planned failover.
- ()  is incorrect.
- () AWS Database Migration Service (AWS DMS) is primarily used for migrating databases to AWS from on-premises environments or for replicating databases for data warehousing and other use cases. It isn't as suitable for ongoing high-availability or failover scenarios as Amazon Aurora Global Database, which is specifically designed for these situations.
- () It is not possible to expand an Auto Scaling group across multiple Regions. ASGs operate within a Region only.
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database-disaster-recovery.html#aurora-global-database-failover
- () https://digitalcloud.training/amazon-aurora/
- () AWS Compute
- () A company operates multiple AWS accounts under AWS Organizations. To better manage the costs, the company wants to allocate different budgets for each of these accounts. The company also wants to prevent additional resource provisioning in an AWS account if it reaches its allocated budget before the end of the budget period.
- () Which combination of solutions will meet these requirements? (Select THREE.)
- () Correct selection
- () Configure alerts in AWS Budgets to notify the company when an account is about to reach its budget threshold. Then use a budget action that links to the IAM role to prevent additional resource provisioning.
- () Use AWS Budgets in the AWS Management Console to set up budgets and specify the cost threshold for each AWS account.
- () Create an IAM user with adequate permissions to allow AWS Budgets to enforce budget actions.
- () Set up an alert in AWS Budgets to notify the company when a particular account meets its budget threshold. Enable real-time monitoring for immediate notification.
- () Set up an IAM role with the necessary permissions that allow AWS Budgets to execute budget actions.
- () Use AWS Budgets to establish different budgets for each AWS account. Configure the budgets in the Billing and Cost Management console.
- () AWS Budgets is a tool that enables you to set custom cost and usage budgets. You can set your budget amount, and AWS provides you with estimated charges and forecasted costs for your AWS usage. Configuring the budgets in the Billing and Cost Management console is a recommended step.
- () AWS Budgets can execute budget actions (like preventing additional resource provisioning) using an IAM role with the necessary permissions.

**Answer:**
Correct Answer: **Establish the application layer in the new region. Use Amazon Aurora Global Database for deploying the database in the primary and new regions. Apply Amazon Route 53 health checks with a failover routing policy to the new region. Promote the secondary to primary as needed.**

---

## Question 11

**Q:** Which strategy should the organization adopt?

**Options:**
- (A) Expand the existing Auto Scaling group into the new Region. Utilize Amazon Aurora Global Database to extend the database across the primary and new regions. Implement Amazon Route 53 health checks with a failover routing policy directed towards the new region.
- (B) Establish the application layer in the new region. Use Amazon Aurora Global Database for deploying the database in the primary and new regions. Apply Amazon Route 53 health checks with a failover routing policy to the new region. Promote the secondary to primary as needed.
- (C) Create a similar application layer in the new region. Establish a new Aurora MySQL database in this region. Use AWS Database Migration Service (AWS DMS) for ongoing replication from the primary database to the new region. Implement Amazon Route 53 health checks with a failover routing policy to the new region.
- (D) Replicate the application layer in the new region. Implement an Aurora MySQL Read Replica in the new region using Route 53 health checks and a failover routing policy. In case of primary failure, promote the Read Replica to primary.
- (E) This solution involves creating an application layer in the new region and using Amazon Aurora Global Database, which supports replicating your databases across multiple regions with minimal impact on performance.
- (F) This configuration can enhance disaster recovery capabilities and can reduce the impact of planned maintenance. Amazon Route 53 health checks with a failover routing policy can automatically route traffic to the new region in the event of a failure in the primary region, thereby ensuring high availability.
- (G) With an Aurora global database, there are two different approaches to failover depending on the scenario. You can use manual unplanned failover (detach and promote) or managed planned failover.
- (H)  is the correct answer (as explained above.)
- (I)  is incorrect.
- (J) AWS Database Migration Service (AWS DMS) is primarily used for migrating databases to AWS from on-premises environments or for replicating databases for data warehousing and other use cases. It isn't as suitable for ongoing high-availability or failover scenarios as Amazon Aurora Global Database, which is specifically designed for these situations.
- () It is not possible to expand an Auto Scaling group across multiple Regions. ASGs operate within a Region only.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database-disaster-recovery.html#aurora-global-database-failover
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-aurora/
- () AWS Compute
- () A company operates multiple AWS accounts under AWS Organizations. To better manage the costs, the company wants to allocate different budgets for each of these accounts. The company also wants to prevent additional resource provisioning in an AWS account if it reaches its allocated budget before the end of the budget period.
- () Which combination of solutions will meet these requirements? (Select THREE.)
- () Correct selection
- () Configure alerts in AWS Budgets to notify the company when an account is about to reach its budget threshold. Then use a budget action that links to the IAM role to prevent additional resource provisioning.
- () Use AWS Budgets in the AWS Management Console to set up budgets and specify the cost threshold for each AWS account.
- () Create an IAM user with adequate permissions to allow AWS Budgets to enforce budget actions.
- () Set up an alert in AWS Budgets to notify the company when a particular account meets its budget threshold. Enable real-time monitoring for immediate notification.
- () Set up an IAM role with the necessary permissions that allow AWS Budgets to execute budget actions.
- () Use AWS Budgets to establish different budgets for each AWS account. Configure the budgets in the Billing and Cost Management console.
- () AWS Budgets is a tool that enables you to set custom cost and usage budgets. You can set your budget amount, and AWS provides you with estimated charges and forecasted costs for your AWS usage. Configuring the budgets in the Billing and Cost Management console is a recommended step.
- () AWS Budgets can execute budget actions (like preventing additional resource provisioning) using an IAM role with the necessary permissions.
- () Configuring alerts in AWS Budgets and linking a budget action to an IAM role for automatic prevention of additional resource provisioning is a correct and efficient way to manage costs.
- ()  is a correct answer (as explained above.)
- ()  is also a correct answer (as explained above.)
- () While AWS Budgets can indeed be set up in the AWS Management Console, the budgets aren't set in the context of cost thresholds for each AWS account. This option is not fully accurate.
- () Although you can create an IAM user with necessary permissions, using an IAM role is generally a better practice. An IAM user is an entity that you create in AWS to represent the person or service that uses it to interact with AWS, while an IAM role is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. A role does not have long-term credentials associated with it like an IAM user does.
- () AWS Budgets doesn't allow for real-time monitoring; the data can be delayed up to 24 hours. The frequency of budget alert notifications is not customizable to the minute or hour; they are typically sent out daily, weekly, or when a certain threshold is crossed.
- () https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-controls.html
- () https://digitalcloud.training/aws-cost-management/
- () AWS Management & Governance
- () A Solutions Architect needs a solution for hosting a website that will be used by a development team. The website contents will consist of HTML, CSS, client-side JavaScript, and images.
- () Which solution is MOST cost-effective?
- () Use a Docker container to host the website on AWS Fargate.
- **() Create an Amazon S3 bucket and host the website there.** [CORRECT]

**Answer:**
Correct Answer: **Create an Amazon S3 bucket and host the website there.**

---

## Question 12

**Q:** Which combination of solutions will meet these requirements? (Select THREE.)

**Options:**
- (A) Correct selection
- (B) Configure alerts in AWS Budgets to notify the company when an account is about to reach its budget threshold. Then use a budget action that links to the IAM role to prevent additional resource provisioning.
- (C) Use AWS Budgets in the AWS Management Console to set up budgets and specify the cost threshold for each AWS account.
- (D) Create an IAM user with adequate permissions to allow AWS Budgets to enforce budget actions.
- (E) Set up an alert in AWS Budgets to notify the company when a particular account meets its budget threshold. Enable real-time monitoring for immediate notification.
- (F) Set up an IAM role with the necessary permissions that allow AWS Budgets to execute budget actions.
- (G) Use AWS Budgets to establish different budgets for each AWS account. Configure the budgets in the Billing and Cost Management console.
- (H) AWS Budgets is a tool that enables you to set custom cost and usage budgets. You can set your budget amount, and AWS provides you with estimated charges and forecasted costs for your AWS usage. Configuring the budgets in the Billing and Cost Management console is a recommended step.
- (I) AWS Budgets can execute budget actions (like preventing additional resource provisioning) using an IAM role with the necessary permissions.
- (J) Configuring alerts in AWS Budgets and linking a budget action to an IAM role for automatic prevention of additional resource provisioning is a correct and efficient way to manage costs.
- ()  is a correct answer (as explained above.)
- ()  is also a correct answer (as explained above.)
- ()  is incorrect.
- () While AWS Budgets can indeed be set up in the AWS Management Console, the budgets aren't set in the context of cost thresholds for each AWS account. This option is not fully accurate.
- () Although you can create an IAM user with necessary permissions, using an IAM role is generally a better practice. An IAM user is an entity that you create in AWS to represent the person or service that uses it to interact with AWS, while an IAM role is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. A role does not have long-term credentials associated with it like an IAM user does.
- () AWS Budgets doesn't allow for real-time monitoring; the data can be delayed up to 24 hours. The frequency of budget alert notifications is not customizable to the minute or hour; they are typically sent out daily, weekly, or when a certain threshold is crossed.
- () References:
- () https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-controls.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-cost-management/
- () AWS Management & Governance
- () A Solutions Architect needs a solution for hosting a website that will be used by a development team. The website contents will consist of HTML, CSS, client-side JavaScript, and images.
- () Which solution is MOST cost-effective?
- () Use a Docker container to host the website on AWS Fargate.
- () Create an Amazon S3 bucket and host the website there.
- () Launch an Amazon EC2 instance and host the website there.
- () Create an Application Load Balancer with an AWS Lambda target.
- () Amazon S3 can be used for hosting static websites and cannot be used for dynamic content. In this case the content is purely static with client-side code running. Therefore, an S3 static website will be the most cost-effective solution for hosting this website.
- ()  is the correct answer.
- ()  is incorrect. This will be more expensive as it uses an EC2 instances.
- ()  is incorrect. A static website on S3 is sufficient for this use case and will be more cost-effective than Fargate.
- ()  is incorrect. This is also a more expensive solution and unnecessary for this use case.
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () AWS Storage
- () Health related data in Amazon S3 needs to be frequently accessed for up to 90 days. After that time the data must be retained for compliance reasons for seven years and is rarely accessed.
- () Which storage classes should be used?
- () Store data in STANDARD for 90 days then transition to REDUCED_REDUNDANCY
- () Store data in INTELLIGENT_TIERING for 90 days then transition to STANDARD_IA
- () Store data in STANDARD for 90 days then expire the data
- **() Store data in STANDARD for 90 days then transition the data to DEEP_ARCHIVE** [CORRECT]
- () In this case the data is frequently accessed so must be stored in standard for the first 90 days. After that the data is still to be kept for compliance reasons but is rarely accessed so is a good use case for DEEP_ARCHIVE.

**Answer:**
Correct Answer: **Store data in STANDARD for 90 days then transition the data to DEEP_ARCHIVE**

---

## Question 13

**Q:** Which solution is MOST cost-effective?

**Options:**
- (A) Use a Docker container to host the website on AWS Fargate.
- (B) Create an Amazon S3 bucket and host the website there.
- (C) Launch an Amazon EC2 instance and host the website there.
- (D) Create an Application Load Balancer with an AWS Lambda target.
- (E) Amazon S3 can be used for hosting static websites and cannot be used for dynamic content. In this case the content is purely static with client-side code running. Therefore, an S3 static website will be the most cost-effective solution for hosting this website.
- (F)  is the correct answer.
- (G)  is incorrect. This will be more expensive as it uses an EC2 instances.
- (H)  is incorrect. A static website on S3 is sufficient for this use case and will be more cost-effective than Fargate.
- (I)  is incorrect. This is also a more expensive solution and unnecessary for this use case.
- (J) References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () AWS Storage
- () Health related data in Amazon S3 needs to be frequently accessed for up to 90 days. After that time the data must be retained for compliance reasons for seven years and is rarely accessed.
- () Which storage classes should be used?
- () Store data in STANDARD for 90 days then transition to REDUCED_REDUNDANCY
- () Store data in INTELLIGENT_TIERING for 90 days then transition to STANDARD_IA
- () Store data in STANDARD for 90 days then expire the data
- () Store data in STANDARD for 90 days then transition the data to DEEP_ARCHIVE
- () In this case the data is frequently accessed so must be stored in standard for the first 90 days. After that the data is still to be kept for compliance reasons but is rarely accessed so is a good use case for DEEP_ARCHIVE.
- ()  is incorrect. You cannot transition from INTELLIGENT_TIERING to STANDARD_IA.
- ()  is incorrect. Expiring the data is not possible as it must be retained for compliance.
- ()  is incorrect. You cannot transition from any storage class to REDUCED_REDUNDANCY.
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/lifecycle-transition-general-considerations.html
- () A company is in the process of improving its security posture and wants to analyze and rectify a high volume of failed login attempts and unauthorized activities being logged in AWS CloudTrail.
- () What is the most efficient solution to help the company identify these security events with the LEAST amount of operational effort?
- **() Use Amazon Athena to directly query CloudTrail logs for failed logins and unauthorized activities.** [CORRECT]
- () Utilize AWS Data Pipeline to regularly extract CloudTrail logs and use a custom script to identify the required security events.
- () Leverage AWS Lambda to trigger on CloudTrail log updates and use a custom script to scan for failed logins and unauthorized actions.
- () Implement Amazon Elasticsearch Service with Kibana to visualize the CloudTrail logs and manually search for these events.
- () Amazon Athena can directly query data from S3 (where CloudTrail logs are stored) using standard SQL, making it a powerful and efficient tool for analyzing these logs. You don't need to manage any infrastructure or write custom scripts, and you can quickly write and run queries to identify the required security events.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () While Lambda functions can be triggered based on CloudTrail log updates and could theoretically be used to scan for security events, this would require substantial setup and ongoing maintenance of the script. It's not the most efficient choice.
- () This solution could work, but the operational overhead of managing the extraction process and maintaining a custom script for analysis is not minimal.
- () While Elasticsearch and Kibana provide powerful search and visualization capabilities, respectively, they require a fair amount of setup and management. This option would provide more in-depth analysis and real-time monitoring, but it wouldn't be the most efficient way to simply identify the security events mentioned.
- () https://docs.aws.amazon.com/athena/latest/ug/cloudtrail-logs.html
- () https://digitalcloud.training/amazon-athena/

**Answer:**
Correct Answer: **Use Amazon Athena to directly query CloudTrail logs for failed logins and unauthorized activities.**

---

## Question 14

**Q:** Which storage classes should be used?

**Options:**
- (A) Store data in STANDARD for 90 days then transition to REDUCED_REDUNDANCY
- (B) Store data in INTELLIGENT_TIERING for 90 days then transition to STANDARD_IA
- (C) Store data in STANDARD for 90 days then expire the data
- (D) Store data in STANDARD for 90 days then transition the data to DEEP_ARCHIVE
- (E) In this case the data is frequently accessed so must be stored in standard for the first 90 days. After that the data is still to be kept for compliance reasons but is rarely accessed so is a good use case for DEEP_ARCHIVE.
- (F)  is the correct answer.
- (G)  is incorrect. You cannot transition from INTELLIGENT_TIERING to STANDARD_IA.
- (H)  is incorrect. Expiring the data is not possible as it must be retained for compliance.
- (I)  is incorrect. You cannot transition from any storage class to REDUCED_REDUNDANCY.
- (J) References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/lifecycle-transition-general-considerations.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () AWS Storage
- () A company is in the process of improving its security posture and wants to analyze and rectify a high volume of failed login attempts and unauthorized activities being logged in AWS CloudTrail.
- () What is the most efficient solution to help the company identify these security events with the LEAST amount of operational effort?
- () Use Amazon Athena to directly query CloudTrail logs for failed logins and unauthorized activities.
- () Utilize AWS Data Pipeline to regularly extract CloudTrail logs and use a custom script to identify the required security events.
- () Leverage AWS Lambda to trigger on CloudTrail log updates and use a custom script to scan for failed logins and unauthorized actions.
- () Implement Amazon Elasticsearch Service with Kibana to visualize the CloudTrail logs and manually search for these events.
- () Amazon Athena can directly query data from S3 (where CloudTrail logs are stored) using standard SQL, making it a powerful and efficient tool for analyzing these logs. You don't need to manage any infrastructure or write custom scripts, and you can quickly write and run queries to identify the required security events.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () While Lambda functions can be triggered based on CloudTrail log updates and could theoretically be used to scan for security events, this would require substantial setup and ongoing maintenance of the script. It's not the most efficient choice.
- () This solution could work, but the operational overhead of managing the extraction process and maintaining a custom script for analysis is not minimal.
- () While Elasticsearch and Kibana provide powerful search and visualization capabilities, respectively, they require a fair amount of setup and management. This option would provide more in-depth analysis and real-time monitoring, but it wouldn't be the most efficient way to simply identify the security events mentioned.
- () https://docs.aws.amazon.com/athena/latest/ug/cloudtrail-logs.html
- () https://digitalcloud.training/amazon-athena/
- () AWS Analytics
- () A systems administrator of a company wants to detect and remediate the compromise of services such as Amazon EC2 instances and Amazon S3 buckets.
- () Which AWS service can the administrator use to protect the company against attacks?
- **() Amazon GuardDuty** [CORRECT]
- () Amazon Macie
- () Amazon Inspector
- () Amazon Cognito
- () Amazon GuardDuty gives you access to built-in detection techniques that are developed and optimized for the cloud. The detection algorithms are maintained and continuously improved upon by AWS Security. The primary detection categories include reconnaissance, instance compromise, account compromise, and bucket compromise.
- () Amazon GuardDuty offers HTTPS APIs, CLI tools, and Amazon CloudWatch Events to support automated security responses to security findings. For example, you can automate the response workflow by using CloudWatch Events as an event source to trigger an AWS Lambda function.
- ()  is incorrect. Cognito provides sign up and sign services for mobiles apps.
- ()  is incorrect. Inspector is more about identifying vulnerabilities and evaluating against security best practices. It does not detect compromise.
- ()  is incorrect. Macie is used for detecting and protecting sensitive data that is in Amazon S3.
- () https://aws.amazon.com/guardduty/features/
- () https://digitalcloud.training/additional-aws-services/

**Answer:**
Correct Answer: **Amazon GuardDuty**

---

## Question 15

**Q:** What is the most efficient solution to help the company identify these security events with the LEAST amount of operational effort?

**Options:**
- (A) Use Amazon Athena to directly query CloudTrail logs for failed logins and unauthorized activities.
- (B) Utilize AWS Data Pipeline to regularly extract CloudTrail logs and use a custom script to identify the required security events.
- (C) Leverage AWS Lambda to trigger on CloudTrail log updates and use a custom script to scan for failed logins and unauthorized actions.
- (D) Implement Amazon Elasticsearch Service with Kibana to visualize the CloudTrail logs and manually search for these events.
- (E) Amazon Athena can directly query data from S3 (where CloudTrail logs are stored) using standard SQL, making it a powerful and efficient tool for analyzing these logs. You don't need to manage any infrastructure or write custom scripts, and you can quickly write and run queries to identify the required security events.
- (F)  is the correct answer (as explained above.)
- (G)  is incorrect.
- (H) While Lambda functions can be triggered based on CloudTrail log updates and could theoretically be used to scan for security events, this would require substantial setup and ongoing maintenance of the script. It's not the most efficient choice.
- (I) This solution could work, but the operational overhead of managing the extraction process and maintaining a custom script for analysis is not minimal.
- (J) While Elasticsearch and Kibana provide powerful search and visualization capabilities, respectively, they require a fair amount of setup and management. This option would provide more in-depth analysis and real-time monitoring, but it wouldn't be the most efficient way to simply identify the security events mentioned.
- () References:
- () https://docs.aws.amazon.com/athena/latest/ug/cloudtrail-logs.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-athena/
- () AWS Analytics
- () A systems administrator of a company wants to detect and remediate the compromise of services such as Amazon EC2 instances and Amazon S3 buckets.
- () Which AWS service can the administrator use to protect the company against attacks?
- () Amazon GuardDuty
- () Amazon Macie
- () Amazon Inspector
- () Amazon Cognito
- () Amazon GuardDuty gives you access to built-in detection techniques that are developed and optimized for the cloud. The detection algorithms are maintained and continuously improved upon by AWS Security. The primary detection categories include reconnaissance, instance compromise, account compromise, and bucket compromise.
- () Amazon GuardDuty offers HTTPS APIs, CLI tools, and Amazon CloudWatch Events to support automated security responses to security findings. For example, you can automate the response workflow by using CloudWatch Events as an event source to trigger an AWS Lambda function.
- ()  is the correct answer.
- ()  is incorrect. Cognito provides sign up and sign services for mobiles apps.
- ()  is incorrect. Inspector is more about identifying vulnerabilities and evaluating against security best practices. It does not detect compromise.
- ()  is incorrect. Macie is used for detecting and protecting sensitive data that is in Amazon S3.
- () https://aws.amazon.com/guardduty/features/
- () https://digitalcloud.training/additional-aws-services/
- () AWS Security, Identity, & Compliance
- () An application runs on Amazon EC2 instances across multiple Availability Zones. The instances run in an Amazon EC2 Auto Scaling group behind an Application Load Balancer. The application performs best when the CPU utilization of the EC2 instances is at or near 40%.
- () What should a solutions architect do to maintain the desired performance across all instances in the group?
- **() Use a target tracking policy to dynamically scale the Auto Scaling group** [CORRECT]
- () Use an AWS Lambda function to update the desired Auto Scaling group capacity
- () Use scheduled scaling actions to scale up and scale down the Auto Scaling group
- () Use a simple scaling policy to dynamically scale the Auto Scaling group
- () With target tracking scaling policies, you select a scaling metric and set a target value. Amazon EC2 Auto Scaling creates and manages the CloudWatch alarms that trigger the scaling policy and calculates the scaling adjustment based on the metric and the target value.
- () The scaling policy adds or removes capacity as required to keep the metric at, or close to, the specified target value. In addition to keeping the metric close to the target value, a target tracking scaling policy also adjusts to the changes in the metric due to a changing load pattern.
- ()  is incorrect as target tracking is a better way to keep the aggregate CPU usage at around 40%
- ()  is incorrect as this can be done automatically.
- ()  is incorrect as dynamic scaling is required to respond to changes in utilization.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html

**Answer:**
Correct Answer: **Use a target tracking policy to dynamically scale the Auto Scaling group**

---

## Question 16

**Q:** Which AWS service can the administrator use to protect the company against attacks?

**Options:**
- (A) Amazon GuardDuty
- (B) Amazon Macie
- (C) Amazon Inspector
- (D) Amazon Cognito
- (E) Amazon GuardDuty gives you access to built-in detection techniques that are developed and optimized for the cloud. The detection algorithms are maintained and continuously improved upon by AWS Security. The primary detection categories include reconnaissance, instance compromise, account compromise, and bucket compromise.
- (F) Amazon GuardDuty offers HTTPS APIs, CLI tools, and Amazon CloudWatch Events to support automated security responses to security findings. For example, you can automate the response workflow by using CloudWatch Events as an event source to trigger an AWS Lambda function.
- (G)  is the correct answer.
- (H)  is incorrect. Cognito provides sign up and sign services for mobiles apps.
- (I)  is incorrect. Inspector is more about identifying vulnerabilities and evaluating against security best practices. It does not detect compromise.
- (J)  is incorrect. Macie is used for detecting and protecting sensitive data that is in Amazon S3.
- () References:
- () https://aws.amazon.com/guardduty/features/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/additional-aws-services/
- () AWS Security, Identity, & Compliance
- () An application runs on Amazon EC2 instances across multiple Availability Zones. The instances run in an Amazon EC2 Auto Scaling group behind an Application Load Balancer. The application performs best when the CPU utilization of the EC2 instances is at or near 40%.
- () What should a solutions architect do to maintain the desired performance across all instances in the group?
- () Use a target tracking policy to dynamically scale the Auto Scaling group
- () Use an AWS Lambda function to update the desired Auto Scaling group capacity
- () Use scheduled scaling actions to scale up and scale down the Auto Scaling group
- () Use a simple scaling policy to dynamically scale the Auto Scaling group
- () With target tracking scaling policies, you select a scaling metric and set a target value. Amazon EC2 Auto Scaling creates and manages the CloudWatch alarms that trigger the scaling policy and calculates the scaling adjustment based on the metric and the target value.
- () The scaling policy adds or removes capacity as required to keep the metric at, or close to, the specified target value. In addition to keeping the metric close to the target value, a target tracking scaling policy also adjusts to the changes in the metric due to a changing load pattern.
- ()  is incorrect as target tracking is a better way to keep the aggregate CPU usage at around 40%
- ()  is incorrect as this can be done automatically.
- ()  is incorrect as dynamic scaling is required to respond to changes in utilization.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
- () https://digitalcloud.training/amazon-ec2-auto-scaling/
- () AWS Compute
- () An application uses an Amazon RDS database and Amazon EC2 instances in a web tier. The web tier instances must not be directly accessible from the internet to improve security.
- () How can a Solutions Architect meet these requirements?
- **() Launch the EC2 instances in a private subnet and create an Application Load Balancer in a public subnet** [CORRECT]
- () Launch the EC2 instances in a public subnet and create an Application Load Balancer in a public subnet
- () Launch the EC2 instances in a public subnet and use AWS WAF to protect the instances from internet-based attacks
- () Launch the EC2 instances in a private subnet with a NAT gateway and update the route table
- () To prevent direct connectivity to the EC2 instances from the internet you can deploy your EC2 instances in a private subnet and have the ELB in a public subnet. To configure this you must enable a public subnet in the ELB that is in the same AZ as the private subnet.
- ()  is incorrect. This configuration will not allow the application to be accessible from the internet, the aim is to only prevent direct access to the EC2 instances.
- ()  is incorrect. With the EC2 instances in a public subnet, direct access from the internet is possible. It only takes a security group misconfiguration or software exploit and the instance becomes vulnerable to attack.
- ()  is incorrect. The EC2 instances should be launched in a private subnet.
- () https://aws.amazon.com/premiumsupport/knowledge-center/public-load-balancer-private-ec2/
- () https://digitalcloud.training/amazon-vpc/

**Answer:**
Correct Answer: **Launch the EC2 instances in a private subnet and create an Application Load Balancer in a public subnet**

---

## Question 17

**Q:** What should a solutions architect do to maintain the desired performance across all instances in the group?

**Options:**
- (A) Use a target tracking policy to dynamically scale the Auto Scaling group
- (B) Use an AWS Lambda function to update the desired Auto Scaling group capacity
- (C) Use scheduled scaling actions to scale up and scale down the Auto Scaling group
- (D) Use a simple scaling policy to dynamically scale the Auto Scaling group
- (E) With target tracking scaling policies, you select a scaling metric and set a target value. Amazon EC2 Auto Scaling creates and manages the CloudWatch alarms that trigger the scaling policy and calculates the scaling adjustment based on the metric and the target value.
- (F) The scaling policy adds or removes capacity as required to keep the metric at, or close to, the specified target value. In addition to keeping the metric close to the target value, a target tracking scaling policy also adjusts to the changes in the metric due to a changing load pattern.
- (G)  is the correct answer.
- (H)  is incorrect as target tracking is a better way to keep the aggregate CPU usage at around 40%
- (I)  is incorrect as this can be done automatically.
- (J)  is incorrect as dynamic scaling is required to respond to changes in utilization.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2-auto-scaling/
- () AWS Compute
- () An application uses an Amazon RDS database and Amazon EC2 instances in a web tier. The web tier instances must not be directly accessible from the internet to improve security.
- () How can a Solutions Architect meet these requirements?
- () Launch the EC2 instances in a private subnet and create an Application Load Balancer in a public subnet
- () Launch the EC2 instances in a public subnet and create an Application Load Balancer in a public subnet
- () Launch the EC2 instances in a public subnet and use AWS WAF to protect the instances from internet-based attacks
- () Launch the EC2 instances in a private subnet with a NAT gateway and update the route table
- () To prevent direct connectivity to the EC2 instances from the internet you can deploy your EC2 instances in a private subnet and have the ELB in a public subnet. To configure this you must enable a public subnet in the ELB that is in the same AZ as the private subnet.
- ()  is incorrect. This configuration will not allow the application to be accessible from the internet, the aim is to only prevent direct access to the EC2 instances.
- ()  is incorrect. With the EC2 instances in a public subnet, direct access from the internet is possible. It only takes a security group misconfiguration or software exploit and the instance becomes vulnerable to attack.
- ()  is incorrect. The EC2 instances should be launched in a private subnet.
- () https://aws.amazon.com/premiumsupport/knowledge-center/public-load-balancer-private-ec2/
- () https://digitalcloud.training/amazon-vpc/
- () AWS Networking & Content Delivery
- () A digital media company uses an Amazon RDS MySQL instance for its content management system. Recently, the company has observed that their RDS instance is nearing its storage capacity due to the constant influx of new data. The company wants to ensure there's always sufficient storage without any operational interruption or manual intervention.
- () Which solution should the company use to address this situation with the LEAST operational overhead?
- () Migrate the database to a larger Amazon RDS MySQL instance.
- () Utilize Amazon ElastiCache to offload some read traffic and reduce database load.
- () Implement a lifecycle policy to delete older data from the MySQL instance.
- **() Enable automatic storage scaling for the MySQL instance.** [CORRECT]
- () Amazon RDS's automatic storage scaling allows the database to automatically increase its storage capacity when the available storage is low. This feature helps to prevent out-of-storage situations and requires no operational overhead.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () While this would provide more storage, it does not address the issue of potential future storage shortages and requires significant operational effort for the migration.
- () While this might help free up some storage, it might not be suitable if all data is essential for business operations. Also, this does not provide a long-term solution if data growth continues.
- () While ElastiCache can help to improve the database's read efficiency, it doesn't directly address the disk space concern for the RDS instance.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PIOPS.StorageTypes.html

**Answer:**
Correct Answer: **Enable automatic storage scaling for the MySQL instance.**

---

## Question 18

**Q:** Which solution should the company use to address this situation with the LEAST operational overhead?

**Options:**
- (A) Migrate the database to a larger Amazon RDS MySQL instance.
- (B) Utilize Amazon ElastiCache to offload some read traffic and reduce database load.
- (C) Implement a lifecycle policy to delete older data from the MySQL instance.
- (D) Enable automatic storage scaling for the MySQL instance.
- (E) Amazon RDS's automatic storage scaling allows the database to automatically increase its storage capacity when the available storage is low. This feature helps to prevent out-of-storage situations and requires no operational overhead.
- (F)  is the correct answer (as explained above.)
- (G)  is incorrect.
- (H) While this would provide more storage, it does not address the issue of potential future storage shortages and requires significant operational effort for the migration.
- (I) While this might help free up some storage, it might not be suitable if all data is essential for business operations. Also, this does not provide a long-term solution if data growth continues.
- (J) While ElastiCache can help to improve the database's read efficiency, it doesn't directly address the disk space concern for the RDS instance.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PIOPS.StorageTypes.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-rds/
- () AWS Database
- () A web application is running on a fleet of Amazon EC2 instances using an Auto Scaling Group. It is desired that the CPU usage in the fleet is kept at 40%.
- () How should scaling be configured?
- () Use a simple scaling policy that launches instances when the average CPU hits 40%
- () Use a step scaling policy that uses the PercentChangeInCapacity value to adjust the group size as required
- () Use a target tracking policy that keeps the average aggregate CPU utilization at 40%
- () Use a custom CloudWatch alarm to monitor CPU usage and notify the ASG using Amazon SNS
- () This is a perfect use case for a target tracking scaling policy. With target tracking scaling policies, you select a scaling metric and set a target value. In this case you can just set the target value to 40% average aggregate CPU utilization.
- ()  is the correct answer.
- ()  is incorrect. A simple scaling policy will add instances when 40% CPU utilization is reached, but it is not designed to maintain 40% CPU utilization across the group.
- ()  is incorrect. The step scaling policy makes scaling adjustments based on a number of factors. The PercentChangeInCapacity value increments or decrements the group size by a specified percentage. This does not relate to CPU utilization.
- ()  is incorrect. You do not need to create a custom Amazon CloudWatch alarm as the ASG can scale using a policy based on CPU utilization using standard configuration.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html
- () https://digitalcloud.training/amazon-ec2-auto-scaling/
- () AWS Compute
- () A financial institution wants to use machine learning (ML) algorithms to detect potential fraudulent transactions. They need to create ML models based on their vast financial transaction data and integrate these models into their business intelligence system for real-time decision-making. The solution should require minimal operational overhead.
- () Which solution will best meet these requirements?
- () Use Amazon Comprehend for analyzing the transaction data and Amazon Elasticsearch for visualization.
- **() Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization.** [CORRECT]
- () Use a pre-built ML Amazon Machine Image (AMI) from the AWS Marketplace to build and train models and use AWS Athena for data visualization.
- () 1. Use AWS Glue to perform ETL jobs on the transaction data and use Amazon Forecast for predictive analytics.
- () Amazon SageMaker is a fully managed service that provides every developer and data scientist with the ability to build, train, and deploy machine learning models quickly. It can directly connect with data sources and has built-in algorithms to ease the ML process.
- () Amazon QuickSight is a business intelligence tool that can be used to create dashboards for data visualization. This combination perfectly suits the requirement.
- () AWS Glue is primarily used for ETL jobs - cleaning, preparing, and moving data. Amazon Forecast is a fully managed service for time-series forecasting, which might not be a complete solution for detecting fraudulent transactions.
- () AWS Marketplace ML AMIs can be used to create and train models, but this will require manual operational effort in terms of setting up and managing the instances. Athena is a query service and does not provide data visualization capabilities that a business intelligence tool like QuickSight provides.

**Answer:**
Correct Answer: **Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization.**

---

## Question 19

**Q:** How should scaling be configured?

**Options:**
- (A) Use a simple scaling policy that launches instances when the average CPU hits 40%
- (B) Use a step scaling policy that uses the PercentChangeInCapacity value to adjust the group size as required
- (C) Use a target tracking policy that keeps the average aggregate CPU utilization at 40%
- (D) Use a custom CloudWatch alarm to monitor CPU usage and notify the ASG using Amazon SNS
- (E) This is a perfect use case for a target tracking scaling policy. With target tracking scaling policies, you select a scaling metric and set a target value. In this case you can just set the target value to 40% average aggregate CPU utilization.
- (F)  is the correct answer.
- (G)  is incorrect. A simple scaling policy will add instances when 40% CPU utilization is reached, but it is not designed to maintain 40% CPU utilization across the group.
- (H)  is incorrect. The step scaling policy makes scaling adjustments based on a number of factors. The PercentChangeInCapacity value increments or decrements the group size by a specified percentage. This does not relate to CPU utilization.
- (I)  is incorrect. You do not need to create a custom Amazon CloudWatch alarm as the ASG can scale using a policy based on CPU utilization using standard configuration.
- (J) References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2-auto-scaling/
- () AWS Compute
- () A financial institution wants to use machine learning (ML) algorithms to detect potential fraudulent transactions. They need to create ML models based on their vast financial transaction data and integrate these models into their business intelligence system for real-time decision-making. The solution should require minimal operational overhead.
- () Which solution will best meet these requirements?
- () Use Amazon Comprehend for analyzing the transaction data and Amazon Elasticsearch for visualization.
- **() Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization.** [CORRECT]
- () Use a pre-built ML Amazon Machine Image (AMI) from the AWS Marketplace to build and train models and use AWS Athena for data visualization.
- () 1. Use AWS Glue to perform ETL jobs on the transaction data and use Amazon Forecast for predictive analytics.
- () Amazon SageMaker is a fully managed service that provides every developer and data scientist with the ability to build, train, and deploy machine learning models quickly. It can directly connect with data sources and has built-in algorithms to ease the ML process.
- () Amazon QuickSight is a business intelligence tool that can be used to create dashboards for data visualization. This combination perfectly suits the requirement.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () AWS Glue is primarily used for ETL jobs - cleaning, preparing, and moving data. Amazon Forecast is a fully managed service for time-series forecasting, which might not be a complete solution for detecting fraudulent transactions.
- () AWS Marketplace ML AMIs can be used to create and train models, but this will require manual operational effort in terms of setting up and managing the instances. Athena is a query service and does not provide data visualization capabilities that a business intelligence tool like QuickSight provides.
- () Amazon Comprehend is primarily used for natural language processing (NLP), which isn't suited for detecting fraudulent transactions. Elasticsearch is a search and analytics engine and might not be the best tool for the use case described here.
- () https://aws.amazon.com/sagemaker/
- () https://digitalcloud.training/aws-machine-learning-services/
- () AWS Machine Learning
- () The Solutions Architect in charge of a critical application must ensure the Amazon EC2 instances are able to be launched in another AWS Region in the event of a disaster.
- () What steps should the Solutions Architect take? (Select TWO.)
- () Enable cross-region snapshots for the Amazon EC2 instances
- () Copy the snapshots using Amazon S3 cross-region replication
- () Launch instances in the second Region using the S3 API
- () Correct selection
- () Create AMIs of the instances and copy them to another Region
- () Launch instances in the second Region from the AMIs
- () You can create AMIs of the EC2 instances and then copy them across Regions. This provides a point-in-time copy of the state of the EC2 instance in the remote Region.
- () Once you’ve created AMIs of EC2 instances and copied them to the second Region, you can then launch the EC2 instances from the AMIs in that Region.
- () This is a good DR strategy as you have moved stateful EC2 instances to another Region.
- ()  is also a correct answer.

**Answer:**
Correct Answer: **Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization.**

---

## Question 20

**Q:** Which solution will best meet these requirements?

**Options:**
- (A) Use Amazon Comprehend for analyzing the transaction data and Amazon Elasticsearch for visualization.
- (B) Use Amazon SageMaker to build, train, and deploy ML models, and use Amazon QuickSight for data visualization.
- (C) Use a pre-built ML Amazon Machine Image (AMI) from the AWS Marketplace to build and train models and use AWS Athena for data visualization.
- (D) 1. Use AWS Glue to perform ETL jobs on the transaction data and use Amazon Forecast for predictive analytics.
- (E) Amazon SageMaker is a fully managed service that provides every developer and data scientist with the ability to build, train, and deploy machine learning models quickly. It can directly connect with data sources and has built-in algorithms to ease the ML process.
- (F) Amazon QuickSight is a business intelligence tool that can be used to create dashboards for data visualization. This combination perfectly suits the requirement.
- (G)  is the correct answer (as explained above.)
- (H)  is incorrect.
- (I) AWS Glue is primarily used for ETL jobs - cleaning, preparing, and moving data. Amazon Forecast is a fully managed service for time-series forecasting, which might not be a complete solution for detecting fraudulent transactions.
- (J) AWS Marketplace ML AMIs can be used to create and train models, but this will require manual operational effort in terms of setting up and managing the instances. Athena is a query service and does not provide data visualization capabilities that a business intelligence tool like QuickSight provides.
- () Amazon Comprehend is primarily used for natural language processing (NLP), which isn't suited for detecting fraudulent transactions. Elasticsearch is a search and analytics engine and might not be the best tool for the use case described here.
- () References:
- () https://aws.amazon.com/sagemaker/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-machine-learning-services/
- () AWS Machine Learning
- () The Solutions Architect in charge of a critical application must ensure the Amazon EC2 instances are able to be launched in another AWS Region in the event of a disaster.
- () What steps should the Solutions Architect take? (Select TWO.)
- () Enable cross-region snapshots for the Amazon EC2 instances
- () Copy the snapshots using Amazon S3 cross-region replication
- () Launch instances in the second Region using the S3 API
- () Correct selection
- () Create AMIs of the instances and copy them to another Region
- () Launch instances in the second Region from the AMIs
- () You can create AMIs of the EC2 instances and then copy them across Regions. This provides a point-in-time copy of the state of the EC2 instance in the remote Region.
- () Once you’ve created AMIs of EC2 instances and copied them to the second Region, you can then launch the EC2 instances from the AMIs in that Region.
- () This is a good DR strategy as you have moved stateful EC2 instances to another Region.
- ()  is the correct answer.
- ()  is also a correct answer.
- ()  is incorrect. Though snapshots (and EBS-backed AMIs) are stored on Amazon S3, you cannot actually access them using the S3 API. You must use the EC2 API.
- ()  is incorrect. You cannot enable “cross-region snapshots” as this is not a feature that currently exists.
- ()  is incorrect. You cannot work with snapshots using Amazon S3 at all including leveraging the cross-region replication feature.
- () https://aws.amazon.com/blogs/aws/ebs-snapshot-copy/
- () https://digitalcloud.training/amazon-ec2/
- () AWS Compute
- () A media company hosts several terabytes of multimedia content across multiple AWS accounts. The company uses AWS Lake Formation to manage its data lake. The company's marketing team needs to securely access and analyze selective data from various accounts for targeted advertisement campaigns.
- () Which solution will meet these requirements with the LEAST operational overhead?
- **() Utilize Lake Formation tag-based access control to authorize and grant cross-account permissions for the required data to the marketing team accounts.** [CORRECT]
- () Replicate the required data to a shared account. Create an IAM access role in that account. Grant access by defining a permission policy that includes users from the marketing team accounts as trusted entities.
- () Use the Lake Formation permissions Grant command in each account where the data is stored to permit the required marketing team users to access the data.
- () Use AWS DataSync to synchronize the necessary data to the marketing team accounts.
- () With Lake Formation tag-based access control, you can manage permissions using tags and grant cross-account permissions, which would meet the requirements with the least operational overhead.
- () This solution involves the unnecessary replication of data, leading to increased storage costs and operational overhead.

**Answer:**
Correct Answer: **Utilize Lake Formation tag-based access control to authorize and grant cross-account permissions for the required data to the marketing team accounts.**

---

## Question 21

**Q:** What steps should the Solutions Architect take? (Select TWO.)

**Options:**
- (A) Enable cross-region snapshots for the Amazon EC2 instances
- (B) Copy the snapshots using Amazon S3 cross-region replication
- (C) Launch instances in the second Region using the S3 API
- (D) Correct selection
- (E) Create AMIs of the instances and copy them to another Region
- (F) Launch instances in the second Region from the AMIs
- (G) You can create AMIs of the EC2 instances and then copy them across Regions. This provides a point-in-time copy of the state of the EC2 instance in the remote Region.
- (H) Once you’ve created AMIs of EC2 instances and copied them to the second Region, you can then launch the EC2 instances from the AMIs in that Region.
- (I) This is a good DR strategy as you have moved stateful EC2 instances to another Region.
- (J)  is the correct answer.
- ()  is also a correct answer.
- ()  is incorrect. Though snapshots (and EBS-backed AMIs) are stored on Amazon S3, you cannot actually access them using the S3 API. You must use the EC2 API.
- ()  is incorrect. You cannot enable “cross-region snapshots” as this is not a feature that currently exists.
- ()  is incorrect. You cannot work with snapshots using Amazon S3 at all including leveraging the cross-region replication feature.
- () References:
- () https://aws.amazon.com/blogs/aws/ebs-snapshot-copy/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2/
- () AWS Compute
- () A media company hosts several terabytes of multimedia content across multiple AWS accounts. The company uses AWS Lake Formation to manage its data lake. The company's marketing team needs to securely access and analyze selective data from various accounts for targeted advertisement campaigns.
- () Which solution will meet these requirements with the LEAST operational overhead?
- () Utilize Lake Formation tag-based access control to authorize and grant cross-account permissions for the required data to the marketing team accounts.
- () Replicate the required data to a shared account. Create an IAM access role in that account. Grant access by defining a permission policy that includes users from the marketing team accounts as trusted entities.
- () Use the Lake Formation permissions Grant command in each account where the data is stored to permit the required marketing team users to access the data.
- () Use AWS DataSync to synchronize the necessary data to the marketing team accounts.
- () With Lake Formation tag-based access control, you can manage permissions using tags and grant cross-account permissions, which would meet the requirements with the least operational overhead.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () This solution involves the unnecessary replication of data, leading to increased storage costs and operational overhead.
- () The Grant command would need to be manually executed in each account where data is stored, which could lead to increased operational overhead, particularly if the data is spread across many accounts.
- () AWS DataSync is designed for online data transfer, not for granting access permissions to data already stored in AWS, so this would not meet the requirement.
- () https://docs.aws.amazon.com/lake-formation/latest/dg/tag-based-access-control.html
- () AWS Storage
- () A company needs to store data from an application. Data in the application changes frequently. All levels of stored data must be audited under a new regulation which the company adheres to.
- () Application storage capacity is running out on the company's on-premises infrastructure. To comply with the new regulation, a solutions architect must offload some data securely to AWS to relieve the on-premises capacity issues.
- () Which solution will meet these requirements?
- **() Use AWS Storage Gateway to move the existing data to Amazon S3. Use AWS CloudTrail to log management events.** [CORRECT]
- () Move existing data to Amazon S3 using AWS DataSync. Log data events using AWS CloudTrail.
- () Move the existing data to Amazon S3 with AWS Snowcone. Using AWS CloudTrail, you can log management events.
- () The existing data can be transferred to Amazon S3 with the help of Amazon S3 Transfer Acceleration. Log data events using AWS CloudTrail.
- () AWS Storage Gateway is a set of hybrid cloud storage services that provide on-premises access to virtually unlimited cloud storage. Secondly AWS CloudTrail monitors and records account activity across your AWS infrastructure, giving you control over storage, analysis, and remediation actions.
- () Move existing data to Amazon S3 using AWS DataSync. Log data events using AWS CloudTrail” is incorrect. AWS DataSync is a secure, online service that automates and accelerates moving data between on-premises and AWS storage service and is not designed as a hybrid storage service.
- () The existing data can be transferred to Amazon S3 with the help of Amazon S3 Transfer Acceleration. Log data events using AWS CloudTrail” is incorrect. Amazon S3 Transfer Acceleration is a bucket-level feature that enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration is designed to optimize transfer speeds from across the world into S3 buckets and is not a migration service.
- ()  is incorrect. AWS Snowcone is not suitable as a hybrid cloud service.

**Answer:**
Correct Answer: **Use AWS Storage Gateway to move the existing data to Amazon S3. Use AWS CloudTrail to log management events.**

---

## Question 22

**Q:** A company runs a streaming media service and the content is stored on Amazon S3. The media catalog server pulls updated content from S3 and can issue over 1 million read operations per second for short periods. Latency must be kept under 5ms for these updates. Which solution will provide the BEST performance for the media catalog updates?

**Options:**
- (A) Implement an Instance store volume on the media catalog server
- (B) Implement Amazon CloudFront and cache the content at Edge Locations
- (C) Update the application code to use an Amazon DynamoDB Accelerator cluster
- (D) Update the application code to use an Amazon ElastiCache for Redis cluster
- (E) Some applications, such as media catalog updates require high frequency reads, and consistent throughput. For such applications, customers often complement S3 with an in-memory cache, such as Amazon ElastiCache for Redis, to reduce the S3 retrieval cost and to improve performance.
- (F) ElastiCache for Redis is a fully managed, in-memory data store that provides sub-millisecond latency performance with high throughput. ElastiCache for Redis complements S3 in the following ways:
- (G) - Redis stores data in-memory, so it provides sub-millisecond latency and supports incredibly high requests per second.
- (H) - It supports key/value based operations that map well to S3 operations (for example, GET/SET => GET/PUT), making it easy to write code for both S3 and ElastiCache.
- (I) - It can be implemented as an application side cache. This allows you to use S3 as your persistent store and benefit from its durability, availability, and low cost. Your applications decide what objects to cache, when to cache them, and how to cache them.
- (J) In this example the media catalog is pulling updates from S3 so the performance between these components is what needs to be improved. Therefore, using ElastiCache to cache the content will dramatically increase the performance.
- ()  is the correct answer.
- ()  is incorrect. CloudFront is good for getting media closer to users but in this case we’re trying to improve performance within the data center moving data from S3 to the media catalog server.
- ()  is incorrect. DynamoDB Accelerator (DAX) is used with DynamoDB but is unsuitable for use with Amazon S3.
- ()  is incorrect. This will improve local disk performance but will not improve reads from Amazon S3.
- () References:
- () https://aws.amazon.com/blogs/storage/turbocharge-amazon-s3-with-amazon-elasticache-for-redis/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-elasticache/
- () AWS Database
- () A healthcare company is migrating its patient record system to AWS. The company receives thousands of encrypted patient data files every day through FTP. An on-premises server processes the data files twice a day. However, the processing job takes hours to finish.
- () The company wants the AWS solution to process incoming data files as soon as they arrive with minimal changes to the FTP clients that send the files. The solution must delete the incoming data files after the files have been processed successfully. Processing for each file needs to take around 10 minutes.
- () Which solution will meet these requirements in the MOST operationally efficient way?
- () Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Standard. Use Amazon EC2 instances managed by an Auto Scaling group to process the files. Set an S3 event notification to trigger an AWS Lambda function that launches the EC2 instances when the files arrive. Delete the files after they are processed.
- () Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Standard. Create an AWS Lambda function to process the files and to delete the files after they are processed. Use an S3 event notification to invoke the Lambda function when the files arrive.
- () Use an Amazon EC2 instance that runs an SFTP server to store incoming files in Amazon S3 Standard. Configure a job queue in AWS Batch. Use Amazon EventBridge rules to invoke the job to process the files twice a day. Delete the files after the job has processed the files.
- () Use AWS Transfer Family to create an SFTP server to store incoming files in Amazon S3 Glacier. Configure an Amazon EC2 instance to process the files. Use Amazon EventBridge rules to invoke the EC2 instance to process the files twice a day from S3 Glacier. Delete the objects after the job has processed the objects.
- () AWS Transfer Family provides fully managed support for file transfers directly into and out of Amazon S3 using SFTP. Storing incoming files in S3 Standard offers high durability, availability, and performance object storage for frequently accessed data.
- () AWS Lambda can respond immediately to S3 events, which allows processing of files as soon as they arrive. Lambda can also delete the files after processing. This meets all requirements and is operationally efficient, as it requires minimal management and has low costs.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () This option involves using Amazon S3 Glacier, which is primarily used for long-term archival storage. Accessing data for processing could take longer and be more expensive than using S3 Standard. In addition, EC2 instances need to be managed and are less efficient for this scenario compared to AWS Lambda.
- () While this solution will work, it is less efficient operationally because managing EC2 instances and an Auto Scaling group is more complex and likely more expensive than simply using AWS Lambda for processing.
- () This option does not meet the requirement of processing incoming data files as soon as they arrive, as EventBridge rules would invoke the job only twice a day. It also involves managing an EC2 instance, which is less operationally efficient than the AWS Transfer Family and AWS Lambda option.
- () https://aws.amazon.com/aws-transfer-family/
- () https://digitalcloud.training/aws-migration-services/
- () AWS Migration & Transfer
- () A High Performance Computing (HPC) application needs storage that can provide 135,000 IOPS. The storage layer is replicated across all instances in a cluster.
- () What is the optimal storage solution that provides the required performance and is cost-effective?
- () Use Amazon EBS Provisioned IOPS volume with 135,000 IOPS
- **() Use Amazon Instance Store** [CORRECT]
- () Use Amazon EC2 Enhanced Networking with an EBS HDD Throughput Optimized volume
- () Use Amazon S3 with byte-range fetch
- () Instance stores offer very high performance and low latency. As long as you can afford to lose an instance, i.e. you are replicating your data, these can be a good solution for high performance/low latency requirements. Also, the cost of instance stores is included in the instance charges so it can also be more cost-effective than EBS Provisioned IOPS.
- ()  is incorrect. In the case of a HPC cluster that replicates data between nodes you don’t necessarily need a shared storage solution such as Amazon EBS Provisioned IOPS – this would also be a more expensive solution as the Instance Store is included in the cost of the HPC instance.

**Answer:**
Correct Answer: **Use Amazon Instance Store**

---

## Question 23

**Q:** What is the optimal storage solution that provides the required performance and is cost-effective?

**Options:**
- (A) Use Amazon EBS Provisioned IOPS volume with 135,000 IOPS
- (B) Use Amazon Instance Store
- (C) Use Amazon EC2 Enhanced Networking with an EBS HDD Throughput Optimized volume
- (D) Use Amazon S3 with byte-range fetch
- (E) Instance stores offer very high performance and low latency. As long as you can afford to lose an instance, i.e. you are replicating your data, these can be a good solution for high performance/low latency requirements. Also, the cost of instance stores is included in the instance charges so it can also be more cost-effective than EBS Provisioned IOPS.
- (F)  is the correct answer.
- (G)  is incorrect. In the case of a HPC cluster that replicates data between nodes you don’t necessarily need a shared storage solution such as Amazon EBS Provisioned IOPS – this would also be a more expensive solution as the Instance Store is included in the cost of the HPC instance.
- (H)  is incorrect. Amazon S3 is not a solution for this HPC application as in this case it will require block-based storage to provide the required IOPS.
- (I)  is incorrect
- (J) References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2/
- () https://digitalcloud.training/amazon-ebs/
- () AWS Storage
- () A company is developing a web-based application that will be used for real-time chat functionality. The application should use WebSocket APIs to maintain a persistent connection with the client. The backend services of the application, hosted in containers within private subnets of a VPC, need to be accessed securely.
- () Which solution will meet these requirements?
- () Develop a WebSocket API using Amazon API Gateway. Host the application in Amazon Elastic Kubernetes Service (EKS) in a private subnet. Establish a private VPC link for the API Gateway to securely access the Amazon EKS cluster.
- () Develop a REST API using Amazon API Gateway. Host the application in Amazon Elastic Kubernetes Service (EKS) in a private subnet. Create a security group that allows API Gateway to access the Amazon EKS cluster.
- () Develop a REST API using Amazon API Gateway. Host the application in Amazon Elastic Kubernetes Service (EKS) in a private subnet. Establish a private VPC link for the API Gateway to securely access the Amazon EKS cluster.
- () Develop a WebSocket API using Amazon API Gateway. Host the application in Amazon Elastic Kubernetes Service (EKS) in a private subnet. Create a security group that allows API Gateway to access the Amazon EKS cluster.
- () The requirement is for a real-time chat application, which makes the use of WebSocket APIs more suitable. Hosting the application in Amazon EKS within a private subnet allows secure and scalable management of the application. Creating a VPC link provides secure, private connectivity between API Gateway and the Amazon EKS service hosted inside the VPC.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () This solution does provide the secure hosting environment and private connectivity between API Gateway and the Amazon EKS cluster, but REST APIs are not suitable for real-time applications like a chat service. This is because REST APIs use request-response model which doesn't provide the continuous connection needed for real-time communication.
- () This option, while correctly suggesting the use of WebSocket APIs and Amazon EKS, proposes the use of a security group for connectivity. However, security groups act as a firewall for associated Amazon EC2 instances, controlling both inbound and outbound traffic at the instance level, while access to services within VPCs is more securely managed through VPC links.
- () REST APIs are not suitable for a real-time chat application. Also, managing access via a security group is not the most secure method for accessing services hosted within private subnets in a VPC.
- () https://docs.aws.amazon.com/whitepapers/latest/best-practices-api-gateway-private-apis-integration/websocket-api.html
- () https://digitalcloud.training/amazon-api-gateway/
- () AWS Networking & Content Delivery
- () A tool needs to analyze data stored in an Amazon S3 bucket. Processing the data takes a few seconds and results are then written to another S3 bucket. Less than 256 MB of memory is needed to run the process. What would be the MOST cost-effective compute solutions for this use case?
- **() AWS Lambda functions** [CORRECT]
- () Amazon Elastic Beanstalk
- () Amazon EC2 spot instances
- () AWS Fargate tasks
- () AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume. Lambda has a maximum execution time of 900 seconds and memory can be allocated up to 3008 MB. Therefore, the most cost-effective solution will be AWS Lambda.
- ()  is incorrect. Fargate runs Docker containers and is serverless. However, you do pay for the running time of the tasks so it will not be as cost-effective.
- ()  is incorrect. EC2 instances must run continually waiting for jobs to process so even with spot this would be less cost-effective (and subject to termination).
- ()  is incorrect. This services also relies on Amazon EC2 instances so would not be as cost-effective.
- () https://aws.amazon.com/lambda/
- () https://digitalcloud.training/aws-lambda/

**Answer:**
Correct Answer: **AWS Lambda functions**

---

## Question 24

**Q:** A tool needs to analyze data stored in an Amazon S3 bucket. Processing the data takes a few seconds and results are then written to another S3 bucket. Less than 256 MB of memory is needed to run the process. What would be the MOST cost-effective compute solutions for this use case?

**Options:**
- (A) AWS Lambda functions
- (B) Amazon Elastic Beanstalk
- (C) Amazon EC2 spot instances
- (D) AWS Fargate tasks
- (E) AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume. Lambda has a maximum execution time of 900 seconds and memory can be allocated up to 3008 MB. Therefore, the most cost-effective solution will be AWS Lambda.
- (F)  is the correct answer.
- (G)  is incorrect. Fargate runs Docker containers and is serverless. However, you do pay for the running time of the tasks so it will not be as cost-effective.
- (H)  is incorrect. EC2 instances must run continually waiting for jobs to process so even with spot this would be less cost-effective (and subject to termination).
- (I)  is incorrect. This services also relies on Amazon EC2 instances so would not be as cost-effective.
- (J) References:
- () https://aws.amazon.com/lambda/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-lambda/
- () AWS Compute
- () An application runs on EC2 instances in a private subnet behind an Application Load Balancer in a public subnet. The application is highly available and distributed across multiple AZs. The EC2 instances must make API calls to an internet-based service. How can the Solutions Architect enable highly available internet connectivity?
- () Configure an internet gateway. Add a route to the gateway to each private subnet route table
- () Create a NAT instance in the private subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT instance
- () Create a NAT gateway and attach it to the VPC. Add a route to the gateway to each private subnet route table
- () Create a NAT gateway in the public subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT gateway
- () The only solution presented that actually works is to create a NAT gateway in the public subnet of each AZ. They must be created in the public subnet as they gain public IP addresses and use an internet gateway for internet access.
- () The route tables in the private subnets must then be configured with a route to the NAT gateway and then the EC2 instances will be able to access the internet (subject to security group configuration).
- ()  is incorrect. You do not attach NAT gateways to VPCs, you add them to public subnets.
- ()  is incorrect. You cannot add a route to an internet gateway to a private subnet route table (private EC2 instances don’t even have public IP addresses).
- ()  is incorrect. You do not create NAT instances in private subnets, they must be created in public subnets.
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () https://digitalcloud.training/amazon-vpc/
- () A Solutions Architect is designing an application that will run on Amazon EC2 instances. The application will use Amazon S3 for storing image files and an Amazon DynamoDB table for storing customer information. The security team require that traffic between the EC2 instances and AWS services must not traverse the public internet.
- () How can the Solutions Architect meet the security team’s requirements?
- () Create a virtual private gateway and configure VPC route tables.
- **() Create gateway VPC endpoints for Amazon S3 and DynamoDB.** [CORRECT]
- () Create a NAT gateway in a public subnet and configure route tables.
- () Create interface VPC endpoints for Amazon S3 and DynamoDB.
- () A VPC endpoint enables private connections between your VPC and supported AWS services and VPC endpoint services powered by AWS PrivateLink. A gateway endpoint is used for Amazon S3 and Amazon DynamoDB. You specify a gateway endpoint as a route table target for traffic that is destined for the supported AWS services.
- ()  is incorrect. A NAT gateway is used for enabling internet connectivity for instances in private subnets. Connections will traverse the internet.
- ()  is incorrect. You should use a gateway VPC endpoint for S3 and DynamoDB.
- ()  is incorrect VGWs are used for VPN connections, they do not allow access to AWS services from a VPC.
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints.html
- () AWS Networking & Content Delivery
- () An e-commerce web application needs a highly scalable key-value database. Which AWS database service should be used?

**Answer:**
Correct Answer: **Create gateway VPC endpoints for Amazon S3 and DynamoDB.**

---

## Question 25

**Q:** An application runs on EC2 instances in a private subnet behind an Application Load Balancer in a public subnet. The application is highly available and distributed across multiple AZs. The EC2 instances must make API calls to an internet-based service. How can the Solutions Architect enable highly available internet connectivity?

**Options:**
- (A) Configure an internet gateway. Add a route to the gateway to each private subnet route table
- (B) Create a NAT instance in the private subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT instance
- (C) Create a NAT gateway and attach it to the VPC. Add a route to the gateway to each private subnet route table
- (D) Create a NAT gateway in the public subnet of each AZ. Update the route tables for each private subnet to direct internet-bound traffic to the NAT gateway
- (E) The only solution presented that actually works is to create a NAT gateway in the public subnet of each AZ. They must be created in the public subnet as they gain public IP addresses and use an internet gateway for internet access.
- (F) The route tables in the private subnets must then be configured with a route to the NAT gateway and then the EC2 instances will be able to access the internet (subject to security group configuration).
- (G)  is the correct answer.
- (H)  is incorrect. You do not attach NAT gateways to VPCs, you add them to public subnets.
- (I)  is incorrect. You cannot add a route to an internet gateway to a private subnet route table (private EC2 instances don’t even have public IP addresses).
- (J)  is incorrect. You do not create NAT instances in private subnets, they must be created in public subnets.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-vpc/
- () AWS Compute
- () A Solutions Architect is designing an application that will run on Amazon EC2 instances. The application will use Amazon S3 for storing image files and an Amazon DynamoDB table for storing customer information. The security team require that traffic between the EC2 instances and AWS services must not traverse the public internet.
- () How can the Solutions Architect meet the security team’s requirements?
- () Create a virtual private gateway and configure VPC route tables.
- () Create gateway VPC endpoints for Amazon S3 and DynamoDB.
- () Create a NAT gateway in a public subnet and configure route tables.
- () Create interface VPC endpoints for Amazon S3 and DynamoDB.
- () A VPC endpoint enables private connections between your VPC and supported AWS services and VPC endpoint services powered by AWS PrivateLink. A gateway endpoint is used for Amazon S3 and Amazon DynamoDB. You specify a gateway endpoint as a route table target for traffic that is destined for the supported AWS services.
- ()  is incorrect. A NAT gateway is used for enabling internet connectivity for instances in private subnets. Connections will traverse the internet.
- ()  is incorrect. You should use a gateway VPC endpoint for S3 and DynamoDB.
- ()  is incorrect VGWs are used for VPN connections, they do not allow access to AWS services from a VPC.
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints.html
- () AWS Networking & Content Delivery
- () An e-commerce web application needs a highly scalable key-value database. Which AWS database service should be used?
- () Amazon RDS
- () Amazon ElastiCache
- **() Amazon DynamoDB** [CORRECT]
- () Amazon RedShift
- () A key-value database is a type of nonrelational (NoSQL) database that uses a simple key-value method to store data. A key-value database stores data as a collection of key-value pairs in which a key serves as a unique identifier. Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability – this is the best database for these requirements.
- ()  is incorrect. Amazon RDS is a relational (SQL) type of database, not a key-value / nonrelational database.
- ()  is incorrect. Amazon RedShift is a data warehouse service used for online analytics processing (OLAP) workloads.
- ()  is incorrect. Amazon ElastiCache is an in-memory caching database. This is not a nonrelational key-value database.
- () https://aws.amazon.com/nosql/key-value/
- () https://digitalcloud.training/amazon-dynamodb/
- () AWS Database
- () A corporation has a web-based multiplayer gaming service that operates using both TCP and UDP protocols. Amazon Route 53 is currently employed to direct application traffic to a set of Network Load Balancers (NLBs) in various AWS Regions. To prepare for an increase in user activity, the company must enhance application performance and reduce latency.

**Answer:**
Correct Answer: **Amazon DynamoDB**

---

## Question 26

**Q:** How can the Solutions Architect meet the security team’s requirements?

**Options:**
- (A) Create a virtual private gateway and configure VPC route tables.
- (B) Create gateway VPC endpoints for Amazon S3 and DynamoDB.
- (C) Create a NAT gateway in a public subnet and configure route tables.
- (D) Create interface VPC endpoints for Amazon S3 and DynamoDB.
- (E) A VPC endpoint enables private connections between your VPC and supported AWS services and VPC endpoint services powered by AWS PrivateLink. A gateway endpoint is used for Amazon S3 and Amazon DynamoDB. You specify a gateway endpoint as a route table target for traffic that is destined for the supported AWS services.
- (F)  is the correct answer.
- (G)  is incorrect. A NAT gateway is used for enabling internet connectivity for instances in private subnets. Connections will traverse the internet.
- (H)  is incorrect. You should use a gateway VPC endpoint for S3 and DynamoDB.
- (I)  is incorrect VGWs are used for VPN connections, they do not allow access to AWS services from a VPC.
- (J) References:
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-vpc/
- () AWS Networking & Content Delivery
- () An e-commerce web application needs a highly scalable key-value database. Which AWS database service should be used?
- () Amazon RDS
- () Amazon ElastiCache
- () Amazon DynamoDB
- () Amazon RedShift
- () A key-value database is a type of nonrelational (NoSQL) database that uses a simple key-value method to store data. A key-value database stores data as a collection of key-value pairs in which a key serves as a unique identifier. Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability – this is the best database for these requirements.
- ()  is incorrect. Amazon RDS is a relational (SQL) type of database, not a key-value / nonrelational database.
- ()  is incorrect. Amazon RedShift is a data warehouse service used for online analytics processing (OLAP) workloads.
- ()  is incorrect. Amazon ElastiCache is an in-memory caching database. This is not a nonrelational key-value database.
- () https://aws.amazon.com/nosql/key-value/
- () https://digitalcloud.training/amazon-dynamodb/
- () AWS Database
- () A corporation has a web-based multiplayer gaming service that operates using both TCP and UDP protocols. Amazon Route 53 is currently employed to direct application traffic to a set of Network Load Balancers (NLBs) in various AWS Regions. To prepare for an increase in user activity, the company must enhance application performance and reduce latency.
- () Which approach will best meet these requirements?
- () Substitute the NLBs with Application Load Balancers (ALBs) and set Route 53 to utilize latency-based routing.
- **() Implement AWS Global Accelerator ahead of the NLBs and align the Global Accelerator endpoint to use the appropriate listener ports.** [CORRECT]
- () Insert an Amazon API Gateway endpoint behind the NLBs, enable API caching, and customize method caching across different stages.
- () Incorporate Amazon CloudFront in front of the NLBs and extend the duration of the Cache-Control max-age directive.
- () AWS Global Accelerator is designed to improve the availability and performance of your applications for local and global users. It directs traffic to optimal endpoints over the AWS global network, thus enhancing the performance of your TCP and UDP traffic by routing packets through the AWS global network infrastructure, reducing jitter, and improving overall game performance.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () Amazon CloudFront is a content delivery network (CDN) that speeds up the delivery of your static and dynamic web content. While it could potentially help with application performance, it doesn't directly improve TCP/UDP performance, which is the specific requirement in this case.
- () While the API Gateway would add more control and security to the application, the caching feature is not necessarily beneficial for this real-time gaming scenario where the content is likely to change frequently and unpredictably.
- () https://aws.amazon.com/global-accelerator/
- () https://digitalcloud.training/aws-global-accelerator/

**Answer:**
Correct Answer: **Implement AWS Global Accelerator ahead of the NLBs and align the Global Accelerator endpoint to use the appropriate listener ports.**

---

## Question 27

**Q:** An e-commerce web application needs a highly scalable key-value database. Which AWS database service should be used?

**Options:**
- (A) Amazon RDS
- (B) Amazon ElastiCache
- (C) Amazon DynamoDB
- (D) Amazon RedShift
- (E) A key-value database is a type of nonrelational (NoSQL) database that uses a simple key-value method to store data. A key-value database stores data as a collection of key-value pairs in which a key serves as a unique identifier. Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability – this is the best database for these requirements.
- (F)  is the correct answer.
- (G)  is incorrect. Amazon RDS is a relational (SQL) type of database, not a key-value / nonrelational database.
- (H)  is incorrect. Amazon RedShift is a data warehouse service used for online analytics processing (OLAP) workloads.
- (I)  is incorrect. Amazon ElastiCache is an in-memory caching database. This is not a nonrelational key-value database.
- (J) References:
- () https://aws.amazon.com/nosql/key-value/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-dynamodb/
- () AWS Database
- () A corporation has a web-based multiplayer gaming service that operates using both TCP and UDP protocols. Amazon Route 53 is currently employed to direct application traffic to a set of Network Load Balancers (NLBs) in various AWS Regions. To prepare for an increase in user activity, the company must enhance application performance and reduce latency.
- () Which approach will best meet these requirements?
- () Substitute the NLBs with Application Load Balancers (ALBs) and set Route 53 to utilize latency-based routing.
- () Implement AWS Global Accelerator ahead of the NLBs and align the Global Accelerator endpoint to use the appropriate listener ports.
- () Insert an Amazon API Gateway endpoint behind the NLBs, enable API caching, and customize method caching across different stages.
- () Incorporate Amazon CloudFront in front of the NLBs and extend the duration of the Cache-Control max-age directive.
- () AWS Global Accelerator is designed to improve the availability and performance of your applications for local and global users. It directs traffic to optimal endpoints over the AWS global network, thus enhancing the performance of your TCP and UDP traffic by routing packets through the AWS global network infrastructure, reducing jitter, and improving overall game performance.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () Amazon CloudFront is a content delivery network (CDN) that speeds up the delivery of your static and dynamic web content. While it could potentially help with application performance, it doesn't directly improve TCP/UDP performance, which is the specific requirement in this case.
- () While the API Gateway would add more control and security to the application, the caching feature is not necessarily beneficial for this real-time gaming scenario where the content is likely to change frequently and unpredictably.
- () https://aws.amazon.com/global-accelerator/
- () https://digitalcloud.training/aws-global-accelerator/
- () AWS Networking & Content Delivery
- () A web application in a three-tier architecture runs on a fleet of Amazon EC2 instances. Performance issues have been reported and investigations point to insufficient swap space. The operations team requires monitoring to determine if this is correct.
- () What should a solutions architect recommend?
- () Enable detailed monitoring in the EC2 console. Create an Amazon CloudWatch SwapUtilization custom metric. Monitor SwapUtilization metrics in CloudWatch
- **() Install an Amazon CloudWatch agent on the instances. Run an appropriate script on a set schedule. Monitor SwapUtilization metrics in CloudWatch** [CORRECT]
- () Configure an Amazon CloudWatch SwapUsage metric dimension. Monitor the SwapUsage dimension in the EC2 metrics in CloudWatch
- () Use EC2 metadata to collect information, then publish it to Amazon CloudWatch custom metrics. Monitor SwapUsage metrics in CloudWatch
- () You can use the CloudWatch agent to collect both system metrics and log files from Amazon EC2 instances and on-premises servers. The agent supports both Windows Server and Linux, and enables you to select the metrics to be collected, including sub-resource metrics such as per-CPU core.
- () There is now a unified agent and previously there were monitoring scripts. Both of these tools can capture SwapUtilization metrics and send them to CloudWatch. This is the best way to get memory utilization metrics from Amazon EC2 instnaces.
- ()  is incorrect as you do not create custom metrics in the console, you must configure the instances to send the metric information to CloudWatch.
- ()  is incorrect as there is no SwapUsage metric in CloudWatch. All memory metrics must be custom metrics.
- ()  is incorrect as performance related information is not stored in metadata.
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html
- () https://digitalcloud.training/amazon-cloudwatch/

**Answer:**
Correct Answer: **Install an Amazon CloudWatch agent on the instances. Run an appropriate script on a set schedule. Monitor SwapUtilization metrics in CloudWatch**

---

## Question 28

**Q:** Which approach will best meet these requirements?

**Options:**
- (A) Substitute the NLBs with Application Load Balancers (ALBs) and set Route 53 to utilize latency-based routing.
- (B) Implement AWS Global Accelerator ahead of the NLBs and align the Global Accelerator endpoint to use the appropriate listener ports.
- (C) Insert an Amazon API Gateway endpoint behind the NLBs, enable API caching, and customize method caching across different stages.
- (D) Incorporate Amazon CloudFront in front of the NLBs and extend the duration of the Cache-Control max-age directive.
- (E) AWS Global Accelerator is designed to improve the availability and performance of your applications for local and global users. It directs traffic to optimal endpoints over the AWS global network, thus enhancing the performance of your TCP and UDP traffic by routing packets through the AWS global network infrastructure, reducing jitter, and improving overall game performance.
- (F)  is the correct answer (as explained above.)
- (G)  is incorrect.
- (H) Amazon CloudFront is a content delivery network (CDN) that speeds up the delivery of your static and dynamic web content. While it could potentially help with application performance, it doesn't directly improve TCP/UDP performance, which is the specific requirement in this case.
- (I) While the API Gateway would add more control and security to the application, the caching feature is not necessarily beneficial for this real-time gaming scenario where the content is likely to change frequently and unpredictably.
- (J) References:
- () https://aws.amazon.com/global-accelerator/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-global-accelerator/
- () AWS Networking & Content Delivery
- () A web application in a three-tier architecture runs on a fleet of Amazon EC2 instances. Performance issues have been reported and investigations point to insufficient swap space. The operations team requires monitoring to determine if this is correct.
- () What should a solutions architect recommend?
- () Enable detailed monitoring in the EC2 console. Create an Amazon CloudWatch SwapUtilization custom metric. Monitor SwapUtilization metrics in CloudWatch
- () Install an Amazon CloudWatch agent on the instances. Run an appropriate script on a set schedule. Monitor SwapUtilization metrics in CloudWatch
- () Configure an Amazon CloudWatch SwapUsage metric dimension. Monitor the SwapUsage dimension in the EC2 metrics in CloudWatch
- () Use EC2 metadata to collect information, then publish it to Amazon CloudWatch custom metrics. Monitor SwapUsage metrics in CloudWatch
- () You can use the CloudWatch agent to collect both system metrics and log files from Amazon EC2 instances and on-premises servers. The agent supports both Windows Server and Linux, and enables you to select the metrics to be collected, including sub-resource metrics such as per-CPU core.
- () There is now a unified agent and previously there were monitoring scripts. Both of these tools can capture SwapUtilization metrics and send them to CloudWatch. This is the best way to get memory utilization metrics from Amazon EC2 instnaces.
- ()  is the correct answer.
- ()  is incorrect as you do not create custom metrics in the console, you must configure the instances to send the metric information to CloudWatch.
- ()  is incorrect as there is no SwapUsage metric in CloudWatch. All memory metrics must be custom metrics.
- ()  is incorrect as performance related information is not stored in metadata.
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html
- () https://digitalcloud.training/amazon-cloudwatch/
- () AWS Management & Governance
- () A company operates a production web application that uses an Amazon RDS MySQL database. The database has automated, non-encrypted daily backups. To increase the security of the data, it has been recommended that encryption should be enabled for backups. Unencrypted backups will be destroyed after the first encrypted backup has been completed.
- () What should be done to enable encryption for future backups?
- **() Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot** [CORRECT]
- () Enable default encryption for the Amazon S3 bucket where backups are stored
- () Modify the backup section of the database configuration to toggle the Enable encryption check box
- () Enable an encrypted read replica on RDS for MySQL. Promote the encrypted read replica to primary. Remove the original database instance
- () Amazon RDS uses snapshots for backup. Snapshots are encrypted when created only if the database is encrypted and you can only select encryption for the database when you first create it. In this case the database, and hence the snapshots, ad unencrypted.
- () However, you can create an encrypted copy of a snapshot. You can restore using that snapshot which creates a new DB instance that has encryption enabled. From that point on encryption will be enabled for all snapshots.
- ()  is incorrect as you cannot create an encrypted read replica from an unencrypted master.
- ()  is incorrect as you cannot add encryption for an existing database.
- ()  is incorrect because you do not have access to the S3 bucket in which snapshots are stored.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html

**Answer:**
Correct Answer: **Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot**

---

## Question 29

**Q:** What should be done to enable encryption for future backups?

**Options:**
- (A) Create a snapshot of the database. Copy it to an encrypted snapshot. Restore the database from the encrypted snapshot
- (B) Enable default encryption for the Amazon S3 bucket where backups are stored
- (C) Modify the backup section of the database configuration to toggle the Enable encryption check box
- (D) Enable an encrypted read replica on RDS for MySQL. Promote the encrypted read replica to primary. Remove the original database instance
- (E) Amazon RDS uses snapshots for backup. Snapshots are encrypted when created only if the database is encrypted and you can only select encryption for the database when you first create it. In this case the database, and hence the snapshots, ad unencrypted.
- (F) However, you can create an encrypted copy of a snapshot. You can restore using that snapshot which creates a new DB instance that has encryption enabled. From that point on encryption will be enabled for all snapshots.
- (G)  is the correct answer.
- (H)  is incorrect as you cannot create an encrypted read replica from an unencrypted master.
- (I)  is incorrect as you cannot add encryption for an existing database.
- (J)  is incorrect because you do not have access to the S3 bucket in which snapshots are stored.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-rds/
- () AWS Compute
- () A company is deploying an analytics application on AWS Fargate. The application requires connected storage that offers concurrent access to files and high performance.
- () Which storage option should the solutions architect recommend?
- **() 1. Create an Amazon EFS file share and establish an IAM role that allows Fargate to communicate with Amazon EFS.** [CORRECT]
- () 1. Create an Amazon S3 bucket for the application and establish an IAM role for Fargate to communicate with Amazon S3.
- () 1. Create an Amazon EBS volume for the application and establish an IAM role that allows Fargate to communicate with Amazon EBS.
- () 1. Create an Amazon FSx for Lustre file share and establish an IAM role that allows Fargate to communicate with FSx for Lustre.
- () The Amazon Elastic File System offers concurrent access to a shared file system and provides high performance. You can create file system policies for controlling access and then use an IAM role that is specified in the policy for access.
- ()  is incorrect. S3 uses a REST API not a file system API so access can be shared but is not concurrent.
- ()  is incorrect. EBS volumes cannot be shared amongst Fargate tasks, they are used with EC2 instances.
- ()  is incorrect. It is not supported to connect Fargate to FSx for Lustre.
- () https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html
- () https://digitalcloud.training/amazon-efs/
- () AWS Storage
- () A solutions architect has created a new AWS account and must secure AWS account root user access.
- () Which combination of actions will accomplish this? (Select TWO.)
- () Correct selection
- () Ensure the root user uses a strong password
- () Store root user access keys in an encrypted Amazon S3 bucket
- () 1. Delete the root user account
- () Enable multi-factor authentication to the root user
- () Add the root user to a group containing administrative permissions
- () There are several security best practices for securing the root user account:
- () · Lock away root user access keys OR delete them if possible
- () · Use a strong password
- () · Enable multi-factor authentication (MFA)
- () The root user automatically has full privileges to the account and these privileges cannot be restricted so it is extremely important to follow best practice advice about securing the root user account.
- ()  is incorrect as the best practice is to lock away or delete the root user access keys. An S3 bucket is not a suitable location for storing them, even if encrypted.
- ()  is incorrect as this does not restrict access and is unnecessary.
- ()  is incorrect as you cannot delete the root user account.

**Answer:**
Correct Answer: **1. Create an Amazon EFS file share and establish an IAM role that allows Fargate to communicate with Amazon EFS.**

---

## Question 30

**Q:** Which storage option should the solutions architect recommend?

**Options:**
- **(A) 1. Create an Amazon EFS file share and establish an IAM role that allows Fargate to communicate with Amazon EFS.** [CORRECT]
- (B) 1. Create an Amazon S3 bucket for the application and establish an IAM role for Fargate to communicate with Amazon S3.
- (C) 1. Create an Amazon EBS volume for the application and establish an IAM role that allows Fargate to communicate with Amazon EBS.
- (D) 1. Create an Amazon FSx for Lustre file share and establish an IAM role that allows Fargate to communicate with FSx for Lustre.
- (E) The Amazon Elastic File System offers concurrent access to a shared file system and provides high performance. You can create file system policies for controlling access and then use an IAM role that is specified in the policy for access.
- (F)  is the correct answer.
- (G)  is incorrect. S3 uses a REST API not a file system API so access can be shared but is not concurrent.
- (H)  is incorrect. EBS volumes cannot be shared amongst Fargate tasks, they are used with EC2 instances.
- (I)  is incorrect. It is not supported to connect Fargate to FSx for Lustre.
- (J) References:
- () https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-efs/
- () AWS Storage
- () A solutions architect has created a new AWS account and must secure AWS account root user access.
- () Which combination of actions will accomplish this? (Select TWO.)
- () Correct selection
- () Ensure the root user uses a strong password
- () Store root user access keys in an encrypted Amazon S3 bucket
- () 1. Delete the root user account
- () Enable multi-factor authentication to the root user
- () Add the root user to a group containing administrative permissions
- () There are several security best practices for securing the root user account:
- () · Lock away root user access keys OR delete them if possible
- () · Use a strong password
- () · Enable multi-factor authentication (MFA)
- () The root user automatically has full privileges to the account and these privileges cannot be restricted so it is extremely important to follow best practice advice about securing the root user account.
- ()  is incorrect as the best practice is to lock away or delete the root user access keys. An S3 bucket is not a suitable location for storing them, even if encrypted.
- ()  is incorrect as this does not restrict access and is unnecessary.
- ()  is incorrect as you cannot delete the root user account.
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html
- () https://digitalcloud.training/aws-iam/
- () AWS Security, Identity, & Compliance

**Answer:**
Correct Answer: **1. Create an Amazon EFS file share and establish an IAM role that allows Fargate to communicate with Amazon EFS.**

---

## Question 31

**Q:** Which combination of actions will accomplish this? (Select TWO.)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Ensure the root user uses a strong password
- (C) Store root user access keys in an encrypted Amazon S3 bucket
- (D) 1. Delete the root user account
- (E) Enable multi-factor authentication to the root user
- (F) Add the root user to a group containing administrative permissions
- (G) There are several security best practices for securing the root user account:
- (H) · Lock away root user access keys OR delete them if possible
- (I) · Use a strong password
- (J) · Enable multi-factor authentication (MFA)
- () The root user automatically has full privileges to the account and these privileges cannot be restricted so it is extremely important to follow best practice advice about securing the root user account.
- ()  is the correct answer.
- ()  is incorrect as the best practice is to lock away or delete the root user access keys. An S3 bucket is not a suitable location for storing them, even if encrypted.
- ()  is incorrect as this does not restrict access and is unnecessary.
- ()  is incorrect as you cannot delete the root user account.
- () References:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-iam/
- () AWS Security, Identity, & Compliance

**Answer:**
Correct Answer: **Correct selection**

---

## Question 32

**Q:** An application makes calls to a REST API running on Amazon EC2 instances behind an Application Load Balancer (ALB). Most API calls complete quickly. However, a single endpoint is making API calls that require much longer to complete and this is introducing overall latency into the system. What steps can a Solutions Architect take to minimize the effects of the long-running API calls?

**Options:**
- (A) Increase the ALB idle timeout to allow the long-running requests to complete
- (B) Change the ALB to a Network Load Balancer (NLB) and use SSL/TLS termination
- (C) Change the EC2 instance to one with enhanced networking to reduce latency
- (D) Create an Amazon SQS queue and decouple the long-running API calls
- (E) An Amazon Simple Queue Service (SQS) can be used to offload and decouple the long-running requests. They can then be processed asynchronously by separate EC2 instances. This is the best way to reduce the overall latency introduced by the long-running API call.
- (F)  is the correct answer.
- (G)  is incorrect. This will not reduce the latency of the API call as network latency is not the issue here, it is the latency of how long the API call takes to complete.
- (H)  is incorrect. The issue is not the connection being interrupted, it is that the API call takes a long time to complete.
- (I)  is incorrect. SSL/TLS termination is not of benefit here as the problem is not encryption or processing of encryption. The issue is API call latency.
- (J) References:
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-application-integration-services/
- () AWS Application Integration
- () A company is looking for ways to incorporate its current AWS usage expenditure into its operational expense tracking dashboard. A solutions architect has been tasked with proposing a method that enables the company to fetch its current year's cost data and project the costs for the forthcoming 12 months programmatically.
- () Which approach would fulfill these needs with the MINIMUM operational burden?
- () Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets.
- () Generate AWS Budgets reports on usage cost data and dispatch the data to the corporation through SMTP.
- () Set up AWS Budgets actions to transmit usage cost data to the corporation via FTP.
- () Make use of downloadable AWS Cost Explorer report files in the .csv format to access usage cost-related data.
- () AWS Cost Explorer API provides programmatic access to AWS cost and usage information. The user can query for aggregated data such as total monthly costs or total daily usage with this API.
- () Also, the Cost Explorer API supports pagination for managing larger data sets, making it efficient for larger queries.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () While AWS Cost Explorer does allow you to download .csv reports of your cost data, this method would not be programmatically accessible and would involve manual steps to download and process the data.
- () AWS Budgets actions allow you to set custom cost and usage budgets that trigger actions (such as turning off EC2 instances) when the budget thresholds you set are breached. However, AWS Budgets does not support transmitting data via FTP.
- () AWS Budgets does not support the dispatching of data through SMTP. AWS Budgets is primarily a tool for setting up alerts on your AWS costs or usage to control your costs, rather than a tool for exporting or transmitting cost data.
- () https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_Operations_AWS_Cost_Explorer_Service.html
- () https://digitalcloud.training/aws-cost-management/
- () AWS Management & Governance
- () An application allows users to upload and download files. Files older than 2 years will be accessed less frequently. A solutions architect needs to ensure that the application can scale to any number of files while maintaining high availability and durability.
- () Which scalable solutions should the solutions architect recommend?
- () Store the files in Amazon Elastic Block Store (EBS) volumes. Schedule snapshots of the volumes. Use the snapshots to archive data older than 2 years
- () Store the files in Amazon Elastic Block Store (EBS) volumes. Create a lifecycle policy to move files older than 2 years to Amazon S3 Glacier
- () Store the files on Amazon Elastic File System (EFS) with a lifecycle policy that moves objects older than 2 years to EFS Infrequent Access (EFS IA)
- **() Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)** [CORRECT]
- () S3 Standard-IA is for data that is accessed less frequently, but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval fee. This combination of low cost and high performance make S3 Standard-IA ideal for long-term storage, backups, and as a data store for disaster recovery files.
- ()  is incorrect. With EFS you can transition files to EFS IA after a file has not been accessed for a specified period of time with options up to 90 days. You cannot transition based on an age of 2 years.
- ()  is incorrect. You cannot identify the age of data and archive snapshots in this way with EBS.
- ()  is incorrect. You cannot archive files from an EBS volume to Glacier using lifecycle policies.
- () https://aws.amazon.com/s3/storage-classes/
- () https://digitalcloud.training/amazon-s3-and-glacier/

**Answer:**
Correct Answer: **Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)**

---

## Question 33

**Q:** Which approach would fulfill these needs with the MINIMUM operational burden?

**Options:**
- (A) Leverage the AWS Cost Explorer API to retrieve usage cost-related data, using pagination for larger data sets.
- (B) Generate AWS Budgets reports on usage cost data and dispatch the data to the corporation through SMTP.
- (C) Set up AWS Budgets actions to transmit usage cost data to the corporation via FTP.
- (D) Make use of downloadable AWS Cost Explorer report files in the .csv format to access usage cost-related data.
- (E) AWS Cost Explorer API provides programmatic access to AWS cost and usage information. The user can query for aggregated data such as total monthly costs or total daily usage with this API.
- (F) Also, the Cost Explorer API supports pagination for managing larger data sets, making it efficient for larger queries.
- (G)  is the correct answer (as explained above.)
- (H)  is incorrect.
- (I) While AWS Cost Explorer does allow you to download .csv reports of your cost data, this method would not be programmatically accessible and would involve manual steps to download and process the data.
- (J) AWS Budgets actions allow you to set custom cost and usage budgets that trigger actions (such as turning off EC2 instances) when the budget thresholds you set are breached. However, AWS Budgets does not support transmitting data via FTP.
- () AWS Budgets does not support the dispatching of data through SMTP. AWS Budgets is primarily a tool for setting up alerts on your AWS costs or usage to control your costs, rather than a tool for exporting or transmitting cost data.
- () References:
- () https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_Operations_AWS_Cost_Explorer_Service.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-cost-management/
- () AWS Management & Governance
- () An application allows users to upload and download files. Files older than 2 years will be accessed less frequently. A solutions architect needs to ensure that the application can scale to any number of files while maintaining high availability and durability.
- () Which scalable solutions should the solutions architect recommend?
- () Store the files in Amazon Elastic Block Store (EBS) volumes. Schedule snapshots of the volumes. Use the snapshots to archive data older than 2 years
- () Store the files in Amazon Elastic Block Store (EBS) volumes. Create a lifecycle policy to move files older than 2 years to Amazon S3 Glacier
- () Store the files on Amazon Elastic File System (EFS) with a lifecycle policy that moves objects older than 2 years to EFS Infrequent Access (EFS IA)
- () Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)
- () S3 Standard-IA is for data that is accessed less frequently, but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval fee. This combination of low cost and high performance make S3 Standard-IA ideal for long-term storage, backups, and as a data store for disaster recovery files.
- ()  is the correct answer.
- ()  is incorrect. With EFS you can transition files to EFS IA after a file has not been accessed for a specified period of time with options up to 90 days. You cannot transition based on an age of 2 years.
- ()  is incorrect. You cannot identify the age of data and archive snapshots in this way with EBS.
- ()  is incorrect. You cannot archive files from an EBS volume to Glacier using lifecycle policies.
- () https://aws.amazon.com/s3/storage-classes/
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () AWS Storage
- () An application runs on Amazon EC2 instances backed by Amazon EBS volumes and an Amazon RDS database. The application is highly sensitive and security compliance requirements mandate that all personally identifiable information (PII) be encrypted at rest.
- () Which solution should a Solutions Architect choose to this requirement?
- () Deploy AWS CloudHSM, generate encryption keys, and use the customer master key (CMK) to encrypt database volumes.
- () Enable encryption on Amazon RDS during creation. Use Amazon Macie to identify sensitive data.
- **() Configure Amazon EBS encryption and Amazon RDS encryption with AWS KMS keys to encrypt instance and database volumes.** [CORRECT]
- () Configure SSL/TLS encryption using AWS KMS customer master keys (CMKs) to encrypt database volumes.
- () The data must be encrypted at rest on both the EC2 instance’s attached EBS volumes and the RDS database. Both storage locations can be encrypted using AWS KMS keys. With RDS, KMS uses a customer master key (CMK) to encrypt the DB instance, all logs, backups, and snapshots.
- ()  is incorrect. This does not encrypt the EBS volumes attached to the EC2 instance and Macie cannot be used with RDS.
- ()  is incorrect. SSL encryption encrypts data in transit but not at rest.
- ()  is incorrect. CloudHSM is not required for this solution, and we need to encrypt the database volumes and the EBS volumes.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- () https://digitalcloud.training/amazon-rds/

**Answer:**
Correct Answer: **Configure Amazon EBS encryption and Amazon RDS encryption with AWS KMS keys to encrypt instance and database volumes.**

---

## Question 34

**Q:** Which scalable solutions should the solutions architect recommend?

**Options:**
- (A) Store the files in Amazon Elastic Block Store (EBS) volumes. Schedule snapshots of the volumes. Use the snapshots to archive data older than 2 years
- (B) Store the files in Amazon Elastic Block Store (EBS) volumes. Create a lifecycle policy to move files older than 2 years to Amazon S3 Glacier
- (C) Store the files on Amazon Elastic File System (EFS) with a lifecycle policy that moves objects older than 2 years to EFS Infrequent Access (EFS IA)
- (D) Store the files on Amazon S3 with a lifecycle policy that moves objects older than 2 years to S3 Standard Infrequent Access (S3 Standard-IA)
- (E) S3 Standard-IA is for data that is accessed less frequently, but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval fee. This combination of low cost and high performance make S3 Standard-IA ideal for long-term storage, backups, and as a data store for disaster recovery files.
- (F)  is the correct answer.
- (G)  is incorrect. With EFS you can transition files to EFS IA after a file has not been accessed for a specified period of time with options up to 90 days. You cannot transition based on an age of 2 years.
- (H)  is incorrect. You cannot identify the age of data and archive snapshots in this way with EBS.
- (I)  is incorrect. You cannot archive files from an EBS volume to Glacier using lifecycle policies.
- (J) References:
- () https://aws.amazon.com/s3/storage-classes/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () AWS Storage
- () An application runs on Amazon EC2 instances backed by Amazon EBS volumes and an Amazon RDS database. The application is highly sensitive and security compliance requirements mandate that all personally identifiable information (PII) be encrypted at rest.
- () Which solution should a Solutions Architect choose to this requirement?
- () Deploy AWS CloudHSM, generate encryption keys, and use the customer master key (CMK) to encrypt database volumes.
- () Enable encryption on Amazon RDS during creation. Use Amazon Macie to identify sensitive data.
- () Configure Amazon EBS encryption and Amazon RDS encryption with AWS KMS keys to encrypt instance and database volumes.
- () Configure SSL/TLS encryption using AWS KMS customer master keys (CMKs) to encrypt database volumes.
- () The data must be encrypted at rest on both the EC2 instance’s attached EBS volumes and the RDS database. Both storage locations can be encrypted using AWS KMS keys. With RDS, KMS uses a customer master key (CMK) to encrypt the DB instance, all logs, backups, and snapshots.
- ()  is incorrect. This does not encrypt the EBS volumes attached to the EC2 instance and Macie cannot be used with RDS.
- ()  is incorrect. SSL encryption encrypts data in transit but not at rest.
- ()  is incorrect. CloudHSM is not required for this solution, and we need to encrypt the database volumes and the EBS volumes.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- () https://digitalcloud.training/amazon-rds/
- () AWS Security, Identity, & Compliance
- () Three AWS accounts are owned by the same company but in different regions. Account Z has two AWS Direct Connect connections to two separate company offices. Accounts A and B require the ability to route across account Z’s Direct Connect connections to each company office. A Solutions Architect has created an AWS Direct Connect gateway in account Z.
- () How can the required connectivity be configured?
- () Associate the Direct Connect gateway to a transit gateway in each region
- () Create a VPC Endpoint to the Direct Connect gateway in account A and B
- () Create a PrivateLink connection in Account Z and ENIs in accounts A and B
- **() Associate the Direct Connect gateway to a virtual private gateway in account A and B** [CORRECT]
- () You can associate an AWS Direct Connect gateway with either of the following gateways:
- () - A transit gateway when you have multiple VPCs in the same Region.
- () - A virtual private gateway.
- () In this case account Z owns the Direct Connect gateway so a VPG in accounts A and B must be associated with it to enable this configuration to work. After Account Z accepts the proposals, Account A and Account B can route traffic from their virtual private gateway to the Direct Connect gateway.
- ()  is incorrect. This would be a good solution if the accounts were in VPCs within a region rather than across regions.
- ()  is incorrect. You cannot create a VPC endpoint for Direct Connect gateways.
- ()  is incorrect. You cannot use PrivateLink connections to publish a Direct Connect gateway.
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html

**Answer:**
Correct Answer: **Associate the Direct Connect gateway to a virtual private gateway in account A and B**

---

## Question 35

**Q:** Which solution should a Solutions Architect choose to this requirement?

**Options:**
- (A) Deploy AWS CloudHSM, generate encryption keys, and use the customer master key (CMK) to encrypt database volumes.
- (B) Enable encryption on Amazon RDS during creation. Use Amazon Macie to identify sensitive data.
- (C) Configure Amazon EBS encryption and Amazon RDS encryption with AWS KMS keys to encrypt instance and database volumes.
- (D) Configure SSL/TLS encryption using AWS KMS customer master keys (CMKs) to encrypt database volumes.
- (E) The data must be encrypted at rest on both the EC2 instance’s attached EBS volumes and the RDS database. Both storage locations can be encrypted using AWS KMS keys. With RDS, KMS uses a customer master key (CMK) to encrypt the DB instance, all logs, backups, and snapshots.
- (F)  is the correct answer.
- (G)  is incorrect. This does not encrypt the EBS volumes attached to the EC2 instance and Macie cannot be used with RDS.
- (H)  is incorrect. SSL encryption encrypts data in transit but not at rest.
- (I)  is incorrect. CloudHSM is not required for this solution, and we need to encrypt the database volumes and the EBS volumes.
- (J) References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-rds/
- () AWS Security, Identity, & Compliance
- () Three AWS accounts are owned by the same company but in different regions. Account Z has two AWS Direct Connect connections to two separate company offices. Accounts A and B require the ability to route across account Z’s Direct Connect connections to each company office. A Solutions Architect has created an AWS Direct Connect gateway in account Z.
- () How can the required connectivity be configured?
- () Associate the Direct Connect gateway to a transit gateway in each region
- () Create a VPC Endpoint to the Direct Connect gateway in account A and B
- () Create a PrivateLink connection in Account Z and ENIs in accounts A and B
- () Associate the Direct Connect gateway to a virtual private gateway in account A and B
- () You can associate an AWS Direct Connect gateway with either of the following gateways:
- () - A transit gateway when you have multiple VPCs in the same Region.
- () - A virtual private gateway.
- () In this case account Z owns the Direct Connect gateway so a VPG in accounts A and B must be associated with it to enable this configuration to work. After Account Z accepts the proposals, Account A and Account B can route traffic from their virtual private gateway to the Direct Connect gateway.
- ()  is incorrect. This would be a good solution if the accounts were in VPCs within a region rather than across regions.
- ()  is incorrect. You cannot create a VPC endpoint for Direct Connect gateways.
- ()  is incorrect. You cannot use PrivateLink connections to publish a Direct Connect gateway.
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
- () https://digitalcloud.training/aws-direct-connect/
- () AWS Networking & Content Delivery
- () The database layer of an on-premises web application is being migrated to AWS. The database currently uses an in-memory cache. A Solutions Architect must deliver a solution that supports high availability and replication for the caching layer.
- () Which service should the Solutions Architect recommend?
- () Amazon RDS Multi-AZ
- **() Amazon ElastiCache Redis** [CORRECT]
- () Amazon DynamoDB
- () Amazon ElastiCache Memcached
- () Amazon ElastiCache Redis is an in-memory database cache and supports high availability through replicas and multi-AZ. The table below compares ElastiCache Redis with Memcached:
- ()  is incorrect as it does not support high availability or multi-AZ.
- ()  is incorrect. This is not an in-memory database and it not suitable for use as a caching layer.
- ()  is incorrect. DynamoDB is a non-relational database. You would not use it for a caching layer. Also, the in-memory, low-latency caching for DynamoDB is implemented using DynamoDB Accelerator (DAX).

**Answer:**
Correct Answer: **Amazon ElastiCache Redis**

---

## Question 36

**Q:** How can the required connectivity be configured?

**Options:**
- (A) Associate the Direct Connect gateway to a transit gateway in each region
- (B) Create a VPC Endpoint to the Direct Connect gateway in account A and B
- (C) Create a PrivateLink connection in Account Z and ENIs in accounts A and B
- (D) Associate the Direct Connect gateway to a virtual private gateway in account A and B
- (E) You can associate an AWS Direct Connect gateway with either of the following gateways:
- (F) - A transit gateway when you have multiple VPCs in the same Region.
- (G) - A virtual private gateway.
- (H) In this case account Z owns the Direct Connect gateway so a VPG in accounts A and B must be associated with it to enable this configuration to work. After Account Z accepts the proposals, Account A and Account B can route traffic from their virtual private gateway to the Direct Connect gateway.
- (I)  is the correct answer.
- (J)  is incorrect. This would be a good solution if the accounts were in VPCs within a region rather than across regions.
- ()  is incorrect. You cannot create a VPC endpoint for Direct Connect gateways.
- ()  is incorrect. You cannot use PrivateLink connections to publish a Direct Connect gateway.
- () References:
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-direct-connect/
- () AWS Networking & Content Delivery
- () The database layer of an on-premises web application is being migrated to AWS. The database currently uses an in-memory cache. A Solutions Architect must deliver a solution that supports high availability and replication for the caching layer.
- () Which service should the Solutions Architect recommend?
- () Amazon RDS Multi-AZ
- () Amazon ElastiCache Redis
- () Amazon DynamoDB
- () Amazon ElastiCache Memcached
- () Amazon ElastiCache Redis is an in-memory database cache and supports high availability through replicas and multi-AZ. The table below compares ElastiCache Redis with Memcached:
- ()  is incorrect as it does not support high availability or multi-AZ.
- ()  is incorrect. This is not an in-memory database and it not suitable for use as a caching layer.
- ()  is incorrect. DynamoDB is a non-relational database. You would not use it for a caching layer. Also, the in-memory, low-latency caching for DynamoDB is implemented using DynamoDB Accelerator (DAX).
- () https://aws.amazon.com/elasticache/redis-vs-memcached/
- () https://digitalcloud.training/amazon-elasticache/
- () AWS Database
- () A solutions architect is designing a high performance computing (HPC) application using Amazon EC2 Linux instances. All EC2 instances need to communicate to each other with low latency and high throughput network performance.
- () Which EC2 solution BEST meets these requirements?
- () Launch the EC2 instances in an Auto Scaling group spanning multiple Availability Zones
- **() Launch the EC2 instances in a cluster placement group in one Availability Zone** [CORRECT]
- () Launch the EC2 instances in a spread placement group in one Availability Zone
- () Launch the EC2 instances in an Auto Scaling group in two Regions. Place a Network Load Balancer in front of the instances
- () When you launch a new EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload. Depending on the type of workload, you can create a placement group using one of the following placement strategies:
- () Cluster – packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of HPC applications.
- () Partition – spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka.
- () Spread – strictly places a small group of instances across distinct underlying hardware to reduce correlated failures.
- () For this scenario, a cluster placement group should be used as this is the best option for providing low-latency network performance for a HPC application.

**Answer:**
Correct Answer: **Launch the EC2 instances in a cluster placement group in one Availability Zone**

---

## Question 37

**Q:** Which service should the Solutions Architect recommend?

**Options:**
- (A) Amazon RDS Multi-AZ
- (B) Amazon ElastiCache Redis
- (C) Amazon DynamoDB
- (D) Amazon ElastiCache Memcached
- (E) Amazon ElastiCache Redis is an in-memory database cache and supports high availability through replicas and multi-AZ. The table below compares ElastiCache Redis with Memcached:
- (F)  is the correct answer.
- (G)  is incorrect as it does not support high availability or multi-AZ.
- (H)  is incorrect. This is not an in-memory database and it not suitable for use as a caching layer.
- (I)  is incorrect. DynamoDB is a non-relational database. You would not use it for a caching layer. Also, the in-memory, low-latency caching for DynamoDB is implemented using DynamoDB Accelerator (DAX).
- (J) References:
- () https://aws.amazon.com/elasticache/redis-vs-memcached/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-elasticache/
- () AWS Database
- () A solutions architect is designing a high performance computing (HPC) application using Amazon EC2 Linux instances. All EC2 instances need to communicate to each other with low latency and high throughput network performance.
- () Which EC2 solution BEST meets these requirements?
- () Launch the EC2 instances in an Auto Scaling group spanning multiple Availability Zones
- () Launch the EC2 instances in a cluster placement group in one Availability Zone
- () Launch the EC2 instances in a spread placement group in one Availability Zone
- () Launch the EC2 instances in an Auto Scaling group in two Regions. Place a Network Load Balancer in front of the instances
- () When you launch a new EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload. Depending on the type of workload, you can create a placement group using one of the following placement strategies:
- () Cluster – packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of HPC applications.
- () Partition – spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka.
- () Spread – strictly places a small group of instances across distinct underlying hardware to reduce correlated failures.
- () For this scenario, a cluster placement group should be used as this is the best option for providing low-latency network performance for a HPC application.
- ()  is incorrect as the spread placement group is used to spread instances across distinct underlying hardware.
- ()  is incorrect as this does not achieve the stated requirement to provide low-latency, high throughput network performance between instances. Also, you cannot use an ELB across Regions.
- ()  is incorrect as this does not reduce network latency or improve performance.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () https://digitalcloud.training/amazon-ec2/
- () AWS Compute
- () A company has several AWS accounts that are used by developers for development, testing and pre-production environments. The company has received large bills for Amazon EC2 instances that are underutilized. A Solutions Architect has been tasked with restricting the ability to launch large EC2 instances in all accounts.
- () How can the Solutions Architect meet this requirement with the LEAST operational overhead?
- **() Create an organization in AWS Organizations that includes all accounts and create a service control policy (SCP) that denies the launch of large EC2 instances.** [CORRECT]
- () Create an IAM role in each account that denies the launch of large EC2 instances. Grant the developers IAM group access to the role.
- () Create a service-linked role for Amazon EC2 and attach a policy the denies the launch of large EC2 instances.
- () Create a resource-based policy that denies the launch of large EC2 instances and attach it to Amazon EC2 in each account.
- () Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. An SCP defines a guardrail, or sets limits, on the actions that the account's administrator can delegate to the IAM users and roles in the affected accounts.
- () In this case the Solutions Architect can use an SCP to define a restriction that denies the launch of large EC2 instances. The SCP can be applied to all accounts, and this will ensure that even those users with permissions to launch EC2 instances will be restricted to smaller EC2 instance types.
- ()  is incorrect. You cannot create service-linked roles yourself; they are created by AWS with predefined policies.
- ()  is incorrect. You cannot attach a resource-based policy to Amazon EC2.
- ()  is incorrect. This is much less operationally efficient compared to using SCPs with AWS Organizations.

**Answer:**
Correct Answer: **Create an organization in AWS Organizations that includes all accounts and create a service control policy (SCP) that denies the launch of large EC2 instances.**

---

## Question 38

**Q:** Which EC2 solution BEST meets these requirements?

**Options:**
- (A) Launch the EC2 instances in an Auto Scaling group spanning multiple Availability Zones
- (B) Launch the EC2 instances in a cluster placement group in one Availability Zone
- (C) Launch the EC2 instances in a spread placement group in one Availability Zone
- (D) Launch the EC2 instances in an Auto Scaling group in two Regions. Place a Network Load Balancer in front of the instances
- (E) When you launch a new EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload. Depending on the type of workload, you can create a placement group using one of the following placement strategies:
- (F) Cluster – packs instances close together inside an Availability Zone. This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of HPC applications.
- (G) Partition – spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka.
- (H) Spread – strictly places a small group of instances across distinct underlying hardware to reduce correlated failures.
- (I) For this scenario, a cluster placement group should be used as this is the best option for providing low-latency network performance for a HPC application.
- (J)  is the correct answer.
- ()  is incorrect as the spread placement group is used to spread instances across distinct underlying hardware.
- ()  is incorrect as this does not achieve the stated requirement to provide low-latency, high throughput network performance between instances. Also, you cannot use an ELB across Regions.
- ()  is incorrect as this does not reduce network latency or improve performance.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2/
- () AWS Compute
- () A company has several AWS accounts that are used by developers for development, testing and pre-production environments. The company has received large bills for Amazon EC2 instances that are underutilized. A Solutions Architect has been tasked with restricting the ability to launch large EC2 instances in all accounts.
- () How can the Solutions Architect meet this requirement with the LEAST operational overhead?
- () Create an organization in AWS Organizations that includes all accounts and create a service control policy (SCP) that denies the launch of large EC2 instances.
- () Create an IAM role in each account that denies the launch of large EC2 instances. Grant the developers IAM group access to the role.
- () Create a service-linked role for Amazon EC2 and attach a policy the denies the launch of large EC2 instances.
- () Create a resource-based policy that denies the launch of large EC2 instances and attach it to Amazon EC2 in each account.
- () Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. An SCP defines a guardrail, or sets limits, on the actions that the account's administrator can delegate to the IAM users and roles in the affected accounts.
- () In this case the Solutions Architect can use an SCP to define a restriction that denies the launch of large EC2 instances. The SCP can be applied to all accounts, and this will ensure that even those users with permissions to launch EC2 instances will be restricted to smaller EC2 instance types.
- ()  is incorrect. You cannot create service-linked roles yourself; they are created by AWS with predefined policies.
- ()  is incorrect. You cannot attach a resource-based policy to Amazon EC2.
- ()  is incorrect. This is much less operationally efficient compared to using SCPs with AWS Organizations.
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () https://digitalcloud.training/aws-organizations/
- () AWS Management & Governance
- () An on-premises server runs a MySQL database and will be migrated to the AWS Cloud. The company require a managed solution that supports high availability and automatic failover in the event of the outage of an Availability Zone (AZ).
- () Which solution is the BEST fit for these requirements?
- **() Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment** [CORRECT]
- () Use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon RDS MySQL. Use the Schema Conversion Tool (SCT) to enable conversion from MySQL to Amazon RDS
- () Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon EC2 MySQL Multi-AZ deployment
- () Create a snapshot of the MySQL database server and use AWS DataSync to migrate the data Amazon S3. Launch a new Amazon RDS MySQL Multi-AZ deployment from the snapshot
- () The AWS DMS service can be used to directly migrate the MySQL database to an Amazon RDS Multi-AZ deployment. The entire process can be online and is managed for you. There is no need to perform schema translation between MySQL and RDS (assuming you choose the MySQL RDS engine).
- ()  is incorrect as there is no such thing as “multi-AZ” on Amazon EC2 with MySQL, you must use RDS.
- ()  is incorrect. You cannot create a snapshot of a MySQL database server running on-premises.
- ()  is incorrect. There is no need to convert the schema when migrating from MySQL to Amazon RDS (MySQL engine).

**Answer:**
Correct Answer: **Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment**

---

## Question 39

**Q:** How can the Solutions Architect meet this requirement with the LEAST operational overhead?

**Options:**
- (A) Create an organization in AWS Organizations that includes all accounts and create a service control policy (SCP) that denies the launch of large EC2 instances.
- (B) Create an IAM role in each account that denies the launch of large EC2 instances. Grant the developers IAM group access to the role.
- (C) Create a service-linked role for Amazon EC2 and attach a policy the denies the launch of large EC2 instances.
- (D) Create a resource-based policy that denies the launch of large EC2 instances and attach it to Amazon EC2 in each account.
- (E) Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. An SCP defines a guardrail, or sets limits, on the actions that the account's administrator can delegate to the IAM users and roles in the affected accounts.
- (F) In this case the Solutions Architect can use an SCP to define a restriction that denies the launch of large EC2 instances. The SCP can be applied to all accounts, and this will ensure that even those users with permissions to launch EC2 instances will be restricted to smaller EC2 instance types.
- (G)  is the correct answer.
- (H)  is incorrect. You cannot create service-linked roles yourself; they are created by AWS with predefined policies.
- (I)  is incorrect. You cannot attach a resource-based policy to Amazon EC2.
- (J)  is incorrect. This is much less operationally efficient compared to using SCPs with AWS Organizations.
- () References:
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-organizations/
- () AWS Management & Governance
- () An on-premises server runs a MySQL database and will be migrated to the AWS Cloud. The company require a managed solution that supports high availability and automatic failover in the event of the outage of an Availability Zone (AZ).
- () Which solution is the BEST fit for these requirements?
- () Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment
- () Use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon RDS MySQL. Use the Schema Conversion Tool (SCT) to enable conversion from MySQL to Amazon RDS
- () Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon EC2 MySQL Multi-AZ deployment
- () Create a snapshot of the MySQL database server and use AWS DataSync to migrate the data Amazon S3. Launch a new Amazon RDS MySQL Multi-AZ deployment from the snapshot
- () The AWS DMS service can be used to directly migrate the MySQL database to an Amazon RDS Multi-AZ deployment. The entire process can be online and is managed for you. There is no need to perform schema translation between MySQL and RDS (assuming you choose the MySQL RDS engine).
- ()  is incorrect as there is no such thing as “multi-AZ” on Amazon EC2 with MySQL, you must use RDS.
- ()  is incorrect. You cannot create a snapshot of a MySQL database server running on-premises.
- ()  is incorrect. There is no need to convert the schema when migrating from MySQL to Amazon RDS (MySQL engine).
- () https://aws.amazon.com/rds/features/multi-az/
- () https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.html
- () https://digitalcloud.training/amazon-rds/
- () https://digitalcloud.training/aws-migration-services/
- () AWS Migration & Transfer
- () An application uses a MySQL database running on an Amazon EC2 instance. The application generates high I/O and constant writes to a single table on the database. Which Amazon EBS volume type will provide the MOST consistent performance and low latency?
- () Cold HDD (sc1)
- () General Purpose SSD (gp2)
- **() Provisioned IOPS SSD (io1)** [CORRECT]
- () Throughput Optimized HDD (st1)
- () The Provisioned IOPS SSD (io1) volume type will offer the most consistent performance and can be configured with the amount of IOPS required by the application. It will also provide the lowest latency of the options presented.
- ()  is incorrect. This is not the best solution for when you require high I/O, consistent performance and low latency.
- ()  is incorrect. This is a HDD type of disk and not suitable for low latency workloads that require consistent performance.
- ()  is incorrect. This is the lowest cost option and not suitable for frequently accessed workloads.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html

**Answer:**
Correct Answer: **Provisioned IOPS SSD (io1)**

---

## Question 40

**Q:** Which solution is the BEST fit for these requirements?

**Options:**
- (A) Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon RDS MySQL Multi-AZ deployment
- (B) Use the AWS Database Migration Service (DMS) to directly migrate the database to Amazon RDS MySQL. Use the Schema Conversion Tool (SCT) to enable conversion from MySQL to Amazon RDS
- (C) Use the AWS Database Migration Service (DMS) to directly migrate the database to an Amazon EC2 MySQL Multi-AZ deployment
- (D) Create a snapshot of the MySQL database server and use AWS DataSync to migrate the data Amazon S3. Launch a new Amazon RDS MySQL Multi-AZ deployment from the snapshot
- (E) The AWS DMS service can be used to directly migrate the MySQL database to an Amazon RDS Multi-AZ deployment. The entire process can be online and is managed for you. There is no need to perform schema translation between MySQL and RDS (assuming you choose the MySQL RDS engine).
- (F)  is the correct answer.
- (G)  is incorrect as there is no such thing as “multi-AZ” on Amazon EC2 with MySQL, you must use RDS.
- (H)  is incorrect. You cannot create a snapshot of a MySQL database server running on-premises.
- (I)  is incorrect. There is no need to convert the schema when migrating from MySQL to Amazon RDS (MySQL engine).
- (J) References:
- () https://aws.amazon.com/rds/features/multi-az/
- () https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Introduction.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-rds/
- () https://digitalcloud.training/aws-migration-services/
- () AWS Migration & Transfer
- () An application uses a MySQL database running on an Amazon EC2 instance. The application generates high I/O and constant writes to a single table on the database. Which Amazon EBS volume type will provide the MOST consistent performance and low latency?
- () Cold HDD (sc1)
- () General Purpose SSD (gp2)
- () Provisioned IOPS SSD (io1)
- () Throughput Optimized HDD (st1)
- () The Provisioned IOPS SSD (io1) volume type will offer the most consistent performance and can be configured with the amount of IOPS required by the application. It will also provide the lowest latency of the options presented.
- ()  is incorrect. This is not the best solution for when you require high I/O, consistent performance and low latency.
- ()  is incorrect. This is a HDD type of disk and not suitable for low latency workloads that require consistent performance.
- ()  is incorrect. This is the lowest cost option and not suitable for frequently accessed workloads.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () https://digitalcloud.training/amazon-ebs/
- () AWS Compute
- () A company is planning to use Amazon S3 to store documents uploaded by its customers. The images must be encrypted at rest in Amazon S3. The company does not want to spend time managing and rotating the keys, but it does want to control who can access those keys.
- () What should a solutions architect use to accomplish this?
- () Server-Side Encryption with keys stored in an S3 bucket
- **() Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)** [CORRECT]
- () Server-Side Encryption with Customer-Provided Keys (SSE-C)
- () Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)
- () SSE-KMS requires that AWS manage the data key but you manage the customer master key (CMK) in AWS KMS. You can choose a customer managed CMK or the AWS managed CMK for Amazon S3 in your account.
- () Customer managed CMKs are CMKs in your AWS account that you create, own, and manage. You have full control over these CMKs, including establishing and maintaining their key policies, IAM policies, and grants, enabling and disabling them, rotating their cryptographic material, adding tags, creating aliases that refer to the CMK, and scheduling the CMKs for deletion.
- () For this scenario, the solutions architect should use SSE-KMS with a customer managed CMK. That way KMS will manage the data key but the company can configure key policies defining who can access the keys.
- ()  is incorrect as you cannot store your keys in a bucket with server-side encryption
- ()  is incorrect as the company does not want to manage the keys.
- ()  is incorrect as the company needs to manage access control for the keys which is not possible when they’re managed by Amazon.

**Answer:**
Correct Answer: **Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)**

---

## Question 41

**Q:** An application uses a MySQL database running on an Amazon EC2 instance. The application generates high I/O and constant writes to a single table on the database. Which Amazon EBS volume type will provide the MOST consistent performance and low latency?

**Options:**
- (A) Cold HDD (sc1)
- (B) General Purpose SSD (gp2)
- (C) Provisioned IOPS SSD (io1)
- (D) Throughput Optimized HDD (st1)
- (E) The Provisioned IOPS SSD (io1) volume type will offer the most consistent performance and can be configured with the amount of IOPS required by the application. It will also provide the lowest latency of the options presented.
- (F)  is the correct answer.
- (G)  is incorrect. This is not the best solution for when you require high I/O, consistent performance and low latency.
- (H)  is incorrect. This is a HDD type of disk and not suitable for low latency workloads that require consistent performance.
- (I)  is incorrect. This is the lowest cost option and not suitable for frequently accessed workloads.
- (J) References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ebs/
- () AWS Compute
- () A company is planning to use Amazon S3 to store documents uploaded by its customers. The images must be encrypted at rest in Amazon S3. The company does not want to spend time managing and rotating the keys, but it does want to control who can access those keys.
- () What should a solutions architect use to accomplish this?
- () Server-Side Encryption with keys stored in an S3 bucket
- **() Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)** [CORRECT]
- () Server-Side Encryption with Customer-Provided Keys (SSE-C)
- () Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)
- () SSE-KMS requires that AWS manage the data key but you manage the customer master key (CMK) in AWS KMS. You can choose a customer managed CMK or the AWS managed CMK for Amazon S3 in your account.
- () Customer managed CMKs are CMKs in your AWS account that you create, own, and manage. You have full control over these CMKs, including establishing and maintaining their key policies, IAM policies, and grants, enabling and disabling them, rotating their cryptographic material, adding tags, creating aliases that refer to the CMK, and scheduling the CMKs for deletion.
- () For this scenario, the solutions architect should use SSE-KMS with a customer managed CMK. That way KMS will manage the data key but the company can configure key policies defining who can access the keys.
- ()  is incorrect as you cannot store your keys in a bucket with server-side encryption
- ()  is incorrect as the company does not want to manage the keys.
- ()  is incorrect as the company needs to manage access control for the keys which is not possible when they’re managed by Amazon.
- () https://docs.aws.amazon.com/kms/latest/developerguide/services-s3.html#sse
- () https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () https://digitalcloud.training/aws-kms/
- () AWS Storage
- () A software development company is deploying a microservices-based application on Amazon Elastic Kubernetes Service (Amazon EKS). The application's traffic fluctuates significantly throughout the day and the company wants to ensure that the EKS cluster scales up and down according to these traffic patterns.
- () Which combination of steps would satisfy these requirements with MINIMAL operational overhead? (Select TWO.)
- () Correct selection
- () Utilize the Kubernetes Metrics Server to enable horizontal pod autoscaling based on resource utilization.
- () Leverage AWS X-Ray to track and analyze the application's network activity.
- () Integrate Amazon SQS and connect it to Amazon EKS for workload management.
- () Implement the Kubernetes Vertical Pod Autoscaler to adjust the CPU and memory allocation for the pods.
- () Employ the Kubernetes Cluster Autoscaler for dynamically managing the quantity of nodes in the EKS cluster.
- () The Metrics Server collects resource metrics like CPU and memory usage from each node and its pods and provides these metrics to the Kubernetes API server for use by the Horizontal Pod Autoscaler, which automatically scales the number of pods in a deployment, replication controller, replica set, or stateful set based on observed CPU utilization.
- () The Kubernetes Cluster Autoscaler automatically adjusts the size of the Kubernetes cluster when there are pods that failed to run in the cluster due to insufficient resources or when there are nodes in the cluster that have been underutilized for an extended period and their pods can be placed on other existing nodes.
- ()  is a correct answer (as explained above.)
- ()  is also a correct answer (as explained above.)
- ()  is incorrect.

**Answer:**
Correct Answer: **Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)**

---

## Question 42

**Q:** What should a solutions architect use to accomplish this?

**Options:**
- (A) Server-Side Encryption with keys stored in an S3 bucket
- (B) Server-Side Encryption with AWS KMS-Managed Keys (SSE-KMS)
- (C) Server-Side Encryption with Customer-Provided Keys (SSE-C)
- (D) Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3)
- (E) SSE-KMS requires that AWS manage the data key but you manage the customer master key (CMK) in AWS KMS. You can choose a customer managed CMK or the AWS managed CMK for Amazon S3 in your account.
- (F) Customer managed CMKs are CMKs in your AWS account that you create, own, and manage. You have full control over these CMKs, including establishing and maintaining their key policies, IAM policies, and grants, enabling and disabling them, rotating their cryptographic material, adding tags, creating aliases that refer to the CMK, and scheduling the CMKs for deletion.
- (G) For this scenario, the solutions architect should use SSE-KMS with a customer managed CMK. That way KMS will manage the data key but the company can configure key policies defining who can access the keys.
- (H)  is the correct answer.
- (I)  is incorrect as you cannot store your keys in a bucket with server-side encryption
- (J)  is incorrect as the company does not want to manage the keys.
- ()  is incorrect as the company needs to manage access control for the keys which is not possible when they’re managed by Amazon.
- () References:
- () https://docs.aws.amazon.com/kms/latest/developerguide/services-s3.html#sse
- () https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () https://digitalcloud.training/aws-kms/
- () AWS Storage
- () A software development company is deploying a microservices-based application on Amazon Elastic Kubernetes Service (Amazon EKS). The application's traffic fluctuates significantly throughout the day and the company wants to ensure that the EKS cluster scales up and down according to these traffic patterns.
- () Which combination of steps would satisfy these requirements with MINIMAL operational overhead? (Select TWO.)
- () Correct selection
- () Utilize the Kubernetes Metrics Server to enable horizontal pod autoscaling based on resource utilization.
- () Leverage AWS X-Ray to track and analyze the application's network activity.
- () Integrate Amazon SQS and connect it to Amazon EKS for workload management.
- () Implement the Kubernetes Vertical Pod Autoscaler to adjust the CPU and memory allocation for the pods.
- () Employ the Kubernetes Cluster Autoscaler for dynamically managing the quantity of nodes in the EKS cluster.
- () The Metrics Server collects resource metrics like CPU and memory usage from each node and its pods and provides these metrics to the Kubernetes API server for use by the Horizontal Pod Autoscaler, which automatically scales the number of pods in a deployment, replication controller, replica set, or stateful set based on observed CPU utilization.
- () The Kubernetes Cluster Autoscaler automatically adjusts the size of the Kubernetes cluster when there are pods that failed to run in the cluster due to insufficient resources or when there are nodes in the cluster that have been underutilized for an extended period and their pods can be placed on other existing nodes.
- ()  is a correct answer (as explained above.)
- ()  is also a correct answer (as explained above.)
- ()  is incorrect.
- () The Vertical Pod Autoscaler adjusts the resources of the pods and not the number of pods or nodes, which won't directly help with scaling according to traffic patterns.
- () Amazon SQS is a message queuing service, and while it can be used to manage workloads by decoupling microservices, it doesn't directly help with autoscaling an EKS cluster based on traffic patterns.
- () AWS X-Ray provides insights into the behavior of your applications, but it doesn't directly help with autoscaling an EKS cluster.
- () https://kubernetes.io/docs/tasks/debug/debug-cluster/resource-metrics-pipeline/#metrics-server
- () https://docs.aws.amazon.com/eks/latest/userguide/autoscaling.html
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Compute
- () A production application runs on an Amazon RDS MySQL DB instance. A solutions architect is building a new reporting tool that will access the same data. The reporting tool must be highly available and not impact the performance of the production application.
- () How can this be achieved?
- () Use Amazon Data Lifecycle Manager to automatically create and manage snapshots
- () Create a Single-AZ RDS Read Replica of the production RDS DB instance. Create a second Single-AZ RDS Read Replica from the replica
- () Create a cross-region Multi-AZ deployment and create a read replica in the second region
- **() Create a Multi-AZ RDS Read Replica of the production RDS DB instance** [CORRECT]
- () You can create a read replica as a Multi-AZ DB instance. Amazon RDS creates a standby of your replica in another Availability Zone for failover support for the replica. Creating your read replica as a Multi-AZ DB instance is independent of whether the source database is a Multi-AZ DB instance.

**Answer:**
Correct Answer: **Create a Multi-AZ RDS Read Replica of the production RDS DB instance**

---

## Question 43

**Q:** Which combination of steps would satisfy these requirements with MINIMAL operational overhead? (Select TWO.)

**Options:**
- (A) Correct selection
- (B) Utilize the Kubernetes Metrics Server to enable horizontal pod autoscaling based on resource utilization.
- (C) Leverage AWS X-Ray to track and analyze the application's network activity.
- (D) Integrate Amazon SQS and connect it to Amazon EKS for workload management.
- (E) Implement the Kubernetes Vertical Pod Autoscaler to adjust the CPU and memory allocation for the pods.
- (F) Employ the Kubernetes Cluster Autoscaler for dynamically managing the quantity of nodes in the EKS cluster.
- (G) The Metrics Server collects resource metrics like CPU and memory usage from each node and its pods and provides these metrics to the Kubernetes API server for use by the Horizontal Pod Autoscaler, which automatically scales the number of pods in a deployment, replication controller, replica set, or stateful set based on observed CPU utilization.
- (H) The Kubernetes Cluster Autoscaler automatically adjusts the size of the Kubernetes cluster when there are pods that failed to run in the cluster due to insufficient resources or when there are nodes in the cluster that have been underutilized for an extended period and their pods can be placed on other existing nodes.
- (I)  is a correct answer (as explained above.)
- (J)  is also a correct answer (as explained above.)
- ()  is incorrect.
- () The Vertical Pod Autoscaler adjusts the resources of the pods and not the number of pods or nodes, which won't directly help with scaling according to traffic patterns.
- () Amazon SQS is a message queuing service, and while it can be used to manage workloads by decoupling microservices, it doesn't directly help with autoscaling an EKS cluster based on traffic patterns.
- () AWS X-Ray provides insights into the behavior of your applications, but it doesn't directly help with autoscaling an EKS cluster.
- () References:
- () https://kubernetes.io/docs/tasks/debug/debug-cluster/resource-metrics-pipeline/#metrics-server
- () https://docs.aws.amazon.com/eks/latest/userguide/autoscaling.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ecs-and-eks/
- () AWS Compute
- () A production application runs on an Amazon RDS MySQL DB instance. A solutions architect is building a new reporting tool that will access the same data. The reporting tool must be highly available and not impact the performance of the production application.
- () How can this be achieved?
- () Use Amazon Data Lifecycle Manager to automatically create and manage snapshots
- () Create a Single-AZ RDS Read Replica of the production RDS DB instance. Create a second Single-AZ RDS Read Replica from the replica
- () Create a cross-region Multi-AZ deployment and create a read replica in the second region
- () Create a Multi-AZ RDS Read Replica of the production RDS DB instance
- () You can create a read replica as a Multi-AZ DB instance. Amazon RDS creates a standby of your replica in another Availability Zone for failover support for the replica. Creating your read replica as a Multi-AZ DB instance is independent of whether the source database is a Multi-AZ DB instance.
- ()  is the correct answer.
- ()  is incorrect. Read replicas are primarily used for horizontal scaling. The best solution for high availability is to use a Multi-AZ read replica.
- ()  is incorrect as you cannot create a cross-region Multi-AZ deployment with RDS.
- ()  is incorrect as using snapshots is not the best solution for high availability.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_MySQL.Replication.ReadReplicas.html#USER_MySQL.Replication.ReadReplicas.MultiAZ
- () https://digitalcloud.training/amazon-rds/
- () AWS Database
- () A company is planning to migrate a large quantity of important data to Amazon S3. The data will be uploaded to a versioning enabled bucket in the us-west-1 Region. The solution needs to include replication of the data to another Region for disaster recovery purposes.
- () How should a solutions architect configure the replication?
- () Create an additional S3 bucket in another Region and configure cross-origin resource sharing (CORS)
- () Create an additional S3 bucket with versioning in another Region and configure cross-origin resource sharing (CORS)
- **() Create an additional S3 bucket with versioning in another Region and configure cross-Region replication** [CORRECT]
- () Create an additional S3 bucket in another Region and configure cross-Region replication
- () Replication enables automatic, asynchronous copying of objects across Amazon S3 buckets. Buckets that are configured for object replication can be owned by the same AWS account or by different accounts. You can copy objects between different AWS Regions or within the same Region. Both source and destination buckets must have versioning enabled.
- ()  is incorrect as the destination bucket must also have versioning enabled.
- ()  is incorrect as CORS is not related to replication.

**Answer:**
Correct Answer: **Create an additional S3 bucket with versioning in another Region and configure cross-Region replication**

---

## Question 44

**Q:** How should a solutions architect configure the replication?

**Options:**
- (A) Create an additional S3 bucket in another Region and configure cross-origin resource sharing (CORS)
- (B) Create an additional S3 bucket with versioning in another Region and configure cross-origin resource sharing (CORS)
- (C) Create an additional S3 bucket with versioning in another Region and configure cross-Region replication
- (D) Create an additional S3 bucket in another Region and configure cross-Region replication
- (E) Replication enables automatic, asynchronous copying of objects across Amazon S3 buckets. Buckets that are configured for object replication can be owned by the same AWS account or by different accounts. You can copy objects between different AWS Regions or within the same Region. Both source and destination buckets must have versioning enabled.
- (F)  is the correct answer.
- (G)  is incorrect as the destination bucket must also have versioning enabled.
- (H)  is incorrect as CORS is not related to replication.
- (I) References:
- (J) https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-s3-and-glacier/
- () AWS Storage
- () A company has some statistical data stored in an Amazon RDS database. The company want to allow users to access this information using an API. A solutions architect must create a solution that allows sporadic access to the data, ranging from no requests to large bursts of traffic.
- () Which solution should the solutions architect suggest?
- () Set up an Amazon API Gateway and use Amazon EC2 with Auto Scaling
- () Set up an Amazon API Gateway and use Amazon ECS
- () Set up an Amazon API Gateway and use AWS Elastic Beanstalk
- () Set up an Amazon API Gateway and use AWS Lambda functions
- () AWS Lambda is an ideal solution as you pay only when requests are made and it can easily scale to accommodate the large bursts in traffic. Lambda works well with both API Gateway and Amazon RDS.
- ()  is incorrect
- () https://docs.aws.amazon.com/lambda/latest/dg/invocation-scaling.html
- () https://digitalcloud.training/aws-lambda/
- () AWS Networking & Content Delivery
- () A company needs to ensure that they can failover between AWS Regions in the event of a disaster seamlessly with minimal downtime and data loss. The applications will run in an active-active configuration.
- () Which DR strategy should a Solutions Architect recommend?
- () Pilot light
- () Warm standby
- **() Multi-site** [CORRECT]
- () Backup and restore
- () A multi-site solution runs on AWS as well as on your existing on-site infrastructure in an active- active configuration. The data replication method that you employ will be determined by the recovery point that you choose. This is either Recovery Time Objective (the maximum allowable downtime before degraded operations are restored) or Recovery Point Objective (the maximum allowable time window whereby you will accept the loss of transactions during the DR process).
- ()  is incorrect. This is the lowest cost DR approach that simply entails creating online backups of all data and applications.
- ()  is incorrect. With a pilot light strategy a core minimum of services are running and the remainder are only brought online during a disaster recovery situation.
- ()  is incorrect. The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud.
- () https://aws.amazon.com/blogs/publicsector/rapidly-recover-mission-critical-systems-in-a-disaster/
- () AWS Cloud Architecture & Design
- () There are badge readers located at every entrance of an organization’s warehouses. A message is sent over HTTPS when badges are scanned to indicate who tried to access the entrance.
- () A solutions architect must design a system to process these messages. A highly available solution is required. The solution must store results in a durable data store for later analysis.

**Answer:**
Correct Answer: **Multi-site**

---

## Question 45

**Q:** Which solution should the solutions architect suggest?

**Options:**
- (A) Set up an Amazon API Gateway and use Amazon EC2 with Auto Scaling
- (B) Set up an Amazon API Gateway and use Amazon ECS
- (C) Set up an Amazon API Gateway and use AWS Elastic Beanstalk
- (D) Set up an Amazon API Gateway and use AWS Lambda functions
- (E) AWS Lambda is an ideal solution as you pay only when requests are made and it can easily scale to accommodate the large bursts in traffic. Lambda works well with both API Gateway and Amazon RDS.
- (F)  is the correct answer.
- (G)  is incorrect
- (H) References:
- (I) https://docs.aws.amazon.com/lambda/latest/dg/invocation-scaling.html
- (J) Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-lambda/
- () AWS Networking & Content Delivery
- () A company needs to ensure that they can failover between AWS Regions in the event of a disaster seamlessly with minimal downtime and data loss. The applications will run in an active-active configuration.
- () Which DR strategy should a Solutions Architect recommend?
- () Pilot light
- () Warm standby
- () Multi-site
- () Backup and restore
- () A multi-site solution runs on AWS as well as on your existing on-site infrastructure in an active- active configuration. The data replication method that you employ will be determined by the recovery point that you choose. This is either Recovery Time Objective (the maximum allowable downtime before degraded operations are restored) or Recovery Point Objective (the maximum allowable time window whereby you will accept the loss of transactions during the DR process).
- ()  is incorrect. This is the lowest cost DR approach that simply entails creating online backups of all data and applications.
- ()  is incorrect. With a pilot light strategy a core minimum of services are running and the remainder are only brought online during a disaster recovery situation.
- ()  is incorrect. The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud.
- () https://aws.amazon.com/blogs/publicsector/rapidly-recover-mission-critical-systems-in-a-disaster/
- () AWS Cloud Architecture & Design
- () There are badge readers located at every entrance of an organization’s warehouses. A message is sent over HTTPS when badges are scanned to indicate who tried to access the entrance.
- () A solutions architect must design a system to process these messages. A highly available solution is required. The solution must store results in a durable data store for later analysis.
- () Which system architecture should the solutions architect recommend?
- () Create an Amazon EC2 instance to serve as the HTTPS endpoint and to process messages. An Amazon S3 bucket should be configured for the EC2 instance to save the results.
- () Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB.
- () Set up an Amazon S3 gateway endpoint in your VPC. Connect the facility network to the VPC via a Site-to-Site VPN connection so that sensor data can be written directly to an S3 bucket.
- **() Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function.** [CORRECT]
- () Amazon API Gateway would be ideal for providing a secure entry point for your application, and for traffic to be sent via HTTPS. AWS Lambda would integrate seamlessly with API Gateway to process the data, as an event-driven solution like this would be perfect when designing a scalable system based on sporadic use. Finally, DynamoDB is highly scalable and is a perfect repository for data to be stored for future analysis.
- ()  is the correct answer (as explained above.)
- ()  is incorrect. As the action of a badge being read to initiate access to a warehouse should only take a few seconds, spinning up an EC2 instance to serve as a HTTPS endpoint would take minutes, and is not suitable for this use case.
- () Direct incoming messages from the sensor to an AWS Lambda function using Amazon Route 53. Create a Lambda function that processes messages and saves results to Amazon DynamoDB” is incorrect. Amazon Route 53 is a managed DNS service, and DNS is not required in this instance as the badge reader does not have a DNS name.
- ()  is incorrect. VPC endpoints are designed to facilitate traffic across the AWS backbone network between AWS services and are not used to create connections between external endpoints outside of the AWS network and an Amazon S3 bucket.
- () https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html
- () https://digitalcloud.training/aws-application-integration-services/
- () A company is creating a solution that must offer disaster recovery across multiple AWS Regions. The solution requires relational a database that can support a Recovery Point Objective (RPO) of 1 second and a Recovery Time Objective (RTO) of 1 minute.

**Answer:**
Correct Answer: **Set up an HTTPS endpoint in Amazon API Gateway. To process the messages and save the results to Amazon DynamoDB, configure an API Gateway endpoint to invoke an AWS Lambda function.**

---

## Question 46

**Q:** Which AWS solution can achieve this?

**Options:**
- (A) Amazon RDS for with a cross-Region replica.
- (B) Amazon DynamoDB global tables.
- (C) Amazon RDS for with Multi-AZ enabled.
- (D) Amazon Aurora Global Database.
- (E) Aurora Global Database lets you easily scale database reads across the world and place your applications close to your users. Your applications enjoy quick data access regardless of the number and location of secondary regions, with typical cross-region replication latencies below 1 second.
- (F) If your primary region suffers a performance degradation or outage, you can promote one of the secondary regions to take read/write responsibilities. An Aurora cluster can recover in less than 1 minute even in the event of a complete regional outage. This provides your application with an effective Recovery Point Objective (RPO) of 1 second and a Recovery Time Objective (RTO) of less than 1 minute, providing a strong foundation for a global business continuity plan.
- (G)  is the correct answer.
- (H)  is incorrect. RDS Multi-AZ is across availability zones, not across Regions.
- (I)  is incorrect. A cross-Region replica for RDS cannot provide an RPO of 1 second as there is typically more latency. You also cannot achieve a minute RPO as it takes much longer to promote a replica to a master.
- (J)  is incorrect. This is not a relational database; it is a non-relational database (NoSQL).
- () References:
- () https://aws.amazon.com/rds/aurora/global-database/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-aurora/
- () AWS Database
- () A solutions architect is optimizing a website for real-time streaming and on-demand videos. The website’s users are located around the world and the solutions architect needs to optimize the performance for both the real-time and on-demand streaming.
- () Which service should the solutions architect choose?
- () AWS Global Accelerator
- () Amazon S3 Transfer Acceleration
- () Amazon Route 53
- **() Amazon CloudFront** [CORRECT]
- () Amazon CloudFront can be used to stream video to users across the globe using a wide variety of protocols that are layered on top of HTTP. This can include both on-demand video as well as real time streaming video.
- ()  is incorrect as this would be an expensive way of getting the content closer to users compared to using CloudFront. As this is a use case for CloudFront and there are so many edge locations it is the better option.
- ()  is incorrect as you still need a solution for getting the content closer to users.
- ()  is incorrect as this is used to accelerate uploads of data to Amazon S3 buckets.
- () https://aws.amazon.com/cloudfront/streaming/
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/on-demand-streaming-video.html
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Networking & Content Delivery
- () A company has launched a multi-tier application architecture. The web tier and database tier run on Amazon EC2 instances in private subnets within the same Availability Zone.
- () Which combination of steps should a Solutions Architect take to add high availability to this architecture? (Select TWO.)
- () Add the existing web application instances to an Auto Scaling group behind an Application Load Balancer (ALB)
- () Create new private subnets in the same VPC but in a different AZ. Create a database using Amazon EC2 in one AZ
- () Correct selection
- () Create new private subnets in the same VPC but in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment
- () Create an Amazon EC2 Auto Scaling group and Application Load Balancer (ALB) spanning multiple AZs
- () Create new public subnets in the same AZ for high availability and move the web tier to the public subnets
- () The Solutions Architect can use Auto Scaling group across multiple AZs with an ALB in front to create an elastic and highly available architecture. Then, migrate the database to an Amazon RDS multi-AZ deployment to create HA for the database tier. This results in a fully redundant architecture that can withstand the failure of an availability zone.
- ()  is a correct answer.
- ()  is also a correct answer.
- ()  is incorrect. If subnets share the same AZ they are not suitable for splitting your tier across them for HA as the failure of a an AZ will take out both subnets.
- ()  is incorrect. The instances are in a single AZ so the Solutions Architect should create a new auto scaling group and launch instances across multiple AZs.
- ()  is incorrect. A database in a single AZ will not be highly available.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-increase-availability.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html

**Answer:**
Correct Answer: **Amazon CloudFront**

---

## Question 47

**Q:** Which service should the solutions architect choose?

**Options:**
- (A) AWS Global Accelerator
- (B) Amazon S3 Transfer Acceleration
- (C) Amazon Route 53
- (D) Amazon CloudFront
- (E) Amazon CloudFront can be used to stream video to users across the globe using a wide variety of protocols that are layered on top of HTTP. This can include both on-demand video as well as real time streaming video.
- (F)  is the correct answer.
- (G)  is incorrect as this would be an expensive way of getting the content closer to users compared to using CloudFront. As this is a use case for CloudFront and there are so many edge locations it is the better option.
- (H)  is incorrect as you still need a solution for getting the content closer to users.
- (I)  is incorrect as this is used to accelerate uploads of data to Amazon S3 buckets.
- (J) References:
- () https://aws.amazon.com/cloudfront/streaming/
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/on-demand-streaming-video.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Networking & Content Delivery
- () A company has launched a multi-tier application architecture. The web tier and database tier run on Amazon EC2 instances in private subnets within the same Availability Zone.
- () Which combination of steps should a Solutions Architect take to add high availability to this architecture? (Select TWO.)
- () Add the existing web application instances to an Auto Scaling group behind an Application Load Balancer (ALB)
- () Create new private subnets in the same VPC but in a different AZ. Create a database using Amazon EC2 in one AZ
- () Correct selection
- () Create new private subnets in the same VPC but in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment
- () Create an Amazon EC2 Auto Scaling group and Application Load Balancer (ALB) spanning multiple AZs
- () Create new public subnets in the same AZ for high availability and move the web tier to the public subnets
- () The Solutions Architect can use Auto Scaling group across multiple AZs with an ALB in front to create an elastic and highly available architecture. Then, migrate the database to an Amazon RDS multi-AZ deployment to create HA for the database tier. This results in a fully redundant architecture that can withstand the failure of an availability zone.
- ()  is a correct answer.
- ()  is also a correct answer.
- ()  is incorrect. If subnets share the same AZ they are not suitable for splitting your tier across them for HA as the failure of a an AZ will take out both subnets.
- ()  is incorrect. The instances are in a single AZ so the Solutions Architect should create a new auto scaling group and launch instances across multiple AZs.
- ()  is incorrect. A database in a single AZ will not be highly available.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-increase-availability.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html
- () https://digitalcloud.training/amazon-ec2/
- () https://digitalcloud.training/amazon-rds/
- () AWS Compute
- () A Solutions Architect needs to capture information about the traffic that reaches an Amazon Elastic Load Balancer. The information should include the source, destination, and protocol.
- () What is the most secure and reliable method for gathering this data?
- () Create a VPC flow log for the subnets in which the ELB is running
- **() Create a VPC flow log for each network interface associated with the ELB** [CORRECT]
- () Use Amazon CloudWatch Logs to review detailed logging information
- () Enable Amazon CloudTrail logging and configure packet capturing
- () You can use VPC Flow Logs to capture detailed information about the traffic going to and from your Elastic Load Balancer. Create a flow log for each network interface for your load balancer. There is one network interface per load balancer subnet.
- ()  is incorrect. CloudTrail performs auditing of API actions, it does not do packet capturing.
- ()  is incorrect as this service does not record this information in CloudWatch logs.
- ()  is incorrect as the more secure option is to use the ELB network interfaces.
- () https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html

**Answer:**
Correct Answer: **Create a VPC flow log for each network interface associated with the ELB**

---

## Question 48

**Q:** Which combination of steps should a Solutions Architect take to add high availability to this architecture? (Select TWO.)

**Options:**
- (A) Add the existing web application instances to an Auto Scaling group behind an Application Load Balancer (ALB)
- (B) Create new private subnets in the same VPC but in a different AZ. Create a database using Amazon EC2 in one AZ
- (C) Correct selection
- (D) Create new private subnets in the same VPC but in a different AZ. Migrate the database to an Amazon RDS multi-AZ deployment
- (E) Create an Amazon EC2 Auto Scaling group and Application Load Balancer (ALB) spanning multiple AZs
- (F) Create new public subnets in the same AZ for high availability and move the web tier to the public subnets
- (G) The Solutions Architect can use Auto Scaling group across multiple AZs with an ALB in front to create an elastic and highly available architecture. Then, migrate the database to an Amazon RDS multi-AZ deployment to create HA for the database tier. This results in a fully redundant architecture that can withstand the failure of an availability zone.
- (H)  is a correct answer.
- (I)  is also a correct answer.
- (J)  is incorrect. If subnets share the same AZ they are not suitable for splitting your tier across them for HA as the failure of a an AZ will take out both subnets.
- ()  is incorrect. The instances are in a single AZ so the Solutions Architect should create a new auto scaling group and launch instances across multiple AZs.
- ()  is incorrect. A database in a single AZ will not be highly available.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-increase-availability.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2/
- () https://digitalcloud.training/amazon-rds/
- () AWS Compute
- () A Solutions Architect needs to capture information about the traffic that reaches an Amazon Elastic Load Balancer. The information should include the source, destination, and protocol.
- () What is the most secure and reliable method for gathering this data?
- () Create a VPC flow log for the subnets in which the ELB is running
- () Create a VPC flow log for each network interface associated with the ELB
- () Use Amazon CloudWatch Logs to review detailed logging information
- () Enable Amazon CloudTrail logging and configure packet capturing
- () You can use VPC Flow Logs to capture detailed information about the traffic going to and from your Elastic Load Balancer. Create a flow log for each network interface for your load balancer. There is one network interface per load balancer subnet.
- ()  is the correct answer.
- ()  is incorrect. CloudTrail performs auditing of API actions, it does not do packet capturing.
- ()  is incorrect as this service does not record this information in CloudWatch logs.
- ()  is incorrect as the more secure option is to use the ELB network interfaces.
- () https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-monitoring.html
- () https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
- () AWS Networking & Content Delivery
- () A financial services company is migrating its sensitive customer data and applications to AWS. They want to ensure that the data is securely stored and managed while reducing the overall maintenance and operational overhead associated with managing databases.
- () Which solution will meet these requirements?
- () Store the data in Amazon S3. Utilize Amazon Macie for ongoing data security and threat detection.
- **() Migrate the data and applications to Amazon RDS instances. Enable encryption at rest using AWS Key Management Service (AWS KMS).** [CORRECT]
- () Migrate the data to Amazon RDS instances. Enable Amazon GuardDuty for data protection and threat detection.
- () Migrate the applications and data to Amazon EC2 instances. Utilize the AWS Key Management Service (AWS KMS) customer managed keys for encryption.
- () Amazon RDS makes it easy to go from project conception to deployment by managing time-consuming database administration tasks including backups, software patching, monitoring, scaling, and replication.
- () Amazon RDS supports encryption at rest, which ensures the security of sensitive data and meets regulatory compliance requirements. AWS Key Management Service (AWS KMS) is integrated with Amazon RDS to make it easier to create, control, and manage keys for encryption.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () While this solution offers data encryption, it does not meet the requirement to reduce operational overhead. Managing databases on EC2 instances requires additional administrative tasks, such as managing backups and applying software patches, which Amazon RDS handles automatically.
- () Amazon S3 and Macie are suitable for data storage and security analysis, respectively. However, Amazon S3 is not designed to serve as a transactional database for applications, which is a key requirement in this scenario.

**Answer:**
Correct Answer: **Migrate the data and applications to Amazon RDS instances. Enable encryption at rest using AWS Key Management Service (AWS KMS).**

---

## Question 49

**Q:** What is the most secure and reliable method for gathering this data?

**Options:**
- (A) Create a VPC flow log for the subnets in which the ELB is running
- (B) Create a VPC flow log for each network interface associated with the ELB
- (C) Use Amazon CloudWatch Logs to review detailed logging information
- (D) Enable Amazon CloudTrail logging and configure packet capturing
- (E) You can use VPC Flow Logs to capture detailed information about the traffic going to and from your Elastic Load Balancer. Create a flow log for each network interface for your load balancer. There is one network interface per load balancer subnet.
- (F)  is the correct answer.
- (G)  is incorrect. CloudTrail performs auditing of API actions, it does not do packet capturing.
- (H)  is incorrect as this service does not record this information in CloudWatch logs.
- (I)  is incorrect as the more secure option is to use the ELB network interfaces.
- (J) References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-monitoring.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/aws-elastic-load-balancing-aws-elb/
- () AWS Networking & Content Delivery
- () A financial services company is migrating its sensitive customer data and applications to AWS. They want to ensure that the data is securely stored and managed while reducing the overall maintenance and operational overhead associated with managing databases.
- () Which solution will meet these requirements?
- () Store the data in Amazon S3. Utilize Amazon Macie for ongoing data security and threat detection.
- () Migrate the data and applications to Amazon RDS instances. Enable encryption at rest using AWS Key Management Service (AWS KMS).
- () Migrate the data to Amazon RDS instances. Enable Amazon GuardDuty for data protection and threat detection.
- () Migrate the applications and data to Amazon EC2 instances. Utilize the AWS Key Management Service (AWS KMS) customer managed keys for encryption.
- () Amazon RDS makes it easy to go from project conception to deployment by managing time-consuming database administration tasks including backups, software patching, monitoring, scaling, and replication.
- () Amazon RDS supports encryption at rest, which ensures the security of sensitive data and meets regulatory compliance requirements. AWS Key Management Service (AWS KMS) is integrated with Amazon RDS to make it easier to create, control, and manage keys for encryption.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () While this solution offers data encryption, it does not meet the requirement to reduce operational overhead. Managing databases on EC2 instances requires additional administrative tasks, such as managing backups and applying software patches, which Amazon RDS handles automatically.
- () Amazon S3 and Macie are suitable for data storage and security analysis, respectively. However, Amazon S3 is not designed to serve as a transactional database for applications, which is a key requirement in this scenario.
- () While Amazon RDS is a correct choice for database management and Amazon GuardDuty offers threat detection, GuardDuty is not specifically designed for data protection within databases. It's a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts and workloads.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- () https://digitalcloud.training/amazon-rds/
- () https://digitalcloud.training/aws-kms/
- () AWS Database
- () A legacy application is being migrated into AWS. The application has a large amount of data that is rarely accessed. When files are accessed they are retrieved sequentially. The application will be migrated onto an Amazon EC2 instance.
- () What is the LEAST expensive EBS volume type for this use case?
- () Throughput Optimized HDD (st1)
- () Provisioned IOPS SSD (io1)
- () General Purpose SSD (gp2)
- **() Cold HDD (sc1)** [CORRECT]
- () The cold HDD (sc1) EBS volume type is the lowest cost option that is suitable for this use case. The sc1 volume type is suitable for infrequently accessed data and use cases that are oriented towards throughput like sequential data access.
- ()  is incorrect. This is the most expensive option and used for use cases that demand high IOPS.
- ()  is incorrect. This is a more expensive SSD volume type that is used for general use cases.
- ()  is incorrect. This is also used for throughput-oriented use cases however it is higher cost than sc1 and better for frequently accessed data.

**Answer:**
Correct Answer: **Cold HDD (sc1)**

---

## Question 50

**Q:** What is the LEAST expensive EBS volume type for this use case?

**Options:**
- (A) Throughput Optimized HDD (st1)
- (B) Provisioned IOPS SSD (io1)
- (C) General Purpose SSD (gp2)
- (D) Cold HDD (sc1)
- (E) The cold HDD (sc1) EBS volume type is the lowest cost option that is suitable for this use case. The sc1 volume type is suitable for infrequently accessed data and use cases that are oriented towards throughput like sequential data access.
- (F)  is the correct answer.
- (G)  is incorrect. This is the most expensive option and used for use cases that demand high IOPS.
- (H)  is incorrect. This is a more expensive SSD volume type that is used for general use cases.
- (I)  is incorrect. This is also used for throughput-oriented use cases however it is higher cost than sc1 and better for frequently accessed data.
- (J) References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2/
- () AWS Compute
- () A telecommunication company has an API that allows users to manage their mobile plans and services. The API experiences significant traffic spikes during specific times such as end of the month and special offer periods. The company needs to ensure low latency response time consistently to ensure a good user experience. The solution should also minimize operational overhead.
- () Which solution would meet these requirements MOST efficiently?
- () Implement the API on an Amazon EC2 instance behind an Application Load Balancer with manual scaling.
- () Use Amazon API Gateway with AWS Fargate tasks to handle the API requests.
- () Use Amazon API Gateway along with AWS Lambda functions with provisioned concurrency.
- () Implement the API using AWS Elastic Beanstalk with auto-scaling groups.
- () Amazon API Gateway and AWS Lambda together make a highly scalable solution for APIs. Provisioned concurrency in Lambda ensures that there is always a warm pool of functions ready to quickly respond to API requests, thereby guaranteeing low latency even during peak traffic times.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () Elastic Beanstalk is a viable option for deploying applications and auto-scaling and can help handle increased traffic, but it doesn't guarantee the low latency requirement during peak traffic times.
- () API Gateway with Fargate can provide scalable compute, but this approach can result in higher operational overhead because of the need to manage the container lifecycle.
- () This solution does not scale automatically and would require manual intervention to ensure optimal performance during traffic spikes. Therefore, it doesn't satisfy the requirement of minimizing operational overhead.
- () https://docs.aws.amazon.com/lambda/latest/dg/provisioned-concurrency.html
- () https://digitalcloud.training/amazon-api-gateway/
- () AWS Networking & Content Delivery
- () A company runs a financial application using an Amazon EC2 Auto Scaling group behind an Application Load Balancer (ALB). When running month-end reports on a specific day and time each month the application becomes unacceptably slow. Amazon CloudWatch metrics show the CPU utilization hitting 100%.
- () What should a solutions architect recommend to ensure the application is able to handle the workload and avoid downtime?
- **() Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule** [CORRECT]
- () Configure Amazon ElastiCache to remove some of the workload from the EC2 instances
- () Configure an Amazon CloudFront distribution in front of the ALB
- () Configure an EC2 Auto Scaling simple scaling policy based on CPU utilization
- () Scheduled scaling allows you to set your own scaling schedule. In this case the scaling action can be scheduled to occur just prior to the time that the reports will be run each month. Scaling actions are performed automatically as a function of time and date. This will ensure that there are enough EC2 instances to serve the demand and prevent the application from slowing down.
- ()  is incorrect as this would be more suitable for providing access to global users by caching content.
- ()  is incorrect as this would not prevent the slow-down from occurring as there would be a delay between when the CPU hits 100% and the metric being reported and additional instances being launched.
- ()  is incorrect as ElastiCache is a database cache, it cannot replace the compute functions of an EC2 instance.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html

**Answer:**
Correct Answer: **Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule**

---

## Question 51

**Q:** Which solution would meet these requirements MOST efficiently?

**Options:**
- (A) Implement the API on an Amazon EC2 instance behind an Application Load Balancer with manual scaling.
- (B) Use Amazon API Gateway with AWS Fargate tasks to handle the API requests.
- (C) Use Amazon API Gateway along with AWS Lambda functions with provisioned concurrency.
- (D) Implement the API using AWS Elastic Beanstalk with auto-scaling groups.
- (E) Amazon API Gateway and AWS Lambda together make a highly scalable solution for APIs. Provisioned concurrency in Lambda ensures that there is always a warm pool of functions ready to quickly respond to API requests, thereby guaranteeing low latency even during peak traffic times.
- (F)  is the correct answer (as explained above.)
- (G)  is incorrect.
- (H) Elastic Beanstalk is a viable option for deploying applications and auto-scaling and can help handle increased traffic, but it doesn't guarantee the low latency requirement during peak traffic times.
- (I) API Gateway with Fargate can provide scalable compute, but this approach can result in higher operational overhead because of the need to manage the container lifecycle.
- (J) This solution does not scale automatically and would require manual intervention to ensure optimal performance during traffic spikes. Therefore, it doesn't satisfy the requirement of minimizing operational overhead.
- () References:
- () https://docs.aws.amazon.com/lambda/latest/dg/provisioned-concurrency.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-api-gateway/
- () AWS Networking & Content Delivery
- () A company runs a financial application using an Amazon EC2 Auto Scaling group behind an Application Load Balancer (ALB). When running month-end reports on a specific day and time each month the application becomes unacceptably slow. Amazon CloudWatch metrics show the CPU utilization hitting 100%.
- () What should a solutions architect recommend to ensure the application is able to handle the workload and avoid downtime?
- () Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule
- () Configure Amazon ElastiCache to remove some of the workload from the EC2 instances
- () Configure an Amazon CloudFront distribution in front of the ALB
- () Configure an EC2 Auto Scaling simple scaling policy based on CPU utilization
- () Scheduled scaling allows you to set your own scaling schedule. In this case the scaling action can be scheduled to occur just prior to the time that the reports will be run each month. Scaling actions are performed automatically as a function of time and date. This will ensure that there are enough EC2 instances to serve the demand and prevent the application from slowing down.
- ()  is the correct answer.
- ()  is incorrect as this would be more suitable for providing access to global users by caching content.
- ()  is incorrect as this would not prevent the slow-down from occurring as there would be a delay between when the CPU hits 100% and the metric being reported and additional instances being launched.
- ()  is incorrect as ElastiCache is a database cache, it cannot replace the compute functions of an EC2 instance.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html
- () https://digitalcloud.training/amazon-ec2-auto-scaling/
- () AWS Compute
- () A company runs an application on premises that stores a large quantity of semi-structured data using key-value pairs. The application code will be migrated to AWS Lambda and a highly scalable solution is required for storing the data.
- () Which datastore will be the best fit for these requirements?
- () Amazon RDS MySQL
- () Amazon EFS
- () Amazon EBS
- **() Amazon DynamoDB** [CORRECT]
- () Amazon DynamoDB is a no-SQL database that stores data using key-value pairs. It is ideal for storing large amounts of semi-structured data and is also highly scalable. This is the best solution for storing this data based on the requirements in the scenario.
- ()  is incorrect. The Amazon Elastic File System (EFS) is not suitable for storing key-value pairs.
- ()  is incorrect. Amazon Relational Database Service (RDS) is used for structured data as it is an SQL type of database.
- ()  is incorrect. Amazon Elastic Block Store (EBS) is a block-based storage system. You attach volumes to EC2 instances. It is not used for key-value pairs or to be used by Lambda functions.
- () https://aws.amazon.com/dynamodb/features/
- () https://digitalcloud.training/amazon-dynamodb/

**Answer:**
Correct Answer: **Amazon DynamoDB**

---

## Question 52

**Q:** What should a solutions architect recommend to ensure the application is able to handle the workload and avoid downtime?

**Options:**
- (A) Configure an EC2 Auto Scaling scheduled scaling policy based on the monthly schedule
- (B) Configure Amazon ElastiCache to remove some of the workload from the EC2 instances
- (C) Configure an Amazon CloudFront distribution in front of the ALB
- (D) Configure an EC2 Auto Scaling simple scaling policy based on CPU utilization
- (E) Scheduled scaling allows you to set your own scaling schedule. In this case the scaling action can be scheduled to occur just prior to the time that the reports will be run each month. Scaling actions are performed automatically as a function of time and date. This will ensure that there are enough EC2 instances to serve the demand and prevent the application from slowing down.
- (F)  is the correct answer.
- (G)  is incorrect as this would be more suitable for providing access to global users by caching content.
- (H)  is incorrect as this would not prevent the slow-down from occurring as there would be a delay between when the CPU hits 100% and the metric being reported and additional instances being launched.
- (I)  is incorrect as ElastiCache is a database cache, it cannot replace the compute functions of an EC2 instance.
- (J) References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-ec2-auto-scaling/
- () AWS Compute
- () A company runs an application on premises that stores a large quantity of semi-structured data using key-value pairs. The application code will be migrated to AWS Lambda and a highly scalable solution is required for storing the data.
- () Which datastore will be the best fit for these requirements?
- () Amazon RDS MySQL
- () Amazon EFS
- () Amazon EBS
- () Amazon DynamoDB
- () Amazon DynamoDB is a no-SQL database that stores data using key-value pairs. It is ideal for storing large amounts of semi-structured data and is also highly scalable. This is the best solution for storing this data based on the requirements in the scenario.
- ()  is incorrect. The Amazon Elastic File System (EFS) is not suitable for storing key-value pairs.
- ()  is incorrect. Amazon Relational Database Service (RDS) is used for structured data as it is an SQL type of database.
- ()  is incorrect. Amazon Elastic Block Store (EBS) is a block-based storage system. You attach volumes to EC2 instances. It is not used for key-value pairs or to be used by Lambda functions.
- () https://aws.amazon.com/dynamodb/features/
- () https://digitalcloud.training/amazon-dynamodb/
- () AWS Database
- () A data analytics company is building a high-performance application that requires concurrent writes to a shared block storage volume from multiple Amazon EC2 instances.
- () The EC2 instances are Nitro-based and reside within the same Availability Zone. The company needs a storage solution that supports simultaneous connections to facilitate data resilience and high availability.
- () Which solution will meet these requirements?
- () Use Amazon S3 with S3 Transfer Acceleration to enhance speed.
- **() Use Provisioned IOPS SSD (io2) EBS volumes with Amazon EBS Multi-Attach.** [CORRECT]
- () Use Amazon EFS with NFSv4.1 protocol across multiple EC2 instances.
- () Use General Purpose SSD (gp2) EBS volumes with Amazon EBS Multi-Attach.
- () io2 volumes are designed for I/O-intensive workloads, particularly database workloads, that require high performance and low latency. io1 and io2 volumes support Multi-Attach, which enables you to attach a single volume to multiple EC2 instances in the same Availability Zone.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () Amazon Elastic File System (EFS) is a scalable file storage for use with Amazon EC2. You can use an Amazon EFS file system as a common data source for workloads and applications running on multiple instances, but it does not provide the block-level storage required for high IOPS operations.
- () Amazon S3 is an object storage service. While S3 Transfer Acceleration does enhance the speed of in-transit file transfers, it is not a block storage solution, it is an object storage solution and is not suitable for this use case.
- () Amazon EBS Multi-Attach only supports io1 and io2 volumes, and it is not supported on gp2 volumes.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes-multi.html
- () https://digitalcloud.training/amazon-ebs/

**Answer:**
Correct Answer: **Use Provisioned IOPS SSD (io2) EBS volumes with Amazon EBS Multi-Attach.**

---

## Question 53

**Q:** Which datastore will be the best fit for these requirements?

**Options:**
- (A) Amazon RDS MySQL
- (B) Amazon EFS
- (C) Amazon EBS
- (D) Amazon DynamoDB
- (E) Amazon DynamoDB is a no-SQL database that stores data using key-value pairs. It is ideal for storing large amounts of semi-structured data and is also highly scalable. This is the best solution for storing this data based on the requirements in the scenario.
- (F)  is the correct answer.
- (G)  is incorrect. The Amazon Elastic File System (EFS) is not suitable for storing key-value pairs.
- (H)  is incorrect. Amazon Relational Database Service (RDS) is used for structured data as it is an SQL type of database.
- (I)  is incorrect. Amazon Elastic Block Store (EBS) is a block-based storage system. You attach volumes to EC2 instances. It is not used for key-value pairs or to be used by Lambda functions.
- (J) References:
- () https://aws.amazon.com/dynamodb/features/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-dynamodb/
- () AWS Database
- () A data analytics company is building a high-performance application that requires concurrent writes to a shared block storage volume from multiple Amazon EC2 instances.
- () The EC2 instances are Nitro-based and reside within the same Availability Zone. The company needs a storage solution that supports simultaneous connections to facilitate data resilience and high availability.
- () Which solution will meet these requirements?
- () Use Amazon S3 with S3 Transfer Acceleration to enhance speed.
- () Use Provisioned IOPS SSD (io2) EBS volumes with Amazon EBS Multi-Attach.
- () Use Amazon EFS with NFSv4.1 protocol across multiple EC2 instances.
- () Use General Purpose SSD (gp2) EBS volumes with Amazon EBS Multi-Attach.
- () io2 volumes are designed for I/O-intensive workloads, particularly database workloads, that require high performance and low latency. io1 and io2 volumes support Multi-Attach, which enables you to attach a single volume to multiple EC2 instances in the same Availability Zone.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () Amazon Elastic File System (EFS) is a scalable file storage for use with Amazon EC2. You can use an Amazon EFS file system as a common data source for workloads and applications running on multiple instances, but it does not provide the block-level storage required for high IOPS operations.
- () Amazon S3 is an object storage service. While S3 Transfer Acceleration does enhance the speed of in-transit file transfers, it is not a block storage solution, it is an object storage solution and is not suitable for this use case.
- () Amazon EBS Multi-Attach only supports io1 and io2 volumes, and it is not supported on gp2 volumes.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes-multi.html
- () https://digitalcloud.training/amazon-ebs/
- () AWS Compute
- () A cloud architect is assessing the resilience of a web application deployed on AWS. It was observed that the application experienced a downtime of about 3 minutes when a scheduled failover was performed on the application's Amazon RDS MySQL database as part of a scaling operation.
- () The organization wants to mitigate such downtime in future scaling exercises while minimizing operational overhead.
- () Which solution will be the MOST effective in achieving this?
- () Implement more RDS MySQL read replicas in the cluster to manage the load during the failover.
- () Establish a secondary RDS MySQL cluster within the same AWS Region. During any future failover, modify the application to connect to the secondary cluster's writer endpoint.
- () Implement an Amazon ElastiCache for Redis cluster to manage the load during the failover.
- **() Configure an Amazon RDS Proxy for the database and modify the application to connect to the proxy endpoint.** [CORRECT]
- () Amazon RDS Proxy is a fully managed, highly available database proxy for Amazon RDS that makes applications more scalable, more resilient to database failures, and more secure.
- () During a failover, RDS Proxy automatically connects to a standby database instance while preserving connections from your application and reducing failover times for RDS and Aurora multi-AZ databases. So, there is minimal downtime for the application.
- () Adding more read replicas to the cluster does not decrease the downtime during a failover. It only improves the database's ability to handle read-heavy workloads. Read replicas do not contribute to a faster failover process.
- () This approach is operationally heavy as it involves managing two separate RDS clusters and manually updating the application's database endpoint during a failover. Moreover, it does not necessarily reduce the downtime during a failover as there might be data inconsistency issues between the primary and secondary clusters, depending on the replication latency.

**Answer:**
Correct Answer: **Configure an Amazon RDS Proxy for the database and modify the application to connect to the proxy endpoint.**

---

## Question 54

**Q:** Which solution will be the MOST effective in achieving this?

**Options:**
- (A) Implement more RDS MySQL read replicas in the cluster to manage the load during the failover.
- (B) Establish a secondary RDS MySQL cluster within the same AWS Region. During any future failover, modify the application to connect to the secondary cluster's writer endpoint.
- (C) Implement an Amazon ElastiCache for Redis cluster to manage the load during the failover.
- (D) Configure an Amazon RDS Proxy for the database and modify the application to connect to the proxy endpoint.
- (E) Amazon RDS Proxy is a fully managed, highly available database proxy for Amazon RDS that makes applications more scalable, more resilient to database failures, and more secure.
- (F) During a failover, RDS Proxy automatically connects to a standby database instance while preserving connections from your application and reducing failover times for RDS and Aurora multi-AZ databases. So, there is minimal downtime for the application.
- (G)  is the correct answer (as explained above.)
- (H)  is incorrect.
- (I) Adding more read replicas to the cluster does not decrease the downtime during a failover. It only improves the database's ability to handle read-heavy workloads. Read replicas do not contribute to a faster failover process.
- (J) This approach is operationally heavy as it involves managing two separate RDS clusters and manually updating the application's database endpoint during a failover. Moreover, it does not necessarily reduce the downtime during a failover as there might be data inconsistency issues between the primary and secondary clusters, depending on the replication latency.
- () ElastiCache is an in-memory cache and not a relational database service. It is typically used to cache frequently accessed data to reduce latency and improve application performance, not for managing failovers.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-rds/
- () AWS Compute
- () An application generates unique files that are returned to customers after they submit requests to the application. The application uses an Amazon CloudFront distribution for sending the files to customers. The company wishes to reduce data transfer costs without modifying the application.
- () How can this be accomplished?
- () Use Lambda@Edge to compress the files as they are sent to users.
- () Enable Amazon S3 Transfer Acceleration to reduce the transfer times.
- () Enable caching on the CloudFront distribution to store generated files at the edge.
- () Use AWS Global Accelerator to reduce application latency for customers.
- () Lambda@Edge is a feature of Amazon CloudFront that lets you run code closer to users of your application, which improves performance and reduces latency. Lambda@Edge runs code in response to events generated by the Amazon CloudFront.
- () You simply upload your code to AWS Lambda, and it takes care of everything required to run and scale your code with high availability at an AWS location closest to your end user.
- () In this case Lambda@Edge can compress the files before they are sent to users which will reduce data egress costs.
- ()  is the correct answer.
- ()  is incorrect. The files are unique to each customer request, so caching does not help.
- ()  is incorrect. The aim is to reduce cost not latency and AWS GA uses the same network as CloudFront so does not assist with latency anyway.
- ()  is incorrect. This does not lower costs.
- () https://aws.amazon.com/lambda/edge/
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Networking & Content Delivery
- () An e-commerce company operates a serverless web application that must interact with numerous Amazon DynamoDB tables to fulfill user requests. It is critical that the application's performance remains consistent and unaffected while interacting with these tables.
- () Which method provides the MOST operationally efficient way to fulfill these requirements?
- () AWS Glue with a DynamoDB connector.
- **() AWS AppSync with multiple data sources and resolvers.** [CORRECT]
- () AWS Lambda with Step Functions.
- () Amazon S3 with Lambda triggers.
- () AWS AppSync simplifies application development by letting you create a flexible API to securely access, manipulate, and combine data from one or more data sources. AppSync is a managed service that uses GraphQL to make it easy for applications to get exactly the data they need, including from multiple DynamoDB tables.
- () AWS AppSync is designed for real-time and offline data access which makes it an ideal solution for this scenario.
- () AWS Step Functions make it easy to coordinate the components of distributed applications and microservices using visual workflows. However, while you could theoretically build a flow to retrieve data from multiple tables, it's not the most efficient solution as it introduces additional complexity and potential latency.

**Answer:**
Correct Answer: **AWS AppSync with multiple data sources and resolvers.**

---

## Question 55

**Q:** How can this be accomplished?

**Options:**
- (A) Use Lambda@Edge to compress the files as they are sent to users.
- (B) Enable Amazon S3 Transfer Acceleration to reduce the transfer times.
- (C) Enable caching on the CloudFront distribution to store generated files at the edge.
- (D) Use AWS Global Accelerator to reduce application latency for customers.
- (E) Lambda@Edge is a feature of Amazon CloudFront that lets you run code closer to users of your application, which improves performance and reduces latency. Lambda@Edge runs code in response to events generated by the Amazon CloudFront.
- (F) You simply upload your code to AWS Lambda, and it takes care of everything required to run and scale your code with high availability at an AWS location closest to your end user.
- (G) In this case Lambda@Edge can compress the files before they are sent to users which will reduce data egress costs.
- (H)  is the correct answer.
- (I)  is incorrect. The files are unique to each customer request, so caching does not help.
- (J)  is incorrect. The aim is to reduce cost not latency and AWS GA uses the same network as CloudFront so does not assist with latency anyway.
- ()  is incorrect. This does not lower costs.
- () References:
- () https://aws.amazon.com/lambda/edge/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-cloudfront/
- () AWS Networking & Content Delivery
- () An e-commerce company operates a serverless web application that must interact with numerous Amazon DynamoDB tables to fulfill user requests. It is critical that the application's performance remains consistent and unaffected while interacting with these tables.
- () Which method provides the MOST operationally efficient way to fulfill these requirements?
- () AWS Glue with a DynamoDB connector.
- () AWS AppSync with multiple data sources and resolvers.
- () AWS Lambda with Step Functions.
- () Amazon S3 with Lambda triggers.
- () AWS AppSync simplifies application development by letting you create a flexible API to securely access, manipulate, and combine data from one or more data sources. AppSync is a managed service that uses GraphQL to make it easy for applications to get exactly the data they need, including from multiple DynamoDB tables.
- () AWS AppSync is designed for real-time and offline data access which makes it an ideal solution for this scenario.
- ()  is the correct answer (as explained above.)
- ()  is incorrect.
- () AWS Step Functions make it easy to coordinate the components of distributed applications and microservices using visual workflows. However, while you could theoretically build a flow to retrieve data from multiple tables, it's not the most efficient solution as it introduces additional complexity and potential latency.
- () While you can use AWS Lambda to execute code in response to triggers like changes to data in an Amazon S3 bucket, this doesn't directly allow the application to retrieve data from multiple DynamoDB tables. This approach would also involve unnecessary data transfers and added latency.
- () AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy to prepare and load your data for analytics. However, AWS Glue isn't meant for real-time data retrieval in an application. Using it for real-time data retrieval would likely be overcomplicated and inefficient.
- () https://aws.amazon.com/appsync/product-details/
- () AWS Compute
- () An application requires a MySQL database which will only be used several times a week for short periods. The database needs to provide automatic instantiation and scaling. Which database service is most suitable?
- **() Amazon Aurora Serverless** [CORRECT]
- () Amazon Aurora
- () Amazon RDS MySQL
- () Amazon EC2 instance with MySQL database installed
- () Amazon Aurora Serverless is an on-demand, auto-scaling configuration for Amazon Aurora. The database automatically starts up, shuts down, and scales capacity up or down based on application needs. This is an ideal database solution for infrequently-used applications.
- ()  is incorrect as this service requires an instance to be running all the time which is more costly.
- () https://aws.amazon.com/rds/aurora/serverless/
- () https://digitalcloud.training/amazon-aurora/

**Answer:**
Correct Answer: **Amazon Aurora Serverless**

---

## Question 56

**Q:** Which method provides the MOST operationally efficient way to fulfill these requirements?

**Options:**
- (A) AWS Glue with a DynamoDB connector.
- (B) AWS AppSync with multiple data sources and resolvers.
- (C) AWS Lambda with Step Functions.
- (D) Amazon S3 with Lambda triggers.
- (E) AWS AppSync simplifies application development by letting you create a flexible API to securely access, manipulate, and combine data from one or more data sources. AppSync is a managed service that uses GraphQL to make it easy for applications to get exactly the data they need, including from multiple DynamoDB tables.
- (F) AWS AppSync is designed for real-time and offline data access which makes it an ideal solution for this scenario.
- (G)  is the correct answer (as explained above.)
- (H)  is incorrect.
- (I) AWS Step Functions make it easy to coordinate the components of distributed applications and microservices using visual workflows. However, while you could theoretically build a flow to retrieve data from multiple tables, it's not the most efficient solution as it introduces additional complexity and potential latency.
- (J) While you can use AWS Lambda to execute code in response to triggers like changes to data in an Amazon S3 bucket, this doesn't directly allow the application to retrieve data from multiple DynamoDB tables. This approach would also involve unnecessary data transfers and added latency.
- () AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy to prepare and load your data for analytics. However, AWS Glue isn't meant for real-time data retrieval in an application. Using it for real-time data retrieval would likely be overcomplicated and inefficient.
- () References:
- () https://aws.amazon.com/appsync/product-details/
- () AWS Compute
- () An application requires a MySQL database which will only be used several times a week for short periods. The database needs to provide automatic instantiation and scaling. Which database service is most suitable?
- () Amazon Aurora Serverless
- () Amazon Aurora
- () Amazon RDS MySQL
- () Amazon EC2 instance with MySQL database installed
- () Amazon Aurora Serverless is an on-demand, auto-scaling configuration for Amazon Aurora. The database automatically starts up, shuts down, and scales capacity up or down based on application needs. This is an ideal database solution for infrequently-used applications.
- ()  is the correct answer.
- ()  is incorrect as this service requires an instance to be running all the time which is more costly.
- () https://aws.amazon.com/rds/aurora/serverless/
- () Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-aurora/
- () AWS Database
- () Dump10
- () An ivy-league university is assisting NASA to find potential landing sites for exploration vehicles of unmanned missions to our neighboring planets. The university uses High Performance Computing (HPC) driven application architecture to identify these landing sites.
- () Which of the following Amazon EC2 instance topologies should this application be deployed on?
- () The Amazon EC2 instances should be deployed in an Auto Scaling group so that application meets high availability requirements
- **() The Amazon EC2 instances should be deployed in a cluster placement group so that the underlying workload can benefit from low network latency and high network throughput** [CORRECT]
- () The Amazon EC2 instances should be deployed in a partition placement group so that distributed workloads can be handled effectively
- () The Amazon EC2 instances should be deployed in a spread placement group so that there are no correlated failures
- () Correct option:
- () Cluster Placement Group:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () Incorrect options:
- () Partition Placement Group:

**Answer:**
Correct Answer: **The Amazon EC2 instances should be deployed in a cluster placement group so that the underlying workload can benefit from low network latency and high network throughput**

---

## Question 57

**Q:** An application requires a MySQL database which will only be used several times a week for short periods. The database needs to provide automatic instantiation and scaling. Which database service is most suitable?

**Options:**
- (A) Amazon Aurora Serverless
- (B) Amazon Aurora
- (C) Amazon RDS MySQL
- (D) Amazon EC2 instance with MySQL database installed
- (E) Amazon Aurora Serverless is an on-demand, auto-scaling configuration for Amazon Aurora. The database automatically starts up, shuts down, and scales capacity up or down based on application needs. This is an ideal database solution for infrequently-used applications.
- (F)  is the correct answer.
- (G)  is incorrect as this service requires an instance to be running all the time which is more costly.
- (H) References:
- (I) https://aws.amazon.com/rds/aurora/serverless/
- (J) Save time with our AWS cheat sheets:
- () https://digitalcloud.training/amazon-aurora/
- () AWS Database
- () Dump10
- () An ivy-league university is assisting NASA to find potential landing sites for exploration vehicles of unmanned missions to our neighboring planets. The university uses High Performance Computing (HPC) driven application architecture to identify these landing sites.
- () Which of the following Amazon EC2 instance topologies should this application be deployed on?
- () The Amazon EC2 instances should be deployed in an Auto Scaling group so that application meets high availability requirements
- () The Amazon EC2 instances should be deployed in a cluster placement group so that the underlying workload can benefit from low network latency and high network throughput
- () The Amazon EC2 instances should be deployed in a partition placement group so that distributed workloads can be handled effectively
- () The Amazon EC2 instances should be deployed in a spread placement group so that there are no correlated failures
- () Correct option:
- () Cluster Placement Group:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () Incorrect options:
- () Partition Placement Group:
- () Spread Placement Group:
- () The Amazon EC2 instances should be deployed in an Auto Scaling group so that application meets high availability requirements - An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling. You do not use Auto Scaling groups per se to meet HPC requirements.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () Which solution will meet these requirements MOST cost-effectively?
- () Use Amazon FSx for Windows File Server to replace the NFS workload. Enable data deduplication and automatic backups. Use Amazon S3 Glacier to move snapshots to a cost-efficient storage tier. Reconfigure the analytics application to access files using SMB protocol
- **() Deploy an AWS Storage Gateway File Gateway on premises. Configure it to present an NFS-compatible file share to the workloads. Store the uploaded files in Amazon S3, and use S3 Lifecycle policies to automatically transition infrequently accessed objects to lower-cost storage classes** [CORRECT]
- () Provision an Amazon Elastic File System (Amazon EFS) file system with the One Zone–IA storage class. Use AWS DataSync to migrate the NFS data to EFS. Configure the application to mount the file system over NFS and activate lifecycle management to tier infrequently accessed files
- () Deploy an AWS Storage Gateway Volume Gateway in cached mode. Attach it as a block device to an on-premises file server and mount NFS on top. Store snapshots in Amazon S3 Glacier Deep Archive, and use AWS Backup to manage recovery operations and tiering

**Answer:**
Correct Answer: **Deploy an AWS Storage Gateway File Gateway on premises. Configure it to present an NFS-compatible file share to the workloads. Store the uploaded files in Amazon S3, and use S3 Lifecycle policies to automatically transition infrequently accessed objects to lower-cost storage classes**

---

## Question 58

**Q:** Which of the following Amazon EC2 instance topologies should this application be deployed on?

**Options:**
- (A) The Amazon EC2 instances should be deployed in an Auto Scaling group so that application meets high availability requirements
- (B) The Amazon EC2 instances should be deployed in a cluster placement group so that the underlying workload can benefit from low network latency and high network throughput
- (C) The Amazon EC2 instances should be deployed in a partition placement group so that distributed workloads can be handled effectively
- (D) The Amazon EC2 instances should be deployed in a spread placement group so that there are no correlated failures
- (E) Correct option:
- (F) Cluster Placement Group:
- (G) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- (H) Incorrect options:
- (I) Partition Placement Group:
- (J) Spread Placement Group:
- () The Amazon EC2 instances should be deployed in an Auto Scaling group so that application meets high availability requirements - An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling. You do not use Auto Scaling groups per se to meet HPC requirements.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () Which solution will meet these requirements MOST cost-effectively?
- () Use Amazon FSx for Windows File Server to replace the NFS workload. Enable data deduplication and automatic backups. Use Amazon S3 Glacier to move snapshots to a cost-efficient storage tier. Reconfigure the analytics application to access files using SMB protocol
- **() Deploy an AWS Storage Gateway File Gateway on premises. Configure it to present an NFS-compatible file share to the workloads. Store the uploaded files in Amazon S3, and use S3 Lifecycle policies to automatically transition infrequently accessed objects to lower-cost storage classes** [CORRECT]
- () Provision an Amazon Elastic File System (Amazon EFS) file system with the One Zone–IA storage class. Use AWS DataSync to migrate the NFS data to EFS. Configure the application to mount the file system over NFS and activate lifecycle management to tier infrequently accessed files
- () Deploy an AWS Storage Gateway Volume Gateway in cached mode. Attach it as a block device to an on-premises file server and mount NFS on top. Store snapshots in Amazon S3 Glacier Deep Archive, and use AWS Backup to manage recovery operations and tiering
- () How File Gateway Works:
- () via - https://docs.aws.amazon.com/filegateway/latest/files3/file-gateway-concepts.html
- () How Volume Gateway Works:
- () via - https://docs.aws.amazon.com/storagegateway/latest/vgw/StorageGatewayConcepts.html
- () References:
- () https://docs.aws.amazon.com/filegateway/latest/files3/what-is-file-s3.html
- () https://docs.aws.amazon.com/filegateway/latest/files3/file-gateway-concepts.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/what-is.html

**Answer:**
Correct Answer: **Deploy an AWS Storage Gateway File Gateway on premises. Configure it to present an NFS-compatible file share to the workloads. Store the uploaded files in Amazon S3, and use S3 Lifecycle policies to automatically transition infrequently accessed objects to lower-cost storage classes**

---

## Question 59

**Q:** Which of the following options is the MOST cost-optimal and resource-efficient solution to build this fleet of Amazon EC2 instances?

**Options:**
- (A) Use Amazon EC2 instances with Amazon EFS mount points
- (B) Use Amazon EC2 instances with access to Amazon S3 based storage
- (C) Use Instance Store based Amazon EC2 instances
- (D) Use Amazon Elastic Block Store (Amazon EBS) based EC2 instances
- (E) Correct option:
- (F) An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host instance. Instance store is ideal for the temporary storage of information that changes frequently such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers. Instance store volumes are included as part of the instance's usage cost.
- (G) As Instance Store based volumes provide high random I/O performance at low cost (as the storage is part of the instance's usage cost) and the resilient architecture can adjust for the loss of any instance, therefore you should use Instance Store based Amazon EC2 instances for this use-case.
- (H) Amazon EC2 Instance Store Overview:
- (I) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- (J) Incorrect options:
- () Use Amazon Elastic Block Store (Amazon EBS) based EC2 instances - Amazon Elastic Block Store (Amazon EBS) based volumes would need to use provisioned IOPS (io1) as the storage type and that would incur additional costs. As we are looking for the most cost-optimal solution, this option is ruled out.
- () Use Amazon EC2 instances with Amazon EFS mount points - Using Amazon Elastic File System (Amazon EFS) implies that extra resources would have to be provisioned (compared to using instance store where the storage is located on disks that are physically attached to the host instance itself). As we are looking for the most resource-efficient solution, this option is also ruled out.
- () Use Amazon EC2 instances with access to Amazon S3 based storage - Using Amazon EC2 instances with access to Amazon S3 based storage does not deliver high random I/O performance, this option is just added as a distractor.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- () Can you identify the correct outcomes for these events? (Select two)
- () Amazon EC2 Auto Scaling creates a new scaling activity for launching a new instance to replace the unhealthy instance. Later, Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it
- () Correct selection
- () As the resources are unbalanced in the Availability Zones, Amazon EC2 Auto Scaling will compensate by rebalancing the Availability Zones. When rebalancing, Amazon EC2 Auto Scaling launches new instances before terminating the old ones, so that rebalancing does not compromise the performance or availability of your application
- () Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it. Later, another scaling activity launches a new instance to replace the terminated instance
- () As the resources are unbalanced in the Availability Zones, Amazon EC2 Auto Scaling will compensate by rebalancing the Availability Zones. When rebalancing, Amazon EC2 Auto Scaling terminates old instances before launching new instances, so that rebalancing does not cause extra instances to be launched
- () Amazon EC2 Auto Scaling creates a new scaling activity to terminate the unhealthy instance and launch the new instance simultaneously
- () Correct options:
- () When rebalancing, Amazon EC2 Auto Scaling launches new instances before terminating the old ones, so that rebalancing does not compromise the performance or availability of your application. Therefore, this option is correct.
- () Availability Zone Rebalancing Overview:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html
- () However, the scaling activity of Auto Scaling works in a different sequence compared to the rebalancing activity. Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it. Later, another scaling activity launches a new instance to replace the terminated instance.
- () Amazon EC2 Auto Scaling creates a new scaling activity for launching a new instance to replace the unhealthy instance. Later, Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it - This option contradicts the correct sequence of events outlined earlier for scaling activity created by Amazon EC2 Auto Scaling. Actually, Auto Scaling first terminates the unhealthy instance and then launches a new instance. Hence this is incorrect.
- () Amazon EC2 Auto Scaling creates a new scaling activity to terminate the unhealthy instance and launch the new instance simultaneously - This is a made-up option as both the terminate and launch activities can't happen simultaneously. This option has been added as a distractor.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html
- () A gaming company is developing a mobile game that streams score updates to a backend processor and then publishes results on a leaderboard. The company has hired you as an AWS Certified Solutions Architect Associate to design a solution that can handle major traffic spikes, process the mobile game updates in the order of receipt, and store the processed updates in a highly available database. The company wants to minimize the management overhead required to maintain the solution.
- () Which of the following will you recommend to meet these requirements?
- **() Push score updates to Amazon Kinesis Data Streams which uses an AWS Lambda function to process these updates and then store these processed updates in Amazon DynamoDB** [CORRECT]

**Answer:**
Correct Answer: **Push score updates to Amazon Kinesis Data Streams which uses an AWS Lambda function to process these updates and then store these processed updates in Amazon DynamoDB**

---

## Question 60

**Q:** Can you identify the correct outcomes for these events? (Select two)

**Options:**
- (A) Amazon EC2 Auto Scaling creates a new scaling activity for launching a new instance to replace the unhealthy instance. Later, Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it
- (B) Correct selection
- (C) As the resources are unbalanced in the Availability Zones, Amazon EC2 Auto Scaling will compensate by rebalancing the Availability Zones. When rebalancing, Amazon EC2 Auto Scaling launches new instances before terminating the old ones, so that rebalancing does not compromise the performance or availability of your application
- (D) Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it. Later, another scaling activity launches a new instance to replace the terminated instance
- (E) As the resources are unbalanced in the Availability Zones, Amazon EC2 Auto Scaling will compensate by rebalancing the Availability Zones. When rebalancing, Amazon EC2 Auto Scaling terminates old instances before launching new instances, so that rebalancing does not cause extra instances to be launched
- (F) Amazon EC2 Auto Scaling creates a new scaling activity to terminate the unhealthy instance and launch the new instance simultaneously
- (G) Correct options:
- (H) When rebalancing, Amazon EC2 Auto Scaling launches new instances before terminating the old ones, so that rebalancing does not compromise the performance or availability of your application. Therefore, this option is correct.
- (I) Availability Zone Rebalancing Overview:
- (J) via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html
- () However, the scaling activity of Auto Scaling works in a different sequence compared to the rebalancing activity. Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it. Later, another scaling activity launches a new instance to replace the terminated instance.
- () Incorrect options:
- () Amazon EC2 Auto Scaling creates a new scaling activity for launching a new instance to replace the unhealthy instance. Later, Amazon EC2 Auto Scaling creates a new scaling activity for terminating the unhealthy instance and then terminates it - This option contradicts the correct sequence of events outlined earlier for scaling activity created by Amazon EC2 Auto Scaling. Actually, Auto Scaling first terminates the unhealthy instance and then launches a new instance. Hence this is incorrect.
- () Amazon EC2 Auto Scaling creates a new scaling activity to terminate the unhealthy instance and launch the new instance simultaneously - This is a made-up option as both the terminate and launch activities can't happen simultaneously. This option has been added as a distractor.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html
- () A gaming company is developing a mobile game that streams score updates to a backend processor and then publishes results on a leaderboard. The company has hired you as an AWS Certified Solutions Architect Associate to design a solution that can handle major traffic spikes, process the mobile game updates in the order of receipt, and store the processed updates in a highly available database. The company wants to minimize the management overhead required to maintain the solution.
- () Which of the following will you recommend to meet these requirements?
- () Push score updates to Amazon Kinesis Data Streams which uses an AWS Lambda function to process these updates and then store these processed updates in Amazon DynamoDB
- () Push score updates to an Amazon Simple Notification Service (Amazon SNS) topic, subscribe an AWS Lambda function to this Amazon SNS topic to process the updates and then store these processed updates in a SQL database running on Amazon EC2 instance
- () Push score updates to an Amazon Simple Queue Service (Amazon SQS) queue which uses a fleet of Amazon EC2 instances (with Auto Scaling) to process these updates in the Amazon SQS queue and then store these processed updates in an Amazon RDS MySQL database
- () Push score updates to Amazon Kinesis Data Streams which uses a fleet of Amazon EC2 instances (with Auto Scaling) to process the updates in Amazon Kinesis Data Streams and then store these processed updates in Amazon DynamoDB
- () Correct option:
- () To help ingest real-time data or streaming data at large scales, you can use Amazon Kinesis Data Streams (KDS). KDS can continuously capture gigabytes of data per second from hundreds of thousands of sources. The data collected is available in milliseconds, enabling real-time analytics. KDS provides ordering of records, as well as the ability to read and/or replay records in the same order to multiple Amazon Kinesis Applications.
- () AWS Lambda integrates natively with Kinesis Data Streams. The polling, checkpointing, and error handling complexities are abstracted when you use this native integration. The processed data can then be configured to be saved in Amazon DynamoDB.
- () These three options use Amazon EC2 instances as part of the solution architecture. The use-case seeks to minimize the management overhead required to maintain the solution. However, Amazon EC2 instances involve several maintenance activities such as managing the guest operating system and software deployed to the guest operating system, including updates and security patches, etc. Hence these options are incorrect.
- () Reference:
- () https://aws.amazon.com/blogs/big-data/best-practices-for-consuming-amazon-kinesis-data-streams-using-aws-lambda/
- () Which AWS solution will best meet the company’s requirements for modernization while ensuring that all data remains on premises?
- () Set up a dedicated AWS Direct Connect connection between the on-premises environment and an AWS Region. Deploy Amazon EKS in the cloud and connect it to the local Kubernetes cluster. Use IAM roles and API Gateway to integrate authentication and traffic flow for hybrid workloads
- () Deploy Amazon ECS with Fargate in a nearby AWS Local Zone. Use CloudWatch Logs to forward events to the primary region. Connect the Local Zone to the company’s data center over a VPN. Configure containers to pull data from on-premises storage through a mounted file share
- () Use an AWS Snowball Edge Compute Optimized device to run EKS-compatible Docker containers on-site. Periodically export application logs and container snapshots to Amazon S3 using Snowball’s offline data transfer features. Use the Snowball console to orchestrate workloads in batches
- **() Install an AWS Outposts rack in the company’s data center. Use Amazon EKS Anywhere on Outposts to run containerized workloads locally while integrating with AWS APIs** [CORRECT]

**Answer:**
Correct Answer: **Install an AWS Outposts rack in the company’s data center. Use Amazon EKS Anywhere on Outposts to run containerized workloads locally while integrating with AWS APIs**

---

## Question 61

**Q:** Which of the following will you recommend to meet these requirements?

**Options:**
- (A) Push score updates to Amazon Kinesis Data Streams which uses an AWS Lambda function to process these updates and then store these processed updates in Amazon DynamoDB
- (B) Push score updates to an Amazon Simple Notification Service (Amazon SNS) topic, subscribe an AWS Lambda function to this Amazon SNS topic to process the updates and then store these processed updates in a SQL database running on Amazon EC2 instance
- (C) Push score updates to an Amazon Simple Queue Service (Amazon SQS) queue which uses a fleet of Amazon EC2 instances (with Auto Scaling) to process these updates in the Amazon SQS queue and then store these processed updates in an Amazon RDS MySQL database
- (D) Push score updates to Amazon Kinesis Data Streams which uses a fleet of Amazon EC2 instances (with Auto Scaling) to process the updates in Amazon Kinesis Data Streams and then store these processed updates in Amazon DynamoDB
- (E) Correct option:
- (F) To help ingest real-time data or streaming data at large scales, you can use Amazon Kinesis Data Streams (KDS). KDS can continuously capture gigabytes of data per second from hundreds of thousands of sources. The data collected is available in milliseconds, enabling real-time analytics. KDS provides ordering of records, as well as the ability to read and/or replay records in the same order to multiple Amazon Kinesis Applications.
- (G) AWS Lambda integrates natively with Kinesis Data Streams. The polling, checkpointing, and error handling complexities are abstracted when you use this native integration. The processed data can then be configured to be saved in Amazon DynamoDB.
- (H) Incorrect options:
- (I) These three options use Amazon EC2 instances as part of the solution architecture. The use-case seeks to minimize the management overhead required to maintain the solution. However, Amazon EC2 instances involve several maintenance activities such as managing the guest operating system and software deployed to the guest operating system, including updates and security patches, etc. Hence these options are incorrect.
- (J) Reference:
- () https://aws.amazon.com/blogs/big-data/best-practices-for-consuming-amazon-kinesis-data-streams-using-aws-lambda/
- () Which AWS solution will best meet the company’s requirements for modernization while ensuring that all data remains on premises?
- () Set up a dedicated AWS Direct Connect connection between the on-premises environment and an AWS Region. Deploy Amazon EKS in the cloud and connect it to the local Kubernetes cluster. Use IAM roles and API Gateway to integrate authentication and traffic flow for hybrid workloads
- () Deploy Amazon ECS with Fargate in a nearby AWS Local Zone. Use CloudWatch Logs to forward events to the primary region. Connect the Local Zone to the company’s data center over a VPN. Configure containers to pull data from on-premises storage through a mounted file share
- () Use an AWS Snowball Edge Compute Optimized device to run EKS-compatible Docker containers on-site. Periodically export application logs and container snapshots to Amazon S3 using Snowball’s offline data transfer features. Use the Snowball console to orchestrate workloads in batches
- **() Install an AWS Outposts rack in the company’s data center. Use Amazon EKS Anywhere on Outposts to run containerized workloads locally while integrating with AWS APIs** [CORRECT]
- () via - https://aws.amazon.com/blogs/containers/fully-private-local-clusters-for-amazon-eks-on-aws-outposts-powered-by-vpc-endpoints/
- () References:
- () https://aws.amazon.com/blogs/containers/fully-private-local-clusters-for-amazon-eks-on-aws-outposts-powered-by-vpc-endpoints/
- () https://aws.amazon.com/eks/eks-anywhere/
- () https://aws.amazon.com/outposts/rack/
- () https://aws.amazon.com/about-aws/global-infrastructure/localzones/
- () https://docs.aws.amazon.com/snowball/latest/developer-guide/whatisedge.html
- () A junior scientist working with the Deep Space Research Laboratory at NASA is trying to upload a high-resolution image of a nebula into Amazon S3. The image size is approximately 3 gigabytes. The junior scientist is using Amazon S3 Transfer Acceleration (Amazon S3TA) for faster image upload. It turns out that Amazon S3TA did not result in an accelerated transfer.

**Answer:**
Correct Answer: **Install an AWS Outposts rack in the company’s data center. Use Amazon EKS Anywhere on Outposts to run containerized workloads locally while integrating with AWS APIs**

---

## Question 62

**Q:** Which AWS solution will best meet the company’s requirements for modernization while ensuring that all data remains on premises?

**Options:**
- (A) Set up a dedicated AWS Direct Connect connection between the on-premises environment and an AWS Region. Deploy Amazon EKS in the cloud and connect it to the local Kubernetes cluster. Use IAM roles and API Gateway to integrate authentication and traffic flow for hybrid workloads
- (B) Deploy Amazon ECS with Fargate in a nearby AWS Local Zone. Use CloudWatch Logs to forward events to the primary region. Connect the Local Zone to the company’s data center over a VPN. Configure containers to pull data from on-premises storage through a mounted file share
- (C) Use an AWS Snowball Edge Compute Optimized device to run EKS-compatible Docker containers on-site. Periodically export application logs and container snapshots to Amazon S3 using Snowball’s offline data transfer features. Use the Snowball console to orchestrate workloads in batches
- **(D) Install an AWS Outposts rack in the company’s data center. Use Amazon EKS Anywhere on Outposts to run containerized workloads locally while integrating with AWS APIs** [CORRECT]
- (E) Correct option:
- (F) via - https://aws.amazon.com/blogs/containers/fully-private-local-clusters-for-amazon-eks-on-aws-outposts-powered-by-vpc-endpoints/
- (G) Incorrect options:
- (H) References:
- (I) https://aws.amazon.com/blogs/containers/fully-private-local-clusters-for-amazon-eks-on-aws-outposts-powered-by-vpc-endpoints/
- (J) https://aws.amazon.com/eks/eks-anywhere/
- () https://aws.amazon.com/outposts/rack/
- () https://aws.amazon.com/about-aws/global-infrastructure/localzones/
- () https://docs.aws.amazon.com/snowball/latest/developer-guide/whatisedge.html
- () A junior scientist working with the Deep Space Research Laboratory at NASA is trying to upload a high-resolution image of a nebula into Amazon S3. The image size is approximately 3 gigabytes. The junior scientist is using Amazon S3 Transfer Acceleration (Amazon S3TA) for faster image upload. It turns out that Amazon S3TA did not result in an accelerated transfer.

**Answer:**
Correct Answer: **Install an AWS Outposts rack in the company’s data center. Use Amazon EKS Anywhere on Outposts to run containerized workloads locally while integrating with AWS APIs**

---

## Question 63

**Q:** Given this scenario, which of the following is correct regarding the charges for this image transfer?

**Options:**
- (A) The junior scientist needs to pay both S3 transfer charges and S3TA transfer charges for the image upload
- (B) The junior scientist does not need to pay any transfer charges for the image upload
- (C) The junior scientist only needs to pay Amazon S3 transfer charges for the image upload
- (D) The junior scientist only needs to pay S3TA transfer charges for the image upload
- (E) Correct option:
- (F) There are no S3 data transfer charges when data is transferred in from the internet. Also with S3TA, you pay only for transfers that are accelerated. Therefore the junior scientist does not need to pay any transfer charges for the image upload because S3TA did not result in an accelerated transfer.
- (G) Amazon S3 Transfer Acceleration (S3TA) Overview:
- (H) via - https://aws.amazon.com/s3/transfer-acceleration/
- (I) Incorrect options:
- (J) The junior scientist only needs to pay S3TA transfer charges for the image upload - Since S3TA did not result in an accelerated transfer, there are no S3TA transfer charges to be paid.
- () The junior scientist only needs to pay Amazon S3 transfer charges for the image upload - There are no S3 data transfer charges when data is transferred in from the internet. So this option is incorrect.
- () The junior scientist needs to pay both S3 transfer charges and S3TA transfer charges for the image upload - There are no Amazon S3 data transfer charges when data is transferred in from the internet. Since S3TA did not result in an accelerated transfer, there are no S3TA transfer charges to be paid.
- () References:
- () https://aws.amazon.com/s3/transfer-acceleration/
- () https://aws.amazon.com/s3/pricing/
- () The IT department at a consulting firm is conducting a training workshop for new developers. As part of an evaluation exercise on Amazon S3, the new developers were asked to identify the invalid storage class lifecycle transitions for objects stored on Amazon S3.
- () Can you spot the INVALID lifecycle transitions from the options below? (Select two)
- () Correct selection
- () Amazon S3 One Zone-IA => Amazon S3 Standard-IA
- () Amazon S3 Intelligent-Tiering => Amazon S3 Standard
- () Amazon S3 Standard => Amazon S3 Intelligent-Tiering
- () Amazon S3 Standard-IA => Amazon S3 One Zone-IA
- () Amazon S3 Standard-IA => Amazon S3 Intelligent-Tiering
- () Correct options:
- () Following are the unsupported life cycle transitions for S3 storage classes - Any storage class to the Amazon S3 Standard storage class. Any storage class to the Reduced Redundancy storage class. The Amazon S3 Intelligent-Tiering storage class to the Amazon S3 Standard-IA storage class. The Amazon S3 One Zone-IA storage class to the Amazon S3 Standard-IA or Amazon S3 Intelligent-Tiering storage classes.
- () Here are the supported life cycle transitions for S3 storage classes - The S3 Standard storage class to any other storage class. Any storage class to the S3 Glacier or S3 Glacier Deep Archive storage classes. The S3 Standard-IA storage class to the S3 Intelligent-Tiering or S3 One Zone-IA storage classes. The S3 Intelligent-Tiering storage class to the S3 One Zone-IA storage class. The S3 Glacier storage class to the S3 Glacier Deep Archive storage class.
- () Amazon S3 supports a waterfall model for transitioning between storage classes, as shown in the diagram below: 
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () Which solution will meet these requirements?
- **() Instruct the partner to create a Network Load Balancer (NLB) in front of the Amazon RDS for MySQL instance. Use AWS PrivateLink to expose the NLB as an interface VPC endpoint in the research company’s VPC** [CORRECT]
- () Instruct the partner to enable public access on the Amazon RDS instance and add a security group rule to allow inbound access from the company’s IP range. The company accesses the database over the public internet through a NAT Gateway configured in a private subnet
- () Set up VPC peering between the company’s VPC and the partner’s VPC. Use AWS Transit Gateway in the partner's account to route traffic from the company’s VPC to the database. Modify the RDS subnet route tables to allow access from the company’s CIDR block
- () Configure a client VPN endpoint in the company’s account. Have researchers connect to the VPN from their local machines. Establish a Direct Connect gateway to the partner’s VPC and route RDS traffic via this connection

**Answer:**
Correct Answer: **Instruct the partner to create a Network Load Balancer (NLB) in front of the Amazon RDS for MySQL instance. Use AWS PrivateLink to expose the NLB as an interface VPC endpoint in the research company’s VPC**

---

## Question 64

**Q:** Can you spot the INVALID lifecycle transitions from the options below? (Select two)

**Options:**
- (A) Correct selection
- (B) Amazon S3 One Zone-IA => Amazon S3 Standard-IA
- (C) Amazon S3 Intelligent-Tiering => Amazon S3 Standard
- (D) Amazon S3 Standard => Amazon S3 Intelligent-Tiering
- (E) Amazon S3 Standard-IA => Amazon S3 One Zone-IA
- (F) Amazon S3 Standard-IA => Amazon S3 Intelligent-Tiering
- (G) Correct options:
- (H) Following are the unsupported life cycle transitions for S3 storage classes - Any storage class to the Amazon S3 Standard storage class. Any storage class to the Reduced Redundancy storage class. The Amazon S3 Intelligent-Tiering storage class to the Amazon S3 Standard-IA storage class. The Amazon S3 One Zone-IA storage class to the Amazon S3 Standard-IA or Amazon S3 Intelligent-Tiering storage classes.
- (I) Incorrect options:
- (J) Here are the supported life cycle transitions for S3 storage classes - The S3 Standard storage class to any other storage class. Any storage class to the S3 Glacier or S3 Glacier Deep Archive storage classes. The S3 Standard-IA storage class to the S3 Intelligent-Tiering or S3 One Zone-IA storage classes. The S3 Intelligent-Tiering storage class to the S3 One Zone-IA storage class. The S3 Glacier storage class to the S3 Glacier Deep Archive storage class.
- () Amazon S3 supports a waterfall model for transitioning between storage classes, as shown in the diagram below: 
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () Which solution will meet these requirements?
- **() Instruct the partner to create a Network Load Balancer (NLB) in front of the Amazon RDS for MySQL instance. Use AWS PrivateLink to expose the NLB as an interface VPC endpoint in the research company’s VPC** [CORRECT]
- () Instruct the partner to enable public access on the Amazon RDS instance and add a security group rule to allow inbound access from the company’s IP range. The company accesses the database over the public internet through a NAT Gateway configured in a private subnet
- () Set up VPC peering between the company’s VPC and the partner’s VPC. Use AWS Transit Gateway in the partner's account to route traffic from the company’s VPC to the database. Modify the RDS subnet route tables to allow access from the company’s CIDR block
- () Configure a client VPN endpoint in the company’s account. Have researchers connect to the VPN from their local machines. Establish a Direct Connect gateway to the partner’s VPC and route RDS traffic via this connection
- () Correct option:
- () via - https://docs.aws.amazon.com/vpc/latest/privatelink/what-is-privatelink.html
- () Share your services through AWS PrivateLink:
- () via - https://docs.aws.amazon.com/vpc/latest/privatelink/privatelink-share-your-services.html
- () References:
- () https://docs.aws.amazon.com/vpc/latest/privatelink/what-is-privatelink.html
- () https://docs.aws.amazon.com/vpc/latest/privatelink/privatelink-share-your-services.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () https://docs.aws.amazon.com/vpc/latest/tgw/what-is-transit-gateway.html
- () https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/what-is.html
- () A media company runs a photo-sharing web application that is accessed across three different countries. The application is deployed on several Amazon Elastic Compute Cloud (Amazon EC2) instances running behind an Application Load Balancer. With new government regulations, the company has been asked to block access from two countries and allow access only from the home country of the company.

**Answer:**
Correct Answer: **Instruct the partner to create a Network Load Balancer (NLB) in front of the Amazon RDS for MySQL instance. Use AWS PrivateLink to expose the NLB as an interface VPC endpoint in the research company’s VPC**

---

## Question 65

**Q:** Which configuration should be used to meet this changed requirement?

**Options:**
- (A) Configure the security group on the Application Load Balancer
- (B) Configure AWS Web Application Firewall (AWS WAF) on the Application Load Balancer in a Amazon Virtual Private Cloud (Amazon VPC)
- (C) Use Geo Restriction feature of Amazon CloudFront in a Amazon Virtual Private Cloud (Amazon VPC)
- (D) Configure the security group for the Amazon EC2 instances
- (E) Correct option:
- (F) AWS Web Application Firewall (AWS WAF) is a web application firewall service that lets you monitor web requests and protect your web applications from malicious requests. Use AWS WAF to block or allow requests based on conditions that you specify, such as the IP addresses. You can also use AWS WAF preconfigured protections to block common attacks like SQL injection or cross-site scripting.
- (G) You can use AWS WAF with your Application Load Balancer to allow or block requests based on the rules in a web access control list (web ACL). Geographic (Geo) Match Conditions in AWS WAF allows you to use AWS WAF to restrict application access based on the geographic location of your viewers. With geo match conditions you can choose the countries from which AWS WAF should allow access.
- (H) Incorrect options:
- (I) Use Geo Restriction feature of Amazon CloudFront in a Amazon Virtual Private Cloud (Amazon VPC) - Geo Restriction feature of Amazon CloudFront helps in restricting traffic based on the user's geographic location. But, CloudFront works from edge locations and doesn't belong to a VPC. Hence, this option itself is incorrect and given only as a distractor.
- (J) Security Groups cannot restrict access based on the user's geographic location.
- () References:
- () https://aws.amazon.com/about-aws/whats-new/2017/10/aws-waf-now-supports-geographic-match/
- () https://aws.amazon.com/blogs/aws/aws-web-application-firewall-waf-for-application-load-balancers/
- () https://aws.amazon.com/about-aws/whats-new/2016/12/AWS-WAF-now-available-on-Application-Load-Balancer/
- () A gaming company is looking at improving the availability and performance of its global flagship application which utilizes User Datagram Protocol and needs to support fast regional failover in case an AWS Region goes down. The company wants to continue using its own custom Domain Name System (DNS) service.
- () Which of the following AWS services represents the best solution for this use-case?
- () Amazon CloudFront
- () AWS Elastic Load Balancing (ELB)
- () Amazon Route 53
- () AWS Global Accelerator
- () AWS Global Accelerator utilizes the Amazon global network, allowing you to improve the performance of your applications by lowering first-byte latency (the round trip time for a packet to go from a client to your endpoint and back again) and jitter (the variation of latency), and increasing throughput (the amount of time it takes to transfer data) as compared to the public internet.
- () AWS Global Accelerator improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions. Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover.
- () Amazon CloudFront - Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.
- () AWS Global Accelerator and Amazon CloudFront are separate services that use the AWS global network and its edge locations around the world. CloudFront improves performance for both cacheable content (such as images and videos) and dynamic content (such as API acceleration and dynamic site delivery), while Global Accelerator improves performance for a wide range of applications over TCP or UDP.
- () AWS Elastic Load Balancing (ELB) - Both of the services, ELB and Global Accelerator solve the challenge of routing user requests to healthy application endpoints. AWS Global Accelerator relies on ELB to provide the traditional load balancing features such as support for internal and non-AWS endpoints, pre-warming, and Layer 7 routing. However, while ELB provides load balancing within one Region, AWS Global Accelerator provides traffic management across multiple Regions.
- () A regional ELB load balancer is an ideal target for AWS Global Accelerator. By using a regional ELB load balancer, you can precisely distribute incoming application traffic across backends, such as Amazon EC2 instances or Amazon ECS tasks, within an AWS Region.
- () If you have workloads that cater to a global client base, AWS recommends that you use AWS Global Accelerator. If you have workloads hosted in a single AWS Region and used by clients in and around the same Region, you can use an Application Load Balancer or Network Load Balancer to manage your resources.
- () Amazon Route 53 - Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost-effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers use to connect to each other. Route 53 is ruled out as the company wants to continue using its own custom DNS service.
- () Reference:
- () https://aws.amazon.com/global-accelerator/faqs/
- () A US-based healthcare startup is building an interactive diagnostic tool for COVID-19 related assessments. The users would be required to capture their personal health records via this tool. As this is sensitive health information, the backup of the user data must be kept encrypted in Amazon Simple Storage Service (Amazon S3). The startup does not want to provide its own encryption keys but still wants to maintain an audit trail of when an encryption key was used and by whom.
- () Which of the following is the BEST solution for this use-case?
- **() Use server-side encryption with AWS Key Management Service keys (SSE-KMS) to encrypt the user data on Amazon S3** [CORRECT]
- () Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the user data on Amazon S3
- () Use client-side encryption with client provided keys and then upload the encrypted user data to Amazon S3
- () Use server-side encryption with customer-provided keys (SSE-C) to encrypt the user data on Amazon S3
- () AWS Key Management Service (AWS KMS) is a service that combines secure, highly available hardware and software to provide a key management system scaled for the cloud. When you use server-side encryption with AWS KMS (SSE-KMS), you can specify a customer-managed CMK that you have already created. SSE-KMS provides you with an audit trail that shows when your CMK was used and by whom. Therefore SSE-KMS is the correct solution for this use-case.
- () Server Side Encryption in S3:

**Answer:**
Correct Answer: **Use server-side encryption with AWS Key Management Service keys (SSE-KMS) to encrypt the user data on Amazon S3**

---

## Question 66

**Q:** Which of the following AWS services represents the best solution for this use-case?

**Options:**
- (A) Amazon CloudFront
- (B) AWS Elastic Load Balancing (ELB)
- (C) Amazon Route 53
- (D) AWS Global Accelerator
- (E) Correct option:
- (F) AWS Global Accelerator utilizes the Amazon global network, allowing you to improve the performance of your applications by lowering first-byte latency (the round trip time for a packet to go from a client to your endpoint and back again) and jitter (the variation of latency), and increasing throughput (the amount of time it takes to transfer data) as compared to the public internet.
- (G) AWS Global Accelerator improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions. Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover.
- (H) Incorrect options:
- (I) Amazon CloudFront - Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.
- (J) AWS Global Accelerator and Amazon CloudFront are separate services that use the AWS global network and its edge locations around the world. CloudFront improves performance for both cacheable content (such as images and videos) and dynamic content (such as API acceleration and dynamic site delivery), while Global Accelerator improves performance for a wide range of applications over TCP or UDP.
- () AWS Elastic Load Balancing (ELB) - Both of the services, ELB and Global Accelerator solve the challenge of routing user requests to healthy application endpoints. AWS Global Accelerator relies on ELB to provide the traditional load balancing features such as support for internal and non-AWS endpoints, pre-warming, and Layer 7 routing. However, while ELB provides load balancing within one Region, AWS Global Accelerator provides traffic management across multiple Regions.
- () A regional ELB load balancer is an ideal target for AWS Global Accelerator. By using a regional ELB load balancer, you can precisely distribute incoming application traffic across backends, such as Amazon EC2 instances or Amazon ECS tasks, within an AWS Region.
- () If you have workloads that cater to a global client base, AWS recommends that you use AWS Global Accelerator. If you have workloads hosted in a single AWS Region and used by clients in and around the same Region, you can use an Application Load Balancer or Network Load Balancer to manage your resources.
- () Amazon Route 53 - Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost-effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers use to connect to each other. Route 53 is ruled out as the company wants to continue using its own custom DNS service.
- () Reference:
- () https://aws.amazon.com/global-accelerator/faqs/
- () A US-based healthcare startup is building an interactive diagnostic tool for COVID-19 related assessments. The users would be required to capture their personal health records via this tool. As this is sensitive health information, the backup of the user data must be kept encrypted in Amazon Simple Storage Service (Amazon S3). The startup does not want to provide its own encryption keys but still wants to maintain an audit trail of when an encryption key was used and by whom.
- () Which of the following is the BEST solution for this use-case?
- **() Use server-side encryption with AWS Key Management Service keys (SSE-KMS) to encrypt the user data on Amazon S3** [CORRECT]
- () Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the user data on Amazon S3
- () Use client-side encryption with client provided keys and then upload the encrypted user data to Amazon S3
- () Use server-side encryption with customer-provided keys (SSE-C) to encrypt the user data on Amazon S3
- () AWS Key Management Service (AWS KMS) is a service that combines secure, highly available hardware and software to provide a key management system scaled for the cloud. When you use server-side encryption with AWS KMS (SSE-KMS), you can specify a customer-managed CMK that you have already created. SSE-KMS provides you with an audit trail that shows when your CMK was used and by whom. Therefore SSE-KMS is the correct solution for this use-case.
- () Server Side Encryption in S3:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html
- () Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the user data on Amazon S3 - When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key. However this option does not provide the ability to audit trail the usage of the encryption keys.
- () Use server-side encryption with customer-provided keys (SSE-C) to encrypt the user data on Amazon S3 - With Server-Side Encryption with Customer-Provided Keys (SSE-C), you manage the encryption keys and Amazon S3 manages the encryption, as it writes to disks, and decryption when you access your objects. However this option does not provide the ability to audit trail the usage of the encryption keys.
- () Use client-side encryption with client provided keys and then upload the encrypted user data to Amazon S3 - Using client-side encryption is ruled out as the startup does not want to provide the encryption keys.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingKMSEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingClientSideEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html

**Answer:**
Correct Answer: **Use server-side encryption with AWS Key Management Service keys (SSE-KMS) to encrypt the user data on Amazon S3**

---

## Question 67

**Q:** Which of the following is the BEST solution for this use-case?

**Options:**
- **(A) Use server-side encryption with AWS Key Management Service keys (SSE-KMS) to encrypt the user data on Amazon S3** [CORRECT]
- (B) Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the user data on Amazon S3
- (C) Use client-side encryption with client provided keys and then upload the encrypted user data to Amazon S3
- (D) Use server-side encryption with customer-provided keys (SSE-C) to encrypt the user data on Amazon S3
- (E) Correct option:
- (F) AWS Key Management Service (AWS KMS) is a service that combines secure, highly available hardware and software to provide a key management system scaled for the cloud. When you use server-side encryption with AWS KMS (SSE-KMS), you can specify a customer-managed CMK that you have already created. SSE-KMS provides you with an audit trail that shows when your CMK was used and by whom. Therefore SSE-KMS is the correct solution for this use-case.
- (G) Server Side Encryption in S3:
- (H) via - https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html
- (I) Incorrect options:
- (J) Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the user data on Amazon S3 - When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key. However this option does not provide the ability to audit trail the usage of the encryption keys.
- () Use server-side encryption with customer-provided keys (SSE-C) to encrypt the user data on Amazon S3 - With Server-Side Encryption with Customer-Provided Keys (SSE-C), you manage the encryption keys and Amazon S3 manages the encryption, as it writes to disks, and decryption when you access your objects. However this option does not provide the ability to audit trail the usage of the encryption keys.
- () Use client-side encryption with client provided keys and then upload the encrypted user data to Amazon S3 - Using client-side encryption is ruled out as the startup does not want to provide the encryption keys.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingKMSEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingClientSideEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html

**Answer:**
Correct Answer: **Use server-side encryption with AWS Key Management Service keys (SSE-KMS) to encrypt the user data on Amazon S3**

---

## Question 68

**Q:** As an AWS Certified Solutions Architect – Associate, can you suggest a way to lower the storage costs while fulfilling the business requirements?

**Options:**
- (A) Configure a lifecycle policy to transition the objects to Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) after 7 days
- (B) Configure a lifecycle policy to transition the objects to Amazon S3 Standard-Infrequent Access (S3 Standard-IA) after 30 days
- (C) Configure a lifecycle policy to transition the objects to Amazon S3 Standard-Infrequent Access (S3 Standard-IA) after 7 days
- (D) Configure a lifecycle policy to transition the objects to Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) after 30 days
- (E) Correct option:
- (F) Constraints for Lifecycle storage class transitions:
- (G) via - https://docs.aws.amazon.com/AmazonS3/latest/dev/lifecycle-transition-general-considerations.html
- (H) Supported Amazon S3 lifecycle transitions:
- (I) Incorrect options:
- (J) As mentioned earlier, the minimum storage duration is 30 days before you can transition objects from Amazon S3 Standard to Amazon S3 One Zone-IA or Amazon S3 Standard-IA, so both these options are added as distractors.
- () References:
- () https://aws.amazon.com/s3/storage-classes/
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/lifecycle-transition-general-considerations.html
- () A large financial institution operates an on-premises data center with hundreds of petabytes of data managed on Microsoft’s Distributed File System (DFS). The CTO wants the organization to transition into a hybrid cloud environment and run data-intensive analytics workloads that support DFS.
- () Which of the following AWS services can facilitate the migration of these workloads?
- () Amazon FSx for Lustre
- () AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)
- **() Amazon FSx for Windows File Server** [CORRECT]
- () Microsoft SQL Server on AWS
- () How Amazon FSx for Windows File Server Works:
- () via - https://aws.amazon.com/fsx/windows/
- () Amazon FSx for Lustre makes it easy and cost-effective to launch and run the world’s most popular high-performance file system. It is used for workloads such as machine learning, high-performance computing (HPC), video processing, and financial modeling. Amazon FSx enables you to use Lustre file systems for any workload where storage speed matters. FSx for Lustre does not support Microsoft’s Distributed File System (DFS), so this option is incorrect.
- () AWS Directory Service for Microsoft Active Directory, also known as AWS Managed Microsoft AD, enables your directory-aware workloads and AWS resources to use managed Active Directory in the AWS Cloud. AWS Managed Microsoft AD is built on the actual Microsoft Active Directory and does not require you to synchronize or replicate data from your existing Active Directory to the cloud. AWS Managed Microsoft AD does not support Microsoft’s Distributed File System (DFS), so this option is incorrect.
- () Microsoft SQL Server on AWS offers you the flexibility to run Microsoft SQL Server database on AWS Cloud. Microsoft SQL Server on AWS does not support Microsoft’s Distributed File System (DFS), so this option is incorrect.
- () Reference:
- () https://aws.amazon.com/fsx/windows/
- () The solo founder at a tech startup has just created a brand new AWS account. The founder has provisioned an Amazon EC2 instance 1A which is running in AWS Region A. Later, he takes a snapshot of the instance 1A and then creates a new Amazon Machine Image (AMI) in Region A from this snapshot. This AMI is then copied into another Region B. The founder provisions an instance 1B in Region B using this new AMI in Region B.

**Answer:**
Correct Answer: **Amazon FSx for Windows File Server**

---

## Question 69

**Q:** Which of the following AWS services can facilitate the migration of these workloads?

**Options:**
- (A) Amazon FSx for Lustre
- (B) AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)
- **(C) Amazon FSx for Windows File Server** [CORRECT]
- (D) Microsoft SQL Server on AWS
- (E) Correct option:
- (F) How Amazon FSx for Windows File Server Works:
- (G) via - https://aws.amazon.com/fsx/windows/
- (H) Incorrect options:
- (I) Amazon FSx for Lustre makes it easy and cost-effective to launch and run the world’s most popular high-performance file system. It is used for workloads such as machine learning, high-performance computing (HPC), video processing, and financial modeling. Amazon FSx enables you to use Lustre file systems for any workload where storage speed matters. FSx for Lustre does not support Microsoft’s Distributed File System (DFS), so this option is incorrect.
- (J) AWS Directory Service for Microsoft Active Directory, also known as AWS Managed Microsoft AD, enables your directory-aware workloads and AWS resources to use managed Active Directory in the AWS Cloud. AWS Managed Microsoft AD is built on the actual Microsoft Active Directory and does not require you to synchronize or replicate data from your existing Active Directory to the cloud. AWS Managed Microsoft AD does not support Microsoft’s Distributed File System (DFS), so this option is incorrect.
- () Microsoft SQL Server on AWS offers you the flexibility to run Microsoft SQL Server database on AWS Cloud. Microsoft SQL Server on AWS does not support Microsoft’s Distributed File System (DFS), so this option is incorrect.
- () Reference:
- () https://aws.amazon.com/fsx/windows/
- () The solo founder at a tech startup has just created a brand new AWS account. The founder has provisioned an Amazon EC2 instance 1A which is running in AWS Region A. Later, he takes a snapshot of the instance 1A and then creates a new Amazon Machine Image (AMI) in Region A from this snapshot. This AMI is then copied into another Region B. The founder provisions an instance 1B in Region B using this new AMI in Region B.

**Answer:**
Correct Answer: **Amazon FSx for Windows File Server**

---

## Question 70

**Q:** At this point in time, what entities exist in Region B?

**Options:**
- (A) 1 Amazon EC2 instance and 2 AMIs exist in Region B
- **(B) 1 Amazon EC2 instance, 1 AMI and 1 snapshot exist in Region B** [CORRECT]
- (C) 1 Amazon EC2 instance and 1 snapshot exist in Region B
- (D) 1 Amazon EC2 instance and 1 AMI exist in Region B
- (E) Correct option:
- (F) An Amazon Machine Image (AMI) provides the information required to launch an instance. You must specify an AMI when you launch an instance. When the new AMI is copied from Region A into Region B, it automatically creates a snapshot in Region B because AMIs are based on the underlying snapshots. Further, an instance is created from this AMI in Region B. Hence, we have 1 Amazon EC2 instance, 1 AMI and 1 snapshot in Region B.
- (G) Amazon Machine Image (AMI) Overview:
- (H) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html
- (I) Incorrect options:
- (J) As mentioned earlier in the explanation, when the new AMI is copied from Region A into Region B, it also creates a snapshot in Region B because AMIs are based on the underlying snapshots. In addition, an instance is created from this AMI in Region B. So, we have 1 Amazon EC2 instance, 1 AMI and 1 snapshot in Region B. Hence all three options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html
- () An IT consultant is helping the owner of a medium-sized business set up an AWS account. What are the security recommendations he must follow while creating the AWS account root user? (Select two)
- () Create AWS account root user access keys and share those keys only with the business owner
- () Encrypt the access keys and save them on Amazon S3
- () Correct selection
- () Create a strong password for the AWS account root user
- () Enable Multi Factor Authentication (MFA) for the AWS account root user account
- () Send an email to the business owner with details of the login username and password for the AWS root user. This will help the business owner to troubleshoot any login issues in future
- () Correct options:
- () Here are some of the best practices while creating an AWS account root user:
- () AWS Root Account Security Best Practices:
- () via - https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html
- () Encrypt the access keys and save them on Amazon S3 - AWS recommends that if you don't already have an access key for your AWS account root user, don't create one unless you absolutely need to. Even an encrypted access key for the root user poses a significant security risk. Therefore, this option is incorrect.
- () Create AWS account root user access keys and share those keys only with the business owner - AWS recommends that if you don't already have an access key for your AWS account root user, don't create one unless you absolutely need to. Hence, this option is incorrect.
- () Send an email to the business owner with details of the login username and password for the AWS root user. This will help the business owner to troubleshoot any login issues in future - AWS recommends that you should never share your AWS account root user password or access keys with anyone. Sending an email with AWS account root user credentials creates a security risk as it can be misused by anyone reading the email. Hence, this option is incorrect.
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users
- () A development team requires permissions to list an Amazon S3 bucket and delete objects from that bucket. A systems administrator has created the following IAM policy to provide access to the bucket and applied that policy to the group. The group is not able to delete objects in the bucket. The company follows the principle of least privilege.
- () : [
- ()             ],

**Answer:**
Correct Answer: **1 Amazon EC2 instance, 1 AMI and 1 snapshot exist in Region B**

---

## Question 71

**Q:** An IT consultant is helping the owner of a medium-sized business set up an AWS account. What are the security recommendations he must follow while creating the AWS account root user? (Select two)

**Options:**
- (A) Create AWS account root user access keys and share those keys only with the business owner
- (B) Encrypt the access keys and save them on Amazon S3
- (C) Correct selection
- (D) Create a strong password for the AWS account root user
- (E) Enable Multi Factor Authentication (MFA) for the AWS account root user account
- (F) Send an email to the business owner with details of the login username and password for the AWS root user. This will help the business owner to troubleshoot any login issues in future
- (G) Correct options:
- (H) Here are some of the best practices while creating an AWS account root user:
- (I) AWS Root Account Security Best Practices:
- (J) via - https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html
- () Incorrect options:
- () Encrypt the access keys and save them on Amazon S3 - AWS recommends that if you don't already have an access key for your AWS account root user, don't create one unless you absolutely need to. Even an encrypted access key for the root user poses a significant security risk. Therefore, this option is incorrect.
- () Create AWS account root user access keys and share those keys only with the business owner - AWS recommends that if you don't already have an access key for your AWS account root user, don't create one unless you absolutely need to. Hence, this option is incorrect.
- () Send an email to the business owner with details of the login username and password for the AWS root user. This will help the business owner to troubleshoot any login issues in future - AWS recommends that you should never share your AWS account root user password or access keys with anyone. Sending an email with AWS account root user credentials creates a security risk as it can be misused by anyone reading the email. Hence, this option is incorrect.
- () Reference:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users
- () A development team requires permissions to list an Amazon S3 bucket and delete objects from that bucket. A systems administrator has created the following IAM policy to provide access to the bucket and applied that policy to the group. The group is not able to delete objects in the bucket. The company follows the principle of least privilege.
- () : [
- ()             ],
- () Which statement should a solutions architect add to the policy to address this issue?
- **() {** [CORRECT]
- ()     ],

**Answer:**
Correct Answer: **{**

---

## Question 72

**Q:** Which statement should a solutions architect add to the policy to address this issue?

**Options:**
- **(A) {** [CORRECT]
- (B) : [
- (C)     ],
- (D) Correct option:
- (E) The main elements of a policy statement are:
- (F) 1. Effect: Specifies whether the statement will Allow or Deny an action (Allow is the effect defined here).
- (G) 2. Action: Describes a specific action or actions that will either be allowed or denied to run based on the Effect entered. API actions are unique to each service (DeleteObject is the action defined here).
- (H) 3. Resource: Specifies the resources—for example, an Amazon S3 bucket or objects—that the policy applies to in Amazon Resource Name (ARN) format ( example-bucket/* is the resource defined here).
- (I) This policy provides the necessary delete permissions on the resources of the Amazon S3 bucket to the group.
- (J) Incorrect options:

**Answer:**
Correct Answer: **{**

---

## Question 73

**Q:** Which of the following options would allow the company to enforce these streaming restrictions? (Select two)

**Options:**
- **(A) Use Amazon Route 53 based weighted routing policy to restrict distribution of content to only the locations in which you have distribution rights** [CORRECT]
- (B) Correct selection
- (C) Use georestriction to prevent users in specific geographic locations from accessing content that you're distributing through a Amazon CloudFront web distribution
- (D) Use Amazon Route 53 based geolocation routing policy to restrict distribution of content to only the locations in which you have distribution rights
- (E) Use Amazon Route 53 based latency-based routing policy to restrict distribution of content to only the locations in which you have distribution rights
- (F) Use Amazon Route 53 based failover routing policy to restrict distribution of content to only the locations in which you have distribution rights
- (G) Correct options:
- (H) Geolocation routing lets you choose the resources that serve your traffic based on the geographic location of your users, meaning the location that DNS queries originate from. For example, you might want all queries from Europe to be routed to an ELB load balancer in the Frankfurt region. You can also use geolocation routing to restrict the distribution of content to only the locations in which you have distribution rights.
- (I) Amazon Route 53 Routing Policy Overview:
- (J) via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () Incorrect options:
- () Use Amazon Route 53 based weighted routing policy to restrict distribution of content to only the locations in which you have distribution rights - Weighted routing lets you associate multiple resources with a single domain name (example.com) or subdomain name (acme.example.com) and choose how much traffic is routed to each resource. This can be useful for a variety of purposes, including load balancing and testing new versions of the software.
- () Use Amazon Route 53 based failover routing policy to restrict distribution of content to only the locations in which you have distribution rights - Failover routing lets you route traffic to a resource when the resource is healthy or to a different resource when the first resource is unhealthy. The primary and secondary records can route traffic to anything from an Amazon S3 bucket that is configured as a website to a complex tree of records.
- () Weighted routing or failover routing or latency routing cannot be used to restrict the distribution of content to only the locations in which you have distribution rights. So all three options above are incorrect.
- () References:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-geo
- () A retail company has developed a REST API which is deployed in an Auto Scaling group behind an Application Load Balancer. The REST API stores the user data in Amazon DynamoDB and any static content, such as images, are served via Amazon Simple Storage Service (Amazon S3). On analyzing the usage trends, it is found that 90% of the read requests are for commonly accessed data across all users.

**Answer:**
Correct Answer: **Use Amazon Route 53 based weighted routing policy to restrict distribution of content to only the locations in which you have distribution rights**

---

## Question 74

**Q:** As a Solutions Architect, which of the following would you suggest as the MOST efficient solution to improve the application performance?

**Options:**
- (A) Enable Amazon DynamoDB Accelerator (DAX) for Amazon DynamoDB and ElastiCache Memcached for Amazon S3
- (B) Enable ElastiCache Redis for DynamoDB and Amazon CloudFront for Amazon S3
- (C) Enable Amazon DynamoDB Accelerator (DAX) for Amazon DynamoDB and Amazon CloudFront for Amazon S3
- (D) Enable ElastiCache Redis for DynamoDB and ElastiCache Memcached for Amazon S3
- (E) Correct option:
- (F) Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for Amazon DynamoDB that delivers up to a 10 times performance improvement—from milliseconds to microseconds—even at millions of requests per second.
- (G) Amazon DynamoDB Accelerator (DAX) is tightly integrated with Amazon DynamoDB—you simply provision a DAX cluster, use the DAX client SDK to point your existing Amazon DynamoDB API calls at the DAX cluster, and let DAX handle the rest. Because DAX is API-compatible with Amazon DynamoDB, you don't have to make any functional application code changes. DAX is used to natively cache Amazon DynamoDB reads.
- (H) Amazon CloudFront is a content delivery network (CDN) service that delivers static and dynamic web content, video streams, and APIs around the world, securely and at scale. By design, delivering data out of Amazon CloudFront can be more cost-effective than delivering it from S3 directly to your users.
- (I) When a user requests content that you serve with CloudFront, their request is routed to a nearby Edge Location. If CloudFront has a cached copy of the requested file, CloudFront delivers it to the user, providing a fast (low-latency) response. If the file they’ve requested isn’t yet cached, CloudFront retrieves it from your origin – for example, the Amazon S3 bucket where you’ve stored your content.
- (J) So, you can use Amazon CloudFront to improve application performance to serve static content from Amazon S3.
- () Incorrect options:
- () Amazon ElastiCache for Redis is a blazing fast in-memory data store that provides sub-millisecond latency to power internet-scale real-time applications. Amazon ElastiCache for Redis is a great choice for real-time transactional and analytical processing use cases such as caching, chat/messaging, gaming leaderboards, geospatial, machine learning, media streaming, queues, real-time analytics, and session store.
- () Amazon ElastiCache for Redis Overview:
- () via - https://aws.amazon.com/elasticache/redis/
- () Although you can integrate Redis with DynamoDB, it's much more involved than using DAX which is a much better fit.
- () Amazon ElastiCache for Memcached is a Memcached-compatible in-memory key-value store service that can be used as a cache or a data store. Amazon ElastiCache for Memcached is a great choice for implementing an in-memory cache to decrease access latency, increase throughput, and ease the load off your relational or NoSQL database.
- () Amazon ElastiCache Memcached cannot be used as a cache to serve static content from Amazon S3, so both these options are incorrect.
- () References:
- () https://aws.amazon.com/dynamodb/dax/
- () https://aws.amazon.com/blogs/networking-and-content-delivery/amazon-s3-amazon-cloudfront-a-match-made-in-the-cloud/
- () https://aws.amazon.com/elasticache/redis/
- () An IT company wants to review its security best-practices after an incident was reported where a new developer on the team was assigned full access to Amazon DynamoDB. The developer accidentally deleted a couple of tables from the production environment while building out a new feature.
- () Which is the MOST effective way to address this issue so that such incidents do not recur?
- () Only root user should have full database access in the organization
- () Remove full database access for all IAM users in the organization
- () The CTO should review the permissions for each new developer's IAM user so that such incidents don't recur
- **() Use permissions boundary to control the maximum permissions employees can grant to the IAM principals** [CORRECT]
- () Permission Boundary Example:
- () via - https://aws.amazon.com/blogs/security/delegate-permission-management-to-developers-using-iam-permissions-boundaries/
- () Remove full database access for all IAM users in the organization - It is not practical to remove full access for all IAM users in the organization because a select set of users need this access for database administration. So this option is not correct.
- () The CTO should review the permissions for each new developer's IAM user so that such incidents don't recur - Likewise the CTO is not expected to review the permissions for each new developer's IAM user, as this is best done via an automated procedure. This option has been added as a distractor.
- () Only root user should have full database access in the organization - As a best practice, the root user should not access the AWS account to carry out any administrative procedures. So this option is not correct.
- () Reference:
- () https://aws.amazon.com/blogs/security/delegate-permission-management-to-developers-using-iam-permissions-boundaries/
- () An IT security consultancy is working on a solution to protect data stored in Amazon S3 from any malicious activity as well as check for any vulnerabilities on Amazon EC2 instances.

**Answer:**
Correct Answer: **Use permissions boundary to control the maximum permissions employees can grant to the IAM principals**

---

## Question 75

**Q:** Which is the MOST effective way to address this issue so that such incidents do not recur?

**Options:**
- (A) Only root user should have full database access in the organization
- (B) Remove full database access for all IAM users in the organization
- (C) The CTO should review the permissions for each new developer's IAM user so that such incidents don't recur
- **(D) Use permissions boundary to control the maximum permissions employees can grant to the IAM principals** [CORRECT]
- (E) Correct option:
- (F) Permission Boundary Example:
- (G) via - https://aws.amazon.com/blogs/security/delegate-permission-management-to-developers-using-iam-permissions-boundaries/
- (H) Incorrect options:
- (I) Remove full database access for all IAM users in the organization - It is not practical to remove full access for all IAM users in the organization because a select set of users need this access for database administration. So this option is not correct.
- (J) The CTO should review the permissions for each new developer's IAM user so that such incidents don't recur - Likewise the CTO is not expected to review the permissions for each new developer's IAM user, as this is best done via an automated procedure. This option has been added as a distractor.
- () Only root user should have full database access in the organization - As a best practice, the root user should not access the AWS account to carry out any administrative procedures. So this option is not correct.
- () Reference:
- () https://aws.amazon.com/blogs/security/delegate-permission-management-to-developers-using-iam-permissions-boundaries/
- () An IT security consultancy is working on a solution to protect data stored in Amazon S3 from any malicious activity as well as check for any vulnerabilities on Amazon EC2 instances.

**Answer:**
Correct Answer: **Use permissions boundary to control the maximum permissions employees can grant to the IAM principals**

---

## Question 76

**Q:** As a solutions architect, which of the following solutions would you suggest to help address the given requirement?

**Options:**
- (A) Use Amazon Inspector to monitor any malicious activity on data stored in Amazon S3. Use security assessments provided by Amazon GuardDuty to check for vulnerabilities on Amazon EC2 instances
- (B) Use Amazon GuardDuty to monitor any malicious activity on data stored in Amazon S3. Use security assessments provided by Amazon GuardDuty to check for vulnerabilities on Amazon EC2 instances
- (C) Use Amazon Inspector to monitor any malicious activity on data stored in Amazon S3. Use security assessments provided by Amazon Inspector to check for vulnerabilities on Amazon EC2 instances
- (D) Use Amazon GuardDuty to monitor any malicious activity on data stored in Amazon S3. Use security assessments provided by Amazon Inspector to check for vulnerabilities on Amazon EC2 instances
- (E) Correct option:
- (F) Amazon GuardDuty offers threat detection that enables you to continuously monitor and protect your AWS accounts, workloads, and data stored in Amazon S3. GuardDuty analyzes continuous streams of meta-data generated from your account and network activity found in AWS CloudTrail Events, Amazon VPC Flow Logs, and DNS Logs. It also uses integrated threat intelligence such as known malicious IP addresses, anomaly detection, and machine learning to identify threats more accurately.
- (G) How Amazon GuardDuty works:
- (H) via - https://aws.amazon.com/guardduty/
- (I) Amazon Inspector security assessments help you check for unintended network accessibility of your Amazon EC2 instances and for vulnerabilities on those EC2 instances. Amazon Inspector assessments are offered to you as pre-defined rules packages mapped to common security best practices and vulnerability definitions.
- (J) Incorrect options:
- () These three options contradict the explanation provided above, so these options are incorrect.
- () References:
- () https://aws.amazon.com/guardduty/
- () https://aws.amazon.com/inspector/
- () An Electronic Design Automation (EDA) application produces massive volumes of data that can be divided into two categories. The 'hot data' needs to be both processed and stored quickly in a parallel and distributed fashion. The 'cold data' needs to be kept for reference with quick access for reads and updates at a low cost.
- () Which of the following AWS services is BEST suited to accelerate the aforementioned chip design process?
- () AWS Glue
- () Amazon EMR
- () Amazon FSx for Lustre
- () Amazon FSx for Windows File Server
- () FSx for Lustre provides the ability to both process the 'hot data' in a parallel and distributed fashion as well as easily store the 'cold data' on Amazon S3. Therefore this option is the BEST fit for the given problem statement.
- ()  with quick access for reads and updates at low cost. Hence this option is not correct.
- () AWS Glue - AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics. AWS Glue job is meant to be used for batch ETL data processing. AWS Glue does not offer the same storage and processing speed as FSx for Lustre. So it is not the right fit for the given high-performance workflow scenario.
- () https://aws.amazon.com/fsx/lustre/
- () https://aws.amazon.com/fsx/windows/faqs/
- () Which approach best meets the company’s requirements?
- () Use AWS Control Tower to enable account access for developers. Create AWS IAM roles in each member account and manually assign permissions. Instruct developers to assume roles across accounts using the AWS CLI
- () Deploy AWS Directory Service for Microsoft Active Directory in AWS. Establish a trust relationship with the on-premises Active Directory. Use IAM roles linked to AD groups to control access to AWS resources
- () Deploy an open-source identity provider (IdP) on Amazon EC2. Synchronize it with the on-premises Active Directory and use SAML to federate access to AWS accounts. Assign IAM roles to federated users based on SAML assertions
- **() Use AWS Directory Service AD Connector to connect AWS to the on-premises Active Directory. Integrate AD Connector with AWS IAM Identity Center. Use permission sets to assign access to AWS accounts and resources based on Active Directory group membership** [CORRECT]

**Answer:**
Correct Answer: **Use AWS Directory Service AD Connector to connect AWS to the on-premises Active Directory. Integrate AD Connector with AWS IAM Identity Center. Use permission sets to assign access to AWS accounts and resources based on Active Directory group membership**

---

## Question 77

**Q:** Which of the following AWS services is BEST suited to accelerate the aforementioned chip design process?

**Options:**
- (A) AWS Glue
- (B) Amazon EMR
- (C) Amazon FSx for Lustre
- (D) Amazon FSx for Windows File Server
- (E) Correct option:
- (F) FSx for Lustre provides the ability to both process the 'hot data' in a parallel and distributed fashion as well as easily store the 'cold data' on Amazon S3. Therefore this option is the BEST fit for the given problem statement.
- (G) Incorrect options:
- (H)  with quick access for reads and updates at low cost. Hence this option is not correct.
- (I) AWS Glue - AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics. AWS Glue job is meant to be used for batch ETL data processing. AWS Glue does not offer the same storage and processing speed as FSx for Lustre. So it is not the right fit for the given high-performance workflow scenario.
- (J) References:
- () https://aws.amazon.com/fsx/lustre/
- () https://aws.amazon.com/fsx/windows/faqs/
- () Which approach best meets the company’s requirements?
- () Use AWS Control Tower to enable account access for developers. Create AWS IAM roles in each member account and manually assign permissions. Instruct developers to assume roles across accounts using the AWS CLI
- () Deploy AWS Directory Service for Microsoft Active Directory in AWS. Establish a trust relationship with the on-premises Active Directory. Use IAM roles linked to AD groups to control access to AWS resources
- () Deploy an open-source identity provider (IdP) on Amazon EC2. Synchronize it with the on-premises Active Directory and use SAML to federate access to AWS accounts. Assign IAM roles to federated users based on SAML assertions
- **() Use AWS Directory Service AD Connector to connect AWS to the on-premises Active Directory. Integrate AD Connector with AWS IAM Identity Center. Use permission sets to assign access to AWS accounts and resources based on Active Directory group membership** [CORRECT]
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_ad_connector.html
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_microsoft_ad.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html
- () https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html
- () The engineering team at an e-commerce company wants to establish a dedicated, encrypted, low latency, and high throughput connection between its data center and AWS Cloud. The engineering team has set aside sufficient time to account for the operational overhead of establishing this connection.

**Answer:**
Correct Answer: **Use AWS Directory Service AD Connector to connect AWS to the on-premises Active Directory. Integrate AD Connector with AWS IAM Identity Center. Use permission sets to assign access to AWS accounts and resources based on Active Directory group membership**

---

## Question 78

**Q:** Which approach best meets the company’s requirements?

**Options:**
- (A) Use AWS Control Tower to enable account access for developers. Create AWS IAM roles in each member account and manually assign permissions. Instruct developers to assume roles across accounts using the AWS CLI
- (B) Deploy AWS Directory Service for Microsoft Active Directory in AWS. Establish a trust relationship with the on-premises Active Directory. Use IAM roles linked to AD groups to control access to AWS resources
- (C) Deploy an open-source identity provider (IdP) on Amazon EC2. Synchronize it with the on-premises Active Directory and use SAML to federate access to AWS accounts. Assign IAM roles to federated users based on SAML assertions
- **(D) Use AWS Directory Service AD Connector to connect AWS to the on-premises Active Directory. Integrate AD Connector with AWS IAM Identity Center. Use permission sets to assign access to AWS accounts and resources based on Active Directory group membership** [CORRECT]
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_ad_connector.html
- (I) https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_microsoft_ad.html
- (J) https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html
- () https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html
- () The engineering team at an e-commerce company wants to establish a dedicated, encrypted, low latency, and high throughput connection between its data center and AWS Cloud. The engineering team has set aside sufficient time to account for the operational overhead of establishing this connection.

**Answer:**
Correct Answer: **Use AWS Directory Service AD Connector to connect AWS to the on-premises Active Directory. Integrate AD Connector with AWS IAM Identity Center. Use permission sets to assign access to AWS accounts and resources based on Active Directory group membership**

---

## Question 79

**Q:** As a solutions architect, which of the following solutions would you recommend to the company?

**Options:**
- (A) Use AWS Direct Connect to establish a connection between the data center and AWS Cloud
- (B) Use AWS Direct Connect plus virtual private network (VPN) to establish a connection between the data center and AWS Cloud
- (C) Use AWS site-to-site VPN to establish a connection between the data center and AWS Cloud
- (D) Use AWS Transit Gateway to establish a connection between the data center and AWS Cloud
- (E) Correct option:
- (F) AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS. AWS Direct Connect lets you establish a dedicated network connection between your network and one of the AWS Direct Connect locations.
- (G) With AWS Direct Connect plus VPN, you can combine one or more AWS Direct Connect dedicated network connections with the Amazon VPC VPN. This combination provides an IPsec-encrypted private connection that also reduces network costs, increases bandwidth throughput, and provides a more consistent network experience than internet-based VPN connections.
- (H) This solution combines the AWS managed benefits of the VPN solution with low latency, increased bandwidth, more consistent benefits of the AWS Direct Connect solution, and an end-to-end, secure IPsec connection. Therefore, AWS Direct Connect plus VPN is the correct solution for this use-case.
- (I) AWS Direct Connect Plus VPN:
- (J) via - https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-direct-connect-vpn.html
- () Incorrect options:
- () Use AWS Transit Gateway to establish a connection between the data center and AWS Cloud - AWS Transit Gateway is a network transit hub that you can use to interconnect your virtual private clouds (VPC) and on-premises networks. AWS Transit Gateway by itself cannot establish a low latency and high throughput connection between a data center and AWS Cloud. Hence this option is incorrect.
- () Use AWS Direct Connect to establish a connection between the data center and AWS Cloud - AWS Direct Connect by itself cannot provide an encrypted connection between a data center and AWS Cloud, so this option is ruled out.
- () References:
- () https://aws.amazon.com/directconnect/
- () https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-direct-connect-plus-vpn-network-to-amazon.html
- () A leading video streaming service delivers billions of hours of content from Amazon Simple Storage Service (Amazon S3) to customers around the world. Amazon S3 also serves as the data lake for its big data analytics solution. The data lake has a staging zone where intermediary query results are kept only for 24 hours. These results are also heavily referenced by other parts of the analytics pipeline.
- () Which of the following is the MOST cost-effective strategy for storing this intermediary query data?
- () Store the intermediary query results in Amazon S3 Glacier Instant Retrieval storage class
- **() Store the intermediary query results in Amazon S3 Standard storage class** [CORRECT]
- () Store the intermediary query results in Amazon S3 One Zone-Infrequent Access storage class
- () Store the intermediary query results in Amazon S3 Standard-Infrequent Access storage class
- () Store the intermediary query results in Amazon S3 Glacier Instant Retrieval storage class - Amazon S3 Glacier Instant Retrieval delivers the fastest access to archive storage, with the same throughput and milliseconds access as the S3 Standard and S3 Standard-IA storage classes. S3 Glacier Instant Retrieval is ideal for archive data that needs immediate access, such as medical images, news media assets, or user-generated content archives.
- () The minimum storage duration charge is 90 days, so this option is NOT cost-effective because intermediary query results need to be kept only for 24 hours. Hence this option is not correct.
- () To summarize again, S3 Standard-IA and S3 One Zone-IA have a minimum storage duration charge of 30 days (so instead of 24 hours, you end up paying for 30 days). S3 Standard-IA and S3 One Zone-IA also have retrieval charges (as the results are heavily referenced by other parts of the analytics pipeline, so the retrieval costs would be pretty high). Therefore, these storage classes are not cost optimal for the given use-case.
- () Reference:
- () https://aws.amazon.com/s3/storage-classes/
- () An organization wants to delegate access to a set of users from the development environment so that they can access some resources in the production environment which is managed under another AWS account.

**Answer:**
Correct Answer: **Store the intermediary query results in Amazon S3 Standard storage class**

---

## Question 80

**Q:** Which of the following is the MOST cost-effective strategy for storing this intermediary query data?

**Options:**
- (A) Store the intermediary query results in Amazon S3 Glacier Instant Retrieval storage class
- **(B) Store the intermediary query results in Amazon S3 Standard storage class** [CORRECT]
- (C) Store the intermediary query results in Amazon S3 One Zone-Infrequent Access storage class
- (D) Store the intermediary query results in Amazon S3 Standard-Infrequent Access storage class
- (E) Correct option:
- (F) Incorrect options:
- (G) Store the intermediary query results in Amazon S3 Glacier Instant Retrieval storage class - Amazon S3 Glacier Instant Retrieval delivers the fastest access to archive storage, with the same throughput and milliseconds access as the S3 Standard and S3 Standard-IA storage classes. S3 Glacier Instant Retrieval is ideal for archive data that needs immediate access, such as medical images, news media assets, or user-generated content archives.
- (H) The minimum storage duration charge is 90 days, so this option is NOT cost-effective because intermediary query results need to be kept only for 24 hours. Hence this option is not correct.
- (I) To summarize again, S3 Standard-IA and S3 One Zone-IA have a minimum storage duration charge of 30 days (so instead of 24 hours, you end up paying for 30 days). S3 Standard-IA and S3 One Zone-IA also have retrieval charges (as the results are heavily referenced by other parts of the analytics pipeline, so the retrieval costs would be pretty high). Therefore, these storage classes are not cost optimal for the given use-case.
- (J) Reference:
- () https://aws.amazon.com/s3/storage-classes/
- () An organization wants to delegate access to a set of users from the development environment so that they can access some resources in the production environment which is managed under another AWS account.

**Answer:**
Correct Answer: **Store the intermediary query results in Amazon S3 Standard storage class**

---

## Question 81

**Q:** As a solutions architect, which of the following steps would you recommend?

**Options:**
- (A) It is not possible to access cross-account resources
- (B) Both IAM roles and IAM users can be used interchangeably for cross-account access
- (C) Create a new IAM role with the required permissions to access the resources in the production environment. The users can then assume this IAM role while accessing the resources from the production environment
- (D) Create new IAM user credentials for the production environment and share these credentials with the set of users from the development environment
- (E) Correct option:
- (F) IAM roles allow you to delegate access to users or services that normally don't have access to your organization's AWS resources. IAM users or AWS services can assume a role to obtain temporary security credentials that can be used to make AWS API calls. Consequently, you don't have to share long-term credentials for access to a resource. Using IAM roles, it is possible to access cross-account resources.
- (G) Incorrect options:
- (H) Create new IAM user credentials for the production environment and share these credentials with the set of users from the development environment - There is no need to create new IAM user credentials for the production environment, as you can use IAM roles to access cross-account resources.
- (I) It is not possible to access cross-account resources - You can use IAM roles to access cross-account resources.
- (J) Both IAM roles and IAM users can be used interchangeably for cross-account access - IAM roles and IAM users are separate IAM entities and should not be mixed. Only IAM roles can be used to access cross-account resources.
- () Reference:
- () https://aws.amazon.com/iam/features/manage-roles/
- () An enterprise runs a microservices-based application on Amazon EKS, deployed on EC2 worker nodes. The application includes a frontend UI service that interacts with Amazon DynamoDB and a data-processing service that stores and retrieves files from Amazon S3. The organization needs to strictly enforce least privilege access: the UI Pods must access only DynamoDB, and the data-processing Pods must access only S3.
- () Which solution will best enforce these access controls within the EKS cluster?
- () Create separate Kubernetes service accounts for the UI and data services. Use IAM Roles for Service Accounts (IRSA) to map each service account to an IAM role with only the required permissions. Assign DynamoDB access to the UI Pods and S3 access to the data Pods
- () Attach an IAM policy directly to each Pod using Kubernetes annotations. Assign the S3 policy to data-service Pods and the DynamoDB policy to UI Pods
- () Create IAM policies for DynamoDB and S3 access, and attach both to the EC2 instance profile used by the EKS nodes. Use Kubernetes role-based access control (RBAC) to control service-level permissions within the cluster
- () Create one Kubernetes service account shared across all Pods. Attach a single IAM role to this account with both AmazonS3FullAccess and AmazonDynamoDBFullAccess policies
- () References:
- () https://docs.aws.amazon.com/eks/latest/userguide/iam-roles-for-service-accounts.html
- () https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html
- () A logistics company is building a multi-tier application to track the location of its trucks during peak operating hours. The company wants these data points to be accessible in real-time in its analytics platform via a REST API. The company has hired you as an AWS Certified Solutions Architect Associate to build a multi-tier solution to store and retrieve this location data for analysis.
- () Which of the following options addresses the given use case?
- () Leverage Amazon Athena with Amazon S3
- () Leverage Amazon API Gateway with AWS Lambda
- () Leverage Amazon QuickSight with Amazon Redshift
- **() Leverage Amazon API Gateway with Amazon Kinesis Data Analytics** [CORRECT]
- () Amazon API Gateway is a fully managed service that allows you to publish, maintain, monitor, and secure APIs at any scale. Amazon API Gateway offers two options to create RESTful APIs, HTTP APIs and REST APIs, as well as an option to create WebSocket APIs.
- () Amazon API Gateway:
- () via - https://aws.amazon.com/blogs/aws/amazon-rds-custom-for-oracle-new-control-capabilities-in-database-environment/
- () For the given use case, you can use Amazon API Gateway to create a REST API that handles incoming requests having location data from the trucks and sends it to the Kinesis Data Analytics application on the back end.
- () Amazon Kinesis Data Analytics:
- () via - https://aws.amazon.com/kinesis/data-analytics/

**Answer:**
Correct Answer: **Leverage Amazon API Gateway with Amazon Kinesis Data Analytics**

---

## Question 82

**Q:** Which solution will best enforce these access controls within the EKS cluster?

**Options:**
- (A) Create separate Kubernetes service accounts for the UI and data services. Use IAM Roles for Service Accounts (IRSA) to map each service account to an IAM role with only the required permissions. Assign DynamoDB access to the UI Pods and S3 access to the data Pods
- (B) Attach an IAM policy directly to each Pod using Kubernetes annotations. Assign the S3 policy to data-service Pods and the DynamoDB policy to UI Pods
- (C) Create IAM policies for DynamoDB and S3 access, and attach both to the EC2 instance profile used by the EKS nodes. Use Kubernetes role-based access control (RBAC) to control service-level permissions within the cluster
- (D) Create one Kubernetes service account shared across all Pods. Attach a single IAM role to this account with both AmazonS3FullAccess and AmazonDynamoDBFullAccess policies
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/eks/latest/userguide/iam-roles-for-service-accounts.html
- (I) https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html
- (J) A logistics company is building a multi-tier application to track the location of its trucks during peak operating hours. The company wants these data points to be accessible in real-time in its analytics platform via a REST API. The company has hired you as an AWS Certified Solutions Architect Associate to build a multi-tier solution to store and retrieve this location data for analysis.
- () Which of the following options addresses the given use case?
- () Leverage Amazon Athena with Amazon S3
- () Leverage Amazon API Gateway with AWS Lambda
- () Leverage Amazon QuickSight with Amazon Redshift
- **() Leverage Amazon API Gateway with Amazon Kinesis Data Analytics** [CORRECT]
- () Amazon API Gateway is a fully managed service that allows you to publish, maintain, monitor, and secure APIs at any scale. Amazon API Gateway offers two options to create RESTful APIs, HTTP APIs and REST APIs, as well as an option to create WebSocket APIs.
- () Amazon API Gateway:
- () via - https://aws.amazon.com/blogs/aws/amazon-rds-custom-for-oracle-new-control-capabilities-in-database-environment/
- () For the given use case, you can use Amazon API Gateway to create a REST API that handles incoming requests having location data from the trucks and sends it to the Kinesis Data Analytics application on the back end.
- () Amazon Kinesis Data Analytics:
- () via - https://aws.amazon.com/kinesis/data-analytics/
- () Leverage Amazon Athena with Amazon S3 - Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena cannot be used to build a REST API to consume data from the source. So this option is incorrect.
- () Leverage Amazon QuickSight with Amazon Redshift - QuickSight is a cloud-native, serverless business intelligence service. Quicksight cannot be used to build a REST API to consume data from the source. Redshift is a fully managed AWS cloud data warehouse. So this option is incorrect.
- () Leverage Amazon API Gateway with AWS Lambda - You cannot use Lambda to store and retrieve the location data for analysis, so this option is incorrect.
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/integrating-api-with-aws-services-kinesis.html
- () https://aws.amazon.com/kinesis/data-analytics/
- () https://aws.amazon.com/kinesis/data-analytics/faqs/
- () The engineering team at an in-home fitness company is evaluating multiple in-memory data stores with the ability to power its on-demand, live leaderboard. The company's leaderboard requires high availability, low latency, and real-time processing to deliver customizable user data for the community of users working out together virtually from the comfort of their home.
- () As a solutions architect, which of the following solutions would you recommend? (Select two)
- () Correct selection
- () Power the on-demand, live leaderboard using Amazon DynamoDB with DynamoDB Accelerator (DAX) as it meets the in-memory, high availability, low latency requirements
- () Power the on-demand, live leaderboard using Amazon Neptune as it meets the in-memory, high availability, low latency requirements
- () Power the on-demand, live leaderboard using Amazon DynamoDB as it meets the in-memory, high availability, low latency requirements
- () Power the on-demand, live leaderboard using Amazon ElastiCache for Redis as it meets the in-memory, high availability, low latency requirements

**Answer:**
Correct Answer: **Leverage Amazon API Gateway with Amazon Kinesis Data Analytics**

---

## Question 83

**Q:** Which of the following options addresses the given use case?

**Options:**
- (A) Leverage Amazon Athena with Amazon S3
- (B) Leverage Amazon API Gateway with AWS Lambda
- (C) Leverage Amazon QuickSight with Amazon Redshift
- **(D) Leverage Amazon API Gateway with Amazon Kinesis Data Analytics** [CORRECT]
- (E) Correct option:
- (F) Amazon API Gateway is a fully managed service that allows you to publish, maintain, monitor, and secure APIs at any scale. Amazon API Gateway offers two options to create RESTful APIs, HTTP APIs and REST APIs, as well as an option to create WebSocket APIs.
- (G) Amazon API Gateway:
- (H) via - https://aws.amazon.com/blogs/aws/amazon-rds-custom-for-oracle-new-control-capabilities-in-database-environment/
- (I) For the given use case, you can use Amazon API Gateway to create a REST API that handles incoming requests having location data from the trucks and sends it to the Kinesis Data Analytics application on the back end.
- (J) Amazon Kinesis Data Analytics:
- () via - https://aws.amazon.com/kinesis/data-analytics/
- () Incorrect options:
- () Leverage Amazon Athena with Amazon S3 - Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena cannot be used to build a REST API to consume data from the source. So this option is incorrect.
- () Leverage Amazon QuickSight with Amazon Redshift - QuickSight is a cloud-native, serverless business intelligence service. Quicksight cannot be used to build a REST API to consume data from the source. Redshift is a fully managed AWS cloud data warehouse. So this option is incorrect.
- () Leverage Amazon API Gateway with AWS Lambda - You cannot use Lambda to store and retrieve the location data for analysis, so this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/integrating-api-with-aws-services-kinesis.html
- () https://aws.amazon.com/kinesis/data-analytics/
- () https://aws.amazon.com/kinesis/data-analytics/faqs/
- () The engineering team at an in-home fitness company is evaluating multiple in-memory data stores with the ability to power its on-demand, live leaderboard. The company's leaderboard requires high availability, low latency, and real-time processing to deliver customizable user data for the community of users working out together virtually from the comfort of their home.
- () As a solutions architect, which of the following solutions would you recommend? (Select two)
- () Correct selection
- () Power the on-demand, live leaderboard using Amazon DynamoDB with DynamoDB Accelerator (DAX) as it meets the in-memory, high availability, low latency requirements
- () Power the on-demand, live leaderboard using Amazon Neptune as it meets the in-memory, high availability, low latency requirements
- () Power the on-demand, live leaderboard using Amazon DynamoDB as it meets the in-memory, high availability, low latency requirements
- () Power the on-demand, live leaderboard using Amazon ElastiCache for Redis as it meets the in-memory, high availability, low latency requirements
- () Power the on-demand, live leaderboard using Amazon RDS for Aurora as it meets the in-memory, high availability, low latency requirements
- () Correct options:
- () Amazon ElastiCache for Redis Overview:
- () Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multiregion, multimaster, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DAX is a DynamoDB-compatible caching service that enables you to benefit from fast in-memory performance for demanding applications. So DynamoDB with DAX can be used to power the live leaderboard.
- () Power the on-demand, live leaderboard using Amazon Neptune as it meets the in-memory, high availability, low latency requirements - Amazon Neptune is a fast, reliable, fully-managed graph database service that makes it easy to build and run applications that work with highly connected datasets. Neptune is not an in-memory database, so this option is not correct.
- () Power the on-demand, live leaderboard using Amazon DynamoDB as it meets the in-memory, high availability, low latency requirements - DynamoDB is not an in-memory database, so this option is not correct.
- () https://aws.amazon.com/elasticache/
- () https://aws.amazon.com/elasticache/redis/
- () https://aws.amazon.com/dynamodb/dax/

**Answer:**
Correct Answer: **Leverage Amazon API Gateway with Amazon Kinesis Data Analytics**

---

## Question 84

**Q:** As a solutions architect, which of the following solutions would you recommend? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Power the on-demand, live leaderboard using Amazon DynamoDB with DynamoDB Accelerator (DAX) as it meets the in-memory, high availability, low latency requirements
- (C) Power the on-demand, live leaderboard using Amazon Neptune as it meets the in-memory, high availability, low latency requirements
- (D) Power the on-demand, live leaderboard using Amazon DynamoDB as it meets the in-memory, high availability, low latency requirements
- (E) Power the on-demand, live leaderboard using Amazon ElastiCache for Redis as it meets the in-memory, high availability, low latency requirements
- (F) Power the on-demand, live leaderboard using Amazon RDS for Aurora as it meets the in-memory, high availability, low latency requirements
- (G) Correct options:
- (H) Amazon ElastiCache for Redis Overview:
- (I) Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multiregion, multimaster, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DAX is a DynamoDB-compatible caching service that enables you to benefit from fast in-memory performance for demanding applications. So DynamoDB with DAX can be used to power the live leaderboard.
- (J) Incorrect options:
- () Power the on-demand, live leaderboard using Amazon Neptune as it meets the in-memory, high availability, low latency requirements - Amazon Neptune is a fast, reliable, fully-managed graph database service that makes it easy to build and run applications that work with highly connected datasets. Neptune is not an in-memory database, so this option is not correct.
- () Power the on-demand, live leaderboard using Amazon DynamoDB as it meets the in-memory, high availability, low latency requirements - DynamoDB is not an in-memory database, so this option is not correct.
- () References:
- () https://aws.amazon.com/elasticache/
- () https://aws.amazon.com/elasticache/redis/
- () https://aws.amazon.com/dynamodb/dax/

**Answer:**
Correct Answer: **Correct selection**

---

## Question 85

**Q:** As a solutions architect, which of the following would you suggest as the BEST possible solution to this issue?

**Options:**
- (A) Amazon SNS has hit a scalability limit, so the team needs to contact AWS support to raise the account limit
- **(B) Amazon SNS message deliveries to AWS Lambda have crossed the account concurrency quota for AWS Lambda, so the team needs to contact AWS support to raise the account limit** [CORRECT]
- (C) The engineering team needs to provision more servers running the Amazon SNS service
- (D) The engineering team needs to provision more servers running the AWS Lambda service
- (E) Correct option:
- (F) Amazon Simple Notification Service (Amazon SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications.
- (G) How Amazon SNS Works:
- (H) via - https://aws.amazon.com/sns/
- (I) With AWS Lambda, you can run code without provisioning or managing servers. You pay only for the compute time that you consume—there’s no charge when your code isn’t running.
- (J) AWS Lambda currently supports 1000 concurrent executions per AWS account per region. If your Amazon SNS message deliveries to AWS Lambda contribute to crossing these concurrency quotas, your Amazon SNS message deliveries will be throttled. You need to contact AWS support to raise the account limit. Therefore this option is correct.
- () Incorrect options:
- () Amazon SNS has hit a scalability limit, so the team needs to contact AWS support to raise the account limit - Amazon SNS leverages the proven AWS cloud to dynamically scale with your application. You don't need to contact AWS support, as SNS is a fully managed service, taking care of the heavy lifting related to capacity planning, provisioning, monitoring, and patching. Therefore, this option is incorrect.
- () As both AWS Lambda and Amazon SNS are serverless and fully managed services, the engineering team cannot provision more servers. Both of these options are incorrect.
- () References:
- () https://aws.amazon.com/sns/
- () https://aws.amazon.com/sns/faqs/
- () A retail company runs a customer management system backed by a Microsoft SQL Server database. The system is tightly integrated with applications that rely on T-SQL queries. The company wants to modernize its infrastructure by migrating to Amazon Aurora PostgreSQL, but it needs to avoid major modifications to the existing application logic.
- () Which combination of actions should the company take to achieve this goal with minimal application refactoring? (Select two)
- () Correct selection
- () Deploy Babelfish for Aurora PostgreSQL to enable support for T-SQL commands
- () Use AWS Schema Conversion Tool (AWS SCT) along with AWS Database Migration Service (AWS DMS) to migrate the schema and data
- () Configure Amazon Aurora PostgreSQL with a custom endpoint that emulates Microsoft SQL Server behavior
- () Use AWS Glue to convert T-SQL queries to PostgreSQL-compatible SQL during the migration
- () Use Amazon Aurora Global Database to replicate data across regions for compatibility
- () Correct options:
- () Babelfish allows Aurora PostgreSQL to understand T-SQL (Microsoft SQL Server's query language) and SQL Server wire protocol, enabling applications to communicate with Aurora using SQL Server-style queries with minimal code changes. This is ideal for minimizing application code refactoring.
- () via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/babelfish.html
- () The AWS Schema Conversion Tool (SCT) helps convert the SQL Server schema to PostgreSQL-compatible syntax, and AWS Database Migration Service (DMS) can move the actual data with minimal downtime. These tools are designed for database migration and are essential for schema and data transfer.
- () Configure Amazon Aurora PostgreSQL with a custom endpoint that emulates Microsoft SQL Server behavior - Aurora endpoints do not provide protocol-level emulation of SQL Server unless Babelfish is explicitly enabled. There is no feature to make Aurora natively emulate SQL Server behavior without Babelfish.
- () Use Amazon Aurora Global Database to replicate data across regions for compatibility - Aurora Global Database helps with cross-region disaster recovery and read scalability, but it does not assist with SQL Server compatibility or reduce application code changes.
- () Use AWS Glue to convert T-SQL queries to PostgreSQL-compatible SQL during the migration - AWS Glue is primarily used for ETL and data transformation, not for application SQL query conversion. It cannot translate T-SQL into PostgreSQL syntax.
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/babelfish.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/babelfish-compatibility.html
- () A healthcare startup needs to enforce compliance and regulatory guidelines for objects stored in Amazon S3. One of the key requirements is to provide adequate protection against accidental deletion of objects.

**Answer:**
Correct Answer: **Amazon SNS message deliveries to AWS Lambda have crossed the account concurrency quota for AWS Lambda, so the team needs to contact AWS support to raise the account limit**

---

## Question 86

**Q:** Which combination of actions should the company take to achieve this goal with minimal application refactoring? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Deploy Babelfish for Aurora PostgreSQL to enable support for T-SQL commands
- (C) Use AWS Schema Conversion Tool (AWS SCT) along with AWS Database Migration Service (AWS DMS) to migrate the schema and data
- (D) Configure Amazon Aurora PostgreSQL with a custom endpoint that emulates Microsoft SQL Server behavior
- (E) Use AWS Glue to convert T-SQL queries to PostgreSQL-compatible SQL during the migration
- (F) Use Amazon Aurora Global Database to replicate data across regions for compatibility
- (G) Correct options:
- (H) Babelfish allows Aurora PostgreSQL to understand T-SQL (Microsoft SQL Server's query language) and SQL Server wire protocol, enabling applications to communicate with Aurora using SQL Server-style queries with minimal code changes. This is ideal for minimizing application code refactoring.
- (I) via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/babelfish.html
- (J) The AWS Schema Conversion Tool (SCT) helps convert the SQL Server schema to PostgreSQL-compatible syntax, and AWS Database Migration Service (DMS) can move the actual data with minimal downtime. These tools are designed for database migration and are essential for schema and data transfer.
- () Incorrect options:
- () Configure Amazon Aurora PostgreSQL with a custom endpoint that emulates Microsoft SQL Server behavior - Aurora endpoints do not provide protocol-level emulation of SQL Server unless Babelfish is explicitly enabled. There is no feature to make Aurora natively emulate SQL Server behavior without Babelfish.
- () Use Amazon Aurora Global Database to replicate data across regions for compatibility - Aurora Global Database helps with cross-region disaster recovery and read scalability, but it does not assist with SQL Server compatibility or reduce application code changes.
- () Use AWS Glue to convert T-SQL queries to PostgreSQL-compatible SQL during the migration - AWS Glue is primarily used for ETL and data transformation, not for application SQL query conversion. It cannot translate T-SQL into PostgreSQL syntax.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/babelfish.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/babelfish-compatibility.html
- () A healthcare startup needs to enforce compliance and regulatory guidelines for objects stored in Amazon S3. One of the key requirements is to provide adequate protection against accidental deletion of objects.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 87

**Q:** As a solutions architect, what are your recommendations to address these guidelines? (Select two) ?

**Options:**
- (A) Correct selection
- (B) Enable multi-factor authentication (MFA) delete on the Amazon S3 bucket
- (C) Enable versioning on the Amazon S3 bucket
- (D) Create an event trigger on deleting any Amazon S3 object. The event invokes an Amazon Simple Notification Service (Amazon SNS) notification via email to the IT manager
- (E) Change the configuration on Amazon S3 console so that the user needs to provide additional confirmation while deleting any Amazon S3 object
- (F) Establish a process to get managerial approval for deleting Amazon S3 objects
- (G) Correct options:
- (H) Versioning is a means of keeping multiple variants of an object in the same bucket. You can use versioning to preserve, retrieve, and restore every version of every object stored in your Amazon S3 bucket. Versioning-enabled buckets enable you to recover objects from accidental deletion or overwrite.
- (I) For example:
- (J) If you overwrite an object, it results in a new object version in the bucket. You can always restore the previous version. If you delete an object, instead of removing it permanently, Amazon S3 inserts a delete marker, which becomes the current object version. You can always restore the previous version. Hence, this is the correct option.
- () Versioning Overview:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html
- () To provide additional protection, multi-factor authentication (MFA) delete can be enabled. MFA delete requires secondary authentication to take place before objects can be permanently deleted from an Amazon S3 bucket. Hence, this is the correct option.
- () Incorrect options:
- () Create an event trigger on deleting any Amazon S3 object. The event invokes an Amazon Simple Notification Service (Amazon SNS) notification via email to the IT manager - Sending an event trigger after object deletion does not meet the objective of preventing object deletion by mistake because the object has already been deleted. So, this option is incorrect.
- () Establish a process to get managerial approval for deleting Amazon S3 objects - This option for getting managerial approval is just a distractor.
- () Change the configuration on Amazon S3 console so that the user needs to provide additional confirmation while deleting any Amazon S3 object - There is no provision to set up Amazon S3 configuration to ask for additional confirmation before deleting an object. This option is incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingMFADelete.html
- () A new DevOps engineer has just joined a development team and wants to understand the replication capabilities for Amazon RDS Multi-AZ deployment as well as Amazon RDS Read-replicas.
- () Which of the following correctly summarizes these capabilities for the given database?
- () Multi-AZ follows asynchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow asynchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region
- **() Multi-AZ follows synchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow asynchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region** [CORRECT]
- () Multi-AZ follows asynchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow synchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region
- () Multi-AZ follows asynchronous replication and spans one Availability Zone (AZ) within a single region. Read replicas follow synchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region
- () Correct option:
- () Amazon RDS Multi-AZ deployments provide enhanced availability and durability for RDS database (DB) instances, making them a natural fit for production database workloads. When you provision a Multi-AZ DB Instance, Amazon RDS automatically creates a primary DB Instance and synchronously replicates the data to a standby instance in a different Availability Zone (AZ). Multi-AZ spans at least two Availability Zones (AZs) within a single region.
- () Amazon RDS replicates all databases in the source DB instance. Read replicas can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region.
- () Exam Alert:
- () Please review this comparison vis-a-vis Multi-AZ vs Read Replica for Amazon RDS:
- () via - https://aws.amazon.com/rds/features/multi-az/
- () These three options contradict the earlier details provided in the explanation. To summarize, Multi-AZ deployment follows synchronous replication for Amazon RDS. Hence these options are incorrect.
- () https://aws.amazon.com/rds/features/multi-az/
- () https://aws.amazon.com/rds/features/read-replicas/
- () A news network uses Amazon Simple Storage Service (Amazon S3) to aggregate the raw video footage from its reporting teams across the US. The news network has recently expanded into new geographies in Europe and Asia. The technical teams at the overseas branch offices have reported huge delays in uploading large video files to the destination Amazon S3 bucket.

**Answer:**
Correct Answer: **Multi-AZ follows synchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow asynchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region**

---

## Question 88

**Q:** Which of the following correctly summarizes these capabilities for the given database?

**Options:**
- (A) Multi-AZ follows asynchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow asynchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region
- (B) Multi-AZ follows synchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow asynchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region
- (C) Multi-AZ follows asynchronous replication and spans at least two Availability Zones (AZs) within a single region. Read replicas follow synchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region
- (D) Multi-AZ follows asynchronous replication and spans one Availability Zone (AZ) within a single region. Read replicas follow synchronous replication and can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region
- (E) Correct option:
- (F) Amazon RDS Multi-AZ deployments provide enhanced availability and durability for RDS database (DB) instances, making them a natural fit for production database workloads. When you provision a Multi-AZ DB Instance, Amazon RDS automatically creates a primary DB Instance and synchronously replicates the data to a standby instance in a different Availability Zone (AZ). Multi-AZ spans at least two Availability Zones (AZs) within a single region.
- (G) Amazon RDS replicates all databases in the source DB instance. Read replicas can be within an Availability Zone (AZ), Cross-AZ, or Cross-Region.
- (H) Exam Alert:
- (I) Please review this comparison vis-a-vis Multi-AZ vs Read Replica for Amazon RDS:
- (J) via - https://aws.amazon.com/rds/features/multi-az/
- () Incorrect Options:
- () These three options contradict the earlier details provided in the explanation. To summarize, Multi-AZ deployment follows synchronous replication for Amazon RDS. Hence these options are incorrect.
- () References:
- () https://aws.amazon.com/rds/features/multi-az/
- () https://aws.amazon.com/rds/features/read-replicas/
- () A news network uses Amazon Simple Storage Service (Amazon S3) to aggregate the raw video footage from its reporting teams across the US. The news network has recently expanded into new geographies in Europe and Asia. The technical teams at the overseas branch offices have reported huge delays in uploading large video files to the destination Amazon S3 bucket.
- () Which of the following are the MOST cost-effective options to improve the file upload speed into Amazon S3 (Select two)
- () Correct selection
- () Use multipart uploads for faster file uploads into the destination Amazon S3 bucket
- () Create multiple AWS Direct Connect connections between the AWS Cloud and branch offices in Europe and Asia. Use the direct connect connections for faster file uploads into Amazon S3
- () Create multiple AWS Site-to-Site VPN connections between the AWS Cloud and branch offices in Europe and Asia. Use these VPN connections for faster file uploads into Amazon S3
- () Use AWS Global Accelerator for faster file uploads into the destination Amazon S3 bucket
- () Use Amazon S3 Transfer Acceleration (Amazon S3TA) to enable faster file uploads into the destination S3 bucket
- () Correct options:
- () Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Amazon S3TA takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html
- () A healthcare company uses its on-premises infrastructure to run legacy applications that require specialized customizations to the underlying Oracle database as well as its host operating system (OS). The company also wants to improve the availability of the Oracle database layer. The company has hired you as an AWS Certified Solutions Architect – Associate to build a solution on AWS that meets these requirements while minimizing the underlying infrastructure maintenance effort.
- () Which of the following options represents the best solution for this use case?
- () Leverage cross AZ read-replica configuration of Amazon RDS for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
- **() Leverage multi-AZ configuration of Amazon RDS Custom for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system** [CORRECT]
- () Deploy the Oracle database layer on multiple Amazon EC2 instances spread across two Availability Zones (AZs). This deployment configuration guarantees high availability and also allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
- () Leverage multi-AZ configuration of Amazon RDS for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system

**Answer:**
Correct Answer: **Leverage multi-AZ configuration of Amazon RDS Custom for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system**

---

## Question 89

**Q:** Which of the following options represents the best solution for this use case?

**Options:**
- (A) Leverage cross AZ read-replica configuration of Amazon RDS for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
- (B) Leverage multi-AZ configuration of Amazon RDS Custom for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
- (C) Deploy the Oracle database layer on multiple Amazon EC2 instances spread across two Availability Zones (AZs). This deployment configuration guarantees high availability and also allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
- (D) Leverage multi-AZ configuration of Amazon RDS for Oracle that allows the Database Administrator (DBA) to access and customize the database environment and the underlying operating system
- (E) Correct option:
- (F) Amazon RDS is a managed service that makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while managing time-consuming database administration tasks. Amazon RDS can automatically back up your database and keep your database software up to date with the latest version. However, RDS does not allow you to access the host OS of the database.
- (G) Amazon RDS Custom for Oracle:
- (H) via - https://aws.amazon.com/blogs/aws/amazon-rds-custom-for-oracle-new-control-capabilities-in-database-environment/
- (I) Incorrect options:
- (J) Amazon RDS for Oracle does not allow you to access and customize your database server host and operating system. Therefore, both these options are incorrect.
- () References:
- () https://aws.amazon.com/blogs/aws/amazon-rds-custom-for-oracle-new-control-capabilities-in-database-environment/
- () https://aws.amazon.com/rds/faqs/
- () A file-hosting service uses Amazon Simple Storage Service (Amazon S3) under the hood to power its storage offerings. Currently all the customer files are uploaded directly under a single Amazon S3 bucket. The engineering team has started seeing scalability issues where customer file uploads have started failing during the peak access hours with more than 5000 requests per second.
- () Which of the following is the MOST resource efficient and cost-optimal way of addressing this issue?
- () Change the application architecture to use Amazon Elastic File System (Amazon EFS) instead of Amazon S3 for storing the customers' uploaded files
- () Change the application architecture to create a new Amazon S3 bucket for each day's data and then upload the daily files directly under that day's bucket
- () Change the application architecture to create a new Amazon S3 bucket for each customer and then upload each customer's files directly under the respective buckets
- () Change the application architecture to create customer-specific custom prefixes within the single Amazon S3 bucket and then upload the daily files into those prefixed locations
- () Optimizing Amazon S3 Performance:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance.html
- () Change the application architecture to create a new Amazon S3 bucket for each day's data and then upload the daily files directly under that day's bucket - Creating a new Amazon S3 bucket for each new day's data is also an inefficient way of handling resource availability (S3 buckets need to be globally unique) as some of the bucket names may not be available for daily data processing. Moreover, this is really not required as we can use S3 prefixes to improve the performance.
- () Change the application architecture to use Amazon Elastic File System (Amazon EFS) instead of Amazon S3 for storing the customers' uploaded files - Amazon EFS is a costlier storage option compared to Amazon S3, so it is ruled out.
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance.html
- () Which solution will meet these requirements with the LEAST operational overhead?
- **() Expose an Amazon API Gateway REST API endpoint to receive transaction requests from mobile clients. Integrate the API with AWS Lambda to perform basic validation. For backend processing, deploy the long-running application to Amazon ECS using the Fargate launch type, allowing ECS to manage compute and memory provisioning automatically, with no server management required** [CORRECT]
- () Configure Amazon SQS to receive encrypted payment notifications from mobile devices. Use Amazon EventBridge rules to extract the payload and perform validation. Route the messages to a backend system hosted on Amazon Lightsail instances with dynamic scaling policies based on memory thresholds and instance health checks
- () Build a REST API using Amazon API Gateway. Integrate it with an AWS Step Functions state machine for validation. Launch the backend application using Amazon EKS with self-managed nodes, and use Kubernetes Jobs to handle transaction processing workflows. Manually scale the cluster based on demand
- () Create an Amazon API Gateway endpoint to receive transaction requests from mobile devices. Use AWS Lambda to validate the transactions. For backend processing, deploy the application on Amazon EKS Anywhere, running on on-premises servers in the company’s data center. Use a custom provisioning script to scale Kubernetes worker nodes based on transaction volume

**Answer:**
Correct Answer: **Expose an Amazon API Gateway REST API endpoint to receive transaction requests from mobile clients. Integrate the API with AWS Lambda to perform basic validation. For backend processing, deploy the long-running application to Amazon ECS using the Fargate launch type, allowing ECS to manage compute and memory provisioning automatically, with no server management required**

---

## Question 90

**Q:** Which of the following is the MOST resource efficient and cost-optimal way of addressing this issue?

**Options:**
- (A) Change the application architecture to use Amazon Elastic File System (Amazon EFS) instead of Amazon S3 for storing the customers' uploaded files
- (B) Change the application architecture to create a new Amazon S3 bucket for each day's data and then upload the daily files directly under that day's bucket
- (C) Change the application architecture to create a new Amazon S3 bucket for each customer and then upload each customer's files directly under the respective buckets
- (D) Change the application architecture to create customer-specific custom prefixes within the single Amazon S3 bucket and then upload the daily files into those prefixed locations
- (E) Correct option:
- (F) Optimizing Amazon S3 Performance:
- (G) via - https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance.html
- (H) Incorrect options:
- (I) Change the application architecture to create a new Amazon S3 bucket for each day's data and then upload the daily files directly under that day's bucket - Creating a new Amazon S3 bucket for each new day's data is also an inefficient way of handling resource availability (S3 buckets need to be globally unique) as some of the bucket names may not be available for daily data processing. Moreover, this is really not required as we can use S3 prefixes to improve the performance.
- (J) Change the application architecture to use Amazon Elastic File System (Amazon EFS) instead of Amazon S3 for storing the customers' uploaded files - Amazon EFS is a costlier storage option compared to Amazon S3, so it is ruled out.
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance.html
- () Which solution will meet these requirements with the LEAST operational overhead?
- **() Expose an Amazon API Gateway REST API endpoint to receive transaction requests from mobile clients. Integrate the API with AWS Lambda to perform basic validation. For backend processing, deploy the long-running application to Amazon ECS using the Fargate launch type, allowing ECS to manage compute and memory provisioning automatically, with no server management required** [CORRECT]
- () Configure Amazon SQS to receive encrypted payment notifications from mobile devices. Use Amazon EventBridge rules to extract the payload and perform validation. Route the messages to a backend system hosted on Amazon Lightsail instances with dynamic scaling policies based on memory thresholds and instance health checks
- () Build a REST API using Amazon API Gateway. Integrate it with an AWS Step Functions state machine for validation. Launch the backend application using Amazon EKS with self-managed nodes, and use Kubernetes Jobs to handle transaction processing workflows. Manually scale the cluster based on demand
- () Create an Amazon API Gateway endpoint to receive transaction requests from mobile devices. Use AWS Lambda to validate the transactions. For backend processing, deploy the application on Amazon EKS Anywhere, running on on-premises servers in the company’s data center. Use a custom provisioning script to scale Kubernetes worker nodes based on transaction volume
- () What is serverless development?
- () via - https://docs.aws.amazon.com/serverless/latest/devguide/welcome.html
- () References:
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html
- () https://docs.aws.amazon.com/serverless/latest/devguide/welcome.html
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-set-up-simple-proxy.html
- () https://aws.amazon.com/eks/eks-anywhere/
- () The engineering team at a data analytics company has observed that its flagship application functions at its peak performance when the underlying Amazon Elastic Compute Cloud (Amazon EC2) instances have a CPU utilization of about 50%. The application is built on a fleet of Amazon EC2 instances managed under an Auto Scaling group. The workflow requests are handled by an internal Application Load Balancer that routes the requests to the instances.

**Answer:**
Correct Answer: **Expose an Amazon API Gateway REST API endpoint to receive transaction requests from mobile clients. Integrate the API with AWS Lambda to perform basic validation. For backend processing, deploy the long-running application to Amazon ECS using the Fargate launch type, allowing ECS to manage compute and memory provisioning automatically, with no server management required**

---

## Question 91

**Q:** What is serverless development?

**Options:**
- **(A) via - https://docs.aws.amazon.com/serverless/latest/devguide/welcome.html** [CORRECT]
- (B) Incorrect options:
- (C) References:
- (D) https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html
- (E) https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html
- (F) https://docs.aws.amazon.com/serverless/latest/devguide/welcome.html
- (G) https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-set-up-simple-proxy.html
- (H) https://aws.amazon.com/eks/eks-anywhere/
- (I) The engineering team at a data analytics company has observed that its flagship application functions at its peak performance when the underlying Amazon Elastic Compute Cloud (Amazon EC2) instances have a CPU utilization of about 50%. The application is built on a fleet of Amazon EC2 instances managed under an Auto Scaling group. The workflow requests are handled by an internal Application Load Balancer that routes the requests to the instances.

**Answer:**
Correct Answer: **via - https://docs.aws.amazon.com/serverless/latest/devguide/welcome.html**

---

## Question 92

**Q:** As a solutions architect, what would you recommend so that the application runs near its peak performance state?

**Options:**
- (A) Configure the Auto Scaling group to use target tracking policy and set the CPU utilization as the target metric with a target value of 50%
- (B) Configure the Auto Scaling group to use step scaling policy and set the CPU utilization as the target metric with a target value of 50%
- (C) Configure the Auto Scaling group to use simple scaling policy and set the CPU utilization as the target metric with a target value of 50%
- (D) Configure the Auto Scaling group to use a Amazon Cloudwatch alarm triggered on a CPU utilization threshold of 50%
- (E) Correct option:
- (F) An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies.
- (G) With target tracking scaling policies, you select a scaling metric and set a target value. Amazon EC2 Auto Scaling creates and manages the CloudWatch alarms that trigger the scaling policy and calculates the scaling adjustment based on the metric and the target value. The scaling policy adds or removes capacity as required to keep the metric at, or close to, the specified target value.
- (H) For example, you can use target tracking scaling to:
- (I) Configure a target tracking scaling policy to keep the average aggregate CPU utilization of your Auto Scaling group at 50 percent. This meets the requirements specified in the given use-case and therefore, this is the correct option.
- (J) Target Tracking Policy Overview:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
- () Incorrect options:
- () With step scaling and simple scaling, you choose scaling metrics and threshold values for the Amazon CloudWatch alarms that trigger the scaling process. Neither step scaling nor simple scaling can be configured to use a target metric for CPU utilization, hence both these options are incorrect.
- () Configure the Auto Scaling group to use a Amazon Cloudwatch alarm triggered on a CPU utilization threshold of 50% - An Auto Scaling group cannot directly use a Cloudwatch alarm as the source for a scale-in or scale-out event, hence this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroup.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-target-tracking.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html
- () The development team at an e-commerce startup has set up multiple microservices running on Amazon EC2 instances under an Application Load Balancer. The team wants to route traffic to multiple back-end services based on the URL path of the HTTP header. So it wants requests for https://www.example.com/orders to go to a specific microservice and requests for https://www.example.com/products to go to another microservice.
- () Which of the following features of Application Load Balancers can be used for this use-case?
- () Query string parameter-based routing
- () Host-based Routing
- **() Path-based Routing** [CORRECT]
- () HTTP header-based routing
- () Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions.
- () If your application is composed of several individual services, an Application Load Balancer can route a request to a service based on the content of the request. Here are the different types -
- () Host-based Routing:
- () You can route a client request based on the Host field of the HTTP header allowing you to route to multiple domains from the same load balancer.
- () Path-based Routing:
- () You can route a client request based on the URL path of the HTTP header.
- () HTTP header-based routing:
- () You can route a client request based on the value of any standard or custom HTTP header.
- () HTTP method-based routing:
- () You can route a client request based on any standard or custom HTTP method.
- () Query string parameter-based routing:
- () You can route a client request based on the query string or query parameters.
- () Source IP address CIDR-based routing:
- () You can route a client request based on source IP address CIDR from where the request originates.
- () Path-based Routing Overview:
- () You can use path conditions to define rules that route requests based on the URL in the request (also known as path-based routing).
- () The path pattern is applied only to the path of the URL, not to its query parameters. 
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html#path-conditions

**Answer:**
Correct Answer: **Path-based Routing**

---

## Question 93

**Q:** Which of the following features of Application Load Balancers can be used for this use-case?

**Options:**
- (A) Query string parameter-based routing
- (B) Host-based Routing
- (C) Path-based Routing
- (D) HTTP header-based routing
- (E) Correct option:
- (F) Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions.
- (G) If your application is composed of several individual services, an Application Load Balancer can route a request to a service based on the content of the request. Here are the different types -
- (H) Host-based Routing:
- (I) You can route a client request based on the Host field of the HTTP header allowing you to route to multiple domains from the same load balancer.
- (J) Path-based Routing:
- () You can route a client request based on the URL path of the HTTP header.
- () HTTP header-based routing:
- () You can route a client request based on the value of any standard or custom HTTP header.
- () HTTP method-based routing:
- () You can route a client request based on any standard or custom HTTP method.
- () Query string parameter-based routing:
- () You can route a client request based on the query string or query parameters.
- () Source IP address CIDR-based routing:
- () You can route a client request based on source IP address CIDR from where the request originates.
- () Path-based Routing Overview:
- () You can use path conditions to define rules that route requests based on the URL in the request (also known as path-based routing).
- () The path pattern is applied only to the path of the URL, not to its query parameters. 
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html#path-conditions
- () Incorrect options:
- () As mentioned earlier in the explanation, none of these three types of routing support requests based on the URL path of the HTTP header. Hence these three are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html
- () A healthcare company is developing a secure internal web portal hosted on AWS. The application must communicate with legacy systems that reside in the company's on-premises data centers. These data centers are connected to AWS via a site-to-site VPN. The company uses Amazon Route 53 as its DNS solution and requires the application to resolve private DNS records for the on-premises services from within its Amazon VPC.
- () What is the MOST secure and appropriate way to meet these DNS resolution requirements?
- () Create a hybrid connectivity gateway and attach the on-premises DNS servers to Route 53 as authoritative zones for internal domains
- **() Create a Route 53 Resolver outbound endpoint. Define a forwarding rule that routes DNS queries for on-premises domains to the on-premises DNS server. Associate the rule with the VPC** [CORRECT]
- () Configure a Route 53 Resolver inbound endpoint and create a DNS forwarding rule. Enable recursive DNS resolution in the VPC to access on-premises services
- () Create a Route 53 private hosted zone for the on-premises domain. Associate the hosted zone with the VPC to allow the application to resolve DNS names of the on-premises services
- () via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- () References:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- () https://docs.aws.amazon.com/whitepapers/latest/hybrid-cloud-dns-options-for-vpc/route-53-resolver-endpoints-and-forwarding-rules.html

**Answer:**
Correct Answer: **Create a Route 53 Resolver outbound endpoint. Define a forwarding rule that routes DNS queries for on-premises domains to the on-premises DNS server. Associate the rule with the VPC**

---

## Question 94

**Q:** What is the MOST secure and appropriate way to meet these DNS resolution requirements?

**Options:**
- (A) Create a hybrid connectivity gateway and attach the on-premises DNS servers to Route 53 as authoritative zones for internal domains
- **(B) Create a Route 53 Resolver outbound endpoint. Define a forwarding rule that routes DNS queries for on-premises domains to the on-premises DNS server. Associate the rule with the VPC** [CORRECT]
- (C) Configure a Route 53 Resolver inbound endpoint and create a DNS forwarding rule. Enable recursive DNS resolution in the VPC to access on-premises services
- (D) Create a Route 53 private hosted zone for the on-premises domain. Associate the hosted zone with the VPC to allow the application to resolve DNS names of the on-premises services
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- (J) https://docs.aws.amazon.com/whitepapers/latest/hybrid-cloud-dns-options-for-vpc/route-53-resolver-endpoints-and-forwarding-rules.html

**Answer:**
Correct Answer: **Create a Route 53 Resolver outbound endpoint. Define a forwarding rule that routes DNS queries for on-premises domains to the on-premises DNS server. Associate the rule with the VPC**

---

## Question 95

**Q:** As a solutions architect, which of the following steps would you recommend to implement the solution?

**Options:**
- (A) Configure your Auto Scaling group by creating a target tracking policy and setting the instance count to 10 at the designated hour. This causes the scale-out to happen before peak traffic kicks in at the designated hour
- (B) Configure your Auto Scaling group by creating a simple tracking policy and setting the instance count to 10 at the designated hour. This causes the scale-out to happen before peak traffic kicks in at the designated hour
- (C) Configure your Auto Scaling group by creating a scheduled action that kicks-off at the designated hour on the last day of the month. Set the desired capacity of instances to 10. This causes the scale-out to happen before peak traffic kicks in at the designated hour
- (D) Configure your Auto Scaling group by creating a scheduled action that kicks-off at the designated hour on the last day of the month. Set the min count as well as the max count of instances to 10. This causes the scale-out to happen before peak traffic kicks in at the designated hour
- (E) Correct option:
- (F) Scheduled scaling allows you to set your own scaling schedule. For example, let's say that every week the traffic to your web application starts to increase on Wednesday, remains high on Thursday, and starts to decrease on Friday. You can plan your scaling actions based on the predictable traffic patterns of your web application. Scaling actions are performed automatically as a function of time and date.
- (G) A scheduled action sets the minimum, maximum, and desired sizes to what is specified by the scheduled action at the time specified by the scheduled action. For the given use case, the correct solution is to set the desired capacity to 10. When we want to specify a range of instances, then we must use min and max values.
- (H) Incorrect options:
- (I) Target tracking policy or simple tracking policy cannot be used to effect a scaling action at a certain designated hour. Both these options have been added as distractors.
- (J) Reference:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/schedule_time.html
- () A major bank is using Amazon Simple Queue Service (Amazon SQS) to migrate several core banking applications to the cloud to ensure high availability and cost efficiency while simplifying administrative complexity and overhead. The development team at the bank expects a peak rate of about 1000 messages per second to be processed via SQS. It is important that the messages are processed in order.
- () Which of the following options can be used to implement this system?
- () Use Amazon SQS FIFO (First-In-First-Out) queue in batch mode of 4 messages per operation to process the messages at the peak rate
- () Use Amazon SQS standard queue to process the messages
- () Use Amazon SQS FIFO (First-In-First-Out) queue to process the messages
- () Use Amazon SQS FIFO (First-In-First-Out) queue in batch mode of 2 messages per operation to process the messages at the peak rate
- () Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS offers two types of message queues - Standard queues vs FIFO queues.
- () For FIFO queues, the order in which messages are sent and received is strictly preserved (i.e. First-In-First-Out). On the other hand, the standard SQS queues offer best-effort ordering. This means that occasionally, messages might be delivered in an order different from which they were sent.
- () By default, FIFO queues support up to 300 messages per second (300 send, receive, or delete operations per second). When you batch 10 messages per operation (maximum), FIFO queues can support up to 3,000 messages per second. Therefore you need to process 4 messages per operation so that the FIFO queue can support up to 1200 messages per second, which is well within the peak rate.
- () FIFO Queues Overview:
- () via - https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html
- () Use Amazon SQS standard queue to process the messages - As messages need to be processed in order, therefore standard queues are ruled out.
- () Use Amazon SQS FIFO (First-In-First-Out) queue to process the messages - By default, FIFO queues support up to 300 messages per second and this is not sufficient to meet the message processing throughput per the given use-case. Hence this option is incorrect.
- () Use Amazon SQS FIFO (First-In-First-Out) queue in batch mode of 2 messages per operation to process the messages at the peak rate - As mentioned earlier in the explanation, you need to use FIFO queues in batch mode and process 4 messages per operation, so that the FIFO queue can support up to 1200 messages per second. With 2 messages per operation, you can only support up to 600 messages per second.
- () References:
- () https://aws.amazon.com/sqs/
- () https://aws.amazon.com/sqs/features/
- () The flagship application for a gaming company connects to an Amazon Aurora database and the entire technology stack is currently deployed in the United States. Now, the company has plans to expand to Europe and Asia for its operations. It needs the games table to be accessible globally but needs the users and games_played tables to be regional only.
- () How would you implement this with minimal application refactoring?
- () Use a Amazon DynamoDB global table for the games table and use Amazon DynamoDB tables for the users and games_played tables
- () Use a Amazon DynamoDB global table for the games table and use Amazon Aurora for the users and games_played tables
- **() Use an Amazon Aurora Global Database for the games table and use Amazon Aurora for the users and games_played tables** [CORRECT]
- () Use an Amazon Aurora Global Database for the games table and use Amazon DynamoDB tables for the users and games_played tables
- () Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 128TB per database instance. Aurora is not an in-memory database.
- () Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each region, and provides disaster recovery from region-wide outages. Amazon Aurora Global Database is the correct choice for the given use-case.

**Answer:**
Correct Answer: **Use an Amazon Aurora Global Database for the games table and use Amazon Aurora for the users and games_played tables**

---

## Question 96

**Q:** Which of the following options can be used to implement this system?

**Options:**
- (A) Use Amazon SQS FIFO (First-In-First-Out) queue in batch mode of 4 messages per operation to process the messages at the peak rate
- (B) Use Amazon SQS standard queue to process the messages
- (C) Use Amazon SQS FIFO (First-In-First-Out) queue to process the messages
- (D) Use Amazon SQS FIFO (First-In-First-Out) queue in batch mode of 2 messages per operation to process the messages at the peak rate
- (E) Correct option:
- (F) Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS offers two types of message queues - Standard queues vs FIFO queues.
- (G) For FIFO queues, the order in which messages are sent and received is strictly preserved (i.e. First-In-First-Out). On the other hand, the standard SQS queues offer best-effort ordering. This means that occasionally, messages might be delivered in an order different from which they were sent.
- (H) By default, FIFO queues support up to 300 messages per second (300 send, receive, or delete operations per second). When you batch 10 messages per operation (maximum), FIFO queues can support up to 3,000 messages per second. Therefore you need to process 4 messages per operation so that the FIFO queue can support up to 1200 messages per second, which is well within the peak rate.
- (I) FIFO Queues Overview:
- (J) via - https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html
- () Incorrect options:
- () Use Amazon SQS standard queue to process the messages - As messages need to be processed in order, therefore standard queues are ruled out.
- () Use Amazon SQS FIFO (First-In-First-Out) queue to process the messages - By default, FIFO queues support up to 300 messages per second and this is not sufficient to meet the message processing throughput per the given use-case. Hence this option is incorrect.
- () Use Amazon SQS FIFO (First-In-First-Out) queue in batch mode of 2 messages per operation to process the messages at the peak rate - As mentioned earlier in the explanation, you need to use FIFO queues in batch mode and process 4 messages per operation, so that the FIFO queue can support up to 1200 messages per second. With 2 messages per operation, you can only support up to 600 messages per second.
- () References:
- () https://aws.amazon.com/sqs/
- () https://aws.amazon.com/sqs/features/
- () The flagship application for a gaming company connects to an Amazon Aurora database and the entire technology stack is currently deployed in the United States. Now, the company has plans to expand to Europe and Asia for its operations. It needs the games table to be accessible globally but needs the users and games_played tables to be regional only.
- () How would you implement this with minimal application refactoring?
- () Use a Amazon DynamoDB global table for the games table and use Amazon DynamoDB tables for the users and games_played tables
- () Use a Amazon DynamoDB global table for the games table and use Amazon Aurora for the users and games_played tables
- () Use an Amazon Aurora Global Database for the games table and use Amazon Aurora for the users and games_played tables
- () Use an Amazon Aurora Global Database for the games table and use Amazon DynamoDB tables for the users and games_played tables
- () Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 128TB per database instance. Aurora is not an in-memory database.
- () Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each region, and provides disaster recovery from region-wide outages. Amazon Aurora Global Database is the correct choice for the given use-case.
- () For the given use-case, we, therefore, need to have two Aurora clusters, one for the global table (games table) and the other one for the local tables (users and games_played tables).
- () Here, we want minimal application refactoring. Amazon DynamoDB and Amazon Aurora have a completely different APIs, due to Amazon Aurora being SQL and Amazon DynamoDB being NoSQL. So all three options are incorrect, as they have Amazon DynamoDB as one of the components.
- () Reference:
- () https://aws.amazon.com/rds/aurora/faqs/
- () Which solution best meets these requirements?
- **() Use a daily AWS Glue job to transform and clean the data stored in Amazon S3. Load the transformed dataset into Amazon Redshift Serverless, which offers MPP capabilities in a serverless model. Enable analysts to use Amazon Redshift ML to build and train ML models** [CORRECT]
- () Provision and run a daily Amazon EMR cluster with Apache Spark to process and transform the S3 data. Load the results into Amazon Redshift (provisioned). Enable ML model development by integrating Redshift with Amazon SageMaker notebooks for advanced modeling tasks
- () Use an AWS Glue job to transform and load data into Amazon RDS for PostgreSQL. Allow analysts to run machine learning models using Amazon Aurora ML integrated with PostgreSQL, leveraging Amazon SageMaker endpoints behind the scenes
- () Run a daily AWS Glue job to process and transform the raw files in S3 and register the outputs as Amazon Athena tables in AWS Glue Data Catalog. Allow analysts to build ML models using Amazon Athena ML, with SQL-based predictions on top of S3 data without moving it to a warehouse

**Answer:**
Correct Answer: **Use a daily AWS Glue job to transform and clean the data stored in Amazon S3. Load the transformed dataset into Amazon Redshift Serverless, which offers MPP capabilities in a serverless model. Enable analysts to use Amazon Redshift ML to build and train ML models**

---

## Question 97

**Q:** How would you implement this with minimal application refactoring?

**Options:**
- (A) Use a Amazon DynamoDB global table for the games table and use Amazon DynamoDB tables for the users and games_played tables
- (B) Use a Amazon DynamoDB global table for the games table and use Amazon Aurora for the users and games_played tables
- (C) Use an Amazon Aurora Global Database for the games table and use Amazon Aurora for the users and games_played tables
- (D) Use an Amazon Aurora Global Database for the games table and use Amazon DynamoDB tables for the users and games_played tables
- (E) Correct option:
- (F) Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 128TB per database instance. Aurora is not an in-memory database.
- (G) Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each region, and provides disaster recovery from region-wide outages. Amazon Aurora Global Database is the correct choice for the given use-case.
- (H) For the given use-case, we, therefore, need to have two Aurora clusters, one for the global table (games table) and the other one for the local tables (users and games_played tables).
- (I) Incorrect options:
- (J) Here, we want minimal application refactoring. Amazon DynamoDB and Amazon Aurora have a completely different APIs, due to Amazon Aurora being SQL and Amazon DynamoDB being NoSQL. So all three options are incorrect, as they have Amazon DynamoDB as one of the components.
- () Reference:
- () https://aws.amazon.com/rds/aurora/faqs/
- () Which solution best meets these requirements?
- **() Use a daily AWS Glue job to transform and clean the data stored in Amazon S3. Load the transformed dataset into Amazon Redshift Serverless, which offers MPP capabilities in a serverless model. Enable analysts to use Amazon Redshift ML to build and train ML models** [CORRECT]
- () Provision and run a daily Amazon EMR cluster with Apache Spark to process and transform the S3 data. Load the results into Amazon Redshift (provisioned). Enable ML model development by integrating Redshift with Amazon SageMaker notebooks for advanced modeling tasks
- () Use an AWS Glue job to transform and load data into Amazon RDS for PostgreSQL. Allow analysts to run machine learning models using Amazon Aurora ML integrated with PostgreSQL, leveraging Amazon SageMaker endpoints behind the scenes
- () Run a daily AWS Glue job to process and transform the raw files in S3 and register the outputs as Amazon Athena tables in AWS Glue Data Catalog. Allow analysts to build ML models using Amazon Athena ML, with SQL-based predictions on top of S3 data without moving it to a warehouse
- () via - https://aws.amazon.com/blogs/big-data/create-train-and-deploy-machine-learning-models-in-amazon-redshift-using-sql-with-amazon-redshift-ml/
- () References:
- () https://aws.amazon.com/blogs/big-data/create-train-and-deploy-machine-learning-models-in-amazon-redshift-using-sql-with-amazon-redshift-ml/
- () https://docs.aws.amazon.com/redshift/latest/mgmt/serverless-whatis.html
- () https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html
- () https://github.com/awslabs/aws-athena-query-federation/wiki/AthenaML-Tutorial
- () An e-commerce company is looking for a solution with high availability, as it plans to migrate its flagship application to a fleet of Amazon Elastic Compute Cloud (Amazon EC2) instances. The solution should allow for content-based routing as part of the architecture.

**Answer:**
Correct Answer: **Use a daily AWS Glue job to transform and clean the data stored in Amazon S3. Load the transformed dataset into Amazon Redshift Serverless, which offers MPP capabilities in a serverless model. Enable analysts to use Amazon Redshift ML to build and train ML models**

---

## Question 98

**Q:** As a Solutions Architect, which of the following will you suggest for the company?

**Options:**
- (A) Use an Auto Scaling group for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure a Public IP address to mask any failure of an instance
- (B) Use a Network Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure a Private IP address to mask any failure of an instance
- **(C) Use an Application Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure Auto Scaling group to mask any failure of an instance** [CORRECT]
- (D) Use an Auto Scaling group for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure an elastic IP address (EIP) to mask any failure of an instance
- (E) Correct option:
- (F) The Application Load Balancer (ALB) is best suited for load balancing HTTP and HTTPS traffic and provides advanced request routing targeted at the delivery of modern application architectures, including microservices and containers. Operating at the individual request level (Layer 7), the Application Load Balancer routes traffic to targets within Amazon Virtual Private Cloud (Amazon VPC) based on the content of the request.
- (G) More info on Application Load Balancer:
- (H) via - https://aws.amazon.com/blogs/aws/new-aws-application-load-balancer/
- (I) Incorrect options:
- (J) Use a Network Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure a Private IP address to mask any failure of an instance - Network Load Balancer cannot facilitate content-based routing so this option is incorrect.
- () Both these options are incorrect as you cannot use the Auto Scaling group to distribute traffic to the Amazon EC2 instances.
- () An elastic IP address (EIP) is a static, public, IPv4 address allocated to your AWS account. With an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account. Elastic IPs do not change and remain allocated to your account until you delete them.
- () More info on Elastic Load Balancing (ELB):
- () via - https://docs.aws.amazon.com/whitepapers/latest/fault-tolerant-components/fault-tolerant-components.pdf
- () You can span your Auto Scaling group across multiple Availability Zones (AZs) within an AWS Region and then attaching a load balancer to distribute incoming traffic across those zones.
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-add-availability-zone.html
- () References:
- () https://aws.amazon.com/blogs/aws/new-aws-application-load-balancer/
- () https://docs.aws.amazon.com/whitepapers/latest/fault-tolerant-components/fault-tolerant-components.pdf
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-add-availability-zone.html
- () The DevOps team at an e-commerce company wants to perform some maintenance work on a specific Amazon EC2 instance that is part of an Auto Scaling group using a step scaling policy. The team is facing a maintenance challenge - every time the team deploys a maintenance patch, the instance health check status shows as out of service for a few minutes. This causes the Auto Scaling group to provision another replacement instance immediately.
- () As a solutions architect, which are the MOST time/resource efficient steps that you would recommend so that the maintenance work can be completed at the earliest? (Select two)
- () Correct selection
- () Put the instance into the Standby state and then update the instance by applying the maintenance patch. Once the instance is ready, you can exit the Standby state and then return the instance to service
- () Suspend the ScheduledActions process type for the Auto Scaling group and apply the maintenance patch to the instance. Once the instance is ready, you can you can manually set the instance's health status back to healthy and activate the ScheduledActions process type again
- () Delete the Auto Scaling group and apply the maintenance fix to the given instance. Create a new Auto Scaling group and add all the instances again using the manual scaling policy
- () Take a snapshot of the instance, create a new Amazon Machine Image (AMI) and then launch a new instance using this AMI. Apply the maintenance patch to this new instance and then add it back to the Auto Scaling Group by using the manual scaling policy. Terminate the earlier instance that had the maintenance issue
- () Suspend the ReplaceUnhealthy process type for the Auto Scaling group and apply the maintenance patch to the instance. Once the instance is ready, you can manually set the instance's health status back to healthy and activate the ReplaceUnhealthy process type again
- () Correct options:
- () How Standby State Works:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-enter-exit-standby.html
- () Delete the Auto Scaling group and apply the maintenance fix to the given instance. Create a new Auto Scaling group and add all the instances again using the manual scaling policy - It's not recommended to delete the Auto Scaling group just to apply a maintenance patch on a specific instance.
- () Suspend the ScheduledActions process type for the Auto Scaling group and apply the maintenance patch to the instance. Once the instance is ready, you can you can manually set the instance's health status back to healthy and activate the ScheduledActions process type again - Amazon EC2 Auto Scaling does not execute scaling actions that are scheduled to run during the suspension period. This option is not relevant to the given use-case.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-enter-exit-standby.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-suspend-resume-processes.html

**Answer:**
Correct Answer: **Use an Application Load Balancer for distributing traffic to the Amazon EC2 instances spread across different Availability Zones (AZs). Configure Auto Scaling group to mask any failure of an instance**

---

## Question 99

**Q:** As a solutions architect, which are the MOST time/resource efficient steps that you would recommend so that the maintenance work can be completed at the earliest? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Put the instance into the Standby state and then update the instance by applying the maintenance patch. Once the instance is ready, you can exit the Standby state and then return the instance to service
- (C) Suspend the ScheduledActions process type for the Auto Scaling group and apply the maintenance patch to the instance. Once the instance is ready, you can you can manually set the instance's health status back to healthy and activate the ScheduledActions process type again
- (D) Delete the Auto Scaling group and apply the maintenance fix to the given instance. Create a new Auto Scaling group and add all the instances again using the manual scaling policy
- (E) Take a snapshot of the instance, create a new Amazon Machine Image (AMI) and then launch a new instance using this AMI. Apply the maintenance patch to this new instance and then add it back to the Auto Scaling Group by using the manual scaling policy. Terminate the earlier instance that had the maintenance issue
- (F) Suspend the ReplaceUnhealthy process type for the Auto Scaling group and apply the maintenance patch to the instance. Once the instance is ready, you can manually set the instance's health status back to healthy and activate the ReplaceUnhealthy process type again
- (G) Correct options:
- (H) How Standby State Works:
- (I) via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-enter-exit-standby.html
- (J) Incorrect options:
- () Delete the Auto Scaling group and apply the maintenance fix to the given instance. Create a new Auto Scaling group and add all the instances again using the manual scaling policy - It's not recommended to delete the Auto Scaling group just to apply a maintenance patch on a specific instance.
- () Suspend the ScheduledActions process type for the Auto Scaling group and apply the maintenance patch to the instance. Once the instance is ready, you can you can manually set the instance's health status back to healthy and activate the ScheduledActions process type again - Amazon EC2 Auto Scaling does not execute scaling actions that are scheduled to run during the suspension period. This option is not relevant to the given use-case.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-enter-exit-standby.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-suspend-resume-processes.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/health-checks-overview.html
- () A software engineering intern at an e-commerce company is documenting the process flow to provision Amazon EC2 instances via the Amazon EC2 API. These instances are to be used for an internal application that processes Human Resources payroll data. He wants to highlight those volume types that cannot be used as a boot volume.
- () Can you help the intern by identifying those storage volume types that CANNOT be used as boot volumes while creating the instances? (Select two)
- () Instance Store
- () Cold Hard disk drive (sc1)
- () Provisioned IOPS Solid state drive (io1)
- () General Purpose Solid State Drive (gp2)
- () Throughput Optimized Hard disk drive (st1)
- () The Amazon EBS volume types fall into two categories:
- () Solid state drive (SSD) backed volumes optimized for transactional workloads involving frequent read/write operations with small I/O size, where the dominant performance attribute is IOPS.
- () Hard disk drive (HDD) backed volumes optimized for large streaming workloads where throughput (measured in MiB/s) is a better performance measure than IOPS.
- () Throughput Optimized HDD (st1) and Cold HDD (sc1) volume types CANNOT be used as a boot volume, so these two options are correct.
- () Please see this detailed overview of the volume types for Amazon EBS volumes.
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () General Purpose SSD (gp2), Provisioned IOPS SSD (io1), and Instance Store can be used as a boot volume.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/RootDeviceStorage.html

**Answer:**
Correct Answer: **Correct selection**

---

## Question 100

**Q:** Can you help the intern by identifying those storage volume types that CANNOT be used as boot volumes while creating the instances? (Select two)

**Options:**
- (A) Instance Store
- (B) Correct selection
- (C) Cold Hard disk drive (sc1)
- (D) Provisioned IOPS Solid state drive (io1)
- (E) General Purpose Solid State Drive (gp2)
- (F) Throughput Optimized Hard disk drive (st1)
- (G) Correct options:
- (H) The Amazon EBS volume types fall into two categories:
- (I) Solid state drive (SSD) backed volumes optimized for transactional workloads involving frequent read/write operations with small I/O size, where the dominant performance attribute is IOPS.
- (J) Hard disk drive (HDD) backed volumes optimized for large streaming workloads where throughput (measured in MiB/s) is a better performance measure than IOPS.
- () Throughput Optimized HDD (st1) and Cold HDD (sc1) volume types CANNOT be used as a boot volume, so these two options are correct.
- () Please see this detailed overview of the volume types for Amazon EBS volumes.
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () Incorrect options:
- () General Purpose SSD (gp2), Provisioned IOPS SSD (io1), and Instance Store can be used as a boot volume.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/RootDeviceStorage.html
- () What is the correct order of the storage charges incurred for the test file on these three storage types?
- **() Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EFS < Cost of test file storage on Amazon EBS** [CORRECT]
- () Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EBS < Cost of test file storage on Amazon EFS
- () Cost of test file storage on Amazon EBS < Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EFS
- () Cost of test file storage on Amazon EFS < Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EBS
- () Correct option:
- () With Amazon EFS, you pay only for the resources that you use. The Amazon EFS Standard Storage pricing is $0.30 per GB per month. Therefore the cost for storing the test file on EFS is $0.30 for the month.
- () For Amazon EBS General Purpose SSD (gp2) volumes, the charges are $0.10 per GB-month of provisioned storage. Therefore, for a provisioned storage of 100GB for this use-case, the monthly cost on EBS is $0.10*100 = $10. This cost is irrespective of how much storage is actually consumed by the test file.
- () For S3 Standard storage, the pricing is $0.023 per GB per month. Therefore, the monthly storage cost on S3 for the test file is $0.023.
- () Therefore this is the correct option.
- () Following the computations shown earlier in the explanation, these three options are incorrect.
- () https://aws.amazon.com/ebs/pricing/
- () https://aws.amazon.com/s3/pricing/(https://aws.amazon.com/s3/pricing/)
- () https://aws.amazon.com/efs/pricing/
- () Which solution meets these requirements MOST cost-effectively?

**Answer:**
Correct Answer: **Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EFS < Cost of test file storage on Amazon EBS**

---

## Question 101

**Q:** What is the correct order of the storage charges incurred for the test file on these three storage types?

**Options:**
- (A) Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EFS < Cost of test file storage on Amazon EBS
- (B) Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EBS < Cost of test file storage on Amazon EFS
- (C) Cost of test file storage on Amazon EBS < Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EFS
- (D) Cost of test file storage on Amazon EFS < Cost of test file storage on Amazon S3 Standard < Cost of test file storage on Amazon EBS
- (E) Correct option:
- (F) With Amazon EFS, you pay only for the resources that you use. The Amazon EFS Standard Storage pricing is $0.30 per GB per month. Therefore the cost for storing the test file on EFS is $0.30 for the month.
- (G) For Amazon EBS General Purpose SSD (gp2) volumes, the charges are $0.10 per GB-month of provisioned storage. Therefore, for a provisioned storage of 100GB for this use-case, the monthly cost on EBS is $0.10*100 = $10. This cost is irrespective of how much storage is actually consumed by the test file.
- (H) For S3 Standard storage, the pricing is $0.023 per GB per month. Therefore, the monthly storage cost on S3 for the test file is $0.023.
- (I) Therefore this is the correct option.
- (J) Incorrect options:
- () Following the computations shown earlier in the explanation, these three options are incorrect.
- () References:
- () https://aws.amazon.com/ebs/pricing/
- () https://aws.amazon.com/s3/pricing/(https://aws.amazon.com/s3/pricing/)
- () https://aws.amazon.com/efs/pricing/
- () Which solution meets these requirements MOST cost-effectively?
- () Use Amazon Lookout for Vision to scan the uploaded text files in the S3 bucket and extract entities. Invoke this workflow using an S3-triggered Lambda function. Parse the output and use Amazon API Gateway to push updates to the frontend in real time
- () Configure S3 Event Notifications to trigger an AWS Lambda function whenever a new product description is uploaded. Inside the function, use Amazon Comprehend's custom entity recognition feature to extract ingredient names. Store these names in the DynamoDB table and let the front-end application query for health scores
- () Create a workflow where Amazon Transcribe is used to convert synthetic audio versions (created from text of the product descriptions) back into text. Analyze the transcripts manually or using simple keyword matching within a Lambda function. Use Amazon SNS to notify the content moderation team for each processed file
- () Use Amazon SageMaker with a custom-trained NLP model to identify ingredients from the uploaded descriptions. Use Amazon EventBridge to invoke a Lambda function that forwards the document content to a SageMaker endpoint and stores the results in DynamoDB. Fine-tune the model using labeled ingredient datasets from open-source repositories and retrain it monthly
- () via - https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- () https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- () https://docs.aws.amazon.com/comprehend/latest/dg/custom-entity-recognition.html
- () https://aws.amazon.com/blogs/machine-learning/build-a-custom-entity-recognizer-using-amazon-comprehend/
- () https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html
- () https://docs.aws.amazon.com/transcribe/latest/dg/what-is.html
- () https://docs.aws.amazon.com/lookout-for-vision/latest/developer-guide/what-is.html
- () A data analytics company measures what the consumers watch and what advertising they’re exposed to. This real-time data is ingested into its on-premises data center and subsequently, the daily data feed is compressed into a single file and uploaded on Amazon S3 for backup. The typical compressed file size is around 2 gigabytes.
- () Which of the following is the fastest way to upload the daily compressed file into Amazon S3?
- () Upload the compressed file in a single operation
- () FTP the compressed file into an Amazon EC2 instance that runs in the same region as the Amazon S3 bucket. Then transfer the file from the Amazon EC2 instance into the Amazon S3 bucket
- **() Upload the compressed file using multipart upload with Amazon S3 Transfer Acceleration (Amazon S3TA)** [CORRECT]
- () Upload the compressed file using multipart upload

**Answer:**
Correct Answer: **Upload the compressed file using multipart upload with Amazon S3 Transfer Acceleration (Amazon S3TA)**

---

## Question 102

**Q:** Which solution meets these requirements MOST cost-effectively?

**Options:**
- (A) Use Amazon Lookout for Vision to scan the uploaded text files in the S3 bucket and extract entities. Invoke this workflow using an S3-triggered Lambda function. Parse the output and use Amazon API Gateway to push updates to the frontend in real time
- (B) Configure S3 Event Notifications to trigger an AWS Lambda function whenever a new product description is uploaded. Inside the function, use Amazon Comprehend's custom entity recognition feature to extract ingredient names. Store these names in the DynamoDB table and let the front-end application query for health scores
- (C) Create a workflow where Amazon Transcribe is used to convert synthetic audio versions (created from text of the product descriptions) back into text. Analyze the transcripts manually or using simple keyword matching within a Lambda function. Use Amazon SNS to notify the content moderation team for each processed file
- (D) Use Amazon SageMaker with a custom-trained NLP model to identify ingredients from the uploaded descriptions. Use Amazon EventBridge to invoke a Lambda function that forwards the document content to a SageMaker endpoint and stores the results in DynamoDB. Fine-tune the model using labeled ingredient datasets from open-source repositories and retrain it monthly
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- (J) https://docs.aws.amazon.com/comprehend/latest/dg/custom-entity-recognition.html
- () https://aws.amazon.com/blogs/machine-learning/build-a-custom-entity-recognizer-using-amazon-comprehend/
- () https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html
- () https://docs.aws.amazon.com/transcribe/latest/dg/what-is.html
- () https://docs.aws.amazon.com/lookout-for-vision/latest/developer-guide/what-is.html
- () A data analytics company measures what the consumers watch and what advertising they’re exposed to. This real-time data is ingested into its on-premises data center and subsequently, the daily data feed is compressed into a single file and uploaded on Amazon S3 for backup. The typical compressed file size is around 2 gigabytes.
- () Which of the following is the fastest way to upload the daily compressed file into Amazon S3?
- () Upload the compressed file in a single operation
- () FTP the compressed file into an Amazon EC2 instance that runs in the same region as the Amazon S3 bucket. Then transfer the file from the Amazon EC2 instance into the Amazon S3 bucket
- **() Upload the compressed file using multipart upload with Amazon S3 Transfer Acceleration (Amazon S3TA)** [CORRECT]
- () Upload the compressed file using multipart upload
- () Amazon S3 Transfer Acceleration (Amazon S3TA) enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.
- () Upload the compressed file in a single operation - In general, when your object size reaches 100 megabytes, you should consider using multipart uploads instead of uploading the object in a single operation. Multipart upload provides improved throughput - you can upload parts in parallel to improve throughput. Therefore, this option is not correct.
- () Upload the compressed file using multipart upload - Although using multipart upload would certainly speed up the process, combining with Amazon S3 Transfer Acceleration (Amazon S3TA) would further improve the transfer speed. Therefore just using multipart upload is not the correct option.
- () FTP the compressed file into an Amazon EC2 instance that runs in the same region as the Amazon S3 bucket. Then transfer the file from the Amazon EC2 instance into the Amazon S3 bucket - This is a roundabout process of getting the file into Amazon S3 and added as a distractor. Although it is technically feasible to follow this process, it would involve a lot of scripting and certainly would not be the fastest way to get the file into Amazon S3.
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html
- () A company uses Amazon S3 buckets for storing sensitive customer data. The company has defined different retention periods for different objects present in the Amazon S3 buckets, based on the compliance requirements. But, the retention rules do not seem to work as expected.
- () Which of the following options represent a valid configuration for setting up retention periods for objects in Amazon S3 buckets? (Select two)
- () You cannot place a retention period on an object version through a bucket default setting
- () When you use bucket default settings, you specify a Retain Until Date for the object version
- () Correct selection
- () When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version
- () Different versions of a single object can have different retention modes and periods
- () The bucket default settings will override any explicit retention mode or period you request on an object version
- () Correct options:

**Answer:**
Correct Answer: **Upload the compressed file using multipart upload with Amazon S3 Transfer Acceleration (Amazon S3TA)**

---

## Question 103

**Q:** Which of the following is the fastest way to upload the daily compressed file into Amazon S3?

**Options:**
- (A) Upload the compressed file in a single operation
- (B) FTP the compressed file into an Amazon EC2 instance that runs in the same region as the Amazon S3 bucket. Then transfer the file from the Amazon EC2 instance into the Amazon S3 bucket
- **(C) Upload the compressed file using multipart upload with Amazon S3 Transfer Acceleration (Amazon S3TA)** [CORRECT]
- (D) Upload the compressed file using multipart upload
- (E) Correct option:
- (F) Amazon S3 Transfer Acceleration (Amazon S3TA) enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.
- (G) Incorrect options:
- (H) Upload the compressed file in a single operation - In general, when your object size reaches 100 megabytes, you should consider using multipart uploads instead of uploading the object in a single operation. Multipart upload provides improved throughput - you can upload parts in parallel to improve throughput. Therefore, this option is not correct.
- (I) Upload the compressed file using multipart upload - Although using multipart upload would certainly speed up the process, combining with Amazon S3 Transfer Acceleration (Amazon S3TA) would further improve the transfer speed. Therefore just using multipart upload is not the correct option.
- (J) FTP the compressed file into an Amazon EC2 instance that runs in the same region as the Amazon S3 bucket. Then transfer the file from the Amazon EC2 instance into the Amazon S3 bucket - This is a roundabout process of getting the file into Amazon S3 and added as a distractor. Although it is technically feasible to follow this process, it would involve a lot of scripting and certainly would not be the fastest way to get the file into Amazon S3.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html
- () A company uses Amazon S3 buckets for storing sensitive customer data. The company has defined different retention periods for different objects present in the Amazon S3 buckets, based on the compliance requirements. But, the retention rules do not seem to work as expected.
- () Which of the following options represent a valid configuration for setting up retention periods for objects in Amazon S3 buckets? (Select two)
- () You cannot place a retention period on an object version through a bucket default setting
- () When you use bucket default settings, you specify a Retain Until Date for the object version
- () Correct selection
- () When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version
- () Different versions of a single object can have different retention modes and periods
- () The bucket default settings will override any explicit retention mode or period you request on an object version
- () Correct options:
- () You can place a retention period on an object version either explicitly or through a bucket default setting. When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version. Amazon S3 stores the Retain Until Date setting in the object version's metadata and protects the object version until the retention period expires.
- () For example, suppose that you have an object that is 15 days into a 30-day retention period, and you PUT an object into Amazon S3 with the same name and a 60-day retention period. In this case, your PUT succeeds, and Amazon S3 creates a new version of the object with a 60-day retention period. The older version maintains its original retention period and becomes deletable in 15 days.
- () You cannot place a retention period on an object version through a bucket default setting - You can place a retention period on an object version either explicitly or through a bucket default setting.
- () When you use bucket default settings, you specify a Retain Until Date for the object version - When you use bucket default settings, you don't specify a Retain Until Date. Instead, you specify a duration, in either days or years, for which every object version placed in the bucket should be protected.
- () The bucket default settings will override any explicit retention mode or period you request on an object version - If your request to place an object version in a bucket contains an explicit retention mode and period, those settings override any bucket default settings for that object version.
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock-overview.html
- () Which combination of actions will meet these goals in the most cost-effective and scalable manner? (Select two)
- () Implement Amazon RDS Proxy between the application and the Aurora PostgreSQL cluster. Deploy EC2 instances in an Auto Scaling group to retry transactions as needed
- () Use an Amazon ElastiCache cluster to cache database queries. Configure the application to store purchase transactions in the cache before writing to the database
- () Deploy an Amazon API Gateway with throttling and usage plans to slow down incoming purchase requests during peak times and maintain application stability
- () Modify the application to publish purchase events to an Amazon SQS queue. Launch an Auto Scaling group of EC2 workers that poll the queue and process purchases asynchronously
- () Deploy read replicas for the Aurora database in another Region and configure EC2 instances to read and write from the nearest replica based on latency

**Answer:**
Correct Answer: **Upload the compressed file using multipart upload with Amazon S3 Transfer Acceleration (Amazon S3TA)**

---

## Question 104

**Q:** Which of the following options represent a valid configuration for setting up retention periods for objects in Amazon S3 buckets? (Select two)

**Options:**
- **(A) You cannot place a retention period on an object version through a bucket default setting** [CORRECT]
- (B) When you use bucket default settings, you specify a Retain Until Date for the object version
- (C) Correct selection
- (D) When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version
- (E) Different versions of a single object can have different retention modes and periods
- (F) The bucket default settings will override any explicit retention mode or period you request on an object version
- (G) Correct options:
- (H) You can place a retention period on an object version either explicitly or through a bucket default setting. When you apply a retention period to an object version explicitly, you specify a Retain Until Date for the object version. Amazon S3 stores the Retain Until Date setting in the object version's metadata and protects the object version until the retention period expires.
- (I) For example, suppose that you have an object that is 15 days into a 30-day retention period, and you PUT an object into Amazon S3 with the same name and a 60-day retention period. In this case, your PUT succeeds, and Amazon S3 creates a new version of the object with a 60-day retention period. The older version maintains its original retention period and becomes deletable in 15 days.
- (J) Incorrect options:
- () You cannot place a retention period on an object version through a bucket default setting - You can place a retention period on an object version either explicitly or through a bucket default setting.
- () When you use bucket default settings, you specify a Retain Until Date for the object version - When you use bucket default settings, you don't specify a Retain Until Date. Instead, you specify a duration, in either days or years, for which every object version placed in the bucket should be protected.
- () The bucket default settings will override any explicit retention mode or period you request on an object version - If your request to place an object version in a bucket contains an explicit retention mode and period, those settings override any bucket default settings for that object version.
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock-overview.html
- () Which combination of actions will meet these goals in the most cost-effective and scalable manner? (Select two)
- () Implement Amazon RDS Proxy between the application and the Aurora PostgreSQL cluster. Deploy EC2 instances in an Auto Scaling group to retry transactions as needed
- () Use an Amazon ElastiCache cluster to cache database queries. Configure the application to store purchase transactions in the cache before writing to the database
- () Deploy an Amazon API Gateway with throttling and usage plans to slow down incoming purchase requests during peak times and maintain application stability
- () Modify the application to publish purchase events to an Amazon SQS queue. Launch an Auto Scaling group of EC2 workers that poll the queue and process purchases asynchronously
- () Deploy read replicas for the Aurora database in another Region and configure EC2 instances to read and write from the nearest replica based on latency
- () Introducing Amazon SQS decouples the web tier from the processing logic, allowing the system to buffer bursts in transaction load without overwhelming the database. EC2 workers in an Auto Scaling group can be dynamically scaled to consume and process queue messages based on throughput needs. This pattern ensures durability, resiliency, and elastic scalability, especially during peak usage. It's also cost-effective because compute usage grows and shrinks with actual demand.
- () Deploy read replicas for the Aurora database in another Region and configure EC2 instances to read and write from the nearest replica based on latency - This option acts as a distractor. While read replicas improve read scalability, they are read-only and cannot handle write traffic.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/WhatIs.html
- () A leading carmaker would like to build a new car-as-a-sensor service by leveraging fully serverless components that are provisioned and managed automatically by AWS. The development team at the carmaker does not want an option that requires the capacity to be manually provisioned, as it does not want to respond manually to changing volumes of sensor data.

**Answer:**
Correct Answer: **You cannot place a retention period on an object version through a bucket default setting**

---

## Question 105

**Q:** Which combination of actions will meet these goals in the most cost-effective and scalable manner? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Implement Amazon RDS Proxy between the application and the Aurora PostgreSQL cluster. Deploy EC2 instances in an Auto Scaling group to retry transactions as needed
- (C) Use an Amazon ElastiCache cluster to cache database queries. Configure the application to store purchase transactions in the cache before writing to the database
- (D) Deploy an Amazon API Gateway with throttling and usage plans to slow down incoming purchase requests during peak times and maintain application stability
- (E) Modify the application to publish purchase events to an Amazon SQS queue. Launch an Auto Scaling group of EC2 workers that poll the queue and process purchases asynchronously
- (F) Deploy read replicas for the Aurora database in another Region and configure EC2 instances to read and write from the nearest replica based on latency
- (G) Correct options:
- (H) Introducing Amazon SQS decouples the web tier from the processing logic, allowing the system to buffer bursts in transaction load without overwhelming the database. EC2 workers in an Auto Scaling group can be dynamically scaled to consume and process queue messages based on throughput needs. This pattern ensures durability, resiliency, and elastic scalability, especially during peak usage. It's also cost-effective because compute usage grows and shrinks with actual demand.
- (I) Incorrect Options:
- (J) Deploy read replicas for the Aurora database in another Region and configure EC2 instances to read and write from the nearest replica based on latency - This option acts as a distractor. While read replicas improve read scalability, they are read-only and cannot handle write traffic.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/WhatIs.html
- () A leading carmaker would like to build a new car-as-a-sensor service by leveraging fully serverless components that are provisioned and managed automatically by AWS. The development team at the carmaker does not want an option that requires the capacity to be manually provisioned, as it does not want to respond manually to changing volumes of sensor data.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 106

**Q:** Given these constraints, which of the following solutions is the BEST fit to develop this car-as-a-sensor service?

**Options:**
- (A) Ingest the sensor data in Amazon Kinesis Data Firehose, which directly writes the data into an auto-scaled Amazon DynamoDB table for downstream processing
- (B) Ingest the sensor data in Amazon Kinesis Data Streams, which is polled by an application running on an Amazon EC2 instance and the data is written into an auto-scaled Amazon DynamoDB table for downstream processing
- (C) Ingest the sensor data in an Amazon Simple Queue Service (Amazon SQS) standard queue, which is polled by an application running on an Amazon EC2 instance and the data is written into an auto-scaled Amazon DynamoDB table for downstream processing
- **(D) Ingest the sensor data in an Amazon Simple Queue Service (Amazon SQS) standard queue, which is polled by an AWS Lambda function in batches and the data is written into an auto-scaled Amazon DynamoDB table for downstream processing** [CORRECT]
- (E) Correct option:
- (F) AWS manages all ongoing operations and underlying infrastructure needed to provide a highly available and scalable message queuing service. With SQS, there is no upfront cost, no need to acquire, install, and configure messaging software, and no time-consuming build-out and maintenance of supporting infrastructure. SQS queues are dynamically created and scale automatically so you can build and grow applications quickly and efficiently.
- (G) As there is no need to manually provision the capacity, so this is the correct option.
- (H) Incorrect options:
- (I) Firehose cannot directly write into a DynamoDB table, so this option is incorrect.
- (J) Using an application on an Amazon EC2 instance is ruled out as the carmaker wants to use fully serverless components. So both these options are incorrect.
- () References:
- () https://aws.amazon.com/sqs/
- () https://docs.aws.amazon.com/lambda/latest/dg/with-kinesis.html
- () https://docs.aws.amazon.com/lambda/latest/dg/with-sqs.html
- () https://aws.amazon.com/kinesis/data-streams/faqs/
- () A new DevOps engineer has joined a large financial services company recently. As part of his onboarding, the IT department is conducting a review of the checklist for tasks related to AWS Identity and Access Management (AWS IAM).

**Answer:**
Correct Answer: **Ingest the sensor data in an Amazon Simple Queue Service (Amazon SQS) standard queue, which is polled by an AWS Lambda function in batches and the data is written into an auto-scaled Amazon DynamoDB table for downstream processing**

---

## Question 107

**Q:** As an AWS Certified Solutions Architect – Associate, which best practices would you recommend (Select two)?

**Options:**
- (A) Grant maximum privileges to avoid assigning privileges again
- (B) Use user credentials to provide access specific permissions for Amazon EC2 instances
- (C) Correct selection
- (D) Enable AWS Multi-Factor Authentication (AWS MFA) for privileged users
- (E) Create a minimum number of accounts and share these account credentials among employees
- (F) Configure AWS CloudTrail to log all AWS Identity and Access Management (AWS IAM) actions
- (G) Correct options:
- (H) As per the AWS best practices, it is better to enable Multi Factor Authentication (MFA) for privileged users via an MFA-enabled mobile device or hardware MFA token.
- (I) AWS recommends to turn on AWS CloudTrail to log all IAM actions for monitoring and audit purposes.
- (J) Incorrect options:
- () Create a minimum number of accounts and share these account credentials among employees - AWS recommends that user account credentials should not be shared between users. So, this option is incorrect.
- () Grant maximum privileges to avoid assigning privileges again - AWS recommends granting the least privileges required to complete a certain job and avoid giving excessive privileges which can be misused. So, this option is incorrect.
- () Use user credentials to provide access specific permissions for Amazon EC2 instances - It is highly recommended to use roles to grant access permissions for EC2 instances working on different AWS services. So, this option is incorrect.
- () References:
- () https://aws.amazon.com/iam/
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html
- () https://aws.amazon.com/cloudtrail/faqs/
- () A government agency is developing a online application to assist users in submitting permit requests through a web-based interface. The system architecture consists of a front-end web application tier and a background processing tier that handles the validation and submission of the forms. The application is expected to see high traffic and it must ensure that every submitted request is processed exactly once, with no loss of data.
- () Which design choice best satisfies these requirements?
- () Leverage Amazon EventBridge to send events from the web application to the processing tier for asynchronous form handling
- () Implement an Amazon SQS FIFO queue to reliably buffer and deliver form submissions from the web application layer to the processing tier
- () Leverage Amazon API Gateway to pass the form submissions to AWS Lambda for processing in real time
- () Implement an Amazon SQS standard queue to reliably buffer and deliver form submissions from the web application layer to the processing tier
- () Correct option:
- () SQS FIFO (First-In-First-Out) queues are designed for exactly-once message processing with order preservation. They prevent duplicate deliveries, making them ideal for transactional workflows such as registration or permit submissions. FIFO queues guarantee that each message is delivered and processed once and only once, which satisfies the application’s reliability and data integrity requirements.
- () Leverage Amazon API Gateway to pass the form submissions to AWS Lambda for processing in real time - While API Gateway with Lambda is effective for real-time synchronous processing, it does not inherently offer decoupling between tiers or a durable queue. It also lacks native support for guaranteed exactly-once processing across asynchronous workloads.
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-fifo-queues.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/standard-queues.html
- () Which solution best meets these requirements in the MOST cost-effective way?
- () Set up an Amazon S3 bucket in the research partner’s account and periodically copy EFS contents into the bucket using scheduled AWS DataSync jobs. Use Amazon S3 Access Points to expose the data to the Lambda function in the central account, allowing access via S3 API calls instead of file system mounts
- () Create a second Lambda function in the research partner's account that mounts the EFS file system locally. Have the main Lambda function in the central account invoke this secondary Lambda via Amazon API Gateway for data access and computation. Use IAM cross-account permissions to allow invocation
- **() Use Amazon EFS resource policies to allow cross-account access to the file system from the central account. Attach the EFS mount target to a shared VPC or peered VPC, and mount the file system in the Lambda function configuration using an EFS access point** [CORRECT]
- () Package the genomic input data as a Lambda layer and publish it in the research partner's account. Share the layer across accounts by modifying its resource policy and attach the layer to the Lambda function in the central account to access the data during execution

**Answer:**
Correct Answer: **Use Amazon EFS resource policies to allow cross-account access to the file system from the central account. Attach the EFS mount target to a shared VPC or peered VPC, and mount the file system in the Lambda function configuration using an EFS access point**

---

## Question 108

**Q:** Which design choice best satisfies these requirements?

**Options:**
- (A) Leverage Amazon EventBridge to send events from the web application to the processing tier for asynchronous form handling
- (B) Implement an Amazon SQS FIFO queue to reliably buffer and deliver form submissions from the web application layer to the processing tier
- (C) Leverage Amazon API Gateway to pass the form submissions to AWS Lambda for processing in real time
- (D) Implement an Amazon SQS standard queue to reliably buffer and deliver form submissions from the web application layer to the processing tier
- (E) Correct option:
- (F) SQS FIFO (First-In-First-Out) queues are designed for exactly-once message processing with order preservation. They prevent duplicate deliveries, making them ideal for transactional workflows such as registration or permit submissions. FIFO queues guarantee that each message is delivered and processed once and only once, which satisfies the application’s reliability and data integrity requirements.
- (G) Incorrect options:
- (H) Leverage Amazon API Gateway to pass the form submissions to AWS Lambda for processing in real time - While API Gateway with Lambda is effective for real-time synchronous processing, it does not inherently offer decoupling between tiers or a durable queue. It also lacks native support for guaranteed exactly-once processing across asynchronous workloads.
- (I) References:
- (J) https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-fifo-queues.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/standard-queues.html
- () Which solution best meets these requirements in the MOST cost-effective way?
- () Set up an Amazon S3 bucket in the research partner’s account and periodically copy EFS contents into the bucket using scheduled AWS DataSync jobs. Use Amazon S3 Access Points to expose the data to the Lambda function in the central account, allowing access via S3 API calls instead of file system mounts
- () Create a second Lambda function in the research partner's account that mounts the EFS file system locally. Have the main Lambda function in the central account invoke this secondary Lambda via Amazon API Gateway for data access and computation. Use IAM cross-account permissions to allow invocation
- () Use Amazon EFS resource policies to allow cross-account access to the file system from the central account. Attach the EFS mount target to a shared VPC or peered VPC, and mount the file system in the Lambda function configuration using an EFS access point
- () Package the genomic input data as a Lambda layer and publish it in the research partner's account. Share the layer across accounts by modifying its resource policy and attach the layer to the Lambda function in the central account to access the data during execution
- () https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html
- () https://docs.aws.amazon.com/efs/latest/ug/efs-access-points.html
- () https://docs.aws.amazon.com/datasync/latest/userguide/what-is-datasync.html
- () https://docs.aws.amazon.com/lambda/latest/dg/chapter-layers.html
- () https://docs.aws.amazon.com/lambda/latest/dg/adding-layers.html
- () While consolidating logs for the weekly reporting, a development team at an e-commerce company noticed that an unusually large number of illegal AWS application programming interface (API) queries were made sometime during the week. Due to the off-season, there was no visible impact on the systems. However, this event led the management team to seek an automated solution that can trigger near-real-time warnings in case such an event recurs.
- () Which of the following represents the best solution for the given scenario?
- () Configure AWS CloudTrail to stream event data to Amazon Kinesis. Use Amazon Kinesis stream-level metrics in the Amazon CloudWatch to trigger an AWS Lambda function that will trigger an error workflow
- () Run Amazon Athena SQL queries against AWS CloudTrail log files stored in Amazon S3 buckets. Use Amazon QuickSight to generate reports for managerial dashboards
- **() Create an Amazon CloudWatch metric filter that processes AWS CloudTrail logs having API call details and looks at any errors by factoring in all the error codes that need to be tracked. Create an alarm based on this metric's rate to send an Amazon SNS notification to the required team** [CORRECT]
- () AWS Trusted Advisor publishes metrics about check results to Amazon CloudWatch. Create an alarm to track status changes for checks in the Service Limits category for the APIs. The alarm will then notify when the service quota is reached or exceeded
- () AWS CloudTrail log data can be ingested into Amazon CloudWatch to monitor and identify your AWS account activity against security threats, and create a governance framework for security best practices. You can analyze log trail event data in CloudWatch using features such as Logs Insight, Contributor Insights, Metric filters, and CloudWatch Alarms.
- () AWS CloudTrail integrates with the Amazon CloudWatch service to publish the API calls being made to resources or services in the AWS account. The published event has invaluable information that can be used for compliance, auditing, and governance of your AWS accounts. Below we introduce several features available in CloudWatch to monitor API activity, analyze the logs at scale, and take action when malicious activity is discovered, without provisioning your infrastructure.
- () For the AWS Cloudtrail logs available in Amazon CloudWatch Logs, you can begin searching and filtering the log data by creating one or more metric filters. Use these metric filters to turn log data into numerical CloudWatch metrics that you can graph or set a CloudWatch Alarm on.
- () Note: AWS CloudTrail Insights helps AWS users identify and respond to unusual activity associated with write API calls by continuously analyzing CloudTrail management events.

**Answer:**
Correct Answer: **Create an Amazon CloudWatch metric filter that processes AWS CloudTrail logs having API call details and looks at any errors by factoring in all the error codes that need to be tracked. Create an alarm based on this metric's rate to send an Amazon SNS notification to the required team**

---

## Question 109

**Q:** Which solution best meets these requirements in the MOST cost-effective way?

**Options:**
- (A) Set up an Amazon S3 bucket in the research partner’s account and periodically copy EFS contents into the bucket using scheduled AWS DataSync jobs. Use Amazon S3 Access Points to expose the data to the Lambda function in the central account, allowing access via S3 API calls instead of file system mounts
- (B) Create a second Lambda function in the research partner's account that mounts the EFS file system locally. Have the main Lambda function in the central account invoke this secondary Lambda via Amazon API Gateway for data access and computation. Use IAM cross-account permissions to allow invocation
- (C) Use Amazon EFS resource policies to allow cross-account access to the file system from the central account. Attach the EFS mount target to a shared VPC or peered VPC, and mount the file system in the Lambda function configuration using an EFS access point
- (D) Package the genomic input data as a Lambda layer and publish it in the research partner's account. Share the layer across accounts by modifying its resource policy and attach the layer to the Lambda function in the central account to access the data during execution
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html
- (I) https://docs.aws.amazon.com/efs/latest/ug/efs-access-points.html
- (J) https://docs.aws.amazon.com/datasync/latest/userguide/what-is-datasync.html
- () https://docs.aws.amazon.com/lambda/latest/dg/chapter-layers.html
- () https://docs.aws.amazon.com/lambda/latest/dg/adding-layers.html
- () While consolidating logs for the weekly reporting, a development team at an e-commerce company noticed that an unusually large number of illegal AWS application programming interface (API) queries were made sometime during the week. Due to the off-season, there was no visible impact on the systems. However, this event led the management team to seek an automated solution that can trigger near-real-time warnings in case such an event recurs.
- () Which of the following represents the best solution for the given scenario?
- () Configure AWS CloudTrail to stream event data to Amazon Kinesis. Use Amazon Kinesis stream-level metrics in the Amazon CloudWatch to trigger an AWS Lambda function that will trigger an error workflow
- () Run Amazon Athena SQL queries against AWS CloudTrail log files stored in Amazon S3 buckets. Use Amazon QuickSight to generate reports for managerial dashboards
- **() Create an Amazon CloudWatch metric filter that processes AWS CloudTrail logs having API call details and looks at any errors by factoring in all the error codes that need to be tracked. Create an alarm based on this metric's rate to send an Amazon SNS notification to the required team** [CORRECT]
- () AWS Trusted Advisor publishes metrics about check results to Amazon CloudWatch. Create an alarm to track status changes for checks in the Service Limits category for the APIs. The alarm will then notify when the service quota is reached or exceeded
- () AWS CloudTrail log data can be ingested into Amazon CloudWatch to monitor and identify your AWS account activity against security threats, and create a governance framework for security best practices. You can analyze log trail event data in CloudWatch using features such as Logs Insight, Contributor Insights, Metric filters, and CloudWatch Alarms.
- () AWS CloudTrail integrates with the Amazon CloudWatch service to publish the API calls being made to resources or services in the AWS account. The published event has invaluable information that can be used for compliance, auditing, and governance of your AWS accounts. Below we introduce several features available in CloudWatch to monitor API activity, analyze the logs at scale, and take action when malicious activity is discovered, without provisioning your infrastructure.
- () For the AWS Cloudtrail logs available in Amazon CloudWatch Logs, you can begin searching and filtering the log data by creating one or more metric filters. Use these metric filters to turn log data into numerical CloudWatch metrics that you can graph or set a CloudWatch Alarm on.
- () Note: AWS CloudTrail Insights helps AWS users identify and respond to unusual activity associated with write API calls by continuously analyzing CloudTrail management events.
- () Configure AWS CloudTrail to stream event data to Amazon Kinesis. Use Amazon Kinesis stream-level metrics in the Amazon CloudWatch to trigger an AWS Lambda function that will trigger an error workflow - AWS CloudTrail cannot stream data to Amazon Kinesis. Amazon S3 buckets and Amazon CloudWatch logs are the only destinations possible.
- () Run Amazon Athena SQL queries against AWS CloudTrail log files stored in Amazon S3 buckets. Use Amazon QuickSight to generate reports for managerial dashboards - Generating reports and visualizations help in understanding and analyzing patterns but is not useful as a near-real-time automatic solution for the given problem.
- () https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudwatch-alarms-for-cloudtrail.html#cloudwatch-alarms-for-cloudtrail-authorization-failures
- () https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-concepts.html
- () https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-insights-events-with-cloudtrail.html
- () https://docs.aws.amazon.com/awssupport/latest/user/cloudwatch-metrics-ta.html
- () The sourcing team at the US headquarters of a global e-commerce company is preparing a spreadsheet of the new product catalog. The spreadsheet is saved on an Amazon Elastic File System (Amazon EFS) created in us-east-1 region. The sourcing team counterparts from other AWS regions such as Asia Pacific and Europe also want to collaborate on this spreadsheet.

**Answer:**
Correct Answer: **Create an Amazon CloudWatch metric filter that processes AWS CloudTrail logs having API call details and looks at any errors by factoring in all the error codes that need to be tracked. Create an alarm based on this metric's rate to send an Amazon SNS notification to the required team**

---

## Question 110

**Q:** Which of the following represents the best solution for the given scenario?

**Options:**
- (A) Configure AWS CloudTrail to stream event data to Amazon Kinesis. Use Amazon Kinesis stream-level metrics in the Amazon CloudWatch to trigger an AWS Lambda function that will trigger an error workflow
- (B) Run Amazon Athena SQL queries against AWS CloudTrail log files stored in Amazon S3 buckets. Use Amazon QuickSight to generate reports for managerial dashboards
- **(C) Create an Amazon CloudWatch metric filter that processes AWS CloudTrail logs having API call details and looks at any errors by factoring in all the error codes that need to be tracked. Create an alarm based on this metric's rate to send an Amazon SNS notification to the required team** [CORRECT]
- (D) AWS Trusted Advisor publishes metrics about check results to Amazon CloudWatch. Create an alarm to track status changes for checks in the Service Limits category for the APIs. The alarm will then notify when the service quota is reached or exceeded
- (E) Correct option:
- (F) AWS CloudTrail log data can be ingested into Amazon CloudWatch to monitor and identify your AWS account activity against security threats, and create a governance framework for security best practices. You can analyze log trail event data in CloudWatch using features such as Logs Insight, Contributor Insights, Metric filters, and CloudWatch Alarms.
- (G) AWS CloudTrail integrates with the Amazon CloudWatch service to publish the API calls being made to resources or services in the AWS account. The published event has invaluable information that can be used for compliance, auditing, and governance of your AWS accounts. Below we introduce several features available in CloudWatch to monitor API activity, analyze the logs at scale, and take action when malicious activity is discovered, without provisioning your infrastructure.
- (H) For the AWS Cloudtrail logs available in Amazon CloudWatch Logs, you can begin searching and filtering the log data by creating one or more metric filters. Use these metric filters to turn log data into numerical CloudWatch metrics that you can graph or set a CloudWatch Alarm on.
- (I) Note: AWS CloudTrail Insights helps AWS users identify and respond to unusual activity associated with write API calls by continuously analyzing CloudTrail management events.
- (J) Incorrect options:
- () Configure AWS CloudTrail to stream event data to Amazon Kinesis. Use Amazon Kinesis stream-level metrics in the Amazon CloudWatch to trigger an AWS Lambda function that will trigger an error workflow - AWS CloudTrail cannot stream data to Amazon Kinesis. Amazon S3 buckets and Amazon CloudWatch logs are the only destinations possible.
- () Run Amazon Athena SQL queries against AWS CloudTrail log files stored in Amazon S3 buckets. Use Amazon QuickSight to generate reports for managerial dashboards - Generating reports and visualizations help in understanding and analyzing patterns but is not useful as a near-real-time automatic solution for the given problem.
- () References:
- () https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudwatch-alarms-for-cloudtrail.html#cloudwatch-alarms-for-cloudtrail-authorization-failures
- () https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-concepts.html
- () https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-insights-events-with-cloudtrail.html
- () https://docs.aws.amazon.com/awssupport/latest/user/cloudwatch-metrics-ta.html
- () The sourcing team at the US headquarters of a global e-commerce company is preparing a spreadsheet of the new product catalog. The spreadsheet is saved on an Amazon Elastic File System (Amazon EFS) created in us-east-1 region. The sourcing team counterparts from other AWS regions such as Asia Pacific and Europe also want to collaborate on this spreadsheet.

**Answer:**
Correct Answer: **Create an Amazon CloudWatch metric filter that processes AWS CloudTrail logs having API call details and looks at any errors by factoring in all the error codes that need to be tracked. Create an alarm based on this metric's rate to send an Amazon SNS notification to the required team**

---

## Question 111

**Q:** As a solutions architect, what is your recommendation to enable this collaboration with the LEAST amount of operational overhead?

**Options:**
- (A) The spreadsheet data will have to be moved into an Amazon RDS for MySQL database which can then be accessed from any AWS region
- (B) The spreadsheet will have to be copied into Amazon EFS file systems of other AWS regions as Amazon EFS is a regional service and it does not allow access from other AWS regions
- (C) The spreadsheet will have to be copied in Amazon S3 which can then be accessed from any AWS region
- (D) The spreadsheet on the Amazon Elastic File System (Amazon EFS) can be accessed in other AWS regions by using an inter-region VPC peering connection
- (E) Correct option:
- (F) Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources.
- (G) Amazon EFS is a regional service storing data within and across multiple Availability Zones (AZs) for high availability and durability. Amazon EC2 instances can access your file system across AZs, regions, and VPCs, while on-premises servers can access using AWS Direct Connect or AWS VPN.
- (H) You can connect to Amazon EFS file systems from EC2 instances in other AWS regions using an inter-region VPC peering connection, and from on-premises servers using an AWS VPN connection. So this is the correct option.
- (I) Incorrect options:
- (J)  to support collabaration as per the use-case. So both these options are ruled out.
- ()  instead of a single file accessed and updated by all teams. Hence this option is incorrect.
- () Reference:
- () https://aws.amazon.com/efs/
- () The product team at a startup has figured out a market need to support both stateful and stateless client-server communications via the application programming interface (APIs) developed using its platform. You have been hired by the startup as a solutions architect to build a solution to fulfill this market need using Amazon API Gateway.
- () Which of the following would you identify as correct?
- () Amazon API Gateway creates RESTful APIs that enable stateless client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateless, full-duplex communication between client and server
- **() Amazon API Gateway creates RESTful APIs that enable stateless client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server** [CORRECT]
- () Amazon API Gateway creates RESTful APIs that enable stateful client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server
- () Amazon API Gateway creates RESTful APIs that enable stateful client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateless, full-duplex communication between client and server
- () Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. APIs act as the front door for applications to access data, business logic, or functionality from your backend services. Using API Gateway, you can create RESTful APIs and WebSocket APIs that enable real-time two-way communication applications.
- () How Amazon API Gateway Works:
- () via - https://aws.amazon.com/api-gateway/
- () Amazon API Gateway creates RESTful APIs that:
- () Are HTTP-based.
- () Enable stateless client-server communication.
- () Implement standard HTTP methods such as GET, POST, PUT, PATCH, and DELETE.
- () Amazon API Gateway creates WebSocket APIs that:
- () Adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server. Route incoming messages based on message content.
- () So Amazon API Gateway supports stateless RESTful APIs as well as stateful WebSocket APIs. Therefore this option is correct.
- () These three options contradict the earlier details provided in the explanation. To summarize, Amazon API Gateway supports stateless RESTful APIs and stateful WebSocket APIs. Hence these options are incorrect.
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html
- () An audit department generates and accesses the audit reports only twice in a financial year. The department uses AWS Step Functions to orchestrate the report creating process that has failover and retry scenarios built into the solution. The underlying data to create these audit reports is stored on Amazon S3, runs into hundreds of Terabytes and should be available with millisecond latency.

**Answer:**
Correct Answer: **Amazon API Gateway creates RESTful APIs that enable stateless client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server**

---

## Question 112

**Q:** Which of the following would you identify as correct?

**Options:**
- (A) Amazon API Gateway creates RESTful APIs that enable stateless client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateless, full-duplex communication between client and server
- **(B) Amazon API Gateway creates RESTful APIs that enable stateless client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server** [CORRECT]
- (C) Amazon API Gateway creates RESTful APIs that enable stateful client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server
- (D) Amazon API Gateway creates RESTful APIs that enable stateful client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateless, full-duplex communication between client and server
- (E) Correct option:
- (F) Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. APIs act as the front door for applications to access data, business logic, or functionality from your backend services. Using API Gateway, you can create RESTful APIs and WebSocket APIs that enable real-time two-way communication applications.
- (G) How Amazon API Gateway Works:
- (H) via - https://aws.amazon.com/api-gateway/
- (I) Amazon API Gateway creates RESTful APIs that:
- (J) Are HTTP-based.
- () Enable stateless client-server communication.
- () Implement standard HTTP methods such as GET, POST, PUT, PATCH, and DELETE.
- () Amazon API Gateway creates WebSocket APIs that:
- () Adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server. Route incoming messages based on message content.
- () So Amazon API Gateway supports stateless RESTful APIs as well as stateful WebSocket APIs. Therefore this option is correct.
- () Incorrect options:
- () These three options contradict the earlier details provided in the explanation. To summarize, Amazon API Gateway supports stateless RESTful APIs and stateful WebSocket APIs. Hence these options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html
- () An audit department generates and accesses the audit reports only twice in a financial year. The department uses AWS Step Functions to orchestrate the report creating process that has failover and retry scenarios built into the solution. The underlying data to create these audit reports is stored on Amazon S3, runs into hundreds of Terabytes and should be available with millisecond latency.

**Answer:**
Correct Answer: **Amazon API Gateway creates RESTful APIs that enable stateless client-server communication and Amazon API Gateway also creates WebSocket APIs that adhere to the WebSocket protocol, which enables stateful, full-duplex communication between client and server**

---

## Question 113

**Q:** As an AWS Certified Solutions Architect – Associate, which is the MOST cost-effective storage class that you would recommend to be used for this use-case?

**Options:**
- (A) Amazon S3 Standard
- (B) Amazon S3 Glacier Deep Archive
- (C) Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
- (D) Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)
- (E) Correct option:
- (F) Amazon S3 Storage Classes Overview:
- (G) via - https://aws.amazon.com/s3/storage-classes/
- (H) Incorrect options:
- (I) Amazon S3 Standard - Amazon S3 Standard offers high durability, availability, and performance object storage for frequently accessed data. As described above, Amazon S3 Standard-IA storage is a better fit than Amazon S3 Standard, hence using S3 standard is ruled out for the given use-case.
- (J) Amazon S3 Glacier Deep Archive - Amazon S3 Glacier Deep Archive is a secure, durable, and low-cost storage class for data archiving. Amazon S3 Glacier Deep Archive does not support millisecond latency, so this option is ruled out.
- () For more details on the durability, availability, cost and access latency - please review this reference link: https://aws.amazon.com/s3/storage-classes
- () Which AWS solution best meets these requirements?
- () Use AWS Glue DataBrew to visually build transformation workflows on top of the raw Parquet files in S3. Use DataBrew recipes to track, audit, and share the transformation steps with others. Enable data profiling to inspect column statistics, null values, and data types across datasets
- () Use Amazon AppFlow to move and transform Parquet files in S3. Configure AppFlow transformations and mappings within the visual interface. Share flows with collaborators through AWS IAM policies and scheduled executions
- () Create Amazon Athena SQL queries to perform transformation steps directly on S3. Store queries in AWS Glue Data Catalog and share saved queries with other users through Amazon Athena's query editor
- () Use AWS Glue Studio’s visual canvas to design data transformation workflows on top of the Parquet files in Amazon S3. Configure Glue Studio jobs to run these transformations without writing code. Share the job definitions with team members for reuse. Use the visual job editor to track transformation progress and inspect profiling statistics for each dataset column
- () AWS Glue DataBrew is a fully managed, serverless data preparation tool that enables users to visually clean, transform, and normalize raw datasets—all without writing any code. It is specifically designed for data analysts, business users, and data engineers who need to prepare data for analytics or machine learning workflows using an intuitive point-and-click interface.
- () What is AWS Glue DataBrew?:
- () via - https://docs.aws.amazon.com/databrew/latest/dg/what-is.html
- () In the scenario, the company ingests Apache Parquet files into Amazon S3 and needs to apply multiple transformation steps such as anomaly filtering, standardizing date formats, and computing aggregates. With DataBrew, users can perform these tasks through a drag-and-drop UI and configure complex workflows using reusable “recipes”—collections of ordered transformation steps that can be saved, versioned, and shared with others in the organization.
- () Furthermore, DataBrew provides built-in data profiling capabilities. It automatically generates column-level statistics such as distributions, cardinality, null value counts, standard deviations, and outlier detection. This visibility enables better data quality assessment before the data is used for reporting or machine learning.
- () DataBrew’s recipe model supports auditability and traceability, satisfying the requirement for data lineage. All transformation steps are recorded and can be exported or replicated across projects. The output of a DataBrew job is written back to Amazon S3, keeping the transformed data accessible for downstream tools like Amazon Athena, Redshift, or QuickSight.
- () Because it's serverless, there’s no infrastructure to manage, and it integrates seamlessly with other AWS services. This makes it ideal for teams that want a no-code, collaborative, auditable, and profile-rich data transformation tool for Parquet-based data lakes in S3.
- ()  with reusable, human-readable steps like DataBrew offers.
- () References:
- () https://docs.aws.amazon.com/databrew/latest/dg/what-is.html
- () https://aws.amazon.com/blogs/big-data/use-aws-glue-databrew-recipes-in-your-aws-glue-studio-visual-etl-jobs/
- () https://docs.aws.amazon.com/appflow/latest/userguide/what-is-appflow.html
- () https://docs.aws.amazon.com/athena/latest/ug/querying.html
- () https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/emr-serverless.html
- () A company runs a data processing workflow that takes about 60 minutes to complete. The workflow can withstand disruptions and it can be started and stopped multiple times.
- () Which is the most cost-effective solution to build a solution for the workflow?
- () Use Amazon EC2 on-demand instances to run the workflow processes
- () Use Amazon EC2 reserved instances to run the workflow processes
- **() Use Amazon EC2 spot instances to run the workflow processes** [CORRECT]

**Answer:**
Correct Answer: **Use Amazon EC2 spot instances to run the workflow processes**

---

## Question 114

**Q:** Which AWS solution best meets these requirements?

**Options:**
- (A) Use AWS Glue DataBrew to visually build transformation workflows on top of the raw Parquet files in S3. Use DataBrew recipes to track, audit, and share the transformation steps with others. Enable data profiling to inspect column statistics, null values, and data types across datasets
- (B) Use Amazon AppFlow to move and transform Parquet files in S3. Configure AppFlow transformations and mappings within the visual interface. Share flows with collaborators through AWS IAM policies and scheduled executions
- (C) Create Amazon Athena SQL queries to perform transformation steps directly on S3. Store queries in AWS Glue Data Catalog and share saved queries with other users through Amazon Athena's query editor
- (D) Use AWS Glue Studio’s visual canvas to design data transformation workflows on top of the Parquet files in Amazon S3. Configure Glue Studio jobs to run these transformations without writing code. Share the job definitions with team members for reuse. Use the visual job editor to track transformation progress and inspect profiling statistics for each dataset column
- (E) Correct option:
- (F) AWS Glue DataBrew is a fully managed, serverless data preparation tool that enables users to visually clean, transform, and normalize raw datasets—all without writing any code. It is specifically designed for data analysts, business users, and data engineers who need to prepare data for analytics or machine learning workflows using an intuitive point-and-click interface.
- (G) What is AWS Glue DataBrew?:
- (H) via - https://docs.aws.amazon.com/databrew/latest/dg/what-is.html
- (I) In the scenario, the company ingests Apache Parquet files into Amazon S3 and needs to apply multiple transformation steps such as anomaly filtering, standardizing date formats, and computing aggregates. With DataBrew, users can perform these tasks through a drag-and-drop UI and configure complex workflows using reusable “recipes”—collections of ordered transformation steps that can be saved, versioned, and shared with others in the organization.
- (J) Furthermore, DataBrew provides built-in data profiling capabilities. It automatically generates column-level statistics such as distributions, cardinality, null value counts, standard deviations, and outlier detection. This visibility enables better data quality assessment before the data is used for reporting or machine learning.
- () DataBrew’s recipe model supports auditability and traceability, satisfying the requirement for data lineage. All transformation steps are recorded and can be exported or replicated across projects. The output of a DataBrew job is written back to Amazon S3, keeping the transformed data accessible for downstream tools like Amazon Athena, Redshift, or QuickSight.
- () Because it's serverless, there’s no infrastructure to manage, and it integrates seamlessly with other AWS services. This makes it ideal for teams that want a no-code, collaborative, auditable, and profile-rich data transformation tool for Parquet-based data lakes in S3.
- () Incorrect options:
- ()  with reusable, human-readable steps like DataBrew offers.
- () References:
- () https://docs.aws.amazon.com/databrew/latest/dg/what-is.html
- () https://aws.amazon.com/blogs/big-data/use-aws-glue-databrew-recipes-in-your-aws-glue-studio-visual-etl-jobs/
- () https://docs.aws.amazon.com/appflow/latest/userguide/what-is-appflow.html
- () https://docs.aws.amazon.com/athena/latest/ug/querying.html
- () https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/emr-serverless.html
- () A company runs a data processing workflow that takes about 60 minutes to complete. The workflow can withstand disruptions and it can be started and stopped multiple times.
- () Which is the most cost-effective solution to build a solution for the workflow?
- () Use Amazon EC2 on-demand instances to run the workflow processes
- () Use Amazon EC2 reserved instances to run the workflow processes
- **() Use Amazon EC2 spot instances to run the workflow processes** [CORRECT]
- () Use AWS Lambda function to run the workflow processes
- () Amazon EC2 instance types:
- () via - https://aws.amazon.com/ec2/pricing/
- () Amazon EC2 Spot instances allow you to request spare Amazon EC2 computing capacity for up to 90% off the On-Demand price.
- () Spot instances are recommended for:
- () Applications that have flexible start and end times Applications that are feasible only at very low compute prices Users with urgent computing needs for large amounts of additional capacity
- () For the given use case, spot instances offer the most cost-effective solution as the workflow can withstand disruptions and can be started and stopped multiple times.
- () For example, considering a process that runs for an hour and needs about 1024 MB of memory, spot instance pricing for a t2.micro instance (having 1024 MB of RAM) is $0.0035 per hour.
- () Spot instance pricing:
- () via - https://aws.amazon.com/ec2/spot/pricing/
- () Contrast this with the pricing of a Lambda function (having 1024 MB of allocated memory), which comes out to $0.0000000167 per 1ms or $0.06 per hour ($0.0000000167 * 1000 * 60 * 60 per hour).
- () AWS Lambda function pricing:
- () via - https://aws.amazon.com/lambda/pricing/
- () Thus, a spot instance turns out to be about 20 times cost effective than a Lambda function to meet the requirements of the given use case.

**Answer:**
Correct Answer: **Use Amazon EC2 spot instances to run the workflow processes**

---

## Question 115

**Q:** What is AWS Glue DataBrew?:

**Options:**
- (A) via - https://docs.aws.amazon.com/databrew/latest/dg/what-is.html
- (B) In the scenario, the company ingests Apache Parquet files into Amazon S3 and needs to apply multiple transformation steps such as anomaly filtering, standardizing date formats, and computing aggregates. With DataBrew, users can perform these tasks through a drag-and-drop UI and configure complex workflows using reusable “recipes”—collections of ordered transformation steps that can be saved, versioned, and shared with others in the organization.
- (C) Furthermore, DataBrew provides built-in data profiling capabilities. It automatically generates column-level statistics such as distributions, cardinality, null value counts, standard deviations, and outlier detection. This visibility enables better data quality assessment before the data is used for reporting or machine learning.
- (D) DataBrew’s recipe model supports auditability and traceability, satisfying the requirement for data lineage. All transformation steps are recorded and can be exported or replicated across projects. The output of a DataBrew job is written back to Amazon S3, keeping the transformed data accessible for downstream tools like Amazon Athena, Redshift, or QuickSight.
- (E) Because it's serverless, there’s no infrastructure to manage, and it integrates seamlessly with other AWS services. This makes it ideal for teams that want a no-code, collaborative, auditable, and profile-rich data transformation tool for Parquet-based data lakes in S3.
- (F) Incorrect options:
- (G)  with reusable, human-readable steps like DataBrew offers.
- (H) References:
- (I) https://docs.aws.amazon.com/databrew/latest/dg/what-is.html
- (J) https://aws.amazon.com/blogs/big-data/use-aws-glue-databrew-recipes-in-your-aws-glue-studio-visual-etl-jobs/
- () https://docs.aws.amazon.com/appflow/latest/userguide/what-is-appflow.html
- () https://docs.aws.amazon.com/athena/latest/ug/querying.html
- () https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/emr-serverless.html
- () A company runs a data processing workflow that takes about 60 minutes to complete. The workflow can withstand disruptions and it can be started and stopped multiple times.
- () Which is the most cost-effective solution to build a solution for the workflow?
- () Use Amazon EC2 on-demand instances to run the workflow processes
- () Use Amazon EC2 reserved instances to run the workflow processes
- **() Use Amazon EC2 spot instances to run the workflow processes** [CORRECT]
- () Use AWS Lambda function to run the workflow processes
- () Correct option:
- () Amazon EC2 instance types:
- () via - https://aws.amazon.com/ec2/pricing/
- () Amazon EC2 Spot instances allow you to request spare Amazon EC2 computing capacity for up to 90% off the On-Demand price.
- () Spot instances are recommended for:
- () Applications that have flexible start and end times Applications that are feasible only at very low compute prices Users with urgent computing needs for large amounts of additional capacity
- () For the given use case, spot instances offer the most cost-effective solution as the workflow can withstand disruptions and can be started and stopped multiple times.
- () For example, considering a process that runs for an hour and needs about 1024 MB of memory, spot instance pricing for a t2.micro instance (having 1024 MB of RAM) is $0.0035 per hour.
- () Spot instance pricing:
- () via - https://aws.amazon.com/ec2/spot/pricing/
- () Contrast this with the pricing of a Lambda function (having 1024 MB of allocated memory), which comes out to $0.0000000167 per 1ms or $0.06 per hour ($0.0000000167 * 1000 * 60 * 60 per hour).
- () AWS Lambda function pricing:
- () via - https://aws.amazon.com/lambda/pricing/
- () Thus, a spot instance turns out to be about 20 times cost effective than a Lambda function to meet the requirements of the given use case.
- () You should note that both on-demand and reserved instances are more expensive than spot instances. In addition, reserved instances have a term of 1 year or 3 years, so they are not suited for the given workflow. Therefore, both these options are incorrect.
- () https://aws.amazon.com/ec2/pricing/
- () https://aws.amazon.com/ec2/spot/pricing/
- () https://aws.amazon.com/lambda/pricing/
- () https://aws.amazon.com/ec2/spot/instance-advisor/

**Answer:**
Correct Answer: **Use Amazon EC2 spot instances to run the workflow processes**

---

## Question 116

**Q:** Which is the most cost-effective solution to build a solution for the workflow?

**Options:**
- (A) Use Amazon EC2 on-demand instances to run the workflow processes
- (B) Use Amazon EC2 reserved instances to run the workflow processes
- (C) Use Amazon EC2 spot instances to run the workflow processes
- (D) Use AWS Lambda function to run the workflow processes
- (E) Correct option:
- (F) Amazon EC2 instance types:
- (G) via - https://aws.amazon.com/ec2/pricing/
- (H) Amazon EC2 Spot instances allow you to request spare Amazon EC2 computing capacity for up to 90% off the On-Demand price.
- (I) Spot instances are recommended for:
- (J) Applications that have flexible start and end times Applications that are feasible only at very low compute prices Users with urgent computing needs for large amounts of additional capacity
- () For the given use case, spot instances offer the most cost-effective solution as the workflow can withstand disruptions and can be started and stopped multiple times.
- () For example, considering a process that runs for an hour and needs about 1024 MB of memory, spot instance pricing for a t2.micro instance (having 1024 MB of RAM) is $0.0035 per hour.
- () Spot instance pricing:
- () via - https://aws.amazon.com/ec2/spot/pricing/
- () Contrast this with the pricing of a Lambda function (having 1024 MB of allocated memory), which comes out to $0.0000000167 per 1ms or $0.06 per hour ($0.0000000167 * 1000 * 60 * 60 per hour).
- () AWS Lambda function pricing:
- () via - https://aws.amazon.com/lambda/pricing/
- () Thus, a spot instance turns out to be about 20 times cost effective than a Lambda function to meet the requirements of the given use case.
- () Incorrect options:
- () You should note that both on-demand and reserved instances are more expensive than spot instances. In addition, reserved instances have a term of 1 year or 3 years, so they are not suited for the given workflow. Therefore, both these options are incorrect.
- () References:
- () https://aws.amazon.com/ec2/pricing/
- () https://aws.amazon.com/ec2/spot/pricing/
- () https://aws.amazon.com/lambda/pricing/
- () https://aws.amazon.com/ec2/spot/instance-advisor/
- () A retail company's dynamic website is hosted using on-premises servers in its data center in the United States. The company is launching its website in Asia, and it wants to optimize the website loading times for new users in Asia. The website's backend must remain in the United States. The website is being launched in a few days, and an immediate solution is needed.
- () What would you recommend?
- **() Use Amazon CloudFront with a custom origin pointing to the on-premises servers** [CORRECT]
- () Use Amazon CloudFront with a custom origin pointing to the DNS record of the website on Amazon Route 53
- () Migrate the website to Amazon S3. Use S3 cross-region replication (S3 CRR) between AWS Regions in the US and Asia
- () Leverage a Amazon Route 53 geo-proximity routing policy pointing to on-premises servers
- () Amazon CloudFront is a web service that gives businesses and web application developers an easy and cost-effective way to distribute content with low latency and high data transfer speeds. Amazon CloudFront uses standard cache control headers you set on your files to identify static and dynamic content. You can use different origins for different types of content on a single site – e.g. Amazon S3 for static objects, Amazon EC2 for dynamic content, and custom origins for third-party content.
- () Amazon CloudFront:
- () via - https://aws.amazon.com/cloudfront/
- () An origin server stores the original, definitive version of your objects. If you're serving content over HTTP, your origin server is either an Amazon S3 bucket or an HTTP server, such as a web server. Your HTTP server can run on an Amazon Elastic Compute Cloud (Amazon EC2) instance or on a server that you manage; these servers are also known as custom origins.
- () via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html

**Answer:**
Correct Answer: **Use Amazon CloudFront with a custom origin pointing to the on-premises servers**

---

## Question 117

**Q:** What would you recommend?

**Options:**
- (A) Use Amazon CloudFront with a custom origin pointing to the on-premises servers
- (B) Use Amazon CloudFront with a custom origin pointing to the DNS record of the website on Amazon Route 53
- (C) Migrate the website to Amazon S3. Use S3 cross-region replication (S3 CRR) between AWS Regions in the US and Asia
- (D) Leverage a Amazon Route 53 geo-proximity routing policy pointing to on-premises servers
- (E) Correct option:
- (F) Amazon CloudFront is a web service that gives businesses and web application developers an easy and cost-effective way to distribute content with low latency and high data transfer speeds. Amazon CloudFront uses standard cache control headers you set on your files to identify static and dynamic content. You can use different origins for different types of content on a single site – e.g. Amazon S3 for static objects, Amazon EC2 for dynamic content, and custom origins for third-party content.
- (G) Amazon CloudFront:
- (H) via - https://aws.amazon.com/cloudfront/
- (I) An origin server stores the original, definitive version of your objects. If you're serving content over HTTP, your origin server is either an Amazon S3 bucket or an HTTP server, such as a web server. Your HTTP server can run on an Amazon Elastic Compute Cloud (Amazon EC2) instance or on a server that you manage; these servers are also known as custom origins.
- (J) via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
- () Incorrect options:
- () Use Amazon CloudFront with a custom origin pointing to the DNS record of the website on Amazon Route 53 - This option has been added as a distractor. CloudFront cannot have a custom origin pointing to the DNS record of the website on Route 53.
- () Leverage a Amazon Route 53 geo-proximity routing policy pointing to on-premises servers - Since the on-premises servers continue to be in the US, so even using a Route 53 geo-proximity routing policy that directs the users in Asia to the on-premises servers in the US would not reduce the latency for the users in Asia. So this option is incorrect.
- () References:
- () https://aws.amazon.com/cloudfront/
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html
- () A company has moved its business critical data to Amazon Elastic File System (Amazon EFS) which will be accessed by multiple Amazon EC2 instances.
- () As an AWS Certified Solutions Architect - Associate, which of the following would you recommend to exercise access control such that only the permitted Amazon EC2 instances can read from the Amazon EFS file system? (Select two)
- () Correct selection
- () Use VPC security groups to control the network traffic to and from your file system
- () Use Amazon GuardDuty to curb unwanted access to Amazon EFS file system
- () Set up the IAM policy root credentials to control and configure the clients accessing the Amazon EFS file system
- () Use network access control list (network ACL) to control the network traffic to and from your Amazon EC2 instance
- () Use an IAM policy to control access for clients who can mount your file system with the required permissions
- () Correct options:
- () Use network access control list (network ACL) to control the network traffic to and from your Amazon EC2 instance - Network ACLs operate at the subnet level and not at the instance level.
- () Set up the IAM policy root credentials to control and configure the clients accessing the Amazon EFS file system - There is no such thing as an IAM policy root credentials and this statement has been added as a distractor.
- () Use Amazon GuardDuty to curb unwanted access to Amazon EFS file system - Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts, workloads, and data stored in Amazon S3. It cannot be used for access control to the Amazon EFS file system.
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Security.html#VPC_Security_Comparison
- () https://docs.aws.amazon.com/efs/latest/ug/accessing-fs-nfs-permissions.html
- () https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html
- () A leading social media analytics company is contemplating moving its dockerized application stack into AWS Cloud. The company is not sure about the pricing for using Amazon Elastic Container Service (Amazon ECS) with the EC2 launch type compared to the Amazon Elastic Container Service (Amazon ECS) with the Fargate launch type.
- () Which of the following is correct regarding the pricing for these two services?
- **() Amazon ECS with EC2 launch type is charged based on EC2 instances and EBS volumes used. Amazon ECS with Fargate launch type is charged based on vCPU and memory resources that the containerized application requests** [CORRECT]

**Answer:**
Correct Answer: **Amazon ECS with EC2 launch type is charged based on EC2 instances and EBS volumes used. Amazon ECS with Fargate launch type is charged based on vCPU and memory resources that the containerized application requests**

---

## Question 118

**Q:** As an AWS Certified Solutions Architect - Associate, which of the following would you recommend to exercise access control such that only the permitted Amazon EC2 instances can read from the Amazon EFS file system? (Select two)

**Options:**
- (A) Correct selection
- (B) Use VPC security groups to control the network traffic to and from your file system
- (C) Use Amazon GuardDuty to curb unwanted access to Amazon EFS file system
- (D) Set up the IAM policy root credentials to control and configure the clients accessing the Amazon EFS file system
- (E) Use network access control list (network ACL) to control the network traffic to and from your Amazon EC2 instance
- (F) Use an IAM policy to control access for clients who can mount your file system with the required permissions
- (G) Correct options:
- (H) Incorrect options:
- (I) Use network access control list (network ACL) to control the network traffic to and from your Amazon EC2 instance - Network ACLs operate at the subnet level and not at the instance level.
- (J) Set up the IAM policy root credentials to control and configure the clients accessing the Amazon EFS file system - There is no such thing as an IAM policy root credentials and this statement has been added as a distractor.
- () Use Amazon GuardDuty to curb unwanted access to Amazon EFS file system - Amazon GuardDuty is a threat detection service that continuously monitors for malicious activity and unauthorized behavior to protect your AWS accounts, workloads, and data stored in Amazon S3. It cannot be used for access control to the Amazon EFS file system.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Security.html#VPC_Security_Comparison
- () https://docs.aws.amazon.com/efs/latest/ug/accessing-fs-nfs-permissions.html
- () https://docs.aws.amazon.com/efs/latest/ug/iam-access-control-nfs-efs.html
- () A leading social media analytics company is contemplating moving its dockerized application stack into AWS Cloud. The company is not sure about the pricing for using Amazon Elastic Container Service (Amazon ECS) with the EC2 launch type compared to the Amazon Elastic Container Service (Amazon ECS) with the Fargate launch type.
- () Which of the following is correct regarding the pricing for these two services?
- **() Amazon ECS with EC2 launch type is charged based on EC2 instances and EBS volumes used. Amazon ECS with Fargate launch type is charged based on vCPU and memory resources that the containerized application requests** [CORRECT]
- () Both Amazon ECS with EC2 launch type and Amazon ECS with Fargate launch type are just charged based on Elastic Container Service used per hour
- () Both Amazon ECS with EC2 launch type and Amazon ECS with Fargate launch type are charged based on vCPU and memory resources that the containerized application requests
- () Both Amazon ECS with EC2 launch type and Amazon ECS with Fargate launch type are charged based on Amazon EC2 instances and Amazon EBS Elastic Volumes used
- () Correct option:
- () Amazon Elastic Container Service (Amazon ECS) is a fully managed container orchestration service. ECS allows you to easily run, scale, and secure Docker container applications on AWS.
- () Amazon ECS Overview:
- () via - https://aws.amazon.com/ecs/
- () With the Fargate launch type, you pay for the amount of vCPU and memory resources that your containerized application requests. vCPU and memory resources are calculated from the time your container images are pulled until the Amazon ECS Task terminates, rounded up to the nearest second. With the EC2 launch type, there is no additional charge for the EC2 launch type. You pay for AWS resources (e.g. EC2 instances or EBS volumes) you create to store and run your application.
- () As mentioned above - with the Fargate launch type, you pay for the amount of vCPU and memory resources. With EC2 launch type, you pay for AWS resources (e.g. EC2 instances or EBS volumes). Hence both these options are incorrect.
- () This is a made-up option and has been added as a distractor.
- () https://aws.amazon.com/ecs/pricing/

**Answer:**
Correct Answer: **Amazon ECS with EC2 launch type is charged based on EC2 instances and EBS volumes used. Amazon ECS with Fargate launch type is charged based on vCPU and memory resources that the containerized application requests**

---

## Question 119

**Q:** Which of the following is correct regarding the pricing for these two services?

**Options:**
- **(A) Amazon ECS with EC2 launch type is charged based on EC2 instances and EBS volumes used. Amazon ECS with Fargate launch type is charged based on vCPU and memory resources that the containerized application requests** [CORRECT]
- (B) Both Amazon ECS with EC2 launch type and Amazon ECS with Fargate launch type are just charged based on Elastic Container Service used per hour
- (C) Both Amazon ECS with EC2 launch type and Amazon ECS with Fargate launch type are charged based on vCPU and memory resources that the containerized application requests
- (D) Both Amazon ECS with EC2 launch type and Amazon ECS with Fargate launch type are charged based on Amazon EC2 instances and Amazon EBS Elastic Volumes used
- (E) Correct option:
- (F) Amazon Elastic Container Service (Amazon ECS) is a fully managed container orchestration service. ECS allows you to easily run, scale, and secure Docker container applications on AWS.
- (G) Amazon ECS Overview:
- (H) via - https://aws.amazon.com/ecs/
- (I) With the Fargate launch type, you pay for the amount of vCPU and memory resources that your containerized application requests. vCPU and memory resources are calculated from the time your container images are pulled until the Amazon ECS Task terminates, rounded up to the nearest second. With the EC2 launch type, there is no additional charge for the EC2 launch type. You pay for AWS resources (e.g. EC2 instances or EBS volumes) you create to store and run your application.
- (J) Incorrect options:
- () As mentioned above - with the Fargate launch type, you pay for the amount of vCPU and memory resources. With EC2 launch type, you pay for AWS resources (e.g. EC2 instances or EBS volumes). Hence both these options are incorrect.
- () This is a made-up option and has been added as a distractor.
- () References:
- () https://aws.amazon.com/ecs/pricing/
- () Dump11
- () A retail company wants to rollout and test a blue-green deployment for its global application in the next 48 hours. Most of the customers use mobile phones which are prone to Domain Name System (DNS) caching. The company has only two days left for the annual Thanksgiving sale to commence.

**Answer:**
Correct Answer: **Amazon ECS with EC2 launch type is charged based on EC2 instances and EBS volumes used. Amazon ECS with Fargate launch type is charged based on vCPU and memory resources that the containerized application requests**

---

## Question 120

**Q:** As a Solutions Architect, which of the following options would you recommend to test the deployment on as many users as possible in the given time frame?

**Options:**
- (A) Use Elastic Load Balancing (ELB) to distribute traffic across deployments
- (B) Use AWS Global Accelerator to distribute a portion of traffic to a particular deployment
- (C) Use AWS CodeDeploy deployment options to choose the right deployment
- (D) Use Amazon Route 53 weighted routing to spread traffic across different deployments
- (E) Correct option:
- (F)  the new version. This type of deployment allows you to test features in the green environment without impacting the currently running version of your application. When you’re satisfied that the green version is working properly, you can gradually reroute the traffic from the old blue environment to the new green environment. Blue/green deployments can mitigate common risks associated with deploying software, such as downtime and rollback capability.
- (G) AWS Global Accelerator is a network layer service that directs traffic to optimal endpoints over the AWS global network, this improves the availability and performance of your internet applications. It provides two static anycast IP addresses that act as a fixed entry point to your application endpoints in a single or multiple AWS Regions, such as your Application Load Balancers, Network Load Balancers, Elastic IP addresses or Amazon EC2 instances, in a single or in multiple AWS regions.
- (H) AWS Global Accelerator uses endpoint weights to determine the proportion of traffic that is directed to endpoints in an endpoint group, and traffic dials to control the percentage of traffic that is directed to an endpoint group (an AWS region where your application is deployed).
- (I) With AWS Global Accelerator, you can shift traffic gradually or all at once between the blue and the green environment and vice-versa without being subject to DNS caching on client devices and internet resolvers, traffic dials and endpoint weights changes are effective within seconds.
- (J) Incorrect options:
- () References:
- () https://aws.amazon.com/blogs/networking-and-content-delivery/using-aws-global-accelerator-to-achieve-blue-green-deployments
- () https://docs.aws.amazon.com/codedeploy/latest/userguide/deployments.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-weighted
- () An IT company has built a solution wherein an Amazon Redshift cluster writes data to an Amazon S3 bucket belonging to a different AWS account. However, it is found that the files created in the Amazon S3 bucket using the UNLOAD command from the Amazon Redshift cluster are not even accessible to the Amazon S3 bucket owner.
- () What could be the reason for this denial of permission for the bucket owner?
- () The owner of an Amazon S3 bucket has implicit access to all objects in his bucket. Permissions are set on objects after they are completely copied to the target location. Since the owner is unable to access the uploaded files, the write operation may be still in progress
- () When objects are uploaded to Amazon S3 bucket from a different AWS account, the S3 bucket owner will get implicit permissions to access these objects. This issue seems to be due to an upload error that can be fixed by providing manual access from AWS console
- () When two different AWS accounts are accessing an Amazon S3 bucket, both the accounts must share the bucket policies. An erroneous policy can lead to such permission failures
- () By default, an Amazon S3 object is owned by the AWS account that uploaded it. So the Amazon S3 bucket owner will not implicitly have access to the objects written by the Amazon Redshift cluster
- () To get access to the data files, an AWS Identity and Access Management (IAM) role with cross-account permissions must run the UNLOAD command again. Follow these steps to set up the Amazon Redshift cluster with cross-account permissions to the bucket:
- () 1. From the account of the Amazon S3 bucket, create an IAM role (Bucket Role) with permissions to the bucket.
- () 2. From the account of the Amazon Redshift cluster, create another IAM role (Cluster Role) with permissions to assume the Bucket Role.
- () 3. Update the Bucket Role to grant bucket access and create a trust relationship with the Cluster Role.
- () 4. From the Amazon Redshift cluster, run the UNLOAD command using the Cluster Role and Bucket Role.
- () This solution doesn't apply to Amazon Redshift clusters or Amazon S3 buckets that use server-side encryption with AWS Key Management Service (AWS KMS).
- () When objects are uploaded to Amazon S3 bucket from a different AWS account, the S3 bucket owner will get implicit permissions to access these objects. This issue seems to be due to an upload error that can be fixed by providing manual access from AWS console - By default, an Amazon S3 object is owned by the AWS account that uploaded it. So, the bucket owner will not have any default permissions on the objects. Therefore, this option is incorrect.
- () The owner of an Amazon S3 bucket has implicit access to all objects in his bucket. Permissions are set on objects after they are completely copied to the target location. Since the owner is unable to access the uploaded files, the write operation may be still in progress - This is an incorrect statement, given only as a distractor.
- () When two different AWS accounts are accessing an Amazon S3 bucket, both the accounts must share the bucket policies. An erroneous policy can lead to such permission failures - This is an incorrect statement, given only as a distractor.
- () Reference:
- () https://aws.amazon.com/premiumsupport/knowledge-center/s3-access-denied-redshift-unload/
- () A SaaS company is modernizing one of its legacy web applications by migrating it to AWS. The company aims to improve the availability of the application during both normal and peak traffic periods. Additionally, the company wants to implement protection against common web exploits and malicious traffic. The architecture must be scalable and integrate AWS WAF to secure incoming traffic.
- () Which solution will best meet these requirements with high availability and minimal configuration complexity?
- () Launch EC2 instances in a single Availability Zone and configure AWS Global Accelerator to route traffic to the instances. Attach AWS WAF to Global Accelerator for application protection
- () Launch two EC2 instances in separate Availability Zones and register them as targets of an Application Load Balancer. Associate the ALB with AWS WAF to filter incoming traffic
- () Create an Auto Scaling group with EC2 instances in multiple Availability Zones. Attach a Network Load Balancer (NLB) to distribute incoming traffic. Integrate AWS WAF directly with the Auto Scaling group for traffic filtering
- **() Deploy the application on multiple Amazon EC2 instances in an Auto Scaling group that spans two Availability Zones. Place an Application Load Balancer (ALB) in front of the group. Associate AWS WAF with the ALB** [CORRECT]

**Answer:**
Correct Answer: **Deploy the application on multiple Amazon EC2 instances in an Auto Scaling group that spans two Availability Zones. Place an Application Load Balancer (ALB) in front of the group. Associate AWS WAF with the ALB**

---

## Question 121

**Q:** What could be the reason for this denial of permission for the bucket owner?

**Options:**
- (A) The owner of an Amazon S3 bucket has implicit access to all objects in his bucket. Permissions are set on objects after they are completely copied to the target location. Since the owner is unable to access the uploaded files, the write operation may be still in progress
- (B) When objects are uploaded to Amazon S3 bucket from a different AWS account, the S3 bucket owner will get implicit permissions to access these objects. This issue seems to be due to an upload error that can be fixed by providing manual access from AWS console
- (C) When two different AWS accounts are accessing an Amazon S3 bucket, both the accounts must share the bucket policies. An erroneous policy can lead to such permission failures
- (D) By default, an Amazon S3 object is owned by the AWS account that uploaded it. So the Amazon S3 bucket owner will not implicitly have access to the objects written by the Amazon Redshift cluster
- (E) Correct option:
- (F) To get access to the data files, an AWS Identity and Access Management (IAM) role with cross-account permissions must run the UNLOAD command again. Follow these steps to set up the Amazon Redshift cluster with cross-account permissions to the bucket:
- (G) 1. From the account of the Amazon S3 bucket, create an IAM role (Bucket Role) with permissions to the bucket.
- (H) 2. From the account of the Amazon Redshift cluster, create another IAM role (Cluster Role) with permissions to assume the Bucket Role.
- (I) 3. Update the Bucket Role to grant bucket access and create a trust relationship with the Cluster Role.
- (J) 4. From the Amazon Redshift cluster, run the UNLOAD command using the Cluster Role and Bucket Role.
- () This solution doesn't apply to Amazon Redshift clusters or Amazon S3 buckets that use server-side encryption with AWS Key Management Service (AWS KMS).
- () Incorrect options:
- () When objects are uploaded to Amazon S3 bucket from a different AWS account, the S3 bucket owner will get implicit permissions to access these objects. This issue seems to be due to an upload error that can be fixed by providing manual access from AWS console - By default, an Amazon S3 object is owned by the AWS account that uploaded it. So, the bucket owner will not have any default permissions on the objects. Therefore, this option is incorrect.
- () The owner of an Amazon S3 bucket has implicit access to all objects in his bucket. Permissions are set on objects after they are completely copied to the target location. Since the owner is unable to access the uploaded files, the write operation may be still in progress - This is an incorrect statement, given only as a distractor.
- () When two different AWS accounts are accessing an Amazon S3 bucket, both the accounts must share the bucket policies. An erroneous policy can lead to such permission failures - This is an incorrect statement, given only as a distractor.
- () Reference:
- () https://aws.amazon.com/premiumsupport/knowledge-center/s3-access-denied-redshift-unload/
- () A SaaS company is modernizing one of its legacy web applications by migrating it to AWS. The company aims to improve the availability of the application during both normal and peak traffic periods. Additionally, the company wants to implement protection against common web exploits and malicious traffic. The architecture must be scalable and integrate AWS WAF to secure incoming traffic.
- () Which solution will best meet these requirements with high availability and minimal configuration complexity?
- () Launch EC2 instances in a single Availability Zone and configure AWS Global Accelerator to route traffic to the instances. Attach AWS WAF to Global Accelerator for application protection
- () Launch two EC2 instances in separate Availability Zones and register them as targets of an Application Load Balancer. Associate the ALB with AWS WAF to filter incoming traffic
- () Create an Auto Scaling group with EC2 instances in multiple Availability Zones. Attach a Network Load Balancer (NLB) to distribute incoming traffic. Integrate AWS WAF directly with the Auto Scaling group for traffic filtering
- () Deploy the application on multiple Amazon EC2 instances in an Auto Scaling group that spans two Availability Zones. Place an Application Load Balancer (ALB) in front of the group. Associate AWS WAF with the ALB
- () References:
- () https://docs.aws.amazon.com/waf/latest/developerguide/how-aws-waf-works.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- () Which solution will best meet these requirements with minimal refactoring and operational overhead?
- () Package the scripts into a container image. Deploy the image to AWS Batch with a managed compute environment on Amazon EC2. Define scheduling policies in AWS Batch to trigger jobs according to cron expressions
- **() Package the scripts into a container image. Use Amazon EventBridge Scheduler to define cron-based recurring schedules. Configure EventBridge Scheduler to invoke AWS Fargate tasks using Amazon ECS** [CORRECT]
- () Convert each script into a Lambda function and package it in a zip archive. Use Amazon EventBridge Scheduler to run the functions on a fixed schedule. Use Amazon S3 to store function outputs and logs
- () Create a container image for each script. Use AWS Step Functions to define a workflow for all scheduled tasks. Use a Wait state to delay execution and run tasks using Step Functions’ RunTask integration with ECS Fargate

**Answer:**
Correct Answer: **Package the scripts into a container image. Use Amazon EventBridge Scheduler to define cron-based recurring schedules. Configure EventBridge Scheduler to invoke AWS Fargate tasks using Amazon ECS**

---

## Question 122

**Q:** Which solution will best meet these requirements with high availability and minimal configuration complexity?

**Options:**
- (A) Launch EC2 instances in a single Availability Zone and configure AWS Global Accelerator to route traffic to the instances. Attach AWS WAF to Global Accelerator for application protection
- (B) Launch two EC2 instances in separate Availability Zones and register them as targets of an Application Load Balancer. Associate the ALB with AWS WAF to filter incoming traffic
- (C) Create an Auto Scaling group with EC2 instances in multiple Availability Zones. Attach a Network Load Balancer (NLB) to distribute incoming traffic. Integrate AWS WAF directly with the Auto Scaling group for traffic filtering
- (D) Deploy the application on multiple Amazon EC2 instances in an Auto Scaling group that spans two Availability Zones. Place an Application Load Balancer (ALB) in front of the group. Associate AWS WAF with the ALB
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/waf/latest/developerguide/how-aws-waf-works.html
- (I) https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- (J) https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- () Which solution will best meet these requirements with minimal refactoring and operational overhead?
- () Package the scripts into a container image. Deploy the image to AWS Batch with a managed compute environment on Amazon EC2. Define scheduling policies in AWS Batch to trigger jobs according to cron expressions
- **() Package the scripts into a container image. Use Amazon EventBridge Scheduler to define cron-based recurring schedules. Configure EventBridge Scheduler to invoke AWS Fargate tasks using Amazon ECS** [CORRECT]
- () Convert each script into a Lambda function and package it in a zip archive. Use Amazon EventBridge Scheduler to run the functions on a fixed schedule. Use Amazon S3 to store function outputs and logs
- () Create a container image for each script. Use AWS Step Functions to define a workflow for all scheduled tasks. Use a Wait state to delay execution and run tasks using Step Functions’ RunTask integration with ECS Fargate
- () Create a container image for each script. Use AWS Step Functions to define a workflow for all scheduled tasks. Use a Wait state to delay execution and run tasks using Step Functions’ RunTask integration with ECS Fargate - AWS Step Functions can schedule tasks using Wait states, but this approach introduces unnecessary orchestration complexity for simple cron workloads. Step Functions are best suited for multi-step workflows, not individual recurring jobs.
- () https://docs.aws.amazon.com/scheduler/latest/UserGuide/what-is-scheduler.html
- () https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html
- () https://docs.aws.amazon.com/step-functions/latest/dg/connect-ecs.html
- () https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html
- () Which combination of options will provide a scalable and low-maintenance solution for this use case? (Select two)
- () Set up an Amazon EC2 instance with a custom SFTP server using OpenSSH. Configure cron jobs to upload received files to S3. Use Amazon CloudWatch to monitor EC2 health and disk usage
- () Correct selection
- () Configure Amazon S3 bucket policies to use IAM role-based access control for each vendor. Combine this with Transfer Family identity provider integration using Amazon Cognito or a custom identity provider for fine-grained permissions
- () Deploy a fully managed AWS Transfer Family endpoint with SFTP enabled. Configure it to store uploaded files directly in an Amazon S3 bucket. Set up IAM roles mapped to each vendor for secure bucket or prefix access
- () Use AWS Transfer Family with SFTP for file uploads. Integrate the SFTP access control with Amazon Route 53 private hosted zones to create vendor-specific upload subdomains pointing to the SFTP endpoint
- () Use Amazon AppFlow to extract data from the legacy vendor systems and transform it into S3-compliant uploads. Schedule batch sync jobs to trigger every hour and send logs to CloudWatch for audit purposes
- () Correct options:

**Answer:**
Correct Answer: **Package the scripts into a container image. Use Amazon EventBridge Scheduler to define cron-based recurring schedules. Configure EventBridge Scheduler to invoke AWS Fargate tasks using Amazon ECS**

---

## Question 123

**Q:** Which solution will best meet these requirements with minimal refactoring and operational overhead?

**Options:**
- (A) Package the scripts into a container image. Deploy the image to AWS Batch with a managed compute environment on Amazon EC2. Define scheduling policies in AWS Batch to trigger jobs according to cron expressions
- (B) Package the scripts into a container image. Use Amazon EventBridge Scheduler to define cron-based recurring schedules. Configure EventBridge Scheduler to invoke AWS Fargate tasks using Amazon ECS
- (C) Convert each script into a Lambda function and package it in a zip archive. Use Amazon EventBridge Scheduler to run the functions on a fixed schedule. Use Amazon S3 to store function outputs and logs
- (D) Create a container image for each script. Use AWS Step Functions to define a workflow for all scheduled tasks. Use a Wait state to delay execution and run tasks using Step Functions’ RunTask integration with ECS Fargate
- (E) Correct option:
- (F) Incorrect options:
- (G) Create a container image for each script. Use AWS Step Functions to define a workflow for all scheduled tasks. Use a Wait state to delay execution and run tasks using Step Functions’ RunTask integration with ECS Fargate - AWS Step Functions can schedule tasks using Wait states, but this approach introduces unnecessary orchestration complexity for simple cron workloads. Step Functions are best suited for multi-step workflows, not individual recurring jobs.
- (H) References:
- (I) https://docs.aws.amazon.com/scheduler/latest/UserGuide/what-is-scheduler.html
- (J) https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html
- () https://docs.aws.amazon.com/step-functions/latest/dg/connect-ecs.html
- () https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html
- () Which combination of options will provide a scalable and low-maintenance solution for this use case? (Select two)
- () Set up an Amazon EC2 instance with a custom SFTP server using OpenSSH. Configure cron jobs to upload received files to S3. Use Amazon CloudWatch to monitor EC2 health and disk usage
- () Correct selection
- () Configure Amazon S3 bucket policies to use IAM role-based access control for each vendor. Combine this with Transfer Family identity provider integration using Amazon Cognito or a custom identity provider for fine-grained permissions
- () Deploy a fully managed AWS Transfer Family endpoint with SFTP enabled. Configure it to store uploaded files directly in an Amazon S3 bucket. Set up IAM roles mapped to each vendor for secure bucket or prefix access
- () Use AWS Transfer Family with SFTP for file uploads. Integrate the SFTP access control with Amazon Route 53 private hosted zones to create vendor-specific upload subdomains pointing to the SFTP endpoint
- () Use Amazon AppFlow to extract data from the legacy vendor systems and transform it into S3-compliant uploads. Schedule batch sync jobs to trigger every hour and send logs to CloudWatch for audit purposes
- () Correct options:
- () https://docs.aws.amazon.com/transfer/latest/userguide/what-is-aws-transfer-family.html
- () https://aws.amazon.com/blogs/storage/architecting-secure-and-compliant-managed-file-transfers-with-aws-transfer-family-sftp-connectors-and-pgp-encryption/
- () https://docs.aws.amazon.com/appflow/latest/userguide/what-is-appflow.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zones-private.html
- () Which of the following represents the MOST operationally efficient way to meet this requirement?
- () Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an Amazon S3 bucket by using a VPC gateway endpoint for Amazon S3. Set up an AWS Lambda function to process event notifications from Amazon S3 and copy the video files from Amazon S3 to the Amazon EFS file system
- () Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an Amazon S3 bucket by using public VIF. Set up an AWS Lambda function to process event notifications from Amazon S3 and copy the video files from Amazon S3 to the Amazon EFS file system
- () Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS VPC peering endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours
- **() Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS PrivateLink interface VPC endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours** [CORRECT]
- () AWS DataSync is an online data transfer service that simplifies, automates, and accelerates copying large amounts of data between on-premises storage systems and AWS Storage services, as well as between AWS Storage services.

**Answer:**
Correct Answer: **Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS PrivateLink interface VPC endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours**

---

## Question 124

**Q:** Which combination of options will provide a scalable and low-maintenance solution for this use case? (Select two)

**Options:**
- (A) Set up an Amazon EC2 instance with a custom SFTP server using OpenSSH. Configure cron jobs to upload received files to S3. Use Amazon CloudWatch to monitor EC2 health and disk usage
- (B) Correct selection
- (C) Configure Amazon S3 bucket policies to use IAM role-based access control for each vendor. Combine this with Transfer Family identity provider integration using Amazon Cognito or a custom identity provider for fine-grained permissions
- (D) Deploy a fully managed AWS Transfer Family endpoint with SFTP enabled. Configure it to store uploaded files directly in an Amazon S3 bucket. Set up IAM roles mapped to each vendor for secure bucket or prefix access
- (E) Use AWS Transfer Family with SFTP for file uploads. Integrate the SFTP access control with Amazon Route 53 private hosted zones to create vendor-specific upload subdomains pointing to the SFTP endpoint
- (F) Use Amazon AppFlow to extract data from the legacy vendor systems and transform it into S3-compliant uploads. Schedule batch sync jobs to trigger every hour and send logs to CloudWatch for audit purposes
- (G) Correct options:
- (H) Incorrect options:
- (I) References:
- (J) https://docs.aws.amazon.com/transfer/latest/userguide/what-is-aws-transfer-family.html
- () https://aws.amazon.com/blogs/storage/architecting-secure-and-compliant-managed-file-transfers-with-aws-transfer-family-sftp-connectors-and-pgp-encryption/
- () https://docs.aws.amazon.com/appflow/latest/userguide/what-is-appflow.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zones-private.html
- () Which of the following represents the MOST operationally efficient way to meet this requirement?
- () Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an Amazon S3 bucket by using a VPC gateway endpoint for Amazon S3. Set up an AWS Lambda function to process event notifications from Amazon S3 and copy the video files from Amazon S3 to the Amazon EFS file system
- () Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an Amazon S3 bucket by using public VIF. Set up an AWS Lambda function to process event notifications from Amazon S3 and copy the video files from Amazon S3 to the Amazon EFS file system
- () Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS VPC peering endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours
- **() Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS PrivateLink interface VPC endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours** [CORRECT]
- () Correct option:
- () AWS DataSync is an online data transfer service that simplifies, automates, and accelerates copying large amounts of data between on-premises storage systems and AWS Storage services, as well as between AWS Storage services.
- () You can use AWS DataSync to migrate data located on-premises, at the edge, or in other clouds to Amazon S3, Amazon EFS, Amazon FSx for Windows File Server, Amazon FSx for Lustre, Amazon FSx for OpenZFS, and Amazon FSx for NetApp ONTAP.
- () AWS DataSync:
- () via - https://aws.amazon.com/datasync/
- () To establish a private connection between your virtual private cloud (VPC) and the Amazon EFS API, you can create an interface VPC endpoint. You can also access the interface VPC endpoint from on-premises environments or other VPCs using AWS VPN, AWS Direct Connect, or VPC peering.
- () AWS Direct Connect provides three types of virtual interfaces: public, private, and transit.
- () AWS Direct Connect VIFs:
- () via - https://aws.amazon.com/premiumsupport/knowledge-center/public-private-interface-dx/
- () For the given use case, you can send data over the Direct Connect connection to an AWS PrivateLink interface VPC endpoint for Amazon EFS by using a private VIF.
- () Using task scheduling in AWS DataSync, you can periodically execute a transfer task from your source storage system to the destination. You can use the DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours.
- () https://aws.amazon.com/datasync/
- () https://aws.amazon.com/blogs/storage/transferring-files-from-on-premises-to-aws-and-back-without-leaving-your-vpc-using-aws-datasync/
- () https://docs.aws.amazon.com/efs/latest/ug/efs-vpc-endpoints.html
- () https://aws.amazon.com/datasync/faqs/
- () https://aws.amazon.com/premiumsupport/knowledge-center/public-private-interface-dx/

**Answer:**
Correct Answer: **Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS PrivateLink interface VPC endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours**

---

## Question 125

**Q:** Which of the following represents the MOST operationally efficient way to meet this requirement?

**Options:**
- (A) Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an Amazon S3 bucket by using a VPC gateway endpoint for Amazon S3. Set up an AWS Lambda function to process event notifications from Amazon S3 and copy the video files from Amazon S3 to the Amazon EFS file system
- (B) Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an Amazon S3 bucket by using public VIF. Set up an AWS Lambda function to process event notifications from Amazon S3 and copy the video files from Amazon S3 to the Amazon EFS file system
- (C) Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS VPC peering endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours
- (D) Configure an AWS DataSync agent on the on-premises server that has access to the NFS file system. Transfer data over the AWS Direct Connect connection to an AWS PrivateLink interface VPC endpoint for Amazon EFS by using a private VIF. Set up an AWS DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours
- (E) Correct option:
- (F) AWS DataSync is an online data transfer service that simplifies, automates, and accelerates copying large amounts of data between on-premises storage systems and AWS Storage services, as well as between AWS Storage services.
- (G) You can use AWS DataSync to migrate data located on-premises, at the edge, or in other clouds to Amazon S3, Amazon EFS, Amazon FSx for Windows File Server, Amazon FSx for Lustre, Amazon FSx for OpenZFS, and Amazon FSx for NetApp ONTAP.
- (H) AWS DataSync:
- (I) via - https://aws.amazon.com/datasync/
- (J) To establish a private connection between your virtual private cloud (VPC) and the Amazon EFS API, you can create an interface VPC endpoint. You can also access the interface VPC endpoint from on-premises environments or other VPCs using AWS VPN, AWS Direct Connect, or VPC peering.
- () AWS Direct Connect provides three types of virtual interfaces: public, private, and transit.
- () AWS Direct Connect VIFs:
- () via - https://aws.amazon.com/premiumsupport/knowledge-center/public-private-interface-dx/
- () For the given use case, you can send data over the Direct Connect connection to an AWS PrivateLink interface VPC endpoint for Amazon EFS by using a private VIF.
- () Using task scheduling in AWS DataSync, you can periodically execute a transfer task from your source storage system to the destination. You can use the DataSync scheduled task to send the video files to the Amazon EFS file system every 24 hours.
- () Incorrect options:
- () References:
- () https://aws.amazon.com/datasync/
- () https://aws.amazon.com/blogs/storage/transferring-files-from-on-premises-to-aws-and-back-without-leaving-your-vpc-using-aws-datasync/
- () https://docs.aws.amazon.com/efs/latest/ug/efs-vpc-endpoints.html
- () https://aws.amazon.com/datasync/faqs/
- () https://aws.amazon.com/premiumsupport/knowledge-center/public-private-interface-dx/
- () https://docs.aws.amazon.com/datasync/latest/userguide/task-scheduling.html
- () A mobile app allows users to submit photos, which are stored in an Amazon S3 bucket. Currently, a batch of Amazon EC2 Spot Instances is launched nightly to process all the day’s uploads. Each photo requires approximately 3 minutes and 512 MB of memory to process. To improve responsiveness and minimize costs, the company wants to shift to near real-time image processing that begins as soon as an image is uploaded.
- () Which solution will provide the MOST cost-effective and scalable architecture to meet these new requirements?
- **() Configure Amazon S3 to send event notifications to an Amazon SQS queue each time a photo is uploaded. Set up an AWS Lambda function to poll the queue and process images asynchronously** [CORRECT]
- () Set up Amazon S3 to push events to an Amazon SQS queue. Launch a single EC2 Reserved Instance that continuously polls the queue and processes each image upon receipt
- () Configure S3 to trigger an AWS App Runner service directly. Deploy a containerized image-processing application to App Runner to automatically process each upload
- () Enable S3 event notifications to invoke an Amazon EventBridge rule. Configure an AWS Step Functions workflow to initiate an Fargate task in Amazon ECS to process the image
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventNotifications.html
- () https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html
- () https://docs.aws.amazon.com/lambda/latest/dg/with-s3-example.html
- () https://docs.aws.amazon.com/apprunner/latest/dg/what-is-apprunner.html

**Answer:**
Correct Answer: **Configure Amazon S3 to send event notifications to an Amazon SQS queue each time a photo is uploaded. Set up an AWS Lambda function to poll the queue and process images asynchronously**

---

## Question 126

**Q:** Which solution will provide the MOST cost-effective and scalable architecture to meet these new requirements?

**Options:**
- (A) Configure Amazon S3 to send event notifications to an Amazon SQS queue each time a photo is uploaded. Set up an AWS Lambda function to poll the queue and process images asynchronously
- (B) Set up Amazon S3 to push events to an Amazon SQS queue. Launch a single EC2 Reserved Instance that continuously polls the queue and processes each image upon receipt
- (C) Configure S3 to trigger an AWS App Runner service directly. Deploy a containerized image-processing application to App Runner to automatically process each upload
- (D) Enable S3 event notifications to invoke an Amazon EventBridge rule. Configure an AWS Step Functions workflow to initiate an Fargate task in Amazon ECS to process the image
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/AmazonS3/latest/userguide/EventNotifications.html
- (I) https://docs.aws.amazon.com/lambda/latest/dg/gettingstarted-limits.html
- (J) https://docs.aws.amazon.com/lambda/latest/dg/with-s3-example.html
- () https://docs.aws.amazon.com/apprunner/latest/dg/what-is-apprunner.html
- () The engineering manager for a content management application wants to set up Amazon RDS read replicas to provide enhanced performance and read scalability. The manager wants to understand the data transfer charges while setting up Amazon RDS read replicas.
- () Which of the following would you identify as correct regarding the data transfer charges for Amazon RDS read replicas?
- () There are data transfer charges for replicating data within the same AWS Region
- () There are no data transfer charges for replicating data across AWS Regions
- () There are data transfer charges for replicating data within the same Availability Zone (AZ)
- () There are data transfer charges for replicating data across AWS Regions
- () Amazon RDS Read Replicas provide enhanced performance and durability for Amazon RDS database (DB) instances. They make it easy to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads.
- () A read replica is billed as a standard DB Instance and at the same rates. You are not charged for the data transfer incurred in replicating data between your source DB instance and read replica within the same AWS Region.
- () via - https://aws.amazon.com/rds/faqs/
- () These three options contradict the explanation provided above, so these options are incorrect.
- () Reference:
- () https://aws.amazon.com/rds/faqs/
- () The DevOps team at a major financial services company uses Multi-Availability Zone (Multi-AZ) deployment for its MySQL Amazon RDS database in order to automate its database replication and augment data durability. The DevOps team has scheduled a maintenance window for a database engine level upgrade for the coming weekend.
- () Which of the following is the correct outcome during the maintenance window?
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the standby database instance to be upgraded which is then followed by the upgrade of the primary database instance. This does not cause any downtime for the duration of the upgrade
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the primary database instance to be upgraded which is then followed by the upgrade of the standby database instance. This does not cause any downtime for the duration of the upgrade
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. However, this does not cause any downtime until the upgrade is complete
- **() Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete** [CORRECT]
- () Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching, and backups.
- () Upgrades to the database engine level require downtime. Even if your Amazon RDS DB instance uses a Multi-AZ deployment, both the primary and standby DB instances are upgraded at the same time. This causes downtime until the upgrade is complete, and the duration of the downtime varies based on the size of your database instance.
- () Amazon RDS DB Engine Maintenance:

**Answer:**
Correct Answer: **Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete**

---

## Question 127

**Q:** Which of the following would you identify as correct regarding the data transfer charges for Amazon RDS read replicas?

**Options:**
- (A) There are data transfer charges for replicating data within the same AWS Region
- (B) There are no data transfer charges for replicating data across AWS Regions
- (C) There are data transfer charges for replicating data within the same Availability Zone (AZ)
- (D) There are data transfer charges for replicating data across AWS Regions
- (E) Correct option:
- (F) Amazon RDS Read Replicas provide enhanced performance and durability for Amazon RDS database (DB) instances. They make it easy to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads.
- (G) A read replica is billed as a standard DB Instance and at the same rates. You are not charged for the data transfer incurred in replicating data between your source DB instance and read replica within the same AWS Region.
- (H) via - https://aws.amazon.com/rds/faqs/
- (I) Incorrect options:
- (J) These three options contradict the explanation provided above, so these options are incorrect.
- () Reference:
- () https://aws.amazon.com/rds/faqs/
- () The DevOps team at a major financial services company uses Multi-Availability Zone (Multi-AZ) deployment for its MySQL Amazon RDS database in order to automate its database replication and augment data durability. The DevOps team has scheduled a maintenance window for a database engine level upgrade for the coming weekend.
- () Which of the following is the correct outcome during the maintenance window?
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the standby database instance to be upgraded which is then followed by the upgrade of the primary database instance. This does not cause any downtime for the duration of the upgrade
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the primary database instance to be upgraded which is then followed by the upgrade of the standby database instance. This does not cause any downtime for the duration of the upgrade
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. However, this does not cause any downtime until the upgrade is complete
- **() Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete** [CORRECT]
- () Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching, and backups.
- () Upgrades to the database engine level require downtime. Even if your Amazon RDS DB instance uses a Multi-AZ deployment, both the primary and standby DB instances are upgraded at the same time. This causes downtime until the upgrade is complete, and the duration of the downtime varies based on the size of your database instance.
- () Amazon RDS DB Engine Maintenance:
- () via - https://aws.amazon.com/premiumsupport/knowledge-center/rds-required-maintenance/
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. However, this does not cause any downtime until the upgrade is complete - For Amazon RDS database engine level upgrade, primary and standby database instances are upgraded at the same time and it causes downtime until the upgrade is complete, hence this option is incorrect.
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the standby database instance to be upgraded which is then followed by the upgrade of the primary database instance. This does not cause any downtime for the duration of the upgrade - For Amazon RDS database engine level upgrade, primary and standby database instances are upgraded at the same time and it causes downtime until the upgrade is complete, hence this option is incorrect.
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the primary database instance to be upgraded which is then followed by the upgrade of the standby database instance. This does not cause any downtime for the duration of the upgrade - For Amazon RDS database engine level upgrade, primary and standby database instances are upgraded at the same time and it causes downtime until the upgrade is complete, hence this option is incorrect.
- () https://aws.amazon.com/premiumsupport/knowledge-center/rds-required-maintenance/
- () An IT company is working on a client project to build a Supply Chain Management application. The web-tier of the application runs on an Amazon EC2 instance and the database tier is on Amazon RDS MySQL. For beta testing, all the resources are currently deployed in a single Availability Zone (AZ). The development team wants to improve application availability before the go-live.

**Answer:**
Correct Answer: **Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete**

---

## Question 128

**Q:** Which of the following is the correct outcome during the maintenance window?

**Options:**
- (A) Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the standby database instance to be upgraded which is then followed by the upgrade of the primary database instance. This does not cause any downtime for the duration of the upgrade
- (B) Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the primary database instance to be upgraded which is then followed by the upgrade of the standby database instance. This does not cause any downtime for the duration of the upgrade
- (C) Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. However, this does not cause any downtime until the upgrade is complete
- **(D) Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete** [CORRECT]
- (E) Correct option:
- (F) Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching, and backups.
- (G) Upgrades to the database engine level require downtime. Even if your Amazon RDS DB instance uses a Multi-AZ deployment, both the primary and standby DB instances are upgraded at the same time. This causes downtime until the upgrade is complete, and the duration of the downtime varies based on the size of your database instance.
- (H) Amazon RDS DB Engine Maintenance:
- (I) via - https://aws.amazon.com/premiumsupport/knowledge-center/rds-required-maintenance/
- (J) Incorrect options:
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. However, this does not cause any downtime until the upgrade is complete - For Amazon RDS database engine level upgrade, primary and standby database instances are upgraded at the same time and it causes downtime until the upgrade is complete, hence this option is incorrect.
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the standby database instance to be upgraded which is then followed by the upgrade of the primary database instance. This does not cause any downtime for the duration of the upgrade - For Amazon RDS database engine level upgrade, primary and standby database instances are upgraded at the same time and it causes downtime until the upgrade is complete, hence this option is incorrect.
- () Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers the primary database instance to be upgraded which is then followed by the upgrade of the standby database instance. This does not cause any downtime for the duration of the upgrade - For Amazon RDS database engine level upgrade, primary and standby database instances are upgraded at the same time and it causes downtime until the upgrade is complete, hence this option is incorrect.
- () Reference:
- () https://aws.amazon.com/premiumsupport/knowledge-center/rds-required-maintenance/
- () An IT company is working on a client project to build a Supply Chain Management application. The web-tier of the application runs on an Amazon EC2 instance and the database tier is on Amazon RDS MySQL. For beta testing, all the resources are currently deployed in a single Availability Zone (AZ). The development team wants to improve application availability before the go-live.

**Answer:**
Correct Answer: **Any database engine level upgrade for an Amazon RDS database instance with Multi-AZ deployment triggers both the primary and standby database instances to be upgraded at the same time. This causes downtime until the upgrade is complete**

---

## Question 129

**Q:** Given that all end users of the web application would be located in the US, which of the following would be the MOST resource-efficient solution?

**Options:**
- (A) Deploy the web-tier Amazon EC2 instances in two regions, behind an Elastic Load Balancer. Deploy the Amazon RDS MySQL database in read replica configuration
- (B) Deploy the web-tier Amazon EC2 instances in two Availability Zones (AZs), behind an Elastic Load Balancer. Deploy the Amazon RDS MySQL database in Multi-AZ configuration
- (C) Deploy the web-tier Amazon EC2 instances in two Availability Zones (AZs), behind an Elastic Load Balancer. Deploy the Amazon RDS MySQL database in read replica configuration
- (D) Deploy the web-tier Amazon EC2 instances in two regions, behind an Elastic Load Balancer. Deploy the Amazon RDS MySQL database in Multi-AZ configuration
- (E) Correct option:
- (F) Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions. It can handle the varying load of your application traffic in a single Availability Zone or across multiple Availability Zones. Therefore, deploying the web-tier Amazon EC2 instances in two Availability Zones (AZs), behind an Elastic Load Balancer would improve the availability of the application.
- (G) Incorrect options:
- (H) Amazon RDS Read Replicas provide enhanced performance and durability for RDS database (DB) instances. They make it easy to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads. Read replicas are meant to address scalability issues. You cannot use read replicas for improving availability, so both these options are incorrect.
- (I) Exam Alert:
- (J) Please review this comparison vis-a-vis Multi-AZ vs Read Replica for Amazon RDS:
- () via - https://aws.amazon.com/rds/features/multi-az/
- () Deploy the web-tier Amazon EC2 instances in two regions, behind an Elastic Load Balancer. Deploy the Amazon RDS MySQL database in Multi-AZ configuration - As Elastic Load Balancing does not work across regions, so this option is incorrect.
- () Reference:
- () https://aws.amazon.com/rds/features/multi-az/
- () Consider the following policy associated with an IAM group containing several users:
- ()         },
- () Which of the following options is correct?
- () Users belonging to the IAM user group cannot terminate an Amazon EC2 instance in the us-west-1 region when the user's source IP is 10.200.200.200
- () Users belonging to the IAM user group can terminate an Amazon EC2 instance belonging to any region except the us-west-1 region when the user's source IP is 10.200.200.200
- **() Users belonging to the IAM user group can terminate an Amazon EC2 instance in the us-west-1 region when the user's source IP is 10.200.200.200** [CORRECT]
- () Users belonging to the IAM user group can terminate an Amazon EC2 instance in the us-west-1 region when the EC2 instance's IP address is 10.200.200.200

**Answer:**
Correct Answer: **Users belonging to the IAM user group can terminate an Amazon EC2 instance in the us-west-1 region when the user's source IP is 10.200.200.200**

---

## Question 130

**Q:** Which of the following options is correct?

**Options:**
- (A) Users belonging to the IAM user group cannot terminate an Amazon EC2 instance in the us-west-1 region when the user's source IP is 10.200.200.200
- (B) Users belonging to the IAM user group can terminate an Amazon EC2 instance belonging to any region except the us-west-1 region when the user's source IP is 10.200.200.200
- (C) Users belonging to the IAM user group can terminate an Amazon EC2 instance in the us-west-1 region when the user's source IP is 10.200.200.200
- (D) Users belonging to the IAM user group can terminate an Amazon EC2 instance in the us-west-1 region when the EC2 instance's IP address is 10.200.200.200
- (E) Correct option:
- (F) The given policy denies all EC2 specification actions on all resources when the region of the underlying resource is not us-west-1. The policy allows the terminate EC2 action on all resources when the source IP address is in the CIDR range 10.200.200.0/24, therefore it would allow the user with the source IP 10.200.200.200 to terminate the Amazon EC2 instance.
- (G) Incorrect options:
- (H) These three options contradict the explanation provided above, so these options are incorrect.
- (I) Reference:
- (J) https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html
- () What will you recommend?
- () Monitor the days to expiry Amazon CloudWatch metric for certificates imported into ACM. Create a CloudWatch alarm to monitor such certificates based on the days to expiry metric and then trigger a custom action of notifying the security team
- () Leverage AWS Config managed rule to check if any SSL/TLS certificates created via ACM are marked for expiration within 30 days. Configure the rule to trigger an Amazon SNS notification to the security team if any certificate expires within 30 days
- () Monitor the days to expiry Amazon CloudWatch metric for certificates created via ACM. Create a CloudWatch alarm to monitor such certificates based on the days to expiry metric and then trigger a custom action of notifying the security team
- () Leverage AWS Config managed rule to check if any third-party SSL/TLS certificates imported into ACM are marked for expiration within 30 days. Configure the rule to trigger an Amazon SNS notification to the security team if any certificate expires within 30 days
- () AWS Certificate Manager is a service that lets you easily provision, manage, and deploy public and private Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates for use with AWS services and your internal connected resources. SSL/TLS certificates are used to secure network communications and establish the identity of websites over the Internet as well as resources on private networks.
- () AWS Config provides a detailed view of the configuration of AWS resources in your AWS account. This includes how the resources are related to one another and how they were configured in the past so that you can see how the configurations and relationships change over time.
- () via - https://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.html
- () You can configure AWS Config to stream configuration changes and notifications to an Amazon SNS topic. For example, when a resource is updated, you can get a notification sent to your email, so that you can view the changes. You can also be notified when AWS Config evaluates your custom or managed rules against your resources.
- () It is certainly possible to use the days to expiry CloudWatch metric to build a CloudWatch alarm to monitor the imported ACM certificates. The alarm will, in turn, trigger a notification to the security team. But this option needs more configuration effort than directly using the AWS Config managed rule that is available off-the-shelf.
- () Any SSL/TLS certificates created via ACM do not need any monitoring/intervention for expiration. ACM automatically renews such certificates. Hence both these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html
- () https://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.html
- () https://docs.aws.amazon.com/config/latest/developerguide/evaluate-config.html
- () https://docs.aws.amazon.com/config/latest/developerguide/acm-certificate-expiration-check.html
- () https://aws.amazon.com/blogs/security/how-to-monitor-expirations-of-imported-certificates-in-aws-certificate-manager-acm/
- () You have multiple AWS accounts within a single AWS Region managed by AWS Organizations and you would like to ensure all Amazon EC2 instances in all these accounts can communicate privately. Which of the following solutions provides the capability at the CHEAPEST cost?
- () Create an AWS Transit Gateway and link all the virtual private cloud (VPCs) in all the accounts together
- () Create a VPC peering connection between all virtual private cloud (VPCs)
- () Create a Private Link between all the Amazon EC2 instances
- **() Create a virtual private cloud (VPC) in an account and share one or more of its subnets with the other accounts using Resource Access Manager** [CORRECT]

**Answer:**
Correct Answer: **Create a virtual private cloud (VPC) in an account and share one or more of its subnets with the other accounts using Resource Access Manager**

---

## Question 131

**Q:** What will you recommend?

**Options:**
- (A) Monitor the days to expiry Amazon CloudWatch metric for certificates imported into ACM. Create a CloudWatch alarm to monitor such certificates based on the days to expiry metric and then trigger a custom action of notifying the security team
- (B) Leverage AWS Config managed rule to check if any SSL/TLS certificates created via ACM are marked for expiration within 30 days. Configure the rule to trigger an Amazon SNS notification to the security team if any certificate expires within 30 days
- (C) Monitor the days to expiry Amazon CloudWatch metric for certificates created via ACM. Create a CloudWatch alarm to monitor such certificates based on the days to expiry metric and then trigger a custom action of notifying the security team
- (D) Leverage AWS Config managed rule to check if any third-party SSL/TLS certificates imported into ACM are marked for expiration within 30 days. Configure the rule to trigger an Amazon SNS notification to the security team if any certificate expires within 30 days
- (E) Correct option:
- (F) AWS Certificate Manager is a service that lets you easily provision, manage, and deploy public and private Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates for use with AWS services and your internal connected resources. SSL/TLS certificates are used to secure network communications and establish the identity of websites over the Internet as well as resources on private networks.
- (G) AWS Config provides a detailed view of the configuration of AWS resources in your AWS account. This includes how the resources are related to one another and how they were configured in the past so that you can see how the configurations and relationships change over time.
- (H) via - https://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.html
- (I) You can configure AWS Config to stream configuration changes and notifications to an Amazon SNS topic. For example, when a resource is updated, you can get a notification sent to your email, so that you can view the changes. You can also be notified when AWS Config evaluates your custom or managed rules against your resources.
- (J) Incorrect options:
- () It is certainly possible to use the days to expiry CloudWatch metric to build a CloudWatch alarm to monitor the imported ACM certificates. The alarm will, in turn, trigger a notification to the security team. But this option needs more configuration effort than directly using the AWS Config managed rule that is available off-the-shelf.
- () Any SSL/TLS certificates created via ACM do not need any monitoring/intervention for expiration. ACM automatically renews such certificates. Hence both these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html
- () https://docs.aws.amazon.com/config/latest/developerguide/how-does-config-work.html
- () https://docs.aws.amazon.com/config/latest/developerguide/evaluate-config.html
- () https://docs.aws.amazon.com/config/latest/developerguide/acm-certificate-expiration-check.html
- () https://aws.amazon.com/blogs/security/how-to-monitor-expirations-of-imported-certificates-in-aws-certificate-manager-acm/
- () You have multiple AWS accounts within a single AWS Region managed by AWS Organizations and you would like to ensure all Amazon EC2 instances in all these accounts can communicate privately. Which of the following solutions provides the capability at the CHEAPEST cost?
- () Create an AWS Transit Gateway and link all the virtual private cloud (VPCs) in all the accounts together
- () Create a VPC peering connection between all virtual private cloud (VPCs)
- () Create a Private Link between all the Amazon EC2 instances
- **() Create a virtual private cloud (VPC) in an account and share one or more of its subnets with the other accounts using Resource Access Manager** [CORRECT]
- () The correct solution is to share the subnet(s) within a VPC using RAM. This will allow all Amazon EC2 instances to be deployed in the same VPC (although from different accounts) and easily communicate with one another.
- () How AWS Resource Access Manager (AWS RAM) Works:
- () via - https://aws.amazon.com/ram/
- () Create an AWS Transit Gateway and link all the virtual private cloud (VPCs) in all the accounts together - AWS Transit Gateway is a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and their on-premises networks to a single gateway. A Transit Gateway will work but will be an expensive solution. Here we want to minimize cost.
- () https://aws.amazon.com/ram/
- () https://aws.amazon.com/privatelink/
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () https://aws.amazon.com/transit-gateway/

**Answer:**
Correct Answer: **Create a virtual private cloud (VPC) in an account and share one or more of its subnets with the other accounts using Resource Access Manager**

---

## Question 132

**Q:** You have multiple AWS accounts within a single AWS Region managed by AWS Organizations and you would like to ensure all Amazon EC2 instances in all these accounts can communicate privately. Which of the following solutions provides the capability at the CHEAPEST cost?

**Options:**
- (A) Create an AWS Transit Gateway and link all the virtual private cloud (VPCs) in all the accounts together
- (B) Create a VPC peering connection between all virtual private cloud (VPCs)
- (C) Create a Private Link between all the Amazon EC2 instances
- **(D) Create a virtual private cloud (VPC) in an account and share one or more of its subnets with the other accounts using Resource Access Manager** [CORRECT]
- (E) Correct option:
- (F) The correct solution is to share the subnet(s) within a VPC using RAM. This will allow all Amazon EC2 instances to be deployed in the same VPC (although from different accounts) and easily communicate with one another.
- (G) How AWS Resource Access Manager (AWS RAM) Works:
- (H) via - https://aws.amazon.com/ram/
- (I) Incorrect options:
- (J) Create an AWS Transit Gateway and link all the virtual private cloud (VPCs) in all the accounts together - AWS Transit Gateway is a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and their on-premises networks to a single gateway. A Transit Gateway will work but will be an expensive solution. Here we want to minimize cost.
- () References:
- () https://aws.amazon.com/ram/
- () https://aws.amazon.com/privatelink/
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () https://aws.amazon.com/transit-gateway/
- () An HTTP application is deployed on an Auto Scaling Group, is accessible from an Application Load Balancer (ALB) that provides HTTPS termination, and accesses a PostgreSQL database managed by Amazon RDS.
- () How should you configure the security groups? (Select three)
- () Correct selection
- () The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 5432
- () The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 80
- () The security group of the Application Load Balancer should have an inbound rule from anywhere on port 443
- () The security group of the Application Load Balancer should have an inbound rule from anywhere on port 80
- () The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Amazon RDS database on port 5432
- () The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Application Load Balancer on port 80
- () Correct options:
- () The following are the characteristics of security group rules: 1. By default, security groups allow all outbound traffic. 2. Security group rules are always permissive; you can't create rules that deny access. 3. Security groups are stateful
- () PostgreSQL port = 5432 HTTP port = 80 HTTPS port = 443
- () The security group of the Application Load Balancer should have an inbound rule from anywhere on port 80 - The client sends an HTTPS request to ALB on port 443 and not on port 80, so this is incorrect.
- () The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Amazon RDS database on port 5432 - The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Application Load Balancer and not from the security group of the Amazon RDS database, so this option is incorrect.
- () The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 80 - The Amazon EC2 instance further accesses the PostgreSQL database managed by Amazon RDS on port 5432 and not on port 80, so this option is incorrect.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () As a solutions architect, which of the following would you recommend as the MOST cost-optimal solution? (Select two)

**Answer:**
Correct Answer: **Create a virtual private cloud (VPC) in an account and share one or more of its subnets with the other accounts using Resource Access Manager**

---

## Question 133

**Q:** How should you configure the security groups? (Select three)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 5432
- (C) The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 80
- (D) The security group of the Application Load Balancer should have an inbound rule from anywhere on port 443
- (E) The security group of the Application Load Balancer should have an inbound rule from anywhere on port 80
- (F) The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Amazon RDS database on port 5432
- (G) The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Application Load Balancer on port 80
- (H) Correct options:
- (I) The following are the characteristics of security group rules: 1. By default, security groups allow all outbound traffic. 2. Security group rules are always permissive; you can't create rules that deny access. 3. Security groups are stateful
- (J) PostgreSQL port = 5432 HTTP port = 80 HTTPS port = 443
- () Incorrect options:
- () The security group of the Application Load Balancer should have an inbound rule from anywhere on port 80 - The client sends an HTTPS request to ALB on port 443 and not on port 80, so this is incorrect.
- () The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Amazon RDS database on port 5432 - The security group of the Amazon EC2 instances should have an inbound rule from the security group of the Application Load Balancer and not from the security group of the Amazon RDS database, so this option is incorrect.
- () The security group of Amazon RDS should have an inbound rule from the security group of the Amazon EC2 instances in the Auto Scaling group on port 80 - The Amazon EC2 instance further accesses the PostgreSQL database managed by Amazon RDS on port 5432 and not on port 80, so this option is incorrect.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () As a solutions architect, which of the following would you recommend as the MOST cost-optimal solution? (Select two)
- () Setup a lifecycle policy to transition the raw zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation
- () Use AWS Glue ETL job to write the transformed data in the refined zone using a compressed file format
- () Setup a lifecycle policy to transition the refined zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation
- () Create an AWS Lambda function based job to delete the raw zone data after 1 day
- () Use AWS Glue ETL job to write the transformed data in the refined zone using CSV format
- () You can manage your objects so that they are stored cost-effectively throughout their lifecycle by configuring their Amazon S3 Lifecycle. An S3 Lifecycle configuration is a set of rules that define actions that Amazon S3 applies to a group of objects. For example, you might choose to transition objects to the Amazon S3 Standard-IA storage class 30 days after you created them, or archive objects to the Amazon S3 Glacier storage class one year after creating them.
- () For the given use-case, the raw zone consists of the source data, so it cannot be deleted due to compliance reasons. Therefore, you should use a lifecycle policy to transition the raw zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation.
- () Please read more about Amazon S3 Object Lifecycle Management:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html
- () Please see this example for a AWS Glue ETL Pipeline:
- () via - https://aws.amazon.com/glue/
- () Create an AWS Lambda function based job to delete the raw zone data after 1 day - As mentioned in the use-case, the source data needs to be kept for a minimum of 5 years for compliance reasons. Therefore the data in the raw zone cannot be deleted after 1 day.
- () Setup a lifecycle policy to transition the refined zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation - You cannot transition the refined zone data into Amazon S3 Glacier Deep Archive because it is used by the business analysts for ad-hoc querying. Hence this option is incorrect.
- () Use AWS Glue ETL job to write the transformed data in the refined zone using CSV format - It is cost-optimal to write the data in the refined zone using a compressed format instead of CSV format. The compressed data would reduce the storage cost incurred on the data in the refined zone. So, this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html

**Answer:**
Correct Answer: **Correct selection**

---

## Question 134

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-optimal solution? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Setup a lifecycle policy to transition the raw zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation
- (C) Use AWS Glue ETL job to write the transformed data in the refined zone using a compressed file format
- (D) Setup a lifecycle policy to transition the refined zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation
- (E) Create an AWS Lambda function based job to delete the raw zone data after 1 day
- (F) Use AWS Glue ETL job to write the transformed data in the refined zone using CSV format
- (G) Correct options:
- (H) You can manage your objects so that they are stored cost-effectively throughout their lifecycle by configuring their Amazon S3 Lifecycle. An S3 Lifecycle configuration is a set of rules that define actions that Amazon S3 applies to a group of objects. For example, you might choose to transition objects to the Amazon S3 Standard-IA storage class 30 days after you created them, or archive objects to the Amazon S3 Glacier storage class one year after creating them.
- (I) For the given use-case, the raw zone consists of the source data, so it cannot be deleted due to compliance reasons. Therefore, you should use a lifecycle policy to transition the raw zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation.
- (J) Please read more about Amazon S3 Object Lifecycle Management:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html
- () Please see this example for a AWS Glue ETL Pipeline:
- () via - https://aws.amazon.com/glue/
- () Incorrect options:
- () Create an AWS Lambda function based job to delete the raw zone data after 1 day - As mentioned in the use-case, the source data needs to be kept for a minimum of 5 years for compliance reasons. Therefore the data in the raw zone cannot be deleted after 1 day.
- () Setup a lifecycle policy to transition the refined zone data into Amazon S3 Glacier Deep Archive after 1 day of object creation - You cannot transition the refined zone data into Amazon S3 Glacier Deep Archive because it is used by the business analysts for ad-hoc querying. Hence this option is incorrect.
- () Use AWS Glue ETL job to write the transformed data in the refined zone using CSV format - It is cost-optimal to write the data in the refined zone using a compressed format instead of CSV format. The compressed data would reduce the storage cost incurred on the data in the refined zone. So, this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html
- () https://aws.amazon.com/glue/
- () A company has recently launched a new mobile gaming application that the users are adopting rapidly. The company uses Amazon RDS MySQL as the database. The engineering team wants an urgent solution to this issue where the rapidly increasing workload might exceed the available database storage.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 135

**Q:** As a solutions architect, which of the following solutions would you recommend so that it requires minimum development and systems administration effort to address this requirement?

**Options:**
- (A) Migrate RDS MySQL database to Amazon Aurora which offers storage auto-scaling
- (B) Enable storage auto-scaling for Amazon RDS MySQL
- (C) Migrate Amazon RDS MySQL database to Amazon DynamoDB which automatically allocates storage space when required
- (D) Create read replica for Amazon RDS MySQL
- (E) Correct option:
- (F) If your workload is unpredictable, you can enable storage autoscaling for an Amazon RDS DB instance. With storage autoscaling enabled, when Amazon RDS detects that you are running out of free database space it automatically scales up your storage. Amazon RDS starts a storage modification for an autoscaling-enabled DB instance when these factors apply:
- (G) Free available space is less than 10 percent of the allocated storage.
- (H) The low-storage condition lasts at least five minutes.
- (I) At least six hours have passed since the last storage modification.
- (J) The maximum storage threshold is the limit that you set for autoscaling the DB instance. You can't set the maximum storage threshold for autoscaling-enabled instances to a value greater than the maximum allocated storage.
- () Incorrect options:
- () Migrate RDS MySQL database to Amazon Aurora which offers storage auto-scaling - Although Aurora offers automatic storage scaling, this option is ruled out since it involves significant systems administration effort to migrate from Amazon RDS MySQL to Aurora. It is much easier to just enable storage auto-scaling for Amazon RDS MySQL.
- () Migrate Amazon RDS MySQL database to Amazon DynamoDB which automatically allocates storage space when required - This option is ruled out since Amazon DynamoDB is a NoSQL database which implies significant development effort to change the application logic to connect and query data from the underlying database. It is much easier to just enable storage auto-scaling for Amazon RDS MySQL.
- () Reference:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_PIOPS.StorageTypes.html
- () A company is developing a global healthcare application that requires the least possible latency for database read/write operations from users in several geographies across the world. The company has hired you as an AWS Certified Solutions Architect Associate to build a solution using Amazon Aurora that offers an effective recovery point objective (RPO) of seconds and a recovery time objective (RTO) of a minute.
- () Which of the following options would you recommend?
- () Set up an Amazon Aurora multi-master Database cluster
- **() Set up an Amazon Aurora Global Database cluster** [CORRECT]
- () Set up an Amazon Aurora provisioned Database cluster
- () Set up an Amazon Aurora serverless Database cluster
- () Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS Regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each Region, and provides disaster recovery from Region-wide outages.
- () If your primary Region suffers a performance degradation or outage, you can promote one of the secondary Regions to take read/write responsibilities. An Aurora cluster can recover in less than 1 minute, even in the event of a complete Regional outage. This provides your application with an effective recovery point objective (RPO) of 1 second and a recovery time objective (RTO) of less than 1 minute, providing a strong foundation for a global business continuity plan.
- () via - https://aws.amazon.com/rds/aurora/global-database/
- () Both these options work in a single AWS Region, so these options are incorrect.
- () Set up an Amazon Aurora multi-master Database cluster - AWS does not offer the multi-master feature in a Aurora database cluster, so this option acts as a distractor.
- () https://aws.amazon.com/rds/aurora/global-database/
- () An application runs big data workloads on Amazon Elastic Compute Cloud (Amazon EC2) instances. The application runs 24x7 all round the year and needs at least 20 instances to maintain a minimum acceptable performance threshold and the application needs 300 instances to handle spikes in the workload. Based on historical workloads processed by the application, it needs 80 instances 80% of the time.

**Answer:**
Correct Answer: **Set up an Amazon Aurora Global Database cluster**

---

## Question 136

**Q:** Which of the following options would you recommend?

**Options:**
- (A) Set up an Amazon Aurora multi-master Database cluster
- **(B) Set up an Amazon Aurora Global Database cluster** [CORRECT]
- (C) Set up an Amazon Aurora provisioned Database cluster
- (D) Set up an Amazon Aurora serverless Database cluster
- (E) Correct option:
- (F) Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS Regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each Region, and provides disaster recovery from Region-wide outages.
- (G) If your primary Region suffers a performance degradation or outage, you can promote one of the secondary Regions to take read/write responsibilities. An Aurora cluster can recover in less than 1 minute, even in the event of a complete Regional outage. This provides your application with an effective recovery point objective (RPO) of 1 second and a recovery time objective (RTO) of less than 1 minute, providing a strong foundation for a global business continuity plan.
- (H) via - https://aws.amazon.com/rds/aurora/global-database/
- (I) Incorrect options:
- (J) Both these options work in a single AWS Region, so these options are incorrect.
- () Set up an Amazon Aurora multi-master Database cluster - AWS does not offer the multi-master feature in a Aurora database cluster, so this option acts as a distractor.
- () Reference:
- () https://aws.amazon.com/rds/aurora/global-database/
- () An application runs big data workloads on Amazon Elastic Compute Cloud (Amazon EC2) instances. The application runs 24x7 all round the year and needs at least 20 instances to maintain a minimum acceptable performance threshold and the application needs 300 instances to handle spikes in the workload. Based on historical workloads processed by the application, it needs 80 instances 80% of the time.

**Answer:**
Correct Answer: **Set up an Amazon Aurora Global Database cluster**

---

## Question 137

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-optimal solution so that it can meet the workload demand in a steady state?

**Options:**
- (A) Purchase 20 on-demand instances. Use Auto Scaling Group to provision the remaining instances as spot instances per the workload demand
- (B) Purchase 80 on-demand instances. Provision additional on-demand and spot instances per the workload demand (Use Auto Scaling Group with launch template to provision the mix of on-demand and spot instances)
- (C) Purchase 80 spot instances. Use Auto Scaling Group to provision the remaining instances as on-demand instances per the workload demand
- (D) Purchase 80 reserved instances (RIs). Provision additional on-demand and spot instances per the workload demand (Use Auto Scaling Group with launch template to provision the mix of on-demand and spot instances)
- (E) Correct option:
- (F) As the steady-state workload demand is 80 instances, we can save on costs by purchasing 80 reserved instances. Based on additional workload demand, we can specify a mix of on-demand and spot instances using Application Load Balancer with a launch template to provision the mix of on-demand and spot instances.
- (G) Please see this detailed overview of various types of Amazon EC2 instances from a pricing perspective:
- (H) via - https://aws.amazon.com/ec2/pricing/
- (I) Incorrect options:
- (J) Purchase 80 on-demand instances. Provision additional on-demand and spot instances per the workload demand (Use Auto Scaling Group with launch template to provision the mix of on-demand and spot instances) - Provisioning 80 on-demand instances would end up costlier than the option where we provision 80 reserved instances. So this option is ruled out.
- () Purchase 80 spot instances. Use Auto Scaling Group to provision the remaining instances as on-demand instances per the workload demand - The option to purchase 80 spot instances is incorrect, as there is no guarantee regarding the availability of the spot instances, which means we may not even meet the steady-state workload.
- () Reference:
- () https://aws.amazon.com/ec2/pricing/
- () A retail company wants to share sensitive accounting data that is stored in an Amazon RDS database instance with an external auditor. The auditor has its own AWS account and needs its own copy of the database.
- () Which of the following would you recommend to securely share the database with the auditor?
- () Set up a read replica of the database and configure IAM standard database authentication to grant the auditor access
- () Export the database contents to text files, store the files in Amazon S3, and create a new IAM user for the auditor with access to that bucket
- () Create an encrypted snapshot of the database, share the snapshot, and allow access to the AWS Key Management Service (AWS KMS) encryption key
- () Create a snapshot of the database in Amazon S3 and assign an IAM role to the auditor to grant access to the object in that bucket
- () You can share the AWS Key Management Service (AWS KMS) key that was used to encrypt the snapshot with any accounts that you want to be able to access the snapshot. You can share AWS KMS Key with another AWS account by adding the other account to the AWS KMS key policy.
- () Making an encrypted snapshot of the database will give the auditor a copy of the database, as required for the given use case.
- () Create a snapshot of the database in Amazon S3 and assign an IAM role to the auditor to grant access to the object in that bucket - Amazon RDS stores the DB snapshots in the Amazon S3 bucket belonging to the same AWS region where the Amazon RDS instance is located. Amazon RDS stores these on your behalf and you do not have direct access to these snapshots in Amazon S3, so it's not possible to grant access to the snapshot objects in Amazon S3.
- () Export the database contents to text files, store the files in Amazon S3, and create a new IAM user for the auditor with access to that bucket - This solution is feasible though not optimal. It requires a lot of unnecessary work and is difficult to audit when such bulk data is exported into text files.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ShareSnapshot.html
- () A security consultant is designing a solution for a company that wants to provide developers with individual AWS accounts through AWS Organizations, while also maintaining standard security controls. Since the individual developers will have AWS account root user-level access to their own accounts, the consultant wants to ensure that the mandatory AWS CloudTrail configuration that is applied to new developer accounts is not modified.
- () Which of the following actions meets the given requirements?
- () Set up a service-linked role for AWS CloudTrail with a policy condition that allows changes only from an Amazon Resource Name (ARN) in the master account
- () Set up an IAM policy that prohibits changes to AWS CloudTrail and attach it to the root user
- **() Set up a service control policy (SCP) that prohibits changes to AWS CloudTrail, and attach it to the developer accounts** [CORRECT]
- () Configure a new trail in AWS CloudTrail from within the developer accounts with the organization trails option enabled
- () Service control policy (SCP) is a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. SCPs help you to ensure your accounts stay within your organization’s access control guidelines.
- () SCPs don't affect users or roles in the management account. They affect only the member accounts in your organization.
- () Configure a new trail in AWS CloudTrail from within the developer accounts with the organization trails option enabled - Configuring each developer account individually is not a viable solution to start with. In addition, any configuration changes can be undone by the user once they are logged into their individual accounts as root users.
- () Set up an IAM policy that prohibits changes to AWS CloudTrail and attach it to the root user - The root user can modify this IAM policy itself, so this option is not correct.

**Answer:**
Correct Answer: **Set up a service control policy (SCP) that prohibits changes to AWS CloudTrail, and attach it to the developer accounts**

---

## Question 138

**Q:** Which of the following would you recommend to securely share the database with the auditor?

**Options:**
- (A) Set up a read replica of the database and configure IAM standard database authentication to grant the auditor access
- (B) Export the database contents to text files, store the files in Amazon S3, and create a new IAM user for the auditor with access to that bucket
- (C) Create an encrypted snapshot of the database, share the snapshot, and allow access to the AWS Key Management Service (AWS KMS) encryption key
- (D) Create a snapshot of the database in Amazon S3 and assign an IAM role to the auditor to grant access to the object in that bucket
- (E) Correct option:
- (F) You can share the AWS Key Management Service (AWS KMS) key that was used to encrypt the snapshot with any accounts that you want to be able to access the snapshot. You can share AWS KMS Key with another AWS account by adding the other account to the AWS KMS key policy.
- (G) Making an encrypted snapshot of the database will give the auditor a copy of the database, as required for the given use case.
- (H) Incorrect options:
- (I) Create a snapshot of the database in Amazon S3 and assign an IAM role to the auditor to grant access to the object in that bucket - Amazon RDS stores the DB snapshots in the Amazon S3 bucket belonging to the same AWS region where the Amazon RDS instance is located. Amazon RDS stores these on your behalf and you do not have direct access to these snapshots in Amazon S3, so it's not possible to grant access to the snapshot objects in Amazon S3.
- (J) Export the database contents to text files, store the files in Amazon S3, and create a new IAM user for the auditor with access to that bucket - This solution is feasible though not optimal. It requires a lot of unnecessary work and is difficult to audit when such bulk data is exported into text files.
- () Reference:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ShareSnapshot.html
- () A security consultant is designing a solution for a company that wants to provide developers with individual AWS accounts through AWS Organizations, while also maintaining standard security controls. Since the individual developers will have AWS account root user-level access to their own accounts, the consultant wants to ensure that the mandatory AWS CloudTrail configuration that is applied to new developer accounts is not modified.
- () Which of the following actions meets the given requirements?
- () Set up a service-linked role for AWS CloudTrail with a policy condition that allows changes only from an Amazon Resource Name (ARN) in the master account
- () Set up an IAM policy that prohibits changes to AWS CloudTrail and attach it to the root user
- **() Set up a service control policy (SCP) that prohibits changes to AWS CloudTrail, and attach it to the developer accounts** [CORRECT]
- () Configure a new trail in AWS CloudTrail from within the developer accounts with the organization trails option enabled
- () Service control policy (SCP) is a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. SCPs help you to ensure your accounts stay within your organization’s access control guidelines.
- () SCPs don't affect users or roles in the management account. They affect only the member accounts in your organization.
- () Configure a new trail in AWS CloudTrail from within the developer accounts with the organization trails option enabled - Configuring each developer account individually is not a viable solution to start with. In addition, any configuration changes can be undone by the user once they are logged into their individual accounts as root users.
- () Set up an IAM policy that prohibits changes to AWS CloudTrail and attach it to the root user - The root user can modify this IAM policy itself, so this option is not correct.
- () The linked service defines the permissions of its service-linked roles, and unless defined otherwise, only that service can assume the roles. The defined permissions include the trust policy and the permissions policy, and that permissions policy cannot be attached to any other entity such as the ARN in the master account.
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () A silicon valley based startup has a content management application with the web-tier running on Amazon EC2 instances and the database tier running on Amazon Aurora. Currently, the entire infrastructure is located in us-east-1 region. The startup has 90% of its customers in the US and Europe. The engineering team is getting reports of deteriorated application performance from customers in Europe with high application load time.
- () As a solutions architect, which of the following would you recommend addressing these performance issues? (Select two)
- () Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable geolocation routing policy in Amazon Route 53
- () Correct selection
- () Create Amazon Aurora read replicas in the eu-west-1 region
- () Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable failover routing policy in Amazon Route 53
- () Create Amazon Aurora Multi-AZ standby instance in the eu-west-1 region
- () Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable latency routing policy in Amazon Route 53
- () Correct options:
- () As customers in Europe are facing performance issues with high application load time, you can use latency based routing to reduce the latency. Hence this is the correct option.
- () Amazon Route 53 Routing Policy Overview:
- () via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html

**Answer:**
Correct Answer: **Set up a service control policy (SCP) that prohibits changes to AWS CloudTrail, and attach it to the developer accounts**

---

## Question 139

**Q:** Which of the following actions meets the given requirements?

**Options:**
- (A) Set up a service-linked role for AWS CloudTrail with a policy condition that allows changes only from an Amazon Resource Name (ARN) in the master account
- (B) Set up an IAM policy that prohibits changes to AWS CloudTrail and attach it to the root user
- **(C) Set up a service control policy (SCP) that prohibits changes to AWS CloudTrail, and attach it to the developer accounts** [CORRECT]
- (D) Configure a new trail in AWS CloudTrail from within the developer accounts with the organization trails option enabled
- (E) Correct option:
- (F) Service control policy (SCP) is a type of organization policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. SCPs help you to ensure your accounts stay within your organization’s access control guidelines.
- (G) SCPs don't affect users or roles in the management account. They affect only the member accounts in your organization.
- (H) Incorrect options:
- (I) Configure a new trail in AWS CloudTrail from within the developer accounts with the organization trails option enabled - Configuring each developer account individually is not a viable solution to start with. In addition, any configuration changes can be undone by the user once they are logged into their individual accounts as root users.
- (J) Set up an IAM policy that prohibits changes to AWS CloudTrail and attach it to the root user - The root user can modify this IAM policy itself, so this option is not correct.
- () The linked service defines the permissions of its service-linked roles, and unless defined otherwise, only that service can assume the roles. The defined permissions include the trust policy and the permissions policy, and that permissions policy cannot be attached to any other entity such as the ARN in the master account.
- () Reference:
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () A silicon valley based startup has a content management application with the web-tier running on Amazon EC2 instances and the database tier running on Amazon Aurora. Currently, the entire infrastructure is located in us-east-1 region. The startup has 90% of its customers in the US and Europe. The engineering team is getting reports of deteriorated application performance from customers in Europe with high application load time.
- () As a solutions architect, which of the following would you recommend addressing these performance issues? (Select two)
- () Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable geolocation routing policy in Amazon Route 53
- () Correct selection
- () Create Amazon Aurora read replicas in the eu-west-1 region
- () Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable failover routing policy in Amazon Route 53
- () Create Amazon Aurora Multi-AZ standby instance in the eu-west-1 region
- () Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable latency routing policy in Amazon Route 53
- () Correct options:
- () As customers in Europe are facing performance issues with high application load time, you can use latency based routing to reduce the latency. Hence this is the correct option.
- () Amazon Route 53 Routing Policy Overview:
- () via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 64TB per database instance.
- () Amazon Aurora read replicas can be used to scale out reads across regions. This will improve the application performance for users in Europe. Therefore, this is also a correct option for the given use-case.
- () Create Amazon Aurora Multi-AZ standby instance in the eu-west-1 region - Amazon Aurora Multi-AZ enhances the availability and durability for the database, it does not help in read scaling, so it is not a correct option for the given use-case.
- () References:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () https://aws.amazon.com/blogs/aws/new-cross-region-read-replicas-for-amazon-aurora/
- () An engineering team wants to examine the feasibility of the user data feature of Amazon EC2 for an upcoming project.
- () Which of the following are true about the Amazon EC2 user data configuration? (Select two)
- () By default, user data runs only during the boot cycle when you first launch an instance
- () By default, scripts entered as user data do not have root user privileges for executing
- () By default, scripts entered as user data are executed with root user privileges

**Answer:**
Correct Answer: **Set up a service control policy (SCP) that prohibits changes to AWS CloudTrail, and attach it to the developer accounts**

---

## Question 140

**Q:** As a solutions architect, which of the following would you recommend addressing these performance issues? (Select two)

**Options:**
- **(A) Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable geolocation routing policy in Amazon Route 53** [CORRECT]
- (B) Correct selection
- (C) Create Amazon Aurora read replicas in the eu-west-1 region
- (D) Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable failover routing policy in Amazon Route 53
- (E) Create Amazon Aurora Multi-AZ standby instance in the eu-west-1 region
- (F) Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable latency routing policy in Amazon Route 53
- (G) Correct options:
- (H) As customers in Europe are facing performance issues with high application load time, you can use latency based routing to reduce the latency. Hence this is the correct option.
- (I) Amazon Route 53 Routing Policy Overview:
- (J) via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 64TB per database instance.
- () Amazon Aurora read replicas can be used to scale out reads across regions. This will improve the application performance for users in Europe. Therefore, this is also a correct option for the given use-case.
- () Incorrect options:
- () Create Amazon Aurora Multi-AZ standby instance in the eu-west-1 region - Amazon Aurora Multi-AZ enhances the availability and durability for the database, it does not help in read scaling, so it is not a correct option for the given use-case.
- () References:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () https://aws.amazon.com/blogs/aws/new-cross-region-read-replicas-for-amazon-aurora/
- () An engineering team wants to examine the feasibility of the user data feature of Amazon EC2 for an upcoming project.
- () Which of the following are true about the Amazon EC2 user data configuration? (Select two)
- () By default, user data runs only during the boot cycle when you first launch an instance
- () By default, scripts entered as user data do not have root user privileges for executing
- () By default, scripts entered as user data are executed with root user privileges
- () By default, user data is executed every time an Amazon EC2 instance is re-started
- () When an instance is running, you can update user data by using root user credentials
- () User Data is generally used to perform common automated configuration tasks and even run scripts after the instance starts. When you launch an instance in Amazon EC2, you can pass two types of user data - shell scripts and cloud-init directives. You can also pass this data into the launch wizard as plain text or as a file.
- () Scripts entered as user data are executed as the root user, hence do not need the sudo command in the script. Any files you create will be owned by root; if you need non-root users to have file access, you should modify the permissions accordingly in the script.
- () By default, user data scripts and cloud-init directives run only during the boot cycle when you first launch an instance. You can update your configuration to ensure that your user data scripts and cloud-init directives run every time you restart your instance.
- () By default, user data is executed every time an Amazon EC2 instance is re-started - As discussed above, this is not a default configuration of the system. But, can be achieved by explicitly configuring the instance.
- () When an instance is running, you can update user data by using root user credentials - You can't change the user data if the instance is running (even by using root user credentials), but you can view it.
- () By default, scripts entered as user data do not have root user privileges for executing - Scripts entered as user data are executed as the root user, hence do not need the sudo command in the script.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html
- () What does this IAM policy do?
- () : [

**Answer:**
Correct Answer: **Setup another fleet of Amazon EC2 instances for the web tier in the eu-west-1 region. Enable geolocation routing policy in Amazon Route 53**

---

## Question 141

**Q:** Which of the following are true about the Amazon EC2 user data configuration? (Select two)

**Options:**
- (A) Correct selection
- (B) By default, user data runs only during the boot cycle when you first launch an instance
- (C) By default, scripts entered as user data do not have root user privileges for executing
- (D) By default, scripts entered as user data are executed with root user privileges
- (E) By default, user data is executed every time an Amazon EC2 instance is re-started
- (F) When an instance is running, you can update user data by using root user credentials
- (G) Correct options:
- (H) User Data is generally used to perform common automated configuration tasks and even run scripts after the instance starts. When you launch an instance in Amazon EC2, you can pass two types of user data - shell scripts and cloud-init directives. You can also pass this data into the launch wizard as plain text or as a file.
- (I) Scripts entered as user data are executed as the root user, hence do not need the sudo command in the script. Any files you create will be owned by root; if you need non-root users to have file access, you should modify the permissions accordingly in the script.
- (J) By default, user data scripts and cloud-init directives run only during the boot cycle when you first launch an instance. You can update your configuration to ensure that your user data scripts and cloud-init directives run every time you restart your instance.
- () Incorrect options:
- () By default, user data is executed every time an Amazon EC2 instance is re-started - As discussed above, this is not a default configuration of the system. But, can be achieved by explicitly configuring the instance.
- () When an instance is running, you can update user data by using root user credentials - You can't change the user data if the instance is running (even by using root user credentials), but you can view it.
- () By default, scripts entered as user data do not have root user privileges for executing - Scripts entered as user data are executed as the root user, hence do not need the sudo command in the script.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html
- () What does this IAM policy do?
- () : [
- ()       ],
- () : {
- () It allows running Amazon EC2 instances in the eu-west-1 region, when the API call is made from the eu-west-1 region
- () It allows running Amazon EC2 instances in any region when the API call is originating from the eu-west-1 region
- **() It allows running Amazon EC2 instances only in the eu-west-1 region, and the API call can be made from anywhere in the world** [CORRECT]
- () It allows running Amazon EC2 instances anywhere but in the eu-west-1 region
- () Correct option:
- () You can use the aws:RequestedRegion key to compare the AWS Region that was called in the request with the Region that you specify in the policy. You can use this global condition key to control which Regions can be requested.
- () aws:RequestedRegion represents the target of the API call. So in this example, we can only launch an Amazon EC2 instance in eu-west-1, and we can do this API call from anywhere.
- () These three options contradict the earlier details provided in the explanation. To summarize, aws:RequestedRegion represents the target of the API call. So, we can only launch an Amazon EC2 instance in eu-west-1 region and we can do this API call from anywhere. Hence these options are incorrect.
- () References:

**Answer:**
Correct Answer: **It allows running Amazon EC2 instances only in the eu-west-1 region, and the API call can be made from anywhere in the world**

---

## Question 142

**Q:** What does this IAM policy do?

**Options:**
- (A) : [
- (B)       ],
- (C) : {
- (D) It allows running Amazon EC2 instances in the eu-west-1 region, when the API call is made from the eu-west-1 region
- (E) It allows running Amazon EC2 instances in any region when the API call is originating from the eu-west-1 region
- (F) It allows running Amazon EC2 instances only in the eu-west-1 region, and the API call can be made from anywhere in the world
- (G) It allows running Amazon EC2 instances anywhere but in the eu-west-1 region
- (H) Correct option:
- (I) You can use the aws:RequestedRegion key to compare the AWS Region that was called in the request with the Region that you specify in the policy. You can use this global condition key to control which Regions can be requested.
- (J) aws:RequestedRegion represents the target of the API call. So in this example, we can only launch an Amazon EC2 instance in eu-west-1, and we can do this API call from anywhere.
- () Incorrect options:
- () These three options contradict the earlier details provided in the explanation. To summarize, aws:RequestedRegion represents the target of the API call. So, we can only launch an Amazon EC2 instance in eu-west-1 region and we can do this API call from anywhere. Hence these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html
- () A financial services company has developed its flagship application on AWS Cloud with data security requirements such that the encryption key must be stored in a custom application running on-premises. The company wants to offload the data storage as well as the encryption process to Amazon S3 but continue to use the existing encryption key.
- () Which of the following Amazon S3 encryption options allows the company to leverage Amazon S3 for storing data with given constraints?
- () Client-Side Encryption with data encryption is done on the client-side before sending it to Amazon S3
- **() Server-Side Encryption with Customer-Provided Keys (SSE-C)** [CORRECT]
- () Server-Side Encryption with Amazon S3 managed keys (SSE-S3)
- () Server-Side Encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS)
- () You have the following options for protecting data at rest in Amazon S3:
- () Server-Side Encryption – Request Amazon S3 to encrypt your object before saving it on disks in its data centers and then decrypt it when you download the objects.
- () Client-Side Encryption – Encrypt data client-side and upload the encrypted data to Amazon S3. In this case, you manage the encryption process, the encryption keys, and related tools.
- () For the given use-case, the company wants to manage the encryption keys via its custom application and let Amazon S3 manage the encryption, therefore you must use Server-Side Encryption with Customer-Provided Keys (SSE-C).
- () Please review these three options for Server Side Encryption on Amazon S3:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html

**Answer:**
Correct Answer: **Server-Side Encryption with Customer-Provided Keys (SSE-C)**

---

## Question 143

**Q:** Which of the following Amazon S3 encryption options allows the company to leverage Amazon S3 for storing data with given constraints?

**Options:**
- (A) Client-Side Encryption with data encryption is done on the client-side before sending it to Amazon S3
- **(B) Server-Side Encryption with Customer-Provided Keys (SSE-C)** [CORRECT]
- (C) Server-Side Encryption with Amazon S3 managed keys (SSE-S3)
- (D) Server-Side Encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS)
- (E) Correct option:
- (F) You have the following options for protecting data at rest in Amazon S3:
- (G) Server-Side Encryption – Request Amazon S3 to encrypt your object before saving it on disks in its data centers and then decrypt it when you download the objects.
- (H) Client-Side Encryption – Encrypt data client-side and upload the encrypted data to Amazon S3. In this case, you manage the encryption process, the encryption keys, and related tools.
- (I) For the given use-case, the company wants to manage the encryption keys via its custom application and let Amazon S3 manage the encryption, therefore you must use Server-Side Encryption with Customer-Provided Keys (SSE-C).
- (J) Please review these three options for Server Side Encryption on Amazon S3:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html
- () Incorrect options:
- () Server-Side Encryption with Amazon S3 managed keys (SSE-S3) - When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key. As an additional safeguard, it encrypts the key itself with a master key that it regularly rotates. So this option is incorrect.
- () Client-Side Encryption with data encryption is done on the client-side before sending it to Amazon S3 - You can encrypt the data client-side and upload the encrypted data to Amazon S3. In this case, you manage the encryption process, the encryption keys, and related tools.
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html
- () A Machine Learning research group uses a proprietary computer vision application hosted on an Amazon EC2 instance. Every time the instance needs to be stopped and started again, the application takes about 3 minutes to start as some auxiliary software programs need to be executed so that the application can function. The research group would like to minimize the application boostrap time whenever the system needs to be stopped and then started at a later point in time.

**Answer:**
Correct Answer: **Server-Side Encryption with Customer-Provided Keys (SSE-C)**

---

## Question 144

**Q:** As a solutions architect, which of the following solutions would you recommend for this use-case?

**Options:**
- (A) Use Amazon EC2 User-Data
- (B) Use Amazon EC2 Instance Hibernate
- (C) Use Amazon EC2 Meta-Data
- (D) Create an Amazon Machine Image (AMI) and launch your Amazon EC2 instances from that
- (E) Correct option:
- (F) When you hibernate an instance, AWS signals the operating system to perform hibernation (suspend-to-disk). Hibernation saves the contents from the instance memory (RAM) to your Amazon EBS root volume. AWS then persists the instance's Amazon EBS root volume and any attached Amazon EBS data volumes.
- (G) When you start your instance:
- (H) The Amazon EBS root volume is restored to its previous state
- (I) The RAM contents are reloaded
- (J) The processes that were previously running on the instance are resumed
- () Previously attached data volumes are reattached and the instance retains its instance ID
- () Overview of Amazon EC2 hibernation:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html
- () By using Amazon EC2 hibernate, we have the capability to resume it at any point of time, with the application already launched, thus helping us cut the 3 minutes start time.
- () Incorrect options:
- () Use Amazon EC2 User-Data - Amazon EC2 instance user data is the data that you specified in the form of a configuration script while launching your instance. Here, the problem is that the application takes 3 minutes to launch, no matter what. EC2 user data won't help us because it's just here to help us execute a list of commands, not speed them up.
- () Use Amazon EC2 Meta-Data - Amazon EC2 instance metadata is data about your instance that you can use to configure or manage the running instance. Instance metadata is divided into categories, for example, host name, events, and security groups. The EC2 meta-data is a distractor and can only help us determine some metadata attributes on our EC2 instances.
- () Create an Amazon Machine Image (AMI) and launch your Amazon EC2 instances from that - An Amazon Machine Image (AMI) provides the information required to launch an instance. You must specify an AMI when you launch an instance. You can launch multiple instances from a single AMI when you need multiple instances with the same configuration. You can use different AMIs to launch instances when you need instances with different configurations.
- () Creating an AMI may help with all the system dependencies, but it won't help us with speeding up the application start time.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html
- () A media company is migrating its flagship application from its on-premises data center to AWS for improving the application's read-scaling capability as well as its availability. The existing architecture leverages a Microsoft SQL Server database that sees a heavy read load. The engineering team does a full copy of the production database at the start of the business day to populate a dev database. During this period, application users face high latency leading to a bad user experience.
- () The company is looking at alternate database options and migrating database engines if required. What would you suggest?
- () Leverage Amazon RDS for SQL server with a Multi-AZ deployment and read replicas. Use the read replica as the dev database
- () Leverage Amazon RDS for MySQL with a Multi-AZ deployment and use the standby instance as the dev database
- **() Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and create the dev database by restoring from the automated backups of Amazon Aurora** [CORRECT]
- () Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and restore the dev database via mysqldump
- () Amazon Aurora Overview:
- () via - https://aws.amazon.com/rds/aurora/
- () Aurora backs up your cluster volume automatically and retains restore data for the length of the backup retention period. Aurora backups are continuous and incremental so you can quickly restore to any point within the backup retention period. No performance impact or interruption of database service occurs as backup data is being written.
- () via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Managing.Backups.html
- () For the given use case, you can create the dev database by restoring from the automated backups of Amazon Aurora.
- () Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and restore the dev database via mysqldump - Restoring the dev database via mysqldump would still result in a significant load on the primary DB, so this option fails to address the given requirement.
- () Leverage Amazon RDS for MySQL with a Multi-AZ deployment and use the standby instance as the dev database - The standby is there just for handling failover in a Multi-AZ deployment. You cannot access the standby instance and use it as a dev database. Hence this option is incorrect.
- () Leverage Amazon RDS for SQL server with a Multi-AZ deployment and read replicas. Use the read replica as the dev database - Amazon RDS supports Multi-AZ deployments for Microsoft SQL Server by using either SQL Server Database Mirroring (DBM) or Always On Availability Groups (AGs). Amazon RDS monitors and maintains the health of your Multi-AZ deployment.
- () Multi-AZ deployments provide increased availability, data durability, and fault tolerance for DB instances. In the event of planned database maintenance or unplanned service disruption, Amazon RDS automatically fails over to the up-to-date secondary DB instance. For SQL Server, I/O activity is suspended briefly during backup for Multi-AZ deployments.
- () A read replica is only meant to serve read traffic. The primary purpose of the read replica is to replicate the data in the primary DB instance. A read replica cannot be used as a dev database because it does not allow any database write operations.

**Answer:**
Correct Answer: **Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and create the dev database by restoring from the automated backups of Amazon Aurora**

---

## Question 145

**Q:** The company is looking at alternate database options and migrating database engines if required. What would you suggest?

**Options:**
- (A) Leverage Amazon RDS for SQL server with a Multi-AZ deployment and read replicas. Use the read replica as the dev database
- (B) Leverage Amazon RDS for MySQL with a Multi-AZ deployment and use the standby instance as the dev database
- (C) Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and create the dev database by restoring from the automated backups of Amazon Aurora
- (D) Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and restore the dev database via mysqldump
- (E) Correct option:
- (F) Amazon Aurora Overview:
- (G) via - https://aws.amazon.com/rds/aurora/
- (H) Aurora backs up your cluster volume automatically and retains restore data for the length of the backup retention period. Aurora backups are continuous and incremental so you can quickly restore to any point within the backup retention period. No performance impact or interruption of database service occurs as backup data is being written.
- (I) via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Managing.Backups.html
- (J) For the given use case, you can create the dev database by restoring from the automated backups of Amazon Aurora.
- () Incorrect options:
- () Leverage Amazon Aurora MySQL with Multi-AZ Aurora Replicas and restore the dev database via mysqldump - Restoring the dev database via mysqldump would still result in a significant load on the primary DB, so this option fails to address the given requirement.
- () Leverage Amazon RDS for MySQL with a Multi-AZ deployment and use the standby instance as the dev database - The standby is there just for handling failover in a Multi-AZ deployment. You cannot access the standby instance and use it as a dev database. Hence this option is incorrect.
- () Leverage Amazon RDS for SQL server with a Multi-AZ deployment and read replicas. Use the read replica as the dev database - Amazon RDS supports Multi-AZ deployments for Microsoft SQL Server by using either SQL Server Database Mirroring (DBM) or Always On Availability Groups (AGs). Amazon RDS monitors and maintains the health of your Multi-AZ deployment.
- () Multi-AZ deployments provide increased availability, data durability, and fault tolerance for DB instances. In the event of planned database maintenance or unplanned service disruption, Amazon RDS automatically fails over to the up-to-date secondary DB instance. For SQL Server, I/O activity is suspended briefly during backup for Multi-AZ deployments.
- () A read replica is only meant to serve read traffic. The primary purpose of the read replica is to replicate the data in the primary DB instance. A read replica cannot be used as a dev database because it does not allow any database write operations.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Managing.Backups.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/SQLServer.ReadReplicas.html
- () An enterprise uses a centralized Amazon S3 bucket to store logs and reports generated by multiple analytics services. Each service writes to and reads from a dedicated prefix (folder path) in the bucket. The company wants to enforce fine-grained access control so that each service can access only its own prefix, without being able to see or modify other services' data. The solution must support scalable and maintainable permissions management with minimal operational overhead.
- () Which approach will best meet these requirements?
- **() Configure individual S3 access points for each analytics service. Attach access point policies that restrict access to only the relevant prefix in the S3 bucket** [CORRECT]
- () Create separate IAM users for each service. Manually assign inline IAM policies to grant read/write permissions to the S3 bucket. Reference specific object names in the policy for each user
- () Deploy Amazon Macie to classify the objects in the bucket by prefix and apply automated object-level access policies to each object based on service tags
- () Create a single S3 bucket policy that lists all object ARNs under each prefix and grants permissions accordingly. Use resource-level permissions to restrict access to individual services
- () via - https://aws.amazon.com/blogs/storage/securing-data-in-a-virtual-private-cloud-using-amazon-s3-access-points/
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html
- () https://aws.amazon.com/blogs/storage/securing-data-in-a-virtual-private-cloud-using-amazon-s3-access-points/
- () https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html

**Answer:**
Correct Answer: **Configure individual S3 access points for each analytics service. Attach access point policies that restrict access to only the relevant prefix in the S3 bucket**

---

## Question 146

**Q:** What do you recommend as a replacement for the DFSR?

**Options:**
- (A) Amazon Simple Storage Service (Amazon S3)
- (B) Amazon Elastic File System (Amazon EFS)
- (C) Amazon FSx for Lustre
- **(D) Amazon FSx for Windows File Server** [CORRECT]
- (E) Correct option:
- (F) Amazon FSx for Windows is a perfect distributed file system, with replication capability, and can be mounted on Windows.
- (G) How Amazon FSx for Windows Works:
- (H) via - https://aws.amazon.com/fsx/windows/
- (I) Incorrect options:
- (J) Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. Amazon S3 cannot be mounted as a file system on Windows, so this option is incorrect.
- () References:
- () https://docs.microsoft.com/en-us/previous-versions/windows/desktop/dfsr/dfsr-overview
- () https://aws.amazon.com/fsx/windows/
- () https://aws.amazon.com/fsx/lustre/
- () A social media application is hosted on an Amazon EC2 fleet running behind an Application Load Balancer. The application traffic is fronted by an Amazon CloudFront distribution. The engineering team wants to decouple the user authentication process for the application, so that the application servers can just focus on the business logic.

**Answer:**
Correct Answer: **Amazon FSx for Windows File Server**

---

## Question 147

**Q:** As a Solutions Architect, which of the following solutions would you recommend to the development team so that it requires minimal development effort?

**Options:**
- (A) Use Amazon Cognito Authentication via Cognito Identity Pools for your Application Load Balancer
- (B) Use Amazon Cognito Authentication via Cognito User Pools for your Amazon CloudFront distribution
- (C) Use Amazon Cognito Authentication via Cognito Identity Pools for your Amazon CloudFront distribution
- (D) Use Amazon Cognito Authentication via Cognito User Pools for your Application Load Balancer
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-authenticate-users.html
- (G) Exam Alert:
- (H) Please review the following note to understand the differences between Amazon Cognito User Pools and Amazon Cognito Identity Pools:
- (I) via - https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html
- (J) Incorrect options:
- () Use Amazon Cognito Authentication via Cognito Identity Pools for your Application Load Balancer - There is no such thing as using Amazon Cognito Authentication via Cognito Identity Pools for managing user authentication for the application. Application-specific user authentication can be provided via Cognito User Pools. Amazon Cognito identity pools provide temporary AWS credentials for users who are guests (unauthenticated) and for users who have been authenticated and received a token.
- () Use Amazon Cognito Authentication via Cognito User Pools for your Amazon CloudFront distribution - You cannot directly integrate Cognito User Pools with CloudFront distribution as you have to create a separate AWS Lambda@Edge function to accomplish the authentication via Cognito User Pools. This involves additional development effort, so this option is not the best fit for the given use-case.
- () Use Amazon Cognito Authentication via Cognito Identity Pools for your Amazon CloudFront distribution - You cannot use Cognito Identity Pools for managing user authentication, so this option is not correct.
- () References:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/listener-authenticate-users.html
- () https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html
- () https://aws.amazon.com/blogs/networking-and-content-delivery/authorizationedge-using-cookies-protect-your-amazon-cloudfront-content-from-being-downloaded-by-unauthenticated-users/
- () Which of the following IAM policies provides read-only access to the Amazon S3 bucket mybucket and its content?
- **() {** [CORRECT]
- ()          ],
- ()       },

**Answer:**
Correct Answer: **{**

---

## Question 148

**Q:** Which of the following IAM policies provides read-only access to the Amazon S3 bucket mybucket and its content?

**Options:**
- **(A) {** [CORRECT]
- (B)          ],
- (C)       },

**Answer:**
Correct Answer: **{**

---

## Question 149

**Q:** Which of the following solutions would reduce both the administrative overhead and the costs while providing shared access to services required by workloads in each of the VPCs?

**Options:**
- (A) Use Transit VPC to reduce cost and share the resources across Amazon Virtual Private Cloud (Amazon VPCs)
- (B) Use VPCs connected with AWS Direct Connect
- (C) Use Fully meshed VPC Peering connection
- **(D) Build a shared services Amazon Virtual Private Cloud (Amazon VPC)** [CORRECT]
- (E) Correct option:
- (F) shared services VPC, which provides access to services required by workloads in each of the VPCs. This might include directory services or VPC endpoints. Sharing resources from a central location instead of building them in each VPC may reduce administrative overhead and cost.
- (G) Centralized VPC Endpoints (multiple VPCs):
- (H) via - https://aws.amazon.com/blogs/architecture/reduce-cost-and-increase-security-with-amazon-vpc-endpoints/
- (I) A VPC endpoint allows you to privately connect your VPC to supported AWS services without requiring an Internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Endpoints are virtual devices that are horizontally scaled, redundant, and highly available VPC components. They allow communication between instances in your VPC and services without imposing availability risks or bandwidth constraints on your network traffic.
- (J) Incorrect options:
- () More on Transit VPC:
- () via - https://d0.awsstatic.com/aws-answers/AWS_Single_Region_Multi_VPC_Connectivity.pdf
- () More on Fully meshed VPC Peers:
- () References:
- () https://aws.amazon.com/blogs/architecture/reduce-cost-and-increase-security-with-amazon-vpc-endpoints/
- () https://d0.awsstatic.com/aws-answers/AWS_Single_Region_Multi_VPC_Connectivity.pdf
- () A systems administrator has created a private hosted zone and associated it with a Virtual Private Cloud (VPC). However, the Domain Name System (DNS) queries for the private hosted zone remain unresolved.

**Answer:**
Correct Answer: **Build a shared services Amazon Virtual Private Cloud (Amazon VPC)**

---

## Question 150

**Q:** As a Solutions Architect, can you identify the Amazon Virtual Private Cloud (Amazon VPC) options to be configured in order to get the private hosted zone to work?

**Options:**
- (A) Remove any overlapping namespaces for the private and public hosted zones
- (B) Enable DNS hostnames and DNS resolution for private hosted zones
- (C) Fix conflicts between your private hosted zone and any Resolver rule that routes traffic to your network for the same domain name, as it results in ambiguity over the route to be taken
- (D) Fix the Name server (NS) record and Start Of Authority (SOA) records that may have been created with wrong configurations
- (E) Correct option:
- (F) DNS hostnames and DNS resolution are required settings for private hosted zones. DNS queries for private hosted zones can be resolved by the Amazon-provided VPC DNS server only. As a result, these options must be enabled for your private hosted zone to work.
- (G) DNS hostnames: For non-default virtual private clouds that aren't created using the Amazon VPC wizard, this option is disabled by default. If you create a private hosted zone for a domain and create records in the zone without enabling DNS hostnames, private hosted zones aren't enabled. To use a private hosted zone, this option must be enabled.
- (H) DNS resolution: Private hosted zones accept DNS queries only from a VPC DNS server. The IP address of the VPC DNS server is the reserved IP address at the base of the VPC IPv4 network range plus two. Enabling DNS resolution allows you to use the VPC DNS server as a Resolver for performing DNS resolution. Keep this option disabled if you're using a custom DNS server in the DHCP Options set, and you're not using a private hosted zone.
- (I) Incorrect options:
- (J) Remove any overlapping namespaces for the private and public hosted zones - If you have private and public hosted zones that have overlapping namespaces, such as example.com and accounting.example.com, then the Resolver routes traffic based on the most specific match. It won't result in unresolved queries, hence this option is wrong.
- () Fix the Name server (NS) record and Start Of Authority (SOA) records that may have been created with wrong configurations - When you create a hosted zone, Amazon Route 53 automatically creates a name server (NS) record and a start of authority (SOA) record for the zone for public hosted zone. However, this issue is about the private hosted zone, hence this is an incorrect option.
- () Fix conflicts between your private hosted zone and any Resolver rule that routes traffic to your network for the same domain name, as it results in ambiguity over the route to be taken - If you have a private hosted zone (example.com) and a Resolver rule that routes traffic to your network for the same domain name, the Resolver rule takes precedence. It won't result in unresolved queries.
- () References:
- () https://aws.amazon.com/premiumsupport/knowledge-center/vpc-enable-private-hosted-zone/
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zone-private-considerations.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zone-public-considerations.html
- () Which solution will best meet these requirements?
- () Replace all Network Load Balancers (NLBs) with Application Load Balancers (ALBs) in each Region. Register the EC2 instances as targets behind the ALBs and use cross-zone load balancing for latency distribution
- () Configure Amazon Route 53 with latency-based routing policies to direct users to the Region with the lowest response time. Use health checks to fail over to another Region if a specific NLB becomes unhealthy
- () Deploy Amazon CloudFront with HTTP caching enabled in front of the NLBs. Use CloudFront edge locations to serve user requests faster and reduce the load on the backend EC2 instances
- **() Deploy a standard accelerator in AWS Global Accelerator and register the existing regional NLBs as endpoints. Use the accelerator to route user requests through AWS’s global edge network to the closest healthy Regional NLB** [CORRECT]
- () How AWS Global Accelerator works:
- () via - https://aws.amazon.com/blogs/networking-and-content-delivery/configuring-client-ip-address-preservation-with-a-network-load-balancer-in-aws-global-accelerator/
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/introduction-how-it-works.html
- () https://aws.amazon.com/blogs/networking-and-content-delivery/configuring-client-ip-address-preservation-with-a-network-load-balancer-in-aws-global-accelerator/
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () The engineering team at a logistics company has noticed that the Auto Scaling group (ASG) is not terminating an unhealthy Amazon EC2 instance.
- () As a Solutions Architect, which of the following options would you suggest to troubleshoot the issue? (Select three)
- () The Amazon EC2 instance could be a spot instance type, which cannot be terminated by the Auto Scaling group (ASG)
- () A custom health check might have failed. The Auto Scaling group (ASG) does not terminate instances that are set unhealthy by custom checks
- () A user might have updated the configuration of the Auto Scaling group (ASG) and increased the minimum number of instances forcing ASG to keep all instances alive
- () Correct selection
- () The instance has failed the Elastic Load Balancing (ELB) health check status
- () The health check grace period for the instance has not expired

**Answer:**
Correct Answer: **Deploy a standard accelerator in AWS Global Accelerator and register the existing regional NLBs as endpoints. Use the accelerator to route user requests through AWS’s global edge network to the closest healthy Regional NLB**

---

## Question 151

**Q:** As a Solutions Architect, which of the following options would you suggest to troubleshoot the issue? (Select three)

**Options:**
- (A) The Amazon EC2 instance could be a spot instance type, which cannot be terminated by the Auto Scaling group (ASG)
- (B) A custom health check might have failed. The Auto Scaling group (ASG) does not terminate instances that are set unhealthy by custom checks
- (C) A user might have updated the configuration of the Auto Scaling group (ASG) and increased the minimum number of instances forcing ASG to keep all instances alive
- (D) Correct selection
- (E) The instance has failed the Elastic Load Balancing (ELB) health check status
- (F) The health check grace period for the instance has not expired
- (G) The instance maybe in Impaired status
- (H) Correct options:
- (I) Amazon EC2 Auto Scaling doesn't terminate an instance that came into service based on Amazon EC2 status checks and Elastic Load Balancing (ELB) health checks until the health check grace period expires.
- (J) More on Health check grace period:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/healthcheck.html#health-check-grace-period
- () Amazon EC2 Auto Scaling does not immediately terminate instances with an Impaired status. Instead, Amazon EC2 Auto Scaling waits a few minutes for the instance to recover. Amazon EC2 Auto Scaling might also delay or not terminate instances that fail to report data for status checks. This usually happens when there is insufficient data for the status check metrics in Amazon CloudWatch.
- () By default, Amazon EC2 Auto Scaling doesn't use the results of ELB health checks to determine an instance's health status when the group's health check configuration is set to EC2. As a result, Amazon EC2 Auto Scaling doesn't terminate instances that fail ELB health checks. If an instance's status is OutofService on the ELB console, but the instance's status is Healthy on the Amazon EC2 Auto Scaling console, confirm that the health check type is set to ELB.
- () Incorrect options:
- () The Amazon EC2 instance could be a spot instance type, which cannot be terminated by the Auto Scaling group (ASG) - This is an incorrect statement. Amazon EC2 Auto Scaling terminates Spot instances when capacity is no longer available or the Spot price exceeds your maximum price.
- () A user might have updated the configuration of the Auto Scaling group (ASG) and increased the minimum number of instances forcing ASG to keep all instances alive - This statement is incorrect. If the configuration is updated and ASG needs more number of instances, ASG will launch new, healthy instances and does not keep unhealthy ones alive.
- () A custom health check might have failed. The Auto Scaling group (ASG) does not terminate instances that are set unhealthy by custom checks - This statement is incorrect. You can define custom health checks in Amazon EC2 Auto Scaling. When a custom health check determines that an instance is unhealthy, the check manually triggers SetInstanceHealth and then sets the instance's state to Unhealthy. Amazon EC2 Auto Scaling then terminates the unhealthy instance.
- () References:
- () https://aws.amazon.com/premiumsupport/knowledge-center/auto-scaling-terminate-instance/
- () https://aws.amazon.com/premiumsupport/knowledge-center/auto-scaling-instance-how-terminated/
- () What should the solutions architect do to meet these requirements?
- () Implement an AWS IoT Core rule to route location updates directly from each sensor to Amazon SNS. Configure the application to poll the SNS topic for new messages
- () Set up a containerized service using Amazon ECS with an internal queue built into the application layer. Configure the motion sensors to send location updates directly to the container endpoints
- () Deploy an Amazon Data Firehose delivery stream to collect the motion data. Configure it to deliver data to an S3 bucket where the application scans and processes the files periodically
- **() Create an Amazon Simple Queue Service (Amazon SQS) queue to buffer the incoming location data. Configure the backend application to poll the queue and process messages** [CORRECT]
- () Correct option:
- () via - https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html
- () https://docs.aws.amazon.com/firehose/latest/dev/what-is-this-service.html
- () https://docs.aws.amazon.com/iot/latest/developerguide/iot-rules.html
- () A Hollywood studio is planning a series of promotional events leading up to the launch of the trailer of its next sci-fi thriller. The executives at the studio want to create a static website with lots of animations in line with the theme of the movie. The studio has hired you as a solutions architect to build a scalable serverless solution.
- () Which of the following represents the MOST cost-optimal and high-performance solution?

**Answer:**
Correct Answer: **Create an Amazon Simple Queue Service (Amazon SQS) queue to buffer the incoming location data. Configure the backend application to poll the queue and process messages**

---

## Question 152

**Q:** Which of the following represents the MOST cost-optimal and high-performance solution?

**Options:**
- (A) Build the website as a static website hosted on Amazon S3. Create an Amazon CloudFront distribution with Amazon S3 as the origin. Use Amazon Route 53 to create an alias record that points to your Amazon CloudFront distribution
- (B) Host the website on an instance in the studio's on-premises data center. Create an Amazon CloudFront distribution with this instance as the custom origin
- (C) Host the website on an Amazon EC2 instance. Create a Amazon CloudFront distribution with the Amazon EC2 instance as the custom origin
- (D) Host the website on AWS Lambda. Create an Amazon CloudFront distribution with Lambda as the origin
- (E) Correct option:
- (F) You can use Amazon S3 to host a static website. On a static website, individual web pages include static content. They might also contain client-side scripts. To host a static website on Amazon S3, you configure an Amazon S3 bucket for website hosting and then upload your website content to the bucket.
- (G) Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.
- (H) Hosting a static website on Amazon S3:
- (I) via - https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html
- (J) Incorrect options:
- () With AWS Lambda, you can run code without provisioning or managing servers. You can't host a website on Lambda. Also, you can't have CloudFront in front of Lambda. So this option is incorrect.
- () Hosting the website on an Amazon EC2 instance or a data-center specific instance is ruled out as the studio wants a serverless solution. So both these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-cloudfront-walkthrough.html
- () A manufacturing company receives unreliable service from its data center provider because the company is located in an area prone to natural disasters. The company is not ready to fully migrate to the AWS Cloud, but it wants a failover environment on AWS in case the on-premises data center fails. The company runs web servers that connect to external vendors. The data available on AWS and on-premises must be uniform.
- () Which of the following solutions would have the LEAST amount of downtime?
- () Set up a Amazon Route 53 failover record. Set up an AWS Direct Connect connection between a VPC and the data center. Run application servers on Amazon EC2 in an Auto Scaling group. Run an AWS Lambda function to execute an AWS CloudFormation template to create an Application Load Balancer
- **() Set up a Amazon Route 53 failover record. Run application servers on Amazon EC2 instances behind an Application Load Balancer in an Auto Scaling group. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3** [CORRECT]
- () Set up a Amazon Route 53 failover record. Execute an AWS CloudFormation template from a script to provision Amazon EC2 instances behind an Application Load Balancer. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3
- () Set up a Amazon Route 53 failover record. Run an AWS Lambda function to execute an AWS CloudFormation template to launch two Amazon EC2 instances. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3. Set up an AWS Direct Connect connection between a VPC and the data center
- () If you have multiple resources that perform the same function, you can configure DNS failover so that Route 53 will route your traffic from an unhealthy resource to a healthy resource.
- () Elastic Load Balancing is used to automatically distribute your incoming application traffic across all the Amazon EC2 instances that you are running. You can use Elastic Load Balancing to manage incoming requests by optimally routing traffic so that no one instance is overwhelmed. Your load balancer acts as a single point of contact for all incoming web traffic to your Auto Scaling group.
- () AWS CloudFormation is a convenient provisioning mechanism for a broad range of AWS and third-party resources. It supports the infrastructure needs of many different types of applications such as existing enterprise applications, legacy applications, applications built using a variety of AWS resources, and container-based solutions.
- () These three options involve AWS CloudFormation as part of the solution. Now, AWS CloudFormation takes time to provision the resources and hence is not the right solution when LEAST amount of downtime is mandated for the given use case. Therefore, these options are not the right fit for the given requirement.
- () https://aws.amazon.com/route53/
- () https://aws.amazon.com/storagegateway/
- () As a solutions architect, which of the following options would you select as the MOST secure configuration? (Select two)
- () For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 443
- () Correct selection
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 1433
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 443

**Answer:**
Correct Answer: **Set up a Amazon Route 53 failover record. Run application servers on Amazon EC2 instances behind an Application Load Balancer in an Auto Scaling group. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3**

---

## Question 153

**Q:** Which of the following solutions would have the LEAST amount of downtime?

**Options:**
- (A) Set up a Amazon Route 53 failover record. Set up an AWS Direct Connect connection between a VPC and the data center. Run application servers on Amazon EC2 in an Auto Scaling group. Run an AWS Lambda function to execute an AWS CloudFormation template to create an Application Load Balancer
- **(B) Set up a Amazon Route 53 failover record. Run application servers on Amazon EC2 instances behind an Application Load Balancer in an Auto Scaling group. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3** [CORRECT]
- (C) Set up a Amazon Route 53 failover record. Execute an AWS CloudFormation template from a script to provision Amazon EC2 instances behind an Application Load Balancer. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3
- (D) Set up a Amazon Route 53 failover record. Run an AWS Lambda function to execute an AWS CloudFormation template to launch two Amazon EC2 instances. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3. Set up an AWS Direct Connect connection between a VPC and the data center
- (E) Correct option:
- (F) If you have multiple resources that perform the same function, you can configure DNS failover so that Route 53 will route your traffic from an unhealthy resource to a healthy resource.
- (G) Elastic Load Balancing is used to automatically distribute your incoming application traffic across all the Amazon EC2 instances that you are running. You can use Elastic Load Balancing to manage incoming requests by optimally routing traffic so that no one instance is overwhelmed. Your load balancer acts as a single point of contact for all incoming web traffic to your Auto Scaling group.
- (H) Incorrect options:
- (I) AWS CloudFormation is a convenient provisioning mechanism for a broad range of AWS and third-party resources. It supports the infrastructure needs of many different types of applications such as existing enterprise applications, legacy applications, applications built using a variety of AWS resources, and container-based solutions.
- (J) These three options involve AWS CloudFormation as part of the solution. Now, AWS CloudFormation takes time to provision the resources and hence is not the right solution when LEAST amount of downtime is mandated for the given use case. Therefore, these options are not the right fit for the given requirement.
- () References:
- () https://aws.amazon.com/route53/
- () https://aws.amazon.com/storagegateway/
- () As a solutions architect, which of the following options would you select as the MOST secure configuration? (Select two)
- () For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 443
- () Correct selection
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 1433
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 443
- () For security group B: Add an inbound rule that allows traffic only from all sources on port 1433
- () For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 1433
- () Correct options:
- () The following are the characteristics of security group rules:
- () By default, security groups allow all outbound traffic.
- () Security group rules are always permissive; you can't create rules that deny access.
- () Security groups are stateful
- () The MOST secure configuration for the given use case is:
- () The above rules make sure that web servers are listening for traffic on all sources on the HTTPS protocol on port 443. The web servers only allow outbound traffic to MSSQL servers in Security Group B on port 1433.
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 1433. The above rule makes sure that the MSSQL servers only accept traffic from web servers in security group A on port 1433.
- () Therefore, both of these options are correct.
- () For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 443 - As the MSSQL based database instances are listening on port 1433, therefore for security group A, the outbound rule should be added on port 443 with the destination as security group B.
- () For security group B: Add an inbound rule that allows traffic only from all sources on port 1433 - The inbound rule should allow traffic only from security group A on port 1433. Allowing traffic from all sources will compromise security.
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 443 - The inbound rule should allow traffic only from security group A on port 1433 because the MSSQL based database instances are listening on port 1433.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () An application is currently hosted on four Amazon EC2 instances (behind Application Load Balancer) deployed in a single Availability Zone (AZ). To maintain an acceptable level of end-user experience, the application needs at least 4 instances to be always available.

**Answer:**
Correct Answer: **Set up a Amazon Route 53 failover record. Run application servers on Amazon EC2 instances behind an Application Load Balancer in an Auto Scaling group. Set up AWS Storage Gateway with stored volumes to back up data to Amazon S3**

---

## Question 154

**Q:** As a solutions architect, which of the following options would you select as the MOST secure configuration? (Select two)

**Options:**
- **(A) For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 443** [CORRECT]
- (B) Correct selection
- (C) For security group B: Add an inbound rule that allows traffic only from security group A on port 1433
- (D) For security group B: Add an inbound rule that allows traffic only from security group A on port 443
- (E) For security group B: Add an inbound rule that allows traffic only from all sources on port 1433
- (F) For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 1433
- (G) Correct options:
- (H) The following are the characteristics of security group rules:
- (I) By default, security groups allow all outbound traffic.
- (J) Security group rules are always permissive; you can't create rules that deny access.
- () Security groups are stateful
- () The MOST secure configuration for the given use case is:
- () The above rules make sure that web servers are listening for traffic on all sources on the HTTPS protocol on port 443. The web servers only allow outbound traffic to MSSQL servers in Security Group B on port 1433.
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 1433. The above rule makes sure that the MSSQL servers only accept traffic from web servers in security group A on port 1433.
- () Therefore, both of these options are correct.
- () Incorrect options:
- () For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 443 - As the MSSQL based database instances are listening on port 1433, therefore for security group A, the outbound rule should be added on port 443 with the destination as security group B.
- () For security group B: Add an inbound rule that allows traffic only from all sources on port 1433 - The inbound rule should allow traffic only from security group A on port 1433. Allowing traffic from all sources will compromise security.
- () For security group B: Add an inbound rule that allows traffic only from security group A on port 443 - The inbound rule should allow traffic only from security group A on port 1433 because the MSSQL based database instances are listening on port 1433.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () An application is currently hosted on four Amazon EC2 instances (behind Application Load Balancer) deployed in a single Availability Zone (AZ). To maintain an acceptable level of end-user experience, the application needs at least 4 instances to be always available.

**Answer:**
Correct Answer: **For security group A: Add an inbound rule that allows traffic from all sources on port 443. Add an outbound rule with the destination as security group B on port 443**

---

## Question 155

**Q:** As a solutions architect, which of the following would you recommend so that the application achieves high availability with MINIMUM cost?

**Options:**
- (A) Deploy the instances in three Availability Zones (AZs). Launch two instances in each Availability Zone (AZ)
- (B) Deploy the instances in one Availability Zones. Launch two instances in the Availability Zone (AZ)
- (C) Deploy the instances in two Availability Zones (AZs). Launch two instances in each Availability Zone (AZ)
- (D) Deploy the instances in two Availability Zones (AZs). Launch four instances in each Availability Zone (AZ)
- (E) Correct option:
- (F) The correct option is to deploy the instances in three Availability Zones (AZs) and launch two instances in each Availability Zone (AZ). Even if one of the AZs goes out of service, still we shall have 4 instances available and the application can maintain an acceptable level of end-user experience. Therefore, we can achieve high availability with just 6 instances in this case.
- (G) Incorrect options:
- (H) Deploy the instances in two Availability Zones (AZs). Launch two instances in each Availability Zone (AZ) - When we launch two instances in two AZs, we run the risk of falling below the minimum acceptable threshold of 4 instances if one of the AZs fails. So this option is ruled out.
- (I) Deploy the instances in two Availability Zones (AZs). Launch four instances in each Availability Zone (AZ) - When we launch four instances in two AZs, we have to bear costs for 8 instances which is NOT cost-optimal. So this option is ruled out.
- (J) Deploy the instances in one Availability Zones. Launch two instances in the Availability Zone (AZ) - We can't have just two instances in a single AZ as that is below the minimum acceptable threshold of 4 instances.
- () An analytics company wants to improve the performance of its big data processing workflows running on Amazon Elastic File System (Amazon EFS). Which of the following performance modes should be used for Amazon EFS to address this requirement?
- () General Purpose
- () Bursting Throughput
- () Max I/O
- () Provisioned Throughput
- () How Amazon EFS Works:
- () via - https://aws.amazon.com/efs/
- () Max I/O performance mode is used to scale to higher levels of aggregate throughput and operations per second. This scaling is done with a tradeoff of slightly higher latencies for file metadata operations. Highly parallelized applications and workloads, such as big data analysis, media processing, and genomic analysis, can benefit from this mode.
- () via - https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () General Purpose - General Purpose performance mode is ideal for latency-sensitive use cases, like web serving environments, content management systems, home directories, and general file serving. If you don't choose a performance mode when you create your file system, Amazon EFS selects the General Purpose mode for you by default.
- () References:
- () https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () https://aws.amazon.com/efs/
- () A financial institution is transitioning its critical back-office systems to AWS. These systems currently rely on Microsoft SQL Server databases hosted on on-premises infrastructure. The data is highly sensitive and subject to regulatory compliance. The organization wants to enhance security and minimize database management tasks as part of the migration.
- () Which solution will best meet these goals with the least operational burden?
- () Migrate the SQL Server databases to Amazon EC2 instances with encrypted EBS volumes. Use an AWS KMS customer managed key to enable encryption
- **() Migrate the SQL Server databases to a Multi-AZ Amazon RDS for SQL Server deployment. Enable encryption at rest by using an AWS Key Management Service (AWS KMS) managed key** [CORRECT]
- () Export the SQL Server databases to CSV format and store them in Amazon S3 with S3 bucket policies for access control. Use AWS Backup for data protection
- () Move the SQL Server data into Amazon Timestream to gain time series insights. Use AWS CloudTrail to monitor access to the data

**Answer:**
Correct Answer: **Migrate the SQL Server databases to a Multi-AZ Amazon RDS for SQL Server deployment. Enable encryption at rest by using an AWS Key Management Service (AWS KMS) managed key**

---

## Question 156

**Q:** An analytics company wants to improve the performance of its big data processing workflows running on Amazon Elastic File System (Amazon EFS). Which of the following performance modes should be used for Amazon EFS to address this requirement?

**Options:**
- (A) General Purpose
- (B) Bursting Throughput
- (C) Max I/O
- (D) Provisioned Throughput
- (E) Correct option:
- (F) How Amazon EFS Works:
- (G) via - https://aws.amazon.com/efs/
- (H) Max I/O performance mode is used to scale to higher levels of aggregate throughput and operations per second. This scaling is done with a tradeoff of slightly higher latencies for file metadata operations. Highly parallelized applications and workloads, such as big data analysis, media processing, and genomic analysis, can benefit from this mode.
- (I) via - https://docs.aws.amazon.com/efs/latest/ug/performance.html
- (J) Incorrect options:
- () General Purpose - General Purpose performance mode is ideal for latency-sensitive use cases, like web serving environments, content management systems, home directories, and general file serving. If you don't choose a performance mode when you create your file system, Amazon EFS selects the General Purpose mode for you by default.
- () References:
- () https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () https://aws.amazon.com/efs/
- () A financial institution is transitioning its critical back-office systems to AWS. These systems currently rely on Microsoft SQL Server databases hosted on on-premises infrastructure. The data is highly sensitive and subject to regulatory compliance. The organization wants to enhance security and minimize database management tasks as part of the migration.
- () Which solution will best meet these goals with the least operational burden?
- () Migrate the SQL Server databases to Amazon EC2 instances with encrypted EBS volumes. Use an AWS KMS customer managed key to enable encryption
- () Migrate the SQL Server databases to a Multi-AZ Amazon RDS for SQL Server deployment. Enable encryption at rest by using an AWS Key Management Service (AWS KMS) managed key
- () Export the SQL Server databases to CSV format and store them in Amazon S3 with S3 bucket policies for access control. Use AWS Backup for data protection
- () Move the SQL Server data into Amazon Timestream to gain time series insights. Use AWS CloudTrail to monitor access to the data
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_SQLServer.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- () A company has historically operated only in the us-east-1 region and stores encrypted data in Amazon S3 using SSE-KMS. As part of enhancing its security posture as well as improving the backup and recovery architecture, the company wants to store the encrypted data in Amazon S3 that is replicated into the us-west-1 AWS region. The security policies mandate that the data must be encrypted and decrypted using the same key in both AWS regions.
- () Which of the following represents the best solution to address these requirements?
- **() Create a new Amazon S3 bucket in the us-east-1 region with replication enabled from this new bucket into another bucket in us-west-1 region. Enable SSE-KMS encryption on the new bucket in us-east-1 region by using an AWS KMS multi-region key. Copy the existing data from the current Amazon S3 bucket in us-east-1 region into this new Amazon S3 bucket in us-east-1 region** [CORRECT]
- () Create an Amazon CloudWatch scheduled rule to invoke an AWS Lambda function to copy the daily data from the source bucket in us-east-1 region to the destination bucket in us-west-1 region. Provide AWS KMS key access to the AWS Lambda function for encryption and decryption operations on the data in the source and destination Amazon S3 buckets
- () Change the AWS KMS single region key used for the current Amazon S3 bucket into an AWS KMS multi-region key. Enable Amazon S3 batch replication for the existing data in the current bucket in us-east-1 region into another bucket in us-west-1 region
- () Enable replication for the current bucket in us-east-1 region into another bucket in us-west-1 region. Share the existing AWS KMS key from us-east-1 region to us-west-1 region
- () AWS KMS supports multi-region keys, which are AWS KMS keys in different AWS regions that can be used interchangeably – as though you had the same key in multiple regions. Each set of related multi-region keys has the same key material and key ID, so you can encrypt data in one AWS region and decrypt it in a different AWS region without re-encrypting or making a cross-region call to AWS KMS.

**Answer:**
Correct Answer: **Create a new Amazon S3 bucket in the us-east-1 region with replication enabled from this new bucket into another bucket in us-west-1 region. Enable SSE-KMS encryption on the new bucket in us-east-1 region by using an AWS KMS multi-region key. Copy the existing data from the current Amazon S3 bucket in us-east-1 region into this new Amazon S3 bucket in us-east-1 region**

---

## Question 157

**Q:** Which solution will best meet these goals with the least operational burden?

**Options:**
- (A) Migrate the SQL Server databases to Amazon EC2 instances with encrypted EBS volumes. Use an AWS KMS customer managed key to enable encryption
- (B) Migrate the SQL Server databases to a Multi-AZ Amazon RDS for SQL Server deployment. Enable encryption at rest by using an AWS Key Management Service (AWS KMS) managed key
- (C) Export the SQL Server databases to CSV format and store them in Amazon S3 with S3 bucket policies for access control. Use AWS Backup for data protection
- (D) Move the SQL Server data into Amazon Timestream to gain time series insights. Use AWS CloudTrail to monitor access to the data
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_SQLServer.html
- (I) https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- (J) A company has historically operated only in the us-east-1 region and stores encrypted data in Amazon S3 using SSE-KMS. As part of enhancing its security posture as well as improving the backup and recovery architecture, the company wants to store the encrypted data in Amazon S3 that is replicated into the us-west-1 AWS region. The security policies mandate that the data must be encrypted and decrypted using the same key in both AWS regions.
- () Which of the following represents the best solution to address these requirements?
- **() Create a new Amazon S3 bucket in the us-east-1 region with replication enabled from this new bucket into another bucket in us-west-1 region. Enable SSE-KMS encryption on the new bucket in us-east-1 region by using an AWS KMS multi-region key. Copy the existing data from the current Amazon S3 bucket in us-east-1 region into this new Amazon S3 bucket in us-east-1 region** [CORRECT]
- () Create an Amazon CloudWatch scheduled rule to invoke an AWS Lambda function to copy the daily data from the source bucket in us-east-1 region to the destination bucket in us-west-1 region. Provide AWS KMS key access to the AWS Lambda function for encryption and decryption operations on the data in the source and destination Amazon S3 buckets
- () Change the AWS KMS single region key used for the current Amazon S3 bucket into an AWS KMS multi-region key. Enable Amazon S3 batch replication for the existing data in the current bucket in us-east-1 region into another bucket in us-west-1 region
- () Enable replication for the current bucket in us-east-1 region into another bucket in us-west-1 region. Share the existing AWS KMS key from us-east-1 region to us-west-1 region
- () AWS KMS supports multi-region keys, which are AWS KMS keys in different AWS regions that can be used interchangeably – as though you had the same key in multiple regions. Each set of related multi-region keys has the same key material and key ID, so you can encrypt data in one AWS region and decrypt it in a different AWS region without re-encrypting or making a cross-region call to AWS KMS.
- () You can use multi-region AWS KMS keys in Amazon S3. However, Amazon S3 currently treats multi-region keys as though they were single-region keys, and does not use the multi-region features of the key.
- () Multi-region AWS KMS keys:
- () via - https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html
- () To require server-side encryption of all objects in a particular Amazon S3 bucket, you can use a policy. For example, the following bucket policy denies the upload object (s3:PutObject) permission to everyone if the request does not include the x-amz-server-side-encryption header requesting server-side encryption with SSE-KMS.
- () :[{
- () The following example IAM policies show statements for using AWS KMS server-side encryption with replication.
- () In this example, the encryption context is the object ARN. If you use SSE-KMS with an Amazon S3 Bucket Key enabled, you must use the bucket ARN as the encryption context.
- () : [{

**Answer:**
Correct Answer: **Create a new Amazon S3 bucket in the us-east-1 region with replication enabled from this new bucket into another bucket in us-west-1 region. Enable SSE-KMS encryption on the new bucket in us-east-1 region by using an AWS KMS multi-region key. Copy the existing data from the current Amazon S3 bucket in us-east-1 region into this new Amazon S3 bucket in us-east-1 region**

---

## Question 158

**Q:** Which of the following represents the best solution to address these requirements?

**Options:**
- **(A) Create a new Amazon S3 bucket in the us-east-1 region with replication enabled from this new bucket into another bucket in us-west-1 region. Enable SSE-KMS encryption on the new bucket in us-east-1 region by using an AWS KMS multi-region key. Copy the existing data from the current Amazon S3 bucket in us-east-1 region into this new Amazon S3 bucket in us-east-1 region** [CORRECT]
- (B) Create an Amazon CloudWatch scheduled rule to invoke an AWS Lambda function to copy the daily data from the source bucket in us-east-1 region to the destination bucket in us-west-1 region. Provide AWS KMS key access to the AWS Lambda function for encryption and decryption operations on the data in the source and destination Amazon S3 buckets
- (C) Change the AWS KMS single region key used for the current Amazon S3 bucket into an AWS KMS multi-region key. Enable Amazon S3 batch replication for the existing data in the current bucket in us-east-1 region into another bucket in us-west-1 region
- (D) Enable replication for the current bucket in us-east-1 region into another bucket in us-west-1 region. Share the existing AWS KMS key from us-east-1 region to us-west-1 region
- (E) Correct option:
- (F) AWS KMS supports multi-region keys, which are AWS KMS keys in different AWS regions that can be used interchangeably – as though you had the same key in multiple regions. Each set of related multi-region keys has the same key material and key ID, so you can encrypt data in one AWS region and decrypt it in a different AWS region without re-encrypting or making a cross-region call to AWS KMS.
- (G) You can use multi-region AWS KMS keys in Amazon S3. However, Amazon S3 currently treats multi-region keys as though they were single-region keys, and does not use the multi-region features of the key.
- (H) Multi-region AWS KMS keys:
- (I) via - https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html
- (J) To require server-side encryption of all objects in a particular Amazon S3 bucket, you can use a policy. For example, the following bucket policy denies the upload object (s3:PutObject) permission to everyone if the request does not include the x-amz-server-side-encryption header requesting server-side encryption with SSE-KMS.
- () :[{
- () The following example IAM policies show statements for using AWS KMS server-side encryption with replication.
- () In this example, the encryption context is the object ARN. If you use SSE-KMS with an Amazon S3 Bucket Key enabled, you must use the bucket ARN as the encryption context.
- () : [{
- () : {
- ()         },

**Answer:**
Correct Answer: **Create a new Amazon S3 bucket in the us-east-1 region with replication enabled from this new bucket into another bucket in us-west-1 region. Enable SSE-KMS encryption on the new bucket in us-east-1 region by using an AWS KMS multi-region key. Copy the existing data from the current Amazon S3 bucket in us-east-1 region into this new Amazon S3 bucket in us-east-1 region**

---

## Question 159

**Q:** Which combination of options will together meet these requirements? (Select two)

**Options:**
- **(A) Use Amazon Simple Queue Service (Amazon SQS) as the replacement for the AMQP message broker. Refactor the application to use SQS SDKs and polling logic** [CORRECT]
- (B) Correct selection
- (C) Replace the current messaging system with Amazon MQ, a fully managed broker that supports AMQP natively. Integrate the application with the Amazon MQ endpoint without modifying the existing message format
- (D) Run the application on Amazon EC2 Auto Scaling groups and use a self-hosted RabbitMQ instance on EC2 to preserve AMQP compatibility
- (E) Deploy the containerized application to Amazon Elastic Kubernetes Service (Amazon EKS) using AWS Fargate to avoid managing EC2 nodes
- (F) Deploy the application to Amazon ECS on EC2, and integrate the messaging workflow using Amazon SNS for asynchronous pub/sub delivery
- (G) Correct options:
- (H) Amazon EKS provides a Kubernetes-compatible, managed container orchestration service, which allows the company to reuse its existing Kubernetes manifests, Helm charts, and service configurations. By deploying workloads using AWS Fargate, the company avoids provisioning and managing EC2 worker nodes, aligning with the goal of reducing infrastructure overhead while maintaining scalability and agility.
- (I) Amazon MQ is a fully managed message broker service that supports AMQP (as well as MQTT, STOMP, and JMS). This allows the company to retain its existing messaging code and AMQP configuration without any major changes. Amazon MQ handles availability, durability, and patching, reducing the operational burden significantly.
- (J) Incorrect options:
- () Use Amazon Simple Queue Service (Amazon SQS) as the replacement for the AMQP message broker. Refactor the application to use SQS SDKs and polling logic - Amazon SQS does not support AMQP. To use SQS, the company would need to rewrite the messaging logic in the application to conform to SQS’s polling-based message model and SDKs. This introduces significant rework and goes against the requirement of minimal code changes.
- () Deploy the application to Amazon ECS on EC2, and integrate the messaging workflow using Amazon SNS for asynchronous pub/sub delivery - Although ECS supports containerized workloads, using EC2 launch type introduces infrastructure management responsibilities (e.g., patching, scaling, monitoring). Additionally, Amazon SNS does not support AMQP and is intended for pub/sub, not point-to-point messaging. This option fails to meet both the protocol and operational efficiency requirements.
- () Run the application on Amazon EC2 Auto Scaling groups and use a self-hosted RabbitMQ instance on EC2 to preserve AMQP compatibility - Hosting RabbitMQ on EC2 can preserve AMQP compatibility, but it comes with the burden of managing the message broker, including patching, scaling, monitoring, and failover logic. This conflicts with the requirement of minimizing operational overhead, especially when a fully managed AMQP service (Amazon MQ) is available.
- () References:
- () https://docs.aws.amazon.com/eks/latest/userguide/fargate.html
- () https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/welcome.html
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
- () https://docs.aws.amazon.com/sns/latest/dg/welcome.html

**Answer:**
Correct Answer: **Use Amazon Simple Queue Service (Amazon SQS) as the replacement for the AMQP message broker. Refactor the application to use SQS SDKs and polling logic**

---

## Question 160

**Q:** Upon a security review of your AWS account, an AWS consultant has found that a few Amazon RDS databases are unencrypted. As a Solutions Architect, what steps must be taken to encrypt the Amazon RDS databases?

**Options:**
- (A) Enable Multi-AZ for the database, and make sure the standby instance is encrypted. Stop the main database to that the standby database kicks in, then disable Multi-AZ
- (B) Enable encryption on the Amazon RDS database using the AWS Console
- (C) Create a Read Replica of the database, and encrypt the read replica. Promote the read replica as a standalone database, and terminate the previous database
- (D) Take a snapshot of the database, copy it as an encrypted snapshot, and restore a database from the encrypted snapshot. Terminate the previous database
- (E) Correct option:
- (F) Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching and backups.
- (G) You can encrypt your Amazon RDS DB instances and snapshots at rest by enabling the encryption option for your Amazon RDS DB instances. Data that is encrypted at rest includes the underlying storage for DB instances, its automated backups, read replicas, and snapshots.
- (H) You can only enable encryption for an Amazon RDS DB instance when you create it, not after the DB instance is created. However, because you can encrypt a copy of an unencrypted DB snapshot, you can effectively add encryption to an unencrypted DB instance. That is, you can create a snapshot of your DB instance, and then create an encrypted copy of that snapshot. So this is the correct option.
- (I) Incorrect options:
- (J) Create a Read Replica of the database, and encrypt the read replica. Promote the read replica as a standalone database, and terminate the previous database - If the master is not encrypted, the read replicas cannot be encrypted. So this option is incorrect.
- () Enable Multi-AZ for the database, and make sure the standby instance is encrypted. Stop the main database to that the standby database kicks in, then disable Multi-AZ - Multi-AZ is to help with High Availability, not encryption. So this option is incorrect.
- () Enable encryption on the Amazon RDS database using the AWS Console - There is no direct option to encrypt an Amazon RDS database using the AWS Console.
- () Steps to encrypt an un-encrypted RDS database: 1. Create a snapshot of the un-encrypted database 2. Copy the snapshot and enable encryption for the snapshot 3. Restore the database from the encrypted snapshot 4. Migrate applications to the new database, and delete the old database
- () Reference:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.Encryption.html
- () Which AWS architecture will best fulfill these requirements?
- () Containerize the application and deploy it to Amazon ECS with EC2 launch type behind an Application Load Balancer. Use Amazon Neptune to store structured relational data with SQL-like queries
- () Host the application on EC2 instances that are part of a target group for an Application Load Balancer. Create an Amazon RDS for MySQL Multi-AZ DB instance to provide high availability and automatic failover for the database
- () Deploy the application to EC2 instances registered in a Network Load Balancer target group. Use Amazon ElastiCache for Redis as the database and configure it with Redis Streams for persistent storage
- () Migrate the application to Amazon EC2 instances in an Auto Scaling group behind an Application Load Balancer. Use Amazon Aurora Serverless v2 for MySQL to manage the database layer with auto-scaling and built-in high availability
- () via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.how-it-works.html
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.how-it-works.html
- () https://aws.amazon.com/blogs/database/read-scalability-with-amazon-aurora-serverless-v2/
- () https://aws.amazon.com/blogs/database/introducing-scaling-to-0-capacity-with-amazon-aurora-serverless-v2/
- () https://docs.aws.amazon.com/neptune/latest/userguide/intro.html
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/WhatIs.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_MySQL.html
- () Which solution will best meet these requirements?
- () Process the extracted output with AWS Lambda to convert the text into CSV format. Query the data using Amazon Athena and visualize it using Amazon QuickSight.
- () Ingest the extracted data into Amazon Redshift using AWS Glue, and use Amazon Rekognition to analyze the tone of the document layouts for sentiment classification.
- () Use Amazon SageMaker to train a custom sentiment analysis model. Store the model outputs in Amazon DynamoDB for structured querying by analysts
- **() Send the extracted text to Amazon Comprehend for entity detection and sentiment analysis. Store the results in Amazon S3 for further access or visualization.** [CORRECT]

**Answer:**
Correct Answer: **Send the extracted text to Amazon Comprehend for entity detection and sentiment analysis. Store the results in Amazon S3 for further access or visualization.**

---

## Question 161

**Q:** Which AWS architecture will best fulfill these requirements?

**Options:**
- (A) Containerize the application and deploy it to Amazon ECS with EC2 launch type behind an Application Load Balancer. Use Amazon Neptune to store structured relational data with SQL-like queries
- (B) Host the application on EC2 instances that are part of a target group for an Application Load Balancer. Create an Amazon RDS for MySQL Multi-AZ DB instance to provide high availability and automatic failover for the database
- (C) Deploy the application to EC2 instances registered in a Network Load Balancer target group. Use Amazon ElastiCache for Redis as the database and configure it with Redis Streams for persistent storage
- (D) Migrate the application to Amazon EC2 instances in an Auto Scaling group behind an Application Load Balancer. Use Amazon Aurora Serverless v2 for MySQL to manage the database layer with auto-scaling and built-in high availability
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.how-it-works.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-serverless-v2.how-it-works.html
- (J) https://aws.amazon.com/blogs/database/read-scalability-with-amazon-aurora-serverless-v2/
- () https://aws.amazon.com/blogs/database/introducing-scaling-to-0-capacity-with-amazon-aurora-serverless-v2/
- () https://docs.aws.amazon.com/neptune/latest/userguide/intro.html
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/WhatIs.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_MySQL.html
- () Which solution will best meet these requirements?
- () Process the extracted output with AWS Lambda to convert the text into CSV format. Query the data using Amazon Athena and visualize it using Amazon QuickSight.
- () Ingest the extracted data into Amazon Redshift using AWS Glue, and use Amazon Rekognition to analyze the tone of the document layouts for sentiment classification.
- () Use Amazon SageMaker to train a custom sentiment analysis model. Store the model outputs in Amazon DynamoDB for structured querying by analysts
- **() Send the extracted text to Amazon Comprehend for entity detection and sentiment analysis. Store the results in Amazon S3 for further access or visualization.** [CORRECT]
- () Amazon Textract with Amazon Comprehend:
- () via - https://aws.amazon.com/blogs/machine-learning/extracting-custom-entities-from-documents-with-amazon-textract-and-amazon-comprehend/
- () https://docs.aws.amazon.com/textract/latest/dg/what-is.html
- () https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- () https://aws.amazon.com/blogs/machine-learning/extracting-custom-entities-from-documents-with-amazon-textract-and-amazon-comprehend/
- () https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html
- () https://docs.aws.amazon.com/athena/latest/ug/what-is.html
- () https://docs.aws.amazon.com/rekognition/latest/dg/what-is.html
- () An e-commerce application uses an Amazon Aurora Multi-AZ deployment for its database. While analyzing the performance metrics, the engineering team has found that the database reads are causing high input/output (I/O) and adding latency to the write requests against the database.

**Answer:**
Correct Answer: **Send the extracted text to Amazon Comprehend for entity detection and sentiment analysis. Store the results in Amazon S3 for further access or visualization.**

---

## Question 162

**Q:** As an AWS Certified Solutions Architect Associate, what would you recommend to separate the read requests from the write requests?

**Options:**
- (A) Provision another Amazon Aurora database and link it to the primary database as a read replica
- (B) Set up a read replica and modify the application to use the appropriate endpoint
- (C) Activate read-through caching on the Amazon Aurora database
- (D) Configure the application to read from the Multi-AZ standby instance
- (E) Correct option:
- (F) An Amazon Aurora DB cluster consists of one or more DB instances and a cluster volume that manages the data for those DB instances. An Aurora cluster volume is a virtual database storage volume that spans multiple Availability Zones (AZs), with each Availability Zone (AZ) having a copy of the DB cluster data. Two types of DB instances make up an Aurora DB cluster:
- (G) Primary DB instance – Supports read and write operations, and performs all of the data modifications to the cluster volume. Each Aurora DB cluster has one primary DB instance.
- (H) Aurora Replica – Connects to the same storage volume as the primary DB instance and supports only read operations. Each Aurora DB cluster can have up to 15 Aurora Replicas in addition to the primary DB instance. Aurora automatically fails over to an Aurora Replica in case the primary DB instance becomes unavailable. You can specify the failover priority for Aurora Replicas. Aurora Replicas can also offload read workloads from the primary DB instance.
- (I) via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.html
- (J) While setting up a Multi-AZ deployment for Aurora, you create an Aurora replica or reader node in a different Availability Zone (AZ).
- () Multi-AZ for Aurora:
- () You use the reader endpoint for read-only connections for your Aurora cluster. This endpoint uses a load-balancing mechanism to help your cluster handle a query-intensive workload. The reader endpoint is the endpoint that you supply to applications that do reporting or other read-only operations on the cluster. The reader endpoint load-balances connections to available Aurora Replicas in an Aurora DB cluster.
- () via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.Endpoints.html
- () Incorrect options:
- () Provision another Amazon Aurora database and link it to the primary database as a read replica - You cannot provision another Aurora database and then link it as a read-replica for the primary database. This option is ruled out.
- () Configure the application to read from the Multi-AZ standby instance - This option has been added as a distractor as Aurora does not have any entity called standby instance. You create a standby instance while setting up a Multi-AZ deployment for Amazon RDS and NOT for Aurora.
- () Multi-AZ for Amazon RDS:
- () Activate read-through caching on the Amazon Aurora database - Amazon Aurora does not have built-in support for read-through caching, so this option just serves as a distractor. To implement caching, you will need to integrate something like Amazon ElastiCache and that would need code changes for the application.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.AuroraHighAvailability.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.Endpoints.html
- () A company is looking at storing their less frequently accessed files on AWS that can be concurrently accessed by hundreds of Amazon EC2 instances. The company needs the most cost-effective file storage service that provides immediate access to data whenever needed.
- () Which of the following options represents the best solution for the given requirements?
- () Amazon Elastic Block Store (EBS)
- () Amazon S3 Standard-Infrequent Access (S3 Standard-IA) storage class
- () Amazon Elastic File System (EFS) Standard storage class
- **() Amazon Elastic File System (EFS) Standard–IA storage class** [CORRECT]
- () Amazon Elastic File System (EFS) Standard–IA storage class - Amazon EFS is a file storage service for use with Amazon compute (EC2, containers, serverless) and on-premises servers. Amazon EFS provides a file system interface, file system access semantics (such as strong consistency and file locking), and concurrently accessible storage for up to thousands of Amazon EC2 instances.
- () The Amazon S3 Standard–IA storage class reduces storage costs for files that are not accessed every day. It does this without sacrificing the high availability, high durability, elasticity, and POSIX file system access that Amazon EFS provides. AWS recommends Standard-IA storage if you need your full dataset to be readily accessible and want to automatically save on storage costs for files that are less frequently accessed.
- () Amazon S3 Standard-Infrequent Access (S3 Standard-IA) storage class - Amazon S3 is an object storage service. Amazon S3 makes data available through an Internet API that can be accessed anywhere. It is not a file storage service, as is needed in the use case.
- () Amazon Elastic Block Store (EBS) - Amazon EBS is a block-level storage service for use with Amazon EC2. Amazon EBS can deliver performance for workloads that require the lowest latency access to data from a single Amazon EC2 instance. Amazon EBS volume cannot be accessed by hundreds of Amazon EC2 instances concurrently. It is not a file storage service, as is needed in the use case.
- () Reference:
- () https://docs.aws.amazon.com/efs/latest/ug/storage-classes.html
- () You are establishing a monitoring solution for desktop systems, that will be sending telemetry data into AWS every 1 minute. Data for each system must be processed in order, independently, and you would like to scale the number of consumers to be possibly equal to the number of desktop systems that are being monitored.
- () What do you recommend?

**Answer:**
Correct Answer: **Amazon Elastic File System (EFS) Standard–IA storage class**

---

## Question 163

**Q:** Which of the following options represents the best solution for the given requirements?

**Options:**
- (A) Amazon Elastic Block Store (EBS)
- (B) Amazon S3 Standard-Infrequent Access (S3 Standard-IA) storage class
- (C) Amazon Elastic File System (EFS) Standard storage class
- (D) Amazon Elastic File System (EFS) Standard–IA storage class
- (E) Correct option:
- (F) Amazon Elastic File System (EFS) Standard–IA storage class - Amazon EFS is a file storage service for use with Amazon compute (EC2, containers, serverless) and on-premises servers. Amazon EFS provides a file system interface, file system access semantics (such as strong consistency and file locking), and concurrently accessible storage for up to thousands of Amazon EC2 instances.
- (G) The Amazon S3 Standard–IA storage class reduces storage costs for files that are not accessed every day. It does this without sacrificing the high availability, high durability, elasticity, and POSIX file system access that Amazon EFS provides. AWS recommends Standard-IA storage if you need your full dataset to be readily accessible and want to automatically save on storage costs for files that are less frequently accessed.
- (H) Incorrect options:
- (I) Amazon S3 Standard-Infrequent Access (S3 Standard-IA) storage class - Amazon S3 is an object storage service. Amazon S3 makes data available through an Internet API that can be accessed anywhere. It is not a file storage service, as is needed in the use case.
- (J) Amazon Elastic Block Store (EBS) - Amazon EBS is a block-level storage service for use with Amazon EC2. Amazon EBS can deliver performance for workloads that require the lowest latency access to data from a single Amazon EC2 instance. Amazon EBS volume cannot be accessed by hundreds of Amazon EC2 instances concurrently. It is not a file storage service, as is needed in the use case.
- () Reference:
- () https://docs.aws.amazon.com/efs/latest/ug/storage-classes.html
- () You are establishing a monitoring solution for desktop systems, that will be sending telemetry data into AWS every 1 minute. Data for each system must be processed in order, independently, and you would like to scale the number of consumers to be possibly equal to the number of desktop systems that are being monitored.
- () What do you recommend?
- () Use an Amazon Simple Queue Service (Amazon SQS) FIFO (First-In-First-Out) queue, and make sure the telemetry data is sent with a Group ID attribute representing the value of the Desktop ID
- () Use an Amazon Simple Queue Service (Amazon SQS) FIFO (First-In-First-Out) queue, and send the telemetry data as is
- () Use an Amazon Simple Queue Service (Amazon SQS) standard queue, and send the telemetry data as is
- () Use an Amazon Kinesis Data Stream, and send the telemetry data with a Partition ID that uses the value of the Desktop ID
- () Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS offers two types of message queues. Standard queues offer maximum throughput, best-effort ordering, and at-least-once delivery. SQS FIFO queues are designed to guarantee that messages are processed exactly once, in the exact order that they are sent.
- ()  attribute. So this is the correct option.
- ()  attribute so that multiple consumers can read data for each Desktop application.
- () Use an Amazon Simple Queue Service (Amazon SQS) standard queue, and send the telemetry data as is - An Amazon SQS standard queue has no ordering capability so that's ruled out.
- () References:
- () https://aws.amazon.com/blogs/compute/solving-complex-ordering-challenges-with-amazon-sqs-fifo-queues/
- () https://aws.amazon.com/sqs/faqs/
- () https://aws.amazon.com/kinesis/data-streams/faqs/
- () A media production studio is building a content rendering and editing platform on AWS. The editing workstations and rendering tools require access to shared files over the SMB (Server Message Block) protocol. The studio wants a managed storage solution that is simple to set up, integrates easily with SMB clients, and minimizes ongoing operational tasks.
- () Which solution will best meet the requirements with the LEAST administrative overhead?
- () Use Amazon S3 with Transfer Acceleration enabled. Configure the application to upload and download files over HTTPS using signed URLs
- () Launch an Amazon EC2 Windows instance and manually configure a Windows file share. Use this instance to serve SMB access to application clients
- () Set up an AWS Storage Gateway Volume Gateway in cached volume mode. Attach the volume as an iSCSI device to the application server and configure a file system with SMB sharing enabled
- **() Provision an Amazon FSx for Windows File Server file system. Mount the file system using the SMB protocol on the media servers** [CORRECT]
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/what-is.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html

**Answer:**
Correct Answer: **Provision an Amazon FSx for Windows File Server file system. Mount the file system using the SMB protocol on the media servers**

---

## Question 164

**Q:** What do you recommend?

**Options:**
- (A) Use an Amazon Simple Queue Service (Amazon SQS) FIFO (First-In-First-Out) queue, and make sure the telemetry data is sent with a Group ID attribute representing the value of the Desktop ID
- (B) Use an Amazon Simple Queue Service (Amazon SQS) FIFO (First-In-First-Out) queue, and send the telemetry data as is
- (C) Use an Amazon Simple Queue Service (Amazon SQS) standard queue, and send the telemetry data as is
- (D) Use an Amazon Kinesis Data Stream, and send the telemetry data with a Partition ID that uses the value of the Desktop ID
- (E) Correct option:
- (F) Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS offers two types of message queues. Standard queues offer maximum throughput, best-effort ordering, and at-least-once delivery. SQS FIFO queues are designed to guarantee that messages are processed exactly once, in the exact order that they are sent.
- (G)  attribute. So this is the correct option.
- (H) Incorrect options:
- (I)  attribute so that multiple consumers can read data for each Desktop application.
- (J) Use an Amazon Simple Queue Service (Amazon SQS) standard queue, and send the telemetry data as is - An Amazon SQS standard queue has no ordering capability so that's ruled out.
- () References:
- () https://aws.amazon.com/blogs/compute/solving-complex-ordering-challenges-with-amazon-sqs-fifo-queues/
- () https://aws.amazon.com/sqs/faqs/
- () https://aws.amazon.com/kinesis/data-streams/faqs/
- () A media production studio is building a content rendering and editing platform on AWS. The editing workstations and rendering tools require access to shared files over the SMB (Server Message Block) protocol. The studio wants a managed storage solution that is simple to set up, integrates easily with SMB clients, and minimizes ongoing operational tasks.
- () Which solution will best meet the requirements with the LEAST administrative overhead?
- () Use Amazon S3 with Transfer Acceleration enabled. Configure the application to upload and download files over HTTPS using signed URLs
- () Launch an Amazon EC2 Windows instance and manually configure a Windows file share. Use this instance to serve SMB access to application clients
- () Set up an AWS Storage Gateway Volume Gateway in cached volume mode. Attach the volume as an iSCSI device to the application server and configure a file system with SMB sharing enabled
- **() Provision an Amazon FSx for Windows File Server file system. Mount the file system using the SMB protocol on the media servers** [CORRECT]
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/what-is.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- () https://docs.aws.amazon.com/storagegateway/latest/vgw/WhatIsStorageGateway.html
- () An IT company wants to optimize the costs incurred on its fleet of 100 Amazon EC2 instances for the next year. Based on historical analyses, the engineering team observed that 70 of these instances handle the compute services of its flagship application and need to be always available. The other 30 instances are used to handle batch jobs that can afford a delay in processing.

**Answer:**
Correct Answer: **Provision an Amazon FSx for Windows File Server file system. Mount the file system using the SMB protocol on the media servers**

---

## Question 165

**Q:** Which solution will best meet the requirements with the LEAST administrative overhead?

**Options:**
- (A) Use Amazon S3 with Transfer Acceleration enabled. Configure the application to upload and download files over HTTPS using signed URLs
- (B) Launch an Amazon EC2 Windows instance and manually configure a Windows file share. Use this instance to serve SMB access to application clients
- (C) Set up an AWS Storage Gateway Volume Gateway in cached volume mode. Attach the volume as an iSCSI device to the application server and configure a file system with SMB sharing enabled
- **(D) Provision an Amazon FSx for Windows File Server file system. Mount the file system using the SMB protocol on the media servers** [CORRECT]
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/fsx/latest/WindowsGuide/what-is.html
- (I) https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- (J) https://docs.aws.amazon.com/storagegateway/latest/vgw/WhatIsStorageGateway.html
- () An IT company wants to optimize the costs incurred on its fleet of 100 Amazon EC2 instances for the next year. Based on historical analyses, the engineering team observed that 70 of these instances handle the compute services of its flagship application and need to be always available. The other 30 instances are used to handle batch jobs that can afford a delay in processing.

**Answer:**
Correct Answer: **Provision an Amazon FSx for Windows File Server file system. Mount the file system using the SMB protocol on the media servers**

---

## Question 166

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-optimal solution?

**Options:**
- (A) Purchase 70 on-demand instances and 30 spot instances
- (B) Purchase 70 reserved instances (RIs) and 30 spot instances
- (C) Purchase 70 on-demand instances and 30 reserved instances
- (D) Purchase 70 reserved instances and 30 on-demand instances
- (E) Correct option:
- (F) As 70 instances need to be always available, these can be purchased as reserved instances for a one-year duration. The other 30 instances responsible for the batch job can be purchased as spot instances. Even if some of the spot instances are interrupted, other spot instances can continue with the job.
- (G) Please see this detailed overview of various types of Amazon EC2 instances from a pricing perspective:
- (H) via - https://aws.amazon.com/ec2/pricing/
- (I) Incorrect options:
- (J) Purchasing 70 on-demand instances would be costlier than 70 reserved instances, so these two options are ruled out.
- () Purchase 70 reserved instances and 30 on-demand instances - Purchasing 30 instances as on-demand instances to handle the batch jobs would not be cost-optimal as these instances don't need to be always available. Spot instances are better at handling such batch jobs. So this option is not correct.
- () Reference:
- () https://aws.amazon.com/ec2/pricing/
- () Amazon EC2 Auto Scaling needs to terminate an instance from Availability Zone (AZ) us-east-1a as it has the most number of instances amongst the Availability Zone (AZs) being used currently. There are 4 instances in the Availability Zone (AZ) us-east-1a like so: Instance A has the oldest launch template, Instance B has the oldest launch configuration, Instance C has the newest launch configuration and Instance D is closest to the next billing hour.
- () Which of the following instances would be terminated per the default termination policy?
- () Instance D
- () Instance B
- () Instance C
- () Instance A
- () Please see this note for a deep-dive on the default termination policy:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () These three options contradict the explanation provided above, so these options are incorrect.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () You would like to use AWS Snowball to move on-premises backups into a long term archival tier on AWS. Which solution provides the MOST cost savings?
- **() Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier Deep Archive on the same day** [CORRECT]
- () Create a AWS Snowball job and target an Amazon S3 Glacier Deep Archive Vault
- () Create an AWS Snowball job and target a Amazon S3 Glacier Vault
- () Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier on the same day
- () AWS Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 terabytes of usable HDD storage, 40 vCPUs, 1 terabyte of SATA SSD storage, and up to 40 gigabytes network connectivity to address large scale data transfer and pre-processing use cases.

**Answer:**
Correct Answer: **Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier Deep Archive on the same day**

---

## Question 167

**Q:** Which of the following instances would be terminated per the default termination policy?

**Options:**
- (A) Instance D
- (B) Instance B
- (C) Instance C
- (D) Instance A
- (E) Correct option:
- (F) Please see this note for a deep-dive on the default termination policy:
- (G) via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- (H) Incorrect options:
- (I) These three options contradict the explanation provided above, so these options are incorrect.
- (J) Reference:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () You would like to use AWS Snowball to move on-premises backups into a long term archival tier on AWS. Which solution provides the MOST cost savings?
- () Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier Deep Archive on the same day
- () Create a AWS Snowball job and target an Amazon S3 Glacier Deep Archive Vault
- () Create an AWS Snowball job and target a Amazon S3 Glacier Vault
- () Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier on the same day
- () AWS Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 terabytes of usable HDD storage, 40 vCPUs, 1 terabyte of SATA SSD storage, and up to 40 gigabytes network connectivity to address large scale data transfer and pre-processing use cases.
- () The original AWS Snowball devices were transitioned out of service and AWS Snowball Edge Storage Optimized are now the primary devices used for data transfer. You may see the AWS Snowball device on the exam, just remember that the original AWS Snowball device had 80 terabytes of storage space.
- () You can't move data directly from AWS Snowball into Amazon S3 Glacier, you need to go through Amazon S3 first, and then use a lifecycle policy. So this option is correct.
- () Amazon S3 Glacier and S3 Glacier Deep Archive are a secure, durable, and extremely low-cost Amazon S3 cloud storage classes for data archiving and long-term backup. They are designed to deliver 99.999999999% durability and provide comprehensive security and compliance capabilities that can help meet even the most stringent regulatory requirements. Finally, Amazon S3 Glacier Deep Archive provides more cost savings than Amazon S3 Glacier.
- () Both these options are incorrect as you can't move data directly from AWS Snowball into a Amazon S3 Glacier Vault or a Glacier Deep Archive Vault. You need to go through Amazon S3 first and then use a lifecycle policy.
- () Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier on the same day - As Amazon S3 Glacier Deep Archive provides more cost savings than Amazon S3 Glacier, you should use Amazon S3 Glacier Deep Archive for long term archival for this use-case.
- () References:
- () https://aws.amazon.com/snowball/features/
- () https://aws.amazon.com/glacier/
- () A health-care solutions company wants to run their applications on single-tenant hardware to meet regulatory guidelines.
- () Which of the following is the MOST cost-effective way of isolating their Amazon Elastic Compute Cloud (Amazon EC2)instances to a single tenant?
- () On-Demand Instances
- () Dedicated Hosts
- () Spot Instances
- **() Dedicated Instances** [CORRECT]

**Answer:**
Correct Answer: **Dedicated Instances**

---

## Question 168

**Q:** You would like to use AWS Snowball to move on-premises backups into a long term archival tier on AWS. Which solution provides the MOST cost savings?

**Options:**
- (A) Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier Deep Archive on the same day
- (B) Create a AWS Snowball job and target an Amazon S3 Glacier Deep Archive Vault
- (C) Create an AWS Snowball job and target a Amazon S3 Glacier Vault
- (D) Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier on the same day
- (E) Correct option:
- (F) AWS Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 terabytes of usable HDD storage, 40 vCPUs, 1 terabyte of SATA SSD storage, and up to 40 gigabytes network connectivity to address large scale data transfer and pre-processing use cases.
- (G) The original AWS Snowball devices were transitioned out of service and AWS Snowball Edge Storage Optimized are now the primary devices used for data transfer. You may see the AWS Snowball device on the exam, just remember that the original AWS Snowball device had 80 terabytes of storage space.
- (H) You can't move data directly from AWS Snowball into Amazon S3 Glacier, you need to go through Amazon S3 first, and then use a lifecycle policy. So this option is correct.
- (I) Incorrect options:
- (J) Amazon S3 Glacier and S3 Glacier Deep Archive are a secure, durable, and extremely low-cost Amazon S3 cloud storage classes for data archiving and long-term backup. They are designed to deliver 99.999999999% durability and provide comprehensive security and compliance capabilities that can help meet even the most stringent regulatory requirements. Finally, Amazon S3 Glacier Deep Archive provides more cost savings than Amazon S3 Glacier.
- () Both these options are incorrect as you can't move data directly from AWS Snowball into a Amazon S3 Glacier Vault or a Glacier Deep Archive Vault. You need to go through Amazon S3 first and then use a lifecycle policy.
- () Create an AWS Snowball job and target an Amazon S3 bucket. Create a lifecycle policy to transition this data to Amazon S3 Glacier on the same day - As Amazon S3 Glacier Deep Archive provides more cost savings than Amazon S3 Glacier, you should use Amazon S3 Glacier Deep Archive for long term archival for this use-case.
- () References:
- () https://aws.amazon.com/snowball/features/
- () https://aws.amazon.com/glacier/
- () A health-care solutions company wants to run their applications on single-tenant hardware to meet regulatory guidelines.
- () Which of the following is the MOST cost-effective way of isolating their Amazon Elastic Compute Cloud (Amazon EC2)instances to a single tenant?
- () On-Demand Instances
- () Dedicated Hosts
- () Spot Instances
- () Dedicated Instances
- () Dedicated Instances are Amazon EC2 instances that run in a virtual private cloud (VPC) on hardware that's dedicated to a single customer. Dedicated Instances that belong to different AWS accounts are physically isolated at a hardware level, even if those accounts are linked to a single-payer account. However, Dedicated Instances may share hardware with other instances from the same AWS account that are not Dedicated Instances.
- () A Dedicated Host is also a physical server that's dedicated for your use. With a Dedicated Host, you have visibility and control over how instances are placed on the server.
- () Differences between Dedicated Hosts and Dedicated Instances:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html#dedicated-hosts-dedicated-instances
- () Spot Instances - A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Your Spot Instance runs whenever capacity is available and the maximum price per hour for your request exceeds the Spot price. Any instance present with unused capacity will be allocated. Even though this is cost-effective, it does not fulfill the single-tenant hardware requirement of the client and hence is not the correct option.
- () Dedicated Hosts - An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your use. Dedicated Hosts allow you to use your existing software licenses on EC2 instances. With a Dedicated Host, you have visibility and control over how instances are placed on the server. This option is costlier than the Dedicated Instance and hence is not the right choice for the current requirement.
- () On-Demand Instances - With On-Demand Instances, you pay for compute capacity by the second with no long-term commitments. You have full control over its lifecycle—you decide when to launch, stop, hibernate, start, reboot, or terminate it. Hardware isolation is not possible and on-demand has one of the costliest instance charges and hence is not the correct answer for current requirements.
- () High Level Overview of Amazon EC2 Instance Purchase Options:
- () via - https://aws.amazon.com/ec2/pricing/
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-instance.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
- () Your company has a monthly big data workload, running for about 2 hours, which can be efficiently distributed across multiple servers of various sizes, with a variable number of CPUs. The solution for the workload should be able to withstand server failures.
- () Which is the MOST cost-optimal solution for this workload?
- **() Run the workload on a Spot Fleet** [CORRECT]

**Answer:**
Correct Answer: **Run the workload on a Spot Fleet**

---

## Question 169

**Q:** Which of the following is the MOST cost-effective way of isolating their Amazon Elastic Compute Cloud (Amazon EC2)instances to a single tenant?

**Options:**
- (A) On-Demand Instances
- (B) Dedicated Hosts
- (C) Spot Instances
- (D) Dedicated Instances
- (E) Correct option:
- (F) Dedicated Instances are Amazon EC2 instances that run in a virtual private cloud (VPC) on hardware that's dedicated to a single customer. Dedicated Instances that belong to different AWS accounts are physically isolated at a hardware level, even if those accounts are linked to a single-payer account. However, Dedicated Instances may share hardware with other instances from the same AWS account that are not Dedicated Instances.
- (G) A Dedicated Host is also a physical server that's dedicated for your use. With a Dedicated Host, you have visibility and control over how instances are placed on the server.
- (H) Differences between Dedicated Hosts and Dedicated Instances:
- (I) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html#dedicated-hosts-dedicated-instances
- (J) Incorrect options:
- () Spot Instances - A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Your Spot Instance runs whenever capacity is available and the maximum price per hour for your request exceeds the Spot price. Any instance present with unused capacity will be allocated. Even though this is cost-effective, it does not fulfill the single-tenant hardware requirement of the client and hence is not the correct option.
- () Dedicated Hosts - An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your use. Dedicated Hosts allow you to use your existing software licenses on EC2 instances. With a Dedicated Host, you have visibility and control over how instances are placed on the server. This option is costlier than the Dedicated Instance and hence is not the right choice for the current requirement.
- () On-Demand Instances - With On-Demand Instances, you pay for compute capacity by the second with no long-term commitments. You have full control over its lifecycle—you decide when to launch, stop, hibernate, start, reboot, or terminate it. Hardware isolation is not possible and on-demand has one of the costliest instance charges and hence is not the correct answer for current requirements.
- () High Level Overview of Amazon EC2 Instance Purchase Options:
- () via - https://aws.amazon.com/ec2/pricing/
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-instance.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
- () Your company has a monthly big data workload, running for about 2 hours, which can be efficiently distributed across multiple servers of various sizes, with a variable number of CPUs. The solution for the workload should be able to withstand server failures.
- () Which is the MOST cost-optimal solution for this workload?
- **() Run the workload on a Spot Fleet** [CORRECT]
- () Run the workload on Reserved Instances (RI)
- () Run the workload on Dedicated Hosts
- () Run the workload on Spot Instances
- () The Spot Fleet selects the Spot Instance pools that meet your needs and launches Spot Instances to meet the target capacity for the fleet. By default, Spot Fleets are set to maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated.
- () A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Spot Instances provide great cost efficiency, but we need to select an instance type in advance. In this case, we want to use the most cost-optimal option and leave the selection of the cheapest spot instance to a Spot Fleet request, which can be optimized with the lowestPrice strategy. So this is the correct option.
- () Key Spot Instance Concepts:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () Run the workload on Reserved Instances (RI) - Reserved Instances are less cost-optimized than Spot Instances, and most efficient when used continuously. Here the workload is once a month, so this is not efficient.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html#spot-fleet-allocation-strategy

**Answer:**
Correct Answer: **Run the workload on a Spot Fleet**

---

## Question 170

**Q:** Which is the MOST cost-optimal solution for this workload?

**Options:**
- **(A) Run the workload on a Spot Fleet** [CORRECT]
- (B) Run the workload on Reserved Instances (RI)
- (C) Run the workload on Dedicated Hosts
- (D) Run the workload on Spot Instances
- (E) Correct option:
- (F) The Spot Fleet selects the Spot Instance pools that meet your needs and launches Spot Instances to meet the target capacity for the fleet. By default, Spot Fleets are set to maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated.
- (G) A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Spot Instances provide great cost efficiency, but we need to select an instance type in advance. In this case, we want to use the most cost-optimal option and leave the selection of the cheapest spot instance to a Spot Fleet request, which can be optimized with the lowestPrice strategy. So this is the correct option.
- (H) Key Spot Instance Concepts:
- (I) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- (J) Incorrect options:
- () Run the workload on Reserved Instances (RI) - Reserved Instances are less cost-optimized than Spot Instances, and most efficient when used continuously. Here the workload is once a month, so this is not efficient.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html#spot-fleet-allocation-strategy

**Answer:**
Correct Answer: **Run the workload on a Spot Fleet**

---

## Question 171

**Q:** You have a team of developers in your company, and you would like to ensure they can quickly experiment with AWS Managed Policies by attaching them to their accounts, but you would like to prevent them from doing an escalation of privileges, by granting themselves the AdministratorAccess managed policy. How should you proceed?

**Options:**
- (A) For each developer, define an IAM permission boundary that will restrict the managed policies they can attach to themselves
- (B) Put the developers into an IAM group, and then define an IAM permission boundary on the group that will restrict the managed policies they can attach to themselves
- (C) Create a Service Control Policy (SCP) on your AWS account that restricts developers from attaching themselves the AdministratorAccess policy
- (D) Attach an IAM policy to your developers, that prevents them from attaching the AdministratorAccess policy
- (E) Correct option:
- (F) AWS supports permissions boundaries for IAM entities (users or roles). A permissions boundary is an advanced feature for using a managed policy to set the maximum permissions that an identity-based policy can grant to an IAM entity. An entity's permissions boundary allows it to perform only the actions that are allowed by both its identity-based policies and its permissions boundaries. Here we have to use an IAM permission boundary. They can only be applied to roles or users, not IAM groups.
- (G) Permissions boundaries for IAM entities:
- (H) via - https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
- (I) Incorrect options:
- (J) Attach an IAM policy to your developers, that prevents them from attaching the AdministratorAccess policy - This option is incorrect as the developers can remove this policy from themselves and escalate their privileges.
- () Put the developers into an IAM group, and then define an IAM permission boundary on the group that will restrict the managed policies they can attach to themselves - IAM permission boundary can only be applied to roles or users, not IAM groups. Hence this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scp.html
- () A financial services company wants to store confidential data in Amazon S3 and it needs to meet the following data security and compliance norms:
- () 1. Encryption key usage must be logged for auditing purposes
- () 2. Encryption Keys must be rotated every year
- () 3. The data must be encrypted at rest
- () Which is the MOST operationally efficient solution?
- () Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with manual key rotation
- () Server-side encryption (SSE-S3) with automatic key rotation
- () Server-side encryption with customer-provided keys (SSE-C) with automatic key rotation
- **() Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with automatic key rotation** [CORRECT]
- () Server-side encryption is the encryption of data at its destination by the application or service that receives it. Amazon S3 encrypts your data at the object level as it writes it to disks in its data centers and decrypts it for you when you access it.
- () Amazon S3 now applies server-side encryption with Amazon S3 managed keys (SSE-S3) as the base level of encryption for every bucket in Amazon S3. Starting January 5, 2023, all new object uploads to Amazon S3 are automatically encrypted at no additional cost and with no impact on performance.
- () Amazon S3 server-side encryption
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/serv-side-encryption.html
- () AWS KMS is a service that combines secure, highly available hardware and software to provide a key management system scaled for the cloud. Amazon S3 uses server-side encryption with AWS KMS (SSE-KMS) to encrypt your S3 object data. Also, when SSE-KMS is requested for the object, the S3 checksum as part of the object's metadata, is stored in encrypted form.
- () If you use KMS keys, you can use AWS KMS through the AWS Management Console or the AWS KMS API to do the following:
- () 1. Centrally create, view, edit, monitor, enable or disable, rotate, and schedule deletion of KMS keys.
- () 2. Define the policies that control how and by whom KMS keys can be used.
- () 3. Audit their usage to prove that they are being used correctly. Auditing is supported by the AWS KMS API, but not by the AWS KMSAWS Management Console.
- () When you enable automatic key rotation for a KMS key, AWS KMS generates new cryptographic material for the KMS key every year.
- () AWS KMS keys:
- () via - https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html
- () For the given use case, you can set up server-side encryption with AWS KMS Keys (SSE-KMS) with automatic key rotation.
- () Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with manual key rotation - Although it is possible to manually rotate the AWS KMS key, it is not the best fit solution as it is not operationally efficient.
- () Server-side encryption (SSE-S3) with automatic key rotation - When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key. As an additional safeguard, it encrypts the key itself with a root key that it regularly rotates. However, with SSE-S3, you cannot log the usage of the encryption key for auditing purposes. So this option is incorrect.
- () Server-side encryption with customer-provided keys (SSE-C) with automatic key rotation - It is possible to automatically rotate the customer-provided keys but you will need to develop the underlying solution to automate the key rotation. Therefore, this option is not operationally efficient.

**Answer:**
Correct Answer: **Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with automatic key rotation**

---

## Question 172

**Q:** Which is the MOST operationally efficient solution?

**Options:**
- (A) Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with manual key rotation
- (B) Server-side encryption (SSE-S3) with automatic key rotation
- (C) Server-side encryption with customer-provided keys (SSE-C) with automatic key rotation
- (D) Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with automatic key rotation
- (E) Correct option:
- (F) Server-side encryption is the encryption of data at its destination by the application or service that receives it. Amazon S3 encrypts your data at the object level as it writes it to disks in its data centers and decrypts it for you when you access it.
- (G) Amazon S3 now applies server-side encryption with Amazon S3 managed keys (SSE-S3) as the base level of encryption for every bucket in Amazon S3. Starting January 5, 2023, all new object uploads to Amazon S3 are automatically encrypted at no additional cost and with no impact on performance.
- (H) Amazon S3 server-side encryption
- (I) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/serv-side-encryption.html
- (J) AWS KMS is a service that combines secure, highly available hardware and software to provide a key management system scaled for the cloud. Amazon S3 uses server-side encryption with AWS KMS (SSE-KMS) to encrypt your S3 object data. Also, when SSE-KMS is requested for the object, the S3 checksum as part of the object's metadata, is stored in encrypted form.
- () If you use KMS keys, you can use AWS KMS through the AWS Management Console or the AWS KMS API to do the following:
- () 1. Centrally create, view, edit, monitor, enable or disable, rotate, and schedule deletion of KMS keys.
- () 2. Define the policies that control how and by whom KMS keys can be used.
- () 3. Audit their usage to prove that they are being used correctly. Auditing is supported by the AWS KMS API, but not by the AWS KMSAWS Management Console.
- () When you enable automatic key rotation for a KMS key, AWS KMS generates new cryptographic material for the KMS key every year.
- () AWS KMS keys:
- () via - https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html
- () For the given use case, you can set up server-side encryption with AWS KMS Keys (SSE-KMS) with automatic key rotation.
- () Incorrect options:
- () Server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS) with manual key rotation - Although it is possible to manually rotate the AWS KMS key, it is not the best fit solution as it is not operationally efficient.
- () Server-side encryption (SSE-S3) with automatic key rotation - When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key. As an additional safeguard, it encrypts the key itself with a root key that it regularly rotates. However, with SSE-S3, you cannot log the usage of the encryption key for auditing purposes. So this option is incorrect.
- () Server-side encryption with customer-provided keys (SSE-C) with automatic key rotation - It is possible to automatically rotate the customer-provided keys but you will need to develop the underlying solution to automate the key rotation. Therefore, this option is not operationally efficient.
- () References:
- () https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#master_keys
- () https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/serv-side-encryption.html
- () An enterprise organization is expanding its cloud footprint and needs to centralize its security event data from various AWS accounts and services. The goal is to evaluate security posture across all environments and improve threat detection and response — without requiring significant custom code or manual integration.
- () Which solution will fulfill these needs with the least development effort?
- () Set up a data lake using AWS Lake Formation to collect and organize security event logs. Use AWS Glue to perform ETL operations and standardize the log formats for centralized analysis
- **() Use Amazon Security Lake to create a centralized data lake that automatically collects security-related logs and events from AWS services and third-party sources. Store the data in an Amazon S3 bucket managed by Security Lake** [CORRECT]
- () Deploy a custom Lambda function to aggregate security logs from multiple AWS accounts. Format the data into CSV files and upload them to a central S3 bucket for analysis
- () Use Amazon Athena with predefined SQL queries to scan security logs stored in multiple S3 buckets. Visualize the findings by exporting results to an Amazon QuickSight dashboard
- () via - https://docs.aws.amazon.com/security-lake/latest/userguide/what-is-security-lake.html
- () https://docs.aws.amazon.com/security-lake/latest/userguide/what-is-security-lake.html
- () https://docs.aws.amazon.com/lake-formation/latest/dg/what-is-lake-formation.html

**Answer:**
Correct Answer: **Use Amazon Security Lake to create a centralized data lake that automatically collects security-related logs and events from AWS services and third-party sources. Store the data in an Amazon S3 bucket managed by Security Lake**

---

## Question 173

**Q:** Which solution will fulfill these needs with the least development effort?

**Options:**
- (A) Set up a data lake using AWS Lake Formation to collect and organize security event logs. Use AWS Glue to perform ETL operations and standardize the log formats for centralized analysis
- **(B) Use Amazon Security Lake to create a centralized data lake that automatically collects security-related logs and events from AWS services and third-party sources. Store the data in an Amazon S3 bucket managed by Security Lake** [CORRECT]
- (C) Deploy a custom Lambda function to aggregate security logs from multiple AWS accounts. Format the data into CSV files and upload them to a central S3 bucket for analysis
- (D) Use Amazon Athena with predefined SQL queries to scan security logs stored in multiple S3 buckets. Visualize the findings by exporting results to an Amazon QuickSight dashboard
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/security-lake/latest/userguide/what-is-security-lake.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/security-lake/latest/userguide/what-is-security-lake.html
- (J) https://docs.aws.amazon.com/lake-formation/latest/dg/what-is-lake-formation.html
- () A developer needs to implement an AWS Lambda function in AWS account A that accesses an Amazon Simple Storage Service (Amazon S3) bucket in AWS account B.

**Answer:**
Correct Answer: **Use Amazon Security Lake to create a centralized data lake that automatically collects security-related logs and events from AWS services and third-party sources. Store the data in an Amazon S3 bucket managed by Security Lake**

---

## Question 174

**Q:** As a Solutions Architect, which of the following will you recommend to meet this requirement?

**Options:**
- (A) AWS Lambda cannot access resources across AWS accounts. Use Identity federation to work around this limitation of Lambda
- (B) Create an IAM role for the AWS Lambda function that grants access to the Amazon S3 bucket. Set the IAM role as the Lambda function's execution role and that would give the AWS Lambda function cross-account access to the Amazon S3 bucket
- (C) The Amazon S3 bucket owner should make the bucket public so that it can be accessed by the AWS Lambda function in the other AWS account
- **(D) Create an IAM role for the AWS Lambda function that grants access to the Amazon S3 bucket. Set the IAM role as the AWS Lambda function's execution role. Make sure that the bucket policy also grants access to the AWS Lambda function's execution role** [CORRECT]
- (E) Correct option:
- (F) Complete list of steps to be followed:
- (G) via - https://aws.amazon.com/premiumsupport/knowledge-center/lambda-execution-role-s3-bucket/
- (H) Incorrect options:
- (I) AWS Lambda cannot access resources across AWS accounts. Use Identity federation to work around this limitation of Lambda - This is an incorrect statement, used only as a distractor.
- (J) The Amazon S3 bucket owner should make the bucket public so that it can be accessed by the AWS Lambda function in the other AWS account - Making the Amazon S3 bucket public for the given use-case will be considered as a security bad practice. It's usually done for very few use-cases such as hosting a website on Amazon S3. Therefore this option is incorrect.
- () Reference:
- () https://aws.amazon.com/premiumsupport/knowledge-center/lambda-execution-role-s3-bucket/
- () To improve the performance and security of the application, the engineering team at a company has created an Amazon CloudFront distribution with an Application Load Balancer as the custom origin. The team has also set up an AWS Web Application Firewall (AWS WAF) with Amazon CloudFront distribution. The security team at the company has noticed a surge in malicious attacks from a specific IP address to steal sensitive data stored on the Amazon EC2 instances.

**Answer:**
Correct Answer: **Create an IAM role for the AWS Lambda function that grants access to the Amazon S3 bucket. Set the IAM role as the AWS Lambda function's execution role. Make sure that the bucket policy also grants access to the AWS Lambda function's execution role**

---

## Question 175

**Q:** As a solutions architect, which of the following actions would you recommend to stop the attacks?

**Options:**
- (A) Create a deny rule for the malicious IP in the Security Groups associated with each of the instances
- **(B) Create an IP match condition in the AWS WAF to block the malicious IP address** [CORRECT]
- (C) Create a ticket with AWS support to take action against the malicious IP
- (D) Create a deny rule for the malicious IP in the network access control list (network ACL) associated with each of the instances
- (E) Correct option:
- (F) AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that block common attack patterns, such as SQL injection or cross-site scripting, and rules that filter out specific traffic patterns you define.
- (G) How AWS WAF Works:
- (H) via - https://aws.amazon.com/waf/
- (I) If you want to allow or block web requests based on the IP addresses that the requests originate from, create one or more IP match conditions. An IP match condition lists up to 10,000 IP addresses or IP address ranges that your requests originate from. So, this option is correct.
- (J) Incorrect options:
- () Create a deny rule for the malicious IP in the network access control list (network ACL) associated with each of the instances - Network access control list (network ACL) are not associated with instances. So this option is also ruled out.
- () Create a deny rule for the malicious IP in the Security Groups associated with each of the instances - You cannot deny rules in Security Groups. So this option is ruled out.
- () Create a ticket with AWS support to take action against the malicious IP - Managing the security of your application is your responsibility, not that of AWS, so you cannot raise a ticket for this issue.
- () Reference:
- () https://docs.aws.amazon.com/waf/latest/developerguide/classic-web-acl-ip-conditions.html
- () A social photo-sharing web application is hosted on Amazon Elastic Compute Cloud (Amazon EC2) instances behind an Elastic Load Balancer. The app gives the users the ability to upload their photos and also shows a leaderboard on the homepage of the app. The uploaded photos are stored in Amazon Simple Storage Service (Amazon S3) and the leaderboard data is maintained in Amazon DynamoDB. The Amazon EC2 instances need to access both Amazon S3 and Amazon DynamoDB for these features.

**Answer:**
Correct Answer: **Create an IP match condition in the AWS WAF to block the malicious IP address**

---

## Question 176

**Q:** As a solutions architect, which of the following solutions would you recommend as the MOST secure option?

**Options:**
- (A) Save the AWS credentials (access key Id and secret access token) in a configuration file within the application code on the Amazon EC2 instances. Amazon EC2 instances can use these credentials to access Amazon S3 and Amazon DynamoDB
- (B) Attach the appropriate IAM role to the Amazon EC2 instance profile so that the instance can access Amazon S3 and Amazon DynamoDB
- (C) Configure AWS CLI on the Amazon EC2 instances using a valid IAM user's credentials. The application code can then invoke shell scripts to access Amazon S3 and Amazon DynamoDB via AWS CLI
- (D) Encrypt the AWS credentials via a custom encryption library and save it in a secret directory on the Amazon EC2 instances. The application code can then safely decrypt the AWS credentials to make the API calls to Amazon S3 and Amazon DynamoDB
- (E) Correct option:
- (F) Applications that run on an Amazon EC2 instance must include AWS credentials in their AWS API requests. You could have your developers store AWS credentials directly within the Amazon EC2 instance and allow applications in that instance to use those credentials. But developers would then have to manage the credentials and ensure that they securely pass the credentials to each instance and update each Amazon EC2 instance when it's time to rotate the credentials.
- (G) via - https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html
- (H) Incorrect options:
- (I) Keeping the AWS credentials (encrypted or plain text) on the Amazon EC2 instance is a bad security practice, therefore these three options using the AWS credentials are incorrect.
- (J) Reference:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html
- () What does this IAM policy do?
- () : [
- ()       ],
- () : {
- **() It allows starting an Amazon EC2 instance only when the IP where the call originates is within the 34.50.31.0/24 CIDR block** [CORRECT]
- () It allows starting an Amazon EC2 instance only when they have a Public IP within the 34.50.31.0/24 CIDR block
- () It allows starting an Amazon EC2 instance only when they have a Private IP within the 34.50.31.0/24 CIDR block
- () It allows starting an Amazon EC2 instance only when they have an Elastic IP within the 34.50.31.0/24 CIDR block
- () Consider the following snippet from the given policy document:
- () The aws:SourceIP in this condition always represents the IP of the caller of the API. That is very helpful if you want to restrict access to certain AWS API for example from the public IP of your on-premises infrastructure.
- () Please see this overview of Elastic vs Public vs Private IP addresses:

**Answer:**
Correct Answer: **It allows starting an Amazon EC2 instance only when the IP where the call originates is within the 34.50.31.0/24 CIDR block**

---

## Question 177

**Q:** Which of the following is the MOST optimal solution to make sure that users can view all the uploaded videos? (Select two)

**Options:**
- (A) Correct selection
- (B) Write a one time job to copy the videos from all Amazon EBS volumes to Amazon S3 and then modify the application to use Amazon S3 standard for storing the videos
- (C) Write a one time job to copy the videos from all Amazon EBS volumes to Amazon RDS and then modify the application to use Amazon RDS for storing the videos
- (D) Write a one time job to copy the videos from all Amazon EBS volumes to Amazon DynamoDB and then modify the application to use Amazon DynamoDB for storing the videos
- (E) Write a one time job to copy the videos from all Amazon EBS volumes to Amazon S3 Glacier Deep Archive and then modify the application to use Amazon S3 Glacier Deep Archive for storing the videos
- (F) Mount Amazon Elastic File System (Amazon EFS) on all Amazon EC2 instances. Write a one time job to copy the videos from all Amazon EBS volumes to Amazon EFS. Modify the application to use Amazon EFS for storing the videos
- (G) Correct options:
- (H) Amazon Elastic Block Store (EBS) is an easy to use, high-performance block storage service designed for use with Amazon Elastic Compute Cloud (EC2) for both throughput and transaction-intensive workloads at any scale.
- (I) Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources. It is built to scale on-demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, eliminating the need to provision and manage capacity to accommodate growth.
- (J) Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.
- () As Amazon EBS volumes are attached locally to the Amazon EC2 instances, therefore the uploaded videos are tied to specific Amazon EC2 instances. Every time the user logs in, they are directed to a different instance and therefore their videos get dispersed across multiple EBS volumes. The correct solution is to use either Amazon S3 or Amazon EFS to store the user videos.
- () Incorrect options:
- () Write a one time job to copy the videos from all Amazon EBS volumes to Amazon S3 Glacier Deep Archive and then modify the application to use Amazon S3 Glacier Deep Archive for storing the videos - Amazon S3 Glacier Deep Archive is meant to be used for long term data archival. It cannot be used to serve static content such as videos or images via a web application. So this option is incorrect.
- () Write a one time job to copy the videos from all Amazon EBS volumes to Amazon RDS and then modify the application to use Amazon RDS for storing the videos - Amazon RDS is a relational database and not the right candidate for storing videos.
- () Write a one time job to copy the videos from all Amazon EBS volumes to Amazon DynamoDB and then modify the application to use Amazon DynamoDB for storing the videos - Amazon DynamoDB is a NoSQL database and not the right candidate for storing videos.
- () Reference:
- () https://aws.amazon.com/ebs/
- () An IT company has an Access Control Management (ACM) application that uses Amazon RDS for MySQL but is running into performance issues despite using Read Replicas. The company has hired you as a solutions architect to address these performance-related challenges without moving away from the underlying relational database schema. The company has branch offices across the world, and it needs the solution to work on a global scale.
- () Which of the following will you recommend as the MOST cost-effective and high-performance solution?
- **() Use Amazon Aurora Global Database to enable fast local reads with low latency in each region** [CORRECT]
- () Spin up a Amazon Redshift cluster in each AWS region. Migrate the existing data into Redshift clusters
- () Use Amazon DynamoDB Global Tables to provide fast, local, read and write performance in each region
- () Spin up Amazon EC2 instances in each AWS region, install MySQL databases and migrate the existing data into these new databases
- () Correct option:
- () Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 64TB per database instance. Aurora is not an in-memory database.
- () Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each region, and provides disaster recovery from region-wide outages. Amazon Aurora Global Database is the correct choice for the given use-case.
- () Amazon Aurora Global Database Features:
- () via - https://aws.amazon.com/rds/aurora/global-database/
- () Use Amazon DynamoDB Global Tables to provide fast, local, read and write performance in each region - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.
- () Global Tables builds upon DynamoDB’s global footprint to provide you with a fully managed, multi-region, and multi-master database that provides fast, local, read, and write performance for massively scaled, global applications. Global Tables replicates your Amazon DynamoDB tables automatically across your choice of AWS regions. Given that the use-case wants you to continue with the underlying schema of the relational database, DynamoDB is not the right choice as it's a NoSQL database.
- () Amazon DynamoDB Global Tables Overview:
- () via - https://aws.amazon.com/dynamodb/global-tables/
- () Spin up a Amazon Redshift cluster in each AWS region. Migrate the existing data into Redshift clusters - Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis. Amazon Redshift is not suited to be used as a transactional relational database, so this option is not correct.
- () Spin up Amazon EC2 instances in each AWS region, install MySQL databases and migrate the existing data into these new databases - Setting up Amazon EC2 instances in multiple regions with manually managed MySQL databases represents a maintenance nightmare and is not the correct choice for this use-case.
- () References:
- () https://aws.amazon.com/rds/aurora/global-database/
- () https://aws.amazon.com/dynamodb/global-tables/
- () An enterprise is building a secure business intelligence API using Amazon API Gateway to serve internal users with confidential analytics data. The API must be accessible only from a set of trusted IP addresses that are part of the organization's internal network ranges. No external IP traffic should be able to invoke the API. A solutions architect must design this access control mechanism with the least operational complexity.
- () What should the architect do to meet these requirements?
- () Deploy the API Gateway resource to an on-premises server using AWS Outposts. Apply host-based firewall rules to filter allowed IPs
- () Modify the security group that is attached to API Gateway to allow only traffic from specific IP addresses

**Answer:**
Correct Answer: **Use Amazon Aurora Global Database to enable fast local reads with low latency in each region**

---

## Question 178

**Q:** Which of the following will you recommend as the MOST cost-effective and high-performance solution?

**Options:**
- (A) Use Amazon Aurora Global Database to enable fast local reads with low latency in each region
- (B) Spin up a Amazon Redshift cluster in each AWS region. Migrate the existing data into Redshift clusters
- (C) Use Amazon DynamoDB Global Tables to provide fast, local, read and write performance in each region
- (D) Spin up Amazon EC2 instances in each AWS region, install MySQL databases and migrate the existing data into these new databases
- (E) Correct option:
- (F) Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 64TB per database instance. Aurora is not an in-memory database.
- (G) Amazon Aurora Global Database is designed for globally distributed applications, allowing a single Amazon Aurora database to span multiple AWS regions. It replicates your data with no impact on database performance, enables fast local reads with low latency in each region, and provides disaster recovery from region-wide outages. Amazon Aurora Global Database is the correct choice for the given use-case.
- (H) Amazon Aurora Global Database Features:
- (I) via - https://aws.amazon.com/rds/aurora/global-database/
- (J) Incorrect options:
- () Use Amazon DynamoDB Global Tables to provide fast, local, read and write performance in each region - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.
- () Global Tables builds upon DynamoDB’s global footprint to provide you with a fully managed, multi-region, and multi-master database that provides fast, local, read, and write performance for massively scaled, global applications. Global Tables replicates your Amazon DynamoDB tables automatically across your choice of AWS regions. Given that the use-case wants you to continue with the underlying schema of the relational database, DynamoDB is not the right choice as it's a NoSQL database.
- () Amazon DynamoDB Global Tables Overview:
- () via - https://aws.amazon.com/dynamodb/global-tables/
- () Spin up a Amazon Redshift cluster in each AWS region. Migrate the existing data into Redshift clusters - Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis. Amazon Redshift is not suited to be used as a transactional relational database, so this option is not correct.
- () Spin up Amazon EC2 instances in each AWS region, install MySQL databases and migrate the existing data into these new databases - Setting up Amazon EC2 instances in multiple regions with manually managed MySQL databases represents a maintenance nightmare and is not the correct choice for this use-case.
- () References:
- () https://aws.amazon.com/rds/aurora/global-database/
- () https://aws.amazon.com/dynamodb/global-tables/
- () An enterprise is building a secure business intelligence API using Amazon API Gateway to serve internal users with confidential analytics data. The API must be accessible only from a set of trusted IP addresses that are part of the organization's internal network ranges. No external IP traffic should be able to invoke the API. A solutions architect must design this access control mechanism with the least operational complexity.
- () What should the architect do to meet these requirements?
- () Deploy the API Gateway resource to an on-premises server using AWS Outposts. Apply host-based firewall rules to filter allowed IPs
- () Modify the security group that is attached to API Gateway to allow only traffic from specific IP addresses
- () Deploy the API Gateway as a regional API in a public subnet and associate the subnet with a security group that permits inbound traffic only from trusted IP ranges
- **() Create a resource policy for the API Gateway API that explicitly denies access to all IP addresses except those listed in an allow list** [CORRECT]
- () Modify the security group that is attached to API Gateway to allow only traffic from specific IP addresses - API Gateway does not use security groups because it is a managed service that is not deployed into a VPC by default. Security groups apply to resources like EC2 instances, RDS databases, or Lambda functions within a VPC. Therefore, this option is not valid for controlling inbound access to an API Gateway endpoint.
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-resource-policies.html
- () https://docs.aws.amazon.com/outposts/latest/userguide/what-is-outposts.html

**Answer:**
Correct Answer: **Create a resource policy for the API Gateway API that explicitly denies access to all IP addresses except those listed in an allow list**

---

## Question 179

**Q:** What should the architect do to meet these requirements?

**Options:**
- (A) Deploy the API Gateway resource to an on-premises server using AWS Outposts. Apply host-based firewall rules to filter allowed IPs
- (B) Modify the security group that is attached to API Gateway to allow only traffic from specific IP addresses
- (C) Deploy the API Gateway as a regional API in a public subnet and associate the subnet with a security group that permits inbound traffic only from trusted IP ranges
- (D) Create a resource policy for the API Gateway API that explicitly denies access to all IP addresses except those listed in an allow list
- (E) Correct option:
- (F) Incorrect options:
- (G) Modify the security group that is attached to API Gateway to allow only traffic from specific IP addresses - API Gateway does not use security groups because it is a managed service that is not deployed into a VPC by default. Security groups apply to resources like EC2 instances, RDS databases, or Lambda functions within a VPC. Therefore, this option is not valid for controlling inbound access to an API Gateway endpoint.
- (H) References:
- (I) https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-resource-policies.html
- (J) https://docs.aws.amazon.com/outposts/latest/userguide/what-is-outposts.html
- () Dump12
- () A media streaming startup is building a set of backend APIs that will be consumed by external mobile applications. To prevent API abuse, protect downstream resources, and ensure fair usage across clients, the architecture must enforce rate limiting and throttling on a per-client basis. The team also wants to define usage quotas and apply different limits to different API consumers.
- () Which solution should the team implement to enforce rate limiting and usage quotas at the API layer?
- () Use a Gateway Load Balancer to inspect and control incoming HTTP traffic and throttle requests by integrating with third-party firewall appliances
- **() Use Amazon API Gateway and configure usage plans with API keys to apply rate limits and quotas per client** [CORRECT]
- () Use a Network Load Balancer (NLB) to terminate TLS and apply rate-limiting logic within backend EC2 instances
- () Use an Application Load Balancer (ALB) with path-based routing and configure listener rules to enforce request limits

**Answer:**
Correct Answer: **Use Amazon API Gateway and configure usage plans with API keys to apply rate limits and quotas per client**

---

## Question 180

**Q:** Which solution should the team implement to enforce rate limiting and usage quotas at the API layer?

**Options:**
- (A) Use a Gateway Load Balancer to inspect and control incoming HTTP traffic and throttle requests by integrating with third-party firewall appliances
- **(B) Use Amazon API Gateway and configure usage plans with API keys to apply rate limits and quotas per client** [CORRECT]
- (C) Use a Network Load Balancer (NLB) to terminate TLS and apply rate-limiting logic within backend EC2 instances
- (D) Use an Application Load Balancer (ALB) with path-based routing and configure listener rules to enforce request limits
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-api-usage-plans.html
- (I) https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- (J) https://docs.aws.amazon.com/elasticloadbalancing/latest/gateway/introduction.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () A financial services company is migrating their messaging queues from self-managed message-oriented middleware systems to Amazon Simple Queue Service (Amazon SQS). The development team at the company wants to minimize the costs of using Amazon SQS.

**Answer:**
Correct Answer: **Use Amazon API Gateway and configure usage plans with API keys to apply rate limits and quotas per client**

---

## Question 181

**Q:** As a solutions architect, which of the following options would you recommend for the given use-case?

**Options:**
- (A) Use SQS message timer to retrieve messages from your Amazon SQS queues
- (B) Use SQS visibility timeout to retrieve messages from your Amazon SQS queues
- (C) Use SQS short polling to retrieve messages from your Amazon SQS queues
- (D) Use SQS long polling to retrieve messages from your Amazon SQS queues
- (E) Correct option:
- (F) Amazon Simple Queue Service (Amazon SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.
- (G) Amazon SQS provides short polling and long polling to receive messages from a queue. By default, queues use short polling. With short polling, Amazon SQS sends the response right away, even if the query found no messages. With long polling, Amazon SQS sends a response after it collects at least one available message, up to the maximum number of messages specified in the request. Amazon SQS sends an empty response only if the polling wait time expires.
- (H) Long polling makes it inexpensive to retrieve messages from your Amazon SQS queue as soon as the messages are available. Using long polling can reduce the cost of using SQS because you can reduce the number of empty receives.
- (I) Short Polling vs Long Polling:
- (J) via - https://aws.amazon.com/sqs/faqs/
- () Incorrect options:
- () Use SQS short polling to retrieve messages from your Amazon SQS queues - With short polling, Amazon SQS sends the response right away, even if the query found no messages. You end up paying more because of the increased number of empty receives.
- () Use SQS visibility timeout to retrieve messages from your Amazon SQS queues - Visibility timeout is a period during which Amazon SQS prevents other consumers from receiving and processing a given message. The default visibility timeout for a message is 30 seconds. The minimum is 0 seconds. The maximum is 12 hours. You cannot use visibility timeout to retrieve messages from your Amazon SQS queues. This option has been added as a distractor.
- () References:
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-short-and-long-polling.html
- () https://aws.amazon.com/sqs/faqs/
- () A company has hired you as an AWS Certified Solutions Architect – Associate to help with redesigning a real-time data processor. The company wants to build custom applications that process and analyze the streaming data for its specialized needs.
- () Which solution will you recommend to address this use-case?
- **() Use Amazon Kinesis Data Streams to process the data streams as well as decouple the producers and consumers for the real-time data processor** [CORRECT]
- () Use Amazon Kinesis Data Firehose to process the data streams as well as decouple the producers and consumers for the real-time data processor
- () Use Amazon Simple Queue Service (Amazon SQS) to process the data streams as well as decouple the producers and consumers for the real-time data processor
- () Use Amazon Simple Notification Service (Amazon SNS) to process the data streams as well as decouple the producers and consumers for the real-time data processor
- () Kinesis Data Streams Overview:
- () via - https://aws.amazon.com/kinesis/data-streams/
- () Use Amazon Simple Queue Service (Amazon SQS) to process the data streams as well as decouple the producers and consumers for the real-time data processor - Amazon Simple Queue Service (Amazon SQS) offers a secure, durable, and available hosted queue that lets you integrate and decouple distributed software systems and components. SQS cannot be used to decouple the producers and consumers for the real-time data processor as described in the given use-case.
- () Amazon Kinesis Data Firehose Overview
- () via - https://aws.amazon.com/kinesis/data-firehose/
- () https://aws.amazon.com/kinesis/data-streams/
- () https://aws.amazon.com/kinesis/data-firehose/
- () The DevOps team at an IT company has created a custom VPC (V1) and attached an Internet Gateway (I1) to the VPC. The team has also created a subnet (S1) in this custom VPC and added a route to this subnet's route table (R1) that directs internet-bound traffic to the Internet Gateway. Now the team launches an Amazon EC2 instance (E1) in the subnet S1 and assigns a public IPv4 address to this instance. Next the team also launches a Network Address Translation (NAT) instance (N1) in the subnet S1.

**Answer:**
Correct Answer: **Use Amazon Kinesis Data Streams to process the data streams as well as decouple the producers and consumers for the real-time data processor**

---

## Question 182

**Q:** Which solution will you recommend to address this use-case?

**Options:**
- **(A) Use Amazon Kinesis Data Streams to process the data streams as well as decouple the producers and consumers for the real-time data processor** [CORRECT]
- (B) Use Amazon Kinesis Data Firehose to process the data streams as well as decouple the producers and consumers for the real-time data processor
- (C) Use Amazon Simple Queue Service (Amazon SQS) to process the data streams as well as decouple the producers and consumers for the real-time data processor
- (D) Use Amazon Simple Notification Service (Amazon SNS) to process the data streams as well as decouple the producers and consumers for the real-time data processor
- (E) Correct option:
- (F) Kinesis Data Streams Overview:
- (G) via - https://aws.amazon.com/kinesis/data-streams/
- (H) Incorrect options:
- (I) Use Amazon Simple Queue Service (Amazon SQS) to process the data streams as well as decouple the producers and consumers for the real-time data processor - Amazon Simple Queue Service (Amazon SQS) offers a secure, durable, and available hosted queue that lets you integrate and decouple distributed software systems and components. SQS cannot be used to decouple the producers and consumers for the real-time data processor as described in the given use-case.
- (J) Amazon Kinesis Data Firehose Overview
- () via - https://aws.amazon.com/kinesis/data-firehose/
- () References:
- () https://aws.amazon.com/kinesis/data-streams/
- () https://aws.amazon.com/kinesis/data-firehose/
- () The DevOps team at an IT company has created a custom VPC (V1) and attached an Internet Gateway (I1) to the VPC. The team has also created a subnet (S1) in this custom VPC and added a route to this subnet's route table (R1) that directs internet-bound traffic to the Internet Gateway. Now the team launches an Amazon EC2 instance (E1) in the subnet S1 and assigns a public IPv4 address to this instance. Next the team also launches a Network Address Translation (NAT) instance (N1) in the subnet S1.

**Answer:**
Correct Answer: **Use Amazon Kinesis Data Streams to process the data streams as well as decouple the producers and consumers for the real-time data processor**

---

## Question 183

**Q:** Under the given infrastructure setup, which of the following entities is doing the Network Address Translation for the Amazon EC2 instance E1?

**Options:**
- (A) Subnet (S1)
- (B) Network Address Translation (NAT) instance (N1)
- **(C) Internet Gateway (I1)** [CORRECT]
- (D) Route Table (R1)
- (E) Correct option:
- (F) An Internet Gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between your VPC and the internet.
- (G) An Internet Gateway serves two purposes: to provide a target in your VPC route tables for internet-routable traffic and to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses. Therefore, for instance E1, the Network Address Translation is done by Internet Gateway I1.
- (H) Additionally, an Internet Gateway supports IPv4 and IPv6 traffic. It does not cause availability risks or bandwidth constraints on your network traffic.
- (I) To enable access to or from the internet for instances in a subnet in a VPC, you must do the following:
- (J) Attach an Internet gateway to your VPC.
- () Add a route to your subnet's route table that directs internet-bound traffic to the internet gateway. If a subnet is associated with a route table that has a route to an internet gateway, it's known as a public subnet. If a subnet is associated with a route table that does not have a route to an internet gateway, it's known as a private subnet.
- () Ensure that instances in your subnet have a globally unique IP address (public IPv4 address, Elastic IP address, or IPv6 address).
- () Ensure that your network access control lists and security group rules allow the relevant traffic to flow to and from your instance.
- () Internet Gateway Overview:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html
- () Incorrect options:
- () Network Address Translation (NAT) instance (N1) - You can use a network address translation (NAT) instance in a public subnet in your VPC to enable instances in the private subnet to initiate outbound IPv4 traffic to the Internet or other AWS services, but prevent the instances from receiving inbound traffic initiated by someone on the Internet. As the instance E1 is in a public subnet, therefore this option is not correct.
- () A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. A subnet is a range of IP addresses in your VPC. A route table contains a set of rules, called routes, that are used to determine where network traffic is directed. Therefore neither Subnet nor Route Table can be used for Network Address Translation.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html
- () An engineering team wants to orchestrate multiple Amazon ECS task types running on Amazon EC2 instances that are part of the Amazon ECS cluster. The output and state data for all tasks need to be stored. The amount of data output by each task is approximately 20 megabytes and there could be hundreds of tasks running at a time. As old outputs are archived, the storage size is not expected to exceed 1 terabyte.

**Answer:**
Correct Answer: **Internet Gateway (I1)**

---

## Question 184

**Q:** As a solutions architect, which of the following would you recommend as an optimized solution for high-frequency reading and writing?

**Options:**
- (A) Use Amazon EFS with Bursting Throughput mode
- (B) Use Amazon DynamoDB table that is accessible by all ECS cluster instances
- (C) Use an Amazon EBS volume mounted to the Amazon ECS cluster instances
- **(D) Use Amazon EFS with Provisioned Throughput mode** [CORRECT]
- (E) Correct option:
- (F) Amazon EFS file systems are distributed across an unconstrained number of storage servers. This distributed data storage design enables file systems to grow elastically to petabyte scale. It also enables massively parallel access from compute instances, including Amazon EC2, Amazon ECS, and AWS Lambda, to your data.
- (G) If your file system is in the Provisioned Throughput mode, you can increase the Provisioned Throughput of your file system as often as you want. You can decrease your file system throughput in Provisioned Throughput mode as long as it's been more than 24 hours since the last decrease. Additionally, you can change between Provisioned Throughput mode and the default Bursting Throughput mode as long as it’s been more than 24 hours since the last throughput mode change.
- (H) via - https://docs.aws.amazon.com/efs/latest/ug/performance.html
- (I) Incorrect options:
- (J) The use-case mentions that the solution should be optimized for high-frequency reading and writing even when the old outputs are archived, therefore Provisioned Throughput mode is a better fit as it guarantees high levels of throughput your applications require without having to pad your file system.
- () Use an Amazon EBS volume mounted to the Amazon ECS cluster instances - Amazon EFS has a higher throughput than Amazon EBS. In addition, Amazon EBS can be attached to multiple Amazon EC2 instances when the underlying EBS type is io1/io2 and the instance is of Nitro type. The use-case does not provide any such details, so this option is ruled out.
- () Use Amazon DynamoDB table that is accessible by all ECS cluster instances - Amazon DynamoDB is not a fit for this scenario as each task output is 20 MB but the storage limit for each item in a Amazon DynamoDB table is 400 KB. You could write custom code to split the task output data into multiple items but it is not an optimal solution compared to using Amazon EFS in Provisioned Throughput mode.
- () References:
- () https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Limits.html#limits-items
- () A company has a license-based, expensive, legacy commercial database solution deployed at its on-premises data center. The company wants to migrate this database to a more efficient, open-source, and cost-effective option on AWS Cloud. The CTO at the company wants a solution that can handle complex database configurations such as secondary indexes, foreign keys, and stored procedures.
- () As a solutions architect, which of the following AWS services should be combined to handle this use-case? (Select two)
- () Correct selection
- () AWS Database Migration Service (AWS DMS)
- () AWS Glue
- () Basic Schema Copy
- () AWS Snowball Edge
- () AWS Schema Conversion Tool (AWS SCT)
- () Correct options:
- () AWS Database Migration Service helps you migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database. AWS Database Migration Service supports homogeneous migrations such as Oracle to Oracle, as well as heterogeneous migrations between different database platforms, such as Oracle or Microsoft SQL Server to Amazon Aurora.
- () Given the use-case where the CTO at the company wants to move away from license-based, expensive, legacy commercial database solutions deployed at the on-premises data center to more efficient, open-source, and cost-effective options on AWS Cloud, this is an example of heterogeneous database migrations.
- () For such a scenario, the source and target databases engines are different, like in the case of Oracle to Amazon Aurora, Oracle to PostgreSQL, or Microsoft SQL Server to MySQL migrations. In this case, the schema structure, data types, and database code of source and target databases can be quite different, requiring a schema and code transformation before the data migration starts.
- () Heterogeneous Database Migrations:
- () via - https://aws.amazon.com/dms/
- () AWS Glue - AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics. AWS Glue job is meant to be used for batch ETL data processing. Therefore, it cannot be used for database migrations.
- () https://aws.amazon.com/dms/
- () https://aws.amazon.com/dms/faqs/
- () https://aws.amazon.com/dms/schema-conversion-tool/
- () A company has a hybrid cloud structure for its on-premises data center and AWS Cloud infrastructure. The company wants to build a web log archival solution such that only the most frequently accessed logs are available as cached data locally while backing up all logs on Amazon S3.

**Answer:**
Correct Answer: **Use Amazon EFS with Provisioned Throughput mode**

---

## Question 185

**Q:** As a solutions architect, which of the following AWS services should be combined to handle this use-case? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) AWS Database Migration Service (AWS DMS)
- (C) AWS Glue
- (D) Basic Schema Copy
- (E) AWS Snowball Edge
- (F) AWS Schema Conversion Tool (AWS SCT)
- (G) Correct options:
- (H) AWS Database Migration Service helps you migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database. AWS Database Migration Service supports homogeneous migrations such as Oracle to Oracle, as well as heterogeneous migrations between different database platforms, such as Oracle or Microsoft SQL Server to Amazon Aurora.
- (I) Given the use-case where the CTO at the company wants to move away from license-based, expensive, legacy commercial database solutions deployed at the on-premises data center to more efficient, open-source, and cost-effective options on AWS Cloud, this is an example of heterogeneous database migrations.
- (J) For such a scenario, the source and target databases engines are different, like in the case of Oracle to Amazon Aurora, Oracle to PostgreSQL, or Microsoft SQL Server to MySQL migrations. In this case, the schema structure, data types, and database code of source and target databases can be quite different, requiring a schema and code transformation before the data migration starts.
- () Heterogeneous Database Migrations:
- () via - https://aws.amazon.com/dms/
- () Incorrect options:
- () AWS Glue - AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics. AWS Glue job is meant to be used for batch ETL data processing. Therefore, it cannot be used for database migrations.
- () References:
- () https://aws.amazon.com/dms/
- () https://aws.amazon.com/dms/faqs/
- () https://aws.amazon.com/dms/schema-conversion-tool/
- () A company has a hybrid cloud structure for its on-premises data center and AWS Cloud infrastructure. The company wants to build a web log archival solution such that only the most frequently accessed logs are available as cached data locally while backing up all logs on Amazon S3.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 186

**Q:** As a solutions architect, which of the following statements would you identify as CORRECT regarding this automatic recovery process? (Select two)

**Options:**
- **(A) Terminated Amazon EC2 instances can be recovered if they are configured at the launch of instance** [CORRECT]
- (B) If your instance has a public IPv4 address, it does not retain the public IPv4 address after recovery
- (C) Correct selection
- (D) If your instance has a public IPv4 address, it retains the public IPv4 address after recovery
- (E) During instance recovery, the instance is migrated during an instance reboot, and any data that is in-memory is retained
- (F) A recovered instance is identical to the original instance, including the instance ID, private IP addresses, Elastic IP addresses, and all instance metadata
- (G) Correct options:
- (H) Incorrect options:
- (I) Terminated Amazon EC2 instances can be recovered if they are configured at the launch of instance - This is incorrect as terminated instances cannot be recovered.
- (J) During instance recovery, the instance is migrated during an instance reboot, and any data that is in-memory is retained - As mentioned above, during instance recovery, the instance is migrated during an instance reboot, and any data that is in-memory is lost.
- () If your instance has a public IPv4 address, it does not retain the public IPv4 address after recovery - As mentioned above, if your instance has a public IPv4 address, it retains the public IPv4 address after recovery.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-recover.html
- () The engineering team at a company wants to use Amazon Simple Queue Service (Amazon SQS) to decouple components of the underlying application architecture. However, the team is concerned about the VPC-bound components accessing Amazon Simple Queue Service (Amazon SQS) over the public internet.

**Answer:**
Correct Answer: **Terminated Amazon EC2 instances can be recovered if they are configured at the launch of instance**

---

## Question 187

**Q:** As a solutions architect, which of the following solutions would you recommend to address this use-case?

**Options:**
- (A) Use Network Address Translation (NAT) instance to access Amazon SQS
- **(B) Use VPC endpoint to access Amazon SQS** [CORRECT]
- (C) Use Internet Gateway to access Amazon SQS
- (D) Use VPN connection to access Amazon SQS
- (E) Correct option:
- (F) AWS customers can access Amazon Simple Queue Service (Amazon SQS) from their Amazon Virtual Private Cloud (Amazon VPC) using VPC endpoints, without using public IPs, and without needing to traverse the public internet. VPC endpoints for Amazon SQS are powered by AWS PrivateLink, a highly available, scalable technology that enables you to privately connect your VPC to supported AWS services.
- (G) Amazon VPC endpoints are easy to configure. They also provide reliable connectivity to Amazon SQS without requiring an internet gateway, Network Address Translation (NAT) instance, VPN connection, or AWS Direct Connect connection. With VPC endpoints, the data between your Amazon VPC and Amazon SQS queue is transferred within the Amazon network, helping protect your instances from internet traffic.
- (H) AWS PrivateLink simplifies the security of data shared with cloud-based applications by eliminating the exposure of data to the public Internet. AWS PrivateLink provides private connectivity between VPCs, AWS services, and on-premises applications, securely on the Amazon network. AWS PrivateLink makes it easy to connect services across different accounts and VPCs to significantly simplify the network architecture.
- (I) Incorrect options:
- (J) Use Internet Gateway to access Amazon SQS - An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It, therefore, imposes no availability risks or bandwidth constraints on your network traffic. This option is ruled out as the team does not want to use the public internet to access Amazon SQS.
- () References:
- () https://aws.amazon.com/privatelink/
- () https://aws.amazon.com/about-aws/whats-new/2018/12/amazon-sqs-vpc-endpoints-aws-privatelink/
- () A retail company has connected its on-premises data center to the AWS Cloud via AWS Direct Connect. The company wants to be able to resolve Domain Name System (DNS) queries for any resources in the on-premises network from the AWS VPC and also resolve any DNS queries for resources in the AWS VPC from the on-premises network.
- () As a solutions architect, which of the following solutions can be combined to address the given use case? (Select two)
- () Create an outbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint
- () Create a universal endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can receive and forward queries to resolvers on the on-premises network via this endpoint
- () Correct selection
- () Create an inbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint
- () Create an outbound endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via this endpoint
- () Create an inbound endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via this endpoint
- () Correct options:
- () To resolve any DNS queries for resources in the AWS VPC from the on-premises network, you can create an inbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint.
- () Resolver Inbound Endpoint:
- () via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- () Resolver Outbound Endpoint:
- () Create an outbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint - DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via an inbound endpoint. Hence, this option is incorrect.
- () Create an inbound endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via this endpoint - Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via an outbound endpoint. Hence, this option is incorrect.
- () Create a universal endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can receive and forward queries to resolvers on the on-premises network via this endpoint - There is no such thing as a universal endpoint on Amazon Route 53 Resolver. This option has been added as a distractor.
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver-getting-started.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- () A financial services company wants to move the Windows file server clusters out of their datacenters. They are looking for cloud file storage offerings that provide full Windows compatibility. Can you identify the AWS storage services that provide highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol compatible with Windows systems? (Select two)
- () Amazon Elastic Block Store (Amazon EBS)
- () File Gateway Configuration of AWS Storage Gateway

**Answer:**
Correct Answer: **Use VPC endpoint to access Amazon SQS**

---

## Question 188

**Q:** As a solutions architect, which of the following solutions can be combined to address the given use case? (Select two)

**Options:**
- **(A) Create an outbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint** [CORRECT]
- (B) Create a universal endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can receive and forward queries to resolvers on the on-premises network via this endpoint
- (C) Correct selection
- (D) Create an inbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint
- (E) Create an outbound endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via this endpoint
- (F) Create an inbound endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via this endpoint
- (G) Correct options:
- (H) To resolve any DNS queries for resources in the AWS VPC from the on-premises network, you can create an inbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint.
- (I) Resolver Inbound Endpoint:
- (J) via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- () Resolver Outbound Endpoint:
- () Incorrect options:
- () Create an outbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint - DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via an inbound endpoint. Hence, this option is incorrect.
- () Create an inbound endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via this endpoint - Amazon Route 53 Resolver can conditionally forward queries to resolvers on the on-premises network via an outbound endpoint. Hence, this option is incorrect.
- () Create a universal endpoint on Amazon Route 53 Resolver and then Amazon Route 53 Resolver can receive and forward queries to resolvers on the on-premises network via this endpoint - There is no such thing as a universal endpoint on Amazon Route 53 Resolver. This option has been added as a distractor.
- () References:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver-getting-started.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resolver.html
- () A financial services company wants to move the Windows file server clusters out of their datacenters. They are looking for cloud file storage offerings that provide full Windows compatibility. Can you identify the AWS storage services that provide highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol compatible with Windows systems? (Select two)
- () Amazon Elastic Block Store (Amazon EBS)
- () File Gateway Configuration of AWS Storage Gateway
- () Amazon FSx for Windows File Server
- () Amazon Simple Storage Service (Amazon S3)
- () Amazon Elastic File System (Amazon EFS)
- () Amazon FSx for Windows File Server is a fully managed, highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol. It is built on Windows Server, delivering a wide range of administrative features such as user quotas, end-user file restore, and Microsoft Active Directory (AD) integration.
- () Depending on the use case, AWS Storage Gateway provides 3 types of storage interfaces for on-premises applications: File, Volume, and Tape. The File Gateway enables you to store and retrieve objects in Amazon S3 using file protocols such as Network File System (NFS) and Server Message Block (SMB).
- () Amazon Elastic File System (Amazon EFS) - Amazon EFS is a file storage service for use with Amazon EC2. Amazon EFS provides a file system interface, file system access semantics, and concurrently-accessible storage for up to thousands of Amazon EC2 instances. Amazon EFS uses the Network File System protocol. EFS does not support SMB protocol.
- () Amazon Elastic Block Store (Amazon EBS) - Amazon EBS is a block-level storage service for use with Amazon EC2. Amazon EBS can deliver performance for workloads that require the lowest latency access to data from a single EC2 instance. EBS does not support SMB protocol.
- () Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. Amazon S3 provides a simple, standards-based REST web services interface that is designed to work with any Internet-development toolkit. S3 does not support SMB protocol.
- () https://aws.amazon.com/fsx/windows/
- () https://aws.amazon.com/storagegateway/file/
- () A financial services company has recently migrated from on-premises infrastructure to AWS Cloud. The DevOps team wants to implement a solution that allows all resource configurations to be reviewed and make sure that they meet compliance guidelines. Also, the solution should be able to offer the capability to look into the resource configuration history across the application stack.

**Answer:**
Correct Answer: **Create an outbound endpoint on Amazon Route 53 Resolver and then DNS resolvers on the on-premises network can forward DNS queries to Amazon Route 53 Resolver via this endpoint**

---

## Question 189

**Q:** A financial services company wants to move the Windows file server clusters out of their datacenters. They are looking for cloud file storage offerings that provide full Windows compatibility. Can you identify the AWS storage services that provide highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol compatible with Windows systems? (Select two)

**Options:**
- **(A) Amazon Elastic Block Store (Amazon EBS)** [CORRECT]
- (B) Correct selection
- (C) File Gateway Configuration of AWS Storage Gateway
- (D) Amazon FSx for Windows File Server
- (E) Amazon Simple Storage Service (Amazon S3)
- (F) Amazon Elastic File System (Amazon EFS)
- (G) Correct options:
- (H) Amazon FSx for Windows File Server is a fully managed, highly reliable file storage that is accessible over the industry-standard Server Message Block (SMB) protocol. It is built on Windows Server, delivering a wide range of administrative features such as user quotas, end-user file restore, and Microsoft Active Directory (AD) integration.
- (I) Depending on the use case, AWS Storage Gateway provides 3 types of storage interfaces for on-premises applications: File, Volume, and Tape. The File Gateway enables you to store and retrieve objects in Amazon S3 using file protocols such as Network File System (NFS) and Server Message Block (SMB).
- (J) Incorrect options:
- () Amazon Elastic File System (Amazon EFS) - Amazon EFS is a file storage service for use with Amazon EC2. Amazon EFS provides a file system interface, file system access semantics, and concurrently-accessible storage for up to thousands of Amazon EC2 instances. Amazon EFS uses the Network File System protocol. EFS does not support SMB protocol.
- () Amazon Elastic Block Store (Amazon EBS) - Amazon EBS is a block-level storage service for use with Amazon EC2. Amazon EBS can deliver performance for workloads that require the lowest latency access to data from a single EC2 instance. EBS does not support SMB protocol.
- () Amazon Simple Storage Service (Amazon S3) - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. Amazon S3 provides a simple, standards-based REST web services interface that is designed to work with any Internet-development toolkit. S3 does not support SMB protocol.
- () References:
- () https://aws.amazon.com/fsx/windows/
- () https://aws.amazon.com/storagegateway/file/
- () A financial services company has recently migrated from on-premises infrastructure to AWS Cloud. The DevOps team wants to implement a solution that allows all resource configurations to be reviewed and make sure that they meet compliance guidelines. Also, the solution should be able to offer the capability to look into the resource configuration history across the application stack.

**Answer:**
Correct Answer: **Amazon Elastic Block Store (Amazon EBS)**

---

## Question 190

**Q:** As a solutions architect, which of the following solutions would you recommend to the team?

**Options:**
- (A) Use AWS CloudTrail to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes
- (B) Use Amazon CloudWatch to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes
- (C) Use AWS Config to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes
- (D) Use AWS Systems Manager to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes
- (E) Correct option:
- (F) How AWS Config Works:
- (G) via - https://aws.amazon.com/config/
- (H) Incorrect options:
- (I) Use Amazon CloudWatch to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes - AWS CloudWatch provides you with data and actionable insights to monitor your applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health. You cannot use Amazon CloudWatch to maintain a history of resource configuration changes.
- (J) Use AWS Systems Manager to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes - Using AWS Systems Manager, you can group resources, like Amazon EC2 instances, Amazon S3 buckets, or Amazon RDS instances, by application, view operational data for monitoring and troubleshooting, and take action on your groups of resources. You cannot use AWS Systems Manager to maintain a history of resource configuration changes.
- () Exam Alert:
- () Think resource performance monitoring, events, and alerts; think Amazon CloudWatch.
- () Think account-specific activity and audit; think AWS CloudTrail.
- () Think resource-specific history, audit, and compliance; think AWS Config.
- () References:
- () https://aws.amazon.com/config/
- () https://aws.amazon.com/cloudwatch/
- () https://aws.amazon.com/cloudtrail/
- () https://aws.amazon.com/systems-manager/
- () A retail organization is moving some of its on-premises data to AWS Cloud. The DevOps team at the organization has set up an AWS Managed IPSec VPN Connection between their remote on-premises network and their Amazon VPC over the internet.
- () Which of the following represents the correct configuration for the IPSec VPN Connection?
- () Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN
- () Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN
- **() Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN** [CORRECT]
- () Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN
- () Amazon VPC provides the facility to create an IPsec VPN connection (also known as AWS site-to-site VPN) between remote customer networks and their Amazon VPC over the internet. The following are the key concepts for a site-to-site VPN:
- () Virtual private gateway: A virtual private gateway (VGW), also known as a VPN Gateway is the endpoint on the AWS VPC side of your VPN connection.
- () VPN connection: A secure connection between your on-premises equipment and your VPCs.
- () VPN tunnel: An encrypted link where data can pass from the customer network to or from AWS.
- () Customer Gateway: An AWS resource that provides information to AWS about your Customer Gateway device.
- () Customer Gateway device: A physical device or software application on the customer side of the Site-to-Site VPN connection.
- () AWS Managed IPSec VPN
- () via - https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html

**Answer:**
Correct Answer: **Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN**

---

## Question 191

**Q:** AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. With Config, you can review changes in configurations and relationships between AWS resources, dive into detailed resource configuration histories, and determine your overall compliance against the configurations specified in your internal guidelines. You can use Config to answer questions such as - “What did my AWS resource look like at xyz point in time?”

**Options:**
- (A) How AWS Config Works:
- (B) via - https://aws.amazon.com/config/
- (C) Incorrect options:
- (D) Use Amazon CloudWatch to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes - AWS CloudWatch provides you with data and actionable insights to monitor your applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health. You cannot use Amazon CloudWatch to maintain a history of resource configuration changes.
- (E) Use AWS Systems Manager to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes - Using AWS Systems Manager, you can group resources, like Amazon EC2 instances, Amazon S3 buckets, or Amazon RDS instances, by application, view operational data for monitoring and troubleshooting, and take action on your groups of resources. You cannot use AWS Systems Manager to maintain a history of resource configuration changes.
- (F) Exam Alert:
- (G) Think resource performance monitoring, events, and alerts; think Amazon CloudWatch.
- (H) Think account-specific activity and audit; think AWS CloudTrail.
- (I) Think resource-specific history, audit, and compliance; think AWS Config.
- (J) References:
- () https://aws.amazon.com/config/
- () https://aws.amazon.com/cloudwatch/
- () https://aws.amazon.com/cloudtrail/
- () https://aws.amazon.com/systems-manager/
- () A retail organization is moving some of its on-premises data to AWS Cloud. The DevOps team at the organization has set up an AWS Managed IPSec VPN Connection between their remote on-premises network and their Amazon VPC over the internet.
- () Which of the following represents the correct configuration for the IPSec VPN Connection?
- () Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN
- () Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN
- **() Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN** [CORRECT]
- () Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN
- () Correct option:
- () Amazon VPC provides the facility to create an IPsec VPN connection (also known as AWS site-to-site VPN) between remote customer networks and their Amazon VPC over the internet. The following are the key concepts for a site-to-site VPN:
- () Virtual private gateway: A virtual private gateway (VGW), also known as a VPN Gateway is the endpoint on the AWS VPC side of your VPN connection.
- () VPN connection: A secure connection between your on-premises equipment and your VPCs.
- () VPN tunnel: An encrypted link where data can pass from the customer network to or from AWS.
- () Customer Gateway: An AWS resource that provides information to AWS about your Customer Gateway device.
- () Customer Gateway device: A physical device or software application on the customer side of the Site-to-Site VPN connection.
- () AWS Managed IPSec VPN
- () via - https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- () A financial services company wants to identify any sensitive data stored on its Amazon S3 buckets. The company also wants to monitor and protect all data stored on Amazon S3 against any malicious activity.

**Answer:**
Correct Answer: **Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN**

---

## Question 192

**Q:** Use AWS CloudTrail to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes - With AWS CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. You can use AWS CloudTrail to answer questions such as - “Who made an API call to modify this resource?”. AWS CloudTrail provides an event history of your AWS account activity thereby enabling governance, compliance, operational auditing, and risk auditing of your AWS account. You cannot use AWS CloudTrail to maintain a history of resource configuration changes.

**Options:**
- (A) Use AWS Systems Manager to review resource configurations to meet compliance guidelines and maintain a history of resource configuration changes - Using AWS Systems Manager, you can group resources, like Amazon EC2 instances, Amazon S3 buckets, or Amazon RDS instances, by application, view operational data for monitoring and troubleshooting, and take action on your groups of resources. You cannot use AWS Systems Manager to maintain a history of resource configuration changes.
- (B) Exam Alert:
- (C) Think resource performance monitoring, events, and alerts; think Amazon CloudWatch.
- (D) Think account-specific activity and audit; think AWS CloudTrail.
- (E) Think resource-specific history, audit, and compliance; think AWS Config.
- (F) References:
- (G) https://aws.amazon.com/config/
- (H) https://aws.amazon.com/cloudwatch/
- (I) https://aws.amazon.com/cloudtrail/
- (J) https://aws.amazon.com/systems-manager/
- () A retail organization is moving some of its on-premises data to AWS Cloud. The DevOps team at the organization has set up an AWS Managed IPSec VPN Connection between their remote on-premises network and their Amazon VPC over the internet.
- () Which of the following represents the correct configuration for the IPSec VPN Connection?
- () Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN
- () Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN
- **() Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN** [CORRECT]
- () Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN
- () Correct option:
- () Amazon VPC provides the facility to create an IPsec VPN connection (also known as AWS site-to-site VPN) between remote customer networks and their Amazon VPC over the internet. The following are the key concepts for a site-to-site VPN:
- () Virtual private gateway: A virtual private gateway (VGW), also known as a VPN Gateway is the endpoint on the AWS VPC side of your VPN connection.
- () VPN connection: A secure connection between your on-premises equipment and your VPCs.
- () VPN tunnel: An encrypted link where data can pass from the customer network to or from AWS.
- () Customer Gateway: An AWS resource that provides information to AWS about your Customer Gateway device.
- () Customer Gateway device: A physical device or software application on the customer side of the Site-to-Site VPN connection.
- () AWS Managed IPSec VPN
- () via - https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () Incorrect options:
- () Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- () A financial services company wants to identify any sensitive data stored on its Amazon S3 buckets. The company also wants to monitor and protect all data stored on Amazon S3 against any malicious activity.

**Answer:**
Correct Answer: **Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN**

---

## Question 193

**Q:** Which of the following represents the correct configuration for the IPSec VPN Connection?

**Options:**
- (A) Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN
- (B) Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN
- **(C) Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN** [CORRECT]
- (D) Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN
- (E) Correct option:
- (F) Amazon VPC provides the facility to create an IPsec VPN connection (also known as AWS site-to-site VPN) between remote customer networks and their Amazon VPC over the internet. The following are the key concepts for a site-to-site VPN:
- (G) Virtual private gateway: A virtual private gateway (VGW), also known as a VPN Gateway is the endpoint on the AWS VPC side of your VPN connection.
- (H) VPN connection: A secure connection between your on-premises equipment and your VPCs.
- (I) VPN tunnel: An encrypted link where data can pass from the customer network to or from AWS.
- (J) Customer Gateway: An AWS resource that provides information to AWS about your Customer Gateway device.
- () Customer Gateway device: A physical device or software application on the customer side of the Site-to-Site VPN connection.
- () AWS Managed IPSec VPN
- () via - https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () Incorrect options:
- () Create a virtual private gateway (VGW) on the on-premises side of the VPN and a Customer Gateway on the AWS side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a Customer Gateway on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () Create a virtual private gateway (VGW) on both the AWS side of the VPN as well as the on-premises side of the VPN - You need to create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN. Therefore, this option is wrong.
- () References:
- () https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-managed-vpn-network-to-amazon.html
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- () A financial services company wants to identify any sensitive data stored on its Amazon S3 buckets. The company also wants to monitor and protect all data stored on Amazon S3 against any malicious activity.

**Answer:**
Correct Answer: **Create a virtual private gateway (VGW) on the AWS side of the VPN and a Customer Gateway on the on-premises side of the VPN**

---

## Question 194

**Q:** As a solutions architect, which of the following solutions would you recommend to help address the given requirements?

**Options:**
- (A) Use Amazon GuardDuty to monitor any malicious activity on data stored in Amazon S3 as well as to identify any sensitive data stored on Amazon S3
- (B) Use Amazon Macie to monitor any malicious activity on data stored in Amazon S3 as well as to identify any sensitive data stored on Amazon S3
- (C) Use Amazon Macie to monitor any malicious activity on data stored in Amazon S3. Use Amazon GuardDuty to identify any sensitive data stored on Amazon S3
- (D) Use Amazon GuardDuty to monitor any malicious activity on data stored in Amazon S3. Use Amazon Macie to identify any sensitive data stored on Amazon S3
- (E) Correct option:
- (F) Amazon GuardDuty offers threat detection that enables you to continuously monitor and protect your AWS accounts, workloads, and data stored in Amazon S3. GuardDuty analyzes continuous streams of meta-data generated from your account and network activity found in AWS CloudTrail Events, Amazon VPC Flow Logs, and DNS Logs. It also uses integrated threat intelligence such as known malicious IP addresses, anomaly detection, and machine learning to identify threats more accurately.
- (G) How Amazon GuardDuty works:
- (H) via - https://aws.amazon.com/guardduty/
- (I) Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data on Amazon S3. Macie automatically detects a large and growing list of sensitive data types, including personally identifiable information (PII) such as names, addresses, and credit card numbers. It also gives you constant visibility of the data security and data privacy of your data stored in Amazon S3.
- (J) How Amazon Macie works:
- () via - https://aws.amazon.com/macie/
- () Incorrect options:
- () These three options contradict the explanation provided above, so these options are incorrect.
- () References:
- () https://aws.amazon.com/guardduty/
- () https://aws.amazon.com/macie/
- () A company is migrating a legacy workload from on premises to AWS. The application receives customer order files from an on premises ERP system by using the SFTP protocol. After files arrive, the application must process them immediately rather than relying on periodic polling. The company already has secure network connectivity between AWS and the on premises environment. The new solution must remain highly available, secure, and resilient across infrastructure failures.
- () Which solution should you implement to meet these requirements?
- **() Deploy an internal AWS Transfer Family SFTP server across two Availability Zones backed by Amazon S3. Configure a Transfer Family managed workflow to invoke an AWS Lambda function immediately after file upload completes** [CORRECT]
- () Deploy an internal AWS Transfer Family SFTP server across two Availability Zones backed by Amazon EFS. Use Amazon EventBridge Scheduler to periodically trigger an AWS Step Functions state machine that scans for new files
- () Deploy an internet facing AWS Transfer Family SFTP server across two Availability Zones backed by Amazon S3. Configure Amazon S3 Event Notifications to invoke an AWS Lambda function when new objects are created
- () Deploy an internet facing AWS Transfer Family SFTP server in a single Availability Zone backed by Amazon EFS. Configure a Transfer Family managed workflow to invoke an AWS Lambda function after file upload completes
- () This solution meets all requirements for security, resilience, and immediate order processing while minimizing operational overhead. It leverages native service integrations designed for SFTP based file ingestion workflows.
- () Reference:
- () https://docs.aws.amazon.com/transfer/latest/userguide/what-is-aws-transfer-family.html
- () An AWS Organization is using Service Control Policies (SCPs) for central control over the maximum available permissions for all accounts in their organization. This allows the organization to ensure that all accounts stay within the organization’s access control guidelines.
- () Which of the given scenarios are correct regarding the permissions described below? (Select three)
- () If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can still perform that action
- () Correct selection
- () Service control policy (SCP) does not affect service-linked role
- () If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can't perform that action
- () Service control policy (SCP) affects service-linked roles

**Answer:**
Correct Answer: **Deploy an internal AWS Transfer Family SFTP server across two Availability Zones backed by Amazon S3. Configure a Transfer Family managed workflow to invoke an AWS Lambda function immediately after file upload completes**

---

## Question 195

**Q:** Which solution should you implement to meet these requirements?

**Options:**
- **(A) Deploy an internal AWS Transfer Family SFTP server across two Availability Zones backed by Amazon S3. Configure a Transfer Family managed workflow to invoke an AWS Lambda function immediately after file upload completes** [CORRECT]
- (B) Deploy an internal AWS Transfer Family SFTP server across two Availability Zones backed by Amazon EFS. Use Amazon EventBridge Scheduler to periodically trigger an AWS Step Functions state machine that scans for new files
- (C) Deploy an internet facing AWS Transfer Family SFTP server across two Availability Zones backed by Amazon S3. Configure Amazon S3 Event Notifications to invoke an AWS Lambda function when new objects are created
- (D) Deploy an internet facing AWS Transfer Family SFTP server in a single Availability Zone backed by Amazon EFS. Configure a Transfer Family managed workflow to invoke an AWS Lambda function after file upload completes
- (E) Correct option:
- (F) This solution meets all requirements for security, resilience, and immediate order processing while minimizing operational overhead. It leverages native service integrations designed for SFTP based file ingestion workflows.
- (G) Incorrect options:
- (H) Reference:
- (I) https://docs.aws.amazon.com/transfer/latest/userguide/what-is-aws-transfer-family.html
- (J) An AWS Organization is using Service Control Policies (SCPs) for central control over the maximum available permissions for all accounts in their organization. This allows the organization to ensure that all accounts stay within the organization’s access control guidelines.
- () Which of the given scenarios are correct regarding the permissions described below? (Select three)
- () If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can still perform that action
- () Correct selection
- () Service control policy (SCP) does not affect service-linked role
- () If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can't perform that action
- () Service control policy (SCP) affects service-linked roles
- () Service control policy (SCP) affects all users and roles in the member accounts, including root user of the member accounts
- () Service control policy (SCP) affects all users and roles in the member accounts, excluding root user of the member accounts
- () Correct options:
- () Service control policy (SCP) are one type of policy that can be used to manage your organization. Service control policy (SCP) offers central control over the maximum available permissions for all accounts in your organization, allowing you to ensure your accounts stay within your organization’s access control guidelines.
- () In service control policy (SCP), you can restrict which AWS services, resources, and individual API actions the users and roles in each member account can access. You can also define conditions for when to restrict access to AWS services, resources, and API actions. These restrictions even override the administrators of member accounts in the organization.
- () Please note the following effects on permissions vis-a-vis the service control policy (SCP):
- () If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can't perform that action.
- () Service control policy (SCP) affects all users and roles in the member accounts, including root user of the member accounts.
- () Service control policy (SCP) does not affect any service-linked role.
- () These three options contradict the details provided in the explanation above.
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scp.html
- () A company has its application servers in the public subnet that connect to the database instances in the private subnet. For regular maintenance, the database instances need patch fixes that need to be downloaded from the internet.

**Answer:**
Correct Answer: **Deploy an internal AWS Transfer Family SFTP server across two Availability Zones backed by Amazon S3. Configure a Transfer Family managed workflow to invoke an AWS Lambda function immediately after file upload completes**

---

## Question 196

**Q:** Which of the given scenarios are correct regarding the permissions described below? (Select three)

**Options:**
- **(A) If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can still perform that action** [CORRECT]
- (B) Correct selection
- (C) Service control policy (SCP) does not affect service-linked role
- (D) If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can't perform that action
- (E) Service control policy (SCP) affects service-linked roles
- (F) Service control policy (SCP) affects all users and roles in the member accounts, including root user of the member accounts
- (G) Service control policy (SCP) affects all users and roles in the member accounts, excluding root user of the member accounts
- (H) Correct options:
- (I) Service control policy (SCP) are one type of policy that can be used to manage your organization. Service control policy (SCP) offers central control over the maximum available permissions for all accounts in your organization, allowing you to ensure your accounts stay within your organization’s access control guidelines.
- (J) In service control policy (SCP), you can restrict which AWS services, resources, and individual API actions the users and roles in each member account can access. You can also define conditions for when to restrict access to AWS services, resources, and API actions. These restrictions even override the administrators of member accounts in the organization.
- () Please note the following effects on permissions vis-a-vis the service control policy (SCP):
- () If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can't perform that action.
- () Service control policy (SCP) affects all users and roles in the member accounts, including root user of the member accounts.
- () Service control policy (SCP) does not affect any service-linked role.
- () Incorrect options:
- () These three options contradict the details provided in the explanation above.
- () Reference:
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scp.html
- () A company has its application servers in the public subnet that connect to the database instances in the private subnet. For regular maintenance, the database instances need patch fixes that need to be downloaded from the internet.

**Answer:**
Correct Answer: **If a user or role has an IAM permission policy that grants access to an action that is either not allowed or explicitly denied by the applicable service control policy (SCP), the user or role can still perform that action**

---

## Question 197

**Q:** Considering the company uses only IPv4 addressing and is looking for a fully managed service, which of the following would you suggest as an optimal solution?

**Options:**
- (A) Configure a Network Address Translation gateway (NAT gateway) in the public subnet of the VPC
- (B) Configure an Egress-only internet gateway for the resources in the private subnet of the VPC
- (C) Configure a Network Address Translation instance (NAT instance) in the public subnet of the VPC
- (D) Configure the Internet Gateway of the VPC to be accessible to the private subnet resources by changing the route tables
- (E) Correct option:
- (F) You can use a Network Address Translation gateway (NAT gateway) to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances. To create a NAT gateway, you must specify the public subnet in which the NAT gateway should reside.
- (G) VPC architecture with NAT:
- (H) via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- (I) Incorrect options:
- (J) Configure an Egress-only internet gateway for the resources in the private subnet of the VPC - An Egress-only internet gateway is an Internet Gateway that supports IPv6 traffic, so this option is not correct for the given use-case.
- () Configure a Network Address Translation instance (NAT instance) in the public subnet of the VPC - You can use a network address translation (NAT) instance in a public subnet in your VPC to enable instances in the private subnet to initiate outbound IPv4 traffic to the internet or other AWS services, but prevent the instances from receiving inbound traffic initiated by someone on the internet. NAT instances are not a managed service, it has to be managed and maintained by the customer.
- () Configure the Internet Gateway of the VPC to be accessible to the private subnet resources by changing the route tables - Internet Gateway cannot be used directly with a private subnet. It is not possible to set up this configuration, without a NAT instance or a NAT gateway in the public subnet.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/egress-only-internet-gateway.html
- () A company is transferring a significant volume of data from on-site storage to AWS, where it will be accessed by Windows, Mac, and Linux-based Amazon EC2 instances within the same AWS region using both SMB and NFS protocols. Part of this data will be accessed regularly, while the rest will be accessed less frequently. The company requires a hosting solution for this data that minimizes operational overhead.
- () What solution would best meet these requirements?
- () Set up an Amazon FSx for OpenZFS instance. Configure an FSx for OpenZFS file ystem on the root volume and migrate the data to the FSx for OpenZFS volume
- () Set up an Amazon Elastic File System (Amazon EFS) volume that uses EFS Intelligent-Tiering. Use AWS DataSync to migrate the data to the EFS volume
- **() Set up an Amazon FSx for ONTAP instance. Configure an FSx for ONTAP file system on the root volume and migrate the data to the FSx for ONTAP volume** [CORRECT]
- () Set up an Amazon Elastic File System (Amazon EFS) volume that uses EFS Infrequent Access. Use AWS DataSync to migrate the data to the EFS volume
- () Amazon FSx for NetApp ONTAP is a storage service that allows customers to launch and run fully managed ONTAP file systems in the cloud. ONTAP is NetApp’s file system technology that provides a widely adopted set of data access and data management capabilities.
- () Amazon FSx for NetApp ONTAP Overview via - https://aws.amazon.com/fsx/netapp-ontap/
- () The given use case mandates that the storage on AWS will be accessed by Windows, Mac, and Linux-based Amazon EC2 instances within the same AWS region using both SMB and NFS protocols. Amongst the Amazon FSx family, FSx for ONTAP is the only file system that supports this key requirement.
- () via - https://aws.amazon.com/fsx/when-to-choose-fsx/
- () Amazon EFS is not supported on Windows instances. So, both these options are incorrect.
- () https://aws.amazon.com/fsx/netapp-ontap/
- () https://aws.amazon.com/fsx/when-to-choose-fsx/
- () https://aws.amazon.com/fsx/openzfs/faqs/
- () https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/AmazonEFS.html

**Answer:**
Correct Answer: **Set up an Amazon FSx for ONTAP instance. Configure an FSx for ONTAP file system on the root volume and migrate the data to the FSx for ONTAP volume**

---

## Question 198

**Q:** What solution would best meet these requirements?

**Options:**
- (A) Set up an Amazon FSx for OpenZFS instance. Configure an FSx for OpenZFS file ystem on the root volume and migrate the data to the FSx for OpenZFS volume
- (B) Set up an Amazon Elastic File System (Amazon EFS) volume that uses EFS Intelligent-Tiering. Use AWS DataSync to migrate the data to the EFS volume
- **(C) Set up an Amazon FSx for ONTAP instance. Configure an FSx for ONTAP file system on the root volume and migrate the data to the FSx for ONTAP volume** [CORRECT]
- (D) Set up an Amazon Elastic File System (Amazon EFS) volume that uses EFS Infrequent Access. Use AWS DataSync to migrate the data to the EFS volume
- (E) Correct option:
- (F) Amazon FSx for NetApp ONTAP is a storage service that allows customers to launch and run fully managed ONTAP file systems in the cloud. ONTAP is NetApp’s file system technology that provides a widely adopted set of data access and data management capabilities.
- (G) Amazon FSx for NetApp ONTAP Overview via - https://aws.amazon.com/fsx/netapp-ontap/
- (H) The given use case mandates that the storage on AWS will be accessed by Windows, Mac, and Linux-based Amazon EC2 instances within the same AWS region using both SMB and NFS protocols. Amongst the Amazon FSx family, FSx for ONTAP is the only file system that supports this key requirement.
- (I) via - https://aws.amazon.com/fsx/when-to-choose-fsx/
- (J) Incorrect options:
- () Amazon EFS is not supported on Windows instances. So, both these options are incorrect.
- () References:
- () https://aws.amazon.com/fsx/netapp-ontap/
- () https://aws.amazon.com/fsx/when-to-choose-fsx/
- () https://aws.amazon.com/fsx/openzfs/faqs/
- () https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/AmazonEFS.html

**Answer:**
Correct Answer: **Set up an Amazon FSx for ONTAP instance. Configure an FSx for ONTAP file system on the root volume and migrate the data to the FSx for ONTAP volume**

---

## Question 199

**Q:** As an AWS Certified Solutions Architect Associate, which of the following would you recommend?

**Options:**
- (A) Set up a Gateway Load Balancer (GWLB) endpoint for Amazon S3. Update the route table in the private subnet to direct the S3-bound traffic via the Gateway Load Balancer (GWLB) endpoint
- (B) Set up a VPC gateway endpoint for Amazon S3. Attach an endpoint policy to the endpoint. Update the route table to direct the S3-bound traffic to the VPC endpoint
- (C) Set up an egress-only internet gateway in the public subnet. Update the route table in the private subnet to route traffic to the internet gateway. Update the network ACL to allow the S3-bound traffic
- (D) Provision an internet gateway. Update the route table in the private subnet to route traffic to the internet gateway. Update the network ACL (NACL) to allow the S3-bound traffic
- (E) Correct option:
- (F) Gateway endpoints provide reliable connectivity to Amazon S3 without requiring an internet gateway or a NAT device for your VPC. After you create the gateway endpoint, you can add it as a target in your route table for traffic destined from your VPC to Amazon S3. There is no additional charge for using gateway endpoints.
- (G) The VPC endpoint policy for the gateway endpoint controls access to Amazon S3 from the VPC through the endpoint. The default policy allows full access.
- (H) via - https://docs.aws.amazon.com/vpc/latest/privatelink/gateway-endpoints.html
- (I) Using the VPC gateway endpoint allows the Amazon EC2 instances to reach Amazon S3 without using the public internet. Since the data transfer remains within the same AWS region, so there is no data transfer costs for ingress as well as egress traffic. Hence this is the most cost-optimal solution.
- (J) Incorrect options:
- () References:
- () https://docs.aws.amazon.com/vpc/latest/privatelink/gateway-endpoints.html
- () https://aws.amazon.com/premiumsupport/knowledge-center/vpc-reduce-nat-gateway-transfer-costs/
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpce-gateway-load-balancer.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/egress-only-internet-gateway.html
- () The database backend for a retail company's website is hosted on Amazon RDS for MySQL having a primary instance and three read replicas to support read scalability. The company has mandated that the read replicas should lag no more than 1 second behind the primary instance to provide the best possible user experience. The read replicas are falling further behind during periods of peak traffic spikes, resulting in a bad user experience as the searches produce inconsistent results.
- () You have been hired as an AWS Certified Solutions Architect - Associate to reduce the replication lag as much as possible with minimal changes to the application code or the effort required to manage the underlying resources.
- () Which of the following will you recommend?
- () Set up an Amazon ElastiCache for Redis cluster in front of the MySQL database. Update the website to check the cache before querying the read replicas
- () Set up database migration from Amazon RDS MySQL to Amazon Aurora MySQL. Swap out the MySQL read replicas with Aurora Replicas. Configure Aurora Auto Scaling
- () Host the MySQL primary database on a memory-optimized Amazon EC2 instance. Spin up additional compute-optimized Amazon EC2 instances to host the read replicas
- () Set up database migration from Amazon RDS MySQL to Amazon DynamoDB. Provision a large number of read capacity units (RCUs) to support the required throughput and enable Auto-Scaling
- () Aurora features a distributed, fault-tolerant, and self-healing storage system that is decoupled from compute resources and auto-scales up to 128 TiB per database instance. It delivers high performance and availability with up to 15 low-latency read replicas, point-in-time recovery, continuous backup to Amazon Simple Storage Service (Amazon S3), and replication across three Availability Zones (AZs).
- () Since Amazon Aurora Replicas share the same data volume as the primary instance in the same AWS Region, there is virtually no replication lag. The replica lag times are in the 10s of milliseconds (compared to the replication lag of seconds in the case of MySQL read replicas). Therefore, this is the right option to ensure that the read replicas lag no more than 1 second behind the primary instance.
- () Aurora Replicas:
- () via - https://aws.amazon.com/rds/aurora/faqs/
- () Host the MySQL primary database on a memory-optimized Amazon EC2 instance. Spin up additional compute-optimized Amazon EC2 instances to host the read replicas - Hosting the MySQL primary database and the read replicas on the Amazon EC2 instances would result in significant overhead to manage the underlying resources such as OS patching, database patching, etc. So this option is incorrect.
- () Set up an Amazon ElastiCache for Redis cluster in front of the MySQL database. Update the website to check the cache before querying the read replicas - Introducing a caching layer would result in significant changes to the application code, so this option is incorrect.
- () Set up database migration from Amazon RDS MySQL to Amazon DynamoDB. Provision a large number of read capacity units (RCUs) to support the required throughput and enable Auto-Scaling - Introducing a NoSQL database, such as Amazon DynamoDB, would result in significant changes to the application code since the database queries would have to be re-written for Amazon DynamoDB. Therefore, this option is incorrect.
- () Reference:
- () https://aws.amazon.com/rds/aurora/faqs/
- () Your application is hosted by a provider on yourapp.provider.com. You would like to have your users access your application using www.your-domain.com, which you own and manage under Amazon Route 53.
- () Which Amazon Route 53 record should you create?
- **() Create a CNAME record** [CORRECT]
- () Create an Alias Record
- () Create a PTR record
- () Create an A record

**Answer:**
Correct Answer: **Create a CNAME record**

---

## Question 200

**Q:** Which of the following will you recommend?

**Options:**
- (A) Set up an Amazon ElastiCache for Redis cluster in front of the MySQL database. Update the website to check the cache before querying the read replicas
- (B) Set up database migration from Amazon RDS MySQL to Amazon Aurora MySQL. Swap out the MySQL read replicas with Aurora Replicas. Configure Aurora Auto Scaling
- (C) Host the MySQL primary database on a memory-optimized Amazon EC2 instance. Spin up additional compute-optimized Amazon EC2 instances to host the read replicas
- (D) Set up database migration from Amazon RDS MySQL to Amazon DynamoDB. Provision a large number of read capacity units (RCUs) to support the required throughput and enable Auto-Scaling
- (E) Correct option:
- (F) Aurora features a distributed, fault-tolerant, and self-healing storage system that is decoupled from compute resources and auto-scales up to 128 TiB per database instance. It delivers high performance and availability with up to 15 low-latency read replicas, point-in-time recovery, continuous backup to Amazon Simple Storage Service (Amazon S3), and replication across three Availability Zones (AZs).
- (G) Since Amazon Aurora Replicas share the same data volume as the primary instance in the same AWS Region, there is virtually no replication lag. The replica lag times are in the 10s of milliseconds (compared to the replication lag of seconds in the case of MySQL read replicas). Therefore, this is the right option to ensure that the read replicas lag no more than 1 second behind the primary instance.
- (H) Aurora Replicas:
- (I) via - https://aws.amazon.com/rds/aurora/faqs/
- (J) Incorrect options:
- () Host the MySQL primary database on a memory-optimized Amazon EC2 instance. Spin up additional compute-optimized Amazon EC2 instances to host the read replicas - Hosting the MySQL primary database and the read replicas on the Amazon EC2 instances would result in significant overhead to manage the underlying resources such as OS patching, database patching, etc. So this option is incorrect.
- () Set up an Amazon ElastiCache for Redis cluster in front of the MySQL database. Update the website to check the cache before querying the read replicas - Introducing a caching layer would result in significant changes to the application code, so this option is incorrect.
- () Set up database migration from Amazon RDS MySQL to Amazon DynamoDB. Provision a large number of read capacity units (RCUs) to support the required throughput and enable Auto-Scaling - Introducing a NoSQL database, such as Amazon DynamoDB, would result in significant changes to the application code since the database queries would have to be re-written for Amazon DynamoDB. Therefore, this option is incorrect.
- () Reference:
- () https://aws.amazon.com/rds/aurora/faqs/
- () Your application is hosted by a provider on yourapp.provider.com. You would like to have your users access your application using www.your-domain.com, which you own and manage under Amazon Route 53.
- () Which Amazon Route 53 record should you create?
- **() Create a CNAME record** [CORRECT]
- () Create an Alias Record
- () Create a PTR record
- () Create an A record
- () A CNAME record maps DNS queries for the name of the current record, such as acme.example.com, to another domain (example.com or example.net) or subdomain (acme.example.com or zenith.example.org).
- () CNAME records can be used to map one domain name to another. Although you should keep in mind that the DNS protocol does not allow you to create a CNAME record for the top node of a DNS namespace, also known as the zone apex. For example, if you register the DNS name example.com, the zone apex is example.com. You cannot create a CNAME record for example.com, but you can create CNAME records for www.example.com, newproduct.example.com, and so on.
- () Please review the major differences between CNAME and Alias Records:
- () via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html
- () Create an A record - Used to point a domain or subdomain to an IP address. 'A record' cannot be used to map one domain name to another.
- () Create a PTR record - A Pointer (PTR) record resolves an IP address to a fully-qualified domain name (FQDN) as an opposite to what A record does. PTR records are also called Reverse DNS records. 'PTR record' cannot be used to map one domain name to another.
- () Create an Alias Record - Alias records let you route traffic to selected AWS resources, such as Amazon CloudFront distributions and Amazon S3 buckets. They also let you route traffic from one record in a hosted zone to another record. 3rd party websites do not qualify for these as we have no control over those. 'Alias record' cannot be used to map one domain name to another.
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html
- () A global pharmaceutical company wants to move most of the on-premises data into Amazon S3, Amazon Elastic File System (Amazon EFS), and Amazon FSx for Windows File Server easily, quickly, and cost-effectively.

**Answer:**
Correct Answer: **Create a CNAME record**

---

## Question 201

**Q:** Which Amazon Route 53 record should you create?

**Options:**
- **(A) Create a CNAME record** [CORRECT]
- (B) Create an Alias Record
- (C) Create a PTR record
- (D) Create an A record
- (E) Correct option:
- (F) A CNAME record maps DNS queries for the name of the current record, such as acme.example.com, to another domain (example.com or example.net) or subdomain (acme.example.com or zenith.example.org).
- (G) CNAME records can be used to map one domain name to another. Although you should keep in mind that the DNS protocol does not allow you to create a CNAME record for the top node of a DNS namespace, also known as the zone apex. For example, if you register the DNS name example.com, the zone apex is example.com. You cannot create a CNAME record for example.com, but you can create CNAME records for www.example.com, newproduct.example.com, and so on.
- (H) Please review the major differences between CNAME and Alias Records:
- (I) via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html
- (J) Incorrect options:
- () Create an A record - Used to point a domain or subdomain to an IP address. 'A record' cannot be used to map one domain name to another.
- () Create a PTR record - A Pointer (PTR) record resolves an IP address to a fully-qualified domain name (FQDN) as an opposite to what A record does. PTR records are also called Reverse DNS records. 'PTR record' cannot be used to map one domain name to another.
- () Create an Alias Record - Alias records let you route traffic to selected AWS resources, such as Amazon CloudFront distributions and Amazon S3 buckets. They also let you route traffic from one record in a hosted zone to another record. 3rd party websites do not qualify for these as we have no control over those. 'Alias record' cannot be used to map one domain name to another.
- () Reference:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html
- () A global pharmaceutical company wants to move most of the on-premises data into Amazon S3, Amazon Elastic File System (Amazon EFS), and Amazon FSx for Windows File Server easily, quickly, and cost-effectively.

**Answer:**
Correct Answer: **Create a CNAME record**

---

## Question 202

**Q:** As a solutions architect, which of the following solutions would you recommend as the BEST fit to automate and accelerate online data transfers to these AWS storage services?

**Options:**
- (A) Use AWS DataSync to automate and accelerate online data transfers to the given AWS storage services
- (B) Use AWS Transfer Family to automate and accelerate online data transfers to the given AWS storage services
- (C) Use AWS Snowball Edge Storage Optimized device to automate and accelerate online data transfers to the given AWS storage services
- (D) Use File Gateway to automate and accelerate online data transfers to the given AWS storage services
- (E) Correct option:
- (F) AWS DataSync is an online data transfer service that simplifies, automates, and accelerates copying large amounts of data to and from AWS storage services over the internet or AWS Direct Connect.
- (G) AWS DataSync fully automates and accelerates moving large active datasets to AWS, up to 10 times faster than command-line tools. It is natively integrated with Amazon S3, Amazon EFS, Amazon FSx for Windows File Server, Amazon CloudWatch, and AWS CloudTrail, which provides seamless and secure access to your storage services, as well as detailed monitoring of the transfer.
- (H) AWS DataSync uses a purpose-built network protocol and scale out architecture to transfer data. A single DataSync agent is capable of saturating a 10 Gbps network link.
- (I) AWS DataSync fully automates the data transfer. It comes with retry and network resiliency mechanisms, network optimizations, built-in task scheduling, monitoring via the DataSync API and Console, and Amazon CloudWatch metrics, events, and logs that provide granular visibility into the transfer process. AWS DataSync performs data integrity verification both during the transfer and at the end of the transfer.
- (J) How AWS DataSync Works:
- () via - https://aws.amazon.com/datasync/
- () Incorrect options:
- () AWS Snowball Edge is suitable for offline data transfers, for customers who are bandwidth constrained or transferring data from remote, disconnected, or austere environments. Therefore, it cannot support automated and accelerated online data transfers.
- () Use AWS Transfer Family to automate and accelerate online data transfers to the given AWS storage services - The AWS Transfer Family provides fully managed support for file transfers directly into and out of Amazon S3 and Amazon EFS. Therefore, it cannot support migration into the other AWS storage services mentioned in the given use-case (Amazon FSx for Windows File Server).
- () References:
- () https://aws.amazon.com/datasync/faqs/
- () https://aws.amazon.com/storagegateway/file/
- () https://aws.amazon.com/aws-transfer-family/
- () A health care application processes the real-time health data of the patients into an analytics workflow. With a sharp increase in the number of users, the system has become slow and sometimes even unresponsive as it does not have a retry mechanism. The startup is looking at a scalable solution that has minimal implementation overhead.
- () Which of the following would you recommend as a scalable alternative to the current solution?
- () Use Amazon Simple Queue Service (Amazon SQS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing
- () Use Amazon Kinesis Data Streams to ingest the data, process it using AWS Lambda or run analytics using Amazon Kinesis Data Analytics
- () Use Amazon Simple Notification Service (Amazon SNS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing
- () Use Amazon API Gateway with the existing REST-based interface to create a high performing architecture
- () KDS makes sure your streaming data is available to multiple real-time analytics applications, to Amazon S3, or AWS Lambda within 70 milliseconds of the data being collected. Amazon Kinesis data streams scale from megabytes to terabytes per hour and scale from thousands to millions of PUT records per second. You can dynamically adjust the throughput of your stream at any time based on the volume of your input data.
- () How Data Streams work:
- () via - https://aws.amazon.com/kinesis/data-streams/?nc=sn&loc=2&dn=2
- () Use Amazon Simple Notification Service (Amazon SNS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing - Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication. Amazon SNS is a push mechanism that does not support robust retry mechanisms, as is needed in the current use case.
- () Use Amazon Simple Queue Service (Amazon SQS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing - Amazon Simple Queue Service (Amazon SQS) is a messaging service that helps in decoupling systems and reducing the complexity of architecture. Amazon SQS can still work but Amazon Kinesis Data streams is custom made for streaming real-time data.
- () Use Amazon API Gateway with the existing REST-based interface to create a high performing architecture - Amazon API Gateway is not meant for handling real-time streaming data.
- () Reference:
- () https://aws.amazon.com/kinesis/data-streams/?nc=sn&loc=2&dn=2
- () A healthcare company has deployed its web application on Amazon Elastic Container Service (Amazon ECS) container instances running behind an Application Load Balancer. The website slows down when the traffic spikes and the website availability is also reduced. The development team has configured Amazon CloudWatch alarms to receive notifications whenever there is an availability constraint so the team can scale out resources. The company wants an automated solution to respond to such events.
- () Which of the following addresses the given use case?
- () Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's target group's CPU utilization rises above a threshold
- **() Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold** [CORRECT]
- () Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the CloudWatch alarm's CPU utilization rises above a threshold

**Answer:**
Correct Answer: **Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold**

---

## Question 203

**Q:** Which of the following would you recommend as a scalable alternative to the current solution?

**Options:**
- (A) Use Amazon Simple Queue Service (Amazon SQS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing
- (B) Use Amazon Kinesis Data Streams to ingest the data, process it using AWS Lambda or run analytics using Amazon Kinesis Data Analytics
- (C) Use Amazon Simple Notification Service (Amazon SNS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing
- (D) Use Amazon API Gateway with the existing REST-based interface to create a high performing architecture
- (E) Correct option:
- (F) KDS makes sure your streaming data is available to multiple real-time analytics applications, to Amazon S3, or AWS Lambda within 70 milliseconds of the data being collected. Amazon Kinesis data streams scale from megabytes to terabytes per hour and scale from thousands to millions of PUT records per second. You can dynamically adjust the throughput of your stream at any time based on the volume of your input data.
- (G) How Data Streams work:
- (H) via - https://aws.amazon.com/kinesis/data-streams/?nc=sn&loc=2&dn=2
- (I) Incorrect options:
- (J) Use Amazon Simple Notification Service (Amazon SNS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing - Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication. Amazon SNS is a push mechanism that does not support robust retry mechanisms, as is needed in the current use case.
- () Use Amazon Simple Queue Service (Amazon SQS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing - Amazon Simple Queue Service (Amazon SQS) is a messaging service that helps in decoupling systems and reducing the complexity of architecture. Amazon SQS can still work but Amazon Kinesis Data streams is custom made for streaming real-time data.
- () Use Amazon API Gateway with the existing REST-based interface to create a high performing architecture - Amazon API Gateway is not meant for handling real-time streaming data.
- () Reference:
- () https://aws.amazon.com/kinesis/data-streams/?nc=sn&loc=2&dn=2
- () A healthcare company has deployed its web application on Amazon Elastic Container Service (Amazon ECS) container instances running behind an Application Load Balancer. The website slows down when the traffic spikes and the website availability is also reduced. The development team has configured Amazon CloudWatch alarms to receive notifications whenever there is an availability constraint so the team can scale out resources. The company wants an automated solution to respond to such events.
- () Which of the following addresses the given use case?
- () Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's target group's CPU utilization rises above a threshold
- **() Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold** [CORRECT]
- () Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the CloudWatch alarm's CPU utilization rises above a threshold
- () Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's CPU utilization rises above a threshold
- () You use the Amazon ECS first-run wizard to create a cluster and a service that runs behind an Elastic Load Balancing load balancer. Then you can configure a target tracking scaling policy that scales your service automatically based on the current application load as measured by the service's CPU utilization (from the ECS, ClusterName, and ServiceName category in CloudWatch).
- () via - https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html
- () These three options contradict the explanation provided above, so these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-autoscaling-targettracking.html
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html

**Answer:**
Correct Answer: **Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold**

---

## Question 204

**Q:** via - https://aws.amazon.com/kinesis/data-streams/?nc=sn&loc=2&dn=2

**Options:**
- (A) Incorrect options:
- (B) Use Amazon Simple Notification Service (Amazon SNS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing - Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for both application-to-application (A2A) and application-to-person (A2P) communication. Amazon SNS is a push mechanism that does not support robust retry mechanisms, as is needed in the current use case.
- (C) Use Amazon Simple Queue Service (Amazon SQS) for data ingestion and configure AWS Lambda to trigger logic for downstream processing - Amazon Simple Queue Service (Amazon SQS) is a messaging service that helps in decoupling systems and reducing the complexity of architecture. Amazon SQS can still work but Amazon Kinesis Data streams is custom made for streaming real-time data.
- (D) Use Amazon API Gateway with the existing REST-based interface to create a high performing architecture - Amazon API Gateway is not meant for handling real-time streaming data.
- (E) Reference:
- (F) https://aws.amazon.com/kinesis/data-streams/?nc=sn&loc=2&dn=2
- (G) A healthcare company has deployed its web application on Amazon Elastic Container Service (Amazon ECS) container instances running behind an Application Load Balancer. The website slows down when the traffic spikes and the website availability is also reduced. The development team has configured Amazon CloudWatch alarms to receive notifications whenever there is an availability constraint so the team can scale out resources. The company wants an automated solution to respond to such events.
- (H) Which of the following addresses the given use case?
- (I) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's target group's CPU utilization rises above a threshold
- **(J) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold** [CORRECT]
- () Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the CloudWatch alarm's CPU utilization rises above a threshold
- () Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's CPU utilization rises above a threshold
- () Correct option:
- () You use the Amazon ECS first-run wizard to create a cluster and a service that runs behind an Elastic Load Balancing load balancer. Then you can configure a target tracking scaling policy that scales your service automatically based on the current application load as measured by the service's CPU utilization (from the ECS, ClusterName, and ServiceName category in CloudWatch).
- () via - https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html
- () These three options contradict the explanation provided above, so these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-autoscaling-targettracking.html
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html

**Answer:**
Correct Answer: **Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold**

---

## Question 205

**Q:** https://aws.amazon.com/kinesis/data-streams/?nc=sn&loc=2&dn=2

**Options:**
- (A) A healthcare company has deployed its web application on Amazon Elastic Container Service (Amazon ECS) container instances running behind an Application Load Balancer. The website slows down when the traffic spikes and the website availability is also reduced. The development team has configured Amazon CloudWatch alarms to receive notifications whenever there is an availability constraint so the team can scale out resources. The company wants an automated solution to respond to such events.
- (B) Which of the following addresses the given use case?
- (C) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's target group's CPU utilization rises above a threshold
- **(D) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold** [CORRECT]
- (E) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the CloudWatch alarm's CPU utilization rises above a threshold
- (F) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's CPU utilization rises above a threshold
- (G) Correct option:
- (H) You use the Amazon ECS first-run wizard to create a cluster and a service that runs behind an Elastic Load Balancing load balancer. Then you can configure a target tracking scaling policy that scales your service automatically based on the current application load as measured by the service's CPU utilization (from the ECS, ClusterName, and ServiceName category in CloudWatch).
- (I) via - https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html
- (J) Incorrect options:
- () These three options contradict the explanation provided above, so these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-autoscaling-targettracking.html
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html

**Answer:**
Correct Answer: **Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold**

---

## Question 206

**Q:** Which of the following addresses the given use case?

**Options:**
- (A) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's target group's CPU utilization rises above a threshold
- **(B) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold** [CORRECT]
- (C) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the CloudWatch alarm's CPU utilization rises above a threshold
- (D) Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the Application Load Balancer's CPU utilization rises above a threshold
- (E) Correct option:
- (F) You use the Amazon ECS first-run wizard to create a cluster and a service that runs behind an Elastic Load Balancing load balancer. Then you can configure a target tracking scaling policy that scales your service automatically based on the current application load as measured by the service's CPU utilization (from the ECS, ClusterName, and ServiceName category in CloudWatch).
- (G) via - https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html
- (H) Incorrect options:
- (I) These three options contradict the explanation provided above, so these options are incorrect.
- (J) References:
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-autoscaling-targettracking.html
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-configure-auto-scaling.html

**Answer:**
Correct Answer: **Configure AWS Auto Scaling to scale out the Amazon ECS cluster when the ECS service's CPU utilization rises above a threshold**

---


