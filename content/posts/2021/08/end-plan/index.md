---
categories:
- Guides
- Misc
coverImage: Screenshot-from-2021-08-06-15-05-32.png
date: "2021-08-06"
tags:
- end-of-life-plan
- family-vault
- trilium-notes
title: Building the end plan
---

_Leave a comment if any of this doesn't make sense. I'll be more than happy to help._

Over the last few years, I've been wanting to setup a comprehensive and secure ‘handover’ document for my family - In case I cease to exist. My key priorities were it should :

- be easy to update and maintain when I am alive
- be easy to reference and access when I am dead
- have multiple fall-back points

Now, the most straightforward way to do this would be to have all the information on a secure spreadsheet or document. But that's not fun! So I decided to use Trilium Notes for it. When it's time, my wife has three options to access the support checklist a) Online via a secure portal/app b) Using a secure flash-drive c) Old school printed sheets

![](images/Screenshot-from-2021-08-06-15-05-32-1200x600.png)

I think this is something super easy to replicate. Leaving this out here should someone find it useful.

Let's get up and running:

1. Grab the [Trilium desktop app from here](https://www.electronjs.org/apps/trilium-notes) and install it on your machine. If it's the first time you are using it, it should prompt you to create a local account. You can sync this with the [server app](https://srikanthperinkulam.com/2021/04/06/installing-trilium-notes/) later if you need one.
2. On first install, Trilium also installs a demo document. This is super helpful to understand how Trilium works. But for now, collapse the '_Trilium Demo_' folder in the left sidebar.
3. Download my  '[Closeout html](https://github.com/sriperinkulam/closeout/raw/main/Closeout%20Template.zip)' template zip file. Right click on the 'root' folder on the left sidebar and click 'Import into'. Select the zip file you just downloaded and click on 'Import'. That's it! Update the template to your needs and export for backups.

Maintaining and backups:

1. To encrypt the folder, just right click on  and select 'protect subtree'.
2. Trilium provides you three modes of export - Zipped HTML, Zipped markdown and OPML. I prefer the HTML export since it can be used in isolation. Do note however that all notes lose their encryption when they're exported out!

Generic notes:

1. I've used Trilium notes since it fits into my workflow. You should be able to import the template into any note-taking app.
2. The template is obviously bare minimum and generic. Tweak/add based on your personal situation.
3. I've intentionally kept my guidance instructions and passwords isolated since I don't want to be printing them on paper. You could have them all in one place here in Trilium and secure the folder.
4. If saving the files/backups on a flash drive, I'd strongly recommend you use [VeraCrypt](https://srikanthperinkulam.com/2020/11/01/encrypting-drives/)

I am a reasonably healthy person with no alarming issues. But hey, you never know! I think it's critical that your family has good guidance on how best to pick up where you left off. Think of this as the last parting gift. It took me about four years of procrastination and few spurts of action to get here. And I am so glad I did. If not anything, it's helping me document these critical pieces in one place.

What's your life closeout plan?
