# Git Workflow Guide

## Branch structure

| Branch | Purpose |
| --- | --- |
| `main` | Production. Never commit directly. |
| `development` | Default working branch. All feature PRs merge here. |
| `feature/*` | Your day-to-day work branches. |

---

## Day-to-day workflow

### 1. Start from a fresh development

Always base your work on the latest `development`:

```bash
git checkout development
git pull origin development
```

### 2. Create a feature branch

Name it after what you're building:

```bash
git checkout -b feature/your-feature-name
```

Good branch names: `feature/user-auth`, `fix/header-layout`, `chore/update-deps`

### 3. Make your changes

Work in small, focused commits. Each commit should do one thing:

```bash
git add path/to/changed-file.js
git commit -m "feat: describe what you did"
```

**Avoid `git add .`** — it's easy to accidentally commit secrets, build artifacts, or unrelated files. Add files explicitly or by folder.

**Before staging, always review what you're about to commit:**

```bash
git status
```

Watch out for files that should never be committed:

| File / pattern | Why |
| --- | --- |
| `.env` | Contains secrets — API keys, tokens, passwords |
| `dist/`, `build/`, `out/` | Build output — generated, not source |
| `node_modules/` | Dependencies — installed from package.json |
| `.DS_Store` | macOS metadata — irrelevant to the project |
| `*.log` | Log files — local noise |
| Any one-time config or setup files | If it's not part of the codebase, it doesn't belong |

These should be covered by `.gitignore`, but `git status` is your last line of defense.

Commit message prefixes:

- `feat:` — new feature
- `fix:` — bug fix
- `chore:` — maintenance (deps, config)
- `refactor:` — code change without behavior change
- `docs:` — documentation only

### 4. Keep your branch up to date

If `development` got new commits while you were working, rebase to stay current:

```bash
git fetch origin
git rebase origin/development
```

Resolve any conflicts, then continue:

```bash
git rebase --continue
```

### 5. Push your branch

```bash
git push origin feature/your-feature-name
```

If you rebased after already pushing, you'll need to force push (safe on your own feature branch):

```bash
git push origin feature/your-feature-name --force-with-lease
```

### 6. Open a Pull Request

- **Base branch:** `development` (not `main`)
- **Title:** short and descriptive — same style as commit messages
- **Description:** what changed and why, plus any testing notes
- Request a review from a teammate

### 7. Get approval and merge

- Address all review comments
- Once approved, **squash and merge** to keep `development` history clean
- Delete the feature branch after merging

---

## Releasing to production

When `development` is stable and ready to ship:

1. Open a PR from `development` → `main`
2. Title it: `release: YYYY-MM-DD` or describe what's going out
3. Get approval, then merge

---

## Rules

- Never commit directly to `development` or `main`
- Never commit secrets or `.env` files
- Don't merge your own PR without a review (unless explicitly agreed)
- Keep PRs small — easier to review, less risk
