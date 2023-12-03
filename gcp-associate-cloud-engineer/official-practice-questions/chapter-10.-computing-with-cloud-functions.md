# Chapter 10. Computing with Cloud Functions

#### 1. A product manager is proposing a new application that will require several backend ser- vices, three business logic services, and access to relational databases. Each service will provide a single function, and it will require several of these services to complete a business task. Service execution time is dependent on the size of input and is expected to take up to 30 minutes in some cases. Which GCP product is a good serverless option for running this related service?

A. Cloud Functions

B. Compute Engine

C. App Engine

D. Cloud Storage



Answers:

C. App Engine is designed to support multiple tightly coupled services comprising an application, making option C the correct answer. This is unlike Cloud Functions, which is designed to support single-purpose functions that operate independently and in response to isolated events in the Google Cloud and complete within a specified period of time. Com- pute Engine is not a serverless option. Cloud Storage is not a computing product.



#### 2. You have been asked to deploy a cloud function to reformat image files as soon as they are uploaded to Cloud Storage. You notice after a few hours that about 10 percent of the files are not processed correctly. After reviewing the files that failed, you realize they are all sub- stantially larger than average. What could be the cause of the failures?

A. There is a syntax error in the function code.

B. The wrong runtime was selected.

C. The timeout is too low to allow enough time to process large files.

D. There is a permissions error on the Cloud Storage bucket containing the files.



Answers:

C. A timeout period that is too low would explain why the smaller files are processed in time but the largest are not, which makes option C the right answer. If only 10 percent of the files are failing, then it is not a syntax error or the wrong runtime selected, as in options A and B. Those errors would affect all files, not just the largest ones. Similarly, if there was a permission problem with the Cloud Storage bucket, it would affect all files.



#### 3. When an action occurs in GCP, such as a file being written to Cloud Storage or a message being added to a Cloud Pub/Sub topic, that action is called what?

A. An incident

B. An event

C. A trigger

D. A log entry



Answers:

B. Those actions are known as events in Google Cloud terminology; thus, option B is the correct answer. An incident may be a security or performance-related occurrence, but those are unrelated to the expected and standardized actions that constitute events. A trigger is a declaration that a certain function should execute when an event occurs. A log entry is related to applications recording data about significant events. Log entries are helpful for monitoring and compliance, but in themselves are not event-related actions.



#### 4. All of the following generate events that can be triggered using Cloud Functions, except which one?

A. Cloud Storage

B. Cloud Pub/Sub

C. SSL

D. Firebase



Answers:

C. The correct answer is option C because SSL is a secure protocol for remotely accessing servers. It is used, for example, to access instances in Compute Engine. It does not have events that can be triggered using Cloud Functions. The three GCP products listed do generate events that can have triggers associated with them.



#### 5. Which runtimes are supported in Cloud Functions?

A. Node.js 5, Node.js 6, and Node.js 8

B. Node.js 8, Python, and Go

C. Node.js 6, Node.js 8, and Python

D. Node.js 8, Python, and Go



Answers:

C. Cloud Functions supports three runtimes: Node.js 6, Node.js 8, and Python. Go and Node.js 5 are not supported runtimes.



#### 6. An HTTP trigger can be invoked by making a request using which of the following?

A. GET only

B. POST and GET only

C. DELETE, POST, and GET

D. DELETE, POST, REVISE, and GET



Answers:

D. HTTP requests using GET, POST, DELETE, PUT, and OPTIONS can invoke an HTTP trigger in Cloud Functions, so option C is the right answer.



#### 7. What types of events are available to Cloud Functions working with Cloud Storage?&#x20;

A. Upload or finalize and delete only

B. Upload or finalize, delete, and list only

C. Upload or finalize, delete, and metadata update only

D. Upload or finalize, delete, metadata update, and archive



Answers:

D. The correct answer, option D, shows the four events supported in Cloud Storage.

google.storage.object.finalize

google.storage.object.delete

google.storage.object.archive

google.storage.object.metadataUpdate



