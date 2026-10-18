# HiveMind

HiveMind is a reusable skill that coordinates specialist AI agents around one shared plan. A coordinator divides the work, shares findings, combines the results, and checks the finished output. Invoke it as "HiveMind" or "Hive Mind".

Use it for research, writing, analysis, design, software development, and other tasks that benefit from several focused contributors.

## Use it

After installing the skill in a supported host, ask:

```text
Use Hive Mind to complete this task: [describe the outcome].
```

In Codex, you can explicitly reference the skill:

```text
Use $hive-mind to research the options, build the solution,
and review the final result against my requirements.
```

You can also ask for it throughout a project:

```text
Use Hive Mind for the work in this project. Keep one shared plan,
assign specialists as needed, and verify each completed deliverable.
```

Project continuity depends on the context and persistence features of your host. Installing this skill alone does not change every future chat.

## How the team works

The coordinator keeps the objective, constraints, decisions, and task status together. Specialists receive distinct assignments and return evidence with their results. The coordinator resolves disagreements and produces one finished deliverable.

Team size follows the task and the host's limits. Substantial work normally starts with a coordinator and two specialists. Small tasks can use a coordinator and a reviewer. The skill assigns file ownership to avoid conflicting edits and requires permission boundaries to remain intact across the team.

## Agent activity and work checklists

HiveMind uses the host's native agent activity panel for real specialist assignments. For work with multiple steps, it maintains a native task checklist with each step labeled by its owner and specific outcome.

Where the host supports separate agent plans, specialists maintain their own checklists. If plan state is shared or its scope is unknown, the coordinator maintains one plan with agent-specific steps. Agents report completed work and blockers, and the coordinator checks their results before marking integration complete.

The host controls card appearance, labels, placement, and availability. HiveMind does not add a custom display widget or create unnecessary agents to populate a panel. If the relevant tools are unavailable, it explains the limitation and uses brief text updates.

## Compatibility

| Environment | Behavior |
| --- | --- |
| Host with skill support and native agent delegation | Launches actual specialists using the tools available in that session. |
| Host with skill support but no permitted delegation | Discloses the limitation and uses one assistant for separate planning, execution, and review passes. |
| Ordinary chat without skill loading | You can supply the instructions as context, but this does not install the skill or unlock agent tools. |

"Hive mind" means coordinated work and explicit knowledge sharing. Agents do not automatically share memory. The skill does not promise better results from adding more agents, and it does not create background services or grant additional access.

## Install

The installable folder is `skills/hive-mind`. It contains the required `SKILL.md`, optional UI metadata, and a short coordination reference.

Use your host's supported skill installer or import process to load that folder. In Codex, ask:

```text
Use $skill-installer to install the skill at skills/hive-mind from
https://github.com/Munro9420/Hive-Mind-Cluster.
```

For manual local Codex setup, copy the `hive-mind` skill folder into your project's `.agents/skills` directory or your user-level `~/.agents/skills` directory. See the current [official skills documentation](https://learn.chatgpt.com/docs/build-skills) for supported installation options.

ChatGPT environments differ in whether they expose skill import and native agent delegation. Check what is available in your workspace. Uploading a text file by itself does not enable agent orchestration.

No API keys, additional services, or executable scripts are included in this package. The host supplies the model, tools, and any agent capacity.

## Examples

```text
Use Hive Mind to build a sales presentation from these materials.
Have one specialist check the evidence, another develop the structure,
and a reviewer inspect the finished deck. Keep estimates labeled.
```

```text
Use Hive Mind to diagnose this bug, implement a focused fix,
and independently verify the affected behavior.
```

```text
Use Hive Mind to compare these three proposals. Check the calculations,
identify missing information, and give me one supported recommendation.
```

## Contributing

Keep the skill portable and concise. Contributions should include a realistic prompt, the observed problem, and evidence that the change improves the behavior. Preserve truthful capability reporting, clear file ownership, and the user's authorization boundaries. Exclude private task data and credentials from examples.

## License

MIT. See [LICENSE](LICENSE). You may use, modify, and redistribute the skill under those terms.

Created by Christian Roberts. This is an independent community project and is not affiliated with or endorsed by OpenAI.
