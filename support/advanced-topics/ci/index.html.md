---
layout: markdown_page
title: Checklist for becoming a GitLab CI Expert
---

Create an issue with this checklist on the [support team issue tracker](https://gitlab.com/gitlab-com/support/issues/)
with the **Title:** *"Gitlab CI Boot Camp - your_name"*

Tackle stage 1 first and the last stage last, but the others can be completed in
any order you prefer.

```
**Goal of this checklist:** Set a clear path for GitLab-CI training

### Stage 1: Commit and Become familiar with what GitLab CI is

- [ ] **Done with Stage 1**

1. [ ] Ping your manager on the issue to notify them you have started
1. [ ] Commit to this by notifying the current experts that they can start
routing non-technical Gitlab CI questions to you
1. [ ] GitLab University
   1. [ ] [Getting started with GitLab and GitLab CI] (https://about.gitlab.com/2015/12/14/getting-started-with-gitlab-and-gitlab-ci/)
   1. [ ] [Continuous Integration, Delivery, and Deployment with GitLab] (https://about.gitlab.com/2016/08/05/continuous-integration-delivery-and-deployment-with-gitlab/)
   1. [ ] [GitLab Container Registry] (https://about.gitlab.com/2016/05/23/gitlab-container-registry/)
   1. [ ] [GitLab & Docker - Recording] (https://www.youtube.com/watch?v=ugOrCcbdHko&index=12&list=PLFGfElNsQthbQu_IWlNOxul0TbS_2JH-e)
1. [ ] [CI Training Video by Jose Tores] (https://drive.google.com/drive/u/2/folders/0B5OISI5eJZ-DSm14U1RVMERvVmM), [Slides] (https://gitlab-org.gitlab.io/ci-training-slides/#/), [Example App] (https://gitlab.com/gitlab-org/ci-training-sample)

### Stage 2: Basic CI

1. [ ] Read the Table Of Contents for the [.gitlab-ci.yml docs] (https://docs.gitlab.com/ee/ci/yaml/README.html)
   and make sure you know the meaning of every heading.
1. [ ] Setup a repository on GitLab.com and create a .gitlab-ci.yml file to
   get a pipeline running using the free shared runners on GitLab.com this can
   be a basic toy project.
1. [ ] Notice that your build waits in **Pending** until a runner becomes
   available, the next step will solve this.
1. [ ] Install a Runner following the [Setup Instructions](https://docs.gitlab.com/runner/install/)
1. [ ] Read about the different [Executors] (https://docs.gitlab.com/runner/executors/)
1. [ ] Register that runner as a [Specific Runner] (https://docs.gitlab.com/ee/ci/runners/README.html#registering-a-specific-runner)
   on your project
1. [ ] Create an example project on your GitLab instance.
1. [ ] Register a shared runner on your GitLab instance and make sure it can
   successfully run the build for your project.

### Stage 3: Intermediate CI
1. [ ] [Pipelines and builds] (https://docs.gitlab.com/ce/ci/pipelines.html)
1. [ ] [Check status of Pipeline and build] (https://docs.gitlab.com/ce/ci/quick_start/README.html#seeing-the-status-of-your-pipeline-and-builds)
1. [ ] [Docker Images] (https://docs.gitlab.com/ee/ci/docker/using_docker_images.html#using-docker-images)
1. [ ] [Register a Docker Runner] (https://docs.gitlab.com/ee/ci/docker/using_docker_images.html#register-docker-runner)
   and change your `.gitlab-ci.yml` to use a Docker image for your language of
   choice.
1. [ ] [Artifacts] (https://docs.gitlab.com/ce/user/project/builds/artifacts.html)
1. [ ] [Change .gitlab-ci.yml to create artifacts] (https://docs.gitlab.com/ce/user/project/builds/artifacts.html#defining-artifacts-in-gitlab-ci-yml)
1. [ ] Set Maximum Artifacts size in Admin and create artifacts above the limit, then check build log for errors
1. [ ] Review Runner [Troubleshooting guide and try to reproduce issues where possible] (https://docs.gitlab.com/runner/faq/)
1. [ ] Read the rest of the [GitLab CI Documentation](https://docs.gitlab.com/ee/ci/README.html)
1. [ ] Set up a project with a basic web application that has some tests, your
   CI script should deploy it to Heroku when all the tests pass.
1. [ ] Create a basic GitLab pages project on GitLab.com and make sure the CI
   script builds it and that the website is visible afterwards.

### Stage 4: Advanced CI

## Stage 4 is still a rough work in progress, don't work on this until it has
been carefully looked over by someone who is familiar with how CI and containers
are best used together. Remove this warning when Stage 4 has been signed off on.

1. [ ] Set up a registry for your project.
1. [ ] Build a Docker image and upload it to the project registry as part of
   the CI pipeline.
1. [ ] Deploy your application to Kubernetes using the Docker container you built.
1. [ ] Set up review apps to be deployed to Kubernetes.
1. [ ] Create a custom image to speed up your build times by having the
   dependencies pre-installed. The same way it is done for GitLab CE and EE. See
   it in action on the first line [here](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/.gitlab-ci.yml).
1. [ ] Set up a manual deploy step, so that it does not deploy to production
   unless someone clicks the button to do so.
1. [ ] Speed up a pipeline using [caching](https://docs.gitlab.com/ce/ci/yaml/#cache).

### Stage 5: Tickets

- [ ] **Done with Stage 5**

1. [ ] Answer 20 GitLab CI tickets and paste the links here. Even if a ticket seems
too advanced for you to answer. Find the answers from an expert and relay it to
the customer.

  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __
  1. [ ] __

### Stage 6: Pair on Customer Calls

1. [ ] Participate on two customer calls regarding Sales or Troubleshooting GitLab CI.
   1. [ ] call with ___
   1. [ ] call with ___

### Stage 7: Quiz?

- [ ] **Done with Stage 7**

### Final Stage

- [ ] Ask Lee and Kamil to look over this list, send a MR to delete this line after they both satisfied with the list
- [ ] Send a MR to declare yourself a **CI Expert** on the team page
```
