---
tags: [containers, virtualization, lxc]
---

# LXD

## lxc list
Show all containers/VMs with status, IPv4, and type.

**Example I used:**
```bash
lxc list --format=table
```

Quick status check on the Meerkat or remote LXD hosts.

## lxc launch
Create and start a new container from an image.

**Example I used:**
```bash
lxc launch ubuntu:24.04 myapp --storage default --network lxdbr0
```

## lxc exec
Run a command inside a running container.

**Example I used:**
```bash
lxc exec myapp -- bash
lxc exec myapp -- systemctl status nginx
```

## lxc file push
Copy a file from the host into a container.

**Example I used:**
```bash
lxc file push ./config.yaml myapp/etc/myapp/config.yaml
```

## lxc config set
Set a configuration key on a container or profile.

**Example I used:**
```bash
lxc config set myapp limits.memory 2GB
lxc config set myapp security.nesting true
```

## lxc snapshot
Create a snapshot of a container.

**Example I used:**
```bash
lxc snapshot myapp before-upgrade
lxc info myapp | grep -A20 Snapshots
```

## lxc restore
Restore a container from a snapshot.

**Example I used:**
```bash
lxc restore myapp before-upgrade
```

## lxc image list
List available images (local + remote).

**Example I used:**
```bash
lxc image list ubuntu: | grep 24.04
```
