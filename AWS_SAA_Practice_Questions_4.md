# AWS SAA-C03 Practice Questions - Part 4

Total Questions: 206

---

## Question 1

**Q:** As a solutions architect, which of the following is the MOST cost-effective solution that you would recommend to the web development team?

**Options:**
- (A) Create an MX record for covid19survey.com that routes traffic to www.covid19survey.com
- (B) Create an NS record for covid19survey.com that routes traffic to www.covid19survey.com
- (C) Create an alias record for covid19survey.com that routes traffic to www.covid19survey.com
- (D) Create a CNAME record for covid19survey.com that routes traffic to www.covid19survey.com
- (E) Correct option:
- (F) Alias records provide Amazon Route 53–specific extension to DNS functionality. Alias records let you route traffic to selected AWS resources, such as Amazon CloudFront distributions and Amazon S3 buckets.
- (G) You can create an alias record at the top node of a DNS namespace, also known as the zone apex, however, you cannot create a CNAME record for the top node of the DNS namespace. So, if you register the DNS name covid19survey.com, the zone apex is covid19survey.com. You can't create a CNAME record for covid19survey.com, but you can create an alias record for covid19survey.com that routes traffic to www.covid19survey.com.
- (H) Exam Alert:
- (I) Incorrect options:
- (J) Create a CNAME record for covid19survey.com that routes traffic to www.covid19survey.com - You cannot create a CNAME record for the top node of the DNS namespace, so this option is incorrect.
- () Create an MX record for covid19survey.com that routes traffic to www.covid19survey.com - An MX record specifies the names of your mail servers and, if you have two or more mail servers, the priority order. It cannot be used to create Amazon Route 53 record to route traffic for the top node of the DNS namespace, so this option is incorrect.
- () Create an NS record for covid19survey.com that routes traffic to www.covid19survey.com - An NS record identifies the name servers for the hosted zone. It cannot be used to create Amazon Route 53 record to route traffic for the top node of the DNS namespace, so this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/ResourceRecordTypes.html
- () A data analytics company manages an application that stores user data in a Amazon DynamoDB table. The development team has observed that once in a while, the application writes corrupted data in the Amazon DynamoDB table. As soon as the issue is detected, the team needs to remove the corrupted data at the earliest.
- () What do you recommend?
- **() Use Amazon DynamoDB point in time recovery to restore the table to the state just before corrupted data was written** [CORRECT]
- () Use Amazon DynamoDB on-demand backup to restore the table to the state just before corrupted data was written
- () Configure the Amazon DynamoDB table as a global table and point the application to use the table from another AWS region that has no corrupted data
- () Use Amazon DynamoDB Streams to restore the table to the state just before corrupted data was written
- () Amazon DynamoDB enables you to back up your table data continuously by using point-in-time recovery (PITR). When you enable PITR, DynamoDB backs up your table data automatically with per-second granularity so that you can restore to any given second in the preceding 35 days.
- ()  call, PITR has you covered.
- () On-demand backup is created upon request. So this option is not correct since an on-demand backup cannot be created pre-emptively to handle data corruption issues that happen once in a while.
- () Configure the Amazon DynamoDB table as a global table and point the application to use the table from another AWS region that has no corrupted data - Global tables build on the global Amazon DynamoDB footprint to provide you with a fully managed, multi-Region, and multi-active database that delivers fast, local, read and write performance for massively scaled, global applications.
- () Global tables eliminate the difficult work of replicating data between Regions and resolving update conflicts, enabling you to focus on your application's business logic. In addition, global tables enable your applications to stay highly available even in the unlikely event of isolation or degradation of an entire Region.
- ()  table in another region. It's just a single logical Global table.
- () Amazon DynamoDB Streams writes stream records in near-real time so that you can build applications that consume these streams and take action based on the contents. It will take considerable effort and custom coding to reliably rebuild table data to the state just before any corrupted data was written. So this option is not the best fit.
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/BackupRestore.html
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/PointInTimeRecovery_Howitworks.html
- () https://aws.amazon.com/dynamodb/global-tables/
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html
- () A media company wants a low-latency way to distribute live sports results which are delivered via a proprietary application using UDP protocol.

**Answer:**
Correct Answer: **Use Amazon DynamoDB point in time recovery to restore the table to the state just before corrupted data was written**

---

## Question 2

**Q:** As a solutions architect, which of the following solutions would you recommend such that it offers the BEST performance for this use case?

**Options:**
- (A) Use Amazon CloudFront to provide a low latency way to distribute live sports results
- (B) Use AWS Global Accelerator to provide a low latency way to distribute live sports results
- (C) Use Auto Scaling group to provide a low latency way to distribute live sports results
- (D) Use Elastic Load Balancing (ELB) to provide a low latency way to distribute live sports results
- (E) Correct option:
- (F) How AWS Global Accelerator Works:
- (G) via - https://aws.amazon.com/global-accelerator/
- (H) Incorrect options:
- (I) Use Amazon CloudFront to provide a low latency way to distribute live sports results - Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.
- (J) Exam Alert:
- () Please note the differences between the capabilities of AWS Global Accelerator and Amazon CloudFront -
- () AWS Global Accelerator and Amazon CloudFront are separate services that use the AWS global network and its edge locations around the world. Amazon CloudFront improves performance for both cacheable content (such as images and videos) and dynamic content (such as API acceleration and dynamic site delivery). AWS Global Accelerator improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions.
- () AWS Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover. Both services integrate with AWS Shield for DDoS protection.
- () References:
- () https://aws.amazon.com/global-accelerator/
- () https://aws.amazon.com/cloudfront/faqs/
- ()  instance tenancy but the VPC (V1) used by the Launch Template LT1 has the instance tenancy set to default. Later the DevOps team creates a new Launch Template (LT2) with shared (default) instance tenancy but the VPC (V2) used by the Launch Template LT2 has the instance tenancy set to dedicated.
- () Which of the following is correct regarding the instances launched via Launch Template LT1 and Launch Template LT2?
- () The instances launched by Launch Template LT1 will have default instance tenancy while the instances launched by the Launch Template LT2 will have dedicated instance tenancy
- () The instances launched by Launch Template LT1 will have dedicated instance tenancy while the instances launched by the Launch Template LT2 will have shared (default) instance tenancy
- **() The instances launched by both Launch Template LT1 and Launch Template LT2 will have dedicated instance tenancy** [CORRECT]
- () The instances launched by both Launch Template LT1 and Launch Template LT2 will have default instance tenancy
- () A launch template specifies instance configuration information. It includes the ID of the Amazon Machine Image (AMI), the instance type, a key pair, security groups, and other parameters used to launch EC2 instances. If you've launched an EC2 instance before, you specified the same information to launch the instance.
- () When you create a Launch Template, the default value for the instance tenancy is shared and the instance tenancy is controlled by the tenancy attribute of the VPC. If you set the Launch Template Tenancy to shared (default) and the VPC Tenancy is set to dedicated, then the instances have dedicated tenancy. If you set the Launch Template Tenancy to dedicated and the VPC Tenancy is set to default, then again the instances have dedicated tenancy.
- () Amazon EC2 provides three options for the tenancy of your EC2 instances:
- () Shared (Shared) – Multiple AWS accounts may share the same physical hardware. This is the default tenancy option when launching an instance.
- () Dedicated instances (Dedicated) – Your instance runs on single-tenant hardware. No other AWS customer shares the same physical server.
- () Dedicated Hosts (Dedicated host) – The instance runs on a physical server that is dedicated to your use. Using Dedicated Hosts makes it easier to bring your own licenses (BYOL) that have dedicated hardware requirements to EC2 and meet compliance use cases. If you choose this option, you must provide a host resource group for Tenancy host resource group.
- () The instances launched by Launch Template LT1 will have dedicated instance tenancy while the instances launched by the Launch Template LT2 will have shared (default) instance tenancy - If either Launch Template Tenancy or VPC Tenancy is set to dedicated, then the instance tenancy is also dedicated. Therefore, this option is incorrect.
- () The instances launched by Launch Template LT1 will have default instance tenancy while the instances launched by the Launch Template LT2 will have dedicated instance tenancy - If either Launch Template Tenancy or VPC Tenancy is set to dedicated, then the instance tenancy is also dedicated. Therefore, this option is incorrect.
- () The instances launched by both Launch Template LT1 and Launch Template LT2 will have default instance tenancy - If either Launch Template Tenancy or VPC Tenancy is set to dedicated, then the instance tenancy is also dedicated. Therefore, this option is incorrect.
- () Reference:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/advanced-settings-for-your-launch-template.html
- () Which combination of solutions will best fulfill these requirements with the least amount of operational overhead? (Select two)
- () Create individual Site-to-Site VPN connections from the data center to each VPC. Set up BGP route propagation for every tunnel to facilitate on-premises-to-VPC routing
- () Convert each existing private VIF into a new Direct Connect gateway association by attaching a virtual private gateway (VGW) to each VPC. Manually configure routing between VGWs
- () Correct selection
- () Create an AWS Transit Gateway and attach all 25 VPCs to it. Enable route propagation for each attachment to automatically manage inter-VPC routing

**Answer:**
Correct Answer: **The instances launched by both Launch Template LT1 and Launch Template LT2 will have dedicated instance tenancy**

---

## Question 3

**Q:** Which of the following is correct regarding the instances launched via Launch Template LT1 and Launch Template LT2?

**Options:**
- (A) The instances launched by Launch Template LT1 will have default instance tenancy while the instances launched by the Launch Template LT2 will have dedicated instance tenancy
- (B) The instances launched by Launch Template LT1 will have dedicated instance tenancy while the instances launched by the Launch Template LT2 will have shared (default) instance tenancy
- (C) The instances launched by both Launch Template LT1 and Launch Template LT2 will have dedicated instance tenancy
- (D) The instances launched by both Launch Template LT1 and Launch Template LT2 will have default instance tenancy
- (E) Correct option:
- (F) A launch template specifies instance configuration information. It includes the ID of the Amazon Machine Image (AMI), the instance type, a key pair, security groups, and other parameters used to launch EC2 instances. If you've launched an EC2 instance before, you specified the same information to launch the instance.
- (G) When you create a Launch Template, the default value for the instance tenancy is shared and the instance tenancy is controlled by the tenancy attribute of the VPC. If you set the Launch Template Tenancy to shared (default) and the VPC Tenancy is set to dedicated, then the instances have dedicated tenancy. If you set the Launch Template Tenancy to dedicated and the VPC Tenancy is set to default, then again the instances have dedicated tenancy.
- (H) Amazon EC2 provides three options for the tenancy of your EC2 instances:
- (I) Shared (Shared) – Multiple AWS accounts may share the same physical hardware. This is the default tenancy option when launching an instance.
- (J) Dedicated instances (Dedicated) – Your instance runs on single-tenant hardware. No other AWS customer shares the same physical server.
- () Dedicated Hosts (Dedicated host) – The instance runs on a physical server that is dedicated to your use. Using Dedicated Hosts makes it easier to bring your own licenses (BYOL) that have dedicated hardware requirements to EC2 and meet compliance use cases. If you choose this option, you must provide a host resource group for Tenancy host resource group.
- () Incorrect options:
- () The instances launched by Launch Template LT1 will have dedicated instance tenancy while the instances launched by the Launch Template LT2 will have shared (default) instance tenancy - If either Launch Template Tenancy or VPC Tenancy is set to dedicated, then the instance tenancy is also dedicated. Therefore, this option is incorrect.
- () The instances launched by Launch Template LT1 will have default instance tenancy while the instances launched by the Launch Template LT2 will have dedicated instance tenancy - If either Launch Template Tenancy or VPC Tenancy is set to dedicated, then the instance tenancy is also dedicated. Therefore, this option is incorrect.
- () The instances launched by both Launch Template LT1 and Launch Template LT2 will have default instance tenancy - If either Launch Template Tenancy or VPC Tenancy is set to dedicated, then the instance tenancy is also dedicated. Therefore, this option is incorrect.
- () Reference:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/advanced-settings-for-your-launch-template.html
- () Which combination of solutions will best fulfill these requirements with the least amount of operational overhead? (Select two)
- () Create individual Site-to-Site VPN connections from the data center to each VPC. Set up BGP route propagation for every tunnel to facilitate on-premises-to-VPC routing
- () Convert each existing private VIF into a new Direct Connect gateway association by attaching a virtual private gateway (VGW) to each VPC. Manually configure routing between VGWs
- () Correct selection
- () Create an AWS Transit Gateway and attach all 25 VPCs to it. Enable route propagation for each attachment to automatically manage inter-VPC routing
- () Reconfigure each VPC to connect through AWS PrivateLink endpoints to a central networking service VPC. Share the service with other VPCs using VPC endpoint services
- () Create a transit virtual interface (VIF) from the Direct Connect connection and associate it with the transit gateway
- () Correct options:
- () Attaching all VPCs to a single AWS Transit Gateway centralizes routing and allows for transitive communication between the VPCs. Enabling route propagation eliminates the need to manually update route tables for every VPC. This design supports scalable, full-mesh VPC connectivity with low operational burden.
- () via - https://docs.aws.amazon.com/whitepapers/latest/hybrid-connectivity/aws-dx-dxgw-with-vgw-multi-regions-and-aws-public-peering.html
- () Using a transit VIF from the Direct Connect connection to the transit gateway enables on-premises-to-VPC connectivity through a single, centralized path. This eliminates the need to maintain multiple private VIFs and simplifies BGP management and route aggregation. Combined with Option A, this forms a highly efficient hub-and-spoke architecture.
- () Create individual Site-to-Site VPN connections from the data center to each VPC. Set up BGP route propagation for every tunnel to facilitate on-premises-to-VPC routing - Creating 25 individual VPN connections adds significant operational complexity, introduces higher latency, and does not make use of the existing high-throughput Direct Connect connection. While VPNs can provide connectivity, they are inferior in performance and scalability for this use case.
- () Reconfigure each VPC to connect through AWS PrivateLink endpoints to a central networking service VPC. Share the service with other VPCs using VPC endpoint services - AWS PrivateLink is used to expose services privately, not to enable full VPC-to-VPC or on-premises routing. It supports one-way access to a specific service, and cannot be used to facilitate general network-level communication between all VPCs and the data center.
- () References:
- () https://aws.amazon.com/transit-gateway/
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/WorkingWithVirtualInterfaces.html
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html
- () https://docs.aws.amazon.com/whitepapers/latest/hybrid-connectivity/aws-dx-dxgw-with-vgw-multi-regions-and-aws-public-peering.html
- () A legacy application is built using a tightly-coupled monolithic architecture. Due to a sharp increase in the number of users, the application performance has degraded. The company now wants to decouple the architecture and adopt AWS microservices architecture. Some of these microservices need to handle fast running processes whereas other microservices need to handle slower processes.
- () Which of these options would you identify as the right way of connecting these microservices?
- () Add Amazon EventBridge to decouple the complex architecture
- **() Configure Amazon Simple Queue Service (Amazon SQS) queue to decouple microservices running faster processes from the microservices running slower ones** [CORRECT]
- () Use Amazon Simple Notification Service (Amazon SNS) to decouple microservices running faster processes from the microservices running slower ones

**Answer:**
Correct Answer: **Configure Amazon Simple Queue Service (Amazon SQS) queue to decouple microservices running faster processes from the microservices running slower ones**

---

## Question 4

**Q:** Which combination of solutions will best fulfill these requirements with the least amount of operational overhead? (Select two)

**Options:**
- (A) Create individual Site-to-Site VPN connections from the data center to each VPC. Set up BGP route propagation for every tunnel to facilitate on-premises-to-VPC routing
- (B) Convert each existing private VIF into a new Direct Connect gateway association by attaching a virtual private gateway (VGW) to each VPC. Manually configure routing between VGWs
- (C) Correct selection
- (D) Create an AWS Transit Gateway and attach all 25 VPCs to it. Enable route propagation for each attachment to automatically manage inter-VPC routing
- (E) Reconfigure each VPC to connect through AWS PrivateLink endpoints to a central networking service VPC. Share the service with other VPCs using VPC endpoint services
- (F) Create a transit virtual interface (VIF) from the Direct Connect connection and associate it with the transit gateway
- (G) Correct options:
- (H) Attaching all VPCs to a single AWS Transit Gateway centralizes routing and allows for transitive communication between the VPCs. Enabling route propagation eliminates the need to manually update route tables for every VPC. This design supports scalable, full-mesh VPC connectivity with low operational burden.
- (I) via - https://docs.aws.amazon.com/whitepapers/latest/hybrid-connectivity/aws-dx-dxgw-with-vgw-multi-regions-and-aws-public-peering.html
- (J) Using a transit VIF from the Direct Connect connection to the transit gateway enables on-premises-to-VPC connectivity through a single, centralized path. This eliminates the need to maintain multiple private VIFs and simplifies BGP management and route aggregation. Combined with Option A, this forms a highly efficient hub-and-spoke architecture.
- () Incorrect options:
- () Create individual Site-to-Site VPN connections from the data center to each VPC. Set up BGP route propagation for every tunnel to facilitate on-premises-to-VPC routing - Creating 25 individual VPN connections adds significant operational complexity, introduces higher latency, and does not make use of the existing high-throughput Direct Connect connection. While VPNs can provide connectivity, they are inferior in performance and scalability for this use case.
- () Reconfigure each VPC to connect through AWS PrivateLink endpoints to a central networking service VPC. Share the service with other VPCs using VPC endpoint services - AWS PrivateLink is used to expose services privately, not to enable full VPC-to-VPC or on-premises routing. It supports one-way access to a specific service, and cannot be used to facilitate general network-level communication between all VPCs and the data center.
- () References:
- () https://aws.amazon.com/transit-gateway/
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/WorkingWithVirtualInterfaces.html
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html
- () https://docs.aws.amazon.com/whitepapers/latest/hybrid-connectivity/aws-dx-dxgw-with-vgw-multi-regions-and-aws-public-peering.html
- () A legacy application is built using a tightly-coupled monolithic architecture. Due to a sharp increase in the number of users, the application performance has degraded. The company now wants to decouple the architecture and adopt AWS microservices architecture. Some of these microservices need to handle fast running processes whereas other microservices need to handle slower processes.
- () Which of these options would you identify as the right way of connecting these microservices?
- () Add Amazon EventBridge to decouple the complex architecture
- **() Configure Amazon Simple Queue Service (Amazon SQS) queue to decouple microservices running faster processes from the microservices running slower ones** [CORRECT]
- () Use Amazon Simple Notification Service (Amazon SNS) to decouple microservices running faster processes from the microservices running slower ones
- () Configure Amazon Kinesis Data Streams to decouple microservices running faster processes from the microservices running slower ones
- () Correct option:
- ()  mechanism. This is an important difference between Amazon SNS and Amazon SQS. Whereas Amazon SQS is a polling mechanism, that gives applications the chance to poll at their own comfort, the push mechanism assumes the other applications are present. For the current requirement, we need messages to be stored till they are processed by the downstream applications. Hence, Amazon SQS is the right choice.
- () Configure Amazon Kinesis Data Streams to decouple microservices running faster processes from the microservices running slower ones - Amazon Kinesis Data Streams are used for streaming real-time high-volume data. Amazon Kinesis is a publish-subscribe model, used when publisher applications need to publish the same data to different consumers in parallel. Amazon SQS is the right fit for the current use case.
- () Add Amazon EventBridge to decouple the complex architecture - This event-based service is extremely useful for connecting non-AWS SaaS (Software as a Service) services to AWS services. With Amazon Eventbridge, the downstream application would need to immediately process the events whenever they arrive, thereby making it a tightly coupled scenario. Hence, this option is not correct.
- () https://aws.amazon.com/sqs/
- () Which options would you combine to build a solution to meet these requirements? (Select two)
- () Create an AWS WAF ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon CloudFront distribution
- () Create a new NACL that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new NACL with the Amazon CloudFront distribution
- () Create a new security group that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new security group with the Amazon CloudFront distribution
- () Configure an origin access identity (OAI) and associate it with the Amazon CloudFront distribution. Set up the permissions in the Amazon S3 bucket policy so that only the OAI can read the objects
- () Create an AWS Web Application Firewall (AWS WAF) ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon S3 bucket policy

**Answer:**
Correct Answer: **Configure Amazon Simple Queue Service (Amazon SQS) queue to decouple microservices running faster processes from the microservices running slower ones**

---

## Question 5

**Q:** Which of these options would you identify as the right way of connecting these microservices?

**Options:**
- (A) Add Amazon EventBridge to decouple the complex architecture
- **(B) Configure Amazon Simple Queue Service (Amazon SQS) queue to decouple microservices running faster processes from the microservices running slower ones** [CORRECT]
- (C) Use Amazon Simple Notification Service (Amazon SNS) to decouple microservices running faster processes from the microservices running slower ones
- (D) Configure Amazon Kinesis Data Streams to decouple microservices running faster processes from the microservices running slower ones
- (E) Correct option:
- (F) Incorrect options:
- (G)  mechanism. This is an important difference between Amazon SNS and Amazon SQS. Whereas Amazon SQS is a polling mechanism, that gives applications the chance to poll at their own comfort, the push mechanism assumes the other applications are present. For the current requirement, we need messages to be stored till they are processed by the downstream applications. Hence, Amazon SQS is the right choice.
- (H) Configure Amazon Kinesis Data Streams to decouple microservices running faster processes from the microservices running slower ones - Amazon Kinesis Data Streams are used for streaming real-time high-volume data. Amazon Kinesis is a publish-subscribe model, used when publisher applications need to publish the same data to different consumers in parallel. Amazon SQS is the right fit for the current use case.
- (I) Add Amazon EventBridge to decouple the complex architecture - This event-based service is extremely useful for connecting non-AWS SaaS (Software as a Service) services to AWS services. With Amazon Eventbridge, the downstream application would need to immediately process the events whenever they arrive, thereby making it a tightly coupled scenario. Hence, this option is not correct.
- (J) References:
- () https://aws.amazon.com/sqs/
- () Which options would you combine to build a solution to meet these requirements? (Select two)
- () Correct selection
- () Create an AWS WAF ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon CloudFront distribution
- () Create a new NACL that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new NACL with the Amazon CloudFront distribution
- () Create a new security group that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new security group with the Amazon CloudFront distribution
- () Configure an origin access identity (OAI) and associate it with the Amazon CloudFront distribution. Set up the permissions in the Amazon S3 bucket policy so that only the OAI can read the objects
- () Create an AWS Web Application Firewall (AWS WAF) ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon S3 bucket policy
- () Correct options:
- () When you use Amazon CloudFront with an Amazon S3 bucket as the origin, you can configure Amazon CloudFront and Amazon S3 in a way that provides the following benefits:
- () Restricts access to the Amazon S3 bucket so that it's not publicly accessible
- () Makes sure that viewers (users) can access the content in the bucket only through the specified Amazon CloudFront distribution—that is, prevents them from accessing the content directly from the bucket, or through an unintended CloudFront distribution.
- () To do this, configure Amazon CloudFront to send authenticated requests to Amazon S3, and configure Amazon S3 to only allow access to authenticated requests from Amazon CloudFront. Amazon CloudFront provides two ways to send authenticated requests to an Amazon S3 origin: origin access control (OAC) and origin access identity (OAI).
- () Exam Alert:
- () Please note that AWS recommends using OAC because it supports:
- () All Amazon S3 buckets in all AWS Regions, including opt-in Regions launched after December 2022
- () Amazon S3 server-side encryption with AWS KMS (SSE-KMS)
- () Dynamic requests (POST, PUT, etc.) to Amazon S3
- () OAI doesn't work for the scenarios in the preceding list, or it requires extra workarounds in those scenarios. However, you will continue to see answers enlisting OAI as the preferred option in the actual exam as it takes about 6 months/1 year for a new feature to appear in the exam.
- () AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to your protected web application resources. You can protect the following resource types:
- () Amazon CloudFront distribution
- () Amazon API Gateway REST API
- () Application Load Balancer
- () AWS AppSync GraphQL API
- () Amazon Cognito user pool
- () AWS WAF also lets you control access to your content. Based on conditions that you specify, such as the IP addresses that requests originate from or the values of query strings, your protected resource responds to requests either with the requested content, with an HTTP 403 status code (Forbidden), or with a custom response.
- () If you want to allow or block web requests based on the IP addresses that the requests originate from, create one or more IP match conditions via your AWS WAF. An IP match condition lists up to 10,000 IP addresses or IP address ranges that your requests originate from.
- () For the given use case, you should add those IP addresses that are allowed in the Amazon EC2 security group into the IP match condition.
- () Create an AWS Web Application Firewall (AWS WAF) ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon S3 bucket policy - You cannot associate an AWS WAF ACL with an Amazon S3 bucket policy.
- () Create a new NACL that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new NACL with the Amazon CloudFront distribution - NACL is associated with a subnet within a VPC. Amazon CloudFront delivers your content through a worldwide network of data centers called edge locations. So a NACL cannot be associated with a Amazon CloudFront distribution.
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/classic-web-acl-ip-conditions.html

**Answer:**
Correct Answer: **Configure Amazon Simple Queue Service (Amazon SQS) queue to decouple microservices running faster processes from the microservices running slower ones**

---

## Question 6

**Q:** Which options would you combine to build a solution to meet these requirements? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Create an AWS WAF ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon CloudFront distribution
- (C) Create a new NACL that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new NACL with the Amazon CloudFront distribution
- (D) Create a new security group that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new security group with the Amazon CloudFront distribution
- (E) Configure an origin access identity (OAI) and associate it with the Amazon CloudFront distribution. Set up the permissions in the Amazon S3 bucket policy so that only the OAI can read the objects
- (F) Create an AWS Web Application Firewall (AWS WAF) ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon S3 bucket policy
- (G) Correct options:
- (H) When you use Amazon CloudFront with an Amazon S3 bucket as the origin, you can configure Amazon CloudFront and Amazon S3 in a way that provides the following benefits:
- (I) Restricts access to the Amazon S3 bucket so that it's not publicly accessible
- (J) Makes sure that viewers (users) can access the content in the bucket only through the specified Amazon CloudFront distribution—that is, prevents them from accessing the content directly from the bucket, or through an unintended CloudFront distribution.
- () To do this, configure Amazon CloudFront to send authenticated requests to Amazon S3, and configure Amazon S3 to only allow access to authenticated requests from Amazon CloudFront. Amazon CloudFront provides two ways to send authenticated requests to an Amazon S3 origin: origin access control (OAC) and origin access identity (OAI).
- () Exam Alert:
- () Please note that AWS recommends using OAC because it supports:
- () All Amazon S3 buckets in all AWS Regions, including opt-in Regions launched after December 2022
- () Amazon S3 server-side encryption with AWS KMS (SSE-KMS)
- () Dynamic requests (POST, PUT, etc.) to Amazon S3
- () OAI doesn't work for the scenarios in the preceding list, or it requires extra workarounds in those scenarios. However, you will continue to see answers enlisting OAI as the preferred option in the actual exam as it takes about 6 months/1 year for a new feature to appear in the exam.
- () AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to your protected web application resources. You can protect the following resource types:
- () Amazon CloudFront distribution
- () Amazon API Gateway REST API
- () Application Load Balancer
- () AWS AppSync GraphQL API
- () Amazon Cognito user pool
- () AWS WAF also lets you control access to your content. Based on conditions that you specify, such as the IP addresses that requests originate from or the values of query strings, your protected resource responds to requests either with the requested content, with an HTTP 403 status code (Forbidden), or with a custom response.
- () If you want to allow or block web requests based on the IP addresses that the requests originate from, create one or more IP match conditions via your AWS WAF. An IP match condition lists up to 10,000 IP addresses or IP address ranges that your requests originate from.
- () For the given use case, you should add those IP addresses that are allowed in the Amazon EC2 security group into the IP match condition.
- () Incorrect options:
- () Create an AWS Web Application Firewall (AWS WAF) ACL and use an IP match condition to allow traffic only from those IPs that are allowed in the Amazon EC2 security group. Associate this new AWS WAF ACL with the Amazon S3 bucket policy - You cannot associate an AWS WAF ACL with an Amazon S3 bucket policy.
- () Create a new NACL that allows traffic from the same IPs as specified in the current Amazon EC2 security group. Associate this new NACL with the Amazon CloudFront distribution - NACL is associated with a subnet within a VPC. Amazon CloudFront delivers your content through a worldwide network of data centers called edge locations. So a NACL cannot be associated with a Amazon CloudFront distribution.
- () References:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/classic-web-acl-ip-conditions.html
- () A big data analytics company is working on a real-time vehicle tracking solution. The data processing workflow involves both I/O intensive and throughput intensive database workloads. The development team needs to store this real-time data in a NoSQL database hosted on an Amazon EC2 instance and needs to support up to 25,000 IOPS per volume.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 7

**Q:** As a solutions architect, which of the following Amazon Elastic Block Store (Amazon EBS) volume types would you recommend for this use-case?

**Options:**
- (A) Cold HDD (sc1)
- (B) Throughput Optimized HDD (st1)
- (C) General Purpose SSD (gp2)
- **(D) Provisioned IOPS SSD (io1)** [CORRECT]
- (E) Correct option:
- (F) Incorrect options:
- (G) General Purpose SSD (gp2) - gp2 is backed by solid-state drives (SSDs) and is suitable for a broad range of transactional workloads, including dev/test environments, low-latency interactive applications, and boot volumes. It supports max IOPS/Volume of 16,000.
- (H) Cold HDD (sc1) - sc1 is backed by hard disk drives (HDDs). It is ideal for less frequently accessed workloads with large, cold datasets. It supports max IOPS/Volume of 250.
- (I) Throughput Optimized HDD (st1) - st1 is backed by hard disk drives (HDDs) and is ideal for frequently accessed, throughput-intensive workloads with large datasets and large I/O sizes, such as MapReduce, Kafka, log processing, data warehouse, and ETL workloads. It supports max IOPS/Volume of 500.
- (J) Reference:
- () https://aws.amazon.com/ebs/volume-types/

**Answer:**
Correct Answer: **Provisioned IOPS SSD (io1)**

---

## Question 8

**Q:** As a solutions architect, which of the following would you suggest resolving this issue?

**Options:**
- **(A) Use Availability Zone (AZ) ID to uniquely identify the Availability Zones across the two AWS Accounts** [CORRECT]
- (B) Use the default subnet to uniquely identify the Availability Zones across the two AWS Accounts
- (C) Use the default VPC to uniquely identify the Availability Zones across the two AWS Accounts
- (D) Reach out to AWS Support for creating the Amazon EC2 instances in the same Availability Zone (AZ) across the two AWS accounts
- (E) Correct option:
- (F) An Availability Zone is represented by a region code followed by a letter identifier; for example, us-east-1a. To ensure that resources are distributed across the Availability Zones for a region, AWS maps Availability Zones to names for each AWS account. For example, the Availability Zone us-west-2a for one AWS account might not be the same location as us-west-2a for another AWS account.
- (G) To coordinate Availability Zones across accounts, you must use the AZ ID, which is a unique and consistent identifier for an Availability Zone. For example, usw2-az2 is an AZ ID for the us-west-2 region and it has the same location in every AWS account.
- (H) Viewing AZ IDs enables you to determine the location of resources in one account relative to the resources in another account. For example, if you share a subnet in the Availability Zone with the AZ ID usw2-az2 with another account, this subnet is available to that account in the Availability Zone whose AZ ID is also usw2-az2.
- (I) You can view the AZ IDs by going to the service health section of the Amazon EC2 Dashboard via your AWS Management Console.
- (J) Availability Zone (AZ) IDs for Availability Zones:
- () Incorrect options:
- () Use the default VPC to uniquely identify the Availability Zones across the two AWS Accounts - A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. Since a VPC spans an AWS region, it cannot be used to uniquely identify an Availability Zone. Therefore, this option is incorrect.
- () Use the default subnet to uniquely identify the Availability Zones across the two AWS Accounts - A subnet is a range of IP addresses in your VPC. A subnet spans an Availability Zone of an AWS region. The default subnet representing the Availability Zone us-west-2a for one AWS account might not be the same location as us-west-2a for another AWS account. Therefore, this option is incorrect.
- () Reach out to AWS Support for creating the Amazon EC2 instances in the same Availability Zone (AZ) across the two AWS accounts - Since the AZ ID is a unique and consistent identifier for an Availability Zone, there is no need to contact AWS Support. Therefore, this option is incorrect.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html
- () An IT training company hosted its website on Amazon S3 a couple of years ago. Due to COVID-19 related travel restrictions, the training website has suddenly gained traction. With an almost 300% increase in the requests served per day, the company's AWS costs have sky-rocketed for just the Amazon S3 outbound data costs.

**Answer:**
Correct Answer: **Use Availability Zone (AZ) ID to uniquely identify the Availability Zones across the two AWS Accounts**

---

## Question 9

**Q:** As a Solutions Architect, can you suggest an alternate method to reduce costs while keeping the latency low?

**Options:**
- (A) Configure Amazon S3 Batch Operations to read data in bulk at one go, to reduce the number of calls made to Amazon S3 buckets
- (B) To reduce Amazon S3 cost, the data can be saved on an Amazon EBS volume connected to an Amazon EC2 instance that can host the application
- (C) Use Amazon EFS service, as it provides a shared, scalable, fully managed elastic NFS file system for storing AWS Cloud or on-premises data
- (D) Configure Amazon CloudFront to distribute the data hosted on Amazon S3 cost-effectively
- (E) Correct option:
- (F) Storing content with Amazon S3 provides a lot of advantages. But to help optimize your application’s performance and security while effectively managing cost, AWS recommends that you also set up Amazon CloudFront to work with your Amazon S3 bucket to serve and protect the content.
- (G) Amazon CloudFront is a content delivery network (CDN) service that delivers static and dynamic web content, video streams, and APIs around the world, securely and at scale. By design, delivering data out of Amazon CloudFront can be more cost-effective than delivering it from Amazon S3 directly to your users.
- (H) Amazon CloudFront serves content through a worldwide network of data centers called Edge Locations. Using edge servers to cache and serve content improves performance by providing content closer to where viewers are located. Amazon CloudFront has edge servers in locations all around the world.
- (I) By caching your content in Edge Locations, Amazon CloudFront reduces the load on your Amazon S3 bucket and helps ensure a faster response for your users when they request content. Also, data transfer out for content by using CloudFront is often more cost-effective than serving files directly from Amazon S3, and there is no data transfer fee from Amazon S3 to CloudFront. You only pay for what is delivered to the internet from Amazon CloudFront, plus request fees.
- (J) Incorrect options:
- () To reduce Amazon S3 cost, the data can be saved on an Amazon EBS volume connected to an Amazon EC2 instance that can host the application - Amazon EBS volumes are fast and are relatively cheap (though Amazon S3 is still a cheaper alternative). But, Amazon EBS volumes are accessible only through Amazon EC2 instances and are bound to a specific region.
- () Use Amazon EFS service, as it provides a shared, scalable, fully managed elastic NFS file system for storing AWS Cloud or on-premises data - Amazon EFS is a shareable file system that can be mounted onto Amazon EC2 instances. Amazon EFS is costlier than Amazon EBS and not a solution if the company is looking at reducing costs.
- () Configure Amazon S3 Batch Operations to read data in bulk at one go, to reduce the number of calls made to Amazon S3 buckets - This statement is incorrect and given only as a distractor. You can use Amazon S3 Batch Operations to perform large-scale batch operations on Amazon S3 objects, and it has nothing to do with content distribution.
- () Reference:
- () https://aws.amazon.com/blogs/networking-and-content-delivery/amazon-s3-amazon-cloudfront-a-match-made-in-the-cloud/
- () A startup is building a serverless microservices architecture where client applications (web and mobile) authenticate users via a third-party OIDC-compliant identity provider. The backend APIs must validate JSON Web Tokens (JWTs) issued by this provider, enforce scope-based access control, and be cost-effective with minimal latency. The development team wants to use a fully managed service that supports JWT validation natively, without writing custom authentication logic.
- () Which solution should the team implement to meet these requirements?
- () Deploy a gRPC backend on Amazon ECS Fargate and expose it through AWS App Runner, handling JWT validation inside the containerized services
- () Use Amazon API Gateway REST API with a Lambda function that manually validates JWT tokens
- () Use Amazon API Gateway WebSocket API with JWT claims validated by a Lambda authorizer
- () Use Amazon API Gateway HTTP API with a native JWT authorizer configured to validate tokens from the OIDC provider
- () Deploy a gRPC backend on Amazon ECS Fargate and expose it through AWS App Runner, handling JWT validation inside the containerized services - Deploying a gRPC backend on ECS Fargate and handling JWT validation within the container logic shifts the responsibility of authentication to the application layer, which increases complexity and violates the requirement for a fully managed JWT validation solution.
- () References:
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-jwt-authorizer.html
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-use-lambda-authorizer.html
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-lambda-auth.html
- () A financial services firm runs a containerized risk analytics tool in its on-premises data center using Docker. The tool depends on persistent data storage for maintaining customer simulation results and operates on a single host machine where the volume is locally mounted. The infrastructure team is looking to replatform the tool to AWS using a fully managed service because they want to avoid managing EC2 instances, volumes, or underlying servers.
- () Which AWS solution best meets these requirements?
- () Use AWS Lambda with a container image runtime. Store stateful data in temporary local storage (/tmp) and sync with Amazon S3 periodically
- () Use Amazon EKS with managed node groups. Provision an Amazon EBS volume and mount it inside the container by creating a Kubernetes persistent volume and claim. Manage storage lifecycle manually
- () Use Amazon ECS with Fargate launch type. Attach an Amazon S3 bucket using a shared access script that mounts the S3 bucket into the container for data storage
- **() Use Amazon ECS with Fargate launch type. Provision an Amazon Elastic File System (Amazon EFS) file system. Mount the EFS volume inside the container at runtime to provide persistent storage access** [CORRECT]
- () This is the most suitable and fully managed solution. ECS with Fargate allows you to run containers without managing EC2 infrastructure, and it integrates natively with Amazon EFS to support persistent, shared storage for stateful applications. You define the EFS volume in the task definition and mount it to the container, allowing multiple tasks to access shared data. This setup requires no server or storage lifecycle management and aligns perfectly with the company's requirements.
- () Use Amazon EKS with managed node groups. Provision an Amazon EBS volume and mount it inside the container by creating a Kubernetes persistent volume and claim. Manage storage lifecycle manually - Although EKS supports Kubernetes-native persistent storage with EBS volumes, this approach still requires provisioning and managing EC2 instances and storage volumes, which contradicts the requirement to avoid managing infrastructure.
- () Use Amazon ECS with Fargate launch type. Attach an Amazon S3 bucket using a shared access script that mounts the S3 bucket into the container for data storage - Amazon S3 is object storage, not a block or file system, and cannot be mounted directly into a container like a file system volume. While applications can access S3 via API, this does not fulfill the requirement for a persistent storage volume that functions like a mounted file system.

**Answer:**
Correct Answer: **Use Amazon ECS with Fargate launch type. Provision an Amazon Elastic File System (Amazon EFS) file system. Mount the EFS volume inside the container at runtime to provide persistent storage access**

---

## Question 10

**Q:** Which solution should the team implement to meet these requirements?

**Options:**
- (A) Deploy a gRPC backend on Amazon ECS Fargate and expose it through AWS App Runner, handling JWT validation inside the containerized services
- (B) Use Amazon API Gateway REST API with a Lambda function that manually validates JWT tokens
- (C) Use Amazon API Gateway WebSocket API with JWT claims validated by a Lambda authorizer
- (D) Use Amazon API Gateway HTTP API with a native JWT authorizer configured to validate tokens from the OIDC provider
- (E) Correct option:
- (F) Incorrect options:
- (G) Deploy a gRPC backend on Amazon ECS Fargate and expose it through AWS App Runner, handling JWT validation inside the containerized services - Deploying a gRPC backend on ECS Fargate and handling JWT validation within the container logic shifts the responsibility of authentication to the application layer, which increases complexity and violates the requirement for a fully managed JWT validation solution.
- (H) References:
- (I) https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-jwt-authorizer.html
- (J) https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-use-lambda-authorizer.html
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-lambda-auth.html
- () A financial services firm runs a containerized risk analytics tool in its on-premises data center using Docker. The tool depends on persistent data storage for maintaining customer simulation results and operates on a single host machine where the volume is locally mounted. The infrastructure team is looking to replatform the tool to AWS using a fully managed service because they want to avoid managing EC2 instances, volumes, or underlying servers.
- () Which AWS solution best meets these requirements?
- () Use AWS Lambda with a container image runtime. Store stateful data in temporary local storage (/tmp) and sync with Amazon S3 periodically
- () Use Amazon EKS with managed node groups. Provision an Amazon EBS volume and mount it inside the container by creating a Kubernetes persistent volume and claim. Manage storage lifecycle manually
- () Use Amazon ECS with Fargate launch type. Attach an Amazon S3 bucket using a shared access script that mounts the S3 bucket into the container for data storage
- () Use Amazon ECS with Fargate launch type. Provision an Amazon Elastic File System (Amazon EFS) file system. Mount the EFS volume inside the container at runtime to provide persistent storage access
- () This is the most suitable and fully managed solution. ECS with Fargate allows you to run containers without managing EC2 infrastructure, and it integrates natively with Amazon EFS to support persistent, shared storage for stateful applications. You define the EFS volume in the task definition and mount it to the container, allowing multiple tasks to access shared data. This setup requires no server or storage lifecycle management and aligns perfectly with the company's requirements.
- () Use Amazon EKS with managed node groups. Provision an Amazon EBS volume and mount it inside the container by creating a Kubernetes persistent volume and claim. Manage storage lifecycle manually - Although EKS supports Kubernetes-native persistent storage with EBS volumes, this approach still requires provisioning and managing EC2 instances and storage volumes, which contradicts the requirement to avoid managing infrastructure.
- () Use Amazon ECS with Fargate launch type. Attach an Amazon S3 bucket using a shared access script that mounts the S3 bucket into the container for data storage - Amazon S3 is object storage, not a block or file system, and cannot be mounted directly into a container like a file system volume. While applications can access S3 via API, this does not fulfill the requirement for a persistent storage volume that functions like a mounted file system.
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/efs-volumes.html
- () https://aws.amazon.com/blogs/containers/developers-guide-to-using-amazon-efs-with-amazon-ecs-and-aws-fargate-part-1/
- () https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html
- () https://docs.aws.amazon.com/lambda/latest/dg/lambda-runtime-environment.html
- () A company recently experienced a database outage in its on-premises data center. The company now wants to migrate to a reliable database solution on AWS that minimizes data loss and stores every transaction on at least two nodes.
- () Which of the following solutions meets these requirements?
- **() Set up an Amazon RDS MySQL DB instance with Multi-AZ functionality enabled to synchronously replicate the data** [CORRECT]
- () Set up an Amazon EC2 instance with a MySQL DB engine installed that triggers an AWS Lambda function to synchronously replicate the data to an Amazon RDS MySQL DB instance
- () Set up an Amazon RDS MySQL DB instance and then create a read replica in a separate AWS Region that synchronously replicates the data
- () Set up an Amazon RDS MySQL DB instance and then create a read replica in another Availability Zone that synchronously replicates the data
- () via - https://aws.amazon.com/rds/features/multi-az/

**Answer:**
Correct Answer: **Set up an Amazon RDS MySQL DB instance with Multi-AZ functionality enabled to synchronously replicate the data**

---

## Question 11

**Q:** Which of the following solutions meets these requirements?

**Options:**
- **(A) Set up an Amazon RDS MySQL DB instance with Multi-AZ functionality enabled to synchronously replicate the data** [CORRECT]
- (B) Set up an Amazon EC2 instance with a MySQL DB engine installed that triggers an AWS Lambda function to synchronously replicate the data to an Amazon RDS MySQL DB instance
- (C) Set up an Amazon RDS MySQL DB instance and then create a read replica in a separate AWS Region that synchronously replicates the data
- (D) Set up an Amazon RDS MySQL DB instance and then create a read replica in another Availability Zone that synchronously replicates the data
- (E) Correct option:
- (F) via - https://aws.amazon.com/rds/features/multi-az/
- (G) Incorrect options:
- (H) Both these options talk about creating a read replica that synchronously replicates the data, but in reality, any updates made to the primary DB instance are asynchronously copied to the read replica. So both these options are incorrect.
- (I) via - https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
- (J) References:
- () https://aws.amazon.com/rds/features/multi-az/
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
- () An e-commerce company runs its web application on Amazon EC2 instances in an Auto Scaling group and it's configured to handle consumer orders in an Amazon Simple Queue Service (Amazon SQS) queue for downstream processing. The DevOps team has observed that the performance of the application goes down in case of a sudden spike in orders received.

**Answer:**
Correct Answer: **Set up an Amazon RDS MySQL DB instance with Multi-AZ functionality enabled to synchronously replicate the data**

---

## Question 12

**Q:** Can you recommend an improved and cost-effective way of generating the business reports while keeping the production application unaffected?

**Options:**
- (A) Configure the Amazon RDS instance to be Multi-AZ DB instance, and connect the report generation tool to the DB instance in a different AZ
- (B) Migrate from General Purpose SSD to magnetic storage to enhance IOPS
- (C) Create a read replica and connect the report generation tool/application to it
- (D) Increase the size of Amazon RDS instance
- (E) Correct option:
- (F) There are a variety of scenarios where deploying one or more read replicas for a given source DB instance may make sense. Common reasons for deploying a read replica include:
- (G) 1. Scaling beyond the compute or I/O capacity of a single DB instance for read-heavy database workloads. This excess read traffic can be directed to one or more read replicas.
- (H) 2. Serving read traffic while the source DB instance is unavailable. If your source DB Instance cannot take I/O requests (e.g. due to I/O suspension for backups or scheduled maintenance), you can direct read traffic to your read replica(s). For this use case, keep in mind that the data on the read replica may be “stale” since the source DB Instance is unavailable.
- (I) 3. Business reporting or data warehousing scenarios; you may want business reporting queries to run against a read replica, rather than your primary, production DB Instance.
- (J) 4. You may use a read replica for disaster recovery of the source DB instance, either in the same AWS Region or in another Region.
- () Comparing Read Replicas with Multi-AZ and Multi-Region Amazon RDS deployments:
- () via - https://aws.amazon.com/rds/features/read-replicas/
- () Incorrect options:
- () Increase the size of Amazon RDS instance - This will not help as it's mentioned that the CPU, memory, and storage are running at only 50% of the total capacity.
- () Migrate from General Purpose SSD to magnetic storage to enhance IOPS - This is incorrect. Amazon RDS supports magnetic storage for backward compatibility only. AWS recommends that you use General Purpose SSD or Provisioned IOPS for any storage needs.
- () Reference:
- () https://aws.amazon.com/rds/features/read-replicas/
- () An engineering lead is designing a VPC with public and private subnets. The VPC and subnets use IPv4 CIDR blocks. There is one public subnet and one private subnet in each of three Availability Zones (AZs) for high availability. An internet gateway is used to provide internet access for the public subnets. The private subnets require access to the internet to allow Amazon EC2 instances to download software updates.
- () Which of the following options represents the correct solution to set up internet access for the private subnets?
- () Set up three egress-only internet gateways, one in each public subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the egress-only internet gateway in its AZ
- () Set up three NAT gateways, one in each public subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the NAT gateway in its AZ
- () Set up three NAT gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the NAT gateway in its AZ
- () Set up three Internet gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the Internet gateway in its AZ
- () You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.
- () Each NAT gateway is created in a specific Availability Zone and implemented with redundancy in that zone.
- () If you have resources in multiple Availability Zones and they share one NAT gateway, and if the NAT gateway’s Availability Zone is down, resources in the other Availability Zones lose internet access. To create an Availability Zone-independent architecture, create a NAT gateway in each Availability Zone and configure your routing to ensure that resources use the NAT gateway in the same Availability Zone.
- () How NAT gateway works:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () Set up three NAT gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the NAT gateway in its AZ - NAT gateways need to be set up in public subnets, so this option is incorrect.
- () Set up three Internet gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the Internet gateway in its AZ - Internet gateways cannot be provisioned in private subnets of a VPC.
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () An online gaming application has a large chunk of its traffic coming from users who download static assets such as historic leaderboard reports and the game tactics for various games. The current infrastructure and design are unable to cope up with the traffic and application freezes on most of the pages.
- () Which of the following is a cost-optimal solution that does not need provisioning of infrastructure?
- **() Use Amazon CloudFront with Amazon S3 as the storage solution for the static assets** [CORRECT]
- () Configure AWS Lambda with an Amazon RDS database to provide a serverless architecture

**Answer:**
Correct Answer: **Use Amazon CloudFront with Amazon S3 as the storage solution for the static assets**

---

## Question 13

**Q:** Which of the following options represents the correct solution to set up internet access for the private subnets?

**Options:**
- (A) Set up three egress-only internet gateways, one in each public subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the egress-only internet gateway in its AZ
- (B) Set up three NAT gateways, one in each public subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the NAT gateway in its AZ
- (C) Set up three NAT gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the NAT gateway in its AZ
- (D) Set up three Internet gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the Internet gateway in its AZ
- (E) Correct option:
- (F) You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances.
- (G) Each NAT gateway is created in a specific Availability Zone and implemented with redundancy in that zone.
- (H) If you have resources in multiple Availability Zones and they share one NAT gateway, and if the NAT gateway’s Availability Zone is down, resources in the other Availability Zones lose internet access. To create an Availability Zone-independent architecture, create a NAT gateway in each Availability Zone and configure your routing to ensure that resources use the NAT gateway in the same Availability Zone.
- (I) How NAT gateway works:
- (J) via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () Incorrect options:
- () Set up three NAT gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the NAT gateway in its AZ - NAT gateways need to be set up in public subnets, so this option is incorrect.
- () Set up three Internet gateways, one in each private subnet in each AZ. Create a custom route table for each AZ that forwards non-local traffic to the Internet gateway in its AZ - Internet gateways cannot be provisioned in private subnets of a VPC.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () An online gaming application has a large chunk of its traffic coming from users who download static assets such as historic leaderboard reports and the game tactics for various games. The current infrastructure and design are unable to cope up with the traffic and application freezes on most of the pages.
- () Which of the following is a cost-optimal solution that does not need provisioning of infrastructure?
- **() Use Amazon CloudFront with Amazon S3 as the storage solution for the static assets** [CORRECT]
- () Configure AWS Lambda with an Amazon RDS database to provide a serverless architecture
- () Use AWS Lambda with Amazon ElastiCache and Amazon RDS for serving static assets at high speed and low latency
- () Use Amazon CloudFront with Amazon DynamoDB for greater speed and low latency access to static assets
- () By caching your content in Edge Locations, Amazon CloudFront reduces the load on your Amazon S3 bucket and helps ensure a faster response for your users when they request content. Also, data transfer out for content by using Amazon CloudFront is often more cost-effective than serving files directly from Amazon S3, and there is no data transfer fee from Amazon S3 to Amazon CloudFront. You only pay for what is delivered to the internet from Amazon CloudFront, plus request fees.
- () Configure AWS Lambda with an Amazon RDS database to provide a serverless architecture - Amazon RDS is not the right choice for the current scenario because of the overhead of a database management system, as the given use-case can be addressed by using Amazon S3 storage solution.
- () Use Amazon CloudFront with Amazon DynamoDB for greater speed and low latency access to static assets - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. But, Amazon DynamoDB is overkill for the given use-case and will prove to be a very costly solution.
- () Use AWS Lambda with Amazon ElastiCache and Amazon RDS for serving static assets at high speed and low latency - As discussed above, Amazon RDS is not needed for this use case where web application needs to display static pages and facilitate downloads of historic data. Amazon S3 is much better suited for this requirement.
- () https://aws.amazon.com/blogs/networking-and-content-delivery/amazon-s3-amazon-cloudfront-a-match-made-in-the-cloud/
- () An e-commerce company is using Elastic Load Balancing (ELB) for its fleet of Amazon EC2 instances spread across two Availability Zones (AZs), with one instance as a target in Availability Zone A and four instances as targets in Availability Zone B. The company is doing benchmarking for server performance when cross-zone load balancing is enabled compared to the case when cross-zone load balancing is disabled.

**Answer:**
Correct Answer: **Use Amazon CloudFront with Amazon S3 as the storage solution for the static assets**

---

## Question 14

**Q:** Which of the following is a cost-optimal solution that does not need provisioning of infrastructure?

**Options:**
- **(A) Use Amazon CloudFront with Amazon S3 as the storage solution for the static assets** [CORRECT]
- (B) Configure AWS Lambda with an Amazon RDS database to provide a serverless architecture
- (C) Use AWS Lambda with Amazon ElastiCache and Amazon RDS for serving static assets at high speed and low latency
- (D) Use Amazon CloudFront with Amazon DynamoDB for greater speed and low latency access to static assets
- (E) Correct option:
- (F) By caching your content in Edge Locations, Amazon CloudFront reduces the load on your Amazon S3 bucket and helps ensure a faster response for your users when they request content. Also, data transfer out for content by using Amazon CloudFront is often more cost-effective than serving files directly from Amazon S3, and there is no data transfer fee from Amazon S3 to Amazon CloudFront. You only pay for what is delivered to the internet from Amazon CloudFront, plus request fees.
- (G) Incorrect options:
- (H) Configure AWS Lambda with an Amazon RDS database to provide a serverless architecture - Amazon RDS is not the right choice for the current scenario because of the overhead of a database management system, as the given use-case can be addressed by using Amazon S3 storage solution.
- (I) Use Amazon CloudFront with Amazon DynamoDB for greater speed and low latency access to static assets - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. But, Amazon DynamoDB is overkill for the given use-case and will prove to be a very costly solution.
- (J) Use AWS Lambda with Amazon ElastiCache and Amazon RDS for serving static assets at high speed and low latency - As discussed above, Amazon RDS is not needed for this use case where web application needs to display static pages and facilitate downloads of historic data. Amazon S3 is much better suited for this requirement.
- () Reference:
- () https://aws.amazon.com/blogs/networking-and-content-delivery/amazon-s3-amazon-cloudfront-a-match-made-in-the-cloud/
- () An e-commerce company is using Elastic Load Balancing (ELB) for its fleet of Amazon EC2 instances spread across two Availability Zones (AZs), with one instance as a target in Availability Zone A and four instances as targets in Availability Zone B. The company is doing benchmarking for server performance when cross-zone load balancing is enabled compared to the case when cross-zone load balancing is disabled.

**Answer:**
Correct Answer: **Use Amazon CloudFront with Amazon S3 as the storage solution for the static assets**

---

## Question 15

**Q:** As a solutions architect, which of the following traffic distribution outcomes would you identify as correct?

**Options:**
- (A) With cross-zone load balancing enabled, one instance in Availability Zone A receives no traffic and four instances in Availability Zone B receive 25% traffic each. With cross-zone load balancing disabled, one instance in Availability Zone A receives 50% traffic and four instances in Availability Zone B receive 12.5% traffic each
- **(B) With cross-zone load balancing enabled, one instance in Availability Zone A receives 20% traffic and four instances in Availability Zone B receive 20% traffic each. With cross-zone load balancing disabled, one instance in Availability Zone A receives 50% traffic and four instances in Availability Zone B receive 12.5% traffic each** [CORRECT]
- (C) With cross-zone load balancing enabled, one instance in Availability Zone A receives 20% traffic and four instances in Availability Zone B receive 20% traffic each. With cross-zone load balancing disabled, one instance in Availability Zone A receives no traffic and four instances in Availability Zone B receive 25% traffic each
- (D) With cross-zone load balancing enabled, one instance in Availability Zone A receives 50% traffic and four instances in Availability Zone B receive 12.5% traffic each. With cross-zone load balancing disabled, one instance in Availability Zone A receives 20% traffic and four instances in Availability Zone B receive 20% traffic each
- (E) Correct option:
- (F) Consider the following diagrams (the scenario illustrated in the diagrams involves 10 target instances split across 2 AZs) to understand the effect of cross-zone load balancing.
- (G) If cross-zone load balancing is enabled, each of the 10 targets receives 10% of the traffic. This is because each load balancer node can route its 50% of the client traffic to all 10 targets.
- (H) via - https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/how-elastic-load-balancing-works.html
- (I) If cross-zone load balancing is disabled:
- (J) Each of the two targets in Availability Zone A receives 25% of the traffic.
- () Each of the eight targets in Availability Zone B receives 6.25% of the traffic.
- () This is because each load balancer node can route its 50% of the client traffic only to targets in its Availability Zone
- () Incorrect options:
- () These three options contradict the details provided in the explanation above, so these options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/how-elastic-load-balancing-works.html
- () The development team at a retail company wants to optimize the cost of Amazon EC2 instances. The team wants to move certain nightly batch jobs to spot instances. The team has hired you as a solutions architect to provide the initial guidance.
- () Which of the following would you identify as CORRECT regarding the capabilities of spot instances? (Select three)
- () If a spot request is persistent, then it is opened again after you stop the Spot Instance
- () Correct selection
- () Spot Fleets can maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated
- () When you cancel an active spot request, it terminates the associated instance as well
- () When you cancel an active spot request, it does not terminate the associated instance
- () If a spot request is persistent, then it is opened again after your Spot Instance is interrupted
- () Spot Fleets cannot maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated
- () Correct options:
- () A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused Amazon EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. The hourly price for a Spot Instance is called a Spot price. The Spot price of each instance type in each Availability Zone is set by Amazon EC2 and adjusted gradually based on the long-term supply of and demand for Spot Instances.
- () A Spot Instance request is either one-time or persistent. If the spot request is persistent, the request is opened again after your Spot Instance is interrupted. If the request is persistent and you stop your Spot Instance, the request only opens after you start your Spot Instance.
- () How Spot requests work:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-requests.html
- () If your Spot Instance request is active and has an associated running Spot Instance, or your Spot Instance request is disabled and has an associated stopped Spot Instance, canceling the request does not terminate the instance; you must terminate the running Spot Instance manually. Moreover, to cancel a persistent Spot request and terminate its Spot Instances, you must cancel the Spot request first and then terminate the Spot Instances.
- () When you cancel an active spot request, it terminates the associated instance as well - If your Spot Instance request is active and has an associated running Spot Instance, then canceling the request does not terminate the instance; you must terminate the running Spot Instance manually. So, this option is incorrect.
- () If a spot request is persistent, then it is opened again after you stop the Spot Instance - If the request is persistent and you stop your Spot Instance, the request only opens after you start your Spot Instance. So, this option is incorrect.
- () Spot Fleets cannot maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated - As mentioned above, Spot Fleets can maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated.

**Answer:**
Correct Answer: **With cross-zone load balancing enabled, one instance in Availability Zone A receives 20% traffic and four instances in Availability Zone B receive 20% traffic each. With cross-zone load balancing disabled, one instance in Availability Zone A receives 50% traffic and four instances in Availability Zone B receive 12.5% traffic each**

---

## Question 16

**Q:** Which of the following would you identify as CORRECT regarding the capabilities of spot instances? (Select three)

**Options:**
- (A) If a spot request is persistent, then it is opened again after you stop the Spot Instance
- (B) Correct selection
- (C) Spot Fleets can maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated
- (D) When you cancel an active spot request, it terminates the associated instance as well
- (E) When you cancel an active spot request, it does not terminate the associated instance
- (F) If a spot request is persistent, then it is opened again after your Spot Instance is interrupted
- (G) Spot Fleets cannot maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated
- (H) Correct options:
- (I) A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused Amazon EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. The hourly price for a Spot Instance is called a Spot price. The Spot price of each instance type in each Availability Zone is set by Amazon EC2 and adjusted gradually based on the long-term supply of and demand for Spot Instances.
- (J) A Spot Instance request is either one-time or persistent. If the spot request is persistent, the request is opened again after your Spot Instance is interrupted. If the request is persistent and you stop your Spot Instance, the request only opens after you start your Spot Instance.
- () How Spot requests work:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-requests.html
- () If your Spot Instance request is active and has an associated running Spot Instance, or your Spot Instance request is disabled and has an associated stopped Spot Instance, canceling the request does not terminate the instance; you must terminate the running Spot Instance manually. Moreover, to cancel a persistent Spot request and terminate its Spot Instances, you must cancel the Spot request first and then terminate the Spot Instances.
- () Incorrect options:
- () When you cancel an active spot request, it terminates the associated instance as well - If your Spot Instance request is active and has an associated running Spot Instance, then canceling the request does not terminate the instance; you must terminate the running Spot Instance manually. So, this option is incorrect.
- () If a spot request is persistent, then it is opened again after you stop the Spot Instance - If the request is persistent and you stop your Spot Instance, the request only opens after you start your Spot Instance. So, this option is incorrect.
- () Spot Fleets cannot maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated - As mentioned above, Spot Fleets can maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-requests.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-fleet.html
- () An application running on an Amazon EC2 instance needs to access a Amazon DynamoDB table in the same AWS account.
- () Which of the following solutions should a solutions architect configure for the necessary permissions?
- () Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Add the Amazon EC2 instance to the trust relationship policy document so that the instance can assume the role
- **() Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Configure an instance profile to assign this IAM role to the Amazon EC2 instance** [CORRECT]
- () Set up an IAM user with the appropriate permissions to allow access to the Amazon DynamoDB table. Store the access credentials in the local storage and read them from within the application code directly
- () Set up an IAM user with the appropriate permissions to allow access to the Amazon DynamoDB table. Store the access credentials in an Amazon S3 bucket and read them from within the application code directly
- () Correct option:
- () A service role is an IAM role that a service assumes to perform actions on your behalf. Service roles provide access only within your account and cannot be used to grant access to services in other accounts. An IAM administrator can create, modify, and delete a service role from within IAM. When you create the service role, you define the trusted entity in the definition.
- () If you are going to use the role with Amazon EC2 or another AWS service that uses Amazon EC2, you must store the role in an instance profile. An instance profile is a container for a role that can be attached to an Amazon EC2 instance when launched. An instance profile can contain only one role, and that limit cannot be increased. If you create the role using the AWS Management Console, the instance profile is created for you with the same name as the role.
- () You should never store the IAM access credentials for a user in Amazon S3 or local storage or a database. It's a security bad practice. It is always recommended to use IAM roles to configure access to other AWS resources from Amazon EC2 instances. Therefore both these options are incorrect.
- () Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Add the Amazon EC2 instance to the trust relationship policy document so that the instance can assume the role - There is no need for this option because when you create an IAM service role for Amazon EC2, the role automatically has Amazon EC2 identified as a trusted entity. Therefore this option is not correct.
- () Configuring a Service Role:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-service.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html
- () The DevOps team at a multi-national company is helping its subsidiaries standardize Amazon EC2 instances by using the same Amazon Machine Image (AMI). Some of these subsidiaries are in the same AWS region but use different AWS accounts whereas others are in different AWS regions but use the same AWS account as the parent company. The DevOps team has hired you as a solutions architect for this project.

**Answer:**
Correct Answer: **Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Configure an instance profile to assign this IAM role to the Amazon EC2 instance**

---

## Question 17

**Q:** Which of the following solutions should a solutions architect configure for the necessary permissions?

**Options:**
- (A) Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Add the Amazon EC2 instance to the trust relationship policy document so that the instance can assume the role
- **(B) Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Configure an instance profile to assign this IAM role to the Amazon EC2 instance** [CORRECT]
- (C) Set up an IAM user with the appropriate permissions to allow access to the Amazon DynamoDB table. Store the access credentials in the local storage and read them from within the application code directly
- (D) Set up an IAM user with the appropriate permissions to allow access to the Amazon DynamoDB table. Store the access credentials in an Amazon S3 bucket and read them from within the application code directly
- (E) Correct option:
- (F) A service role is an IAM role that a service assumes to perform actions on your behalf. Service roles provide access only within your account and cannot be used to grant access to services in other accounts. An IAM administrator can create, modify, and delete a service role from within IAM. When you create the service role, you define the trusted entity in the definition.
- (G) If you are going to use the role with Amazon EC2 or another AWS service that uses Amazon EC2, you must store the role in an instance profile. An instance profile is a container for a role that can be attached to an Amazon EC2 instance when launched. An instance profile can contain only one role, and that limit cannot be increased. If you create the role using the AWS Management Console, the instance profile is created for you with the same name as the role.
- (H) Incorrect options:
- (I) You should never store the IAM access credentials for a user in Amazon S3 or local storage or a database. It's a security bad practice. It is always recommended to use IAM roles to configure access to other AWS resources from Amazon EC2 instances. Therefore both these options are incorrect.
- (J) Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Add the Amazon EC2 instance to the trust relationship policy document so that the instance can assume the role - There is no need for this option because when you create an IAM service role for Amazon EC2, the role automatically has Amazon EC2 identified as a trusted entity. Therefore this option is not correct.
- () Configuring a Service Role:
- () References:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-service.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html
- () The DevOps team at a multi-national company is helping its subsidiaries standardize Amazon EC2 instances by using the same Amazon Machine Image (AMI). Some of these subsidiaries are in the same AWS region but use different AWS accounts whereas others are in different AWS regions but use the same AWS account as the parent company. The DevOps team has hired you as a solutions architect for this project.
- () Which of the following would you identify as CORRECT regarding the capabilities of an Amazon Machine Image (AMI)? (Select three)
- () Correct selection
- () You can copy an Amazon Machine Image (AMI) across AWS Regions
- () You can share an Amazon Machine Image (AMI) with another AWS account
- () Copying an Amazon Machine Image (AMI) backed by an encrypted snapshot results in an unencrypted target snapshot
- () Copying an Amazon Machine Image (AMI) backed by an encrypted snapshot cannot result in an unencrypted target snapshot
- () You cannot share an Amazon Machine Image (AMI) with another AWS account
- () You cannot copy an Amazon Machine Image (AMI) across AWS Regions
- () Correct options:
- () An Amazon Machine Image (AMI) provides the information required to launch an instance. An AMI includes the following:
- () One or more Amazon EBS snapshots, or, for instance-store-backed AMIs, a template for the root volume of the instance.
- () Launch permissions that control which AWS accounts can use the AMI to launch instances.
- () A block device mapping that specifies the volumes to attach to the instance when it's launched.
- ()  - is correct.
- () Copying AMIs across regions:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html
- ()  is correct.
- () These three options contradict the details provided in the explanation above.

**Answer:**
Correct Answer: **Set up an IAM service role with the appropriate permissions to allow access to the Amazon DynamoDB table. Configure an instance profile to assign this IAM role to the Amazon EC2 instance**

---

## Question 18

**Q:** Which of the following would you identify as CORRECT regarding the capabilities of an Amazon Machine Image (AMI)? (Select three)

**Options:**
- (A) Correct selection
- (B) You can copy an Amazon Machine Image (AMI) across AWS Regions
- (C) You can share an Amazon Machine Image (AMI) with another AWS account
- (D) Copying an Amazon Machine Image (AMI) backed by an encrypted snapshot results in an unencrypted target snapshot
- (E) Copying an Amazon Machine Image (AMI) backed by an encrypted snapshot cannot result in an unencrypted target snapshot
- (F) You cannot share an Amazon Machine Image (AMI) with another AWS account
- (G) You cannot copy an Amazon Machine Image (AMI) across AWS Regions
- (H) Correct options:
- (I) An Amazon Machine Image (AMI) provides the information required to launch an instance. An AMI includes the following:
- (J) One or more Amazon EBS snapshots, or, for instance-store-backed AMIs, a template for the root volume of the instance.
- () Launch permissions that control which AWS accounts can use the AMI to launch instances.
- () A block device mapping that specifies the volumes to attach to the instance when it's launched.
- ()  - is correct.
- () Copying AMIs across regions:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html
- ()  is correct.
- () Incorrect options:
- () These three options contradict the details provided in the explanation above.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html
- () Which solution will best meet these requirements?
- () Use Amazon EFS with the Standard storage class and mount the file system using NFS from both Windows and Linux instances
- **() Deploy Amazon FSx for Windows File Server and mount it using the SMB protocol from both Windows and Linux EC2 instances** [CORRECT]
- () Create an S3 bucket and mount it on EC2 instances using Mountpoint for Amazon S3, managing access through IAM policies to support both Windows and Linux workloads
- () Deploy Amazon FSx for Lustre and mount the file system using a POSIX-compliant client from both platforms
- () Correct option:
- () References:
- () https://aws.amazon.com/blogs/storage/access-file-shares-on-amazon-fsx-for-windows-file-server-from-a-linux-environment/
- () https://docs.aws.amazon.com/fsx/latest/WindowsGuide/what-is.html
- () https://aws.amazon.com/s3/features/mountpoint/
- () https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html

**Answer:**
Correct Answer: **Deploy Amazon FSx for Windows File Server and mount it using the SMB protocol from both Windows and Linux EC2 instances**

---

## Question 19

**Q:** Which of the following options support the case for using Amazon ElastiCache to meet the given requirements? (Select two)

**Options:**
- **(A) Use Amazon ElastiCache to improve the performance of Extract-Transform-Load (ETL) workloads** [CORRECT]
- (B) Correct selection
- (C) Use Amazon ElastiCache to improve the performance of compute-intensive workloads
- (D) Use Amazon ElastiCache to improve latency and throughput for read-heavy application workloads
- (E) Use Amazon ElastiCache to improve latency and throughput for write-heavy application workloads
- (F) Use Amazon ElastiCache to run highly complex JOIN queries
- (G) Correct option:
- (H) Amazon ElastiCache allows you to run in-memory data stores in the AWS cloud. Amazon ElastiCache is a popular choice for real-time use cases like Caching, Session Stores, Gaming, Geospatial Services, Real-Time Analytics, and Queuing.
- (I) via - https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/elasticache-use-cases.html
- (J) Amazon ElastiCache can be used to significantly improve latency and throughput for many read-heavy application workloads (such as social networking, gaming, media sharing, leaderboard, and Q&A portals) or compute-intensive workloads (such as a recommendation engine) by allowing you to store the objects that are often read in the cache.
- () Overview of Amazon ElastiCache features:
- () via - https://aws.amazon.com/elasticache/features/
- () Incorrect options:
- () Use Amazon ElastiCache to improve latency and throughput for write-heavy application workloads - As mentioned earlier in the explanation, Amazon ElastiCache can be used to significantly improve latency and throughput for many read-heavy application workloads. Caching is not a good fit for write-heavy applications as the cache goes stale at a very fast rate.
- () Use Amazon ElastiCache to improve the performance of Extract-Transform-Load (ETL) workloads - ETL workloads involve reading and transforming high-volume data which is not a good fit for caching. You should use AWS Glue or Amazon EMR to facilitate ETL workloads.
- () Use Amazon ElastiCache to run highly complex JOIN queries - Complex JSON queries can be run on relational databases such as Amazon RDS or Amazon Aurora. Amazon ElastiCache is not a good fit for this use case.
- () References:
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/elasticache-use-cases.html
- () https://aws.amazon.com/elasticache/features/
- () A startup has recently moved their monolithic web application to AWS Cloud. The application runs on a single Amazon EC2 instance. Currently, the user base is small and the startup does not want to spend effort on elaborate disaster recovery strategies or Auto Scaling Group. The application can afford a maximum downtime of 10 minutes.

**Answer:**
Correct Answer: **Use Amazon ElastiCache to improve the performance of Extract-Transform-Load (ETL) workloads**

---

## Question 20

**Q:** In case of a failure, which of these options would you suggest as a cost-effective and automatic recovery procedure for the instance?

**Options:**
- **(A) Configure an Amazon CloudWatch alarm that triggers the recovery of the Amazon EC2 instance, in case the instance fails. The instance, however, should only be configured with an Amazon EBS volume** [CORRECT]
- (B) Configure an Amazon CloudWatch alarm that triggers the recovery of the Amazon EC2 instance, in case the instance fails. The instance can be configured with Amazon Elastic Block Store (Amazon EBS) or with instance store volumes
- (C) Configure Amazon EventBridge events that can trigger the recovery of the Amazon EC2 instance, in case the instance or the application fails
- (D) Configure AWS Trusted Advisor to monitor the health check of Amazon EC2 instance and provide a remedial action in case an unhealthy flag is detected
- (E) Correct option:
- (F) If your instance fails a system status check, you can use Amazon CloudWatch alarm actions to automatically recover it. The recover option is available for over 90% of deployed customer Amazon EC2 instances. The Amazon CloudWatch recovery option works only for system check failures, not for instance status check failures. Also, if you terminate your instance, then it can't be recovered.
- (G) The automatic recovery process attempts to recover your instance for up to three separate failures per day. Your instance may subsequently be retired if automatic recovery fails and a hardware degradation is determined to be the root cause for the original system status check failure.
- (H) Incorrect options:
- (I) Configure Amazon EventBridge events that can trigger the recovery of the Amazon EC2 instance, in case the instance or the application fails - You cannot use Amazon EventBridge events to directly trigger the recovery of the Amazon EC2 instance.
- (J) Configure an Amazon CloudWatch alarm that triggers the recovery of the Amazon EC2 instance, in case the instance fails. The instance can be configured with Amazon Elastic Block Store (Amazon EBS) or with instance store volumes - The recover action is supported only on instances that have Amazon EBS volumes configured on them, instance store volumes are not supported for automatic recovery by Amazon CloudWatch alarms.
- () Configure AWS Trusted Advisor to monitor the health check of Amazon EC2 instance and provide a remedial action in case an unhealthy flag is detected - You can use Amazon EventBridge events to detect and react to changes in the status of AWS Trusted Advisor checks. This support is only available with AWS Business Support and AWS Enterprise Support. AWS Trusted Advisor by itself does not support health checks of Amazon EC2 instances or their recovery.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-recover.html
- () An e-commerce company uses Microsoft Active Directory to provide users and groups with access to resources on the on-premises infrastructure. The company has extended its IT infrastructure to AWS in the form of a hybrid cloud. The engineering team at the company wants to run directory-aware workloads on AWS for a SQL Server-based application. The team also wants to configure a trust relationship to enable single sign-on (SSO) for its users to access resources in either domain.

**Answer:**
Correct Answer: **Configure an Amazon CloudWatch alarm that triggers the recovery of the Amazon EC2 instance, in case the instance fails. The instance, however, should only be configured with an Amazon EBS volume**

---

## Question 21

**Q:** As a solutions architect, which of the following AWS services would you recommend for this use-case?

**Options:**
- (A) Active Directory Connector
- (B) Amazon Cloud Directory
- (C) AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)
- (D) Simple Active Directory (Simple AD)
- (E) Correct option:
- (F) AWS Directory Service provides multiple ways to use Amazon Cloud Directory and Microsoft Active Directory (AD) with other AWS services.
- (G) Incorrect options:
- (H) Active Directory Connector - Use AD Connector if you only need to allow your on-premises users to log in to AWS applications and services with their Active Directory credentials. AD Connector simply connects your existing on-premises Active Directory to AWS. You cannot use it to run directory-aware workloads on AWS, hence this option is not correct.
- (I) Simple Active Directory (Simple AD) - Simple AD provides a subset of the features offered by AWS Managed Microsoft AD. Simple AD is a standalone managed directory that is powered by a Samba 4 Active Directory Compatible Server. Simple AD does not support features such as trust relationships with other domains. Therefore, this option is not correct.
- (J) Amazon Cloud Directory - Amazon Cloud Directory is a cloud-native directory that can store hundreds of millions of application-specific objects with multiple relationships and schemas. Use Amazon Cloud Directory if you need a highly scalable directory store for your application’s hierarchical data. You cannot use it to establish trust relationships with other domains on the on-premises infrastructure. Therefore, this option is not correct.
- () Exam Alert:
- () Reference:
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html
- () Which solution best addresses these needs?
- () Create an Amazon CloudFront distribution in front of the ALB. Enable AWS WAF on the distribution and configure custom rules to filter traffic from known malicious IP ranges and geographies. Use CloudFront access logs for analysis
- **() Subscribe to AWS Shield Advanced to gain proactive DDoS protection. Engage the AWS DDoS Response Team (DRT) to analyze traffic patterns and apply mitigations. Use the built-in logging and reporting to maintain an audit trail of detected events** [CORRECT]
- () Enable Amazon Inspector for the EC2 instances. Use its vulnerability findings to detect potential DDoS attack vectors and patch the EC2 environments accordingly
- () Deploy Amazon GuardDuty and integrate with the EC2 environment. Use GuardDuty findings to manually block suspected IP addresses at the ALB level or within EC2 security groups
- () Correct options:
- () References:
- () https://aws.amazon.com/blogs/aws/category/aws-shield/
- () https://docs.aws.amazon.com/waf/latest/developerguide/ddos-overview.html
- () https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html
- () https://docs.aws.amazon.com/inspector/latest/user/what-is-inspector.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html
- () A retail company uses AWS Cloud to manage its IT infrastructure. The company has set up AWS Organizations to manage several departments running their AWS accounts and using resources such as Amazon EC2 instances and Amazon RDS databases. The company wants to provide shared and centrally-managed VPCs to all departments using applications that need a high degree of interconnectivity.

**Answer:**
Correct Answer: **Subscribe to AWS Shield Advanced to gain proactive DDoS protection. Engage the AWS DDoS Response Team (DRT) to analyze traffic patterns and apply mitigations. Use the built-in logging and reporting to maintain an audit trail of detected events**

---

## Question 22

**Q:** Which solution best addresses these needs?

**Options:**
- (A) Create an Amazon CloudFront distribution in front of the ALB. Enable AWS WAF on the distribution and configure custom rules to filter traffic from known malicious IP ranges and geographies. Use CloudFront access logs for analysis
- **(B) Subscribe to AWS Shield Advanced to gain proactive DDoS protection. Engage the AWS DDoS Response Team (DRT) to analyze traffic patterns and apply mitigations. Use the built-in logging and reporting to maintain an audit trail of detected events** [CORRECT]
- (C) Enable Amazon Inspector for the EC2 instances. Use its vulnerability findings to detect potential DDoS attack vectors and patch the EC2 environments accordingly
- (D) Deploy Amazon GuardDuty and integrate with the EC2 environment. Use GuardDuty findings to manually block suspected IP addresses at the ALB level or within EC2 security groups
- (E) Correct options:
- (F) Incorrect options:
- (G) References:
- (H) https://aws.amazon.com/blogs/aws/category/aws-shield/
- (I) https://docs.aws.amazon.com/waf/latest/developerguide/ddos-overview.html
- (J) https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html
- () https://docs.aws.amazon.com/inspector/latest/user/what-is-inspector.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html
- () A retail company uses AWS Cloud to manage its IT infrastructure. The company has set up AWS Organizations to manage several departments running their AWS accounts and using resources such as Amazon EC2 instances and Amazon RDS databases. The company wants to provide shared and centrally-managed VPCs to all departments using applications that need a high degree of interconnectivity.

**Answer:**
Correct Answer: **Subscribe to AWS Shield Advanced to gain proactive DDoS protection. Engage the AWS DDoS Response Team (DRT) to analyze traffic patterns and apply mitigations. Use the built-in logging and reporting to maintain an audit trail of detected events**

---

## Question 23

**Q:** As a solutions architect, which of the following options would you choose to facilitate this use-case?

**Options:**
- (A) Use VPC sharing to share a VPC with other AWS accounts belonging to the same parent organization from AWS Organizations
- (B) Use VPC sharing to share one or more subnets with other AWS accounts belonging to the same parent organization from AWS Organizations
- (C) Use VPC peering to share one or more subnets with other AWS accounts belonging to the same parent organization from AWS Organizations
- (D) Use VPC peering to share a VPC with other AWS accounts belonging to the same parent organization from AWS Organizations
- (E) Correct option:
- (F) You can share Amazon VPCs to leverage the implicit routing within a VPC for applications that require a high degree of interconnectivity and are within the same trust boundaries. This reduces the number of VPCs that you create and manage while using separate accounts for billing and access control.
- (G) Incorrect options:
- (H) Use VPC sharing to share a VPC with other AWS accounts belonging to the same parent organization from AWS Organizations - Using VPC sharing, an account that owns the VPC (owner) shares one or more subnets with other accounts (participants) that belong to the same organization from AWS Organizations. The owner account cannot share the VPC itself. Therefore this option is incorrect.
- (I) Use VPC peering to share a VPC with other AWS accounts belonging to the same parent organization from AWS Organizations - A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network. VPC peering does not facilitate centrally managed VPCs. Therefore this option is incorrect.
- (J) References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-sharing.html
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () A company maintains its business-critical customer data on an on-premises system in an encrypted format. Over the years, the company has transitioned from using a single encryption key to multiple encryption keys by dividing the data into logical chunks. With the decision to move all the data to an Amazon S3 bucket, the company is now looking for a technique to encrypt each file with a different encryption key to provide maximum security to the migrated on-premises data.
- () How will you implement this requirement without adding the overhead of splitting the data into logical groups?
- () Store the logically divided data into different Amazon S3 buckets. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data
- () Configure a single Amazon S3 bucket to hold all data. Use server-side encryption with AWS KMS (SSE-KMS) and use encryption context to generate a different key for each file/object that you store in the S3 bucket
- () Configure a single Amazon S3 bucket to hold all data. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data
- () Use Multi-Region keys for client-side encryption in the AWS S3 Encryption Client to generate unique keys for each file of data
- () Server-side encryption is the encryption of data at its destination by the application or service that receives it. Amazon S3 encrypts your data at the object level as it writes it to disks in its data centers and decrypts it for you when you access it. When you use server-side encryption with Amazon S3 managed keys (SSE-S3), each object is encrypted with a unique key. As an additional safeguard, it encrypts the key itself with a root key that it regularly rotates.
- () Note: Amazon S3 now applies server-side encryption with Amazon S3 managed keys (SSE-S3) as the base level of encryption for every bucket in Amazon S3. Starting January 5, 2023, all new object uploads to Amazon S3 will be automatically encrypted at no additional cost and with no impact on performance.
- () Store the logically divided data into different Amazon S3 buckets. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data - Server-side encryption with Amazon S3 managed keys (SSE-S3) is the easiest way to implement the given requirement, as there is no additional overhead of splitting data. Multiple S3 buckets are redundant for this requirement.
- () Use Multi-Region keys for client-side encryption in the AWS S3 Encryption Client to generate unique keys for each file of data - Server-side encryption is the encryption of data at its destination by the application or service that receives it. The requirement is about server-side encryption and not about client-side encryption, hence this choice is incorrect.
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/serv-side-encryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html
- () A software company manages a fleet of Amazon EC2 instances that support internal analytics applications. These instances use an IAM role with custom policies to connect to Amazon RDS and AWS Secrets Manager for secure access to credentials and database endpoints. The IT operations team wants to implement a centralized patch management solution that simplifies compliance and security tasks. Their goal is to automate OS patching across EC2 instances without disrupting the running applications.
- () Which approach will allow the company to meet these goals with the least administrative overhead?
- () Manually install the Systems Manager Agent (SSM Agent) on each EC2 instance. Schedule daily patch jobs using cron scripts
- () Create a second IAM role with the AmazonSSMManagedInstanceCore policy and attach both the new and the existing IAM roles to each EC2 instance using Systems Manager Hybrid Activation
- () Detach the existing IAM role from all EC2 instances. Replace it with a new role that has both the original permissions and the AmazonSSMManagedInstanceCore policy to enable Systems Manager features
- **() Enable Default Host Management Configuration in AWS Systems Manager Quick Setup** [CORRECT]
- () via - https://aws.amazon.com/blogs/mt/enable-management-of-your-amazon-ec2-instances-in-aws-systems-manager-using-default-host-management-configuration/
- () Manually install the Systems Manager Agent (SSM Agent) on each EC2 instance. Schedule daily patch jobs using cron scripts - Manually scripting patching operations using cron jobs introduces high operational overhead and does not leverage native AWS integrations. This method lacks scalability, centralized compliance reporting, and the benefit of automated remediation provided by Systems Manager.

**Answer:**
Correct Answer: **Enable Default Host Management Configuration in AWS Systems Manager Quick Setup**

---

## Question 24

**Q:** How will you implement this requirement without adding the overhead of splitting the data into logical groups?

**Options:**
- (A) Store the logically divided data into different Amazon S3 buckets. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data
- (B) Configure a single Amazon S3 bucket to hold all data. Use server-side encryption with AWS KMS (SSE-KMS) and use encryption context to generate a different key for each file/object that you store in the S3 bucket
- (C) Configure a single Amazon S3 bucket to hold all data. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data
- (D) Use Multi-Region keys for client-side encryption in the AWS S3 Encryption Client to generate unique keys for each file of data
- (E) Correct option:
- (F) Server-side encryption is the encryption of data at its destination by the application or service that receives it. Amazon S3 encrypts your data at the object level as it writes it to disks in its data centers and decrypts it for you when you access it. When you use server-side encryption with Amazon S3 managed keys (SSE-S3), each object is encrypted with a unique key. As an additional safeguard, it encrypts the key itself with a root key that it regularly rotates.
- (G) Note: Amazon S3 now applies server-side encryption with Amazon S3 managed keys (SSE-S3) as the base level of encryption for every bucket in Amazon S3. Starting January 5, 2023, all new object uploads to Amazon S3 will be automatically encrypted at no additional cost and with no impact on performance.
- (H) Incorrect options:
- (I) Store the logically divided data into different Amazon S3 buckets. Use server-side encryption with Amazon S3 managed keys (SSE-S3) to encrypt the data - Server-side encryption with Amazon S3 managed keys (SSE-S3) is the easiest way to implement the given requirement, as there is no additional overhead of splitting data. Multiple S3 buckets are redundant for this requirement.
- (J) Use Multi-Region keys for client-side encryption in the AWS S3 Encryption Client to generate unique keys for each file of data - Server-side encryption is the encryption of data at its destination by the application or service that receives it. The requirement is about server-side encryption and not about client-side encryption, hence this choice is incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/serv-side-encryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html
- () A software company manages a fleet of Amazon EC2 instances that support internal analytics applications. These instances use an IAM role with custom policies to connect to Amazon RDS and AWS Secrets Manager for secure access to credentials and database endpoints. The IT operations team wants to implement a centralized patch management solution that simplifies compliance and security tasks. Their goal is to automate OS patching across EC2 instances without disrupting the running applications.
- () Which approach will allow the company to meet these goals with the least administrative overhead?
- () Manually install the Systems Manager Agent (SSM Agent) on each EC2 instance. Schedule daily patch jobs using cron scripts
- () Create a second IAM role with the AmazonSSMManagedInstanceCore policy and attach both the new and the existing IAM roles to each EC2 instance using Systems Manager Hybrid Activation
- () Detach the existing IAM role from all EC2 instances. Replace it with a new role that has both the original permissions and the AmazonSSMManagedInstanceCore policy to enable Systems Manager features
- () Enable Default Host Management Configuration in AWS Systems Manager Quick Setup
- () via - https://aws.amazon.com/blogs/mt/enable-management-of-your-amazon-ec2-instances-in-aws-systems-manager-using-default-host-management-configuration/
- () Manually install the Systems Manager Agent (SSM Agent) on each EC2 instance. Schedule daily patch jobs using cron scripts - Manually scripting patching operations using cron jobs introduces high operational overhead and does not leverage native AWS integrations. This method lacks scalability, centralized compliance reporting, and the benefit of automated remediation provided by Systems Manager.
- () Detach the existing IAM role from all EC2 instances. Replace it with a new role that has both the original permissions and the AmazonSSMManagedInstanceCore policy to enable Systems Manager features - Detaching and replacing the existing IAM role risks disrupting application functionality that depends on the role’s current policies (e.g., RDS access). This introduces downtime and manual changes to launch templates or running instances, violating the requirement to avoid disruption.
- () https://aws.amazon.com/blogs/mt/enable-management-of-your-amazon-ec2-instances-in-aws-systems-manager-using-default-host-management-configuration/
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/quick-setup-host-management.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html
- () An IT company hosts windows based applications on its on-premises data center. The company is looking at moving the business to the AWS Cloud. The cloud solution should offer shared storage space that multiple applications can access without a need for replication. Also, the solution should integrate with the company's self-managed Active Directory domain.
- () Which of the following solutions addresses these requirements with the minimal integration effort?
- () Use File Gateway of AWS Storage Gateway to create a hybrid storage solution
- () Use Amazon FSx for Lustre as a shared storage solution with millisecond latencies
- **() Use Amazon FSx for Windows File Server as a shared storage solution** [CORRECT]
- () Use Amazon Elastic File System (Amazon EFS) as a shared storage solution
- () With Amazon FSx, you get highly available and durable file storage starting from $0.013 per GB-month. Data deduplication enables you to optimize costs even further by removing redundant data. You can increase your file system storage and scale throughput capacity at any time, making it easy to respond to changing business needs. There are no upfront costs or licensing fees.
- () How Amazon FSx for Windows File Server works:

**Answer:**
Correct Answer: **Use Amazon FSx for Windows File Server as a shared storage solution**

---

## Question 25

**Q:** Which approach will allow the company to meet these goals with the least administrative overhead?

**Options:**
- (A) Manually install the Systems Manager Agent (SSM Agent) on each EC2 instance. Schedule daily patch jobs using cron scripts
- (B) Create a second IAM role with the AmazonSSMManagedInstanceCore policy and attach both the new and the existing IAM roles to each EC2 instance using Systems Manager Hybrid Activation
- (C) Detach the existing IAM role from all EC2 instances. Replace it with a new role that has both the original permissions and the AmazonSSMManagedInstanceCore policy to enable Systems Manager features
- (D) Enable Default Host Management Configuration in AWS Systems Manager Quick Setup
- (E) Correct option:
- (F) via - https://aws.amazon.com/blogs/mt/enable-management-of-your-amazon-ec2-instances-in-aws-systems-manager-using-default-host-management-configuration/
- (G) Incorrect options:
- (H) Manually install the Systems Manager Agent (SSM Agent) on each EC2 instance. Schedule daily patch jobs using cron scripts - Manually scripting patching operations using cron jobs introduces high operational overhead and does not leverage native AWS integrations. This method lacks scalability, centralized compliance reporting, and the benefit of automated remediation provided by Systems Manager.
- (I) Detach the existing IAM role from all EC2 instances. Replace it with a new role that has both the original permissions and the AmazonSSMManagedInstanceCore policy to enable Systems Manager features - Detaching and replacing the existing IAM role risks disrupting application functionality that depends on the role’s current policies (e.g., RDS access). This introduces downtime and manual changes to launch templates or running instances, violating the requirement to avoid disruption.
- (J) References:
- () https://aws.amazon.com/blogs/mt/enable-management-of-your-amazon-ec2-instances-in-aws-systems-manager-using-default-host-management-configuration/
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/quick-setup-host-management.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html
- () An IT company hosts windows based applications on its on-premises data center. The company is looking at moving the business to the AWS Cloud. The cloud solution should offer shared storage space that multiple applications can access without a need for replication. Also, the solution should integrate with the company's self-managed Active Directory domain.
- () Which of the following solutions addresses these requirements with the minimal integration effort?
- () Use File Gateway of AWS Storage Gateway to create a hybrid storage solution
- () Use Amazon FSx for Lustre as a shared storage solution with millisecond latencies
- **() Use Amazon FSx for Windows File Server as a shared storage solution** [CORRECT]
- () Use Amazon Elastic File System (Amazon EFS) as a shared storage solution
- () With Amazon FSx, you get highly available and durable file storage starting from $0.013 per GB-month. Data deduplication enables you to optimize costs even further by removing redundant data. You can increase your file system storage and scale throughput capacity at any time, making it easy to respond to changing business needs. There are no upfront costs or licensing fees.
- () How Amazon FSx for Windows File Server works:
- () via - https://aws.amazon.com/fsx/windows/
- () Use Amazon Elastic File System (Amazon EFS) as a shared storage solution - Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources. Amazon EFS is a powerful, shared storage solution that would have been the right answer if the customer systems were Linux based. Amazon EFS is compatible with only Linux-based AMIs for Amazon EC2.
- () Reference:
- () https://aws.amazon.com/fsx/windows/
- () A small business has been running its IT systems on the on-premises infrastructure but the business now plans to migrate to AWS Cloud for operational efficiencies.

**Answer:**
Correct Answer: **Use Amazon FSx for Windows File Server as a shared storage solution**

---

## Question 26

**Q:** Which of the following solutions addresses these requirements with the minimal integration effort?

**Options:**
- (A) Use File Gateway of AWS Storage Gateway to create a hybrid storage solution
- (B) Use Amazon FSx for Lustre as a shared storage solution with millisecond latencies
- **(C) Use Amazon FSx for Windows File Server as a shared storage solution** [CORRECT]
- (D) Use Amazon Elastic File System (Amazon EFS) as a shared storage solution
- (E) Correct option:
- (F) With Amazon FSx, you get highly available and durable file storage starting from $0.013 per GB-month. Data deduplication enables you to optimize costs even further by removing redundant data. You can increase your file system storage and scale throughput capacity at any time, making it easy to respond to changing business needs. There are no upfront costs or licensing fees.
- (G) How Amazon FSx for Windows File Server works:
- (H) via - https://aws.amazon.com/fsx/windows/
- (I) Incorrect options:
- (J) Use Amazon Elastic File System (Amazon EFS) as a shared storage solution - Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources. Amazon EFS is a powerful, shared storage solution that would have been the right answer if the customer systems were Linux based. Amazon EFS is compatible with only Linux-based AMIs for Amazon EC2.
- () Reference:
- () https://aws.amazon.com/fsx/windows/
- () A small business has been running its IT systems on the on-premises infrastructure but the business now plans to migrate to AWS Cloud for operational efficiencies.

**Answer:**
Correct Answer: **Use Amazon FSx for Windows File Server as a shared storage solution**

---

## Question 27

**Q:** As a Solutions Architect, can you suggest a cost-effective serverless solution for its flagship application that has both static and dynamic content?

**Options:**
- (A) Host both the static and dynamic content of the web application on Amazon EC2 with Amazon RDS as database. Amazon CloudFront should be configured to distribute the content across geographically disperse regions
- (B) Host the static content on Amazon S3 and use AWS Lambda with Amazon DynamoDB for the serverless web application that handles dynamic content. Amazon CloudFront will sit in front of AWS Lambda for distribution across diverse regions
- (C) Host both the static and dynamic content of the web application on Amazon S3 and use Amazon CloudFront for distribution across diverse regions/countries
- (D) Host the static content on Amazon S3 and use Amazon EC2 with Amazon RDS for generating the dynamic content. Amazon CloudFront can be configured in front of Amazon EC2 instance, to make global distribution easy
- (E) Correct option:
- (F) AWS Lambda with Amazon DynamoDB is the right answer for a serverless solution. Amazon CloudFront will help in enhancing user experience by delivering content, across different geographic locations with low latency. Amazon S3 is a cost-effective and faster way of distributing static content for web applications.
- (G) Incorrect options:
- (H) Host both the static and dynamic content of the web application on Amazon S3 and use Amazon CloudFront for distribution across diverse regions/countries - Amazon S3 is not the right fit for hosting Dynamic content, so this option is incorrect.
- (I) Host the static content on Amazon S3 and use Amazon EC2 with Amazon RDS for generating the dynamic content. Amazon CloudFront can be configured in front of Amazon EC2 instance, to make global distribution easy - The company is looking for a serverless solution, and Amazon EC2 is not a serverless service as the Amazon EC2 instances have to be managed by AWS customers.
- (J) Host both the static and dynamic content of the web application on Amazon EC2 with Amazon RDS as database. Amazon CloudFront should be configured to distribute the content across geographically disperse regions - This is a possible solution, but not a cost-effective or optimal one. Since static content can be cost-effectively managed on Amazon S3 and can be accessed and distributed faster when compared to fetching the content from the Amazon EC2 server.
- () Reference:
- () https://aws.amazon.com/blogs/networking-and-content-delivery/deliver-your-apps-dynamic-content-using-amazon-cloudfront-getting-started-template/
- () A healthcare startup is modernizing its monolithic Python-based analytics application by transitioning to a microservices architecture on AWS. As a pilot, the team wants to refactor one module into a standalone microservice that can handle hundreds of requests per second. They are seeking an AWS-native solution that supports Python, scales automatically with traffic, and requires minimal infrastructure management and operational overhead to build, test, and deploy the service efficiently.
- () Which AWS solution best meets these requirements?
- () Deploy the microservice in an AWS Fargate task using Amazon ECS. Package the code in a Docker container image with a Python runtime and configure ECS Service Auto Scaling to respond to CPU utilization metrics
- () Use AWS App Runner to build and deploy the Python application directly from a GitHub repository. Allow App Runner to manage traffic scaling and deployments
- () Use Amazon EC2 Spot Instances in an Auto Scaling group. Launch the Python application as a background service and install all required dependencies at instance startup
- **() Use AWS Lambda to run the Python-based microservice. Integrate it with Amazon API Gateway for HTTP access and enable provisioned concurrency for performance during peak loads** [CORRECT]
- () via - https://aws.amazon.com/blogs/compute/creating-low-latency-high-volume-apis-with-provisioned-concurrency/
- () Use Amazon EC2 Spot Instances in an Auto Scaling group. Launch the Python application as a background service and install all required dependencies at instance startup - While Spot Instances are cost-effective, they are not reliable for production workloads due to the risk of interruption. Additionally, managing EC2 Auto Scaling groups and instance health checks introduces high operational overhead, which contradicts the goal of minimal infrastructure and low maintenance.
- () References:
- () https://docs.aws.amazon.com/lambda/latest/dg/services-apigateway.html
- () https://aws.amazon.com/blogs/compute/creating-low-latency-high-volume-apis-with-provisioned-concurrency/
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () https://docs.aws.amazon.com/apprunner/latest/dg/what-is-apprunner.html
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html
- () A leading online gaming company is migrating its flagship application to AWS Cloud for delivering its online games to users across the world. The company would like to use a Network Load Balancer to handle millions of requests per second. The engineering team has provisioned multiple instances in a public subnet and specified these instance IDs as the targets for the NLB.

**Answer:**
Correct Answer: **Use AWS Lambda to run the Python-based microservice. Integrate it with Amazon API Gateway for HTTP access and enable provisioned concurrency for performance during peak loads**

---

## Question 28

**Q:** As a solutions architect, can you help the engineering team understand the correct routing mechanism for these target instances?

**Options:**
- (A) Traffic is routed to instances using the primary public IP address specified in the primary network interface for the instance
- **(B) Traffic is routed to instances using the primary private IP address specified in the primary network interface for the instance** [CORRECT]
- (C) Traffic is routed to instances using the primary elastic IP address specified in the primary network interface for the instance
- (D) Traffic is routed to instances using the instance ID specified in the primary network interface for the instance
- (E) Correct option:
- (F) A Network Load Balancer functions at the fourth layer of the Open Systems Interconnection (OSI) model. It can handle millions of requests per second. After the load balancer receives a connection request, it selects a target from the target group for the default rule. It attempts to open a TCP connection to the selected target on the port specified in the listener configuration.
- (G) Request Routing and IP Addresses -
- (H) If you specify targets using an instance ID, traffic is routed to instances using the primary private IP address specified in the primary network interface for the instance. The load balancer rewrites the destination IP address from the data packet before forwarding it to the target instance.
- (I) If you specify targets using IP addresses, you can route traffic to an instance using any private IP address from one or more network interfaces. This enables multiple applications on an instance to use the same port. Note that each network interface can have its security group. The load balancer rewrites the destination IP address before forwarding it to the target.
- (J) Incorrect options:
- () Traffic is routed to instances using the primary public IP address specified in the primary network interface for the instance - If you specify targets using an instance ID, traffic is routed to instances using the primary private IP address specified in the primary network interface for the instance. So public IP address cannot be used to route the traffic to the instance.
- () Traffic is routed to instances using the primary elastic IP address specified in the primary network interface for the instance - If you specify targets using an instance ID, traffic is routed to instances using the primary private IP address specified in the primary network interface for the instance. So elastic IP address cannot be used to route the traffic to the instance.
- () Traffic is routed to instances using the instance ID specified in the primary network interface for the instance - You cannot use instance ID to route traffic to the instance. This option is just added as a distractor.
- () References:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-target-groups.html
- () The DevOps team at an IT company has recently migrated to AWS and they are configuring security groups for their two-tier application with public web servers and private database servers. The team wants to understand the allowed configuration options for an inbound rule for a security group.

**Answer:**
Correct Answer: **Traffic is routed to instances using the primary private IP address specified in the primary network interface for the instance**

---

## Question 29

**Q:** As a solutions architect, which of the following would you identify as an INVALID option for setting up such a configuration?

**Options:**
- **(A) You can use an Internet Gateway ID as the custom source for the inbound rule** [CORRECT]
- (B) You can use a range of IP addresses in CIDR block notation as the custom source for the inbound rule
- (C) You can use a security group as the custom source for the inbound rule
- (D) You can use an IP address as the custom source for the inbound rule
- (E) Correct option:
- (F) A security group acts as a virtual firewall that controls the traffic for one or more instances. When you launch an instance, you can specify one or more security groups; otherwise, you can use the default security group. You can add rules to each security group that allows traffic to or from its associated instances. You can modify the rules for a security group at any time; the new rules are automatically applied to all instances that are associated with the security group.
- (G) Please see this list of allowed source or destination for security group rules:
- (H) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- (I) Therefore, you cannot use an Internet Gateway ID as the custom source for the inbound rule.
- (J) Incorrect options:
- () As described in the list of allowed sources or destinations for security group rules, the above options are supported.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () A media startup is looking at hosting their web application on AWS Cloud. The application will be accessed by users from different geographic regions of the world to upload and download video files that can reach a maximum size of 10 gigabytes. The startup wants the solution to be cost-effective and scalable with the lowest possible latency for a great user experience.

**Answer:**
Correct Answer: **You can use an Internet Gateway ID as the custom source for the inbound rule**

---

## Question 30

**Q:** As a Solutions Architect, which of the following will you suggest as an optimal solution to meet the given requirements?

**Options:**
- (A) Use Amazon EC2 with Amazon ElastiCache for faster distribution of content, while Amazon S3 can be used as a storage service
- **(B) Use Amazon S3 for hosting the web application and use Amazon S3 Transfer Acceleration (Amazon S3TA) to reduce the latency that geographically dispersed users might face** [CORRECT]
- (C) Use Amazon EC2 with AWS Global Accelerator for faster distribution of content, while using Amazon S3 as storage service
- (D) Use Amazon S3 for hosting the web application and use Amazon CloudFront for faster distribution of content to geographically dispersed users
- (E) Correct option:
- (F) S3TA improves transfer performance by routing traffic through Amazon CloudFront’s globally distributed Edge Locations and over AWS backbone networks, and by using network protocol optimizations.
- (G) For applications interacting with your Amazon S3 buckets through the S3 API from outside of your bucket’s region, S3TA helps avoid the variability in Internet routing and congestion. It does this by routing your uploads and downloads over the AWS global network infrastructure, so you get the benefit of AWS network optimizations.
- (H) Incorrect options:
- (I) via - https://aws.amazon.com/s3/faqs/
- (J) Reference:
- () [https://aws.amazon.com/s3/transfer-acceleration/](https://aws.amazon.com/s3/transfer-acceleration
- () https://aws.amazon.com/s3/faqs/
- () A developer has configured inbound traffic for the relevant ports in both the Security Group of the Amazon EC2 instance as well as the Network Access Control List (Network ACL) of the subnet for the Amazon EC2 instance. The developer is, however, unable to connect to the service running on the Amazon EC2 instance.

**Answer:**
Correct Answer: **Use Amazon S3 for hosting the web application and use Amazon S3 Transfer Acceleration (Amazon S3TA) to reduce the latency that geographically dispersed users might face**

---

## Question 31

**Q:** As a solutions architect, how will you fix this issue?

**Options:**
- **(A) Security Groups are stateful, so allowing inbound traffic to the necessary ports enables the connection. Network ACLs are stateless, so you must allow both inbound and outbound traffic** [CORRECT]
- (B) Rules associated with Network ACLs should never be modified from command line. An attempt to modify rules from command line blocks the rule and results in an erratic behavior
- (C) IAM Role defined in the Security Group is different from the IAM Role that is given access in the Network ACLs
- (D) Network ACLs are stateful, so allowing inbound traffic to the necessary ports enables the connection. Security Groups are stateless, so you must allow both inbound and outbound traffic
- (E) Correct option:
- (F) Security groups are stateful, so allowing inbound traffic to the necessary ports enables the connection. Network ACLs are stateless, so you must allow both inbound and outbound traffic.
- (G) To enable the connection to a service running on an instance, the associated network ACL must allow both inbound traffic on the port that the service is listening on as well as allow outbound traffic from ephemeral ports. When a client connects to a server, a random port from the ephemeral port range (1024-65535) becomes the client's source port.
- (H) The designated ephemeral port then becomes the destination port for return traffic from the service, so outbound traffic from the ephemeral port must be allowed in the network ACL.
- (I) By default, network ACLs allow all inbound and outbound traffic. If your network ACL is more restrictive, then you need to explicitly allow traffic from the ephemeral port range.
- (J) If you accept traffic from the internet, then you also must establish a route through an internet gateway. If you accept traffic over VPN or AWS Direct Connect, then you must establish a route through a virtual private gateway (VGW).
- () Incorrect options:
- () Network ACLs are stateful, so allowing inbound traffic to the necessary ports enables the connection. Security Groups are stateless, so you must allow both inbound and outbound traffic - This is incorrect as already discussed.
- () IAM Role defined in the Security Group is different from the IAM Role that is given access in the Network ACLs - This is a made-up option and just added as a distractor.
- () Rules associated with Network ACLs should never be modified from command line. An attempt to modify rules from command line blocks the rule and results in an erratic behavior - This option is a distractor. AWS does not support modifying rules of Network ACLs from the command line tool.
- () Reference:
- () https://aws.amazon.com/premiumsupport/knowledge-center/resolve-connection-sg-acl-inbound/
- () A company has set up AWS Organizations to manage several departments running their own AWS accounts. The departments operate from different countries and are spread across various AWS Regions. The company wants to set up a consistent resource provisioning process across departments so that each resource follows pre-defined configurations such as using a specific type of Amazon EC2 instances, specific IAM roles for AWS Lambda functions, etc.

**Answer:**
Correct Answer: **Security Groups are stateful, so allowing inbound traffic to the necessary ports enables the connection. Network ACLs are stateless, so you must allow both inbound and outbound traffic**

---

## Question 32

**Q:** As a solutions architect, which of the following options would you recommend for this use-case?

**Options:**
- (A) Use AWS CloudFormation stacks to deploy the same template across AWS accounts and regions
- **(B) Use AWS CloudFormation StackSets to deploy the same template across AWS accounts and regions** [CORRECT]
- (C) Use AWS Resource Access Manager (AWS RAM) to deploy the same template across AWS accounts and regions
- (D) Use AWS CloudFormation templates to deploy the same template across AWS accounts and regions
- (E) Correct option:
- (F)  across specified regions.
- (G) AWS CloudFormation StackSets:
- (H) via - https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html
- (I) Incorrect options:
- (J) Use AWS CloudFormation templates to deploy the same template across AWS accounts and regions - AWS Cloudformation template is a JSON or YAML-format, text-based file that describes all the AWS resources you need to deploy to run your application. A template acts as a blueprint for a stack. AWS CloudFormation templates cannot be used to deploy the same template across AWS accounts and regions.
- () Use AWS CloudFormation stacks to deploy the same template across AWS accounts and regions - AWS CloudFormation stack is a set of AWS resources that are created and managed as a single unit when AWS CloudFormation instantiates a template. A stack cannot be used to deploy the same template across AWS accounts and regions.
- () Use AWS Resource Access Manager (AWS RAM) to deploy the same template across AWS accounts and regions - AWS Resource Access Manager (AWS RAM) is a service that enables you to easily and securely share AWS resources with any AWS account or within your AWS Organization. Resource Access Manager cannot be used to deploy the same template across AWS accounts and regions.
- () References:
- () https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html
- () https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-whatis-howdoesitwork.html
- () The engineering team at an e-commerce company wants to migrate from Amazon Simple Queue Service (Amazon SQS) Standard queues to FIFO (First-In-First-Out) queues with batching.
- () As a solutions architect, which of the following steps would you have in the migration checklist? (Select three)
- () Make sure that the name of the FIFO (First-In-First-Out) queue is the same as the standard queue
- () Convert the existing standard queue into a FIFO (First-In-First-Out) queue
- () Make sure that the throughput for the target FIFO (First-In-First-Out) queue does not exceed 300 messages per second
- () Correct selection
- () Delete the existing standard queue and recreate it as a FIFO (First-In-First-Out) queue
- () Make sure that the name of the FIFO (First-In-First-Out) queue ends with the .fifo suffix
- () Make sure that the throughput for the target FIFO (First-In-First-Out) queue does not exceed 3,000 messages per second
- () Correct options:
- () Amazon SQS offers two types of message queues. Standard queues offer maximum throughput, best-effort ordering, and at-least-once delivery. SQS FIFO queues are designed to guarantee that messages are processed exactly once, in the exact order that they are sent.
- () By default, FIFO queues support up to 3,000 messages per second with batching, or up to 300 messages per second (300 send, receive, or delete operations per second) without batching. Therefore, using batching you can meet a throughput requirement of upto 3,000 messages per second.
- () The name of a FIFO queue must end with the .fifo suffix. The suffix counts towards the 80-character queue name limit. To determine whether a queue is FIFO, you can check whether the queue name ends with the suffix.
- () If you have an existing application that uses standard queues and you want to take advantage of the ordering or exactly-once processing features of FIFO queues, you need to configure the queue and your application correctly. You can't convert an existing standard queue into a FIFO queue. To make the move, you must either create a new FIFO queue for your application or delete your existing standard queue and recreate it as a FIFO queue.
- () Make sure that the name of the FIFO (First-In-First-Out) queue is the same as the standard queue - The name of a FIFO queue must end with the .fifo suffix.
- () Make sure that the throughput for the target FIFO (First-In-First-Out) queue does not exceed 300 messages per second - By default, FIFO queues support up to 3,000 messages per second with batching.
- () https://aws.amazon.com/sqs/faqs/
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html
- () As a solutions architect, which of the following options would you identify as CORRECT? (Select three)
- () NAT instance supports port forwarding

**Answer:**
Correct Answer: **Use AWS CloudFormation StackSets to deploy the same template across AWS accounts and regions**

---

## Question 33

**Q:** As a solutions architect, which of the following steps would you have in the migration checklist? (Select three)

**Options:**
- **(A) Make sure that the name of the FIFO (First-In-First-Out) queue is the same as the standard queue** [CORRECT]
- (B) Convert the existing standard queue into a FIFO (First-In-First-Out) queue
- (C) Make sure that the throughput for the target FIFO (First-In-First-Out) queue does not exceed 300 messages per second
- (D) Correct selection
- (E) Delete the existing standard queue and recreate it as a FIFO (First-In-First-Out) queue
- (F) Make sure that the name of the FIFO (First-In-First-Out) queue ends with the .fifo suffix
- (G) Make sure that the throughput for the target FIFO (First-In-First-Out) queue does not exceed 3,000 messages per second
- (H) Correct options:
- (I) Amazon SQS offers two types of message queues. Standard queues offer maximum throughput, best-effort ordering, and at-least-once delivery. SQS FIFO queues are designed to guarantee that messages are processed exactly once, in the exact order that they are sent.
- (J) By default, FIFO queues support up to 3,000 messages per second with batching, or up to 300 messages per second (300 send, receive, or delete operations per second) without batching. Therefore, using batching you can meet a throughput requirement of upto 3,000 messages per second.
- () The name of a FIFO queue must end with the .fifo suffix. The suffix counts towards the 80-character queue name limit. To determine whether a queue is FIFO, you can check whether the queue name ends with the suffix.
- () If you have an existing application that uses standard queues and you want to take advantage of the ordering or exactly-once processing features of FIFO queues, you need to configure the queue and your application correctly. You can't convert an existing standard queue into a FIFO queue. To make the move, you must either create a new FIFO queue for your application or delete your existing standard queue and recreate it as a FIFO queue.
- () Incorrect options:
- () Make sure that the name of the FIFO (First-In-First-Out) queue is the same as the standard queue - The name of a FIFO queue must end with the .fifo suffix.
- () Make sure that the throughput for the target FIFO (First-In-First-Out) queue does not exceed 300 messages per second - By default, FIFO queues support up to 3,000 messages per second with batching.
- () References:
- () https://aws.amazon.com/sqs/faqs/
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html
- () As a solutions architect, which of the following options would you identify as CORRECT? (Select three)
- () NAT instance supports port forwarding
- () NAT instance can be used as a bastion server
- () Security Groups can be associated with a NAT instance
- () NAT gateway can be used as a bastion server
- () NAT gateway supports port forwarding
- () Security Groups can be associated with a NAT gateway
- () A NAT instance or a NAT Gateway can be used in a public subnet in your VPC to enable instances in the private subnet to initiate outbound IPv4 traffic to the Internet.
- () How NAT Gateway works:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () How NAT Instance works:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-comparison.html

**Answer:**
Correct Answer: **Make sure that the name of the FIFO (First-In-First-Out) queue is the same as the standard queue**

---

## Question 34

**Q:** As a solutions architect, which of the following options would you identify as CORRECT? (Select three)

**Options:**
- (A) Correct selection
- (B) NAT instance supports port forwarding
- (C) NAT instance can be used as a bastion server
- (D) Security Groups can be associated with a NAT instance
- (E) NAT gateway can be used as a bastion server
- (F) NAT gateway supports port forwarding
- (G) Security Groups can be associated with a NAT gateway
- (H) Correct options:
- (I) A NAT instance or a NAT Gateway can be used in a public subnet in your VPC to enable instances in the private subnet to initiate outbound IPv4 traffic to the Internet.
- (J) How NAT Gateway works:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () How NAT Instance works:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/VPC_NAT_Instance.html
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-comparison.html
- () Incorrect options:
- () These three options contradict the details provided in the explanation above, so these options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-comparison.html
- () A gaming company uses Application Load Balancers in front of Amazon EC2 instances for different services and microservices. The architecture has now become complex with too many Application Load Balancers in multiple AWS Regions. Security updates, firewall configurations, and traffic routing logic have become complex with too many IP addresses and configurations.
- () The company is looking at an easy and effective way to bring down the number of IP addresses allowed by the firewall and easily manage the entire network infrastructure. Which of these options represents an appropriate solution for this requirement?
- () Configure Elastic IPs for each of the Application Load Balancers in each Region
- () Set up a Network Load Balancer with elastic IP address. Register the private IPs of all the Application Load Balancers as targets of this Network Load Balancer
- **() Launch AWS Global Accelerator and create endpoints for all the Regions. Register the Application Load Balancers of each Region to the corresponding endpoints** [CORRECT]
- () Assign an Elastic IP to an Auto Scaling Group (ASG), and set up multiple Amazon EC2 instances to run behind the Auto Scaling Groups, for each of the Regions
- () Correct option:
- () AWS Global Accelerator is a networking service that sends your user’s traffic through Amazon Web Service’s global network infrastructure, improving your internet user performance by up to 60%. When the internet is congested, Global Accelerator’s automatic routing optimizations will help keep your packet loss, jitter, and latency consistently low.
- () With AWS Global Accelerator, you are provided two global static customer-facing IPs to simplify traffic management. On the back end, add or remove your AWS application origins, such as Network Load Balancers, Application Load Balancers, elastic IP address (EIP), and Amazon EC2 Instances, without making user-facing changes. To mitigate endpoint failure, AWS Global Accelerator automatically re-routes your traffic to your nearest healthy available endpoint.
- () Simplified and resilient traffic routing for multi-Region applications:
- () via - https://aws.amazon.com/global-accelerator/
- () Configure Elastic IPs for each of the Application Load Balancers in each Region - An Application Load Balancer cannot be assigned an Elastic IP address (static IP address).
- () Set up a Network Load Balancer with elastic IP address. Register the private IPs of all the Application Load Balancers as targets of this Network Load Balancer - A Network Load Balancer can be configured to take an Elastic IP address. However, with hundreds of Application Load Balancers and Network Load Balancers, the solution will be equally cumbersome to manage.
- () Assign an Elastic IP to an Auto Scaling Group (ASG), and set up multiple Amazon EC2 instances to run behind the Auto Scaling Groups, for each of the Regions - You cannot assign an elastic IP address to an Auto Scaling Group (ASG), since ASG just manages a collection of Amazon EC2 instances.
- () References:
- () https://aws.amazon.com/global-accelerator/

**Answer:**
Correct Answer: **Launch AWS Global Accelerator and create endpoints for all the Regions. Register the Application Load Balancers of each Region to the corresponding endpoints**

---

## Question 35

**Q:** The company is looking at an easy and effective way to bring down the number of IP addresses allowed by the firewall and easily manage the entire network infrastructure. Which of these options represents an appropriate solution for this requirement?

**Options:**
- (A) Configure Elastic IPs for each of the Application Load Balancers in each Region
- (B) Set up a Network Load Balancer with elastic IP address. Register the private IPs of all the Application Load Balancers as targets of this Network Load Balancer
- **(C) Launch AWS Global Accelerator and create endpoints for all the Regions. Register the Application Load Balancers of each Region to the corresponding endpoints** [CORRECT]
- (D) Assign an Elastic IP to an Auto Scaling Group (ASG), and set up multiple Amazon EC2 instances to run behind the Auto Scaling Groups, for each of the Regions
- (E) Correct option:
- (F) AWS Global Accelerator is a networking service that sends your user’s traffic through Amazon Web Service’s global network infrastructure, improving your internet user performance by up to 60%. When the internet is congested, Global Accelerator’s automatic routing optimizations will help keep your packet loss, jitter, and latency consistently low.
- (G) With AWS Global Accelerator, you are provided two global static customer-facing IPs to simplify traffic management. On the back end, add or remove your AWS application origins, such as Network Load Balancers, Application Load Balancers, elastic IP address (EIP), and Amazon EC2 Instances, without making user-facing changes. To mitigate endpoint failure, AWS Global Accelerator automatically re-routes your traffic to your nearest healthy available endpoint.
- (H) Simplified and resilient traffic routing for multi-Region applications:
- (I) via - https://aws.amazon.com/global-accelerator/
- (J) Incorrect options:
- () Configure Elastic IPs for each of the Application Load Balancers in each Region - An Application Load Balancer cannot be assigned an Elastic IP address (static IP address).
- () Set up a Network Load Balancer with elastic IP address. Register the private IPs of all the Application Load Balancers as targets of this Network Load Balancer - A Network Load Balancer can be configured to take an Elastic IP address. However, with hundreds of Application Load Balancers and Network Load Balancers, the solution will be equally cumbersome to manage.
- () Assign an Elastic IP to an Auto Scaling Group (ASG), and set up multiple Amazon EC2 instances to run behind the Auto Scaling Groups, for each of the Regions - You cannot assign an elastic IP address to an Auto Scaling Group (ASG), since ASG just manages a collection of Amazon EC2 instances.
- () References:
- () https://aws.amazon.com/global-accelerator/
- () https://aws.amazon.com/blogs/networking-and-content-delivery/using-static-ip-addresses-for-application-load-balancers/
- () A social media startup uses AWS Cloud to manage its IT infrastructure. The engineering team at the startup wants to perform weekly database rollovers for a MySQL database server using a serverless cron job that typically takes about 5 minutes to execute the database rollover script written in Python. The database rollover will archive the past week’s data from the production database to keep the database small while still keeping its data accessible.

**Answer:**
Correct Answer: **Launch AWS Global Accelerator and create endpoints for all the Regions. Register the Application Load Balancers of each Region to the corresponding endpoints**

---

## Question 36

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-efficient and reliable solution?

**Options:**
- (A) Create a time-based schedule option within an AWS Glue job to invoke itself every week and run the database rollover script
- (B) Provision an Amazon EC2 scheduled reserved instance to run the database rollover script to be run via an OS-based weekly cron expression
- (C) Provision an Amazon EC2 spot instance to run the database rollover script to be run via an OS-based weekly cron expression
- **(D) Schedule a weekly Amazon EventBridge event cron expression to invoke an AWS Lambda function that runs the database rollover job** [CORRECT]
- (E) Correct option:
- (F) AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume. AWS Lambda supports standard rate and cron expressions for frequencies of up to once per minute.
- (G) Schedule expressions using rate or cron:
- (H) Incorrect options:
- (I) References:
- (J) https://aws.amazon.com/lambda/
- () https://docs.aws.amazon.com/lambda/latest/dg/services-cloudwatchevents-expressions.html

**Answer:**
Correct Answer: **Schedule a weekly Amazon EventBridge event cron expression to invoke an AWS Lambda function that runs the database rollover job**

---

## Question 37

**Q:** Which of the following is the most appropriate solution to meet these requirements?

**Options:**
- (A) Create a single EFS mount target in one AZ and allow all EC2 instances in other AZs to access it using the default mount target
- (B) Create EFS mount targets in each AZ and mount the EFS file system to EC2 instances in the same AZ as the mount target
- (C) Use Mountpoint for Amazon S3 to mount an S3 bucket on each EC2 instance and use it as a shared storage layer across Availability Zones
- (D) Create mount targets for Amazon EFS on an EC2 instance in each AZ and use them to serve as access points for other instances
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/efs/latest/ug/accessing-fs.html
- (G) Incorrect options:
- (H) Create a single EFS mount target in one AZ and allow all EC2 instances in other AZs to access it using the default mount target - Creating a single mount target in one AZ and having all EC2 instances across AZs access it leads to cross-AZ traffic, which increases latency and incurs data transfer costs. This setup ignores the purpose of EFS mount targets in multiple AZs and underutilizes the capability to serve traffic locally within each AZ.
- (I) References:
- (J) https://docs.aws.amazon.com/efs/latest/ug/accessing-fs.html
- () https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () https://docs.aws.amazon.com/efs/latest/ug/how-it-works.html
- () A startup's cloud infrastructure consists of a few Amazon EC2 instances, Amazon RDS instances and Amazon S3 storage. A year into their business operations, the startup is incurring costs that seem too high for their business requirements.
- () Which of the following options represents a valid cost-optimization solution?
- () Use AWS Cost Optimization Hub to get a report of Amazon EC2 instances that are either idle or have low utilization and use AWS Compute Optimizer to look at instance type recommendations
- () Use AWS Trusted Advisor checks on Amazon EC2 Reserved Instances to automatically renew reserved instances (RI). AWS Trusted advisor also suggests Amazon RDS idle database instances
- () Use Amazon S3 Storage class analysis to get recommendations for transitions of objects to Amazon S3 Glacier storage classes to reduce storage costs. You can also automate moving these objects into lower-cost storage tier using Lifecycle Policies
- () Use AWS Compute Optimizer recommendations to help you choose the optimal Amazon EC2 purchasing options and help reserve your instance capacities at reduced costs
- () AWS Compute Optimizer provides Amazon EC2 recommendations to help you improve performance, save money, or both. You can use these recommendations to decide whether to change to a new instance type. To make recommendations, Compute Optimizer analyzes your existing instance specifications and utilization metrics. The compiled data is then used to recommend which Amazon EC2 instance types are best able to handle the existing workload.
- () https://docs.aws.amazon.com/cost-management/latest/userguide/coh-optimization-strategies.html
- () https://aws.amazon.com/compute-optimizer/
- () https://aws.amazon.com/premiumsupport/technology/trusted-advisor/best-practice-checklist/
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/analytics-storage-class.html
- () A retail company uses AWS Cloud to manage its technology infrastructure. The company has deployed its consumer-focused web application on Amazon EC2-based web servers and uses Amazon RDS PostgreSQL database as the data store. The PostgreSQL database is set up in a private subnet that allows inbound traffic from selected Amazon EC2 instances. The database also uses AWS Key Management Service (AWS KMS) for encrypting data at rest.
- () Which of the following steps would you recommend to facilitate end-to-end security for the data-in-transit while accessing the database?
- () Create a new security group that blocks SSH from the selected Amazon EC2 instances into the database
- () Create a new network access control list (network ACL) that blocks SSH from the entire Amazon EC2 subnet into the database
- () Use IAM authentication to access the database instead of the database user's access credentials
- **() Configure Amazon RDS to use SSL for data in transit** [CORRECT]

**Answer:**
Correct Answer: **Configure Amazon RDS to use SSL for data in transit**

---

## Question 38

**Q:** Which of the following options represents a valid cost-optimization solution?

**Options:**
- (A) Use AWS Cost Optimization Hub to get a report of Amazon EC2 instances that are either idle or have low utilization and use AWS Compute Optimizer to look at instance type recommendations
- (B) Use AWS Trusted Advisor checks on Amazon EC2 Reserved Instances to automatically renew reserved instances (RI). AWS Trusted advisor also suggests Amazon RDS idle database instances
- (C) Use Amazon S3 Storage class analysis to get recommendations for transitions of objects to Amazon S3 Glacier storage classes to reduce storage costs. You can also automate moving these objects into lower-cost storage tier using Lifecycle Policies
- (D) Use AWS Compute Optimizer recommendations to help you choose the optimal Amazon EC2 purchasing options and help reserve your instance capacities at reduced costs
- (E) Correct option:
- (F) AWS Compute Optimizer provides Amazon EC2 recommendations to help you improve performance, save money, or both. You can use these recommendations to decide whether to change to a new instance type. To make recommendations, Compute Optimizer analyzes your existing instance specifications and utilization metrics. The compiled data is then used to recommend which Amazon EC2 instance types are best able to handle the existing workload.
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/cost-management/latest/userguide/coh-optimization-strategies.html
- (J) https://aws.amazon.com/compute-optimizer/
- () https://aws.amazon.com/premiumsupport/technology/trusted-advisor/best-practice-checklist/
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/analytics-storage-class.html
- () A retail company uses AWS Cloud to manage its technology infrastructure. The company has deployed its consumer-focused web application on Amazon EC2-based web servers and uses Amazon RDS PostgreSQL database as the data store. The PostgreSQL database is set up in a private subnet that allows inbound traffic from selected Amazon EC2 instances. The database also uses AWS Key Management Service (AWS KMS) for encrypting data at rest.
- () Which of the following steps would you recommend to facilitate end-to-end security for the data-in-transit while accessing the database?
- () Create a new security group that blocks SSH from the selected Amazon EC2 instances into the database
- () Create a new network access control list (network ACL) that blocks SSH from the entire Amazon EC2 subnet into the database
- () Use IAM authentication to access the database instead of the database user's access credentials
- () Configure Amazon RDS to use SSL for data in transit
- () via - https://aws.amazon.com/rds/features/security/
- () Use IAM authentication to access the database instead of the database user's access credentials - You can authenticate to your database instance using AWS Identity and Access Management (IAM) database authentication. IAM database authentication works with MySQL and PostgreSQL. With this authentication method, you don't need to use a password when you connect to a database instance. Instead, you use an authentication token.
- () IAM authentication is just another way to authenticate the user's credentials while accessing the database. It would not significantly enhance the security in a way that enabling SSL does by facilitating the in-transit encryption for the database.
- () Both these options are added as distractors. You cannot SSH into an Amazon RDS database instance.
- () https://aws.amazon.com/rds/features/security/
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_MySQL.html#MySQL.Concepts.SSLSupport
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html#PostgreSQL.Concepts.General.SSL
- () https://aws.amazon.com/blogs/database/using-iam-authentication-to-connect-with-pgadmin-amazon-aurora-postgresql-or-amazon-rds-for-postgresql/
- () Amazon Route 53 is configured to route traffic to two Network Load Balancer nodes belonging to two Availability Zones (AZs): AZ-A and AZ-B. Cross-zone load balancing is disabled. AZ-A has four targets and AZ-B has six targets.
- () Which of the below statements is true about traffic distribution to the target instances from Amazon Route 53?
- **() Each of the four targets in AZ-A receives 12.5% of the traffic** [CORRECT]
- () Each of the four targets in AZ-A receives 8% of the traffic
- () Each of the six targets in AZ-B receives 10% of the traffic
- () Each of the four targets in AZ-A receives 10% of the traffic

**Answer:**
Correct Answer: **Each of the four targets in AZ-A receives 12.5% of the traffic**

---

## Question 39

**Q:** Which of the following steps would you recommend to facilitate end-to-end security for the data-in-transit while accessing the database?

**Options:**
- (A) Create a new security group that blocks SSH from the selected Amazon EC2 instances into the database
- (B) Create a new network access control list (network ACL) that blocks SSH from the entire Amazon EC2 subnet into the database
- (C) Use IAM authentication to access the database instead of the database user's access credentials
- (D) Configure Amazon RDS to use SSL for data in transit
- (E) Correct option:
- (F) via - https://aws.amazon.com/rds/features/security/
- (G) Incorrect options:
- (H) Use IAM authentication to access the database instead of the database user's access credentials - You can authenticate to your database instance using AWS Identity and Access Management (IAM) database authentication. IAM database authentication works with MySQL and PostgreSQL. With this authentication method, you don't need to use a password when you connect to a database instance. Instead, you use an authentication token.
- (I) IAM authentication is just another way to authenticate the user's credentials while accessing the database. It would not significantly enhance the security in a way that enabling SSL does by facilitating the in-transit encryption for the database.
- (J) Both these options are added as distractors. You cannot SSH into an Amazon RDS database instance.
- () References:
- () https://aws.amazon.com/rds/features/security/
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_MySQL.html#MySQL.Concepts.SSLSupport
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html#PostgreSQL.Concepts.General.SSL
- () https://aws.amazon.com/blogs/database/using-iam-authentication-to-connect-with-pgadmin-amazon-aurora-postgresql-or-amazon-rds-for-postgresql/
- () Amazon Route 53 is configured to route traffic to two Network Load Balancer nodes belonging to two Availability Zones (AZs): AZ-A and AZ-B. Cross-zone load balancing is disabled. AZ-A has four targets and AZ-B has six targets.
- () Which of the below statements is true about traffic distribution to the target instances from Amazon Route 53?
- () Each of the four targets in AZ-A receives 12.5% of the traffic
- () Each of the four targets in AZ-A receives 8% of the traffic
- () Each of the six targets in AZ-B receives 10% of the traffic
- () Each of the four targets in AZ-A receives 10% of the traffic
- () The nodes for your load balancer distribute requests from clients to registered targets. When cross-zone load balancing is enabled, each load balancer node distributes traffic across the registered targets in all enabled Availability Zones (AZs). When cross-zone load balancing is disabled, each load balancer node distributes traffic only across the registered targets in its Availability Zone (AZ).
- () Amazon Route 53 will distribute traffic such that each load balancer node receives 50% of the traffic from the clients.
- () If cross-zone load balancing is disabled: 1. Each of the four targets in AZ-A receives 12.5% of the traffic. 2. Each of the six targets in AZ-B receives 8.3% of the traffic.
- () This is because each load balancer node can route its 50% of the client traffic only to targets in its Availability Zone (AZ).
- () Each of the six targets in AZ-B receives 10% of the traffic - As mentioned above in the correct explanation, each of the six targets in AZ-B receives 8.3% of the traffic.
- () Each of the four targets in AZ-A receives 8% of the traffic - As mentioned above in the correct explanation, each of the four targets in AZ-A receives 12.5% of the traffic.
- () Each of the four targets in AZ-A receives 10% of the traffic - As mentioned above in the correct explanation, each of the four targets in AZ-A receives 12.5% of the traffic.
- () Reference:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/how-elastic-load-balancing-works.html
- () Which scaling strategy should a solutions architect recommend to meet these requirements?
- () Configure step scaling policies based on EC2 CPU utilization. Use CloudWatch alarms to trigger scaling actions when utilization crosses defined thresholds with incremental adjustments
- () Set up simple scaling policies with longer cooldown periods to avoid rapid scaling. Trigger scale-out events based on average network throughput
- **() Use predictive scaling for the Auto Scaling group to analyze daily and weekly patterns, and configure dynamic scaling with target tracking policies to respond to real-time traffic changes** [CORRECT]
- () Implement scheduled scaling actions based on pre-defined time windows from historical traffic data. Adjust instance count manually for known high-traffic hours

**Answer:**
Correct Answer: **Use predictive scaling for the Auto Scaling group to analyze daily and weekly patterns, and configure dynamic scaling with target tracking policies to respond to real-time traffic changes**

---

## Question 40

**Q:** Which of the below statements is true about traffic distribution to the target instances from Amazon Route 53?

**Options:**
- (A) Each of the four targets in AZ-A receives 12.5% of the traffic
- (B) Each of the four targets in AZ-A receives 8% of the traffic
- (C) Each of the six targets in AZ-B receives 10% of the traffic
- (D) Each of the four targets in AZ-A receives 10% of the traffic
- (E) Correct option:
- (F) The nodes for your load balancer distribute requests from clients to registered targets. When cross-zone load balancing is enabled, each load balancer node distributes traffic across the registered targets in all enabled Availability Zones (AZs). When cross-zone load balancing is disabled, each load balancer node distributes traffic only across the registered targets in its Availability Zone (AZ).
- (G) Amazon Route 53 will distribute traffic such that each load balancer node receives 50% of the traffic from the clients.
- (H) If cross-zone load balancing is disabled: 1. Each of the four targets in AZ-A receives 12.5% of the traffic. 2. Each of the six targets in AZ-B receives 8.3% of the traffic.
- (I) This is because each load balancer node can route its 50% of the client traffic only to targets in its Availability Zone (AZ).
- (J) Incorrect options:
- () Each of the six targets in AZ-B receives 10% of the traffic - As mentioned above in the correct explanation, each of the six targets in AZ-B receives 8.3% of the traffic.
- () Each of the four targets in AZ-A receives 8% of the traffic - As mentioned above in the correct explanation, each of the four targets in AZ-A receives 12.5% of the traffic.
- () Each of the four targets in AZ-A receives 10% of the traffic - As mentioned above in the correct explanation, each of the four targets in AZ-A receives 12.5% of the traffic.
- () Reference:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/how-elastic-load-balancing-works.html
- () Which scaling strategy should a solutions architect recommend to meet these requirements?
- () Configure step scaling policies based on EC2 CPU utilization. Use CloudWatch alarms to trigger scaling actions when utilization crosses defined thresholds with incremental adjustments
- () Set up simple scaling policies with longer cooldown periods to avoid rapid scaling. Trigger scale-out events based on average network throughput
- **() Use predictive scaling for the Auto Scaling group to analyze daily and weekly patterns, and configure dynamic scaling with target tracking policies to respond to real-time traffic changes** [CORRECT]
- () Implement scheduled scaling actions based on pre-defined time windows from historical traffic data. Adjust instance count manually for known high-traffic hours
- () via - https://aws.amazon.com/blogs/compute/introducing-native-support-for-predictive-scaling-with-amazon-ec2-auto-scaling/
- () Set up simple scaling policies with longer cooldown periods to avoid rapid scaling. Trigger scale-out events based on average network throughput - Simple scaling policies perform one action per alarm and are limited in flexibility. Long cooldowns reduce the frequency of scaling actions but can delay necessary adjustments. It also lacks the ability to scale proactively or adapt to complex usage patterns.
- () References:
- () https://aws.amazon.com/blogs/compute/introducing-native-support-for-predictive-scaling-with-amazon-ec2-auto-scaling/
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-predictive-scaling.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-scheduled-scaling.html
- () A ride-sharing company wants to improve the ride-tracking system that stores GPS coordinates for all rides. The engineering team at the company is looking for a NoSQL database that has single-digit millisecond latency, can scale horizontally, and is serverless, so that they can perform high-frequency lookups reliably.

**Answer:**
Correct Answer: **Use predictive scaling for the Auto Scaling group to analyze daily and weekly patterns, and configure dynamic scaling with target tracking policies to respond to real-time traffic changes**

---

## Question 41

**Q:** Which scaling strategy should a solutions architect recommend to meet these requirements?

**Options:**
- (A) Configure step scaling policies based on EC2 CPU utilization. Use CloudWatch alarms to trigger scaling actions when utilization crosses defined thresholds with incremental adjustments
- (B) Set up simple scaling policies with longer cooldown periods to avoid rapid scaling. Trigger scale-out events based on average network throughput
- **(C) Use predictive scaling for the Auto Scaling group to analyze daily and weekly patterns, and configure dynamic scaling with target tracking policies to respond to real-time traffic changes** [CORRECT]
- (D) Implement scheduled scaling actions based on pre-defined time windows from historical traffic data. Adjust instance count manually for known high-traffic hours
- (E) Correct option:
- (F) via - https://aws.amazon.com/blogs/compute/introducing-native-support-for-predictive-scaling-with-amazon-ec2-auto-scaling/
- (G) Incorrect options:
- (H) Set up simple scaling policies with longer cooldown periods to avoid rapid scaling. Trigger scale-out events based on average network throughput - Simple scaling policies perform one action per alarm and are limited in flexibility. Long cooldowns reduce the frequency of scaling actions but can delay necessary adjustments. It also lacks the ability to scale proactively or adapt to complex usage patterns.
- (I) References:
- (J) https://aws.amazon.com/blogs/compute/introducing-native-support-for-predictive-scaling-with-amazon-ec2-auto-scaling/
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-predictive-scaling.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-scaling-simple-step.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-scheduled-scaling.html
- () A ride-sharing company wants to improve the ride-tracking system that stores GPS coordinates for all rides. The engineering team at the company is looking for a NoSQL database that has single-digit millisecond latency, can scale horizontally, and is serverless, so that they can perform high-frequency lookups reliably.

**Answer:**
Correct Answer: **Use predictive scaling for the Auto Scaling group to analyze daily and weekly patterns, and configure dynamic scaling with target tracking policies to respond to real-time traffic changes**

---

## Question 42

**Q:** As a Solutions Architect, which database do you recommend for their requirements?

**Options:**
- (A) Amazon ElastiCache
- (B) Amazon Relational Database Service (Amazon RDS)
- (C) Amazon DynamoDB
- (D) Amazon Neptune
- (E) Correct option:
- (F) Sample Amazon DynamoDB solution for Real time applications:
- (G) via - https://aws.amazon.com/dynamodb/
- (H) Incorrect options:
- (I) How Amazon ElastiCache works:
- (J) via - https://aws.amazon.com/elasticache/
- () Example Use cases of Amazon Neptune:
- () via - https://aws.amazon.com/neptune/
- () References:
- () https://aws.amazon.com/dynamodb/
- () https://aws.amazon.com/elasticache/
- () https://aws.amazon.com/neptune/
- () A company's business logic is built on several microservices that are running in the on-premises data center. They currently communicate using a message broker that supports the MQTT protocol. The company is looking at migrating these applications and the message broker to AWS Cloud without changing the application logic.
- () Which technology allows you to get a managed message broker that supports the MQTT protocol?
- () Amazon MQ
- () Amazon Simple Notification Service (Amazon SNS)
- () Amazon Kinesis Data Streams
- () Amazon Simple Queue Service (Amazon SQS)
- () Therefore, the only possible answer is Amazon MQ.
- () Incorrect option:
- () Amazon Kinesis Data Streams - Amazon Kinesis Data Streams (KDS) is a massively scalable and durable real-time data streaming service. KDS can continuously capture gigabytes of data per second from hundreds of thousands of sources such as website clickstreams, database event streams, financial transactions, social media feeds, IT logs, and location-tracking events.
- () Amazon Simple Notification Service (Amazon SNS) - Amazon Simple Notification Service (Amazon SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging.
- () Amazon SNS, Amazon SQS, and Amazon Kinesis are AWS's proprietary technologies and do not come with MQTT compatibility.
- () https://aws.amazon.com/amazon-mq/
- () A company uses Application Load Balancers in multiple AWS Regions. The Application Load Balancers receive inconsistent traffic that varies throughout the year. The engineering team at the company needs to allow the IP addresses of the Application Load Balancers in the on-premises firewall to enable connectivity.
- () Which of the following represents the MOST scalable solution with minimal configuration changes?
- () Set up a Network Load Balancer in one Region. Register the private IP addresses of the Application Load Balancers in different Regions with the Network Load Balancer. Configure the on-premises firewall's rule to allow the Elastic IP address attached to the Network Load Balancer
- () Develop an AWS Lambda script to get the IP addresses of the Application Load Balancers in different Regions. Configure the on-premises firewall's rule to allow the IP addresses of the Application Load Balancers
- **() Set up AWS Global Accelerator. Register the Application Load Balancers in different Regions to the AWS Global Accelerator. Configure the on-premises firewall's rule to allow static IP addresses associated with the AWS Global Accelerator** [CORRECT]

**Answer:**
Correct Answer: **Set up AWS Global Accelerator. Register the Application Load Balancers in different Regions to the AWS Global Accelerator. Configure the on-premises firewall's rule to allow static IP addresses associated with the AWS Global Accelerator**

---

## Question 43

**Q:** Which technology allows you to get a managed message broker that supports the MQTT protocol?

**Options:**
- (A) Amazon MQ
- (B) Amazon Simple Notification Service (Amazon SNS)
- (C) Amazon Kinesis Data Streams
- (D) Amazon Simple Queue Service (Amazon SQS)
- (E) Correct option:
- (F) Therefore, the only possible answer is Amazon MQ.
- (G) Incorrect option:
- (H) Amazon Kinesis Data Streams - Amazon Kinesis Data Streams (KDS) is a massively scalable and durable real-time data streaming service. KDS can continuously capture gigabytes of data per second from hundreds of thousands of sources such as website clickstreams, database event streams, financial transactions, social media feeds, IT logs, and location-tracking events.
- (I) Amazon Simple Notification Service (Amazon SNS) - Amazon Simple Notification Service (Amazon SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging.
- (J) Amazon SNS, Amazon SQS, and Amazon Kinesis are AWS's proprietary technologies and do not come with MQTT compatibility.
- () References:
- () https://aws.amazon.com/amazon-mq/
- () A company uses Application Load Balancers in multiple AWS Regions. The Application Load Balancers receive inconsistent traffic that varies throughout the year. The engineering team at the company needs to allow the IP addresses of the Application Load Balancers in the on-premises firewall to enable connectivity.
- () Which of the following represents the MOST scalable solution with minimal configuration changes?
- () Set up a Network Load Balancer in one Region. Register the private IP addresses of the Application Load Balancers in different Regions with the Network Load Balancer. Configure the on-premises firewall's rule to allow the Elastic IP address attached to the Network Load Balancer
- () Develop an AWS Lambda script to get the IP addresses of the Application Load Balancers in different Regions. Configure the on-premises firewall's rule to allow the IP addresses of the Application Load Balancers
- **() Set up AWS Global Accelerator. Register the Application Load Balancers in different Regions to the AWS Global Accelerator. Configure the on-premises firewall's rule to allow static IP addresses associated with the AWS Global Accelerator** [CORRECT]
- () Migrate all Application Load Balancers in different Regions to the Network Load Balancers. Configure the on-premises firewall's rule to allow the Elastic IP addresses of all the Network Load Balancers
- () AWS Global Accelerator is a networking service that helps you improve the availability and performance of the applications that you offer to your global users. AWS Global Accelerator is easy to set up, configure, and manage. It provides static IP addresses that provide a fixed entry point to your applications and eliminate the complexity of managing specific IP addresses for different AWS Regions and Availability Zones.
- () Associate the static IP addresses provided by AWS Global Accelerator to regional AWS resources or endpoints, such as Network Load Balancers, Application Load Balancers, Amazon EC2 Instances, and Elastic IP addresses. The IP addresses are anycast from AWS edge locations so they provide onboarding to the AWS global network close to your users.
- () Simplified and resilient traffic routing for multi-Region applications using AWS Global Accelerator:
- () via - https://aws.amazon.com/global-accelerator/
- () Incorrect options:
- () Set up a Network Load Balancer in one Region. Register the private IP addresses of the Application Load Balancers in different Regions with the Network Load Balancer. Configure the on-premises firewall's rule to allow the Elastic IP address attached to the Network Load Balancer - Using a single Network Load Balancer is not possible across AWS regions since an Network Load Balancer is Region bound. Multiple Network Load Balancers have to be registered for the on-premises firewall.
- () Reference:
- () https://aws.amazon.com/global-accelerator/faqs/
- () As an e-sport tournament hosting company, you have servers that need to scale and be highly available. Therefore you have deployed an Elastic Load Balancing (ELB) with an Auto Scaling group (ASG) across 3 Availability Zones (AZs). When e-sport tournaments are running, the servers need to scale quickly. And when tournaments are done, the servers can be idle. As a general rule, you would like to be highly available, have the capacity to scale and optimize your costs.
- () What do you recommend? (Select two)
- () Use Dedicated hosts for the minimum capacity
- () Set the minimum capacity to 1
- () Correct selection
- () Set the minimum capacity to 2
- () Set the minimum capacity to 3
- () Use Reserved Instances (RIs) for the minimum capacity
- () Correct options:
- () An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
- () You configure the size of your Auto Scaling group by setting the minimum, maximum, and desired capacity. The minimum and maximum capacity are required to create an Auto Scaling group, while the desired capacity is optional. If you do not define your desired capacity upfront, it defaults to your minimum capacity.

**Answer:**
Correct Answer: **Set up AWS Global Accelerator. Register the Application Load Balancers in different Regions to the AWS Global Accelerator. Configure the on-premises firewall's rule to allow static IP addresses associated with the AWS Global Accelerator**

---

## Question 44

**Q:** Which of the following represents the MOST scalable solution with minimal configuration changes?

**Options:**
- (A) Set up a Network Load Balancer in one Region. Register the private IP addresses of the Application Load Balancers in different Regions with the Network Load Balancer. Configure the on-premises firewall's rule to allow the Elastic IP address attached to the Network Load Balancer
- (B) Develop an AWS Lambda script to get the IP addresses of the Application Load Balancers in different Regions. Configure the on-premises firewall's rule to allow the IP addresses of the Application Load Balancers
- **(C) Set up AWS Global Accelerator. Register the Application Load Balancers in different Regions to the AWS Global Accelerator. Configure the on-premises firewall's rule to allow static IP addresses associated with the AWS Global Accelerator** [CORRECT]
- (D) Migrate all Application Load Balancers in different Regions to the Network Load Balancers. Configure the on-premises firewall's rule to allow the Elastic IP addresses of all the Network Load Balancers
- (E) Correct option:
- (F) AWS Global Accelerator is a networking service that helps you improve the availability and performance of the applications that you offer to your global users. AWS Global Accelerator is easy to set up, configure, and manage. It provides static IP addresses that provide a fixed entry point to your applications and eliminate the complexity of managing specific IP addresses for different AWS Regions and Availability Zones.
- (G) Associate the static IP addresses provided by AWS Global Accelerator to regional AWS resources or endpoints, such as Network Load Balancers, Application Load Balancers, Amazon EC2 Instances, and Elastic IP addresses. The IP addresses are anycast from AWS edge locations so they provide onboarding to the AWS global network close to your users.
- (H) Simplified and resilient traffic routing for multi-Region applications using AWS Global Accelerator:
- (I) via - https://aws.amazon.com/global-accelerator/
- (J) Incorrect options:
- () Set up a Network Load Balancer in one Region. Register the private IP addresses of the Application Load Balancers in different Regions with the Network Load Balancer. Configure the on-premises firewall's rule to allow the Elastic IP address attached to the Network Load Balancer - Using a single Network Load Balancer is not possible across AWS regions since an Network Load Balancer is Region bound. Multiple Network Load Balancers have to be registered for the on-premises firewall.
- () Reference:
- () https://aws.amazon.com/global-accelerator/faqs/
- () As an e-sport tournament hosting company, you have servers that need to scale and be highly available. Therefore you have deployed an Elastic Load Balancing (ELB) with an Auto Scaling group (ASG) across 3 Availability Zones (AZs). When e-sport tournaments are running, the servers need to scale quickly. And when tournaments are done, the servers can be idle. As a general rule, you would like to be highly available, have the capacity to scale and optimize your costs.
- () What do you recommend? (Select two)
- () Use Dedicated hosts for the minimum capacity
- () Set the minimum capacity to 1
- () Correct selection
- () Set the minimum capacity to 2
- () Set the minimum capacity to 3
- () Use Reserved Instances (RIs) for the minimum capacity
- () Correct options:
- () An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
- () You configure the size of your Auto Scaling group by setting the minimum, maximum, and desired capacity. The minimum and maximum capacity are required to create an Auto Scaling group, while the desired capacity is optional. If you do not define your desired capacity upfront, it defaults to your minimum capacity.
- () An Auto Scaling group is elastic as long as it has different values for minimum and maximum capacity. All requests to change the Auto Scaling group's desired capacity (either by manual scaling or automatic scaling) must fall within these limits.
- () Here, even though our ASG is deployed across 3 Availability Zones (AZs), the minimum capacity to be highly available is 2. When we specify 2 as the minimum capacity, the ASG would create these 2 instances in separate Availability Zones (AZs). If demand goes up, the ASG would spin up a new instance in the third Availability Zone (AZ). Later as the demand subsides, the ASG would scale-in and the instance count would be back to 2.
- () In case of an Availability Zone (AZ) outage, the instance in that Availability Zone (AZ) would go down however the other instance would still be available. The ASG would provision the replacement instance in the third Availability Zone (AZ) to keep the minimum count to 2.
- () Set the minimum capacity to 1 - This is not failure proof, since only one instance will be maintained consistently and this will be from only one Availability Zone (AZ).
- () Set the minimum capacity to 3 - This is not a cost-effective option, as two instances in two different Availability Zones (AZs) are enough to make the architecture disaster-proof.
- () Use Dedicated hosts for the minimum capacity - As there is no use-case to utilize existing per-socket, per-core, or per-VM software licenses or to run the instance on a dedicated physical host, so the option to use dedicated hosts for the minimum capacity is ruled out.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroup.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-capacity-limits.html
- () A company has recently created a new department to handle their services workload. An IT team has been asked to create a custom VPC to isolate the resources created in this new department. They have set up the public subnet and internet gateway (IGW). However, they are not able to ping the Amazon EC2 instances with elastic IP address (EIP) launched in the newly created VPC.
- () As a Solutions Architect, the team has requested your help. How will you troubleshoot this scenario? (Select two)
- () Contact AWS support to map your VPC with subnet
- () Check if the security groups allow ping from the source
- () Disable Source / Destination check on the Amazon EC2 instance
- () Create a secondary internet gateway to attach with public subnet and move the current internet gateway to private and write route tables

**Answer:**
Correct Answer: **Set up AWS Global Accelerator. Register the Application Load Balancers in different Regions to the AWS Global Accelerator. Configure the on-premises firewall's rule to allow static IP addresses associated with the AWS Global Accelerator**

---

## Question 45

**Q:** What do you recommend? (Select two)

**Options:**
- **(A) Use Dedicated hosts for the minimum capacity** [CORRECT]
- (B) Set the minimum capacity to 1
- (C) Correct selection
- (D) Set the minimum capacity to 2
- (E) Set the minimum capacity to 3
- (F) Use Reserved Instances (RIs) for the minimum capacity
- (G) Correct options:
- (H) An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
- (I) You configure the size of your Auto Scaling group by setting the minimum, maximum, and desired capacity. The minimum and maximum capacity are required to create an Auto Scaling group, while the desired capacity is optional. If you do not define your desired capacity upfront, it defaults to your minimum capacity.
- (J) An Auto Scaling group is elastic as long as it has different values for minimum and maximum capacity. All requests to change the Auto Scaling group's desired capacity (either by manual scaling or automatic scaling) must fall within these limits.
- () Here, even though our ASG is deployed across 3 Availability Zones (AZs), the minimum capacity to be highly available is 2. When we specify 2 as the minimum capacity, the ASG would create these 2 instances in separate Availability Zones (AZs). If demand goes up, the ASG would spin up a new instance in the third Availability Zone (AZ). Later as the demand subsides, the ASG would scale-in and the instance count would be back to 2.
- () In case of an Availability Zone (AZ) outage, the instance in that Availability Zone (AZ) would go down however the other instance would still be available. The ASG would provision the replacement instance in the third Availability Zone (AZ) to keep the minimum count to 2.
- () Incorrect options:
- () Set the minimum capacity to 1 - This is not failure proof, since only one instance will be maintained consistently and this will be from only one Availability Zone (AZ).
- () Set the minimum capacity to 3 - This is not a cost-effective option, as two instances in two different Availability Zones (AZs) are enough to make the architecture disaster-proof.
- () Use Dedicated hosts for the minimum capacity - As there is no use-case to utilize existing per-socket, per-core, or per-VM software licenses or to run the instance on a dedicated physical host, so the option to use dedicated hosts for the minimum capacity is ruled out.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroup.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-capacity-limits.html
- () A company has recently created a new department to handle their services workload. An IT team has been asked to create a custom VPC to isolate the resources created in this new department. They have set up the public subnet and internet gateway (IGW). However, they are not able to ping the Amazon EC2 instances with elastic IP address (EIP) launched in the newly created VPC.
- () As a Solutions Architect, the team has requested your help. How will you troubleshoot this scenario? (Select two)
- () Contact AWS support to map your VPC with subnet
- () Check if the security groups allow ping from the source
- () Disable Source / Destination check on the Amazon EC2 instance
- () Create a secondary internet gateway to attach with public subnet and move the current internet gateway to private and write route tables
- () Check if the route table is configured with internet gateway
- () An internet gateway (IGW) is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. An internet gateway serves two purposes: to provide a target in your VPC route tables for internet-routable traffic, and to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses. An internet gateway supports IPv4 and IPv6 traffic.
- () To enable access to or from the internet for instances in a subnet in a VPC, you must do the following: 1. Attach an internet gateway to your VPC. 2. Add a route to your subnet's route table that directs internet-bound traffic to the internet gateway. 3. Ensure that instances in your subnet have a globally unique IP address 4. Ensure that your network access control lists and security group rules allow the relevant traffic to flow to and from your instance.
- () A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed. After creating an IGW, make sure the route tables are updated. Additionally, ensure the security group allows the ICMP protocol for ping requests.
- () The following are the characteristics of security group rules: 1. By default, security groups allow all outbound traffic. 2. Security group rules are always permissive; you can't create rules that deny access. 3. Security groups are stateful
- () Create a secondary internet gateway to attach with public subnet and move the current internet gateway to private and write route tables - There is no such thing as a secondary IGW. This option is added as a distractor.
- () Contact AWS support to map your VPC with subnet - You cannot contact AWS support to map your VPC with the subnet.
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html#change_source_dest_check
- () How can you implement an efficient cost strategy for your Amazon S3 bucket? (Select two)

**Answer:**
Correct Answer: **Use Dedicated hosts for the minimum capacity**

---

## Question 46

**Q:** As a Solutions Architect, the team has requested your help. How will you troubleshoot this scenario? (Select two)

**Options:**
- **(A) Contact AWS support to map your VPC with subnet** [CORRECT]
- (B) Correct selection
- (C) Check if the security groups allow ping from the source
- (D) Disable Source / Destination check on the Amazon EC2 instance
- (E) Create a secondary internet gateway to attach with public subnet and move the current internet gateway to private and write route tables
- (F) Check if the route table is configured with internet gateway
- (G) Correct options:
- (H) An internet gateway (IGW) is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. An internet gateway serves two purposes: to provide a target in your VPC route tables for internet-routable traffic, and to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses. An internet gateway supports IPv4 and IPv6 traffic.
- (I) To enable access to or from the internet for instances in a subnet in a VPC, you must do the following: 1. Attach an internet gateway to your VPC. 2. Add a route to your subnet's route table that directs internet-bound traffic to the internet gateway. 3. Ensure that instances in your subnet have a globally unique IP address 4. Ensure that your network access control lists and security group rules allow the relevant traffic to flow to and from your instance.
- (J) A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed. After creating an IGW, make sure the route tables are updated. Additionally, ensure the security group allows the ICMP protocol for ping requests.
- () The following are the characteristics of security group rules: 1. By default, security groups allow all outbound traffic. 2. Security group rules are always permissive; you can't create rules that deny access. 3. Security groups are stateful
- () Incorrect options:
- () Create a secondary internet gateway to attach with public subnet and move the current internet gateway to private and write route tables - There is no such thing as a secondary IGW. This option is added as a distractor.
- () Contact AWS support to map your VPC with subnet - You cannot contact AWS support to map your VPC with the subnet.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html#change_source_dest_check
- () How can you implement an efficient cost strategy for your Amazon S3 bucket? (Select two)
- () Create a Lifecycle Policy to transition all objects to Amazon S3 Glacier after 180 days
- () Create a Lifecycle Policy to transition objects to Amazon S3 Glacier using a prefix after 180 days
- () Create a Lifecycle Policy to transition objects to Amazon S3 One Zone IA using a prefix after 45 days
- () Create a Lifecycle Policy to transition all objects to Amazon S3 Standard IA after 45 days
- () Create a Lifecycle Policy to transition objects to Amazon S3 Standard IA using a prefix after 45 days
- () To manage your S3 objects, so they are stored cost-effectively throughout their lifecycle, configure their Amazon S3 Lifecycle. An S3 Lifecycle configuration is a set of rules that define actions that Amazon S3 applies to a group of objects. There are two types of actions:
- () Transition actions — Define when objects transition to another storage class. For example, you might choose to transition objects to the S3 Standard-IA storage class 30 days after you created them, or archive objects to the S3 Glacier storage class one year after creating them.
- () Expiration actions — Define when objects expire. Amazon S3 deletes expired objects on your behalf.
- () Amazon S3 Standard-IA is for data that is accessed less frequently but requires rapid access when needed. Amazon S3 Standard-IA offers high durability, high throughput, and low latency of S3 Standard, with a low per gigabyte storage price and per gigabyte retrieval fee. This combination of low cost and high performance makes Amazon S3 Standard-IA ideal for long-term storage, backups, and as a data store for disaster recovery files. The minimum storage duration charge is 30 days.
- () As the use-case mentions that after 45 days, image files are rarely requested, but the thumbnails still are. So you need to use a prefix while configuring the Lifecycle Policy so that only objects in the s3://my-bucket/images are transitioned to Standard IA and not all the objects in the bucket.
- () Amazon S3 Glacier and S3 Glacier Deep Archive are secure, durable, and extremely low-cost Amazon S3 cloud storage classes for data archiving and long-term backup. They are designed to deliver 99.999999999% durability, and provide comprehensive security and compliance capabilities that can help meet even the most stringent regulatory requirements.
- () Create a Lifecycle Policy to transition all objects to Amazon S3 Standard IA after 45 days - As discussed above, you need to use a prefix while configuring the Lifecycle Policy so that only objects in the s3://my-bucket/images are transitioned to Amazon S3 Standard IA and not all the objects in the bucket.
- () Create a Lifecycle Policy to transition objects to Amazon S3 Glacier using a prefix after 180 days - After 180 days, you can move all the objects to Amazon S3 Glacier storage as per the use case. Glacier doesn't need prefixes for the given use-case.
- () Amazon S3 One Zone-IA is for data that is accessed less frequently but requires rapid access when needed. Unlike other S3 Storage Classes which store data in a minimum of three Availability Zones (AZs), S3 One Zone-IA stores data in a single AZ and costs 20% less than S3 Standard-IA. The minimum storage duration charge is 30 days.
- () Finally, Amazon S3 One Zone IA will not achieve the necessary availability in case an Availability Zone (AZ) goes down.
- () https://aws.amazon.com/s3/storage-classes/
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html

**Answer:**
Correct Answer: **Contact AWS support to map your VPC with subnet**

---

## Question 47

**Q:** How can you implement an efficient cost strategy for your Amazon S3 bucket? (Select two)

**Options:**
- (A) Correct selection
- (B) Create a Lifecycle Policy to transition all objects to Amazon S3 Glacier after 180 days
- (C) Create a Lifecycle Policy to transition objects to Amazon S3 Glacier using a prefix after 180 days
- (D) Create a Lifecycle Policy to transition objects to Amazon S3 One Zone IA using a prefix after 45 days
- (E) Create a Lifecycle Policy to transition all objects to Amazon S3 Standard IA after 45 days
- (F) Create a Lifecycle Policy to transition objects to Amazon S3 Standard IA using a prefix after 45 days
- (G) Correct options:
- (H) To manage your S3 objects, so they are stored cost-effectively throughout their lifecycle, configure their Amazon S3 Lifecycle. An S3 Lifecycle configuration is a set of rules that define actions that Amazon S3 applies to a group of objects. There are two types of actions:
- (I) Transition actions — Define when objects transition to another storage class. For example, you might choose to transition objects to the S3 Standard-IA storage class 30 days after you created them, or archive objects to the S3 Glacier storage class one year after creating them.
- (J) Expiration actions — Define when objects expire. Amazon S3 deletes expired objects on your behalf.
- () Amazon S3 Standard-IA is for data that is accessed less frequently but requires rapid access when needed. Amazon S3 Standard-IA offers high durability, high throughput, and low latency of S3 Standard, with a low per gigabyte storage price and per gigabyte retrieval fee. This combination of low cost and high performance makes Amazon S3 Standard-IA ideal for long-term storage, backups, and as a data store for disaster recovery files. The minimum storage duration charge is 30 days.
- () As the use-case mentions that after 45 days, image files are rarely requested, but the thumbnails still are. So you need to use a prefix while configuring the Lifecycle Policy so that only objects in the s3://my-bucket/images are transitioned to Standard IA and not all the objects in the bucket.
- () Amazon S3 Glacier and S3 Glacier Deep Archive are secure, durable, and extremely low-cost Amazon S3 cloud storage classes for data archiving and long-term backup. They are designed to deliver 99.999999999% durability, and provide comprehensive security and compliance capabilities that can help meet even the most stringent regulatory requirements.
- () Incorrect options:
- () Create a Lifecycle Policy to transition all objects to Amazon S3 Standard IA after 45 days - As discussed above, you need to use a prefix while configuring the Lifecycle Policy so that only objects in the s3://my-bucket/images are transitioned to Amazon S3 Standard IA and not all the objects in the bucket.
- () Create a Lifecycle Policy to transition objects to Amazon S3 Glacier using a prefix after 180 days - After 180 days, you can move all the objects to Amazon S3 Glacier storage as per the use case. Glacier doesn't need prefixes for the given use-case.
- () Amazon S3 One Zone-IA is for data that is accessed less frequently but requires rapid access when needed. Unlike other S3 Storage Classes which store data in a minimum of three Availability Zones (AZs), S3 One Zone-IA stores data in a single AZ and costs 20% less than S3 Standard-IA. The minimum storage duration charge is 30 days.
- () Finally, Amazon S3 One Zone IA will not achieve the necessary availability in case an Availability Zone (AZ) goes down.
- () References:
- () https://aws.amazon.com/s3/storage-classes/
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html
- () What do you recommend?
- () Create a read-replica Auto Scaling policy for the PostgreSQL database to dynamically add replicas during peak load. Distribute traffic evenly using an RDS proxy with failover configuration
- () Enable Multi-AZ deployment for the primary RDS instance to improve write resilience and fault tolerance. Use Multi-AZ standby failover to distribute reads during peak hours
- **() Place an Amazon ElastiCache for Redis cluster in front of the PostgreSQL database. Modify the application to cache recent location reads and updates in Redis, using a TTL-based eviction strategy** [CORRECT]
- () Migrate the location data to Amazon OpenSearch Service and use its geospatial indexing features to retrieve and store coordinates in near real-time. Visualize tracking data using OpenSearch Dashboards
- () Correct option:
- () This solution is the most cost-effective and scalable approach for improving the performance of a real-time location tracking workload where frequent updates and reads are required per second.
- () Amazon ElastiCache for Redis is a fully managed, in-memory data store that offers sub-millisecond latency for read and write operations. It is ideal for workloads that involve frequent, short-lived data interactions, such as tracking a user's changing GPS coordinates in real time. Instead of hitting the Amazon RDS for PostgreSQL database for every update or query, the application can cache these values temporarily in Redis.
- () Redis natively supports geospatial data types and commands like GEOADD, GEORADIUS, and GEODIST, making it a perfect fit for storing and querying latitude and longitude data. This means the app can quickly retrieve all drivers within a radius of a user without putting pressure on the relational database.
- () To maintain data freshness and avoid memory bloat, a TTL (Time To Live) policy can be used on each cache entry—ensuring that each player's location automatically expires after, say, 30 seconds unless refreshed. This TTL-based eviction strategy helps keep the dataset current while minimizing the Redis memory footprint.
- () Working with geospatial data in Amazon ElastiCache for Redis:
- () via - https://aws.amazon.com/blogs/database/working-with-geospatial-data-in-amazon-elasticache-for-redis/
- () Enable Multi-AZ deployment for the primary RDS instance to improve write resilience and fault tolerance. Use Multi-AZ standby failover to distribute reads during peak hours - Multi-AZ deployments improve availability and failover, not scalability or performance. It also does nothing to improve write throughput or reduce latency under normal operations.
- () https://aws.amazon.com/blogs/database/working-with-geospatial-data-in-amazon-elasticache-for-redis/
- () https://aws.amazon.com/blogs/database/amazon-elasticache-utilizing-redis-geospatial-capabilities/
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html

**Answer:**
Correct Answer: **Place an Amazon ElastiCache for Redis cluster in front of the PostgreSQL database. Modify the application to cache recent location reads and updates in Redis, using a TTL-based eviction strategy**

---

## Question 48

**Q:** Which solution best meets these requirements in the most operationally efficient manner?

**Options:**
- (A) Enable AWS IAM Identity Center and manually create user accounts and groups within it. Assign these users permission sets in each AWS account. Manage synchronization with on-premises Active Directory using custom PowerShell scripts
- (B) Use Amazon Cognito as the primary identity store and create a custom OpenID Connect (OIDC) federation with the on-premises Active Directory. Assign IAM roles using Cognito identity pools and propagate access to multiple AWS accounts using resource policies
- (C) Deploy an OpenLDAP server on Amazon EC2, sync it with the on-premises Active Directory, and integrate it with each AWS account by creating IAM roles that trust the EC2-hosted LDAP server as a SAML provider
- **(D) Deploy AWS IAM Identity Center and configure it to use AWS Directory Service for Microsoft Active Directory (Enterprise Edition). Establish a two-way trust relationship between the managed directory and the on-premises Active Directory to enable federated authentication across all AWS accounts** [CORRECT]
- (E) Correct option:
- (F) How AWS IAM Identity Center Active Directory sync enhances AWS application experiences:
- (G) via - https://aws.amazon.com/blogs/security/how-aws-sso-active-directory-sync-enhances-aws-application-experiences/
- (H) Incorrect options:
- (I) References:
- (J) https://docs.aws.amazon.com/singlesignon/latest/userguide/manage-your-identity-source-ad.html
- () https://aws.amazon.com/blogs/security/how-aws-sso-active-directory-sync-enhances-aws-application-experiences/
- () https://docs.aws.amazon.com/singlesignon/latest/userguide/manage-your-identity-source.html
- () https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-identity.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html
- () An Elastic Load Balancer has marked all the Amazon EC2 instances in the target group as unhealthy. Surprisingly, when a developer enters the IP address of the Amazon EC2 instances in the web browser, he can access the website.
- () What could be the reason the instances are being marked as unhealthy? (Select two)
- () Your web-app has a runtime that is not supported by the Application Load Balancer
- () Correct selection
- () The security group of the Amazon EC2 instance does not allow for traffic from the security group of the Application Load Balancer
- () You need to attach elastic IP address (EIP) to the Amazon EC2 instances
- () The route for the health check is misconfigured
- () The Amazon Elastic Block Store (Amazon EBS) volumes have been improperly mounted
- () Correct options:
- () An Application Load Balancer periodically sends requests to its registered targets to test their status. These tests are called health checks.
- () Each load balancer node routes requests only to the healthy targets in the enabled Availability Zones (AZs) for the load balancer. Each load balancer node checks the health of each target, using the health check settings for the target groups with which the target is registered. If a target group contains only unhealthy registered targets, the load balancer nodes route requests across its unhealthy targets.
- () You must ensure that your load balancer can communicate with registered targets on both the listener port and the health check port. Whenever you add a listener to your load balancer or update the health check port for a target group used by the load balancer to route requests, you must verify that the security groups associated with the load balancer allow traffic on the new port in both directions.
- () Application Load Balancer Configuration for Security Groups and Health Check Routes:
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-update-security-groups.html
- () The Amazon Elastic Block Store (Amazon EBS) volumes have been improperly mounted - You can access the website using the IP address which means there is no issue with the Amazon EBS volumes. So this option is not correct.
- () Your web-app has a runtime that is not supported by the Application Load Balancer - There is no connection between a web app runtime and the application load balancer. This option has been added as a distractor.
- () You need to attach elastic IP address (EIP) to the Amazon EC2 instances - This option is a distractor as Elastic IPs do not need to be assigned to Amazon EC2 instances while using an Application Load Balancer.
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-update-security-groups.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html
- () An enterprise has decided to move its secondary workloads such as backups and archives to AWS cloud. The CTO wishes to move the data stored on physical tapes to Cloud, without changing their current tape backup workflows. The company holds petabytes of data on tapes and needs a cost-optimized solution to move this data to cloud.
- () What is an optimal solution that meets these requirements while keeping the costs to a minimum?
- () Use AWS DataSync, which makes it simple and fast to move large amounts of data online between on-premises storage and AWS Cloud. Data moved to Cloud can then be stored cost-effectively in Amazon S3 archiving storage classes

**Answer:**
Correct Answer: **Deploy AWS IAM Identity Center and configure it to use AWS Directory Service for Microsoft Active Directory (Enterprise Edition). Establish a two-way trust relationship between the managed directory and the on-premises Active Directory to enable federated authentication across all AWS accounts**

---

## Question 49

**Q:** What could be the reason the instances are being marked as unhealthy? (Select two)

**Options:**
- (A) Your web-app has a runtime that is not supported by the Application Load Balancer
- (B) Correct selection
- (C) The security group of the Amazon EC2 instance does not allow for traffic from the security group of the Application Load Balancer
- (D) You need to attach elastic IP address (EIP) to the Amazon EC2 instances
- (E) The route for the health check is misconfigured
- (F) The Amazon Elastic Block Store (Amazon EBS) volumes have been improperly mounted
- (G) Correct options:
- (H) An Application Load Balancer periodically sends requests to its registered targets to test their status. These tests are called health checks.
- (I) Each load balancer node routes requests only to the healthy targets in the enabled Availability Zones (AZs) for the load balancer. Each load balancer node checks the health of each target, using the health check settings for the target groups with which the target is registered. If a target group contains only unhealthy registered targets, the load balancer nodes route requests across its unhealthy targets.
- (J) You must ensure that your load balancer can communicate with registered targets on both the listener port and the health check port. Whenever you add a listener to your load balancer or update the health check port for a target group used by the load balancer to route requests, you must verify that the security groups associated with the load balancer allow traffic on the new port in both directions.
- () Application Load Balancer Configuration for Security Groups and Health Check Routes:
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-update-security-groups.html
- () Incorrect options:
- () The Amazon Elastic Block Store (Amazon EBS) volumes have been improperly mounted - You can access the website using the IP address which means there is no issue with the Amazon EBS volumes. So this option is not correct.
- () Your web-app has a runtime that is not supported by the Application Load Balancer - There is no connection between a web app runtime and the application load balancer. This option has been added as a distractor.
- () You need to attach elastic IP address (EIP) to the Amazon EC2 instances - This option is a distractor as Elastic IPs do not need to be assigned to Amazon EC2 instances while using an Application Load Balancer.
- () References:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-update-security-groups.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html
- () An enterprise has decided to move its secondary workloads such as backups and archives to AWS cloud. The CTO wishes to move the data stored on physical tapes to Cloud, without changing their current tape backup workflows. The company holds petabytes of data on tapes and needs a cost-optimized solution to move this data to cloud.
- () What is an optimal solution that meets these requirements while keeping the costs to a minimum?
- () Use AWS DataSync, which makes it simple and fast to move large amounts of data online between on-premises storage and AWS Cloud. Data moved to Cloud can then be stored cost-effectively in Amazon S3 archiving storage classes
- () Use AWS VPN connection between the on-premises datacenter and your Amazon VPC. Once this is established, you can use Amazon Elastic File System (Amazon EFS) to get a scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources
- () Use AWS Direct Connect, a cloud service solution that makes it easy to establish a dedicated network connection from on-premises to AWS to transfer data. Once this is done, Amazon S3 can be used to store data at lesser costs
- **() Use Tape Gateway, which can be used to move on-premises tape data onto AWS Cloud. Then, Amazon S3 archiving storage classes can be used to store data cost-effectively for years** [CORRECT]
- () Correct option:
- () Tape Gateway enables you to replace using physical tapes on-premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway supports all leading backup applications and caches virtual tapes on-premises for low-latency data access. Tape Gateway encrypts data between the gateway and AWS for secure data transfer and compresses data while transitioning virtual tapes between Amazon S3 and Amazon S3 Glacier, or Amazon S3 Glacier Deep Archive, to minimize storage costs.
- () Tape Gateway compresses and stores archived virtual tapes in the lowest-cost Amazon S3 storage classes, Amazon S3 Glacier and Amazon S3 Glacier Deep Archive. This makes it feasible for you to retain long-term data in the AWS Cloud at a very low cost. With Tape Gateway, you only pay for what you consume, with no minimum commitments and no upfront fees.
- () Tape Gateway stores your virtual tapes in S3 buckets managed by the AWS Storage Gateway service, so you don’t have to manage your own Amazon S3 storage. Tape Gateway integrates with all leading backup applications allowing you to start using cloud storage for on-premises backup and archive without any changes to your backup and archive workflows.
- () Tape Gateway Overview:
- () via - https://aws.amazon.com/storagegateway/vtl/
- () Use AWS DataSync, which makes it simple and fast to move large amounts of data online between on-premises storage and AWS Cloud. Data moved to Cloud can then be stored cost-effectively in Amazon S3 archiving storage classes - AWS DataSync supports only NFS and SMB file types and hence is not the right choice for the given use case.
- () https://aws.amazon.com/storagegateway/vtl/
- () https://aws.amazon.com/storagegateway/faqs/
- () You have developed a new REST API leveraging the Amazon API Gateway, AWS Lambda and Amazon Aurora database services. Most of the workload on the website is read-heavy. The data rarely changes and it is acceptable to serve users outdated data for about 24 hours. Recently, the website has been experiencing high load and the costs incurred on the Aurora database have been very high.

**Answer:**
Correct Answer: **Use Tape Gateway, which can be used to move on-premises tape data onto AWS Cloud. Then, Amazon S3 archiving storage classes can be used to store data cost-effectively for years**

---

## Question 50

**Q:** What is an optimal solution that meets these requirements while keeping the costs to a minimum?

**Options:**
- (A) Use AWS DataSync, which makes it simple and fast to move large amounts of data online between on-premises storage and AWS Cloud. Data moved to Cloud can then be stored cost-effectively in Amazon S3 archiving storage classes
- (B) Use AWS VPN connection between the on-premises datacenter and your Amazon VPC. Once this is established, you can use Amazon Elastic File System (Amazon EFS) to get a scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources
- (C) Use AWS Direct Connect, a cloud service solution that makes it easy to establish a dedicated network connection from on-premises to AWS to transfer data. Once this is done, Amazon S3 can be used to store data at lesser costs
- **(D) Use Tape Gateway, which can be used to move on-premises tape data onto AWS Cloud. Then, Amazon S3 archiving storage classes can be used to store data cost-effectively for years** [CORRECT]
- (E) Correct option:
- (F) Tape Gateway enables you to replace using physical tapes on-premises with virtual tapes in AWS without changing existing backup workflows. Tape Gateway supports all leading backup applications and caches virtual tapes on-premises for low-latency data access. Tape Gateway encrypts data between the gateway and AWS for secure data transfer and compresses data while transitioning virtual tapes between Amazon S3 and Amazon S3 Glacier, or Amazon S3 Glacier Deep Archive, to minimize storage costs.
- (G) Tape Gateway compresses and stores archived virtual tapes in the lowest-cost Amazon S3 storage classes, Amazon S3 Glacier and Amazon S3 Glacier Deep Archive. This makes it feasible for you to retain long-term data in the AWS Cloud at a very low cost. With Tape Gateway, you only pay for what you consume, with no minimum commitments and no upfront fees.
- (H) Tape Gateway stores your virtual tapes in S3 buckets managed by the AWS Storage Gateway service, so you don’t have to manage your own Amazon S3 storage. Tape Gateway integrates with all leading backup applications allowing you to start using cloud storage for on-premises backup and archive without any changes to your backup and archive workflows.
- (I) Tape Gateway Overview:
- (J) via - https://aws.amazon.com/storagegateway/vtl/
- () Incorrect options:
- () Use AWS DataSync, which makes it simple and fast to move large amounts of data online between on-premises storage and AWS Cloud. Data moved to Cloud can then be stored cost-effectively in Amazon S3 archiving storage classes - AWS DataSync supports only NFS and SMB file types and hence is not the right choice for the given use case.
- () References:
- () https://aws.amazon.com/storagegateway/vtl/
- () https://aws.amazon.com/storagegateway/faqs/
- () You have developed a new REST API leveraging the Amazon API Gateway, AWS Lambda and Amazon Aurora database services. Most of the workload on the website is read-heavy. The data rarely changes and it is acceptable to serve users outdated data for about 24 hours. Recently, the website has been experiencing high load and the costs incurred on the Aurora database have been very high.

**Answer:**
Correct Answer: **Use Tape Gateway, which can be used to move on-premises tape data onto AWS Cloud. Then, Amazon S3 archiving storage classes can be used to store data cost-effectively for years**

---

## Question 51

**Q:** How can you easily reduce the costs while improving performance, with minimal changes?

**Options:**
- (A) Enable AWS Lambda In Memory Caching
- **(B) Enable Amazon API Gateway Caching** [CORRECT]
- (C) Add Amazon Aurora Read Replicas
- (D) Switch to using an Application Load Balancer
- (E) Correct option:
- (F)  for applications to access data, business logic, or functionality from your backend services. Using API Gateway, you can create RESTful APIs and WebSocket APIs that enable real-time two-way communication applications. API Gateway supports containerized and serverless workloads, as well as web applications.
- (G) Incorrect options:
- (H) Add Amazon Aurora Read Replicas - Amazon Aurora features a distributed, fault-tolerant, self-healing storage system that auto-scales up to 64TB per database instance. It delivers high performance and availability with up to 15 low-latency read replicas, point-in-time recovery, continuous backup to Amazon S3, and replication across three Availability Zones (AZs).
- (I) Enable AWS Lambda In Memory Caching - AWS Lambda has no native in-memory caching capability. AWS Lambda is a serverless compute capacity. This option is incorrect and has been added as a distractor.
- (J) Reference:
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-caching.html

**Answer:**
Correct Answer: **Enable Amazon API Gateway Caching**

---

## Question 52

**Q:** As a solutions architect, which of the following AWS database services would you suggest as the BEST fit to handle such use cases?

**Options:**
- (A) Amazon Neptune
- (B) Amazon Aurora
- (C) Amazon Redshift
- (D) Amazon OpenSearch Service
- (E) Correct option:
- (F) Amazon Neptune is a fast, reliable, fully managed graph database service that makes it easy to build and run applications that work with highly connected datasets. The core of Amazon Neptune is a purpose-built, high-performance graph database engine optimized for storing billions of relationships and querying the graph with milliseconds latency. Neptune powers graph use cases such as recommendation engines, fraud detection, knowledge graphs, drug discovery, and network security.
- (G) Amazon Neptune is highly available, with read replicas, point-in-time recovery, continuous backup to Amazon S3, and replication across Availability Zones. Neptune is secure with support for HTTPS encrypted client connections and encryption at rest. Neptune is fully managed, so you no longer need to worry about database management tasks such as hardware provisioning, software patching, setup, configuration, or backups.
- (H) Social Networking example with Amazon Neptune:
- (I) via - https://aws.amazon.com/neptune/
- (J) Identity graphs example with Amazon Neptune:
- () Incorrect options:
- () Amazon Redshift - Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis. The given use-case is not about data warehousing, so this is not a correct option.
- () Reference:
- () https://aws.amazon.com/neptune/
- () Which AWS solution best meets these requirements?
- () Implement Amazon FSx for Windows File Server and configure on-premises servers to mount the file system using a VPN connection. Store all primary data in FSx and use it as the central NAS replacement
- () Set up Amazon S3 Standard-Infrequent Access (S3 Standard-IA) as the primary storage tier. Configure the on-premises file server to replicate changes to the S3 bucket using AWS DataSync for asynchronous updates
- () Deploy AWS Storage Gateway using stored volumes. Retain the full dataset on-premises and asynchronously back up point-in-time snapshots to Amazon S3. Configure applications to read from the local volume and recover data from the cloud if needed
- **() Deploy AWS Storage Gateway using cached volumes. Store frequently accessed data locally, while writing all primary data asynchronously to Amazon S3** [CORRECT]
- () via - https://docs.aws.amazon.com/storagegateway/latest/vgw/StorageGatewayConcepts.html
- () https://docs.aws.amazon.com/storagegateway/latest/vgw/StorageGatewayConcepts.html
- () A social media company wants the capability to dynamically alter the size of a geographic area from which traffic is routed to a specific server resource.
- () Which feature of Amazon Route 53 can help achieve this functionality?
- () Geolocation routing
- () Latency-based routing
- () Weighted routing

**Answer:**
Correct Answer: **Deploy AWS Storage Gateway using cached volumes. Store frequently accessed data locally, while writing all primary data asynchronously to Amazon S3**

---

## Question 53

**Q:** Which feature of Amazon Route 53 can help achieve this functionality?

**Options:**
- (A) Geolocation routing
- (B) Latency-based routing
- (C) Weighted routing
- (D) Geoproximity routing
- (E) Correct option:
- (F) Geoproximity routing lets Amazon Route 53 route traffic to your resources based on the geographic location of your users and your resources. You can also optionally choose to route more traffic or less to a given resource by specifying a value, known as a bias. A bias expands or shrinks the size of the geographic region from which traffic is routed to a resource.
- (G) To optionally change the size of the geographic region from which Amazon Route 53 routes traffic to a resource, specify the applicable value for the bias: 1. To expand the size of the geographic region from which Amazon Route 53 routes traffic to a resource, specify a positive integer from 1 to 99 for the bias. Amazon Route 53 shrinks the size of adjacent regions.
- (H) 1. To shrink the size of the geographic region from which Amazon Route 53 routes traffic to a resource, specify a negative bias of -1 to -99. Amazon Route 53 expands the size of adjacent regions.
- (I) More on how bias works in Geoproximity routing:
- (J) via - https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () Incorrect options:
- () Geolocation routing - Geolocation routing lets you choose the resources that serve your traffic based on the geographic location of your users, meaning the location that DNS queries originate from. For example, you might want all queries from Europe to be routed to an Elastic Load Balancing (ELB) load balancer in the Frankfurt region.
- () When you use geolocation routing, you can localize your content and present some or all of your website in the language of your users. You can also use geolocation routing to restrict the distribution of content to only the locations in which you have distribution rights. Another possible use is for balancing load across endpoints in a predictable, easy-to-manage way so that each user location is consistently routed to the same endpoint.
- () Latency-based routing - If your application is hosted in multiple AWS Regions, you can improve performance for your users by serving their requests from the AWS Region that provides the lowest latency.
- () To use latency-based routing, you create latency records for your resources in multiple AWS Regions. When Amazon Route 53 receives a DNS query for your domain or subdomain (example.com or acme.example.com), it determines which AWS Regions you've created latency records for, determines which region gives the user the lowest latency, and then selects a latency record for that region. Amazon Route 53 responds with the value from the selected record, such as the IP address for a web server.
- () Weighted routing - Weighted routing lets you associate multiple resources with a single domain name (example.com) or subdomain name (acme.example.com) and choose how much traffic is routed to each resource. This can be useful for a variety of purposes, including load balancing and testing new versions of software.
- () To configure weighted routing, you create records that have the same name and type for each of your resources. You assign each record a relative weight that corresponds with how much traffic you want to send to each resource. Amazon Route 53 sends traffic to a resource based on the weight that you assign to the record as a proportion of the total weight for all records in the group.
- () Reference:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html
- () Which solution will best meet these requirements?
- () Establish inter-Region VPC peering between each VPC in the us-west-2 and eu-central-1 Regions. Use static routing tables in each VPC to define peer relationships and enable cross-Region communication
- () Create private VIFs (virtual interfaces) in each Region and associate them directly with foreign-region VPCs using routing table entries and BGP. Use VPC endpoints in each account to forward cross-Region traffic
- () Connect both Direct Connect links to a shared Direct Connect gateway. Attach each Region's virtual private gateway (VGW) to the Direct Connect gateway, enabling transitive routing between the VPCs and the on-premises networks across Regions
- () Deploy EC2-based VPN appliances in each VPC. Configure a full mesh VPN topology between all VPCs and data centers using CloudHub-style routing across Regions
- () via - https://aws.amazon.com/blogs/networking-and-content-delivery/hybrid-cloud-architectures-using-aws-direct-connect-gateway/
- () References:
- () https://aws.amazon.com/blogs/networking-and-content-delivery/hybrid-cloud-architectures-using-aws-direct-connect-gateway/
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/direct-connect-gateways-intro.html
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/WorkingWithVirtualInterfaces.html
- () A media company uses Amazon ElastiCache Redis to enhance the performance of its Amazon RDS database layer. The company wants a robust disaster recovery strategy for its caching layer that guarantees minimal downtime as well as minimal data loss while ensuring good application performance.
- () Which of the following solutions will you recommend to address the given use-case?
- () Add read-replicas across multiple availability zones (AZs) to reduce the risk of potential data loss because of failure
- () Schedule daily automatic backups at a time when you expect low resource utilization for your cluster
- **() Opt for Multi-AZ configuration with automatic failover functionality to help mitigate failure** [CORRECT]

**Answer:**
Correct Answer: **Opt for Multi-AZ configuration with automatic failover functionality to help mitigate failure**

---

## Question 54

**Q:** Which of the following solutions will you recommend to address the given use-case?

**Options:**
- (A) Add read-replicas across multiple availability zones (AZs) to reduce the risk of potential data loss because of failure
- (B) Schedule daily automatic backups at a time when you expect low resource utilization for your cluster
- **(C) Opt for Multi-AZ configuration with automatic failover functionality to help mitigate failure** [CORRECT]
- (D) Schedule manual backups using Redis append-only file (AOF)
- (E) Correct option:
- (F) Multi-AZ is the best option when data retention, minimal downtime, and application performance are a priority.
- (G) Data-loss potential - Low. Multi-AZ provides fault tolerance for every scenario, including hardware-related issues.
- (H) Performance impact - Low. Of the available options, Multi-AZ provides the fastest time to recovery, because there is no manual procedure to follow after the process is implemented.
- (I) Cost - Low to high. Multi-AZ is the lowest-cost option. Use Multi-AZ when you can't risk losing data because of hardware failure or you can't afford the downtime required by other options in your response to an outage.
- (J) Incorrect options:
- () Schedule daily automatic backups at a time when you expect low resource utilization for your cluster - Data loss potential is high, almost up to a day's worth of data. Hence, this is not the right option.
- () Schedule manual backups using Redis append-only file (AOF) - Manual backups using AOF are retained indefinitely and are useful for testing and archiving. You can schedule manual backups to occur up to 20 times per node within any 24-hour period. Although AOF provides a measure of fault tolerance, it can't protect your data from a hardware-related cache node failure, so there is a risk of data loss.
- () Add read-replicas across multiple availability zones (AZs) to reduce the risk of potential data loss because of failure - To scale read capacity, Amazon ElastiCache allows you to add up to five read replicas across multiple availability zones. Read replicas are used to ease out read traffic from the primary database and cannot be used as a complete fault-tolerant solution in itself.
- () Reference:
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/FaultTolerance.html
- () A developer in your company has set up a classic 2 tier architecture consisting of an Application Load Balancer and an Auto Scaling group (ASG) managing a fleet of Amazon EC2 instances. The Application Load Balancer is deployed in a subnet of size 10.0.1.0/24 and the Auto Scaling group is deployed in a subnet of size 10.0.4.0/22.

**Answer:**
Correct Answer: **Opt for Multi-AZ configuration with automatic failover functionality to help mitigate failure**

---

## Question 55

**Q:** As a solutions architect, you would like to adhere to the security pillar of the well-architected framework. How do you configure the security group of the Amazon EC2 instances to only allow traffic coming from the Application Load Balancer?

**Options:**
- (A) Add a rule to authorize the CIDR 10.0.4.0/22
- (B) Add a rule to authorize the CIDR 10.0.1.0/24
- (C) Add a rule to authorize the security group of the Auto Scaling group
- **(D) Add a rule to authorize the security group of the Application Load Balancer** [CORRECT]
- (E) Correct option:
- (F) An Auto Scaling group (ASG) contains a collection of Amazon EC2 instances that are treated as a logical grouping for automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
- (G) The following are the characteristics of security group rules: 1. By default, security groups allow all outbound traffic. 2. Security group rules are always permissive; you can't create rules that deny access. 3. Security groups are stateful
- (H) Application Load Balancer (ALB) operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses and Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- (I) Incorrect option:
- (J) Adding the entire CIDR of the Application Load Balancer would work, but wouldn't guarantee that only the Auto Scaling group can access the Amazon EC2 instances that are part of the Auto Scaling group. Here, the right solution is to add a rule on the Auto Scaling group security group to allow incoming traffic only from the security group configured for the Application Load Balancer.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () A CRM web application was written as a monolith in PHP and is facing scaling issues because of performance bottlenecks. The CTO wants to re-engineer towards microservices architecture and expose their application from the same load balancer, linked to different target groups with different URLs: checkout.mycorp.com, www.mycorp.com, yourcorp.com/profile and yourcorp.com/search. The CTO would like to expose all these URLs as HTTPS endpoints for security purposes.

**Answer:**
Correct Answer: **Add a rule to authorize the security group of the Application Load Balancer**

---

## Question 56

**Q:** As a solutions architect, which of the following would you recommend as a solution that requires MINIMAL configuration effort?

**Options:**
- (A) Use an HTTP to HTTPS redirect
- (B) Use a wildcard Secure Sockets Layer certificate (SSL certificate)
- **(C) Use Secure Sockets Layer certificate (SSL certificate) with SNI** [CORRECT]
- (D) Change the Elastic Load Balancing (ELB) SSL Security Policy
- (E) Correct option:
- (F) You can host multiple TLS secured applications, each with its own TLS certificate, behind a single load balancer. To use SNI, all you need to do is bind multiple certificates to the same secure listener on your load balancer. ALB will automatically choose the optimal TLS certificate for each client.
- (G) ALB’s smart certificate selection goes beyond SNI. In addition to containing a list of valid domain names, certificates also describe the type of key exchange and cryptography that the server supports, as well as the signature algorithm (SHA2, SHA1, MD5) used to sign the certificate.
- (H) Incorrect options:
- (I) Use a wildcard Secure Sockets Layer certificate (SSL certificate) - As the use case requires different domain names, so you cannot use a wildcard SSL certificate.
- (J) Use an HTTP to HTTPS redirect - This will not provide multiple secure endpoints for different URLs such as checkout.mycorp.com or www.mycorp.com, therefore it is incorrect for the given use-case.
- () Change the Elastic Load Balancing (ELB) SSL Security Policy - Elastic Load Balancing (ELB) SSL Security Policy will not provide multiple secure endpoints for different URLs such as checkout.mycorp.com or www.mycorp.com, therefore it is incorrect for the given use-case.
- () References:
- () https://aws.amazon.com/blogs/aws/new-application-load-balancer-sni/
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-security-policy-table.html
- () What does this AWS CloudFormation snippet do? (Select three)
- () SecurityGroupIngress:
- () - IpProtocol: tcp
- () FromPort: 80
- () ToPort: 80
- () CidrIp: 0.0.0.0/0
- () FromPort: 22
- () ToPort: 22
- () CidrIp: 192.168.1.1/32
- () Correct selection
- () It lets traffic flow from one IP on port 22
- () It prevents traffic from reaching on HTTP unless from the IP 192.168.1.1
- () It allows any IP to pass through on the HTTP port
- () It configures the inbound rules of a network access control list (network ACL)
- () It configures a security group's inbound rules
- () It configures a security group's outbound rules
- () It only allows the IP 0.0.0.0 to reach HTTP
- () Correct options:
- () The following are the characteristics of security group rules: 1. By default, security groups allow all outbound traffic. 2. Security group rules are always permissive; you can't create rules that deny access. 3. Security groups are stateful
- () AWS CloudFormation provides a common language for you to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts. This gives you a single source of truth for your AWS and third-party resources.
- ()  in our security group rule represents a different rule (YAML syntax)
- () Therefore the AWS CloudFormation snippet creates two Security Group inbound rules that allow any IP to pass through on the HTTP port and lets traffic flow from one source IP (192.168.1.1) on port 22.
- () It configures the inbound rules of a network access control list (network ACL) - A Network Access Control List ( Network ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up network ACLs with rules similar to your security groups to add an additional layer of security to your VPC.
- () These three options contradict the description provided above. So these are incorrect.

**Answer:**
Correct Answer: **Use Secure Sockets Layer certificate (SSL certificate) with SNI**

---

## Question 57

**Q:** What does this AWS CloudFormation snippet do? (Select three)

**Options:**
- **(A) SecurityGroupIngress:** [CORRECT]
- (B) - IpProtocol: tcp
- (C) FromPort: 80
- (D) ToPort: 80
- (E) CidrIp: 0.0.0.0/0
- (F) FromPort: 22
- (G) ToPort: 22
- (H) CidrIp: 192.168.1.1/32
- (I) Correct selection
- (J) It lets traffic flow from one IP on port 22
- () It prevents traffic from reaching on HTTP unless from the IP 192.168.1.1
- () It allows any IP to pass through on the HTTP port
- () It configures the inbound rules of a network access control list (network ACL)
- () It configures a security group's inbound rules
- () It configures a security group's outbound rules
- () It only allows the IP 0.0.0.0 to reach HTTP
- () Correct options:
- () The following are the characteristics of security group rules: 1. By default, security groups allow all outbound traffic. 2. Security group rules are always permissive; you can't create rules that deny access. 3. Security groups are stateful
- () AWS CloudFormation provides a common language for you to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts. This gives you a single source of truth for your AWS and third-party resources.
- ()  in our security group rule represents a different rule (YAML syntax)
- () Therefore the AWS CloudFormation snippet creates two Security Group inbound rules that allow any IP to pass through on the HTTP port and lets traffic flow from one source IP (192.168.1.1) on port 22.
- () Incorrect options:
- () It configures the inbound rules of a network access control list (network ACL) - A Network Access Control List ( Network ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You might set up network ACLs with rules similar to your security groups to add an additional layer of security to your VPC.
- () These three options contradict the description provided above. So these are incorrect.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html
- () https://aws.amazon.com/cloudformation/
- () An IT company has a large number of clients opting to build their application programming interface (API) using Docker containers. To facilitate the hosting of these containers, the company is looking at various orchestration services available with AWS.
- () As a Solutions Architect, which of the following solutions will you suggest? (Select two)
- () Use Amazon Elastic Container Service (Amazon ECS) with Amazon EC2 for serverless orchestration of the containerized services
- () Use Amazon SageMaker for serverless orchestration of the containerized services
- () Use Amazon Elastic Kubernetes Service (Amazon EKS) with AWS Fargate for serverless orchestration of the containerized services
- () Use Amazon EMR for serverless orchestration of the containerized services
- () Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate for serverless orchestration of the containerized services
- () Building APIs with Docker containers has been gaining momentum over the years. For hosting and exposing these container-based APIs, they need a solution which supports HTTP requests routing, autoscaling, and high availability. In some cases, user authorization is also needed.
- () For this purpose, many organizations are orchestrating their containerized services with Amazon Elastic Container Service (Amazon ECS) or Amazon Elastic Kubernetes Service (Amazon EKS), while hosting their containers on Amazon EC2 or AWS Fargate. Then, they can add scalability and high availability with Service Auto Scaling (in Amazon ECS) or Horizontal Pod Auto Scaler (in Amazon EKS), and they expose the services through load balancers.
- () When you use Amazon ECS as an orchestrator (with EC2 or Fargate launch type), you also have the option to expose your services with Amazon API Gateway and AWS Cloud Map instead of a load balancer. AWS Cloud Map is used for service discovery: no matter how Amazon ECS tasks scale, AWS Cloud Map service names would point to the right set of Amazon ECS tasks. Then, API Gateway HTTP APIs can be used to define API routes and point them to the corresponding AWS Cloud Map services.

**Answer:**
Correct Answer: **SecurityGroupIngress:**

---

## Question 58

**Q:** As a Solutions Architect, which of the following solutions will you suggest? (Select two)

**Options:**
- (A) Use Amazon Elastic Container Service (Amazon ECS) with Amazon EC2 for serverless orchestration of the containerized services
- (B) Use Amazon SageMaker for serverless orchestration of the containerized services
- (C) Correct selection
- (D) Use Amazon Elastic Kubernetes Service (Amazon EKS) with AWS Fargate for serverless orchestration of the containerized services
- (E) Use Amazon EMR for serverless orchestration of the containerized services
- (F) Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate for serverless orchestration of the containerized services
- (G) Correct options:
- (H) Building APIs with Docker containers has been gaining momentum over the years. For hosting and exposing these container-based APIs, they need a solution which supports HTTP requests routing, autoscaling, and high availability. In some cases, user authorization is also needed.
- (I) For this purpose, many organizations are orchestrating their containerized services with Amazon Elastic Container Service (Amazon ECS) or Amazon Elastic Kubernetes Service (Amazon EKS), while hosting their containers on Amazon EC2 or AWS Fargate. Then, they can add scalability and high availability with Service Auto Scaling (in Amazon ECS) or Horizontal Pod Auto Scaler (in Amazon EKS), and they expose the services through load balancers.
- (J) When you use Amazon ECS as an orchestrator (with EC2 or Fargate launch type), you also have the option to expose your services with Amazon API Gateway and AWS Cloud Map instead of a load balancer. AWS Cloud Map is used for service discovery: no matter how Amazon ECS tasks scale, AWS Cloud Map service names would point to the right set of Amazon ECS tasks. Then, API Gateway HTTP APIs can be used to define API routes and point them to the corresponding AWS Cloud Map services.
- () Incorrect options:
- () Use Amazon Elastic Container Service (Amazon ECS) with Amazon EC2 for serverless orchestration of the containerized services - Amazon EC2 can be used to host the container services. Amazon EC2 needs hosting and management of the instance, hence does not come under serverless solution. Fargate can be used for serverless container solutions.
- () Use Amazon EMR for serverless orchestration of the containerized services - Amazon EMR is a web service that enables businesses, researchers, data analysts, and developers to easily and cost-effectively process vast amounts of data. It utilizes a hosted Hadoop framework running on the web-scale infrastructure of Amazon EC2 and Amazon S3. EMR is not a docker orchestration service, as required for the use case.
- () Use Amazon SageMaker for serverless orchestration of the containerized services - Amazon SageMaker helps data scientists and developers to prepare, build, train, and deploy high-quality machine learning (ML) models quickly by bringing together a broad set of capabilities purpose-built for ML. A powerful tool, SageMaker is not a docker orchestration service, as required for the use case.
- () Reference:
- () https://aws.amazon.com/blogs/architecture/field-notes-serverless-container-based-apis-with-amazon-ecs-and-amazon-api-gateway/
- () Which configuration will best meet these requirements?
- () Configure the Aurora cluster to use Aurora I/O-Optimized storage. This configuration delivers high throughput and low-latency I/O performance with predictable pricing and no I/O-based charges
- () Select Provisioned IOPS (io1) as the storage type for the Aurora cluster. Manually adjust IOPS based on expected traffic during peak usage
- () Configure the Aurora cluster to use General Purpose SSD (gp2) storage. Increase performance by scaling database compute capacity to reduce IOPS bottlenecks
- () Configure the cluster with Magnetic (Standard) storage to minimize baseline storage costs and rely on Aurora’s autoscaling to handle demand spikes
- () Correct option:
- () Configure the Aurora cluster to use General Purpose SSD (gp2) storage. Increase performance by scaling database compute capacity to reduce IOPS bottlenecks - While General Purpose (gp2) SSD storage can provide reasonable baseline performance, it uses a burst-bucket model for IOPS that is not ideal under sustained heavy load. It cannot scale IOPS independently of storage size, and relying on compute scaling to compensate for storage I/O limitations can be inefficient and more expensive.
- () Select Provisioned IOPS (io1) as the storage type for the Aurora cluster. Manually adjust IOPS based on expected traffic during peak usage - Provisioned IOPS allows precise tuning of IOPS levels, but it is not supported directly as a configurable storage type in Aurora. Instead, Aurora abstracts much of the IOPS provisioning logic. Even if it were supported, manually adjusting IOPS would increase operational complexity and cost more compared to Aurora’s I/O-Optimized option.
- () Configure the cluster with Magnetic (Standard) storage to minimize baseline storage costs and rely on Aurora’s autoscaling to handle demand spikes - Magnetic storage is a legacy, low-cost option that is not suitable for high-performance production workloads. It suffers from high latency and limited throughput, making it a poor choice for applications with spiky or sustained I/O demand. Moreover, magnetic storage is not supported in newer Aurora configurations.
- () References:
- () https://aws.amazon.com/blogs/aws/new-amazon-aurora-i-o-optimized-cluster-configuration-with-up-to-40-cost-savings-for-i-o-intensive-applications/
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.StorageReliability.html
- () A small rental company had 5 employees, all working under the same AWS cloud account. These employees deployed their applications built for various functions- including billing, operations, finance, etc. Each of these employees has been operating in their own VPC. Now, there is a need to connect these VPCs so that the applications can communicate with each other.
- () Which of the following is the MOST cost-effective solution for this use-case?
- () Use an AWS Direct Connect connection
- **() Use a VPC peering connection** [CORRECT]
- () Use a Network Address Translation gateway (NAT gateway)
- () Use an Internet Gateway
- () More on VPC Peering:
- () via - https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html

**Answer:**
Correct Answer: **Use a VPC peering connection**

---

## Question 59

**Q:** Which configuration will best meet these requirements?

**Options:**
- (A) Configure the Aurora cluster to use Aurora I/O-Optimized storage. This configuration delivers high throughput and low-latency I/O performance with predictable pricing and no I/O-based charges
- (B) Select Provisioned IOPS (io1) as the storage type for the Aurora cluster. Manually adjust IOPS based on expected traffic during peak usage
- (C) Configure the Aurora cluster to use General Purpose SSD (gp2) storage. Increase performance by scaling database compute capacity to reduce IOPS bottlenecks
- (D) Configure the cluster with Magnetic (Standard) storage to minimize baseline storage costs and rely on Aurora’s autoscaling to handle demand spikes
- (E) Correct option:
- (F) Incorrect options:
- (G) Configure the Aurora cluster to use General Purpose SSD (gp2) storage. Increase performance by scaling database compute capacity to reduce IOPS bottlenecks - While General Purpose (gp2) SSD storage can provide reasonable baseline performance, it uses a burst-bucket model for IOPS that is not ideal under sustained heavy load. It cannot scale IOPS independently of storage size, and relying on compute scaling to compensate for storage I/O limitations can be inefficient and more expensive.
- (H) Select Provisioned IOPS (io1) as the storage type for the Aurora cluster. Manually adjust IOPS based on expected traffic during peak usage - Provisioned IOPS allows precise tuning of IOPS levels, but it is not supported directly as a configurable storage type in Aurora. Instead, Aurora abstracts much of the IOPS provisioning logic. Even if it were supported, manually adjusting IOPS would increase operational complexity and cost more compared to Aurora’s I/O-Optimized option.
- (I) Configure the cluster with Magnetic (Standard) storage to minimize baseline storage costs and rely on Aurora’s autoscaling to handle demand spikes - Magnetic storage is a legacy, low-cost option that is not suitable for high-performance production workloads. It suffers from high latency and limited throughput, making it a poor choice for applications with spiky or sustained I/O demand. Moreover, magnetic storage is not supported in newer Aurora configurations.
- (J) References:
- () https://aws.amazon.com/blogs/aws/new-amazon-aurora-i-o-optimized-cluster-configuration-with-up-to-40-cost-savings-for-i-o-intensive-applications/
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Overview.StorageReliability.html
- () A small rental company had 5 employees, all working under the same AWS cloud account. These employees deployed their applications built for various functions- including billing, operations, finance, etc. Each of these employees has been operating in their own VPC. Now, there is a need to connect these VPCs so that the applications can communicate with each other.
- () Which of the following is the MOST cost-effective solution for this use-case?
- () Use an AWS Direct Connect connection
- **() Use a VPC peering connection** [CORRECT]
- () Use a Network Address Translation gateway (NAT gateway)
- () Use an Internet Gateway
- () More on VPC Peering:
- () via - https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () Use an Internet Gateway - An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It, therefore, imposes no availability risks or bandwidth constraints on your network traffic. Internet Gateway is not meant for connecting between VPCs.
- () Use a Network Address Translation gateway (NAT gateway) - You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances. You are charged for creating and using a NAT gateway in your account. NAT gateway hourly usage and data processing rates apply. NAT Gateway is not used for connection between VPCs.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () A CRM company has a software as a service (SaaS) application that feeds updates to other in-house and third-party applications. The SaaS application and the in-house applications are being migrated to use AWS services for this inter-application communication.

**Answer:**
Correct Answer: **Use a VPC peering connection**

---

## Question 60

**Q:** Which of the following is the MOST cost-effective solution for this use-case?

**Options:**
- (A) Use an AWS Direct Connect connection
- **(B) Use a VPC peering connection** [CORRECT]
- (C) Use a Network Address Translation gateway (NAT gateway)
- (D) Use an Internet Gateway
- (E) Correct option:
- (F) More on VPC Peering:
- (G) via - https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- (H) Incorrect options:
- (I) Use an Internet Gateway - An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It, therefore, imposes no availability risks or bandwidth constraints on your network traffic. Internet Gateway is not meant for connecting between VPCs.
- (J) Use a Network Address Translation gateway (NAT gateway) - You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to the internet or other AWS services, but prevent the internet from initiating a connection with those instances. You are charged for creating and using a NAT gateway in your account. NAT gateway hourly usage and data processing rates apply. NAT Gateway is not used for connection between VPCs.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () A CRM company has a software as a service (SaaS) application that feeds updates to other in-house and third-party applications. The SaaS application and the in-house applications are being migrated to use AWS services for this inter-application communication.

**Answer:**
Correct Answer: **Use a VPC peering connection**

---

## Question 61

**Q:** As a Solutions Architect, which of the following would you suggest to asynchronously decouple the architecture?

**Options:**
- (A) Use Elastic Load Balancing (ELB) for effective decoupling of system architecture
- **(B) Use Amazon EventBridge to decouple the system architecture** [CORRECT]
- (C) Use Amazon Simple Notification Service (Amazon SNS) to communicate between systems and decouple the architecture
- (D) Use Amazon Simple Queue Service (Amazon SQS) to decouple the architecture
- (E) Correct option:
- (F) Both Amazon EventBridge and Amazon SNS can be used to develop event-driven applications, but for this use case, EventBridge is the right fit.
- (G) How Amazon EventBridge works:
- (H) via - https://aws.amazon.com/eventbridge/
- (I) Incorrect options:
- (J) Use Amazon Simple Notification Service (Amazon SNS) to communicate between systems and decouple the architecture - As discussed above, Amazon SNS can be used for event-based services. But, our use case needs integration with third-party SaaS services, hence Amazon EventBridge is the right choice, as Amazon SNS does not support third-party services integration.
- () Use Amazon Simple Queue Service (Amazon SQS) to decouple the architecture - Amazon SQS is a message queuing service from amazon and works well for decoupling applications. It does not directly integrate with third-party SaaS services.
- () Use Elastic Load Balancing (ELB) for effective decoupling of system architecture - Elastic Load Balancing (ELB) offers a synchronous decoupling of applications, which is not the right fit for the current use case.
- () References:
- () https://aws.amazon.com/eventbridge/
- () https://aws.amazon.com/sns/
- () A financial services company is implementing two separate data retention policies to comply with regulatory standards:
- () Policy A: Critical transaction records must be immediately available for audit and must not be deleted or overwritten for 7 years.
- () Policy B: Archived compliance data must be stored in a low-cost, long-term storage solution and locked from deletion or modification for at least 10 years.

**Answer:**
Correct Answer: **Use Amazon EventBridge to decouple the system architecture**

---

## Question 62

**Q:** As a solutions architect, which combination of AWS features should you recommend to enforce these policies effectively?

**Options:**
- (A) Use Amazon S3 Standard storage class with S3 Lifecycle policies for Policy A, and S3 Glacier Flexible Retrieval for Policy B
- (B) Use Amazon S3 Glacier Vault Lock for both policies to reduce storage costs while enforcing retention
- (C) Use Amazon S3 Object Lock in Governance mode for both policies to ensure data cannot be deleted prematurely
- **(D) Use Amazon S3 Object Lock in Compliance mode for Policy A, and S3 Glacier Vault Lock for Policy B** [CORRECT]
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock.html
- (G) via - https://aws.amazon.com/blogs/storage/protecting-data-with-amazon-s3-object-lock/
- (H) Incorrect options:
- (I) Use Amazon S3 Standard storage class with S3 Lifecycle policies for Policy A, and S3 Glacier Flexible Retrieval for Policy B - This option is incorrect because Lifecycle policies alone do not prevent deletion or modification—they are primarily for automated transitions and expirations.
- (J) Use Amazon S3 Glacier Vault Lock for both policies to reduce storage costs while enforcing retention - Glacier Vault Lock is not suitable for use cases requiring immediate access to data like Policy A.
- () Use Amazon S3 Object Lock in Governance mode for both policies to ensure data cannot be deleted prematurely - Governance mode allows certain users to override locks if they have permissions, which is not appropriate for strict compliance use cases.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock.html
- () https://aws.amazon.com/blogs/storage/protecting-data-with-amazon-s3-object-lock/
- () Your company is deploying a website running on AWS Elastic Beanstalk. The website takes over 45 minutes for the installation and contains both static as well as dynamic files that must be generated during the installation process.
- () As a Solutions Architect, you would like to bring the time to create a new instance in your AWS Elastic Beanstalk deployment to be less than 2 minutes. Which of the following options should be combined to build a solution for this requirement? (Select two)
- () Use AWS Elastic Beanstalk deployment caching feature
- () Correct selection
- () Create a Golden Amazon Machine Image (AMI) with the static installation components already setup
- () Store the installation files in Amazon S3 so they can be quickly retrieved
- () Use Amazon EC2 user data to install the application at boot time
- () Use Amazon EC2 user data to customize the dynamic installation parts at boot time
- () Correct options:
- () AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.
- () You can simply upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. At the same time, you retain full control over the AWS resources powering your application and can access the underlying resources at any time.
- () When you create an AWS Elastic Beanstalk environment, you can specify an Amazon Machine Image (AMI) to use instead of the standard Elastic Beanstalk AMI included in your platform version. A custom AMI can improve provisioning times when instances are launched in your environment if you need to install a lot of software that isn't included in the standard AMIs.
- () A Golden AMI is an AMI that you standardize through configuration, consistent security patching, and hardening. It also contains agents you approve for logging, security, performance monitoring, etc. For the given use-case, you can have the static installation components already setup via the golden AMI.
- () Amazon EC2 instance user data is the data that you specified in the form of a configuration script while launching your instance. You can use Amazon EC2 user data to customize the dynamic installation parts at boot time, rather than installing the application itself at boot time.
- () Store the installation files in Amazon S3 so they can be quickly retrieved - Amazon S3 bucket can be used as a storage location for your source code, logs, and other artifacts that are created when you use AWS Elastic Beanstalk. It cannot be used to run or generate dynamic files since Amazon S3 is not an environment but a storage service.
- () Use Amazon EC2 user data to install the application at boot time - User data of an instance can be used to perform common automated configuration tasks or run scripts after the instance starts. User data, cannot, however, be used to install the application since it takes over 45 minutes for the installation which contains static as well as dynamic files that must be generated during the installation process.
- () Use AWS Elastic Beanstalk deployment caching feature - AWS Elastic Beanstalk deployment caching is a made-up option. It is just added as a distractor.
- () https://aws.amazon.com/elasticbeanstalk/
- () https://aws.amazon.com/blogs/awsmarketplace/announcing-the-golden-ami-pipeline/
- () https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/AWSHowTo.S3.html
- () https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.customenv.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instancedata-add-user-data.html
- () For security purposes, a development team has decided to deploy the Amazon EC2 instances in a private subnet. The team plans to use VPC endpoints so that the instances can access some AWS services securely. The members of the team would like to know about the two AWS services that support Gateway Endpoints.

**Answer:**
Correct Answer: **Use Amazon S3 Object Lock in Compliance mode for Policy A, and S3 Glacier Vault Lock for Policy B**

---

## Question 63

**Q:** As a Solutions Architect, you would like to bring the time to create a new instance in your AWS Elastic Beanstalk deployment to be less than 2 minutes. Which of the following options should be combined to build a solution for this requirement? (Select two)

**Options:**
- **(A) Use AWS Elastic Beanstalk deployment caching feature** [CORRECT]
- (B) Correct selection
- (C) Create a Golden Amazon Machine Image (AMI) with the static installation components already setup
- (D) Store the installation files in Amazon S3 so they can be quickly retrieved
- (E) Use Amazon EC2 user data to install the application at boot time
- (F) Use Amazon EC2 user data to customize the dynamic installation parts at boot time
- (G) Correct options:
- (H) AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.
- (I) You can simply upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. At the same time, you retain full control over the AWS resources powering your application and can access the underlying resources at any time.
- (J) When you create an AWS Elastic Beanstalk environment, you can specify an Amazon Machine Image (AMI) to use instead of the standard Elastic Beanstalk AMI included in your platform version. A custom AMI can improve provisioning times when instances are launched in your environment if you need to install a lot of software that isn't included in the standard AMIs.
- () A Golden AMI is an AMI that you standardize through configuration, consistent security patching, and hardening. It also contains agents you approve for logging, security, performance monitoring, etc. For the given use-case, you can have the static installation components already setup via the golden AMI.
- () Amazon EC2 instance user data is the data that you specified in the form of a configuration script while launching your instance. You can use Amazon EC2 user data to customize the dynamic installation parts at boot time, rather than installing the application itself at boot time.
- () Incorrect options:
- () Store the installation files in Amazon S3 so they can be quickly retrieved - Amazon S3 bucket can be used as a storage location for your source code, logs, and other artifacts that are created when you use AWS Elastic Beanstalk. It cannot be used to run or generate dynamic files since Amazon S3 is not an environment but a storage service.
- () Use Amazon EC2 user data to install the application at boot time - User data of an instance can be used to perform common automated configuration tasks or run scripts after the instance starts. User data, cannot, however, be used to install the application since it takes over 45 minutes for the installation which contains static as well as dynamic files that must be generated during the installation process.
- () Use AWS Elastic Beanstalk deployment caching feature - AWS Elastic Beanstalk deployment caching is a made-up option. It is just added as a distractor.
- () References:
- () https://aws.amazon.com/elasticbeanstalk/
- () https://aws.amazon.com/blogs/awsmarketplace/announcing-the-golden-ami-pipeline/
- () https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/AWSHowTo.S3.html
- () https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.customenv.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instancedata-add-user-data.html
- () For security purposes, a development team has decided to deploy the Amazon EC2 instances in a private subnet. The team plans to use VPC endpoints so that the instances can access some AWS services securely. The members of the team would like to know about the two AWS services that support Gateway Endpoints.
- () As a solutions architect, which of the following services would you suggest for this requirement? (Select two)
- () Amazon DynamoDB
- () Amazon Kinesis
- () Amazon Simple Notification Service (Amazon SNS)
- () Amazon S3
- () Amazon Simple Queue Service (Amazon SQS)
- () A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.
- () Endpoints are virtual devices. They are horizontally scaled, redundant, and highly available VPC components. They allow communication between instances in your VPC and services without imposing availability risks or bandwidth constraints on your network traffic.
- () There are two types of VPC endpoints: Interface Endpoints and Gateway Endpoints. An Interface Endpoint is an Elastic Network Interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service.
- () A Gateway Endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service. The following AWS services are supported: Amazon S3 and Amazon DynamoDB.
- () You can use two types of VPC endpoints to access Amazon S3: gateway endpoints and interface endpoints. A gateway endpoint is a gateway that you specify in your route table to access Amazon S3 from your VPC over the AWS network. Interface endpoints extend the functionality of gateway endpoints by using private IP addresses to route requests to Amazon S3 from within your VPC, on premises, or from a VPC in another AWS Region using VPC peering or AWS Transit Gateway.
- () You must remember that these two services use a VPC gateway endpoint. The rest of the AWS services use VPC interface endpoints.
- () Gateway VPC endpoints:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpce-gateway.html
- () As mentioned in the description above, these three options use interface endpoints, so these are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html

**Answer:**
Correct Answer: **Use AWS Elastic Beanstalk deployment caching feature**

---

## Question 64

**Q:** As a solutions architect, which of the following services would you suggest for this requirement? (Select two)

**Options:**
- (A) Correct selection
- (B) Amazon DynamoDB
- (C) Amazon Kinesis
- (D) Amazon Simple Notification Service (Amazon SNS)
- (E) Amazon S3
- (F) Amazon Simple Queue Service (Amazon SQS)
- (G) Correct options:
- (H) A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.
- (I) Endpoints are virtual devices. They are horizontally scaled, redundant, and highly available VPC components. They allow communication between instances in your VPC and services without imposing availability risks or bandwidth constraints on your network traffic.
- (J) There are two types of VPC endpoints: Interface Endpoints and Gateway Endpoints. An Interface Endpoint is an Elastic Network Interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service.
- () A Gateway Endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service. The following AWS services are supported: Amazon S3 and Amazon DynamoDB.
- () You can use two types of VPC endpoints to access Amazon S3: gateway endpoints and interface endpoints. A gateway endpoint is a gateway that you specify in your route table to access Amazon S3 from your VPC over the AWS network. Interface endpoints extend the functionality of gateway endpoints by using private IP addresses to route requests to Amazon S3 from within your VPC, on premises, or from a VPC in another AWS Region using VPC peering or AWS Transit Gateway.
- () You must remember that these two services use a VPC gateway endpoint. The rest of the AWS services use VPC interface endpoints.
- () Gateway VPC endpoints:
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpce-gateway.html
- () Incorrect options:
- () As mentioned in the description above, these three options use interface endpoints, so these are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html
- () What would you recommend as an AWS Certified Solutions Architect - Associate?
- () Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon Kinesis Data Firehose to persist the data on Amazon S3. Lastly, use Amazon Athena to analyze the data in real time
- () Leverage Amazon SQS to capture the data from the website. Configure a fleet of Amazon EC2 instances under an Auto scaling group to process messages from the Amazon SQS queue and trigger the scaling policy based on the number of pending messages in the queue. Perform real-time analytics using a third-party library on the Amazon EC2 instances
- **() Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon Kinesis Data Analytics which can query the data in real time. Lastly, the analyzed feed is output into Amazon Kinesis Data Firehose to persist the data on Amazon S3** [CORRECT]
- () Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon QuickSight which can query the data in real time. Lastly, the analyzed feed is output into Kinesis Data Firehose to persist the data on Amazon S3
- () Correct option:
- () You can use Amazon Kinesis Data Streams to build custom applications that process or analyze streaming data for specialized needs. Amazon Kinesis Data Streams manages the infrastructure, storage, networking, and configuration needed to stream your data at the level of your data throughput. You don't have to worry about provisioning, deployment, or ongoing maintenance of hardware, software, or other services for your data streams.
- () Amazon Kinesis Data Analytics:
- () via - https://aws.amazon.com/kinesis/
- () Amazon Kinesis Data Firehose is an extract, transform, and load (ETL) service that reliably captures, transforms and delivers streaming data to data lakes, data stores, and analytics services.
- () For the given use case, post the real-time analysis, the output feed from Kinesis Data Analytics is output into Kinesis Data Firehose which dumps the data into Amazon S3 without any data loss.
- () Amazon Kinesis Data Firehose:
- () Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon QuickSight which can query the data in real time. Lastly, the analyzed feed is output into Kinesis Data Firehose to persist the data on Amazon S3 - Amazon QuickSight cannot use Amazon Kinesis Data Streams as a source. In addition, Amazon QuickSight cannot be used for real-time streaming data analysis from its source. Therefore this option is incorrect.
- () References:
- () https://aws.amazon.com/kinesis/

**Answer:**
Correct Answer: **Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon Kinesis Data Analytics which can query the data in real time. Lastly, the analyzed feed is output into Amazon Kinesis Data Firehose to persist the data on Amazon S3**

---

## Question 65

**Q:** What would you recommend as an AWS Certified Solutions Architect - Associate?

**Options:**
- (A) Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon Kinesis Data Firehose to persist the data on Amazon S3. Lastly, use Amazon Athena to analyze the data in real time
- (B) Leverage Amazon SQS to capture the data from the website. Configure a fleet of Amazon EC2 instances under an Auto scaling group to process messages from the Amazon SQS queue and trigger the scaling policy based on the number of pending messages in the queue. Perform real-time analytics using a third-party library on the Amazon EC2 instances
- **(C) Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon Kinesis Data Analytics which can query the data in real time. Lastly, the analyzed feed is output into Amazon Kinesis Data Firehose to persist the data on Amazon S3** [CORRECT]
- (D) Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon QuickSight which can query the data in real time. Lastly, the analyzed feed is output into Kinesis Data Firehose to persist the data on Amazon S3
- (E) Correct option:
- (F) You can use Amazon Kinesis Data Streams to build custom applications that process or analyze streaming data for specialized needs. Amazon Kinesis Data Streams manages the infrastructure, storage, networking, and configuration needed to stream your data at the level of your data throughput. You don't have to worry about provisioning, deployment, or ongoing maintenance of hardware, software, or other services for your data streams.
- (G) Amazon Kinesis Data Analytics:
- (H) via - https://aws.amazon.com/kinesis/
- (I) Amazon Kinesis Data Firehose is an extract, transform, and load (ETL) service that reliably captures, transforms and delivers streaming data to data lakes, data stores, and analytics services.
- (J) For the given use case, post the real-time analysis, the output feed from Kinesis Data Analytics is output into Kinesis Data Firehose which dumps the data into Amazon S3 without any data loss.
- () Amazon Kinesis Data Firehose:
- () Incorrect options:
- () Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon QuickSight which can query the data in real time. Lastly, the analyzed feed is output into Kinesis Data Firehose to persist the data on Amazon S3 - Amazon QuickSight cannot use Amazon Kinesis Data Streams as a source. In addition, Amazon QuickSight cannot be used for real-time streaming data analysis from its source. Therefore this option is incorrect.
- () References:
- () https://aws.amazon.com/kinesis/
- () https://aws.amazon.com/quicksight/resources/faqs/
- () An e-commerce company wants to migrate its on-premises application to AWS. The application consists of application servers and a Microsoft SQL Server database. The solution should result in the maximum possible availability for the database layer while minimizing operational and management overhead.

**Answer:**
Correct Answer: **Leverage Amazon Kinesis Data Streams to capture the data from the website and feed it into Amazon Kinesis Data Analytics which can query the data in real time. Lastly, the analyzed feed is output into Amazon Kinesis Data Firehose to persist the data on Amazon S3**

---

## Question 66

**Q:** As a solutions architect, which of the following would you recommend to meet the given requirements?

**Options:**
- (A) Migrate the data to Amazon RDS for SQL Server database in a Multi-AZ deployment
- (B) Migrate the data to Amazon RDS for SQL Server database in a cross-region Multi-AZ deployment
- (C) Migrate the data to Amazon RDS for SQL Server database in a cross-region read-replica configuration
- (D) Migrate the data to Amazon EC2 instance hosted SQL Server database. Deploy the Amazon EC2 instances in a Multi-AZ configuration
- (E) Correct option:
- (F) Amazon RDS supports Multi-AZ deployments for Microsoft SQL Server by using either SQL Server Database Mirroring (DBM) or Always On Availability Groups (AGs). Amazon RDS monitors and maintains the health of your Multi-AZ deployment. If problems occur, Amazon RDS automatically repairs unhealthy database instances, reestablishes synchronization, and initiates failovers.
- (G) This option provides the maximum possible availability for the database layer while minimizing operational and management overhead.
- (H) Incorrect options:
- (I) Migrate the data to Amazon EC2 instance hosted SQL Server database. Deploy the Amazon EC2 instances in a Multi-AZ configuration - Hosting SQL Server database on Amazon EC2 instance involves significant operational and management overhead in terms of OS patching, database patching, etc. So this option is incorrect.
- (J) Migrate the data to Amazon RDS for SQL Server database in a cross-region read-replica configuration - Amazon RDS Read Replicas enable you to create one or more read-only copies of your database instance within the same AWS Region or in a different AWS Region. Read replicas are used to enhance the read scalability of a database. You cannot use read replicas to improve the availability of a database. Therefore this option is incorrect.
- () Migrate the data to Amazon RDS for SQL Server database in a cross-region Multi-AZ deployment - Amazon RDS Multi-AZ deployments provide enhanced availability for database instances within a single AWS Region. There is no such thing as a cross-region Multi-AZ deployment. Hence this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_SQLServerMultiAZ.html
- () https://aws.amazon.com/about-aws/whats-new/2018/01/amazon-rds-read-replicas-now-support-multi-az-deployments/
- ()  from the old Load Balancer to the new one.
- () The users are still not redirected to the new Load Balancer. What has gone wrong in the configuration?
- () The Alias Record is misconfigured
- () The Time To Live (TTL) is still in effect
- () The health checks are failing
- () The CNAME Record is misconfigured
- () Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. Amazon Route 53 effectively connects user requests to infrastructure running in AWS – such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3 buckets – and can also be used to route users to infrastructure outside of AWS.
- () You can use Amazon Route 53 to configure DNS health checks to route traffic to healthy endpoints or to independently monitor the health of your application and its endpoints. Amazon Route 53 Traffic Flow makes it easy for you to manage traffic globally through a variety of routing types, including Latency Based Routing, Geo DNS, Geoproximity, and Weighted Round Robin—all of which can be combined with DNS Failover to enable a variety of low-latency, fault-tolerant architectures.
- () TTL (time to live), is the amount of time, in seconds, that you want DNS recursive resolvers to cache information about a record. If you specify a longer value (for example, 172800 seconds, or two days), you reduce the number of calls that DNS recursive resolvers must make to Amazon Route 53 to get the latest information for the record. This has the effect of reducing latency and reducing your bill for Route 53 service.
- () However, if you specify a longer value for TTL, it takes longer for changes to the record (for example, a new IP address) to take effect because recursive resolvers use the values in their cache for longer periods before they ask Route 53 for the latest information. If you're changing settings for a domain or subdomain that's already in use, AWS recommends that you initially specify a shorter value, such as 300 seconds, and increase the value after you confirm that the new settings are correct.
- () For this use-case, the most likely issue is that the TTL is still in effect so you have to wait until it expires for the new request to perform another DNS query and get the value for the new Load Balancer.
- () The CNAME Record is misconfigured - A CNAME record can redirect DNS queries to any DNS record. For example, you can create a CNAME record that redirects queries from acme.example.com to zenith.example.com or to acme.example.org. You don't need to use Amazon Route 53 as the DNS service for the domain that you're redirecting queries to.
- () The health checks are failing - Simple Records do not have health checks, so this option is incorrect.
- () https://aws.amazon.com/route53/
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-values-basic.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html
- () An e-commerce analytics company is preparing to archive several years of transaction records and customer analytics reports in Amazon S3 for long-term storage. To meet compliance requirements, the archived data must be encrypted at rest. Additionally, the solution must be cost-effective and ensure that key rotation occurs automatically every 12 months to comply with the company’s internal data governance policy.
- () Which solution will meet these requirements with the least operational overhead?
- () Encrypt the data locally using client-side encryption libraries and upload the encrypted files to S3. Create a KMS key with imported key material and configure key rotation settings
- **() Use AWS Key Management Service (KMS) to create a customer managed key with automatic rotation enabled. Configure the S3 bucket’s default encryption to use the customer managed key. Migrate the data to the S3 bucket** [CORRECT]
- () Use AWS CloudHSM to generate encryption keys. Configure S3 to use these custom encryption keys via client-side encryption and rotate the keys annually using an on-premises key management workflow
- () Use Amazon S3 server-side encryption with S3-managed keys (SSE-S3). Upload data with default encryption enabled. Rely on the built-in key management and rotation behavior of SSE-S3
- () This solution provides the lowest operational overhead while meeting both encryption and automatic annual key rotation requirements. By creating a customer managed KMS key and enabling automatic key rotation, AWS KMS will handle rotation every year without manual action. Configuring the S3 bucket's default encryption to use this KMS key ensures that all new objects are automatically encrypted at rest, regardless of upload method. This is a fully managed, secure, and compliant approach.

**Answer:**
Correct Answer: **Use AWS Key Management Service (KMS) to create a customer managed key with automatic rotation enabled. Configure the S3 bucket’s default encryption to use the customer managed key. Migrate the data to the S3 bucket**

---

## Question 67

**Q:** The users are still not redirected to the new Load Balancer. What has gone wrong in the configuration?

**Options:**
- (A) The Alias Record is misconfigured
- (B) The Time To Live (TTL) is still in effect
- (C) The health checks are failing
- (D) The CNAME Record is misconfigured
- (E) Correct option:
- (F) Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. Amazon Route 53 effectively connects user requests to infrastructure running in AWS – such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3 buckets – and can also be used to route users to infrastructure outside of AWS.
- (G) You can use Amazon Route 53 to configure DNS health checks to route traffic to healthy endpoints or to independently monitor the health of your application and its endpoints. Amazon Route 53 Traffic Flow makes it easy for you to manage traffic globally through a variety of routing types, including Latency Based Routing, Geo DNS, Geoproximity, and Weighted Round Robin—all of which can be combined with DNS Failover to enable a variety of low-latency, fault-tolerant architectures.
- (H) TTL (time to live), is the amount of time, in seconds, that you want DNS recursive resolvers to cache information about a record. If you specify a longer value (for example, 172800 seconds, or two days), you reduce the number of calls that DNS recursive resolvers must make to Amazon Route 53 to get the latest information for the record. This has the effect of reducing latency and reducing your bill for Route 53 service.
- (I) However, if you specify a longer value for TTL, it takes longer for changes to the record (for example, a new IP address) to take effect because recursive resolvers use the values in their cache for longer periods before they ask Route 53 for the latest information. If you're changing settings for a domain or subdomain that's already in use, AWS recommends that you initially specify a shorter value, such as 300 seconds, and increase the value after you confirm that the new settings are correct.
- (J) For this use-case, the most likely issue is that the TTL is still in effect so you have to wait until it expires for the new request to perform another DNS query and get the value for the new Load Balancer.
- () Incorrect options:
- () The CNAME Record is misconfigured - A CNAME record can redirect DNS queries to any DNS record. For example, you can create a CNAME record that redirects queries from acme.example.com to zenith.example.com or to acme.example.org. You don't need to use Amazon Route 53 as the DNS service for the domain that you're redirecting queries to.
- () The health checks are failing - Simple Records do not have health checks, so this option is incorrect.
- () References:
- () https://aws.amazon.com/route53/
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-values-basic.html
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-choosing-alias-non-alias.html
- () An e-commerce analytics company is preparing to archive several years of transaction records and customer analytics reports in Amazon S3 for long-term storage. To meet compliance requirements, the archived data must be encrypted at rest. Additionally, the solution must be cost-effective and ensure that key rotation occurs automatically every 12 months to comply with the company’s internal data governance policy.
- () Which solution will meet these requirements with the least operational overhead?
- () Encrypt the data locally using client-side encryption libraries and upload the encrypted files to S3. Create a KMS key with imported key material and configure key rotation settings
- () Use AWS Key Management Service (KMS) to create a customer managed key with automatic rotation enabled. Configure the S3 bucket’s default encryption to use the customer managed key. Migrate the data to the S3 bucket
- () Use AWS CloudHSM to generate encryption keys. Configure S3 to use these custom encryption keys via client-side encryption and rotate the keys annually using an on-premises key management workflow
- () Use Amazon S3 server-side encryption with S3-managed keys (SSE-S3). Upload data with default encryption enabled. Rely on the built-in key management and rotation behavior of SSE-S3
- () This solution provides the lowest operational overhead while meeting both encryption and automatic annual key rotation requirements. By creating a customer managed KMS key and enabling automatic key rotation, AWS KMS will handle rotation every year without manual action. Configuring the S3 bucket's default encryption to use this KMS key ensures that all new objects are automatically encrypted at rest, regardless of upload method. This is a fully managed, secure, and compliant approach.
- () via - https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html
- () Use Amazon S3 server-side encryption with S3-managed keys (SSE-S3). Upload data with default encryption enabled. Rely on the built-in key management and rotation behavior of SSE-S3 - While SSE-S3 provides at-rest encryption with no additional configuration, it uses Amazon-managed keys, and key rotation is not user-configurable or trackable. SSE-S3 keys are rotated irregularly behind the scenes, which does not satisfy compliance requirements that call for annual, auditable key rotation.
- () Encrypt the data locally using client-side encryption libraries and upload the encrypted files to S3. Create a KMS key with imported key material and configure key rotation settings - This option adds unnecessary operational complexity. When using imported key material in KMS, automatic rotation is disabled, the customer is responsible for manually rotating and re-importing the key material. This defeats the goal of minimizing operational overhead and complicates compliance validation.
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingKMSEncryption.html
- () https://docs.aws.amazon.com/kms/latest/developerguide/rotate-keys.html
- () https://docs.aws.amazon.com/kms/latest/developerguide/importing-keys.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingServerSideEncryption.html
- () https://docs.aws.amazon.com/cloudhsm/latest/userguide/introduction.html
- () Which solution should the architect implement to resolve this issue with the least operational overhead?
- () Enable Amazon EC2 Auto Scaling with custom CloudWatch alarms based on cluster-wide CPU and memory usage to dynamically adjust node count in the EKS worker node group
- () Use AWS Fargate to replace the EKS worker nodes with serverless compute profiles, allowing Fargate to scale pods automatically without managing EC2 infrastructure
- () Implement an AWS Lambda function that runs every 10 minutes and checks EKS pod scheduling status. Trigger node scaling manually using the eksctl CLI or AWS SDK if unschedulable pods are detected
- **() Deploy the Kubernetes Cluster Autoscaler to the EKS cluster. Configure it to integrate with the existing EC2 Auto Scaling group to automatically launch or terminate nodes based on pending pod demands** [CORRECT]

**Answer:**
Correct Answer: **Deploy the Kubernetes Cluster Autoscaler to the EKS cluster. Configure it to integrate with the existing EC2 Auto Scaling group to automatically launch or terminate nodes based on pending pod demands**

---

## Question 68

**Q:** Which solution should the architect implement to resolve this issue with the least operational overhead?

**Options:**
- (A) Enable Amazon EC2 Auto Scaling with custom CloudWatch alarms based on cluster-wide CPU and memory usage to dynamically adjust node count in the EKS worker node group
- (B) Use AWS Fargate to replace the EKS worker nodes with serverless compute profiles, allowing Fargate to scale pods automatically without managing EC2 infrastructure
- (C) Implement an AWS Lambda function that runs every 10 minutes and checks EKS pod scheduling status. Trigger node scaling manually using the eksctl CLI or AWS SDK if unschedulable pods are detected
- **(D) Deploy the Kubernetes Cluster Autoscaler to the EKS cluster. Configure it to integrate with the existing EC2 Auto Scaling group to automatically launch or terminate nodes based on pending pod demands** [CORRECT]
- (E) Correct option:
- (F) The Kubernetes Cluster Autoscaler is the recommended and most seamless solution to automatically manage the size of an EKS cluster's underlying compute resources. It works in tandem with the Kubernetes scheduler and continuously monitors the cluster for unschedulable pods—these are pods that cannot be scheduled due to a lack of available resources (CPU, memory, etc.) on the current set of EC2 nodes.
- (G) This approach ensures the EKS cluster is highly elastic, cost-effective, and operationally simple, making it the best fit for real-time, variable workloads with minimal administrative overhead.
- (H) via - https://aws.amazon.com/blogs/aws/introducing-karpenter-an-open-source-high-performance-kubernetes-cluster-autoscaler/
- (I) Incorrect options:
- (J) Implement an AWS Lambda function that runs every 10 minutes and checks EKS pod scheduling status. Trigger node scaling manually using the eksctl CLI or AWS SDK if unschedulable pods are detected - While feasible, this solution introduces high operational overhead by requiring a custom polling mechanism, Lambda orchestration, and script maintenance. It lacks the native intelligence of Cluster Autoscaler and is harder to maintain and troubleshoot.
- () References:
- () https://aws.amazon.com/blogs/aws/introducing-karpenter-an-open-source-high-performance-kubernetes-cluster-autoscaler/
- () https://aws.amazon.com/blogs/containers/amazon-eks-cluster-multi-zone-auto-scaling-groups/
- () https://docs.aws.amazon.com/eks/latest/userguide/fargate.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () A company has developed a popular photo-sharing website using a serverless pattern on the AWS Cloud using Amazon API Gateway and AWS Lambda. The backend uses an Amazon RDS PostgreSQL database. The website is experiencing high read traffic and the AWS Lambda functions are putting an increased read load on the Amazon RDS database.

**Answer:**
Correct Answer: **Deploy the Kubernetes Cluster Autoscaler to the EKS cluster. Configure it to integrate with the existing EC2 Auto Scaling group to automatically launch or terminate nodes based on pending pod demands**

---

## Question 69

**Q:** The architecture team is planning to increase the read throughput of the database, without changing the application's core logic. As a Solutions Architect, what do you recommend?

**Options:**
- (A) Use Amazon RDS Read Replicas
- (B) Use Amazon ElastiCache
- (C) Use Amazon DynamoDB
- (D) Use Amazon RDS Multi-AZ feature
- (E) Correct option:
- (F) More on Amazon RDS Read Replicas:
- (G) via - https://aws.amazon.com/rds/features/read-replicas/
- (H) Incorrect options:
- (I) Use Amazon ElastiCache - Amazon ElastiCache allows you to seamlessly set up, run, and scale popular open-Source compatible in-memory data stores in the cloud. Build data-intensive apps or boost the performance of your existing databases by retrieving data from high throughput and low latency in-memory data stores. Amazon ElastiCache is a popular choice for real-time use cases like Caching, Session Stores, Gaming, Geospatial Services, Real-Time Analytics, and Queuing.
- (J) Use Amazon DynamoDB - Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. Amazon DynamoDB can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.
- () Amazon RDS Multi-AZ helps with disaster recovery in case of an AZ failure. Amazon ElastiCache would definitely help with the read load, but would require a refactor of the application's core logic. Amazon DynamoDB with DAX would also probably help with the read load, but once again it would require a refactor of the application's core logic. Here, our only option to scale reads is to use Amazon RDS Read Replicas.
- () References:
- () https://aws.amazon.com/rds/features/multi-az/
- () https://aws.amazon.com/rds/features/read-replicas/
- () A niche social media application allows users to connect with sports athletes. As a solutions architect, you've designed the architecture of the application to be fully serverless using Amazon API Gateway and AWS Lambda. The backend uses an Amazon DynamoDB table. Some of the star athletes using the application are highly popular, and therefore Amazon DynamoDB has increased the read capacity units (RCUs). Still, the application is experiencing a hot partition problem.
- () What can you do to improve the performance of Amazon DynamoDB and eliminate the hot partition problem without a lot of application refactoring?
- **() Use Amazon DynamoDB DAX** [CORRECT]
- () Use Amazon DynamoDB Streams
- () Use Amazon DynamoDB Global Tables
- () Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.
- () Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second. DAX does all the heavy lifting required to add in-memory acceleration to your DynamoDB tables, without requiring developers to manage cache invalidation, data population, or cluster management.
- () . Therefore, this is the correct option.
- () Use Amazon DynamoDB Global Tables - Amazon DynamoDB Global Tables builds upon DynamoDB’s global footprint to provide you with a fully managed, multi-region, and multi-master database that provides fast, local, read and write performance for massively scaled, global applications. Global Tables replicates your Amazon DynamoDB tables automatically across your choice of AWS regions. But Global Tables cannot address the hotkey issue.
- () https://aws.amazon.com/dynamodb/dax/
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html
- () A digital media company needs to manage uploads of around 1 terabyte each from an application being used by a partner company.

**Answer:**
Correct Answer: **Use Amazon DynamoDB DAX**

---

## Question 70

**Q:** What can you do to improve the performance of Amazon DynamoDB and eliminate the hot partition problem without a lot of application refactoring?

**Options:**
- **(A) Use Amazon DynamoDB DAX** [CORRECT]
- (B) Use Amazon DynamoDB Streams
- (C) Use Amazon ElastiCache
- (D) Use Amazon DynamoDB Global Tables
- (E) Correct option:
- (F) Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.
- (G) Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second. DAX does all the heavy lifting required to add in-memory acceleration to your DynamoDB tables, without requiring developers to manage cache invalidation, data population, or cluster management.
- (H) . Therefore, this is the correct option.
- (I) Incorrect options:
- (J) Use Amazon DynamoDB Global Tables - Amazon DynamoDB Global Tables builds upon DynamoDB’s global footprint to provide you with a fully managed, multi-region, and multi-master database that provides fast, local, read and write performance for massively scaled, global applications. Global Tables replicates your Amazon DynamoDB tables automatically across your choice of AWS regions. But Global Tables cannot address the hotkey issue.
- () References:
- () https://aws.amazon.com/dynamodb/dax/
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html
- () A digital media company needs to manage uploads of around 1 terabyte each from an application being used by a partner company.

**Answer:**
Correct Answer: **Use Amazon DynamoDB DAX**

---

## Question 71

**Q:** As a Solutions Architect, how will you handle the upload of these files to Amazon S3?

**Options:**
- (A) Use AWS Snowball
- **(B) Use multi-part upload feature of Amazon S3** [CORRECT]
- (C) Use AWS Direct Connect to provide extra bandwidth
- (D) Use Amazon S3 Versioning
- (E) Correct option:
- (F) Multi-part upload allows you to upload a single object as a set of parts. Each part is a contiguous portion of the object's data. You can upload these object parts independently and in any order. If transmission of any part fails, you can retransmit that part without affecting other parts. After all parts of your object are uploaded, Amazon S3 assembles these parts and creates the object.
- (G) In general, when your object size reaches 100 megabytes, you should consider using multipart uploads instead of uploading the object in a single operation. If the file is greater than 5 gigabytes in size, you must use multi-part upload to upload that file to Amazon S3.
- (H) Incorrect options:
- (I) Use AWS Direct Connect to provide extra bandwidth - AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS. Using AWS Direct Connect, you can establish private connectivity between AWS and your datacenter, office, or colocation environment, which in many cases can reduce your network costs, increase bandwidth throughput, and provide a more consistent network experience than Internet-based connections.
- (J) Use AWS Snowball - AWS Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 terabytes of usable HDD storage, 40 vCPUs, 1 TB of SATA SSD storage, and up to 40 gigabytes network connectivity to address large scale data transfer and pre-processing use cases.
- () (The original AWS Snowball devices were transitioned out of service and AWS Snowball Edge Storage Optimized are now the primary devices used for data transfer. You may see the Snowball device on the exam, just remember that the original AWS Snowball device had 80 terabytes of storage space).
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/uploadobjusingmpu.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UploadingObjects.html
- () The engineering team at a social media company has recently migrated to AWS Cloud from its on-premises data center. The team is evaluating Amazon CloudFront to be used as a CDN for its flagship application. The team has hired you as an AWS Certified Solutions Architect – Associate to advise on Amazon CloudFront capabilities on routing, security, and high availability.
- () Which of the following would you identify as correct regarding Amazon CloudFront? (Select three)
- () Correct selection
- () Use field level encryption in Amazon CloudFront to protect sensitive data for specific content
- () Amazon CloudFront can route to multiple origins based on the content type
- () Use an origin group with primary and secondary origins to configure Amazon CloudFront for high-availability and failover
- () Amazon CloudFront can route to multiple origins based on the price class
- () Use AWS Key Management Service (AWS KMS) encryption in Amazon CloudFront to protect sensitive data for specific content
- () Use geo restriction to configure Amazon CloudFront for high-availability and failover
- () Correct options:
- () You can configure a single Amazon CloudFront web distribution to serve different types of requests from multiple origins. For example, if you are building a website that serves static content from an Amazon Simple Storage Service (Amazon S3) bucket and dynamic content from a load balancer, you can serve both types of content from a Amazon CloudFront web distribution.
- () You can set up Amazon CloudFront with origin failover for scenarios that require high availability. To get started, you create an origin group with two origins: a primary and a secondary. If the primary origin is unavailable or returns specific HTTP response status codes that indicate a failure, CloudFront automatically switches to the secondary origin.
- () To set up origin failover, you must have a distribution with at least two origins. Next, you create an origin group for your distribution that includes two origins, setting one as the primary. Finally, you create or update a cache behavior to use the origin group.
- () via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html
- () Field-level encryption allows you to enable your users to securely upload sensitive information to your web servers. The sensitive information provided by your users is encrypted at the edge, close to the user, and remains encrypted throughout your entire application stack. This encryption ensures that only applications that need the data—and have the credentials to decrypt it—are able to do so.
- () To use field-level encryption, when you configure your Amazon CloudFront distribution, specify the set of fields in POST requests that you want to be encrypted, and the public key to use to encrypt them. You can encrypt up to 10 data fields in a request. (You can’t encrypt all of the data in a request with field-level encryption; you must specify individual fields to encrypt.)
- () via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html
- () Use AWS Key Management Service (AWS KMS) encryption in Amazon CloudFront to protect sensitive data for specific content - This option has been added as a distractor. You can use field level encryption in Amazon CloudFront to protect sensitive data for specific content.
- () Use geo restriction to configure Amazon CloudFront for high-availability and failover - You can use geo restriction, also known as geo blocking, to prevent users in specific geographic locations from accessing content that you're distributing through a Amazon CloudFront distribution. Geo restriction is not used to configure Amazon CloudFront for high availability and failover.
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html

**Answer:**
Correct Answer: **Use multi-part upload feature of Amazon S3**

---

## Question 72

**Q:** Which of the following would you identify as correct regarding Amazon CloudFront? (Select three)

**Options:**
- (A) Correct selection
- (B) Use field level encryption in Amazon CloudFront to protect sensitive data for specific content
- (C) Amazon CloudFront can route to multiple origins based on the content type
- (D) Use an origin group with primary and secondary origins to configure Amazon CloudFront for high-availability and failover
- (E) Amazon CloudFront can route to multiple origins based on the price class
- (F) Use AWS Key Management Service (AWS KMS) encryption in Amazon CloudFront to protect sensitive data for specific content
- (G) Use geo restriction to configure Amazon CloudFront for high-availability and failover
- (H) Correct options:
- (I) You can configure a single Amazon CloudFront web distribution to serve different types of requests from multiple origins. For example, if you are building a website that serves static content from an Amazon Simple Storage Service (Amazon S3) bucket and dynamic content from a load balancer, you can serve both types of content from a Amazon CloudFront web distribution.
- (J) You can set up Amazon CloudFront with origin failover for scenarios that require high availability. To get started, you create an origin group with two origins: a primary and a secondary. If the primary origin is unavailable or returns specific HTTP response status codes that indicate a failure, CloudFront automatically switches to the secondary origin.
- () To set up origin failover, you must have a distribution with at least two origins. Next, you create an origin group for your distribution that includes two origins, setting one as the primary. Finally, you create or update a cache behavior to use the origin group.
- () via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html
- () Field-level encryption allows you to enable your users to securely upload sensitive information to your web servers. The sensitive information provided by your users is encrypted at the edge, close to the user, and remains encrypted throughout your entire application stack. This encryption ensures that only applications that need the data—and have the credentials to decrypt it—are able to do so.
- () To use field-level encryption, when you configure your Amazon CloudFront distribution, specify the set of fields in POST requests that you want to be encrypted, and the public key to use to encrypt them. You can encrypt up to 10 data fields in a request. (You can’t encrypt all of the data in a request with field-level encryption; you must specify individual fields to encrypt.)
- () via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html
- () Incorrect options:
- () Use AWS Key Management Service (AWS KMS) encryption in Amazon CloudFront to protect sensitive data for specific content - This option has been added as a distractor. You can use field level encryption in Amazon CloudFront to protect sensitive data for specific content.
- () Use geo restriction to configure Amazon CloudFront for high-availability and failover - You can use geo restriction, also known as geo blocking, to prevent users in specific geographic locations from accessing content that you're distributing through a Amazon CloudFront distribution. Geo restriction is not used to configure Amazon CloudFront for high availability and failover.
- () References:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/high_availability_origin_failover.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PriceClass.html
- () Which solution will best meet these requirements in a cost-effective manner?
- () Convert the Aurora MySQL DB cluster into a multi-writer setup using Aurora global database. Allow concurrent writes from multiple application nodes across Regions
- **() Integrate Amazon ElastiCache for Redis between the application and Aurora. Cache frequently accessed query results in Redis to reduce the number of identical read requests hitting the database** [CORRECT]
- () Add another Aurora read replica to distribute the increasing read load across more read nodes. Adjust the application to perform client-side load balancing across the read replicas
- () Enable Aurora Serverless v2 for the DB cluster to automatically scale read and write capacity in response to usage spikes. Route all traffic through the cluster endpoint
- () Correct option:
- () Convert the Aurora MySQL DB cluster into a multi-writer setup using Aurora global database. Allow concurrent writes from multiple application nodes across Regions - Aurora multi-writer setups are designed for globally distributed write workloads, not for optimizing local repeated reads. Multi-writer configurations increase cost and add complexity with conflict resolution and write coordination. This is overkill for a workload that’s bottlenecked on read traffic, not write concurrency.
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/elasticache-use-cases.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
- () A retail company is using AWS Site-to-Site VPN connections for secure connectivity to its AWS cloud resources from its on-premises data center. Due to a surge in traffic across the VPN connections to the AWS cloud, users are experiencing slower VPN connectivity.

**Answer:**
Correct Answer: **Integrate Amazon ElastiCache for Redis between the application and Aurora. Cache frequently accessed query results in Redis to reduce the number of identical read requests hitting the database**

---

## Question 73

**Q:** Which solution will best meet these requirements in a cost-effective manner?

**Options:**
- (A) Convert the Aurora MySQL DB cluster into a multi-writer setup using Aurora global database. Allow concurrent writes from multiple application nodes across Regions
- (B) Integrate Amazon ElastiCache for Redis between the application and Aurora. Cache frequently accessed query results in Redis to reduce the number of identical read requests hitting the database
- (C) Add another Aurora read replica to distribute the increasing read load across more read nodes. Adjust the application to perform client-side load balancing across the read replicas
- (D) Enable Aurora Serverless v2 for the DB cluster to automatically scale read and write capacity in response to usage spikes. Route all traffic through the cluster endpoint
- (E) Correct option:
- (F) Incorrect options:
- (G) Convert the Aurora MySQL DB cluster into a multi-writer setup using Aurora global database. Allow concurrent writes from multiple application nodes across Regions - Aurora multi-writer setups are designed for globally distributed write workloads, not for optimizing local repeated reads. Multi-writer configurations increase cost and add complexity with conflict resolution and write coordination. This is overkill for a workload that’s bottlenecked on read traffic, not write concurrency.
- (H) References:
- (I) https://docs.aws.amazon.com/AmazonElastiCache/latest/dg/elasticache-use-cases.html
- (J) https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
- () A retail company is using AWS Site-to-Site VPN connections for secure connectivity to its AWS cloud resources from its on-premises data center. Due to a surge in traffic across the VPN connections to the AWS cloud, users are experiencing slower VPN connectivity.
- () Which of the following options will maximize the VPN throughput?
- () Create a virtual private gateway with equal cost multipath routing and multiple channels
- () Create an AWS Transit Gateway with equal cost multipath routing and add additional VPN tunnels
- () Use Transfer Acceleration for the VPN connection to maximize the throughput
- () Use AWS Global Accelerator for the VPN connection to maximize the throughput
- () VPN connection is a secure connection between your on-premises equipment and your VPCs. Each VPN connection has two VPN tunnels which you can use for high availability. A VPN tunnel is an encrypted link where data can pass from the customer network to or from AWS. The following diagram shows the high-level connectivity with virtual private gateways.
- () via - https://aws.amazon.com/premiumsupport/knowledge-center/transit-gateway-ecmp-multiple-tunnels/
- () Use Transfer Acceleration for the VPN connection to maximize the throughput - Transfer Acceleration is an Amazon S3 bucket-level feature that enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration is designed to optimize transfer speeds from across the world into S3 buckets. Transfer Acceleration takes advantage of the globally distributed edge locations in Amazon CloudFront.
- () This option has been added as a distractor as it is not relevant to AWS VPN connections.
- () AWS Global Accelerator can be used to optimize the network path, using the congestion-free AWS global network to route traffic to the endpoint that provides the best application performance . You can use an accelerated VPN connection to avoid network disruptions that might occur when traffic is routed over the public internet. AWS Global Accelerator will not maximize the VPN throughput, so it is not the best fit for the given use case.
- () Create a virtual private gateway with equal cost multipath routing and multiple channels - A virtual private gateway is the VPN endpoint on the Amazon side of your Site-to-Site VPN connection that can be attached to a single VPC. A virtual private gateway does not support equal cost multi-path (ECMP) routing, so this option is incorrect.
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- () https://aws.amazon.com/premiumsupport/knowledge-center/transit-gateway-ecmp-multiple-tunnels/
- () A systems administrator is creating IAM policies and attaching them to IAM identities. After creating the necessary identity-based policies, the administrator is now creating resource-based policies.
- () Which is the only resource-based policy that the IAM service supports?
- () AWS Organizations Service Control Policies (SCP)
- () Access control list (ACL)
- () Permissions boundary
- **() Trust policy** [CORRECT]
- () Trust policies define which principal entities (accounts, users, roles, and federated users) can assume the role. An IAM role is both an identity and a resource that supports resource-based policies. For this reason, you must attach both a trust policy and an identity-based policy to an IAM role. The IAM service supports only one type of resource-based policy called a role trust policy, which is attached to an IAM role.

**Answer:**
Correct Answer: **Trust policy**

---

## Question 74

**Q:** Which of the following options will maximize the VPN throughput?

**Options:**
- (A) Create a virtual private gateway with equal cost multipath routing and multiple channels
- (B) Create an AWS Transit Gateway with equal cost multipath routing and add additional VPN tunnels
- (C) Use Transfer Acceleration for the VPN connection to maximize the throughput
- (D) Use AWS Global Accelerator for the VPN connection to maximize the throughput
- (E) Correct option:
- (F) VPN connection is a secure connection between your on-premises equipment and your VPCs. Each VPN connection has two VPN tunnels which you can use for high availability. A VPN tunnel is an encrypted link where data can pass from the customer network to or from AWS. The following diagram shows the high-level connectivity with virtual private gateways.
- (G) via - https://aws.amazon.com/premiumsupport/knowledge-center/transit-gateway-ecmp-multiple-tunnels/
- (H) Incorrect options:
- (I) Use Transfer Acceleration for the VPN connection to maximize the throughput - Transfer Acceleration is an Amazon S3 bucket-level feature that enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration is designed to optimize transfer speeds from across the world into S3 buckets. Transfer Acceleration takes advantage of the globally distributed edge locations in Amazon CloudFront.
- (J) This option has been added as a distractor as it is not relevant to AWS VPN connections.
- () AWS Global Accelerator can be used to optimize the network path, using the congestion-free AWS global network to route traffic to the endpoint that provides the best application performance . You can use an accelerated VPN connection to avoid network disruptions that might occur when traffic is routed over the public internet. AWS Global Accelerator will not maximize the VPN throughput, so it is not the best fit for the given use case.
- () Create a virtual private gateway with equal cost multipath routing and multiple channels - A virtual private gateway is the VPN endpoint on the Amazon side of your Site-to-Site VPN connection that can be attached to a single VPC. A virtual private gateway does not support equal cost multi-path (ECMP) routing, so this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- () https://aws.amazon.com/premiumsupport/knowledge-center/transit-gateway-ecmp-multiple-tunnels/
- () A systems administrator is creating IAM policies and attaching them to IAM identities. After creating the necessary identity-based policies, the administrator is now creating resource-based policies.
- () Which is the only resource-based policy that the IAM service supports?
- () AWS Organizations Service Control Policies (SCP)
- () Access control list (ACL)
- () Permissions boundary
- **() Trust policy** [CORRECT]
- () Trust policies define which principal entities (accounts, users, roles, and federated users) can assume the role. An IAM role is both an identity and a resource that supports resource-based policies. For this reason, you must attach both a trust policy and an identity-based policy to an IAM role. The IAM service supports only one type of resource-based policy called a role trust policy, which is attached to an IAM role.
- () AWS Organizations Service Control Policies (SCP) - If you enable all features of AWS organization, then you can apply service control policies (SCPs) to any or all of your accounts. SCPs are JSON policies that specify the maximum permissions for an organization or organizational unit (OU). The SCP limits permissions for entities in member accounts, including each AWS account root user. An explicit deny in any of these policies overrides the allow.
- () Access control list (ACL) - Access control lists (ACLs) are service policies that allow you to control which principals in another account can access a resource. ACLs cannot be used to control access for a principal within the same account. Amazon S3, AWS WAF, and Amazon VPC are examples of services that support ACLs.
- () Permissions boundary - AWS supports permissions boundaries for IAM entities (users or roles). A permissions boundary is an advanced feature for using a managed policy to set the maximum permissions that an identity-based policy can grant to an IAM entity. An entity's permissions boundary allows it to perform only the actions that are allowed by both its identity-based policies and its permissions boundaries.
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html#policies_resource-based
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
- () A company runs a popular dating website on the AWS Cloud. As a Solutions Architect, you've designed the architecture of the website to follow a serverless pattern on the AWS Cloud using Amazon API Gateway and AWS Lambda. The backend uses an Amazon RDS PostgreSQL database. Currently, the application uses a username and password combination to connect the AWS Lambda function to the Amazon RDS database.
- () You would like to improve the security at the authentication level by leveraging short-lived credentials. What will you choose? (Select two)
- () Correct selection
- () Attach an AWS Identity and Access Management (IAM) role to AWS Lambda
- () Use IAM authentication from AWS Lambda to Amazon RDS PostgreSQL
- () Deploy AWS Lambda in a VPC
- () Restrict the Amazon RDS database security group to the AWS Lambda's security group
- () Embed a credential rotation logic in the AWS Lambda, retrieving them from SSM
- () Correct options:

**Answer:**
Correct Answer: **Trust policy**

---

## Question 75

**Q:** Which is the only resource-based policy that the IAM service supports?

**Options:**
- (A) AWS Organizations Service Control Policies (SCP)
- (B) Access control list (ACL)
- (C) Permissions boundary
- **(D) Trust policy** [CORRECT]
- (E) Correct option:
- (F) Trust policies define which principal entities (accounts, users, roles, and federated users) can assume the role. An IAM role is both an identity and a resource that supports resource-based policies. For this reason, you must attach both a trust policy and an identity-based policy to an IAM role. The IAM service supports only one type of resource-based policy called a role trust policy, which is attached to an IAM role.
- (G) Incorrect options:
- (H) AWS Organizations Service Control Policies (SCP) - If you enable all features of AWS organization, then you can apply service control policies (SCPs) to any or all of your accounts. SCPs are JSON policies that specify the maximum permissions for an organization or organizational unit (OU). The SCP limits permissions for entities in member accounts, including each AWS account root user. An explicit deny in any of these policies overrides the allow.
- (I) Access control list (ACL) - Access control lists (ACLs) are service policies that allow you to control which principals in another account can access a resource. ACLs cannot be used to control access for a principal within the same account. Amazon S3, AWS WAF, and Amazon VPC are examples of services that support ACLs.
- (J) Permissions boundary - AWS supports permissions boundaries for IAM entities (users or roles). A permissions boundary is an advanced feature for using a managed policy to set the maximum permissions that an identity-based policy can grant to an IAM entity. An entity's permissions boundary allows it to perform only the actions that are allowed by both its identity-based policies and its permissions boundaries.
- () References:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html#policies_resource-based
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
- () A company runs a popular dating website on the AWS Cloud. As a Solutions Architect, you've designed the architecture of the website to follow a serverless pattern on the AWS Cloud using Amazon API Gateway and AWS Lambda. The backend uses an Amazon RDS PostgreSQL database. Currently, the application uses a username and password combination to connect the AWS Lambda function to the Amazon RDS database.
- () You would like to improve the security at the authentication level by leveraging short-lived credentials. What will you choose? (Select two)
- () Correct selection
- () Attach an AWS Identity and Access Management (IAM) role to AWS Lambda
- () Use IAM authentication from AWS Lambda to Amazon RDS PostgreSQL
- () Deploy AWS Lambda in a VPC
- () Restrict the Amazon RDS database security group to the AWS Lambda's security group
- () Embed a credential rotation logic in the AWS Lambda, retrieving them from SSM
- () Correct options:
- () You can authenticate to your database instance using AWS Identity and Access Management (IAM) database authentication. IAM database authentication works with MySQL and PostgreSQL. With this authentication method, you don't need to use a password when you connect to a database instance. Instead, you use an authentication token.
- () An authentication token is a unique string of characters that Amazon RDS generates on request. Authentication tokens are generated using AWS Signature Version 4. Each token has a lifetime of 15 minutes. You don't need to store user credentials in the database, because authentication is managed externally using IAM. You can also still use standard database authentication.
- () IAM database authentication provides the following benefits: 1. Network traffic to and from the database is encrypted using Secure Sockets Layer (SSL). 2. You can use IAM to centrally manage access to your database resources, instead of managing access individually on each DB instance. 3. For applications running on Amazon EC2, you can use profile credentials specific to your Amazon EC2 instance to access your database instead of a password, for greater security.
- () AWS Systems Manager Parameter Store (aka SSM Parameter Store) provides secure, hierarchical storage for configuration data management and secrets management. You can store data such as passwords, database strings, Amazon EC2 instance IDs, Amazon Machine Image (AMI) IDs, and license codes as parameter values. You can store values as plain text or encrypted data.
- () Embed a credential rotation logic in the AWS Lambda, retrieving them from SSM - Retrieving credentials from SSM is overkill for the expected solution and hence this is not a correct option.
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.IAMDBAuth.html
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html
- () The engineering team at an e-commerce company has been tasked with migrating to a serverless architecture. The team wants to focus on the key points of consideration when using AWS Lambda as a backbone for this architecture.
- () As a Solutions Architect, which of the following options would you identify as correct for the given requirement? (Select three)
- () Serverless architecture and containers complement each other but you cannot package and deploy AWS Lambda functions as container images
- () AWS Lambda allocates compute power in proportion to the memory you allocate to your function. AWS, thus recommends to over provision your function time out settings for the proper performance of AWS Lambda functions
- () Since AWS Lambda functions can scale extremely quickly, it's a good idea to deploy a Amazon CloudWatch Alarm that notifies your team when function metrics such as ConcurrentExecutions or Invocations exceeds the expected threshold
- () By default, AWS Lambda functions always operate from an AWS-owned VPC and hence have access to any public internet address or public AWS APIs. Once an AWS Lambda function is VPC-enabled, it will need a route through a Network Address Translation gateway (NAT gateway) in a public subnet to access public resources
- () The bigger your deployment package, the slower your AWS Lambda function will cold-start. Hence, AWS suggests packaging dependencies as a separate package from the actual AWS Lambda package
- () If you intend to reuse code in more than one AWS Lambda function, you should consider creating an AWS Lambda Layer for the reusable code

**Answer:**
Correct Answer: **Trust policy**

---

## Question 76

**Q:** You would like to improve the security at the authentication level by leveraging short-lived credentials. What will you choose? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Attach an AWS Identity and Access Management (IAM) role to AWS Lambda
- (C) Use IAM authentication from AWS Lambda to Amazon RDS PostgreSQL
- (D) Deploy AWS Lambda in a VPC
- (E) Restrict the Amazon RDS database security group to the AWS Lambda's security group
- (F) Embed a credential rotation logic in the AWS Lambda, retrieving them from SSM
- (G) Correct options:
- (H) You can authenticate to your database instance using AWS Identity and Access Management (IAM) database authentication. IAM database authentication works with MySQL and PostgreSQL. With this authentication method, you don't need to use a password when you connect to a database instance. Instead, you use an authentication token.
- (I) An authentication token is a unique string of characters that Amazon RDS generates on request. Authentication tokens are generated using AWS Signature Version 4. Each token has a lifetime of 15 minutes. You don't need to store user credentials in the database, because authentication is managed externally using IAM. You can also still use standard database authentication.
- (J) IAM database authentication provides the following benefits: 1. Network traffic to and from the database is encrypted using Secure Sockets Layer (SSL). 2. You can use IAM to centrally manage access to your database resources, instead of managing access individually on each DB instance. 3. For applications running on Amazon EC2, you can use profile credentials specific to your Amazon EC2 instance to access your database instead of a password, for greater security.
- () Incorrect options:
- () AWS Systems Manager Parameter Store (aka SSM Parameter Store) provides secure, hierarchical storage for configuration data management and secrets management. You can store data such as passwords, database strings, Amazon EC2 instance IDs, Amazon Machine Image (AMI) IDs, and license codes as parameter values. You can store values as plain text or encrypted data.
- () Embed a credential rotation logic in the AWS Lambda, retrieving them from SSM - Retrieving credentials from SSM is overkill for the expected solution and hence this is not a correct option.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.IAMDBAuth.html
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html
- () The engineering team at an e-commerce company has been tasked with migrating to a serverless architecture. The team wants to focus on the key points of consideration when using AWS Lambda as a backbone for this architecture.
- () As a Solutions Architect, which of the following options would you identify as correct for the given requirement? (Select three)
- () Serverless architecture and containers complement each other but you cannot package and deploy AWS Lambda functions as container images
- () AWS Lambda allocates compute power in proportion to the memory you allocate to your function. AWS, thus recommends to over provision your function time out settings for the proper performance of AWS Lambda functions
- () Since AWS Lambda functions can scale extremely quickly, it's a good idea to deploy a Amazon CloudWatch Alarm that notifies your team when function metrics such as ConcurrentExecutions or Invocations exceeds the expected threshold
- () By default, AWS Lambda functions always operate from an AWS-owned VPC and hence have access to any public internet address or public AWS APIs. Once an AWS Lambda function is VPC-enabled, it will need a route through a Network Address Translation gateway (NAT gateway) in a public subnet to access public resources
- () The bigger your deployment package, the slower your AWS Lambda function will cold-start. Hence, AWS suggests packaging dependencies as a separate package from the actual AWS Lambda package
- () If you intend to reuse code in more than one AWS Lambda function, you should consider creating an AWS Lambda Layer for the reusable code
- () AWS Lambda functions always operate from an AWS-owned VPC. By default, your function has the full ability to make network requests to any public internet address — this includes access to any of the public AWS APIs. For example, your function can interact with AWS DynamoDB APIs to PutItem or Query for records. You should only enable your functions for VPC access when you need to interact with a private resource located in a private subnet. An Amazon RDS instance is a good example.
- () Once your function is VPC-enabled, all network traffic from your function is subject to the routing rules of your VPC/Subnet. If your function needs to interact with a public resource, you will need a route through a NAT gateway in a public subnet.
- () When to VPC-Enable an AWS Lambda Function:
- () via - https://aws.amazon.com/blogs/architecture/best-practices-for-developing-on-aws-lambda/
- () Since AWS Lambda functions can scale extremely quickly, this means you should have controls in place to notify you when you have a spike in concurrency. A good idea is to deploy an Amazon CloudWatch Alarm that notifies your team when function metrics such as ConcurrentExecutions or Invocations exceeds your threshold. You should create an AWS Budget so you can monitor costs on a daily basis.
- () You can configure your AWS Lambda function to pull in additional code and content in the form of layers. A layer is a ZIP archive that contains libraries, a custom runtime, or other dependencies. With layers, you can use libraries in your function without needing to include them in your deployment package. Layers let you keep your deployment package small, which makes development easier. A function can use up to 5 layers at a time.
- () You can create layers, or use layers published by AWS and other AWS customers. Layers support resource-based policies for granting layer usage permissions to specific AWS accounts, AWS Organizations, or all accounts. The total unzipped size of the function and all layers can't exceed the unzipped deployment package size limit of 250 megabytes.
- () The bigger your deployment package, the slower your AWS Lambda function will cold-start. Hence, AWS suggests packaging dependencies as a separate package from the actual AWS Lambda package - This statement is incorrect and acts as a distractor. All the dependencies are also packaged into the single Lambda deployment package.
- () Serverless architecture and containers complement each other but you cannot package and deploy AWS Lambda functions as container images - This statement is incorrect. You can now package and deploy AWS Lambda functions as container images.
- () https://aws.amazon.com/blogs/architecture/best-practices-for-developing-on-aws-lambda/
- () https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html
- () https://aws.amazon.com/blogs/aws/new-for-aws-lambda-container-image-support/

**Answer:**
Correct Answer: **Correct selection**

---

## Question 77

**Q:** As a Solutions Architect, which of the following options would you identify as correct for the given requirement? (Select three)

**Options:**
- **(A) Serverless architecture and containers complement each other but you cannot package and deploy AWS Lambda functions as container images** [CORRECT]
- (B) AWS Lambda allocates compute power in proportion to the memory you allocate to your function. AWS, thus recommends to over provision your function time out settings for the proper performance of AWS Lambda functions
- (C) Correct selection
- (D) Since AWS Lambda functions can scale extremely quickly, it's a good idea to deploy a Amazon CloudWatch Alarm that notifies your team when function metrics such as ConcurrentExecutions or Invocations exceeds the expected threshold
- (E) By default, AWS Lambda functions always operate from an AWS-owned VPC and hence have access to any public internet address or public AWS APIs. Once an AWS Lambda function is VPC-enabled, it will need a route through a Network Address Translation gateway (NAT gateway) in a public subnet to access public resources
- (F) The bigger your deployment package, the slower your AWS Lambda function will cold-start. Hence, AWS suggests packaging dependencies as a separate package from the actual AWS Lambda package
- (G) If you intend to reuse code in more than one AWS Lambda function, you should consider creating an AWS Lambda Layer for the reusable code
- (H) Correct options:
- (I) AWS Lambda functions always operate from an AWS-owned VPC. By default, your function has the full ability to make network requests to any public internet address — this includes access to any of the public AWS APIs. For example, your function can interact with AWS DynamoDB APIs to PutItem or Query for records. You should only enable your functions for VPC access when you need to interact with a private resource located in a private subnet. An Amazon RDS instance is a good example.
- (J) Once your function is VPC-enabled, all network traffic from your function is subject to the routing rules of your VPC/Subnet. If your function needs to interact with a public resource, you will need a route through a NAT gateway in a public subnet.
- () When to VPC-Enable an AWS Lambda Function:
- () via - https://aws.amazon.com/blogs/architecture/best-practices-for-developing-on-aws-lambda/
- () Since AWS Lambda functions can scale extremely quickly, this means you should have controls in place to notify you when you have a spike in concurrency. A good idea is to deploy an Amazon CloudWatch Alarm that notifies your team when function metrics such as ConcurrentExecutions or Invocations exceeds your threshold. You should create an AWS Budget so you can monitor costs on a daily basis.
- () You can configure your AWS Lambda function to pull in additional code and content in the form of layers. A layer is a ZIP archive that contains libraries, a custom runtime, or other dependencies. With layers, you can use libraries in your function without needing to include them in your deployment package. Layers let you keep your deployment package small, which makes development easier. A function can use up to 5 layers at a time.
- () You can create layers, or use layers published by AWS and other AWS customers. Layers support resource-based policies for granting layer usage permissions to specific AWS accounts, AWS Organizations, or all accounts. The total unzipped size of the function and all layers can't exceed the unzipped deployment package size limit of 250 megabytes.
- () Incorrect options:
- () The bigger your deployment package, the slower your AWS Lambda function will cold-start. Hence, AWS suggests packaging dependencies as a separate package from the actual AWS Lambda package - This statement is incorrect and acts as a distractor. All the dependencies are also packaged into the single Lambda deployment package.
- () Serverless architecture and containers complement each other but you cannot package and deploy AWS Lambda functions as container images - This statement is incorrect. You can now package and deploy AWS Lambda functions as container images.
- () References:
- () https://aws.amazon.com/blogs/architecture/best-practices-for-developing-on-aws-lambda/
- () https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html
- () https://aws.amazon.com/blogs/aws/new-for-aws-lambda-container-image-support/
- () A junior developer has downloaded a sample Amazon S3 bucket policy to make changes to it based on new company-wide access policies. He has requested your help in understanding this bucket policy.

**Answer:**
Correct Answer: **Serverless architecture and containers complement each other but you cannot package and deploy AWS Lambda functions as container images**

---

## Question 78

**Q:** As a Solutions Architect, which of the following would you identify as the correct description for the given policy?

**Options:**
- (A) : [
- (B) : {
- (C) It authorizes an IP address and a Classless Inter-Domain Routing (CIDR) to access the S3 bucket
- (D) It ensures Amazon EC2 instances that have inherited a security group can access the bucket
- (E) It ensures the Amazon S3 bucket is exposing an external IP within the Classless Inter-Domain Routing (CIDR) range specified, except one IP
- (F) It authorizes an entire Classless Inter-Domain Routing (CIDR) except one IP address to access the Amazon S3 bucket
- (G) Correct option:
- (H) Let's analyze the bucket policy one step at a time:
- (I)  (== 1 IP, 54.240.143.188/32), which means one IP address is explicitly blocked from accessing the examplebucket and its contents.
- (J) Example Bucket policies:
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html
- () Incorrect options:
- () These three options contradict the explanation provided above, so these options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html
- () A ride-sharing company wants to use an Amazon DynamoDB table for data storage. The table will not be used during the night hours whereas the read and write traffic will often be unpredictable during day hours. When traffic spikes occur they will happen very quickly.
- () Which of the following will you recommend as the best-fit solution?
- () Set up Amazon DynamoDB table with a global secondary index
- () Set up Amazon DynamoDB global table in the provisioned capacity mode
- () Set up Amazon DynamoDB table in the provisioned capacity mode with auto-scaling enabled
- **() Set up Amazon DynamoDB table in the on-demand capacity mode** [CORRECT]
- () Amazon DynamoDB has two read/write capacity modes for processing reads and writes on your tables:
- () On-demand
- () Provisioned (default, free-tier eligible)
- () Amazon DynamoDB on-demand is a flexible billing option capable of serving thousands of requests per second without capacity planning. DynamoDB on-demand offers pay-per-request pricing for read and write requests so that you pay only for what you use.
- () The on-demand mode is a good option if any of the following are true:
- () You create new tables with unknown workloads.
- () You have unpredictable application traffic.

**Answer:**
Correct Answer: **Set up Amazon DynamoDB table in the on-demand capacity mode**

---

## Question 79

**Q:** Which of the following will you recommend as the best-fit solution?

**Options:**
- (A) Set up Amazon DynamoDB table with a global secondary index
- (B) Set up Amazon DynamoDB global table in the provisioned capacity mode
- (C) Set up Amazon DynamoDB table in the provisioned capacity mode with auto-scaling enabled
- (D) Set up Amazon DynamoDB table in the on-demand capacity mode
- (E) Correct option:
- (F) Amazon DynamoDB has two read/write capacity modes for processing reads and writes on your tables:
- (G) On-demand
- (H) Provisioned (default, free-tier eligible)
- (I) Amazon DynamoDB on-demand is a flexible billing option capable of serving thousands of requests per second without capacity planning. DynamoDB on-demand offers pay-per-request pricing for read and write requests so that you pay only for what you use.
- (J) The on-demand mode is a good option if any of the following are true:
- () You create new tables with unknown workloads.
- () You have unpredictable application traffic.
- () You prefer the ease of paying for only what you use.
- () If you choose provisioned mode, you specify the number of reads and writes per second that you require for your application. You can use auto-scaling to adjust your table’s provisioned capacity automatically in response to traffic changes. This helps you govern your DynamoDB use to stay at or below a defined request rate to obtain cost predictability.
- () Provisioned mode is a good option if any of the following are true:
- () You have predictable application traffic.
- () You run applications whose traffic is consistent or ramps gradually.
- () You can forecast capacity requirements to control costs.
- () via - https://aws.amazon.com/blogs/database/amazon-dynamodb-auto-scaling-performance-and-cost-optimization-at-any-scale/
- () With on-demand, Amazon DynamoDB instantly allocates capacity as it is needed. There is no concept of provisioned capacity, and there is no delay waiting for Amazon CloudWatch thresholds or the subsequent table updates. On-demand is ideal for bursty, new, or unpredictable workloads whose traffic can spike in seconds or minutes, and when underprovisioned capacity would impact the user experience. On-demand is a perfect solution if your team is moving to a NoOps or serverless environment.
- () The given use case clearly states that when the traffic spikes occur they happen very quickly, thereby implying an unpredictable traffic pattern, therefore the on-demand capacity mode is the correct option for the given use case.
- () Incorrect options:
- () Set up Amazon DynamoDB table in the provisioned capacity mode with auto-scaling enabled - As mentioned in the explanation above, you should use the provisioned capacity mode (even with auto-scaling) only when you have predictable application traffic.
- ()  because queries on the index can span all of the data in the base table, across all partitions. A global secondary index is stored in its own partition space away from the base table and scales separately from the base table. GSI cannot be used to handle an unpredictable load on a DynamoDB table.
- () Set up Amazon DynamoDB global table in the provisioned capacity mode - Global tables build on the global Amazon DynamoDB footprint to provide you with a fully managed, multi-Region, and multi-active database that delivers fast, local, read and write performance for massively scaled, global applications. Global tables replicate your DynamoDB tables automatically across your choice of AWS Regions.
- () Global tables eliminate the difficult work of replicating data between Regions and resolving update conflicts, enabling you to focus on your application's business logic. In addition, global tables enable your applications to stay highly available even in the unlikely event of isolation or degradation of an entire Region.
- () Amazon DynamoDB global tables:
- () via - https://aws.amazon.com/dynamodb/global-tables/
- () Amazon DynamoDB global table cannot be used to handle an unpredictable load on a Amazon DynamoDB table.
- () References:
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadWriteCapacityMode.html
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/SecondaryIndexes.html
- () https://aws.amazon.com/blogs/database/amazon-dynamodb-auto-scaling-performance-and-cost-optimization-at-any-scale/
- () https://aws.amazon.com/dynamodb/global-tables/
- () A fintech startup hosts its real-time transaction metadata in Amazon DynamoDB tables. During a recent system maintenance event, a junior engineer accidentally deleted a production table, resulting in major service downtime and irreversible data loss. Leadership has mandated an immediate solution that prevents future data loss from human error, while requiring minimal ongoing maintenance or manual effort from the engineering team.
- () Which approach best addresses these requirements with the least operational overhead?
- **() Enable deletion protection on DynamoDB tables** [CORRECT]
- () Enable point-in-time recovery (PITR) on each DynamoDB table
- () Configure AWS CloudTrail to monitor DynamoDB API calls. Set up an Amazon EventBridge rule to detect DeleteTable events and trigger a Lambda function that recreates the deleted table using backup data stored in Amazon S3
- () Manually export each table as a full backup to Amazon S3 on a weekly basis. Use the DynamoDB export to S3 feature and rely on manual recovery if tables are deleted
- () Enable point-in-time recovery (PITR) on each DynamoDB table - PITR enables you to restore a table to any point in time within the last 35 days, but it does not prevent deletion. If a table is accidentally deleted, you can restore its data using PITR, but this still involves manual recovery operations and does not eliminate downtime or prevent disruption. While useful for data corruption recovery, PITR is reactive rather than preventive.

**Answer:**
Correct Answer: **Enable deletion protection on DynamoDB tables**

---

## Question 80

**Q:** Which approach best addresses these requirements with the least operational overhead?

**Options:**
- **(A) Enable deletion protection on DynamoDB tables** [CORRECT]
- (B) Enable point-in-time recovery (PITR) on each DynamoDB table
- (C) Configure AWS CloudTrail to monitor DynamoDB API calls. Set up an Amazon EventBridge rule to detect DeleteTable events and trigger a Lambda function that recreates the deleted table using backup data stored in Amazon S3
- (D) Manually export each table as a full backup to Amazon S3 on a weekly basis. Use the DynamoDB export to S3 feature and rely on manual recovery if tables are deleted
- (E) Correct option:
- (F) Incorrect options:
- (G) Enable point-in-time recovery (PITR) on each DynamoDB table - PITR enables you to restore a table to any point in time within the last 35 days, but it does not prevent deletion. If a table is accidentally deleted, you can restore its data using PITR, but this still involves manual recovery operations and does not eliminate downtime or prevent disruption. While useful for data corruption recovery, PITR is reactive rather than preventive.
- (H) Manually export each table as a full backup to Amazon S3 on a weekly basis. Use the DynamoDB export to S3 feature and rely on manual recovery if tables are deleted - Exporting backups to S3 manually on a schedule introduces operational overhead, and weekly frequency may lead to substantial data loss between backups. Additionally, recovery is a manual process, which is error-prone and time-consuming, especially in an incident response situation.
- (I) References:
- (J) https://aws.amazon.com/blogs/database/how-to-use-deletion-protection-to-enhance-your-amazon-dynamodb-table-protection-strategy/
- () https://aws.amazon.com/dynamodb/pitr/
- () The engineering team at a global e-commerce company is currently reviewing their disaster recovery strategy. The team has outlined that they need to be able to quickly recover their application stack with a Recovery Time Objective (RTO) of 5 minutes, in all of the AWS Regions that the application runs. The application stack currently takes over 45 minutes to install on a Linux system.

**Answer:**
Correct Answer: **Enable deletion protection on DynamoDB tables**

---

## Question 81

**Q:** As a Solutions architect, which of the following options would you recommend as the disaster recovery strategy?

**Options:**
- (A) Create an Amazon Machine Image (AMI) after installing the software and copy the AMI across all Regions. Use this Region-specific AMI to run the recovery process in the respective Regions
- (B) Use Amazon EC2 user data to speed up the installation process
- (C) Create an Amazon Machine Image (AMI) after installing the software and use this AMI to run the recovery process in other Regions
- (D) Store the installation files in Amazon S3 for quicker retrieval
- (E) Correct option:
- (F) An Amazon Machine Image (AMI) provides the information required to launch an instance. You must specify an AMI when you launch an instance. You can launch multiple instances from a single AMI when you need multiple instances with the same configuration. You can use different AMIs to launch instances when you need instances with different configurations.
- (G) For the current use case, you need to create an AMI such that the application stack is already set up. But AMIs are bound to the Region they are created in. So, you need to copy the AMI across Regions for disaster recovery readiness.
- (H) AWS does not copy launch permissions, user-defined tags, or Amazon S3 bucket permissions from the source AMI to the new AMI. After the copy operation is complete, you can apply launch permissions, user-defined tags, and Amazon S3 bucket permissions to the new AMI.
- (I) AMIs Cross-Region copying:
- (J) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html
- () Incorrect options:
- () Store the installation files in Amazon S3 for quicker retrieval - Amazon Simple Storage Service (Amazon S3) is an object storage service from AWS. It will not help with speeding up the installation since Amazon S3 is a storage service. You will still need an Amazon EC2 instance to have the necessary installation environment.
- () Use Amazon EC2 user data to speed up the installation process - User data of an Amazon EC2 instance can be used to perform common automated configuration tasks or run scripts after the instance starts. User data, cannot, however, be used to install the application. Amazon EC2 user data would not help as it would run the same installation script for the same duration of 45 minutes.
- () Create an Amazon Machine Image (AMI) after installing the software and use this AMI to run the recovery process in other Regions - As discussed above, AMIs are Region-specific and need to be copied to all Regions they are intended to be used in.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/CopyingAMIs.html
- () A genomics research firm is processing sporadic bursts of data-intensive workloads using Amazon EC2 instances. The shared storage must support unpredictable spikes in file operations, but the average daily throughput demand remains relatively low. The team has selected Amazon Elastic File System (EFS) for its scalability and wants to ensure optimal cost and performance during bursts without provisioning throughput manually.
- () Which approach should the team take to best meet these requirements?
- () Switch the EFS storage class to EFS One Zone to reduce cost, which will automatically enable burst throughput mode
- () Enable EFS burst throughput mode on the file system using the General Purpose performance mode and EFS Standard storage class
- () Enable EFS Infrequent Access (IA) storage class to reduce storage cost while continuing to benefit from burst throughput mode
- () Change the throughput mode to provisioned and configure the desired throughput value to support burst workloads
- () via - https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html
- () https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () An IT company runs a high-performance computing (HPC) workload on AWS. The workload requires high network throughput and low-latency network performance along with tightly coupled node-to-node communications. The Amazon EC2 instances are properly sized for compute and storage capacity and are launched using default options.
- () Which of the following solutions can be used to improve the performance of the workload?
- () Select dedicated instance tenancy while launching Amazon EC2 instances
- **() Select a cluster placement group while launching Amazon EC2 instances** [CORRECT]
- () Select the appropriate capacity reservation while launching Amazon EC2 instances
- () Select an Elastic Inference accelerator while launching Amazon EC2 instances

**Answer:**
Correct Answer: **Select a cluster placement group while launching Amazon EC2 instances**

---

## Question 82

**Q:** Which approach should the team take to best meet these requirements?

**Options:**
- (A) Switch the EFS storage class to EFS One Zone to reduce cost, which will automatically enable burst throughput mode
- (B) Enable EFS burst throughput mode on the file system using the General Purpose performance mode and EFS Standard storage class
- (C) Enable EFS Infrequent Access (IA) storage class to reduce storage cost while continuing to benefit from burst throughput mode
- (D) Change the throughput mode to provisioned and configure the desired throughput value to support burst workloads
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/efs/latest/ug/performance.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html
- (J) https://docs.aws.amazon.com/efs/latest/ug/performance.html
- () An IT company runs a high-performance computing (HPC) workload on AWS. The workload requires high network throughput and low-latency network performance along with tightly coupled node-to-node communications. The Amazon EC2 instances are properly sized for compute and storage capacity and are launched using default options.
- () Which of the following solutions can be used to improve the performance of the workload?
- () Select dedicated instance tenancy while launching Amazon EC2 instances
- **() Select a cluster placement group while launching Amazon EC2 instances** [CORRECT]
- () Select the appropriate capacity reservation while launching Amazon EC2 instances
- () Select an Elastic Inference accelerator while launching Amazon EC2 instances
- () When you launch a new Amazon EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload.
- () Cluster placement group packs instances close together inside an Availability Zone (AZ). This strategy enables workloads to achieve the low-latency network performance necessary for tightly coupled node-to-node communication that is typical of HPC applications.
- () More on Cluster placement groups:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () Select dedicated instance tenancy while launching Amazon EC2 instances - Dedicated Instances are Amazon EC2 instances that run in a VPC on hardware that's dedicated to a single customer. Your Dedicated instances are physically isolated at the host hardware level from instances that belong to other AWS accounts. Dedicated Instances are useful from a compliance perspective, but are not meant for performance improvement.
- () Select an Elastic Inference accelerator while launching Amazon EC2 instances - Amazon Elastic Inference accelerators are GPU-powered hardware devices that are designed to work with any Amazon EC2 instance, Amazon Sagemaker instance, or Amazon ECS task to accelerate deep learning inference workloads at a low cost. They are for workloads that need deep learning. Also, AWS PrivateLink VPC Endpoints are needed for Elastic Inference accelerators, which makes it unsuitable for the current scenario.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () A company wants to adopt a hybrid cloud infrastructure where it uses some AWS services such as Amazon S3 alongside its on-premises data center. The company wants a dedicated private connection between the on-premise data center and AWS. In case of failures though, the company needs to guarantee uptime and is willing to use the public internet for an encrypted connection.
- () What do you recommend? (Select two)
- () Use AWS Direct Connect connection as a backup connection
- () Correct selection
- () Use AWS Direct Connect connection as a primary connection
- () Use Egress Only Internet Gateway as a backup connection
- () Use AWS Site-to-Site VPN as a primary connection
- () Use AWS Site-to-Site VPN as a backup connection
- () Correct options:

**Answer:**
Correct Answer: **Select a cluster placement group while launching Amazon EC2 instances**

---

## Question 83

**Q:** Which of the following solutions can be used to improve the performance of the workload?

**Options:**
- (A) Select dedicated instance tenancy while launching Amazon EC2 instances
- (B) Select a cluster placement group while launching Amazon EC2 instances
- (C) Select the appropriate capacity reservation while launching Amazon EC2 instances
- (D) Select an Elastic Inference accelerator while launching Amazon EC2 instances
- (E) Correct option:
- (F) When you launch a new Amazon EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload.
- (G) Cluster placement group packs instances close together inside an Availability Zone (AZ). This strategy enables workloads to achieve the low-latency network performance necessary for tightly coupled node-to-node communication that is typical of HPC applications.
- (H) More on Cluster placement groups:
- (I) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- (J) Incorrect options:
- () Select dedicated instance tenancy while launching Amazon EC2 instances - Dedicated Instances are Amazon EC2 instances that run in a VPC on hardware that's dedicated to a single customer. Your Dedicated instances are physically isolated at the host hardware level from instances that belong to other AWS accounts. Dedicated Instances are useful from a compliance perspective, but are not meant for performance improvement.
- () Select an Elastic Inference accelerator while launching Amazon EC2 instances - Amazon Elastic Inference accelerators are GPU-powered hardware devices that are designed to work with any Amazon EC2 instance, Amazon Sagemaker instance, or Amazon ECS task to accelerate deep learning inference workloads at a low cost. They are for workloads that need deep learning. Also, AWS PrivateLink VPC Endpoints are needed for Elastic Inference accelerators, which makes it unsuitable for the current scenario.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () A company wants to adopt a hybrid cloud infrastructure where it uses some AWS services such as Amazon S3 alongside its on-premises data center. The company wants a dedicated private connection between the on-premise data center and AWS. In case of failures though, the company needs to guarantee uptime and is willing to use the public internet for an encrypted connection.
- () What do you recommend? (Select two)
- () Use AWS Direct Connect connection as a backup connection
- () Correct selection
- () Use AWS Direct Connect connection as a primary connection
- () Use Egress Only Internet Gateway as a backup connection
- () Use AWS Site-to-Site VPN as a primary connection
- () Use AWS Site-to-Site VPN as a backup connection
- () Correct options:
- () AWS Direct Connect lets you establish a dedicated network connection between your network and one of the AWS Direct Connect locations. Using industry-standard 802.1q VLANs, this dedicated connection can be partitioned into multiple virtual interfaces. AWS Direct Connect does not involve the Internet; instead, it uses dedicated, private network connections between your intranet and Amazon VPC.
- () AWS Direct Connect as a primary connection guarantees great performance and security (as the connection is private). Using Direct Connect as a backup solution would work but probably carries a risk it would fail as well. As we don't mind going over the public internet (which is reliable, but less secure as connections are going over the public route), we should use a Site to Site VPN which offers an encrypted connection to handle failover scenarios.
- () Use Egress Only Internet Gateway as a backup connection - An Egress-Only Internet Gateway is a horizontally scaled, redundant, and highly available VPC component that allows outbound communication over IPv6 from instances in your VPC to the Internet, and prevents the Internet from initiating an IPv6 connection with your instances. Egress-Only Internet Gateway cannot be used to connect on-premises data centers to AWS Cloud.
- () Use AWS Site-to-Site VPN as a primary connection - AWS Site-to-Site VPN as a primary connection is not advisable since the use of internet-based connection is only for failover scenarios, as stated in the problem.
- () Use AWS Direct Connect connection as a backup connection - AWS Direct Connect connection is a highly secure, physical connection. It is also a costly solution and hence does not make much sense to set up the connection and keep it only as a backup.
- () References:
- () https://aws.amazon.com/directconnect/
- () https://aws.amazon.com/vpn/
- () A development team has configured Elastic Load Balancing for host-based routing. The idea is to support multiple subdomains and different top-level domains.
- () The rule *.example.com matches which of the following?
- () example.test.com
- **() test.example.com** [CORRECT]
- () example.com

**Answer:**
Correct Answer: **test.example.com**

---

## Question 84

**Q:** The rule *.example.com matches which of the following?

**Options:**
- (A) example.test.com
- (B) test.example.com
- (C) example.com
- (D) Correct option:
- (E) You can use host conditions to define rules that route requests based on the hostname in the host header (also known as host-based routing). This enables you to support multiple subdomains and different top-level domains using a single load balancer.
- (F) A hostname is not case-sensitive, can be up to 128 characters in length, and can contain any of the following characters: 1. A–Z, a–z, 0–9 2. - . 3. * (matches 0 or more characters) 4. ? (matches exactly 1 character)
- (G)  character.
- (H) The rule *.example.com matches test.example.com but doesn't match example.com.
- (I) Incorrect options:
- (J) These three options contradict the explanation provided above, so these options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html
- () A company wants to grant access to an Amazon S3 bucket to users in its own AWS account as well as to users in another AWS account. Which of the following options can be used to meet this requirement?
- () Use a user policy to grant permission to users in its account as well as to users in another account
- **() Use a bucket policy to grant permission to users in its account as well as to users in another account** [CORRECT]
- () Use either a bucket policy or a user policy to grant permission to users in its account as well as to users in another account
- () Use permissions boundary to grant permission to users in its account as well as to users in another account
- () A bucket policy is a type of resource-based policy that can be used to grant permissions to the principal that is specified in the policy. Principals can be in the same account as the resource or in other accounts. For cross-account permissions to other AWS accounts or users in another account, you must use a bucket policy.
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html
- () If an AWS account that owns a bucket wants to grant permission to users in its own AWS account, it can use either a bucket policy or a user policy. The user policies are for managing permissions for users in their own AWS account and NOT for users in other AWS accounts. Therefore both these options are incorrect.
- () Use permissions boundary to grant permission to users in its account as well as to users in another account - Use a managed policy as the permissions boundary for an IAM entity (user or role). That policy defines the maximum permissions that the identity-based policies can grant to an entity, but does not grant permissions, so this option is not correct for the given use case.
- () via - https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () A Pharmaceuticals company is looking for a simple solution to connect its VPCs and on-premises networks through a central hub.

**Answer:**
Correct Answer: **Use a bucket policy to grant permission to users in its account as well as to users in another account**

---

## Question 85

**Q:** A hostname is not case-sensitive, can be up to 128 characters in length, and can contain any of the following characters: 1. A–Z, a–z, 0–9 2. - . 3. * (matches 0 or more characters) 4. ? (matches exactly 1 character)

**Options:**
- (A)  character.
- (B) The rule *.example.com matches test.example.com but doesn't match example.com.
- (C) Incorrect options:
- (D) example.com
- (E) example.test.com
- (F) These three options contradict the explanation provided above, so these options are incorrect.
- (G) Reference:
- (H) https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html
- (I) A company wants to grant access to an Amazon S3 bucket to users in its own AWS account as well as to users in another AWS account. Which of the following options can be used to meet this requirement?
- (J) Use a user policy to grant permission to users in its account as well as to users in another account
- **() Use a bucket policy to grant permission to users in its account as well as to users in another account** [CORRECT]
- () Use either a bucket policy or a user policy to grant permission to users in its account as well as to users in another account
- () Use permissions boundary to grant permission to users in its account as well as to users in another account
- () Correct option:
- () A bucket policy is a type of resource-based policy that can be used to grant permissions to the principal that is specified in the policy. Principals can be in the same account as the resource or in other accounts. For cross-account permissions to other AWS accounts or users in another account, you must use a bucket policy.
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html
- () If an AWS account that owns a bucket wants to grant permission to users in its own AWS account, it can use either a bucket policy or a user policy. The user policies are for managing permissions for users in their own AWS account and NOT for users in other AWS accounts. Therefore both these options are incorrect.
- () Use permissions boundary to grant permission to users in its account as well as to users in another account - Use a managed policy as the permissions boundary for an IAM entity (user or role). That policy defines the maximum permissions that the identity-based policies can grant to an entity, but does not grant permissions, so this option is not correct for the given use case.
- () via - https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () A Pharmaceuticals company is looking for a simple solution to connect its VPCs and on-premises networks through a central hub.

**Answer:**
Correct Answer: **Use a bucket policy to grant permission to users in its account as well as to users in another account**

---

## Question 86

**Q:** A company wants to grant access to an Amazon S3 bucket to users in its own AWS account as well as to users in another AWS account. Which of the following options can be used to meet this requirement?

**Options:**
- (A) Use a user policy to grant permission to users in its account as well as to users in another account
- **(B) Use a bucket policy to grant permission to users in its account as well as to users in another account** [CORRECT]
- (C) Use either a bucket policy or a user policy to grant permission to users in its account as well as to users in another account
- (D) Use permissions boundary to grant permission to users in its account as well as to users in another account
- (E) Correct option:
- (F) A bucket policy is a type of resource-based policy that can be used to grant permissions to the principal that is specified in the policy. Principals can be in the same account as the resource or in other accounts. For cross-account permissions to other AWS accounts or users in another account, you must use a bucket policy.
- (G) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html
- (H) Incorrect options:
- (I) If an AWS account that owns a bucket wants to grant permission to users in its own AWS account, it can use either a bucket policy or a user policy. The user policies are for managing permissions for users in their own AWS account and NOT for users in other AWS accounts. Therefore both these options are incorrect.
- (J) Use permissions boundary to grant permission to users in its account as well as to users in another account - Use a managed policy as the permissions boundary for an IAM entity (user or role). That policy defines the maximum permissions that the identity-based policies can grant to an entity, but does not grant permissions, so this option is not correct for the given use case.
- () via - https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () A Pharmaceuticals company is looking for a simple solution to connect its VPCs and on-premises networks through a central hub.

**Answer:**
Correct Answer: **Use a bucket policy to grant permission to users in its account as well as to users in another account**

---

## Question 87

**Q:** As a Solutions Architect, which of the following would you suggest as the solution that requires the LEAST operational overhead?

**Options:**
- **(A) Use AWS Transit Gateway to connect the Amazon VPCs to the on-premises networks** [CORRECT]
- (B) Partially meshed VPC peering can be used to connect the Amazon VPCs to the on-premises networks
- (C) Use Transit VPC Solution to connect the Amazon VPCs to the on-premises networks
- (D) Fully meshed VPC peering can be used to connect the Amazon VPCs to the on-premises networks
- (E) Correct option:
- (F) AWS Transit Gateway:
- (G) via - https://aws.amazon.com/transit-gateway/
- (H) Incorrect options:
- (I) Transit VPC:
- (J) The simplest way to connect two VPCs is to use VPC Peering. In this setup, a connection enables full bidirectional connectivity between the VPCs. This peering connection is used to route traffic between the VPCs. VPCs across accounts and AWS Regions can also be peered together. VPC peering only incurs costs for traffic traveling over the connection (there is no hourly infrastructure fee).
- () Network setup using VPC Peering:
- () via - https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/vpc-peering.html
- () You cannot use VPC Peering to establish on-premises connectivity with AWS Cloud, so both these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/transit-gateway-vs-transit-vpc.html
- () https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/vpc-peering.html
- () A company has noticed that its Amazon EBS Elastic Volume (io1) accounts for 90% of the cost and the remaining 10% cost can be attributed to the Amazon EC2 instance. The Amazon CloudWatch metrics report that both the Amazon EC2 instance and the Amazon EBS volume are under-utilized. The Amazon CloudWatch metrics also show that the Amazon EBS volume has occasional I/O bursts. The entire infrastructure is managed by AWS CloudFormation.

**Answer:**
Correct Answer: **Use AWS Transit Gateway to connect the Amazon VPCs to the on-premises networks**

---

## Question 88

**Q:** As a Solutions Architect, what do you propose to reduce the costs?

**Options:**
- **(A) Convert the Amazon EC2 instance EBS volume to gp2** [CORRECT]
- (B) Change the Amazon EC2 instance type to something much smaller
- (C) Keep the Amazon EBS volume to io1 and reduce the IOPS
- (D) Don't use a AWS CloudFormation template to create the database as the AWS CloudFormation service incurs greater service charges
- (E) Correct option:
- (F) Amazon EBS provides the various volume types, that differ in performance characteristics and price so that you can tailor your storage performance and cost to the needs of your applications. The volumes types fall into two categories:
- (G) SSD-backed volumes optimized for transactional workloads involving frequent read/write operations with small I/O size, where the dominant performance attribute is IOPS.
- (H) HDD-backed volumes optimized for large streaming workloads where throughput (measured in MiB/s) is a better performance measure than IOPS
- (I) Provisioned IOPS SSD (io1) volumes are designed to meet the needs of I/O-intensive workloads, particularly database workloads, that are sensitive to storage performance and consistency. Unlike gp2, which uses a bucket and credit model to calculate performance, an io1 volume allows you to specify a consistent IOPS rate when you create the volume, and Amazon EBS delivers the provisioned performance 99.9 percent of the time.
- (J) Therefore, gp2 is the right choice as it is more cost-effective than io1, and it also allows a burst in performance when needed.
- () Incorrect options:
- () Keep the Amazon EBS volume to io1 and reduce the IOPS - Keeping the Amazon EBS volume to io1 and reducing the IOPS may interfere with the burst of performance we need, so this option is ruled out.
- () Change the Amazon EC2 instance type to something much smaller - Changing the Amazon EC2 instance type to something much smaller won't affect 90% of the costs that are incurred, therefore this option is also incorrect.
- () Don't use a AWS CloudFormation template to create the database as the AWS CloudFormation service incurs greater service charges - This statement is incorrect as AWS CloudFormation is a free service to use. The resources that are invoked by CloudFormation are charged as per their utilization rates, but using AWS CloudFormation will not cost anything.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html#EBSVolumeTypes_gp2
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html#EBSVolumeTypes_piops
- () The engineering team at a leading e-commerce company is anticipating a surge in the traffic because of a flash sale planned for the weekend. You have estimated the web traffic to be 10x. The content of your website is highly dynamic and changes very often.

**Answer:**
Correct Answer: **Convert the Amazon EC2 instance EBS volume to gp2**

---

## Question 89

**Q:** As a Solutions Architect, which of the following options would you recommend to make sure your infrastructure scales for that day?

**Options:**
- (A) Use an Amazon Route 53 Multi Value record
- (B) Use an Auto Scaling Group
- (C) Use an Amazon CloudFront distribution in front of your website
- (D) Deploy the website on Amazon S3
- (E) Correct option:
- (F) An Auto Scaling group (ASG) contains a collection of Amazon EC2 instances that are treated as a logical grouping for automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
- (G) The size of an Auto Scaling group depends on the number of instances that you set as the desired capacity. You can adjust its size to meet demand, either manually or by using automatic scaling.
- (H) An Auto Scaling group starts by launching enough instances to meet its desired capacity. It maintains this number of instances by performing periodic health checks on the instances in the group. The Auto Scaling group continues to maintain a fixed number of instances even if an instance becomes unhealthy. If an instance becomes unhealthy, the group terminates the unhealthy instance and launches another instance to replace it.
- (I) Auto Scaling group is the correct answer here.
- (J) Incorrect option:
- () Amazon CloudFront is not a good solution here as the content is highly dynamic, and Amazon CloudFront will cache things.
- () Dynamic applications cannot be deployed to Amazon S3. This option has been added as a distractor.
- () Use an Amazon Route 53 Multi Value record - Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. Use Multi Value answer routing policy when you want Route 53 to respond to DNS queries with up to eight healthy records selected at random. Amazon Route 53 does not help in scaling your application. This option has been added as a distractor.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroup.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html
- () You are working as a Solutions Architect for a photo processing company that has a proprietary algorithm to compress an image without any loss in quality. Because of the efficiency of the algorithm, your clients are willing to wait for a response that carries their compressed images back. You also want to process these jobs asynchronously and scale quickly, to cater to the high demand. Additionally, you also want the job to be retried in case of failures.
- () Which combination of choices do you recommend to minimize cost and comply with the requirements? (Select two)
- () Correct selection
- () Amazon EC2 Spot Instances
- () Amazon EC2 On-Demand Instances
- () Amazon Simple Notification Service (Amazon SNS)
- () Amazon EC2 Reserved Instances (RIs)
- () Amazon Simple Queue Service (Amazon SQS)
- () Correct options:
- () To process these jobs, due to the unpredictable nature of their volume, and the desire to save on costs, spot Instances are recommended as compared to on-demand instances. As spot instances are cheaper than reserved instances and do not require long term commitment, spot instances are a better fit for the given use-case.
- () Amazon EC2 Instance purchasing options:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
- () Amazon Simple Queue Service (Amazon SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS offers two types of message queues. Standard queues offer maximum throughput, best-effort ordering, and at-least-once delivery. Amazon SQS FIFO (First-In-First-out) queues are designed to guarantee that messages are processed exactly once, in the exact order that they are sent.
- () Amazon SQS will allow you to buffer the image compression requests and process them asynchronously. It also has a direct built-in mechanism for retries and scales seamlessly.
- () Incorrect options:
- () Amazon Simple Notification Service (Amazon SNS) - Amazon Simple Notification Service (Amazon SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging. SNS is not the right fit for this use-case, since its not a queuing mechanism.
- () Amazon EC2 Reserved Instances (RIs) - Reserved instances (RIs) reduce your Amazon EC2 costs by making a commitment to a consistent instance configuration, including instance type and Region, for a term of 1 or 3 years. For the given use case, this kind of annual commitment might not be a desirable option.
- () https://aws.amazon.com/sqs/
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () As a solutions architect, you have created a solution that utilizes an Application Load Balancer with stickiness and an Auto Scaling Group (ASG). The Auto Scaling Group spans across 2 Availability Zones (AZs). AZ-A has 3 Amazon EC2 instances and AZ-B has 4 Amazon EC2 instances. The Auto Scaling Group is about to go into a scale-in event due to the triggering of a Amazon CloudWatch alarm.
- () What will happen under the default Auto Scaling Group configuration?
- **() The instance with the oldest launch template or launch configuration will be terminated in AZ-B** [CORRECT]

**Answer:**
Correct Answer: **The instance with the oldest launch template or launch configuration will be terminated in AZ-B**

---

## Question 90

**Q:** Which combination of choices do you recommend to minimize cost and comply with the requirements? (Select two)

**Options:**
- (A) Correct selection
- (B) Amazon EC2 Spot Instances
- (C) Amazon EC2 On-Demand Instances
- (D) Amazon Simple Notification Service (Amazon SNS)
- (E) Amazon EC2 Reserved Instances (RIs)
- (F) Amazon Simple Queue Service (Amazon SQS)
- (G) Correct options:
- (H) To process these jobs, due to the unpredictable nature of their volume, and the desire to save on costs, spot Instances are recommended as compared to on-demand instances. As spot instances are cheaper than reserved instances and do not require long term commitment, spot instances are a better fit for the given use-case.
- (I) Amazon EC2 Instance purchasing options:
- (J) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
- () Amazon Simple Queue Service (Amazon SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. SQS offers two types of message queues. Standard queues offer maximum throughput, best-effort ordering, and at-least-once delivery. Amazon SQS FIFO (First-In-First-out) queues are designed to guarantee that messages are processed exactly once, in the exact order that they are sent.
- () Amazon SQS will allow you to buffer the image compression requests and process them asynchronously. It also has a direct built-in mechanism for retries and scales seamlessly.
- () Incorrect options:
- () Amazon Simple Notification Service (Amazon SNS) - Amazon Simple Notification Service (Amazon SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging. SNS is not the right fit for this use-case, since its not a queuing mechanism.
- () Amazon EC2 Reserved Instances (RIs) - Reserved instances (RIs) reduce your Amazon EC2 costs by making a commitment to a consistent instance configuration, including instance type and Region, for a term of 1 or 3 years. For the given use case, this kind of annual commitment might not be a desirable option.
- () References:
- () https://aws.amazon.com/sqs/
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () As a solutions architect, you have created a solution that utilizes an Application Load Balancer with stickiness and an Auto Scaling Group (ASG). The Auto Scaling Group spans across 2 Availability Zones (AZs). AZ-A has 3 Amazon EC2 instances and AZ-B has 4 Amazon EC2 instances. The Auto Scaling Group is about to go into a scale-in event due to the triggering of a Amazon CloudWatch alarm.
- () What will happen under the default Auto Scaling Group configuration?
- **() The instance with the oldest launch template or launch configuration will be terminated in AZ-B** [CORRECT]
- () A random instance in the AZ-A will be terminated
- () A random instance will be terminated in AZ-B
- () An instance in the AZ-A will be created
- () Correct option:
- () Amazon EC2 Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. You create collections of Amazon EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes below this size.
- () With each Auto Scaling group, you can control when it adds instances (referred to as scaling out) or removes instances (referred to as scaling in) from your network architecture.
- () The default termination policy is designed to help ensure that your instances span Availability Zones evenly for high availability. The default policy is kept generic and flexible to cover a range of scenarios.
- () Per the given use-case, AZs will be balanced first, then the instance with the oldest launch template or launch configuration within the applicable AZ (AZ-B) will be terminated.
- () Default Termination policy:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () These three options contradict the details provided in the explanation above. Hence these are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () A Big Data processing company has created a distributed data processing framework that performs best if the network performance between the processing machines is high. The application has to be deployed on AWS, and the company is only looking at performance as the key measure.

**Answer:**
Correct Answer: **The instance with the oldest launch template or launch configuration will be terminated in AZ-B**

---

## Question 91

**Q:** What will happen under the default Auto Scaling Group configuration?

**Options:**
- **(A) The instance with the oldest launch template or launch configuration will be terminated in AZ-B** [CORRECT]
- (B) A random instance in the AZ-A will be terminated
- (C) A random instance will be terminated in AZ-B
- (D) An instance in the AZ-A will be created
- (E) Correct option:
- (F) Amazon EC2 Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. You create collections of Amazon EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes below this size.
- (G) With each Auto Scaling group, you can control when it adds instances (referred to as scaling out) or removes instances (referred to as scaling in) from your network architecture.
- (H) The default termination policy is designed to help ensure that your instances span Availability Zones evenly for high availability. The default policy is kept generic and flexible to cover a range of scenarios.
- (I) Per the given use-case, AZs will be balanced first, then the instance with the oldest launch template or launch configuration within the applicable AZ (AZ-B) will be terminated.
- (J) Default Termination policy:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () Incorrect options:
- () These three options contradict the details provided in the explanation above. Hence these are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-instance-termination.html
- () A Big Data processing company has created a distributed data processing framework that performs best if the network performance between the processing machines is high. The application has to be deployed on AWS, and the company is only looking at performance as the key measure.

**Answer:**
Correct Answer: **The instance with the oldest launch template or launch configuration will be terminated in AZ-B**

---

## Question 92

**Q:** As a Solutions Architect, which deployment do you recommend?

**Options:**
- (A) Optimize the Amazon EC2 kernel using EC2 User Data
- (B) Use a Spread placement group
- **(C) Use a Cluster placement group** [CORRECT]
- (D) Use Spot Instances
- (E) Correct option:
- (F) When you launch a new Amazon EC2 instance, the EC2 service attempts to place the instance in such a way that all of your instances are spread out across underlying hardware to minimize correlated failures. You can use placement groups to influence the placement of a group of interdependent instances to meet the needs of your workload. Depending on the type of workload, you can create a placement group using one of the following placement strategies:
- (G) Cluster – packs instances close together inside an Availability Zone (AZ). This strategy enables workloads to achieve the low-latency network performance necessary for tightly-coupled node-to-node communication that is typical of HPC applications.
- (H) Partition – spreads your instances across logical partitions such that groups of instances in one partition do not share the underlying hardware with groups of instances in different partitions. This strategy is typically used by large distributed and replicated workloads, such as Hadoop, Cassandra, and Kafka.
- (I) Spread – strictly places a small group of instances across distinct underlying hardware to reduce correlated failures.
- (J) There is no charge for creating a placement group.
- () A cluster placement group is a logical grouping of instances within a single Availability Zone (AZ). A cluster placement group can span peered VPCs in the same Region. Instances in the same cluster placement group enjoy a higher per-flow throughput limit of up to 10 Gbps for TCP/IP traffic and are placed in the same high-bisection bandwidth segment of the network.
- () Cluster placement groups are recommended for applications that benefit from low network latency, high network throughput, or both. They are also recommended when the majority of the network traffic is between the instances in the group. To provide the lowest latency and the highest packet-per-second network performance for your placement group, choose an instance type that supports enhanced networking.
- () Image of Cluster placement group:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () Image of Partition placement group:
- () Image of Spread placement group:
- () Incorrect options:
- () Use Spot Instances - A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused Amazon EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted. Since performance is the key criteria, this is not the right choice.
- () Optimize the Amazon EC2 kernel using EC2 User Data - Optimizing the Amazon EC2 kernel won't help with network performance as it's bounded by the EC2 instance type mainly. Therefore, this option is incorrect.
- () Use a Spread placement group - A spread placement group is a group of instances that are each placed on distinct racks, with each rack having its own network and power source. The instances are placed across distinct underlying hardware to reduce correlated failures. A spread placement group can span multiple Availability Zones (AZs) in the same Region. You can have a maximum of seven running instances per Availability Zone (AZ) per group.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html
- () An e-commerce company has copied 1 petabyte of data from its on-premises data center to an Amazon S3 bucket in the us-west-1 Region using an AWS Direct Connect link. The company now wants to set up a one-time copy of the data to another Amazon S3 bucket in the us-east-1 Region. The on-premises data center does not allow the use of AWS Snowball.
- () As a Solutions Architect, which of the following options can be used to accomplish this goal? (Select two)
- () Set up Amazon S3 Transfer Acceleration (Amazon S3TA) to copy objects across Amazon S3 buckets in different Regions using S3 console
- () Use AWS Snowball Edge device to copy the data from one Region to another Region
- () Correct selection
- () Set up Amazon S3 batch replication to copy objects across Amazon S3 buckets in another Region using S3 console and then delete the replication configuration
- () Copy data from the source bucket to the destination bucket using the aws S3 sync command
- () Copy data from the source Amazon S3 bucket to a target Amazon S3 bucket using the S3 console
- () Correct options:
- () You can use the command like so:
- () aws s3 sync s3://DOC-EXAMPLE-BUCKET-SOURCE s3://DOC-EXAMPLE-BUCKET-TARGET
- () Amazon S3 Batch Replication provides you a way to replicate objects that existed before a replication configuration was in place, objects that have previously been replicated, and objects that have failed replication. This is done through the use of a Batch Operations job.
- () If you want to enable live replication for existing objects for your bucket, you must contact AWS Support and raise a support ticket. This is required to ensure that replication is configured correctly.
- () Set up Amazon S3 Transfer Acceleration (Amazon S3TA) to copy objects across Amazon S3 buckets in different Regions using S3 console - Amazon S3 Transfer Acceleration (Amazon S3TA) is a bucket-level feature that enables fast, easy, and secure transfers of files over long distances between your client and an Amazon S3 bucket. You cannot use Transfer Acceleration to copy objects across Amazon S3 buckets in different Regions using Amazon S3 console.

**Answer:**
Correct Answer: **Use a Cluster placement group**

---

## Question 93

**Q:** As a Solutions Architect, which of the following options can be used to accomplish this goal? (Select two)

**Options:**
- **(A) Set up Amazon S3 Transfer Acceleration (Amazon S3TA) to copy objects across Amazon S3 buckets in different Regions using S3 console** [CORRECT]
- (B) Use AWS Snowball Edge device to copy the data from one Region to another Region
- (C) Correct selection
- (D) Set up Amazon S3 batch replication to copy objects across Amazon S3 buckets in another Region using S3 console and then delete the replication configuration
- (E) Copy data from the source bucket to the destination bucket using the aws S3 sync command
- (F) Copy data from the source Amazon S3 bucket to a target Amazon S3 bucket using the S3 console
- (G) Correct options:
- (H) You can use the command like so:
- (I) aws s3 sync s3://DOC-EXAMPLE-BUCKET-SOURCE s3://DOC-EXAMPLE-BUCKET-TARGET
- (J) Amazon S3 Batch Replication provides you a way to replicate objects that existed before a replication configuration was in place, objects that have previously been replicated, and objects that have failed replication. This is done through the use of a Batch Operations job.
- () If you want to enable live replication for existing objects for your bucket, you must contact AWS Support and raise a support ticket. This is required to ensure that replication is configured correctly.
- () Incorrect options:
- () Set up Amazon S3 Transfer Acceleration (Amazon S3TA) to copy objects across Amazon S3 buckets in different Regions using S3 console - Amazon S3 Transfer Acceleration (Amazon S3TA) is a bucket-level feature that enables fast, easy, and secure transfers of files over long distances between your client and an Amazon S3 bucket. You cannot use Transfer Acceleration to copy objects across Amazon S3 buckets in different Regions using Amazon S3 console.
- () References:
- () https://aws.amazon.com/premiumsupport/knowledge-center/move-objects-s3-bucket/
- () https://aws.amazon.com/snowball/faqs/
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html
- () A financial services firm has traditionally operated with an on-premise data center and would like to create a disaster recovery strategy leveraging the AWS Cloud.

**Answer:**
Correct Answer: **Set up Amazon S3 Transfer Acceleration (Amazon S3TA) to copy objects across Amazon S3 buckets in different Regions using S3 console**

---

## Question 94

**Q:** As a Solutions Architect, you would like to ensure that a scaled-down version of a fully functional environment is always running in the AWS cloud, and in case of a disaster, the recovery time is kept to a minimum. Which disaster recovery strategy is that?

**Options:**
- **(A) Warm Standby** [CORRECT]
- (B) Multi Site
- (C) Pilot Light
- (D) Backup and Restore
- (E) Correct option:
- (F) The term warm standby is used to describe a DR scenario in which a scaled-down version of a fully functional environment is always running in the cloud. A warm standby solution extends the pilot light elements and preparation. It further decreases the recovery time because some services are always running. By identifying your business-critical systems, you can fully duplicate these systems on AWS and have them always on.
- (G) Incorrect options:
- (H) Multi Site - A multi-site solution runs in AWS as well as on your existing on-site infrastructure, in an active-active configuration. The data replication method that you employ will be determined by the recovery point that you choose.
- (I) References:
- (J) https://d1.awsstatic.com/whitepapers/aws-disaster-recovery.pdf
- () https://d1.awsstatic.com/asset-repository/products/CloudEndure/CloudEndure_Affordable_Enterprise-Grade_Disaster_Recovery_Using_AWS.pdf
- () You are working for a software as a service (SaaS) company as a solutions architect and help design solutions for the company's customers. One of the customers is a bank and has a requirement to whitelist a public IP when the bank is accessing external services across the internet.

**Answer:**
Correct Answer: **Warm Standby**

---

## Question 95

**Q:** Which architectural choice do you recommend to maintain high availability, support scaling-up to 10 instances and comply with the bank's requirements?

**Options:**
- (A) Use an Auto Scaling Group with Dynamic Elastic IPs attachment
- (B) Use a Network Load Balancer with an Auto Scaling Group
- (C) Use an Application Load Balancer with an Auto Scaling Group
- (D) Use a Classic Load Balancer with an Auto Scaling Group
- (E) Correct option:
- (F) Network Load Balancers expose a fixed IP to the public web, therefore allowing your application to be predictably reached using this IP, while allowing you to scale your application behind the Network Load Balancer using an ASG.
- (G) Incorrect options:
- (H) Classic Load Balancers and Application Load Balancers use the private IP addresses associated with their Elastic network interfaces as the source IP address for requests forwarded to your web servers.
- (I) These IP addresses can be used for various purposes, such as allowing the load balancer traffic on the web servers and for request processing. It's a best practice to use security group referencing on the web servers for whitelisting load balancer traffic from Classic Load Balancers or Application Load Balancers.
- (J) However, because Network Load Balancers don't support security groups, based on the target group configurations, the IP addresses of the clients or the private IP addresses associated with the Network Load Balancers must be allowed on the web server's security group.
- () Use a Classic Load Balancer with an Auto Scaling Group - Classic Load Balancer provides basic load balancing across multiple Amazon EC2 instances and operates at both the request level and connection level. Classic Load Balancer is intended for applications that were built within the Amazon EC2-Classic network.
- () Application and Classic Load Balancers expose a fixed DNS (=URL) rather than the IP address. So these are incorrect options for the given use-case.
- ()  has been added as a distractor. ASG does not have a dynamic Elastic IPs attachment feature.
- () References:
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () https://aws.amazon.com/premiumsupport/knowledge-center/elb-find-load-balancer-IP/
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-internet-facing-load-balancers.html
- () You started a new job as a solutions architect at a company that has both AWS experts and people learning AWS. Recently, a developer misconfigured a newly created Amazon RDS database which resulted in a production outage.
- () How can you ensure that Amazon RDS specific best practices are incorporated into a reusable infrastructure template to be used by all your AWS users?
- () Attach an IAM policy to interns preventing them from creating an Amazon RDS database
- () Create an AWS Lambda function which sends emails when it finds misconfigured Amazon RDS databases
- () Store your recommendations in a custom AWS Trusted Advisor rule
- **() Use AWS CloudFormation to manage Amazon RDS databases** [CORRECT]
- () AWS CloudFormation provides a common language for you to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts. This gives you a single source of truth for your AWS and third-party resources.
- () AWS CloudFormation allows you to keep your infrastructure as code and re-use the best practices around your company for configuration parameters. Therefore, this is the correct option for the given use-case.
- () Create an AWS Lambda function which sends emails when it finds misconfigured Amazon RDS databases - Using an AWS Lambda function to scan for a misconfigured Amazon RDS database is a reactive mechanism. It does not help in creating reusable infrastructure templates.
- () Attach an IAM policy to interns preventing them from creating an Amazon RDS database - Using an IAM policy to prevent interns from creating an Amazon RDS database does not solve the problem of allowing any user to create resources by leveraging reusable infrastructure templates. So, this option is ruled out.
- () https://aws.amazon.com/premiumsupport/technology/trusted-advisor/
- () https://aws.amazon.com/cloudformation/
- () A Big Data analytics company writes data and log files in Amazon S3 buckets. The company now wants to stream the existing data files as well as any ongoing file updates from Amazon S3 to Amazon Kinesis Data Streams.

**Answer:**
Correct Answer: **Use AWS CloudFormation to manage Amazon RDS databases**

---

## Question 96

**Q:** How can you ensure that Amazon RDS specific best practices are incorporated into a reusable infrastructure template to be used by all your AWS users?

**Options:**
- (A) Attach an IAM policy to interns preventing them from creating an Amazon RDS database
- (B) Create an AWS Lambda function which sends emails when it finds misconfigured Amazon RDS databases
- (C) Store your recommendations in a custom AWS Trusted Advisor rule
- **(D) Use AWS CloudFormation to manage Amazon RDS databases** [CORRECT]
- (E) Correct option:
- (F) AWS CloudFormation provides a common language for you to model and provision AWS and third-party application resources in your cloud environment. AWS CloudFormation allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all regions and accounts. This gives you a single source of truth for your AWS and third-party resources.
- (G) AWS CloudFormation allows you to keep your infrastructure as code and re-use the best practices around your company for configuration parameters. Therefore, this is the correct option for the given use-case.
- (H) Incorrect options:
- (I) Create an AWS Lambda function which sends emails when it finds misconfigured Amazon RDS databases - Using an AWS Lambda function to scan for a misconfigured Amazon RDS database is a reactive mechanism. It does not help in creating reusable infrastructure templates.
- (J) Attach an IAM policy to interns preventing them from creating an Amazon RDS database - Using an IAM policy to prevent interns from creating an Amazon RDS database does not solve the problem of allowing any user to create resources by leveraging reusable infrastructure templates. So, this option is ruled out.
- () References:
- () https://aws.amazon.com/premiumsupport/technology/trusted-advisor/
- () https://aws.amazon.com/cloudformation/
- () A Big Data analytics company writes data and log files in Amazon S3 buckets. The company now wants to stream the existing data files as well as any ongoing file updates from Amazon S3 to Amazon Kinesis Data Streams.

**Answer:**
Correct Answer: **Use AWS CloudFormation to manage Amazon RDS databases**

---

## Question 97

**Q:** As a Solutions Architect, which of the following would you suggest as the fastest possible way of building a solution for this requirement?

**Options:**
- (A) Leverage Amazon S3 event notification to trigger an AWS Lambda function for the file create event. The AWS Lambda function will then send the necessary data to Amazon Kinesis Data Streams
- (B) Amazon S3 bucket actions can be directly configured to write data into Amazon Simple Notification Service (Amazon SNS). Amazon SNS can then be used to send the updates to Amazon Kinesis Data Streams
- (C) Configure Amazon EventBridge events for the bucket actions on Amazon S3. An AWS Lambda function can then be triggered from the Amazon EventBridge event that will send the necessary data to Amazon Kinesis Data Streams
- (D) Leverage AWS Database Migration Service (AWS DMS) as a bridge between Amazon S3 and Amazon Kinesis Data Streams
- (E) Correct option:
- (F) You can achieve this by using AWS Database Migration Service (AWS DMS). AWS DMS enables you to seamlessly migrate data from supported sources to relational databases, data warehouses, streaming platforms, and other data stores in AWS cloud.
- (G) AWS DMS supports Amazon S3 as the source and Kinesis as the target, so data stored in an S3 bucket is streamed to Kinesis. Several consumers, such as AWS Lambda, Amazon Kinesis Data Firehose, Amazon Kinesis Data Analytics, and the Kinesis Consumer Library (KCL), can consume the data concurrently to perform real-time analytics on the dataset. Each AWS service in this architecture can scale independently as needed.
- (H) Architecture of the proposed solution:
- (I) via - https://aws.amazon.com/blogs/big-data/streaming-data-from-amazon-s3-to-amazon-kinesis-data-streams-using-aws-dms/
- (J) Incorrect options:
- () Leverage Amazon S3 event notification to trigger an AWS Lambda function for the file create event. The AWS Lambda function will then send the necessary data to Amazon Kinesis Data Streams - Using AWS Lambda functions would require significant custom development to write the data into Amazon Kinesis Data Streams, so this option is not the right fit.
- () Amazon S3 bucket actions can be directly configured to write data into Amazon Simple Notification Service (Amazon SNS). Amazon SNS can then be used to send the updates to Amazon Kinesis Data Streams - Amazon S3 cannot directly write data into Amazon SNS, although it can certainly use Amazon S3 event notifications to send an event to Amazon SNS. Also, Amazon SNS cannot directly send messages to Amazon Kinesis Data Streams. So this option is incorrect.
- () Reference:
- () https://aws.amazon.com/blogs/big-data/streaming-data-from-amazon-s3-to-amazon-kinesis-data-streams-using-aws-dms/
- () Dump14
- () Which solution best meets these requirements?
- () Use AWS Storage Gateway in file gateway mode to expose an NFS file share. Deploy AWS Transfer Family with a public endpoint and map user identities using IAM roles. Configure IP allow lists using AWS WAF
- () Use Amazon S3 with server-side encryption enabled. Create an AWS Transfer Family SFTP endpoint with a VPC endpoint in a private subnet. Restrict access to known IPs using security group rules. Manage user-level permissions using IAM role-based access mappings
- **() Use Amazon EFS with encryption enabled. Create an AWS Transfer Family SFTP endpoint in a VPC with Elastic IP addresses. Restrict access using a security group that allows traffic only from known IPs. Manage user access using POSIX identity mappings and IAM policies** [CORRECT]
- () Use Amazon FSx for Lustre as the backend storage. Create an AWS Transfer Family SFTP service with a public endpoint. Configure IAM policies to manage user access and attach a security group that restricts access to trusted IP addresses
- () References:
- () https://docs.aws.amazon.com/transfer/latest/userguide/what-is-aws-transfer-family.html
- () https://docs.aws.amazon.com/filegateway/latest/files3/what-is-file-s3.html
- () https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html
- () A retail company wants to establish encrypted network connectivity between its on-premises data center and AWS Cloud. The company wants to get the solution up and running in the fastest possible time and it should also support encryption in transit.

**Answer:**
Correct Answer: **Use Amazon EFS with encryption enabled. Create an AWS Transfer Family SFTP endpoint in a VPC with Elastic IP addresses. Restrict access using a security group that allows traffic only from known IPs. Manage user access using POSIX identity mappings and IAM policies**

---

## Question 98

**Q:** As a solutions architect, which of the following solutions would you suggest to the company?

**Options:**
- (A) Use AWS Direct Connect to establish encrypted network connectivity between the on-premises data center and AWS Cloud
- **(B) Use AWS Site-to-Site VPN to establish encrypted network connectivity between the on-premises data center and AWS Cloud** [CORRECT]
- (C) Use AWS Secrets Manager to establish encrypted network connectivity between the on-premises data center and AWS Cloud
- (D) Use AWS Data Sync to establish encrypted network connectivity between the on-premises data center and AWS Cloud
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/vpn/latest/s2svpn/internetwork-traffic-privacy.html
- (I) https://docs.aws.amazon.com/directconnect/latest/UserGuide/encryption-in-transit.html
- (J) Reporters at a news agency upload/download video files (about 500 megabytes each) to/from an Amazon S3 bucket as part of their daily work. As the agency has started offices in remote locations, it has resulted in poor latency for uploading and accessing data to/from the given Amazon S3 bucket. The agency wants to continue using a serverless storage solution such as Amazon S3 but wants to improve the performance.
- () As a solutions architect, which of the following solutions do you propose to address this issue? (Select two)
- () Create new Amazon S3 buckets in every region where the agency has a remote office, so that each office can maintain its storage for the media assets
- () Move Amazon S3 data into Amazon Elastic File System (Amazon EFS) created in a US region, connect to Amazon EFS file system from Amazon EC2 instances in other AWS regions using an inter-region VPC peering connection
- () Correct selection
- () Use Amazon CloudFront distribution with origin as the Amazon S3 bucket. This would speed up uploads as well as downloads for the video files
- () Spin up Amazon EC2 instances in each region where the agency has a remote office. Create a daily job to transfer Amazon S3 data into Amazon EBS volumes attached to the Amazon EC2 instances
- () Enable Amazon S3 Transfer Acceleration (Amazon S3TA) for the Amazon S3 bucket. This would speed up uploads as well as downloads for the video files
- () Correct options:
- () Following is a good reference blog for a deep-dive:
- () https://aws.amazon.com/blogs/aws/amazon-cloudfront-content-uploads-post-put-other-methods/
- () Amazon S3 Transfer Acceleration (Amazon S3TA) can speed up content transfers to and from Amazon S3 by as much as 50-500% for long-distance transfer of larger objects. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path. So this option is also correct.
- () Amazon S3TA:
- () via - https://aws.amazon.com/s3/transfer-acceleration/
- () Create new Amazon S3 buckets in every region where the agency has a remote office, so that each office can maintain its storage for the media assets - Creating new Amazon S3 buckets in every region is not an option, since the agency maintains centralized storage. Hence this option is incorrect.
- () Both these options using Amazon EC2 instances are not correct for the given use-case, as the agency wants a serverless storage solution.
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html
- () https://aws.amazon.com/s3/transfer-acceleration/
- () A company's cloud architect has set up a solution that uses Amazon Route 53 to configure the DNS records for the primary website with the domain pointing to the Application Load Balancer (ALB). The company wants a solution where users will be directed to a static error page, configured as a backup, in case of unavailability of the primary website.

**Answer:**
Correct Answer: **Use AWS Site-to-Site VPN to establish encrypted network connectivity between the on-premises data center and AWS Cloud**

---

## Question 99

**Q:** As a solutions architect, which of the following solutions do you propose to address this issue? (Select two)

**Options:**
- **(A) Create new Amazon S3 buckets in every region where the agency has a remote office, so that each office can maintain its storage for the media assets** [CORRECT]
- (B) Move Amazon S3 data into Amazon Elastic File System (Amazon EFS) created in a US region, connect to Amazon EFS file system from Amazon EC2 instances in other AWS regions using an inter-region VPC peering connection
- (C) Correct selection
- (D) Use Amazon CloudFront distribution with origin as the Amazon S3 bucket. This would speed up uploads as well as downloads for the video files
- (E) Spin up Amazon EC2 instances in each region where the agency has a remote office. Create a daily job to transfer Amazon S3 data into Amazon EBS volumes attached to the Amazon EC2 instances
- (F) Enable Amazon S3 Transfer Acceleration (Amazon S3TA) for the Amazon S3 bucket. This would speed up uploads as well as downloads for the video files
- (G) Correct options:
- (H) Following is a good reference blog for a deep-dive:
- (I) https://aws.amazon.com/blogs/aws/amazon-cloudfront-content-uploads-post-put-other-methods/
- (J) Amazon S3 Transfer Acceleration (Amazon S3TA) can speed up content transfers to and from Amazon S3 by as much as 50-500% for long-distance transfer of larger objects. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path. So this option is also correct.
- () Amazon S3TA:
- () via - https://aws.amazon.com/s3/transfer-acceleration/
- () Incorrect options:
- () Create new Amazon S3 buckets in every region where the agency has a remote office, so that each office can maintain its storage for the media assets - Creating new Amazon S3 buckets in every region is not an option, since the agency maintains centralized storage. Hence this option is incorrect.
- () Both these options using Amazon EC2 instances are not correct for the given use-case, as the agency wants a serverless storage solution.
- () References:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html
- () https://aws.amazon.com/s3/transfer-acceleration/
- () A company's cloud architect has set up a solution that uses Amazon Route 53 to configure the DNS records for the primary website with the domain pointing to the Application Load Balancer (ALB). The company wants a solution where users will be directed to a static error page, configured as a backup, in case of unavailability of the primary website.

**Answer:**
Correct Answer: **Create new Amazon S3 buckets in every region where the agency has a remote office, so that each office can maintain its storage for the media assets**

---

## Question 100

**Q:** Which configuration will meet the company's requirements, while keeping the changes to a bare minimum?

**Options:**
- (A) Use Amazon Route 53 Latency-based routing. Create a latency record to point to the Amazon S3 bucket that holds the error page to be displayed
- (B) Set up Amazon Route 53 active-active type of failover routing policy. If Amazon Route 53 health check determines the Application Load Balancer endpoint as unhealthy, the traffic will be diverted to a static error page, hosted on Amazon S3 bucket
- (C) Use Amazon Route 53 Weighted routing to give minimum weight to Amazon S3 bucket that holds the error page to be displayed. In case of primary failure, the requests get routed to the error page
- **(D) Set up Amazon Route 53 active-passive type of failover routing policy. If Amazon Route 53 health check determines the Application Load Balancer endpoint as unhealthy, the traffic will be diverted to a static error page, hosted on Amazon S3 bucket** [CORRECT]
- (E) Correct option:
- (F) Use an active-passive failover configuration when you want a primary resource or group of resources to be available the majority of the time and you want a secondary resource or group of resources to be on standby in case all the primary resources become unavailable. When responding to queries, Amazon Route 53 includes only healthy primary resources. If all the primary resources are unhealthy, Route 53 begins to include only the healthy secondary resources in response to DNS queries.
- (G) Incorrect options:
- (H) Use Amazon Route 53 Latency-based routing. Create a latency record to point to the Amazon S3 bucket that holds the error page to be displayed - If your application is hosted in multiple AWS Regions, you can improve performance for your users by serving their requests from the AWS Region that provides the lowest latency - this is Latency-based routing and is not helpful for the current use case.
- (I) References:
- (J) https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-types.html#dns-failover-types-active-passive
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-latency
- () A company needs a massive PostgreSQL database and the engineering team would like to retain control over managing the patches, version upgrades for the database, and consistent performance with high IOPS. The team wants to install the database on an Amazon EC2 instance with the optimal storage type on the attached Amazon EBS volume.

**Answer:**
Correct Answer: **Set up Amazon Route 53 active-passive type of failover routing policy. If Amazon Route 53 health check determines the Application Load Balancer endpoint as unhealthy, the traffic will be diverted to a static error page, hosted on Amazon S3 bucket**

---

## Question 101

**Q:** As a solutions architect, which of the following configurations would you suggest to the engineering team?

**Options:**
- (A) Amazon EC2 with Amazon EBS volume of General Purpose SSD (gp2) type
- (B) Amazon EC2 with Amazon EBS volume of Throughput Optimized HDD (st1) type
- **(C) Amazon EC2 with Amazon EBS volume of Provisioned IOPS SSD (io1) type** [CORRECT]
- (D) Amazon EC2 with Amazon EBS volume of cold HDD (sc1) type
- (E) Correct option:
- (F) Amazon EBS provides the following volume types, which differ in performance characteristics and price so that you can tailor your storage performance and cost to the needs of your applications.
- (G) The volumes types fall into two categories:
- (H) SSD-backed volumes optimized for transactional workloads involving frequent read/write operations with small I/O size, where the dominant performance attribute is IOPS
- (I) HDD-backed volumes optimized for large streaming workloads where throughput (measured in MiB/s) is a better performance measure than IOPS
- (J) Provision IOPS type supports critical business applications that require sustained IOPS performance, or more than 16,000 IOPS or 250 MiB/s of throughput per volume. Examples are large database workloads, such as: MongoDB Cassandra Microsoft SQL Server MySQL PostgreSQL Oracle
- () Therefore, Amazon EC2 with Amazon EBS volume of Provisioned IOPS SSD (io1) type is the right fit for the given use-case.
- () Please see this detailed overview of the volume types for Amazon EBS volumes.
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () Incorrect options:
- () Per the explanation in the detailed overview provided above, these three options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () A financial services company runs its flagship web application on AWS. The application serves thousands of users during peak hours. The company needs a scalable near-real-time solution to share hundreds of thousands of financial transactions with multiple internal applications. The solution should also remove sensitive details from the transactions before storing the cleansed transactions in a document database for low-latency retrieval.

**Answer:**
Correct Answer: **Amazon EC2 with Amazon EBS volume of Provisioned IOPS SSD (io1) type**

---

## Question 102

**Q:** Which of the following options represent the root cause for this issue?

**Options:**
- (A) The database user credentials (username and password) configured for the application are incorrect
- (B) The security group configuration for the application servers does not have the correct rules to allow inbound connections from the database instance
- (C) The security group configuration for the database instance does not have the correct rules to allow inbound connections from the application servers
- (D) The database user credentials (username and password) configured for the application do not have the required privilege for the given database
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html
- (G) Incorrect options:
- (H) The security group configuration for the application servers does not have the correct rules to allow inbound connections from the database instance - As mentioned in the explanation above, the application servers don't need inbound connections from the database instance, rather the database instance needs the correct inbound rule with application servers' security group as the source.
- (I)  error.
- (J) References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html
- () https://aws.amazon.com/premiumsupport/knowledge-center/rds-cannot-connect/
- () A medium-sized business has a taxi dispatch application deployed on an Amazon EC2 instance. Because of an unknown bug, the application causes the instance to freeze regularly. Then, the instance has to be manually restarted via the AWS management console.
- () Which of the following is the MOST cost-optimal and resource-efficient way to implement an automated solution until a permanent fix is delivered by the development team?
- () Setup an Amazon CloudWatch alarm to monitor the health status of the instance. In case of an Instance Health Check failure, Amazon CloudWatch Alarm can publish to an Amazon Simple Notification Service (Amazon SNS) event which can then trigger an AWS lambda function. The AWS lambda function can use Amazon EC2 API to reboot the instance
- () Use Amazon EventBridge events to trigger an AWS Lambda function to check the instance status every 5 minutes. In the case of Instance Health Check failure, the AWS lambda function can use Amazon EC2 API to reboot the instance
- () Setup an Amazon CloudWatch alarm to monitor the health status of the instance. In case of an Instance Health Check failure, an EC2 Reboot CloudWatch Alarm Action can be used to reboot the instance
- () Use Amazon EventBridge events to trigger an AWS Lambda function to reboot the instance status every 5 minutes
- () Using Amazon CloudWatch alarm actions, you can create alarms that automatically stop, terminate, reboot, or recover your Amazon EC2 instances. You can use the stop or terminate actions to help you save money when you no longer need an instance to be running. You can use the reboot and recover actions to automatically reboot those instances or recover them onto new hardware if a system impairment occurs.
- () You can create an Amazon CloudWatch alarm that monitors an Amazon EC2 instance and automatically reboots the instance. The reboot alarm action is recommended for Instance Health Check failures (as opposed to the recover alarm action, which is suited for System Health Check failures).
- () Using Amazon EventBridge event or Amazon CloudWatch alarm to trigger an AWS lambda function, directly or indirectly, is wasteful of resources. You should just use the EC2 Reboot CloudWatch Alarm Action to reboot the instance. So all the options that trigger the AWS lambda function are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/UsingAlarmActions.html
- () Which solution should a solutions architect recommend to meet these requirements?
- () Create Amazon EBS-backed Amazon Machine Images (AMIs) from the production EC2 instances. Launch new EC2 instances in the test environment from the AMIs. Use Amazon EC2 instance store volumes for temporary simulation data
- **() Take snapshots of the production EBS volumes. Enable EBS fast snapshot restore on the snapshots. Create new EBS volumes from the snapshots and attach them to EC2 instances in the test environment** [CORRECT]
- () Create new EBS volumes in the test environment and use AWS Backup to perform a backup job of the production volumes. Restore the backup directly to the test EBS volumes to begin simulations
- () Use Amazon EBS io2 volumes with Multi-Attach enabled. Attach the same production EBS volumes to both the production and test EC2 instances simultaneously to avoid cloning delays and ensure high IOPS performance
- () This solution uses EBS fast snapshot restore (FSR), which allows immediate, full-performance access to new EBS volumes created from snapshots—eliminating the usual initialization delay. Creating volumes from snapshots ensures that test data is logically cloned without impacting the source, and the FSR feature guarantees the I/O performance required by the analytics workloads. This method is efficient, scalable, and preserves isolation between test and production environments.

**Answer:**
Correct Answer: **Take snapshots of the production EBS volumes. Enable EBS fast snapshot restore on the snapshots. Create new EBS volumes from the snapshots and attach them to EC2 instances in the test environment**

---

## Question 103

**Q:** Which of the following is the MOST cost-optimal and resource-efficient way to implement an automated solution until a permanent fix is delivered by the development team?

**Options:**
- (A) Setup an Amazon CloudWatch alarm to monitor the health status of the instance. In case of an Instance Health Check failure, Amazon CloudWatch Alarm can publish to an Amazon Simple Notification Service (Amazon SNS) event which can then trigger an AWS lambda function. The AWS lambda function can use Amazon EC2 API to reboot the instance
- (B) Use Amazon EventBridge events to trigger an AWS Lambda function to check the instance status every 5 minutes. In the case of Instance Health Check failure, the AWS lambda function can use Amazon EC2 API to reboot the instance
- (C) Setup an Amazon CloudWatch alarm to monitor the health status of the instance. In case of an Instance Health Check failure, an EC2 Reboot CloudWatch Alarm Action can be used to reboot the instance
- (D) Use Amazon EventBridge events to trigger an AWS Lambda function to reboot the instance status every 5 minutes
- (E) Correct option:
- (F) Using Amazon CloudWatch alarm actions, you can create alarms that automatically stop, terminate, reboot, or recover your Amazon EC2 instances. You can use the stop or terminate actions to help you save money when you no longer need an instance to be running. You can use the reboot and recover actions to automatically reboot those instances or recover them onto new hardware if a system impairment occurs.
- (G) You can create an Amazon CloudWatch alarm that monitors an Amazon EC2 instance and automatically reboots the instance. The reboot alarm action is recommended for Instance Health Check failures (as opposed to the recover alarm action, which is suited for System Health Check failures).
- (H) Incorrect options:
- (I) Using Amazon EventBridge event or Amazon CloudWatch alarm to trigger an AWS lambda function, directly or indirectly, is wasteful of resources. You should just use the EC2 Reboot CloudWatch Alarm Action to reboot the instance. So all the options that trigger the AWS lambda function are incorrect.
- (J) Reference:
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/UsingAlarmActions.html
- () Which solution should a solutions architect recommend to meet these requirements?
- () Create Amazon EBS-backed Amazon Machine Images (AMIs) from the production EC2 instances. Launch new EC2 instances in the test environment from the AMIs. Use Amazon EC2 instance store volumes for temporary simulation data
- () Take snapshots of the production EBS volumes. Enable EBS fast snapshot restore on the snapshots. Create new EBS volumes from the snapshots and attach them to EC2 instances in the test environment
- () Create new EBS volumes in the test environment and use AWS Backup to perform a backup job of the production volumes. Restore the backup directly to the test EBS volumes to begin simulations
- () Use Amazon EBS io2 volumes with Multi-Attach enabled. Attach the same production EBS volumes to both the production and test EC2 instances simultaneously to avoid cloning delays and ensure high IOPS performance
- () This solution uses EBS fast snapshot restore (FSR), which allows immediate, full-performance access to new EBS volumes created from snapshots—eliminating the usual initialization delay. Creating volumes from snapshots ensures that test data is logically cloned without impacting the source, and the FSR feature guarantees the I/O performance required by the analytics workloads. This method is efficient, scalable, and preserves isolation between test and production environments.
- () References:
- () https://docs.aws.amazon.com/ebs/latest/userguide/ebs-fast-snapshot-restore.html
- () https://docs.aws.amazon.com/ebs/latest/userguide/ebs-volumes-multi.html
- () Which solution will fulfill these requirements?
- **() Create a gateway VPC endpoint for Amazon S3 in the VPC. Ensure that the EC2 instance’s subnet route table is updated to route S3 traffic through the endpoint. Confirm that appropriate IAM policies are in place to permit access via the VPC endpoint** [CORRECT]
- () Create an S3 access point within the same Region and attach a policy that grants the EC2 instance access. Update the application to use the access point alias to upload data
- () Set up a NAT gateway in the public subnet and modify the route table of the EC2 instance's subnet to direct Amazon S3 traffic through the NAT gateway
- () Provision a dedicated AWS Direct Connect link to route traffic from the VPC to Amazon S3 privately
- () There is no additional charge for using gateway endpoints. Amazon S3 supports both gateway endpoints and interface endpoints. With a gateway endpoint, you can access Amazon S3 from your VPC, without requiring an internet gateway or NAT device for your VPC, and with no additional cost. However, gateway endpoints do not allow access from on-premises networks, from peered VPCs in other AWS Regions, or through a transit gateway.
- () Set up a NAT gateway in the public subnet and modify the route table of the EC2 instance's subnet to direct Amazon S3 traffic through the NAT gateway - Although NAT gateways can route traffic to the internet, they do not provide private access to S3. Traffic sent through a NAT gateway to S3 still uses public endpoints and incurs data transfer charges. This does not satisfy the requirement to avoid public endpoint usage.
- () Provision a dedicated AWS Direct Connect link to route traffic from the VPC to Amazon S3 privately - Direct Connect is ideal for high-throughput, low-latency, hybrid workloads where traffic flows from on-premises to AWS. However, it is unnecessary for this use case, which involves internal traffic between EC2 and S3 within AWS.
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-s3.html

**Answer:**
Correct Answer: **Create a gateway VPC endpoint for Amazon S3 in the VPC. Ensure that the EC2 instance’s subnet route table is updated to route S3 traffic through the endpoint. Confirm that appropriate IAM policies are in place to permit access via the VPC endpoint**

---

## Question 104

**Q:** Which solution should a solutions architect recommend to meet these requirements?

**Options:**
- (A) Create Amazon EBS-backed Amazon Machine Images (AMIs) from the production EC2 instances. Launch new EC2 instances in the test environment from the AMIs. Use Amazon EC2 instance store volumes for temporary simulation data
- (B) Take snapshots of the production EBS volumes. Enable EBS fast snapshot restore on the snapshots. Create new EBS volumes from the snapshots and attach them to EC2 instances in the test environment
- (C) Create new EBS volumes in the test environment and use AWS Backup to perform a backup job of the production volumes. Restore the backup directly to the test EBS volumes to begin simulations
- (D) Use Amazon EBS io2 volumes with Multi-Attach enabled. Attach the same production EBS volumes to both the production and test EC2 instances simultaneously to avoid cloning delays and ensure high IOPS performance
- (E) Correct option:
- (F) This solution uses EBS fast snapshot restore (FSR), which allows immediate, full-performance access to new EBS volumes created from snapshots—eliminating the usual initialization delay. Creating volumes from snapshots ensures that test data is logically cloned without impacting the source, and the FSR feature guarantees the I/O performance required by the analytics workloads. This method is efficient, scalable, and preserves isolation between test and production environments.
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/ebs/latest/userguide/ebs-fast-snapshot-restore.html
- (J) https://docs.aws.amazon.com/ebs/latest/userguide/ebs-volumes-multi.html
- () Which solution will fulfill these requirements?
- () Create a gateway VPC endpoint for Amazon S3 in the VPC. Ensure that the EC2 instance’s subnet route table is updated to route S3 traffic through the endpoint. Confirm that appropriate IAM policies are in place to permit access via the VPC endpoint
- () Create an S3 access point within the same Region and attach a policy that grants the EC2 instance access. Update the application to use the access point alias to upload data
- () Set up a NAT gateway in the public subnet and modify the route table of the EC2 instance's subnet to direct Amazon S3 traffic through the NAT gateway
- () Provision a dedicated AWS Direct Connect link to route traffic from the VPC to Amazon S3 privately
- () There is no additional charge for using gateway endpoints. Amazon S3 supports both gateway endpoints and interface endpoints. With a gateway endpoint, you can access Amazon S3 from your VPC, without requiring an internet gateway or NAT device for your VPC, and with no additional cost. However, gateway endpoints do not allow access from on-premises networks, from peered VPCs in other AWS Regions, or through a transit gateway.
- () Set up a NAT gateway in the public subnet and modify the route table of the EC2 instance's subnet to direct Amazon S3 traffic through the NAT gateway - Although NAT gateways can route traffic to the internet, they do not provide private access to S3. Traffic sent through a NAT gateway to S3 still uses public endpoints and incurs data transfer charges. This does not satisfy the requirement to avoid public endpoint usage.
- () Provision a dedicated AWS Direct Connect link to route traffic from the VPC to Amazon S3 privately - Direct Connect is ideal for high-throughput, low-latency, hybrid workloads where traffic flows from on-premises to AWS. However, it is unnecessary for this use case, which involves internal traffic between EC2 and S3 within AWS.
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-s3.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html
- () A fintech company currently operates a real-time search and analytics platform on-premises. This platform ingests streaming data from multiple data-producing systems and provides immediate search capabilities and interactive visualizations for end users. As part of its cloud migration strategy, the company wants to rearchitect the solution using AWS-native services.
- () Which of the following represents the most efficient solution?
- () Use AWS Glue streaming ETL to process data streams and load the data into Amazon Redshift. Use Amazon Redshift’s full-text search capabilities for querying. Use Amazon QuickSight for data visualizations
- **() Ingest and process the streaming data using Amazon Kinesis Data Streams, then index the data with Amazon OpenSearch Service for real-time search capabilities. Use Amazon QuickSight to build interactive dashboards and visualizations based on the indexed data** [CORRECT]
- () Deploy Amazon EC2 instances to handle the ingestion and processing of streaming data, storing the results in Amazon S3. Utilize Amazon Athena to search the stored data, and use Amazon Managed Grafana to generate dashboards and visual insights
- () Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate to ingest the data into Amazon DynamoDB to facilitate full text search. Use Amazon CloudWatch to create dashboards and query the data
- () This solution leverages Amazon Kinesis Data Streams for high-throughput, low-latency stream ingestion, and Amazon OpenSearch Service for full-text indexing and real-time search. OpenSearch is purpose-built for search and analytics workloads. For visualization, Amazon QuickSight can be connected to OpenSearch or other data sources to build rich dashboards. This architecture provides a scalable, fully managed, real-time search and analytics platform using AWS-native services.
- () via - https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html

**Answer:**
Correct Answer: **Ingest and process the streaming data using Amazon Kinesis Data Streams, then index the data with Amazon OpenSearch Service for real-time search capabilities. Use Amazon QuickSight to build interactive dashboards and visualizations based on the indexed data**

---

## Question 105

**Q:** Which solution will fulfill these requirements?

**Options:**
- (A) Create a gateway VPC endpoint for Amazon S3 in the VPC. Ensure that the EC2 instance’s subnet route table is updated to route S3 traffic through the endpoint. Confirm that appropriate IAM policies are in place to permit access via the VPC endpoint
- (B) Create an S3 access point within the same Region and attach a policy that grants the EC2 instance access. Update the application to use the access point alias to upload data
- (C) Set up a NAT gateway in the public subnet and modify the route table of the EC2 instance's subnet to direct Amazon S3 traffic through the NAT gateway
- (D) Provision a dedicated AWS Direct Connect link to route traffic from the VPC to Amazon S3 privately
- (E) Correct option:
- (F) There is no additional charge for using gateway endpoints. Amazon S3 supports both gateway endpoints and interface endpoints. With a gateway endpoint, you can access Amazon S3 from your VPC, without requiring an internet gateway or NAT device for your VPC, and with no additional cost. However, gateway endpoints do not allow access from on-premises networks, from peered VPCs in other AWS Regions, or through a transit gateway.
- (G) Incorrect options:
- (H) Set up a NAT gateway in the public subnet and modify the route table of the EC2 instance's subnet to direct Amazon S3 traffic through the NAT gateway - Although NAT gateways can route traffic to the internet, they do not provide private access to S3. Traffic sent through a NAT gateway to S3 still uses public endpoints and incurs data transfer charges. This does not satisfy the requirement to avoid public endpoint usage.
- (I) Provision a dedicated AWS Direct Connect link to route traffic from the VPC to Amazon S3 privately - Direct Connect is ideal for high-throughput, low-latency, hybrid workloads where traffic flows from on-premises to AWS. However, it is unnecessary for this use case, which involves internal traffic between EC2 and S3 within AWS.
- (J) References:
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-s3.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html
- () A fintech company currently operates a real-time search and analytics platform on-premises. This platform ingests streaming data from multiple data-producing systems and provides immediate search capabilities and interactive visualizations for end users. As part of its cloud migration strategy, the company wants to rearchitect the solution using AWS-native services.
- () Which of the following represents the most efficient solution?
- () Use AWS Glue streaming ETL to process data streams and load the data into Amazon Redshift. Use Amazon Redshift’s full-text search capabilities for querying. Use Amazon QuickSight for data visualizations
- **() Ingest and process the streaming data using Amazon Kinesis Data Streams, then index the data with Amazon OpenSearch Service for real-time search capabilities. Use Amazon QuickSight to build interactive dashboards and visualizations based on the indexed data** [CORRECT]
- () Deploy Amazon EC2 instances to handle the ingestion and processing of streaming data, storing the results in Amazon S3. Utilize Amazon Athena to search the stored data, and use Amazon Managed Grafana to generate dashboards and visual insights
- () Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate to ingest the data into Amazon DynamoDB to facilitate full text search. Use Amazon CloudWatch to create dashboards and query the data
- () This solution leverages Amazon Kinesis Data Streams for high-throughput, low-latency stream ingestion, and Amazon OpenSearch Service for full-text indexing and real-time search. OpenSearch is purpose-built for search and analytics workloads. For visualization, Amazon QuickSight can be connected to OpenSearch or other data sources to build rich dashboards. This architecture provides a scalable, fully managed, real-time search and analytics platform using AWS-native services.
- () via - https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html
- () https://docs.aws.amazon.com/streams/latest/dev/introduction.html
- () https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html
- () https://docs.aws.amazon.com/quicksight/latest/user/welcome.html
- () A company hires experienced specialists to analyze the customer service calls attended by its call center representatives. Now, the company wants to move to AWS Cloud and is looking at an automated solution to analyze customer service calls for sentiment analysis via ad-hoc SQL queries.

**Answer:**
Correct Answer: **Ingest and process the streaming data using Amazon Kinesis Data Streams, then index the data with Amazon OpenSearch Service for real-time search capabilities. Use Amazon QuickSight to build interactive dashboards and visualizations based on the indexed data**

---

## Question 106

**Q:** Which of the following represents the most efficient solution?

**Options:**
- (A) Use AWS Glue streaming ETL to process data streams and load the data into Amazon Redshift. Use Amazon Redshift’s full-text search capabilities for querying. Use Amazon QuickSight for data visualizations
- **(B) Ingest and process the streaming data using Amazon Kinesis Data Streams, then index the data with Amazon OpenSearch Service for real-time search capabilities. Use Amazon QuickSight to build interactive dashboards and visualizations based on the indexed data** [CORRECT]
- (C) Deploy Amazon EC2 instances to handle the ingestion and processing of streaming data, storing the results in Amazon S3. Utilize Amazon Athena to search the stored data, and use Amazon Managed Grafana to generate dashboards and visual insights
- (D) Use Amazon Elastic Container Service (Amazon ECS) with AWS Fargate to ingest the data into Amazon DynamoDB to facilitate full text search. Use Amazon CloudWatch to create dashboards and query the data
- (E) Correct option:
- (F) This solution leverages Amazon Kinesis Data Streams for high-throughput, low-latency stream ingestion, and Amazon OpenSearch Service for full-text indexing and real-time search. OpenSearch is purpose-built for search and analytics workloads. For visualization, Amazon QuickSight can be connected to OpenSearch or other data sources to build rich dashboards. This architecture provides a scalable, fully managed, real-time search and analytics platform using AWS-native services.
- (G) via - https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html
- (H) Incorrect options:
- (I) References:
- (J) https://docs.aws.amazon.com/streams/latest/dev/introduction.html
- () https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html
- () https://docs.aws.amazon.com/quicksight/latest/user/welcome.html
- () A company hires experienced specialists to analyze the customer service calls attended by its call center representatives. Now, the company wants to move to AWS Cloud and is looking at an automated solution to analyze customer service calls for sentiment analysis via ad-hoc SQL queries.

**Answer:**
Correct Answer: **Ingest and process the streaming data using Amazon Kinesis Data Streams, then index the data with Amazon OpenSearch Service for real-time search capabilities. Use Amazon QuickSight to build interactive dashboards and visualizations based on the indexed data**

---

## Question 107

**Q:** As a Solutions Architect, which of the following solutions would you recommend?

**Options:**
- (A) Use Amazon Kinesis Data Streams to read the audio files and machine learning (ML) algorithms to convert the audio files into text and run customer sentiment analysis
- (B) Use Amazon Transcribe to convert audio files to text and Amazon Quicksight to perform SQL based analysis on these text files to understand the underlying patterns. Visualize and display them onto user Dashboards for reporting purposes
- (C) Use Amazon Kinesis Data Streams to read the audio files and Amazon Alexa to convert them into text. Amazon Kinesis Data Analytics can be used to analyze these files and Amazon Quicksight can be used to visualize and display the output
- **(D) Use Amazon Transcribe to convert audio files to text and Amazon Athena to perform SQL based analysis to understand the underlying customer sentiments** [CORRECT]
- (E) Correct option:
- (F) Amazon Transcribe is an automatic speech recognition (ASR) service that makes it easy to convert audio to text. One key feature of the service is called speaker identification, which you can use to label each individual speaker when transcribing multi-speaker audio files. You can specify Amazon Transcribe to identify 2–10 speakers in the audio clip.
- (G) Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run. To leverage Athena, you can simply point to your data in Amazon S3, define the schema, and start querying using standard SQL. Most results are delivered within seconds.
- (H) Analyzing multi-speaker audio files using Amazon Transcribe and Amazon Athena:
- (I) via - https://aws.amazon.com/blogs/machine-learning/automating-the-analysis-of-multi-speaker-audio-files-using-amazon-transcribe-and-amazon-athena
- (J) Incorrect options:
- () Use Amazon Kinesis Data Streams to read the audio files and machine learning (ML) algorithms to convert the audio files into text and run customer sentiment analysis - Amazon Kinesis can be used to stream real-time data for further analysis and storage. Kinesis Data Streams cannot read audio files. You will still need to use AWS Transcribe for ASR services.
- () Use Amazon Kinesis Data Streams to read the audio files and Amazon Alexa to convert them into text. Amazon Kinesis Data Analytics can be used to analyze these files and Amazon Quicksight can be used to visualize and display the output - Amazon Kinesis Data Streams cannot read audio files. Amazon Alexa cannot be used as an Automatic Speech Recognition (ASR) service, though Alexa internally uses ASR for its working.
- () Use Amazon Transcribe to convert audio files to text and Amazon Quicksight to perform SQL based analysis on these text files to understand the underlying patterns. Visualize and display them onto user Dashboards for reporting purposes - Amazon Quicksight is used for the visual representation of data through dashboards. However, it is not an SQL query based analysis tool like Amazon Athena. So, this option is incorrect.
- () References:
- () https://aws.amazon.com/blogs/machine-learning/automating-the-analysis-of-multi-speaker-audio-files-using-amazon-transcribe-and-amazon-athena
- () https://aws.amazon.com/athena
- () An online gaming company wants to block access to its application from specific countries; however, the company wants to allow its remote development team (from one of the blocked countries) to have access to the application. The application is deployed on Amazon EC2 instances running under an Application Load Balancer with AWS Web Application Firewall (AWS WAF).
- () As a solutions architect, which of the following solutions can be combined to address the given use-case? (Select two)
- () Correct selection
- () Use AWS WAF geo match statement listing the countries that you want to block
- () Use AWS WAF IP set statement that specifies the IP addresses that you want to allow through
- () Use Application Load Balancer geo match statement listing the countries that you want to block
- () Create a deny rule for the blocked countries in the network access control list (network ACL) associated with each of the Amazon EC2 instances
- () Use Application Load Balancer IP set statement that specifies the IP addresses that you want to allow through
- () Correct options:
- () AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that block common attack patterns and rules that filter out specific traffic patterns you define.
- () You can deploy AWS WAF on Amazon CloudFront as part of your CDN solution, the Application Load Balancer that fronts your web servers or origin servers running on Amazon EC2, or Amazon API Gateway for your APIs.
- () AWS WAF - How it Works?:
- () via - https://aws.amazon.com/waf/
- () To block specific countries, you can create a AWS WAF geo match statement listing the countries that you want to block, and to allow traffic from IPs of the remote development team, you can create a WAF IP set statement that specifies the IP addresses that you want to allow through. You can combine the two rules as shown below:
- () Create a deny rule for the blocked countries in the network access control list (network ACL) associated with each of the Amazon EC2 instances - A network access control list (network ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. A network access control list (network ACL) does not have the capability to block traffic based on geographic match conditions.
- () An Application Load Balancer operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- () An Application Load Balancer cannot block or allow traffic based on geographic match conditions or IP based conditions. Both these options have been added as distractors.
- () https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-geo-match.html
- () https://aws.amazon.com/blogs/security/how-to-use-aws-waf-to-filter-incoming-traffic-from-embargoed-countries/
- () A DevOps team is tasked with enabling secure and temporary SSH access to Amazon EC2 instances for developers during deployments. The team wants to avoid distributing long-term SSH key pairs and instead prefers ephemeral access that can be audited and revoked immediately after the session ends. The team wants direct access via the AWS Management Console.
- () What do you recommend?
- () Use an EC2 Instance Connect Endpoint to reach the instances even though they already have public IP addresses, because Instance Connect requires an endpoint for all SSH sessions

**Answer:**
Correct Answer: **Use Amazon Transcribe to convert audio files to text and Amazon Athena to perform SQL based analysis to understand the underlying customer sentiments**

---

## Question 108

**Q:** As a solutions architect, which of the following solutions can be combined to address the given use-case? (Select two)

**Options:**
- (A) Correct selection
- (B) Use AWS WAF geo match statement listing the countries that you want to block
- (C) Use AWS WAF IP set statement that specifies the IP addresses that you want to allow through
- (D) Use Application Load Balancer geo match statement listing the countries that you want to block
- (E) Create a deny rule for the blocked countries in the network access control list (network ACL) associated with each of the Amazon EC2 instances
- (F) Use Application Load Balancer IP set statement that specifies the IP addresses that you want to allow through
- (G) Correct options:
- (H) AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that block common attack patterns and rules that filter out specific traffic patterns you define.
- (I) You can deploy AWS WAF on Amazon CloudFront as part of your CDN solution, the Application Load Balancer that fronts your web servers or origin servers running on Amazon EC2, or Amazon API Gateway for your APIs.
- (J) AWS WAF - How it Works?:
- () via - https://aws.amazon.com/waf/
- () To block specific countries, you can create a AWS WAF geo match statement listing the countries that you want to block, and to allow traffic from IPs of the remote development team, you can create a WAF IP set statement that specifies the IP addresses that you want to allow through. You can combine the two rules as shown below:
- () Incorrect options:
- () Create a deny rule for the blocked countries in the network access control list (network ACL) associated with each of the Amazon EC2 instances - A network access control list (network ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. A network access control list (network ACL) does not have the capability to block traffic based on geographic match conditions.
- () An Application Load Balancer operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- () An Application Load Balancer cannot block or allow traffic based on geographic match conditions or IP based conditions. Both these options have been added as distractors.
- () References:
- () https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-geo-match.html
- () https://aws.amazon.com/blogs/security/how-to-use-aws-waf-to-filter-incoming-traffic-from-embargoed-countries/
- () A DevOps team is tasked with enabling secure and temporary SSH access to Amazon EC2 instances for developers during deployments. The team wants to avoid distributing long-term SSH key pairs and instead prefers ephemeral access that can be audited and revoked immediately after the session ends. The team wants direct access via the AWS Management Console.
- () What do you recommend?
- () Use an EC2 Instance Connect Endpoint to reach the instances even though they already have public IP addresses, because Instance Connect requires an endpoint for all SSH sessions
- **() Use EC2 Instance Connect to inject a temporary public key and establish SSH access using the instance’s public IP address** [CORRECT]
- () Use EC2 Instance Connect to inject a static SSH key and connect via the instance's private IP address directly from the internet
- () Use EC2 Instance Connect with Systems Manager Agent disabled, and connect via private IP using an internal proxy endpoint
- () Correct option:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-connect-methods.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-with-ec2-instance-connect-endpoint.html
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html
- () A financial auditing firm uses Amazon S3 to store sensitive client records that are subject to write-once-read-many (WORM) regulations to prevent alteration or deletion of records for a specific retention period. The firm wants to enforce immutable storage, such that even administrators cannot overwrite or delete the records during the lock duration. They also need audit-friendly enforcement to prevent accidental or malicious deletion.

**Answer:**
Correct Answer: **Use EC2 Instance Connect to inject a temporary public key and establish SSH access using the instance’s public IP address**

---

## Question 109

**Q:** AWS WAF - How it Works?:

**Options:**
- (A) via - https://aws.amazon.com/waf/
- (B) To block specific countries, you can create a AWS WAF geo match statement listing the countries that you want to block, and to allow traffic from IPs of the remote development team, you can create a WAF IP set statement that specifies the IP addresses that you want to allow through. You can combine the two rules as shown below:
- (C) Incorrect options:
- (D) Create a deny rule for the blocked countries in the network access control list (network ACL) associated with each of the Amazon EC2 instances - A network access control list (network ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. A network access control list (network ACL) does not have the capability to block traffic based on geographic match conditions.
- (E) Use Application Load Balancer geo match statement listing the countries that you want to block
- (F) Use Application Load Balancer IP set statement that specifies the IP addresses that you want to allow through
- (G) An Application Load Balancer operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- (H) An Application Load Balancer cannot block or allow traffic based on geographic match conditions or IP based conditions. Both these options have been added as distractors.
- (I) References:
- (J) https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-geo-match.html
- () https://aws.amazon.com/blogs/security/how-to-use-aws-waf-to-filter-incoming-traffic-from-embargoed-countries/
- () A DevOps team is tasked with enabling secure and temporary SSH access to Amazon EC2 instances for developers during deployments. The team wants to avoid distributing long-term SSH key pairs and instead prefers ephemeral access that can be audited and revoked immediately after the session ends. The team wants direct access via the AWS Management Console.
- () What do you recommend?
- () Use an EC2 Instance Connect Endpoint to reach the instances even though they already have public IP addresses, because Instance Connect requires an endpoint for all SSH sessions
- **() Use EC2 Instance Connect to inject a temporary public key and establish SSH access using the instance’s public IP address** [CORRECT]
- () Use EC2 Instance Connect to inject a static SSH key and connect via the instance's private IP address directly from the internet
- () Use EC2 Instance Connect with Systems Manager Agent disabled, and connect via private IP using an internal proxy endpoint
- () Correct option:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-connect-methods.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-with-ec2-instance-connect-endpoint.html
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager.html
- () A financial auditing firm uses Amazon S3 to store sensitive client records that are subject to write-once-read-many (WORM) regulations to prevent alteration or deletion of records for a specific retention period. The firm wants to enforce immutable storage, such that even administrators cannot overwrite or delete the records during the lock duration. They also need audit-friendly enforcement to prevent accidental or malicious deletion.

**Answer:**
Correct Answer: **Use EC2 Instance Connect to inject a temporary public key and establish SSH access using the instance’s public IP address**

---

## Question 110

**Q:** Which configuration of S3 Object Lock will ensure that the retention policy is strictly enforced, and no user (including root or administrators) can override or delete protected objects during the lock period?

**Options:**
- (A) Use S3 Object Lock in Governance Mode, which allows only IAM users with elevated permissions to override or remove retention settings
- (B) Use S3 Lifecycle Policies to transition data to Glacier Deep Archive and treat it as immutable during the archival period
- (C) Enable S3 Versioning and set a bucket policy that denies s3:DeleteObject to all users during the retention period
- (D) Use S3 Object Lock in Compliance Mode, which enforces retention policies strictly and prevents all users from modifying or deleting data during the retention period
- (E) Correct option:
- (F) S3 Object Lock in Compliance Mode is designed to meet stringent regulatory requirements. In this mode, no user, not even the root user, can override or delete a locked object until the retention period expires. This ensures strict WORM behavior, making Compliance Mode ideal for regulated industries where immutability must be enforced regardless of user permissions. Attempting to modify or delete objects locked in compliance mode results in an AccessDenied error, even for administrators.
- (G) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock.html#object-lock-retention-modes
- (H) Incorrect options:
- (I) Reference:
- (J) https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lock.html#object-lock-retention-modes
- () Which solution will best meet these requirements?
- () Use AWS CloudFront to route requests from the application’s internal services to the SaaS provider through edge locations
- () Establish a VPN connection using AWS Site-to-Site VPN to create a secure tunnel between the internal services and the third-party SaaS provider
- () Use AWS PrivateLink to create a private endpoint within the application’s VPC that connects securely to the SaaS provider’s VPC
- () Set up VPC peering between the application VPC and the SaaS provider’s VPC to allow direct communication
- () AWS PrivateLink is a fully managed service that enables private connectivity between Virtual Private Clouds (VPCs), AWS services, and supported third-party SaaS applications over the AWS network, without exposing traffic to the public internet. In this case, the internal service components of the application can securely access the third-party SaaS APIs by creating an interface VPC endpoint for the SaaS provider's service.
- () via - https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/aws-privatelink.html
- () Establish a VPN connection using AWS Site-to-Site VPN to create a secure tunnel between the internal services and the third-party SaaS provider - While Site-to-Site VPN can establish a secure connection, it typically requires IPsec-compatible devices and may route traffic over the internet, depending on the SaaS provider's setup. It also introduces more operational complexity and latency compared to AWS-native private connectivity options.
- () Use AWS CloudFront to route requests from the application’s internal services to the SaaS provider through edge locations - CloudFront is designed for content distribution and caching at edge locations. It does not establish private or secure backend connectivity between internal services and SaaS APIs, and traffic still traverses the public internet.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/privatelink/what-is-privatelink.html
- () https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/aws-privatelink.html
- () A streaming solutions company is building a video streaming product by using an Application Load Balancer (ALB) that routes the requests to the underlying Amazon EC2 instances. The engineering team has noticed a peculiar pattern. The Application Load Balancer removes an instance from its pool of healthy instances whenever it is detected as unhealthy but the Auto Scaling group fails to kick-in and provision the replacement instance.
- () What could explain this anomaly?
- **() The Auto Scaling group is using Amazon EC2 based health check and the Application Load Balancer is using ALB based health check** [CORRECT]
- () The Auto Scaling group is using ALB based health check and the Application Load Balancer is using Amazon EC2 based health check
- () Both the Auto Scaling group and Application Load Balancer are using ALB based health check
- () Both the Auto Scaling group and Application Load Balancer are using Amazon EC2 based health check
- () An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for automatic scaling and management.
- () Auto Scaling Group Overview:

**Answer:**
Correct Answer: **The Auto Scaling group is using Amazon EC2 based health check and the Application Load Balancer is using ALB based health check**

---

## Question 111

**Q:** What could explain this anomaly?

**Options:**
- (A) The Auto Scaling group is using Amazon EC2 based health check and the Application Load Balancer is using ALB based health check
- (B) The Auto Scaling group is using ALB based health check and the Application Load Balancer is using Amazon EC2 based health check
- (C) Both the Auto Scaling group and Application Load Balancer are using ALB based health check
- (D) Both the Auto Scaling group and Application Load Balancer are using Amazon EC2 based health check
- (E) Correct option:
- (F) An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for automatic scaling and management.
- (G) Auto Scaling Group Overview:
- (H) via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- (I) Application Load Balancer automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, and AWS Lambda functions. It can handle the varying load of your application traffic in a single Availability Zone or across multiple Availability Zones.
- (J) Incorrect options:
- () The Auto Scaling group is using ALB based health check and the Application Load Balancer is using Amazon EC2 based health check - Application Load Balancer cannot use EC2 based health checks, so this option is incorrect.
- () Both the Auto Scaling group and Application Load Balancer are using Amazon EC2 based health check - Application Load Balancer cannot use EC2 based health checks, so this option is incorrect.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-health-checks.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/health-checks-overview.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-add-elb-healthcheck.html
- () A pharmaceutical company is considering moving to AWS Cloud to accelerate the research and development process. Most of the daily workflows would be centered around running batch jobs on Amazon EC2 instances with storage on Amazon Elastic Block Store (Amazon EBS) volumes. The CTO is concerned about meeting HIPAA compliance norms for sensitive data stored on Amazon EBS.
- () Which of the following options outline the correct capabilities of an encrypted Amazon EBS volume? (Select three)
- () Correct selection
- () Data at rest inside the volume is encrypted
- () Data moving between the volume and the instance is encrypted
- () Data moving between the volume and the instance is NOT encrypted
- () Any snapshot created from the volume is encrypted
- () Data at rest inside the volume is NOT encrypted
- () Any snapshot created from the volume is NOT encrypted
- () Correct options:
- () Therefore, the incorrect options are:
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html
- () A retail company maintains an AWS Direct Connect connection to AWS and has recently migrated its data warehouse to AWS. The data analysts at the company query the data warehouse using a visualization tool. The average size of a query returned by the data warehouse is 60 megabytes and the query responses returned by the data warehouse are not cached in the visualization tool. Each webpage returned by the visualization tool is approximately 600 kilobytes.
- () Which of the following options offers the LOWEST data transfer egress cost for the company?
- () Deploy the visualization tool on-premises. Query the data warehouse over the internet at a location in the same AWS region
- () Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over the internet at a location in the same region
- () Deploy the visualization tool on-premises. Query the data warehouse directly over an AWS Direct Connect connection at a location in the same AWS region
- **() Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over a Direct Connect connection at a location in the same region** [CORRECT]

**Answer:**
Correct Answer: **Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over a Direct Connect connection at a location in the same region**

---

## Question 112

**Q:** Which of the following options outline the correct capabilities of an encrypted Amazon EBS volume? (Select three)

**Options:**
- (A) Correct selection
- (B) Data at rest inside the volume is encrypted
- (C) Data moving between the volume and the instance is encrypted
- (D) Data moving between the volume and the instance is NOT encrypted
- (E) Any snapshot created from the volume is encrypted
- (F) Data at rest inside the volume is NOT encrypted
- (G) Any snapshot created from the volume is NOT encrypted
- (H) Correct options:
- (I) Therefore, the incorrect options are:
- (J) Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html
- () A retail company maintains an AWS Direct Connect connection to AWS and has recently migrated its data warehouse to AWS. The data analysts at the company query the data warehouse using a visualization tool. The average size of a query returned by the data warehouse is 60 megabytes and the query responses returned by the data warehouse are not cached in the visualization tool. Each webpage returned by the visualization tool is approximately 600 kilobytes.
- () Which of the following options offers the LOWEST data transfer egress cost for the company?
- () Deploy the visualization tool on-premises. Query the data warehouse over the internet at a location in the same AWS region
- () Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over the internet at a location in the same region
- () Deploy the visualization tool on-premises. Query the data warehouse directly over an AWS Direct Connect connection at a location in the same AWS region
- () Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over a Direct Connect connection at a location in the same region
- () Correct option:
- () AWS Direct Connect is a networking service that provides an alternative to using the internet to connect to AWS. Using AWS Direct Connect, data that would have previously been transported over the internet is delivered through a private network connection between your on-premises data center and AWS.
- () For the given use case, the main pricing parameter while using the AWS Direct Connect connection is the Data Transfer Out (DTO) from AWS to the on-premises data center. DTO refers to the cumulative network traffic that is sent through AWS Direct Connect to destinations outside of AWS. This is charged per gigabyte (GB), and unlike capacity measurements, DTO refers to the amount of data transferred, not the speed.
- () via - https://aws.amazon.com/directconnect/pricing/
- () Each query response is 60 megabytes in size and each webpage for the visualization tool is 600 kilobytes in size. If you deploy the visualization tool in the same AWS region as the data warehouse, then you only need to pay for the 600 kilobytes of DTO charges for the webpage. Therefore this option is correct.
- () However, if you deploy the visualization tool on-premises, then you need to pay for the 60 MB of DTO charges for the query response from the data warehouse to the visualization tool.
- () Incorrect options:
- () Data transfer pricing over AWS Direct Connect is lower than data transfer pricing over the internet, so both of these options are incorrect.
- () Deploy the visualization tool on-premises. Query the data warehouse directly over an AWS Direct Connect connection at a location in the same AWS region - As mentioned in the explanation above, if you deploy the visualization tool on-premises, then you need to pay for the 60 megabytes of DTO charges for the query response from the data warehouse to the visualization tool. So this option is incorrect.
- () References:
- () https://aws.amazon.com/directconnect/pricing/
- () https://aws.amazon.com/getting-started/hands-on/connect-data-center-to-aws/services-costs/
- () https://aws.amazon.com/directconnect/faqs/
- () Which solution should you recommend?
- **() Set up AWS Global Accelerator with listeners configured for HTTPS. Create endpoint groups for Europe and Asia and add the existing us-west-2 EC2 endpoint to these groups** [CORRECT]
- () Use Amazon Route 53 latency-based routing to direct user requests to a copy of the EC2 API deployed in each major geographic Region
- () Deploy Amazon API Gateway in multiple AWS Regions and synchronize the API definitions. Use AWS Lambda as a proxy to forward requests to the EC2-hosted API in us-west-2

**Answer:**
Correct Answer: **Set up AWS Global Accelerator with listeners configured for HTTPS. Create endpoint groups for Europe and Asia and add the existing us-west-2 EC2 endpoint to these groups**

---

## Question 113

**Q:** Which of the following options offers the LOWEST data transfer egress cost for the company?

**Options:**
- (A) Deploy the visualization tool on-premises. Query the data warehouse over the internet at a location in the same AWS region
- (B) Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over the internet at a location in the same region
- (C) Deploy the visualization tool on-premises. Query the data warehouse directly over an AWS Direct Connect connection at a location in the same AWS region
- (D) Deploy the visualization tool in the same AWS region as the data warehouse. Access the visualization tool over a Direct Connect connection at a location in the same region
- (E) Correct option:
- (F) AWS Direct Connect is a networking service that provides an alternative to using the internet to connect to AWS. Using AWS Direct Connect, data that would have previously been transported over the internet is delivered through a private network connection between your on-premises data center and AWS.
- (G) For the given use case, the main pricing parameter while using the AWS Direct Connect connection is the Data Transfer Out (DTO) from AWS to the on-premises data center. DTO refers to the cumulative network traffic that is sent through AWS Direct Connect to destinations outside of AWS. This is charged per gigabyte (GB), and unlike capacity measurements, DTO refers to the amount of data transferred, not the speed.
- (H) via - https://aws.amazon.com/directconnect/pricing/
- (I) Each query response is 60 megabytes in size and each webpage for the visualization tool is 600 kilobytes in size. If you deploy the visualization tool in the same AWS region as the data warehouse, then you only need to pay for the 600 kilobytes of DTO charges for the webpage. Therefore this option is correct.
- (J) However, if you deploy the visualization tool on-premises, then you need to pay for the 60 MB of DTO charges for the query response from the data warehouse to the visualization tool.
- () Incorrect options:
- () Data transfer pricing over AWS Direct Connect is lower than data transfer pricing over the internet, so both of these options are incorrect.
- () Deploy the visualization tool on-premises. Query the data warehouse directly over an AWS Direct Connect connection at a location in the same AWS region - As mentioned in the explanation above, if you deploy the visualization tool on-premises, then you need to pay for the 60 megabytes of DTO charges for the query response from the data warehouse to the visualization tool. So this option is incorrect.
- () References:
- () https://aws.amazon.com/directconnect/pricing/
- () https://aws.amazon.com/getting-started/hands-on/connect-data-center-to-aws/services-costs/
- () https://aws.amazon.com/directconnect/faqs/
- () Which solution should you recommend?
- () Set up AWS Global Accelerator with listeners configured for HTTPS. Create endpoint groups for Europe and Asia and add the existing us-west-2 EC2 endpoint to these groups
- () Use Amazon Route 53 latency-based routing to direct user requests to a copy of the EC2 API deployed in each major geographic Region
- () Deploy Amazon API Gateway in multiple AWS Regions and synchronize the API definitions. Use AWS Lambda as a proxy to forward requests to the EC2-hosted API in us-west-2
- () Deploy an Amazon CloudFront distribution in front of the API endpoint and apply the CachingOptimized managed policy to enhance caching behavior and improve content delivery efficiency
- () Use Amazon Route 53 latency-based routing to direct user requests to a copy of the EC2 API deployed in each major geographic Region - Latency-based routing works well when application stacks are deployed in multiple Regions. However, this approach involves replicating the EC2-based API infrastructure across multiple Regions, significantly increasing compute, data transfer, and management overhead. This is not the most cost-effective option as requested in the scenario.
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/introduction-how-it-works.html
- () https://aws.amazon.com/global-accelerator/features/#Use_cases
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-api-endpoint-types.html
- () A streaming service provider collects user experience feedback through embedded feedback forms in their mobile and web apps. Feedback submissions frequently spike to thousands per hour during content launches or service outages. Currently, the feedback is sent via email to the operations team for manual review. The company now wants to automate feedback collection and sentiment analysis so that insights can be generated quickly and stored for a full year for trend analysis.
- () Which solution provides the most scalable and automated approach to meet these requirements?
- () Build a web service on Amazon EC2 that receives feedback data and stores each record in a DynamoDB table. Use the EC2 application to invoke Amazon Comprehend for sentiment detection and write results to a second table. Apply a TTL of 365 days to each table
- **() Design a RESTful API with Amazon API Gateway that forwards incoming feedback data to an Amazon SQS queue. Set up an AWS Lambda function to process the queue messages, analyze sentiment using Amazon Comprehend, and store results in a DynamoDB table with a 365-day TTL configured on each item** [CORRECT]
- () Route all feedback submissions through Amazon Kinesis Data Streams. Use an AWS Lambda consumer to batch process incoming records, invoke Amazon Translate to detect language and convert input to English, and save the processed content in an Amazon OpenSearch Service index. Configure OpenSearch Index State Management (ISM) policies to delete documents after 12 months
- () Use Amazon EventBridge to capture feedback events and forward them to an AWS Step Functions workflow. The workflow invokes Lambda functions for validation, calls Amazon Transcribe to convert the text to audio for archival, and stores the results in an Amazon RDS database. Configure a lifecycle policy to remove records after 12 months

**Answer:**
Correct Answer: **Design a RESTful API with Amazon API Gateway that forwards incoming feedback data to an Amazon SQS queue. Set up an AWS Lambda function to process the queue messages, analyze sentiment using Amazon Comprehend, and store results in a DynamoDB table with a 365-day TTL configured on each item**

---

## Question 114

**Q:** Which solution should you recommend?

**Options:**
- (A) Set up AWS Global Accelerator with listeners configured for HTTPS. Create endpoint groups for Europe and Asia and add the existing us-west-2 EC2 endpoint to these groups
- (B) Use Amazon Route 53 latency-based routing to direct user requests to a copy of the EC2 API deployed in each major geographic Region
- (C) Deploy Amazon API Gateway in multiple AWS Regions and synchronize the API definitions. Use AWS Lambda as a proxy to forward requests to the EC2-hosted API in us-west-2
- (D) Deploy an Amazon CloudFront distribution in front of the API endpoint and apply the CachingOptimized managed policy to enhance caching behavior and improve content delivery efficiency
- (E) Correct option:
- (F) Incorrect options:
- (G) Use Amazon Route 53 latency-based routing to direct user requests to a copy of the EC2 API deployed in each major geographic Region - Latency-based routing works well when application stacks are deployed in multiple Regions. However, this approach involves replicating the EC2-based API infrastructure across multiple Regions, significantly increasing compute, data transfer, and management overhead. This is not the most cost-effective option as requested in the scenario.
- (H) References:
- (I) https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- (J) https://docs.aws.amazon.com/global-accelerator/latest/dg/introduction-how-it-works.html
- () https://aws.amazon.com/global-accelerator/features/#Use_cases
- () https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-api-endpoint-types.html
- () A streaming service provider collects user experience feedback through embedded feedback forms in their mobile and web apps. Feedback submissions frequently spike to thousands per hour during content launches or service outages. Currently, the feedback is sent via email to the operations team for manual review. The company now wants to automate feedback collection and sentiment analysis so that insights can be generated quickly and stored for a full year for trend analysis.
- () Which solution provides the most scalable and automated approach to meet these requirements?
- () Build a web service on Amazon EC2 that receives feedback data and stores each record in a DynamoDB table. Use the EC2 application to invoke Amazon Comprehend for sentiment detection and write results to a second table. Apply a TTL of 365 days to each table
- () Design a RESTful API with Amazon API Gateway that forwards incoming feedback data to an Amazon SQS queue. Set up an AWS Lambda function to process the queue messages, analyze sentiment using Amazon Comprehend, and store results in a DynamoDB table with a 365-day TTL configured on each item
- () Route all feedback submissions through Amazon Kinesis Data Streams. Use an AWS Lambda consumer to batch process incoming records, invoke Amazon Translate to detect language and convert input to English, and save the processed content in an Amazon OpenSearch Service index. Configure OpenSearch Index State Management (ISM) policies to delete documents after 12 months
- () Use Amazon EventBridge to capture feedback events and forward them to an AWS Step Functions workflow. The workflow invokes Lambda functions for validation, calls Amazon Transcribe to convert the text to audio for archival, and stores the results in an Amazon RDS database. Configure a lifecycle policy to remove records after 12 months
- () https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/TTL.html
- () https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ism.html
- () https://docs.aws.amazon.com/transcribe/latest/dg/what-is.html
- () https://docs.aws.amazon.com/translate/latest/dg/what-is.html
- () Which solution should the team use to meet this requirement?
- () Use Amazon Inspector to detect over-permissive IAM policies and access paths across the environment
- **() Use AWS Identity and Access Management (IAM) Access Analyzer to evaluate resource-based and identity-based policies and identify resources shared outside the account or organization** [CORRECT]
- () Use IAM Access Advisor to get detailed access analysis of S3 bucket policies and determine which principals outside the organization have access
- () Use AWS Config to track configuration changes and infer resource-sharing behavior by analyzing compliance rules

**Answer:**
Correct Answer: **Use AWS Identity and Access Management (IAM) Access Analyzer to evaluate resource-based and identity-based policies and identify resources shared outside the account or organization**

---

## Question 115

**Q:** Which solution provides the most scalable and automated approach to meet these requirements?

**Options:**
- (A) Build a web service on Amazon EC2 that receives feedback data and stores each record in a DynamoDB table. Use the EC2 application to invoke Amazon Comprehend for sentiment detection and write results to a second table. Apply a TTL of 365 days to each table
- (B) Design a RESTful API with Amazon API Gateway that forwards incoming feedback data to an Amazon SQS queue. Set up an AWS Lambda function to process the queue messages, analyze sentiment using Amazon Comprehend, and store results in a DynamoDB table with a 365-day TTL configured on each item
- (C) Route all feedback submissions through Amazon Kinesis Data Streams. Use an AWS Lambda consumer to batch process incoming records, invoke Amazon Translate to detect language and convert input to English, and save the processed content in an Amazon OpenSearch Service index. Configure OpenSearch Index State Management (ISM) policies to delete documents after 12 months
- (D) Use Amazon EventBridge to capture feedback events and forward them to an AWS Step Functions workflow. The workflow invokes Lambda functions for validation, calls Amazon Transcribe to convert the text to audio for archival, and stores the results in an Amazon RDS database. Configure a lifecycle policy to remove records after 12 months
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/comprehend/latest/dg/what-is.html
- (I) https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/TTL.html
- (J) https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ism.html
- () https://docs.aws.amazon.com/transcribe/latest/dg/what-is.html
- () https://docs.aws.amazon.com/translate/latest/dg/what-is.html
- () Which solution should the team use to meet this requirement?
- () Use Amazon Inspector to detect over-permissive IAM policies and access paths across the environment
- **() Use AWS Identity and Access Management (IAM) Access Analyzer to evaluate resource-based and identity-based policies and identify resources shared outside the account or organization** [CORRECT]
- () Use IAM Access Advisor to get detailed access analysis of S3 bucket policies and determine which principals outside the organization have access
- () Use AWS Config to track configuration changes and infer resource-sharing behavior by analyzing compliance rules
- () Use Amazon Inspector to detect over-permissive IAM policies and access paths across the environment - Amazon Inspector is primarily a vulnerability assessment tool focused on EC2 instances, container images, and Lambda functions. It checks for software vulnerabilities and security best practices, but it does not evaluate IAM policies or analyze whether resources like S3 buckets or roles are accessible to external accounts. It is not designed for access path analysis or policy-level visibility.
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html
- () https://aws.amazon.com/blogs/security/set-permission-guardrails-using-iam-access-advisor-analyze-service-last-accessed-information-aws-organization/
- () A leading media company wants to do an accelerated online migration of hundreds of terabytes of files from their on-premises data center to Amazon S3 and then establish a mechanism to access the migrated data for ongoing updates from the on-premises applications.

**Answer:**
Correct Answer: **Use AWS Identity and Access Management (IAM) Access Analyzer to evaluate resource-based and identity-based policies and identify resources shared outside the account or organization**

---

## Question 116

**Q:** Which solution should the team use to meet this requirement?

**Options:**
- (A) Use Amazon Inspector to detect over-permissive IAM policies and access paths across the environment
- **(B) Use AWS Identity and Access Management (IAM) Access Analyzer to evaluate resource-based and identity-based policies and identify resources shared outside the account or organization** [CORRECT]
- (C) Use IAM Access Advisor to get detailed access analysis of S3 bucket policies and determine which principals outside the organization have access
- (D) Use AWS Config to track configuration changes and infer resource-sharing behavior by analyzing compliance rules
- (E) Correct option:
- (F) Incorrect options:
- (G) Use Amazon Inspector to detect over-permissive IAM policies and access paths across the environment - Amazon Inspector is primarily a vulnerability assessment tool focused on EC2 instances, container images, and Lambda functions. It checks for software vulnerabilities and security best practices, but it does not evaluate IAM policies or analyze whether resources like S3 buckets or roles are accessible to external accounts. It is not designed for access path analysis or policy-level visibility.
- (H) References:
- (I) https://docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html
- (J) https://aws.amazon.com/blogs/security/set-permission-guardrails-using-iam-access-advisor-analyze-service-last-accessed-information-aws-organization/
- () A leading media company wants to do an accelerated online migration of hundreds of terabytes of files from their on-premises data center to Amazon S3 and then establish a mechanism to access the migrated data for ongoing updates from the on-premises applications.

**Answer:**
Correct Answer: **Use AWS Identity and Access Management (IAM) Access Analyzer to evaluate resource-based and identity-based policies and identify resources shared outside the account or organization**

---

## Question 117

**Q:** As a solutions architect, which of the following would you select as the MOST performant solution for the given use-case?

**Options:**
- (A) Use Amazon S3 Transfer Acceleration (Amazon S3TA) to migrate existing data to Amazon S3 and then use AWS DataSync for ongoing updates from the on-premises applications
- (B) Use File Gateway configuration of AWS Storage Gateway to migrate data to Amazon S3 and then use Amazon S3 Transfer Acceleration (Amazon S3TA) for ongoing updates from the on-premises applications
- **(C) Use AWS DataSync to migrate existing data to Amazon S3 and then use File Gateway to retain access to the migrated data for ongoing updates from the on-premises applications** [CORRECT]
- (D) Use AWS DataSync to migrate existing data to Amazon S3 as well as access the Amazon S3 data for ongoing updates
- (E) Correct option:
- (F) AWS DataSync is an online data transfer service that simplifies, automates, and accelerates copying large amounts of data to and from AWS storage services over the internet or AWS Direct Connect.
- (G) AWS DataSync fully automates the data transfer. It comes with retry and network resiliency mechanisms, network optimizations, built-in task scheduling, monitoring via the AWS DataSync API and Console, and Amazon CloudWatch metrics, events, and logs that provide granular visibility into the transfer process. AWS DataSync performs data integrity verification both during the transfer and at the end of the transfer.
- (H) How AWS DataSync Works:
- (I) via - https://aws.amazon.com/datasync/
- (J) AWS Storage Gateway is a hybrid cloud storage service that gives you on-premises access to virtually unlimited cloud storage. The service provides three different types of gateways – Tape Gateway, File Gateway, and Volume Gateway – that seamlessly connect on-premises applications to cloud storage, caching data locally for low-latency access. File gateway offers SMB or NFS-based access to data in Amazon S3 with local caching.
- () The combination of AWS DataSync and File Gateway is the correct solution. AWS DataSync enables you to automate and accelerate online data transfers to AWS storage services. File Gateway then provides your on-premises applications with low latency access to the migrated data.
- () Incorrect options:
- () Use AWS DataSync to migrate existing data to Amazon S3 as well as access the Amazon S3 data for ongoing updates - AWS DataSync is used to easily transfer data to and from AWS with up to 10x faster speeds. It is used to transfer data and cannot be used to facilitate ongoing updates to the migrated files from the on-premises applications.
- () Use Amazon S3 Transfer Acceleration (Amazon S3TA) to migrate existing data to Amazon S3 and then use AWS DataSync for ongoing updates from the on-premises applications - If your application is already integrated with the Amazon S3 API, and you want higher throughput for transferring large files to Amazon S3, Amazon S3 Transfer Acceleration can be used. However AWS DataSync cannot be used to facilitate ongoing updates to the migrated files from the on-premises applications.
- () Reference:
- () https://aws.amazon.com/datasync/features/

**Answer:**
Correct Answer: **Use AWS DataSync to migrate existing data to Amazon S3 and then use File Gateway to retain access to the migrated data for ongoing updates from the on-premises applications**

---

## Question 118

**Q:** Which option best meets the application’s availability, durability, and RPO objectives?

**Options:**
- (A) Deploy Amazon FSx for Lustre and configure a backup plan using AWS Backup for cross-Region replication of the file system metadata
- **(B) Use Amazon Elastic File System (Amazon EFS) with the Standard storage class and configure AWS Backup to create cross-Region backups on a scheduled basis** [CORRECT]
- (C) Configure Amazon S3 with the S3 Standard storage class and mount it in containers using Mountpoint for Amazon S3. Use AWS Backup to replicate objects to another Region
- (D) Use Amazon FSx for NetApp ONTAP with a Multi-AZ deployment and rely on its native high availability and AWS Backup integration to replicate the file system to another Region automatically
- (E) Correct option:
- (F) Amazon EFS is a fully managed, scalable, NFS-compatible file system ideal for containerized workloads. It provides multi-AZ mount targets by default and supports integration with AWS Backup for automated cross-Region backup and restore. When used with AWS Backup, EFS can achieve an RPO of 8 hours or less through scheduled backups. The Standard storage class offers high durability and low latency, making it a strong fit for active workloads that span Availability Zones.
- (G) Incorrect options:
- (H) Configure Amazon S3 with the S3 Standard storage class and mount it in containers using Mountpoint for Amazon S3. Use AWS Backup to replicate objects to another Region - While Amazon S3 is durable and supports cross-Region replication, it is an object storage service, not a file system. It lacks POSIX compliance even when used with Mountpoint for Amazon S3. So, this option is incorrect.
- (I) References:
- (J) https://docs.aws.amazon.com/aws-backup/latest/devguide/cross-region-backup.html
- () https://docs.aws.amazon.com/aws-backup/latest/devguide/backup-feature-availability.html#features-by-resource
- () https://aws.amazon.com/blogs/aws/mountpoint-for-amazon-s3-generally-available-and-ready-for-production-workloads/
- () https://www.amazonaws.cn/en/fsx/lustre/faqs/#Availability_and_durability
- () https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/what-is-fsx-ontap.html
- () A big data analytics company is using Amazon Kinesis Data Streams (KDS) to process IoT data from the field devices of an agricultural sciences company. Multiple consumer applications are using the incoming data streams and the engineers have noticed a performance lag for the data delivery speed between producers and consumers of the data streams.

**Answer:**
Correct Answer: **Use Amazon Elastic File System (Amazon EFS) with the Standard storage class and configure AWS Backup to create cross-Region backups on a scheduled basis**

---

## Question 119

**Q:** As a solutions architect, which of the following would you recommend for improving the performance for the given use-case?

**Options:**
- (A) Swap out Amazon Kinesis Data Streams with Amazon Kinesis Data Firehose
- **(B) Use Enhanced Fanout feature of Amazon Kinesis Data Streams** [CORRECT]
- (C) Swap out Amazon Kinesis Data Streams with Amazon SQS Standard queues
- (D) Swap out Amazon Kinesis Data Streams with Amazon SQS FIFO queues
- (E) Correct option:
- (F) Amazon Kinesis Data Streams (KDS) is a massively scalable and durable real-time data streaming service. KDS can continuously capture gigabytes of data per second from hundreds of thousands of sources such as website clickstreams, database event streams, financial transactions, social media feeds, IT logs, and location-tracking events.
- (G) By default, the 2MB/second/shard output is shared between all of the applications consuming data from the stream. You should use enhanced fan-out if you have multiple consumers retrieving data from a stream in parallel. With enhanced fan-out developers can register stream consumers to use enhanced fan-out and receive their own 2MB/second pipe of read throughput per shard, and this throughput automatically scales with the number of shards in a stream.
- (H) Amazon Kinesis Data Streams Fanout:
- (I) via - https://aws.amazon.com/blogs/aws/kds-enhanced-fanout/
- (J) Incorrect options:
- () Exam Alert:
- () via - https://aws.amazon.com/kinesis/data-streams/faqs/
- () References:
- () https://aws.amazon.com/blogs/aws/kds-enhanced-fanout/
- () https://aws.amazon.com/kinesis/data-streams/faqs/
- () A media company is evaluating the possibility of moving its IT infrastructure to the AWS Cloud. The company needs at least 10 terabytes of storage with the maximum possible I/O performance for processing certain files which are mostly large videos. The company also needs close to 450 terabytes of very durable storage for storing media content and almost double of it, i.e. 900 terabytes for archival of legacy data.

**Answer:**
Correct Answer: **Use Enhanced Fanout feature of Amazon Kinesis Data Streams**

---

## Question 120

**Q:** As a Solutions Architect, which set of services will you recommend to meet these requirements?

**Options:**
- (A) Amazon EBS for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage
- (B) Amazon EC2 instance store for maximum performance, AWS Storage Gateway for on-premises durable data access and Amazon S3 Glacier Deep Archive for archival storage
- **(C) Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage** [CORRECT]
- (D) Amazon S3 standard storage for maximum performance, Amazon S3 Intelligent-Tiering for intelligent, durable storage, and Amazon S3 Glacier Deep Archive for archival storage
- (E) Correct option:
- (F) An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer. Instance store is ideal for the temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers.
- (G) You can specify instance store volumes for an instance only when you launch it. You can't detach an instance store volume from one instance and attach it to a different instance.
- (H) Some instance types use NVMe or SATA-based solid-state drives (SSD) to deliver high random I/O performance. This is a good option when you need storage with very low latency, but you don't need the data to persist when the instance terminates or you can take advantage of fault-tolerant architectures.
- (I) Amazon S3 Standard offers high durability, availability, and performance object storage for frequently accessed data. Because it delivers low latency and high throughput, Amazon S3 Standard is appropriate for a wide variety of use cases, including cloud applications, dynamic websites, content distribution, mobile and gaming applications, and big data analytics.
- (J) Incorrect options:
- () Amazon S3 standard storage for maximum performance, Amazon S3 Intelligent-Tiering for intelligent, durable storage, and Amazon S3 Glacier Deep Archive for archival storage - Amazon EC2 instance store volumes provide the best I/O performance for low latency requirement, as in the current use case. The Amazon S3 Intelligent-Tiering storage class is designed to optimize costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead.
- () Amazon S3 Glacier Deep Archive is Amazon S3’s lowest-cost storage class and supports long-term retention and digital preservation for data that may be accessed once or twice a year. It is designed for customers — particularly those in highly-regulated industries, such as the Financial Services, Healthcare, and Public Sectors — that retain data sets for 7-10 years or longer to meet regulatory compliance requirements.
- () Reference:
- () https://aws.amazon.com/s3/storage-classes/
- () The engineering team at a weather tracking company wants to enhance the performance of its relational database and is looking for a caching solution that supports geospatial data.

**Answer:**
Correct Answer: **Amazon EC2 instance store for maximum performance, Amazon S3 for durable data storage, and Amazon S3 Glacier for archival storage**

---

## Question 121

**Q:** As a solutions architect, which of the following solutions will you suggest?

**Options:**
- (A) Use Amazon ElastiCache for Redis
- (B) Use Amazon ElastiCache for Memcached
- (C) Use AWS Global Accelerator
- (D) Use Amazon DynamoDB Accelerator (DAX)
- (E) Correct option:
- (F) Redis has purpose-built commands for working with real-time geospatial data at scale. You can perform operations like finding the distance between two elements (for example people or places) and finding all elements within a given distance of a point.
- (G) Incorrect options:
- (H) Use Amazon ElastiCache for Memcached - Both Redis and MemCached are in-memory, open-source data stores. Memcached, a high-performance distributed memory cache service, is designed for simplicity while Redis offers a rich set of features that make it effective for a wide range of use cases. Memcached does not offer support for geospatial data.
- (I) via - https://aws.amazon.com/elasticache/redis-vs-memcached/
- (J) Use Amazon DynamoDB Accelerator (DAX) - Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for Amazon DynamoDB. DAX does not support relational databases.
- () Use AWS Global Accelerator - AWS Global Accelerator is a networking service that helps you improve the availability and performance of the applications that you offer to your global users. This option has been added as a distractor, it has nothing to do with database caching.
- () Reference:
- () https://aws.amazon.com/elasticache/redis-vs-memcached/
- () Which approach best meets the requirements while minimizing costs?
- () Configure an Amazon EventBridge rule to monitor system-level metrics from the EC2 instance. Trigger a Lambda function to re-deploy the application in a different Availability Zone when CPU utilization exceeds 70%
- () Build an Amazon Machine Image (AMI) from the existing EC2 instance and configure a launch template. Create an Auto Scaling group using the launch template with Spot Instance pricing enabled. Attach an Application Load Balancer to distribute traffic across dynamically launched instances
- () Clone the EC2 instance using an AMI and launch a second On-Demand instance. Register both instances with an Application Load Balancer to distribute incoming traffic evenly
- () Containerize the application using Amazon ECS with Fargate launch type. Deploy the container to a single Fargate task and set a CloudWatch alarm to increase memory and CPU allocation dynamically based on load
- () This approach leverages EC2 Auto Scaling to automatically scale the number of instances based on demand while using Spot Instances to minimize compute costs. The application’s stateless design is ideal for this setup. The Application Load Balancer distributes traffic across healthy instances. Using a launch template with an AMI ensures consistency across instances. This solution balances scalability with cost efficiency and aligns with AWS best practices for elastic, stateless workloads.
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/which-fleet-method-to-use.html
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/launch-template-spot-instances.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/which-fleet-method-to-use.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/launch-instances-from-launch-template.html#launch-templates-spot-fleet
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html
- () How will you resolve the issue and make sure it doesn't happen again?
- () Disable the Termination from the Auto Scaling Group any time a user reports an issue
- **() Install an Amazon CloudWatch Logs agents on the Amazon EC2 instances to send logs to Amazon CloudWatch** [CORRECT]
- () Use AWS Lambda to regularly SSH into the Amazon EC2 instances and copy the log files to Amazon S3
- () Make a snapshot of the Amazon EC2 instance just before it gets terminated

**Answer:**
Correct Answer: **Install an Amazon CloudWatch Logs agents on the Amazon EC2 instances to send logs to Amazon CloudWatch**

---

## Question 122

**Q:** Which approach best meets the requirements while minimizing costs?

**Options:**
- (A) Configure an Amazon EventBridge rule to monitor system-level metrics from the EC2 instance. Trigger a Lambda function to re-deploy the application in a different Availability Zone when CPU utilization exceeds 70%
- (B) Build an Amazon Machine Image (AMI) from the existing EC2 instance and configure a launch template. Create an Auto Scaling group using the launch template with Spot Instance pricing enabled. Attach an Application Load Balancer to distribute traffic across dynamically launched instances
- (C) Clone the EC2 instance using an AMI and launch a second On-Demand instance. Register both instances with an Application Load Balancer to distribute incoming traffic evenly
- (D) Containerize the application using Amazon ECS with Fargate launch type. Deploy the container to a single Fargate task and set a CloudWatch alarm to increase memory and CPU allocation dynamically based on load
- (E) Correct option:
- (F) This approach leverages EC2 Auto Scaling to automatically scale the number of instances based on demand while using Spot Instances to minimize compute costs. The application’s stateless design is ideal for this setup. The Application Load Balancer distributes traffic across healthy instances. Using a launch template with an AMI ensures consistency across instances. This solution balances scalability with cost efficiency and aligns with AWS best practices for elastic, stateless workloads.
- (G) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/which-fleet-method-to-use.html
- (H) Incorrect options:
- (I) References:
- (J) https://docs.aws.amazon.com/autoscaling/ec2/userguide/launch-template-spot-instances.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/which-fleet-method-to-use.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/launch-instances-from-launch-template.html#launch-templates-spot-fleet
- () https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html
- () How will you resolve the issue and make sure it doesn't happen again?
- () Disable the Termination from the Auto Scaling Group any time a user reports an issue
- **() Install an Amazon CloudWatch Logs agents on the Amazon EC2 instances to send logs to Amazon CloudWatch** [CORRECT]
- () Use AWS Lambda to regularly SSH into the Amazon EC2 instances and copy the log files to Amazon S3
- () Make a snapshot of the Amazon EC2 instance just before it gets terminated
- () You can use the Amazon CloudWatch Logs agent installer on an existing Amazon EC2 instance to install and configure the Amazon CloudWatch Logs agent. After installation is complete, logs automatically flow from the instance to the log stream you create while installing the agent. The agent confirms that it has started and it stays running until you disable it.
- () Here, the natural and by far the easiest solution would be to use the Amazon CloudWatch Logs agents on the Amazon EC2 instances to automatically send log files into Amazon CloudWatch, so we can analyze them in the future easily should any problem arise.
- () Disable the Termination from the Auto Scaling Group any time a user reports an issue - Disabling the Termination from the Auto Scaling Group would prevent our Auto Scaling Group from being Elastic and impact our costs. Therefore this option is incorrect.
- () Make a snapshot of the Amazon EC2 instance just before it gets terminated - Making a snapshot of the Amazon EC2 instance before it gets terminated could work but it's tedious, not elastic and very expensive, since our interest is just the log files. Therefore this option is not the best fit for the given use-case.
- () You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are incremental backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved. This minimizes the time required to create the snapshot and saves on storage costs by not duplicating data.
- () Use AWS Lambda to regularly SSH into the Amazon EC2 instances and copy the log files to Amazon S3 - AWS Lambda lets you run code without provisioning or managing servers. It cannot be used for production-grade serverless log analytics. Using AWS Lambda would be extremely hard to use for this task. Therefore this option is not the best fit for the given use-case.
- () Reference:
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/QuickStartEC2Instance.html
- () Which solution will best meet the new compliance and operational requirements? (Select two)
- () Use Amazon CloudWatch Logs Insights to monitor patching success and then manually adjust ALB target group registrations before and after each patch window
- () Modify the load balancer configuration to attach EC2 instances using instance ID-based target groups instead of IP-based targets, allowing Systems Manager to directly communicate with instance metadata
- () Correct selection
- () Use AWS Systems Manager Automation with the AWSEC2-PatchLoadBalancerInstance document to manage patching
- () Configure Systems Manager Maintenance Windows to coordinate patching and instance removal from the ALB during the defined window
- () Configure a custom Lambda function triggered by an Amazon EventBridge rule that disables the EC2 instance's network interface during the patching window and re-enables it after patching completes
- () Correct options:

**Answer:**
Correct Answer: **Install an Amazon CloudWatch Logs agents on the Amazon EC2 instances to send logs to Amazon CloudWatch**

---

## Question 123

**Q:** How will you resolve the issue and make sure it doesn't happen again?

**Options:**
- (A) Disable the Termination from the Auto Scaling Group any time a user reports an issue
- (B) Install an Amazon CloudWatch Logs agents on the Amazon EC2 instances to send logs to Amazon CloudWatch
- (C) Use AWS Lambda to regularly SSH into the Amazon EC2 instances and copy the log files to Amazon S3
- (D) Make a snapshot of the Amazon EC2 instance just before it gets terminated
- (E) Correct option:
- (F) You can use the Amazon CloudWatch Logs agent installer on an existing Amazon EC2 instance to install and configure the Amazon CloudWatch Logs agent. After installation is complete, logs automatically flow from the instance to the log stream you create while installing the agent. The agent confirms that it has started and it stays running until you disable it.
- (G) Here, the natural and by far the easiest solution would be to use the Amazon CloudWatch Logs agents on the Amazon EC2 instances to automatically send log files into Amazon CloudWatch, so we can analyze them in the future easily should any problem arise.
- (H) Incorrect options:
- (I) Disable the Termination from the Auto Scaling Group any time a user reports an issue - Disabling the Termination from the Auto Scaling Group would prevent our Auto Scaling Group from being Elastic and impact our costs. Therefore this option is incorrect.
- (J) Make a snapshot of the Amazon EC2 instance just before it gets terminated - Making a snapshot of the Amazon EC2 instance before it gets terminated could work but it's tedious, not elastic and very expensive, since our interest is just the log files. Therefore this option is not the best fit for the given use-case.
- () You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are incremental backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved. This minimizes the time required to create the snapshot and saves on storage costs by not duplicating data.
- () Use AWS Lambda to regularly SSH into the Amazon EC2 instances and copy the log files to Amazon S3 - AWS Lambda lets you run code without provisioning or managing servers. It cannot be used for production-grade serverless log analytics. Using AWS Lambda would be extremely hard to use for this task. Therefore this option is not the best fit for the given use-case.
- () Reference:
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/QuickStartEC2Instance.html
- () Which solution will best meet the new compliance and operational requirements? (Select two)
- () Use Amazon CloudWatch Logs Insights to monitor patching success and then manually adjust ALB target group registrations before and after each patch window
- () Modify the load balancer configuration to attach EC2 instances using instance ID-based target groups instead of IP-based targets, allowing Systems Manager to directly communicate with instance metadata
- () Correct selection
- () Use AWS Systems Manager Automation with the AWSEC2-PatchLoadBalancerInstance document to manage patching
- () Configure Systems Manager Maintenance Windows to coordinate patching and instance removal from the ALB during the defined window
- () Configure a custom Lambda function triggered by an Amazon EventBridge rule that disables the EC2 instance's network interface during the patching window and re-enables it after patching completes
- () Correct options:
- () The AWSEC2-PatchLoadBalancerInstance Systems Manager Automation document is specifically designed for patching EC2 instances that are part of a load balancer. It automatically removes the instance from the ALB target group, waits for in-flight requests to complete, applies patches, performs reboots if needed, and then safely re-registers the instance. This workflow prevents application downtime or request failures during patching and ensures compliance with security policies.
- () Systems Manager Maintenance Windows can be configured to run Automation documents or Lambda functions at precise times. You can schedule a task to remove instances from the load balancer using pre-defined documents (such as AWSEC2-PatchLoadBalancerInstance) and then re-register them once patching is complete. This offers fine-grained scheduling and orchestration for controlled patching without disrupting traffic.
- () References:
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html
- () https://docs.aws.amazon.com/systems-manager-automation-runbooks/latest/userguide/automation-awsec2-patch-load-balancer-instance.html
- () https://docs.aws.amazon.com/systems-manager-automation-runbooks/latest/userguide/automation-runbook-reference.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html
- () You are a cloud architect at an IT company. The company has multiple enterprise customers that manage their own mobile applications that capture and send data to Amazon Kinesis Data Streams. They have been getting a ProvisionedThroughputExceededException exception. You have been contacted to help and upon analysis, you notice that messages are being sent one by one at a high rate.
- () Which of the following options will help with the exception while keeping costs at a minimum?
- () Increase the number of shards
- () Use Exponential Backoff
- **() Use batch messages** [CORRECT]
- () Decrease the Stream retention duration

**Answer:**
Correct Answer: **Use batch messages**

---

## Question 124

**Q:** Which solution will best meet the new compliance and operational requirements? (Select two)

**Options:**
- (A) Use Amazon CloudWatch Logs Insights to monitor patching success and then manually adjust ALB target group registrations before and after each patch window
- (B) Modify the load balancer configuration to attach EC2 instances using instance ID-based target groups instead of IP-based targets, allowing Systems Manager to directly communicate with instance metadata
- (C) Correct selection
- (D) Use AWS Systems Manager Automation with the AWSEC2-PatchLoadBalancerInstance document to manage patching
- (E) Configure Systems Manager Maintenance Windows to coordinate patching and instance removal from the ALB during the defined window
- (F) Configure a custom Lambda function triggered by an Amazon EventBridge rule that disables the EC2 instance's network interface during the patching window and re-enables it after patching completes
- (G) Correct options:
- (H) The AWSEC2-PatchLoadBalancerInstance Systems Manager Automation document is specifically designed for patching EC2 instances that are part of a load balancer. It automatically removes the instance from the ALB target group, waits for in-flight requests to complete, applies patches, performs reboots if needed, and then safely re-registers the instance. This workflow prevents application downtime or request failures during patching and ensures compliance with security policies.
- (I) Systems Manager Maintenance Windows can be configured to run Automation documents or Lambda functions at precise times. You can schedule a task to remove instances from the load balancer using pre-defined documents (such as AWSEC2-PatchLoadBalancerInstance) and then re-register them once patching is complete. This offers fine-grained scheduling and orchestration for controlled patching without disrupting traffic.
- (J) Incorrect options:
- () References:
- () https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html
- () https://docs.aws.amazon.com/systems-manager-automation-runbooks/latest/userguide/automation-awsec2-patch-load-balancer-instance.html
- () https://docs.aws.amazon.com/systems-manager-automation-runbooks/latest/userguide/automation-runbook-reference.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html
- () You are a cloud architect at an IT company. The company has multiple enterprise customers that manage their own mobile applications that capture and send data to Amazon Kinesis Data Streams. They have been getting a ProvisionedThroughputExceededException exception. You have been contacted to help and upon analysis, you notice that messages are being sent one by one at a high rate.
- () Which of the following options will help with the exception while keeping costs at a minimum?
- () Increase the number of shards
- () Use Exponential Backoff
- **() Use batch messages** [CORRECT]
- () Decrease the Stream retention duration
- () Correct option:
- () Amazon Kinesis Data Streams Overview:
- () via - https://aws.amazon.com/kinesis/data-streams/
- () When a host needs to send many records per second (RPS) to Amazon Kinesis, simply calling the basic PutRecord API action in a loop is inadequate. To reduce overhead and increase throughput, the application must batch records and implement parallel HTTP requests. This will increase the efficiency overall and ensure you are optimally using the shards.
- () Use Exponential Backoff - While this may help in the short term, as soon as the request rate increases, you will see the ProvisionedThroughputExceededException exception again.
- () Increase the number of shards - Increasing shards could be a short term fix but will substantially increase the cost, so this option is ruled out.
- () Decrease the Stream retention duration - This operation may result in data loss and won't help with the exceptions, so this option is incorrect.
- () https://aws.amazon.com/blogs/big-data/implementing-efficient-and-reliable-producers-with-the-amazon-kinesis-producer-library/
- () https://aws.amazon.com/kinesis/data-streams/
- () While troubleshooting, a cloud architect realized that the Amazon EC2 instance is unable to connect to the internet using the Internet Gateway.
- () Which conditions should be met for internet connectivity to be established? (Select two)
- () The instance's subnet is associated with multiple route tables with conflicting configurations
- () The subnet has been configured to be public and has no access to the internet
- () The network access control list (network ACL) associated with the subnet must have rules to allow inbound and outbound traffic
- () The route table in the instance’s subnet should have a route to an Internet Gateway

**Answer:**
Correct Answer: **Use batch messages**

---

## Question 125

**Q:** Which of the following options will help with the exception while keeping costs at a minimum?

**Options:**
- (A) Increase the number of shards
- (B) Use Exponential Backoff
- (C) Use batch messages
- (D) Decrease the Stream retention duration
- (E) Correct option:
- (F) Amazon Kinesis Data Streams Overview:
- (G) via - https://aws.amazon.com/kinesis/data-streams/
- (H) When a host needs to send many records per second (RPS) to Amazon Kinesis, simply calling the basic PutRecord API action in a loop is inadequate. To reduce overhead and increase throughput, the application must batch records and implement parallel HTTP requests. This will increase the efficiency overall and ensure you are optimally using the shards.
- (I) Incorrect options:
- (J) Use Exponential Backoff - While this may help in the short term, as soon as the request rate increases, you will see the ProvisionedThroughputExceededException exception again.
- () Increase the number of shards - Increasing shards could be a short term fix but will substantially increase the cost, so this option is ruled out.
- () Decrease the Stream retention duration - This operation may result in data loss and won't help with the exceptions, so this option is incorrect.
- () References:
- () https://aws.amazon.com/blogs/big-data/implementing-efficient-and-reliable-producers-with-the-amazon-kinesis-producer-library/
- () https://aws.amazon.com/kinesis/data-streams/
- () While troubleshooting, a cloud architect realized that the Amazon EC2 instance is unable to connect to the internet using the Internet Gateway.
- () Which conditions should be met for internet connectivity to be established? (Select two)
- () The instance's subnet is associated with multiple route tables with conflicting configurations
- () The subnet has been configured to be public and has no access to the internet
- () Correct selection
- () The network access control list (network ACL) associated with the subnet must have rules to allow inbound and outbound traffic
- () The route table in the instance’s subnet should have a route to an Internet Gateway
- () The instance's subnet is not associated with any route table
- () Correct options:
- () The network access control list (network ACL) that is associated with the subnet must have rules to allow inbound and outbound traffic on port 80 (for HTTP traffic) and port 443 (for HTTPs traffic). This is a necessary condition for Internet Gateway connectivity.
- () A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed. The route table in the instance’s subnet should have a route defined to the Internet Gateway.
- () The instance's subnet is not associated with any route table - This is an incorrect statement. A subnet is implicitly associated with the main route table if it is not explicitly associated with a particular route table. So, a subnet is always associated with some route table.
- () The instance's subnet is associated with multiple route tables with conflicting configurations - This is an incorrect statement. A subnet can only be associated with one route table at a time.
- () The subnet has been configured to be public and has no access to the internet - This is an incorrect statement. Public subnets have access to the internet via Internet Gateway.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html
- () The data engineering team at an e-commerce company has set up a workflow to ingest the clickstream data into the raw zone of the Amazon S3 data lake. The team wants to run some SQL based data sanity checks on the raw zone of the data lake.
- () What AWS services would you recommend for this use-case such that the solution is cost-effective and easy to maintain?
- () Load the incremental raw zone data into Amazon Redshift on an hourly basis and run the SQL based sanity checks
- () Load the incremental raw zone data into an Amazon EMR based Spark Cluster on an hourly basis and use SparkSQL to run the SQL based sanity checks
- () Load the incremental raw zone data into Amazon RDS on an hourly basis and run the SQL based sanity checks
- **() Use Amazon Athena to run SQL based analytics against Amazon S3 data** [CORRECT]
- () Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon S3 using standard SQL. Amazon Athena is serverless, so there is no infrastructure to set up or manage, and customers pay only for the queries they run. You can use Athena to process logs, perform ad-hoc analysis, and run interactive queries.

**Answer:**
Correct Answer: **Use Amazon Athena to run SQL based analytics against Amazon S3 data**

---

## Question 126

**Q:** Which conditions should be met for internet connectivity to be established? (Select two)

**Options:**
- (A) The instance's subnet is associated with multiple route tables with conflicting configurations
- (B) The subnet has been configured to be public and has no access to the internet
- (C) Correct selection
- (D) The network access control list (network ACL) associated with the subnet must have rules to allow inbound and outbound traffic
- (E) The route table in the instance’s subnet should have a route to an Internet Gateway
- (F) The instance's subnet is not associated with any route table
- (G) Correct options:
- (H) The network access control list (network ACL) that is associated with the subnet must have rules to allow inbound and outbound traffic on port 80 (for HTTP traffic) and port 443 (for HTTPs traffic). This is a necessary condition for Internet Gateway connectivity.
- (I) A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed. The route table in the instance’s subnet should have a route defined to the Internet Gateway.
- (J) Incorrect options:
- () The instance's subnet is not associated with any route table - This is an incorrect statement. A subnet is implicitly associated with the main route table if it is not explicitly associated with a particular route table. So, a subnet is always associated with some route table.
- () The instance's subnet is associated with multiple route tables with conflicting configurations - This is an incorrect statement. A subnet can only be associated with one route table at a time.
- () The subnet has been configured to be public and has no access to the internet - This is an incorrect statement. Public subnets have access to the internet via Internet Gateway.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html
- () The data engineering team at an e-commerce company has set up a workflow to ingest the clickstream data into the raw zone of the Amazon S3 data lake. The team wants to run some SQL based data sanity checks on the raw zone of the data lake.
- () What AWS services would you recommend for this use-case such that the solution is cost-effective and easy to maintain?
- () Load the incremental raw zone data into Amazon Redshift on an hourly basis and run the SQL based sanity checks
- () Load the incremental raw zone data into an Amazon EMR based Spark Cluster on an hourly basis and use SparkSQL to run the SQL based sanity checks
- () Load the incremental raw zone data into Amazon RDS on an hourly basis and run the SQL based sanity checks
- () Use Amazon Athena to run SQL based analytics against Amazon S3 data
- () Correct option:
- () Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon S3 using standard SQL. Amazon Athena is serverless, so there is no infrastructure to set up or manage, and customers pay only for the queries they run. You can use Athena to process logs, perform ad-hoc analysis, and run interactive queries.
- () Amazon Athena Benefits:
- () via - https://aws.amazon.com/athena/
- () Load the incremental raw zone data into Amazon Redshift on an hourly basis and run the SQL based sanity checks - Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis. As the development team would have to maintain and monitor the Amazon Redshift cluster size and would require significant development time to set up the processes to consume the data periodically, so this option is ruled out.
- () Load the incremental raw zone data into Amazon RDS on an hourly basis and run the SQL based sanity checks - Loading the incremental data into Amazon RDS implies data migration jobs will have to be written via a AWS Lambda function or an Amazon EC2 based process. This goes against the requirement that the solution should involve the least amount of development effort and ongoing maintenance. Hence this option is not correct.
- () https://aws.amazon.com/athena/
- () A digital content production company has transitioned all of its media assets to Amazon S3 in an effort to reduce storage costs. However, the rendering engine used in production continues to run in an on-premises data center and requires frequent and low-latency access to large media files. The company wants to implement a storage solution that maintains application performance while keeping costs low.
- () Which approach should the company choose to meet these requirements in the most cost-effective way?
- () Use Mountpoint for Amazon S3 on the on-premises rendering servers to facilitate low-latency access to the S3 bucket
- () Set up a dedicated on-premises storage array that periodically fetches data from Amazon S3 using a custom-built application. Mount this storage volume on the rendering servers as their primary working directory
- () Deploy an Amazon FSx for Lustre file system and sync media data from Amazon S3 into it using DataSync. Mount the FSx file system on the on-premises render servers using a VPN tunnel
- **() Set up an Amazon S3 File Gateway to provide storage for the on-premises application** [CORRECT]
- () Amazon S3 File Gateway is designed specifically for on-premises applications that need low-latency access to S3 data. It caches frequently accessed data locally and exposes the S3 bucket as an NFS or SMB file share, making it ideal for performance-sensitive workloads like rendering. It is also cost-effective as the majority of data remains in S3.
- () via - https://docs.aws.amazon.com/filegateway/latest/files3/what-is-file-s3.html

**Answer:**
Correct Answer: **Set up an Amazon S3 File Gateway to provide storage for the on-premises application**

---

## Question 127

**Q:** What AWS services would you recommend for this use-case such that the solution is cost-effective and easy to maintain?

**Options:**
- (A) Load the incremental raw zone data into Amazon Redshift on an hourly basis and run the SQL based sanity checks
- (B) Load the incremental raw zone data into an Amazon EMR based Spark Cluster on an hourly basis and use SparkSQL to run the SQL based sanity checks
- (C) Load the incremental raw zone data into Amazon RDS on an hourly basis and run the SQL based sanity checks
- (D) Use Amazon Athena to run SQL based analytics against Amazon S3 data
- (E) Correct option:
- (F) Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon S3 using standard SQL. Amazon Athena is serverless, so there is no infrastructure to set up or manage, and customers pay only for the queries they run. You can use Athena to process logs, perform ad-hoc analysis, and run interactive queries.
- (G) Amazon Athena Benefits:
- (H) via - https://aws.amazon.com/athena/
- (I) Incorrect options:
- (J) Load the incremental raw zone data into Amazon Redshift on an hourly basis and run the SQL based sanity checks - Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis. As the development team would have to maintain and monitor the Amazon Redshift cluster size and would require significant development time to set up the processes to consume the data periodically, so this option is ruled out.
- () Load the incremental raw zone data into Amazon RDS on an hourly basis and run the SQL based sanity checks - Loading the incremental data into Amazon RDS implies data migration jobs will have to be written via a AWS Lambda function or an Amazon EC2 based process. This goes against the requirement that the solution should involve the least amount of development effort and ongoing maintenance. Hence this option is not correct.
- () Reference:
- () https://aws.amazon.com/athena/
- () A digital content production company has transitioned all of its media assets to Amazon S3 in an effort to reduce storage costs. However, the rendering engine used in production continues to run in an on-premises data center and requires frequent and low-latency access to large media files. The company wants to implement a storage solution that maintains application performance while keeping costs low.
- () Which approach should the company choose to meet these requirements in the most cost-effective way?
- () Use Mountpoint for Amazon S3 on the on-premises rendering servers to facilitate low-latency access to the S3 bucket
- () Set up a dedicated on-premises storage array that periodically fetches data from Amazon S3 using a custom-built application. Mount this storage volume on the rendering servers as their primary working directory
- () Deploy an Amazon FSx for Lustre file system and sync media data from Amazon S3 into it using DataSync. Mount the FSx file system on the on-premises render servers using a VPN tunnel
- () Set up an Amazon S3 File Gateway to provide storage for the on-premises application
- () Amazon S3 File Gateway is designed specifically for on-premises applications that need low-latency access to S3 data. It caches frequently accessed data locally and exposes the S3 bucket as an NFS or SMB file share, making it ideal for performance-sensitive workloads like rendering. It is also cost-effective as the majority of data remains in S3.
- () via - https://docs.aws.amazon.com/filegateway/latest/files3/what-is-file-s3.html
- () References:
- () https://docs.aws.amazon.com/filegateway/latest/files3/what-is-file-s3.html
- () https://aws.amazon.com/blogs/aws/mountpoint-for-amazon-s3-generally-available-and-ready-for-production-workloads/
- () A data analytics team at a global media firm is building a new analytics platform to process large volumes of both historical and real-time data. This data is stored in Amazon S3. The team wants to implement a serverless solution that allows them to query the data directly using SQL. Additionally, the solution must ensure that all data is encrypted at rest and automatically replicated to another AWS Region to support business continuity.
- () Which solution will meet these requirements with the LEAST operational overhead?
- **() Create an Amazon S3 bucket configured with server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Athena to run SQL queries on the data** [CORRECT]
- () Enable Cross-Region Replication (CRR) on the existing Amazon S3 bucket. Apply server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Use Amazon Athena to run SQL queries on the replicated data
- () Enable Cross-Region Replication (CRR) on the existing Amazon S3 bucket. Apply server-side encryption using Amazon S3 managed keys (SSE-S3). Use Amazon Athena to run SQL queries on the replicated data
- () Create an Amazon S3 bucket configured with server-side encryption using Amazon S3 managed keys (SSE-S3). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Redshift Spectrum to query the S3 data using SQL
- () via - https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html

**Answer:**
Correct Answer: **Create an Amazon S3 bucket configured with server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Athena to run SQL queries on the data**

---

## Question 128

**Q:** Which approach should the company choose to meet these requirements in the most cost-effective way?

**Options:**
- (A) Use Mountpoint for Amazon S3 on the on-premises rendering servers to facilitate low-latency access to the S3 bucket
- (B) Set up a dedicated on-premises storage array that periodically fetches data from Amazon S3 using a custom-built application. Mount this storage volume on the rendering servers as their primary working directory
- (C) Deploy an Amazon FSx for Lustre file system and sync media data from Amazon S3 into it using DataSync. Mount the FSx file system on the on-premises render servers using a VPN tunnel
- (D) Set up an Amazon S3 File Gateway to provide storage for the on-premises application
- (E) Correct option:
- (F) Amazon S3 File Gateway is designed specifically for on-premises applications that need low-latency access to S3 data. It caches frequently accessed data locally and exposes the S3 bucket as an NFS or SMB file share, making it ideal for performance-sensitive workloads like rendering. It is also cost-effective as the majority of data remains in S3.
- (G) via - https://docs.aws.amazon.com/filegateway/latest/files3/what-is-file-s3.html
- (H) Incorrect options:
- (I) References:
- (J) https://docs.aws.amazon.com/filegateway/latest/files3/what-is-file-s3.html
- () https://aws.amazon.com/blogs/aws/mountpoint-for-amazon-s3-generally-available-and-ready-for-production-workloads/
- () A data analytics team at a global media firm is building a new analytics platform to process large volumes of both historical and real-time data. This data is stored in Amazon S3. The team wants to implement a serverless solution that allows them to query the data directly using SQL. Additionally, the solution must ensure that all data is encrypted at rest and automatically replicated to another AWS Region to support business continuity.
- () Which solution will meet these requirements with the LEAST operational overhead?
- () Create an Amazon S3 bucket configured with server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Athena to run SQL queries on the data
- () Enable Cross-Region Replication (CRR) on the existing Amazon S3 bucket. Apply server-side encryption using AWS KMS multi-Region keys (SSE-KMS). Use Amazon Athena to run SQL queries on the replicated data
- () Enable Cross-Region Replication (CRR) on the existing Amazon S3 bucket. Apply server-side encryption using Amazon S3 managed keys (SSE-S3). Use Amazon Athena to run SQL queries on the replicated data
- () Create an Amazon S3 bucket configured with server-side encryption using Amazon S3 managed keys (SSE-S3). Enable cross-Region replication (CRR) on the source bucket. Use Amazon Redshift Spectrum to query the S3 data using SQL
- () via - https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html
- () Both of these options skip the step of creating a new bucket in the target AWS Region. You cannot enable CRR on a bucket without specifying the target bucket for replication in another Region. So, these options are incorrect.
- () https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/replication.html
- () https://docs.aws.amazon.com/athena/latest/ug/what-is.html
- () An enterprise runs a critical Oracle database workload in its on-premises environment. The company now plans to replicate both existing records and continuous transactional changes to a managed Oracle environment in AWS. The target database will run on Amazon RDS for Oracle. Data transfer volume is expected to fluctuate throughout the day, and the team wants the solution to provision compute resources automatically based on actual workload requirements.
- () Which solution will meet these requirements?
- () Deploy the AWS DMS replication instance on Amazon EC2. Configure the instance with custom scripts that monitor CPU usage and resize the instance using EC2 Auto Scaling policies.
- () Use AWS Glue to extract data from the on-premises Oracle database and write the output to Amazon RDS for Oracle. Configure Glue to run on demand when changes are detected
- () Use AWS Lambda to capture change data from the on-premises Oracle database. Trigger Lambda functions to write the updates to Amazon RDS for Oracle in real time.
- **() Configure an AWS DMS Serverless replication task to synchronize historical and ongoing changes between the on-premises Oracle database and Amazon RDS for Oracle** [CORRECT]
- () AWS DMS Serverless is designed specifically for scenarios like this — where data replication workloads vary and automation is required. AWS DMS Serverless automatically provisions and scales compute resources based on workload demand. It supports ongoing replication, including change data capture (CDC), and is fully managed, reducing operational complexity. This solution avoids the need to guess capacity requirements or manually adjust instance sizes.

**Answer:**
Correct Answer: **Configure an AWS DMS Serverless replication task to synchronize historical and ongoing changes between the on-premises Oracle database and Amazon RDS for Oracle**

---

## Question 129

**Q:** Which solution will fulfill these needs in the most cost-efficient manner?

**Options:**
- (A) Create separate DynamoDB tables in multiple Regions. Use AWS Data Pipeline to synchronize data periodically between Regions to maintain availability
- **(B) Use DynamoDB global tables for automatic multi-Region replication. Enable provisioned capacity mode with auto scaling to optimize cost and ensure consistent availability** [CORRECT]
- (C) Enable DynamoDB Accelerator (DAX) to reduce response time for read operations. Deploy DAX in one Region, and use scheduled Lambda functions to replicate data to other Regions
- (D) Deploy separate DynamoDB tables in each required AWS Region using on-demand capacity mode. Implement a custom cross-Region replication mechanism by streaming data changes with DynamoDB Streams and processing them through AWS Lambda functions
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GlobalTables.html
- (I) https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/V2globaltables_HowItWorks.html
- (J) https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html
- () A media company wants to get out of the business of owning and maintaining its own IT infrastructure. As part of this digital transformation, the media company wants to archive about 5 petabytes of data in its on-premises data center to durable long term storage.

**Answer:**
Correct Answer: **Use DynamoDB global tables for automatic multi-Region replication. Enable provisioned capacity mode with auto scaling to optimize cost and ensure consistent availability**

---

## Question 130

**Q:** As a solutions architect, what is your recommendation to migrate this data in the MOST cost-optimal way?

**Options:**
- (A) Setup AWS Site-to-Site VPN connection between the on-premises data center and AWS Cloud. Use this connection to transfer the data into Amazon S3 Glacier
- (B) Transfer the on-premises data into multiple AWS Snowball Edge Storage Optimized devices. Copy the AWS Snowball Edge data into Amazon S3 Glacier
- (C) Transfer the on-premises data into multiple AWS Snowball Edge Storage Optimized devices. Copy the AWS Snowball Edge data into Amazon S3 and create a lifecycle policy to transition the data into Amazon S3 Glacier
- (D) Setup AWS direct connect between the on-premises data center and AWS Cloud. Use this connection to transfer the data into Amazon S3 Glacier
- (E) Correct option:
- (F) Incorrect options:
- (G) Transfer the on-premises data into multiple AWS Snowball Edge Storage Optimized devices. Copy the AWS Snowball Edge data into Amazon S3 Glacier - As mentioned earlier, you can't directly copy data from AWS Snowball Edge devices into Amazon S3 Glacier. Hence, this option is incorrect.
- (H) Reference:
- (I) https://aws.amazon.com/snowball/
- (J) A media company operates a web application that enables users to upload photos. These uploads are stored in an Amazon S3 bucket located in the eu-west-2 Region. To enhance performance and provide secure access under a custom domain name, the company wants to integrate Amazon CloudFront for uploads to the S3 bucket. The architecture must support secure HTTPS connections using a custom domain, and the upload process must ensure optimal speed and security.
- () Which combination of actions will fulfill these requirements? (Select two)
- () Create a CloudFront distribution with an S3 static website endpoint as the origin and enable upload operations
- () Set up a custom origin request policy in CloudFront that includes all viewer headers and query strings. Enable S3 Object Ownership to allow CloudFront to assume control of uploaded files via a signed URL
- () Request a public certificate from AWS Certificate Manager (ACM) in the eu-west-2 Region and associate it with the CloudFront distribution
- () Correct selection
- () Set up Amazon S3 to accept uploads from CloudFront by enabling origin access control (OAC)
- () Request a public certificate from AWS Certificate Manager (ACM) in the us-east-1 Region and associate it with the CloudFront distribution
- () Correct options:
- () CloudFront only supports ACM certificates that are created in the us-east-1 (N. Virginia) Region. Even if the content resides in a different Region (like eu-west-2), a public certificate for HTTPS on a custom domain name must originate from us-east-1. This certificate is used to secure content access through CloudFront over HTTPS.
- () Origin Access Control (OAC) is the recommended method for granting CloudFront permission to upload to (write into) an S3 bucket securely. OAC supersedes the older Origin Access Identity (OAI) approach and supports both read and write operations. This allows you to restrict direct access to the S3 bucket and ensure that only CloudFront can act as a secure intermediary for uploads.
- () via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- () Create a CloudFront distribution with an S3 static website endpoint as the origin and enable upload operations - This is incorrect because S3 static website endpoints only support GET and HEAD requests and are intended for public read access. They do not support PUT/POST operations required for user uploads. Therefore, they are not suitable for the secure upload workflow described.
- () Set up a custom origin request policy in CloudFront that includes all viewer headers and query strings. Enable S3 Object Ownership to allow CloudFront to assume control of uploaded files via a signed URL - While customizing origin request policies and enabling S3 Object Ownership might help with some access controls, they do not provide a mechanism to upload content directly via CloudFront. Additionally, signed URLs are primarily used for download access, not for file uploads via CloudFront.
- () Request a public certificate from AWS Certificate Manager (ACM) in the eu-west-2 Region and associate it with the CloudFront distribution - This option is incorrect because CloudFront cannot use ACM public certificates that are created in any Region other than us-east-1. If a certificate is created in eu-west-2, it won’t be attachable to the CloudFront distribution.
- () References:
- () https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-urls.html
- () Which solution should the team implement?
- () Stream EC2 system logs to an Amazon OpenSearch Service domain for real-time indexing and visualization. Use OpenSearch Dashboards to monitor CPU and memory metrics
- () Use Amazon EventBridge to collect EC2 state changes and publish them to Amazon SNS. Subscribe a monitoring dashboard to the SNS topic to visualize metrics
- () Install the CloudWatch agent on all EC2 instances. Configure the agent to collect high-resolution custom metrics and stream them to CloudWatch Logs for analysis via Amazon Athena
- **() Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics to track performance** [CORRECT]
- () By default, EC2 instances publish CloudWatch metrics at 5-minute intervals. Enabling detailed monitoring changes this to 1-minute intervals, allowing the team to observe system performance with the necessary granularity. CloudWatch metrics provide native integration with EC2 and are the most efficient way to analyze CPU, network, and disk utilization without complex setups.

**Answer:**
Correct Answer: **Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics to track performance**

---

## Question 131

**Q:** Which combination of actions will fulfill these requirements? (Select two)

**Options:**
- (A) Create a CloudFront distribution with an S3 static website endpoint as the origin and enable upload operations
- (B) Set up a custom origin request policy in CloudFront that includes all viewer headers and query strings. Enable S3 Object Ownership to allow CloudFront to assume control of uploaded files via a signed URL
- (C) Request a public certificate from AWS Certificate Manager (ACM) in the eu-west-2 Region and associate it with the CloudFront distribution
- (D) Correct selection
- (E) Set up Amazon S3 to accept uploads from CloudFront by enabling origin access control (OAC)
- (F) Request a public certificate from AWS Certificate Manager (ACM) in the us-east-1 Region and associate it with the CloudFront distribution
- (G) Correct options:
- (H) CloudFront only supports ACM certificates that are created in the us-east-1 (N. Virginia) Region. Even if the content resides in a different Region (like eu-west-2), a public certificate for HTTPS on a custom domain name must originate from us-east-1. This certificate is used to secure content access through CloudFront over HTTPS.
- (I) Origin Access Control (OAC) is the recommended method for granting CloudFront permission to upload to (write into) an S3 bucket securely. OAC supersedes the older Origin Access Identity (OAI) approach and supports both read and write operations. This allows you to restrict direct access to the S3 bucket and ensure that only CloudFront can act as a secure intermediary for uploads.
- (J) via - https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- () Incorrect options:
- () Create a CloudFront distribution with an S3 static website endpoint as the origin and enable upload operations - This is incorrect because S3 static website endpoints only support GET and HEAD requests and are intended for public read access. They do not support PUT/POST operations required for user uploads. Therefore, they are not suitable for the secure upload workflow described.
- () Set up a custom origin request policy in CloudFront that includes all viewer headers and query strings. Enable S3 Object Ownership to allow CloudFront to assume control of uploaded files via a signed URL - While customizing origin request policies and enabling S3 Object Ownership might help with some access controls, they do not provide a mechanism to upload content directly via CloudFront. Additionally, signed URLs are primarily used for download access, not for file uploads via CloudFront.
- () Request a public certificate from AWS Certificate Manager (ACM) in the eu-west-2 Region and associate it with the CloudFront distribution - This option is incorrect because CloudFront cannot use ACM public certificates that are created in any Region other than us-east-1. If a certificate is created in eu-west-2, it won’t be attachable to the CloudFront distribution.
- () References:
- () https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-urls.html
- () Which solution should the team implement?
- () Stream EC2 system logs to an Amazon OpenSearch Service domain for real-time indexing and visualization. Use OpenSearch Dashboards to monitor CPU and memory metrics
- () Use Amazon EventBridge to collect EC2 state changes and publish them to Amazon SNS. Subscribe a monitoring dashboard to the SNS topic to visualize metrics
- () Install the CloudWatch agent on all EC2 instances. Configure the agent to collect high-resolution custom metrics and stream them to CloudWatch Logs for analysis via Amazon Athena
- () Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics to track performance
- () Correct option:
- () By default, EC2 instances publish CloudWatch metrics at 5-minute intervals. Enabling detailed monitoring changes this to 1-minute intervals, allowing the team to observe system performance with the necessary granularity. CloudWatch metrics provide native integration with EC2 and are the most efficient way to analyze CPU, network, and disk utilization without complex setups.
- () via - https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch-metrics-basic-detailed.html
- () Use Amazon EventBridge to collect EC2 state changes and publish them to Amazon SNS. Subscribe a monitoring dashboard to the SNS topic to visualize metrics - EventBridge and SNS are designed for event-driven architectures and alerting—not for performance monitoring or detailed metric analysis. This approach would not provide the continuous, granular data the company needs to evaluate real-time performance trends. Moreover, SNS is not built to directly support monitoring dashboards.
- () Stream EC2 system logs to an Amazon OpenSearch Service domain for real-time indexing and visualization. Use OpenSearch Dashboards to monitor CPU and memory metrics - While Amazon OpenSearch Service is excellent for log indexing and search, it does not natively collect EC2 performance metrics like CPU utilization or disk I/O. To make this work, the company would need to implement custom log collection and parsing, which adds unnecessary complexity compared to using CloudWatch.
- () Install the CloudWatch agent on all EC2 instances. Configure the agent to collect high-resolution custom metrics and stream them to CloudWatch Logs for analysis via Amazon Athena - Although this setup could support fine-grained metric collection, it introduces significant operational overhead. It requires manual agent installation, configuration, and maintenance across all instances. Analyzing logs via Athena also introduces query latency, which is not ideal for real-time performance tracking.
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch-metrics-basic-detailed.html
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html
- () https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html
- () Which solution meets the company's encryption and cost optimization goals?
- **() Enable S3 Bucket Keys for server-side encryption with AWS KMS (SSE-KMS) so that new objects use a bucket-level key rather than requesting individual KMS data keys for every object** [CORRECT]
- () Switch to server-side encryption using Amazon S3 managed keys (SSE-S3) to eliminate all AWS KMS-related encryption charges while maintaining the same level of encryption control
- () Configure a VPC endpoint for S3 and restrict access to the bucket to traffic originating from the endpoint to avoid additional KMS charges

**Answer:**
Correct Answer: **Enable S3 Bucket Keys for server-side encryption with AWS KMS (SSE-KMS) so that new objects use a bucket-level key rather than requesting individual KMS data keys for every object**

---

## Question 132

**Q:** Which solution should the team implement?

**Options:**
- (A) Stream EC2 system logs to an Amazon OpenSearch Service domain for real-time indexing and visualization. Use OpenSearch Dashboards to monitor CPU and memory metrics
- (B) Use Amazon EventBridge to collect EC2 state changes and publish them to Amazon SNS. Subscribe a monitoring dashboard to the SNS topic to visualize metrics
- (C) Install the CloudWatch agent on all EC2 instances. Configure the agent to collect high-resolution custom metrics and stream them to CloudWatch Logs for analysis via Amazon Athena
- (D) Enable detailed monitoring on all EC2 instances and use Amazon CloudWatch metrics to track performance
- (E) Correct option:
- (F) By default, EC2 instances publish CloudWatch metrics at 5-minute intervals. Enabling detailed monitoring changes this to 1-minute intervals, allowing the team to observe system performance with the necessary granularity. CloudWatch metrics provide native integration with EC2 and are the most efficient way to analyze CPU, network, and disk utilization without complex setups.
- (G) via - https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch-metrics-basic-detailed.html
- (H) Incorrect options:
- (I) Use Amazon EventBridge to collect EC2 state changes and publish them to Amazon SNS. Subscribe a monitoring dashboard to the SNS topic to visualize metrics - EventBridge and SNS are designed for event-driven architectures and alerting—not for performance monitoring or detailed metric analysis. This approach would not provide the continuous, granular data the company needs to evaluate real-time performance trends. Moreover, SNS is not built to directly support monitoring dashboards.
- (J) Stream EC2 system logs to an Amazon OpenSearch Service domain for real-time indexing and visualization. Use OpenSearch Dashboards to monitor CPU and memory metrics - While Amazon OpenSearch Service is excellent for log indexing and search, it does not natively collect EC2 performance metrics like CPU utilization or disk I/O. To make this work, the company would need to implement custom log collection and parsing, which adds unnecessary complexity compared to using CloudWatch.
- () Install the CloudWatch agent on all EC2 instances. Configure the agent to collect high-resolution custom metrics and stream them to CloudWatch Logs for analysis via Amazon Athena - Although this setup could support fine-grained metric collection, it introduces significant operational overhead. It requires manual agent installation, configuration, and maintenance across all instances. Analyzing logs via Athena also introduces query latency, which is not ideal for real-time performance tracking.
- () References:
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/cloudwatch-metrics-basic-detailed.html
- () https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html
- () https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html
- () Which solution meets the company's encryption and cost optimization goals?
- () Enable S3 Bucket Keys for server-side encryption with AWS KMS (SSE-KMS) so that new objects use a bucket-level key rather than requesting individual KMS data keys for every object
- () Switch to server-side encryption using Amazon S3 managed keys (SSE-S3) to eliminate all AWS KMS-related encryption charges while maintaining the same level of encryption control
- () Configure a VPC endpoint for S3 and restrict access to the bucket to traffic originating from the endpoint to avoid additional KMS charges
- () Use client-side encryption by generating a local symmetric key and uploading it to Amazon S3 along with each object’s metadata for decryption
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-key.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-key.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingClientSideEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingEncryption.html
- () Which solution will best meet these requirements with the least development effort?
- **() Set up a 7-day EBS snapshot retention rule in Recycle Bin and apply the rule for all snapshots** [CORRECT]
- () Enable AWS Backup Vault Lock on the backup vault and store EBS snapshots in that vault to enforce deletion protection
- () Set up the IAM policy of the user to deny EBS snapshot deletion
- () Implement a Lambda-based backup automation workflow that archives snapshot metadata in DynamoDB and stores backups in Amazon S3 Glacier Deep Archive for long-term recovery

**Answer:**
Correct Answer: **Set up a 7-day EBS snapshot retention rule in Recycle Bin and apply the rule for all snapshots**

---

## Question 133

**Q:** Which solution meets the company's encryption and cost optimization goals?

**Options:**
- (A) Enable S3 Bucket Keys for server-side encryption with AWS KMS (SSE-KMS) so that new objects use a bucket-level key rather than requesting individual KMS data keys for every object
- (B) Switch to server-side encryption using Amazon S3 managed keys (SSE-S3) to eliminate all AWS KMS-related encryption charges while maintaining the same level of encryption control
- (C) Configure a VPC endpoint for S3 and restrict access to the bucket to traffic originating from the endpoint to avoid additional KMS charges
- (D) Use client-side encryption by generating a local symmetric key and uploading it to Amazon S3 along with each object’s metadata for decryption
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-key.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-key.html
- (J) https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingClientSideEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingEncryption.html
- () Which solution will best meet these requirements with the least development effort?
- **() Set up a 7-day EBS snapshot retention rule in Recycle Bin and apply the rule for all snapshots** [CORRECT]
- () Enable AWS Backup Vault Lock on the backup vault and store EBS snapshots in that vault to enforce deletion protection
- () Set up the IAM policy of the user to deny EBS snapshot deletion
- () Implement a Lambda-based backup automation workflow that archives snapshot metadata in DynamoDB and stores backups in Amazon S3 Glacier Deep Archive for long-term recovery
- () Implement a Lambda-based backup automation workflow that archives snapshot metadata in DynamoDB and stores backups in Amazon S3 Glacier Deep Archive for long-term recovery - This approach adds significant development effort and does not natively prevent snapshot deletion. So, it is incorrect.
- () Set up the IAM policy of the user to deny EBS snapshot deletion - While denying deletion can prevent accidental loss, it also completely blocks all snapshot deletions, including those that are genuinely expired or no longer needed. This violates the requirement to avoid indefinite snapshot retention, leading to storage bloat and increased cost.
- () https://docs.aws.amazon.com/ebs/latest/userguide/recycle-bin.html
- () https://docs.aws.amazon.com/aws-backup/latest/devguide/vault-lock.html
- () A silicon valley based healthcare startup uses AWS Cloud for its IT infrastructure. The startup stores patient health records on Amazon Simple Storage Service (Amazon S3). The engineering team needs to implement an archival solution based on Amazon S3 Glacier to enforce regulatory and compliance controls on data access.

**Answer:**
Correct Answer: **Set up a 7-day EBS snapshot retention rule in Recycle Bin and apply the rule for all snapshots**

---

## Question 134

**Q:** Which solution will best meet these requirements with the least development effort?

**Options:**
- **(A) Set up a 7-day EBS snapshot retention rule in Recycle Bin and apply the rule for all snapshots** [CORRECT]
- (B) Enable AWS Backup Vault Lock on the backup vault and store EBS snapshots in that vault to enforce deletion protection
- (C) Set up the IAM policy of the user to deny EBS snapshot deletion
- (D) Implement a Lambda-based backup automation workflow that archives snapshot metadata in DynamoDB and stores backups in Amazon S3 Glacier Deep Archive for long-term recovery
- (E) Correct option:
- (F) Incorrect Options:
- (G) Implement a Lambda-based backup automation workflow that archives snapshot metadata in DynamoDB and stores backups in Amazon S3 Glacier Deep Archive for long-term recovery - This approach adds significant development effort and does not natively prevent snapshot deletion. So, it is incorrect.
- (H) Set up the IAM policy of the user to deny EBS snapshot deletion - While denying deletion can prevent accidental loss, it also completely blocks all snapshot deletions, including those that are genuinely expired or no longer needed. This violates the requirement to avoid indefinite snapshot retention, leading to storage bloat and increased cost.
- (I) References:
- (J) https://docs.aws.amazon.com/ebs/latest/userguide/recycle-bin.html
- () https://docs.aws.amazon.com/aws-backup/latest/devguide/vault-lock.html
- () A silicon valley based healthcare startup uses AWS Cloud for its IT infrastructure. The startup stores patient health records on Amazon Simple Storage Service (Amazon S3). The engineering team needs to implement an archival solution based on Amazon S3 Glacier to enforce regulatory and compliance controls on data access.

**Answer:**
Correct Answer: **Set up a 7-day EBS snapshot retention rule in Recycle Bin and apply the rule for all snapshots**

---

## Question 135

**Q:** As a solutions architect, which of the following solutions would you recommend as the MOST effective in countering these malicious attacks?

**Options:**
- (A) Use AWS Firewall Manager with CloudFront distribution
- (B) Use Amazon Route 53 with Amazon CloudFront distribution
- (C) Use AWS Security Hub with Amazon CloudFront distribution
- (D) Use AWS Web Application Firewall (AWS WAF) with Amazon CloudFront distribution
- (E) Correct option:
- (F) AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that block common attack patterns, such as SQL injection or cross-site scripting, and rules that filter out specific traffic patterns you define.
- (G) How AWS WAF Works:
- (H) via - https://aws.amazon.com/waf/
- (I) A web access control list (web ACL) gives you fine-grained control over the web requests that your Amazon CloudFront distribution, Amazon API Gateway API, or Application Load Balancer responds to.
- (J) When you create a web ACL, you can specify one or more Amazon CloudFront distributions that you want AWS WAF to inspect. AWS WAF starts to allow, block, or count web requests for those distributions based on the conditions that you identify in the web ACL. Therefore, combining AWS WAF with Amazon CloudFront can prevent SQL injection and cross-site scripting attacks. So this is the correct option.
- () Incorrect options:
- () Use Amazon Route 53 with Amazon CloudFront distribution - Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. You cannot use Route 53 to prevent SQL injection and cross-site scripting attacks. So this option is incorrect.
- () Use AWS Firewall Manager with CloudFront distribution - AWS Firewall Manager is a security management service that allows you to centrally configure and manage firewall rules across your accounts and applications in AWS Organization. You cannot use AWS Firewall Manager to prevent SQL injection and cross-site scripting attacks. So this option is incorrect.
- () References:
- () https://aws.amazon.com/waf/features/
- () https://docs.aws.amazon.com/waf/latest/developerguide/web-acl.html
- () https://docs.aws.amazon.com/waf/latest/developerguide/cloudfront-features.html
- () An application with global users across AWS Regions had suffered an issue when the Elastic Load Balancing (ELB) in a Region malfunctioned thereby taking down the traffic with it. The manual intervention cost the company significant time and resulted in major revenue loss.
- () What should a solutions architect recommend to reduce internet latency and add automatic failover across AWS Regions?
- **() Set up AWS Global Accelerator and add endpoints to cater to users in different geographic locations** [CORRECT]
- () Set up an Amazon Route 53 geoproximity routing policy to route traffic
- () Set up AWS Direct Connect as the backbone for each of the AWS Regions where the application is deployed
- () Create Amazon S3 buckets in different AWS Regions and configure Amazon CloudFront to pick the nearest edge location to the user
- () By using AWS Global Accelerator, you can:
- () 1. Associate the static IP addresses provided by AWS Global Accelerator to regional AWS resources or endpoints, such as Network Load Balancers, Application Load Balancers, EC2 Instances, and Elastic IP addresses. The IP addresses are anycast from AWS edge locations so they provide onboarding to the AWS global network close to your users.
- () 2. Easily move endpoints between Availability Zones or AWS Regions without needing to update your DNS configuration or change client-facing applications.
- () 3. Dial traffic up or down for a specific AWS Region by configuring a traffic dial percentage for your endpoint groups. This is especially useful for testing performance and releasing updates.
- () 4. Control the proportion of traffic directed to each endpoint within an endpoint group by assigning weights across the endpoints.
- () AWS Global Accelerator for Multi-Region applications:
- () via - https://aws.amazon.com/global-accelerator/
- () Set up AWS Direct Connect as the backbone for each of the AWS Regions where the application is deployed - AWS Direct Connect can reduce latency to great extent. Direct Connect is used to connect on-premises systems to AWS Cloud for extremely low latency use cases. It cannot be used to serve users directly.
- () Create Amazon S3 buckets in different AWS Regions and configure Amazon CloudFront to pick the nearest edge location to the user - If most of the content is static, we can configure Amazon CloudFront to improve performance. In the current scenario, the architecture has ELBs, Amazon EC2 instances too that need to be covered in the automatic failover plan.
- () https://aws.amazon.com/global-accelerator/features/
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-geoproximity
- () A financial data processing company runs a workload on Amazon EC2 instances that fetch and process real-time transaction batches from an Amazon SQS queue. The application needs to scale based on unpredictable message volume, which fluctuates significantly throughout the day. The system must process messages with minimal delay and no downtime, even during peak spikes. The company is seeking a solution that balances cost-efficiency with availability and elasticity.
- () Which EC2 purchasing strategy best meets these requirements in the most cost-effective manner?
- () Purchase EC2 Reserved Instances to match peak capacity and assign all message processing tasks to these instances regardless of load variations

**Answer:**
Correct Answer: **Set up AWS Global Accelerator and add endpoints to cater to users in different geographic locations**

---

## Question 136

**Q:** What should a solutions architect recommend to reduce internet latency and add automatic failover across AWS Regions?

**Options:**
- (A) Set up AWS Global Accelerator and add endpoints to cater to users in different geographic locations
- (B) Set up an Amazon Route 53 geoproximity routing policy to route traffic
- (C) Set up AWS Direct Connect as the backbone for each of the AWS Regions where the application is deployed
- (D) Create Amazon S3 buckets in different AWS Regions and configure Amazon CloudFront to pick the nearest edge location to the user
- (E) Correct option:
- (F) By using AWS Global Accelerator, you can:
- (G) 1. Associate the static IP addresses provided by AWS Global Accelerator to regional AWS resources or endpoints, such as Network Load Balancers, Application Load Balancers, EC2 Instances, and Elastic IP addresses. The IP addresses are anycast from AWS edge locations so they provide onboarding to the AWS global network close to your users.
- (H) 2. Easily move endpoints between Availability Zones or AWS Regions without needing to update your DNS configuration or change client-facing applications.
- (I) 3. Dial traffic up or down for a specific AWS Region by configuring a traffic dial percentage for your endpoint groups. This is especially useful for testing performance and releasing updates.
- (J) 4. Control the proportion of traffic directed to each endpoint within an endpoint group by assigning weights across the endpoints.
- () AWS Global Accelerator for Multi-Region applications:
- () via - https://aws.amazon.com/global-accelerator/
- () Incorrect options:
- () Set up AWS Direct Connect as the backbone for each of the AWS Regions where the application is deployed - AWS Direct Connect can reduce latency to great extent. Direct Connect is used to connect on-premises systems to AWS Cloud for extremely low latency use cases. It cannot be used to serve users directly.
- () Create Amazon S3 buckets in different AWS Regions and configure Amazon CloudFront to pick the nearest edge location to the user - If most of the content is static, we can configure Amazon CloudFront to improve performance. In the current scenario, the architecture has ELBs, Amazon EC2 instances too that need to be covered in the automatic failover plan.
- () References:
- () https://aws.amazon.com/global-accelerator/features/
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-geoproximity
- () A financial data processing company runs a workload on Amazon EC2 instances that fetch and process real-time transaction batches from an Amazon SQS queue. The application needs to scale based on unpredictable message volume, which fluctuates significantly throughout the day. The system must process messages with minimal delay and no downtime, even during peak spikes. The company is seeking a solution that balances cost-efficiency with availability and elasticity.
- () Which EC2 purchasing strategy best meets these requirements in the most cost-effective manner?
- () Purchase EC2 Reserved Instances to match peak capacity and assign all message processing tasks to these instances regardless of load variations
- () Use EC2 Reserved Instances for the baseline workload and configure EC2 Auto Scaling to launch On-Demand Instances for all traffic spikes
- () Use EC2 Spot Instances exclusively with Auto Scaling enabled to match message volume fluctuations and save on compute costs
- **() Use Reserved Instances for the baseline level of traffic and configure EC2 Auto Scaling with Spot Instances to handle spikes in message volume** [CORRECT]
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () https://docs.aws.amazon.com/savingsplans/latest/userguide/what-is-savings-plans.html
- () A global enterprise is modernizing its hybrid IT infrastructure to improve both availability and network performance. The company operates a TCP-based application hosted on Amazon EC2 instances that are deployed across multiple AWS Regions, while a secondary UDP-based component of the application is hosted in its on-premises data centers. These application components must be accessed by customers around the world with minimal latency and consistent uptime.
- () Which combination of options should a solutions architect implement for the given use case? (Select two)
- () Create a Network Load Balancer (NLB) in each Region to handle the EC2-based TCP traffic. For the UDP-based on-premises workload, configure Application Load Balancers in each Region to route to the on-premises endpoints via IP-based target groups
- () Deploy AWS PrivateLink to connect each on-premises UDP workload to the AWS Regions through interface endpoints exposed by the Network Load Balancers
- () Set up AWS Direct Connect connections to route all TCP and UDP traffic through a single Region, using static routes and BGP failover
- () Correct selection
- () Configure an AWS Global Accelerator standard accelerator, and register the TCP-based EC2 workloads behind the load balancers
- () Create a Network Load Balancer (NLB) in each Region to handle the EC2-based TCP traffic. For the UDP-based on-premises workload, configure NLBs in each Region to route to the on-premises endpoints via IP-based target groups

**Answer:**
Correct Answer: **Use Reserved Instances for the baseline level of traffic and configure EC2 Auto Scaling with Spot Instances to handle spikes in message volume**

---

## Question 137

**Q:** Which EC2 purchasing strategy best meets these requirements in the most cost-effective manner?

**Options:**
- (A) Purchase EC2 Reserved Instances to match peak capacity and assign all message processing tasks to these instances regardless of load variations
- (B) Use EC2 Reserved Instances for the baseline workload and configure EC2 Auto Scaling to launch On-Demand Instances for all traffic spikes
- (C) Use EC2 Spot Instances exclusively with Auto Scaling enabled to match message volume fluctuations and save on compute costs
- (D) Use Reserved Instances for the baseline level of traffic and configure EC2 Auto Scaling with Spot Instances to handle spikes in message volume
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups.html
- (I) https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- (J) https://docs.aws.amazon.com/savingsplans/latest/userguide/what-is-savings-plans.html
- () A global enterprise is modernizing its hybrid IT infrastructure to improve both availability and network performance. The company operates a TCP-based application hosted on Amazon EC2 instances that are deployed across multiple AWS Regions, while a secondary UDP-based component of the application is hosted in its on-premises data centers. These application components must be accessed by customers around the world with minimal latency and consistent uptime.
- () Which combination of options should a solutions architect implement for the given use case? (Select two)
- () Create a Network Load Balancer (NLB) in each Region to handle the EC2-based TCP traffic. For the UDP-based on-premises workload, configure Application Load Balancers in each Region to route to the on-premises endpoints via IP-based target groups
- () Deploy AWS PrivateLink to connect each on-premises UDP workload to the AWS Regions through interface endpoints exposed by the Network Load Balancers
- () Set up AWS Direct Connect connections to route all TCP and UDP traffic through a single Region, using static routes and BGP failover
- () Correct selection
- () Configure an AWS Global Accelerator standard accelerator, and register the TCP-based EC2 workloads behind the load balancers
- () Create a Network Load Balancer (NLB) in each Region to handle the EC2-based TCP traffic. For the UDP-based on-premises workload, configure NLBs in each Region to route to the on-premises endpoints via IP-based target groups
- () Correct options:
- () AWS Global Accelerator supports improving the availability and performance of global applications with TCP-based traffic. It routes users to the closest healthy endpoint in multiple Regions via the AWS global network and supports automatic failover. Registering load balancers as endpoints ensures that the TCP workload hosted on EC2 instances benefits from low-latency access and high availability.
- () Network Load Balancers support both TCP and UDP traffic. By creating NLBs in each Region, the architecture allows load balancing for EC2 workloads and can forward UDP traffic to IP-based targets in on-premises networks. This setup ensures that both stateful TCP and stateless UDP workloads are accessible and scalable from AWS.
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () Set up AWS Direct Connect connections to route all TCP and UDP traffic through a single Region, using static routes and BGP failover - AWS Direct Connect enhances dedicated network performance between AWS and on-premises infrastructure but does not inherently provide intelligent global routing, failover, or multi-region resilience. It is not optimal for distributing traffic across Regions or managing global availability.
- () Deploy AWS PrivateLink to connect each on-premises UDP workload to the AWS Regions through interface endpoints exposed by the Network Load Balancers - AWS PrivateLink enables secure connectivity to AWS services via VPC endpoints but supports only TCP-based traffic. It cannot be used to route or expose UDP-based services, making it unsuitable for the on-premises UDP workload.
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- () An application hosted on Amazon EC2 contains sensitive personal information about all its customers and needs to be protected from all types of cyber-attacks. The company is considering using the AWS Web Application Firewall (AWS WAF) to handle this requirement.
- () Can you identify the correct solution leveraging the capabilities of AWS WAF?
- () AWS WAF can be directly configured only on an Application Load Balancer or an Amazon API Gateway. One of these two services can then be configured with Amazon EC2 to build the needed secure architecture
- **() Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures** [CORRECT]
- () AWS WAF can be directly configured on Amazon EC2 instances for ensuring the security of the underlying application data
- () Configure an Application Load Balancer (ALB) to balance the workload for all the Amazon EC2 instances. Configure Amazon CloudFront to distribute from an Application Load Balancer since AWS WAF cannot be directly configured on ALB. This configuration not only provides necessary safety but is scalable too

**Answer:**
Correct Answer: **Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures**

---

## Question 138

**Q:** Which combination of options should a solutions architect implement for the given use case? (Select two)

**Options:**
- (A) Create a Network Load Balancer (NLB) in each Region to handle the EC2-based TCP traffic. For the UDP-based on-premises workload, configure Application Load Balancers in each Region to route to the on-premises endpoints via IP-based target groups
- (B) Deploy AWS PrivateLink to connect each on-premises UDP workload to the AWS Regions through interface endpoints exposed by the Network Load Balancers
- (C) Set up AWS Direct Connect connections to route all TCP and UDP traffic through a single Region, using static routes and BGP failover
- (D) Correct selection
- (E) Configure an AWS Global Accelerator standard accelerator, and register the TCP-based EC2 workloads behind the load balancers
- (F) Create a Network Load Balancer (NLB) in each Region to handle the EC2-based TCP traffic. For the UDP-based on-premises workload, configure NLBs in each Region to route to the on-premises endpoints via IP-based target groups
- (G) Correct options:
- (H) AWS Global Accelerator supports improving the availability and performance of global applications with TCP-based traffic. It routes users to the closest healthy endpoint in multiple Regions via the AWS global network and supports automatic failover. Registering load balancers as endpoints ensures that the TCP workload hosted on EC2 instances benefits from low-latency access and high availability.
- (I) Network Load Balancers support both TCP and UDP traffic. By creating NLBs in each Region, the architecture allows load balancing for EC2 workloads and can forward UDP traffic to IP-based targets in on-premises networks. This setup ensures that both stateful TCP and stateless UDP workloads are accessible and scalable from AWS.
- (J) via - https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () Incorrect Options:
- () Set up AWS Direct Connect connections to route all TCP and UDP traffic through a single Region, using static routes and BGP failover - AWS Direct Connect enhances dedicated network performance between AWS and on-premises infrastructure but does not inherently provide intelligent global routing, failover, or multi-region resilience. It is not optimal for distributing traffic across Regions or managing global availability.
- () Deploy AWS PrivateLink to connect each on-premises UDP workload to the AWS Regions through interface endpoints exposed by the Network Load Balancers - AWS PrivateLink enables secure connectivity to AWS services via VPC endpoints but supports only TCP-based traffic. It cannot be used to route or expose UDP-based services, making it unsuitable for the on-premises UDP workload.
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- () References:
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/what-is-global-accelerator.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- () An application hosted on Amazon EC2 contains sensitive personal information about all its customers and needs to be protected from all types of cyber-attacks. The company is considering using the AWS Web Application Firewall (AWS WAF) to handle this requirement.
- () Can you identify the correct solution leveraging the capabilities of AWS WAF?
- () AWS WAF can be directly configured only on an Application Load Balancer or an Amazon API Gateway. One of these two services can then be configured with Amazon EC2 to build the needed secure architecture
- **() Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures** [CORRECT]
- () AWS WAF can be directly configured on Amazon EC2 instances for ensuring the security of the underlying application data
- () Configure an Application Load Balancer (ALB) to balance the workload for all the Amazon EC2 instances. Configure Amazon CloudFront to distribute from an Application Load Balancer since AWS WAF cannot be directly configured on ALB. This configuration not only provides necessary safety but is scalable too
- () Correct option:
- () When you use AWS WAF with Amazon CloudFront, you can protect your applications running on any HTTP webserver, whether it's a webserver that's running in Amazon Elastic Compute Cloud (Amazon EC2) or a web server that you manage privately. You can also configure Amazon CloudFront to require HTTPS between CloudFront and your own webserver, as well as between viewers and Amazon CloudFront.
- () Configure an Application Load Balancer (ALB) to balance the workload for all the Amazon EC2 instances. Configure Amazon CloudFront to distribute from an Application Load Balancer since AWS WAF cannot be directly configured on ALB. This configuration not only provides necessary safety but is scalable too - This statement is wrong. You can configure AWS WAF on Application Load Balancers (ALB).
- () AWS WAF can be directly configured on Amazon EC2 instances for ensuring the security of the underlying application data - AWS WAF can be deployed on Amazon CloudFront, the Application Load Balancer (ALB), and Amazon API Gateway. It cannot be configured directly on an Amazon EC2 instance.
- () AWS WAF can be directly configured only on an Application Load Balancer or an Amazon API Gateway. One of these two services can then be configured with Amazon EC2 to build the needed secure architecture - This statement is only partially correct. AWS WAF can also be deployed on Amazon CloudFront service.
- () https://aws.amazon.com/waf/faqs/
- () https://docs.aws.amazon.com/waf/latest/developerguide/cloudfront-features.html
- () Computer vision researchers at a university are trying to optimize the I/O bound processes for a proprietary algorithm running on Amazon EC2 instances. The ideal storage would facilitate high-performance IOPS when doing file processing in a temporary storage space before uploading the results back into Amazon S3.

**Answer:**
Correct Answer: **Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures**

---

## Question 139

**Q:** Can you identify the correct solution leveraging the capabilities of AWS WAF?

**Options:**
- (A) AWS WAF can be directly configured only on an Application Load Balancer or an Amazon API Gateway. One of these two services can then be configured with Amazon EC2 to build the needed secure architecture
- **(B) Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures** [CORRECT]
- (C) AWS WAF can be directly configured on Amazon EC2 instances for ensuring the security of the underlying application data
- (D) Configure an Application Load Balancer (ALB) to balance the workload for all the Amazon EC2 instances. Configure Amazon CloudFront to distribute from an Application Load Balancer since AWS WAF cannot be directly configured on ALB. This configuration not only provides necessary safety but is scalable too
- (E) Correct option:
- (F) When you use AWS WAF with Amazon CloudFront, you can protect your applications running on any HTTP webserver, whether it's a webserver that's running in Amazon Elastic Compute Cloud (Amazon EC2) or a web server that you manage privately. You can also configure Amazon CloudFront to require HTTPS between CloudFront and your own webserver, as well as between viewers and Amazon CloudFront.
- (G) Incorrect options:
- (H) Configure an Application Load Balancer (ALB) to balance the workload for all the Amazon EC2 instances. Configure Amazon CloudFront to distribute from an Application Load Balancer since AWS WAF cannot be directly configured on ALB. This configuration not only provides necessary safety but is scalable too - This statement is wrong. You can configure AWS WAF on Application Load Balancers (ALB).
- (I) AWS WAF can be directly configured on Amazon EC2 instances for ensuring the security of the underlying application data - AWS WAF can be deployed on Amazon CloudFront, the Application Load Balancer (ALB), and Amazon API Gateway. It cannot be configured directly on an Amazon EC2 instance.
- (J) AWS WAF can be directly configured only on an Application Load Balancer or an Amazon API Gateway. One of these two services can then be configured with Amazon EC2 to build the needed secure architecture - This statement is only partially correct. AWS WAF can also be deployed on Amazon CloudFront service.
- () References:
- () https://aws.amazon.com/waf/faqs/
- () https://docs.aws.amazon.com/waf/latest/developerguide/cloudfront-features.html
- () Computer vision researchers at a university are trying to optimize the I/O bound processes for a proprietary algorithm running on Amazon EC2 instances. The ideal storage would facilitate high-performance IOPS when doing file processing in a temporary storage space before uploading the results back into Amazon S3.

**Answer:**
Correct Answer: **Create Amazon CloudFront distribution for the application on Amazon EC2 instances. Deploy AWS WAF on Amazon CloudFront to provide the necessary safety measures**

---

## Question 140

**Q:** As a solutions architect, which of the following AWS storage options would you recommend as the MOST performant as well as cost-optimal?

**Options:**
- **(A) Use Amazon EC2 instances with Instance Store as the storage option** [CORRECT]
- (B) Use Amazon EC2 instances with Amazon EBS General Purpose SSD (gp2) as the storage option
- (C) Use Amazon EC2 instances with Amazon EBS Provisioned IOPS SSD (io1) as the storage option
- (D) Use Amazon EC2 instances with Amazon EBS Throughput Optimized HDD (st1) as the storage option
- (E) Correct option:
- (F) As Instance Store delivers high random I/O performance, it can act as a temporary storage space, and these volumes are included as part of the instance's usage cost, therefore this is the correct option.
- (G) Amazon EC2 Instance Store:
- (H) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- (I) Incorrect options:
- (J) Use Amazon EC2 instances with Amazon EBS Throughput Optimized HDD (st1) as the storage option - Throughput Optimized HDD (st1) are low-cost HDD volumes designed for frequently accessed, throughput-intensive workloads such as Big data and Data warehouses. Amazon EBS st1 is persistent storage and costlier than Instance Stores (the cost of the storage volume is in addition to that of the Amazon EC2 instance), therefore this option is not correct.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html
- () Which combination of steps will meet these requirements? (Select two)
- () Enable AWS Config rules to detect noncompliant EC2 instances. Trigger an AWS Systems Manager Automation runbook to reapply missing tags automatically when noncompliance is detected
- () Create a tag enforcement Lambda function that runs on a schedule to identify EC2 instances without the required tag. The function sends a notification to administrators and optionally shuts down noncompliant resources
- () Correct selection
- () Define a tag policy in AWS Organizations that enforces the dataClassification key and restricts values to 'confidential' and 'public'. Attach this tag policy to the applicable organizational unit (OU) to enforce uniform tagging behavior across accounts
- () Create a service control policy (SCP) that denies the ec2:RunInstances API action unless the required tag key is present in the request. Create a second SCP that denies the ec2:DeleteTags action for EC2 resources. Attach both SCPs to the relevant OU in AWS Organizations
- () Use AWS Identity and Access Management (IAM) permission boundaries to restrict EC2-related actions unless the dataClassification tag is present. Apply these boundaries to all IAM roles used for EC2 provisioning
- () Correct options:
- () AWS Tag Policies, managed through AWS Organizations, allow administrators to define rules for tag keys and values. These policies do not directly prevent resource creation, but they help enforce tag consistency and visibility by flagging noncompliant resources.
- () Service Control Policies (SCPs) allow you to centrally govern permissions for accounts in AWS Organizations. An SCP defines the maximum set of permissions available to IAM users and roles in an account. When combined with condition keys, SCPs can enforce fine-grained controls on specific operations.
- () via - https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps_examples_tagging.html
- () Create a tag enforcement Lambda function that runs on a schedule to identify EC2 instances without the required tag. The function sends a notification to administrators and optionally shuts down noncompliant resources - This reactive approach relies on periodic audits rather than enforcing tagging at the time of resource creation. It increases operational overhead and cannot guarantee immediate compliance, especially for short-lived resources.
- () Use AWS Identity and Access Management (IAM) permission boundaries to restrict EC2-related actions unless the dataClassification tag is present. Apply these boundaries to all IAM roles used for EC2 provisioning - While IAM permission boundaries can restrict actions within a boundary, they are not designed to enforce tag-based controls across all users or to prevent tag deletion. SCPs and tag policies are more appropriate at the organizational level.
- () Enable AWS Config rules to detect noncompliant EC2 instances. Trigger an AWS Systems Manager Automation runbook to reapply missing tags automatically when noncompliance is detected - AWS Config and automation runbooks offer remediation, but do not prevent noncompliant resources from being created in the first place. This violates the requirement for proactive enforcement and minimal public exposure of misclassified data.
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_tag-policies.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps_examples_tagging.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html
- () The engineering team at a retail company manages 3 Amazon EC2 instances that make read-heavy database requests to the Amazon RDS for the PostgreSQL database instance. As an AWS Certified Solutions Architect - Associate, you have been tasked to make the database instance resilient from a disaster recovery perspective.

**Answer:**
Correct Answer: **Use Amazon EC2 instances with Instance Store as the storage option**

---

## Question 141

**Q:** Which combination of steps will meet these requirements? (Select two)

**Options:**
- **(A) Enable AWS Config rules to detect noncompliant EC2 instances. Trigger an AWS Systems Manager Automation runbook to reapply missing tags automatically when noncompliance is detected** [CORRECT]
- (B) Create a tag enforcement Lambda function that runs on a schedule to identify EC2 instances without the required tag. The function sends a notification to administrators and optionally shuts down noncompliant resources
- (C) Correct selection
- (D) Define a tag policy in AWS Organizations that enforces the dataClassification key and restricts values to 'confidential' and 'public'. Attach this tag policy to the applicable organizational unit (OU) to enforce uniform tagging behavior across accounts
- (E) Create a service control policy (SCP) that denies the ec2:RunInstances API action unless the required tag key is present in the request. Create a second SCP that denies the ec2:DeleteTags action for EC2 resources. Attach both SCPs to the relevant OU in AWS Organizations
- (F) Use AWS Identity and Access Management (IAM) permission boundaries to restrict EC2-related actions unless the dataClassification tag is present. Apply these boundaries to all IAM roles used for EC2 provisioning
- (G) Correct options:
- (H) AWS Tag Policies, managed through AWS Organizations, allow administrators to define rules for tag keys and values. These policies do not directly prevent resource creation, but they help enforce tag consistency and visibility by flagging noncompliant resources.
- (I) Service Control Policies (SCPs) allow you to centrally govern permissions for accounts in AWS Organizations. An SCP defines the maximum set of permissions available to IAM users and roles in an account. When combined with condition keys, SCPs can enforce fine-grained controls on specific operations.
- (J) via - https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps_examples_tagging.html
- () Incorrect options:
- () Create a tag enforcement Lambda function that runs on a schedule to identify EC2 instances without the required tag. The function sends a notification to administrators and optionally shuts down noncompliant resources - This reactive approach relies on periodic audits rather than enforcing tagging at the time of resource creation. It increases operational overhead and cannot guarantee immediate compliance, especially for short-lived resources.
- () Use AWS Identity and Access Management (IAM) permission boundaries to restrict EC2-related actions unless the dataClassification tag is present. Apply these boundaries to all IAM roles used for EC2 provisioning - While IAM permission boundaries can restrict actions within a boundary, they are not designed to enforce tag-based controls across all users or to prevent tag deletion. SCPs and tag policies are more appropriate at the organizational level.
- () Enable AWS Config rules to detect noncompliant EC2 instances. Trigger an AWS Systems Manager Automation runbook to reapply missing tags automatically when noncompliance is detected - AWS Config and automation runbooks offer remediation, but do not prevent noncompliant resources from being created in the first place. This violates the requirement for proactive enforcement and minimal public exposure of misclassified data.
- () References:
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_tag-policies.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps_examples_tagging.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html
- () The engineering team at a retail company manages 3 Amazon EC2 instances that make read-heavy database requests to the Amazon RDS for the PostgreSQL database instance. As an AWS Certified Solutions Architect - Associate, you have been tasked to make the database instance resilient from a disaster recovery perspective.
- () Which of the following features will help you in disaster recovery of the database? (Select two)
- () Use Amazon RDS Provisioned IOPS (SSD) Storage in place of General Purpose (SSD) Storage
- () Enable the automated backup feature of Amazon RDS in a multi-AZ deployment that creates backups across multiple Regions
- () Use the database cloning feature of the Amazon RDS Database cluster
- () Use cross-Region Read Replicas
- () Enable the automated backup feature of Amazon RDS in a multi-AZ deployment that creates backups in a single AWS Region
- () In addition to using Read Replicas to reduce the load on your source database instance, you can also use Read Replicas to implement a DR solution for your production DB environment. If the source DB instance fails, you can promote your Read Replica to a standalone source server. Read Replicas can also be created in a different Region than the source database. Using a cross-Region Read Replica can help ensure that you get back up and running if you experience a regional availability issue.
- () Amazon RDS provides high availability and failover support for database instances using Multi-AZ deployments. Amazon RDS uses several different technologies to provide failover support. Multi-AZ deployments for MariaDB, MySQL, Oracle, and PostgreSQL DB instances use Amazon's failover technology.
- () The automated backup feature of Amazon RDS enables point-in-time recovery for your database instance. Amazon RDS will back up your database and transaction logs and store both for a user-specified retention period. If it’s a Multi-AZ configuration, backups occur on standby to reduce the I/O impact on the primary. Amazon RDS supports Cross-Region Automated Backups. Manual snapshots and Read Replicas are also supported across multiple Regions.
- () Enable the automated backup feature of Amazon RDS in a multi-AZ deployment that creates backups in a single AWS Region - This is an incorrect statement. Automated backups can be created across AWS Regions.
- () Use Amazon RDS Provisioned IOPS (SSD) Storage in place of General Purpose (SSD) Storage - Amazon RDS Provisioned IOPS Storage is an SSD-backed storage option designed to deliver fast, predictable, and consistent I/O performance. This storage type enhances the performance of the RDS database, but this isn't a disaster recovery option.
- () Use the database cloning feature of the Amazon RDS Database cluster - This option has been added as a distractor. Database cloning is only available for Amazon Aurora and not for Amazon RDS.
- () https://aws.amazon.com/rds/features/
- () https://aws.amazon.com/blogs/database/implementing-a-disaster-recovery-strategy-with-amazon-rds/
- () https://aws.amazon.com/about-aws/whats-new/2021/07/amazon-rds-cross-region-automated-backups-regional-expansion/

**Answer:**
Correct Answer: **Enable AWS Config rules to detect noncompliant EC2 instances. Trigger an AWS Systems Manager Automation runbook to reapply missing tags automatically when noncompliance is detected**

---

## Question 142

**Q:** Which of the following features will help you in disaster recovery of the database? (Select two)

**Options:**
- (A) Use Amazon RDS Provisioned IOPS (SSD) Storage in place of General Purpose (SSD) Storage
- (B) Correct selection
- (C) Enable the automated backup feature of Amazon RDS in a multi-AZ deployment that creates backups across multiple Regions
- (D) Use the database cloning feature of the Amazon RDS Database cluster
- (E) Use cross-Region Read Replicas
- (F) Enable the automated backup feature of Amazon RDS in a multi-AZ deployment that creates backups in a single AWS Region
- (G) Correct options:
- (H) In addition to using Read Replicas to reduce the load on your source database instance, you can also use Read Replicas to implement a DR solution for your production DB environment. If the source DB instance fails, you can promote your Read Replica to a standalone source server. Read Replicas can also be created in a different Region than the source database. Using a cross-Region Read Replica can help ensure that you get back up and running if you experience a regional availability issue.
- (I) Amazon RDS provides high availability and failover support for database instances using Multi-AZ deployments. Amazon RDS uses several different technologies to provide failover support. Multi-AZ deployments for MariaDB, MySQL, Oracle, and PostgreSQL DB instances use Amazon's failover technology.
- (J) The automated backup feature of Amazon RDS enables point-in-time recovery for your database instance. Amazon RDS will back up your database and transaction logs and store both for a user-specified retention period. If it’s a Multi-AZ configuration, backups occur on standby to reduce the I/O impact on the primary. Amazon RDS supports Cross-Region Automated Backups. Manual snapshots and Read Replicas are also supported across multiple Regions.
- () Incorrect options:
- () Enable the automated backup feature of Amazon RDS in a multi-AZ deployment that creates backups in a single AWS Region - This is an incorrect statement. Automated backups can be created across AWS Regions.
- () Use Amazon RDS Provisioned IOPS (SSD) Storage in place of General Purpose (SSD) Storage - Amazon RDS Provisioned IOPS Storage is an SSD-backed storage option designed to deliver fast, predictable, and consistent I/O performance. This storage type enhances the performance of the RDS database, but this isn't a disaster recovery option.
- () Use the database cloning feature of the Amazon RDS Database cluster - This option has been added as a distractor. Database cloning is only available for Amazon Aurora and not for Amazon RDS.
- () References:
- () https://aws.amazon.com/rds/features/
- () https://aws.amazon.com/blogs/database/implementing-a-disaster-recovery-strategy-with-amazon-rds/
- () https://aws.amazon.com/about-aws/whats-new/2021/07/amazon-rds-cross-region-automated-backups-regional-expansion/
- () Which solution should a solutions architect recommend to meet these requirements?
- () Use Amazon RDS for MySQL with a cross-Region read replica. Route all writes to the primary Region and use read replicas for local access in other Regions
- () Use Amazon Aurora database with MySQL engine, and configure read-only nodes in other Regions to handle local traffic while routing all write operations to the central Region
- **() Migrate the order data to Amazon DynamoDB and create a global table. Deploy the application in each Region and connect to the local DynamoDB replica for low-latency access** [CORRECT]
- () Use Amazon Neptune to store tracking updates as graph data. Deploy clusters in each Region and replicate changes using custom-built Lambda functions and Amazon SQS.
- () Correct option:
- () This solution also eliminates the need to manage complex replication logic, ensures high resilience against Regional failures, and provides seamless multi-active availability—allowing each Region to continue operating independently even if another Region experiences disruption.
- () https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/GlobalTables.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.XRgn.html
- () A medical devices company uses Amazon S3 buckets to store critical data. Hundreds of buckets are used to keep the data segregated and well organized. Recently, the development team noticed that the lifecycle policies on the Amazon S3 buckets have not been applied optimally, resulting in higher costs.

**Answer:**
Correct Answer: **Migrate the order data to Amazon DynamoDB and create a global table. Deploy the application in each Region and connect to the local DynamoDB replica for low-latency access**

---

## Question 143

**Q:** As a Solutions Architect, can you recommend a solution to reduce storage costs on Amazon S3 while keeping the IT team's involvement to a minimum?

**Options:**
- (A) Use Amazon S3 Outposts storage class to reduce the costs on Amazon S3 storage by storing the data on-premises
- (B) Use Amazon S3 One Zone-Infrequent Access, to reduce the costs on Amazon S3 storage
- **(C) Use Amazon S3 Intelligent-Tiering storage class to optimize the Amazon S3 storage costs** [CORRECT]
- (D) Configure Amazon EFS to provide a fast, cost-effective and sharable storage service
- (E) Correct option:
- (F) The Amazon S3 Intelligent-Tiering storage class is designed to optimize costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead. It works by storing objects in two access tiers: one tier that is optimized for frequent access and another lower-cost tier that is optimized for infrequent access.
- (G) Amazon S3 Storage Classes can be configured at the object level and a single bucket can contain objects stored in Amazon S3 Standard, Amazon S3 Intelligent-Tiering, Amazon S3 Standard-IA, and Amazon S3 One Zone-IA. You can upload objects directly to Amazon S3 Intelligent-Tiering, or use S3 Lifecycle policies to transfer objects from Amazon S3 Standard and Amazon S3 Standard-IA to Amazon S3 Intelligent-Tiering. You can also archive objects from Amazon S3 Intelligent-Tiering to Amazon S3 Glacier.
- (H) Incorrect options:
- (I) Use Amazon S3 Outposts storage class to reduce the costs on Amazon S3 storage by storing the data on-premises - This is a distractor as Amazon S3 on Outposts (S3 Outposts) delivers object storage to your on-premises AWS Outposts environment. It is used in conjunction with AWS Outposts and has no relevance to the current use case.
- (J) Reference:
- () https://aws.amazon.com/s3/storage-classes/

**Answer:**
Correct Answer: **Use Amazon S3 Intelligent-Tiering storage class to optimize the Amazon S3 storage costs**

---

## Question 144

**Q:** As a solutions architect, which of the following would you recommend as the MOST resource-efficient and scalable solution?

**Options:**
- (A) Use an internet gateway to interconnect the VPCs
- **(B) Use AWS transit gateway to interconnect the VPCs** [CORRECT]
- (C) Use a VPC endpoint to interconnect the VPCs
- (D) Establish VPC peering connections between all VPCs
- (E) Correct option:
- (F) An AWS transit gateway is a network transit hub that you can use to interconnect your virtual private clouds (VPC) and on-premises networks.
- (G) AWS Transit Gateway Overview:
- (H) via - https://docs.aws.amazon.com/vpc/latest/tgw/what-is-transit-gateway.html
- (I) VPC Peering Connections Overview:
- (J) via - https://docs.aws.amazon.com/vpc/latest/peering/vpc-peering-basics.html
- () Incorrect options:
- () Use an internet gateway to interconnect the VPCs - An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet. It, therefore, imposes no availability risks or bandwidth constraints on your network traffic. You cannot use an internet gateway to interconnect your VPCs and on-premises networks, hence this option is incorrect.
- () Use a VPC endpoint to interconnect the VPCs - A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. You cannot use a VPC endpoint to interconnect your VPCs and on-premises networks, hence this option is incorrect.
- () Establish VPC peering connections between all VPCs - Establishing VPC peering between all VPCs is an inelegant and clumsy way to establish connectivity between all VPCs. Instead, you should use a Transit Gateway that acts as a network transit hub to interconnect your VPCs and on-premises networks.
- () References:
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html
- () https://docs.aws.amazon.com/vpc/latest/tgw/what-is-transit-gateway.html
- () A Customer relationship management (CRM) application is facing user experience issues with users reporting frequent sign-in requests from the application. The application is currently hosted on multiple Amazon EC2 instances behind an Application Load Balancer. The engineering team has identified the root cause as unhealthy servers causing session data to be lost. The team would like to implement a distributed in-memory cache-based session management solution.

**Answer:**
Correct Answer: **Use AWS transit gateway to interconnect the VPCs**

---

## Question 145

**Q:** As a Solutions Architect, which of the following configurations would you select as the best fit for these requirements?

**Options:**
- (A) The Auto Scaling group should be configured with the minimum capacity set to 2, with 1 instance each in two different Availability Zones. The maximum capacity of the Auto Scaling group should be set to 6
- (B) The Auto Scaling group should be configured with the minimum capacity set to 2 and the maximum capacity set to 6 in a single Availability Zone
- **(C) The Auto Scaling group should be configured with the minimum capacity set to 4, with 2 instances each in two different Availability Zones. The maximum capacity of the Auto Scaling group should be set to 6** [CORRECT]
- (D) The Auto Scaling group should be configured with the minimum capacity set to 4, with 2 instances each in two different AWS Regions. The maximum capacity of the Auto Scaling group should be set to 6
- (E) Correct option:
- (F) You configure the size of your Auto Scaling group by setting the minimum, maximum, and desired capacity. The minimum and maximum capacity are required to create an Auto Scaling group, while the desired capacity is optional. If you do not define your desired capacity upfront, it defaults to your minimum capacity.
- (G) Amazon EC2 Auto Scaling attempts to distribute instances evenly between the Availability Zones that are enabled for your Auto Scaling group. This is why the minimum capacity should be 4 instances and not 2. Auto Scaling group will launch 2 instances each in both the AZs and this redundancy is needed to keep the service available always.
- (H) Incorrect options:
- (I) The explanation above gives the correct rationale for minimum capacity as well as the instance distribution across AZs, so both these options are incorrect.
- (J) The Auto Scaling group should be configured with the minimum capacity set to 4, with 2 instances each in two different AWS Regions. The maximum capacity of the Auto Scaling group should be set to 6 - An Auto Scaling group can contain Amazon EC2 instances in one or more Availability Zones within the same region. However, Auto Scaling groups cannot span multiple Regions.
- () Reference:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/auto-scaling-benefits.html
- () An e-commerce company uses Amazon Simple Queue Service (Amazon SQS) queues to decouple their application architecture. The engineering team has observed message processing failures for some customer orders.

**Answer:**
Correct Answer: **The Auto Scaling group should be configured with the minimum capacity set to 4, with 2 instances each in two different Availability Zones. The maximum capacity of the Auto Scaling group should be set to 6**

---

## Question 146

**Q:** As a solutions architect, which of the following solutions would you recommend for handling such message failures?

**Options:**
- (A) Use long polling to handle message processing failures
- (B) Use a dead-letter queue to handle message processing failures
- (C) Use a temporary queue to handle message processing failures
- (D) Use short polling to handle message processing failures
- (E) Correct option:
- (F) How do dead-letter queues work?:
- (G) via - https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html
- (H) Incorrect options:
- (I) Reference:
- (J) https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html
- () The content division at a digital media agency has an application that generates a large number of files on Amazon S3, each approximately 10 megabytes in size. The agency mandates that the files be stored for 5 years before they can be deleted. The files are frequently accessed in the first 30 days of the object creation but are rarely accessed after the first 30 days. The files contain critical business data that is not easy to reproduce, therefore, immediate accessibility is always required.
- () Which solution is the MOST cost-effective for the given use case?
- **() Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Delete the files 5 years after object creation** [CORRECT]
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Archive the files to Amazon S3 Glacier Deep Archive 5 years after object creation
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 One Zone-IA 30 days after object creation. Delete the files 5 years after object creation
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Glacier Flexible Retrieval 30 days after object creation. Delete the files 5 years after object creation
- () Amazon S3 Standard-IA class is for data that is accessed less frequently but requires rapid access when needed. Amazon S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per gigabyte storage price and per GB retrieval charge.
- () via - https://aws.amazon.com/s3/storage-classes/
- () For the given use case, you can set up an Amazon S3 lifecycle configuration and create a transition action to move objects from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. You can set up an expiration action to delete the object 5 years after object creation.
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Glacier Flexible Retrieval 30 days after object creation. Delete the files 5 years after object creation - Amazon S3 Glacier Flexible Retrieval storage class has the best case retrieval time of the order of minutes, so this option is incorrect for the given requirement.
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Archive the files to Amazon S3 Glacier Deep Archive 5 years after object creation - The files can simply be deleted 5 years after object creation instead of archiving the files to Amazon S3 Glacier Deep Archive. There is no need to incur the cost of archival.
- () References:
- () https://aws.amazon.com/s3/storage-classes/
- () https://aws.amazon.com/s3/storage-classes/glacier/
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html
- () The engineering team at an e-commerce company uses an AWS Lambda function to write the order data into a single DB instance Amazon Aurora cluster. The team has noticed that many order- writes to its Aurora cluster are getting missed during peak load times. The diagnostics data has revealed that the database is experiencing high CPU and memory consumption during traffic spikes. The team also wants to enhance the availability of the Aurora DB.
- () Which of the following steps would you combine to address the given scenario? (Select two)
- () Correct selection

**Answer:**
Correct Answer: **Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Delete the files 5 years after object creation**

---

## Question 147

**Q:** How do dead-letter queues work?:

**Options:**
- (A) via - https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html
- (B) Incorrect options:
- (C) Use short polling to handle message processing failures
- (D) Use long polling to handle message processing failures
- (E) Reference:
- (F) https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dead-letter-queues.html
- (G) The content division at a digital media agency has an application that generates a large number of files on Amazon S3, each approximately 10 megabytes in size. The agency mandates that the files be stored for 5 years before they can be deleted. The files are frequently accessed in the first 30 days of the object creation but are rarely accessed after the first 30 days. The files contain critical business data that is not easy to reproduce, therefore, immediate accessibility is always required.
- (H) Which solution is the MOST cost-effective for the given use case?
- **(I) Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Delete the files 5 years after object creation** [CORRECT]
- (J) Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Archive the files to Amazon S3 Glacier Deep Archive 5 years after object creation
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 One Zone-IA 30 days after object creation. Delete the files 5 years after object creation
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Glacier Flexible Retrieval 30 days after object creation. Delete the files 5 years after object creation
- () Correct option:
- () Amazon S3 Standard-IA class is for data that is accessed less frequently but requires rapid access when needed. Amazon S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per gigabyte storage price and per GB retrieval charge.
- () via - https://aws.amazon.com/s3/storage-classes/
- () For the given use case, you can set up an Amazon S3 lifecycle configuration and create a transition action to move objects from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. You can set up an expiration action to delete the object 5 years after object creation.
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Glacier Flexible Retrieval 30 days after object creation. Delete the files 5 years after object creation - Amazon S3 Glacier Flexible Retrieval storage class has the best case retrieval time of the order of minutes, so this option is incorrect for the given requirement.
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Archive the files to Amazon S3 Glacier Deep Archive 5 years after object creation - The files can simply be deleted 5 years after object creation instead of archiving the files to Amazon S3 Glacier Deep Archive. There is no need to incur the cost of archival.
- () References:
- () https://aws.amazon.com/s3/storage-classes/
- () https://aws.amazon.com/s3/storage-classes/glacier/
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html
- () The engineering team at an e-commerce company uses an AWS Lambda function to write the order data into a single DB instance Amazon Aurora cluster. The team has noticed that many order- writes to its Aurora cluster are getting missed during peak load times. The diagnostics data has revealed that the database is experiencing high CPU and memory consumption during traffic spikes. The team also wants to enhance the availability of the Aurora DB.
- () Which of the following steps would you combine to address the given scenario? (Select two)
- () Correct selection
- () Handle all read operations for your application by connecting to the reader endpoint of the Amazon Aurora cluster so that Aurora can spread the load for read-only connections across the Aurora replica
- () Create a standby Aurora instance in another Availability Zone to improve the availability as the standby can serve as a failover target
- () Create a replica Aurora instance in another Availability Zone to improve the availability as the replica can serve as a failover target
- () Use Amazon EC2 instances behind an Application Load Balancer to write the order data into Amazon Aurora cluster
- () Increase the concurrency of the AWS Lambda function so that the order-writes do not get missed during traffic spikes
- () Correct options:
- () When you create a second, third, and so on DB instance in an Aurora-provisioned DB cluster, Aurora automatically sets up replication from the writer DB instance to all the other DB instances. These other DB instances are read-only and are known as Aurora Replicas.

**Answer:**
Correct Answer: **Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Delete the files 5 years after object creation**

---

## Question 148

**Q:** Which solution is the MOST cost-effective for the given use case?

**Options:**
- **(A) Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Delete the files 5 years after object creation** [CORRECT]
- (B) Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Archive the files to Amazon S3 Glacier Deep Archive 5 years after object creation
- (C) Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 One Zone-IA 30 days after object creation. Delete the files 5 years after object creation
- (D) Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Glacier Flexible Retrieval 30 days after object creation. Delete the files 5 years after object creation
- (E) Correct option:
- (F) Amazon S3 Standard-IA class is for data that is accessed less frequently but requires rapid access when needed. Amazon S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per gigabyte storage price and per GB retrieval charge.
- (G) via - https://aws.amazon.com/s3/storage-classes/
- (H) For the given use case, you can set up an Amazon S3 lifecycle configuration and create a transition action to move objects from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. You can set up an expiration action to delete the object 5 years after object creation.
- (I) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- (J) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html
- () Incorrect options:
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Glacier Flexible Retrieval 30 days after object creation. Delete the files 5 years after object creation - Amazon S3 Glacier Flexible Retrieval storage class has the best case retrieval time of the order of minutes, so this option is incorrect for the given requirement.
- () Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Archive the files to Amazon S3 Glacier Deep Archive 5 years after object creation - The files can simply be deleted 5 years after object creation instead of archiving the files to Amazon S3 Glacier Deep Archive. There is no need to incur the cost of archival.
- () References:
- () https://aws.amazon.com/s3/storage-classes/
- () https://aws.amazon.com/s3/storage-classes/glacier/
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/lifecycle-transition-general-considerations.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-lifecycle-mgmt.html
- () The engineering team at an e-commerce company uses an AWS Lambda function to write the order data into a single DB instance Amazon Aurora cluster. The team has noticed that many order- writes to its Aurora cluster are getting missed during peak load times. The diagnostics data has revealed that the database is experiencing high CPU and memory consumption during traffic spikes. The team also wants to enhance the availability of the Aurora DB.
- () Which of the following steps would you combine to address the given scenario? (Select two)
- () Correct selection
- () Handle all read operations for your application by connecting to the reader endpoint of the Amazon Aurora cluster so that Aurora can spread the load for read-only connections across the Aurora replica
- () Create a standby Aurora instance in another Availability Zone to improve the availability as the standby can serve as a failover target
- () Create a replica Aurora instance in another Availability Zone to improve the availability as the replica can serve as a failover target
- () Use Amazon EC2 instances behind an Application Load Balancer to write the order data into Amazon Aurora cluster
- () Increase the concurrency of the AWS Lambda function so that the order-writes do not get missed during traffic spikes
- () Correct options:
- () When you create a second, third, and so on DB instance in an Aurora-provisioned DB cluster, Aurora automatically sets up replication from the writer DB instance to all the other DB instances. These other DB instances are read-only and are known as Aurora Replicas.
- () via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
- () If the primary instance in a DB cluster using single-master replication fails, Aurora automatically fails over to a new primary instance in one of two ways:
- () By promoting an existing Aurora Replica to the new primary instance By creating a new primary instance
- () via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.AuroraHighAvailability.html
- () Create a standby Aurora instance in another Availability Zone to improve the availability as the standby can serve as a failover target - There are no standby instances in Aurora. Aurora performs an automatic failover to a read replica when a problem is detected. So this option is incorrect.
- () Read replicas, Multi-AZ deployments, and multi-region deployments: 
- () via - https://aws.amazon.com/rds/features/read-replicas/

**Answer:**
Correct Answer: **Set up an Amazon S3 bucket lifecycle policy to move files from Amazon S3 Standard to Amazon S3 Standard-IA 30 days after object creation. Delete the files 5 years after object creation**

---

## Question 149

**Q:** Which of the following steps would you combine to address the given scenario? (Select two)

**Options:**
- (A) Correct selection
- (B) Handle all read operations for your application by connecting to the reader endpoint of the Amazon Aurora cluster so that Aurora can spread the load for read-only connections across the Aurora replica
- (C) Create a standby Aurora instance in another Availability Zone to improve the availability as the standby can serve as a failover target
- (D) Create a replica Aurora instance in another Availability Zone to improve the availability as the replica can serve as a failover target
- (E) Use Amazon EC2 instances behind an Application Load Balancer to write the order data into Amazon Aurora cluster
- (F) Increase the concurrency of the AWS Lambda function so that the order-writes do not get missed during traffic spikes
- (G) Correct options:
- (H) When you create a second, third, and so on DB instance in an Aurora-provisioned DB cluster, Aurora automatically sets up replication from the writer DB instance to all the other DB instances. These other DB instances are read-only and are known as Aurora Replicas.
- (I) via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
- (J) If the primary instance in a DB cluster using single-master replication fails, Aurora automatically fails over to a new primary instance in one of two ways:
- () By promoting an existing Aurora Replica to the new primary instance By creating a new primary instance
- () via - https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.AuroraHighAvailability.html
- () Incorrect options:
- () Create a standby Aurora instance in another Availability Zone to improve the availability as the standby can serve as a failover target - There are no standby instances in Aurora. Aurora performs an automatic failover to a read replica when a problem is detected. So this option is incorrect.
- () Read replicas, Multi-AZ deployments, and multi-region deployments: 
- () via - https://aws.amazon.com/rds/features/read-replicas/
- () Increase the concurrency of the AWS Lambda function so that the order-writes do not get missed during traffic spikes - Increasing the concurrency of the AWS Lambda function would not resolve the issue since the bottleneck is at the database layer, as exhibited by the high CPU and memory consumption for the Aurora instance. This option has been added as a distractor.
- () Use Amazon EC2 instances behind an Application Load Balancer to write the order data into Amazon Aurora cluster - Using Amazon EC2 instances behind an Application Load Balancer would not resolve the issue since the bottleneck is at the database layer, as exhibited by the high CPU and memory consumption for the Aurora instance. This option has been added as a distractor.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.AuroraHighAvailability.html
- () https://aws.amazon.com/rds/features/read-replicas/
- () Which solution offers the most cost-effective architecture?
- **() Create an Amazon S3 bucket with Intelligent-Tiering enabled. Update the application to store and retrieve project files using the Amazon S3 API** [CORRECT]
- () Replace the EFS file system with Amazon FSx for Lustre. Mount the file system to EC2 instances and store project files there to reduce access latency and cost
- () Replace the EFS file system with Amazon FSx for NetApp ONTAP. Use volume tiering to move cold data to lower-cost capacity pool storage. Update the application to use the ONTAP mount path
- () Use AWS Backup to export all EFS files daily to an Amazon S3 bucket. Retain the EFS file system in Standard-IA class for occasional real-time access and route all archival queries to the S3 export
- () Correct option:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/intelligent-tiering-overview.html
- () https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html
- () https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html
- () https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/what-is-fsx-ontap.html

**Answer:**
Correct Answer: **Create an Amazon S3 bucket with Intelligent-Tiering enabled. Update the application to store and retrieve project files using the Amazon S3 API**

---

## Question 150

**Q:** Which solution offers the most cost-effective architecture?

**Options:**
- (A) Create an Amazon S3 bucket with Intelligent-Tiering enabled. Update the application to store and retrieve project files using the Amazon S3 API
- (B) Replace the EFS file system with Amazon FSx for Lustre. Mount the file system to EC2 instances and store project files there to reduce access latency and cost
- (C) Replace the EFS file system with Amazon FSx for NetApp ONTAP. Use volume tiering to move cold data to lower-cost capacity pool storage. Update the application to use the ONTAP mount path
- (D) Use AWS Backup to export all EFS files daily to an Amazon S3 bucket. Retain the EFS file system in Standard-IA class for occasional real-time access and route all archival queries to the S3 export
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/AmazonS3/latest/userguide/intelligent-tiering-overview.html
- (I) https://docs.aws.amazon.com/fsx/latest/LustreGuide/what-is.html
- (J) https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html
- () https://docs.aws.amazon.com/fsx/latest/ONTAPGuide/what-is-fsx-ontap.html
- () Which solution best meets these requirements?
- () Establish a dedicated AWS Direct Connect connection between the corporate network and AWS. Configure VPC route tables to control traffic flow and use security groups and network ACLs to restrict access as needed
- () Set up AWS Site-to-Site VPN to connect the on-premises network to the AWS VPC. Use route tables to manage traffic flow and configure security groups and network ACLs to allow only authorized communication between systems
- () Use AWS Client VPN to allow corporate users to connect to the VPC individually. Manage access controls with security groups and IAM policies
- () Set up a bastion host in a public subnet of the VPC to provide SSH-based access to AWS resources from the corporate network. Use security groups to control access
- () Correct options:
- () AWS Site-to-Site VPN uses IPsec tunnels, which provide encryption at the network layer, ensuring that traffic is securely transmitted between the on-premises network and the VPC. By applying security groups and network ACLs, fine-grained traffic control is possible. Additionally, session-layer encryption (e.g., HTTPS, TLS) can be layered on top, satisfying both encryption requirements with minimal overhead. This is the most cost-effective and secure solution for the given requirements.
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPC_VPN.html
- () https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/what-is.html
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/encryption-in-transit.html
- () A digital media startup allows users to submit images through its web portal. These images are uploaded directly into an Amazon S3 bucket. On average, around 200 images are uploaded daily. The company wants to automatically generate a smaller preview version (thumbnail) of each new image and store the resulting thumbnails in a separate Amazon S3 bucket. The team prefers a design that is low-cost, requires minimal infrastructure management, and automatically reacts to new uploads.
- () Which solution will meet these requirements MOST cost-effectively?
- () Enable Amazon S3 Access Analyzer and configure it to call an AWS Lambda function whenever a new image is added. Use the Lambda function to generate and store the thumbnail
- **() Configure the S3 bucket to send an event notification to an AWS Lambda function each time a new image is uploaded. Use the Lambda function to process the image, create a thumbnail, and store the thumbnail in the second S3 bucket** [CORRECT]
- () Deploy a containerized application on AWS Fargate that polls the S3 bucket every minute to detect new uploads. Configure the container to generate thumbnails and save them in the second bucket
- () Set up a step-based processing workflow using AWS Glue jobs triggered on a regular interval. Use the jobs to scan the primary S3 bucket for new files and generate thumbnails for any that lack them. Write the thumbnails to a second S3 bucket
- () Set up a step-based processing workflow using AWS Glue jobs triggered on a regular interval. Use the jobs to scan the primary S3 bucket for new files and generate thumbnails for any that lack them. Write the thumbnails to a second S3 bucket - AWS Glue is designed for ETL (Extract, Transform, Load) operations on structured and semi-structured data, not real-time image processing. Running Glue jobs on a schedule for this use case introduces unnecessary complexity and cost.
- () Deploy a containerized application on AWS Fargate that polls the S3 bucket every minute to detect new uploads. Configure the container to generate thumbnails and save them in the second bucket - While Fargate is serverless, continuously polling the S3 bucket is inefficient and incurs costs even when no new images are present. It also adds operational complexity compared to event-driven processing.
- () Enable Amazon S3 Access Analyzer and configure it to call an AWS Lambda function whenever a new image is added. Use the Lambda function to generate and store the thumbnail - S3 Access Analyzer is used for auditing and security analysis, not event-driven processing or triggering Lambda functions. It cannot be used to detect object uploads or initiate thumbnail generation.

**Answer:**
Correct Answer: **Configure the S3 bucket to send an event notification to an AWS Lambda function each time a new image is uploaded. Use the Lambda function to process the image, create a thumbnail, and store the thumbnail in the second S3 bucket**

---

## Question 151

**Q:** As a Solutions Architect, which of the following will you identify as the outcome of the scenario?

**Options:**
- (A) The application will be down until the primary database has recovered itself
- (B) An email will be sent to the System Administrator asking for manual intervention
- (C) The URL to access the database will change to the standby database
- **(D) The CNAME record will be updated to point to the standby database** [CORRECT]
- (E) Correct option:
- (F) Amazon RDS provides high availability and failover support for DB instances using Multi-AZ deployments. Amazon RDS uses several different technologies to provide failover support. Multi-AZ deployments for MariaDB, MySQL, Oracle, and PostgreSQL DB instances use Amazon's failover technology. SQL Server DB instances use SQL Server Database Mirroring (DBM) or Always On Availability Groups (AGs).
- (G) Failover is automatically handled by Amazon RDS so that you can resume database operations as quickly as possible without administrative intervention. When failing over, Amazon RDS simply flips the canonical name record (CNAME) for your DB instance to point at the standby, which is in turn promoted to become the new primary. Multi-AZ means the URL is the same, the failover is automated, and the CNAME will automatically be updated to point to the standby database.
- (H) Incorrect options:
- (I) The URL to access the database will change to the standby database - As discussed above, URL remains the same.
- (J) An email will be sent to the System Administrator asking for manual intervention - This option is incorrect and it has been added as a distractor.
- () The application will be down until the primary database has recovered itself - This option is incorrect and it has been added as a distractor.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.MultiAZ.html
- () https://aws.amazon.com/rds/faqs/
- () Which combination of solutions will meet these requirements? (Select two)
- () Correct selection
- () Use an Auto Scaling group to deploy EC2 instances across multiple Availability Zones within a single Region. Register the instances in a target group behind an Application Load Balancer to distribute web traffic evenly
- () Use an Auto Scaling group to deploy EC2 instances across multiple Availability Zones in two AWS Regions. Register the instances in a target group behind an Application Load Balancer to distribute web traffic evenly
- () Migrate the existing MySQL database to an Amazon Aurora MySQL cluster. Deploy the primary DB instance and one or more read replicas in different Availability Zones
- () Use Amazon CloudFront with Lambda@Edge to serve dynamic content from EC2 instances located in different Regions
- () Deploy an additional EC2 instance in a different AWS Region, and configure Amazon Route 53 with a failover routing policy to direct traffic to the secondary instance during primary Region outages
- () Correct options:
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () Use an Auto Scaling group to deploy EC2 instances across multiple Availability Zones in two AWS Regions. Register the instances in a target group behind an Application Load Balancer to distribute web traffic evenly - An Application Load Balancer operates only within a single AWS Region and can route traffic to targets in multiple Availability Zones within that Region, but not across Regions. So, this option is incorrect.
- () Use Amazon CloudFront with Lambda@Edge to serve dynamic content from EC2 instances located in different Regions - CloudFront is ideal for caching static content, but it’s not designed for dynamic database-driven applications hosted on EC2. Using Lambda@Edge for a database-backed application introduces architectural mismatches and increases complexity.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html

**Answer:**
Correct Answer: **The CNAME record will be updated to point to the standby database**

---

## Question 152

**Q:** Which combination of solutions will meet these requirements? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Use an Auto Scaling group to deploy EC2 instances across multiple Availability Zones within a single Region. Register the instances in a target group behind an Application Load Balancer to distribute web traffic evenly
- (C) Use an Auto Scaling group to deploy EC2 instances across multiple Availability Zones in two AWS Regions. Register the instances in a target group behind an Application Load Balancer to distribute web traffic evenly
- (D) Migrate the existing MySQL database to an Amazon Aurora MySQL cluster. Deploy the primary DB instance and one or more read replicas in different Availability Zones
- (E) Use Amazon CloudFront with Lambda@Edge to serve dynamic content from EC2 instances located in different Regions
- (F) Deploy an additional EC2 instance in a different AWS Region, and configure Amazon Route 53 with a failover routing policy to direct traffic to the secondary instance during primary Region outages
- (G) Correct options:
- (H) via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- (I) Incorrect options:
- (J) Use an Auto Scaling group to deploy EC2 instances across multiple Availability Zones in two AWS Regions. Register the instances in a target group behind an Application Load Balancer to distribute web traffic evenly - An Application Load Balancer operates only within a single AWS Region and can route traffic to targets in multiple Availability Zones within that Region, but not across Regions. So, this option is incorrect.
- () Use Amazon CloudFront with Lambda@Edge to serve dynamic content from EC2 instances located in different Regions - CloudFront is ideal for caching static content, but it’s not designed for dynamic database-driven applications hosted on EC2. Using Lambda@Edge for a database-backed application introduces architectural mismatches and increases complexity.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html

**Answer:**
Correct Answer: **Correct selection**

---

## Question 153

**Q:** Which solution best meets these requirements while ensuring the least operational overhead?

**Options:**
- (A) Use a combination of AWS Lambda functions and EC2 Spot Instances for processing. Store processed images in Amazon FSx
- **(B) Use AWS Batch to process image jobs. Orchestrate the workflow using AWS Step Functions and store output files in Amazon S3** [CORRECT]
- (C) Deploy Amazon Elastic Kubernetes Service (Amazon EKS) with self-managed EC2 worker nodes for image processing. Use Amazon SQS to queue jobs and store processed outputs in Amazon EBS volumes
- (D) Use Amazon EC2 Auto Scaling groups with a static fleet of instances for image processing. Trigger each job through Step Functions and store results on attached EBS volumes
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html
- (I) https://docs.aws.amazon.com/step-functions/latest/dg/welcome.html
- (J) https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html
- () A developer has configured inbound traffic for the relevant ports in both the Security Group of the Amazon EC2 instance as well as the network access control list (network ACL) of the subnet for the Amazon EC2 instance. The developer is, however, unable to connect to the service running on the Amazon EC2 instance.

**Answer:**
Correct Answer: **Use AWS Batch to process image jobs. Orchestrate the workflow using AWS Step Functions and store output files in Amazon S3**

---

## Question 154

**Q:** Which of the following is the MOST cost-optimal solution to fix this issue?

**Options:**
- (A) Enable Multi-AZ for the Amazon RDS database and run the analytics workload on the standby database
- **(B) Create a Read Replica in the same Region as the Master database and point the analytics workload there** [CORRECT]
- (C) Create a Read Replica in another Region as the Master database and point the analytics workload there
- (D) Migrate the analytics application to AWS Lambda
- (E) Correct option:
- (F) Creating a Read Replica is the answer. As we want to minimize the costs, we need to launch the Read Replica in the same Region as you are not charged for the data transfer incurred in replicating data between your source database instance and read replica within the same AWS Region.
- (G) Exam Alert:
- (H) Please review this comparison vis-a-vis Multi-AZ vs Read Replica for Amazon RDS:
- (I) via - https://aws.amazon.com/rds/features/multi-az/
- (J) Incorrect options:
- () Enabling Multi-AZ helps make our database highly-available, but the standby database is not accessible and cannot be used for reads or write. It's just a database that will become primary when the other database encounters a failure. So this option is not correct.
- () Migrate the analytics application to AWS Lambda- AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume.
- () Running the application on AWS Lambda will not help, as it will still run against the main database and slow down our e-commerce application.
- () Create a Read Replica in another Region as the Master database and point the analytics workload there - This is incorrect because we have to pay for inter-Region data replication charges for the Read Replica, whereas the replication of data within a single Region is free.
- () References:
- () https://aws.amazon.com/rds/features/multi-az/
- () https://aws.amazon.com/rds/features/read-replicas/
- () A financial services company is looking to move its on-premises IT infrastructure to AWS Cloud. The company has multiple long-term server bound licenses across the application stack and the CTO wants to continue to utilize those licenses while moving to AWS.

**Answer:**
Correct Answer: **Create a Read Replica in the same Region as the Master database and point the analytics workload there**

---

## Question 155

**Q:** As a solutions architect, which of the following would you recommend as the MOST cost-effective solution?

**Options:**
- (A) Use Amazon EC2 reserved instances (RI)
- (B) Use Amazon EC2 dedicated instances
- (C) Use Amazon EC2 on-demand instances
- (D) Use Amazon EC2 dedicated hosts
- (E) Correct option:
- (F) You can use Dedicated Hosts to launch Amazon EC2 instances on physical servers that are dedicated for your use. Dedicated Hosts give you additional visibility and control over how instances are placed on a physical server, and you can reliably use the same physical server over time. As a result, Dedicated Hosts enable you to use your existing server-bound software licenses like Windows Server and address corporate compliance and regulatory requirements.
- (G) Incorrect options:
- (H) Use Amazon EC2 dedicated instances - Dedicated instances are Amazon EC2 instances that run in a VPC on hardware that's dedicated to a single customer. Your dedicated instances are physically isolated at the host hardware level from instances that belong to other AWS accounts. Dedicated instances may share hardware with other instances from the same AWS account that are not dedicated instances. Dedicated instances cannot be used for existing server-bound software licenses.
- (I) Amazon EC2 presents a virtual computing environment, allowing you to use web service interfaces to launch instances with a variety of operating systems, load them with your custom application environment, manage your network’s access permissions, and run your image using as many or few systems as you desire.
- (J) Amazon EC2 provides the following purchasing options to enable you to optimize your costs based on your needs:
- () On-Demand Instances – Pay, by the second, for the instances that you launch.
- () Reserved Instances (RI) – Reduce your Amazon EC2 costs by making a commitment to a consistent instance configuration, including instance type and Region, for a term of 1 or 3 years.
- () Neither on-demand instances nor reserved instances can be used for existing server-bound software licenses.
- () References:
- () https://aws.amazon.com/ec2/dedicated-hosts/
- () https://aws.amazon.com/ec2/dedicated-hosts/faqs/
- () https://aws.amazon.com/ec2/pricing/dedicated-instances/
- () A company has multiple Amazon EC2 instances operating in a private subnet which is part of a custom VPC. These instances are running an image processing application that needs to access images stored on Amazon S3. Once each image is processed, the status of the corresponding record needs to be marked as completed in a Amazon DynamoDB table.
- () How would you go about providing private access to these AWS resources which are not part of this custom VPC?
- () Create a separate interface endpoint for Amazon S3 and Amazon DynamoDB each. Then connect to these services by adding these as targets in the route table of the custom VPC
- () Create a gateway endpoint for Amazon DynamoDB and add it as a target in the route table of the custom VPC. Create an Origin Access Identity for Amazon S3 and then connect to the S3 service using the private IP address
- () Create a gateway endpoint for Amazon S3 and add it as a target in the route table of the custom VPC. Create an interface endpoint for Amazon DynamoDB and then add it as a target in the route table of the custom VPC
- **() Create a separate gateway endpoint for Amazon S3 and Amazon DynamoDB each. Add two new target entries for these two gateway endpoints in the route table of the custom VPC** [CORRECT]
- () Endpoints are virtual devices. They are horizontally scaled, redundant, and highly available VPC components. They allow communication between instances in your VPC and services without imposing availability risks or bandwidth constraints on your network traffic.
- () A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.
- () There are two types of VPC endpoints: interface endpoints and gateway endpoints. An interface endpoint is an elastic network interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service.
- () A gateway endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service. The following AWS services are supported:
- () Amazon S3
- () Amazon DynamoDB
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html
- () https://aws.amazon.com/about-aws/whats-new/2024/03/amazon-dynamodb-aws-privatelink/
- () The engineering team at an e-commerce company wants to set up a custom domain for internal usage such as internaldomainexample.com. The team wants to use the private hosted zones feature of Amazon Route 53 to accomplish this.
- () Which of the following settings of the VPC need to be enabled? (Select two)
- () Correct selection
- () enableDnsSupport
- () enableDnsHostnames
- () enableDnsDomain

**Answer:**
Correct Answer: **Create a separate gateway endpoint for Amazon S3 and Amazon DynamoDB each. Add two new target entries for these two gateway endpoints in the route table of the custom VPC**

---

## Question 156

**Q:** How would you go about providing private access to these AWS resources which are not part of this custom VPC?

**Options:**
- (A) Create a separate interface endpoint for Amazon S3 and Amazon DynamoDB each. Then connect to these services by adding these as targets in the route table of the custom VPC
- (B) Create a gateway endpoint for Amazon DynamoDB and add it as a target in the route table of the custom VPC. Create an Origin Access Identity for Amazon S3 and then connect to the S3 service using the private IP address
- (C) Create a gateway endpoint for Amazon S3 and add it as a target in the route table of the custom VPC. Create an interface endpoint for Amazon DynamoDB and then add it as a target in the route table of the custom VPC
- (D) Create a separate gateway endpoint for Amazon S3 and Amazon DynamoDB each. Add two new target entries for these two gateway endpoints in the route table of the custom VPC
- (E) Correct option:
- (F) Endpoints are virtual devices. They are horizontally scaled, redundant, and highly available VPC components. They allow communication between instances in your VPC and services without imposing availability risks or bandwidth constraints on your network traffic.
- (G) A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.
- (H) There are two types of VPC endpoints: interface endpoints and gateway endpoints. An interface endpoint is an elastic network interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service.
- (I) A gateway endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service. The following AWS services are supported:
- (J) Amazon S3
- () Amazon DynamoDB
- () Incorrect options:
- () References:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html
- () https://aws.amazon.com/about-aws/whats-new/2024/03/amazon-dynamodb-aws-privatelink/
- () The engineering team at an e-commerce company wants to set up a custom domain for internal usage such as internaldomainexample.com. The team wants to use the private hosted zones feature of Amazon Route 53 to accomplish this.
- () Which of the following settings of the VPC need to be enabled? (Select two)
- () Correct selection
- () enableDnsSupport
- () enableDnsHostnames
- () enableDnsDomain
- () enableVpcSupport
- () enableVpcHostnames
- () Correct options:
- () A private hosted zone is a container for records for a domain that you host in one or more Amazon virtual private clouds (VPCs). You create a hosted zone for a domain (such as example.com), and then you create records to tell Amazon Route 53 how you want traffic to be routed for that domain within and among your VPCs.
- () For each VPC that you want to associate with the Route 53 hosted zone, change the following VPC settings to true:
- () The options enableVpcSupport, enableVpcHostnames and enableDnsDomain have been added as distractors.
- () Reference:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zone-private-creating.html
- () A digital media firm is scaling its cloud footprint and wants to isolate development, testing, and production workloads using separate AWS accounts. It also wants a centralized approach to managing networking infrastructure such as subnets and gateways, without repeating configurations in every account. Additionally, the solution must enforce security best practices—like mandatory logging and guardrails—when new accounts are created. The firm prefers a low-maintenance, governance-driven setup.
- () Which solution best meets these goals while minimizing operational overhead?
- () Use AWS Service Catalog to define pre-approved VPC templates. Launch one VPC per workload account from the catalog, and enforce networking guardrails using AWS Config conformance packs
- () Use AWS Organizations to create new accounts and a shared networking account with a central VPC. Share the VPC subnets via AWS RAM and rely on service control policies (SCPs) to enforce guardrails manually
- () Use AWS Control Tower to launch accounts. Deploy separate VPCs in each workload account and centralize security inspection by using Gateway Load Balancers to route traffic through a shared security appliance
- **() Use AWS Control Tower to create and govern accounts. Deploy a centralized VPC in a shared networking account and share its subnets across workload accounts using AWS Resource Access Manager (AWS RAM)** [CORRECT]

**Answer:**
Correct Answer: **Use AWS Control Tower to create and govern accounts. Deploy a centralized VPC in a shared networking account and share its subnets across workload accounts using AWS Resource Access Manager (AWS RAM)**

---

## Question 157

**Q:** Which of the following settings of the VPC need to be enabled? (Select two)

**Options:**
- (A) Correct selection
- (B) enableDnsSupport
- (C) enableDnsHostnames
- (D) enableDnsDomain
- (E) enableVpcSupport
- (F) enableVpcHostnames
- (G) Correct options:
- (H) A private hosted zone is a container for records for a domain that you host in one or more Amazon virtual private clouds (VPCs). You create a hosted zone for a domain (such as example.com), and then you create records to tell Amazon Route 53 how you want traffic to be routed for that domain within and among your VPCs.
- (I) For each VPC that you want to associate with the Route 53 hosted zone, change the following VPC settings to true:
- (J) Incorrect options:
- () The options enableVpcSupport, enableVpcHostnames and enableDnsDomain have been added as distractors.
- () Reference:
- () https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zone-private-creating.html
- () A digital media firm is scaling its cloud footprint and wants to isolate development, testing, and production workloads using separate AWS accounts. It also wants a centralized approach to managing networking infrastructure such as subnets and gateways, without repeating configurations in every account. Additionally, the solution must enforce security best practices—like mandatory logging and guardrails—when new accounts are created. The firm prefers a low-maintenance, governance-driven setup.
- () Which solution best meets these goals while minimizing operational overhead?
- () Use AWS Service Catalog to define pre-approved VPC templates. Launch one VPC per workload account from the catalog, and enforce networking guardrails using AWS Config conformance packs
- () Use AWS Organizations to create new accounts and a shared networking account with a central VPC. Share the VPC subnets via AWS RAM and rely on service control policies (SCPs) to enforce guardrails manually
- () Use AWS Control Tower to launch accounts. Deploy separate VPCs in each workload account and centralize security inspection by using Gateway Load Balancers to route traffic through a shared security appliance
- () Use AWS Control Tower to create and govern accounts. Deploy a centralized VPC in a shared networking account and share its subnets across workload accounts using AWS Resource Access Manager (AWS RAM)
- () Correct option:
- () via - https://docs.aws.amazon.com/controltower/latest/userguide/what-is-control-tower.html
- () References:
- () https://docs.aws.amazon.com/controltower/latest/userguide/what-is-control-tower.html
- () https://docs.aws.amazon.com/ram/latest/userguide/getting-started-sharing.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-sharing.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html
- () A startup uses a fleet of Amazon EC2 servers to manage its CRM application. These Amazon EC2 servers are behind Elastic Load Balancing (ELB). Which of the following configurations are NOT allowed for Elastic Load Balancing?
- () Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone B of us-west-1 region
- () Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed across two Availability Zones of us-east-1 region
- **() Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region** [CORRECT]
- () Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone A of us-east-1 region

**Answer:**
Correct Answer: **Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region**

---

## Question 158

**Q:** Which solution best meets these goals while minimizing operational overhead?

**Options:**
- (A) Use AWS Service Catalog to define pre-approved VPC templates. Launch one VPC per workload account from the catalog, and enforce networking guardrails using AWS Config conformance packs
- (B) Use AWS Organizations to create new accounts and a shared networking account with a central VPC. Share the VPC subnets via AWS RAM and rely on service control policies (SCPs) to enforce guardrails manually
- (C) Use AWS Control Tower to launch accounts. Deploy separate VPCs in each workload account and centralize security inspection by using Gateway Load Balancers to route traffic through a shared security appliance
- (D) Use AWS Control Tower to create and govern accounts. Deploy a centralized VPC in a shared networking account and share its subnets across workload accounts using AWS Resource Access Manager (AWS RAM)
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/controltower/latest/userguide/what-is-control-tower.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/controltower/latest/userguide/what-is-control-tower.html
- (J) https://docs.aws.amazon.com/ram/latest/userguide/getting-started-sharing.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-sharing.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html
- () A startup uses a fleet of Amazon EC2 servers to manage its CRM application. These Amazon EC2 servers are behind Elastic Load Balancing (ELB). Which of the following configurations are NOT allowed for Elastic Load Balancing?
- () Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone B of us-west-1 region
- () Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed across two Availability Zones of us-east-1 region
- **() Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region** [CORRECT]
- () Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone A of us-east-1 region
- () Elastic Load Balancer automatically distributes incoming traffic across multiple targets – Amazon EC2 instances, containers, IP addresses, and Lambda functions – in multiple Availability Zones and ensures only healthy targets receive traffic. ELB cannot distribute incoming traffic for targets deployed in different regions. This configuration is NOT allowed for the Elastic Load Balancer and therefore this is the correct option.
- () These three options are valid configurations for the Elastic Load Balancing to distribute traffic (either within an Availability Zone or between two Availability Zones).
- () Reference:
- () https://aws.amazon.com/elasticloadbalancing/
- () An e-commerce application uses a relational database that runs several queries that perform joins on multiple tables. The development team has found that these queries are slow and expensive, therefore these are a good candidate for caching. The application needs to use a caching service that supports multi-threading.

**Answer:**
Correct Answer: **Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region**

---

## Question 159

**Q:** A startup uses a fleet of Amazon EC2 servers to manage its CRM application. These Amazon EC2 servers are behind Elastic Load Balancing (ELB). Which of the following configurations are NOT allowed for Elastic Load Balancing?

**Options:**
- (A) Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone B of us-west-1 region
- (B) Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed across two Availability Zones of us-east-1 region
- **(C) Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region** [CORRECT]
- (D) Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. All the four instances are deployed in Availability Zone A of us-east-1 region
- (E) Correct option:
- (F) Elastic Load Balancer automatically distributes incoming traffic across multiple targets – Amazon EC2 instances, containers, IP addresses, and Lambda functions – in multiple Availability Zones and ensures only healthy targets receive traffic. ELB cannot distribute incoming traffic for targets deployed in different regions. This configuration is NOT allowed for the Elastic Load Balancer and therefore this is the correct option.
- (G) Incorrect options:
- (H) These three options are valid configurations for the Elastic Load Balancing to distribute traffic (either within an Availability Zone or between two Availability Zones).
- (I) Reference:
- (J) https://aws.amazon.com/elasticloadbalancing/
- () An e-commerce application uses a relational database that runs several queries that perform joins on multiple tables. The development team has found that these queries are slow and expensive, therefore these are a good candidate for caching. The application needs to use a caching service that supports multi-threading.

**Answer:**
Correct Answer: **Use the Elastic Load Balancing to distribute traffic for four Amazon EC2 instances. Two of these instances are deployed in Availability Zone A of us-east-1 region and the other two instances are deployed in Availability Zone B of us-west-1 region**

---

## Question 160

**Q:** As a solutions architect, which of the following services would you recommend for the given use case?

**Options:**
- (A) Amazon ElastiCache for Memcached
- (B) Amazon ElastiCache for Redis
- (C) AWS Global Accelerator
- (D) Amazon DynamoDB Accelerator (DAX)
- (E) Correct option:
- (F) Amazon ElastiCache is a web service that makes it easy to deploy, operate, and scale an in-memory data store and cache in the cloud. The service improves the performance of web applications by allowing you to retrieve information from fast, managed, in-memory data stores, instead of relying entirely on slower disk-based databases.
- (G) Memcached is an open-source, distributed, in-memory key-value store that can retrieve data in milliseconds. Caching site information with Memcached can help you improve the performance and scalability of your site while controlling cost.
- (H) Choose Memcached if the following apply to you:
- (I) You need the simplest model possible.
- (J) You need to run large nodes with multiple cores or threads (support for multi-threading).
- () You need the ability to scale out and in, adding and removing nodes as demand on your system increases and decreases.
- () You need to cache objects.
- () via - https://aws.amazon.com/elasticache/redis-vs-memcached/
- () Incorrect options:
- () Redis does not support multi-threading, so this option is not the right fit for the given use case.
- () Amazon DynamoDB Accelerator (DAX) - Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for Amazon DynamoDB. DAX does not support relational databases.
- () AWS Global Accelerator - AWS Global Accelerator is a networking service that helps you improve the availability and performance of the applications that you offer to your global users. This option has been added as a distractor, it has nothing to do with database caching.
- () References:
- () https://aws.amazon.com/caching/aws-caching/
- () https://docs.aws.amazon.com/AmazonElastiCache/latest/mem-ug/elasticache-use-cases.html
- () https://aws.amazon.com/elasticache/redis-vs-memcached/
- () A development team is looking for a solution that saves development time and deployment costs for an application that uses a high-throughput request-response message pattern.
- () Which of the following Amazon SQS queue types is the best fit to meet this requirement?
- () Amazon Simple Queue Service (Amazon SQS) FIFO queues
- **() Amazon Simple Queue Service (Amazon SQS) temporary queues** [CORRECT]
- () Amazon Simple Queue Service (Amazon SQS) dead-letter queues
- () Amazon Simple Queue Service (Amazon SQS) delay queues
- () Temporary queues help you save development time and deployment costs when using common message patterns such as request-response. You can use the Temporary Queue Client to create high-throughput, cost-effective, application-managed temporary queues.
- () The client maps multiple temporary queues—application-managed queues created on demand for a particular process—onto a single Amazon SQS queue automatically. This allows your application to make fewer API calls and have a higher throughput when the traffic to each temporary queue is low. When a temporary queue is no longer in use, the client cleans up the temporary queue automatically, even if some processes that use the client aren't shut down cleanly.
- () The following are the benefits of temporary queues:
- () 1. They serve as lightweight communication channels for specific threads or processes.
- () 2. They can be created and deleted without incurring additional costs.
- () 3. They are API-compatible with static (normal) Amazon SQS queues. This means that existing code that sends and receives messages can send messages to and receive messages from virtual queues.
- () End-to-end process for sending messages through virtual queues:
- () via - https://aws.amazon.com/blogs/compute/simple-two-way-messaging-using-the-amazon-sqs-temporary-queue-client/
- () Amazon Simple Queue Service (Amazon SQS) FIFO queues - Amazon SQS FIFO (First-In-First-Out) queues are designed to enhance messaging between applications when the order of operations and events is critical, or where duplicates can't be tolerated. FIFO queues also provide exactly-once processing but have a limited number of transactions per second (TPS).
- () Amazon Simple Queue Service (Amazon SQS) delay queues - Delay queues let you postpone the delivery of new messages to a queue for a number of seconds, for example, when your consumer application needs additional time to process messages. If you create a delay queue, any messages that you send to the queue remain invisible to consumers for the duration of the delay period. The default (minimum) delay for a queue is 0 seconds. The maximum is 15 minutes.
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-temporary-queues.html
- () https://aws.amazon.com/blogs/compute/simple-two-way-messaging-using-the-amazon-sqs-temporary-queue-client/

**Answer:**
Correct Answer: **Amazon Simple Queue Service (Amazon SQS) temporary queues**

---

## Question 161

**Q:** Which of the following Amazon SQS queue types is the best fit to meet this requirement?

**Options:**
- (A) Amazon Simple Queue Service (Amazon SQS) FIFO queues
- **(B) Amazon Simple Queue Service (Amazon SQS) temporary queues** [CORRECT]
- (C) Amazon Simple Queue Service (Amazon SQS) dead-letter queues
- (D) Amazon Simple Queue Service (Amazon SQS) delay queues
- (E) Correct option:
- (F) Temporary queues help you save development time and deployment costs when using common message patterns such as request-response. You can use the Temporary Queue Client to create high-throughput, cost-effective, application-managed temporary queues.
- (G) The client maps multiple temporary queues—application-managed queues created on demand for a particular process—onto a single Amazon SQS queue automatically. This allows your application to make fewer API calls and have a higher throughput when the traffic to each temporary queue is low. When a temporary queue is no longer in use, the client cleans up the temporary queue automatically, even if some processes that use the client aren't shut down cleanly.
- (H) The following are the benefits of temporary queues:
- (I) 1. They serve as lightweight communication channels for specific threads or processes.
- (J) 2. They can be created and deleted without incurring additional costs.
- () 3. They are API-compatible with static (normal) Amazon SQS queues. This means that existing code that sends and receives messages can send messages to and receive messages from virtual queues.
- () End-to-end process for sending messages through virtual queues:
- () via - https://aws.amazon.com/blogs/compute/simple-two-way-messaging-using-the-amazon-sqs-temporary-queue-client/
- () Incorrect options:
- () Amazon Simple Queue Service (Amazon SQS) FIFO queues - Amazon SQS FIFO (First-In-First-Out) queues are designed to enhance messaging between applications when the order of operations and events is critical, or where duplicates can't be tolerated. FIFO queues also provide exactly-once processing but have a limited number of transactions per second (TPS).
- () Amazon Simple Queue Service (Amazon SQS) delay queues - Delay queues let you postpone the delivery of new messages to a queue for a number of seconds, for example, when your consumer application needs additional time to process messages. If you create a delay queue, any messages that you send to the queue remain invisible to consumers for the duration of the delay period. The default (minimum) delay for a queue is 0 seconds. The maximum is 15 minutes.
- () References:
- () https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-temporary-queues.html
- () https://aws.amazon.com/blogs/compute/simple-two-way-messaging-using-the-amazon-sqs-temporary-queue-client/
- () An IT company is using Amazon Simple Queue Service (Amazon SQS) queues for decoupling the various components of application architecture. As the consuming components need additional time to process Amazon Simple Queue Service (Amazon SQS) messages, the company wants to postpone the delivery of new messages to the queue for a few seconds.

**Answer:**
Correct Answer: **Amazon Simple Queue Service (Amazon SQS) temporary queues**

---

## Question 162

**Q:** How can you provide these users access in the least possible time, with minimal changes?

**Options:**
- (A) Update the Amazon S3 bucket policy
- (B) Create a group, attach the policy to the group and place the users in the group
- (C) Create a policy and assign it manually to the 50 users
- (D) Create an AWS Multi-Factor Authentication (AWS MFA) user with read / write access and link 50 IAM with AWS MFA
- (E) Correct option:
- (F) Here creating a group, assigning users to that group and attaching policies to that group is the best way.
- (G) Incorrect options:
- (H) Update the Amazon S3 bucket policy - Updating the Amazon S3 bucket policy could work but would not scale, as the size of the S3 bucket policy is limited (Bucket policies are limited to 20 KB in size).
- (I) A policy is an object in AWS that, when associated with an identity or resource, defines their permissions. AWS evaluates these policies when an IAM principal (user or role) makes a request. Permissions in the policies determine whether the request is allowed or denied.
- (J) Identity-based policies – Attach managed and inline policies to IAM identities (users, groups to which users belong, or roles). Identity-based policies grant permissions to an identity.
- () Resource-based policies – Attach inline policies to resources. The most common examples of resource-based policies are Amazon S3 bucket policies and IAM role trust policies. Resource-based policies grant permissions to the principal that is specified in the policy. Principals can be in the same account as the resource or in other accounts.
- () Creating a policy and assigning it manually to users would work but would be hard to scale and manage.
- () Create an AWS Multi-Factor Authentication (AWS MFA) user with read / write access and link 50 IAM with AWS MFA - AWS MFA adds extra security because it requires users to provide unique authentication from an AWS supported MFA mechanism in addition to their regular sign-in credentials when they access AWS websites or services. AWS MFA cannot help in terms of granting read/write access to only 50 of the IAM users.
- () References:
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html
- () The data engineering team at a company wants to analyze Amazon S3 storage access patterns to decide when to transition the right data to the right storage class.
- () Which of the following represents a correct option regarding the capabilities of Amazon S3 Analytics storage class analysis?
- () Storage class analysis only provides recommendations for Standard to Standard One-Zone IA classes
- () Storage class analysis only provides recommendations for Standard to Glacier Flexible Retrieval classes
- **() Storage class analysis only provides recommendations for Standard to Standard IA classes** [CORRECT]
- () Storage class analysis only provides recommendations for Standard to Glacier Deep Archive classes
- () By using Amazon S3 analytics Storage Class Analysis you can analyze storage access patterns to help you decide when to transition the right data to the right storage class. This new Amazon S3 analytics feature observes data access patterns to help you determine when to transition less frequently accessed STANDARD storage to the STANDARD_IA (IA, for infrequent access) storage class.
- () Storage class analysis only provides recommendations for Standard to Standard IA classes.
- () After storage class analysis observes the infrequent access patterns of a filtered set of data over a period of time, you can use the analysis results to help you improve your lifecycle configurations. You can configure storage class analysis to analyze all the objects in a bucket. Or, you can configure filters to group objects together for analysis by common prefix (that is, objects that have names that begin with a common string), by object tags, or by both prefix and tags.
- () These three options contradict the explanation provided above, so these options are incorrect.
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/analytics-storage-class.html
- () A social media application lets users upload photos and perform image editing operations. The application offers two classes of service: pro and lite. The product team wants the photos submitted by pro users to be processed before those submitted by lite users. Photos are uploaded to Amazon S3 and the job information is sent to Amazon SQS.

**Answer:**
Correct Answer: **Storage class analysis only provides recommendations for Standard to Standard IA classes**

---

## Question 163

**Q:** Which of the following represents a correct option regarding the capabilities of Amazon S3 Analytics storage class analysis?

**Options:**
- (A) Storage class analysis only provides recommendations for Standard to Standard One-Zone IA classes
- (B) Storage class analysis only provides recommendations for Standard to Glacier Flexible Retrieval classes
- **(C) Storage class analysis only provides recommendations for Standard to Standard IA classes** [CORRECT]
- (D) Storage class analysis only provides recommendations for Standard to Glacier Deep Archive classes
- (E) Correct option:
- (F) By using Amazon S3 analytics Storage Class Analysis you can analyze storage access patterns to help you decide when to transition the right data to the right storage class. This new Amazon S3 analytics feature observes data access patterns to help you determine when to transition less frequently accessed STANDARD storage to the STANDARD_IA (IA, for infrequent access) storage class.
- (G) Storage class analysis only provides recommendations for Standard to Standard IA classes.
- (H) After storage class analysis observes the infrequent access patterns of a filtered set of data over a period of time, you can use the analysis results to help you improve your lifecycle configurations. You can configure storage class analysis to analyze all the objects in a bucket. Or, you can configure filters to group objects together for analysis by common prefix (that is, objects that have names that begin with a common string), by object tags, or by both prefix and tags.
- (I) Incorrect options:
- (J) These three options contradict the explanation provided above, so these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/analytics-storage-class.html
- () A social media application lets users upload photos and perform image editing operations. The application offers two classes of service: pro and lite. The product team wants the photos submitted by pro users to be processed before those submitted by lite users. Photos are uploaded to Amazon S3 and the job information is sent to Amazon SQS.

**Answer:**
Correct Answer: **Storage class analysis only provides recommendations for Standard to Standard IA classes**

---

## Question 164

**Q:** Which combination of steps will enable secure S3 integration for this workload? (Select two)

**Options:**
- (A) Correct selection
- (B) Create an Amazon Cognito identity pool to allow federated identities. Use it to generate temporary AWS credentials that grant S3 access when users successfully authenticate
- (C) Use the existing Amazon Cognito user pool to directly grant users permission to upload and download objects in the S3 bucket
- (D) Create an Amazon S3 VPC endpoint in the VPC where the application is hosted to enable private connectivity between the application and S3
- (E) Configure an AWS Lambda function that proxies user uploads to S3. Invoke the Lambda function after each user login to isolate the S3 access
- (F) Attach an S3 bucket policy that allows access only if requests include a custom HTTP header containing a valid Cognito user ID
- (G) Correct options:
- (H) via - https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html
- (I) Incorrect options:
- (J) Use the existing Amazon Cognito user pool to directly grant users permission to upload and download objects in the S3 bucket - Amazon Cognito user pools provide authentication, not authorization for AWS resources like S3. You cannot directly assign S3 permissions using user pools alone. You must integrate the user pool with an identity pool, which generates temporary AWS credentials mapped to IAM roles with S3 access. This option omits a critical step and would not allow secure access to S3.
- () References:
- () https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/amazon-s3-policy-keys.html
- () https://docs.aws.amazon.com/service-authorization/latest/reference/list_amazons3.html#amazons3-policy-keys
- () https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-s3.html
- () As a Solutions Architect, you would like to completely secure the communications between your Amazon CloudFront distribution and your Amazon S3 bucket which contains the static files for your website. Users should only be able to access the Amazon S3 bucket through Amazon CloudFront and not directly.
- () What do you recommend?
- () Create a bucket policy to only authorize the IAM role attached to the Amazon CloudFront distribution
- **() Create an origin access identity (OAI) and update the Amazon S3 Bucket Policy** [CORRECT]
- () Make the Amazon S3 bucket public
- () Update the Amazon S3 bucket security groups to only allow traffic from the Amazon CloudFront security group
- () Correct option:
- () To restrict access to content that you serve from Amazon S3 buckets, you need to follow the following steps:
- () 1. Create a special Amazon CloudFront user called an origin access identity (OAI) and associate it with your distribution.
- () 2. Configure your Amazon S3 bucket permissions so that Amazon CloudFront can use the OAI to access the files in your bucket and serve them to your users. Make sure that users can’t use a direct URL to the Amazon S3 bucket to access a file there.
- () After you take these steps, users can only access your files through Amazon CloudFront, not directly from the Amazon S3 bucket.
- () Update the Amazon S3 bucket security groups to only allow traffic from the Amazon CloudFront security group - Amazon S3 buckets don't have security groups, hence this is an incorrect option.
- () Make the Amazon S3 bucket public - If the Amazon S3 bucket is made public, it can be accessed by anyone directly. This is not the requirement.
- () Create a bucket policy to only authorize the IAM role attached to the Amazon CloudFront distribution - You cannot attach IAM roles to the Amazon CloudFront distribution. Here you need to use an OAI.
- () Reference:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- () The engineering team at a startup is evaluating the most optimal block storage volume type for the Amazon EC2 instances hosting its flagship application. The storage volume should support very low latency but it does not need to persist the data when the instance terminates. As a solutions architect, you have proposed using Instance Store volumes to meet these requirements.
- () Which of the following would you identify as the key characteristics of the Instance Store volumes? (Select two)
- () You can specify instance store volumes for an instance when you launch or restart it
- () Instance store is reset when you stop or terminate an instance. Instance store data is preserved during hibernation

**Answer:**
Correct Answer: **Create an origin access identity (OAI) and update the Amazon S3 Bucket Policy**

---

## Question 165

**Q:** Which of the following would you identify as the key characteristics of the Instance Store volumes? (Select two)

**Options:**
- (A) You can specify instance store volumes for an instance when you launch or restart it
- (B) Instance store is reset when you stop or terminate an instance. Instance store data is preserved during hibernation
- (C) Correct selection
- (D) You can't detach an instance store volume from one instance and attach it to a different instance
- (E) If you create an Amazon Machine Image (AMI) from an instance, the data on its instance store volumes isn't preserved
- (F) An instance store is a network storage type
- (G) Correct options:
- (H) You can specify instance store volumes for an instance only when you launch it. You can't detach an instance store volume from one instance and attach it to a different instance. The data in an instance store persists only during the lifetime of its associated instance. If an instance reboots (intentionally or unintentionally), data in the instance store persists.
- (I) If you create an AMI from an instance, the data on its instance store volumes isn't preserved and isn't present on the instance store volumes of the instances that you launch from the AMI.
- (J) Incorrect options:
- () Instance store is reset when you stop or terminate an instance. Instance store data is preserved during hibernation - When you stop, hibernate, or terminate an instance, every block of storage in the instance store is reset. Therefore, this option is incorrect.
- () You can specify instance store volumes for an instance when you launch or restart it - You can specify instance store volumes for an instance only when you launch it.
- () An instance store is a network storage type - An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- () Which solution will help improve the application’s responsiveness and scalability during peak load periods?
- **() Use an EC2 Auto Scaling group with a target tracking policy to automatically scale the processing tier. Configure the policy to monitor the ApproximateNumberOfMessages in the SQS queue** [CORRECT]
- () Use scheduled Auto Scaling for the processing tier based on past peak periods. Use average CPU utilization to define scaling thresholds
- () Add Amazon Kinesis Data Streams to buffer order events from the web tier. Configure the processing tier to consume records from the stream and use enhanced fan-out for high throughput
- () Use Amazon EventBridge to schedule batch processing jobs for the queue. Configure the event rule to invoke EC2-based workers every 10 minutes to process messages in the SQS queue
- () Correct option:
- () Use scheduled Auto Scaling for the processing tier based on past peak periods. Use average CPU utilization to define scaling thresholds - Scheduled scaling assumes that peak times are predictable, but the scenario explicitly states they are variable and unpredictable. While CPU utilization is a valid metric, it lags behind and only reflects stress once it occurs, not proactively. Also, scheduled scaling doesn’t adapt in real-time, making it ineffective for responding to dynamic queue growth.
- () References:
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-scheduled-scaling.html
- () https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-what-is.html
- () https://docs.aws.amazon.com/streams/latest/dev/introduction.html
- () The engineering team at a social media company has noticed that while some of the images stored in Amazon S3 are frequently accessed, others sit idle for a considerable span of time.

**Answer:**
Correct Answer: **Use an EC2 Auto Scaling group with a target tracking policy to automatically scale the processing tier. Configure the policy to monitor the ApproximateNumberOfMessages in the SQS queue**

---

## Question 166

**Q:** Which solution will help improve the application’s responsiveness and scalability during peak load periods?

**Options:**
- **(A) Use an EC2 Auto Scaling group with a target tracking policy to automatically scale the processing tier. Configure the policy to monitor the ApproximateNumberOfMessages in the SQS queue** [CORRECT]
- (B) Use scheduled Auto Scaling for the processing tier based on past peak periods. Use average CPU utilization to define scaling thresholds
- (C) Add Amazon Kinesis Data Streams to buffer order events from the web tier. Configure the processing tier to consume records from the stream and use enhanced fan-out for high throughput
- (D) Use Amazon EventBridge to schedule batch processing jobs for the queue. Configure the event rule to invoke EC2-based workers every 10 minutes to process messages in the SQS queue
- (E) Correct option:
- (F) Incorrect options:
- (G) Use scheduled Auto Scaling for the processing tier based on past peak periods. Use average CPU utilization to define scaling thresholds - Scheduled scaling assumes that peak times are predictable, but the scenario explicitly states they are variable and unpredictable. While CPU utilization is a valid metric, it lags behind and only reflects stress once it occurs, not proactively. Also, scheduled scaling doesn’t adapt in real-time, making it ineffective for responding to dynamic queue growth.
- (H) References:
- (I) https://docs.aws.amazon.com/autoscaling/ec2/userguide/as-using-sqs-queue.html
- (J) https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-scheduled-scaling.html
- () https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-what-is.html
- () https://docs.aws.amazon.com/streams/latest/dev/introduction.html
- () The engineering team at a social media company has noticed that while some of the images stored in Amazon S3 are frequently accessed, others sit idle for a considerable span of time.

**Answer:**
Correct Answer: **Use an EC2 Auto Scaling group with a target tracking policy to automatically scale the processing tier. Configure the policy to monitor the ApproximateNumberOfMessages in the SQS queue**

---

## Question 167

**Q:** As a solutions architect, what is your recommendation to build the MOST cost-effective solution?

**Options:**
- (A) Store the images using the Amazon S3 Standard-IA storage class
- (B) Create a data monitoring application on an Amazon EC2 instance in the same region as the bucket storing the images. The application is triggered daily via Amazon CloudWatch and it changes the storage class of infrequently accessed objects to Amazon S3 Standard-IA and the frequently accessed objects are migrated to Amazon S3 Standard class
- (C) Create a data monitoring application on an Amazon EC2 instance in the same region as the bucket storing the images. The application is triggered daily via Amazon CloudWatch and it changes the storage class of infrequently accessed objects to Amazon S3 One Zone-IA and the frequently accessed objects are migrated to Amazon S3 Standard class
- **(D) Store the images using the Amazon S3 Intelligent-Tiering storage class** [CORRECT]
- (E) Correct option:
- (F) The Amazon S3 Intelligent-Tiering storage class is designed to optimize costs by automatically moving data to the most cost-effective access tier, without performance impact or operational overhead. It works by storing objects in two access tiers: one tier that is optimized for frequent access and another lower-cost tier that is optimized for infrequent access.
- (G) For a small monthly monitoring and automation fee per object, Amazon S3 monitors access patterns of the objects in S3 Intelligent-Tiering and moves the ones that have not been accessed for 30 consecutive days to the infrequent access tier. If an object in the infrequent access tier is accessed, it is automatically moved back to the frequent access tier. Therefore using the Amazon S3 Intelligent-Tiering storage class is the correct solution for the given problem statement.
- (H) Amazon S3 Storage Classes Overview:
- (I) Incorrect options:
- (J) Creating a data monitoring application on an Amazon EC2 instance for managing the desired Amazon S3 storage class entails significant development cost as well as infrastructure maintenance effort. The Amazon S3 Intelligent-Tiering storage class does the job in a cost-effective way. Therefore both these options are incorrect.
- () Reference:
- () https://aws.amazon.com/s3/storage-classes/
- () An e-commerce company uses Amazon RDS MySQL DB to store the data. The analytics department at the company runs its reports on the same database. The engineering team has noticed sluggish performance on the database when the analytics reporting process is in progress.

**Answer:**
Correct Answer: **Store the images using the Amazon S3 Intelligent-Tiering storage class**

---

## Question 168

**Q:** As an AWS Certified Solutions Architect - Associate, which of the following would you suggest as the MOST cost-optimal solution to improve the performance?

**Options:**
- (A) Create a read-replica with the same compute capacity and the same storage capacity as the primary. Point the reporting queries to run against the read replica
- (B) Create a standby instance in a multi-AZ configuration with the same compute capacity and the same storage capacity as the primary. Point the reporting queries to run against the standby instance
- (C) Create a standby instance in a multi-AZ configuration with half compute capacity and half storage capacity as the primary. Point the reporting queries to run against the standby instance
- (D) Create a read-replica with half compute capacity and half storage capacity as the primary. Point the reporting queries to run against the read replica
- (E) Correct option:
- (F) Amazon RDS Read Replicas:
- (G) via - https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
- (H) You can use read replicas to improve the performance of your Amazon RDS MySQL DB by handling business reporting or data warehousing scenarios where you might want business reporting queries to run against your read replica, rather than your production database instance.
- (I) You can create up to five read replicas from one DB instance. For replication to operate effectively, each read replica should have the same amount of compute and storage resources as the source database instance. If you scale the source database instance, also scale the read replicas.
- (J) via - https://docs.amazonaws.cn/en_us/AmazonRDS/latest/UserGuide/USER_MySQL.Replication.ReadReplicas.html
- () Incorrect options:
- () Create a read-replica with half compute capacity and half storage capacity as the primary. Point the reporting queries to run against the read replica - As mentioned in the explanation above, you should create a read-replica with the same compute capacity and the same storage capacity as the primary.
- () Multi-AZ deployments are not a read scaling solution, so you cannot use a standby to serve read traffic. The standby is there just for failover. Hence both these options are incorrect.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ReadRepl.html
- () https://docs.amazonaws.cn/en_us/AmazonRDS/latest/UserGuide/USER_MySQL.Replication.ReadReplicas.html
- () A company has many Amazon Virtual Private Cloud (Amazon VPC) in various accounts, that need to be connected in a star network with one another and connected with on-premises networks through AWS Direct Connect.
- () What do you recommend?
- () Virtual private gateway (VGW)
- () AWS PrivateLink
- () VPC Peering Connection
- **() AWS Transit Gateway** [CORRECT]
- () Without AWS Transit Gateway
- () via - https://aws.amazon.com/transit-gateway/
- () With AWS Transit Gateway
- () VPC Peering Connection - A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your VPCs, or with a VPC in another AWS account. The VPCs can be in different regions (also known as an inter-region VPC peering connection).
- () VPC Peering helps connect two VPCs and is not transitive. It would require to create many peering connections between all the VPCs to have them connect. This alone wouldn't work, because we would need to also connect the on-premises data center through Direct Connect and Direct Connect Gateway, but that's not mentioned in this answer.
- () Virtual private gateway (VGW) - A virtual private gateway (VGW), also known as a VPN Gateway, is the endpoint on the VPC side of your VPN connection. You can create a virtual private gateway before creating the VPC itself. VPN Gateway is a distractor here because we haven't mentioned a VPN.
- () https://aws.amazon.com/transit-gateway/
- () https://docs.aws.amazon.com/vpc/latest/peering/what-is-vpc-peering.html

**Answer:**
Correct Answer: **AWS Transit Gateway**

---

## Question 169

**Q:** As a solutions architect, which of the following AWS services would you recommend as the MOST cost-optimal solution?

**Options:**
- (A) Amazon S3 Standard-IA
- (B) Amazon EFS Infrequent Access
- (C) Amazon S3 Standard
- (D) Amazon EFS Standard
- (E) Correct option:
- (F) How Amazon EFS Infrequent Access Works:
- (G) via - https://aws.amazon.com/efs/features/infrequent-access/
- (H) Incorrect options:
- (I) Amazon EFS Standard - Amazon EFS Infrequent Access is more cost-effective than EFS Standard for the given use-case, therefore this option is incorrect.
- (J) Both these options are object-based storage, whereas the given use-case requires a POSIX compliant file storage solution. Hence these two options are incorrect.
- () Reference:
- () https://aws.amazon.com/efs/features/infrequent-access/
- () Which solution will most effectively address the performance issues with the least operational overhead?
- () Create multiple S3 buckets in different Regions and replicate image data based on user location. Configure CloudFront to upload and download from the nearest bucket
- () Migrate the website from S3 to Amazon EC2 instances in multiple Regions. Use an Application Load Balancer with AWS Global Accelerator to distribute global traffic and reduce latency
- () Deploy an Amazon CloudFront distribution with the S3 bucket as the origin to improve download speeds. Enable S3 Transfer Acceleration to reduce upload latency for global users
- () Enable AWS Global Accelerator on the S3 bucket to accelerate both uploads and downloads. Reconfigure the website to route requests through the accelerator
- () References:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/about-endpoints.html
- () A financial services firm operates a mission-critical transaction processing platform hosted in the AWS us-east-2 Region. The backend is powered by a MySQL-compatible Amazon Aurora cluster, with high transaction volumes throughout the day. As part of its business continuity planning, the firm has selected us-west-2 as its designated disaster recovery (DR) Region.
- () The firm has defined strict DR objectives:
- () Recovery Point Objective (RPO): ≤ 5 minutes
- () Recovery Time Objective (RTO): ≤ 15 minutes
- () Leadership has asked for a DR solution that ensures fast cross-regional failover with minimal operational overhead and configuration effort. What do you recommend?
- () Create an Aurora read replica in us-west-2 with equivalent capacity to the primary cluster's writer node in us-east-2. Monitor replication health and configure a manual promotion process for failover
- () Provision a separate Aurora MySQL-compatible cluster in us-west-2, and configure AWS Database Migration Service (AWS DMS) to replicate data from the primary database to the DR cluster continuously. Perform manual failover during DR events
- **() Convert the Aurora cluster to an Aurora global database, with the secondary cluster deployed in us-west-2. Rely on Aurora global database managed failover to meet RTO and RPO objectives** [CORRECT]
- () Deploy a separate Aurora cluster in us-west-2, and use scheduled AWS Lambda functions with custom scripts to export and import snapshots from us-east-2 every 5 minutes

**Answer:**
Correct Answer: **Convert the Aurora cluster to an Aurora global database, with the secondary cluster deployed in us-west-2. Rely on Aurora global database managed failover to meet RTO and RPO objectives**

---

## Question 170

**Q:** Which solution will most effectively address the performance issues with the least operational overhead?

**Options:**
- (A) Create multiple S3 buckets in different Regions and replicate image data based on user location. Configure CloudFront to upload and download from the nearest bucket
- (B) Migrate the website from S3 to Amazon EC2 instances in multiple Regions. Use an Application Load Balancer with AWS Global Accelerator to distribute global traffic and reduce latency
- (C) Deploy an Amazon CloudFront distribution with the S3 bucket as the origin to improve download speeds. Enable S3 Transfer Acceleration to reduce upload latency for global users
- (D) Enable AWS Global Accelerator on the S3 bucket to accelerate both uploads and downloads. Reconfigure the website to route requests through the accelerator
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/DownloadDistS3AndCustomOrigins.html
- (I) https://docs.aws.amazon.com/AmazonS3/latest/userguide/transfer-acceleration.html
- (J) https://docs.aws.amazon.com/global-accelerator/latest/dg/about-endpoints.html
- () A financial services firm operates a mission-critical transaction processing platform hosted in the AWS us-east-2 Region. The backend is powered by a MySQL-compatible Amazon Aurora cluster, with high transaction volumes throughout the day. As part of its business continuity planning, the firm has selected us-west-2 as its designated disaster recovery (DR) Region.
- () The firm has defined strict DR objectives:
- () Recovery Point Objective (RPO): ≤ 5 minutes
- () Recovery Time Objective (RTO): ≤ 15 minutes
- () Leadership has asked for a DR solution that ensures fast cross-regional failover with minimal operational overhead and configuration effort. What do you recommend?
- () Create an Aurora read replica in us-west-2 with equivalent capacity to the primary cluster's writer node in us-east-2. Monitor replication health and configure a manual promotion process for failover
- () Provision a separate Aurora MySQL-compatible cluster in us-west-2, and configure AWS Database Migration Service (AWS DMS) to replicate data from the primary database to the DR cluster continuously. Perform manual failover during DR events
- () Convert the Aurora cluster to an Aurora global database, with the secondary cluster deployed in us-west-2. Rely on Aurora global database managed failover to meet RTO and RPO objectives
- () Deploy a separate Aurora cluster in us-west-2, and use scheduled AWS Lambda functions with custom scripts to export and import snapshots from us-east-2 every 5 minutes
- () via - https://aws.amazon.com/blogs/storage/protecting-data-with-amazon-s3-object-lock/
- () Create an Aurora read replica in us-west-2 with equivalent capacity to the primary cluster's writer node in us-east-2. Monitor replication health and configure a manual promotion process for failover - Aurora cross-Region read replicas do not offer managed failover and require manual intervention and additional orchestration during a disaster. Although replication latency is low, managing failover manually adds operational burden and increases risk of human error, affecting RTO.
- () Deploy a separate Aurora cluster in us-west-2, and use scheduled AWS Lambda functions with custom scripts to export and import snapshots from us-east-2 every 5 minutes - Snapshot export/import is not near real-time, and even with scripting, this method cannot guarantee a 5-minute RPO. Snapshot-based DR also requires manual failover orchestration, violating both the RPO and RTO requirements.
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
- () https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/implement-cross-region-disaster-recovery-with-aws-dms-and-amazon-aurora.html
- () https://docs.aws.amazon.com/dms/latest/userguide/Welcome.html
- () A tech enterprise operates several workloads using Amazon EC2, AWS Fargate, and AWS Lambda across various teams. To optimize compute costs, the company has purchased Compute Savings Plans. The cloud operations team needs to implement a solution that not only monitors utilization but also sends automated alerts when coverage levels of the Compute Savings Plans fall below a defined threshold.
- () What is the MOST operationally efficient way to achieve this?
- () Enable Compute Optimizer recommendations for EC2 and Fargate. Configure automatic notifications for cost optimization opportunities and Savings Plans coverage drops
- () Create a standalone dashboard in Amazon CloudWatch to track EC2 and Fargate usage. Use metric math to estimate coverage and trigger alarms
- () Configure a custom script that queries the Savings Plans utilization API and pushes results to an Amazon S3 bucket. Use Amazon QuickSight to visualize coverage and email reports weekly
- **() Use AWS Budgets to create a daily coverage budget specifically for Compute Savings Plans. Define a coverage threshold and configure notifications to alert relevant stakeholders** [CORRECT]

**Answer:**
Correct Answer: **Use AWS Budgets to create a daily coverage budget specifically for Compute Savings Plans. Define a coverage threshold and configure notifications to alert relevant stakeholders**

---

## Question 171

**Q:** Leadership has asked for a DR solution that ensures fast cross-regional failover with minimal operational overhead and configuration effort. What do you recommend?

**Options:**
- (A) Create an Aurora read replica in us-west-2 with equivalent capacity to the primary cluster's writer node in us-east-2. Monitor replication health and configure a manual promotion process for failover
- (B) Provision a separate Aurora MySQL-compatible cluster in us-west-2, and configure AWS Database Migration Service (AWS DMS) to replicate data from the primary database to the DR cluster continuously. Perform manual failover during DR events
- (C) Convert the Aurora cluster to an Aurora global database, with the secondary cluster deployed in us-west-2. Rely on Aurora global database managed failover to meet RTO and RPO objectives
- (D) Deploy a separate Aurora cluster in us-west-2, and use scheduled AWS Lambda functions with custom scripts to export and import snapshots from us-east-2 every 5 minutes
- (E) Correct option:
- (F) via - https://aws.amazon.com/blogs/storage/protecting-data-with-amazon-s3-object-lock/
- (G) Incorrect options:
- (H) Create an Aurora read replica in us-west-2 with equivalent capacity to the primary cluster's writer node in us-east-2. Monitor replication health and configure a manual promotion process for failover - Aurora cross-Region read replicas do not offer managed failover and require manual intervention and additional orchestration during a disaster. Although replication latency is low, managing failover manually adds operational burden and increases risk of human error, affecting RTO.
- (I) Deploy a separate Aurora cluster in us-west-2, and use scheduled AWS Lambda functions with custom scripts to export and import snapshots from us-east-2 every 5 minutes - Snapshot export/import is not near real-time, and even with scripting, this method cannot guarantee a 5-minute RPO. Snapshot-based DR also requires manual failover orchestration, violating both the RPO and RTO requirements.
- (J) References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html
- () https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/implement-cross-region-disaster-recovery-with-aws-dms-and-amazon-aurora.html
- () https://docs.aws.amazon.com/dms/latest/userguide/Welcome.html
- () A tech enterprise operates several workloads using Amazon EC2, AWS Fargate, and AWS Lambda across various teams. To optimize compute costs, the company has purchased Compute Savings Plans. The cloud operations team needs to implement a solution that not only monitors utilization but also sends automated alerts when coverage levels of the Compute Savings Plans fall below a defined threshold.
- () What is the MOST operationally efficient way to achieve this?
- () Enable Compute Optimizer recommendations for EC2 and Fargate. Configure automatic notifications for cost optimization opportunities and Savings Plans coverage drops
- () Create a standalone dashboard in Amazon CloudWatch to track EC2 and Fargate usage. Use metric math to estimate coverage and trigger alarms
- () Configure a custom script that queries the Savings Plans utilization API and pushes results to an Amazon S3 bucket. Use Amazon QuickSight to visualize coverage and email reports weekly
- **() Use AWS Budgets to create a daily coverage budget specifically for Compute Savings Plans. Define a coverage threshold and configure notifications to alert relevant stakeholders** [CORRECT]
- () via - https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html
- () Enable Compute Optimizer recommendations for EC2 and Fargate. Configure automatic notifications for cost optimization opportunities and Savings Plans coverage drops - AWS Compute Optimizer offers instance type recommendations based on performance metrics but does not track or notify on Savings Plans coverage. It helps right-size workloads but does not integrate with Savings Plans metrics or budgets. Therefore, it cannot fulfill the requirement of alerting on under-coverage.
- () Create a standalone dashboard in Amazon CloudWatch to track EC2 and Fargate usage. Use metric math to estimate coverage and trigger alarms - Although Amazon CloudWatch is powerful for metrics and alarms, Savings Plans coverage metrics are not directly available in CloudWatch. You would need to implement a complex estimation process using usage metrics, which is both error-prone and operationally inefficient. AWS Budgets is purpose-built for this use case and is much simpler to implement.
- () Reference:
- () https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html
- () You are deploying a critical monolith application that must be deployed on a single web server, as it hasn't been created to work in distributed mode. Still, you want to make sure your setup can automatically recover from the failure of an Availability Zone (AZ).
- () Which of the following options should be combined to form the MOST cost-efficient solution? (Select three)
- () Correct selection
- () Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=1, desired=1
- () Create a Spot Fleet request
- () Assign an Amazon EC2 Instance Role to perform the necessary API calls
- () Create an elastic IP address (EIP) and use the Amazon EC2 user-data script to attach it
- () Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=2, desired=2
- () Create an Application Load Balancer and a target group with the instance(s) of the Auto Scaling Group
- () Correct options:

**Answer:**
Correct Answer: **Use AWS Budgets to create a daily coverage budget specifically for Compute Savings Plans. Define a coverage threshold and configure notifications to alert relevant stakeholders**

---

## Question 172

**Q:** What is the MOST operationally efficient way to achieve this?

**Options:**
- (A) Enable Compute Optimizer recommendations for EC2 and Fargate. Configure automatic notifications for cost optimization opportunities and Savings Plans coverage drops
- (B) Create a standalone dashboard in Amazon CloudWatch to track EC2 and Fargate usage. Use metric math to estimate coverage and trigger alarms
- (C) Configure a custom script that queries the Savings Plans utilization API and pushes results to an Amazon S3 bucket. Use Amazon QuickSight to visualize coverage and email reports weekly
- **(D) Use AWS Budgets to create a daily coverage budget specifically for Compute Savings Plans. Define a coverage threshold and configure notifications to alert relevant stakeholders** [CORRECT]
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html
- (G) Incorrect options:
- (H) Enable Compute Optimizer recommendations for EC2 and Fargate. Configure automatic notifications for cost optimization opportunities and Savings Plans coverage drops - AWS Compute Optimizer offers instance type recommendations based on performance metrics but does not track or notify on Savings Plans coverage. It helps right-size workloads but does not integrate with Savings Plans metrics or budgets. Therefore, it cannot fulfill the requirement of alerting on under-coverage.
- (I) Create a standalone dashboard in Amazon CloudWatch to track EC2 and Fargate usage. Use metric math to estimate coverage and trigger alarms - Although Amazon CloudWatch is powerful for metrics and alarms, Savings Plans coverage metrics are not directly available in CloudWatch. You would need to implement a complex estimation process using usage metrics, which is both error-prone and operationally inefficient. AWS Budgets is purpose-built for this use case and is much simpler to implement.
- (J) Reference:
- () https://docs.aws.amazon.com/cost-management/latest/userguide/budgets-managing-costs.html
- () You are deploying a critical monolith application that must be deployed on a single web server, as it hasn't been created to work in distributed mode. Still, you want to make sure your setup can automatically recover from the failure of an Availability Zone (AZ).
- () Which of the following options should be combined to form the MOST cost-efficient solution? (Select three)
- () Correct selection
- () Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=1, desired=1
- () Create a Spot Fleet request
- () Assign an Amazon EC2 Instance Role to perform the necessary API calls
- () Create an elastic IP address (EIP) and use the Amazon EC2 user-data script to attach it
- () Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=2, desired=2
- () Create an Application Load Balancer and a target group with the instance(s) of the Auto Scaling Group
- () Correct options:
- () Amazon EC2 Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. You create collections of EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes below this size.
- () So we have an Auto Scaling Group with desired=1, across two AZ, so that if an instance goes down, it is automatically recreated in another AZ. So this option is correct.
- () Application Load Balancer (ALB) operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- () An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is associated with your AWS account. With an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account.
- () Now, between the ALB and the Elastic IP. If we use an ALB, things will still work, but we will have to pay for the provisioned ALB which sends traffic to only one Amazon EC2 instance. Instead, to minimize costs, we must use an Elastic IP.
- () For that Elastic IP to be attached to our Amazon EC2 instance, we must use an EC2 user data script, and our Amazon EC2 instance must have the correct IAM permissions to perform the API call, so we need an Amazon EC2 instance role.
- () Create a Spot Fleet request - A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. The hourly price for a Spot Instance is called a Spot price.
- () The Spot Fleet selects the Spot Instance pools that meet your needs and launches Spot Instances to meet the target capacity for the fleet. By default, Spot Fleets are set to maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated.
- () Spot Fleets requests would not fit our purpose as we are looking at a critical application. Spot instances can be terminated. So this option is incorrect.
- () Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=2, desired=2 - An Auto Scaling Group with desired=2 would create two instances, and this won't work for us as our monolith application is not made to work with two instances as per the given use-case.
- () Create an Application Load Balancer and a target group with the instance(s) of the Auto Scaling Group - If we use an Application Load Balancer (ALB), things will still work, but we will have to pay for the provisioned ALB which sends traffic to only one Amazon EC2 instance. So this option is not correct.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html
- () A media company has its corporate headquarters in Los Angeles with an on-premises data center using an AWS Direct Connect connection to the AWS VPC. The branch offices in San Francisco and Miami use AWS Site-to-Site VPN connections to connect to the AWS VPC. The company is looking for a solution to have the branch offices send and receive data with each other as well as with their corporate headquarters.

**Answer:**
Correct Answer: **Use AWS Budgets to create a daily coverage budget specifically for Compute Savings Plans. Define a coverage threshold and configure notifications to alert relevant stakeholders**

---

## Question 173

**Q:** Which of the following options should be combined to form the MOST cost-efficient solution? (Select three)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=1, desired=1
- (C) Create a Spot Fleet request
- (D) Assign an Amazon EC2 Instance Role to perform the necessary API calls
- (E) Create an elastic IP address (EIP) and use the Amazon EC2 user-data script to attach it
- (F) Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=2, desired=2
- (G) Create an Application Load Balancer and a target group with the instance(s) of the Auto Scaling Group
- (H) Correct options:
- (I) Amazon EC2 Auto Scaling helps you ensure that you have the correct number of Amazon EC2 instances available to handle the load for your application. You create collections of EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling ensures that your group never goes below this size.
- (J) So we have an Auto Scaling Group with desired=1, across two AZ, so that if an instance goes down, it is automatically recreated in another AZ. So this option is correct.
- () Application Load Balancer (ALB) operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- () An Elastic IP address is a static IPv4 address designed for dynamic cloud computing. An Elastic IP address is associated with your AWS account. With an Elastic IP address, you can mask the failure of an instance or software by rapidly remapping the address to another instance in your account.
- () Now, between the ALB and the Elastic IP. If we use an ALB, things will still work, but we will have to pay for the provisioned ALB which sends traffic to only one Amazon EC2 instance. Instead, to minimize costs, we must use an Elastic IP.
- () For that Elastic IP to be attached to our Amazon EC2 instance, we must use an EC2 user data script, and our Amazon EC2 instance must have the correct IAM permissions to perform the API call, so we need an Amazon EC2 instance role.
- () Incorrect options:
- () Create a Spot Fleet request - A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. The hourly price for a Spot Instance is called a Spot price.
- () The Spot Fleet selects the Spot Instance pools that meet your needs and launches Spot Instances to meet the target capacity for the fleet. By default, Spot Fleets are set to maintain target capacity by launching replacement instances after Spot Instances in the fleet are terminated.
- () Spot Fleets requests would not fit our purpose as we are looking at a critical application. Spot instances can be terminated. So this option is incorrect.
- () Create an auto-scaling group that spans across 2 Availability Zones, which min=1, max=2, desired=2 - An Auto Scaling Group with desired=2 would create two instances, and this won't work for us as our monolith application is not made to work with two instances as per the given use-case.
- () Create an Application Load Balancer and a target group with the instance(s) of the Auto Scaling Group - If we use an Application Load Balancer (ALB), things will still work, but we will have to pay for the provisioned ALB which sends traffic to only one Amazon EC2 instance. So this option is not correct.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html
- () A media company has its corporate headquarters in Los Angeles with an on-premises data center using an AWS Direct Connect connection to the AWS VPC. The branch offices in San Francisco and Miami use AWS Site-to-Site VPN connections to connect to the AWS VPC. The company is looking for a solution to have the branch offices send and receive data with each other as well as with their corporate headquarters.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 174

**Q:** As a solutions architect, which of the following AWS services would you recommend addressing this use-case?

**Options:**
- (A) VPC Endpoint
- **(B) AWS VPN CloudHub** [CORRECT]
- (C) VPC Peering connection
- (D) Software VPN
- (E) Correct option:
- (F) Per the given use-case, the corporate headquarters has an AWS Direct Connect connection to the VPC and the branch offices have Site-to-Site VPN connections to the VPC. Therefore using the AWS VPN CloudHub, branch offices can send and receive data with each other as well as with their corporate headquarters.
- (G) AWS VPN CloudHub:
- (H) via - https://docs.aws.amazon.com/vpn/latest/s2svpn/VPN_CloudHub.html
- (I) Incorrect options:
- (J) VPC Peering connection - A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network. VPC peering facilitates a connection between two VPCs within the AWS network, therefore this option cannot be used to send and receive data between the remote branch offices of the company.
- () Software VPN - Amazon VPC offers you the flexibility to fully manage both sides of your Amazon VPC connectivity by creating a VPN connection between your remote network and a software VPN appliance running in your Amazon VPC network. Since Software VPN just handles connectivity between the remote network and Amazon VPC, therefore it cannot be used to send and receive data between the remote branch offices of the company.
- () References:
- () https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/aws-vpn-cloudhub-network-to-amazon.html
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/VPN_CloudHub.html
- () The systems administrator at a company wants to set up a highly available architecture for a bastion host solution.

**Answer:**
Correct Answer: **AWS VPN CloudHub**

---

## Question 175

**Q:** As a solutions architect, which of the following options would you recommend as the solution?

**Options:**
- (A) Create an elastic IP address (EIP) and assign it to all Amazon EC2 instances that are bastion hosts managed by an Auto Scaling Group
- (B) Create a VPC Endpoint for a fleet of Amazon EC2 instances that are bastion hosts managed by an Auto Scaling Group
- (C) Create a public Network Load Balancer that links to Amazon EC2 instances that are bastion hosts managed by an Auto Scaling Group
- (D) Create a public Application Load Balancer that links to Amazon EC2 instances that are bastion hosts managed by an Auto Scaling Group
- (E) Correct option:
- (F) Network Load Balancer is best suited for use-cases involving low latency and high throughput workloads that involve scaling to millions of requests per second. Network Load Balancer operates at the connection level (Layer 4), routing connections to targets - Amazon EC2 instances, microservices, and containers – within Amazon Virtual Private Cloud (Amazon VPC) based on IP protocol data.
- (G) Including bastion hosts in your VPC environment enables you to securely connect to your Linux instances without exposing your environment to the Internet. After you set up your bastion hosts, you can access the other instances in your VPC through Secure Shell (SSH) connections on Linux. Bastion hosts are also configured with security groups to provide fine-grained ingress control.
- (H) You need to remember that Bastion Hosts are using the SSH protocol, which is a TCP based protocol on port 22. They must be publicly accessible.
- (I) Here, the correct answer is to use a Network Load Balancer, which supports TCP traffic, and will automatically allow you to connect to the Amazon EC2 instance in the backend.
- (J) Incorrect options:
- () Create an elastic IP address (EIP) and assign it to all Amazon EC2 instances that are bastion hosts managed by an Auto Scaling Group - An elastic IP address (EIP) can only be attached to one Amazon EC2 instance at a time, so it won't provide you a highly available setup on its own. Note that if we had two Elastic IPs and two Bastion Hosts, this would work.
- () VPC Endpoints are not used on top of Amazon EC2 instances. They're a way to access AWS services privately within your VPC (without using the public internet). This is a distractor.
- () An Application Load Balancer only supports HTTP traffic, which is layer 7, while the SSH protocol is based on TCP and is layer 4. So, the Application Load Balancer doesn't work.
- () References:
- () https://docs.aws.amazon.com/quickstart/latest/linux-bastion/architecture.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/network/introduction.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html
- () A healthcare company wants to run its applications on single-tenant hardware to meet compliance guidelines.
- () Which of the following is the MOST cost-effective way of isolating the Amazon EC2 instances to a single tenant?
- () Dedicated Instances
- () Dedicated Hosts
- () On-Demand Instances
- () Spot Instances
- () Dedicated Instances are Amazon EC2 instances that run in a virtual private cloud (VPC) on hardware that's dedicated to a single customer. Dedicated Instances that belong to different AWS accounts are physically isolated at a hardware level, even if those accounts are linked to a single-payer account. However, Dedicated Instances may share hardware with other instances from the same AWS account that are not Dedicated Instances.
- () A Dedicated Host is also a physical server that's dedicated for your use. With a Dedicated Host, you have visibility and control over how instances are placed on the server.
- () Differences between Dedicated Hosts and Dedicated Instances:
- () via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html#dedicated-hosts-dedicated-instances
- () Spot Instances - A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Your Spot Instance runs whenever capacity is available and the maximum price per hour for your request exceeds the Spot price. Any instance present with unused capacity will be allocated. Even though this is cost-effective, it does not fulfill the single-tenant hardware requirement of the client and hence is not the correct option.
- () Dedicated Hosts - An Amazon EC2 Dedicated Host is a physical server with Amazon EC2 instance capacity fully dedicated to your use. Dedicated Hosts allow you to use your existing software licenses on Amazon EC2 instances. With a Dedicated Host, you have visibility and control over how instances are placed on the server. This option is costlier than the Dedicated Instance and hence is not the right choice for the current requirement.
- () On-Demand Instances - With On-Demand Instances, you pay for the compute capacity by the second with no long-term commitments. You have full control over its lifecycle—you decide when to launch, stop, hibernate, start, reboot, or terminate it. Hardware isolation is not possible and on-demand has one of the costliest instance charges and hence is not the correct answer for current requirements.
- () High Level Overview of Amazon EC2 Instance Purchase Options:
- () via - https://aws.amazon.com/ec2/pricing/
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-instance.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
- () Which solution should the company implement to meet these requirements with the least operational overhead?
- **() Use AWS IAM Identity Center integrated with the organization’s directory. Define permission sets with least-privilege policies for Amazon RDS and Amazon S3. Assign users to groups based on their team roles and map those groups to the appropriate permission sets** [CORRECT]

**Answer:**
Correct Answer: **Use AWS IAM Identity Center integrated with the organization’s directory. Define permission sets with least-privilege policies for Amazon RDS and Amazon S3. Assign users to groups based on their team roles and map those groups to the appropriate permission sets**

---

## Question 176

**Q:** Which of the following is the MOST cost-effective way of isolating the Amazon EC2 instances to a single tenant?

**Options:**
- (A) Dedicated Instances
- (B) Dedicated Hosts
- (C) On-Demand Instances
- (D) Spot Instances
- (E) Correct option:
- (F) Dedicated Instances are Amazon EC2 instances that run in a virtual private cloud (VPC) on hardware that's dedicated to a single customer. Dedicated Instances that belong to different AWS accounts are physically isolated at a hardware level, even if those accounts are linked to a single-payer account. However, Dedicated Instances may share hardware with other instances from the same AWS account that are not Dedicated Instances.
- (G) A Dedicated Host is also a physical server that's dedicated for your use. With a Dedicated Host, you have visibility and control over how instances are placed on the server.
- (H) Differences between Dedicated Hosts and Dedicated Instances:
- (I) via - https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html#dedicated-hosts-dedicated-instances
- (J) Incorrect options:
- () Spot Instances - A Spot Instance is an unused Amazon EC2 instance that is available for less than the On-Demand price. Your Spot Instance runs whenever capacity is available and the maximum price per hour for your request exceeds the Spot price. Any instance present with unused capacity will be allocated. Even though this is cost-effective, it does not fulfill the single-tenant hardware requirement of the client and hence is not the correct option.
- () Dedicated Hosts - An Amazon EC2 Dedicated Host is a physical server with Amazon EC2 instance capacity fully dedicated to your use. Dedicated Hosts allow you to use your existing software licenses on Amazon EC2 instances. With a Dedicated Host, you have visibility and control over how instances are placed on the server. This option is costlier than the Dedicated Instance and hence is not the right choice for the current requirement.
- () On-Demand Instances - With On-Demand Instances, you pay for the compute capacity by the second with no long-term commitments. You have full control over its lifecycle—you decide when to launch, stop, hibernate, start, reboot, or terminate it. Hardware isolation is not possible and on-demand has one of the costliest instance charges and hence is not the correct answer for current requirements.
- () High Level Overview of Amazon EC2 Instance Purchase Options:
- () via - https://aws.amazon.com/ec2/pricing/
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-instance.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html
- () Which solution should the company implement to meet these requirements with the least operational overhead?
- **() Use AWS IAM Identity Center integrated with the organization’s directory. Define permission sets with least-privilege policies for Amazon RDS and Amazon S3. Assign users to groups based on their team roles and map those groups to the appropriate permission sets** [CORRECT]
- () Use AWS Organizations to group team accounts under a single organizational unit (OU). Attach Service Control Policies (SCPs) to the OU that define access boundaries for Amazon RDS and Amazon S3 based on each team’s responsibilities. Assign users to accounts and let SCPs enforce the required access
- () Create individual IAM users for each team member. Attach role-based IAM policies granting permissions to RDS and S3 based on team roles. Use AWS IAM Access Analyzer to monitor for unused permissions and rotate access keys periodically
- () Create an IAM identity provider that integrates with the company's IdP (e.g., Azure AD or Okta). Use SAML federation to grant access to IAM roles that are manually assigned to each user. Create and maintain inline IAM policies for each role to access RDS and S3
- () via - https://docs.aws.amazon.com/singlesignon/latest/userguide/permissionsetsconcept.html
- () https://docs.aws.amazon.com/singlesignon/latest/userguide/getting-started.html
- () https://docs.aws.amazon.com/singlesignon/latest/userguide/permissionsetsconcept.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () A software engineering intern at a company is documenting the features offered by Amazon EC2 Spot instances and Spot fleets.
- () Can you help the intern by selecting the correct options that identify the key characteristics of these two types of Spot entities? (Select two)
- () A Spot fleet can only consist of a set of Spot Instances that are launched to meet your target capacity
- () Correct selection
- () A Spot fleet can consist of a set of Spot Instances and optionally On-Demand Instances that are launched to meet your target capacity

**Answer:**
Correct Answer: **Use AWS IAM Identity Center integrated with the organization’s directory. Define permission sets with least-privilege policies for Amazon RDS and Amazon S3. Assign users to groups based on their team roles and map those groups to the appropriate permission sets**

---

## Question 177

**Q:** Which solution should the company implement to meet these requirements with the least operational overhead?

**Options:**
- (A) Use AWS IAM Identity Center integrated with the organization’s directory. Define permission sets with least-privilege policies for Amazon RDS and Amazon S3. Assign users to groups based on their team roles and map those groups to the appropriate permission sets
- (B) Use AWS Organizations to group team accounts under a single organizational unit (OU). Attach Service Control Policies (SCPs) to the OU that define access boundaries for Amazon RDS and Amazon S3 based on each team’s responsibilities. Assign users to accounts and let SCPs enforce the required access
- (C) Create individual IAM users for each team member. Attach role-based IAM policies granting permissions to RDS and S3 based on team roles. Use AWS IAM Access Analyzer to monitor for unused permissions and rotate access keys periodically
- (D) Create an IAM identity provider that integrates with the company's IdP (e.g., Azure AD or Okta). Use SAML federation to grant access to IAM roles that are manually assigned to each user. Create and maintain inline IAM policies for each role to access RDS and S3
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/singlesignon/latest/userguide/permissionsetsconcept.html
- (G) Incorrect options:
- (H) References:
- (I) https://docs.aws.amazon.com/singlesignon/latest/userguide/getting-started.html
- (J) https://docs.aws.amazon.com/singlesignon/latest/userguide/permissionsetsconcept.html
- () https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_saml.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps.html
- () A software engineering intern at a company is documenting the features offered by Amazon EC2 Spot instances and Spot fleets.
- () Can you help the intern by selecting the correct options that identify the key characteristics of these two types of Spot entities? (Select two)
- () A Spot fleet can only consist of a set of Spot Instances that are launched to meet your target capacity
- () Correct selection
- () A Spot fleet can consist of a set of Spot Instances and optionally On-Demand Instances that are launched to meet your target capacity
- () Spot instances are spare Amazon EC2 capacity that can save you up 90% off of On-Demand prices. Spot instances can be interrupted by Amazon EC2 for capacity requirements with a 2-minute notification
- () Spot fleets are spare EC2 capacity that can save you up 90% off of On-Demand prices. Spot fleets are usually interrupted by Amazon EC2 for capacity requirements with a 2-minute notification
- () Spot fleets allow you to request Amazon EC2 Spot instances for 1 to 6 hours at a time to avoid being interrupted
- () Correct options:
- () Spot instances are spare Amazon EC2 capacity that can save you up 90% off of On-Demand prices that Amazon Web Services can interrupt with a 2-minute notification. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted.
- () via - https://docs.amazonaws.cn/en_us/AWSEC2/latest/UserGuide/how-spot-fleet-works.html
- () These two options contradict the explanation provided above, so these options are incorrect.
- () Spot fleets allow you to request Amazon EC2 Spot instances for 1 to 6 hours at a time to avoid being interrupted - You could use Spot blocks (now deprecated) to request Amazon EC2 Spot instances for 1 to 6 hours to avoid being interrupted. So, Spot fleets cannot be used for this purpose.
- () https://www.amazonaws.cn/en/ec2/spot-instances/faqs/
- () https://docs.amazonaws.cn/en_us/AWSEC2/latest/UserGuide/how-spot-fleet-works.html
- () A healthcare company runs a fleet of Amazon EC2 instances in two private subnets (named PR1 and PR2) across two Availability Zones (AZs) named A1 and A2. The Amazon EC2 instances need access to the internet for operating system patch management and third-party software maintenance. To facilitate this, the engineering team at the company wants to set up two Network Address Translation gateways (NAT gateways) in a highly available configuration.
- () Which of the following options would you suggest?
- () Set up a total of one NAT gateway. NAT gateway N1 should be set up in public subnet PU1 in any of the Availability Zones A1 or A2
- () Set up a total of two NAT gateways. Both NAT gateways N1 and N2 should be set up in a single public subnet PU1 in any of the Availability Zones A1 or A2
- () Set up a total of two NAT gateways. NAT gateway N1 should be set up in private subnet PR1 in Availability Zone A1. NAT gateway N2 should be set up in private subnet PR2 in Availability Zone A2
- **() Set up a total of two NAT gateways. NAT gateway N1 should be set up in public subnet PU1 in Availability Zone A1. NAT gateway N2 should be set up in public subnet PU2 in Availability Zone A2** [CORRECT]

**Answer:**
Correct Answer: **Set up a total of two NAT gateways. NAT gateway N1 should be set up in public subnet PU1 in Availability Zone A1. NAT gateway N2 should be set up in public subnet PU2 in Availability Zone A2**

---

## Question 178

**Q:** Can you help the intern by selecting the correct options that identify the key characteristics of these two types of Spot entities? (Select two)

**Options:**
- (A) A Spot fleet can only consist of a set of Spot Instances that are launched to meet your target capacity
- (B) Correct selection
- (C) A Spot fleet can consist of a set of Spot Instances and optionally On-Demand Instances that are launched to meet your target capacity
- (D) Spot instances are spare Amazon EC2 capacity that can save you up 90% off of On-Demand prices. Spot instances can be interrupted by Amazon EC2 for capacity requirements with a 2-minute notification
- (E) Spot fleets are spare EC2 capacity that can save you up 90% off of On-Demand prices. Spot fleets are usually interrupted by Amazon EC2 for capacity requirements with a 2-minute notification
- (F) Spot fleets allow you to request Amazon EC2 Spot instances for 1 to 6 hours at a time to avoid being interrupted
- (G) Correct options:
- (H) Spot instances are spare Amazon EC2 capacity that can save you up 90% off of On-Demand prices that Amazon Web Services can interrupt with a 2-minute notification. Because Spot Instances enable you to request unused EC2 instances at steep discounts, you can lower your Amazon EC2 costs significantly. Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted.
- (I) via - https://docs.amazonaws.cn/en_us/AWSEC2/latest/UserGuide/how-spot-fleet-works.html
- (J) Incorrect options:
- () These two options contradict the explanation provided above, so these options are incorrect.
- () Spot fleets allow you to request Amazon EC2 Spot instances for 1 to 6 hours at a time to avoid being interrupted - You could use Spot blocks (now deprecated) to request Amazon EC2 Spot instances for 1 to 6 hours to avoid being interrupted. So, Spot fleets cannot be used for this purpose.
- () References:
- () https://www.amazonaws.cn/en/ec2/spot-instances/faqs/
- () https://docs.amazonaws.cn/en_us/AWSEC2/latest/UserGuide/how-spot-fleet-works.html
- () A healthcare company runs a fleet of Amazon EC2 instances in two private subnets (named PR1 and PR2) across two Availability Zones (AZs) named A1 and A2. The Amazon EC2 instances need access to the internet for operating system patch management and third-party software maintenance. To facilitate this, the engineering team at the company wants to set up two Network Address Translation gateways (NAT gateways) in a highly available configuration.
- () Which of the following options would you suggest?
- () Set up a total of one NAT gateway. NAT gateway N1 should be set up in public subnet PU1 in any of the Availability Zones A1 or A2
- () Set up a total of two NAT gateways. Both NAT gateways N1 and N2 should be set up in a single public subnet PU1 in any of the Availability Zones A1 or A2
- () Set up a total of two NAT gateways. NAT gateway N1 should be set up in private subnet PR1 in Availability Zone A1. NAT gateway N2 should be set up in private subnet PR2 in Availability Zone A2
- () Set up a total of two NAT gateways. NAT gateway N1 should be set up in public subnet PU1 in Availability Zone A1. NAT gateway N2 should be set up in public subnet PU2 in Availability Zone A2
- () Correct option:
- () A NAT gateway is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.
- () For the given use case, the Amazon EC2 instances in the private subnets can connect to the internet through public NAT gateways in their respective Availability Zones (AZ). You should create public NAT gateway in the public subnet of each AZ and must associate an elastic IP address with the NAT gateway at creation. Then, you can route traffic from the NAT gateway to the internet gateway for the VPC.
- () If you have resources in multiple Availability Zones and they share one NAT gateway, and if the NAT gateway’s Availability Zone is down, resources in the other Availability Zones lose internet access. To create a highly available or an Availability Zone independent architecture, create a NAT gateway in each Availability Zone and configure your routing to ensure that resources use the NAT gateway in the same Availability Zone.
- () via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () Set up a total of two NAT gateways. NAT gateway N1 should be set up in private subnet PR1 in Availability Zone A1. NAT gateway N2 should be set up in private subnet PR2 in Availability Zone A2 - For the Amazon EC2 instances in the private subnet, you can facilitate outbound internet connectivity in a highly available configuration by creating a public NAT gateway in the public subnet of each AZ. You cannot create NAT gateways in the private subnet for the given use case.
- () Set up a total of two NAT gateways. Both NAT gateways N1 and N2 should be set up in a single public subnet PU1 in any of the Availability Zones A1 or A2 - For the Amazon EC2 instances in the private subnet, you can facilitate outbound internet connectivity in a highly available configuration by creating a public NAT gateway in the public subnet of each AZ. You cannot create both NAT gateways in a single public subnet, as this configuration would not be highly available.
- () Set up a total of one NAT gateway. NAT gateway N1 should be set up in public subnet PU1 in any of the Availability Zones A1 or A2 - For the Amazon EC2 instances in the private subnet, you can facilitate outbound internet connectivity in a highly available configuration by creating a public NAT gateway in the public subnet of each AZ. You cannot create a single NAT gateway, as this configuration would not be highly available.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () The development team at a company manages a Python based nightly process with a runtime of 30 minutes. The process can withstand any interruptions in its execution and start over again. The process currently runs on the on-premises infrastructure and it needs to be migrated to AWS.
- () Which of the following options do you recommend as the MOST cost-effective solution?
- () Run on AWS Lambda
- () Run on Amazon EMR
- () Run on an Application Load Balancer
- **() Run on a Spot Instance with a persistent request type** [CORRECT]

**Answer:**
Correct Answer: **Run on a Spot Instance with a persistent request type**

---

## Question 179

**Q:** Which of the following options would you suggest?

**Options:**
- (A) Set up a total of one NAT gateway. NAT gateway N1 should be set up in public subnet PU1 in any of the Availability Zones A1 or A2
- (B) Set up a total of two NAT gateways. Both NAT gateways N1 and N2 should be set up in a single public subnet PU1 in any of the Availability Zones A1 or A2
- (C) Set up a total of two NAT gateways. NAT gateway N1 should be set up in private subnet PR1 in Availability Zone A1. NAT gateway N2 should be set up in private subnet PR2 in Availability Zone A2
- (D) Set up a total of two NAT gateways. NAT gateway N1 should be set up in public subnet PU1 in Availability Zone A1. NAT gateway N2 should be set up in public subnet PU2 in Availability Zone A2
- (E) Correct option:
- (F) A NAT gateway is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances.
- (G) For the given use case, the Amazon EC2 instances in the private subnets can connect to the internet through public NAT gateways in their respective Availability Zones (AZ). You should create public NAT gateway in the public subnet of each AZ and must associate an elastic IP address with the NAT gateway at creation. Then, you can route traffic from the NAT gateway to the internet gateway for the VPC.
- (H) If you have resources in multiple Availability Zones and they share one NAT gateway, and if the NAT gateway’s Availability Zone is down, resources in the other Availability Zones lose internet access. To create a highly available or an Availability Zone independent architecture, create a NAT gateway in each Availability Zone and configure your routing to ensure that resources use the NAT gateway in the same Availability Zone.
- (I) via - https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- (J) Incorrect options:
- () Set up a total of two NAT gateways. NAT gateway N1 should be set up in private subnet PR1 in Availability Zone A1. NAT gateway N2 should be set up in private subnet PR2 in Availability Zone A2 - For the Amazon EC2 instances in the private subnet, you can facilitate outbound internet connectivity in a highly available configuration by creating a public NAT gateway in the public subnet of each AZ. You cannot create NAT gateways in the private subnet for the given use case.
- () Set up a total of two NAT gateways. Both NAT gateways N1 and N2 should be set up in a single public subnet PU1 in any of the Availability Zones A1 or A2 - For the Amazon EC2 instances in the private subnet, you can facilitate outbound internet connectivity in a highly available configuration by creating a public NAT gateway in the public subnet of each AZ. You cannot create both NAT gateways in a single public subnet, as this configuration would not be highly available.
- () Set up a total of one NAT gateway. NAT gateway N1 should be set up in public subnet PU1 in any of the Availability Zones A1 or A2 - For the Amazon EC2 instances in the private subnet, you can facilitate outbound internet connectivity in a highly available configuration by creating a public NAT gateway in the public subnet of each AZ. You cannot create a single NAT gateway, as this configuration would not be highly available.
- () Reference:
- () https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html
- () The development team at a company manages a Python based nightly process with a runtime of 30 minutes. The process can withstand any interruptions in its execution and start over again. The process currently runs on the on-premises infrastructure and it needs to be migrated to AWS.
- () Which of the following options do you recommend as the MOST cost-effective solution?
- () Run on AWS Lambda
- () Run on Amazon EMR
- () Run on an Application Load Balancer
- () Run on a Spot Instance with a persistent request type
- () Run on an Application Load Balancer - Application Load Balancer operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- () Application Load Balancer helps distribute load for HTTP(S) requests. This option has been added as a distractor.
- () Run on Amazon EMR - Amazon EMR is the industry-leading cloud big data platform for processing vast amounts of data using open source tools such as Apache Spark, Apache Hive, Apache HBase, Apache Flink, Apache Hudi, and Presto. Amazon EMR uses Hadoop, an open-source framework, to distribute your data and processing across a resizable cluster of Amazon EC2 instances.
- () Amazon EMR is to run Big Data load that is meant to be run on Hadoop, this is also a distractor.
- () Run on AWS Lambda - AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume.
- () AWS Lambda would be the perfect fit if our script could run in less than 15 minutes, as this is the maximum timeout for AWS Lambda.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-requests.html
- () The engineering team at an IT company is deploying an Online Transactional Processing (OLTP) application that needs to support relational queries. The application will have unpredictable spikes of usage that the team does not know in advance.
- () Which database would you recommend using?
- **() Amazon Aurora Serverless** [CORRECT]
- () Amazon ElastiCache
- () Amazon DynamoDB with Provisioned Capacity and Auto Scaling
- () Amazon DynamoDB with On-Demand Capacity
- () Amazon Aurora Serverless is the perfect way to create a database that can scale down to 0 servers, and scale up to many servers, as an OLTP database. So this is the correct option.

**Answer:**
Correct Answer: **Amazon Aurora Serverless**

---

## Question 180

**Q:** Which of the following options do you recommend as the MOST cost-effective solution?

**Options:**
- (A) Run on AWS Lambda
- (B) Run on Amazon EMR
- (C) Run on an Application Load Balancer
- (D) Run on a Spot Instance with a persistent request type
- (E) Correct option:
- (F) Incorrect options:
- (G) Run on an Application Load Balancer - Application Load Balancer operates at the request level (layer 7), routing traffic to targets – Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions based on the content of the request. Ideal for advanced load balancing of HTTP and HTTPS traffic, Application Load Balancer provides advanced request routing targeted at delivery of modern application architectures, including microservices and container-based applications.
- (H) Application Load Balancer helps distribute load for HTTP(S) requests. This option has been added as a distractor.
- (I) Run on Amazon EMR - Amazon EMR is the industry-leading cloud big data platform for processing vast amounts of data using open source tools such as Apache Spark, Apache Hive, Apache HBase, Apache Flink, Apache Hudi, and Presto. Amazon EMR uses Hadoop, an open-source framework, to distribute your data and processing across a resizable cluster of Amazon EC2 instances.
- (J) Amazon EMR is to run Big Data load that is meant to be run on Hadoop, this is also a distractor.
- () Run on AWS Lambda - AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume.
- () AWS Lambda would be the perfect fit if our script could run in less than 15 minutes, as this is the maximum timeout for AWS Lambda.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/spot-requests.html
- () The engineering team at an IT company is deploying an Online Transactional Processing (OLTP) application that needs to support relational queries. The application will have unpredictable spikes of usage that the team does not know in advance.
- () Which database would you recommend using?
- () Amazon Aurora Serverless
- () Amazon ElastiCache
- () Amazon DynamoDB with Provisioned Capacity and Auto Scaling
- () Amazon DynamoDB with On-Demand Capacity
- () Amazon Aurora Serverless is the perfect way to create a database that can scale down to 0 servers, and scale up to many servers, as an OLTP database. So this is the correct option.
- () Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.
- () Amazon DynamoDB is a NoSQL database and doesn't do relational queries, therefore it's a choice we have to eliminate, even though the two modes proposed here help us cope with an unpredictable amount of usage. So both these options are incorrect.
- () References:
- () https://aws.amazon.com/rds/aurora/serverless/
- () https://aws.amazon.com/rds/
- () What is the most efficient solution to meet this goal with the least operational overhead?
- () Deploy an AWS Lambda function to run daily in each developer’s account. Use the function to analyze cost usage reports via the Cost Explorer API. If costs exceed a predefined threshold, the function invokes an AWS Config remediation rule
- () Use AWS Service Catalog to restrict developers to predefined resource templates with pricing limits. In each developer account, create a scheduled Lambda function that stops all running resources at the end of the day and and restart these resources at the start of next business day
- () Use AWS Cost Explorer to enable detailed usage and cost reports for each developer account. Configure daily usage reports to be emailed to developers. Create dashboards for each developer in Cost Explorer, and require them to monitor their resource consumption and take action if they approach spending thresholds
- **() Use AWS Budgets to define spending thresholds for each developer’s account. Configure budget alerts to notify developers when actual or forecasted usage exceeds the set limit. Attach Budgets actions to automatically apply a restrictive DenyAll IAM policy to the developer’s primary IAM role when the budget threshold is crossed** [CORRECT]
- () This option combines budget tracking, notification, and enforcement using native AWS Budgets capabilities. With Budgets actions, administrators can define automated responses (e.g., applying a DenyAll policy) when a user’s spend exceeds the defined budget. This solution is fully serverless, scalable, and low maintenance — ideal for controlling developer costs without requiring daily manual intervention.

**Answer:**
Correct Answer: **Use AWS Budgets to define spending thresholds for each developer’s account. Configure budget alerts to notify developers when actual or forecasted usage exceeds the set limit. Attach Budgets actions to automatically apply a restrictive DenyAll IAM policy to the developer’s primary IAM role when the budget threshold is crossed**

---

## Question 181

**Q:** Which database would you recommend using?

**Options:**
- (A) Amazon Aurora Serverless
- (B) Amazon ElastiCache
- (C) Amazon DynamoDB with Provisioned Capacity and Auto Scaling
- (D) Amazon DynamoDB with On-Demand Capacity
- (E) Correct option:
- (F) Amazon Aurora Serverless is the perfect way to create a database that can scale down to 0 servers, and scale up to many servers, as an OLTP database. So this is the correct option.
- (G) Incorrect options:
- (H) Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.
- (I) Amazon DynamoDB is a NoSQL database and doesn't do relational queries, therefore it's a choice we have to eliminate, even though the two modes proposed here help us cope with an unpredictable amount of usage. So both these options are incorrect.
- (J) References:
- () https://aws.amazon.com/rds/aurora/serverless/
- () https://aws.amazon.com/rds/
- () What is the most efficient solution to meet this goal with the least operational overhead?
- () Deploy an AWS Lambda function to run daily in each developer’s account. Use the function to analyze cost usage reports via the Cost Explorer API. If costs exceed a predefined threshold, the function invokes an AWS Config remediation rule
- () Use AWS Service Catalog to restrict developers to predefined resource templates with pricing limits. In each developer account, create a scheduled Lambda function that stops all running resources at the end of the day and and restart these resources at the start of next business day
- () Use AWS Cost Explorer to enable detailed usage and cost reports for each developer account. Configure daily usage reports to be emailed to developers. Create dashboards for each developer in Cost Explorer, and require them to monitor their resource consumption and take action if they approach spending thresholds
- **() Use AWS Budgets to define spending thresholds for each developer’s account. Configure budget alerts to notify developers when actual or forecasted usage exceeds the set limit. Attach Budgets actions to automatically apply a restrictive DenyAll IAM policy to the developer’s primary IAM role when the budget threshold is crossed** [CORRECT]
- () This option combines budget tracking, notification, and enforcement using native AWS Budgets capabilities. With Budgets actions, administrators can define automated responses (e.g., applying a DenyAll policy) when a user’s spend exceeds the defined budget. This solution is fully serverless, scalable, and low maintenance — ideal for controlling developer costs without requiring daily manual intervention.
- () https://aws.amazon.com/blogs/aws-cloud-financial-management/get-started-with-aws-budgets-actions/
- () https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html
- () A company is developing a document management application on AWS. The application runs on Amazon EC2 instances in multiple Availability Zones (AZs). The company requires the document store to be highly available and the documents need to be returned immediately when requested. The engineering team has configured the application to use Amazon Elastic Block Store (Amazon EBS) to store the documents but the team is willing to consider other options to meet the availability requirement.

**Answer:**
Correct Answer: **Use AWS Budgets to define spending thresholds for each developer’s account. Configure budget alerts to notify developers when actual or forecasted usage exceeds the set limit. Attach Budgets actions to automatically apply a restrictive DenyAll IAM policy to the developer’s primary IAM role when the budget threshold is crossed**

---

## Question 182

**Q:** What is the most efficient solution to meet this goal with the least operational overhead?

**Options:**
- (A) Deploy an AWS Lambda function to run daily in each developer’s account. Use the function to analyze cost usage reports via the Cost Explorer API. If costs exceed a predefined threshold, the function invokes an AWS Config remediation rule
- (B) Use AWS Service Catalog to restrict developers to predefined resource templates with pricing limits. In each developer account, create a scheduled Lambda function that stops all running resources at the end of the day and and restart these resources at the start of next business day
- (C) Use AWS Cost Explorer to enable detailed usage and cost reports for each developer account. Configure daily usage reports to be emailed to developers. Create dashboards for each developer in Cost Explorer, and require them to monitor their resource consumption and take action if they approach spending thresholds
- **(D) Use AWS Budgets to define spending thresholds for each developer’s account. Configure budget alerts to notify developers when actual or forecasted usage exceeds the set limit. Attach Budgets actions to automatically apply a restrictive DenyAll IAM policy to the developer’s primary IAM role when the budget threshold is crossed** [CORRECT]
- (E) Correct option:
- (F) This option combines budget tracking, notification, and enforcement using native AWS Budgets capabilities. With Budgets actions, administrators can define automated responses (e.g., applying a DenyAll policy) when a user’s spend exceeds the defined budget. This solution is fully serverless, scalable, and low maintenance — ideal for controlling developer costs without requiring daily manual intervention.
- (G) Incorrect options:
- (H) References:
- (I) https://aws.amazon.com/blogs/aws-cloud-financial-management/get-started-with-aws-budgets-actions/
- (J) https://docs.aws.amazon.com/cost-management/latest/userguide/ce-what-is.html
- () A company is developing a document management application on AWS. The application runs on Amazon EC2 instances in multiple Availability Zones (AZs). The company requires the document store to be highly available and the documents need to be returned immediately when requested. The engineering team has configured the application to use Amazon Elastic Block Store (Amazon EBS) to store the documents but the team is willing to consider other options to meet the availability requirement.

**Answer:**
Correct Answer: **Use AWS Budgets to define spending thresholds for each developer’s account. Configure budget alerts to notify developers when actual or forecasted usage exceeds the set limit. Attach Budgets actions to automatically apply a restrictive DenyAll IAM policy to the developer’s primary IAM role when the budget threshold is crossed**

---

## Question 183

**Q:** As a solutions architect, which of the following will you recommend?

**Options:**
- (A) Create snapshots for the Amazon EBS volumes regularly and then build new volumes using those snapshots in additional Availability Zones
- (B) Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 Glacier as the document store
- (C) Provision at least three Provisioned IOPS Amazon Instance Store volumes for the Amazon EC2 instances and then mount these volumes to multiple Amazon EC2 instances
- (D) Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 as the document store
- (E) Correct option:
- (F) Instances that use Amazon EBS for the root device automatically have an Amazon EBS volume attached. When you launch an Amazon EBS-backed instance, AWS creates an Amazon EBS volume for each Amazon EBS snapshot referenced by the AMI you use. An Amazon EBS-backed instance can be stopped and later restarted without affecting data stored in the attached volumes.
- (G) Amazon S3 provides access to reliable, fast, and inexpensive data storage infrastructure. It is designed to make web-scale computing easier by enabling you to store and retrieve any amount of data, at any time, from within Amazon EC2 or anywhere on the web. S3 is highly available and can be configured to work as a document store for the given use case.
- (H) Incorrect options:
- (I) Set up Amazon EBS as the Amazon EC2 instance root volume and then configure the application to use Amazon S3 Glacier as the document store - As the documents need to be returned immediately when requested, Amazon S3 Glacier is not the right fit, since there is a lag of several minutes/hours when you want to read data from Glacier.
- (J) Provision at least three Provisioned IOPS Amazon Instance Store volumes for the Amazon EC2 instances and then mount these volumes to multiple Amazon EC2 instances - You cannot mount Instance Store volumes to multiple Amazon EC2 instances. An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html
- () https://aws.amazon.com/s3/storage-classes/
- () A company needs an Active Directory service to run directory-aware workloads in the AWS Cloud and it should also support configuring a trust relationship with any existing on-premises Microsoft Active Directory.
- () Which AWS Directory Service is the best fit for this requirement?
- () Active Directory Connector
- () Simple Active Directory (Simple AD)
- () AWS Transit Gateway
- () AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)
- () AWS Directory Service lets you run Microsoft Active Directory (AD) as a managed service. AWS Directory Service for Microsoft Active Directory, also referred to as AWS Managed Microsoft AD, is powered by Windows Server 2012 R2. When you select and launch this directory type, it is created as a highly available pair of domain controllers connected to your virtual private cloud (VPC).
- () With AWS Managed Microsoft AD, you can run directory-aware workloads in the AWS Cloud, including Microsoft SharePoint and custom .NET and SQL Server-based applications. You can also configure a trust relationship between AWS Managed Microsoft AD in the AWS Cloud and your existing on-premises Microsoft Active Directory, providing users and groups with access to resources in either domain, using single sign-on (SSO).
- () AWS Managed Microsoft AD is your best choice if you need actual Active Directory features to support AWS applications or Windows workloads, including Amazon Relational Database Service for Microsoft SQL Server. It's also best if you want a standalone AD in the AWS Cloud that supports Office 365 or you need an LDAP directory to support your Linux applications.
- () Active Directory Connector - AD Connector is a directory gateway with which you can redirect directory requests to your on-premises Microsoft Active Directory without caching any information in the cloud. AD Connector is your best choice when you want to use your existing on-premises directory with compatible AWS services.
- () AWS Transit Gateway - AWS Transit Gateway connects VPCs and on-premises networks through a central hub. Transit Gateway is not an Active Directory service.
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_simple_ad.html
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_ad_connector.html
- () A company helps its customers legally sign highly confidential contracts. To meet the strong industry requirements, the company must ensure that the signed contracts are encrypted using the company's proprietary algorithm. The company is now migrating to AWS Cloud using Amazon Simple Storage Service (Amazon S3) and would like you, the solution architect, to advise them on the encryption scheme to adopt.
- () What do you recommend?
- () Server-side encryption with customer-provided keys (SSE-C)
- () Server-side encryption with AWS KMS keys (SSE-KMS)
- () Server-side encryption with Amazon S3 managed keys (SSE-S3)
- **() Client Side Encryption** [CORRECT]
- () Server-side encryption with AWS KMS keys (SSE-KMS) - AWS Key Management Service (AWS KMS) is a service that combines secure, highly available hardware and software to provide a key management system scaled for the cloud. When you use server-side encryption with AWS KMS (SSE-KMS), you can specify a customer-managed CMK that you have already created. SSE-KMS provides you with an audit trail that shows when your CMK was used and by whom.
- () Server-side encryption with Amazon S3 managed keys (SSE-S3) - When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key.
- () Server-side encryption with customer-provided keys (SSE-C) - With Server-Side Encryption with Customer-Provided Keys (SSE-C), you manage the encryption keys and Amazon S3 manages the encryption, as it writes to disks, and decryption when you access your objects.

**Answer:**
Correct Answer: **Client Side Encryption**

---

## Question 184

**Q:** Which AWS Directory Service is the best fit for this requirement?

**Options:**
- (A) Active Directory Connector
- (B) Simple Active Directory (Simple AD)
- (C) AWS Transit Gateway
- (D) AWS Directory Service for Microsoft Active Directory (AWS Managed Microsoft AD)
- (E) Correct option:
- (F) AWS Directory Service lets you run Microsoft Active Directory (AD) as a managed service. AWS Directory Service for Microsoft Active Directory, also referred to as AWS Managed Microsoft AD, is powered by Windows Server 2012 R2. When you select and launch this directory type, it is created as a highly available pair of domain controllers connected to your virtual private cloud (VPC).
- (G) With AWS Managed Microsoft AD, you can run directory-aware workloads in the AWS Cloud, including Microsoft SharePoint and custom .NET and SQL Server-based applications. You can also configure a trust relationship between AWS Managed Microsoft AD in the AWS Cloud and your existing on-premises Microsoft Active Directory, providing users and groups with access to resources in either domain, using single sign-on (SSO).
- (H) AWS Managed Microsoft AD is your best choice if you need actual Active Directory features to support AWS applications or Windows workloads, including Amazon Relational Database Service for Microsoft SQL Server. It's also best if you want a standalone AD in the AWS Cloud that supports Office 365 or you need an LDAP directory to support your Linux applications.
- (I) Incorrect options:
- (J) Active Directory Connector - AD Connector is a directory gateway with which you can redirect directory requests to your on-premises Microsoft Active Directory without caching any information in the cloud. AD Connector is your best choice when you want to use your existing on-premises directory with compatible AWS services.
- () AWS Transit Gateway - AWS Transit Gateway connects VPCs and on-premises networks through a central hub. Transit Gateway is not an Active Directory service.
- () References:
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_simple_ad.html
- () https://docs.aws.amazon.com/directoryservice/latest/admin-guide/directory_ad_connector.html
- () A company helps its customers legally sign highly confidential contracts. To meet the strong industry requirements, the company must ensure that the signed contracts are encrypted using the company's proprietary algorithm. The company is now migrating to AWS Cloud using Amazon Simple Storage Service (Amazon S3) and would like you, the solution architect, to advise them on the encryption scheme to adopt.
- () What do you recommend?
- () Server-side encryption with customer-provided keys (SSE-C)
- () Server-side encryption with AWS KMS keys (SSE-KMS)
- () Server-side encryption with Amazon S3 managed keys (SSE-S3)
- () Client Side Encryption
- () Server-side encryption with AWS KMS keys (SSE-KMS) - AWS Key Management Service (AWS KMS) is a service that combines secure, highly available hardware and software to provide a key management system scaled for the cloud. When you use server-side encryption with AWS KMS (SSE-KMS), you can specify a customer-managed CMK that you have already created. SSE-KMS provides you with an audit trail that shows when your CMK was used and by whom.
- () Server-side encryption with Amazon S3 managed keys (SSE-S3) - When you use Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3), each object is encrypted with a unique key.
- () Server-side encryption with customer-provided keys (SSE-C) - With Server-Side Encryption with Customer-Provided Keys (SSE-C), you manage the encryption keys and Amazon S3 manages the encryption, as it writes to disks, and decryption when you access your objects.
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingKMSEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingClientSideEncryption.html
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/serv-side-encryption.html
- () You are looking to build an index of your files in Amazon S3, using Amazon RDS PostgreSQL. To build this index, it is necessary to read the first 250 bytes of each object in Amazon S3, which contains some metadata about the content of the file itself. There are over 100,000 files in your S3 bucket, amounting to 50 terabytes of data.
- () How can you build this index efficiently?
- **() Create an application that will traverse the S3 bucket, issue a Byte Range Fetch for the first 250 bytes, and store that information in Amazon RDS** [CORRECT]
- () Create an application that will traverse the Amazon S3 bucket, then use S3 Select Byte Range Fetch parameter to get the first 250 bytes, and store that information in Amazon RDS
- () Create an application that will traverse the Amazon S3 bucket, read all the files one by one, extract the first 250 bytes, and store that information in Amazon RDS
- () Use the Amazon RDS Import feature to load the data from Amazon S3 to PostgreSQL, and run a SQL query to build the index
- () Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.
- () Using the Range HTTP header in a GET Object request, you can fetch a byte-range from an object, transferring only the specified portion. You can use concurrent connections to Amazon S3 to fetch different byte ranges from within the same object. This helps you achieve higher aggregate throughput versus a single whole-object request. Fetching smaller ranges of a large object also allows your application to improve retry times when requests are interrupted.
- () A byte-range request is a perfect way to get the beginning of a file and ensuring we remain efficient during our scan of our Amazon S3 bucket. So this is the correct option.
- () Use the Amazon RDS Import feature to load the data from Amazon S3 to PostgreSQL, and run a SQL query to build the index - You cannot import data from Amazon S3 into Amazon RDS, so this option is incorrect.

**Answer:**
Correct Answer: **Create an application that will traverse the S3 bucket, issue a Byte Range Fetch for the first 250 bytes, and store that information in Amazon RDS**

---

## Question 185

**Q:** How can you build this index efficiently?

**Options:**
- (A) Create an application that will traverse the S3 bucket, issue a Byte Range Fetch for the first 250 bytes, and store that information in Amazon RDS
- (B) Create an application that will traverse the Amazon S3 bucket, then use S3 Select Byte Range Fetch parameter to get the first 250 bytes, and store that information in Amazon RDS
- (C) Create an application that will traverse the Amazon S3 bucket, read all the files one by one, extract the first 250 bytes, and store that information in Amazon RDS
- (D) Use the Amazon RDS Import feature to load the data from Amazon S3 to PostgreSQL, and run a SQL query to build the index
- (E) Correct option:
- (F) Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.
- (G) Using the Range HTTP header in a GET Object request, you can fetch a byte-range from an object, transferring only the specified portion. You can use concurrent connections to Amazon S3 to fetch different byte ranges from within the same object. This helps you achieve higher aggregate throughput versus a single whole-object request. Fetching smaller ranges of a large object also allows your application to improve retry times when requests are interrupted.
- (H) A byte-range request is a perfect way to get the beginning of a file and ensuring we remain efficient during our scan of our Amazon S3 bucket. So this is the correct option.
- (I) Incorrect options:
- (J) Use the Amazon RDS Import feature to load the data from Amazon S3 to PostgreSQL, and run a SQL query to build the index - You cannot import data from Amazon S3 into Amazon RDS, so this option is incorrect.
- () Create an application that will traverse the Amazon S3 bucket, read all the files one by one, extract the first 250 bytes, and store that information in Amazon RDS - If you build an application that loads all the files from Amazon S3, that would work, but you would read 50TB of data and that may be very expensive and slow. So this option is incorrect.
- () Exam Alert:
- () Please note that with Amazon S3 Select, you can scan a subset of an object by specifying a range of bytes to query using the ScanRange parameter. This capability lets you parallelize scanning the whole object by splitting the work into separate Amazon S3 Select requests for a series of non-overlapping scan ranges. Use the Amazon S3 Select ScanRange parameter and Start at (Byte) and End at (Byte).
- () via - https://docs.aws.amazon.com/AmazonS3/latest/dev/selecting-content-from-objects.html
- () Reference:
- () https://docs.aws.amazon.com/AmazonS3/latest/dev/optimizing-performance-guidelines.html#optimizing-performance-guidelines-get-range
- () Which solution meets these requirements most cost-effectively?
- () Configure an S3 Lifecycle policy to migrate datasets to S3 Glacier Flexible Retrieval after 30 days and delete them automatically 4 years after creation
- () Set up an S3 Lifecycle configuration to transfer all datasets to S3 One Zone-Infrequent Access (S3 One Zone-IA) after 30 days, and permanently delete them 4 years after creation
- () Define an S3 Lifecycle policy that transitions datasets to S3 Glacier Instant Retrieval 30 days after creation and schedules the deletion of each object exactly 4 years after its creation
- **() Define an S3 Lifecycle policy that transitions datasets to S3 Standard-Infrequent Access (S3 Standard-IA) 30 days after creation and schedules the deletion of each object exactly 4 years after its creation** [CORRECT]
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
- () https://aws.amazon.com/s3/pricing/
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/storage-class-intro.html#sc-infreq-data-access
- () A company manages a multi-tier social media application that runs on Amazon Elastic Compute Cloud (Amazon EC2) instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto Scaling group across multiple Availability Zones (AZs) and use an Amazon Aurora database. As an AWS Certified Solutions Architect – Associate, you have been tasked to make the application more resilient to periodic spikes in read request rates.
- () Which of the following solutions would you recommend for the given use-case? (Select two)
- () Correct selection
- () Use Amazon Aurora Replica
- () Use AWS Direct Connect
- () Use AWS Shield
- () Use Amazon CloudFront distribution in front of the Application Load Balancer
- () Use AWS Global Accelerator
- () Correct options:
- () You can use Amazon Aurora replicas and Amazon CloudFront distribution to make the application more resilient to spikes in request rates.

**Answer:**
Correct Answer: **Define an S3 Lifecycle policy that transitions datasets to S3 Standard-Infrequent Access (S3 Standard-IA) 30 days after creation and schedules the deletion of each object exactly 4 years after its creation**

---

## Question 186

**Q:** Which of the following solutions would you recommend for the given use-case? (Select two)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) Use Amazon Aurora Replica
- (C) Use AWS Direct Connect
- (D) Use AWS Shield
- (E) Use Amazon CloudFront distribution in front of the Application Load Balancer
- (F) Use AWS Global Accelerator
- (G) Correct options:
- (H) You can use Amazon Aurora replicas and Amazon CloudFront distribution to make the application more resilient to spikes in request rates.
- (I) Amazon CloudFront offers an origin failover feature to help support your data resiliency needs. Amazon CloudFront is a global service that delivers your content through a worldwide network of data centers called edge locations or points of presence (POPs). If your content is not already cached in an edge location, Amazon CloudFront retrieves it from an origin that you've identified as the source for the definitive version of the content.
- (J) Incorrect options:
- () Use AWS Shield - AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS. AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency. There are two tiers of AWS Shield - Standard and Advanced. AWS Shield cannot be used to improve application resiliency to handle spikes in traffic.
- () References:
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/disaster-recovery-resiliency.html
- () https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Replication.html
- () https://aws.amazon.com/global-accelerator/faqs/
- () https://docs.aws.amazon.com/global-accelerator/latest/dg/disaster-recovery-resiliency.html
- () A biotechnology company has multiple High Performance Computing (HPC) workflows that quickly and accurately process and analyze genomes for hereditary diseases. The company is looking to migrate these workflows from their on-premises infrastructure to AWS Cloud.

**Answer:**
Correct Answer: **Correct selection**

---

## Question 187

**Q:** As a solutions architect, which of the following networking components would you recommend on the Amazon EC2 instances running these HPC workflows?

**Options:**
- (A) Elastic Network Interface (ENI)
- (B) Elastic Fabric Adapter (EFA)
- (C) Elastic Network Adapter (ENA)
- (D) Elastic IP Address (EIP)
- (E) Correct option:
- (F) How Elastic Fabric Adapter Works:
- (G) via - https://aws.amazon.com/hpc/efa/
- (H) Incorrect options:
- (I) Elastic Network Interface (ENI) - An Elastic Network Interface (ENI) is a logical networking component in a VPC that represents a virtual network card. You can create a network interface, attach it to an instance, detach it from an instance, and attach it to another instance. The ENI is the simplest networking component available on AWS and is insufficient for HPC workflows.
- (J) Elastic IP Address (EIP) - An Elastic IP address (EIP) is a static IPv4 address associated with your AWS account. An Elastic IP address is a public IPv4 address, which is reachable from the internet. It is not a networking device that can be used to facilitate HPC workflows.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/efa.html
- () https://aws.amazon.com/hpc/efa/
- () A startup wants to create a highly available architecture for its multi-tier application. Currently, the startup manages a single Amazon EC2 instance along with a single Amazon RDS MySQL DB instance. The startup has hired you as an AWS Certified Solutions Architect - Associate to build a solution that meets these requirements while minimizing the underlying infrastructure maintenance effort.
- () What will you recommend?
- **() Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances across two Availability Zones. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up Amazon RDS MySQL DB in a multi-AZ configuration** [CORRECT]
- () Provision a second Amazon EC2 instance in another Availability Zone. Provision a second Amazon RDS MySQL DB in another Availabililty Zone. Leverage Amazon Route 53 for equal distribution of incoming traffic to the Amazon EC2 instances. Use a custom script to sync data across the two MySQL DBs
- () Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances in a single Availability Zone. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up Amazon RDS MySQL DB in a multi-AZ configuration
- () Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances across two Availability Zones. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up a read replica of the Amazon RDS MySQL DB in another Availability Zone
- () Amazon EC2 Auto Scaling is a fully managed service designed to launch or terminate Amazon EC2 instances automatically to help ensure you have the correct number of Amazon EC2 instances available to handle the load for your application.
- () via - https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () Application Load Balancer automatically distributes your incoming traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses, in one or more Availability Zones. It monitors the health of its registered targets, and routes traffic only to the healthy targets.
- () via - https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- () In a multi-AZ deployment, Amazon RDS automatically provisions and maintains a synchronous “standby” replica in a different Availability Zone. Updates to your DB Instance are synchronously replicated across Availability Zones to the standby to keep both in sync and protect your latest database updates against DB instance failure.
- () via - https://aws.amazon.com/rds/features/multi-az/
- () To create a highly available architecture for the given use case, you need to set up an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances across two Availability Zones and then point the Application Load Balancer to the target group having the Amazon EC2 instances.
- () Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances across two Availability Zones. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up a read replica of the Amazon RDS MySQL DB in another Availability Zone - A read replica cannot be used to enhance the availability of an Amazon RDS MySQL DB. You must use the multi-AZ configuration of Amazon RDS MySQL for this use case.
- () Provision a second Amazon EC2 instance in another Availability Zone. Provision a second Amazon RDS MySQL DB in another Availabililty Zone. Leverage Amazon Route 53 for equal distribution of incoming traffic to the Amazon EC2 instances. Use a custom script to sync data across the two MySQL DBs - This option has been added as a distractor. It requires significant monitoring and development effort to keep the Amazon EC2 instances highly available as well as keep the MySQL DBs in sync.
- () https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html
- () https://aws.amazon.com/rds/features/multi-az/
- () A digital media streaming company wants to use Amazon CloudFront to distribute its content only to its service subscribers. As a solutions architect, which of the following solutions would you suggest to deliver restricted content to the bona fide end users? (Select two)
- () Require HTTPS for communication between Amazon CloudFront and your S3 origin

**Answer:**
Correct Answer: **Create an Auto-Scaling group with a desired capacity of a total of two Amazon EC2 instances across two Availability Zones. Configure an Application Load Balancer having a target group of these Amazon EC2 instances. Set up Amazon RDS MySQL DB in a multi-AZ configuration**

---

## Question 188

**Q:** A digital media streaming company wants to use Amazon CloudFront to distribute its content only to its service subscribers. As a solutions architect, which of the following solutions would you suggest to deliver restricted content to the bona fide end users? (Select two)

**Options:**
- **(A) Require HTTPS for communication between Amazon CloudFront and your S3 origin** [CORRECT]
- (B) Forward HTTPS requests to the origin server by using the ECDSA or RSA ciphers
- (C) Require HTTPS for communication between Amazon CloudFront and your custom origin
- (D) Correct selection
- (E) Use Amazon CloudFront signed URLs
- (F) Use Amazon CloudFront signed cookies
- (G) Correct options:
- (H) Many companies that distribute content over the internet want to restrict access to documents, business data, media streams, or content that is intended for selected users, for example, users who have paid a fee.
- (I) To securely serve this private content by using Amazon CloudFront, you can do the following:
- (J) Require that your users access your private content by using special Amazon CloudFront signed URLs or signed cookies.
- () A signed URL includes additional information, for example, expiration date and time, that gives you more control over access to your content. So this is a correct option.
- () Amazon CloudFront signed cookies allow you to control who can access your content when you don't want to change your current URLs or when you want to provide access to multiple restricted files, for example, all of the files in the subscribers' area of a website. So this is also a correct option.
- () Incorrect options:
- () Requiring HTTPS for communication between Amazon CloudFront and your custom origin (or S3 origin) only enables secure access to the underlying content. You cannot use HTTPS to restrict access to your private content. So both these options are incorrect.
- () Forward HTTPS requests to the origin server by using the ECDSA or RSA ciphers - This option is just added as a distractor. You cannot use HTTPS to restrict access to your private content.
- () Reference:
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-urls.html
- () https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-signed-cookies.html
- () A company uses Amazon DynamoDB as a data store for various kinds of customer data, such as user profiles, user events, clicks, and visited links. Some of these use-cases require a high request rate (millions of requests per second), low predictable latency, and reliability. The company now wants to add a caching layer to support high read volumes.
- () As a solutions architect, which of the following AWS services would you recommend as a caching layer for this use-case? (Select two)
- () Amazon ElastiCache
- () Amazon DynamoDB Accelerator (DAX)
- () Amazon Redshift
- () Amazon OpenSearch Service
- () Amazon Relational Database Service (Amazon RDS)
- () Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second. DAX does all the heavy lifting required to add in-memory acceleration to your DynamoDB tables, without requiring developers to manage cache invalidation, data population, or cluster management. Therefore, this is a correct option.
- () DAX Overview:
- () via - https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.concepts.html
- () Amazon ElastiCache for Memcached is an ideal front-end for data stores like Amazon RDS or Amazon DynamoDB, providing a high-performance middle tier for applications with extremely high request rates and/or low latency requirements. Therefore, this is also a correct option.
- () Amazon Relational Database Service (Amazon RDS) - Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching, and backups. Amazon RDS cannot be used as a caching layer for Amazon DynamoDB.
- () Amazon OpenSearch Service - Amazon OpenSearch Service is a managed service that makes it easy for you to perform interactive log analytics, real-time application monitoring, website search, and more. OpenSearch is an open source, distributed search and analytics suite derived from Elasticsearch. It cannot be used as a caching layer for Amazon DynamoDB.
- () Amazon Redshift - Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis. It cannot be used as a caching layer for Amazon DynamoDB.
- () References:
- () https://aws.amazon.com/dynamodb/dax/
- () https://aws.amazon.com/elasticache/faqs/
- () Which combination of savings plans will satisfy these requirements? (Select two)

**Answer:**
Correct Answer: **Require HTTPS for communication between Amazon CloudFront and your S3 origin**

---

## Question 189

**Q:** As a solutions architect, which of the following AWS services would you recommend as a caching layer for this use-case? (Select two)

**Options:**
- (A) Correct selection
- (B) Amazon ElastiCache
- (C) Amazon DynamoDB Accelerator (DAX)
- (D) Amazon Redshift
- (E) Amazon OpenSearch Service
- (F) Amazon Relational Database Service (Amazon RDS)
- (G) Correct options:
- (H) Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for DynamoDB that delivers up to a 10x performance improvement – from milliseconds to microseconds – even at millions of requests per second. DAX does all the heavy lifting required to add in-memory acceleration to your DynamoDB tables, without requiring developers to manage cache invalidation, data population, or cluster management. Therefore, this is a correct option.
- (I) DAX Overview:
- (J) via - https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.concepts.html
- () Amazon ElastiCache for Memcached is an ideal front-end for data stores like Amazon RDS or Amazon DynamoDB, providing a high-performance middle tier for applications with extremely high request rates and/or low latency requirements. Therefore, this is also a correct option.
- () Incorrect options:
- () Amazon Relational Database Service (Amazon RDS) - Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching, and backups. Amazon RDS cannot be used as a caching layer for Amazon DynamoDB.
- () Amazon OpenSearch Service - Amazon OpenSearch Service is a managed service that makes it easy for you to perform interactive log analytics, real-time application monitoring, website search, and more. OpenSearch is an open source, distributed search and analytics suite derived from Elasticsearch. It cannot be used as a caching layer for Amazon DynamoDB.
- () Amazon Redshift - Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis. It cannot be used as a caching layer for Amazon DynamoDB.
- () References:
- () https://aws.amazon.com/dynamodb/dax/
- () https://aws.amazon.com/elasticache/faqs/
- () Which combination of savings plans will satisfy these requirements? (Select two)
- () Purchase a Compute Savings Plan that provides cost savings for usage across EC2, Fargate, and Lambda services
- () Purchase a SageMaker Savings Plan that applies discounted pricing to SageMaker training, inference, and notebook instances
- () Purchase an EC2 Instance Savings Plan that covers EC2 and containerized tasks on Amazon ECS running with Fargate launch type
- () Create a Reserved Instance for each EC2 instance and subscribe to AWS Support to monitor Reserved Instance utilization monthly
- () Subscribe to a hybrid deployment discount plan that includes discounts for both AWS and on-premises Kubernetes workloads
- () Create a Reserved Instance for each EC2 instance and subscribe to AWS Support to monitor Reserved Instance utilization monthly - While Reserved Instances can offer discounts for EC2, they are less flexible than Savings Plans and do not cover services like Fargate, Lambda, or SageMaker. Additionally, subscribing to AWS Support does not contribute to cost savings.
- () Subscribe to a hybrid deployment discount plan that includes discounts for both AWS and on-premises Kubernetes workloads - No such hybrid deployment savings plan currently exists that combines AWS native compute resources with on-premises services. This option is not technically valid and does not address the company's AWS-only workload requirements.
- () Purchase an EC2 Instance Savings Plan that covers EC2 and containerized tasks on Amazon ECS running with Fargate launch type - EC2 Instance Savings Plans apply only to EC2 instance families and do not apply to Fargate workloads. Fargate usage requires Compute Savings Plans for cost optimization.
- () https://docs.aws.amazon.com/savingsplans/latest/userguide/what-is-savings-plans.html
- () https://aws.amazon.com/savingsplans/ml-pricing/
- () Your application is deployed on Amazon EC2 instances fronted by an Application Load Balancer. Recently, your infrastructure has come under attack. Attackers perform over 100 requests per second, while your normal users only make about 5 requests per second.
- () How can you efficiently prevent attackers from overwhelming your application?
- () Use AWS Shield Advanced and setup a rate-based rule
- **() Use an AWS Web Application Firewall (AWS WAF) and setup a rate-based rule** [CORRECT]
- () Configure Sticky Sessions on the Application Load Balancer
- () Define a network access control list (network ACL) on your Application Load Balancer

**Answer:**
Correct Answer: **Use an AWS Web Application Firewall (AWS WAF) and setup a rate-based rule**

---

## Question 190

**Q:** Which combination of savings plans will satisfy these requirements? (Select two)

**Options:**
- (A) Correct selection
- (B) Purchase a Compute Savings Plan that provides cost savings for usage across EC2, Fargate, and Lambda services
- (C) Purchase a SageMaker Savings Plan that applies discounted pricing to SageMaker training, inference, and notebook instances
- (D) Purchase an EC2 Instance Savings Plan that covers EC2 and containerized tasks on Amazon ECS running with Fargate launch type
- (E) Create a Reserved Instance for each EC2 instance and subscribe to AWS Support to monitor Reserved Instance utilization monthly
- (F) Subscribe to a hybrid deployment discount plan that includes discounts for both AWS and on-premises Kubernetes workloads
- (G) Correct options:
- (H) Incorrect options:
- (I) Create a Reserved Instance for each EC2 instance and subscribe to AWS Support to monitor Reserved Instance utilization monthly - While Reserved Instances can offer discounts for EC2, they are less flexible than Savings Plans and do not cover services like Fargate, Lambda, or SageMaker. Additionally, subscribing to AWS Support does not contribute to cost savings.
- (J) Subscribe to a hybrid deployment discount plan that includes discounts for both AWS and on-premises Kubernetes workloads - No such hybrid deployment savings plan currently exists that combines AWS native compute resources with on-premises services. This option is not technically valid and does not address the company's AWS-only workload requirements.
- () Purchase an EC2 Instance Savings Plan that covers EC2 and containerized tasks on Amazon ECS running with Fargate launch type - EC2 Instance Savings Plans apply only to EC2 instance families and do not apply to Fargate workloads. Fargate usage requires Compute Savings Plans for cost optimization.
- () References:
- () https://docs.aws.amazon.com/savingsplans/latest/userguide/what-is-savings-plans.html
- () https://aws.amazon.com/savingsplans/ml-pricing/
- () Your application is deployed on Amazon EC2 instances fronted by an Application Load Balancer. Recently, your infrastructure has come under attack. Attackers perform over 100 requests per second, while your normal users only make about 5 requests per second.
- () How can you efficiently prevent attackers from overwhelming your application?
- () Use AWS Shield Advanced and setup a rate-based rule
- () Use an AWS Web Application Firewall (AWS WAF) and setup a rate-based rule
- () Configure Sticky Sessions on the Application Load Balancer
- () Define a network access control list (network ACL) on your Application Load Balancer
- () Correct option:
- () AWS Web Application Firewall (AWS WAF) is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that block common attack patterns, such as SQL injection or cross-site scripting, and rules that filter out specific traffic patterns you define.
- () The correct answer is to use WAF (which has integration on top of your ALB) and define a rate-based rule.
- () Sticky Sessions on your Application Load Balancer is a distractor here. Sticky sessions are a mechanism to route requests from the same client to the same target. Application Load Balancer supports sticky sessions using load balancer generated cookies. If you enable sticky sessions, the same target receives the request and can use the cookie to recover the session context.
- () Define a network access control list (network ACL) on your Application Load Balancer - A network access control list (network ACL) does not work, as this only helps to block specific IPs. On top of things, network access control list (network ACL) is defined at the subnet level, and not for an Application Load Balancer.
- () Use AWS Shield Advanced and setup a rate-based rule - AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS. AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency, so there is no need to engage AWS Support to benefit from DDoS protection. There are two tiers of AWS Shield - Standard and Advanced.
- () AWS Shield Advanced provides enhanced resource-specific detection and employs advanced mitigation and routing techniques for sophisticated or larger attacks.
- () AWS Shield Advanced will give you DDoS protection overall, and you cannot set up rate-based rules in Shield.
- () https://aws.amazon.com/waf/
- () https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-rate-based.html
- () https://aws.amazon.com/shield/
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html#sticky-sessions
- () A healthcare analytics firm operates a backend application within a private subnet of its VPC. The application is fronted by an Application Load Balancer (ALB) and accesses Amazon S3 to store medical reports. The VPC includes both a NAT gateway and an internet gateway, but the company's strict compliance policy prohibits any data traffic from traversing the internet. The team must redesign the architecture to comply with the security policy and improve cost-efficiency.
- () Which solution best satisfies these requirements in the most cost-effective manner?
- **() Create a gateway VPC endpoint for Amazon S3 and update the route table for the private subnet to direct S3 traffic through the endpoint** [CORRECT]
- () Create an S3 interface VPC endpoint and modify the security group to allow access from the application’s private subnet. Route all S3 traffic through the interface endpoint
- () Modify the S3 bucket policy to allow requests only from the Elastic IP address associated with the NAT gateway
- () Create a VPC peering connection with another VPC that has direct access to S3. Forward the S3 API requests through the peered VPC using proxy EC2 instances

**Answer:**
Correct Answer: **Create a gateway VPC endpoint for Amazon S3 and update the route table for the private subnet to direct S3 traffic through the endpoint**

---

## Question 191

**Q:** How can you efficiently prevent attackers from overwhelming your application?

**Options:**
- (A) Use AWS Shield Advanced and setup a rate-based rule
- (B) Use an AWS Web Application Firewall (AWS WAF) and setup a rate-based rule
- (C) Configure Sticky Sessions on the Application Load Balancer
- (D) Define a network access control list (network ACL) on your Application Load Balancer
- (E) Correct option:
- (F) AWS Web Application Firewall (AWS WAF) is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that block common attack patterns, such as SQL injection or cross-site scripting, and rules that filter out specific traffic patterns you define.
- (G) The correct answer is to use WAF (which has integration on top of your ALB) and define a rate-based rule.
- (H) Incorrect options:
- (I) Sticky Sessions on your Application Load Balancer is a distractor here. Sticky sessions are a mechanism to route requests from the same client to the same target. Application Load Balancer supports sticky sessions using load balancer generated cookies. If you enable sticky sessions, the same target receives the request and can use the cookie to recover the session context.
- (J) Define a network access control list (network ACL) on your Application Load Balancer - A network access control list (network ACL) does not work, as this only helps to block specific IPs. On top of things, network access control list (network ACL) is defined at the subnet level, and not for an Application Load Balancer.
- () Use AWS Shield Advanced and setup a rate-based rule - AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS. AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency, so there is no need to engage AWS Support to benefit from DDoS protection. There are two tiers of AWS Shield - Standard and Advanced.
- () AWS Shield Advanced provides enhanced resource-specific detection and employs advanced mitigation and routing techniques for sophisticated or larger attacks.
- () AWS Shield Advanced will give you DDoS protection overall, and you cannot set up rate-based rules in Shield.
- () References:
- () https://aws.amazon.com/waf/
- () https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-rate-based.html
- () https://aws.amazon.com/shield/
- () https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html#sticky-sessions
- () A healthcare analytics firm operates a backend application within a private subnet of its VPC. The application is fronted by an Application Load Balancer (ALB) and accesses Amazon S3 to store medical reports. The VPC includes both a NAT gateway and an internet gateway, but the company's strict compliance policy prohibits any data traffic from traversing the internet. The team must redesign the architecture to comply with the security policy and improve cost-efficiency.
- () Which solution best satisfies these requirements in the most cost-effective manner?
- () Create a gateway VPC endpoint for Amazon S3 and update the route table for the private subnet to direct S3 traffic through the endpoint
- () Create an S3 interface VPC endpoint and modify the security group to allow access from the application’s private subnet. Route all S3 traffic through the interface endpoint
- () Modify the S3 bucket policy to allow requests only from the Elastic IP address associated with the NAT gateway
- () Create a VPC peering connection with another VPC that has direct access to S3. Forward the S3 API requests through the peered VPC using proxy EC2 instances
- () Correct options:
- () via - https://docs.aws.amazon.com/vpc/latest/privatelink/gateway-endpoints.html
- () via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/privatelink-interface-endpoints.html#types-of-vpc-endpoints-for-s3
- () Modify the S3 bucket policy to allow requests only from the Elastic IP address associated with the NAT gateway - While this restricts access from specific IPs, it still causes S3 API calls to traverse the public internet via the NAT gateway, violating the security policy that prohibits internet-based traffic. Furthermore, it incurs additional NAT gateway data processing costs. This approach may restrict access, but does not solve the core compliance issue.
- () https://docs.aws.amazon.com/vpc/latest/privatelink/gateway-endpoints.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/privatelink-interface-endpoints.html#types-of-vpc-endpoints-for-s3
- () https://docs.aws.amazon.com/vpc/latest/privatelink/concepts.html
- () A company is deploying a publicly accessible web application. To accomplish this, the engineering team has designed the VPC with a public subnet and a private subnet. The application will be hosted on several Amazon EC2 instances in an Auto Scaling group. The team also wants Transport Layer Security (TLS) termination to be offloaded from the Amazon EC2 instances.
- () Which solution should a solutions architect implement to address these requirements in the most secure manner?
- () Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
- () Set up a Network Load Balancer in the private subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
- **() Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer** [CORRECT]

**Answer:**
Correct Answer: **Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer**

---

## Question 192

**Q:** Which solution best satisfies these requirements in the most cost-effective manner?

**Options:**
- (A) Create a gateway VPC endpoint for Amazon S3 and update the route table for the private subnet to direct S3 traffic through the endpoint
- (B) Create an S3 interface VPC endpoint and modify the security group to allow access from the application’s private subnet. Route all S3 traffic through the interface endpoint
- (C) Modify the S3 bucket policy to allow requests only from the Elastic IP address associated with the NAT gateway
- (D) Create a VPC peering connection with another VPC that has direct access to S3. Forward the S3 API requests through the peered VPC using proxy EC2 instances
- (E) Correct options:
- (F) via - https://docs.aws.amazon.com/vpc/latest/privatelink/gateway-endpoints.html
- (G) Incorrect options:
- (H) via - https://docs.aws.amazon.com/AmazonS3/latest/userguide/privatelink-interface-endpoints.html#types-of-vpc-endpoints-for-s3
- (I) Modify the S3 bucket policy to allow requests only from the Elastic IP address associated with the NAT gateway - While this restricts access from specific IPs, it still causes S3 API calls to traverse the public internet via the NAT gateway, violating the security policy that prohibits internet-based traffic. Furthermore, it incurs additional NAT gateway data processing costs. This approach may restrict access, but does not solve the core compliance issue.
- (J) References:
- () https://docs.aws.amazon.com/vpc/latest/privatelink/gateway-endpoints.html
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/privatelink-interface-endpoints.html#types-of-vpc-endpoints-for-s3
- () https://docs.aws.amazon.com/vpc/latest/privatelink/concepts.html
- () A company is deploying a publicly accessible web application. To accomplish this, the engineering team has designed the VPC with a public subnet and a private subnet. The application will be hosted on several Amazon EC2 instances in an Auto Scaling group. The team also wants Transport Layer Security (TLS) termination to be offloaded from the Amazon EC2 instances.
- () Which solution should a solutions architect implement to address these requirements in the most secure manner?
- () Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
- () Set up a Network Load Balancer in the private subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
- **() Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer** [CORRECT]
- () Set up a Network Load Balancer in the private subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer
- () Correct option:
- () A load balancer serves as the single point of contact for clients. The load balancer distributes incoming traffic across multiple targets, such as Amazon EC2 instances. This increases the availability of your application. You add one or more listeners to your load balancer.
- () With a Network Load Balancer, you can offload the decryption/encryption of Transport Layer Security (TLS) traffic from your application servers to the Network Load Balancer, which helps you optimize the performance of your backend application servers while keeping your workloads secure. Additionally, Network Load Balancers preserve the source IP of the clients to the back-end applications, while terminating Transport Layer Security (TLS) on the load balancer.
- () An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
- () The NLB has to be accessible over the internet and hence has to be in a public subnet and will act as a single point-of-contact for all incoming traffic. NLB will forward the incoming traffic to the Amazon EC2 instances managed by the ASG in the private subnet.
- () Exam Alert:
- () You should note that the Application Load Balancer also supports Transport Layer Security (TLS) offloading. The Classic Load Balancer supports SSL offloading.
- () Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer - The Auto Scaling group with its target EC2 instances should be in the private subnet to avoid access to EC2 instances over the public internet. Having EC2 instances in the public subnet would weaken the security posture of the application. Hence, this option is incorrect.
- () NLB should be in the public subnet as it represents the internet-facing component of the web tier. Therefore, both these options are incorrect.
- () Reference:
- () https://aws.amazon.com/blogs/aws/new-tls-termination-for-network-load-balancers/
- () A company is experiencing stability issues with their cluster of self-managed RabbitMQ message brokers and the company now wants to explore an alternate solution on AWS.

**Answer:**
Correct Answer: **Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer**

---

## Question 193

**Q:** Which solution should a solutions architect implement to address these requirements in the most secure manner?

**Options:**
- (A) Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
- (B) Set up a Network Load Balancer in the private subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer
- **(C) Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer** [CORRECT]
- (D) Set up a Network Load Balancer in the private subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer
- (E) Correct option:
- (F) A load balancer serves as the single point of contact for clients. The load balancer distributes incoming traffic across multiple targets, such as Amazon EC2 instances. This increases the availability of your application. You add one or more listeners to your load balancer.
- (G) With a Network Load Balancer, you can offload the decryption/encryption of Transport Layer Security (TLS) traffic from your application servers to the Network Load Balancer, which helps you optimize the performance of your backend application servers while keeping your workloads secure. Additionally, Network Load Balancers preserve the source IP of the clients to the back-end applications, while terminating Transport Layer Security (TLS) on the load balancer.
- (H) An Auto Scaling group contains a collection of Amazon EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management. An Auto Scaling group also enables you to use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.
- (I) The NLB has to be accessible over the internet and hence has to be in a public subnet and will act as a single point-of-contact for all incoming traffic. NLB will forward the incoming traffic to the Amazon EC2 instances managed by the ASG in the private subnet.
- (J) Exam Alert:
- () You should note that the Application Load Balancer also supports Transport Layer Security (TLS) offloading. The Classic Load Balancer supports SSL offloading.
- () Incorrect options:
- () Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the public subnet and associate it with the Network Load Balancer - The Auto Scaling group with its target EC2 instances should be in the private subnet to avoid access to EC2 instances over the public internet. Having EC2 instances in the public subnet would weaken the security posture of the application. Hence, this option is incorrect.
- () NLB should be in the public subnet as it represents the internet-facing component of the web tier. Therefore, both these options are incorrect.
- () Reference:
- () https://aws.amazon.com/blogs/aws/new-tls-termination-for-network-load-balancers/
- () A company is experiencing stability issues with their cluster of self-managed RabbitMQ message brokers and the company now wants to explore an alternate solution on AWS.

**Answer:**
Correct Answer: **Set up a Network Load Balancer in the public subnet. Create an Auto Scaling group in the private subnet and associate it with the Network Load Balancer**

---

## Question 194

**Q:** As a solutions architect, which of the following AWS services would you recommend that can provide support for quick and easy migration from RabbitMQ?

**Options:**
- (A) Amazon MQ
- (B) Amazon Simple Notification Service (Amazon SNS)
- (C) Amazon Simple Queue Service (Amazon SQS) Standard
- (D) Amazon SQS FIFO (First-In-First-Out)
- (E) Correct option:
- (F) Incorrect options:
- (G) Amazon Simple Notification Service (Amazon SNS) - Amazon Simple Notification Service (Amazon SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging. SNS does not provide support for migration from RabbitMQ as its a fully managed pub/sub messaging service. Hence this option is incorrect.
- (H) Amazon SQS FIFO (First-In-First-Out) - Amazon SQS FIFO (First-In-First-Out) has all the capabilities of the standard queue. They are used when the order of operations and events is critical, or where duplicates can't be tolerated. SQS FIFO does not provide support for migration from RabbitMQ. Hence this option is incorrect.
- (I) Reference:
- (J) https://aws.amazon.com/amazon-mq/
- () https://aws.amazon.com/blogs/compute/migrating-from-rabbitmq-to-amazon-mq/
- () A global financial services provider operates data analytics workloads across multiple AWS Regions. The company stores regulated datasets in Amazon S3 buckets and requires visibility into security and compliance configurations. As part of a new audit initiative, the compliance team must identify all S3 buckets across the environment that do not have versioning enabled. The solution must scale across all Regions and accounts with minimal manual intervention.
- () Which solution will meet these requirements with the LEAST operational overhead?
- () Configure an AWS CloudTrail trail across all Regions. Create an Amazon EventBridge rule that filters for PutBucketVersioning and DeleteBucketVersioning API calls. Trigger an AWS Lambda function to analyze the bucket configurations and generate a report of unversioned buckets
- () Create a centralized Amazon S3 Multi-Region Access Point for all buckets. Use this access point to perform versioning checks programmatically by inspecting objects' metadata from each bucket
- () Enable Amazon S3 Storage Lens with advanced metrics and recommendations. Use the per-bucket dashboard to filter and view versioning status across Regions and identify all buckets that do not have versioning enabled
- () Enable IAM Access Analyzer for all Regions. Review the analyzer reports to identify S3 buckets without versioning enabled and configure IAM policies to restrict access to such buckets
- () Enable IAM Access Analyzer for all Regions. Review the analyzer reports to identify S3 buckets without versioning enabled and configure IAM policies to restrict access to such buckets - IAM Access Analyzer is used to evaluate resource sharing and access configurations. It does not check for or report on bucket-level settings such as versioning.
- () Create a centralized Amazon S3 Multi-Region Access Point for all buckets. Use this access point to perform versioning checks programmatically by inspecting objects' metadata from each bucket - S3 Multi-Region Access Points simplify cross-Region data access but do not provide visibility into bucket configuration or versioning status. It is not designed for compliance checks.
- () References:
- () https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
- () https://aws.amazon.com/s3/storage-lens/
- () A systems administration team has a requirement to run certain custom scripts only once during the launch of the Amazon Elastic Compute Cloud (Amazon EC2) instances that host their application.
- () Which of the following represents the best way of configuring a solution for this requirement with minimal effort?
- () Use AWS CLI to run the user data scripts only once while launching the instance
- () Run the custom scripts as instance metadata scripts on the Amazon EC2 instances
- () Update Amazon EC2 instance configuration to ensure that the custom scripts, added as user data scripts, are run only during the boot process
- **() Run the custom scripts as user data scripts on the Amazon EC2 instances** [CORRECT]
- () When you launch an instance in Amazon EC2, you have the option of passing user data to the instance that can be used to perform common automated configuration tasks and even run scripts after the instance starts. You can pass two types of user data to Amazon EC2: shell scripts and cloud-init directives.
- () By default, user data scripts and cloud-init directives run only during the boot cycle when you first launch an instance. Hence, no extra configuration is needed, apart from including the custom scripts in user data scripts.
- () Update Amazon EC2 instance configuration to ensure that the custom scripts, added as user data scripts, are run only during the boot process - You can update your configuration to ensure that your user data scripts and cloud-init directives run every time you restart your instance. By default, the scripts are run, only once during the boot process while first launching the instance.
- () Run the custom scripts as instance metadata scripts on the Amazon EC2 instances- Instance metadata is data about your instance that you can use to configure or manage the running instance. Metadata cannot be used to run custom scripts.
- () Use AWS CLI to run the user data scripts only once while launching the instance - This statement is incorrect and used only as a distractor.
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html

**Answer:**
Correct Answer: **Run the custom scripts as user data scripts on the Amazon EC2 instances**

---

## Question 195

**Q:** Which of the following represents the best way of configuring a solution for this requirement with minimal effort?

**Options:**
- (A) Use AWS CLI to run the user data scripts only once while launching the instance
- (B) Run the custom scripts as instance metadata scripts on the Amazon EC2 instances
- (C) Update Amazon EC2 instance configuration to ensure that the custom scripts, added as user data scripts, are run only during the boot process
- **(D) Run the custom scripts as user data scripts on the Amazon EC2 instances** [CORRECT]
- (E) Correct option:
- (F) When you launch an instance in Amazon EC2, you have the option of passing user data to the instance that can be used to perform common automated configuration tasks and even run scripts after the instance starts. You can pass two types of user data to Amazon EC2: shell scripts and cloud-init directives.
- (G) By default, user data scripts and cloud-init directives run only during the boot cycle when you first launch an instance. Hence, no extra configuration is needed, apart from including the custom scripts in user data scripts.
- (H) Incorrect options:
- (I) Update Amazon EC2 instance configuration to ensure that the custom scripts, added as user data scripts, are run only during the boot process - You can update your configuration to ensure that your user data scripts and cloud-init directives run every time you restart your instance. By default, the scripts are run, only once during the boot process while first launching the instance.
- (J) Run the custom scripts as instance metadata scripts on the Amazon EC2 instances- Instance metadata is data about your instance that you can use to configure or manage the running instance. Metadata cannot be used to run custom scripts.
- () Use AWS CLI to run the user data scripts only once while launching the instance - This statement is incorrect and used only as a distractor.
- () References:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html
- () The engineering team at a retail company is planning to migrate to AWS Cloud from the on-premises data center. The team is evaluating Amazon Relational Database Service (Amazon RDS) as the database tier for its flagship application. The team has hired you as an AWS Certified Solutions Architect Associate to advise on Amazon RDS Multi-AZ capabilities.
- () Which of the following would you identify as correct for Amazon RDS Multi-AZ? (Select two)
- () To enhance read scalability, a Multi-AZ standby instance can be used to serve read requests
- () Correct selection
- () Amazon RDS automatically initiates a failover to the standby, in case primary database fails for any reason
- () Updates to your database Instance are asynchronously replicated across the Availability Zone to the standby in order to keep both in sync
- () For automated backups, I/O activity is suspended on your primary database since backups are not taken from standby database
- () Amazon RDS applies operating system updates by performing maintenance on the standby, then promoting the standby to primary and finally performing maintenance on the old primary, which becomes the new standby
- () Correct options:
- () Running a DB instance as a Multi-AZ deployment can further reduce the impact of a maintenance event because Amazon RDS applies operating system updates by following these steps:
- () Perform maintenance on the standby.
- () Promote the standby to primary.
- () Perform maintenance on the old primary, which becomes the new standby.
- () When you modify the database engine for your DB instance in a Multi-AZ deployment, then Amazon RDS upgrades both the primary and secondary DB instances at the same time. In this case, the database engine for the entire Multi-AZ deployment is shut down during the upgrade.
- () You also benefit from enhanced database availability when running your DB instance as a Multi-AZ deployment. If an Availability Zone failure or DB instance failure occurs, your availability impact is limited to the time automatic failover takes to complete.
- () Another implied benefit of running your DB instance as a Multi-AZ deployment is that DB instance failover is automatic and requires no administration. In an Amazon RDS context, this means you are not required to monitor DB instance events and initiate manual DB instance recovery in the event of an Availability Zone failure or DB instance failure.
- () For automated backups, I/O activity is suspended on your primary database since backups are not taken from standby database - The availability benefits of Multi-AZ also extend to planned maintenance. For example, with automated backups, I/O activity is no longer suspended on your primary during your preferred backup window, since backups are taken from the standby.
- () To enhance read scalability, a Multi-AZ standby instance can be used to serve read requests - A Multi-AZ standby cannot serve read requests. Multi-AZ deployments are designed to provide enhanced database availability and durability, rather than read scaling benefits. As such, the feature uses synchronous replication between primary and standby. AWS implementation makes sure the primary and the standby are constantly in sync, but precludes using the standby for read or write operations.
- () Reference:
- () https://aws.amazon.com/rds/faqs/
- () The engineering team at a multi-national company uses AWS Firewall Manager to centrally configure and manage firewall rules across its accounts and applications using AWS Organizations.
- () Which of the following AWS resources can the AWS Firewall Manager configure rules on? (Select three)
- () AWS Web Application Firewall (AWS WAF)
- () AWS Shield Advanced
- () VPC Route Table
- () VPC Security Group
- () Amazon Inspector

**Answer:**
Correct Answer: **Run the custom scripts as user data scripts on the Amazon EC2 instances**

---

## Question 196

**Q:** Which of the following would you identify as correct for Amazon RDS Multi-AZ? (Select two)

**Options:**
- **(A) To enhance read scalability, a Multi-AZ standby instance can be used to serve read requests** [CORRECT]
- (B) Correct selection
- (C) Amazon RDS automatically initiates a failover to the standby, in case primary database fails for any reason
- (D) Updates to your database Instance are asynchronously replicated across the Availability Zone to the standby in order to keep both in sync
- (E) For automated backups, I/O activity is suspended on your primary database since backups are not taken from standby database
- (F) Amazon RDS applies operating system updates by performing maintenance on the standby, then promoting the standby to primary and finally performing maintenance on the old primary, which becomes the new standby
- (G) Correct options:
- (H) Running a DB instance as a Multi-AZ deployment can further reduce the impact of a maintenance event because Amazon RDS applies operating system updates by following these steps:
- (I) Perform maintenance on the standby.
- (J) Promote the standby to primary.
- () Perform maintenance on the old primary, which becomes the new standby.
- () When you modify the database engine for your DB instance in a Multi-AZ deployment, then Amazon RDS upgrades both the primary and secondary DB instances at the same time. In this case, the database engine for the entire Multi-AZ deployment is shut down during the upgrade.
- () You also benefit from enhanced database availability when running your DB instance as a Multi-AZ deployment. If an Availability Zone failure or DB instance failure occurs, your availability impact is limited to the time automatic failover takes to complete.
- () Another implied benefit of running your DB instance as a Multi-AZ deployment is that DB instance failover is automatic and requires no administration. In an Amazon RDS context, this means you are not required to monitor DB instance events and initiate manual DB instance recovery in the event of an Availability Zone failure or DB instance failure.
- () Incorrect options:
- () For automated backups, I/O activity is suspended on your primary database since backups are not taken from standby database - The availability benefits of Multi-AZ also extend to planned maintenance. For example, with automated backups, I/O activity is no longer suspended on your primary during your preferred backup window, since backups are taken from the standby.
- () To enhance read scalability, a Multi-AZ standby instance can be used to serve read requests - A Multi-AZ standby cannot serve read requests. Multi-AZ deployments are designed to provide enhanced database availability and durability, rather than read scaling benefits. As such, the feature uses synchronous replication between primary and standby. AWS implementation makes sure the primary and the standby are constantly in sync, but precludes using the standby for read or write operations.
- () Reference:
- () https://aws.amazon.com/rds/faqs/
- () The engineering team at a multi-national company uses AWS Firewall Manager to centrally configure and manage firewall rules across its accounts and applications using AWS Organizations.
- () Which of the following AWS resources can the AWS Firewall Manager configure rules on? (Select three)
- () AWS Web Application Firewall (AWS WAF)
- () AWS Shield Advanced
- () VPC Route Table
- () VPC Security Group
- () Amazon Inspector
- () Amazon GuardDuty
- () Using AWS Firewall Manager, you can centrally configure AWS WAF rules, AWS Shield Advanced protection, Amazon Virtual Private Cloud (VPC) security groups, AWS Network Firewalls, and Amazon Route 53 Resolver DNS Firewall rules across accounts and resources in your organization. It does not support Network ACLs as of today.
- () via - https://aws.amazon.com/firewall-manager/faqs/
- () Amazon GuardDuty - Amazon GuardDuty offers threat detection that enables you to continuously monitor and protect your AWS accounts, workloads, and data stored in Amazon S3. Amazon GuardDuty analyzes continuous streams of meta-data generated from your account and network activity found in AWS CloudTrail Events, Amazon VPC Flow Logs, and DNS Logs.
- () How Amazon GuardDuty Works:
- () Amazon Inspector - Amazon Inspector is an automated security assessment service that helps you test the network accessibility of your Amazon EC2 instances and the security state of your applications running on the instances.
- () VPC Route Table - A route table serves as the traffic controller for your virtual private cloud (VPC). Each route table contains a set of rules, called routes, that determine where network traffic from your subnet or gateway is directed.
- () These three options are not in the list of AWS resources supported by AWS Firewall Manager, so these options are incorrect.
- () References:
- () https://aws.amazon.com/firewall-manager/faqs/
- () https://aws.amazon.com/guardduty/

**Answer:**
Correct Answer: **To enhance read scalability, a Multi-AZ standby instance can be used to serve read requests**

---

## Question 197

**Q:** Which of the following AWS resources can the AWS Firewall Manager configure rules on? (Select three)

**Options:**
- **(A) Correct selection** [CORRECT]
- (B) AWS Web Application Firewall (AWS WAF)
- (C) AWS Shield Advanced
- (D) VPC Route Table
- (E) VPC Security Group
- (F) Amazon Inspector
- (G) Amazon GuardDuty
- (H) Correct options:
- (I) Using AWS Firewall Manager, you can centrally configure AWS WAF rules, AWS Shield Advanced protection, Amazon Virtual Private Cloud (VPC) security groups, AWS Network Firewalls, and Amazon Route 53 Resolver DNS Firewall rules across accounts and resources in your organization. It does not support Network ACLs as of today.
- (J) via - https://aws.amazon.com/firewall-manager/faqs/
- () Incorrect options:
- () Amazon GuardDuty - Amazon GuardDuty offers threat detection that enables you to continuously monitor and protect your AWS accounts, workloads, and data stored in Amazon S3. Amazon GuardDuty analyzes continuous streams of meta-data generated from your account and network activity found in AWS CloudTrail Events, Amazon VPC Flow Logs, and DNS Logs.
- () How Amazon GuardDuty Works:
- () Amazon Inspector - Amazon Inspector is an automated security assessment service that helps you test the network accessibility of your Amazon EC2 instances and the security state of your applications running on the instances.
- () VPC Route Table - A route table serves as the traffic controller for your virtual private cloud (VPC). Each route table contains a set of rules, called routes, that determine where network traffic from your subnet or gateway is directed.
- () These three options are not in the list of AWS resources supported by AWS Firewall Manager, so these options are incorrect.
- () References:
- () https://aws.amazon.com/firewall-manager/faqs/
- () https://aws.amazon.com/guardduty/
- () https://aws.amazon.com/inspector/
- () A company's real-time streaming application is running on AWS. As the data is ingested, a job runs on the data and takes 30 minutes to complete. The workload frequently experiences high latency due to large amounts of incoming data. A solutions architect needs to design a scalable and serverless solution to enhance performance.
- () Which combination of steps should the solutions architect take? (Select two)
- () Set up Amazon Kinesis Data Streams to ingest the data
- () Set up AWS Database Migration Service (AWS DMS) to ingest the data
- () Set up AWS Fargate with Amazon ECS to process the data
- () Provision Amazon EC2 instances in an Auto Scaling group to process the data
- () Set up AWS Lambda with AWS Step Functions to process the data
- () AWS Fargate is a serverless compute engine for containers that works with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS). Fargate makes it easy for you to focus on building your applications. Fargate removes the need to provision and manage servers, lets you specify and pay for resources per application, and improves security through application isolation by design.
- () For the given use case, we can use Kinesis Data Streams as the ingestion layer and the containerized ECS application on AWS Fargate as the processing layer. Both these components are serverless and can scale to offer the desired performance.
- () Set up AWS Database Migration Service (AWS DMS) to ingest the data - AWS Database Migration Service helps you migrate databases to AWS quickly and securely. DMS cannot be used for real-time data ingestion. Hence, this option is incorrect.
- () Set up AWS Lambda with AWS Step Functions to process the data - The maximum timeout value for any AWS Lambda function is 15 minutes. When the specified timeout is reached, AWS Lambda terminates the execution of your Lambda function. Since the use case talks about a job that runs for 30 minutes, Lambda is not an option here.
- () Provision Amazon EC2 instances in an Auto Scaling group to process the data - The given requirement is for a serverless solution to process the data. Hence, provisioning an Amazon EC2 instance is clearly not the right solution.
- () Reference:
- () https://aws.amazon.com/blogs/big-data/building-a-scalable-streaming-data-processor-with-amazon-kinesis-data-streams-on-aws-fargate/

**Answer:**
Correct Answer: **Correct selection**

---

## Question 198

**Q:** Which combination of steps should the solutions architect take? (Select two)

**Options:**
- (A) Correct selection
- (B) Set up Amazon Kinesis Data Streams to ingest the data
- (C) Set up AWS Database Migration Service (AWS DMS) to ingest the data
- (D) Set up AWS Fargate with Amazon ECS to process the data
- (E) Provision Amazon EC2 instances in an Auto Scaling group to process the data
- (F) Set up AWS Lambda with AWS Step Functions to process the data
- (G) Correct options:
- (H) AWS Fargate is a serverless compute engine for containers that works with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS). Fargate makes it easy for you to focus on building your applications. Fargate removes the need to provision and manage servers, lets you specify and pay for resources per application, and improves security through application isolation by design.
- (I) For the given use case, we can use Kinesis Data Streams as the ingestion layer and the containerized ECS application on AWS Fargate as the processing layer. Both these components are serverless and can scale to offer the desired performance.
- (J) Incorrect options:
- () Set up AWS Database Migration Service (AWS DMS) to ingest the data - AWS Database Migration Service helps you migrate databases to AWS quickly and securely. DMS cannot be used for real-time data ingestion. Hence, this option is incorrect.
- () Set up AWS Lambda with AWS Step Functions to process the data - The maximum timeout value for any AWS Lambda function is 15 minutes. When the specified timeout is reached, AWS Lambda terminates the execution of your Lambda function. Since the use case talks about a job that runs for 30 minutes, Lambda is not an option here.
- () Provision Amazon EC2 instances in an Auto Scaling group to process the data - The given requirement is for a serverless solution to process the data. Hence, provisioning an Amazon EC2 instance is clearly not the right solution.
- () Reference:
- () https://aws.amazon.com/blogs/big-data/building-a-scalable-streaming-data-processor-with-amazon-kinesis-data-streams-on-aws-fargate/
- () You have deployed a database technology that has a synchronous replication mode to survive disasters in data centers. The database is therefore deployed on two Amazon EC2 instances in two Availability Zones (AZs). The database must be publicly available so you have deployed the Amazon EC2 instances in public subnets. The replication protocol currently uses the Amazon EC2 public IP addresses.
- () What can you do to decrease the replication cost?
- () Create a Private Link between the two Amazon EC2 instances
- () Use the Amazon EC2 instances private IP for the replication
- () Assign elastic IP address (EIP) to the Amazon EC2 instances and use them for the replication
- () Use an Elastic Fabric Adapter (EFA)
- () Correct option:
- () The source of the cost is that traffic between two EC2 instances is going over the public internet, thus incurring high costs. Here, the correct answer is to use Private IP, so that the network remains private, for a minimal cost.
- () Assign elastic IP address (EIP) to the Amazon EC2 instances and use them for the replication - Using Elastic IPs will not solve the problem as the traffic will still be going over the public internet.
- () Create a Private Link between the two Amazon EC2 instances - AWS PrivateLink simplifies the security of data shared with cloud-based applications by eliminating the exposure of data to the public Internet. AWS PrivateLink provides private connectivity between VPCs, AWS services, and on-premises applications, securely on the Amazon network.
- () Use an Elastic Fabric Adapter (EFA) - The Elastic Fabric Adapter (EFA) is a network interface for Amazon EC2 instances that enables customers to run HPC applications requiring high levels of inter-instance communications, like computational fluid dynamics, weather modeling, and reservoir simulation, at scale on AWS. This option is not relevant to the given use-case.
- () References:
- () https://aws.amazon.com/privatelink/
- () https://aws.amazon.com/hpc/efa/
- () An application is hosted on multiple Amazon EC2 instances in the same Availability Zone (AZ). The engineering team wants to set up shared data access for these Amazon EC2 instances using Amazon EBS Multi-Attach volumes.
- () Which Amazon EBS volume type is the correct choice for these Amazon EC2 instances?
- () Cold HDD Amazon EBS volumes
- () Throughput Optimized HDD Amazon EBS volumes
- () General-purpose SSD-based Amazon EBS volumes
- **() Provisioned IOPS SSD Amazon EBS volumes** [CORRECT]
- () Multi-Attach is supported exclusively on Provisioned IOPS SSD volumes.
- () General-purpose SSD-based Amazon EBS volumes - These SSD-backed Amazon EBS volumes provide a balance of price and performance. AWS recommends these volumes for most workloads. These volume types are not supported for Multi-Attach functionality.

**Answer:**
Correct Answer: **Provisioned IOPS SSD Amazon EBS volumes**

---

## Question 199

**Q:** What can you do to decrease the replication cost?

**Options:**
- (A) Create a Private Link between the two Amazon EC2 instances
- (B) Use the Amazon EC2 instances private IP for the replication
- (C) Assign elastic IP address (EIP) to the Amazon EC2 instances and use them for the replication
- (D) Use an Elastic Fabric Adapter (EFA)
- (E) Correct option:
- (F) The source of the cost is that traffic between two EC2 instances is going over the public internet, thus incurring high costs. Here, the correct answer is to use Private IP, so that the network remains private, for a minimal cost.
- (G) Incorrect options:
- (H) Assign elastic IP address (EIP) to the Amazon EC2 instances and use them for the replication - Using Elastic IPs will not solve the problem as the traffic will still be going over the public internet.
- (I) Create a Private Link between the two Amazon EC2 instances - AWS PrivateLink simplifies the security of data shared with cloud-based applications by eliminating the exposure of data to the public Internet. AWS PrivateLink provides private connectivity between VPCs, AWS services, and on-premises applications, securely on the Amazon network.
- (J) Use an Elastic Fabric Adapter (EFA) - The Elastic Fabric Adapter (EFA) is a network interface for Amazon EC2 instances that enables customers to run HPC applications requiring high levels of inter-instance communications, like computational fluid dynamics, weather modeling, and reservoir simulation, at scale on AWS. This option is not relevant to the given use-case.
- () References:
- () https://aws.amazon.com/privatelink/
- () https://aws.amazon.com/hpc/efa/
- () An application is hosted on multiple Amazon EC2 instances in the same Availability Zone (AZ). The engineering team wants to set up shared data access for these Amazon EC2 instances using Amazon EBS Multi-Attach volumes.
- () Which Amazon EBS volume type is the correct choice for these Amazon EC2 instances?
- () Cold HDD Amazon EBS volumes
- () Throughput Optimized HDD Amazon EBS volumes
- () General-purpose SSD-based Amazon EBS volumes
- () Provisioned IOPS SSD Amazon EBS volumes
- () Multi-Attach is supported exclusively on Provisioned IOPS SSD volumes.
- () General-purpose SSD-based Amazon EBS volumes - These SSD-backed Amazon EBS volumes provide a balance of price and performance. AWS recommends these volumes for most workloads. These volume types are not supported for Multi-Attach functionality.
- () Throughput Optimized HDD Amazon EBS volumes - These HDD-backed volumes provide a low-cost HDD designed for frequently accessed, throughput-intensive workloads. These volume types are not supported for Multi-Attach functionality.
- () Cold HDD Amazon EBS volumes - These HDD-backed volumes provide a lowest-cost HDD design for less frequently accessed workloads. These volume types are not supported for Multi-Attach functionality.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes-multi.html
- () A global enterprise maintains a hybrid cloud environment and wants to transfer large volumes of data between its on-premises data center and Amazon S3 for backup and analytics workflows. The company has already established a Direct Connect (DX) connection to AWS and wants to ensure high-bandwidth, low-latency, and secure private connectivity without traversing the public internet. The architecture must be designed to access Amazon S3 directly from on-premises systems using this DX connection.
- () Which configuration should the network engineering team implement to allow direct access to Amazon S3 from the on-premises data center using Direct Connect?
- () Use a Private Virtual Interface (Private VIF) on the Direct Connect connection and create a VPC endpoint to route traffic to S3 over the private network
- **() Provision a Public Virtual Interface (Public VIF) on the Direct Connect connection to access Amazon S3 public IP addresses from the on-premises data center** [CORRECT]
- () Use a Transit Gateway with Direct Connect Gateway to route on-premises traffic through a VPC and then to Amazon S3 using private IP addressing
- () Configure a VPN connection over the public internet to AWS and route S3 traffic through the tunnel instead of using Direct Connect
- () via - https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html
- () Configure a VPN connection over the public internet to AWS and route S3 traffic through the tunnel instead of using Direct Connect - Using a VPN connection over the public internet to route traffic to S3 bypasses the benefits of Direct Connect, such as low latency, dedicated bandwidth, and private connectivity. VPN traffic traverses the public internet and therefore violates the requirements of the given use case.

**Answer:**
Correct Answer: **Provision a Public Virtual Interface (Public VIF) on the Direct Connect connection to access Amazon S3 public IP addresses from the on-premises data center**

---

## Question 200

**Q:** Which Amazon EBS volume type is the correct choice for these Amazon EC2 instances?

**Options:**
- (A) Cold HDD Amazon EBS volumes
- (B) Throughput Optimized HDD Amazon EBS volumes
- (C) General-purpose SSD-based Amazon EBS volumes
- (D) Provisioned IOPS SSD Amazon EBS volumes
- (E) Correct option:
- (F) Multi-Attach is supported exclusively on Provisioned IOPS SSD volumes.
- (G) Incorrect options:
- (H) General-purpose SSD-based Amazon EBS volumes - These SSD-backed Amazon EBS volumes provide a balance of price and performance. AWS recommends these volumes for most workloads. These volume types are not supported for Multi-Attach functionality.
- (I) Throughput Optimized HDD Amazon EBS volumes - These HDD-backed volumes provide a low-cost HDD designed for frequently accessed, throughput-intensive workloads. These volume types are not supported for Multi-Attach functionality.
- (J) Cold HDD Amazon EBS volumes - These HDD-backed volumes provide a lowest-cost HDD design for less frequently accessed workloads. These volume types are not supported for Multi-Attach functionality.
- () Reference:
- () https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volumes-multi.html
- () A global enterprise maintains a hybrid cloud environment and wants to transfer large volumes of data between its on-premises data center and Amazon S3 for backup and analytics workflows. The company has already established a Direct Connect (DX) connection to AWS and wants to ensure high-bandwidth, low-latency, and secure private connectivity without traversing the public internet. The architecture must be designed to access Amazon S3 directly from on-premises systems using this DX connection.
- () Which configuration should the network engineering team implement to allow direct access to Amazon S3 from the on-premises data center using Direct Connect?
- () Use a Private Virtual Interface (Private VIF) on the Direct Connect connection and create a VPC endpoint to route traffic to S3 over the private network
- () Provision a Public Virtual Interface (Public VIF) on the Direct Connect connection to access Amazon S3 public IP addresses from the on-premises data center
- () Use a Transit Gateway with Direct Connect Gateway to route on-premises traffic through a VPC and then to Amazon S3 using private IP addressing
- () Configure a VPN connection over the public internet to AWS and route S3 traffic through the tunnel instead of using Direct Connect
- () via - https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html
- () Configure a VPN connection over the public internet to AWS and route S3 traffic through the tunnel instead of using Direct Connect - Using a VPN connection over the public internet to route traffic to S3 bypasses the benefits of Direct Connect, such as low latency, dedicated bandwidth, and private connectivity. VPN traffic traverses the public internet and therefore violates the requirements of the given use case.
- () https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html
- () A retail company needs a secure connection between its on-premises data center and AWS Cloud. This connection does not need high bandwidth and will handle a small amount of traffic. The company wants a quick turnaround time to set up the connection.
- () What is the MOST cost-effective way to establish such a connection?
- **() Set up an AWS Site-to-Site VPN connection** [CORRECT]
- () Set up AWS Direct Connect
- () Set up a bastion host on Amazon EC2
- () Set up an Internet Gateway between the on-premises data center and AWS cloud
- () By default, instances that you launch into an Amazon VPC can't communicate with your own (remote) network. You can enable access to your remote network from your VPC by creating an AWS Site-to-Site VPN (Site-to-Site VPN) connection, and configuring routing to pass traffic through the connection. A VPN connection refers to the connection between your VPC and your own on-premises network.
- () An AWS Site-to-Site VPN connection offers two VPN tunnels between a virtual private gateway or a transit gateway on the AWS side, and a customer gateway (which represents a VPN device) on the remote (on-premises) side.
- () A virtual private gateway (VGW) is the VPN concentrator on the Amazon side of the AWS Site-to-Site VPN connection. You create a virtual private gateway and attach it to the VPC from which you want to create the AWS Site-to-Site VPN connection.
- () How virtual private gateway works:
- () via - https://docs.aws.amazon.com/vpn/latest/s2svpn/how_it_works.html

**Answer:**
Correct Answer: **Set up an AWS Site-to-Site VPN connection**

---

## Question 201

**Q:** Which configuration should the network engineering team implement to allow direct access to Amazon S3 from the on-premises data center using Direct Connect?

**Options:**
- (A) Use a Private Virtual Interface (Private VIF) on the Direct Connect connection and create a VPC endpoint to route traffic to S3 over the private network
- (B) Provision a Public Virtual Interface (Public VIF) on the Direct Connect connection to access Amazon S3 public IP addresses from the on-premises data center
- (C) Use a Transit Gateway with Direct Connect Gateway to route on-premises traffic through a VPC and then to Amazon S3 using private IP addressing
- (D) Configure a VPN connection over the public internet to AWS and route S3 traffic through the tunnel instead of using Direct Connect
- (E) Correct option:
- (F) via - https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html
- (G) Incorrect options:
- (H) Configure a VPN connection over the public internet to AWS and route S3 traffic through the tunnel instead of using Direct Connect - Using a VPN connection over the public internet to route traffic to S3 bypasses the benefits of Direct Connect, such as low latency, dedicated bandwidth, and private connectivity. VPN traffic traverses the public internet and therefore violates the requirements of the given use case.
- (I) Reference:
- (J) https://docs.aws.amazon.com/directconnect/latest/UserGuide/Welcome.html
- () A retail company needs a secure connection between its on-premises data center and AWS Cloud. This connection does not need high bandwidth and will handle a small amount of traffic. The company wants a quick turnaround time to set up the connection.
- () What is the MOST cost-effective way to establish such a connection?
- **() Set up an AWS Site-to-Site VPN connection** [CORRECT]
- () Set up AWS Direct Connect
- () Set up a bastion host on Amazon EC2
- () Set up an Internet Gateway between the on-premises data center and AWS cloud
- () By default, instances that you launch into an Amazon VPC can't communicate with your own (remote) network. You can enable access to your remote network from your VPC by creating an AWS Site-to-Site VPN (Site-to-Site VPN) connection, and configuring routing to pass traffic through the connection. A VPN connection refers to the connection between your VPC and your own on-premises network.
- () An AWS Site-to-Site VPN connection offers two VPN tunnels between a virtual private gateway or a transit gateway on the AWS side, and a customer gateway (which represents a VPN device) on the remote (on-premises) side.
- () A virtual private gateway (VGW) is the VPN concentrator on the Amazon side of the AWS Site-to-Site VPN connection. You create a virtual private gateway and attach it to the VPC from which you want to create the AWS Site-to-Site VPN connection.
- () How virtual private gateway works:
- () via - https://docs.aws.amazon.com/vpn/latest/s2svpn/how_it_works.html
- () An AWS transit gateway is a transit hub that you can use to interconnect your virtual private clouds (VPC) and on-premises networks. For more information, see Amazon VPC Transit Gateways. You can create a Site-to-Site VPN connection as an attachment on a transit gateway.
- () How AWS transit gateway works:
- () Set up an Internet Gateway between the on-premises data center and AWS cloud - An Internet Gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between your VPC and the internet. An Internet Gateway cannot be used to set up a connection between its on-premises data center and AWS Cloud.
- () References:
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/how_it_works.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html
- ()  anymore. You would like to preserve the SQL querying capability on your data and get the queries started immediately. Also, you want to adopt a pricing model that allows you to save the maximum amount of cost on Amazon Redshift.
- () What do you recommend? (Select two)
- () Move the data to Amazon S3 Glacier Deep Archive after 30 days
- () Correct selection
- () Move the data to Amazon S3 Standard IA after 30 days
- () Create a smaller Amazon Redshift Cluster with the cold data

**Answer:**
Correct Answer: **Set up an AWS Site-to-Site VPN connection**

---

## Question 202

**Q:** What is the MOST cost-effective way to establish such a connection?

**Options:**
- **(A) Set up an AWS Site-to-Site VPN connection** [CORRECT]
- (B) Set up AWS Direct Connect
- (C) Set up a bastion host on Amazon EC2
- (D) Set up an Internet Gateway between the on-premises data center and AWS cloud
- (E) Correct option:
- (F) By default, instances that you launch into an Amazon VPC can't communicate with your own (remote) network. You can enable access to your remote network from your VPC by creating an AWS Site-to-Site VPN (Site-to-Site VPN) connection, and configuring routing to pass traffic through the connection. A VPN connection refers to the connection between your VPC and your own on-premises network.
- (G) An AWS Site-to-Site VPN connection offers two VPN tunnels between a virtual private gateway or a transit gateway on the AWS side, and a customer gateway (which represents a VPN device) on the remote (on-premises) side.
- (H) A virtual private gateway (VGW) is the VPN concentrator on the Amazon side of the AWS Site-to-Site VPN connection. You create a virtual private gateway and attach it to the VPC from which you want to create the AWS Site-to-Site VPN connection.
- (I) How virtual private gateway works:
- (J) via - https://docs.aws.amazon.com/vpn/latest/s2svpn/how_it_works.html
- () An AWS transit gateway is a transit hub that you can use to interconnect your virtual private clouds (VPC) and on-premises networks. For more information, see Amazon VPC Transit Gateways. You can create a Site-to-Site VPN connection as an attachment on a transit gateway.
- () How AWS transit gateway works:
- () Incorrect options:
- () Set up an Internet Gateway between the on-premises data center and AWS cloud - An Internet Gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between your VPC and the internet. An Internet Gateway cannot be used to set up a connection between its on-premises data center and AWS Cloud.
- () References:
- () https://docs.aws.amazon.com/vpn/latest/s2svpn/how_it_works.html
- () https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html
- ()  anymore. You would like to preserve the SQL querying capability on your data and get the queries started immediately. Also, you want to adopt a pricing model that allows you to save the maximum amount of cost on Amazon Redshift.
- () What do you recommend? (Select two)
- () Move the data to Amazon S3 Glacier Deep Archive after 30 days
- () Correct selection
- () Move the data to Amazon S3 Standard IA after 30 days
- () Create a smaller Amazon Redshift Cluster with the cold data
- () Analyze the cold data with Amazon Athena
- () Migrate the Amazon Redshift underlying storage to Amazon S3 IA
- () Correct options:
- () Amazon S3 Standard-IA is for data that is accessed less frequently but requires rapid access when needed. Amazon S3 Standard-IA offers high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval fee. This combination of low cost and high performance makes S3 Standard-IA ideal for long-term storage, backups, and as a data store for disaster recovery files. The minimum storage duration charge is 30 days.
- () Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to set up or manage, and customers pay only for the queries they run. You can use Amazon Athena to process logs, perform ad-hoc analysis, and run interactive queries.
- () Moving the data to Amazon S3 glacier will prevent us from being able to query it. Therefore, we should migrate the data to Amazon S3 Standard IA and use Amazon Athena to analyze the cold data.
- ()  of storage classes like Amazon S3, so this option is also ruled out.
- () Create a smaller Amazon Redshift Cluster with the cold data - Creating a smaller cluster with the cold data would not decrease the storage cost of Amazon Redshift, which will only increase with time as we keep on creating data. Therefore this option is ruled out.
- () Move the data to Amazon S3 Glacier Deep Archive after 30 days - Amazon S3 Glacier Deep Archive (GDA) is a secure, durable, and extremely low-cost Amazon S3 cloud storage class for data archiving and long-term backup. It is designed to deliver 99.999999999% durability, and provide comprehensive security and compliance capabilities that can help meet even the most stringent regulatory requirements. GDA has a first-byte latency of several hours, so this option is incorrect.
- () https://aws.amazon.com/athena/
- () https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html
- () A digital media company wants to track user engagement across its streaming platform by capturing events such as video starts, pauses, and search queries. These events must be ingested and analyzed in real time to improve user experience and optimize recommendations. The platform experiences unpredictable spikes in traffic during popular content releases. The company needs a highly scalable and serverless solution that can seamlessly adjust to changing workloads without manual provisioning.
- () Which solution will meet these requirements in the MOST efficient and scalable way?

**Answer:**
Correct Answer: **Set up an AWS Site-to-Site VPN connection**

---

## Question 203

**Q:** Which solution will meet these requirements in the MOST efficient and scalable way?

**Options:**
- (A) Use an Amazon Kinesis Data Streams stream in on-demand capacity mode to ingest user engagement data. Configure an AWS Lambda function as a consumer to process the events in real time
- (B) Deploy a fleet of Amazon EC2 instances running Apache Kafka to ingest clickstream data. Set up custom scripts to manually scale the Kafka cluster based on CPU usage. Use Amazon Athena to run periodic queries on stored clickstream logs
- (C) Use Amazon Simple Notification Service (Amazon SNS) to publish clickstream events. Subscribe an Amazon SQS standard queue to receive the events. Process the events in batches with AWS Glue jobs scheduled at fixed intervals
- (D) Use Amazon Kinesis Data Firehose to ingest user events. Set the destination as Amazon S3. Use Amazon Athena with scheduled queries to analyze the data periodically
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/streams/latest/dev/introduction.html
- (I) https://aws.amazon.com/blogs/aws/amazon-kinesis-data-streams-on-demand-stream-data-at-scale-without-managing-capacity/
- (J) https://docs.aws.amazon.com/msk/latest/developerguide/what-is-msk.html
- () Which solution meets these requirements in the most secure and scalable way?
- () Set up a centralized email forwarding service with rules that inspect notification content and forward emails to the appropriate team based on keywords such as “billing,” “security,” or “operations.” Keep the current root email addresses as they are, and rely on this service to triage alerts
- () Configure each AWS account’s root user to use an alias that redirects messages to a centralized mailbox monitored by platform administrators. Then assign alternate contacts for each account using company-managed distribution lists for billing, security, and operations to handle service-specific notifications
- () Change each AWS account’s root email to a unique departmental email list and configure IAM notification settings to send alerts based on service type. Do not use AWS alternate contacts since notifications are already routed by service in the IAM console
- () Assign each AWS account’s root user email to a single designated member of the respective department (e.g., security lead or billing analyst). Encourage these individuals to monitor the email accounts regularly. Also configure alternate contacts with the same individual email addresses
- () https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-01.html
- () https://docs.aws.amazon.com/organizations/latest/userguide/orgs_best-practices.html
- () https://docs.aws.amazon.com/accounts/latest/reference/accounts-welcome.html
- () During a review, a security team has flagged concerns over an Amazon EC2 instance querying IP addresses used for cryptocurrency mining. The Amazon EC2 instance does not host any authorized application related to cryptocurrency mining.
- () Which AWS service can be used to protect the Amazon EC2 instances from such unauthorized behavior in the future?
- () AWS Firewall Manager
- () AWS Shield Advanced
- () AWS Web Application Firewall (AWS WAF)
- **() Amazon GuardDuty** [CORRECT]
- () Amazon GuardDuty continuously monitors for malicious or unauthorized behavior to help protect your AWS resources, including your AWS accounts and access keys. Amazon GuardDuty identifies any unusual or unauthorized activity, like cryptocurrency mining or infrastructure deployments in a region that has never been used. Powered by threat intelligence and machine learning, GuardDuty is continuously evolving to help you protect your AWS environment.
- () The cryptocurrency finding expands the service’s ability to detect Amazon EC2 instances querying IP addresses associated with the cryptocurrency-related activity. The finding type is: CryptoCurrency:EC2/BitcoinTool.B, CryptoCurrency:EC2/BitcoinTool.B!DNS.
- () This finding informs you that the listed Amazon EC2 instance in your AWS environment is querying a domain name that is associated with Bitcoin or other cryptocurrency-related activity. Bitcoin is a worldwide cryptocurrency and digital payment system that can be exchanged for other currencies, products, and services. Bitcoin is a reward for bitcoin mining and is highly sought after by threat actors.
- () If you use the Amazon EC2 instance to mine or manage cryptocurrency, or this instance is otherwise involved in blockchain activity, this finding could represent expected activity for your environment. If this is the case in your AWS environment, AWS recommends that you set up a suppression rule for this finding.
- () AWS Web Application Firewall (AWS WAF) - AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits and bots that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that control bot traffic and block common attack patterns, such as SQL injection or cross-site scripting.

**Answer:**
Correct Answer: **Amazon GuardDuty**

---

## Question 204

**Q:** Which solution meets these requirements in the most secure and scalable way?

**Options:**
- (A) Set up a centralized email forwarding service with rules that inspect notification content and forward emails to the appropriate team based on keywords such as “billing,” “security,” or “operations.” Keep the current root email addresses as they are, and rely on this service to triage alerts
- (B) Configure each AWS account’s root user to use an alias that redirects messages to a centralized mailbox monitored by platform administrators. Then assign alternate contacts for each account using company-managed distribution lists for billing, security, and operations to handle service-specific notifications
- (C) Change each AWS account’s root email to a unique departmental email list and configure IAM notification settings to send alerts based on service type. Do not use AWS alternate contacts since notifications are already routed by service in the IAM console
- (D) Assign each AWS account’s root user email to a single designated member of the respective department (e.g., security lead or billing analyst). Encourage these individuals to monitor the email accounts regularly. Also configure alternate contacts with the same individual email addresses
- (E) Correct option:
- (F) Incorrect options:
- (G) References:
- (H) https://docs.aws.amazon.com/prescriptive-guidance/latest/aws-startup-security-baseline/acct-01.html
- (I) https://docs.aws.amazon.com/organizations/latest/userguide/orgs_best-practices.html
- (J) https://docs.aws.amazon.com/accounts/latest/reference/accounts-welcome.html
- () During a review, a security team has flagged concerns over an Amazon EC2 instance querying IP addresses used for cryptocurrency mining. The Amazon EC2 instance does not host any authorized application related to cryptocurrency mining.
- () Which AWS service can be used to protect the Amazon EC2 instances from such unauthorized behavior in the future?
- () AWS Firewall Manager
- () AWS Shield Advanced
- () AWS Web Application Firewall (AWS WAF)
- **() Amazon GuardDuty** [CORRECT]
- () Amazon GuardDuty continuously monitors for malicious or unauthorized behavior to help protect your AWS resources, including your AWS accounts and access keys. Amazon GuardDuty identifies any unusual or unauthorized activity, like cryptocurrency mining or infrastructure deployments in a region that has never been used. Powered by threat intelligence and machine learning, GuardDuty is continuously evolving to help you protect your AWS environment.
- () The cryptocurrency finding expands the service’s ability to detect Amazon EC2 instances querying IP addresses associated with the cryptocurrency-related activity. The finding type is: CryptoCurrency:EC2/BitcoinTool.B, CryptoCurrency:EC2/BitcoinTool.B!DNS.
- () This finding informs you that the listed Amazon EC2 instance in your AWS environment is querying a domain name that is associated with Bitcoin or other cryptocurrency-related activity. Bitcoin is a worldwide cryptocurrency and digital payment system that can be exchanged for other currencies, products, and services. Bitcoin is a reward for bitcoin mining and is highly sought after by threat actors.
- () If you use the Amazon EC2 instance to mine or manage cryptocurrency, or this instance is otherwise involved in blockchain activity, this finding could represent expected activity for your environment. If this is the case in your AWS environment, AWS recommends that you set up a suppression rule for this finding.
- () AWS Web Application Firewall (AWS WAF) - AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits and bots that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that control bot traffic and block common attack patterns, such as SQL injection or cross-site scripting.
- () None of these three services can detect unauthorized cryptocurrency mining activity on EC2 instances, so these options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-ec2.html#cryptocurrency-ec2-bitcointoolbdns
- () A global logistics provider operates several legacy applications on virtual machines (VMs) within a private data center. Due to accelerated business growth and limited capacity in its existing infrastructure, the provider decides to migrate select applications to AWS. The company opts for a lift-and-shift strategy for its non-mission-critical systems to meet tight migration deadlines. The solution must support rapid migration without requiring extensive application refactoring.
- () Which combination of actions will best support this migration approach? (Select three)
- () Shut down the source virtual machines and immediately provision EC2 replacement instances using manual AMI creation
- () Correct selection
- () Launch a cutover instance after completing testing and confirming that replication is up-to-date
- () Use Amazon EC2 Auto Scaling to automatically re-create the VMs in AWS by launching replacement instances with matching configurations
- () Use AWS Application Migration Service (MGN). Install the AWS Replication Agent on the source VMs
- () Use AWS CloudEndure Disaster Recovery to continuously replicate the VMs to AWS and then promote the target instances for production use
- () Perform the initial replication. Launch test instances in AWS to validate the migrated VMs before final cutover
- () Correct options:
- () AWS Application Migration Service (MGN) is a highly automated lift-and-shift (rehost) solution that simplifies, expedites, and reduces the cost of migrating applications to AWS. It allows companies to lift-and-shift a large number of physical, virtual, or cloud servers without compatibility issues, performance disruption, or long cutover windows. Application Migration Service replicates source servers into your AWS account.

**Answer:**
Correct Answer: **Amazon GuardDuty**

---

## Question 205

**Q:** Which AWS service can be used to protect the Amazon EC2 instances from such unauthorized behavior in the future?

**Options:**
- (A) AWS Firewall Manager
- (B) AWS Shield Advanced
- (C) AWS Web Application Firewall (AWS WAF)
- **(D) Amazon GuardDuty** [CORRECT]
- (E) Correct option:
- (F) Amazon GuardDuty continuously monitors for malicious or unauthorized behavior to help protect your AWS resources, including your AWS accounts and access keys. Amazon GuardDuty identifies any unusual or unauthorized activity, like cryptocurrency mining or infrastructure deployments in a region that has never been used. Powered by threat intelligence and machine learning, GuardDuty is continuously evolving to help you protect your AWS environment.
- (G) The cryptocurrency finding expands the service’s ability to detect Amazon EC2 instances querying IP addresses associated with the cryptocurrency-related activity. The finding type is: CryptoCurrency:EC2/BitcoinTool.B, CryptoCurrency:EC2/BitcoinTool.B!DNS.
- (H) This finding informs you that the listed Amazon EC2 instance in your AWS environment is querying a domain name that is associated with Bitcoin or other cryptocurrency-related activity. Bitcoin is a worldwide cryptocurrency and digital payment system that can be exchanged for other currencies, products, and services. Bitcoin is a reward for bitcoin mining and is highly sought after by threat actors.
- (I) If you use the Amazon EC2 instance to mine or manage cryptocurrency, or this instance is otherwise involved in blockchain activity, this finding could represent expected activity for your environment. If this is the case in your AWS environment, AWS recommends that you set up a suppression rule for this finding.
- (J) Incorrect options:
- () AWS Web Application Firewall (AWS WAF) - AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits and bots that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that control bot traffic and block common attack patterns, such as SQL injection or cross-site scripting.
- () None of these three services can detect unauthorized cryptocurrency mining activity on EC2 instances, so these options are incorrect.
- () Reference:
- () https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-ec2.html#cryptocurrency-ec2-bitcointoolbdns
- () A global logistics provider operates several legacy applications on virtual machines (VMs) within a private data center. Due to accelerated business growth and limited capacity in its existing infrastructure, the provider decides to migrate select applications to AWS. The company opts for a lift-and-shift strategy for its non-mission-critical systems to meet tight migration deadlines. The solution must support rapid migration without requiring extensive application refactoring.
- () Which combination of actions will best support this migration approach? (Select three)
- () Shut down the source virtual machines and immediately provision EC2 replacement instances using manual AMI creation
- () Correct selection
- () Launch a cutover instance after completing testing and confirming that replication is up-to-date
- () Use Amazon EC2 Auto Scaling to automatically re-create the VMs in AWS by launching replacement instances with matching configurations
- () Use AWS Application Migration Service (MGN). Install the AWS Replication Agent on the source VMs
- () Use AWS CloudEndure Disaster Recovery to continuously replicate the VMs to AWS and then promote the target instances for production use
- () Perform the initial replication. Launch test instances in AWS to validate the migrated VMs before final cutover
- () Correct options:
- () AWS Application Migration Service (MGN) is a highly automated lift-and-shift (rehost) solution that simplifies, expedites, and reduces the cost of migrating applications to AWS. It allows companies to lift-and-shift a large number of physical, virtual, or cloud servers without compatibility issues, performance disruption, or long cutover windows. Application Migration Service replicates source servers into your AWS account.
- () AWS Application Migration Service (MGN) is the recommended AWS tool for lift-and-shift VM migrations. It supports real-time replication of on-premises workloads to AWS with minimal disruption. The Replication Agent is installed on each source VM to handle continuous data transfer. This eliminates the need for image creation or application rewrites, making it ideal for quick, large-scale migrations.
- () This reflects a standard step in AWS MGN migration workflows. After the initial sync is complete, test instances are launched to validate the integrity and functionality of the migrated VMs. This is critical for quality assurance before moving workloads into production and helps reduce the risk of failure after cutover.
- () via - https://docs.aws.amazon.com/mgn/latest/ug/migration-workflow-gs.html
- () This represents the final step in AWS MGN migrations. After validation testing and a final sync of changes from the on-premises environment, a cutover instance is launched to go live in production. The original VM can be decommissioned once the EC2 instance is confirmed to be working as intended.
- () References:
- () https://docs.aws.amazon.com/mgn/latest/ug/what-is-application-migration-service.html
- () https://docs.aws.amazon.com/mgn/latest/ug/migration-workflow-gs.html

**Answer:**
Correct Answer: **Amazon GuardDuty**

---

## Question 206

**Q:** Which combination of actions will best support this migration approach? (Select three)

**Options:**
- **(A) Shut down the source virtual machines and immediately provision EC2 replacement instances using manual AMI creation** [CORRECT]
- (B) Correct selection
- (C) Launch a cutover instance after completing testing and confirming that replication is up-to-date
- (D) Use Amazon EC2 Auto Scaling to automatically re-create the VMs in AWS by launching replacement instances with matching configurations
- (E) Use AWS Application Migration Service (MGN). Install the AWS Replication Agent on the source VMs
- (F) Use AWS CloudEndure Disaster Recovery to continuously replicate the VMs to AWS and then promote the target instances for production use
- (G) Perform the initial replication. Launch test instances in AWS to validate the migrated VMs before final cutover
- (H) Correct options:
- (I) AWS Application Migration Service (MGN) is a highly automated lift-and-shift (rehost) solution that simplifies, expedites, and reduces the cost of migrating applications to AWS. It allows companies to lift-and-shift a large number of physical, virtual, or cloud servers without compatibility issues, performance disruption, or long cutover windows. Application Migration Service replicates source servers into your AWS account.
- (J) AWS Application Migration Service (MGN) is the recommended AWS tool for lift-and-shift VM migrations. It supports real-time replication of on-premises workloads to AWS with minimal disruption. The Replication Agent is installed on each source VM to handle continuous data transfer. This eliminates the need for image creation or application rewrites, making it ideal for quick, large-scale migrations.
- () This reflects a standard step in AWS MGN migration workflows. After the initial sync is complete, test instances are launched to validate the integrity and functionality of the migrated VMs. This is critical for quality assurance before moving workloads into production and helps reduce the risk of failure after cutover.
- () via - https://docs.aws.amazon.com/mgn/latest/ug/migration-workflow-gs.html
- () This represents the final step in AWS MGN migrations. After validation testing and a final sync of changes from the on-premises environment, a cutover instance is launched to go live in production. The original VM can be decommissioned once the EC2 instance is confirmed to be working as intended.
- () Incorrect options:
- () References:
- () https://docs.aws.amazon.com/mgn/latest/ug/what-is-application-migration-service.html
- () https://docs.aws.amazon.com/mgn/latest/ug/migration-workflow-gs.html

**Answer:**
Correct Answer: **Shut down the source virtual machines and immediately provision EC2 replacement instances using manual AMI creation**

---


