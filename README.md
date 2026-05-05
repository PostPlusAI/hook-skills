# Hook Skills

**5 open-source skills for stronger short-form video hooks.**

Hook Skills is a focused skill pack for designing, decoding, routing, and QA-ing short-form video hooks.

It is built for TikTok, Reels, Shorts, UGC ads, AI video workflows, and any creative system where the first 1-3 seconds decide whether the viewer keeps watching.

This repo packages the hook layer only:

- choose the right opening route
- turn vague ideas into a stable hook brief
- decode benchmark references into reusable opening logic
- design stronger visual openings
- QA prompts before spending generation credits

## Why This Exists

Most short-form videos do not fail because the body is bad.

They fail because the opening does not create a concrete viewer question before the content feels like an ad.

We built these skills to make hook work less fuzzy and more operational:

- mechanism before wording
- product reveal timing before product hype
- visible conflict before visual polish
- reusable diagnosis before random inspiration

## What Is Inside

### Routing

- [`pattern-router`](routing/pattern-router/SKILL.md)  
  Choose the right opening route before prompt writing starts.

- [`hook-design`](routing/hook-design/SKILL.md)  
  Turn a rough idea into a reusable `Hook Brief`.

- [`reference-decode`](routing/reference-decode/SKILL.md)  
  Distill benchmark clips and frames into reusable opening structure.

### Creative

- [`visual-hook`](creative/visual-hook/SKILL.md)  
  Strengthen frame one, first slide, or first 1-3 seconds.

### QA

- [`prompt-preflight-qa`](qa/prompt-preflight-qa/SKILL.md)  
  Catch weak openings, early product reveal, and prompt drift before generation.

## How We Distilled It

This repo is informed by analysis across **1,000+ short-form hooks, benchmark openings, and hook-adjacent prompt examples**.

The working method:

1. Collect winning and failed opening examples across short-form formats.
2. Group them by stop-scroll job, not by niche or surface wording.
3. Compare viewer question, product timing, visible proof, and self-recognition.
4. Extract reusable opening mechanisms and failure patterns.
5. Package those judgments into installable skills instead of a swipe file.

Read the full write-up in [`docs/methodology.md`](docs/methodology.md).

## Quick Start

| Tool | Install |
| --- | --- |
| Claude Code | `/plugin marketplace add PostPlusAI/hook-skills` |
| OpenClaw | `clawhub install PostPlusAI/hook-skills` or bundle |
| Gemini CLI | `gemini extensions install https://github.com/PostPlusAI/hook-skills` |
| Qwen Code | `qwen extensions install https://github.com/PostPlusAI/hook-skills` |
| Amp | `amp skill add PostPlusAI/hook-skills` |
| Kimi Code CLI | `kimi plugin install https://github.com/PostPlusAI/hook-skills.git` |
| CodeBuddy | `/plugin marketplace add PostPlusAI/hook-skills then /plugin install postplus-hook-skills` |
| Cursor / Codex / Windsurf / Cline / Copilot / 35+ agents | `npx skills add PostPlusAI/hook-skills` |

Install one skill:

```bash
npx skills add PostPlusAI/hook-skills -s hook-design
```

The repository includes the marketplace and extension manifests needed for these install surfaces.

## Try These Requests

```text
Turn this rough opening into a stronger hook brief
```

```text
The product appears too early. Fix the hook logic first
```

```text
Decode this benchmark into a reusable opening structure
```

```text
Review this prompt before we spend credits on generation
```

## Pipeline

```
                        ┌──────────────────────┐
                        │     Raw input         │
                        │  (brief / references  │
                        │   / prompt draft)     │
                        └──────────┬───────────┘
                                   │
                                   ▼
                   ┌───────────────────────────┐
                   │      pattern-router       │
                   │                           │
                   │  Routes the opening job:  │
                   │  segment type, viewer     │
                   │  question, product rule   │
                   │                           │
                   │  Output: Route Summary    │
                   └──────────┬───────────────┘
                              │
                              ▼
                   ┌───────────────────────────┐
                   │       hook-design         │
                   │                           │
                   │  Locks mechanism +        │
                   │  product timing. Reads    │
                   │  hook-principles.md +     │
                   │  hook-examples.md for     │
                   │  reference.               │
                   │                           │
                   │  Output: Hook Brief       │
                   └──────────┬───────────────┘
                              │
              ┌───────────────┴────────────────┐
              │                                │
              ▼                                ▼
 ┌──────────────────────┐       ┌──────────────────────┐
 │   reference-decode   │       │     visual-hook      │
 │                      │       │                      │
 │  When benchmarks or  │       │  When frame-one or   │
 │  references exist:   │       │  first 3 s need      │
 │  extract essence,    │       │  visual strength:    │
 │  viewer question,    │       │  map hook mechanism  │
 │  grammar, drift      │       │  to visual family    │
 │  boundaries          │       │                      │
 └──────────┬───────────┘       └──────────┬───────────┘
            │                              │
            └──────────────┬───────────────┘
                           │
                           ▼
                  ┌──────────────────────────┐
                  │   prompt-preflight-qa    │
                  │                          │
                  │  Pre-generation check:   │
                  │  opening strength,       │
                  │  product timing, drift   │
                  │  risk, missing fields    │
                  │                          │
                  │  Output: Verdict + Fixes │
                  └──────────┬───────────────┘
                             │
                             ▼
                  ┌──────────────────────────┐
                  │  Ready for image /       │
                  │  video generation        │
                  └──────────────────────────┘
```

**Reference files (in `routing/hook-design/`):**

```
hook-principles.md    6 mechanism definitions, product reveal rules,
                      common failure patterns

hook-examples.md      200+ example sentences organized by mechanism,
                      3 complete Hook Brief diagnosis examples,
                      appendices (FAQ, tips, niche references)
```

The goal is not to generate more hook ideas. The goal is to make the opening logic explicit enough that downstream prompt writing does not have to guess.

## Repo Structure

```text
hook-skills/
├── routing/
│   ├── pattern-router/
│   ├── hook-design/
│   └── reference-decode/
├── creative/
│   └── visual-hook/
├── qa/
│   └── prompt-preflight-qa/
├── .claude-plugin/
├── .codebuddy-plugin/
└── docs/
    └── methodology.md
```

## Positioning

This is the open-source hook layer.

It is intentionally narrow, practical, and easy to install.

More production skills, research workflows, and creative systems: [postplus.io](https://postplus.io)

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Versioning

See [`VERSIONS.md`](VERSIONS.md).
