# Chapter 18. Monitoring, Logging, and Cost Estimating

#### 1. What Stackdriver service is used to generate alerts when the CPU utilization of a VM exceeds 80 percent?

A. Logging

B. Monitoring&#x20;

C. Cloud Trace&#x20;

D. Cloud Debug



Answers:

B. The Monitoring service is used to set a threshold on metrics and generate alerts when a metric exceeds the threshold for a specified period of time, so option B is correct. Option A is incorrect; Logging is for collecting logged events. Option C is incorrect; Cloud Trace is for application tracing. Option D is incorrect; Debug is used to debug applications.



#### 2. You have just created a virtual machine, and you’d like Stackdriver Monitoring to alert you via email whenever the CPU average utilization exceeds 75 percent for 5 minutes. What do you need to do to the VM to have this happen?

A. Install a Stackdriver workspace

B. Install the Stackdriver monitoring agent on the VM

C. Edit the VM configuration in Cloud Console and check the Monitor With Stackdriver checkbox

D. Set a notification channel



Answers:

B. You must install the monitoring agent on the VM. The agent will collect data and send it to Stackdriver, so option B is correct. Option A is incorrect because a Workspace is not installed on a VM; it is created in Stackdriver. Option C is incorrect; there is no Monitor With Stackdriver check box in the VM configuration form. Option D is incorrect because you set notification channels in Stackdriver, not on a VM.



#### 3. Stackdriver can be used to monitor resources where?

A. In Google Cloud Platform only

B. In Google Cloud Platform and Amazon Web Services only

C. In Google Cloud Platform and on premises data centers

D. In Google Cloud Platform, Amazon Web Services, and on premises data centers



Answers:

D. Stackdriver can monitor resources in GCP, AWS, and in on-premise data centers, so option D is correct. Options A through C are incorrect because they do not include two other correct options.



#### 4. Grouping a set of metrics that arrive in a period of time into regular-sized buckets is called what?

A. Aggregation&#x20;

B. Alignment

C. Minimization&#x20;

D. Consolidation



Answers:

B. Aligning is the process of separating data points into regular buckets, so option B is correct. Option A is incorrect; aggregation is used to combine data points using a statistic, such as mean. Options C and D are incorrect; they are not processes related to processing streams of metric data.



#### 5. You have created a condition of CPU utilization, and you want to receive notifications. Which of the following are options?

A. Email only

B. PagerDuty only

C. Hipchat and PagerDuty

D. Email, PagerDuty, and Hipchat



Answers:

D. All three options are valid notification channels in Stackdriver Monitoring, so option D is correct. PagerDuty and HipChat are popular DevOps tools.



#### 6. When you create a policy to notify you of a potential problem with your infrastructure, you can specify optional documentation. Why would you bother putting documentation in that form?

A. It is saved to Cloud Storage for future use.

B. It can help you or a colleague understand the purpose of the policy.

C. It can contain information that would help someone diagnose and correct the problem.

D. Options B and C.



Answers:

D. The documentation is useful for documenting the purpose of the policy and for provid- ing guidance for solving the problem, so option D is correct. Option A is incorrect; where a policy is stored is irrelevant to its usefulness. Options B and C alone are partially correct, but option D is a better answer.



#### 7. What is alert fatigue, and why is it a problem?

A. Too many alert notifications are sent for events that do not require human intervention, and eventually DevOps engineers begin to pay less attention to notifications.

B. Too many alerts put unnecessary load on your systems.

C. Too few alerts leave DevOps engineers uncertain of the state of your applications and

infrastructure.

D. Too many false alerts



Answers:

A. Alert fatigue is a state caused by too many alert notifications being sent for events that do not require human intervention, so option A is correct. This creates the risk that eventu- ally DevOps engineers will begin to pay less attention to notifications. Option B is incor- rect, although it is conceivable that too many alerts could adversely impact performance, but that is not likely. Option C is a potential problem, too, but that is not alert fatigue. Option D is incorrect because too many true alerts contribute to alert fatigue.



#### 8. How long is log data stored in Stackdriver Logging?&#x20;

A. 7 days

B. 15 days&#x20;

C. 30 days&#x20;

D. 60 days



Answers:

C. Stackdriver Logging stores log entries for 30 days, so option C is correct.



#### 9. You need to store log entries for a longer period of time than Stackdriver Logging retains them. What is the best option for preserving log data?

A. There is no option; once the data retention period passes, Stackdriver Logging deletes the data.

B. Create a log sink and export the log data using Stackdriver Logging’s export functionality.

C. Write a Python script to use the Stackdriver API to write the data to Cloud Storage.

D. Write a Python script to use the Stackdriver API to write the data to BigQuery.



Answers:

B. The best option is to use Stackdriver Logging’s export functionality to write log data to a log sink, so option B is correct. Option A is incorrect; there is a way to export data. Options C and D are incorrect because writing a custom script would take more time to develop and maintain than using Logging’s export functionality.



#### 10. Which of the following are options for logging sinks?

A. Cloud Storage bucket only

B. BigQuery dataset and Cloud Storage bucket only

C. Cloud Pub/Sub topic only

D. Cloud Storage bucket, BigQuery dataset, and Cloud Pub/Sub topic



Answers:

D. All three, Cloud Storage buckets, BigQuery data sets, and Cloud Pub/Sub topics, are available as sinks for logging exports, so option D is correct.



#### 11. Which of the following can be used to filter log entries when viewing logs in Stackdriver Logging?

