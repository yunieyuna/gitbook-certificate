# Chapter 11. Planning Storage in the Cloud

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

#### 1. You are tasked with defining lifecycle configurations on buckets in Cloud Storage. You need to consider all possible options for transitioning from one storage class to another. All of the following transitions are allowed except for one. Which one is that?

A. Nearline to coldline

B. Regional to nearline

C. Multiregional to coldline

D. Regional to multiregional



Answers:

D. Once a bucket is created as either regional or multiregional, it cannot be changed to the other, so option D is correct. Nearline to coldline and regional to nearline are both allowed, as is multiregional to coldline.



#### 2. Your manager has asked for your help in reducing Cloud Storage charges. You know that some of the files stored in Cloud Storage are rarely accessed. What kind of storage would you recommend for those files?

A. Nearline

B. Regional

C. Coldline

D. Multiregional



Answers:

C. The goal is to reduce cost, so you would want to use the least costly storage option. Coldline has the lowest per-gigabyte charge at $0.07/GB/month, so option C is correct. Nearline is the next lowest followed by regional. Multiregional has the highest per-gigabyte charge. Both nearline and coldline have access charges, but those are not considered in this question.



#### 3. You are working with a startup developing analytics software for IoT data. You have to be able to ingest large volumes of data consistently and store it for several months. The startup has several applications that will need to query this data. Volumes are expected to grow to petabyte volumes. Which database should you use?

A. Cloud Spanner

B. Bigtable

C. BigQuery

D. Datastore



Answers:

B. Bigtable is a wide-column database that can ingest large volumes of data consistently, so option B is correct. It also supports low-millisecond latency, making it a good choice for supporting querying. Cloud Spanner is a global relational database that is not suitable for high-speed ingestion of large volumes of data. Datastore is an object data model and not a good fit for IoT or other time series data. BigQuery is an analytics database and not designed for ingestion of large volumes of data in short periods of time.



#### 4. A software developer on your team is asking for your help improving the query performance of a database application. The developer is using a Cloud SQL MySQL, Second Generation instance. Which options would you recommend?

A. Memorystore and SSD persistent disks

B. Memorystore and HDD persistent disks

C. Datastore and SSD persistent disks

D. Datastore and HDD persistent disks



Answers:

A. Option A is correct because Memorystore is a managed Redis cache. The cache can\
be used to store the results of queries. Follow-on queries that reference the data stored in the cache can read it from the cache, which is much faster than reading from persistent disks. SSDs have significantly lower latency than hard disk drives and should be used for performance-sensitive applications like databases. Options B and D are incorrect because HDD persistent disks do give the best performance with respect to IOPS. Options C and D are incorrect because Datastore is a managed NoSQL database and would not have any impact on SQL query performance.



#### 5. You are creating a set of persistent disks to store data for exploratory data analysis. The disks will be mounted on a virtual machine in the us-west2-a zone. The data is historical data retrieved from Cloud Storage. The data analysts do not need peak performance and are more concerned about cost than performance. The data will be stored in a local relational database. Which type of storage would you recommend?

A. SSDs

B. HDDs

C. Datastore&#x20;

D. Bigtable



Answers:

B. HDDs are the better choice for persistent disks for a local database when performance\
is not the primary concern and you are trying to keep costs down, so option B is correct. Option A is wrong because SSDs are more expensive and the users do not need the lowest latency available. Options C and D are wrong; both of those are other databases that would not be used to store data in a local relational database.



#### 6. Which of the following statements about Cloud Storage is not true?

A. Cloud Storage buckets can have retention periods.

B. Lifecycle configurations can be used to change storage class from regional to multiregional.

C. Cloud Storage does not provide block-level access to data within files stored in buckets.

D. Cloud Storage is designed for high durability.



Answers:

B. Lifecycle configurations can change storage class from regional to nearline or coldline. Once a bucket is created as regional or multiregional, it cannot be changed to the other, so option B is the right answer. Option A is true; you can set retention periods when creating a bucket. Option C is true; Cloud Storage does not provide file system–like access to internal data blocks. Option D is true because Cloud Storage is highly durable.



#### 7. When using versioning on a bucket, what is the latest version of the object called?

A. Live version

B. Top version

C. Active version

D. Safe version



Answers:

A. The most recent version of an object is called the live version, so option A is correct. Options B and C are incorrect; top and active are not terms used to refer to versions. Option D is incorrect because option A is correct.



#### 8. A product manager has asked for your advice on which database services might be options for a new application. Transactions and support for tabular data are important. Ideally, the database would support common query tools. What databases would you recommend the product manager consider?

A. BigQuery and Spanner&#x20;

B. Cloud SQL and Spanner&#x20;

C. Cloud SQL and Bigtable&#x20;

D. Bigtable and Spanner



Answers:

B. Both Cloud SQL and Spanner are relational databases and are well suited for transaction- processing applications, so option B is right. Option A is incorrect because BigQuery is relational, but it is designed for data warehousing and analytics, not transaction processing. Options C and D are incorrect because Bigtable a wide-column NoSQL database, not a relational database.



#### 9. The Cloud SQL service provides fully managed relational databases. What two types of databases are available in Cloud SQL?

