---
layout: markdown_page
title: "Marketing Operations"
---
Welcome to the Marketing Operations Handbook.

[Up one level to the Marketing & Sales Development Handbook](https://about.gitlab.com/handbook/marketing/marketing-sales-development/)    

----

## On this page
* [Overview](#overview)
* [Marketing Tech Stack](#techstack)
* [How-tos & FAQs](#howto)
* [Leads](#leads)  
* [Email Management](#email)
 

----


## Overview <a name="overview"></a>

Marketing Operations (Mktg OPS) supports the entire Marketing team as well as other teams within GitLab. Mktg OPS works closely with Sales Operations to ensure information between systems is seamless and we are using consistent terminology in respective systems. 	


## Marketing Tech Stack <a name="techstack"></a>

Our current marketing tech stack consists of the following tools: 
- Clearbit: Enrichment tool to add details to customer & prospect record to aide in sales process and overall database segmentation.
- DiscoverOrg: Industry specific data enrichment for leads/contacts/accounts
- FunnelCake: Buyer lifecycle and funnel analytics tool
- Google Analytics: Web analytics tool that tracks and reports website traffic
- Google Tag Manager: Tool to add/update website tags, incl. conversion tracking, site analytics, remarketing, without needing to edit website code
- InsideView: Lead enrichment tool
- Lean Data: Lead routing and account matching tool
- Marketo: Marketing automation and database management tool  
- Olark: Real-time chat function for customer engagement
- Outreach.io: Email communication tool for the BDR/SDR/AEs to manage communication with leads/contacts
- Piwik: Open source web analytics platform used to measure web performance
- Salesforce: Customer Relationship Management (CRM) tool used to manage all customer & prospect data
- Terminus: Account-based Marketing (ABM) advertising tool to drive B2B demand
- Unbounce: Custom landing page tool specific for driving conversions
- Zoom: Video and Web Conferencing tool used for webcasts and online demos

### [Tech stack contract details and admins](https://about.gitlab.com/handbook/marketing/marketing-sales-development/marketing-operations/contracts) 


## How-tos & FAQs <a name="howto"></a>

### Marketing Team OKR Issue Board <a name="okr"></a>
For Q4 2017, we will be using an [Issue Board](https://gitlab.com/gitlab-com/marketing/boards/377172?milestone_title=Q4%202017&=) to track our department OKRs.   

To create an OKR issue do the following:   
 - **Title**: [META] {Team Name} OKR 1 (2 or 3): {Name of your OKR}  
      - Do not use a hash in front of the OKR number, it will associate the issue with existing issue with same number. Incorrect: '#1' 
      - If using a hash in front of the OKR number put a space between the two characters. Correct: '# 1'
 - **Description**: List your 3 Key Results as todos/checkboxes  
 - **Assignee**: Assign to yourself   
 - **Milestone**: Associate the [META] Issue with 'Q4 2017'
 - **Labels**: 'OKR', your team label (Design, Content, etc), and appropriate status - 'Not Started' (starting position for 99% of OKRs), 'Progressing', or 'Partially Completed'   

When you start working on an OKR, update the label from ‘Not Started’ -> ‘Progressing’. If creating "sub-Issues" related to your META OKR Issue, associate using the 'Related Issue' section. 

Merge Requests related to OKRs should also be associated ‘Q4 2017’ Milestone and contain ‘OKR’ & team label. 


### Webcast &amp; Event Setup <a name="setup"></a>  
When creating an event (live or online), webcast, or gated content its important to integrate the campaign across the three main platforms used - Unbounce (landing page), Marketo (Marketing Automation) and Salesforce (CRM). This provides transparency about the event to anyone with access to Salesforce, namely the Sales and Marketing teams.  

[Instructions](https://docs.google.com/a/gitlab.com/document/d/1yWPT2yxxhBIpBFjqZLS3SBaKEJdxSBdSKG72dcrDF5k/edit?usp=sharing) to create an event from scratch or clone an existing event. 


## Leads <a name="leads"></a>  

Mktg OPS is responsible for setting up and maintaining the lead routing for all inbound leads and also managing the database. There are two main tools used for lead routing: Marketo for form fillouts, lead enrichment and scoring, and Lean Data for account matching and routing based on account type (customer, prospect, strategic, etc), region and sales segment.  

[Lead routing rules](https://about.gitlab.com/handbook/sales/sales_ops/leandata/#lead-routing-rules) can be found in the Sales Operation section of the handbook.

As leads are created they are scored based on a collection of demographic information, engagement and/or behavioural data. Once a lead reaches a score of 90 points or more they are considered a Marketing Qualified Lead (MQL). Currently there are two MQL buckets: (1) hand raisers (A leads) and (2) passive leads. Detailed information about the [Lead definition](https://about.gitlab.com/handbook/marketing/business-development/#mql) can be found in the Business Development section of the Handbook.    

The [MQL Scoring Model](https://docs.google.com/a/gitlab.com/document/d/1_kSxYGlIZNNyROLda7hieKsrbVtahd-RP6lU6y9gAIk/edit?usp=sharing) is based on a 100-point system. Positive and negative points are assigned to a lead based on their demographic and firmographic information, and their behaviour and/or engagement with the GitLab website and marketing campaigns.  
This model was implemented on 13 February 2017 and only impacted leads moving forward. For reporting purposes, it was decided not to retroactively adjust scores and MQL dates. 


## Email Management <a name="email"></a> 
Email database management is a core responsibility for Mktg OPS. Ensuring GitLab is following email best practices, in compliance with International spam laws and overall health of active database are all priorities.  


### Requesting an Email
To request an email, create an issue in Marketing and assign it to JJ Cordz and tagging Mitchell Wright (in addition to whomever else needs to be aware of email). Required request information, please be as complete as possible in providing detail related to the email:
- **Sender Name**: Typically we use GitLab Team for most outgoing communications; for Security Alerts we use GitLab Security. Choosing a name that is consistent with the type and/or content of email being sent is important, if unsure make a note and we will make recommendation  
- **Sender Email Address**: What email address should be used? [List of available email aliases](#emailalias)
- **Subject Line**: 50 character max is preferred 
- **Email Body Copy**: Can be a text snippet within issue, clearly identified comment on issue or attach a Google doc with copy 
- **Target Date to Send Email**: at a minimum a few days notice is preferred because we need to balancing the number of emails being sent to our database so they are not perceived (or marked) as spam; however, a simple email can be turned in a few hours if absolutely necessary
- **Recipient List**: Emails can be sent to one of the [existing segments](#emailsegment) or a recipient list can be provided as a .csv file 


### Email Communication Policy   
As of 22 August 2017, all email marketing communications are explicit opt-in. Using the [Email Subscription Center](https://page.gitlab.com/SubscriptionCenter.html), users can control their email communication preferences. There are currently 4 [email segments](#emailsegment). 



### Email Segments <a name="emailsegment"></a> 
Database segments and how someone subscribes to specific segment:  

- **Newsletter**: All users who sign up for a GitLab.com account are automatically added to this segment and users can subscribe to the newsletter through the blog, Contact Us page and CE download page.
- **Security Alerts**: Subscribe on the GitLab [Contact Us page](https://about.gitlab.com/contact/)
- **Webcasts**: When someone registers to a live or on-demand webcast
- **Live Events**: When someone registers to attend a live event, meet up or in-person training. Use of this segment is narrowed down by geolocation so notification and invitation emails are specific to related area.  



### Aliases <a name="emailalias"></a> 
Current list of email aliases used in Marketo to send email: 
- Community@ company domain: external email address for sending confirmation emails related to GitLab products. Replies are forwarded to Zen Desk support    
- Content@ company domain: external email address associated with management of our SlideShare account. Replies are forwarded to Sr. Director of Marketing & Sales Development, Content Marketing Manager & team   
- Events@ company domain: external email address for sending live, VIP &amp; in-person training related emails. Replies go to Field Marketing Manager and Marketing OPS Manager     
- Giveaways@ company domain: external email address for receiving content & social media related promotional giveaways. Replies go to Content Marketing Team, Field Marketing Manager and Marketing OPS Manager    
- Leads@ company domain: external email address for internal Lead alerts. Replies go to Marketing OPS Manager and Online Marketing Manager
- News@ company domain: external email address used to send newsletter. Replies go to Online Marketing Manager
- MarketingOPS@ company domain: external email address used to direct generic operational requests to Marketing OPS Manager and Online Marketing Manager
- MarketingSFDC@ company domain: external email address associated with management of Salesforce. Replies forward to Online Marketing Manager, Field Marketing Manager, Sr. Director of Marketing & Sales Development, Product Marketing Manager and Content Marketing Manager
- SecurityAlerts@ company domain: external email address used to send security alerts. Replies go to Online Marketing Manager   
- Sponsorships@ company domain: external email address used to manage sponsor requests from community. Replies forward to Community Advocate Team
- Support@ company domain: external email address for sending Breaking Change and/or support related customer communications. Replies go to Zen Desk support     
- Surveys@ company domain: external email address for sending the Developer Survey and/or related surveys. Replies go to Content Team, Sr. Director of Marketing & Sales Development and Product Marketing Manager   
- Webcasts@ company domain: external email address for sending webcast related emails. Replies go to Content Marketing Team and Online Marketing Manager    


### Types of Email
**Breaking Change Emails**  
These are operation emails that can be sent on a very selective as needed basis. This is an operational-type email that overrides the unsubscribe and does not provide the opportunity for someone to opt-out. Usage example: GitLab Hosted billing change, Release update 9.0.0 changes, GitLab Page change and Old CI Runner clients. 
It is very important to have Engineering and/or Product team (whoever is requesting this type of email) help us narrow these announcements to the people that actually should be warned so we are communicating to a very specific targeted list. 


**Newsletter**  
Sent bi-monthly (every 2 weeks). Content Team is responsible for creating the content for each Newsletter.  


**Security Alerts**  
Sent on an as needed basis containing important information about any security patches, identified vulnerabilities, etc related to the GitLab platform. These emails are purely text based. 


**Webcasts**   
Invitation and/or notification emails sent about future webcasts.   


**Live Events**   
Invitation emails to attend a live event (VIP or Executive Lunch), meetup, or in-person training. These emails are sent to a geolocational subset of the overall segment. This type of email is also used when we are attending a conference and want to make people aware of any booth or event we may be holding and/or sponsoring.   


### Alert Emails   
Alert emails are sent directly to the Lead Owner on record. If Lead is owned by a Partner, the alert email is sent to the BDR Email Address on record.    
APAC -> To: Kyla Gradin & Jameson Burton (evenly distributed)     
NCSA -> To: Kyla Gradin, Lanice Sims & Jameson Burton (evenly distributed)    
EMEA -> To: Conor Brady    
Federal -> To: Brent Caldwell; cc: Paul Almeida  

**New Trial Lead Alert**    
Sender: ALERT - Lead    
From Email/Reply-to: leads@    
Subject Line: Enterprise Premium Trial: {{lead.First Name}} {{lead.Last Name}} from {{company.Company Name}}   


**Contact Request**   
Sender: ALERT - Contact   
From Email/Reply-to: leads@      
Subject Line: Contact Sales Request: {{lead.First Name}} {{lead.Last Name}} from {{company.Company Name}}   


**Consultancy Request**   
Sender: ALERT - Consultancy   
From Email/Reply-to: leads@   
Subject Line: Consultancy Request: {{lead.First Name}} {{lead.Last Name}} from {{company.Company Name}}   


**Development Request**   
Sender: ALERT - Development    
From Email/Reply-to: leads@    
Subject Line: Development Request: {{lead.First Name}} {{lead.Last Name}} from {{company.Company Name}}   


**Federal Contact Sales Request**  
Sender: ALERT - Federal Contact  
From Email/Reply-to: leads@   
Subject Line: Federal Contact Sales: {{lead.First Name}} {{lead.Last Name}} from {{company.Company Name}}   


**New Lead MQL**  
Sender: ALERT - New MQL Lead  
From Email/Reply-to: leads@  
Subject Line: New MQL Lead: {{lead.First Name}} {{lead.Last Name}} from {{company.Company Name}}  


**Professional Services Request**   
Sender: ALERT - Professional Services   
From Email/Reply-to: leads@      
Subject Line: Professional Services Request: {{lead.First Name}} {{lead.Last Name}} from {{company.Company Name}}   

