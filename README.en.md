# Cyber Emperor

`cyber-emperor` is a practical OpenClaw skill for orchestrating complex work through a governance-first multi-agent model inspired by the traditional "Three Departments and Six Ministries" structure.

It is **not** just about spawning more agents. It is about turning messy work into a disciplined execution flow:
- planning
- review
- dispatch
- parallel execution
- validation
- delivery

## Repository Contents

- `README.md` — bilingual landing page
- `README.zh-CN.md` — Chinese documentation
- `README.en.md` — English documentation
- `skills/cyber-emperor/SKILL.md` — the main skill definition
- `skills/cyber-emperor/README.md` — a short companion overview

## Core Positioning

`cyber-emperor` is a **governance / orchestration framework**:
- **Zhongshu Sheng** — planning and task decomposition
- **Menxia Sheng** — review, correction, and risk control
- **Shangshu Sheng** — dispatch, aggregation, and closeout
- **The Six Ministries** — role assignment, scope control, standards, execution, validation, and delivery

It is designed to work together with:
- `sessions_spawn` for real subagent dispatch
- `shadow-clone` for parallel execution structure
- `claude-code-hook` for zero-polling complex coding tasks

## Good Fit

Use it for:
- medium and large tasks
- multi-module or multi-stage collaboration
- work that needs planning, implementation, testing, documentation, and unified delivery
- complex coding and project-level orchestration

Avoid it for:
- tiny single-file edits
- pure lookup / Q&A tasks
- work that can be finished directly in a few minutes
- cases where orchestration costs more than it helps

## Design Rules

1. The main session should orchestrate instead of doing all detailed execution itself
2. Subagents must be actually spawned instead of being “simulated” in words
3. Complex coding should be routed to `claude-code-hook`
4. Multiple subagents should not edit the same critical file at once
5. There must be a validation layer and a unified delivery layer

## Public Publishing Rule

This is a public repository and must not contain any secrets, tokens, passwords, private keys, cookies, or other credentials.

Share methods, not keys.

## License

This repository is released under a **Custom Non-Commercial License**. You may view, study, copy, and modify the contents for personal, educational, research, and other non-commercial purposes. **Commercial use, commercial distribution, and use in paid products or services require prior written authorization.** See [LICENSE.md](./LICENSE.md).

## Next Steps

You can expand this repository into a broader public skill collection with:
- more skills
- reusable task templates
- demo screenshots
- changelogs
