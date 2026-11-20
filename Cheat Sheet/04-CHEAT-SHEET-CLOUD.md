# AZ-900 cheat sheet 1/3 — Describe cloud concepts

*One page. Facts snapshot 2026-11; verify current behaviour on Microsoft Learn before the exam.*

## What cloud computing is

| Item | What to remember |
|---|---|
| Definition | Delivery of computing services — compute, storage, networking, databases, AI — over the internet, usually with consumption-based pricing. |
| Provider responsibilities | Physical datacenters, hosts, storage hardware, and the global network. |
| Customer responsibilities | Data, identities, access, and the configuration of whatever the service exposes. |
| Consumption model | Pay for what you use; release the resource and the meter stops. No upfront hardware purchase. |
| CapEx vs OpEx | Buying servers is capital expenditure; cloud usage is operating expenditure that follows demand. |
| Economies of scale | Providers buy and operate at massive scale, lowering the cost per unit for customers. |

## Deployment models

| Model | What it means | Typical reason |
|---|---|---|
| **Public cloud** | Provider-owned, multi-tenant, delivered over the internet. Azure, Microsoft 365. | Lowest operations, elastic scale, no hardware. |
| **Private cloud** | Cloud-style pooling dedicated to one organisation, on site or hosted. | Strict control, single tenancy. |
| **Hybrid cloud** | Private or on-premises connected to public cloud. | Regulation, latency, or legacy systems keep some data on site. |
| **Multi-cloud** | Services from more than one public provider. | Avoid lock-in, best-of-breed services. |
| **Sovereign cloud** | Isolated Azure instance for legal or compliance reasons (US Government, China). | Data sovereignty and screened personnel. |

## Service models

| Model | You manage | Microsoft manages | Examples |
|---|---|---|---|
| **IaaS** | OS, runtime, apps, data, network config | Hosts, storage, virtualization, physical network | Azure Virtual Machines, managed disks |
| **PaaS** | App code, data, some configuration | OS, runtime, scaling, patching, servers | App Service, Azure SQL Database, Functions |
| **SaaS** | Users, data, settings | The entire application and platform | Microsoft 365, Dynamics 365 |

**Rule of thumb:** if you patch the guest OS you are in IaaS; if you only bring code you are in PaaS; if you only configure a finished product you are in SaaS.

## Shared responsibility

| Layer | IaaS | PaaS | SaaS |
|---|---|---|---|
| Physical datacenter, hosts, network | Microsoft | Microsoft | Microsoft |
| Hypervisor and host OS | Microsoft | Microsoft | Microsoft |
| Guest OS and runtime | **Customer** | Microsoft | Microsoft |
| Application code | **Customer** | **Customer** | Microsoft |
| Data, identities, access | **Customer** | **Customer** | **Customer** |
| Device and account hygiene | **Customer** | **Customer** | **Customer** |

**Always customer:** data, accounts, permissions, and how the service is configured.
**Always Microsoft:** the physical and virtualization layer.

## Benefits and characteristics

| Term | Meaning |
|---|---|
| **High availability** | Minimal downtime through redundancy, health probes, and fast failover. |
| **Reliability** | Keeps working correctly and recovers from failures. |
| **Scalability** | Add or remove capacity: scale up (bigger) or scale out (more instances). |
| **Elasticity** | Automatic scaling that matches capacity to demand. |
| **Predictability** | Consistent performance and a forecastable cost. |
| **Agility** | Provision, change, and tear down resources in minutes. |
| **Geo-distribution** | Deploy to multiple regions to reduce latency for users. |
| **Disaster recovery** | Restore service and data after a major event; measured by RTO and RPO. |
| **Manageability** | Manage resources through the portal, CLI, PowerShell, APIs, and templates. |
| **Security and governance** | Central policy, identity, and compliance controls backed by provider certifications. |

## Resilience vocabulary

| Term | Plain meaning |
|---|---|
| **RTO** | Recovery time objective — how long the service may be down. |
| **RPO** | Recovery point objective — how much data loss is acceptable, measured in time. |
| **Fault tolerance** | The system keeps running when a component fails. |
| **Serverless** | Run code on demand without provisioning servers; pay per execution (Azure Functions). |

## Quick decision table

| Requirement | Choose |
|---|---|
| No hardware, elastic scale, no regulatory constraint | Public cloud |
| Some data must stay on site by law | Hybrid or private cloud |
| Avoid dependence on one provider | Multi-cloud |
| Legally isolated Azure instance | Sovereign region |
| Need OS control or lift and shift | IaaS |
| Deploy code, no OS management | PaaS |
| Finished app, configure only | SaaS |
| Survive the failure of one component | High availability |
| Add and remove capacity automatically | Elasticity |
| Provision and tear down in minutes | Agility |
| Forecast both performance and cost | Predictability |
| Lowest cost per unit from provider scale | Economies of scale |

## Exam traps

- Public cloud does **not** mean public data; it means provider-owned, shared infrastructure.
- Cloud removes **hardware** management, not your responsibility for data and access.
- Scalability is capability; elasticity is automation.
- "Minimal changes and OS control" points to IaaS; "no server management" points to PaaS or serverless.
- Hybrid combines private/on-premises with public; multi-cloud combines public providers.
