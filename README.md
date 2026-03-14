# Carlson Speaking — Presentation Guidance

A repository for creating and refining presentations on security, work programs, and learning opportunities, using principles from Toastmasters.

## Features

- **Presentation Templates** — Structured templates in `specs/` for building effective presentations on topics like security awareness or program updates.
- **Persona-Based Communication** — Tailored guidance for various stakeholder types in `docs/personas/`.
- **Governance Standards** — Guidelines for reviewing and maintaining high-quality prose in `docs/governance/`.
- **Toastmasters Principles** — Core public speaking concepts adapted for technical and corporate presentations.

## Core Topics
- Security Information Briefings
- Work Program Overviews
- Hosting Learning Opportunities

## Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/stevencarlson/carlson-speaking.git
   ```

2. **Explore Content**
   - Review `prompts/project-context.md` for project details.
   - Check `specs/` for examples of structured guidance.
   - Read `docs/personas/` to understand the communication angles.

## Personas

This repo includes stakeholder personas for guided communication and AI prompts:

- **The Boss** — Business/executive perspective.
- **The Irrational** — Emotional/reactive perspective.
- **The Herd** — Team/consensus perspective.
- **The Cynic** — Critical/skeptical perspective.

See `docs/personas/` for details on how to use these in prompts (e.g., "You are the 'Boss' persona...").

## AI Integration

This repository is designed to be AI-friendly:
- `AGENTS.md` serves as the primary instruction file for AI agents.
- `prompts/` contains context files to help LLMs understand the project scope.
  - `prompts/skills/toastmasters-coach.md`: System prompt for presentation coaching.
  - `prompts/skills/persona-simulator.md`: System prompt for role-playing audience personas.
  - `prompts/skills/filler-word-counter.md`: System prompt for counting filler words in a transcript.
  - `prompts/skills/glance-test-evaluator.md`: System prompt for evaluating slide design for clarity.
  - `prompts/skills/accessibility-checker.md`: System prompt for inclusive design checks.
  - `prompts/skills/elevator-pitch-crafter.md`: System prompt for crafting a 30-second summary.
  - `prompts/skills/narrative-arc-builder.md`: System prompt for structuring a presentation as a story.
  - `prompts/skills/post-presentation-follow-up.md`: System prompt for drafting follow-up emails.
  - `prompts/skills/contingency-planner.md`: System prompt for planning for technology failures.
  - `prompts/skills/speaking-anxiety-coach.md`: System prompt for managing presentation nerves.
  - `prompts/skills/data-storytelling-assistant.md`: System prompt for data storytelling and chart optimization.
  - `prompts/skills/q-and-a-strategist.md`: System prompt for Q&A preparation and bridging techniques.
  - `prompts/skills/remote-delivery-coach.md`: System prompt for virtual presentation setup.
  - `prompts/skills/stage-choreographer.md`: System prompt for planning stage movement and anchoring.
  - `prompts/skills/vocal-variety-coach.md`: System prompt for annotating scripts for vocal delivery.
  - `prompts/skills/feedback-facilitator.md`: System prompt for generating questions for a dry run.
- Specific agent entrypoints exist for tools like Cursor, Gemini, and GitHub Copilot.

## Contributing

We welcome contributions to improve speaking guidance!
- Open a PR or issue to suggest improvements.
- See CONTRIBUTING.md for guidelines.

## License & Maintainer

- **License:** MIT License. See LICENSE for details.
- **Maintainer:** @stevencarlson

---

**Status:** Active guidance collection.