#### 8. You are tasked with designing a function to execute in Cloud Functions. The function will need more than the default amount of memory and should be applied only when a finalize event occurs after a file is uploaded to Cloud Storage. The function should only apply its logic to files with a standard image file type. Which of the following required features can- not be specified in a parameter and must be implemented in the function code?

A. Cloud function name

B. Memory allocated for the function

C. File type to apply the function to

D. Event type



Answers:

C. There is no option to specify the file type to apply the function to, so option C is cor- rect. You can, however, specify the bucket to which the function is applied. You could only save files or the types you want processed in that bucket, or you could have your function check file type and then execute the rest of the function or not, based on type. All the other options listed are parameters to a Cloud Storage function.



#### 9. How much memory can be allocated to a Cloud Function?

A. 128MB to 256MB

B. 128MB to 512MB

C. 128MB to 1GB

D. 128MB to 2GB



Answers:

D. Cloud Functions can have between 128MB and 2GB of memory allocated, which makes option D the correct answer. The default is 256MB.



#### 10. How long can a cloud function run by default before timing out?

A. 30 seconds

B. 1 minute

C. 9 minutes

D. 20 minutes



Answers:

B. By default Cloud Functions can run for up to 1 minute before timing out, so option B is correct. You can, however, set the timeout parameter for a cloud function for periods of up to 9 minutes before timing out.



#### 11. You want to use the command line to manage Cloud Functions that will be written in Python. In addition to running the gcloud components update command, what com- mand should you run to ensure you can work with Python functions?

A. gcloud component install

B. gcloud components install beta&#x20;

C. gcloud components install python&#x20;

D. gcloud functions install beta



Answers:

B. Python Cloud Functions is currently in beta. The standard set of gcloud commands does not include commands for alpha or beta release features by default. You will need to explicitly install beta features using the gcloud components install beta command, so option B is the right answer. Option A will install standard gcloud commands. Options C and D are not valid gcloud commands.



#### 12. You want to create a cloud function to transform audio files into different formats. The audio files will be uploaded into Cloud Storage. You want to start transformations as soon as the files finish uploading. Which trigger would you specify in the cloud function to cause it to execute after the file is uploaded?

A. google.storage.object.finalize

B. google.storage.object.upload

C. google.storage.object.archive

D. google.storage.object.metadataUpdate



Answers:

A. The correct trigger in option A is google.storage.object.finalize, which occurs after a file is uploaded. Option B is not a valid trigger name. Option C triggers when a file\
is archived, not uploaded. Option D is triggered when some metadata attribute changes, but not necessarily only after a file uploads.



#### 13. You are defining a cloud function to write a record to a database when a file in Cloud Stor- age is archived. What parameters will you have to set when creating that function?

A. runtime only

B. trigger-resource only

C. runtime, trigger-resource, trigger-event only

D. runtime, trigger-resource, trigger-event, file-type



Answers:

C. The three parameters are runtime, trigger-resource, and trigger-event, as listed in option C. All must be set, so options A and B are incorrect. file-type is not a param- eter to creating a cloud function on Cloud Storage, so option D is incorrect.



#### 14. You’d like to stop using a cloud function and delete it from your project. Which command would you use from the command line to delete a cloud function?

A. gcloud functions delete

B. gcloud components function delete&#x20;

C. gcloud components delete

D. gcloud delete functions



Answers:

A. The correct answer is option A, gcloud functions delete. Option B references components, which is incorrect. You do need to reference components when installing or updating gcloud commands but not when deleting a cloud function, so options B and C are incorrect. Option D is incorrect because the GCP entity type, in this case functions, comes before the name of the operation, in this case delete, in a gcloud command.



#### 15. You have been asked to deploy a cloud function to work with Cloud Pub/Sub. As you review the Python code, you notice a reference to a Python function called base64.b64decode. Why would a decode function be required in a Pub/Sub cloud function?

A. It’s not required and should not be there.

B. Messages in Pub/Sub topics are encoded to allow binary data to be used in places where text data is expected. Messages need to be decoded to access the data in the message.

