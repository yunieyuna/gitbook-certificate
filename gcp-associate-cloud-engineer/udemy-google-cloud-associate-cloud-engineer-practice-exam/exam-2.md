# Exam 2

#### 1. A data warehouse administrator is trying to load data from Cloud Storage to BigQuery. What permissions will they need?

A. bigquery.tables.updateData

B. bigquery.jobs.create

C. bigquery.tables.list

D. bigquery.tables.create

E. bigquery.jobs.list



**Explanation**

A, B, D. To load data, an identity must have bigquery.tables.create, bigquery.tables.updateData, and bigquery.jobs.create. bigquery.tables.list is needed to list tables and metadata on tables. For more information, see https://cloud.google.com/bigquery/docs/batch-loading-data and https://cloud.google.com/bigquery/docs/access-control.



#### 2. You want to deploy an application to a Kubernetes Engine cluster using a manifest file called my-app.yaml. What command would you use?

A. kubectl deployment apply my-app.yaml

B. gcloud deployment apply my-app.yaml

C. gcloud containers deployment apply my-app.yaml

D. kubectl apply -f my-app.yaml



**Explanation**

D. The correct answer is to use the "kubectl apply -f" with the name of the deployment file. Deployments are Kubernetes abstractions and are managed using kubectl, not gcloud. The other options are not valid commands. For more information, see https://kubernetes.io/docs/reference/kubectl/overview/.



#### 3. Your company has a complicated billing structure for GCP projects. You would like to set up multiple configurations for use with the command line interface. What command would you use to create those?

A. gcloud config configurations create

B. gcloud config configurations set

C. gcloud configurations create

D. gcloud configurations set



**Explanation**

A. The correct command is gcloud config configurations create. Gcloud configurations crae, gcloud config configurations set, and gcloud configurations set are not valid gcloud commands to create configurations. For more information, see https://cloud.google.com/sdk/gcloud/reference/config/configurations/create.



#### 4. A client of yours wants to deploy a stateless application to Kubernetes cluster. The replication controller is named my-app-rc. The application should scale based on CPU utilization; specifically when CPU utilization exceeds 80%. There should never be fewer than 2 pods or more than 6. What command would you use to implement autoscaling with these parameters?

A. kubectl apply rc my-app-rc --min=2 --max=6 --cpu-percent=80

B. kubectl autoscale rc my-app-rc --min=2 --max=6 --cpu-percent=80

C. gcloud containers autoscale rc my-app-rc --min=2 --max=6 --cpu-percent=80

D. gcloud containers apply rc my-app-rc --min=2 --max=6 --cpu-percent=80



**Explanation**

B. The correct command is to use kubectl autoscale specifying the appropriate min, max, and cpu percent. Specifically: kubectl autoscale rc my-app-rc --min=2 --max=6 --cpu-percent=80. The other options are not valid commands. For more information, see https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/.



#### 5. You have deployed a sole tenant node in Compute Engine. How will this restrict what VMs run on that node.

A. Only one VM will run on that node.

B. Only VMs from the same project will run on the node.

C. Only VMs using the same operating system will run on that node.

D. Only VMs from the same organization will run on that node.



**Explanation**

B. On a sole tenant node, only VMs from the same project will run on that node. They do not need to use the same operating system. Sole tenant nodes are not restricted to a single VM. VMs from the same organization but different projects will not run on the same sole tenant instance. For more information, see https://cloud.google.com/compute/docs/nodes/sole-tenant-nodes.



#### 6. As a consultant to a mid-sized retailer you have been asked to help choose a managed database platform for the company's inventory management application. The retailer's market is limited to the Northeast United States. What service would you recommend?

A. Cloud SQL

B. Bigtable

C. Cloud Dataproc

D. Cloud Spanner



**Explanation**

A. Cloud SQL is a managed relational database service suitable for regionally used applications. Cloud Spanner is also a managed relational database but it is designed for multi-region and global applications. BigQuery is not used for transaction processing systems. Cloud Dataproc is a managed Spark/Hadoop service, not a relational database. For more information, see https://cloud.google.com/sql/docs.



