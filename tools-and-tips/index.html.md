---
layout: markdown_page
title: "Tools and Tips"
---

## On this page
{:.no_toc}

- TOC
{:toc}

A lot of tools we use are described in the rest of the handbook (GitLab, Google
Docs, Google Hangouts, 1Password, etc.). This section is for tools that don't
fit anywhere else.

### Sundial

If you move to another location, you should update Sundial to reflect that change.
In order to do that:

1. Search for "Private Sundial URL" in Google Drive.
1. Go to the Sundial URL mentioned in the Google doc.
1. Click "Log in" in the upper right corner.
1. Choose to "Login with Google" using your GitLab Gmail account.
1. Hover over your name in the upper right corner and choose "Update your location".

### Google Slides templates

Use these [GitLab branded slide templates](https://drive.google.com/drive/folders/0B6i7Xg1yiB8teTdIT21pWHYwYms?usp=sharing) when creating slide decks for internal or external use. Make a copy of the slide deck and only edit the copy; do not edit the template itself.

#### Updating your slide deck theme

Here are a few quick steps for updating your slide decks to match the most recent template:

1. In the top toolbar click `Theme` which will open the Themes panel (on the right-hand side).
![Change theme in Google Slides](/images/handbook/tools-and-tips/google-slides-change-theme.png)
1. At the bottom of the Themes panel, click `Import theme`.
1. In the Import theme dialog box type `template` into the search field.
1. Find the `GitLab-Deck-Template-Dark` or `GitLab-Deck-Template-Light` and click the `Select` button in the bottom left to apply the theme to your slide deck.

### Google Forms templates

Use these [Gitlab branded form templates](https://drive.google.com/open?id=0BxrZ6azkqZ1bVDl1TTZuelFOb1k) when creating internal or external surveys or forms. Make a copy of the form and only edit the copy; do not edit the template itself.

### Calendly

[Calendly](https://calendly.com/) connects to your Google calendar so people can book a time with you without having a Google Account.

1. Set up a [Calendly](https://calendly.com/) account.
1. Link it to your GitLab Google Calendar to make it possible for people to schedule a call with you.
1. All meetings will have the same Google Hangouts URL on your calendar based on your @gitlab.com email handle. You can use that in the booking text above. Events on your calendar will automatically have the Google Hangouts URL added, so you can use [the plus landing page](https://plus.google.com/hangouts/_/gitlab.com) to quickly jump into the call. Please note that the appointment will show up in other people's calendars with a different link, so it is essential that you set a text with the link for your time slot as specified below.
1. Set up the 45 minute time slot with the following event description text (replacing XXXXX with your @gitlab.com handle):

    > This will be a Google Hangouts at https://plus.google.com/hangouts/_/gitlab.com/XXXXX
    >
    > Question? Please email me. GitLab Primer: https://about.gitlab.com/primer/

1. If you intend to use any of the other event types, make sure to add this to their event descriptions as well.
1. For people outside of GitLab Inc, send them your Calendly link that links directly to the 45 minute time slot: "Are any of the times on https://calendly.com/XXXXX/45min/ convenient for you? If so please book one, if not please let me know what times are good for you and we'll find an alternative."
1. Update your availability on [Calendy Event Types](https://calendly.com/event_types/).
1. Add your Calendly link to your [Slack profile](https://get.slack.help/hc/en-us/articles/204092246-Editing-your-profile). For `Display Text`, use this line: `Schedule a meeting with me!` so GitLabbers can schedule a 1:1 call with you in GitLab, by simply clicking your Calendly link in your Slack profile.

Keep in mind that unlike normal Google Calendar events, Calendly events are not automatically synchronized between both parties when changes are made. If an event needs to be cancelled or modified, make sure to use Calendly to do so.

### Shush

[$4.99 tool for OS X](http://mizage.com/shush/) that lets you set a hotkey (e.g. `fn`) to mute your microphone ("push-to-talk" or "push-to-mute").
Never again will you have to switch your window focus to Google Hangouts or Zoom to speak or mute.
The icon will show the current state of your mic input (x means muted).
With a right click (or your configured hotkey) you can switch from push to talk to push to mute.
Don't forget to unblock your mic in Zoom/Google Hangouts immediately after joining.
Be warned that page up with fn+down arrow will activate it.
Use space for page down instead of fn+up arrow.

#### Shush alternative for Linux

If you use Linux (e.g. [Arch](https://www.archlinux.org/), [Ubuntu](https://www.ubuntu.com/) or [Fedora](https://getfedora.org/)) you can create a system-wide keyboard shortcut to mute/unmute your mic.
Please note that it only works for Linux distributions which use [ALSA](http://alsa-project.org) for sounds (most popular Linux distributions use ALSA). All you need to do is go to your desktop environment's _Keyboard Settings_ and create a custom shortcut with the command `amixer set Capture toggle` and assign a key combination of your choice (e.g. `Pause Break` key). Once this is done, you can mute/unmute your mic using the assigned keyboard shortcut while you're in any application. Refer to this original answer on [Askubuntu](http://askubuntu.com/a/13364/12242) to learn more.

### Disabling OS X Notification Center

During a presentation or screen share, you might want to disable your notifications on OS X to prevent distractions or possible embarrassment.

The Notification Center can be quickly disabled by Option-Clicking the menu bar icon in the top right of your screen. This disables notifications until the next day. Option-Click again to re-enable immediately. Alternatively, click on the Notification Center icon, then scroll _up_ to reveal the "Do Not Disturb" toggle.

### Slack

#### Do Not Disturb Hours

Slack now supports "Do Not Disturb Hours" so you won't be pinged in the middle of the night or while you are dealing with family matters. You can set your "Do Not Disturb Hours" by clicking on the bell at the top of the left pane in the Slack app. You also have the option of snoozing for 20 minutes or up to 24 hours. Note: Do Not Disturb can be overridden in the event of an emergency. See Slack documentation for more information.

#### Browse Channels

You can browse all available GitLab channels by clicking on "Channels" on the left pane in the Slack app. From there, you can see every channel, who created it, and how many members there are. Every team member is automatically added to `#general`, where announcements are made and information for the entire company is shared. There are also a few default channels that every new hire is added to, such as: `#celebrations`, `#new_labbers`, `#questions`, `#random`, `#thanks`, & `#working-on`; these channels are optional, but we think they are a great place for team members to interact and get to know each other.

#### Slack Status

Slack has the functionality to set an individual [status](https://slackhq.com/set-your-status-in-slack-28a793914b98). For example, you can select away from keyboard, vacation, or working remotely. This is a great way to let your team know if you are available or not.

### Google Calendar

#### Modifying Events
[This Chrome extension](https://chrome.google.com/webstore/detail/google-calendar-guests-mo/hjhicmeghjagaicbkmhmbbnibhbkcfdb?hl=en) will allow guests to modify calendar appointments by default.

Add a filter to remove invites responses from your inbox with the following query:

`*.ics subject:("invitation" OR "accepted" OR "rejected" OR "updated" OR "canceled event" OR "declined") when where calendar who organizer`

#### Gitlab Availability Calendar

The GitLab Availability Calendar is available to all team members on a read/write basis. It should be automatically be in your calendars list on the left side of your screen in Google Calendar. This calendar is the place for:

* Adding your time off so team members know when you'll be unavailable.
* Company-wide meetings, such as the [Team Call](https://about.gitlab.com/handbook/communication/#team-call), [Functional Group Updates](https://about.gitlab.com/handbook/people-operations/functional-group-updates/), [Retrospectives & Kickoffs](https://about.gitlab.com/handbook/communication/#kickoffs), and more.

Anyone in GitLab can go into the GitLab Availability calendar and invite themselves to one of these events, or change the details (for example, if you are adding presentation slides). If you are unable to do so, please reach out to People Ops.

Note: To avoid calendar noise, time off / unavailablity events should be limited to full-day calendar entries.  There is no need to add personal appointments or other short events to the calendar, as timed events should be reserved for company-wide meetings.

#### GitLab Team Meetings Calendar

The GitLab Team Meetings Calendar is also available to all team members and can be found in your calendars list. You can find the details for other teams' meetings here, so you can attend a different team's meeting and ask questions, learn about what they're working on, and get to know the rest of the GitLab functional groups. These meetings are open to everyone in GitLab. If you are creating a new team meeting, please copy it to the GitLab Team Meetings calendar, and reach out to People Ops with any questions.

### Zoom

To set up a Zoom meeting, sign up for a free [basic account](https://gitlab.zoom.us/signup) using your GitLab email address, and share the link for your "personal meeting room" with your participants. Note that on the Basic license, meetings are capped at 100 people, and meeting durations are capped at 40 minutes. If you need to be able to organize calls longer than 40 minutes using Zoom, contact Jennifer Garcia or #peopleops to be granted a [Pro account](https://about.gitlab.com/handbook/general-onboarding/onboarding-processes/#onboarding-processes). By default, only Support Engineers and members of the Sales team are given Pro accounts during onboarding since their job routinely involves making video calls with (potential) customers.

To record the meeting set up [cloud recording](https://support.zoom.us/hc/en-us/articles/202921119-Automatic-Recording). You can also configure Zoom to save to the cloud automatically. Go to "My Meeting Settings" and find the "Recording" section, then click on "Cloud Recording".
Setting the topic of the meeting is important, otherwise all meetings will be recorded with a generic name. Once recording is complete, your videos will not appear in the “Recordings” section of your Zoom account. Your recordings will automatically be saved to a folder on Google Drive under "GitLab Videos".

Our Zoom account has [End-to-End Encryption](https://gitlab.com/gitlab-com/peopleops/issues/223) enabled. This may impact performance, so if you run into any issues, let People Ops know.

If there is a meeting active, a new meeting cannot start until the host ends the meeting or all participants leave. People Ops can force end a meeting by logging into Zoom with the credentials in 1Password, going to My Meetings, finding the meeting they would like to end, then selecting "End." This will allow the next meeting to begin.

#### Livestreaming to YouTube

You can use Zoom to livestream your meeting directly to YouTube.
It requires some preparation, so make sure to do the first three steps ahead of time.

1. Make sure you have access to the GitLab YouTube account. Read the secure note in 1Password called "Youtube" for instructions.
1. Ask for the Zoom Webinar license to be assigned to you by Jennifer Garcia or #peopleops at least one day in advance, and let #peopleops know when you are done using it. Or share Zoom account within team. 
1. Schedule your meeting as [webinar](https://zoom.us/webinar/).
1. Join the meeting ahead of time, click on `More` and `Live on YouTube`.
1. Now choose the GitLab YouTube account and mark it as `Public` (or unlisted for a test).
1. Click in Zoom on `Go Live!` to start streaming.

There are a few limitations:

1. Only 50 people can be 'presenters', that is people sharing their video and audio.
1. You will have to manually promote people to become presenters, from being just attendees. Do this by going to participants and clicking on the dropdown menu. Promote people to the highest level to allow them to promote others.

The video of the livestream will be available automatically on YouTube and anyone visiting our YouTube page
will be notified that we're streaming live.
Sharing the stream after it already started is fine, people can go back in time,
even while the stream is ongoing.

[See the Zoom documentation on live streaming](https://support.zoom.us/hc/en-us/articles/115000350446-Streaming-a-Webinar-on-YouTube-Live)

#### Zoom on Linux using FOSS (Firejail)
While Zoom works on Linux, the application is not free software. As a result,
some might be wary of running this directly on their computer. One way of
running Zoom without worrying about what it does is to use
[firejail](https://firejail.wordpress.com/).

To use Zoom with Firejail, first install Zoom or download the archive. Zoom
offers standalone binaries that you can download should your distribution not
have a package for Zoom. Once installed, install firejail.

Once both firejail and Zoom are installed we need two things:

1. A firejail profile for Zoom
2. A directory we can use as the home directory for Zoom, preventing it from
   messing with your home directory

You can use the following firejail profile and store it in
`~/.config/firejail/zoom.profile`:

```
noblacklist ~/.config/zoomus.conf

include /etc/firejail/zoom.local
include /etc/firejail/disable-common.inc
include /etc/firejail/disable-programs.inc
include /etc/firejail/disable-devel.inc

whitelist ~/.zoom

caps.drop all
netfilter
nonewprivs
noroot
protocol unix,inet,inet6,netlink
seccomp

private-tmp
```

Next we need a home directory for Zoom. For this example we'll use
`/opt/zoom/home`:

```bash
sudo mkdir -p /opt/zoom/home
sudo chown -R $USER /opt/zoom
```

With this in place we can start Zoom using firejail as follows:

```bash
firejail --quiet --profile=~/.config/firejail/zoom.profile --private=/opt/zoom/home /path/to/zoom/ZoomLauncher
```

Note that you must start the `ZoomLauncher` binary and not the shell script
wrapper called `zoom`.

### Google Cloud Platform

Please see the secure note with the name "Google Cloud Platform" in the shared vault in 1password for the credentials.

Once in the console, you can spin up VM instances, Kubernetes clusters, etc. Please
remove any resources that you are not using, since the company is [billed
monthly](https://cloud.google.com/pricing/). If you are unable to create a
resource due to quota limits, file an issue on the [Infrastructure
Tracker](https://gitlab.com/gitlab-com/infrastructure).

### Gmail

#### Filters

It might be useful to add a Gmail filter that adds a label to any GitLab
notification email in which you are specifically mentioned, as opposed to a
notification that you received simply because you were subscribed to the issue
or merge request.

1. Search for `@your_gitlab_username` in Gmail.
1. Click the down arrow on the right side of the search field.
1. Click "Create filter with this search".
1. Check "Apply the label:" and select a label to add, or create a new one, such
   as "Mentioned".
1. Check "Also apply filter to matching conversations.".
1. Click "Create filter".

#### Advance

If you use the archive function you normally return to your overview.
With auto-advance you can return to the next message.
Enable "Auto-advance" in the labs section under settings.
The default setting of showing the next older message is OK.

#### Email signature

Set up an [email signature](https://support.google.com/mail/answer/8395) which includes your full name and job title so people can quickly know what you do.

### Hangouts

Computers with older CPUs (pre-2016/Skylake) may be missing hardware acceleration for [VP9](https://en.wikipedia.org/wiki/VP9#Hardware_encoding.2Fdecoding_support).
In Chrome, this can cause excessive CPU due to use of the codec.
On MacOS switching to Safari or using [h264ify](https://github.com/erkserkserks/h264ify) ([Chrome Web Store](https://chrome.google.com/webstore/detail/h264ify/aleakchihdccplidncghkekgioiakgal)) solves this since it will use h264 that is hardware accelerated.

To check the status of acceleration on Chrome, see the "Video Encode" option in [about://gpu](about://gpu).

### Hangouts on air

Hangouts on Air probably only works with a maximum of 15 people for scheduled calls (same limit as normal Google Hangouts).

Potential problem: even when I logged in as GitLab and got the bar below the call, I could not switch it to on-air!
I did notice that the time was not properly set (anymore?).
I did a test event before and that seemed to work OK.
I'll try one more time to see if it works.

Potential problem 2: the video showed up as listed by default

Go to [My live events on YouTube](https://www.youtube.com/my_live_events) and switch to the GitLab account on the top right (you need to be a manager of our YouTube channel).

Go to => life streaming => events and create a new one with the attributes:

- type => quick (using Google Hangouts on Air)
- advanced: promotions: disable both checkboxes
- time needs to be set correctly

The view on watch page URL only allows for people to watch it.
Window that pops up when you press the start hangout on air button has the proper URL that you can send to other people and/or add it to the calendar invite, it is structured like: https://plus.google.com/hangouts/_/ytl/LONGHASH.
When people join the event they have to [accept a warning](https://gitlab.com/snippets/16245).

[Completed live events](https://www.youtube.com/my_live_events?filter=completed) will show the video and you can click the image to view it.
You can use actions to make it public here

BTW Trying to set this up via Google+ via [Hangouts on Air](https://support.google.com/plus/answer/7126353?hl=en) instead of via YouTube doesn't seem to connect to the right YouTube channel, even if you selected the right account on the top right.

###Grammarly
[Grammarly] (https://www.grammarly.com) is a good tool for those who want to feel more comfortable drafting written communication in English (American or British). There is a free and premium version.

### Gravatar

Link your GitLab email address to an easily recognizable photo of yourself on [Gravatar](https://en.gravatar.com/). It is company policy to use a photo, and not an avatar, a stock photo, or something with sunglasses for any of your GitLab accounts, as we have a lot of GitLabbers and our brains are comfortable with recognizing people; let's use them.

### Appear.in

[Appear.in](https://appear.in/) allows you to instantly create a free video chat room for up to 8 participants with no login and no installation. It also offers a free reliable mobile video conference app.

### One Tab

[One Tab (Free)](https://www.one-tab.com/) tames tabs into a list which can be sorted and exported.

### Quitter

[Quitter (Free)](https://marco.org/apps) will switch off apps for you after some period of inactivity. Consider using this to hide Slack after a while to reduce your urge to check new messages all the time.

### TripMode

[TripMode ($7.99)](https://www.tripmode.ch/) lets you control which apps can use the internet. Especially useful when you're working on a cellular/metered connection.

### ShareX

[ShareX (Free / Windows only)](https://getsharex.com/) is the ultimate screen capture toolbox for Windows, which includes many different options to record your screen and automate your workflow with automatic uploading, resizing and much more.

### Teampaper Snap

[Teampaper Snap (Free / Mac only)](http://teampaper.me/snap/) is the ultimate screen capture tool for Mac to voice your thoughts on anything you can see on a screen.

### Clocker

[Clocker (Free / macOS Only)](https://abhishekbanthia.com/clocker/) adds a clean and distraction free world clock to your menu bar so you can check on your fellow teammates across different timezones.

### Check which process occupies a given port

When the GitLab Development Kit cannot start using the `./run` command and
Unicorn terminates because port 3000 is already in use, you will have to check
what process is using it. Running `sudo lsof -i -n -P | grep TCP | grep 3000`
will yield the offender so this process can be killed. It might be wise to alias
this command in your `.bash_profile` or equivalent for your shell.

### Shell aliases

Use command aliases in your shell to speed up your workflow. Take a look at [these aliases](https://gitlab.com/sytses/dotfiles/blob/master/zsh/aliases.zsh) and others in [Sid's dotfiles project](https://gitlab.com/sytses/dotfiles/tree/master). For example, by adding the following to your `.bash_profile` or equivalent for your shell, you can just type <kbd>s</kbd> to checkout the `master` branch of this website, pull the latest changes, and open the repository in Sublime Text:

```sh
alias gco='git checkout'
alias gl='git pull --prune'
alias gca='git commit -a'
alias gp='git push origin HEAD'
alias www='cd ~/Dropbox/Repos/www-gitlab-com/source'
alias s='www;subl .;gco master;gl'
```

After editing, you can just type <kbd>gca</kbd> to commit all of your changes, followed by <kbd>gp</kbd> to push them to the remote branch.

### Sublime text

Putting the following in Preferences.sublime-settings - User will among other things ensure that if you open the www-gitlab-com website you're not opening the output files by accident:

```
{
    "font_size": 18,
    "spell_check": true,
    "translate_tabs_to_spaces": true,
    "trim_trailing_white_space_on_save": true,
    "folder_exclude_patterns": ["public"]
}
```

### MobileDay

If you install [MobileDay (Free)](https://mobileday.com/) on your phone and give it access to your Google Calendar it can dial into conference calls for you. It is very good at detecting the number and password from the calendar invite.

### Keeping You Awake

[Keeping You Awake (Free & Open Source)](https://github.com/newmarcel/KeepingYouAwake) is a macOS utility application that can prevent your Mac from entering sleep mode for a predefined duration or as long as it is activated.

### Enable screen lock on your mac menu bar

1. Open up the `Keychain Access` application
2. In the menu bar (next to the apple logo), click on `Keychain Access`
3. Click on `Preferences`
4. Check the box `Show keychain status in menu bar`
5. The lock icon should now show up on your menu bar

You can lock your screen by clicking the lock icon on the menu bar and clicking `Lock Screen`

### Visual help to differentiate between GitLab servers

If you are working on multiple GitLab instances and want to have a visual differentiation, you can change the default [Application theme](https://docs.gitlab.com/ee/user/profile/preferences.html#syntax-highlighting-theme) to a different color.

### How to change your username at GitLab.com

- Starting point: let's say your username is `old-mary` and you want it
to be just `mary`.
- **Note:** each GitLab account is tracked by an **userID**, which is a number stored in
a database. If we change the username, the userID does not change. And all the
permissions, issues, MRs, and relevant stuff within GitLab are related to your
**userID**, not with your username.
- **Note:** if you are not a GitLab Team member, the same process applies except
your e-mail ([STEP 2](#change-username-step-2)), which will be different
(will not be @gitlab.com email), so you can replace it with your own email account.

**STEP 1: Request your new username**

- Access the username you want to request via `https://gitlab.com/mary`.
- Check its activity and projects to see if he/she is an inactive user
[according to the handbook](/handbook/support/policies/#dormant-usernames).
- Send your request to `support@gitlab.com`, explaining the reasons why
you need that username.
- There's no guarantee that the username will be available for you. Please
check the [handbook guidelines for dormant usernames](/handbook/support/policies/#dormant-usernames).

**STEP 2: Create a new account with your new username**
{: #change-username-step-2}

- If support replies to you telling that the username is free to use, create a new
GitLab.com account with it. Use a personal email to register your new account and
choose one that has not been used with your old GitLab account.
- Navigate to your [**Profile Settings** > **Emails**](https://gitlab.com/profile/emails),
and add a new email. ⭐️ **Trick** ⭐️ If your email at GitLab is `mary@gitlab.com`,
add the new email as `mary+something@gitlab.com`:
this is a [Gmail trick](https://support.google.com/mail/answer/12096?hl=en)! All
your emails sent to this alias will end up in your GitLab email account. 😃
- Navigate to <https://gitlab.com/profile/notifications> and choose the notifications
email: `mary+something@gitlab.com`.
- Open your old account in one browser and the new one in another browser
(e.g., Chrome and Firefox, or Chrome and Safari) - log in to both accounts at
the same time.

**STEP 3: Let's have some fun (kidding, this is critical!)**

- Navigate to <https://gitlab.com/profile/account> in both your accounts.
- Look for your username. This operation has to be done quickly, otherwise you are
risking to loose your awesome new username to someone else quicker than you. We
need to **swap** the usernames between both accounts, so you'll keep all your
history, your privileges, issues, and MRs assigned to you, etc.
- If you work with 2 monitors, open each browser on one monitor. If you don't,
open them side by side, so that you can keep an eye on both at the same time.
- Rename your new username `mary` to something like `mary-1` and **DO NOT** click
**update username** yet. Rename your old username `old-mary` to your new
username `mary` and **DO NOT** update that either. Just leave them typed into the boxes.
- Make sure you did the previous step right!
- ⚠️ **CRITICAL** ⚠️ Update the first one (`mary` to `mary-1`). Immediately, click
**update** on the other one (`old-mary` to `mary`).
- Immediately, rename the `mary-1` to your old one `old-mary` and click
**update username** again.
- Ta-Da! 🙌

**STEP 4: Move your projects (or not)**

- Now, if you have any personal projects, you might want to import them to
your new account (the one that has your old username now). To do that, in
your new account (the one with the old username), click **Create a New Project**,
give it the very same name as the original one, click **Git - add repo by url**,
and paste the `https://` url of your project there. To make things easier, make
sure all the projects you want to import are set to `public` view.  You can make
them private afterwards.
- If you have GitLab Pages projects with the default **GitLab.io** url, you will need
to import them to you new account, then make a change to **trigger a build** and
redeploy your site. They will be affected only if you're using a
[CNAME with a subdomain instead of an A record](/2016/04/07/gitlab-pages-setup/#custom-domains).
This won't affect Pages projects that use custom domains, as they all point to
the same Pages server IP via `A` record. Your groups won't be affected either,
as they operate under their own namespace. Add both users as members of your
groups and nothing changes.

That's it! Don't forget to update your username on the
[team page](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/team.yml)
and on the [Marketing Handbook](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/source/handbook/marketing/index.html.md),
in case you're a Marketing Team member.

### How to share a presentation in Zoom

At some point, you may need to give a slide presentation using Zoom. Ideally, you should be able to see your speaker notes while participants see your slide show. This is fairly easy to do with two monitors by using presenter view and sharing the monitor which contains the slides. If you have only one monitor, it is still possible using the following steps:

1. Open your slide deck in Google Slides. Make sure to close any other tabs you may have open. Participants will be able to see these tabs when it comes time to present.
1. Select `Presenter view`. This will make your presentation take up the entire screen.
1. Hover near the bottom of your presentation and you will see a pop up menu. From this menu, select the `Toggle Full Screen` option, third button from the right, next to settings. This will end full screen mode without leaving the presenter view.
1. To see your speaker notes, hover at the bottom of your presentation window again and select `Presenter View` from the menu.
1. You will now have a presenter view pop-up window which allows you to see your speaker notes as well as advance the slides.
1. In another browser window enter the Zoom meeting room.
1. Once in the meeting, select `Share Screen` from the options at the bottom of the screen.
1. Do not share your desktop. From the options, select the browser window containing your Google Slides deck. This will allow you to share just the browser window containing your slides.
1. If you would also like to see the Zoom chat, hover your cursor at the top of the screen containing your Zoom meeting. A menu will appear, from this menu select More > Chat.
1. Position the windows any way you need to see the presentation and speaker notes.
1. Make sure to change slides using the presenter view pop up window. This will advance the presentation for your viewers as well as advancing your speaker notes.

If you would like to practice presenting, you can do so using your own private Zoom room.

1. Open the Zoom app and click `Start with video`.
1. Click `Record`.
1. Repeat the steps above.
1. Stop and watch the recording. You'll see what the participants would see.

### How to create gifs

We have a [dedicated section](/handbook/product/making-gifs) for that in the handbook.

### Long haul flights

Note: you have to pay for these items yourself.

- [Quiet comfort 35 Bose over ear noise canceling headphones](https://www.bose.com/en_us/products/headphones/over_ear_headphones/quietcomfort-35-wireless-ii.html)
- [Shaped sleep mask](https://www.amazon.com/gp/product/B01HYIER7W/ref=oh_aui_search_detailpage?ie=UTF8&psc=1) (so it doesn't touch your dyed out eyes)
- Custom molded ear plugs (can be up to $200 hearing aid store but are usable in many situations, there are also [DYI kits](https://www.amazon.com/Radians-CEP001-Custom-Molded-Earplugs/dp/B003A28P4I) but Sid has not tried that)
- [Melatonin](https://www.webmd.com/vitamins-supplements/ingredientmono-940-melatonin.aspx?activeingredientid=940) (possible unsafe during pregnancy and breast-feeding)
- Sleeping pills (over the counter is fine)

### Do NOT Use

**Flash**: Due to security flaws, we strongly recommend _not_ using Adobe Flash. Certainly do not install it on your local machine. But even the Google Chrome plugin that let's you see embedded Flash content in websites can pose a security hazard. If you have not already, go to your [Chrome Flash Settings](chrome://settings/content/flash) and disable Flash. For further context, note that [Google Chrome is removing Flash support soon](https://nakedsecurity.sophos.com/2016/05/18/yet-more-bad-news-for-flash-as-google-chrome-says-goodbye-sort-of/), and while the [plugin is better than a local install of Flash](http://security.stackexchange.com/questions/98117/should-flash-be-disabled-or-are-sandboxes-secure-enough), it still leaves vulnerabilities for [zero-day attacks](http://www.pctools.com/security-news/zero-day-vulnerability/).
