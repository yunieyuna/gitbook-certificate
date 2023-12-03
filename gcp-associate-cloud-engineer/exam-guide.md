# Exam Guide

## **Section 1: Setting up a cloud solution environment**

### 1.1 Setting up cloud projects and accounts. Activities include:

&#x20;   ●  Creating a resource hierarchy

&#x20;   ●  Applying organizational policies to the resource hierarchy

&#x20;   ●  Granting members IAM roles within a project

&#x20;   ●  Managing users and groups in Cloud Identity (manually and automated)

&#x20;   ●  Enabling APIs within projects

&#x20;   ●  Provisioning and setting up products in Google Cloud’s operations suite

### 1.2 Managing billing configuration. Activities include:

&#x20;   ●  Creating one or more billing accounts

&#x20;   ●  Linking projects to a billing account

&#x20;   ●  Establishing billing budgets and alerts

&#x20;   ●  Setting up billing exports

### 1.3 Installing and configuring the command line interface (CLI), specifically the Cloud SDK (e.g., setting the default project).



## **Section 2: Planning and configuring a cloud solution**

### 2.1 Planning and estimating Google Cloud product use using the Pricing Calculator

### 2.2 Planning and configuring compute resources. Considerations include:

&#x20;   ●  Selecting appropriate compute choices for a given workload (e.g., Compute Engine, Google Kubernetes Engine, Cloud Run, Cloud Functions)

&#x20;   ●  Using preemptible VMs and custom machine types as appropriate

### 2.3 Planning and configuring data storage options. Considerations include:

&#x20;   ●  Product choice (e.g., Cloud SQL, BigQuery, Firestore, Cloud Spanner, Cloud Bigtable)

&#x20;   ●  Choosing storage options (e.g., Zonal persistent disk, Regional balanced persistent disk, Standard, Nearline, Coldline, Archive)

### 2.4 Planning and configuring network resources. Tasks include:

&#x20;   ●  Differentiating load balancing options

&#x20;   ●  Identifying resource locations in a network for availability

&#x20;   ●  Configuring Cloud DNS



## **Section 3: Deploying and implementing a cloud solution**

### 3.1 Deploying and implementing Compute Engine resources. Tasks include:

&#x20;   ●  Launching a compute instance using the Google Cloud console and Cloud SDK (gcloud) (e.g., assign disks, availability policy, SSH keys)

&#x20;   ●  Creating an autoscaled managed instance group using an instance template

&#x20;   ●  Generating/uploading a custom SSH key for instances

&#x20;   ●  Installing and configuring the Cloud Monitoring and Logging Agent

&#x20;   ●  Assessing compute quotas and requesting increases

### 3.2 Deploying and implementing Google Kubernetes Engine resources. Tasks include:

&#x20;   ●  Installing and configuring the command line interface (CLI) for Kubernetes (kubectl)

&#x20;   ●  Deploying a Google Kubernetes Engine cluster with different configurations including AutoPilot, regional clusters, private clusters, etc.

&#x20;   ●  Deploying a containerized application to Google Kubernetes Engine

&#x20;   ●  Configuring Google Kubernetes Engine monitoring and logging

### 3.3 Deploying and implementing Cloud Run and Cloud Functions resources. Tasks include, where applicable:

&#x20;   ●  Deploying an application and updating scaling configuration, versions, and traffic splitting

&#x20;   ●  Deploying an application that receives Google Cloud events (e.g., Pub/Sub events, Cloud Storage object change notification events)

### 3.4 Deploying and implementing data solutions. Tasks include:

&#x20;   ●  Initializing data systems with products (e.g., Cloud SQL, Firestore, BigQuery, Cloud Spanner, Pub/Sub, Cloud Bigtable, Dataproc, Dataflow, Cloud Storage)

&#x20;   ●  Loading data (e.g., command line upload, API transfer, import/export, load data from Cloud Storage, streaming data to Pub/Sub)

### 3.5 Deploying and implementing networking resources. Tasks include:

&#x20;   ●  Creating a VPC with subnets (e.g., custom-mode VPC, shared VPC)

&#x20;   ●  Launching a Compute Engine instance with custom network configuration (e.g., internal-only IP address, Google private access, static external and private IP address, network tags)

&#x20;   ●  Creating ingress and egress firewall rules for a VPC (e.g., IP subnets, network tags, service accounts)

&#x20;   ●  Creating a VPN between a Google VPC and an external network using Cloud VPN

&#x20;   ●  Creating a load balancer to distribute application network traffic to an application (e.g., Global HTTP(S) load balancer, Global SSL Proxy load balancer, Global TCP Proxy load balancer, regional network load balancer, regional internal load balancer)

### 3.6 Deploying a solution using Cloud Marketplace. Tasks include:

&#x20;   ●  Browsing the Cloud Marketplace catalog and viewing solution details

