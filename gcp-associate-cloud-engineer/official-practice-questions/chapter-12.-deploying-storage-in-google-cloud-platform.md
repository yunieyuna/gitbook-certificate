# Chapter 12. Deploying Storage in Google Cloud Platform

#### 1. Cloud SQL is a fully managed relational database service, but database administrators still have to perform some tasks. Which of the following tasks do Cloud SQL users need to perform?

A. Applying security patches

B. Performing regularly scheduled backups

C. Creating databases

D. Tuning the operating system to optimize Cloud SQL performance



Answers:

C. Creating databases is the responsibility of database administrators or other users of Cloud SQL, so option C is correct. Google applies security patches and performs other maintenance, so option A is incorrect. GCP performs regularly scheduled backups, so option B is incorrect. Database administrators need to schedule backups, but GCP makes sure they are performed on schedule. Cloud SQL users can’t SSH into a Cloud SQL server, so they can’t tune the operating system. That’s not a problem; Google takes care of that.



#### 2. Which of the following commands is used to create a backup of a Cloud SQL database?&#x20;

A. gcloud sql backups create

B. gsutil sql backups create

C. gcloud sql create backups

D. gcloud sql backups export



Answers:

A. Cloud SQL is controlled using the gcloud command; the sequence of terms in gcloud commands is gcloud followed by the service, in this case SQL; followed by a resource, in this case backups, and a command or verb, in this case create. Option A is the correct answer. Option B is incorrect because gsutil is used to work with Cloud Storage, not Cloud SQL. Option C is wrong because the order of terms is incorrect; backups comes before create. Option D is incorrect because the command or verb should be create.



#### 3. Which of the following commands will run an automatic backup at 3:00 a.m. on an instance called ace-exam-mysql?

A. gcloud sql instances patch ace-exam-mysql --backup-start-time 03:00

B. gcloud sql databases patch ace-exam-mysql –-backup-start-time 03:00

C. cbt sql instances patch ace-exam-mysql -–backup-start-time 03:00

D. bq gcloud sql instances patch ace-exam-mysql -–backup-start-time 03:00



Answers:

A. Option A is the correct answer. The base command is gcloud sql instances patch, which is followed by the instance name and a start time passed to the –-backup-start-time parameter. Option B is incorrect because databases is not the correct resource to refer- ence; instances is. Option C uses the cbt command, which is for use with Bigtable, so it is incorrect. Similarly, Option D is incorrect because it uses the bq command, which is used to manage BigQuery resources.



#### 4. What is the query language used by Datastore?&#x20;

A. SQL

B. MDX

C. GQL

D. DataFrames



Answers:

C. Datastore uses a SQL-like query language called GQL, so option C is correct. Option A is incorrect; SQL is not used with this database. Option B is incorrect; MDX is a query language for online analytic processing (OLAP) systems. Option D is incorrect because DataFrames is a data structure used in Spark.



#### 5. What is the correct command-line structure to export data from Datastore?

A. gcloud datastore export '\[NAMESPACE]' gs://\[BUCKET\_NAME]

B. gcloud datastore export gs://\[BUCKET\_NAME]

C. gcloud datastore export --namespaces='\[NAMESPACE]' gs://\[BUCKET\_NAME]&#x20;

D. gcloud datastore dump --namespaces='\[NAMESPACE]' gs://\[BUCKET\_NAME]



Answers:

C. Option C is the correct command. It has the correct base command, gcloud datastore export, followed by the --namespaces parameter and the name of a Cloud Storage bucket to hold the export file. Option A is incorrect because the --namespaces parameter name\
is missing. Option B is incorrect because it is missing a namespace. Option D is incorrect because it uses the command or verb dump instead of export.



#### 6. When you enter a query into the BigQuery query form, BigQuery analyzes the query and displays an estimate of what metric?&#x20;

A. Time required to enter the query&#x20;

B. Cost of the query

C. Amount of data scanned

D. Number of bytes passed between servers in the BigQuery cluster



Answers:

C. Option C is correct; BigQuery displays an estimate of the amount of data scanned. This is important because BigQuery charges for data scanned in queries. Option A is incorrect; knowing how long it took you to enter a query is not helpful. Option B is incorrect; you need to use the scanned data estimate with the Pricing Calculator to get an estimate cost. Option D is incorrect; you do not create clusters in BigQuery as you do with Bigtable and Dataproc. Network I/O data is not displayed.



#### 7. You want to get an estimate of the volume of data scanned by BigQuery from the command line. Which option shows the command structure you should use?

A. gcloud BigQuery query estimate \[SQL\_QUERY]

B. bq ––location=\[LOCATION] query --use\_legacy\_sql=false ––dry\_run

\[SQL\_QUERY]

