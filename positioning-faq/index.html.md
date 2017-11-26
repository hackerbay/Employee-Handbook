---
layout: markdown_page
title: "GitLab Positioning FAQ"
---

## On this page
{:.no_toc}

- TOC
{:toc}

### What is GitLab?

1. GitLab is an open source tool used by developers to create and manage code bases collaboratively. Built on Git, which is a very popular and efficient distributed version control system, GitLab gives you all the tools needed for Git repository management from code reviews to issue tracking and more.
1. We have a few different versions of GitLab.
    - GitLab.com.  Hosted, open source for private repos. Just signup and get started.
    - GitLab CE.  On-premises, self-hosted GitLab with LDAP integration, issue tracker, webhooks, and integrated CI.
    - GitLab EE.  GitLab Enterprise Edition builds on top of the Community Edition and includes extra features mainly aimed at organizations with more than 100 users. It has LDAP group sync, audit logs and multiple roles. It includes deeper authentication and authorization integration, has fine-grained workflow management, has extra server management options and it integrates with your tool stack.
    - GitHost.io  Private, single-tenant GitLab instances hosted by us.
    - Know the comparison chart - https://about.gitlab.com/features/#compare

### I use GitHub.  What can GitLab offer me?

1. GitHub has done a lot for the Git space. Great company.
1. For the basics, we have some key differences: (no more)
    - Scales better with multiple application servers- Run GitLab in a cluster
    - Multiple authentication levels
    - Group level milestones
    - 4 times more cost effective
    - Community of 1,000 developers contributing to updates that are pushed on the 22nd of every month

### Our company uses GitHub.com for all open source projects, so why should we use GitLab Enterprise Edition on-premises and not GitHub Enterprise?

