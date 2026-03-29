# AWS SAA-C03 Practice Questions - Part 3

Total Questions: 39

---

## Question 1

**Q:** What authentication method can be used for programmatic or CLI-based access that avoids the use of usernames and passwords?

**Options:**
- (A) Access Key ID/Username
- (B) Username/Secret Access Key
- (C) Password/Access Key ID
- **(D) Access Key ID/Secret Access Key** [CORRECT]

**Explanation:**
Access Key ID/Secret Access Key is the correct answer. The AWS Access Keys are a combination of an Access Key ID and a secret access key. Using this method allows for programmatic access to AWS services and can also be beneficial when performing command-line interface (CLI) operations.

---

## Question 2

**Q:** Scenario: You are using large-scale databases and intensive processing EC2 instances. If you know the amount of resources required for one year or more for an AWS EC2 instance or RDS database, what can be utilized to reduce costs by 40% or more?

**Options:**
- **(A) Reserved pricing** [CORRECT]
- (B) Free tier services
- (C) None of these
- (D) On-Demand pricing

**Explanation:**
Reserved pricing is the correct answer. The AWS Pricing Calculator can be used to estimate costs for the major AWS services including S3 and EC2. The other listed items are used to work with costs related to actual implemented solutions.

---

## Question 3

**Q:** What can be configured to optimize EFS performance in relation to NFS mount options?

**Options:**
- (A) Use FTP instead of NFS
- (B) Use NFSv4.0
- **(C) Use NFSv4.1** [CORRECT]
- (D) Use TFTP instead of NFS

**Explanation:**
Use NFSv4.1 is the correct answer. NFSv4.1 improves performance over NFSv4.0 and should be used whenever possible. Neither FTP nor TFTP improve performance over NFS and are not available as an NFS mount configuration option.

---

## Question 4

**Q:** What is the up-front cost incurred by creating S3 buckets?

**Options:**
- (A) Variable depending on bucket configuration parameters
- **(B) $0** [CORRECT]
- (C) $10 per bucket
- (D) $100 per bucket

**Explanation:**
$0 is the correct answer. The creation of S3 buckets does not incur cost. Costs accrue based on the usage of the bucket (storage consumed and data transferred).

---

## Question 5

**Q:** How should you enforce the use of an 8-character password for all AWS logins?

**Options:**
- **(A) Through a password policy** [CORRECT]
- (B) For each login created
- (C) For each group
- (D) You cannot enforce such settings

**Explanation:**
Through a password policy is the correct answer. You can create a password policy that is then applied to logins. The policy can define password characteristics and the frequency at which passwords must be changed.

---

## Question 6

**Q:** What solution is the least expensive, within AWS, for long-term data storage and archives?

**Options:**
- (A) Snowball
- (B) S3 Standard
- (C) Redshift
- **(D) Glacier** [CORRECT]

**Explanation:**
Glacier is the correct answer. Glacier is the best option among those listed for long-term storage at lower cost. Snowball is used to move data into the cloud using an offline device. Redshift is an OLAP data warehouse database. S3 standard could be used, but it is more expensive than Glacier for long-term storage.

---

## Question 7

**Q:** Which one of the following languages is not supported by Elastic Beanstalk?

**Options:**
- (A) Java
- (B) Python
- **(C) Perl** [CORRECT]
- (D) Node.js

**Explanation:**
Perl is the correct answer. Perl is not supported by Elastic Beanstalk. Java, .NET, Node.js, PHP, Ruby, Python, and Go are supported.

---

## Question 8

**Q:** Your client has been experiencing problems with their aging in-house infrastructure and is extremely concerned about managing the cost of maintaining their online presence. After deciding that the cost of developing a sound DR plan more than makes up for the negative impact of being offline, the board has directed you to prepare a proposal that achieves an RTO of 20 hours, an RPO of 1 hour, and keeps the costs of meeting those target time windows to a minimum. They have also mandated the use of the AWS Storage Gateway to mitigate the risk associated with a catastrophic NAS failure. Which of the following solutions best meet the requirements?

