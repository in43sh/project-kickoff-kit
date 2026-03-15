# project-kickoff-kit

A starter kit for kicking off collaborative dev projects. Copy what you need into a new repo and go.

## What's inside

### `docs/`

Drop these into the team repo at project start.

| File | Purpose |
| ---- | ------- |
| `SETUP.md` | Onboarding — clone, install, env setup, run locally |
| `CONTRIBUTING.md` | Git workflow — branching, commits, PRs, merge strategy |
| `GIT_GUIDE.md` | Branch naming and commit message conventions |
| `FRONTEND_GUIDE.md` | React + Tailwind best practices and project structure |

### `github/`

GitHub repository ruleset configs. Import via **Settings → Rules → Rulesets → Import**.

| File | Purpose |
| ---- | ------- |
| `main-branch-protection.json` | Locks `main` — requires PR + 1 approval, no direct pushes |
| `dev-branch-protection.json` | Protects `development` — requires PR + 1 approval |

### `.github/`

Drop into the repo root — GitHub picks these up automatically.

| File | Purpose |
| ---- | ------- |
| `pull_request_template.md` | Pre-fills PR description with a standard checklist |
| `ISSUE_TEMPLATE/bug_report.md` | Structured bug report form |
| `ISSUE_TEMPLATE/feature_request.md` | Structured feature request form |
| `workflows/ci.yml` | Runs lint + tests on every PR to `main` or `development` |

### Config files

| File | Purpose |
| ---- | ------- |
| `.gitignore` | Ignores `node_modules`, build output, `.env`, OS files |
| `.eslintrc.json` | ESLint rules for React + hooks |
| `.prettierrc` | Prettier formatting defaults |

## How to use

1. Create a new GitHub repo for your project
2. Copy `docs/` files into the repo root
3. Copy `.github/` into the repo root
4. Copy `.gitignore`, `.eslintrc.json`, and `.prettierrc` into the repo root
5. Import the `github/` JSON files via **Settings → Rules → Rulesets → Import**
6. Share `docs/` links with the team at kickoff
