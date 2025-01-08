---
categories:
- Site
date: "2015-04-08"
tags:
- akismet
- amazon-s3
- amazon-webservices
- broken-link
- bytheway-annotations
- cloudfront
- custom-post-type
- custom-sidebars
- display-posts-shortcode
- jetpack
- plugins
- pods
- regenerate-thumbnails
- tablepress
- w3-total-cache
- wordfence
- wordpress-must-have-plugins
- wp-gpx-maps
- wp-seo
- wp-optimize
title: Important plugins for your WP Installation
---

Over the last seven years, since I [moved to a self hosted platform](https://srikanthperinkulam.com/site-hosting/transition-from-v1-0-to-v2-0 "Transition from v1.0 to v2.0") I've grown really fond of WordPress as a CMS. The ease of its installation and maintenance, the power of scaling, the flexibility to adapt it to your requirements and it's ever present support framework is something that I've really grown to appreciate over time.

I've worked on several installations of WordPress and over these years extensively tested quite a few plugins. <!--more-->Here's a log of plugins that I've really found useful and hopefully will update this list as I experiment more with them:

\[fruitful\_tabs type="default" width="100%" fit="false"\]

\[fruitful\_tab title="Security and Regular Maintenance "\]

##### **[Wordfence Security](https://wordpress.org/plugins/wordfence/)**

Started using this plugin when one of my sites was hacked (more on this later) and sworn by it ever since then. With server-side scans, e-mail alerts and regular updates, this is one plugin you should install by default.

##### **[Bad Behavior](https://wordpress.org/plugins/bad-behavior/)**

You just need to get hacked once to realize how vulnerable you actually are! I installed this plugin as a primary shield to spammers and malicious code and the ships' been sailing in full mast ever since.

##### [Updraft Plus](https://wordpress.org/plugins/updraftplus/)

A backup and restoration plugin I came across recently that easily backups the core files and databases to S3 buckets (And other services)

##### [**Akismet**](https://wordpress.org/plugins/akismet/)

There's absolutely no reason why shouldn't install this plugin. Its free, works wonders and just so easy to set up. Add a captcha and your site should be rock-solid.

\[/fruitful\_tab\]

\[fruitful\_tab title="Speed and SEO"\]

##### [**W3 Total Cache**](https://wordpress.org/plugins/w3-total-cache/)

Though not that straightforward, you can count on this plugin to drastically improve your site's speed and performance. There are tons of reference guides available online and in a few minutes you should be all fired up!

##### **[CloudFlare](https://wordpress.org/plugins/cloudflare/)**

Install this plugin once you setup a cloudflare account (Free) for your site. Besides the benefits of a [CDN](http://www.cloudflare.com/features-cdn) you also get another layer of security for [DOS attacks](http://en.wikipedia.org/wiki/Denial-of-service_attack).

##### [**Wordpress SEO**](https://wordpress.org/plugins/wordpress-seo/)

The most powerful SEO plugin I've come across yet. With a nifty setup it compels you to write better content. The ease of updating your meta tags and the dynamic scoring gives you a very clear picture on your SEO rankings for each post.

##### [**WP-Optimize**](https://wordpress.org/plugins/wp-optimize/)

Worpress being the dynamic CMS gives you robust features such as post revisions, Trackbacks and pingbacks, transient options to state a few. Over time as your portal content increases, this may cause unnecessary meta data and content. WP-optimize does a wonderful job of optimizing and cleaning your database.

##### [**Broken link checker**](https://wordpress.org/plugins/broken-link-checker/)

One nifty plugin to keep track of your links. Based on your site settings, this plugin gives you complete control of the links you use on your portal and does a brilliant job not only in picking up broken links but also giving you remedial options.

\[/fruitful\_tab\]

\[fruitful\_tab title="Custom Post Types"\]

##### [**Pods - Custom Content Types and Fields**](https://wordpress.org/plugins/pods/)

Enter the world of Custom content types and fields - The true power of Wordpress as a CMS. Pods helps you generate CPTs in a matter of seconds. I chanced on this plugin when I just learnt about CPTs and have been extensively using them ever since.

##### **Book Review Library**

Think of this as a variant of the Pods plugin. This plugin comes in-built with features such as authors and ratings.

##### [**Current Menu Item for Custom Post Types**](https://wordpress.org/plugins/current-menu-item-for-custom-post-types/)

This plugin lets you add a parent page for a CPT and highlight the menu accordingly.

\[/fruitful\_tab\]

\[fruitful\_tab title="Enhanced features"\]

##### [TablePress](https://wordpress.org/plugins/tablepress/)

WordPress by default doesn't provide tables. This plugin gives you a truly functional and easy to implement table feature for your installation. With import and export features, this is one plugin that really stands out in its kind.

##### **[ByTheWay Annotations](https://wordpress.org/plugins/bytheway/)**

If you've read any of my [Actuarial Postpad posts](https://srikanthperinkulam.com/actuarial-postpad/ "The Actuarial Postpad"), you would have noticed the power of \[btw\] ByTheWaty Annotations \[/btw\]! One effective short-code usage to highlight content.

##### **[Custom Sidebars](https://wordpress.org/plugins/custom-sidebars/)**

Powered by the super-awesome [wpmudev](https://premium.wpmudev.org/) team, this is one plugin you could use to modify the way you display content even in really complex themes. The flexibility to work on the sidebars is truly amazing!

##### [**Display posts shortcode**](https://wordpress.org/plugins/display-posts-shortcode/)

This plugin gives you the power to display list of posts based on certain criteria. The truly powerful feature is its ability to work with Custom Post Types. Well documented and one truly powerful plugin.

##### [**Jetpack**](https://wordpress.org/plugins/jetpack/)

Powered by [Automattic](http://automattic.com/), this plugin gives you a slew of features to customize your Wordpress installation. Most of the settings work out of the box and brings in features previously only available to Wordpress.com users.

##### [**Simple Mathjax**](https://wordpress.org/plugins/simple-mathjax/)

One powerful plugin to solve all your latex worries on Wordpress. Most of my mathematical posts are powered by Simple Mathjax and Jetpacks inbuilt latex support. [CodeCogs LATEX equation editor](http://www.codecogs.com/latex/eqneditor.php) is yet another support framework truly worth exploring!

##### [**SyntaxHighlighter Evolved**](https://wordpress.org/plugins/syntaxhighlighter/)

This plugin easily helps you post your syntax highlighted code in your posts. With its support for many languages and its ease of use, this plugin is a must have if you work with developing and sharing code snippets.

##### [**WP CSV**](https://wordpress.org/plugins/wp-csv/)

One simple CSV export and import plugin. Works with CPTs too.

##### [**Better Font Awesome**](https://wordpress.org/plugins/better-font-awesome/)

Helps you automatically integrate the latest version of the [font awesome toolkit](http://fontawesome.io/) into your Wordpress installation.

\[/fruitful\_tab\]

\[fruitful\_tab title="Storage and Media"\]

##### [**Amazon Webservices**](https://wordpress.org/plugins/amazon-web-services/)

I recently moved all my images to the Amazon S3 service to steer clear of image link issues and server delays. The Amazon Webservices plugin is a primary plugin to connect your Wordpress installation to Amazons' Webservices account.

##### [**Amazon S3 and CloudFront**](https://wordpress.org/plugins/amazon-s3-and-cloudfront/)

Coupled with the Amazon Webservices plugin, this plugin automatically uploads all your images on to the S3 bucket you'd setup previously. The optional CloudFront feature also brings in the additional benefit of serving your images from Amazons' CDN.

##### [**Regenerate Thumbnails**](https://wordpress.org/plugins/regenerate-thumbnails/)

A handy plugin to regenerate all your thumbnails. Very useful when you have images that are not yet ported on to the Amazon S3 bucket but would like to do so in bulk. More of a secondary option but truly worth it!

##### [**Instagrate to wordpress**](https://wordpress.org/plugins/instagrate-to-wordpress/)

Sync your Instagram posts with Wordpress and use the auto post to seamlessly post updates to your portal.

\[/fruitful\_tab\]

\[fruitful\_tab title="Charts and Mapping"\]

##### [**WP-GPX-Maps**](https://wordpress.org/plugins/wp-gpx-maps/)

When talking about fitness, data and Wordpress , this is one plugin I would highly recommend. Using imported GPX files, this plugin gives you dynamic elevation, speed, cadence and heart-rate plots. Brilliance at work!

##### **gpx2chart**

Yet another nifty plugin that captures your Garmin data beautifully with core statistics tabled out. Talk about details!

\[/fruitful\_tab\]

\[/fruitful\_tabs\]
