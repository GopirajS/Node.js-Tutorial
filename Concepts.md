# **Node.js & Microservices – Complete Quick Revision**

This is a combined revision reference covering all 11 topics. Each concept has a simple meaning that you can quickly understand and remember for interviews.

# **1. Important Scaling Concepts**

| Concept                        | Simple Meaning                                                                      |
| ------------------------------ | ----------------------------------------------------------------------------------- |
| Scalability                    | The ability of an application to handle increasing traffic and workload.            |
| Application Scaling            | Increasing application resources to handle more requests.                           |
| Vertical Scaling               | Increasing CPU, RAM, or other resources on an existing server.                      |
| Horizontal Scaling             | Adding more servers or application instances to handle traffic.                     |
| Single Server Architecture     | Running the application on one server.                                              |
| Multiple Server Architecture   | Running the application across multiple servers.                                    |
| Application Instance           | One running copy of an application.                                                 |
| Concurrent Users               | Multiple users accessing an application at the same time.                           |
| Requests Per Second (RPS)      | Number of requests a server handles per second.                                     |
| Throughput                     | Amount of work processed within a specific time.                                    |
| Latency                        | Time taken to process a request and return a response.                              |
| Response Time                  | Total time taken to respond to a request.                                           |
| Bottleneck                     | A component that limits overall application performance.                            |
| CPU Utilization                | Percentage of CPU resources being used.                                             |
| Memory Utilization             | Amount of RAM currently being used.                                                 |
| Resource Optimization          | Using CPU, memory, and other resources efficiently.                                 |
| Load Distribution              | Distributing incoming requests across multiple servers.                             |
| Load Balancer                  | Distributes incoming requests across multiple application servers.                  |
| Health Check                   | Checks whether a server or application is working properly.                         |
| Auto Scaling                   | Automatically increasing or decreasing application instances based on demand.       |
| Minimum Instances              | Minimum number of application instances that must run.                              |
| Maximum Instances              | Maximum number of application instances allowed.                                    |
| Scale Up                       | Increase resources on an existing server.                                           |
| Scale Down                     | Reduce resources on an existing server.                                             |
| Scale Out                      | Add more servers or instances.                                                      |
| Scale In                       | Remove unnecessary servers or instances.                                            |
| High Availability (HA)         | Keeping an application available even when some components fail.                    |
| Fault Tolerance                | Ability to continue operating when some components fail.                            |
| Single Point of Failure (SPOF) | One component whose failure can stop the entire system.                             |
| Redundancy                     | Keeping additional resources available as backups.                                  |
| Graceful Shutdown              | Closing an application safely without abruptly interrupting active work.            |
| Zero-Downtime Deployment       | Deploying a new version without making the application unavailable.                 |
| Rolling Deployment             | Updating application instances gradually, one group at a time.                      |
| Blue-Green Deployment          | Maintaining two environments and switching traffic from the old one to the new one. |
| Canary Deployment              | Releasing a new version to a small percentage of users first.                       |
| Rollback                       | Returning to a previously working application version.                              |

# **2. Cluster, PM2 & Load Balancing**

| Concept                  | Simple Meaning                                                                    |
| ------------------------ | --------------------------------------------------------------------------------- |
| Node.js Single Thread    | JavaScript application code normally runs on one main thread per Node.js process. |
| Event Loop               | Handles asynchronous callbacks and coordinates non-blocking operations.           |
| Cluster Module           | Creates multiple Node.js worker processes that can share a server port.           |
| Primary Process          | Manages and coordinates worker processes in a Node.js cluster.                    |
| Worker Process           | A separate Node.js process that handles application requests.                     |
| Multi-Core Processing    | Using multiple CPU cores to execute work in parallel.                             |
| Worker Restart           | Starting a new worker when an existing worker crashes.                            |
| Process Management       | Starting, stopping, monitoring, and restarting application processes.             |
| PM2                      | A process manager for Node.js applications.                                       |
| PM2 Fork Mode            | Runs an application as a single process managed by PM2.                           |
| PM2 Cluster Mode         | Runs multiple application instances using available CPU cores.                    |
| PM2 Reload               | Restarts or reloads application processes with minimal downtime.                  |
| PM2 Monitoring           | Tracks application CPU, memory, uptime, and other process information.            |
| Memory Leak              | Memory that is no longer needed but is not released properly.                     |
| Heap Snapshot            | A record of objects currently stored in the JavaScript heap.                      |
| Reverse Proxy            | A server that receives client requests and forwards them to backend servers.      |
| Nginx                    | A web server commonly used as a reverse proxy and load balancer.                  |
| Load Balancing Algorithm | A method used to distribute requests between servers.                             |
| Round Robin              | Distributes requests between servers in sequence.                                 |
| Weighted Round Robin     | Sends more requests to servers with higher assigned weights.                      |
| Least Connections        | Sends requests to the server with the fewest active connections.                  |
| IP Hash                  | Selects a server based on the client's IP address.                                |
| Sticky Session           | Tries to route requests from the same client to the same server.                  |
| Session Persistence      | Maintains a user's session across multiple requests.                              |
| Shared Session Storage   | Stores sessions in a common storage such as Redis.                                |
| Worker Failure           | A worker process stops unexpectedly.                                              |
| Graceful Restart         | Restarts a process while allowing active requests to finish.                      |
| Process Monitoring       | Observing application processes to detect failures and resource issues.           |

# **3. Microservices Architecture**

| Concept                    | Simple Meaning                                                                                 |
| -------------------------- | ---------------------------------------------------------------------------------------------- |
| Monolithic Architecture    | An application where multiple business functionalities are developed and deployed as one unit. |
| Microservices Architecture | An application divided into small, independently manageable services.                          |
| Microservice               | A small service responsible for a specific business capability.                                |
| Service Boundary           | The boundary that defines what a service owns and manages.                                     |
| Bounded Context            | A clearly defined business domain with its own model and terminology.                          |
| Single Responsibility      | A service should focus on one main business responsibility.                                    |
| Loose Coupling             | Services should have minimal dependency on each other.                                         |
| High Cohesion              | Related business responsibilities should stay together.                                        |
| Independent Deployment     | Deploying one service without deploying every other service.                                   |
| Independent Scaling        | Scaling only the services that need additional resources.                                      |
| Database per Service       | Each microservice owns and manages its own database.                                           |
| Shared Database            | Multiple services access the same database.                                                    |
| Data Ownership             | Each service is responsible for managing its own business data.                                |
| Service Dependency         | One service depends on another service to complete an operation.                               |
| Service Contract           | An agreed interface that defines how services communicate.                                     |
| API Contract               | Defines API endpoints, request formats, responses, and expected behavior.                      |
| Domain-Driven Design (DDD) | Designing software around business domains and their rules.                                    |
| Service Decomposition      | Breaking a large application into smaller services.                                            |
| Service Discovery          | Finding the network location of an available service.                                          |
| Distributed Application    | An application whose components run across multiple processes or machines.                     |
| Shared Business Logic      | Business rules used by multiple parts of an application.                                       |
| Shared Library             | Reusable code package used by multiple services.                                               |
| Strangler Pattern          | Gradually replacing parts of a monolith with microservices.                                    |
| Modular Monolith           | A single deployable application divided into well-separated modules.                           |
| Service Orchestration      | Coordinating multiple services through a central controller.                                   |
| Service Choreography       | Services coordinate through events without a central controller.                               |

# **4. Microservices Communication**

| Concept                          | Simple Meaning                                                                      |
| -------------------------------- | ----------------------------------------------------------------------------------- |
| Synchronous Communication        | One service waits for another service's response.                                   |
| Asynchronous Communication       | One service sends work or a message without waiting for immediate completion.       |
| Request-Response                 | A client sends a request and receives a response.                                   |
| REST API                         | An HTTP-based approach for communication between applications and services.         |
| HTTP                             | A protocol used for communication between clients and servers.                      |
| HTTPS                            | HTTP communication protected by TLS encryption.                                     |
| API Endpoint                     | A specific URL where an API operation can be accessed.                              |
| HTTP Methods                     | Methods such as GET, POST, PUT, PATCH, and DELETE.                                  |
| HTTP Status Code                 | A number indicating the result of an HTTP request.                                  |
| gRPC                             | A high-performance remote procedure call framework commonly using Protocol Buffers. |
| Protocol Buffers                 | A compact format for serializing structured data.                                   |
| WebSocket                        | A protocol that provides persistent, two-way communication.                         |
| Webhook                          | An HTTP callback sent when a specific event occurs.                                 |
| Message Broker                   | A system that receives, stores, and delivers messages between services.             |
| Producer                         | A service that sends messages.                                                      |
| Consumer                         | A service that receives and processes messages.                                     |
| Message Payload                  | The data contained inside a message.                                                |
| Event                            | A record that something has happened in the system.                                 |
| Event Notification               | A message informing another service that an event occurred.                         |
| Service-to-Service Communication | Communication between backend services.                                             |
| API Timeout                      | Maximum time allowed for an API request to complete.                                |
| Retry                            | Attempting a failed operation again.                                                |
| Exponential Backoff              | Increasing the delay between retry attempts.                                        |
| Idempotent Operation             | An operation that produces the same intended result when repeated.                  |
| Correlation ID                   | An identifier used to track related requests across services.                       |
| Distributed Tracing              | Tracking one request as it travels across multiple services.                        |
| API Versioning                   | Maintaining different versions of an API.                                           |
| Backward Compatibility           | Allowing older clients to continue working after changes.                           |

