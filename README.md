# IAM Roles for Startups



## Motivation

Many startups are now using AWS infrastructure for their company, but being new to AWS, they are unaware of the importance of IAM ROLES. It's hard to remember the importance of your permissions structure when you're just starting out. Our goal is to provide the initial hand holding for the business owner with setting up IAM Roles with basic templates to expedite the process of moving you to AWS. After all, security is of utmost importance, especially starting out. Not starting with the right structure is going to cause accumulation of technical debt.

This project focuses on creating a skeleton of IAM roles for startups or any company moving to AWS. This provides the company with the ability to get started with little or no modifications. For new companies (and even old companies), time is money. The less time you need to spend setting up permissions structures in AWS, the more money you have to build your company in other ways. We are here to help. The project focuses on multi-size startup companies:

- Small - 5 people
- Midsize - ~12 people
- Large - 40 or above

Follow Us On [![alt text][2.1]][2]

[2.1]: http://i.imgur.com/P3YfQoD.png
[2]: http://www.facebook.com/SingaporeTechEntrepreneurs/

## Role of Security


In this project, we try to place security above everything. We are trying to avoid accidental deletions. We are assuming that every team member will log in from known IPs. As an added layer of security, we are making MFA mandatory for every user that logs in, even admins. To add the mandatory MFA, there is a policy called ```forceMfa.json``` that will need to be created and added to a group called ```FORCE_MFA```. Each IAM user to be created, will need to be a part of the ```FORCE_MFA``` group. This policy will deny IAM user's access to AWS resources until they add their MFA and use it to authenticate.


## Assumptions

Based on best practices in AWS, we are working with the following assumptions:

- Presence of generic job roles.
- Every user will log in from the companies external IP
- Use of blacklist instead of whitelist to keep the roles tidy.


## Job Profiles

We are considering job profiles across different verticals, i.e: business, finance, tech and ops.

read [ROLES.md](https://github.com/Singapore-Tech-Entrepreneurs/Startup-AWS-IAM-Roles/blob/master/ROLES.md) for role and its assumption details.

## Setting Up Roles

- Create IAM Policies for each Job Type
- Create IAM Groups for each Job Type with respective IAM Policiy attached
- Add users to IAM groups based on their position
- ALL users need added to the FORCE_MFA group which has the FORCE_MFA policy attached.

## Contributing

- Fork it!
- Create your feature branch: git checkout -b my-new-feature
- stage your feature: git add <changed_file>
- Commit your changes: git commit -m 'feat: add new feature' -m 'add my-new-feature, use it as: my-new-feautre(args)' -m 'closes #26'
- Push to the branch: git push origin my-new-feature
- Submit a pull request :D


## Contributors

- Anthony Petecca @RealityShift
- Padmakar Ojha @dvopsway
- Michael Amurjuev @LawTech Enthusiast
- Kj Venky @kjvenky
