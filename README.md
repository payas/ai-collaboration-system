# AI Collaboration System

A lightweight protocol for improving how developers and AI models work together across the life of a project.

## The Problem

Most developers know how to prompt an AI model. What many teams still lack is a reliable way to collaborate with one over time. The same corrections get repeated. Workflow preferences are forgotten between sessions. Outputs can be technically correct while missing the real intent.

This is not a prompting problem. It is a collaboration problem.

**For the full editorial version, read [The Missing Layer In AI Coding Workflows (PDF)](./ai-collaboration-system.pdf).**

## The Solution

A small system with three pieces:

1. **A collaboration log** — a living file that captures durable patterns about how the collaboration works best
2. **A persistent rule** — a lightweight reminder that keeps the log present in the model's context
3. **A selective update habit** — only log what is durable, merge what repeats, skip the noise

The developer defines the intent. The model bootstraps and maintains the system.

## Quick Start

Copy `COLLABORATION-SYSTEM-BLUEPRINT.md` into your project, then tell the model:

```
Create a collaboration system for this project by following the instructions in
@COLLABORATION-SYSTEM-BLUEPRINT.md.

Set up the required files, keep the system lightweight, and use it as durable
project memory for how we collaborate.
```

The `@` syntax works in Cursor. In Claude Code, reference the file by path instead.

That's it. The model reads the blueprint, creates the log and rule, and seeds a first entry. You work normally from there.

## What's In This Repo

### Core

- [`COLLABORATION-SYSTEM-BLUEPRINT.md`](./COLLABORATION-SYSTEM-BLUEPRINT.md) — the reusable recipe the model follows to create the system
- [`docs/01-the-gap.md`](./docs/01-the-gap.md) — the problem this system solves
- [`docs/02-installing-the-system.md`](./docs/02-installing-the-system.md) — detailed setup guide and operational flow
- [`docs/03-feedback-signals.md`](./docs/03-feedback-signals.md) — how developer feedback quality shapes collaboration quality
- [`docs/04-context-and-tools.md`](./docs/04-context-and-tools.md) — why the system improves outcomes without adding new capabilities
- [`docs/05-how-I-use-it.md`](./docs/05-how-I-use-it.md) — a practical workflow for carrying collaboration patterns from one project into the next

### Example

- [`examples/COLLABORATION-LOG-EXAMPLE.md`](./examples/COLLABORATION-LOG-EXAMPLE.md) — a real collaboration log from a working project, showing what the system looks like in practice

## Reading Order

If you want to understand the idea:

1. [`docs/01-the-gap.md`](./docs/01-the-gap.md)
2. [`docs/03-feedback-signals.md`](./docs/03-feedback-signals.md)

If you want to install it:

1. [`COLLABORATION-SYSTEM-BLUEPRINT.md`](./COLLABORATION-SYSTEM-BLUEPRINT.md)
2. [`docs/02-installing-the-system.md`](./docs/02-installing-the-system.md)

If you want the deeper explanation of how it works:

- [`docs/04-context-and-tools.md`](./docs/04-context-and-tools.md)

If you want the practical workflow I use personally:

- [`docs/05-how-I-use-it.md`](./docs/05-how-I-use-it.md)

## What Good Looks Like

When the system is working, you notice:

- Less repeated confusion
- Faster context recovery between sessions
- Cleaner iteration loops
- Better branching and comparison
- The model adapts without being re-taught the same preferences

If it starts feeling heavy, simplify it. The system should support the work, not compete with it.

## Author

Ale Cortés — 2026

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

Use it, adapt it, share it. Just give credit.
