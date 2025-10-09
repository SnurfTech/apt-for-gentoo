# APT for [Gentoo Linux](https://gentoo.org/)
This is a Python wrapper for Gentoo Linux's package manager, Emerge, but it has an interface similar to Debian Linux's package manager, APT. 

> Currently doesn't support the -y or --assume-yes flags, but does include the "unmask" option, which allows you to unmask a package by using vim to open /etc/portage/package.accept_keywords (If you're unsure on how to use this option, then don't use it) 

> Please note that this is not an official release of APT, and that this program may not include every feature and some may be changed or tweaked

## Table of Contents:

- [Install](/#install)
- [Uninstall](/#uninstall)
- [Help Text](/#help-text)

## Install:

Install dependencies:

```
emerge -n net-misc/curl app-editors/vim dev-python/colorama dev-lang/python
```

Install APT:

```
mkdir -p ~/.local/bin
curl -L https://raw.githubusercontent.com/XRG2014/apt-for-gentoo/main/apt -o apt-get
ln -s ~/.local/bin/apt-get ~/.local/bin/apt
chmod +x ~/.local/bin
```

Now, add ```~/.local/bin``` to your PATH environment variable if it is not already there.
```
echo 'export PATH=$PATH:~/.local/bin' >> ~/.profile
```

> If you want, you can replace ```~/.profile``` with something like ```~/.bashrc```.

(optional) Uninstall cURL:

> cURL is no longer needed

```
emerge -Cv net-misc/curl
```

## Uninstall:

(optional) Uninstall dependencies:

> Assuming you didn't uninstall cURL after you finished installing APT. (If you did, then just remove the phrase "net-misc/curl" from the command below.) 

```
emerge -Cv net-misc/curl app-editors/vim dev-python/colorama dev-lang/python
```

Run these commands:

```
rm -f ~/.local/bin/apt ~/.local/bin/apt-get
```

### Help Text:

```
usage: apt [--help] [-h?] ...
-?, -h, --help:      display help text
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
