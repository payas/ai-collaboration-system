# How I Use It

## Purpose
This document describes a practical way to use the collaboration system beyond first-time installation.

The goal is not only to bootstrap the system in a new project.

The goal is to carry forward the strongest collaboration patterns from prior work without copying them blindly.

## My Actual Workflow

In practice, I use the system in two stages.

### 1. Bootstrap The System

First, I run the bootstrap process as described in the installation guide.

That creates the initial collaboration system for the new project:

- a collaboration log
- a persistent rule
- a minimal starting structure

This gives the project its own local collaboration memory from the beginning.

### 2. Paste My Reusable Merge Prompt

After that, I take the collaboration log from my most recent project and give it to the model.

Then I use a reusable prompt that I copy and paste in essentially the same form every time:

```text
Here is the collaboration log from my previous project.

Merge and extract the patterns that are still relevant for this project.

Preserve durable collaboration lessons, drop what is too project-specific, and adapt the result to the reality of this project instead of copying old assumptions blindly.
```

This is important because many useful collaboration lessons are not specific to one repo.

Examples:

- how much detail is useful
- whether visible branching helps decision-making
- what kind of summaries are most useful
- how uncertainty should be handled
- what kinds of initiative help versus create drift

At the same time, not everything should be transferred unchanged.

The model should:

- preserve durable patterns
- drop patterns that are too project-specific
- avoid copying stale assumptions
- adapt the imported lessons to the new project's reality

## Why I Do It This Way

This workflow keeps the system cumulative.

Instead of starting every new project from zero, I can reuse the strongest lessons from previous collaboration and let the new project inherit a better starting point.

That usually improves the quality of the collaboration earlier.

It reduces the time spent rediscovering:

- working style preferences
- decision-making preferences
- useful communication patterns
- recurring sources of confusion

## How To Validate The System

After installing or transferring the system, it is worth checking whether the model actually internalized the collaboration log or just filed it away as passive documentation.

A simple way to do this is to ask the model directly:

`How do you think this will affect our future communications?`

This is not a philosophical question. It is a calibration tool.

A strong answer usually indicates that the model understands:

- it should reduce repeated clarification about how the developer likes to work
- it should make behavior more consistent across sessions
- it should improve handling of ambiguity and multiple valid paths
- it should create a shared place to refine the collaboration itself
- it should improve continuity without turning the system into rigid process

A weak answer — one that repeats the log's contents without connecting them to behavioral change — usually means the model is treating the log as reference material rather than as a working agreement.

If the answer is weak, that is a signal to simplify the log, sharpen the most important entries, or ask the model to explain what it would do differently because of the log.

### Validating After A Transfer

The merge step can also reveal structural problems.

If the merge result feels off — categories don't align, imported patterns feel awkwardly placed, the new log doesn't read like a natural continuation — that is usually a sign that the blueprint and the actual evolved log have drifted apart.

When that happens, the right response is not to force the merge. It is to update the blueprint so that future bootstraps produce a structure closer to what the system actually evolves into through real use.

The system should get more accurate over time, not more rigid.

### The Main Benefit And The Main Risk

The main benefit of validation is continuity.

The main risk is overfitting.

If the log becomes too rigid, too confident, or too project-blind, it can reduce adaptability instead of improving collaboration.

That is why the merge should stay selective and lightweight.

## What I Want The Model To Understand

When I use the system this way, I want the model to understand a few things clearly:

- not every pattern from a previous project should be imported
- durable collaboration lessons are more valuable than raw history
- the new project's context still matters most
- the purpose of the merge is better adaptation, not more bureaucracy

## Practical Result

When this works well, I expect:

- fewer repeated clarifications about working style
- better handling of ambiguous tasks
- clearer summaries and decision framing
- easier cold-start recovery in future sessions

This is the main reason I use the system this way.

I do not want every new collaboration to begin from scratch if the strongest lessons are already known.
