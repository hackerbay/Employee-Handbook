---
layout: markdown_page
title: Product
---

The document below talks about _how_ we do product at GitLab, not about _what_.
For the _what_, see [Product Direction](/direction/).

## Communication
{:.no_toc}

- [**Public Issue Tracker (for GitLab CE)**](https://gitlab.com/gitlab-org/gitlab-ce/issues); please use confidential issues for topics that should only be visible to team members at GitLab.
- [**Chat channel**](https://gitlab.slack.com/archives/product); please use the `#product`, and `#scheduling` chat channels for questions that don't seem appropriate to use the issue tracker for.

## On this page
{:.no_toc}

- TOC
{:toc}

## Other pages related to Product
{:.no_toc}

* [Release posts](/handbook/marketing/blog/release-posts/)
* [Making Gifs](/handbook/product/making-gifs/)
* [Data analysis](/handbook/product/data-analysis/)
* [Technical Writing](/handbook/product/technical-writing/)
* [Markdown Guide](/handbook/product/technical-writing/markdown-guide/)
* [Demo](/handbook/sales/demo/)

## Who to talk to for what

### Introduction

If you have any product-related questions, comments, input or otherwise,
the product manager is the primary person you should talk to,
_if creating an issue does not suffice_. Otherwise, [read this section on how
to create an issue](/handbook/product/#how-to-submit-a-new-issue).

This includes, but is not limited to features, bugs and other
changes that need more attention, be prioritized, changed, or discussed.

Product managers will reach out to stakeholders in making or communicating any
decision. The weight of balancing priorities and ensuring we build excellent
software is on the product manager and they will need all the input they can to
achieve this.

### Inside the DevOps lifecycle

1. Plan - Victor
1. Create - James and Victor
  - Platform - James
    - Git repository management
    - Analytics
    - Wiki
    - Repo editor
  - Code Review - Victor
  - IDE - James
1. Verify - Fabio
1. Package - Fabio
1. Release - Fabio
1. Configure - Fabio
1. Monitor - Josh

### Outside the DevOps lifecycle

- Build - Joshua
- customers.gitlab.com - Mike
- Edge - Job
- Idea to production demo - Mark
- Internationalization - Mike
- Geo - James
- Security product - Fabio
- GitLab.com (subscriptions) - Mike
- Gitter - Mike
- license.gitlab.com - Mike
- Pages - Fabio
- Platform - Mike
  - Signup
  - User management & authentication (incl LDAP)
  - Groups and Subgroups
- Audit log - Mike
- Salesforce - Victor
- Technical Writing - Job
- version.gitlab.com - Victor

Enterprise edition features fall under their respective PM,
not under one PM in particular. For instance, Service Desk falls under Victor,
because it's part of our Issues.

### Mike Bartlett

- Slack: `@mikeb`
- GitLab: `@mydigitalself`

Reach out for anything that falls under the following things.

#### GitLab.com

* GitLab.com subscriptions
* Onboarding
* User management
  * Authentication
  * Authorization
  * LDAP/SAML/SSO integration
* Audit log
* Group management
* Integrations
  * Generic webhooks
* Licenses

For example, if a customer would like us to support a particular extension to
LDAP or wants to have a particular importer, contact Mike.

For anything related to GitLab.com, Mike is also the first responder.
If you want to know more about the rollout of particular features on GitLab.com or how
our plans work, talk to Mike.

#### customers.gitlab.com

Our subscription manager.

#### license.gitlab.com

Our license creator and manager.

### Fabio Busatto

- Slack: `@fabio`
- GitLab: `@bikebilly`

#### CI/CD

* CI
* Jobs (née Builds)
* Runner
* Auto DevOps
* Code Quality
* Container Registry
* Pipelines
* Deployments
* Environments
* Pages
* Integrations
  * Jenkins
  * etc... relating to CI/CD

Fabio handles anything related to CI and CD within GitLab. If a customer would
like to see build artifacts improved, speak to Fabio.

### Joshua Lambert

- Slack: `@joshua`
- GitLab: `@joshlambert`

####  Prometheus

Anything related to monitoring inside of GitLab, falls under Josh's
responsibility. If a customer wants to monitor particular data or see this
improved, speak to Joshua.

[Prometheus](https://prometheus.io/) shipped with GitLab 8.16. The Prometheus Team is tasked with:

Delvering out-of-the-box monitoring and alerting features for applications, including GitLab
Improving [Prometheus open source project](https://github.com/prometheus) to support that goal
Helping other groups, such as infrastructure and UI/UX, instrument and gather data

#### Build

Build is all about how we ship GitLab and make sure everyone can easily install, update and maintain GitLab. This includes:

* installing GitLab on various platforms
* VMs, Docker images of GitLab
* Supported operating systems
* Pivotal Cloud Foundry tile
* Cloud images (AWS, Azure, GCE)
* Kubernetes Helm Charts, Redhat Openshift, Mesosphere DC/OS
* High Availability (HA)
* This also includes introducing/changing any dependency inside of the whole

GitLab stack. This includes (but is not limited to): gems with native
extensions,

### Mark Pundsack

- Slack: `@markpundsack`
- GitLab: `@markpundsack`

#### I2P Demo

Anything related to the [Idea to Production demo](/handbook/sales/demo/) itself
is Mark's responsibility, but not all features in the idea-to-production scope.

### James Ramsay

- Slack: `@jramsay`
- GitLab: `@jramsay`

#### Internationalization (i18n)

Anything related to the contribution, management and development of
multiple-languages support in the interface of GitLab.

#### Platform

* git repository management
  * Hooks
  * LFS
  * Housekeeping (e.g. git gc)
  * Mirroring
  * Import/export
  * Protected Branches
  * File locking
  * Commit history
* Analytics
  * Commit history graphs
  * Cycle analytics
* Wiki
* Repo editor

#### Geo

### Job van der Voort

- Slack: `@job`
- GitLab: `@JobV`

#### about.gitlab.com

#### Technical Writing

The Technical Writing team is responsible for:

* [docs.gitlab.com](https://gitlab.com/gitlab-com/gitlab-docs)
* CE docs
* EE docs
* Technical written tutorials which live in CE or EE docs
  (video tutorials will come later).

We are there to assist developers in their documentation writing process by
providing copy editing and reviewing services and are not responsible for
writing the first draft of documentation for new or updated features.

We will maintain and improve the overall health of documentation e.g.
by creating topic index pages, improving organization and creating tutorials.

We manage our documentation tasks for CE and EE on the following issues boards
which track labels beginning with `docs-`:

* [CE Documentation Issue Board](https://gitlab.com/gitlab-org/gitlab-ce/boards/106589)
* [EE Documentation Issue Board](https://gitlab.com/gitlab-org/gitlab-ee/boards/266349)

#### High level and process

Contact Job for any questions about the strategy of product or process within
product.

### Victor Wu

- Slack: `@victor`
- GitLab: `@victorwu`

#### Discussion

For anything that falls under:

* Markdown
* Issues
  * Quick Actions
* Merge Requests
  * Diffs
  * Code Review
  * Conflict Resolver
* Snippets
* Search
  * Elasticsearch
* Notifications
  * Todos
  * E-mail
* Planning
  * Milestones
  * Labels
  * Due Dates
  * etc.
* Service Desk
* Slash Commands
* Portfolio Management
  * Epics
  * Roadmaps
* Integrations
  * Jira
  * Slack
  * Mattermost
  * Anything else related to conversation and issue management

#### version.gitlab.com

* Every part of version.gitlab.com and usage ping

#### Salesforce

* Everything related to Salesforce and its integration with version.gitlab.com

This means that if a customer would like to see burndown charts, which
relates to issues, you should speak to Victor.

## How to work as/with product

At GitLab, the PM leads their specialization. That is, the Platform PM decides
what is being worked on by the platform team in which release and makes sure
this furthers our goals. This includes bugs, features, architectural changes.

The PM can't be expected to parse every single bug, issue that comes by, so
they will have to rely heavily on the input of the various stakeholders. To be
able to achieve this, both the PM and the stakeholders have to actively work
together. It's a two-way street.

In general terms, if you require something to happen with the product or if you
need engineering resources for a particular change, you approach a PM.
Preferably through creating an issue, the GitLab way and mentioning them there.

In the same vein, PMs are required to ask for feedback from the stakeholder of
particular changes. If a change will affect GitLab.com and its maintenance, a
PM should proactively reach out to infrastructure engineers to help with the
scoping, design and decisions on this change.

It is then up to the PM to weigh all these inputs and decide on a
[prioritization](#prioritization). It is to be expected that they are best equipped to make this
prioritization, keeping in mind all goals of GitLab.

### Example: A customer has a feature request

If you hear a feature request from a customer, you should follow the normal
procedure: you create an issue, label it correctly. Let's say the customer requests an enhancement to Issues. You know by reading above that you'll have label this with `Discussion` and you can mention or reach out to Victor to expedite this if warranted.

Salesperson for organizations asking for Enterprise Edition feature request,
shall work with product manager to arrange conversation to further explore feature request and desired outcome. The process will be:

* Sales schedules 1 hour zoom meeting with product manager, customer and themselves. Call recorded if customer gives permission.
* Product Manager creates any additional questions beyond what is below, they would like answered
  * What version of GitLab are you currently using? CE / EES / EEP?
  * How are you currently doing source code management? GitLab merge requests or another tool? How about CI/CD?
  * How are you currently doing issue management? How are you using HP ALM? Agile/Kanban? What do your sprint/iterations look like? 1 week? 1 month? 2 months?
  * What is the integration like between issue management and source code management?
  * How do teams manage multiple repos? Does a team typically work on repo at a time? Or do they work on multiple repos at the same time?
* Sales sends questions to customer prior to meeting.
* Meeting is created in Salesforce.com
* Sales creates a google document for notes from call with customer.  Google Doc shared with product manager and sales manager
* Sales and product manager schedule 15 minute pre-meeting to share what we know about the customer thus far as not to waste time asking questions we already know the answer to. Notes from this pre-meeting are added to the google document.
* Sales adds a link to the google document under the account object as a note.

### Example: Many support requests come in about a bug with CI

Same as before, make sure an issue is made and make your case with Mark on that
this is becoming a problem and needs to be fixed. Mark will make sure that this
is fixed or resolved in some other way.

### Example: I think create new files is slow

Everything in GitLab should be fast and creating files falls under the
repository, so you create an issue and make Mike aware of it by mentioning it.

Mike in turn will investigate whether this is a general problem or one specific
to GitLab.com, in collaboration with infrastructure and others and schedule any
necessary changes for an upcoming release.

## Product Process

Introducing changes requires a number of steps, with some overlap, that should be
completed in order:

### Prioritization: Ahead of kickoff

1. Requirements for the change are fully defined
1. Design is ready to be implemented
1. Technical architecture has been drafted and is agreed upon
1. Scoping and splitting up in issues has happened

### Execution

1. Backend development
1. Frontend development
1. QA and feature assurance
1. Deploy

## Communication<a name="reach-productteam"></a>

- [**Public Issue Tracker (for GitLab Community Edition)**](https://gitlab.com/gitlab-org/gitlab-ce)
and [**for GitLab Enterprise Edition**](https://gitlab.com/gitlab-org/gitlab-ee) - please use
confidential issues for topics that should only be visible to team members
 at GitLab.
- [**Chat channel**](https://gitlab.slack.com/archives/product) - please use the
`#product` chat channels for questions that don't seem appropriate to use the
issue tracker or more generic chat channels for.

## Goals of Product

Everyone at GitLab is involved with the product. It's the reason why we are
working together.

With every release of GitLab, we want to achieve each of the following
goals.

1. Improve GitLab's existing tools.
1. Achieve [our vision](/direction/#vision) of a
complete toolset.
1. Make our product more interesting for our customers through Products and
EE exclusive features.

## Scope of responsibilities

The product team is responsible for iteration on most of GitLab's products and
projects:

- GitLab CE and EE
- GitLab.com
- about.gitlab.com
- customers.gitlab.com
- version.gitlab.com
- license.gitlab.com

This includes the entire stack and all its facets. The product team needs to
prioritize and weigh bugs, features, regressions, performance, but also
architectural changes and other changes required for ensuring GitLab is
excellent.

## Product at GitLab

GitLab is designed and developed in a unique way.

The direction for the GitLab product is spelled out on the
[Direction page](/direction). This document provides lessons and heuristics on
how to design changes and new features. Our iterative process is demonstrated in
a [blog post](/2017/01/04/behind-the-scenes-how-we-built-review-apps/).

Much of our product philosophies are inspired by [Ruby on Rails doctrine](http://rubyonrails.org/doctrine/) of ['Rails is omakase'](http://david.heinemeierhansson.com/2012/rails-is-omakase.html). I highly suggest reading these.

### TL;DR

1. [Minimally Viable Change](#the-minimally-viable-change): Work in iterations
by implementing only the minimally viable change.
1. [Convention over Configuration](#convention-over-configuration): Avoid
configuration and make it work out of the box.
1. [Be Ambitious](#be-ambitious): do things no one else is doing.
1. [Do not mess with Flow](#do-not-mess-with-flow): _frictionless_ from idea to
production. Avoid adding clicks.

### Product Core Values

#### The Minimally Viable Change

Reduce every change proposal to its very minimally viable form.
This allows us to ship almost anything within a single release,
get immediate feedback and avoid deep investments in ideas that might
not work. Other advantages:

- This helps avoiding the sunk-cost fallacy in situations where we might
decide to drop a change, as we almost never spend more than a few weeks working
on something.
- It prevents over-engineering.
- It forces everyone involved to look for the most simple solution to a problem,
which is often the superior solution.
- It forces working towards an 80/20 solution, where competing products might cater
to the last 20% of the market, a minimally viable solution is _good enough_ for 80%.
- Further changes or enhancements to the change are driven by feedback from
actual users. This is a much more informative mechanism than the intuition
of a product person (though note that this doesn't mean we should just build
whatever feedback tells us).

Virtually every feature must be maintained forever. (The standard of sunsetting a
feature is very high.) Creating a new feature means that you incur the technical,
design, and product costs of maintenance and compatibility forever. Making small
changes with quick feedback loops reduces the risk of introducing a new feature
where the value doesn't justify the long-term costs.

Despite its minimal form, the change
* always requires documentation,
* has to have its usage tracked from day 1, if the feature has a meaningful
impact.

![](/handbook/product/p1.png)

#### Convention over Configuration

Prefer choices that are well thought out, based on current best practices.
Avoid unnecessary configuration.

For example, when considering adding a checkbox or two radio boxes, think really
hard what users really want. Most of the time, you'll find you really only need
one solution, so remove the option. When two possible choices really are
necessary, the best or most common one should be default, and the other one
should be possible. If the non-default choices are significantly less common,
then consider taking them out of the main workflow for making decisions such as
putting them behind an Advanced configuration tab.

Every configuration in GitLab multiplies its complexity, which means
the application is harder to use, harder to develop, and
less friendly to its users.

Making features configurable is _easy_ and _lazy_.
It's a natural reaction to propose a big change to be configurable,
as you worry it'll negatively affect certain users. However,
by making a feature configurable, you've now created two problems.

![](/handbook/product/p2.png)

Work on solutions that work for everyone, that replace all
previous solutions.

Sometimes configuration is inevitable or preferable. GitLab should
work perfectly right out of the box for most users. Your configuration
can't make that experience worse and should always _get out of the
way of the user_.

##### Encouraging behavior

Convention also implies that we're encouraging our customers to do things
in a certain way. A very concrete example of this is the ability to disable
pipelines.We believe that our integrated solution will give a superior user
experience and we're motivated to encourage behavior. For this reason, adding a
configuration to be able to disable this permanently (be that in template or
instance-wide), is something that should be avoided.

Encourage favorable behaviors by limiting configuration.

##### Default to ON

In addition to encouraging behavior by limiting the ability to toggle features,
when introducing new features default to turning things ON if they are
configurable at all.

##### Deciding on configurations

Avoiding configurations is not always possible. When we do have to make this
choice, the second order of preference is to configure something in the GitLab
interface. Only as a last resort should a configuration appear in file
(`gitlab.rb` or `gitlab.yml`).

##### Configuration in file

There are two major configuration files available in GitLab. It should be
avoided to add new configurations to either.

- [`gitlab.yml`](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/config/gitlab.yml.example)
is the configuration file used by the Rails application. This is where the domain is configured. Other configurations should be moved to the UI as much as possible and no new configurations should be added here.
- [`gitlab.rb`](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/files/gitlab-config-template/gitlab.rb.template)
is the configuration file of Omnibus-GitLab. It acts not only as
an abstraction of the configuration of `gitlab.yml` for GitLab-Rails, but also
the source for _all configurations_ for services included and managed within
the Omnibus-GitLab. Newly introduced services probably need to be configured
here.

When you have to add new configuration, make sure that the features and
services are on by default.
Only add a configuration line to either of this configuration files if the
feature or service cannot be fully disabled from the admin UI.

[Convention over configuration is also listed in the CONTRIBUTING file in GitLab's repositories.](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#contribution-acceptance-criteria)

#### Be Ambitious

Many crazy, over-ambitious ideas just sound like they are impossible
because no one else is doing them.

Because we have amazing engineers and a culture of shipping a minimally
viable change, we are able to do a lot more 'impossible' things than other
people.

That's why we're shipping merge conflict resolution, why we shipped built-in CI
before anyone else did it, why we built a better static pages solution, and why
we're able to compete.

![](/handbook/product/p3.png)

#### Simplicity

Doing something simple in GitLab should be simple and require no
human cpu-cycles to do so. Things that are simple now, should
be simple in two and ten years.

This sounds obvious, but messing with Flow is easily done. In most
cases, flow is disrupted by adding another action, another click.

For instance: You want users to be made aware of the rules of a project.
Your proposal is a little popup that shows the rules before they create an
issue. This means that every time that someone creates an issue they need
to click once before resuming their normal action. This is unacceptable.
A better solution is to add a link to the issue that points the user to this.

![](/handbook/product/p4.png)

It's very hard to maintain flow with a lot of configurations and options.
In cases where you want to enforce certain behaviour, the most obvious step
is to add another step or action. This can be avoided by making the action
work in parallel (like a link in the issue), encouraging rather than enforcing
certain behaviours.

We don't want users to be able to construct workflows that break GitLab or
make it work in unpredictable ways.

#### Discoverability Without Being Annoying

Feature discoverability is important to allow existing and new users to access
old and new features, thereby increasing the value for them, and allowing GitLab
to get as much feedback as possible, and as soon as possible, in order to quickly
iterate.

However, if not carefully designed and implemented, UI that purports to increase
discoverability may actually _harm_ the overall experience by constantly shoving
unwanted images and text in the face of the user. The end result is that the user
loses trust in GitLab, so that they no longer take the time to carefully parse text and
other UI elements in the future. Even worse, they might leave GitLab because of this
degraded experience. The following are a few illustrative examples and best practices.

##### Empty states

- Empty states are the simplest paradigm for feature discoverability.
They should always be considered.
- Typically any empty list view should be replaced with an empty state design, similar to below.
- Empty state designs should provide an immediate call to action, thus improving
discoverability.
- Once the UI area is no longer "empty", that design is no longer
present and there is no harm to the user experience at all.

![pipelines_empty_state.png](/handbook/product/pipelines_empty_state.png)

##### Banners

- Banners draw attention to the user by introducing a feature
to them in a nearby context.
- Benefits
  - Attractive graphics to draw attention.
  - Brief explanatory text.
  - A call to action for the user to start using the feature.
- Downsides
  - They invade the user's current flow and intended actions.
  - They are visually disruptive.
- To offset the downsides
  - There should only be one banner on the page at a time.
  - They should carry minimal information and not overwhelm the page.

Think of this: Your co-worker is hard at work in front of their computer. You
suddenly tap their shoulder or yell at them to tell them about some new cool widget.
You better have a good reason for that. Your widget better be awesome.

- Banners need to be dismissible permanently so that a user _never_ sees it again
in their entire lifetime after they have dismissed it.
- We have one chance to introduce a feature to a user with a banner.
- Once they have chosen to dismiss it, it should never appear again because we do
not want to betray their trust when they
click dismiss.
- Trust is incrementally earned with delightful experiences. If a banner
re-appears after dismissal, trust is dismantled.

Back to the analogy: Your co-worker said they don't care about that new cool widget. Never,
ever, ever, bring that up again. They told you they don't care. You need to respect
that.

- Banner dismissal must be associated with the user in the system database, and
that it persists even across version upgrades.
- If a user accesses GitLab with different clients, the dismissal
state is consistent and the user has zero chance of seeing that banner again.
- A corollary is that banners should only be shown when a user is logged in.

![pipelines_empty_state.png](/handbook/product/banner_customize_experience.png)

##### Navigation

Leveraging navigation is an effective design paradigm to introduce a user to a new
feature or general area of GitLab.

- See example design below: There is a subtle pulsating blue dot to draw a user's attention.
- This plants a seed in the user's mind that they can go and investigate that feature at a later time.
- But if at the current moment they don't want to be disturbed, they can ignore it because it is only
a slight visual disturbance (as compared to a banner which takes up more screen
real estate).

- The pulsating blue dot UI should be dismissable, with the same dismissibility
requirements as banners, for the same trust reasons discussed above.
- If dismissed once, it stays dismissed forever, for that user, across all clients that the user can
access GitLab.

- In the same way a page should not have more than one banner, the navigation should
_not_ have more than one call to action (the blue dot in this case).
- We do not want to overload the user with too much noise.

Back to the analogy. We're not going to bother our co-worker with 5 different cool new widgets at the same time.

- GitLab should only ever show at most one blue dot. This should be implemented by
the GitLab having a prioritized list of blue dots stored in the backend.
- It should show the highest priority blue dot that has not already been dismissed.

![tooltip_boards.png](/handbook/product/tooltip_boards.png)

### Prioritization

As this document and the [direction page](/direction) will show you,
there are a million things we want to do,
so how do we prioritize between them and schedule anything in particular?
Roughly speaking, we balance the following priorities:

1. Security fixes
1. Data-loss fixes
1. Regression fixes (things that worked before)
1. Performance fixes
1. Technical debt fixes
1. Other fixes
1. New features

Any new feature will have to meet the following requirements:

1. It is [technically viable](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#contribution-acceptance-criteria)
1. The technical complexity is acceptable (We want to preserve our ability to make changes quickly in the future so we try to avoid: complex code, complex data structures, and optional settings)
1. It is orthogonal to other features (prevent overlap with current and future features)
1. The requirements are clear
1. It can be achieved within the scheduled milestone (Larger issues should be split up, so that individual steps can be achieved within a single milestone)

New features are prioritized on a couple of dimensions:

- Is it a top projects from the [OKRs](https://about.gitlab.com/okrs/)?
- Does it bring our [vision](https://about.gitlab.com/direction/#vision) closer?
- Does it help make our community safer though [moderation tools](https://gitlab.com/gitlab-org/gitlab-ce/issues/19313)?
- Is this something requested by many of our customers?
- Does it help generate revenue for us for our paid [Enterprise Edition Tiers](https://about.gitlab.com/handbook/product/#enterprise-edition-tiers)
- Is it something we need ourselves?
- Has it been much requested on the issue tracker?
- Does it benefit a large portion of our users?

Every release of GitLab has to be better than the last. This means that
bugs, regressions, security issues, and necessary performance and architecture changes always take up
the capacity they require to ensure GitLab remains stable, secure and fast.

We hope to realize our [vision](https://about.gitlab.com/direction/#vision),
while making sure we're building things that our customers want. In practice this means
we aim to ship one or more features that preferably fit within our vision,
but also solve problems our customers have. These features bring the product forward,
and build value for the largest group of people possible. E.g. issue relationships is a highly
requested feature and one that fits neatly within our vision. Everyone will benefit from
this.

In practice, it is not always possible to only ship things that strictly fall within our vision.
Other changes are prioritized and scheduled based on demand. An example would be a specific
form of authentication that is only used in particular organizations. This is not a big
win to all our customers, but if it's not too much work, can be very big win to a subset of
customers. Demand can also come internally, such as things that'll help achieve goals
within the team or specifically drive business goals, such as particular EE features.

We take all priorities in account when planning and schedule larger initiatives across the
teams (such as: we're integrating CI: everyone has to contribute to this in some way),
but most changes are scheduled at a team-level (make issues faster; add a new way to schedule pipelines).

#### Example

To make it concrete with an example, the CI/CD team might ask:

* What else is needed for the idea-to-production vision? Are there other APIs needed for ChatOps integration? Can we trigger manual actions via API? [Environment-specific variables](https://gitlab.com/gitlab-org/gitlab-ce/issues/20367), [activity](https://gitlab.com/gitlab-org/gitlab-ce/issues/19992)
* What moves us towards automatic deploys of `gitlab-ce`?
* What moves the [CI/CD vision](/direction#ci--cd) forward?
* Can we polish the existing feature set? (e.g. [#21126](https://gitlab.com/gitlab-org/gitlab-ce/issues/21126), [#18178](https://gitlab.com/gitlab-org/gitlab-ce/issues/18178), [Show builds in context of pipeline](https://gitlab.com/gitlab-org/gitlab-ce/issues/20863), [#5983](https://gitlab.com/gitlab-org/gitlab-ce/issues/5983), [#3976](https://gitlab.com/gitlab-org/gitlab-ce/issues/3976))
* Can we speed up CI/CD pipelines? (e.g. sticky runners, [automatic parallelization](https://gitlab.com/gitlab-org/gitlab-ce/issues/21480))
* What can we do to make customers happy? ([list](https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&state=opened&utf8=✓&label_name%5B%5D=CI&label_name%5B%5D=customer))a
* What can we do to ship EE features for CI? (e.g. [gitlab-org/gitlab-ee#933](https://gitlab.com/gitlab-org/gitlab-ee/issues/933))

#### Milestones

We schedule an issue by assigning it a milestone; for more on this see
[Planning a Future Release](#planning-future-release).

### Naming features

Naming new features or renaming existing features is notoriously hard and sensitive to many opinions.

#### Factors in picking a name

- It should clearly express what the feature is, in order to avoid the [AWS naming situation](https://www.expeditedssl.com/aws-in-plain-english).
- It should follow [usability heuristics](http://www.designprinciplesftw.com/collections/10-usability-heuristics-for-user-interface-design) when in doubt.
- It should be common in the industry.
- It should not overlap with any other existing concepts in GitLab.
- It should be as few words as possible (so people won't use a shortened name).
- If you remove words from the name, it is still unique (helps to give it as few words as possible).

#### Process

- It's highly recommended to start with discussing this as early as possible.
- Seek a broad range of opinions and consider the arguments carefully.
- The PM responsible for the area involved should make the final decision and not delay the naming.
- Definitely naming should not be a blocker for a feature being released.
- Reaching consensus is not the goal and not a requirement for establishing a name.

#### Renaming

The bar for renaming existing features is extremely high, especially for long-time features with a lot of usage.
Some valid but not exclusive reasons are:

- New branding opportunities
- Reducing confusion as we introduce new adjacent features
- Reducing confusion as we re-factor existing features

### Performance

Fast applications are better applications. Everything from the core user experience,
to building integrations and using the API is better if every query is quick,
every page loads fast. When you're building new features, performance has to be top of mind.

We must strive to make every single page fast. That means it's not acceptable that new
pages add to performance debt. When they ship, they should be fast.

You must account for cases where someone has thousands of objects or just a single.

Read the handbook page relating to [performance of GitLab.com](/handbook/engineering/performance), and the Speed Index targets shown there. Then:

- Make sure that new pages and interactions meet the Speed Index targets.
- Existing pages should never be significantly slowed down with the introduction of new features
or changes.
- Pages that load very slow (even when only under certain conditions) should be sped up by
prioritizing work on their performance or changes that would lead to improved page load speeds
(such as pagination, showing less data ,etc).
- Any page that takes more than 4 seconds to load (speed index) should be considered very slow.
- Use the [availability & performance priority labels](/handbook/engineering/performance/#performance-labels)
to communicate and prioritize issues relating to performance.

Of course, you must prioritize improvements according to the impact (per the [availability & performance priority labels](/handbook/engineering/performance/#performance-labels)).
Pages that are
visited often should be prioritized over pages that rarely have any visitors. However,
as page load time approaches 4 seconds or above, they are no longer useable and should be
fixed at the earliest opportunity.

For a detailed in-depth performance overview, see the [engineering performance page](/handbook/engineering/performance).

### Alpha, Beta, GA

Occasionally we want to test large, complex features without having the
confidence that we'll be able to scale, support and maintain them as they are.
In this case we have the option to release them as Alpha or Beta.

In general, we should avoid releasing Alpha and Beta versions of features.
A minimally viable change should be _viable_ and therefore not need a
pre-release. That said, if it comes to be that we have no valid alternative,
below the definitions of each stage.

It's never acceptable to make changes that can
damage existing production data available to our users.

#### Alpha

- not ready for production use
- unstable and can cause performance and stability issues
- the configuration and dependencies likely to change
- features and functions can be removed
- data loss can occur (be that through bugs or updates)

#### Beta

- not ready for production use
- unstable and can cause performance and stability issues
- configuration and dependencies unlikely to change
- features and functions unlikely to change
- data loss not likely

#### Generally Available (GA)

Passed the [Production Readiness Review](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md) for GitLab.com, which means that it is:

- ready for production use at any scale
- fully documented and supported

### Discouraging, deprecating and removing features

Deprecating features (changes) follows a particular pattern.
Use the language `Discouraged (maintained)`, `Deprecated (not maintained)` or `Removed` to
specify the state of a feature that is going to be or is removed.

Features that are discouraged, deprecated or removed should be:

1. Labelled accordingly in the documentation
1. Labelled accordingly in the application

Features that are Deprecated or Removed should be removed from
marketing pages.

#### Discouraged (maintained)

- planned to be removed at some point in the future, but will be deprecated publicly ahead of time
- maintained: bugs and regressions are fixed
- still available with new installations, but documentation mentions
that use is discouraged (with alternatives if relevant)

#### Deprecated (no longer maintained)

- may be removed at any point in the future
- no longer maintained: bugs and regressions are no longer fixed
- still available with new installations, but documentation mentions
deprecated state

#### Removed

- no longer available in the latest version of the product

## How to work as a PM

If you follow the guidelines above, you won't be writing long, detailed
specs for a part of the product for the next year. So how should you be
spending your time?

Invest the majority of your time in understanding the problem deeply (say 70%).
Then spend 10% of your time writing the spec _for only the first iteration_ and
handling comments, while the remaining 20% you work on promoting it.

A problem you understand well will always have a (seemingly) simple or obvious
solution. Reduce it to its simplest form (see above) and only ship that.

Once you've shipped your solution, both you and the community will
have a much better idea on what can be improved and what should be prioritized
for future iterations.

As a PM you're the person that has to kick-off new initiatives. You're not
responsible for shipping something on time, but you are responsible for taking
action and setting the direction. Be active everywhere, over-communicate and
sell the things you think are important to the rest of the team and community.

As a PM, you need need to set the bar for engineering; to push engineering and
the rest of the company. You almost want engineering to complain about the pace
that product is setting. Our default instinct will be to slow down. We can't
give in to that.

As a PM you don't own the product: ask other people for feedback and give
team members and the community the space to suggest and create without your
direct intervention. It's your job to make sure something is decided and
planned, not to come up with every idea or change.

### Dogfood everything

The best way to understand the pain of the users is to go through what we ask
them to do while setting up or using GitLab. As a PM, you should go through
every feature, at the minimum the ones you are responsible for. All of them. That
includes features that are not in GitLab's UI directly but require server
configuration. If you, as a PM, can't understand the documentation or struggle
to install something, who else would even bother to do it? Going through this is
not only beneficial to understand what the pain points are, it will also tell
you what you can enhance, from a better flow to a better documentation.

#### Example: configuring GitLab

Most of GitLab is configured through the file `gitlab.rb`. It's tempting to
add a new parameter in this file - it's easy, fast to do, and won't require to
add a new UI to allow the configuration of this new setting. However, changing
this file requires you to reconfigure GitLab. To do that, you have to login to
your server and type in commands to reconfigure your instance. Possibly,
multiple times if you have more than one server.

This is not something that we can ask our customers to do. Only by using your
own product and features, will you realize that some practices should be avoided
if you can.

### Product Workflow

Almost everything that we do is documented in an issue.

#### How to submit a new issue

1. If you have time, the first thing you should do is search both CE and EE
projects if a similar issue already exists. We shouldn't create duplicates if we
can avoid them.
1. Identify if the issue is about GitLab Community Edition (CE) or GitLab
Enterprise Edition (EE), although this can easily be changed later.
1. You should clearly state what the current pain point is, what we are trying
to solve, what the benefits will be, what it should do, how to accomplish that
and the next steps.
1. The issue's body should be written in a clear way, without ambiguity.
1. If the body of the issue contains too many paragraphs, it can surely be
rewritten to be shorter.
1. Do not use acronyms or abbreviations. Everyone should be able to jump on the
issue and participate without needing a glossary.
1. Choose which labels are relevant to the issue. If you are unsure about what
certain labels are for, head up to the Labels page ([CE](https://gitlab.com/gitlab-org/gitlab-ce/labels)
or [EE](https://gitlab.com/gitlab-org/gitlab-ee/labels)) and read the
descriptions. The Engineering handbook provides [good hints](/engineering/workflow/#workflow-labels)
on how to choose the right label.
1. Unless you know what you are doing, do not
    - assign someone to the issue
    - assign a milestone
    - set a due date
    - add weight - weight represents the technical complexity and should be
    defined by our developers
1. Mention the different stakeholders in the body of your issue. In most product
related issues, we usually mention the product manager, the design lead (if
needed), and the frontend and backend leads as appropriate.
Some teams have [experts](/jobs/expert) or [liaisons](/jobs/liaisons) that can be mentioned instead of the leads.
Mentioning the people in the body issue will
trigger the notification mechanisms chosen by the people who are mentioned -
therefore there is no need to notify people in another channel after the issue
has been created (Slack, email).

#### Wireframes

When relevant, you can include a wireframe in your issues in order to illustrate
your point. You don't need to include wireframes per se - our UX/design team can
help us on that matter. Simply ping them if you need their help. We like
[Balsamiq](https://balsamiq.com/) for its simplicity and its sketch-y approach.
If you don't have inspiration, you can also paste screenshots of similar
features in other products.

#### What is a Meta issue?

Meta is a label assigned to issues that contain a large list of todos. If you
are familiar with the Agile methodology, it's similar to an epic. At GitLab we
have a short release cycle: the 22nd of every month. In some cases we won't be
able to tackle all the tasks of a meta issue in a single release - this is why
we centralize all the things that we need to do in a meta issue, then break it
down to issues small enough that they will fit into one release. Most of the
time, meta issues generate lots of comments and passionate discussions. As a
consequence, they always lead to something great.

Meta issues themselves generally should not be assigned to a milestone as the
actual work is expressed in sub-issues. Sometimes, if you want the meta issue to
show up in our [direction](/direction) page with a given release, you may want
add a milestone, but only if you know for sure that all sub-issues will be
*completed* by that milestone. Don't assign a milestone for when you're going to
*start* the meta issue.

#### Long-lasting issues

A general guideline is that an issue should only span one release. If we know an
issue is going to span multiple releases, split it up in multiple issues.

Meta/epic issues are the exception to this rule, but should be kept to a
minimum and only serve to guide broader subjects, not a single feature
over multiple releases. This to make sure we stick to our values of
the minimally viable change.

The above means that feature issues should be closed after a first iteration
whenever possible. We'll know more in the future and this keeps remaining
issues short and actionable.

In addition, it's almost never a bad idea to throw away an original plan and
start fresh. Try to do this more often than you're comfortable. Close the issue
and create a new one.

#### Which issue should you be working on?

When you don't have specific tasks assigned, you should work on issues that are
labeled `Product work`, in both EE and CE projects. These are issues that need
our attention the most.

#### Feature assurance

Before a new features is shipped, the PM should test it out to make sure it
effectively solves the original problem. This is not about quality assurance
(QA); developers are responsible for the quality of their code. This is about
feature assurance (FA). Feature assurance is necessary because sometimes there
are misunderstandings between the original issue proposal and the final
implementation, sometimes proposals that seem like they would solve the problem
actually don't, and sometimes solutions just don't feel as good when
implemented.

If you can test out the feature during development, pulling down branches
locally (or with a review app!), that's great. But sometimes it's not convenient
to test a feature until it's bundled into a release candidate and deployed to
GitLab.com. If so, make sure to test out features as soon as you can so any new
issues can be addressed before final release. Also, take the FA cycle into
account when scheduling new milestone work.

#### Managing Upcoming Releases

Refer to the [Product Development Timeline](/handbook/engineering/workflow/#product-development-timeline)
for details on how Product works with UX and Engineering to schedule and work on
issues in upcoming releases.

#### Planning for Future Releases
{: #planning-future-release}

Product Managers assign milestones to issues to indicate when an issue is likely
to be scheduled and worked on. As we consider farther out milestones, the certainty of
the scope of their assigned issues and their implementation timelines are increasingly
vague. In particular, issues may be moved to another project, disassembled, or merged
with other issues over time as they bounce between different milestones.

The milestone of an issue can be changed at any moment. The current assigned milestone
reflects the current planning. If the plan changes, the milestone should be updated
as soon as possible to reflect that changed plan.

Approximately, closer-to-current-time milestones are assigned to issues that are
higher priority. The times also reflect an approximate product roadmap, with further
out milestones reflecting increasing uncertainty.

The milestones are:

- Milestones associated with an actual upcoming release, e.g. `9.4, 9.5`, etc.
- `Next 2-3 months`
- `Next 3-6 months`

These assigned milestones should be used as a signal for GitLab stakeholders and
collaborators (especially UX and Engineering) to help them with their own respective
workflows.

In addition we have a `Backlog` milestone. Product Managers assign this milestone
to issues that they think make sense in the product, but don't have yet a clear
timeline of when it should be worked on. Again, a milestone of an issue can be
changed at any moment, including the `Backlog` milestone.

We make sure to do this ahead of starting to work on a release. Capacity is discussed
between the PMs and the engineering leads.

For a detailed timeline, see [the product development timeline](https://about.gitlab.com/handbook/engineering/workflow/#product-development-timeline).

#### Content of an MVP

We only ship in a Minimally Viable Product mode. Here are some guidelines about
it:

* The issue should be the smallest iteration we can do to address the problem.
* The issue that describes the change should be as concise a possible, while
providing enough information to understand
    * the context,
    * what we want to achieve,
    * who is it for,
    * what are the use cases.
* The MVP should be achievable in one iteration.
* If relevant, check if we can measure the usage of the feature by modifying the
usage ping.
* If the issue generates a lot of discussion, make sure that the issue
description always reflects the latest decisions at any given moment.
* Feel free to edit the issue description without keeping an history or the
previous content, as long as it reflects the latest decisions.
* It's not shipped until it's documented, no matter what the change is.

#### When to create or close an issue

You should create an issue if:

- There isn't already an issue for what you're intending to write. Search first
- a feature is mentioned in chat channels like #product, #competition or elsewhere
- a customer requests a particular feature

You should consider **not** creating an issue when:

- It's an iteration on what we haven't built yet.
- you're planning ahead very far and it's something specific. The further away something is,
the more vague or encompassing the issue should be. This will reduce the total amount of issues. E.g.
create one issue for a new feature, rather than several issues that will follow each other.
- there is an existing issue. Even if the quality is low, people might link to it. Consider rewriting the
description and leaving a comment that you did so. Closing issues to reopen the same issue is generally not a good idea.

Close issues that are either:

1. duplicated elsewhere.
1. no longer relevant due to other reasons.
1. 'not the next iteration': an iteration on a proposed feature that is unlikely to ship in the next few months.

When closing an issue, leave a comment with why you're closing the issue and link
to anything of relevance (the other duplicate, the original feature that this is an iteration on).

The 'not the next iteration' is the most important one to resolve.
It is very easy to create a big plan with meta issues and lots of
But it is essential that we iterate and ship the minimum viable change.
We have to ship the iteration, wait for it to be used, and listen for the feedback.
As a product manager you think about the bigger picture when making a proposal to improve the product.
The important thing is to not write this down is a bunch of issues.
Think of a plan but only record the first step.
This we we can preserve the efficiency of [our value of iteration](https://about.gitlab.com/handbook/values/#iteration).
Closing issues whenever possible is an important part of your job and helps to keep a good overview of what is next.
Consider using the following template to close the issue:

Closing this because XXX is something we should do first. If that feature is done we can learn from having that being used. If we learn that this is still relevant we can then reopen it. See https://about.gitlab.com/handbook/product/#when-to-create-or-close-an-issue for more detail about this policy.

#### Competition Channel

When someone posts information in the `#competition` channel that warrants
creating an issue and/or [a change in `features.yml`][features], follow this
procedure:

- Create a thread on the item by posting `I'm documenting this`
- Either do the following yourself, or link to this paragraph for the
person picking this up to follow
- If needed: create an issue
- [Add the item to the `features.yml`][features]
- If GitLab does not have this feature, link to the issue you created
- Finish the thread with a link to the commit and issue

### Where should you look when you need help?

* The first things you should read are this handbook as well as the [general
handbook](/handbook/).
* You can ask questions related to Product in the `#product` Slack channel.
* General questions should be asked in `#questions`.
* Specific Git related questions should be asked in `#git-help`.
* HR questions should be asked in `#peopleops`.

### Shipping

#### Internal and external evangelization

Before shipping a new or updated feature, you are responsible for its
evangelization, both internally and externally. When something is released, the
following teams need to be aware of it as they will all need to do something
about it:

* Marketing: depending on the importance of the feature, we need the help of
marketing to promote this feature on our different communication channels.
* Sales: sales need to know what's new or changed in the product so they can
have better arguments to convince new or existing customers during their sales
process.
* Support: as they are in contact with our users and customers all day long,
support should perfectly know how our products work.

You can promote your work in several ways:

* start with documenting what will be released and share this documentation with
the different teams,
* schedule meeting, if you think it's important, with the teams listed above.

#### GitLab University

To promote a major new feature internally, you can ask to host a GitLab
University, a company wide demo session. This is a great opportunity to make
sure every one is on the same page.

### Major feature rollout

Major features deserve proper attention from product and marketing. With a
proper rollout, we'll have ample marketing opportunities and receive more
feedback ahead, during and after the release.

Here is the ideal rollout schedule. For each step, there is the indication about
who is responsible for it.

1. Feature is drafted in an issue (PM)
2. Feature is planned in an upcoming release (PM)
3. A feature proposal blog post is made (PM or Dev), where we'll describe
	* What we are planning on doing,
	* How you'll be able to buy it: CE or any EE Editions,
	* Link to the issue,
	* When it'll be available, if possible,
	* Anything else that is interesting to share in order to fuel the discussion.
4. Feature is implemented, documentation is written (Dev).
5. Feature should appear on the website (Marketing)
	* For very significant features: Feature page on the website is made and
  pushed, with the mention "Available from X.X"
	* For other features: Feature should be listed on some page (/comparison,
    Enterprise page, /features page).
6. Feature is launched with the release (Marketing)
	* "Available from X.X" is removed
	* Documentation and other resources are linked
	* Pricing page is updated if needed
7. Feature is highlighted in a blog post (Marketing)
	* This post is linked from the feature page on the website (if applicable)

### How and when to reject a feature request

Rejecting a feature request or a merge request is not an easy thing. People can
feel quite protective of their ideas. They might have invested a lot of time and
energy in writing those ideas. You can be tempted to accept a feature only to
avoid hurting the people who thought of it. Worst, if you reject an idea too
harshly, you might discourage other people to contribute, which is something we
want to avoid.

However, as the number of issues and merge requests grow more and more, we should
be diligent about rejecting features we are sure will not do. It's better for
everyone: for the product team so we don't maintain a huge backlog of things we
will not do anyway, and for the users who won't have to wait for our feedback
indefinitely.

Note: it's fine to not respond to issues that we think have potential until they
gather momentum.

Feature requests and merge requests can be rejected for the following reasons:

* Not within our scope: the Direction page [lists all the areas](/direction/#outside-our-scope)
where GitLab, the product, won't go. Point the issue's author to this article
and close the issue.
* We don't want another setting: whenever we can, we try to [avoid having settings](#convention-over-configuration).
Some settings are inevitable - most aren't. Ask the user to change how she
approaches the feature in order to get rid of the setting.
* Too complex: we want to have a user-friendly, simple product that does complex
things. Not the other way around. Tell the user to take a step back and think
about the problem she wants to solve in the first place. Offer directions on
what she could do instead. If she's not willing to do it, indicate that you will
have to close the issue/merge request because it will go nowhere.
* Bring an Enterprise exclusive feature to the Community Edition: this problem
is already addressed in the [About page](/about/#contributing-an-ee-only-feature-to-ce).
Indicate that we will investigate whether the feature can be ported to the
Community Edition, discuss it with other teams members and come back to the user
in a timely fashion.
* Low priority: sometimes, features are interesting but we simply don't have the
capacity to implement them. In that case, simply tell the truth and indicate that
we don't have enough resources at our disposal to do it at the moment.

Don't forget to thank the authors for the time and effort taken to submit the
feature request/merge request. In all cases and without exception, you should be
nice and polite when interacting with users and customers.

### Responsibilities and Expectations

As a PM you're expected to:

- Follow the issues you've been involved with / are assigned to as PM. That usually means reading all comments. Use email notifications for this.
- Make sure the issue description and title is updated when necessary. It should always reflect the current state of the issue.
- Make sure issues are moved forward when needed. Not only should you avoid being the bottleneck, you should be the person moving issues forward when they get stuck or overlooked.
- Make sure features solve the original problem effectively
- Make sure features are complete: documentation, marketing, API, etc.
- Know when to cut corners and when not to. If we merge documentation a day
later, that's usually acceptable. Inversely, discovering by demand of a
customer that documentation is lacking is not.
- Excite and market new features and changes internally and externally
- Help build a vision for GitLab and GitLab's features
- Deeply understand whatever it is you're working on. You should be spending a lot of time learning about your subject matters.
- Have regular meetings (at least one a week) with customers
- Make sure marketing materials related to your work are updated

#### Customer meetings

It's important to get direct feedback from our customers on things we've
built, are building or should be building.

As a PM you should have regular meetings with customers that are using the
things you've been working on and with customers that are not - in order
to get an idea of why they're not switching to our solution.

##### Set up a meeting

To setup a customer meeting, identify what you're interested in discovering
and prepare appropriately.

You can find information about how customers are using GitLab through sales
and version.gitlab.com. Sales and support should also be able to bring you
into contact with a customer.

There is no formal internal process to schedule a customer meeting,
if that need arises, we can formulate one.

##### During and after

During the meeting, spend most of your time listening and obtaining information.
It's not your job to sell GitLab, but it should be obvious when it's the time
to tell more about our products.

After the meeting, make sure all your notes and feedback lands in issues.

#### Marketing materials

As a PM you're responsible for making sure changes you've shipped are well represented
throughout GitLab's documentation and marketing materials. This means that on
release, [`features.yml` is updated][features], documentation is merged and deployed, and
any existing content is updated where necessary.

It's not acceptable to do this after the release. GitLab is very complex and features
and functions are easily missed, even those that provide significant value to customers
(e.g. the many ways you can authenticate with GitLab).

You can recruit the help of the marketing and technical writing team if needed,
but it's highly recommend to do small updates yourself. This takes less time and overhead
than communicating what needs to be done to someone else.

#### Release posts

As a PM, you are [accountable](/handbook/marketing/blog/release-posts/#general-contributions)
for adding new features (under your umbrella) to the monthly release post, respecting the
guidelines defined on the
[release posts handbook](/handbook/marketing/blog/release-posts/) and its **due dates**.

Every month, a PM will take the
[leadership](/handbook/marketing/blog/release-posts/#authorship)
of the release post, being responsible for delivering it in time.

Refer to the [release posts handbook](/handbook/marketing/blog/release-posts/)
to go over all the details.

### Communication guidelines for product managers

As a product manager, you're vastly more knowledgeable about GitLab than anyone else.
This means that you have the responsibility to always provide a balanced and complete
view when discussing anything related to product. Other people won't have the same
background and context you might have.

For example, when someone involved in sales asks you about upcoming issues in a particular
area, you respond with:

- a clear overview of what is coming (link to the single source of truth)
- how that relates to the request of the customer
- that we're flexible in this and are interested in hearing more from the customer
- if necessary: a suggestion to discuss this directly with the customer

This seems obvious, but a slight misunderstanding can have big consequences:
promising a customer that something is done by a certain date vs. indicating
that we're working on something and hope to have a first iteration in the near future.

## Enterprise Edition Tiers

### Talking about EE only decisions

When talking about why a certain change goes into Enterprise Edition instead of Community Edition, [mention the stewardship paragraph in the about page][stewardship]
directly and link to it.

[stewardship]: /stewardship/#what-features-are-ee-only

### What goes in what version

Determine what market segment is most likely to need a feature, then classify as follows:

- CE contains features that are **most** relevant for [SMB](https://about.gitlab.com/handbook/sales/#market-segmentation)
- EE Starter contains features that are **most** relevant for [mid-market organizations](https://about.gitlab.com/handbook/sales/#market-segmentation)
- EE Premium contains features that are **most** relevant for [large organizations](https://about.gitlab.com/handbook/sales/#market-segmentation)
- EE Ultimate contains features that are **most** relevant for [strategic organizations](https://about.gitlab.com/handbook/sales/#market-segmentation)

There aren't any features that are only useful to larger organizations,
so for every EE feature there will be smaller organizations that might need it.
We're not saying that there aren't any small organizations that need the feature,
just that we think that larger organizations are more likely to need it.
The more of GitLab that you use the more likely it is that you benefit from a higher tier.
Even a single person using GitLab might be best off using EE Ultimate.

Deciding on whether something should be a Premium feature or a Starter feature can be hard.
Bringing something down the tiers (EEP to EES) is always possible, whether the opposite isn't.

### EES, EEP, and EEU requirements

All EES, EEP, and EEU features should:

- Work easily for our customers that host GitLab on-premise. That is their
licenses need not to be updated and the new feature is default-on for the
instance
- Work with GitLab.com Bronze / Silver / Gold subscriptions. This means there has to be
some way of toggling or using the feature at a namespace level.
- Have documentation, be featured on [products](/products) and
[comparison](/comparison) at launch

### Pricing plans

For more information about how we thing about pricing please see the [pricing page in the handbook](/pricing).

### Designing features for Enterprise Editions

To make it possible to ship a feature for Enterprise Edition, ideally
the code is completely separate. I.e. the frontend and backend of the feature
only exist in the `gitlab-ee` project. However, this is not always possible.

In cases where it's preferable to have the backend code live in the `gitlab-ce`
repository, it's acceptable to only ship the frontend for the feature in EE.
In practice this makes the feature EE-only.

## GitLab.com

GitLab.com runs GitLab Enterprise Edition.

To keep our code easy to maintain and to make sure everyone reaps the benefits
of all our efforts, we will not separate GitLab.com codebase from EE.

To avoid complexity, GitLab.com subscriptions and GitLab EE tiers have a 1:1 match.
No exceptions to this rule are acceptable.

- Free: Community Edition features
- Bronze: Enterprise Edition Starter features
- Silver: EES + Enterprise Edition Premium features
- Gold: EES, EEP + Enterprise Edition Ultimate features
- Public projects are considered to have a Gold subscription level

Because we are not able to give admin access and do not yet have full feature
parity between a self-hosted instance and GitLab.com, we avoid saying that there is
a one on one match between subscriptions levels and tiers in marketing materials.
This has been the cause of confusion in the past for customers.

### Restriction of closed source Javascript

In addition, to meet the [ethical criteria of GNU](https://www.gnu.org/software/repo-criteria-evaluation.html),
all our javascript code on GitLab.com has to be free as in freedom.
This is why we [moved to Piwik](https://about.gitlab.com/2015/11/27/gitlab-switches-to-piwik-analytics-to-free-the-javascript/),
over Google Analytics. Read more about this on [GNU's website](https://www.gnu.org/philosophy/javascript-trap.html).

## Private tools and dashboards for monitoring and KPI tracking

[EE usage](https://version.gitlab.com/): dev.gitlab.org account

[Grafana](http://performance.gitlab.net): Google gitlab.com account

[Kibana](https://log.gitlap.com): dev.gitlab.org account

[LogTrail](https://log.gitlap.com): dev.gitlab.org account

[Piwik](https://piwik.gitlab.com): GitLab 1Password account

[S3stat](https://www.s3stat.com): GitLab 1Password account

[Sentry](https://sentry.gitlap.com): dev.gitlab.org account

## Writing about features

As PM we need to constantly write about the features we ship: in a blog post,
internally to promote something, in emails sent to customers.

While we want every PM to have his unique voice and style, there are some
guidelines that one should take into account when writing about features. Let's
highlight them with a concrete example, Preventing Secrets in your repositories,
 that [we've shipped in 8.12](/2016/09/22/gitlab-8-12-released/#preventing-secrets-in-your-repositories-ee).

* Start with the context. Explain what the current situation is without the
feature. Describe the pain points.

> It's a bad idea to commit secrets (such as keys and certificates) to your repositories: they'll be cloned to the machines of anyone that has access to the repository, only one of which has to be insecure for the information to be compromised. Yet it happens quite easily. You write `git commit -am 'quickfix' && git push` and suddenly you've committed files that were meant to stay local!

* Explain what we've shipped to fix this problem.

> GitLab now has a new push rule that will prevent commits with secrets from entering the repository.

* Describe how to use the feature in simple terms.

> Just check the checkbox and GitLab will prevent common unsafe files such as .pem and .key from being committed.

* Point to the documentation and any other relevant links (previous posts, etc).

### Writing release blog posts

For every monthly release, there is a blog post announcing features.
The blog post should contain anything _exciting_ or _disruptive_.
All new features should appear in the blog post.
We want to help people understand exciting features (which are often new), and increase adoption.
Disruptive features may change workflows or even introduce unavoidable inconveniences.
We want to anticipate questions and avoid confusion by communicating these changes through the blog post.
Smaller tweaks and bug fixes don't necessarily need to be mentioned,
but if interesting, can be included at the bottom of the post.

## Areas

You have a hierarchy of bundling features:

1. DevOps lifecycle stages (stages), see [SDLC](https://about.gitlab.com/sdlc/)
1. Product categories (categories), see [SDLC](https://about.gitlab.com/sdlc/)
1. Feature areas (areas), see end of ['Plan Positioning' Google Doc](https://docs.google.com/document/d/19RNBDoy-rLmR3PEhN8GJVOdb8Et2-IMjaMPYcXzUUEI/edit#)
1. Individual features (features), see [Features](https://about.gitlab.com/features/)

The areas are used to position the plans (CE, EES, EEP, EEU).
Each plan has a maximum of 7 areas.

When we introduce a new feature we look for each plan if it matches an area.
We start at EEU and go down to CE, the first area that matches is the plan for the feature.
For CE the areas are equal to the 7 stages of the DevOps lifecycle.
This is because if areas of non-CE plans don't match it ends up in CE, so it has to cover everyone.

## Analyst product categorizations

GitLab is a single application that spans many product categories.
Forrester and Gartner define several of these categories and their definition
of a space can be useful to determine what important competing products are.
Below some relevant categories that GitLab is or will be competing in.

### Forrester: Continuous Integration Tools

- Leaders: GitLab CI, CloudBees Jenkins, CircleCI, Microsoft
- [link to report](https://www.forrester.com/report/The+Forrester+Wave+Continuous+Integration+Tools+Q3+2017/-/E-RES137261)

### Forrester: Configuration Management Software For Infrastructure Automation

- Leaders: Puppet Enterprise, Chef Automate
- [link to report](https://reprints.forrester.com/#/assets/2/675/'RES137964'/reports)

### Gartner: Software Change and Configuration Management Software

- Market Guide: Amazon Web Services, Atlassian, BitKeeper, CA Technologies, Codice Software, Collabnet, GitHub, GitLab, IBM, Micro Focus/Borland, Microsoft, Perforce, PTC, SeaPine Software, Serena, SourceGear, Visible Systems, WANdisco, Wildbit
- [link to report](https://www.gartner.com/document/3118917)

### Gartner: Software Test Automation

- Leaders: HPE, Tricentis, IBM
- [link to report](https://www.gartner.com/document/3512920)

### Forrester: Modern Application Functional Test Automation Tools

- Leaders: Parasoft, IBM, Tricentis, HPE
- [link to report](https://www.forrester.com/report/The+Forrester+Wave+Modern+Application+Functional+Test+Automation+Tools+Q4+2016/-/E-RES123866)

### Gartner: Performance Testing

- Market Guide: Automation Anywhere, BlazeMeter, Borland, CA Technologies, HPE, IBM, Neotys, Oracle, Parasoft, RadView, SmartBear, Soasta, Telerik, TestPlant
- [link to report](https://www.gartner.com/document/3133717)

### Gartner: Application Release Automation

- Leaders: Electric Cloud, CA (Automic), XebiaLabs, IBM
- [Magic qaudrant](http://electric-cloud.com/resources/whitepapers/gartner-magic-quadrant-application-release-automation/)

### Forrester: Continuous Delivery and Release Automation

- Leaders: Chef, CA, Microsoft
- [link to report](https://www.forrester.com/report/The+Forrester+Wave+Continuous+Delivery+And+Release+Automation+Q3+2017/-/E-RES137969)

### Gartner: Application Performance Monitoring Suites

- Leaders: New Relic
- [link to report](https://www.gartner.com/doc/3551918)

### Gartner: Application Security Testing

- Leaders: HPE, Veracode, IBM, Synopsys, WhiteHat Security
- [link to report](https://www.gartner.com/doc/3623017)

### Forrester: Application Security Testing

- Vendor Landscape report: Acunetix, CAST Software, Checkmarx, Contrast Security, Data Theorem, HPE, IBM, Netsparker, NowSecure, Parasoft, PortSwigger Web Security, Qualys, Rapid7, Rogue Wave Software, SiteLock, SonarSource, Synopsys, Trustwave, Veracode, Whitehat Security
- [link to report](https://www.forrester.com/report/Vendor+Landscape+Application+Security+Testing/-/E-RES137462)

### Gartner: Project Portfolio Management

- Leaders: Planview, CA Technologies, Changepoint
- [link to report](https://www.gartner.com/document/3728917)

### Forrester: Strategic Portfolio Management Tools

- Leaders: AgileCraft, CA, ServiceNow
- [link to report](https://www.forrester.com/report/The+Forrester+Wave+Strategic+Portfolio+Management+Tools+Q3+2017/-/E-RES136707)

### Forrester: Portfolio Management For The Tech Management Agenda

- Leaders: CA, Planview
- [link to report](https://www.forrester.com/report/The+Forrester+Wave+Portfolio+Management+For+The+Tech+Management+Agenda+Q1+2015/-/E-RES114742)

### Gartner: Enterprise Agile Planning Tools

- Leaders: CA, Atlassian, VersionOne
- [link to report](https://www.gartner.com/doc/3695417)

### Forrester: Enterprise Collaborative Work Management

- Leaders: Clarizen, Redbooth, Wrike, Planview, Asana, and Smartsheet
- [link to report](https://www.forrester.com/report/The+Forrester+Wave+Enterprise+Collaborative+Work+Management+Q4+2016/-/E-RES121721)

### Forrester: Application Life-Cycle Management, Q4 2012

- Covered in report: Atlassian, CollabNet, HP, IBM, Microsoft, PTC, Rally Software, Rocket Aldon, and Serena Software
- [link to report](https://www.forrester.com/report/The+Forrester+Wave+Application+LifeCycle+Management+Q4+2012/-/E-RES60080)

### Gartner: Container Management Software

- Market Guide: Apcera, Apprenda, CoreOS, Docker, Joyent, Mesosphere, Pivotal, Rancher Labs, Red Hat
- [link to report](https://www.gartner.com/document/3782167)

### Gartner: Data Science Platforms

- Leaders: IBM, SAS, RapidMiner, KNIME
- [link to report](https://www.gartner.com/doc/3606026)

## Links

- [Engineering Workflow](/handbook/engineering/workflow)
- [Release posts handbook](/handbook/marketing/blog/release-posts/)

[features]: https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/doc/features.md
