# AGENTS.md

This repository uses AGENTS.md as the canonical agent guide according to https://agents.md/

## Purpose
- Provide project-specific agent instructions in a machine-readable human-friendly markdown.
- Exactly one `AGENTS.md` in repo root, with optional nested AGENTS.md in subtrees (not required here).
- Include setup, test, code style, and workflow rules.

## Project context
- Repository: `RockRunner007/template`
- Description: secure spec-driven template for internal service projects.
- Branch policy: direct push to `main` is blocked; all code changes must go through Pull Request and required checks. Use branch naming pattern `scarlson/{feature}` for this workflow.

## Build & test
- `npm install` (or chosen language-specific install)
- `npm test` or `./scripts/test` (adjust for your stack)
- CI workflows:
  - `.github/workflows/test-and-build.yml`
  - `.github/workflows/codeql-analysis.yml`
  - `.github/workflows/dependency-update.yml`
  - `.github/workflows/security-scan.yml`

## Code style
- Maintain existing repository conventions and lints.
- Prefer small patches and explicit file path references.

## Governance
- New features require spec docs under `specs/`.
- Create issues with `.github/ISSUE_TEMPLATE` templates.
- Use `.github/pull_request_template.md` for PR metadata.

## How agents should use these files
- The closest `AGENTS.md` in the path wins.
- If a subdirectory has custom guidance, that file applies to edits in that subtree.
- Non-standard files (`agent.md`, `claude.md`, etc.) are optional helpers for custom workflows.

## Cross-agent wrappers
- `agent.md` is a generic instruction set (the one we maintain here).
- `claude.md`, `cursor.md`, `codex.md`, `pilot.md` are model-specific entry points that refer to this file.

## QA & final run
- Run `npm test` (or equivalent) until all checks pass.
- Open a PR with summary, testing details, and compliance to security/code policy.
- Ensure `.github/ISSUE_TEMPLATE` and `README` badges are present.