#### 7. The CFO of your company wants to improve an existing data warehouse by migrating it to Google Cloud. They want to minimize operational overhead while ensuring existing SQL tools can be used with the migrated data warehouse. What GCP service would you recommend?

A. BigQuery

B. Cloud SQL

C. Bigtable

D. Cloud Spanner



**Explanation**

A. BigQuery is a managed, petabyte scale data warehouse, which uses SQL. Bigtable does not support SQL. Cloud SQL and Cloud Spanner support SQL but are designed for transaction processing, not analytical applications like data warehouses. For more information, see https://cloud.google.com/bigquery/docs/how-to.



#### 8. A developer is trying to upload files from their local device to a Compute Engine VM using the gcloud scp command. The copy command is failing. What would you check to try to correct the problem?

A. Grant the identity compute.admin permission

B. Add the identity of the developer to the administrator group for the VM.

C. Grant the identity the roles/compute.admin role

D. Ensure firewall rules allow traffic to port 22 to allow SSH connections.



**Explanation**

D. To copy files to a VM, a firewall rule must be in place to allow traffic on port 22, the default SSH port. Administrator privileges are not needed to upload a file so the other three options are not correct. For more information, see https://cloud.google.com/compute/docs/instances/transfer-files.



#### 9. A large enterprise has created multiple organizations in GCP. They would like to connect the VPC networks across organizations. What should they do?

A. Implement a Shared VPC

B. Implement a VPN between VPCs

C. Define firewall rules to allow egress traffic to other VPC networks

D. Implement VPC Network Peering between VPCs



**Explanation**

D. Since the connected networks are in different organizations, they must use VPC Network Peering. VPC sharing is only available within a single organization. Firewall rule changes may be needed, but that is not sufficient. VPNs are used to connect GCP networks with on premises networks. For more information, see https://cloud.google.com/vpc/docs/vpc-peering.



#### 10. You have just created a custom mode network using the command: gcloud compute networks create. You want to eventually deploy instances in multiple regions. What is the next thing you should do?

A. Create firewall rules to load balance traffic

B. Create a VPN between the custom model network and other networks in the VPC.

C. Create subnets in all regions

D. Create subnets in regions where you plan to deploy instances(Correct)



**Explanation**

D. After creating a custom mode network, you will need to create subnets in regions where instances will be deployed. You do not have to create subnets in all regions but an instance cannot be deployed to a region without a subnet. Firewalls are used to control the ingress and egress of data, they are not used to load balance. VPNs are used to provide connectivity between Google Cloud and outside networks, such as an on premises network. For more information, see https://cloud.google.com/vpc/docs/using-vpc and https://cloud.google.com/sdk/gcloud/reference/compute/networks/subnets/create.



#### 11. An auditor is reviewing your GCP use. They have asked for access to any audit logs available in GCP. What audit logs are available for each project, folder, and organization?

A. Policy Access

B. System Event

C. Performance Metrics

D. Data Access

E. Admin Activity

F. User Login



**Explanation**

B, D, E. Cloud Audit Logs maintain three audit logs: Admin Activity logs, Data Access logs, and System Event logs. There is no such thing as a Policy Access log, a User Login log, or a Performance Metric log in GCP Audit Logs. For more information, see https://cloud.google.com/logging/docs/audit.



#### 12. Your organization has created multiple folders, one for each department. In each folder, departments have one or more projects. What would you expect resources within the folder to share?

A. IAM policies

B. Service accounts

C. Permissions

D. IAM roles



**Explanation**

A. Folders are used to group resources that share common IAM policies. Service accounts are specific to a set of operating requirements within a project. Permissions are associated with roles but not directly with folders. IAM roles are granted to identities, not folders. For more information, see https://cloud.google.com/resource-manager/docs/creating-managing-folders.



#### 13. A startup has created an IoT application that analyzes data from sensors deployed on vehicles. The application depends on a database that can write large volumes of data at low latency. The startup has used HBase in the past but want to migrate to a managed database service. What service would you recommend?

A. Cloud Spanner

B. Bigtable

