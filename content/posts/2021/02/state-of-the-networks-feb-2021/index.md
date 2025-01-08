---
categories:
- Tech
- Tech
- Site
- Tech
coverImage: Homelab-SoTN-Feb-2021.png
date: "2021-02-05"
tags:
- sotn
title: State of The Networks - Feb 2021
---

_A quick rundown on the state of the home-servers I run or applications I host on the cloud._ _Published while listening to: [Malang](https://invidious.snopyta.org/watch?v=RlcY37n5j9M)_

With our temporary relocation, I currently manage two 'home-labs' - one which I remotely manage with a WireGuard tunnel and the other just a local-access only setup. The remote home-lab is essentially a Nextcloud server running on a [DietPi OS](https://dietpi.com/) spun on an RPi4. I pulled down the HAProxy config on the fronting server since that was no longer required.

![](images/Homelab-SoTN-Feb-2021-600x478.png)

The local home-lab currently encompasses four units:

- [NextcloudPi](https://ownyourbits.com/nextcloudpi/) running on an RPi3 and connected to a 1TB main drive: This has been our primary document and media backup servers silently chugging along for close to three years now!
- [OSMC](https://osmc.tv/) installed on another RPi3: With a 1TB media drive, Amazon video and Youtube addons this primarily serves as a secondary family Television. A bit on the sluggish end but does the job for now.
- DietPi running on an [Odroid-XU4](https://wiki.odroid.com/odroid-xu4/odroid-xu4): Pi-Hole for Ad control and WireGuard to access the remote home-lab.
- [PoPOS](https://pop.system76.com/) running on an Intel NUC7: My primary workstation! An attached 1TB drive acts as the secondary backup for my NC setup and then I run sync jobs to a 256GB flash drive for a cold backup of the really important files.

And then, on a remote VM I run a slew of services that handle most of my social and productivity tools. Fronted by Traefik and running in docker containers, the following services run on the 8GB server:

- [Bookstack](https://www.bookstackapp.com/) – Wiki software which I am currently using to help publish my dad’s second book
- [Known](https://known.srkn.org/) – I mostly use this as a quick bookmarking tool. I also post short updates or status notes here infrequently.
- [Wallabag](https://www.wallabag.it/en) – Read-later app
- [Pixelfed](https://srikanthperinkulam.com/2020/06/14/guyon-flats-and-tuffys-tavern-trail/) – Way better than Instagram and [my go-to space](https://pixel.srkn.org/sriperinkulam) to post individual images
- [Minflux](https://selfoss.aditu.de/) – The light-weight feed-reader that I pipe all my RSS subscriptions to
- [Trilium Notes](https://github.com/zadam/trilium) – A terrific Evernote alternative with awesome Markdown support
- [Signal-CLI](https://github.com/bbernhard/signal-cli-rest-api) – I use this for server trigger notifications to be sent via SMS
- [Etherpad](https://etherpad.org/) – Quick, collaborative notes
- [CryptPad](https://cryptpad.fr/) - Collaboration suite for documents
- Calibre - I use this to manage [my digital books collection](https://lib.srkn.org/)
- Lychee - A nifty photo gallery where I currently save my [digital stamps](https://srikanthperinkulam.com/2020/08/26/stamp-collection-digitized/)
- WordPress – I run 4 instances of WordPress – Portals for folks in my family
- Nextcloud – This one’s more to test the recent releases before I deploy them on my home-lab

Sometime down the lane I would like to setup a [Snikket instance](https://snikket.org/) for family chats.