**Options:**
- (A) Provide their engineering staff with an AWS account and create IAM users, groups, and roles. Use CloudFormation/CloudFormer to clone the existing on-premises environment and store the build scripts in GitHub. Migrate the in-house DNS to Route 53 to simplify cutover. Set up the Storage Gateway and the Snapshot schedule to meet the RPO. Provide the engineering team with a CLI script to kick-start the CloudFormation build and restoration of the Storage Gateway snapshots.
- (B) Provide their engineering staff with an AWS account. Create a small, under-sized DR DB instance and use application synchronization to keep the DR instance synchronized within 30 seconds of the production instance. Build one of each web/app server and keep these patched and online. Provide the Ops team with written instructions explaining how to upgrade the DB host to a full-sized instance within 20 minutes.
- (C) Provide their engineering staff with an AWS account, and ask them to rebuild all the servers in AWS to form a fully functional hot-standby environment. Use Storage Gateway to copy the data on the NAS to S3 so that it can be accessed by the database servers.
- **(D) Work with the customer’s engineers to identify the key servers and data. Help them set up an AWS account with IAM users, groups, and roles. Build templates of the critical web/app servers and save these as AMIs. Agree upon RDS specifications that meet the stated requirements. Set up the Storage Gateway and the Snapshot schedule to meet the RPO. Document, script, or automate the steps to initiate the RDS instance, the EC2 instances, the steps to restore the latest data from the Storage Gateway snapshots into RDS, plus any DNS changes. Test the process with each of the operations team’s shifts.** [CORRECT]

**Explanation:**
Work with the customer’s engineers to identify the key servers and data. Help them set up an AWS account with IAM users, groups, and roles. Build templates of the critical web/app servers and save these as AMIs. Agree upon RDS specifications that meet the stated requirements. Set up the Storage Gateway and the Snapshot schedule to meet the RPO. Document, script, or automate the steps to initiate the RDS instance, the EC2 instances, the steps to restore the latest data from the Storage Gateway snapshots into RDS, plus any DNS changes. Test the process with each of the operations team’s shifts is correct.

---

## Question 9

**Q:** Given that Elastic Beanstalk automatically creates the environment to run your application code, what is the extra cost associated with its use?

**Options:**
- (A) $0.25 per minute required to create the environment
- (B) $50 per application
- **(C) No extra cost** [CORRECT]
- (D) $100 per application

**Explanation:**
No extra cost is the correct answer. There is no extra cost associated with using Elastic Beanstalk. You are charged for the resources used to actually run the application, but are not charged to implement the environment required.

---

## Question 10

**Q:** What EC2 instance type can be used to provide up to a 90% discount off on-demand instance prices?

**Options:**
- (A) Reduced Cost instance
- **(B) Spot instance** [CORRECT]
- (C) Downgraded instance
- (D) Automatic instance

**Explanation:**
Spot instance is the correct answer. Spot instances run whenever capacity is available and the maximum price for a request exceeds the Spot price, according to AWS documentation. They should only when your process includes the flexibility of running with interruption and running whenever it can as opposed to specific required times. On-Demand instances are also used when you desire to reduce costs over always-on instances (typical EC2 instances) but allows for launching at specific required times. The other instance types listed do not exist in AWS.

---

## Question 11

**Q:** To audit the API calls made to your account, which AWS service would you use?

**Options:**
- **(A) AWS CloudTrail** [CORRECT]
- (B) AWS CloudWatch
- (C) AWS Lambda
- (D) AWS Systems Manager

**Explanation:**
AWS CloudTrail is correct. AWS CloudTrail is used to audit the API calls.

---

## Question 12

**Q:** What should be implemented to ensure security when using AWS Access Keys?

**Options:**
- (A) Key Decryption
- (B) Key Encryption
- (C) Password-protected keys
- **(D) Key Rotation** [CORRECT]

**Explanation:**
Key rotation is the correct answer. Key rotation is used to retire older keys. The longer keys are used, the more likely they have been compromised. Rotate keys by generating new keys, updating applications and users with the new keys, deactivating the old keys, monitoring to ensure you've captured all of the use cases for the keys.

---

## Question 13

**Q:** What cannot be specified for an S3 bucket?

**Options:**
- (A) The name
- (B) Encryption
- **(C) The Availability Zone (AZ)** [CORRECT]
- (D) The permissions

**Explanation:**
The Availability Zone (AZ) is the correct answer. While S3 buckets are stored in an AZ, you cannot specify into which AZ it should be placed. Regardless of the S3 storage class, the AZ is selected automatically by AWS.

---

## Question 14