C. Cloud Dataproc

D. BigQuery



**Explanation**

B. Bigtable is a wide column database with low latency writes that is well suited for IoT data storage. BigQuery is a data warehouse service. Cloud Dataproc is a managed Spark/Hadoop service. Cloud Spanner is a global-scale relational database designed for transaction processing. For more information, see https://cloud.google.com/bigtable/docs/schema-design and https://cloud.google.com/bigtable/docs/schema-design-steps.



#### 14. A software development team is using Google Container Registry to manage container images. You have recently joined the team and want to view metadata about existing container images. What command would you use?

A. gcloud images container list

B. gcloud container list metadata

C. gcloud container images list

D. gcloud container metadata list



**Explanation**

C. The correct command is gcloud container images list. The other options are not valid gcloud commands. For more information, see https://cloud.google.com/sdk/gcloud/reference/container/images/list.



#### 15. The contents of the a Cloud Storage bucket called free-photos-gcp are currently stored in multiregional storage class. You want to change the storage class to nearline. What command would you use?

A. gsutil migrate -s nearline gs://free-photos-gcp

B. gsutil migrate --from multiregional --to nearline gs://free-photos-gcp

C. gsutil rewrite -s nearline gs://free-photos-gcp

D. gsutil rewrite -from multiregional --to nearline gs://free-photos-gcp



**Explanation**

C. The correct command for changing the storage class is gsutil rewrite with the target storage class and bucket specified. Gsutil migrate is not a valid command. There is no need to specify the parameters -from or -to. For more information, see https://cloud.google.com/storage/docs/gsutil/commands/rewrite.



#### 16. During an audit, auditors determined that there are insufficient access controls on Cloud Storage buckets. The auditors recommend you use uniform bucket-level access. After applying uniform bucket-level access some users that had access to objects in buckets no longer have access. What could be the cause?

A. Applying uniform bucket-level access removes all access privileges. No user will have access until permissions are reset.

B. ACLs are removed when uniform bucket-level access is applied. ACLs must be recreated.

C. Users do not have permissions through ACLs that allow them access to objects in buckets. Prior to setting uniform bucket-level access, those users had access through IAM.

D. Users do not have IAM permissions that allow them access to objects in buckets. Prior to setting uniform bucket-level access, those users had access through ACLs.



**Explanation**

D. Access is granted to Cloud Storage objects using IAM or access control lists (ACLs). When uniform bucket-level access is applied, users only have access through IAM roles and permissions. A users that could access objects before uniform bucket-level access is applied but not after must have had access through ACLs. For more information, see https://cloud.google.com/storage/docs/uniform-bucket-level-access.



#### 17. A client has asked for your advice about building a data transformation pipeline. The pipeline will read data from Cloud Storage and Cloud Spanner, merge data from the two sources and write the data to a BigQuery data set. The client does not want to manage servers or other infrastructure, if possible. What GCP service would you recommend?

A. Cloud Dataprep

B. Cloud Data Fusion

C. Cloud Build

D. Compute Engine



**Explanation**

B. Cloud Data Fusion is a managed service that is designed for building data transformation pipelines. Compute Engine is not a managed service. Cloud Dataprep is used to prepare data for analytics and machine learning. Cloud Build is a service for creating container images. For more information, see https://cloud.google.com/data-fusion/docs/how-to.



#### 18. A startup has an app that allows users to upload images to Cloud Storage. The images should be analyzed as soon as possible once they are loaded. Processing takes approximately 1 second for each image. There are periods when no images are uploaded and other times when many images are upload in short periods of time. What compute option would you use to process images?

A. Kubernetes Engine

B. Cloud Functions

C. App Engine Flexible

D. Compute Engine



**Explanation**

B. Cloud Functions is used to respond to events in GCP, including uploading of files in Cloud Storage. Processing can finish within the time limits Cloud Functions must run. Since there are periods when no images are uploaded, there is no need to have an application running continuously and checking for new image uploads so App Engine Flexible, Cloud Engine, and Kubernetes Engine are more than required. For more information, see https://cloud.google.com/functions/docs/how-to.



