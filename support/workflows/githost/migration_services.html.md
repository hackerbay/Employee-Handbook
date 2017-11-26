---
layout: markdown_page
title: Migration Services
category: GitHost
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

## GitHost Migration Services

### Overview

Support offers migration services from private GitLab instances to [GitHost.io](https://githost.io) instances. This document details the process involved in migrating data to a new instance.

**Requirements**

Only the following GitLab instances can be migrated.

1. Current GitLab version or same version as GitHost.io instances
1. Omnibus GitLab installation

### Backup existing GitLab instance

The customer will need to run a backup of their existing instance by using the [backup Rake](doc.gitlab.com/ee/raketasks/backup_restore.html) task.

1. Verify the GitLab version matches the latest version - `sudo gitlab-rake gitlab:env:info`
1. Request the customer creates a new backup (following the steps below):
   1. Create a new backup - `sudo gitlab-rake gitlab:backup:create`
   1. The new backup will be located at `/var/opt/gitlab/backups/{{TIMESTAMP}}_gitlab_backup.tar`
   1. Backup `/etc/gitlab/gitlab-secrets.json`
   1. Compress both the `gitlab_backup.tar` file and `gitlab-secrets.json` file.
   1. Upload backup file to Google drive or any other secure location (e.g S3) and provide the link to support.

### Restore to a new GitHost Instance

1. Ensure the instance has been created and is online, do this through the GitHost.io admin dashboard. 
   1. If the customer is yet to create the instance, request this is done before proceeding with the restore.  
1. SSH into the customer's instance. For information on how to SSH to a GitHost instance see https://dev.gitlab.org/gitlab/GitHost
   1. Download the backup generated earlier (see Backup existing GitLab instance). 
   1. You can use `wget` or `curl` to download the backup. 
   1. Copy the downloaded backup to `/var/opt/gitlab/backups` 
   1. Set the correct permissions - `chown git: /var/opt/gitlab/backups{{TIMESTAMP}}_gitlab_backup.tar`
   1. Stop GitLab services accessing the DB - `sudo gitlab-ctl stop unicorn; sudo gitlab-ctl stop sidekiq`
   1. Restore the backup `sudo gitlab-rake gitlab:backup:restore BACKUP={{TIMESTAMP}}` - More information can be found on the [backup/restore docs](https://docs.gitlab.com/ee/raketasks/backup_restore.html)
   1. Start GitLab - `sudo gitlab-ctl start`
1. Check the instance is online by visiting it directly in your web browser. 
1. Email the customer requesting they check that all data is present. 

#### Google Drive

1. Request the customer shares the link with `@gitlab.com` email account
1. SSH into GitHost instance
1. [Download](https://github.com/prasmussen/gdrive#downloads) the gdrive binary. Use `gdrive-linux-x64` as GitHost instances are x64. Set the correct permissions.

   ```
    curl -L -o "gdrive-linux-x64" 'https://docs.google.com/uc?export=download&id=0B3X9GlR6EmbnQ0FtZmJJUXEyRTA'
    chmod 777 gdrive-linux-x64
   ```

1. Authenticate with Google drive (follow the instructions)

   ```
   ./gdrive-linux-x64 about
   ```

1. Determine the Google Drive file ID. As an example the fileID for the link `https://drive.google.com/open?id=0B7_OwkDsUIgFWXA1B2FPQfV5S8H`, is `0B7_OwkDsUIgFWXA1B2FPQfV5S8H` (the string after `?id=`)

1. Download the file using gdrive

   ```
   ./gdrive-linux-x64 download <FILEID>
   ```

1. Clean up

   **Remove gdrive**

   ```
   rm gdrive-linux-x64
   rm -R ~/.gdrive # this is important as it contains the authentication token
   ```

   **Revoke permissions**

   Visit: https://security.google.com/settings/security/permissions and revoke permissions for the "GDrive App"