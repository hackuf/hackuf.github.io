---
layout: post
title:  "New Project: Twitter AutoRefresh"
date:   2014-08-08 02:00:00
categories: blog projects
---

I've had this problem with Twitter and auto-refreshing so I wrote a Chrome extension to help with that. (Now available on the Chrome Web Store!)

When I use Twitter, I either scroll endlessly or I keep it open on a second monitor just watching the new tweets come in. However, I had this issue with my current auto-refresh extension because it would jump to the top of my timeline whenever I got a new tweet. And, to get the extension to stop refreshing, I had to go and manually disable the extension.

Well, no more! I decided to whip up my first Chrome extension (yay!) and have the refresh easily disabled. In order to do this, the extension creates a new module on the Twitter left dashboard that just contains clickable text that allows a user to turn on/off the refresh. To check to see whether new tweets came in, the extension just checks to see whether the title of the page was updated. Pretty neat, huh?

I have uploaded it to the Chrome Web Store, so you can easily install it by going to [the webstore link](https://chrome.google.com/webstore/detail/twitter-autorefresh/hnkdmkjkkgiahldbbejflafhdbkdmegd?hl=en&gl=US). And, if you want to view the code, check out the [repository on GitHub](https://github.com/andrewjkerr/twitter-refresh).

Make sure to tweet me [@andrewuf](https://www.twitter.com/andrewuf) to let me know what you think!

**Update August 8 12:45** - Twitter AutoRefresh now is on the Chrome Web Store! You can find it [here](https://chrome.google.com/webstore/detail/twitter-autorefresh/hnkdmkjkkgiahldbbejflafhdbkdmegd?hl=en&gl=US).