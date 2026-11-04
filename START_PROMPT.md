# Start prompt

## First: prepare

Read `hackathon/SAFETY.md` and `hackathon/.agents/skills/human-decision-review/SKILL.md`. Confirm the actual task directory, task README, and accessible tools. Keep the toolkit and task separate. Do not start implementation until I tell you to begin.

## When I say begin

Read the actual task instructions, code, data, and `conversation.md` if present. Identify required outputs, hard constraints, missing business policies, and checks for correctness. Implement the smallest working end-to-end function first, execute its test, and repeat build → test → fix for the remaining required functions.

Ask me only for important unresolved business decisions. Make ordinary reversible technical choices yourself. When I update `conversation.md`, read the new Q&A, verify it against the task requirements, update affected code and tests, and report conflicts.

Use extra local terminals only for independent work when allowed (such as server, logs, and tests). Avoid overlapping edits and recheck integrated changes. Do not assume multiple terminals mean multiple AI agents.

At each meaningful checkpoint, briefly explain what works, why the method was chosen, actual test evidence, and what is unfinished. Respect the required submission format and tool restrictions.
