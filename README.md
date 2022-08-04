# POS OS Software Installation Guide

<b>Initial Updates</b>
```shell
sudo apt update
```
```shell
sudo apt upgrade
```

<b>Grub Installation for dual OS</b>
<p>https://jacci.net/linux/pop-os/how-to-install-grub-on-pop-os-20-04/</p>

```shell
sudo apt install grub-efi grub2-common
```

```shell
sudo grub-install
```

<p>Due to a bad install of grub, it is needed to copy grub.efi to the to the appropriate folder and overwrite. As follows.</p>

```shell
sudo cp /boot/grub/x86_64-efi/grub.efi /boot/efi/EFI/pop/grubx64.efi
```

https://askubuntu.com/questions/761563/ubuntu-16-04-cant-install-grub-customizer

```shell
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
```

```shell
sudo apt-get update
```
```shell
sudo apt-get install grub-customizer
```

<p>open now grub-customizer</p>

```shell
grub-customizer
```

<p>Set this config in grub-cutomizer window:</p>
<p>Change OUTPUT_FILE:</p>
<p>/boot/grub/grub.cfg => /boot/efi/EFI/pop/grub.cfg</p>


<b>Chrome</b>
<p>Download from https://www.google.com/chrome/</p>

<b>VirtualBox</b>
```shell
sudo apt install virtualbox
```

<b>Vagrant</b>

```shell
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
```

```shell
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
```

```shell
sudo apt-get update && sudo apt-get install vagrant
```

<b>Apache2 Installation</b>

```shell
sudo apt install apache2
```

```shell
sudo /etc/init.d/apache2 start
```

<b>Git</b>

```shell
sudo apt-get install git
```

<b>PHP 7.4</b> 
<p>https://tecadmin.net/install-php-ubuntu-20-04/</p>

```shell
sudo apt install software-properties-common ca-certificates lsb-release apt-transport-https 
```
```shell
LC_ALL=C.UTF-8 add-apt-repository ppa:ondrej/php
```

```shell
sudo apt update
```

```shell
sudo apt install php7.4 
```

```shell
sudo apt install php7.4-mysql php7.4-mbstring php7.4-xml php7.4-curl php-common
```

```shell
sudo apt install php-fpm php7.4-fpm php7.2-fpm php5.6-fpm
```

```shell
sudo apt install php-pear
```

```shell
sudo update-alternatives --config php
```

<p>Project folder permission</p>

```shell
/var/www/html$ cd ..
```

```shell
/var/www$ sudo chmod 777 -R html
```

<b>MySQL</b>

```shell
sudo apt update
```

```shell
sudo apt install mysql-server
```

```shell
sudo systemctl start mysql.service
```

<b>Configuring MySQL</b>

```shell
sudo mysql_secure_installation
```
<p>or</p>

```shell
sudo mysql
```

```shell
SELECT user,authentication_string,plugin,host FROM mysql.user;
```

```shell
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```

```shell
FLUSH PRIVILEGES;
```

```shell
SELECT user,authentication_string,plugin,host FROM mysql.user;
```

```shell
exit
```

```shell
sudo mysql_secure_installation
```

<b>PHPMyAdmin</b>

```shell
sudo apt install phpmyadmin
```

<b>SSH Key Generate</b>
<p>https://docs.oracle.com/en/cloud/cloud-at-customer/occ-get-started/generate-ssh-key-pair.html</p>

```shell
ssh-keygen -t rsa
```

```shell
ssh-keygen -b 2048 -t rsa
```

<b>Composer</b>
<p>Download from https://getcomposer.org/download/ latest version file composer.phar</p>

```shell
cd /Downloads
```

```shell
php composer.phar
```

```shell
sudo chmod 755 composer.phar
```

```shell
sudo mv composer.phar /usr/bin/composer
```

<b>Slack</b> 
<p>Dowload from https://slack.com/</p>

<b>PhpStorm</b>
<p>Download from https://www.jetbrains.com/phpstorm/download/#section=linux</p>

```shell
cd /Downloads
```

<p>https://linuxhint.com/install-phpstorm-ubuntu-linux/</p>

```shell
tar -xvf PhpStorm-2020.3.1.tar.gz
```

<p>copy Downloads to Home directory</p>
<p>rename PhpStorm-203.6882.180 to PhpStorm</p>

```shell
cd PhpStorm/bin
```

```shell
./phpstorm.sh
```

<b>Phpstorm plugins:-</b>
<ol>
  <li>.env files support</li>
  <li>.ignore</li>
  <li>Atom Material Icons</li>
  <li>CSV</li>
  <li>Git Flow Integration</li>
  <li>sudo apt-get install git-flow</li>
  <li>Key Promoter X</li>
  <li>PHP Annotation</li>
  <li>PHP Inspection (EA Extended)</li>
  <li>PHP Toolbox</li>
  <li>Rainbow Brackets</li>
  <li>Yii2 Support</li>
</ol>

<b>.htaccess enable</b>
<p>https://www.digitalocean.com/community/tutorials/how-to-rewrite-urls-with-mod_rewrite-for-apache-on-ubuntu-20-04</p>

```shell
sudo a2enmod rewrite
```

```shell
sudo service apache2 restart
```

<p>Open the default Apache configuration file using nano or your favorite text editor.</p>

```shell
sudo cd /etc/apache2/sites-available
```

```shell
sudo nano 000-default.conf
```

<p>Add these below lines and save file.<p>
  
  ```conf
  <VirtualHost *:80>
    <Directory /var/www/html>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
    
    . . .
</VirtualHost>
  ```

  ```shell
  sudo /etc/init.d/apache2 restart
  ```
  

<b>PostMan</b>
<p>Download from https://www.postman.com/downloads/ and install</p>

<b>Desktop Icons</b>
<p>https://linuxhint.com/customize-desktop-pop-os/</p>

```shell
sudo apt install gnome-tweaks
```

```shell
sudo apt install gnome-shell-extensions -y
```

<p>PhpStorm Desktop Icon</p>
<p>Open Text Edit and save below with PhpStorm.desktop</p>

<b>PhpStorm PHP Quality Tools</b>
https://www.jetbrains.com/help/phpstorm/using-php-code-sniffer.html

1. PHP Code Sniffer
   https://github.com/squizlabs/PHP_CodeSniffer
   
2. Mess Detector 
  https://github.com/phpmd/phpmd/releases/tag/2.10.2
  https://phpmd.org/download/index.html

3. Psalm
   https://psalm.dev/docs/running_psalm/installation/
   Config: https://psalm.dev/docs/running_psalm/configuration/

4. PHP Stan
   https://phpstan.org/user-guide/getting-started
   Config: https://phpstan.org/config-reference#config-file

5. PHP CS Fixer
   https://github.com/FriendsOfPHP/PHP-CS-Fixer

<p>After unzip, run composer</p>
```shell
  composer install
```
3. and so on.

```desktop
[Desktop Entry]
Name=PHPStorm
Type=Application
Terminal=false
Icon=/home/{username}/PhpStorm/bin/phpstorm.png
Exec=/home/{username}/PhpStorm/bin/phpstorm.sh
Categories=Development
```

<p>PostMan Desktop Icon<p>
<p>Open Text Edit and save below with PostMan.desktop</p>

```desktop
[Desktop Entry]
Name=PostMan
Comment=PostMan
Keywords=post;chrome;postman
Exec=/home/muslimahmad/Postman/Postman
Icon=/home/muslimahmad/Postman/app/icons/icon_128x128.png
Terminal=false
Type=Application
Categories=softwares
```
