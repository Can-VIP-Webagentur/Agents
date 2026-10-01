---
name: agent-orchestration
description: "Use when deciding whether to delegate a substantial task to multiple Codex agents, coordinating independent work in parallel, or integrating their results."
---

# Agent Orchestration

For each substantial task, decide whether multiple agents would improve speed or coverage. Delegate automatically when the work separates into independent pieces and a subagent capability is available. Handle the task directly when it is small, tightly sequential, or has shared-file conflicts that would cost more to coordinate than to do serially.

## Decide what to delegate

- Look for work that can proceed independently, such as separate read-only investigations, focused reviews, or implementation in clearly separate files.
- Use the smallest useful number of agents. Usually two or three are enough; never create agents without a distinct deliverable.
- Keep dependent steps in order. Do not delegate a task that depends on facts or edits not available yet.
- Keep work with shared-file edits under one owner. If parallel edits are necessary, assign disjoint files and tell each agent exactly what it owns.
- If the current Codex environment has no subagent tool, continue without delegation.

## Assign work clearly

Give each agent a narrow task with the relevant background, constraints, files or areas to inspect, and the result format you need. Say whether it may edit files or must stay read-only. Ask it to report findings, changed files, and unresolved questions without taking on adjacent work.

## Coordinate and integrate

Stay responsible for the complete result. Track delegated tasks, review their findings and diffs, resolve conflicting recommendations, and integrate the useful work. Verify important claims against the repository or source material. Do not report an agent's claim as verified until you have checked it.

Follow the user's scope and existing permissions. Agents must not publish, deploy, send messages, change external systems, or make other external changes unless the user explicitly authorized that action. Do not add or run tests unless the user asks for tests.

In the final response, summarize the completed result. Mention delegated work only when it helps the user understand the result or its verification.
