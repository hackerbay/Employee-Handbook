---
layout: markdown_page
title: "Build"
---

## Common links

* [Build issue tracker][issue tracker]. If
you need to submit sensitive issue, please use confidential issues.
* [Slack chat channel](https://gitlab.slack.com/archives/build)

## Team responsibility

Build is about how we ship GitLab, and making sure everyone can easily install,
update and maintain GitLab.

This means:

- Make Omnibus packages
- Maintain the official installations on our [installation page](https://about.gitlab.com/installation/)
- Make sure nightly builds are installed on dev.gitlab.org
- Keep the installation and download pages up to date and attractive
- Address community questions in the [omnibus-gitlab issue tracker](https://gitlab.com/gitlab-org/omnibus-gitlab/issues/)
and mentions in GitLab CE/EE repositories on issues with `Build` label
- Maintain infrastructure used by the team

### Projects

| Name | Location | Description |
| -------- | -------- |
| Omnibus Gitlab | [gitlab-org/omnibus-gitlab](https://gitlab.com/gitlab-org/omnibus-gitlab) | Build Omnibus packages with HA support for LTS versions of all major Linux operating systems such as Ubuntu, Debian, CentOS/RHEL, OpenSUSE, SLES |
| Docker GitLab image | [gitlab-org/omnibus-gitlab/docker](https://gitlab.com/gitlab-org/omnibus-gitlab/tree/master/docker) | Build Docker images for GitLab CE/EE based on the omnibus-gitlab package |
| AWS images | [AWS marketplace](https://aws.amazon.com/marketplace/pp/B071RFCJZK?qid=1493819387811&sr=0-1&ref_=srh_res_product_title) | AWS image based on the omnibus-gitlab package |
| Azure images | [Azure marketplace](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/gitlab.gitlab-ee?tab=Overview) | Azure image based on the omnibus-gitlab package |
| Kubernetes helm charts | [charts/charts.gitlab.io](https://gitlab.com/charts/charts.gitlab.io) [Official Helm Charts](https://github.com/kubernetes/charts) | Application definitions for Kubernetes Helm based on the omnibus-gitlab package |
| Redhat Openshift | [Openshift template](https://gitlab.com/gitlab-org/omnibus-gitlab/docker/openshift-template.json) | Template for Openshift Origin based on the omnibus-gitlab package |
| Mesosphere DC/OS package | [Universe repository](https://github.com/mesosphere/universe/tree/version-3.x/repo/packages/G/gitlab) | Package for Mesosphere DC/OS based on omnibus-gitlab package |
| GitLab PCF tile | [gitlab.com/gitlab-pivotal](https://gitlab.com/gitlab-pivotal) | One click installation of GitLab in Pivotal Cloud Foundry based on omnibus-gitlab package |
| GitLab Terraform configuration | [gitlab-terraform](https://gitlab.com/gitlab-terraform) | Terraform configuration for various cloud providers |
| Omnibus GitLab Builder | [GitLab Omnibus Builder](https://gitlab.com/gitlab-org/gitlab-omnibus-builder) | Create environment containing build dependencies for the omnibus-gitlab package |

## How to work with Build

Everything that is done in GitLab will end up in the packages that are shipped
to users. While that sounds like the last link in the chain, it is one of the
most important ones. This means that informing the Build team of a change in an
early stage is crucial for releasing your feature. While last minute changes are
inevitable and can happen, we should strive to avoid them.

We expect every team to reach out to the Build team before scheduling a feature
in an upcoming release in the following cases:

* The change requires a new or an update on a gem with native extensions.
* The change requires a new or updated external software dependency.
  * Also when the external dependency has its own external dependencies.
* The change adds, modifies, or removes files that should be managed by
omnibus-gitlab. For example:
  * The change introduces new directories in the package.
* The change requires a new configuration file.
* The change requires a change in a previously established configuration.

To sum up the above list:

If you need to do `install`, `update`, `make`, `mkdir`, `mv`, `cp`, `chown`,
`chmod`, compilation or configuration change in any part of GitLab stack, you
need to reach out to the Build team for opinion as early as possible.

This will allow us to schedule appropriately the changes (if any) we have to make
to the packages.

If a change is reported late in the release cycle or not reported at all,
your feature/change might not be shipped within the release.

If you have any doubt whether your change will have an impact on the Build team,
don't hesitate to ping us in your issue and we'll gladly help.

## Internal team training

Every Build team member is responsible for creating a training session for the
rest of the team. These trainings will be recorded and available to the whole
team.

### Purpose

The purpose of team training is to introduce the work done to the rest of your team.
It also allows the rest of the team to easily transition into new features and projects
and prepare them for maintenance.

Training should be:

* Providing a high level overview of the invested work
* Describing the main challenges encountered during development
* Explaining the possible pit-falls and specificities

Training *should not* be:

* Replacement for documentation
* Replacement for writing down progress in issues
* Replacement for follow up issues

Simply put, the training is a summation of: notes taken in issues during development,
programming challenges, high level overview of written documentation. Your team
member should be able to take over the maintenance or build on top of your feature
with less effort after they have been part of the training.

*Note* Do not shy away from being technical in your training. You can ask yourself:
What would have been useful for me when I started working on this task? What
would have helped me be more efficient?

### Efficiency of the training

In order to see whether the training is efficient, Build lead will rotate team
members on projects where training was done. For example, if the feature
requires regular releases, the person who gave the training will be considered
a tutor. Different team member will follow the training and documentation and
will ask the original maintainer for help. The new person responsible is now
also responsible for improving the feature. They are now also responsible of
training other team members.

### FAQ

Q: Isn't this double work?
A: No. The training should be prepared while documenting the task.

Q: Won't this slow me down?
A: At the beginning, possibly. However, every hour of the training given will
multiple the value of it by the amount of team members.

Q: Isn't it more useful to let the team check out the docs and ask questions?
A: In an ideal world, possibly. However, everyone has a lot of tasks assigned
and they might not be able to go through the docs until they need to do something.
This might be months later and you, as a person who would give the training, might not
be able help efficiently anymore.

## Public by default

All work carried out by the Build team is public. Some exceptions apply:

* Work has possible security implications - If during the course of work security concerns are no longer valid,
it is expected for this work to become public.
* Work is done with a third party - Only when a third party requests that the work is not public.
* Work has financial implications - Unless financial details can be omitted from the work.
* Work has legal implications - Unless legal details can be omitted from the work.

If you are unsure whether something needs to remain private, check with the team lead.

## Working on dev.gitlab.org

Some of the team work is carried out on our development server at `dev.gitlab.org`.
[Infrastructure overview document](https://docs.gitlab.com/omnibus/release/README.html#infrastructure) lists the reasons.

Unless your work is related to the security, all other work is carried out in projects on `GitLab.com`.

## Resources

When using any of the resources listed below, same rules apply:

* Consider the cost and whether anything can be done to reduce the cost.
* You can boot up as many machines as you need.
* It is your responsibility to clean up after yourself; if a machine is not used,
remove it.
* If you observe any resource that is running for long periods of time,
ask the person responsible whether the machine is still in use.
* Prepend your username to any resource you start. Eg. if your name is Jane Doe, resource
should be named `janedoe-machine-for-testing`.

### GCP

Every team member has access to `testground` project at [Google Cloud Platform](https://console.cloud.google.com/).
If you don't have access, ask the team lead by creating issue in [Build team issue tracker][issue tracker] and label it `Access Request`.

### Digital Ocean

Every team member has access to [dev-resources project](https://gitlab.com/gitlab-com/dev-resources/) which allows everyone
to create and delete machines on demand.

### AWS

Team does not have access to AWS accounts. In case you need an AWS
resource, ask the team lead for access by creating issue in [Build team issue tracker][issue tracker] and label it `Access Request`. Please supply the details
on what type of access you need.

## Cloud Images

The process documenting the steps necessary to update the GitLab images available on
the various cloud providers is detailed on our [Cloud Image Process page](https://about.gitlab.com/cloud-images/).

## Infrastructure

As part of the team tasks, team has responsibility towards the following nodes:

* dev.gitlab.org - GitLab CE running on this server needs to be operational
* omnibus-builder-runners-manager.gitlab.org - GitLab CI runner manager used for spawning build machines
* packages.gitlab.com - To be defined, this is a joint effort between Production and Build at this point as this
server is important part of the infrastructure.

### dev.gitlab.org

Every day at 1:30 UTC, a nightly build gets triggered on dev.gitlab.org. The cron trigger times are currently defined
at [the scheduled pipeline page on dev.gitlab.org](https://dev.gitlab.org/gitlab/omnibus-gitlab/pipeline_schedules).

Every day at 7:20 UTC, the nightly CE packages gets automatically deployed on dev.gitlab.org. Any errors in
the install process will be logged in [Sentry](https://sentry.gitlap.com/gitlab/devgitlaborg/). Slack notifications
will appear in #dev-gitlab.
The cron task is currently defined in [dev.gitlab.org role](https://dev.gitlab.org/cookbooks/chef-repo/blob/4f90a2061a8d1fa2a0c6d5aeb33499df14c040a3/roles/dev-gitlab-org.json#L183-190).

#### Maintenance tasks

Requirements:

* Access to the node
* Depending on whether the task requires permanent changes to `/etc/gitlab/gitlab.rb`, access to the [Chef repo](https://dev.gitlab.org/cookbooks/chef-repo). If you do not have access to this repository, make sure
you create [an issue in Infrastructure issue tracker](https://gitlab.com/gitlab-com/infrastructure/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=)
and label it `access request`.

Teams responsibility is to make sure that the GitLab instance on this server is operational.
The omnibus-gitlab package on this server is a stock package with required configuration to keep it operational.
Regular omnibus-gitlab commands can be used on this node.
If, for some reason, you need to apply a change to `/etc/gitlab/gitlab.rb`, this change
needs to be introduced in the [dev-gitlab-org role](https://dev.gitlab.org/cookbooks/chef-repo/blob/fa6131d9d06299940a72c51cf60ea62c54fe3461/roles/dev-gitlab-org.json).

If you do not have access to this repository, but you need to do a hot-patch or configuration
testing, the following steps can be performed:

* Stop chef-client on this node: `sudo service chef-client stop`.
* Make the necessary change to get the instance running again. If that requires change in gitlab.rb file,
change it manually and run reconfigure.
* Reach out to Production team to get help on getting your `gitlab.rb` configuration
change committed to the Chef server.
* After this has been applied, start the chef-client on the node: `sudo service chef-client start`
* Make sure that any change you did is noted in an issue! It is your responsibility to revert the
change on this node once the fix is in place in the package!

#### Improvements

* [Deploy notifications](https://gitlab.com/gitlab-org/omnibus-gitlab/issues/2543)

### omnibus-builder-runners-manager.gitlab.org

GitLab CI runner manager is responsible for creating build machines for package builds.
This node configuration is managed by [cookbook-gitlab-runner](https://gitlab.com/gitlab-cookbooks/cookbook-wrapper-gitlab-runner).
Configuration values are stored in [the corresponding vault](https://dev.gitlab.org/cookbooks/chef-repo/blob/bb367e272662da9e9efdfd9adec13769e44a9bc3/roles/omnibus-builder-runners-manager.json#L18).

Currently, the version of GitLab CI runner is locked. We aim to be close to the current version of runner in order
to get the fixes that we need without getting into issues that could cause a failure. These failures could prevent
the release from going out so be careful with unnecessary changes on this node.

The runner manager is configured to use two docker machine drivers, "digitalocean" and "scaleway".

The former boots up machines in a Digital Ocean account for package and Docker image builds.
The latter boots up machines in a Scaleway account for Raspberry Pi (arm platform) builds.

#### Maintenance tasks

Requirements:

* Access to the node
* Access to a Chef Vault admin. At minimum, contact the Build Lead for help.

When the version of GitLab CI runner needs to be changed:

  * To be performed by a Chef Vault admin
    * In local clone of Chef Repo, they will need to run `bundle exec rake 'edit_role_secrets[omnibus-builder-runners-manager]'`. This command
  will fetch the secrets from the chef vault and open up your text editor.
    * Change the version of the package listed in the `gitlab-ci-multi-runner` section.
    * After saving the change, there will be a lot of output which also includes deleting of some existing content in the chef vault. This is expected behaviour.
    * Commit.

  * To be performed by any team member:
    * Login to the node and run, `sudo /root/runner_upgrade.sh` to perform the upgrade. This will stop the chef-client service, stop the runner and cleanup the machines,
  run the chef-client to fetch the new version and finally, start gitlab runner again.

When you notice that the builds are pending on our dev.gitlab.org project, it is possible that
the number of failed machines is high. Failed machines prevent the runner manager from
starting up new machines and this can slow down or even block the release.
To resolve this:

  * Login to the omnibus-builder-runners-manager.gitlab.org node
  * Enter the root session: `sudo su`. This is required because `docker-machine` command will list running machines
  for currently active user
  * Run `docker-machine ls`. This will print out the list of machines that are either in `Running`, `Error` or have an empty state.
  * To list only machines in `Error` state, you can use `/root/machines_operations.sh list-failing`
  * To safely clean the machines with `Error` state, run `/root/machines_operations.sh remove-failing`
  * If the machine has an empty state, you can always remove the machine manually or use `docker-machine ls | grep -v 'Running' | awk '{print $1}' | xargs docker-machine rm --force`.
  This line will remove all machines that do not have `Running` state.

### packages.gitlab.com

At this moment, Build team is only the user of packages.gitlab.com. Release packages
are served to our users and customers from our CI on `dev.gitlab.org`.

The duties for this server are yet to be defined with the Production team.

Given that the package server is currently deployed on our own infrastructure,
from an omnibus type package, if Production requires help the team should do a
best effort to help trough any issues.

[issue tracker]: https://gitlab.com/gitlab-org/build/team-tasks
