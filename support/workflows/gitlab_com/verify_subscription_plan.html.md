---
layout: markdown_page
title: Verify a GitLab.com Subscription Plan
category: GitLab.com
---

### On this page
{:.no_toc}

- TOC
{:toc}

----

### Overview
Many customers sign up for GitLab.com Subscription Plans and this guide will
tell you how to verify what a customer has subscribed to.

---

### Workflow

#### Using Support Middleware (Recommended)

1. Go to https://support-mw.gitlab.com/ and sign in with your GitLab Google
   Account

1. Once logged in, run a search for the customer (company or domain name)

   + If you can't find the customer here you can try one of the other methods,
     below

1. If you find the result, click the arrow on the far right of the entry to
   see more

1. On this new page, you can find the plan and whether or not it is active.

#### Using customers.gitlab.com

1. Sign in to [customers.gitlab.com](https://customers.gitlab.com) using the 
   support credentials in 1Password

1. Select **Customers** from the navigation on the left

1. In the **Filter** box, search for the customer using any of the criteria
   you got from the customer (name, company, etc.)

   + If you don't find the customer this way, ask the customer for more 
     information about their account on customers.gitlab.com

1. On the right side of the customer's entry, you will see a lowercase **i**.
   Click on it to see lots of this customer's data.

   + On the new page you can find the Zuora and SalesForce accounts.

1. Click the **Impersonate** tab on the top of the page
1. On this new page you will see the customer's plan and its expiration date.

#### Using SalesForce

1. Sign in to [Salesforce](https://login.salesforce.com/) using the support
   credentials in 1Password

1. At the top of the page, search for the user or company

1. Look under the **Accounts** category for a result.  Click on the **Account
   Name** that matches the company you're looking for.

1. Under **GitLab Subscription Information** look for the Purchased Products.
   You can also find the Next Renewal Date in this section.
