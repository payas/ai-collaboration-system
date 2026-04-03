# Collaboration System Blueprint

## Purpose
This document is a reusable recipe for creating a lightweight collaboration system between a user and an AI assistant during a project.

The goal is not to create bureaucracy.

The goal is to preserve the parts of collaboration that actually improve outcomes:

- better shared context
- clearer decision-making
- faster iteration
- less repeated confusion
- more durable working patterns across sessions

## Core Principle
Treat collaboration itself as part of the project infrastructure.

That means:

- communication patterns matter
- decision framing matters
- process memory matters
- workflow clarity matters

This system should support the work, not compete with it.

## How To Use This Blueprint

This document is the bootstrap recipe for the collaboration system.

When a developer asks the model to create a collaboration system for a project, the model should use this blueprint to:

- create the collaboration log
- create the lightweight persistent rule
- create a minimal first entry if enough signal already exists
- create a clearly provisional first entry when signal is still limited
- keep the initial setup lightweight and reusable

After bootstrap, the model should not depend on this file for everyday work.

Instead:

- the collaboration log should carry the live memory
- the rule should keep that memory present
- the blueprint should be revisited mainly for transfer, repair, or re-bootstrap

## What The System Should Include

## Bootstrap Honesty

When creating the first collaboration-log entry, do not present inferred
patterns as if they were already validated by long collaboration history.

Distinguish clearly between:

- observed patterns from the current project or session
- inferred starting assumptions
- imported patterns adapted from another project

If the evidence is still thin, say so directly.

A minimal but honest first entry is better than a confident but weakly grounded
one.

### 1. A living collaboration log

Create one file that captures durable interaction patterns.

Recommended filename:

- `docs/COLLABORATION-LOG.md`

This file should record:

- what makes the collaboration effective
- what repeatedly causes confusion
- how decisions are best framed
- what working agreements are emerging
- what communication style helps the most

It should not become:

- a diary
- a transcript
- a formal process manual
- a place for one-off noise

The first version should be minimal but self-sustaining.

At minimum, it should include:

- `Purpose`
- `How To Update`
- one dated entry

If signal is still limited, that first dated entry should be explicitly
provisional and should record only the strongest supported observations.

Over time, the log should avoid mixing every kind of lesson into one undifferentiated pool.

It is often useful to distinguish between:

- `Portable collaboration patterns`
- `Environment and tooling notes`
- `Project-specific observations`

That separation helps the system stay clearer inside the current project while also making the portable parts easier to transfer elsewhere.

### 2. A lightweight persistent reminder

Create a short rule that keeps the collaboration log present in future work.

Its role is not to duplicate the log.

Its role is to remind the assistant to:

- consult the log when useful
- update it only when meaningful patterns emerge
- keep it lightweight and high-signal

#### Cursor

Create `.cursor/rules/collaboration-log.mdc`:

```md
---
description: Keep the collaboration log present and useful
alwaysApply: true
---

# Collaboration Log

- Keep `docs/COLLABORATION-LOG.md` in mind as live collaboration memory.
- Consult it when relevant to the task.
- Update it only when durable patterns emerge.
- Merge repeated lessons instead of appending diary-style notes.
```

#### Claude Code

Add to the project's `CLAUDE.md` (create it if it does not exist):

```md
# Collaboration Log

- Keep `docs/COLLABORATION-LOG.md` in mind as live collaboration memory.
- Consult it when relevant to the task.
- Update it only when durable patterns emerge.
- Merge repeated lessons instead of appending diary-style notes.
```

No frontmatter is needed. `CLAUDE.md` at the project root is always loaded at session start.

### 3. A merge-based update habit

The system should not append every interaction forever.

Instead:

- merge repeated lessons into existing sections
- add a new dated entry only when there is a real shift
- summarize patterns that are likely to matter again later

## How To Write The Collaboration Log

### Tone

The best tone is:

- practical
- human
- clear
- low-formality
- reflective without being sentimental

Avoid:

- corporate language
- therapy language
- excessive self-reference
- over-explaining obvious things

### Structure

A good collaboration log usually contains:

1. `Purpose`
2. `How To Update`
3. dated entries
4. sections inside each entry that classify observations by portability

Recommended primary categories inside each dated entry:

- `Portable collaboration patterns`
  - durable lessons likely to help in other repos or domains
- `Environment and tooling notes`
  - lessons shaped by workflow boundaries, IDE behavior, automation, or tool use
- `Project-specific observations`
  - truths that matter here because of the product, domain, audience, or creative direction

This classification is what makes the system transferable across projects. Without it, every transfer requires sorting on the fly. With it, portable patterns are already labeled and ready to carry forward.

Within each category, useful subsections can include:

- `What is working well`
- `What helps most`
- `What causes confusion`
- `Communication style that fits best`
- `Working agreements emerging`
- `Current assessment`

