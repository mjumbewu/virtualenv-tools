================
Virtualenv Tools
================

Usage
-----

To activate a virtual environment::

    . activate-env path/to/env/

If you have moved an environment, to update it::

    relocate-env newpath/to/env/

Example
~~~~~~~

For example, whenever I start a new project, I run::

    virtualenv .env --no-site-packages
    . activate-env .env

If I rename my project, it usually looks something like this::

    cd ..
    mv oldproject newproject
    cd newproject
    relocate-env .env

Sometimes the relocate can take a while, as it does a find and replace (with 
sed) for all the files in the environment.

Installation
------------

Place ``activate-env`` and ``relocate-env`` in a directory on your $PATH (I put 
mine in $HOME/.bin).  If you don't want to put that pesky ``. `` before each
call to ``activate-env``, you'll need to add an alias to your *.bashrc* file.
For example::

    export PATH=$PATH:~/.bin
    alias activate-env=". activate-env"