A. SQL Server and MySQL

B. SQL Server and PostgreSQL

C. PostgreSQL and MySQL

D. MySQL and Oracle



Answers:

C. Both MySQL and PostgreSQL are Cloud SQL options so Option C is correct. Options A and B are incorrect, SQL Server is not a Cloud SQL option. Option D is incorrect because Oracle is not a Cloud SQL option. You could choose to run SQL Server or Oracle on your instances but you would have to manage them, unlike Cloud SQL managed databases.



#### 10. Which of the following Cloud Spanner configurations would have the highest hourly cost?

A. Located in us-central1

B. Located in nam3

C. Located in us-west1-a

D. Located in nam-eur-asia1



Answers:

D. The multiregional and multi-super-regional location of nam-eur-aisa1 is the most expensive, which makes option D the right answer. Option A is a region that costs less than the multi-super-regional nam-eur-asia1. Option C is incorrect; that is a zone, and Spanner is configured to regions or super regions. Option B is incorrect; it is only a single super region, which cost less than deploying to multiple super regions.



#### 11. Which of the following are database services that do not require you to specify configuration information for VMs?

A. BigQuery only

B. Datastore only

C. Firebase and Datastore

D. BigQuery, Datastore, and Firebase



Answers:

D. BigQuery, Datastore, and Firebase are all fully managed services that do not require you to specify configuration information for VMs, which makes option D correct. Cloud SQL and Bigtable require you to specify some configuration information for VMs.



#### 12. What kind of data model is used by Datastore?&#x20;

A. Relational

B. Document

C. Wide-column&#x20;

D. Graph



Answers:

B. Datastore is a document database, which makes option B correct. Cloud SQL and Span- ner are relational databases. Bigtable is a wide-column database. Google does not offer a managed graph database.



#### 13. You have been tasked with creating a data warehouse for your company. It must support tens of petabytes of data and use SQL for a query language. Which managed database service would you choose?

A. BigQuery

B. Bigtable

C. Cloud SQL

D. SQL Server



Answers:

A. BigQuery is a managed service designed for data warehouses and analytics. It uses standard SQL for querying, which makes option A the right answer. Bigtable can support the volume of data described, but it does not use SQL as a query language. Cloud SQL is not the best option to scale to tens of petabytes. SQL Server is a relational database from Microsoft; it is not a GCP-managed database service.



#### 14. A team of mobile developers is developing a new application. It will require synchronizing data between mobile devices and a backend database. Which database service would you recommend?

A. BigQuery&#x20;

B. Firestore&#x20;

C. Spanner&#x20;

D. Bigtable



Answers:

B. Firestore is a document database that has mobile supporting features, like data synchro- nization, so option B is the right answer. BigQuery is for analytics, not mobile or transac- tional applications. Spanner is a global relational database but does not have mobile-specific features. Bigtable could be used with mobile devices, but it does not have mobile-specific features like synchronization.



#### 15. A product manager is considering a new set of features for an application that will require additional storage. What features of storage would you suggest the product manager consider?

A. Read and write patterns only

B. Cost only

C. Consistency and cost only

D. None, they are all relevant considerations.



Answers:

D. In addition to read and write patterns, cost, and consistency, you should consider trans- action support and latency, which makes option D correct.



#### 16. What is the maximum size of a Memorystore cache?&#x20;

A. 100GB

B. 300GB&#x20;

C. 400GB&#x20;

D. 50GB



Answers:

B. Option B is correct because Memorystore can be configured to use between 1GB and 300GB of memory.



#### 17. Once a bucket has its storage class set to coldline, what are other storage classes it can transition to?

A. Regional

B. Nearline

C. Multi-regional

D. None of the above



Answers:

D. Once a bucket is set to coldline, it cannot be changed to another storage class; thus, option D is correct. Regional and multiregional can change to nearline and coldline. Nearline buckets can change to coldline.



#### 18. Before you can start storing data in BigQuery, what must you create?

A. A data set

B. A bucket

C. A persistent disk

D. An entity



Answers:

A. To use BigQuery to store data, you must have a data set to store it, which makes option A the right answer. Buckets are used by Cloud Storage, not BigQuery. You do not manage persistent disks when using BigQuery. An entity is a data structure in Datastore, not Big- Query.



#### 19. What features can you configure when running a Second Generation MySQL database in Cloud SQL?

A. Machine type

B. Maintenance windows

C. Failover replicas

D. All of the above



Answers:

D. With a second-generation instance, you can configure the MySQL version, connectivity, machine type, automatic backups, failover replicas, database flags, maintenance windows, and labels, so option D is correct.



#### 20. A colleague is wondering why some storage charges are so high. They explain that they have moved all their storage to nearline and coldline storage. They routinely access most of the object on any given day. What is one possible reason the storage costs are higher than expected?

A. Nearline and coldline incur access charges.

B. Transfer charges.

C. Multiregional coldline is more expensive.

D. Regional coldline is more expensive.



Answers:

A. Access charges are used with nearline and coldline storage, which makes option A cor- rect. There is no transfer charge involved. Options C and D do not refer to actual storage classes.

