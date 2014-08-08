---
layout: post
title:  "New Project: TwitterRefresh"
date:   2014-08-08
categories: blog projects
---

I've had this problem with Twitter and auto-refreshing so I wrote a Chrome extension to help with that.

<br />

When I use Twitter, I either scroll endlessly or I keep it open on a second monitor just watching the new tweets come in. However, I had this issue with my current auto-refresh extension because it would jump to the top of my timeline whenever I got a new tweet. And, to get the extension to stop refreshing, I had to go and manually disable the extension.

<br />

Well, no more! I decided to whip up my first Chrome extension (yay!) and have the refresh easily disabled. In order to do this, the userscript creates a new module on the Twitter left dashboard that just contains clickable text that allows a user to turn on/off the refresh. To check to see whether new tweets came in, the userscript just checks to see whether the title of the page was updated. Pretty neat, huh?

<br />

To install, just enable "Developer mode" in the extensions page in Chrome and drag and drop the [downloaded twitter-refresh.user.js file](https://github.com/andrewjkerr/twitter-refresh/raw/master/twitter-refresh.user.js) onto that page. And, if you want to view the code, check out the [repository on GitHub](https://github.com/andrewjkerr/twitter-refresh).

<br />

Make sure to tweet me [@andrewuf](https://www.twitter.com/andrewuf) to let me know what you think!