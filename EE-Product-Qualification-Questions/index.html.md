---
layout: markdown_page
title: "GitLab EE Product Qualification Questions"
---


We need have a library of questions we need to ask in the buying process to help identify and influence the decision process for EES and EEP. The purpose of these questions is to help us and more importantly the prospect recognize their problem and for us to present the right solution for them, which would be EES or EEP.

* Admin control with Pivotal Tile (EEP)
* Aduit Logs (EEP)
  - Do you have audit controls you have to adhere to? (problem question)
  - What kind of audit data does your security team need to be able to see? (implication question)
  - Are all of your projects required to be audited the same way? (implication question)
* Multiple LDAP server support (also compatible with Active Directory)
* Auditor Users (EEP)
* Canary Deployments (EEP)
* Dedicated High Availability support (EEP)
* Deploy Boards (EEP)
* Disaster Recovery (EEP)
* Geo (EEP)
  - Where are your developers located? (Implication question)
  - What are your DR requirements? (Problem question)
  - Does WAN speed cause your users' experience to suffer? (Problem question)
  - How large are your repositories? Do you have an idea on how long it takes to clone or fetch from them right now? (Problem)
  - How much time would it save your team if they were able to clone a large repository in seconds compared to the minutes it takes now? (Implication)
* Service Desk (EEP)
* File Locking (EEP)
  - Do you have or do you see your organization having multiple people working on the same file and you want to avoid merge conflicts? (Problem Question)
  - What problems do you and your organization run into when there are merge conflicts? (Implication Question)
  - Does your repository contain binary files? (Problem Question)
  - If yes, what challenges do you have when these binary files have merge conflicts and multiple people making changes? (Implication Question)
* Host static pages straight (with TLS and CNAME support) from GitLab using GitLab Pages
* Burndown charts
* Contribution Analytics, see detailed statistics of contributors
* Multiple LDAP server support (also compatible with Active Directory)
  - Does your organization have more than one domain name? eg: an acquired company
  - How do you manage access to shared resources across multiple business units with different domains?
  - Would you like to enable inner-sourcing for better innovation across the entire company including multiple domains?
* LDAP group synchronization (also compatible with Active Directory)
  - Can your GitLab Admins ensure that access to company IP is blocked as soon as an employee is terminated?
  - How much time does your GitLab Admin spend assigning permissions to newly hired developers?
  - When a new team is created for a new project, how much time does your GitLab Admin spend creating a GitLab group with the appropriate permissions?
  - How much time does your GitLab Admin spend cleaning  up user accounts to determine a more accurate active user count?
* Create and remove admins based on an LDAP group
* Kerberos user authentication
* Integrate with Atlassian Crowd
  - Does your organization currently use Atlassian Crowd?
  - If yes, how important is it to you to integrate Atlassian Crowd into GitLab?
* Share a project with other groups
  - How do currently share a project with other groups? (problem question)
  - Are there certain projects that other groups would find valuable having access to but you are unable to share that project with them or share easily with them?
* Rebase merge requests before merge
  - Do you prefer a linear history on a project?
  - Is developer productivity hampered by trying to comprehend a projects history?
  - How do you force developers to rebase their changes before merging to Master and how effective is it?
  - Do Project Leads waste time cleaning up a projects commit history?
* Use fast-forward merges when possible
* Push Rules (commit message must mention an issue, no tag deletion, etc.)
  - Do developers store large binaries  in your Git repositories?
  - How does that affect performance of clone times?
  - Do your repositories suffer from 'bloat'?
  - Does your workflow require commits to be tied to an applicable Issue or Bug ID?
  - How problematic is it when a developer deletes a tag with a push?
* Webhooks at Group Level
* Lock project membership to the members of a group
  - Do you currently have projects that only certain members of a group should have access to or you would like them to only have access to, instead of the entire group? (problem question)
  - How would being able to grant permission to a project to certain members of a group help you? (implication question)
* Approve Merge Requests
  - Is it important for you to keep the quality of your code high? (Problem Question)
  - How do you prevent Developers from being able to approve their own merge requests? (Problem Question)
  - How do you currently make sure that the right people approve code before it is applied to your most important branches? (Problem Question)
  - What happens if bad code makes it into your application and breaks it? (Implication Question)
* Mirror External Repositories
  - Do you need changes in a GitLab project to update a legacy system repo?
  - Do you want to keep abreast of changes to a repository located on a different system?
  - How do you currently manage changes to a single project across multiple systems?
  - Do you have repositories located on a different server that you still want to work with? (Problem Question)
  - How much more efficient would your team be if your external repositories were automatically updated every hour with the ability to view the activity feed showing any new changes? (Implication Question)
  - Is it important to your team to keep an already existing repository in addition to your new GitLab one? (Problem Question)
  - Is there a current company policy that you need to keep some of your legacy system in place with your current repositories? (Problem Question)
  - How much more efficient would your team be if they didn't have to spend time reconfiguring your existing integrations by having your external repository automatically updated? (Implication Question)
* Multiple assignees for issues
* Set weight of issues
  - How many open issues do you typically have at any given point in time? (Problem Question)
  - Is it hard to keep track of the amount of work involved with individual issues? (Problem Question)
  - Do you have to prioritize which issues to complete in order to meet release deadlines? (Problem Question)
  - What happens if you need to push out your release date into the future and you miss your initial deadline? (Implication Question)
* Issue board focus mode
* Squash and Merge
* Create templates for issues and merge requests
  - Is there specific information that needs to be included with each Issue and Merge Request? (Problem Question)
  - How often does extra time need to be spent clarifying the details or getting additional information for Issues or Merge Requests? (Implication Question)
* An admin can email all users of a project, a group or the entire server
* Omnibus package supports log forwarding
* Project importing from GitHub Enterprise to GitLab
  - Is it important for you to keep the projects and work you have set up in GHE? (problem question)
  - Would you like to have your team work on the projects you have in GHE inside the GitLab UI?
* Project importing from GitLab.com to your private GitLab instance
  - Is it important for you to keep the projects and work you have set up in GitLab.com? (problem question)
* Super-powered search using Elasticsearch
  - How large is your instance as far as repos, projects, etc?
  - Does your team every struggle finding specific areas of your code through search?
  - How often would you say your team searches through code, and how efficient is the process at the moment?
  - Would if be helpful if we could reduce the time it takes to search through all your data in your instance?
  - How much time would be saved if your team could find the information in seconds?
* Global Code Search
  - How do developers currently find code from different teams that might be useful for their project eg: a plugin?
  - How do you ensure developers don't reinvent the wheel?
  - Are you looking to enable innersourcing?
* Prevent committing secrets
  - Are you currently able to stop developers accidentally putting a secret such as login credentials into a repository?
  - What are the risks if they do?
* Branch Permissions for users
  - How do you currently manage branch permissions?
  - Are pushes and merges from certain users problematic?
  - Would you like the ability to restict push and merge access to certain users?
* Display merge request status for builds on Jenkins CI
* Omnibus package supports configuring an external MySQL database
* Import from GitLab.com 
* Email all users of a project, group, or entire server 
* Limit project size at a global, group, and project level
* Multiple Issue Boards
