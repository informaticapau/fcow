# fcow - command
Version 1.0

## Install
Download debian package from the latest Github Actions workflow run artifact, unzip it, and install with:
```sh
sudo apt install ./fcow_1.0-1.deb
```

## HELP
```
Usage: fcow [options]

By default prints a colored cow with a random fortune message.

Options:
  -r|--random        Makes the cow RANDOM

Examples:
  fcow
  fcow -h|--help
  fcow -v|--version
  fcow -r|--random


You may like execute:
`echo "alias clear='clear && fcow -r'" >> ~/.bash_aliases`

You can edit permanent aliases in "~/.bash_aliases"

```

## Build
Two ways:

1. Making copies:
```sh
mkdir /usr/local/share/fcow
cp src/fcow /usr/local/bin/fcow
cp share/HELP /usr/local/share/fcow/HELP
mkdir /usr/local/man/man6/
cp man/fcow.6 /usr/local/man/man6/fcow.6
```

2. Making symlinks:
```sh
ln -srf src/fcow /usr/local/bin/fcow
mkdir /usr/local/share/fcow
ln -srf share /usr/local/share/fcow
mkdir /usr/local/man/man6/
ln -srf man/fcow.6 /usr/local/man/man6/fcow.6
```
