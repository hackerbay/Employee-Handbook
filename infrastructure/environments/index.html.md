---
layout: markdown_page
title: "Infrastructure Environments"
---


## Environments

### Development

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Development | various | Development| on save | Fixture | individual dev|


  Development happens on a local machine. Therefore there is no way to provide any SLA. Access is to the individual dev. This could be either EE/CE depending on what the developer is working on.

### Demo

  | **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Demo | [spreadsheet](https://docs.google.com/spreadsheets/d/1HZ-7XhDNzdCBxfjzDFIQi7EjliptkpY4CB3LbiLa9MY/edit#gid=0) | Sales| Release | Fixture | Production Team|

  This should be a fully featured version of the current EE release. The high SLA and tightened access is to ensure it is always available for sales. There are no features (feature flags/canary/etc) that we do not ship.

### .org

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| .org | [dev.gitlab.org](dev.gitlab.org) | Tools for Gitlab.com | Nightly | Real Work | Production and build team |

  Currently there are two main uses for the .org envrionment, Builds and repos that are needed in case gitlab.com is offline.  This is a critical piece of infrastructure that is always growing in size due to build artifacts.  There  are discussions to make a new build server where nightly CE/EE builds can be deployed or to move the infra repos to a new host that would be an separate (not gitlab.com) EE instance.

### Review Apps

  | **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Review apps | various | Test proposal| on commit | Fixture | Review app owner |


 ephemeral app environments that are created dynamically every time you push a new branch up to GitLab, and they&#39;re automatically deleted when the branch is deleted. Single container with limited access.

### One-off

  | **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
| one-off  | various | Testing specific features in a large environment | Release + patches | User specific  | Team developing feature |

  This is less of a staging environment more like a large scale development environments. This could be because of the number of repos required, or a full sized db is required. A version of CE/EE is installed and then patches are applied as work progresses. These should be very limited in number.


### Staging


  | **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Staging  | [staging.gitlab.com](http://staging.gitlab.com) | To test master | Nightly | [Pseudonymization of prod](https://en.wikipedia.org/wiki/Pseudonymization) | all engineers |

**version 0.5**

  This is the version we have today. A full environment that is managed by Chef and Terraform(single environment).  This setup can at most be updated nightly\* because it requires an omnibus version to install. This would be a static environment with a pseudonymization production database.  the DB is a snapshot of the pre-prod DB (updated only often enough to keep migration times to a minimum).

 \* or however often we can have an omnibus build created.

**Version 1.0**

K8s &amp; helm charts (cloud native)

   The final version of staging is multiple container deploys managed by K8s via helm charts. This could be mapped to Master and re-deployed every time there is a successful merge to master.  There is already work started to move us to containers.   [https://gitlab.com/gitlab-org/omnibus-gitlab/issues/2420](https://gitlab.com/gitlab-org/omnibus-gitlab/issues/2420)

### Pre-production

  | **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|preprod | [pre.gitlab.com](http://pre.gitlab.com) | Simulate prod | Release Canidate | Weekly copy of Production | Production team |

 The pre-prod environment will be a mirror of the production environment topology, a full production DB and access restrictions. We will utilize end to end tests , via gitlab-qa, to ensure the quality of the deploy. In the future I would like to be able to mirror production traffic into pre-prod. This would make all of pre-prod in effect a canary deploy, except that if it breaks under load, real users are not affected.

## Production

  | **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Production  | [www.gitlab.com](http://www.gitlabc.com) | Production| Release Canidate | Production | Production team |


   Production will be full scale and size with the ability to have a canary deploy. Production has limited access.

## Self-Hosted

| **Name** | **URL** | **Purpose** | **Deploy** | **Database** | **Terminal access** |
| --- | --- | --- | --- | --- | --- |
|Self-Hosted  | various | Self hosted versions of CE & EE | User specific  | User specific  | User specific |

These are environments that are run on-premise by the end-user. We have no influence, access or control of these environments.

