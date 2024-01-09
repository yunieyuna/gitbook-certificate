# Chapter 14. Networking in the Cloud: Virtual Private Clouds and Virtual Private Networks

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

#### 1. Virtual private clouds have a \_\_\_\_\_ scope.

A. Zonal

B. Regional

C. Super-regional&#x20;

D. Global



Answers:

D. Virtual private clouds are global, so option D is correct. By default, they have subnets in all regions. Resources in any region can be accessed through the VPC. Options A, B, and C are all incorrect.



#### 2. You have been tasked with defining CIDR ranges to use with a project. The project includes 2 VPCs with several subnets in each VPC. How many CIDR ranges will you need to define?

A. One for each VPC

B. One for each subnet

C. One for each region

D. One for each zone



Answers:

B. IP ranges are assigned to subnets, so option B is correct. Each subnet is assigned an IP range for its exclusive use. IP ranges are assigned network structures, not zones and regions. VPCs can have multiple subnets but each subnet has its own address range.



#### 3. The legal department needs to isolate its resources on its own VPC. You want to have network provide routing to any other service available on the global network. The VPC network has not learned global routes. What parameter may have been missed when creating the VPC subnets?

A. DNS server policy

B. Dynamic routing

C. Static routing policy

D. Systemic routing policy



Answers:

B. Option B is correct; dynamic routing is the parameter that specifies whether routes are learned regionally or globally. Option A is incorrect; DNS is a name resolution service and is not involved with routing. Option C is incorrect; there is no static routing policy param- eter. Option D is incorrect because global routing is not an actual option.



#### 4. The command to create a VPC from the command line is:&#x20;

A. gcloud compute networks create

B. gcloud networks vpc create

C. gsutil networks vpc create

D. gcloud compute create networks



Answers:

A. The correct answer is gcloud compute networks create, which is option A. Option B is incorrect; networks vpc is not a correct part of the command. Option C is incorrect because gsutil is the command used to work with Cloud Storage. Option D is incorrect because there is no such thing.



#### 5. You have created several subnets. Most of them are sending logs to Stackdriver. One subnet is not sending logs. What option may have been misconfigured when creating the subnet that is not forwarding logs?

A. Flow Logs

B. Private IP Access

C. Stackdriver Logging

D. Variable-Length Subnet Masking



Answers:

A. The Flow Log option of the create vpc command determines whether logs are sent to Stackdriver, so option A is correct. Option B, Private IP Access, determines whether an external IP address is needed by a VM to use Google services. Option C is incorrect because Stackdriver Logging is the service, not a parameter used when creating a sub- net. Option D is incorrect because variable-length subnet masking has to do with CIDR addresses, not logging.



#### 6. At what levels of the resource hierarchy can a shared VPC be created?&#x20;

A. Folders and resources

B. Organizations and project

C. Organizations and folders

D. Folders and subnets



Answers:

C. Shared VPCs can be created at the organization or folder level of the resource hierarchy, so option C is correct. Options A and B are incorrect; shared VPCs are not created at the resource or project levels. Option D is incorrect; shared VPCs are not applied at subnets, which are resources in the resource hierarchy.



#### 7. You are using Cloud Console to create a VM that you want to exist in a custom subnet you just created. What section of the Create Instance form would you use to specify the custom subnet?

A. Networking tab of the Management, Security, Disks, Networking, Sole Tenancy section

B. Management tab of the Management, Security, Disks, Networking, Sole Tenancy section

C. Sole Tenancy tab of Management, Security, Disks, Networking, Sole Tenancy

D. Sole Tenancy tab of Management, Security, Disks, Networking



Answers:

A. The correct answer is the Networking tab of the Management, Security, Disks, Net- working, Sole Tenancy section of the form, which makes option A correct. The Manage- ment tab is not about subnet configurations. Option D is incorrect because it does not lead to Sole Tenancy options.



#### 8. You want to implement interproject communication between VPCs. Which feature of VPCs would you use to implement this?

A. VPC peering

B. Interproject peering&#x20;

C. VPN

D. Interconnect



Answers:

A. VPC is used for interproject communications. Option B is incorrect; there is no inter- project peering. Options C and D are incorrect; they have to do with linking on-premise networks with networks in GCP.



#### 9. You want to limit traffic to a set of instances. You decide to set a specific network tag on each instance. What part of a firewall rule can reference the network tag to determine the set of instances affected by the rule?

A. Action

B. Target

C. Priority&#x20;

D. Direction



Answers:

B. The target can be all instances in a network, instances with particular network tags, or instances using a specific service account, so option B is correct. Option A is incorrect; action is either allow or deny. Option C is incorrect; priority determines which of all the matching rules is applied. Option D is incorrect; it specifies whether the rule is applied to incoming or outgoing traffic.



#### 10. What part of a firewall rule determines whether a rule applies to incoming or outgoing traffic?

A. Action

B. Target

C. Priority&#x20;

D. Direction



Answers:

D. Direction specifies whether the rule is applied to incoming or outgoing traffic, which makes option D the right answer. Option A is incorrect; action is either allow or deny. Option B is incorrect; target specifies the set of instances that the rule applies to. Option C is incorrect; priority determines which of all matching rules is applied.