#### 19. Your department runs a legacy application on an on premises cluster. The nodes in the cluster are heterogeneous. You want to migrate this cluster to Google Cloud. What Compute Engine resource would you use?

A. Unmanaged instance group

B. Managed instance groups (MIGs)

C. Network load balancer

D. Autoscaler



**Explanation**

A. Heterogeneous clusters can be run on unmanaged instance groups but not managed instance groups. Network load balancer is used to distribute workload in a cluster but it is not an instance group itself. Autoscaler adds and removes nodes in a managed instance group as needed. For more information, see https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-unmanaged-instances.



#### 20. You want to load balance an application that receives traffic from other resources in the same VPC. All traffic is TCP with IPv4 addresses. What load balancer would you recommend?

A. SSL Proxy Load Balancing

B. Network TCP/UDP Load Balancing

C. Internal TCP/UDP Load Balancing

D. TCP Proxy Load Balancing



**Explanation**

C. Internal TCP/UDP Load Balancing is used for internal traffic, that is not from the internet. SSL Proxy, TCP Proxy, and Network TCP/UDP load balancing are used with external traffic. For more information, see https://cloud.google.com/load-balancing/docs/choosing-load-balancer.



#### 21. You want to use Cloud Identity to create identities. You have received a verification record for your domain. Where would you add that record?

A. In the domain's DNS setting

B. In the billing account for your organization

C. In IAM settings for each identity

D. In the metadata of each resource created in your organization



**Explanation**

A. Cloud Identity provides domain verification records, which are added to DNS settings for the domain. IAM is used to control access granted to identities, it is not a place to manage domains. The billing account is used for payment tracking, it is not a place to manage domains. Resources do have metadata, but that metadata is not used to manage domains. For more information on verifying domains, see https://cloud.google.com/identity/docs/verify-domain.



#### 22. An application running in Compute Engine sometimes gets spikes in load. You want to add instances automatically when load increases significantly and plan to use managed instance groups. What would you need to create in order to automatically scale the cluster?

A. Persistent Disk

B. Instance template

C. Load balancer

D. Snapshot



**Explanation**

B. An instance template is needed to enable Compute Engine to automatically add instances to a managed instance group. Snapshots are not required to add instances to a managed instance group. Persistent disks are not needed to control the addition of nodes to a managed instance group. Load balancers are used with managed instance groups but are not the thing that automatically adds nodes to the managed instance group. For more information, see https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances.



#### 23. You have created a process that will run nightly. The process needs read and write access to two Cloud Storage buckets. You do not want to use your identity to ensure the process has sufficient privileges. How would you ensure the process can read and write to the Cloud Storage buckets?

A. Create a service account and assign permissions directly to enable read and write access.

B. Create a federated identity and grant it permissions directly to enable read and write access.

C. Create a service account and grant it a role that provides read and write permission.

D. Create a Cloud Identity and grant it a role that provides read and write permissions.



**Explanation**

C. Service accounts are used to provide applications and instances with an identity that can have roles that give the identity sufficient permission to execute operations it needs to perform.



#### 24. A manager in your company is having trouble tracking the use and cost of resources across several projects. In particular, they do not know which resources are created by different teams they manage. What would you suggest the manager use to help better understand which resources are used by which team?

A. Trace logs

B. IAM policies

C. Labels

D. Audit logs



**Explanation**

C. Labels are key-value pairs attached to resources and used to manage them. The manager could use a key-value pair with the key 'team-name' and the value the name of the team that created the resource. Audit logs do not necessarily have the names of teams that own a resource. Traces are used for performance monitoring and analysis. IAM policies are used to control access to resources, not to track which team created them. For more information, see https://cloud.google.com/resource-manager/docs/creating-managing-labels.



#### 25. A photographer wants to share images they have stored in a Cloud Storage bucket called free-photos-on-gcp. What command would you use to allow all users to read these files?

A. gsutil ch allUsers:Viewer gs://free-photos-on-gcp

B. gcloud ch allUsers:objectViewer gs://free-photos-on-gcp

