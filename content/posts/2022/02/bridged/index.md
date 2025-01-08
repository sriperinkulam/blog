---
categories:
- Tech
- Tech
date: "2022-02-20"
tags:
- bridge
- matrix
- whatsapp
title: Bridged
---

After a good [one year away](https://srikanthperinkulam.com/2021/01/10/digital-reset/) from Whatsapp, I'm back on it . This time however, on better terms.  All thanks to the [Mautrix bridge](https://maunium.net/go/mautrix-whatsapp/) and the [Matrix protocol](https://matrix.org/faq/#what-is-matrix%3F).  Essentially, I can access my whatsapp account data on my regular phone or desktop using [Elements' pretty robust app](https://element.io/get-started) system. Note that the whatsapp app however is either running on a Virtual Machine or in my case an old phone fronted with a VPN. Since whatsapp only needs the primary phone to connect with their servers once every two weeks, it's pretty much just sitting there turned off while all the group and individual messages show up on the bridged element app.

There's tremendous benefit to this approach:

- The metadata that whatsapp is known to generously absorb from your ecosystem is heavily **reduced**
- You still get to stay in touch with folks who're pure lazy to install another communications app
- You get to be in the ecosystem and nudge people out
- This works not just with Whatsapp, but telegram, iMessage, FB messenger and other messaging apps.

Setting this up took me barely 30 minutes - thanks to this exceptionally well documented [ansible playbook](https://github.com/spantaleev/matrix-docker-ansible-deploy/) . Sounds and reads terse but it is super straightforward to follow through. At this point, calls are not bridged. It otherwise works absolutely seamless. Not quite sure how long I'd use this. It started off more from the perspective of testing out matrix and the surrounding ecosystem and it's been a fun ride so far.

Walk over that bridge. Will ya? Now, if you do not want to set this all up yourselves, you could for a small price, use the service provided by either [element](https://element.io/element-one) or [Beeper](https://www.beeper.com/) . I think they offer it at at a fantastic price-point.
