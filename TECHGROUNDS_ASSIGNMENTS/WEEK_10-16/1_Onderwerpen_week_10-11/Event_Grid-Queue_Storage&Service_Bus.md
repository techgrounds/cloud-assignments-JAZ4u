# [Event Grid, Queue Storage & Service Bus ]

### 1. Event Grid:

Azure Event Grid is a fully managed event routing service that enables you to react to events from various Azure services as well as custom sources. Here's an overview:

- **Publish-Subscribe Model**: Event Grid follows a publish-subscribe model, where publishers emit events and subscribers react to those events. Publishers can be Azure services (like Blob Storage, Azure Functions, Azure IoT Hub) or custom applications.

- **Event Types**: Event Grid supports a wide range of event types, including resource lifecycle events (such as creation, deletion, and updates), custom events, and events from third-party sources.

- **Event Handlers**: Subscribers to Event Grid events are known as event handlers. Event handlers can be Azure Functions, Azure Logic Apps, Azure Automation runbooks, webhooks, or custom applications.

- **Dynamic Scaling**: Event Grid automatically scales to handle millions of events per second, making it suitable for real-time scenarios such as IoT telemetry, log processing, and workflow automation.

- **Serverless**: Event Grid is serverless, meaning you don't need to provision or manage any infrastructure. You only pay for the number of operations processed by Event Grid and any outbound data transfers.

### 2. Queue Storage:

Azure Queue Storage is a scalable message queue service that enables you to store and process messages asynchronously. Here's an overview:

- **FIFO Queues**: Queue Storage supports first-in-first-out (FIFO) message delivery, ensuring that messages are processed in the order they were added to the queue.

- **Decoupled Communication**: Queue Storage facilitates decoupled communication between different components of an application. Senders can add messages to a queue without needing to know the details of the receivers, allowing for loose coupling and improved scalability.

- **Asynchronous Processing**: Messages in Queue Storage can trigger asynchronous processing tasks, such as background jobs, batch processing, or distributed processing across multiple instances of an application.

- **At-Least-Once Delivery**: Queue Storage guarantees at-least-once delivery of messages, meaning that each message will be delivered to a receiver at least once, but it may be delivered multiple times in case of failures.

- **Scalability and Durability**: Queue Storage scales automatically to accommodate increasing message volumes and provides built-in redundancy and durability to ensure message persistence and availability.

### 3. Service Bus:

Azure Service Bus is a fully managed enterprise messaging service that enables reliable and secure communication between applications and services. Here's an overview:

- **Message Queues and Topics/Subscriptions**: Service Bus supports both message queues and topics. Message queues provide point-to-point communication, while topics enable publish-subscribe messaging patterns using subscriptions.

- **Brokered Messaging**: Service Bus provides brokered messaging features such as message routing, session management, and transaction support, making it suitable for complex messaging scenarios.

- **Dead-Letter Queues**: Service Bus includes dead-letter queues, where messages that cannot be delivered after multiple delivery attempts are automatically moved. Dead-letter queues help in troubleshooting and handling message processing errors.

- **Advanced Features**: Service Bus offers advanced features such as message locking, scheduled message delivery, message deferral, and duplicate detection, allowing for precise control over message processing and delivery.

- **Enterprise-Grade Security**: Service Bus provides enterprise-grade security features such as access control, encryption at rest, and transport-level security to ensure the confidentiality, integrity, and availability of messages.

In summary, Event Grid, Queue Storage, and Service Bus are essential Azure services for building scalable, reliable, and event-driven applications. They facilitate asynchronous communication, message processing, and event-driven workflows in various Azure scenarios.

## Key-terms

### Azure Event Grid:

1. **Event**: A notification of a change in a resource. Events can include information such as the source, type, and data associated with the change.

2. **Event Source**: The service or resource that emits events. Examples include Blob Storage, Azure Functions, Azure IoT Hub, and custom publishers.

3. **Event Handler**: A component or endpoint that subscribes to events and reacts to them. Event handlers can be Azure Functions, Azure Logic Apps, webhooks, or custom applications.

4. **Topic**: A logical grouping of related events. Event sources publish events to topics, and subscribers can subscribe to one or more topics to receive events.

5. **Subscription**: A subscription defines the destination for events within a topic. Subscriptions can filter events based on event type or subject pattern.

6. **Event Grid Schema**: The structure of an event, including standard properties such as event type, subject, data, and metadata.

7. **Event Delivery**: The process of delivering events from event sources to event handlers. Event Grid supports both push-based (HTTP/WebHook) and pull-based (Azure Event Hubs) delivery models.

8. **Retry Policy**: Event Grid automatically retries event delivery in case of transient failures. You can configure the retry policy to control the number of retries, interval between retries, and back-off strategy.

### Azure Queue Storage:

1. **Queue**: A storage entity used to store messages. Messages are added to the end of the queue by producers and retrieved from the front of the queue by consumers.

2. **Message**: A unit of data stored in a queue. Messages typically contain payload data and optional metadata.

