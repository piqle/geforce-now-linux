# NVIDIA GeForce NOW on Linux

A modified and maintained launcher for NVIDIA GeForce NOW on Linux.

## Options and default behaviour

The script behaviour can be modified by setting the appropriate environment variables (or by modifying the script directly).

These are the configurable options:

- `START_MAXIMIZED`: Default: **On**. Starts maximized but not completely full screen.
- `START_IN_INCOGNITO`: Default: **Off**. Starts in incognito mode (note this doesn't appear to work at least on my system).
- `START_FULLSCREEN`: Default: **On**. Starts full screen (no titlebar), exit fullscreen with F11, close with Alt+F4.
- `OVERRIDE_USER_AGENT`: Default: **Off**. Pretend to be running under ChromeOS via the User Agent string.
- `CHROMIUM_VARIANTS`: List on browsers to try, in order or preference (see [*Supported browsers*](#supported_browsers)). \
    Default: google-chrome, microsoft-edge, vivaldi, microsoft-edge-dev, chromium
- `HW_ACCELERATION`: Default: **Off**. Enables hardware acceleration (if not enabled by default)

To invoke e.g. neither maximized nor fullscreen:
```shell
$ START_MAXIMIZED=0 START_FULLSCREEN=0 geforce-now-linux
```

GeForce NOW is launched in *app mode* (i.e. the bowser address bar, tabs and menus aren't shown).

## Supported browsers <a name="supported_browsers"></a>

The script will try to run on the first *Chromium variant* found on the system

NOTE: Opera doesn't appear to support *app mode*, so it isn't included in the list.
