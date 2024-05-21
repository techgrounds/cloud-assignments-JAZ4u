# [1/ Azure files, App Service, CDN, DNS, SQL,COSMOS DB]

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

# <u>Cosmos DB:</u>

- **What is it?**: Cosmos DB is a globally distributed, multi-model database service provided by Microsoft Azure. It's designed to offer high availability, low latency, and scalability across different geographical regions. Cosmos DB supports multiple data models, including document, key-value, graph, and column-family, making it versatile for various types of applications.
  
  - **Practical Experience**: Practical experience with Cosmos DB typically involves tasks such as:
    1. **Data Modeling**: Designing the database schema to suit the application's requirements, choosing the appropriate data model (e.g., document, graph) based on the data structure and access patterns.
2. **Development**: Implementing code to interact with Cosmos DB, including CRUD (Create, Read, Update, Delete) operations, querying data using SQL-like syntax (in the case of document model), and handling consistency levels.

3. **Deployment**: Configuring and deploying Cosmos DB instances within Azure, setting up replication across regions for global distribution, and optimizing performance by choosing appropriate throughput and partitioning strategies.

4. **Performance Tuning**: Monitoring and optimizing database performance, including indexing strategies, partitioning schemes, and query optimization.

5. **Integration**: Integrating Cosmos DB with other Azure services and tools, such as Azure Functions, Azure Logic Apps, Azure Data Factory, and Azure Synapse Analytics, to build end-to-end solutions.

6. **Security and Compliance**: Implementing security measures to protect data stored in Cosmos DB, including authentication, authorization, encryption, and compliance with regulatory standards such as GDPR or HIPAA.

Practical experience with Cosmos DB would involve working on these aspects either through development, deployment, or maintenance tasks within a project or application that utilizes Azure Cosmos DB as its database backend.

## Key-terms

1. **Physical Partition**: In Azure Cosmos DB, data is horizontally partitioned across multiple physical partitions for scalability and performance. Each physical partition is a unit of storage and compute resources managed by the service. Azure Cosmos DB dynamically manages the distribution of data across these partitions based on the chosen partition key.

2. **Request Unit (RU)**: Request Unit is a measure of throughput in Azure Cosmos DB. It represents the amount of resources required to perform read or write operations against the database. The RU/s (Request Units per second) determines the rate at which these operations can be performed. Higher RU/s allocation allows for higher throughput and faster response times.

3. **Leader and Follower**: In Azure Cosmos DB's multi-region replication model, each region has one write region (Leader) and one or more read regions (Followers). The Leader region accepts write operations and propagates changes to the Follower regions asynchronously. Follower regions can serve read operations with low latency, providing data access closer to users.

4. **Cosmos DB Hash Numbers**: Cosmos DB uses hash numbers for partitioning data across physical partitions. The hash function generates a numerical value based on the partition key of each item. This hash number determines which physical partition the item belongs to, ensuring even distribution of data across partitions for efficient storage and query processing.

5. **Partition Key**: The Partition Key is a property chosen by the developer to partition data within a Cosmos DB container. It determines how data is distributed across physical partitions. Selecting an appropriate partition key is crucial for achieving optimal performance and scalability, as it affects query distribution and resource utilization.

6. **Containers**: In Azure Cosmos DB, a container is a logical entity used to store and manage JSON documents or other data entities. Each container is associated with a specific partition key and can have its own throughput settings. Containers can be thought of as analogous to tables in relational databases but with schema flexibility to accommodate various data models.

7. **Parse & Bind**: In the context of Azure Cosmos DB server-side programming, parse and bind refer to the process of parsing and binding parameters passed to stored procedures, triggers, or user-defined functions. Parsing involves extracting values from the input parameters, while binding involves associating these values with variables or placeholders used in the code logic.

8. **Global Distribution**: Azure Cosmos DB offers the ability to distribute data globally across multiple Azure regions. This ensures low-latency access to data for users worldwide by placing data closer to them geographically. It also provides high availability and disaster recovery capabilities.

9. **Multi-Model**: Azure Cosmos DB supports multiple data models, including document, key-value, graph, and column-family. This allows developers to choose the most appropriate data model for their application's specific needs without having to use separate databases.

10. **Consistency Levels**: Azure Cosmos DB offers various consistency levels to balance consistency, availability, and latency requirements. These levels include strong consistency, bounded staleness, session consistency, consistent prefix, and eventual consistency.

11. **Partitioning**: Partitioning in Azure Cosmos DB involves distributing data across multiple physical partitions to achieve scalability and performance. It's essential for distributing the workload evenly and ensuring that the database can handle a large volume of requests.

12. **Throughput**: Throughput in Azure Cosmos DB refers to the measure of resources allocated to a database to handle requests per second (RUs/s). Request Units (RUs) are a unit of measure representing the resources required to perform read and write operations against the database.

13. **SDKs (Software Development Kits)**: Azure Cosmos DB provides SDKs for various programming languages, including .NET, Java, Python, Node.js, and others. These SDKs simplify development by providing libraries and APIs for interacting with Cosmos DB programmatically.

14. **Change Feed**: The change feed in Azure Cosmos DB is a persistent log of changes that occur in the database. It allows developers to track and process changes to the data in near-real-time, enabling scenarios such as data synchronization, auditing, and event-driven architectures.

