# Module 2: Create Your First Repo and Commits

Goal: initialize a repo, track files, and create useful commit history.

## 1) Create a practice project

```bash
mkdir git-playground
cd git-playground
git init
```

Check status:

```bash
git status
```

## 2) Create your first file and stage it

```bash
echo "# Git Playground" > README.md
git add README.md
git status
```

You should see `new file: README.md` under "Changes to be committed".

## 3) Make your first commit

```bash
git commit -m "Add initial README"
```

View history:

```bash
git log --oneline
```

## 4) Make a second commit

```bash
echo "Learning Git step by step" >> README.md
git add README.md
git commit -m "Add learning note to README"
```

Inspect what changed:

```bash
git show --stat
```

## 5) Practice unstaging and restaging

```bash
echo "Temporary line" >> README.md
git add README.md
git restore --staged README.md
git status
```

Now stage and commit properly:

```bash
git add README.md
git commit -m "Add temporary line for practice"
```

## Interactive Checkpoint

1. Run `git log --oneline -n 3`.
2. Explain (to yourself) the difference between `git add` and `git commit`.
3. Run `git status` and verify working tree is clean.