# Exam 1

#### 1. Your organization has created multiple projects in several folders. You have been assigned to manage and want to get descriptive information about each project. What command would you use to get metadata about a project?

A. gcloud projects describe \[PROJECT\_ID] or gcloud projects describe \[PROJECT\_NAME]

B. gcloud projects describe \[PROJECT\_NAME] only

C. gcloud describe project \[PROJECT\_ID] only

D. gcloud describe project \[PROJECT\_NAME] only



**Answers:**

A. The correct command is gcloud projects describe followed by the PROJECT\_ID or the PROJECT\_NAME.



#### 2. A new team member has just created a new project in Google Cloud. What role is automatically granted to them when they create the project?

A. roles/editor

B. roles/owner

C. roles/brower

D. roles/viewer



**Answers:**

B. When you create a project, you are automatically granted the roles/owner role. The owner role includes permissions granted by roles/editor, roles/viewer, and roles/browser.



#### 3. Your organization has created multiple folders, one for each department. In each folder, departments have one or more projects. What would you expect resources within the folder to share?

A. Service acounts

B. Permissions

C. IAM policies

D. IAM roles



**Answers:**

C. Folders are used to group resources that share common IAM policies. Service accounts are specific to a set of operating requirements within a project. Permissions are associated with roles but not directly with folders. IAM roles are granted to identities, not folders.



#### 4. A manager in your company is having trouble tracking the use and cost of resources across several projects. In particular, they do not know which resources are created by the different teams they manage. What would you suggest the manager use to help better understand which resources are used by which team?

A. Audit logs

B. Labels

C. Trace logs

D. IAM policies



**Answers:**

B. Labels are key-value pairs attached to resources and used to manage them. The manager could use a key-value pair with the key 'team-name' and the value the name of the team that created the resource. Audit logs do not necessarily have the names of teams that own a resource. Traces are used for performance monitoring and analysis. IAM policies are used to control access to resources, not to track which team created them.



#### 5. An auditor is reviewing your Google Cloud use. They have asked for access to any audit logs available in GCP. What audit logs are available for each project, folder, and organization?

A. Admin Activity

B. Data Access

C. Policy Access

D. System Event

E. User Login

F. Performance Metrics



**Answers:**

A, B, D. Cloud Audit Logs maintain three audit logs: Admin Activity logs, Data Access logs, and System Event logs. There is no such thing as a Policy Access log, a User Login log, or a Performance Metric log in GCP Audit Logs.



#### 6. To avoid potentially violating a regulation, your company has determined that it will only use Google Cloud resources in North America. How would you ensure no resources are created outside of North America?

A. Create a policy at the organization level of the resource hierarchy that includes a constraint using a Resource Location Restriction.

B. Create an IAM policy that prevents users from creating resources outside of North America.

C. Create a policy at the folder level of the resource hierarchy that includes a constraint using a Resource Location Restriction.

D. Create a data lifecycle management policy that prevents data from being saved outside of North America.



**Answers:**

A. Constraints are the standard way to restrict where resources can be created and applying policies with constraints will enforce those constraints for all resources in the organization. If the policy were applied at the folder level, it would have to be applied for all folders and that is not as efficient as applying at the organization level.



#### 7. You want to use Cloud Identity to create identities. You have received a verification record for your domain. Where would you add that record?

A. In IAM settings for each identity

B. In the domain's DNS setting

C. In the metadata of each resource created in your organization

D. In the billing account for your organization



**Answers:**

B. Cloud Identity provides domain verification records, which are added to DNS settings for the domain.



#### 8. As a consultant to a new Google Cloud customer, you are asked to help set up billing accounts. What permission must an identity have in order to create a billing account?

A. billing.create

B. roles/billing.create

C. billing.accounts.create

D. roles/billing.accounts.create



**Answers:**

C. billing.accounts.create is the permission needed to create a billing account. Roles are sets of permissions but they are not permissions themselves.



#### 9. Your company has a complicated billing structure for Google Cloud projects. You would like to set up multiple configurations for use with the command line interface. What command would you use to create those?

A. gcloud config configurations create

B. gcloud configurations create

C. gcloud config configurations set

D. gcloud configurations set



**Answers:**

A. The correct command is gcloud config configurations create.



