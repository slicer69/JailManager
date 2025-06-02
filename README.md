# JailManager
A Bash shell script for creating, managing, and removing jails.

This project provides a simple shell script for creating and managing jails. It
does not require any dependencies other than Bash and it works on any
FreeBSD system (version 13.x and newer) with either the UFS or ZFS filesystem.

To get started, first install bash:

     pkg install bash

Next download the Jail Manager script and place it in an executable location on your
system:

     curl "https://raw.githubusercontent.com/slicer69/JailManager/refs/heads/main/jm" > jm
     cp jm /usr/local/bin/

Please note the above "cp" command, as with the commands which follow in this document,
should be run as root. Either directly or by using an access elevating tool such as "sudo"
or "doas".

Then run this one-time command to initialize the FreeBSD system for running jails.

     jm init

The above command needs onlyto be run once, to prepare the system's directories
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

