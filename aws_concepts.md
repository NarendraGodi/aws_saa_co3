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