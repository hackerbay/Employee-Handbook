---
layout: markdown_page
title: "Community Writers Program - Terms and Conditions"
twitter_image: '/images/tweets/community-writers-terms-and-conditions.png'
description: "Terms and Conditions applied to the GitLab Community Writers Program"
---

## Community Writers Program - Terms and Conditions
{:.no_toc}
For an overview, please check the [Community Writers Program](../) webpage.

----

## On this page
{:.no_toc}

- TOC
{:toc}

----

### Purposes of the Program

The [Community Writers Program](../) has the purpose of producing high-quality resources to:

- facilitate the use of GitLab as a fully integrated software development platform
- increase the use of GitLab as [Continuous Integration, Delivery, and Development](/2016/08/05/continuous-integration-delivery-and-deployment-with-gitlab/) platform
- ease GitLab's usability for specific use cases
- explore in-depth GitLab's [features](/features/) and capabilities
- promote the use of GitLab Documentation as a source of developer-related resources
- facilitate the search through technical content for GitLab users (in the documentation website)

### Publishing Technical Articles

[Technical Articles](https://docs.gitlab.com/ce/development/writing_documentation.html#technical-articles)
live in the [GitLab Documentation](https://docs.gitlab.com) website.
To guarantee that we maintain high quality and high accuracy, every piece of content
is submitted to review and approval from the [Community Writers Lead](#program-manager),
or, in their absence, from one of the technical writers at GitLab.

### Requirements

- Writers should have **excellent written skills** and have **previous experience**
in writing technical content, which needs to be clear, correct, concise,
trustful, well structured, and easy to follow along.
- Writers should have **excellent written English skills**.
- Writers should be **experienced in writing in markdown** and being able to structure
their files without further assistance.
- Writers should be active users of **Git and GitLab**, and must have a user
account on GitLab.com.
- Writers should be fully capable of creating their own content and presenting
it **ready to publish**. We will not consider content that needs extensive reviews to get ready.
- Writers should **integrally domain the process they're willing to write about**.
We will not help writers with their procedure; we expect you to fully
domain it before willing to join this Program.
- Writers should **read all the guidelines** and **respect them entirely**. We will not
consider for reviews articles that don't respect them.
- Writers should **accept the review** and avoid confronting the reviewer endlessly;
do it only when strictly necessary. Reviewers are there to help to refine the content,
and to ensure it has the quality standards required by GitLab.
- Content must be **original, comprehensible, technical, and unprecedented**.

### Steps to Getting Published

The following stages are required to get your article published by GitLab.

#### 1. Topic

- Writers choose one of the existing issues labeled "[up-for-grabs](https://gitlab.com/gitlab-com/community-writers/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=up-for-grabs)", or create a new one in the
[Community Writers issue tracker](https://gitlab.com/gitlab-com/community-writers/issues).
**Pick only one issue at a time**.

#### 2. Pre-assessment

- Writers propose the [outlines](../../#3rd-plan) of their articles in the issue thread,
together with a writing sample, and the introduction of their article.
  - **Writing sample**: any technical material previously written by the author,
  preferably on the same or similar topic.
  - **Introduction**: write the introduction of your article (100-150 words). We'll evaluate your approach, writing style, organization, clearness, and conciseness.
  - **Outlines**: your article's topic structure. We'll evaluate how you structure your subject in sub-topics, the depth of your content and the logic of your construction. Your outlines should respond: what is required to get started, what problem does your article solve, why is it important, what's the motivation to follow your method.
- Once you've gathered the outlines, introduction and writing sample,
drop us a line in the issue thread to let us know you're willing to tackle it:
    
    ```md
    @marcia I would like to write about this subject and I accept the
    [terms](https://about.gitlab.com/handbook/product/technical-writing/community-writers/terms-and-conditions/)
    of the Community Writers Program.
    ```

- The issue will be labeled "pre-assess".
- The editor evaluates the outlines, the writing sample and the introduction in the issue thread.
- Based on them, the editor might approve or not the author to write.
- If approved, the author will have a green light to write the content and
send us the first draft. In this case, the editor will drop a line in the issue thread:

    ```md
    @user, you got it! Please write your draft in markdown and send
    it in a [new confidential issue](https://gitlab.com/gitlab-com/community-writers/issues/new)
    to this project. We do not open any attachments.
    ```

- If approved, the original issue will be labeled "draft" by the editor.
Both labels "pre-assess" and "up-for-grabs" will be removed.
- If not approved, the label "pre-assess" will be removed.

**Note:** if you just comment in the issue and don't provide us with a writing
sample and the introduction of the article, we will not respond to your comment.
{:.note}

#### 3. Draft

- Writers should write based on the [Writing Method](../../#writing-method) and
[Style Guidelines](https://docs.gitlab.com/ce/development/doc_styleguide.html)
  - **Writing Method**: maintains the same requirements for QA: audience, outline, brainstorm, plan, research, draft, test, improve, and review.
  - **Style Guidelines**: maintains the same structure in the entire documentation: markup, directory structure, links format, etc.
- Writers should send us the first draft (written in **markdown**) through
a new confidential issue to be created by the authors themselves. We will not
open any attachments.
The new issue will be **confidential** for preserving the author's
privacy during the evaluation of the article and the compensation offer,
and for maintaining their content private (unpublished). This issue will be labeled
"confidential issue" and remain confidential.

#### 4. Evaluation

- We will respond to the new confidential issue thread as soon as we can,
accepting or rejecting the proposal according to the [evaluation criteria](#evaluation-criteria).
- The original issue will be labeled "evaluate".
- If we reject the content, we can either give the author one chance to make it
better, or reject it entirely. In this case, the issue will be labeled "up-for-grabs", and the confidential issue will be closed.
- If we accept the content, we will proceed to review, and the original issue
will be labeled "review-in-progress". Both labels "draft" and "evaluate" will be removed.

#### 5. Review

- We will review the content and require the author to make the necessary
changes, improvements, and adjustments.
- We will make the review as much brief and direct as possible.
We expect the author to submit their draft ready to be published.
- Once the review is accomplished by the author, we will provide them with
the compensation offer, according to the [compensation criteria](#compensation-criteria).

#### 6. Merge Request

- If the author accepts the compensation offer, we will require the author to submit a merge request
to [GitLab CE](https://gitlab.com/gitlab-org/gitlab-ce/) or
[GitLab EE](https://gitlab.com/gitlab-org/gitlab-ee/) repositories.
See the [Writing Documentation](https://docs.gitlab.com/ce/development/writing_documentation.html)
section for further instructions.
- On the merge request, the editors will proceed with the final review:
they may ask for the author to make further adjustments, or they can copyedit the article themselves.
- As soon as the review is complete, the issue will be labeled "approved",
and the label "review in progress" will be removed.

#### 7. Get Published and Get Paid

- Once your content has been approved to get published, the merge request will be merged, and the article will be
published on the GitLab Documentation website.
- The original issue will be labeled "published".
- Once your content has been published, we will send you an invoice template to be filled with your personal data and instructions to proceed to receive the compensation previously agreed. GitLab will pay you in American Dollars (USD) from a bank account in the USA, via wired transfer to your bank account.
- Both issues will be closed.

### Compensation Criteria

Once you get approved to submit your content in a merge request, we will inform you
about the compensation range your article is eligible to. If you agree with
compensation offered, you can submit the merge request.

The offer will be based on the **complexity** and/or **knowledge level** of your content:

| Complexity | Knowledge Level | Compensation Range |
| ---------- | --------------- | :----------------: |
| Simple | Beginner | **$50** to **$100** |
| Intermediary | Intermediate | **$100** to **$150** |
| Complex | Advanced | **$150** to **$200** |

The overall evaluation is based on these criteria, but the reviewer will
consider your article as a whole to define the compensation offer.

The amount is expressed in American Dollars (USD).

### Evaluation Criteria

The content will be evaluated based on:

- Readability
- Flow
- Structure
- Grammar
- Complexity
- Accuracy
- Respects the Style Guidelines
- Respects the Writing Method

### Content Ownership

- Once in a merge request, the [ownership](https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/legal/individual_contributor_license_agreement.md) of that content is GitLab's, therefore,
the author **cannot** publish that content somewhere else until it's published by GitLab.
- Once the article gets published by GitLab, the author is welcome to reproduce the content
totally or partially, on their own blog or somewhere else, as long as they provide attribution to GitLab:

    ```
    This article was [originally published](link-to-article) by [GitLab](https://about.gitlab.com).
    ```

**Note:** Once the content is published, GitLab reserves the right to change,
rewrite, update, and remove the content totally, at GitLab's will.
{:.note}

#### Updates

If the content gets out-of-date, we may ask the author to update it.
GitLab reserves the right to update it, rewrite it
(subjected to authorship updates), or remove it entirely.

### Time Frame

Once you're approved to write the draft on the pre-assessment stage, we expect you
to have the content ready to be sent to us up to three working days after our response.

We expect to have your content published up to one month after the beginning of
the process. It can be concluded faster than that, or slower, depending on the actual demand of
work from our editors, and on the quality of your content.

### Ineligibility

You are considered **ineligible** for the Community Writers Program:

- If you're a GitLab Team member.
- If you intent to promote your own product, company, or the company you work for.
In this case, you might be eligible for a [Guest Blog Post](/handbook/marketing/blog/#guest-posts).
- If you don't fulfill the [requirements](#requirements) described above.

### Program Manager

The Community Writers Program is part of the [Technical Writing](../../) Team at GitLab.
[Marcia Ramos](/team/#XMDRamos), the **Community Writers Lead**, manages the program.

Our technical writers are also experienced editors, who will provide authors with feedback,
proofreading, and copyediting.

### Important Notes

- If you want to write about your own product (or the product you represent),
and how it integrates with GitLab, we'll be happy to have you as a
[Guest Writer](/handbook/marketing/blog/#guest-posts). The Community Writers Program
won't apply for these cases.
- You are encouraged to write more than one article. If you succeed on
the first process, we'll invite you to write for us regularly.
The process for writing more than one article is exactly the same for
writing the first one. Please, pick up only one issue at a time.
- GitLab reserves the right to refuse to publish any article at any time of the process.
- GitLab reserves the right to close the issue at any time, and do not proceed with that subject.
- Once you start the process by choosing a topic, you agree with the terms and
conditions established on the present document.
- The terms and conditions presented by this document are subject to
changes without previous notice.

Last update: 2017/08/01
{:.note .text-right}
