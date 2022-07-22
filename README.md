# Gophish-Daemon
> Daemon for gophish service

-----------------

`nano /etc/systemd/system/gophish.service`

> Add these lines in the gophish.service file  
> Do not forget to change the directories

```
[Unit]
Description=Gophish Server
After=network.target
StartLimitIntervalSec=0
[Service]
Type=simple
User=root
WorkingDirectory=/root/gophish
ExecStart=/root/gophish/gophish

[Install]
WantedBy=multi-user.target`
```

```
systemctl daemon-reload
systemctl start gophish
```
