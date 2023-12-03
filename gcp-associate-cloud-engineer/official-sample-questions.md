# \[Official] Sample Questions

#### 1. Your organization plans to migrate its financial transaction monitoring application to Google Cloud. Auditors need to view the data and run reports in BigQuery, but they are not allowed to perform transactions in the application. You are leading the migration and want the simplest solution that will require the least amount of maintenance. What should you do?&#x20;

A. Assign roles/bigquery.dataViewer to the individual auditors.&#x20;

B. Create a group for auditors and assign roles/viewer to them.&#x20;

C. Create a group for auditors, and assign roles/bigquery.dataViewer to them.&#x20;

D. Assign a custom role to each auditor that allows view-only access to BigQuery.



Answers: C

* A is not correct because Google recommended practice is to assign IAM roles to groups, not individuals. Groups are easier to manage than individual users and they provide high level visibility into roles and permissions.&#x20;
* B is not correct because it uses a basic role to give auditors view access to all resources on the project.&#x20;
* C is correct because it uses a predefined role to provide view access to BigQuery for the group of auditors. Auditors can be added or deleted from the group if job responsibilities change.&#x20;
* D is not correct because using a predefined role can accomplish the goal and requires less maintenance.



#### 2. You are managing your company’s first Google Cloud project. Project leads, developers, and internal testers will participate in the project, which includes sensitive information. You need to ensure that only specific members of the development team have access to sensitive information. You want to assign the appropriate Identity and Access Management (IAM) roles that also require the least amount of maintenance. What should you do?&#x20;

A. Assign a basic role to each user.&#x20;

B. Create groups. Assign a basic role to each group, and then assign users to groups.&#x20;

C. Create groups. Assign a Custom role to each group, including those who should have access to sensitive data. Assign users to groups.&#x20;

D. Create groups. Assign an IAM Predefined role to each group as required, including those who should have access to sensitive data. Assign users to groups.



Answers: D

* A is not correct for two reasons: The recommended practice is to use groups and not to assign roles to each user. Beyond that, Basic Roles do not have enough granularity to account for access to sensitive data.&#x20;
* B is not correct because Basic roles do not have enough granularity to account for access to sensitive data.&#x20;
* C is not correct because creating and maintaining Custom roles will require more maintenance than using Predefined roles.&#x20;
* D is correct because Predefined roles are fine-grained enough to set permissions for specific roles requiring sensitive data access. This solution also uses groups, which is the recommended practice for managing permissions for individual roles.



#### 3. You are responsible for monitoring all changes in your Cloud Storage and Firestore instances. For each change, you need to invoke an action that will verify the compliance of the change in near real time. You want to accomplish this with minimal setup. What should you do?&#x20;

A. Use the trigger mechanism in each datastore to invoke the security script.&#x20;

B. Use Cloud Function events, and call the security script from the Cloud Function triggers.

C. Redirect your data-changing queries to an App Engine application, and call the security script from the application.

D. Use a Python script to get logs of the datastores, analyze them, and invoke the security script.&#x20;



Answers: B

* A is not correct because setting triggers in each individual database requires additional setup.&#x20;
* B is correct because it provides fast response and requires the minimal amount of setup.&#x20;
* C is not correct because it requires custom programming.&#x20;
* D is not correct because it requires significant custom programming.



#### 4. Your application needs to process a significant rate of transactions. The rate of transactions exceeds the processing capabilities of a single virtual machine (VM). You want to spread transactions across multiple servers in real time and in the most cost-effective manner. What should you do?&#x20;

A. Send transactions to BigQuery. On the VMs, poll for transactions that do not have the ‘processed’ key, and mark them ‘processed’ when done.&#x20;

B. Set up Cloud SQL with a memory cache for speed. On your multiple servers, poll for transactions that do not have the ‘processed’ key, and mark them ‘processed’ when done.&#x20;

C. Send transactions to Pub/Sub. Process them in VMs in a managed instance group.&#x20;

D. Record transactions in Cloud Bigtable, and poll for new transactions from the VMs.



Answers: C

