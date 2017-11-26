---
layout: markdown_page
title: Support Channels
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

Our [support engineers](/jobs/support-engineer) handle the channels listed below.
They are sorted in order of priority (strictest SLA at top), and as a result, it is possible that channels that appear lower
in this list experience longer delays in receiving responses. We are actively [hiring](/jobs/)
more Support Engineers to strengthen the team and provide support to the community.

## Emergency Tickets

When an emergency ticket comes in, it triggers a [PagerDuty](https://gitlab.pagerduty.com) incident. All
Support Engineers must have the PagerDuty application installed on their phones once they are added to
the on-call rotation schedule.

When a PD incident is triggered, the alarm will go off for the person on call. You should acknowledge the
incident within 5 minutes, or the person on second level support will be alerted. The PD incident will
have the link to the corresponding Zendesk issue from where you will continue the conversation with the customer.

Once acknowledged, you need to login to [Zendesk](https://gitlab.Zendesk.com), go to the corresponding ticket
and let the customer know that you will handle their case. On this response you should ask for the best way
to contact them. Usual channels are Phone, Skype, [WebEx](/handbook/support/onboarding/#webex) or Hangouts. It is also a good idea to send them a meeting link where you are waiting, requesting that they join and to let you know if they will not be able to join.

Once the emergency has been resolved, return to the ticket in [Zendesk](https://gitlab.Zendesk.com) and document any steps taken to resolve the issue.

### Crisis Situations

If you are unable to help the customer and their instance is in a critical state (unavailable, uncertainty of
data loss, etc.), you should **escalate** the PD incident to second level support, and work through the issue
together. It may also be necessary to ask for assitance from a developer in the appropriate slack channel. While you are waiting for help to join the call, focus on getting their server to a usable state.

If an emergency takes longer than an hour to resolve,
and/or multiple people are or need to be involved, **start a google doc** that is open to the customer and the wider team at GitLab, and keep track of the
issues and ideas there. Zendesk's 'linear' display of communication with a customer is not as effective in crisis situations, and the
majority of developers do not have access to Zendesk in the first place. Announce the google doc in the appropriate
slack channel (#infrastructure, #development, #general) so that individuals can contribute solutions and ideas. When the crisis
has been resolved, be sure to transfer pertinent know-how from the google doc to relevant documentation, handbooks, and/or
issue trackers, so that the google doc can be deprecated a.s.a.p.  In addition, Support Engineers and Developers involved
in the crisis should make time to have a hangout for hand-off to make sure that everyone has the chance to recover and stay
clear-headed.

## Security disclosures

We have a [Responsible Disclosure Policy](https://about.gitlab.com/disclosure/).
Emails sent to security@gitlab.com go into Zendesk and receive an autoresponder that
says: "Thank you for your responsible disclosure of a potential GitLab vulnerability.
We'll follow up with you within one business day." We also accept reports via [HackerOne](https://hackerone.com/gitlab), see [more information](/handbook/support/channels#hackerone) on this channel.

Please be very patient with these reports. Do not say 'there is no problem', you
might be misunderstanding something that can lead to a 0 day disclosure.
Give examples and keep asking questions until you understand the problem or until
the researcher concludes there is no problem.
If someone invested time to help us, offer to mention them on our [Security Researcher Acknowledgments page](/vulnerability-acknowledgements/)
even if there was no actual vulnerability.
If you say that we'll get back to them **always** mention that they can email us at any time for an update.
This is really important to prevent a 0 day disclosure resulting from us forgetting to respond.

If you need help from developers to diagnose the issue please open a confidential issue so we can work in private. Only if the security report is _about_ confidential issues, then use dev.gitlab.org instead.
If someone opens a public issue please leave a message:
"Thank you for helping to
make GitLab more secure! We removed the contents of your vulnerability disclosure
to keep it private. We opened an internal issue to look at your disclosure. Can
you please use our [Responsible Disclosure Policy](/disclosure/)
to send us an email that references this url so we can communicate in private?"

### PGP Process

The key used to encode/decode PGP messages is stored in our Support Vault on 1Password.
We only provide our public PGP key upon request because it makes collaborating much
harder and only a small percentage of all disclosures are serious enough to require that overhead.

See [PGP Process](/handbook/support/pgp_process) for
information about using the security PGP key pair and decrypting messages.

### HackerOne

We also use [HackerOne](https://hackerone.com/gitlab) to manage security reports.
The HackerOne dashboard lists all reports for which you need to respond within one business day. These
reports are also piped into ZenDesk, but they need to be responded to from the HackerOne dashboard and closed manually in ZenDesk
upon completion of the initial response. Remember that all researchers should receive feedback as with regular support tickets,
and you should not hesitate to triage or escalate the report.

The complete workflow for handling HackerOne reports can be found on the [Security Team page](https://about.gitlab.com/handbook/engineering/security/#hackerone-reports).

If you need to grant HackerOne permissions to a new GitLab user, have an admin send
an invitation from HackerOne and add you to the Internal group. You can find out who
the admins are by asking on the #support channel.

## Regular Zendesk tickets

You should always answer the tickets in a [FIFO](https://en.wikipedia.org/wiki/FIFO_(computing_and_electronics))
manner. Make sure that you answer the tickets that are assigned to you first and then move on to new tickets
that have come in and are unassigned, again using FIFO. When you need others to help please create an issue on
the relevant GitLab issue tracker.

## Follow up on issues posted on GitLab issue tracker

For ZenDesk issues you will have created issues on the relevant issue tracker.
Please refer to the priority as listed under [GitLab Workflow in the handbook](/handbook/communication/#gitlab-workflow).

## GitLab.com Support Tracker

For issues specific to GitLab.com that have nothing to do with availability we have the
[Support Tracker](https://gitlab.com/gitlab-com/support-forum/issues). This forum must also be checked periodically
for new issues and to report back if an issue has been solved. Ensure that you assign the issue to yourself to enable you to keep track of the issue and also to enable other support engineers to easily pick on unassigned tasks at a glance. Some people use this forum to report issues they
are having with their on-premises installation. In that case, you should refer them to the
[CE issue tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues) or to our
[Getting Help](/getting-help/) page, depending on the issue they are having.

## GitLab CE/EE/Omnibus issue trackers

It is always encouraged to take a look at all our issue trackers and respond to bug reports or feature
requests:

- [GitLab EE](https://gitlab.com/gitlab-org/gitlab-ee/issues) some customers create issues here instead of
emailing us. When a new issue is created here, a ticket is created in ZenDesk, so we always know when this is
the case.
- [GitLab CE](https://gitlab.com/gitlab-org/gitlab-ce/issues)
- [Omnibus](https://gitlab.com/gitlab-org/omnibus-gitlab/issues)

See [the issue triage policies](/handbook/engineering/issues/issue-triage-policies) for the above trackers for more information on how issues should be handled.

## TODO Docker

TODO Questions from Docker's [GitLab CE](https://hub.docker.com/r/gitlab/gitlab-ce/) page flow into ZenDesk.

## Non channel work

If you have time for it please improve GitLab: fix bugs, add features, and polish the website.
You can also consider hanging out on IRC to answer questions and help people (#gitlab on freenode.net).
