# Simple webapp

This is a very basic Python webapp for use as an example in DevOps deployment specifications.

## Usage

Run the app server as follows:

`python3 server.py`

The website should appear on port 8080 on the machine you're running it on. If running locally, view at http://localhost:8080/.

To detach it from the shell and keep it running even if you close your terminal session:

`nohup python3 server.py &`

## Installation on server running Ubuntu20.04

1. Copy _/opt/webapp/webapp.service_ to _/etc/systemd/system/webapp.service_ and set ownership to `root:root` (you may need to reload systemd with `systemctl daemon-reload`).
1. Enable and start service: `systemctl enable webapp ; systemctl start webapp`.
1. Website should appear on port 8080.
1. Logs to _/var/log/messages_ via rsyslog (this can be changed by editing your rsyslog configuration).
