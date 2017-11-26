---
layout: markdown_page
title: "Vacancies"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Introduction

For a listing of open jobs, please see the [vacancies section on the Jobs page](/jobs#vacancies).
Vacancies are maintained in Lever based on our job descriptions.
Our job descriptions are the single source of truth for what we need.
The relevant parts are copy-pasted to Lever to open a vacancy.
The /jobs page must be updated first before a job is added or updated in Lever.

One job description can describe multiple levels in the job.
Lever typically will only have one level described for the specific role we are
looking for, and as a result only the relevant parts are copy-pasted.

## Vacancy Creation Process

If you want to hire for a position you will need to follow the steps below.
A vacancy needs to be open on our jobs page before we can start interviewing.

As part of the vacancy creation process, you will be asked to obtain approval from
your Executive team member. Your Executive team member must escalate and obtain
authorization for any new job positions/searches if they are not part of the Hiring
Forecast (search for an internal Google sheet by that name on Google Drive). Typically
the Executive Team member escalates to the CFO and/or the CEO. Roles listed on the
Hiring Forecast will have a status of Open, Closed, Filled, Draining, or Pending
Approval which are defined below:

* Open - vacancy is open and we are actively sourcing and hiring for the role
* Closed - no vacancy, not actively sourcing or hiring for the role
* Filled - vacancy has been filled by internal or external candidate
* Draining - vacancy is closed, no longer accepting new applicants, but will review existing candidates through the hiring process and fill the role if a qualified candidate is identified from existing applicants
* Pending Approval - vacancy has been suggested by executive team member and is pending board, CEO, or CFO approval.

To open a vacancy, please go to the [People Ops project](https://gitlab.com/gitlab-com/peopleops/issues)
and create a new issue. Next to title where it says "Choose a template", choose the `vacancy` template. Follow the directions that populate in the issue.

You will be asked to provide details on the vacancy, to either create or update the job description, create a hiring process, create an assessment for applicants, and create application questions for the role.

1. If a description of the role does not already exist, the hiring manager will create a vacancy description and assign the MR to their Executive Leadership, per the vacancy issue template.
    1. Create the relevant page in `https://about.gitlab.com/jobs/[name-of-job]`, being sure to use only lower case in naming your directory if it doesn't already exist. If the location of the applicant is important, then the location and a compensation range corresponding to that location can be provided as part of the vacancy posting.
    1. The job description provided on this page will be used _both_ for the
    Lever recruiting posting (see steps further down), as well as serving as
    the description that team members and managers alike use in conversations
    around career development and performance management.
    1. Always add `Responsibilities`, `Requirements`, and `Hiring Process` to the job description.
1. A Recruiter will use a this [gender decoder](http://gender-decoder.katmatfield.com/) to ensure that the language and structure of the vacancy description is gender neutral. The recruiter will make necessary edits to the vacancy description to create a neutral description.

Per the vacancy issue template, the person requesting the vacancy will need to ping the People Ops Analyst to propose an appropriate NYC benchmark compensation for the role, and they will submit the proposal to the [compensation committee](/handbook/people-operations/global-compensation/#compensation-committee) for approval.
   - For any position, filling in the NYC benchmark salary in the `jobs.yml` file will automatically cause the [Compensation Calculator](/handbook/people-operations/global-compensation) to show at the bottom of the position description page.
   - For some positions, it may be possible or desirable to exclusively seek candidates outside of higher cost regions. This is a role by role decision between the Hiring Manager and People Operations. _If_ it is decided to seek candidates outside of higher cost regions, then that needs to be explicitly communicated on the position description page in order to set fair expectations for candidates and recruiters alike. Sample text to consider placing on the position description page: "Globally, xx % of people live in metro areas with a rent index greater than yy, while at GitLab, this is zz % of people in this role currently. Therefore, in line with our value of staying [frugal](/handbook/values), we are now focusing on only hiring in metro areas with a **rent index lower than yy**. Please bear this in mind when using the compensation calculator below." (obviously, fill in the missing numbers).

Once all steps in the vacancy issue are completed, a member of the Recruiting team will create the position in [Lever](https://hire.lever.co/jobs), using the exact same job title and job description as provided in the issue. If this step is completed out of order, people are able to apply even though the position posting may not have been approved yet.
   * In Lever, click "Create Job Posting" in top right corner.
   * For location, select a specific timezone or "Remote".
   * For department/team, select the appropriate team.
   * For work type, choose full-time or intern.
   * Under "Job Posting Status" you can choose whether this job will be published upon creation, kept internal, or a draft.
   * For the description, copy and paste any opening paragraphs from the position description on Gitlab.com. Beneath that, copy and paste the "About GitLab" section from another vacancy, which includes a short blurb about GitLab, what we value, and the top 10 reasons to work at GitLab.
   * Under `Lists` create a new list titled "Responsibilities" and copy and paste the responsibilities from the job description on GitLab.com. Do the same for "Requirements", and any other sections as needed.
   * Include the hiring process in the `Closing` section, along with a link to the compensation calculator for the role if applicable.
   * Under `Custom Questions`, add the following: "Additional Questions", "Salary", and "Cover Letter". If there are additional specific questions for that role, either select the appropriate form or create a new one.
   * Finally, you can also customize the default Feedback Forms that interviewers will complete during different stages of the interview. If there is no custom feedback form, choose "General Feedback".
   * Once finished, click "Create Posting". If you chose "published" under "Job Posting Status", the job will become live on our jobs page.
 1. All job openings must be posted on our careers page for at least 5 business days before we can close it or make an offer; this includes all new positions and [promotions](/handbook/people-operations/compensation-title-changes/#promotions).

## Publicize the job

The manager should always ask the team for passive referrals for open positions. GitLab team members can refer candidates through our [referral program](/handbook/incentives/#referral-bonuses)

The employment team will **always** publicize the job through the following means:

1. Tweet the new job post with the help of the content marketing manager and team.
1. Request "soft” referrals by encouraging all GitLab team members to post links to the jobs site on their LinkedIn profiles.
1. [Hacker News Who's Hiring](https://news.ycombinator.com/ask): On the first of the month, include a note for GitLab in the Hacker News thread of "Who's Hiring" . Template text:
`REMOTE ONLY GitLab - We're hiring production engineers, developers, designers, and more, see https://about.gitlab.com/jobs/ We're a remote only company so everyone can participate and contribute equally. GitLab Community Edition is an open-source Ruby on Rails project with over 1000 contributors.`

**Note**: The employment team may advertise the job through the following sites and is open to posting to more, in order to widely publish a variety of vacancies:

1. [Hacker News Jobs](https://news.ycombinator.com/jobs) as a Y Combinator alumni we can post directly to the front page. The EA vault has credentials so ask an EA to post. Template text: `GitLab (YC W15) is hiring XXX and more - Remote Only`
1. [LinkedIn](https://www.linkedin.com/) (Able to post 6 jobs simultaneously, please mention to employment team if you want your role listed here)
1. [StackOverflow](http://stackoverflow.com/jobs) (Able to post 3 jobs simultaneously, please mention to employment team if you want your role listed here)
1. [TechLadies](https://www.hiretechladies.com/) (Able to post 4 roles simultaneously, please mention to employment team if you want your role listed here; at this time we are not posting engineering roles to TechLadies)
1. [RemoteBase](https://remotebase.io/) (Free; job descriptions are synced directly to our respective job description sites)
1. [WeWorkRemotely](https://weworkremotely.com) ($200 for 30 days, per position, used infrequently)
1. [RemoteOK](https://remoteok.io) ($200 for 90 days, per position, used infrequently)
1. [Indeed Prime](http://www.indeed.com/) (Primarily used for non-engineering roles)

## Sourcing for Open Positions

On difficult or hard-to-fill positions, the employment team will use available tools to source for additional candidates. Please communicate with the employment team if sourcing is needed for a strategic, specialized, or difficult to fill position.

## Closing a vacancy

To close a vacancy:

1. The employment team will clear the pipeline of candidates in all stages of application. Consider adding tags to candidates who were interesting but were passed over in this hiring process. Adding tags makes it easier to find them in Lever later on if you are recruiting for the same or a similar position. You can also snooze a candidate if you anticipate reopening the role at a later date.
1. Ask a Lever admin (People Ops) to close the position in Lever.

If the position was posted on any job site (i.e. Stack Overflow, PowerToFly) the employment team will email the partner or remove the position from that site.
