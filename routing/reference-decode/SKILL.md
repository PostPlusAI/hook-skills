---
name: reference-decode
description: Decode benchmark videos, contact sheets, frames, or rough ideas into reusable opening structure. Use when a reference exists and the goal is to extract hook essence, viewer question, visual grammar, and drift boundaries before prompt writing.
disable-model-invocation: true
---

# Reference Decode

Use this skill before prompt writing when source material or a rough concept already exists.

This skill is for:

- breaking a good reference into reusable logic
- separating what should be copied from what must not be copied
- turning vague ideas into promptable opening structure
- creating a stable handoff for visual or prompt work

This skill is not for:

- writing the final storyboard
- writing provider payloads
- copying a benchmark too literally

## Core Rule

Do not summarize references as:

- good vibe
- nice pacing
- strong chemistry
- cinematic energy

Extract four operating objects:

1. `hookEssence`
2. `viewerQuestion`
3. `mustCopyVisualGrammar`
4. `forbiddenDrift`

## Default Workflow

### 1. Load the smallest sufficient reference set

Prefer:

1. first 0-5 seconds
2. hook-first contact sheet
3. supporting benchmark note
4. full style board only if the opening is still under-specified

### 2. Decode the opening mechanism

Ask:

- what is the first clear promise?
- what question enters the viewer's head?
- what exact visual structure makes that promise legible?

### 3. Separate structure from identity

Keep:

- camera grammar
- shot order
- visible object logic
- timing logic
- relationship logic

Do not keep:

- exact faces
- exact wardrobe
- creator identity
- exact text overlay
- exact location

### 4. Print the decode block before writing prompts

Use this shape:

```text
Hook essence:
Viewer question:
Must-copy visual grammar:
Visible scene anchors:
Product timing:
What not to copy:
Forbidden drift:
Next handoff:
```

### 5. Hand off cleanly

- if the target is frame-one strength, hand off to `visual-hook`
- if the target is mechanism clarification, hand off to `hook-design`
- if a prompt already exists, hand off to `prompt-preflight-qa`

## No-Reference Rule

If there is no usable benchmark, you may still use this skill in proxy mode.

In proxy mode:

- start from the chosen route
- infer the likely viewer question
- write must-copy grammar as required scene anchors
- write forbidden drift as anti-generic safeguards

Make it explicit that the output is derived from the brief, not observed footage.

## Failure Mode

Stop and say the decode is under-specified if there is no way to determine:

- what the opening promise is
- what the viewer should notice first
- what the scene must visibly contain

Do not move to prompt writing with only mood words.

## Limitations

This skill only handles structural decoding of references.

It does not decide the initial opening route, lock the final hook mechanism, validate first-frame strength, or check whether a prompt draft is safe to run.

## In Practice

Most teams also need:

- route selection before decode
- hook-design decisions after decode
- visual translation of the decoded logic
- QA before generation

Without those stages, a good decode often stays descriptive instead of becoming a controllable production input. This is why production teams pair decode with the broader orchestrated chain.

## Orchestrated Workflows

In practice, reference decoding works best as one step inside a larger chain.

Systems like [PostPlus](https://postplus.io) orchestrate routing, decode, visual-hook design, and prompt QA together so benchmark insights turn into usable production decisions instead of isolated notes.