* A is not correct because its latency is significantly higher than the real-time response required.&#x20;
* B is not correct because it will not deliver the desired performance.&#x20;
* C is correct because Pub/Sub is a scalable solution that can effectively distribute a large number of tasks among multiple servers at a low cost.&#x20;
* D is not correct because, although fast, it will introduce an additional expense for storing the data.



#### 5. Your team needs to directly connect your on-premises resources to several virtual machines inside a virtual private cloud (VPC). You want to provide your team with fast and secure access to the VMs with minimal maintenance and cost. What should you do?&#x20;

A. Set up Cloud Interconnect.&#x20;

B. Use Cloud VPN to create a bridge between the VPC and your network.&#x20;

C. Assign a public IP address to each VM, and assign a strong password to each one.&#x20;

D. Start a Compute Engine VM, install a software router, and create a direct tunnel to each VM.



Answers: B

* A is not correct because it is significantly more expensive than other existing solutions.&#x20;
* B is correct because it agrees with the Google recommended practices.&#x20;
* C is not correct because it will require a sizable maintenance effort.&#x20;
* D is not correct because setting up connections for each individual VM requires a significant amount of maintenance.



#### 6. You are implementing Cloud Storage for your organization. You need to follow your organization’s regulations. They include: 1) Archive data older than one year. 2) Delete data older than 5 years. 3) Use standard storage for all other data. You want to implement these guidelines automatically and in the simplest manner available. What should you do?&#x20;

A. Set up Object Lifecycle management policies.&#x20;

B. Run a script daily. Copy data that is older than one year to an archival bucket, and delete five-year-old data.&#x20;

C. Run a script daily. Set storage class to ARCHIVE for data that is older than one year, and delete five-year-old data.&#x20;

D. Set up default storage class for three buckets named: STANDARD, ARCHIVE, DELETED. Use a script to move the data in the appropriate bucket when its condition matches your company guidelines.



Answers: A

* A is correct because Object Lifecycle allows you to automate the implementation of your organization’s data policy.&#x20;
* B is not correct because changing an object's storage class does not require copying the object to another bucket.&#x20;
* C is not correct because it requires custom programming.&#x20;
* D is not correct because moving an object to a DELETED bucket does not really delete it.



#### 7. You are creating a Cloud IOT application requiring data storage of up to 10 petabytes (PB). The application must support high-speed reads and writes of small pieces of data, but your data schema is simple. You want to use the most economical solution for data storage. What should you do?&#x20;

A. Store the data in Cloud Spanner, and add an in-memory cache for speed.&#x20;

B. Store the data in Cloud Storage, and distribute the data through Cloud CDN for speed.

C. Store the data in Cloud Bigtable, and implement the business logic in the programming language of your choice.&#x20;

D. Use BigQuery, and implement the business logic in SQL.



Answers: C

* A is not correct because Cloud Spanner would not be the most economical solution.&#x20;
* B is not correct because blob-oriented Cloud Storage is not a good fit for reading and writing small pieces of data.&#x20;
* C is correct because Bigtable provides high-speed reads and writes, accommodates a simple schema, and is cost-effective.&#x20;
* D is not correct because BigQuery does not provide the high-speed reads and writes required by IoT.



#### 8. You have created a Kubernetes deployment on Google Kubernetes Engine (GKE) that has a backend service. You also have pods that run the frontend service. You want to ensure that there is no interruption in communication between your frontend and backend service pods if they are moved or restarted. What should you do?&#x20;

A. Create a service that groups your pods in the backend service, and tell your frontend pods to communicate through that service.&#x20;

B. Create a DNS entry with a fixed IP address that the frontend service can use to reach the backend service.&#x20;

C. Assign static internal IP addresses that the frontend service can use to reach the backend pods.&#x20;

D. Assign static external IP addresses that the frontend service can use to reach the backend pods.



Answers: A

* A is correct because Kubernetes service serves the purpose of providing a destination that can be used when the pods are moved or restarted.&#x20;
* B is not correct because a DNS entry is created by service creation.&#x20;
* C is not correct because static internal IP addresses do not automatically change when pods are restarted.&#x20;
* D is not correct because static external IP addresses do not automatically change when pods are restarted, and they take traffic outside of Google networks.



