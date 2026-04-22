# Module 4: Merge Conflicts (Guided Lab)

Goal: intentionally create a conflict, resolve it, and complete the merge.

## Lab Setup

Start from your practice repo on `main`.

```bash
git switch main
```

Create a file:

```bash
echo "App title: Git Playground" > app.txt
git add app.txt
git commit -m "Add app title"
```

## 1) Create branch A and edit same line

```bash
git switch -c feature/change-title-a
```

Edit `app.txt` so line 1 becomes:

```text
App title: Git Playground A
```

Commit:

```bash
git add app.txt
git commit -m "Change title in branch A"
```

## 2) Create branch B from main and edit same line differently

```bash
git switch main
git switch -c feature/change-title-b
```

Edit `app.txt` so line 1 becomes:

```text
App title: Git Playground B
```

Commit:

```bash
git add app.txt
git commit -m "Change title in branch B"
```

## 3) Trigger the conflict

Merge branch A into branch B:

```bash
git merge feature/change-title-a
```

Expected:

```text
CONFLICT (content): Merge conflict in app.txt
Automatic merge failed; fix conflicts and then commit the result.
```

## 4) Resolve conflict manually

Open `app.txt`. You will see markers like:

```text
<<<<<<< HEAD
App title: Git Playground B
=======
App title: Git Playground A
>>>>>>> feature/change-title-a
```

Replace with the final line you want, for example:

```text
App title: Git Playground A and B
```

Then complete merge:

```bash
git add app.txt
git commit -m "Resolve merge conflict in app title"
```

## 5) Verify result

```bash
git log --oneline --graph --decorate -n 10
git status
```

## Interactive Checkpoint

1. Explain why conflict happened (same line changed in two branches).
2. Resolve conflict without deleting accidental content.
3. Complete merge commit successfully.