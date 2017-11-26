---
layout: markdown_page
title: Support Handbook
---

## Welcome to the GitLab Support Handbook
{: .no_toc}

**Looking for technical support? Please visit the [Support Page](https://about.gitlab.com/support/) instead.**
{:.no_toc}

----

### On this page
{:.no_toc}

- TOC
{:toc}

----

## <i class="fa fa-book fa-fw icon-color font-awesome" aria-hidden="true"></i> Support Resources

- [Support Engineer Onboarding](/handbook/support/onboarding)
   - [Onboarding Checklist](/handbook/support/onboarding/checklist)
- [Support Policies](/handbook/support/policies)
- [Support Workflows](/handbook/support/workflows/)
- [Support Channels](/handbook/support/channels)
- [On-Call](/handbook/on-call/)
- [Advanced Topics](/handbook/support/advanced-topics)

----

## <i class="fa fa-question-circle fa-fw icon-color font-awesome" aria-hidden="true"></i>  Support Direction

The overall direction for Support in 2017 is set by our overall [strategic objectives](/strategy), with a particular emphasis on continued improvement of (Premium) Customer satisfaction with Support. As can also be inferred from our [publicly visible OKR page](https://about.gitlab.com/okrs/), the effort focuses on the following elements.

**Triaging Support Effort**

By triaging support effort through internal SLAs and integration of SalesForce, Zuora, and Zendesk, the team can improve the support experience
for Premium customers while still addressing the questions of _all_ subscribers.

**Increase Capacity & Develop Experts**

In 2016 we expanded the support team significantly, and this trend will continue in 2017. Along the way, the Support team developed internal training tools to assist in rapid, robust, self-guided training for any team member. As GitLab -- the product -- continues to expand, so will the skill and knowledge of all Support Engineers to be able to continue providing an excellent customer support experience.

Know someone who might be a great fit for our team? Please refer them to the [Support Engineer job description](/jobs/support-engineer).

**Actionable Analytics**

Better reporting on ticket metrics (topic, response times, product it relates to, etc.) will help guide the Support Team's priorities in terms of adding to the greatest documentation needs, bug fixes, and support processes.



## Service and support we provide

For an overview of the support we provide to customers and GitLab.com users, please see the general [support page](https://about.gitlab.com/support/). What follows is a more detailed description of the level of service.

## Service Level Agreements
{: #sla}

The channels are sorted in order of priority, there are 4 SLA categories:

| SLA | Channel                | Response Time                          |
|-----|----------------------------|----------------------------------------|
| 1   | [Emergencies (Premium Customers only)](/handbook/support/channels/#emergency-tickets)                | 30 minutes                             |
| 2   | [Premium Customer - Regular Tickets](/handbook/support/channels/#regular-zendesk-tickets)                | 4 hrs (business)                             |
| 3   | [Regular Tickets](/handbook/support/channels/#regular-zendesk-tickets) and [Security](/handbook/support/channels/#security-disclosures) | 1 business day                         |

**Response time indicates the first reply time.**

Preferably we like to answer tickets sooner than the SLA requires.
The higher a channel is in the list the sooner it should be answered.

The above SLAs are based on ticket priority which can be set manually by support agents. See [setting ticket priority](https://about.gitlab.com/handbook/support/workflows/zendesk/setting_ticket_priority.html)

## Tiered Support

GitLab operates with three tiers of customer support. Each tier has a set of responsibilities as outlined below.

### SLA Workflow

Support Engineers should work on tickets within their assigned support speciality as a first priority. Tickets should be picked up in the following order to make sure that SLAs are not breached, and customers receive the proper level of service:

1. Important Tickets
1. Premium Tickets Near Breaching
1. Premium Tickets Breached
1. Enterprise Edition Near Breaching
1. Enterprise Edition Breached

After these are addressed we can work on tickets in any order. When a ticket is breaching or has breached its first reply (or next reply) SLA this ticket must be picked up by any Support Engineer independently of who is assigned to it (although see the note re: courtesy in the list above). This also applies to tickets for Resellers (i.e. anyone picks up if close to breaching, regardless of who the Dedicated Support Engineer is).

### Important Tickets

This is a special view that is used for two purposes:

1. Triggered Emergencies by customers. These will be paged, show up in slack, and now always be at the top of the queue.
1. Strategic Issues as deemed by the support lead. During large customer onboardings or other times where we may need to provide heighted response times the Support Lead may escalate tickets to important status. If so, this will be communicated on a team call. This is an extraordinary measure, and there should be no more than 3-4 organizations this applies to at any given time.

### Hot Queue: How GitLab manages ticket assignments

Support teams often use an "assignment" model, where an agent is assigned a ticket and sees the ticket through to completion. If they are stuck, they can re-assign this ticket to another agent to pick up and try and complete. At GitLab however, we're taking advantage of our global support team and using a system dubbed "Hot Queuing". This system means that we all work from one global queue and it's expected that multiple agents will be working together on most issues. This allows us to do the following:

+ Keep tickets moving forward 24/7.
+ Exposes the team to more issues so more learning is happening.
+ Provide faster response to customers since tickets are not hidden away in an agent's personal queue and "bound" to an agent's workday.
+ Everyone has an accurate global representation of the support load.

#### When should tickets be assigned?

There are times in the support process that an agent will want to assign the ticket to themselves:

+ If they are going to take the ticket to a call/screenshare, take it out of the queue by assigning the ticket to yourself. After the call, if the ticket is still on-going, feel free to unassign yourself so that everyone can continue to move it forward.
+ If you are commited to solving the problem strategically. There are times where we want this, and agents have full discretion to choose that, but it should be few and far between.

#### What if I can't answer a ticket?

If you see a ticket in the queue that you are not able to answer, you should:

+ Make an internal note with your gut feelings as to where the issue might be.
+ CC yourself so you can follow along as the ticket progresses.
+ If you know that agents will need logs or version information, feel free to start with a simple response asking for such.
+ Consider escalating the ticket to Tier 2 (see below)

With the hot queue, we all work together and no one should be scared to start a ticket.



### Tier 1 Support

+ Provide a resolution to the customer, resolved at first point of contact (FPOC).
+ Document information from the customer in relation to the problem.
+ Tickets the Support Engineer is unable to resolve at Tier 1 level should be escalated to Tier 2. The following types of escalations can apply:
   + Resolution was attempted at Tier 1 but the problem persists (interaction with the customer)
   + First reply SLA is breaching and the ticket is not within Tier 1 support scope, inform the customer and escalate to Tier 2.
   + Ticket is not within Tier 1 support scope, escalate to Tier 2.
   + As a rough guideline, agents should consider escalating to Tier 2 after working on a ticket for more than 45 minutes. After escalating to Tier 2, the agent can choose to keep working on it or go back to triaging Tier 1 tickets.
   + If all Tier 1 tickets are cleared out, move on to Tier 2 tickets.

**Examples of requests solved at Tier 1**

+ Known issues/bugs (_A GitLab issue already exists_)
+ Requests for information (customer questions)
   + Quick configuration changes - "How do I enable this feature?"
   + Any other questions, e.g "Does GitLab support this?"

### Tier 2 Support

+ Unknown issues/problems that require investigation. Follow up with customers over multiple interactions. Report the ongoing status of a pending issue/bug fix.
+ Provide workarounds (_where applicable_) to address the problem and quickly resolve any production critical issues.
+ In situations where a bug is found or a new feature is requested the engineer will create a GitLab project issue and track the changes providing an update when necessary.
+ Escalate unresolved support requests to the GitLab Development team. Work closely with developers to analyze, troubleshoot, and resolve difficult issues.
+ When possible, please provide feedback to the agent that escalated the ticket.
  If there is further information required from the customer before the problem
  can be diagnosed, or if the answer is in the documentation, the agent who
  escalated needs to learn about this so that they can perform those tasks
  before escalating in the future.

### Tier 3 Support

Support requests escalated to tier 3:

+ Production critical problems faced by "GitLab Plus" customers.
+ Problems that cannot be resolved at tier 2 within a reasonable amount of time (internal SLA).
+ Requests that require direct input from the [VP of Engineering](https://about.gitlab.com/jobs/vp-of-engineering/) or from the [Support Lead](https://about.gitlab.com/jobs/support-lead/).

#### Escalating between Tiers

We use 3 Zendesk [macros](https://support.zendesk.com/hc/en-us/articles/203690796#topic_kda_eew_uf) to escalate between support tiers. These macros are located under the "Escalations" category in the ZD macros list.

+ `Escalations::Tier 1`
+ `Escalations::Tier 2`
+ `Escalations::Tier 3`

Applying any of these macros will move the ticket to the tier group selected,
create a quick internal note describing why you are escalating.

### Zendesk SLA settings and Breach alerts

SLAs are set as Business Rules within Zendesk. For more information, please refer to the specific [Zendesk](/handbook/support/workflows/zendesk/zendesk_admin.html) page.

## How we're doing

The [Zendesk Insights dashboard](https://gitlab.Zendesk.com/agent/reporting/analytics/period:0/dashboard:buLJ3T7IiFnr)
lists the activity for all of our current channels and summarizes the last 30 days (Zendesk login required).

## Additional resources for the support team

### Breach Hawks

Breach hawks are members of the support team who help the rest of the team keep an eye out for nearly-breaching tickets, so that they can be responded to in a timely manner. Of course, any and all members of the Support Team will have a sense of how many tickets are close to breaching and how high the load is on any given day. But it can happen that you're deep into a ticket, a customer call, etc., unaware of the impending doom. That's where breach hawks come in: they tackle their tickets, but they also keep an eye out for the team at large and can call in the [Support Turbos](#support-turbo) when needed.

### fix4all

"fix4all" is a rotation where one developer - or anyone in GitLab - spends a
week of his or her time helping the support team, as described in more detail on
the ["fix4all" rotation page](/handbook/engineering/fix4all).

### Support Turbo

Every now and then, it may occur that we come close to breaching our SLAs.
To prevent an actual breach from occurring, the Support team can call on the help
of several "Support Turbo" developers who are denoted on the [Team Page](https://about.gitlab.com/team/).

Support Turbos are separate from the ["fix4all"
rotation](/handbook/engineering/fix4all), in that Turbos are on an as-needed
basis while the fix4all rotation is a week-long commitment per person. Anyone
within the support team can call Turbos when there is a need for it. Turbos
should be called by pinging specific people via Slack. If you are in doubt who
is available, you can use `@turbos`, but this may lead to a bystander effect.

The support team calls for help when necessary via Slack. Support Turbos
should treat requests to solve breaching tickets with high priority. If a
Turbo is working on something that cannot wait (e.g. security release,
critical regressions, direction issues with near deadlines), the Turbo should
ensure that someone else fields the request for Turbos by checking with the
development lead or VP of Engineering.

Further guidelines when rolling up your sleeves to do Turbo work:

- Start in either Tier 1 or Tier 2, depending on your own level of comfort. If there are no tickets left in Tier 2, move to Tier 1, and vice versa.
- Turbos should attempt to pick up "single touch" tickets (though this is not always easy to recognize) whenever possible
- Since Turbos log in using a generic agent, there are some special considerations:
   - Pro-actively sign the tickets with their name, or leave an internal note so that the rest of the team knows which individual provided a response. This is helpful to be able to reach out and gain context, etc.
   - Do not [assign tickets](https://support.zendesk.com/hc/en-us/articles/203690956) to the generic agent account. Leave the assignee as the "group", otherwise these tickets will get lost.
   - Please remember that people may pick up any ticket after you've replied. Adding any issues, docs, or follow-up expections for a reply as an internal comment would be really beneficial for the person picking it up after you.


## Calls, Trainings, Implementation Support, and Live Upgrade Assistance

As described in more detail in the [support listings](https://about.gitlab.com/support/) as well as the [support onboarding page](/handbook/support/onboarding/), we offer services beyond simply responding to tickets. More information on scheduling customer calls can be found in the [support standard operating procedures](https://about.gitlab.com/handbook/support/workflows/general/customer_calls.html).

#### Implementation Support

We offer "implementation support" for new EE customers. This is similar to live upgrade assistance, except that live upgrade assistance is a Premium Support offering, while Implementation Support is an option available for purchase by _any_ EE customer.

##### Requesting Implementation Support

- The relevant account executive should open a confidential issue on the [support team issue tracker](https://gitlab.com/gitlab-com/support/issues/), and include the following information:
   - Customer name and domain name
   - Note whether customer is Premium Support, or "only" requesting Implementation Support
   - Collect from the customer, if possible, the following information:
      - Server operating system (Red Hat, CentOS, Debian, Ubuntu) and version
      - Install type:
         - Fresh install?
         - Upgrade from CE?
            - In-place or migration to new server?
            - What version are they on, and what version do they expect to upgrade to?
            - Source or Omnibus installation?
            - Available downtime window - anytime or off-hours?
   - Assign to Support Lead
   - Mark as confidential
- The account executive should make sure to add "Implementation Support" as a product field in Zuora for the customer. This allows the Support team to recognize such requests in Zendesk right away when the customer reaches out to schedule the installation.
- The account executive should then instruct/invite the customer to submit a request for Implementation Support using the [support web form](https://support.gitlab.com). From here on, it is in the hands of the Support Team.

##### What Implementation Support covers

- Pre-installation preparation over email or short call to check that everything is in place for a high probability of success with the installation. If backups need to be made for instance, this should be done before the call / installation since it can take a long time.
- Up to 4 hrs of "live" assistance for the installation, on video call with screen sharing, during regular business hours.
- Following the initial install, the customer will have access to Premium Support for a full week (1 calendar week), including 24x7 emergency support.

##### What Implementation Support does not cover

- Consulting services to help determine how to set up for High Availability
  (except where separately purchased)
- Active assistance in setting up HA systems. We can currently only provide HA
  for an active/active setup as that's what we have
  [documented](https://docs.gitlab.com/ce/administration/high_availability/README.html)
- Further live upgrade assistance beyond the initial implementation (except for
  Premium Support customers)
- The installation and configuration of the underlying server, including (but
  not be limited to) account provisioning, networking, and file system
  configuration
- Establishing a third party authentication & authorization solution (such as
  LDAP, SAML). However,  it **does include** integration of supported
  authentication frameworks into GitLab

## Dedicated Support Engineers

We offer Dedicated Support Engineers (DSE) for Resellers where the relationship is deemed to be more important than the quick turnaround. This means that tickets that arrive in Zendesk from people within the reseller's organization are routed to a dedicated SE by way of a trigger in Zendesk. (Note, until February 2017 we offered this service to Premium Support Customers, but deprecated it in favor of a faster SLA).

- See how to [set a DSE trigger](/handbook/support/workflows/zendesk/create_dse_trigger.html)
- To make sure that the resellers are served well, even when their dedicated SE is not directly
available, there is a view in Zendesk to display all "dedicated" tickets so
that other Support Engineers can see them and jump in to avoid an SLA breach.
- If you are the Dedicated Support Engineer for an account and you will be away for a
foreseeable reason (such as vacation), change the trigger in Zendesk for the duration
of your absence. Any tickets answered by others should mention "I will be helping
you in this matter since your dedicated Support Engineer, [name], is unfortunately
currently unavailable to respond to your ticket." When you return, you should review
all tickets submitted by the subscriber during your absence, and make sure to follow-through
or follow-up as required.

## Contacting support

### Internal Support for GitLab team members

Fellow GitLab team members can reach out for help from the Support Team in various ways:

1. For normal support questions ("Can GitLab do x?", "How do I do y with GitLab?") try:
   - pose your question on the `#questions` channel in Slack, so that everyone can contribute to an answer. If you're not getting an answer, try pinging the group handle for the support team, but be aware that this pings _everyone_  in the team.
1. For longer term or larger scope questions, such a process change, or data gathering
requests, create a [support issue](https://gitlab.com/gitlab-com/support/issues)
1. If customers or users have questions, advise them to contact support directly via the [support web form](https://support.gitlab.com).
1. As a last resort, ping the support team on the support chat channel.

### Support Issue Tracker

The [Support project](https://gitlab.com/gitlab-com/support/issues)
hosts an issue tracker meant to improve our workflow by reporting any
problems that may arise in our tools or processes. It's also meant to
propose and discuss ideas in general.

The issue tracker is open to the community and part of the GitLab.com
group. It should not contain any sensitive information. Links to Zendesk
or other references are encouraged.

### Support chat channels

We use our chat internally as a realtime communication tool. The support channels are as follows:

- [#questions](https://gitlab.slack.com/messages/questions) - If your question is something that you think anyone in the company could answer or is valuable to the greater company to know, ask it here!
- [#Support](https://gitlab.slack.com/messages/support) - This is the general support team channel. Don't know where to ask a question about a ticket? Start here.
- [#support-live-feed](https://gitlab.slack.com/messages/support-live-feed) - Feed of all Zendesk related events
- [#supp-ee-specialists](https://gitlab.slack.com/messages/supp-ee-specialists) - This specifically for the Enterprise Edition specialists.
- [#services-support](https://gitlab.slack.com/messages/services-support) - This specifically for the service support team. They handle GitLab.com account and subscription support and GitHost.
- [#githost](https://gitlab.slack.com/messages/githost) - This channel handles monitoring for GitHost instances.
- [#gitlab-issue-feed](https://gitlab.slack.com/messages/gitlab-issue-feed) - Feed of all GitLab-CE issues
