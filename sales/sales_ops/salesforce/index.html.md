---
layout: markdown_page
title: "SalesForce"
---

### Standard Object Definitions

#### Lead

A lead is a prospect who has yet to be qualified. Lead may have expressed interest by requesting contact, starting a trial, attending a webinar or trade show, or registering on GitLab.com or our customer portal. Leads are typically followed up by our Business Development Reps (BDR) or Account Executives. During this initial qualification process, a BDR will uncover certain details that will determine whether the prospect is qualified. For more information on the BDR Qualification process, [click here](https://about.gitlab.com/handbook/marketing/business-development/#qualifying). Once qualified, the lead is converted into an Account, Contact, and Opportunity.

#### Account

An account can either be a prospect who was qualified by a BDR or Account Executive, an existing customer, or a partner. Accounts will contain all company information, including billing and shipping address, company phone, website, support package, industry, employee count, and annual revenue. An account will be the parent record for associated contacts, opportunities, subscriptions, invoices, and payments.

#### Contact

A contact is a person associated to an account record. Information contained in the contact record include name, mailing address, title, role, phone, and email. An account can have many contacts associated to it. Contacts can be added to opportunities via [Contact Roles](https://help.salesforce.com/articleView?id=000005632&type=1&language=en_US).

#### Opportunity

An opportunity is created when a prospect has expressed interest in GitLab. The opportunity record includes information regarding close dates, contract value, and type. An opportunity will be in a certain stage, depending on where it is in the sales cycle. For more information on stages, click [here](https://about.gitlab.com/handbook/sales/#opportunity-stages).

#### Tasks and Events

Tasks and events are used when logging calls and meetings into Salesforce. Collectively called "activities", these records are meant to track interactions with customers and prospects. For example, you might create a task after you've attempted to call a prospect. You may also want to create a task as a reminder to complete a certain task, such as call a prospect or send an email. Tasks can also be created by external systems such as Marketo or Outreach when emails are sent to leads or contacts. External resources: [Difference Between a Task and an Event](https://success.salesforce.com/answers?id=90630000000gvEbAAI), [SFDC Task Documentation](https://help.salesforce.com/articleView?id=activities.htm&r=https%3A%2F%2Fwww.google.com.ph%2F&type=0)

### Non-Standard Object Definitions

#### [Account Plan](https://about.gitlab.com/handbook/sales/sales_ops/salesforce/account-plan/)

An account plan is a custom object that is used to track any strategies and tactics against a large or strategic account. In this object, you will work with your regional director to define a strategy against a target account. In this object, you will capture bookings goals, business and technical challeges you're looking to solve, internal team members, external contacts, and other relevant information related to the account plan.

### External Resources
* [Salesforce Success Community](https://success.salesforce.com/)
* [Salesforce Help](https://help.salesforce.com/home)
* [Salesforce Glossary](https://help.salesforce.com/articleView?id=glossary.htm&type=0)

#### Commonly Asked Questions
* [How to Create a Report](https://help.salesforce.com/articleView?id=reports_builder_create.htm&type=0)
* [How to Create a List View](https://help.salesforce.com/articleView?id=customviews.htm&type=0&language=en_US&release=208.6)