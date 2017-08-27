# A Typical Business organisation

**Assumption that our startup using the following:**

**Google Apps:**  For emails, docs and other shared files.

**Marketing:**  Mixpanel, Google Analytics

**Code Repository:** Github / Bitbucket / Gitlab (Instead of AWS services)

**Database:** RDS, DynamoDB or NOSQL on EC2.

\*No one will have full IAM access unless he is architect or above.
Pipelines will be used from the code repository. (Either Bitbucket pipelines or Gitlab Pipelines) (Instead of AWS services)

## Role 1:  Business Owner

**Description:**  Ultimate owner of the business / CEO / Founder

Everything including billing. Owners should setup the Multi Factor Authentication. All the others users (including admin/ctos) should only login via IAM logins. Owner can set up an IAM role to share billing settings with CTO but this should be done via console.

**AWS Resource Permissions:** Everything from the workplace IP (Static IP)

## Role 2:  Cloud Architect

**Description:**  Owner of the cloud infrastructure and maintenance.

Everything including billing. Logs in using IAM role. Owner should setup a IAM role to share billing settings with Architect but this should be done via console.

**AWS Resource Permissions:** Everything from the workplace IP (Static IP)

## Role 3:  Data Architect

**Description:**  Responsible for organisational Data.

Needs permission to everything below the data layer and resources specific to it.

**AWS Resource Permissions:**

- RDS
- Redshift
- Simple Storage Service (S3)
- DynamoDB
- Kinesis
- EMR
- Data pipelines
- Simple DB
- SQS
- SNS


## Role 4:  Data Scientist**

**Description:**  Responsible for organisational Data compute. I dont see a much difference between both of them but we can discuss this further.

Needs permission to everything below the data layer and resources specific to it.

**AWS Resource Permissions:**

- RDS
- Redshift
- Simple Storage Service (S3)
- DynamoDB
- Kinesis
- EMR
- Data pipelines
- Simple DB
- SQS
- SNS


## Role 5:  Database Admin**

**Description:**  Responsible for organisational Database Maintenance.

Needs permission to everything that stores data persistently. Sometimes even cloudsearch, becomes important if they become part of the consumer infrastructure.

**AWS Resource Permissions:**

- RDS
- Redshift
- Simple Storage Service (S3)
- DynamoDB
- Simple DB
- SQS
- SNS


## Role 6:  Frontend Developer**

**Description:**  Responsible for development of user facing front-end.

Needs permission to debug issues related to frontend and setup some notifications if needed.

**AWS Resource Permissions:**

- Code commit
- Cloudfront to check and handle caching issues if needed.
- Simple Storage Service (S3)
- SQS
- SNS
- Route53

## Role 7:  Backend Developer**

**Description:**  Responsible for development and monitoring of backend APIS

Needs permission to debug issues related to frontend and setup some notifications if needed.

**AWS Resource Permissions:**

- Code commit
- Cloudfront to check and handle caching issues if needed.
- EC2
- Lambda
- RDS
- Cloudsearch
- Elastic Search
- Simple Storage Service (S3)
- API Gateway
- CloudTrail
- SQS
- SNS
- Key Management
- Elastic Beanstalk
- Cloud Trail
- XRay
- Cognito

## Role 8:  FullStack Developer**

**Description:**  Responsible for both the frontend and backend developer.

Needs permission to debug issues related to frontend and setup some notifications if needed.-

**AWS Resource Permissions:**

- Code commit
- Cloudfront to check and handle caching issues if needed.
- EC2
- Lambda
- RDS
- Cloudsearch
- Elastic Search
- Simple Storage Service (S3)
- API Gateway
- CloudTrail
- SQS
- SNS
- Key Management
- Elastic Beanstalk
- Cloud Trail
- XRay
- Cognito

## Role 9:  Mobile Developer**

**Description:**  Responsible for mobile apps development and tracings. His work is more close to frontend developer than backend development.

**AWS Resource Permissions:**

- Code commit
- Cloudfront to check and handle caching issues if needed.
- SQS
- SNS
- Cloud Trail
- XRay
- Cognito
- Cloud Watch
- Device Farm
- Mobile analytics
- Mobile targetting

## Role 10:  Marketing Technologist**

**Description:**  Responsible for marketing strategies.

