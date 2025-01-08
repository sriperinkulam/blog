---
categories:
- Tech
- Site
- Tech
coverImage: 20190226_143422.jpg
date: "2019-02-26"
tags:
- chatter
- diet-pi
- odroid-xu4
- raspberry-pi3
- yunohost
title: Bringing the cloud home
---

I finally got my Shoebox server setup working! I now have three Single board Computer \[SBC\] working in tandem behind my home router to accomplish what I've been wanting to do for quite sometime now - Setting up an easy-to-maintain, in-house server for all my data and web hosting needs. Fixing this all together has been a tremendous learning experience. I still need to weed out some pesky issues but I believe I have the bearing right now.

Here's my current setup:

1. [NexcloudPi](https://ownyourbits.com/nextcloudpi/) installed on a [Raspberry pi 3B+](https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/) board
2. [Yunohost](https://yunohost.org/#/) installed on an [Odroid XU4](https://www.hardkernel.com/shop/odroid-xu4-special-price/) board
3. [Diet-Pi](https://dietpi.com/) installed on another Raspberry pi 3B+ board

I've been using Nextcloud as my data storage solution for more than a year now. It does what I expect it to do and much more. NextcloudPi handles the intricate details and takes out the hassles that come with hosting data on personal servers.

On the ODroid-XU4, I installed debian stretch as the base OS and then manually installed Yunohost as my web server. I use ServerPilot on my Digital ocean servers and was looking for a close match while self hosting. Love YHs web-ui and they did seem to support quite a few web apps. I also have my eyes on [cozy](https://docs.cozy.io/en/tutorials/selfhost-debian/) and [caprover](https://caprover.com/). Might explore these at a later point in time if decide to switch to a different SBC.

Both NextcloudPi and Yunohost have letsencrypt tools to setup and manage certificates for the domains/sub domains. While super useful, I realised to benefit from that feature, I had to rely on haproxy. With some [pointers from the Nextcloud forum](https://help.nextcloud.com/t/accessing-nextcloudpi-behind-haproxy/47489), I decided to use another pi to front as the main server. Installed Diet-pi on it since it's just something I really liked and configured haproxy on it to map to the corresponding server based on the hostname. While at it, I also added in a switch between the router and various servers.

I still need to work on making this more robust. One niggling issue is the speed is heavily compromised. I'm guessing it's do with my haproxy config and I should be able to fix it pretty soon. Once I have this sorted out, I need to spend some time hardening the security of the server, further configure Yunohost, device my backup strategies and finally moving my websites over from Digital Ocean.
