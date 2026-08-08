# pcs – Personal Command Sheets

A lightweight, topic-organized Linux command-line cheat sheet system.

Each topic is a Markdown file containing the commands **you** actually use, with real examples from your past work. Designed to sit comfortably alongside `man` pages.

## Features

- **Topic-based organization** – one Markdown file per subject (`lxd`, `btrfs`, `git`, …)
- **Personal examples** – capture the exact invocations you have used
- **Tags** – filter topics by tag (`pcs list --tag containers`)
- **Man integration** – `pcs man <cmd>` shows your personal notes first, then a man synopsis
- **Search** – full-text search across every sheet
- **Printable output** – clean text or Markdown ready for printing / PDF
- **Zero external runtime dependencies** (Python ≥ 3.9 stdlib only)
- **XDG compliant** – data lives in `~/.local/share/pcs/sheets/`
- **Starter sheets** included for common sysadmin topics

## Installation

```bash
# From the project root
pip install -e .

# Or just put the package on your PYTHONPATH / install via
python -m pip install .
```

After installation the `pcs` command is available.

You can also run without installing:

```bash
python -m pcs list
```

## Quick start

```bash
# List topics
pcs list
pcs list --tag containers

# View a topic (uses glow/bat/less if available)
pcs show lxd

# Create a new topic
pcs new firewall --tags networking,security

# Add a command + example interactively
pcs add lxd

# Search
pcs search snapshot

# Personal examples + man synopsis
pcs man lxc
pcs man systemctl --full          # also open the full man page

# Which topic contains a command?
pcs which btrfs

# Printable version
pcs print git --format text > git-cheatsheet.txt
pcs print lxd --format md | pandoc -o lxd.pdf   # if you want PDF
```

## Data location

```bash
pcs path
# → /home/you/.local/share/pcs/sheets
```

All topic files are plain Markdown. You can edit them directly, keep them in git, or sync with Nextcloud/DAVx5.

## Markdown format

```markdown
---
tags: [containers, virtualization]
---

# LXD

## lxc list
Show all containers with status.

**Example I used:**
```bash
lxc list --format=table
```

When checking status on the Meerkat.
```

## Environment

- `EDITOR` – used by `pcs edit` and `pcs new --edit` (default: `nano`)
- `PAGER` – fallback pager
- Prefers `glow` → `bat` → `less` for nice rendering

## Extending

The code is deliberately simple (stdlib only) so you can easily add:

- fzf interactive selection
- history capture helpers
- export to HTML / PDF
- Cardano / Fire-department specific topics
- shell completion

Pull requests and local forks welcome.

---

**License:** MIT  
**Author:** Heath D. Robertson