# **5. API Gateway & Service Discovery**

| Concept                   | Simple Meaning                                                              |
| ------------------------- | --------------------------------------------------------------------------- |
| API Gateway               | A single entry point that routes client requests to backend services.       |
| Single Entry Point        | Clients access multiple services through one common endpoint.               |
| Request Routing           | Sending a request to the correct backend service.                           |
| Gateway Authentication    | Checking the identity of a client at the gateway.                           |
| Gateway Authorization     | Checking whether a client is allowed to access a resource.                  |
| Authentication            | Verifying who a user or service is.                                         |
| Authorization             | Checking what an authenticated user or service can do.                      |
| JWT                       | A token format used to securely represent claims between parties.           |
| OAuth 2.0                 | An authorization framework that allows applications to access resources.    |
| OpenID Connect (OIDC)     | An identity layer built on top of OAuth 2.0.                                |
| Identity Provider (IdP)   | A system that authenticates users and issues identity information.          |
| Rate Limiting             | Restricting how many requests a client can make within a time period.       |
| Throttling                | Controlling or slowing down request traffic when necessary.                 |
| HTTP 429                  | Status code indicating too many requests.                                   |
| Request Validation        | Checking whether incoming request data is valid.                            |
| Gateway Caching           | Temporarily storing responses to reduce backend requests.                   |
| Gateway Load Balancing    | Distributing gateway traffic across backend service instances.              |
| Gateway High Availability | Running multiple gateway instances to avoid a single point of failure.      |
| Service Registry          | A system that stores service names and their available network locations.   |
| Service Registration      | A service registering its location with a registry.                         |
| Service Discovery         | Finding available service instances dynamically.                            |
| Dynamic Service Discovery | Automatically finding service instances without hardcoding their addresses. |
| Static Service Discovery  | Configuring service addresses manually.                                     |
| Health-Based Discovery    | Selecting only healthy service instances.                                   |
| Consul                    | A tool that provides service discovery and health checking.                 |
| Kubernetes Service        | A stable network endpoint for accessing a group of Kubernetes pods.         |
| Environment Variables     | Configuration values supplied to an application through its environment.    |
| Centralized Configuration | Managing configuration for multiple services in one central place.          |
| Secrets Management        | Securely storing passwords, API keys, and other sensitive values.           |
| API Versioning Strategy   | Managing API changes while supporting existing clients.                     |

# **6. Database Scaling in Microservices**

| Concept                       | Simple Meaning                                                                                 |
| ----------------------------- | ---------------------------------------------------------------------------------------------- |
| Database per Service          | Each microservice owns its database.                                                           |
| Shared Database               | Multiple services access the same database.                                                    |
| Database Ownership            | A service controls its own data and schema.                                                    |
| Database Isolation            | Preventing services from directly depending on each other's database.                          |
| Data Duplication              | Storing copies of the same information in different locations.                                 |
| Data Synchronization          | Keeping related data copies updated.                                                           |
| Eventual Consistency          | Different data copies become consistent after some time.                                       |
| Strong Consistency            | A successful update is immediately visible to subsequent consistent reads.                     |
| Distributed Transaction       | A business transaction involving multiple services or databases.                               |
| Saga Pattern                  | Managing a business transaction through multiple local transactions.                           |
| Saga Choreography             | Services coordinate a Saga by publishing and consuming events.                                 |
| Saga Orchestration            | A central coordinator controls the Saga steps.                                                 |
| Compensating Transaction      | A business operation that reverses or offsets a previous operation.                            |
| Read Replica                  | A replicated database instance used mainly for read operations.                                |
| Primary Database              | The main database that handles writes and coordinates replication.                             |
| Read/Write Separation         | Sending read operations to replicas and write operations to the primary.                       |
| Replication                   | Copying data from one database to another.                                                     |
| Replication Lag               | The delay between a primary database update and its appearance on a replica.                   |
| Vertical Scaling              | Increasing resources on a database server.                                                     |
| Horizontal Scaling            | Distributing database workload across multiple servers.                                        |
| Database Partitioning         | Dividing a large table into smaller parts.                                                     |
| Range Partitioning            | Dividing data based on ranges, such as dates or IDs.                                           |
| List Partitioning             | Dividing data based on a list of predefined values.                                            |
| Hash Partitioning             | Distributing records based on a hash of a selected value.                                      |
| Database Sharding             | Distributing database records across multiple database servers.                                |
| Shard                         | One individual part of a sharded database.                                                     |
| Shard Key                     | The field used to determine which shard stores a record.                                       |
| Shard Rebalancing             | Redistributing data when the number or capacity of shards changes.                             |
| Database Index                | A data structure that helps retrieve records faster.                                           |
| Query Optimization            | Improving SQL queries to reduce execution time and resource usage.                             |
| Batch Processing              | Processing multiple database records in one operation or group.                                |
| Database Migration            | Changing database structure through controlled schema updates.                                 |
| Schema Versioning             | Tracking changes to database structure over time.                                              |
| Backward-Compatible Migration | Changing a schema without breaking older application versions.                                 |
| Expand-and-Contract           | Adding new schema structures first, migrating application usage, then removing old structures. |
| Reconciliation                | Comparing related records and correcting inconsistencies.                                      |

# **7. Message Queues & Event-Driven Architecture**

| Concept                         | Simple Meaning                                                                                                  |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Message Queue                   | A system that stores messages until consumers process them.                                                     |
| Message Broker                  | Middleware that receives and delivers messages between applications.                                            |
| Producer                        | Application or service that publishes messages.                                                                 |
| Consumer                        | Application or service that processes messages.                                                                 |
| Queue                           | A collection of messages waiting to be processed.                                                               |
| Topic                           | A named channel where events or messages are published.                                                         |
| Publisher                       | A component that sends messages to a broker or topic.                                                           |
| Subscriber                      | A component that receives messages from a topic.                                                                |
| Event-Driven Architecture (EDA) | An architecture where services communicate by publishing and reacting to events.                                |
| Event                           | A record that something has happened.                                                                           |
| Event Publisher                 | A service that publishes an event.                                                                              |
| Event Consumer                  | A service that reacts to an event.                                                                              |
| Event Payload                   | Data included in an event.                                                                                      |
| Message Acknowledgment (ACK)    | Confirmation that a message was successfully processed or received, depending on broker semantics.              |
| Negative Acknowledgment (NACK)  | Indication that a message was not successfully processed.                                                       |
| Message Retry                   | Attempting to process a failed message again.                                                                   |
| Dead Letter Queue (DLQ)         | A separate queue for messages that cannot be processed successfully.                                            |
| Message Persistence             | Saving messages so they can survive broker restarts.                                                            |
| Message Durability              | Ensuring messages or queues are retained according to broker configuration.                                     |
| Message Ordering                | Maintaining the required order of message processing.                                                           |
| Message Priority                | Giving certain messages higher processing priority.                                                             |
| Consumer Group                  | A group of consumers that share message-processing work.                                                        |
| Competing Consumers             | Multiple consumers process messages from the same queue.                                                        |
| Fan-Out                         | Delivering one event to multiple subscribers.                                                                   |
| Pub/Sub                         | A communication pattern where publishers send messages and subscribers receive them.                            |
| Point-to-Point                  | A messaging pattern where a message is processed by one consumer from a queue.                                  |
| At-Most-Once Delivery           | A message is delivered zero or one time, so it may be lost.                                                     |
| At-Least-Once Delivery          | A message is delivered one or more times, so duplicates are possible.                                           |
| Exactly-Once Processing         | A guarantee of one effective processing result within a defined system boundary; requires careful coordination. |
| Duplicate Message               | The same message is delivered more than once.                                                                   |
| Idempotent Consumer             | A consumer that safely handles duplicate messages.                                                              |
| Transactional Outbox            | Stores business data and an outgoing event record in the same database transaction.                             |
| Change Data Capture (CDC)       | Capturing database changes and publishing them to other systems.                                                |
| Event Schema                    | The defined structure and fields of an event.                                                                   |
| Event Versioning                | Managing changes to event structures over time.                                                                 |
| Event Replay                    | Processing previously stored events again.                                                                      |
| Backpressure                    | Controlling incoming work when consumers cannot process it fast enough.                                         |
| Queue Lag                       | The amount of unprocessed messages waiting in a queue or topic.                                                 |
| RabbitMQ                        | A message broker commonly used for queue-based messaging.                                                       |
| Apache Kafka                    | A distributed event-streaming platform.                                                                         |
| AWS SQS                         | A managed message queuing service.                                                                              |
| BullMQ                          | A Redis-based job and message queue library for Node.js.                                                        |

# **8. Distributed Systems & Reliability**

