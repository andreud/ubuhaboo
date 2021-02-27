# Server Stack

## Apache

Install and basic conf
```shell
$ apt install apache2
$ nano /etc/apache2/ports.conf
$ nano /etc/apache2/sites-available/000-default.conf
```

## Nginx

Install from Ububtu apt repos

```shell
$ apt install nginx 
$ apt install nginx nginx-extras

# Firewall
$ ufw app list
$ ufw allow 'Nginx HTTP' # Example: allow HTTP profile
$ ufw status

```

[Start](https://www.nginx.com/resources/wiki/start/)

[Config Pitfalls](https://www.nginx.com/resources/wiki/start/topics/tutorials/config_pitfalls/)

Configure
```shell
$ cd /etc/nginx/
$ nginx -t
```

## PHP

### For Apache

### For Nginx

```shell
# Install
$ apt install php-fpm php-mysql		
# PHP config file
$ /etc/php/7.4/fpm/php.ini	
# Manage service
$ service php7.4-fpm restart
```

[SO Thread for probles with some Nginx versions](https://stackoverflow.com/questions/43262435/nginxs-fastcgi-php-conf-snippet-is-missing)


### Composer

```shell
$ cd
$ curl -sS https://getcomposer.org/installer -o composer-setup.php
$ sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```

[DO Article](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-20-04)

## Node, npm, nvm, pm2

Install nodejs

```shell
$ sudo apt update
$ sudo apt install nodejs
$ nodejs -v
$ sudo apt install npm
$ npm -v
```

Install nvm

```shell
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
# To use it, you must first source your .bashrc file:
$ source ~/.bashrc

# Which versions of Node are available:
$ nvm list-remote

# Add and use any node version
$ nvm install v13.6.0
$ nvm use v13.6.0
```

## MySQL

Install & set up

```shell
$ sudo apt install mysql-server
$ sudo mysql_secure_installation
$ sudo mysql
```

By default, mysql's root user can only login by using sudo & implicit password.

Create a database and user:

```
mysql> CREATE DATABASE '<database_name>';
mysql> CREATE USER '<username>'@'%' IDENTIFIED WITH mysql_native_password BY '<password>';
mysql> GRANT ALL ON <database_name>.* TO '<username>'@'%';
mysql> exit;
```

```shell
$ mysql -u{username} -p
```

## Postgres

## Redis

## Supervisor


## Elastic Search

Installing 
```shell
$ curl -fsSL https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
$ echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
$ sudo apt update
$ sudo apt install elasticsearch

# start service
sudo systemctl start elasticsearch
# Next, run the following command to enable Elasticsearch to start up every time your server boots:
sudo systemctl enable elasticsearch
```

Configuring
```shell
$ sudo nano /etc/elasticsearch/elasticsearch.yml
```

[Full Article](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-elasticsearch-on-ubuntu-20-04)

## Docker


