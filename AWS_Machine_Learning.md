## AWS Services Reference

| Service | Description |
|---|---|
| **Amazon DynamoDB** | A fully managed, serverless NoSQL key-value and document database that delivers single-digit millisecond performance at any scale. |
| **Amazon VPC (Virtual Private Cloud)** | A service that lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network you define. |
| **VPC Gateway Endpoint** | A gateway that you specify in your route table to allow traffic to Amazon S3 or DynamoDB without requiring an internet gateway, NAT device, or VPN connection. |
| **VPC Interface Endpoint** | An elastic network interface (ENI) with a private IP address that serves as an entry point for traffic to supported AWS services via AWS PrivateLink. |
| **AWS VPN** | A managed service that establishes encrypted tunnels between your on-premises network or client devices and your Amazon VPC. |
| **VPC Peering** | A networking connection between two VPCs that enables routing of traffic between them using private IPv4 or IPv6 addresses. |
| **AWS Transit Gateway** | A network transit hub that interconnects multiple VPCs and on-premises networks through a central gateway, simplifying network architecture. |
| **Amazon EC2 (Elastic Compute Cloud)** | A web service that provides secure, resizable compute capacity in the cloud, allowing you to run virtual servers on demand. |
| **Amazon Machine Image (AMI)** | A pre-configured template containing the software configuration (OS, application server, and applications) required to launch an EC2 instance. |
| **Amazon EBS Snapshots** | Point-in-time copies of Amazon EBS volumes stored in Amazon S3, used for backup, disaster recovery, and volume creation. |
| **Amazon S3 (Simple Storage Service)** | An object storage service offering industry-leading scalability, data availability, security, and performance for storing and retrieving any amount of data. |

---

## AWS Machine Learning – Practice Questions

---

### Question 34

**Q:** An application in a private subnet needs to query data in an Amazon DynamoDB table. Use of the DynamoDB public endpoints must be avoided. What is the most EFFICIENT and secure method of enabling access to the table?

**Options:**

- Create a private Amazon DynamoDB endpoint and connect to it using an AWS VPN
- **✅ Create a gateway VPC endpoint and add an entry to the route table**
- Create an interface VPC endpoint in the VPC with an Elastic Network Interface (ENI)
- Create a software VPN between DynamoDB and the application in the private subnet

**A:** **Create a gateway VPC endpoint and add an entry to the route table**

**Explanation:**

A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection.

Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.

With a gateway endpoint, you configure your route table to point to the endpoint. Amazon S3 and DynamoDB use gateway endpoints.

- **CORRECT:** "Create a gateway VPC endpoint and add an entry to the route table" is the correct answer.
- **INCORRECT:** "Create an interface VPC endpoint in the VPC with an Elastic Network Interface (ENI)" is incorrect — this would be used for services supported by interface endpoints, not gateway endpoints.
- **INCORRECT:** "Create a private Amazon DynamoDB endpoint and connect to it using an AWS VPN" is incorrect — you cannot create an Amazon DynamoDB private endpoint and connect to it over VPN. Private endpoints are VPC endpoints connected via route table entries or ENIs depending on the service.
- **INCORRECT:** "Create a software VPN between DynamoDB and the application in the private subnet" is incorrect — you cannot create a software VPN between DynamoDB and an application.

**References:**
- https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html
- https://digitalcloud.training/amazon-vpc/

---

### Question 45

**Q:** An international logistics company has web applications running on AWS in the us-west-2 Region and database servers in the eu-central-1 Region. The applications running in a VPC in us-west-2 need to communicate securely with the databases running in a VPC in eu-central-1. Which network design will meet these requirements?

**Options:**

