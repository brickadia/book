# Dedicated Server
Brickadia allows you to host a server on a dedicated machine. You may want to do this if:
- You have a VPS/bare metal server spare
- You want to avoid hosting a server on your own machine/home network
- You want to offload the processing required onto another machine

## Requirements
Before you start this guide, you will need the following:
1. A machine that is running `Windows` or `Linux`
  - For the best reliability, we recommend getting a VPS or a bare metal machine from a server rental company. If you are home hosting off an old laptop, your results may vary.
2. A way to connect to that machine, either through `SSH` or with a keyboard & monitor.

## Linux
In this tutorial, we assume you are hosting a server on a Debian based distro. 

### User
In general, we recommend installing Brickadia onto a user that isnt `root`[^root].

```bash
sudo adduser brickadia
```


### Install



### Windows Setup




[^root]: Its good practice in linux not to run applications under `root` unless they require that level of access to the system. There is nothing preventing you from doing so however.
