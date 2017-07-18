Install development environment on my mac:
------------------------------------------
These are the steps needed to install my environment, I have to create a script to do it automatically every time is needed, but I don't need it too often, and generally when I need it procedure has changed a bit thanks to Apple :)


1) Install homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"   

2) Install PIP:
sudo easy_install pip

3) Install Virtualenv:
sudo pip install virtualenv

4) Install django on virtualenv
pip install django==1.10
(installs django 1.10, change version as needed)

5) Configure git
git config --global color.ui true 
git config --global user.name "Your name" 
git config --global user.email "your@email.com" 
ssh-keygen -t rsa -C "your@email.com" 

6) Mysql
brew install mysql 
ln -sfv /usr/local/opt/mysql/*plist ~/Library/LaunchAgents 
launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist 

7) Postgresql
brew install postgresql 
ln -sfv /usr/local/opt/postgresql/*plist ~/Library/LaunchAgents 
launchctl load ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist 

8) MongoDB
brew install mongodb

Lately I have not used apache or anything like that anymore, because both Django and Laravel have builtin servers for development.
