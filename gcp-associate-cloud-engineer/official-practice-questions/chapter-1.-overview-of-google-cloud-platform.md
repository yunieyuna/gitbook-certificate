# Chapter 1. Overview of Google Cloud Platform

#### 1. What is the fundamental unit of computing in cloud computing?

A. Physical server

B. VM

C. Block

D. Subnet



**Answers:**

B. The basic unit for purchasing computing resources is the virtual machine (VM). A physical server underlies VMs, but the resources of a physical server are allocated to VMs. Blocks and subnets are not relevant to the fundamental unit of computing.

**Extra Knowledge:**&#x20;

* `Block` storage uses a fixed-size data structure called a block to organize data. Block storage is commonly used in ephemeral and persistent disks attached to VMs.



#### 2. If you use a cluster that is managed by a cloud provider, which of these will be managed for you by the cloud provider?

A. Monitoring

B. Networking

C. Some security management tasks&#x20;

D. All of the above



**Answers:**

D. When using managed clusters, the cloud provider will monitor the health of nodes in the cluster, set up networking between nodes in the cluster, and configure firewall and other security controls.



#### 3. You need serverless computing for file processing and running the backend of a website; which two products can you choose from Google Cloud Platform?

A. Kubernetes Engine and Compute Engine&#x20;

B. App Engine and Cloud Functions

C. Cloud Functions and Compute Engine&#x20;

D. Cloud Functions and Kubernetes Engine



**Answers:**

B. App Engine is a serverless platform for running applications, while Cloud Functions is a service for executing short-running functions in response to events. Kubernetes Engine is a managed cluster service, and both Kubernetes Engine and Compute Engine require you to configure servers.

**Extra Knowledge:**&#x20;

* Both VMs and managed kubernetes clusters require some level of effort to configure and administer computing resources.
* Serverless computing is an approach that allows develop- ers and application administrators to run their code in a computing environment that does not require setting up VMs or kubernetes clusters.
* Google Cloud Platform has two serverless computing options: App Engine and Cloud Functions.
  * App Engine is used for applications and containers that run for extended peri- ods of time, such as a website backend, point-of-sale system, or custom business appli- cation.
  * Cloud Functions is a platform for running code in response to an event, such as uploading a file or adding a message to a message queue.



#### 4. You have been asked to design a storage system for a web application that allows users to upload large data files to be analyzed by a business intelligence workflow. The files should be stored in a high-availability storage system. File system functionality is not required. Which storage system in Google Cloud Platform should be used?

A. Block storage

B. Object storage

C. Cache

B. Network File System



**Answers:**

B. Object storage, like Cloud Storage, provides redundantly stored objects without lim-\
its on the amount of data you can store, which makes option B correct. Since file system functionality is not required, option D is not a good option. Block storage could be used, but you would have to manage your own replication to ensure high availability. Caches are transient, in-memory storage and are not high-availability, persistent storage systems.

**Extra Knowledge:**&#x20;

* Object storage is a system that manages the use of storage in terms of objects or blobs.
  * Objects are grouped into buckets. Each object is individually addressable, usually by a URL.
  * Object storage is not limited by the size of disks or solid-state drives (SSDs) attached to a server.
  * Multiple copies of objects are stored to improve availability and durability. In some cases, copies of objects may be stored in different regions to ensure availability even if a region becomes inaccessible.
  * Another advantage of object storage is that it is serverless. There is no need to create VMs and attach storage to them.



#### 5. All block storage systems use what block size?

A. 4KB

B. 8KB

C. 16KB

D. Block size can vary.



**Answers:**

D. Block sizes in a block storage system can vary; therefore, option D is the correct answer. Block size is established when a file system is created. 4KB block sizes are commonly used in Linux.

**Extra Knowledge:**&#x20;

* In Linux file systems, 4KB is a common block size. Relational databases often write directly to blocks, but they often use larger sizes, such as 8KB or more.



#### 6. You have been asked to set up network security in a virtual private cloud. Your company wants to have multiple subnetworks and limit traffic between the subnetworks. Which net- work security control would you use to control the flow of traffic between subnets?

A. Identity access management

B. Router

C. Firewall

D. IP address table



**Answers:**

