# Engineering skills

The `engineering` Claude Code plugin provides seven skills for software development:

- [shaping](skills/shaping/SKILL.md): shapes rough, solved, bounded solutions before
  implementation.
- [implementing](skills/implementing/SKILL.md): implements agreed work through
  emergent scopes, architectural refinement, and independent verification.
- [naming-things](skills/naming-things/SKILL.md): chooses names and terminology by
  clarifying meaning, behavior, and reader context.
- [explaining-code](skills/explaining-code/SKILL.md): explains how code and software
  systems work through evidence-driven walkthroughs and code-native views.
- [technical-writing](skills/technical-writing/SKILL.md): writes developer documentation
  and hands the completed draft to Editor to improve clarity and flow.
- [building-skills](skills/building-skills/SKILL.md): writes and revises skill prompts,
  including activation descriptions, instructions, and references.
- [writing-prompts](skills/writing-prompts/SKILL.md): writes and revises model instructions
  in system prompts, skills, repository guidance, and tool descriptions.

## Agents

[Editor](agents/editor.md) improves draft clarity and flow while preserving meaning.
It can rebuild sentences, reorder paragraphs, and remove AI writing patterns. It
returns revised text or edits explicitly assigned files. The main agent remains
responsible for the document's purpose and content.

[Scout](agents/scout.md) investigates proposed changes, including affected behavior
and consumers, compatibility risks, and unresolved questions. It may run focused
experiments in disposable environments while leaving the working checkout and
shared resources unchanged. It returns findings, not an implementation or plan.

Editor and Scout use these Claude Code configurations:

| Agent | Model/effort |
| --- | --- |
| Editor | Opus/low |
| Scout | Sonnet 5.5/high |

Sources are recorded in agent frontmatter comments because Claude Code's agent
schema has no source metadata field.

[Finder](agents/finder.md), [Librarian](agents/librarian.md), and
[Oracle](agents/oracle.md) are also included as Claude Code agents.

## Installation

Install with Claude Code:

```sh
claude plugin marketplace add andreimaxim/skills
claude plugin install engineering@andreimaxim
```

## Principles

The [design principles](skills/building-skills/SKILL.md#principles) in `building-skills`
guide both skills and agent prompts.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for local development and validation.
