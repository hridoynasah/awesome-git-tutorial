# Module 1: Setup and Git Basics

Goal: install Git, configure your identity, and understand the three Git areas.

## 1) Install Git

- Windows: https://git-scm.com/download/win
- macOS: `brew install git`
- Ubuntu/Debian: `sudo apt update && sudo apt install git -y`

Verify:

```bash
git --version
```

Expected:

```text
git version 2.x.x
```

## 2) Configure your identity (global)

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Check values:

```bash
git config --global --list
```

Optional quality-of-life settings:

```bash
git config --global init.defaultBranch main
git config --global color.ui auto
```

## 3) Understand the 3 Git areas

- Working directory: where you edit files.
- Staging area (index): what will go into the next commit.
- Repository history: saved commits.

Think of it as:

`edit -> stage -> commit`

## 4) First safety checks

```bash
git --help
git status
```

If not in a repo, `git status` will say:

```text
fatal: not a git repository
```

That is normal right now.

## Interactive Checkpoint

1. Run `git --version`.
2. Run `git config --global --list`.
3. Confirm your `user.name` and `user.email` are visible.

If completed, continue to Module 2.