---
layout: markdown_page
title: "Sales Operations"
---

---
## On this page
{:.no_toc}

- TOC
{:toc}

---

## Sales Operations Page

Overview of sales tech stack along with other tools that sales interacts with; tips, tricks, and how to's for the various applications; and external resources that will help user be more productive with our business systems.

### Overview of Tech Stack

The following is a brief overview of the different tools that make up the tech stack (as well as tools managed by other departments, but used by the Sales team).

#### [Salesforce](https://about.gitlab.com/handbook/sales/sales_ops/salesforce)

Salesforce is our CRM of record. It integrates with all of the other applications in our business tech stack. Salesforce stores prospect, customer, and partner information. This includes contact information, products purchased, bookings, support tickets, and invoices, among other information.

#### Marketo

Marketo is our marketing automation platform managed by our Marketing Ops team. Anyone who signs up for a trial, requests contact from GitLab, attends a webinar or trade show, or engages in any other marketing activity, will end up in Marketo. These prospects will receive scores based on their level of engagement and these scores will be used by the Business Developement Representatives and Account Executives to prioritize which prospects to follow up with. Marketo is also our primary tool for delivering marketing communciation to prospects and customers. You can read more about the Marketo and the other tools in the Marketing stack [here](https://about.gitlab.com/handbook/marketing/lead-generation/marketing-operations/).

#### DiscoverOrg

DiscoverOrg provides our Sales Development Representatives and Account Executives with access to hundreds of thousands of prospects and their contact information, company information, tech stack, revenue, and other relevant data. Individual records or bulk exports can imported into Salesforce using extensive search criteria such as job function, title, industry, location, tech stack, employee count, and company revenue.

#### Clearbit

Clearbit is a data enrichment tool that will be used to fill in important information for new leads created in Salesforce. This information could include address, phone number, industry, IT employees and other important values when assessing both the quality of the lead as well as routing. The technology uses proprietary  logic to match prospects to companies in their extensive database.

#### [LeanData](https://about.gitlab.com/handbook/sales/sales_ops/leandata)

When a lead is created in Salesforce, LeanData will be the tool that routes it to the appropriate user. Routing rules include sales segmentation, region, lead source, and owned accounts. For example, if a lead from a named account is created, it will be routed directly to the owner of the named account. Also, LeanData provide cross-object visibility between leads and accounts and contacts. When in an account record, a user can view "matched" leads by company name, email domain, and other criteria.

#### Outreach.io

Outreach.io is a tool used to automate emails in the form of sequences. Users can track open rates, click through rates, response rates for various templates and update sequences based on these metrics.

#### Sertifi

Sertifi is used when a quote or other document requiring signature needs to be delivered to a prospect.

#### Zuora

Zuora is our subscription management and billing system, primarily managed by our Finance team. A quote object within Salesforce is created with a specific configuration, and an order form (PDF) is be generated. Once the order form is signed, the Quote in Salesforce is converted to a Subscription in Zuora and the invoice is delivered or payment is applied if the customer provides their credit card details.

#### Zendesk

Customer support tickets are managed through Zendesk and can be visible in the Lead, Account, or Opportunity object in Salesforce in the form of a Visualforce page. This provides visibility for non-Zendesk users into the support tickets created by their prospects and customers. For more information on this tool, you can visit the Support page [here](/handbook/support).