| Concept                        | Simple Meaning                                                                                                         |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------- |
| Distributed System             | Multiple computers or services working together as one system.                                                         |
| Distributed Node               | An individual machine or service in a distributed system.                                                              |
| Network Partition              | A communication failure that separates parts of a distributed system.                                                  |
| Network Latency                | Time taken for data to travel across a network.                                                                        |
| Network Timeout                | A request takes longer than the allowed time.                                                                          |
| Partial Failure                | Some components fail while other components continue working.                                                          |
| Fault Tolerance                | Ability to continue operating despite component failures.                                                              |
| High Availability              | Keeping a service accessible with minimal downtime.                                                                    |
| Reliability                    | Ability of a system to perform correctly over time.                                                                    |
| Resilience                     | Ability to recover from failures and continue operating.                                                               |
| Redundancy                     | Maintaining additional components to avoid service interruption.                                                       |
| Failover                       | Switching to a backup component when the primary component fails.                                                      |
| Failback                       | Returning operations to the primary component after recovery.                                                          |
| Retry Mechanism                | Attempting failed operations again.                                                                                    |
| Retry Limit                    | Maximum number of retry attempts.                                                                                      |
| Exponential Backoff            | Increasing the delay between retries.                                                                                  |
| Jitter                         | Adding randomness to retry delays to prevent many clients retrying together.                                           |
| Circuit Breaker                | Temporarily stopping calls to a failing service to prevent further failures.                                           |
| Circuit Breaker – Closed       | Requests are allowed normally.                                                                                         |
| Circuit Breaker – Open         | Requests are blocked temporarily.                                                                                      |
| Circuit Breaker – Half-Open    | A limited number of test requests are allowed to check recovery.                                                       |
| Fallback                       | An alternative response or operation used when a service fails.                                                        |
| Timeout                        | A maximum allowed duration for an operation.                                                                           |
| Bulkhead Pattern               | Isolating resources so failure in one area does not exhaust the entire system.                                         |
| Rate Limiting                  | Restricting the number of requests within a time period.                                                               |
| Load Shedding                  | Rejecting or dropping lower-priority work when overloaded.                                                             |
| Idempotency                    | Repeating an operation without creating additional unintended effects.                                                 |
| Idempotency Key                | A unique identifier used to recognize repeated requests.                                                               |
| Eventual Consistency           | Data becomes consistent across services over time.                                                                     |
| CAP Theorem                    | In the presence of a network partition, a distributed data system must trade off between consistency and availability. |
| Consistency                    | All relevant reads observe data according to the system's consistency guarantee.                                       |
| Availability                   | A system continues responding to requests.                                                                             |
| Partition Tolerance            | A system continues operating despite network communication failures between nodes.                                     |
| Leader Election                | Selecting one node to coordinate a particular distributed task.                                                        |
| Distributed Lock               | A lock used to coordinate access to a shared resource across multiple processes or machines.                           |
| Race Condition                 | The result depends on the timing or order of concurrent operations.                                                    |
| Deadlock                       | Processes wait indefinitely for resources held by one another.                                                         |
| Concurrency                    | Multiple tasks make progress during overlapping periods.                                                               |
| Parallelism                    | Multiple tasks execute at the same time.                                                                               |
| Distributed Tracing            | Tracking a request across multiple services.                                                                           |
| Correlation ID                 | An identifier that connects related operations across services.                                                        |
| Disaster Recovery              | Restoring a system after a major failure.                                                                              |
| Recovery Point Objective (RPO) | Maximum acceptable amount of data loss measured in time.                                                               |
| Recovery Time Objective (RTO)  | Maximum acceptable time to restore a service.                                                                          |

# **9. Docker, Kubernetes & Deployment**

| Concept                         | Simple Meaning                                                          |
| ------------------------------- | ----------------------------------------------------------------------- |
| Containerization                | Packaging an application and its dependencies into a container.         |
| Docker                          | A platform for building and running containers.                         |
| Docker Image                    | A packaged template used to create containers.                          |
| Docker Container                | A running instance of a Docker image.                                   |
| Dockerfile                      | Instructions used to build a Docker image.                              |
| Docker Build                    | Creating an image from a Dockerfile.                                    |
| Docker Registry                 | A place to store and distribute Docker images.                          |
| Docker Hub                      | A public container image registry.                                      |
| Container Runtime               | Software responsible for running containers.                            |
| Container Networking            | Communication between containers and external systems.                  |
| Docker Volume                   | Persistent storage used by containers.                                  |
| Docker Compose                  | A tool for defining and running multi-container applications.           |
| Multi-Stage Build               | Using multiple build stages to create smaller production images.        |
| Environment Configuration       | Providing different configuration values for each environment.          |
| Container Orchestration         | Managing container deployment, scaling, networking, and recovery.       |
| Kubernetes (K8s)                | A platform for orchestrating containerized applications.                |
| Kubernetes Cluster              | A group of machines managed by Kubernetes.                              |
| Node                            | A machine that runs Kubernetes workloads.                               |
| Control Plane                   | The Kubernetes components that manage the cluster.                      |
| Worker Node                     | A machine that runs application workloads.                              |
| Pod                             | The smallest deployable unit in Kubernetes.                             |
| Deployment                      | A Kubernetes resource that manages replicated application pods.         |
| ReplicaSet                      | Maintains the desired number of running pods.                           |
| Service                         | Provides a stable network endpoint for accessing pods.                  |
| Ingress                         | Manages external HTTP/HTTPS access to services in a Kubernetes cluster. |
| ConfigMap                       | Stores non-sensitive application configuration.                         |
| Secret                          | Stores sensitive configuration data.                                    |
| Persistent Volume (PV)          | A storage resource available to Kubernetes workloads.                   |
| Persistent Volume Claim (PVC)   | A request for persistent storage.                                       |
| Namespace                       | Logically separates resources inside a Kubernetes cluster.              |
| Horizontal Pod Autoscaler (HPA) | Automatically adjusts pod replicas based on configured metrics.         |
| Liveness Probe                  | Checks whether a container is alive and should continue running.        |
| Readiness Probe                 | Checks whether a container is ready to receive traffic.                 |
| Startup Probe                   | Checks whether an application has finished starting.                    |
| Rolling Update                  | Gradually replaces old pods with new ones.                              |
| Rollback                        | Reverts a deployment to an earlier version.                             |
| Resource Requests               | CPU and memory resources requested by a container.                      |
| Resource Limits                 | Maximum CPU and memory resources a container can use.                   |
| CI/CD                           | Automating application building, testing, and deployment.               |
| Continuous Integration (CI)     | Automatically building and testing code changes.                        |
| Continuous Delivery             | Keeping changes ready for deployment.                                   |
| Continuous Deployment           | Automatically deploying changes after successful pipeline checks.       |
| Infrastructure as Code (IaC)    | Managing infrastructure through configuration files and code.           |
| Helm                            | A package manager for Kubernetes applications.                          |

# **10. Monitoring, Logging & Production Troubleshooting**

| Concept                                  | Simple Meaning                                                                 |
| ---------------------------------------- | ------------------------------------------------------------------------------ |
| Monitoring                               | Continuously checking application and infrastructure health.                   |
| Logging                                  | Recording application events and errors.                                       |
| Metrics                                  | Numerical measurements that describe application performance.                  |
| Tracing                                  | Tracking the path of a request across application components.                  |
| Observability                            | Understanding a system's internal state using logs, metrics, and traces.       |
| Application Performance Monitoring (APM) | Monitoring application performance and identifying bottlenecks.                |
| Error Monitoring                         | Detecting and tracking application errors.                                     |
| Centralized Logging                      | Collecting logs from multiple services in one place.                           |
| Structured Logging                       | Recording logs in a consistent format, often JSON.                             |
| Log Level                                | The severity category of a log message.                                        |
| DEBUG                                    | Detailed information useful for debugging.                                     |
| INFO                                     | Normal application activity.                                                   |
| WARN                                     | A potential problem that does not necessarily stop the application.            |
| ERROR                                    | An operation or request failed.                                                |
| FATAL                                    | A critical failure that may stop the application.                              |
| Request ID                               | An identifier used to track an individual request.                             |
| Correlation ID                           | An identifier used to connect related operations across services.              |
| Distributed Tracing                      | Following requests through multiple services.                                  |
| Trace                                    | The complete recorded journey of a request.                                    |
| Span                                     | One operation within a trace.                                                  |
| Trace ID                                 | An identifier for an entire distributed trace.                                 |
| Span ID                                  | An identifier for one operation within a trace.                                |
| CPU Monitoring                           | Tracking processor usage.                                                      |
| Memory Monitoring                        | Tracking application memory consumption.                                       |
| Disk Monitoring                          | Tracking disk usage and performance.                                           |
| Network Monitoring                       | Tracking network traffic, latency, and errors.                                 |
| Database Monitoring                      | Tracking database queries, connections, and performance.                       |
| Slow Query                               | A database query that takes longer than expected.                              |
| Connection Pool                          | A reusable collection of database connections.                                 |
| Connection Pool Exhaustion               | All available database connections are busy or unavailable.                    |
| Event Loop Lag                           | Delay in the Node.js event loop responding to scheduled work.                  |
| Heap Usage                               | Amount of JavaScript heap memory currently used.                               |
| Memory Leak Detection                    | Identifying memory that is unnecessarily retained.                             |
| Uptime                                   | How long an application has been running or available.                         |
| Downtime                                 | Period when an application or service is unavailable.                          |
| SLA                                      | An agreement defining expected service availability or performance.            |
| SLI                                      | A measurable indicator of service performance or reliability.                  |
| SLO                                      | A target value for a service-level indicator.                                  |
| Error Rate                               | Percentage or number of requests that fail.                                    |
| Latency Percentile                       | A latency measurement at a particular percentile, such as P95 or P99.          |
| P95 Latency                              | The response time within which 95% of requests complete.                       |
| P99 Latency                              | The response time within which 99% of requests complete.                       |
| Alerting                                 | Notifying a team when a monitored condition crosses a threshold.               |
| Incident                                 | An event that disrupts or degrades a service.                                  |
| Root Cause Analysis (RCA)                | Finding the underlying reason for a failure.                                   |
| Postmortem                               | Reviewing an incident to understand what happened and prevent recurrence.      |
| Prometheus                               | A monitoring and metrics collection system.                                    |
| Grafana                                  | A platform for visualizing metrics and dashboards.                             |
| ELK Stack                                | Elasticsearch, Logstash, and Kibana for log collection, storage, and analysis. |
| OpenTelemetry                            | A standard toolkit for collecting traces, metrics, and logs.                   |
| Sentry                                   | A tool for error tracking and performance monitoring.                          |

