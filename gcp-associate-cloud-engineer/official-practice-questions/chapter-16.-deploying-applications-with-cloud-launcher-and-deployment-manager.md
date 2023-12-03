# Chapter 16. Deploying Applications with Cloud Launcher and Deployment Manager

#### 1. What are the categories of Cloud Launcher solutions?

A. Data sets only

B. Operating systems only

C. Developer tools and operating systems only

D. Data sets, operating systems, and developer tools



Answers:

D. Categories of solutions include all of the categories mentioned, so option D is correct. Others include Kubernetes Apps, API & Services, and Databases.



#### 2. What is the other name of Cloud Launcher?

A. Cloud Deployment Manager

B. Marketplace

C. Cloud Tools

D. Cloud Solutions: Third Party



Answers:

B. The Cloud Launcher is also known as Marketplace, so option B is correct. Option A is incorrect because the Cloud Deployment Manager is used to create deployment templates. Options C and D are fictional names of services.



#### 3. Where do you navigate to launch a Cloud Launcher solution?&#x20;

A. Overview page of the solution

B. Main Cloud Launcher page

C. Network Services

D. None of the above



Answers:

A. You launch a solution by clicking the Launch on Compute Engine link in the overview page, so option A is correct. Option B is incorrect; the main page has summary informa- tion about the products. Option C is incorrect; Network Services is unrelated to this topic. Option D is incorrect because option A is the correct answer.



#### 4. You want to quickly identify the set of operating systems available in Cloud Launcher. Which of these steps would help with that?

A. Use Google Search to search the Web for a listing.

B. Use filters in Cloud Launcher.

C. Scroll through the list of solutions displayed on the start page of Cloud Launcher.&#x20;

D. It is not possible to filter to operating systems.



Answers:

B. Cloud Launcher has a set of predefined filters, including filtering by operating system, so option B is correct. Option A may eventually lead to the correct information, but it is not efficient. Option D is incorrect because it is impractical for such a simple task.



#### 5. You want to use Cloud Launcher to deploy a WordPress site. You notice there is more than one WordPress option. Why is that?

A. It’s a mistake. Submit a ticket to Google support.&#x20;

B. Multiple vendors may offer the same application.&#x20;

C. It’s a mistake. Submit a ticket to the vendors.

D. You will never see such an option.



Answers:

B. Multiple vendors may offer configurations for the same applications, so option B is cor- rect. This gives users the opportunity to choose the one best suited to their requirements. Options A and C are incorrect; this is a feature of Cloud Launcher. Option D is incorrect because option B is the correct answer.



#### 6. You have used Cloud Launcher to deploy a WordPress site and would now like to deploy a database. You notice that the configuration form for the databases is different from the form used with WordPress. Why is that?

A. It’s a mistake. Submit a ticket to Google support.

B. You’ve navigated to a different subform of Cloud Launcher.

C. Configuration properties are based on the application you are deploying and will be different depending on what application you are deploying.

D. This cannot happen.



Answers:

C. Cloud Launcher will display configuration options appropriate for the application you are deploying, so option C is correct. For example, when deploying WordPress, you will have the option of deploying an administration tool for PHP. Option A is incorrect; this is a feature of Cloud Launcher. Option B is incorrect; you are not necessarily on the wrong form. Option D is incorrect; this is a feature of Cloud Launcher.



#### 7. You have been asked by your manager to deploy a WordPress site. You expect heavy traf- fic, and your manager wants to make sure the VM hosting the WordPress site has enough resources. Which resources can you configure when launching a WordPress site using Cloud Launcher?

A. Machine type&#x20;

B. Disk type

C. Disk size

D. All of the above



Answers:

D. You can change the configuration of any of the items listed, so option D is correct. You can also specify firewall rules to allow both HTTP and HTTPS traffic or change the zone in which the VM runs.



#### 8. You would like to define as code the configuration of a set of application resources. The GCP service for creating resources using a configuration file made up of resource specifica- tions defined in YAML syntax is called what?

A. Compute Engine

B. Deployment Manager

C. Marketplace Manager

D. Marketplace Deployer



Answers:

B. Deployment Manager is the name of the service for creating application resources using a YAML configuration file, so option B is correct. Option A is incorrect, although you could use scripts with gcloud commands to deploy resources in Compute Engine. Options C and D are incorrect because those are fictitious names of products.



#### 9. What file format is used to define Deployment Manager configuration files?&#x20;

A. XML

B. JSON&#x20;

C. CSV&#x20;

D. YAML



Answers:

