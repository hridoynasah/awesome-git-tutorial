# Module 6: Fork, Clone, Contribute, and Open a Pull Request

Goal: contribute to someone else's repository using the standard GitHub flow.

## Big Picture

1. Fork original repository on GitHub.
2. Clone your fork locally.
3. Create a feature branch.
4. Commit and push changes to your fork.
5. Open a Pull Request (PR) from your fork branch to original repo.

## 1) Fork on GitHub

On the target repository page, click **Fork**.

After forking:

- Original repo is typically called `upstream` in your local setup.
- Your fork is typically `origin`.

## 2) Clone your fork

```bash
git clone https://github.com/<your-user>/<fork-repo>.git
cd <fork-repo>
```

Check remote:

```bash
git remote -v
```

## 3) Add original repository as `upstream`

```bash
git remote add upstream https://github.com/<original-owner>/<original-repo>.git
git remote -v
```

## 4) Sync your fork with upstream

```bash
git switch main
git fetch upstream
git merge upstream/main
git push origin main
```

## 5) Create a feature branch and make changes

```bash
git switch -c feature/fix-typo
```

Edit files, then:

```bash
git add .
git commit -m "Fix typo in docs"
git push -u origin feature/fix-typo
```

## 6) Open Pull Request (PR)

On GitHub (your fork page), click **Compare & pull request**.

Set:

- Base repository: original repo
- Base branch: usually `main`
- Head repository: your fork
- Compare branch: `feature/fix-typo`

Write:

- Clear title
- What changed
- Why it changed
- Screenshots/logs if relevant

Submit PR.

## 7) Update your PR after review comments

```bash
git switch feature/fix-typo
# make requested changes
git add .
git commit -m "Address review feedback"
git push
```

PR updates automatically.

## 8) Keep your fork fresh (routine)

```bash
git switch main
git fetch upstream
git merge upstream/main
git push origin main
```

## Interactive Checkpoint

1. Fork a public repository.
2. Clone your fork and set `upstream`.
3. Open one PR with a small docs/code change.
4. Respond to at least one review comment and push an update.