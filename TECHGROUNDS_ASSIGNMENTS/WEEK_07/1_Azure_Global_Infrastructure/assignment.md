# [1/ Azure Global Infrastructure]

Alles in de cloud, van servers tot networking, is virtualized. Als klant van een cloud provider hoef je je geen zorgen te maken over de onderliggende fysieke infrastructuur. De fysieke locatie van je applicatie of data kan echter wel belangrijk zijn.

De global infrastructure van Azure bestaat uit de volgende componenten:

- Regions
- Availability Zones
- Region Pairs

Je hebt zelf controle over welke regio je gebruikt, maar niet elke service is beschikbaar in elke regio. Sommige services zijn ook niet gebonden aan een specifieke regio. Denk hierbij bijvoorbeeld aan Azure Subscriptions. Voor andere diensten als Azure Virtual Machines kan je juist een specifiek datacenter kiezen.

## Key-terms

1. **The global infrastructure of Azure**: Azure operates a global network of datacenters strategically located around the world to ensure low latency and high availability for its services.

2. **Regions**: Azure is organized into geographical regions, which are clusters of datacenters located within a specific geographic area. Each region is designed to provide high availability and fault tolerance.

3. **Availability Zones**: Within certain Azure regions, there are Availability Zones, which are physically separate datacenters within the same region. Availability Zones are designed to provide additional redundancy and fault tolerance.

4. **Region Pairs**: Azure regions are paired for data residency, disaster recovery, and other purposes. Each region pair consists of two regions within the same geography (such as within the same continent), but they are far enough apart to provide redundancy in case of a regional failure.

5. **Azure Subscriptions**: Azure Subscriptions are the billing and management containers for Azure services. Subscriptions define the billing and usage boundaries for resources deployed within Azure.

6. **Azure Virtual Machines**: Azure Virtual Machines (VMs) allow users to create and manage virtualized compute instances in the cloud. VMs are available in various configurations, including different sizes, operating systems, and deployment options.

7. **Azure datacenter**: Azure datacenters are the physical facilities where Azure infrastructure is hosted. These datacenters house servers, networking equipment, and other hardware necessary to run Azure services.

## Assignment

Bestudeer:

- Wat is een Azure Region?
- Wat is een Azure Availability Zone?
- Wat is een Azure Region Pair?
- Waarom zou je een regio boven een andere verkiezen?

### Used sources

- chat GPT

- https://www.merriam-webster.com/

