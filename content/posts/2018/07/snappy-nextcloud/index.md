---
categories:
- Tech
- Tech
date: "2018-07-09"
tags:
- chatter
- coreos
- nextcloud-box
- snappy
- ubuntu
title: Snappy Nextcloud
---

Last year, I procured a [Nextcloud box](https://nextcloud.com/box/) and moved part of my data to it. I'd just heard about [Ubuntu Snappy Core OS](https://srikanthperinkulam.com/2017/11/04/fired-up/) and was keen on porting my install to that setup. I finally got around doing that last week and thought I'd quickly jot down the install steps for reference later. Essentially, I installed the Core OS on a 32GB microSD card and installed Nextcloud as a snap. Two 1TB hard drives service the Pi3 and are synced with rclone. Below is a crude outline of the setup:

**Install and sign-in to the UbuntuCore OS:**

1.Download the latest [Ubuntu Core OS](https://www.ubuntu.com/core) and use [Etcher](https://etcher.io/) to burn it on to a microSSD card.

2.On your local machine generate a public/private rsa key using the following command: `ssh-keygen -t rsa` Create an [UbuntuOne](https://login.ubuntu.com/) account if you don't already have one and import your ssh key to your account. You'll need this to ssh into your Core OS pretty soon.

3.Slide in the microSSD card onto the Pi3 board. Then connect a monitor, keyboard and hard drive to the Pi3 and power it on. The Pi3 Board B comes with in-built wi-fi and bluetooth and once powered on it should automatically prompt you to connect to the wi-fi and then to your UbuntuONE account. Once this is setup, you should be able to ssh into the CoreOS from your local machine using: `ssh ubuntu-username@192.168.0.xx` \[btw\] If ssh fails - "Error - signandsend\_pubkey: signing failed: agent refused operation". This is most likely because the ssh agent is already running but isn't able to find the private keys. To add the keys to the authentication agent, enter `ssh-add`. Also to see list of fingerprints of all identities added use `ssh-add -l` \[/btw\]\[btw\]To add a password for the user: `sudo passwd ubuntu-username`\[/btw\]\[btw\]To re-configure network at anytime: `sudo console-conf`\[/btw\]

**External Drive setup** 1.I use two external hard-drives one as a primary and the other as a secondary. First format the drives: `sudo fdisk /dev/sda` \[btw\]`Welcome to fdisk (util-linux 2.27.1). Changes will remain in memory only, until you decide to write them. Be careful before using the write command. Command (m for help): o Created a new DOS disklabel with disk identifier 0x8b913f43. Command (m for help): n Partition type p primary (0 primary, 0 extended, 4 free) e extended (container for logical partitions) Select (default p): p Partition number (1-4, default 1): First sector (2048-1953458175, default 2048): Last sector, +sectors or +size{K,M,G,T,P} (2048-1953458175, default 1953458175): Created a new partition 1 of type 'Linux' and of size 931.5 GiB. Command (m for help): w The partition table has been altered. Calling ioctl() to re-read partition table. Syncing disks.` \[/btw\]

2.Format the partition and give it the label data. This label will be used to reference it for mounting later: `sudo mkfs.ext4 -L data /dev/sda1` \[btw\] mke2fs 1.42.13 (17-May-2015) /dev/sda1 contains a ext4 file system labelled 'data' last mounted on Sat Nov 18 08:38:49 2017 Proceed anyway? (y,n) y Creating filesystem with 244182016 4k blocks and 61046784 inodes Filesystem UUID: c03685e6-fc4d-4d69-b8cf-8b17b24f2e0a Superblock backups stored on blocks: 32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208, 4096000, 7962624, 11239424, 20480000, 23887872, 71663616, 78675968, 102400000, 214990848 Allocating group tables: done  
Writing inode tables: done  
Creating journal (32768 blocks): done Writing superblocks and filesystem accounting information: done \[/btw\]

3.To mount the partition we're forced to rely on systemd since most of Ubuntu core system is read-only and editing /etc/fstab is not an option. Mount units need to be named after the mount point directories they control. So create the media-data.mount unit: `sudo vi /writable/system-data/etc/systemd/system/media-data.mount` and add in the following content: `[Unit] Description=Mount unit for data [Mount] What=/dev/disk/by-label/data Where=/media/data Type=ext4 [Install] WantedBy=multi-user.target`

4.Reload systemd to reflect the changes,Start and enable the mount volume so it gets automatically mounted: `sudo systemctl daemon-reload sudo systemctl start media-data.mount sudo systemctl enable media-data.mount`

5.Make sure Ubuntucore is up to date and refresh: `sudo snap refresh sudo reboot` After the reboot make sure /media/data is mounted and functional: `sudo systemctl status media-data.mount`

**Install and configure Nextcloud as a snap**

1.Install Nextcloud: `sudo snap install nextcloud` 2.Access the nextcloud install from any browser in the network using the IP address: http://192.168.0.xx, create an admin account and complete the installation. 3.Enable the 'External Storages' app under 'Apps'. 4.Associate the removable media with nextcloud: `sudo snap connect nextcloud:removable-media core:removable-media` 5.Map /media/data with nextcloud in the external storage with the following settings: `Folder name: data External storage: Local Authentication: None Configuration: /media/data Available for: All` 6.Setup encryption certificates: `sudo nextcloud.enable-https self-signed` 7.To access the setup pi3 server from outside the local network, you'll need to map the dynamic dns provided by your ISP to a global address. I used no-ip and my netgear router to facilitate this. 8. Do note that when you upload files, by default they're saved to the microSD card!!\[btw\]here: /var/snap/nextcloud/common/nextcloud/data/_NC\_user_/files\[/btw\]. Read [this forum](https://help.nextcloud.com/t/is-there-a-safe-and-reliable-way-to-move-data-directory-out-of-web-root/3642/51) for details. 9. If more than one user would be using the external data mount either install the 'File access control' app and setup rules or create folders for each person and just mount those folders for each user in the Nextcloud admin panel.
