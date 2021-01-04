# Things that I install on a new computer

This checklist makes it faster to set up a new computer for me.
It's based on MacOS, since that seems to be the trend for my last computers.

## Apps

 - [Alacritty](https://github.com/alacritty/alacritty/releases)
 - [Chrome](https://www.google.com/chrome/)
 - [XCode](https://apps.apple.com/us/app/xcode/id497799835)
 - [Skype](https://go.skype.com/mac.download)
 - [Composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos)
 - [brew.sh](https://brew.sh/#install)
 - [Gimp](https://www.gimp.org/downloads/)
 - [Spotify](https://www.spotify.com/us/download/mac/)
 - [Alfred](https://www.alfredapp.com/)
 - [Discord](https://discord.com/api/download?platform=osx)
 - [Docker Desktop](https://docs.docker.com/docker-for-mac/install/)
 - [DBVis](https://www.dbvis.com/download/)
 - [Telegram](https://telegram.org/dl/macos)
 - [Opera](https://www.opera.com/computer/thanks?ni=stable&os=mac)
 - [YACReader](https://www.yacreader.com/downloads)
 - [Calibre](https://calibre-ebook.com/download_osx)

## Adjust System Preferences

    > Dock
    ....Position on screen: left
    ........ Automatically hide and show the dock
    > Desktop & Screensaver
    .... Screensaver
    ........ Hot corners
    ............ top right > Lock Screen
    ............ bottom left > Desktop
    ............ bottom right > Mission Control

## Command line tools

    brew install stow
    cd ~/Workspace
    git clone --recursive https://github.com/pepellou/dotfiles.git
    cd dotfiles
    stow bash
    stow git
    stov vim
    vim
    (in vim) :BundleInstall!

    brew install --cask basictex

    brew install stockfish

    brew install phpunit

    brew install bat

    brew install the_silver_searcher
