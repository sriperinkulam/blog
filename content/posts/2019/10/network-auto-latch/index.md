---
categories:
- Tech
- Site
date: "2019-10-25"
tags:
- network
- nextcloud
title: Network auto-latch
---

I realised the raspberry pi that hosts my [nextcloud setup](https://srikanthperinkulam.com/?s=nextcloud) wasn't quite latching back on to the network if the router was turned off or if the internet was sketchy. Was a pain to hard boot the device manually to reset it. Decided to write a short script to reset the network connection when it noticed something was off.

```

ping -c4 192.168.0.1 > /dev/null
if [ $? != 0 ] 
then
  echo "SOS..Restarting eth0 for network latch"
  /sbin/ifdown 'eth0'
  sleep 5
  /sbin/ifup --force 'eth0'
fi
```

A chron job runs every 10 minutes to take pulse of the network, runs the above code and picks up connectivity without manual intervention!
