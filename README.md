# APT for [Gentoo Linux](https://gentoo.org/)
A Python program, made for Gentoo Linux that uses emerge to install packages, but has an interface similar to the APT package manager from Debian Linux

> Currently doesn't support the -y or --assume-yes flags, but does include the "unmask" option, which allows you to unmask a package by using vim to open /etc/portage/package.accept_keywords (If you're unsure on how to use this option, then don't use it) 

> Please note that this is not an official release of APT, and that this program may not include every feature and some of them may be changed or tweaked

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
usage: apt [--help] [-h?] ...
--help, -h, -?:      display help text
install:             install package
remove, autoremove:  remove package
show:                show details and information about a package
update:              update repositories and ebuilds
upgrade:             upgrade package or everything
full-upgrade:        upgrade everything with no restrictions
search, list:        search for a package using keyword
satify:              update configuration files
unmask:              unmask a package (This option doesn't support arguments, and if your unsure on how to use it, then don't)
```
