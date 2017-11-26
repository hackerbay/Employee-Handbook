---
layout: markdown_page
title: Jenkins
category: Shared Infrastructure
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Jenkins Server

[Jenkins](https://jenkins.io/index.html) is an open source automation 
server which integrates with GitLab. To test and debug we've configured 
a server.

+ HTTP: http://jenkins.gitlap.com:8080
+ HTTPS: https://jenkins.gitlap.com:8443

### Server Access:

All credentials are stored on the Support vault from 1Password, except 
for the DigitalOcean account.

#### Hosted Server

This server is hosted on DigitalOcean, to gain access to this account 
please request credentials on #infrastructure. 
 
The droplet's name is jenkins-ubuntu-staging.  

#### SSH 

The vault holds a private SSH key. Make sure you store it safely and 
change permission to the file with `chmod 400 <key-name>`.

#### Application

The vault entry holds the admin account to be able to login to the 
server, feel free to create your own user. 

### SSL

Jenkins has been configured to use a self-signed SSL certificate for testing purposes. 

The certificate was generated using the following commands:

```
openssl genrsa -out key.pem
openssl req -new -key key.pem -out csr.pem
openssl x509 -req -days 9999 -in csr.pem -signkey key.pem -out cert.pem
rm csr.pem
```

The files `key.pem` and `cert.pem` are located in `/var/lib/jenkins/cert/`

Jenkins configuration file `/etc/default/jenkins`

```
JENKINS_ARGS="--webroot=/var/cache/$NAME/war --httpsPort=8443 --httpsCertificate=/var/lib/jenkins/cert/cert.pem --httpsPrivateKey=/var/lib/jenkins/cert/key.pem --httpPort=8080"
```

#### License

This server doesn't require a license.   

#### Mail

The Jenkins mail service has been configured through a google account. 
Credentials are available.
  
### Server Specs

- DigitalOcean droplet
- 4 GB Memory
- 2 CPUs
- 60 GB SSD Disk
- Region: NYC2
- OS: Ubuntu 14.04.4 x64 

# Jenkins Integration Debugging/Testing

## Running Jenkins locally

Although we have a centralized instance of Jenkins, it's often necessary to
test with a specific version of Jenkins and plugins. In this case, a local
instance of Jenkins will work best.

You will need Java installed on your workstation to start Jenkins. See
http://www.oracle.com/technetwork/java/javase/downloads/index.html for
packages.

Download the desired version of Jenkins from http://mirrors.jenkins-ci.org/war/.
Save/move the `war` file to an easily accessible location. In a console, start
Jenkins with `java -jar /path/to/jenkins.war --httpPort=8081`. The `--httpPort`
is optional, and defaults to `8080`. There are more command-line options
depending on your needs. See
https://wiki.jenkins-ci.org/display/JENKINS/Starting+and+Accessing+Jenkins
for more details.

Open Jenkins in your browser at http://localhost:8081 (using the port specified
previously). Install any plugins, as necessary. Now that Jenkins is configured,
you can test using GDK or another local install of GitLab.

> **Note:** Data is saved to `~/.jenkins/` by default. 