C. gsutil iam ch allUsers:objectViewer gs://free-photos-on-gcp

D. gcloud iam ch allUsers:Viewer gs://free-photos-on-gcp



**Explanation**

C. The correct command is gsutil iam ch allUsers:objectViewer gs://free-photos-on-gcp. Gsutil is used with Cloud Storage, not gcloud so the gcloud ch option is incorrect. The term objectViewer is the correct way to grant read access to objects in a bucket. For more information, see https://cloud.google.com/storage/docs/gsutil/commands/iam.



#### 26. A group of data scientists need access to data stored in Cloud Bigtable. You want to follow Google recommended best practices for security. What role would you assign to the data scientist to allow them to read data from Bigtable?

A. roles/bigtable.admin

B. roles/bigtable.reader

C. roles/bigtable.owner

D. roles/bigtable.user



**Explanation**

B. The role/bigtable.reader gives the data scientist the ability to read data but not write data or modify the database. This follows the Principle of Least Privilege as recommended by Google. Roles/bigtable.admin gives permissions to administer all instances in a project, which is not needed by a data scientist. Roles/bigtable.user provides read and write permissions but data scientist do not need read permission. There is no predefined role called roles/bigtable.owner. For more information, see https://cloud.google.com/bigtable/docs/access-control.



#### 27. A client of yours has a Python 3 application that usually has very little load but sometimes experiences sudden and extreme spikes in traffic. They want to run it in GCP but they want to keep costs as low as possible. They also want to minimize management overhead. What service would you recommend?

A. Compute Engine

B. Cloud Functions

C. App Engine

D. Kubernetes Engine



**Explanation**

C. App Engine is designed for applications written in supported languages, including Python 3, that need to run at low cost, and need to scale in response to rapid increases in load. App Engine is a managed service and as such minimizes operational overhead . Compute Engine and Kubernetes Engine both require more management overhead. Cloud Functions are used to respond to events in GCP, not to execute a continually running application. For more information, see https://cloud.google.com/appengine/docs/standard.



#### 28. You have a Cloud Datastore database that you would like to backup. You'd like to issue a command and have it return immediately while the backup runs in the background. You want the backup file to be stored in a Cloud Storage bucket named my-datastore-backup. What command would you use?

A. gsutil datastore export gs://my-datastore-backup --async

B. gcloud datastore backup gs://my-datastore-backup

C. gcloud datastore export gs://my-datastore-backup

D. gcloud datastore export gs://my-datastore-backup --async



**Explanation**

D. The correct command is gcloud datastore export gs://my-datastore-backup --async. Export, not backup, is the datastore command to save data to a Cloud Storage bucket. Gsutil is used to manage Cloud Storage, not Cloud Datastore. For more information, see https://cloud.google.com/datastore/docs/export-import-entities.



#### 29. Kubernetes Engine collects application logs by default when the log data is written where?

A. SYSLOG

B. STDOUT

C. SYSERR

D. STDERR



**Explanation**

B, D. Kubernetes Engine collects log data written to standard output (STDOUT) and standard error (STDERR). For more information, see https://cloud.google.com/blog/products/management-tools/using-logging-your-apps-running-kubernetes-engine.



#### 30. You have created a set of firewall rules to control ingress and egress traffic to a network. Traffic that you intended to allow to leave the network appears to be blocked. What could you do to get information to help you diagnose the problem?

A. Enable firewall rule logging for each of the firewall rules

B. Enable Cloud Monitoring of each firewall rule

C. Enable Cloud Trace of each firewall rule

D. Use Cloud Debugger to debug the firewall rules



**Explanation**

A. Firewall rule logging can be enabled for each firewall rule. Each time the rule is applied to allow or deny traffic, a connection record is created. Connection records can be viewed in Cloud Logging. Cloud Monitoring is used for collecting and view metrics on resource performance. Cloud Trace is used to understand performance in distributed systems. Cloud Debugger is used by developers to identify and correct errors in code. For more information, see https://cloud.google.com/vpc/docs/firewall-rules-logging.



#### 31. A new team member has just created a new project in Google Cloud. What role is automatically granted to them when they create the project?

