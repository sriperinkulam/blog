---
title: "Sitelog"
layout: "now"
url: "/sitelog"
summary: sitelog
date: '2024-11-30'
hidemeta: true
rss: false
---

Sort of a change log to keep track of modifications done to this portal.
### Tuesday, 04. February 2025 10:21PM 
- Disabled ISSO and setup a custom comments framework.

### Saturday, 01. February 2025 07:11PM 
- Brought in the [book notes](/book-note) from the old site. Not much but a placeholder for future notes. 

### Saturday, 25. January 2025 10:20PM 
- Incorporated a way to show both the gpx map and garmin data summary in one visual block.

### Friday, 24. January 2025 04:18PM 
- Added a [More](/more) tab to collect all the random pages that I've created in the past.
- Moved the comments under a button for lazy loading.

### Friday, 17. January 2025 12:39AM 
- Added posts count on the archive page
- Added a quasi-firework display for posts tagged "Year End notes". Currently only works starting 2024.

### Saturday, 11. January 2025 11:16AM 
- Migrated site to Github. Might have to modify my posting workflow a bit. 
- Fixed images not showing up on the [micro](/micro) tab. Looks like the rel-url was getting copied over and my layout wasn't accounting for that. Decided to extract the url from the image file itself and displayed it in the post.

### Monday, 06. January 2025 11:50PM 
- Added gzip compression to the Caddy Reverse proxy block
- Added WAF rules in cloudflare to block useless bots. 

### Dec 2024

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

### Nov 2024

- [x] Used lonekorean's fantastic [wordpress-export-to-markdown](https://github.com/lonekorean/wordpress-export-to-markdown) tool to convert WP xml to markdown
- [x] learned that the *hugo server* and *hugo build* serve different purposes
- [x] Setup aliases on NUC and Thinkpond to quickly build and publish. Moved the actual publishing workflow to the Thinkpond and retained the main static site on the NUC.
- [x] Fixed permalinks to prevent link rot, almost?
- [x] Fixed RSS feed issues
	- [x] For posts tagged as *micro* set the title to just date+time so that micro.blog picks it up as a note and not display the title. 
- [x] Migrate older posts as deemed fit
- [x] Build a proper archive page. Made some decent progress, thanks to [D'Arcy Norman's](https://darcynorman.net/archives/), pointers [here](https://discourse.gohugo.io/t/listing-all-posts/30575/4) . 
- [x] Build a proper photo gallery
