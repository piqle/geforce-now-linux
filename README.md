# NVIDIA GeForce NOW Linux Launcher (REDUX)

A modified and maintained launcher for NVIDIA GeForce NOW on Linux.

#### NOTE: THIS IS A PUBLIC REPO BUT IS UNDERGOING REFACTORING. EXPECT ISSUES.

## Configuration

The script behaviour can be modified by setting the appropriate environment variables *(or by modifying the script directly).*

### Options

- `START_MAXIMIZED`: Default: **On**. Starts maximized *(Not full screened)*
- `START_IN_INCOGNITO`: Default: **Off**. Starts in incognito mode *(Note: This may not work)*
- `START_FULLSCREEN`: Default: **On**. Starts full screen. **Exit fullscreen with F11, close with Alt+F4.**
- `OVERRIDE_USER_AGENT`: Default: **Off**. Pretend to be running under ChromeOS via the User Agent string.
- `CHROMIUM_VARIANTS`: List of browsers to try, in order of preference.
    
    -  **Default:** google-chrome, microsoft-edge, vivaldi, microsoft-edge-dev, chromium

- `HW_ACCELERATION`: Default: **Off**. Enables hardware acceleration *(if not enabled by default)*

## Usage
### 1. Clone repository
   ```shell
   $ git clone https://github.com/piqle/gfn-linux-redux.git
   ```
### 2. Launch

*To invoke e.g. neither maximized nor fullscreen:*
```shell
$ START_MAXIMIZED=0 START_FULLSCREEN=0 geforce-now-linux
```
GeForce NOW is launched in *app mode* (i.e. the browser address bar, tabs and menus aren't shown).

## Supported browsers <a name="supported_browsers"></a>

The script will try to run on the first *Chromium variant* found on the system

**NOTE: Opera doesn't appear to support *app mode*, so it isn't included in the list.**
