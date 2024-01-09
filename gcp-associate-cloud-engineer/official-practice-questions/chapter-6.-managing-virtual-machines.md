# Chapter 6. Managing Virtual Machines

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

#### 1. Which page in Google Cloud Console would you use to create a single instance of a VM?

A. Compute Engine

B. App Engine

C. Kubernetes Engine

D. Cloud Functions



Answers:

A. The Compute Engine page is where you have the option of creating a single VM instance, so option A is the correct answer. App Engine is used for containers and running applications in language-specific runtime environments. Kubernetes Engine is used to create and manage Kubernetes clusters. Cloud Functions is where you would create a function to run in Google’s serverless cloud function environment.



#### 2. You view a list of Linux VM instances in the console. All have public IP addresses assigned. You notice that the SSH option is disabled for one of the instances. Why might that be the case?

A. The instance is preemptible and therefore does not support SSH.

B. The instance is stopped.

C. The instance was configured with the No SSH option.

D. The SSH option is never disabled.



Answers:

B. Instances can be stopped, and when they are, then you cannot connect to them via SSH, which makes option B the correct answer. Starting the instance will enable SSH access. Option A is not correct because you can log into preemptible machines. Option C is incor- rect because there is no No SSH option. Option D is incorrect because the SSH option can be disabled.



#### 3. You have noticed unusually slow response time when issuing commands to a Linux server, and you decide to reboot the machine. Which command would you use in the console to reboot?

A. Reboot

B. Reset

C. Restart

D. Shutdown followed by Startup



Answers:

B. The Reset command can be used to restart a VM; thus, option B is correct. The prop- erties of the VM will not change, but data in memory will be lost. There is no Reboot, Restart, Shutdown, or Startup option in the console.



#### 4. In the console, you can filter the list of VM instances by which of the following?

A. Labels only

B. Member of managed instance group only

C. Labels, status, or members of managed instance group

D. Labels and status only



Answers:

C. Labels, members of a managed instance group, and status are all available for filtering, so option C is the correct answer. You can also filter by internal IP, external IP, zone, net- work, deletion protection, and member of a managed or unmanaged instance group.



#### 5. You will be building a number of machine learning models on an instance and attaching GPU to the instance. When you run your machine learning models they take an unusually long time to run. It appears that GPU is not being used. What could be the cause of this?

A. GPU libraries are not installed.

B. The operating system is based on Ubuntu.

C. You do not have at least eight CPUs in the instance.

D. There isn’t enough persistent disk space available.



Answers:

A. To function properly, the operating system must have GPU libraries installed, so option A is correct. The operating system does not have to be Ubuntu based, and there is no need to have at least eight CPUs in an instance before you can attach and use a GPU. Available disk space does not determine if a GPU is used or not.



#### 6. When you add a GPU to an instance, you must ensure that:

A. The instance is set to terminate during maintenance.

B. The instance is preemptible.

C. The instance does not have nonboot disks attached.

D. The instance is running Ubuntu 14.02 or later.



Answers:

A. If you add a GPU to a VM, you must set the instance to terminate during maintenance, which makes option A the correct response. This is set in the Availability Policies section of the VM configuration form. The instance does not need to be preemptible and it can have non-boot disks attached. The instance is not required to run Ubuntu 14.02 or later.



#### 7. You are using snapshots to save copies of a 100GB disk. You make a snapshot and then add 10GB of data. You create a second snapshot. How much storage is used in total for the two snapshots (assume no compression)?

A. 210 GB, with 100GB for the first and 110GB for the second

B. 110 GB, with 100GB for the first and 10GB for the second

C. 110 GB, with 110 for the second (the first snapshot is deleted automatically)

D. 221 GB, with 100GB for the first, 110GB for the second, plus 10 percent of the second snapshot (11 GB) for metadata overhead



Answers:

B. When you first create a snapshot, GCP will make a full copy of the data on the persis- tent disk. The next time you create a snapshot from that disk, GCP will only copy the data that has changed since the last snapshot. Option A is incorrect; GCP does not store a full copy of the second snapshot. Option C is incorrect; the first snapshot is not deleted auto- matically. Option D is incorrect, subsequent snapshots do not incur 10 percent overhead.



#### 8. You have decided to delegate the task of making backup snapshots to a member of your team. What role would you need to grant to your team member to create snapshots?

A. Compute Image Admin

B. Storage Admin

C. Compute Snapshot Admin

D. Compute Storage Admin



Answers:

D. To work with snapshots, a user must be assigned the Compute Storage Admin role, which makes option D the correct answer. The other options are fictitious roles.



#### 9. The source of an image may be:

A. Only disks

B. Snapshots or disks only

C. Disks, snapshots, or another image

D. Disks, snapshots, or any database export file



Answers:

C. Images can be created from four sources, namely, disks, snapshots, cloud storage files, or another image, so option C is the right answer. Database export files are not sources for images.



#### 10. You have built images using Ubuntu 14.04 and now want users to start using Ubuntu 16.04. You don’t want to just delete images based on Ubuntu 14.04, but you want users to know they should start using Ubuntu 16.04. What feature of images would you use to accomplish this?

A. Redirection&#x20;

B. Deprecated&#x20;

C. Unsupported&#x20;

D. Migration



Answers:

