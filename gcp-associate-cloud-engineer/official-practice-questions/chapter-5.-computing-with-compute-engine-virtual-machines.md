# Chapter 5. Computing with Compute Engine Virtual Machines

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

#### 1. You have just opened the GCP console at console.google.com. You have authenticated with the user you want to use. What is one of the first things you should do before perform- ing tasks on VMs?

A. Open Cloud Shell.

B. Verify you can SSH into a VM.

C. Verify that the selected project is the one you want to work with.

D. Review the list of running VMs.



Answers:

C. You should verify the project selected because all operations you perform will apply\
to resources in the selected project, making option C the correct answer. You do not need to open Cloud Shell unless you want to work with the command line, and if you did, you should verify that the project is correctly selected first. Logging into a VM using SSH is one of the tasks that requires you to be working with the correct project, so logging in via SSH should not happen before verifying the project. The list of VMs in the VM Instance win- dow is a list of VMs in the current project. You should verify which project you are using to ensure you are viewing the set of VMs you think you are using.



#### 2. What is a one-time task you will need to complete before using the console?

A. Set up billing

B. Create a project

C. Create a storage bucket

D. Specify a default zone



Answers:

A. You will need to set up billing if it is not already enabled when you start using the console, so option A is the right answer. You may create a project, but you will be able to do this only if billing is enabled. You do not need to create a storage bucket to work with the console. Specifying a default zone is not a one-time task; you may change zones throughout the life of your project.



#### 3. A colleague has asked for your assistance setting up a test environment in Google Cloud. They have never worked in GCP. You suggest starting with a single VM. Which of the following is the minimal set of information you will need?

A. A name for the VM and a machine type

B. A name for the VM, a machine type, a region, and a zone

C. A name for the VM, a machine type, a region, a zone, and a CIDR block

D. A name for the VM, a machine type, a region, a zone, and an IP address



Answers:

B. The name of the VM, the region and zone, and the machine type can all be specified in the console along with other parameters, so option B is correct. Option A is missing required parameters. A CIDR block is a range of IP addresses that is associated with a subnet and not needed to create a VM. An IP address is assigned automatically so it is not required.



#### 4. An architect has suggested a particular machine type for your workload. You are in the console creating a VM and you don’t see the machine type in the list of available machine types. What could be the reason for this?

A. You have selected the incorrect subnet.

B. That machine type is not available in the zone you specified.

C. You have chosen an incompatible operating system.

D. You have not specified a correct memory configuration.



Answers:

B. Different zones may have different machine types available, so you will need to specify a region first and then a zone to determine the set of machine types available. If the machine type does not appear in the list, it is not available in that zone. This makes option B the correct answer. Options A and C are incorrect. Subnets and IP addresses are not related to the machine types available. Unless you are specifying a custom machine type, you do not specify the amount of memory; that is defined by the machine type, so option D is incorrect.



#### 5. Your manager asks for your help with understanding cloud computing costs. Your team runs dozens of VMs for three different applications. Two of the applications are for use by the marketing department and one is use by the finance department. Your manager wants a way to bill each department for the cost of the VMs used for their applications. What would you suggest to help solve this problem?

A. Access controls

B. Persistent disks

C. Labels and descriptions

D. Descriptions only



Answers:

C. Labels and descriptions are for helping us track our own attributes of resources; GCP does not need them to perform its tasks. As the number of servers grows, it can become difficult to track which VMs are used for which applications and services, so option C is the correct answer. Labels and a general description will help administrators track numbers of VMs and their related costs. Options A and B are used for security and storage but do not help with managing multiple VMs. Option D is only partially correct. Descriptions are helpful but so are labels.



#### 6. If you wanted to set the preemptible property using Cloud Console, in which section of the Create An Instance page would you find the option?&#x20;

A. Availability Policy

B. Identity And API Access

C. Sole Tenancy

D. Networking



Answers:

A. The Availability Policy section within the Management tab is where you set preemptibility, so option A is correct. Identity And API Access is used to control the VM’s access to Google Cloud APIs and which service account is used with the VM. Sole Tenancy is used if you need to run your VMs on physical servers that only run your VMs. Networking is used to set network tags and change the network interface.



#### 7. You need to set up a server with a high level of security. You want to be prepared in case of attacks on your server by someone trying to inject a rootkit (a kind of malware that can alter the operating system). Which option should you select when creating a VM?

