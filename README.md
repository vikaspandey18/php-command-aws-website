# php-command-aws-website
This are list of command for uploading php website on the aws ec2 instance with mysql

# Update apt
sudo apt-get update

# Install MySQL
sudo apt-get install mysql-server

# MySQL Secure Installation
sudo mysql_secure_installation
This will generate the password to login in shell into mysql
username = root
password = admin@456

# Install Apache
sudo apt-get install apache2

# Install PHP
sudo apt-get install php libapache2-mod-php

# Restart Apache
sudo systemctl restart apache2

# Install phpMyAdmin
sudo apt-get install phpmyadmin php-mbstring

# Enable phpMyAdmin
sudo a2enconf phpmyadmin.conf

# Fix if previous command is giving an error
sudo ln -s /etc/phpmyadmin/apache.conf /etc/apache2/conf-available/phpmyadmin.conf

sudo a2enconf phpmyadmin.conf

# Restart apache2
sudo systemctl restart apache2

# Login Mysql
sudo mysql

# Change phpMyAdmin Password
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'StrongP@ssw0rd!';

# Disable phpMyAdmin
sudo a2disconf phpmyadmin.conf

sudo systemctl restart apache2

# Enable File Permission
sudo chown ubuntu /var/www/html

# Free SSL
sudo apt install certbot python3-certbot-apache

sudo certbot --apache -d test.domain.com -d www.test.domain.com


