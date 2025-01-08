---
categories:
- Tech
- Tech
- Tech
- Site
- Tech
coverImage: State-of-the-Network-Jun-2020--scaled.jpg
date: "2020-06-18"
month: 2020-06
tags:
- sotn
title: State of The Networks – Jun 2020
year: 2020
---

_A quick rundown on the state of the home-servers I run or applications I host on the cloud._

My 'Homelab' setup has not changed much since my [last update in January](https://srikanthperinkulam.com/2020/02/04/state-of-the-networks-jan-2020/). I did add in a [switch](https://srikanthperinkulam.com/2020/05/17/switched/) and installed a wireguard vpn on the RPI 3B+ that fronts as a reverse proxy for the Nextcloud media devices. I also got a Seagate 2TB drive and built two partitions into it. One acts as a backup for my Nextcloud files and the other is a 'cold backup' of my Hetzner cloud instance.

![](images/State-of-the-Network-Jun-2020--1200x977.jpg)

For personal use, I maintain two remote cloud servers on Hetzner:

**Hetzner 01**:

The first server essentially handles most of my social and productivity tools. Fronted by Traefik and running in docker containers, the following services run on the 8GB server:

- [Bookstack](https://www.bookstackapp.com/) - Wiki software which I am currently using to help publish my dad's second book
- [Known](https://known.srkn.org/) - FB alternative. I mostly use this as a quick bookmarking tool. I also post short updates or status notes here infrequently.
- Wordpress  - I run 4 instances of Wordpress - Portals for folks in my family.
- [Wallabag](https://www.wallabag.it/en) - Read-later app
- [Pixelfed](https://srikanthperinkulam.com/2020/06/14/guyon-flats-and-tuffys-tavern-trail/) - My go-to space to post individual images.
- [Selfoss](https://selfoss.aditu.de/) - The light-weight feed-reader that I pipe all my RSS subscriptions to.
- Nextcloud - This one's more to test the recent releases before I deploy them on my homelab.
- [Trilium Notes](https://github.com/zadam/trilium) - My go-to place to save quick notes
- [Signal-CLI](https://github.com/bbernhard/signal-cli-rest-api) - I use this for server trigger notifications to be sent via SMS
- Mattermost - Slack alternative
- Etherpad - Quick, collaborative notes

**Hetzner 02:**

This server hosts my Matrix and Jitsi Conference applications. While at it, I also have a Riot instance running in parallel that fronts the Synapse install.
