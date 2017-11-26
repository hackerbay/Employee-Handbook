---
layout: markdown_page
title: "UX Team"
---

### On this page

{:.no_toc}

- TOC
{:toc}

## UX Guide

The [UX Guide][ux-guide] documents our principles, approach, and perspective to
the experience of GitLab. Help keep this document up to date and correct by
creating [merge requests](https://gitlab.com/gitlab-org/gitlab-ce/merge_requests/).

## UX Strategy

The vision of GitLab is far from finished and there are a lot of emergent
properties that will allow us to simplify. We believe in iterative improvements
and value aggressive change. We will get some things wrong and quickly strive
to make them right. We have a long way to go, that is why we are taking big
steps.

Please see the [2017 UX Strategy](/handbook/ux/strategy) to view the evolving
UX vision for GitLab.

## UX Workflow

In general, follow the [GitLab Workflow](/handbook/communication/#gitlab-workflow)
and the [Engineering Workflow](/handbook/engineering/workflow/). Also see the
[Basics of GitLab development in the Developer Onboarding](/handbook/developer-onboarding/#basics-of-gitlab-development).
See below for workflow notes relevant to UX Designers and UX Researchers.

### Designer

**Creating and labelling issues**

* [**UX** label][ux-label]: if any kind of UX work is required
* [**UI polish** label](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UI+polish): if it covers _only_ visual improvement(s) to the existing user interface
* [**UX debt** label](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX+debt): if it covers user experience improvement(s) that weren't fully implemented or could be refined after implementation
* [**regression** label](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=regression): if it's a bug introduced in the latest release that broke correct behavior (see the [contribution guidelines](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/CONTRIBUTING.md#regression-issues) for more info)
* [**UX ready** label][ux-ready-label]: if UX work is completed and all feedback is addressed

**Working on issues**

1. Assigning / Taking on Issues:
   1. We try not to assign issues to people but to have people pick issues in a milestone themselves.
   1. All issues in a milestone labeled [Deliverable](https://gitlab.com/groups/gitlab-org/issues?state=opened&label_name%5B%5D=Deliverable) that needs [UX][ux-label] should be assigned to a specific designer by the kickoff. If an issue has no one assigned by kickoff, the issue will be assigned to someone.
   1. Once you have completed work on an issue and labeled it [UX ready][ux-ready-label], please remain assigned. You will be the 'go-to' person for UX questions and reviews.

1. Choose:
   1. Filter by the [UX][ux-label] label and then choose in the following order:
      1. Has the current release's milestone
      1. Has the next release's milestone
      1. [Has milestone **Next 2-3 months**](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&milestone_title=Next+2-3+months&label_name%5B%5D=UX)
      1. [Has milestone **Next 3-6 months**](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&milestone_title=Next+3-6+months&label_name%5B%5D=UX)
      1. [Has milestone **Backlog**](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&milestone_title=Backlog&label_name%5B%5D=UX)
      1. [Popular or with high community involvement (number of comments or upvotes)](https://gitlab.com/groups/gitlab-org/issues?label_name%5B%5D=UX&scope=all&sort=upvotes_desc&state=opened)
      1. [Everything else][ux-label]
   1. Before committing to issues, check if another [UX Designer](/team) has already participated. If their latest activity on that issue was within two months and you’d still like to work on it, ask them what the status is and if you can pick it up for them. If their latest activity on that issue was more than two months ago, just let them know that you’ll be picking it up for them.

1. Work:
   * Define the scope:
      * UX issues have a tendency to expand in scope. Aggressively split off new issues, ideas, and concepts into their own issues. Large issues become really challenging to drive decisions in and make progress on. If you’re ever unsure how to split apart large issues, work with the UX Lead.
      * Developers should be able to ship a product within one life cycle. If a feature is too large to ship within one release, work together to determine the best way of splitting the feature into smaller segments.
      * Bring developers into the conversation early. Ask for feedback on how to split up features while still maintaining the integrity of the UX.
      * When breaking up features into smaller parts, make sure that the end design goal is known. Giving the team the full picture will help developers write code aimed at achieving that goal in the future.
      * Keep the issue description updated with the agreed scope, even if doesn’t impact your work. This is everyone’s responsibility. The issue description must be the Single Source Of Truth (SSOT), not the discussion or individual comments.
   * Propose solutions:
      * Add comments with your proposals. Propose **one** solution, not multiple alternative solutions for others to pick, as this undermines your position as a UX expert and leads to a [design by committee](https://en.wikipedia.org/wiki/Design_by_committee) situation. If you have a good reason to propose multiple alternative solutions make sure to explain why.
      * Anticipate questions that others might have and try to answer them in your proposal comments. You don’t have to explain everything, but try to communicate a bit of your rationale every time you propose something. This is particularly important when proposing changes or challenging the status quo. This reduces the feedback loop and time spent on unnecessary discussions while contributing to the credibility of the UX team, who deal with a lot of *seemingly* subjective issues.
      * Keep the SSOT updated with what’s already agreed upon so that everyone can know where to look. This includes images or links to your design work.
      * If you’re working with design files, follow the instructions in the [GitLab Design project][gitlab-design-project-readme] and regularly commit them.
      * If you are proposing a solution that will introduce a new UX paradigm, or change an existing one, there are additional steps to follow. See the 'Maintain' section below for those steps.
1. Deliver:
   1. Once your work is complete, make sure that the SSOT is updated. This is where you should direct people when they have questions about what should be done and how.
   1. If applicable, commit all design assets and files according to the instructions in the [GitLab Design project][gitlab-design-project-readme].
   1. Once UX work is completed and all feedback is addressed, remove the [UX][ux-label] label, add the [UX ready][ux-ready-label] label, and:
      * If the issue is scheduled for a milestone, add the next [workflow label](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/PROCESS.md#workflow-labels) needed to progress the issue. Typically, this is the [frontend](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=frontend) label.
      * If the issue is not scheduled, mention the [responsible product manager](/handbook/product/#who-to-talk-to-for-what) to [schedule it](/handbook/engineering/workflow/#scheduling-issues)
1. Follow through:
   1. Keep the SSOT in the description updated until the issue is closed. This applies to both text and mockups. Previous content (by a PM, for example) should be removed or archived into a separate section in the description. If the developer working on the issue ever has any questions on what they should implement, they can ask the designer to update the issue description with the design.
   1. For obvious changes, make the SSOT description update directly. [You don't need to wait for consensus](/handbook/values/). Use your judgement.
   1. Make sure you remain assigned and that you’re subscribed to the issue and related merge requests. Continue to follow them, addressing any additional UX issues that come up.
   1. If you are asked to review an MR for an issue you were not assigned to, remind the author who the assigned designer is and assign to original designer for review.
1. Maintain:
   1. If the UX work introduces or changes any of the UX standards or building blocks:
      * If applicable, create a merge request to update the [UX Guide][ux-guide].
      * If applicable, create a merge request to update the [GitLab Elements Sketch file](https://gitlab.com/gitlab-org/gitlab-design/blob/master/production/resources/gitlab-elements.sketch).
      * When any of those requests are merged, add an agenda item to the next UX weekly call to inform everyone of those changes.

### Researcher

**How do I raise a research request for the UX researcher?**

You can raise a research request in one of two ways:

1. Raise a new issue
    * Within the [CE](https://gitlab.com/gitlab-org/gitlab-ce/) or [EE](https://gitlab.com/gitlab-org/gitlab-ee/) project, raise a new issue using the research template.
    * Add the label `UX Research` to the issue.
    * @ mention Sarah O'Donnell `@sarahod`
    * Sarah will schedule the work accordingly.
1. In an existing issue
    * @ mention Sarah O’Donnell `@sarahod` in the existing issue, summarise what you need researching.
    * Add the label `UX Research` to the issue.
    * Sarah will schedule the work accordingly.

**What is the UX researcher workflow?**

1. Work with the UX team to determine what should be researched.
1. Create a research issue:
    * Create an issue within the [UX research](https://gitlab.com/gitlab-org/ux-research) project.
    * Label the issue with the area of GitLab you’re testing (for example, `navigation`) and the status of the issue (`in progress`).
    * Mark the issue as `confidential` until the research is completed so it doesn’t influence user behavior.
    * Assign the issue to yourself. You should only be assigned to an issue when you are actively working on it.
    * Add a progress checklist (a checklist of tasks you need to complete in order to complete the research) to the issue description. This makes it easier for people to understand where the research is up to.
    * Add a summary of what is being tested to the issue description, along with any related issue numbers.
1. Conduct the research.
1. Update the issue you created in the UX research project:
    * Document the findings and recommendations within the issue.
    * Unmark the issue within the UX research project as `confidential`. (In some cases the issue may need to remain confidential if sensitive information is shared. If you’re unsure of whether an issue should remain confidential, please check with Sarah O’Donnell `@sarahod`).
    * Update the status of the issue to `done`.
    * Remove yourself as the assignee from the issue.
1. Inform people of your research:
    * Within the issue, encourage discussion between yourself, UX designers and product owners about which findings should be turned into issues within the GitLab CE or EE project.
    * Create the agreed, new issues within the GitLab CE or EE project. If relevant issues already exist, add your findings to the existing issue description or comments. Always link your findings back to the issue within the UX Research project. 
    * Label any new issues as [appropriate](/handbook/engineering/workflow/#workflow-labels).
    * Close the issue within the UX Research project.
    * Add a link to the completed research within the UX Research project's [ReadMe file](https://gitlab.com/gitlab-org/ux-research/blob/master/README.md)

## UX on Social Media

It is encouraged to share UX designs and insight on social media platforms such
as Twitter and Dribbble.

### Twitter

You can contribute design-related posts to our [@GitLab Twitter account](https://twitter.com/gitlab)
by adding your tweet to our [UX Design Twitter spreadsheet][twitter-sheet].

1. Add a new row with your tweet message, a relevant link, and an optional photo.
1. Ensure that your tweet is no more than 140 characters. If you’re including a link, ensure you have enough characters and consider using a [link shortening service](https://bitly.com/).
1. The UX Lead will check the spreadsheet at the beginning of each week and schedule any tweets on Tweetdeck.
1. Once a tweet is scheduled, the tweet will be moved to the "Scheduled" tab of the spreadsheet.

### Dribbble

GitLab has a [Dribbble team account](https://dribbble.com/GitLab) where you can
add work in progress, coming soon, and recently released works.

* If a Dribbble post has a corresponding open issue, link to the issue so designers can contribute on GitLab.
* Add the Dribbble post to our [UX Design Twitter spreadsheet][twitter-sheet], along with a link to the corresponding open issue if applicable.
* If you’re not a member of the GitLab Dribbble team and would like to be, contact the UX Lead to grant you membership.

[ux-guide]: https://docs.gitlab.com/ce/development/ux_guide/
[ux-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX
[ux-ready-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX+ready
[gitlab-design-project-readme]: https://gitlab.com/gitlab-org/gitlab-design/blob/master/README.md
[twitter-sheet]: https://docs.google.com/spreadsheets/d/1GDAUNujD1-eRYxAj4FIYbCyy8ltCwwIWqVTd9-gf4wA/edit
