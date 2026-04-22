# Awesome Git Tutorial

![Git](https://img.shields.io/badge/Git-Tutorial-F05032?logo=git&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-blue)
![Modules](https://img.shields.io/badge/Modules-3-success)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-555)

Hands-on Git tutorial repository covering setup, first commits, and collaboration workflow.

## Overview

This repository is organized as three modules:

1. Install and configure Git
2. Initialize a repository and create commits
3. Work with branches, merge to `main`, and push to remote

The content is designed for practical terminal-first learning with command examples and expected outputs.

## Repository Structure

```text
awesome-git-tutorial/
├── MODULE1.md
├── MODULE2.md
├── MODULE3.md
└── README.md
```

## Modules

### Module 1: Install Git and Configure Identity
File: `MODULE1.md`

Topics covered:
- Installing Git on Linux, macOS, and Windows (WSL path shown)
- Understanding command syntax (`command [options] [arguments]`)
- Configuring Git identity (`user.name`, `user.email`)
- Configuration scopes: system, global, local
- Common configuration updates (`core.editor`, `color.ui`, `init.defaultBranch`)

### Module 2: Initialize a Repo and Make First Commit
File: `MODULE2.md`

Topics covered:
- Running `git init` and inspecting `.git`
- Checking status with `git status`
- Staging with `git add`
- Creating commits with `git commit -m`
- Viewing history with `git log`
- Working with commit hashes, `git show`, `git diff`, and `git revert`

### Module 3: Branch, Merge, and Push
File: `MODULE3.md`

Topics covered:
- Creating and switching branches
- Publishing a branch to remote
- Merging feature work into `main`
- Resolving merge conflicts
- Pushing merged changes to remote

## Prerequisites

- Git installed (`git --version`)
- A terminal (PowerShell, Bash, or similar)
- A GitHub account and repository access for remote workflows

## Quick Start

```bash
git clone git@github.com:hridoynasah/awesome-git-tutorial.git
cd awesome-git-tutorial
```

Then follow modules in order:
1. `MODULE1.md`
2. `MODULE2.md`
3. `MODULE3.md`

## Suggested Practice Flow

1. Create files and commit by module.
2. Keep work on a development branch.
3. Merge into `main` after each module milestone.
4. Push branch and `main` regularly.

## Learning Outcomes

After completing all modules, you should be able to:
- Configure Git correctly for personal and project use.
- Create and inspect commits confidently.
- Use branches for isolated work.
- Merge safely into `main`.
- Push local history to a remote repository.
