# [1/ Azure files, App Service, CDN, DNS, SQL]

From this moment on, you'll receive fewer concrete assignments. We're relying more on your independent learning skills. Don't worry, you're not alone. You have each other, and the established structure remains in place where you can still ask everyone questions endlessly.

Some services you only need to know theoretically. Others you should have at least turned on and configured once. Each topic describes whether it's a theoretical or practical subject.

Useful questions to keep (/must keep) in mind during your research on the topics:

- What problem does X solve?
- What key terms are associated with X?
- How does X fit in / replace X in an on-premises setting?
- How can I combine X with other services?
- What is the difference between X and other similar services?

A handy list of tasks you should be able to perform practically:

- Where can I find this service in the console?
- How do I turn on this service?
- How can I link this service to other resources?

## Key-terms

1. **Azure Files**:
   
   - **What is it?**: Azure Files offers fully managed file shares in the cloud, accessible via the industry-standard Server Message Block (SMB) protocol.
   - **Practical Experience**: You can create and manage file shares in Azure Files to store and access files from anywhere. This can be useful for applications that require shared file storage or for backing up files in the cloud.

2. **SQL Databases in Azure**:
   
   - **What is it?**: Azure SQL Database is a fully managed relational database service provided by Microsoft in the Azure cloud.
   - **Practical Experience**: With Azure SQL Database, you can create and manage relational databases without the need to manage underlying infrastructure. You can provision databases, manage security, and scale resources as needed to handle your application workload.

3. **Azure App Service**:
   
   - **What is it?**: Azure App Service is a fully managed platform for building, deploying, and scaling web applications and APIs.
   - **Practical Experience**: You can deploy web applications written in various programming languages such as .NET, Java, Node.js, Python, and PHP to Azure App Service. It offers features like automatic scaling, continuous deployment, and integration with Azure services for building modern cloud applications.

4. **Azure CDN (Content Delivery Network)**:
   
   - **What is it?**: Azure CDN is a global content delivery network that helps deliver high-bandwidth content to users with low latency and high availability.
   - **Practical Experience**: By configuring Azure CDN, you can cache static content like images, videos, scripts, and stylesheets closer to your users, resulting in faster load times and reduced bandwidth costs. You can integrate Azure CDN with various Azure services like Blob Storage, Web Apps, and Media Services to accelerate content delivery.

5. **Azure DNS**:
   
   - **What is it?**: Azure DNS is a hosting service for Domain Name System (DNS) domains that provides name resolution using Microsoft Azure infrastructure.
   - **Practical Experience**: With Azure DNS, you can manage DNS records for your domain names hosted in Azure. This includes creating, updating, and deleting DNS records such as A, CNAME, MX, and TXT records. Azure DNS provides high availability and low-latency DNS resolution for your applications and services running in Azure.

## Assignment

Task:
Gain practical experience with:

- Azure Files
- SQL Databases in Azure
- Azure App Service

Gain theoretical knowledge of:

- Azure CDN
- Azure DNS

### Used sources

- CHAT_GPT

### Encountered problems

- no problems

### Result

Task:
Gain practical experience with:

- Azure Files
  To gain cost-efficient practical experience with Azure Files in Azure, follow these steps:
  1. **Azure Free Account**: Sign up for an Azure free account if you haven't already. This provides you with a limited amount of Azure services, including Azure Files, for free during the initial period.
  
  2. **Choose the Right Pricing Tier**: When creating an Azure Files share, choose the appropriate pricing tier based on your requirements. Consider starting with the Standard tier, which offers lower costs compared to the Premium tier.
  
  3. **Optimize Storage Usage**: Efficiently manage your storage usage to minimize costs. Set appropriate quotas for file shares and regularly monitor usage to avoid unnecessary storage consumption.
  
  4. **Leverage Cool and Archive Tiers**: For data that is infrequently accessed, consider using Azure Files with the Cool or Archive tier. These tiers offer lower storage costs compared to the Hot tier, with the trade-off of slightly higher access costs.
  
  5. **Use Shared Access Signatures (SAS)**: Securely share access to Azure Files by using Shared Access Signatures (SAS). This allows you to control access permissions and expiration times, reducing the risk of unauthorized access and potential costs.
  
  6. **Implement Lifecycle Policies**: Implement lifecycle management policies to automatically tier files to cooler storage tiers or delete outdated files. This helps optimize storage costs by moving inactive data to lower-cost storage tiers or removing unnecessary data altogether.
  
  7. **Utilize Snapshots**: Take advantage of Azure Files snapshots to create point-in-time backups of your file shares. Snapshots provide a cost-effective way to protect your data without incurring the cost of storing multiple copies of files.
  
  8. **Monitor and Optimize Data Transfer**: Monitor data transfer costs associated with Azure Files, especially if you're accessing files from different regions or over the internet. Optimize data transfer by minimizing unnecessary transfers and leveraging Azure Content Delivery Network (CDN) for faster access.
  
  9. **Explore Integration with Other Services**: Experiment with integrating Azure Files with other Azure services such as Azure Virtual Machines, Azure Kubernetes Service (AKS), and Azure App Service. Explore use cases where Azure Files can be used as shared storage for applications hosted on these services.
  
  10. **Monitor and Manage Access Controls**: Regularly review and manage access controls for Azure Files to ensure that only authorized users and applications have access to the data. This helps prevent unauthorized access and potential cost implications associated with data breaches.
  
  11. **Stay Informed**: Stay informed about new features, best practices, and cost-saving strategies related to Azure Files by regularly checking official documentation, blogs, forums, and community resources. Continuously evaluate and adjust your usage patterns to optimize costs while gaining practical experience with Azure Files.
  
  By following these steps and actively managing your Azure Files resources, you can gain cost-efficient practical experience while effectively leveraging the capabilities of Azure Files for file storage and sharing in Azure.
  
