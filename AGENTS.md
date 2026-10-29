# Repository guidance for coding agents

This public repository is a **study toolkit**, not a project containing the real SK hynix exam task.

## Read first
- `README.md`: scope and security.
- `START_PROMPT.md`: requested Codex starter prompt.
- `SKILL_TREE.md`: Korean purpose-first selection map, relevant/irrelevant conditions and Cofa prohibited actions.\n- `SKILLS.md` and `PLUGINS.md`: link catalog, not installed capabilities.
- `WORKFLOW.md` and `CHECKLIST.md`: optional practical guidance.

## Work safely
1. The actual exam task's README and the current Cofa instructions take priority over these notes.
2. Never assume that a linked repository, Plugin or `SKILL.md` has been fetched, installed or enabled. Verify access and report uncertainty.
3. Select only a relevant, permitted workflow. Do not add unrelated features, external services, agents or dependencies.
4. Check commands and any network or write action before execution; do not weaken sandbox controls, perform prohibited Computer Use, connect a separate AI model or update Codex.
5. Do not push/exfiltrate exam inputs, code, outputs, screenshots, candidate URLs, tokens, credentials, or personal information to this repository or other external locations. Never expose real task material in a public commit.
6. Test actual output before claiming completion; distinguish observed success from untested assumptions.
7. If an action might conflict with the latest Cofa rules, stop that action and explain the restriction. The later official email overrides older conflicting guides.
8. Keep output compact for narrow terminal displays; provide file paths and evidence rather than long repetitive chat text.

## Local original skills (Korean labels in `agents/openai.yaml`)
- `.agents/skills/check-before-submit/SKILL.md`
- `.agents/skills/find-and-fix-errors/SKILL.md`
- `.agents/skills/check-data-errors/SKILL.md`

These are lightweight original study instructions, not copied third-party Plugin code. Repo-local skills or `AGENTS.md` are **not automatically available merely because a URL was pasted**; discovery depends on the allowed runtime, clone/workspace location and tool support. Do not claim Cofa compatibility without testing.

**Important:** The 6 later exam written answers must be completed by the candidate without AI.