A. Firewall

B. Shield VM

C. Project-wide SSH keys

D. Boot disk integrity check



Answers:

B. Shield VM is an advanced set of security controls that includes Integrity Monitoring, a check to ensure boot images have not been tampered with, which makes option B the right answer. Firewalls are used to control ingress and egress of network traffic to a server or subnet. Project-wide SSH keys are used for authenticating users across servers within a proj- ect. Boot disk integrity check is a fictional feature.



#### 8. All of the following parameters can be set when adding an additional disk through Google Cloud Console, except one. Which one?

A. Disk type

B. Encryption key management&#x20;

C. Block size

D. Source image for the disk



Answers:

C. Block size is not an option in the Additional Disks dialog, so option C is correct. Encryption key management, disk type, and the option of specifying a source image are all available options.



#### 9. You lead a team of cloud engineers who maintain cloud resources for several departments in your company. You’ve noticed a problem with configuration drift. Some machine configurations are no longer in the same state as they were when created. You can’t find notes or documentation on how the changes were made or why. What practice would you implement to solve this problem?

A. Have all cloud engineers use only command-line interface in Cloud Shell.

B. Write scripts using gcloud commands to change configuration and store those scripts in

a version control system.

C. Take notes when making changes to configuration and store them in Google Drive.

D. Limit privileges so only you can make changes so you will always know when and why configurations were changed.



Answers:

B. Using version-controlled scripts is the best approach of the four options. Scripts can\
be documented with reasons for the changes and they can be run repeatedly on different machines to implement the same change. This reduces the chance of error when manually entering a command. Option A does not help to improve documenting why changes were made. Option C could help improve documentation, but executable scripts are precise and accurate reflections of what was executed. Notes may miss details. Option D is not advisable. You could become a bottleneck to making changes, changes cannot be made when you are unavailable, and your memory may not be a reliable way to track all configuration changes.



#### 10. When using the Cloud SDK command-line interface, which of the following is part of commands for administering resources in Compute Engine?

A. gcloud compute instances

B. gcloud instances

C. gcloud instances compute

D. None of the above



Answers:

A. gcloud compute instances is the start of commands for administering Compute Engine resources, making option A the right answer. Option B, gcloud instances, is missing the compute keyword that indicates we are working with Compute Engine. Option C has switched the order of compute and instances. Option D is false because option A is the correct answer.



#### 11. A newly hired cloud engineer is trying to understand what VMs are running in a particular project. How could the engineer get summary information on each VM running in a project?

A. Execute the command gcloud compute list

B. Execute the command gcloud compute instances list

C. Execute the command gcloud instances list

D. Execute the command gcloud list instances



Answers:

B. Option B follows the pattern of the glcoud command, which is hierarchical and starts with the glcoud name of the service, in this case compute for Compute Engine, followed by the next level down, which in this case is instances. Finally, there is the action or verb, in this case list. Option A is missing the term instances to indicate you are working with VM instances. Option C is missing the compute keyword to indicate you are working with Compute Engine. Option D is missing the compute instance keyword and has switched the order of instances and list.



#### 12. When creating a VM using the command line, how should you specify labels for the VM?

A. Use the --labels option with labels in the format of KEYS:VALUES.

B. Use the --labels option with labels in the format of KEYS=VALUE.

C. Use the --labels option with labels in the format of KEYS,VALUES.

D. This is not possible in the command line.



Answers:

B. The correct format is to use the `--labels` parameter and specify the key followed by\
an equal sign followed by the value in option B. Options A and C have the wrong character separating the key and value. Option D is incorrect because it is possible to specify labels in the command line.



#### 13. In the boot disk advanced configuration, which operations can you specify when creating a new VM?

A. Add a new disk, reformat an existing disk, attach an existing disk

B. Add a new disk and reformat an existing disk

C. Add a new disk and attach an existing disk

D. Reformat an existing disk and attach an existing disk



Answers:

C. The two operations you can specify when using the book disk configuration are adding a new disk and attaching an existing disk, so option C is correct. Reformatting an existing disk is not an option, so options A, B, and D cannot be the correct answer.



#### 14. You have acquired a 10 GB data set from a third-party research firm. A group of data scientists would like to access this data from their statistics programs written in R. R works well with Linux and Windows file systems, and the data scientists are familiar with file operations in R. The data scientists would each like to have their own dedicated VM with the data available in the VM’s file system. What is a way to make this data readily available on a VM and minimize the steps the data scientists will have to take?

