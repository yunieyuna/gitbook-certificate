# Exam 3

### 1. You have determined that an application using a service account is not functioning correctly. You think it may be an access control problem. You would like to view audit logs to determine if this is the case. What audit log would you review?

A. Admin Activity Log

B. Data Access Audit Log

C. Policy Denied Audit Log

D. Identity Access Audit Log



**Explanation**

C. The Policy Denied Audit Log captures details when a user or service account is denied access because of a security policy violation. The Admin Activity Log tracks administrative actions including changes to configurations and metadata. The Data Access Audit Log tracks changes or reads of resource data or metadata. There is no Identity Access Audit Log in GCP.



### 2. A DevOps engineer has just joined your team and needs to review audit logs. Which of the following roles could you use to grant the needed permissions without granting more permissions than needed to read logs?

A. roles/logging.privateLogsViewer

B. roles/logging.admin

C. roles/logging.configWriter

D. roles/logging.bucketWriter



**Explanation**

A. roles/logging.privateLogsViewer provides provides read-only access to log entries in logs, including private logs. roles/logging.admin would give permission to review logs but would also grant other permissions that are not needed. roles/logging.configWriter grants permissions to read and write the configurations of logs-based metrics and sinks for exporting logs. roles/logging.bucketWriter provides permission to write to a Cloud Storage bucket.



### 3. Your most recent GCP bill is higher than expected because of a significant increase in storage charges. Your department recently enabled an audit log that is off by default for most services. You think that audit logging may be responsible for the increased storage charges. Which type of audit log would you think could be responsible?

A. System Event Audit Log

B. Data Access Audit Log

C. Admin Activity audit logs

D. Policy Denied Audit Log



**Explanation**

B. Data Access Audit logs generate large amounts of data and are disabled by default for most services; it is enabled by default for BigQuery. The other audit logs are not likely to generate the same volume of data as the Data Access Audit logs.



### 4. You have created a new set of service accounts and want them to be used by existing VMs running in Compute Engine. What command would you use to assign one of the service accounts to a VM instance?

A. gcloud compute service-accounts assign

B. gcloud compute instances assign

C. gcloud compute instances set-service-account

D. gcloud instances set-service-account



**Explanation**

C. The command gcloud compute instances set-service-account assigns a service account to a VM instance. The other options are not valid gcloud commands.



### 5. A system admin needs to be able to create an instance that runs as a service account, attaches a persistent disk to an instance that runs as a service account, and set instance metadata on an instance that runs as a service account. Which of the following roles are required to meet those requirements?

A. roles/compute.storageAdmin

B. roles/compute.instanceAdmin.v1

C. roles/compute.imageUser

D. roles/iam.serviceAccountUser

E. roles/iam.serviceAccountCreator



**Explanation**

B, D. roles/compute.instanceAdmin.v1 gives full control of Compute Engine instances, instance groups, disks, snapshots, and images. roles/iam.serviceAccountUser gives permission to run operations as the service account.



### 6. You have been given the responsibility to manage projects in GCP. What set of permissions will you need to manage projects?

A. resourcemanager.projects.getIamPolicy and resourcemanager.projects.setIamPolicy only

B. resourcemanager.projects.get only

C. resourcemanager.projects.get, resourcemanager.projects.getIamPolicy, and resourcemanager.projects.setIamPolicy only

D. resourcemanager.projects.get and resourcemanager.projects.setIamPolicy only



**Explanation**

C. The permissions, resourcemanager.projects.get, for retrieving projects identified by a project ID, resourcemanager.projects.getIamPolicy, for getting IAM access control policy for the specified Project, and resourcemanager.projects.setIamPolicy, for setting IAM access control policy for the specified project, are all required.



### 7. You have been given the responsibility to manage several projects in GCP. You want to list roles defined in a particular project. What Cloud SDK command would you use? (Note: \[PROJECT] is a placeholder for a project identifier.)

A. gcloud iam roles list --project=\[PROJECT]

B. gcloud iam list roles --project=\[PROJECT]

C. gsutil iam list roles --project=\[PROJECT]