&#x20;   ●  Deploying a Cloud Marketplace solution

### 3.7 Implementing resources via infrastructure as code. Tasks include:

&#x20;   ●  Building infrastructure via Cloud Foundation Toolkit templates and implementing best practices

&#x20;   ●  Installing and configuring Config Connector in Google Kubernetes Engine to create, update, delete, and secure resources



## **Section 4: Ensuring successful operation of a cloud solution**

### 4.1 Managing Compute Engine resources. Tasks include:

&#x20;   ●  Managing a single VM instance (e.g., start, stop, edit configuration, or delete an instance)

&#x20;   ●  Remotely connecting to the instance

&#x20;   ●  Attaching a GPU to a new instance and installing necessary dependencies

&#x20;   ●  Viewing current running VM inventory (instance IDs, details)

&#x20;   ●  Working with snapshots (e.g., create a snapshot from a VM, view snapshots, delete a snapshot)

&#x20;   ●  Working with images (e.g., create an image from a VM or a snapshot, view images, delete an image)

&#x20;   ●  Working with instance groups (e.g., set autoscaling parameters, assign instance template, create an instance template, remove instance group)

&#x20;   ●  Working with management interfaces (e.g., Google Cloud console, Cloud Shell, Cloud SDK)

### 4.2 Managing Google Kubernetes Engine resources. Tasks include:

&#x20;   ●  Viewing current running cluster inventory (nodes, pods, services)

&#x20;   ●  Browsing Docker images and viewing their details in the Artifact Registry

&#x20;   ●  Working with node pools (e.g., add, edit, or remove a node pool)

&#x20;   ●  Working with pods (e.g., add, edit, or remove pods)

&#x20;   ●  Working with services (e.g., add, edit, or remove a service)

&#x20;   ●  Working with stateful applications (e.g. persistent volumes, stateful sets)

&#x20;   ●  Managing Horizontal and Vertical autoscaling configurations

&#x20;   ●  Working with management interfaces (e.g., Google Cloud console, Cloud Shell, Cloud SDK, kubectl)

### 4.3 Managing Cloud Run resources. Tasks include:

&#x20;   ●  Adjusting application traffic-splitting parameters

&#x20;   ●  Setting scaling parameters for autoscaling instances

&#x20;   ●  Determining whether to run Cloud Run (fully managed) or Cloud Run for Anthos

### 4.4 Managing storage and database solutions. Tasks include:

&#x20;   ●  Managing and securing objects in and between Cloud Storage buckets

&#x20;   ●  Setting object life cycle management policies for Cloud Storage buckets

&#x20;   ●  Executing queries to retrieve data from data instances (e.g., Cloud SQL, BigQuery, Cloud Spanner, Datastore, Cloud Bigtable)

&#x20;   ●  Estimating costs of data storage resources

&#x20;   ●  Backing up and restoring database instances (e.g., Cloud SQL, Datastore)

&#x20;   ●  Reviewing job status in Dataproc, Dataflow, or BigQuery

### 4.5 Managing networking resources. Tasks include:

&#x20;   ●  Adding a subnet to an existing VPC

&#x20;   ●  Expanding a subnet to have more IP addresses

&#x20;   ●  Reserving static external or internal IP addresses

&#x20;   ●  Working with CloudDNS, CloudNAT, Load Balancers and firewall rules

### 4.6 Monitoring and logging. Tasks include:

&#x20;   ●  Creating Cloud Monitoring alerts based on resource metrics

&#x20;   ●  Creating and ingesting Cloud Monitoring custom metrics (e.g., from applications or logs)

&#x20;   ●  Configuring log sinks to export logs to external systems (e.g., on-premises or BigQuery)

&#x20;   ●  Configuring log routers

&#x20;   ●  Viewing and filtering logs in Cloud Logging

&#x20;   ●  Viewing specific log message details in Cloud Logging

&#x20;   ●  Using cloud diagnostics to research an application issue (e.g., viewing Cloud Trace data, using Cloud Debug to view an application point-in-time)

&#x20;   ●  Viewing Google Cloud status



## **Section 5: Configuring access and security**

### 5.1 Managing Identity and Access Management (IAM). Tasks include:

&#x20;   ●  Viewing IAM policies

&#x20;   ●  Creating IAM policies

&#x20;   ●  Managing the various role types and defining custom IAM roles (e.g., primitive, predefined and custom)

### 5.2 Managing service accounts. Tasks include:

&#x20;   ●  Creating service accounts

&#x20;   ●  Using service accounts in IAM policies with minimum permissions

&#x20;   ●  Assigning service accounts to resources

&#x20;   ●  Managing IAM of a service account

&#x20;   ●  Managing service account impersonation

&#x20;   ●  Creating and managing short-lived service account credentials

### 5.3 Viewing audit logs
