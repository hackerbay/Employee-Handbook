---
layout: markdown_page
title: "Sales Handbook Standard Operating Procedures"
---

---
## On this page
{:.no_toc}

- TOC
{:toc}

---

## Sales Standard Operating Procedures Purpose

Processes for Sales.

### Adding Leads via Discover.org

* GiLab uses a 3rd party service to identify potential leads to prospect into and drive demand for GitLab Enterprise Edition and GitLab Products.
* For an account/lead you own, you may request Sales Operations to upload any new contacts from Discover.org.  The request process is:
  * Within the lead/account use the chatter function to make the request and tag Francis Aquino (Dir. Sales Operations).  Example, "Request for contacts to be added via Discover.org"
  * Once the contacts have been uploaded, Sales Operations will respond via the same chatter message confirming the data upload has been done.
  * Turnaround time for each request will be 2 business days or less.  Sales Operations strives to respond to each request within the same business day, if at all possible.
* Before making a request for more contacts, please make sure you have a plan and time set aside to prospect to these new leads.  A plan means:
  * Messaging targeted to the account - based on vertical, competition and/or use of CE.
  * Email templates created that you would like to send
  * Time set aside to execute on your outbound plan

### Processing Orders

#### Step 1 - New Account

1. Click on the Accounts tab
1. Click on New button to Create Account
1. Select either Standard or Channel record Type. Each record type will have a different Account layout based on our engagement.
1. Standard Record Type should be used for all non-reseller partner accounts.
1. Channel Record Type should be used for all reseller partner accounts.
1. Create Account Screen – Enter all mandatory fields and click on Save – Account is created


#### Step 2 - Contacts

1. Create Contacts, by clicking on the new contact button
1. Make sure to add in the address for any contacts associated with the quote (Bill To and Sold To)

#### Step 3 -  Opportunity

1. Create Opportunity by navigating to the Opportunity Related list and click on New button
1. Select the Opportunity Record Type. Like Accounts, the options are Standard and Channel.
1. Standard should be selected when engaged in a Sales opportunity.
1. Channel should be selected when engaged in a Reseller opportunity (attempting to sign a reseller partner in a new territory, not Sales opportunities where resellers are involved).
1. Enter all the required fields based on your business process and click on Save Button

#### Step 4 - ZQuotes – New QUOTE

This is the process to create a quote. If you want to clone an existing quote, please see the Cloning an Existing Quote section.

