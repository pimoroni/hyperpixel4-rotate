# HyperPixel 4 Rotation Utilities

These bash scripts help you set the correct config files to rotate HyperPixel 4 displays on Raspberry Pi OS Bullseye.

These scripts assume you are using the HyperPixel as your *only* display. You will need a custom touch mapping if you wish to use it in conjunction with an HDMI display, since touch maps across the *whole* display area.

:warning: You *must* remove any `dtparam` entries from `/boot/config.txt` that affect the x/y swap and inversion at the driver level.

If you supply an `--xorg` argument after the display orientation, the tool will attempt to create Xorg touch and display config files for generic, Xorg based distros.

# Square

Use `hyperpixel4sq-rotate` followed by one of `left`, `right`, `normal` or `inverted`.

## Config Files Affected

Lightdm/udev on Raspberry Pi OS:

* `/etc/udev/rules.d/98-hyperpixel4-square-calibration.rules`

Xorg (may work on some generic setups):

* `/usr/share/X11/xorg.conf.d/88-hyperpixel4-square-touch.conf`
* `/usr/share/X11/xorg.conf.d/88-dpi-1-rotate.conf`

# Rectangular

Use `hyperpixel4-rotate` followed by one of `left`, `right`, `normal` or `inverted`.

`left` and `right` correspond to landscape orientation, `normal` and `inverted` correspond to portrait.

## Config Files Affected

Lightdm/udev on Raspberry Pi OS:

* `/etc/udev/rules.d/98-hyperpixel4-calibration.rules`

Xorg (may work on some generic setups):

* `/usr/share/X11/xorg.conf.d/88-hyperpixel4-touch.conf`
* `/usr/share/X11/xorg.conf.d/88-dpi-1-rotate.conf`


