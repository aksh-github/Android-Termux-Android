
# Linux on Android with Termux 

## On Android

Install openssh if not already


Follow the cmds from
	https://wiki.termux.com/wiki/Remote_Access
	section: Setting up password authentication

To start ssh on termux

```
	sshd
```

## Login to termux From remote system

You can login to termux like
	https://wiki.termux.com/wiki/Remote_Access
Using the SSH client

Gen. cmd will be: 
 
```
ssh -p 8022 user@hostname_or_ip
```

## Install Linux distro on Termux

https://youtu.be/9_xUs6CEtVc?si=0HMJ795uduwTvgEc

https://github.com/LinuxDroidMaster/Termux-Desktops/blob/main/Documentation/proot/alpine_proot.md#-first-steps-

### Install Dir for distro
/data/data/com.termux/files/usr/var/lib/proot-distro/installed-rootfs

Once installed we can login using
 
```
pd login alpine
```

	Update and upgrade the default packages:
 
```
apk update
apk upgrade
```

  Add user

  
```
adduser droidmaster
nano /etc/sudoers
```

	Add the following line to the sudoers file:

 ```
	droidmaster All=(ALL:ALL) ALL
```

### Install ngrok in termux directly

Follow steps on https://github.com/JesusChapman/termux-ngrok

Typically do NOT replace or modify open ssh install / version.
