# Skills - Agent Guidance

This repository publishes reusable software-development skills as the `engineering`
Claude Code plugin. Skills live in `skills/<skill-name>/SKILL.md`, with supporting
files in each skill's directory. Subagents live in `agents/<name>.md`, with their
configuration in frontmatter and their system prompt in the body. Plugin and
marketplace metadata live in `.claude-plugin/`.

## Project references

- Before authoring or reviewing a skill or agent, read the [design principles](skills/building-skills/SKILL.md#principles).
- Before changing skills, agents, or packaging, read [CONTRIBUTING.md](CONTRIBUTING.md) for
  structure, local development, validation, and updates.
- Read the affected skill or agent and its relevant bundled references.
  Inspect related skills and agents when responsibilities overlap.

This file guides work on the repository; it is not loaded as context with the
installed plugin. Keep each skill's activation cues and essential constraints in
its own `SKILL.md`, with supporting context in its bundled references.