#### 9. You are responsible for the user-management service for your global company. The service will add, update, delete, and list addresses. Each of these operations is implemented by a Docker container microservice. The processing load can vary from low to very high. You want to deploy the service on Google Cloud for scalability and minimal administration. What should you do?&#x20;

A. Deploy your Docker containers into Cloud Run.&#x20;

B. Start each Docker container as a managed instance group.&#x20;

C. Deploy your Docker containers into Google Kubernetes Engine.&#x20;

D. Combine the four microservices into one Docker image, and deploy it to the App Engine instance.



Answers: A

* A is correct because Cloud Run is a managed service that requires minimal administration.&#x20;
* B is not correct because managed instance groups lack management capabilities to expose their services.&#x20;
* C is not correct because, although GKE provides scalability, it requires ongoing administration of the cluster.&#x20;
* D is not correct because it required effort to reimplement the four microservices in one Docker container. You will also lose your microservice architecture.



#### 10. You provide a service that you need to open to everyone in your partner network. You have a server and an IP address where the application is located. You do not want to have to change the IP address on your DNS server if your server crashes or is replaced. You also want to avoid downtime and deliver a solution for minimal cost and setup. What should you do?&#x20;

A. Create a script that updates the IP address for the domain when the server crashes or is replaced.&#x20;

B. Reserve a static internal IP address, and assign it using Cloud DNS.&#x20;

C. Reserve a static external IP address, and assign it using Cloud DNS.&#x20;

D. Use the Bring Your Own IP (BYOIP) method to use your own IP address.



Answers: C

* A is not correct because updating DNS records could take up to 24 hours and it will cause downtime.&#x20;
* B is not correct because internal IPs are not routable and cannot be seen on the internet.&#x20;
* C is correct because external IPs are routable and can be advertised and seen on the internet, and this is also the most cost-effective solution.&#x20;
* D is not correct because, while it is possible, bringing your own IP address is not as cost effective as Google Cloud DNS



#### 11. Your team is building the development, test, and production environments for your project deployment in Google Cloud. You need to efficiently deploy and manage these environments and ensure that they are consistent. You want to follow Google-recommended practices. What should you do?&#x20;

A. Create a Cloud Shell script that uses gcloud commands to deploy the environments.&#x20;

B. Create one Terraform configuration for all environments. Parameterize the differences between environments.&#x20;

C. For each environment, create a Terraform configuration. Use them for repeated deployment. Reconcile the templates periodically.&#x20;

D. Use the Cloud Foundation Toolkit to create one deployment template that will work for all environments, and deploy with Terraform.



Answers: D

* A is not correct because creating a custom script of gcloud commands that adheres to Google Cloud recommended practices would require substantial development and maintenance effort.&#x20;
* B is not correct because parameterizing the environment differences is time consuming and error prone.&#x20;
* C is not correct because it is prone to error and involves significant reconciliation work.&#x20;
* D is correct because the Cloud Foundation Toolkit (CFT) provides ready-made templates that reflect Google Cloud recommended practices and can be used to automate creation of the environments.



#### 12. You receive an error message when you try to start a new VM: “You have exhausted the IP range in your subnet.” You want to resolve the error with the least amount of effort. What should you do?&#x20;

A. Create a new subnet and start your VM there.&#x20;

B. Expand the CIDR range in your subnet, and restart the VM that issued the error.&#x20;

C. Create another subnet, and move several existing VMs into the new subnet.&#x20;

D. Restart the VM using exponential backoff until the VM starts successfully.



Answers: B

* A is not correct because you do not need a new subnet. Once you expand the CIDR range, the initial VM will work by redeploying it.&#x20;
* B is correct because once you expand the CIDR range, you can redeploy it, and it will work.&#x20;
* C is not correct because moving your VMs to another subnet is an additional time-consuming effort that is not required.&#x20;
* D is not correct because once the CIDR range is exhausted, redeploying the failed VM will not resolve the issue.



