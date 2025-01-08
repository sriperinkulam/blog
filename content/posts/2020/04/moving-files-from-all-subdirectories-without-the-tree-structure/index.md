---
categories:
- Tech
- Tech
- Tech
date: "2020-04-19"
month: 2020-04
title: Moving files from all subdirectories without the tree structure
year: 2020
---

Appa, who's very active on Facebook, recently wanted an easy way to sift through his old videos and photos that were up on his account. I decided to take a dump of his data from the network using the [download your information](https://www.facebook.com/dyi/) section. I initiated the process with just a few clicks and after a few days, I was able to download the zipped files of all the content he had posted on FB. including the likes, messages, shares etc. If you haven't already, I would strongly recommend you get a copy of your data. I rarely interact on Facebook these days so it was even more interesting to see all the information they collect on you.

Anyways, once I had the zipped files, I wanted to sift through the folder structure and copy over all the media from it to a specific location. Using a combination of the tree and find commands this was pretty straightforward. Logging them here for later reference:

_List files with tree hierarchy:_

`tree`

_Find all files within the current directory and nested sub-directories and move them to specific folder:_

`find . -print -name "*_.*_" -type f -exec mv -n {} /path/to/destination/directory/ \;`

Once I had the files \[Totally about 25Gb\], I realised I had to move them over to my dad's machine. Good old [Syncthing](https://syncthing.net/) came to use here to send over the files.
