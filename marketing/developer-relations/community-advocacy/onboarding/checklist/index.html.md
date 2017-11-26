---
layout: markdown_page
title: Community Advocate Bootcamp Checklist
---

## Bootcamp Checklist for Training of New Community Advocates
<a name="checklist"></a>

Your manager should create an issue with this checklist on the [support team issue tracker](https://gitlab.com/gitlab-com/support/issues/) for you as part of your onboarding.
This list looks strange in this handbook because it is formatted to be copy-pasted into an issue and then render properly there.

The topics are  generally ordered by priority in which they need to be tackled,
but feel free to work on later things in the list when you are waiting on something.

```
We need to keep iterating on this checklist so please submit MR's for any improvements
that you can think of. If an item does not start with a role or name of someone else, it's yours to do.

**Goal of this entire checklist:** Set a clear path for Community Advocacy training

### Stage 0: Complete general onboarding to have all necessary accounts and permissions

- [ ] **Done with Stage 0**

_Typically completed within first week_

1. [ ] General expectations: it is expected that you will _start_ to tackle Stages 0, 1, 2, and 3 as early as your first week, but you are not expected to complete all items for some number of weeks. We believe that you often learn best and fastest by diving into (relatively easy) tickets, and learning by doing. However, this has to be balanced with making time to learn some of the tougher topics. The expectation is therefore that you are sufficiently advanced in your onboarding by the end of your first week, that you can answer 2-5 "simple" tickets. Over the following weeks, your manager will set higher targets for the number and difficulty of tickets to be tackled, but you should always have about 2-3 hrs per day to spend on working through this bootcamp. Some days it will be less, some days it will be more, depending on ticket load and how deep "in the zone" you are in either the bootcamp or the tickets you are responding to; but an average of 2-3 hrs per day should allow you to complete everything through to the end of Stage 6 within about four weeks.
1. [ ] General Onboarding Checklist: this should have been created for you on [the peopleops issue tracker](https://gitlab.com/gitlab-com/peopleops/issues/) as an issue by PeopleOps when you were hired.
   1. [ ] Finish every item on that list starting with `New team member:` until you are waiting for someone to answer a question or do something before you can continue that list.
   1. [ ] Start with Stage 1 here, but also with the first steps in Stage 2 and Stage 3.
   1. [ ] Check back daily on what was blocking you on your General Onboarding Checklist until that list is completely done, then focus on this one.

### Stage 1: Become familiar with git and GitLab basics

- [ ] **Done with Stage 1**

_Typically started in first week, completed by end of second week_

If you are already comfortable with using Git and GitLab and you will be able to
retain a good amount of information by just reading and watching through, that is
okay. But if you see a topic that is completely new to you, stop the video and try
it out for yourself before continuing.

1. [ ] Just quickly check on your Zendesk account to make sure that is ready for you when you need it.
1. [ ] Add a [profile picture](https://support.zendesk.com/hc/en-us/articles/203690996-Updating-your-user-profile-and-password#topic_rgk_2z2_kh) to your Zendesk account
1. [ ] Let your manager know if for some reason you were not able to create an account on Zendesk.
1. [ ] Under your profile on Zendesk, it should read `Agent`. If it reads `Light Agent`, inform your manager.

Cover these topics on the [GitLab University](https://docs.gitlab.com/ce/university/):

1. [ ] Under the topic of Git
  1. [ ] [About Version Control](https://docs.google.com/presentation/d/16sX7hUrCZyOFbpvnrAFrg6tVO5_yT98IgdAqOmXwBho/edit#slide=id.gd69537a19_0_14)
  1. [ ] [Try Git](https://www.codeschool.com/account/courses/try-git)
1. [ ] Under the topic of GitLab Basics
  1. [ ] All the [GitLab Basics](http://docs.gitlab.com/ce/gitlab-basics/README.html) that you don't feel comfortable with. If you get stuck, see the linked videos under GLB in GitLab University
  1. [ ] [GitLab Flow](https://www.youtube.com/watch?v=UGotqAUACZA)
  1. [ ] Take a look at how the different GitLab versions [compare](https://about.gitlab.com/features/#compare)
1. [ ] Any of these that you don't feel comfortable with in the [user training](https://gitlab.com/gitlab-org/University/tree/master/training) we use for our customers.
  1. [ ] `env_setup.md`
  1. [ ] `feature_branching.md`
  1. [ ] `explore_gitlab.md`
  1. [ ] `stash.md`
  1. [ ] `git_log.md`
  1. [ ] For the rest of the topics in `user training`, just do a quick read over the file names so you start remembering where to find them.
1. [ ] Get familiar with the services GitLab offers
  1. [ ] The differences between [CE and EE](https://about.gitlab.com/pricing/)
  1. [ ] [GitHost](https://about.gitlab.com/gitlab-hosted/)

### Stage 2. Installation and Administration basics.

- [ ] **Done with Stage 2**

_Typically started in first week, completed by end of third week_

**Goals**

- Get your development machine set up.
- Familiarize yourself with the codebase
- Be prepared to reproduce issues that our users encounter.
- Be comfortable with the different installation options of GitLab
  and configure LDAP.
- Have an installation available for reproducing customer bug reports.

1. [ ] Check back on your Zendesk account if you are not yet an `Agent`.
1. [ ] Manager: Add team member to to the `GitLab Support` Google Calendar.

**Set up your development machine**

1. [ ] Install the [GDK](https://gitlab.com/gitlab-org/gitlab-development-kit)
1. [ ] Add [OpenLDAP](https://gitlab.com/gitlab-org/gitlab-development-kit/blob/master/doc/howto/ldap.md) to your GDK installation.

**Installations**

You will keep one installation continually updated on Digital Ocean, just like many of our clients. But you need to choose where you would like to test other installations. TODO: We need to list some benefits of each choice here.

1. [ ] Choose your preferred test environment between Local VM's or Digital Ocean and put it in a comment below.

Installation from source is not common but will give you a greater understanding of the components that we employ and how everything fits together.

1. [ ] Perform each of the following [Installation Methods](https://about.gitlab.com/installation/) on your preferred test environment you chose above:
  1. [ ] Install via [Omnibus](https://gitlab.com/gitlab-org/omnibus-gitlab/)
  1. [ ] Populate with some test data: User account, Project, Issue
  1. [ ] Backup using our [Backup rake task](http://docs.gitlab.com/ce/raketasks/backup_restore.html#create-a-backup-of-the-gitlab-system)
  1. [ ] Install via [Docker](https://gitlab.com/gitlab-org/gitlab-ce/tree/master/docker)
  1. [ ] Restore backup to your Docker VM using our [Restore rake task](http://docs.gitlab.com/ce/raketasks/backup_restore.html#restore-a-previously-created-backup)
  1. [ ] Version 7 from [Source](https://gitlab.com/gitlab-org/gitlab-ce/blob/7-14-stable/doc/install/installation.md)
1. [ ] As a part of your general onboarding checklist, you should have asked for a Digital Ocean droplet to be created for you, where you can install and maintain your own instance of GitLab
  1. [ ] Install via [Omnibus](https://gitlab.com/gitlab-org/omnibus-gitlab/)
  1. [ ] Populate with some test data
    1. [ ] Populated Repos
    1. [ ] Users
    1. [ ] Groups
    1. [ ] Projects
    1. [ ] You can check this box but this one never stops as long as you are a Support Engineer for GitLab. Keep this installation up-to-date as patch and version releases become available, just like our customers would.
1. [ ] Ask as many questions as you can think of on the `#support` chat channel

### Stage 3. Customer Interaction through Zendesk

- [ ] **Done with Stage 3**

_Typically started in first week, and completed by the end of the fourth week_

**Goals**

- Have a good understanding of ticket flow through Zendesk and how to interact with our various channels
- See some common issues that our customers are facing and how to resolve them.

**Initial Zendesk training**

1. [ ] Complete Zendesk Agent training (allow 40 minutes for completion)
  1. Navigate to [Zendesk university](https://university.zendesk.com/#/purchase/category/34942) and order the **"Agents: Zendesk Fundamentals Online"** course
     1. Add the **"Agents: Zendesk Fundamentals Online"** course to your cart and click "Proceed to Checkout"
     1. Follow the prompts and finalize your order.
     1. You'll receive an email with information on accessing the Zendesk course
  1. Proceed to complete the **"Agents: Zendesk Fundamentals Online"** course
1. [ ] Review additional Zendesk resources
  1. [ ] [UI Overview](https://support.zendesk.com/hc/en-us/articles/203661806-Introduction-to-the-Zendesk-agent-interface)
  1. [ ] [Updating Tickets](https://support.zendesk.com/hc/en-us/articles/212530318-Updating-and-solving-tickets)
  1. [ ] [Working w/ Tickets](https://support.zendesk.com/hc/en-us/articles/203690856-Working-with-tickets) *Read: avoiding agent collision.*

**Learn about the Support process**

Zendesk is our Support Centre and our main communication line with our customers. We communicate with customers through several other channels too, see the support handbook for the full list.

1. [ ] Ask different people in your team if they would be willing to do a 45 minute screen share with you as they answer tickets on Zendesk, thinking out loud as much as they can and answering your questions. Continue with the rest of the list while you wait for these to get scheduled.
  1. [ ] call with ___
  1. [ ] call with ___
  1. [ ] call with ___
1. [ ] Dive into our ZenDesk support process by reading how to [handle tickets](https://about.gitlab.com/handbook/support/marketing/developer-relations/community-advocacy/#zendesk-workflow)
1. [ ] Start getting real world experience by handling real tickets, all the while gaining further experience with the Product.
   1. [ ] First, learn about our [Support Channels](https://about.gitlab.com/handbook/support/channels), and be aware which ones are handled by the [Community Advocacy team](https://about.gitlab.com/handbook/marketing/developer-relations/community-advocacy)
    1. [ ] Start with [StackOverflow](https://about.gitlab.com/handbook/marketing/developer-relations/community-advocacy/#stack-overflow) and the [GitLab forum](https://about.gitlab.com/handbook/marketing/developer-relations/community-advocacy/#forum).
      1. Here you will find a large variety of queries mainly from our Users who are self hosting GitLab CE
      1. [ ] Answer one by understanding a question dig in to try to find a solution
  1. [ ] [Proceed on to the GitLab.com Support Tracker](https://about.gitlab.com/handbook/support/channels/#gitlabcom-support-tracker)
     1. Here you will find queries regarding our own GitLab.com
     1. [ ] Find a user you can help and help them, this will give you an understanding of issues that users run into
1. [ ] Check out your colleagues' responses
   1. [ ] Read through about 20 old tickets that your colleagues have worked on and their responses
1. [ ] Take a look at the [GitLab.com Team page](https://about.gitlab.com/team/) to find the resident experts in their fields

**Learn about raising issues and fielding feature proposals**

1. [ ] Understand what's in the pipeline and proposed features at GitLab: [Direction Page](https://about.gitlab.com/direction/)
1. [ ] Practice searching issues and filtering using [labels](https://gitlab.com/gitlab-org/gitlab-ce/labels) to find existing feature proposals and bugs
1. [ ] If raising a new issue always provide a relevant label and a link to the relevant ticket in Zendesk
1. [ ] Add [customer labels](https://gitlab.com/gitlab-org/gitlab-ce/issues?label_name%5B%5D=customer) for those issues relevant to our subscribers
1. [ ] Take a look at the [existing issue templates](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#issue-tracker) to see what is expected
1. [ ] Raise issues for bugs in a manner that would make the issue easily reproducible. A Developer or a contributor may work on your issue.
1. [ ] Schedule a 45 minute call with your trainer where you share your screen
with them while you answer tickets on Zendesk, they give you feedback and answer
your questions. The goal with this call is for your trainer to pass on tactical
knowledge about the ticket handling process. Repeat this step a few times if that seems useful.

### Congratulations. You now have your Zendesk Wings!

### From now on you can spend most of your work time answering tickets on Zendesk, try to set aside 2 hours per day to make it through **Stage 4-6** of this list. Never hesitate to ask as many questions as you can think of on the `#devrel` chat channel

### Stage 4. The art of community

- [ ] Order, expense, and read the Art of Community by Jono Bacon ([Amazon Link](https://www.amazon.com/Art-Community-Building-New-Participation/dp/1449312063))

### Stage 5. Gathering Diagnostics

- [ ] **Done with Stage 4**

_Typically do this around the third week._

**Goal** Understand the gathering of diagnostics for GitLab instances

1. [ ] Learn about the GitLab checks that are available
    1. [ ] [Environment Information and maintenance checks](http://docs.gitlab.com/ce/raketasks/maintenance.html)
    1. [ ] [GitLab check](http://docs.gitlab.com/ce/raketasks/check.html)
    1. [ ] Omnibus commands
        1. [ ] [Status](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/maintenance/README.md#get-service-status)
        1. [ ] [Starting and stopping services](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/maintenance/README.md#starting-and-stopping)
        1. [ ] [Starting a rails console](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/maintenance/README.md#invoking-rake-tasks)
1. [ ] Ping the Support Lead to provide you admin access to GitLab.com, so that you can resolve user issues there. Create an admin user account for this purpose.

### Stage 6. Optional Advanced GitLab Topics

Discuss with your training manager if you should stop here and close your issue
or continue. Also discuss which of the advanced topics should be followed. Do
not just do all of them as they might not be relevant to what customers need
right now and can be a significant time investment.

These are some of GitLab's more advanced features. You can make use of
GitLab.com to understand the features from an end-user perspective and then use
your own instance to understand setup and configuration of the feature from an
Administrative perspective

- [ ] Set up and try [Git LFS](https://docs.gitlab.com/ee/workflow/lfs/manage_large_binaries_with_git_lfs.html)
- [ ] Get to know the [GitLab API](https://docs.gitlab.com/ee/api/README.html), its capabilities and shortcomings
- [ ] Learn how to [migrate from SVN to Git](https://docs.gitlab.com/ee/workflow/importing/migrating_from_svn.html)
- [ ] Set up [GitLab CI](https://docs.gitlab.com/ee/ci/quick_start/README.html)
- [ ] Create your first [GitLab Page](https://docs.gitlab.com/ee/pages/administration.html)
- [ ] Get familiar with the GitLab source code by finding the differences
between the [EE codebase](https://gitlab.com/gitlab-org/gitlab-ee) and the [CE codebase](https://gitlab.com/gitlab-org/gitlab-ce)
```
