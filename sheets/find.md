---
tags: [files, search]
---

# Find & Locate

## find
Find files modified in the last 7 days under a directory.

**Example I used:**
```bash
find /var/log -type f -mtime -7 -ls
```

## find (delete)
Find and delete files older than 30 days matching a pattern.

**Example I used:**
```bash
find /tmp -name "*.tmp" -mtime +30 -delete
```

## find (size)
Find large files (>100 MB).

**Example I used:**
```bash
find /home -type f -size +100M -exec ls -lh {} \;
```

## locate
Fast file name search (requires updatedb).

**Example I used:**
```bash
locate -i "config.yaml"
sudo updatedb
```

## fd
Modern find alternative (if installed).

**Example I used:**
```bash
fd -e md -e txt
fd --type f --changed-within 2weeks
```

## grep -r
Recursive content search with line numbers and color.

**Example I used:**
```bash
grep -rn --color=auto "TODO" .
rg "TODO"   # if ripgrep is installed
```
