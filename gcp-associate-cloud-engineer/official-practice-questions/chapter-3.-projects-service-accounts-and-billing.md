# Chapter 3. Projects, Service Accounts, and Billing

#### Understanding Level:

* O: Understand the whole question
* △: Not sure about part of the question
* ×: Don't understand the question

| Question Number | Trial 1 | Trial 2 | Trial 3 |
| --------------- | ------- | ------- | ------- |
| 1               |         |         |         |
| 2               |         |         |         |
| 3               |         |         |         |
| 4               |         |         |         |
| 5               |         |         |         |
| 6               |         |         |         |
| 7               |         |         |         |
| 8               |         |         |         |
| 9               |         |         |         |
| 10              |         |         |         |
| 11              |         |         |         |
| 12              |         |         |         |
| 13              |         |         |         |
| 14              |         |         |         |
| 15              |         |         |         |
| 16              |         |         |         |
| 17              |         |         |         |
| 18              |         |         |         |
| 19              |         |         |         |
| 20              |         |         |         |

#### 1. You are designing cloud applications for a healthcare provider. The records management application will manage medical information for patients. Access to this data is limited to a small number of employees. The billing department application will have insurance and payment information. Another group of employees will have access billing information. In addition, the billing system will have two components: a private insurance billing system and a government payer billing system. Government regulations require that software used to bill the government must be isolated from other software systems. Which of the follow- ing resource hierarchies would meet these requirements and provide the most flexibility to adapt to changing requirements?

A. One organization, with folders for records management and billing. The billing folder would have private insurer and government payer folders within it. Common constraints would be specified in organization-level policies. Other policies would be defined at the appropriate folder.

B. One folder for records management, one for billing, and no organization. Policies defined at the folder level.

C. One organization, with folders for records management, private insurer, and govern- ment payer below the organization. All constraints would be specified in organization- level policies. All folders would have the same policy constraints.

D. None of the above.



Answers:

A. Option A, the correct answer, separates the two main applications into their own folders and further allows separating private insurance from government payer, but using folders for each. This satisfies the regulatory need to keep the government payer software isolated from other software. Option B does not include an organization, which is the root of the resource hierarchy. Option C is not flexible with regard to differences in constraints on different applications. Option D is false because option A does meet the requirements.



#### 2. When you create a hierarchy, you can have more than one of which structure?

A.  Organization only

B. Folder only

C. Folder and project

D. Project only



Answers:

C. Resource hierarchies have a single organization at the root, which makes option C correct. Below that, there are folders that can contain other folders or projects. Folders can contain multiple folders and multiple projects.



#### 3. You are designing an application that uses a series of services to transform data from its original form into a format suitable for use in a data warehouse. Your transformation appli- cation will write to the message queue as it processes each input file. You don’t want to give users permission to write to the message queue. You could allow the application to write to the message queue by using which of the following?

A. Billing account

B. Service account

C. Messaging account

D. Folder



Answers:

B. Service accounts are designed to give applications or VMs permission to perform tasks. Billing accounts are for associating charges with a payment method. Folders are part of resource hierarchies and have nothing to do with enabling an application to perform a task. Messaging accounts are a fictitious option.



#### 4. Your company has a number of policies that need to be enforced for all projects. You decide to apply policies to the resource hierarchy. Not long after you apply the policies, an engineer finds that an application that had worked prior to implementing policies is no longer working. The engineer would like you to create an exception for the application. How can you override a policy inherited from another entity in the resource hierarchy?

A. Inherited policies can be overridden by defining a policy at a folder or project level.

B. Inherited policies cannot be overridden.

C. Policies can be overridden by linking them to service accounts.

D. Policies can be overridden by linking them to billing accounts.



Answers:

B. Inherited policies can be overridden by defining a policy at a folder or project level. Service accounts and billing accounts are not part of the resource hierarchy and are not involved in overriding policies.

(Actual answer is A?)



#### 5. Constraints are used in resource hierarchy policies. Which of the following are types of constraints allowed?

A. Allow a specific set of values

B. Deny a specific set of values

C. Deny a value and all its child values

D. Allow all allowed values

