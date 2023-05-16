# HyperPixel 4 Rotation Utilities

These bash scripts help you set the correct config files to rotate HyperPixel 4 displays on Raspberry Pi OS Bullseye.

These scripts assume you are using the HyperPixel as your *only* display. You will need a custom touch mapping if you wish to use it in conjunction with an HDMI display, since touch maps across the *whole* display area.

# Square

Use `hyperpixel4sq-rotate` followed by one of `left`, `right`, `normal` or `inverted`.

:warning: You *must* remove any `dtparam` entries from `/boot/config.txt` that affect the x/y swap and inversion at the driver level.

# Rectangular

Use `hyperpixel4-rotate` followed by one of `left`, `right`, `normal` or `inverted`.
