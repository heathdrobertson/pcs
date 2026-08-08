---
tags: [network, ssh, tailscale, vpn]
---

# Networking

## ip addr
Show IP addresses and interfaces (modern replacement for ifconfig).

**Example I used:**
```bash
ip -c addr
ip -br addr
```

## ip route
Show routing table.

**Example I used:**
```bash
ip route show
ip route get 1.1.1.1
```

## ss
Show listening sockets (modern netstat).

**Example I used:**
```bash
ss -tulpn
ss -tlnp | grep :22
```

## tailscale status
Show Tailscale connection status and peers.

**Example I used:**
```bash
tailscale status
tailscale status --json | jq .
```

## tailscale up
Bring Tailscale up with specific flags.

**Example I used:**
```bash
sudo tailscale up --accept-routes --ssh
```

## ssh
SSH with agent forwarding and specific identity.

**Example I used:**
```bash
ssh -A -i ~/.ssh/id_ed25519 user@host
```

## ssh-copy-id
Install public key on a remote host.

**Example I used:**
```bash
ssh-copy-id -i ~/.ssh/id_ed25519.pub user@host
```

## nmap
Quick port scan of a local host.

**Example I used:**
```bash
nmap -sT -O 192.168.1.50
```
