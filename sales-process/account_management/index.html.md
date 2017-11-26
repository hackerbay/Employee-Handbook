---
layout: markdown_page
title: "Sales Process > Account Management"
---

## Touching base with standard subscribers

## Preparing renewal

## What is an order?

1. A Purchase Order (PO) issued by the company

1. A signed quote (the quote that we send)

1. An e-mail agreement (“we accept the quote/subscription/etc”) or any other written statement

## Development work management

Do NOT invoice before feature/work is completed.

* Feature is requested by customer

* Sales creates issue in issue tracker that links to the email (tags: company name, feature, estimate) and, if needed, mentions in agenda. Issue is assigned to sales milestone 

* Dev makes estimate/gives feedback

1. Estimate: between x and y hours (if it takes much time to do an estimate and we doubt if the customer will order)

1. Quote: x number of hours (in all other cases)

* Sales communicates estimate to customer

* Repeat 3 and 4 in case of a range estimate

* If customer agrees with estimate and feedback, then:

1. Add estimate and order to the hourly tab of the Sales sheet

1. Sales removes estimate label and adds promised label

1. Sales adds comment on milestone and context of developer agreeing on the milestone, changes milestone in the issue

1. Adds the issue name and link to the feature in the deal

* If customer does not commit in a reasonable time, issue is marked as closed and sales follows up through the deal

* If feature will not be done, sales marks issue as closed

* Once feature is delivered, adds number of hours spent in the deal, sales announces customer, closes feature with link to email

* Sales adds the real number of hours spent to the sales sheet

* Sales invoices customer ([credit card](source/handbook/sales-process/accounting) or bank) for the quoted number of hours

* Deal is marked won

* Implicit handover between sales and finance is sending the invoice (Sytse)

## Consultancy work management

1. Customer contacts sales for consultancy work

1. Sales sends email to support@ with details and time estimate

1. Support will OTB (OK to book) or ask for more information

1. If more information is needed sales will ask it and add to the Zendesk ticket

1. If OTB and customer agrees with the estimate, sales will ask the customer to contact support@ for booking time and adds to the sales sheet 'Hourly' as quoted

1. After ordering, sales marks deal as won and amends sales sheet

1. If, during the call, the time allocated on the quote is exceeded, the Support Engineer will inform the client that they are going overtime, and that all overtime will be invoiced to the client at normal consultancy rate

1. If an unforeseen GitLab bug needs to be fixed in order to address the consultancy request, the Support Engineer will inform the client that GitLab B.V. will make the fix, and that the additional hours spent will be invoiced to the client at normal consultancy rate

1. If the work is finished or the client decides to stop the consultancy process, support logs the hours spent in the ‘Hourly’ sales sheet, column “Realized” and informs sales via email or Highrise

1. Support notifies customer via Zendesk that Sales will be in touch with them

1. Sales creates invoice corresponding to the number of hours in the “Realized” column

## Handover from sales to support for subscription clients

1. Sales includes a link to the relevant Highrise deal
1. Support looks in the highrise deal, if the conversation is too long they leave a note in Highrise asking for a summary

## Support for potential customers

1. Sales hears about a bug / issue the potential customer is having and decides 
that GitLab should try to solve it in the interest of winning the deal. At that point:
   - Sales asks the customer to email support regarding their issue; OR
   - Sales forwards the issue from the customer to support, and in doing so also 
puts the sales team in the cc to avoid creating duplicate tickets for the Support Team.

## Creating an Issue for feature requests

1. Create an issue on the [public issue tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues) and mention someone (Dimitriy, Sytse, Job).
1. Do not mention customer name but confirm if large, medium, or small, and include URL to Saleforce account.

## Federal agency templates and certificates 

1. GitLab does not have VPAT or 508 certificates
