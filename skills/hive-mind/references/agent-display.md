# Native agent activity and task checklists

Use this reference for the HiveMind display in hosts that expose agent and plan tools. Inspect the tools supplied in the current session before applying these examples.

## Choose the available display

| Available capability | Action |
| --- | --- |
| Native delegation and separate plans per agent thread | Spawn useful specialists and let each maintain its own checklist; keep the coordinator's integration plan separate. |
| Native delegation and a shared or unverified plan scope | Spawn useful specialists; the coordinator alone maintains owner-prefixed steps and incorporates worker progress reports. |
| Native delegation without a plan tool | Use the real agent panel plus concise text updates for specific work and blockers. |
| Plan tool without permitted delegation | Use one assistant's plan and disclose that no subagents were launched. |
| Neither capability | Give a brief text status when useful; never describe separate review passes as independent agents. |

## Native tool mapping

In a session exposing `collaboration.spawn_agent`, start a named assignment through that tool. Keep the returned agent ID or canonical task name. Use `send_message`, `followup_task`, `list_agents`, `wait_agent`, and interruption or closure only when those capabilities exist and their documented behavior fits the action. Other hosts use other names. Follow the live tool schema, including invocation routing, context, model, and concurrency restrictions.

Where `update_plan` is available, use it for the checklist. Use only its accepted status values. If it supports only pending, in_progress, and completed, describe blockers in its explanation or step text, leave unfinished steps pending, and explain the next action. Do not invent a blocked or cancelled status. Do not mark unfinished work completed to make the card look done.

A successful spawn proves an agent was created. It does not prove that the client rendered a particular panel. A successful plan update proves the tool accepted the plan. It does not prove that each thread has an isolated checklist. Confirm plan scope from host documentation or observed behavior; while uncertain, let the coordinator be the sole writer.

## Required visible-work assignment

Include these fields with the normal specialist assignment:

- Display task name: a short name describing the assigned work.
- Work steps: the small set of concrete outcomes the agent owns.
- Plan ownership: either the agent's separate native plan or progress reports for the coordinator's shared plan.
- Progress reports: the step started, the step finished and its evidence, and any blocker.
- Completion: findings, artifacts, checks performed, unresolved work, and final assignment status.

When an agent owns a separate native plan, have it publish the plan before substantive work, update it after meaningful transitions, and reconcile the checklist before its final handoff. All steps belong to its assignment; do not copy the coordinator's full plan into every agent's checklist.

For a shared plan, use labels such as "Evidence review: check citations" and "Quality review: inspect the final draft." Keep waiting work pending, and change completed status only after the corresponding handoff supports it. If several agents work at once but the plan permits only one in-progress step, use a single active coordination step for that wave and track the distinct assignments in its explanation or the native agent panel.

## Finish and verify

Check actual agent results against the requested outcome before closing the coordinator's integration step. Keep successful assignments, failures, cancellations, blockers, and unfinished checks distinct in the summary.

If the user asks whether the display works, distinguish:
1. Native agents were launched and returned results.
2. The planning tool accepted status updates.
3. The user or another supported observation confirmed the rendered cards.

Report only the levels verified. Exact styling and whether a card appears in the main thread or inside an agent thread depend on the host. Do not change permissions, install infrastructure, or create a custom application to imitate the native card.

The official [ChatGPT and Codex subagents guide](https://learn.chatgpt.com/docs/agent-configuration/subagents) describes native activity, agent threads, and Active and Done lists. Treat the current host's tools as authoritative for execution.
