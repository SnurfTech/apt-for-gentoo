# APT for [Gentoo Linux](https://gentoo.org/)
A Python program, made for Gentoo Linux that uses emerge to install packages, but has an interface similar to the APT package manager from Debian Linux

> Currently doesn't support the -y or --assume-yes flags, but does include the "unmask" flag, which allows you to unmask a package by using vim to open /etc/portage

> Please note that this is not an official release of APT, and that this program may not include every feature

## Table of Contents:

- [Install](/#install)
- [Uninstall](/#uninstall)
- [Help Text](/#help-text)

### Install:

Install dependencies:

```
emerge -n curl vim dev-python/colorama python3
```

Run these commands:

```
cd /usr/bin
sudo curl https://raw.githubusercontent.com/XRG2014/apt-for-gentoo/main/apt -o apt
sudo curl https://raw.githubusercontent.com/XRG2014/apt-for-gentoo/main/apt -o apt-get
sudo chmod +x apt
sudo chmod +x apt-get
```

(optional) Uninstall curl:

> Curl is no longer needed

```
emerge -Cv curl
```

### Uninstall:

(optional) Uninstall dependencies:

> Assuming you don't have curl uninstalled (If you do, then just remove the phrase "curl" from the command below) 

```
emerge -Cv curl vim dev-python/colorama python3
```

Run these commands:

```
sudo rm -rfv /usr/bin/apt
sudo rm -rfv /usr/bin/apt-get
```

### Help Text:

```
usage: apt [--help] [--sync] [-h?] ...
--help, -h, -?:      display help text
install:             install package
remove, autoremove:  remove package
update:              update repositories and ebuilds
upgrade:             upgrade package or everything
config-update:       update configuration files
unmask:              unmask a package (no arguments)
```
