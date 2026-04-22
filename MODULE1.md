# Module 1: Install Git, Learn Command Syntax, and Configure Identity

This module covers installing Git, understanding terminal command structure, and configuring your Git identity.

## 1) Check system requirements

Before installing Git, ensure that you have administrator access to your machine. Git is available for Windows, macOS, and Linux.

## 2) Download Git

Action:
Open the official Git download page and choose the installer for your operating system.

Link:
`https://git-scm.com/install/`

## 3) Install Git on Linux and Windows (WSL)

Command:
```bash
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt install git
```
Output:
```text
(no output)
```

Note: `apt update` refreshes your package list, and `software-properties-common` enables adding repositories. This ensures you install the latest stable Git.

## 4) Install Git on macOS

Command:
```bash
brew update
brew install git
```
Output:
```text
(no output)
```

If you do not have Homebrew installed, install it first at `https://brew.sh`.

## 5) Verify the installation

Command:
```bash
git --version
```
Output:
```text
git version <version-number>
```

Seeing the version confirms Git is installed and ready to use.

## 6) Command syntax basics

The general command format is:
```bash
command [option(s)] [argument(s)]
```

Definitions:
- **Command:** The program you want to run (e.g., `ls`, `echo`, `mkdir`).
- **Options (flags):** Modify how the command runs (e.g., `-l`, `-a`, `--help`).
- **Arguments:** Inputs like filenames or paths (order matters).

Example:
```bash
mkdir my-project
```
Explanation:
- `mkdir` is the command.
- `my-project` is the argument (the directory name).

Example with options:
```bash
ls -la /home/user/documents
```
Explanation:
- `ls` is the command.
- `-la` are the options (list all files in long format).
- `/home/user/documents` is the argument (the directory to list).

# Configuring Git

Before you start using Git, configure it with your personal information. Git uses this to record who made each commit.

## 7) Understand configuration levels

Git has three configuration levels:
1. **System** (`/etc/gitconfig`): Applies to all users and repositories on the machine.
2. **Global** (`~/.gitconfig`): Applies to your user account across all repositories.
3. **Local** (`.git/config`): Applies to a single repository.

Most of the time, you will use global settings.

## 8) Set your identity

Command:
```bash
git config --global user.name "Your Full Name"
```
Output:
```text
(no output)
```

Example:
```bash
git config --global user.name "John Doe"
```

Command:
```bash
git config --global user.email "your.email@example.com"
```
Output:
```text
(no output)
```

Example:
```bash
git config --global user.email "john.doe@example.com"
```

Note: The `--global` flag applies the setting to all repositories for your user account.

## 9) Verify your configuration

Command:
```bash
git config --list
```
Output:
```text
<all configuration values>
```

Command:
```bash
git config --global --list
```
Output:
```text
<global configuration values>
```

Command:
```bash
git config user.name
git config user.email
```
Output:
```text
<configured value>
```

## 10) Update configuration

Command:
```bash
git config --global user.name "New Name"
git config --global user.email "newemail@example.com"
```
Output:
```text
(no output)
```

## 11) Configure a single repository (local)

Command:
```bash
git config user.name "Different Name"
git config user.email "work.email@company.com"
```
Output:
```text
(no output)
```

Note: Without `--global`, the settings apply only to the current repository.

## 12) Other common configuration changes

Set your default text editor:
```bash
git config --global core.editor "nano"
```

Enable colored output:
```bash
git config --global color.ui true
```

Set the default branch name for new repositories:
```bash
git config --global init.defaultBranch main
```

Configure line ending handling:
```bash
git config --global core.autocrlf true
```

Note: On Windows, use `true`. On macOS and Linux, use `input`.

## 13) Remove a configuration setting

Command:
```bash
git config --global --unset user.name
```
Output:
```text
(no output)
```

This removes the global user name configuration, though Git will still require it when making commits.

## 14) View changes again

Command:
```bash
git config --global --list
```
Output:
```text
<global configuration values>
```
