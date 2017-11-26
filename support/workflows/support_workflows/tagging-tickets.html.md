---
layout: markdown_page
title: Tagging Tickets
category: Support Workflows
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

### Tag tickets
{: #tags}

To be able to capture metrics on which topics are most frequently asked about, when you start on a ticket,
add tags to it.

Currently, the tags that are in use are:

- `bug`
- `call` - if the problem results in a screen share
- `CI`
- `Docker`
- `documentation` - if it requires further documentation
- `feature proposal`
- `Importing` - for any issues relating to importing from GH, BB, etc.
- `Jenkins`
- `JIRA`
- `Kerberos`
- `LDAP`
- `release-quality` - for cases where customers specifically comment on regressions and code quality
- `SAML`
- `SSL`
- `UX/UI`


- Tagging tickets will allow us to better capture what topics need to be documented in more detail,
and/or which areas of the product development can use some attention to prevent creating more requests for support.
- Tags cannot be seen by the customers, they are for internal purposes only.


### Tag Locker

The above tags can be added to tickets using the [Tag Locker](https://www.zendesk.com/apps/tag-locker/) app. We use Tag Locker instead of Zendesk's own tagging function since there are tags that are automatically appended to tickets and which trigger certain actions (such as proper SLA settings). Therefore, it is important not to be able to remove certain tags.

Tag Locker can be found on the right side when viewing a ticket. Click the menu button or search for a tag and click the tag text.

![Tag Locker](/images/support/tag_locker.png)

### Adding tags

To add a _new_ tag this list, create a merge request to update this page, and assign the merge request to a Zendesk admin, since admin privileges are required to make tags in Tag Locker.