B. Deprecated marks the image as no longer supported and allows you to specify a replace- ment image to use going forward, making option B the correct answer. Deprecated images are available for use but may not be patched for security flaws or have other updates. The other options are fictitious features of images.



#### 11. You want to generate a list of VMs in your inventory and have the results in JSON format. What command would you use?

A. gcloud compute instances list

B. gcloud compute instances describe

C. gcloud compute instances list --format json&#x20;

D. gcloud compute instances list --output json



Answers:

C. The base command for working with instances is gcloud compute instances, which makes option C the correct answer. The list command is used to show details of all instances. By default, output is in human-readable form, not json. Using the --format json option forces the output to be in JSON format. --output is not a valid option.



#### 12. You would like to understand details of how GCP starts a virtual instance. Which optional parameter would you use when starting an instance to display those details?

A. --verbose&#x20;

B. --async

C. --describe&#x20;

D. --details



Answers:

B. –-async causes information about the start process to be displayed; therefore, option B is correct. --verbose is an analogous parameter in many Linux commands. --describe provides details about an instance but not necessarily the startup process. --details is not a valid parameter.



#### 13. Which command will delete an instance named ch06-instance-3?

A. gcloud compute instances delete instance=ch06-instance-3&#x20;

B. gcloud compute instance stop ch06-instance-3

C. gcloud compute instances delete ch06-instance-3

D. gcloud compute delete ch06-instance-3



Answers:

C. The command to delete an instance is gcloud compute instances delete followed by the name of the instance, so option C is correct. Option A is incorrect because there is no instance parameter. Option B is incorrect because that command stops but does not delete the instance. Option D is missing instances in the command, which is required to indicate what type of entity is being deleted.



#### 14. You are about to delete an instance named ch06-instance-1 but want to keep its boot disk. You do not want to keep other attached disks. What gcloud command would you use?

A. gcloud compute instances delete ch06-instance-1 ––keep-disks=boot

B. gcloud compute instances delete ch06-instance-1 ––save-disks=boot

C. gcloud compute instances delete ch06-instance-1 ––keep-disks=filesystem&#x20;

D. gcloud compute delete ch06-instance-1 ––keep-disks=filesystem



Answers:

A. gcloud compute instances is the base command followed by delete, the name of the instance, and --keep-disks=boot, so option A is correct. There is no --save-disk parameter. Option C is wrong because filesystem is not a valid value for the keep-disk parameter. Option D is missing the instances option which is required in the command.



#### 15. You want to view a list of fields you can use to sort a list of instances. What command would you use to see the field names?

A. gcloud compute instances list

B. gcloud compute instances describe

C. gcloud compute instances list --detailed

D. gcloud compute instances describe --detailed



Answers:

B. The correct answer is option B, which is to use the describe command. Option A will show some fields but not all. Options C and D are incorrect because there is no detailed parameter.



#### 16. You are deploying an application that will need to scale and be highly available. Which of these Compute Engine components will help achieve scalability and high availability?

A. Preemptible instances

B. Instance groups

C. Cloud Storage

D. GPUs



Answers:

B. Instance groups are sets of VMs that can be configured to scale and are used with load balancers, which contribute to improving availability, so option B is correct. Preemptible instances are not highly available because they can be shut down at any time by GCP. Cloud Storage is not a Compute Engine component. GPUs can help improve throughput for math-intensive operations but do not contribute to high availability.



#### 17. Before creating an instance group, you need to create what?

A. Instances in the instance group

B. Instance group template

C. Boot disk image

D. Source snapshot



Answers:

B. An instance group template is used to specify how the instance group should be created, which makes option B the correct answer. Option A is incorrect because instances are cre- ated automatically when an instance group is created. Boot disk images and snapshots do not have to be created before creating an instance group.



#### 18. How would you delete an instance group template using the command line?&#x20;

A. gcloud compute instances instance-template delete

B. glcoud compute instance-templates delete

C. gcloud compute delete instance-template

D. gcloud compute delete instance-templates



Answers:

B. The command to delete an instance group is gcloud compute instance-template delete, so option B is correct. Option A incorrectly includes the term instances. Option C is in incorrect order. Option D is wrong because instance-template is in the wrong position and is plural in the option.



#### 19. What can be the basis for scaling up an instance group?

A. CPU utilization and operating system updates

B. Disk usage and CPU utilization only

C. Network latency, load balancing capacity, and CPU utilization

D. Disk usage and operating system updates only



Answers:

C. You can configure an autoscaling policy to trigger adding or removing instances based on CPU utilization, monitoring metric, load balancing capacity, or queue-based workloads. Disk, network latency, and memory can trigger scaling if monitoring metrics on those resources are configured. So, option C is correct.



#### 20. An architect is moving a legacy application to Google Cloud and wants to minimize the changes to the existing architecture while administering the cluster as a single entity. The legacy application runs on a load-balanced cluster that runs nodes with two different configurations. The two configurations are required because of design decisions made several years ago. The load on the application is fairly consistent, so there is rarely a need to scale up or down. What GCP Compute Engine resource would you recommended using?

A. Preemptible instances

B. Unmanaged instance groups

C. Managed instance groups

D. GPUs



Answers:

B. Unmanaged instance groups are available for limited use cases such as this. Unmanaged instance groups are not recommended in general. Managed instance groups are the recom- mended way to use instance groups, but the two different configurations prevents their use. Preemptible instances and GPUs are not relevant to this scenario.