#### 10. As a developer using Google Cloud, you will need to set up a local development environment. You will want to authorize the use of gcloud commands to access resources. What commands could you use to authorize access?

A. gcloud init

B. gcloud login

C. gcloud auth login

D. gcloud config login



**Answers:**

A, C. Gcloud init will authorize access and perform other common setup steps. Gcloud auth login will authorize access only.



#### 11. A client of yours has a Python 3 application that provides an API endpoint that runs continually. The service usually has very little load but sometimes experiences sudden and extreme spikes in traffic. They want to run it in Google Cloud but they want to keep costs as low as possible. They also want to minimize management overhead. What service would you recommend?

A. Compute Engine

B. Kubernetes Engine

C. Cloud Functions

D. App Engine



**Answers:**

D. App Engine is designed for applications written in supported languages, including Python 3, that need to run at low cost and scale in response to rapid increases in load. App Engine is a managed service and as such minimizes operational overhead. If the application were containerized, Cloud Run would also be an option. Compute Engine and Kubernetes Engine both require more management overhead. Cloud Functions are used to respond to events in GCP, not to execute a continually running application.



#### 12. You will be running an application that requires high levels of security. You want to ensure the application does not run on a server that has been compromised by a rootkit or other kernel-level malware. What kind of virtual machine would you use?

A. Preemptible VM

B. Shielded VM

C. Hardened VM

D. GPU-enabled VM

\
**Answers:**

B. Shielded VMs are hardened virtual machines that use Secure Boot, virtual trusted platform module enabled Measured Boot, and integrity monitoring.



#### 13. A developer is trying to upload files from their local device to a Compute Engine VM using the gcloud compute scp command. The copy command is failing. What would you check to try to correct the problem?

A. Add the identity of the developer to the administrator group for the VM.

B. Ensure firewall rules allow traffic to port 22 to allow SSH connections.

C. Grant the identity the roles/compute.admin role

D. Grant the identity compute.admin permission



**Answers:**

B. To copy files to a VM, a firewall rule must be in place to allow traffic on port 22, the default SSH port.



#### 14. You want to clone a persistent disk. What characteristics of the source and cloned disk must be the same?

A. Zone

B. Region

C. Size

D. disk type



**Answers:**

A, B, D. The source and cloned disk must be in the same zone and region and must be of the same type. The size of the clone must be at least the size of the source disk.



#### 15. You have a set of snapshots that you keep as backups of several persistent disks. You want to know the source disk for each snapshot. What command would you use to get that information?

A. gcloud snapshots describe

B. gcloud compute snapshots list

C. gcloud compute snapshots describe

D. gcloud compute disk describe



**Answers:**

C. The correct command is gcloud compute snapshots describe which shows information about the snapshot, including source disk, creation time, and size.



#### 16. Your department runs a legacy application on an on premises cluster. The nodes in the cluster are heterogeneous. You want to migrate this cluster to Google Cloud. What Compute Engine resource would you use?

A. Managed instance groups (MIGs)

B. Unmanaged instance group

C. Network load balancer

D. Autoscaler



**Answers:**

B. Heterogeneous clusters can be run on unmanaged instance groups but not managed instance groups.



#### 17. An application running in Compute Engine sometimes gets spikes in load. You want to add instances automatically when the load increases significantly and plan to use managed instance groups. What would you need to create in order to automatically scale the cluster?

A. Instance template

B. Snapshot

C. Persistent Disk

D. Shielded VM



**Answers:**

A. An instance template is needed to enable Compute Engine to automatically add instances to a managed instance group.



#### 18. You have deployed a sole tenant node in Compute Engine. How will this restrict what VMs run on that node.

A. Only VMs from the same organization will run on that node.

B. Only VMs from the same project will run on the node.

C. Only one VM will run on that node.

D. Only VMs using the same operating system will run on that node.



**Answers:**

B. On a sole tenant node, only VMs from the same project will run on that node. They do not need to use the same operating system. Sole tenant nodes are not restricted to a single VM.



#### 19. You have created a target pool with instances in two zones that are in the same region. The target pool is not functioning correctly. What could be the cause of the problem?

A. The target pool is missing a health check.

B. The target pool nodes are configured with different memory specifications

C. The target pool is not sending metrics to Cloud Monitoring.

D. The target pool is not sending logs to Cloud Logging.