D. gsutil list iam roles \[PROJECT]



**Explanation**

A. gcloud iam roles list --project=\[PROJECT] is the correct command. Gsutil is the command line for managing Cloud Storage, not IAM.



### 8. A colleague who is new to GCP has asked for your help with understanding predefined roles. They would like to know details about several predefined roles. What command would you suggest they use?

A. gcloud roles predefined describe \[ROLE-ID]

B. gcloud iam roles describe \[ROLE-ID]

C. gcloud iam roles list \[ROLE-ID]

D. gcloud roles predefined describe \[ROLE-ID]



**Explanation**

B. gcloud iam roles describe \[ROLE-ID] is the correct command for displaying information about a role.



### 9. You are considering running a Windows server in GCP. You would like to review a list of Windows Server images available. What command would you use?

A. gcloud compute list windows-cloud

B. gcloud compute instances describe windows-cloud

C. gcloud compute images list --project windows-cloud --no-standard-images

D. gcloud compute images describe --project windows-cloud --no-standard-images



**Explanation**

C. The command gcloud compute images list --project windows-cloud --no-standard-images will list Windows Server images. List provides a list of images with minimal information. Describe is used to show more detailed information.



### 10. Your team uses a number of custom images. You want to be able to release new versions of each image while still maintaining the ability to rollback to a previous version if needed. What feature of Compute Engine would you use for this purpose?

A. image families

B. managed instance groups

C. unmanaged instance groups

D. community supported images



**Explanation**

A. Image families are used to group related images together so you can roll forward or back between specific images versions. Image families always point to the latest version of an image that is not deprecated. Managed and unmanaged instance groups are types of clusters, not an image management feature. Community supported images not directly supported by Compute Engine and are maintained by community members.



### 11. A team of developers would like to have a standard work environment in Compute Engine. You would like to be able to create multiple instances with identical configurations. The configurations should be easy to change. What feature of Compute Engine would you use specify the configuration?

A. instance template

B. managed instance groups

C. unmanaged instance groups

D. snapshot



**Explanation**

A. Instance templates specify the configuration of virtual machines and managed instance groups. Unmanaged instance groups may be heterogeneous and do not use instance templates. Snapshots are copies of disks at a point in time. They are useful for backups and copying disks but are not used for specifying configurations.



### 12. A client has asked you to help implement a cluster of servers that can scale up and down as needed and will be resilient to a failure in a zone. What feature of Compute Engine would you use?

A. unmanaged instance groups

B. managed instance groups

C. instance templates

D. snapshot



**Explanation**

B. Managed instance groups are used to create sets of identically configured VMs that can autoscale an can be configure for regional deployment, which would address the need to be resilient to a failure in a single zone.



### 13. A client of yours needs to be sure that only applications from their project run on the same physical server as their applications. What feature of Compute Engine would you recommend?

A. Shielded VMs

B. Sole-tenant nodes

C. Managed instance groups

D. Preemptible VMs



**Explanation**

B. Sole-tenant nodes provides for exclusive access to a physical server. Shielded VMs provide additional security protections but do not guarantee sole-tenancy. Managed instance groups is a set of identically configured VMs. Preemptible VMs are low cost VMs that may be shutdown at any time by Google.



### 14. Your use of GCP has grown significantly and you now have many resources to manage. Some resources are in different environments and some are for different teams. You would like to easily group resources so you can manage them more effectively. What feature of GCP would you use?

A. Labels

B. Images

C. Snapshots

D. Managed instance groups



**Explanation**

A. Labels allow you to specify key-value pairs for grouping resources, for example, a VM cloud be labeled with the key value pair 'envior:production.'



### 15. You would like to grant a role to an identity so that it can access a resource. Which of the resource's subcommands would you use to grant a role on a resource?

A. add-iam-policy-binding with no flags

B. add-iam-policy-binding with --member and --role flags

C. set-iam-policy with --member and --role flags

D. set-iam-policy with no flags



**Explanation**

