# Chpt 4. Introduction to Computing in Google Cloud

## Factors to consider when choosing where to run your VM

* Cost, which can vary between regions.&#x20;
* Data locality regulations, such as keeping data about European Union citizens in the European Union.&#x20;
* High availability. If you are running multiple instances, you may want them in different zones and possibly different regions. If one of the zones or regions become inaccessible, the instances in other zones and regions can still provide services.&#x20;
* Latency, which is important if you have users in different parts of the world. Keeping instances and data geographically close to application users can help reduce latency.&#x20;
* Need for specific hardware platforms, which can vary by region. For example, at the time of writing europe-west1 has Intel Xeon E5, also known as Sandy Bridge, platforms, but Europe-west2 does not.

## Preemptible Virtual Machine

* Preemptible VMs are short-lived compute instances suitable for running certain types of workloads— particularly for applications that perform financial modeling, rendering, big data, continuous integration, and web crawling operations.
* These VMs offer the same configuration options as regular compute instances and persist for up to 24 hours.
* If an application is fault-tolerant and can withstand possible instance interruptions (with a 30 second warning), then using preemptible VM instances can reduce Google Compute Engine costs significantly.

## Limitations of Preemptible VM

* May terminate at any time. If they terminate within 10 minutes of starting, you will not be charged for that time.
* Will be terminated within 24 hours.
* May not always be available. Availability may vary across zones and regions.
* Cannot migrate to a regular VM.&#x20;
* Cannot be set to automatically restart.&#x20;
* Are not covered by any service level agreement (SLA).

## App Engine Standard Environment

* It consists of a preconfigured, language-specific runtime.

## App Engine Flexible Environment

* The App Engine flexible environment provides more options and control to developers who would like the benefits of a platform as a service (PaaS) like App Engine, but without the language and customization constraints of the App Engine standard environment

## Kubernetes Engine

* Kubernetes is an open source tool created by Google for administering clusters of virtual and bare-metal machines.
* It allows you to do the following:
  * Create clusters of VMs that run the Kubernetes orchestration software for containers
  * Deploy containerized applications to the cluster&#x20;
  * Administer the cluster&#x20;
  * Specify policies, such as autoscaling&#x20;
  * Monitor cluster health
* Kubernetes is designed to support clusters that run a variety of applications. This is different from other cluster management platforms that provide a way to run one application over multiple servers.
* K8s Engine provides the following functions:
  * Load balancing across Compute Engine VMs that are deployed in a Kubernetes cluster&#x20;
  * Automatic scaling of nodes (VMs) in the cluster&#x20;
  * Automatic upgrading of cluster software as needed&#x20;
  * Node monitoring and health repair&#x20;
  * Logging&#x20;
  * Support for node pools, which are collections of nodes all with the same configuration

## Cloud Functions

* Cloud Functions is a serverless computing platform designed to run single-purpose pieces of code in response to events in the GCP environment.
* There is no need to provision or manage VMs, containers, or clusters when using Cloud Functions.
* Cloud Functions is not a general-purpose computing platform like Compute Engine or App Engine. Cloud Functions provides the “glue” between services that are otherwise independent.
* Use Cases
  * Cloud Functions is well suited to short-running, event-based processing. If your workflows upload, modify, or otherwise alter files in Cloud Storage or use message queues to send work between services, then the Cloud Functions service is a good option for running code that starts the next step in processing.
    * Internet of Things (IoT), in which a sensor or other device can send information about the state of a sensor. Depending on the values sent, Cloud Functions could trigger an alert or start processing data that was uploaded from the sensor.
    * Mobile applications that, like IoT apps, send data to the cloud for processing
    * Asynchronous workflows in which each step starts at some time after the previous steps completes, but there are no assumptions about when the processing steps will complete