**Answers:**

A. Target pools must have a health check to function properly. Nodes can be in different zones but must be in the same region. Cloud Monitoring and Cloud Logging are useful but they are not required for the target pool to function properly. Nodes in a pool have the same configuration.



#### 20. A startup has an app that allows users to upload images to Cloud Storage. The images should be analyzed as soon as possible once they are loaded. Processing takes approximately 1 second for each image. There are periods when no images are uploaded and other times when many images are uploaded in short periods of time. What compute option would you use to process images?

A. App Engine Standard

B. App Engine Flexible

C. Cloud Functions

D. Cloud Run



**Answers:**

C. Cloud Functions is used to respond to events in Google Cloud, including uploading of files in Cloud Storage. Since there are periods when no images are uploaded, there is no need to have an application running continuously and checking for new image uploads.



#### 21. The CFO of your company wants to improve an existing data warehouse by migrating it to Google Cloud. They want to minimize operational overhead while ensuring existing SQL tools can be used with the migrated data warehouse. What Google Cloud service would you recommend?

A. Bigtable

B. BigQuery

C. Cloud SQL

D. Cloud Spanner



**Answers:**

B. BigQuery is a managed, petabyte scale data warehouse, which uses SQL. Bigtable does not support SQL. Cloud SQL and Cloud Spanner support SQL but are designed for transaction processing, not analytical applications like data warehouses.



#### 22. As a consultant to a mid-sized retailer, you have been asked to help choose a managed database platform for the company's inventory management application. The retailer's market is limited to the Northeast United States. What service would you recommend?

A. Bigtable

B. Cloud SQL

C. Cloud Spanner

D. Cloud Dataproc



**Answers:**

B. Cloud SQL is a managed relational database service suitable for regionally used applications. Cloud Spanner is also a managed relational database but it is designed for multi-region and global applications. BigQuery is not used for transaction processing systems. Cloud Dataproc is a managed Spark/Hadoop service, not a relational database.



#### 23. A startup has created an IoT application that analyzes data from sensors deployed on vehicles. The application depends on a database that can write large volumes of data at low latency.  The startup has used HBase in the past but wants to migrate to a managed database service. What service would you recommend?

A. Bigtable

B. BigQuery

C. Cloud Spanner

D. Cloud Dataproc



**Answers:**

A. Bigtable is a wide column database with low latency writes that is well suited for IoT data storage. BigQuery is a data warehouse service. Cloud Dataproc is a managed Spark/Hadoop service. Cloud Spanner is a global-scale relational database designed for transaction processing.



#### 24. A startup is implementing an IoT application that will ingest data at high speeds. The architect for the startup has decided that data should be ingested in a queue that can store the data until the processing application is able to process it. The architect also wants to use a managed service in Google Cloud. What service would you recommend?

A. Bigtable

B. Cloud Pub/Sub

C. Cloud Dataflow

D. Cloud Dataproc



**Answers:**

B. Cloud Pub/Sub is a queuing service that is used to ingest data and store it until it can be processed. Bigtable is a NoSQL database, not a queueing service. Cloud Dataflow is a stream and batch processing service, not a queueing service. Cloud Dataproc is a managed Spark/Hadoop service.



#### 25. Your company has an on-premises Spark cluster that is to be migrated to Google Cloud. The CFO wants to minimize operational overhead. What Google Cloud service would you recommend?

A. Bigtable

B. Cloud Dataflow

C. Cloud Pub/Sub

D. Cloud Dataproc



**Answers:**

D. Cloud Dataproc is a managed Spark/Hadoop service that can be used to migrate Hadoop clusters GCP.



#### 26. A photographer wants to share images they have stored in a Cloud Storage bucket called free-photos-on-gcp. What command would you use to allow all users to read these files?

A. gcloud iam ch allUsers:Viewer gs://free-photos-on-gcp

B. gcloud ch allUsers:objectViewer gs://free-photos-on-gcp

C. gsutil iam ch allUsers:objectViewer gs://free-photos-on-gcp

D. gsutil ch allUsers:Viewer gs://free-photos-on-gcp



**Answers:**

C. The correct command is gsutil iam ch allUsers:objectViewer gs://free-photos-on-gcp. Gsutil is used with Cloud Storage, not gcloud. The term objectViewer is the correct way to grant read access to objects in a bucket.



