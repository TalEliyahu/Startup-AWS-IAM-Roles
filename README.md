# IAM Roles for Startups

## Motivation

Many startups are now setting up on aws infrastructure and its long before they figure out importance of IAM role, to be fair its of least importance initially because its not worth the time and energy, businesses initially should focus on product itself. But what if there was hand holding and it won't take too much time to setup IAM roles. After all you want to be secure in initial phases. Forget startups even midsize and some large companies make this mistake and later it becomes too much tech debt.

This project focuses on creating skeleton of IAM Roles for startups with which they can get started with little or no modifications. The project focuses on multi size startups.

- Small - 5 people
- Midsize - 12 people
- Large - 40 or above

## Role of security

In this project we trying keep security above everything, we are trying to avoid accidental deletions. We are assuming that every team member will logging in from known IPs. As added layer of security we are making MFA mandatory for every user that logs in, even admins.

## Assumptions

We are working with following assumtions:

- We are assuming generic job roles.
- In case an employees is wearing multiple hats, make sure you
- update the accordingly. We have tried to block certain destructive actions like bucket deletion, accidental terminations for users who are not aws admin like frontend, backend engineers.
- We have tried to blacklist instead of whitelist to keep the roles look more clean.

## Job Profiles

We are considering job profiles across different verticals i.e: business, finance, tech and ops.

read [ROLES.md](https://github.com/Singapore-Tech-Entrepreneurs/Startup-AWS-IAM-Roles/blob/master/ROLES.md) for role and its assumption details.

## Setting up Roles

Create groups based on job profiles and attach policy documents from this project to it. Now create users and assign them to these groups.

## Contributing

- Fork it!
- Create your feature branch: git checkout -b my-new-feature
- stage your feature: git add <changed_file>
- Commit your changes: git commit -m 'feat: add new feature' -m 'add my-new-feature, use it as: my-new-feautre(args)' -m 'closes #26'
- Push to the branch: git push origin my-new-feature
- Submit a pull request :D
