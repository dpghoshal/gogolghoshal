---
layout: default
comments: true
title: My always-up-to-date guide to reinstalling Fedora
date: 2014-05-17
permalink: /posts/2014-05-17-my-always-up-to-date-guide-to-reinstalling-fedora
published: true
---

## My always-up-to-date guide to reinstalling Fedora

*UPDATE: Fedora is no longer my primary OS. Hence I have stopped updating this post.*

*Note: This guide is meant as a handy reference for my own use. If anybody else finds it useful, that's a bonus.*

###Installing Fedora 20 64-bit (default GNOME desktop)

Remember to encrypt disk. 

Remember to provide a proper hostname for machine.


Partioning scheme (for 500 GB hard disk):


New Fedora 20 Installation  
DATA  
/home ===> 417.236 GB  
SYSTEM  
/boot ===> 500 MB  
/ ===> 51.2 GB  
swap ===> 8 GB

Installation complete. Fedora up & running.

Tinker with Settings menu.

Install Fastest mirror plugin for Yum

	$ sudo yum install yum-plugin-fastestmirror

Update Fedora

	$ sudo yum update

Reboot

Install TrueCrypt (from website)  
(To uninstall TrueCrypt, run 'truecrypt-uninstall.sh')

To run TrueCrypt GUI with sudo permission:

	$ sudo visudo

comment out the line "Defaults requiretty"

Copy 'superset' data from backup (might take a while)  
(new location of data is /home/gogol/superset/ )

Install RPMFusion repo (follow instructions given on <http://rpmfusion.org/Configuration> )

Install wget 

	$ sudo yum install wget

Install rpm.livna.org repo (follow instructions given on <http://rpm.livna.org/> )

Install codecs etc 

	$ sudo yum install libdvdcss gstreamer-plugins-ugly gstreamer-plugins-bad gstreamer-ffmpeg xine-lib-extras-freeworld

Install VLC media player 

	$ sudo yum install vlc

Install Redshift

	$ sudo yum install redshift

To add redshift to session startup:  
ALT+F2  ->  gnome-session-properties  
add "redshift -l $lat$:$long$" (substitute $lat$ & $long$ with the latitude & longitude of current location)

Install Tmux

	$ sudo yum install tmux

Install Calibre from website, and set up the libraries.

Install Chrome (from website rpm file)

Install the GNU Compiler Collection

	$ sudo yum install gcc

Install git

	$ sudo yum install git

Follow instructions given on <https://help.github.com/articles/using-jekyll-with-pages>

	$ sudo yum install ruby  
	$ gem install bundler  
	$ sudo yum install ruby-devel

Navigate to repo folder and do

	$ bundle install

Set up SSH keys for GitHub gogolghoshal account  
(Follow instructions given on <https://help.github.com/articles/generating-ssh-keys> )


To create permanent aliases for backup steps, add the following lines to the ~/.bashrc file:

	alias b1="sudo truecrypt /run/media/gogol/Gogol_Seagate_500GB/BACKUP_Gogol/Truecrypt_container_file /home/gogol/Ext_HDD"
	alias b2="bash ~/superset/gogol_backup_script"
	alias b3="sudo truecrypt -d"

To add "New Document" option to Nautilus right-click menu:

	$ cd ~/Templates  
	$ touch new

Install DropBox (from website rpm file). Sync DropBox profile.  
Error: Dropbox can't monitor the filesystem.  
Please run

	echo fs.inotify.max_user_watches=100000 | sudo tee -a /etc/sysctl.conf; sudo sysctl -p

and restart Dropbox.

Install Deluge BitTorrent client

	$ sudo yum install deluge

Install SpiderOak (from website rpm file). Sync SpiderOak profile.

Install LastPass Pocket from website (follow website instructions).

* * *

[Archive](../archive)
