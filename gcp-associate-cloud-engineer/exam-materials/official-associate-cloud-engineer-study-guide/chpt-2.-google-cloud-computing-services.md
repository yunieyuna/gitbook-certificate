# Chpt 2. Google Cloud Computing Services

## Storage

* Multiregion storage allows for faster access to data when users or applications are distributed across regions.
* The cold storage class is low-cost archival storage designed for high durability and infrequent access. This class of storage is suitable for data that is accessed less than once per year.

## Cloud storage for Firebase

* Mobile app developers may find Cloud Storage for Firebase to be the best combination of cloud object storage and the ability to support uploads and downloads from mobile devices with sometimes unreliable network connections.
* The Cloud Storage for Firebase API is designed to provide secure transmission as well as robust recovery mechanisms to handle potentially problematic network quality.

## Cloud Filestore

* Sometimes, developers need to have access to a file system housed on network-attached storage. For these use cases, the Cloud Filestore service provides a shared file system for use with Compute Engine and Kubernetes Engine.
* Filestore can provide high numbers of input-output operations per second (IOPS) as well as variable storage capacity. File system administrators can configure Cloud Filestore to meet their specific IOPS and capacity requirements.
* Filestore implements the Network File System (NFS) protocol so system administrators can easily mount shared file systems on virtual servers.

## Cloud SQL

* Cloud SQL is GCP’s managed relational database service that allows users to set up MySQL or PostgreSQL databases on VMs without having to attend to database administration tasks, such as backing up databases or patching database software.

## Cloud Bigtable

* Cloud Bigtable is designed for petabyte-scale applications that can manage up to billions of rows and thousands of columns.
* It is based on a NoSQL model known as a wide-column data model, and unlike Cloud SQL that supports relational databases.
* Bigtable is suited for applications that require low-latency write and read operations. It is designed to support millions of operations per second.

## Cloud Spanner

* Cloud Spanner is Google’s globally distributed relational database that combines the key benefits of relational databases, such as strong consistency and transactions, with the ability to scale horizontally like a NoSQL database.
* Spanner is a high availability database with a 99.999 percent availability Service Level Agreements (SLA), making it a good option for enterprise applications that demand scalable, highly available relational database services.
* Cloud Spanner also has enterprise-grade security with encryption at rest and encryption in transit, along with identity-based access controls.

## Cloud Datastore

* Cloud Datastore is a NoSQL document database. This kind of database uses the concept of a document, or collection of key-value pairs, as the basic building block.
* Documents allow for flexible schemas. For example, a document about a book may have key-value pairs listing author, title, and date of publication. Some books may also have information about companion websites and translations into other languages. The set of keys that may be included does not have to be defined prior to use in document databases. This is especially helpful when applications must accommodate a range of attributes, some of which may not be known at design time.
* Cloud Datastore is accessed via a REST API that can be used from applications running in Compute Engine, Kubernetes Engine, or App Engine. This database will scale automatically based on load.
* Although it is a NoSQL database, Cloud Datastore supports transactions, indexes, and SQL-like queries.
* Cloud Datastore is well suited to applications that demand high scalability and structured data and do not always need strong consistency when reading data. Product catalogs, user profiles, and user navigation history are examples of the kinds of applications that use Cloud Datastore.

## Cloud Memorystore

* Cloud Memorystore is an in-memory cache service.
* Cloud Memorystore is a managed Redis service for caching frequently used data in memory.

## Cloud Firestore

* Cloud Firestore is another GCP-managed NoSQL database service designed as a backend for highly scalable web and mobile applications.
* A distinguishing feature of Cloud Firestore is its client libraries that provide offline support, synchronization, and other features for managing data across mobile devices, IoT devices, and backend data stores.
  * For example, applications on mobile devices can be updated in real time as data in the backend changes.
* When running in Native mode, Cloud Firestore provides real-time data synchronization and offline support.

## Virtual Private Cloud (VPC)

* Enterprise can logically isolate its cloud resources by creating a virtual private cloud (VPC).
* A distinguishing feature of GPC is that a VPC can span the globe without relying on the public Internet. Traffic from any server on a VPC can be securely routed through the Google global network to any other point on that network.
* Another advantage of the Google network structure is that your backend servers can access Google services, such as machine learning or IoT services, without creating a public IP address for backend servers.
* VPCs in the Google Cloud can be linked to on-premise virtual private networks using Internet Protocol Security (IPSec).
* Although a VPC is global, enterprises can use separate projects and billing accounts to manage different departments or groups within the organization. Firewalls can be used to restrict access to resources on a VPC as well.

## Cloud CDN

* With content delivery networks (CDNs), users anywhere can request content from systems distributed in various regions. CDNs enable low-latency response to these requests by caching content on a set of endpoints across the globe.
* Google currently has more than 90 CDN endpoints that are managed as a global resource, so there is no need to maintain region-specific configurations.
* CDNs are especially important for sites with large amounts of static content and a global audience. News sites, for example, could use the Cloud CDN service to ensure fast response to requests from any point in the world.

## Specialized Services

### Apigee API Platform

* The Apigee API platform is a management service for GCP customers providing API access to their applications.
* The Apigee platform allows developers to deploy, monitor, and secure their APIs.
* It is difficult to predict load on an API, and sometimes spikes in use can occur. For those times, the Apigee API platform provides routing and rate-limiting based on policies customers can define.





