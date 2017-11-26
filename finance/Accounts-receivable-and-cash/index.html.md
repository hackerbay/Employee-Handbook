---
layout: markdown_page
title: "Accounts Receivable and Cash"
---

## On this page
{:.no_toc}

- TOC
{:toc}


## Accounts Receivable
<a name="ar"></a>

### Invoicing

1. Log in to Zuora and Salesforce.
1. In Salesforce, click the "+" icon and select "Z-Quotes".
1. Subscriptions to be invoiced are sorted by date. Choose a subscription from today's date and proceed.
1. Still in Salesforce, check the customer account for a current PO number under the notes and attachments.
1. Then in Zuora, search for the corresponding customer subscription and open the record.
1. Check to see if the PO from the file in Salesforce matches that of Zuora. If not, update the record in Zuora with the latest PO number.
1. Verify that the "Bill to" and "Sold to" contacts listed in the Zuora customer record match the related record in Salesforce. If not, update Zuora.
1. Verify that the payment terms and method listed in Zuora match the related record in Salesforce. If not, update Zuora.
1. In Zuora, scroll down to transactions and click "Create Bill Run."
1. It is important to find the subscription start date in Salesforce and enter it in the "Target Date for this bill run" field in Zuora. The invoice date should be today's date.
1. Once these dates agree, click "Create Bill Run."
1. On the following screen, select the bill run that was just created (the bill run files begin with BR- followed by a set of numbers).
1. Scroll down and click on the invoice that was just generated. The PDF file will be at the bottom of the page.
1. Open the PDF file and review every field of the invoice for accuracy.
1. Once the review is complete, close the invoice and click “Post Invoice.”
1. Proceed to bill the remaining subscriptions.

At this point the invoicing process is complete. Now, continue on to the Cash Receipt posting process for those invoices that were paid by credit card.

## Cash Receipt
<a name="cash-receipt"></a>

### Credit card customer

Follow this procedure if the customer paid by credit card.
You may recall from the invoicing process that there was still a balance due when saving the invoice.  The following steps will record the payment and remove the balance due.

1. Login to Stripe dashboard and click on Payments under Transactions (left hand side). You will see a listing of the latest Stripe transactions listed by amount, Recurly transaction, name, date, and time. There is also an option to filter the report by clicking on XXX at the top left. Click on XXX to export to excel. This will give you a workbook area and also a breakdown of the fees which we will work on later.
1. In NetSuite, click on the "Transactions" tab on the left.
    * Click on the orange "OPEN INVOICES " tab. This will bring up all open invoices listed by date, invoice #, customer, etc.
1. Match invoice #s  between the Stripe dashboard and NetSuite. If you click on a transaction in the Stripe dashboard, it will take you to a screen that shows more detail, including the invoice # being paid. You can work your way from the bottom up.
1. In NetSuite, click "Receive Payment" on the matched payment and invoice.
1.  Receiving the payment
    * Enter the payment date, which is the payment date from Stripe dashboard.
    * Payment method = Credit Card.
    * Reference no. = "Recurly Transaction ID:" found under Metadata in Stripe dashboard.
    * Deposit to = Stripe.
    * NetSuite will auto-fill the payment amount with the entire balance due. No need to change this unless the payment amount from Stripe is different.
    * Click on "Save and Close".
    * Repeat the above for all the remaining invoices that were paid by credit card.

1. Post a journal entry to record Stripe Fees.
    * In NetSuite, click on the "+" sign. Under "Other", select "Journal Entry".
    * It is okay to leave the journal date as long as it is within the month the fees were incurred. If not, change it to the last day of the month.
    * NetSuite will auto fill the journal number. Do not change.
    * Account #1 Entry
      * Fill the "Account #1" entry with "Credit Card Transaction fees".
      * Fill the "Debits" entry with the value from the Stripe report that was exported. The value will be the sum of "Column I" in the Stripe report, which is the fee amount. Be sure to only sum the rows which you just posted payments for.
      * Leave the "Credits" entry empty.
      * Fill the "Description" entry with "To record credit card transaction fees for period (enter the date range for the transactions posted)".
      * Leave the "Name" entry empty.
      * Fill the "Class" entry with "Sales".
    * Account #2 Entry
      * Fill the "Account #2" entry with "Stripe".
      * Leave the "Debits" entry empty.
      * The "Credits" entry will autofill. This should be the same amount as the "Debits" entry for Account #1.
      * The "Description" entry will autofill. This should be the same as the "Description" entry for Account #1.
      * Leave the "Name" entry blank.
      * Leave the "Class" entry blank.
      * Click "Save".

This transaction transfers the payment obligation from the customer to Stripe.  The payment obligation from Stripe is removed when Stripe transfers  the funds to GitLab's bank account.

### Posting a payment from Stripe when a transfer is received from Stripe.

Post a journal entry:
1. Fill the "Journal Date" with the date that payment was received in the bank.
1. Fill the "Credit Account" with Stripe.
1. Fill the "Debit Account" with "Comerica Checking - GitLab Inc."
1. Leave "Name" blank.
1. Leave "Class" blank.
1. Fill the "Description" with "To record Stripe transfer (date of transfer)".
1. Click "Save".


### Posting a payment from a “bank customer”

In Netsuite:
1. Click on the “+” sign.
1. Click on “Receive Payment” under Customers.
1. Fill the "Payment Date" with the date payment was received.
1. Fill the "Payment Method" choose from the dropdown menu.
1. Fill the "Reference No." with the check # or bank reference # from incoming wire.
1. Fill the "Deposit to" with "Comerica Checking".
1. Fill the "Amount Received" with the amount received from the incoming wire.

## Refunds

### How to initiate a refund request

1. Send an e-mail to ar@gitlab.com with the following information (if applicable)
   * Customer Account Name
   * Subscription number
   * Invoice number
   * Reason for refund

### How to process a refund in Zuora

1. A refund request has been received by e-mail or refund opportunity in SFDC.
1. Log in to Zuora.
1. Search for the invoice that needs to be refunded.
1. On the invoice screen, scroll down to "Transaction(s) associated to this Invoice" and click on the payment associated to the invoice to be refunded.
1. On the payment screen, click on more and click on "Refund this payment."
1. Create the refund.
1. An auto-generated e-mail will be sent to the customer that the refund has been processed.
1. The payment will be reversed on the invoice and there will be a balance due.
1. Cancel the subscription in Zuora using the first day of the service period to be refunded.
1. Create a bill run for the subscription cancellation.
1. Post the invoice and transfer the credit balance.
1. Apply the credit balance to the original invoice.
1. Request a refund opportunity to be created in Salesforce if it hasn't been created already.
1. Enter in the refund invoice number and the date of the refund on the refund opportunity.

### How to process a partial refund in Stripe

1. Log in to Stripe.
1. Type in the cardholder’s name in the search field at the top of the screen.
1. Click on the original charge that will be refunded.
1. Click on the refund button.
1. Enter in the amount to refund.
1. Enter in the reason code.
1. In the description field, enter the reason for the refund and include the invoice that was created in Zuora for the refunded amount.
1. Click on refund.
1. Go back to Zuora.
1. Put the customer account in silent mode under "Communication Profile." 
1. Post the invoice draft.
1. Transfer to credit balance.
   * Accounting Code: Stripe - Inc
1. Put the customer account back into Default/B2B under "Communication Profile."
1. Verify that the balance due is $0.00 on the refund invoice that was created.
1. Manually e-mail the customer, do not use Zuora to create the email as you cannot update the contents. Include a screenshot of the partial refund from Stripe and attach a copy of the refund invoice.