# **11. Real-Time System Design Scenarios**

| Concept                     | Simple Meaning                                                                                      |
| --------------------------- | --------------------------------------------------------------------------------------------------- |
| System Design               | Planning the architecture and components of an application.                                         |
| High-Level Design (HLD)     | Describes the main components and how they interact.                                                |
| Low-Level Design (LLD)      | Describes detailed implementation, classes, modules, and data structures.                           |
| Functional Requirements     | What the system should do.                                                                          |
| Non-Functional Requirements | How well the system should perform, scale, and remain secure.                                       |
| Traffic Estimation          | Estimating the number of users and requests a system must handle.                                   |
| Capacity Planning           | Estimating the resources required to handle expected workloads.                                     |
| API Design                  | Defining endpoints, request formats, responses, and error handling.                                 |
| Database Design             | Planning tables, relationships, indexes, and data ownership.                                        |
| Data Modeling               | Defining how application data is structured and related.                                            |
| Caching                     | Temporarily storing frequently used data for faster access.                                         |
| Cache Hit                   | Requested data is available in the cache.                                                           |
| Cache Miss                  | Requested data is not available in the cache.                                                       |
| Cache Invalidation          | Removing or updating outdated cached data.                                                          |
| Cache-Aside                 | Application checks the cache first and loads missing data from the database.                        |
| Write-Through Cache         | Writes data to the cache and backing database together as part of the write strategy.               |
| Write-Behind Cache          | Writes data to the cache first and updates the database later.                                      |
| Redis                       | An in-memory data store commonly used for caching and messaging.                                    |
| CDN                         | A Content Delivery Network that serves content from geographically distributed locations.           |
| Static Content              | Files such as images, CSS, and JavaScript that generally do not change per request.                 |
| Dynamic Content             | Content generated based on user input or application data.                                          |
| Pagination                  | Dividing a large result set into smaller pages.                                                     |
| Offset Pagination           | Retrieving records using an offset and limit.                                                       |
| Cursor Pagination           | Retrieving records using a reference to the last item or another ordering position.                 |
| Search Optimization         | Improving the speed and relevance of search operations.                                             |
| Elasticsearch               | A search and analytics engine used for full-text search and data analysis.                          |
| File Upload Architecture    | Managing file uploads, validation, storage, and retrieval.                                          |
| Object Storage              | Storing files as objects, such as in Amazon S3.                                                     |
| Pre-Signed URL              | A time-limited URL that grants permission to perform a specific storage operation.                  |
| Background Job              | Work processed outside the main HTTP request-response cycle.                                        |
| Job Queue                   | A queue that stores tasks waiting for background processing.                                        |
| Scheduled Job               | A task executed at a predefined time or interval.                                                   |
| Cron Job                    | A scheduled task configured using time-based rules.                                                 |
| Real-Time Notification      | Sending updates to users as events occur.                                                           |
| WebSocket Connection        | A persistent two-way connection between a client and server.                                        |
| Socket.IO                   | A JavaScript library for real-time, event-based communication.                                      |
| Redis Pub/Sub               | A Redis messaging feature for publishing messages to subscribers.                                   |
| Chat System                 | An application that supports real-time messaging between users.                                     |
| Presence                    | Information about whether a user is online, offline, or active.                                     |
| Message Delivery Status     | Indicates whether a message was sent, delivered, or read.                                           |
| E-commerce Order Flow       | A sequence involving cart, order, payment, inventory, and notification services.                    |
| Payment Idempotency         | Preventing duplicate payment processing when requests are repeated.                                 |
| Inventory Management        | Tracking product quantities and stock changes.                                                      |
| Inventory Reservation       | Temporarily reserving stock while an order is being completed.                                      |
| Double Booking              | Assigning the same limited resource to multiple customers unintentionally.                          |
| Concurrency Control         | Managing simultaneous operations to prevent conflicting updates.                                    |
| Optimistic Locking          | Detecting conflicting updates using a version or timestamp check.                                   |
| Pessimistic Locking         | Locking data to prevent other operations from modifying it simultaneously.                          |
| Database Transaction        | A group of database operations handled as one logical unit.                                         |
| ACID                        | Atomicity, Consistency, Isolation, and Durability properties of transactions.                       |
| Race Condition              | A result that depends on the timing of concurrent operations.                                       |
| Idempotency Key             | A unique key used to prevent duplicate processing of repeated requests.                             |
| Security                    | Protecting application data, users, APIs, and infrastructure.                                       |
| Authentication              | Verifying user identity.                                                                            |
| Authorization               | Checking user permissions.                                                                          |
| Encryption                  | Converting data into a protected format.                                                            |
| TLS                         | A protocol that protects data transmitted over a network.                                           |
| Hashing                     | Converting data into a fixed-size digest, commonly used for password verification.                  |
| RBAC                        | Role-Based Access Control; permissions are assigned through roles.                                  |
| CORS                        | Cross-Origin Resource Sharing; controls browser access to cross-origin resources.                   |
| CSRF                        | Cross-Site Request Forgery; tricks a user's browser into sending an unwanted authenticated request. |
| XSS                         | Cross-Site Scripting; injects malicious scripts into web pages.                                     |
| SQL Injection               | Manipulating database queries through unsafe user input.                                            |

# **Important Differences to Remember**

These comparisons are especially useful for scenario-based Node.js and microservices interviews.

## **1. Scaling & Performance Differences**

| Comparison                                  | Difference                                                                                    |
| ------------------------------------------- | --------------------------------------------------------------------------------------------- |
| Vertical Scaling vs Horizontal Scaling      | Vertical adds resources to one server; horizontal adds more servers.                          |
| Scale Up vs Scale Out                       | Scale up increases existing server capacity; scale out adds instances.                        |
| Scale Down vs Scale In                      | Scale down reduces existing server resources; scale in removes instances.                     |
| Throughput vs Latency                       | Throughput measures work completed per time; latency measures time taken for an operation.    |
| Concurrency vs Parallelism                  | Concurrency allows overlapping progress; parallelism executes tasks simultaneously.           |
| High Availability vs Fault Tolerance        | High availability minimizes downtime; fault tolerance continues operating despite failures.   |
| Redundancy vs Failover                      | Redundancy provides extra components; failover switches operations to a backup.               |
| Load Balancing vs Auto Scaling              | Load balancing distributes traffic; auto scaling changes the number of instances.             |
| Rolling Deployment vs Blue-Green Deployment | Rolling updates instances gradually; blue-green switches between two environments.            |
| Blue-Green vs Canary Deployment             | Blue-green switches environments; canary gradually exposes a new version to selected traffic. |

## **2. Cluster, PM2 & Load Balancing Differences**

| Comparison                              | Difference                                                                                                                                                                |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Process vs Thread                       | A process has its own memory space; threads execute within a process and share its memory.                                                                                |
| Cluster vs Worker Threads               | Cluster creates separate processes; worker threads create additional threads within a process.                                                                            |
| Cluster vs PM2                          | Cluster is a Node.js module; PM2 is a process manager that can run applications in cluster mode.                                                                          |
| Fork Mode vs Cluster Mode               | Fork mode runs a single managed process; cluster mode runs multiple instances.                                                                                            |
| Primary Process vs Worker Process       | Primary manages workers; workers handle application work.                                                                                                                 |
| Reverse Proxy vs Load Balancer          | A reverse proxy forwards client requests to backend servers; a load balancer distributes traffic among multiple servers. A reverse proxy can also act as a load balancer. |
| Round Robin vs Least Connections        | Round Robin distributes sequentially; Least Connections prefers the server with fewer active connections.                                                                 |
| Sticky Session vs Shared Session        | Sticky session routes a client to a particular server; shared session stores session data centrally.                                                                      |
| Restart vs Reload                       | Restart stops and starts a process; reload replaces processes in a controlled way, potentially reducing downtime.                                                         |
| Graceful Shutdown vs Immediate Shutdown | Graceful shutdown allows active work to finish; immediate shutdown terminates without waiting.                                                                            |

## **3. Microservices Architecture Differences**

| Comparison                                       | Difference                                                                                                                           |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| Monolith vs Microservices                        | Monolith is deployed as one application; microservices are independently deployable services.                                        |
| Monolith vs Modular Monolith                     | Monolith may have tightly connected modules; modular monolith enforces clearer internal boundaries but remains one deployment.       |
| Microservice vs Module                           | A microservice can run and deploy independently; a module is part of an application.                                                 |
| Tight Coupling vs Loose Coupling                 | Tight coupling means strong dependencies; loose coupling means fewer dependencies.                                                   |
| High Cohesion vs Low Cohesion                    | High cohesion keeps related responsibilities together; low cohesion mixes unrelated responsibilities.                                |
| Shared Database vs Database per Service          | Shared database is accessed by multiple services; database per service gives each service ownership of its data.                     |
| Service Orchestration vs Choreography            | Orchestration uses a central coordinator; choreography uses events and independent service reactions.                                |
| API Communication vs Event Communication         | API communication requests data or an operation; event communication announces that something happened.                              |
| Independent Deployment vs Coordinated Deployment | Independent deployment releases one service separately; coordinated deployment requires multiple components to be released together. |

