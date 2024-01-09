# Chapter 7. Computing with Kubernetes

#### Understanding Level:

* O: Understand the whole question
* △: Not sure about part of the question
* ×: Don't understand the question

| Question Number | Trial 1 | Trial 2 | Trial 3 |
| --------------- | ------- | ------- | ------- |
| 1               | ×       |         |         |
| 2               | ×       |         |         |
| 3               | ×       |         |         |
| 4               | ×       |         |         |
| 5               | ×       |         |         |
| 6               | ×       |         |         |
| 7               | △       |         |         |
| 8               | O       |         |         |
| 9               | ×       |         |         |
| 10              | ×       |         |         |
| 11              | ×       |         |         |
| 12              | ×       |         |         |
| 13              | O       |         |         |
| 14              | ×       |         |         |
| 15              | ×       |         |         |
| 16              | ×       |         |         |
| 17              | ×       |         |         |
| 18              | ×       |         |         |
| 19              | ×       |         |         |
| 20              | ×       |         |         |

#### 1. A new engineer is asking for clarification about when it is best to use Kubernetes and when to use instance groups. You point out that Kubernetes uses instance groups. What purpose do instance groups play in a Kubernetes cluster?

A. They monitor the health of instances.

B. They create pods and deployments.

C. They create sets of VMs that can be managed as a unit.

D. They create alerts and notification channels.



Answers:

C. Kubernetes creates instance groups as part of the process of creating a cluster, which makes option C the correct answer. Stackdriver, not instance groups, is used to monitor the health of nodes and to create alerts and notifications. Kubernetes creates pods and deployments; they are not provided by instance groups.



#### 2. What kinds of instances are required to have a Kubernetes cluster?

A. A cluster master and nodes to execute workloads.

B. A cluster master, nodes to execute workloads, and Stackdriver nodes to monitor node health.

C. Kubernetes nodes; all instances are the same.

D. Instances with at least four vCPUs.



Answers:

A. A Kubernetes cluster has a single cluster master and one or more nodes to execute workloads, so option A is the correct answer. Stackdriver is not part of the Kubernetes cluster;\
it is a separate GCP service. Kubernetes does not require instances with at least four vCPUs; in fact, the default node configuration uses one vCPU.



#### 3. What is a pod in Kubernetes?

A. A set of containers

B. Application code deployed in a Kubernetes cluster

C. A single instance of a running process in a cluster

D. A controller that manages communication between clients and Kubernetes services



Answers:

C. Pods are single instances of a running process in a cluster, so option C is correct. Pods run containers but are not sets of containers. Application code runs in containers that are deployed in pods. Pods are not controllers, so they cannot manage communication with clients and Kubernetes services.



#### 4. You have developed an application that calls a service running in a Kubernetes cluster. The service runs in pods that can be terminated if they are unhealthy and replaced with other pods that might have a different IP address. How should you code your application to ensure it functions properly in this situation?

A. Query Kubernetes for a list of IP addresses of pods running the service you use.

B. Communicate with Kubernetes services so applications do not have to be coupled to

specific pods.

C. Query Kubernetes for a list of pods running the service you use.

D. Use a gcloud command to get the IP addresses needed.



Answers:

B. Services are applications that provide API endpoints that allow applications to discover pods running a particular application, making option B correct. Options A and C, if they could be coded using the API designed for managing clusters, would require more code than working with services and are subject to changes in a larger set of API functions. Option D is not an actual option.



#### 5. You have noticed that an application’s performance has degraded significantly. You have recently made some configuration changes to resources in your Kubernetes cluster and suspect that those changes have alerted the number of pods running in the cluster. Where would you look for details on the number of pods that should be running?

A. Deployments&#x20;

B. Stackdriver&#x20;

C. ReplicaSet&#x20;

D. Jobs



Answers:

