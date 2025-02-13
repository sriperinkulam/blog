---
draft: false
title: Implementing static comments
date: "2025-02-05T21:30:00-05:00"
author: SSP
layout: IWArticle
params:
   syndication:
      fediverse: ""
   IWkind: StatusNote
categories: ["site",""]
tags: ["micro", "comments"] 
tootid: ""
---
![](images/comments.png)

I bit the bullet and setup a rudimentary comment system for this site. For the last few months, I relied on [ISSO](https://github.com/isso-comments/isso/), but it kinda felt a bit too heavy. Finally scratched the itch and switched over to a basic form and some javascript to push comments over to my self-hosted ntfy server. For now, I've left the moderation to manual mode - I have to copy over the comments manually from NTFY to a comments.json file. A GO script that usually publishes this site also builds the comments for each of the posts as needed  based on the posts' permalink. Pretty friction-less and nifty! {{< permalink >}}
