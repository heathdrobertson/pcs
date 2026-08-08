---
tags: [vcs, development]
---

# Git

## git status
Show short working-tree status with branch info.

**Example I used:**
```bash
git status -sb
```

## git log
Pretty one-line log with graph.

**Example I used:**
```bash
git log --oneline --graph --decorate -20
```

## git stash
Stash changes including untracked files.

**Example I used:**
```bash
git stash push -u -m "wip: before refactor"
git stash list
git stash pop
```

## git commit
Amend the previous commit (when nothing has been pushed yet).

**Example I used:**
```bash
git commit --amend --no-edit
```

## git rebase
Interactive rebase of the last N commits.

**Example I used:**
```bash
git rebase -i HEAD~5
```

## git remote
Show remotes with fetch/push URLs.

**Example I used:**
```bash
git remote -v
```

## git branch
List local and remote-tracking branches.

**Example I used:**
```bash
git branch -vv
git branch -r
```

## git diff
Show staged changes only.

**Example I used:**
```bash
git diff --cached
```
