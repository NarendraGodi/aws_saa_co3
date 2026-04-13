# AWS Networking & Content Delivery

## Introduction
AWS provides a variety of networking and content delivery services that allow you to create robust, scalable, and flexible architectures. This document covers the key services and best practices for AWS networking.

---

## VPC (Virtual Private Cloud)

### What is a VPC?
A **Virtual Private Cloud (VPC)** is a logically isolated, private virtual network within the AWS Cloud. It allows you to launch AWS resources (EC2 instances, RDS databases, Lambda, etc.) in a network that **you define and control** — just like a traditional on-premises data center network, but in the cloud.

- **Scope**: VPCs are **regional** — they span all Availability Zones (AZs) within a region.
- **IP Addressing**: You define a **CIDR block** (e.g., `10.0.0.0/16`) for your VPC when creating it.
- **Isolation**: Resources inside a VPC are isolated from other VPCs and the internet by default.
- **Customization**: You control routing, subnets, gateways, and security settings.

### Key Components of a VPC
| Component | Description |
|---|---|
| **Subnets** | Subdivisions of a VPC tied to a specific AZ. Can be public or private. |
| **Route Tables** | Define how traffic is routed within the VPC and to outside networks. |
| **Internet Gateway (IGW)** | Enables internet access for resources in public subnets. |
| **NAT Gateway** | Allows private subnet resources to access the internet without being directly exposed. |
| **Security Groups** | Stateful, instance-level virtual firewalls. |
| **Network ACLs (NACLs)** | Stateless, subnet-level firewalls. |
| **VPC Peering** | Connects two VPCs privately using AWS network. |
| **Endpoints** | Allows private access to AWS services without traversing the internet. |

### Types of VPCs

#### 1. 🟦 Default VPC
- **Automatically created** by AWS in every region for every AWS account.
- Comes pre-configured with:
  - A default CIDR block: `172.31.0.0/16`
  - A default subnet in **each AZ** of the region
  - An **Internet Gateway** already attached
  - A default route table with internet access
- Resources launched in the default VPC get both **public and private IP addresses** automatically.
- **Use case**: Quick testing, development, and getting started with AWS.
- ⚠️ **Not recommended** for production workloads due to lack of customization and security isolation.

#### 2. 🟩 Custom VPC (Non-Default VPC)
- **Manually created** by the user with full control over configuration.
- You define:
  - Your own **CIDR block** (e.g., `10.0.0.0/16`)
  - **Public and private subnets** across AZs
  - **Routing rules**, gateways, and security policies
- No internet access by default — you must explicitly add an Internet Gateway and configure routes.
- **Use case**: Production workloads, multi-tier architectures, secure and isolated environments.
- ✅ **Recommended** for all serious/production deployments.

### Public vs Private Subnets (within a VPC)
| | Public Subnet | Private Subnet |
|---|---|---|
| **Internet Access** | Direct via Internet Gateway | Via NAT Gateway only (outbound) |
| **Use Case** | Web servers, load balancers | Databases, application servers |
| **Public IP** | Assigned automatically (if configured) | Not assigned |

### Important Points for SAA-C03 Exam
- A VPC **spans all AZs** in a region; subnets are **AZ-specific**.
- You can have up to **5 VPCs per region** by default (soft limit, can be increased).
- VPC **CIDR blocks cannot be changed** after creation (but secondary CIDRs can be added).
- **Security Groups are stateful** (return traffic is automatically allowed); **NACLs are stateless** (you must explicitly allow inbound AND outbound).
- **VPC Peering** is non-transitive — if VPC A peers with B and B peers with C, A cannot communicate with C unless directly peered.
- **Default VPC** can be deleted but AWS recommends keeping it; it can also be recreated.
- Resources in a VPC can communicate with each other using **private IPs** without needing an internet gateway.

---

## Route 53
- **Description**: Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service.
- **Best Practices**:
  - Use health checks to route traffic to healthy endpoints.
  - Implement latency-based routing for optimal user experience.

## CloudFront
- **Description**: Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency and high transfer speeds.
- **Best Practices**:
  - Enable caching for static content.
  - Use signed URLs for secured content delivery.

## Elastic Load Balancing (ELB)
- **Description**: ELB automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances.
- **Best Practices**:
  - Use application load balancers for HTTP/HTTPS traffic.
  - Monitor instance health and automatically remove unhealthy instances.

## Conclusion
By employing these AWS networking and content delivery services and following best practices, you can build scalable and efficient applications.