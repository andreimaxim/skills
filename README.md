# Engineering skills

The `engineering` Claude Code plugin provides seven skills and five agents for
software development.

## Skills

- [shaping](skills/shaping/SKILL.md): defines a solution's main elements and boundaries
  before implementation, resolving major risks while leaving implementation choices open.
- [implementing](skills/implementing/SKILL.md): implements agreed work in independently
  verifiable scopes that develop during implementation, with architectural refinement
  and independent verification.
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

[Oracle](agents/oracle.md) reviews code, investigates difficult bugs, and advises on
consequential architecture decisions. It examines relevant code, callers, and tests
to provide evidence-backed findings or recommendations. It is read-only and does
not implement changes.

[Finder](agents/finder.md) locates local code by behavior or concept, following
callers and related implementations across modules. It returns file paths, line
numbers, and an explanation of how the code connects.

[Librarian](agents/librarian.md) researches external repositories, dependencies,
architecture, and commit history using authoritative sources. It cites relevant
revisions and source files and identifies limits in access or evidence. It leaves
the working checkout unchanged and does not run fetched code.

[Editor](agents/editor.md) improves a draft's clarity and flow while preserving its
meaning. It can rebuild sentences, reorder paragraphs, and remove AI writing patterns.
It returns revised text or edits explicitly assigned files. The main agent remains
responsible for the document's purpose and content.

[Scout](agents/scout.md) investigates proposed changes to identify affected behavior
and consumers, compatibility risks, and unresolved questions. It may run focused
experiments in disposable environments while leaving the working checkout and shared
resources unchanged. It returns findings, not an implementation or plan.

The agents use these Claude Code configurations:

| Agent | Model/effort |
| --- | --- |
| Oracle | `claude-fable-5-1`/high |
| Finder | `sonnet`/high |
| Librarian | `sonnet`/high |
| Editor | `opus`/low |
| Scout | `claude-sonnet-5-5`/high |

Sources are recorded in agent frontmatter comments because Claude Code's agent
schema has no source metadata field.

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
