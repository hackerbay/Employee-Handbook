---
layout: markdown_page
title: "Monitoring of GitLab.com"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Other Related Pages

- [Production Architecture](production-architecture)
- [GitLab.com Settings](https://about.gitlab.com/gitlab-com/settings/)
- [GitLab performance monitoring documentation](https://docs.gitlab.com/ce/administration/monitoring/performance/introduction.html)
- [Performance of the Application](/handbook/engineering/performance)

## Monitoring

### Pingdom Statistics

For a quick view of the availability and performance history of GitLab.com, we
use <https://stats.pingdom.com>. Specifically, this has the availability and latency of reaching
   - a [GitLab.com issue](http://stats.pingdom.com/81vpf8jyr1h9/1902794/history).
   For reference, it is the [first gitlab-ce issue](https://gitlab.com/gitlab-org/gitlab-ce/issues/1).
   - a [_GitHub.com_ issue](http://stats.pingdom.com/81vpf8jyr1h9/1902795/history).
   For reference, it is the first issue in the [gitlabhq project](https://github.com/gitlabhq/gitlabhq/issues/1).
   - [GitLab.com](https://gitlab.com/) "plain and simple" called the [GitLab public check](http://stats.pingdom.com/81vpf8jyr1h9/646997/history).

### Main Monitoring Dashboards

We collect data using InfluxDB and Prometheus, leveraging available exporters
like the node or the postgresql exporters, and we build whatever else is
necessary. The data is visualized in graphs and dashboards that are built using
Grafana. There are two interfaces to track this, as described in more detail
below.

#### [Public monitoring infrastructure](http://monitor.gitlab.net/)

  - No authentication is required
  - Automatically syncs from the private monitoring infrastructure on every
  chef client execution. **Don't change dashboards here, they will be overwritten.**
  - Refer to this interface by default; only use the private one for those cases
  where the public dashboard is not available.
  - Data gathered in InfluxDB is _not_ currently available in public, since InfluxDB does not scrub access tokens from URLs that are measured.

#### [Private monitoring infrastructure](https://performance.gitlab.net)

  - Private GitLab account is required to access
  - Highly Available setup
  - Alerting feeds from this setup
  - All dashboards here also display on the public monitoring infrastructure.
  - Separated from the public for security and availability reasons, they
  should have exactly the same graphs after we deprecate InfluxDB.

#### Adding Dashboards

To learn how to setup a new graph or dashboard using Grafana, take a look at the following resources

- [Guide to setting up Grafana dashboards by Grafana](http://docs.grafana.org/guides/getting_started/)
- [YouTube video showing how to set up a dashboard](https://www.youtube.com/watch?v=sKNZMtoSHN4&index=7&list=PLDGkOdUX1Ujo3wHw9-z5Vo12YLqXRjzg2)
- The [Grafana repo](https://gitlab.com/gitlab-org/grafana-dashboards) where we keep an archive of InfluxDB dashboards created in Grafana. Use these to see details in the file structure, but note that the repo is truly an archive (nothing populates _from_ it) and can be out of date.
- Need access to add a dashboard? Ask any team lead within the infrastructure team.


### Selection of Useful Dashboards from the Monitoring

#### Blackbox Monitoring

* [GitLab Web Status](http://performance.gitlab.net/dashboard/db/gitlab-web-status): front end perspective of GitLab. Useful to understand how GitLab.com looks from the user perspective. Use this graph to quickly troubleshoot what part of GitLab is slow.
* [GitLab Git Status](http://performance.gitlab.net/dashboard/db/gitlab-git-status): front end perspective of GitLab ssh access.

#### Public Whitebox Monitoring

* [Fleet overview](http://monitor.gitlab.net/dashboard/db/fleet-overview): useful to see the fleet status from the inside of GitLab.com. Use this graph to quickly see if the workers or the database are under heavy load, and to check load balancer bandwidth.
* [Postgres Stats](http://monitor.gitlab.net/dashboard/db/postgres-stats): useful to understand how is the database behaving in depth. Use this graph to review if we have spikes of exclusive locks, active or idle in transaction processes
* [Postgres Queries](http://monitor.gitlab.net/dashboard/db/postgres-queries) use this dashboard to understand if we have blocked or slow queries, dead tuples, etc.
* [Storage Stats](http://monitor.gitlab.net/dashboard/db/storage-stats) use this dashboard to understand storage use and performance.

#### Private Whitebox Monitor

* [Host Stats](http://performance.gitlab.net/dashboard/db/host-stats): useful to dive deep into a specific host to understand what is going on with it. Select a host from the dropdown on the top.
* [Business Stats](http://performance.gitlab.net/dashboard/db/business-stats): shows many pushes, new repos and CI builds.
* [Daily overview](http://performance.gitlab.net/dashboard/db/daily-overview): shows endpoints with amount of calls and performance metrics. Useful to understand what is slow generally.

## Logs

Network, System, and Application logs are processed, stored, and searched using the [ELK stack](https://www.elastic.co/products).
For monitoring system performance and metrics Grafana is still the preferred interface. However, for investigating errors and incidents raw logs are available via Kibana at https://log.gitlap.com.

Kibana dashboards are used to monitor application activity, spam events, transient errors, system and network authentication
events, security events, etc. Commonly used dashboards are the Abuse, SSH, and Rack Attack dashboards.

### Adding dashboards

To learn how to create Kibana dashboards use the following resources:

- [Kibana Dashboard tutorial from Elastic.co](https://www.elastic.co/guide/en/kibana/current/tutorial-dashboard.html)
- [Building a dashboard](https://www.elastic.co/guide/en/kibana/current/dashboard-getting-started.html)
- [Using TimeLion for time series visualization](https://www.elastic.co/guide/en/kibana/current/timelion.html)

## GitLab Profiler

[GitLab profiler data](http://redash.gitlab.com/dashboard/gitlab-profiler-statistics), accessible using your GitLab Google credentials,
is a dashboard with links to
  [request profiles](https://docs.gitlab.com/ee/administration/monitoring/performance/request_profiling.html)
  and SQL queries run when loading pages on GitLab.com.

  To add a page to this dashboard, create a merge request to the
    [gitlab-com/gitlab-profiler](https://gitlab.com/gitlab-com/gitlab-profiler)
    project.

## Instrumenting Ruby to monitor performance

Blocks of Ruby code can be "instrumented" to measure performance.
  - [Documentation of instrumentation](https://docs.gitlab.com/ce/development/instrumentation.html)
 with more detail on [how to implement this](https://docs.gitlab.com/ce/development/instrumentation.html#instrumenting-ruby-blocks)
  - An example of how this is used for GitLab itself, can be found in this [initializer](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/config/initializers/8_metrics.rb).