A. roles/browser

B. roles/editor

C. roles/viewer

D. roles/owner



**Explanation**

D. When you create a project, you are automatically granted the roles/owner role. The owner role includes permissions granted by roles/editor, roles/viewer, and roles/browser. For more information, see https://cloud.google.com/resource-manager/docs/access-control-proj.



#### 32. You have created a target pool with instances in two zones which are in the same region. The target pool is not functioning correctly. What could be the cause of the problem?

A. The target pool nodes are configured with different memory specifications

B. The target pool is not sending logs to Cloud Logging.

C. The target pool is missing a health check.

D. The target pool is not sending metrics to Cloud Monitoring.



**Explanation**

C. Target pools must have a health check to function properly. Nodes can be in different zones but must be in the same region. Cloud Monitoring and Cloud Logging are useful but they are not required for the target pool to function properly. Nodes in a pool have the same configuration. For more information, see https://cloud.google.com/load-balancing/docs/target-pools.



#### 33. You have created a Kubernetes Engine cluster that will run machine learning training processes and machine learning prediction processes. The training processes require more CPU and memory than the prediction processes. How would you configure the cluster to support this?

A. Increase the number of deployments for the machine learning training process.

B. Use two node pools, one configured with more CPU and memory than the other.

C. Use multiple pods with some configured for more CPU and memory.

D. Increase the number of replica sets for the machine learning training process.

**Explanation**

B. Node pools are used to configure resources for particular workloads. All nodes in a node pool are configured the same. Replica sets and deployments do not control the number of CPUs or amount of memory.



#### 34. As a developer using GCP, you will need to set up a local development environment. You will want to authorize the use of gcloud commands to access resources. What commands could you use to authorize access?

A. gcloud auth login

B. gcloud login

C. gcloud config login

D. gcloud init



**Explanation**

A, D. Gcloud init will authorize access and perform other common setup steps. Gcloud auth login will authorize access only. Gcloud login and gcloud config login are not valid commands. For more information, see https://cloud.google.com/sdk/docs/initializing.



#### 35. You want to run a Kubernetes cluster for a high availability set of applications. What type of cluster would you use?

A. Multi-regional

B. Multi-zonal

C. Regional

D. Single zone



**Explanation**

C. Regional clusters have replicas of the control plane while single zone and multi-zonal clusters have only one control plane. There is no such thing as multi-regional cluster. For more information, see https://cloud.google.com/blog/products/containers-kubernetes/best-practices-for-creating-a-highly-available-gke-cluster.



#### 36. You will be creating a GKE cluster and want to use Cloud Operations for GKE instead of legacy monitoring and logging. If you create the cluster using a gcloud container clusters create command, what parameter would you specify to explicitly enable Cloud Operations for GKE?

A. --enable-gke-monitor

B. --disable-legacy-monitoring

C. --enable-cloud-operations

D. --enable-stackdriver-kubernetes



**Explanation**

D. The correct way to enable Cloud Operations for GKE is to use the parameter --enable-stackdriver-kubernetes. The other options are not valid parameter names. For more information, see https://cloud.google.com/sdk/gcloud/reference/container/clusters/create.



#### 37. You are creating a set of virtual machines in Compute Engine. GCP will automatically assign an IP address to each. What type of IP address will be assigned?

A. Global external address

B. Regional internal address

C. Global internal address

D. Regional external address



**Explanation**

B. GCP assigns regional internal IP addresses for VM instances, including GKE pods, nodes, and services. They are also used for Internal TCP/UDP Load Balancing and Internal HTTP(S) Load Balancing. For more information, see https://cloud.google.com/compute/docs/ip-addresses.



#### 38. A Cloud Storage user wants to rename several files in a bucket. What command should they use?

A. gsutil cp

B. gsutil rename

C. gsutil rn

D. gsutil mv



**Explanation**

D. To rename a file in cloud storage, use the move command gsutil mv. Gsutil cp will copy files, not rename them. Gsutil rewrite and gsutil rn are not a valid command. For more information, see https://cloud.google.com/storage/docs/gsutil/commands/mv.



