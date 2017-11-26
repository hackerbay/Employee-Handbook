---
layout: markdown_page
title: Checklist for becoming a Docker Expert
---

Create an issue with this checklist on the [support team issue tracker](https://gitlab.com/gitlab-com/support/issues/)
with the **Title:** *"Docker Bootcamp - your_name"*

Tackle stage 1 first and the last stage last, but the others can be completed in
any order you prefer.

```
### Stage 1: Commit and Become familiar with what Docker is

1. [ ] Ping your manager on the issue to notify them you have started.
1. [ ] Notify the current experts that they can start routing easier Docker
       questions to you.
1. [ ] Work through [GitLab University Docker](https://www.youtube.com/watch?v=ugOrCcbdHko).

### Stage 2: Theory (Expense non-free learning materials to GitLab)

1. [ ] Watch Unit 1 & 2 of [Scalable Microservices With Kubernetes](https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615).
1. [ ] Read [Docker in practice, by Miell and Sayers](https://www.manning.com/books/docker-in-practice).
1. [ ] Watch the introductory [Play by Play: Docker for Web Developers course](https://www.pluralsight.com/courses/play-by-play-docker-web-developers-john-papa-dan-wahlin).
1. [ ] Watch the more complete [Docker for Web Developers course](https://www.pluralsight.com/courses/docker-web-development).
1. [ ] Read the docs for the [Docker Registry integrated into GitLab](https://docs.gitlab.com/ce/user/project/container_registry.html).
1. [ ] Read the docs for the [GitLab Docker Images](https://docs.gitlab.com/omnibus/docker/README.html)

### Stage 3: Practical

- [ ] **Done with Stage 3**

1. [ ] Install Docker on your laptop.
1. [ ] On a Digital Ocean droplet, which you can create [here](https://gitlab.com/gitlab-com/environments)
       run the Just GitLab environment in [testlab](https://gitlab.com/gl-support/testlab).
1. [ ] Understand why there are no [host volumes](https://docs.docker.com/engine/tutorials/dockervolumes/)
       being mounted in the above setup, but when installing GitLab in
       production they are highly recommended.
1. [ ] Create a [Dockerfile](https://docs.docker.com/engine/reference/builder/)
       and build an image with it, which runs a web application that you
       otherwise would run on your local machine.
1. [ ] Set up a dev-tools image that has command-line dev tools configured to
       your personal preferences, set up and ready to use as soon as a
       container starts, if you don't have a preferred setup, have at least Vim
       with **ctrl + p** set up to find files, and Oh My Zshell to let you
       know which branch you are on when using Git.
1. [ ] Run Firefox inside a Gui container. It might be easier to borrow a Linux
       Laptop for this or run it in a VM.
1. [ ] Use [Docker Compose](https://docs.docker.com/compose/compose-file/) to
       bring up a [GitLab container](https://docs.gitlab.com/omnibus/docker/README.html#gitlab-docker-images)
       with [Postgres disabled in Omnibus](https://docs.gitlab.com/ce/administration/high_availability/gitlab.html),
       linked to a [Postgres container](https://hub.docker.com/_/postgres/)
       running the database. All configuration should be defined in the
       docker-compose.yml file so that GitLab is 100% operational after running
       `docker-compose up`.

### Stage 4: GitLab CI

1. [ ] Read the docs for the [Using Docker Images](https://docs.gitlab.com/ce/ci/docker/using_docker_images.html)
       with GitLab CI.
1  [ ] Read about [Docker in Docker](https://hub.docker.com/_/docker/) (dind).
1. [ ] Read the docs for building Docker images in GitLab CI with [Docker in Docker](https://docs.gitlab.com/ce/ci/docker/using_docker_build.html).
1. [ ] Get [GitLab CI to build a Docker image](https://docs.gitlab.com/ce/ci/docker/using_docker_build.html)
       and upload it to a GitLab registry.

### Stage 5: Tickets

- [ ] Contribute valuable responses on at least 5 Docker tickets. Even if a ticket seems
too advanced for you to answer. Find the answers from an expert and relay it to
the customer.

   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __
   1. [ ] __

### Stage 6: Quiz?

- [ ] Need link to Quiz here
- [ ] Quiz answers were checked by Kamil, and he said you passed

### Final Stage

- [ ] Your Manager needs to check this box to acknowledge that you finished
- [ ] Send a MR to declare yourself a **Docker Expert** on the team page
```

