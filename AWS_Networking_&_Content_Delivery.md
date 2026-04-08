## AWS Services Reference

| Service | Description |
|---------|-------------|
| AWS Global Accelerator | A service that improves the availability and performance of your applications with static IP addresses as a fixed entry point to your application endpoints. |
| Amazon CloudFront | A content delivery network (CDN) that securely delivers data, videos, applications, and APIs to customers globally with low latency and high transfer speeds. |
| Amazon Route 53 | A scalable Domain Name System (DNS) web service designed to provide highly reliable and cost-effective routing. |
| Amazon VPC | A service that lets you provision a logically isolated section of the AWS cloud where you can launch AWS resources in a virtual network that you define. |
| VPC Peering | A networking connection between two VPCs that enables you to route traffic between them privately using IPv4 or IPv6 addresses. |
| VPC Endpoints (Gateway/Interface) | Allow you to connect to AWS services without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. |
| AWS PrivateLink | A technology that enables you to privately connect your VPC to supported AWS services and VPC endpoint services without exposing your traffic to the public internet. |
| AWS Direct Connect | A cloud service that makes it easy to establish a dedicated network connection from your premises to AWS. |
| AWS Site-to-Site VPN | A service that allows you to securely connect your on-premises network or branch office site to your Amazon VPC. |
| AWS Client VPN | A managed client-based VPN service that allows you to securely access your AWS resources from any location using an OpenVPN-based VPN client. |
| Elastic Load Balancing (ALB/NLB) | Automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, and IP addresses. |
| Amazon S3 Transfer Acceleration | A feature that enables faster data transfers to and from Amazon S3 by using Amazon CloudFront's globally distributed edge locations. |
| Amazon S3 Multi-Region Access Points | A feature that simplifies performance and availability for applications that retrieve data from multiple AWS Regions. |
| Amazon FSx | A fully managed file system that makes it easy to launch and run file systems in the cloud. |
| AWS DataSync | A data transfer service that simplifies, automates, and accelerates copying large amounts of data to and from AWS storage services. |
| AWS CloudTrail | A service that enables governance, compliance, and operational and risk auditing of your AWS account. |
| Amazon EKS | A fully managed Kubernetes service that makes it easy to run Kubernetes on AWS without needing to install and operate your own Kubernetes control plane. |
| EC2 Auto Scaling | A service that automatically adjusts the number of Amazon EC2 instances in your application according to demand. |
| EC2 Instance Store | Temporary storage that is located on disks that are physically attached to the host computer of your EC2 instance. |

---

## AWS Networking & Content Delivery – Practice Questions

### Question 1 (Networking)

**Q:** What should you do to ensure all traffic to your VPC resources is secured?

**Options:**  
- **✅ Configure VPNs or Direct Connect**  
- Configure only Security Groups  
- Configure only NACLs  
- Disable all public access

**A:** VPNs provide secure connectivity.  

**Explanation:**  
- **CORRECT:** VPNs and Direct Connect ensure that your resources are not exposed to the public internet.  
- **INCORRECT:** Security Groups and NACLs alone do not secure traffic at the network level.  

**References:**  
- AWS Documentation on VPC Security
- AWS Best Practices for Networking

### Question 2 (CDN)

**Q:** How can you accelerate content delivery to users worldwide?

**Options:**  
- **✅ Use Amazon CloudFront**  
- Implement only Route 53  
- Use only Elastic Load Balancers  
- Utilize VPC Peering only

**A:** Amazon CloudFront provides global content delivery.  

**Explanation:**  
- **CORRECT:** CloudFront caches content at edge locations for faster access.  
- **INCORRECT:** Other options do not provide the same level of content caching and distribution.  

**References:**  
- Amazon CloudFront Developer Guide
- AWS Whitepapers on CDN

### Question 3 (AWS Services)

**Q:** Which AWS service can help with managing your VPC peering connections?

**Options:**  
- **✅ Use AWS Management Console**  
- AWS CLI only  
- Only SDKs  
- Use CloudFormation exclusively

**A:** The AWS Management Console provides the necessary interface.  

**Explanation:**  
- **CORRECT:** The console allows for easy visualization and management of VPC connections.  
- **INCORRECT:** CLI and SDKs may not have all the features available in the console.  

**References:**  
- VPC Peering Guide
- AWS Management Console Documentation
