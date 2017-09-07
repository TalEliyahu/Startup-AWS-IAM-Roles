# IAM Roles for Startups



## Motivation

Many startups are now using AWS infrastructure for their company, but being new to AWS, they are unaware of the importance of IAM ROLES. It's hard to remember the importance of your permissions structure when you're just starting out. Our goal is to provide the initial hand holding for the business owner with setting up IAM Roles with basic templates to expedite the process of moving you to AWS. After all, security is of utmost importance, especially starting out. Not starting with the right structure is going to cause accumulation of technical debt.

This project focuses on creating a skeleton of IAM roles for startups or any company moving to AWS. This provides the company with the ability to get started with little or no modifications. The project focuses on multi-size startup companies:

- Small - 5 people
- Midsize - ~12 people
- Large - 40 or above

Follow Us On [![alt text][2.1]][2]

[2.1]: http://i.imgur.com/P3YfQoD.png
[2]: http://www.facebook.com/SingaporeTechEntrepreneurs/

## Role of Security

In this project, we try to place security above everything. We are placing deny on deletions in our policies to stop avoid accidental deletions (this can be changed by the company owner at their own discretion). As an added layer of security, we are making MFA mandatory for every user that logs in, even admins. If anybody logs in without an MFA, the only permissions they will have is to turn on their MFA.

## Assumptions

Based on best practices in AWS, ee are working with the following assumptions:

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

- Padmakar Ojha @dvopsway
- Michael Amurjuev @LawTech Enthusiast
- Kj Venky @kjvenky
