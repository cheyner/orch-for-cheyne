# Orchestration jump-start for Cheyne

[![asciicast](https://asciinema.org/a/d0affob0jp2op4yg35aqjj2ea.png)](https://asciinema.org/a/d0affob0jp2op4yg35aqjj2ea)

You need some dependencies:

    brew cask install virtualbox
    brew cask install vagrant
    brew cask install vagrant-manager
    brew install ansible
    vagrant plugin install landrush

Then, update ./roles/web-php/defaults/main.yml as necessary.

Finally, run:

    vagrant up