B. The correct subcommand is add-iam-policy-binding with --member and --role flags. The subcommand is available for several resource types, including: disk, images, instances, and snapshots among others.



### 16. A VM is mistakenly started in the wrong region and zone. You suspect the default region and zone setting for your project is set incorrectly. What command would you use on the command line to show the default region and zone?

A. gcloud project info describe

B. gcloud project info list

C. gcloud project-info describe --project \[PROJECT ID]

D. gcloud compute project-info describe --project \[PROJECT ID]



**Explanation**

D. This is a compute service setting so you would use gcloud compute and the resource is a project so project-info is required. The correct command is gcloud compute project-info describe --project \[PROJECT ID].



### 17. You would like to use SSH host keys on your VMs to improve security. What feature of Compute Engine VMs do you need to enable to store SSH host keys?

A. Shielded VMs

B. Sole-tenant nodes

C. guest attributes

D. labels



**Explanation**

C. The correct answer is guest attributes. When guest attributes are enabled, Compute Engine will store your generated host keys as guest attributes.



### 18. As an administrator of a Kubernetes Engine cluster with many users from several teams and departments, you would like to easily analyze resource usage by team and department. What mechanisms could you use to differentiate resource usage?

A. Labels

B. Guest attributes

C. Namespaces

D. key-value pairs

E. instance attributes



**Explanation**

A, C. Labels are key/value pairs that are attached to objects to specify identifying attributes of objects that are useful for users and admins. Namespaces are virtual clusters designed for environments like the one described, with many users, team, or other organization group structures.



### 19. You want to create an autoscaling Kubernetes cluster in Kubernetes Engine. What type of command would you specify?

A. gcloud container clusters create with --enable-autoscaling flag and --min-nodes and max-nodes parameters.

B. gcloud kubernetes clusters create with --enable-autoscaling flag and --min-nodes and max-nodes parameters.

C. kubectl clusters create with --enable-autoscaling flag and --min-nodes and max-nodes parameters.

D. kubectl containers create with --enable-autoscaling flag and --min-nodes and max-nodes parameters.



**Explanation**

A. The correct command is gcloud container clusters create with --enable-autoscaling flag and --min-nodes and max-nodes parameters. Kubectl is a command line for managing resources, such as pods, within a Kubernetes cluster.



### 20. You are running several services in Cloud Run. You will need to programmatically determine the name of the configuration that created the container. Where would you find this?

A. In the K\_Configuration environment variable

B. In the container startup script

C. In the service startup script

D. In the VM instance metadata



**Explanation**

A. When Cloud Run starts a container, it creates environment variables: K\_Configuration, K\_Revision, K\_Service, and Port. K\_Configuration specifies the configuration that created the container.



### 21. An app development team wants to develop a service written in C++ that can process a file after it is uploaded to Cloud Storage. The processing time varies based on the size and complexity of the content of the file. Almost all files can be processed in less than 1 minute but some files can take up to 20 minutes to process. The developers are already using containers and Cloud Pub/Sub for other services. They plan to use Cloud Storage's trigger mechanism to send a message to Pub/Sub on upload. You want to minimize operational overhead while ensuring all files are processed correctly. What GCP compute service would you use?

A. Compute Engine

B. App Engine Standard

C. Cloud Run

D. Anthos



**Explanation**

C. Cloud Run can execute container images with custom applications written in any programming language. It is a managed service so operational overhead is minimized. Cloud Pub/Sub configured with a push subscription could invoke a service running in Cloud Run. Compute Engine is not a managed service and would have more operational overhead. App Engine Standard does not support C++ applications. Anthos is a platform for managing multiple Kubernetes clusters in multiple environments and while it could be used to run the service, it is more than required by the specifications.



### 22. You have deployed a service using App Engine that requires a batch job run every hour. You notice that the batch job is running every two hours instead of every hour. You'd like to change the job specification to correct the problem. What file would you edit to correct the problem?

A. app.yaml

B. cron.yaml

C. batch.yaml

D. job.yaml



**Explanation**

B. Cron.yaml files contain specifications for running scheduled jobs in App Engine. App.yaml has overall application specifications. Batch.yaml and job.yaml are not specified as part of App Engine services.



