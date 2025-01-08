---
categories:
- Site
author: SSP
date: "2024-11-02"
draft: false
layout: post
month: 2024-11
tags:
- hugo
title: Migrating to Hugo
year: 2024
---

Open notes with a running list of things I'm working on for this site. 

## DEC 2024

- [ ] Build roadmap for Garmin posts migration
	- [x] Fetch activity summaries over as an archive
	- [ ] Build a yearly summary per activity 
- [ ] Add webmentions to the site. Thanks, [Hugo](https://hugo.md/post/add-webmentions-to-hugo-from-micro-blog/)!
	- Tweak CSS to display webmentions properly. Maybe explore [this](https://github.com/PlaidWeb/webmention.js).
	- Maybe explore setting up an interactions content type [like Jessica](https://www.jayeless.net/2021/02/integrating-webmentions-into-hugo.html)
- [ ] Fix syndication issues
	- Limit RSS Feed fetch to just 5 recent posts
	- Make FrontMatter updates Camelcase proof
	- Consolidate into just one GO script
	- Figure out how to fetch synd links for micro posts without embed links[^2]
- [x] Consolidate categories[^1]
- [ ] Convert old tweets to a summary page on this portal
- [x] Merge old instagram posts to the [photos](/photos) page[^3]
- [ ] Maybe add some pagination to the [micro](/micro) page
- [ ] Migrate old PixelFed photos over.
- [x] Add a proper comment form for posts[^4].
- [x] Setup a script to autopost to GoToSocial. 

[^1]: Wrote a quick GO script to consolidate these 
[^2]: Decided to add a permalink to each post at the end. A shortcode automatically fetches the permalink and adds it to the end of each post. 
[^3]: Moved the photos over. Decided to leave the photo notes behind. 
[^4]: [Decided to use ISSO](https://srikanthperinkulam.com/2024/12/09/last-mile-closures/) over Remark42
## NOV 2024

- [x] Used lonekorean's fantastic [wordpress-export-to-markdown](https://github.com/lonekorean/wordpress-export-to-markdown) tool to convert WP xml to markdown
- [x] learned that the *hugo server* and *hugo build* serve different purposes
- [x] Setup aliases on NUC and Thinkpond to quickly build and publish. Moved the actual publishing workflow to the Thinkpond and retained the main static site on the NUC.
- [x] Fixed permalinks to prevent link rot, almost?
- [x] Fixed RSS feed issues
	- [x] For posts tagged as *micro* set the title to just date+time so that micro.blog picks it up as a note and not display the title. 
- [x] Migrate older posts as deemed fit
- [x] Build a proper archive page. Made some decent progress, thanks to [D'Arcy Norman's](https://darcynorman.net/archives/), pointers [here](https://discourse.gohugo.io/t/listing-all-posts/30575/4) . 
- [x] Build a proper photo gallery