E. All of the above



Answers:

E. All of the listed types of constraints are supported in policies.



#### 6. A team with four members needs you to set up a project that needs only general permissions for all resources. You are granting each person a primitive role for different levels of access, depending on their responsibilities in the project. Which of the following are not included as primitive roles in Google Cloud Platform?

A. Owner&#x20;

B. Publisher&#x20;

C. Editor

D. Viewer



Answers:

B. Option B is the correct answer because Publisher is not a primitive role. Owner, Editor, and Viewer are the three primitive privileges in GCP.



#### 7. You are deploying a new custom application and want to delegate some administration tasks to DevOps engineers. They do not need all the privileges of a full application admin- istrator, but they do need a subset of those privileges. What kind of role should you use to grant those privileges?

A. Primitive&#x20;

B. Predefined&#x20;

C. Advanced&#x20;

D. Custom



Answers:

D. Primitive roles only include the Owner, Editor, and View permissions. Predefined roles are designed for GCP products and services, like App Engine and BigQuery. For a custom application, you can create sets of privileges that give the user with that role as much per- mission as needed but not more.



#### 8. An app for a finance company needs access to a database and a Cloud Storage bucket. There is no predefined role that grants all the needed permissions without granting some permissions that are not needed. You decide to create a custom role. When defining custom roles, you should follow which of the following principles?

A. Rotation of duties

B. Least principle

C. Defense in depth&#x20;

D. Least privilege



Answers:

D. Users should have only the privileges that are needed to carry out their duties. This is the principle of least privilege. Rotation of duties is another security principle related to having different people perform a task at a different times. Defense in depth is the practice of using multiple security controls to protect the same asset. Option B is not a real security principal.



#### 9. How many organizations can you create in a resource hierarchy?&#x20;

A. 1

B. 2

C. 3

D. Unlimited



Answers:

A. A resource hierarchy has only one organization, which makes option A correct. You can, however, create multiple folders and projects within a resource hierarchy.



#### 10. You are contacted by the finance department of your company for advice on how to auto- mate payments for GCP services. What kind of account would you recommend setting up?

A. Service account&#x20;

B. Billing account&#x20;

C. Resource account&#x20;

D. Credit account



Answers:

B. In option B, the correct answer, the billing account is used to specify payment information and should be used to set up automatic payments. Service accounts are used to grant privileges to a VM and are not related to billing and payments. Resource accounts and credit accounts do not exist.



#### 11. You are experimenting with GCP for your company. You do not have permission to incur costs. How can you experiment with GCP without incurring charges?

A. You can’t; all services incur charges.

B. You can use a personal credit card to pay for charges.

C. You can use only free services in GCP.

D. You can use only serverless products, which are free to use.



Answers:

C. GCP offers a free service level for many products, which makes option C the correct answer. You can use these services without having to set up a billing account. Google charges for serverless products, such as Cloud Functions and App Engine, when customers exceed the amount allowed under the free tier.



#### 12. Your DevOps team has decided to use Stackdriver monitoring and logging. You have been asked to set up Stackdriver workspaces. When you set up a Stackdriver workspace, what kind of resource is it associated with?

A. A Compute Engine instance only

B. A Compute Engine instance or Kubernetes Engine cluster only

C. A Compute Engine instance, Kubernetes Engine cluster, or App Engine app

D. A project



Answers:

D. Stackdriver Workspaces are linked to projects, not individual resources like VM instances, clusters, or App Engine apps, so option D is correct. Options A, B, and C all incorrectly indicate that Workspaces are associated with individual compute resources.



#### 13. A large enterprise is planning to use GCP across a number of subdivisions. Each subdivision is managed independently and has its own budget. Most subdivisions plan to spend tens of thousands of dollars per month. How would you recommend they set up their billing account(s)?

A. Use a single self-service billing account.

B. Use multiple self-service billing accounts.

C. Use a single invoiced billing account.

D. Use multiple invoiced billing accounts.



Answers:

D. Large enterprises should use invoicing when incurring large charges, which makes option D the right answer. A self-service account is appropriate only for amounts that are within the credit limits of credit cards. Since the subdivisions are independently managed and have their own budgets, each should have its own billing accounts.



