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