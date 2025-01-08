---
categories:
- Tech
date: "2020-05-17"
month: 2020-05
title: Optimizing images
year: 2020
---

My Samsung phone by default generates pretty high resolution pictures. Even with the most basic setting, captured images turn out to be ~3MB! I'm not a huge photo buff and don't necessarily need such high clarity pictures which consume a lot of space. I recently came across two amazing utilities that help optimize images in Linux: jpegoptim and optipng

Install them via terminal:

```
sudo apt-get install jpegoptim
sudo apt-get install optipng 
```

And optimize away!

```
jpegoptim --size=1024k <file-name>.jpg
```

Be sure note to go minimalist ( ~ 125k - Like I did in a few of my recent posts), since that doesn't quite do a lossless compression.

The utility can also be used to bulk optimize images which can be super useful!