**Notes:** Doesn&#39;t need any access from AWS. He is more focused on tools like Google analytics, Asana, Project management tools.

## Role 11:  SEO Consultant**

**Description:**  Responsible for SEO strategies and Content Marketing.

**Notes:** Doesn&#39;t need any access from AWS. He is more focused on tools like Google analytics.

## Role 12:  Web analytics**

**Description:**  Responsible for SEO strategies and Web analytics.

**Notes:** Doesn&#39;t need any access from AWS. He is more focused on tools like Google analytics.

## Role 13:  Digital Marketing Manager**

**Description:**  Responsible for SEO strategies and Web analytics.

**Notes:** Doesn&#39;t need any access from AWS. He is more focused on tools like Google analytics and A/B testing tools.

## Role 14, 15, 16, 17, 18:  All These are content or Marketting Roles**

**Notes:** Doesn&#39;t need any access from AWS.

## Role 19: UI/UX Designer**

**Notes:** Doesn&#39;t need any access from AWS.

## Role 20: Software developer**

**Description:**  Responsible for development and monitoring of backend APIS. I am not sure how this differs from the Backend or frontend developer role.

Needs permission to debug issues related to frontend and setup some notifications if needed.

**AWS Resource Permissions:**

- Code commit
- Cloudfront to check and handle caching issues if needed.
- EC2
- Lambda
- RDS
- Cloudsearch
- Elastic Search
- Simple Storage Service (S3)
- API Gateway
- CloudTrail
- SQS
- SNS
- Key Management
- Elastic Beanstalk
- Cloud Trail
- XRay
- Cognito

**Notes:** Roles mentioned in the article seems to be to descriptive and most of them fit into fullstack/backend or frontend developer role.

## Role 21: Framework Specialists**

**Description:**  Responsible for both the frontend and backend developer.

Needs permission to debug issues related to frontend and setup some notifications if needed.

**AWS Resource Permissions:**

- Code commit
- Cloudfront to check and handle caching issues if needed.
- EC2
- Lambda
- RDS
- Cloudsearch
- Elastic Search
- Simple Storage Service (S3)
- API Gateway
- CloudTrail
- SQS
- SNS
- Key Management
- Elastic Beanstalk
- Cloud Trail
- XRay
- Cognito

## Role 22: Data modeller**

Doesn&#39;t need any access from AWS. This job is more abstract than actual practical implementation on AWS.

## Role 23: Technical Lead.**

A technical lead is the leader of a group of developers.

**AWS Resource Permissions:**

- Code commit
- Cloudfront to check and handle caching issues if needed.
- EC2
- Lambda
- RDS
- Cloudsearch
- Elastic Search
- Simple Storage Service (S3)
- API Gateway
- CloudTrail
- SQS
- SNS
- Key Management
- Elastic Beanstalk
- Cloud Trail
- XRay
- Cognito

## Role 24: Devops manager**

**Description:** A DevOps Manager is the bridge between developer, quality, and technology teams – helping them understand each other tasks and situations so that they can work together to get the best results. He will require permissions close to the CTO.

**AWS Resource Permissions:**

- Code commit
- Code build
- Code deploy
- Code pipeline
- Code star
- XRay
- EC2
- Lambda
- RDS
- Cloudsearch
- Elastic Search
- Simple Storage Service (S3)
- API Gateway
- CloudTrail
- SQS
- SNS
- Key Management
- Elastic Beanstalk
- Cloud Trail
- XRay
- Cognito

## Role 25, 26 : Management Roles (No AWS)**

## Role 27: Security Specialist**

**Description:** The critical role you&#39;ll play as a security specialist will mean you&#39;ll analyze and maintain security of data, systems, and equipment and investigate any breaches to prevent them in the future. There are two types of security that is needed, internal and external. Internal security refers to protecting resources from the internal company employees and External security refers to protecting from external access.

Considering how important this role is. I usually prefer a very all resources access to ensure that data is secure across the system.

**AWS Resource Permissions:** All

There are two approaches people take for QA testing. Automated and manual:

## Role 28: Manual QA Specialist**

Doesn&#39;t need any access from AWS. Usually they test on browsers, but scope is in general very vague.

## Role 29: Automated QA Specialist**

This job is closer to backend developer. As he will write the QA tests and Devops guys is responsible to run them as a part of deployment process.