#### 14. An application administrator is responsible for managing all resources in a project. She wants to delegate responsibility for several service accounts to another administrator. If additional service accounts are created, the other administrator should manage those as well. What is the best way to delegate privileges needed to manage the service accounts?

A. Grant iam.serviceAccountUser to the administrator at the project level.

B. Grant iam.serviceAccountUser to the administrator at the service account level.

C. Grant iam.serviceProjectAccountUser to the administrator at the project level.

D. Grant iam.serviceProjectAccountUser to the administrator at the service account level.



Answers:

A. When a user is granted iam.serviceAccountUser at the project level, that user can manage all service accounts in the project, so option A is correct. If a new service account is created, they will automatically have privilege to manage that service account. You could grant iam.serviceAccountUser to the administrator at the service account level, but that would require setting the role for all service accounts. If a new service account is created, the application administrator would have to grant iam.serviceAccountUser to the other administrator on the new service account. iam.serviceProjectAccountUser is a fictional role.



#### 15. You work for a retailer with a large number of brick and mortar stores. Every night the stores upload daily sales data. You have been tasked with creating a service that verifies the uploads every night. You decide to use a service account. Your manager questions the security of your proposed solution, particularly about authenticating the service account. You explain the authentication mechanism used by service accounts. What authentication mechanism is used?

A. Username and password

B. Two-factor authentication

C. Encrypted keys

D. Biometrics



Answers:

C. When a service account is created, Google generates encrypted keys for authentication, making option C correct. Usernames and passwords are not an option for service accounts. Two-factor authentication is an authentication practice that requires two forms of authentication, such as a username password pair and a code from an authentication device. Biometrics cannot be used by services and is not an option.



#### 16. What objects in GCP are sometimes treated as resources and sometimes as identities?&#x20;

A. Billing accounts

B. Service accounts

C. Projects

D. Roles



Answers:

B. Service accounts are resources that are managed by administrators, but they also function as identities that can be assigned roles, which makes option B the correct answer. Billing accounts are not related to identities. Projects are not identities; they cannot take on roles. Roles are resources but not identities. They can take on privileges, but those privi- leges are used only when they are attached to an identity.



#### 17. You plan to develop a web application using products from the GCP that already include established roles for managing permissions such as read-only access or the ability to delete old versions. Which of the following roles offers these capabilities?

A. Primitive roles&#x20;

B. Predefined roles&#x20;

C. Custom roles

D. Application roles



Answers:

B. Predefined roles are defined for a particular product, such as App Services or Compute Engine, so option B is the right answer. They bundle privileges often needed together when managing or using a service. Primitive roles are building blocks for other roles. Custom roles are created by users to meet their particular needs; Application roles is a fictitious role.



#### 18. You are reviewing a new GCP account created for use by the finance department. An auditor has questions about who can create projects by default. You explain who has privileges to create projects by default. Who is included?

A. Only project administrators

B. All users

C. Only users without the role resourcemanager.projects.create

D. Only billing account users



Answers:

B. By default all users in an organization can create projects, which makes option B correct. The role resourcemanager.projects.create is the role that allows users to create projects. The billing account is not associated with creating projects.



#### 19. How many projects can be created in an account?&#x20;

A. 10

B. 25

C. There is no limit.

D. Each account has a limit determined by Google.



Answers:

D. The maximum number of organizations is determined on a per-account basis by Google, so option D is the correct answer. If you need additional organizations, you can contact Google and ask for an increase in your limit.



#### 20. You are planning how to grant privileges to users of your company’s GCP account. You need to document what each user will be able to do. Auditors are most concerned about a role called Organization IAM roles. You explain that users with that role can perform a number of tasks, which include all of the following except which one?

A. Defining the structure of the resource hierarchy

B. Determining what privileges a user should be assigned

C. Defining IAM policies over the resource hierarchy

D. Delegating other management roles to other users



Answers:

B. Users with the Organization IAM role are not necessarily responsible for determining what privileges should be assigned to users. That is determined based on the person’s role in the organization and the security policies established within the organization, which makes option B correct.

