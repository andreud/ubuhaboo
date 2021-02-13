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

### Copy pubkey to server

This allows parrwordless login into this server

```shell
$ ssh-copy-id -i  ~/.ssh/<key_name>.pub  <server-user>@<server-ip>
```
