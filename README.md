# JailManager
A Bash shell script for creating, managing, and removing jails.

This project provides a simple shell script for creating and managing jails. It
does not require any dependencies other than Bash and it works on any
FreeBSD system (version 13.x and newer) in the -RELEASE branch with either the UFS or ZFS filesystem.

To get started, there are two options. The first is to simply install Jail Manager from
FreeBSD's package repository:

     pkg install jailmanager

Alternatively, you can install Jail Manager from this repository using the folling three commands.
This will install the Bash shell, fetch the Jail Manager script, and install it on your system:

     pkg install bash
     fetch "https://raw.githubusercontent.com/slicer69/JailManager/refs/heads/main/jm"
     cp jm /usr/local/bin/

Please note the above "pkg" and "cp" commands, as with the commands which follow in this document,
should be run as root. Either directly or by using an access elevating tool such as "sudo"
or "doas".

At this point the Jail Manager script has been installed. We can then run this one-time 
command to initialize the FreeBSD system for running jails.

     jm init

The above command needs only to be run once, to prepare the system's directories
and services.

To create a jail called "hello" run:

     jm create hello

To start the new jail run:

     jm start hello

To see a list of all jails, running or not, run:

     jm list-all

To see a list of running jails run:

     jm list

To launch a shell that runs inside the new jail run:

     jm enter hello

The shell inside the jail can be terminated by running "exit".

To update an existing jail called hello run:

     jm update hello

To stop a running jail called hello run:

     jm stop hello

Old jails can be removed by running:

     jm destroy hello

