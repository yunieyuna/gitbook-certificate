# Chapter 8. Managing Kubernetes Clusters

#### 1. You are running several microservices in a Kubernetes cluster. You’ve noticed some performance degradation. After reviewing some logs, you begin to think the cluster may be improperly configured, and you open Cloud Console to investigate. How do you see the details of a specific cluster?

A. Type the cluster name into the search bar.

B. Click the cluster name.

C. Use the gcloud cluster details command.

D. None of the above.



Answer:

B. When on the Cloud Console pages, you can click the cluster name to see a Details page, so option B is the correct answer. Typing the name of cluster in the search bar does not always return cluster details; it can return instance group details. There is no such com- mand as gcloud cluster details.



#### 2. You are viewing the details of a cluster in Cloud Console and want to see how many vCPUs are available in the cluster. Where would you look for that information?

A. Node Pools section of the Cluster Details page

B. Labels section of the Cluster Details page

C. Summary line of the Cluster Listing page

D. A and C



Answer:

D. You can find the number of vCPUs on the cluster listing in the Total Cores column or on the Details page in the Node Pool section in the size parameter, making option D correct. The Labels section does not have vCPU information.



#### 3. You have been assigned to help diagnose performance problems with applications running on several Kubernetes clusters. The first thing you want to do is understand, at a high level, the characteristics of the clusters. Which command should you use?

A. gcloud container list

B. gcloud container clusters list

C. gcloud clusters list

D. None of the above



Answer:

B. The correct command includes gcloud container to describe the service, clusters to indicate the resource you are referring to, and list to indicate the command, which makes option B the correct answer. Options A and C are not valid commands.



#### 4. When you first try to use the kubectl command, you get an error message indicating that the resource cannot be found or you cannot connect to the cluster. What command would you use to try to eliminate the error?

A. gcloud container clusters access

B. gdcloud container clusters get-credentials&#x20;

C. gcloud auth container

D. gcloud auth container clusters



Answer:

B. It is likely you do not have access privileges to the cluster. The gdcloud container clusters get-credentials command is the correct command to configure kubectl to use GCP credentials for the cluster, so option B is the right option. Options A, C, and D are invalid commands.



#### 5. An engineer recently joined your team and is not aware of your team’s standards for creating clusters and other Kubernetes objects. In particular, the engineer has not properly labeled several clusters. You want to modify the labels on the cluster from Cloud Console. How would you do it?

A. Click the Connect button.

B. Click the Deploy menu option.

C. Click the Edit menu option.

D. Type the new labels in the Labels section.



Answer:

C. Clicking the Edit button allows you to change, add, or remove labels, so option C is the correct answer. The Connect button is on the cluster listing page, and the Deploy button\
is for creating new deployments. There is no way to enter labels under the Labels section when displaying details.



#### 6. You receive a page in the middle of the night informing you that several services running on a Kubernetes cluster have high latency when responding to API requests. You review moni- toring data and determine that there are not enough resources in the cluster to keep up with the load. You decide to add six more VMs to the cluster. What parameters will you need to specify when you issue the cluster resize command?

A. Cluster size

B. Cluster name

C. Node pool name

D. All of the above



Answer:

D. When resizing, the gcloud container clusters resize command requires the name of the cluster and the node pool to modify. The size is required to specify how many nodes should be running. Therefore, option D is correct.



#### 7. You want to modify the number of pods in a cluster. What is the best way to do that?

A. Modify pods directly

B. Modify deployments

C. Modify node pools directly

D. Modify nodes



Answer:

B. Pods are used to implement replicas of a deployment. It is a best practice to modify\
the deployments, which are configured with a specification of the number of replicas that should always run, so option B is the correct answer. Option A is incorrect; you should not modify pods directly. Options C and D are incorrect because they do not change the num- ber of pods running an application.



#### 8. You want to see a list of deployments. Which option from the Kubernetes Engine navigation menu would you select?

A. Clusters

B. Storage

C. Workloads&#x20;

D. Deployments



Answer:

C. Deployments are listed under Workloads, making option C the correct answer. The Cluster option shows details about clusters but does not have details on deployments. Stor- age shows information about persistent volumes and storage classes. Deployments is not an option.



#### 9. What actions are available from the Actions menu when viewing deployment details?

A. Scale and Autoscale only

B. Autoscale, Expose, and Rolling Update

C. Add, Modify, and Delete

D. None of the above



Answer:

B. There are four actions available for deployments (Autoscale, Expose, Rolling Update, and Scale), so option B is correct. Add, Modify, and Delete are not options.



#### 10. What is the command to list deployments from the command line?

A. gcloud container clusters list-deployments

B. gcloud container clusters list

C. kubectl get deployments

D. kubectl deployments list\


Answer:

C. Since deployments are managed by Kubernetes and not GCP, we need to use a kubectl command and not a gcloud command, which makes option C correct. Option D is incorrect because it follows the gcloud command structure, not the kubectl command structure. The kubectl command has the verb, like get, before the resource type, like deployments, for example.



