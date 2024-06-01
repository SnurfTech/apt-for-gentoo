# Node.js for iOS/iPadOS [a-Shell](https://holzschu.github.io/a-Shell_iOS)
A [Node.js](https://nodejs.org)-like program that I coded for iOS/iPadOS a-Shell. It uses the jsc command, and it includes a fake [NVM](https://github.com/nvm-sh/nvm) (Node Version Manager).

Coded in Python.

### Install:

Install dependencies:

```
pip install colorama
```

Run these commands in a-Shell:

```
mkdir -p ~/Documents/.nvm/bin
curl https://github.com/XRG2014/Node.js-a-Shell/blob/main/.nvm/bin/nvm.py -o ~/Documents/.nvm/bin/nvm.py
curl https://github.com/XRG2014/Node.js-a-Shell/blob/main/.nvm/bin/node.py -o ~/Documents/.nvm/bin/node.py
```

Now run **ONLY ONE PAIR** of commands shown below:

> _This one uses ```~/Documents/.bashrc```_:

```
echo 'alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"' | tee -a ~/Documents/.bashrc
echo 'alias node="python3 -ub ~/Documents/.nvm/bin/node.py"' | tee -a ~/Documents/.bashrc
```

> _This one uses ```~/Documents/.profile```_:

```
echo 'alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"' | tee -a ~/Documents/.profile
echo 'alias node="python3 -ub ~/Documents/.nvm/bin/node.py"' | tee -a ~/Documents/.profile
```

### Uninstall:

(optional) Uninstall dependencies:

```
pip uninstall colorama
```

Run this command in a-Shell:

```
rm -rfv ~/Documents/.nvm
```

Now find these lines and remove them in ```~/Documents/.bashrc``` and ```~/Documents/.profile```, or which ever one you used to install Node.js:

(If the lines don't exist in a file then you can ignore it and go to the next one.)

```
alias nvm="python3 -ub ~/Documents/.nvm/bin/nvm.py"
alias node="python3 -ub ~/Documents/.nvm/bin/node.py"
```
