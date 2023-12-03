# Assessment Test

### 1. Instance templates are used to create a group of identical VMs. The instance templates include:

A. Machine type, boot disk image or container image, zone, and labels&#x20;

B. Cloud Storage bucket definitions

C. A load balancer description

D. App Engine configuration file



Answers:&#x20;

A. Machine type, boot disk image or container image, zone, and labels are all configuration parameters or attributes of a VM and therefore would be included in an instance group configuration that creates those VMs.



### 2. The command-line command to create a Cloud Storage bucket is:

A. gcloud mb

B. gsutil mb

C. gcloud mkbucket&#x20;

D. gsutil mkbucket



Answers:&#x20;

B. gsutil is the command line for accessing and manipulating Cloud Storage from the command line. mb is the specific command for creating, or making, a bucket.



### 3. Your company has an object management policy that requires that objects stored in Cloud Storage be migrated from regional storage to nearline storage 90 days after the object is created. The most efficient way to do this is to:

1. Create a cloud function to copy objects from regional storage to nearline storage.
2. Set the MigrateObjectAfter property on the stored object to 90 days.
3. Copy the object to persistent storage attached to a VM and then copy the object to a bucket created on nearline storage.
4. Create a lifecycle management configuration policy specifying an age of 90 days and SetStorageClass as nearline.



Answers:&#x20;

D. The lifecycle configuration policy allows administrators to specify criteria for migrating data to other storage systems without having to concern themselves with running jobs to actually execute the necessary steps. The other options are inefficient or do not exist.



### 4. An education client maintains a site where users can upload videos, and your client needs to assure redundancy for the files; therefore, you have created two buckets for Cloud Storage. Which command do you use to synchronize the contents of the two buckets?

A. gsutil rsync&#x20;

B. gcloud cp sync&#x20;

C. gcloud rsync&#x20;

D. gsutil cp sync



Answers:&#x20;

A. gsutil is the command-line tool for working with Cloud Storage. rsync is the specific command in gsutil for synchronizing buckets.



### 5. VPCs are resources.&#x20;

A. Regional

B. Zonal&#x20;

C. Global&#x20;

D. Subnet



Answers:&#x20;

C. Google operates a global network, and VPCs are resources that can span that global network.



### 6. A remote component in your network has failed, which results in a transient network error. When you submit a gsutil command, it fails because of a transient error. By default, the command will:

A. Terminate and log a message to Stackdriver

B. Retry using a truncated binary exponential back-off strategy

C. Prompt the user to decide to retry or quit

D. Terminate and log a message to Cloud Shell



Answers:&#x20;

B. gcloud by default will retry a failed network operation and will wait a long time before each retry. The time to wait is calculated using a truncated binary exponential back-off strategy.



### 7. All of the following are components of firewall rules except which one?

A. Direction of traffic

B. Action on match

C. Time to live (TTL)

D. Protocol



Answers:&#x20;

C. Firewall rules do not have TTL parameters. Direction of traffic, action on match, and protocol are all components of firewall rules.



### 8. Adding virtual machines to an instance group can be triggered in an autoscaling policy by all of the following, except which one?

A. CPU utilization

B. Stackdriver metrics

C. IAM policy violation

D. Load balancing serving capacity



Answers:&#x20;

C. IAM policy violations do not trigger changes in the size of clusters. All other options can be used to trigger a change in cluster size.



### 9. Your company’s finance department is developing a new account management application that requires transactions and the ability to perform relational database operations using fully compliant SQL. Data store options in GCP include:

A. Spanner and Cloud SQL

B. Datastore and Bigtable

C. Spanner and Cloud Storage&#x20;

D. Datastore and Cloud SQL



Answers:&#x20;

A. Only Spanner and Cloud SQL databases support transactions and have a SQL interface. Datastore has transactions but does not support fully compliant SQL; it has a SQL-like query language. Cloud Storage does not support transactions or SQL.



### 10. The marketing department in your company wants to deploy a web application but does not want to have to manage servers or clusters. A good option for them is:

A. Compute Engine

B. Kubernetes Engine

C. App Engine

D. Cloud Functions



Answers:&#x20;

C. App Engine is a PaaS that allows developers to deploy full applications without having to manage servers or clusters. Compute Engine and Kubernetes Engine require management of servers. Cloud Functions is suitable for short-running Node.js or Python functions but not full applications.



### 11. Your company is building an enterprise data warehouse and wants SQL query capabilities over petabytes of data, but does not want to manage servers or clusters. A good option for them is:

A. Cloud Storage

B. BigQuery

C. Bigtable

D. Datastore



Answers:&#x20;

B. BigQuery is designed for petabyte-scale analytics and provides a SQL interface.



### 12. You have been hired as a consultant to a startup in the Internet of Things (IoT) space. The startup will stream large volumes of data into GCP. The data needs to be filtered, trans- formed, and analyzed before being stored in GCP Datastore. A good option for the stream processing component is:

A. Dataproc

B. Cloud Dataflow

C. Cloud Endpoints

D. Cloud Interconnect



Answers:&#x20;

