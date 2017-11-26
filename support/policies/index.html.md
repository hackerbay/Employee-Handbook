---
layout: markdown_page
title: Support Policies
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

### Removal of 2FA

[Two-factor Authentication](http://docs.gitlab.com/ee/profile/two_factor_authentication.html) (2FA)
can only be removed from a GitLab.com account if one of the following combinations are met:

#### Combination 1 (self-service):

Users can generate new recovery codes using SSH, if they've previously added
SSH public keys to their profile. The new recovery codes can then be used at
sign in. This option is presented to users in the Zendesk macro. If they cannot
use this method then move on to the manual methods below.

```
ssh git@gitlab.com 2fa_recovery_codes
```

#### Combination 2 (ID verification):

Photo ID and picture of user with ID

Examples:

+ Driver's License
+ Passport
+ Military/Government ID
+ Permanent Resident Cards


### Dormant Usernames

**Note: As of November 15, 2017, due to a high number of these requests GitLab is no
longer
processing dormant username requests.**

When we have a larger support team in place to process these requests in the
future we will offer this again.
Support often gets requests from gitlab.com users to release a username.
This can be implemented if the following criteria are met:

1. The account in question has no data.
1. There hasn't been any activity on the account (i.e. code, issues, merge requests)
   for six months. This considers activity on projects the account owns
   as well as activity on projects the account participants in.
1. Support has had two failed attempts to contact the user within a
 two week period.
1. The user cannot be an owner of any active project.

Usernames will be appended with `_idle` to keep the account active but
release the namespace.

Support agents will not release a current user's contact information to another
user. GitLab also will not contact a user on behalf of another user to request
surrender of an apparently active username.

### Code of Conduct

Just as Support Engineers are expected to adhere to the [Code of
Conduct](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#code-of-conduct), we
also expect customers to treat Support Engineers with the same level of respect.

If you receive threatening or hostile emails from a user, please create a
confidential issue in the [GitLab Support Issue Tracker](https://gitlab.com/gitlab-com/support/issues)
and include:

1. A history of the user's communication
1. Relevant links
1. Summary of the high-level issues

Include the Support Lead, VP of Engineering, and Chief Culture Officer in this issue. Together we will
evaluate on a case-by-case basis whether to take action (e.g. ban the user from the forums
for violating the Code of Conduct).
