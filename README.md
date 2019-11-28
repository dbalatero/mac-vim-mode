# mac-vim-mode

This repository contains a bootstrap installer that will set up your Mac with
a global Vim mode that works almost anywhere in the OS.

Exceptions are system inputs marked as secure, such as password fields, or
anything in 1Password.

## Setup

Run this command in your Terminal:

```
bash <(curl -s https://raw.githubusercontent.com/dbalatero/mac-vim-mode/master/installer)
```

If you don't trust the script, please audit it in Github. It should be pretty
straight-forward to read, and doesn't require root/sudo.

## What the script does:

* Installs Hammerspoon
* Sets up your Hammerspoon config directory
* Clones VimMode.spoon
* Sets up a basic config if it doesn't exist

The script is idempotent, so you can run it again and again without
side-effects.

The script is also progressive - it will only setup what is missing. If you
already have Hammerspoon, it will skip it. If you already have the
VimMode.spoon installed, it won't reinstall it.

## Updating your VimMode.spoon version in the future

To update VimMode to the latest code, just use git:

```
cd ~/.hammerspoon/Spoons/VimMode.spoon && git pull
```
