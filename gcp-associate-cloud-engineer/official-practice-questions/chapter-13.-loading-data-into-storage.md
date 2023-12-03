# Chapter 13. Loading Data into Storage

#### 1. Which of the following commands is used to create buckets in Cloud Storage?&#x20;

A. gcloud storage buckets create

B. gsutil storage buckets create

C. gsutil mb

D. gcloud mb



Answers:

C. gsutil is the command-line utility for working with Cloud Storage. It is one of the few GCP services that does not use gcloud. (BigQuery and Bigtable are others.) Option C is the correct answer because mb, short for “make bucket,” is the verb that follows gsutil to create a bucket. Options A and D are wrong because they use gcloud instead of gsutil. Option B is wrong because it uses gsutil with a command syntax used by gcloud.



#### 2. You need to copy files from your local device to a bucket in Cloud Storage. What command would you use? Assume you have Cloud SDK installed on your local computer.

A. gsutil copy

B. gsutil cp

C. gcloud cp

D. gcloud storage objects copy



Answers:

B. The correct answer is option B; gsutil is the command to copy files to Cloud Storage. Option A is incorrect; the verb is cp, not copy. Options C and D are wrong because gsutil, not gcloud, is the command-line utility for working with Cloud Storage.



#### 3. You are migrating a large number of files from a local storage system to Cloud Storage. You want to use the Cloud Console instead of writing a script. Which of the following Cloud Storage operations can you perform in the console?

A. Upload files only

B. Upload folders only

C. Upload files and folders

D. Compare local files with files in the bucket using the diff command



Answers:

C. From the console, you can upload both files and folders. Options A and B are incorrect because they are missing an operation that can be performed in the console. Option D is incorrect because there is no diff operation in Cloud Console.



#### 4. A software developer asks for your help exporting data from a Cloud SQL database. The developer tells you which database to export and which bucket to store the export file in, but hasn’t mentioned which file format should be used for the export file. What are the options for the export file format?

A. CSV and XML

B. CSV and JSON

C. JSON and SQL

D. CSV and SQL



Answers:

D. When exporting a database from Cloud SQL, the export file format options are CSV and SQL, which makes option D correct. Option A is incorrect because XML is not an option. Options B and C are incorrect because JSON is not an option.



#### 5. A database administrator has asked for an export of a MySQL database in Cloud SQL. The database administrator will load the data into another relational database and would to do it with the least amount of work. Specifically, the loading method should not require the data- base administrator to define a schema. What file format would you recommend for this task?

A. SQL&#x20;

B. CSV&#x20;

C. XML&#x20;

D. JSON



Answers:

A. Option A, SQL format, exports a database as a series of SQL data definition commands. These commands can be executed in another relational database without having to first cre- ate a schema. Option B could be used, but that would require mapping columns to columns in a schema that was created before loading the CSV, and the database administrator would like to avoid that. Options C and D are incorrect because they are not export file format options.



#### 6. Which command will export a MySQL database called ace-exam-mysql1 to a file called ace-exam-mysql-export.sql in a bucket named ace-exam-buckete1?

A. gcloud storage export sql ace-exam-mysql1 gs://ace-exam-buckete1/ace-

exam-mysql-export.sql \ ––database=mysql

B. gcloud sql export ace-exam-mysql1 gs://ace-exam-buckete1/ace-exam- mysql-export.sql \ ––database=mysql

C. gcloud sql export sql ace-exam-mysql1 gs://ace-exam-buckete1/ace-exam- mysql-export.sql \ ––database=mysql

D. gcloud sql export sql ace-exam-mysql1 gs://ace-exam-mysql-export.sql/ ace-exam-buckete1/ \ ––database=mysql



Answers:

C. Option C is the correct command, gcloud sql export sql, indicating that the service is Cloud SQL, the operation is export, and the export file format is SQL. The filename and tar- get bucket are correctly formed. Option A is incorrect because it references gcloud storage, not gcloud sql. Option B is incorrect because it is missing an export file format parameter. Option D is incorrect because the bucket name and filename are in the wrong order.



