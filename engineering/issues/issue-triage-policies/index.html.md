---
layout: markdown_page
title: Issue Triage Policies
---

GitLab believes in [Open Development][open-development], and we encourage the
community to file issues and open merge requests for our projects on
[GitLab.com](https://gitlab.com/groups/gitlab-org). Their contributions are
valuable, and we should handle them as effectively as possible. A central part
of this is triage - the process of categorisation according to type and severity.

Any GitLab team member can triage issues. Keeping the number of untriaged issues
low is essential for maintainability, and is our collective responsibility.
Consider triaging a few issues around your other responsibilities, or scheduling
some time for it on a regular basis.

## Triaging issues

Initial triage involves (at a minimum) labelling an issue appropriately, so
untriaged issues can be discovered by searching for issues without any labels.
Follow one of these links:

* [GitLab CE][ce-issues-query]
* [GitLab EE][ee-issues-query]
* [GitLab Omnibus][omnibus-issues-query]
* [GitLab.com Support Tracker][support-issues-query]

Pick an issue, with preference given to the oldest in the list, and evaluate it with a critical eye, bearing the [policies](#policies) below in mind. Some questions to ask yourself:

* Do you understand what the issue is describing?
* What labels apply? Particularly consider [team, subject, and type](/handbook/engineering/workflow/#workflow-labels) labels
* How critical does it seem? Does it need to be escalated to a lead or the VP of engineering?
* Would the `security` label be appropriate?
* Should it be made confidential? It's usually the case for `security` issues or
  issues that contain private information

Apply each label that seems appropriate. Issues with a security impact should be
treated specially - see the [security disclosure process](/handbook/support/channels/#security-disclosures).

If the issue seems unclear - you aren't sure which labels to apply - ask the
requestor to clarify matters for you. Keep our
[user communication guidelines](/handbook/communication/#user-communication-guidelines) in mind
at all times, and commit to keeping up the conversation until you have enough
information to complete triage.

Check for duplicates! Searching for some keywords in the issue should give you a
short list of possibilities to scan through. Check both open and closed issues,
as it may be a duplicate of a solved problem.

Consider whether the issue is still valid. Especially for older issues, a `bug`
may have been fixed since it was reported, or a `feature proposal` may have
already been implemented.

Be sure to check cross-reference notes from other issues or merge requests, they
are a great source of information! For instance, by looking at a cross-referenced
merge request, you could see a "Picked into `8-13-stable`, will go into `8.13.6`."
which would mean that the issue is fixed since the version `8.13.6`.

If the issue meets the requirements, it may be appropriate to make a
[scheduling request](/handbook/engineering/workflow/#scheduling-issues) - use
your judgement!

You're done! The issue has all appropriate labels, and may now be in the backlog,
closed, awaiting scheduling, or awaiting feedback from the requestor. Pick
another, if you've got the time.

## Policies

### Outdated issues

For issues that haven't been updated in the last 3 months the "Awaiting Feedback" label should be added to the issue. After 14 days, if no response has been made by anyone on the issue, the issue should be closed. This is a slightly modified version of the Rails Core policy on outdated issues.

If they respond at any point in the future, the issue can be considered for reopening. If we can't confirm an issue still exists in recent versions of GitLab, we're just adding noise to the issue tracker.

### Duplicates

Before opening a new issue, make sure to **search for keywords** and verify your issue isn't a duplicate.

Checking for and/or reporting duplicates when you notice them.

All things held equal, the earliest issue should be considered the canonical version. If one issue has a better title, description, and/or more comments and positive reactions, it should be prioritized over earlier issues even if it's a duplicate.

### Lean toward closing

We simply can't satisfy everyone. We need to balance pleasing users as much as possible with keeping the project maintainable.

- If the issue is a bug report without reproduction steps or version information, close the issue and ask the reporter to provide more information.
- If we're definitely not going to add a feature/change, say so and close the issue.

### Label issues as they come in

When an issue comes in, it should be triaged and labeled. Issues without labels are harder to find and often get lost.

### Take ownership of issues you've opened

Sort by "Author: your username" and close any issues which you know have been fixed or have become irrelevant for other reasons. Label them if they're not labeled already.

### Questions/support issues

If it's a question, or something vague that can't be addressed by the development team for whatever reason, close it and direct them to the relevant support resources we have (e.g. our Discourse forum or emailing Support).

### New labels

If you notice a common pattern amongst various issues (e.g. a new feature that doesn't have a dedicated label yet), suggest adding a new label in chat.

Douwe is the "Label King", make sure he approves of a label before adding it. This way we don't have a bunch of repetitive/unused/inconsistent labels.

## Events

We also hold regular, quarterly events where the Community, Core Team Members and Team Members can contribute to tackling some of our open issues. Please see [the dedicated page](/community/issue-bash) for further information and upcoming event dates


## Notes

The original issue about these policies is [#17693][17693]. We'll be working to improve the situation from within GitLab itself as time goes on.

The following projects, resources, and blog posts were very helpful in crafting these policies:

- [CodeTriage][code-triage]
- [How to be an open source gardener][open-source-gardener]
- [Managing the Deluge of Atom Issues][atom-issues]
- [Handling Large OSS Projects Defensively][handling-big-projects]
- [My condolences, you’re now the maintainer of a popular open source project][my-condolences]
- [The Art of Closing][art-of-closing]

[open-development]: https://about.gitlab.com/2015/12/16/improving-open-development-for-everyone/
[ce-issues-query]: https://gitlab.com/gitlab-org/gitlab-ce/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=No+Label&assignee_id=0
[ee-issues-query]: https://gitlab.com/gitlab-org/gitlab-ee/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=No+Label&assignee_id=0
[omnibus-issues-query]: https://gitlab.com/gitlab-org/omnibus-gitlab/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=No+Label&assignee_id=0
[support-issues-query]: https://gitlab.com/gitlab-com/support-forum/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=No+Label&assignee_id=0
[17693]: https://gitlab.com/gitlab-org/gitlab-ce/issues/17693
[code-triage]: https://www.codetriage.com/
[open-source-gardener]: http://words.steveklabnik.com/how-to-be-an-open-source-gardener
[atom-issues]: http://blog.atom.io/2016/04/19/managing-the-deluge-of-atom-issues.html
[handling-big-projects]: http://artsy.github.io/blog/2016/07/03/handling-big-projects/
[my-condolences]: https://runcommand.io/2016/06/26/my-condolences-youre-now-the-maintainer-of-a-popular-open-source-project/
[art-of-closing]: https://blog.jessfraz.com/post/the-art-of-closing/
