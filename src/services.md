# Services

## List all services

```shell
$ systemctl list-units -t service  --all
```

## Service logs

```shell
$ journalctl -fu <service> # Show a service logs, useful when it doesnt restart
$ journalctl -o json # Show logs in JSON
$ journalctl -p <critic|info|warning|error> # Filter log by message type
$ journalctl --disk-usage # Show all sevices logs size in disk

```

systemctl vs service ?

