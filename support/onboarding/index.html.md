---
layout: markdown_page
title: Support Engineer Onboarding
---

## On this page
{:.no_toc}

- TOC
{:toc}

----


## Expectations of the support team
{: #expectations}

As members of the support team we are the first to interact with someone when they have a problem or question.
As such it is up to us to represent the company and make sure we present ourselves properly. Therefore we are
expected to:

- Always be friendly and respectful.
- Be open to new ideas and points of view.
- It is OK if you don't know something. You can always ask someone else.
- It is OK to say no to a customer, but try to suggest a workaround and escalate to a Senior if necessary.
- Read the guidelines on how to [respond on social media](https://about.gitlab.com/handbook/marketing/social-media-guidelines).

## Support Engineering Bootcamp
{: #se-bootcamp}

When you first join the team everything will be new to you. In order to get you
started with GitLab quickly a [Support Engineering Bootcamp Checklist](https://about.gitlab.com/handbook/support/onboarding/checklist)
will be created for you to help guide you through your training.

## Tools

We use Zendesk to handle tickets, and we will sometimes schedule calls. That is most often done through Zoom, but can also be done through WebEx if the customer's system does not allow them to install the Zoom plugin.

### Zendesk

For more detail on Zendesk, see the [Zendesk specific page](/handbook/support/workflows/zendesk/).

### Zoom

Zoom is a powerful and light-weight videoconferencing tool that works for 90% of the customer calls (see the bit about WebEx for the other 10%). As part of your support boot camp, you should have received a Pro account there so that you can schedule your own calls. To start a call, log on to [gitlab.zoom.us](https://gitlab.zoom.us/) using your personal credentials and click on "My Meetings" for a link to your personal meeting room. Share this with the customer.

Zoom allows you to see the customer's desktop and
to control it on request; and it also offers the option of recording the call (we do not typically do this, be certain to ask for the customer's permission of you have a good reason for recording). It also gives the customer the possibility to join via phone and
us the possibility to use our computer audio connection.

### WebEx

For some customers, only Cisco systems are allowed and for those cases, WebEx will be the best tool for calls. To start a call / session use the `GitLab Support` WebEx account. Go to our
[WebEx Portal](https://gitlabmeetings.webex.com), click on the login button on the top right and use the
credentials found in the Support Vault on 1Password.

![WebEx Login](/images/support/web-ex-login.png)

Once logged in, click the `Enter Room` button to start the WebEx meeting and send the following link to
the customer and ask them to join the call.

```
https://gitlabmeetings.webex.com/meet/gitlabsupport
```

![WebEx Room](/images/support/web-ex-room.png)

WebEx allows you to see the customer's desktop and
to control it on request. It also gives the customer the possibility to join via phone and
us the possibility to use our computer audio connection.


## Handling tickets

### Assigning a ticket to yourself
{: #assign-yourself}

Assign a ticket to yourself the moment you decide you are going to work on it. If the nature of the problem
requires you to investigate further, let the customer know that you need further time to investigate, assign
the ticket to yourself, and submit the reply. By assigning the ticket to yourself you are letting your team members
know that you will work with this customer and by replying to the customer, even if you need further time to
craft a proper answer, you are acknowledging their request.


### Point to documentation, or make it
{: #document-it}

As a general rule, you should always include a link to the applicable documentation as
part of your response to a ticket. If the documentation does not exist yet, then
_make_ the documentation and send the link in the response. For those situations
where making documentation is a more time consuming exercise:

- Click the "Document this" checkbox (found on the left-hand side of the ticket)
- Enter an ["internal note"](https://support.zendesk.com/hc/en-us/articles/213519318-Adding-comments-to-tickets#topic_bpn_sbd_bv) describing the documentation requirements
- Update the ticket
- Do not just look at the Docs and see how other directories and files were
structured, we are trying to change some of that so please follow the [documentation styleguide](https://docs.gitlab.com/ce/development/doc_styleguide.html#location-and-naming-of-documents)

Tickets with the "Document this" option are added to a ZenDesk view ["Documentation"](https://gitlab.zendesk.com/agent/#/filters/91188447).
A [Zap](https://zapier.com/app/editor/9938098/overview) is used to add ticket details to a [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1GcQvDThsXuV_n4OFwdYNmq07oO7coiS8xkMP84_-eKo/edit#gid=0).

### Create issues

During your interaction with the customers you will most likely need to create or update an
issue, either for a feature request, for a bug, or for further documentation.
Since we do everything in the open, it is good practice to send the link of the
issue to the requesting customer, so that they can also keep an eye on the discussion
there, and weigh in if necessary.


Workflow for creating an issue:

- Visit the issues page of the project, [CE example here](https://gitlab.com/gitlab-org/gitlab-ce/issues)
- Search to make sure the issue doesn't already exist
- Click **New Issue**
- Choose a template from the **Choose a template** dropdown and take a look at the
**Typical kinds of issues created** below.
- Fill in all the relevant sections
- @mention someone in the issue to attract attention to it. Choose an expert [here](https://about.gitlab.com/team/) or feel free to ask
in the #support channel on slack who it should be reviewed by. Do not worry that you are poking
someone to review a job when you don't even know them and they might be much more senior than you,
if it's not appropriate for them, they will know the right person to pass it along to and do that.

Typical kinds of issues created:

- **Bug**
   - Make sure it looks like a bug - otherwise ping one of the developers to confirm.
   - Reproduce the bug
   - Assign the bug fix to the next milestone
   - Report back to customer with a link to the issue
- **Proposed feature request**
   - Provide maximum information and use case from customer in the issue,
mention any alternatives, how badly the customer wants it.
   - Ask a developer for opinion (do we want this feature in GitLab: yes/no, the
developer might ask more questions before answer)
   - Report back to customer with a link to the issue

Typical workflow for updating an existing issue:

1. Comment on the issue that another customer is having a problem, adding relevant details
and a link to the ZenDesk ticket. Also if it is an EE customer, add the `~customer`
label to the ticket.
1. Send the customer a link to the issue and invite them to comment.
1. If the customer replies with satisfaction that their concern is
being addressed after seeing the issue, ask them if it would be okay to mark
the ticket as resolved and to instead continue the conversation on the issue.

Sometimes it is helpful to create an issue on the [support issue tracker](https://gitlab.com/gitlab-com/support/issues)
when dealing with a **tough ticket**. Creating an issue allows more people within
GitLab easy access to the questions and suggestions since not everyone is familiar
with ZenDesk. When in doubt, create an issue. Also see the section on [when to escalate](#when-escalate).

#### Ticket fields

The only custom ticket field we use is the `GitLab issues` field. In here you will fill in every
related GitLab issue that is related to this ticket as a way to cross-link between them.

Every issue you mention here must also contain a link to the ticket in question, either in the
description or in a comment.

Use this field as a reminder of when and where to follow up.

### Recording information about the organization
{: #fix-organization}

We use ZenDesk Organization Profiles to store relevant information about the customer, like environment setup,
hardware specs, usage patterns, etc, so that if you need this information, it is readily available from
within ZenDesk. To see this information, click on the link to the left of the requester's name (in our example
it's the link that says 'GitLab' right next to Haydn's name).

![ZenDesk Organizations](/images/support/zendesk-org.png)

If a customer does not have an organization set up you can create one by clicking on the field next to
the requester's name (This field says GitLab on the screenshot above, to the left of Haydn's name). When
doing this, please fill in the correct name and email domains for the new Organization.

On the organization view, use the `Notes` field to write relevant information about the Organization
in question.

![Organization Details](/images/support/org-details.png)

### Tag tickets
{: #tags}

To be able to capture metrics on which topics are most frequently asked about, when you start on a ticket,
add tags to it. For a list of current tags, what they mean, and how to add tags, see the [tags workflow](/handbook/support/workflows/support_workflows/tagging-tickets.html).


### After the first response
{: #first-response}

In most cases when you reply to a customer you expect a reply back. In this case the ticket should be
marked as `Pending`. If this ticket doesn't receive a reply within 7 days, you should follow up with
the customer. If this is your second response without a reply you can mark the ticket as solved at this
point, otherwise ask them if they still need help or have further questions.

When a feature request or the fix for a bug has been scheduled for a future release, you should let the
customer know about the version for which this has been scheduled and when that version is going to be
releases, e.g. June 22nd for 8.9, and add the `promised` tag to the ZenDesk ticket.

Sometimes a customer will send an email to ask for a response to an issue that was
already created on a public issue tracker. In such
cases, include the link to the given issue in the "GitLab Issue" box, go ahead and
reply from the issue tracker, but also follow-up through ZenDesk by providing a link
to your comment in the issue tracker. Providing the response to the customer is
what sets the "first response time" metric, and allows the tickets to be closed
when appropriate.

### When and how to escalate a ticket?
{: #when-escalate}

Do not hesitate to ask for help with a ticket, you can ask any of your colleagues to assist you. You can do this via
Slack initially by [@mentioning](https://get.slack.help/hc/en-us/articles/205240127-Using-mentions) their name and providing a link to the description with an overview of the issue.
If the person you know can help you the best (expert on a specific topic) is not available on
Slack, you can assign the ticket to them, add a comment summarizing the situation, and submit the
ticket as **open**. Especially if you do are not yet fully familiar with the particular topic of the issue,
don't spend more than 30 minutes on an issue before escalating it internally.

### When to mark a ticket as solved?
{: #when-solved}

A ticket can be marked as solved when you are certain that you were able to resolve the requester's
problem, or, as mentioned above, when many days go by without a reply from the requester. The exception
to this rule is in social media support channels that do not integrate well with ZenDesk such as Disqus,
the Forum, Stack Overflow, and others, where each comment creates a new ticket. In those cases, you can
close the ticket as soon as you have provided a response (and also close the ticket created by your own response).

### Clearing out Suspended Tickets
{: #clear-suspended}

In ZenDesk, various filters send a ticket straight to "suspended" status. This is mostly useful
to remove spam and it works quite well. However, it is possible that actual tickets
are accidentally routed to Suspended Tickets, so it is important to check the new Suspended Ticket queue
at least once a day. Doing this on a regular basis also keeps that queue manageable.

### Allowing teammates to adopt a ticket
{: #allow-others}

When you are viewing a ticket teammates see an eye icon on the left of the ticket in the Views Screen.

![Organization Details](/images/support/zd-eye-icon.png)

This implies that you're reading or working on the ticket so if your not going
to handle it make sure to close it by closing the tab at the upper section of the
screen that has the ticket's title.

If you see a ticket with this icon that either you feel you can add value to it,
or has been open for too long then please ask your teammate through Slack if he
or she is still working on it. The person's name appears by hovering over the,
ticket's title on the list view or by selecting the ticket and reading the
"Also on this ticket" section on the top left. Notice that if a general account
like GitLab Support is being used there is no name to refer to so you might want
to ask on the support and/or general chat channel with the ticket's link.

### Update agent signature
{: #agent-signature}

Your personal ZenDesk signature is shown at the end of every ticket response.
You can update this to include a personalized valediction like "Thanks" or "Best Regards" by following these steps.

* In Zendesk, click your user icon in the upper-right corner and select View Profile Page .
* Under Signature in the left sidebar, enter the signature text.

An example agent signature:

```
Thanks,

{{agent.name}}
GitLab, Inc.
```

### How to handle emails forwarded from others at GitLab

Every now and then, a GitLab team member will forward a support request from a customer, prospective customer, user, etc. These requests then appear as tickets from the team member, instead of from the original requestor. Always reply directly to the original requester, keeping the person who forwarded it in the cc. You will need to manually alter the "Requester" field of the ticket, by clicking on the "(change)" link next to the email address of the apparent requester in the ticket title.

## Digital Ocean account access

As part of onboarding SE team members will be given access to the GitLab Digital Ocean team account.
This can be used for testing and to reproduce customer problems. Please consider the following when using this account:

+ Do not destroy, stop, or modify droplets that you haven't created
+ Always include your name in the droplet hostname - e.g `user-ldap-testing-box`
+ Use resources sparingly and remove droplets that have served a purpose and are no longer in use
+ Do not create droplets unrelated to GitLab (personal projects)

## Receiving feedback
{: #feedback}

After 24 hours of marking the ticket as solved a survey is sent to our customers, where they can rate
the level of support they received. If a customer rates a ticket to which you were assigned as bad, an
email will be sent to you and the ZenDesk manager to notify you of the fact. When this happens, you should
let a Senior know about the problem and follow up with the customer to see if something you did can
be improved.

You will also receive a message if the feedback is positive, and it is encouraged to
celebrate those "wins" with the rest of the team through the #support or #thanks
chat channel. Read the positive feedback carefully, often it contains a question
or suggestion for improvement which should be followed up on.


## Customer Calls Best Practices

### Before a Call

After sending the WebEx Invite, go to the ticket and ask for confirmation. Having the customer confirmation will also help to detect errors on the scheduling process such as an incorrect timezone, date, etc.

Add the call with description and duration to the Support Team Calendar.

### During a Call

Once you started the call and the client connects, identify yourself. Example:

> Hi {customer name}, this is {agent name} from GitLab Support.

If you started the call and the client doesn't join, wait for a couple minutes. After 10 minutes of waiting
go to the ticket and send a reply to check if the customer is having either issues with the scheduled time
or connecting to the WebEx Platform.

If after another 10 minutes you don't get answer, go ahead and re-schedule.

If a call takes too long (> 1 hour), and/or if you're not making progress, discuss with the customer the need to re-schedule.

+ If you were having problems helping the customer, make sure to contact a teammate to join you on the re-scheduled call (Call Escalation)
+ If the customer had problems either with their setup, environment, or connectivity, remember him to solve them before the new
call when re-scheduling.

### After a Call

Update the ticket with a brief description of what was accomplished or not during the call making sure to point out the missing
information to solve the ticket.

## Customer Training

Support Engineers are regularly asked to provide customer training, and/or to provide answers to technical
questions from potential customers. The materials for the customer training should be kept up to date
where Solution Architects of the Customer Success team perform training through current services.
Importantly, requests for time in training should be done via the [internal Customer Success issue tracker](https://gitlab.com/gitlab-com/customer-success/issues) using the 'Training' label.
If you are receiving such a request via email or Slack, please move it to an issue to allow for wider participation
or easy escalation when needed.

## Keeping up to date with new GitLab versions

Since we ship a new release each month on the 22nd, and since we manage to fit _a lot_ of great new features and fixes into each release, it is sometimes difficult for the Support Team to keep up to date with key changes.

In general, it is the responsibility of each Support Engineer individually to read the release blog post, dig deeper where you need to or want to, and keep yourself up to date. However, to facilitate this further, we have a Pre-Release Call every third Thursday of the month (it is listed on the GitLab Support calendar). During the call, key parts of the product that are expanding rapidly or add more complexity than usual will be reviewed together by reading the draft release-post and inviting on team leads to walk the Support Engineers through major changes, e.g. in CI.  

## Team member is unavailable
{: #not-available}

### Vacation

You are encouraged to take as many vacations days as you need, as per our [handbook](/handbook). There
are, however, some things to consider when a member of the support team takes a vacation.

**On-call schedule must be covered**

Before leaving for vacation, 2 weeks before at the latest, you should coordinate with your colleagues
to see who can take over the days when you should be on-call. This can happen via an issue in our
[support issue tracker](https://gitlab.com/gitlab-com/support/issues) or via
a Hangout that you should schedule.
See the [on-call](https://about.gitlab.com/handbook/on-call/#swapping-on-call-duty) page for more information.

**Calendar Availability**

If your Calendly link is being given out to customers or interviewees to schedule
calls with you, you need to make sure that no one schedules a call with you on
the days you are away. See Calendly's instructions for handling this [here](https://help.calendly.com/hc/en-us/articles/223194148).
When you create an all-day event in Google Calendar, the
default behavior is to set you as **"Available"** for that day. This means that
if you create an all-day event to mark yourself off, and even after creating that
event if you change it to a **non-all-day-event** by giving it a time, people
will be able to schedule calls with you on that day. You have to create an event
that has a set time, from the time of creation, or change the event settings to
mark you as **"Unavailable"**. It is not a bad idea to double check your
availability on an **out-of-office** event after creating it.

**Rest of the team**

At any point in time at least half of the support team must be available to handle all our tasks, so
be sure to let everyone know about your plans as soon as you know something. This can be done in the
Availability Calendar. Vacation days are first come first served.

**Tickets assigned to you**

As a courtesy to other team members, please try to address all "Open" tickets (awaiting a response from the customer) in your queue.

When taking leave longer then 1 day, you should mark yourself as unavailable in Zendesk.
Do this at the end of your last work day this will ensure tickets flow correctly to other agents.

Marking yourself as unavailable in Zendesk:

1. Sign into [ZenDesk](https://gitlab.zendesk.com/agent).
1. Try to ensure any active tickets are in the **Pending** or **On-Hold** states and not **Open**.
2. View the [Out Of Office](https://gitlab.zendesk.com/agent/apps/out-of-office) app.
3. Toggle your agent status to "Unavailable".
   + Note: Only tick **"Unassign All Open Tickets"** if you have **Open** tickets that are still awaiting a response from the support team.
5. Click "Set to Unavailable"

### Illness

You should always take care of yourself and make sure you are healthy. If you need to take a sick day, let
your team members know. If there is an important ticket pending, ask one of your colleagues to help you if
you foresee that you will be unavailable for more than 1 day.

If you are on-call but ill, ask one of your colleagues to cover for you.

### Unforeseen events

If you need to take care of something urgent, there is no need to ask for permission. Just notify the team
via the #support channel in Slack. If you are on-call, ask one of your colleagues to
cover for you.
