# Installing Brickadia for use with Proton

## Prerequisites

This will require an official version of Proton (downloadable from Steam (enable listing *Tools* in your Library/Games view) or from [Valve's official repository](https://github.com/ValveSoftware/Proton/releases)), or any unofficial Proton fork you wish to use (GloriousEggroll, tkg, etc.).  
You will also need Wine and winetricks installed, please see Wine's or your Linux distro's documentation on installing these.  

### **!!! The guide will follow Arch Linux procedures for installing packages, please adapt these instructions to your Linux distribution. !!!**

By default, Steam will place official Proton releases in `~/.local/share/Steam/steamapps/common`, and looks for unofficial forks in `~/.steam/steam/compatibilitytools.d`.  

Commands denoted with a `#` will require root, those denoted with `$` will be run as a normal user. `sudo` can be used to request root-level access on a per-command basis.

### Setting things up
First, we need to install the prerequisite packages:
- wine
- winetricks
- curl
- steam *(optional)*

***Note:** The `multilib` repository must be enabled for `wine`, `winetricks`, and optionally `steam`. Enable this in `/etc/pacman.conf`.*
```
# pacman -S wine winetricks
```

To keep things tidy, we need to create a folder for Brickadia to reside in, as well as the directory Proton needs to store its data.
```
$ mkdir -p ~/Games/Brickadia; cd ~/Games/Brickadia
```

Now we download the Brickadia launcher's installer
```
$ curl -o BrickadiaInstaller.exe "https://static.brickadia.com/launcher/1.4/BrickadiaInstaller.exe"
```

### Installing the launcher
We first need to set an environment variable so that Proton knows where to store data. To make life a little easier for us, we'll also set where we have Proton installed.
```
$ export STEAM_COMPAT_DATA_PATH=$HOME/Games/Brickadia
$ export PROTON_DIR=$HOME/.local/share/Steam/steamapps/common/Proton\ 5.0
```

Then, we run the launcher installer using Proton
```
$ "$PROTON_DIR"/proton run BrickadiaInstaller.exe
```

*The installer may seem to lock up after a minute while installing the VC2010 redistributable package.* If this is the case, simply Ctrl-C in your terminal and re-run the above command. It may take 2-3 attempts, but should eventually pull through and finish installing.  

Once the launcher installs, we need to re-install VC2010 manually *(author note: I don't know if the x64 version installed by the installer is damaged or if the x86 version is supposed to be installed alongside it. winetricks takes care of both situations.)*  

Ignore any warnings that appear in the terminal, these are normal. Choose the repair option for the x64 installer.
```
$ WINEPREFIX=$STEAM_COMPAT_DATA_PATH/pfx winetricks vcrun2010
```

### Running the game
After the launcher is installed and VC2010 is manually re-installed, the launcher should now be able to download the game's files and launch.  
To make things easier, we'll put the directory the launcher was installed to in an environment variable.
```
$ export LAUNCHER_DIR=$STEAM_COMPAT_DATA_PATH/pfx/drive_c/Program\ Files/Brickadia/BrickadiaLauncher
```
Now we launch!
```
$ "$PROTON_DIR"/proton run "$LAUNCHER_DIR"/BrickadiaLauncher.exe
```

# Scripts for one-click installing/running
Place these in the `~/Games/Brickadia` folder you created in the beginning of the guide:
https://gist.github.com/TheBlackParrot/280b9f86dcc41085f9213b9ef75dcf55
