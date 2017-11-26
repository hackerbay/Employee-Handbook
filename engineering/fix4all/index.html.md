---
layout: markdown_page
title: "fix4all: Developer Rotation on the Support Team"
---

## Background

The support team fields a wide array of questions from customers, and
we as the company learn quite a lot about ways to improve GitLab just
by helping our customers. In addition, sometimes customer-reported
bugs get addressed in a timely manner, but other times they remain
unfixed for quite some time.

## Introducing fix4all

fix4all is a rotation where one developer--or anyone in GitLab--will
spend a week of his/her time helping the support team. There are
several goals:

1. Reduce the time it takes to resolve customer tickets.
1. Reduce the time to fix customer bugs.
1. Increase the shared knowledge between developers and Support Engineers.
1. Increase customer awareness within the development team.
1. Foster better cooperation between members of different groups.

## Implementation

At the release kickoff, we will assign four developers to
be on the fix4all rotation. Each participant will be assigned a week
within that month to focus on helping support.

Follow your normal working hours when assigned to fix4all. You may have other
commitments to fulfil; that's fine, but if you can't dedicate at least half
your time to fix4all, discuss this with the Support Lead in advance.

### Tasks

Each developer will be assigned a week where they work directly with
the support team. The exact day-to-day tasks may vary depending on the
most pressing needs at the moment. Review the following resources before
starting your fix4all rotation:

+ [Zendesk Overview](https://support.zendesk.com/entries/21981122)
+ [Support Handbook](https://about.gitlab.com/handbook/support/)
+ [Support Turbo Overview](https://about.gitlab.com/handbook/support/#support-turbo)

When your fix4all week begins, join the #support channel and introduce
yourself! You may also wish to join #support-live-feed to monitor tickets
as they come in.

In general, you should follow these priorities:

* Help Support Engineers who need someone to jump on a call with them.
* Help Support Engineers to answer customer tickets they're handling.
* Respond to Zendesk tickets.
* Work on bugs labeled `customer+` or `customer`.

### Helping Support Engineers

If a Support Engineer needs someone to join a call with them, or has
questions about a ticket they're handling, and you're available, then
you are their first resource!

Take an optimistic view of your own expertise and be willing to research
a topic if necessary, but if the question is too far outside of your
expertise, let them know and help them to get the right people involved.

### Responding to ZenDesk tickets

If there are a large number of unanswered tickets, or some are close to
breaching, you should answer some tickets! The
[Support Handbook](https://about.gitlab.com/handbook/support/) is the
canonical reference, but here's a quick-start guide:

* Sign into ZenDesk using the 'Generic GitLab ZenDesk Agent' credentials in
  1password.
* Don't assign tickets to the generic agent, as they may get lost.
* Look for Tier 1 and Tier 2 tickets that aren't currently being worked on
  (ZenDesk will show you if other people are currently looking at a ticket).
* Keep GitLab's
  [user communication guidelines](https://about.gitlab.com/handbook/communication/#user-communication-guidelines)
  in mind at all times.
* When replying, set the ticket status to 'Pending' (awaiting response from
  customer) or 'Solved' (no reply expected).
* If appropriate, open new issues for the customer or add the `customer` or
  `customer+`. Perhaps you or a future fix4all engineer will work on it!
* Consider whether the ticket could have been avoided with
  documentation fixes. Open an MR with those changes if so.
* If you want to follow up tickets, you can add your personal GitLab email
  address to the `CC` list (do not use the `cc me` button).

### Bugs

If the Support team doesn't need help with tickets, you should aim to fix
bugs labeled `customer` or `customer+` in GitLab CE or EE, starting with the
highest-priority items:

* GitLab CE
  [customer](https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=customer&sort=priority),
  [customer+](https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=customer%2B&sort=priority)
  issues.
* GitLab EE
  [customer](https://gitlab.com/gitlab-org/gitlab-ee/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=customer&sort=priority),
  [customer+](https://gitlab.com/gitlab-org/gitlab-ee/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=customer%2B&sort=priority)
  issues.

Aim to complete issues you started work on during a fix4all rotation, even if
that means you need to work on them after your time on fix4all has finished.
