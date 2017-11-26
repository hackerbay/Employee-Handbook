---
layout: markdown_page
title: "Technical Writing"
---

### Welcome to the Technical Writing Handbook!
{:.no_toc}

----

## On this page
{:.no_toc}

* Will be replaced with the ToC, excluding the "On this page" header
{:toc}

----

## Technical Writing

> _Technical writing is sometimes defined as simplifying the complex. In a concise and deceptively simple definition, it is a whole range of skills and characteristics that address nearly every field of human endeavor at some level._ ([techwhirl.com](http://techwhirl.com/what-is-technical-writing/))

At GitLab, tech writers are the folks who take care of writing and maintaining technical content clear, concise, consistent, professional, and up-to-date.

[Technical Writers] are part of the Product Team. Their mission is to
help GitLab to:

- have all features well documented
- ensure the information regarding GitLab CE/EE/CI and its particularities are up to date
- write guides, recipes, and blog content
- assist the team with documentation and non-documentation tasks
- review every technical content published in the channels we use

[Documentation] helps the GitLab community to:

- setup and administrate their accounts
- setup and update GitLab instances
- use every tool and feature
- handle integrations, services, and tools

Docs are written technically, methodically,
programmatically, clearly, and practically.

[Blog posts][blog] have the same purpose of assisting the GitLab community,
but with a more flexible and reader-friendly language. Also,
besides the technical content, posts can be informative, tell use-case stories,
customer experience, and present a much more diverse
sort of content, since it's somehow interesting for our audience.

Whenever we write for GitLab, it's necessary to keep in mind that we are writing _on behalf_ of GitLab. We are representing the
company. Therefore, it's important to keep our personal opinions, tendencies, and point of views apart, and try to be clear, direct, concise, and professional above all. This is detailed right below, on the section [Professional Writing Techniques].
Make sure to read this through before writing for GitLab.

Also, our content is written in markdown Kramdown. Make sure to read the [Markdown Style Guide] before adventuring yourself writing for
our website [about.GitLab.com] and our [Blog], which are our "faces to the world".

On the [GitLab Blog Handbook][marketing-blog], you'll find out more about the GitLab
Blog directive, and the [Blog Style Guidelines][blog-guidelines].

## Markdown Style Guide for about.GitLab.com

Check out our [Markdown Style Guide] for the markup used throughout about.GitLab.com, including any markdown page and blog post. You'll
find useful information there, some [Kramdown] magic, and it might save you a lot of typing.

----

## Professional Writing Techniques

When writing professionally, it's important to understand some standards to follow through, for the purpose of achieving high quality work in a optimum time for conclusion.

Technical papers have the characteristic of being less personal and more formal: they're not the right place to express our opinions, nor to give advice. Accuracy matters most.

For classical scientific papers, the rules are much more restrictive and the language is absolutely formal. For blog posts, we need to use a middle term. Be clear, precise, and professional, but be empathetic and "reader-friendly". A discrete and occasional touch of humor is also welcome.

When writing non-technical blog posts, we can be less formal and more personal, depending on the subject we are writing about. In any case, though, we need to be professional. Meaning, we can be friendly and personal, but we need to focus on the point. The method suggested in this document is valid for both technical and non-technical themes, once it's related to the process of writing, not to the content itself.

Before writing on behalf of GitLab, make sure you've read through this [guide][marketing-blog].

### Technical Blog Posts

Are considered [technical][tech-writing-wiki] posts: tutorials, guides, overviews, techniques, methods, processes, and anything else which requires some sort of technical knowledge or standard procedure. For them, follow all the steps described in the [writing method](#method).

### Non-Technical Blog Posts

For non-technical post, we won't need to get into all the [steps](#method) below. Check which category matches best with the subject you'll be working on to know how to proceed.

- **Personal Experience**
   - _Personal content_: user stories, user experience, opinion-based overviews and comparisons, etc.
   - _Inside GitLab_

   Skip the steps: [4th. Research](#th-research) and [7th. Test](#th-test).

- **Information** (If the content is not a tutorial or a guide, but it has informative purposes)
   - _Feature overviews_
   - _Product comparisons_
   - _Case studies_

   The [7th](#th-test) step can be skipped. For the [4th](#th-research) step, provide links to corroborate your information.

- **Quick Announcements**
   - _Release announcements_
   - _Feature highlights_

   All the steps can be skipped, **except**: 1st, 6th, 8th, 9th, and 10th.

- **Other**

   If your chosen subject doesn't match any previous category, read through the method, and try to use your sense to adapt it according to your case. Fell free to ask for help if needed.

### Writing Method

The following method suggests steps to take in order to create high quality written productions. This approach is recommended, but flexible. Feel free to adapt it to your needs.

#### 1st. Subject, Audience, Requirements

The first step to take if defining the subject, the audience, the knowledge level, and the requirements.

- Choose a subject you are very familiar with and comfortable to explain it in deep details.
- Create a title for your article, based on the previous step. A good title is very short, and accurate.
- Choose the audience:
   - Who might have interest on this subject? Which instance of GitLab would be involved? GitLab EE, CE?
   - What is the expertise level necessary to follow your steps? The user needs to be familiar with the subject, or comfortable with, or need to be an expert?
   - What is required o make it work locally for the user? Specify the Operational System, any necessary software, any hardware condition.
- Add this information to a new issue on the [blog posts issue tracker][blog-tracker]
- Mind that you'll need to create a sentence to be included in the beginning of the article with this information. It can be explicit or subjective.
  For example, for a tutorial for Android: _"We assume you know the process of creating an Android App, you already have projects running locally, and you are familiar with the GitLab UI"_. This would tell the reader that he needs to be an intermediate/advanced app developer, he/she needs to have every software necessary to run an Android application installed locally, and he/she has used GitLab before.


#### 2nd. Brainstorm

Think about everything that is possible for the subject you want to follow through. Write down every piece of information, every detail, every cool stuff that can be achieved, schemes, key processes, any knowledge that can be included in a text about your theme. Doesn't matter the order, if it's important or not, if makes absolute sense or not. Free your brain and let it work with no boundaries. Here the creativity and originality matters most.

#### 3rd. Plan

Perfect. Now you have a lot of ideas to organize. On this part you will filter the important things from your brainstorming notes, arrange them in some logic, and cut off what's not necessary. You'll do that by creating the _outlines_ for your article. Organize the headings in titles, subtitles, bullet points, brief descriptions, and include important [(key)words] that popped up into your head and you want to include in your article.

Keep in mind the audience you'd chosen before. Do not complicate things if you are writing for beginners, nor simplify too much if you're targeting advanced personal.

#### 4th. Research

Now that you know what you want to include in your paper, it's time to find reliable sources to support your scheme. You know the process, but you need to include sources for technical information.

For example, let's consider a post about Android Apps. If you say that you need an emulator for previewing your Android app locally, provide a link to the [official Android documentation][android-doc] where it's said that you need an emulator, and also add a link for the [emulator][android-emulator] itself.

Search for the sources you already know you'll need. Copy and paste the links with interesting information to a text document, or bookmark them, however you prefer. Gather the links in a way you can find them easily, to include them while you draft.

Mind that this step will end only when your post is published. You will need to come back to search for sources again and again, until the end.

A _reliable source_ is officially documented information, content described in books, newspaper's articles, scientific papers, etc. <!-- some ideas to make a better sentence here?  -->

#### 5th. Draft

Now that you have a skeleton for your article, and some links to guide you through, you'll start to write, filling the gaps along the structure you'd planned before.

Never make a statement without providing the source for that information, unless it is your own conclusion, and you have the expertise to defend it. This posture will avoid mistrust and lost of credibility. Follow the [Writing Tips](#writing-tips) below.

It's much quicker to write with a previous plan. Go on and write everything you need. Don't try to review every sentence or to think too much before writing down. You'll have time to review afterwards.

#### 6th. Improve

After you finished, read everything again, and see if you're not repeating yourself, or if there is some unnecessary information. Cut off everything nonessential. This will have been your first review.

After your first review, try to do other things to intentionally deviate your attention from the text. Preferably, close the file and open it just in the next day, after some sleep. This will help you to clear your head, then you'll catch mistakes you wouldn't have after several hours working on the same thing.

Now, along your second review, it's time to spot typos and grammar mistakes. Check if the text sounds clear, easy to understand and if it's not boring. Make any necessary adjustments, then start the review over again.

#### 7th. Test

If you wrote a tutorial or any procedure that can be tested, test it. Go over your steps **exactly as you described them**, and check if you succeed following your own steps. Preferably test in as many conditions as possible: using different Operational Systems, distinct configurations, different versions, whatever applies to your case. If you have someone close to you that could contribute testing it for you too, better yet. After testing, go through the steps 4th to 6th again, if necessary.

#### 8th. Submit

When you're happy with your draft, submit it in a [WIP][WIP MR] (Work In Progress) merge request.

#### 9th. Review

Mind that your reviewers will probably ask for changes, make difficult questions, insist in some points. Do not be discouraged by the review. It will only help you to succeed even more, and to enhance the quality of your work.

If you don't agree with the reviewer at some point, just say it. Discuss your matter and defend your point of view, until you both agree with each other.

#### 10th. Publish

After you adjust the post according to the reviewers' requests, it will get published and everybody will be happy for you!

### Writing Tips

There is a simple list below, for things to do and to avoid when writing. It's not a exact science, though. Try to balance between what's best and what's possible, be yourself, and use your sense.

- Be original: do not repeat yourself - nor repeat other posts and documentation
- Be concise: say what you need to say. Not more, nor less
- Be attentive: do not repeat the same word, use [synonyms]
- Be smart: try to predict questions - and answer them along the text
- Be precise: do not make any statement if you don't have a reliable source or the expertise to defend it
- Be clear: everything seems to be logic for whom is writing. Not necessarily for those reading
- Be organized: in tutorials, do not jump over a step presuming the audience knows that. It breaks logic and looses engrossment
- Be consistent: try to adopt patterns to facilitate the comprehension
- Be professional: prefer "it is" over "I think"
- Be inclusive: use "we" rather then "you" or "I"
- Be creative: think _out-of-the-box_ and explore things _out-of-the-blue_

----


<!-- Identifiers, in alphabetical order -->

[about.GitLab.com]: https://about.gitlab.com/
[android-doc]: http://developer.android.com/intl/pt-br/tools/help/emulator.html
[android-emulator]: http://developer.android.com/intl/pt-br/tools/devices/emulator.html
[blog]: https://about.gitlab.com/blog
[blog-guidelines]: /handbook/marketing/blog/#styles-guidelines
[blog-tracker]: https://gitlab.com/gitlab-com/blog-posts/issues
[bundler]: http://bundler.io/
[documentation]: http://docs.gitlab.com/
[git]: https://git-scm.com/
[issue-docs]: https://gitlab.com/gitlab-org/gitlab-ce/issues/
[(key)words]: http://www.wordstream.com/seo-keyword
[Kramdown]: http://kramdown.gettalong.org
[Mac screenshot]: https://support.apple.com/en-us/HT201361
[Markdown Style Guide]: markdown-guide/
[marketing-blog]: /handbook/marketing/blog/
[middleman]: https://middlemanapp.com/basics/install/
[Nimbus Screenshot]: http://nimbus.everhelper.me/screenshot.php
[Professional Writing Techniques]: #professional-writing-techniques
[Screenshot Tool]: https://help.ubuntu.com/lts/ubuntu-help/screen-shot-record.html
[Snipping Tool]: https://support.microsoft.com/en-us/help/13776/windows-use-snipping-tool-to-capture-screenshots
[synonyms]: http://www.thesaurus.com/
[technical aspects]: https://about.gitlab.com/handbook/marketing/product-marketing/content-marketing/#technical-aspects
[technical writers]: /jobs/technical-writer/
[tech-writing-wiki]: https://en.wikipedia.org/wiki/Technical_writing
[tinypng]: https://tinypng.com/
[unsplash]: https://unsplash.com/
[WIP MR]: http://docs.gitlab.com/ce/workflow/wip_merge_requests.html "Work In Progress Merge Request"
[www-gitlab-com]: https://gitlab.com/gitlab-com/www-gitlab-com/
