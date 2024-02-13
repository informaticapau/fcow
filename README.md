# fcow - command
`Version 1.2`

A full colored cow will advice your future

## Install
Download debian package from the latest [Release](https://github.com/informaticapau/fcow/releases), and install with:
```sh
sudo apt install ./fcow_1.2-1.deb
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
ln -srvf src/fcow /usr/local/bin/fcow
mkdir /usr/local/share/fcow
ln -srvf share /usr/local/share/fcow
mkdir /usr/local/man/man6/
ln -srvf man/fcow.6 /usr/local/man/man6/fcow.6
```


## HELP
```
Usage: fcow [options]

By default prints a colored cow with a random fortune message.

Options:
  -r|--random        Makes the cow RANDOM
  -s|--save          Save the last fcow
  -l|--list          List all the saved fcows
  -e|--entry         Select and display an specific entry
  -d|--delentry      Delete an specific entry
  -t|--trans         Specify a language to translate


Examples:
- Display a random fcow
  $ fcow -r
- Display a random fcow in portuguese
  $ fcow -r -t pt
- Save the last fcow as 'pepe'
  $ fcow -s pepe
- Display all saved fcows
  $ fcow -l
- Get and display the saved fcow named 'pepe'
  $ fcow -e pepe
- Remove fcow named 'pepe'
  $ fcow -d pepe


You may like execute:
`echo "alias clear='clear && fcow -r'" >> ~/.bash_aliases`

You can edit permanent aliases in "~/.bash_aliases"
```
