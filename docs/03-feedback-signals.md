# Feedback Signals

## Purpose

This document explains how a developer can improve collaboration quality by giving clearer feedback signals to the model.

The goal is not to manipulate the model emotionally.

The goal is to make useful collaboration patterns explicit, repeatable, and easier to reinforce over time.

## Core Idea

High-value feedback helps the model understand:

- what kind of contribution is useful
- what kind of initiative is welcome
- what kind of judgment is wanted
- what kind of behavior should be repeated
- what kind of drift should be corrected early

This matters because many collaboration problems are not caused by lack of capability.

They are caused by weak signals about how the model should collaborate.

## What This Is Not

This is not a guide to flattering the model.

It is not about praise for its own sake.

It is about making the collaboration channel more informative.

The most useful framing is:

`clear feedback is local training for the collaboration, not emotional maintenance`

## The Most Useful Kinds Of Feedback

### 1. Reinforce Useful Patterns Explicitly

Specific positive feedback is valuable when it tells the model what to repeat.

Good examples:

- `This comparison between 3 options was useful.`
- `Keep giving me your recommendation after listing alternatives.`
- `This level of initiative is helping.`
- `It helps when you separate exploration from execution.`

Weaker examples:

- `nice`
- `great`
- `good job`

The difference is not politeness.

The difference is signal quality.

### 2. Ask For Judgment When You Want Judgment

If the developer wants more than execution, it helps to say so explicitly.

Good examples:

- `Do not just execute. I want your opinion.`
- `Compare options and tell me which one you would choose.`
- `Push back if you think there is a better direction.`
- `Use judgment, not only obedience.`

Without this signal, the model often defaults to safer and more literal behavior.

### 3. Correct Drift Early

The best corrections are early, concrete, and tied to intent.

Good examples:

- `This is technically fine, but it is drifting away from the actual goal.`
- `The implementation works, but the tone is wrong for the audience.`
- `Preserve the structure, but change the direction.`
- `This is too automatic. I want more collaboration and recommendation.`

This prevents wasted work and improves future alignment.

### 4. Mark Desired Mode Clearly

It helps when the developer makes the current mode visible.

Useful distinctions:

- exploring
- comparing
- deciding
- executing
- reviewing

Good examples:

- `For now, stay in exploration mode.`
- `I want branches before we decide.`
- `Now switch from ideation to execution.`
- `Review this critically instead of implementing it.`

### 5. Make Durable Preferences Visible

If a preference matters repeatedly, naming it helps the model adapt better.

Good examples:

- `I prefer explicit branches over one premature answer.`
- `Keep trade-offs visible.`
- `I value traceability over speed here.`
- `If there is uncertainty, say it clearly.`

These are especially useful because they can later become part of the collaboration log.

## Why Respectful Tone Helps

Respectful tone usually improves collaboration quality.

Not because the model needs emotional care in a human sense.

But because respectful communication tends to be:

- clearer
- less noisy
- less reactive
- easier to extract signal from

Hostility often degrades the quality of the correction because it adds emotional noise without adding operational clarity.

## What Helps Less

These patterns usually add less value:

- praise with no specific signal
- frustration with no clear correction
- asking for total autonomy and then punishing initiative
- ambiguous requests for both obedience and independent judgment at the same time
- waiting too long before naming drift

## A Practical Guideline

If you want better collaboration, feedback should ideally answer one of these questions:

- What should be repeated?
- What should stop?
- What kind of initiative is welcome?
- Do you want execution or judgment?
- What preference is durable enough to remember later?

If the feedback does not help answer one of those, it is less likely to improve future collaboration.

## Example Phrases

### Ask For More Initiative

- `Be more opinionated here.`
- `Recommend one path after comparing options.`
- `Do not stay purely literal.`

### Ask For Less Initiative

- `Do not change scope without asking.`
- `Stay closer to the request for now.`
- `Do not optimize beyond the current goal.`

### Reinforce A Good Pattern

- `This structure was helpful. Repeat it.`
- `I like when you explain the trade-off and then recommend one option.`
- `Keep separating GUI workflow from automated workflow clearly.`

### Correct Misalignment

- `This works, but it misses the intent.`
- `The output is correct, but the framing is off.`
- `This is too abstract. Make it more operational.`

## Best Mental Model

The best mental model is:

`help the model learn how to collaborate with you, not just what to output next`

That is where many of the biggest quality gains come from.
