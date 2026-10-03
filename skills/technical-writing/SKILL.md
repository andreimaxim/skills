---
name: technical-writing
description: Writes and revises technical documentation, including READMEs, how-to guides, reference, explanations, technical proposals, and design documents, around what the reader needs to accomplish or understand. Use when drafting or editing developer documentation, shaping pitches, ticket solutions, or PR descriptions.
---

# Technical writing

Write or revise technical documents around what the intended reader needs to accomplish or
understand. Establish the audience, purpose, and assumed knowledge from the request and
existing documentation.

For example:

- A developer learning SQL joins needs a small dataset, queries to run, and results they can
  check. Introduce alternatives after they've seen one join work.
- An on-call developer rolling back a failed deployment needs a usable recovery procedure.
  They should not have to read the history of the deployment system before finding the commands.
- A developer checking the maximum upload size needs the exact limit and any exceptions, not
  a tour of the upload pipeline.
- A developer asking why reports are generated asynchronously needs the constraints and
  trade-offs behind the design. Queue configuration instructions don't answer that question.
- An engineering manager evaluating a proposal for bulk editing needs to understand
  the user's problem, proposed interaction, trade-offs, and boundaries. Show dependencies that
  affect the work's scope, and distinguish proposed behavior from what already exists.
- A product manager reading a ticket solution about an incorrect session status needs the cause,
  the remedy, and the resulting status and badge color for the affected users. Include technical
  details that explain the fix or its impact, such as missing data from an upstream response and
  the extra database query needed to obtain it. Present distinct behavior changes separately.
  Omit commit history and exhaustive lists of unchanged behavior.
- A developer reviewing a PR that changes payment retries needs the reason for the change,
  its effect on behavior, and the evidence supporting it. Highlight risks and verification
  gaps instead of narrating the diff file by file.

A README may have several purposes. Organize its sections by what readers need to do or
understand, so they can find what they need without reading unrelated material. For pitches
and design documents, follow the relevant template or agreed structure.

For procedures, make prerequisites, conditions, and observable results explicit. Place
warnings before the actions they constrain. Organize reference material by the system it
describes, preserving exact defaults, limits, and exceptions. Ground explanations in the
actual constraints, alternatives, and consequences.

Match commands, examples, and claims to the supplied source. When revising, preserve useful
structure and the author's intended meaning. Change what obstructs the reader rather than
rewriting merely for a different style.

Once the draft is complete, delegate a prose-cleanup pass to the Editor agent. Give it the
draft, intended audience, requested tone, and relevant sources and constraints. Assess its
edits for factual accuracy and preserved meaning before delivering the document. The main
agent remains responsible for the content and structure.