- [AZ-900 Episode 7 | Geographies, Regions &amp; Availability Zones | Microsoft Azure Fundamentals Course - YouTube](https://www.youtube.com/watch?v=C-nNw1mGwzE)

- [Azure Regions &amp; Availability Zones | AZ-900 Exam Preparation | Azure Fundamentals - YouTube](https://www.youtube.com/watch?v=Q-VYtWajJ4E)

- [Azure Regions, Availability zones, Data centers | Azure for beginners (AZ-900) | EP8 - YouTube](https://www.youtube.com/watch?v=FBBarlL3pRE)

- [Choose the Right Azure Region for You | Microsoft Azure](https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies/#overview)

- [Global Infrastructure | Microsoft Azure](https://azure.microsoft.com/en-us/explore/global-infrastructure/)

- learn.techgrounds.nl

### Encountered problems

- no problems encountered

# Result

Bestudeer:

- <u>Wat is een Azure Region?</u>
  
  - <u></u>In Azure, regions are the fundamental geographical units that house datacenters and serve as the foundation for deploying and running Azure services. Here's a breakdown of what regions entail:
  1. **Geographical Clusters**: Each Azure region comprises a cluster of datacenters situated within a specific geographic area. These datacenters are strategically located to cater to the needs of users and businesses in that region.
  
  2. **High Availability**: Azure regions are designed to ensure high availability of services and applications by distributing resources across multiple datacenters within the region. This redundancy helps mitigate the risk of downtime due to hardware failures, maintenance, or other disruptions.
  
  3. **Fault Tolerance**: By leveraging redundant infrastructure across multiple datacenters within the same region, Azure ensures fault tolerance. In the event of a failure in one datacenter, services and applications can seamlessly failover to other healthy datacenters within the region, minimizing service interruptions.
  
  4. **Compliance and Data Residency**: Azure regions often comply with local data residency and compliance requirements, ensuring that customer data stays within specific geographic boundaries as mandated by regulations or organizational policies.
  
  5. **Scalability**: Azure regions provide the scalability needed to accommodate the growing demand for cloud services. Microsoft continually expands its regional footprint to support the increasing adoption of Azure across various industries and geographies.
  
  6. **Performance Optimization**: Users can select the Azure region that best suits their performance requirements and proximity to end-users or other resources. Choosing a region closer to users can reduce latency and improve the overall performance of applications and services.
  
  Overall, Azure regions serve as the building blocks of Microsoft's global cloud infrastructure, offering customers a wide range of options to deploy, manage, and scale their applications and services while ensuring reliability, compliance, and performance.

- <u>Wat is een Azure Availability Zone?</u>
  
  - <u></u>Availability Zones (AZs) in Azure are physically separate datacenters within the same Azure region. They are designed to provide high availability, fault tolerance, and resiliency for applications and services deployed in the cloud.
  
  Key characteristics of Azure Availability Zones include:
  
  1. **Physical Separation**: Each Availability Zone is located in a physically separate datacenter with independent power, cooling, and networking infrastructure. This separation helps minimize the risk of a single point of failure affecting all zones simultaneously.
  
  2. **Redundancy**: By distributing resources across multiple Availability Zones within the same region, Azure ensures redundancy and fault tolerance. In the event of a failure in one Availability Zone, applications and services can automatically failover to resources in another zone without impacting availability.
  
  3. **Low Latency**: Availability Zones within the same region are interconnected through high-speed, low-latency networking, enabling fast communication and data transfer between zones.
  
  4. **Resilience**: Azure's Service Level Agreements (SLAs) for virtual machines, storage, and other services often include guarantees for availability and uptime across multiple Availability Zones. This resilience ensures that applications and services remain operational even in the face of hardware failures, maintenance events, or other disruptions.
  
  5. **Scalability**: Availability Zones allow customers to scale their applications horizontally by distributing workloads across multiple zones. This scalability enables customers to handle increased traffic or workload demand without sacrificing performance or reliability.
  
  Overall, Availability Zones in Azure provide customers with the flexibility to design and deploy resilient, highly available applications and services that can withstand failures and disruptions at the infrastructure level. By leveraging multiple Availability Zones within the same region, organizations can achieve greater reliability and continuity for their critical workloads in the cloud.

- <u>Wat is een Azure Region Pair?</u>
  
  - <u></u>Region pairs in Azure are strategic combinations of two Azure regions, typically located within the same geography, such as within the same continent. These region pairs are specifically designed to provide data residency, disaster recovery, and other purposes for Azure customers.
  
  The primary purpose of region pairs is to ensure data residency compliance and to provide redundancy and high availability for applications and services deployed in Azure. By pairing regions within close geographic proximity but far enough apart to reduce the risk of simultaneous failures due to natural disasters, power outages, or other disruptive events, Azure ensures that customers can maintain business continuity and data integrity.
  
  In the event of a regional outage or disaster in one region of the pair, Azure services and data can be quickly failed over or replicated to the paired region, minimizing downtime and data loss. This disaster recovery capability is crucial for mission-critical applications and services that require high availability and resilience.
  
  Region pairs also facilitate compliance with data sovereignty regulations by ensuring that customer data remains within specific geographic boundaries. Organizations with strict data residency requirements can deploy their applications and services in the paired regions to meet these regulatory obligations while still benefiting from Azure's global infrastructure and scalability.
  
  Overall, region pairs play a vital role in Azure's resilience, disaster recovery capabilities, and compliance with data residency regulations, providing customers with confidence in the availability, reliability, and security of their cloud deployments.

- <u>Waarom zou je een regio boven een andere verkiezen?</u>
  
  - <u></u>Choosing one Azure region over another can depend on several factors, such as:
  1. **Proximity to Users**: Selecting a region close to your users can minimize latency and improve the overall performance and user experience of your applications or services.
  
  2. **Compliance and Data Residency**: Different regions may have specific compliance requirements or data residency regulations. Choosing a region that complies with these regulations ensures that your data remains within the necessary legal boundaries.
  
  3. **Availability and Uptime**: Azure regions may have varying levels of availability and uptime guarantees. Consider the Service Level Agreements (SLAs) offered by each region and choose the one that best aligns with your application's availability requirements.
  
  4. **Pricing**: Azure services may have different pricing in each region. Evaluating the cost-effectiveness of each region based on your usage patterns and budget can help you select the most economical option.
  
  5. **Availability of Services**: Not all Azure services are available in every region. If your application relies on specific Azure services, you should choose a region where those services are supported.
  
  6. **Disaster Recovery and Redundancy**: Some regions are strategically paired as region pairs to provide redundancy and disaster recovery capabilities. Choosing regions within a region pair ensures that your application remains available even in the event of a regional failure.
  
  By considering these factors and assessing your specific requirements, you can make an informed decision about which Azure region best suits your needs.