kernel-archosg9
===============

Kernel Adaption from Omapzoom 3.0 line

Forked from http://git.omapzoom.org/?p=kernel/omap.git;a=shortlog;h=refs/heads/p-android-omap-3.0.
Merged with archos specific changes (in progress) of the g9 tablet.

Currently there works the initial boot process. USB Hub is initialized, so UART3 can be used.
See http://forum.xda-developers.com/showpost.php?p=30032311&postcount=65 for instructions how to use
the serial over USB port method.

Don't use the CONFIG_DEBUG_LL=y option. It doesn't work in this kernel.

In addition to that, the adb usb bridge can also used for debugging.
Currently the kernel is rebooted because the watchdog daemon cannot initialize the device.
Some spinlock errors and are around and also some mutext context failures.