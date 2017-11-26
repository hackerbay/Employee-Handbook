---
layout: markdown_page
title: Checklist for becoming a GitLab-LDAP Expert
---

Create an issue with this checklist on the [support team issue tracker](https://gitlab.com/gitlab-com/support/issues/)
with the **Title:** *"LDAP Boot Camp - your_name"*

**Goal of this checklist:** Set a clear path for LDAP Expert training

Remember to contribute to any documentation that needs updating
```
### Stage 1: Commit and Become familiar with what LDAP is

- [ ] **Done with Stage 1**

1. [ ] Ping your manager on the issue to notify them you have started
1. [ ] Commit to this by notifying the current experts that they can start
routing less-technical LDAP questions to you
1. [ ] GitLab University
   1. [ ] [What is LDAP-Overview](https://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol)
   1. [ ] [Training Video](https://drive.google.com/open?id=0B9T-nz-7uMATSUxGT3hDX3RKdTg)
   1. [ ] [GitLab LDAP](https://docs.gitlab.com/ce/university/#3-5-ldap-and-active-directory)
1. [ ] Read through all the [LDAP Documentation for CE](https://docs.gitlab.com/ce/administration/auth/ldap.html)
1. [ ] Read through all the [LDAP Documentation for EE](https://docs.gitlab.com/ee/administration/auth/ldap-ee.html) which covers EE specific portions.

### Stage 2: Technical Setup

- [ ] **Done with Stage 2**

1. Setup openLDAP server on your dev environment. This point is already covered in Support Bootcamp but for non Support members please follow the points below.

 * [ ] Install the [GDK](https://gitlab.com/gitlab-org/gitlab-development-kit)
 * [ ] Add [OpenLDAP](https://gitlab.com/gitlab-org/gitlab-development-kit/tree/master/gitlab-openldap) to your GDK installation.
 * [ ] Try Group sync in the GDK environment. If you don't succeed, contact an LDAP expert, then contribute to documentation on this.

 ### Stage 3: Tickets

- [ ] **Done with Stage 3**

1. [ ] Go through a few solved LDAP tickets to check the responses and get a sense of the types of frequently asked questions that come up.
1. [ ] Answer 20 LDAP tickets and paste the links here. Even if a ticket seems
too advanced for you to answer. Find the answers from an expert and relay it to
the customer.
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

### Stage 4: Pair on Customer Calls

- [ ] **Done with Stage 4**

1. [ ] Installation calls where we help a client who needs to integrate LDAP
   1. [ ] call with ___
  1. [ ] call with ___
1. [ ] Diagnosis calls, where something is wrong with LDAP for a customer
  1. [ ] call with ___
  1. [ ] call with ___

### Stage 5: Quiz?

- [ ] **Done with Stage 5**

### Final Stage

- [ ] Ask Lee and Drew to look over this list, send a MR to delete this line after they both satisfied with the list
- [ ] Send a MR to declare yourself a **LDAP Expert** on the team page

 ```