#### 7. As part of a compliance regimen, your team is required to back up data from your Datastore database to an object storage system. Your data is stored in the default namespace. What command would you use to export the default namespace from Datastore to a bucket called ace-exam-bucket1?

A. gcloud datastore export ––namespaces="(default)" gs://ace-exam-bucket1&#x20;

B. gcloud datastore export ––namespaces="(default)" ace-exam-bucket1

C. gcloud datastore dump ––namespaces="(default)" gs://ace-exam-bucket1&#x20;

D. gcloud datastore dump ––namespaces="(default)" ace-exam-bucket1



Answers:

A. Option A uses the correct command, which is gcloud datastore export followed by a namespace and a bucket name. Option B is incorrect because the bucket name is miss- ing gs://. Options C and D are incorrect because they use the command dump instead of export. The bucket name in option D is missing gs://.



#### 8. As required by your company’s policy, you need to back up your Datastore database at least once per day. An auditor is questioning whether or not Datastore export is sufficient. You explain that the Datastore export command produces what outputs?

A. A single entity file

B. A metadata file

C. A metadata file and a folder with the data

D. A metadata file, an entity file, and a folder with the data



Answers:

C. The export process creates a metadata file with information about the data exported and a folder that has the data itself, so option C is correct. Option A is incorrect because export does not produce a single file; it produces a metadata file and a folder with the data. Option B is incorrect because it does not include the data folder. Option D is incorrect because the correct answer is option C.



#### 9. Which of the following file formats is not an option for an export file when exporting from BigQuery?

A. CSV&#x20;

B. XML&#x20;

C. Avro&#x20;

D. JSON



Answers:

B. Option B is correct because XML is not an option in BigQuery’s export process. All other options are available.



#### 10. Which of the following file formats is not supported when importing data into BigQuery?&#x20;

A. CSV

B. Parquet&#x20;

C. Avro&#x20;

D. YAML



Answers:

D. Option D is correct because YAML is not a file storage format; it used for specifying configuration data. Options A, B, and C are all supported import file types.



#### 11. You have received a large data set from an Internet of Things (IoT) system. You want to use BigQuery to analyze the data. What command-line command would you use to make data available for analysis in BigQuery?

A. bq load ––autodetect ––source\_format=\[FORMAT] \[DATASET].\[TABLE] \[PATH\_TO\_SOURCE]

B. bq import ––autodetect ––source\_format=\[FORMAT] \[DATASET].\[TABLE] \[PATH\_TO\_SOURCE]

C. gloud BigQuery load ––autodetect ––source\_format=\[FORMAT] \[DATASET]. \[TABLE] \[PATH\_TO\_SOURCE]

D. gcloud BigQuery load ––autodetect ––source\_format=\[FORMAT] \[DATASET]. \[TABLE] \[PATH\_TO\_SOURCE]



Answers:

A. The correct command is bq load in option A. The autodetect and source\_format parameters and path to source are correctly specified in all options. Option B is incorrect because it uses the term import instead of load. Options C and D are incorrect because they use gcloud instead of bq.



#### 12. You have set up a Cloud Spanner process to export data to Cloud Storage. You notice that each time the process runs you incur charges for another GCP service, which you think is related to the export process. What other GCP service might be incurring charges during the Cloud Spanner export?

A. Dataproc&#x20;

B. Dataflow&#x20;

C. Datastore&#x20;

D. bq



Answers:

B. The correct answer is B because Dataflow is a pipeline service for processing streaming and batch data that implements workflows used by Cloud Spanner. Option A is incorrect; Dataproc is a managed Hadoop and Spark service, which is used for data analysis. Option C is incorrect; Datastore is a NoSQL database. Option D is incorrect because bq is used with BigQuery only.



#### 13. As a developer on a project using Bigtable for an IoT application, you will need to export data from Bigtable to make some data available for analysis with another tool. What would you use to export the data, assuming you want to minimize the amount of effort required on your part?

A. A Java program designed for importing and exporting data from Bigtable

B. gcloud bigtable table export

C. bq bigtable table export

D. An import tool provided by the analysis tool



Answers:

