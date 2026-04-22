# Module 2: Initialize a Repo and Make Your First Commit

This module walks through creating a Git repository, staging files, committing, and viewing history.

## 1) Initialize a Git repository

Command:
```bash
git init
```
Output:
```text
Initialized empty Git repository in D:/WorkSpace/awesome-git-tutorial/.git/
```

## 2) Verify the repo structure

Command:
```bash
ls -a
```
Output:
```text
.  ..  .git  MODULE1.md  MODULE2.md  README.md
```

Command:
```bash
ls .git
```
Output:
```text
HEAD
branches
config
description
hooks
info
objects
refs
```

## 3) Check repository status

Command:
```bash
git status
```
Output:
```text
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        MODULE1.md
        MODULE2.md
        README.md

nothing added to commit but untracked files present (use "git add" to track)
```

## 4) Stage files (add to the index)

Staging tells Git which changes should be included in the next commit.

Command:
```bash
git add <path-to-file>
```
Output:
```text
(no output)
```

Example:
```bash
git add README.md
```
Output:
```text
(no output)
```

Verify the staged file:
```bash
git status
```
Output:
```text
On branch main

No commits yet

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        MODULE1.md
        MODULE2.md
```

## 5) Commit changes

A commit is a snapshot of the repository at a point in time. Each commit has a message that explains the change.

Command:
```bash
git commit -m "Add README.md"
```
Output:
```text
[main (root-commit) 9fceb02] Add README.md
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```

Note: `-m` stands for "message".

## 6) View commit history

`git --no-pager log -n 3` prints the most recent commits without paging.

Command:
```bash
git --no-pager log -n 3
```
Output:
```text
commit 9fceb021c6f05a9f2e1e8d3a532b9f3f8d2d2e8d
Author: Your Name <you@example.com>
Date:   Tue Jan 19 21:03:00 2026 -0500

    Add README.md
```

### Pager tips

Git uses a pager (like `less`) automatically for long output.

Keys:
- Scroll down: `Enter`
- Scroll up: `b`
- Search: `/text` then `Enter`
- Next match: `n`
- Quit: `q`

Force a pager:
```bash
git log | less
```
Output:
```text
commit 9fceb021c6f05a9f2e1e8d3a532b9f3f8d2d2e8d
Author: Your Name <you@example.com>
Date:   Tue Jan 19 21:03:00 2026 -0500

    Add README.md
```

Disable the pager:
```bash
git --no-pager log
```
Output:
```text
commit 9fceb021c6f05a9f2e1e8d3a532b9f3f8d2d2e8d
Author: Your Name <you@example.com>
Date:   Tue Jan 19 21:03:00 2026 -0500

    Add README.md
```

## 7) Commit hashes (full vs short)

Each commit has a unique 40-character hash. You can safely use the first 7 characters as a shorthand if they are unique in your repo.

Full hash:
`9fceb021c6f05a9f2e1e8d3a532b9f3f8d2d2e8d`
Short hash:
`9fceb02`

View a commit:
```bash
git show 9fceb02
```
Output:
```text
commit 9fceb021c6f05a9f2e1e8d3a532b9f3f8d2d2e8d
Author: Your Name <you@example.com>
Date:   Tue Jan 19 21:03:00 2026 -0500

    Add README.md

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..e69de29
```

Checkout a commit (detached HEAD):
```bash
git checkout 9fceb02
```
Output:
```text
Note: switching to '9fceb02'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

HEAD is now at 9fceb02 Add README.md
```

Revert a commit:
```bash
git revert 9fceb02
```
Output:
```text
[main 4c2a1f0] Revert "Add README.md"
 1 file changed, 1 deletion(-)
 delete mode 100644 README.md
```

Compare commits:
```bash
git diff 9fceb02 HEAD
```
Output:
```text
diff --git a/README.md b/README.md
deleted file mode 100644
index e69de29..0000000
```
