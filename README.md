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
emerge dev-python/colorama
```

Run these commands in the terminal of your choice:

```
cd ~
wget https://github.com/XRG2014/apt-for-gentoo/blob/main/apt.py
```

Now run **ONLY ONE** of commands shown below:

> _This one uses ```~/.bashrc```_:

```
echo 'alias apt="python3 -ub ~/apt.py"' | tee -a ~/.bashrc
```

> _This one uses ```~/.profile```_:

```
echo 'alias apt="python3 -ub ~/apt.py"' | tee -a ~/.profile
```

### Uninstall:

(optional) Uninstall dependencies:

```
emerge -Cv dev-python/colorama
```

Run this command in the terminal of your choice:

```
rm -rfv ~/apt.py
```

Now find this line and remove it in ```~/.bashrc``` or ```~/.profile``` (Which ever file you used to install APT):

> If the line doesn't exist in the file then APT might already be uninstalled

```
alias apt="python3 -ub ~/apt.py"
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
