# APT for [Gentoo Linux](https://gentoo.org/)
A Python program, made for Gentoo Linux that uses emerge to install packages, but has an interface similar to the APT package manager from Debian Linux

> Currently doesn't support the -y or --assume-yes flags

> Please note that this is not an official release of APT, and that this program may not include every feature

## Table of Contents:

- [Install](/#install)
- [Uninstall](/#uninstall)
- [Help Text](/#help-text)

### Install:

Install dependencies:

```
emerge -n wget curl dev-python/colorama python3
```

Run these commands:

```
cd /usr/bin
sudo wget https://github.com/XRG2014/apt-for-gentoo/blob/main/apt
sudo curl https://github.com/XRG2014/apt-for-gentoo/blob/main/apt -o apt-get
sudo chmod +x apt
sudo chmod +x apt-get
```

### Uninstall:

(optional) Uninstall dependencies:

```
emerge -Cvn wget curl dev-python/colorama python3
```

Run this command:

```
sudo rm -rfv ~/apt.py
```

### Help Text:

```
usage: apt [--help] [--sync] [-h?] ...
--help, -h, -?:      display help text
--sync:              run "emerge --sync"
install:             install package
remove, autoremove:  remove package
update:              update package
upgrade:             upgrade package
config-update:       update configuration files
unmask:              unmask a package (no arguments)
```
