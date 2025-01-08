---
categories:
- Site
coverImage: file.png
date: "2017-03-03"
tags:
- digitalocean
- indieweb
- sites
- workflows
title: Migrations, Workflows and Awesomeness
---

Since mid 2016, I've been wanting to consolidate all the portals I manage. Having set them up on separate domain spaces, It was getting excruciatingly difficult to update/maintain/upgrade them. The admin interface at times was dead slow and I had restrictions with server permissions which wasn't quite helpful. My first thought was to procure a home server and host all the portals from there. Besides speed and control, It would also give me flexibility to tinker with other self-hosted apps that I've been itching to work on. It looked like a great solution but I knew it would also need me to invest a lot of time, getting up to speed with server administration. With my new [running schedule](https://srikanthperinkulam.com/category/channel/training/) and several other things, time was a luxury I didn't have and I was soon scouting for alternatives.

<!--more-->

I figured the 'cloud' was a good alternative. While debating between AWS and Azure I came across [DigitalOcean](https://www.digitalocean.com/) \[DO\] which seemed to be a great testing ground for Cloud services. It seemed to have all that I was looking for and apparently was also pretty easy to setup. Besides, with another service called [Serverpilot.io](https://serverpilot.io/) I could spin a portal with just a few clicks. Sometime late in December when one of my shared servers expired, I bit the bullet and signed up with DO. It's been pretty stable and worry-free so far. I see a tremendous improvement in speed, and goes without saying, the flexibility is incredible. As an added bonus, I also got to port to https using [LetsEncrypt](https://letsencrypt.org/). Something that I sub-consciously wanted to do for a long time now. Couldn't have asked for more! Over the next few weeks, as other shared accounts expire, I plan to migrate all of my other websites over to DO. It's been a fun ride and a huge learning experience.

In the process I also came across a few nifty tools that do incredible things. The [All-in-one WP Migration](https://wordpress.org/plugins/all-in-one-wp-migration/) plugin does wonders in migration. All you need to do is install it in your old server setup, download the export and then import that into your brand new wordpress setup. This plugin takes care of EVERYTHING - posts, pages, CPTs, database, media and what not! It takes me just a minute to migrate my whole setup! Amazing! On another front, I've been itching to find a tool to publish to my site directly from my phone. The wordpress app worked just fine but didn't quite meet all my needs. And then one day, I chanced upon a neat workaround using the [workflow](https://workflow.is/) app on my iphone. One of those days when I wasn't quite in the mood for podcasts, I used the 20 minute train commute to build some custom workflows. Soon I could push updates to my site - be it bookmarks, moments, quick notes, replies, running updates etc which seamlessly get posted with just a few clicks. Once these 'posts' enter my website, I use a couple of plugins to add featured images ([Quick featured images](https://wordpress.org/plugins/quick-featured-images/)) and/or auto post to twitter using [SNAP](https://wordpress.org/plugins/social-networks-auto-poster-facebook-twitter-g/). Some thought behind this was also to live the [indieweb philosophy](https://indieweb.org/Principles).

![](images/file-169x300.png)

Ever since I started training for the 50 miler, I seem to have developed a better approach to time-management. During the week I keep note of all the tasks I would like to work on, prioritize them and then only work on the finishing the top three. This way I spend at-most half an hour during the weekend on server admin tasks and weed out the one's with lower priority. This approach leads to having several want-to but unfinished tasks on the list. However, I guess it's the best in terms of distributing time across the [buckets](https://srikanthperinkulam.com/2016/11/11/non-negotiable-milers/).