15. **Indexing**: Azure Cosmos DB automatically indexes data for efficient querying. Developers can customize indexing policies to optimize query performance based on access patterns and data distribution.

16. **Triggers and Stored Procedures**: Azure Cosmos DB supports server-side logic through triggers and stored procedures. Triggers enable automatic execution of custom code in response to database operations, while stored procedures allow developers to define reusable logic for complex transactions.

17. **Cosmos DB**:
- **What is it?**: Cosmos DB is a globally distributed, multi-model database service provided by Microsoft Azure. It's designed to offer high availability, low latency, and scalability across different geographical regions. Cosmos DB supports multiple data models, including document, key-value, graph, and column-family, making it versatile for various types of applications.
  
  - **Practical Experience**: Practical experience with Cosmos DB typically involves tasks such as:
  1. **Data Modeling**: Designing the database schema to suit the application's requirements, choosing the appropriate data model (e.g., document, graph) based on the data structure and access patterns.
  2. **Development**: Implementing code to interact with Cosmos DB, including CRUD (Create, Read, Update, Delete) operations, querying data using SQL-like syntax (in the case of document model), and handling consistency levels.
  3. **Deployment**: Configuring and deploying Cosmos DB instances within Azure, setting up replication across regions for global distribution, and optimizing performance by choosing appropriate throughput and partitioning strategies.
4. **Performance Tuning**: Monitoring and optimizing database performance, including indexing strategies, partitioning schemes, and query optimization.

5. **Integration**: Integrating Cosmos DB with other Azure services and tools, such as Azure Functions, Azure Logic Apps, Azure Data Factory, and Azure Synapse Analytics, to build end-to-end solutions.

6. **Security and Compliance**: Implementing security measures to protect data stored in Cosmos DB, including authentication, authorization, encryption, and compliance with regulatory standards such as GDPR or HIPAA.

Practical experience with Cosmos DB would involve working on these aspects either through development, deployment, or maintenance tasks within a project or application that utilizes Azure Cosmos DB as its database backend.

## Assignment

Task:
Gain practical experience with:

- Cosmos DB

### Used sources

- CHAT_GPT
- https://www.youtube.com/watch?v=hBY2YcaIOQM
- https://www.youtube.com/watch?v=D5xU7_98jWc
- [Pricing model of Azure Cosmos DB | Microsoft Learn](https://learn.microsoft.com/en-us/azure/cosmos-db/how-pricing-works)
- [Quickstart - Create Azure Cosmos DB resources from the Azure portal | Microsoft Learn](https://learn.microsoft.com/en-us/azure/cosmos-db/nosql/quickstart-portal)
- [Azure Cosmos DB Tutorial for Beginners - YouTube](https://www.youtube.com/watch?v=Z3hDUIXrAj0)
- [What is Azure Cosmos DB? | Azure Cosmos DB Essentials Season 1 - YouTube](https://www.youtube.com/watch?v=Jvgh64rvdXU)
- 

### Encountered problems

- no problems

### Result

Task:
Gain practical experience with:

- Cosmos DB
  Gaining practical experience with Azure Cosmos DB involves a combination of learning resources, hands-on practice, and real-world projects. Here's a step-by-step guide to help you get started:
1. **Learn the Basics**: Begin by understanding the fundamentals of Azure Cosmos DB. Microsoft's documentation provides comprehensive resources, including tutorials, quickstarts, and conceptual overviews. Focus on topics such as data modeling, partitioning, consistency levels, and global distribution.

2. **Azure Free Tier**: Sign up for an Azure account if you don't already have one. Azure offers a free tier with a limited amount of Cosmos DB usage, allowing you to explore and experiment with the service without incurring costs.

3. **Hands-on Labs**: Take advantage of hands-on labs and interactive tutorials provided by Microsoft Learn. These guided exercises walk you through various aspects of Cosmos DB, from creating databases and collections to querying data and optimizing performance.

4. **Sample Applications**: Explore sample applications and code samples available in the Azure Cosmos DB GitHub repository. These examples cover different programming languages and scenarios, giving you practical insights into how Cosmos DB can be used in real-world projects.

5. **Online Courses**: Enroll in online courses or training programs dedicated to Azure Cosmos DB. Platforms like Pluralsight, Udemy, and Coursera offer courses specifically focused on Cosmos DB, ranging from beginner to advanced levels.

6. **Documentation and Blogs**: Continuously refer to the official Azure Cosmos DB documentation for in-depth information and best practices. Additionally, follow blogs and articles written by Azure experts and community members to stay updated on new features, tips, and tricks.

7. **Build a Project**: Start a personal or small-scale project that utilizes Cosmos DB as the database backend. This could be a web application, mobile app, or IoT solution. Implement various features such as data storage, retrieval, and real-time updates to gain practical experience.

8. **Collaborate and Network**: Join online forums, discussion groups, and communities focused on Azure and Cosmos DB. Participate in discussions, ask questions, and share your experiences with others. Collaborating with peers and learning from their experiences can accelerate your learning process.

9. **Certification**: Consider pursuing Azure certifications, such as the Azure Developer Associate or Azure Database Administrator Associate, which cover Cosmos DB among other Azure services. Certification exams validate your skills and knowledge, enhancing your credibility in the job market.

By following these steps and actively engaging with the Azure Cosmos DB ecosystem, you can gain practical experience and become proficient in leveraging this powerful database service for various applications and projects.