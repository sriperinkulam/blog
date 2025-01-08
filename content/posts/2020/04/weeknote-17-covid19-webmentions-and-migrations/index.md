---
categories:
- Tech
- Site
- Tech
- Week-notes
coverImage: Screenshot_20200427-041015_WhatsApp.jpg
date: "2020-04-24"
month: 2020-04
title: Weeknote 17 - Covid19, Webmentions and Migrations
year: 2020
---

_A glimpse of the past week and the few articles, podcasts, tools, videos and music that captivated my attention:_

This week I got a better handle at deploying and maintaining docker images. With that squared out, I decided to decommission the Digital Ocean servers that I had setup [back in 2017](https://srikanthperinkulam.com/2017/03/02/migrations-workflows/) and migrate the applications over to my Hetzner server. I no longer have to rely on ServerPilot. All my applications are now deployed as docker containers fronted by #Traefik as a reverse proxy.

The jitsi server instance I [deployed last week](https://srikanthperinkulam.com/2020/04/19/self-hosting-jitsi-video-conferencing/) has been serving pretty well so far! I tweaked it further to enable [local recording](https://blog.radiumz.org/en/article/local-recording-jitsi-meet). Meena has been using it to run her online Yoga sessions and she can now also use it to record the podcast that she soon plans to start! Session recording and live-streaming is something I still need to configure in my current setup. The logs indicate it's failing on the Jibri handshake and that's something I'll need to figure out once I have a bit more time in hand.

Other actionable tasks on the tech front include figuring out a swift way to deploy PHP based applications on Docker. I still need to port over my Known and [PixelFed](https://pixel.srkn.org/sriperinkulam) applications.

Last week, [Philip](http://www.philipbrewer.net/) nudged me to look into my webmentions. The theme I previously had wasn't displaying them as comments. I needed a bit of a 'creativity boost' and decided to use a new theme. Really liked the McLuhan theme by [Anders Noren](https://www.andersnoren.se/teman/mcluhan-wordpress-theme/) and decided to give it a spin. Noticed [a minor issue with the comments section](https://wordpress.org/support/topic/mcluhan-comments-fetched-are-from-a-different-post/#new-topic-0) and was easily able to fix it. I do however want to make a few tweaks to it, which I hopefully will get around attending to over the next few weeks. I also have my eye on [Prateek](https://prtksxna.com/)'s [Zuari theme](https://wordpress.org/themes/zuari/) which is deeply [indieweb](https://indieweb.org/) compliant.

Last evening, [Atchuth](https://atchuth.wordpress.com/) mentioned he's now using his RPi4 as a full fledged desktop machine. He's moved over from DietPi to the Raspbian OS. Makes sense given his current use-case. Sharath on the other hand is still using his RPi 4 predominantly as a Nextcloud server.

This week has been great in terms of re-connecting with some good old friends! We're planning a re-union sometime next year. 20 year since we finished school! Phew!

The Khat-pat makers group that I am part of is now getting more traction and it's awesome just hearing out the cool things that other folks are doing. This week's session was on building drones from scratch!

I also got around connecting with the kids I taught 10 years ago! They've all moved on to college and are into various things now. One kid wanted to become a stellar teacher and this  is one of the best messages I've received so far!

Last night we played a few good rounds of Pictionary/Dumb-charades with the kids. Shasta had a terrific time just watching the 'adults' in their elements. You never get too old for this game!

**Interesting podcasts this week**

Picturing Data: Monocle

https://monocle.com/extensions/monocle/bin/mp3\_downloader.php?file=https://api.soundcloud.com/tracks/788260468/download/&filename=monocle\_on\_design\_442.mp3

**Interesting tools this week**

The [Termux app](https://termux.com/) has been an amazing value-add to my phone for those quick server check-in's!

**Interesting reads this week**

[‘We can’t go back to normal’: How will coronavirus change the world?](https://outline.com/agNcAx): 2020 will be etched in the memories of most people living today as one that drastically changed how we as humans functioned. As Covid19 spreads across various countries, it's influencing and compelling dire actions. What was considered to be impossible at various level, is now just a quick decision point - Financial stimulus, vaccine production, remote work and schooling to name a prominent few. As we build resistance to the virus as a society and consequently as the adrenaline that's currently rampant drains out, we're going to see the fallout's of our actions or several inaction's thereof. Assuming another event of this magnitude does not occur over the next decade, the world is going to need a major overhaul to recover from the pandemic.

[Beginner's guide to PGP](https://bag.srkn.org/share/5ea2f0cbab1fa1.31532716): A simple and easy read on PGP with actionable guidance for non-tech folks out there. It's given that over the next few months most countries are going to erode into the privacy of its citizens. Policies that are brought into effect now for surveillance and tracing will overarchingly become the norm and will be almost impossible to retract. It's critical that we act now to safeguard what little privacy we can. It's never been about - 'There's nothing that I have to hide.' Ignorance can and will heavily be mis-appropriated for someone else's benefit.

[Why one Neuroscientist started blasting his core](https://bag.srkn.org/share/5e9ecbae16ccb0.15652872): Neural pathways, stress control systems and of course the adrenal medula. Yet another fascinating read on how amazing the human body is!

[How Saudi Arabia's religious project transformed Indonesia](https://bag.srkn.org/share/5ea68cce89b171.88947262): Religion, politics and power are so damned intertwined. If anything, its one of those defining necessities and vices of humanity.

[It's time to build](https://bag.srkn.org/share/5ea68e112d5251.85133599): So beautifully phrased! It's high time we dusted those tarp sheets and get to build from ground-up. Over time we've become complacent as a society and we need one strong re-boot!
