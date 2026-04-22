# Contributing Guide

Thanks for contributing to this tutorial repository.

This project is beginner-friendly. Small improvements are welcome.

## Ways You Can Contribute

- Fix typos or grammar mistakes.
- Improve explanations in module files.
- Add practical command examples.
- Improve beginner clarity and learning flow.
- Report issues or suggest new module ideas.

## Before You Start

- Read [README.md](./README.md)
- Follow the module order in `modules/`
- Keep changes focused and easy to review

## Contribution Workflow

1. Fork this repository.
2. Clone your fork:

```bash
git clone https://github.com/<your-username>/awesome-git-tutorial.git
cd awesome-git-tutorial
```

3. Add upstream remote:

```bash
git remote add upstream https://github.com/hridoynasah/awesome-git-tutorial.git
```

4. Create a branch:

```bash
git switch -c docs/short-description
```

5. Make your changes.
6. Run a quick check:

```bash
git status
git diff
```

7. Commit with a clear message:

```bash
git add .
git commit -m "Docs: improve Module 2 commit explanation"
```

8. Push to your fork:

```bash
git push -u origin docs/short-description
```

9. Open a Pull Request to `main` in the original repository.

## Pull Request Checklist

- Change is focused and not unrelated.
- Text is beginner-friendly and clear.
- Commands are correct and tested if possible.
- File paths and links are valid.
- PR title and description explain what changed and why.

## Writing Style

- Use simple language.
- Prefer short sections and practical examples.
- Explain why a command is used, not only what it does.

## Sync Your Fork (Optional but Recommended)

```bash
git switch main
git fetch upstream
git merge upstream/main
git push origin main
```

## Need Help?

Open an issue with:

- What you tried
- What you expected
- What happened instead
- Screenshots or command output (if relevant)