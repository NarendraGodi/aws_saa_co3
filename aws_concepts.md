### 9. Load Balancer (ELB — Elastic Load Balancing)
- **What**: Distributes incoming traffic across multiple targets (EC2, containers, IPs, Lambda) for **high availability**, **fault tolerance**, and **scalability**.
- **Managed by AWS** — no infrastructure to maintain

#### Types of Load Balancers

| | ALB | NLB | GWLB | CLB |
|---|---|---|---|---|
| **Layer** | 7 (HTTP/HTTPS) | 4 (TCP/UDP/TLS) | 3 (IP) | 4 & 7 |
| **Routes by** | URL, headers, query strings | IP + Port | IP packets | Basic HTTP/TCP |
| **Use for** | Web apps, APIs, microservices | Low latency, high throughput | Security appliances | Legacy only |
| **Static IP** | ❌ | ✅ (Elastic IP) | ❌ | ❌ |
| **Lambda target** | ✅ | ❌ | ❌ | ❌ |
| **Status** | ✅ Current | ✅ Current | ✅ Current | ⚠️ Deprecated |

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

#### 4. Classic Load Balancer (CLB) ⚠️ Legacy
- Old generation, supports basic HTTP/TCP load balancing
- **Deprecated** — migrate to ALB or NLB

#### Key Points
- All ELBs support **health checks** — automatically stop sending traffic to unhealthy targets
- ALB & NLB support **target groups** (EC2, IP, Lambda, containers)
- NLB preserves the **client source IP**; ALB does not (uses `X-Forwarded-For` header)
- ELBs are **regional** and span multiple AZs for HA
- **Cross-zone load balancing**: Distributes traffic evenly across all targets in all AZs
  - ALB: ✅ Enabled by default | NLB/GWLB: ❌ Disabled by default (extra charge if enabled)

---