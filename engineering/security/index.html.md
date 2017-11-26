---
layout: markdown_page
title: "Security Team"
---

## Common Links

- Security crosses many teams in the company, but most often security related 
issues are posted in the [public (!) security issue tracker](https://gitlab.com/gitlab-com/security/issues/), 
but they also appear in the [infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/issues/), 
or [gitlab-ce](https://gitlab.com/gitlab-org/gitlab-ce/issues/), or even 
[organization](https://gitlab.com/gitlab-com/organization/issues/) trackers 
with the `~security` label. Please use confidential issues for topics that 
should only be visible to team members at GitLab.
- [Chat channel](https://gitlab.slack.com/archives/security); please use the `#security` chat channel for questions that don't seem appropriate to use the issue tracker or the internal email address for.
- [Frequently asked questions about Security of GitLab](/security) _the application_  as well as GitLab _the organization_  are documented on the top-level [security page](/security).
- [Security Best Practices](/handbook/security), using 1Password and similar tools, are documented on their own [security best practices page](/handbook/security).
- GitLab.com and GitLab Hosted [data breach notification policy](https://about.gitlab.com/security/#data-breach-notification-policy).

## On this page
{:.no_toc}

- TOC
{:toc}

## Security topics

At a high level, the topic of security encompasses keeping GitLab.com safe, from
the perspective of the application, the infrastructure, and the organization.

We track progress on tackling security related issues across the spectrum through
an ["always WIP Risk Assessment"](#risk-assessment), and its associated
(confidential) meta issue that is kept up to date to
[list the top 10 actions](https://gitlab.com/gitlab-com/infrastructure/issues/1851)
the team is working on.

## Issue Triage

The Security team needs to be able to communicate the priorities of security
related issues to the Product, Development, and Infrastructure teams. Here's
how the team can set priorities internally for subsequent communication
(inspired in part by how the [support team does this](/handbook/support/workflows/support_workflows/issue_escalations.html.md)).

### Use labels

Always. Use `~security` and as appropriate also `~bug`, `~feature proposal`,
`~customer`. Add [Security Level priority labels](#security-priority-labels)
( `~SL1`, `~SL2`, `~SL3`) to indicate perceived priority inside the Security Team.

The reasoning behind adding an `~SL` label to _every_ of these issues is that each issue _should_ have had
someone consider the urgency and impact, and this is best done at time of creating the issue since that is
when the information and context is "fresh" in your mind. It is OK to change the assessment and label at a
later date upon reflection. When issues are filed _without_  an `~SL` label it
will be unclear whether an issue lacks the label due to lack of urgency / impact,
or due to missing a step in the process.


### Security Priority Labels

Use the following as a guideline to determine which Security Level Priority
label to use for bugs and feature proposals. For this, consider the _likelihood_
and _impact_  of a security incident that could result from this issue not being
resolved.

- **Likelihood:**  _For example: If left unresolved, can we expect to see an
incident within a release cycle?_
  - L1 - Wide open gap easily found, or perhaps even ways for the incident to
  be triggered _accidentally_ .
  - L2
  - L3 - Unlikely an incident would occur (hard to find vulnerability, super
    edge cases).
- **Impact:** _For example: Can data be lost or compromised as a result?_
  - I1 - Any data loss. Or data exposed of many users.
  - I2
  - I3 - Meta data exposed (e.g. number of merge requests pushed) of some users

| **Likelihood \ Impact**          | **I1 - High** | **I2 - Medium**  | **I3 - Low**   |
|-------------------------------|---------------|------------------|----------------|
| **L1 - High**                 | `SL1`         | `SL1`            | `SL2`          |
| **L2 - Medium**               | `SL1`         | `SL2`            | `SL3`          |
| **L3 - Low**                  | `SL2`         | `SL3`            | `SL3`          |

#### Escalating from the Security Team to the Development Team

**Note**
- Issues are not scheduled for a particular release unless the team leads add them to a release milestone
*and* they are assigned to a developer.
- Safety valve: If something is "truly urgent", pinging leads in the issues when they are created is the best
way to go, so it can be made Next Patch Release. This will often be preceded by loud debate and concurrence on
chat.

Issues with an `SL1` or `SL2` rating should be immediately brought to the attention
of the relevant product managers, and team leads by pinging them in the issue
and/or escalating via email and chat if they are unresponsive.

Issues with an `SL1` rating are given priority over all other releases and should
be patched immediately.

Issues with an `SL2` rating will be scheduled for the next security release, which may
be days or weeks ahead depending on severity and other issues that are waiting for
patches. An `SL2` rating is not a guarantee that a patch will be ready prior to
the next security release, but that should be the goal.

Issues with an `SL3` rating have a lower sense of urgency and are assigned a target
of the next minor version. If a low-risk or low-impact vulnerability is reported that would
normally be rated `SL3` but the researcher has provided a 30 day time window (or less)
for disclosure this issue may receive an `SL2` rating to ensure that it is
patched before disclosure. Any `SL3` issues that are approaching their public disclosure
window can be re-assigned an `SL2` rating.

An `SL4` rating is also available. `SL4` is used for issues that are suggestions
to improve security without a well-defined path for implementation, vulnerabilities
that are low risk but would require complex changes to the application or
architecture to fix, or other long-term issues. `SL4` issues have no defined
schedule for closure.

#### More Risk Rating Examples

`SL1`:
* Remote Command Execution (RCE)
* SQL Injection (SQLi)
* Authentication Bypass
* Authorization vulnerabilities that expose critical data (password hashes, repositories, tokens)

`SL2`:
* Cross-site Scripting (XSS)
* Authorization vulnerabilities that do not expose critical data
* Resource exhaustion denial-of-service (DoS)
* Cross-site Request Forgery (CSRF)

`SL3`:
* Tab nabbing
* Race conditions that do not put user data in jeopardy
* Path disclosure

`SL4`:
* Implement new security feature
* Remove support for dangerous protocol

## Security releases

The processes for security releases is described with a checklist of events on
the [critical release process](/handbook/engineering/critical-release-process)
page, as well as in the [release-tools](https://gitlab.com/gitlab-org/release-tools/blob/master/doc/security.md) project.

## Fighting Spam

The security team plays a large role in defining procedures for defending against
and dealing with spam. Common targets for spam are public snippets, projects, issues,
merge requests, and comments. Advanced techniques for dealing with these types of spam
are detailed in the [Spam Fighting runbook](https://docs.google.com/document/d/1V0X2aYiNTZE1npzeqDvq-dhNFZsEPsL__FqKOMXOjE8).

## Always "WIP" Risk Assessment
{: #risk-assessment}

GitLab has an "always WIP" Risk Assessment and all team members are encouraged to
participate. The Risk Assessment consists of a list of all risks or threats to
the GitLab infrastructure and GitLab as a company, their likelihood of occurring,
the impact should they occur, and what actions can be taken to prevent these
risks from damaging the company or mitigate the damage should they be realized.

The risk assessment is stored as a Google Sheet (search Google Drive for "Risk
Assessment"; make sure you are searching for spreadsheets shared with GitLab.com)
and is available to all team members. It should not be shared with people outside of the company
without permission.

The format of the Risk Assessment may seem intimidating at first. If you do not
know what values to use for risk ratings, impact ratings, likelihoods or any other
value leave them blank and reach out to the Security Team to help you determine
appropriate values. It is more important to have all risks documented than it is to have all values
completed when adding new risks. Guidelines and instructions for how to add a
risk and how to calculate each rating or score are included on the
"Instructions" tab.

## Vulnerability Reports and HackerOne

GitLab receives vulnerability reports by various pathways, including:
- HackerOne bug bounty program
- `security@gitlab.com`
- Issues opened on the public issue trackers
- Reports or questions come in from customers through Zendesk.

For **any** reported vulnerability:

- Open a confidential issue the appropriate issue tracker **within 24 hrs** of
receiving the report. If the vulnerability was reported via a public issue, make
the issue confidential.
- An initial determination should be made as to severity and impact. Never
**dismiss** a security report outright. Instead, follow up with the
reporter, asking clarifying questions.
- For next steps, see the process as it is detailed below for HackerOne reports,
and adhere to the guidelines there for vulnerabilities reported in other ways as
well in terms of frequency of communication and so forth.
- Remember to prepare patches, blog posts, email templates, etc. on `dev` or in
other non-public ways even if there is a reason to believe that the vulnerability
is already out in the public domain (e.g. the original report was made in a public
issue that was later made confidential).

### HackerOne Flow

GitLab utilizes [HackerOne](https://www.hackerone.com) for its bug bounty program.
Security researchers can report vulnerabilities in GitLab applications or the
GitLab infrastructure via the HackerOne website. Team members authorized to
respond to HackerOne reports use procedures outlined here.

- Open a confidential issue the appropriate issue tracker **within 24 hrs** of
receiving the report (usually [CE](https://gitlab.com/gitlab-org/gitlab-ce/issues)),
_except_ in the case of an obviously invalid report, see below.
   - HackerOne provides an "export" option that simplifies copying data from the HackerOne
issue to GitLab. Export the data in markdown format and paste it into the new
issue.
   - Always add the `~HackerOne` label to these issues, for later reporting and tracking.
   - If the you are unsure as to the validity or impact of the finding this should be stated in the
     issue so that others can investigate.  
- Attempt to verify the report and triage the vulnerability.
   - Add the appropriate [Security Priority Labels](#security-priority-labels)
   - As applicable, notify relevant team members via the issue, chat, and email,
   depending on the chosen security level.
- Change the state of the report to "Triaged" in HackerOne and include a link to the issue
as the reference.
- At this point, but **always within 24 hrs** of the receiving the report, the
HackerOne researcher should be notified that the issue has been triaged. Always
let the researcher know:
  * Whether or not the finding has been verified.
  * That the issue has been triaged and provide a link to the confidential issue. Do
  not invite the researcher to the issue via their GitLab account if they ask. Sensitive
  data such as related vulnerabilities are sometimes discussed in these issues.
  * That the GitLab issue will be opened to the public when a patch has been released.
  * That they will be updated on our progress via HackerOne as soon as we know more.
  * Always mention that they can contact us at any time for an update.
- Discussion and remediation of vulnerabilities can sometimes take longer than we
  would prefer. Even so, frequent communication with reporters is far better than  
  leaving reporters in the dark, even if our progress is slow. Therefore:
    - For vulnerabilities where patches are actively being worked on,
  reporters should be updated at least **weekly**.
    - In the case where fixes are not as clear or discussion is still on-going
    as to whether a patch will be created at all, reporters should be notified
    of updates at least **monthly**.
    - In any case, no report should go "stale" where updates are not provided
    within the last month.

#### If a report is unclear

If a report is unclear, or the reviewer has any questions about the validity of
the finding or how it can be exploited, now is the time to ask. Move the report to the
"Needs More Info" state until the researcher has provided all the information necessary to
determine the validity and impact of the finding. Use your best judgement to determine
whether it makes sense to open a confidential issue anyway, noting in it that you
are seeking more information from the reporter. When in doubt, err on the side
of opening the issue.

One the report has been clarified, follow the "regular flow" described above.

#### If a report violates the rules

If a report violates the rules of GitLab's bug bounty program use good judgement
in deciding how to proceed. For instance, if a researcher has tested a vulnerability
against GitLab production systems (a violation), but the vulnerability has not
placed GitLab user data at risk, notify them that they have violated the terms
of the bounty program but you are still taking the report seriously and will treat
it normally. If the researcher has acted in a dangerous or malicious way, inform
them that they have violated the terms of the bug bounty program and will not
receive credit. Then continue with the "regular flow" as you normally would.

#### If the report is invalid

If the report is invalid (in your determination) or does not pose a security risk
to GitLab or GitLab users it can be closed without opening an issue on GitLab.com.
When this happens inform the researcher why it is not a vulnerability and close
the issue as "Informational". HackerOne offers the option to close an issue
as "Not Applicable" or "Spam". Both of these categories result in damage to the
researcher's reputation and should only be used in obvious cases of abuse.

### When a patch is ready

When a patch has been developed, tested, approved, merged into the security
branch, and a new security release is being prepared it is time to inform the
researcher via HackerOne. Post a comment on the HackerOne issue to all parties
informing them that a patch is ready and will be included with the next security
release. Provide release dates, if available, but try not to promise a release
on a specific date if you are unsure.

This is also a good time to ask if they would like public credit in our release
blog post and on our vulnerability acknowledgements page for the finding. We will
link their name or alias to their HackerOne profile, Twitter handle, Facebook profile,
company website, or URL of their choosing. Also ask if they would like the HackerOne
report to be made public upon release. It is always preferable to publicly disclose
reports unless the researcher has an objection.

### On release day

On the day of the security release several things happen in order:

* The new GitLab packages are published.
* All security patches are pushed to the public repository.
* The public is notified via the GitLab blog release post, security alerts email, and Twitter.
* The vulnerability acknowledgements page is updated with appropriate credits to
the reporting researchers.

Once all of these things have happened notify the HackerOne researcher that the
vulnerability and patch are now public. The GitLab issue should be closed and
the HackerOne report should be closed as "Resolved". Public disclosure should be
requested if they have not objected to doing so. Any sensitive information
contained in the HackerOne report should be sanitized before disclosure.

### Swag for reports

GitLab awards swag codes for free GitLab swag to any reports that result in a
security patch. Limit: 1 per reporter. When a report is closed, ask the reporter
if they would like a swag code for free GitLab clothing or accessories. Swag codes
are available by request from the marketing team.

## Vulnerability Scanning

GitLab maintains a custom vulnerability scanner that is used to regularly scan all GitLab
assets for common vulnerabilities as well as previously patched GitLab vulnerabilities
and to ensure that no GitLab security-sensitive services are accidentally exposed.

Details on this scanner and how it is configured are available to all team members in a
Google Doc entitled "Vulnerability Scanner Config".

## Package Signing
{: #package-signing}

The packages we ship are signed with GPG keys, as described in the
[omnibus documentation](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/package-information/signed_packages.md).
The process around how to make and store the key pair in a secure manner is
described in [the runbooks](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/manage-package-signing-keys.md).
Those runbooks also point out that the management of the keys is handled by the
Security team and not the Build team. For more details that are specific to key
locations and access at GitLab, find the internal google doc titled "Package
Signing Keys at GitLab" on Google Drive.
