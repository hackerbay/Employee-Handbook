---
layout: markdown_page
title: "Engineering Workflow"
---

This document explains the workflow for anyone working with issues in GitLab Inc.
For the workflow that applies to everyone please see [PROCESS.md](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md).

## On this page
{:.no_toc}

- TOC
{:toc}


## GitLab Flow

Products at GitLab are built using the [GitLab Flow](http://doc.gitlab.com/ee/workflow/gitlab_flow.html).

## Broken master

If you notice that the tests for the `master` branch of GitLab CE or EE are
failing (red) or broken (green as a false positive), fixing this takes priority
over everything else development related, since everything we do while tests are
broken may break existing functionality, or introduce new bugs and security
issues.

Create an issue, post about it in `#development` so that other developers are
aware of the problem and can help. If the problem cannot be fixed by you within
a few hours, `@mention` the relevant Engineering Leads and CTO in the issue and
on Slack, so that resources can be assigned to fix it as quickly as possible.

## Security issues

If you find or are alerted of a security issue, major or small, fixing this
takes priority over everything else development related.

Create a **confidential issue** mentioning the Security and the relevant
Engineering Leads, as well as the VP of Engineering, and post about it in
`#security`.

You should always use dev.gitlab.org for security work. Never push code related
to a security issue to GitLab.com, and don't submit MRs for security issues on
GitLab.com. For more, see the documentation on
[security releases](https://gitlab.com/gitlab-org/release-tools/blob/master/doc/security.md).

## Basics

1. Start working on an issue you’re assigned to. If you’re not assigned to any issue, find the issue with the highest priority you can work on, by relevant label. [You can use this query, which sorts by priority for the started milestones][priority-issues], and filter by the label for your team.
1. If you need to schedule something or prioritize it, apply the appropriate
  labels (see [Scheduling issues](#scheduling-issues)).
1. If you are working on an issue that touches on areas outside of your expertise, be
  sure to mention someone in the other group(s) as you soon as you start working on it.
  This allows others to give you early feedback, which should save you time in the
  long run.
1. You are responsible for the issue that you're assigned to. This means it has
  to ship with the milestone it's associated with. If you are not able to do
  this, you have to communicate it early to your manager. In teams, the team is
  responsible for this (see [Working in Teams](#working-in-teams)).
1. You (and your team, if applicable) are responsible for:
  - ensuring that your changes [apply cleanly to GitLab Enterprise Edition][ce-ee-docs].
  - the testing of a new feature or fix, especially right after it has been
    merged and packaged.
1. Once a release candidate has been deployed to the staging environment, please
  verify that your changes work as intended. We have seen issues where bugs did
  not appear in development but showed in production (e.g. due to CE-EE merge
  issues).

For general guidelines about issues and merge requests, be sure to read the
[GitLab Workflow][gitlab-workflow].

[priority-issues]: https://gitlab.com/groups/gitlab-org/issues?scope=all&sort=priority&state=opened&milestone_title=%23started&assignee_id=0
[ce-ee-docs]: https://docs.gitlab.com/ee/development/limit_ee_conflicts.html
[gitlab-workflow]: /handbook/communication/#gitlab-workflow

## Working in Teams

For larger issues or issues that contain many different moving parts,
you'll be likely working in a team. This team will typically consist of a
[backend developer](https://about.gitlab.com/jobs/developer/), a
[frontend developer](https://about.gitlab.com/jobs/frontend-engineer/), a
[UX designer](https://about.gitlab.com/jobs/ux-designer/) and a
[product manager](https://about.gitlab.com/jobs/product-manager/).

1. Teams have a shared responsibility to ship the issue in the planned release.
    1. If the team suspects that they might not be able to ship something in
  time, the team should escalate / inform others as soon as possible.
  A good start is informing your lead.
    1. It's generally preferable to ship a smaller iteration of an issue,
  than ship something a release later.
1. Consider starting a Slack channel for a new team,
but remember to write all relevant information in the related issue(s).
You don't want to have to read up on two threads, rather than only one, and
Slack channels are not open to the greater GitLab community.

## Choosing something to work on

Start working on things with the highest priority in the current milestone. The
priority of items are defined under labels in the repository, but you are able
to sort by priority.

After sorting by priority, choose something that you’re able to tackle and falls
under your responsibility. That means that if you’re a frontend developer,
you work on something with the label `frontend`.

To filter very precisely, you could filter all issues for:

- Milestone: Started
- Assignee: Unassigned
- Label: Your label of choice. For instance `CI/CD`, `Discussion`, `Edge`, `frontend`, or `Platform`
- Sort by priority

[Use this link to quickly set the above parameters][priority-issues]. You'll
still need to filter by the label for your own team.

If you’re in doubt about what to work on, ask your lead. They will be able to tell you.

## Triaging and reviewing code from the rest of the community

It's every [developers' responsibilities] to triage and review code contributed
by the rest of the community, and work with them to get it ready for production.

Merge requests from the rest of the community should be labeled with the
`Community Contribution` label.

This should be to be part of your daily routine. For instance, every morning you
could triage new merge requests from the rest of the community that are not yet
labeled `Community Contribution` and either review them or ask a relevant person
to review it.

Make sure to follow our
[Code Review Guidelines](https://docs.gitlab.com/ce/development/code_review.html).

[developers' responsibilities]: /jobs/developer/#responsibilities

## Workflow labels

Labels are described in our [Contribution guide][contrib-labels-guide].

[contrib-labels-guide]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#workflow-labels

## Working with GitLab.com

GitLab.com is a very large instance of GitLab Enterprise Edition.
It runs release candidates for new releases, and sees a lot of issues because of the amount of traffic it gets.
There are several internal tools available for developers at GitLab to get data about what's happening in the production system:

### Performance data

There is extensive [monitoring](https://monitor.gitlab.net/) publicly available
for GitLab.com. For more on this and related tools, see the [monitoring
 handbook](/handbook/engineering/monitoring).

More details on [GitLab Profiler](http://redash.gitlab.com/dashboard/gitlab-profiler-statistics)
are also found in the [monitoring performance handbook](/handbook/engineering/monitoring).

### Error reporting

- [Sentry](https://sentry.gitlap.com/) is our error reporting tool
- [log.gitlap.com](https://log.gitlap.com/) has production logs
- [prometheus.gitlab.com](https://prometheus.gitlab.com/alerts) has alerts for
  the [production team](/handbook/infrastructure/#production-team)

### Feature flags

If you've built feature flags into your code, be sure to read about
[how to use the feature flag to test a feature on GitLab.com](/handbook/infrastructure/#feature-flags).

## Scheduling issues

GitLab Inc has to be selective in working on particular issues.
We have a limited capacity to work on new things. Therefore, we have to
schedule issues carefully.

Product Managers are responsible for scheduling all issues
in their respective [product areas](/handbook/product/#who-to-talk-to-for-what),
including features, bugs, and tech debt. Product managers alone determine the [prioritization](https://about.gitlab.com/handbook/product/#prioritization).
The UX Lead and Engineering Leads are responsible for allocating people making sure things are done on time. Product Managers are _not_ responsible for these activities, they are not project managers.

Direction issues are the big, prioritized new features for each release.
They are limited to a small number per release so that we have plenty of
capacity to work on other important issues, bug fixes, etc.

If you want to schedule an `Accepting Merge Requests` issue, please remove
the label first.

Any scheduled issue should have a team label assigned, and at least one type label.

### Requesting something to be scheduled

To request scheduling an issue, ask the [responsible product manager](/handbook/product/#who-to-talk-to-for-what)

We have many more requests for great features than we have capacity to work on.
There is a good chance we’ll not be able to work on something.
Make sure the appropriate labels (such as `customer`) are applied so every issue is given the priority it deserves.

### Process improvement

There is an informal scheduling process discussion in the #scheduling Slack channel.
Anyone can join and suggest improvements to our scheduling process.

## Product development timeline

Teams (Product, UX, Engineering) continually work on issues according to their respective
workflows. There is no specified process whereby a particular resource should be working
on a set of issues in a given time period. However, there are specific deadlines that
should inform team workflows and prioritization. Suppose we are talking about milestone `m`
that will be shipped in month `M` (on the 22nd). We have the following deadlines:

- By month `M-1, 4th`: Release scope is established.  In-scope issues marked with milestone `m`.
- By month `M-1, 7th`: `m` issues are updated with docs starter blurb. Release post (WIP merge request) created with `m` issues and docs starter blurbs.
- On month `M-1, 8th` (or next business day): Kickoff call with WIP release post.
- By month `M, 7th`: Completed `m` issues with docs have been merged into master. Unstarted or unfinished `m` issues are de-scoped from `m`, with `m` being removed from them.
- On month `M, 22nd`: Release shipped to production. Release post published.

Refer to [release post due dates](/handbook/marketing/blog/release-posts/#due-dates)
for additional deadlines.

Note that release timelines are overlapping. For example, when a release is shipped
to production on the 22nd, the scope for the following release has already been established
earlier in that same month.

An in-scope issue already has a docs starter blurb (written by the PM) by the time
engineers start development. Engineers should create and merge in the updated docs
as part of completing an issue by the 7th. PMs revise the starter docs blurbs in the
release post appropriately before the release post is published.

Refer to [Feature freeze on the 7th for the release on the 22nd](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md#feature-freeze-on-the-7th-for-the-release-on-the-22nd)
for further timeline details of code releases, including major/minor version releases, as well as patch releases.

## Updating issues throughout development

Team members use labels to track issues throughout development. This gives visibility to
other developers, product managers, and designers, so that they can adjust their plans
during a monthly iteration. An issue should follow these stages:

- `In dev`: A developer indicates they are developing an issue by applying the `In dev` label.
- `In review`: A developer indicates the issue is in code review and UX review by removing the `In dev` label, and applying the `In review` label.


## Kickoff

At the beginning of each release, we have a kickoff meeting, publicly livestreamed to YouTube.
In the call, the Product Development team (PMs, UX designers, and Engineers) communicate with
the rest of the organization which issues are in scope for the upcoming release.
The call is structured by [product area](../../product/index.html.md#who-to-talk-to-for-what)
with each PM leading their part of the call.

The notes are available in a publicly-accessible [Google doc](https://docs.google.com/document/d/1ElPkZ90A8ey_iOkTvUs_ByMlwKK6NAB2VOK5835wYK0/edit?usp=sharing).
Refer to the doc for details on viewing the livestream.

## Retrospective

After each release, we have a retrospective meeting, publicly livestreamed to YouTube.
We discuss what went well, what went wrong, and what we can improve for the next release.

The notes are available in a publicly-accessible [Google doc](https://docs.google.com/document/d/1nEkM_7Dj4bT21GJy0Ut3By76FZqCfLBmFQNVThmW2TY/edit?usp=sharing).
Refer to the doc for details on viewing the livestream.
