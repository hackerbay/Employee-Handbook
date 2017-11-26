---
layout: markdown_page
title: 2FA Removal
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

##### Overview

Use this when a request to disable 2FA on GitLab.com is received. This policy is covered in the Support handbook [policy section](https://about.gitlab.com/handbook/support/#removal-of-2fa-a-name2faremovala). 

##### Notes: 

In future this guide may include 2FA recovery via SSH (user self-service) see <https://gitlab.com/gitlab-org/gitlab-shell/merge_requests/74>

______________

##### Workflow

1. Apply the **"Account::2FA Removal Verification - GitLab.com"** Macro
2. Mark the ticket as "Pending"

##### User responds with ID verification 

1. Ensure the provided photo includes the persons face and ID.

1. Ensure the provided ID is one of the following:
    + Driver's License
    + Passport
    + Military/Government ID
    + Permanent Resident Cards

1. Confirm the ID matches the users last and first name on the GitLab.com account.

1. Provided the ID matches, use the **Account::2FA Removal Verification - GitLab.com - Successful** Macro
2. Mark the ticket as "Solved"


##### User responds with repository verification 

1. Verify the file uploaded
    + File contains the provided text string.
    + File has been uploaded to a "Personal Repository"

2. Apply an "Internal Comment" with a link to the commit (if not already included)
3. Apply the ID matches, use the **Account::2FA Removal Verification - GitLab.com - Successful** Macro

##### Failed to verify provided ID or repository 

1. Apply the **Account::2FA Removal Verification - GitLab.com - Failed** Macro


##### User is unable to provide verification

If the user claims they're unable to provide identification we should review the matter internally (Support Team) and determine the best course of action. 

__________________

**Macros**

* [Account::2FA Removal Verification - GitLab.com](https://gitlab.zendesk.com/agent/admin/macros/103721068)
* [Account::2FA Removal Verification - GitLab.com - Failed](https://gitlab.zendesk.com/agent/admin/macros/103790308)
* [Account::2FA Removal Verification - GitLab.com - Successful](https://gitlab.zendesk.com/agent/admin/macros/103772548)
