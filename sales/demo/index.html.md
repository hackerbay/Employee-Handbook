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

Today, modern software development teams need version control for everything,
automated testing, support for complex build and deployment configurations, and
end-to-end visibility and traceability so they can work to improve their
software development and operations over time. But for most teams, getting this
tooling right is incredibly difficult.

This demonstration will highlight [GitLab’s single platform for the complete
DevOps lifecycle](https://about.gitlab.com/direction/#scope), from idea to
production, through chat, issues, planning, merge request, CI, CD, and
monitoring.

![](handbook/sales/devops-loop.svg)

If you encounter issues replicating this demo on GKE or on your own Kubernetes
cluster please [open an
issue](https://gitlab.com/charts/charts.gitlab.io/issues/new). We're still
working to improve this demo further, please see [all open idea-to-production
issues](https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=idea-to-production).

A [deep dive on CI/CD](#cicd-deep-dive) is also detailed, along with a video demonstration of the flow.

## Table of Contents
{:.no_toc}

- TOC
{:toc}

## Preparation

> * Disable desktop notifications (on a Mac, top-right corner, option click).
> * Open up new browser window so the audience doesn’t see all your other open tabs.
> * Resize your browser window to something reasonable for sharing. 1280x720 is a good option. [Here](720p.scpt)'s a handy Applescript if you're on a Mac and using Chrome. Add it to your User Scripts folder and how Applescript in your menu bar, and it'll be really easy to trigger.
> * Consider just sharing web browser window so the audience isn’t distracted by notes or other windows.
> * If displaying full-screen, go to 'Displays' settings, Resolution: Scaled, Larger text.
> * Consider opening this page on an iPad that has screen lock disabled.

## GitLab installation

There are four options:

1. [Log in at gitlab.i2p.online](https://gitlab.i2p.online) (for GitLab sales people)
1. [Set up a cluster on Google Container Engine (GKE)](/handbook/sales/demo/gke-setup)
1. [set up a cluster on Azure Container Service (ACS)](/handbook/sales/demo/acs-setup)
1. [Offline local demo environment with Minikube](https://gitlab.com/charts/charts.gitlab.io/blob/add-minikube-support/minikube.md)

<!--### Enable Auto DevOps

> * Log in as administrator
> * Go to Admin Area (wrench icon)
> * Click on `Settings`
> * Under `Continuous Integration and Deployment`, click on `Enabled Auto DevOps (Beta) for projects by default`
> * Click `Save`
> * Log out as administrator-->

## Project set up

### Cleanup

> * Delete previous GitLab groups you made last time
> * Delete previous Kubernetes namespace for projects (`kubectl delete namespace minimal-ruby-app-<initials>-<project-id>`)
> * Delete previous Mattermost team or at least leave Mattermost team

### Create a user

*Note: If using a shared demo, each demo-giver only needs to do this once.*

Now let's register a new user in our GitLab server.

> * Click `Register`
> * Create a user with your name and email address (no verification sent)

### Create a group

We've got GitLab running and we're logged in. Since we'll want to work as a
team, we'll create a GitLab group. Groups allow you to organize projects into
directories and quickly gives users access to several projects at once. With
GitLab 9.0, you can even nest subgroups under groups to match your org
structure. Let’s give ours a unique name.

> * Click hamburger menu in top-left corner > Groups
> * Click `New Group`
> * Give the group a unique name, perhaps the name of the company you're demoing to, or a made up name (all lowercase, no spaces or special characters other than `-`)
> * Change Visibility level to `Public`
> * Leave `Create a Mattermost team for this group` checked
> * Click `Create group`

### Create a project

*Note: If you've given the demo before, make sure to delete the `minimal-ruby-app` project first.*

Now let’s create a new project. I'll start from a really simple example app just
to save myself some typing.

> * Click `New Project`
> * Under `Import project from`, click `Repo by URL`
> * Set `Git repository URL` to `https://gitlab.com/auto-devops-examples/minimal-ruby-app.git`
> * Leave `Project name` as `minimal-ruby-app`
> * Make it public

### Set up Mattermost Command

Now let's get our project connected to the built-in Mattermost. Mattermost is an
open source Slack alternative that comes bundled with GitLab. We also integrate
with Slack so you could use that as your chat client as well.

> * Select `Mattermost Slash Commands`
> * Click `Add to Mattermost`
> * Pick group name from list
> * Click `Install`

### Setup GitLab Auto DevOps

Now we’re ready to configure GitLab Auto DevOps. Auto DevOps is the easiest way
to configure GitLab CI/CD. Back to the project, let’s go the CI/CD settings. We
just need to enable Auto DevOps and give it a base domain. `KUBE_DOMAIN` to use
our own domain.

> * Go to Project, `Settings`
> * Expand `General pipeline settings`
> * Click `Enable Auto DevOps`
> * Change domain to `i2p.online` (or the base domain you are using)
> * `Save changes`

Great, that completes our setup. Now lets kick off the first pipeline.

> * Go to `https://gitlab.i2p.online/<group name>/minimal-ruby-app/pipelines/new`
> * Leave `master` branch
> * `Create pipeline`

As you can see, our first pipeline is now running. This will build our project,
create a container image using our Dockerfile, and then deploy to production.

### Project permissions (optional)

Okay, so everything we need to bring an application from idea to production is
set up. But let's assume you want to safeguard your source code before handing
this over to your developers. I'll take you through a few key ways you can
outline project permissions and manage your team's workflows.

**User roles and permissions**: Since this is a public project, we’ll want to ensure that we have a way to manage what actions each team member can take. For example, we may want only certain people to be able to merge to `master` or to be able to adjust the CI project configuration.

**Change a user’s permission level**: In GitLab, permissions are managed at a user and group level and they apply to projects and GitLab CI. We have five different role types, so you can set granular permissions and keep your code and configurations management secure. To save your admins time and the headache of managing multiple logins, GitLab integrates with your Active Directory and LDAP. You can just connect GitLab to your LDAP server and it will automatically sync users, groups, and admins.

**Project settings**: In addition to permissions, we also have features to help you manage the team’s workflow and bake quality control into your development process.

**Navigate to project settings for protected branches**: It’s no secret that code review is essential to keeping code quality high. But when the team is on a deadline, there could be an incentive to skip code review and force-push changes. Therefore, in addition to permissions, we also allow you to identify protected branches to prevent people from pushing code without review. The `master` branch is protected by default but you can easily protect other branches, like your QA branch, and restrict push and merge access to certain users or groups.

**Navigate to project settings for merge request approvals**: If you want to take code review a step further and ensure your code is always reviewed and signed off by specific team members, you can enable merge request approvals. GitLab lets you set the number of necessary approvals and predefine a list of approvers or approval groups that will need to approve every merge request in the project.

Permissions, merge request approvals, and protected branches help you build
quality control into your development process so you can confidently hand GitLab
over to your developers to get started on turning their ideas into a reality.

## Idea to Production

### Idea (Plan)

Let's start in our Mattermost client. Today, more of your team's conversations
are happening in chat, not in issues. With GitLab's chat command integration,
you can easily turn ideas into issues.

> * Go to Mattermost `https://mattermost.i2p.online` (Change the domain to match the domain used for your GitLab installation)
> * Skip tutorial
> * Type: `/minimal-ruby-app help`

On first use, the command will ask you to connect your GitLab account, which is
as simple as clicking the provided link in the response.

> * Click connect your GitLab account
> * Click Authorize # As of 10.0.3, this will 500. Just close the tab and continue
> * Go to Mattermost
> * Type: `/minimal-ruby-app help`

Great. Now we can see what commands are available. Let's go ahead and create an
issue.

> ```
> /minimal-ruby-app issue new Make homepage more descriptive
> SHIFT ENTER
> Currently it is just Hello World.
> ```

### Issue (Plan)

Great, we’ve created a new issue, directly from chat, and now we can click
through to see our first issue on our new project.

> * Click on the link that starts with #1

### Board (Plan)

Inspiration is perishable, so let's pick this one up right away. As a team lead
or manager, I'd go to the Issue Board.

> Go to `Issues > Board`

Since this is our first time, we have to add a couple columns here to match our
workflow. These columns are fully-customizable and you can have multiple Issue
Boards per project to help your team organize their releases. I'll just add the
default "To Do" and "Doing" columns.

> * `Add default lists`

There. Now we can just add the new issue from the backlog into the Doing column,
because we want to resolve this issue right now.

> * Drag issue from `Backlog` to `Doing`

### Commit (Create)

Now let’s get coding! I'll head over to the Repository and start editing. You
can see that it's a really simple app; basically just Hello World, but with some
random timings to make performance graphs more interesting. I'm going to go
ahead and update the message and remove the TODO comment.

> * Go to `Repository`
> * Go to `server.rb`
> * Click `Edit` button
> * Add `Updated ` in front of  `Hello, world!`
> * Delete the `#TODO: use HTML` line
> DON'T COMMIT

Now instead of committing directly to `master`, I’m going to create a new
branch, named with the issue number.

> * Set target branch to `1-homepage` (no longer than 24 characters)
> * Leave `start a new merge request with these changes` checked
> * `Commit changes`

And now it gives me an option to create a Merge Request, how nice of it. Let's
go ahead and do that. GitLab knows by the branch name that it closes issue #1
and adds that message automatically so we don't have to do anything except hit
submit.

> * Check `Remove source branch when merge request is accepted.`
> * `Submit merge request`
> * If popup asks to show notifications, click Allow.

### Build (Verify)

As soon as the Merge Request is created, we see it automatically kicked off the
CI/CD Pipeline that will test our contributed code.

> * Click on pipeline number on MR widget

Here we see a pipeline that contains 4 stages for Build, Test, Review, and
Cleanup. In the build job, we build the Docker container image and push it to
the built-in container registry.

> * Click on Build

If we didn't have a Dockerfile, it would have used Heroku buildpacks to detect
the language and framework and build an appropriate Docker image.

### Runner progress (optional: if CI/CD is taking a while)

While it’s running, we can head back to our Kubernetes console to see that our
GitLab Runner is working directly with Kubernetes to spawn new containers for
each job, as they are needed. It even creates a namespace for the project,
providing isolation.

> * Go to Kubernetes
> * Change Namespace to `default`
> * Click on Pods
> * Change the Namespace drop-down to `minimal-ruby-app-<number>`
> * Click on Pods

### Test (Verify)

> * Click back (to pipeline view)

In the Test stage we see two jobs.

> * Click `test`

The `test` job detects the language used, again using Heroku buildpacks. In this
case it's Ruby, and so it runs `rake test`.

### Code Quality (Verify)

> * Click back (to pipeline view)
> * Click `codequality`

The other test job, `codequality`, runs static analysis on your code to look for
stylistic and other quality problems.

### Review (Create)

#### Review apps

When the tests pass, it automatically creates a temporary review app in our
Kubernetes cluster.

> * Go Back
> * Click on Review

Here we see a bunch of steps it’s doing automatically for us with the highlight
being a deployment to Kubernetes, using our default Helm chart. If the app had a
Helm chart in the project itself, it would have used that custom chart instead.
Or I can even add a project variable to point to another chart. But here, we’re
using the default.

To see the beauty of the review app, let’s go back to the merge request.

> * Click Back
> * Click Back (again, to get to the MR)
> * Refresh if needed

Here we see a new line showing us that it was deployed to the review app, and
here’s the URL to actually see my change running live. This is great because I
don’t want to trust reading the code; I want to see it live in a production-like
environment and this review app provides that.

* Click on external link to review app

So this is what we just changed, and any new changes pushed to our branch will
automatically update the app.

Now back to the merge request...

> * Close review app tab
> * Click `Expand` on Code quality

We see there’s a new line for the code quality. We see that it likes that we
removed the TODO. If we made things worse, it would show up here as well.

#### Debugging (Terminal)

Now if there were any problems, for example differences between development and
production, and you don't want to keep testing changes by pushing them to source
control, we could debug those problems right here. By clicking the web terminal
button we get a command prompt in the same container as our application.

> * Click on `review/1-homepage`
> * Click Terminal button (on the upper right, 1st on right)

All our files are here. Let's edit the server.rb file.

> * `ls`
> * `vi server.rb`
> * i (to insert)
> * Update text to `Corrected Hello World!`
> * esc (to go back to normal mode)
> * ZZ (to save and close)

Now we’ve saved the changes, let's restart the server.

> * `killall ruby`

And now we can view the web page live to see how we like the changes.

> * Click external URL link on top right (2nd from right)

#### Code review

At this point we'd usually ask for another developer on the team to review our merge request. They can see the exact code that has changed, comment on it, and we'd see a thread of the discussion, as well as get an email notification, of course.

> * Close review app tab
> * Close environment tab
> * Click on `Changes`
> * Click on a changed line to show ability to comment
> * Comment "Looks good", `Comment`
> * Go to `Discussion` tab to see comment

#### Merge to `master`

This all looks great so let’s merge the changes into the `master` branch.

> * Click `Merge`

### Production (Package & Release)

> * Click on `CI/CD > Pipelines`
> * Click on top pipeline

Now we see it’s kicked off a new pipeline. And inside this pipeline, it looks
familiar, but a little different. Instead of creating a review app, this one is
deploying right into production. This is continuous deployment at its best.

#### Environments with deployment history

> * Go to Environments

Going to the Environments page, I see production listed here and the last deploy
happened less than a minute ago. And I can easily click through to see what it
looks like.

> * Click external URL link (left-most button)

There we go! We've got our new text changes; all the way from idea to
production!

> * Close production app tab

### Scaling and Deploy Boards (Configure) (optional: requires GitLab EE)

Now, there’s more to this page. Expanding the environment, I see the deploy
board for `production`. Right now it's only showing a single pod, but let’s go
and scale that up. I’ll go to CI/CD settings and add a project variable to set
the PRODUCTION REPLICAS to 4.

* `Settings -> CI/CD`
* Expand `Secret variables`
* Set key to `PRODUCTION_REPLICAS`
* Set value to `4`
* `Add new variable`

Now let’s go back. And I can redeploy.

* Click back twice to get back to environment list or go to `CI/CD > Environments`
* Click `Re-deploy`
* Open deploy board (triangle next to `production`)

Soon we’ll see the deploy board update in realtime as the fleet rolls out, and
we can wait a bit to see the deploy finish.

### Monitoring (Monitor)

So that's a high level status of the deploy, but how about monitoring the
ongoing health of your app environments? Clicking on the graph icon, I see
response metrics, with latency, error rate, and throughput, and system metrics,
with CPU and memory usage, and all of these are taken from the built-in
Prometheus monitoring, the leading open-source monitoring solution. There’s not
much to see right now, but this will show the last 8 hours so you can monitor
how your app is doing. There's lines for each deploy as well, so you can
corelate changes in performance caused by recent deployments. Application
performance monitoring can help your team be more strategic, preventing errors
vs. simply reacting to them. Imagine if your application monitoring tool could
help you avoid pushing poor-performing code in the first place, saving your
business future downstream costs? That's exactly where we are heading.

### Closing the loop (optional)

Let's close the loop here and go back to our merge request. Since it's already been merged, we have to look for it in the right tab.

> * Go to `Merge Requests > Merged`
> * Click on top merge request

On the merge request, we now see another status showing that this code has
indeed been deployed to production. This is great for managers looking at closed
merge requests to know if they've actually been deployed or not. But we go
further and show feedback about your application's performance, right on the
merge request, telling you how much your memory usage changed before and after
the merge request was deployed.

### Custom pipeline - staging and canary (optional: requires GitLab EE)

So that covers Auto DevOps from build, test, code quality, review app, deploy to
production, and monitoring. Pretty awesome. But what if you want to do something
differently?

Well, here I’ll go to manually set up CI, but instead of having to start from
scratch and re-create all that we just saw, I can pick Auto DevOps from the
templates, and import the whole thing.

> * Go to `Overview`
> * Click on `Set up CI`
> * Pick `Auto DevOps` template

There’s a lot in here, but it’s not as scary as it first looks. And there’s some
helpful tips in here already. Say I’m not ready for continuous deployment to
production, I can just uncomment out this staging job. And if I want to add
canary deployments, I uncomment this one. I then just need to uncomment this one
last line to make my deployments to production manual and I’m ready to go.

> * Remove leading `.` from staging job
> * Remove leading `.` from canary job
> * Remove `#` in front of `when: manual` line in production job

So I save this into master. And now I see another pipeline is kicked off. This
one again looks familiar, but there are two new stages for staging and canary.

> * `Commit changes` to `master`
> * Go to `CI/CD > Pipelines`
> * Click on top pipeline

Let's just wait for staging to finish deploying. There, now we can go back to
environments and see there's a new staging environment. With this configuration
staging is going to be automatically updated with the latest changes.

> * Go to `CI/CD > Environments`
> * Click on `staging` external URL
> * Close staging tab

But production is no longer going to update automatically. When we're ready, we
have to manually promote from staging to production. But we’re not going to ship
directly to the entire production fleet. GitLab supports canary deploys,
basically letting you deploy to a smaller portion of your fleet to reduce risk.
So here I'll click on the `Canary` manual action to start the deployment. And I
can even see my canary deployment happening in the deploy board!

> * Click on `staging` manual action dropdown, select `Canary`
> * Expand staging deploy board

Now there's one new pod in production running the new canary code, and it's
taking a portion of production traffic, but the rest of the pods are still
running the old code. This is a great way to reduce risk in deployments.

When we’ve validated that the canary is working as expected, we can then go and
ship it completely to production. Let's go ahead and do that now.

> * Click on `production` manual action, select `Production`
> * Wait for deployment to finish
> * Click on `production` external URL

Great, now it’s in production!

So whether you want continuous deployment to production, or a continuous
delivery flow that’s more under your control, or even if you want something else
altogether, we’ve got you covered.

> * Close production tab

### Feedback (Cycle Analytics) (optional)

To help you spot bottlenecks in your development process, GitLab has a built-in dashboard that tracks how long it takes the team to move from idea to production.

> * Go to `Overview > Cycle Analytics`

Here we can see some metrics on the overall health of our project, and then a
breakdown of average times spent in each stage on the way from idea to
production. So far, we're doing amazingly well, by completing a release cycle in
minutes.

This is great for managers looking to better understand their company's release
cycle time, which is critical to staying competitive and responding to
customers and changing market needs.

### Instance Monitoring (optional)

Not only does Prometheus monitor your apps, but it monitors the GitLab instance
itself. Let's go to the Prometheus dashboard.

> * Visit Prometheus `https://prometheus.i2p.online`  (Change the domain to match the domain used for your GitLab installation)

Let’s look at a couple simple queries that show how your GitLab instance is
performing. Here’s our CPU usage:

> * Copy `1 - rate(node_cpu{mode="idle"}[5m])` into the Expression bar; hit enter.
> * Click Graph

And then memory usage:

> * Copy `(1 - ((node_memory_MemFree + node_memory_Cached) / node_memory_MemTotal)) * 100` into the Expression Bar; hit enter.

### Conclusion

So that's it. In less than 10 minutes, we took an an idea through the complete
DevOps loop, with issue tracking, planning with an issue board, committing to
the repo, testing with continuous integration, reviewing with a merge request
and a review app, debugging in the terminal, deploying to production, scaling
the application, application performance monitoring, and closing the feedback
loop with cycle analytics. And all of this on top of a container scheduler that
allows GitLab, the GitLab Runners for CI, and the applications that we deploy,
to scale. Welcome to GitLab, the only platform for complete DevOps, helping you
bring modern applications from idea to production, quickly and reliably.

## CI/CD Deep Dive

Let's now switch over to the last portion of our demonstration, a more in-depth look at GitLab CI.

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/pBe4t1CD8Fc?start=1885" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

### Configuration and Integration

Let's start at the top with configuring CI and setting up any required integrations.

#### Connecting to a Repository (Mirroring)

Now, we've already installed GitLab earlier so we will continue on to connecting our source code repository. The vast majority of our customers utilize our built-in Git repository functionality, due to it's great feature set and seamless integration with CI/CD. However for those would like to utilize a different SCM tool, you can connect any Git based repository by simply configuring mirroring.

> Project Settings > Repository > Pull from a remote repository

We'll get started with our built-in repository and a simple Java app which is composed to two parts. A Java library and a front-end service which depends on that library to respond to users with a simple greeting.

#### Integration with Agile Planning Tools (JIRA & Slack)

Similar to the repository, GitLab also includes a powerful set of planning tools as you saw earlier. However we also have great integration options here as well, for example tools like JIRA and Slack. Let's see how these are configured now.

Configuring JIRA takes just a minute or two. We've provided our server's URL, credentials to authenticate, and then our project information: the key and a transition so we can close issues. That's it!

> Project Settings > Integrations > JIRA

Enabling Slack notification and ChatOps commands are similarly easy. For notifications we simply choose what events we want to push to our channel, and then provide a webhook for our Slack server. In this case we are pushing Pipeline events, for both successful and failed pipelines on all branches.

> Project Settings > Integrations > Slack Notifications

#### Working with `.gitlab-ci.yml` (Versioned, Ways to edit)

> Repository

Now, setting up downstream tool integration is accomplished by working with our pipeline definition file, `.gitlab-ci.yml`, which specifies the stages, jobs, and actions we want to perform.

Before we do that though, let's just talk briefly about the various options for working with this file. As you can see, this is file is checked in to our repository, which provides a number of benefits:
* The file is versioned which means pipeline changes can be tested in branches supporting any changes in your app code. Similarly if you need to go back to an old version, perhaps to ship a security release, the associated pipeline will be exactly how you left it for that particular release.
* It also means that there are a large number of ways to work with this file. Nearly all IDE's have direct integration with Git, so you can use your favorite editor. The classic CLI is of course always possible as well, as well as our integrated web based editor that you can see here.

Let's now take a closer look at this file, and how you can define the pipeline and integrate with a wide variety of tools.

#### Settings in `.gitlab-ci.yml` (Self Service, Bash script, Templates)

> Click on the `.gitlab-ci.yml` file to view

At the top of the file we have defined a few global defaults:
* A docker image to run our commands within, in this case the official Maven image
* A few environment variables
* Cache settings, which allow folders to be persisted between jobs to increase performance

Next we start to define our stages and jobs. In GitLab CI, a Pipeline is made up of a series stages. Each stage then contains one or more jobs. There are no limitations on how many jobs a single stage can have.

The stages keyword defines the order the stages should execute in. So our flow will be: build, test, generate docs, release, and then deploy.

##### Build Stage (Maven, Bash scripting)

We then start to define our jobs, or the actions we want to perform.

Our first job is to build our library, which we utilize Maven for. You can see here we simply invoke Maven, as we would as if we were running it on our machines. That is because the script you see here, is actually just Bash script. This means provides a great amount of flexibility, because you can now automate anything you would normally do on your machine.

##### Test Stage (2 jobs, code coverage output, artifacts)

After we built our library, we are now going to test it.

Our test stage includes two jobs: unit tests and static analysis with codeclimate. We are going to leverage Maven again to run our tests, but we'll also include jacoco to generate code coverage reports. We then output the coverage percentage into the build log. The last step in this job is to take our code coverage reports and persist them with GitLab's integrated artifact repository. We do this by simply specifying the folders we want to save.

While that is happening, we will also be running static analysis with codeclimate. Here we override the default image, to utilize the official Docker image. We use that to then execute run Docker-in-Docker, to execute the codeclimate image to analyze our source. Once that is done, we retrieve our JSON report and persist it as an artifact.

##### Doc Stage (Generate, Artifacts)

Here, we are simply generating our javadocs and again retaining them as an artifact.

##### Release Stage (Protected Variable)

Now that we have tested our library, we are ready to release it. We are going to use Maven again to publish our library out to our Packagecloud server. Now you are paying really close attention, you will see we are using a variable we did not define above. That is because this is a credential token, which should not be checked into the repository. Instead, we add this as a Protected Variable in our project settings, which only administrators can view.

##### Deploy Stage (Pages, Cross-Project Pipelines)

Finally we have our last stage, deploy, which includes two jobs.

Our Pages job is slightly unique, in that this is a special job that works in tandem with GitLab Pages, our static site hosting feature. With Pages, deploying a static site is as easy as creating an artifact. We do that here by specifying we will utilize the artifacts of two of our jobs: unit tests and javadocs. This job then copies those into a single directory structure and persists it as an artifact. GitLab Pages will then take this and deploy out to the integrated hosting service, providing an easy and automated way of posting in our case, our code coverage and documentation.

Now for our last job, recall that our Java app was made up of two components: this library and a front-end service which used it. At this point, we've confirmed that all of our tests pass which is a good start. But what about downstream projects that utilize this? Well this job kicks off what we refer to as a cross-project pipeline. We take a stock alpine image, install curl, then use it to trigger the webhook to start a new front-end service pipeline. Confirming downstream projects are not negatively affected by upstream changes is as easy as a few lines of YML.

##### Wrap up (Self-service: no plugins, Flexible: Bash script, Templates)

As you can see, this supports our larger goals of GitLab: scalability, flexibility, and self-service:
* A developer can integrate with any tool they need, without having to worry about installing plugins or involving the administrators. They can simply provide the required container or VM to run the script in, or install their own runner on a machine with the associated requirements.
* Integrating with static analysis and unit testing frameworks is just a lines of code.
* Moving into the Part 2, you can see integrating with build automation tools like Maven is similarly straight forward and easy.
* We also have a collection of templates which can be used to help users get started.

#### Deep Tool Integration & Intelligence (Code Climate, Code Coverage, JIRA Issue)

Now we already showed how easy it is to execute unit tests and static analysis, but our integration goes a lot deeper. I have a pending merge request ready for me to review, so lets take a look.

> Open pending merge request

As a code reviewer, my job is really important: to ensure that only high quality code that meets our standards is merged. To assist in manual review, we often include automated tools to like static analysis and code coverage. However these reports can often be lengthy and tedious to review, leading to decreased usage. With GitLab's holistic vision, we have a unique opportunity so solve these challenges.

So it looks like one of our developers forgot to clean up a stray FIXME comment that was already addressed. Our pipeline succeeded, so that is promising. We built our code, ran our unit tests and static analysis, and generated our javadocs. That's all pretty straight forward, but as you can see our integration goes further with additional intelligence.

Here we've extracted the code coverage from the unit testing job and present it directly on the interface.  We've also done analysis of the codeclimate report. By comparing the results from this branch to the branch we are looking to merge into, we can provide the reviewer with the delta in code quality if this were to be accepted. Instead of sifting through a bunch of results, I'm presented with what is relevant to this change.

Of course down below we can review and collaborate on the actual code changes. But this all looks good, so let's go ahead and merge.

> Merge

Now similar to what you saw earlier with our integrated issue feature, we will go ahead and close the associated JIRA issue as well. Let's take a quick look at this issue.

> Show it is already linked, and now closed. Close tab and return to MR.

### Executing Build Automation

By committing a change to master we now have a new pipeline running, let's take a look to see how it executes and the notifications we receive.

> *Command-Click* on Pipelines to open a new tab, then click on the pipeline we just started on Master to see the overview.

We can now see a real-time overview of our pipeline as it progresses. Our build stage just completed, and you can now see our two test stages executing in parallel.  Let's take a closer look at our unit test job.

#### Unit Tests Job (Maven, Code Coverage, Artifacts)

> Click on `unit tests` job

As before, we get a live look at the build log as it is being executed by our Runner. You can see Maven is executing, and finally our tests have passed. Here is the code coverage output which GitLab is parsing, and our artifacts. On the right hand side, you can see we are presenting the code coverage and also offer a way to browse the artifacts. They can also be accessed in the future by other jobs.

Now lets go take a look at our codeclimate job.

#### Code Climate Job (Docker, Artifact)

> Click on `codeclimate` job from right pane

In this job, you can see us downloading the codeclimate image and executing it. We then collect the output and persist as an artifact. It's that easy.

Going back to pipeline overview, we can check back in on our progress.

> Click on Pipeline # at the top of the page to go back to overview

Our release job is now executing, lets see how that is progressing.

#### Release Job (Protected Variable, Maven deploy)

We're now ready to publish our library to our packagecloud server, utilizing Maven. Remember we had utilized a protected variable for this, to ensure the secure token was not committed into the repository.

> Scroll up in build log to show the environment variable functioning

And that's it, our library is now available for others to consume.

> Go back to pipeline overview

#### Pages Job (as necessary to kill time for success notifications)

In our Pages job, we are leveraging the artifacts we collected in our earlier stages. Here, we simply copy them into a single directory structure, and persist them in a new artifact. Our GitLab Pages service will take over from here to copy our code coverage and documentation to our static site. Note this works with any static site generator as well.

#### Notifications - Success: Browser, Slack, Favicon, Email (off by default)

As you can see from our notifications, our pipeline has succeeded. In the event you didn't catch them all during that flurry, let's review them quickly:

* GitLab itself will alert you via browser notifications when a pipeline succeeds or fails.
* Since we configured Slack notifications, we received a notification there as well. Let's take a look.

> Switch to Slack tab, show notification

* GitLab also updates the favicon for both our MR and pipeline views, indicating we were successful.
* Last we could also have received an email as well, however by default we do not send them for successful pipelines.

> Go back to pipeline overview

#### Cross Project Pipelines (Environment Screen, Registry)

Let's check in and see how our Cross Project Pipeline is doing, for our front-end service.

> Click on downstream stage

Here you can see a relatively simple pipeline:
* We will build project
* Execute our tests
* Package up our JAR file
* Build our Docker container
* Deploy to Production

> Click on Production

Great, it looks like our deploy has finished and our environment is available. You can always get more information on an environment by clicking on it, where we will show you the deploy history as well as options for monitoring and troubleshooting.

We can also get a closer look at our integrated container registry.

> Click on the Registry tab

Here we can a view of all the containers we currently have pushed to the registry, and their associated tags. If we'd like, we can manually remove some if we don't need them anymore. We also provide a tool to manage your containers in bulk, as well.

Aside from an integrated UI, one of the key benefits of integrating the registry is the unified authentication architecture. Instead of having to manage credentials and security on your own, GitLab makes is extremely simple. We provide a simple environment variable to access the registry which is valid for as long as the job is executing.

#### Pipeline Wrap-up (flexible, self-service)

So that's our "Happy Path". With just a few lines of YML we accomplished:

* Integration with Maven, Unit Tests, Code Coverage, and Code Climate
* Generation of Javadocs
* Releasing our library to Package Cloud
* Publishing the latest documentation to our team's site
* And triggering downtream project pipelines to ensure there we no negative impacts

And we did that all without involving a single administrator or opening a ticket. Completely self-service by a developer.

### Negative Path

But you know what? I think we can make some improvements to library.

> Go back to dep.java and edit the bye text.

This library, as you can see, greets and wishes farewell to our users. Let's make it a little more polite though, by saying "Goodbye".

We'll commit this to a new branch, and create a new Merge Request.

> Commit to new branch, create new Merge Request

#### Failed Merge Request (MWPS, GitLab, Slack, Favicon, Email)

Since we've now created a new branch, we have a new Pipeline running. Now if I am the reviewer and already checked out the changes, I can simply click on our Merge When Pipeline Succeeds button. This will automatically merge the issue as long as we have a good pipeline. However if it fails and the developer needs to make a further change, it will of course have to get re-reviewed. This is a great way to save some time for your reviewers, so they aren't waiting until a pipeline complete before moving on.

Now we're going ahead and building the new version of our library, and next up we'll be running our tests. Let's see how our unit tests are going.

> *Command-Click* on `unit tests` job

Uh oh, as you can tell from the notifications it looks like our tests failed. In this case, we changed the message but forgot to update our tests.

Let's quickly review the notifications we received:
* GitLab itself sent a browser notification, indicating the failed pipeline
* With our Slack integration, we received an alert there as well. (Show Slack)
* If you take a look, our favicons also updated to indicate an errors
* And finally since this was a failed pipeline, we received an email alert as well

> Show email tab
> Return to the job log for the unit tests

##### Failed Merge Follow up (New Issue, New Todo)

As you can see we have a wide array of ways to inform users that their pipeline failed. But what is at least as important as notifications, is follow up.

Looking back at our failed job we can see a new button has appeared, to easily create an issue for this problem. Clicking it will open an issue with some helpful information already filled out, like the build log.

Looking at the top right corner of our screen, you may also have noticed we have a new To Do. To dos are essentially an automatic built in tool, to help our users ensure things don't fall into the cracks. For example, you've been mentioned in an issue or comment, or in this case had a failed pipeline.

This way it's easier for users to go about their day, with less repetition, and fewer mistakes.

So that's a quick review of what we would call the "Negative Path". Let's take a look at some of the available options for reviewing pipeline performance.

### Monitoring CI (Pipeline History, CI Monitoring with Prometheus)

> Click on Pipelines tab for the list of all pipelines

First, GitLab retains a complete pipeline history for all current and old pipelines, stages, and jobs. We track the status of each job, but also retain the build logs permanently. As for the artifacts a default expiration can be set to manage space, but it is easily overridden from within the `.gitlab-ci.yml` file.

This page is great for checking out the status of pipelines for a variety of branches, and getting insight into what the CI system is doing.

But that isn't the only way to get an understanding of what the CI system is currently executing. We also offer a wealth of metrics that are tracked with the integrated Prometheus monitoring system. Let's take a look at the public monitoring dashboard for GitLab.com

> Show monitor.gitlab.net

Here you can see a wide variety of metrics, ranging from the number of jobs in each state to how many parallel jobs a given runner is executing. All of these metrics are available not just on SaaS, but also self-hosted as well.

### Analytics (Charts, Static Analysis, Code Coverage, Cycle Analytics, APM)

GitLab also provides methods to understand the health of the CI pipelines for a particular job as well. We have a dedicated analytics page we call Charts, which shows additional information for each project.

> Open Pipelines > Charts

Here you can get insight into the average success rate and execution duration of your pipelines. For us, ours are executing quite quickly, usually under 2 minutes.

We also provide historical insight into how the success rate is changing over time, and the number of jobs executed within the last week, month and year.

And we've already taken a look at some of the other analytics services we offer as part of CI:
* Our static analysis intelligence with codeclimate
* Code coverage parsing
* and cycle analytics, for team health and efficiency.

### GitLab Runner (Shared, Specific, Autoscaling)

Now I've mentioned our Runner a couple times, but we've been mostly looking at what it can do. Next we'll take a few minutes to talk about this important part of GitLab CI.

The GitLab Runner is a small portable app, which we build for a wide variety of platforms. It's essentially the worker bee, which picks up and executes the jobs we specify in our pipelines.

In our Pipelines settings page is where a developer can take a look at the Runner configuration for their project. You will see we have two categories of Runners: shared and specific.

> Go to Settings, Pipelines.

#### Shared (Ease, Speed, Efficient Management)

Shared runners are runners that have been provided by the administrators of the GitLab instance, we've been using one as you can see here. By allowing administrators to provide a shared pool, there are a number of benefits:

* Consolidation of infrastructure, whether cloud or on premise. Cluster and credentials can be centrally managed.
* Reduces effort required to set up CI for each team

But there are some cases where an administrator has not provided a shared pool, or they don't meet your needs.

#### Specific (Self-service, Install)

For these cases, we have the ability for any development team to connect their own Runners. They simply download the Runner, enter in the URL and key, and they are on their way.

Let's take a look at that process now. In the interest of time, I've already downloaded the OS X version.

The first action we want to take is to register our runner:

> gitlab-runner register

During registration we configure a few aspects of the runner:
* We set the URL and token
* Name that we want to appear on the Runner page
* And then any tags we want to specify. Tags allow you to uniquely identify runners with certain properties, for example here we can set `osx` and `xcode8` to identify what we have installed. These are then specified in the `.gitlab-ci.yml` for the job you want to run.

#### Runner Architecture (Shell/SSH, VM, Container, Auto-Scaling)

The last choice we have to make is what mode of operation we want for our Runner. The simplest is Shell, where it executes the script on the machine and account it's installed on.

We then have support for working with images and containers, via virtual box, parallels, and of course Docker. The runner will start the specified image, execute the job, and then clean up. These modes are great for shared runners, because the development team can still bring their own base image to start from.

The last mode of operation, is what we call our auto-scaling runner. We support this on Docker Machine and Kubernetes, and here the Runner will elastically process jobs as needed to process the CI queue.

#### Wrap up (Self-service, Flexible, Scalable)

And that's it for the configuration, we just start our Runner and it is ready to process jobs.

> gitlab-runner start
> Refresh the Runner settings page

This ability of GitLab CI, to allow development teams to set up their own CI infrastructure, is really transformative.

First, self-service: Instead of needing to file a request for a new piece of hardware, wait for the response, justify the changes and cost, have a PO potentially filed... the dev team takes 2 minutes with an old machine from the cabinet an off they go. The dev team is happy and more productive, and the infrastructure is happy they don't have to worry about managing a flock of Mac Minis for the iOS team in their data center.

Second it provides a lot of flexibility. If you need to run jobs on an ARM device, perhaps for Android or Deep Learning, it's as easy as installing the Runner on Android. Need to run something on a mainframe like Linux on Z? Build the runner and away you go. Managing hardware and software dependencies, when something like a container is not possible, could not get any easier.

Last, is scalability. A handful of auto-scaling runners on GitLab.com routinely process over a thousand concurrent CI jobs. If more are needed, simply turn up the dial.

### GitLab Pages

The final area we wanted to discuss was GitLab Pages. As you saw earlier with our Pipeline, we pushed our javadocs and code coverage reports here with just a few lines of YML. This site is then hosted by GitLab at a specific domain, making it easy to publish technical content or even entire websites with CI.

### Wrap (Flexible: Bash it, script it. Self-service: runners, no plugins. Scalable: SaaS scale CI)

To summarize, GitLab CI is flexible. If you can bash it, you can automate it. Self service runners, no plugins. And SaaS scale CI, with auto-scaling.

Questions?
