# Infrastructure Diagram for Small Startup



## 10,000 Foot Overview

In our diagram, we show a demo of how we suggest the infrastructure could be made for a small startup. In this diagram, everything is cloud based whether it's managed by the startup or 3rd party. The IAM roles you see are examples of how IAM roles would fit into this infrastructure but keep in mind, they would only be able to support AWS resources.

## 3rd Party Web Apps

We utilize several 3rd party web applications to help save cost and create efficiencies for our startups. We assume the use of SendBird for chat with customers, G Suite for email within the startup, GitLab for version control, and ASANA for ticket and team tracking. We also will be utilizing CloudFlare for DDoS protection against our web application servers.


## AWS Infrastructure

We will utilize the following services in AWS:

- VPC
- Route53
- Elasticbeanstalk
- CloudWatch
- S3

The VPC will contain 3 subnets - Public, Private, and DB layers. Create a NAT Gateway for NAT'ing the private and db layer. The security between layers will be controleld with security groups in EC2. IAM Roles will be made (see the other documents in this repo) to help control access to the AWS resources.
