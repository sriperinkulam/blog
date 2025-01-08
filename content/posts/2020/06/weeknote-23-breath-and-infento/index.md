---
categories:
- Week-notes
date: "2020-06-06"
month: 2020-06
title: Weeknote 23 - Breath and Infento
year: 2020
---

_A glimpse of the past week and the few things that captivated my attention:_

[David](https://distanceathletics.com/trainer/david-bidler/) offered us a complementary sign-in to his [Breathing Workshop](https://breathetoperform.mykajabi.com/catchyourbreath). Excited to get that rolling! He's also released his first book - [Breathe to Perform](https://www.thebreathetoperformprogram.com/). Can't wait to get our hands on it!

Over the last week, I've been strongly considering moving over from WordPress to a static site generator. I've been using WordPress for 15 or so years now and have had absolutely no issues. The minimalism factor of static site generators makes it quite appealing though and then there's that constant nudge to try something new. Will have to weight that against the migration work involved and take a call.

I recently bought a 2TB Seagate drive and connected it to my 'Mothership' laptop. I split it into two partitions - one acts as the secondary backup of the files I save on my RPi+WD1TB drive and the other for files I do not necessarily need on NC. While at it, I also setup an rsync pull from my Hetzner Cloud server to backup my docker volumes. Keeping the backups manual for now.

```text-plain
sudo rsync -nchavzP --delete --stats user@xxx.xxx.xxx.xxx:/path/to/docker/volumes/ 
"/media/Drive/partition2/Hetzner Backup/"
```

Quite a few interesting developments since I sent in a blurb to the TFI alumni group. I've expanded my '[services](https://srikanthperinkulam.com/services/)' a bit more now and I see it as a way of contributing to the educational ecosystem back in India.

Meena suggested I build a bike for Shasta. I was initially looking at building a no-nonsense mobile platform - just a plank on three wheels and a pedal. While looking at options though, I chanced upon Infento. Looked very promising and loved the modular aspect of it. So we went ahead and ordered the [Infento Explorer kit](https://www.infento.com/product/explorer-kit/). Should be delivered sometime today!

The US is going through some real dark times now. We've not even come out of the pandemic (which we grossly mismanaged). It feels like we're back to square one and it doesn't have to be like this! What is it that drives humans to these abysmal depths?

**Currently Reading**

I've finally gotten back to reading books! With so many things on the to-do list, reading in the past did take a back-seat.

- The adventurer's son - A memoir by Dial and Roman
- The Wedge by Scott Carney
- The Art of Invisibility by Kevin Mitnick
- LikeWar – The Weaponization of Social Media by Emerson T. Brooking, P.W. Singer
- The Art of Thinking Clearly by Rolf Dobelli
- Click Here to Kill Everybody by Bruce Schneier

**Interesting podcasts this week:**

Started listening to '[Passenger List](https://srikanthperinkulam.com/book-review/the-wedge/)'. Atlantic Flight 702

https://dts.podtrac.com/redirect.mp3/dovetail.prxu.org/232/2005da8d-34e6-4b1b-bb0b-d9f34a6e8f77/PL\_PREVIEW\_V1\_COMING\_SEP\_JOHN\_NEW\_VERSION\_PREMIERES\_SUBSCRIBE\_NOW\_1\_.mp3

 

**Interesting reads this week:**

[US investment in Next-gen nuclear power](https://bag.srkn.org/share/5ec5a10cab73c1.22768810): From most perspectives, this makes sense. Would be interesting to see the developments as other countries catch-up!

[Yoga with Adriene](https://bag.srkn.org/share/5ec5a7ceb47e30.28806443): This one's mostly for Meena!

[Does Birth order affect personality](https://bag.srkn.org/share/5ece30eca48b19.17551407): As a fourth in the birth order, I did find this quite interesting.

[Pelorus Jack](https://en.m.wikipedia.org/wiki/Pelorus_Jack): The dolphin that guided ships across the French canal. Also the first individual sea creature protected by law in any country!