**Q:** You have been engaged by a company to design and lead a migration to an AWS environment. The team is concerned about the capabilities of the new environment, especially when it comes to avoiding all bottlenecks. The design calls for about 20 instances (C3.2xLarge) pulling jobs/messages from SQS. Network traffic per instance is estimated to be around 500Mbps at the beginning and end of each job. Which network configuration should you plan on deploying?

**Options:**
- (A) Activate EBS-Optimization on the instance to maximize network throughput.
- (B) Use a second network interface to separate the SQS traffic from the storage traffic.
- (C) Choose a different instance type that better matched the traffic demand.
- (D) Deploy as a placement group, as the aggregated burst traffic could be around 10Gbps.
- **(E) Spread the instances over multiple AZs to minimize the traffic concentration and maximize the fault tolerance.** [CORRECT]

**Explanation:**
Spread the instances over multiple AZs to minimize the traffic concentration and maximize the fault tolerance is correct. When considering network traffic, you need to understand the difference between storage traffic and general network traffic, and the ways to address each. The 10Gbps is a red herring, in that the 500Mbps only occurs for short intervals, and therefore your sustained throughput is not 10Gbps. Wherever possible, use simple solutions such as spreading the load out rather than expensive high-tech solutions. 

---

## Question 15

**Q:** You must transfer one exabyte of data into AWS and you do not want to transfer it across the Internet. What AWS solution should you use?

**Options:**
- (A) Snowball
- (B) HTTPS transfer to S3 buckets
- **(C) Snowmobile** [CORRECT]
- (D) Direct Connect

**Explanation:**
Snowmobile is the correct answer. AWS Snowmobile supports exabyte-scale data transfer. The Snowmobile is connected to your network, the data is transferred to the Snowmobile, and then it is physically transported to an AWS data center and transferred to the cloud. The Snowball solution can handle up to 80 TB of data. Both Direct Connect and HTTPS transfer to S3 buckets that would transfer across the Internet in some way.

---

## Question 16

**Q:** You must attach an EBS volume to an EC2 instance that offers 500 GiB of storage at the lowest cost. What EBS type should be used?

**Options:**
- (A) Throughput-optimized HDD
- (B) Provisioned IOPS
- **(C) Cold HDD** [CORRECT]
- (D) General SSD

**Explanation:**
Cold HDD is the correct answer. Cold HDD is the lowest cost storage solution. General (or General Purpose) SSD is more expensive, though not as expensive as Provisioned IOPS. Throughput-optimized HDD is magnetic storage, like Cold HDD, but is not as inexpensive as Cold HDD.

---

## Question 17

**Q:** In addition to database instance class and redundancy options (such as Multi-AZ configurations), what has the most significant impact on the direct cost for RDS databases?

**Options:**
- (A) The use of EC2 instances to access the database
- (B) The use of remote clients to access the database
- **(C) The database engine in use** [CORRECT]
- (D) The creation of snapshots

**Explanation:**
The database engine in use is the correct answer. You can download, from AWS S3 to your local network, up to 1 GB per month at no charge. The other listed ranges are the pricing scales as of 2020. For example, from 1 GB to 9.999 TB is $0.09 per GB of transfer. From 10 TB to 40 TB is $0.085 per GB of transfer. And from 40 TB to 100 TB is $0.07 per GB of transfer.

---

## Question 18

**Q:** You must plan a Route 53 deployment in AWS. What routing policy is used to send all traffic to a single resource?

**Options:**
- (A) Geolocation routing
- **(B) Simple routing** [CORRECT]
- (C) Latency-based routing
- (D) Route 53 is not used in this way

**Explanation:**
Simple routing is the correct answer. Simple routing routes all traffic to a particular resource. This is typical DNS name resolution. Geolocation routing routes based on the location of the requestor. Latency-based routing routes based on the delay in communications between the source and the various possible resources.

---

## Question 19

**Q:** When policies can be written in a language in AWS, what language is most often used?

**Options:**
- (A) Python
- (B) HTML
- **(C) JSON** [CORRECT]
- (D) YAML

**Explanation:**
JSON is the correct answer. JSON is the most common language used for policy creation in AWS. JSON stands for JavaScript Object Notation.

---

## Question 20

**Q:** What can be easily implemented to segregate a group of servers from the rest of your AWS cloud so that the servers can communicate with each other and the Internet, but not with other servers in your cloud?

