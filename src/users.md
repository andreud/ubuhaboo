# Users

## Show all users

```shell
$ cat /etc/passwd
```

## Current user

```shell
$ id # show current user name, groups
$ su - <username> # switch user
$ sudo su - <username> # switch user without prompt password 
$ sudo -l # show user permissions
```

## User Management

```shell
$ adduser
$ useradd
$ passwd
```

## Show a user groups

```shell
$ groups <username>
```

## Add/Delete user from sudoers file (sudo group)

```shell
$ usermod -aG sudo <username>
```

Or

```shell
$ gpasswd -a <username> sudo
$ gpasswd -d <username> sudo
```