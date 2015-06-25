Jenkins + BitBucket
===================

    wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
    sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'
    sudo apt-get update
    sudo apt-get install jenkins

    wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add - 
    sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
    sudo apt-get update
    sudo apt-get install xvfb firefox google-chrome-stable nodejs node nodejs-legacy pyvnc2swf vnc4server fluxbox wmctrlbash
    sudo curl -L https://www.npmjs.com/install.sh | sh
    sudo npm install -g phantomjs
    sudo npm install -g github:n1k0/casperjs.git


    sudo apt-get install curl bison build-essential zlib1g-dev libssl-dev libreadline-dev libxml2-dev git-core gawk libyaml-dev libsqlite3-dev sqlite3 autoconf libgdbm-dev libncurses5-dev automake libtool pkg-config libffi-dev
    sudo -Hiu jenkins

Edit `/etc/defaults/jenkins`:

    JAVA_ARGS="-Xmx1048m -XX:MaxPermSize=512m -Djava.awt.headless=true"


Add this:
    [[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm"
to
    ~/.bashrc

Add this:

    rvm_install_on_use_flag=1
    rvm_project_rvmrc=1
    rvm_gemset_create_on_use_flag=1

to ~/.rvmrc


Then install RVM for user 'jenkins'. https://rvm.io/rvm/install
    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
    \curl -sSL https://get.rvm.io | bash -s stable --rails --autolibs=read-fail

