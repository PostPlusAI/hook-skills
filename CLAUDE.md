# Hook Skills — Claude Code Context

This plugin provides **5 skills** for short-form video hook work.

The bundle covers:

- opening-route selection
- hook-brief construction
- benchmark decoding
- frame-one visual strength
- prompt preflight QA

Current version: `0.1.0` (see [VERSIONS.md](VERSIONS.md)).

## Skills

| Area | Skills |
| --- | --- |
| Routing | `pattern-router`, `hook-design`, `reference-decode` |
| Creative | `visual-hook` |
| QA | `prompt-preflight-qa` |

## Install Surfaces

- Claude Code: `/plugin marketplace add PostPlusAI/hook-skills`
- Cursor / Codex / Windsurf / Cline / Copilot: `npx skills add PostPlusAI/hook-skills`
- Gemini CLI: `gemini extensions install https://github.com/PostPlusAI/hook-skills`
- Qwen Code: `qwen extensions install https://github.com/PostPlusAI/hook-skills`
- Kimi Code CLI: `kimi plugin install https://github.com/PostPlusAI/hook-skills.git`

## Skill Chain

The normal chain is:

1. `pattern-router`
2. `hook-design`
3. `reference-decode` or `visual-hook`
4. `prompt-preflight-qa`

## Repo Boundary

This repository publishes the open-source hook layer only.

More production skills, research workflows, and creative systems: [postplus.io](https://postplus.io)