- Create a VPC peering connection between the us-west-2 VPC and the eu-central-1 VPC. Add the appropriate routes to the subnet route tables. Create an inbound rule in the us-west-2 application security group that allows traffic from the eu-central-1 database server IP addresses.
- Establish a VPC peering connection between the us-west-2 VPC and the eu-central-1 VPC. Modify the subnet route tables accordingly. Create an inbound rule in the eu-central-1 database security group that references the security group ID of the application servers in us-west-2.
- Establish a transit gateway with a peering attachment between the us-west-2 VPC and the eu-central-1 VPC. After the transit gateways are properly peered and routing is configured, create an inbound rule in the eu-central-1 database security group that references the security group ID of the application servers in us-west-2.
- **✅ Configure a VPC peering connection between the us-west-2 VPC and the eu-central-1 VPC. Update the subnet route tables accordingly. Create an inbound rule in the eu-central-1 database security group that allows traffic from the us-west-2 application server IP addresses.**

**A:** **Configure a VPC peering connection between the us-west-2 VPC and the eu-central-1 VPC. Update the subnet route tables accordingly. Create an inbound rule in the eu-central-1 database security group that allows traffic from the us-west-2 application server IP addresses.**

**Explanation:**

The correct solution establishes a VPC peering connection between the two regions, and it properly sets up the inbound rule in the eu-central-1 database security group to allow traffic from the us-west-2 application server IP addresses, which is the correct way to configure this as security groups can't be referenced across regions.

- **CORRECT:** "Configure a VPC peering connection between the us-west-2 VPC and the eu-central-1 VPC. Update the subnet route tables accordingly. Create an inbound rule in the eu-central-1 database security group that allows traffic from the us-west-2 application server IP addresses" is the correct answer.
- **INCORRECT:** "Establish a VPC peering connection... Create an inbound rule... that references the security group ID of the application servers in us-west-2" is incorrect — you cannot reference a security group from another region. Security groups are region-specific and can only be referenced within the same region.
- **INCORRECT:** "Create a VPC peering connection... Create an inbound rule in the us-west-2 application security group..." is incorrect — the inbound rule should be configured in the eu-central-1 database security group to allow traffic from us-west-2, not the other way around.
- **INCORRECT:** "Establish a transit gateway with a peering attachment... that references the security group ID of the application servers in us-west-2" is incorrect — you cannot reference a security group from another region. Security groups are region-specific and can only be referenced within the same region.

**References:**
- https://docs.aws.amazon.com/vpc/latest/peering/vpc-peering-security-groups.html
- https://digitalcloud.training/amazon-vpc/

---

### Question 18

**Q:** The Solutions Architect in charge of a critical application must ensure the Amazon EC2 instances are able to be launched in another AWS Region in the event of a disaster. What steps should the Solutions Architect take? (Select TWO.)

**Options:**

- Enable cross-region snapshots for the Amazon EC2 instances
- Copy the snapshots using Amazon S3 cross-region replication
- Launch instances in the second Region using the S3 API
- **✅ Create AMIs of the instances and copy them to another Region**
- **✅ Launch instances in the second Region from the AMIs**

**A:** **Create AMIs of the instances and copy them to another Region** and **Launch instances in the second Region from the AMIs**

**Explanation:**

You can create AMIs of the EC2 instances and then copy them across Regions. This provides a point-in-time copy of the state of the EC2 instance in the remote Region.

Once you've created AMIs of EC2 instances and copied them to the second Region, you can then launch the EC2 instances from the AMIs in that Region.

This is a good DR strategy as you have moved stateful EC2 instances to another Region.

- **CORRECT:** "Create AMIs of the instances and copy them to another Region" is the correct answer.
- **CORRECT:** "Launch instances in the second Region from the AMIs" is also a correct answer.
- **INCORRECT:** "Launch instances in the second Region using the S3 API" is incorrect — though snapshots (and EBS-backed AMIs) are stored on Amazon S3, you cannot actually access them using the S3 API. You must use the EC2 API.
- **INCORRECT:** "Enable cross-region snapshots for the Amazon EC2 instances" is incorrect — you cannot enable "cross-region snapshots" as this is not a feature that currently exists.
- **INCORRECT:** "Copy the snapshots using Amazon S3 cross-region replication" is incorrect — you cannot work with snapshots using Amazon S3 at all, including leveraging the cross-region replication feature.

**References:**
- https://aws.amazon.com/blogs/aws/ebs-snapshot-copy/
- https://digitalcloud.training/amazon-ec2/
