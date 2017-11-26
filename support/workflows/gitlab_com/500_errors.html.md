---
layout: markdown_page
title: Diagnose Errors on GitLab.com
category: GitLab.com
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

##### Overview
This guide provides resources for the diagnosing of **50x** errors on GitLab.com. 
This is used when a user contacts support stating they're receiving an error on GitLab.com.


##### Notes:

Check on the **#alert** & **#infrastructure** Slack channels to ensure this isn't an outage or infrastructure issue. 
______________

##### Workflow

1. Obtain the full URL the user was visiting when the error occurred. 

1. **Search Kibana**
  1. Login to [https://log.gitlap.com/app/kibana](https://log.gitlap.com/app/kibana)
  1. Select the correct time filter (top right) - e.g 30 minutes, 24 hours
  1. Use the search field to narrow down the results. For example you can search the `gitlab-ee` project for any mention of `error` using the query `"gitlab-ee" AND "error"`
  1. It's recommended to apply a **Negative Filter** to the logs below, these generate a large amount of noise and may not be relevant to your search.
     1. `gitlab_error.log` `gitlab_access.log` 
  1. See the [Kibana guide](https://www.elastic.co/guide/en/kibana/current/discover.html) for more information.

1. **Search Sentry**
    1. Login to [https://sentry.gitlap.com/gitlab/gitlabcom/](https://sentry.gitlap.com/gitlab/gitlabcom/)
       1. Use the search field to specify a relevant value. For example the following search would look for any errors with the URL shown that are unresolved. `is:unresolved url:https://gitlab.com/gitlab-org/gitlab-ce/issues `
       2. You can also search by username example `user.username:MyUserName` (this is case-sensitive)  
       1. You can also select filtering values by clicking the "filter" button .
    1. See the [Sentry guide](https://docs.getsentry.com/hosted/learn/search/) for more information.

1. **Escalation** 
   1. Gather as much information. Make an internal note on the ticket including links to the logs found in Kibana or Sentry. 
   1. Search the [GitLab-CE](https://gitlab.com/gitlab-org/gitlab-ce) project for any related issue.
   1. Make a comment in the **#Support** slack channel with a link to the error or short description of the error.
   1. Confirm if the issue is known or unknown. [Issue is known](#issue-is-known) - [Issue is unknown](#issue-is-unknown)

1. **Response**
   1. **Issue is known**
     1. If the issue is known it should have a corresponding GitLab project issue. 
     1. Respond to the user with information about the cause of the issue, linking to the related GitLab project issues.
        
   1. **Issue is unknown**
     1. **Issues found in Sentry**
         1. Convert the issue to a GitLab project issue by using the "Create GitLab Issue" button on the issue page.
         1. Comment on the issue providing a link to the ZenDesk ticket.
         1. Respond to the user with a link to the GitLab project issue.
     1. **Issues found in Kibana**
         1. Get a ["short url"](https://www.elastic.co/guide/en/kibana/3.0/sharing-dashboards.html) to the Kibana logs.
         1. Create and label a new [GitLab-CE](https://gitlab.com/gitlab-org/gitlab-ce) issue.
         1. Comment on the issue providing a link to the ZenDesk ticket and the Kibana logs.
         1. Respond to the user with a link to the GitLab project issue.
