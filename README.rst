Instruction for setting up dev tools for OS X Mavericks
=======================================================

Mavericks development setup:
----------------------------

Make sure xCode is installed

In terminal:

download/install brew::

    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”

    brew update

    brew doctor

    brew install python

    brew install python3

    pip install virtualenv
    
    brew install pyenv

Databases::

    brew install mysql

    brew install postgresql

django
------

Create/start project::

    mkdir [projectname] && cd [projectname]
    pyvenv env
    source env/bin/activate
    pip install django
    django-admin.py startproject [projectname]
    ./manage.py startapp [appname]
    ./manage.py runserver 0.0.0.0:8000








