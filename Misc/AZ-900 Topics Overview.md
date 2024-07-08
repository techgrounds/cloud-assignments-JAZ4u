### AZ-900 Topics Overview (as of January 23, 2024)

#### Azure Architectural Components and Services

**Compute**

- **Azure Virtual Machines (VMs):** On-demand, scalable computing resources for running applications. VMs can run Windows or Linux and provide high availability with options like VM Scale Sets.
- **Azure App Services:** PaaS offering to host web applications, RESTful APIs, and mobile backends. It supports multiple languages and frameworks.
- **Azure Functions:** Serverless compute service for running event-driven code without managing servers. Ideal for tasks like data processing and real-time file processing.
- **Azure Kubernetes Service (AKS):** Manages Kubernetes clusters for containerized applications, providing scaling and orchestration.

**Networking**

- **Azure Virtual Network (VNet):** Enables secure communication between Azure resources and on-premises environments. VNets can be segmented into subnets and connected through peering.
- **Azure VPN Gateway:** Establishes secure, cross-premises connections using VPN protocols.
- **Azure ExpressRoute:** Creates private connections between Azure datacenters and on-premises infrastructure or colocation facilities.
- **Azure DNS:** Hosts domain names and provides DNS resolution.
- **Load Balancer:** Distributes incoming network traffic across multiple resources to ensure high availability.

**Storage**

- **Azure Blob Storage:** Unstructured data storage service for scalable object storage of binary and text data.
- **Azure File Storage:** Managed file shares accessible via the SMB protocol.
- **Azure Disk Storage:** Provides persistent, high-performance disk storage for Azure VMs.
- **Storage Tiers:** Hot, Cool, and Archive tiers for cost-effective data storage based on access patterns.
- **Redundancy Options:** Locally Redundant Storage (LRS), Geo-Redundant Storage (GRS), and Read-Access Geo-Redundant Storage (RA-GRS) to ensure data durability and availability.

#### Features and Tools to Secure, Govern, and Administer Azure

**Identity and Access Management**

- **Microsoft Entra ID (Azure AD):** Provides identity and access management, enabling SSO, MFA, and conditional access policies.
- **Azure Role-Based Access Control (RBAC):** Manages who has access to Azure resources, what they can do with those resources, and what areas they have access to.

**Security**

- **Zero Trust Model:** Security strategy focusing on verifying every access request as though it originates from an open network.
- **Microsoft Defender for Cloud:** Provides threat protection and security posture management for cloud workloads.
- **Conditional Access:** Enforces access controls based on conditions like user risk, location, and device compliance.

**Governance and Compliance**

- **Azure Policy:** Enforces organizational standards and assesses compliance at scale.
- **Resource Locks:** Prevents accidental deletion or modification of critical resources.
- **Microsoft Purview:** Manages data governance and compliance, providing insights into data locations, usage, and protection.

**Monitoring and Management**

- **Azure Monitor:** Collects, analyzes, and acts on telemetry data from Azure resources. Includes Log Analytics and Application Insights for detailed monitoring and diagnostics.
- **Azure Advisor:** Provides best practices recommendations for improving performance, security, and cost-effectiveness.
- **Azure Service Health:** Tracks the health of Azure services and resources.

#### Skills and Experience Areas

**Infrastructure Management**

- Managing and maintaining IT infrastructure, including servers, networking, and storage.

**Database Management**

- Designing, implementing, and managing databases, ensuring performance, security, and availability.

**Software Development**

- Developing, deploying, and maintaining software applications using various programming languages and frameworks.

### Skills at a Glance

#### Describe Cloud Concepts (25–30%)

- **Define Cloud Computing:** Delivering computing services over the internet (cloud) to offer faster innovation, flexible resources, and economies of scale.
- **Shared Responsibility Model:** Cloud provider manages the infrastructure, while the customer manages the data and applications.
- **Cloud Models:** 
  - **Public Cloud:** Services are delivered over the public internet and shared across multiple organizations.
  - **Private Cloud:** Services are maintained on a private network for a single organization.
  - **Hybrid Cloud:** Combines public and private clouds, allowing data and applications to be shared between them.
- **Consumption-Based Model:** Customers pay only for the resources they use, offering cost-efficiency and scalability.
- **Serverless Computing:** Allows developers to build applications without managing infrastructure, automatically scaling with demand.

**Benefits of Cloud Services**

- **High Availability:** Ensures services are always accessible.
- **Scalability:** Adjust resources based on demand.
- **Reliability:** Provides dependable service with SLAs.
- **Security and Governance:** Implements robust security measures and compliance.
- **Manageability:** Simplifies IT management through automation and centralized control.

**Cloud Service Types**

- **Infrastructure as a Service (IaaS):** Provides virtualized computing resources over the internet.
- **Platform as a Service (PaaS):** Offers hardware and software tools over the internet.
- **Software as a Service (SaaS):** Delivers software applications over the internet on a subscription basis.

#### Describe Azure Architecture and Services (35–40%)

- **Core Architectural Components:**
  - **Regions and Region Pairs:** Geographic areas containing multiple datacenters for high availability and disaster recovery.
  - **Availability Zones:** Isolated locations within a region to ensure service resilience.
  - **Datacenters:** Physical locations housing Azure servers and infrastructure.
  - **Resources and Resource Groups:** Units of Azure services grouped for management purposes.
  - **Subscriptions and Management Groups:** Structures for organizing resources and controlling access.

**Compute and Networking Services**

- **Compute Types:** VMs, containers (AKS), and serverless (Azure Functions).
- **Virtual Networking:** Connects resources securely, including VNets, subnets, and peering.
- **Public and Private Endpoints:** Secure access points for Azure services.

**Storage Services**

- **Azure Storage Services:** Includes Blob, File, Disk, and Queue storage.
- **Storage Tiers and Redundancy:** Options for cost management and data protection.
- **Migration Tools:** AzCopy, Azure Storage Explorer, Azure File Sync, Azure Migrate, and Azure Data Box.

**Identity, Access, and Security**

- **Directory Services:** Microsoft Entra ID, domain services.
- **Authentication Methods:** SSO, MFA, passwordless.
- **External Identities:** B2B, B2C.
- **Security Models:** Zero Trust, defense-in-depth, Microsoft Defender for Cloud.

#### Describe Azure Management and Governance (30–35%)

- **Cost Management:**
  - **Factors Affecting Costs:** Resource usage, storage, compute.
  - **Cost Tools:** Pricing calculator, Total Cost of Ownership (TCO) Calculator.
  - **Cost Management Capabilities:** Budgeting, forecasting, and monitoring.

**Governance and Compliance Tools**

- **Microsoft Purview:** Data governance.
- **Azure Policy and Resource Locks:** Enforce compliance and protect resources.

**Management and Deployment Tools**

- **Azure Portal and Cloud Shell:** Interfaces for managing Azure resources.
- **Azure Arc:** Extends Azure management to on-premises and multi-cloud environments.
- **Infrastructure as Code (IaC):** ARM templates for automated deployments.

**Monitoring Tools**

- **Azure Advisor:** Provides recommendations for best practices.
- **Azure Service Health:** Monitors the health of Azure services.
- **Azure Monitor:** Tracks performance and health of resources.

These topics cover the essential areas needed for understanding and working with Microsoft Azure, providing a foundation for the AZ-900 certification exam.
