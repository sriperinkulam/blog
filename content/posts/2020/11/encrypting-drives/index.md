---
categories:
- Tech
- Tech
coverImage: 20201017_100233.jpg
date: "2020-11-01"
month: 2020-11
tags:
- badblocks
- seagate
- smart-test
title: Encrypting drives
year: 2020
---

Earlier last week one of my external hard-disks went kaput. Though it's fair to assume the recent travel could have led to this, my guess is that it was just a case of an ill-fated drive. While I did lose all the data on that drive, I thankfully had duplicate copies of the over 200GB data on other drives or machines. This is the first time that I'm losing a hard-drive and I'm so glad I was prudent enough to have multiple copies. All thanks to the folks over at Backblaze who frequently [publish hard-drive failure statistics](https://www.backblaze.com/blog/category/cloud-storage/hard-drive-stats/) on their stock!

![](images/20201017_100233-1200x1200.jpg)

Now, losing that data got me thinking if I was really wise in just storing that data naked without any encryption. If I did want to claim the warranty on the drive, I will have to send over the hard-drive to Seagate. I am just not comfortable sending it over now since technically, most if not all of it, can be forensically retrieved. On that thought while researching on possible encryption tools, I landed on [VeraCrypt](https://www.veracrypt.fr/). I instantly formatted my backup drives, setup an encrypted container and pointed my selfhosted Nextcloud installation to that virtual 'drive'. The initial formatting does take time since VeraCrypt replaces data bit-by-bit and creates a clean slate. Once that is done, decrypting the data is just a matter of seconds. While at it, I also subjected all my other hard-drives to [SMART](https://en.wikipedia.org/wiki/S.M.A.R.T.) tests and [badblock](https://en.wikipedia.org/wiki/Badblocks) tests to make sure they were following suit!

It's been about two weeks and I am super impressed with the ease and functionality of Veracrypt. It definitely is an additional step in the workflow. However, as they say - Privacy comes at a cost and I am willing to go that extra mile for an overall peace of mind.
