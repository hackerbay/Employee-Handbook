---
layout: markdown_page
title: "Production Team"
---

## Common Links

- [Public Infrastructure Issue Tracker](https://gitlab.com/gitlab-com/infrastructure/issues/);
please use confidential issues for topics that should only be visible to team members at GitLab.
- [Chat channel](https://gitlab.slack.com/archives/production); please use the
`#production` chat channel for questions that don't seem appropriate to use the
issue tracker or the internal email address for.
- [GitLab Production Calendar](https://calendar.google.com/calendar/embed?src=gitlab.com_si2ach70eb1j65cnu040m3alq0%40group.calendar.google.com&ctz=America/Los_Angeles); add it to your own views by hitting the `+GoogleCalendar` button in the lower right of the screen when viewing the Calendar with the link here.
- [Production On-Call Reports](https://gitlab.com/gitlab-com/infrastructure/issues?scope=all&utf8=%E2%9C%93&state=all&label_name[]=oncall%20report)
- [Production VPN Configuration](https://gitlab.com/gitlab-cookbooks/gitlab_openvpn/blob/master/README.md)

## On this page
{:.no_toc}

- TOC
{:toc}

## Production Team

Production engineers work on keeping the infrastructure that runs our services
running fast and reliably. This infrastructure includes staging, GitLab.com and
dev.GitLab.org; see the [list of nodes](https://dev.gitlab.org/cookbooks/chef-repo/tree/master/nodes).

Production engineers also have a strong focus on building the right toolsets
and automations to enable development to ship features as fast and bug free as
possible, leveraging the tools provided by GitLab.com itself - we must dogfood.

Another part of the job is building monitoring tools that allow quick
troubleshooting as a first step, then turning this into alerts to notify based on
symptoms, to then fixing the problem or automating the remediation. We can only scale
GitLab.com by being smart and using resources effectively, starting with our
own time as the main scarce resource.

### Tenets

1. Security: reduce risk to its minimum, and make the minimum explicit.
1. Transparency, clarity and directness: public and explicit by default, we work in the open, we strive to get signal over noise.
1. Efficiency: smart resource usage, we should not fix scalability problems by throwing more resources at it but by understanding where the waste is happening and then working to make it disappear. We should work hard to reduce toil to a minimum by automating all the boring work out of our way.

## Workflow

### Workout of the Week (WoW) Milestone

Issues in the tracker are organized into [milestones](https://gitlab.com/gitlab-com/infrastructure/milestones)
to define the "workout of the week" (WoW) from one week to the next. The "week"
runs from Wednesday to end of Tuesday. The other milestone in use is "Next WoW"
to track items scheduled for the next week. Every week, the Production Lead
renames the WoW to "WoW ending yyyy-mm-dd", and closes it; then renames "Next
WoW" to "WoW". By doing this, the closed milestones provide a history of what
the team has worked on, while the team only needs to be concerned with two open
 milestones. If issues are added to the "WoW" after the week has already
 started, add the `~unscheduled` label (not needed if the issue is `~outage`
 since those are by definition unscheduled).

### Labeling Issues
{: #issue-labeling}

We use [issue labels](https://gitlab.com/gitlab-com/infrastructure/labels)
within the Infrastructure issue tracker to assist in prioritizing and organizing
work. Prioritized labels are:

- `~(perceived) data loss`
- `~critical`
- `~SL1` and `~SL2`
- `~unblocks others`
- `~outage`
- `~goal`
- `~blocked`

We also use the `~AP1`, `~AP2`, `~AP3` labels as described in [availability &
performance priority labels](/handbook/engineering/performance/#performance-labels).
Those are mainly used to communicate priority of issues to Product Managers, for
scheduling purposes.

#### Goals and meta goal

`~goals` are issues that are in a WoW and we agreed as a team that we will do
everything in our power to deliver them.  Goal issues should fit in one WoW,
that is, they are deliverable in a single week time, if they do not fit in one
WoW we are probably talking about a `~meta ~goal`.

We use this kind of issues to indicate a general direction (generally speaking
something that will take from 1 to 3 months of work) This means that a `~meta
~goal` should be achievable in one quarter.

`~meta` issues that are not also `~goal` are the tasks that are larger than
what fits in a quarter, therefore they need to be sliced into actually
deliverable pieces that can also become a goal.

#### Other labels

We use some other labels to indicate specific conditions and then measure the
impact of these conditions within production or the production engineering team.
This is specially important from the time investment in specific parts of the
production engineering team, to reduce toil or to reduce the chance of a
failure by accessing to production more than enough.

Labels that are particularly important for gathering data are:

- `~toil` Repetitive, boring work that should be automated away.
- `~unscheduled` An issue that became an interruption to the team and had to be
  handled in a WoW. It's unplanned work.
- `~unblocks others` An issue that is allowing some other part of the company
  to deliver something.
- `~access request` When someone is requesting to get access to some part of
  the infrastructure.
- `~requires production access` Every time someone with production access has
  to jump into a console to perform some manual operation like running a script
  in a rails console, or connecting to Redis or the database directly

### Always help others
{: #always-help}

We should never stop helping and unblocking team members. To this end, data should always be
gathered to assist in highlighting areas for automation and the creation of
self-service processes. Creating an issue from the request with the proper
labels is the first step. The default should be that the person requesting help
makes the issue; but we can help with that step too if needed.

If this issue is urgent for whatever reason, we should label them following
the instructions above and add them to the ongoing WoW.

### Issue or outage hand off

Ongoing outages, as well as issues that have the `~(perceived) data loss` label
 and are (therefore) actively being worked on need a hand off to happen as team
 members cycle in and out of their timezones and availability. The on call log
  can be used to assist with this. (See link at top to on-call log).

## Production events logging

There are 2 kind of production events that we track:

- Changes to the production fleet: for this we record things [in the Chef Repo](https://dev.gitlab.org/cookbooks/chef-repo).
  - Deploys will be recorded automagically because of the way we do deploys.
  - General operations can be recorded by creating an empty commit in the repo and pushing it into origin.
- Outages and general production incidents
  - If we are required to act in production manually to perform any operation we should create an issue and consider labeling it as _toil_ to track the cost of such manual work load.
  - It we had a disruption in the service, we must create a blameless post mortem. Refer to the [Outages and Blameless Post Mortems](../#postmortems) section of the Infrastructure page.

## Backups
{: #backups}

### Summary of backup strategy

- Backups of our databases are taken every 24 hours with continuous incremental
data (at 60 sec intervals) streaming into a separate cloud service from the
production fleet. These backups are encrypted.
- Backups of our filesystems are taken via Azure snapshots every 24 hours.

For details see the runbooks, in particular regarding details on
[Azure snapshots](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/azure-snapshots.md)
and [Database backups using WAL-E (encrypted)](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/using-wale-gpg.md)

### R.A.D. - Restore Appreciation Days
{: #rads}

Every last Friday of the month, we have a R.A.D. "party". Two production engineers
tag use this day to test our backup processes by fully restoring a backup of the database
to a test instance and testing it for data integrity. We plan to continue to do this
until such time as the restoring + testing can be done automatically - which is
part of the longer term plans described in
[the production direction meta issue](https://gitlab.com/gitlab-com/infrastructure/issues/1504).

The current procedure for R.A.D is to test restore of the
[production database](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/using-wale-gpg.md),
one or two secondary databases (version, customers, etc.),
[PackageCloud database](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/packagecloud-infrastructure.md),
and test a restore of an NFS server from [Azure snapshots](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/azure-snapshots.md).
We time the restore processes for each of the above to give us an idea of how
long it might take to recover from any given disaster.
