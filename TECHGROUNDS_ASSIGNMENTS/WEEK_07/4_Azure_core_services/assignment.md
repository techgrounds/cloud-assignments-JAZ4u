# [4/ Azure Core Services]

You can think of this document as a sort of guide to your AZ-900 certification. It lists the services you need to know in a bit more detail. Additionally, this document describes how to handle the other services you may encounter in the (practice) exam.

There are many services in Azure, but some are more important than others. Azure mentions the following architectural components and services of which you should have a fairly in-depth understanding of what they do:

- Regions and Region Pairs
- Availability Zones
- Resource Groups
- Subscriptions
- Management Groups
- Azure Resource Manager
- Virtual Machines
- Azure App Services
- Azure Container Instances (ACI)
- Azure Kubernetes Service (AKS)
- Azure Virtual Desktop
- Virtual Networks
- VPN Gateway
- Virtual Network Peering
- ExpressRoute
- Container (Blob) Storage
- Disk Storage
- File Storage
- Storage Tiers
- Cosmos DB
- Azure SQL Database
- Azure Database for MySQL
- Azure Database for PostgreSQL
- SQL Managed Instance
- Azure Marketplace

Of course, there are many more services that may appear on your exam. For these services, it's sufficient to be familiar with the product page (see here for an example of an Azure product page).

In addition to services, you can also expect questions about various cloud concepts, such as High Availability, the consumption-based pricing model, and the shared responsibility model.

## Key-terms

- 1. **Regions and Region Pairs**: Azure data centers are located in various geographic regions worldwide. Regions are areas within a specific geography, such as North America, Europe, or Asia Pacific. Region Pairs are geographically separate data center locations within the same geopolitical region, providing redundancy and disaster recovery capabilities.
  
  2. **Availability Zones**: Availability Zones are physically separate data centers within an Azure region. They offer high availability and fault tolerance by ensuring that applications and data remain available even if one zone within a region fails.
  
  3. **Resource Groups**: Resource Groups are containers that hold related Azure resources for a specific solution or application. They provide a way to manage and organize resources, enabling easier management, monitoring, and access control.
  
  4. **Subscriptions**: Subscriptions are the billing containers in Azure. They define the billing scope and provide access to Azure services based on the subscription's permissions and limits.
  
  5. **Management Groups**: Management Groups are containers that help you manage access, policies, and compliance across multiple subscriptions. They provide a way to apply governance controls consistently across an organization's Azure environment.
  
  6. **Azure Resource Manager (ARM)**: ARM is the deployment and management service for Azure. It provides a consistent management layer that enables you to deploy, manage, and monitor Azure resources in a declarative manner using templates.
  
  7. **Virtual Machines (VMs)**: Azure VMs are scalable computing instances that run applications and workloads. They offer flexibility in terms of size, operating system, and deployment options.
  
  8. **Azure App Services**: App Services is a platform-as-a-service (PaaS) offering for building, deploying, and scaling web applications and APIs. It supports multiple programming languages and frameworks.
  
  9. **Azure Container Instances (ACI)**: ACI is a serverless container service that enables you to run containers on Azure without managing underlying infrastructure. It provides rapid deployment and scaling of containerized applications.
  
  10. **Azure Kubernetes Service (AKS)**: AKS is a managed Kubernetes service that simplifies the deployment, management, and scaling of containerized applications using Kubernetes orchestration.
  
  11. **Azure Virtual Desktop**: Azure Virtual Desktop is a desktop and app virtualization service that enables users to access Windows desktops and applications from anywhere on any device.
  
  12. **Virtual Networks**: Virtual Networks enable you to create isolated network environments in Azure, allowing you to securely connect Azure resources and extend on-premises networks to the cloud.
  
  13. **VPN Gateway and ExpressRoute**: These are networking services that provide secure connectivity options for connecting on-premises networks to Azure resources.
  
  14. **Virtual Network Peering**: Virtual Network Peering allows you to connect virtual networks within the same region or across different regions, enabling seamless communication between resources.
  
  15. **Container (Blob), Disk, and File Storage**: These are different types of storage services in Azure for storing various types of data, including blobs, disks, and files, with different performance and durability options.
  
  16. **Storage Tiers**: Azure Storage offers multiple tiers for storing data based on access frequency and performance requirements, including hot, cool, and archive tiers.
  
  17. **Cosmos DB**: Cosmos DB is a globally distributed, multi-model database service for building highly responsive and scalable applications. It supports various data models and provides low-latency access to data worldwide.
  
  18. **Azure SQL Database, Azure Database for MySQL, Azure Database for PostgreSQL, SQL Managed Instance**: These are managed database services in Azure for SQL Server, MySQL, and PostgreSQL, offering features such as automatic backups, scaling, and high availability.
  
  19. **Azure Marketplace**: Azure Marketplace is a digital storefront where you can find, try, and buy thousands of third-party solutions and services certified to run on Azure.

