# Cyber Emperor Skill

A practical OpenClaw skill for orchestrating complex work with a "Three Departments and Six Ministries" multi-agent model.

## What this repository contains

- `skills/cyber-emperor/SKILL.md` — the main skill definition
- `skills/cyber-emperor/README.md` — a short companion overview

## Core idea

`cyber-emperor` is not just “spawn more agents”. It is a governance/orchestration layer for complex tasks:

- **Zhongshu Sheng** — planning and task decomposition
- **Menxia Sheng** — review, correction, and delivery judgment
- **Shangshu Sheng** — dispatch, aggregation, and closeout
- **Six Ministries** — role assignment, scope control, standards, execution, validation, and delivery

It is designed to work together with:

- `sessions_spawn` for actual subagent dispatch
- `shadow-clone` for parallel execution structure
- `claude-code-hook` for zero-polling complex coding work

## When to use

Use it for:

- medium/large project work
- multi-module changes
- multi-stage delivery
- tasks that require planning, implementation, testing, and documentation

Avoid it for:

- tiny edits
- pure Q&A
- tasks that are faster to do directly than to orchestrate

## Repository structure

```text
skills/
  cyber-emperor/
    SKILL.md
    README.md
```

## Publishing notes

This repository is intended as a standalone GitHub home for the Cyber Emperor skill, with documentation suitable for reuse and future expansion.
