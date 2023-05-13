# Linux Setup

This guide assumes you are hosting a server on a Debian based distro, on a x86-64 CPU[^arm]

You can use any linux distro you want to host Brickadia, you will just need to adjust the commands to what your distro provides by default.

## New User

Its recommend installing Brickadia onto a user that isn't `root`[^root].

```sh
sudo adduser brickadia
```

After running this command, you will get the following (shortend) output:

> Creating home directory `/home/brickadia' ...
>
> New password:

Enter the users new password, and just press 'ENTER' to skip the questions adduser asks you.

To access the user, you must use the command:

```sh
su - brickadia
```

From now on, this guide will assume you are logged in as `brickadia`.

## Installation

Brickadia does not offer a separate binary for servers, instead you are required to download the launcher.

Head on over to [Brickadia download page](https://brickadia.com/download) and copy the link to `Linux(Other) .tar.xz` archive.

On your server, donwload the archive with:
```sh
wget https://static.brickadia.com/launcher/[VERSION]/brickadia-launcher.tar.xz
```

This will download `brickadia-launcher.tar.xz`. Next you will need to extract the launcher from tar.

```sh
tar -xf brickadia-launcher.tar.xz && cd brickadia-launcher
```

Inside the new `brickadia-launcher`, run the following command to download the game:

```sh
./brickadia-launcher --server
```

<details>
  <summary>Help, I just got a Permission denied error</summary>

  If you get the following error: `./brickadia-launcher: Permission denied`, you will need to run:

  ```sh
  chmod +x ./brickadia-launcher
  ```
</details>

Once the game has downloaded, the game will start the server. You should close the server (ctrl + c) and move onto the next step.

## Port Forwarding

Read [portforward.brickadia.dev](https://portforward.brickadia.dev/), as this will always contain the latest ports you will want to port forward.

We will be using [ufw](https://help.ubuntu.com/community/UFW) to port forward, as most distros tend to include it out of the box.

```sh
sudo ufw allow 7777/udp
```

## Startup

Brickadia servers require authentication before they can appear on the master list. To do so, you must pass your username and password at least once when launching the server.[^password]

```sh
 ./brickadia-launcher --server -- -User=Username -Password="password"
```

After this, you do not need to pass your username or password as the file is cached in `~/.config/Epic/Brickadia/Saved/Auth`.

Assuming all went well, you should now be able to join your server. You can configure your game once you have joined it, by pressing `Esc` and pressing `Edit Game`.

## Misc

Files of importance:
- Configs: `~/.config/Epic/Brickadia/`
- Install: `~/.local/share/brickadia-launcher/`

Commands:
- `quit` - Quit the game

----

[^arm]: Arm is not supported officially, however [box64](https://github.com/ptitSeb/box64) has been known to work with Brickadia.

[^root]: Its good practice in linux not to run applications under `root` unless they require that level of access to the system. There is nothing preventing you from doing so.

[^password]: The command includes a space at the start, as it tells bash to not save it in `~/.bash_history`