A. Bigtable data is exported using a compiled Java program, so option A is correct. Option B is incorrect; there is no gcloud Bigtable command. Option C is incorrect; bq is not used with Bigtable. Option D is incorrect because it does not export data from Bigtable.



#### 14. You have just exported from a Dataproc cluster. What have you exported?

1. Data in Spark DataFrames
2. All tables in the Spark database
3. Configuration data about the cluster
4. All tables in the Hadoop database



Answers:

C. Exporting from Dataproc exports data about the cluster configuration, which makes option C correct. Option A is incorrect; data in DataFrames is not exported. Option B is incorrect; Spark does not have tables for persistently storing data like relational databases. Option D is incorrect; no data from Hadoop is exported.



#### 15. A team of data scientists has requested access to data stored in Bigtable so that they can train machine learning models. They explain that Bigtable does not have the features required to build machine learning models. Which of the following GCP services are they most likely to use to build machine learning models?

A. Datastore

B. Dataflow

C. Dataproc

D. DataAnalyze



Answers:

C. The correct answer is option C; the service Dataproc supports Apache Spark, which has libraries for machine learning. Options A and B are incorrect, neither is an analysis or machine learning service. Option D, DataAnalyze, is not an actual service.



#### 16. The correct command to create a Pub/Sub topic is which of the following?&#x20;

A. gcloud pubsub topics create

B. gcloud pubsub create topics

C. bq pubsub create topics

D. cbt pubsub topics create



Answers:

A. The correct command in option A uses gcloud followed by the service, in this case pubsub, followed by the resource, in this case topics; and finally the verb, in this case create. Option B is incorrect because the last two terms are out of order. Options C and D are incorrect because they do not use gcloud. bq is the command-line tool for BigQuery. cbt is the command-line tool for Bigtable.



#### 17. Which of the following commands will create a subscription on the topic ace-exam-topic1?

A. gcloud pubsub create ––topic=ace-exam-topic1 ace-exam-sub1

B. gcloud pubsub subscriptions create ––topic=ace-exam-topic1

C. gcloud pubsub subscriptions create ––topic=ace-exam-topic1 ace-exam-sub1&#x20;

D. gsutil pubsub subscriptions create ––topic=ace-exam-topic1 ace-exam-sub1



Answers:

C. The correct answer, option C, uses gcloud pubsub subscriptions create followed by the topic and the name of the subscription. Option A is incorrect because it is missing the term subscriptions. Option B is incorrect because it is missing the name of the sub- scription. Option D is incorrect because it uses gsutil instead of gcloud.



#### 18. What is one of the direct advantages of using a message queue in distributed systems?

A. It increases security.

B. It decouples services, so if one lags, it does not cause other services to lag.

C. It supports more programming languages.

D. It stores messages until they are read by default.



Answers:

B. Using a message queue between services decouples the services, so if one lags it does not cause other services to lag, which makes option B correct. Option A is incorrect because adding a message queue does not directly mitigate any security risks that might exist in the distributed system, such as overly permissive permissions. Option C is incorrect; adding a queue is not directly related to programming languages. Option D is incorrect; by default, message queues have a retention period.



#### 19. To ensure you have installed beta gcloud commands, which command should you run?&#x20;

A. gcloud components beta install

B. gcloud components install beta

C. gcloud commands install beta

D. gcloud commands beta install



Answers:

B. The correct answer is B, gcloud components followed by install and then beta. Option A is incorrect because beta and install are in the wrong order. Options C and D are wrong because commands is used instead of components.



#### 20. What parameter is used to tell BigQuery to automatically detect the schema of a file on import?

A. ––autodetect&#x20;

B. ––autoschema&#x20;

C. ––detectschema&#x20;

D. ––dry\_run



Answers:

A. The correct parameter name is autodetect, which is option A. Options B and C are not actually valid bq parameters. Option D is a valid parameter, but it returns the estimated size of data scanned to when executing a query.



#### 21. The compression options deflate and snappy are available for what file types when exporting from BigQuery?

A. Avro&#x20;

B. CSV&#x20;

C. XML&#x20;

D. Thrift



Answers:

A. Avro supports Deflate and Snappy compression. CSV supports Gzip and no compression. XML and Thrift are not export file type options.

