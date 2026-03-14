# AGENTS.md

This repository uses AGENTS.md as the canonical agent guide according to https://agents.md/

## Purpose
- Provide instructions for AI agents assisting with speaking guidance and markdown content.
- Exactly one `AGENTS.md` in repo root, with optional nested AGENTS.md in subtrees (not required here).
- Include content style and workflow rules for documentation.

## Project context
- Description: A structured markdown collection for providing guidance for speaking.
- Branch policy: direct push to `main` is blocked; all code changes must go through Pull Request and required checks. Use branch naming pattern `scarlson/{feature}` for this workflow.

## Content Style
- Maintain clear, professional, and persona-driven prose.
- Use standard Markdown formatting.

## Governance
- New guidance topics require docs under `specs/`.
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
- Ensure all markdown links are valid.
- Open a PR with a summary of the guidance added and the intended audience/persona.
- Ensure `.github/ISSUE_TEMPLATE` and `README` badges are present.