C. Firewalls in Google Cloud Platform (GCP) are software-defined network controls that limit the flow of traffic into and out of a network or subnetwork, so option C is the correct answer. Routers are used to move traffic to appropriate destinations on the network. Identity access management is used for authenticating and authorizing users; it is not relevant to network controls between subnetworks. IP address tables are not a security control.

**Extra Knowledge:**&#x20;

* VPCs contain subnetworks, call subnets, which are regional resources. Subnets have a range of IP addresses associated with them. Subnets provide private internal addresses. Resources use these addresses to communicate with each other and with Google APIs and services.



#### 7. When you create a machine learning service to identify text in an image, what type of serv- ers should you choose to manage compute resources?

A. VMs

B. Clusters of VMs

C. No servers; specialized services are serverless

D. VMs running Linux only



**Answers:**

C. Option C is correct because specialized services in GCP are serverless. Google manages the compute resources used by the services. There is no need for a user to allocate or monitor VMs.

**Extra Knowledge:**&#x20;

* Most public cloud providers offer specialized services that can be used as building blocks of applications or as part of a workflow for processing data.
* Specialized services are serverless; you do not need to configure servers or clusters.
* These are some of the specialized services in Google Cloud Platform:
  * AutoML, a machine learning service&#x20;
  * Cloud Natural Language, a service for analyzing text&#x20;
  * Cloud Vision for analyzing images&#x20;
  * Cloud Inference API, a service for computing correlations over time-series data



#### 8. Investing in servers for extended periods of time, such as committing to use servers for three to five years, works well when?

A. A company is just starting up

B. A company can accurately predict server need for an extended period of time

C. A company has a fixed IT budget

D. A company has a variable IT budget



**Answers:**

B. Option B is correct; investing in servers works well when an organization can accurately predict the number of servers and other equipment it will need for an extended period and can utilize that equipment consistently. Startups are not established businesses with his- tories that can guide expected needs in three to five years. It does not matter if a budget is fixed or variable; investing in servers should be based on demand for server capacity.



#### 9 .Your company is based in X and will be running a virtual server for Y. What factor determines the unit per minute cost?

A. The time of day the VM is run&#x20;

B. The characteristics of the server&#x20;

C. The application you run

D. None of the above



**Answers:**

B. The characteristics of the server, such as the number of virtual servers, the amount of memory, and the region where you run the VM, influence the cost, so option B is correct. Time of day is not a factor, nor is the type of application you run on the VM.



#### 10 .You plan to use Cloud Vision to analyze images and extract text seen in the image. You plan to process between 1,000 and 2,500 images per hour. How many VMs should you allocate to meet peak demand?

A. 1

B. 10

C. 25

D. None; Cloud Vision is a serverless service.



**Answers:**

D. Cloud Vision is one of GCP’s specialized services. Users of the service do not need to configure any VMs to use the service.

**Extra Knowledge:**&#x20;

* Most public cloud providers offer specialized services that can be used as building blocks of applications or as part of a workflow for processing data.
* Specialized services are serverless; you do not need to configure servers or clusters.
* These are some of the specialized services in Google Cloud Platform:
  * AutoML, a machine learning service&#x20;
  * Cloud Natural Language, a service for analyzing text&#x20;
  * Cloud Vision for analyzing images&#x20;
  * Cloud Inference API, a service for computing correlations over time-series data



#### 11. You have to run a number of services to support an application. Which of the following is a good deployment model?

A. Run on a large, single VM

B. Use containers in a managed cluster

C. Use two large VMs, making one of them read only

D. Use a small VM for all services and increase the size of the VM when CPU utilization

exceeds 90 percent



**Answers:**

B. Containers give the most flexibility for using the resources of a cluster efficiently and orchestration platforms reduce the operations overhead, which makes option B correct. Running in a single cluster is not recommended because if the server fails, all services will be down. Using two VMs with one read-only is not useful. Read-only servers are sometimes used with databases, but there was no mention of databases in the question. Using a small VM and upgrading when it is no longer able to keep up with the workload delivers poor-quality service to users and should be avoided.



#### 12. You have created a VM. Which of the following system administration operations are you allowed to perform on it?

A. Configure the file system

B. Patch operating system software

C. Change file and directory permissions

D. All of the above



