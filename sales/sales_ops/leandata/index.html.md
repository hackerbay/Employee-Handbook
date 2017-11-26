---
layout: markdown_page
title: "LeanData"
---

---
## On this page
{:.no_toc}

- TOC
{:toc}

---

## LeanData

### What is LeanData?

LeanData enables strategic lead management within Salesforce so leads are assigned to the right reps. This is done by leveraging LeanData's fuzzy logic algorithms and lead-matching database. Whether we introduce a sales process based on named accounts, geographic territories, employee size (or all of the above), LeanData allows us to easily manage seemingly complex lead assignment rules.

### How It Works

LeanData is made up of three primary solutions: Lead/Account Matching, Lead Routing Rules, and Cross-Object Visibility.

#### Lead/Account Matching

The primary feature for LeanData is matching leads to accounts using a number of different criteria: company name, email address, and IP address. If a new lead is created in Salesforce, LeanData will review the criteria to determine if it matches an existing account in the system and will deliver the lead to the correct user as per our defined lead routing rules. Note that our matching criteria will include both the company information and region.

#### Lead Routing Rules

Our lead routing rules are as follows:

1. Any record created with a person score greater than or equal to 50 will be inserted into Lean Data flow. Every time the person score is updated, Lean Data will run a check to see if the record needs to be processed through the flow.   
2. Every record will be checked against the database to determine if there is a duplicate record: 
     - If LEAD record matches an existing CONTACT record within a "target account" owned by an O-SDR, then the lead is converted to a contact record and merged with existing record.   
3. If a record matches an existing account and there is a I-SDR on the record -> lead will be routed to that I-SDR.
4. If a record matches an existing account and there is NOT a I-SDR on record -> lead will move to next step in the funnel.  
4. If a record matches an existing record, in the same Region and is not owned by a Reseller account -> lead is routed to the Lead Owner. 
5. If a record matches an existing record, in the same Region and is owned by a Reseller account -> lead is moved to the next stage of the funnel. 
6. If a record matches an existing record, in a different Region -> lead is moved through the funnel to the next stage. 
7. If a record has not been matched to existing records or accounts, the leads will be distributed based on Region:  
     * APAC: If Korean, route to Conor Brady; all others US/APAC I-SDR Round Robin
     * EMEA: EMEA I-SDR Round Robin  
     * NCSA: US/APAC I-SDR Round Robin
     * Federal, Government, Non-Profit, Education: US/APAC I-SDR Round Robin   

Changes to specific lead routing made on 3 November 2017, leads with source of "Contact Request" in in the `Strategic` and `Large` sales segments will be routed to the Account Owner/Account Executive that owns the account. Details related to this change can be found in the [SDR Handbook](https://about.gitlab.com/handbook/marketing/marketing-sales-development/sdr/#leadRouting). Update to the Lean Data rules are pending related to this change.    

#### Cross-Object Visibility

One of the most widely-known issues with the Salesforce architecture is the lack of relationship between the lead and account/contact objects. LeanData addresses this lack of functionality. A user can be in an account record and see all related lead records. Within the lead object, a user can view all related leads and accounts. 

**LeanData from the Account Page**
 ![](/source/handbook/sales/sales_ops/leandata/leandata-contact.png)

* Merging a Duplicate Account
  * At this time, this feature is not supported. Please send a note via Chatter on the record you would like merged: "Please merge this account with `<URL of original account>`."

* Converting a Lead from the Account Page
  * Click on the "Convert" link for the lead you would like to add to the Account.
  * You can assign the contact to yourself or another user.
  * The account name will default to the account record you were just on. If you want to create a new account, select the "Create New Account" option.
  * "Do not create a new opportunity upon conversion" is defaulted to TRUE. If you want to create a new opportunity, uncheck this box.
  * Click the "Convert" button.

**LeanData from the Lead Page**
 ![](/source/handbook/sales/sales_ops/leandata/leandata-lead.png)
 
 * Merging a Duplicate Lead
  * Before you merge, please visit a Salesforce article regarding merging leads, ["Considerations for Merging Duplicate Leads"](https://help.salesforce.com/articleView?id=leads_merge_considerations.htm&type=0&language=en_US).
  * Click on the "Merge" link for the lead you would like to merge to the current Lead.
  * Select one lead as the “Master Record.” The created date, created by, and read-only fields will retain information from the Master Record.
  * Select the fields that you want to retain from each record.
  * Click "Merge".
  * Click "OK".
 
 * Converting a Lead from the Lead Page
  * Click on the "Convert" link for the lead you would like to add to the Account.
  * You can assign the contact to yourself or another user.
  * The account name will default to the account record you were just on. If you want to create a new account, select the "Create New Account" option.
  * "Do not create a new opportunity upon conversion" is defaulted to TRUE. If you want to create a new opportunity, uncheck this box.
  * Click the "Convert" button.

