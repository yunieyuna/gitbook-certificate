# Chapter 17. Configuring Access and Security

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

#### 1. What does IAM stand for?

A. Identity and Authorization Management

B. Identity and Access Management

C. Identity and Auditing Management

D. Individual Access Management



Answers:

B. IAM stands for Identity and Access Management, so option B is correct. Option A is incorrect; the A does not stand for authorization, although that is related. Option C is incorrect; the A does not stand for auditing, although that is related. Option D is incorrect. IAM also works with groups, not just individuals.



#### 2. When you navigate to IAM & Admin in Cloud Console, what appears in the main body of the page?

A. Members and roles assigned

B. Roles only

C. Members only

D. Roles and permissions assigned



Answers:

A. Members and their roles are listed, so option A is correct. Options B and C are incorrect because they are missing the other main piece of information provided in the listing. Option D is incorrect; permissions are not displayed on that page.



#### 3. Why are primitive roles classified in a category in addition to IAM?

A. They are part of IAM.

B. They were created before IAM.

C. They were created after IAM.

D. They are not related to access control.



Answers:

B. Primitive roles were created before IAM and provided coarse-grained access controls, so option B is correct. Option A is incorrect; they are used for access control. Option C is incorrect; IAM is the newer form of access control. Option D is incorrect; they do provide access control functionality.



#### 4. A developer intern is confused about what roles are used for. You describe IAM roles as a collection of what?

A. Identities

B. Permissions

C. Access control lists

D. Audit logs



Answers:

B. Roles are used to group permissions that can then be assigned to identities, so option B is correct. Option A is incorrect; roles do not have identities, but identities can be granted roles. Option C is incorrect; roles do not use access control lists. Option D is incorrect; roles do not include audit logs. Logs are collected and managed by Stackdriver Logging.



#### 5. You want to list roles assigned to users in a project called ace-exam-project. What gcloud command would you use?

A. gcloud iam get-iam-policy ace-exam-project

B. gcloud projects list ace-exam-project

C. gcloud projects get-iam-policy ace-exam-project&#x20;

D. gcloud iam list ace-exam-project



Answers:

C. The correct answer is gcloud projects get-iam-policy ace-exam-project, so option C is correct. Option A is incorrect because the resource should be projects and not iam. Option B is incorrect; list does not provide detailed descriptions. Option D is incor- rect because iam and list are incorrectly referenced.



#### 6. You are working in the form displayed after clicking the Add link in the IAM form of IAM & Admin in Cloud Console. There is a parameter called New Members. What items would you enter in that parameter?

A. Individual users only

B. Individual users or groups

C. Roles or individual users

D. Roles or groups



Answers:

B. New members can be users, indicated by their email addresses, or groups, so option B is correct. Option A is incorrect; it does not include groups. Options C and D are incorrect because roles are not added there.



#### 7. You have been assigned the App Engine Deployer role. What operations can you perform?

A. Write new versions of an application only

B. Read application configuration and settings only

C. Read application configuration and settings and write new configurations

D. Read application configuration and settings and write new versions



Answers:

D. Deployers can read application configurations and settings and write new application versions, so option D is correct. Option A is incorrect because it is missing the ability to read configurations and settings. Option B is incorrect because it is missing writing new versions. Option C is incorrect because it references writing new configurations.



#### 8. You want to list permissions in a role using Cloud Console. Where would you go to see that?

A. IAM & Admin; select Roles. All permissions will be displayed.

B. IAM & Admin; select Roles. Check the box next to a role to display the permissions in that role.

C. IAM & Admin; select Audit Logs.

D. IAM & Admin; select Service Accounts and then Roles.



Answers:

B. The correct steps are navigating to IAM & Admin, selecting Roles, and then checking the box next to a role, so option B is correct. Option A is incorrect; all roles are not dis- played automatically. Option C is incorrect; audit logs do not display permissions. Option D is incorrect; there is no Roles option in Service Accounts.



#### 9. You are meeting with an autidor to discuss security practices in the cloud. The auditor asks how you implement several best practices. You describe how IAM predefined roles help to implement which security best practice(s)?

A. Least privilege

B. Separation of duties

C. Defense in depth

D. Options A and B



Answers:

D. Predefined roles help implement both least privilege and separation of duties, so option D is correct. Predefined roles do not implement defense in depth by themselves but could be used with other security controls to implement defense in depth.



#### 10. What launch stages are available when creating custom roles?

A. Alpha and beta only

B. General availability only

C. Disabled only

D. Alpha, beta, general availability, and disabled



Answers:

D. The four launch stages available are alpha, beta, general availability, and disabled, so option D is correct.



#### 11. The gcloud command to create a custom role is what?

A. gcloud project roles create

B. gcloud iam roles create

C. gcloud project create roles

D. gcloud iam create roles



Answers:

B. The correct answer, option B, is gcloud iam roles create. Option A is incorrect because it references project instead of iam. Option C is incorrect because it references project instead of iam, and the terms create and roles are out of order. Option D is incorrect because the terms create and roles are out of order.



#### 12. A DevOps engineer is confused about the purpose of scopes. Scopes are access controls that are applied to what kind of resources?