- **The AZ-900 exam**
  
  - The AZ-900 exam, also known as "Microsoft Azure Fundamentals," is an entry-level certification exam offered by Microsoft. It is designed for individuals who are new to Azure and want to demonstrate foundational knowledge of cloud services and how they are provided with Microsoft Azure. Here's an overview of the AZ-900 exam:
    
    **Exam Objectives:**
    
    The AZ-900 exam covers the following fundamental concepts related to Microsoft Azure:
    
    1. **Cloud Concepts**: Understand the benefits and considerations of cloud computing, including high availability, scalability, elasticity, agility, and economies of scale. Learn about different cloud deployment models (public, private, hybrid) and service models (Infrastructure as a Service - IaaS, Platform as a Service - PaaS, Software as a Service - SaaS).
    
    2. **Core Azure Services**: Gain familiarity with core Azure services across various categories, including compute, networking, storage, databases, and identity. Understand the purpose and key features of services such as Azure Virtual Machines, Azure Blob Storage, Azure SQL Database, Azure App Service, Azure Virtual Network, and Azure Active Directory.
    
    3. **Security, Privacy, Compliance, and Trust**: Learn about security features and tools available in Azure to secure data, applications, and infrastructure. Understand Azure security services, identity management, network security, compliance certifications, and privacy controls.
    
    4. **Azure Pricing and Support**: Understand Azure pricing models, including pay-as-you-go, consumption-based pricing, and pricing calculators. Learn about Azure subscription types, billing, and support options available for Azure customers.
    
    5. **Azure Governance and Compliance**: Gain an understanding of Azure management tools, such as Azure Policy and Azure Resource Manager (ARM), and their role in enforcing organizational standards and compliance requirements. Learn about Azure governance methodologies and how to monitor and manage resources effectively.
    
    **Exam Format:**
    
    - Exam Name: Microsoft Azure Fundamentals (AZ-900)
    - Exam Format: Multiple choice questions
    - Number of Questions: Typically between 40-60 questions
    - Exam Duration: 60 minutes
    - Passing Score: Around 700 points out of 1000
    - Exam Languages: Available in multiple languages
    
    **Preparation Resources:**
    
    Microsoft offers official preparation resources for the AZ-900 exam, including:
    
    1. **Microsoft Learn**: Free online learning platform with interactive modules, hands-on labs, and assessments covering Azure fundamentals.
    
    2. **Microsoft Official Practice Tests**: Official practice tests available for purchase to help candidates assess their readiness for the exam.
    
    3. **Azure Documentation**: Official Azure documentation provides in-depth information about Azure services, features, and best practices.
    
    4. **Books and Video Courses**: Various books and online video courses are available from Microsoft Press and other publishers to supplement exam preparation.
    
    The AZ-900 exam is an excellent starting point for individuals looking to begin their journey with Azure and gain a foundational understanding of cloud computing concepts and Azure services.

## Assignment

Study:

- De Exam Guide voor Microsoft Azure Fundamentals (AZ-900)

### Used sources

