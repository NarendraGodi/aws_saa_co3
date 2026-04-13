# AWS SAA-C03 Concepts — Quick Revision Guide

---

## 📡 Networking

### 1. VPC (Virtual Private Cloud)
- **What**: Logically isolated virtual network in AWS. You control IP ranges, subnets, routing, and security.
- **Scope**: Regional (spans all AZs in a region). Subnets are AZ-specific.

#### Types of VPCs
| | Default VPC | Custom VPC |
|---|---|---|
| Created by | AWS automatically | You |
| CIDR | `172.31.0.0/16` | You define it |
| Internet Access | ✅ Pre-configured | ❌ Must configure |
| Use for | Dev/Testing | ✅ Production |

#### Key Points
- Max **5 VPCs per region** (soft limit)
- CIDR block **cannot be changed** after creation
- **Security Groups** = Stateful (instance-level)
- **NACLs** = Stateless (subnet-level)
- **VPC Peering** = Non-transitive (A↔B, B↔C ≠ A↔C)
- Resources talk to each other via **private IPs** (no IGW needed)

---

### 2. Subnets
- A **subnet** is a subdivision of a VPC's CIDR block, tied to a **single AZ**.
- You deploy resources (EC2, RDS, etc.) into subnets, not directly into VPCs.

#### Types of Subnets
| | Public Subnet | Private Subnet |
|---|---|---|
| **Internet Access** | Direct via IGW | Outbound only via NAT Gateway |
| **Public IP** | Auto-assigned (if configured) | ❌ Not assigned |
| **Use for** | Web servers, Load Balancers | Databases, App servers |

#### Key Points
- A subnet **belongs to exactly one AZ**
- **Public subnet** = route table has a route to an **Internet Gateway (IGW)**
- **Private subnet** = NO route to IGW; uses **NAT Gateway** for outbound internet
- **Reserved IPs per subnet**: AWS reserves **5 IPs** (first 4 + last 1) in every subnet
  - e.g., in `10.0.0.0/24` → `.0, .1, .2, .3` and `.255` are reserved → only **251 usable IPs**
- Subnet CIDR must be a **subset** of the VPC CIDR
- One subnet = one AZ, but one AZ can have **multiple subnets**

---

### 3. Route Table
- **What**: A set of rules (routes) that determines where network traffic is directed within a VPC.
- Every subnet **must be associated** with a route table.

#### How it works
| Destination | Target | Meaning |
|---|---|---|
| `10.0.0.0/16` | local | Traffic stays within the VPC |
| `0.0.0.0/0` | igw-xxxx | All other traffic → Internet Gateway |
| `0.0.0.0/0` | nat-xxxx | All other traffic → NAT Gateway |

#### Key Points
- Every VPC has a **Main Route Table** (default, auto-created)
- You can create **Custom Route Tables** and associate them with specific subnets
- A subnet with a route to an **IGW** = **Public Subnet**
- A subnet with a route to a **NAT Gateway** = **Private Subnet**
- **Most specific route wins** (longest prefix match)
- One route table can be associated with **multiple subnets**
- One subnet can only be associated with **one route table** at a time

---

### 4. Internet Gateway (IGW)
- **What**: A horizontally scaled, redundant, highly available VPC component that allows communication between your VPC and the internet.
- **Attached to**: VPC (one IGW per VPC)

#### Key Points
- Supports **both inbound and outbound** internet traffic
- **Free** to use (no hourly charge); you only pay for data transfer
- Must be **attached to the VPC** and the subnet's route table must have a route `0.0.0.0/0 → IGW`
- Performs **NAT** for instances with public IPs
- **Highly available** by default — no need to manage redundancy

---

### 5. NAT Gateway
- **What**: A managed AWS service that allows instances in a **private subnet** to initiate **outbound** internet traffic, without allowing inbound connections from the internet.
- **Lives in**: A **public subnet** (needs an Elastic IP)

#### Key Points
- **Outbound only** — internet cannot initiate connections to private instances
- **Managed by AWS** — no patching, no maintenance
- **AZ-specific** — for HA, deploy one NAT Gateway **per AZ**
- Charged **per hour + per GB** of data processed
- Private subnet route table: `0.0.0.0/0 → NAT Gateway`

---

### IGW vs NAT Gateway
| | Internet Gateway (IGW) | NAT Gateway |
|---|---|---|
| **Traffic Direction** | Inbound + Outbound | Outbound only |
| **Used by** | Public subnet resources | Private subnet resources |
| **Public IP needed** | Yes (on the instance) | Yes (Elastic IP on NAT GW itself) |
| **Cost** | Free (data transfer charges) | Hourly + per GB |
| **Managed by** | AWS (auto HA) | AWS (per AZ) |
| **Use case** | Web servers, public-facing apps | Patching private EC2s, downloading updates |

---

### 6. VPC DNS Settings (Enable DNS Support and Enable DNS Hostnames)