**Options:**
- (A) Availability Zone (AZ)
- (B) AWS Marketplace AMIs
- (C) VPN
- **(D) VPC** [CORRECT]

**Explanation:**
VPC is the correct answer. A Virtual Private Cloud (VPC) can be created and instances can be placed in the VPC and allowed to communicate with each other and the Internet. If you do not enable the VPC to communicate with other VPCs, the server instances in one VPC cannot communicate with the instances in other VPCs. Availability Zones and AMIs do not directly provide for this. A VPN also does not provide this solution.

---

## Question 21

**Q:** What is the default upload operation type for data transferred to an S3 bucket?

**Options:**
- **(A) A single PUT operation** [CORRECT]
- (B) FTP transmission
- (C) sFTP transmission
- (D) A multi-part PUT operation

**Explanation:**
A single PUT operation is the correct answer. By default, all files transferred to an S3 bucket are transferred using a single PUT operation. AWS suggests that files up to 100 MB in size can be transferred using this default operation. Larger files may require uploads through multi-part operations.

---

## Question 22

**Q:** You want to provide multiple virtual hard disks to an EC2 instance. What can you attach to an instance to provide these virtual hard disks?

**Options:**
- (A) EIP
- (B) VPC
- (C) NACL
- **(D) EBS volume** [CORRECT]

**Explanation:**
EBS volume is the correct answer. Multiple Elastic Block Store (EBS) volumes can be attached to an EC2 instance to act as hard disks. Several EBS volume types exist providing different performance levels. A VPC is not a virtual hard disk, but a virtual network segment. A NACL is a network access control list used to function as a firewall for a VPC. An Elastic IP (EIP) address is a statically assigned IP address that can be purchased for an instance by associating it with an Elastic Network Interface (ENI) bound to the instance.

---

## Question 23

**Q:** Which one of the following resources cannot be automatically scaled with AWS Auto Scaling?

**Options:**
- (A) EC2 Auto Scaling groups
- **(B) Microsoft SQL Server RDS databases** [CORRECT]
- (C) DynamoDB tables
- (D) Aurora DB clusters

**Explanation:**
Microsoft SQL Server RDS databases is the correct answer. You cannot scale Microsoft SQL Server or Oracle databases hosted in RDS. You can scale EC2 Auto Scaling groups, Aurora DB clusters, DynamoDB tables, DynamoDB global secondary indexes, ECS services, and Spot Fleet requests.

---

## Question 24

**Q:** What is a security best practice that should be implemented for the root login immediately after creating an AWS account?

**Options:**
- **(A) Enable MFA** [CORRECT]
- (B) Disable MFA
- (C) Delete the root login
- (D) Enable root login firewalling

**Explanation:**
Enable MFA is the correct answer. You should enable multi-factor authentication (MFA) for the root login and create another account for administrative actions immediately upon creating a new AWS account. You should not delete the root login and, in fact, cannot, as it is the only account that can perform specific account management actions.

---

## Question 25

**Q:** You have been monitoring a sensitive Auto Scaling group, and you expect it to scale in as you enter a period of downtime over the holiday. The Auto Scaling group is distributed over three AZs (AZ -A and AZ -B have two instances each, and AZ -C has three instances). All instances have different CPU and memory utilization levels and have been running for a different number of days. All instances come from different versions of a root AMI and have different numbers of sessions connected. Which instance will be the first to shut down?

**Options:**
- **(A) The instance in AZ -C that has the oldest launch configuration will terminate first.** [CORRECT]
- (B) The instance with the fewest current sessions will terminate first.
- (C) The instance in AZ -C that has the least number of sessions will terminate first.
- (D) The instance in AZ -C that has been running the longest will terminate first.
- (E) The instance that has been running longest will terminate first.

**Explanation:**
The instance in AZ -C that has the oldest launch configuration will terminate first is correct. As per the Auto Scaling rules, the oldest launch configurations are terminated first because they have the older versions of the AMIs. The reason is that the one with the oldest launch configuration will have the old hardware as well as old versions of patches, firmware, and so on. Therefore, the instance with the older versions is terminated first so that when the instance is restarted, it is refreshed with a new version of the hardware. 

---

## Question 26

**Q:** You want to implement a multi-account AWS cloud deployment that more easily complies with business policies during implementation. You wish to implement guardrails that prevent users from taking specific actions that might breech security policies. What AWS service can provide this and works with organizations as well?