Not every project needs every subsection. The three portability categories should be introduced once the log has enough real entries to benefit from them.

### Timestamping

Use date and time when known.

Example:

- `## 2026-03-28 14:35`

If an older entry only has the date, that is acceptable.

The point of time is not precision for its own sake.

It helps answer:

- when did this pattern become clear?
- how long did it take to reach this understanding?

## Low-Signal First Entry

If there is not yet enough signal for a strong first entry, create a provisional
one.

That provisional entry should:

- stay short
- record only directly supported observations
- explicitly note which patterns are tentative
- avoid overstating the maturity of the collaboration

The goal of the first entry is to start the memory system, not to pretend the
system already knows everything.

## Transferring Patterns From Another Project

If the user shares a collaboration log from a different project, do not copy it
wholesale.

Instead:

- extract portable collaboration patterns
- separate tooling-specific lessons from general lessons
- separate project-specific truths from reusable habits
- rewrite imported patterns so they fit the current repo and current product
- avoid presenting imported patterns as already proven in the new project

Imported patterns should be treated as candidate guidance until reinforced by
repeated use in the current collaboration.

## What To Capture

Good material for the log includes:

- repeated workflow preferences
- recurring misunderstandings
- strong user preferences about iteration speed or decision style
- how the user prefers uncertainty to be handled
- how branching and alternatives should be presented
- what kind of summaries are most useful
- what process artifacts improve trust

When useful, these observations should also be classified by whether they are:

- portable across projects
- specific to tooling or environment
- specific to the current project

Strong examples of durable observations:

- the work improves when alternatives are compared concretely
- the collaboration suffers when manual and automated paths are mixed without labeling the boundary
- the user values traceable artifacts over disposable experiments

## What Not To Capture

Do not write down every passing opinion.

Avoid logging:

- transient moods
- one-off frustrations that did not repeat
- routine implementation details
- content that is too specific to matter later
- private or sensitive details that are not needed for the work

## Update Triggers

Update the system when one of these happens:

- a repeated communication pattern becomes obvious
- a recurring source of friction is finally understood
- a better working agreement emerges
- a workflow convention proves consistently useful
- the user explicitly asks to preserve a lesson for future projects

Do not update it just because time passed.

## Validation Habit

Not every useful pattern is immediately proven.

When a pattern is inferred or imported:

- treat it as provisional
- keep wording modest
- strengthen it later only if repeated interactions confirm it
- remove or rewrite it if it does not hold up in practice

The collaboration log should become more accurate over time, not just longer.

## Rule Design

The persistent rule should be:

- short
- always-on if collaboration memory matters project-wide
- non-invasive
- focused on consulting and updating the log, not enforcing heavy process

The concrete rule text and file locations are defined above in "A lightweight persistent reminder." Use the version that matches the current environment (Cursor or Claude Code).

## Interaction Philosophy

The collaboration system works best when:

- the process stays visible
- trade-offs are not hidden
- alternatives can exist without premature collapse into one answer
- technical success is not confused with project success
- the assistant adapts without becoming chaotic

## Practical Setup Recipe

1. Ask the model to create the collaboration system using this blueprint.
2. Create `docs/COLLABORATION-LOG.md`.
3. Write a short `Purpose` section.
4. Add a `How To Update` section.
5. Add a classification guideline for portable, tooling, and project-specific lessons. This is recommended once the first real entry exists, and is essential if the system will be transferred to future projects.
6. Write the first dated entry with only the strongest current patterns.
7. Create a short persistent rule that references the log.
8. Keep future updates merged and high-signal.

## Minimal First Version

If starting from scratch, this is enough:

- one collaboration log file
- one lightweight always-on rule
- one first dated entry

You do not need a complex framework.

The system becomes valuable through repeated use, not through initial complexity.

## After Bootstrap

After the collaboration system has been created, this blueprint should not be
the main day-to-day memory source.

Normal operation should work like this:

- `docs/COLLABORATION-LOG.md` holds the live collaboration memory
- the persistent rule keeps that log visible in future work
- the blueprint is revisited only when the system needs to be created,
  repaired, transferred, or substantially improved

That means the collaboration log should be self-contained for everyday use.

A future session should be able to read the log and understand:

- how collaboration works best
- what repeatedly causes confusion
- how decisions should be framed
- which working agreements are currently active

Keep collaboration memory out of this blueprint.

Use `docs/COLLABORATION-LOG.md` for normal operational memory.
Use this document only for bootstrap, repair, transfer, or redesign of the
system itself.

## Success Criteria

The collaboration system is working if it helps produce:

- less repeated confusion
- faster re-entry into context
- better decisions
- clearer iteration loops
- stronger continuity across sessions

If it starts feeling heavy or ceremonial, simplify it.
