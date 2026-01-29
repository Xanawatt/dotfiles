# My dotfiles

This repository contains the dotfiles I use on all of my systems

## Requirements

You must have the following installed:
- git
- stow

### Manual installation for stow (where you can't use `apt install stow`)
```bash
mkdir -p ~/.local/src ~/.local/bin
cd ~/.local/src
curl -O http://ftp.gnu.org/gnu/stow/stow-latest.tar.gz
tar xf stow-latest.tar.gz
release=$(ls -Avr | grep -m1 -axEe 'stow-[0-9.]+')
cd $release

./configure --prefix ~/.local/stow/$release
make
make install

cd ~/.local/stow
./$release/bin/stow $release
cd ~/.local/src && rm -fr $release stow-latest.tar.gz
```

## Installation

Clone the git repo into your $HOME directory

```
git clone git@github.com:Xanawatt/dotfiles.git .dotfiles
cd .dotfiles
```


