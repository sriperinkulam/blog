---
title: "Colophon"
layout: "now"
url: "/colophon"
summary: Colophon
date: '2025-01-25'
hidemeta: true
rss: false
---
Over time I've incorporated quite a few moving blocks to bring this site to function the way it does. This page is an attempt to document those various facets. See [sitelog](/sitelog) for chronological updates made on this site.

### Publishing workflow

I use the fabulous [Markor app](https://github.com/gsantner/markor) on my phone to draft posts on the go. Syncthing runs in the background to sync posts to my laptop. If the laptop is turned on, HUGO running via docker automatically picks up these new posts, a script builds the site, and then pushes these updates to github. To draft posts on the laptop, I use the [Remarkable app](https://remarkableapp.github.io/linux.html). My templates directory in debian has pre-built templates for long and short articles which I can easily copy over when drafting posts on the laptop.


### Comments

I moved away from [ISSO](https://github.com/isso-comments/isso/) and setup my own custom comments system. Comments when submitted on posts and certain pages, now get pushed to my ntfy.sh server. There's mild spam detection in place. 

At some point I would also like to integrate webmentions and pingbacks. The guts are ready but I haven't seen the push to blend them in yet.

### Garmin

I manually fetch the GPX files and summary from my Garmin account as needed. These are saved in the assets and static folders. If a specific post has front-matter set to point to those filenames, it shows an overlay of the stats on the gpx map. See [this post](https://srikanthperinkulam.com/2025/01/19/la-malinche-hike/) for example. Also a [Garmin](/garmin) page shows the summary of all activities. Could tweak this to show totals for a year etc. which I have not gotten to yet.

### Rewind

I built the [Rewind](/rewind) page to coax me to read my older posts. In every build, this page essentially loads all posts within three days of the current date in the previous years.



