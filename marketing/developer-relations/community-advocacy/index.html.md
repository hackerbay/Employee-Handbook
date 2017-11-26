---
layout: markdown_page
title: "Community Advocacy"
---

## Finding the Community Advocates

- [**Public Issue Tracker**, as part of the Marketing team](https://gitlab.com/gitlab-com/marketing/issues/); please use confidential issues for topics that should only be visible to team members at GitLab.
- [**Support Issue Tracker**, issues filtered to *Community*](https://gitlab.com/gitlab-com/support/issues?label_name%5B%5D=Community+); please use this issue tracker for community related issues only.
- [**Chat channel**](https://gitlab.slack.com/messages/community-advocacy); please use the `#community-advocacy` chat channel for questions that don't seem appropriate to use the issue tracker for.

## On this page
{:.no_toc}

- TOC
{:toc}

----

## <i class="fa fa-book fa-fw icon-color font-awesome" aria-hidden="true"></i> Community Advocate Resources

- Community Advocate Onboarding
  - [Onboarding Checklist](/handbook/marketing/developer-relations/community-advocacy/onboarding/checklist/)

----

## Role of Community Advocacy

## Goal

The goal of community advocacy is to grow the number of active GitLab contributors.
We do this by increasing conversion in the [contributor journey](https://about.gitlab.com/handbook/journeys/#contributor-journey).

## Plan

1. Order, expense, and read the Art of Community by Jono Bacon (Added to CA Bootcamp)
1. Finish [Features in one yaml](https://gitlab.com/gitlab-com/www-gitlab-com/issues/1334) (Connor)
1. Add diversity events to [event list](https://about.gitlab.com/events/) mentioning that we sponsor it but don't attend (Matija)
1. Reinstate the [webstore](https://gitlab.myshopify.com/) with Art if not done already (Matija)
1. Have discount codes that are easily distributed by team members (maybe ChatOps?) (Matija)
1. Sent the MVP a quirky gift
1. Sent every major contributor a personalized gift
1. Host online sessions for code and docs contributors
1. Start keeping track of our core contributors
1. Do the rest of the [contributor journey](https://about.gitlab.com/handbook/journeys/#contributor-journey)

## Vision

1. GitLab has 1000's of active core contributors
1. Being a core contributor is a very rewarding experience
1. There are 10's of active GitLab/[ConvDev](http://conversationaldevelopment.com/) meet-ups
1. 100's of talks per year given on conferences and meetups
1. Our most active core contributors come to our summits
1. 100's of people contribute to the code and docs every month
1. We use software that helps us to keep track of core contributors (can be forum, Highrise, software made for advocacy, or a custom Rails app)
1. There is a core contributors page organized per region with the same information as the [team page](https://about.gitlab.com/team/) and what they contributed, where they work (if they have a linkedin profile), and a button to sent them an email via a form.
1. We measure and optimize every step of the [contributor journey](https://about.gitlab.com/handbook/journeys/#contributor-journey)

## Respond to every community question about GitLab asked online

- This includes helping members of the community with _their_ questions, but also making sure that the community is heard and that the feedback from the community reaches the rest of the team at GitLab.
- Engage with the developer community in a way that is direct but friendly and authentic. Be able to carry the tone of the GitLab brand while also giving the proper answers or direction to members of the community.
- Help update the [social media guidelines](/handbook/marketing/social-media-guidelines/) and GitLab voice as new situations arise.
- Work with leadership to find a way to track and measure response time across all channels with the ideal response time being under 1 hour for all channels by the end of Q1, 2017.
- Explore different tools from Zendesk to Mentions to find a way to track all mentions of GitLab across the internet.
- Don’t be afraid of animated gifs and well-placed humor! We are not robots.
- Work within the GitLab process to help users report bugs, make feature requests, contact support, and provide feedback to the product.

## Community Interaction Archetypes

### Stability Complaints

- Apologize for the inconvenience
- Search for an active issue that could be the cause of instability (deployment downtime, load spikes, ...)
    - [Sentry](https://sentry.gitlap.com/gitlab/)
    - [Infrastructure Issue Repository](https://gitlab.com/gitlab-com/infrastructure/issues/)
    - [`production`](https://gitlab.slack.com/messages/production) Slack channel
- Determine if the user is still affected
- Link to the relevant issue

### Feature Requests

- Analyze the request
- Open an issue for it
- Thank the user for the contribution (See [our Social Media Guidelines](/handbook/marketing/social-media-guidelines/))
- Link back to the the community member to provide further feedback in the issue

### General Questions / Issues with .com

- Gauge the complexity of the question
- Search related issues / documentation
    - [GitLab CE Issues Tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues/)
    - [GitLab Documentation](http://docs.gitlab.com/)
- Forward to [GitLab Support Forum](https://gitlab.com/gitlab-com/support-forum/issues/)

### Bug Reports

- Reproduce the bug
- Open an issue
    - [GitLab CE Issues Tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues/)
    - Label the issue
- Link back to the community member
- (Optional) Link in the appropriate chat channel

### Others

- Mention -> Use the `Mention` ZenDesk macro
- EE Customer issues / GitHost customers -> Forward to support
- 2FA reset queries -> Forward to support
- Non-English Tweets -> Use the `Non-English` ZenDesk macro
- Any kind of political questions / remark (even if they're just asking if we're politically neutral or not) -> Do not respond (They tend not to be productive.)

### Special Types

- Event Sponsorship Requests -> Forward to [emily@gitlab.com](mailto:emily@gitlab.com)
- Spam -> Mark as spam
- GitLab package reported as compromised -> [immediately stop packagecloud via Slack](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/stop-or-start-packagecloud.md)

### Notes / Remarks

- When asking something in chat that's relevant for a ticket, leave a link to the chat message as an internal comment in the ticket
- Always be sure to check if an issue (bug or feature proposal) exists before opening one / asking a user to open it

## Mentions

The [#mentions-of-gitlab](https://gitlab.slack.com/messages/mentions-of-gitlab/) chat channel tracks mentions of GitLab across multiple sources. This allows us to respond to user requests across various platforms.

We currently track the following sources for GitLab mentions:

1. Product Hunt
2. Tumblr
3. Hacker News
4. Reddit

These mentions get piped to the Slack channel by [notify.ly](https://notify.ly/).

All comments on our [blog posts](/blog/) and any mention of GitLab on [Lobsters](https://lobste.rs/) also gets funneled to this channel using [zapier](https://zapier.com/).

## Specific channels

Respond to the GitLab community across the following channels in a timely manner:

- Hacker News
- Disqus
- Twitter (via Zendesk)
- Mailing List
- `community@gitlab.com` email
- Facebook
- [forum.gitlab.com](https://forum.gitlab.com)
- StackOverflow
- Reddit
- YouTube
- Quora
- Google alerts
- Comments on news stories in the media, and ....
- .... more.

### Hacker News

Respond to GitLab mentions on HackerNews. These get piped into the `#mentions-of-gitlab` chat channel.

When responding to a post about GitLab on HackerNews:

* Leave a link to the thread in `#devrel` and ping other `@advocates`
* See [Involving Experts](#involving-experts) below
* Don't post answers that are almost the same, link to the original one instead
* Address multi-faceted comments by breaking them down and using points, numbering and quoting

### Disqus

All the comments from our blog are handled by Disqus. There's an integration with ZenDesk in place which pipes posts to ZenDesk as tickets.

Go through the tickets per-post, see if all comments have received responses, respond if any need responses, then mark all the relevant tickets as Solved.

### Twitter

Tweets that mention [@GitLab](https://twitter.com/GitLab), or [@GitLabStatus](https://twitter.com/GitLabStatus) will create a ticket in Zendesk, and show up in the "Twitter" view. All responses should be sent from Zendesk.

If a tweet is responded to from TweetDeck, this risks duplicate responses. Responding from Zendesk also enables us to track our response times vs. [our internal SLA](/handbook/support/#sla).

Reply to almost all tweets, following the [social media guidelines](/handbook/marketing/social-media-guidelines/), and the guidelines on [representing GitLab on Twitter](/handbook/marketing/developer-relations/developer-advocacy/#representing-gitlab-on-twitter) regardless of whether the tweet is of a technical nature or not. Follow up with the support team if the issue is too complex to handle.

#### General

- Tweets use short links which require you to visit that link to make sure you understand the context.
- Clarify if the request refers to GitLab or an externally hosted GitLab instance as we can only handle requests for [GitLab.com](https://gitlab.com).

When resolving Twitter tickets you should:

1. Use [Play mode](https://support.zendesk.com/hc/en-us/articles/203690856-Working-with-tickets#topic_avj_hfg_vt) in the Twitter view. The default Twitter view will sort tickets by created date (ascending).
1. Not skip any tickets
1. Assign the ticket to yourself or ask in the appropriate chat channel if you don't know how to answer it
1. Not cross assign tickets

#### Handles

- The [@GitLabStatus](https://twitter.com/GitLabStatus) account should only be used to give updates on the availability of [GitLab.com](https://gitlab.com) and to follow up on users reporting that [GitLab.com](https://gitlab.com) is unavailable or responding to a previous availability update on [@GitLabStatus](https://twitter.com/GitLabStatus).
- When a tweet mentions 1 or more of the handles described above, it should be replied to from the main handle ([@GitLab](https://twitter.com/GitLab)
- If a wrong handle is used in a response, take note and respond from the correct one in the follow-up (if there is one)
- [@GitLabSupport](https://twitter.com/GitLabSupport) is [a deprecated handle](https://gitlab.com/gitlab-com/support/issues/253) and should not be used

#### Usage of likes

Use "Likes" on Twitter for promoting positive feedback about our product since we direct users there when we want to show that people really love the product. Avoid using it for anything else.

### Mailing list

Respond to questions on the [GitLab Mailing List](https://groups.google.com/forum/#!forum/gitlabhq).

### community@ email

Respond to email sent to our `community@` address.

### Facebook

Messages sent to our [Facebook page](https://www.facebook.com/gitlab/) also feed into ZenDesk.

### GitLab Forum

Questions from the [GitLab Forum](https://forum.gitlab.com/) flow into ZenDesk, but can only be responded to from within the Forum environment.

### Stack Overflow

The [Stack Overflow tagged questions](https://stackoverflow.com/questions/tagged/gitlab) that relate to GitLab flow into Zendesk, but can only be responded to from within Stack Overflow.

After you create an account on [Stack Overflow](http://stackoverflow.com/) (if you don't already have one), you should start by answering a few simple questions in an area you're familiar with (a language, web framework, development platform, API, etc.) or in the GitLab tag(s) if you feel comfortable. The goal is to get enough ["Reputation"](http://stackoverflow.com/help/whats-reputation) and have access to a few more features.

Consider offering some of your Reputation using [bounties](http://stackoverflow.com/help/bounty) if a question is particularly advanced and you don't believe you can answer yourself, and the question seems deserving of an answer (e.g. if it has lots of upvotes).

### Reddit

Respond to mentions of GitLab on Reddit, especially ones in the [GitLab Subreddit](https://www.reddit.com/r/gitlab/).

### YouTube

Repond to comments made on the [GitLab Youtube Channel](https://www.youtube.com/channel/UCnMGQ8QHMAnVIsI3xJrihhg).

### Quora

Respond to questions about GitLab on Quora, especially the ones that appear in the [GitLab Topic channel](https://www.quora.com/topic/GitLab/).

## Involving Experts

When responding to community messages, you should always strive to involve a resident GitLab expert on the subject if possible.

This gives:

* a higher quality of answers
* shows that our whole company is comitted to helping people
* the expert more feedback from users

Please ping the expert in the relevant channel (e.g. in `#frontend` if it's a frontend question) with:

```plain
@expert_username [LINK TO COMMUNITY COMMENT] https://about.gitlab.com/handbook/marketing/developer-relations/community-advocacy/#can-you-please-respond-to-this?
```

And add an internal note with the link of the Slack message to the associated Zendesk ticket. If there is no Zendesk ticket related to the mention (e.g.a HackerNews mention) track it in the `#devrel` channel.

## Can you please respond to this?

You got a link to this because we'd like you to respond to the mentioned community comment. We want to make sure we give the best answer possible by connecting the wider community with our experts and expose you to more community feedback.

When responding to community mentions, you should check out the [social media guidelines](https://about.gitlab.com/handbook/marketing/social-media-guidelines/).

If you can't respond to the linked comment, that's OK, but please quickly let the person who pinged you know so they can ping someone else.

## Release Post Calendar Planning

Block off your calendar to anticipate for release posts. They occur regularly every 22nd in the month, just like each GitLab release.

## MVP Appreciation Gifts

1. Determine MVP after merge window closes
1. Find MVP's contact information
  * An email address is usually stored in git commit data
  * A user might have email or twitter info on his profile
1. Investigate the MVP's interests
1. Choose a suitable gift (up to 200$ USD)
1. Send the gift
  * The MVP should have the gift 48h before the post goes live
1. Verify shipment status
  * Make sure that it was sent
  * Make sure that it arrived
1. Mention the MVP gift in the release post
  * Make sure there's a picture of the gift in the release post

## Good Custom Swag Providers

|Provider|Website URL|Example Pricing|Note|
|:-:|:-:|:-:|:-:|
|CustomInk|[CustomInk](https://customink.com)|[T-Shirt Pricing](https://www.customink.com/products/categories/short-sleeve-t-shirts/16/styles)||
|RageOn|[RageOn](https://www.rageon.com)|[Product Pricing](https://connect.rageon.com/prices/product)||

## Handling the `#swag` channel

Handle swag requests made in the `#swag` channel.

### Requester

Here's the process for requesting a swag gift for a contributor/user/customer:

* Leave a message in the `#swag` channel with
  * URL to blog post, tweet, etc.
  * *(Optional)* Name
  * *(Optional)* Email
  * *(Optional)* Shipment Address
  * *(Optional)* Items requested (with sizes if you know them)

Request templates:

* Minimal
```plain
https://twitter.com/gitlab/status/884983979992121344
```

* Partial
```plain
https://twitter.com/gitlab/status/884983979992121344 - John Doe - email@example.com
```

* Maximum
```plain
https://twitter.com/gitlab/status/884983979992121344 - John Doe - email@example.com - 1233 Howard St 2F, CA, USA - 1 x L T-Shirt & 2 large stickers
```

_NOTE:_ If you don't specify which swag to send, we'll send a standard package (T-Shirt + 2 stickers)
_NOTE:_ Please keep a single swag request confined to one message to avoid clutter

### CA

* Reach out to the swag recepient
  * Thank him for his work/support
  * Gather the missing info needed for fulfilling the swag drop ship
* Fulfill the swag shipment in Printfection
  * If items are specified
    * Create a new drop ship
    * Add items
    * Fill shipment info
  * If no items are specified
    * Take an unused giveaway link from [the community swag giveaway spreadsheet](https://docs.google.com/a/gitlab.com/spreadsheets/d/1LiRTSTHnF_NGyEPlqeRMUBi5cpffCHgMK8K0wAvVD4E/edit?usp=sharing)
    * Mark the link as redeemed by entering the date in the `Redeemed` column
* Notify the recepient that the drop ship has been created or send him a giveaway link
* Comment to the requester in a thread, notifying that the swag request has been fulfilled

_NOTE:_ Please keep in mind the [list of countries we do not do business in](https://about.gitlab.com/handbook/sales-process/images_sales_process/#export-control).

## Diversity Sponsorship

* We offer a $500 [sponsorship](https://about.gitlab.com/2016/02/02/gitlab-diversity-sponsorship/) to any group that aims to improve diversity in tech
* We receive requests through the [community sponsorship form](https://about.gitlab.com/community/sponsorship/)
* After receiving the request for sponsorship, create a merge request adding them to the [events list](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/events.yml)
* After creating the MR, ask them to send an invoice to Accounts Payable (ap@gitlab.com) with the link of the MR for verification
  * After they send it, the amount will be sent via direct deposit
* If we have a team member in the location of the event, alert them so they have the option to attend
* After we have committed to sponsor the event, [schedule a tweet](https://about.gitlab.com/handbook/marketing/social-marketing/#event-promotion) announcing our involvement and add the amount to the marketing budget spreadsheet

_NOTE:_ Please keep in mind the [list of countries we do not do business in](https://about.gitlab.com/handbook/sales-process/images_sales_process/#export-control).

## Sample Daily Workflow

1. [ZenDesk](https://gitlab.zendesk.com):
    1. Go through the recommended Disqus view
    1. Go through the recommended Twitter view
    1. Go through the recommended Facebook view
1. Go through the [GitLab Forum](https://forum.gitlab.com/), answering all relevant tickets
1. Go through [StackOverflow GitLab tagged questions](https://stackoverflow.com/questions/tagged/gitlab), answering them
1. Go through the [GitLab Subreddit](https://www.reddit.com/r/gitlab/), answering all relevant tickets
1. Handle ToDos
1. Rinse and Repeat ↻

## Relevant Links

- [Social Media Guidelines](/handbook/marketing/social-media-guidelines/)
- [Support handbook](/handbook/support/)
