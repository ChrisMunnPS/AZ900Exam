# AZ-900 cheat sheet 2/3 — Azure architecture and services

*One page. Facts snapshot 2026-11; verify current behaviour on Microsoft Learn before the exam.*

## Physical and management structure

| Item | What to remember |
|---|---|
| **Region** | Geographic area with one or more datacenters connected by a low-latency network. Most resources are regional. |
| **Availability zone** | Physically separate datacenter group in a region with independent power, cooling, and networking. Zone-enabled regions have **at least three**. |
| **Region pair** | Two regions in the same geography at least **300 miles** apart; updates roll out one at a time and data stays in the geography (Brazil South excepted). |
| **Sovereign region** | Isolated Azure instance (US Government, China via 21Vianet). |
| **Global services** | Microsoft Entra ID, Azure DNS, and Azure Traffic Manager are not tied to one region. |
| **Resource group** | Flat container; a resource is in exactly one group; deleting the group deletes its contents. |
| **Subscription** | Billing and access-control boundary; one tenant can have many subscriptions. |
| **Management group** | Groups subscriptions for inherited policy and access; up to 6 levels below the root, 10,000 per directory, one parent. |
| **Hierarchy** | Tenant root → management groups → subscriptions → resource groups → resources. |

## Compute

| Service | Use it for |
|---|---|
| **Virtual Machines** | Full OS control, lift and shift, legacy apps, custom software. You patch the guest OS. |
| **VM scale sets** | Identical, load-balanced VMs that scale out and in automatically. |
| **Availability sets** | Spread VMs across fault domains and update domains inside one datacenter. |
| **Container Instances** | Fastest way to run one container; no orchestration; per-second billing. |
| **Azure Kubernetes Service** | Orchestrate a large fleet of containers. |
| **Azure Functions** | Event-driven serverless code; pay per execution; Durable Functions keep state. |
| **App Service** | PaaS web apps, APIs, mobile back ends, WebJobs; deployment slots and autoscaling. |
| **Azure Virtual Desktop** | Managed Windows desktops and apps streamed to users. |

**VM families:** B burstable · D general · E memory · F compute · M large memory · L storage · N GPU.

## Networking

| Service | What it does |
|---|---|
| **Virtual network (VNet)** | Private IP networking; isolation, segmentation, routing. Subnets divide the address space. |
| **Network security group** | Allow/deny rules by priority on a subnet or NIC. |
| **VPN Gateway** | Encrypted site-to-site, point-to-site, or VNet-to-VNet tunnel over the internet. |
| **ExpressRoute** | Private dedicated circuit that does not traverse the public internet. |
| **Azure DNS** | Public zone hosting; private zones resolve names inside VNets. |
| **Load Balancer** | Layer 4 (TCP/UDP) distribution with health probes. |
| **Application Gateway** | Layer 7 reverse proxy: URL path routing, TLS termination, optional WAF. |
| **Front Door** | Global anycast HTTP entry: latency routing, failover, caching, edge WAF. |

## Storage

| Service | What it holds |
|---|---|
| **Blob storage** | Unstructured objects: images, video, backups, logs. Tiers: hot, cool (30-day min), cold (90-day min), archive (180-day min, offline). |
| **Azure Files** | Managed SMB and NFS file shares, mountable by Windows, Linux, and macOS. |
| **Queue storage** | Messages that decouple application components. |
| **Table storage** | NoSQL key-value store for structured, non-relational data. |
| **Storage account** | 3–24 characters, lowercase letters and numbers only, globally unique; sets region, performance, and redundancy. |

**Redundancy:** LRS = 3 copies in one datacenter · ZRS = 3 zones in one region · GRS = LRS plus asynchronous copies in the paired region · RA-GRS = GRS plus a readable secondary · GZRS = ZRS plus region copies.

## Identity and security

| Item | What to remember |
|---|---|
| **Microsoft Entra ID** | Cloud identity provider for users, groups, apps, and devices. |
| **Authentication vs authorization** | Authentication proves identity; authorization decides what is allowed. |
| **MFA** | Two or more factor types: know (password), have (authenticator), are (biometrics). |
| **Conditional Access** | If-then sign-in policy using user, device, location, app, and risk signals. |
| **Single sign-on** | One authentication for many applications. |
| **B2B / B2C** | B2B invites partners as guests; B2C serves consumer identities in your apps. |
| **RBAC** | Role assignment at management group, subscription, resource group, or resource. |

## AI and IoT

| Service | Use it for |
|---|---|
| **Azure AI services** | Prebuilt vision, speech, language, and document APIs — no model training. |
| **Azure OpenAI** | Generative AI chat and content with Azure security and governance. |
| **Azure Machine Learning** | Build, train, and manage custom models. |
| **IoT Hub** | Secure bidirectional device-to-cloud and cloud-to-device messaging. |
| **IoT Central** | Simplified SaaS IoT platform for solution builders. |
| **IoT Edge** | Run cloud workloads close to devices. |

## Exam traps

- Zones protect inside a region; region pairs protect across regions.
- Peering is not transitive — not an AZ-900 focus, but useful context.
- A resource belongs to one resource group, and groups cannot be nested.
- Storage account names cannot contain uppercase letters, hyphens, or underscores.
- Load Balancer is layer 4; Application Gateway is regional layer 7; Front Door is global layer 7.
