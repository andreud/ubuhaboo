# Users

## Show all users

```sh
$ cat /etc/passwd
```

## Current user

```sh
$ id # show current user name, groups
$ su - <username> # switch user
$ sudo su - <username> # switch user without prompt password 
$ sudo -l # show user permissions
```

## User Management

```sh
$ adduser
$ useradd
$ passwd
```

## Show a user groups

```sh
$ groups <username>
```

## Add/Delete user from sudoers file (sudo group)

```sh
$ usermod -aG sudo <username>
```

Or

```sh
$ gpasswd -a <username> sudo
$ gpasswd -d <username> sudo
```