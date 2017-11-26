---
layout: markdown_page
title: Issue Escalations
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

Escalating GitLab issues correctly is an important part of providing quick and accurate customer support. The support team uses the processes and escalation points described on this page when dealing with GitLab issues.

## Issue Prioritization

In general, the Product team  will prioritize all issues
(not just customer requests) as described elsewhere in the handbook, specifically for
[the product managers](/handbook/product/product-areas/#prioritization), and for [engineering](/handbook/engineering/workflow). From those pages, generally, it goes in order of:

1. Regressions
1. Bugs
1. Product Direction / Vision
1. New Feature Proposal

The Support Team plays a role in communicating the **impact to customers** of regressions, bugs, and feature
requests. By using issue templates and then using the appropriate labels on those issues, the team can
communicate _within the support team_ about which customer-affecting issues are high priority, and also show
this to the team at large. By then participating in the scheduling effort for each release, the Support Team
represents the voice of the customer in product development.

### General notes on making issues

#### Use templates

When reporting a bug/regression or feature proposal. For example, `gitlab-ce` project has 'Bug' and 'Feature Proposal'
templates.

#### Use labels

Always. Use either `~bug` or `~feature proposal` and
also add `~customer`. For certain premium subscribers, you may need to use
`~customer+`. If there are one or more component labels that are appropriate,
such as `~ldap`, add those, too. Add [Support Priority labels](#support-priority-labels) ( `~SP1`, `~SP2`, `~SP3`) to indicate perceived priority inside the Support Team.

#### Maintain confidentiality

If an image, log output, etc. is required for the issue, try to produce your own test image. If you are unable
to reproduce the issue and you wish to use the image provided by the customer make sure you _obtain
permission_ from the customer since the image may (inadvertently) include sensitive information like names,
group names, user names, or code.

#### Information gathering

For the *Application and environment information* section of issue templates, use:

+ Omnibus: `sudo gitlab-rake gitlab:check`
+ Source: `sudo -u git -H bundle exec rake gitlab:check RAILS_ENV=production SANITIZE=true`
________________________
+ Omnibus: `sudo gitlab-rake gitlab:env:info`
+ Source: `sudo -u git -H bundle exec rake gitlab:env:info RAILS_ENV=production`

### Regressions

We aim to fix [regressions](/handbook/glossary/#regression) in patch releases, when possible. However, not all regressions are created equal - we will work to patch the high-impact ones first.

For all regressions, add the `~regression` label and the milestone the regression was introduced in.
For high-impact regressions, also add `~"Next Patch Release"` and ping the relevant lead, along with any experts on the subject area.

### Bugs and Feature Proposals

By default, add an appropriate [support priority label](#support-priority-labels) to bugs and feature proposals. The labels are `~SP1`, `~SP2`, and `~SP3`, where `SP1` is the highest priority.
These labels are applied in addition to the `~bug`, `~feature proposal` and `~customer` labels. Use
priority labels in accordance with the urgency / impact matrix below.

The reasoning behind adding an `~SP` label to _every_ of these issues is that each issue _should_ have had
someone consider the urgency and impact, and this is best done at time of creating the issue since that is
when the information and context is "fresh" in your memory. It is OK to change the assessment and label at a
later date upon reflection (for example, during the support-internal scheduling meeting). When an issues are
allowed to be filed _without_  an `~SP` label it will be unclear whether an issue lacks the label due to lack
of urgency / impact, or due to missing a step in the process.

> **Note about feature proposals:** GitLab has limited development resources.
  Additionally, we must think about how widely applicable a feature may be to
  other users. Requests that are very specific to one company's workflow are
  likely to be rejected. Even if a feature seems widely applicable, we may
  leave the feature proposal dormant for some time and see if other users
  and customers chime in that they are also interested. Features that garner
  interest from multiple organizations will be considered more rapidly. Of
  course, there are always exceptions to these 'rules'. This note is meant to
  set the expectation that feature proposals may not be implemented quickly.

### Support Priority labels

Use the following as a guideline to determine which Support Priority label to use (if any) for bugs and feature proposals.

- **Urgency:** _For example: Does this break all GitLab functionally or just a small part?_
  - U1 - A large part, or a fundamental part
  - U2
  - U3 - Only a small part
- **Impact:** _For example: How many users does this impact?_
  - I1 - Many users
  - I2
  - I3 - Limited number of users

| **Urgency \ Impact**          | **I1 - High** | **I2 - Medium**  | **I3 - Low**   |
|-------------------------------|---------------|------------------|----------------|
| **U1 - High**                 | `SP1`         | `SP1`            | `SP2`          |
| **U2 - Medium**               | `SP1`         | `SP2`            | `SP3`          |
| **U3 - Low**                  | `SP2`         | `SP3`            | `SP3`          |

### Escalating from the Support Team to the Development Team

On the last Tuesday of each month, the Support Team reviews the `SP` labeled issues (especially `SP1` and
`SP2`), discusses priorities, and chooses the top few to present to the Product team
for potential deliverables in the next release.

After the support team prioritizes it, we ping the relevant product manager for the express purpose of
scheduling. Having the Product team comment in the issues directly follows our core value of being transparent and will help customers understand the
context around why / when their issues are being resolved, and it provides direct feedback from
customers to the Development and Product teams.

Working this way, it is possible that a customer reported issue is not picked up for a while (scheduling
first, then time to work on a fix, then schedule for release, etc.). However, the idea is that this is OK
because most truly urgent issues will in fact be regressions that don’t have this
scheduling problem. If a bug isn't a regression, that means it has existed for more than a month when the customer notes it, and thus we've gone at least a full month without someone reporting the issue as urgent.

**Note**
- Issues are not scheduled for a particular release unless Product adds them to a release milestone
*and* they are assigned to a developer. We aim to be realistic about scheduled deliverables and will
avoid scheduling issues that cannot be delivered in a given release.
- Safety valve: If something is "truly urgent", pinging leads in the issues when they are created is the best
way to go, so it can be made Next Patch Release. This will often be preceded by loud debate and concurrence on
chat.

## Functional escalation points

| Service/Product  | Escalation Types                 | Escalation Point                                        | Assignment      |
|------------------|--------------------------------|-----------------------------------------------------------|------------------
| GitLab CE        | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-ce/issues/new        |
| GitLab EE        | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-ee/issues/new        |
| GitHost.io       | Bug reports, Feature proposals | https://gitlab.com/gitlab-com/githost/issues/new          | Maintainer of GitHost.io
| Omnibus GitLab   | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/omnibus-gitlab/issues/new   | Omnibus GitLab specialist
| GitLab Runner    | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-runner/new  | GitLab CI specialist
| GitLab Workhorse | Bug reports, Feature proposals | https://gitlab.com/gitlab-org/gitlab-workhorse/issues/new | Maintainer of gitlab-workhorse


**See the [GitLab team page](https://about.gitlab.com/team/) for assignments**


## Operational escalation points


| Service/Product       | Escalation Type                                                                                  | Escalation Point                                         |  Assignment      |
|-----------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------|----------------------- |
| GitLab Infrastructure | Anything related to the **running of GitLab.com**, performance, something breaks                | https://gitlab.com/gitlab-com/infrastructure/issues/new | Production Lead/Senior Production Engineer
| GitLab Support        | Any and all questions in relation to providing customer service for GitLab users and customers. | https://gitlab.com/gitlab-com/support/issues/new        | Support Team Lead/Senior Support Engineer

**See the [GitLab team page](https://about.gitlab.com/team/) for assignments**

### Notes

#### GitHost.io

+ GitHost [project](https://dev.gitlab.org/gitlab/GitHost)
+ GitHost [service](http://githost.io)

#### Omnibus GitLab

+ Related to Omnibus GitLab packaging only.
+ GitLab [omnibus release packages](https://packages.gitlab.com/gitlab)

#### GitLab Runner

- Information on [GitLab Runner](https://gitlab.com/gitlab-org/gitlab-runner#features)
- [Runner documentation](http://docs.gitlab.com/ce/ci/runners/README.html)

#### GitLab Workhorse

- Information on [GitLab Workhorse](https://about.gitlab.com/2016/04/12/a-brief-history-of-gitlab-workhorse/)
- **Description**  *"Gitlab-workhorse is a smart reverse proxy for GitLab. It handles "large" HTTP requests such as file downloads, file uploads, Git push/pull and Git archive downloads."*

#### GitLab Infrastructure

- Reach the infra team on [Slack](https://gitlab.slack.com/archives/infrastructure)
- Old blog post on [infrastructure](https://about.gitlab.com/2016/04/29/look-into-gitlab-infrastructure/)

