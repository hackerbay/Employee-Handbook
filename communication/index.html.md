---
layout: markdown_page
title: "GitLab Communication"
extra_js:
  - libs/moment.min.js
  - libs/moment-timezone-with-data.min.js
  - team-call.js
---

## On this page
{:.no_toc}

- TOC
{:toc}

We're a **distributed**, **remote-only** company where people work remotely without missing out.
For this, we use **asynchronous communication** and are as open as we can be by communicating through public issues, chat channels,
and placing an emphasis on ensuring that conclusions of offline conversations are written down.
These communication guidelines are meant to facilitate smooth communication in an
ever-growing remote-only company.
Please keep in mind that you represent GitLab and our culture, also on Social Media.
When commenting on posts please keep in mind: "Don't argue but represent."

### GitLab Workflow

#### Everything starts with an issue

1. Always **create** an issue for things you work on. If it is worth spending time on, it is worth creating an issue since that enables other people to learn and help. You can always edit the description or close it when the problem changed to something different or was solved.
1. If a user suggests an enhancement, try and find an existing issue that addresses their concern, or create a new one. Ask if they'd like to elaborate on their idea in one of these issues.
1. **Double link** issues to prevent internal confusion and us failing to report back to the reporters. For example, open an issue with a link to ZenDesk and close the issue with a copy of the response. Or add "Report: " lines to the description with links to relevant issues and feature requests and ensure they are closed and note this with a comment. If you are not responsible for reporting back please do not close an issue, instead re-assign it.
1. If two issues are related, **crosslink** them (a link from each issue to the other one). Put the link at the top of each issue's description with a short mention of the relationship (Report, etc.). If there are more than 2 issues, use one issue as the central one and crosslink all issues to this one. Please, also crosslink between ZenDesk and GitLab issues.
1. After a discussion about a feature **update the issue body** with the consensus or final conclusions. This makes it much easier to see the current state of an issue for everyone involved in the implementation and prevents confusion and discussion later on.
1. Submit the **smallest** item of work that makes sense. When creating an issue describe the smallest fix possible, put suggestions for enhancements in separate issues and link them. If you're new to GitLab and are writing documentation or instructions, submit your first merge request for at most 20 lines.
1. Do not leave issues open for a long time, issues should be **actionable** and realistic. If you are assigned to an issue but don't have time to work on it, assign it to someone else.
1. Make a conscious effort to **prioritize**<a name="prioritize"></a> your work. The priority of items depends on multiple factors: Is there a team member waiting for the answer? What is the impact if you delay it? How many people does it affect, etc.? This is detailed in [Engineering Workflow](/handbook/engineering/workflow).
1. Use the public issue trackers on GitLab.com for everything since [we work out in the open](https://about.gitlab.com/2015/08/03/almost-everything-we-do-is-now-open/). Issue trackers that can be found on the relevant page in the handbook and in the projects under [the gitlab-com group](https://gitlab.com/gitlab-com/).
1. Pick issues from the current [milestone](https://gitlab.com/groups/gitlab-org/milestones).
1. We try not to assign issues to people but to have people **pick issues** in a milestone themselves.
1. Assign an issue to yourself as soon as you start to work on it, but not
  before that time. If you complete part of an issue and need someone else to
  take the next step, **re-assign** the issue to that person.
1. When re-assigning an issue, make sure that the issue body contains the latest information. The issue body should be the **single source of truth**.
1. When working on an issue, **ask for feedback** from your peers. For example, if you're a designer and you propose a design, ping a fellow designer to review your work. If they approve, you can move it to the next step. If they suggest changes, you get the opportunity to improve your design. This promotes collaboration and advances everyone's skills.
1. We keep our **promises** and do not make external promises without internal agreement.
1. Do not close an issue until it is **[done][d-o-d]**.
1. When **closing** an issue leave a comment explaining why you are closing the issue.

[d-o-d]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#definition-of-done

#### Implement it with a merge request

Merge request guidelines for all contributors are described in our [Contribution
guide][mr-guidelines].

Code review guidelines for reviewers and maintainers are described in our [Code
Review Guidelines][code-review-guidelines].

Following are additional guidelines for GitLab Inc. team
members:

1. Even when something is not done, share it internally so people can comment
  early and prevent rework. Create a **[Work In
  Progress](https://about.gitlab.com/2016/01/08/feature-highlight-wip/)** merge request so it is not merged by accident.
1. If any followup actions are required on the issue after the merge request is
  merged (like reporting back to any customers or writing documentation), avoid
  auto closing it.
1. When _you_ are done with your merge request, remove the "WIP" prefix and
  follow the [Code Review Guidelines][code-review-guidelines].
1. You can still make changes based on feedback of course, but by removing the
  "WIP" prefix it clarifies that the main body of work has been completed.

[mr-guidelines]: https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#merge-request-guidelines
[code-review-guidelines]: https://docs.gitlab.com/ce/development/code_review.html

### Internal Communication

1. All written communication happens in English, even when sent one on one,
because sometimes you need to forward an email or chat.
1. Use **asynchronous communication** when possible (issues and email instead of chat)
1. Issues are preferred over email, email is preferred over chat, announcements happen on the team call agenda, and [people should be able to do their work without getting interrupted by chat](https://m.signalvnoise.com/is-group-chat-making-you-sweat-744659addf7d#.21t7089jk).
1. To use email instead of chat it is OK to send an _internal_ email that contains only a short message, similar as you would use in chat. Save time by not including a salutation like 'Hi Emma,' and first write the subject of the email which you copy and paste into the body. You are not expected to be available all the time. It is perfectly fine to respond to emails and chat mentions until your planned work hours.
1. Sometimes synchronous communication is the better option, but do not default
to it. See the [guidelines on video chats](#video-calls) for more detail.
1. It is very OK to ask as many questions as you have, but ask them so many
people can answer them and many people see the answer (so use issues or public
chat channels instead of private messages or one-on-one emails) and make sure
you try to document the answers.
1. If you mention something (a merge request, issue, commit, webpage, comment,
etc.) please include a link to it.
1. All company data should be **shareable** by default. Don't use a local text
file but rather leave comments on an issue.
1. When someone asks something give back a deadline or that you did it. Answers like: 'will do', 'OK', 'it is on my todo list' are not helpful. If it is small is better to spend 2 minutes and do the tasks so the other person can mentally forget about it. If it is large you need to figure out when you'll do it, by returning that information the other person might decide to solve it in another way if it takes too long.

### Email

1. Send one email per subject as multiple items in one email will cause delays
(have to respond to everything) or misses (forgot one of the items).
1. Always reply to emails, even when no action is needed. This lets the other
person know that you received it. A thread is done when there is a single word
reply, such as OK, thanks, or done.
1. If you forward an email without other comments please add FYI (for your
information), FYA (for your action), or FYJ (for your judgment). If you forward an external request with FYJ it just means the person who forwarded it will not follow up on the request and expects you to decide if you should follow up or not.
1. Email forwarding rules are specified in the shared _GitLab Email Forwarding_ Google Doc accessible only to people in the company. If you want to be added or removed from an internal alias (for example, "sales@gitlab.com"), change a rule, or add a forwarding email alias, please [suggest an edit](https://support.google.com/docs/answer/6033474?hl=en) in the doc.
1. Emails are asynchronous, for example, if your manager emails you on a weekend it is fine to reply during the workweek.
1. If an email is or has become urgent feel free to ping people via chat referencing the subject of the email.

### Chat

1. If you use chat please use a public channel whenever possible, mention the
person you want to reach if it is urgent. This ensures it is easy for other people
to chime in, and easy to involve other people, if needed.
1. In chat try to keep the use of keywords that mention the whole channel to a
minimum. They should only be used for pings that are both urgent and important,
not just important. By overusing channel mentions you make it harder to respond
to personal mentions in a timely manner since people get pinged too frequently.
If something is urgent and important:
   * Use `@here` to notify all currently _active_ members in the room.
   * Use `@channel` to notify _ALL_ members in the room, irrespective of away status.
1. If something is important but not urgent - like complimenting or encouraging the
entire team - use email or post in the channel without `@`-mentioning the team.
1. If you agree in a chat to start a video call (typically by asking "Call?")
the person that didn't leave the last comment starts the call. So either respond
to the "Call?" request with a video link or say "Yes" and let the other person
start it. Don't say "Yes" and start a call 5 seconds later since it is likely
you'll both be creating a video call link at the same time.
1. The usage of ChatBots for integrations can sometimes depend upon the name of the chat room. You should consult the room about such integrations before changing the name of commonly used / popular rooms in order to avoid inadvertently breaking integrations.

### Google Docs

1. Never use a Google Doc / Presentations for something non-confidential that has to end up on the website or the **handbook**. Work on these edits via commits to a merge request. Then link to the merge request or diff to present the change to people. This prevents a duplication of effort and/or an out of date handbook.
1. If you _do_ need a Google Doc, create one with your company G Suite (formerly Google
Apps) account. By default, share it with the whole company using the _Anyone at GitLab can find and access_ link sharing permission
and the _Anyone within GitLab can edit_ access permission (preferred) or the _Anyone within GitLab can comment_ access permission.
Easily do this by creating Google Docs within a Shared Folder in Google Drive.
1. When referring to a Google Doc in the handbook, refrain from directly linking it. Instead, indicate the name of the doc.
(In the past, linking a Google Doc has led to inadvertently opening the sharing settings beyond what was intended.)
This also helps prevent spam from people outside GitLab requesting access to a doc when clicking its link.
1. If you are having trouble finding a shared Google Doc, make sure you [Search &lt;your domain&gt;](https://support.google.com/a/answer/3187967?hl=en) in Google Drive.
1. In our handbook, if you find yourself wondering whether it is better to provide a public link to a Google Doc vs. writing out the content on the website, use the following guideline: Is this document frequently adapted / customized? If yes, then provide a link, making sure that the document can be _commented on_ by _anyone_ with the link. For instance, this is how we share our employment [contracts](/handbook/contracts/). If the document is rarely customized, then provide the content directly on the site and deprecate the Google Doc.

### Presentations

1. All presentations are made in Google Slides using our template named 'GitLab-Deck-Template-Light'.
1. The title of every slide should be the message you want the audience to take away, not the subject matter. So use 'Our revenue more than doubled' instead of 'Revenue growth'.

### Say Thanks

1. Thank people that did a great job in our "Thanks" chat channel. If someone is
a team member just @ mention them. If multiple people were working on something
try mentioning each person by "@name". "Thanks everyone" does not say much.
1. To thank someone who is not a team member, mention your manager, our People Ops Coordinator, the name of the person, a quirky gift
and link to their work. For example, "@manager, @peopleopscoordinator: Joe deserves a lawnmower for _link_".
With your manager's blessing, the People Ops Coordinator will approach the person in question for their address saying we want to send
some swag. We'll ship it in gift wrap with "Thanks for your great work on _link_, love
from @gitlab".
1. Don't thank the CEO or other executives for something that the company paid for, thank GitLab instead.

### Not sure where to go?

If there is something that you want to discuss, but you do not feel that it is
a reasonable option to discuss with either your manager or CEO, then you can reach
out to any of the other C-level GitLabbers or our board member Bruce Armstrong.

### Team Call

1. Schedule
   * PST: <span id="main-PST"></span>
   * UTC: <span id="main-UTC"></span>
   * <span id="main-abbr"></span>: <span id="main-USER"></span>
1. APAC schedule
   * PST: <span id="apac-PST"></span>
   * UTC: <span id="apac-UTC"></span>
   * <span id="apac-abbr"></span>: <span id="apac-USER"></span>
1. Everyone at GitLab is invited to the team call.
1. There is an additional makeup team call on Fridays where anyone who missed their weekend update can share what they have been up to. Optionally, team members can share an update if they feel so inclined. Please add your name to the list for that day.
1. We also have a team call for GitLabbers in the APAC region to share their weekend update. This call will also be recorded so the rest of the team can see what their colleagues have been up to! Everyone is encouraged to join this call as well, but it is not mandatory.
1. Every last Friday of the month we have an AMA to talk about anything our team is thinking about.
1. We use [Zoom](https://gitlab.zoom.us) for the call since Google Hangouts is capped at 15 people (please be sure to mute your microphone). The link is in the calendar invite and also listed at the top of the team agenda Google Doc called _Team Agenda_.
1. The call is recorded automatically, and all calls are transferred every hour to a Google Drive folder called "GitLab Videos". There is a subfolder called "GitLab Team Call", which is accessible to all users with a GitLab.com e-mail account.
1. We start on time and do not wait for people.
1. The person who has the first item on the agenda starts the call.
1. If you are unable to attend just add your name to the team agenda as "Not attending".
1. We start by discussing the subjects that are on the agenda for today.
   * Everyone is free to add subjects. Please start with your name and be sure to link to an issue, merge request or commit if it is relevant.
   * When done with a point mention the subject of the next item and hand over to the next person.
   * When someone passes the call to you, no need to say, “Can you hear me?” Just begin talking. If we can’t hear you, we’ll let you know.
1. New team members should connect to their first team call 10 minutes before the call starts to make sure Zoom, your camera, and your microphone are all working properly. The new team member's manager will introduce them and ask the following questions: "Tell us about where you were before GitLab, why you wanted to join our team, and what you like to do in your spare time."
1. We ask 15-20 people per day to share updates about the most exciting thing from your past or upcoming week/weekend. If anyone has something they'd like to talk about, last person in the list will ask the group if they have anything else to share. The team agenda lists who is meant to speak on which day; this can be altered daily if conflicts arise.
1. There is no need to excuse yourself with "I didn't do anything interesting", "I just watched television" or "That's all". It is not a competition. Instead share the most interesting detail, for example what television show you watched, book you are reading, video game you played, or what you ate. More mundane subjects are things other team-members can relate to more.
1. The sequence of asking people is in a random order where each team member is assigned a day. Since we are growing rapidly, GitLabbers share their weekend update every two weeks. Days are split into group A and group B, which alternates depending on the week. People Ops will denote on the agenda which group will share that day. New GitLabbers will share every week for the first three months on Wednesdays. If there are non-team page people in the call we end with those.
1. It is OK to talk over people or interrupt people to ask questions, cheer for them or show your compassion. This encourages more conversation and feedback in the call.
1. Please look if the person you hand over to is present in the participant list so you don't hand over to someone who is not present.
1. The last person wishes everyone a good day.
1. Even if you cannot join the call, consider reviewing the recorded call or at minimum read through the team agenda and the links from there. We often use the team call to make announcements or discuss changes in processes, so make sure to catch up on the news if you have missed a team call (or more).

### Release Retrospectives and Kickoffs
{: #kickoffs}

After GitLab releases a new version on the 22nd of each month, we have a
30-minute call on the next business day reflecting on what could have been
better:

1. What went well this month?
2. What went wrong this month?
3. What could we have done better?

We spend the first part of the retrospective meeting reviewing the action
items from the previous month.

After the retrospective meeting is done, we launch immediately into the
kickoff meeting. The product team and other leads will have already have had
some discussion in a [meta issue on the GitLab.com CE
tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&state=opened&label_name=meta)
on what should be prioritized for each release. The purpose of this kickoff is
to get everyone on the same page and to invite comments.

We will post the recordings of the kickoff and retrospective to YouTube and
share the notes publicly.

### Random Chat and Room
{: #random-room}

1. The [#random](https://gitlab.slack.com/archives/random) chat channel is your go-to place to share random ideas, pictures, articles, and more. It's a great channel to check out when you need a mental break.
1. Come hang out any time in the **random room**, an open Google Hangout video chat where anyone with a GitLab email address can come and leave as they please. The link is in the description of the `#random` chat channel; consider bookmarking it. This room is open for all and should be distinct from the [Coffee Break Calls](https://about.gitlab.com/handbook/working-remotely/#coffee-break-calls), which are 1x1 conversations between teammates.

### Scheduling Meetings

1. If you want to ask GitLabbers if they are available for an event please send a new calendar appointment from and to the company address. This makes it easier for people to check availability and to put on their calendar. It automatically shows up on calendars even when the email is not opened. It is easier to signal presence and to see the status of everyone. Please respond quickly to invites so people can make plans.
1. Every scheduled meeting should either have a Google Presentation (for example for functional updates that don't require participation) or a Google Doc (for most meetings) linked. If it is a Google Doc it should have an agenda, including any preparation materials (can be a presentation). Put the agenda in a Google Doc that has edits rights for all participants (including people not part of GitLab Inc.). Link the Google Doc from the meeting invite. Take notes of the points and todos during the meeting. Nobody wants to write up a meeting after the fact and this helps to structure the thought process and everyone can contribute. Being able to structure conclusions and follow up actions in realtime makes a video call more effective than an in-person meeting. If it is important enough to schedule a meeting it is important enough to have a Doc linked. If we want to be on the same page we should be looking at that page.
1. If you want to check if a team member is available for an outside meeting, create a calendar appointment and invite the team member only after they respond yes. Then invite outside people.
1. When scheduling a call with multiple people, invite them using a Google Calendar that is your own, or one specific to the people joining, so the calendar item
doesn't unnecessarily appear on other people's calendars.
1. If you want to move a meeting just move the calendar appointment instead of reaching out via other channels. Note the change at the top of the description.
1. Please click 'Guests can modify event' so people can update the time in the calendar instead of having to reach out via other channels. You can install [the Google-Calendar-Guests-Can-Modify-Event-By-Default plugin in Chrome](https://github.com/robin-drexler/Google-Calendar-Guests-Can-Modify-Event-By-Default) to do this automatically.
1. If you want to schedule a meeting with a person not on the team please use [Calendly](handbook/tools-and-tips/#calendly).
1. When scheduling a meeting we value people's time and prefer the "speedy meetings" setting in our Google Calendar. This gives us meetings of, for example, 25 or 50  minutes leaving some time to write notes etc before continuing to our next call or meeting. (This setting can be found under the calendar Settings menu at "default event duration")
1. When creating a calendar event that will be used company wide, please place it on the GitLab Availability Calendar. That way the event is easily located by all individuals.
1. When you need to cancel a meeting, make sure to delete/decline the meeting and choose the option **Delete & update guests** to make sure everyone knows you can't attend and don't wait for you.

### Video Calls

1. Use video calls if you find yourself going back and forth in an issue/via email
or over chat. Rule of thumb: if you have gone back and forth 3 times, it's time
for a video call.
1. Having pets, children, significant others, friends, and family visible during
video chats is encouraged. If they are human, ask them to wave at your remote
team member to say "Hi".
1. We prefer [Zoom](https://gitlab.zoom.us/).
1. For meetings that are scheduled via calendar there is automatically a Google Hangouts URL added. This is the meeting place. Having a url in advance is much more reliable than trying to call via Hangouts as the meeting start.
1. Google Calendar also has a [Zoom plugin](https://chrome.google.com/webstore/detail/zoom-scheduler/kgjfgplpablkjnlkjmjdecgdpfankdle?hl=en-US) where you can easily add a Zoom link for a video call to the invite
1. For meetings that are scheduled with Zoom, make sure to take out the Google Hangouts link to avoid confusion.
   1. If you need more privileges on Zoom (longer meeting times, more people in the meeting, etc.), please contact People Ops as described [specifically for Zoom](/handbook/tools-and-tips/#sts=Zoom).
   1. Note that if you select to record meetings to the cloud (setting within Zoom), they will be automatically placed in the GitLab Videos folder in Google Drive on an hourly basis. You can find these videos in Google Drive by entering in the search bar: `title:"GitLab Videos" source:domain`.
   1. Note also that after a meeting ends, Zoom may take some time to process the recording before it is actually available. The sync to Google Drive happens on the hour mark, so if the recording is not available, it may take another hour to be transferred.
1. Use a headset with a microphone, [Apple Earpods](https://www.apple.com/shop/accessories/all-accessories/headphones-speakers) are great. Do not use computer speakers, they cause an echo. Do not use your computer microphone, it accentuates background noise. If you want to use your [Bose headphones](https://www.bose.com/en_us/products/headphones/noise_cancelling_headphones.html) that is fine but please ensure the microphone is active.
1. Consider using a utility to easily mute/unmute yourself, see [Shush](/handbook/tools-and-tips/#shush) in the tools section.
1. In video calls everyone should own a camera and a headset, even when they are in the same room. This helps seeing and hearing the person that is talking. It also allows people to easily talk and mute themselves. Using a headset also prevents echo. You wouldn't share an office seat together, so don't share your virtual seat at the table.
1. We start on time and do not wait for people. People are expected to join no later than the scheduled minute of the meeting (before :01 if it is scheduled for :00). The question 'is everyone here' is not needed.
1. We end on the scheduled time. It might feel rude to end a meeting, but you're actually allowing all attendees to be on time for their next meeting.

### User Communication Guidelines

1. Keep conversations positive, friendly, real, and productive while adding value.
1. If you make a mistake, admit it. Be upfront and be quick with your correction. If you're posting to a blog, you may choose to modify an earlier post. Just make it clear that you have done so.
1. There can be a fine line between healthy debate and incendiary reaction. Try to frame what you write to invite differing points of view without inflaming others. You don’t need to respond to every criticism or barb. Be careful and considerate.
1. Answer questions, thank people even if it’s just a few words. Make it a two way conversation.
1. Appreciate suggestions and feedback.
1. Don't make promises that you can't keep.
1. Guide users who ask for help or give a suggestion and share links. [Improving Open Development for Everyone](https://about.gitlab.com/2015/12/16/improving-open-development-for-everyone/), [Types of requests](https://about.gitlab.com/2014/12/08/explaining-gitlab-bugs/).
1. When facing negative comment, respond patiently and treat every user as an individual, people with the strongest opinions can turn into [the strongest supporters](https://about.gitlab.com/2015/05/20/gitlab-gitorious-free-software/).

### Writing Style Guidelines

1. {: #american-english} At GitLab, we use American English as the standard written language.
1. Do not use rich text, it makes it hard to copy/paste. Use [Markdown](/handbook/product/technical-writing/markdown-guide) for things stored in git. In Google Docs use "Normal text" using the style/heading/formatting dropdown and paste without formatting.
1. Don't use ALL CAPS because if feels like shouting.
1. We use Unix style (lf) line endings, not Windows style (crlf), please ensure `*.md text eol=lf` is set in the repository's `.gitattributes` and run `git config --global core.autocrlf input` on your client.
1. Do not create links like "here" or "click here". All links should have relevant anchor text that describes what they link to, such as: "GitLab CI source installation documentation".
1. Always use [ISO dates](https://en.wikipedia.org/wiki/ISO_8601#Calendar_dates) in all writing and legal documents since other formats [lead to online confusion](http://xkcd.com/1179/). Use `yyyy-mm-dd`, for example 2015-04-13, and never 04-13-2015, 13-04-2015, nor 2015/04/13.
1. For engineering (for example production postmortems) we use UTC as the timezone. For all other uses we use Pacific time since we are a San Francisco based company. Please refer to time as '9:00 Pacific' and not PST since that is ambiguous during daylight savings.
1. If you have multiple points in a comment or email, please number them to make replies easier.
1. When you reference an issue, merge request, comment, commit, page, doc, etc. and you have the URL available please paste that in.
1. In making URLs, always prefer hyphens to underscores, and always use lowercase.
1. The community includes users, contributors, core team members, customers, people working for GitLab Inc., and friends of GitLab. If you want to refer to "people not working for GitLab Inc." just say that and don't use the word community. If you want to refer to people working for GitLab Inc. you can also use "the GitLab Inc. team" but don't use the "GitLab Inc. employees".
1. When we refer to the GitLab community excluding GitLabbers please say "wider community" instead of "community".
1. All people working for GitLab (the company) are the [GitLab team](/team). We also have the [Core team](/core-team) that consists of volunteers.
1. Please always refer to GitLab Inc. people as GitLabbers, not employees.
1. Use inclusive and gender-neutral language in all writing. So for example, write "they, their" instead of "he, his".
1. Always write GitLab with a capitalized G and L, even when writing GitLab.com.
1. Always capitalize the names of GitLab [features](/features).
1. Do not use a hyphen when writing the term "open source."
1. Monetary amounts shouldn't have one digit, so prefer $19.90 to $19.9.
1. If an email needs a response, write the answer at the top of it.
1. Use the future version of words, just like we don't write internet with a capital letter anymore. We write frontend and webhook without a hyphen or space.
1. Our homepage is https://about.gitlab.com/ (with the `about.` and with `https`).
1. Try to use the [active voice](https://writing.wisc.edu/Handbook/CCS_activevoice.html) whenever possible.
1. Please refer to self-hosted installations as on-premises, not on-premise.
1. If you use headers properly format them (`##` in Markdown, "Heading 2" in Google docs), start at the second header level because header level 1 is for titles. Do not end headers with a colon.
1. Always use an [Oxford comma](https://en.wikipedia.org/wiki/Serial_comma) in lists of three or more terms.
1. Always use a single space between sentences rather than two.
1. Read our [Documentation Styleguide](https://docs.gitlab.com/ce/development/doc_styleguide.html) for more information when writing documentation.
1. Do not use acronyms when you can avoid it as you can't assume people know what you are talking about. Example: instead of `MR`, write `merge request`
1. We segment our customers/prospects into 4 segments [Strategic, Large, Mid-Market and Small Medium Business (SMB)](/handbook/sales/#market-segmentation).

### Beamy Guidelines

Beamy is our company conference call robot. It lives in the San Francisco Howard St. office.
Its main purpose is to allow those outside of the office a view into the space and people.
When you call in to the beam your face will appear on the screen (so make sure your webcam
works) and you can drive the robot around the office. It simulates being in the space without
physically being there. It is really cool and everyone should try it and have fun with it.

* You need an invite email to connect and to download a desktop client, please @mention Emily in the #general channel if you don't have the invite yet.
* **Beamy times**: 8am until 6pm Pacific time. [Please check the current time!](https://time.is/San_Francisco) on workdays and during all company events, for other times please @mention Sytse in the Slack #valley channel to see if it is OK. It is on auto connect so you'll beam right in.
* The email invite will come from "Suitable Tech". Once you are sent an invite you can beam in at any time and drive around our beam. Don’t forget to park it back on the charger when you are done. You can do so by driving up to the charger, when you see a green outline press AND HOLD 'p' until it's parked. Make sure it is charging, otherwise try again.
* If you don't use headphones be careful about your volume and microphone placement, it might start singing, if so immediately mute your microphone and switch to headphones.
* More info about Beam can be found at [Suitable Tech](https://suitabletech.com).
* Please report any questions or issues you have about the beam in the Slack #peopleops channel.

### Company phone number
{: #phone-number}

If you need to provide the details of GitLab's contact information you can take the [address of the office](/visiting) for reference; or the [mailing address](/handbook/people-operations/#addresses) of the office in the Netherlands if that is more applicable.

If a phone number is required, leave this field empty by default. If that is not possible, then use
the general number (+1-415-761-1791), but be aware that this number simply guides to a voice message that refers the caller back to contacting us via email.

## Organization code names

* Listed in Google Sheet under 'Organization code names'
* To make it easier to recognize code names we base them on classic car models.

There are two types of code names:

* **Don't mention publicly** We can use code names anywhere we regularly share items in that medium with people outside the company: issue trackers, functional group updates, etc. For these we don't have to use code names in things that are never published: salesforce, zuora, zendesk, verbal conversations.
* **Don't write down** there are organizations that we shouldn't write down anywhere.