## **4. Microservices Communication Differences**

| Comparison                               | Difference                                                                                                                             |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Synchronous vs Asynchronous              | Synchronous waits for a response; asynchronous does not need an immediate response.                                                    |
| REST vs gRPC                             | REST commonly uses HTTP and JSON; gRPC commonly uses HTTP/2 and Protocol Buffers.                                                      |
| REST vs WebSocket                        | REST uses request-response communication; WebSocket provides persistent two-way communication.                                         |
| WebSocket vs Webhook                     | WebSocket keeps a two-way connection open; webhook sends an HTTP callback when an event occurs.                                        |
| WebSocket vs HTTP Polling                | WebSocket supports server-pushed messages over a persistent connection; polling repeatedly sends requests to check for updates.        |
| API vs Webhook                           | An API is called by a client; a webhook sends an event notification to a configured endpoint.                                          |
| Timeout vs Retry                         | Timeout limits how long an operation can take; retry attempts the operation again.                                                     |
| Retry vs Exponential Backoff             | Retry repeats an operation; exponential backoff increases the delay between attempts.                                                  |
| Idempotent vs Non-Idempotent             | Idempotent operations can be repeated without additional unintended effects; non-idempotent operations may produce additional effects. |
| Authentication vs Authorization          | Authentication verifies identity; authorization checks permissions.                                                                    |
| JWT vs Session                           | JWT carries signed claims in a token; session-based authentication stores session state on the server or shared session store.         |
| API Versioning vs Backward Compatibility | Versioning maintains different API versions; backward compatibility allows older clients to keep working.                              |

## **5. API Gateway & Service Discovery Differences**

| Comparison                               | Difference                                                                                                                      |
| ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| API Gateway vs Load Balancer             | Gateway manages API-level routing and policies; load balancer distributes traffic across instances.                             |
| API Gateway vs Reverse Proxy             | API Gateway provides API-specific features; reverse proxy forwards requests to backend servers.                                 |
| API Gateway vs Service Registry          | Gateway handles incoming client requests; registry stores service locations.                                                    |
| Static vs Dynamic Service Discovery      | Static uses manually configured addresses; dynamic discovers available instances automatically.                                 |
| Service Registry vs Service Discovery    | Registry stores service information; discovery finds available services using that information.                                 |
| Authentication vs Authorization          | Authentication checks who you are; authorization checks what you can access.                                                    |
| Rate Limiting vs Throttling              | Rate limiting enforces a request quota; throttling controls request speed or traffic.                                           |
| JWT vs OAuth 2.0                         | JWT is a token format; OAuth 2.0 is an authorization framework.                                                                 |
| Environment Variables vs Secrets Manager | Environment variables supply configuration; a secrets manager securely stores and controls access to sensitive credentials.     |
| Consul vs Kubernetes Service             | Consul provides service discovery and related features; Kubernetes Service provides a stable endpoint for Kubernetes workloads. |

## **6. Database Scaling Differences**

| Comparison                                      | Difference                                                                                                                             |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Partitioning vs Sharding                        | Partitioning divides data into smaller parts; sharding distributes data across multiple database servers.                              |
| Vertical vs Horizontal Database Scaling         | Vertical increases database server resources; horizontal distributes database workload across servers.                                 |
| Primary vs Read Replica                         | Primary handles writes; read replica mainly handles reads.                                                                             |
| Replication vs Sharding                         | Replication copies data; sharding distributes different portions of data.                                                              |
| Read Scaling vs Write Scaling                   | Read scaling increases read capacity; write scaling increases the ability to handle write operations.                                  |
| Strong Consistency vs Eventual Consistency      | Strong consistency provides immediate consistency according to its guarantees; eventual consistency allows temporary differences.      |
| Database Transaction vs Distributed Transaction | A database transaction operates within a database transaction boundary; a distributed transaction spans multiple systems or databases. |
| Saga vs Two-Phase Commit                        | Saga uses local transactions and compensating actions; two-phase commit coordinates a distributed commit protocol.                     |
| Choreography vs Orchestration                   | Choreography coordinates through events; orchestration coordinates through a central controller.                                       |
| Retry vs Compensation                           | Retry attempts the operation again; compensation performs a business action to offset an earlier operation.                            |
| Partition Key vs Shard Key                      | Partition key determines a record's partition; shard key determines the shard that stores a record.                                    |
| Indexing vs Partitioning                        | Indexing speeds up data retrieval; partitioning divides a table into smaller data segments.                                            |
| Schema vs Data                                  | Schema defines the database structure; data is the actual stored information.                                                          |
| Migration vs Rollback                           | Migration applies a schema or data change; rollback reverses or restores a previous change where possible.                             |

## **7. Message Queues & Event-Driven Architecture Differences**

| Comparison                                      | Difference                                                                                                                                                      |
| ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Queue vs Topic                                  | A queue commonly distributes messages to competing consumers; a topic supports publishing events to multiple subscribers.                                       |
| Producer vs Consumer                            | Producer sends messages; consumer processes messages.                                                                                                           |
| Publisher vs Subscriber                         | Publisher sends events; subscriber receives events.                                                                                                             |
| Message Queue vs Event Streaming                | A message queue commonly manages work items; event streaming stores ordered event records for consumers to read.                                                |
| RabbitMQ vs Kafka                               | RabbitMQ is a traditional message broker; Kafka is a distributed event-streaming platform.                                                                      |
| Point-to-Point vs Pub/Sub                       | Point-to-point delivers a message to one competing consumer; pub/sub distributes events to subscribers.                                                         |
| Synchronous vs Asynchronous Messaging           | Synchronous communication waits for a response; asynchronous messaging allows processing later.                                                                 |
| ACK vs NACK                                     | ACK confirms successful handling or receipt; NACK indicates unsuccessful handling.                                                                              |
| At-Most-Once vs At-Least-Once                   | At-most-once may lose messages but avoids redelivery; at-least-once may redeliver messages.                                                                     |
| At-Least-Once vs Exactly-Once                   | At-least-once allows duplicates; exactly-once aims for one effective processing result within a defined boundary.                                               |
| Retry vs Dead Letter Queue                      | Retry attempts processing again; DLQ stores messages that repeatedly fail.                                                                                      |
| Event vs Command                                | Event describes something that happened; command requests that something should happen.                                                                         |
| Event Replay vs Retry                           | Replay processes previously stored events again; retry attempts a failed operation again.                                                                       |
| Transactional Outbox vs Direct Event Publishing | Outbox stores the event with business data in one transaction; direct publishing can risk losing an event if the database update succeeds but publishing fails. |
| Message Durability vs Message Persistence       | Durability describes a guarantee that messages survive failures; persistence is the mechanism of storing messages.                                              |
| Queue Lag vs Processing Time                    | Queue lag measures pending work; processing time measures how long a task takes.                                                                                |

## **8. Distributed Systems & Reliability Differences**

| Comparison                          | Difference                                                                                                                                   |
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Reliability vs Availability         | Reliability is consistent correct operation over time; availability is readiness to serve requests.                                          |
| Availability vs Fault Tolerance     | Availability measures accessibility; fault tolerance describes behavior when components fail.                                                |
| Fault Tolerance vs Resilience       | Fault tolerance continues despite failures; resilience includes recovery and adaptation.                                                     |
| Failover vs Failback                | Failover switches to a backup; failback returns to the primary.                                                                              |
| Retry vs Circuit Breaker            | Retry attempts a failed operation again; circuit breaker temporarily blocks calls to an unhealthy service.                                   |
| Circuit Breaker vs Bulkhead         | Circuit breaker stops calls to failing dependencies; bulkhead isolates resources.                                                            |
| Timeout vs Circuit Breaker          | Timeout limits how long a request waits; circuit breaker prevents repeated calls to an unhealthy service.                                    |
| Fallback vs Retry                   | Fallback uses an alternative result; retry attempts the original operation again.                                                            |
| Rate Limiting vs Load Shedding      | Rate limiting restricts incoming request rates; load shedding rejects work when the system is overloaded.                                    |
| Idempotency vs Deduplication        | Idempotency makes repeated operations safe; deduplication identifies and removes repeated messages or requests.                              |
| RPO vs RTO                          | RPO measures acceptable data loss; RTO measures acceptable recovery time.                                                                    |
| Distributed Lock vs Database Lock   | Distributed lock coordinates access across machines; database lock coordinates access to database resources.                                 |
| Race Condition vs Deadlock          | Race condition depends on execution timing; deadlock occurs when operations wait indefinitely for each other.                                |
| Leader Election vs Load Balancing   | Leader election selects a coordinator; load balancing distributes work.                                                                      |
| CAP Consistency vs ACID Consistency | CAP consistency concerns distributed-system behavior during partitions; ACID consistency concerns preserving database rules and constraints. |

## **9. Docker, Kubernetes & Deployment Differences**

