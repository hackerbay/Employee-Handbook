---
layout: markdown_page
title: JIRA
category: Shared Infrastructure
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

## Jira Server

[Jira](https://www.atlassian.com/software/jira/core) is a project 
management product from Atlassian which integrates with GitLab. To test 
and debug we've configured a server at http://jira.gitlap.com:8080.

We also have a project on GitLab.com configured and ready for any testing
purposes at https://gitlab.com/gitlab-com/jira-test.

### Server Access:

All credentials are stored on the Support vault from 1Password, except 
for the DigitalOcean account.

#### Hosted Server

This server is hosted on DigitalOcean, to gain access to this account 
please request credentials on #infrastructure. 
 
The droplet's name is jira-centos-testing.  

#### SSH 

The vault holds a private SSH key. Make sure you store it safely and 
change permission to the file with `chmod 400 <key-name>`.

#### Application

Two available usernames and their respective passwords are available 
through the vault entry. Please use the stored URL to access the 
application. 

#### License

This is a commercial product for which we hold a 10 user license. Most 
information is available through the vault entry, if there is something 
missing please request by opening an issue and mentioning @balameb.   

The license expires 21 jun 2017 and only covers Jira Core. 

#### Mail

The Jira mail service has been configured through a google account. 
Credentials are available.
 
#### Gravatar

The main account uses Gravatar to look pretty. Credentials are available. 
  
### Server Specs

- DigitalOcean droplet
- 2 GB Memory
- 2 CPUs
- 40 GB SSD Disk
- Region: NYC2
- OS: CentOS 7.2 x64 
