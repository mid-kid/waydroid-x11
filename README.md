Waydroid X11
============

Simple script to launch Waydroid in an X11 session, using Weston as a nested compositor. These can be installed onto your system, and won't interfere with launching Waydroid from a native Wayland session.

Dependencies
------------

* Waydroid: This script builds on top of waydroid
* Weston: Used to provide the Wayland compositor in the X11 session

Installation
------------

Download and unpack the release archive from the [releases page](https://github.com/mid-kid/waydroid-x11/releases), and issue the following commands:

```
./configure
make
sudo make install
```

Optional configure options:
* `--enable-drm`: Installs a standalone Waydroid session, that can be started from your login screen.

Usage
-----

Waydroid X11 should appear in your applications menu. Launch it and start using Waydroid!

To launch waydroid with a different screen resolution, use `waydroid-x11 --width=720 --height=1080`, changing the numbers to fit.

More information, bugs, etc
---------------------------

See the man pages: `man 1 waydroid-x11` and `man 1 waydroid-drm`.
