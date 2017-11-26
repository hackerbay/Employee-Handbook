---
layout: markdown_page
title: "Data analysis"
---
## Redash data visualization tool
Redash is a data visualization tool. Currently it has one data source, i.e. the database in `version.gitlab.com`.
This database stores both CE and EE usage pings that are sent from customers who [enabled the feature](https://docs.gitlab.com/ce/user/admin_area/settings/usage_statistics.html).
You can create and save SQL queries that execute against that database, and create charts based on those results, that can be refreshed dynamically.
Log in to `http://redash.gitlab.com` using your GitLab Google credentials.

We are working on adding a second data source for `staging.gitlab.com`, so that we can get production gitlab.com inside Redash as well.

** Note: ** Current Redash admins are Stan, Pablo and Marin.  

## Access data
Follow these steps to get access to raw data from gitlab.com and EE usage pings stored in `version.gitlab.com`.

### Get a GitLab Linux account
Ask production folks (`#infrastructure` channel) to set up a Linux account for you. Mine is `victor`, and is used as an example below.

---

### Access `worker1.staging.gitlab.com` staging rails console
Access the server
```
$ ssh victor@worker1.staging.gitlab.com
```

Run
```
$ sudo gitlab-rails c production
```

---

### Access `db1.staging.gitlab.com` db
As required, ask production folks to refresh the `db1.staging.gitlab.com` db with the `gitlab.com` db.

Access the server
```
$ ssh victor@db1.staging.gitlab.com
```

Run
```
$ sudo gitlab-psql gitlabhq_production
```

---

### Access `version.gitlab.com` db
Access the server
```
$ ssh victor@version.gitlab.com
```

Use `psql`
```
$ sudo su postgres
$ psql
```

Access the db
```
postgres=# \c version_gitlab_com_production
postgres=# \dt
```

---

### Access `piwik.gitlab.com` db
Access the server
```
$ ssh victor@piwik.gitlab.com
```

Use `mysql` and access the db
```
$ sudo mysql --defaults-file=/etc/mysql/debian.cnf
```

Refer to the [Piwik schema](https://developer.piwik.org/guides/persistence-and-the-mysql-backend)

---

### Access db from a sql client
Access db from a sql client for additional features and ease of use. The sql client can connect to your local machine, and tunnel to the server. A suggested native Mac sql client for PostgreSQL is [Postico](https://eggerapps.at/postico/). Ask GitLab to expense a license. Download and install. For MySQL, [Sequel Pro](http://sequelpro.com) (i.e. "Pancakes") is decent.


Set up forwarding through your local machine by running one of the following
```
$ ssh -L5432:localhost:5432 victor@db1.staging.gitlab.com
$ ssh -L5432:localhost:5432 victor@version.gitlab.com
$ ssh -L3306:localhost:3306 victor@piwik.gitlab.com
```

#### `db1.staging.gitlab.com`
Find the database password on `db1.staging.gitlab.com`
```
$ sudo vi /etc/gitlab/gitlab.rb
```
Look at `postgresql['sql_password']`.

In your sql client, connect with
```
host: localhost
port: 5432
username: gitlab
password: <password>
database: gitlabhq_production
```

#### `version.gitlab.com`
Find the database login and password on `version.gitlab.com`
```
$ sudo cat /home/gitlab-version/version-gitlab-com/config/database.yml
```

In your sql client, connect with
```
host: localhost
port: 5432
username: <username>
password: <password>
database: version_gitlab_com_production
```

#### `piwik.gitlab.com`
Find the database login and password on `piwik.gitlab.com`
```
$ sudo vi /etc/mysql/debian.cnf
```

In your sql client, connect with
```
host: 127.0.0.1
port: 3306
username: <username>
password: <password>
database: piwik
```