| Comparison                                   | Difference                                                                                                |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| Docker Image vs Container                    | Image is a template; container is a running instance of an image.                                         |
| Docker vs Kubernetes                         | Docker builds and runs containers; Kubernetes orchestrates containerized applications.                    |
| Container vs Virtual Machine                 | Containers share the host operating system kernel; VMs run separate guest operating systems.              |
| Dockerfile vs Docker Compose                 | Dockerfile defines how to build an image; Compose defines how to run multiple services.                   |
| Image vs Registry                            | Image packages the application; registry stores and distributes images.                                   |
| Pod vs Container                             | Pod is a Kubernetes deployment unit; container is the application runtime inside it.                      |
| Pod vs Deployment                            | Pod runs containers; Deployment manages desired pod replicas and updates.                                 |
| Deployment vs ReplicaSet                     | Deployment manages rollout and rollback; ReplicaSet maintains the required pod count.                     |
| Kubernetes Service vs Ingress                | Service provides internal or configured network access to pods; Ingress manages HTTP/HTTPS entry routing. |
| ConfigMap vs Secret                          | ConfigMap stores non-sensitive configuration; Secret stores sensitive configuration data.                 |
| Liveness vs Readiness Probe                  | Liveness checks whether the container should restart; readiness checks whether it should receive traffic. |
| Readiness vs Startup Probe                   | Readiness checks whether an app can receive traffic; startup checks whether it has completed startup.     |
| HPA vs Cluster Autoscaler                    | HPA changes pod replica counts; Cluster Autoscaler changes the number of cluster nodes.                   |
| Rolling Update vs Rollback                   | Rolling update deploys a new version gradually; rollback returns to a previous version.                   |
| CI vs CD                                     | CI automatically builds and tests changes; CD prepares or automatically deploys changes.                  |
| Continuous Delivery vs Continuous Deployment | Delivery keeps changes ready for release; deployment releases changes automatically.                      |

## **10. Monitoring, Logging & Production Troubleshooting Differences**

| Comparison                        | Difference                                                                                            |
| --------------------------------- | ----------------------------------------------------------------------------------------------------- |
| Monitoring vs Logging             | Monitoring tracks system health; logging records events and activity.                                 |
| Logging vs Tracing                | Logging records individual events; tracing tracks a request across services.                          |
| Metrics vs Logs                   | Metrics are numerical measurements; logs are event records.                                           |
| Tracing vs Monitoring             | Tracing follows request execution; monitoring tracks overall system health.                           |
| Observability vs Monitoring       | Monitoring checks known conditions; observability helps investigate unknown problems.                 |
| Trace vs Span                     | Trace represents the complete request journey; span represents one operation within that journey.     |
| Trace ID vs Span ID               | Trace ID identifies the complete trace; span ID identifies one operation.                             |
| P95 vs P99 Latency                | P95 covers 95% of requests; P99 covers 99% of requests.                                               |
| SLA vs SLO vs SLI                 | SLA is an agreement; SLO is a target; SLI is the measurement.                                         |
| CPU Usage vs Memory Usage         | CPU measures processor utilization; memory measures RAM consumption.                                  |
| Memory Leak vs High Memory Usage  | Memory leak is memory retained unnecessarily; high memory usage may be normal or caused by workload.  |
| Error Rate vs Latency             | Error rate measures failures; latency measures response time.                                         |
| Root Cause Analysis vs Postmortem | RCA finds the underlying cause; postmortem reviews the incident and improvement actions.              |
| Prometheus vs Grafana             | Prometheus collects and stores metrics; Grafana visualizes data in dashboards.                        |
| ELK vs Prometheus                 | ELK focuses on logs and search; Prometheus focuses on metrics.                                        |
| OpenTelemetry vs Grafana          | OpenTelemetry instruments and collects telemetry; Grafana visualizes and explores observability data. |

## **11. Real-Time System Design Differences**

| Comparison                                | Difference                                                                                                                      |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| HLD vs LLD                                | HLD describes overall architecture; LLD describes implementation details.                                                       |
| Functional vs Non-Functional Requirements | Functional defines what the system does; non-functional defines how well it works.                                              |
| Cache vs Database                         | Cache stores frequently accessed data temporarily; database provides persistent data storage.                                   |
| Cache Hit vs Cache Miss                   | Hit means data exists in cache; miss means data must be fetched elsewhere.                                                      |
| Cache-Aside vs Write-Through              | Cache-aside loads data into cache when needed; write-through updates cache and backing storage together.                        |
| Write-Through vs Write-Behind             | Write-through updates backing storage as part of the write; write-behind updates backing storage later.                         |
| Redis vs MySQL                            | Redis is an in-memory data store; MySQL is a relational database.                                                               |
| CDN vs Reverse Proxy                      | CDN distributes content geographically; reverse proxy forwards requests to backend servers.                                     |
| Static vs Dynamic Content                 | Static content is generally served as stored; dynamic content is generated based on application data or requests.               |
| Offset vs Cursor Pagination               | Offset uses a numeric starting position; cursor uses a reference to the last item or ordering position.                         |
| WebSocket vs Socket.IO                    | WebSocket is a communication protocol; Socket.IO is a library with additional real-time communication features.                 |
| WebSocket vs Redis Pub/Sub                | WebSocket connects clients to servers; Redis Pub/Sub distributes messages between connected application instances.              |
| Background Job vs Cron Job                | Background job runs outside the main request; cron job runs on a schedule.                                                      |
| Queue vs Scheduled Job                    | Queue stores pending work; scheduled job runs at a predefined time or interval.                                                 |
| Object Storage vs Database Storage        | Object storage stores files; database storage manages structured records.                                                       |
| Pre-Signed URL vs Direct Upload           | A pre-signed URL gives temporary permission to upload or download; direct upload sends the file through the application server. |
| Optimistic vs Pessimistic Locking         | Optimistic detects conflicts during updates; pessimistic locks data before modifying it.                                        |
| Authentication vs Authorization           | Authentication verifies identity; authorization checks permissions.                                                             |
| Encryption vs Hashing                     | Encryption is reversible with the key; hashing is designed to be one-way.                                                       |
| SQL Injection vs XSS                      | SQL injection attacks database queries; XSS injects malicious scripts into web pages.                                           |
| CSRF vs XSS                               | CSRF tricks a browser into making unwanted authenticated requests; XSS injects malicious scripts into a page.                   |
| ACID vs BASE                              | ACID emphasizes transaction guarantees; BASE emphasizes availability and eventual consistency in distributed data systems.      |

# **Most Important Concepts to Memorize for a Node.js Interview**

If you have limited revision time, prioritize these concepts:

**Application scaling**

- Vertical scaling vs horizontal scaling
- Cluster vs worker threads
- PM2 fork mode vs cluster mode
- Load balancing algorithms
- Zero-downtime deployment

**Microservices**

- Monolith vs microservices
- Database per service
- Service discovery
- API Gateway
- REST vs gRPC vs WebSocket

**Communication and messaging**

- Synchronous vs asynchronous
- RabbitMQ vs Kafka
- Queue vs topic
- ACK vs NACK
- Retry vs DLQ
- Transactional Outbox

**Reliability**

- Saga pattern
- Eventual consistency
- Circuit breaker
- Retry with exponential backoff
- Idempotency
- Fault tolerance

**Database**

- Read replicas
- Partitioning vs sharding
- Replication lag
- SQL indexes
- Database migrations

**Deployment and monitoring**

- Docker image vs container
- Pod vs Deployment
- Liveness vs readiness
- CI/CD
- Logs vs metrics vs traces
- P95 vs P99 latency

**My recommendation:** Don't just memorize definitions. For each concept, practice answering three questions: What is it? Why do we use it? When would you use it in a real Node.js project? This will help you handle scenario-based interview questions much more confidently.



# **Project Management Terms – Complete Quick Revision**

These are commonly used project management terms in software development companies, especially in Agile, Scrum, software development, and client projects.

## **1. Project Management Basics**

| Term                 | Simple Meaning                                                           |
| -------------------- | ------------------------------------------------------------------------ |
| Project              | A temporary effort to create a product or achieve a specific goal.       |
| Project Management   | Planning, organizing, and controlling project activities.                |
| Project Manager (PM) | Person responsible for managing project delivery, people, and timelines. |
| Project Owner        | Person or organization responsible for the project's overall success.    |
| Product Manager      | Person responsible for product vision, strategy, and priorities.         |
| Project Scope        | Defines what is included and excluded from a project.                    |
| Project Objective    | The main goal the project needs to achieve.                              |
| Project Deliverable  | A specific output that must be completed and delivered.                  |
| Milestone            | An important checkpoint or achievement in a project.                     |
| Deadline             | The final date or time by which work must be completed.                  |
| Timeline             | The planned schedule of project activities.                              |
| Project Plan         | A document describing how the project will be completed.                 |
| Project Budget       | Estimated money required to complete the project.                        |
| Project Resources    | People, tools, equipment, and infrastructure needed.                     |
| Stakeholder          | Anyone who has an interest in or is affected by the project.             |
| Client               | The person or organization requesting or paying for the project.         |
| End User             | The person who actually uses the application.                            |
| Sponsor              | A person who provides support, funding, or authority for the project.    |
| Project Charter      | A document that formally authorizes a project.                           |
| Success Criteria     | Conditions that determine whether a project is successful.               |
| Project Closure      | The formal completion and closing of a project.                          |

## **2. Agile & Scrum Methodology**