#### 27. The contents of a Cloud Storage bucket called free-photos-gcp are currently stored in a standard storage class bucket. You want to change the storage class to nearline. What command would you use?

A. gcloud storage objects update gs://free-photos-gcp --storage-class=Nearline

B. gsutil migrate -s nearline gs://free-photos-gcp

C. gsutil rewrite -from multiregional --to nearline gs://free-photos-gcp

D. gsutil migrate --from multiregional --to nearline gs://free-photos-gcp



**Answers:**

A. The correct command for changing the storage class is gcloud storage objects update with the target storage class and bucket specified.



#### 28. A Cloud Storage user wants to rename several files in a bucket. What command should they use?

A. gsutil mv

B. gsutil rename

C. gsutil cp

D. gsutil rn



**Answers:**

A. To rename a file in cloud storage, use the move command gsutil mv.



#### 29. During an audit, auditors determined that there are insufficient access controls on Cloud Storage buckets. The auditors recommend you use uniform bucket-level access. After applying uniform bucket-level access some users that had access to objects in buckets no longer have access. What could be the cause?

A. Users do not have IAM permissions that allow them access to objects in buckets. Prior to setting uniform bucket-level access, those users had access through ACLs.

B. Applying uniform bucket-level access removes all access privileges. No user will have access until permissions are reset.

C. Users do not have permissions through ACLs that allow them access to objects in buckets. Prior to setting uniform bucket-level access, those users had access through IAM.

D. ACLs are removed when uniform bucket-level access is applied. ACLs must be recreated.



**Answers:**

A. Access is granted to Cloud Storage objects using IAM or access control lists (ACLs). When uniform bucket-level access is applied, users only have access through IAM roles and permissions. A users that could access objects before uniform bucket-level access is applied but not after must have had access through ACLs.



#### 30. You are using HTTP(S) Load Balancing for a Web application that has several services. Depending on the URL specified by a user, requests are routed to different backend services. What would you use to specify how those requests should be routed?

A. URL maps

B. Routes

C. Firewall rules

D. Traces



**Answers:**

A. URL maps specify direct requests to particular services. Routes are used to specify paths to destination IP addresses outside a subnet. Firewall rules control the flow of traffic on a network. Traces are used to understand performance characteristics of services in a distributed system.



#### 31. You want to load balance an application that receives traffic from other resources in the same VPC. All traffic is TCP with IPv4 addresses. What load balancer would you recommend?

A. SSL Proxy Load Balancing

B. TCP Proxy Load Balancing

C. Internal TCP/UDP Load Balancing

D. Network TCP/UDP Load Balancing



**Answers:**

C. Internal TCP/UDP Load Balancing is used for internal traffic, that is not from the internet. SSL Proxy, TCP Proxy, and Network TCP/UDP load balancing are used with external traffic.



#### 32. You want to run a Kubernetes cluster for a high-availability set of applications using Google Kubernetes Engine (GKE). What type of cluster would you use?

A. Single zone

B. Multi-zonal

C. Regional

D. Dedicated cluster



**Answers:**

C. Regional clusters have replicas of the control plane while single zone and multi-zonal clusters have only one control plane. There is no such thing as a dedicated cluster in GKE.



#### 33. You have created a Kubernetes Engine cluster that will run machine learning training processes and machine learning prediction processes. The training processes require more CPU and memory than the prediction processes. How would you configure the cluster to support this?

A. Use multiple pods with some configured for more CPU and memory.

B. Use two node pools, one configured with more CPU and memory than the other.

C. Increase the number of replica sets for the machine learning training process.

D. Increase the number of deployments for the machine learning training process.



**Answers:**

B. Node pools are used to configure resources for particular workloads. All nodes in a node pool are configured the same. Replica sets and deployments do not control the number of CPUs or amount of memory.



#### 34. You will be creating a GKE cluster and want to use Cloud Operations for GKE instead of legacy monitoring and logging. If you create the cluster using a gcloud container clusters create command, what parameter would you specify to explicitly enable Cloud Operations for GKE?

A. --logging and --monitoring

B. --enable-cloud-operations

C. --enable-gke-monitor

D. --disable-legacy-monitoring



**Answers:**

A. The correct way to enable Cloud Operations for GKE is to use the parameters --logging and --monitoring.



