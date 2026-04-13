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