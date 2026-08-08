---
tags: [admin, ubuntu, system]
---

# General Admin

## apt
Update and upgrade in one go (Ubuntu).

**Example I used:**
```bash
sudo apt update && sudo apt full-upgrade -y
```

## dpkg
List installed packages matching a pattern.

**Example I used:**
```bash
dpkg -l | grep -i nginx
apt list --installed | grep -i python
```

## lsblk
Show block devices in a tree with filesystem info.

**Example I used:**
```bash
lsblk -f
lsblk -o NAME,SIZE,FSTYPE,LABEL,MOUNTPOINT
```

## df / du
Human-readable disk usage.

**Example I used:**
```bash
df -hT
du -sh /var/* | sort -h
```

## chmod / chown
Recursive ownership and permission fix.

**Example I used:**
```bash
sudo chown -R heath:heath /home/heath/project
chmod -R u+rwX,g+rX,o-rwx /home/heath/project
```

## tar
Create a compressed archive excluding certain paths.

**Example I used:**
```bash
tar --exclude='./node_modules' --exclude='./.git' -czvf project.tar.gz .
```

## rsync
Sync a directory while preserving permissions and showing progress.

**Example I used:**
```bash
rsync -aAXv --progress /source/ /destination/
```
