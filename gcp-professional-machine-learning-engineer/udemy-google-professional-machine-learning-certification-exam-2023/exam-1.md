# Exam 1

## Q1

* The data collected must not leave the region in which the call originated, and no Personally Identifiable Information (PII) can be stored or analyzed
  * \-> Dataflow - Unified stream and batch data proessing that's serverless, fast, and cost-effective
* The data science team has a third-party tool for visualization and access which requires a SQL ANSI-2011 compliant interface.
  * \-> Bigquery - Good for analytics and dashboards

## Q2

* You are asked to build a model that will recommend new products to the user based on their purchase behavior and similarity with other users.
  * \-> Build a collaborative-based filtering model

## Q3

* Adjust precision & recall

Precision = TruePositives / (TruePositives + FalsePositives)

Recall = TruePositives / (TruePositives + FalseNegatives)

## Q4

* A variety of on-premises data marts
* Integrating data across the servers
* A fully managed, cloud-native data integration service
* Allow you lower the total cost of work and reduce repetitive work
* Prefer a codeless interface for building Extract, Transform, Load (ETL) process
  * \-> Cloud Data Fusion:&#x20;
    * Fully managed, cloud-native data integration service
      * Designed to simplify the process of building and managing ETL pipelines across a variety of data sources and targets.
      * Reference: [https://cloud.google.com/data-fusion](https://cloud.google.com/data-fusion)

## Q5

* Regulated insurance company
* Build insurance approval model
  * \-> Several factors
    * Traceability: It's important to be able to trace the data used to build the model and the decisions made by the model. This is important for transparency and accountability.
    * Reproducibility: The model should be built in a way that allows for its reproducibility. This means that other researchers should be able to reproduce the same results using the same data and methods.
    *   Explainability: The model should be able to provide clear and understandable explanations for its decisions.

        This is important for building trust with customers and ensuring compliance with regulations.
    * Other factors that may also be important to consider, depending on the specific context of the insurance company and its customers, include data privacy and security, fairness, and bias mitigation.

## Q6

* input-bound
  * In computer science, I/O bound refers to a condition in which the time it takes to complete a computation is determined principally by the period spent waiting for input/output operations to be completed, which can be juxtaposed with being CPU bound. This circumstance arises when the rate at which data is requested is slower than the rate it is consumed or, **in other words, more time is spent requesting data than processing it.**
  * Ref: [https://en.wikipedia.org/wiki/I/O\_bound](https://en.wikipedia.org/wiki/I/O\_bound)
* A. Use the interleave option for reading data. - Yes, that helps to parallelize data reading.
  * "interleave" in computer science
    * is the scheduling or switching between various tasks or processes to enable simultaneous or concurrent execution.
    * Ref: [https://www.quora.com/What-is-the-definition-of-interleaving-in-computer-science](https://www.quora.com/What-is-the-definition-of-interleaving-in-computer-science)
* B. Reduce the value of the repeat parameter. - No, this is only to repeat rows of the dataset.&#x20;
* C. Increase the buffer size for the shuttle option. - No, there is only a shuttle option.&#x20;
* D. Set the prefetch option equal to the training batch size. - Yes, this will pre-load the data.&#x20;
* E. Decrease the batch size argument in your transformation. - No, could be even slower due to more I/Os.

## Q7



## Q8

* Model performing poorly due to a change in the distribution of the input data.
  * \-> Create alerts to monitor for skew, and retrain the model
  * Ref: [https://developers.google.com/machine-learning/guides/rules-of-ml/#rule\_37\_measure\_trainingserving\_skew](https://developers.google.com/machine-learning/guides/rules-of-ml/#rule\_37\_measure\_trainingserving\_skew)

## Q9

* Migrate from op-premises to cloud.
* Want to minimize code refactoring and infrastructure overhead for easier migration
  * \-> Vertex AI for distributed training.

## Q10

* Have trained model on Vertex AI
* Want to use the trained model on data in Bigquery
* Want to minimizing computational overhead
  * \-> Export the model to BigQuery ML

## Q11

* You have created an ML model and want to use the data to refresh your model as soon as new data is available.
* As part of your CI/CD workflow, you want to automatically run a Kubeflow Pipelines training job on Google Kubernetes Engine (GKE).
  * \-> <mark style="background-color:blue;">**Cloud Pub/Sub**</mark>
    * Is a fully managed, real time messaging service that allows you to send and receive messages between independent applications.
    * Ref: [https://www.youtube.com/watch?v=cvu53CnZmGI\&ab\_channel=GoogleCloudTech](https://www.youtube.com/watch?v=cvu53CnZmGI\&ab\_channel=GoogleCloudTech)
    * Ref from Calvin:&#x20;
      * [https://walnut-decision-6a6.notion.site/Basics-49c877383b3d4c31a0aff283b273db86](https://walnut-decision-6a6.notion.site/Basics-49c877383b3d4c31a0aff283b273db86)
      * [https://walnut-decision-6a6.notion.site/Basics-da7cf5e5fe0348129c89133357ad5802](https://walnut-decision-6a6.notion.site/Basics-da7cf5e5fe0348129c89133357ad5802)
    * Resource Limits
      * [https://cloud.google.com/pubsub/quotas#quotas](https://cloud.google.com/pubsub/quotas#quotas)
      * Project: 10,000 topics
      * Topic: 10,000 attached subscriptions

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

## Q12

* Hypertuning is taking longer than expected and is delaying the downstream processes.
* How to speed up this job without significantly compromising model's effectiveness
  * \-> Set the early stopping parameter to TRUE
  * \-> Decrease the maximum number of trials during subsequent trainined phases.

## Q13

* Bank with millions of users
* Current model predicts customers' account balances 3 days in the future.
* Will notify users when account balance is likely to drop below $25.
  * \-> 1. Build a notification system on Firebase.
  * \-> 2. Register each user with a user ID on the Firebase Cloud Messaging server
* Firebase Cloud Messaging (FCM)
  * is a cross-platform messaging solution that lets you reliably send messages at no cost.
  * Ref: [https://firebase.google.com/docs/cloud-messaging](https://firebase.google.com/docs/cloud-messaging)

## Q14

* Ref: [https://developers.google.com/machine-learning/crash-course/feature-crosses/check-your-understanding](https://developers.google.com/machine-learning/crash-course/feature-crosses/check-your-understanding)

## Q15

* You have been asked to develop a solution to classify incoming calls by product so that requests can be more quickly routed to the correct support team.
* You have already transcribed the calls using the Speech-to-Text API.
* You want to minimize data preprocessing and development time.
  * \-> AutoML Natural Language to extract custom entities

## Q16

* Dataset with 100B records stored in several CSV files.
* How to improve the input/output execution performance?
  * \-> Convert CSV files into shards of TFRecords
    * Splitting TFRecord files into shards helps you shuffle large datasets that won't fit into memory.
    * Ref: [https://datascience.stackexchange.com/questions/16318/what-is-the-benefit-of-splitting-tfrecord-file-into-shards](https://datascience.stackexchange.com/questions/16318/what-is-the-benefit-of-splitting-tfrecord-file-into-shards)
  * \-> <mark style="color:red;">**Storing data in Cloud Storage (?)**</mark>

## Q17

* Need to use your ML model on the aggregated data collected at the end of each day (Which means real-time service is not necessary).
* With minimal manual intervention
  * \-> Use batch prediction functionality of Vertex AI

## Q18

* <mark style="background-color:blue;">**Data Catalog**</mark>
  * Highly scalable data discovery and metadata management service.
  * Provides a simple-to-use search interface
  * And an API for programmatic access
    * Ref: [https://cloud.google.com/data-catalog/docs/concepts/overview](https://cloud.google.com/data-catalog/docs/concepts/overview)
* Thousands of datasets with accurate descriptions for each table
* Want to search proper Bigquery table
  * \-> Data Catalog

## Q19

* Nested cross-validation for time series model

## Q20



## Q21

* Build ML model for detecting real-time anomalies in sensor data
* Using Pub/Sub to handle incoming requests
* Storing results for further analytics and visualization
  * \-> Vertex AI: model creation
  * \-> Dataflow: Data transformation
  * \-> Bigquery: Analytics and visualization



* <mark style="background-color:blue;">**Dataflow**</mark>
  * Serverless, fast, and cost-effective data-processing service for stream and batch data
  * Remove operational overhead by automating the infrastructure provisioning and auto-scaling as data grows
    * ref: [https://cloud.google.com/dataflow/docs/machine-learning](https://cloud.google.com/dataflow/docs/machine-learning)

## Q22



## Q23

* Imbalance Data
  * Downsample
  * Upweight
    * Ref: [https://developers.google.com/machine-learning/data-prep/construct/sampling-splitting/imbalanced-data#downsampling-and-upweighting](https://developers.google.com/machine-learning/data-prep/construct/sampling-splitting/imbalanced-data#downsampling-and-upweighting)

## Q24

* Serverless tool with SQL syntax
  * \-> Bigquery
  * (Data Fusion is not SQL syntax)
  * (Dataproc is not serverless)
  * (Cloud SQL is not serverless)

## Q25

* Vertex AI support all the frameworks, including Keras, PyTorch, theano, Scikit-learn, and custom library.

## Q26

* Test set shuold represent ground truth distribution ot infer credible model evaluation.
* So once new products become available, test set should be updated to reflect the new product distribution.

## Q27

Kubeflow Pipeline

* Ref: [https://www.kubeflow.org/docs/components/pipelines/v1/introduction/](https://www.kubeflow.org/docs/components/pipelines/v1/introduction/)

## Q28

CI/CD for Kubeflow pipelines.

* At the heart of tひひhis architecture is Cloud Build, infrastructure.

## Q29

sparse categorical cross-entropy



## Q30



## Q31



## Q32



## Q33



## Q34



## Q35



## Q36



## Q37



## Q38



## Q39



## Q40



## Q41



## Q42



## Q43



## Q44



## Q45



## Q46



## Q47



## Q48



## Q49



## Q50



## Q51



## Q52



## Q53



## Q54



## Q55



## Q56



## Q57



## Q58



## Q59



## Q60















&#x20;
