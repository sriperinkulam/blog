---
categories:
- Micro
- Tech
date: "2017-05-04"
title: Centralized publishing
---

Early in 2017, I consciously decided to consolidate all my social accounts and use my website as the main 'vehicle' for online interactions. While exploring options, I chanced upon the [Indieweb philosop](https://indieweb.org/principles)y which seemed to resonate quite a lot with my thoughts. Over the next few weeks I started taking steps to eventually migrate my publishing platform to a more robust framework. Below is a rough outline of what I have in place so far. I'll try to keep this article live with updates as I work on enhancements.

**Core framework:**

This website is built with Wordpress and is currently hosted on [DigitalOcean](https://www.digitalocean.com/) \[DO\] fired-up by [ServerPilot.](https://serverpilot.io/) I upgraded to DO early in 2017 from a shared server and I'm enjoying the tremendous benefits that comes with it. More on that is [here](https://srikanthperinkulam.com/2017/03/02/migrations-workflows/).

 **Interaction with Silos:**

While I'm not quite an online dweller on social networks, I do post once a while on Instagram, Twitter and Facebook. Over the last few years, I've syndicated my posts to these networks on and off using various plugins. But none of those had features to fetch the interactions or responses back to my portal. Something that I really 'craved' for. While looking for better alternatives, I chanced upon the concept of [webmentions](https://indieweb.org/Webmention). Meandering through the gamut of options, I eventually found a few tweaks that would work best for my publishing workflow.

The first step was to get my wordpress install talk indieweb. The [WP starter](https://indieweb.org/WordPress) page and the [Advanced WP setup](https://indieweb.org/Advanced_WordPress_Set_Up) page on the Indieweb wiki were good places to get the wheels rolling and setup a base framework. Since I predominantly publish or draft articles while commuting, I was exploring options to post from a mobile device (iPhone). I lost my trust on the official wordpress app after it lost a couple of my drafts. And then I chanced upon [Workflow](http://workflow.is/) which looked reliable and seemed to fit all my needs. Outlined below is a rough note on how I interact with the three silos using the workflow app on my iPhone and some custom functions in my WP install.

The general idea was to collect, process and publish. Based on the desired action (Post a status or activity update, Bookmark a link, Reply to a post and Publish a photo) I designed workflows to process the information and push it over to the Wordpress action. One minor issue was that the [post-kinds plugin](https://wordpress.org/plugins/indieweb-post-kinds/) sets up and uses a wordpress taxonomy called 'kind' to hand-shake with the [micropub](https://indieweb.org/Micropub) server. Since the WP action in Workflow did not accept entries for taxonomies, I had to create a 'latch' to identify the posts that I create via my workflows and map them to the corresponding 'kind' taxonomy. A few trials and I figured I could use a 'custom field' in the workflow app with some custom code in my functions plugin to map this out for me. The other minor tweak was to make my posts [microformat](http://microformats.org/) compliant for the webmentions to work their magic. To get this working all I had to do was to feed the [requisite html](https://brid.gy/about#webmentions) corresponding to that specific action into markdown just before passing it to the wordpress action in workflow.  Once that was done posting from my phone became a lot more easier (and fun!).

I chose to rely on a couple of slick plugins to post to the silos. [SNAP](https://wordpress.org/plugins/social-networks-auto-poster-facebook-twitter-g/) helps me push notes out to twitter and I use a tag 'trigger' in my workflow to decide which posts I do not want publish on to twitter. I also use some custom code to add [webactions](https://indieweb.org/webactions) to my twitter specific posts.  And then followed [Chris Aldrich's](http://boffosocko.com/2017/04/15/mentions-from-twitter-to-my-website/) tweak to collect twitter mentions on a [specific page](https://srikanthperinkulam.com/knocks/). To handle Instagram, I use the [Dsgnwrks Instagram Importer](https://wordpress.org/plugins/dsgnwrks-instagram-importer/) to consume photos (and their reactions). [Ownyourgram](https://ownyourgram.com/) for some reason wasn't pushing photos to my server.

**Intents and desires:**

While the current publishing workflow works like a charm, I do need to do a few more tweaks to make this a more seamless process. Few things to note in no particular order:

- 'Sync' desktop and mobile workflows. Currently I've different workflows while posting from these platforms. I use the Indieweb Pressthis bookmarklet while on the desktop and the 'workflow' app while posting from my iPhone.
- Design a platform independent workflow. With workflow's recent [acquisition by apple](https://techcrunch.com/2017/03/22/apple-has-acquired-workflow-a-powerful-automation-tool-for-ipad-and-iphone/), I'm skeptical of the outcome and need to come up with something that's more resilient. Shouldn't be dang difficult to spin a quick PWA or tweak some of the [nifty tools](https://indieweb.org/Micropub/Clients) that folks have already built.
- Make my PeriRSS feed reader 'talk' to my portal. Basically enhance it with webactions.
- Talk better with microformats.
- Publish my code / workflows so others can easily tweak or adapt them for their use.

[like](https://twitter.com/intent/favorite?tweet_id=859951821950943232) [reply](https://twitter.com/intent/tweet?tweet_id=859951821950943232) [repost](https://twitter.com/intent/retweet?tweet_id=859951821950943232)

[like](https://twitter.com/intent/favorite?tweet_id=859951821950943232) [reply](https://twitter.com/intent/tweet?tweet_id=859951821950943232) [repost](https://twitter.com/intent/retweet?tweet_id=859951821950943232)
