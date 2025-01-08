---
categories:
- Tech
- Tech
- Tech
coverImage: Screenshot_20200507-041810_Firefox.jpg
date: "2020-05-07"
month: 2020-05
tags:
- evernote-alternative
- trilium-docker
- trilium-notes
title: Migrating over to Trilium notes
year: 2020
---

**_PS: For step-by-step instructions read [this](https://srikanthperinkulam.com/2021/04/06/installing-trilium-notes/) post instead_**

I've had my eyes on [Trilium notes](https://github.com/zadam/trilium) since last year. Having setup a robust docker framework [earlier this year](https://srikanthperinkulam.com/2020/04/24/weeknote-17-covid19-webmentions-and-migrations/), I decided to test Trilium out. Gave it a test run this morning and am way impressed with its' functionalities! With docker, installation was super easy and I am strongly leaning towards using Trilium as my primary note application.

The yml file to get this running on docker (swarm) is in my [github gist](https://gist.github.com/sriperinkulam/60323d29922069887f627ccedc65bad3). You'd obviously need to have docker installed, docker swarm running with the traefik container and the domain mapped as needed. My [Jitsi post](https://srikanthperinkulam.com/2020/04/19/self-hosting-jitsi-video-conferencing/) has this outlined further.

While I haven't spent a fair amount of time diving deep into the setup, here's a quick first impression:

**Pros:**

- Beautiful interface that can be as sparse or as detailed as you'd like it to be
- Encrypted by default and further protected sessions for sensitive notes
- A note-info section that details attributes and link-maps
- Notes can be 'cloned' under multiple places in a tree
- Code scripting, tables, markdown, images, files - It's got it all!
- Web clipper for quick screen and context grabs
- Export and Import functionalities

**Cons:**

- No mobile apps yet! However, it does have a mobile front-end which should be a good alternative
- No multi-user support yet

I was exploring Joplin as an alternative initially but decided to stick with Trilium since the [Joplin app](https://joplinapp.org/) currently has limited functionality (Creating nested trees in the mobile app). Meena's been looking at switching over from her current Evernote setup and I think this might be a terrific replacement for her. Was never really a fan of Evernote and that dislike strengthened further when I had to install the app either on a Mac or PC to export my content! I am so glad we have the strength of open-source to weigh against these silo'ist setups!