#### Enable DNS Support
- **What**: Enables DNS resolution inside the VPC using AWS built-in DNS server at **VPC CIDR base + 2** (e.g., `10.0.0.2`)
- **Default**: Enabled in both Default and Custom VPCs
- **When enabled**: Instances can resolve AWS service hostnames (e.g., `s3.amazonaws.com`) and internal VPC hostnames to IP addresses

#### Enable DNS Hostnames
- **What**: Assigns a **public DNS hostname** (e.g., `ec2-54-23-1-2.compute-1.amazonaws.com`) to instances that have a public IP address
- **Default**: Enabled in Default VPC | Disabled in Custom VPC
- **When enabled**: Instances with public IPs get a human-readable public DNS name, useful for connecting to them by hostname instead of IP

#### Key Points
- **Both must be ON** for instances to receive public DNS hostnames
- If `DNS Support = OFF` DNS resolution fails entirely in the VPC
- If `DNS Support = ON` but `DNS Hostnames = OFF` Instances resolve names but do not get public DNS hostnames
- Both settings are **required** when associating a **Route 53 Private Hosted Zone** with the VPC

#### Summary Table
| Setting | Default VPC | Custom VPC | When to Enable |
|---|---|---|---|
| **DNS Support** | On | On | Always needed for any DNS resolution in VPC |
| **DNS Hostnames** | On | Off | When instances need public DNS names, or using Route 53 Private Hosted Zones |

---

### 7. Elastic IP (EIP)
- **What**: A **static, public IPv4 address** that you own and can attach/detach to AWS resources (EC2, NAT Gateway, etc.) at any time.
- **Why**: Normal public IPs on EC2 instances **change every time** the instance is stopped/started. Elastic IPs stay fixed.

#### Key Points
- **Static** — the IP does not change even if you stop/start the instance
- **Tied to your account** — not to a specific instance; you allocate it and assign it
- Can be **remapped instantly** to another instance (useful for failover)
- **Free** when associated with a running instance
- **Charged** when allocated but **NOT associated** with a running instance (~$0.005/hr)
- Max **5 Elastic IPs per region** (soft limit)
- **Required** by NAT Gateway — each NAT GW needs one Elastic IP

#### Normal Public IP vs Elastic IP
| | Normal Public IP | Elastic IP |
|---|---|---|
| **Persistence** | Changes on stop/start | Static, never changes |
| **Cost** | Free | Free if in use, charged if idle |
| **Remappable** | No | Yes |
| **Use case** | Temporary/dev instances | Production, NAT Gateway, failover |

---

### 8. Security Groups vs NACLs

#### Security Groups (SG)
- **What**: A virtual **stateful firewall** at the **instance level** (EC2, RDS, Lambda, etc.)
- **Stateful**: Return traffic is **automatically allowed** — you only need to define inbound OR outbound rules
- **Default**: Allows all outbound, denies all inbound
- Rules are **allow only** — you cannot explicitly deny traffic

#### NACLs (Network Access Control Lists)
- **What**: A virtual **stateless firewall** at the **subnet level**
- **Stateless**: Return traffic must be **explicitly allowed** in both directions
- **Default NACL**: Allows ALL inbound and outbound traffic
- **Custom NACL**: Denies ALL traffic until you add rules
- Rules are **numbered** and evaluated in order (lowest number first)
- Can have both **allow and deny** rules

#### Key Comparison
| | Security Group | NACL |
|---|---|---|
| **Level** | Instance | Subnet |
| **State** | Stateful | Stateless |
| **Rules** | Allow only | Allow + Deny |
| **Rule evaluation** | All rules evaluated | Rules evaluated in number order |
| **Return traffic** | Auto-allowed | Must explicitly allow |
| **Default** | Deny all inbound, Allow all outbound | Allow all (default NACL) |
| **Association** | Assigned to instances | Assigned to subnets |
| **Use case** | Fine-grained instance-level control | Broad subnet-level control, block IPs |

#### Key Points
- **First line of defense** = NACL (subnet level) then **Second line** = Security Group (instance level)
- Use NACLs to **block specific IPs** (e.g., block a malicious IP) — SGs cannot deny
- A single SG can be applied to **multiple instances**
- A subnet can only have **one NACL** at a time
- **Ephemeral ports** (1024-65535) must be allowed in NACL outbound rules for return traffic

---

### 9. Load Balancer (ELB — Elastic Load Balancing)
- **What**: Distributes incoming traffic across multiple targets (EC2, containers, IPs, Lambda) for **high availability**, **fault tolerance**, and **scalability**.
- **Managed by AWS** — no infrastructure to maintain

#### Types of Load Balancers

| | ALB | NLB | GWLB | CLB |
|---|---|---|---|---|
| **Layer** | 7 (HTTP/HTTPS) | 4 (TCP/UDP/TLS) | 3 (IP) | 4 and 7 |
| **Routes by** | URL, headers, query strings | IP + Port | IP packets | Basic HTTP/TCP |
| **Use for** | Web apps, APIs, microservices | Low latency, high throughput | Security appliances | Legacy only |
| **Static IP** | No | Yes (Elastic IP) | No | No |
| **Lambda target** | Yes | No | No | No |
| **Status** | Current | Current | Current | Deprecated |

