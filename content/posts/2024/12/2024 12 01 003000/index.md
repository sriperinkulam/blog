---
categories:
- Site
- ""
author: SSP
date: "2024-12-01T00:30:00-05:00"
draft: false
layout: IWArticle
month: 2024-12
params:
  IWkind: StatusNote
  syndication:
    fediverse: https://chat.srkn.org/@ssp/statuses/01JE0DXB15D0J7BY37VY44NR0F
tags:
- micro
- hugo
title: 2024 12 01 003000
year: 2024
---

Moved over the syndication links in my posts to post-meta. The syndication icon only shows up if a valid link is present in the FrontMatter of a post. Once micro.blog picks up the feed, it's currently set to auto publish to the fediverse on my GoToSocial (GTS) instance.  On the backend, a GO script fetches the RSS feed from my GTS instance and saves the RSS feed item link and the corresponding link to my post in a JSON file. Another script quickly looks up which post's FrontMatter needs to be updated for the syndication links in each post and updates the files as needed. A bit windy but seems to do the job for now. I might end up consolidating these into just one script later and/or directly use the masto API to publish to the fediverse and grab the syndication link from there. For now, I'm pretty psyched this is all working.