**Options:**
- (A) Amazon EventBridge
- (B) Amazon Sumerian
- (C) AWS Glue
- **(D) AWS Control Tower** [CORRECT]

**Explanation:**
AWS Control Tower is the correct answer. The one service that provides all the required features is AWS Control Tower. According to AWS documentation, AWS Control Tower provides the easiest way to set up and govern a secure, compliant, multi-account AWS environment. Amazon Sumerian is used for Augmented Reality and Virtual Reality. Amazon EventBridge is used to connect applications to various data sources. AWS Glue is an ETL (extract, transform, and load) tool for data manipulation and transfer.

---

## Question 27

**Q:** What is the solution for logging actions taken within the AWS cloud, such as creating resources, deleting resources, and reconfiguring resources?

**Options:**
- **(A) CloudTrail** [CORRECT]
- (B) SQS
- (C) CloudWatch
- (D) SNS

**Explanation:**
CloudTrail is the correct answer. AWS CloudTrail is used to audit or log the administrative actions taken within AWS. All actions occur based on API calls and these API action activities are logged. CloudWatch captures performance metrics. SNS is the notification service and SQS is the message queueing service.

---

## Question 28

**Q:** You are implementing a web hosting architecture in AWS. Three EC2 instances are in use. The first is a web server, the second an application server, and the third is a database server. The web server communicates with the application server, but not with the database server. The application server communicates with the database server and the web server. Outside uses may access the web server directly, but they cannot access other servers. What kind of secure architecture are you implementing?

**Options:**
- (A) A monolithic secure architecture
- (B) A single-server secure architecture
- **(C) A multi-tier secure architecture** [CORRECT]
- (D) A single-tier secure architecture

**Explanation:**
A multi-tier secure architecture is the correct answer. The description is of a multi-tier or n-tier secure architecture – in this case, a three-tier architecture. A single-tier, monolithic, or single-server architecture may refer to the same type of architecture that uses only one tier.

---

## Question 29

**Q:** You are working with roles. When changes are made to roles, when do they take effect?

**Options:**
- (A) When any associate instance is restarted
- **(B) Immediately** [CORRECT]
- (C) When resources become available
- (D) When the active role is not longer actively used

**Explanation:**
immediately is the correct answer. Any changes made to roles are effective immediately. There is no delay or wait for resources.

---

## Question 30

**Q:** You are reviewing Change Control requests and note a change designed to reduce wasted CPU cycles by increasing the value of the VisibilityTimeout attribute. What does this mean?

**Options:**
- (A) When the consumer instance polls for new work, the consumer instance will wait a certain amount of time until it has a full workload before closing the connection.
- (B) When the consumer instance polls for new work, the SQS service will allow it to wait a certain amount of time for a message to be available before closing the connection.
- (C) When a new message is added to the SQS queue, it will be hidden from consumer instances for a fixed period of time.
- (D) While processing a message, a consumer instance can amend the message visibility counter by a fixed amount.
- (E) While processing a message, a consumer instance can reset the message visibility by restarting the preset timeout counter.
- **() When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time.** [CORRECT]

**Explanation:**
When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time is correct. When a consumer instance retrieves a message, that message will be hidden from other consumer instances for a fixed period of time. You have the ability to control this timeout period. 

---

## Question 31

**Q:** What can be implemented to prevent traffic from the network to your EC2 instance from impacting the performance of traffic between your EC2 instance and an attached EBS volume?

**Options:**
- (A) Implement network-optimized instances
- **(B) Implement EBS-optimized instances** [CORRECT]
- (C) Put the EBS volume in one VPC and the instance in another
- (D) Place the EBS volume in one region and the instance in another

**Explanation:**
Implement EBS-optimized instances is the correct answer. Using EBS-optimized instances will prevent regular instance network traffic from impacting communications between the instance and the EBS volume. It is never a good idea, for performance, to move storage farther away from the processing instance.

---

## Question 32

**Q:** What is the primary difference between durability and availability as it related to AWS storage?

**Options:**
- (A) Availability and durability are synonymous
- **(B) Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not** [CORRECT]
- (C) Durability is related to accessing the data at a point in time and accessibility is related to the existence of the data whether durable or not
- (D) Availability ensures data can be recovered and durability ensures data can be accessed

