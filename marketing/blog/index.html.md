---
layout: markdown_page
title: "Blog Handbook"
---

### Welcome to the GitLab Blog Handbook!
{:.no_toc}

----

## On this page
{:.no_toc}

- TOC
{:toc}

----

## GitLab Blog
{: #blog}

Our [Blog] is managed by the Marketing Team.

<div class="alert alert-purple center"><h3 class="purple"><i class="fa fa-gitlab" style="color:rgb(252,109,38); font-size:.85em" aria-hidden="true"></i> &nbsp;&nbsp;<strong>EVERYONE CAN CONTRIBUTE</strong>&nbsp;&nbsp; <i class="fa fa-gitlab" style="color:rgb(252,109,38); font-size:.85em" aria-hidden="true"></i></h3></div>

### Blog endboss

[Rebecca Dodd](https://about.gitlab.com/team/#Reberoodle) is the blog endboss.

If the post author does not know who can do a final review or merge their post
they can assign it to Rebecca. A post author must get at least one review from someone in their immediate team and use a spelling and grammar checker before assigning the MR to Rebecca.

### Publishing Processes

#### Blog Editorial Team

- Erica Lindberg ([@erica](https://gitlab.com/erica)), Content Marketing Manager
- Rebecca Dodd ([@rebecca](https://gitlab.com/rebecca)), Content Editor
- Emily von Hoffmann ([@evhoffmann](https://gitlab.com/evhoffmann)), Jr. Content Editor

#### Third-party posts

Blog posts concerning third parties or partners, whether they are to be published on the GitLab blog or externally,
should be proposed to the blog editorial team before agreeing.
1. Create an issue in the [Marketing project](https://gitlab.com/gitlab-com/marketing/issues) and ping @rebecca and @erica. 
2. If technical input is required, we will ask for instructions from the third party, otherwise it is at the discretion of the blog editorial and technical writing teams whether or not to go forward.

#### Team posts

1. Choose a [topic](#blog-content)
1. Define the target audience, knowledge level and system requirements ([example])
1. Create an outline (a few items describing what you want to discuss along the post)
1. Create an issue in the [Marketing project](https://gitlab.com/gitlab-com/marketing/) with the label `Blog` and ping @rebecca so she can factor it into the publishing schedule
1. Write the post according to the [Professional Writing Techniques][writing-tech] and to the [Markdown Guide]
1. Submit your draft as a WIP MR (Work in Progress Merge Request) to the [GitLab website project][gitlabwww]
1. Get [reviewed](#general-reviews) by your team, and address their feedback
1. Get feedback and review from the [editorial team](#blog-editorial-team) and assign to @rebecca to merge
1. Ask @evhoffmann to promote on social media (Twitter/Facebook)

See the [checklist](#check-list-before-merging) before merging.

**Important:** never write your draft on pre-styled text editors like Google Docs or Microsoft Word. They don't use the same
character encoding as markdown does (UTF-8), and it may cause issues when rendering markdown into HTML. Please use one of
the [recommended code editors][code-editors].
{: #sample .alert .alert-warning}

#### Publishing process for Community Writers

The [Community Writers Program](/handbook/product/technical-writing/community-writers/) has changed.
Please check the new [Terms and Conditions](/handbook/product/technical-writing/community-writers/terms-and-conditions/).

### Objectives &amp; Purposes

- Use the [blog](/blog) to encourage potential users to try GitLab
- Motivate our community to explore GitLab features
- Be empathetic for and useful to our community
- Communicate the benefits of GitLab's unique innovations and tools (e.g., CI)
- Bring in voices from all throughout the company, as well as
from GitLab users and our customers. As always, **everyone can contribute**!

### What content should go on the blog?

The blog is:

- Another marketing channel like Twitter/Facebook/YouTube.
- For longer form news on what we have done or are doing.
- For ephemeral content, think of it as a longer tweet.
- Not the permanent place for tutorials, they should live in the the docs and be
  shared on the blog in the form of a "longer tweet"

The documentation is different to the blog in that it is:

- A reference on everything about our product.
- For feature coverage, API, University (written and video tutorials).
- For persistent content.

### Anatomy of a Blog Post

Later sections of this handbook contain granular examples of different types of posts and how to write them, but a few broad things should be true of all posts, no matter the writer or the topic.

#### Big Picture
- Adopt a personal, conversational tone. For example, feel free to pose rhetorical questions and explain the answers as though you are speaking with a friend.
- Most blog posts are in their most potent form when kept to 500-750 words or fewer.
- You should be able to articulate the purpose/central question of your post in 2-3 sentences or less before even [pitching the topic](https://gitlab.com/gitlab-com/blog-posts/issues). Think of this as your post's "right to exist," because your post will also contain the answer (i.e., the conclusion) to the question it raises. If you can't clearly state the central problem and solution of your post, you need to brainstorm a little more before beginning to write.

#### Introduction
- Establish your central question, problem, or argument within the first sentence or two.
- Briefly bring up the answer to your question in the introduction, because this informs readers of your path, and will help you stay focused.
- Every sentence following the introduction should move you closer to the resolution of your central question. If you are unsure about a sentence, ask yourself, "What fact or point am I trying to establish here, and does this sentence succeed in doing so?" Try to make every word pull its own weight.

#### Body
- Map out the points you need to establish in order for your conclusion to make sense to the reader. You can begin by supplying the details of Who, What, Why, When, Where, and How.
- Ask yourself, "Do I as an [engineer/marketer/team member/executive] know things that are crucial to my reasoning that the reader may not know?" Include a brief explanation of these.

#### Conclusion
- Briefly restate your key question and its answer, adding or reiterating any details and analysis.

### Post Formats

We aim to publish content multiple times a week, with a reliable publishing schedule. The user will most likely have a
pleasant experience if we combine multiple posts formats, trying never to be too much repetitive. Repetition is boring.
<!-- According to our [Content Marketing Strategy][WE'D NEED A LINK], --> We'll alternate between the following formats:

- Short form articles
- Long form articles
- Release announcements
- Feature highlights
- Inside GitLab

## Blog Content

Try to think about what our community might be interested in reading before picking up a subject to work on; you should always begin by identifying your target audience for the post. Here are some example topics & categories:

### Product-specific topics

- Feature highlights bring attention to specific features at GitLab
- Inside GitLab Workflow
- Key features overviews
- New feature releases

### User Stories

- Contributor stories "why I contribute to GitLab"
- Use case stories "how we use GitLab"
- Boss stories "how GitLab enabled innersourcing"
- Inception stories "how GitLab uses GitLab"
- Adoption stories "how we switched from SVN to GitLab"
- Customer stories "why we chose GitLab"

Do you have a better idea? Don't hesitate, [create an issue][blog-tracker] with your proposal and we'll be glad to look into it.

## Technical Aspects

**All** blog posts should always have a real **author name**. When applicable, add a section "Acknowledgments" to the end of the post to thank contributors.

### Types of Blog Posts

{::options parse_block_html="true" /}

<div class="panel panel-gitlab-orange">
#### <i class="fa fa-globe fa-fw" style="color:rgb(252,109,38); font-size:.85em" aria-hidden="true"></i> Release Posts
{: .panel-heading #release-posts}
<div class="panel-body">

Find out more about them on the [release posts handbook](release-posts/)!

Examples: [release] posts, [security release] posts.
</div>
</div>

<div class="panel panel-gitlab-purple">
#### <i class="fa fa-gitlab fa-fw" style="color:rgb(252,109,38); font-size:.85em" aria-hidden="true"></i> Team Members' Posts
{: .panel-heading #team-members-posts}
<div class="panel-body">
Whenever we have something interesting to talk about, we encourage our own team
members to write their stories. And there are a lot of awesome ones! Even if you are not a writer, you are very welcome to write, and our reviewers will be happy to help you with the language, the technical aspects, the markup, the concepts and whatever else you might need.

If you are part of the [GitLab Team](/team/), please contribute! The review process is simple,
please take a look at the [General Publishing Process] below.
</div>
</div>

<div class="panel panel-warning">
#### <i class="fa fa-rocket fa-fw" style="color:rgb(252,109,38); font-size:.85em" aria-hidden="true"></i> Guest Posts
{: .panel-heading #guest-posts}
<div class="panel-body">
These posts are specific for community members that want to write about their own tools, features, and software integrations with GitLab. They can be written by the owners, executives or any team members of those companies, and will be reviewed by the GitLab Blog Editors..

For instance, we've had the post on [Integrating GitLab with Microsoft Azure][azure-post]. It was written by one of Microsoft's employees, then reviewed and polished by our own Technical Writers. A similar process occurred to publish the post on [Continuous Delivery with GitLab and Convox][convox-post].

**Note:** we do not offer compensation for Guest Posts.
{:.note}
</div>
</div>

### GitLab Community Writers Program
{: #community-writers}

Read through the new [terms and conditions](handbook/product/technical-writing/community-writers/terms-and-conditions/) for the [Community Writers Program](/handbook/product/technical-writing/community-writers/), [announced on April 2017](/2017/04/11/announcing-the-new-community-writers-program/).

### Styles

Check out our [styles guidelines].

### Forked project

Before you write, make sure you forked [`www-gitlab-com`], cloned to your computer, and were able to preview it locally by running `bundle exec middleman`.
Before making any change, create a new branch `git checkout -b branchname` cloned from `master`.

### Check list before merging

Reviewer - check these before you publish:

- Check if the post follows the [Blog Style Guide](#styles-guidelines)
- Check all links - make sure none is broken
- Check the file extension `.html.md`
- Check the date on the file name
- Check the date in the post
- Check the image(s) is(are) crunched down.
- Check the blog appears good locally
- When you have double checked, you can assign to @rebecca to review and merge

It takes about 7-10 mins for the blog post to appear as published after merged. As soon as it's live, check the
post for broken links using this tool (or similar): <http://www.deadlinkchecker.com/>. Fix anything _before_ sharing
in any communication channel or social media network.

## Get inspired

- The content doesn't have to be about GitLab, it can also be other content aimed at developers, Hacker News or team leads
- You need to have high quality and high volume, great times are in the [Priceonomics content marketing handbook]
- For the Hacker News guidelines please see the [Hacker News section of the social media guidelines](/handbook/marketing/social-media-guidelines/#hacker-news).
- What worked for Apigee was the 'collaboration in the 21st century' theme
- Explore a reading club such as [a NoSQL summer]
- Milk [GitLab Flow] for more blog posts and videos

----

## Blog Style Guidelines
{: #styles-guidelines}

This style guide is specifically for blog posts on [about.GitLab.com/blog][blog].

### File

The blog posts are located in the project [www-gitlab-com], under `/source/posts/`.

The file name must have this structure: `yyyy-mm-dd-title-of-the-post.html.md`. The date can be
changed just before publishing, so don't worry if it is accurate or not. Future dates are accepted,
in case you have estimated the publishing date, which is defined by the Marketing Team.

In all file names, prefer using dashes `-` than underscores `_`. Do not leave blank spaces in file names, ever.

### Markdown

All posts are written in markdown Kramdown. Please read through the [Markdown Style Guide] for reference.

### Frontmatter

The post **frontmatter** is the first part of any post. It is standard and cannot be changed, so please make
sure to provide the correct information, and do not add nor remove anything from the default template:

```yaml
---
title: "This is the post title"
author: Firstname Lastname
author_gitlab: GitLab.com username # included in February, 2017
author_twitter: Twitter username
categories: technical overview
image_title: '/images/blogimages/post-cover-image.jpg'
description: "Short description for the blog post" # included in August, 2016
---
```

<i class="fa fa-exclamation-triangle" aria-hidden="true"></i> New frontmatter! Social Media information: `twitter_image`, `description`, CTA buttons, `author_gitlab`, and `guest`!
{: .alert .alert-warning .ambar}

```yaml
---
title: "This is the post title"
author: Firstname Lastname
author_gitlab: GitLab.com username
author_twitter: Twitter username
categories: technical overview
image_title: '/images/blogimages/post-cover-image.jpg'
description: "Short description for the blog post"
twitter_image: '/images/tweets/post-screenshot-image.png' # optional
cta_button_text: 'Watch the <strong>XXX release webcast</strong> live!' # optional
cta_button_link: 'https://page.gitlab.com/xxx.html' # optional
guest: true # required when the author is not a GitLab Team Member
ee_cta: false # required only if you do not want to display the EE-trial banner
keywords: [ keyword1, keyword2 ] # optional
twitter_text: "Text to tweet" # optional
---
```

The following sections describe each entry of the frontmatter.

#### Title

Make sure the post title represents very well the subject, and make it as short as possible.
Do the same for headings.

#### Author Name

Use the author's full name. If the name has special chars, type it within
double quotes `"Full Name"`.

#### GitLab.com Handle

Add the author's GitLab.com handle (username only, without "@"). If your username is `johndoe`,
accessible under `https://gitlab.com/johndoe`, this field should be filled as follows:

```yaml
author_gitlab: johndoe
```

This field is required.

Introduced in January, 2017.
{:.note}


#### Twitter Handle

Add the author's Twitter handle (username only, without "@"). If your username is `johndoe`,
accessible under `https://twitter.com/johndoe`, this field should be filled as follows:

```yaml
author_twitter: johndoe
```

Don't worry if you don't have an account on Twitter. Leave the field `author_twitter` blank.

#### Twitter Text
Add a text to tweet in `twitter_text`. If no text is provided it will use post's title.
```yaml
twitter_text: "We just released a new feature!"
```

#### Categories

Use only **one** of the following categories per post.
**Do not** capitalize nor pluralize them, nor change any letter,
otherwise you'll create another category, which is somenthing we don't want to do unpurposely.

- concepts _(use it when your post in on continuous integration, innersource, open source, version control, SaaS, etc)_
- customer stories
- events
- Functional Group Updates _(for [FGU posts](handbook/people-operations/functional-group-updates/) only)_
- git
- GitLab _(all GitLab products/features: Geo, GDK, Pages, LDPA, Hooks, etc.)_
- GitLab CI
- GitLab CE _(use it when highlighting CE features, advantages, etc.)_
- GitLab EE _(EE-only features)_
- GitLab workflow _(issues, merge requests, confidential issues, milestones, todos, etc.)_
- inside GitLab _(remote-first, remote work, team interview, work experience, etc.)_
- integration _(GitLab + something else)_
- press
- release
- security release _(when the main objective is GitLab security)_
- technical overview
- tutorial

We'll improve it, but by now you can find posts under the same category by navigating to
`https://about.gitlab.com/blog/categories/category-name/`. Dashes will be automatically added
to multi-word categories and all of them will be lowercased in the URL. For example, the
category "GitLab CE" will be available under `https://about.gitlab.com/blog/categories/gitlab-ce/`.

If you think we are missing an important category, please let us know by adding a comment
to this issue: <https://gitlab.com/gitlab-com/www-gitlab-com/issues/721>.

#### Cover Image
{: #cover-image-frontmatter}

Do not leave the post without a cover image (`image_title`), unless you have a strong reason to do so.
Read more about it [below](#cover-image).

#### Description

The [`description`](https://moz.com/learn/seo/meta-description) meta tag [is important][description-tag]
for SEO, also is part of [Facebook Sharing][og] and [Twitter Cards]. We set it up in the
[post frontmatter](#frontmatter), as a small summary of what the post is about.

It's a way of making the post title shorter, then add complementary information in the description.
It's not meant to repeat the post title, use your creativity to describe what's in the post.
Try to use about 70 to 100 chars in one sentence.

It is mandatory for all the new posts, and it [has been included][MR-description] in the default post
frontmatter generated by [the command `rake new_post`](#create-a-new-post).

Use this syntax (double quotes included):

```yaml
description: "This is an example description for a blog post."
```

Check the [Social Marketing Handbook] for more information.

#### Keywords
The kewwords are used both as a meta tag [is important][description-tag]
for SEO and as hashtags for the twitter sharable section.

```yaml
keywords: [ keyword1, keyword2]
```

#### Social Media Sharing Image
{: #social-media-info}

It's the image which will be displayed on social media feeds.
It's defined in the post `frontmatter`.

```yaml
twitter_image: '/images/tweets/image-name.png'
```


Whenever you want to display exactly the cover image in social media feeds, don't add a `twitter_image` to the frontmatter. The blog cover image you used will render just as-is in your social timeline via the card automatically produced on Twitter & Facebook. If you want to preview what your card will look like, or verify that the link you're sharing has cards enabled, use Twitter's [card validator tool](https://cards-dev.twitter.com/validator). This is the approach we use for blog posts with titles longer than one line when viewed on our [blog homepage](https://about.gitlab.com/blog/). The Release post may be an exception. 

Whenever the blog post title fits on one line when viewed on the blog homepage, you may choose to add a twitter image. The standard procedure for this image is:

- Locally preview the blog landing page including your post at <http://localhost:4567/blog> and zoom in
- Use a screen capture tool (as `cmd+shift+4` on your Mac and [Snipping tool] on your PC) to take a screenshot of the background image + title overlay of your post*
- Compress the image with [TinyPNG.com][tinypng]
- Rename it after the post's filename, so that it will have exactly the same name as your
post does, omitting the post date (if your post is called `2016-05-20-hello-world.html.md`, the `twitter_image` should be named `hello-world.png`)
- Add it to the project's directory at `/source/images/tweets/`

*This is the portion to take the screenshot from (purple line):

![twitter_image for the blog](/images/handbook/marketing/social-sharing-img.png){:.shadow}

You can also use another image for social sharing.

For further information, read the Social Media Sharing section at the [Social Marketing Handbook].

#### Call To Action (CTA)
{: #cta}

There are two new possible entries in the frontmatter:

```yaml
cta_button_text: 'Watch the <strong>XXX release webcast</strong> live!'
cta_button_link: 'https://page.gitlab.com/xxx.html'
```

The first entry is text, referring to the link added to the second one. Therefore,
always use them together.

The examples above link to a release webcast, but you can add any pair of text
and link to this CTA. Use it wisely.

**Do not** include any [UTM parameters] to the link. Always wrap their values with quotes.
{:.alert .alert-warning}

The final result is a red button over the cover image of the post.

![Hero CTA preview](/images/handbook/marketing/hero-cta.png){:.shadow}

The CTA entry is optional; if you don't need to add any CTA to the hero, just omit both entries, leaving the frontmatter without them.

This option was introduced in January/2017.
{:.note}

#### EE-Trial Banner

![ee-trial banner](/images/ee-trial-banner.png)

To not display the EE-trial banner on the blog post, set `ee_cta` to `false` in the frontmatter:

```yaml
ee_cta: false
```

It is set to true by default, so there's no need to add `ee_cta: true` to the frontmatter.

Use it wisely; the EE-trial banner is important for Lead Gen.

#### Guest

The variable `guest` indicates whether the author is a guest (anyone who's not a GitLab Team member). It should be only included in the frontmatter when that's the case. Technically, it's a conditional variable (`true` or `false`) to link the author's name their profile in the [Team](/team/) page.

For Guest Posts, Partner Posts, and Crossposts, it must be present:

```yaml
guest: true
```

For Team Posts, please do not add it at all (instead of setting it to `false`).

Introduced in February, 2017.
{:.note}

#### Comments

Comments are present in all posts by default. Set it to false only if you have a strong reason to
do so (`comments: false`). They are our best source of feedback on posts.

#### Date

The variable `date: yyyy-mm-aa hh:mm:ss` is not necessary in the frontmatter, unless you want to set an specific time. If you do, just make sure that the date in the file name matches with the date in the frontmatter, otherwise the build will fail. It's going to be necessary when publishing more than one post per day. The latest will stay on the top of the [blog landing page][blog].

### Create a new post

You can create a new post however you prefer: adding a new file to `/source/posts/`, duplicating an existing post, or using the command line, which is the safest way to do so. Just is type into your terminal (opened in your local project directory):

```sh
rake new_post
```

Hit **enter** or **return**, then you'll be prompted to enter the post title. Type in the title exactly as you
want it, for example "Hello World - I'm a new post" and rake will take care of the file name for you.
Then you just open the file, fill in with your name, Twitter handle, and the post category, then you'll be
good to start writing.

### Writing Style

At GitLab, we use [American English](/handbook/communication/#american-english) as the standard written language.

GitLab content primarily follows [AP Style],
which is searchable online. However we use [sentence case](https://www.thoughtco.com/sentence-case-titles-1691944) for all titles and subheadings, as it is easier to apply consistently and helps readers to scan titles more easily.

Any questions that cannot be answered
by the AP Stylebook may be resolved by referring to the
[Chicago Manual of Style]. To learn about GitLab's advanced
formatting system, check out our [Markdown Guide].

### Body structure

Just below the frontmatter, start writing your post, including the sections as follows:

- Introduction. State the problem, audience, and purpose of the article.
- Add the `<!-- more -->` separator. This is going to separate the visible part on the landing
page <https://about.GitLab.com/blog/> from the rest of the article body.
- Software and hardware requirements - explain what the reader needs before following your steps.
- Concepts - state and explain the concepts needed to follow through your post.
- Article body - develop the subject of your post. Mind that we [wrap text].
- Section `## Conclusion` - summarize the article.
- Section `## About guest author` - when the author is not a GitLab Team member, add this section telling
in 3 or 4 sentences who is the guest author, and what is her/his background on the post's subject.
It must be written by the author her/himself.
- Section `## Acknowledgments` - whenever there are more people deeply involved in having the post ready to go,
you can add this section to show your gratitude to your colleagues.

If the article is part of a series, make sure to link back among all articles
in the series to each one after they get published.

### References

As explained on the [Professional Writing Techniques][writing-tech], always provide source for your statements.

### Illustration

Illustrate your examples, with code blocks or screenshots. Be consistent along your examples. E.g., if you are using a generic URL
to exemplify your steps `domain.com`, be consistent and keep it `domain.com`, throughout the post.

**Important security point:** Do not expose your personal details by using your real tokens or
security credentials.
Use placeholders such as `[project's CI token]` stub instead. Or blur them if displayed on screenshots.

### Images

#### Creating images
{: .no_toc}

- Static images should be used to illustrate concepts, provide diagrams, elements of the UI or orient the reader.
- Images should not be used to render commands or configuration which would prevent
someone being able to copy and paste.
- Animated GIFs can be used sparingly where you need to show a process or some event
happening over the course of time or several actions, though they should not replace text descriptions or instructions.
- Use screenshots to identify and localize specific parts of the screeen. There are great tools
for doing so. For example, [Nimbus Screenshot]  (browser extention), [Mac screenshot],
[Snipping Tool] for Windows, and [Screenshot Tool] for Ubuntu.

#### Preparing images
{: .no_toc}

For the blog, images should be cropped in a 1.7 width/height pixel *proportion* (ideally 1275px x 750px)
so the image doesn't get clipped when displayed as a lead image in the blog list.
This includes the cover image.
Compress the image, for example using [TinyPNG.com][tinypng] or any other image editor. All images should be at least smaller than 1MB. JPEGs tend to be smaller than PNGs so use JPEGs when possible.
To preserve the harmony along the post, try to keep all the images with the same width
(e.g., the ones used in [this post][width-post]).

The only images accepted for about.GitLab.com are public domain images and
screenshots. Whenever you choose an image which is not a screenshot, add a
link to the original image to the merge request description and as an HTML comment:

```html
<!-- image: image-url -->
```

Do the same for [cover images](#cover-image), adding a link to the original image
to the end of the post as a comment and to the MR description:

```html
<!-- cover image: image-url -->
```

#### Image shadow

It is important to highlight the image so that it can easily be recognized as image, and not as part of the text.
The way we use is adding a [CSS custom class][css-shadow] called `shadow`. You do that by adding the markup `{: .shadow}`
right besides the image markup:

```md
![Image Alternative Text](/path/to/image.png){: .shadow}
```

#### Where to place images
{: .no_toc}

Images used to illustrate articles should be placed in the `/source/images/blogimages/` directory.
Unless they are 'free to use' lead images from [Unsplash][unsplash], which should be placed in the
`/source/images/unsplash` directory.

#### Naming images
{: .no_toc}

If you are using a set of images, create a **new directory** under `/source/images/blogimages/`, name it according to
your post's title and add all the images there. For example, if your post has a file name
`2015-03-20-my-awesome-post.html.md`, your new folder should be named `/my-awesome-post/`.

If you use just a couple images, you can add them directly to `/source/images/blogimages/`, but make sure they begin with the same
name as you post's. This way it's easy to anyone know which image is related to each post. Name the files according to the previous example.
So, following the same logic, your cover image would be named `my-awesome-post-cover.png`, accessed under
`/source/images/blogimages/my-awesome-post-cover.png`.

#### Cover image
{: .no_toc}

Choose a cover image for your post. Try any public domain resource that
reflects somehow your post's subject. In the absence of an image, use one of these:

- GitLab Default: `'/images/default-blog-image.png'` (purple background and the Tanuki logo)
- Blog Default: `'/images/blogimages/gitlab-blog-cover.png'` (purple background, the Tanuki logo and "GitLab")

Please add a reference to the cover image source, owner, and licence at the end of
the blog post, even if it doesn't require attribution:

```md
----

Cover image: ["Image title"](link-to-original-image) by [owner name and surname](link), licensed
under [CC X](link-to-licence).
{: .note}
```

If the image does not have a title, default to the following format:

```md
----

[Cover image](link-to-original-image) by [owner name and surname](link), licensed
under [CC X](link-to-licence).
{: .note}
```

The cover image has the following proportions:

- On the [blog landing page][blog]: 1275px x 750px w/h = 1.7
- On blog post page (widescreen): 1920px x 550px w/h = 3.5

Try to have them harmonically aligned with the title,
which overlays the background image in both cases.

To crop the image, use the size of 1275x750 px. If you want
to align the background image with the title overlay, use the widescreen
proportion.

#### Creating GIFs
{: .no_toc}

Animated GIFs are very useful to illustrate short dynamic processes, which might be easier to understand with this kind of resource.
There are a few ways to create animated GIFs, one of them is using [Giphy Capture], a light-weight app for Mac.

Avoid GIFs with a huge file size, they will be difficult to load for users with bad internet connection. In those cases,
you can either cut the GIFs in smaller pieces, or record a video, or use a sequential image (e.g., the ones used in [this post][gifs-post]).

Read more on [Making Gifs] in the Product Handbook.

### GitLab Specific Terms

- **GitLab** is always spelled with capital "G" and "L".
- If you're writing about the CI feature, it's not a separate product.
For example don't refer to "Gitlab CI's runner" please refer to "GitLab Runner", capital "R".
- **GitLab, Inc.** is the company. **GitLab** is the SaaS, which refers to **GitLab.com**, **GitLab EE** and **GitLab CE**.
- We refer to **GitLab team members** instead of staff.
- Make sure the CI configuration file is spelled ``` `.gitlab-ci.yml` ```, with the leading period and backticks.
- When we refer to specific configuration sections or pages in GitLab they should be in **bold**.
- Refer to this website as **about.GitLab.com**, with capital "G" and "L", as always. **GitLab.com** is not the website, is the SaaS.

---

## Quick Guide for Release Posts

Update (April, 2017): check the [release posts handbook](release-posts/).

<!-- Identifiers, in alphabetical order -->

<!-- INTRO -->

[dev-rel]: /handbook/marketing/developer-relations/
[prod]: /handbook/marketing/product-marketing/

<!-- GITLAB BLOG DIRECTIVES -->

[a NoSQL summer]: //nosqlsummer.org/
[about Swift]: https://realm.io/news/top-5-swift-videos-of-2014/
[backlog]: https://dev.gitlab.org/gitlab/blog-posts/issues?milestone_id=&scope=all&sort=created_desc&state=opened&utf8=%E2%9C%93&author_id=&assignee_id=0&milestone_title=&label_name=
[Blog post style guide]: https://gitlab.com/gitlab-com/blog-posts/blob/master/STYLEGUIDE.md
[blog-tracker]: https://gitlab.com/gitlab-com/blog-posts/issues
[Community Writers]: /handbook/product/technical-writing/community-writers/
[example]: /handbook/product/technical-writing/#st-subject-audience-requirements
[GitLab Flow]: //doc.gitlab.com/ee/workflow/gitlab_flow.html
[GitLab Workflow]: https://www.youtube.com/watch?v=enMumwvLAug "Introduction to GitLab Workflow"
[GitLab]: /
[gitlabwww]: https://gitlab.com/gitlab-com/www-gitlab-com
[Kramdown]: //kramdown.gettalong.org/
[post-convox]: https://about.gitlab.com/2016/06/09/continuous-delivery-with-gitlab-and-convox/#about-guest-author-noah-zoschke
[post-iOS]: https://about.gitlab.com/2016/03/10/setting-up-gitlab-ci-for-ios-projects/#about-guest-author-angelo-stavrow
[Priceonomics content marketing handbook]: http://priceonomics.com/the-content-marketing-handbook/
[public domain]: https://en.wikipedia.org/wiki/Public_domain
[Realm.io]: //realm.io
[styles guidelines]: #styles-guidelines
[tech-writing-audience]: /handbook/product/technical-writing/#st-subject-audience-requirements
[tinypng]: //tinypng.com
[WIP MR]: http://docs.gitlab.com/ce/workflow/wip_merge_requests.html "Work In Progress Merge Request"
[writing-tech]: /handbook/product/technical-writing/#professional-writing-techniques
[`www-gitlab-com`]: https://gitlab.com/gitlab-com/www-gitlab-com/

<!-- BLOG STYLE GUIDELINES -->

[(key)words]: http://www.wordstream.com/seo-keyword
[@Lindberg]: https://gitlab.com/u/Lindberg
[@marcia]: https://gitlab.com/u/marcia
[about.GitLab.com]: https://about.gitlab.com/
[android-doc]: http://developer.android.com/intl/pt-br/tools/help/emulator.html
[android-emulator]: http://developer.android.com/intl/pt-br/tools/devices/emulator.html
[AP Style]: http://www.apstylebook.com/online/?do=chapter
[Axil]: https://gitlab.com/u/axil
[azure-post]: /2016/07/13/how-to-setup-a-gitlab-instance-on-microsoft-azure/
[Blog Editorial Team]: #blog-editorial-team
[Blog Editorial Team]: #blog-editorial-team
[blog-tracker]: https://gitlab.com/gitlab-com/blog-posts/issues
[blog]: /blog/
[bundler]: http://bundler.io/
[Chicago Manual of Style]: http://www.chicagomanualofstyle.org/home.html
[code-editors]: /handbook/product/technical-writing/markdown-guide/#markdown-editors
[convox-post]: /2016/06/09/continuous-delivery-with-gitlab-and-convox/
[cross-1]: /2016/08/04/moving-to-gitlab-yes-its-worth-it/
[cross-2]: /2016/08/11/building-an-elixir-release-into-docker-image-using-gitlab-ci-part-1/
[cross-3]: /2016/08/19/applying-gitlab-labels-automatically/
[css-shadow]: /handbook/product/technical-writing/markdown-guide/#special-classes
[description-tag]: http://www.wordstream.com/meta-tags
[Digital Ocean]: /2016/04/19/gitlab-partners-with-digitalocean-to-make-continuous-integration-faster-safer-and-more-affordable/
[documentation]: http://docs.gitlab.com/
[Emily Kyle]: https://twitter.com/emilylucie
[General Publishing Process]: #general-publications
[General Reviews]: #general-reviews
[gifs-post]: /2016/08/19/posting-to-your-gitlab-pages-blog-from-ios/
[Giphy Capture]: https://itunes.apple.com/us/app/giphy-capture.-the-gif-maker/id668208984?mt=12
[git]: https://git-scm.com/
[GitLab CE]: https://gitlab.com/gitlab-org/gitlab-ce/
[GitLab EE]: https://gitlab.com/gitlab-org/gitlab-ee/
[issue-close]: https://docs.gitlab.com/ce/user/project/issues/automatic_issue_closing.html
[issue-docs]: https://gitlab.com/gitlab-org/gitlab-ce/issues/
[Koding]: /2016/07/26/koding-and-gitlab-integrated/
[Mac screenshot]: https://support.apple.com/en-us/HT201361
[Making Gifs]: /handbook/product/making-gifs
[Markdown Guide]: /handbook/product/technical-writing/markdown-guide/
[Markdown Style Guide]: /handbook/product/technical-writing/markdown-guide/
[marketing-blog]: #blog
[Mattermost]: /2015/08/18/gitlab-loves-mattermost/
[middleman]: https://middlemanapp.com/basics/install/
[MR-description]: https://gitlab.com/gitlab-com/www-gitlab-com/merge_requests/2740/
[Nimbus Screenshot]: http://nimbus.everhelper.me/screenshot.php
[OG]: https://developers.facebook.com/docs/sharing/webmasters#markup
[outlines]: /handbook/product/technical-writing/#3rd-plan
[Pivotal Cloud Foundry]: /2015/11/03/pivotal-cloud-foundry-tile-for-gitlab-ee/
[post-iOS-CI]: /2016/03/10/setting-up-gitlab-ci-for-ios-projects/
[post-lets-encrypt]: /2016/04/11/tutorial-securing-your-gitlab-pages-with-tls-and-letsencrypt/
[post-pages]: /2016/04/07/gitlab-pages-setup/
[release]: /blog/categories/release/
[Screenshot Tool]: https://help.ubuntu.com/lts/ubuntu-help/screen-shot-record.html
[Sean]: https://gitlab.com/u/SeanPackham
[security release]: /blog/categories/security-release/
[Snipping Tool]: https://support.microsoft.com/en-us/help/13776/windows-use-snipping-tool-to-capture-screenshots
[Snipping tool]: https://support.microsoft.com/en-us/help/13776/windows-use-snipping-tool-to-capture-screenshots
[Social Marketing Handbook]: ../social-marketing/
[synonyms]: http://www.thesaurus.com/
[tech-writing-wiki]: https://en.wikipedia.org/wiki/Technical_writing
[technical aspects]: #technical-aspects
[technical writers]: /jobs/technical-writer/
[tinypng]: https://tinypng.com/
[twitter card validator]: https://cards-dev.twitter.com/validator
[twitter cards]: https://dev.twitter.com/cards/overview
[unsplash]: https://unsplash.com/
[UTM parameters]: http://www.annielytics.com/blog/analytics/how-to-trash-your-google-analytics-account-with-campaign-tagging/
[width-post]: /2016/08/05/feature-highlight-set-dates-for-issues/
[WIP MR]: http://docs.gitlab.com/ce/workflow/wip_merge_requests.html "Work In Progress Merge Request"
[www-gitlab-com]: https://gitlab.com/gitlab-com/www-gitlab-com/
[wrap text]: /handbook/product/technical-writing/markdown-guide/#wrapping-text
[Yubico]: /2016/08/31/gitlab-and-yubico-security-webcast/

<!-- Labels -->

[$100]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=%24+100
[$200]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=%24200
[TOP PRIORITY]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=TOP+PRIORITY
[Release]: https://gitlab.com/gitlab-com/www-gitlab-com/issues?label_name%5B%5D=release
[team]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=Team+Post
[Events]: https://gitlab.com/gitlab-com/www-gitlab-com/issues?label_name%5B%5D=Events
[Community Post]: https://gitlab.com/gitlab-com/blog-posts/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Community%20Posts
[Guest Post]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=Guest+Posts
[Partner Post]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=Partner+Post
[Ghost Post]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=Ghost+Posts
[Crosspost]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=Crosspost
[Up-for-grabs]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=up-for-grabs
[Up-for-grabs-GitLab]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=up-for-grabs-GitLab
[On-it]: https://gitlab.com/gitlab-com/blog-posts/issues?label_name%5B%5D=On-it

<!-- Styles -->

<style>
 .center {
   text-align: center;
   display: block;
   margin-right: auto;
   margin-left: auto;
 }
 .alert-purple {
   color: rgb(107,79,187);
   background-color: #fff;
   border-color: rgba(107,79,187,.5);
 }
  .purple {
   color: rgb(107,79,187) !important;
 }
   .ambar {
    color: rgb(138,109,59) !important;
 }
 </style>