#### 13. You are running several related applications on Compute Engine virtual machine (VM) instances. You want to follow Google-recommended practices and expose each application through a DNS name. What should you do?&#x20;

A. Use the Compute Engine internal DNS service to assign DNS names to your VM instances, and make the names known to your users.&#x20;

B. Assign each VM instance an alias IP address range, and then make the internal DNS names public.&#x20;

C. Assign Google Cloud routes to your VM instances, assign DNS names to the routes, and make the DNS names public.&#x20;

D. Use Cloud DNS to translate your domain names into your IP addresses.



Answers: D

* A is not correct because email is not the way for submitting DNS publication requests.&#x20;
* B is not correct because you cannot make the internal DNS name public.&#x20;
* C is not correct because you cannot make DNS names public.&#x20;
* D is correct because Cloud DNS is the proper tool for translating domain names into IP addresses.



#### 14. You are charged with optimizing Google Cloud resource consumption. Specifically, you need to investigate the resource consumption charges and present a summary of your findings. You want to do it in the most efficient way possible. What should you do?

A. Rename resources to reflect the owner and purpose. Write a Python script to analyze resource consumption.&#x20;

B. Attach labels to resources to reflect the owner and purpose. Export Cloud Billing data into BigQuery, and analyze it with Data Studio.&#x20;

C. Assign tags to resources to reflect the owner and purpose. Export Cloud Billing data into BigQuery, and analyze it with Data Studio.&#x20;

D. Create a script to analyze resource usage based on the project to which the resources belong. In this script, use the IAM accounts and services accounts that control given resources.



Answers: B

* A is not correct because it requires custom programming and does not follow Google recommended practices and is not the most efficient solution.&#x20;
* B is correct because it describes Google Recommended practice: labels are attached to resources and these labels are then propagated into billing items.&#x20;
* C is not correct because tags are no longer created when a label is created for a resource and cannot be used for tracking resources.&#x20;
* D is not correct because it requires custom programming.



#### 15. You are creating an environment for researchers to run ad hoc SQL queries. The researchers work with large quantities of data. Although they will use the environment for an hour a day on average, the researchers need access to the functional environment at any time during the day. You need to deliver a cost-effective solution. What should you do?&#x20;

A. Store the data in Cloud Bigtable, and run SQL queries provided by Bigtable schema.&#x20;

B. Store the data in BigQuery, and run SQL queries in BigQuery.&#x20;

C. Create a Dataproc cluster, store the data in HDFS storage, and run SQL queries in Spark.&#x20;

D. Create a Dataproc cluster, store the data in Cloud Storage, and run SQL queries in Spark.



Answers: B

* A is not correct because HBase does not allow ad-hoc queries.&#x20;
* B is correct because BigQuery allows for ad hoc queries and is cost effective.&#x20;
* C is not correct because HDFS is not the recommended storage to use with Dataproc on Google Cloud.&#x20;
* D is not correct because it is not the most cost-effective solution, because cluster is always running.



#### 16. You are migrating your workload from on-premises deployment to Google Kubernetes Engine (GKE). You want to minimize costs and stay within budget. What should you do?&#x20;

A. Configure Autopilot in GKE to monitor node utilization and eliminate idle nodes.&#x20;

B. Configure the needed capacity; the sustained use discount will make you stay within budget.&#x20;

C. Scale individual nodes up and down with the Horizontal Pod Autoscaler.&#x20;

D. Create several nodes using Compute Engine, add them to a managed instance group, and set the group to scale up and down depending on load.



Answers: A

* A is correct because Autopilot is designed to reduce the operational cost of managing clusters and optimize your clusters for production.&#x20;
* B is not correct because it violates the principle of provisioning on-demand rather than overprovisioning. Although sustained use discount lowers the budget, not using unnecessary resources will keep costs down more.&#x20;
* C is not correct because Horizontal Pod Autoscaler is for adjusting the Kubernetes parameters for performance, not for taking out unnecessary resources.&#x20;
* &#x20;D is not correct because, although Google Kubernetes Engine uses Compute Engine internally, managed instance groups lack the Autopilot capabilities for scaling Kubernetes.



