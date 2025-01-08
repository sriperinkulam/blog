---
categories:
- Tech
date: "2008-06-05"
tags:
- add-new-tag
- installing-grub
- modifying-grub-entries
- ubuntu-missing-after-windows-install
- ubuntu-windows
- ubuntu-windows-grub
- windows-missing-after-ubuntu-install
title: Dual booting Multiple OS
---

Hosting more that one OS on your hard disk can be a pain if you're not really sure on configuring the boot loader. I'll confine the scope of this post to parenting only Debian based Linux OS ( Ubuntu ) and WIndoze. Because for the most part of it, I've only worked on them.

Why would you have to Install / reconfigure Grub in the first case?

1) You had to install Windows after you installed Ubuntu/Linux which led to the Grub ( Previously installed by Ubuntu ) to be over written by the Windows Boot loader.

2) You screwed up an installation right at the wrong spot and now you can boot neither Windows nor Linux.

Installing Grub through a Live CD:

1. Insert the Ubuntu Live CD into the tray and restart your system
2. Once you're at the Live CD Desktop, Navigate to the terminal ( Applications>Accessories>Terminal)
3. Type **sudo fdisk -l** /\* This would list all the OS installations and drives that you have. Make note in which drive Ubuntu has been installed - Let's say it's hda3\*/
4. Next we'll have to enter the Grub shell. Fot that type **sudo grub**
5. In the grub menu type find **/boot/grub/stage1** . This would return a listing of the drives in which the OS's/ boot records are installed.
6. Identify where Ubuntu's Grub is on, by relating the output from step 3 and the above output.Now to let the Grub shell know what grub files are to be used, type **root (hd0, 3)** /\* You'll have to change this accordingly as per your output from step 3\*/
7. Now to install Grub on MBR,  type **setup (hd0)**
8. By now, You should have got a success message from the grub shell telling you that the Grub has successfully been installed.
9. Type **quit** and exit the terminal. Reboot and this should have properly fixed your Grub.

Installing Grub using the Super Grub disk:

If in case you do not have a Live CD, you can download a super grub disk and use it to setup the Grub for you. Check this page for more info on using the Super grub disk.

Note:

Installing Grub in your MBR will overwrite WIndows bootloader. If in case you do not find Windows in your boot menu after rebooting, all that you have to do is to make an entry in the Grub boot list.

Making an Entry of Windows in the Grub boot list:

- In the terminal , type sudo gedit /boot/grub/menu.lst /\* Always have a backup of this file. Screwing this will only cause more trouble \*/
- Add the following lines wherever you would like the Windows entry to be listed

title WIndows XP Professional Edition

root(hdX,Y) /\* Based on the fdisk -l output. Note: /dev/hda1 ==(hd0,0). /dev/hda2==(hd0,1) --> Grub  convention \*/

savedefault

makeactive

chainloader +1

- Save Menu.lst and reboot. This should resolve the issue
