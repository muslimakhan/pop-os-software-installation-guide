sudo apt update
sudo apt upgrade

https://jacci.net/linux/pop-os/how-to-install-grub-on-pop-os-20-04/
sudo apt install grub-efi grub2-common

sudo grub-install

Due to a bad install of grub, it is needed to copy grub.efi to the to the appropriate folder and overwrite. As follows.
sudo cp /boot/grub/x86_64-efi/grub.efi /boot/efi/EFI/pop/grubx64.efi

https://askubuntu.com/questions/761563/ubuntu-16-04-cant-install-grub-customizer
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
sudo apt-get update
sudo apt-get install grub-customizer

open grub-customizer

OUTPUT_FILE:
/boot/grub/grub.cfg => /boot/efi/EFI/pop/grub.cfg



Slack 
Chrome
=>All above from sites

VirtualBox
sudo apt install virtualbox

Vagrant 
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt-get update && sudo apt-get install vagrant

phpStorm
download
https://www.jetbrains.com/phpstorm/download/#section=linux
cd /Downloads
https://linuxhint.com/install-phpstorm-ubuntu-linux/
tar -xvf PhpStorm-2020.3.1.tar.gz
copy Downloads to Home directory
rename PhpStorm-203.6882.180 to PhpStorm
cd PhpStorm/bin 
./phpstorm.sh

Desktop Icons
https://linuxhint.com/customize-desktop-pop-os/
sudo apt install gnome-tweaks
sudo apt install gnome-shell-extensions -y

Apache2 Installation
sudo apt install apache2
sudo /etc/init.d/apache2 start

Git 
sudo apt-get install git

PHP 7.4 
https://tecadmin.net/install-php-ubuntu-20-04/
sudo apt install software-properties-common ca-certificates lsb-release apt-transport-https 
LC_ALL=C.UTF-8 add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php7.4 
sudo apt install php7.4-mysql php7.4-mbstring php7.4-xml php7.4-curl php-common
sudo apt install php-fpm php7.4-fpm php7.2-fpm php5.6-fpm
sudo apt install php-pear
sudo update-alternatives --config php


/var/www/html$ cd ..
/var/www$ sudo chmod 777 -R html

MySQL
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql.service

Configuring MySQL
sudo mysql_secure_installation

or 
sudo mysql
SELECT user,authentication_string,plugin,host FROM mysql.user;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
SELECT user,authentication_string,plugin,host FROM mysql.user;
exit
sudo mysql_secure_installation

PHPMyAdmin
sudo apt install phpmyadmin

https://docs.oracle.com/en/cloud/cloud-at-customer/occ-get-started/generate-ssh-key-pair.html
ssh-keygen -t rsa
ssh-keygen -b 2048 -t rsa

Composer 
Download from https://getcomposer.org/download/ latest version file composer.phar
cd /Downloads
sudo mv composer.phar /usr/bin/composer


Phpstorm plugins:-
.env files support
.ignore
Atom Material Icons
CSV
Git Flow Integration
sudo apt-get install git-flow
Key Promoter X
PHP Annotation
PHP Inspection (EA Extended)
PHP Toolbox
Rainbow Brackets
Yii2 Support

