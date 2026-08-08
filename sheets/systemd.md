---
tags: [services, system]
---

# Systemd

## systemctl status
Show detailed status of a unit.

**Example I used:**
```bash
systemctl status nginx.service
systemctl status --no-pager
```

## systemctl list-units
List failed units only.

**Example I used:**
```bash
systemctl list-units --failed
systemctl --failed
```

## systemctl daemon-reload
Reload unit files after editing a service.

**Example I used:**
```bash
sudo systemctl daemon-reload
sudo systemctl restart myapp.service
```

## journalctl
Follow logs for a specific unit.

**Example I used:**
```bash
journalctl -u nginx.service -f
journalctl -u nginx.service --since "1 hour ago"
```

## systemctl enable
Enable a service to start at boot and start it now.

**Example I used:**
```bash
sudo systemctl enable --now myapp.service
```

## systemctl cat
Show the full unit file content (including drop-ins).

**Example I used:**
```bash
systemctl cat nginx.service
```

## systemd-analyze
Show time spent in each startup phase.

**Example I used:**
```bash
systemd-analyze
systemd-analyze blame | head -20
```
