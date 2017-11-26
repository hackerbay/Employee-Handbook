---
layout: markdown_page
title: "Accounting"
---

## Manual invoicing in Recurly for subscribers paying by bank transfer

* [New account](https://gitlab.recurly.com/accounts/new)

1. Account code: customer contact email address

1. Username: can be blank

1. Fill in First name and Last name of our contact

1. Fill in company

1. Fill in VAT field (if needed)

1. Tax exempt? - leave unchecked

1. Fill in the rest of the company information, and add company billing address to address information area

1. Press Create account

* Press “Add subscription”

* Select Plan Details and Quantity

* Billing Details -> +Edit

* Collection method: Manual

* Add PO number

* Terms: Net 30 (or 60 for exceptions)

* Terms and conditions copy and paste one of the following:

1. For non-EU clients: No VAT according to article 44 and 59 of the European VAT Directive

1. For EU clients: VAT shifted to recipient according to article 44 and 196 of the European VAT Directive

1. Dutch clients: leave blank

* Add the following information to the terms and conditions:

This order is subject to the [GitLab Terms](https://about.gitlab.com/terms/)
Payment via check is not possible
Please pay this invoice by bank transfer:
Bank: Rabobank, Croeselaan 18, 3500HG Utrecht, Utrecht, The Netherlands, +31302160000 SWIFT / BIC code: RABONL2U, Bank account number: 153952644, IBAN: NL48RABO0153952644

* Press Add subscription button

## Manual invoicing in Recurly for consultancy / development / training customers

* [New account](https://gitlab.recurly.com/accounts/new)

1. Account code: customer contact email address

1. Username: can be blank

1. Fill in First name and Last name of our contact

1. Fill in company

1. Fill in VAT field (if needed)

1. Tax exempt? - leave unchecked

1. Fill in the rest of the company information, and add company billing address to address information area

1. Press Create account

* Press “add charge” button

* Enter the unit amount and any other relevant details, then click the Add Charge button (it’s a good rule of thumb to include a description with the charge. The description will display with the line item on the customer’s invoice)

* “Digital product”

* “Collect Sales tax” checked

* Press “Create invoice”

* Back to the account, press “Generate invoice”

* Collection method: Manual

* Terms: Net 30 (or 60)

* Terms and conditions:

1. For non-EU clients: No VAT according to article 44 and 59 of the European VAT Directive

1. For EU clients: VAT shifted to recipient according to article 44 and 196 of the European VAT Directive

1. Dutch clients: leave blank

* Add the following information to the terms and conditions:

Payment via check is not possible
Please pay this invoice by bank transfer:
Bank: Rabobank, Croeselaan 18, 3500HG Utrecht, Utrecht, The Netherlands, +31302160000 SWIFT / BIC code: RABONL2U, Bank account number: 153952644, IBAN: NL48RABO0153952644

* Create draft sale in Twinfield

## Change customer from credit card payment to bank transfer payment

1. Customer account

1. Subscriptions -> More

1. Press Edit button

1. Billing -> + Edit

1. Choose “on next renewal”

1. Change to “manual invoice” and add invoice details

1. Press “Update subscription”

1. Invoice will be created on the date of the renewal

## EU VAT VIES check

Do the VIES check before sending an invoice to a EU client (not needed for Dutch clients) [VAT request](http://ec.europa.eu/taxation_customs/vies/vatRequest.html) print to PDF, email the resulting page to Sytse with the invoice.

GitLab.com VAT nr. is NL 137696735B02

GitLab B.V. VAT nr is NL 853740343B01

## Consolidated invoices

1. If a customer decides to commit both to a subscription and development work in one go, then we create a consolidated invoice immediately after the PO

* In case we worked extra for the development, we create new invoice with extra amount

* In case we worked less, we issue a credit invoice for the reminder

It is preferred to avoid both the above cases (extra work for us)

## Correcting an invoice for a customer who forgot to add VAT number when subscribing via Recurly

1. Check whether customer want the VAT number added

1. Perform the EU VAT VIES check

1. Recurly -> Accounts -> identify account -> invoice -> refund invoice -> uncheck Prorate -> Refund invoice

1. Update Billing info with VAT number

1. Charges and Credits -> Add charge

* Amount (per Unit): same as on original invoice

* Tax Type: Digital product

* Quantity: same as on original invoice

* Description: same as on original invoice

1. Add charge

1. Generate invoice -> Post invoice

1. Twinfield: create three draft sales, one for each invoice (original one but with line item price changed so that VAT checks out, credit one but with line item price changed so that VAT checks out, correct one)

## Crediting an old Recurly transaction (more than 1 Q old)

1. Assuming new invoicing dashboard

1. New invoice

1. Identify old Recurly invoice

1. Date is date of original invoice

1. Top text: in-depth explanation on the reason behind the credit invoice

1. Items just like in original invoice, but with negative amounts

1. Fill out the ICL details if needed (Services, date of new invoice)

1. Send PDF

1. Send the credit invoice to the customer (this is legally required)

## Crediting a transaction made in Recurly

1. [Invoice refunds](https://docs.recurly.com/invoices#invoice_refunds)

1. All refunds, credits, and subscription cancellations should have a note made in the Account Notes section starting with ISO 8601 date format (yyyy/mm/dd).

## Customer accidentally created a new subscription instead of updating the old one, both in the same account

1. Customer account -> find new subscription -> More

1. “Cancel Subscription”, full refund

1. Find original subscription -> More

1. Change to correct number of user packs

1. Press “Update subscription"

1. Inform customer of the changes

## Using Recurly to invoice hourly clients (or special order) by credit card

* For an existing client you can skip the first two steps

* We create an account for the customer on Recurly

* We email them a link to their hosted account management page to enter billing information

* We open the customer’s account and click the Add Charge button in the Charges and Credits section

* Enter the unit amount and any other relevant details, then click the Add Charge button (it’s a good rule of thumb to include a description with the charge. The description will display with the line item on the customer’s invoice)

* Keep the “Collect Sales Tax” button checked; Type: Digital Product

* This will create an uninvoiced charge on the customer’s account. By default, this charge will be automatically rolled into the customer’s next subscription renewal invoice. If you’d like to collect this charge immediately, click the Generate Invoice button on the customer’s main account page

* Customer notes:

1. Non-EU clients: No VAT according to article 44 and 59 of the European VAT Directive

1. For EU clients: VAT shifted to recipient according to article 44 and 196 of the European VAT Directive

1. Dutch clients: leave blank

* Review the invoice details and click the Post Invoice button

* Once the invoice is posted, Recurly will automatically collect on the invoice during our next automatic bill run (typically at the top of every hour). You will see the account’s balance go back to $0.00 when this charge is successfully processed

## Customer wants to update their Recurly account or billing information

1. Each Recurly account has a hosted account page where they can manage their information. The link is in Recurly -> accounts -> account name -> Hosted pages information.

1. Use the Hosted Account Management URL to go directly to the page without logging in.

You can find additional documentation [here](https://docs.recurly.com/hosted-account-management).

## Email templates customization
In the Recurly email templates for "New Subscription", "Payment Confirmation" and "Payment Declined" we added the following:
This subscription is subject to the [GitLab Subscription Terms](http://www.gitlab.com/terms/#subscription)

* For companies outside the EU: No VAT according to article 44 and 59 of the European VAT Directive. 

* For companies within the EU where no VAT is invoiced: VAT shifted to recipient according to article 44 and 196 of the European VAT Directive.

### Coupon code for special pricing

1. Go to [new coupons](https://gitlab.recurly.com/coupons/new)

1. Coupon name: organization name (e.g. Penn State)

1. Coupon code: half-random, recognizable as custom (e.g. pennstate123abc)

1. Discount: percentage

1. Lifespan: Forever (default)

1. Limit to specific plans: yes

1. Max Redemptions: 1

1. Redeem by Date: in 60 days

1. Include the coupon code in the quote