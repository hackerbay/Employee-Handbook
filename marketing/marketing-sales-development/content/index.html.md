---
layout: markdown_page
title: "Content"
---

## Welcome to the Content Marketing Handbook

The Content Marketing organization includes Social Marketing and oversees the 
GitLab blog. 

## On this page
* [Editorial Mission Statement](#editorialmissionstatement)
* [Communication](#communication)
* [Definition of Content](#definingcontent)
* [Key Responsibilities](#keyresponsibilities)
* [Campaigns](#campaigns)
* [Campaign Brief Process](#campaignbrief)
* [Publishing Case Studies](#casestudy)
* [Webcasts](#webcasts)

## Editorial Mission Statement

Empower and inspire DevOps teams to collaborate better, be more productive, and ship faster by sharing insightful and actionable information, advice, and resources. 

### Vision

Build the largest and most diverse community of cutting edge co-conspirators who are leading the way to define and create the next generation of software development practices. 

### 2018 Core Content Strategy Statement

The content we produce helps increase awareness of GitLab’s complete and single application with the goal of broadening our market share and increasing sales by providing informative and persuasive content that makes DevOps teams feel excited, curious, and confident so that they can adopt & integrate industry best practices into their workflow. 

## Communication 

### Team:
- **Erica Lindberg, Content Marketing Manager** [@erica](https://gitlab.com/erica)
  - Area of focus: content and campaign strategy including webpages and webcasts
- **Rebecca Dodd, Content Editor** [@rebecca](https://gitlab.com/rebecca)
  - Area of focus: blog, newsletters, editorial calendar, and copyediting 
- **Emily von Hoffman, Jr. Content Editor** [@evhoffmann](https://gitlab.com/evhoffmann)
  - Area of focus: social marketing, live streams, and user generated content (UGC)

### Channels:
- **Chat:** please use the following slack channels `#content` for general inquiries, `#blog` for questions regarding blog content, and `#twitter` for questions about social.
- **Issue trackers:** 
  - [General Content Marketing](https://gitlab.com/gitlab-com/marketing/boards/104871)
  - [Blog posts](https://gitlab.com/gitlab-com/marketing/boards/353941)
  - [Webcasts](https://gitlab.com/gitlab-com/marketing/boards/356113) 
  - [Case studies](https://gitlab.com/gitlab-com/marketing/boards/361043) - jointly ownened with Product Marketing 
  - [Q4 OKRs](https://gitlab.com/gitlab-com/marketing/boards/377172?scope=all&utf8=%E2%9C%93&state=opened&milestone_title=Q4%202017&label_name[]=Content%20Marketing)

## Defining "Content"

“Content” is an incredibly broad and all-encompassing term. In it’s most simplistic 
form, content means something that has substance. Because “content” does not carry 
a universal definition, it’s important to clarify its meaning in the context of 
what it means for GitLab. 

At GitLab, we define content in two ways:

1. **Foundational Content:** Substance or material dealt with in speech and editorial distinct from its form or style. Foundational content is the basis for all company communications and consists of three pillars: organization, audience, and product.  
2. **Published Content:** Information made publically available digitally or in print for a defined audience. Published content is what we share to educate and engage our community, users, prospects, and customers. 

We can further define content by function:

### Content Marketing & Strategy
**The marketing technique of of creating and distributing targeted, relevant, and valuable content** to attract, acquire, and engage a clearly defined and understood target audience. The objective is to drive and enable profitable customer action. 

The role of the content marketing & strategy function is to determine the content strategy to build and grow targeted audiences through published content, and assist in the planning and execution of marketing campaigns. 

**This is currently the only operating content function at GitLab** 

### Content Operations
**The management and governance of content.** It includes aligning content to business goals, analysis and influences the development, production, evaluation, and sunsetting of content. The objective is to manage content as a strategic business asset. 

The role of the content operations function is to categorize, audit, and analyze content to ensure that content is being utilized to its maximum potential and to perform gap analysis to identify areas where there is a lack of useful content. 

**Checklist for good content:**

- Relevant 
- Useful
- User or customer-centered
- Clear, Consistent, Concise
- Supported

## Key Responsibilties 

At the highest level, Content Marketing is resposible for building awareness, trust, 
and preference for the GitLab brand with developers, engineers, and IT professionals. 

1. Audience development 
2. Editorial voice and style
3. Defining & executing the quarterly content strategy
4. Lead generation

## Campaigns<a name="campaigns"></a>
Leadgen is responsible for executing marketing campaigns for GitLab.  We define a campaign as any programmed interaction with a user, customer, or prospect.  For each campaign, we will create a campaign brief that outlines the overall strategy, goals, and plans for the campaign.

## Campaign brief process<a name="campaignbrief"></a>
To create a campaign brief, first start with the [campaign brief template](https://docs.google.com/a/gitlab.com/document/d/1GttZqr7sjuvP9kWuIPfbif2b2VyNJtbN8CbL4tKJX2Q/edit?usp=sharing).  Fill out all fields in the brief as completely as possible.  Certain fields might not be applicable to a particular campaign.  For example, an email nurture campaign leveraging text based emails won’t have a visual design component.  This field can be left blank in that example.

Once the campaign brief is filled out, create an issue in the GitLab Marketing project and link to the campaign brief.

On the GitLab issue, make sure to:
* Tag all stakeholders
* Use the Marketing Campaign label
* Set the appropriate due date (the due date should be the campaign launch date)
* If there are specific deliverables, create a todo list in the issue description for each stakeholder along with a due date

## Publishing a case study <a name="casestudy"></a>
To create a Case Study blog post, start by creating a `.yml` file in `/data/case_studies` directory under Marketing site repo. Keep the name of file same as company name (this is not mandatory but it is easier to manage), for eg; if company name is "Foobar", create a file as `/data/case_studies/foobar.yml`. Once created, add contents of the file using [this sample Case Study template](https://gitlab.com/gitlab-com/www-gitlab-com/snippets/1685439), and then update the values of each property based on case study details, remember, **do NOT change property names**. Once this file is added, you'll need to restart marketing site server by first closing it using `Ctrl+C` and then running `bundle exec middleman` again.

When the server is started, you can view generated Case Study blog post in your local instance of marketing site under the URL, for eg; `http://localhost:4567/customers/foobar`. Please note that you don't need to restart server again if you make any changes to `foobar.yml` file, this is required only when a **new** file is added to the `/data/case_studies` directory.

## Webcasts<a name="webcasts"></a>

Webcasts are one the greatest tools we have to communicate with our audience.
GitLab webcasts aim to be informative, actionable, and interactive.

### Best practices

1. Give yourself **at least** 15 days of promotion.
2. Send invitation emails 3 weeks out, 2 weeks out, 1 week out, and 2 hours before event.
3. Only send promotional emails Tuesday, Wednesday, or Thursday for optimal results.
4. Send reminder emails to registrants 1 week out, day before, and one hour before the event.
5. Host webcasts on a Wednesday or Thursday.
6. Post links to additional, related resources during the event.
7. Include "contact us" information at the end of the presentation.
8. Send the recording to all registrants, whether they attended or not.
9. Publish a post-webcast blog post capturing some key insights to encourage on-demand registrations.
10. Add webcast to the GitLab resources page.

### Speaker approval

The Lead Generation team depends on GitLab's subject matter experts to deliver webcast presentations. However, we must ensure that
when we ask a speaker to participate on a webcast that the work is approved. Please use the following process when asking someone outside of marketing
to participate on a webcast.

1. Have an abstract of the content prepared before asking for a presenter.
2. Send the abstract to both the proposed speaker and their manager to review. **A speaker is not considered booked unless they have approval from their manager.**
3. Address and resolve any concerns regarding the abstract.
4. Once the manager approves and the speaker accepts, you can move forward with the webcast.

### Tips for speakers

Here are some basic tips to help ensure that you have a good experience preparing for and presenting on a webcast.

#### Before committing
Ask us any questions you have about the time commitment etc. and what exactly our expectations are. Talk about it with your manager if you're on the fence about your availability, bandwidth, or interest. Make sure you're both on the same page. We want this to be a meaningful professional development exercise for you, not a favor to us that you're lukewarm about — if you feel that way, none of will be able to do our best job. We'll be honest with you, so please do the same for us.

#### Before the dry run
Select and set up your presentation space. Pick a spot with good wifi, and we recommend setting up an external mic for better audio quality, although this is optional. If you will be presenting from your home, alert your spouse/roommates of the time/date & ask them to be out of the house if necessary. Depending on your preferences and comfort level with public speaking, run through the script several times.

#### Before the presentation
Try to get a good sleep the night before, and, if the presentation is in the morning, wake up early enough to run through your notes at least once. Review our [Positioning FAQ](https://about.gitlab.com/handbook/positioning-faq/), or keep the page handy in case you are asked in the Q&A about how GitLab compares to our competitors.

### Logistical set-up

1. Create webcast in Zoom
   - Make sure the registration confirmation email and the reminder emails are set to send from Zoom. As Zoom implements their more robust Marketo integration, we will send from Marketo, but for now we need to send from Zoom to ensure that the correct unique link is sent to registrants.
1. Create the webcast program in Marketo
   - Title the webcast in the following format: `YYYYMMDD_{Webcast Title}`. For example, 20170418_MovingToGit
1. Update `My Tokens` at the webcast program level
   - DO NOT UPDATE THE `apiKey` or `apiSecret`. These should be the same for every webcast
   - Update the `{{my.zoomWebinarId}}` token with the webinar ID from the Zoom webcast created in step 1
   - Update the add to calendar tokens
      - Copy the Google Calendar link from the webinar page on Zoom
      - Update the information in the iCal and Outlook calendar files (these will be identical)
   - Update the event date and time
   - Update the email body with the description of the webcast
1. Turn on smart campaigns in Marketo
   - Activate the `Zoom Attended` campaign
   - Activate the `Webcast_Registered` campaign
   - Activate the `Registered From Zoom` campaign
   - Schedule the `Zoom Absent Attendees` campaign to run after the webcast will be finished (give the campaign a few hour buffer minimum)
1. Set up Marketo integration within Zoom
   - Log in to Zoom, and select the webcast from the `Webinars` tab
   - Scroll down and click on the `Integration` tab
   - Click `Edit` next to `Generate Leads in Marketo`
   - Turn on `Send registration information to a Smart Campaign` and select the `Registered From Zoom` smart campaign for the proper webcast program
   - Turn on `Send attendee information to a Smart Campaign` and select the `Zoom Attended` smart campaign for the proper webcast program
   - Select the `ZoomWebinarOtherInfo` custom object, check the following boxes, and select the corresponding Marketo Custom Object Fields:
      - Webinar ID
      - Webinar Topic
      - Q&A
      - Poll
1. Edit the landing page to have the appropriate webcast description, date, and time.
