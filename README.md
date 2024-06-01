# APT for [Gentoo Linux](https://gentoo.org/)
A Python program, made for Gentoo Linux that uses emerge to install packages, but has an interface similar to the APT package manager from Debian Linux. 

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

Now find this line and remove it in ```~/Documents/.bashrc``` and ```~/Documents/.profile```, or which ever file you used to install APT:

(If the line doesn't exist in a file then you can ignore it and/or go to the next one.)

```
alias apt="python3 -ub ~/apt.py"
```
