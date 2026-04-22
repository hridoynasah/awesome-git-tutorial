# Module 3: Branching and Everyday Workflow

Goal: create feature branches, merge safely, and understand daily team flow.

## 1) Create a feature branch

From your repo:

```bash
git switch -c feature/add-about
```

## 2) Make changes on the feature branch

```bash
echo "## About\nThis repo is for Git practice." >> README.md
git add README.md
git commit -m "Add About section"
```

## 3) Switch back and merge

```bash
git switch main
git merge feature/add-about
```

If there is no conflict, this is usually fast-forward for simple history.

## 4) Delete merged branch

```bash
git branch -d feature/add-about
```

## 5) Useful branch commands

```bash
git branch
git branch -a
git log --oneline --graph --decorate -n 10
```

## Team-friendly branch naming examples

- `feature/user-profile`
- `fix/login-error`
- `docs/setup-guide`

## Interactive Checkpoint

1. Create a new branch and commit one small change.
2. Merge it back to `main`.
3. Delete the branch after merge.
4. Confirm with `git branch` that only `main` remains.