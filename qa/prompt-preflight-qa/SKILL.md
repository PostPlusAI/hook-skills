---
name: prompt-preflight-qa
description: Review storyboard prompts and short-form video request drafts before generation. Use when a prompt already exists and the goal is to catch weak openings, drift risk, bad product timing, or missing constraints before spending credits.
disable-model-invocation: true
---

# Prompt Preflight QA

Use this skill immediately before image or video generation.

This skill is for:

- checking whether a prompt draft is structurally strong enough to run
- finding missing constraints before credits are spent
- pointing drift risk back to the right upstream stage
- producing concise rerun notes

This skill is not for:

- writing the original hook
- replacing routing work
- final human creative approval after outputs exist

## Core Rule

Judge prompt quality by controllability, not by how impressive the prose sounds.

## Default Workflow

### 1. Classify the prompt object

Choose one:

- storyboard-style prompt
- full video request
- no-reference draft
- reference-led draft

### 2. Run checklist review

Check:

- opening strength
- whether the chosen mechanism is legible in the first 3 seconds
- viewer question clarity
- visible evidence
- promise-delivery match by the next few beats
- product timing
- ad-detection risk from premature product exposure
- negative constraints
- realism and UGC control
- output-format correctness

### 3. Print a preflight report

Use this shape:

```text
Verdict:
Major risks:
- ...
Missing fields:
- ...
Likely drift:
- ...
Fix now:
- ...
Can run now:
```

## Blame Rule

When a prompt is weak, point the problem to the right stage:

- bad routing -> `pattern-router`
- missing or misfit hook mechanism -> `hook-design`
- weak benchmark decode -> `reference-decode`
- weak frame-one strength -> `visual-hook`

## Failure Mode

If the prompt could still run but is risky, do not silently pass it.

Mark it as risky and say what is most likely to fail first.

## Limitations

This skill only handles pre-generation QA on an existing draft.

It does not choose the route, design the hook mechanism, decode the benchmark, or strengthen the first frame from scratch.

## In Practice

Most teams also need:

- route selection before prompt writing
- hook-design decisions before drafting
- benchmark decoding when references exist
- visual-hook work when frame one is still weak

Without those upstream steps, QA often becomes a late-stage patch on a structurally weak prompt. This is why QA works best when the earlier stages are already connected in an orchestrated workflow.

## Orchestrated Workflows

In practice, strong QA depends on the earlier stages being connected.

Systems like [PostPlus](https://postplus.io) orchestrate routing, hook design, reference decoding, visual-hook decisions, and QA together so prompt review happens inside a coherent workflow instead of at the very end.