C. ReplicaSets are controllers that are responsible for maintaining the correct number of pods, which makes option C the correct answer. Deployments are versions of application code running on a cluster. Stackdriver is a monitoring and logging service that monitors but does not control Kubernetes clusters. Jobs is an abstraction of workloads and is not tied to the number of pods running in a cluster.



#### 6. You are deploying a high availability application in Kubernetes Engine. You want to maintain availability even if there is a major network outage in a data center. What feature of Kubernetes Engine would you employ?

A. Multiple instance groups&#x20;

B. Multizone/region cluster&#x20;

C. Regional deployments&#x20;

D. Load balancing



Answers:

B. Multizone/multiregion clusters are available in Kubernetes Engine and are used to provide resiliency to an application, so option B is correct. Option A refers to instance groups that are a feature of Compute Engine, not directly of Kubernetes Engine. Option C is incorrect; regional deployments is a fictitious term. Load balancing distributes load and is part of Kubernetes by default. If load is not distributed across zones or regions, it does not help to add resiliency across data centers.



#### 7. You want to write a script to deploy a Kubernetes cluster with GPUs. You have deployed clusters before, but you are not sure about all the required parameters. You need to deploy this script as quickly as possible. What is one way to develop this script quickly?

A. Use the GPU template in the Kubernetes Engine cloud console to generate the gcloud command to create the cluster

B. Search the Web for a script

C. Review the documentation on gcloud parameters for adding GPUs

D. Use an existing script and add parameters for attaching GPUs



Answers:

A. Option A is the best answer. Starting with an existing template, filling in parameters, and generating the gcloud command is the most reliable way. Option D may work, but multiple parameters that are needed for your configuration may not be in the script you start with. There may be some trial and error with this option. Options B and C may lead to a solution but could take some time to complete.



#### 8. What gcloud command will create a cluster named ch07-cluster-1 with four nodes?&#x20;

A. gcloud beta container clusters create ch07-cluster-1 --num-nodes=4&#x20;

B. gcloud container beta clusters create ch07-cluster-1 --num-nodes=4&#x20;

C. gcloud container clusters create ch07-cluster-1 --num-nodes=4

D. gcloud beta container clusters create ch07-cluster-1 4



Answers:

A. The correct command is option A. Option B has beta in the wrong position. Option C is missing beta. Option D is missing the --num-nodes parameter name.



#### 9. When using Create Deployment from Cloud Console, which of the following cannot be specified for a deployment?

A. Container image

B. Application name

C. Time to live (TTL)

D. Initial command



Answers:

C. Time to Live is not an attribute of deployments, so option C is the correct answer. Application name, container image, and initial command can all be specified.



#### 10. Deployment configuration files created in Cloud Console use what type of file format?&#x20;

A. CSV

B. YAML&#x20;

C. TSV&#x20;

D. JSON



Answers:

B. Deployment configuration files created in Cloud Console are saved in YAML format. CSV, TSV, and JSON are not used.



#### 11. What command is used to run a Docker image on a cluster?&#x20;

A. gcloud container run

B. gcloud beta container run

C. kubectl run

D. kubectl beta run



Answers:

C. The kubectl command is used to control workloads on a Kubernetes cluster once it is created, so option C is correct. Options A and B are incorrect because gcloud is not used to manipulate Kubernetes processes. Option D is wrong because beta is not required in kubectl commands.



#### 12. What command would you use to have 10 replicas of a deployment named ch07-app-deploy?

A. kubectl upgrade deployment ch07-app-deploy --replicas=5&#x20;

B. gcloud containers deployment ch07-app-deploy --replicas=5&#x20;

C. kubectl scale deployment ch07-app-deploy --replicas=10

D. kubectl scale deployment ch07-app-deploy --pods=5



Answers:

C. Option C is the correct command. Option A uses the term upgrade instead of scale. Option B incorrectly uses gcloud. Option D uses the incorrect parameter pods.



#### 13. Stackdriver is used for what operations on Kubernetes clusters?

A. Notifications only

B. Monitoring and notifications only

C. Logging only

D. Notifications, monitoring, and logging