### 23. A game developer is using App Engine to run several services. One of the services queries a Datastore database for user information. Queries over a single property work correctly but queries that reference two or more properties are not returning any data. You have been asked to help diagnose the problem. Which file in the application would you look to first to diagnose the problem?

A. app.yaml

B. cron.yaml

C. index.yaml

D. dispatch.yaml



**Explanation**

C. Index.yaml files contain indexes for complex queries that reference more than one attribute. Datastore automatically creates indexes for single attributes. All queries must have a supporting index. App.yaml is for application specifications. Cron.yaml is for scheduled jobs. Dispatch.yaml is for overriding routing rules.



### 24. You have several buckets using Nearline storage class that you would like to change to Coldline storage. What command would you use?

A. gsutil rewrite -s Coldline gs://PATH\_TO\_OBJECT

B. gcloud storage rewrite -s Coldline gs://PATH\_TO\_OBJECT

C. gsutil newclass -s Coldline gs://PATH\_TO\_OBJECT

D. gcloud storage newclass -s Coldline gs://PATH\_TO\_OBJECT



**Explanation**

A. Gsutil is the command line utility for Cloud Storage. The rewrite command with the -s parameter is used to change storage classes.



### 25. You have just taken over responsibility to manage a large number of objects in Cloud Storage. You are reviewing a random sample of objects and want to know the creation time and content type for those objects. You plan to write a shell script to display this data. What command would you use in your script to retrieve that metadata?

A. gsutil metadata gs://BUCKET\_NAME/OBJECT\_NAME

B. gsutil stat gs://BUCKET\_NAME/OBJECT\_NAME

C. gsutil list gs://BUCKET\_NAME/OBJECT\_NAME

D. gsutil describe gs://BUCKET\_NAME/OBJECT\_NAME



**Explanation**

B. The correct command to list that metadata is gsutil stat gs://BUCKET\_NAME/OBJECT\_NAME.



### 26. A colleague has asked you to help them better managed multiple files in Cloud Storage. They would like to automate as much of the management as possible. You recommend using lifecycle management policies. What operations can be automatically performed using lifecycle policy management?

A. Delete

B. Enable versioning

C. Set storage class

D. Move files

E. Copy files



**Explanation**

A, C. The two operations that can be performed using Cloud Storage lifecycle management are deleting objects and setting the storage class.



### 27. Due to security concerns, you want to ensure all data written to your Cloud Storage buckets are encrypted. What do you need to do to ensure data is encrypted when stored in Cloud Storage?

A. Use the --encrypt flag with gsutil

B. Set a lifecycle policy that specifies encryption is on

C. Set up customer managed encryption keys and use those keys to encrypt data before saving to Cloud Storage

D. Nothing, this is the default behavior.



**Explanation**

D. All data stored in Google Cloud is encrypted before it is persisted. You do not have to do anything to ensure your data is encrypted at rest in GCP.



### 28. A team providing business intelligence solutions to your company is migrating to GCP. They make extensive use of SQL and want to continue to use SQL. They currently use relational databases to store data. Data is loaded every night. When data is older than 3 years, it is no longer needed. They expect the database to grow to 100 GB within six months. Most of the operations on the database query a few columns but scan many rows. They also want to minimize database management overhead. What GCP service would you recommend they use?

A. Bigtable

B. BigQuery

C. Cloud Firestore

D. Cloud SQL



**Explanation**

B. BigQuery is a managed analytical database that supports SQL. It is optimized for write once/read many operations. It can easily store 100 GB or more of data. It is a managed service designed to support data warehouses. Bigtable and Cloud Firestore are NoSQL databases and do not support SQL. Cloud SQL does support SQL but it is designed for transaction processing and does not support up to 100 GB in a single database.



### 29. A startup is deploying analytical services for Internet of Things (IoT) applications. The service will need to ingest large volumes of time series data in short periods of time. Users will query the data is a few different ways but those ways are known and fixed. What managed GCP database service would you recommend?

