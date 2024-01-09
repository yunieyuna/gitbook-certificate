# Chapter 2. Google Cloud Computing Services

#### Understanding Level:

* O: Understand the whole question
* △: Not sure about part of the question
* ×: Don't understand the question

| Question Number | Trial 1 | Trial 2 | Trial 3 |
| --------------- | ------- | ------- | ------- |
| 1               |         |         |         |
| 2               |         |         |         |
| 3               |         |         |         |
| 4               |         |         |         |
| 5               |         |         |         |
| 6               |         |         |         |
| 7               |         |         |         |
| 8               |         |         |         |
| 9               |         |         |         |
| 10              |         |         |         |
| 11              |         |         |         |
| 12              |         |         |         |
| 13              |         |         |         |
| 14              |         |         |         |
| 15              |         |         |         |
| 16              |         |         |         |
| 17              |         |         |         |
| 18              |         |         |         |
| 19              |         |         |         |
| 20              |         |         |         |

#### 1. You are planning to deploy a SaaS application for customers in North America, Europe, and Asia. To maintain scalability, you will need to distribute workload across servers in multiple regions. Which GCP service would you use to implement the workload distribution?

A. Cloud DNS

B. Cloud Spanner

C. Cloud Load Balancing&#x20;

D. Cloud CDN



**Answers:**

C. Cloud Load Balancing distributes workloads within and across regions, provides health checks, and implements autoscaling. Cloud DNS provides domain name services, such as translating a URL like www.example.com to an IP address. Cloud Spanner is a distributed relational database but does not implement workload distribution. Cloud CDN distributes content across regions to reduce latency when delivering content to users across the globe.



#### 2. You have decided to deploy a set of microservices using containers. You could install and manage Docker on Compute Engine instances, but you’d rather have GCP provide some container management services. Which two GCP services allow you to run containers in a managed service?

1. App Engine standard environment and App Engine flexible environment
2. Kubernetes Engine and App Engine standard environment
3. Kubernetes Engine and App Engine flexible environment
4. App Engine standard environment and Cloud Functions



Answers:

C. App Engine flexible environments allow you to run containers on the App Engine PaaS. Kubernetes Engine is an orchestration platform for running containers. Both provide con- tainer management services. The App Engine standard environment runs applications in language-specific sandboxes and is not a general container management system. Cloud Functions is a serverless service for running code in response to events. It does not provide container services.



#### 3. Why would an API developer want to use the Apigee API platform?

A. To get the benefits of routing and rate-limiting

B. Authentication services

C. Version control of code

D. A and B

E. All of the above



Answers:

D. Options A and B are both correct answers. The Apigee API platform provides policy- based rate-limiting and routing services to help accommodate spikes in traffic. It also provides OAuth 2.0 and SAML authentication. It does not provide version control; Cloud Source Repositories is the service user for version control.



#### 4. You are deploying an API to the public Internet and are concerned that your service will be subject to DDoS attacks. Which GCP service should you consider to protect your API?

A. Cloud Armor

B. Cloud CDN

C. Cloud IAM

D. VPCs



Answer:

A. Cloud Armor builds on GCP’s load balancing services to provide the ability to allow or restrict access based on IP address, deploy rules to counter cross-site scripting attacks, and provide countermeasures to SQL injection attacks. Cloud CDN is a content distribution service, not a security service. Identity Access Management is a security service, but it is for authentication and authorization, not denial-of-service mitigation. Virtual private clouds are used to restrict network access to an organization’s resources, but it does not have fea- tures to mitigate denial-of-service attacks. Also, Cloud CDN acts as a first line of defense in the case of DDoS attacks.



#### 5. You have an application that uses a Pub/Sub message queue to maintain a list of tasks that are to be processed by another application. The application that consumes messages from the Pub/Sub queue removes the message only after completing the task. It takes approxi- mately 10 seconds to complete a task. It is not a problem if two or more VMs perform the same task. What is a cost-effective configuration for processing this workload?

A. Use preemptible VMs

B. Use standard VMs

C. Use DataProc

D. Use Spanner



Answer:

