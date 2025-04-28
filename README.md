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

--License:
 Copyright (C) 2010 Dimitris Diamantis (aka ftso)
 This is free software. You may redistribute copies of it under the terms of the GNU General Public License <http://www.gnu.org/licenses/gpl.html>.
 There is NO WARRANTY, to the extent permitted by law.


--Contact:
 For bug reports or comments contact ftso via email at kotsifi@gmail.com or message at @ftso on twitter


Enjoy :-)
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMM/ _| |MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMM| |_| __/ __|/ _ \MMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMM|_____|MMMMM|  _| |_\__ \ (_) |MMMM|_____|MMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMM|_|  \__|___/\___/MMMMMMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMWX0OXMMMMMMMMMMMMMMMMMMMMMMMMMMM	
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMNOdoloOMMMMMNX0kk0NMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMXO00XMN0xololcxXMMN0kdlccokXMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMKlcdOKOoccodlcxXMNOlclolcdKWMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMWKXM0:';lxo;;:lolcoKM0lclodccxXMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMMMMMMMXookc.',,;'',;:;;lxdo::clcclONMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMNkdxOKX0:.'...........',;,'.',;:cxXWMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMNl  .':c, ...................';lONMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMx.    .         ............;d0NMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMMMO.        ...'''............c0MMMMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMNKk;     .'coxO0K0Od;.     ..,;lkKNMMMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMO;.    .,lkKXXXXXNNX0o.    .'cdxoclkXMMMMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMMXd...,cx0XWWWWNXXKKKK0x,. ..;dO0KOdc:oONMMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMMNd..cxOKXNWNNNNNNXK0OOOOk:,cd0NNXK0Oko'.:KMMMMMMMMMMMMMMMM
MMMMMMMMMMMMMMMK:. ,dk0XXXXXXXXKOdc:lxO0K000XWWWWNNKOx:. ,kNMMMMMMMMMMMMMM
MMMMMMMMMMMMMNO;   ,ok0KKKKKKKKx;,. 'lc::dKXXXXXXXXX0xc.  .oXMMMMMMMMMMMMM
MMMMMMMMMMMMMk'    'ld0KKKKKKKKk;. .;l,..l0KKKKKKKKKOd;.   .oNMMMMMMMMMMMM
MMMMMMMMMMMMK:     .,cx000000000OxodxkkxkO000000000ko:.     .dNMMMMMMMMMMM
MMMMMMMMMMM0:        .;lxO00000KKK0KKXNNXK0000kdol:,..       'OWMMMMMMMMMM
MMMMMMMMMMXc           ..ck000OkOOkxk0KKKXWWWW0l,.            ,OMMMMMMMMMM
MMMMMMMMMW0:.          .cONWWN0kKXK000O0XWMMMMMW0o'          .'xWMMMMMMMMM
MMMMMMMMNOdl:,,'''....;kXNWWMMNOkOkkO0KNWMMMMMWWNN0c....''',;:ldONMMMMMMMM
MMMMMX00xxdooc;;;:clloxkO00KKKXXXXKXNNWMMWNXKKK00Okxolcc:;;:loodxx0NMMMMMM
MMMNOc;lll:lxxdl;,''',:cldxkOxookKXNNNNXOxodkOkxolc;,''',:ldkdc:lllcoONMMM
MNk,. .'...,dxxxdoc;'....;::::cclOKXXXX0dccc::::,....';coddxxo' .''...cKMM
MN0Okd;.   ,oddddddol:,'';;,codllOXXXXX0dcodl:,:,.';cll:::cldl.   ,x00KNMM
MMMMMM0lcc;,loooooooollc:;'coooclOXXXXX0dclooo:,;cllll:;;;;;c:';ldKMMMMMMM
MMMMMMMMMMk;:cccclllllooc:,;:::;lOXNNNX0d:::::;,:lolc:;;;;;;:;oXMMMMMMMMMM
MMMMMMMMMMXl,::::lllc:;clc;'',,'cOXNNNXKd;,,,'';:::;;::;;;;;;,xMMMMMMMMMMM
MMMMMMMMMMMx',,;cll:;;;col:'....:OXXXXX0d,....;ccc;;:c:cc:,,':0MMMMMMMMMMM
MMMMMMMMMMMXl...,cc'...,l:......:OKXXXX0o'....':cc,:l;';l:'..oNMMMMMMMMMMM
MMMMMMMMMMMMd...'c:....'c;......;xOOOOOkl'....,:cc;,:c:cc,..'kMMMMMMMMMMMM
MMMMMMMMMMMMk'..,;,''''',,'.....';:,,:lc,.....';;,''';;,,'..,OMMMMMMMMMMMM
MMMMMMMMMMMM0ollc:;'................',;;'.............',:llokNMMMMMMMMMMMM
MMMMMMMMMMMMMMWX0xl;'......'',,,,;;;::::;;,,,'........,:loxO0NMMMMMMMMMMMM
MMMMMMMMMMMMXd;,;:cloodddooc:,...''''''''''..,:loddxxddolc;'.,:ckWMMMMMMMM
MMMMMMMMMMMMMx,:oddddddddddddl;'...........';lddddddddddddol:;;,,OMMMMMMMM
MMMMMMMMMMMMNxllooooooooooooollc;.'::::::c:;coddddxxxxxdddddool:lNMMMMMMMM
MMMMMMMMMMMMKxdoodxxkkkkkkxdolc:cxXMMMMMMMXkl:lddxkkkkkkxxdolclo0MMMMMMMMM
MMMMMMMMMMMMMMNKKK0kOOOkx#@ www.ftsoogle.dom.gr @#xddkkkkkkxddkWWMMMMMMMMM
