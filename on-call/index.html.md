---
layout: markdown_page
title: On-Call
---

- [Production On-Call Log](https://docs.google.com/document/d/1nWDqjzBwzYecn9Dcl4hy1s4MLng_uMq-8yGRMxtgK6M/edit#)

## On this page
{:.no_toc}

- TOC
{:toc}

----

We use [PagerDuty](http://gitlab.pagerduty.com/) to
set the on-call schedules, and to route notifications to the correct on-call hero. There is one rotation for Production related emergencies (i.e. GitLab.com downtime), and another for Customer Emergencies. These each have their own schedules, on-call heroes, and escalation policies.


## Expectations for On-Call

- If you are on call, then you are expected to be available and ready to respond to PagerDuty pings as soon as possible, but certainly within any response times set by our [Service Level Agreements](https://about.gitlab.com/handbook/support/#sla) in the case of Customer Emergencies. This may require bringing a laptop and reliable internet connection with you if you have plans outside of your work space while being on call, as an example.
- We take on-call seriously. There are escalation policies in place so that if a first responder does not respond fast enough another team member or members is/are alerted. Such policies are essentially expected to never be triggered, but they cover extreme and unforeseeable circumstances.
- Triage the [infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/issues), applying appropriate labels and reaching out others when needed, so the rest of the team can focus on the WoW.
- Act as an umbrella to avoid team randomization.
- Keep an eye on monitoring and logging dashboards in order to detect and react faster to incidents, or even preventing them.
- Provide support to the release managers in the release process.
- Automate as much as possible to get rid of toil, create new alerts and tools to enhance the on-call experience.
- As noted in the [main handbook](https://about.gitlab.com/handbook/paid-time-off), after being on call take time off. Being available for issues and outages will wear you off even if you had no pages, and resting is critical for proper functioning. Just let your team know.
- More detailed descriptions can be found [here](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/lead-away.md).

### Swapping On-Call Duty

To swap on-call duty with a fellow on-call hero:

- create an issue on the [organization issue tracker](https://gitlab.com/gitlab-com/organization/issues/new)
to announce for what block of duty you need to make a swap. Do this as far as possible in advance,
but certainly no later than 2 weeks before the swap needs to be made. @mention your colleagues.
- once a replacement has been found, input this as an override on the main schedule in PagerDuty.
This is done by clicking on the relevant block of time in PagerDuty, selecting "override" and
filling in the name of the person you swapped with. Also see [this article](https://support.pagerduty.com/hc/en-us/articles/202830170-Creating-and-Deleting-Overrides) for reference.

## Customer Emergency On-Call Rotation

- We do 7 days of 8 hour shifts in a follow-the-sun style, based on your location.
- After 10 minutes, if the alert has not been acknowledged, _everyone_ on the customer on-call rotation is alerted. After a further 5 minutes, management is alerted.
- You can view the [schedule](https://gitlab.pagerduty.com/schedules#PIQ317K) and the [escalation policy](https://gitlab.pagerduty.com/escalation_policies#PKV6GCH) on PagerDuty.
- After each shift, _if_ there was an alert / incident, the on call person will send a hand off email to the next on call explaining what happened and what's ongoing, pointing at the right issues with the progress.


## Production Team On-Call Rotation

- We do 7 days of 12 hours shifts in a follow-the-sun style, based on your location.
- After 15 minutes, if the alert has not been acknowledged, the person who was on-call in the previous 12 hrs is alerted. After a further 15 minutes, management is alerted.
- You can view the [primary schedule](https://gitlab.pagerduty.com/schedules/PQ9W7ID) and the [secondary schedule](https://gitlab.pagerduty.com/schedules/P23P5AE) as well as the [escalation policy](https://gitlab.pagerduty.com/escalation_policies#P7IG7DS) on PagerDuty.
- After each shift the on call person will send a hand off email to the next on call explaining what happened and what's ongoing, pointing at the right issues with the progress.
- If nothing happened, consider sending an email to just let the next on-call hero be aware that nothing has happened.
- We track metrics on uptime first, then on time to fix (TTF). We do so to understand where the pain is, and how much time we are investing in fixing a problem. We use those metrics to drive automation priorities.
- When being on call prioritize work that will make the on call better (that includes building projects, systems, adding metrics, removing noisy alerts). We strive to have nothing to do when on call and to have meaningful alerts and pages. The only way that this will happen is by investing time in automating ourselves out a job.
- The main expectation when being on call is to triage the urgency of a page: if GitLab.com is down look for the right [runbook](https://dev.gitlab.org/cookbooks/runbooks) and do your best to bring it back up, but If you don't know what to do use your phone to call someone to help out.

### Shadow On-Call

We have a [shadow schedule](https://gitlab.pagerduty.com/schedules#PPKR403) that
will alert at the same time as the primary on-call. This is helpful for those
occasions where one or more Developers or others who are not normally on-call
want to be or need to be on-call as part of their current assignment.

Due to PagerDuty limitations, it is impossible to set it to only overlap with
one person. As such, remember to manually change it or remove it from the
escalation policy when you don't want  to be using it. This is irritating, but
not the end of the world.


### How to page current production on-call

From Slack you can page by using the slash pd command, like so: `/pd message for the on call`

This will trigger high urgency notification rules and escalates as needed.

## Adding and removing people from the roster

In principle, it is straightforward to add or remove people from the on-call schedules, through the same "schedule editing" links provided above for setting overrides. However, **do not** change the timezone setting (located in the upper left corner of the image below) unless you absolutely most certainly intend to. As indicated in the image below, when editing a schedule (adding, removing, changing time blocks, etc.), make sure you keep the timezone setting in the upper left corner constant. If you change the timezone setting, PagerDuty will _not_ move the time 'blocks' for on-call duty, but instead it will assume that you meant to keep the selected time blocks (e.g. "11am to 7pm") in the _new_ timezone. As a result, your new schedule may become disjointed from the old ones (old = the schedule as set _before_ the "change on this date" selection), and gaps may appear in the schedule.

![](/handbook/on-call/changing_pagerduty.png)