C. It is required to add padding characters to the end of the message to make all messages the same length.

D. The decode function maps data from a dictionary data structure to a list data structure.



Answers:

B. Messages are stored in a text format, base64, so that binary data can be stored in the message in a text format, so option B is correct. Option A is incorrect; it is needed to map from a binary encoding to a standard text encoding. Option C is incorrect because the function does not pad with extra characters to make them the same length. Option D is incorrect; it does not change dictionary data types into list data types.



#### 16. Which of these commands will deploy a Python cloud function called pub\_sub\_function\_test?

A. gcloud functions deploy pub\_sub\_function\_test

B. gcloud functions deploy pub\_sub\_function\_test --runtime python37

C. gcloud functions deploy pub\_sub\_function\_test --runtime python37 --trigger-topic gcp-ace-exam-test-topic

D. gcloud functions deploy pub\_sub\_function\_test --runtime python --trigger-topic gcp-ace-exam-test-topic



Answers:

C. Option C is correct because it includes the name of the function, the runtime environ- ment, and the name of the Pub/Sub topic. Option A is incorrect because it’s missing both the runtime and the topic. Option B is incorrect because it is missing the topic. Option D is incorrect because the runtime specification is incorrect; you have to specify python37 and not python as the runtime.



#### 17. When specifying a Cloud Storage cloud function, you have to specify an event type, such as finalize, delete, or archive. When specifying a Cloud Pub/Sub cloud function, you do not have to specify an event type. Why is this the case?

A. Cloud Pub/Sub does not have triggers for event types.

B. Cloud Pub/Sub has triggers on only one event type, when a message is published.

C. Cloud Pub/Sub determines the correct event type by analyzing the function code.

D. The statement in the question is incorrect; you do have to specify an event type with Cloud Pub/Sub functions.



Answers:

B. There is only one type of event that is triggered in Cloud Pub/Sub, and that is when a message is published, which is option B. Option A is incorrect; Cloud Pub/Sub has one event type that can have a trigger. Option C is incorrect; Cloud Pub/Sub does not analyze the code to determine when it should be run. Option D is incorrect; you do not have to specify an event type with Cloud Pub/Sub functions.



#### 18. Your company has a web application that allows job seekers to upload résumé files. Some files are in Microsoft Word, some are PDFs, and others are text files. You would like to store all résumés as PDFs. How could you do this in a way that minimizes the time between upload and conversion and with minimal amounts of coding?

A. Write an App Engine application with multiple services to convert all documents to PDF.

B. Implement a Cloud Function on Cloud Storage to execute on a finalize event. The function checks the file type, and if it is not PDF, the function calls a PDF converter function and writes the PDF version to the bucket that has the original.

C. Add the names of all files to a Cloud Pub/Sub topic and have a batch job run at regular intervals to convert the original files to PDF.

D. Implement a Cloud Function on Cloud Pub/Sub to execute on a finalize event. The function checks the file type, and if it is not PDF, the function calls a PDF converter function and writes the PDF version to the bucket that has the original.



Answers:

B. The correct answer is option B because it uses a Cloud Storage finalize event to trigger conversion if needed. There is minimal delay between the time the file is uploaded and when it is converted. Option A is a possibility but would require more coding than option B. Option C is not a good option because files are not converted until the batch job runs. Option D is incorrect because you cannot create a cloud function for Cloud Pub/Sub using a finalize event. That event is for Cloud Storage, not Cloud Pub/Sub.



#### 19. What are options for uploading code to a cloud function?

A. Inline editor

B. Zip upload

C. Cloud source repository

D. All of the above



Answers:

D. All of the options are available along with zip from Cloud Storage.



#### 20. What type of trigger allows developers to use HTTP POST, GET, and PUT calls to invoke a cloud function?

A. HTTP

B. Webhook

C. Cloud HTTP

D. None of the above



Answers:

A. The HTTP trigger allows for the use of POST, GET, and PUT calls, so option A is the correct answer. Webhook and Cloud HTTP are not valid trigger types. Option D is incor- rect because option A is the correct answer.

