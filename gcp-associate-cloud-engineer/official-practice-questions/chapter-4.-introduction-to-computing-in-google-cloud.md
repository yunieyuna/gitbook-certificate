# Chapter 4. Introduction to Computing in Google Cloud

#### 1. You are deploying a Python web application to GCP. The application uses only custom code and basic Python libraries. You expect to have sporadic use of the application for the foreseeable future and want to minimize both the cost of running the application and the DevOps overhead of managing the application. Which computing service is the best option for running the application?

A. Compute Engine

B. App Engine standard environment

C. App Engine flexible environment

D. Kubernetes Engine



Answers:

B. The App Engine standard environment can run Python applications, which can autoscale down to no instances when there is no load and thereby minimize costs. Compute Engine and the App Engine flexible environment both require more configuration management than the App Engine standard environment. Kubernetes Engine is used when a cluster of servers is needed to support large or multiple applications using the same computing resources.



#### 2. Your manager is concerned about the rate at which the department is spending on cloud services. You suggest that your team use preemptible VMs for all of the following except which one?

A. Database server

B. Batch processing with no fixed time requirement to complete

C. High-performance computing cluster

D. None of the above



Answers:

A. Database servers require high availability to respond to queries from users or applications. Preemptible machines are guaranteed to shut down in at most 24 hours. A batch processing job with no fixed time requirements could use preemptible machines as long as the VM is restarted. High-performance computing clusters can use preemptible machines because work on a preemptible machine can be automatically rescheduled for another node on the cluster when a server is preempted. D is incorrect because there is a correct answer in the set of options.



#### 3. What parameters need to be specified when creating a VM in Compute Engine?

A. Project and zone

B. Username and admin role

C. Billing account

D. Cloud Storage bucket



Answers:

A. VMs are created in projects, which are part of the resource hierarchy. They are also located in geographic regions and data centers, so a zone is specified as well. Usernames and admin roles are not specified during creation. The billing account is tied to a project and so does not have to be specified when the VM is created. Cloud storage buckets are created independently of VMs. Not all VMs will make use of storage buckets.



#### 4. Your company has licensed a third-party software package that runs on Linux. You will run multiple instances of the software in a Docker container. Which of the following GCP services could you use to deploy this software package?

A. Compute Engine only

B. Kubernetes Engine only

C. Compute Engine, Kubernetes Engine, and the App Engine flexible environment only

D. Compute Engine, Kubernetes Engine, the App Engine flexible environment, or the App Engine standard environment



Answers:

C. Compute Engine can run Docker containers if you install Docker on the VM. Kubernetes and the App Engine flexible environment support Docker containers. The App Engine standard environment provides language-specific runtime environments and does not allow customers to specify custom Docker images for use.



#### 5. You can specify packages to install into a Docker container by including commands in which file?

A. Docker.cfg&#x20;

B. Dockerfile&#x20;

C. Config.dck&#x20;

D. install.cfg



Answers:

B. The name of the file that is used to build and configure a Docker container is Dockerfile.



#### 6. How much memory of a node does Kubernetes require as overhead?

A. 10GB to 20GB

B. 1GB to 2GB

C. 1.5GB

D. A scaled amount starting at 25 percent of memory and decreasing to 2 percent of marginal memory as the total amount of memory increases.



Answers:

D. Kubernetes uses 25 percent of memory up to 4GB and then slightly less for the next 4GB, and it continues to reduce the percentage of additional memory down to 2 percent of memory over 128GB.



#### 7. Your manager is making a presentation to executives in your company advocating that you start using Kubernetes Engine. You suggest that the manager highlight all the features Kubernetes provides to reduce the workload on DevOps engineers. You describe several features, including all of the following except which one?

A. Load balancing across Compute Engine VMs that are deployed in a Kubernetes cluster

B. Security scanning for vulnerabilities

C. Automatic scaling of nodes in the cluster

D. Automatic upgrading of cluster software as needed



Answers:

B. Kubernetes provides load balancing, scaling, and automatic upgrading of software. It does not provide vulnerability scanning. GCP does have a Cloud Security Scanner product, but that is designed to work with App Engine to identify common application vulnerabilities.



#### 8. Your company is about to release a new online service that builds on a new user interface experience driven by a set of services that will run on your servers. There is a separate set of services that manage authentication and authorization. A data store set of services keeps track of account information. All three sets of services must be highly reliable and scale to meet demand. Which of the GCP services is the best option for deploying this?

A. App Engine standard environment

B. Compute Engine

C. Cloud Functions

D. Kubernetes Engine



Answers:

D. The scenario described is a good fit for Kubernetes. Each of the groups of services can be structured in pods and deployed using Kubernetes deployment. Kubernetes Engine manages node health, load balancing, and scaling. App Engine Standard Edition has language-specific sandboxes and is not a good fit for this use case. Cloud Functions is designed for short-running event processing and is not the kind of continuous processing needed in this scenario. Compute Engine could meet the requirements of this use case, but it would require more effort on the part of application administrators and DevOps professionals to configure load balancers, monitor health, and manage software deployments.



#### 9. A mobile application uploads images for analysis, including identifying objects in the image and extracting text that may be embedded in the image. A third party has created the mobile application, and you have developed the image analysis service. You both agree to use Cloud Storage to store images. You want to keep the two services completely decoupled, but you need a way to invoke the image analysis as soon as an image is uploaded. How should this be done?

A. Change the mobile app to start a VM running the image analysis service and have that VM copy the file from storage into local storage on the VM. Have the image service run on the VM.

B. Write a function in Python that is invoked by Cloud Functions when a new image file is written to the Cloud Storage bucket that receives new images. The function should submit the URL of the uploaded file to the image analysis service. The image analysis service will then load the image from Cloud Storage, perform analysis, and generate results, which can be saved to Cloud Storage.

