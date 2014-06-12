# Sublime Text 3 Dotfiles

Yup, it's mah subime config.

## Installation
Install instructions. Cause I'm nice. Fix the path if you're not on OSX.

    # CONFIGURATION
    sublime_data_dir="$HOME/Library/Application Support/Sublime Text 3"
    sublime_dotfiles_url="git@github.com:nfarrar/dotfiles-sublime-text-3.git"

    # git fetch files into the existing sublime data directory
    cd $sublime_data_dir
    git init
    git remote add origin $sublime_dotfiles_url
    git fetch origin

    # checkout master
    git checkout -b master --track origin/master

    # init & update the package control submodule
    git submodule init
    git submodule update

## Bonus Round

1. Fork the repo, modify configs and track your changes. Win.
2. Install myrepos, register the repo, and automate your setup.
3. Install alfred2 & the sublime-project workflow. Sexytime.

Register with myrepos:

    brew install myrepos
    cd "$HOME/Library/Application Support/Sublime Text 3"
    mr register

And add the following to $HOME/.mrconfig:

    [Library/Application Support/Sublime Text 3]
    checkout =
        cd "$HOME/Library/Application Support/Sublime Text 3"
        git init
        git remote add origin "git@github.com:nfarrar/dotfiles-sublime-text-3.git"
        git fetch origin
        git checkout -b master --track origin/master
        git submodule init
        git submodule update

## LICENSE

 AYFKMWTS. 