| Term                      | Simple Meaning                                                                    |
| ------------------------- | --------------------------------------------------------------------------------- |
| Agile                     | An approach to software development that delivers work in small, iterative steps. |
| Scrum                     | An Agile framework for managing development work in short cycles.                 |
| Sprint                    | A fixed period during which a team completes planned work.                        |
| Sprint Planning           | A meeting to decide what work the team will complete during a sprint.             |
| Daily Stand-up            | A short daily meeting to discuss progress and blockers.                           |
| Sprint Review             | A meeting to demonstrate completed work to stakeholders.                          |
| Sprint Retrospective      | A meeting to discuss what went well and what needs improvement.                   |
| Product Backlog           | A prioritized list of all required product work.                                  |
| Sprint Backlog            | Work selected for completion during the current sprint.                           |
| Product Increment         | The usable product output completed during a sprint.                              |
| Product Owner             | Person responsible for managing and prioritizing the product backlog.             |
| Scrum Master              | Person who helps the team follow Scrum and removes process obstacles.             |
| Development Team          | People responsible for building and delivering the product increment.             |
| User Story                | A requirement written from the user's perspective.                                |
| Epic                      | A large requirement that can be divided into smaller user stories.                |
| Feature                   | A specific functionality provided by an application.                              |
| Task                      | A small unit of work assigned to a team member.                                   |
| Subtask                   | A smaller activity within a task.                                                 |
| Story Point               | A relative estimate of the effort or complexity of a user story.                  |
| Velocity                  | Amount of work a team completes in a sprint, often measured in story points.      |
| Definition of Ready (DoR) | Conditions that should be met before work is accepted into a sprint.              |
| Definition of Done (DoD)  | Conditions that must be satisfied before work is considered complete.             |
| Backlog Refinement        | Reviewing and improving backlog items before planning.                            |
| Sprint Goal               | The main objective the team wants to achieve during a sprint.                     |
| Scrum Board               | A board showing the progress of sprint work.                                      |

## **3. Task & Workflow Management**

| Term                   | Simple Meaning                                                      |
| ---------------------- | ------------------------------------------------------------------- |
| Task Assignment        | Giving a specific task to a team member.                            |
| Task Tracking          | Monitoring task progress and completion.                            |
| To Do                  | Work that has not started yet.                                      |
| In Progress            | Work currently being performed.                                     |
| In Review              | Work waiting for review or approval.                                |
| Testing / QA           | Work being checked for defects and requirements.                    |
| Blocked                | Work cannot continue because of an issue or dependency.             |
| Done                   | Work has been completed according to agreed criteria.               |
| Pending                | Work is waiting for an action or decision.                          |
| On Hold                | Work is temporarily paused.                                         |
| Reopened               | A completed task is opened again because more work is needed.       |
| Assigned To            | The person responsible for completing a task.                       |
| Reporter               | The person who created or reported the task.                        |
| Assignee               | The person assigned to work on a task.                              |
| Priority               | The importance of completing a task relative to other work.         |
| Severity               | The seriousness of a defect or issue.                               |
| Due Date               | The date by which a task should be completed.                       |
| Dependency             | A task that relies on another task or activity.                     |
| Blocker                | An issue that prevents progress.                                    |
| Workload               | The amount of work assigned to a person or team.                    |
| Work In Progress (WIP) | Work that has started but is not yet completed.                     |
| WIP Limit              | Maximum number of tasks allowed in a workflow stage.                |
| Handover               | Transferring work or responsibility to another person or team.      |
| Escalation             | Reporting an issue to a higher authority for support or resolution. |
| Follow-up              | Checking the status of previously discussed work.                   |

## **4. Estimation, Planning & Scheduling**

| Term                           | Simple Meaning                                                                          |
| ------------------------------ | --------------------------------------------------------------------------------------- |
| Estimation                     | Predicting the effort, time, or resources required for work.                            |
| Effort Estimation              | Estimating how much work is required.                                                   |
| Time Estimation                | Estimating how long a task will take.                                                   |
| Complexity                     | How difficult a task is to implement.                                                   |
| Planning Poker                 | A team technique for estimating story points.                                           |
| Story Point Estimation         | Estimating relative work complexity and effort.                                         |
| Time Tracking                  | Recording the time spent on tasks.                                                      |
| Timesheet                      | A record of working hours.                                                              |
| Work Breakdown Structure (WBS) | Dividing a large project into smaller manageable activities.                            |
| Task Breakdown                 | Dividing a large task into smaller tasks.                                               |
| Resource Allocation            | Assigning people and resources to project activities.                                   |
| Capacity Planning              | Estimating how much work a team can handle.                                             |
| Sprint Capacity                | Amount of work a team can realistically complete in a sprint.                           |
| Buffer Time                    | Extra time reserved for unexpected issues.                                              |
| Critical Path                  | The sequence of dependent tasks that determines the shortest possible project duration. |
| Gantt Chart                    | A visual chart showing tasks, durations, and schedules.                                 |
| Baseline                       | The approved original project plan used for comparison.                                 |
| Milestone Tracking             | Monitoring important project checkpoints.                                               |
| Schedule Variance              | Difference between planned and actual schedule progress.                                |
| Scope Creep                    | Uncontrolled expansion of project requirements.                                         |
| Deadline Management            | Planning and monitoring work to meet deadlines.                                         |

## **5. Requirements & Documentation**

| Term                       | Simple Meaning                                                         |
| -------------------------- | ---------------------------------------------------------------------- |
| Requirement                | A feature or condition the application must satisfy.                   |
| Business Requirement       | What the business wants to achieve.                                    |
| Functional Requirement     | What the application should do.                                        |
| Non-Functional Requirement | How well the application should work.                                  |
| Technical Requirement      | A technical condition or constraint for implementation.                |
| Requirement Gathering      | Collecting information about what the client needs.                    |
| Requirement Analysis       | Understanding and evaluating collected requirements.                   |
| Requirement Specification  | Document describing the requirements in detail.                        |
| BRD                        | Business Requirements Document; describes business needs.              |
| SRS                        | Software Requirements Specification; describes software requirements.  |
| FRS                        | Functional Requirements Specification; describes system functionality. |
| User Flow                  | Steps a user follows to complete an action.                            |
| Use Case                   | Describes how an actor interacts with a system to achieve a goal.      |
| Acceptance Criteria        | Conditions that must be satisfied for a requirement to be accepted.    |
| Wireframe                  | A basic layout showing the structure of a screen.                      |
| Prototype                  | An early model used to demonstrate or test an idea.                    |
| Technical Documentation    | Documents explaining architecture, APIs, setup, or implementation.     |
| API Documentation          | Explains API endpoints, parameters, requests, and responses.           |
| Change Request             | A formal request to modify an agreed requirement or project scope.     |
| Requirement Traceability   | Tracking requirements through design, development, and testing.        |
| Sign-off                   | Formal approval from an authorized person.                             |
| Meeting Minutes (MoM)      | Written summary of meeting discussions and decisions.                  |

## **6. Team Communication & Collaboration**

| Term                    | Simple Meaning                                                           |
| ----------------------- | ------------------------------------------------------------------------ |
| Team Collaboration      | Working together to achieve a shared goal.                               |
| Coordination            | Organizing work between team members.                                    |
| Communication Gap       | Missing or unclear communication between people.                         |
| Status Update           | Information about current task or project progress.                      |
| Progress Report         | Summary of completed work, pending work, and issues.                     |
| Daily Update            | Short summary of what was done and what is planned.                      |
| Meeting Agenda          | List of topics to discuss in a meeting.                                  |
| Meeting Minutes (MoM)   | Record of decisions and discussions from a meeting.                      |
| Action Item             | A specific activity assigned during a meeting.                           |
| Point of Contact (POC)  | The person responsible for communication on a particular subject.        |
| Knowledge Transfer (KT) | Sharing project knowledge with another person or team.                   |
| Cross-Functional Team   | A team with members from different skill areas.                          |
| Ownership               | Taking responsibility for a task or outcome.                             |
| Accountability          | Being answerable for assigned responsibilities and results.              |
| Feedback                | Information provided to improve work or performance.                     |
| Conflict Resolution     | Handling disagreements and finding a solution.                           |
| Client Communication    | Discussing requirements, progress, issues, and delivery with the client. |
| Stakeholder Management  | Managing stakeholder expectations and communication.                     |
| Approval                | Permission to proceed with a task or decision.                           |
| Consensus               | Agreement reached by a group.                                            |

## **7. Bug, Issue & Risk Management**

| Term                      | Simple Meaning                                                        |
| ------------------------- | --------------------------------------------------------------------- |
| Bug                       | An error in software that causes incorrect behavior.                  |
| Defect                    | A deviation from expected software behavior or requirements.          |
| Issue                     | A problem or concern that needs attention.                            |
| Incident                  | An event that disrupts or degrades a service.                         |
| Root Cause                | The underlying reason a problem occurred.                             |
| Root Cause Analysis (RCA) | Investigating the underlying reason for a problem.                    |
| Risk                      | A possible future event that may affect the project.                  |
| Risk Assessment           | Evaluating the likelihood and impact of a risk.                       |
| Risk Mitigation           | Actions taken to reduce the probability or impact of a risk.          |
| Risk Register             | A document that tracks identified project risks.                      |
| Blocker                   | An issue preventing work from progressing.                            |
| Dependency Risk           | Risk caused by relying on another task, team, or service.             |
| Contingency Plan          | An alternative plan for handling unexpected situations.               |
| Severity                  | How seriously a defect affects the system.                            |
| Priority                  | How urgently an issue should be addressed.                            |
| Regression Bug            | A defect introduced in functionality that previously worked.          |
| Production Bug            | A defect found in the live application.                               |
| Hotfix                    | An urgent fix for a production issue.                                 |
| Workaround                | A temporary solution that avoids the problem without fully fixing it. |
| Resolution                | The action or result that solves an issue.                            |
| Retesting                 | Testing again after a defect has been fixed.                          |
| Regression Testing        | Checking that existing functionality still works after changes.       |
| Incident Management       | Handling, resolving, and documenting service incidents.               |
| Risk vs Issue             | Risk may happen in the future; an issue is already happening.         |