B. Cloud Dataflow allows for stream and batch processing of data and is well suited for this kind of ETL work. Dataproc is a managed Hadoop and Spark service that is used for big data analytics. Cloud Endpoints is an API service, and Cloud Interconnect is a network service.



### 13. Preemptible virtual machines may be shut down at any time but will always be shut down after running:

A. 6 hours

B. 12 hours

C. 24 hours

D. 48 hours



Answers:&#x20;

C. If a preemptible machine has not been shut down within 24 hours, Google will stop the instance.



### 14. You have been tasked with designing an organizational hierarchy for managing depart- ments and their cloud resources. What organizing components are available in GCP?

A. Organization, folders, projects

B. Buckets, directories, subdirectories

C. Organizations, buckets, projects

D. Folders, buckets, projects



Answers:&#x20;

A. Organizations, folders, and projects are the components used to manage an organizational hierarchy. Buckets, directories, and subdirectories are used to organize storage.



### 15. During an incident that has caused an application to fail, you suspect some resource may not have appropriate roles granted. The command to list roles granted to a resource is:

A. gutil iam list-grantable-roles&#x20;

B. gcloud iam list-grantable-roles&#x20;

C. gcloud list-grantable-roles

D. gcloud resources grantable-roles



Answers:&#x20;

B. gcloud is the command-line tool for working with IAM, and list-grantable-roles is

the correct command.



### 16. The availability of CPU platforms can vary between zones. To get a list of all CPU types available in a particular zone, you should use:

A. gcloud compute zones describe&#x20;

B. gcloud iam zones describe

C. gutil zones describe

D. gcloud compute regions list



Answers:&#x20;

A. gcloud is the command-line tool for manipulating compute resources, and zones

describe is the correct command.



### 17. To create a custom role, a user must possess which role?&#x20;

A. iam.create

B. compute.roles.create&#x20;

C. iam.roles.create

D. Compute.roles.add



Answers:&#x20;

C. iam.roles.create is correct; the other roles do not exist.



### 18. You have been asked to create a network with 1,000 IP addresses. In the interest of minimizing unused IP addresses, which CIDR suffix would you use to create a network with at least 1,000 addresses but no more than necessary?

A. /20&#x20;

B. /22&#x20;

C. /28&#x20;

D. /32



Answers:&#x20;

B. The /22 suffix produces 1,022 usable IP addresses.



### 19. A team of data scientists have asked for your help setting up an Apache Spark cluster. You suggest they use a managed GCP service instead of managing a cluster themselves on Compute Engine. The service they would use is:

A. Cloud Dataproc&#x20;

B. Cloud Dataflow&#x20;

C. Cloud Hadoop&#x20;

D. BigQuery



Answers:&#x20;

A. Cloud Dataproc is the managed Spark service. Cloud Dataflow is for stream and batch processing of data, BigQuery is for analytics, and Cloud Hadoop is not a GCP service.



### 20. You have created a web application that allows users to upload files to Cloud Storage. When files are uploaded, you want to check the file size and update the user’s total storage used in their account. A serverless option for performing this action on load is:

A. Cloud Dataflow

B. Cloud Dataproc

C. Cloud Storage

D. Cloud Functions



Answers:&#x20;

D. Cloud Functions responds to events in Cloud Storage, making them a good choice for taking an action after a file is loaded.



### 21. Your company has just started using GCP, and executives want to have a dedicated connec- tion from your data center to the GCP to allow for large data transfers. Which networking service would you recommend?

A. Google Cloud Carrier Internet Peering&#x20;

B. Google Cloud Interconnect – Dedicated&#x20;

C. Google Cloud Internet Peering

D. Google Cloud DNS



Answers:&#x20;

B. Google Cloud Interconnect – Dedicated is the only option for a dedicated connection between a customer’s data center and a Google data center.



### 22. You want to have GCP manage cryptographic keys, so you’ve decided to use Cloud Key Management Services. Before you can start creating cryptographic keys, you must:

A. Enable Google Cloud Key Management Service (KMS) API and set up billing

B. Enable Google Cloud KMS API and create folders

C. Create folders and set up billing

D. Give all users grantable roles to create keys



Answers:&#x20;

A. Enabling the Google Cloud KMS API and setting up billing are steps common to using GCP services.



### 23. In Kubernetes Engine, a node pool is:

A. A subset of nodes across clusters&#x20;

B. A set of VMs managed outside of Kubernetes Engine&#x20;

C. A set of preemptible VMs&#x20;

D. A subset of node instances within a cluster that all have the same configuration



Answers:&#x20;

D. A node pool is a subset of node instances within a cluster that all have the same configuration.



### 24. The GCP service for storing and managing Docker containers is:

A. Cloud Source Repositories

B. Cloud Build

C. Container Registry

D. Docker Repository



Answers:&#x20;

C. The GCP service for storing and managing Docker containers is Container Registry. Cloud Build is for creating images. The others are not GCP services.



### 25. Code for Cloud Functions can be written in:

A. Node.js and Python

B. Node.js, Python, and Go

C. Python and Go

D. Python and C



Answers:&#x20;

A. Node.js 6, Node.js 8, and Python are the languages supported by Cloud Functions.



