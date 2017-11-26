---
layout: markdown_page
title: "Setup your own test OpenShift Origin instance for the Idea to Production Demo"
---

## Overview
{:.no_toc}

This document is meant to outline a simple way of setting up an OpenShift Origin
test box for demonstrating our Idea to Production [demo](/handbook/sales/idea-to-production-demo/).


## Hardware and OS Requirements

This setup is meant to work on a Linux or Mac host. Windows is not supported at
this time.

In order to run the demo smoothly, you should have at least 10Gb of RAM available
for the demo, and at least 4 CPU cores.

If you do not have a supported operating system, or enough machine resources, you
can provision a Linux machine in the cloud to run your setup on.

Tested on:
 - [Digital Ocean](https://www.digitalocean.com/): `16 GB RAM / 8 CPUs`
 - [Amazon EC2](https://aws.amazon.com/ec2/): `t2.xlarge`

 You need to have ports `8443` and `80` open to the public for TCP traffic.

## Software Requirements

In order to run the demo, you need to install Docker, the OC Client Tools, and our setup script.


### Install Docker

You will need to install Docker on your OpenShift machine if you have not installed it already.

The best way to install Docker is by going to their [official installation instructions](https://docs.docker.com/engine/installation/)
and following the install instructions for your OpenShift machine's operating system.

The installation steps should walk you through running Docker's Hello World app.
There also be additional instructions on running Docker without the use of sudo,
which is needed for this setup. So to recap what you should done:

- Installed the Docker prerequisites
- Installed Docker
- Started Docker
- Enabled your user to run the docker command without sudo
- Restarted or launched a new terminal to get new user permissions
- Are able to run the following without `sudo`

  ```
  docker run hello-world
  ```

Once Docker is installed and running, we need to configure support for a insecure local registry:

#### Insecure Local Registry on Linux

Configure the Docker daemon with an insecure registry parameter of `172.30.0.0/16`

 - In RHEL and Fedora, edit the `/etc/sysconfig/docker` file and add or uncomment the insecure registry line:

     ```
     sudo vi /etc/sysconfig/docker
     ```

     ```
     INSECURE_REGISTRY='--insecure-registry 172.30.0.0/16'
     ```

 - After editing the config, restart the Docker daemon.

     ```
     sudo systemctl restart docker
     ```

 - In Ubuntu edit `/lib/systemd/system/docker.service` and edit edit the `ExecStart` line:

   ```
   sudo vi /lib/systemd/system/docker.service
   ```

   ```
   ExecStart=/usr/bin/dockerd --insecure-registry 172.30.0.0/16 -H fd://
   ```

 - After editing the config, restart the Docker daemon.

   ```
   sudo systemctl daemon-reload
   sudo systemctl restart docker
   ```

For troubleshooting these steps refer to the [OpenShift cluster up docs](https://github.com/openshift/origin/blob/master/docs/cluster_up_down.md#linux)

#### Insecure Local Registry on Mac

Once Docker is running, add an insecure registry of `172.30.0.0/16`:

 - From the Docker menu in the toolbar, select Preferences...
 - Click on Advanced in the preferences dialog
 - Under Insecure registries:, click on the + icon to add a new entry
 - Enter `172.30.0.0/16` and press return
 - Click on Apply and Restart

For troubleshooting these steps refer to the [OpenShift cluster up docs](https://github.com/openshift/origin/blob/master/docs/cluster_up_down.md#macos-with-docker-for-mac)

On the Mac you will also need to make sure you have enabled Docker to access enough CPU and RAM resources.
THis can be done from the Preferences windows, and you need at least 4 CPUs and 10GB of RAM.

### Install the OC Client Tools

The OC client tools are released with OpenShift Origin and are located on Origin's
[GitHub Releases Page](https://github.com/openshift/origin/releases)

We will be running the Demo using the latest stable release of OpenShift Origin. Currently *1.3.2*

To install the tools, run the following from a terminal on the OpenShift host machine:

1. In a new directory, download and extract the tools:
  - Linux:

    ```
    curl -L  https://github.com/openshift/origin/releases/download/v1.3.2/openshift-origin-client-tools-v1.3.2-ac1d579-linux-64bit.tar.gz | tar -xz
    ```

  - Mac:

    ```
    curl -L -O https://github.com/openshift/origin/releases/download/v1.3.2/openshift-origin-client-tools-v1.3.2-ac1d579-mac.zip
    unzip openshift-origin-client-tools*
    ```

1. Place the tools on your path:
   - Linux:

     ```
     sudo cp openshift-origin-client-tools-*/oc /usr/local/bin/.
     ```

   - Mac:

     ```
     cd openshift-origin-client-tools-*
     sudo chflags nohidden /private
     sudo echo pwd >> /private/etc/paths.d/origin-paths
     export PATH=$(pwd):$PATH
     ```

1. Test that the tools are on your path:

   ```
   oc version
   ```

   Should return version output:

   ```
   oc v1.3.2
   kubernetes v1.3.0+52492b4
   features: Basic-Auth GSSAPI Kerberos SPNEGO
   ```

### Download and install our Setup script

This script will launch OpenShift Origin using Docker by running the cluster up
script. We will use it to provision some storage, and update user permissions on
the cluster to allow the demo to run.

In case you are not running our setup script, and instead already have a OpenShift
cluster setup. We have outlined what the script does [below](#gitlab-plugin-install-source) so you can make similar
changes to your cluster.

1. Get the setup script, in a new directory from your terminal:
   - Linux:

     ```
     curl -L https://gitlab.com/gitlab-org/omnibus-gitlab/repository/archive.tar.gz?ref=i2ptest | tar -zx
     ```

   - Mac:

     ```
     curl -L -O https://gitlab.com/gitlab-org/omnibus-gitlab/repository/archive.zip?ref=i2ptest
     unzip archive.zip*
     ```

1. Place the script on your path:
  - Linux:

    ```
    cd omnibus-gitlab-*
    echo "export PATH=$(pwd)/docker/openshift/oc-cluster-wrapper:\$PATH" >> ~/.bashrc
    export PATH=$(pwd)/docker/openshift/oc-cluster-wrapper:$PATH
    ```

  - Mac:

    ```
    cd omnibus-gitlab-*
    sudo echo $(pwd)/docker/openshift/oc-cluster-wrapper >> /private/etc/paths.d/origin-paths
    export PATH=$(pwd)/docker/openshift/oc-cluster-wrapper:$PATH
    ```

1. Test that the script is on your path:

  ```
  oc-cluster help
  ```

  This should return a list of valid commands.

  ```
  oc-cluster up [profile] [OPTIONS]
  oc-cluster down
  oc-cluster destroy [profile]
  oc-cluster list
  oc-cluster status
  oc-cluster ssh
  oc-cluster console
  oc-cluster completion bash
  oc-cluster plugin-install <plugin>
  oc-cluster plugin-uninstall <plugin>
  oc-cluster plugin-list
  oc-cluster create-volume volumeName [size|10Gi] [path|/root/.oc/profiles/<profile>/volumes/<volumeName>]
  oc-cluster create-shared-volume project/volumeName [size|10Gi] [path|/root/.oc/volumes/<volumeName>]
  ```

## Setup and Run the cluster

1. Find the public hostname and public IP you can use to access the cluster. And export them into your terminal.
   If you don't have a Public DNS entry, you can use `<your public ip>.xip.io`
   - For AWS you must use your DNS for the hostname and `apps.<your public ip>.xip.io` in
     the suffix unless you have setup a wildcarded dns
   - If you are using Digital Ocean, the hostname will work with `<your public ip>.xip.io`
     and suffix with `apps.<your public ip>.xip.io`
   - If you are running locally on you own box, the example provided should work.

   ```
   export OC_CLUSTER_PUBLIC_HOSTNAME=127.0.0.1.xip.io
   export OC_CLUSTER_ROUTING_SUFFIX=apps.127.0.0.1.xip.io
   ```

1. Launch the Cluster:

   ```
   oc-cluster up
   ```

1. Once it is finished it should have given you a link to the web console. If
you are working on a cloud instance, this link will probably be wrong, and showing
and internal IP address.

To access the console open `https://<your public hostname>:8443` in a browser tab.
You will have to accept the invalid certificate.

Then login to OpenShift using username: `developer` password: `developer`

1. In your terminal, install the gitlab plugin:

   ```
   oc-cluster plugin-install gitlab
   ```

   You can read up on what happens during the plugin-install [below](#gitlab-plugin-install-source).

This will output a link to the template you can use for the OpenShift demo. It will also
output the two hostnames you will need to populate the demo with.

## Start the Demo

The output from the previous step should have given you the link to the template.

The rest of the demo process can be mostly followed from the [Demo Script](/handbook/sales/idea-to-production-demo/)
But you will want to use the template link provided from our setup script.

Which is: `https://gitlab.com/gitlab-org/omnibus-gitlab/raw/i2ptest/docker/openshift/idea-2-prod-template.json`

And while filling in parameters for the template, you will need to provide the two custom hostnames.


GitLab Hostname: `gitlab.<your routing suffix>`

Mattermost Hostname: `mattermost.<your routing suffix>`

Note, anywhere else in the demo script that references `tanukionline.com` will be replaced with you DNS name.

### Running the demo multiple times

Because you have limited storage, you will need to uninstall and re-install the gitlab-plugin each time
you want to run the demo. This involves making sure the correct values are on your path:

```
export OC_CLUSTER_PUBLIC_HOSTNAME=127.0.0.1.xip.io
export OC_CLUSTER_ROUTING_SUFFIX=apps.127.0.0.1.xip.io
```

Where the values match what you used during setup.

And then running

```
oc-cluster plugin-uninstall gitlab
oc-cluster plugin-install gitlab
```

### Restart OpenShift after the server has been restarted:

Once again the environment variables need to be set:

```
export OC_CLUSTER_PUBLIC_HOSTNAME=127.0.0.1.xip.io
export OC_CLUSTER_ROUTING_SUFFIX=apps.127.0.0.1.xip.io
```

Where the values match what you used during setup

And then start up the instance:

```
oc-cluster up
```

## GitLab Plugin Install Source

The GitLab plugin that we install to provision the storage and permissions looks like this:

```
# Prefetch the Docker images so the demo is faster
oc import-image gitlab-ce:8.13.0 --from=docker.io/ayufan/gitlab-i2p:latest --confirm
oc import-image gitlab-ce-redis:3.2.3 --from=docker.io/redis:3.2.3-alpine --confirm
oc import-image gitlab-ce-postgresql:9.4 --from=docker.io/centos/postgresql-94-centos7:latest --confirm
oc import-image gitlab-ce-runner:1.7.0 --from=docker.io/gitlab/gitlab-runner:alpine-v1.7.0-rc.2 --confirm

# Allow all logged in users to use the anyuid security context
oc adm policy add-scc-to-group anyuid system:authenticated --as=system:admin

# Create 6 persistent volumes for storage
create-volume pv-gitlab-01
create-volume pv-gitlab-02
create-volume pv-gitlab-03
create-volume pv-gitlab-04
create-volume pv-gitlab-05
create-volume pv-gitlab-06
```

The create volume command used looks like:

```
function create-volume {
  [ $# -lt 1 ] && echo "volumename is required" && exit 1
  local __profile=$(cat $OPENSHIFT_HOME_DIR/active_profile)
  local __volume=$1
  local __size=${2:-"10Gi"}
  local __path=${3:-$OPENSHIFT_HOME_DIR/profiles/${__profile}/volumes/${__volume}}

  [[ ! $__size =~ ^[[:digit:]]+[GM]i$ ]] && echo "Not a valid volume size, use <number>Gi or <number>Mi" && exit 1

  oc get persistentvolume ${__volume} --as=system:admin &>/dev/null && echo "The PersistentVolume already exits" && exit 1

  # Gives 777 permisions to the folder, otherwise non-root cannot write on it
  mkdir -m 777 -p $__path

cat <<-EOF > /tmp/pv.yaml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: ${__volume}
spec:
  capacity:
    storage: ${__size}
  accessModes:
    - ReadWriteOnce
    - ReadWriteMany
  persistentVolumeReclaimPolicy: Recycle
  hostPath:
    path: ${__path}
EOF

oc create -f /tmp/pv.yaml --as=system:admin
rm /tmp/pv.yaml

echo "Volume created in ${__path}"
}
```

The breakdown of what this is doing is as follows:

1. Pre-fetch the container images into OpenShift registry
1. Allow all logged in users to create containers running as root
   - This is done broadly specifically for the demo. So that you can create your project
     later. In a real setup, you would first create your project, then a
     service account specifically for the gitlab-ce container, and grant root only to it.
1. Create the 6 persistent volumes required for the demo
   - These particular ones are set to be hostPath mounted for the single node cluster demo
   - We use the Recycle reclaim policy to remove their directory when they are deleted
