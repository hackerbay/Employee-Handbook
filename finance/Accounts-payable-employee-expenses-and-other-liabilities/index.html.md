---
layout: markdown_page
title: "Accounts Payable, Employee Expenses, and Other Liabilities"
---

## On this page
{:.no_toc}

- TOC
{:toc}


### NetSuite

Invoices will arrive by email to ap@gitlab.com.

1. Forward email to the appropriate GitLab team member for approval.
1. Create a PDF copy of the email containing the approval response.
1. File the invoice and approval in the "Invoices" folder in Google Drive.
1. Enter the invoice in NetSuite. Step by step instructions for this process are below.

#### Entering a Bill (invoice) in NetSuite

1. On the home page, click the “+” icon near the global search bar at the top of the screen and select “Bill."
1. Select the appropriate vendor record. If adding a new vendor, follow the bullets below before proceeding, otherwise skip to step 3.
    * Enter the company name, email address, applicable subsidiary, physical address, payment terms, primary currency, and Tax ID. (Note that the address field is located under the "Address" tab, while the Tax ID, primary currency, and payment terms fields are located under the "Financial" tab)
    * Enter the banking information in the "Comments" field then click “Save.”
    * Go to the "+" icon at the top of the vendor record and select "Bill" from the dropdown box.
1. Enter Bill date. The due date should auto-fill based on payment terms entered during vendor setup. If not, select the correct due date and update the vendor record after the bill has been entered and saved.
1. Enter Bill number.
1. Go to the "Expense and Items" tab below to enter the expense details.
1. Select appropriate GL-account under the "Account" dropdown box. (Be sure to check whether the invoice represents a prepaid expense, fixed asset, etc.)
1. Enter Bill amount.
1. Select tax code, if applicable.
1. Enter department. (This must be entered if the account you selected in step 6 is an expense account)
1. Add attachments: Go to the "Communication" tab and find the "Files" subtab.
1. Click "New File.” A new window will appear, allowing you to select the file you wish to attach.
1. In the new window, select the "Attachments Received" folder in the dropdown box, then click "Choose File" to attach both a copy of the vendor bill and email approval. (The supporting email approval must be attached along with a copy of the invoice)
1. Click "Save.”
1. In Google Drive, file invoice in the “Unpaid” folder.

### Processing payment for invoices

1. Upon receipt of vendor invoices:
    * File a .pdf copy of the invoice to dropbox\For Approval.
    * Notify manager of new invoices to be approved by forwarding the email from the vendor.
    * Invoices are to be approved based on signed agreements, contract terms, and or purchase orders.
    * After review, manager to reply to email with “Approved”. An audit trail is required and this email will serve this purpose.
1. On approval, move the invoice from dropbox\For Approval to dropbox\Inbox
1. Post the invoice through accounting system. Before paying any vendor (for Inc. only), be sure there is a W-9 on file for them.
1. On a daily basis, generate an AP aging summary from the accounting system and identify invoices to be paid.
1. Initiate payment(s) through the bank (Comerica/Rabobank) and notify management that there is a pending payment.  Include a summary of invoices being paid.
1. Verify the payment has cleared the bank.
1. Upon verified payment of the invoice move the .pdf copy of the invoice from dropbox\Inbox to folder inbox\”vendor name”.
1. Post the payment through the accounting system.

### Processing Expensify Reports 

1. In Expensify, go to the “Reports” tab.
1. Filter the listed reports and narrow the results to reports that are marked as “Reimbursed.”
1. Click the checkbox next to each report that you wish to export to NetSuite.
1. Once the reports have been selected, go to the “Export to” dropdown menu near the top of the page and click “NetSuite.”
1. A box will appear showing the real-time status of the export. The process is complete once this box confirms a successful export. If you receive an error message, see the information below and follow the remaining steps.
    * Unsuccessful exports typically result from an error related to NetSuite records. Each Expensify user must have a corresponding NetSuite Employee record and Vendor record.
    * Check NetSuite to verify if the employee in question has both a Vendor and Employee record.
    * If the records exist, add the employee’s email address to both records. In order for the export to work, this must be the same email address that is assigned to the employee within Expensify.
    * If the records do not exist, create both an Employee and Vendor record in NetSuite, complete with email addresses. Expensify uses the employee email address when mapping its records to that of NetSuite. The export will not work without proper alignment of email addresses in the NetSuite and Expensify records.

### Recording Employee Stock Option Expense

Employee stock options are recorded on a calendar quarterly basis. The puropse of this entry is to record the expense and allocate it between the appropriate departments.

1. Request a copy of the eShares "Equity Incentive Plan Grant Date" report from the CFO (the report should be in CSV/Excel format).
1. We will focus on the Expense Summary and Date tabs
1. On the Expense Summary tab, click on the journal entry amount to see column and tabs being referenced in the formula. 
    * This should be column AX of the Date tab, and this column will be used to allocate the total expense between departments.
1. Sort the columns on the Date tab and delete all rows with a zero balance 
1. Add a column to the Date tab with department information that corresponds to the employees referenced in column B (department information can be found in NetSuite).
1. Create a pivot table using the data from column AX and the department column created in the previous step.
    * The pivot table should provide the amount of stock option expense attributable to each department.
1. Check that the total amount of the pivot table matches the amount on the Expense Summary tab.
1. Proceed to NetSuite to create a journal entry that matches the Expense Summary tab.
1. Date the journal entry using the last day of the quarter being closed. 
1. The debit side of the entry uses GL "6077 Stock Compensation Expense" for all departments other than Cost of Sales which uses GL "5090 Stock Compensation Cost of Sales."
1. Be sure to fill in the Department attribute when adding lines to the journal entry.
1. The credit side of the entry only needs one line and uses GL "3015 Additional Paid in Capital- Stock Options"
1. Save the report used to calculate the journal entry and attach it to the entry within NetSuite.
1. Click Save and the entry is complete.

