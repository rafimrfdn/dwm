This is my very first DWM 6.2 newest build. Very simple and works well for my workflow.

Patches in this DWM
===================

- Autostart           // use to make autostart.sh file run after DWM first start on system
- Warp                // use to make mouse always follows the focus screen
- Fullgaps            // use to create gaps between window
- Systray             // I use this to set tray before the dwmbloks (date status)
- Pertag              // use this to make different tag mode for every tag. Ex: [1] set to Floating, but in [2] can set to Monocle
- Alwayscenter        // make floating window always in center of the screen

dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.


Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.

