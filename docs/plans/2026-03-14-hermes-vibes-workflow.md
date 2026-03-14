# Hermes + Vibes Dual-Repo Workflow

Last updated: 2026-03-14

## Repo Layout

- Hermes fork: `~/Documents/personal/hermes-agent`
- Vibes fork: `~/Documents/personal/vibes-cli`
- Integration lab (tooling, notes): `~/Documents/personal/hermes-vibes-lab`

## Branch Naming

- Hermes: `feature/vibes-<topic>` (e.g., `feature/vibes-autoresearch`)
- Vibes: `feature/hermes-<topic>` (e.g., `feature/hermes-autoresearch`)

Keep branch names short, lowercase, hyphen-separated. One feature per branch.

## Sync Procedure

1. `git checkout main`
2. `git fetch upstream`
3. `git merge upstream/main`
4. Resolve conflicts (if any)
5. `git push origin main`

Repeat in both repos before starting new work and before opening PRs.

## Hackathon Checklist

- Follow conventional commits (`feat`, `fix`, `refactor`, `docs`, `chore`).
- Run `hermes doctor` + `pytest` (Hermes) before requesting validation.
- Run Vibes CLI smoke tests per CONTRIBUTING guidelines.
- Post Discord validation requests before PR (per hermes-fork-dev skill).
- Document new workflows/skills under `docs/` in the relevant repo.

## Cross-Repo Coordination

- Hermes handles orchestration, tools, autoresearch logic.
- Vibes supplies the Fireproof/VibeOS runtime and Claude Code plugin artifacts.
- New shared tooling and experiments live in `~/Documents/personal/hermes-vibes-lab`.

## Future Steps

- Create feature branches in both repos for autoresearch integration.
- Build automation scripts in `hermes-vibes-lab` (Python + TypeScript).
- Reverse engineer Vibes CLI internals and map out integration APIs.
- Design end-to-end demo workflow for hackathon judging.