#### 1. Application Load Balancer (ALB)
- Routes based on **URL path** (`/api` vs `/images`), **host headers**, query strings, HTTP methods
- Supports **WebSockets**, HTTP/2, **Lambda** as target, **sticky sessions**
- Best for: Web apps, microservices, containers (ECS/EKS)

#### 2. Network Load Balancer (NLB)
- Operates at **TCP/UDP** level — extremely **low latency** (millions of req/sec)
- Supports **static/Elastic IPs** — useful when clients need a fixed IP
- Best for: Gaming, IoT, financial apps, VPN

#### 3. Gateway Load Balancer (GWLB)
- Routes traffic **transparently** through third-party virtual appliances (firewalls, IDS/IPS)
- Uses **GENEVE protocol** on port 6081
- Best for: Network security inspection before traffic reaches your app

#### 4. Classic Load Balancer (CLB) - Legacy
- Old generation, supports basic HTTP/TCP load balancing
- **Deprecated** — migrate to ALB or NLB

#### Key Points
- All ELBs support **health checks** — automatically stop sending traffic to unhealthy targets
- ALB and NLB support **target groups** (EC2, IP, Lambda, containers)
- NLB preserves the **client source IP**; ALB does not (uses `X-Forwarded-For` header)
- ELBs are **regional** and span multiple AZs for HA
- **Cross-zone load balancing**: Distributes traffic evenly across all targets in all AZs
  - ALB: Enabled by default | NLB/GWLB: Disabled by default (extra charge if enabled)

---

### 10. VPC Connectivity Options

#### 1. VPN (Site-to-Site VPN)
- **What**: Encrypted tunnel over the **public internet** between your on-premises network and AWS VPC
- **Components**: **Customer Gateway** (your side) + **Virtual Private Gateway** (AWS side)
- **Speed**: Up to **1.25 Gbps**, higher latency (goes over internet)
- **Setup time**: Fast (minutes to hours)
- **Cost**: Low (pay per VPN connection hour + data transfer)
- **When to use**: Quick setup, cost-effective on-premises to AWS connectivity, backup for Direct Connect

#### 2. Direct Connect (DX)
- **What**: **Dedicated private physical connection** between your data center and AWS (bypasses internet entirely)
- **Speed**: 1 Gbps, 10 Gbps, 100 Gbps
- **Setup time**: Slow (weeks to months — physical provisioning required)
- **Cost**: Higher (port hours + data transfer)
- **When to use**: High bandwidth, consistent low latency, large data transfers, compliance/regulatory requirements

#### 3. Transit Gateway (TGW)
- **What**: A **central hub** (cloud router) that connects multiple VPCs, VPNs, and Direct Connect connections
- **Analogy**: Instead of peering every VPC with every other (NxN connections), connect all to TGW (N connections)
- **Scope**: Regional, but supports **cross-region peering**
- **When to use**: 3+ VPCs to connect, hub-and-spoke architecture, cross-region or cross-account connectivity

#### 4. VPC Peering
- **What**: A **direct private connection** between **two VPCs** using AWS backbone (no internet, no gateway needed)
- **Limitation**: **Non-transitive** — A-B and B-C does NOT give A-C connectivity
- **Supports**: Same account, cross-account, cross-region
- **When to use**: Simple 1-to-1 VPC connectivity, small number of VPCs

#### 5. PrivateLink (VPC Endpoints)
- **What**: Exposes a **service privately** to other VPCs without VPC peering, internet, or NAT — traffic stays within AWS network
- **Types**:
  - **Interface Endpoint** (PrivateLink): Creates a private IP (ENI) in your subnet to reach AWS services or your own services
  - **Gateway Endpoint**: Route-table based, for **S3** and **DynamoDB** only (free)
- **When to use**: Access AWS services (S3, SSM, SQS, etc.) privately, expose your own service securely to other VPCs/accounts

#### When to Use What?
| Scenario | Use |
|---|---|
| Connect on-premises to AWS quickly and cheaply | **VPN** |
| Connect on-premises to AWS with high speed and low latency | **Direct Connect** |
| VPN + redundancy/failover | **Direct Connect + VPN as backup** |
| Connect 3+ VPCs together | **Transit Gateway** |
| Connect 2 VPCs privately | **VPC Peering** |
| Access S3/DynamoDB without internet | **Gateway Endpoint** |
| Access AWS services (SSM, SQS, etc.) privately via private IP | **Interface Endpoint (PrivateLink)** |
| Expose your own service privately to other accounts/VPCs | **PrivateLink** |

#### Key Points
- VPC Peering is **simpler but does not scale** — use Transit Gateway for many VPCs
- Direct Connect is **not encrypted by default** — combine with VPN for encryption over DX
- PrivateLink does **not require CIDR overlap** resolution — works even with overlapping CIDRs
- Gateway Endpoints are **free**; Interface Endpoints are **charged per hour + per GB**
- Transit Gateway supports **multicast** and **inter-region peering**

---