A. Store the data in Cloud Storage.

B. Create VMs using a source image created from a disk with the data on it.&#x20;

C. Store the data in Google Drive.

D. Load the data into BigQuery.



Answers:

B. 10 GB of data is small enough to store on a single disk. By creating an image of a disk with the data stored on it, you can specify that source image when creating a VM. Option A would require the data scientist to copy the data from Cloud Storage to a disk on the VM. Option C would similarly require copying the data. Option D would load data into a database, not a file system as specified in the requirements.



#### 15. The Network tab of the create VM form is where you would perform which of the following operations?

A. Set the IP address of the VM

B. Add a network interface to the VM

C. Specify a default router

D. Change firewall configuration rules



Answers:

B. In the Network tab of the VM form, you can add another network interface, so option B is correct. GCP sets the IP address, so option A is incorrect. There is no option to specify a router or change firewall rules on the Network tab, so options C and D are incorrect.



#### 16. You want to create a VM using the gcloud command. What parameter would you include to specify the type of boot disk?

A. boot-disk-type&#x20;

B. boot-disk

C. disk-type

D. type-boot-disk



Answers:

A. The correct option is boot-disk-type, which is option A. The other three options are not parameters to the gcloud compute instances command.



#### 17. Which of the following commands will create a VM with four CPUs that is named web-server-1?

A. gcloud compute instances create --machine-type=n1-standard-4 web-server-1

B. gcloud compute instances create --cpus=4 web-server-1

C. gcloud compute instances create --machine-type=n1-standard-4 –instance- name web-server-1

D. gcloud compute instances create --machine-type=n1-4-cpu web-server-1



Answers:

A. Option A is the correct command. It is the only option that includes a correct machine type and properly specifies the name of the instance. Option B uses the --cpus parameter, which does not exist. Option C uses the parameter instance-name, which does not exist. The instance name is passed as an argument and does not need a parameter name. Option D is incorrect because machine type n1-4-cpu is not a valid machine type.



#### 18. Which of the following commands will stop a VM named web-server-1?&#x20;

A. gcloud compute instances halt web-server-1

B. gcloud compute instances --terminate web-server1

C. gcloud compute instances stop web-server-1

D. gcloud compute stop web-server-1



Answers:

C. Option C is the correct command, which is gcloud compute instances, to indicate you are working with VMs, followed by the stop command and the name of the VM. Option A is incorrect because halt is not an option. Option B is incorrect because –terminate is not a parameter. Option D is missing the word instances, which indicates you are working with VMs.



#### 19. You have just created an Ubuntu VM and want to log into the VM to install some software packages. Which network service would you use to access the VM?&#x20;

A. FTP

B. SSH

C. RDP

D. ipconfig



Answers:

B. SSH is service for connecting to a remote server and logging into a terminal window. Once logged in, you would have access to a command line, so option B is the right answer. FTP is a file transfer protocol and does not allow you to log in and perform system administration tasks. RDP is a protocol used to remotely access Windows servers, not Ubuntu, which is a Linux distribution. ipconfig is a command-line utility for configuring IP stacks on a device and does not allow you to log into a remote server.



#### 20. Your management team is considering three different cloud providers. You have been asked to summarize billing and cost information to help the management team compare cost structures between clouds. Which of the following would you mention about the cost of VMs in GCP?

A. VMs are billed in 1-second increments, cost varies with the number of CPUs and amount of memory in a machine type, you can create custom machine types, preemptible VMs cost up to 80 percent less than standard VMs, and Google offers discounts for sustained usage.

B. VMs are billed in 1-second increments and VMs can run up to 24 hours before they will be be shut down.

C. Google offers discounts for sustained usage in only some regions, cost varies with the number of CPUs and amount of memory in a machine type, you can create custom machine types, preemptible VMs cost up to 80 percent less than standard VMs.

D. VMs are charged for a minimum of 1 hour of use and cost varies with the number of CPUs and amount of memory in a machine type.



Answers:

A. All of the statements in option A are true and relevant to billing and costs. Option B\
is correct that VMs are billed in 1-second increments, but the only preemptible VMs are shut down within 24 hours of starting. Option C is incorrect because discounts are not limited to some regions. Option D is incorrect because VMs are not charged for a minimum of 1 hour.