A. BigQuery

B. Bigtable(Correct)

C. Cloud SQL

D. Cloud Spanner



**Explanation**

B. Bigtable is a NoSQL wide-column database well suited to low latency writes. Since only a few, well defined query patterns are needed, you can design the data model to support those patterns. BigQuery does not support large volumes of low latency writes. Cloud SQL and Cloud Spanner are relational databases designed for transaction processing systems but this use case does not require a transaction processing system.



### 30. You are administering a project that uses BigQuery. You would like to list all the datasets in the project. What command would you use?

A. bq ls

B. bq dir

C. gsutil ls

D. gsutil dir



**Explanation**

A. BigQuery uses the bq command line. The command to list datasets is bq ls.



### 31. You would like to display information about a dataset named primarydata in a project called analytics1. What command would you use?

A. bq ls --format=prettyjson analytics1:primarydata

B. bq show --format=prettyjson analytics1:primarydata

C. bq metadata --format=prettyjson analytics1:primarydata

D. bq ls --format=prettyjson analytics1//primarydata



**Explanation**

B. The bq command is used with BigQuery and the show command displays information about a data set. Projects and datasets are specified as \[project name]:\[dataset name].



### 32. The CFO of your company is concerned that BigQuery costs are growing too large. They ask for recommendations on how to reduce the cost of querying without reducing the utility of the service. Most of the queries are based on the time the data arrived. What would you recommend as one way to reduce the amount of data scanned?

A. Use ingestion time partitioned tables and specify \_PARTITIONTIME filters when querying.

B. Use read replicas and query only the read replica not the primary, which is where data is written.

C. Use covering indexes to respond to queries using only the index without needing to seek additional blocks of data.

D. Use the LIMIT option in SELECT statements to prevent more than a fixed number of rows from being returned.



**Explanation**

A. Ingestion time partitioned tables creates partitions by ingestion time. The pseudo column \_PARTITIONTIME is added to the table and can be used to restrict the amount of data scanned. BigQuery does not provide for read replicas like some databases. BigQuery does not use indexes. The LIMIT option does not reduce the amount of data scanned, it only limits the number of rows returned.



### 33. A startup is developing an Internet of Things (IoT) service. When data is first ingested, some basic data quality checks are performed that ensure the format is correct. The data will be ingested using Pub/Sub. When new data arrives, it should automatically have the quality checks applied. The checks will always run for less than one second. What compute service would you use to apply the data quality checks?

A. Compute Engine

B. App Engine Standard

C. App Engine Flexible

D. Cloud Functions



**Explanation**

D. Cloud Functions are the best option since it is a managed service that can be invoked on events, such as when a message is ingested by Cloud Pub/Sub. Also the code to execute runs for short periods of time.



### 34. An IoT startup is uploading 2 TB of historical data to Cloud Storage. The data is in files with one file per day per sensor. There are thousands of files. The filenames are the date followed by sensor ID. The loads are not proceeding as quickly as expected. What might be the cause of the slower than expected upload?

A. The file names use the date as the first part of the filename so they may be creating hotspots when writing data to Cloud Storage.

B. The files are in CSV instead of Avro format.

C. The data in files is being encrypted before being persisted to storage.

D. The files are in gzip format instead of Avro format



**Explanation**

A. Files are written to servers within the Cloud Storage system based on filenames. Lexically close file names are written to the same server. This can lead to hotspots in which a few servers have heavy loads while other servers have little or no load.



### 35. You are working in Cloud Shell to diagnose a problem with a Cloud SQL server running MySQL. You would like to connect to the MySQL instance from the command line. What command would you use to connect to the database as root using the built-in client?

A. gcloud sql connect \[INSTANCE ID] --user=root

B. mysql --host=\[INSTANCE ID] --user=root

C. gsutil sql connect \[INSTANCE ID] --user=root

D. gcloud mysql connect \[INSTANCE IP] --user=root



**Explanation**

A. To use the client built into Cloud Shell, the correct command is gcloud sql connect followed by the instance ID of the database you want to connect to along with the --user parameter to specify the username.