**Explanation:**
Availability is related to accessing the data at a point in time and durability is related to the existence of the data whether accessible or not is the correct answer. Availability and durability should not be confused. Availability is a measurement of data accessibility. That is, how often the data is there when a user attempts to access it. Durability is a measurement of data existence. That is, how long the data will be ensured to exist in some recoverable storage method, even if it is not immediately accessible by a particular user.

---

## Question 33

**Q:** What AWS service can be used to automate server scaling and configuration based on Chef or Puppet?

**Options:**
- **(A) OpsWorks** [CORRECT]
- (B) Elastic MapReduce
- (C) CloudFormation
- (D) CloudFront

**Explanation:**
OpsWorks is the correct answer. AWS OpsWorks supports Chef, Puppet, and stacks for automatic scaling and configuration of server environments. CloudFront is a CDN and Elastic MapReduce is used for data analytics. CloudFormation is not based on Chef or Puppet, but can be used to initially launch an entire required solution.

---

## Question 34

**Q:** What cannot be accomplished with an EFS storage solution?

**Options:**
- (A) Connecting it to a Linux instance
- (B) Encryption
- **(C) Connecting it to a Windows instance** [CORRECT]
- (D) Storing documents as well as database files

**Explanation:**
Connecting it to a Windows instance is the correct answer. EFS supports Linux instances, but it does not support Windows instances. It can be used to store any file types and it also supports encryption.

---

## Question 35

**Q:** What is the maximum S3 PUTs per second rate supported in AWS?

**Options:**
- **(A) 3500** [CORRECT]
- (B) 100
- (C) 2500
- (D) 1000

**Explanation:**
3500 is the correct answer. The PUTs per second rate was raised from 100 to 3500 in 2018 and can be very important for those preparing for the AWS exams.

---

## Question 36

**Q:** You are designing a password policy for IAM users. Which one of the following cannot be configured for password policies in the AWS Console?

**Options:**
- **(A) Prevent passwords including the user’s last name** [CORRECT]
- (B) Enable password expiration
- (C) Require at least one number
- (D) Minimum password length

**Explanation:**
Prevent passwords including the user’s last name is the correct answer. You cannot prevent passwords including the user’s last name in the password policies for IAM. However, you can specify minimum password length, uppercase letters, lowercase letters, numbers, nonalphanumeric characters, voluntary user password changes, password expiration, prevent password reuse, and password expiration requires administrator reset.

---

## Question 37

**Q:** You are considering the use of encryption for an EBS volume. When should the encryption be applied?

**Options:**
- (A) When the EBS volume is detached from an instance
- (B) During OS installation within the instance that will use the EBS volume
- (C) When the EBS volume is attached to an instance
- **(D) At the time the EBS volume is created** [CORRECT]

**Explanation:**
At the time the EBS volume is created is the correct answer. If you choose to encrypt an EBS volume, it must be encrypted at the time of creation.

---

## Question 38

**Q:** What kind of storage is defined as data storage that persists only during the lifetime of an associated instance and that is lost when a drive fails, an instance stops, or an instance is terminated?

**Options:**
- **(A) Instance store** [CORRECT]
- (B) EFS
- (C) EBS volume

**Explanation:**
Instance store is the correct answer. The instance store is a temporary block storage solution for an instance. It holds temporary information such as buffers, caches, and scratch data. Instance stores are exposed as block devices known as ephemeral0 through ephemeral23 as needed, for a maximum of 24 instance stores per instance. EBS, EFS and S3 all provide permanent storage.

---

## Question 39

**Q:** You successfully configure VPC peering between VPC-A and VPC-B. You then establish an IGW and a Direct-Connect connection in VPC-B. Can instances in VPC-A connect to your corporate office via the Direct-Connect service as well as connect to the Internet via the IGW?

**Options:**
- (A) Instances in VPC-A will be able to access the corporate office but not the Internet.
- (B) Yes, VPC peering is designed to route traffic between the VPCs.
- (C) Instances in VPC-A will be able to access the Internet, but not the corporate office.
- **(D) No, VPC peering does not support edge-to-edge routing.** [CORRECT]

**Explanation:**
No, VPC peering does not support edge-to-edge routing is correct. The answer is no because VPC peering does not support edge-to-edge routing. Say, for example, that VPC-A is peered to VPC-B, and VPC-B is peered to VPC-C. In this case, VPC-A and VPC-C won’t be able to talk unless there is a peering between them. 

---


