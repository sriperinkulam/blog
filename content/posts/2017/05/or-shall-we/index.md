---
categories:
- Micro
- Micro
date: "2017-05-23"
tags:
- chatter
- facepiles
- indieweb
- webmentions
title: Or, shall we?
---

Spent sometime today troubleshooting two pesky issues.

Having switched to a new theme I realized my publishing workflow wasn't fetching comments from Instagram posts. The Dsgnwrks plugin was fetching the images fine.  But since I'd missed adding the syndication link for brid.gy to work its magic, the comments were not being back fed. This should be an easy fix. Probably I'll use the custom fields that dsgnwrks creates and update syndication links field using  a quick custom function.

The second issue was that the new theme wasn't displaying webmentions. What should have been a quick fix, took me some time to figure out that the comment block was only being called if there were any 'comment' type comments. Quickly added an 'or' to check for 'webmention' type comments too and that was set. One of those pesky 'must have caught earlier' issues!

Now that these have been sorted out, I'll probably work on displaying these 'likes' as facepiles.