1. With GitLab Enterprise Edition you can use [Repository Mirroring](http://doc.gitlab.com/ee/workflow/repository_mirroring.html) to mirror your open source projects from GitHub.com to your on premises GitLab server. Alternatively, if you want to have a public mirror of your GitLab project, you can now do so effortlessly using mirroring. GitHub Enterprise does not have mirroring.
1. Open source projects have different needs than projects developed on-premises by organizations. GitLab was built specifically for use by organizations on-premises and so has more features specific to the enterprise such as 5 levels of [permissions](http://doc.gitlab.com/ee/permissions/permissions.html), and the ability to install on a variety of operating systems.
1. Unlike other Git management solutions which can have different project views etc, GitHub and GitLab are very similar in features and functionality as well as the workflow they support. Their URL’s and API’s are also similar, so developers will quickly become familiar with GitLab.
 
### GitLab is winning enterprise 

1. GitLab is focusing a considerable amount of energy on making Git the way large companies manage their code repositories. Our open-source community has created a powerful tool that we are excited to bring into the enterprise world.
1. GitLab enterprise key features:
    - Most installed on-premises Git solution - GitLab is used by over 100,000 organisations worldwide, on their own servers.
    - GitLab handles huge repositories well - Big repository? No problem. GitLab is built to handle very large repositories.
    - Access to the server - You have complete control of the server/instance, so you can install additional software (intrusion detection, performance monitoring, etc.) and view log files on the server itself.
    - Pricing - we are much more cost effective.

### I use Bitbucket.  What can GitLab offer me?

1. Bitbucket has done a lot for the enterprise Git space. Great company.
1. GitLab.com and Community Edition are completely free - Bitbucket.com is pay if you have more than 5 users.
1. Backed by a community of a few hundred thousand developers and 1,000 contributors.
1. We launch new features monthly and are iterating on our product faster than anyone in the market. Thanks to our community and our open-way of working, we’ve been able to release new features quickly and effectively.
    - Job’s blog post on the topic is a great read, https://about.gitlab.com/2015/04/15/bitbucket-vs-gitlab-com/

### I use or am looking at software tools like VersionOne and Rally; how does GitLab compare?

1. Both VersionOne and Rally are strong on the project management side and include road mapping, backlog management, and release management - especially when scaling to teams. GitLab provides strong collaboration across detailed issue management, task assignment, version control, repo management, code review, CI/CD, deploy and resource monitoring. For the enterprise, both tool sets fulfill an important role.
1. If you are working with a Conversational/Agile development style, GitLab EE Premium will solve your needs. GitLab is the next-generation development toolset that covers **100%** of your software development lifecyle in one unified experience. 
1. If you are going down a path to SAFe, VersionOne is a great option, there is also a native integration from VersionOne with GitLab for the code repo and CI/CD. 
    
### I use or am looking at GitSwarm from Perforce.  Do I need GitLab too?  Am I missing anything by not working directly with GitLab?

1. GitSwarm is built on GitLab CE or EE.
1. GitSwarm combines Perforce and GitLab to give developers a Git-based workflow they prefer while also providing an organization with enterprise-class scalability, security, and file management performance from Perforce.
1. We’re happy that Perforce chose GitLab to help their customers create, code, and deploy together. To learn more, have a look at the GitSwarm overview, https://www.perforce.com/gitswarm.
1. How should GitLab account executives engage prospects that are currently using or evaluating GitSwarm?
    - If the prospect is already using GitSwarm CE, the GitLab channel representative should work with the Perforce account executive to focus on the benefits of upgrading the customer to GitSwarm EE.
    - Perforce customers can pay via a perpetual license fee up-front with an annual Support and Maintenance fee or they can purchase via an annual subscription fee.
    - GitLab’s new LFS feature addresses the need to provide storage for large binary files, which is a need of many Perforce clients leveraging Git. This is a must-have feature for companies in the video, hardware, and gaming space.
    - GitLab has partnered with Perforce as a reseller.
    - GitLab channel managers should be proactive in identifying companies that are using Perforce Helix and work with Perforce account executives in developing a plan to move them to using GitSwarm EE (or at a minimum GitSwarm CE).
    - Many long-term Perforce customers are in the process of evaluating Git solutions for certain user segments within their organizations and this is good time to support Perforce in proactively building a relationship during the early evaluation stages.

### We’re already using GitLab CE for free. Why should we upgrade?

1. CE is a great option for smaller teams but larger organizations benefit from the features of GitLab EE.
1. GitLab Enterprise Edition builds on top of the Community Edition and includes extra features mainly aimed at organizations with more than 100 users.
1. It has LDAP group sync, audit logs and multiple roles.
1. It includes deeper authentication and authorization integration, has fine-grained workflow management, has extra server management options and it integrates with your tool stack.
1. More customizable and secure.
    
### Who are some of your customers?

1. Used by more than 100,000 organizations.
1. Large - Microsoft, IBM, AT&T, CERN
1. Small - SpaceX, Stack Overflow
    
### Why are you monetizing an open-source product?

1. Our community has worked hard on making a great product.
1. The enterprise world could benefit from this product.
1. We wanted to be able to offer some features that aren’t necessarily needed in the open source world but are needed for large companies.
1. For those features, we charge our large customers and in return are able to create those features and hire people to work on the open source project.
    
### I use the hosted version of GitLab. Why would my company need on-premises?

1. More secure and customizable.
1. LDAP integration
1. Paid support
1. 2FA
1. Permissions management
    
### How does support work?

1. For on-premises EE - https://about.gitlab.com/pricing/ - gitlab enterprise edition with paid support
1. For GitLab.com - Bronze support - monthly fee - https://gitlab.recurly.com/subscribe/gitlab-com-bronze-yearly-20
1. Active StackOverflow community for free users.

### Do you offer a solution for migrating data from GitHub, Bitbucket, SVN to GitLab?

1. Import from Bitbucket, GitHub, anywhere
1. Want to start using GitLab? You can easily import your repositories from Bitbucket, GitHub, Gitorious, or anywhere else, all in batch!
1. Migrating SVN to GitLab
    - http://doc.gitlab.com/ce/workflow/importing/migrating_from_svn.html
    - SVN stands for Subversion and is a version control system (VCS). Git is a distributed version control system.
        
### Why aren’t you using a GPL license?

1. Based on Ruby on Rails
1. MIT license is common for Ruby and RoR
