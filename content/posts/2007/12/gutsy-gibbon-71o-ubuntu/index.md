---
categories:
- Tech
date: "2007-12-22"
title: Gutsy Gibbon 7.1O - Ubuntu
---

Finally, Installed Gutsy on my system today! :-)After failed attempts to install it last weekend, I was a bit apprehensive this time. But today, two minutes into the install I realized where I was faltering. I'd created four partitions on my Hard disk of 30 Gigs each for Windows. Fiesty was running on the remaining 40Gigs. Last week during the installation I'd configured the setup to create a Primary ext3 partition instead of making it a logical one.That was what was leading the setup to freeze! Surprisingly I was never warned during the initial stages. Anyways, I fortunately happened to notice the goof up this time and then the rest of the Installation was a breeze! Flat 10 minutes and I had Gutsy live and kicking! :-)

The first thing I'd looked for after logging in was to check out the classy desktop effects that Gutsy comes bundled with. But to my dismay the OS threw up messages telling me Advanced Desktop effects could not be configured. It didn't even specify the cause. A bit of Googling brought out the hidden mite - My Hardware settings were blacklisted since it couldn't support both video rendering and classy desktop effects at the same time. But then I just wanted to find a workaround to get things working. Finally I happened to find one in the Ubuntu Forums itself. All I had to do was to deactivate the Hardware config. check that Compiz by default does when initiated. This could be done by running the following command in the terminal.

mkdir -p ~/.config/compiz/ && echo SKIP\_CHECKS=yes >> ~/.config/compiz/compiz-manager

Once that roadblock had been dealt with I only had to install the Gnome Compiz manager through the Synaptic package manager. Synaptic installs are cakewalks. All relevant dependencies get installed and broken installations are pretty rare. Installation of the Compiz manager led to the creation of a Preferences tab in the Advanced Desktop settings. This is where real FUN starts. A bit of tweaking and you have your desktop at your whims! I'll probably let the pictures do the talking!

_The Workaround explicitly mentions that crashes are prone to occur if both video and Advanced Desktop settings are run at the same time. So keep in mind to get back to the default settings when you plan to watch videos on your Gutsy._ _A pain but still worth it!_ :-)

There's still a lot more to explore ( or should i say exploit :-) ) . Will get back if I happen to find something interesting!
