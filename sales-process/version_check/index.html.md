---
layout: markdown_page
title: "GitLab Version Check"
---

[Blog post about version check: https://about.gitlab.com/2015/05/07/version-check/](https://about.gitlab.com/2015/05/07/version-check/)

## What is the functionality of the GitLab Version Check?

GitLab users who open the help page in the web interface or the admin area 
will see an image in the top right corner with the text "up to date" in green,
"new version out" in yellow or "update asap" in red. This enables them to
quickly see if they run an outdated or even vulnerable version of GitLab. 
The version check is enabled by default and can be disabled in the admin area.

## How does the GitLab Version Check work?

Every single time a user opens the help page or the admin area,
the browser of the user requests an image file from version.gitlab.com.
The browser request tells version.gitlab.com the GitLab version which is
currently running and it responds with the appropriate image so the
user can see if the GitLab version is up to date.

## Which information does the browser request contain?

The request contains information about the browser, the
GitLab version and the HTTP referrer. The HTTP referrer is the URL from
which the request was sent. So it is the URL of the help page or the admin
area page of the users GitLab instance. E.g. if you visit the help page on
gitlab.com the HTTP referrer is https://gitlab.com/help. Furthermore the
browser has to send the IP address of the user combined with the request to
receive a response. The IP address won't be saved.

## What is version.gitlab.com?

Version.gitlab.com collects all browser requests mentioned above and adds
them to a database. It saves the HTTP referrer URL, the current GitLab version,
the timestamp of the request and information about the browser. As mentioned
above it does not save IP addresses.

## Why does GitLab save this information?

This information provides better insights into where and how GitLab is
used and helps us to improve GitLab for everyone, for example by seeing which
versions are popular and require a backport of a security fix.

## Who has access to this database?

Only the GitLab team has access to version.gitlab.com.

## Which information can be derived from the HTTP referrer?

The HTTP referrer can contain the local or public hostname or IP address of a
GitLab instance. It depends on how the user accessed the GitLab web interface.
Local hostnames and local IP addresses are only relevant and reachable within
the local network in which the instance is running. Therefore local hostnames
can be named anything, for example 'myownGitLab'. Public hostnames or
IP addresses can contain information about the owner of the host network.
For example if the HTTP referrer contains 'dev.gitlab.com' it is assumable that
this instance is owned by GitLab.

## Limitations

Because an HTTP referrer can be easily spoofed and because a local hostname can
be named anything, it is impossible to be completely sure if any derived
information is actually valid.