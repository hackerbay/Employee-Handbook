---
layout: markdown_page
title: Checklist for becoming a GitHost Admin
---

Create an issue with this checklist on the [support team issue tracker](https://gitlab.com/gitlab-com/support/issues/)
with the **Title:** *"GitHost Boot Camp - your_name"*

Tackle stage 1 first and the last stage last, but the others can be completed in
any order you prefer.

```
**Goal of this checklist:** Set a clear path for GitHost training

### Stage 1: Become familiar with GitHost

- [ ] **Done with Stage 1**

1. [ ] Ping your manager on the issue to notify them you have started
1. [ ] Commit to this by notifying the current experts that they can start routing non-technical GitHost related questions to you
1. [ ] Read the [GitHost FAQs](https://about.gitlab.com/gitlab-hosted/)
1. [ ] Read the [introduction to GitHost](https://dev.gitlab.org/gitlab/GitHost/blob/master/doc/introduction.md)
1. [ ] Watch the [introduction to GitHost video](https://drive.google.com/a/gitlab.com/file/d/0B0zUJJYhL0-ycXlsT3VtdjJ3cW8/view?usp=drive_web)

1. [ ] Find answers to the following question
   1. [ ] What EE and CE services are available through GitHost?
   1. [ ] What services are not available through GitHost?
   1. [ ] What kind of migration services do we offer?
   1. [ ] What kind of support do we offer to GitHost users?
   1. [ ] Where can I find the source code to the GitHost application?
   1. [ ] How do I login to the Rails console of the GitHost server?  What is the command to do this from any directory on this server?
   1. [ ] How do I login to a customer's instance?  What are the full commands to do this? What is the scripted shortcut and how do I use it?

### Stage 2:

- [ ] **Done with Stage 2**

Remember to contribute to any documentation that needs updating

1. [ ] Read documentation for accessing instances, migration, changing regions, upgrading to EE from CE, and common problems. Paste the links here.
    1. [ ] __
    1. [ ] __
    1. [ ] __
    1. [ ] __
    1. [ ] __

1. [ ] Watch the [additional training video on GitHost](https://drive.google.com/a/gitlab.com/file/d/0B5OISI5eJZ-DbVpGaGpFUFFnYms/view?usp=sharing)
1. [ ] Ask an admin to create a test CE instance for you and give you the instance ID and IP address
1. [ ] Ask an admin to give you SSH access to the GitHost production server
1. [ ] Upgrade your CE GitHost instance to EE (someone can upgrade an instance from CE to EE on the instance itself, but GitHost 'metadata' would not be properly updated without SSH access)
1. [ ] Migrate to a test instance from your local or DO testing environment
1. [ ] Change the region for your test instance


### Stage 3: Tickets

- [ ] **Done with Stage 3**

1. [ ] Look for 10 old GitHost tickets and read through them to understand what the issue was and how it was addressed. Paste the links here.

   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __

1. [ ] Answer 10 tickets and paste the links here. Do this even if a ticket
seems too advanced for you to answer. Find the answers from an expert and relay
it to the customer.

  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __

### Stage 4: Shadow or Pair on customer requests

- [ ] **Done with Stage 4**

1. [ ] Do a migration to GitHost
1. [ ] Upgrade a CE instance to EE
1. [ ] Troubleshoot a stuck instance/runner


### Final Stage
- [ ] Ask Lee and Drew to look over this list.
- [ ] Send a MR to declare yourself a **GitHost Expert** on the team page
```
