# Server Stack

## Apache

```shell
$ apt install apache2
$ nano /etc/apache2/ports.conf
$ nano /etc/apache2/sites-available/000-default.conf
```

## Nginx

```shell
$ apt install nginx 
$ apt install nginx nginx-extras
```

## PHP

### For Apache

### For Nginx

## Node, npm, nvm, pm2

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

