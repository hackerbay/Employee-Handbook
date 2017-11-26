---
layout: markdown_page
title: "Customer Use-Cases"
---
1. Using JIRA with GitLab EE
    * A company in the healthcare space had been using EE for about a year now,
    and the number one reason they decided they could make the move to GitLab EE
    was because it works well with JIRA. They had been using JIRA for years, so
    any interruption to this workflow would not be easy for them. Because GitLab
    works well with JIRA, they were able to move over quickly and found features
    like referencing JIRA issues in GitLab merge requests, issues, and commits,
    as well as the ability to close JIRA issues with GitLab commits to be easy
    for them.
    * Placeholder to add another story
1. Using Jenkins with GitLab EE, then trying GitLab Integrated CI
    * Like the case above, another company had been using Jenkins as their CI
    tool for a long time. As they were evaluating GitLab and found we had a
    Jenkins CI integration, this allowed them to make the move to GitLab EE
    without disrupting what their team was already use to. Being able to 
    display merge request status for builds on Jenkins CI within GitLab was the
    number one reason they decided to make the move to EE. They also became 
    aware of GitLab's recently implemented Integrated CI, which their users have 
    started to test and are finding it may be a solution that ends up working 
    better for them.
    * Placeholder to add another story
1. Moving from CE to EE
    * A long time CE user decided to move their company to EE as they grew from 
    10 users to 120 in 2 years. Their needs changed, so features like LDAP 
    Group Sync that allowed the Admin. to manage group's and their permission 
    levels easier, were essential. Another key feature in EE that they now 
    needed was Git Hooks. They wanted to prevent git tag removal from their 
    users, so implementing a Git Hook allowed them to now do this. On top of 
    these features, they were happy to discover how easy it was to upgrade to EE
    from CE simply by using the Omnibus package.
    * Placeholder to add another story
1. Using High Availability with GitLab
    * A current Standard Subscriber decided they wanted to move from having a 
    single instance on GitLab EE, to having an HA setup. GitLab offered them 
    multiple HA solutions, and after speaking with our Support Engineer's, they
    decided that using two machines with one being a single slave server was 
    their best option. What was important to them was each machine had all of
    their GitLab repositories, configuration, and the database. With the slave
    server being a copy of the master, they used DRBD to ensure their data from
    the master is being replicated to the slave server in a timely manner. This
    of course made everyone feel better :)
    * Placeholder to add another story
1. Access to your server and security 
    * A customer in the banking industry had security as their number one 
    concern. An on-premises solution like GitLab EE is exactly what they needed
    as it allowed them to have access to their own server, view log files, and 
    they could also install additional software like intrusion detection. Since
    GitLab EE also comes with Audit Events, they could have a history and view 
    changes made within the GitLab server which was of extreme importance to 
    them.
    * Placeholder to add another story
1. Importing repos and files from GitHub
    * Placeholder to add story
    * Placeholder to add another story
1. Migrating from SVN to Git
    * Placeholder to add story
    * Placeholder to add another story
1. Protected Branches
    * The customer had been using Bitbucket and was not able to limit developer 
      permissions to specific branches and repositories.  They had an ongoing 
      problem with developers accidentally pushing branches to the wrong project 
      or without proper code review. They decided to switch to GitLab because 
      we offer protected branches with more of a fine grained level of 
      permissions at the Master level. 
    * Placeholder to add another story 
