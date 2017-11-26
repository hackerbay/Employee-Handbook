---
layout: markdown_page
title: GitHost Administration
category: GitHost
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

## GitHost Administration

### Requesting Access

Ask any of the administrators to give you access to the GitHost UI. Within the UI you will be able to see customer instances, their setup, and their IDs.

You will need to request SSH access to the GitHost production box. For this, please send a chat message to an admin with your Public Key and ask to be added to the authorized_keys of the githost user.

### Documentation
The latest GitHost Administration docs can be found [here](https://dev.gitlab.org/gitlab/GitHost/blob/master/doc/README.md).

### Performance problems on older/smaller instances

We have some customers still on discontinued plans that fall well below
the minimum recommended specifications for running GitLab. This currently
includes any instance with less than 4GB of RAM. Unfortunately, we cannot
guarantee the performance of these instances. Make an effort to look at the
instance for any obvious problems, but don't spend too much time.

If the performance issue appears to be caused by general lack of resources,
suggest that the customer upgrade to one of our newer plans. Some customers may
qualify for discounts - see [Discontinued Plans](discontinued_plans.html)
