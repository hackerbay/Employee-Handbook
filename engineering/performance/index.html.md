---
layout: markdown_page
title: "Performance"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Other Related Pages
{:.no_toc}

- [GitLab.com (infra) architecture](handbook/infrastructure/production-architecture/)
- [Monitoring GitLab.com](handbook/infrastructure/monitoring/)
- [Application Architecture documentation](https://docs.gitlab.com/ce/development/architecture.html)
- [GitLab.com Settings](https://about.gitlab.com/gitlab-com/settings/)
- [GitLab performance monitoring documentation](https://docs.gitlab.com/ce/administration/monitoring/performance/introduction.html)

**Meta issue** to track various issues listed here is at on the [infrastructure tracker](https://gitlab.com/gitlab-com/infrastructure/issues/2373).

## Performance Target

### Speed index

Performance of GitLab and GitLab.com is ultimately about the user experience. As
also described in the [product management handbook](https://about.gitlab.com/handbook/product/#performance),
"faster applications are better applications". Therefore, the target we set for
performance of GitLab.com is based on the [Speed Index](https://sites.google.com/a/webpagetest.org/docs/using-webpagetest/metrics/speed-index)
which is defined as "the average time at which visible parts of the page are displayed".

---

**Target:** Average Speed Index < 2 seconds.

---

There are many other performance metrics that can be useful in analyzing and
prioritizing work, some of those are discussed in the sections
below. But the user experienced Speed Index is the target for the site as a
whole, and should be what everything ties back to in the end.

In everything that is to follow, times are measured from a single geo-location
(in Europe) using ["Cable" connectivity](https://sites.google.com/a/webpagetest.org/docs/using-webpagetest/metrics/speed-index#TOC-5Mbps-Cable)
for that location (5 /1 Mbps).


### Past and Current Performance

The URLs from GitLab.com listed in the table below form the basis for measuring
performance improvements - these are heavy use cases. The times indicate time
passed from web request to "the average time at which visible parts of the page
are displayed" (per the definition of Speed Index). Since the "user" of these
URLs is a controlled entity in this case, it represents an _external_  measure
of "Speed Index".



| Type |  End of Q2-17 | End of Q3-17 | Now |
|------|-------------:|-------------:|-----|
|Issue: [GitLab CE #4058] |  [7365] | [2874] | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |
| Merge request: [GitLab CE !9546] | [9034] | [13161]  | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |
| Pipeline: [GitLab CE pipeline 9360254] | [14454] | [3010] |  [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |
| Repo: [GitLab CE repo] | [3230] | [2189] | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |

<!-- issue links -->
[GitLab CE #4058]: https://gitlab.com/gitlab-org/gitlab-ce/issues/4058
[7365]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
[2874]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
<!-- MR links -->
[GitLab CE !9546]: https://gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546
[9034]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
[13161]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
<!-- Pipeline links -->
[GitLab CE pipeline 9360254]: https://gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254
[14454]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
[3010]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
<!-- Repo links -->
[GitLab CE repo]: http://gitlab.com/gitlab-org/gitlab-ce/tree/master
[3230]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-29-07-44-06/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
[2189]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
---

## Steps

### Web Request
{: #flow-of-web-request}

All items that start with the tachometer (<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>)
symbol represent a step in the flow that we _measure_. Wherever possible, the
tachometer icon links to the relevant dashboard in our [monitoring](handbook/infrastructure/monitoring/).
Each step in the listing below links back to its corresponding entry in the
[goals table](#web-goals-table).


Consider the scenario of a user opening their browser, and surfing to their dashboard
by typing `gitlab.com/dashboard`, here is what happens:

1. <a name="request-reaches-BE"></a> [**User request**](#tb-request-reaches-BE)
    1. <a name="start-request"></a> User enters gitlab.com/dashboard in their browser and hits enter
    1. <a name="lookup-IP"></a> [Lookup IP in DNS](#tb-lookup-IP) (not measured)
       - Browser looks up IP address in DNS server
       - DNS request goes out and comes
    back (typically ~10-20 ms, [data?]; often times it is already cached so
      then it would be faster).
       - For more details on the steps from browser to application, enjoy reading <https://github.com/alex/what-happens-when>
    1. <a name="browser2AzLB"></a> [Browser to Azure LB](#tb-browser2AzLB) (not measured)
       - Now that the browser knows where to find the IP address, browser sends the web
    request (for gitlab.com/dashboard) to Azure's load balancer (LB).
1. <a name="backend-processes"></a> [**Backend processes**](#tb-backend-processes)
    1. <a name="AzLB2HAProxy"></a> [Azure LB to HAProxy](#tb-Az2LB2HAProxy) (not measured)
       - Azure's load balancer determines where to route the packet (request), and
       sends the request to our Frontend Load Balancer(s) (also referred to as
         HAProxy).
    1. <a name="HAProxy-SSL"></a> [HAProxy SSL with browser](#tb-HAProxy-SSL) (not measured)
       - HAProxy (load balancer) does SSL negotiation with the browser
    1. <a name="HAProxy2NGINX"></a> [HAProxy to NGINX](#tb-HAProxy-SSL) (not measured)
       - HAProxy forwards the request to NGINX in one of our front end workers.
       In this case, since we are tracking a web request, it would be the NGINX box in the
         "Web" box in the [production-architecture diagram](/handbook/infrastructure/production-architecture); but alternatively the request can come in via API or a git command
         from the command line, hence the API, and git "boxes" in that diagram.
        - Since all of our servers are in ONE Azure VNET, the overhead of SSL
          handshake and teardown between HAProxy and NGINX should be close to negligible.
    1. <a name="NGINX-buffer"></a> [NGINX buffers request](#tb-NGINX-buffer) (not measured)
       - NGINX gathers all network packets related to the request ("request
       buffering"). The request may be split into multiple packets by the intervening network,
       for more on that, read up on [MTUs](https://en.wikipedia.org/wiki/Maximum_transmission_unit).
       - In other flows, this won't be true. Specifically, request buffering is
       [switched off for LFS](https://gitlab.com/gitlab-org/gitlab-workhorse/issues/130).
    1. <a name="NGINX2workhorse"></a> [NGINX to Workhorse](#tb-NGINX2workhorse) (not measured)
       - NGINX forwards the full request to Workhorse (in one combined request).
    1. <a name="workhorse2various"></a> [Workhorse distributes request](#tb-workhorse2various)
       - Workhorse splits the request into parts to forward to:
       - <a name="workhorse2unicorn"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=13&fullscreen&orgId=1)
       [Unicorn](#tb-workhorse2unicorn).  Time spent waiting for Unicorn to pick up a request is `HTTP queue time`.
       - <a name="workhorse2gitaly"></a> [Gitaly](#tb-workhorse2gitaly) [not in this scenario, but not measured in any case]
       - <a name="workhorse2nfs"></a> [NFS](#tb-workhorse2nfs) (git clone through HTTP) [not in this scenario, but not measured in any case]
       - <a name="workhorse2redis"></a> [Redis](#tb-workhorse2redis) (long polling) [not in this scenario, but not measured in any case]
    1. <a name="unicorn2various"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=2&fullscreen&orgId=1) [Unicorn calls services](#tb-unicorn2various)
       - Unicorn, (often just called "Rails", or "application server"),
       translates the request into a Rails controller request; in this case
       `RootController#index`. The round trip time it takes for a request to
       _start_  in Unicorn and _leave_ Unicorn is what we call `Transaction
       Timings`. RailsController requests are sent to (and data is received from):
       - <a name="unicorn2db"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=9&fullscreen&orgId=1) [PostgreSQL](#tb-unicorn2db) (`SQL timings`),
       - <a name="unicorn2nfs"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/daily-overview?panelId=14&fullscreen&orgId=1) [NFS](#tb-unicorn2nfs) (`git timings`),
       - <a name="unicorn2redis"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/daily-overview?panelId=13&fullscreen&orgId=1) [Redis](#tb-unicorn2redis) (`cache timings`).
       - In this `gitlab.com/dashboard` example, the controller addresses all three [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/rails-controllers?orgId=1&var-action=RootController%23index&var-database=Production).
       - There are usually _multiple_ SQL calls (or file, or cache, etc.) calls for a given
      controller request. These add to the overall timing, especially since they are
      sequential. For example, in
      this scenario, there are [29 SQL calls (search for `Load`)](http://profiler.gitlap.com/20170524/901687e2-9fa1-4256-8414-c4835dc31dbc.txt.gz)
      when this _particular user_ hits `gitlab.com/dashboard/issues`. The number of SQL calls
      will depend on how many projects the person has, how much may already be in cache, etc.
       - Rails tackles the steps within a controller request sequentially.
          In other words if it needs to make calls out to the database and to
          git, it is not set up to those in parallel but rather has to wait for
          the response to the first step before proceeding to the next step.
       - In the Rails stack, middleware typically adds to the number of round trips
       to Redis, NFS, and PostgreSQL, per controller call, in addition to the
       timings of Rails controllers.  Middleware is used for {session state, user
      identity, endpoint authorization, rate limiting, logging, etc} while the
      controllers typically have at least one round trip for each of {retrieve
      settings, cache check, build model views, cache store, etc.}. Each such
      roundtrip is _estimated_ to take < 10 ms.
    1. <a name="unicorn-views"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=8&fullscreen&orgId=1)  [Unicorn constructs Views](#tb-unicorn-views)
         - The construction of views can take a long time (`view timings`).
         In some controllers, data is gathered _first_ after which a view is
         constructed. In other controllers, data is gathered _from within_  a
         View, so that the `view timing` in those cases includes the time it
         took to call NFS, PostgreSQL, Redis, etc. And in many cases, both are done.
         - A particular view in Rails will often be constructed from multiple partial
        views. These will be used from a template file, specified by the controller
        action, that is, itself, generally included within a layout template.
        Partials can include other partials. This is done for good code
        organization and reuse. As an example, when the _particular user_  from the
        example above loads `gitlab.com/dashboard/issues`, there are [56 nested / partial views rendered (search for `View::`)](http://profiler.gitlap.com/20170524/901687e2-9fa1-4256-8414-c4835dc31dbc.html.gz)
         - Partial views may be cached via various [Rails techniques](http://guides.rubyonrails.org/caching_with_rails.html), such as Fragment Caching. In addition,
         GitLab has a Markdown cache stored in the database that is used to
         speed up the conversion of Markdown to HTML.
         - Perceived performance in the way of First Paint can be affected by
         how much of the content of a view is rendered by the backend vs.
         sending a "minimal" html blob to the user and relying on Javascript /
         AJAX / etc. to fetch additional elements that take the page from First
         Paint to "Fully Loaded". See the section about the frontend for more on this.
    1. <a name="unicorn2html"></a> [Unicorn makes HTML](#tb-unicorn2html) (not measured)
        - Once the Views are built, Unicorn completes making the "HTML blob" that
        is then returned to the browser.
        - Some of these blobs are expensive to compute, and are sometimes hard-coded
      to be sent from Unicorn to Redis (i.e. to cache) once rendered.
    1. <a name="html2browser"></a> [HTML to Browser](#tb-html2browser) (not measured)
       - The HTML blob is sent back to the Browser via the following path:
       - <a name="unicorn2workhorse"></a> [Unicorn to Workhorse](#tb-unicorn2workhorse) (not measured)
       - <a name="workhorse2NGINX"></a> [Workhorse to NGINX](#tb-workhorse2NGINX) (not measured)
       - <a name="NGINX2HAProxy"></a> [NGINX to HAProxy](#tb-NGINX2HAProxy) (not measured)
       - <a name="HAProxy2AzLB"></a> [HAProxy to Azure LB](#tb-HAProxy2AzLB) (not measured)
       - <a name="AzLB2browser"></a> [Azure LB to Browser](#tb-AzLB2browser) (not measured)
1. <a name="renderpage"></a> [**Render Page**](#tb-renderpage)
    1. <a name="browser-firstbyte"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/gitlab-web-status?refresh=1m&panelId=14&fullscreen&orgId=1&from=now-90d&to=now) [**First Byte**](#tb-browser-firstbyte)
      - The time when the browser receives the [first byte](/handbook/glossary/#first-byte).
      In addition to everything in the backend, this also depends on network speed.
      In the dashboard linked to by the tachometer above, First Byte is measured
      from a Digital Ocean box in the US with relatively little network lag thus
      representing an estimate of _internal_ First Byte. Past performance on
      first byte is recorded [elsewhere on this page](#first-byte-external).
      - For any page, you can use your browser's "inspect" tool to look at "TTFB" (time to first byte).
      - [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/)
      `First Byte - External` is measured for a hand selected number of URLs using [SiteSpeed](https://sitespeed.io)
    1. <a name="reaching-speed-index"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) [**Speed Index**](#tb-reaching-speed-index)
      - Browser parses the HTML blob and sends out further requests
      to GitLab.com to fetch assets such as javascript bundles, CSS, images, and
      webfonts.
      - The timing of this step depends (amongst other things) on the number and
      the size of assets, as well as network speed. For _each_ static asset, there is a
      round-trip of:
            - for cached assets: browser <i class="fa fa-long-arrow-right fa-fw"
           aria-hidden="true"></i> nginx <i class="fa fa-long-arrow-right fa-fw"
           aria-hidden="true"></i> nginx confirms cached asset is still valid <i
           class="fa fa-long-arrow-right fa-fw" aria-hidden="true"></i> browser
            - for non-cached or expired cached assets: browser <i class="fa
           fa-long-arrow-right fa-fw" aria-hidden="true"></i> workhorse <i class="fa
           fa-long-arrow-right fa-fw" aria-hidden="true"></i> workhorse grabs asset
           from local cache <i class="fa fa-long-arrow-right fa-fw"
         aria-hidden="true"></i> browser.
            - for a page that is served through GitLab Pages: browser <i class="fa
           fa-long-arrow-right fa-fw" aria-hidden="true"></i> pages daemon
           (independent service in the architecture) <i class="fa fa-long-arrow-right
           fa-fw" aria-hidden="true"></i> browser.
      - Stylesheets can block page rendering by default, which can lead to
      unnecessary delays in page rendering.
      - Starting in 9.5, scripts won't block rendering anymore as they are
      loaded with `defer="true"`, so they are parsed and executed in the same
      order as they are called but only after html + css has been rendered.
      - Enough meaningful content is rendered on screen to calculated the "Speed Index".
    1. <a name="reaching-fullyLoaded"></a> [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) [Fully Loaded](#tb-reaching-fullyLoaded)
      - When the scripts are loaded, Javascript compiles and evaluates them within the page.
      - On some pages, we use AJAX to allow for async loading. The AJAX call can
      be triggered by all kinds of things; for example a frontend element (button)
      or e.g. the `DOMContentLoaded` event. The new call is for a new URL, and such requests are routed either
      through the Web or API workers, invoke their respective Rails controllers
      on the backend, and return the requested files (HTML, JSON, etc).
      For example, the calendar and activity feeds on a username page `gitlab.com/username`
      are two separate AJAX calls, triggered by `DOMContentLoaded`. (The
      `DOMContentLoaded` event "marks the point when both the [DOM](https://css-tricks.com/dom/)
      is ready and there are no stylesheets that are blocking JavaScript
      execution" (taken from an article about the [critical rendering
      path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp))).
      The alternative to using AJAX would be to include the full Rails code to
      generate the calendar and activity feed within the same controller that
      is called by the gitlab.com/username URL; which would lead to slower First
      Paint since it simply involves more calls to the database etc.


---

### Git Commit Push

First read about the [steps in a web request](#flow-of-web-request) above, then pick up the
thread here.

After pushing to a repository, e.g. from the _web UI_:

1. In a web browser, make an edit to a repo file, type a commit message, and
 hit "Commit"
1. NGINX receives the git commit and passes it to Workhorse
1. Workhorse launches a `git-receive-pack` process (on the workhorse machine)
to save the new commit to NFS
1. On the workhorse machine, `git-receive-pack` fires a [git hook](/glossary/#git-hook)
to trigger `GitLab Shell`.
   - GitLab Shell accepts Git payloads pushed over SSH and acts upon them (e.g.
     by checking if you're authorized to perform the push, scheduling the data
     for processing, etc).
   - In this case, GitLab Shell provides the `post-receive` hook, and
the `git-receive-pack` process passes along details of what was pushed to the
repo to the `post-receive` hook. More specifically, it passes a list of three items: old
revision, new revision, and ref (e.g. tag or branch) name.
1. Workhorse then passes the `post-receive` hook to Redis, which is the Sidekiq queue.
   - Workhorse informed that the push succeeded or failed (could have failed due to the repo not available, Redis being down, etc.)
1. Sidekiq picks up the job from Redis and removes the job from the queue
1. Sidekiq updates PostgreSQL
1. Unicorn can now query PostgreSQL.

---

## Goals

### Web Request

Consider the scenario of a user opening their browser, and surfing to their
favorite URL on `GitLab.com`. The steps are described in the section on
["web request"](#flow-of-web-request). In this table, the steps are measured and
goals for improvement are set.

Guide to this table:
- All times are reported in milliseconds.
- `# per request` : average number of times this step occurs per request. For
instance, an average "transaction" may require [0.2 SQL calls, 0.4 git calls, 1
call to cache](https://docs.google.com/spreadsheets/d/15mhXjwkx2lOXJps7lsp_o0zbwGSyOdYOTc8-McwBy0A/pubhtml),
and 30 nested views to be built.
- `p99 Q2-17`: the p99 timing (in milliseconds) at the end of Q2, 2017
- `p99 Now`: link to the dashboard that displays the _current_ p99 timing
- `p99 Q3-17`: the target for the p99 timing by the end of Q3, 2017
- Numbers in _italics_ are _per event_  and/or _in parallel_  with other timings,
and therefore do not sum to the (sub)totals. The non-italic numbers _do_ sum to the (sub)totals.

<a name="web-goals-table"></a>

| Step                                                    | # per request | p99 Q2-17 | p99 Now | p99 Q3-17 goal | Issue links and impact |
|---------------------------------------------------------|--------------:|--------:|--------:|-------------:|------------------------|
| <a name="tb-request-reaches-BE"></a>[**USER REQUEST**](#request-reaches-BE) |               |         |         |              |                        |
| <a name="tb-lookup-IP"></a>[Lookup IP in DNS](#lookup-IP)                          |     1         |~10| ? |~10|  [Use a second DNS provider](https://gitlab.com/gitlab-com/infrastructure/issues/1711)  |
| <a name="tb-browser2AzLB"></a>[Browser to Azure LB](#browser2AzLB)                    |     1         |~10| ? |~10|                        |
| <a name="tb-backend"></a>[**BACKEND PROCESSES**](#backend-processes) |    |         |         |              | [Extend monitoring horizon](https://gitlab.com/gitlab-com/infrastructure/issues/1879) |
|<a name="tb-AzLB2HAProxy"></a>[Azure LB to HAProxy](#AzLB2HAProxy)                     |     1         |~2| ? |~2|                        |
|<a name="tb-HAProxy-SSL"></a>[HAProxy SSL with Browser](#HAProxy-SSL)                 |     1         |~10| ? |~10| [Speed up SSL](https://gitlab.com/gitlab-com/infrastructure/issues/2321) |
|<a name="tb-HAProxy2NGINX"></a>[HAProxy to NGINX](#HAProxy2NGINX)              |     1         |~2| ? |~2|                        |
|<a name="tb-NGINX-buffer"></a>[NGINX buffers request](#NGINX-buffer)                   |     1         |~10| ? |~10|                        |
|[<a name="tb-NGINX2workhorse"></a>NGINX to Workhorse](#NGINX2workhorse)          |     1         |~2|  ? |~2|                        |
|<a name="tb-workhorse2various"></a>[Workhorse distributes request](#workhorse2various)      |     1         |         |         |      | [Adding monitoring to workhorse](https://gitlab.com/gitlab-com/infrastructure/issues/2025) |
|<a name="tb-workhorse2unicorn"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to Unicorn_](#workhorse2unicorn) | 1 | 18  | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=13&fullscreen&orgId=1) | 10 | [Adding Unicorns](https://gitlab.com/gitlab-com/infrastructure/issues/1883) |
|<a name="tb-workhorse2gitaly"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to Gitaly_](#workhorse2gitaly)   | |     | ?  |     |   |
|<a name="tb-workhorse2nfs"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to NFS_](#workhorse2nfs)         | |     | ?  |     |   |
|<a name="tb-workhorse2redis"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to Redis_](#workhorse2redis)      | |     | ?  |     |   |
|<a name="tb-unicorn2various"></a>[Unicorn calls services](#unicorn2various)          |  1  |  2500       | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=2&fullscreen&orgId=1)  |  1000 | [Allow more GitLab internals monitoring](https://gitlab.com/gitlab-org/gitlab-ce/issues/28465)    |
|<a name="tb-unicorn2db"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn_ <i class="fa fa-arrows-h fa-fw" aria-hidden="true"></i> _Postgres_](#unicorn2db)      | | _250_ |[<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=9&fullscreen&orgId=1)| _100_ | [Speed up slow queries](https://gitlab.com/gitlab-org/gitlab-ce/issues/34535)  |
|<a name="tb-unicorn2nfs"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn <i class="fa fa-arrows-h fa-fw" aria-hidden="true"></i> NFS_](#unicorn2nfs)          | | _460_ | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/daily-overview?panelId=14&fullscreen&orgId=1)  | _200_ | [Move to Gitaly](https://gitlab.com/gitlab-org/gitaly/issues/313) - [sample result](https://gitlab.com/gitlab-com/infrastructure/issues/1912#note_31368476) |
|<a name="tb-unicorn2redis"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn <i class="fa fa-arrows-h fa-fw" aria-hidden="true"></i> Redis_](unicorn2redis)       | |  _18_ | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/daily-overview?panelId=13&fullscreen&orgId=1) |     |   |
|<a name="tb-unicorn-views"></a>[Unicorn constructs Views](#unicorn-views) |  | 1500   | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=8&fullscreen&orgId=1)  |  |       |
|<a name="tb-unicorn2html"></a>[Unicorn makes HTML](#unicorn2html) |  |    |   |  |       |
|<a name="tb-html2browser"></a>[HTML to Browser](#html2browser) |  |    |   |  |       |
|<a name="tb-unicorn2workhorse"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Unicorn to Workhorse_](#unicorn2workhorse) | 1 | ~2 | ?  | ~2  |  |
|<a name="tb-workhorse2NGINX"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Workhorse to NGINX_](#workhorse2NGINX)             |      1        | ~2| ? |~2|                        |
|<a name="tb-NGINX2HAProxy"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_NGINX to HAProxy_](#NGINX2HAProxy)                 |      1        |~2| ? |~2| [Compress HTML in NGINX](https://gitlab.com/gitlab-org/gitlab-ce/issues/33719)  |
|<a name="tb-HAProxy2AzLB"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_HAProxy to Azure LB_](#HAProxy2AzLB)               |      1        |~2| ? |~2|                        |
|<a name="tb-AzLB2browser"></a>&nbsp;&nbsp;&nbsp;&nbsp;[_Azure LB to Browser_](#AzLB2browser)               |      1        |~20| ? |~20|                        |
|<a name="tb-renderpage"></a>[**RENDER PAGE**](#renderpage) |  |         |         |              |                        |
|<a name="tb-browser-firstbyte"></a> [**FIRST BYTE**](#browser-firstbyte) (see [note 1](#note-blackbox))]  |   | **1080 - 6347** |   [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](https://performance.gitlab.net/dashboard/db/gitlab-web-status)      | **1000**  |                        |
|<a name="tb-reaching-speed-index"></a>[**SPEED INDEX**](#reaching-speed-index) (see [note 2](#note-fp-times)) |  | **3230 - 14454** | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/)  |   **2000**     | [Remove inline scripts](https://gitlab.com/gitlab-org/gitlab-ce/issues/34903), [Defer script loading when possible](https://gitlab.com/gitlab-org/gitlab-ce/merge_requests/12759), [Lazy load images](https://gitlab.com/gitlab-org/gitlab-ce/issues/34361), [Set up a CDN for faster asset loading](https://gitlab.com/gitlab-com/infrastructure/issues/2092), [Use image resizing in CDN](https://gitlab.com/gitlab-org/gitlab-ce/issues/34364) |
|<a name="tb-reaching-fullyLoaded"></a>[Fully Loaded](#reaching-fullyLoaded) (see [note](#note-fl-times)) |  |   6093 - 14003   |  [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/)  |  not specified  |   [Enable webpack code splitting](https://gitlab.com/gitlab-org/gitlab-ce/issues/33391) |
|---------------------------------------------------------|---------------|---------|---------|--------------|------------------------|


**Notes:**
- 1\. <a name="note-blackbox"></a> The range here corresponds to the range in First Byte times
of the 4 sample URLs provided in the First Byte [table](#first-byte). However, based on all _non-staging_
URL's measured in [this dashboard](https://performance.gitlab.net/dashboard/db/gitlab-web-status?refresh=1m&panelId=14&fullscreen&orgId=1&from=now-90d&to=now),
between 2017-03-30 and 2017-06-28, the number would be 3,833 ms.
- 2\. <a name="note-fp-times"></a> The range here corresponds to the range in Speed Indices
of the 4 sample URLs provided in the Speed Index [table](#speed-index).
- 3\. <a name="note-fl-time"></a> The range here corresponds to the range in Fully Loaded times
of the 4 sample URLs provided in the Speed Index [table](#speed-index).


### Git Commit Push

_Table to be built; merge requests welcome!_


## Modifiers

For any performance metric, the following modifiers can be applied:
- **User**: how a _real_  GitLab user would experience and measure the time.
- **Internal**: the time as measured from _inside_  GitLab.com's infrastructure (the
  boundary is defined as being at the "network | Azure load balancer" interface).
- **External**: the time as measured from any specified point outside GitLab.com's
infrastructure; for example a DO box with Prometheus monitoring or a browser in
a specified geo-region on a specified network speed.

## First byte

### External

Timing history for First Byte are listed in the table below (click
on the tachometer icons for _current_ timings). All times are in milliseconds.

| Type |  End of Q2-17 | End of Q3-17 | Now |
|------|-------------:|-------------:|-----|
|Issue: [GitLab CE #4058] |  [3693] | [1874] | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |
| Merge request: [GitLab CE !9546] | [6347] | [11547]  | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |
| Pipeline: [GitLab CE pipeline 9360254] | [2987] | [1512] |  [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |
| Repo: [GitLab CE repo] | [1071] | [1096] | [<i class="fa fa-tachometer fa-fw" aria-hidden="true"></i>](http://207.154.197.115/gl/sitespeed-result/gitlab.com/) |

<!-- issue links -->
[GitLab CE #4058]: https://gitlab.com/gitlab-org/gitlab-ce/issues/4058
[3693]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
[1874]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/issues/4058/index.html
<!-- MR links -->
[GitLab CE !9546]: https://gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546
[6347]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
[11547]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/merge_requests/9546/index.html
<!-- Pipeline links -->
[GitLab CE pipe 9360254]: https://gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254
[2987]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-27-08-18-14/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
[1512]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/pipelines/9360254/index.html
<!-- Repo links -->
[GitLab CE repo]: http://gitlab.com/gitlab-org/gitlab-ce/tree/master
[1071]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-06-29-07-44-06/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html
[1096]: http://207.154.197.115/gl/sitespeed-result/gitlab.com/2017-10-09-12-10-12/pages/gitlab.com/gitlab-org/gitlab-ce/tree/master/index.html


### Internal
{: #first-byte-internal}

To go a little deeper and measure performance of the application & infrastructure without
consideration for frontend and network aspects, we look at "transaction timings"
[as recorded by Unicorn](#unicorn2various). These timings can be seen on the
[Rails Controller dashboard](https://performance.gitlab.net/dashboard/db/rails-controllers?orgId=1&var-action=Projects::MergeRequestsController%23show&var-database=Production) _per URL that is accessed_ .

For instance, to get the transaction timing for the merge request referenced
above first visit the merge request page, then visit the Rails Controller
dashboard and scroll down to the [Transaction Details table](https://performance.gitlab.net/dashboard/db/rails-controllers?panelId=11&fullscreen&orgId=1&var-action=Projects::MergeRequestsController%23show&var-database=Production).
We do not currently have time series graphs _per URL_ nor do we have specific targets in terms of what this timing should be.

## Availability and Performance Priority Labels
{: #performance-labels}

To clarify the priority of issues that relate to GitLab.com's availability and
performance consider adding an _Availability and Performance Priority Label_,
`~AP1` through `~AP3`. This is similar to what is in use in the Support and
Security teams, they use [`~SP`](https://about.gitlab.com/handbook/support/workflows/support_workflows/issue_escalations.html#support-priority-labels)
and [`~SL`](https://about.gitlab.com/handbook/engineering/security/#security-priority-labels)
labels respectively to indicate priority.

Use the following as a guideline to determine which Availability and Performance
Priority label to use for bugs and feature proposals. Consider the _likelihood_
and _urgency_  of the "scenario" that could result from this issue (not) being
resolved.

- **Urgency:**  _Examples_
 - U1
    - Outage likely within a month.
    - Affects many team members and/or many GitLab.com users
 - U2
    - Outage likely within three months.
    - Affects some team members and/or a few GitLab.com users
 - U3
    - Outage can happen, but not likely in next three months.
    - Affects some team members but no GitLab.com users

- **Impact:** _Examples_
 - I1
    - Outage of >= 25 minutes.
    - Performance improvement (or avoiding degradation) of >= 100 ms expected.
 - I2
    - Outage of 5 - 25 minutes.
    - Performance improvement (or avoiding degradation) of 10-100 ms expected.
 - I3
    - Outage of 0 - 5 minutes.
    - Performance improvement (or avoiding degradation) of <= 10 ms expected.


| **Urgency \ Impact**          | **I1 - High** | **I2 - Medium**  | **I3 - Low**   |
|----------------------------|---------------|------------------|----------------|
| **U1 - High**              | `AP1`         | `AP1`            | `AP2`          |
| **U2 - Medium**            | `AP1`         | `AP2`            | `AP3`          |
| **U3 - Low**               | `AP2`         | `AP3`            | `AP3`          |


## Database Performance

Some general notes about parameters that affect database performance, at a very
crude level.

- From whitebox monitoring,
   - Of time spent on/by Rails controllers, this much is spent in the database: <https://performance.gitlab.net/dashboard/db/rails-controllers?orgId=1&panelId=5&fullscreen> (for a specific Rails controller / page)
   - _Global_ SQL timings: <https://performance.gitlab.net/dashboard/db/transaction-overview?panelId=9&fullscreen&orgId=1&from=now-2d&to=now>
- A single HTTP request will execute a single controller. A controller in turn
will usually only use one available database connection, though it may use 2 if
first a read was performed, followed by a write.
   - pgbouncer allows up to 150 concurrent PostgreSQL connections. If this limit
is reached it will block pgbouncer connections until a PostgreSQL
 connection becomes available.
    - PostgreSQL allows up to 300 connections (connected, whether they're active
    or not doesn't matter). Once this limit is reached new connections will be
    rejected, resulting in an error in the application.
    - When the number of processes > number of cores available on the database
    servers, the CPU constantly switches cores to run the requested processes;
    this contention for cores can lead to degraded performance.
- As long as the database CPU load < 100% (<http://monitor.gitlab.net/dashboard/db/postgres-stats?refresh=5m&orgId=1&from=now%2Fw&to=now&panelId=13&fullscreen>),
then in theory the database can handle more load without adding latency. In
practice database specialists like to keep CPU load below 50%.
    - As an example of how load is determined by underlying application design:
     DB CPU percent used to be lower (20%, prior to 9.2, then up to 50-75% [when
       9.2 RC1 went live](https://gitlab.com/gitlab-org/gitlab-ce/issues/32536),
       then back down to 20% by the time 9.2 was released.
- pgbouncer
   - What it does: pgbouncer maps _N_ incoming connections to _M_ PostreSQL
   connections, with _N_ >= _M_ (_N_ < _M_ would make no sense). For example,
   you can map 1024 incoming connections to 10 PostgreSQL connections. This is mostly influenced by the number of
concurrent queries you want to be able to handle. For example, for GitLab.com
our primary rarely goes above 100 (usually it sits around 20-30), while
secondaries rarely go above 20-30 concurrent queries. The more secondaries you
add, the more you can spread load and thus require fewer connections (at the
  cost of having more servers).
   - Analogy: pgbouncer is a bartender serving drinks to many customers. Instead
   of making the drinks himself she instructs 1 out of 20 “backend” bartenders
   to do so. While one of these bartenders is working on a drink the other 19
   (including the “main” one) are available for new orders. Once a drink is done
   one of the 20 “backend” bartenders gives it to the main bartender, which in
   turn gives it to the customer that requested the drink. In this analogy, the
  _N_ incoming connections are the patrons of the bar, and there are _M_ "backend"
   bartenders.
   - Pgbouncer frontend connections (= incoming ones) are very cheap, and you
   have have lots of these (e.g. thousands). Typically you want _N_ >= _A_ with
   _N_ being the pgbouncer connection limit, and _A_ being the number of
   connections needed for your application.
   - PostgreSQL connections are much more expensive resource wise, and ideally
   you have no more than the number of CPU cores available per server (e.g. 32).
   Depending on your load this may not always be sufficient, e.g. a primary in
   our setup will need to allow 100-150 connections at peak.
   - Pgbouncer can be configured to terminate PostgreSQL connections when idle
   for a certain time period, conserving resources.