A. This is a good use case for preemptible VMs because they could reduce the cost of running the second application without the risk of losing work. Since tasks are deleted from the queue only after they are completed if a preemptible VM is shut down before completing the task, another VM can perform the task. Also, there is no harm in running a task more than once, so if two VMs do the same task, it will not adversely affect the output of the application. DataProc and Spanner are not appropriate products for this task.



#### 6. Your department is deploying an application that has a database backend. You are con- cerned about the read load on the database server and want to have data available in mem- ory to reduce the time to respond to queries and to reduce the load on the database server. Which GCP service would you use to keep data in memory?

A. Cloud SQL

B. Cloud Memorystore&#x20;

C. Cloud Spanner

D. Cloud Datastore



Answer:

B. Cloud Memorystore is the only GCP designed to cache data in memory. Cloud SQL is\
a relational database service and might be a good option for the backend database. Cloud Spanner is a global relational database and is a good option when you need a globally con- sistent database. Cloud Datastore is a document database suitable for product catalogs, user profiles, and other semistructured data.



#### 7. The Cloud SDK can be used to configure and manage resources in which of the following services?

A. Compute Engine

B. Cloud Storage

C. Network firewalls

D. All of the above



Answer:

D. All three of the services listed, Compute Engine, Cloud Storage, and network firewalls, can be managed and configured using Cloud SDK.



#### 8. What server configuration is required to use Cloud Functions?

A. VM configuration

B. Cluster configuration

C. Pub/Sub configuration

D. None



Answer:

D. Cloud Functions is a serverless product, no configuration is required.



#### 9. You have been assigned the task of consolidating log data generated by each instance of an application. Which of the Stackdriver management tools would you use?&#x20;

A. Monitoring

B. Trace

C. Debugger

D. Logging



Answer:

D. The Stackdriver Logging product is used to consolidate and manage logs generated by applications and servers.



#### 10. Which specialized services are most likely to be used to build a data warehousing platform that requires complex extraction, transformation, and loading operations on batch data as well as processing streaming data?

A. Apigee API platform

B. Data analytics

C. AI and machine learning

D. Cloud SDK



Answer:

B. The data analytics set of specialized services includes products that help with extraction, transformation, and loading (ETL) and work with both batch and streaming data. The Apigee API platform is used for managing APIs and does not meet the needs described. AI and machine learning might be useful for analyzing data in the data warehouse, but the services in that set are not always helpful for ETL operations. Cloud SDK is used to control services but by itself is not directly able to perform the operations needed.



#### 11. Your company has deployed 100,000 Internet of Things (IoT) sensors to collect data on the state of equipment in several factories. Each sensor will collect and send data to a data store every 5 seconds. Sensors will run continuously. Daily reports will produce data on the maximum, minimum, and average value for each metric collected on each sensor. There is no need to support transactions in this application. Which database product would you recommend?

A. Cloud Spanner

B. Cloud Bigtable

C. Cloud SQL MySQL

D. Cloud SQL PostgreSQL



Answer:

B. Bigtable is designed to accept billions of rows of data. Collecting data from\
100,000 sensors every 5 seconds will generate 6,000,000 data points every minute, or 8,640,000,000 data points per day. Spanner is a relational database and supports transactions, but they are not needed. Cloud SQL MySQL and Cloud SQL PostgreSQL would be difficult to scale to this level of read and write performance.



#### 12. You are the lead developer on a medical application that uses patients’ smartphones to capture biometric data. The app is required to collect data and store it on the smartphone when data cannot be reliably transmitted to the backend application. You want to minimize the amount of development you have to do to keep data synchronized between smartphones and backend data stores. Which data store option should you recommend?

A. Cloud Firestore

B. Cloud Spanner

C. Cloud Datastore

D. Cloud SQL



Answer:

A. Cloud Firestore is a mobile database service that can synchronize data between mobile devices and centralized storage. Spanner is a global relational database for large-scale applications that require transaction support in highly scaled databases. Datastore and Cloud SQL could be used but would require more custom development to synchronize data between mobile devices and the centralized data store.



#### 13. A software engineer comes to you for a recommendation. She has implemented a machine learning algorithm to identify cancerous cells in medical images. The algorithm is compu- tationally intensive, makes many mathematical calculations, requires immediate access to large amounts of data, and cannot be easily distributed over multiple servers. What kind of Compute Engine configuration would you recommend?