**Answers:**

D. All of the operations are available to a system administrator after creating a VM, so option D is correct.



#### 13. Cloud Filestore is based on what file system technology?

A. Network File System (NFS)

B. XFS

C. EXT4

D. ReiserFS



**Answers:**

A. Option A is correct; Cloud Filestore is based on Network Filesystem (NSF), which is a distributed file management system. The other options are file systems supported by Linux but are not the foundation of Cloud Filestore.



#### 14. When setting up a network in GCP, your network the resources in it are treated as what?&#x20;

A. Virtual private cloud

B. Subdomain

C. Cluster

D. None of the above



**Answers:**

A. When you create a network, it is treated as a virtual private cloud, which makes option A correct. Resources are added to the VPC and are not accessible outside the VPC unless you explicitly configure them to be. A subdomain is related to web domains and not related to GPC network configuration. Clusters, such as Kubernetes clusters, may be in your network, but are not a characteristic of the network.



#### 15. You need to store data for X and therefore you are using a cache for Y. How will the cache affect data retrieval?

A. A cache improves the execution of client-side JavaScript.

B. A cache will continue to store data even if power is lost, improving availability.

D. Caches can get out of sync with the system of truth.

D. Using a cache will reduce latency, since retrieving from a cache is faster than retrieving from SSDs or HDDs.



**Answers:**

D. Caches use memory, and that makes them the fastest storage type for reading data, so option D is right. Caches are data stores on the backend of distributed systems, not the clients. A cache would have no effect on client-side JavaScript execution. Caches do not store data in a cache if power is lost; the data would have to be reloaded. Caches can get out of sync with the system of truth because the system of truth could be updated, but the cache may not be updated. Caches have faster read times than SSDs and HDDs.



#### 16. Why can cloud providers offer elastic resource allocation?

A. Cloud providers can take resources from lower-priority customers and give them to higher-priority customers.

B. Extensive resources and the ability to quickly shift resources between customers enables public cloud providers to offer elastic resource allocation more efficiently than can be done in smaller data centers.

C. They charge more the more resources you use.

D. They don’t.



**Answers:**

B. Option B is correct; cloud providers have large capacity and can quickly allocate\
those resources to different customers. With a mix of customers and workloads, they can optimize the allocation of resources. Option A is incorrect; cloud providers do not take resources from one customer to give them to another, with the exception of preemptible instances. Option C is incorrect; cloud providers usually offer discounts for increased use.



#### 17. What is not a characteristic of specialized services in Google Cloud Platform?

A. They are serverless; you do not need to configure servers or clusters.

B. They provide a specific function, such as translating text or analyzing images.

C. They require monitoring by the user.

D. They provide an API to access the functionality of the service.



**Answers:**

C. Specialized services are monitored by Google so users do not have to monitor them; therefore, option C is correct. Specialized services provide a specific compute functionality but do not require the user to configure any resources. They also provide APIs.



#### 18. Your client’s transactions must access a drive attached to a VM that allows for random access to parts of files. What kind of storage does the attached drive provide?

A. Object storage

B. Block storage

C. NoSQL storage&#x20;

D. Only SSD storage



**Answers:**

B. Attached drives are block storage devices. Cloud Storage is the object storage service and does not attach directly to a VM. NoSQL is a type of database, not a storage system. Attached drives may be either SSDs or hard drives.



#### 19. You are deploying a new relational database to support a web application. Which type of storage system would you use to store data files of the database?

A. Object storage

B. Data storage

C. Block storage

D. Cache



Answers:

C. Databases require persistent storage on block devices. Object storage does not provide data block or file system storage, making option C the correct answer. Data storage is not a type of storage system. Caches are often used with databases to improve read performance, but they are volatile and are not suitable for persistently storing data files.



#### 20. A user prefers services that require minimal setup; why would you recommend Cloud Storage, App Engine, and Cloud Functions?

A. They are charged only by time.

B. They are serverless.

C. They require a user to configure VMs.

D. They can only run applications written in Go.



**Answers:**

B. All three services are serverless, so the user does not need to configure VMs; therefore, option B is correct. Cloud Storage is charged based on time and size of data stored. App Engine Standard and Cloud Functions are not restricted to just the Go language.