#### 17. Your application allows users to upload pictures. You need to convert each picture to your internal optimized binary format and store it. You want to use the most efficient, cost-effective solution. What should you do?&#x20;

A. Store uploaded files in Cloud Bigtable, monitor Bigtable entries, and then run a Cloud Function to convert the files and store them in Bigtable.&#x20;

B. Store uploaded files in Firestore, monitor Firestore entries, and then run a Cloud Function to convert the files and store them in Firestore.&#x20;

C. Store uploaded files in Filestore, monitor Filestore entries, and then run a Cloud Function to convert the files and store them in Filestore.&#x20;

D. Save uploaded files in a Cloud Storage bucket, and monitor the bucket for uploads. Run a Cloud Function to convert the files and to store them in a Cloud Storage bucket.



Answers: D

* A is not correct because BigTable has limitations on storing binary files.&#x20;
* B is not correct because Firestore is not efficient for large binary files.&#x20;
* C is not correct because it is not the most cost-effective solution.&#x20;
* D is correct because it follows Google recommended-practices and is the most efficient, cost-effective solution.



#### 18. You are migrating your on-premises solution to Google Cloud. As a first step, the new cloud solution will need to ingest 100 TB of data. Your daily uploads will be within your current bandwidth limit of 100 Mbps. You want to follow Google-recommended practices for the most cost-effective way to implement the migration. What should you do?&#x20;

A. Set up Partner Interconnect for the duration of the first upload.&#x20;

B. Obtain a Transfer Appliance, copy the data to it, and ship it to Google.&#x20;

C. Set up Dedicated Interconnect for the duration of your first upload, and then drop back to regular bandwidth.&#x20;

D. Divide your data between 100 computers, and upload each data portion to a bucket. Then run a script to merge the uploads together.



Answers: B

* A is not correct because Partner Interconnect, although less expensive than Dedicated Interconnect, is still not the most cost effective solution for this migration.&#x20;
* B is correct because it follows Google recommended practices for these data sizes and is the most cost-effective solution to implement the migration.&#x20;
* C is not correct because Dedicated Interconnect is not the most cost-effective for this use case.&#x20;
* D is not correct because it is not the most cost effective solution.



#### 19. You are setting up billing for your project. You want to prevent excessive consumption of resources due to an error or malicious attack and prevent billing spikes or surprises. What should you do?&#x20;

A. Set up budgets and alerts in your project.&#x20;

B. Set up quotas for the resources that your project will be using.&#x20;

C. Set up a spending limit on the credit card used in your billing account.&#x20;

D. Label all resources according to best practices, regularly export the billing reports, and analyze them with BigQuery.



Answers: B

* A is not correct because budgets and alerts will result in notifications, but will not prevent excessive resource consumption.&#x20;
* B is correct because setting up quotas will prevent resource consumption from exceeding specified limits.&#x20;
* C is not correct because it will not prevent excessive resource consumption. Instead, your credit card will incur an unpaid balance; you will receive an email about it from Google and will still be liable to pay.&#x20;
* D is not correct because analyzing the root cause for going over the budget will not prevent overspend.



#### 20. Your project team needs to estimate the spending for your Google Cloud project for the next quarter. You know the project requirements. You want to produce your estimate as quickly as possible. What should you do?&#x20;

A. Build a simple machine learning model that will predict your next month’s spend.&#x20;

B. Estimate the number of hours of compute time required, and then multiply by the VM per-hour pricing.&#x20;

C. Use the Google Cloud Pricing Calculator to enter your predicted consumption for all groups of resources.&#x20;

D. Use the Google Cloud Pricing Calculator to enter your consumption for all groups of resources, and then adjust for volume discounts.



Answers: C

* A is not correct because, although ML produces excellent results in many areas, there are more straightforward approaches that require less time to produce an estimate.&#x20;
* B is not correct because you need to add other charges, such as storage and data egress charges.&#x20;
* C is correct because the Google Cloud Pricing Calculator quickly gives the result, and you know the resources required for the project.&#x20;
* D is not correct because volume discounts, also called sustained use discounts, are applied automatically and are included in the calculator estimates.

