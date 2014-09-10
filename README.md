mavericks-dev-setup
===================

Instruction for setting up dev tools for OS X Mavericks

Mavericks development setup

download/install brew:
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”

install xCode

brew update

brew doctor

brew install python

brew install python3
Caveats
This formula is keg-only, which means it was not symlinked into /usr/local.

Mac OS X provides similar software, and installing this software in
parallel can cause all kinds of trouble.

OS X provides the BSD libedit library, which shadows libreadline.
er to prevent conflicts when programs look for libreadline we are
ting this GNU Readline installation to keg-only.

Generally there are no consequences of this for you. If you build your
own software and it requires this formula, you'll need to add to your
build variables:

    LDFLAGS:  -L/usr/local/opt/readline/lib
    CPPFLAGS: -I/usr/local/opt/readline/include
pip install virtualenv
brew install pyenv
Optional Databases:
brew install mysql
To connect:
    mysql -uroot

To have launchd start mysql at login:
    ln -sfv /usr/local/opt/mysql/*.plist ~/Library/LaunchAgents
Then to load mysql now:
    launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist
Or, if you don't want/need launchctl, you can just run:
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
mkdir [projectname]
 && cd [projectname]
pyvenv env
source env/bin/activate
pip install django
django-admin.py startproject [projectname]
./manage.py startapp [appname]
./manage.py runserver 0.0.0.0:8000