3. **FIFO (First-In-First-Out)**: A message delivery guarantee provided by Queue Storage, ensuring that messages are processed in the order they were added to the queue.

4. **Visibility Timeout**: The duration for which a message is invisible to other consumers after it has been dequeued by a consumer. If the message is not deleted within the visibility timeout period, it becomes visible again for other consumers to process.

5. **Peek**: A operation that retrieves messages from the queue without removing them. Peeking allows consumers to inspect messages without dequeuing them.

6. **Dequeue**: An operation that removes a message from the queue for processing by a consumer. Once dequeued, the message is no longer visible to other consumers.

7. **Dead-Letter Queue**: A separate queue used to store messages that cannot be processed successfully after multiple delivery attempts. Dead-letter queues help in identifying and troubleshooting message processing errors.

### Azure Service Bus:

1. **Message Broker**: A service that mediates communication between message producers and consumers. Service Bus acts as a message broker, ensuring reliable and secure message delivery.

2. **Queue**: A destination for storing and processing messages in a first-in-first-out (FIFO) manner. Queues provide point-to-point communication between producers and consumers.

3. **Topic**: A logical container for publishing and subscribing to messages. Topics support publish-subscribe messaging patterns, where multiple subscribers can receive messages based on their interests.

4. **Subscription**: A filter-based subscription to a topic. Subscriptions define the criteria for selecting messages from a topic, allowing subscribers to receive only relevant messages.

5. **Message Lock**: A mechanism used to prevent multiple consumers from processing the same message simultaneously. When a message is dequeued by a consumer, it is locked for a specified duration to ensure exclusive processing.

6. **Duplicate Detection**: A feature that prevents the processing of duplicate messages within a specified time window. Service Bus detects and eliminates duplicate messages to ensure message integrity and deduplication.

7. **Partitioning**: A technique for distributing messages across multiple storage partitions to achieve scalability and load balancing. Partitioning enables Service Bus to handle high-throughput scenarios while maintaining message order within each partition.

Understanding these key terms will help you navigate and utilize Azure Event Grid, Queue Storage, and Service Bus effectively for building scalable and reliable messaging and event-driven applications in the Azure cloud.

## Assignment

Gaining practical, cost-free experience with Azure services like Event Grid, Queue Storage, and Service Bus can be achieved through a combination of Azure's free offerings, local development environments, and learning resources. Here's a guide tailored to each service:

### Azure Event Grid:

1. **Azure Free Account**: Sign up for a free Azure account to access Azure Event Grid. You'll receive $200 worth of Azure credits for the first 30 days and limited free services for 12 months.

2. **Microsoft Learn**: Explore Microsoft Learn's free modules on Azure Event Grid. These modules provide hands-on exercises in a sandbox environment where you can practice creating, routing, and reacting to events.

3. **Local Development**: Install the Azure Functions Core Tools and create a local Event Grid emulator using tools like Azure Storage Emulator. This allows you to simulate Event Grid events locally without incurring any costs.

4. **Community Resources**: Engage with the Azure community through forums like Stack Overflow or the Azure subreddit. Participate in discussions, ask questions, and learn from others' experiences with Event Grid.

### Azure Queue Storage:

1. **Azure Free Account**: Utilize your Azure free account to explore Queue Storage. Queue Storage offers a generous free tier, allowing you to store a significant number of messages and perform operations at no cost within the limits.

2. **Local Development**: Install the Azure Storage Emulator or Azure Storage Explorer to create and manage queues locally. You can develop and test queue-based applications without incurring any costs.

3. **Microsoft Learn**: Microsoft Learn provides tutorials and modules on Azure Queue Storage. Follow these tutorials to learn how to create, manage, and process messages in Azure queues within the free sandbox environment.

4. **Sample Applications**: Explore sample applications and GitHub repositories that demonstrate queue-based messaging patterns. Many of these repositories provide sample code and instructions for building and testing queue-based applications.

### Azure Service Bus:

1. **Azure Free Account**: Leverage your Azure free account to experiment with Azure Service Bus. Service Bus offers a free tier with a limited number of messaging units, allowing you to send and receive messages at no cost within the limits.

2. **Microsoft Learn**: Microsoft Learn offers learning paths and modules on Azure Service Bus. These modules include hands-on exercises where you can practice creating topics, subscriptions, and processing messages in a sandbox environment.

3. **Local Development**: Install the Azure Service Bus Explorer or Azure SDKs for .NET, Java, or Python to develop and test Service Bus applications locally. You can simulate topics, subscriptions, and message processing without incurring any costs.

4. **Community Resources**: Engage with the Azure community to learn from others' experiences with Service Bus. Join forums, attend webinars, and participate in community events to expand your knowledge and skills.

By leveraging these methods, you can gain practical experience with Azure Event Grid, Queue Storage, and Service Bus at no cost. Whether you're a beginner or looking to enhance your skills, these resources provide valuable learning opportunities without requiring a financial investment.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

[Omschrijf hoe je weet dat je opdracht gelukt is (gebruik screenshots waar nodig).]