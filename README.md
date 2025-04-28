# protectmyfs
Protectmyfs is a shell script for easy fsprotect configuration from recovery mode (single kernel parameter) of grub 2 menu.


 
--About:
 When you enable the file system protection...
 Filesystems will be protected and no change is ever written to the disk.
 All changes will be written to the virtual memory and will be lost after the system reboot.
 The benefit is that you can try to do anything that can "destroy" the system without worry!

 More about fsprotect: http://www.v13.gr/index.php?nocache=0&m=vsite-proj&proj=fsprotect


--Version:
 Version 1.0


--Dependencies:
 (Tested on Ubuntu and Kubuntu 10.04)
 *Fsprotect (version 1.0.5 or above)
    http://packages.debian.org/unstable/admin/fsprotect
 *Notify-send
    libnotify1, libnotify-bin
 *Grub version 2
 *Whiptail


--Installation:
 Just copy the script into the '/usr/share/recovery-mode/options/' directory and make it executable.


-- Running:
 On the grub 2 menu select the 'recovery mode' and then 'Protect the file system'.


--Warnings:
  *You can use the script only if you have 2Gb virtual memory (ram+swap) or more.
  *POP3 emails, database changes, bookmarks etc will be lost after reboot.
  *The ROOT filesystem needs to be given at least 1Gb. On the other filesystem, if the gigabytes limit not be given, the default 0.5G will be used.
  *On ubuntu systems the network manager maybe not load the default connection automatically. (This is an apparmor's problem)
