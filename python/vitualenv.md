# Setup Virtual Environment
    $ pip3.5 install virtualenv virtualenvwrapper

add the lines to `~/.profile` or `~/.bashrc`
```
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3.5
export WORK_ON_HOME=$HOME/.virtualenvs
export PROJECT_HOME=$HOME/Dropbox/code
source /usr/local/bin/virtualenvwrapper.sh
```
and than `$ source ~/.bashrc` to reload