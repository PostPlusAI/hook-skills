---
name: hook-design
description: Structure a rough short-form opening into a reusable Hook Brief with explicit mechanism choice, product reveal timing, and downstream handoff guidance. Use when a hook idea is fuzzy, generic, or too product-first.
disable-model-invocation: true
---

# Hook Design

Use this skill after the broad opening route is known and before prompt writing gets too concrete.

This skill is for:

- turning rough hook ideas into a stable `Hook Brief`
- making product reveal timing explicit
- replacing generic hook language with self-identifying specificity
- giving later skills a clean opening logic handoff

This skill is not for:

- choosing the segment family from scratch
- writing the final storyboard grid
- writing provider-ready prompts
- giving final pre-generation approval

## Core Rule

The opening should create a concrete viewer question before the content feels like an ad.

Do not let the product appear before the hook logic is doing visible work.

Treat the hook as a mechanism choice, not a line-polishing exercise.

## Method

Read [`hook-principles.md`](hook-principles.md).

Use [`hook-examples.md`](hook-examples.md) for reference examples, mechanism guidance, and output format diagnosis.

## Default Workflow

### 1. Confirm the upstream route

If the segment type or route is still unclear, use `pattern-router` first.

Do not let this skill replace routing.

### 2. Classify the hook problem

Choose the closest working need:

- rough hook idea that needs structure
- opening line that sounds generic
- product reveal that happens too early
- hook critique that needs rerun direction

Then identify the dominant `Hook mechanism`.

## Hook Mechanism Taxonomy

Choose one primary mechanism before polishing the line.

### 1. `boldClaim`

Use when:

- the opening should challenge a stale belief
- the brand has a clear contrarian stance
- the viewer will pause to evaluate whether the claim is true

Common failure:

- vague provocation with no proof path

### 2. `questionGap`

Use when:

- the viewer has a real unanswered question
- the hook should open an information gap, not a dramatic claim
- the body can answer the question quickly

Common failure:

- generic questions with obvious answers

### 3. `proofFirst`

Use when:

- trust is the main barrier
- visible evidence or numbers can appear early
- the result is more compelling than the setup

Common failure:

- exaggerated proof with no visible credibility

### 4. `painRecognition`

Use when:

- the audience already lives with the pain
- self-identification is stronger than novelty
- the problem needs more specificity, not more hype

Common failure:

- broad category language that fits everyone and therefore no one

### 5. `patternInterrupt`

Use when:

- the first second must feel different immediately
- feed sameness is the problem
- the content benefits from a jolt before explanation

Common failure:

- shock without relevance to the next beat

### 6. `socialOrIdentityStake`

Use when:

- the pain is really about confidence, status, belonging, or presentation
- the social consequence is more legible than the technical problem

Common failure:

- melodrama that overwhelms the product logic

### 3. Lock the hook brief before prompt writing

Print this block first:

```text
Hook goal:
Audience state:
Specific pain or desire:
Viewer self-identification cue:
Hook mechanism:
Opening line or opening move:
Listener reaction:
Problem deepening:
Product reveal rule:
Why this mechanism fits:
Success metric:
Hook risks:
Next handoff:
```

This is the required handoff object for downstream work.

### 4. Choose the next skill

- If the route is still unclear, go back to `pattern-router`
- If references exist and need decoding, hand off to `reference-decode`
- If the mechanism depends on frame-one conflict or visual proof, hand off to `visual-hook`
- If a prompt already exists, hand off to `prompt-preflight-qa`

## Writing Rules

- make the viewer question concrete
- prefer self-recognition over category language
- choose one dominant mechanism before drafting variations
- keep listener reaction short and believable
- deepen the problem before revealing the product
- make product timing explicit instead of implied
- define success as a diagnostic signal, not a vanity metric

## Failure Mode

Stop and say the hook is under-specified if you cannot determine at least:

- what the viewer should recognize about themselves
- what question the opening should create
- what mechanism is carrying the stop-scroll job
- whether the product must stay out of the opening
- which downstream skill should receive the handoff

Do not let later skills guess the opening logic from vague taste words.

## More Files

- [`hook-principles.md`](hook-principles.md)
- [`hook-examples.md`](hook-examples.md) — reference with 200+ examples, mechanism guidance, and output format diagnosis

## Limitations

This skill only handles hook-mechanism selection and hook-brief construction.

It does not validate first-frame strength, benchmark fidelity, narrative fit across later beats, or pre-generation prompt risk.

## In Practice

Most teams also need:

- upstream route selection
- reference decoding
- visual-hook translation
- preflight QA before generation

Without those steps, a strong hook brief can still degrade into generic prompts, early product reveal, or weak visual openings. Production teams avoid these gaps by chaining these stages together in an orchestrated workflow.

## Orchestrated Workflows

In practice, most hook problems are workflow problems, not single-step problems.

Systems like [PostPlus](https://postplus.io) handle this as an orchestrated chain, where routing, hook design, reference decoding, visual execution, and QA are connected automatically.