A. Storage buckets

B. VM instances

C. Persistent disks

D. Subnets



Answers:

B. Scopes are permissions granted to VM instances, so option B is correct. Scopes in com- bination with IAM roles assigned to service accounts assigned to the VM instance deter- mine what operations the VM instance can perform. Options A and C are incorrect; scopes do not apply to storage resources. Option D is incorrect; scopes do not apply to subnets.



#### 13. A scope is identified using what kind of identifier?

A. A randomly generated ID

B. A URL beginning with https://www.googleserviceaccounts/

C. A URL beginning with https://www.googleapis.com/auth/

D. A URL beginning with https://www.googleapis.com/auth/PROJECT\_ID]



Answers:

C. Scope identifiers start with https://www.googleapis.com/auth/ and are followed by a scope-specific name, such as devstorage.read\_only or logging.write, so option C is correct. Option A is incorrect; scope IDs are not randomly generated. Option B is incorrect; the domain name is not googleserviceaccounts. Option D is incorrect; scopes are not linked directly to projects.



#### 14. A VM instance is trying to read from a Cloud Storage bucket. Reading the bucket is allowed by IAM roles granted to the service account of the VM. Reading buckets is denied by the scopes assigned to the VM. What will happen if the VM tries to read from the bucket?

A. The application performing the read will skip over the read operation.

B. The read will execute because the most permissive permission is allowed.

C. The read will not execute because both scopes and IAM roles are applied to determine what operations can be performed.

D. The read operation will succeed, but a message will be logged to Stackdriver Logging.



Answers:

C. Both scopes and IAM roles assigned to service accounts must allow an operation for it to succeed, so option C is correct. Option A is incorrect; access controls do not affect the flow of control in applications unless explicitly coded for that. Option B is incorrect; the most permissive permission is not used. Option D is incorrect; the operation will not succeed.



#### 15. What are the options for setting scopes in a VM?

A. Allow Default Access and Allow Full Access only

B. Allow Default Access, Allow Full Access, and Set Access for Each API

C. Allow Full Access or Set Access For Each API only

D. Allow Default Access and Set Access For Each API only



Answers:

B. The options for setting scopes are: Allow Default Access, Allow Full Access, and Set Access For Each API, so option B is correct. Option A is incorrect; it is missing Set Access For Each API. Option C is incorrect; it is missing Allow Default Access. Option D is incor- rect; it is missing Allow Full Access.



#### 16. What gcloud command would you use to set scopes?

A. gcloud compute instances set-scopes

B. gcloud compute instances set-service-account&#x20;

C. gcloud compute service-accounts set-scopes

D. gcloud compute service-accounts define-scopes



Answers:

B. The correct command is gcloud compute instances set-service-account, so option B is correct. Option A is incorrect; there is no set-scopes command verb. Option C is incorrect; the command verb is not set-scopes. Option D is incorrect; there is no command verb define-scopes.



#### 17. What gcloud command would you use to assign a service account when creating a VM?

A. gcloud compute instances create \[INSTANCE\_NAME]

\--service-account \[SERVICE\_ACCOUNT\_EMAIL]

B. gcloud compute instances create-service-account \[INSTANCE\_NAME]\[SERVICE\_ACCOUNT\_EMAIL]

C. gcloud compute instances define-service-account \[INSTANCE\_NAME]\[SERVICE\_ACCOUNT\_EMAIL]

D. gcloud compute create instances-service-account \[INSTANCE\_NAME]\[SERVICE\_ACCOUNT\_EMAIL]



Answers:

A. You can assign a service account when creating a VM using the create command. Option B is incorrect; there is no create-service-account command verb. Option C is incorrect; there is no define-service-account command verb. Option D is incorrect; there is no instances-service-account command; also, create should come at the end of the command.



#### 18. What GCP service is used to view audit logs?

A. Compute Engine

B. Cloud Storage

C. Stackdriver Logging

D. Custom logging



Answers:

C. Stackdriver Logging collects, stores, and displays log messages, so option C is correct. Option A is incorrect; Compute Engine does not manage logs. Option B is incorrect; Cloud Storage is not used to view logs, although log files can be stored there. Option D is incor- rect; custom logging solutions are not GCP services.



#### 19. What options are available for filtering log messages when viewing audit logs?

A. Period time and log level only

B. Resource, type of log, log level, and period of time only

C. Resource and period of time only

D. Type of log only



Answers:

B. Logs can be filtered by resource, type of logs, log level, and period of time only, so option B is correct. Options A, C, and D are incorrect because they are missing at least one option.



#### 20. An auditor needs to review audit logs. You assign read-only permission to a custom role you create for auditors. What security best practice are you following?

A. Defense in depth

B. Least privilege

C. Separation of duties

D. Vulnerability scanning



Answers:

B. This is an example of assigning the least privilege required to perform a task, so option B is correct. Option A is incorrect; defense in depth combines multiple security controls. Option C is incorrect because it is having different people perform sensitive tasks. Option D is incorrect; vulnerability scanning is a security measure applied to applications that helps reveal potential vulnerabilities in an application that an attacker could exploit.