### 36. You are hosting a large amount of image and video content for an educational service. Learners from around the world use the service. You currently host content on servers in your own data center in North America. Learners in Asia, Africa, and Europe experience long latencies loading content. What GCP service could you use to ensure that all learners experience the same level of latency and the latency is kept low, especially for frequently accessed content?

A. Cloud Storage Nearline Storage Class

B. Cloud CDN

C. Cloud VPN

D. Persistent disks



**Explanation**

B. Cloud CDN is a content distribution network for global content delivery. It caches data at distributed points around the world so users requests for content are routed to the closest content location.



### 37. You have created a virtual private cloud (VPC) in auto mode, which automatically creates a subnet in each region. How is the CIDR block determined for each region?

A. You will specify non-overlapping CIDR blocks for each region.

B. Each region will automatically be assigned a set of predefined IP ranges that fit within the 10.128.0.0/9 CIDR block.

C. You will specify non-overlapping CIDR ranges for the set of regions you want a subnet created for.

D. Each region will be automatically assigned a range of external IP addresses.



**Explanation**

B. When using auto mode VPC creation, a subnet is created in each region and each subnet is assigned a range of IP addresses that fit within the 10.128.0.0/9 CIDR block.



### 38. A data scientist is running several large queries against BigQuery. They would like to know how much the query will cost before running the query. How would recommend they do that?

A. Use the bq query command with the --estimate-cost flag

B. Use the bq query command with the --dry\_run flag

C. Use the bq query command with the --cost flag

D. Use the bq query command with the --limit parameter and the --scan parameter



**Explanation**

B. The --dry\_run flag is used with the bq query command to estimate the cost of running a query.



### 39. You are setting up a service in Kubernetes Engine. You would like to have all internal clients send requests to a stable internal IP address. What type of service would you create?

A. Headless

B. NodePort

C. LoadBalancer

D. ClusterIP



**Explanation**

D. ClusterIP service is the default type of service and is used to enable internal clients to send requests to a stable internal IP address. Headless service type is used when a stable IP address is not needed. NodePort is used to enable clients to send requests to the IP address of a node on one or more nodePort values specified by the service. LoadBalancer clients send request to the IP address of a network load balancer.



### 40. A developer would like to create an image from a snapshot. What command should they use to create an image named devimage1 from a snapshot called devsnapshot1?

A. gcloud compute images create devimage1 --source-snapshot devsnapshot1

B. gcloud disk images create devimage1 --source-snapshot devsnapshot1

C. gcloud images create devimage1 --source-snapshot devsnapshot1

D. gcloud disk create devimage1 --source-snapshot devsnapshot1



**Explanation**

A. Images are Compute Engine resources so they use gcloud compute commands. Images are the resource that is being created so the command is gcloud compute images create followed by the image name and the source-snapshot parameter.



### 41. A distributed application uses Cloud Pub/Sub to send messages to a service that analyzes the data. Each message should only be sent once but for some reason, messages are sent repeatedly. What configuration parameter would you investigate in order to correct this problem?

A. --dead-letter-topic

B. --ack-deadline

C. --max-retry-delay

D. min-retry-delay



**Explanation**

B. The problem may be caused by the consuming application not acknowledging the message has been successfully processed within the time required. The --ack-deadline may be set too low and the consuming application may not send the acknowledgement within that time. Increasing the --ack-deadline would give the consuming application more time to acknowledge successful processing of the message.



### 42. You believe you may have over provisioned several VMs. You would like to get data on the CPU load at 15 minute intervals from all Linux servers. How would you do this with the least amount of work?

A. Install a bash script that uses the sar -u command to get CPU utilization and write the value to syslog.

B. Install a bash script that uses the sar -u command to get CPU utilization and write the value to sysout.

C. Install the Cloud Monitoring agent on each server and monitor the load\_15m metric.

D. Install the Prometheus agent on each server and monitor the load\_15m metric.



**Explanation**

C. The Cloud Monitoring agent collects data on CPU utilization and other metrics. Installing the agent and then view the collected data with Cloud Monitoring requires the least amount of work.



