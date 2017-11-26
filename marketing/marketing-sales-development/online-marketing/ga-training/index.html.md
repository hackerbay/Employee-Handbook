---
layout: markdown_page
title: "Online Marketing"
---
This is meant to be a crash course in Google Analytics. It is meant to help you get up and running your basic understanding of Google Analytics so that you can answer some simple and common questions regarding our website traffic.

----

- TOC
{:toc}

----

## Dimensions vs Metrics
Dimensions are the different attributes of your data. For example, the landing page is a dimension that is the first page a person views when they come to the site.

Metrics are the numbers that are being measured, such as number of page views or number of sessions.

Each dimension and metric has a scope, so it’s important to understand the three different scopes:  
1) User-level
2) Session-level
3) Page-level

Due to the scoping, not every dimension can be combined with every metric. In most cases, the dimensions and the metrics should match the scope.

## Understanding Reporting
### Setting a date range

You can use the calendar in the top right to set the active date range. You can also select the `compare to` box to compare metrics from different time periods. This will allow you to see month over month or year over year growth for the desired metrics.

### Annotations

Annotations are used to mark a point in time in Google Analytics. They can be used to mark an important event such as a change to the set-up of Google Analytics, or an event that heavily impacted traffic positively or negatively.

To create an annotation, double-click on a date. The double-click will bring up the annotation field where you can enter details, and select `private` or `public`. Public annotations can be seen by anyone that has access to that view within Google Analytics, and private annotations can only be seen by you.

### Data Tables

Most reports have a data table below the graph. The data tables contain a dimension and associated metrics.

The `Primary Dimension` of the data tables can be changed by selecting a different primary dimension from above the table.

A secondary dimension can also be added by clicking on the `Seconday Dimension` button above the table and selecting the secondary dimension you’d like to add to the table.

## Audience Reports

The audience reports are used to understand characteristics of your users such as location, and browser used, and user behavior over multiple visits such as average session time.

## Acquisition Reports

The acquisition reports help you know how people find the website. These reports will help you to analyze the benefits of the different digital marketing efforts that you are involved in.

### Channels Report

The `All Traffic > Channels` report breaks down all the different channels that are sending traffic to the site. You can click on any of the channels to drill down  and get more granular data about that specific channel. For example, if you click on the `Referral` channel, you will see which sites are referring traffic to your site.

## Behaviors Reports

The behaviors section is about how users use the website. This includes what pages of the site people are looking at as well as how they flow through the site.

### All Pages Report

The `All Pages` report shows the number of times a given page was viewed within the selected period of time. You can change the primary dimension to `Page Title` if it is easier to tell what the page is by looking at the title rather than the URL.

`Avg. Time on Page` and `Bounce Rate` can be used to find underperforming content or content that is very engaging to users and can be used in future marketing efforts.

### Landing Pages and Exit Pages

The `Landing Pages` and `Exit Pages` reports are scoped at the session and tell us how many people are beginning a session at a certain page (landing page) and how many people are ending a session at a certain page (exit page).

These reports can be valuable to see what content is bringing people to the site and what content is causing people to leave the site.

### Events

Events can be set up to track actions that people take on the website, such as clicking links or selecting drop downs. These events can be set up in Google Tag Manager and for the most part won’t require any additional code to be placed on the website.