D. Configuration files are defined in YAML syntax, so option D is correct. Options A, B, and C are all incorrect; configuration files are defined in YAML.



#### 10. A Deployment Manager configuration file starts with what term?&#x20;

A. Deploy

B. Resources&#x20;

C. Properties&#x20;

D. YAML



Answers:

B. Configuration files define resources and start with the term resources, so option B is cor- rect. Options A, B, and C are all incorrect. Those terms do not start the configuration file.



#### 11. Which of the following are used to define a resource in a Cloud Deployment Manager con- figuration file?

A. type only

B. properties only

C. name and type only

D. type, properties, and name



Answers:

D. All three, type, properties, and name, are used when defining resources in a Cloud Deployment Manager configuration file, so option D is correct.



#### 12. What properties may be set when defining a disk on a VM?

A. A device name only

B. A Boolean indicating a boot disk and a Boolean indicating autodelete

C. A Boolean indicating autodelete only

D. A device name, a Boolean indicating a boot disk, and a Boolean indicating autodelete



Answers:

D. All three can be set; specifically, the keys are deviceName, boot, and autodelete. Option D is correct.



#### 13. You need to look up what images are available in the zone in which you want to deploy a VM. What command would you use?

A. gcloud compute images list&#x20;

B. gcloud images list

C. gsutil compute images list&#x20;

D. gcloud compute list images



Answers:

A. Option A is the correct command. Option B is incorrect; it is missing the term compute. Option C is incorrect; gsutil is the command for working with Cloud Storage. Option D is incorrect because the terms list and images are in the wrong order.



#### 14. You want to use a template file with Deployment Manager. You expect the file to be complicated. What language would you use?

A. Jinja2&#x20;

B. Ruby&#x20;

C. Go

D. Python



Answers:

D. Google recommends using Python for complicated templates, so option D is correct. Option A is incorrect because Jinja2 is recommended only for simple templates. Options B and C are incorrect; neither language is supported for templates.



#### 15. What command launches a deployment?

A. gcloud deployment-manager deployments create&#x20;

B. gcloud cloud-launcher deployments create

C. gcloud deployment-manager deployments launch&#x20;

D. gcloud cloud-launcher deployments launch



Answers:

A. The correct answer is gcloud deployment-manager deployments create, so option A is correct. Options B and D are incorrect; the service is not called cloud-launcher in the command. Option C is incorrect; launch is not a valid verb for this command.



#### 16. A DevOps engineer is noticing a spike in CPU utilization on your servers. You explain you have just launched a deployment. You’d like to show the DevOps engineer the details of a deployment you just launched. What command would you use?

A. gcloud cloud-launcher deployments describe

B. gcloud deployment-manage deployments list

C. gcloud deployment-manager deployments describe&#x20;

D. gcloud cloud-launcher deployments list



Answers:

C. The correct answer is gcloud deployment-manager deployments describe, so option C is correct. Options A and D are incorrect; cloud-launcher is not the name of the service. Option B is incorrect; list displays a brief summary of each deployment. describe displays a detailed description.



#### 17. If you expand the More link in the Networking section when deploying a Cloud Launcher solution, what will you be able to configure?

A. IP addresses

B. Billing

C. Access controls

D. Custom machine type



Answers:

A. You will be able to configure IP addresses, so option A is correct. You cannot configure billing or access controls in Deployment Manager, so options B and C are incorrect. You can configure the machine type, but that is not the More section of Networking.



#### 18. What are the license types referenced in Cloud Launcher?

A. Free only

B. Free and Paid only

C. Free and Bring your own license (BYOL) only

D. Free, paid, and bring your own license



Answers:

D. The correct answer is option D because free, paid, and BYOL are all license options used in Cloud Launcher.



#### 19. Which license type will add charges to your GCP bill when using Cloud Launcher with this type of license?&#x20;

A. Free

B. Paid

C. BYOL

D. Chargeback



Answers:

B. The paid license types include payment for the license in your GCP charges, so option B is correct. The free license type does not incur charges. The BYOL license type requires you to work with the software vendor to get and pay for a license. There is no such license type as chargeback, so option D is incorrect.



#### 20. You are deploying a Cloud Launcher application that includes a LAMP stack. What soft-ware will this deploy?

A. Apache server and Linux only

B. Linux only

C. MySQL and Apache only

D. Apache, MySQL, Linux, and PHP



Answers:

D. LAMP is short for Linux, Apache, MySQL, and PHP. All are included when installing LAMP solutions, so option D is correct.