#### 11. You want to define a CIDR range that applies to all destination addresses. What IP address would you specify?

A. 0.0.0.0/0

B. 10.0.0.0/8

C. 172.16.0.0/12&#x20;

D. 192.168.0.0/16



Answers:

A. The 0.0.0.0/0 matches all IP addresses, so option A is correct. Option B represents a block of 16,777,214 addresses. Option C represents a block of 1,048,574 addresses. Option D represents a block of 65,534. You can experiment with CIDR block options using a CIDR calculator such as the one at www.subnet-calculator.com/cidr.php.



#### 12. You are using gcloud to create a firewall rule. Which command would you use?&#x20;

A. gcloud network firewall-rules create

B. gcloud compute firewall-rules create

C. gcloud network rules create

D. gcloud compute rules create



Answers:

B. The product you are working with is compute and the resource you are creating is a fire- wall rule, so option B is correct. Options A and C references network instead of compute. Option D references rules instead of firewall-rules.



#### 13. You are using gcloud to create a firewall rule. Which parameter would you use to specify the subnet it should apply to?

A. ––subnet

B. ––network

C. ––destination&#x20;

D. ––source-ranges



Answers:

B. The correct parameter is network, which makes option B correct. Option A is incorrect; subnet is not a parameter to gcloud to create a firewall. Option C is incorrect; desti- nation is not a valid parameter. Option D is incorrect; source-ranges is for specifying sources of network traffic the rule applies to.



#### 14. An application development team is deploying a set of specialized service endpoints and wants to limit traffic so that only traffic going to one of the endpoints is allowed through by firewall rules. The service endpoints will accept any UDP traffic and each endpoint will use a port in the range of 20000–30000. Which of the following commands would you use?

A. gcloud compute firewall-rules create fwr1 --allow=udp:20000-30000 --direction=ingress

B. gcloud network firewall-rules create fwr1 --allow=udp:20000-30000 --direction=ingress

C. gcloud compute firewall-rules create fwr1 --allow=udp

D. gcloud compute firewall-rules create fwr1 --direction=ingress



Answers:

A. The rule in option A uses the correct gcloud command and specifies the allow and direction parameters. Option B is incorrect because it references gcloud network instead of gcloud compute. Option C is incorrect because it does not specify the port range. Option D is incorrect because it does not specify the protocol or port range.



#### 15. You have a rule to allow inbound traffic to a VM. You want it to apply only if there is not another rule that would deny that traffic. What priority should you give this rule?

A. 0

B. 1

C. 1000&#x20;

D. 65535



Answers:

D. Option D is correct because it is the largest number allowed in the range of values for priorities. The larger the number, the lower the priority. Having the lowest priority will ensure that other rules that match will apply.



#### 16. You want to create a VPN using Cloud Console. What section of Cloud Console should you use?

A. Compute Engine

B. App Engine

C. Hybrid Connectivity

D. IAM & Admin



Answers:

C. The VPC create option is available in the Hybrid Connectivity section, so option C is cor- rect. Compute Engine, App Engine, and IAM & Admin do not have features related to VPNs.



#### 17. You are using Cloud Console to create a VPN. You want to configure the GCP end of the VPN. What section of the Create VPN form would you use?&#x20;

A. Tunnels

B. Routing Options

C. Google Compute Engine VPN

D. IKE Version



Answers:

C. The Google Compute Engine VPN is where you specify information about the Google Cloud end of the VPN connection, so option C is correct. You specify name, descrip- tion, network, region, and IP address. Option A is incorrect because tunnels are about the connections between the cloud and the remote network. Option B is incorrect; Routing Options is about how to configure routers. Option D is incorrect; IKE Version is about exchanging secret keys.



#### 18. You want the router on a tunnel you are creating to learn routes from all GCP regions on the network. What feature of GCP routing would you enable?

A. Global dynamic routing

B. Regional routing

C. VPC

D. Firewall rules



Answers:

A. Option A is correct because global dynamic routing is used to learn all routes on a net- work. Option B is incorrect; regional routing would learn only routes in a region. Options C and D are incorrect because they are not used to configure routing options.



#### 19. When you create a cloud router, what kind of unique identifier do you need to assign for the BGP protocol?

A. IP address

B. ASN

C. Dynamic load routing ID&#x20;

D. None of the above



Answers:

B. The autonomous system number (ASN) is a number used to identify a cloud router on a network, so option B is correct. IP addresses are not unique identifiers for the BGP protocol. Option C is incorrect; there is no dynamic load routing ID. Option D is incorrect because option B is correct.



#### 20. You are using gcloud to create a VPN. Which command would you use?&#x20;

A. gcloud compute target-vpn-gateways only

B. gcloud compute forwarding-rule and gcloud compute target-vpn-gateways only

C. gcloud compute vpn-tunnels only

D. gcloud compute forwarding-rule, gcloud compute target-vpn-gateways, and gcloud compute vpn-tunnels



Answers:

D. When using gcloud to create a VPN, you need to create forwarding rules, tunnels, and gateways, so all the gcloud commands listed would be used.

