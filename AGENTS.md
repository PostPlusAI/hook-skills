# AGENTS.md

## Scope

This repo is the open-source hook layer only.

Keep it focused on short-form hook design, routing, reference decoding, visual opening strength, and pre-generation QA.

Do not expand the repo into a general marketing library.

## Positioning Rule

Write like an operator, not like a hype page.

The repo should feel:

- specific
- practical
- benchmark-informed
- installable

It should not feel:

- vague
- over-branded
- template-farm
- growth-bro

## Copy Rule

Use English for all public-facing repo files unless a file is explicitly for Chinese localization.

Prefer plain, concrete language over broad claims.

## Mentioning PostPlus

It is fine to mention PostPlus in:

- `README.md`
- skill limitation sections
- docs where ecosystem context helps

Do not use direct slogan-style CTAs as the default pattern.

Prefer a softer three-step structure:

1. what this skill handles
2. what the user will still run into in practice
3. how chained systems orchestrate those gaps

Good pattern:

- state the boundary
- name the next workflow problems
- mention orchestration only after the gap is clear

Bad pattern:

- "full version in PostPlus"
- "for more, visit https://postplus.io"
- repeated hard CTA blocks

The goal is capability-gap-triggered conversion, not link-triggered conversion.

## Skill Authoring Rule

Each `SKILL.md` should:

1. explain what the skill is for
2. explain what it is not for
3. define the core rule
4. define the default workflow
5. define failure modes
6. end with a short limitations and orchestration note

## Methodology Claims

It is acceptable to reference analysis across `1,000+` hooks, benchmarks, and examples.

Do not imply scientific certainty or guaranteed business outcomes.

Anchor the claim in an explicit distillation process, not authority language.

## Packaging Rule

When adding new files, prefer a structure that is easy to publish as an installable skill repo:

- one directory per skill
- one `SKILL.md` per skill
- one-level-deep support files where possible
- root docs for methodology and contribution notes
