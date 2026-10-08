# mini-prod-app

## What is this project?
A small simulated production application repository that demonstrates
professional Git practices: config management, health monitoring files,
a proper .gitignore, feature branches, and Pull Requests.

## Project structure
| File | Purpose |
|------|---------|
| `app.txt` | Sample application configuration |
| `health.txt` | Service health information |
| `status.txt` | Deployment status |
| `.gitignore` | Excludes logs, env files, dependencies |

## Setup
```bash
git clone https://github.com/<your-username>/mini-prod-app.git
cd mini-prod-app
cp .env.example .env   # if used; never commit real secrets
```

## How to test
1. Check config: `cat app.txt` and confirm `PORT`, `ENVIRONMENT`, `LOG_LEVEL` are set.
2. Check health: `grep "status:" health.txt` should print `status: healthy`.
3. Check ignore rules: `touch test.log .env && git status` should not list them.

## Git workflow
- `main` holds stable, production-ready code.
- Each change is built on a feature branch (`feature/...`, `hotfix/...`).
- Commits are small and use conventional messages (`feat:`, `fix:`, `docs:`, `chore:`).
- Branches are merged into `main` through Pull Requests.
- Mistakes on `main` are undone with `git revert`, not by rewriting history.

## Production challenge
**What happened:** <I faild the authentication problem with github , e.g. a bad port value was merged and
health.txt showed unhealthy>
**How it was detected:** <e.g. health check status changed>
**How it was fixed:** <e.g. git revert of commit abc123, service restored>
**Lesson learned:** <e.g. review config changes in PRs, keep a health check>