1. Click on New Quote button within the opportunity
1. Enter all details and click on Next and select products to complete the Quote creation process
1. All the fields marked in red are mandatory fields, below are fields description
1. Valid Date – Date until when Quote is valid; This is auto set to 30 days from today’s date
1. Quote Template – click on the button to select the Quote template
1. Bill To contact  - Click on the vlookup button to enter the Bill To contact information. This will bring up a pop-up window that will list all the contact that were created during Step 2 of the process. Bill To person would be the contact to whom the bill will be sent
1. Sold To Contact - Click on the vlookup button to enter the Sold To contact information. This will bring up a pop-up window that will list all the contact that were created during Step 2 of the process. Sold To person would be the contact to whom the product was sold
1, Invoice Owner -
* This field will only be used incase of creating a Quote created for a End Customer that involves a Partner; Please see [Creating a Quote for Partner Section](#resellerQuote)
1. Invoice Owner Contact - is the person at the Invoice Owner who will receive the invoice.
1. Note that the GitLab entity information will be populated via the following rules:
 * If a Direct Customer or Invoice Owner is an Unauthorized Reseller and the Ship To Country is the United Kingdom, the entity is GitLab Ltd (UK).
 * If a Direct Customer or Invoice Owner is an Unauthorized Reseller and the Ship To Country is the Netherlands, the entity is GitLab BV (NL).
 * If a Direct Customer or Invoice Owner is an Unauthorized Reseller and the Ship To Country is not the United Kingdom or the Netherlands, the entity is GitLab Inc. (US).
 * If the Invoice Owner is an Authorized Reseller and the Ship To Country is the United Kingdom, the entity is GitLab Ltd (UK).
 * If the Invoice Owner is an Authorized Reseller and the Ship To Country is the United States, the entity is GitLab Inc. (US).
 * If the Invoice Owner is an Authorized Reseller and the Ship To Country is not the United Kingdom or the United States, the entity is GitLab BV (NL).
1. Payment Method -  refers to the type of payment the customer is using for paying this Quote/Subscription
1. Payment Methods currently defined are as follows –
 * Credit Card
 * ACH
 * Check
 * Wire Transfer
1. Currency - only USD is available.
1. Click Thru EULA - is used when an agreement has not been signed; A use case being a product (EE) is sold through a partner
1. Start Date -  Specify the date on which this subscription, or contract, is effective. This date becomes the Contract Effective Date of the subscription in Zuora. Note: Customers can purchase in advance of the subscription Start Date. In this case, when the Quote is pushed to Z-billing the license generated will be encrypted with the future Start Date and will not function until then.
1. Subscription Term Type:
 * By default set as Termed
1. Initial Term and Renewal Term -  Specify initial term and the renewal term in months
1. Auto Renew -  it is checked by Default; Subscription automatically renew when the initial term for a subscription is over. This is turned off when the Invoice Owner is a Reseller.
1. Tax Exempt - Need to check with client to make sure they are tax exempt and load tax exempt certificate into their account in SFDC.
1. Tax Exempt - If tax exempt click yes on drop down menu and add additional notes if needed.
1. If the Invoice will come from GitLab Ltd or GitLab BV, you are required to enter the VAT/Tax ID field. A validation error will not allow you to save the quote, so if you do not have this information available, just enter "0000" until you receive it. You will not be able to send a quote to Zuora if the VAT/Tax ID is "0000".
1. Special Terms and Notes - Enter any additional notes that is not specified by the above settings.
1. Click on Next to make the product selection
1. Product Selector Page
1. Click on Product Vlookup Button to make the product selection
1. Click on Rate plan Vlookup Button to make the rate plan selection
 * GitLab Enterprise Edition is the rate plan when selling per license seats @ $39
1. In the Discount field, enter the discount in percentage (%) you wish to apply. This will automatically update the Effective Price field.
1. Conversely, if you wish to apply a specific price to a product, enter the price in the Effective Price field. This will update the Discount (%) field.
2. Enter the quantity of the product.
1. After you hit enter, the Total Price of the line item will update.
1. Finally, enter the Period of the line item.
1. Click Save to save the changes you made to the line item.
1. If you need to add additional products to the quote, click New Product Button and repeat the steps of adding a product, rate plan, discount, price, and quantity.
1. After you've completed adding all products to a quote, click Next Button and you will be taken back to the Quote record detail screen.
1. Once the quote has been created, you can modify it, delete it, or send it from Salesforce to Zuora to create a subscription.
1. Before you can deliver the quote to the prospect or customer, it must be approved. Please refer to the [Opportunity Discounting Approval Matrix](https://docs.google.com/document/d/1-8TG8YLAQB-465mFLYnX3wkB6C6-0aI1A4CzdfjpacU/edit) to review the approval tiers.
1. To request approval, go to the Opportunity record in Salesforce and go to the Chatter feed. To direct the Chatter message to a particular person or persons, use `@firstnamelastname`. Note that multiple people may be required to approve a quote (eg, Discount for EE Premium greater than 10% and an ACV greater than $499,999.99). A Chatter message will ensure all requests and approvals are documents within the opportunity.

#### Step 5 – Generate Quote

1. Once a quote has been approved, go back to the quote and click Generate PDF or Generate Word.  The document will be saved as an attachment in the Notes and Attachments section in the opportunity record. 
2. The default template for all transaction types (new, amendment, or renewals) will be the direct (non-channel) quotes that do not show $0 line items. If you want to select a different template, click the search icon next to the Quote Template field and select the desired template. A description of each template will be visible next to each template.

#### Step 6 – Send for signature via Sertifi

1. Within the ZQuote object, click Sertifi E-Sign button near the top of page.
1. 1st signer will be auto-populated with the bill to contact.  You can change if needed by clicking on the search icon next to the contact name field.
1. You will now be asked to attach the Quote PDF.  Under the drop down for Related Notes and Attachments.  Select the quote for signature and click send for signature.
1. Once the prospect/customer has signed, you will receive an email with the signed quote as an attachment. The signed document will also be added to the Notes and Attachments section of the Opportunity.

#### Step 7 – Send to Zuora

1. Once the Quote is signed, the Sales rep will click on Send to Zuora button. This will complete a few actions. First it will create the subscription in Zuora. Second, it will create the Billing Account. Lastly, it will prepare the system to send an invoice to the customer (this is completed by the Finance team).
2. To send a quote to Zuora, go to the Quote and click on the Send to Zuora button.
3. Review the customer and product details.
4. Click Submit.

##### Quote Metrics

The following quote metrics are available:

 * MRR (Monthly Recurring Revenue) - Monthly recurring revenue (MRR) calculates subscription recurring fees normalized to a monthly value.
 * Delta MRR - Delta of the total MRRs between the original subscription and the amendment.
 * TCV (Total Contract Value) - Total contract value (TCV) calculates the total recurring charges over the lifetime of a subscription.
 * Delta TCV - Delta of the TCVs between the original subscription and the amendment.
 * Sub-total - The quote subtotal for the specified billing periods, excluding discount charges and taxes.
 * Discount - The sum of all discount charges for the specified billing periods.
 * Tax - The tax calculated for the specified billing periods.
 * Total - The quote total for the specified billing periods, including discount charges and taxes.

##### Edit Quote Button

 * You can only edit a quote before it is sent to Z-Billing. After a quote is sent to Z-Billing and its subscription is created, you can no longer edit the quote in Salesforce.

##### Edit a Quote

 * To Edit a Quote, click Edit Quote Details.
 * On Edit Quote Details page, make the desired changes.
 * Click Save.

##### Select products Button

 * To add, remove, or update products, rate plans, and charges for a quote sales rep can click Select Products.
 * Make necessary changes to products, rate plans, and charges
 * Click Save.

##### Delete Button

 * On the Quote Detail page, click Delete Quote Details to delete a quote that was created.
 * A message would appear to confirm on delete on click of ok quote gets deleted

##### Generate PDF Button

 * This will allow the sales rep to Generate a quote pdf
 * On click of Generate PDF – Quote PDF gets generated

#####  Send to Z-Billing Button

 * On the Order Preview page that opens, review the information, and then click Submit to send the quote to Z-Billing.
 * A confirmation popup shows up, Zuora Quotes has successfully sent your quote to the Z-Billing and a subscription was created

#### Step 8 – Before You Submit an Opportunity for Approval

The following is a list of required documents/processes needed before you submit an opportunity for approval:

#####  Direct Deals that do not involve resellers
1. Prospect/Client paid via Credit Card through the web portal (terms are agreed upon sign up).
2. Prospect/Client has returned a signed quote (attach to the opportunity). Quote required for all purchases not made via web portal in order to confirm products purchased, # of seats, term, and pricing.  Quote is also needed to confirm they agree to terms and conditions.
3. In rare circumstances a PO can be accepted in lieu of a signed agreement along with customer acceptance of the click through EULA.  The PO must be submitted to legal@gitlab.com in advance for approval.  Note that the vast majority of customer POs carry terms that invalidate the EULA.

#####  Authorized Reseller Deals that involve an official reseller purchasing on behalf of an End User
1. Reseller has returned a signed authorized reseller quote (attach to opportunity). Quote required for all purchases in order to confirm products purchased, # of seats, term, and pricing.  Quote is also needed to confirm they agree to terms and conditions.
2. Clickthrough EULA must be delivered and accepted by the End User. Please attach a Note to the Notes and Attachments section with a confirmation link or email.

#####  Unauthorized Reseller Deals that involve an unofficial reseller purchasing on behalf of an End User
1. If a PO is received, it must reference our quote showing the Quote ID, products, # of users, term, and pricing of the subscription.  The acceptance of terms language can be removed but click-thru EULA needs to be checked when sending out the license key unless the customer has previously accepted a EULA.
2. If the customer has previously accepted a EULA, then we can use it as the governing terms for this purchase.  In such a case find the ```EULA Acceptance ID``` from our [EULA Request Server](https://customers.gitlab.com/admin/eula_request) and ```EULA Acceptance Date``` and insert the following into the quote: *"By accepting this quote, you, and the entity that you represent (collectively, “Customer”) unconditionally agree to be bound by the terms agreed to in EULA ```EULA Acceptance ID``` previously accepted on ```EULA Acceptance Date```."*
1. If the PO is **approved** by legal, the reseller must return an unauthorized reseller quote (no signature) and is attached to the opportunity. Quote required for all purchases not made via web portal in order to confirm products purchased, # of seats, term, and pricing.  Quote is also needed to confirm they agree to terms and conditions. Also, a Click through EULA must be delivered and accepted by the End User. Please attach a Note to the Notes and Attachments section with a confirmation link or email.
1. If the PO is **not approved** by legal, the end user must sign a standard quote between GitLab and the end user company. Please follow the steps in the Direct Deals section above.

#####  Required fields in Salesforce before submitting for approval
Once you've gathered all required documents and have uploaded them into the Notes and Attachments section of the Opportunity, you'll need to make sure certain fields are populated in the Account and Opportunity records in Salesforce.

1. On the Account record:
  * Industry
  * Billing and Shipping Address
  * In the Special Terms field, add any non-standard terms related to the subscription (ramps, special pricing), support (non-standard SLAs), finance (special billing/payment terms), or legal.
1. On the Opportunity record:
  * Attach any signed agreements, POs, and quotes as an attachment to the opportunity record in Salesforce.com.  If sent/signed via Sertifi, this will happen automatically.
  * Go to the Contact Roles related list and add a Primary Contact. Ideally, you'll add Contact Roles much earlier in the sales cycle.
  * If the opportunity involved a partner, meaning partner will get credit for the opportunity, please click new in the partner section and add partner. There should only be one partner selected for each opportunity.
  * Add the Competitors. Note that this is only required for New Business and Existing Customer - Cross Sell Business; it is not required for Renewals or Add On Business.
  * Make sure your Close Date is for the date you are submitting the opportunity for approval.
  * Provide a Reason We Won the deal. A few sentences on highlighting whether it was our pricing, packages, feature set, etc should do.
  * Once these steps are completed, save the record and submit the opportunity for approval.

#### Step 9 – Submitting an Opportunity for Approval

1. Submit the Opportunity for Approval:
  * Click on the Submit for Approval button on the opportunity. The button is along the top of the page before the Opportunity Details section.
  * If you run into an error submitting the opportunity for approval:
       1. Check the Close Date. The Close Date should be equal or greater than 2016-12-12, the day the approval process was implemented.
       1. Make sure the Approval Status is not equal to "Approved". If the opportunity was already approved, there is no need to resubmit for approval.
  * Once you submit the opportunity for approval, it will be locked, meaning that you will not be able to make any updates. If you'd like to unlock the opportunity to make any changes, you'll have to recall the approval submission. Scroll down to the Approval History section and click on the Recall Approval Request button. Once you've made your changes, you can resubmit your opportunity for approval.
  * The opportunity Stage will update to Awaiting Approval.
  * An email will be sent to you confirming that the opportunity has been submitted for approval.
  * An email will also be sent to the approval queue, which consists of members of Finance and Sales Operations.
  * If the opportunity has been rejected, the approver will add notes in the Approval Notes field. You will then receive an email explaining why the opportunity was rejected. Please resolve the issues, then resubmit the opportunity for approval.
  * The Stage will be reverted back to Verbal Commitment, regardless of the previous Stage when initially submitted.
  * If the opportunity has been approved, you will receive an email that the opportunity has been approved.
  * The opportunity will automatically change to Closed Won and the Close Date will update to the date of submission.

### After the Deal is Closed Won

Once an opportunity is approved and marked as Closed Won, the following occurs:

1. A renewal opportunity will be automatically created for the account. The following assignment rules are in place:
  * If Sales Segmentation is SMB, then the renewal opportunity will be assigned to Sales Admin.
  * If Sales Segmentation is Mid-Market, then the renewal opportunity will be assigned to the Account Manager by Region or Sub-Region.
  * If Sales Segmentation is Large or Strategic, then the renewal opportunity will be assigned to the Account Executive.
  * In all Sales Segments, if the Account Manager field is populated, assignments will override to this user.
1. An automated task is created to check in with the Account, 30 days after the deal closes.  The purpose for this check in is to make sure they are happy, address any questions they have, ask them to be a reference or to speak with our product marketing team on how they use GitLab.
1. If the customer agrees to be a reference, please complete the following steps:
  * In the Referenceable Customer field on the account page, change the picklist value to "Yes".
  * Select all the Reference Types they are willing to offer (please see the next section for an explanation of the Reference Types).
  * Enter any Reference Comments related to the customer's willingness to be a reference.
  * Also go to the contact object who agreed to be a reference and under the field "role" please select "reference - investors and prospects".
  * If customer agrees to speak with product marketing about how they use GitLab, please email product marketing manager.
1. If the customer declines to be a reference in any way, please note that we cannot mention them in any external conversations with prospects or investors. Please make sure to add notes in the Reference Notes field on why the customer declined.
1. Once the opportunity is closed won, the field "type" on the account object will change to "Customer".
1. A task will be auto created in Salesforce.com reminding you to update the Technology Stack field on the account to reflect the GitLab Tools they are using. Example: GitLab Issue Tracker, CI, Wiki
1. Create an add-on or Existing Account (new division) opportunity if there has been one identified by you at this time.

**Reference Types:**

* Homepage: The customer allows GitLab to use their logo on the GitLab homepage. Please obtain an image file with their logo, or gain customer acceptance of a logo to be used on the GitLab website.
* Customer Story: The customer allows GitLab to share their story and use case with prospects and investors.
* Case Study: The customer allows GitLab's marketing team to draft content highlighting their business challenges and how GitLab solved those challenges.
* Verbal Reference: The customer agrees to speak with either investors or prospective customers on their experience with GitLab.

#### Cloning an Existing Quote

If you'd like to save time by cloning an existing quote, you can do so by doing the following:

1. On the Quote Detail page of the quote you want to clone, click Clone Quote.
2. On the Quote Clone Configuration page, select the following options:
    * Clone Products: Select to clone the products associated with the quote. This option only applies to the New Subscription quotes. Ensure that the products associated with the quote are maintained in the current version of the product catalog.
    * Maintain Quote: Select to be directed to the first step in the Quote Wizard flow that allows you to edit the newly cloned quote. The flows are configured based on the quote type, i.e., New Subscription, Amendment, and Renewal, in the Quote Wizard Settings.
5. Click Next.
    * If you selected the Maintain Quote option, you are redirected to the first step in the Quote Wizard of the newly cloned quote.
    * If you did not select the Maintain Quote option, you are redirected to the Quote Detail page of the newly cloned quote.
8. Please note that you cannot clone the products on an amendment (add-on or renewal quote.)

#### Using the Primary Quote Checkbox

If you create multiple quotes for a single opportunity (EEP vs. EES, single year vs. multi-year, etc.), you can select one of the quotes as the "primary", which  will push the details of that quote to the opportunity. Once you select a different quote as primary, the details of the opportunity are overwritten with the new primary quote's details (amount, initial term, start date, and related quote).

#### Opportunity Values 

The following fields are populated via a series of workflows or calculations from an associated quote or subscription in Zuora to the Opportunity object in Salesforce:

1. Annual Contract Value (ACV) is the value of first twelve months of a subscription. This field is calculated by the Opportunity Term and the MRR fields on the Opportunity. Here are the calculations: If the Opportunity Term is greater than 12 months,  the ACV will be the `12 * MRR`; otherwise the ACV will be `Opportunity Term * MRR`.
2. Renewal ACV is manually populated at this time and takes all renewing opportunities and sums the ACV of these opportunities. For example, there are two opportunities (a new opportunity at 7,800 ACV and an addon at 3,900 ACV). The Renewal ACV for the renewal opportunity will be 11,700.
3. Incremental ACV is `ACV-Renewal ACV`. This value can be negative if the customer is planning to renew at a lower ACV than the previous subscription.
4. Opportunity Term is a value that is captured based on certain scenarios:
   * Single Quote
      * For New Business with a single quote, this field will be populated via the `Initial Term` field on the Quote object.
      * For Renewals with a single quote, this value will be populated via the `Renewal Term` field on the Quote object.
      * For Add-On Business with a single quote, this value will be populated via a formula that takes the `Term End Date - Start Date`. Any partial month will automatically be rounded up to the next month (2 months 1 day will automatically round up to 3 months).
   * Multiple Quotes: If there are multiple quotes, the values from the `Primary Quote` (Quote) will be pushed to the opportunity. If there is not a   primary quote, this values can be manually entered.
   * No Quotes
      * Sales-Assisted- All Types: If there are no quotes, the value will be null and can be manually entered.
      * Web Direct- New Business or Renewal: This value will be hardcoded with `12` months since all web direct opportunities are 1 year in length.
      * Web Direct- Add On Business: This value will take the `End Date` (Subscription) `- Start Date` (opporutnity created date).
5. MRR (Monthly Recurring Revenue) is a value that is captured based on certain scenarios:
   * Single Quote
      * For New Business or Renewals with a single quote, this value will be populated via the `MRR` field on the Quote object.
      * For Add-On Business with a single quote, this value will be populated via `Delta MRR` field on the Quote object.
      * Multiple Quotes: If there are multiple quotes, the values from the `Primary Quote` will be pushed to the opportunity. If there is not a primary quote, this values can be manually entered.
   * No Quotes
      * Sales-Assisted: If there are no quotes, the value will be null and can be manually entered.
      * Web Direct- New Business or Renewal: MRR will be the `Amount/12`
6. Start Date varies by type and is captured based on certain scenarios:
   * Single Quote: for all types of business with a single quote, this field will be populated via the `Start Date` field. For new business or renewal, this will be the date that the new or renewal subsription starts, respectively. For Add-On Business, this will be the start date of the amendment.
   * Multiple Quotes: If there are multiple quotes, the values from the `Primary Quote` will be pushed to the opportunity. If there is not a primary quote, this values can be manually entered.
   * No Quotes
      * Sales-Assisted: If there are no quotes, the value will be null and can be manually entered.
      * Web Direct- New Business or Add-On Business: For new web direct purchases, the `Start Date` will be the `Created Date` of the opportunity
      * Web Direct- Renewal: For web direct renewals, the `Start Date` will be the `Term End Date` + 1 of the subscription.
6. End Date is a value that is captured based on certain scenarios:
   * Single Quote
      * For New Business or Renewals, this field will be populated via a workflow that will take the End Date from the `Start Date + Opportunity Term`.
      * For Add-On Business, this field will be populated via the `Term End Date` on the Quote object.
   * Multiple Quotes: If there are multiple quotes, the values from the `Primary Quote` will be pushed to the opportunity. If there is not a primary quote, this values can be manually entered.
   * No Quotes
      * Sales-Assisted: If there are no quotes, the value will be null and can be manually entered.
      * Web Direct- New Business and Renewals: Since all web direct purchases are for 12 months, the End Date will be calculated taking the `Start Date + 12 months`
      * Web Direct- Add-On Business: End Date will be taken from the `Term End Date` on the Subscription object.

If a quote is sent to Zuora, the values from the Quote will overwrite any values on the opportunity, regardless of whether the quote is primary or not. If there are discrepancies between any of the values, such as the MRR, Amount, or Start and End Dates, please contact Finance or Sales Operations to resolve. We will either need to make amendments to the subscription or manually override the value in the Opportunity.

#### How to Handle Duplicate Accounts and Opportunities from Web Direct Purchases

In some cases, a prospect or customer that is currently engaged with an AE or AM on an opportunity might be proactive and sign up online via the web portal. If this occurs, then a duplicate Account, Opportunity, and Contact may be created. In the event that a duplicate opportunity is created, please do the following to resolve. Unfortunately there is no current method of merging opportunities so the work is manual at this time:

1. Go to the web direct opportunity and add a Chatter note to Francis Aquino. To message someone directly, add the `@` sign before typing their name.
1. Add this note in Chatter: "Here is the duplicate web direct for the following opportunity <URL of original opportunity>".
1. Sales Ops will mark the web direct opportunity as `9-Duplicate` while marking the original opportunity as `6-Closed Won`. This will ensure that historical creation dates, lead sources, and other information is maintained for analysis.
1. If a duplicate account is created, Sales Ops will merge the two accounts together and change the CRM ID in Zuora from the new account to the old account.

If the prospect is still a Lead record that has not converted into an Account, please complete the following steps:

1. Go to the Lead record and copy the following information from the Lead Information section to the Opportunity Detail section: Lead Source, Business Development Rep.
1. In the Opportunity Detail section, change the Sales Qualified to TRUE, Sales Qualified Date should be the Close Date, and the SQL Amount should be the Amount.
1. In the Qualified Questions section, copy over the answers from the Lead to the Opportunity.
1. In the Activities History related list, reassociate tasks from the original opp to the new opp. If there are a lot of activities, move over the most important tasks. To do this, go to the activity you'd like to move and click Edit. In the Related To section on the right side, replace the original opportunity name with the new one.
1. Change the Lead Status to Web Portal Purchase and save the record.

#### Closing Deals for GitHost

 * Confirm with client the best contact for installation, the type of plan, and how many EE users will be needed, then create quote.
 * When the quote is created, the system will automatically add the GitHost Subscription Terms to the quote in addition to the GitLab EE Subcription Terms.
 * Once quote is singed, send to zbilling
 * Once sent to zbilling there will be an automated email that goes out to support@gitlab.com alerting the support team to contact the client to connect their GitLab EE license key with the GitHost instance
 * A second email will be sent to the client with the GitLab EE license key and the process will be complete

#### Closing Deals for Educational Institutions receiving educational pricing

 * The customer should purchase a license as normal through Zuora, except that the number of users purchased should only include non-student users (as described in [Educational Pricing](https://about.gitlab.com/license-faq/)).
 * After the customer purchases the license, the account executive then manually creates and sends a license that includes the total number of users, where `total # of users = students + non-students`.

#### View and download invoices in Salesforce

 As soon as an invoice is generated, the sales rep can view and download it as a PDF in Salesforce. Scroll to the bottom within the Salesforce-Account and click on the invoice number under "Invoices". Then on the bottom of the invoice view, click "Invoice PDF".

 A paid invoice will have a zeroed Balance and positive Payment Amount.

### Returning Customer Creation Process(Upgrade/Renewals/Cancellations)

1. Create an Opportunity for an [Add-on or Renewal](https://about.gitlab.com/handbook/sales/#opportunity-types).  If a cancellation, click on Opportunity they want to cancel.
1. Click on New Quote button within the opportunity.
1. Since this is a returning customer, sales rep will see a screen showing the current subscription.
1. This screen determines that this customer is already established in Zuora and will allow the sales rep to perform on the 4 actions –

#### Updating Subscription for the account

1. Amend existing subscription for this billing account
2. Renew existing subscription for this billing account
3. Cancel existing subscription for this billing account

##### New Subscription for the account

1. This will allow the Sales rep to create a [new subscription](https://about.gitlab.com/handbook/sales/#opportunity-types) for the existing billing account.
1. Clicking on Next will take the sales rep thru the same Quoting flow that was seen the new Quote creation process

##### Amend existing subscription for the billing account

1. This process is used to perform any [upgrade to a subscription plan or add-on of additional seats t same subscription](https://about.gitlab.com/handbook/sales/#opportunity-types)on an existing subscription.
1. Choosing “Amend existing subscription for billing account”, will allow sales rep to perform amendment to an existing subscription.(Upgrades)
1. Clicking on the this radio button will list all subscriptions that are tied to the customer
1. Click to choose the subscription for performing an Amendment and hit on Next button

##### Cancel existing subscription for the billing account

1. This process is used to cancel an existing subscription. (Note that if a customer purchases seats for the wrong billing account, please see the next section.)
1. Click on Opportunity to cancel.
1. Click on New Quote
1. Since this is a returning customer, sales rep will see a screen showing the current subscription.
1. Choosing “Cancel existing subscription for billing account”,
1. Clicking on the this radio button will list all subscriptions that are tied to the customer
1. Click the subscription for performing a cancellation and hit on Next button
1. Select cancellation date and click Next Button.

##### Cancel an erroneous subscription for the billing account

1. This process is used to cancel an erroneous subscription.
1. For example, a customer may purchase additional seats or products via the web portal which was originally intended as on add-on to an existing subscription.
1. Provide Finance or Sales Operations with the erroneously created Zuora Subscription ID, invoice number and the correct Zuora Subscription ID.
1. Finance will cancel the subscription and either refund the invoice (if a credit card purchase) or cancel the invoice (if check or other payment method).
1. Finance will then amend the correct Zuora Subscription ID and will either charge the card on file or send the invoice via email.

#### Zuora Supporting 4 types of Amendments –

1. Terms and Conditions amendment – The sales rep will be able to change the terms and conditions of an existing subscription;
1. Remove product Amendment – The sales rep will be be able to perform a Remove a product Amendment;
 * In this case, sales rep will have to Set the Start date (Contract effective date in Zuora terms) when the remove product amendment should happen
 * Click on Next
 * This will take them to the product selector page and displays the original product that was purchased within the subscription
 * Sales rep can now remove the product
1. Add product Amendment – Sales rep can add a new product from the product selector page
1. Update Product Amendment – Sales rep can update the existing product of the existing selected product
 * Note: Do not change the Terms and conditions unless you are performing a terms and conditions amendment(except for start date).
       Let's take an example - Let's say a customer once to add more seats to their license.  
       1. Set the start date
       1. Change the quantity field to reflect the new total number of seats
         * Hit on Save

Once on the Quote Summary, will click on generate PDF to generate a Quote PDF
Send it to the customer - only if there is no record of a signed quote. If customer purchased online, they agreed to our terms and condition, so no need to have them sign a quote.  It is ideal though.
Upon Sign-off, or existing signed quote, click on the Send to Z-billing button to send the Quote over to Zuora

##### Renew existing subscription for the billing account

1. This process is used to perform Renewal on an existing subscription; this is only created if the AUTO RENEW Flag is set to “NO” for a subscription initially.
1. Choosing “Renew existing subscription for billing account”, will allow sales rep to perform Renewal to an existing subscription;
1. Clicking on the this radio button will list all subscriptions that are tied to the customer
1. Clicking on next will take the sales to the Create Renewal Quote page
1. Sales rep will select the renewal Quote Template from the list
1. Enter the Renewal term in months
1. Will hit on Next
1. Skip the product selector page, unless want to update the QTY or want to add a new product
 * if they are adding more seats, change the quantity field to reflect the new total number of seats
1. Once on the Quote Summary, will click on generate PDF to generate a Quote PDF
1. Send it to the customer, via Sertifi button within Zquote screen
1. Upon Sign-off will click on the Send to Z-billing button to send the Quote over to Zuora
1. Close Won the opportunity

##### Renew existing subscription with a "true-up" for the billing account

1. This process is used to perform a Renewal on an existing subscription and to add a one time charge for true up; this is only created if the AUTO RENEW Flag is set to “NO” for a subscription initially.
1. Choosing “Renew existing subscription for billing account”, will allow sales rep to perform Renewal to an existing subscription;
1. Clicking on the this radio button will list all subscriptions that are tied to the customer
1. Clicking on next will take the sales to the Create Renewal Quote page
1. Sales rep will select the renewal Quote Template from the list
1. Enter the Renewal term in months
1. Will hit on Next
1. On the product selector page, add the true up product
 * enter the number of seats they will true-up.  Add in the price of the seat, 100% of price they paid.
1. Next, update their current subscription to reflect the new total number of seats they will be renewing for which will be equal or greater than the amount they had with their subscription plus the true up amount.
1. Once on the Quote Summary, will click on generate PDF to generate a Quote PDF
1. Send it to the customer, via Sertifi button within Zquote screen
1. Upon Sign-off will click on the Send to Z-billing button to send the Quote over to Zuora
1. Close Won the opportunity

##### Tracking Churned Subscriptions and Opportunities

In the event that a customer downgrades, terminates, or does not renew their subscription, Sales Operations and Finance will process the churn information in the opportunity record. Churned opportunities will be identified by having a negative Incremental Annual Contract Value (IACV). The following information will be captured:

* Churn Type: 
  * Downgrade (Price) is used when a customer renews with the same product, but the per unit price is discounted for whatever reason.
  * Downgrade (Product) is used when a customer either downgrades to a lower paid package or removes an add on at renewal.
  * Downgrade (Seats) is used when a customer reduces the number of seats from the previous year at renewal.
  * Termination is used when a customer requests to cancel their subscription mid-term.
  * Non-Renewal is used when a customer requests to cancel their subcription upon renewal.
* Churn ARR: The annual recurring revenue that was lost. 
* Churn Month: The month that the churn occurred. Most of the time, this will be the close date. However, a churn may be retroactive and occur in a prior month.
* Churn Notes: Open text field to capture any additional notes regarding the churn. If the customer has provided specific reasons for churn, the details will be entered in this field. 

The following events will trigger an email to Sales Operations and Finance for tracking churn:

* An opportunity has been submitted for approval with a negative amount. This signifies either a credit or refund of a subscription was requested by a customer and processed by an Account Executive or Account Manager.
* A renewal opportunity has been won, but has a negative IACV. This signfies that the customer has downgraded. Sales Operations and Finance will reach out to the opportunity owner to understand the nature of the churn.
* A renewal opportunity has been lost. This signifies that the customer did not renew their subscription. Sales Operations and Finance will reach out to the opporutnity owner to understand why the customer did not wish to renew.

### Creating a Quote for an Authorized Reseller Partner

A reseller quote has a few different things than a regular quote:

* Before you generate a quote for an authorized reseller, make sure to go to the reseller's account record in Salesforce. In the Account Detail section, enter the Payment Term (30, 60, etc) that has been agreed upon between GitLab and the reseller. Make sure to only enter the numeric value and not "Net 30" or "Net 60". This value will appear in the Quote document in the Terms section.
* Quote Name Field:  append “via reseller name” to the Quote name (i.e.: “Quote for Federal Reserve via ReleaseTEAM”)
* Quote Template:  Needs to be a reseller template, such as "Reseller New Quote" or "Reseller Amendment Quote".  Since resellers cannot accept terms for their customers, the reseller template contains different language around acceptance.
* Sold To Contact and Bill To Contact fields both need to be a person at the end customer.  This is who will accept the EULA.
* Invoice Owner Field:  This needs to be the resellers account.  If you do not see the reseller listed, then you need to send the SFDC URL of the reseller’s billing contact to finance and for an Invoice Owner record to be created.
* Invoice Owner Contact: This is the Bill To Contact for the reseller. This is important as the Bill To Contact's account record will populate the GitLab entity, and all information related to that GitLab entity (Entity Name, Entity Contact Info, Entity Banking Information, and Entity Beneficiary Information).
* Click Through EULA required: Set this to Yes.  This will cause a URL to be sent to the customer where they agree to our Terms and Conditions before getting their license key.  This is important as a reseller cannot agree to terms on behalf of the end user.  Alternatively, the reseller could obtain a physical signature and send it to you.
* Discount: Authorized resellers all have pre-defined discounts depending upon the market they serve and the services they provide to GitLab.  GitHost is never discounted as our margin after paying Digital Ocean is very small.  We do not give discounts to fulfillment houses like SHI, Insights, or other resellers that are not authorized resellers.  Reseller discounts can be found on the first page of the [Resellers List](https://docs.google.com/spreadsheets/d/1tQjPMRUuzsDR4mNj74aY-W8jBQH4u9h7PpEsw088Zx0/edit#gid=1395032632)
When in doubt please consult the reseller team.

### Using Customer Form Agreements
{: #CustomerFormAgreements}

Our experience shows that using a prospect's form agreement is expensive and, more importantly, time consuming.  Deals in which we use the customer agreement take on average 60 days longer to close than if completing using our standard subscription agreement with changes as requested by customer counsel.  The arguments in favor of using our agreement are as follows:

1. Our agreement is an annual subscription agreement with a true-up whereas customer form agreements typically are based on paid up licenses.
1. We are an open source company and our agreement provides licenses for both the CE version of the product and the EE version as well as dealing with contributions of code from our customer.
1. We have non-standard but customer favorable warranty and acceptance provisions.
1. We are very accommodating of customer requested changes to our form agreement which is why we can close deals quickly.

Despite the overwhelming arguments in favor of using the GitLab form some prospects insist on using their form agreement.  GitLab will accommodate such requests with the following assumptions:

1. GitLab must have been selected as the solution of choice by the customer.
1. The deal must be in excess of $15,000.
1. The primary decision maker must indicate their willingness to facilitate the internal process in a manner that brings issues to closure within 30 days of negotiations.  The decision maker must also acknowledge that they understand that the form agreement may require significant revisions based on what is described in the above section.
Items 1 and 3 above must be acknowledged in writing prior to proceeding with the contract markup.

### Using Cases in Salesforce

A Case is a question or feedback from a prospect or customer. While there are many ways that a customer can reach out to GitLab, the following are the only email addresses that will crease a Case in Salesforce:

#### New Business Inquiries
* sales@: this is an inquiry from a prospect requesting information on GitLab's services. These inquiries will be handled by the BDR and Sales Team, depending on record or territory ownership.

#### Existing Customer Inquiries
* ar@: questions around billing or payments.
* renewals@: these are questions regarding renewing a subscription.
* support@: these are technical questions or issues submitted by our customers or trial users.
* Please see the [Account Management Handbook] (https://about.gitlab.com/handbook/account-management/) for more information regarding existing customer inquiries.

#### Emails to Sales@
When a case is submitted, if the contacts email address is in Salesforce, the contact owner will be assigned to the case.  If there is no match, the case will go to our [BDR Queue](https://na34.salesforce.com/500?fcf=00B610000042ioq). Anyone can check this queue and reassign to yourself if this is your contact or respond to this case.

Cases display in an Emails related list. The Emails related list includes all emails sent by your customer regarding a particular case, as well the email threads between you and your customer. The first 77 characters of an email message appear in the related list so that you can see what the message is about without having to click on it.

#### Reassigning Sales@ Cases to the Account Management Queue
Since sales@ was the default email address for pre-sales and post-sales communication before the creation of ar@ and renewals@, customers might still send questions on billing or renewals to sales@. When this happens, reassign the Case to the [Account Management Queue] (https://na34.salesforce.com/500?fcf=00B610000042ioq):

1. Go to the Case record.
2. Next to the Case Owner field, click on the "Change" link.
3. In the pull down field, select "Queue".
4. Then type in the Owner field, "Account Management Queue".
5. Make sure the checkbox to "Send Notification Email" is checked.
6. Click Save.
#### To work with Email-to-Case or On-Demand Email-to-Case emails

* Click Send An Email to send an email to a contact, another user, or any other email address. Select a "From Address".  Preferably use sales@ address.
* Click Reply to respond to an email. The email response automatically includes the email body as received from the customer. Enter your response and click Send.
* Click To All to respond to all participants on an email thread.
* The email address of the contact who created the case automatically appears in the To field, as long as the creator is an existing contact. To add more recipients, click Lookup icon to look up an address, or type or paste email addresses or names in the To field.
* When you enter an email address or name that matches one contact or user, the address appears as a button with the person’s name.
* To add several addresses at once, copy and paste them separated by spaces or commas. These email addresses appear as buttons, and, if they’re associated with a contact or user, show the contact’s name.
* When you enter an email address that matches multiple contacts or users, the address appears as a button. Clicking the button brings up a list of people associated with the email address so you can choose the one you want to associate with the message.
* If you need to copy other people on the message, click Add Cc or Add Bcc.
* By default, the email subject is the name of the case it’s related to. You can edit the subject if you need to.

* Click the subject of the email to view the email. From the email, you can reply to the sender, reply to everyone, forward the email, or delete it.
* While viewing an email, you can display a list of all the emails associated with the case by clicking Email Message List, and you can navigate to the case's other emails by clicking Next or Previous.
* While viewing an email, click Forward to forward it. The email automatically includes the email body as received from the customer. Optionally, enter text and click Send.

#### Closing a Case

* Before closing a case, make sure that the account is associated with the case
* Choose the case reason before you close

### Process after you close a Premium Support Subscription

Once you close a deal that includes Premium Support, you need to:

1. On the account object in Salesforce, check the **Support Level** in the _GitLab Subscription Information_ section, so that it carries through to Zuora and Zendesk.
2. Notify the Customer Success team there is a new Premium support customer, by creating an issue on the [Customer Success](https://gitlab.com/groups/gitlab-com/customer-success/-/issues) project using the _Premium support onboarding_ template. Be sure to include all parts of the issue:
   - Name of organization
   - Domain name, and optionally named individuals that are most likely to submit support tickets
   - Link to the SalesForce record.
   - Mark the issue confidential!
