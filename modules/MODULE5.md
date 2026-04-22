# Module 5: Remotes and Pulling from Local Repositories

Goal: learn remote basics and how to pull from another local repository path.

## 1) Understand `origin`

- `origin` is just a remote name.
- A remote can be GitHub URL or local folder path.

List remotes:

```bash
git remote -v
```

## 2) Add a GitHub remote (normal case)

```bash
git remote add origin https://github.com/<your-user>/<your-repo>.git
git push -u origin main
```

## 3) Pull latest changes

```bash
git pull origin main
```

## 4) Pull from another local repository (important)

Scenario: teammate has a local repo in `D:/repos/teammate-project` and you want to pull from it.

Add that local repo as remote:

```bash
git remote add teammate D:/repos/teammate-project
```

Fetch and inspect branches:

```bash
git fetch teammate
git branch -a
```

Pull teammate main into your current branch:

```bash
git pull teammate main
```

You can also merge explicitly after fetch:

```bash
git fetch teammate
git merge teammate/main
```

## 5) Remove or update remotes

Remove a remote:

```bash
git remote remove teammate
```

Change remote URL/path:

```bash
git remote set-url origin https://github.com/<your-user>/<your-repo>.git
```

## Interactive Checkpoint

1. Add a local-path remote.
2. Run `git fetch <remote-name>`.
3. Pull one branch from that remote.
4. Verify with `git log --oneline --graph --decorate -n 10`.