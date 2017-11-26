---
layout: markdown_page
title: "GitLab Handbook Usage"
---

## Advantages

At GitLab our handbook is extensive and keeping it relevant is an important part of everyone's job. The reasons for having our processes described in a handbook are:

1. Reading is much faster than listening.
1. Reading is async, you don't have to interrupt someone or wait for them to become available.
1. Recruiting is easier if people can see what we stand for and how we operate.
1. Retention is better if people know what they are getting into before they join.
1. On-boarding is easier if you can find all relevant information spelled out.
1. Teamwork is easier if you can read how other parts of the company work.
1. Discussing changes is easier if you can read what the current process is.
1. Communicating change is easier if you can just point to the diff.
1. Everyone can contribute to it by proposing a change via a merge request.

## Flow

1. A (process) problem comes up, frequently in an issue or chat.
1. A proposal is made in a merge request to the handbook.
1. After merging the change is announced by linking to the diff in the MR or commit. Major ones are put in the agenda of the team call. Medium ones are put in a chat channel. If there was an issue close it out with a link to the diff.

## Why handbook first

Documenting things in the handbook takes more time initially. You have to think where to make the change, integrate it with the existing content, and possibly add to or refactor the handbook to have a foundation. But it saves time over a longer period and it is essential to scale and adapt our organization. It is not unlike writing tests for your software. Only communicate a (proposed) change via a change to the handbook; don't use a presentation, email, chat message, or another medium to communicate the gist of the change. It might be more convenient to the presenter but it makes it harder for the audience to understand the context and implications for other processes. Handbook first is needed to make sure there is no duplication, the handbook is always up to date, and others are able to contribute.

## Guidelines

Please follow these guidelines and remind others of them.

1. If you need to discuss with a team member for help please realize that probably the majority of the community also doesn't know, be sure to **document** the answer to radiate this information to the whole community. After the question is answered, discuss where it should be documented and who will do it. You can remind other people of this by asking "Who will document this?"
1. When you discuss something in chat always try to **link** to a URL where relevant, for example, the documentation you have a question about or the page that answered your question. You can remind other people of this by asking "Can you please link?"
1. To change a guideline or process, **suggest an edit** in the form of a merge request.
After it is merged you can talk about it during the team call if applicable. You can remind other people of this by asking "Can you please send a merge request for the handbook?"
1. Communicate process changes by linking to the **merged diff** (a commit that shows the changes before and after). If you are communicating a change for the purpose of discussion and feedback, it is ok to link to an **unmerged diff**. If  Do not change the process first, and then view the documentation as a lower priority task. Planning to do the documentation later inevitably leads to duplicate work communicating the change and to outdated documentation. You can remind other people of this by asking "Can you please update the handbook first?"
1. Remember, the handbook is not what we hope to do, what we should formally do, or what we did months ago. **It is what we do right now.** So if you want to change a process change the handbook in order to change it. To propose a change to a process make a merge request to change the handbook. Don't use another channel to propose a handbook change (email, Google Doc, etc.).
1. Like everything else, our processes are always in flux. Everything is always in draft, the initial version should be in the handbook, too. If you are proposing a change to the handbook, whenever possible, skip the issue and submit a merge request. Mention the people that affected by the change in the merge request. In many cases, merge requests are easier to collaborate on since you can see the proposed changes.
1. To propose a change a merge request is preferred over an issue description. A merge request allows people to see the context of your change.
1. If something is a limited test to a group of users, add it to the handbook and note as such. Then remove the note once the test is over and every case should use the new process.
1. When communicating something always include a link to the relevant (and up to date) part of the **handbook** instead of including the text in the email/chat/etc. You can remind other people of this by asking "Can you please link to the relevant part of the handbook?"
1. If you copy content please remove it at the origin place and replace it with a link to the new content. Duplicate content leads to updating it in the wrong place, keep it [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).
1. Make sure to always cross-link items if there are related items (elsewhere in the handbook, in docs, or in issues).
1. The handbook is structured by function to ensure every item in it has a clear owner and location. Please cross-link liberally but avoid unstructured content like lists of links, FAQ's, and company wide glossary since these are very hard to keep up to date. Instead put the link, the answer, and the definition in the most relevant place.
1. Use headers liberally. Add a Table of Contents ([ToC](https://gitlab.com/gitlab-com/www-gitlab-com/merge_requests/7141/diffs#f054d0f855ebef2a11559c362a356a2f9e010b99_6_6)) if a page is longer than one screen. Headers should have normal capitalization (don't use [ALL CAPS](https://en.wikipedia.org/wiki/All_caps) nor [TitleCase](http://www.grammar-monster.com/glossary/title_case.htm)).
1. If someone inside or outside GitLab makes a good suggestion invite them to add it to the handbook. Send the person the url of the relevant page and section and offer to do it for them if they can't. Having them make and send it will make the change and review reflect their knowledge.
1. All documentation that also applies to code contributions from the wider community should be in the GitLab CE project (for example in [CONTRIBUTING](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md) or the [code review guidelines](https://docs.gitlab.com/ce/development/code_review.html), not the handbook that is only for team members.
1. Learn how to edit the [handbook using git](/handbook/git-page-update). Please read through the [Writing Style Guidelines](https://about.gitlab.com/handbook/communication/#writing-style-guidelines) before contributing.
1. When you submit a merge request, make sure that it gets merged quickly. It should not take more than a few days to get a merge request approved to the handbook. Mention people in the merge request or reach them via Slack. If you get a suggestion for a large improvement on top of the exiting one consider doing that separately. Create an issue, get the exiting MR merged, then create a new merge request. Getting your merge requests approved quickly may prevent merge conflicts from happening.
1. Only mark a merge request as "WIP" (Work in Progress) if it will negatively affect the company if merged too early. That can be the case for application code but is almost not possible for handbook MRs.
1. If you have to move content have a merge request that moves it and does nothing else. If you want to clean it up, summarize it, or expand on it do that haver the moving MR is merged. This is much easier to review.
1. The handbook is for things concerning (future) GitLab team members only. If something concerns users of GitLab, it should be documented in the [GitLab documentation](http://doc.gitlab.com/), the [GitLab Development Kit (GDK)](https://gitlab.com/gitlab-org/gitlab-development-kit), the [CONTRIBUTING file](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md) or the [PROCESS file](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md).
