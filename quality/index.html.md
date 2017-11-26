---
layout: markdown_page
title: "Quality"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Common Links

- [**Public Issue Tracker (for GitLab CE)**](https://gitlab.com/gitlab-org/gitlab-ce);
  please use confidential issues for topics that should only be visible to team members at GitLab.
- Chat channels; please use chat channels for questions that don't seem appropriate to use the issue tracker for.
  - [#qa](https://gitlab.slack.com/archives/qa): QA pipelines post into this
    channel, QA engineers should monitor this channel to act on alerts. "Acting
    on" may be remediating or just fixing noisy alerts.

## Quality goals and team(s)

### High level goals

* Stabilize & improve the release process
  * What should we be checking prior to each release, when & who is responsible
  * When and how should automated tests be run
  * Learn from common or frequent mistakes & regressions
* Improve [GitLab QA] test coverage, reliability and efficiency
  * Run-time, de-duplication
  * Which tests should run when
  * How can we put test result data in front of the right people & have them act on it
* Gain insight into development & test metrics
  * See: [https://gitlab.com/gitlab-org/triage/issues/1](https://gitlab.com/gitlab-org/triage/issues/1)
* Long-term improvements to the development process
  * Unit test coverage
  * CE/EE maintenance
  * Developers contributing to [GitLab QA] scenarios
  * Integrate feedback from Sales & Customer Support

### Teams in Quality

- [Edge](edge)

## Projects

* [GitLab Development Kit](https://gitlab.com/gitlab-org/gitlab-development-kit)
* [GitLab QA]

## Other Related Pages

- [Engineering](/handbook/engineering)
- [Issue Triage](issue-triage)
- [Issue Triage Policies](/handbook/engineering/issues/issue-triage-policies)
- [Performance of GitLab](/handbook/engineering/performance)
- [Monitoring of GitLab.com](/handbook/infrastructure/monitoring)
- [Production Readiness Guide](https://gitlab.com/gitlab-com/infrastructure/blob/master/.gitlab/issue_templates/production_readiness.md)

[GitLab QA]: https://gitlab.com/gitlab-org/gitlab-qa
