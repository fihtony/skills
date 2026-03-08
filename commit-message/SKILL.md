---
name: commit-messages
description: Generate conventional commit messages from git diffs. Use when the user asks for a commit message, or when reviewing staged changes for commit.
---

# Commit Message Format

## Format

Use Conventional Commits:

```
<type>(<scope>): <short description>

[optional body]
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`.

## Steps

1. Run `git diff --staged` (or `git status`) to see changes.
2. Infer type and scope from file paths and diff content.
3. Write a short, imperative subject line (e.g. "add login" not "added login").
4. If the change is non-trivial, add a brief body.

## Examples

- Changes in `src/auth/` → `feat(auth): ...`
- Fix in `api/users.py` → `fix(api): ...`
- Docs only → `docs: ...`