- SQL Databases in Azure
  To gain cost-efficient practical experience with SQL Databases in Azure, follow these steps:
  1. **Azure Free Account**: Sign up for an Azure free account to access a limited amount of Azure services for free, including Azure SQL Database, during the initial period.
  
  2. **Choose the Right Service Tier**: Select the appropriate service tier and performance level for your SQL Database based on your workload requirements. Start with the basic or standard tier to keep costs low initially.
  
  3. **Right-Size Resources**: Optimize the configuration of your SQL Database to match your workload's requirements. Adjust the compute and storage resources based on usage patterns to avoid over-provisioning and unnecessary costs.
  
  4. **Use Serverless Compute**: Consider using Azure SQL Database serverless compute option for sporadic workloads. With serverless compute, you only pay for the compute resources used per second, making it cost-efficient for unpredictable workloads.
  
  5. **Explore Reserved Capacity**: Explore the option of purchasing reserved capacity for Azure SQL Database. Reserved capacity offers significant cost savings compared to pay-as-you-go pricing, especially for long-term commitments.
  
  6. **Use Azure Hybrid Benefit**: If you have existing SQL Server licenses with Software Assurance, take advantage of Azure Hybrid Benefit to save on SQL Database costs. Azure Hybrid Benefit allows you to use your on-premises SQL Server licenses to pay a reduced rate on Azure SQL Database.
  
  7. **Leverage Elastic Pools**: If you have multiple databases with varying usage patterns, consider using Azure SQL Database elastic pools. Elastic pools allow you to share resources among multiple databases, reducing costs compared to provisioning separate databases.
  
  8. **Monitor and Optimize Performance**: Continuously monitor the performance of your SQL Database using Azure Monitor and Azure SQL Analytics. Identify and optimize queries, indexes, and database design to improve performance and reduce resource utilization, leading to cost savings.
  
  9. **Implement Data Retention Policies**: Define and implement data retention policies to manage the storage costs of your SQL Database. Regularly review and archive unnecessary data to minimize storage consumption and associated costs.
  
  10. **Explore Cost Management Tools**: Use Azure Cost Management and Billing tools to track, analyze, and optimize your SQL Database spending. Set budgets, create alerts, and analyze cost trends to identify opportunities for cost savings.
  
  11. **Learn Best Practices**: Educate yourself on best practices for optimizing SQL Database costs in Azure. Follow Azure documentation, whitepapers, and online resources to stay updated on cost-saving strategies and recommendations.
  
  12. **Experiment with Development/Test Environments**: Use Azure SQL Database for development and testing purposes. Take advantage of the free tier or lower-priced service tiers for non-production workloads to minimize costs while gaining practical experience.
  
  
- Azure App Service
  To gain cost-efficient practical experience with Azure App Service, follow these steps:
  1. **Azure Free Account**: Sign up for an Azure free account to access a limited amount of Azure services for free, including Azure App Service, during the initial period.
  
  2. **Start with Shared or Basic Tier**: Begin with the Shared or Basic tier of Azure App Service, which offers lower costs compared to higher tiers. These tiers are suitable for lightweight applications or for development and testing purposes.
  
  3. **Right-Size Resources**: Optimize the configuration of your Azure App Service plan based on your application's resource requirements. Choose the appropriate number of instances, CPU cores, and memory to match your workload without over-provisioning.
  
  4. **Auto-Scale Based on Demand**: Utilize auto-scaling features available in Azure App Service to automatically adjust the number of instances based on demand. This ensures that you only pay for the resources you need during peak usage periods, reducing costs during idle times.
  
  5. **Use Azure Functions for Serverless Workloads**: Consider using Azure Functions for serverless compute workloads instead of traditional Azure App Service plans. Azure Functions offer a pay-per-execution pricing model, which can be more cost-efficient for sporadic or event-driven workloads.
  
  6. **Leverage Deployment Slots**: Take advantage of deployment slots in Azure App Service for staging and testing deployments. Deployment slots allow you to deploy your application to a separate environment without incurring additional costs, ensuring that your production environment remains unaffected.
  
  7. **Implement Caching and Content Delivery Networks (CDNs)**: Implement caching mechanisms and utilize CDNs to improve performance and reduce the load on your Azure App Service instances. Cached content reduces the number of requests served directly from your application, potentially lowering costs associated with data transfer and compute resources.
  
  8. **Optimize Database Usage**: If your application relies on a database, optimize database queries, indexes, and configurations to minimize resource consumption. Utilize database scaling options and consider using Azure SQL Database Elastic Pools for cost-efficient management of multiple databases.
  
  9. **Monitor Resource Usage**: Continuously monitor resource usage and performance metrics of your Azure App Service instances using Azure Monitor. Identify opportunities for optimization and adjust resource allocations accordingly to avoid unnecessary costs.
  
  10. **Implement Cost Management Policies**: Set up cost management policies and budget alerts to monitor and control spending on Azure App Service. Define spending limits and receive notifications when spending exceeds predefined thresholds, allowing you to take corrective actions promptly.
  
  11. **Explore Reserved Instances**: Consider purchasing reserved instances for Azure App Service plans to benefit from discounted pricing compared to pay-as-you-go rates. Reserved instances offer significant cost savings for long-term commitments, especially for production workloads with predictable usage patterns.
  
  12. **Stay Informed**: Stay informed about cost-saving features, best practices, and updates related to Azure App Service through official documentation, blogs, forums, and community resources. Continuously evaluate and adjust your deployment strategies to optimize costs while gaining practical experience with Azure App Service.
  
  

Gain theoretical knowledge of:

- Azure CDN
- Azure DNS