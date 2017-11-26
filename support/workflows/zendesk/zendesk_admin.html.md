---
layout: markdown_page
title: Zendesk Admin
category: Zendesk
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Adding / Removing Agents in Zendesk

To add or remove "full" agents to our Zendesk account, contact Zendesk support through the email address contained in the Support vault on 1Password titled "Zendesk Account Manager". This makes sure that the request is routed more quickly than if it is just sent in via their generic support address. Since we are on an annual contract, changes typically require a purchase order to be signed by the [VP of Engineering](/jobs/vp-of-engineering), but the change request can be initiated by any current "full" agent.

## Zendesk settings

### Service Level Agreements set as Business Rules

Within Zendesk, the SLAs are set as follows. Under Business Rules in the Admin console,
Service Level Agreements are defined. Currently only one is defined, with different response times
required depending on the _priority_  of the ticket which can be Urgent, High, Normal, or Low.

Emergency tickets (SLA category 1 per the list above) are tagged as "Urgent" using a 30 minute max response time setting.

SLA category 2 items are tagged as either High or Normal priority.

- High with a max response time setting of 8 business hours: security disclosures and subscribers.
- Normal with a max response time setting of 12 business hours: general support questions via the Zendesk web form and support@ address.

An email is sent to everyone in the support team when an SLA breach is imminent, see
the [automation in Zendesk](https://gitlab.Zendesk.com/agent/admin/automations/edit/80833987).

Within Zendesk, currently we do _not_ have an SLA assigned (and no automated warnings)
to any tickets from channels in category 3 and 4, but we do track response times.
