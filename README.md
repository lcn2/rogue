# Welcome to rogue v5.4.4 modified

This is a fork of [Davidslv's rogue v5.4.4](https://github.com/Davidslv/rogue) modified.

Our port was modified for macOS.  Non-macOS systems that are
Unix-like, have ncurses, have zsh and a C compiler should be able
to compile this code without too much effort.

## Prerequisites

Using [Homebrew](https://brew.sh) we installed ncurses:

```sh
brew install ncurses
```

As of the time this `README.md` was written, we were using ncurses "stable 6.4 (bottled) [keg-only] as Poured from bottle on 2023-01-12 at 19:42:15".

This code assumes that `/bin/zsh` is installed.

## To configure for compiling

NOTE: The default compiler for macOS is clang.  If your non-macOS system has gcc, then omit the "CC=clang" below.

./configure CC=clang CFLAGS="-Wno-deprecated-non-prototype" --with-ncurses --enable-scorefile=.rogue.scr --enable-lockfile=.rogue.lck --enable-wizardmode

## To compile

make clean

make

## To install after compiling

sudo make install

## To uninstall after configuring

sudo make uninstall

### CHANGE LOG

Added this `README.md` file.

Changed the shell to use the default macOS _zsh_.

Changed the "PACKAGE\_BUGREPORT" to _devnull@example.net_.

Fixed a wizard mode code bug.

Turned on wizard mode by default.

Documented in the man page how to enable wizard mode.

Changed the rogue save file to `~/.rogue.save`.

Fixed install-sh to properly set the mode during installation.

Fixed install-sh to properly handle `-g GROUP` and `-o USER`.

Added `-h` to install-sh to be an alias for the `--help` option.

Fixed `make uninstall`.