#### 39. You will be running an application that requires high levels of security. You want to ensure the application does not run on a server that has been compromised by a rootkit or other kernel-level malware. What kind of virtual machine would you use?

A. Preemptible VM

B. Hardened VM

C. GPU-enabled VM

D. Shielded VM



**Explanation**

D. Shielded VMs are hardened virtual machines that use Secure Boot, virtual trusted platform module enabled Measured Boot, and integrity monitoring. Preemptible VMs can be taken back by Google at any time but cost significantly less than standard prices. Hardened VM is not a valid option in Compute Engine. GPU-enabled VMs can improve the performance of compute intensive applications, such as training machine learning models. For more information, see https://cloud.google.com/security/shielded-cloud/shielded-vm.



#### 40. Your organization has created multiple projects in several folders. You have been assigned to manage them and want to get descriptive information about each project. What command would you use to get metadata about a project?

A. gcloud projects describe \<PROJECT\_ID>

B. gcloud describe projects \<PROJECT\_NAME>

C. gcloud describe projects \<PROJECT\_ID>

D. gcloud projects describe \<PROJECT\_NAME>



**Explanation**

A. The correct command is 'gcloud projects describe \<PROJECT\_ID'>. 'gcloud projects describe \<PROJECT\_NAME>' is incorrect because PROJECT\_NAME is not used in this command. 'gcloud describe projects' is wrong because 'describe' and 'projects' are in the wrong order in the command. 'gcloud describe project \<PROJECT\_NAME>' is incorrect because it uses PROJECT\_NAME instead of PROJECT\_ID. For more information, see https://cloud.google.com/sdk/gcloud/reference/projects/describe.



#### 41. To avoid potentially violating a regulation, your company has determined that it will only use GCP resources in North America. How would you ensure no resources are created outside of North America?

A. Create a policy at the folder level of the resource hierarchy that includes a constraint using a Resource Location Restriction.

B. Create a data lifecycle management policy that prevents data from being saved outside of North America.

C. Create a policy at the organization level of the resource hierarchy that includes a constraint using a Resource Location Restriction.

D. Create an Cloud Audit policy that prevents users from creating resources outside of North America.



**Explanation**

C. Constraints are the standard way to restrict where resources can be created and applying policies with constraints will enforce those constraints for all resources in the organization. If the policy were applied at the folder level, it would have to be applied for all folders and that is not as efficient as applying at the organization level. There is no such thing as a Cloud Audit policy. For more information, see https://cloud.google.com/resource-manager/docs/organization-policy/defining-locations.



#### 42. Your company is migrating an on premises archive of files to Google Cloud. The archived files are infrequently used but on average about once every 30 days. You would like to minimize the cost of storage. What storage option would you recommend?

A. Nearline Storage

B. Coldline Storage

C. Multi-regional storage

D. Persistent Disks



**Explanation**

A. Nearline Storage is a class of Cloud Storage designed for objects that will be accessed at most once every 30 days. Coldline Storage is suitable for objects accessed at most once per year. Multi-regional storage is best suited for objects that should have low latency access from multiple regions. Persistent disks should not be used for archival storage. For more information, see https://cloud.google.com/storage/docs/storage-classes.



#### 43. A group of developers are creating a multi-tiered application. Each tier is in its own project. The developer would like to work with a common VPC network. What would you use to implement this?

A. Create a shared VPC

B. Create a VPN between projects

C. Create firewall rules to load balance traffic between each project's subnets.

D. Create routes between subnets of each project



**Explanation**

A. A shared VPC allows projects to share a common VPC network. VPNs are used to link VPCs to on premises networks. Routes and firewall rules are not sufficient for implementing a common VPC. Firewall rules are not used to load balance, they are used to control the ingress and egress of traffic on a network. For more information, see https://cloud.google.com/vpc/docs/shared-vpc and https://cloud.google.com/composer/docs/how-to/managing/configuring-shared-vpc.



