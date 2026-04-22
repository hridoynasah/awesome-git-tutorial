# Module 3: Branching, Merging, and Pushing to Remote

This module explains how to work safely on branches, merge to `main`, and publish your work to a remote repository.

## 1) Check your current branch

Command:
```bash
git branch
```
Output:
```text
* dev
  main
```

## 2) Create a feature branch

Command:
```bash
git switch -c feature/module3
```
Output:
```text
Switched to a new branch 'feature/module3'
```

Alternative (older syntax):
```bash
git checkout -b feature/module3
```

## 3) Make and commit your changes

Command:
```bash
git add MODULE3.md README.md
git commit -m "Complete module 3 and refresh README"
```
Output:
```text
[feature/module3 <hash>] Complete module 3 and refresh README
 2 files changed, <n> insertions(+)
```

## 4) Push the branch to remote

Command:
```bash
git push -u origin feature/module3
```
Output:
```text
Branch 'feature/module3' set up to track remote branch 'feature/module3' from 'origin'.
```

The `-u` flag sets upstream so future pushes can use just `git push`.

## 5) Merge branch into main

Command:
```bash
git switch main
git pull origin main
git merge feature/module3
```
Output:
```text
Updating <old>..<new>
Fast-forward
 MODULE3.md | ...
 README.md  | ...
```

If your merge is not fast-forward, Git will create a merge commit.

## 6) Push merged changes

Command:
```bash
git push origin main
```
Output:
```text
To github.com:<user>/<repo>.git
   <old>..<new>  main -> main
```

## 7) Resolve conflicts (if needed)

When both branches edit the same lines, Git stops and marks conflicts.

Command:
```bash
git status
```
Output:
```text
both modified: <file>
```

Fix conflict markers in the file:
```text
<<<<<<< HEAD
content from main
=======
content from branch
>>>>>>> feature/module3
```

Then finish merge:
```bash
git add <file>
git commit
```

## 8) Clean up merged branches

Delete local merged branch:
```bash
git branch -d feature/module3
```

Delete remote branch:
```bash
git push origin --delete feature/module3
```

## 9) Verify final state

Command:
```bash
git branch -a
git --no-pager log --oneline -n 10 --graph --decorate
```
Output:
```text
* main
  dev
  remotes/origin/main
```
