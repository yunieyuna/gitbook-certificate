# Chapter 15. Networking in the Cloud: DNS, Load Balancing, and IP Addressing

#### 1. What record type is used to specify the IPv4 address of a domain?&#x20;

A. AAAA

B. A

C. NS&#x20;

D. SOA



Answers:

B. The A record is used to map a domain name to an IPv4 address, so option B is correct. Option A is incorrect because the AAAA record is used for IPv6 addresses. Option C is incorrect; NS is a name server record. Option D is incorrect; SOA is a start of authority record.



#### 2. The CEO of your startup just read a news report about a company that was attacked by something called cache poisoning. The CEO wants to implement additional security measures to reduce the risk of DNS spoofing and cache poisoning. What would you recommend?

A. Using DNSSEC

B. Adding SOA records

C. Adding CNAME records

D. Deleting CNAME records



Answers:

A. DNSSEC is a secure protocol designed to prevent spoofing and cache poisoning, so option A is correct. Options B and C are incorrect because SOA and CNAME records con- tain data about the DNS record; they are not an additional security measure. Option D is incorrect because deleting a CNAME record does not improve security.



#### 3. What do the TTL parameters specify in a DNS record?

A. Time a record can exist in a cache before it should be queried again

B. Time a client has to respond to a request for DNS information

C. Time allowed to create a CNAME record

D. Time before a human has to manually verify the information in the DNS record



Answers:

A. The TTL parameters specify the time a record can be in a cache before the data should be queried again, so option A is correct. Option B is incorrect; this time period is not related to timeouts. Option C is incorrect; the TTLs are not related to time restriction on data change operations. Option D is not correct; there is no manual review required.



#### 4. What command is used to create a DNS zone in the command line?&#x20;

A. gsutil dns managed-zones create

B. gcloud beta dns managed-zones create

C. gcloud beta managed-zones create

D. gcloud beta dns create managed zones



Answers:

B. The correct answer, Option B, is gcloud beta dns managed-zones create. Option A is incorrect, it uses the gsutil command which is used to work with Cloud Storage. Option C is incorrect, it is missing the term dns. Option D is incorrect, the ordering of terms is incorrect.



#### 5. What parameter is used to make a DNS zone private?&#x20;

A. --private

B. --visibility=private&#x20;

C. --private=true

D. --status=private



Answers:

B. The visibility parameter is the parameter that can be set to private, so option B is correct. Option A is not a valid parameter. Option C is incorrect; private is not a parameter. Similarly, option D is incorrect; status is not a valid parameter for making a DNS zone private.



#### 6. Which load balancers provide global load balancing?

A. HTTP(S) only

B. SSL Proxy and TCP Proxy only

C. HTTP(S), SSL Proxy, and TCP Proxy

D. Internal TCP/UDP, HTTP(S), SSL Proxy, and TCP Proxy



Answers:

C. The three global load balancers are HTTP(S), SSL Proxy, and TCP Proxy, so option C\
is correct. Options A and B are missing at least one global load balancer. Option D is incor- rect because Internal TCP/UD is a regional load balancer.



#### 7. Which regional load balancer allows for load balancing based on IP protocol, address,and port?

A. HTTP(S)

B. SSL Proxy

C. TCP Proxy

D. Network TCP/UDP



Answers:

D. Network TCP/UDP enables balancing based on IP protocol, address, and port, so option D is correct. Options A, B, and C are all global load balancers, not regional ones.



#### 8. You are configuring a load balancer and want to implement private load balancing. Which option would you select?

A. Only Between My VMs

B. Enable Private

C. Disable Public

D. Local Only



Answers:

A. In the console there is an option to select between From Internet To My VMs and Only Between My VMs. This is the option to indicate private or public, so option A is correct. Options B, C, and D are all fictitious parameters.



#### 9. What two components need to be configured when creating a TCP Proxy load balancer?

A. Frontend and forwarding rule

B. Frontend and backend

C. Forwarding rule and backend only

D. Backend and forwarding rule only



Answers:

B. TCP Proxy load balancers require you to configure both the frontend and backendthe , so option B is correct. Options A and D are incorrect because they are missing one compo- nent. Option C is incorrect; forwarding rules are the one component specified with network load balancing. There is no component known as a traffic rule.



#### 10. A health check is used to check what resources?

A. Load balancer

B. VMs

C. Storage buckets

D. Persistent disks



Answers:

B. Health checks monitor the health of VMs used with load balancers, so option B is correct. Option A is incorrect, nearline storage is a type of Cloud Storage. Option C and D are incorrect; storage devices or buckets are not health checked.



#### 11. Where do you specify the ports on a TCP Proxy load balancer that should have their traffic forwarded?

A. Backend

B. Frontend

C. Network Services section

D. VPC



Answers:

B. You specify ports to forward when configuring the frontend, so option B is correct. The backend is where you configure how traffic is routed to VMs. Option C is incorrect; Net- work Services is a high-level area of the console. Option D is incorrect; VPCs are not where you specify load balancer configurations.



#### 12. What command is used to create a network load balancer at the command line?&#x20;

A. gcloud compute forwarding-rules create

B. gcloud network forwarding-rules create

C. gcloud compute create forwarding-rules

D. gcloud network create forwarding-rules



Answers:

A. The correct answer, option A, is gcloud compute forwarding-rules create. Option B is incorrect; the service should be compute, not network. Option C is incorrect; create comes after forwarding-rules. Option D is incorrect because it has the wrong service, and the verb is in the wrong position.



#### 13. A team is setting up a web service for internal use. They want to use the same IP address for the foreseeable future. What type of IP address would you assign?&#x20;

A. Internal

B. External

C. Static

D. Ephemeral



Answers:

C. Static addresses are assigned until they are released, so option C is correct. Options A and B are incorrect because internal and external addresses determine whether traffic is routed into and out of the subnet. External addresses can have traffic reach them from the Internet; internal addresses cannot. Option D is incorrect; ephemeral addresses are released when a VM shuts down or is deleted.



#### 14. You are starting up a VM to experiment with a new Python data science library. You’ll SSH via the server name into the VM, use the Python interpreter interactively for a while and then shut down the machine. What type of IP address would you assign to this VM?

A. Ephemeral&#x20;

B. Static

C. Permanent&#x20;

D. IPv8



Answers:

A. An ephemeral address is sufficient, since resources outside the subnet will not need\
to reach the VM and you can SSH into the VM from the console, so option A is correct. Option B is incorrect because there is no need to assign a permanent address, which would then have to be released. Option C is incorrect; there is no Permanent type. Option D is incorrect; there is no IPv8 address.



#### 15. You have created a subnet called sn1 using 192.168.0.0 with 65,534 addresses. You realize that you will not need that many addresses, and you’d like to reduce that number to 254. Which of the following commands would you use?

A. gcloud compute networks subnets expand-ip-range sn1 --prefix-length=24

B. gcloud compute networks subnets expand-ip-range sn1 --prefix-length=-8

C. gcloud compute networks subnets expand-ip-range sn1 --size=256

D. There is no command to reduce the number of IP addresses available.



Answers:

D. You cannot reduce the number of addresses using any of the commands, so option D is correct. Option A is incorrect because the prefix length specified in the expand-ip-range command must be a number less than the current length. If there are 65,534 addresses, then the prefix length is 16. Option B is incorrect for the same reason, and the prefix length cannot be a negative number. Option C is incorrect; there is no ––size parameter.



#### 16. You have created a subnet called sn1 using 192.168.0.0. You want it to have 14 addresses. What prefix length would you use?

A. 32&#x20;

B. 28&#x20;

C. 20&#x20;

D. 16



Answers:

B. The prefix length specifies the length in bits of the subnet mask. The remaining bits of the IP address are used for device addresses. Since there are 32 bits in an IP address, you subtract the length of the mask to get the number of bits used to represent the address. 16 is equal to 24, so you need 4 bits to represent 14 addresses. 32-4 is 28, so option B is the cor- rect answer. Option A would leave 1 address, option C would provide 4,094 addresses, and option D would provide 65,534.



#### 17. You want all your network traffic to route over the Google network and not traverse the public Internet. What level of network service should you choose?

A. Standard

B. Google-only&#x20;

C. Premium

D. Non-Internet



Answers:

C. Premium is the network service level that routes all traffic over the Google network, so option C is correct. Option A is incorrect; the Standard tier may use the public Inter- net when routing traffic. Options B and D are incorrect; there are no service tiers called Google-only or non-Internet.



#### 18. You have a website hosted on a Compute Engine VM. Users can access the website using the domain name you provided. You do some maintenance work on the VM and stop the server and restart it. Now users cannot access the website. No other changes have occurred on the subnet. What might be the cause of the problem?

A. The restart caused a change in the DNS record.

B. You used an ephemeral instead of a static IP address.

C. You do not have enough addresses available on your subnet.&#x20;

D. Your subnet has changed.



Answers:

B. Stopping and starting a VM will release ephemeral IP addresses, so option B is correct. Use a static IP address to have the same IP address across reboots. Option A is incorrect; rebooting a VM does not change a DNS record. Option C is incorrect because if you had enough addresses to get an address when you first started the VM and you then released that IP address, there should be at least one IP address assuming no other devices are added to the subnet. Option D is incorrect because no other changes, including changes to the subnet, were made.



#### 19. You are deploying a distributed system. Messages will be passed between Compute Engine VMs using a reliable UDP protocol. All VMs are in the same region. You want to use the load balancer that best fits these requirements. Which kind of load balancer would you use?

A. Internal TCP/UDP&#x20;

B. TCP Proxy

C. SSL Proxy

D. HTTP(S)



Answers:

A. Internal TCP/UDP is a good option. It is a regional load balancer that supports UDP, so option A is correct. Options B, C, and D are all global load balancers. Option B supports TCP, not UDP. Option D supports HTTP and HTTPS, not UDP.



#### 20. You want to use Cloud Console to review the records in a DNS entry. What section of Cloud Console would you navigate to?

A. Compute Engine

B. Network Services

C. Kubernetes Engine

D. Hybrid Connectivity



Answers:

B. Network Services is the section of Cloud Console that has the Cloud DNS console, so option B is correct. Option A is incorrect; Compute Engine does not have DNS manage- ment forms. Neither does option C, Kubernetes Engine. Option D is related to networking, but the services in Hybrid Connectivity are for services such as VPNs.