C. gsutil ––location=\[LOCATION] query --use\_legacy\_sql=false ––dry\_run \[SQL\_QUERY]

D. cbt BigQuery query estimate \[SQL\_QUERY]



Answers:

B. Option B shows the correct bq command structure, which includes location and the ––dry\_run option. This option calculates an estimate without actually running the query. Options A and C are incorrect because they use the wrong command; gcloud and gsutil are not used with BigQuery. Option D is also wrong. cbt is a tool for working with Big- table, not BigQuery. Be careful not to confuse the two because their names are similar.



#### 8. You are using Cloud Console and want to check on some jobs running in BigQuery. You navigate to the BigQuery part of the console. Which menu item would you click to view jobs?

A. Job History.

B. Active Jobs.

C. My Jobs.

D. You can’t view job status in the console; you have to use bq on the command line.



Answers:

A. Option A is correct; the menu option is Job History. Options B and C are incorrect; there is no Active Jobs or My Jobs option. Job History shows active jobs, completed jobs, and jobs that generated errors. Option D is incorrect; you can get job status in the console.



#### 9. You want to estimate the cost of running a BigQuery query. What two services within Google Cloud Platform will you need to use?

A. BigQuery and Billing

B. Billing and Pricing Calculator

C. BigQuery and Pricing Calculator&#x20;

D. Billing and Pricing Calculator



Answers:

C. BigQuery provides an estimate of the amount of data scanned, and the Pricing Calculator gives a cost estimate for scanning that volume of data. Options A, B, and C are incorrect; the Billing service tracks charges incurred. It is not used to estimate future or potential charges.



#### 10. You have just created a Cloud Spanner instance. You have been tasked with creating a way to store data about a product catalog. What is the next step after creating a Cloud Spanner instance that you would perform to enable you to load data?

A. Run gcloud spanner update-security-patches.

B. Create a database within the instance.

C. Create tables to hold the data.

D. Use the Cloud Spanner console to import data into tables created with the instance.



Answers:

B. Option B is correct; the next step is to create a database within the instance. Once a database is created, tables can be created, and data can be loaded into tables. Option A\
is incorrect; Cloud Spanner is a managed database, so you do not need to apply security patches. Option C is incorrect because you can’t create tables without first having created a database. Option D is incorrect; no tables are created that you could import data into when an instance is created.



#### 11. You have created a Cloud Spanner instance and database. According to Google best practices, how often should you update VM packages using apt-get?

A. Every 24 hours.

B. Every 7 days.

C. Every 30 days.

D. Never, Cloud Spanner is a managed service.



Answers:

D. Option D is correct because there is no need to apply patches to the underlying compute resources when using Cloud Spanner. because Google manages resources used by Cloud Spanner. Updating packages is a good practice when using VMs, for example, with Compute Engine, but it is not necessary with a managed service.



#### 12. Your software team is developing a distributed application and wants to send messages from one application to another. Once the consuming application reads a message, it should be deleted. You want your system to be robust to failure, so messages should be available for at least three days before they are discarded. Which GCP service is best designed to support this use case?

A. Bigtable

B. Dataproc

C. Cloud Pub/Sub

D. Cloud Spanner



Answers:

C. This use case is well suited to Pub/Sub, so option C is correct. It involves sending messages to the topic, and the subscription model is a good fit. Pub/Sub has a retention period to support the three-day retention period. Option A is incorrect; Bigtable is designed for storing large volumes of data. Dataproc is for processing and analyzing data, not passing it between systems. Cloud Spanner is a global relational database. You could design an application to meet this use case, but it would require substantial development and be costly to run.



#### 13. Your manager asks you to set up a bare-bones Pub/Sub system as a sandbox for new devel- opers to learn about messaging systems. What are the two resources within Pub/Sub you will need to create?

A. Topics and tables

B. Topics and databases

C. Topics and subscriptions

D. Tables and subscriptions



Answers:

C. Pub/Sub works with topics, which receive and hold messages, and subscriptions, which make messages available to consuming applications; therefore, option C is correct. Option A is incorrect; tables are data structures in relational databases, not message queues. Similarly, option B is wrong because databases exist in instances of database management systems, not messaging systems. Option D is wrong because tables are not a resource in messaging systems.



#### 14. Your company is launching an IoT service and will receive large volumes of streaming data. You have to store this data in Bigtable. You want to explore the Bigtable environment from the command line. What command would you run to ensure you have command-line tools installed?

A. apt-get install bigtable-tools

B. apt-get install cbt

C. gcloud components install cbt

D. gcloud components install bigtable-tools



Answers:

C. The correct command is gcloud components install cbt to install the Bigtable command-line tool, so option C is correct. Options A and B are incorrect; apt-get is used to install packages on some Linux systems but is not specific to GCP. Option D is incorrect; there is no such command as bigtable-tools.



