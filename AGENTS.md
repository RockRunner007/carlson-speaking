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

## Skills
- Reusable system prompts and skills are located in `prompts/skills/`.
- `prompts/skills/toastmasters-coach.md`: Provides coaching on presentation principles.
- `prompts/skills/persona-simulator.md`: Allows role-playing as defined personas for communication practice.
- `prompts/skills/filler-word-counter.md`: Analyzes transcripts for filler words like "um" and "ah".
- `prompts/skills/glance-test-evaluator.md`: Evaluates presentation slides for visual clarity and simplicity.
- `prompts/skills/accessibility-checker.md`: Checks presentations for inclusive design and WCAG compliance.
- `prompts/skills/elevator-pitch-crafter.md`: Helps distill a presentation into a 30-second summary.
- `prompts/skills/narrative-arc-builder.md`: Helps structure a presentation as a compelling story.
- `prompts/skills/post-presentation-follow-up.md`: Helps draft follow-up emails after a presentation.
- `prompts/skills/contingency-planner.md`: Helps prepare for technology failures during a presentation.
- `prompts/skills/speaking-anxiety-coach.md`: Helps manage pre-presentation nervousness.
- `prompts/skills/data-storytelling-assistant.md`: Helps transform raw data into compelling visual stories.
- `prompts/skills/q-and-a-strategist.md`: Helps predict questions and formulate strategic answers.
- `prompts/skills/remote-delivery-coach.md`: Provides a pre-flight checklist for virtual presentations.
- `prompts/skills/stage-choreographer.md`: Provides stage directions for in-person presentations.
- `prompts/skills/vocal-variety-coach.md`: Annotates scripts with cues for pace, pitch, and volume.
- `prompts/skills/feedback-facilitator.md`: Generates targeted questions for a practice audience.
- Agents should check this directory for specialized capabilities (e.g., coaching, reviewing).
- When adopting a skill, adhere strictly to the rules defined in that skill file.

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
