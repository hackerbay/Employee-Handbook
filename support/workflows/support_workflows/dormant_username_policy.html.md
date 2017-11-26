---
layout: markdown_page
title: Dormant Username Policy
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

##### Overview
Apply this workflow when a customer has lodged a dormant a [dormant username](https://about.gitlab.com/handbook/support/#dormantusers) request.

##### Notes:
When applying any of the Macros ensure to replace the placeholder **“REQUESTEDUSERNAME”** with the username requested.
______________

##### Workflow

1. Search for the requested username in [GitLab.com admin](https://gitlab.com/admin/users), once found visit the users admin profile.
1. Apply the **“Account::Dormant Username::Internal Checklist”** Macro
1. Answer all questions in the **“Internal Checklist”** (Yes/No) ensuring to cross check the information found in the admin section. 
1. If all answers are **Yes** for the internal checklist follow: [Username is available](#username-is-available) 
1. if the username is not available follow: [Username is not available](#username-is-not-available)

##### Username is available 

1. Reply to the requester with the **Account::Dormant Username::First Response** Macro
1. Create a **new ZenDesk ticket** with the **username owner's email address (found in admin)**. 
1. Apply the **“Account::Dormant Username::Contact Username Owner”** Macro and mark the ticket as **Pending**. 
1. Make an internal comment providing a link to the ticket “requesting user's ticket”
1. Wait for **a response** or the ticket to be **automatically reopened** in a week.
1. Apply the **“Account::Dormant Username::Contact Username Owner”** Macro a second time and mark the ticket as **Pending**.
1. Wait for **a response** or the ticket to be **automatically reopened** in a week.


##### Username owner responded
If the username owners makes a response (don’t remove my username) follow these steps:

1. Apply the **“Account::Dormant Username::Cancel Request”** Macro to the **username owners response**.
1. Apply the **“Account::Dormant Username::Failed Username Request”** to the **username requesters ticket**. 


##### Username owner has not responded

If the contacted user makes no response (within a 2 week period) the ticket will be **automatically marked as open and an email sent to the assigned agent** 

If the username owners makes no response follow these steps:

1. Rename the username:
1. Navigate to the username in admin - https://gitlab.com/admin/users
1. Select “Edit” on the user's profile
1. Append “_idle” to the user’s username 
1. Save changes


1. Apply the **“Account::Dormant Username::Successful Username Request”** Macro to the **username requesters ticket** and mark the ticket as **Solved**. 
2. Mark the **username owners ticket** as **Solved**


##### Username is not available 

1. Apply **"Account::Dormant Username::Failed Username Request"** Macro and mark ticket as **Solved**


##### FAQs

1. Does a login in response to dormant request mean that the account is active? No, the user has to explicitly reply to the dormant request saying "I want to keep my username". If the user hasn't responded and has just logged in, send a final message saying something like, "I see you logged in at X, but you need to let us know here if you want to keep your username".
1. What constitutes data in the account? A group, a project, etc. means data. Even if the project or group is empty.


__________________

**Macros**

* [Account::Dormant Username::Failed Username Request](https://gitlab.zendesk.com/rules/94534768/edit)
* [Account::Dormant Username::Internal Checklist](https://gitlab.zendesk.com/rules/93505588/edit)
* [Account::Dormant Username::First Response](https://gitlab.zendesk.com/rules/94687707)
* [Account::Dormant Username::Contact Username Owner](https://gitlab.zendesk.com/rules/94531288/edit)
* [Account::Dormant Username::Cancel Request](https://gitlab.zendesk.com/rules/94534828/edit)

**Automations**

* [Dormant Username Check](https://gitlab.zendesk.com/rules/94693587/edit)
