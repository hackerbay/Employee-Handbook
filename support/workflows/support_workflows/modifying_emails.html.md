---
layout: markdown_page
title: Modifying Emails
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

##### Overview

Use this when a user made a typo in their email address while signing up on GitLab.com and are unable to receive confirmation emails.


______________

##### Workflow

1. Make sure the account in question is a new account. This workflow does not apply to existing / in-use accounts.
1. If there is a typo in the email address, follow [Fix email address](#fix-email-address).
2. If the email address is correct, but the user is not receiving the confirmation email, follow [Check emails in mailgun](#check-emails-in-mailgun).

##### Fix email address

Email address for an account can be changed via the GitLab.com Users Admin area.

1. Go to [https://gitlab.com/admin/users](https://gitlab.com/admin/users) and search the account.
2. Click `Edit`.
3. Fix the email address to the correct one and save your changes.
4. Send a confirmation email to the user from [https://gitlab.com/users/confirmation/new](https://gitlab.com/users/confirmation/new).
5. Respond to the user.

##### Check emails in mailgun

1. Login into mailgun.com using `supportteam` credentials in Support vault.
2. Go to [https://mailgun.com/app/logs/mg.gitlab.com](https://mailgun.com/app/logs/mg.gitlab.com).
3. Search logs for the particular email address and see if email is being bounced or delayed.
    + If email is delayed, respond to the user and ask them to wait.
    + If email is bounced, remove the email from the suppressions list here: [https://mailgun.com/app/suppressions/mg.gitlab.com/bounces](https://mailgun.com/app/suppressions/mg.gitlab.com/bounces)

