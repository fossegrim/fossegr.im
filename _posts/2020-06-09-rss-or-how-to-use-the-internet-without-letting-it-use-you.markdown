---
categories: [computing, productivity, emacs, rss]
layout: post
title: RSS or How to Use the Internet Without Letting It Use You
---
> Just use the Internet and don't let it use you
    
This post is about how I use RSS, and you should, to put the control of the content you consume on you, as opposed to mal-intentioned web-sites.
## The problem
The Internet is full of distractions, and why would it not be? Companies profit from your time spent on their web-site and therefore they want to maximize that time. Over the years they have become quite good at this.

One of the techniques media sites uses to achieve this is creating feedback loops. By repeatedly feeding you more and more content to consume they keep you in for as long as possible. Different sites do this in different ways. In the case of streaming web-sites such as YouTube new content is suggested and played continuously on the side-bar. Other web-sites like reddit and twitter do this by continuously appending new content when the user reaches the current end of the web-page.

This is a very inefficient and far from ideal way of consuming media which really benefits the companies profiting from your attention. But you still need to consume your media right?

## The solution
Luckily there is a solution which allows you to not have to rely on the feedback loops of media sites to consume their content.

RSS or Really Simple Syndication is an *ancient* protocol from the late 90s for subscribing to updates from web-sites. There are RSS feeds available for lots of web-sites among which are Hacker News, YouTube and many more. I will get back to how to subscribe to these later on.

The difference between RSS and the feed services offered by media web-sites is that with this the end user is in control. The way it works is that the web-sites publishes a feed of content that a RSS client can subscribe to. Then the RSS client can retrieve the feeds and thereon out the feed is in your hands permanently. Your RSS client can process the feed further before displaying it to you if you so prefer.

## Setting up an RSS client
To get started with RSS you need an RSS client. I personally use elfeed in Emacs, but any client will do. In this section I will show you how to get started with elfeed. If you do not use Emacs I recommend using another client. Any client will do, but [feeder](https://feeder.co) looks like a good start. The only requirement is the ability to subscribe to feeds which all clients by definition satisfy.

If you use Doom Emacs installation is done by uncommenting the RSS package in `~/.doom.d/init.el` and reloading Doom with `SPC h r r`.

Otherwise you can install the elfeed package directly from Melpa using use-package or any other method you would like.

```Lisp
(use-package elfeed)
```

Thereafter you can set the `elfeed-feeds` variable to a list of the feeds you want.
```Lisp
(setq elfeed-feeds
      '(feed-1 feed 2 ...))
```

You can view your feeds with `M-x elfeed` and update them with `M-x elfeed-update`.

## Subscribing to web-sites
Now that we are set up with a RSS client need to add some feeds to it.

As said earlier we will set up feeds to my blog, Hacker News and YouTube.

### My blog and Hacker News
Setting up feeds for Hacker News and my blog is simple. Simply subscribe to the respective feeds: [news.ycombinator.com/rss](https://news.ycombinator.com/rss) and [fossegr.im/feed.xml](http://fossegr.im/feed.xml). These feeds are equivalent to the current front page of Hacker News and the blog posts on my web-site.

### YouTube
YouTube maintains RSS feeds for all channels and playlists. Getting the URLs is not intuitive, but easy none-the-less.

#### Channels
The RSS feed URL of a channel is the channel id appended to `https://www.youtube.com/feeds/videos.xml?channel_id=`. The channel id is found at the end of a normal channel URL as illustrated in the screenshot.
![My YouTube channel](/assets/images/my-youtube-channel.png)

For example the RSS feed URL of my YouTube channel is [https://www.youtube.com/feeds/videos.xml?channel_id=UCWQ1f0ZhD-qhJB3AfJEoW0w](https://www.youtube.com/feeds/videos.xml?channel_id=UCWQ1f0ZhD-qhJB3AfJEoW0w).

#### Playlists
To get a playlist RSS feed URL the process is similar.
The RSS feed URL of a playlist is the playlist id appended to `https://www.youtube.com/feeds/videos.xml?playlist_id=`. The playlist id is found at the end of a normal playlist URL as illustrated in the screenshot.![A YouTube playlist](/assets/images/a-youtube-playlist.png)

For example the RSS feed URL of Protesilaos' Emacs playlist is [https://www.youtube.com/feeds/videos.xml?playlist_id=PL8Bwba5vnQK14z96Gil86pLMDO2GnOhQ6](https://www.youtube.com/feeds/videos.xml?playlist_id=PL8Bwba5vnQK14z96Gil86pLMDO2GnOhQ6)

### Other feeds
There are many other web-sites supporting RSS. In my experience most web-sites worth using has either first or third party RSS feeds available.

Take care

Olav