#### 44. A startup is implementing an IoT application that will ingest data at high speeds. The architect for the startup has decided that data should be ingested in a queue that can store the data until the processing application is able to process it. The architect also wants to use a managed service in Google Cloud. What service would you recommend?

A. Cloud Pub/Sub

B. Bigtable

C. Cloud Dataproc

D. Cloud Dataflow



**Explanation**

A. Cloud Pub/Sub is a queuing service that is used to ingest data and store it until it can be processed. Bigtable is a NoSQL database, not a queueing service. Cloud Dataflow is a stream and batch processing service, not a queueing service. Cloud Dataproc is a managed Spark/Hadoop service. For more information, see https://cloud.google.com/pubsub/docs/overview.



#### 45. Your company has an on premises Hadoop cluster that is to be migrated to Google Cloud. The CFO wants to minimize operational overhead. What GCP service would you recommend?

A. Bigtable

B. Cloud Pub/Sub

C. Cloud Dataflow

D. Cloud Dataproc



**Explanation**

D. Cloud Dataproc is a managed Spark/Hadoop service that can be used to migrate Hadoop clusters GCP. Cloud Pub/Sub is a queuing service that is used to ingest data and store it until it can be processed. Bigtable is a NoSQL database, not a queueing service. Cloud Dataflow is a stream and batch processing service, not a queueing service. For more information, see https://cloud.google.com/dataproc/docs/how-to.



#### 46. As a consultant to a new GCP customer, you are asked to help set up billing accounts. What permission must an identity have in order to create a billing account?

A. billing.create

B. roles/billing.accounts.create

C. roles/billing.create

D. billing.accounts.create



**Explanation**

D. billing.accounts.create is the permission needed to create a billing account. billing.create is not a valid permission. Roles are sets of permissions but they are not permissions themselves so roles/billing.create and roles/billing.accounts.create are not correct answers. For more information, see https://cloud.google.com/billing/docs/how-to/manage-billing-account.



#### 47. You want to clone a persistent disk. What characteristics of the source and cloned disk must be the same?

A. disk type

B. Size

C. Region

D. Zone



**Explanation**

A, C, D. The source and cloned disk must be in the same zone and region and must be of the same type. The size of the clone must be at least the size of the source disk but does not need to be the same. For more information, see https://cloud.google.com/compute/docs/disks/create-snapshots.



#### 48. You are using HTTP(S) Load Balancing for a Web application that has several services. Depending on the URL specified by a user, requests are routed to different backend services. What would you use to specify how those request should be routed?

A. Firewall rules

B. Routes

C. URL maps

D. Traces



**Explanation**

C. URL maps specify direct requests to particular services. Routes are used to specify paths to destination IP addresses outside a subnet. Firewall rules control the flow of traffic on a network. Traces are used to understand performance characteristics of services in a distributed system. For more information, see https://cloud.google.com/load-balancing/docs/url-map.



#### 49. The CFO of you company feels you are spending too much on BigQuery. You determine that a few long running queries are costing more than they should. You would like to experiment with different ways of writing these queries. You'd like to know the estimated cost of running each query without actually running them. How could you do this?

A. Use the --estimate-cost with the gcloud command

B. Use the --estimate-cost option with the bq command

C. Use the --dry-run option with a bq query command

D. Use the Pricing Calculator



**Explanation**

C. The correct answer is to use the --dry-run option with the bq select command. The Pricing Calculator can give you an estimate of aggregate costs based on storage and amount of data queried but it does not provide estimates of a the cost of running a specific query. There is no --estimate-cost option with either the bq or gcloud command. For more information, see https://cloud.google.com/bigquery/docs/estimate-costs.



#### 50. You have a set of snapshots that you keep as backups of several persistent disks. You want to know the source disk for each snapshot. What command would you use to get that information?

A. gcloud compute snapshots describe

B. gcloud snapshots describe

C. gcloud compute snapshots list

D. gcloud compute disk describe



**Explanation**

A. The correct command is gcloud compute snapshots describe which shows information about the snapshot, including source disk, creation time, and size. The other options are not valid gcloud commands. For more information, see https://cloud.google.com/sdk/gcloud/reference/compute/snapshots/describe.

