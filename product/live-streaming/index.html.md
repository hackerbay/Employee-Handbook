---
layout: markdown_page
title: "Live Streaming"
---

Go to the [Handbook](/handbook/)

### On this page
{:.no_toc}

- TOC
{:toc}

## Software

### Encoder
- [OBS Studio Win/Mac/Lin Open Source](https://obsproject.com/) or install with 'brew cask install obs' on mac

### Audio Rerouting
- [Soundflower Mac Open Source](https://github.com/mattingalls/Soundflower) or install with `brew cask install soundflower`
- [Loopback Mac Closed Source](http://www.rogueamoeba.com/loopback/) - Great closed source alternative
- [Windows alternatives](https://www.reddit.com/r/audioengineering/comments/3geqse/soundflower_alternative_on_windows/)
- [Linux alternatives](http://askubuntu.com/questions/602593/whats-a-good-soundflower-replacement-for-ubuntu)

### Important links

- [Youtube live streaming introduction page](https://support.google.com/youtube/answer/2474026?hl=en) - Here you can check if your channel meets all requirements for live streaming
- [Youtube tutorial on setting up a live stream](https://support.google.com/youtube/answer/2853700?hl=en) - If you need extra help or information on setting up a youtube live stream in general
- [Youtube live dashboard](https://www.youtube.com/live_dashboard#) - Here you can find your encoder setup variables, manage your stream and see your chat

## Setup

- Install both OBS Studio (encoder) and an audio rerouting software.
- [Check](https://support.google.com/youtube/answer/2474026?hl=en) if your channel is ready to live stream.
- Copy your encoder variables en setup your live streaming environment with the [Youtube live dashboard](https://www.youtube.com/live_dashboard#)
- Open up OBS Studio and open preferences
- Input your encoder variables under "Stream"

![obs studio preferences](/handbook/product/live-streaming/OBS_Studio_Stream.jpeg)

- Configure your to-be-recorded software's audio to be rerouted to an alternative audio source/output.
- Under "Audio" in OBS Studio preferences, select the alternative audio source/output under Mic/Auxiliary Device 2. See [this page](http://code-zest.blogspot.nl/2016/02/setting-up-obs-with-audio-output-in-mac.html) for more help
- Under "Video" select your preferred resolution and fps settings. Please take note that these should optimally reflect video aspect ratio's such as `1920x1080`.
- Optionally you can set up some output options under "Output"
- In de normal window of OBS Studio you should now see 2 audio sliders, including "Mic/Aux 2". Configure these to your liking.
- Select "Start Streaming": _You are now streaming_
- Go to your [Youtube live dashboard](https://www.youtube.com/live_dashboard#) to see your live stream and interact with your viewers.
