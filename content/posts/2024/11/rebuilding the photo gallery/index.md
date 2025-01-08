---
categories:
- Site
author: SSP
date: "2024-11-09"
draft: false
layout: IWArticle
month: 2024-11
params:
  syndication:
    fediverse: https://chat.srkn.org/@ssp/statuses/01JCABZ84Y4Q5Q267E20F4V3VQ
tags:
- hugo
title: Rebuilding the photo gallery
tootid: 01JCABZ84Y4Q5Q267E20F4V3VQ
year: 2024
---

Thanks to [Bill Glover](https://billglover.me/2023/11/07/creating-a-photography-gallery-with-hugo/), I was able to rebuild my [photo gallery](https://srikanthperinkulam.com/photos/). Similar to how I built this earlier in wordpress, all I'm doing is mimicking an archive page but with just the images. Took me a bit to figure out that the *with* function breaks the context and I had to dynamically reassign the permalink. With that sorted, this page should auto-update whenever I publish posts. Yay!