- [GitHub - AzureMentor/Azure-AZ-900-Study-Guide: Study Guide for the Microsoft Azure Fundamentals Exam](https://github.com/AzureMentor/Azure-AZ-900-Study-Guide/tree/master)
  
  - [Azure-AZ-900-Study-Guide/1-Describe cloud concepts (25–30%).md at master · AzureMentor/Azure-AZ-900-Study-Guide · GitHub](https://github.com/AzureMentor/Azure-AZ-900-Study-Guide/blob/master/1-Describe%20cloud%20concepts%20(25–30%25).md)
  
  - [Azure-AZ-900-Study-Guide/2-Describe Azure architecture and services (35–40%).md at master · AzureMentor/Azure-AZ-900-Study-Guide · GitHub](https://github.com/AzureMentor/Azure-AZ-900-Study-Guide/blob/master/2-Describe%20Azure%20architecture%20and%20services%20(35–40%25).md)
  
  - [Azure-AZ-900-Study-Guide/3-Describe Azure management and governance (30–35%).md at master · AzureMentor/Azure-AZ-900-Study-Guide · GitHub](https://github.com/AzureMentor/Azure-AZ-900-Study-Guide/blob/master/3-Describe%20Azure%20management%20and%20governance%20(30–35%25).md)
  
  - [Azure-AZ-900-Study-Guide/README.md at master · AzureMentor/Azure-AZ-900-Study-Guide · GitHub](https://github.com/AzureMentor/Azure-AZ-900-Study-Guide/blob/master/README.md)

- ARIA

- CHAT-GPT

- learn.techgrounds.nl

- [AZ-900: 765 Questions (2024) | Documentation | Exam Tips | PDF Dumps (Exam Cram💡) - YouTube](https://www.youtube.com/watch?v=C6RFbx1STUk&ab_channel=TheTechBlackBoard)

- [AZ-900 Azure Fundamentals Exam Cram (2024 Edition) - Full Course - YouTube](https://www.youtube.com/watch?v=8n-kWJetQRk&ab_channel=InsideCloudandSecurity)

- [AZ-900 Exam Cram FULL-2024_HANDOUT.pdf - Microsoft Word Online](https://onedrive.live.com/view.aspx?resid=1590B798C9CD6D68!158639&authkey=!ACcAstG4pRkLS_M)

- https://www.youtube.com/@InsideCloudAndSecurity
  
  - https://onedrive.live.com/?authkey=%21ACcAstG4pRkLS%5FM&id=1590B798C9CD6D68%21136912&cid=1590B798C9CD6D68

### Encountered problems

- no problems

### Result

Study:

- **The Exam Guide for Microsoft Azure Fundamentals (AZ-900)**
  
  - **Exam Overview:**
    
    - The Microsoft Azure Fundamentals (AZ-900) exam is designed for candidates who are looking to demonstrate foundational knowledge of cloud services and how those services are provided with Microsoft Azure.
    - This exam is suitable for candidates with non-technical backgrounds or those new to cloud computing.
    - Passing the AZ-900 exam can be a stepping stone to more advanced Azure certifications.
    
    **Exam Objectives:** The AZ-900 exam covers the following key topics:
    
    1. Cloud Concepts:
       
       - Understand cloud computing concepts, such as high availability, scalability, elasticity, agility, and disaster recovery.
       - Differentiate between Infrastructure as a Service (IaaS), Platform as a Service (PaaS), and Software as a Service (SaaS).
    
    2. Core Azure Services:
       
       - Identify core Azure services, including Azure Compute, Azure Storage, Azure Networking, and Azure Databases.
       - Understand the benefits and use cases for each Azure service.
    
    3. Security, Privacy, Compliance, and Trust:
       
       - Understand Azure security features, such as encryption, secure network connectivity, and shared responsibility model.
       - Learn about Azure compliance offerings, privacy, and data protection standards.
    
    4. Azure Pricing and Support:
       
       - Understand Azure pricing options, such as pay-as-you-go, reserved instances, and total cost of ownership (TCO).
       - Explore Azure support options and service level agreements (SLAs).
    
    **Preparation Resources:**
    
    - Microsoft provides official exam resources, including exam skills outline, self-paced online courses, and practice tests, to help candidates prepare for the AZ-900 exam.
    - Hands-on experience with Azure services through the Azure portal is highly recommended to reinforce your learning.
    
    By focusing on these exam objectives and utilizing the recommended resources, you can better prepare for the Microsoft Azure Fundamentals (AZ-900) exam. Good luck with your studies and exam preparation! If you have any specific questions about the exam topics or need further guidance, feel free to ask.