#### 15. You need to create a table called iot-ingest-data in Bigtable. What command would you use?&#x20;

A. cbt createtable iot-ingest-data

B. gcloud bigtable tables create ace-exam-bt-table

C. gcloud bigtable create tables ace-exam-bt-table

D. gcloud create ace-exam-bt-table



Answers:

A. You would need to use a cbt command, which is the command-line tool for working with Bigtable, so option A is correct. All other options reference gcloud and are therefore incorrect.



#### 16. Cloud Dataproc is a managed service for which two big data platforms?

A. Spark and Cassandra

B. Spark and Hadoop

C. Hadoop and Cassandra

D. Spark and TensorFlow



Answers:

B. Cloud Dataproc is a managed service for Spark and Hadoop, so option B is correct. Cassandra is a big data distributed database but is not offered as a managed service by Google, so options A and C are incorrect. Option D is incorrect because TensorFlow is a deep learning platform not included in Dataproc.



#### 17. Your department has been asked to analyze large batches of data every night. The jobs will run for about three to four hours. You want to shut down resources as soon as the analysis is done, so you decide to write a script to create a Dataproc cluster every night at midnight. What command would you use to create a cluster called spark-nightly-analysis in the us-west2-a zone?

A. bq dataproc clusters create spark-nightly-analysis ––zone us-west2-a

B. gcloud dataproc clusters create spark-nightly-analysis ––zone us-west2-a

C. gcloud dataproc clusters spark-nightly-analysis ––zone us-west2-a

D. None of the above



Answers:

B. The correct command is gcloud dataproc clusters create followed by the name of the cluster and the a --zone parameter. Option B is correct. Option A is incorrect because bq is the command-line tool for BigQuery, not Dataproc. Option C is a gcloud command missing a verb or command, so it is incorrect. Option D is wrong because option B is the correct answer.



#### 18. You have a number of buckets containing old data that is hardly ever used. You don’t want to delete it, but you want to minimize the cost of storing it. You decide to change the storage class to coldline for each of those buckets. What is the command structure that you would use?

A. gcloud rewrite -s \[STORAGE\_CLASS] gs://\[PATH\_TO\_OBJECT]&#x20;

B. gsutil rewrite -s \[STORAGE\_CLASS] gs://\[PATH\_TO\_OBJECT]&#x20;

C. cbt rewrite -s \[STORAGE\_CLASS] gs://\[PATH\_TO\_OBJECT]

D. bq rewrite -s \[STORAGE\_CLASS] gs://\[PATH\_TO\_OBJECT]



Answers:

B. gsutil is the correct command, so option B is correct. Option A is incorrect because gcloud commands are not used to manage Cloud Storage. Similarly, options C and D are incorrect because they use commands for Bigtable and BigQuery, respectively.



#### 19. You want to rename an object stored in a bucket. What command structure would you use?

A. gsutil cp gs://\[BUCKET\_NAME]/\[OLD\_OBJECT\_NAME] gs://\[BUCKET\_NAME]/

\[NEW\_OBJECT\_NAME]

B. gsutil mv gs://\[BUCKET\_NAME]/\[OLD\_OBJECT\_NAME] gs://\[BUCKET\_NAME]/ \[NEW\_OBJECT\_NAME]

C. gsutil mv gs://\[OLD\_OBJECT\_NAME] gs://\[NEW\_OBJECT\_NAME]

D. gcloud mv gs://\[OLD\_OBJECT\_NAME] gs://\[NEW\_OBJECT\_NAME]



Answers:

B. The command in option B correctly renames an object from an old name to a new name. Option A is incorrect because it uses a cp command instead of mv. Option C does not include bucket names, so it is incorrect. Option D uses gcloud, but gsutil is the com- mand-line tool for working with Cloud Storage.



#### 20. An executive in your company emails you asking about creating a recommendation system that will help sell more products. The executive has heard there are some GCP solutions that may be good fits for this problem. What GCP service would you recommend the executive look into?

A. Cloud Dataproc, especially Spark and its machine learning library

B. Cloud Dataproc, especially Hadoop

C. Cloud Spanner, which is a global relational database that can hold a lot of data

D. Cloud SQL, because SQL is a powerful query language



Answers:

A. Dataproc with Spark and its machine learning library are ideal for this use case, so option A is correct. Option B suggests Hadoop, but it is not a good choice for machine learning applications. Option C is incorrect because Spanner is designed as a global rela- tional database with support for transaction processing systems, not analytic and machine learning systems. Option D is incorrect. SQL is a powerful query language, but it does not support the kinds of machine learning algorithms needed to solve the proposed problem.

