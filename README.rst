mavericks-dev-setup
===================

Instruction for setting up dev tools for OS X Mavericks
-------------------------------------------------------
Mavericks development setup:

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

Optional Databases::

    brew install mysql

        To connect:
            mysql -uroot
        To have launchd start mysql at login::
            ln -sfv /usr/local/opt/mysql/*.plist ~/Library/LaunchAgents
        Then to load mysql now::
             launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist
        Or, if you don't want/need launchctl, you can just run::
            mysql.server start

    brew install postgresql
        
        To have launchd start postgresql at login:
            ln -sfv /usr/local/opt/postgresql/*.plist ~/Library/LaunchAgents
        Then to load postgresql now:
            launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist
        Or, if you don't want/need launchctl, you can just run:
            postgres -D /usr/local/var/postgres

    brew install mongodb
        
        To have launchd start mongodb at login:
            ln -sfv /usr/local/opt/mongodb/*.plist ~/Library/LaunchAgents
        Then to load mongodb now:
            launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist
        Or, if you don't want/need launchctl, you can just run:
            mongod --config /usr/local/etc/mongod.conf
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








