---
layout: markdown_page
title: Checklist for becoming a GitLab Geo Expert
---

Create an issue with this checklist on the [support team issue tracker](https://gitlab.com/gitlab-com/support/issues/)
with the **Title:** *"Geo Bootcamp - your_name"*

Tackle stage 1 first and the last stage last, but the others can be completed in
any order you prefer.

```
**Goal of this checklist:** Set a clear path for Geo Expert training

### Stage 1: Commit and Become familiar with what Geo is

- [ ] **Done with Stage 1**

1. [ ] Ping your manager on the issue to notify them you have started
1. [ ] In your Slack Notification Settings, set **Geo** as a **Hilight Word**
1. [ ] Commit to this by notifying the current experts that they can start
routing non-technical Geo questions to you
1. [ ] GitLab University
   1. [ ] [GLU Deck on Geo](https://drive.google.com/open?id=1r9nXLxU9fuAJdEDTi0ZWg7JyU5Ng4hNJPY3jnQyaor8)
   1. [ ] [GLU Recording on Geo](https://drive.google.com/open?id=0BxSd33hPSs-jRGRLUkpuWHF2cjQ)
1. [ ] Read through all the [Geo Documentation](https://docs.gitlab.com/ee/gitlab-geo/README.html)

### Stage 2: Technical Setup

- [ ] **Done with Stage 2**

Remember to contribute to any documentation that needs updating

1. [ ] Standard installation following the [Setup Instructions](https://docs.gitlab.com/ee/gitlab-geo/README.html#setup-instructions)
to install Geo on two VM's
1. [ ] Set up a local repo to push to the primary and pull from the secondary
1. [ ] Destroy the primary and promote the secondary node to primary by following
the [GitLab Geo Disaster Recovery Instructions](https://gitlab.com/help/gitlab-geo/disaster-recovery.md)
   1. [ ] Connect a local repo to this new primary and make sure you can push and pull
1. [ ] Custom ports for SSH and HTTP
1. [ ] Set up custom certificates / [self signed](http://docs.gitlab.com/omnibus/common_installation_problems/README.html#using-self-signed-certificate-or-custom-certificate-authorities)
1. [ ] HTTP/HTTPS Test to make sure Geo is working after each step
   1. [ ] Start with HTTP on both servers and change to the following:
   1. [ ] Primary use HTTP, secondary HTTPS
   1. [ ] Primary use HTTPS, secondary HTTP
   1. [ ] HTTPS on both
   1. [ ] Back to HTTP
1. [ ] Upgrade and Downgrade
   1. [ ] Start with GitLab CE
   1. [ ] Upgrade to GitLab EE
   1. [ ] Configure Geo
   1. [ ] Disable Geo after a trial period
   1. [ ] Downgrade back to CE

### Stage 3: Tickets

- [ ] Contribute valuable responses on at least 5 Geo tickets. Even if a ticket seems
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

### Stage 4: Pair on Customer Calls

- [ ] **Done with Stage 4**

1. [ ] Sales calls with customers that have expressed interest in Geo, and will
be asking questions about it.
   1. [ ] call with ___
   1. [ ] call with ___
   1. [ ] call with ___
1. [ ] Installation calls where we help a client install Geo
   1. [ ] call with ___
   1. [ ] call with ___
   1. [ ] call with ___

### Stage 5: Quiz?

- [ ] Need link to Quiz here
- [ ] Quiz answers were checked by Gabriel, and he said you passed

### Final Stage

- [ ] Your Manager needs to check this box to acknowledge that you finished
- [ ] Send a MR to declare yourself a **Geo Expert** on the team page
```
