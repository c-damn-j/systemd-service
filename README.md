# systemd-service
Create a systemd service to run a command at startup

### Create service

First you need to create a file in the systemd folder

```
sudo nano /etc/systemd/system/goodcommand.service
```
Now paste the following into it:
```
[Unit]

Description=a good description
[Service]

ExecStart=/path/to/command/or/script
[Install]
WantedBy=multi-user.target
```
Reload Systemd
```
sudo systemctl daemon-reload
```
Now enable the service
```
sudo systemctl enable goodcommand.service
```
Congrats!

#gg