### 43. To improve the security of your applications, you want to create several custom roles with limited permissions. What role would give you sufficient permission to create custom roles?

A. roles/iam.roles.create

B. roles/iam.roles.create.custom

C. roles/iam.serviceAccountUser

D. roles/iam.serviceAccountUser.create



**Explanation**

A. The role roles/iam.roles.create will provide the permissions required to create custom roles.



### 44. You need to deploy a load balancer that will support external clients using TCP traffic, including SSL. You want to offload SSL processing. What load balancer would you deploy?

A. HTTP(S) Load Balancing

B. SSL Proxy

C. TCP Proxy

D. Network TCP/UDP Load Balancing



**Explanation**

B. SSL Proxy should be used for external TCP traffic with the SSL processing offloaded to the the proxy.



### 45. You need to deploy a load balancer that will support internal TCP traffic within a single region. What load balancer would you deploy?

A. Network TCP/UDP Load Balancing

B. SSL Proxy

C. TCP Proxy

D. Internal HTTP(S) Load Balancing



**Explanation**

A. Network TCP/UDP Load Balancing is used for internal TCP traffic.



### 46. A team of data scientists wants to migrate an on premises Spark cluster to Google Cloud. They would like to use a managed service. What GCP service would you recommend?

A. Cloud Data Studio

B. Cloud Dataproc

C. Cloud Dataflow

D. Cloud Bigtable



**Explanation**

B. Cloud Dataproc is a managed Spark/Hadoop cluster service. Cloud Data Studio is a reporting and analytics tool. Cloud Dataflow is a batch and stream processing platform. Cloud Bigtable is a NoSQL database.



### 47. Your team has created a set of Docker images. You want to be able to better manage groups of containers. What could you do to images to enable grouping by environment, installed component, etc?

A. Add tags with the gcloud container images add-tag command

B. Set the account parameter when creating the images

C. Set the billing account parameter when creating the image

D. Add configurations with the gcloud container images add-configuration command



**Explanation**

A. Tags are used to group resources in GCP. They are added to images using the gcloud container images add-tag command.



### 48. A group of epidemiologists is running a large number of simulations. They are using several high CPU virtual machines. Each simulation takes approximately 10 minutes to complete. If a simulation fails before completing, it is restarted on another VM. The epidemiologists would like to minimize the GCP costs without increasing the time need to complete a simulation. What would you recommend?

A. Use more virtual machine instances

B. Use preemptible virtual machine instances

C. Use Shielded VM instances

D. Use sole-tenant VMS



**Explanation**

B. Preemptible VMs cost significantly less then standard priced VMs. Preemptible VMs run up to 24 hours before being shut down by Google. The epidemiologist could can tolerate failures in some simulations since failed simulation are re-run.



### 49. As a consultant to a global logistics company, you have been asked to advise on the migration from an on premises inventory system to Google Cloud. The inventory system uses a relational database. Your client wants to use a managed database service that supports users in multiple regions. Inventory data needs to be consistent at all times. What service would you recommend?

A. Cloud Bigtable

B. Cloud BigQuery

C. Cloud Spanner

D. Cloud SQL



**Explanation**

C. Cloud Spanner is a globally scalable, managed relational database that supports consistency. Cloud Bigtable is a NoSQL database. BigQuery is an analytical database. Cloud SQL is a relational database but it is designed for regional use cases.



### 50. A developer has to work with several clients all using Google Cloud. They would like to easily switch between clients when working on the command line. What would you recommend they do?

A. Create a configuration for each client and use the gcloud config configurations activate command to activate the appropriate configuration for each client.

B. Create a configuration for each client and use the gcloud auth command to activate the appropriate configuration for each client.

C. Create a policy for each client and use the gcloud policy command to activate the appropriate policy for each client.

D. Create a policy for each client and use the gcloud auth-policy command to activate the appropriate policy for each client.



**Explanation**

A. The gcloud config configurations activate command allows for rapid changes to the configuration for the Cloud SDK and could be used for that purpose in this use case.



