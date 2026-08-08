---
tags: [filesystem, storage, snapshots]
---

# Btrfs

## btrfs subvolume list
List all subvolumes under a path.

**Example I used:**
```bash
sudo btrfs subvolume list /
sudo btrfs subvolume list -t /mnt/data
```

## btrfs subvolume snapshot
Create a read-only or read-write snapshot.

**Example I used:**
```bash
sudo btrfs subvolume snapshot -r /home /snapshots/home-$(date +%Y%m%d)
```

## btrfs filesystem usage
Show detailed space usage for a Btrfs filesystem.

**Example I used:**
```bash
sudo btrfs filesystem usage /
sudo btrfs filesystem df /
```

## btrfs filesystem show
List all Btrfs filesystems and their devices.

**Example I used:**
```bash
sudo btrfs filesystem show
```

## btrfs device stats
Show device error statistics (useful after disk issues).

**Example I used:**
```bash
sudo btrfs device stats /
```

## btrfs balance start
Rebalance data/metadata across devices (RAID1 etc.).

**Example I used:**
```bash
sudo btrfs balance start -dusage=50 -musage=50 /
```

## btrfs scrub start
Start a data integrity scrub.

**Example I used:**
```bash
sudo btrfs scrub start /
sudo btrfs scrub status /
```

## btrfs send / receive
Efficiently send a snapshot to another location (or machine).

**Example I used:**
```bash
sudo btrfs send /snapshots/home-20260801 | sudo btrfs receive /mnt/backup/
```