#### 35. Kubernetes Engine collects application logs by default when the log data is written where?

A. STDOUT

B. STDERR

C. SYSLOG

D. SYSERR



**Answers:**

A, B. Kubernete Engine collects log data written to standard output (STDOUT) and standard error (STDERR).



#### 36. A data warehouse administrator is trying to load data from Cloud Storage to BigQuery. What permissions will they need?

A. bigquery.tables.create

B. bigquery.tables.list

C. bigquery.tables.updateData

D. bigquery.jobs.create

E. bigquery.jobs.list



**Answers:**

A, C, D. To load data, an identity must have bigquery.tables.create, bigquery.tables.updateData, and bigquery.jobs.create.



#### 37. The CFO of your company feels you are spending too much on BigQuery. You determine that a few long running queries are costing more than they should. You would like to experiment with different ways of writing these queries. You'd like to know the estimated cost of running each query without actually running them. How could you do this?

A. Use the --dry-run option with a bq query command

B. Use the Price Calculator

C. Use the --estimate-cost option with the bq command

D. Use the --estimate-cost with the gcloud command



**Answers:**

A. The correct answer is to use the --dry-run option with the bq select command.



#### 38. You have just created a custom mode network using the command: gcloud compute networks create. You want to eventually deploy instances in multiple regions. What is the next thing you should do?

A. Create subnets in all regions

B. Create subnets in regions where you plan to deploy instances

C. Create firewall rules to control ingress traffic

D. Create a VPN between the custom mode network and other networks in the VPC.



**Answers:**&#x20;

B. After creating a custom mode network, you will need to create subnets in regions where instances will be deployed. You do not have to create subnets in all regions but an instance cannot be deployed to a region without a subnet.



#### 39. A group of developers is creating a multi-tiered application. Each tier is in its own project. The developer would like to work with a common VPC network. What would you use to implement this?

A. Create a VPN between projects

B. Create a shared VPC

C. Create routes between subnets of each project

D. Create firewall rules to allow ingress and egress traffic between each project's subnets.



**Answers:**&#x20;

B. A shared VPC allows projects to share a common VPC network. VPNs are used to link VPCs to on premises networks. Routes and firewall rules are not sufficient for implementing a common VPC.



#### 40. You have created a set of firewall rules to control ingress and egress traffic to a network. Traffic that you intended to allow to leave the network appears to be blocked. What could you do to get information to help you diagnose the problem?

A. Enable firewall rule logging for each of the firewall rules

B. Enable Cloud Monitoring of each firewall rule

C. Enable Cloud Trace of each firewall rule

D. Use Cloud Debugger to debug the firewall rules



**Answers:**

A. Firewall rule logging can be enabled for each firewall rule. Each time the rule is applied to allow or deny traffic, a connection record is created. Connection records can be viewed in Cloud Logging.



#### 41. A client has asked for your advice about building a data transformation pipeline. The pipeline will read data from Cloud Storage and Cloud Spanner, merge data from the two sources, and write the data to a BigQuery data set. The client does not want to manage servers or other infrastructure, if possible. What Google Cloud service would you recommend?

A. Compute Engine

B. Cloud Data Fusion

C. Cloud Dataprep

D. Cloud Build



**Answers:**

B. Cloud Data Fusion is a managed service that is designed for building data transformation pipelines. Compute Engine is not a managed service. Cloud Dataprep is used to prepare data for analytics and machine learning. Cloud Build is a service for creating container images.



#### 42. A group of data scientists needs access to data stored in Cloud Bigtable. You want to follow Google's recommended best practices for security. What role would you assign to the data scientist to allow them to read data from Bigtable?

A. roles/bigtable.admin

B. roles/bigtable.reader

C. roles/bigtable.user

D. roles/bigtable.owner



**Answers:**

B. The role/bigtable.reader gives the data scientist the ability to read data but not write data or modify the database. This follows the Principle of Least Privilege as recommended by Google.



#### 43. You have created a process that will run nightly. The process needs read and write access to two Cloud Storage buckets. You do not want to use your identity to ensure the process has sufficient privileges. How would you ensure the process can read and write to the Cloud Storage buckets?

A. Create a Cloud Identity and grant it a role that provides read and write permissions.

B. Create a service account and grant it a role that provides read and write permission.

