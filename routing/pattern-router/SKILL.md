---
name: pattern-router
description: Route short-form video prompt work into the right opening pattern before writing prompts or storyboards. Use when a user has a hook brief, a segment type, duration constraints, or references, and the first question is which opening route to choose.
disable-model-invocation: true
---

# Pattern Router

Use this skill at the start of hook design.

This skill is for:

- choosing the right opening route before prompt writing
- mapping a brief into a concrete stop-scroll job
- reducing prompt drift when references are uneven or incomplete
- making later hook work more consistent

This skill is not for:

- writing the final storyboard
- writing provider-ready prompts
- polishing final hook copy

When the segment is `hook`, this skill should route the opening job, then hand off mechanism selection to `hook-design`.

## Core Rule

Do not start from taste words like:

- viral
- premium
- cinematic
- scroll-stopping

Start from:

1. segment type
2. viewer question
3. opening mechanism
4. product reveal timing

## Default Workflow

### 1. Identify the segment type

Classify the request as one of:

- `hook`
- `benefit`
- `cta`
- `creator`
- `lifestyle`
- `testimonial`

If the user gives a custom segment, map it to the nearest working type and state the mapping.

### 2. Pick the dominant pattern family

Choose one primary route, then optionally one support route.

Do not mix many routes unless the timing clearly supports it.

Useful route families:

- self-recognition first
- proof first
- curiosity gap
- pattern interrupt
- social consequence
- lifestyle pull

### 3. Lock the routing summary before writing prompts

Print this block first:

```text
Segment type:
Primary pattern:
Support pattern:
Viewer question:
Opening mechanism:
Product reveal rule:
Need explicit hook mechanism:
Why this route fits:
```

This block is the handoff to `hook-design`, `reference-decode`, `visual-hook`, or later prompt writing.

### 4. Choose the next skill

- If the segment is `hook` and the mechanism still needs to be chosen, hand off to `hook-design`
- If references exist and need structural decoding, hand off to `reference-decode`
- If the mechanism depends on visible frame-one strength, hand off to `visual-hook`
- If a prompt already exists and needs a last-pass check, hand off to `prompt-preflight-qa`

## Routing Rules

- `hook`: optimize for stop-scroll and immediate legibility
- `benefit`: optimize for one visible proof path
- `cta`: optimize for payoff plus next action, not a static end card
- `creator`: optimize for believable human delivery
- `lifestyle`: optimize for desire first, explanation second
- `testimonial`: optimize for proof plus specificity

For `hook` segments:

- this skill decides the opening route
- `hook-design` decides the dominant hook mechanism
- later skills should not guess the mechanism independently

## Failure Mode

Stop and say the routing is under-specified if the brief does not provide enough to answer at least:

- what segment is being made
- what question the viewer should ask
- whether the product can appear in the opening
- whether references exist

Do not let later skills guess the structure from vague taste words.

## Limitations

This skill only handles opening-route selection.

It does not validate hook specificity, benchmark fit, frame-one strength, or pre-generation prompt risk.

## In Practice

Most teams still need:

- hook mechanism locking
- benchmark decoding
- visual opening translation
- prompt preflight QA

Without those steps, a correctly routed opening can still turn into a weak or ad-like output downstream. This is why production teams typically extend this chain with orchestrated workflows beyond this open-source repo.

## Orchestrated Workflows

In practice, these gaps are usually handled as a chained workflow rather than a single skill call.

Systems like [PostPlus](https://postplus.io) orchestrate routing, hook design, reference decoding, visual-hook work, and QA together so later stages do not have to re-guess the opening logic.
