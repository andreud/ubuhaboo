# Users

## Current user

```shell
$ id # show current user name, groups
$ su - <username> # switch user
$ sudo su - <username> # switch user without prompt password 
$ sudo -l # show user permissions
```

## User Management

### Show all users

```shell
$ cat /etc/passwd
```

### Create a user with a home directory: 
(With this method, new user wont get auto-completion nor history by default)
```Shell
$ useradd -m <username>
$ passwd <username> 
<password>

```

Option 2
```shell
$ adduser <username>
```

### Change a user password
```shell
$ passwd <username>
```
### Show a user groups

```shell
$ groups <username>
```

## Add/Delete user from sudoers file (sudo group)

```shell
$ usermod -aG sudo <username>
# Or
$ gpasswd -a <username> sudo
$ gpasswd -d <username> sudo
```