#### 11. What parameters of a deployment can be set in the Create Deployment page in Cloud Console?

A. Container image

B. Cluster name

C. Application name

D. All of the above



Answer:

D. You can specify container image, cluster name, and application name along with the labels, initial command, and namespace; therefore, option D is the correct answer.



#### 12. Where can you view a list of services when using Cloud Console?

A. In the Deployment Details page

B. In the Container Details page

C. In the Cluster Details page

D. None of the above



Answer:

A. The Deployment Details page includes services, so option A is the correct answer. Con- tainers are used to implement services; service details are not available there. The Clusters Detail page does not contain information on services running in the cluster.



#### 13. What kubectl command is used to add a service?&#x20;

A. run

B. start

C. initiate&#x20;

D. deploy



Answer:

A. kubectl run is the command used to start a deployment. It takes a name for the deployment, an image, and a port specification. The other options are not valid kubectl commands.



#### 14. You are supporting machine learning engineers who are testing a series of classifiers. They have five classifiers, called ml-classifier-1, ml-classifier-2, etc. They have found that ml- classifier-3 is not functioning as expected and they would like it removed from the cluster. What would you do to delete a service called ml-classifier-3?

A. Run the command kubectl delete service ml-classifier-3.

B. Run the command kubectl delete ml-classifier-3.

C. Run the command gcloud service delete ml-classifier-3.

D. Run the command gcloud container service delete ml-classifier-3.



Answer:

A. Option A shows the correct command, which is kubectl delete service ml- classifier-3. Option B is missing the service term. Options C and D cannot be correct because services are managed by Kubernetes, not GCP.



#### 15. What service is responsible for managing container images?

A. Kubernetes Engine

B. Compute Engine

C. Container Registry

D. Container Engine



Answer:

C. The Container Registry is the service for managing images that can be used in other services, including Kubernetes Engine and Compute Engine, making option C correct. Both Compute Engine and Kubernetes Engine use images but do not manage them. There is no service called Container Engine.



#### 16. What command is used to list container images in the command line?&#x20;

A. gcloud container images list

B. gcloud container list images

C. kubectl list container images

D. kubectl container list images



Answer:

A. Images are managed by GCP, so the correct command will be a gcloud command,\
so option A is the correct answer. Option B is incorrect because the verb is placed before the resource. Options C and D are incorrect because kubectl is for managing Kubernetes resources, not GCP resources like container images.



#### 17. A data warehouse designer wants to deploy an extraction, transformation, and load process to Kubernetes. The designer provided you with a list of libraries that should be installed, including drivers for GPUs. You have a number of container images that you think may meet the requirements. How could you get a detailed description of each of those containers?

A. Run the command gcloud container images list details.

B. Run the command gcloud container images describe.

C. Run the command gcloud image describe.

D. Run the command gcloud container describe.



Answer:

B. The correct command is gcloud container images describe, which makes option B the right answer. describe is the gcloud verb or operation for showing the details of an object. All other options are invalid commands.



#### 18. You have just created a deployment and want applications outside the cluster to have access to the services provided by the deployment. What do you need to do to the service?&#x20;

A. Give it a public IP address.

B. Issue a kubectl expose deployment command.

C. Issue a gcloud expose deployment command.

D. Nothing, making it accessible must be done at the cluster level.



Answer:

B. The kubectl expose deployment command makes a service accessible, so option B is the correct answer. IP addresses are assigned to VMs, not services. The command gcloud does not manage Kubernetes services, so option C is incorrect. Option D is incorrect because making a service accessible is not a cluster-level task.



#### 19. You have deployed an application to a Kubernetes cluster that processes sensor data from a fleet of delivery vehicles. The volume of incoming data depends on the number of vehicles making deliveries. The number of vehicles making deliveries is dependent on the number of customer orders. Customer orders are high during daytime hours, holiday seasons, and when major advertising campaigns are run. You want to make sure you have enough nodes running to handle the load, but you want to keep your costs down. How should you config- ure your Kubernetes cluster?

A. Deploy as many nodes as your budget allows.

B. Enable autoscaling.

C. Monitor CPU, disk, and network utilization and add nodes as necessary.

D. Write a script to run gcloud commands to add and remove nodes when peaks usually start and end, respectively.



Answer:

B. Autoscaling is the most cost-effective and least burdensome way to respond to changes in demand for a service, so option B is the correct answer. Option A may run nodes even when they are not needed. Option C is manually intensive and requires human intervention. Option D reduces human intervention but does not account for unexpected spikes or lulls in demand.



#### 20. When using Kubernetes Engine, which of the following might a cloud engineer need to configure?

A. Nodes, pods, services, and clusters only

B. Nodes, pods, services, clusters, and container images

C. Nodes, pods, clusters, and container images only

D. Pods, services, clusters, and container images only



Answer:

B. Cloud engineers working with Kubernetes will need to be familiar with working with clusters, nodes, pods, and container images. They will also need to be familiar with deploy- ment. Option B is the correct answer because the other options are all missing an important component of Kubernetes that cloud engineers will have to manage.

