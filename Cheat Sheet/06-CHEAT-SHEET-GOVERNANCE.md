# AZ-900 cheat sheet 3/3 — Describe Azure management and governance

*One page. Facts snapshot 2026-11; verify current behaviour on Microsoft Learn before the exam.*

## Cost management

| Tool | Use it for |
|---|---|
| **Azure Pricing calculator** | Estimate the monthly cost of a planned set of Azure services. |
| **Total Cost of Ownership (TCO) calculator** | Compare an existing on-premises estate with the equivalent Azure cost. |
| **Cost analysis** | Review actual spend and trends grouped by resource, resource group, service, or tag. |
| **Budgets** | Set a spending target and alert on actual or forecast thresholds. Budgets **warn**; they do not block spend. |
| **Tags** | Name-value metadata for cost allocation, ownership, and environment. Not inherited automatically. |
| **Azure Advisor** | Free recommendations for cost, reliability, security, performance, and operational excellence. |
| **Reservations / savings plans** | Commit to one or three years for a lower rate on predictable workloads. |

**Cost drivers:** region, resource size, running time, storage volume and tier, transactions, and outbound (egress) data transfer. Deallocating or deleting idle resources is the fastest saving.

## Governance

| Control | What it does |
|---|---|
| **Azure RBAC** | Assigns a role to a user, group, service principal, or managed identity at a scope. Permissions inherit downward. |
| **Owner** | Full access including granting access. |
| **Contributor** | Create and manage resources, cannot grant access. |
| **Reader** | View resources only. |
| **User Access Administrator** | Manage access only, not resources. |
| **Azure Policy** | Enforces what resources may look like: allowed regions, required tags, permitted SKUs. Evaluates create and update requests. |
| **Policy effects** | Deny, Audit, Append, Modify, DeployIfNotExists, AuditIfNotExists, Disabled. |
| **Resource locks** | **CanNotDelete** blocks deletion; **ReadOnly** blocks changes and deletion. Locks apply to everyone, including Owners, and inherit to child scopes. |
| **Management groups** | Apply policy and access once across many subscriptions. |
| **Tags** | Organise and report; a resource does not inherit its resource group's tags automatically. |

**RBAC vs Policy:** RBAC controls **who can do what**; Policy controls **what the result may look like**. A policy Deny blocks even subscription Owners.

## Monitoring

| Tool | What it shows |
|---|---|
| **Azure Monitor** | Central platform for metrics, logs, alerts, dashboards, and workbooks. |
| **Metrics** | Numeric time series, near real time; platform metrics are automatic. |
| **Logs / Log Analytics** | Detailed records queried with **KQL** (`where`, `summarize`, `project`, `bin`, `join`). |
| **Activity log** | Control-plane audit: who created, changed, or deleted a resource. |
| **Alert rule** | The condition — metric threshold, log query, or activity event. |
| **Action group** | The response — email, SMS, voice, push, webhook, function, Logic App, runbook, ITSM. |
| **Application Insights** | Request, dependency, exception, and performance telemetry for apps. |
| **Service Health** | Azure incidents, planned maintenance, and advisories for your services and regions. |
| **Advisor** | Personalised recommendations in five categories. |
| **Microsoft Defender for Cloud** | Security posture, secure score, and workload protection across clouds. |

**Your resources vs the platform:** Azure Monitor watches what you deployed; Service Health reports what Microsoft is doing.

## Deployment and tooling

| Tool | Notes |
|---|---|
| **Azure portal** | Web GUI for creating and managing resources. |
| **Azure CLI** | Cross-platform commands such as `az group create`. |
| **Azure PowerShell** | Cmdlets such as `New-AzResourceGroup` in the Az module. |
| **Azure Cloud Shell** | Browser terminal with CLI and PowerShell preinstalled and already authenticated. |
| **ARM templates** | Declarative JSON describing the desired end state; idempotent redeploys. |
| **Bicep** | Declarative language that compiles to ARM JSON; cleaner syntax, same engine. |
| **Infrastructure as code** | Repeatable deployments plus version control and review of infrastructure changes. |

**Declarative vs imperative:** a template describes the destination; a script describes the steps. Both can automate, but only the template is naturally idempotent.

## Compliance, privacy, and agreements

| Item | What it covers |
|---|---|
| **Microsoft Trust Center** | Published security, privacy, and compliance information and certifications. |
| **Service Trust Portal** | Audit reports and compliance evidence for customers. |
| **Microsoft Privacy Statement** | What personal data Microsoft collects and how it is used and protected. |
| **Microsoft Purview Compliance Manager** | Assesses your tenant against standards such as ISO 27001 or GDPR and tracks improvement actions. |
| **Service Level Agreement (SLA)** | Availability commitment with service credits if missed; not a guarantee of zero downtime. |
| **Preview features** | May change or be withdrawn and are typically excluded from the standard SLA; avoid in production. |

**Shared compliance:** Microsoft certifies the platform; the customer must configure and operate it compliantly.

## Quick decision table

| Requirement | Choose |
|---|---|
| Estimate a new Azure design | Pricing calculator |
| Justify a migration | TCO calculator |
| See actual spend by department | Cost analysis with tags |
| Warn before overspending | Budget with alerts |
| Prevent deletion | CanNotDelete lock |
| Prevent any change | ReadOnly lock |
| Block resources outside a region | Azure Policy (Deny) |
| Grant least privilege | RBAC at the narrowest scope |
| Investigate who deleted a resource | Activity log |
| Track app exceptions and latency | Application Insights |
| Learn about an Azure outage | Service Health |
| Reduce cost on idle VMs | Advisor recommendations |
