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