C. Have a Kubernetes cluster running continuously, with one pod dedicated to listing the contents of the upload bucket and detecting new files in Cloud Storage and another pod dedicated to running the image analysis software.

D. Have a Compute Engine VM running and continuously listing the contents of the upload bucket in Cloud Storage to detect new files. Another VM should be continually running the image analysis software.



Answers:

B. This is an ideal use case for Cloud Functions. The cloud function is triggered by a file upload event. The cloud function calls the image processing service. With this setup, the two services are independent. No additional servers are required. Option A violates the requirement to keep the services independent. Options C and D incur more management overhead and will probably cost more to operate than option B.



#### 10. Your team is developing a new pipeline to analyze a stream of data from sensors on manufacturing devices. The old pipeline occasionally corrupted data because parallel threads overwrote data written by other threads. You decide to use Cloud Functions as part of the pipeline. As a developer of a Cloud Function, what do you have to do to prevent multiple invocations of the function from interfering with each other?

A. Include a check in the code to ensure another invocation is not running at the same time.

B. Schedule each invocation to run in a separate process.

C. Schedule each invocation to run in a separate thread.

D. Nothing. GCP ensures that function invocations do not interfere with each other.



Answers:

D. Each invocation of a cloud function runs in a secure, isolated runtime environment. There is no need to check whether other invocations are running. With the Cloud Functions service, there is no way for a developer to control code execution at the process or thread level.



#### 11. A client of yours processes personal and health information for hospitals. All health information needs to be protected according to government regulations. Your client wants to move their application to Google Cloud but wants to use the encryption library that they have used in the past. You suggest that all VMs running the application have the encryption library installed. Which kind of image would you use for that?

A. Custom image

B. Public image

C. CentOS 6 or 7



Answers:

A. You would create a custom image after you installed the custom code, in this case the encryption library. A public image does not contain custom code, but it could be used as the base that you add custom code to. Both CentOS and Ubuntu are Linux distributions. You could use either as the base image that you add custom code to, but on their own, they do not have custom code.



#### 12. What is the lowest level of the resource hierarchy?

A. Folder

B. Project

C. File

D. VM instance



Answers:

B. Projects are the lowest level of the resource hierarchy. The organization is at the top of the hierarchy, and folders are between the organization and projects. VM instances are not part of the resource hierarchy.



#### 13. Your company is seeing a marked increase in the rate of customer growth in Europe. Latency is becoming an issue because your application is running in us-central1. You suggest deploying your services to a region in Europe. You have several choices. You should consider all of the following factors except which one?

A. Cost

B. Latency

C. Regulations&#x20;

D. Reliability



Answers:

D. All Google regions have the same level of service level agreement, so reliability is the same. Costs may differ between regions. Regulations may require that data stay within a geographic area, such as the European Union. Latency is a consideration when you want a region that is close to end users or data you will need is already stored in a particular region.



#### 14. What role gives users full control over Compute Engine instances?

A. Compute Manager role

B. Compute Admin role

C. Compute Manager role

D. Compute Security Admin



Answers:

B. Compute Engine Admin Role is the role that gives users complete control over instances. Options A and C are fictitious roles. Compute Engine Security Admin gives users the privi- leges to create, modify, and delete SSL certificates and firewall rules.



#### 15. Which of the following are limitations of a preemptible VM?

A. Will be terminated within 24 hours.

B. May not always be available. Availability may vary across zones and regions.

C. Cannot migrate to a regular VM.

D. All of the above



Answers:

D. Preemptible VMs will be terminated after 24 hours. Google does not guarantee that preemptible VMs will be available. Once an instance is started as a preemptible machine, it cannot migrate to a regular VM. You could, however, save a snapshot and use that to create a new regular instance.



### 16. Custom VMs can have up to how many vCPUs?&#x20;

A. 16

B. 32&#x20;

C. 64&#x20;

D. 128



Answers:

C. Custom VMs can have up to 64 CPUs and up to 6.5GB of memory per vCPU.



#### 17. When using the App Engine standard environment, which of the following language’s runtime is not supported?

A. Java

B. Python&#x20;

C. C

D. Go



Answers:

C. The C programming language is not supported in the App Engine standard environment. If you need to run a C application, it can be compiled and run in a container running in the App Engine flexible environment.



#### 18. Kubernetes reserves CPU resources in percentage of cores available. The percentage is what range?

A. 1 percent to 10 percent

B. 0.25 percent to 6 percent

C. 0.25 percent to 2 percent

D. 10 percent to 12 percent



Answers:

B. Kubernetes reserves CPU capacity according to the following schedule:

1. 6 percent of the first core
2. 1 percent of the next core (up to two cores)
3. 0.5 percent of the next two cores (up to four cores)
4. 0.25 percent of any cores above four cores



#### 19. Kubernetes deployments can be in what states?

A. Progressing, stalled, completed

B. Progressing, completed, failed

C. Progressing, stalled, failed, completed

D. Progressing, stalled, running, failed, completed



Answers:

B. The only states a Kubernetes deployment can be in are progressing, completed, and failed.



#### 20. A client has brought you in to help reduce their DevOps overhead. Engineers are spending too much time patching servers and optimizing server utilization. They want to move to serverless platforms as much as possible. Your client has heard of Cloud Functions and wants to use them as much as possible. You recommend all of the following types of applications except which one?

A. Long-running data warehouse data load procedures

B. IoT backend processing

C. Mobile application event processing

D. Asynchronous workflows



Answers:

A. Cloud Functions is best suited for event-driven processing, such as a file being uploaded to Cloud Storage or an event being writing to a Pub/Sub queue. Long-running jobs, such as loading data into a data warehouse, are better suited to Compute Engine or App Engine.



