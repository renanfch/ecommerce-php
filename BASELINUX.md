Como preparar uma maquina base em linux
Linux Mint

# google chrome
```
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
echo 'deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main' | sudo tee /etc/apt/sources.list.d/google-chrome.list
sudo apt-get update 
sudo apt-get install google-chrome-stable
```

# keeweb 
* Download normal e instalar usando instalador de pacotes

# skype
- Instalar pelo gerenciador de app

# atom beta
```
curl -sL https://packagecloud.io/AtomEditor/atom/gpgkey | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
sudo apt-get update
sudo apt-get install atom-beta
```

# wine
- https://wiki.winehq.org/Ubuntu

# apache
```
sudo apt-get update
sudo apt-get install apache2
sudo a2enmod rewrite
```

# php 7.2
```
sudo apt-get update 
sudo apt-get upgrade
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update 
sudo apt-get install php7.2
sudo apt-get install php-pear php7.2-curl php7.2-dev php7.2-gd php7.2-mbstring php7.2-zip php7.2-mysql php7.2-xml php7.2-soap php7.2-pgsql
```
# php 5.6
```
sudo apt-get remove --purge php5*
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
sudo apt-get install php5.6-common php5.6-cli php5.6 libapache2-mod-php5.6 php5.6-curl php5.6-dev php5.6-gd php5.6-mbstring php5.6-zip php5.6-mysql php5.6-xml php5.6-soap php5.6-pgsql php5.6-mysql
```

# mysql 5.6
- O prestashop não funcionou no mysql 5.7, então instalar o 5.6
```
sudo add-apt-repository 'deb http://archive.ubuntu.com/ubuntu trusty universe'
sudo apt-get update
sudo apt install mysql-server-5.6 * see note below if you get an error
sudo apt install mysql-client-5.6
```
# mysql 5.7
```
https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-18-04
sudo apt-get update
sudo apt-get install mysql-server
mysql_secure_installation
```

# postgresql
```
sudo apt-get update
sudo apt-get install postgresql postgresql-contrib
https://www.digitalocean.com/community/tutorials/como-instalar-e-utilizar-o-postgresql-no-ubuntu-16-04-pt
```

# composer
```
sudo apt-get update
sudo apt-get install curl php-cli php-mbstring git unzip
cd ~
curl -sS https://getcomposer.org/installer -o composer-setup.php
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```

# nodejs & npm
```
sudo apt-get update
sudo chown -R $USER /usr/local (este aqui acho que nao é necessário rodar)
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt-get install -y nodejs
sudo apt-get install -y build-essential
```

# git
```
Para clonar um repositorio
cd /
cd var/www/
sudo chown username: html/ (username é o usario do linux)
cd html/
git clone https://usuariogit@github.com/xpto/xpto.git nomeDaPastaQueSeráCriada/
git branch -a (lista os branch remotos também)
git checkout origin/experimental (para clonar os branchs e ativar)
git checkout experimental (para clonar os branchs e ativar)

```


# Atualizar repositorio laravel
```
cd /
cd var/www/html/pastaRepositorio
composer install
npm install
npm run dev 
ou 
npm run prod
cp .env.example .env
php artisan key:generate

- Operações para criar build
php artisan version:build (atualiza o numero da versão, após algum commit)
```
# Script PHP version switch
```
git clone https://github.com/mauroagr/php-switch-scripts.git troca_php
cd troca_php
./setup.sh
```
- Para mudar de php, use:
```
./run-5.6.sh
./run-7.2.sh
```

# XMIND
INSTALLER
https://github.com/dinos80152/XMind-Linux-Installer
BUG
http://support.xmind.net/customer/portal/questions/17144128-xmind-starts-but-then-is-aborted-just-before-starting-to-run