## **8. Software Development & Delivery**

| Term                    | Simple Meaning                                                                   |
| ----------------------- | -------------------------------------------------------------------------------- |
| SDLC                    | Software Development Life Cycle; stages involved in building software.           |
| Requirement Analysis    | Understanding what needs to be developed.                                        |
| Design Phase            | Planning the software architecture and user interface.                           |
| Development Phase       | Writing and integrating application code.                                        |
| Testing Phase           | Checking whether the application works correctly.                                |
| Deployment              | Releasing the application to an environment.                                     |
| Maintenance             | Supporting and improving software after release.                                 |
| Code Review             | Reviewing code written by another developer.                                     |
| Pull Request (PR)       | A request to review and merge code changes.                                      |
| Merge                   | Combining code changes from different branches.                                  |
| Branch                  | A separate line of development in version control.                               |
| Commit                  | A saved set of code changes in version control.                                  |
| Release                 | Making a particular software version available.                                  |
| Build                   | A generated application package or executable output.                            |
| Deployment Pipeline     | Automated steps for building, testing, and deploying software.                   |
| QA                      | Quality Assurance; activities that help ensure software quality.                 |
| UAT                     | User Acceptance Testing; users verify whether the application meets their needs. |
| Staging Environment     | An environment used to test the application before production.                   |
| Production Environment  | The live environment used by actual users.                                       |
| Development Environment | An environment used by developers to build and test changes.                     |
| Release Notes           | A summary of changes included in a software release.                             |
| Version Control         | Tracking and managing changes to source code.                                    |
| Technical Debt          | Future maintenance cost caused by shortcuts or poor technical decisions.         |
| Refactoring             | Improving code structure without changing its external behavior.                 |
| Deployment Approval     | Authorization required before a release.                                         |
| Rollback                | Returning to a previous working software version.                                |

## **9. Project Tracking & Performance Metrics**

| Term                    | Simple Meaning                                                         |
| ----------------------- | ---------------------------------------------------------------------- |
| KPI                     | Key Performance Indicator; a measurement used to evaluate performance. |
| Project Health          | Overall status of project progress, budget, quality, and risks.        |
| Burndown Chart          | Shows remaining work during a sprint or project.                       |
| Burnup Chart            | Shows completed work against total project scope.                      |
| Velocity                | Amount of work completed by a Scrum team during a sprint.              |
| Sprint Progress         | How much planned sprint work has been completed.                       |
| Completion Rate         | Percentage of assigned work completed.                                 |
| On-Time Delivery        | Completing work by the planned deadline.                               |
| Productivity            | Amount of useful work completed relative to resources or time.         |
| Resource Utilization    | How much available working capacity is being used.                     |
| Defect Rate             | Number or percentage of defects found.                                 |
| Lead Time               | Time from a work request being made to its delivery.                   |
| Cycle Time              | Time from starting work to completing it.                              |
| Throughput              | Number of work items completed in a given period.                      |
| Planned vs Actual       | Comparing estimated work or time with what actually happened.          |
| Variance                | Difference between planned and actual results.                         |
| Budget Variance         | Difference between planned and actual project spending.                |
| Schedule Variance       | Difference between planned and actual schedule performance.            |
| Customer Satisfaction   | How satisfied customers are with the product or service.               |
| Delivery Predictability | How consistently a team delivers work as planned.                      |

## **10. Common Project Management Tools**

| Tool            | Simple Meaning                                                      |
| --------------- | ------------------------------------------------------------------- |
| Jira            | Tracks software tasks, bugs, sprints, and project workflows.        |
| Trello          | Manages tasks using visual boards and cards.                        |
| Asana           | Manages projects, tasks, and team activities.                       |
| ClickUp         | Combines task management, project tracking, and documentation.      |
| Monday.com      | Manages workflows and project progress.                             |
| Azure DevOps    | Provides planning, code repositories, pipelines, and testing tools. |
| GitHub Projects | Tracks development work using project boards and views.             |
| GitLab          | Provides source control, issue tracking, and CI/CD.                 |
| Slack           | Team messaging and collaboration.                                   |
| Microsoft Teams | Meetings, messaging, and team collaboration.                        |
| Confluence      | Creates and manages project documentation.                          |
| Notion          | Organizes notes, documentation, tasks, and knowledge.               |
| Figma           | Creates UI designs, wireframes, and prototypes.                     |
| Excel           | Tracks tasks, timelines, estimates, and project reports.            |
| Google Sheets   | Collaborative spreadsheets for project tracking.                    |

# **Important Differences to Remember**

These are common interview and workplace comparisons.

| Comparison                               | Difference                                                                                                           |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Project Manager vs Product Manager       | Project Manager manages delivery; Product Manager manages product direction and priorities.                          |
| Project vs Product                       | Project is a temporary effort; product is something developed and maintained for users.                              |
| Agile vs Scrum                           | Agile is a development approach; Scrum is a framework within Agile.                                                  |
| Scrum vs Kanban                          | Scrum uses fixed-length sprints; Kanban focuses on continuous workflow.                                              |
| Epic vs User Story vs Task               | Epic is large work; user story describes user value; task is an implementation activity.                             |
| Product Backlog vs Sprint Backlog        | Product backlog contains all prioritized product work; sprint backlog contains work selected for the current sprint. |
| Sprint Review vs Retrospective           | Review demonstrates the product; retrospective improves the team's working process.                                  |
| Product Owner vs Scrum Master            | Product Owner prioritizes product work; Scrum Master supports the Scrum process.                                     |
| Milestone vs Deadline                    | Milestone is an important checkpoint; deadline is the final completion date.                                         |
| Scope vs Requirement                     | Scope defines project boundaries; requirements describe what the system must do.                                     |
| Functional vs Non-Functional Requirement | Functional describes what the system does; non-functional describes how well it works.                               |
| Priority vs Severity                     | Priority determines how soon something should be fixed; severity measures its impact.                                |
| Bug vs Feature                           | Bug is incorrect behavior; feature is intended functionality.                                                        |
| Bug vs Issue                             | Bug is a software defect; issue is a broader problem or work item.                                                   |
| Risk vs Issue                            | Risk may happen; issue has already occurred.                                                                         |
| Blocker vs Dependency                    | Blocker prevents progress; dependency means one activity relies on another.                                          |
| Estimate vs Actual                       | Estimate is the prediction; actual is what really happened.                                                          |
| Effort vs Duration                       | Effort is the amount of work; duration is the elapsed time.                                                          |
| Lead Time vs Cycle Time                  | Lead time starts from the request; cycle time starts when work begins.                                               |
| Burndown vs Burnup                       | Burndown tracks remaining work; burnup tracks completed work against total scope.                                    |
| QA vs UAT                                | QA checks software quality; UAT checks whether it meets user needs.                                                  |
| Staging vs Production                    | Staging is for pre-release validation; production is the live environment.                                           |
| Deployment vs Release                    | Deployment installs software into an environment; release makes functionality available to users.                    |
| Code Review vs Testing                   | Code review examines implementation; testing checks application behavior.                                            |
| Hotfix vs Regular Release                | Hotfix addresses an urgent issue; regular release delivers planned changes.                                          |
| Rollback vs Revert                       | Rollback restores a previous deployed version or state; revert reverses a specific change, often in version control. |
| Accountability vs Responsibility         | Responsibility means doing the assigned work; accountability means being answerable for the outcome.                 |
| Sign-off vs Approval                     | Sign-off is formal confirmation; approval is permission to proceed.                                                  |
| Change Request vs Scope Creep            | Change request is a formal proposed change; scope creep is uncontrolled scope expansion.                             |
| Project Plan vs Project Report           | Plan describes intended work; report describes actual progress and status.                                           |

# **Practical terms to use in daily software developer work**

These phrases are useful when communicating with project managers, team leads, clients, and other developers.

| Workplace Phrase                           | Meaning                                                   |
| ------------------------------------------ | --------------------------------------------------------- |
| I have picked up the task.                 | I have started working on the task.                       |
| The task is in progress.                   | I am currently working on it.                             |
| The task is completed.                     | I have finished the work.                                 |
| The task is pending review.                | The work is waiting for someone to review it.             |
| I am blocked by an API dependency.         | I cannot continue until the API is available.             |
| I need clarification on the requirement.   | Some requirement details are unclear.                     |
| The estimated completion time is two days. | I expect to finish in two days.                           |
| There is a scope change.                   | The project requirements have changed.                    |
| I found a production issue.                | I identified a problem in the live application.           |
| I have raised a pull request.              | I submitted my code for review.                           |
| The changes are deployed to staging.       | The updated code is available in the testing environment. |
| QA has reported a defect.                  | The testing team found a problem.                         |
| I have fixed the reported issue.           | I corrected the defect.                                   |
| I am waiting for client approval.          | The client needs to approve the work.                     |
| We need to prioritize this task.           | This task needs more immediate attention.                 |
| I will provide an update by EOD.           | I will share progress by the end of the day.              |
| We may need to revise the timeline.        | The planned completion date may need to change.           |
| The task depends on another team's work.   | Another team's completion is required first.              |
| I have completed the knowledge transfer.   | I have shared the required project knowledge.             |
| We are targeting the next sprint.          | We plan to complete this work in the next sprint.         |

**For a 4-year Full Stack Developer interview,** focus especially on Agile, Scrum, sprint planning, Jira, task estimation, requirement gathering, client communication, code review, UAT, production bugs, RCA, and deployment. These are the project-management terms most likely to come up when discussing how you manage projects end to end.