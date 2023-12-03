# Chapter 9. Computing with App Engine

#### 1. You have designed a microservice that you want to deploy to production. Before it can be deployed, you have to review how you will manage the service lifecycle. The architect is particularly concerned about how you will deploy updates to the service with minimal dis- ruption. What aspect of App Engine components would you use to minimize disruptions during updates to the service?

A. Services

B. Versions

C. Instance groups

D. Instances



Answers:

B. Versions support migration. An app can have multiple versions, and by deploying with the --migrate parameter, you can migrate traffic to the new version, so option B is the correct answer. Services are a higher-level abstraction and represent the functionality\
of a microservice. An app may have multiple services, but they serve different purposes. Instances execute code in a version. Instances may be added and removed as needed, but they will run only one version of a service. Instance groups are part of Compute Engine and are not an App Engine component.



#### 2. You’ve just released an application running in App Engine Standard. You notice that there are peak demand periods in which you need up to 12 instances, but most of the time 5 instances are sufficient. What is the best way to ensure that you have enough instances to meet demand without spending more than you have to?

A. Configure your app for autoscaling and specify max instances of 12 and min instances of 5.

B. Configure your app for basic scaling and specify max instances of 12 and min instances of 5.

C. Create a cron job to add instances just prior to peak periods and remove instances after the peak period is over.

D. Configure your app for instance detection and do not specify a max or minimum num- ber of instances.



Answers:

A. Autoscaling enables setting a maximum and minimum number of instances, which makes option A correct. Basic scaling does not support maximum and minimum instances. Option C is not recommended because it is difficult to predict when load will peak and even if the schedule is predictable today, it may change over time. Option D is wrong; there is no instance detection option.



#### 3. In the hierarchy of App Engine components, what is the lowest-level component?&#x20;

A. Application

B. Instance&#x20;

C. Version&#x20;

D. Service



Answers:

B. Application is the top-level component, so option B is the correct answer. Applications have one or more services. Services have one or more versions. Versions are executed on one or more instances when the application is running.



#### 4. What command should you use to deploy an App Engine app from the command line?&#x20;

A. gcloud components app deploy

B. gcloud app deploy

C. gcloud components instances deploy

D. gcloud app instance deploy



Answers:

B. The correct command is gcloud app deploy, which is option B. Options A and C are incorrect because gcloud components commands are used to install gcloud commands for working with parts of App Engine, such as the Python runtime environment. Option D is incorrect; you do not need to specify instance in the command.



#### 5. You have deployed a Django 1.5 Python application to App Engine. This version of Django requires Python 3. For some reason, App Engine is trying to run the application using Python 2. What file would you check and possibly modify to ensure that Python 3 is used with this application?

A. app.config

B. app.yaml

C. services.yaml&#x20;

D. deploy.yaml



Answers:

B. The app.yaml file is used to configure an App Engine application, which makes option B correct. The other options are not files used to configure App Engine.



#### 6. You have several App Engine apps you plan to deploy from your project. What have you failed to account for in this design?

A. App Engine only supports one app per project.&#x20;

B. App Engine only supports two apps per project.&#x20;

C. App Engine apps exist outside of projects.

D. Nothing, this is a common pattern.



Answers:

A. A project can support only one App Engine app, so option A is the right answer. If you’d like to run other applications, they will need to be placed in their own projects.



#### 7. The latest version of your microservice code has been approved by your manager, but the product owner does not want the new features released until a press release is published. You’d like to get the code out but not expose it to customers. What is the best way to get the code out as soon as possible without exposing it to customers?

A. Deploy with gcloud app deploy --no-traffic.

B. Write a cron job to deploy after the press release is published.

C. Deploy with gcloud app deploy --no-promote.

D. Deploy as normal after the press release is published.



Answers:

C. The correct answer is option C because the correct parameter is --no-promote. Option A uses no-traffic, which is not a valid parameter to the gcloud app deploy command. Option B does not get the code out and could release the code too early if there is a delay in getting the press release out. Option D does not meet the requirements of getting the code out as soon as possible.



#### 8. You have just deployed an app that hosts services that provide the current time in any time zone. The project containing the code is called current-time-zone, the service providing the user interface is called time-zone-ui, and the service performing the calculation is called time-zone-calculate. What is the URL where a user could find your service?

A. current-time-zone.appengine.com&#x20;

B. current-time-zone.appspot.com&#x20;

C. time-zone-ui.appspot.com

D. time-zone-calculate.appspot.com



Answers:

B. App Engine applications are accessible from URLs that consist of the project name fol- lowed by appspot.com, so option B is correct. Option A is incorrect because the domain is not appengine.com. Options C and D are incorrect because the names of services are not used to reference the application as a whole.



#### 9. You are concerned that as users make connections to your application, the performance will degrade. You want to make sure that more instances are added to your App Engine application when there are more than 20 concurrent requests. What parameter would you specify in app.yaml?

A. max\_concurrent\_requests

B. target\_throughput\_utilization&#x20;

C. max\_instances

D. max\_pending\_latency



Answers:

A. max\_concurrent\_requests lets you specify the maximum number of concurrent requests before another instance is started, which makes option A correct. target\_ throughput\_utilization functions similarly but uses a 0.05 to 0.95 scale to specify max- imum throughput utilization. max\_instances specifies the maximum number of instances but not the criteria for adding instances. max\_pending\_latency is based on the time a request waits, not the number of requests.



#### 10. What parameters can be configured with basic scaling?

A. max\_instances and min\_instances

B. idle\_timeout and min\_instances

C. idle\_timeout and max\_instances

D. idle\_timeout and target\_throughput\_utilization



Answers:

C. Basic scaling only allows for idle time and maximum instances, so option C is the right answer. min\_instances is not supported. target\_throughput\_utilization is an auto- scaling parameter, not a basic scaling parameter.



#### 11. The runtime parameter in app.yaml is used to specify what?

A. The script to execute

B. The URL to access the application

C. The language runtime environment

D. The maximum time an application can run



Answers:

C. The runtime parameter specifies the language environment to execute in, which makes option C correct. The script to execute is specified by the script parameter. The URL to access the application is based on the project name and the domain appspot.com. There is no parameter for specifying the maximum time an application can run.



#### 12. What are the two kinds of instances available in App Engine Standard?

A. Resident and dynamic

B. Persistent and dynamic

C. Stable and dynamic

D. Resident and nonresident



Answers:

A. Resident instances are used with manual scaling while dynamic instances are used with autoscaling and basic scaling, so option A is the correct answer. There are no persistent, stable, or nonresident types of App Engine instances.



#### 13. You work for a startup, and costs are a major concern. You are willing to take a slight per- formance hit if it will save you money. How should you configure the scaling for your apps running in App Engine?

A. Use dynamic instances by specifying autoscaling or basic scaling.

B. Use resident instances by specifying autoscaling or basic scaling.

C. Use dynamic instances by specifying manual scaling.

D. Use resident instances by specifying manual scaling.



Answers:

A. Using dynamic instances by specifying autoscaling or basic scaling will automatically adjust the number of instances in use based on load, so option A is correct. Option B is incorrect because autoscaling and basic scaling only create dynamic instances. Options C and D are incorrect because manual scaling will not adjust instances automatically, so you may continue to run more instances than needed at some points.



#### 14. A team of developers has created an optimized version of a service. This should run 30 percent faster in most cases. They want to roll it out to all users immediately, but you are concerned that the substantial changes need to be released slowly in case there are significant bugs. What can you do to allocate some users to the new version without exposing all users to it?

A. Issue the command gcloud app services set-traffic.

B. Issue the command gcloud instances services set-traffic.

C. Issue the command gcloud app set-traffic.

D. Change the target IP address of the service for some clients.



Answers:

A. The correct answer is gcloud app services set-traffic. Option B is incorrect because the term instances is not needed. Option C is incorrect because it does not specify the term services. Option D is incorrect because that would require changes on the client’s part.



#### 15. What parameter to gcloud app services set-traffic is used to specify the method to use when splitting traffic?

A. ––split-traffic&#x20;

B. ––split-by

C. ––traffic-split&#x20;

D. ––split-method



Answers:

A. --split-traffic is the parameter used to specify the method for splitting traffic, which makes option A correct. Valid options are cookie, ip, and random. All other options are not valid parameters to the gcloud app services set-traffic command.



#### 16. What parameter to gcloud app services set-traffic is used to specify the percentage of traffic that should go to each instance?

A. ––split-by

B. ––splits

C. ––split-percent&#x20;

D. ––percent-split



Answers:

B. --split is the parameter for specifying a list of instances and the percent of traffic they should receive, so option B is the right answer. The other options are not valid parameters for the gcloud app services set-traffic command.



#### 17. You have released a new version of a service. You have been waiting for approval from the product manager to start sending traffic to the new version. You get approval to route traf- fic to the new version. What parameter to gcloud app services set-traffic is used to specify that traffic should be moved to a newer version of the app?

A. ––move-to-new

B. ––migrate-to-new&#x20;

C. ––migrate

D. ––move



Answers:

C. --migrate is the parameter for specifying that traffic should be moved or migrated to the newer instance, which makes option C the correct answer. The other options are not valid parameters for the gcloud app services set-traffic command.



#### 18. The status of what components can be viewed in the App Engine console?&#x20;

A. Services only

B. Versions only

C. Instances and versions

D. Services, versions, and instances



Answers:

D. From the App Engine console you can view the list of services and versions as well as information about the utilization of each instance.



#### 19. What are valid methods for splitting traffic?

A. By IP address only

B. By HTTP cookie only

C. Randomly and by IP address only

D. By IP address, HTTP cookies, and randomly



Answers:

D. All three methods listed, IP address, HTTP cookie, and random splitting, are allowed methods for splitting traffic.



#### 20. What is the name of the cookie used by App Engine when cookie-based splitting is used?&#x20;

A. GOOGID

B. GOOGAPPUID&#x20;

C. APPUID

D. UIDAPP



Answers:

B. The cookie used for splitting in App Engine is called GOOGAPPUID, which makes option B the correct answer. Options A, C, and D are not valid names.

