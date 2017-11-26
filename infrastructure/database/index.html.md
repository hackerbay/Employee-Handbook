---
layout: markdown_page
title: "Database Team"
---

## Table Of Contents
{:.no_toc}

* TOC
{:toc}

## Focus of Database Team

The Database team focuses on improving performance, reliability, and availability
of GitLab and GitLab.com. This is done through a variety of different ways such
as:

* Making application changes to improve the performance of database queries.
* Adding database monitoring capabilities in GitLab.
* Deploying pgbouncer to reduce the number of database connections that are
  necessary.
* Adjusting the settings of GitLab.com's PostgreSQL cluster for optimal
  performance.
* Building, testing, and maintaining a failover system for both GitLab.com and
  users of GitLab's High Availability features.
* Assisting other developers by answering database related questions and
  reviewing database related changes.
* Documenting tools, monitoring, and database best practices in order to share as
  much knowledge as possible.

For further details, see the [current vacancy for a Database
Specialist](/jobs/specialist/database/).

## Common Links

To make it easier to find your way around you can find a list of useful or
important links below.

### Monitoring & Performance Related Tools

As a database specialist the following tools can be very helpful:

* [Private Grafana](https://performance.gitlab.net/): for both application and
  system level performance data.
* [Performance Bar](https://docs.gitlab.com/ce/administration/monitoring/performance/performance_bar.html):
  type `pb` in GitLab and a bar with performance metrics will show up at the top
  of the page. This tool is especially useful for viewing the queries executed
  and their timings.
* [Sherlock](https://docs.gitlab.com/ee/development/profiling.html#sherlock):
  a tool similar to the performance bar but meant for development environments.
  Sherlock is able to show backtraces and the output of `EXPLAIN ANALYZE` for
  executed queries. Enable by starting Rails with `env ENABLE_SHERLOCK=1 bundle
  exec rails s`.
* <https://explain.depesz.com/> for visualizing the output of `EXPLAIN ANALYZE`.

### Dashboards

The following (private) Grafana dashboard are important / useful for database
specialists:

* [Postgres Stats](https://performance.gitlab.net/dashboard/db/postgres-stats)
* [Postgres Tuple Statistics](https://performance.gitlab.net/dashboard/db/postgres-tuple-statistics)
* [Transaction Overview](https://performance.gitlab.net/dashboard/db/transaction-overview?orgId=1)
* [Rails Controllers](https://performance.gitlab.net/dashboard/db/rails-controllers?orgId=1)

### Documentation

Basically everything under
<https://docs.gitlab.com/ee/development/README.html#databases>, but the
following guides in particular are important:

* [What requires downtime?](https://docs.gitlab.com/ee/development/what_requires_downtime.html)
* [Adding database indexes](https://docs.gitlab.com/ee/development/adding_database_indexes.html)
* [Post Deployment Migrations](https://docs.gitlab.com/ee/development/post_deployment_migrations.html)
* [Background Migrations](https://docs.gitlab.com/ee/development/background_migrations.html)
* [SQL Migration Style Guide](https://docs.gitlab.com/ee/development/migration_style_guide.html)
* [SQL Query Guidelines](https://docs.gitlab.com/ee/development/sql.html)

For various other development related guides refer to
<https://docs.gitlab.com/ee/development/README.html>.

### Slack Channels

We recommend you join at least the following Slack channels:

* [#database](https://gitlab.slack.com/messages/database)
* [#development](https://gitlab.slack.com/messages/development)
* [#performance](https://gitlab.slack.com/messages/performance)
* [#production](https://gitlab.slack.com/messages/production)

Don't try to keep up with everything as some of these channels can see a lot of
activity, instead just idle there in case somebody needs you. The most important
channel is `#database`.

We also recommend turning off `@here` and `@channel` mentions for `#production`
and `#development` to reduce the amount of unwanted notifications.

## Important Groups

Make sure you are a member of the group
<https://gitlab.com/gitlab-org/database-specialists>. This makes it easier to
assign merge request approvers or mention all database specialists at once.

## Workflow

There are 3 main repositories database specialists work in:

* <https://gitlab.com/gitlab-org/gitlab-ce>
* <https://gitlab.com/gitlab-org/gitlab-ee>
* <https://gitlab.com/gitlab-com/infrastructure>

We also primarily use the following labels:

* "database": for anything database related.
* "AP1", "AP2" and "AP3": for estimating/specifying the performance and
  availability priority (from high to low). See ["Availability and Performance
  Priority Labels"](https://about.gitlab.com/handbook/engineering/performance/#performance-labels)
  for more information. In short: AP1 is the most important, AP3 the least.
* "performance": for performance related issues and merge requests.

### Issue Boards

To make it easier to work we have the following issue boards:

* [CE Database Issue Board][ce-issue-board]: This board shows all CE issues
  labelled as "database" and AP1, AP2 or AP3.
* [EE Database Issue Board][ee-issue-board]: The same board but for EE issues.

For the Infrastructure repository we don't have AP issues, instead you can just
use the following link to list all "database" issues:
<https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=database>.

### Creating Issues

Always make sure an issue exists for the work you are about to perform. As a
rule of thumb: work does not exist unless there is an issue for it. Issues are not
only used to describe the work to do, but also to track progress. Make sure you
update your issues on a regular basis with your findings, statistics, progress,
etc. It's better to share too much information on the work being done than to
share too little.

### Assigning Issues

We recommend you only assign issues to yourself if you are actively working on
them. If you are simply _interested_ in an issue it's best left unassigned until
you are working on it. This way you don't end up with an issue list that is
thousands of issues long with no progress being made.

### Ask!

Don't sit around doing nothing if you can't find anything to work on! Instead
just ask what should be done in the `#database` channel if no AP1/2/3 issues
are available.

### Weekly Goals

For planning we use so called "Weekly Goals". Weekly goals are written in an
issue that's created for the next work week / sprint. These work weeks range
from Wednesday to the end of the next Tuesday. These issues are assigned to all
database specialists. Some examples of these issues:

* <https://gitlab.com/gitlab-com/infrastructure/issues/2459>
* <https://gitlab.com/gitlab-com/infrastructure/issues/2394>

The work to be done is planned together with other database specialists. When
planning try to plan enough for 4 or so days, but make sure you don't plan too
much. It's better to plan less and achieve everything than to plan a lot and
achieve very little.

The format of the issue bodies is fairly straightforward: for every database
specialist there is a checklist referring to other issues (perhaps with some
brief info) to perform, which are checked off as work is completed. Checklists
can be created using the following Markdown:

```markdown
* [ ] This is an item on my checklist
* [x] This item is marked as done
```

The results of the weekly goals are discussed in the weekly infrastructure call,
which takes place 30 minutes before the team call.

An overview of existing issues can be found at
<https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=database&label_name[]=goal>.

To make it easier to create these issues you can use the Infrastructure issue
template "Database Goals".

## Notification Settings

To prevent yourself from getting buried in unread notifications it's best to
adjust the default notification settings of your GitLab account. We recommend
the following:

* Set the "Global notification level" setting in
  <https://gitlab.com/profile/notifications> to "Disabled".
* Make sure "Receive notifications about your own activity" is unchecked.
* Disable notifications for the "gl-infra" group if you are a member, unless you
  are interested in getting notifications whenever somebody mentions `@gl-infra`
  (which can happen quite a lot).

Using this setup you will _not_ get any Email notifications. TODOs are still
created but _only_ if somebody mentions your username or a group you are a
member of.

## Slack Notifications

We recommend turning off Slack notification popups as these can be quite
invasive, especially when multiple notifications are displayed at once. Turning
off the sound notifications can also greatly help as you won't be distracted
every time somebody sends you a message or mentions your username.

[ce-issue-board]: https://gitlab.com/gitlab-org/gitlab-ce/boards/345590?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=database
[ee-issue-board]: https://gitlab.com/gitlab-org/gitlab-ee/boards/349503?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=database
