---
categories:
- Tech
- Tech
- Tech
- Week-notes
date: "2020-05-10"
month: 2020-05
tags:
- fasting
- selfoss
- trilium
title: Weeknote 19 - feeds and sessions
year: 2020
---

_A glimpse of the past week and the few things that captivated my attention:_

Weather's been pretty erratic this week. We also had a mild dusting yesterday out of the blue! Might consider heading out for a hike later today.

I nudged Meena to write more. We've had some interesting discussions on Yoga and other things over the past week and I do think she has a ton to share! She's also planning to train for a 50miler which I am super excited about! Oh and beyond all that marketing ploy, Happy Mothers' day.

Shasta's talking a lot more now. Pretty sure her verbal diarrhea is soon going to start soon too!  The other day, while sitting with Appa she said something to the effect of 'i-pae' pointing to the ipad. Grandfather and daughter are totally connecting on these gadgets!

Git: I agree on many levels with [what Kev posted recently](https://kevq.uk/confession-i-have-no-idea-how-to-use-git/) about Github. I enjoy working on and deploying software tools. What I do not enjoy is the whole git pull, push, fork thing!

Sessions: I am running a session later this week for the Khat-pat folks on self hosting. Planning to keep it mostly hands-on and crisp. The idea is to get them started on taking better control of their presence on the interwebs! I'd also love to join the Indieweb folks one of these days. They have [one coming up on the 20th](https://events.indieweb.org/2020/05/online-indieweb-meetup-nyc-vkY32vBfCTEJ)!

Tools: Earlier this week, I came across e-mail cloaking services - [Simplelogin](https://simplelogin.io/) and [Anondaddy](https://anonaddy.com/). Love the idea and I might give them a shot the next time I subscribe or sign-up for a service.

Feed Readers: Over the past few years, I've used multiple feed readers - Netvibes, TheOldReader, FreshRSS and Fever. They were all good in specific aspects but I didn't really find them to be that one tool which I could use to consume the inter-webs my way. Earlier this week I decided to self-host one and narrowed down to FreshRSS, miniflux and selfoss. After a few iterations of deploying and testing, I stuck with [selfoss](https://selfoss.aditu.de/). It's super light-weight and has all the specific features I was looking for.  To deploy it on docker, I used the [boiler-plate template that I created earlier](https://srikanthperinkulam.com/2020/04/28/deploying-known-on-a-docker-stack/) when setting up my [known](https://known.srkn.org) instance.  The gist file for the docker-compose is [here](https://gist.github.com/sriperinkulam/bf31682e6d9805ac29d6e4ff02bacb28). The install should take you at most 10 minutes assuming you have the base framework setup. What I do love about selfoss is the ability to push articles over to my [wallabag](https://bag.srkn.org/) instance.

Trilium: I've moved most of my notes over to Trilium and I am absolutely loving it! While it's hierarchical, it is also setup [not to be one](https://github.com/zadam/trilium/wiki/Patterns-of-personal-knowledge-base).

**Interesting reads this week:**

[Time-restricted eating](https://bag.srkn.org/share/5eb322c0461ff3.59682906): Philip [referenced this article recently](https://www.philipbrewer.net/2020/05/03/experiments-with-time-restricted-eating/) and I think it's brilliant! Also went ahead and signed up for Rhonda's podcast.

[Tracking using ultrasound frequencies](https://bag.srkn.org/share/5eb705c2235124.51234929): Whoa! This totally blew my mind! If google uses it to connect your devices with chrome cast, what's really stopping them from using it to track what you are watching? And now how do you block that invasion?

[Workplaces in the era](https://bag.srkn.org/share/5eb6f8cbd8a783.67620597): Firms will have additional pressure from (or will be incentivised by) their insurance companies to have monitoring in place. Over the span of few months, this will be the new normal. Looking back, haven't we all got used to keying-in and out at our workplaces?

[We kill people based on metadata](https://bag.srkn.org/share/5eb700e76826f2.47966883): Quite a lot is changed since 2014. What hasn't though is how fragmented and withdrawn several government and private entities are even in times of crisis.

[The mystic veil of End-to-End encryption](https://bag.srkn.org/share/5eb7034fba3519.79379071): Interesting read on the data sharing between these apps.  The other day I was wondering how [Bark](https://www.bark.us/)'s able to access messages from these apps. Likely they have something on these lines drifting underneath? While I love the concept of the app and the benefits it provides, I did cringe and walk away because I just wasn't sure how they'd be handling the data.
