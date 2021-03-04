# System

## Timezones

```shell
$ timedatectl
```
System timezone is configured by symlinking /etc/localtime to a binary timezone identifier in the /usr/share/zoneinfo dir. Its also written to the /etc/timezone file:

```shell
$ ls -l /etc/localtime
$ cat /etc/timezone
```

Changing timezone

```shell
$ timedatectl list-timezones
$ sudo timedatectl set-timezone <your_time_zone>
```
