# Installing The System

## Goal
This guide shows how to activate the collaboration system in a new project from zero.

The aim is not to add process for its own sake.

The aim is to create a lightweight, durable memory for how the developer and the model collaborate best.

The important framing is:

- the developer defines the intent
- the model can bootstrap the system
- the model can help maintain it over time

## The Easiest Way To Start

In practice, the easiest way to install the system is not to build it manually.

It is to ask the model to create it for the project.

### Cursor

```text
Create a collaboration system for this project by following the instructions in
@docs/COLLABORATION-SYSTEM-BLUEPRINT.md.

Set up the required files, keep the system lightweight, and use it as durable
project memory for how we collaborate. Create the collaboration log, the
persistent rule, and a minimal first entry if appropriate.
```

### Claude Code

```text
Create a collaboration system for this project by following the instructions in
docs/COLLABORATION-SYSTEM-BLUEPRINT.md.

Set up the required files, keep the system lightweight, and use it as durable
project memory for how we collaborate. Create the collaboration log, the
persistent rule, and a minimal first entry if appropriate.
```

Replace the path with wherever the blueprint or equivalent starter recipe lives in the target project.

That prompt gives the model a clear job:

- read the blueprint
- create the needed files
- keep the setup lightweight
- initialize the system without overbuilding it

## Role Of The Blueprint

The blueprint is the reusable source recipe for the system.

Its role is to define:

- what the system is
- what files it should include
- how updates should work
- what should and should not be captured

It is most useful for:

- first-time setup
- transferring the system to another project
- repairing or re-bootstrapping the system if it drifts

It should not be the only place where update behavior is defined.

Once the system is instantiated, the collaboration log itself should contain enough guidance to remain usable without constantly re-reading the blueprint.

## Minimum Viable Setup
At the project level, the system still needs three pieces:

1. a collaboration log
2. a lightweight persistent rule
3. an update habit based on durable patterns

What matters is that these pieces exist.

They can be created by the model after a single clear instruction.

## Operational Flow

Once the system exists, the normal operating flow should be:

1. the developer works normally with the model
2. the persistent rule keeps the collaboration log present
3. the model consults the log when collaboration memory is relevant
4. the model updates the log only when durable patterns emerge
5. the blueprint is revisited only for transfer, repair, or re-bootstrap

This keeps the system light in daily use while preserving a strong source recipe in the background.

## What The Model Should Create

### 1. Collaboration Log

Create:

- `docs/COLLABORATION-LOG.md`

Purpose:

- preserve durable collaboration patterns
- store working agreements
- reduce repeated confusion
- improve continuity across sessions

Important:

The first collaboration log should be minimal, but not empty of operating guidance.

It should include at least:

- `Purpose`
- `How To Update`
- one dated entry

That makes the log self-sustaining enough for normal day-to-day use.

Recommended top-level structure:

- `Purpose`
- `How To Update`
- dated entries

Recommended sections inside each dated entry:

- `Current interaction pattern`
- `What is working well`
- `What helps most`
- `What causes confusion`
- `Communication style that fits best`
- `Working agreements emerging`
- `Current assessment`

### 2. Persistent Rule

Create a short persistent rule in your project rule system.

Its job is not to duplicate the log.

Its job is to remind the assistant to:

- keep the collaboration log in mind
- consult it when relevant
- update it only when meaningful, reusable lessons appear

If your environment supports always-on project rules, make it always apply.

The rule should stay:

- short
- lightweight
- non-bureaucratic

The rule is not the source of the update policy.

It is the reminder mechanism.

The fuller logic lives in:

- the blueprint as source recipe
- the collaboration log as live operating memory

### 3. Minimal First Entry

Do not try to predict everything.

Write only the strongest patterns you can already see.

Examples of good early observations:

- how much detail helps or hurts
- whether branching is useful
- what kind of summaries are most useful
- what tends to create confusion
- how uncertainty should be handled

The goal of the first entry is not completeness.

The goal is to seed the system with enough real signal that future updates have a structure to merge into.

## How The System Should Be Maintained

Update the log when:

- the same collaboration pattern appears repeatedly
- a recurring friction becomes clear
- a better working agreement emerges
- the user explicitly says a lesson should be preserved

Do not update it for every small interaction.

If you log everything, the file becomes noise.

This is why the maintenance pattern matters as much as the initial setup.

The model should treat the log as durable memory, not as a running journal.

## What Good Updates Look Like

Good updates are:

- short
- durable
- practical
- mergeable into existing sections

Good examples:

- “The work improves when alternatives are compared concretely.”
- “Manual and automated paths should be labeled clearly.”
- “The project benefits from preserving branch names instead of informal memory.”

## What Bad Updates Look Like

Avoid:

- transcript-style notes
- one-off frustrations with no durable lesson
- routine task summaries
- repeated points that should have been merged

## Timestamp Guidance

Use date and time when known.

Example:

- `## 2026-03-28 14:35`

If exact time is not available, date-only is still acceptable.

## Suggested File Tree

### Cursor

```text
docs/
  COLLABORATION-LOG.md

.cursor/
  rules/
    collaboration-log.mdc
```

### Claude Code

```text
docs/
  COLLABORATION-LOG.md

CLAUDE.md
```

In Claude Code, add the collaboration log instructions directly to the project's `CLAUDE.md` file. This file is loaded automatically at the start of every session.

## Minimal Rule Example

### Cursor

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

### Claude Code

Add to your project's `CLAUDE.md`:

```md
# Collaboration Log

- Keep `docs/COLLABORATION-LOG.md` in mind as live collaboration memory.
- Consult it when relevant to the task.
- Update it only when durable patterns emerge.
- Merge repeated lessons instead of appending diary-style notes.
```

No frontmatter is needed. `CLAUDE.md` at the project root is always loaded at session start.

## Minimal First Entry Example

```md
## Purpose

This file is a lightweight memory of how to collaborate better within the
project.

It captures durable interaction patterns, workflow lessons, and
decision-making habits that improve continuity over time.

## How To Update

- Keep the date and time when known.
- Summarize only durable patterns.
- Merge repeated lessons into existing sections when possible.
- Avoid transcript-style notes and one-off noise.

## 2026-03-28 14:35

### What Is Working Well

- Short summaries after substantial work help maintain clarity.
- Branching alternatives before choosing one improves decisions.

### What Causes Confusion

- Mixing exploratory and production paths without labeling the boundary.
```

## Human And Model Roles

The developer's role is mainly to:

- decide that the system should exist
- correct drift when collaboration quality drops
- point out lessons worth preserving

The model's role is mainly to:

- bootstrap the system from a clear instruction
- create the required files
- keep the system lightweight
- update it only when durable lessons emerge

## Success Criteria

The system is working if it creates:

- less repeated confusion
- faster context recovery
- more consistent adaptation by the assistant
- better continuity across long-running work

If it starts feeling heavy, simplify it.