A. High memory, high CPU

B. High memory, high CPU, GPU

C. Mid-level memory, high CPU

D. High CPU, GPU



Answer:

B. A computationally intensive application obviously requires high CPUs, but the fact that there are many mathematical calculations indicates that a GPU should be used. You might consider running this in a cluster, but the work is not easily distributed over multiple servers, so you will need to have a single server capable of handling the load. Immediate access to large amounts of data indicates that a high-memory machine should be recommended.



#### 14. You are tasked with mapping the authentication and authorization policies of your on-premises applications to GPC’s authentication and authorization mechanisms. The GCP documentation states that an identity must be authenticated in order to grant privileges to that identity. What does the term identity refer to?

A. VM ID

B. User

C. Role

D. Set of privileges



Answer:

B. Identities are abstractions of users. They can also represent characteristics of processes that run on behalf of a human user or a VM in the GCP. Identities are not related to VM IDs. Roles are collections of privileges that can be granted to identities. Option D is synonymous with option C.



#### 15. A client is developing an application that will need to analyze large volumes of text information. The client is not expert in text mining or working with language. What GCP service would you recommend they use?

A. Cloud Vision

B. Cloud ML

C. Cloud Natural Language Processing

D. Cloud Text Miner



Answer:

C. Cloud Natural Language Processing provides functionality for analyzing text. Cloud Text Miner does not exist. Cloud ML is a general-purpose machine learning service that could be applied to text analysis but would require knowledge of language processing, which the client does not have. Cloud Vision is for image processing.



#### 16. Data scientists in your company want to use a machine learning library available only in Apache Spark. They want to minimize the amount of administration and DevOps work. How would you recommend they proceed?

A. Use Cloud Spark

B. Use Cloud Dataproc

C. Use Bigquery

D. Install Apache Spark on a cluster of VMs



Answer:

B. Both options B and D would meet the need of running Spark, which would give the data scientists access to the machine library they need. However, option D requires that they manage and monitor the cluster of servers, which would require more DevOps and administration work than if they used the Dataproc service. Option C, BigQuery, is a scalable database, not a platform for running Spark. Cloud Spark is a fictitious product and does not exist in the GCP.



#### 17. Database designers at your company are debating the best way to move a database to GCP. The database supports an application with a global user base. Users expect support for transactions and the ability to query data using commonly used query tools. The database designers decide that any database service they choose will need to support ANSI 2011 and global transactions. Which database service would you recommend?

A. Cloud SQL

B. Cloud Spanner

C. Cloud Datastore

D. Cloud Bigtable



Answer:

B. Option B is correct. Spanner supports ANSI 2011 standard SQL and global transactions. Cloud SQL supports standard SQL but does not have global transaction. Datastore and Bigtable are NoSQL databases.



#### 18. Which specialized service supports both batch and stream processing workflows?

A. Cloud Dataproc

B. Bigquery

C. Cloud Datastore

D. AutoML



Answer:

A. Dataproc is designed to execute workflows in both batch and streaming modes, which makes option A correct. BigQuery is a data warehouse service. Datastore is a document database. AutoML is a machine learning service.



#### 19. You have a Python application you’d like to run in a scalable environment with the least amount of management overhead. Which GCP product would you select?

A. App Engine flexible environment

B. Cloud Engine

C. App Engine standard environment

D. Kubernetes Engine



Answer:

C. App Engine standard environment provides a serverless Python sandbox that scales automatically, so option C is correct. App Engine flexible environment runs containers and requires more configuration. Cloud Engine and Kubernetes Engine both require significant management and monitoring.



#### 20. A product manager at your company reports that customers are complaining about the reliability of one of your applications. The application is crashing periodically, but developers have not found a common pattern that triggers the crashes. They are concerned that they do not have good insight into the behavior of the application and want to perform a detailed review of all crash data. Which Stackdriver tool would you use to view consolidated crash information?

A. DataProc

B. Monitoring

C. Logging

D. Error Reporting



Answer:

D. Error reporting consolidates crash information, which makes Error Reporting the right answer. Monitoring collects metrics on application and server performance. Logging is a log management service. Dataproc is not part of Stackdriver; it is a managed Hadoop and Spark service.

