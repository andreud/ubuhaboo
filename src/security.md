# Security

## SSH

```shell
$ nano /etc/ssh/sshd_config # Config SSH service
$ sudo sytemctl restart ssh
```

```shell
$ ssh-keygen # Create new keypair w/ default params
$ ls ~/.ssh  # List SSH keys for current user
```

Copy pubkey to server

This allows parrwordless login into this server

```shell
$ ssh-copy-id -i  ~/.ssh/<key_name>.pub  <server-user>@<server-ip>
```


## SSL with certbot

https://certbot.eff.org/lets-encrypt/ubuntufocal-nginx

Install certbot

```shell
$ sudo snap install --classic certbot
$ sudo ln -s /snap/bin/certbot /usr/bin/certbot # Only needed if 'certbot' command isnt available after install
```

Get certificate with certbot

Op 1. Get certificate and autoconfigure for nginx
```shell
$ sudo certbot --nginx
```
Op 2. Just get certificate, youll have to cofigure web server manually

```shell
$ sudo certbot certonly --nginx
```

More options for Op 2
```shell
$ sudo certbot certonly -d example.com -w /etc/nginx/letsencrypt/example.com --dry-run
```

Renew
```shell
sudo certbot renew --dry-run
```

You can leave this command in a corn job like this so it renews automatically
```
0 0 1 4 * /snap/bin/certbot renew >/dev/null 2>&1
```
