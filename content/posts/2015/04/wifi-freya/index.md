---
categories:
- Tech
date: "2015-04-17"
tags:
- elementary-os-wifi
- enable-wifi
- freya-wifi
- hard-and-soft-blocks
- rfkill
- rfkill-wifi
- ubuntu-wifi
- wifi-and-bluetooth
- wifi-disabled
- wifi-softblocked
title: Enabling WiFi from the terminal
---

After a few rough beta installs of the OS, I decided to do a clean install of  [Freya](http://elementary.io/). It's been a smooth sail so far but for the intermittent WiFi disconnects. For some reason the WiFi gets soft disabled at times. Until I figure out what's causing this to happen and for future reference here's a nifty work-around:

- Determine the current state of the radio transmitters using [rfkill](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Power_Management_Guide/RFKill.html). You'll be able to see immediately If any of your devices are soft blocked.

> \[code\] $ sudo rfkill list all \[/code\]

- Unblock radio transmitters as needed. In my case, something was turning the Wi-Fi off. I just had to turn this on using the below command:

> \[code\] $ rfkill unblock wifi \[/code\]

Note: In a few laptops the Wi-Fi  key is also mapped to the Bluetooth function, so to activate or deactivate you'll just have to tap a few times to disable or enable wifi and/or bluetooth.
