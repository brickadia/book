# Installation

Brickadia has a launcher that will update the game for you, so you'll only need to install it once.

## Windows

Download the Windows installer from [the download page] and run it.

Windows SmartScreen may say that "Windows protected your PC" because the installer has not been run by enough users. To continue, click **More info**, then **Run anyway**.

If you do not have the **More info** option, you will need to adjust a setting:

1. Open the Windows Defender settings
2. Go to **App & browser control**
3. Under *Check apps and files*, select the **Warn** option instead of the **Block** option
4. Run the installer again

You'll get a shortcut to start Brickadia on your desktop, and several others in your start menu.

## Linux

*The Vulkan renderer in the game is known to be unstable in its current state. If you're experiencing random bouts of crashing, you may want to [try running the game in Proton](./installation_proton.md).*

### Debian/Ubuntu

Download the `brickadia-launcher.deb` package from [the download page].

On most distributions, you should be able to open it to install it. If not, run this command:

```bash
sudo apt install ~/Downloads/brickadia-launcher.deb
```

Application entries will be added for Brickadia.

### Other

An official package is not available for any other distributions yet, but you can download an archive of the launcher that should work on most Linux distributions, provided that you find the dependencies.

Download the `brickadia-launcher.tar.xz` archive from [the download page]. Extract it, and run the `brickadia-launcher` file to start the game.

[the download page]: https://brickadia.com/download

The following is a list of dependencies based on the Debian package. The exact names may vary slightly by distro.
```
libbsd0
libc6
libcom-err2
libdbus-1-3
libexpat1
libfontconfig1
libfreetype6
libgcc1
libgcrypt20
libgl1
libglib2.0-0
libglvnd0
libglx0
libgpg-error0
libgssapi-krb5-2
libk5crypto3
libkeyutils1
libkrb5-3
libkrb5support0
liblz4-1
liblzma5
libpcre3
libpng16-16
libstdc++6
libsystemd0
libx11-6
libx11-xcb1
libxau6
libxcb-icccm4
libxcb-image0
libxcb-keysyms1
libxcb-randr0
libxcb-render-util0
libxcb-render0
libxcb-shape0
libxcb-shm0
libxcb-sync1
libxcb-util0 or libxcb-util1
libxcb-xfixes0
libxcb-xinerama0
libxcb-xkb1
libxcb1
libxdmcp6
libxext6
libxkbcommon-x11-0
libxkbcommon0
zlib1g
```