Answers:

D. Stackdriver is a comprehensive monitoring, logging, alerting, and notification service that can be used to monitor Kubernetes clusters.



#### 14. Before monitoring a Kubernetes cluster, what must you create with Stackdriver?&#x20;

A. Log

B. Workspace&#x20;

C. Pod

D. ReplicaSet



Answers:

B. Workspaces are logical structures for storing information about resources in a project that are being monitored, so option B is correct. Stackdriver works with logs, but a log is not required before starting to use Stackdriver. Pods and ReplicaSets are part of Kubernetes, not Stackdriver.



#### 15. What kind of information is provided in the Details page about an instance in Stackdriver?

A. CPU usage only

B. Network traffic only

C. Disk I/O, CPU usage, and network traffic

D. CPU usage and disk I/O



Answers:

C. The Stackdriver Instance Detail page includes time-series charts on CPU usage, network traffic, and disk I/O.



#### 16. When creating an alerting policy, what can be specified?

A. Conditions, notifications, and time to live

B. Conditions, notifications, and documentation

C. Conditions only

D. Conditions, documentation, and time to live



Answers:

B. When creating an alert policy, you can specify conditions, notifications, and documentation, making option B the correct answer. Options A and D are incorrect because there is no Time to Live attribute on policies. Option C is wrong because it does not include notifications and documentation.



#### 17. Your development team needs to be notified if there is a problem with applications running on several Kubernetes clusters. Different team members prefer different notification methods in addition to Stackdriver alerting. What is the most efficient way to send notifications and meet your team’s requests?

A. Set up SMS text messaging, Slack, and email notifications on an alert.

B. Create a separate alert for each notification channel.

C. Create alerts with email notifications and have those notification emails forwarded to other notification systems.

D. Use a single third-party notification mechanism.



Answers:

A. Alerts can have multiple channels, so Option A is correct. Channels include email, webhooks, and SMS text messaging as well as third-party tools such as PagerDuty, Campfire, and Slack. There is no need for multiple alerts with individual notifications. Option C is ad hoc and would require additional maintenance overhead. Option D does not meet requirements.



#### 18. A new engineer is trying to set up alerts for a Kubernetes cluster. The engineer seems to be creating a large number of alerts and you are concerned this is not the most efficient way and will lead to more maintenance work than required. You explain that a more efficient way is to create alerts and apply them to what?

A. One instance only

B. An instance or entire group

C. A group only

D. A pod



Answers:

B. Alerts are assigned to instances or sets of instances; therefore, option B is correct. Option A is incorrect because it does not include groups. Option C is incorrect because it does not include instances. Option D is wrong because alerts are not assigned to pods.



#### 19. You are attempting to execute commands to initiate a deployment on a Kubernetes cluster. The commands are not having any effect. You suspect that a Kubernetes component is not functioning correctly. What component could be the problem?

A. The Kubernetes API

B. A StatefulSet

C. Cloud SDK gcloud commands

D. ReplicaSet



Answers:

A. All interactions with the cluster are done through the master using the Kubernetes API. If an action is to be taken on a node, the command is issued by the cluster master, so option A is the correct answer. Options B and D are incorrect because they are controllers within the cluster and do not impact how commands are received from client devices. Option C is incorrect because kubectl, not gcloud, is used to initiate deployments.



#### 20. You have deployed an application to a Kubernetes cluster. You have noticed that several pods are starved for resources for a period of time and the pods are shut down. When resources are available, new instantiations of those pods are created. Clients are still able to connect to pods even though the new pods have different IP addresses from the pods that were terminated. What Kubernetes component makes this possible?

A. Services&#x20;

B. ReplicaSet&#x20;

C. Alerts

D. StatefulSet



Answers:

A. Services provide a level of indirection to accessing pods. Pods are ephemeral. Clients connect to services, which can discover pods. ReplicaSets and StatefulSets provide managed pods. Alerts are for reporting on the state of resources.

