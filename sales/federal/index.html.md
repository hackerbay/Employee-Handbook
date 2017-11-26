---
layout: markdown_page
title: "Demo"
---

## Video
{:.no_toc}

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/PoBaY_rqeKA" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

## Overview
{:.no_toc}

Today, modern software development teams need version control for everything, automated testing, support for complex build and deploy configurations, and end-to-end visibility and traceability so they can work to improve their software development process over time. But for most teams, getting this tooling right is incredibly difficult.

GitLab provides the most efficient platform for software development and delivery, covering the entire lifecycle from idea to production.

This demonstration will highlight [GitLab’s single platform for the full software development lifecycle](https://about.gitlab.com/direction/#scope), from idea to production, through chat, issues, planning, merge request, CI, CD, measurement, and monitoring.

![](handbook/sales/lifecycle.png)

We want to to make sure [everyone can replicate this demo](https://gitlab.com/gitlab-org/gitlab-ce/issues/25986).
We've changed this page to make it work with Google Container Engine (GKE) instead of OpenShift.
If you encounter issues replicating this demo on GKE or on your own Kubernetes cluster please [open an issue](https://gitlab.com/gitlab-org/kubernetes-gitlab-demo/issues/new).
We're still working to improve this demo further, please see [all open idea-to-production issues](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=idea-to-production).

## Table of Contents
{:.no_toc}

- TOC
{:toc}

## Instructions

For GitLab sales people giving this demo, you should skip setting up the cluster and GitLab instance, and instead use `gitlab.i2p.online`. Do the steps for [Create a user](#create-a-user) once, and then start each new demo at [Setup a group and project in GitLab](#set-up-a-group-and-project-in-gitlab). If you've given the demo before, make sure to delete the `minimal-ruby-app` project before starting!

Otherwise, [set up a cluster on Google Container Engine (GKE)](gke-setup) or [set up a cluster on Azure Container Service (ACS)](acs-setup) and install GitLab CE or EE.

## Create a user

*Note: If using a shared demo, each demo-giver only needs to do this once.*

Now let's register a new user in our GitLab server.

> * Click `Register`
> * Create a user with your name and email address (no verification sent)

## Set up a group and project in GitLab

*Note: If using a shared demo, each new demo will start here. Log in at [gitlab.i2p.online](https://gitlab.i2p.online).*

### Create a group

We've got GitLab running and we're logged in. Since we'll want to work as a team, we'll create a GitLab group. Groups allow you to organize projects into directories and quickly gives users access to several projects at once. With GitLab 9.0, you can even nest subgroups under groups to match your org structure. Let’s give ours a unique name.

> * Click hamburger menu in top-left corner > Groups
> * Click `New Group`
> * Give the group a unique name, perhaps the name of the company you're demoing to, or a made up name (all lowercase, no spaces or special characters other than `-`)
> * Change Visibility level to `Public`
> * Leave `Create a Mattermost team for this group` checked
> * Click `Create group`