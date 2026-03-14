# AI Contributor Guidance

This file complements `AGENTS.md` with quick, actionable pointers for AI-powered contributions.

## Quick start for AI agents
1. Read `AGENTS.md` first (single source of truth).
2. Prefer small, safe edits and provide patch-style outputs.
3. Use GitHub CLI for integration:
   - `gh issue create --template bug`
   - `gh issue create --template feature`
   - `gh pr create --title "..." --body "..."`
4. Follow branch protection:
   - Do not push directly to `main`.
   - Create PRs from feature branches.

## Testing commands
- `npm install`
- `npm test`
- `npm run lint`

## Optional tools
- For Cursor: use `.cursorignore`
- For Aider: use `.aider.conf.yml`
- For Gemini: use `.gemini/settings.json`

## CI checks
- `test-and-build` workflow
- `codeql-analysis` workflow
- `dependency-update` workflow
- `security-scan` workflow
