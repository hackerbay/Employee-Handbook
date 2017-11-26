---
layout: markdown_page
title: Discontinued Plans
category: GitHost
---

## On this page
{:.no_toc}

- TOC
{:toc}

----

## Discontinued Plans

From time to time, we update pricing on GitHost and we must discontinue older
plans. When this happens we offer to allow existing customers to keep their
current plan and upgrade to a new plan at a discount.

### December 30, 2015

On this date, we increased pricing and introduced new plans. For existing
customers we offered to let them keep their existing plan for up to 2 years.
At any point during that 2 years, the customer can also opt to upgrade to
one of our current plans at a 40% discount.

This grandfather and discount period expires on December 30, 2017.

Instances on the following plans are eligible for the discount:

- ["Developer (Discontinued)" (ID: 1)](https://githost.io/admin/plans/1)
- ["Startup (Discontinued)" (ID: 2)](https://githost.io/admin/plans/2)
- ["Business (Discontinued)" (ID: 3)](https://githost.io/admin/plans/3)
- ["Base (Discontinued)" (ID: 4)](https://githost.io/admin/plans/4)
- ["Developer Plus (Discontinued)" (ID: 7)](https://githost.io/admin/plans/7)

Please note that the plan names may overlap with some other plans that currently
exist, or were more recently discontinued. That is why the plan ID is also
provided above. Cross-check the plan name with the ID in the database to determine
if the user gets the discount.

### Processing a discount upgrade

When customers request an upgrade at the discounted rate, first check if an
existing private discounted plan exists. For example, at the time of this
writing we have a 'Startup (40% Off)' ($48/month) and 'Developer Plus (40% Off)'
($21/month) plans. If the appropriate plan exists, resize the customer's instance
to the plan. The customer cannot do this themselves because the plans are private
and will not show up in the list for them.

If the discounted plan does not exist, create a new private plan. Take the
current price of the plan the customer wishes to upgrade to and multiply by
0.6 to find the discounted price.
