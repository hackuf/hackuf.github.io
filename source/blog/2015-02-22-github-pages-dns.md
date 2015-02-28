---
title:  "Setting Up A Domain for GitHub Pages"
date:   2015-02-22 00:45:00
tags:   github, dns
---

<style>
.gist {
  width: 336px;
  display: block;
  margin: 0 auto;
}
</style>

Today, I decided to switch to using a custom domain with GitHub Pages instead of just forwarding to my GitHub Pages URL. Since andrewjkerr.com is my personal domain, I figured that a re-direction wasn't as professional as just masking and it was pretty simple to do. However, there was a small issue I ran into and, since I will probably do this again, I decided to document the process for future reference.

The first step to using a custom domain with GitHub Pages is to upload a file named `CNAME` to your respository with your custom URL in it. For example, my [CNAME](https://github.com/andrewjkerr/andrewjkerr.github.io/blob/master/CNAME) file just has `andrewjkerr.com` in it. You can do this pretty easily from the command line: `echo 'example.com' > CNAME`. Commit it, push it, and you're good to go as far as GitHub is concerned.

Now, you might have noticed that I left the www off. Why? Well, because I think the URL looks better without it. As far as I know, the tech community is split on whether www is depreciated or not, but you better pick one and stick with it. There are plenty of well known sites that leave the www off (Twitter and GitHub are great examples) and even Safari strips the www off in the address bar. GitHub Pages is smart enough to redirect to whatever URL is in your CNAME file. For example, if you leave off the www in your CNAME file, GitHub will redirect `www.example.com` to `example.com` and vice-versa.

Once you've pushed the CNAME file to your respository you can go ahead and add the A records to your domain. In order to have the www/no-www to work, you'll need to add A records for both @ and www like the following:

<script src="https://gist.github.com/andrewjkerr/417e7362047c5fe63aa7.js"></script>

With these records added, go ahead and run `nslookup example.com` and `nslookup www.example.com` and you should see that your domains are now pointed to GitHub:

<img src="/img/andrewjkerr-nslookup.png" style="display: block; margin: 0 auto" />

And that's it! I've found that the only problem with using a custom domain on GitHub is losing HTTPS so, if you need HTTPS, I would recommend against doing this. But, if you don't need HTTPS, it's so easy to use a custom domain that there's no reason not to!