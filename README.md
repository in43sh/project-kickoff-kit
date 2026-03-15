# project-kickoff-kit

A starter kit for kicking off collaborative dev projects. Copy what you need into a new repo and go.

## What's inside

### `docs/`
Drop these into the team repo at project start.

| File | Purpose |
| ---- | ------- |
| `CONTRIBUTING.md` | Git workflow — branching, commits, PRs, merge strategy |
| `GIT_GUIDE.md` | Branch naming and commit message conventions |
| `FRONTEND_GUIDE.md` | React + Tailwind best practices and project structure |

### `github/`
GitHub repository ruleset configs. Import via **Settings → Rules → Rulesets → Import**.

| File | Purpose |
| ---- | ------- |
| `main-branch-protection.json` | Locks `main` — requires PR + 1 approval, no direct pushes |
| `dev-branch-protection.json` | Protects `development` — requires PR + 1 approval |

## How to use

1. Create a new GitHub repo for your project
2. Copy `docs/` files into the repo root
3. Import both JSON files via GitHub ruleset settings
4. Share `docs/` links with the team at kickoff
