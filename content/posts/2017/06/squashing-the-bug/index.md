---
categories:
- Micro
date: "2017-06-30"
tags:
- chatter
- indieweb
- liked
- microformats
title: Squashing the bug
---

Squashed a minor bug in my code for 'favorite' posts. The post wasn't getting marked up with Microformats when the content (response) was blank.

The way it's currently setup, I have just one workflow for all 'types' of post (podcast, reply, like, repost, bookmark, read etc.) and looks like I missed a logic flow that 'like' posts may not necessarily have a note from me. A quick conditional check and the workflow works like a charm!

![](images/cropped-cropped-SP01-550afdebv1_site_icon.png)[Srikanth Perinkulam](https://srikanthperinkulam.com)
