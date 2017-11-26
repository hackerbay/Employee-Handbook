---
layout: markdown_page
title: "Infrastructure"
---

## Common Links

- [Public Infrastructure Issue Tracker](https://gitlab.com/gitlab-com/infrastructure/issues/); please use confidential issues for topics that should only be visible to team members at GitLab. No longer active, but kept for reference, is the legacy public [Operations issue tracker](https://gitlab.com/gitlab-com/operations/issues) as well.
- Refer to the [Work of the Week](https://gitlab.com/gitlab-com/infrastructure/milestones) section to see the ongoing tasks being done by the infrastructure team.
- Chat channels; please use chat channels for questions that don't seem appropriate to use the issue tracker for.
  - [#prometheus-alerts](https://gitlab.slack.com/archives/infrastructure): monitoring tools post into this channel, production engineers should monitor this channel to act on alerts. "Acting on" may be remediating or just fixing noisy alerts.
  - [#production](https://gitlab.slack.com/archives/production): for general conversation about production engineering.
  - [#security](https://gitlab.slack.com/archives/security): for general conversation about security.
  - [#gitaly](https://gitlab.slack.com/archives/gitaly): for general conversation about Gitaly.
  - [#database](https://gitlab.slack.com/archives/database): for general conversation about database related topics.
- Refer to the [runbooks](https://gitlab.com/gitlab-com/runbooks) and contribute back to them. Also see the [runbooks](#runbooks) section on this page.
- [GitLab Production Calendar](https://calendar.google.com/calendar/embed?src=gitlab.com_si2ach70eb1j65cnu040m3alq0%40group.calendar.google.com&ctz=America/Los_Angeles); add it to your own views by hitting the `+GoogleCalendar` button in the lower right of the screen when viewing the Calendar with the link here.
- [Production On-Call Log](https://docs.google.com/document/d/1nWDqjzBwzYecn9Dcl4hy1s4MLng_uMq-8yGRMxtgK6M/edit#)
- [Monitoring](https://about.gitlab.com/handbook/engineering/monitoring/): For all things logging, monitoring, and performance.

## On this page
{:.no_toc}

- TOC
{:toc}

## Other Pages
{:.no_toc}

- [GitLab.com architecture](production-architecture/)
- [GitLab.com environments](environments/)
- [Monitoring GitLab.com](/handbook/engineering/monitoring/)
- [Performance of GitLab.com](/handbook/engineering/performance)
- [Database team handbook](database/)
- [Gitaly team handbook](gitaly/)
- [Production team handbook](production/)
- [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md)
- [Security team handbook](/handbook/engineering/security/)
- [GitLab.com and GitLab Hosted data breach notification policy](https://about.gitlab.com/security/#data-breach-notification-policy)
- [On Call](/handbook/on-call/)

## Infrastructure goals and team(s)

### High level goals

Per our [current set of OKRs](/okrs/), the infrastructure team works on making
"GitLab.com ready for mission-critical tasks". Specifically, this means the
infrastructure team works on
<a name="internal-sla"></a>

1. GitLab.com's availability and scalability.
   - Current goal: Availability at [99.9%](http://stats.pingdom.com/81vpf8jyr1h9/1902794/history).
   - Availability here is defined as the uptime of the site linked above (which
     is in fact the first issue in the gitlab-ce issue tracker; for more on
     pingdom see the [monitoring page](/handbook/engineering/monitoring/)),
     measured per calendar month, and as recorded on
      [pingdom](http://stats.pingdom.com/81vpf8jyr1h9/1902794/history).
1. GitLab.com's performance.
   - Current goal: [99% of user requests have "First Byte - Internal" < 1 second](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=2&fullscreen&orgId=1)
   - Latency here is measured via the "Transaction Timings"
   dashboard linked above. Those timings only represent part of the [web request processing time](/handbook/engineering/performance) but are well-defined and most within control of the Infrastructure team.
1. Keeping it easy to maintain GitLab instances, for administrators all over the world.

### Teams in Infrastructure

To accomplish these goals, we've defined four teams within Infrastructure to tackle:

* [Production](/handbook/infrastructure/production/): keeping GitLab.com available
and scalable. This includes (among other things) ownership of staging, improving
deployment processes, and building an infrastructure that enables development to
go fast.
* [Database](/handbook/infrastructure/database/): keeping GitLab.com's database
 available, fast, and scalable.
* [Gitaly](/handbook/infrastructure/gitaly/): making Git access available,
scalable, and fast.

### Collaboration across the company for Site Reliability

Individuals from the Infrastructure team frequently collaborate very closely
with different product teams (e.g. Platform, Discussion, CI, Packaging, etc) and
[Reliability Experts](https://about.gitlab.com/jobs/expert/reliability/) from
product teams collaborate closely with the Infrastructure team. Together, they
work on the topics listed above, using the principles and methods of [Site
Reliability Engineering](https://landing.google.com/sre/book.html) a little bit
more each day.

#### Embedded Production Engineers
{: #embedded}

Production engineers can be "embedded" with one or multiple
different teams for anything from a few weeks to months.

If you are an "embedded" Production Engineer, then you are expected to:

- Participate in team calls for the team that you are embedded with.
- Keep up to date with the general Production Engineering team and duties:
   - Take care of issues, fires, and on-call. In fact, those will still be your
priority unless something else has been explicitly agreed between the Production
Lead and the team where you are embedded.
   - Continue to report to the Production Lead and participate in the Production
    team meetings.
    - Share the context of the team you are embedded with, with the rest of the
    Production Team.
- Help the team that you are embedded with to make their feature set or service
 "production ready". Use and improve upon the [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md).

Since at GitLab most "feature sets or services" are mostly already in
production, being embedded means that you work on making sure that the feature set or
service meets the requirements for Production Readiness _post factum_. This will
typically involve
improving the runbooks and documentation, alerting, monitoring, coding for
resiliency, etc. An embedment ends when the feature set or service has passed the
criteria in the [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md)
and is already in production.

#### Reliability Experts

Developers focused on the reliability and production readiness of their feature
set or service are named [Reliability Expert](/jobs/expert/reliability) and work
closely with Production Engineers.

## Production and Staging Access

*Roles*
Production access (specifically: ssh access to production) is limited to people
in the roles of production, support, and release-manager. If you are in one of
these roles and don’t have access, please open an issue in the infrastructure tracker,
make the request and add the label “access”. All roles are listed in the [GitLab chef cookbook](https://gitlab.com/gitlab-cookbooks/gitlab_users#currently-defined-roles)  

Staging access is treated at the same level as production access because it
currently contains production data. This will be changed in the future to
allow broader access.   

In order to fully remove all production access in the future, we need to accomplish the following:  

1. Get a list of the reasons why people need access to production https://gitlab.com/gitlab-com/infrastructure/issues/2702
2. Fix the logging infrastructure  https://gitlab.com/gitlab-com/infrastructure/issues/2225#note_35367845
3. Fix staging to resemble production , and allow logins  https://gitlab.com/gitlab-com/infrastructure/issues/2674
4. Fix canary deployments   https://gitlab.com/gitlab-com/infrastructure/issues/1504
5. Look to automate or create tools for everything we discovered in step 1 (not fixed by steps 2-4)
6. iterate steps 1 & 5 over until there is no need for access to production.  

Any other team member should not have access to production. If you are such a
team member and you need information from the production environment, please
request it via an issue in the infrastructure issue tracker. Please
make sure to apply the appropriate labels. For more information, read about the
[labels](production/#issue-labeling) that are most useful and the Production
team's commitment to [always try to help](production/#always-help).

### Release Managers _do_ have access

[Release managers](/release-managers) require production ssh access to perform
deploys. Therefore, release managers will have production access until
production engineering can offer a deployment automation that does not require
chef nor ssh access. This is an ongoing effort.  

### Developer Team leads access  

In order to help facilitate quick incident resolution, team leads will have production access.

### CI/CD team
The ci/cd team has production access to the runners and runner managers. The up to date list of the runners and runner managers roles are in [GitLab chef cookbooks] (https://gitlab.com/gitlab-cookbooks/gitlab_users#currently-defined-roles)

---  
### Feature Flags: Access and Use
{: #feature-flags}

Feature Flags provide an excellent way to introduce new features into the code
base and into production that might affect the stability of GitLab,com,
as described in [the "direction" issue](https://gitlab.com/gitlab-org/gitlab-ee/issues/779).

Having the power to toggle a feature flag does not constitute Production Access
as defined above (ssh access). In general, the more Developers have access to
use feature flags the better since it should make it much easier for Developers
to quickly assess the impact of the feature on performance, stability, etc.
However, the act of toggling _can_ have an impact on the health and operation
of the production environment.

To balance the potential benefits with the possible risks, we've developed the
following rules:
1. Any Developer can be granted access to toggle feature flags; simply request
this via an issue in the infrastructure issue tracker.
1. The feature flag can only be toggled by calling the chatbot from the
`#production` chat channel. This is done on purpose to make sure that the
Production Engineers can be aware of the activity.
1. The feature flag should be set to expose no more than 1% of the traffic to
the new feature - at least initially.
1. When you enable a feature flag, you need to be available (responsive on
  Slack) for a period of time that makes sense in the context of the feature;
  typically count on several hours post-toggle. That way if there _are_ any
  unintended consequences, you (as the expert on the feature) can quickly help
  the team identify possible reasons and remedies for the unexpected behavior.
1. It's absolutely possible to deviate from these rules for any
reason: please open an issue to discuss the needs of your particular case
before executing it. This gives the Production team a chance to consider what
unforeseen consequences this may have.

#### How to get access to Feature Flags

Access to feature flags is on an ad-hoc basis. Please open an issue with
infrastructure and include the label “access request”. Pease note that you need
an existing account with Marvin. To get an account you just need to talk to
Marvin, it will create the account automatically for you.

### Access to systems with pseudonymized data

Some systems use pseudonymized versions of production data, for example by working
with a subset of repos and a database that has been pseudonymized using the
["howto psuedonymize" runbook](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/pseudonymization-gitlab-db.md).
This allows developers to test features and functionality on staging and on test
installations with relatively realistic database sizes. However, the process of
pseudonymization of  the data does _not_ remove or replace all of the user data and should
therefore still be treated with the same level of security and protection that
we have in place for access to regular production data.

---

## Cloud Service Access

### Amazon AWS

Unlike other cloud providers, AWS is used for a wide variety of services and access
is available to various team members for various _levels_ of access that match
their _need_ (for example, access to Billing vs. access to S3 buckets with backups).
Various AWS accounts exist for different purposes. As an example, there is an AWS
account that is used to manage S3 backups, and another that is available to the
Support Team to test instances installed on AWS services.

- For an overview of the various accounts and
their basic purpose, find the Google Sheet titled "GitLab AWS accounts" (only
accessible by GitLab team members).
- To gain access to an AWS account, go to the "GitLab AWS accounts" sheet and
leave a comment on the appropriate tab (corresponds to AWS account) specifying
your request (e.g. "please give me X role in Y account") and mention one of the
Administrators for the relevant account (listed on that same sheet) to get their
attention.
   - Note that this is identical to the process we use to gain access to 1Password
shared vaults, and also how we gain access to email aliases in the GitLab Email
Forwarding google doc. It is not an ideal process, and we expect to [replace it with a
simpler process eventually](https://gitlab.com/gitlab-com/infrastructure/issues/2556).
   - For "deep" levels of access (e.g. access to production data of any kind),
   you may still need to open an issue on the infrastructure issue tracker to
   have your manager authorize the request.
- Do _not_ share access credentials for AWS accounts. AWS has an excellent audit
log, but it is only of value if "users" on the system are not shared by multiple
actual people. Bear in mind that for each AWS account that you have access to, you _may_ have
a different username, which can be confusing.
- For the AWS account that is in use for GitLab.com related services, details on the
configuration of security groups within Amazon AWS and a full breakdown of
policies and services is detailed in the Google Doc entitled "AWS - GitLabdotCom - Security
Groups and Policies" (only accessible by GitLab team members).
- Some actions require access to the AWS account by the root user (for example
  change account names, accept another group into the account,
change billing settings, etc.). Each AWS account can only
have a single root user. To reduce the [bus factor](https://en.wikipedia.org/wiki/Bus_factor)
multiple people within GitLab have access to the root user credentials (this is the one exception to
the earlier rule of not sharing AWS credentials). If you require AWS root access
for any reason, contact one of the people listed on the "AWS root access" secure
note in the shared vault on 1Password.



### Azure

To be written.

---

## Documentation

### Runbooks

[Runbooks are public](https://gitlab.com/gitlab-com/runbooks). They are
automatically mirrored to our [private development environment](https://dev.gitlab.org/cookbooks/runbooks/),
this is so because if GitLab.com is down, we can still access the runbooks there.

These runbooks aim to provide simple solutions for common problems. The
solutions are linked to from our alerting system.  The runbooks should be kept
up to date with whatever we learn as we scale GitLab.com so that our customers
can also adopt them.

Runbooks are divided into 2 main sections:

- _What to do when_: points to specific runbooks to run in stressful situations (on-call)
- _How do I_: points to general administration texts that explain how to perform different administration tasks.

When writing a new runbook, be mindful what the goal of it is:

- If it is for on-call situations, make it crisp and brief. Try to keep the
following structure: pre-check, resolution, post-check .
- If it is for general management, it can be freely formatted.

### Chef cookbooks

Some basic rules:

- Use maintained cookbooks from https://supermarket.chef.io.
- Create a wrapper cookbook whenever a feature is missing.
- Make sure our custom cookbooks are public available from https://gitlab.com/gitlab-cookbooks.
- Make sure there is a copy in our DEV environment https://dev.gitlab.org/cookbooks and setup push mirror to keep it in sync.
- Berkshelf should only point to our cookbooks in DEV so we are able to fix our cookbooks whenever GitLab.com comes unavailable.
- Cookbooks should be developed using the team. We use merge requests and code review to share knowledge and build the best product we can.
- Cookbooks should be covered with ChefSpec and TestKitchen testing in order to ensure they do what they are supposed to and don't have conflicts.

Generally our [chef cookbooks](https://gitlab.com/groups/gitlab-cookbooks) live in the open, and they get mirrored back to our
[internal cookbooks group](https://dev.gitlab.org/cookbooks) for availability reasons.

There may be cases of cookbooks that could become a security concern, in which case it is ok to keep them in our GitLab
private instance. This should be assessed in a case by case and documented properly.

### Internal documentation

Available in the [Chef Repo](https://dev.gitlab.org/cookbooks/chef-repo).
There is some documentation that is specific to GitLab.com. Things that are specific to our infrastructure
providers or that would create a security threat for our installation.

Still, this documentation is [in the Chef Repo](https://dev.gitlab.org/cookbooks/chef-repo), and we aim to
start pulling things out of there into the runbooks, until this documentation is thin and GitLab.com only.

## Outages and Blameless Post Mortems
{: #postmortems}

Every time there is a production incident we will create an issue in the [infrastructure
issue tracker](https://gitlab.com/gitlab-com/infrastructure/issues) with the _outage_ label.

In this issue we will gather the following information:
* The timeline of events: what happened first, what later, what reasoning triggered what action.
* Sample graphs or logs captured from our monitoring explaining how they drove our reasoning.
* [The 5 whys](https://en.wikipedia.org/wiki/5_Whys) that lead to the root cause that triggered the incident.
* The things that worked well
* The things that can be improved
* Further actions with links to the issues that cover them

These issues should also be tagged with any other label that makes sense, for
example, if the issue is related to storage, label it as such.

The responsibility of creating this post mortem is initially on the person that
handled the incident, unless it gets assigned explicitly to someone else.

### Public by default policy

These blameless post mortems have to be public by default with just a few exceptions:
* The post mortem would affect a customer or employee privacy: revealing the real user name, email, private project names, any data that can identify the person, etc.
* The post mortem would reveal billing information.
* The post mortem would reveal GitLab's confidential information.

That's it, there are no other reasons.

If what's blocking us from revealing this information is shame because we made
a mistake, that is not a good enough reason.

The post mortem is blameless because our mistakes are not a person mistake but
a company mistake, if we made a bad decision because our monitoring failed we
have to fix our monitoring, not blame someone for making a decision based on
insufficient data.

On top of this, blameless post-mortems help in the following ways:

* We can help people understand the complexity of running a service in
production, and how things can go wrong.
* We help ourselves to learn by reflecting and analyzing on why this issue has
happened.
* We force ourselves to think about what we need to do to not make the same
mistake again, or to improve our infrastructure in a way that we don't have to
deal with the same incident.
* We open our reasoning and information to the public so they can chime in and
help us out.
* We leave a great trace of information for onboarding new engineers. They can
see how production fails.
* We can use these post-mortems for recruiting and marketing.

Once this Post Mortem is created, we will tweet from the GitLabStatus account
with a link to the issue and a brief explanation of what is it about.


## Making Changes to GitLab.com

The production environment of GitLab.com should be treated with care since we
strive to make GitLab.com so reliable that it can be mission-critical for our
customers. _Allowable downtime_  is a scarce resource.

Therefore, to be able to deploy useful and cool new things into production,
we need to
- use checklists to prepare and carry out the changes, and
- schedule the (non-automated, non-self-serve) changes we make to our
production environment (to be sure the necessary people are there, and to prevent having multiple changes happening at the same time).

### Production Change Checklist

Any team or individual can initiate a change to GitLab.com by following this checklist. Create an issue in the infrastructure [issue
 tracker](https://gitlab.com/gitlab-com/infrastructure/issues) and select the [`change_checklist` template](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/change_checklist.md)

### Changes that need a checklist and a schedule

For example:
- When you introduce something _new_ such as installing `pgbouncer`, enabling ElasticSearch, etc.
- Anything that _may_ result in downtime. Not sure? Then assume that it will result in downtime.
- Anything that constitutes a change to GitLab.com _and_ requires the assistance of a Production Engineer.

### Changes that _may_ need a checklist, but not explicit scheduling

For example:
- A self-service process, such as adding alerting (which only requires a
  merge request to the relevant repo), or fixing a chef-client.
- "Quick" fixes that do _not_ require a Production Engineer.

### Changes in staging

Testing things in staging typically only needs scheduling to avoid conflicting with others, but is otherwise straightforward since it is mostly self-service.

- Consider using the same format of the checklist - it is good form to know
how to roll back for example. Using the checklist will also set the baseline for
when you want to introduce the change into production; thus saving time. But it
is not required to follow the full checklist in order to make changes on staging.
- **Do** schedule changes to staging, on the "GitLab Production" calendar (link at [top of page](#common-links)). This
is to prevent conflicts when different people or teams are trying to work on
staging for different purposes.
- Given that there are quite a few people who can use self-service in staging,
there should be no need for resourcing there from the Production team, and you
do not need an explicit OK from the Production Lead.

### Deployments

Deployments of release(s) (candidates) are a special case. We don't want to block
deployments if we can avoid it. And since they are currently performed by release managers there is
generally no need for someone from production engineering to be heavily involved.
Still, follow the next steps to schedule a deploy:

* **Schedule the deploy** both in staging and production on the "GitLab Production"
calendar (link at [top of page](#common-links)) as soon as possible. Do this to avoid conflicting with any other
production operation that will happen (don't oversubscribe).
* Use a 4 hr block too, sometimes deploys delay to start for odd reasons, you
don't want to run out of time.
* Notify the production engineering team by inviting ops-contact. This will raise
awareness.
* [Announce the deployment] well in advance.
* If you need help from production engineering for whatever reason, be explicit
in the invite, or get in touch in the production chat channel to ask.

[Announce the deployment]: https://gitlab.com/gitlab-org/takeoff/blob/master/doc/announce-a-deployment.md


## Make GitLab.com settings the default

As said in the [production engineer job description](jobs/production-engineer/index.html)
one of the goals is "Making GitLab easier to maintain to administrators all over the world".
One of the ways we do it is making GitLab.com settings the default for all our customers.
It is very important that GitLab.com is running GitLab Enterprise Edition with all its default settings.
We don't want users running GitLab at scale to run into any problems.

If it is not possible to use the default settings the difference should be documented in
[GitLab.com settings](https://about.gitlab.com/gitlab-com/settings/#gitlab-pages)
_before_ applying them to GitLab.com.

## Involving Azure

- GitLab has access to "Azure Rapid Response". The level of support is described
on [their website](https://azure.microsoft.com/en-us/support/plans/response/),
but TL;DR it means that the SLAs are:
   - Initial response for Sev A < 15 mins, Sev B < 2 Hours, Sev C < 4 hours.
- The Azure team prefers if we ask questions via the support portal, but there is
an Azure representative whom we can ping in our issue tracker. This is mostly
helpful in cases of non-urgent questions, and questions of an advisory nature.
- Light hand-holding for things such as architecture review is available. To
reach out for this assistance, submit an "advisory case" ticket through the portal.

* Azure subscription and service limits, quotas, and constraints: https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits
