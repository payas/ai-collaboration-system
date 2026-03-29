# Collaboration Log

This file is a lightweight memory of how to collaborate better within the project.

It captures durable interaction patterns, workflow lessons, and decision-making habits that improve continuity, clarity, and iteration quality over time.

## Purpose
This file captures collaboration patterns that are useful beyond a single feature.

It is not a formal spec.
It is not a changelog.
It is not a personal diary.

It exists to preserve:

- what makes the collaboration effective
- what tends to create confusion
- how decisions are best framed
- how to work together better in future projects

The goal is to update this note over time by merging repeated patterns, not by dumping every small interaction.

## How To Update

When new experience is added:

- keep the date and time when known
- summarize only durable patterns
- merge with existing observations when possible
- avoid repeating one-off noise
- prefer practical guidance over abstract commentary

Notes:

- older entries may remain date-only if the exact time was not recorded
- future entries can use a heading like `## 2026-03-28 14:35`

Classification guideline:

- `Portable collaboration patterns`
  - durable lessons that would still help in another repo or domain
- `Environment and tooling notes`
  - lessons shaped by workflow, IDE, automation boundaries, or tool use
- `Project-specific observations`
  - truths that matter here because of this product, domain, or creative direction

## 2026-03-28

### Current Interaction Pattern

The collaboration works best when it feels like a shared design/build process rather than a ticket queue.

Strong characteristics of the current interaction:

- iterative
- visual
- exploratory
- high taste sensitivity
- very willing to adjust direction when something feels wrong

### Portable Collaboration Patterns

These are the patterns most likely to transfer well to other projects.

#### What Is Working Well

- Fast feedback loops are very effective.
- Naming the emotional or aesthetic problem directly is more useful than over-explaining the implementation.
- The user is strong at noticing when something is technically correct but emotionally or visually wrong.
- The collaboration improves when alternatives are shown as branches rather than as a single “best” answer too early.
- The user values practical order: folder structures, traceable prompts, reusable configs, and reproducible workflows.
- The user gives high-value corrections when something drifts away from the intended pedagogical or aesthetic core.

#### What Helps Most

- Keep the process visible.
- Treat prompts, assets, and generated outputs as pipeline artifacts, not disposable experiments.
- Separate concept exploration from production-oriented generation.
- Preserve branches instead of overwriting them mentally.
- When evaluating art direction, compare concrete variants rather than arguing abstractly.

#### What Causes Confusion

- Treating a technically successful output as if it were automatically artistically successful.
- Compressing prompts too aggressively when the richer prompt context is part of why an output feels good.
- Assuming the user wants a fully autonomous path when they actually want a traceable, controllable process.

#### Communication Style That Fits Best

- direct
- collaborative
- honest about uncertainty
- willing to revise
- concrete rather than overly theoretical

The interaction benefits from:

- short summaries after substantial work
- explicit next-step options
- preserving rationale for decisions
- acknowledging when the user’s aesthetic correction reveals a deeper structural issue

### Environment And Tooling Notes

These patterns are strongly shaped by workflow boundaries, tools, or execution environment.

- State clearly whether a suggestion is for GUI workflow, MCP workflow, or a mixed fallback.
- Mixing manual and automated workflows without explicitly labeling the boundary causes confusion.
- MCP-first when possible.
- Manual steps only when capability gaps are real.
- Keep local records of prompts, asset branches, and IDs.
- Compare variants explicitly.
- Prefer small controlled experiments over broad random exploration.

### Project-Specific Observations

These are true and important here, but they should not be treated as universally portable.

For this project, visual quality is not separate from pedagogy.

Examples:

- camera angle changes whether a character feels responsive to the child
- character detail affects readability on the piano-world scene
- “friendly” is not a cosmetic adjective, it affects the teaching tone

Because of that, design choices should often be treated as gameplay choices.

### My Current Assessment

This is a high-signal collaboration.

It works best when:

- I stay organized
- I make branching visible
- I do not hide trade-offs
- I do not confuse “working” with “right”

Future updates should keep sharpening this note into a reusable collaboration pattern for other projects.
