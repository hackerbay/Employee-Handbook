---
layout: markdown_page
title: "Updating this website using Git"
---

## On this page
{:.no_toc}

- TOC
{:toc}

For more information about using Git and GitLab see [GitLab University](https://docs.gitlab.com/ce/university/).

This is a guide on what you'll need to install and run on your machine to get
Git up and running so you can create your first merge request in minutes! Follow
the numbered steps below to complete your setup.

### 1. Start using GitLab

1. Here's where you can find step-by-step guides on the [basics of working with Git and GitLab](http://doc.gitlab.com/ce/gitlab-basics/README.html). You'll need those later.
1. Create your [SSH Keys](http://doc.gitlab.com/ce/gitlab-basics/create-your-ssh-keys.html).

### 2. Install Git

1. Open a terminal.
1. Check your Git version by executing: `git --version`.
1. If Git is not installed, you should be prompted to install it. Follow this [guide](http://docs.gitlab.com/ce/gitlab-basics/start-using-git.html) to installing Git and
linking your account to Git.

### 3. Install RVM

1. Visit [https://rvm.io](https://rvm.io/).
1. In a terminal, execute: `curl -sSL https://get.rvm.io | bash -s stable`.
1. Close terminal.
1. Open a new terminal to load the new environment.

### 4. Install Ruby and Bundler

1. In a terminal, execute: `rvm install 2.3.3` to install Ruby
   (enter your system password if prompted).
1. Execute: `rvm use 2.3.3 --default` to set your default Ruby to `2.3.3`.
1. Execute: `ruby --version` to verify Ruby is installed. You should see:
   `ruby 2.3.3p222 (2016-11-21 revision 56859)`.
1. Execute: `gem install bundler` to install [Bundler](http://bundler.io/).

### 5. Clone the source of the website and install its dependencies

1. If you set up SSH keys previously, in terminal execute: `git clone git@gitlab.com:gitlab-com/www-gitlab-com.git` to clone the website. If you prefer using https, then execute: `git clone https://gitlab.com/gitlab-com/www-gitlab-com.git`, but note that if you've activated 2FA on your GitLab.com account, you'll need to take some additional steps to set up [personal access tokens](https://gitlab.com/profile/personal_access_tokens). If you ever want to switch between SSH and https, execute `git remote remove origin`, followed by `git remote add origin [..]` where the `[..]` is the part that starts with `git@` for SSH, or with `https:` for https.
1. Execute: `cd www-gitlab-com` to change to the `www-gitlab-com` directory.
1. Execute: `bundle install` to install all gem dependencies.

### 6. Prevent newlines from causing all following lines in a file to be tagged as changed

This is especially a problem for anyone running a Mac OSX operating system. The
command to 'tame' git is `git config --global core.autocrlf input` - execute it.

### 7. Start contributing

Instructions on how to update the website are in the
[readme of www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/README.md).

Most pages that you might want to edit are written in markdown [Kramdown](http://kramdown.gettalong.org/).
Read through our [Markdown Guide](/handbook/product/technical-writing/markdown-guide/) to understand its syntax and create new content.

### Local Checks of Your Changes

#### 1. Preview website changes locally

1. In a terminal, execute: `bundle exec middleman`.
1. Visit http://localhost:4567 in your browser.
1. You will need to install a text editor to edit the site locally. We recommend
   [Sublime Text 3](http://www.sublimetext.com/3) or [Atom](https://atom.io/).

#### 2. Test if all URL links in a page are valid

Until this is automated in CI, a quick way to see if there are any invalid
links inside a page is the following.

1. Install the [check-my-links][https://chrome.google.com/webstore/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf/) extension in Chrome (no other browsers
   support unfortunately).
1. Open the page you wish to preview (see previous step).
1. Click the newly installed extension in the upper right corner of Chrome.

A pop-up window will open and tell you how many links, if any, are invalid.
Fix any invalid links and ideally any warnings, commit and push your changes,
and test again.