C. Create a federated identity and grant it permissions directly to enable read and write access.

D. Create a service account and assign permissions directly to enable read and write access.



**Answers:**

B. Service accounts are used to provide applications and instances with an identity that can have roles that give the identity sufficient permission to execute operations it needs to perform.



#### 44. A large enterprise has created multiple organizations in Google Cloud. They would like to connect the VPC networks across organizations. What should they do?

A. Define firewall rules to allow egress traffic to other VPC networks

B. Implement VPC Network Peering between VPCs

C. Implement a Shared VPC

D. Implement a VPN between VPCs



**Answers:**

B. Since the connected networks are in different organizations, they must use VPC Network Peering. VPC sharing is only available within a single organization. Firewall rule changes may be needed, but that is not sufficient. VPNs are used to connect GCP networks with on premises networks.



#### 45. You are creating a set of virtual machines in Compute Engine. Google Cloud will automatically assign an IP address to each. What type of IP address will be assigned?

A. Regional internal address

B. Global internal address

C. Regional external address

D Global external address



**Answers:**

A. Google Cloud assigns regional internal IP addresses for VM instances, including GKE pods, nodes, and services. They are also used for Internal TCP/UDP Load Balancing and Internal HTTP(S) Load Balancing



#### 46. You want to deploy an application to a Kubernetes Engine cluster using a manifest file called my-app.yaml. What command would you use?

A. kubectl apply -f my-app.yaml

B. gcloud containers deployment apply my-app.yaml

C. kubectl deployment apply my-app.yaml

D. gcloud deployment apply my-app.yaml



**Answers:**

A. The correct answer is to use the "kubectl apply -f" with the name of the deployment file. Deployments are Kubernetes abstractions and are managed using kubectl, not gcloud. The other options are not valid commands.



#### 47. A client of yours wants to deploy a stateless application to a Kubernetes cluster using a deployment. The replication controller is named my-app-rc. The application should scale based on CPU utilization; specifically when CPU utilization exceeds 80%. There should never be fewer than 2 pods or more than 6. What command would you use to implement autoscaling with these parameters?

A. kubectl autoscale deployment my-app-rc --min=2 --max=6 --cpu-percent=80

B. kubectl apply deployment my-app-rc --min=2 --max=6 --cpu-percent=80

C. gcloud containers autoscale rc my-app-rc --min=2 --max=6 --cpu-percent=80

D. gcloud containers apply rc my-app-rc --min=2 --max=6 --cpu-percent=80



**Answers:**

A. The correct command is to use kubectl autoscale deployment specifying the appropriate min, max, and cpu percent. The other options are not valid commands.



#### 48. You have a Cloud Datastore database that you would like to back up. You'd like to issue a command and have it return immediately while the backup runs in the background.  You want the backup file to be stored in a Cloud Storage bucket named my-datastore-backup. What command would you use?

A. gcloud datastore backup gs://my-datastore-backup

B. gcloud datastore export gs://my-datastore-backup --async

C. gsutil datastore export gs://my-datastore-backup --async

D. gcloud datastore export gs://my-datastore-backup



**Answers:**

B. The correct command is gcloud datastore export gs://my-datastore-backup --async. Export, not backup, is the datastore command to save data to a Cloud Storage bucket. Gsutil is used to manage Cloud Storage, not Cloud Datastore.



#### 49. A software development team is using Google Cloud Artifact Registry to manage container images. You have recently joined the team and want to view metadata about existing registries. What command would you use?

A. gcloud artifacts repositories list

B. gcloud reposoitories container list

C. gcloud container metadata list

D. gcloud container list metadata



**Answers:**

A> The correct command is gcloud artifacts repositories list. The other options are not valid commands.



#### 50. Your company is migrating an on premises archive of files to Google Cloud. The archived files are infrequently used but on average about once every 30 days. You would like to minimize the cost of storage. What storage option would you recommend?

A. Nearline Storage

B. Coldline Storage

C. Multi-regional storage

D. Persistent Disks



**Answers:**

A. Nearline Storage is a class of Cloud Storage designed for objects that will be accessed at most once every 30 days. Coldline Storage is suitable for objects accessed at most once per year. Multi-regional storage is best suited for objects that should have low latency access from multiple regions. Persistent disks should not be used for archival storage.

