---
categories:
- Tech
date: "2007-08-26"
title: 'Ubuntu: BSNL Broadband Connection'
---

Holla...

My first post typed in from Ubuntu with it hooked to the net!!!

Just managed to configure the Broadband connection in Ubuntu!! Am on cloud nine, given the fact that I'd been struggling in vain for the past few months to get a few Linux flavours hooked on to the net. Believe me, There couldn't be anything else that's as simple as this!!

Here's the trick ( if at all it could be called that!) for those novices ( obviously like me! ) who haven't yet had luck configuring their systems.

1> Switch off your modem

2>Open the Network settings Dialog box ( System> Administration> Network)

3>Select 'Wired Connection' and click on the Properties.

4> In the 'Connection Settings' Menu select 'Static IP ' type in the following values and save:

IP Address : 192.168.1.2

/\* Assigning the Ethernet Card an IP different from that of the modem\*/

Subnet Mask: 255.255.255.0

/\* No idea why this value is always this :-) \*/

Gateway address: 192.168.1.1

/\* The Modem is being made the default gateway\*/

5>Switch on the Modem and wait for a few minutes for the values to get recorded.

6>In the Terminal ( Applications>Accessories> Terminal) type 'sudo pppoeconf'

6>A window pops with a blue screen notifying that an ethernet device has been found. Just follow the on screen instructions till you reach the screen which asks you for your BSNL UID and PASS. Ping in the values (after deleting the text Username from the line) and you're done!! :-)

I've still got to figure out how to disconnect from the n/w though that shouldn't be a big issue.....

**\[Update: 22-Oct-09\]**

Just type the following commands in the terminal:

> sudo ifconfig eth0 192.168.1.2 netmask 255.255.255.0 up

> sudo route add default gw 192.168.1.1 eth0

This could also do the trick.