A. Label or text search only

B. Resource type and log type only

C. Time and resource type only

D. Label or text search, resource type, log type, and time



Answers:

D. All of the options listed can be used to filter, so option D is correct. Log level is another option as well.



#### 12. Which of the following is not a standard log level that can be used to filter log viewings?&#x20;

A. Critical

B. Halted&#x20;

C. Warning&#x20;

D. Info



Answers:

B. The correct answer, option B, is halted. There is no such standard log level status. Sta- tuses include Critical, Error, Warning, Info, and Debug.



#### 13. You are viewing log entries and spot one that looks suspicious. You are not familiar with the kind of log entry, and you want to see the complete details of the log entry as quickly as possible. What would you do?

A. Drill down one by one into each structure in the log entry.

B. Click Expand all to show all details.

C. Write a Python script to reformat the log entry.

D. Click the Show Detail link next to the log entry.



Answers:

B. The fastest way to see the details is to expand all levels of structured data in the entry, so option B is correct. Option A would show the details, but it is not the fastest way. Option C is more time-consuming than using the functionality built into Stackdriver Logging. Option D is incorrect; there is no such link.



#### 14. What Stackdriver service is best for identifying where bottlenecks exist in your application?&#x20;

A. Monitoring

B. Logging&#x20;

C. Trace&#x20;

D. Debug



Answers:

C. Cloud Trace is a distributed tracing application that provides details on how long dif- ferent parts of code run, so option C is correct. Option A is incorrect; monitoring is used to notify DevOps engineers when resources are not functioning as expected. Option B is incorrect; Logging is for collecting, storing, and viewing log data, and although log entries might help diagnose bottlenecks, it is not specifically designed for that. Option D is incor- rect; Debug is used to generate snapshots and inject logpoints.



#### 15. There is a bug in a microservice. You have reviewed application outputs but cannot identify the problem. You decide you need to step through the code. What Stackdriver service would you use to give you insight into the status of the services at particular points in execution?

A. Monitoring&#x20;

B. Logging

C. Trace

D. Debug



Answers:

D. Debug is used to generate snapshots that provide a view of the status of an application at a particular point in its execution, so option D is correct. Option A is incorrect; moni- toring is used to notify DevOps engineers when resources are not functioning as expected. Option B is incorrect; Logging is for collecting, storing, and viewing log data. Option C is incorrect because Cloud Trace is a distributed tracing application that provides details on how long different parts of code run.



#### 16. You believe there may be a problem with BigQuery in the us-central zone. Where would you go to check the status of the BigQuery service for the quickest access to details?

A. Email Google Cloud Support.

B. Check https://status.cloud.google.com/.

C. Check https://bigquery.status.cloud.google.com/.

D. Call Google tech support.



Answers:

B. The Google Cloud Status Dashboard at https://status.cloud.google.com/ has information on the status of GCP services, so option B is correct. Options A and B might lead to information, but they would take longer. Option C is not a link to a source of infor- mation on BigQuery.



#### 17. You would like to estimate the cost of GCP resources you will be using. Which services would require you to have information on the virtual machines you will be using?&#x20;

A. Compute Engine and BigQuery

B. Compute Engine and Kubernetes Engine

C. BigQuery and Kubernetes Engine

D. BigQuery and Cloud Pub/Sub



Answers:

B. Both Compute Engine and Kubernetes Engine will require details about the VMs’ con- figurations, so option B is correct. The other options are incorrect because BigQuery and Cloud Pub/Sub are serverless services.



#### 18. You are generating an estimate of the cost of using BigQuery. One of the parameters is Query Pricing. You have to specify a value in TB units. What is the value you are specifying?

A. The amount of data stored in BigQuery

B. The amount of data returned by the query

C. The amount of data scanned by the query

D. The amount of data in Cloud Storage bucket



Answers:

C. Query pricing in BigQuery is based on the amount of data scanned, so option C is cor- rect. Option A is incorrect; the amount of data storage is specified in the Storage Pricing section. Option B is incorrect; query pricing is not based on the volume of data returned. Option D is incorrect because this is not related to Cloud Storage. Option D is incorrect because option C is correct.



#### 19. Why do you need to specify the operating system to be used when estimating the cost of a VM?

A. All operating systems are charged a fixed rate.

B. Some operating systems incur a cost.

C. It’s not necessary; it is only included for documentation.

D. To estimate the cost of Bring Your Own License configurations.



Answers:

B. Some operating systems, like Microsoft Windows Server, require a license, so option B is correct. Google sometimes has arrangements with vendors to collect fees for using pro- prietary software. Option A is incorrect; there is no fixed rate charge for operating systems. Option C is incorrect; the information is sometimes needed to compute charges. Option D is incorrect because if you Bring Your Own License, there is no additional license charge.



#### 20. You want to create a custom metric for use in Stackdriver Monitoring but do not want to use the low-level Stackdriver API. What is an alternative open source option for working with custom metrics?

A. Prometheus&#x20;

B. OpenCensus&#x20;

C. Grafana

D. Nagios



Answers:

B. OpenCensus is a library for developing custom metrics that can be used with Stackdriver Logging, so option B is correct. Option A is incorrect; Prometheus is an open source moni- toring tool, but it is not used to define custom metrics in Stackdriver Monitoring. Option C is incorrect; Grafana is a visualization tools for Prometheus. Option D is incorrect; Nagios is an open source monitoring and alerting service, but it is not used for defining custom metrics in Stackdriver Logging.

