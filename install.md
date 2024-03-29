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
 - [Node](https://nodejs.org/en/download/)
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
 - [Slack](https://slack.com/downloads/mac)
 - [Daisy Disk](https://apps.apple.com/app/daisydisk/id411643860?ign-mpt=uo%3D4&mt=12)
 - [ChessX](https://sourceforge.net/projects/chessx/)
 - [Opera Gx](https://www.opera.com/gx)
 - [jq](https://stedolan.github.io/jq/)

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

    sudo chown -R pepellou /usr/local/lib/node_modules
    sudo chgrp -R admin /usr/local/lib/node_modules

    cd ~/Workspace
    git clone --recursive git@github.com:pepellou/dotfiles.git
    cd dotfiles
    vi install    # redefine any necessary paths at the top of the file
    ./install

    brew install tree

    brew install --cask basictex

    brew install stockfish

    brew install phpunit

    brew install bat

    brew install the_silver_searcher

    npm install --global http-server

    npm install --global gulp-cli

    git clone git@github.com:pepellou/stupid-simple-bash-scripts.git
    cd stupid-simple-bash-scripts
    cp scripts/* /usr/local/bin/

    brew install rbenv
    rbenv init
    curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash
    rbenv install 2.7.2

    npm install -g tldr

    brew install nvm

    npm install -g gatsby-cli

    # for lichess dev:
    brew install sbt
    brew install yarn
    brew tap mongodb/brew
    brew install mongodb-community@4.4
    brew services start mongodb/brew/mongodb-community
    brew install redis
    brew services start redis

    npm i -g gitmoji-cli

    ## Java and Maven

    # Download JDK from https://jdk.java.net/
    cd ~/Downloads
    tar -xvf openjdk-16.0.1_osx-x64_bin.tar.gz
    sudo mv jdk-16.0.1.jdk /Library/Java/JavaVirtualMachines

    # Add these 3 lines to ~/.bashrc and ~/.zshrc
    JAVA_HOME="/Library/Java/JavaVirtualMachines/jdk-16.0.1.jdk/Contents/Home"
    PATH="${JAVA_HOME}/bin:${PATH}"
    export PATH

    # Download Maven from https://maven.apache.org/download.cgi (download the “Binary tar.gz archive”)
    cd ~/Downloads
    tar -xvf apache-maven-3.8.1-bin.tar.gz
    mv apache-maven-3.8.1 ~/Workspace

    # Add these 3 lines to ~/.bashrc and ~/.zshrc
    export M2_HOME="/Users/pepellou/Workspace/apache-maven-3.8.1"
    PATH="${M2_HOME}/bin:${PATH}"
    export PATH

    # Install oh-my-zsh
    wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
    sh install.sh

    # Install Spaceship theme for oh-my-zsh
    git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
    ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

    # Useful plugins for oh-my-zsh
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

    # Funny quotes utilities
    brew install fortune
    brew install cowsay

    # Fuzzy search tool
    git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf && ~/.fzf/install

    # Command-line pomodoro tool
    npm install -g pomd

    # Git Stats
    brew install gnuplot
    cd ~/Workspace
    git clone git://github.com/hoxu/gitstats.git
    ln -s ~/Workspace/gitstats/gitstats /usr/local/bin/gitstats
