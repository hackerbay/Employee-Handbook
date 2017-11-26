---
layout: markdown_page
title: Testing Environment
category: General
---

## On this page
{:.no_toc}

- TOC
{:toc}

----


## Testing Environment License

For a test license you can log into the license app with your GitLab login. You can use one of the [shared licenses](https://license.gitlab.com/licenses/1449) or if you need special add-ons, such as geo, you can generate a new one.

Please keep in mind *you can't generate licenses for customers* only for testing
purposes. To generate a new license, log in to the license app and click on the
'New License' green button on the right side of the screen. Click on "You can also manually create a license
without a Zuora subscription" at the bottom of the screen and fill out all non-optional
fields.

## Digital Ocean and Docker Testing Environment

For a Digital Ocean and Docker testing environment [follow this guide](https://docs.gitlab.com/ce/install/digitaloceandocker.html).


## VMWare Testing Environment

This guide involves configuring and setting up VMWare and Docker locally and assumes you're using Mac OS X.

#### Install VMWare

+ Navigate to https://store.vmware.com and purchase “VMware Fusion 8 (for Mac OS X)”
   + Download “VMware Fusion 8 (for Mac OS X)” using the provided link
   + Install VMWare Fusion 8
   + Launch VMWare Fusion
   + Enter license details when prompted

#### Install Docker Toolbox

1. [https://www.docker.com/products/docker-toolbox](https://www.docker.com/products/docker-toolbox)

#### Create new docker host

This command will create a new VMware fusion virtual machine called `gitlab-test-env` that will act as a docker host.

+ CPUs: Same as host (`-1`)
+ RAM: 4GB
+ Name: `gitlab-test-env`
+ Driver: `vmwarefusion`

```
docker-machine create \
--vmwarefusion-cpu-count -1 \
--vmwarefusion-memory-size 4096 \
--vmwarefusion-disk-size 30000 \
--driver vmwarefusion gitlab-test-env
```

+ Resource: https://docs.docker.com/machine/drivers/vm-fusion/

## Creating GitLab test instance

#### Connect your shell to the new machine

In this example we'll create a GitLab EE 8.10.8 instance.

First connect the docker client to the docker host you created previously.

```
eval "$(docker-machine env gitlab-test-env)"
```

You can add this to your `~/.bash_profile` file to ensure the `docker` client uses the `gitlab-test-env` docker host

#### Get the available tags for GitLab
Optionally replace the `ee` in the url with `ce`

```
wget -q https://registry.hub.docker.com/v1/repositories/gitlab/gitlab-ee/tags -O - | sed -e 's/[][]//g' -e 's/"//g' -e 's/ //g' | tr '}' '\n' | awk -F: '{print $3}'
```

#### Create new GitLab container

+ HTTP port: `8888`
+ SSH port: `2222`
   + Set `gitlab_shell_ssh_port` using `--env GITLAB_OMNIBUS_CONFIG `
+ Hostname: IP of docker host
+ Container name: `gitlab-test-8.10`
+ GitLab version: **EE** `8.10.8-ee.0`

#####  Setup container settings

```
export SSH_PORT=2222
export HTTP_PORT=8888
export VERSION=8.10.8-ee.0
export NAME=gitlab-test-8.10
```

#####  Create container
```
docker run --detach \
--env GITLAB_OMNIBUS_CONFIG="external_url 'http://$(docker-machine ip gitlab-test-env):$HTTP_PORT'; gitlab_rails['gitlab_shell_ssh_port'] = $SSH_PORT;" \
--hostname $(docker-machine ip gitlab-test-env) \
-p $HTTP_PORT:$HTTP_PORT -p $SSH_PORT:22 \
--name $NAME \
gitlab/gitlab-ee:$VERSION
```

#### Connect to the GitLab container

##### Retrieve the docker host IP

```
docker-machine ip gitlab-test-env
# example output: 192.168.151.134
```

+ Browse to: http://192.168.151.134:8888/

##### Execute interactive shell/edit configuration

```
docker exec -it $NAME /bin/bash
```

```
# example commands
root@192:/# vi /etc/gitlab/gitlab.rb
root@192:/# gitlab-ctl reconfigure
```

##### How to update gitlab.rb values with sed

For example, to set the **gitlab_shell_ssh** port on a container named
**gitlab-ee** to port **2222**

```
docker exec -it gitlab-ee \
sed -i "s/.*gitlab_shell_ssh_port.*/gitlab_rails['gitlab_shell_ssh_port'] = 2222/g" /etc/gitlab/gitlab.rb

docker exec -it gitlab-ee gitlab-ctl reconfigure
```

#### Resources

+ [https://docs.gitlab.com/omnibus/docker/](https://docs.gitlab.com/omnibus/docker/)
+ [https://docs.docker.com/machine/get-started/](https://docs.docker.com/machine/get-started/)
+ [https://docs.docker.com/machine/reference/ip/](https://docs.docker.com/machine/reference/ip/)
